---
title: تضمين تطبيقات اللوحة من Power Apps
description: تصف هذه المقالة كيفية تضمين تطبيقات اللوحة من Microsoft Power Apps في العميل لزيادة الأداء الوظيفي للمنتج.
author: jasongre
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: d7dc45e56c5fa616c288ebb4b919f039b7358794
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/06/2022
ms.locfileid: "9123643"
---
# <a name="embed-canvas-apps-from-power-apps"></a>تضمين تطبيقات اللوحة من Power Apps

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

إن Microsoft Power Apps عبارة عن خدمة تسمح للمطورين والمستخدمين غير التقنيين ببناء تطبيقات أعمال مخصصة للأجهزة المحمولة وأجهزة الكمبيوتر اللوحية والويب من دون كتابة تعليمات برمجية. تدعم تطبيقات التمويل والعمليات التكامل مع Power Apps. يمكن تضمين تطبيقات اللوحة، التي تقوم أنت أو مؤسستك أو النظام البيئي الأوسع بتطويرها في تطبيقات التمويل والعمليات لزيادة الأداء الوظيفي للمنتج. على سبيل المثال، قد تقوم بإنشاء تطبيق لوحة من Power Apps لتكملة أحد تطبيقات التمويل والعمليات بواسطة معلومات تم استردادها من نظام آخر.

لمزيد من المعلومات حول تضمين تطبيقات اللوحة، شاهد مقطع الفيديو القصير [كيفية تضمين تطبيقات اللوحة](https://www.youtube.com/watch?v=x3qyA1bH-NY).

## <a name="adding-an-embedded-canvas-app-from-power-apps-to-a-page"></a>إضافة تطبيق لوحة مضمن من Power Apps إلى صفحة

قبل تضمين تطبيق لوحة من Power Apps في العميل، تحتاج إلى البحث عن تطبيق يحتوي على المرئيات أو الوظيفة المطلوبة أو إنشائه. لا تتضمن هذه المقالة وصفًا مفصلاً لعملية إنشاء التطبيقات. إذا كان Power Apps جديدًا بالنسبة لك، فراجع [وثائق Power Apps](/powerapps/).

هناك ثلاث طرق لتضمين تطبيق لوحة في تطبيق التمويل والعمليات. يمكنك استخدام النهج الذي يناسب السيناريو الخاص بك. 

- قم بتضمين تطبيق اللوحة في الزر **Power Apps** في جزء الإجراءات القياسي للصفحة. تظهر التطبيقات التي تضيفها بهذه الطريقة كعناصر على زر قائمة **Power Apps**، وتفتح التطبيقات في الأجزاء الجانبية. 
- قم بتضمين تطبيق اللوحة مباشرةً على صفحة موجودة كصفحة علامة تبويب جديدة (علامة التبويب المحورية أو علامة التبويب السريعة أو الشفرة أو قسم مساحة العمل).
- أنشئ تجربة صفحة كاملة جديدة اللوحة من لوحة المعلومات.

عند تكوين تطبيق اللوحة المضمن، يمكنك تحديد حقل واحد تريد إرساله كسياق إلى التطبيق. تسمح هذه الخطوة للتطبيق بأن يكون متجاوبًا استنادًا إلى البيانات التي تعرضها حاليًا.

> [!NOTE]
> لا يمكنك استخدام هذه الآلية لتضمين التطبيقات المستندة إلى النماذج.

### <a name="embedding-a-canvas-app-on-an-existing-page"></a>تضمين تطبيق لوحة على صفحة موجودة

يوضح الإجراء التالي كيفية تضمين تطبيق لوحة على صفحة موجودة من Power Apps.

1. انتقل إلى الصفحة التي تريد تضمين تطبيق اللوحة فيها. ستحتوي هذه الصفحة على أي بيانات يجب تمريرها إلى التطبيق كمدخلات.
2. افتح الجزء **إضافة تطبيق من Power Apps**:

    - إذا كان التطبيق سيتم تضمينه مباشرة في الصفحة، فحدد **خيارات** \> **تخصيص هذه الصفحة** \> **المزيد**، ثم اتبع إحدى الخطوات التالية:

        - إذا تم تشغيل ميزة **تطبيقات الصفحة الكاملة**، فحدد **إضافة صفحة**، ثم حدد المنطقة التي تريد إضافة التطبيق إليها. لتضمين التطبيق في زر قائمة **Power Apps**، حدد جزء الإجراءات. لتضمين التطبيق مباشرة على الصفحة، حدد علامة التبويب المناسبة أو علامة التبويب السريعة أو الشفرة أو القسم المناسب (إذا كنت في مساحة عمل). ثم، في جزء **إضافة تطبيق**، حدد **Power Apps**.
        - إذا تم تشغيل ميزة **تطبيقات الصفحة الكاملة**، فحدد **إضافة تطبيق من Power Apps**، ثم حدد المنطقة التي تريد إضافة التطبيق إليها. لتضمين التطبيق في زر قائمة **Power Apps**، حدد جزء الإجراءات. لتضمين التطبيق مباشرة على الصفحة، حدد علامة التبويب المناسبة أو علامة التبويب السريعة أو الشفرة أو القسم المناسب (إذا كنت في مساحة عمل).

    - إذا كان سيتم الوصول إلى التطبيق باستخدام زر قائمة **Power Apps**، يمكنك تحديد زر قائمة **Power Apps**  في جزء الإجراءات القياسية، ثم تحديد **إضافة تطبيق**.

3. قم بتكوين التطبيق المضمن. لمزيد من المعلومات، راجع قسم [تكوين تطبيق لوحة](#configuring-a-canvas-app) لاحقًا في هذه المقالة.
4. بعد التأكد من صحة التكوين، حدد **إدراج**.

    - إذا تم إيقاف تشغيل ميزة **طرق العرض المحفوظة**، تتم مطالبتك بتحديث المستعرض لرؤية التطبيق المضمن.
    - إذا تم تشغيل ميزة **طرق العرض المحفوظة**، يجب حفظ طريقة العرض حتى يتم استمرار التغيير.

### <a name="embedding-a-canvas-app-as-a-full-page-experience-from-the-dashboard"></a>تضمين تطبيق لوحة كتجربة صفحة كاملة من لوحة المعلومات

قد ترغب في تضمين تطبيق لوحة من لوحة المعلومات إذا لم يكن التطبيق مرتبطًا بصفحة موجودة، أو إذا كنت تريد فقط إظهار التطبيق كتجربة صفحة كاملة داخل تطبيق التمويل والعمليات.

> [!NOTE]
> لتوفير هذه الإمكانية، يجب تشغيل ميزة **تطبيقات الصفحة الكاملة** في إدارة الميزات. 

1. افتح لوحة المعلومات.
2. حدد مع الاستمرار (أو انقر بزر الماوس الأيمن) على الصفحة، وحدد **تشخيص**، ثم حدد **إضافة صفحة**.
3. في جزء **إضافة صفحة**، حدد **Power Apps**.
4. قم بتكوين التطبيق المضمن. لمزيد من المعلومات، راجع قسم [تكوين تطبيق لوحة](#configuring-a-canvas-app) لاحقًا في هذه المقالة.
5. حدد **حفظ** لإضافة التطبيق إلى لوحة القيادة كتجانب جديد.
6. حدد التجانب الجديد في لوحة المعلومات، وتأكد من ظهور تطبيق اللوحة بالشكل المتوقع.

### <a name="configuring-a-canvas-app"></a>تكوين تطبيق لوحة

عند تضمين تطبيق لوحة، يجب تعيين المعلمات التالية:

- **الاسم** – أدخل النص الذي يجب أن يظهر للزر أو علامة التبويب التي ستحتوي على التطبيق المضمن. في كثير من الأحيان، قد ترغب في تكرار اسم التطبيق في هذا الحقل.
- **معرف التطبيق** – تحديد المعرف الفريد العمومي (GUID) لتطبيق اللوحة الذي تريد تضمينه. لاسترداد هذه القيمة، ابحث عن التطبيق في [make.powerapps.com](https://make.powerapps.com)، ثم ابحث عن حقل **معرف التطبيق** تحت **التفاصيل‏‎**.
- **سياق الإدخال للتطبيق** – يمكنك اختياريًا تحديد الحقل الذي يحتوي على البيانات التي تريد تمريرها إلى التطبيق كإدخال. للحصول على معلومات عن كيفية وصول التطبيق إلى البيانات المرسلة من تطبيقات التمويل والعمليات، راجع القسم [إنشاء تطبيق يستفيد من البيانات من تطبيقات التمويل والعمليات](#building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps) لاحقًا في هذه المقالة.

    بدءًا من الإصدار 10.0.19، يتم أيضًا تمرير الكيان القانوني الحالي كسياق لتطبيق اللوحة عبر معلمة عنوان URL لـ **cmp**. لن يؤثر هذا السلوك على تطبيق اللوحة الهدف حتى يستخدم هذا التطبيق تلك المعلومات.

- **حجم التطبيق** – تحديد نوع التطبيق الذي تقوم بتضمينه. حدد **رفيع** للتطبيقات التي يتم إنشاؤها للأجهزة المحمولة أو **عريض** للتطبيقات التي يتم إنشاؤها لأجهزة الكمبيوتر اللوحية. تضمن هذه المعلمة تخصيص مساحة كافية للتطبيق المضمن.
- **الكيانات القانونية** – يمكنك تحديد الكيانات القانونية التي يجب أن يكون التطبيق متاحا لها. بشكل افتراضي، يتوفر التطبيق لجميع الكيانات القانونية. يتوفر هذا الخيار فقط عند التضمين مباشرة على صفحة موجودة ويتم إيقاف تشغيل ميزة **[طرق العرض المحفوظة](saved-views.md)**.

## <a name="sharing-an-embedded-app"></a>مشاركة التطبيق المضمن

بعد تضمين تطبيق اللوحة على صفحة والتأكد من عمله بشكل صحيح مع أي سياق بيانات يتم تمريره من هذه الصفحة، قد تحتاج إلى مشاركة التطبيق مع مستخدمين آخرين في النظام. لمشاركة تطبيق لوحة مضمن، اتبع الخطوات التالية.

1. [شارك تطبيق اللوحة في Power Apps](/powerapps/maker/canvas-apps/share-app) مع المستخدمين المناسبين، حتى يتمكنوا من الوصول إلى التطبيق مباشرة Power Apps.
2. شارك التخصيصات المقترنة بالتطبيق المضمن مع المستخدمين المطلوبين. يمكنك استخدام أي أسلوب من الأساليب التالية:

    - **نشر طريقة العرض (مستحسن):** إذا تم تشغيل ميزة **[طرق العرض المحفوظة](saved-views.md)**، فإن الطريقة الموصى بها والمفضلة هي إنشاء طريقة عرض تتضمن تطبيق اللوحة المضمنة، ثم نشر طريقة العرض هذه للمستخدمين المطلوبين. يضمن هذا الأسلوب أن جميع المستخدمين الذين لديهم أدوار أمان مستهدفة بواسطة طريقة العرض المنشورة سيرون تطبيق اللوحة على الصفحة.

        يمكنك أيضًا نشر تطبيق لوحة تم تضمينه كتجربة صفحة كاملة من لوحة المعلومات. في لوحة المعلومات، حدد باستمرار (أو انقر بزر الماوس الأيمن) فوق التجانب المرتبط بالتطبيق، وحدد **تخصيص**، ثم حدد **نشر صفحة**. يتم عرض تجربة تشبه تجربة *طرق عرض النشر*، ويمكنك تحديد أدوار الأمان للنشر إليها. في التحديث 10.0.21 أو أحدث، إذا تم تشغيل ميزة **تحسين دعم الكيان القانوني لطرق العرض المحفوظة**، يمكنك أيضا نشر التطبيق إلى الكيانات القانونية المطلوبة.

    - إذا تم إيقاف تشغيل ميزة **طرق العرض المحفوظة**، يمكن لمسؤول النظام منح إضفاء طابع شخصي يتضمن تطبيق اللوحة إلى المجموعة المناسبة من المستخدمين عبر صفحة **التخصيص**. أو، يمكنك تصدير عمليات تخصيص صفحتك، ثم إرسالها إلى مستخدم واحد أو أكثر. بإمكان كل واحد من هؤلاء المستخدمين استيراد التخصيص. يحتوي شريط أدوات التخصيص على أزرار تسمح لك بتصدير التخصيصات واستيرادها.

> [!NOTE]
> إذا تمت مشاركة تطبيق اللوحة مع مستخدمين خارجيين، فلن يتمكن هؤلاء المستخدمون من استخدام التطبيق المضمن داخل تطبيقات التمويل والعمليات. ومع ذلك، يمكنهم الوصول إلى التطبيق داخل Power Apps مباشرةً. يتضمن المستخدمون الخارجيون الضيوف والمستخدمين الذين لا ينتمون إلى دليل Microsoft 365 Azure حيث يتم نشر تطبيق التمويل والعملية.

راجع [تخصيص تجربة المستخدم](personalize-user-experience.md) لمزيد من التفاصيل حول إمكانات التخصيص في المنتج وكيفية استخدامها.

## <a name="building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps"></a>بناء تطبيق لوحة يستخدم البيانات التي تم إرسالها من تطبيقات التمويل والعمليات

عندما تقوم ببناء تطبيق لوحة سيتم تضمينه في تطبيق التمويل والعمليات، هناك جزء مهم من العملية يقضي باستخدام بيانات الإدخال من تطبيق التمويل والعمليات هذا. من تجربة تطوير Power Apps ، يمكن الوصول إلى بيانات الإدخال التي يتم تمريرها من تطبيق التمويل والعمليات باستخدام متغير **Param("EntityId")** بالإضافة إلى ذلك، بدءًا من الإصدار 10.0.19، سيتم أيضًا تمرير الكيان القانوني الحالي إلى تطبيق اللوحة عبر متغير **Param("cmp")**. 

على سبيل المثال، في وظيفة OnStart الخاصة بالتطبيق، يمكنك تعيين بيانات الإدخال من تطبيقات التمويل والعمليات إلى متغير مثل هذا:

``` Power Apps
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));

If(!IsBlank(Param("cmp")), Set(FinOpsLegalEntity, Param("cmp")), Set(FinOpsLegalEntity, ""));
```

## <a name="viewing-a-canvas-app"></a>عرض تطبيق لوحة

لعرض تطبيق لوحة مضمن في صفحة في تطبيق التمويل والعمليات، انتقل إلى صفحة لديها تطبيق مضمن. تذكر أنه يمكن الوصول إلى التطبيقات باستخدام الزر **Power Apps** الموجود في جزء الإجراءات القياسية. أو، يمكنها أن تظهر تطبيق مباشرةً على صفحة كعلامة تبويب جديدة أو كعلامة تبويب سريعة أو ريشة، أو كقسم جديد في مساحة عمل. عند قيام المستخدمين أولاً بمحاولة تحميل تطبيق على الصفحة، ستتم مطالبتهم بتسجيل الدخول. تضمن هذه الخطوة أن تكون لدى المستخدمين الأذونات المناسبة لاستخدام التطبيق.

## <a name="editing-an-embedded-app"></a>تحرير تطبيق مضمن

بعد تضمين تطبيق في صفحة، قد تحتاج إلى إجراء بعض التغييرات لتكوين التطبيق. على سبيل المثال، ربما تحتاج إلى تعديل التسمية المقترنة بالتطبيق المضمن أو أنه قد تم إنشاء إصدار جديد من التطبيق وتحتاج إلى تحديث "معرف التطبيق" للإشارة إلى الأحدث.

اتبع هذه الخطوات لتحرير تكوين تطبيق مضمن:

1. انتقل إلى جزء **تحرير التطبيق**.

    - في حالة الوصول إلى التطبيق المضمن من خلال زر قائمة Power Apps، حدد مع الاستمرار (انقر بزر الماوس الأيمن) فوق زر قائمة Power Apps، ثم حدد **تخصيص**. حدد التطبيق الذي تريد تكوينه من القائمة المنسدلة **تحديد تطبيق**.
    - عند ظهور التطبيق المضمن مباشرةً في الصفحة، حدد **الخيارات**، ثم حدد **تخصيص هذه الصفحة**. باستخدام أداة **التحديد**، انقر فوق التطبيق المضمن.
    - إذا تمت إضافة التطبيق المضمن من لوحة المعلومات، فافتح لوحة المعلومات، وحدد (أو انقر بزر الماوس الأيمن) فوق التجانب المقترن بتطبيق اللوحة، وحدد **تخصيص**، ثم حدد **تحرير الصفحة**.

2. قم بإجراء التعديلات المطلوبة على تكوين التطبيق، ثم انقر فوق **حفظ**.

## <a name="removing-an-app"></a>إزالة تطبيق

بعد تضمين تطبيق في صفحة، هناك بضعة طرق لإزالته إذا لزم الأمر:

- انتقل إلى جزء **تحرير تطبيق** باستخدام الإرشادات من قسم [تحرير تطبيق مضمن](#editing-an-embedded-app) السابق في هذه المقالة. تأكد من عرض الجزء معلومات للتطبيق المضمن الذي تريد إزالته، ثم انقر فوق الزر **حذف**.
- إذا تمت إضافة التطبيق المضمن من لوحة المعلومات، فافتح لوحة المعلومات، وحدد (أو انقر بزر الماوس الأيمن) فوق التجانب المقترن بتطبيق اللوحة، وحدد **تخصيص**، ثم حدد **إزالة الصفحة**. 
- نظرًا لحفظ التطبيق المضمن كبيانات تخصيص، سيؤدي أيضًا مسح تخصيص الصفحة إلى إزالة أي تطبيقات مضمنة في تلك الصفحة. لاحظ أن مسح تخصيص الصفحة دائم ولا يمكن التراجع عنه. لإزالة تخصيصاتك في صفحة، حدد **الخيارات**، ثم **تخصيص هذه الصفحة**، ثم زر **مسح**. بعد تحديث المستعرض الخاص بك، ستتم إزالة جميع التخصيصات السابقة لهذه الصفحة. راجع [تخصيص تجربة المستخدم](personalize-user-experience.md) لمزيد من المعلومات حول كيفية تحسين الصفحات باستخدام التخصيص.

## <a name="appendix"></a>الملحق

### <a name="developer-modeling-a-canvas-app-on-a-form"></a>[المطور] نمذجة تطبيق اللوحة في نموذج

بينما تركز هذه المقالة على تضمين تطبيقات اللوحة من خلال التخصيص، يتوفر للمطورين أيضًا خيار إضافة تطبيق اللوحة إلى نموذج باستخدام تجربة تطوير Visual Studio . للقيام بذلك، ما عليك سوى إضافة PowerApps HostControl إلى النموذج. توفر خصائص البيانات الوصفية المتوفرة في عنصر التحكم نفس الإمكانات مثل تجربة التخصيص.

### <a name="developer-specifying-where-an-app-can-be-embedded"></a>[المطور] تحديد المكان حيث يمكن تضمين التطبيق

يمكن للمستخدمين تضمين تطبيق في أي صفحة افتراضيًا، إما ضمن زر قائمة Power Apps أو مباشرةً على الصفحة كعلامة تبويب أو علامة تبويب سريعة أو ريشة أو كقسم جديد في مساحة عمل. ولكن إذا لزم الأمر، بإمكان المطورين أيضًا تكوين هذه الميزة للسماح فقط بتضمين تطبيقات على صفحات معينة عن طريق تطبيق الأساليب التالية:

- **isPowerAppPersonalizationEnabled** – إذا أرجع هذا الأسلوب خطأ لصفحة معينة، فلن يظهر زر قائمة Power Apps، ولن يتمكن المستخدمون من تضمين تطبيقات في أي مكان في هذه الصفحة، بما في ذلك كعلامة تبويب.
- **isPowerAppTabPersonalizationEnabled** – إذا أرجع هذا الأسلوب خطأً لصفحة معينة، فلن يتمكن المستخدمون من تضمين تطبيقات مباشرةً في الصفحة كعلامة تبويب أو علامة تبويب سريعة أو قسم بانوراما. سيبقى باستطاعة المستخدمين تضمين تطبيقات من خلال زر قائمة Power Apps في حالة السماح بالتضمين في الصفحة.

يوضح المثال التالي فئة جديدة باستخدام الطريقتين المطلوبتين لتكوين المكان الذي يمكن تضمين التطبيقات فيه.

```powerapps
[ExtensionOf(classStr(FormRunConfigurationPowerAppsConfiguration))]

public final class ClassTest_Extension
{
    public static boolean isPowerAppPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppPersonalizationEnabled(pageName);
        return result;
    }
    
    public static boolean isPowerAppTabPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppTabPersonalizationEnabled(pageName);
        return result;
    }
}
```

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

