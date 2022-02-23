---
title: تكوين تكامل Common Data Service
description: يُمكنك تشغيل التكامل بين Common Data Service وDynamics 365 Human Resources أو إيقاف تشغيله. يُمكنك أيضًا عرض تفاصيل المزامنة، ومسح بيانات التعقب، وإعادة مزامنة كيان للمساعدة في استكشاف الأخطاء في مشاكل البيانات وإصلاحها بين البيئتين.
author: andreabichsel
manager: AnnBe
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d9ee4715526e18b33ae4b7e90b081ed5868bb19c
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527900"
---
# <a name="configure-common-data-service-integration"></a>تكوين تكامل Common Data Service

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يُمكنك تشغيل التكامل بين Common Data Service وDynamics 365 Human Resources أو إيقاف تشغيله. يُمكنك أيضًا عرض تفاصيل المزامنة، ومسح بيانات التعقب، وإعادة مزامنة كيان للمساعدة في استكشاف الأخطاء في مشاكل البيانات وإصلاحها بين البيئتين.

عند إيقاف تشغيل التكامل، يُمكن للمستخدمين إجراء تغييرات في Human Resources أو Common Data Service، ولكن لا تتم مزامنة هذه التغييرات بين البيئتين.

بشكل افتراضي، يكون التكامل بين Human Resources وCommon Data Service متوقفًا عن التشغيل.

قد ترغب في إيقاف تشغيل التكامل في هذه الحالات:

- تقوم بتعبئة البيانات من خلال Data Management Framework ويجب عليك استيراد البيانات عدة مرات للوصول إلى حالة صحيحة.

- توجد مشاكل في البيانات إما في Human Resources أو Common Data Service. إذا قمت بإيقاف تشغيل التكامل، يُمكنك حذف سجل في إحدى البيئات دون حذفه في الآخر. عند تشغيل التكامل مرة أخرى، سوف تتم مزامنة السجل الموجود في البيئة التي لم يتم حذفه فيها مرة أخرى إلى البيئة التي تم حذفه فيها. تبدأ المزامنة في المرة التالية التي يتم فيها تشغيل الوظيفة الدفعية **مزامنة طلب تكامل Common Data Service المفقود**.

> [!WARNING]
> عند إيقاف تشغيل تكامل البيانات، تأكد من أنك لم تقم بتحرير نفس السجل في كلتا البيئتين. عند تشغيل التكامل مرة أخرى، سوف تتم مزامنة آخر سجل قمت بتحريره. وبالتالي، إذا لم تقم بإجراء نفس التغييرات على السجل في كلا البيئتين، فقد يؤدي ذلك إلى فقد البيانات.

## <a name="access-the-common-data-service-integration-page"></a>الوصول إلى صفحة تكامل Common Data Service

1. في مثيل Human Resources الذي ترغب في عرض أو تكوين إعدادات للتكامل مع Common Data Service فيه، حدد التجانب **إدارة النظام**.

    [![تجانب إدارة النظام](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)

2. حدد علامة التبويب **الارتباطات**.

    [![علامة التبويب ارتباطات](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)

3. تحت **عمليات التكامل**، حدد **تكوين Common Data Service**.

    [![ارتباط تكوين Common Data Service ](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a>تشغيل تكامل البيانات بين Human Resources و Common Data Service أو إيقاف تشغيله.

- لتشغيل التكامل، قم بتعيين خيار **تمكين التكامل إلى Common Data Service** إلى **نعم**.

    > [!NOTE]
    > عند تشغيل التكامل، سوف تتم مزامنة البيانات في المرة التالية التي يتم فيها تشغيل الوظيفة الدفعية **مزامنة طلب تكامل Common Data Service المفقود**. يجب أن تكون كافة البيانات متاحة بعد اكتمال الوظيفة الدفعية.

- لإيقاف تشغيل التكامل، قم بتعيين الخيار إلى **لا**.

[![تشغيل تكامل Common Data Service أو إيقاف تشغيله](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)

> [!WARNING]
> نوصي بضرورة إيقاف تشغيل تكامل Common Data Service أثناء تنفيذ مهام ترحيل البيانات. بإمكان تحميلات البيانات الكبيرة أن تؤثر على الأداء بشكل ملحوظ. على سبيل المثال، قد يستغرق تحميل 2000 عامل ساعات متعددة عند تمكين التكامل، وأقل من ساعة عند تعطيله. الأرقام المتوفرة في هذا المثال هي لأغراء العرض التوضيحي فقط. يمكن أن يختلف مقدار الوقت الدقيق الذي تستغرقه عملية استيراد السجلات بشكل كبير استنادًا إلى العديد من العوامل.

## <a name="view-data-integration-details"></a>عرض تفاصيل تكامل البيانات

في علامة التبويب السريعة **الإدارة** في صفحة **تكامل Common Data Service**، يُمكنك رؤية كيف تكون السجلات مرتبطة ببعضها بين Human Resources وCommon Data Service.

- لعرض السجلات الخاصة بكيان ما، حدد الكيان في حقل **اسم كيان CDS**. تعرض الشبكة كافة السجلات المرتبطة بالكيان المُحدد.

[![عرض السجلات لكيان](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)

> [!NOTE]
> حاليًا، لا يتم سرد كافة كيانات Common Data Service. تظهر فقط الكيانات التي تدعم استخدام الحقول المخصصة في الشبكة. تتوفر الكيانات الجديدة من خلال الإصدارات المستمرة لـ Human Resourcesـ. 

تتضمن الشبكة الحقول التالية:

- **اسم كيان CDS** - اسم الكيان في Common Data Service.
- **مرجع كيان CDS** - المُعرف الذي يستخدمه Common Data Service لتحديد سجل. تُكافئ هذه القيمة قيمة **RecId** لـ Human Resourcesـ. يُمكنك العثور على المُعرف عندما تقوم بفتح كيان Common Data Service في Microsoft Excel.
- **اسم كيان Human Resources** - آخر كيان قام بمزامنة البيانات إلى Common Data Service. يمكن أن يكون للكيان إما بادئة Common Data Service أو بادئة أخرى.
- **مرجع Human Resources** - قيمة **RecId** المقترنة بالسجل في Human Resources.
- **تم حذفه من CDS** - قيمة تشير إلى ما إذا كان السجل قد تم حذفه من Common Data Service أو لا.

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a>إزالة اقتران سجل في Human Resources من Common Data Service

إذا واجهت مشاكل خلال مزامنة البيانات بين Human Resources و Common Data Service، فقد تكون قادرًا على حلها عن طريق مسح التعقب والسماح بإعادة مزامنة جدول التعقب. إذا قمت بإزالة الاقتران، ثم قمت بتغيير سجل أو حذفه في Common Data Service، فلن تتم مزامنة التغييرات مع Human Resources. إذا قمت بإجراء تغييرات في Human Resources، يتم إنشاء سجل تعقب جديد، ويتم تحديث السجل في Common Data Service.

- لإزالة اقتران سجل بين Human Resources و Common Data Service، حدد الكيان في حقل **اسم كيان CDS**، ثم حدد **مسح معلومات التعقب**.

[![مسح معلومات التعقب](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)

لتشغيل مزامنة كاملة على الكيان بعد مسح التتبع، راجع الإجراء التالي.

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a>مزامنة كيان بين Human Resources و Common Data Service

استخدم هذا الإجراء في الحالات التالية:

- يستغرق ظهور التغييرات من Common Data Service في Human Resources وقتًا طويلاً.

- يجب تحديث جدول التعقب بعد مسح التعقب.

لتشغيل مزامنة كاملة على كيان بين Human Resources وCommon Data Service:

1. في حقل **اسم كيان CDS**، حدد الكيان.

2. حدد **المزامنة الآن**.

[![تشغيل مزامنة كاملة](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)


