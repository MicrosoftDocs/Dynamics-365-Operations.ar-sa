---
title: تحديثات الجودة الاستباقية
description: يقدم هذا المقال معلومات حول التسليم الاستباقي لتحديثات الجودة.
author: rashmansur
ms.date: 11/07/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2022-08-19
ms.search.form: ''
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 7d8de017c54a13a9935d74d33a57813922c9f823
ms.sourcegitcommit: 8aee31d6dffabe13969dd5b9de4e0bf95f53e67e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/19/2022
ms.locfileid: "9887120"
---
# <a name="proactive-quality-updates"></a>تحديثات الجودة الاستباقية

[!include[banner](../includes/banner.md)]

على مدى السنوات العديدة الماضية، أحرزت Microsoft تقدمًا مستمرًا فيما نشير إليه [نسخة واحدة](../../dev-itpro/lifecycle-services/oneversion-overview.md). يعد الوضع الداخلي لإصدار واحد بسيط مما يلي: أقرب امكانيه تمكننا من الحصول علي كافة العملاء الموجودين علي نفس إصدار البرنامج ، كلما زادت الجودة التي يمكننا تقديمها. نقوم بالبحث عن المشكلات وإصلاحها مره واحده ، سنقوم بالحصول علي هذه الحلول في ايدي المزيد من العملاء بسرعة أكبر.

ويتم التاكيد علي هذه العملية المحلية بواسطة النتائج: العدد الأقل من الحوادث عبر منتجاتنا. عندما لا يكون العملاء علي نفس الإصدار بشكل متناسق ، فعليك الاطلاع علي انهم متاثرون بالمشكلات التي يكون الحل متاحا لها بالفعل. لقد فعلنا تقدما كبيرا مع Dynamics 365 Finance, Dynamics 365 Supply Chain Dynamics 365 Project Operationsو Dynamics 365 Commerce ، وشكرا علي السلف الفنية الحديثة ، فيمكن الآن اتخاذ الخطوة التالية. ليس المعلومات التالية ما سنقوم به ، وما الذي قمنا باجراءه بالفعل لتعيين المرحلة ، وكيف ومتى سيتم تقديم القدرات الجديدة بدون مقاطعه.

## <a name="what-you-need-to-know"></a>ما تحتاج إلى معرفته

- يتم تطبيق تحديثات الجودة الاستباقية (PQU) على أساس شهري.
- يتم السماح باستثناءات لتحديثات الجودة الاستباقية للعملاء الذين يتم تنظيمهم في إدارة الأغذية والأدوية (FDA) في الولايات المتحدة الأمريكية فقط.
- لن تقوم تحديثات الجودة الاستباقية أبدًا بإرجاع البيئة إلى إصدار قديم أو الترقية تلقائيًا من إصدار تحديث خدمة واحد إلى آخر. 
- تقوم شركة Microsoft بتحديد كيفية إدارة تحديثات الجودة الاستباقية للبيئات التنظيمية، وللعملاء أصحاب السيادة والعملاء أصحاب السحابة في القطاع الحكومي.
- يتم ترحيل الإخطارات المتعلقة بتحديثات الجودة الاستباقية في [مركز رسائل Microsoft 365](https://admin.microsoft.com/AdminPortal/).
- وبخمسة أيام قبل تطبيق تحديث الجودة الاستباقية على إحدى البيئات، يتم إخطار العملاء بأن التحديث سيحدث.
- يتعذر على العملاء إلغاء تحديثات الجودة الاستباقية أو تأجيلها.
- يتم تثبيت تحديثات الجودة الاستباقية أثناء [إطار الصيانة المخطط لها‬](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows) المحددة للمنطقة.
- يتم تصميم تحديثات الجودة لتكون أقل خطورة من حيث المشكلات أو التراجعات، ويتم دعم ذلك بواسطة بيانات Microsoft.
- تنصح شركة Microsoft بإجراء اختبار مستهدف لمشكلات معينة أو إصلاحات عاجلة محددة ترتبط بتحديث الجودة الاستباقي.
- سيتم إلحاق كل بيئات الاختبار، باستثناء تلك التي لها استثناء حد الوقت بسبب الأسباب التنظيمية، وذلك في 7 يناير 2023.
- ستبدأ عملية إلحاق الإنتاج لتحديثات الجودة الاستباقية من 21 يناير 2023. 
- ستبدأ عملية إلحاق الإنتاج فقط بمشاريع Lifecycle Services التي لها بيئة (بيئات) اختيار يتم إعدادها حتى الآن لاستلام تحديثات الجودة الاستباقية بوتيرة منتظمة لكافة إصدارات تحديث الخدمة المعتمدة. لا ينطبق هذا إلا على بيئات العملاء التي لم يتم توفير أية استثناءات لها بسبب الأسباب التنظيمية أو القانونية الأخرى.
- للحصول على جدول كامل لتحديثات الجودة الاستباقية لبيئة الاختيار وبيئات الإنتاج عبر الدورة التدريبية لعام 2023، راجع أدناه.
- يحتوي كل تحديث خدمة على تدريب إصدار PQU واحد مستمر أو محدد للبدء على الأقل. وبمجرد أن يتم إعداد البيئات الخاصة بك لعملية PQU، قد تتلقى تحديث جودة استباقي مجدول مسبقًا على كافة الوثائق عند الانتقال إلى تحديث خدمة إصدار أحدث. يُرجى التحقق من الجدول لتحديد متى تتم جدولة PQU لتحديث الخدمة إذا كنت تخطط للترقية إلى تحديث خدمة إصدار أحدث. 

> [!Note]
> وسوف تتلقى بيئات اختبار الأداء القياسي (tier4) واختبار الأداء الرئيسي (tier5) وبيئات الإنتاج تحديثات PQU في عطلات نهاية الأسبوع. 

## <a name="focus-on-quality-updates"></a>التركيز علي التحديثات الاصلاحيه

نقوم حاليا بتوفير سبعه [تحديثات](public-preview-releases.md) خدمه لكل عام. علي سبيل المثال ، 10.0.29 الإصدار هو تحديث خدمه. وحتى التاريخ الحديث ، كان هناك ثمانيه تحديثات في السنه. ومع ذلك ، قمنا بإسقاط تحديث واحد كاستجابة لملاحظات العملاء التي تقوم بكشف الرغبة في تجنب التغييرات بالقرب من نهاية سنه التقويم.

لن نقوم بتغيير وتيره تحديثات الخدمة. بدلا من ذلك ، فان الخطوة التالية للامام في الإصدار الواحد من جورنيي تركز علي التحديثات *الاصلاحيه*. تعد تحديثات الجودة بنيات تراكمية للإصلاحات الضرورية. ولا تتضمن ميزات جديده. في اي وقت محدد ، ينتشر مجتمع العملاء بالبالكامل بين التحديثات الثلاثة أو الاربعه الحديثة للخدمة. ومع ذلك ، بالنسبة لأي تحديث خدمه محدد ، يمكن استخدام العديد من إصدارات تحديث الجودة المختلفة داخل المجموعة ، وذلك وفقا لتواريخ عند نشر الأشخاص. في الخطوة التالية ، سنقوم بالاطلاع علي تحديثات جوده البث. نحن نستخدم هذا النموذج بالفعل للتطبيقات المستندة الينا Dataverseوقد شاهدت النتائج المتوقعة للحصول علي الجودة المحسنة وانخفاض حوادث الدعم.

بالطبع ، فان التخفيض بالعيوب قد يؤدي إلى تقليل الحاجة إلى التحديثات الاصلاحيه أو كليها. لدينا مبادرات متعددة في رحله الطيران لتقليل العيوب التي تتطلب تحديثات الجودة. وحتى في حاله بايلوادس التحديث في الجودة ، يقوم التناسق عبر أساس العميل بتحسين السوبورتابيليتي ، والحصول علي تحسينات علي العملاء بسرعة أكبر ، وتقليل تكرار العملاء يواجهون مشكلات بوجود حلول موجودة بالفعل.

## <a name="making-proactive-distribution-possible"></a>القيام بالتوزيع الاستباقي المحتمل

تم بالفعل نشر السلف المتعددة التي تتيح التسليم الاستباقي لتحديثات الجودة:

- **قرب-صفر تحديث** التعطل – لدفع بيئات أكثر تكرارا ، من الضروري ان يتم تقليل تاثير أتاحه البيئة للحفاظ علي اتفاقيات مستوي الخدمة Dynamics 365 (استئناف). قريب-صفر تم تقديم تحديث فتره التعطل في الأصل للمساعدة في تحسين عمليه التصحيح الشهرية لنظام التشغيل باستخدام كتله تجاوز الفشل لتنشيط الصورة المحدثة بأقل توقف. يتم تحسين اليه تطبيق التحديثات بحيث لا تكون بالأمر الأقل كفاءه ، سيتم تغطيه كل من تصحيح نظام التشغيل ونشر تحديث الجودة.

    بالنسبة للمستخدمين التفاعليين ، ربما تتم مقاطعه جلسة عمل نشطه ، ستنتقل أعاده المحاولة إلى البيئة المحدثة الآن. بتقديم [جدولة المجموعات المستندة إلى أولوية](../../dev-itpro/sysadmin/priority-based-batch-scheduling.md)، فإنه يتم استرداد واستئناف جدولة المجموعة والمعالجة مباشرة بعد التحديث. ستكون جدوله المجموعة المستندة إلى اولويه في مكانها للعملاء قبل البدء في المشاركة في التوزيع الاستباقي لتحديثات الجودة لبيئات الإنتاج الخاصة بهم.

- **الساعات** الداكنة – يتم تحديد الساعات الداكنة لكل منطقه من مناطق Azure ، سيتم اجراء تحديثات تعطل فيها بقرب صفر في فتره الساعة الداكنة.

## <a name="the-proactive-update-process"></a>عمليه التحديث الاستباقية

سيؤدي نشر تحديثات الجودة الاستباقية إلى تتبع عمليه توزيع أمنه (سدب). سارتقاء مواصفات سدب ، ولكن سيتم نشر تحديثات الجودة أولا علي بيئات تحديد الصلاحيات. وكنسبه مئوية لساندبوكسيس التي تم نشرها بنجاح ، فانه سيتم بدء النشر إلى بيئات الإنتاج. ستقوم أنظمه الاستماع بمراقبه بيانات تتبع الاستخدام وليفيسيتي الأخطاء ، سيؤدي ذلك إلى إيقاف عمليه التشغيل التمهيدي لإصدار معين في حاله اكتشاف اي انحدار. سيظل بإمكان العملاء سحب تحديثات الجودة قبل النشر الاستباقي إذا كانوا يريدون ذلك.

تظهر بيانات أداره الإصدارات الحالية التي يتم تقديم اقل من 3 بالمائة من التراجعات في تحديثات الجودة. بالتركيز المتزايد علي تقليل الانحدار والسدب المحسن ، فان التاثير المحتمل علي التراجعات سيكون اقل دقه من مكاسب الجودة التي حققتها بسرعة أكبر في الحصول علي الإصلاحات التي يتم نشرها للعملاء علي نطاق واسع.

## <a name="process-changes"></a>معالجة التغييرات

يتم تنفيذ مجموعه من تغييرات العملية قبل تنشيط نشر التحديث الاستباقي للجودة:

- **وسوف تضمن المخطط** – تولينج ان عمليات إنشاء تحديث الجودة تتضمن فقط تغييرات المخطط التي يمكن تطبيقها اثناء اتصال الخدمة. ستساعد هذه الطريقة في المحافظة علي امكانيه تطبيق التحديث بالقرب من التوقف عن الصفر.
- **زيادة سكروتيني** التغيير-حاليا ، توجد بالفعل خطوه عمليه اضافيه لاعتماد التغييرات للتضمين في أحد تحديثات الجودة. سيتم زيادة السكروتيني في الخطوة الاضافيه للمساعدة في الحد من احتمال التراجع. لا يسمح بفصل التغييرات في التحديثات الاصلاحيه ، سيساعد سكروتيني التغيير المتزايد علي ضمان تلبيه هذا الهدف.
- **إمكانية الرؤية** – سنرسل إخطارات من خلال مركز الإدارة وLifecycle Services والقنوات الأخرى المتاحة لتحديثات الجودة الاستباقية القادمة. بالاضافه إلى ذلك ، سيكون لفرق العمل والعملاء المحتملين امكانيه الرؤية في المكان الذي تم فيه توزيع تحديثات الجودة بشكل استباقي.

    > [!NOTE]
    > يقوم فريق اتصالات Microsoft بالاستقصاء عن حاله التولينج المستمرة للبريد الكتروني الذي يمنع تسليم اعلامات البريد الكتروني. الرجاء متابعه مراقبه مركز الرسائل Microsoft 365 لعمليات إلحاق والاعلام بالرسائل المرتبطة.

- **سيتم استخدام الفشل بأمان عبر فلايتينج** – فلايتينج لحماية تغييرات التعليمات البرمجية كلما كان قابلا للتطبيق في إصلاح أخطاء في تحديث الجودة أو استخدام الميزة الموجودة فلايتينج المتعلقة بالإصلاح. إذا كان الاحتياطي أو تشغيل التغيير مطلوبا بعد النشر الاستباقي ، فيمكن القيام بذلك من خلال نظام فلايتينج لتجنب المزيد من الأعطال.
- **تعيين مزامنة بيئة الاختبار** – تحديث منظم لبيئة اختيار معزولة للاختيار بالإضافة إلى أن الإنتاج غير مدعوم في هذا الوقت. ستتلقى كافة بيئات الاختيار الطبقة 2 والطبقة 3 تحديثات استباقية قبل 7 أيام على الأقل من بيئة الإنتاج في مشروع Lifecycle Services. مرة أخرى، لا ينطبق هذا إلا على بيئات العملاء التي لم يتم توفير أية استثناءات لها بسبب الأسباب التنظيمية أو القانونية الأخرى.

## <a name="what-is-the-rollout-roadmap-for-quality-updates"></a>ما هو جدول إطلاق تحديثات الجوده؟

بدأ توزيع تحديثات الجودة الاستباقية لبيئات الاختيار في سبتمبر 2022، لعملاء Azure لمجموعة Azure العامة. بحلول 1 يناير 2023، سنقوم بإكمال عملية الإلحاق 99% من بيئات الاختبار لتحديثات الجودة الاستباقية.

يتم السماح باستثناءات عملية التوزيع التي تم تحديثها بشكل استباقي فقط للعملاء الذين يتم تنظيمهم في إدارة FDA. ما زلنا نقوم بكيفية أداره البيئات التنظيمية والسوفيريجن والعملاء الحكوميين. 

ونظرا لان العملاء سيستلمون بايلوادس أصغر بشكل دوري ، فاننا نتوقع الحصول علي العملية الحالية لتصبح أسهل. سنقوم بضبط تكرار نشر التحديث كما نقوم بتوضيح القدرة علي تشغيل العملية بدون توقف. تعمل هذه العملية بالفعل لنظام وتطبيقات Dataverse الخاصة بنا، ويتم تسليم التحسينات المتوقعة في جودة الخدمة. إننا نتخذ نفس الخطوة للأمام لتطبيقات التمويل العمليات.


## <a name="when-will-quality-updates-start-for-production-environments"></a>متى يتم بدء تشغيل تحديثات الجودة الخاصة ببيئات التشغيل؟
خلال الأشهر القليلة الأولى من 2023، بدءًا من 15 يناير - سنبدأ عملية الإلحاق في بيئة تشغيل للتحديثات الاستباقية وزيادة النسبة المئوية لبيئات التشغيل التي تتلقي تحديثات استباقية تدريجيًا. سنقوم فقط بالتأكد من بيئة إنتاج في مشروع Lifecycle Services الذي يحتوي على بيئات اختيار بالفعل مُعدة لتلقي التحديثات الاستباقية. وقبل التحديث، سيتم إعلام العملاء الذين لديهم بيئات تشغيل تم إعدادها من خلال مركز الرسائل أو شعار Lifecycle Services. للحصول على جدول كامل لتحديثات الجودة الاستباقية لبيئة الاختيار وبيئات الإنتاج عبر الدورة التدريبية لعام 2023، راجع أدناه.

## <a name="what-is-the-schedule-for-sandbox-proactive-quality-updates"></a>ما هو الجدول الزمني لتحديثات الجودة الاستباقية في وضع الحماية؟
للحصول على معلومات حول الساعات الداكنة لكل منطقة، راجع [ما هي نوافذ الصيانة المخططة حسب المنطقة؟](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows).

### <a name="proactive-quality-update-release-10029"></a><a name="schedule"></a> إصدار تحديث الجودة الاستباقي: 10.0.29
**إصدار التطبيق: 10.0.1326.70**  
**الموافقة على أحدث مقال من مقالات قاعدة المعارف: 750332**

| إرساء | المناطق | الجدول الزمني المكتمل | جدول الحماية القادمة|
|---|---|---|---|
| إرساء 1 | مركزي كندا ، شرق كندا ، وسط فرنسا ، مركزي الهند ، شرق النرويج ، غرب سويسرا | 14 أكتوبر إلى 17 أكتوبر، 2022، 2 نوفمبر إلى 5 نوفمبر، 2022، 13 نوفمبر إلى 16 نوفمبر، 2022، 5 ديسمبر إلى 8 ديسمبر، 2022 | 2 يناير حتى 5 يناير، 2023 |
| إرساء 2 | فرنسا الجنوبية ، الهند الجنوبية ، غرب النرويج ، شمال سويسرا ، شمال جنوب افريقيا ، شرق أستراليا ، جنوب المملكة الشمالية ، شمال أواي ، شرق اليابان ، أستراليا جنوب شرق ، جنوب شرق اسيا | 15 أكتوبر إلى 18 أكتوبر، 2022، 2 نوفمبر إلى 5 نوفمبر، 2022، 13 نوفمبر إلى 16 نوفمبر، 2022، 5 ديسمبر إلى 8 ديسمبر، 2022 | 2 يناير حتى 5 يناير، 2023 |
| إرساء 3 | شرق اسيا ، غرب المملكة الغربية البرازيل ، غرب اليابان ، جنوب غرب أوروبا الغربية ، شرق الولايات الرسمية أواي | 16 أكتوبر إلى 19 أكتوبر، 2022، 2 نوفمبر إلى 5 نوفمبر، 2022، 13 نوفمبر إلى 16 نوفمبر، 2022، 5 ديسمبر إلى 8 ديسمبر، 2022 | 2 يناير حتى 5 يناير، 2023 |
| إرساء 4 | شمال أوروبا ووسط الولايات الاميركيه وغرب الولايات الاميركيه | 17 أكتوبر إلى 20 أكتوبر، 2022، 2 نوفمبر إلى 5 نوفمبر، 2022، 15 نوفمبر إلى 18 نوفمبر، 2022، 5 ديسمبر إلى 8 ديسمبر، 2022 | 2 يناير حتى 5 يناير، 2023 |
| إرساء 5 | وزارة الدفاع ، سحابة المجتمع الحكومية ، الصين | غير مجدول | غير مجدول |

### <a name="proactive-quality-update-release-10030"></a><a name="schedule"></a> إصدار تحديث الجودة الاستباقي: 10.0.30
**إصدار التطبيق: 10.0.1362.77**
**الموافقة علي أحدث مقال من مقالات قاعده المعارف: 767597**

| إرساء | المناطق | الجدول الزمني المكتمل | جدول الحماية القادمة |
|---|---|---|---|
| إرساء 1 | مركزي كندا ، شرق كندا ، وسط فرنسا ، مركزي الهند ، شرق النرويج ، غرب سويسرا | من 1 ديسمبر إلى 4 ديسمبر 2022 |  من 13 ديسمبر إلى 16 ديسمبر 2022 | 
| إرساء 2 | فرنسا الجنوبية ، الهند الجنوبية ، غرب النرويج ، شمال سويسرا ، شمال جنوب افريقيا ، شرق أستراليا ، جنوب المملكة الشمالية ، شمال أواي ، شرق اليابان ، أستراليا جنوب شرق ، جنوب شرق اسيا | من 2 ديسمبر إلى 5 ديسمبر 2022 |  من 13 ديسمبر إلى 16 ديسمبر 2022 | 
| إرساء 3 | شرق آسيا، غرب المملكة المتحدة، غرب اليابان، جنوب البرازيل، شمال أوروبا، شرق الولايات المتحدة، الإمارات العربية المتحدة، الوسط | من 3 ديسمبر إلى 6 ديسمبر 2022 |  من 13 ديسمبر إلى 16 ديسمبر 2022 | 
| إرساء 4 | غرب أوروبا، منطقة وسط الولايات المتحدة الأمريكية وغرب الولايات المتحدة الأمريكية | من 4 ديسمبر إلى 7 ديسمبر 2022 |  من 13 ديسمبر إلى 16 ديسمبر 2022 | 
| إرساء 5 | وزارة الدفاع ، سحابة المجتمع الحكومية ، الصين | غير مجدول | غير مجدول |

### <a name="proactive-quality-update-calendar-year-2023-schedule"></a><a name="schedule"></a> جدول سنة التقويم 2023 لتحديث الجودة الاستباقي

#### <a name="stations-to-region-mapping"></a><a name="Stations-Regions"></a> تعيين المحطات إلى المنطقة

| المحطات | المناطق |
|---|---|
| إرساء 1 | سيتم تحديده لاحقًا |
| إرساء 2 | مركزي كندا ، شرق كندا ، وسط فرنسا ، مركزي الهند ، شرق النرويج ، غرب سويسرا |
| إرساء 3 | فرنسا الجنوبية ، الهند الجنوبية ، غرب النرويج ، شمال سويسرا ، شمال جنوب افريقيا ، شرق أستراليا ، جنوب المملكة الشمالية ، شمال أواي ، شرق اليابان ، أستراليا جنوب شرق ، جنوب شرق اسيا |
| إرساء 4 | شرق آسيا، غرب المملكة المتحدة، غرب اليابان، جنوب البرازيل، شمال أوروبا، شرق الولايات المتحدة، الإمارات العربية المتحدة، الوسط |
| إرساء 5 | غرب أوروبا، منطقة وسط الولايات المتحدة الأمريكية وغرب الولايات المتحدة الأمريكية |
| إرساء 6 | وزارة الدفاع ، سحابة المجتمع الحكومية ، الصين |


> [!IMPORTANT]
> يعد هذا جدولاً عالي المستوى لسنة 2023. للحصول على جدول محدد أكثر، راجع العينة الموجودة أدناه لإصدار يناير 10.0.30 الإصدار 2. سيتم تحديث إصدار التطبيق والجدول الدقيق قبل 7 أيام من بدء تدريب تحديث الجودة.

> [!Note]
> سوف تتلقى بيئات عمليات الإنتاج المُعدة التحديث تدريب 10.0.30 الإصدار 2، وسوف تتلقى البيئات المُعدة اتصالاً سريعًا.

| تدريب تحديث الجودة | إصدار أخير | مدة التدريب |
|---|---|---|
| 10.0.30 الإصدار -2 | 16 ديسمبر، 2022 | من 2 يناير حتى 29 يناير، 2023 |
| 10.0.30 الإصدار -3 | 13 يناير 2023 | من 30 يناير إلى 25 فبراير، 2023 |
| 10.0.30 الإصدار -4 | 24 فبراير 2023 | من 6 مارس إلى 8 أبريل، 2023 |
| 10.0.31 الإصدار -1 | 3 فبراير 2023 | من 13 فبراير، 2023 إلى 18 مارس، 2023|
| 10.0.31 الإصدار -2 | 3 مارس، 2023 | من 6 مارس، 2023 إلى 15 أبريل، 2023|
| 10.0.31 الإصدار -3 | 14 أبريل 2023 | من 24 أبريل، 2023 إلى 27 مايو، 2023|
| 10.0.32 الإصدار -1 | 31 مارس، 2023 | من 10 أبريل، 2023 إلى 13 مايو، 2023|
| 10.0.32 الإصدار -2 | 28 أبريل 2023 | من 8 مايو، 2023 إلى 10 يونيو ، 2023|
| 10.0.32 الإصدار -3 | 26 مايو 2023 | من 5 يونيو، 2023 إلى 8 يوليو، 2023|
| 10.0.33 الإصدار -1 | 28 أبريل 2023 | من 8 مايو، 2023 إلى 10 يونيو ، 2023|
| 10.0.33 الإصدار -2 | 26 مايو 2023 | من 5 يونيو، 2023 إلى 8 يوليو، 2023|
| 10.0.33 الإصدار -3 | 14 يوليو 2023 | من 24 يوليو، 2023، إلى 26 أغسطس، 2023|
| 10.0.34 الإصدار -1 | 23 يونية 2023 | من 3 يوليو، 2023، إلى 5 أغسطس، 2023|
| 10.0.34 الإصدار -2 | 21 يوليو 2023 | من 31 يوليو، 2023 إلى 2 سبتمبر، 2023|
| 10.0.34 الإصدار -3 | 1 سبتمبر 2023 | من 11 سبتمبر، 2023 إلى 14 أكتوبر، 2023|
| 10.0.35 الإصدار -1 | 28 يوليو 2023 | من 7 أغسطس، 2023 إلى 9 سبتمبر، 2023|
| 10.0.35 الإصدار -2 | 25 أغسطس 2023 | من 4 سبتمبر، 2023 إلى 7 أكتوبر، 2023|
| 10.0.35 الإصدار -3 | 20 أكتوبر 2023 | من 30 أكتوبر، 2023 إلى 16 ديسمبر، 2023|
| 10.0.36 الإصدار -1 | 29 سبتمبر 2023 | من 9 أكتوبر 2023، إلى 11 نوفمبر 2023|
| 10.0.36 الإصدار -2 | 27 أكتوبر 2023 | من 6 نوفمبر، 2023 إلى 16 ديسمبر 2023|
| 10.0.36 الإصدار -3 | 12 يناير 2024 | من 22 يناير، 2023 إلى 24 فبراير، 2024|
| 10.0.37 الإصدار -1 | 3 نوفمبر 2023 | من 13 نوفمبر، 2023 إلى 6 يناير، 2024|
| 10.0.37 الإصدار -2 | 30 ديسمبر 2023 | من 8 يناير، 2024 إلى 10 فبراير، 2024|
| 10.0.37 الإصدار -3 | 27 يناير 2024 | من 5 فبراير، 2024 إلى 9 مارس، 2024|
| 10.0.37 الإصدار -4 | 23 فبراير 2024 | من 4 مارس، 2024 إلى 6 أبريل، 2024|

### <a name="proactive-quality-update-upcoming-10030-release-2-train-schedule"></a><a name="schedule"></a> جدول تدريب تحديث الجودة الاستباقية المقبل 10.0.30 الإصدار 2
**إصدار التطبيق: 10.0.1362.99**

| المحطات | جدول الحماية القادمة | جدول الإنتاج المقبل |
|---|---|---|
| إرساء 1 | غير متاح | غير متاح |
| إرساء 2 | 2 يناير حتى 5 يناير، 2023 | من 21 يناير حتى 22 يناير، 2023 |
| إرساء 3 | من 3 يناير حتى 6 يناير، 2023 | من 28 يناير حتى 29 يناير، 2023 |
| إرساء 4 | من 9 يناير حتى 12 يناير، 2023 | غير متاح |
| إرساء 5 | من 16 يناير حتى 19 يناير، 2023 | غير متاح |
| إرساء 6 | غير متاح | غير متاح |

> [!IMPORTANT] 
> قبل خمسة أيام من تاريخه، ستقوم Microsoft بتحديث الجدول السابق وإرسال إخطار إلى مجموعة من البيئات المجدولة لتلقي تحديثات الجودة هذه. الجدول السابق قابل للتطبيق فقط علي البيئات التي تم اخطارها بأحد التحديثات القادمة. للحصول على معلومات حول الساعات الداكنة لكل منطقة، راجع [ما هي نوافذ الصيانة المخططة حسب المنطقة؟](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows).
>
> بالنسبة لكل مجموعه *مناطق أو محطه* ، حيث تتم جدوله تحديث الجودة حاليا ليتم سحبه ، يعرض الجدول نطاقا من أربعه أيام. ستبدا عمليات تحديث الجودة ببيئات الحماية فقط. بعد ذلك ، مع زيادة النسبة المئوية لصناديق الحماية التي تم نشرها بنجاح ، سيبدأ النشر في بيئات الإنتاج بإخطارات مسبقة للعملاء.
> 
> ستظهر تحديثات الجودة دائما بطريقه متدرجة تمكننا من استهداف مجموعه من البيئات لكل جدول وإكمال كافة المجموعات بنهاية اليوم الرابع لأحدي المحطات. ومع ذلك ، لا يعني هذا ان تحديث البيئة سيمتد أربعه أيام. وهو فقط يعني انه لا يمكننا تحديد مجموعه البيئات التي سيتم تحديثها في يوم معين ضمن نطاق أربعه أيام. سيتم اجراء كافة التحديثات خلال ساعة داكنه بالقرب من فتره توقف الصفر. سديفينيتيفيلي التحديثات إلى النهاية ضمن النافذة الداكنة بالساعة في منطقه محدده.

## <a name="how-are-the-dark-hours-handled-for-customers-that-have-one-finance-and-operations-apps-instance-but-are-active-in-multiple-time-zones"></a>كيف تتم معالجه الساعات الداكنة للعملاء الذين لديهم مثيل واحد لأحدي تطبيقات التمويل والعمليات، ولكنها نشطه في مناطق زمنيه متعددة؟ 
لا توجد جداول زمنية خاصة خارج الأوقات المظلمة حيث يوجد مثيل تطبيقات المالية والعمليات ، حيث نخطط لطرح تحديثات الجودة بأدنى حد من التعطيل مع [nZDT](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#what-does-near-zero-downtime-maintenance-mean).

## <a name="what-is-the-current-rollout-cadence-for-proactive-quality-updates"></a>ما هو إيقاع الطرح الحالي لتحديثات الجودة الاستباقية؟
يتم شحن التحديثات الاستباقية للجودة (بقوس) حاليا مره واحده لكل إصدار معتمد من تحديث الخدمة. يتم الآن دفع تحديث واحد فقط كل شهر لتحديد بيئات اليه تحديد الصلاحيات ما لم ينتقل العملاء إلى إصدار تحديث خدمه جديد. وفي هذه الحالة ، قد يحصلون علي بقو مجدولة مسبقا كجزء من التدريب الموجود لتحديث الخدمة الجديد. بعد اكتمال العملية التمهيدية العالمية في 2023 ، سيزيد تكرار هذه التحديثات. ستتلقى دائما اشعار بشهر واحد علي الأقل عند وجود تغيير في إيقاع الشحن.

## <a name="how-will-microsoft-ensure-the-quality-of-these-updates"></a>كيف ستتأكد شركه Microsoft من جوده هذه التحديثات؟
تسعى شركة Microsoft جاهدة للحفاظ على خط أنابيب التحرير فعالًا بدرجة كافية لتقديم حمولات صغيرة للحفاظ على انخفاض تكلفة التحقق من الصحة. يمر كل إصلاح في تحديث الجودة من خلال عمليه توزيع صارمة وأمنه تساعد علي تحسين الجودة والموثوقية، ومن ثم تقليل تعرض العميل للتأثير. سيحدث التوزيع في مراحل علي بيئات الاختبار المعزول أولاً، متبوعًا بالإنتاج. تسمح عمليات التوزيع المرحلية بالمراقبة المناسبة لتحديد ما إذا كانت هناك عمليه توزيع أمنه. سنقوم بإيقاف عمليه الإطلاق إذا تم الكشف عن مشكلات مع كل مجموعه من العملاء الذين تم نشرها والتأكد من أن كل خطوه في العملية الإطلاق تحتوي علي وقت كافٍ لوجود مشاكل بالسطح. لكل تحديث جوده قادم، سنقوم بتقديم رؤية في الجدول من خلال التحديثات إلى الوثائق العامة ورسائل البريد الكتروني، لذا يمكن للعملاء التخطيط للأيام المقبلة‬.

## <a name="can-customers-delay-reschedule-or-pause-a-quality-update"></a>هل يمكن للعملاء تأخير تحديث الجودة أو إعادة جدولته أو إيقافه مؤقتًا؟
الرقم إن الهدف الأساسي من تحديثات الجودة هو ضمان أن الأساسيات مثل الأمان والخصوصية والموثوقية والتوافر والأداء يتم تحسينها باستمرار لعملائنا. من خلال تأخير التحديث أو إيقافه مؤقتًا، سيكون الأمان والتوافر والموثوقية في خطر.

## <a name="how-do-i-know-what-set-of-changes-went-into-a-quality-update-payload"></a>كيف يمكنني معرفة مجموعة التغييرات التي تم إدخالها في حمولة تحديث الجودة؟
اتبع الخطوات أدناه لتحديد قائمة التغييرات التي تدخل في حمولة تحديث الجودة. 

استخدم 10.0.28 لتدريب تحديث الجودة وإصدار التطبيق المرتبط 10.0.1265.89.

1. في Lifecycle Services، قم بفتح الصفحة **تفاصيل البيئة** للوصول إلى وضع الحماية الخاص بك. 
2. في المقطع التحديثات **المتوفرة** ، حدد **عرض تحديث** لأحدث إصدار لإصدارات التحديث الخاصة بالجودة. 
3. تصدير البناء إلى CSV أو Microsoft Excel إلى ملف.
4. في الملف الذي تم تصديره، قم بتصفية وتحديد **إنشاء الإصدار** الذي يقل عن رقم الإصدار 10.0.1265.89 أو يساوي. يجب أن تكون الآن قادرًا على رؤية حمولة دلتا.
 
> [!NOTE]
> يجب ان يحدث التصدير إلى ملف CSV أو Excel قبل تحديث البيئة. والا ، يمكنك استخدام بيئة بنفس التكوين الذي لم يتم تثبيت التحديث عليه واتباع الخطوات الموضحة أعلاه.

[![مثال علي بيئة مع تحديث الجودة.](./media/how-to-get-kb-list-pqu.png)](./media/how-to-get-kb-list-pqu.png)

## <a name="what-is-the-process-if-a-critical-issue-is-found-after-a-quality-update"></a>ما هي العملية التي تتم إذا تم العثور علي مشكله هامة بعد تحديث الجودة؟
تتمثل المشكلة أو الانحدار الحرج في حدث واحد أو أكثر يؤدي عادةً إلى تدهور تجربة العديد من العملاء مع واحدة أو أكثر من خدماتنا. قد تتسبب هذه المشكلات في حدوث وقت تعطل غير مخطط له بما في ذلك عدم التوفر وتدهور الأداء والتداخل مع إداره الخدمة. في حاله وجود تأثير واسع للعميل نظرًا لمثل هذه التراجعات، سنقوم بإيقاف عمليه الإطلاق لتحديث الجودة حتى يتسنى لنا الاتصال بالمشكلة وإصلاحها. بشكل عام، سيوفر تحديث الجودة التالي الإصلاح الضروري لاستئناف الإطلاق.

في حاله تاثر بيئة عميل واحده، اتصل بدعم Microsoft لفتح أحدي البطاقات. واستنادًا إلى المبررات، سنقوم بإيقاف تشغيل تحديث الجودة لكافة البيئات الأخرى في ذلك المشروع حتى يتم تفادي المشكلة.

## <a name="can-customers-still-manually-apply-hotfix-updates-from-lifecycle-services"></a>هل يمكن للعملاء الاستمرار في تطبيق تحديثات الإصلاحات العاجلة يدويًا من Lifecycle Services؟
نعم. لضمان التماثل المستمر مع كيفية عمل الإصلاحات العاجلة، فإنه لا يزال من الممكن تطبيق تحديثات الإصلاحات العاجلة على بيئات العملاء في Lifecycle Services. ومع ذلك، فمن المهم ملاحظه ان الإصلاحات الضرورية التي يتم نشرها كجزء من تحديث الجودة، وذلك من خلال السدب القياسي قبل ان يتم نشر التحديث. وهذا يقلل من خطر التراجع بسبب التعرض لجوده أعلي. نوصي باختيار تحديث الجودة من خلال تطبيق الإصلاحات العاجلة يدويًا لزيادة المصداقية.

## <a name="can-customers-proactively-install-a-quality-update-build-ahead-of-the-schedule"></a>هل يمكن للعملاء تثبيت إصدار تحديث عالي الجودة بشكل استباقي قبل الموعد المحدد؟
نعم. يمكنك تثبيت تحديث الجودة بشكل استباقي. ستقوم Microsoft بتخطي التحديث إذا كان إصدار البنية الحالي للبيئة مساويًا أو أعلى من تحديث الجودة المطلوب.

## <a name="if-an-environment-has-an-upcoming-scheduled-monthly-service-update-within-a-week-will-it-still-receive-quality-updates"></a>إذا كان للبيئة تحديث الخدمة الشهرية القادمة في الأسبوع، فهل سيتم استلام تحديثات الجودة؟
- لا يتم تطبيق تحديثات الجودة على بيئات الإنتاج إذا كان هناك تحديث وشيك للخدمة مجدول في غضون أسبوع من وقت جدولة تحديث الجودة.
- إذا كانت ‏‫بيئة الاختبار المعزول لها نفس إصدار البناء أو أعلي من تحديث الجودة الوشيك، سيتم تخطيها.
- إذا كانت ‏‫بيئة التشغيل لها نفس إصدار البناء أو أعلي من تحديث الجودة الوشيك، سيتم تخطيها.
- إذا كان لتحديد الصلاحيات نفس إصدار البناء أو إصدار أعلي بسبب تحديث الجودة أو التحديث اليدوي لعمليه الإنتاج، سيستمر الإنتاج في الحصول علي الإصدار المجدول من تحديث الخدمة الشهري. إذا لم تكن ترغب في تحديث بيئة التشغيل المجدولة إلى إصدار تحديث الخدمة، فإنه يمكنك إيقاف تحديث الخدمة مؤقتًا من Lifecycle Services. 
- ونوصي باستخدام أحدث إصدار من إصدارات التحديث الخاصة بالجودة لاختبار التغييرات التي أجريتها لتحديث خدمة قادم للحصول علي استقرار ونتائج أفضل.

## <a name="if-an-environment-has-an-upcoming-scheduled-action-and-a-scheduled-quality-update-in-the-same-maintenance-window-will-it-still-receive-the-quality-update"></a>إذا كان للبيئة اجراء مجدول قادم وتحديث جوده مجدول في نفس اطار الصيانة ، فهل سيظل يتلقى تحديث الجودة ؟
إذا كان هناك اي اتصال باجراء مجدول مسبقا ، علي سبيل المثال ، نقطه في الاستعادة الزمنيه (بيتر) ، تتم أعاده جدوله تحديث الجودة إلى اطار الصيانة التالي المتوفر في اطار أربعه أيام. لمزيد من التفاصيل حول الجدول ، انظر [ما هو الجدول الزمني لتحديثات الجودة الاستباقية؟](#schedule). 

## <a name="can-an-environment-be-brought-back-to-its-previous-state-if-there-are-issues-after-a-quality-update-is-applied"></a>هل يمكن إعادة البيئة إلى حالتها السابقة في حاله ما إذا كانت هناك مشكلات بعد تطبيق تحديث جوده؟
بعد تطبيق تحديث الجودة، لا مجال للتراجع تحت أين من الأحوال. وهناك فقط خيارات إعادة توجيه التصحيح المتاحة لتفادي المشكلات.

## <a name="what-about-fda-regulation-and-gxp"></a>ماذا عن قوانين الفيدرالية الصادرة عن إدارة الأغذية والأدوية (FDA) وGxP؟
ولا يزال الخطة الخاصة بالعملاء الخاضعين للتحقق واللوائح الخاصة بقوانين الفيدرالية الصادرة عن إدارة الأغذية والأدوية (FDA) في حالة تطور. من المتوقع وجود تحديثات اضافيه في هذا الجزء قريبًا. والآن، فإن كافة العملاء الآخرين معفيون من تحديثات الجودة. لضمان ان العميل يقع ضمن FDA اللوائح ، الرجاء زيارة [عروض GxP من Microsoft Azure](/azure/compliance/offerings/offering-gxp).

## <a name="what-versions-of-service-updates-are-supported-for-these-quality-updates"></a>ما هي إصدارات تحديثات الخدمة المعتمدة لهذه التحديثات الإصلاحية؟
يتأهل العملاء في جميع الإصدارات المدعومة من تحديثات الخدمة للحصول على تحديثات الجودة. 

## <a name="finance-and-operations-apps-deployments-with-retail-components-typically-require-additional-work-in-addition-to-having-to-redeploy-mpos-how-will-these-quality-updates-impact-the-retail-sdk"></a>تتطلب عمليات نشر تطبيقات التمويل والعمليات مع مكونات البيع بالتجزئة عملاً إضافيًا، بالإضافة إلى الحاجة إلى أعاده نشر ‏‫نقطة البيع الحديثة (MPOS)‬. كيف تؤثر تحديثات الجودة هذه على Retail SDK؟ 
نظرًا لأن طبيعة الإصلاح العاجل نفسها لا تتغير في حمولة تحديثات الجودة، فإننا لا نتوقع أي تأثير إضافي يتعلق على وجه التحديد بمكونات Retail في الوقت الحالي.

## <a name="is-there-any-impact-to-cloud-hosted-environments-che"></a>هل هناك أي تأثير على البيئات المستضافة على الشبكة السحابية (CHE)؟ 
بيئات CHE خارج نطاق تحديثات الجودة لأنها خارج نطاق معاينة Microsoft.

## <a name="are-there-any-integration-issues-with-microsoft-dataverse"></a>هل يوجد أي مشكلات تكامل مع Microsoft Dataverse? 
ولا توجد مشكلات تكامل معروفه لتحديثات الجودة مع Dataverse.

