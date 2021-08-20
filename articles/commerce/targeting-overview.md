---
title: استهداف الأجهزة والسوق وتحديد الموقع الجغرافي
description: يصف هذا الموضوع كيفية إنشاء الجماهير والأهداف وتحريرها وإدارتها في منشئ مواقع Microsoft Dynamics 365 Commerce باستخدام معلومات الجهاز والسوق والموقع الجغرافي.
author: sushma-rao
ms.date: 07/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2021-07-31
ms.dyn365.ops.version: AX 10.0.21
ms.openlocfilehash: 3ecc04c97b42b17f257aa40f665136c70de398748b9bda0da860c7000c062807
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730841"
---
# <a name="device-market-and-geolocation-targeting"></a>استهداف الأجهزة والسوق وتحديد الموقع الجغرافي

[!include [banner](includes/banner.md)]

يصف هذا الموضوع كيفية إنشاء الجماهير والأهداف وتحريرها وإدارتها في منشئ مواقع Microsoft Dynamics 365 Commerce باستخدام معلومات الجهاز والسوق والموقع الجغرافي.

يتيح لك Dynamics 365 Commerce تخصيص أشكال مختلفة من محتوى صفحتك (المعروف باسم *الأهداف*) لمجموعات معينة من العملاء (تعرف باسم *الجماهير*) للمساعدة في زيادة تفاعل المستخدمين ورضاهم. يمكنك إنشاء جمهور أو هدف أولا. ومع ذلك، تتطلب تجربة استهداف ناجحة كلا هذين العنصرين.

يمكنك إنشاء وإدارة الجماهير في منشئ موقع Commerce، استنادا إلى بيانات العملاء مثل الموقع ومعلومات الجهاز وحالة تسجيل الدخول والمعلومات الأخرى المشتقة ديناميكيا من طلبات ويب العملاء. يمكنك أيضا إنشاء وإدارة الأهداف على وحدات التجارة الإلكترونية وشظايا في منشئ موقع التجارة.

**تنويه:** أنت مسؤول عن استخدام هذه الميزة وفقا لجميع القوانين واللوائح المعمول بها، بما في ذلك تلك المتعلقة بالاستهداف والتنميط. 

## <a name="audiences"></a>شرائح الجمهور

الجمهور هو مجموعة من المستخدمين، ويتم تحديد العضوية في المجموعة من خلال مجموعة من القواعد الديناميكية. هذه القواعد هي اختبارات منطق بسيطة يتم تشغيلها مقابل المعلومات المتوفرة في طلبات العملاء أو الأجزاء الأخرى المتوفرة. يمكنك دمج قواعد متعددة باستخدام عوامل التشغيل AND/OR.

التجارة تدعم أصلا القطع الأساسية مثل معلومات الجهاز وحالة تسجيل الدخول والمرجع ومعلمات سلسلة الاستعلام. كما يدعم القطاعات القابلة للتوسعة من خلال الاتصالات بموفري الجهات الخارجية.

### <a name="basic-segments"></a>الأجزاء الأساسية

بشكل افتراضي، تتوفر الشرائح التالية ويمكن تضمينها في تعريفات الجمهور:

- **حالة تسجيل الدخول** – اختبار ما إذا كان المستخدم مصادقا أم لا.
- **منصة الجهاز** – اختبار لأنواع الأجهزة التالية:

    - المحمول‬
    - ‏‏سطح المكتب
    - كمبيوتر لوحي
    - أخرى

- **نظام تشغيل الجهاز** – اختبار لأنظمة التشغيل التالية:

    - Windows
    - Linux
    - iOS
    - Android، غير ذلك

- **معلمات سلسلة الاستعلام** – اختبار وجود زوج قيمة مفتاح في معلمة سلسلة استعلام من عنوان URL طلب. على سبيل المثال، بالنسبة لعنوان URL `www.fabrikam.com/en-us/request?promo=true` ، يمكن كتابة قاعدة لاختبار أن المعلمة **الترويجية** لها القيمة **true**.
- **ملف تعريف الارتباط** – اختبار لقيمة ملف تعريف الارتباط التي تم تعيينها للمجال في عنوان URL الطلب. على سبيل المثال، قد يتضمن طلب Fabrikam.com ملف تعريف ارتباط يحتوي على اسم **CustomLayout** والقيمة **1**. يتحقق اختبار ملف تعريف الارتباط من وجود ملف تعريف ارتباط ولكنه لا ينشئ ملف تعريف ارتباط بشكل صريح. في المثال السابق، يجب أن يكون JavaScript قد سبق تعيين ملف تعريف الارتباط **CustomLayout** من وحدة نمطية أخرى أو بعض العمليات التجارية الأخرى.

    > [!NOTE]
    > تأكد من أن استخدامك لملفات تعريف الارتباط يتوافق مع القوانين المعمول بها.

- **المحيل** – إذا اتبع مستخدم رابطا لطلب الصفحة، فإن المحيل هو عنوان URL للصفحة التي استضافت الارتباط.

### <a name="extensible-segments"></a>شرائح قابلة للتوسعة

تتيح لك التجارة توسيع قائمة الشرائح المتوفرة من خلال الاتصال بموفري تجزئة الجهات الخارجية. سيقوم موفر تجزئة بوصف أنواع المقاطع المتوفرة. لمزيد من المعلومات حول كيفية الاتصال بموفر تحديد الموقع الجغرافي أو التقسيم، راجع [تكوين الموصلات وتمكينها](e-commerce-extensibility/connectors.md).

> [!NOTE]
> - إذا تم تمكين موفر خارجي، فقد يتصل بخدمة لا يمكن التنبؤ بها الأداء. للمساعدة في ضمان تجربة مستخدم أفضل، إذا طلب مستخدم صفحة تتضمن استهدافا، وكانت تلك الصفحة تشير إلى جمهور يتحقق من موفر شرائح تابع لجهة خارجية، يتم عرض الإصدار الافتراضي للصفحة.
> - يجب على المستخدم الموافقة على السماح بملفات تعريف الارتباط. متصفح المستخدم ثم يطلب جميع شرائح من مقدمي ذات الصلة، ويتم وضع النتائج في ملف تعريف الارتباط التي يتم إرجاعها إلى المستخدم. سوف تستخدم الطلبات اللاحقة إلى الصفحة هذه المعلومات لخدمة المحتوى المستهدف للمستخدم. لمزيد من المعلومات حول التوافق مع ملفات تعريف الارتباط، راجع [التوافق مع ملفات تعريف الارتباط](cookie-compliance.md).

**تنويه:** إذا قمت بتمكين هذه الميزة، سيتم مشاركة بياناتك مع أنظمة الجهات الخارجية التي تحددها. يمكنك التحكم في البيانات، إن وجدت، التي تقدمها إلى جهة خارجية. أنت تدرك أن معايير التعامل مع البيانات والامتثال الخاصة بالطرف الثالث قد تختلف عن معايير Microsoft Dynamics 365 Commerce. تعد خصوصيتك مهمة لشركه Microsoft. لمعرفه المزيد، اقرأ [إشعار الخصوصية وملفات تعريف الارتباط](https://privacy.microsoft.com/privacystatement).

### <a name="create-an-audience-in-site-builder"></a>إنشاء جمهور في منشئ المواقع

لإنشاء جمهور في منشئ موقع Commerce، اتبع الخطوات التالية.

1. في جزء التنقل الأيسر، حدد **الجماهير**.
1. حدد **جديد**.
1. أدخل اسمًا للجماهير. يمكنك أيضا إضافة علامات ووصف اختياري.
1. حدد **إنشاء** ثم **إضافة كتلة قاعدة جديدة**. كتلة قاعدة هي مجموعة من القواعد التي يتم ربطها بشروط AND. يمكنك أيضا إنشاء كتل قاعدة متعددة لها شروط OR بينها.
1. حدد مصدر بيانات للشرائح، ثم حدد اسم الشريحة، والمشغل، والقيم. يمكنك إنشاء المزيد من القواعد وحذفها في كتلة قاعدة، أو يمكنك إنشاء كتل قواعد بأكملها وحذفها. يمكنك أيضا نقل كتل القواعد لأعلى أو لأسفل كما تحتاج.

    > [!NOTE]
    > يمكن أن يكون لديك ما يصل إلى 100 قيمة في قائمة، ويمكن أن يحتوي كل عنصر قائمة على ما يصل إلى 50 حرفا.

1. عندما تكون راضيا عن تكوين الجمهور، حدد **إنهاء التحرير**. يمكنك بعد ذلك تحديد **نشر** لإتاحة الجمهور للاستخدام في هدف مباشر. بدلا من ذلك، يمكنك نشر الجمهور مع الهدف. 

لتحرير جمهور، حدد الارتباط التشعبي له في علامة التبويب **الجماهير**، ثم حدد **تحرير** في محرر الجمهور الذي يظهر. لعرض قائمة الأهداف والصفحات التي تشير إلى جمهور، حدد الجمهور في طريقة عرض قائمة الجمهور، ثم حدد **عرض التعيينات**. لحذف جمهور في طريقة عرض قائمة الجمهور أو محرر الجمهور، قم بإلغاء نشره إذا كان قد تم نشره بالفعل، ثم حدد **حذف** على شريط الأوامر.

> [!NOTE]
> الجماهير هي مفهوم على مستوى الموقع في منشئ مواقع Commerce. يمكنك مشاركة نفس الجمهور عبر أهداف متعددة.

## <a name="targets"></a>الأهداف

الهدف هو تجربة المستخدم التي يتم عرضها لأعضاء جمهور واحد أو أكثر من الجماهير المحددة. ويمكن أن تتضمن أشكالا مختلفة من وحدة نمطية واحدة أو أكثر على صفحة أو في جزء. 

يمكنك تحديد جدول زمني لأهدافك لتحديد المدة التي يجب أن تظل فيها نشطة. لاحظ أن هذا الإجراء منفصل عن إجراء جدولة مجموعة نشر تحدد متى سيتم نشر مجموعة من المحتوى. يمكنك أيضا معاينة أهدافك لمعرفة شكلها لأعضاء الجماهير المحددة. بالإضافة إلى ذلك، يمكنك تحديد أولويات أهدافك لتحديد الهدف الذي يجب إظهاره في حالة حدوث تعارض.

### <a name="create-a-target"></a>إنشاء هدف

لإنشاء هدف للصفحة الديناميكية في منشئ مواقع Commerce، اتبع الخطوات التالية.

1. في جزء التنقل الأيسر، حدد **الصفحات**. ثم حدد الارتباط التشعبي للصفحة التي تحتوي على الوحدات النمطية التي تريد استهدافها.
1. حدد **تحرير** لإخراج الصفحة المطلوب تحريرها.
1. في القائمة **الهدف**، حدد **هدف جديد** لإنشاء قذيفة هدف جديد. يمكنك إنشاء أهداف متعددة على صفحة كما تريد.
1. أدخل اسمًا ووصفًا للهدف، ثم حدد **التالي**
1. حدد **إضافة** لتضمين الجماهير التي ستشاهد المحتوى المستهدف، أو لاستبعاد الجماهير. بعد ذلك حدد **التالي**.

    > [!NOTE]
    > تعيين الجمهور هو خطوة اختيارية أثناء إنشاء الهدف. ومع ذلك، قبل نشر الهدف، يجب تضمين جمهور واحد على الأقل للتأكد من أن المجموعات المستهدفة من المستخدمين سوف ترى المحتوى المستهدف.

1. حدد الإطار الزمني لعرض الهدف بتحديد المنطقة الزمنية وتواريخ وأوقات البدء والانتهاء. يمكنك تعيين الهدف بحيث يتم عرضه في جميع الأوقات أثناء النافذة، أو يمكنك تحديد أيام وأوقات محددة. عند الانتهاء، حدد **التالي**.

    > [!NOTE]
    > الأوقات والمنطقة الزمنية التي تحددها عمومية. إذا كنت تريد استهداف مواقع مختلفة في أوقات مختلفة أو في مناطق زمنية مختلفة، يجب إنشاء أهداف مختلفة وتحديد الجدول الزمني المطلوب لكل موقع.

1. راجع التفاصيل، وعندما يبدو كل شيء صحيحا، حدد **إنشاء تجربة هدف** ثم **انتقل إلى الهدف**. يتم إنشاء قذيفة الهدف. يمكنك الآن إضافة وحدات إليها.
1. حدد الوحدة النمطية التي تريد استهدافها، وحدد علامة القطع (**...**) ، ثم حدد **إضافة إلى الهدف الحالي**. عندما تستهدف وحدة نمطية أصل، يصبح كل أطفالها جزءا من هذا الهدف. يتم تمييز الوحدات المستهدفة باللون الأخضر.
1. قم بإجراء تحديثات المحتوى الضرورية للوحدة النمطية المستهدفة، وأضف المزيد من الوحدات النمطية إلى الهدف كما تريد. بعد ذلك حدد **حفظ** لحفظ كل تغييراتك.
1. قبل نشر الهدف، تأكد من تحديد **معاينة** على شريط الأوامر لمراجعته. يمكنك بعد ذلك تحديد إحدى الخيارات التالية:

    - **الإصدار الأولي الأساسي** – حدد هذا الخيار من أجل الإصدار الأولي للتباين المحدد فقط (الصفحة الافتراضية أو الهدف)، دون أي جماهير مقترنة.
    - **إصدار أولي متقدم** – حدد هذا الخيار إذا كان لديك أهداف متعددة على صفحة وتريد الإصدار الأولي لها كمستخدم ينتمي إلى مجموعة مختارة من الجماهير، أو في تاريخ/وقت محدد. حدد **التالي** لتحديده من قائمة الجماهير ذات الصلة. يمكنك أيضا إزالة عامل التصفية لتحديده بين جميع الجماهير.

1. عندما تكون راضيا عن التكوين الهدف، يجب نشر الصفحة لجعل الهدف مباشرًا. حدد **نشر** لجعل الهدف يتم بثه مباشرة. بدلا من ذلك، يمكنك استخدام مجموعة نشر لجدولة وقت بث الصفحة مباشرة. للحصول على معلومات حول نشر المجموعات، راجع [العمل مع مجموعات النشر](publish-groups.md).

يمكنك أيضا استهداف الأجزاء. الإجراء مشابه. ومع ذلك، في الخطوة 1، حدد **أجزاء** بدلا من **صفحات** في جزء التنقل الأيسر.

> [!NOTE]
> لتجنب أي تأثير سلبي على المقاييس، يمكنك الحصول على تجربة أو أهداف على صفحة أو في جزء. لا يمكنك الحصول على تجربة وأهداف على حد سواء.

### <a name="manage-targets"></a>إدارة الأهداف

لتحرير الأهداف أو تكرارها أو حذفها، انتقل إلى الصفحة الافتراضية أو الجزء، واتبع الخطوات التالية.

1. في القائمة المنسدلة، حدد **الهدف** ، ثم حدد **إدارة الأهداف**.
1. حدد هدفا لتحريره أو تكراره أو حذفه.
1. إذا كان لديك أهداف متعددة في نفس الوحدة النمطية، أو إذا كان لدى أهداف متعددة جداول متعارضة، فحدد **تحديد أولويات الأهداف لتحديد الترتيب الذي يجب إظهارها فيه**. إذا أضفت أكثر من هدف واحد على صفحة أو في جزء، يظهر الزر **تحديد الأولويات للأهداف** أيضا في شريط الإعلام لتذكيرك بتحديد أولويات الأهداف. إذا لم يتم تحديد أية أولوية، يتم تحديد الهدف الأحدث بشكل افتراضي.

### <a name="localize-targets"></a>توطين الأهداف

يتم تضمين الأهداف على الصفحات وفي الأجزاء تلقائيا عند تصدير ملفات XLIFF و استيرادها لأغراض التعريب. ومع ذلك، إذا لم تكن هناك أي لغات مطلوبة، يمكنك حذف الأهداف الخاصة بها بعد استيراد ملفات XLIFF المترجمة.

> [!NOTE]
> تتم إدارة الأهداف لكل قناة و موضع. لا يتم نقل التغييرات التي تجريها على الأهداف في قناة أو موضع تلقائيا إلى قنوات أو مناطق أخرى.

[!INCLUDE[footer-include](../includes/footer-banner.md)]