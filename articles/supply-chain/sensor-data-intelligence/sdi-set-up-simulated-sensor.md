---
title: اعداد أداه استشعار محاكيه للاختبار
description: توضح هذه المقالة كيفيه إعداد المحاكي الذي يمكنك استخدامه لاختبار معلومات ‏‫الوظيفة الإضافية Sensor Data Intelligence‬ من دون تثبيت أيه أدوات استشعار فعليه.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: f12d6e1d417a260477b1eb4e027b850d1862f51f
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689794"
---
# <a name="set-up-a-simulated-sensor-for-testing"></a>اعداد أداه استشعار محاكيه للاختبار

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

إذا كنت ترغب في اختبار معلومات بيانات الاستشعار من دون تثبيت أيه أدوات استشعار فعليه، فيمكنك استخدام خدمة *المحاكي Raspberry PI Azure IoT عبر الإنترنت* لمحاكاة إشارات الاستشعار وإرسالها إلى حل إنترنت الأشياء الخاص بك ( IoT) علي Microsoft Azure. لمزيد من المعلومات حول المحاكي، راجع [اتصال Raspberry Pi عبر الإنترنت لمركز Azure IoT (Node.js)](/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started).

## <a name="video-instructions"></a>تعليمات الفيديو

يوضح الفيديو التالي كيفيه اعداد أداه استشعار محاكيه للاختبار. توفر الأقسام المتبقية في هذه المقالة نفس الإرشادات بتنسيق مستند إلى النص.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE588g6]

## <a name="create-a-device-in-azure-iot-hub"></a>إنشاء جهاز في مركز Azure IoT

يجب أولاً إعداد جهاز لمصادقة إشارات الاستشعار علي مركز Azure IoT.

1. في Azure، انتقل إلى قائمه الموارد الخاصة بمجموعه الموارد التي قمت بإنشاءها للاستخدام مع ‏‫الوظيفة الإضافية Sensor Data Intelligence‬. (لمزيد من المعلومات، راجع [نشر حل IoT علي Azure](sdi-deploy-iot-solution-on-azure.md).)
1. في قائمه الموارد، ابحث عن السجل حيث تم تعيين حقل **النوع** إلى *مركز IoT*. في عمود **الاسم** حدد الاسم لفتح صفحة البيانات الخاصة بالموارد.
1. في جزء التنقل الأيسر، حدد **الأجهزة**.
1. في صفحة **الأجهزة** ، حدد **إضافه جهاز**.
1. في صفحة **إنشاء جهاز** ، قم بتعيين الحقول التالية:

    - **معرف الجهاز** – أدخل اسمًا للجهاز الجديد (علي سبيل المثال ، *جهاز IoT الخاص بي*).
    - **نوع المصادقة** – حدد *المفاتيح المتماثلة*.
    - **إنشاء المفاتيح تلقائيًا**- حدد خانه الاختيار هذه.
    - **قم بتوصيل هذا الجهاز بمركز IoT** - حدد *تمكين*.

1. حدد **موافق** للعودة إلى صفحة **الأجهزة**.
1. ابحث عن الجهاز الجديد في القائمة في عمود **معرف الجهاز** حدد الاسم لفتح صفحة البيانات الخاصة بالجهاز. إذا لم تر الجهاز الجديد في القائمة، فقم بتحديث الصفحة.
1. قم بنسخ قيمة **‬‏‫سلسلة الاتصال الأساسية** (علي سبيل المثال ، عن طريق تحديد الزر **نسخ إلى الحافظة** ). ستحتاج إلى هذه القيمة لاحقا عندما تقوم باعداد محاكيRaspberry Pi IoT لمحاكاة إشارات أداة الاستشعار. لذلك، خذ بعين الاعتبار اللصق في ملف نصي من الآن.

## <a name="add-the-azure-connection-string-to-the-raspberry-pi-iot-simulator"></a>إضافه سلسله اتصال Azure إلى محاكي Raspberry Pi IoT

اتبع هذه الخطوات لإضافة سلسلة الاتصال من الجهاز في مركز Azure IoT إلى البرنامج النصي الموجود في خدمه Raspberry.

1. يستخدم هذا الزر في [فتح محاكيRaspberry Pi IoT](https://azure-samples.github.io/raspberry-pi-web-simulator/).
1. في الجزء محرر التعليمات البرمجية، ابحث عن السطر الذي يحتوي علي الأمر التالي.

    `const connectionString = '[Your IoT hub device connection string]';`

1. استبدال نص التعليمات، بما في ذلك الأقواس ، مع قيمة **سلسلة الاتصال الاساسيه** التي قمت بنسخها في المقطع السابق. تشبه النتيجة المثال التالي.

    `const connectionString = 'HostName=XXX;DeviceId=YYY;SharedAccessKey=ZZZ';`

## <a name="add-sensor-ids-and-values-to-the-payload-in-the-raspberry-pi-iot-simulator"></a>إضافه معرفات وقيم أداة الاستشعار إلى الحمولة في محاكي Raspberry Pi IoT

يجب عليك الآن اعداد محاكيRaspberry Pi IoT مع أدوات الاستشعار التي تمت محاكاتها والقيم التي سيتم إرسالها كبايلوادس.

- في محرر التعليمات البرمجية لمحاكي Raspberry Pi IoT، ابحث عن الوظيفة `getMessage` ، وقم بتحريرها بحيث تتطابق مع التعليمات البرمجية التالية. (يتم إعداد أدوات الاستشعار في البنود `cb()` .)

    ```cpp
    function getMessage(cb) {
        messageId++;
        sensor.readSensorData()
        .then(function (data) {
            cb(JSON.stringify({ value: 1, sensorId: 'MachineStatus' }), false);
            cb(JSON.stringify({ value: 70, sensorId: 'Quality' }), false);
            cb(JSON.stringify({ value: 1, sensorId: 'AssetMaintenance' }), false);
            cb(JSON.stringify({ value: 1, sensorId: 'ProductionDelay' }), false);
            cb(JSON.stringify({ value: 20, sensorId: 'AssetDowntime' }), false);
        })
        .catch(function (err) {
            console.error('Failed to read out sensor data: ' + err);
        });
    }
    ```

    > [!IMPORTANT]
    > يجب ان تكون معرفات أدوات الاستشعار المحددة في محرر الكود لمحاكي راسببيري Pi إيوت مطابقه لمعرفات المجس التي ستقوم بتحديدها فيما بعد للسيناريوهات الموجودة في Supply Chain Management. تستخدم التعليمة البرمجية الموجودة في المثال السابق معرفات أداه الاستشعار القابله للقراءة البشرية. ومع ذلك، في السيناريو الفعلي، ستكون معرفات أداه الاستشعار عبارة عن قيم المعرف الفريد العمومي (GUID) التي يتم توفيرها بواسطة الشركة المصنعة لأداه الاستشعار. يتم أيضا استخدام معرفات أداه الاستشعار لقابليه القراءة البشرية المستخدمة في هذا المثال في الامثله الموجودة في [سيناريو جودة الإنتاج](sdi-scenario-product-quality.md), [وسيناريو صيانة الأصل](sdi-scenario-asset-maintenance.md), [وسيناريو تأخير الإنتاج](sdi-scenario-production-delays.md), and [وسيناريو حالة الجهاز](sdi-scenario-equipment-downtime.md)). ولذلك، استخدم هذا الكود إذا كنت ستعمل خلال هذه السيناريوهات.

## <a name="edit-the-interval-for-sending-sensor-signals"></a>تحرير الفاصل الزمني لإرسال إشارات الاستشعار

يجب ان تقوم الآن بتعيين الفترة التي يجب ان يرسل فيها محاكي Raspberry Pi IoT إشارات الاستشعار التي تمت مضاهاتها.

1. في محرر الكود الخاص بمحاكي Raspberry Pi IoT، ابحث عن استدعاء الدالة التالية.

    `setInterval(sendMessage, 2000);`

2. وبشكل افتراضي، يرسل محاكي Raspberry Pi IoT إشاره الاستشعار كل 2,000 مللي ثانيه (ثانيتين). يمكنك تعديل القيم كما تقتضي الحاجة.

## <a name="run-the-raspberry-pi-iot-simulator"></a>تشغيل محاكيRaspberry Pi IoT.

- حدد **تشغيل** لبدء المحاكي وأبدا في إرسال بيانات أداه الاستشعار التي تمت محاكاتها.
