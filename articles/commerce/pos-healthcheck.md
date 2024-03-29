---
title: التحقق من سلامة الأجهزة الطرفية وخدمات نقطة البيع
description: يقدم هذا المقال نظرة عامة على عملية فحص السلامة في نقطة البيع (POS).
author: BrianShook
ms.date: 03/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2019-03-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 44fd4b6246d3d7947527416c2b8b447bd64f179f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863311"
---
# <a name="health-check-for-pos-peripherals-and-services"></a>التحقق من سلامة الأجهزة الطرفية وخدمات نقطة البيع

[!include [banner](includes/banner.md)]

يصف هذا المقال عملية فحص السلامة في نقطة البيع (POS).

## <a name="overview"></a>نظرة عامة

بإمكان متاجر البيع بالتجزئة أن تكون عبارة عن بيئات معقده يتم فيها استخدام الكثير من التطبيقات والأجهزة. ومع ازدياد العمليات، قد يكون من الصعب ضمان تشغيل العمليات بسلاسة بشكل دائم، بسبب التبعيات، على سبيل المثال، الأجهزة الطرفية التي قد تتعطل أو تنفصل عن طريق الخطأ خلال اليوم. قد تكون عملية استكشاف وإصلاح المشاكل المتعلقة بالأجهزة والخدمات مكلفة لكبار التجار ومحبطة للعمليات الصغيرة.

يتضمن الإصدار 10.0.10 والإصدارات اللاحقة من Microsoft Dynamics 365 Commerce عملية فحص السلامة التي يمكنها أن تساعد في منع هذه التكلفة وهذا الإحباط. توفر هذه العملية أسلوبًا لاختبار الأجهزة مباشرة من نقطة البيع خارج العمليات العادية. وبالتالي، يمكنها أن تساعد بائعي التجزئة في اكتشاف المشاكل قبل حدوثها.

## <a name="key-terms"></a>المصطلحات الأساسية

| الفصل الدراسي | ‏‏الوصف |
|---|---|
| الجهاز الطرفي | أي جهاز يستخدمه تطبيق نقطة البيع لتسهيل الحركات والعمليات الأخرى في المتجر. تتضمن الأمثلة أدراج النقدية والماسحات الضوئية للكود الشريطي ووحدات الدفع الطرفية. |
| الخدمة | في هذا المقال، تعد الخدمة تطبيقًا إضافيًا يعتمد عليه تطبيق البيع لتنفيذ الحركات والعمليات اليومية. تشتمل الأمثلة على التطبيقات التي تساعد في حسابات الضرائب أو الشحن. |

## <a name="health-check-operation"></a>عملية فحص السلامة

عملية فحص السلامة هي العملية 717 في صفحة **عمليات‏‎ نقطة البيع** في مقرات Commerce. يمكن استخدامها أثناء وجود نقطة البيع في وضع غير مرتبط بالدرج. ومع ذلك، يجب أن تكون محطة الأجهزة نشطة.

بشكل افتراضي، تقوم عملية فحص السلامة باختبار فقط الأجهزة التي تم تكوينها في ملف تعريف الأجهزة لمحطة الأجهزة النشطة حاليًا للسجل. إذا استخدم سجل محطات أجهزة متعددة خلال اليوم، لإجراء عمليات فحص السلامة لجميع محطات الأجهزة هذه، يجب توصيله بكل محطة أجهزة على حدة. عملية فحص السلامة غير متوفرة على مستوى المتجر. ومع ذلك، من الممكن إجراء هذا النوع من الفحص من خلال قابلة توسعة Commerce Server.

### <a name="out-of-box-health-checks"></a>عمليات فحص السلامة الجاهزة

| النوع | الاتصال | تفاصيل |
|---|---|---|
| الطابعة | OPOS | يختبر هذا الفحص الوظائف الأساسية لربط الكائنات وتضمينها لنقطة البيع (OPOS). فيما يلي بعض الأمثلة:<ul><li>فتح: **Open** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>إغلاق: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> |
| شاشة عرض سطرية | OPOS | تختبر عملية الفحص هذه وظائف OPOS الأساسية. فيما يلي بعض الأمثلة:<ul><li>فتح: **Open** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>إغلاق: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> |
| العرض الثنائي | Windows | تضمن عملية الفحص هذه قيام نظام التشغيل بالكشف عن شاشة Windows ثانية. | 
| MSR | OPOS | تختبر عملية الفحص هذه وظائف OPOS الأساسية. فيما يلي بعض الأمثلة:<ul><li>فتح: **Open** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>إغلاق: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> |
| الدرج | OPOS | تختبر عملية الفحص هذه وظائف OPOS الأساسية. فيما يلي بعض الأمثلة:<ul><li>فتح: **Open** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>إغلاق: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> | 
| الماسح الضوئي | OPOS | تختبر عملية الفحص هذه وظائف OPOS الأساسية. فيما يلي بعض الأمثلة:<ul><li>فتح: **Open** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>إغلاق: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> | 
| المقياس | OPOS | تختبر عملية الفحص هذه وظائف OPOS الأساسية. فيما يلي بعض الأمثلة:<ul><li>فتح: **Open** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>إغلاق: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> |
| لوحة PIN | OPOS | تختبر عملية الفحص هذه وظائف OPOS الأساسية. فيما يلي بعض الأمثلة:<ul><li>فتح: **Open** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>إغلاق: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Close**</li></ul> |
| الوحدة الطرفية للدفع | SDK الدفعات | يقوم هذا الفحص باختبار الوظائف الأساسية للوحدة الطرفية للدفع التي تقدمها SDK الدفعات. <ul><li>تأمين</li><li>BeginTransaction</li><li>EndTransaction</li><li>ReleaseDevice</li><li>إغلاق</li></ul> |

### <a name="using-the-health-check-operation-in-the-pos"></a>استخدام عملية فحص السلامة في نقطة البيع

عند بدء عملية فحص السلامة في نقطة البيع، يسرد جزء إلى اليسار الأجهزة التي تم تكوينها ويعرض حالة كل جهاز. لتنفيذ عملية فحص السلامة على جهاز واحد، حدد الجهاز، ثم حدد **اختبار الجهاز المحدد**. لتنفيذ عملية فحص السلامة على جميع الأجهزة، حدد **اختبار الكل**. تقوم وظيفة **اختبار الكل** باختبار جميع الأجهزة، كل واحد على حدة، وتحدّث حالة كل جهاز في عمود **الحالة**.

يبين عمود **الفحص الأخير** تاريخ آخر عملية فحص سلامة لكل جهاز.

إذا نجحت عملية فحص سلامة أحد الأجهزة (أي لم تتم مصادفة أي خطأ)، ستكون حالة الجهاز **موافق**. إذا فشلت عملية فحص السلامة، فستشير الحالة إلى مصادفة خطأ. في هذه الحالة، يوفر الجزء الموجود على الجانب الأيسر تفاصيل ذات صلة بالخطأ، أو يطلب من المستخدم الاتصال بمسؤول النظام.

في بعض الأجهزة، مثل قفل مفاتيح OPOS، لا تتوفر اختبارات جاهزة لفحص السلامة. إذا لم يتم الكشف عن اختبار فحص السلامة لأي جهاز مستخدم، فستكون الحالة **غير مدعوم**.

### <a name="extending-health-checks"></a>توسيع عمليات فحص السلامة

يتم تكوين اختبارات فحص السلامة الجاهزة لتوفير بعض الرسائل المألوفة للمستخدم تتعلق بأخطاء عادية. ومع ذلك، لم يتم تناول جميع السيناريوهات. ومن خلال قابلية التوسعة، بإمكان التجار تعيين رسائل مألوفة لدى المستخدم إلى أخطاء قد تكون خاصة ببيئتهم.

يمكن أيضًا إنشاء عمليات فحص سلامة مخصصة لاختبار الأجهزة غير المدعومة بطريقة جاهزة أو اختبار أي أجهزة تعتمد عليها نقطة البيع.

## <a name="related-articles"></a>مقالات ذات صلة

[مشغلات نقطة البيع الحديثة (MPOS) والطباعة](dev-itpro/pos-trigger-printing.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]