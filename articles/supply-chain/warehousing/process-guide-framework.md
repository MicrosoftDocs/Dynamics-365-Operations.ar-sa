---
title: إطار عمل دليل العملية
description: يوفر هذا المقال معلومات حول اطار عمل دليل العملية للمطورين الذين يقومون بتوسيع العمليات المتنقلة الخاصة بمستودعنا في XX++.
author: Mirzaab
ms.date: 11/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: e88f32e0347a808d03615cf85e50b1592d691670
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860424"
---
# <a name="process-guide-framework"></a>إطار عمل دليل العملية

[!include [banner](../includes/banner.md)]

يوفر هذا المقال معلومات حول اطار عمل دليل العملية للمطورين الذين يقومون بتوسيع العمليات المتنقلة الخاصة بمستودعنا في XX++. يتم توسيع عمليات الجوال الخاصة بالمستودع كنتيجة للعمليات التي يتم تقسيمها إلى خطوات صغيره. تم استخراج التسلسل التجاري وبناء واجهه المستخدم لكل خطوه في فئات فرديه ، والتي تتيح امكانيه التوسع.

## <a name="overview-of-the-existing-design"></a>نظره عامه علي التصميم الموجود

تعرض تدفقات تنفيذ الاجهزه المحمولة للمستودع خلال نقطه نهاية خدمه مخصصه واحده. ويصل الطلب من تطبيق الاجهزه المحمولة علي شكل سلسله XML ، والذي يحتوي علي بيانات تعريف واجهه المستخدم المقدمة في تطبيق الاجهزه المحمولة ، بالاضافه إلى القيم التي تم إدخالها بواسطة المستخدم.

عند استلام الطلب ، تكون الخطوة الاولي هي إلغاء تسلسل XML هذا. تحول الفئة **WHSMobileAppServiceXMLTranslator** إلى حاويه تحتوي علي كل من معلومات التحكم ، بالاضافه إلى معلومات الجلسة.

بذلك ، يتم استخدام المعلومات الموجودة في الحاوية لتقرير اي عمليه المستودع التي يقوم المستخدم بالعمل عليها ، أو علي وشك البدء (تعداد **WHSWorkExecuteMode**) ، ووفقا لذلك يتم إنشاء مثيل لفئة مشتقه من **WHSWorkExecuteDisplay**. يتم استدعاء الأسلوب **displayform()** ، والذي يقوم بعد ذلك بما يلي:

-   يقوم بمعالجه البيانات من المستخدم (المفوض إلى الفئة **WHSRFControlData** ، ولكن هناك بعض العمليات التي تقوم بتنفيذ منطق معين بواسطة تجاوز أسلوب **processControl()**).

-   تنفيذ منطق العمل.

-   زيادة الخطوة.

-   يبني الحاوية التي تمثل واجهه المستخدم الجديدة (عاده في أسلوب **build…()**).

ويتم بعد ذلك إرجاع الحاوية إلى المترجم ، والذي يقوم بعد ذلك إنشاء تسلسل XML ، وإرسالها مره أخرى كاستجابة للجهاز المحمول.

يعرض مخطط التسلسل التالي نظرة عامة على تدفق التنفيذ. لاحظ ان الرسم التخطيطي هو أكثر من نظره عامه منظمة وليس تمثيل 1:1 للتعليمات البرمجية الفعلية.

![نظرة عامة منظمة على العملية.](media/schematic-overview.png) 

### <a name="reason-for-the-redesign"></a>سبب إعادة التصميم

يقدم التصميم أعلاه اطار عمل بسيط للغاية لإنشاء العمليات المستخدمة في تدفقات الهواتف الجوالة. ومع ذلك ، كما هو موضح أعلاه ، تستخدم أساليب **displayform()** العديد من المسؤوليات. وهي تقوم بتفويضها إلى أساليب وفئات أخرى ولكن في غياب المسؤوليات الملموسة في الفئات ، فانه يتم العمل بطريقه غير متناسقة عبر الفئات. أيضا ، كلما زاد عدد السيناريوهات المعتمدة في زيادة أصلية ، فان بعض هذه الفئات يمكن ان تصبح معقده تماما. لجعل الأمور أكثر تشويقا ، يتم تجاوز بعض هذه الفئات/الأساليب وأعاده استخدامها في أوضاع متعددة. والنتيجة هي الأساليب الطويلة للغاية بتعقيد عالي سيكلوماتيك. وهذه الإصدارات واجهت مشكلات الصيانة في الماضي. إصلاح الأخطاء في هذه الأساليب قد خطر والانحدار عرضه.
علي سبيل المثال ، يتم الاشاره إلى الأسلوب **processWorkLine()** الموجود في الفئة **WhsWorkExecuteDisplay** من العمليات المتعددة (بشكل أساسي ، في اي مكان يتم فيه تنفيذ العمل).

لجعل هذه الخيارات القابلة للتوسع ، فان أحد الخيارات سيقوم بتقسيم أساليب **displayForm** إلى أساليب أصغر وتقديم نقاط القابلية للتوسعة. ومع ذلك ، وبسبب مصفوفة السيناريو ، سيكون من الصعب علي الشركاء كتابه الملحقات والتحقق من صحتها مقابل التراجع. ليس فقط هذا بسبب نقص توزيع المسؤوليات المهيكلة المذكورة أعلاه ، فان التعليمات البرمجية ستكون متزايدة في الطرق غير المتوقعة بمرور الوقت ، واجهت التحديات في امتدادات جوده الإنشاء.

ونتيجة لذلك ، يعد أعاده التصميم هو الخيار المستدام ، مع هدف للحصول علي الفئات المعرفة بوضوح بوجود مسؤوليات مستقله. يجب ان يكون للفئة مسؤوليه واحده وسبب واحد للتغيير وسبب واحد ليتم توسيعه.

## <a name="design-overview"></a>نظره عامه علي التصميم

في اطار العمل المعاد تصميمه ، ريفولفيس الاستراتيجية الاساسيه حول المبادئين التاليتين: تقسيم تدفق التنفيذ إلى مكونات فرديه بمسؤوليات محدده بشكل جيد والتي لها نقاط امتداد جيده في كل مكون.

اسم اطار العمل الجديد هو "ProcessGuide". وهذا لان أيم هذه الفئات لإرشاد المستخدم من خلال عمليه تجاريه (مقارنه بالعميل الغني والذي يعد خبرات تستند إلى النماذج حيث يوجد للمستخدم مرونة أكثر في كيفيه تفاعلها مع البيانات أو بالترتيب الذي يقومون به بأداء المهام).

> [!NOTE]
> التفصيل الأكثر اهميه هو حذف البادئة "WHS" عن عمد. في حين تقديم العمليات المتنقلة مبدئيا لتخزينها ، فانه من المقرر ان يكون لها حدود تم تجاوزها لدعم عمليات الإنتاج المتنوعة وأداره المخزون. ونتيجة لذلك ، تم استبعاد مرجع المستودع في اسم اطار العمل.

لتحديد المكونات ، تتمثل الخطوة الاولي في النظر إلى عمليه بدء الإنتاج (الفئة **WhsWorkExecuteDisplayProdStart**). فيما يلي مخطط العملية.

![صوره العملية المنظمة.](media/production-start-process-schematic.png)

بالنظر إلى تدفق عناصر التحكم ، ما يلي هو المكونات المطلوبة:

-   وحده تحكم للتنقل عبر العملية التجارية بالكامل.
-   خطوه مسؤوله عن تنفيذ خطوه في العملية.
-   معالج بيانات لمعالجه البيانات في أحدي الخطوات.
-   منشئ صفحات مسؤول عن إنشاء واجهه المستخدم لأحدي الخطوات.
-   وكيل تنقل مسؤول عن انتقال الخطوة.
-   فئة مسؤوله عن تنفيذ العملية التجارية.

في الرسم التخطيطي لتدفق العملية أعلاه ، إذا قمت بالبدء في الخطوة 1 وبدء معالجه البيانات من الخطوة السابقة ، ثم الانتهاء من إنشاء واجهه مستخدم ، سيستمر معالجه البيانات في الخطوة التالية. وهذا يقدم ازدواجا مشدودا بين الخطوات المتتالية ، ونتيجة لذلك ، ستبدو العملية المنظمة الجديدة عاليه المستوي كما يلي:

![صوره للعمليه المنظمة العالية المستوي.](media/high-level-schematic.png)

فيما يلي المكونات الاساسيه في العملية التي تمت أعاده تصميمها:

-   **ProcessGuideController** -هذه الفئة تنسق التنفيذ الإجمالي لعمليه الاعمال. وهو يحدد المصانع التي تقوم بإنشاء مثيل للخطوة وعامل التنقل ، والذي يشكل بشكل لاحق تنفيذ العملية ، بالاضافه إلى منطق التنظيف للإلغاء أو إنهاء العملية.

-   **ProcessGuideStep** -تمثل هذه الفئة خطوه واحده في العملية التجارية. تحتوي هذه الفئة علي تعريف لوحده المصانع التي تقوم بإنشاء مثيل للصفحة والإجراءات ومعالجات البيانات ويكون مسؤولا عن استدعاءها بالتسلسل الصحيح.

-   **ProcessGuideNavigationAgent** -هذه الفئة مسؤوله عن التنقل بين الخطوات. عند اكتمال أحدي الخطوات ، يكون عامل التنقل مسؤولا عن تعريف الخطوة التالية ويمرر إيه معلمات قد تحتاجها الخطوة السابقة للاتصال بالخطوة التالية.

-   **ProcessGuidePageBuilder** -هذه الفئة مسؤوله عن إنشاء واجهه مستخدم.

-   **ProcessGuideAction** -تمثل هذه الفئة إجراءا ، يظهر كزر للمستخدم.

-   **ProcessGuideDataProcessor** -هذه الفئة مسؤوله عن معالجه المستخدم الذي ادخل البيانات في أحد الحقول.

## <a name="execution-flow"></a>تدفق التنفيذ.

نقطه بداية تدفق التنفيذ تبقي بدون تغيير. ولذلك ، لا يزال الطلب يصل خلال نفس نقاط النهاية ، متبوعا بإلغاء تسلسل XML في الحاوية. ثم يتم تمرير هذه الحاوية إلى **getNextFormState()**.

توجد ثلاث فئات هامه للملاحظة:

-  **ProcessGuideSessionState** -يتضمن ذلك معلومات حاله جلسة العمل – الوضع والنجاح ووحده التحكم والخطوة التي يتم تنفيذها ، وهكذا.

-  **ProcessGuidePage** – يحتوي هذا علي تمثيل ذي نوع قوي لبيانات تعريف واجهه المستخدم.

-  **ProcessGuideRequest** -يحتوي هذا علي العضوين السابقين كعضو وهو تمثيل ذي نوع قوي للطلب الذي تم استلامه من الجهاز المحمول.

يتم إنشاء هذه الفئات باستخدام معلومات الحاوية (كلا من الحالة وبيانات عنصر التحكم التي قام المستخدم بإدخالها). ويوفر ذلك طريقه أمنه النوع للوصول إلى القيم ومعالجتها. بالمقارنة مع الوصول المتكرر للحاويه اثناء العملية ، يوفر ذلك الميزة بالاضافه إلى امكانيه القراءة والأداء.

يتم استخدام معلومات حاله جلسة العمل لإنشاء مثيل لفئة **ProcessGuideController** الصحيحة. بمجرد إنشاء مثيل لها ، يتم استدعاء الأسلوب **createResponse()** في الفئة **ProcessGuideController**. ويعد هذا الأسلوب نقطه الإدخال إلى منطق دليل العملية ، وبعد التنفيذ ، تعيد الاستجابة (الممثلة في الفئة **ProcessGuideResponse**). يتم بعد ذلك تحويل الاستجابة مره أخرى إلى الحاوية والتسليم للخلف إلى المنطق القديم ، والذي يقوم بإنشاء تسلسل في XML وترسل الاستجابة إلى الجهاز المحمول مره أخرى.

بعد ذلك ، يحتاج جهاز التحكم إلى العثور علي الخطوة التالية لتنفيذها. إذا كانت هذه هي بداية عمليه جديده ، فسوف تستدعي وحده التحكم **initialStep()** للحصول علي الخطوة الاولي في العملية. بعد ذلك ، فانه سيستدعي أسلوب **execute()** في **ProcessGuideStep**. ومن ثم ، قد تقوم هذه الطريقة بإنشاء فئة **ProcessGuidePageBuilder** واستدعاء **buildPage()** ، والذي ينتج عنه كائن **ProcessGuidePage**، وهو تمثيل ظاهري لواجهه المستخدم التي سيتم تقديمها إلى المستخدم. ستقوم الخطوة بعد ذلك بإرسال النتيجة إلى وحده التحكم ، التي ستقوم بعد ذلك بحفظ حاله جلسة العمل الحالية ثم إرجاع النتيجة مره أخرى إلى **getNextFormState()** في نموذج الفئة **ProcessGuideResponse**. وبعد ذلك ، يتم تحويل الاستجابة مره أخرى إلى الحاوية ، التالي يتم إنشاء تسلسل إلى XML وترسل الاستجابة إلى الجهاز المحمول.

يشرح مخطط التسلسل التالي تدفق عنصر التحكم هذا. لاحظ ان هذا هو تدفق عنصر التحكم الأكثر شيوعا بشكل مبسط لشرح التصميم.

![تدفق التحكم المبسط.](media/control-flow.png)

عندما يقوم المستخدم باجراء علي الجهاز المحمول بالنقر فوق زر (أو مسح القيمة – التي عاده ما يقوم بتشغيل الاجراء الافتراضي) – يصل الطلب إلى الأسلوب **createResponse()** في الفئة **ProcessGuideController** من خلال نفس المسار. ومع ذلك ، علي الرغم من ذلك ، يعرف جهاز التحكم بمعلومات حاله جلسة العمل التي يوجد فيها المستخدم. ووفقا لذلك ، يقوم بإنشاء فئة **ProcessGuideStep** المناسبة واستدعاء أسلوب execute. **ProcessGuideStep** ، بدوره ، تقرا اسم الاجراء الذي قام المستخدم باستدعاءه ثم يقوم بإنشاء مثيل لفئة **ProcessGuideAction** المناسبة واستدعاءات **execute()**.

فئة **ProcessGuideAction** مسؤوله عن تنفيذ الاجراء المحدد ، علي الرغم من وجود استثناءين للاجراء.

الأول هو الفئة **ProcessGuideOKAction**. يشير هذا الاجراء إلى ان المستخدم يريد التاكيد والانتقال للامام في العملية. وفقا لهذا الأسلوب-يقوم فعلا بالرد علي الفئة ProcessGuideStep، مما يعني ان الخطوة تستدعي **processData()** في **ProcessGuideDataProcessor**. وهذا يقوم بمعالجه البيانات التي قام المستخدم بإدخالها ، ثم يقوم بتحديث حاله الخطوة وإرسال النتيجة إلى وحده التحكم. استنادا إلى نتيجة المعالج ، تقوم الخطوة باستدعاء منشئ الصفحة لبناء واجهه المستخدم المناسبة أو تعيين حاله الخطوة كمكتملة. وينعكس ذلك في النصف العلوي من مخطط التسلسل أدناه.

والاستثناء الآخر هو اجراء إلغاء ، الذي تم تنفيذه في الفئتين **ProcessGuideCancelResetProcessAction** و **ProcessGuideCancelExitProcessAction**. تمثل هذه الإجراءات هدفا للغاء العملية والعودة اما إلى بداية العملية أو إنهاء العملية تماما. مثل الاجراء **موافق**، تنفذ هذه الإجراءات أيضا ردا علي الخطوة ، التي تشير إلى الهدف **ProcessGuideController**. ثم يقوم جهاز التحكم بتنفيذ التنظيف الضروري لمتغيرات الحالة ونقل عنصر التحكم إلى الخطوة الاولي في العملية أو إنهاء العملية تماما.

بعد إتمام الخطوة ، إذا تم تعيين حاله الخطوة علي **مكتمل**، فان وحده التحكم تقوم بإنشاء مثيل **ProcessGuideNavigationAgent** ، والذي يقوم بإرجاع اسم الخطوة التالية. ثم يقوم جهاز التحكم بإنشاء مثيل لهذه الخطوة واستدعاء أسلوب **execute()** – وتستمر الدورة. وبشكل عام ، تقوم الخطوة الجديدة باستدعاء **ProcessGuidePageBuilder** المقابلة لبناء واجهه المستخدم لعرض الشاشة التالية التي سيتم تقديمها للمستخدم ، والتي يتم بعد ذلك إرسالها مره أخرى. وينعكس ذلك التدفق في النصف السفلي من مخطط التسلسل أدناه.

![مخطط التسلسل.](media/sequence-diagram.png)

## <a name="building-a-new-process-using-the-processguide-framework"></a>إنشاء عمليه جديده باستخدام إطار عمل ProcessGuide

أفضل طريقه لشرح تدفق عناصر التحكم هي استخدام مثال موجود في التطبيق – عمليه بدء الإنتاج.

## <a name="overview-of-the-production-start-process"></a>نظرة عامة على عملية بدء الإنتاج

هيا نبدا باستيعاب تدفق العمليات. في الخطوة الاولي ، تتم مطالبه المستخدم بمعرف أمر الإنتاج.

![المطالبة بمعرف الإنتاج.](media/production-id-prompt.png)

عند قيام المستخدم بإدخال معرف أمر الإنتاج ، يتم التحقق من صحة رقم الأمر. وتعتمد بعض عمليات التحقق من الصحة التي يتم تشغيلها علي ما إذا كان الأمر في نفس المستودع اثناء قيام المستخدم بتسجيل الدخول إلى ، وحاله الأمر. في حاله فشل التحقق من الصحة ، يتم عرض رسالة خطا للمستخدم. في حاله نجاح عمليه التحقق من الصحة ، يقوم المستخدم بعرض تفاصيل أمر الإنتاج والصنف.

يمكن للمستخدم اما إلغاء الأمر للعودة إلى بداية العملية أو النقر فوق **موافق** للتاكيد. في الحالة الثانية ، يتم تعيين أمر الإنتاج إلى الحالة **تم البدء** ، ويتم ترحيل دفاتر اليومية المقابلة ، ثم ينتقل عنصر التحكم إلى الخطوة الاولي ، وتظهر رسالة "العمل المنجز" للمستخدم.


## <a name="creating-the-controller"></a>إنشاء عنصر التحكم

الخطوة الاولي في بناء العملية التجارية تقوم بإنشاء فئة وحده التحكم ، توسيع من الفئة **ProcessGuideController** المجردة التي تقوم بتنفيذ السلوكيات الافتراضية لوحده التحكم. اسم الفئة الجديدة هو **ProdProcessGuideProductionStartController** ويتم تزيينها بقيمه **WHSWorkExecuteMode** التي تساوي **StartProdOrder**. يتم استخدام نفس المثيل المستند إلى **SysExtension** الذي تم استخدامه في الفئات **WHSWorkExecuteDisplay**، والذي يساعد علي إنشاء مثيل لجهاز التحكم عندما يقوم المستخدم بتنفيذ عنصر قائمه لهذا الوضع.

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode::StartProdOrder)]
public class ProdProcessGuideProductionStartController extends ProcessGuideController
```

> [!NOTE]
> نمط التسمية للفئة هو **\<FunctionalArea\>ProcessGuide\<Businessprocessname\>وحده تحكم**. هذا هو النمط المستخدم لفئات وحده التحكم ولتوسيعها إلى الفئات الأخرى.


## <a name="building-the-first-step"></a>بناء الخطوة الاولي

بعد ذلك ، لتعريف الخطوة الاولي التي تقوم فيها بإنشاء فئة **ProdProcessGuidePromptProductionIdStep**، توسيع من **ProcessGuideStep**.

يتم تفويض مهمة إنشاء الفئة إلى مصنع خطوه ، والذي يتم استدعاؤه بواسطة الفئة الاساسيه **ProcessGuideController**. يقوم تنفيذ المصنع الافتراضي بإنشاء مثيل للخطوة بناء علي الاسم. ولذلك ، لإنشاء مثيل **ProdProcessGuidePromptProductionIdStep** كخطوه اولي في جهاز التحكم ، يجب عليك القيام بشيئين:

-   قم بتزيين الفئة **ProdProcessGuidePromptProductionIdStep** بالسمة **ProcessGuideStepName**.

    ```xpp
    [ProcessGuideStepName(classStr(ProdProcessGuidePromptProductionIdStep))] public class ProdProcessGuidePromptProductionIdStep extends ProcessGuideStep
    ```

-   في فئة وحده التحكم ، قم بتنفيذ الأسلوب المجرد **initialStepName()** لإرجاع اسم الخطوة.

    ```xpp
    protected final ProcessGuideStepName initialStepName()
    {
        return classStr(ProdProcessGuidePromptProductionIdStep);
    }
    ````   
    
> [!NOTE]
> القيمة الموجودة في السمة **ProcessGuideStepName** لا تحتاج تماما إلى مطابقه اسم الفئة كما هو موضح أعلاه. ومع ذلك ، فان تنفيذ ذلك يسمح بالتوحيد وأمان النوع حول المراجع التبادلية عند استخدام الفئة. يوصي باستخدام اصطلاح التسمية هذا.
>
> يتم تنفيذ الإنشاء المستند إلى **ProcessGuideStepName** من خلال الخطوة في الفئة **ProcessGuideStepDefaultFactory**. في الحالة النادرة التي ترغب في ان تقوم فيها استراتيجية مختلفه بإنشاء مثيل للخطوة ، تحتاج إلى القيام بما يلي:
> -   إنشاء فئة مصنع جديده ترث من **ProcessGuidStepAbstractFactory**.
> -   بشكل اختياري ، قم بإنشاء فئة معلمه جديده تقوم بتطبيق واجهه **ProcessGuideIStepCreationParameters**، والتي تحتوي علي المعلمات التي يحتاجها المصنع.
> -   في فئة وحده التحكم الخاصة بك ، قم بتجاوز أساليب **stepFactory()** و **stepCreationParameters()** لإرجاع المصنع السابق والمعلمات.

الخطوة التالية هي تنفيذ وظيفة الفئة  **ProdProcessGuidePromptProductionIdStep**. تحتاج لتطبيق المنطق لإنشاء واجهه المستخدم ، ومعالجه البيانات المدخلة من قبل المستخدم ، وتحديد الوقت الذي تكتمل فيه الخطوة.

### <a name="building-the-user-interface-for-the-first-step"></a>بناء واجهه المستخدم للخطوة الاولي.

يتم إنشاء واجهه المستخدم باستخدام فئة ترث من الفئة **ProcessGuidePageBuilder** المجردة. بالنسبة لهذه الخطوة ، قم بتسميه الفئة لتمثل ما يفعله – **ProdProcessGuidePromptProductionIdPageBuilder**.

اليه إنشاء المثيل للفئة تشبه كيفيه إنشاء مثيل للخطوة من وحده التحكم. 

-   قم بتزيين الفئة **ProdProcessGuidePromptProductionIdPageBuilder** بالسمة **ProcessGuidePageBuilderName**.

    ```xpp
    [ProcessGuidePageBuilderName(classStr(ProdProcessGuidePromptProductionIdPageBuilder))] public class ProdProcessGuidePromptProductionIdPageBuilder extends ProcessGuidePageBuilder
    ```

-   في الفئة **ProdProcessGuidePromptProductionIdStep**، قم بتطبيق الأسلوب المجرد **pageBuilderName()** لإرجاع هذا الاسم.

    ```xpp
    protected final ProcessGuidePageBuilderName pageBuilderName()
    {
        return classStr(ProdProcessGuidePromptProductionIdPageBuilder);
    }
    ```    

> [!TIP]
> وبشكل مشابه لمنشئ الخطوة ، يوجد أيضا نمط مصنع تجريدي يتم تطبيقه لمصنع منشئ الصفحة. في الحالة النادرة التي ترغب في ان تقوم فيها استراتيجية مختلفه بإنشاء مثيل منشئ الصفحات، يمكنك القيام بما يلي:
> - إنشاء فئة مصنع جديده ترث من **ProcessGuidePageBuilderAbstractFactory**.
> - بشكل اختياري ، قم بإنشاء فئة معلمه جديده تقوم بتطبيق واجهه **ProcessGuideIPageBuilderCreationParameters**، والتي تحتوي علي المعلمات التي يحتاجها المصنع.
> - في فئة وحده التحكم الخاصة بك ، قم بتجاوز أساليب **pageBuilderFactory()** و **pageBuilderCreationParameters()** لإرجاع المصنع السابق والمعلمات.

لتطبيق واجهه المستخدم ، تحتاج إلى صفحه تحتوي علي مربع نص واحد لإدخال معرف أمر الإنتاج ، بالاضافه إلى زر **موافق** والزر **إلغاء الأمر**. يجب ان يقوم الزر **إلغاء الأمر** بإنهاء العملية.

لتنفيذ ذلك ، تحتاج إلى تجاوز أسلوبين في الفئة **ProdProcessGuidePromptProductionIdPageBuilder**:

-   استخدم الأسلوب **addDataControls()** لأضافه مربع النص.

    ```xpp
    protected final void addDataControls(ProcessGuidePage _page)
    {
        _page.addTextBox(ProcessGuideDataTypeNames::ProdId, "@SYS4398", extendedTypeNum(ProdId));
    }
    ```   

-   استخدم الأسلوب **addActionControls()** لأضافه الزرين **موافق** و **إلغاء الأمر**.

    ```xpp
    protected final void addActionControls(ProcessGuidePage _page)
    {
        #ProcessGuideActionNames
        _page.addButton(step.createAction(#ActionOK), true);
        _page.addButton(step.createAction(#ActionCancelExitProcess));
    }
    ``` 

يؤدي هذا إلى أضافه عناصر تحكم البيانات ، متبوعه بالأزرار. ومع ذلك ، إذا كنت تريد إنشاء شاشه بعناصر تحكم بيانات وأزرار متداخلة، يمكنك تجاوز أسلوب **addControls()** بدلا من المرونة.

السيناريو الإضافي يعتبر كيفيه أعاده إنشاء الصفحة في حاله فشل التحقق من الصحة ، علي سبيل المثال ، إذا قام المستخدم بإدخال معرف أمر إنتاج غير صحيح. تقوم الفئة الاساسيه **ProcessGuidePageBuilder** بتطبيق السلوك الافتراضي ، والذي يعيد إنشاء واجهه المستخدم ، ويقوم بمسح القيمة الممسوحة ضوئيا ، وأضافه التحكم بالخطا مع رسالة الخطا. ونظرا لان هذا هو السلوك الافتراضي الذي ترغب في استخدامه ، فلن تحتاج إلى أضافه إيه تعليمه برمجيه لمعالجه الأخطاء.

> [!TIP]
> إذا كنت ترغب في تطبيق سلوك واجهه المستخدم المخصصة لحالات الخطا ، يمكنك تجاوز واحد أو أكثر من الأساليب **rebuildFromRequestPage()** و **isErrorState()** و **reuseRequestPageOnError()**.

### <a name="processing-the-user-entered-data-in-the-first-step"></a>معالجه البيانات المدخلة من قبل المستخدم في الخطوة الاولي

يتم اجراء معالجه البيانات في الفئة **ProcessGuideDataProcessorDefault**، والتي تقوم بدورها باستدعاء فئة **WhsRfControlData** القديمة. ولا يلزم اجراء إيه تغييرات لهذا السلوك الافتراضي ، و **WhsRfControlData** بالفعل منطق التحقق من صحة الحقل **ProdId**، التالي لا تحتاج إلى كتابه اي منطق لمعالجه هذا. في حاله الملحقات المطلوبة لمنطق التحقق من الصحة ، خذ بعين الاعتبار استخدام اليه الامتداد المستندة إلى **WhsControl**.

### <a name="determine-if-the-first-step-is-complete"></a>تحديد ما إذا كانت الخطوة الاولي مكتملة

وفي حاله نجاح عمليه التحقق من الصحة ، فان الوقت الذي يتم فيه وضع علامة علي الخطوة علي انها مكتملة. ويتم اجراء ذلك في الفئة الاساسيه ، ومع ذلك ، تحتاج إلى تطبيق الشرط لتحديد اكتمال الخطوة. والطريقة التي تم تجاوزها التالية هي ذلك.

```xpp
protected final boolean isComplete()
{
    WhsrfPassthrough pass = controller.parmSessionState().parmPass();
    ProdId prodId = pass.lookup(ProcessGuideDataTypeNames::ProdId);
        return (prodId != '');
}
```   

### <a name="step-two-view-order-details-and-confirm"></a>الخطوة الثانية: عرض تفاصيل الأمر والتاكيد

في الخطوة الثانية من العملية ، يظهر المستخدم شاشه تحتوي علي تفاصيل حول الأمر. يمكن للمستخدم اما النقر فوق الزر **موافق** لتاكيد بدء أمر الإنتاج ، أو النقر فوق **إلغاء الأمر** للرجوع إلى بداية العملية. علي سبيل المثال ، قم بتسميه الخطوة **ProdProcessGuideConfirmProductionOrderStep** وفئة منشئ الصفحة **ProdProcessGuideConfirmProductionOrderPageBuilder**

وتبدو الفئة ProdProcessGuideConfirmProductionOrderStep كما يلي.

```xpp
[ProcessGuideStepName(classStr(ProdProcessGuideConfirmProductionOrderStep))]
public class ProdProcessGuideConfirmProductionOrderStep extends ProcessGuideStep
{
    protected final ProcessGuidePageBuilderName pageBuilderName()
    {
        return classStr(ProdProcessGuideConfirmProductionOrderPageBuilder);
     }
}
```     

ونظرا لان المستخدم لا يدخل إيه قيم هنا ، فلن تحتاج إلى تجاوز الأسلوب **isComplete()**. يتم إكمال الخطوة عندما ينقر المستخدم فوق **موافق**.

تتجاوز فئة منشئ الصفحات أسلوب **addDataControls()** لأضافه ثلاث تسميات. تعرض التسمية الاوليه معرف أمر الإنتاج ، وتحتوي الثانية علي معلومات الصنف (مثل معرف الصنف أو الابعاد أو الوصف) ويحتوي الثالث علي الكمية ووحده القياس.

ويتم بعد ذلك تجاوز **addActionControls()** لأضافه 2 أزرار – الزر **موافق** والزر **إلغاء الأمر** لإلغاء العملية والرجوع إلى بداية العملية.

```xpp
/// <summary>
/// The <c>ProdProcessGuideConfirmProductionOrderPageBuilder</c> builds a page that allows the user to see details of a production order
/// and then confirm.
/// </summary>
[ProcessGuidePageBuilderName(classStr(ProdProcessGuideConfirmProductionOrderPageBuilder))]
public class ProdProcessGuideConfirmProductionOrderPageBuilder extends ProcessGuidePageBuilder
{
    protected void addDataControls(ProcessGuidePage _page)
    {
        WhsrfPassthrough pass = controller.parmSessionState().parmPass();
        ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
        UnitOfMeasureSymbol inventUOM = InventTableModule::find(prodTable.ItemId, ModuleInventPurchSales::Invent).UnitId;
        
        _page.addLabel(ProcessGuideDataTypeNames::ProdIdLabelName, strFmt("@WAX1684", prodTable.ProdId), extendedTypeNum(ProdId));
        _page.addLabel(ProcessGuideDataTypeNames::ItemInfo, this.generateItemInfoForProdId(pass.lookup(ProcessGuideDataTypeNames::ProdId)), extendedTypeNum(WHSRFUndefinedDataType));
        _page.addLabel(ProcessGuideDataTypeNames::QtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId)), inventUOM), extendedTypeNum(WHSRFQuantityAndUOM));

        if (PdsGlobal::pdsIsCWItem(prodTable.ItemId))
        {
            _page.addLabel(ProcessGuideDataTypeNames::InventQtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::pdsCWProposalStartupQty(prodTable.ProdId)), PdsCatchWeightItem::pdsCWUnitId(prodTable.ItemId)), extendedTypeNum(WHSRFQuantityAndUOM));
        }
    }

    protected void addActionControls(ProcessGuidePage _page)
    {
        #ProcessGuideActionNames
        _page.addButton(step.createAction(#ActionOK), true);
        _page.addButton(step.createAction(#ActionCancelResetProcess));
    }
```

> [!NOTE]
> يمكنك العثور علي نفس التعليمات البرمجية المصدر لأساليب X++ في هذا المقال باستخدام مستكشف التطبيق. عامل تصفيه علي اسم الفئة ، ثم انقر بزر الماوس الأيمن فوق اسم الفئة وحدد **عرض التعليمات البرمجية**.

### <a name="step-3-start-the-production-order"></a>الخطوة 3: بدء أمر الإنتاج

والخطوة الثالثة هي التي يتم فيها تنفيذ منطق تسلسل العمل لبدء أمر الإنتاج. تعد هذه الخطوة مختلفه إلى حد ما عن الخطوات السابقة ، وذلك في حاله ان هذه الخطوة لا تحتوي علي واجهه مستخدم. يتم تنفيذ هذه الخطوة دون مطالبه عند قيام المستخدم بالنقر فوق **موافق** في الخطوة السابقة.

تقوم الفئة **ProcessGuideStepWithoutPrompt** المجردة بتطبيق السلوك الافتراضي لمثل هذه الخطوات. ولذلك ، يجب ان تقوم الخطوة الحالية بتوسيع فئة **ProcessGuideStepWithoutPrompt** وتجاوز أسلوب **doExecute()**.

التعليمه البرمجية التالية توضح مثال لتطبيق الفئة والأسلوب **doExecute()**. ويقوم الأسلوب ببساطه باسترداد معرف الأمر ومعرف المستخدم من حاله جلسة العمل واستدعاء الأسلوب لبدء أمر الإنتاج هذا.

```xpp
/// <summary>
/// The <c>ProdProcessGuideStartProductionOrderStep</c> represents a step that starts a production order.
/// </summary>
[ProcessGuideStepName(classStr(ProdProcessGuideStartProductionOrderStep))]
public class ProdProcessGuideStartProductionOrderStep extends ProcessGuideStepWithoutPrompt
{
    protected final void doExecute()
    {
        WhsrfPassthrough pass = controller.parmSessionState().parmPass();
        WHSUserId userId = pass.lookup(ProcessGuideDataTypeNames::UserId);
        ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
        WhsWorkExecute workExecute = WhsWorkExecute::construct();
        workExecute.prodStartUp(prodTable.ProdId, ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId), userId);

        this.addProcessCompletionMessage();

        super();
    }

}
```

في حاله الاستثناء ، يضمن المنطق الخاص بمعالجه استثناء اطار العمل ان العملية تراجعت إلى الخطوة السابقة.

> [!NOTE]
> يضيف استدعاء ل **addProcessCompletionMessage()** الرسالة "العمل المنجز" إلى معلمات التنقل. ستعرض الخطوة التالية (بفرض ان لديها واجهه مستخدم) هذه الرسالة. وتعالج الفئات الاساسيه هذا المنطق ، ولا يلزم أضافه إيه تعليمات برمجيه محدده إلى فئات العملية لتحقيق هذا السلوك.


### <a name="building-the-navigation-through-the-steps"></a>بناء التنقل من خلال الخطوات التالية

الفئة الاساسيه **ProcessGuideController** بإنشاء مثيل للفئة **ProcessGuideNavigationAgentDefault**، والتي تعتمد علي مسار التنقل المعرف مسبقا ، وهو عبارة عن خريطة بسيطه لخطوات المصدر والوجهة. بالنسبة لسيناريو بدء الإنتاج ، نظرا لعدم وجود اي منطق تفريعي شرطي ، فان هذا التطبيق يكفي. ولذلك ، تحتاج فقط إلى تجاوز الأسلوب **إinitializeNavigationRoute()** لتحديد مسار التنقل.

```xpp
    protected ProcessGuideNavigationRoute initializeNavigationRoute()
    {
        ProcessGuideNavigationRoute navigationRoute = new ProcessGuideNavigationRoute();
        navigationRoute.addFollowingStep(classStr(ProdProcessGuidePromptProductionIdStep), classStr(ProdProcessGuideConfirmProductionOrderStep));
        navigationRoute.addFollowingStep(classStr(ProdProcessGuideConfirmProductionOrderStep), classStr(ProdProcessGuideStartProductionOrderStep));
        navigationRoute.addFollowingStep(classStr(ProdProcessGuideStartProductionOrderStep), classStr(ProdProcessGuidePromptProductionIdStep));

        return navigationRoute;
    }
```

هناك عمليات يتم فيها وجود منطق تفريعي شرطي (استنادا إلى إجراءات المستخدم أو إيه شروط أخرى). تحتاج مثل هذه العمليات للقيام بما يلي:

-   تنفيذ عوامل التنقل المحددة الموروثة من الفئة **ProcessGuideNavigationAgent**.

-   تطبيق مصنع وكيل التنقل الذي تم توريثه من الفئة **ProcessGuideNavigationAgentAbstractFactory**، التي تحتوي علي منطق لإنشاء مثيل عامل التنقل الصحيح استنادا إلى الخطوة الحالية أو حاله جلسة العمل أو اجراء المستخدم أو اي منطق آخر.

-   بشكل اختياري ، قم بتجاوز **navigationAgentCreationParameters()** في فئة وحده التحكم لتمرير المعلمات المناسبة.

-   تجاوز **navigationAgentFactory()** في وحده التحكم لإنشاء منشئ عميل عامل التنقل الذي تم إنشاؤه أعلاه.

### <a name="action-classes"></a>فئات الإجراءات

تمثل فئات الإجراءات إجراءات المستخدم ، لذلك يستخدم هذا المثال الاجراء **موافق** لإظهار كيفيه إنشاء الإجراءات.

```xpp
[ProcessGuideActionName(#ActionOK)]
public class ProcessGuideOKAction extends ProcessGuideAction
{
    public final str label()
    {
        return "@SYS5473";
     }
     protected final void doExecute()
     {
        step.executeOKAction();
      }
}
```    

يجب ان تطبق الفئة الأساليب التجريدية 2.

-   **label()** ، الذي يرجع التسمية التي سيتم عرضها في عنصر تحكم الزر المرتبط بهذا الاجراء.

-   **doExecute()** ، الذي يقوم بتنفيذ الاجراء. كما ذكر سابقا ، يقوم الزر **موافق** ببساطه بتنفيذ رد علي الخطوة. ومع ذلك ، قد يكون للإجراءات الأخرى منطق أكثر تعقيدا.

يتم إنشاء مثيل للإجراءات باستخدام **SysExtension** علي أساس سمه **ProcessGuideActionName**. مثل إنشاء مثيل لمنشئي الصفحات ، فئة الخطوة تقوم بتطبيق منشئ الاجراء الافتراضي ، ومن الممكن تجاوز ذلك. يضيف منشئ الصفحة عنصر تحكم زر مثل هذا.

```xpp
_page.addButton(step.createAction(#ActionOK), true);
```

وفي هذه المرحلة ، يطلب منك الخطوة إنشاء فئة اجراء للاسم الذي تم تمريره ويربط ذلك الاجراء بالزر.

### <a name="summary"></a>ملخص

لتلخيص كل ما تم شرحه في هذا المقال، فيما يلي ملخص شامل للتعليمات البرمجية اللازمة للعملية:

1.  **ProdProcessGuideProductionStartController**

    1.  قم بتجاوز **initialStepName()** لتوفير اسم الخطوة الاولي.
    2.  تجاوز **initializeNavigationRoute()** لإنشاء مخطط التنقل.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideProductionStartController</c> class is the controller class for the production order start process guide.
        /// </summary>
        [WHSWorkExecuteMode(WHSWorkExecuteMode::StartProdOrder)]
        public class ProdProcessGuideProductionStartController extends ProcessGuideController
        {
            protected ProcessGuideStepName initialStepName()
            {
                return classStr(ProdProcessGuidePromptProductionIdStep);
            }

            protected ProcessGuideNavigationRoute initializeNavigationRoute()
            {
                ProcessGuideNavigationRoute navigationRoute = new ProcessGuideNavigationRoute();
                navigationRoute.addFollowingStep(classStr(ProdProcessGuidePromptProductionIdStep), classStr(ProdProcessGuideConfirmProductionOrderStep));
                navigationRoute.addFollowingStep(classStr(ProdProcessGuideConfirmProductionOrderStep), classStr(ProdProcessGuideStartProductionOrderStep));
                navigationRoute.addFollowingStep(classStr(ProdProcessGuideStartProductionOrderStep), classStr(ProdProcessGuidePromptProductionIdStep));

                return navigationRoute;
            }

        }
        ```

2.  **ProdProcessGuidePromptProductionIdStep**

    1.  تجاوز **isComplete()** لتحديد الوقت الذي تعتبر فيه الخطوة كامله.
    2.  تجاوز **pageBuilderName()** لتحديد منشئ الصفحة الذي سيتم استخدامه.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuidePromptProductionIdStep</c> represents a step that 
        /// that prompts the user for a production order id.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuidePromptProductionIdStep))]
        public class ProdProcessGuidePromptProductionIdStep extends ProcessGuideStep
        {
            protected boolean isComplete()
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                ProdId prodId = pass.lookup(ProcessGuideDataTypeNames::ProdId);

                return (prodId != '');
            }

            protected ProcessGuidePageBuilderName pageBuilderName()
            {
                return classStr(ProdProcessGuidePromptProductionIdPageBuilder);
            }

        }
        ```

3.  **ProdProcessGuidePromptProductionIdPageBuilder**

    1.  تجاوز **addDataControls()** لأضافه مربع نص **معرف الإنتاج**.
    2.  تجاوز **addActionControls()** لأضافه الزرين **موافق** و **إلغاء الأمر**.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuidePromptProductionIdPageBuilder</c> class builds a page 
        /// that prompts the user for a production order id.
        /// </summary>
        [ProcessGuidePageBuilderName(classStr(ProdProcessGuidePromptProductionIdPageBuilder))]
        public class ProdProcessGuidePromptProductionIdPageBuilder extends ProcessGuidePageBuilder
        {
            protected void addDataControls(ProcessGuidePage _page)
            {
                _page.addTextBox(ProcessGuideDataTypeNames::ProdId, "@SYS4398", extendedTypeNum(ProdId));
            }

            protected void addActionControls(ProcessGuidePage _page)
            {
                #ProcessGuideActionNames
                _page.addButton(step.createAction(#ActionOK), true);
                _page.addButton(step.createAction(#ActionCancelExitProcess));
            }

        }
        ```

4.  **ProdProcessGuideConfirmProductionOrderStep**

    1.  تجاوز **pageBuilderName()** لتحديد منشئ الصفحة الذي سيتم استخدامه.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideConfirmProductionOrderStep</c> class represents the step for viewing production order
        /// details and confirming the same.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuideConfirmProductionOrderStep))]
        public class ProdProcessGuideConfirmProductionOrderStep extends ProcessGuideStep
        {    
            protected ProcessGuidePageBuilderName pageBuilderName()
            {
                return classStr(ProdProcessGuideConfirmProductionOrderPageBuilder);
            }

        }
        ```

3.  **ProdProcessGuideConfirmProductionOrderPageBuilder**

    1.  تجاوز **addDataControls()** لأضافه تسميات معلومات الأمر والصنف والكمية.

    2.  تجاوز **addActionControls()** لأضافه الزرين **موافق** و **إلغاء الأمر**.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideConfirmProductionOrderPageBuilder</c> builds a page that allows the user to see details of a production order
        /// and then confirm.
        /// </summary>
        [ProcessGuidePageBuilderName(classStr(ProdProcessGuideConfirmProductionOrderPageBuilder))]
        public class ProdProcessGuideConfirmProductionOrderPageBuilder extends ProcessGuidePageBuilder
        {
            protected void addDataControls(ProcessGuidePage _page)
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
                UnitOfMeasureSymbol inventUOM = InventTableModule::find(prodTable.ItemId, ModuleInventPurchSales::Invent).UnitId;

                _page.addLabel(ProcessGuideDataTypeNames::ProdIdLabelName, strFmt("@WAX1684", prodTable.ProdId), extendedTypeNum(ProdId));
                _page.addLabel(ProcessGuideDataTypeNames::ItemInfo, this.generateItemInfoForProdId(pass.lookup(ProcessGuideDataTypeNames::ProdId)), extendedTypeNum(WHSRFUndefinedDataType));
                _page.addLabel(ProcessGuideDataTypeNames::QtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId)), inventUOM), extendedTypeNum(WHSRFQuantityAndUOM));

                if (PdsGlobal::pdsIsCWItem(prodTable.ItemId))
                {
                    _page.addLabel(ProcessGuideDataTypeNames::InventQtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::pdsCWProposalStartupQty(prodTable.ProdId)), PdsCatchWeightItem::pdsCWUnitId(prodTable.ItemId)), extendedTypeNum(WHSRFQuantityAndUOM));
                }
            }

            protected void addActionControls(ProcessGuidePage _page)
            {
                #ProcessGuideActionNames
                _page.addButton(step.createAction(#ActionOK), true);
                _page.addButton(step.createAction(#ActionCancelResetProcess));
            }

        ```

        > [!NOTE]
        > يتم استبعاد الأسلوب **generateItemInfoForProdId()** المستخدم لإنشاء تسميات معلومات الصنف من هذا المقال. يستعلم هذا الأسلوب عن جداول قليله للحصول علي معرف الصنف ووصفه وابعاده. إذا كنت تريد فهم أفضل **generateItemInfoForProdId()** ، انظر إلى التعليمات البرمجية المصدر.

4.  **ProdProcessGuideStartProductionOrderStep**

    1.  تجاوز **doExecute()** لاجراء عمليه بدء الإنتاج وأضافه رسالة إكمال العملية.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideStartProductionOrderStep</c> represents a step that starts a production order.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuideStartProductionOrderStep))]
        public class ProdProcessGuideStartProductionOrderStep extends ProcessGuideStepWithoutPrompt
        {
            protected final void doExecute()
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                WHSUserId userId = pass.lookup(ProcessGuideDataTypeNames::UserId);
                ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
                WhsWorkExecute workExecute = WhsWorkExecute::construct();
                workExecute.prodStartUp(prodTable.ProdId, ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId), userId);

                this.addProcessCompletionMessage();

                super();
            }

        }
        ```

> [!NOTE]
> لاحظ انه يوجد الكثير من النقوش الشائعة (أعاده إنشاء واجهه مستخدم عند حدوث خطا ، وتعيين رسالة إكمال العملية ، سلوك **موافق** و **إلغاء**) إلى اطار العمل – التالي حفظ مطور التطبيق من كتابه التعليمات البرمجية المتداولة التي تكون عرضه للخطا ، ولها مخاطره في سلوك غير متناسق عبر العمليات. حيث يحتاج السيناريو لديفيت من المسار الشائع ، علي الرغم من ذلك ، يوفر مطور التطبيق خيار تجاوز الأساليب المناسبة – ولكنه بعد ذلك الانحراف المقصود بشكل صريح و تراكابل.


### <a name="extending-a-business-process"></a>تمديد العملية التجارية

وحتى الآن ، قام هذا المقال بتمييز كيفيه إنشاء عمليه جديده باستخدام اطار عمل **ProcessGuide**. في هذا المقطع النهائي ، ستجد بعض الامثله عن كيفيه توسيع هذه العملية التجارية.

### <a name="add-a-step-in-a-flow-using-processguidenavigationagentdefault"></a>أضافه خطوه في تدفق (استخدام ProcessGuideNavigationAgentDefault)

مكان التوسيع:

-   التابع لفئة **ProcessGuideController** للعملية.

كيفيه التوسيع:

-   قم بتوسيع الأسلوب **initializeNavigationRoute()** في فئة وحده التحكم ، ثم قم باستدعاء **addFollowingStep()** في الفئة **ProcessGuideNavigationRoute**.

### <a name="add-a-step-in-a-flow-using-custom-navigation-agent"></a>أضافه خطوه في تدفق (استخدام وكيل التنقل المخصص)

مكان التوسيع:

-   تابع لـ **ProdProcessGuideNavigationAgentFactory/ProdProcessGuideNavigationAgent**.

كيفيه التوسيع:

-   إنشاء فئة تابعه جديده **ProcessGuideNavigationAgent** التي تقوم بإرجاع اسم الخطوة المطلوب.

-   إنشاء فئة جديده **ProcessGuideNavigationAgentFactory** مشتقه من التي تقوم الشرطية بإرجاع عامل التنقل الذي تم إنشاؤه أعلاه.

-   تمديد الأسلوب **navigationAgentFactory()** في فئة وحده التحكم لإرجاع عامل التنقل الذي تم إنشاؤه أعلاه.

### <a name="add-a-new-control-in-the-ui-of-an-existing-step"></a>أضافه عنصر تحكم جديد في واجهه المستخدم الخاصة بخطوه موجودة 

مكان التوسيع:

-   تابع لـ **ProdProcessGuidePageBuilder** للخطوة.

كيفيه التوسيع:

-   قم بتوسيع الأسلوب **addDataControls()** وقم باضافه عنصر التحكم الإضافي.

### <a name="complete-overhaul-of-the-user-interface-in-an-existing-step"></a>إصلاح كامل لواجهه المستخدم في خطوه موجودة

مكان التوسيع:

-   تابع لـ **ProdProcessGuideStep**.

كيفيه التوسيع:

-   قم بإنشاء فئة تابعه جديده لفئة **ProdProcessGuidePageBuilder**، ثم قم بتنفيذ واجهه المستخدم المطلوبة.

-   توسيع الأسلوب **pageBuildeName()** في فئة الخطوة لإرجاع **ProcessGuidePageBuilderNameAttribute** للفئة التي تم إنشاؤها أعلاه.

### <a name="alter-logic-when-a-step-is-considered-complete"></a>تغيير المنطق عند اعتبار أحدي الخطوات مكتملة

مكان التوسيع:

-   تابع لـ **ProdProcessGuideStep**.

كيفيه التوسيع:

-   توسيع الأسلوب **isComplete()** لبناء المنطق الإضافي.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]