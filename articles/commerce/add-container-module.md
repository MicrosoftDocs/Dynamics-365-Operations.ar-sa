---
title: وحدة الحاوية
description: يتناول هذا المقال وحدات الحاوية ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 58fa222dfef9e559da00fef448c572800651bd63
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272897"
---
# <a name="container-module"></a>وحدة الحاوية

[!include [banner](includes/banner.md)]

يتناول هذا المقال وحدات الحاوية ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.

وحدة الحاوية هي وحدة تستضيف الوحدات الأخرى داخلها. يتمثل الغرض الأساسي من وحدة الحاوية في تعريف تخطيط الوحدات الموجودة فيها، من خلال الخصائص التي تم تعيينها لها. على سبيل المثال، يُمكن أن تظهر هذه الوحدات بجوار بعضها في تخطيط ذو عمودين أو ثلاثة أعمدة أو أربعة أعمدة أو ستة أعمدة. ويُمكن أيضًا أن تكون محدودة بعرض الحاوية أو يُمكنها ملء الشاشة. ويُمكن أيضًا إضافة عنوان لكل وحدة حاوية.

تتوفر ثلاثة أنواع من وحدات الحاوية: الحاوية والحاوية ذات فتحتين والحاوية ذات ثلاث فتحات. ويمكن وضع وحدات من أي نوع داخل هذه الحاويات. 

> [!NOTE] 
> ننصح بوضع الوحدات دائمًا داخل وحدة حاوية، بحيث يمكن أن تكون محدودة بعرض الحاوية.

## <a name="examples-of-container-modules-in-e-commerce"></a>أمثلة على وحدات الحاويات في التجارة الإلكترونية

- يُريد مؤلف الموقع تخطيط ثلاثة أعمدة، بحيث تظهر الثلاث وحدات بجوار بعضها. وبالتالي، يستخدم كاتب الموقع وحدة الحاوية للحاوية بنوع 3 فتحات.
- يُريد مؤلف الموقع تخطيط ستة أعمدة، بحيث تظهر الست وحدات بجوار بعضها. وبالتالي، يستخدم مؤلف الموقع حاوية من النوع الذي يحتوي على ستة أعمدة داخله.
- يرغب مؤلف الموقع في وضع وحدة على صفحة ولكنه لا يرغب في أن تملأ الوحدة الشاشة. وبالتالي، يُضيف مؤلف الموقع الوحدة إلى وحدة الحاوية وتعيين خاصية **عرض** الحاوية إلى **ملائمة الحاوية**.

تعرض الصورة التالية مثالاً عن وحدة الحاوية التي تحتوي على وحدة دوارة في منشئ موقع Commerce. في هذا المثال، تم تعيين خاصية **العرض** للوحدة الدوارة إلى **ملء الشاشة**.

![مثال وحدة حاوية.](./media/ecommerce-container.PNG)

## <a name="container-module-properties"></a>خصائص وحدة الحاوية

| اسم الخاصية     | القيم | الوصف |
|-------------------|--------|-------------|
| العنوان           | نص العنوان وعلامة العنوان (**H1**, **H2**, **H3**, **H4**, **H5**, أو **H6**) | يُمكن توفير عنوان اختياري للحاوية. وبشكل افتراضي، يتم استخدام علامة العنوان **H2** للعنوان. ولكن، يُمكن تغيير العلامة لتتوافق مع متطلبات الوصول. |
| العرض             | **ملائمة الحاوية** أو **ملء الشاشة** | إذا تم تعيين القيمة إلى **ملائمة الحاوية** (القيمة الافتراضية)، فإن الوحدات داخل الحاوية تقتصر على عرض الحاوية. إذا تم تعيين القيمة إلى **ملء الشاشة**، فلن تقتصر الوحدات على عرض الحاوية ولكن يُمكن أن تملئ الشاشة. |
| عدد الأعمدة | **1**, **2**, **3**, **4**, **6**, أو **12** | تُحدد هذه الخاصية عدد الأعمدة الموجودة في الحاوية. يُمكن أن تحتوي الحاوية على 12 عمودًا بحد أقصى. |

## <a name="container-with-2-slots"></a>حاوية بفتحتين

يتم تحسين الحاوية من نوع الفتحتين لتخطيط من عمودين. يحتوي هذا النوع من الحاويات على فتحتين للسماح بعرض الوحدات الموجودة بالداخل بجوار بعضهم.

يُمكن استخدام خصائص إضافية لتحسين التخطيط لمنافذ عرض مختلفة (الأجهزة المحمولة والأجهزة اللوحية وأجهزة الكمبيوتر وغيرها). بالنسبة لكل منفذ عرض، يُمكن تحديد عرض كل عمود. تتوفر إعداد عرض العمود التالية:

- **75%/25%** – تحتوي الوحدة الأولى على عمود عرضه 75بالمائة، والوحدة الثانية تحتوي على عمود عرضه 25 بالمائة. ويتوفر أيضًا الخيار **25%/75%**.
- **50%/50%** – وكلا الوحدتين لديهم عرض عمود متساوي.
- **67%/33%** – تحتوي الوحدة الأولى على عمود عرضه 67 بالمائة، وتحتوي الوحدة الثانية على عمود عرضه 33 بالمائة. ويتوفر أيضًا الخيار **33%/67%**.
- **100%** – وتحتوي الوحدتان على عرض عمود كامل. ولذلك، يتم تكديس الوحدات عموديًا في عمود واحد. وبالرغم من أن تخطيط العمود الواحد يتعارض مع هدف الحاوية من نوع الفتحتين، فقد يكون من المفضل لبعض منافذ طرق العرض (على سبيل المثال، منافذ عرض صغيرة للغاية مثل الأجهزة المحمولة).

### <a name="container-with-2-slots-properties"></a>حاوية بخصائص فتحتين

| اسم الخاصية                   | القيم | ‏‏الوصف |
|---------------------------------|--------|-------------|
| العنوان                         | نص العنوان وعلامة العنوان | يُمكن توفير عنوان اختياري للحاوية. |
| تكوين منفذ عرض صغير جدًا | **25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%**, أو **100%** | تُحدد هذه الخاصية التخطيط لمنافذ العرض الصغيرة جدًا. |
| تكوين منفذ عرض صغير   | **25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%**, أو **100%** | تُحدد هذه الخاصية التخطيط لمنافذ العرض الصغيرة، مثل الأجهزة المحمولة. |
| تكوين منفذ عرض متوسط  | **25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%**, أو **100%** | تُحدد هذه الخاصية التخطيط لمنافذ العرض المتوسطة، مثل الأجهزة اللوحية. |
| تكوين منفذ عرض كبير   | **25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%**, أو **100%** | تُحدد هذه الخاصية التخطيط لمنافذ العرض الكبيرة، مثل أجهزة الكمبيوتر. |

## <a name="container-with-3-slots"></a>حاوية بثلاث فتحات

يتم تحسين الحاوية من نوع 3 فتحات لتخطيط من ثلاثة أعمدة.

يُمكن استخدام خصائص إضافية لتحسين التخطيط لمنافذ عرض مختلفة. بالنسبة لكل منفذ عرض، يُمكن تحديد عرض كل عمود. تتوفر إعداد عرض العمود التالية:

- **33%/33%/33%** – تحتوي كافة الأعمدة الثلاثة على عرض عمود متساوي.
- **50%/25%/25%** – تحتوي الوحدة الأولى على عرض عمود 50 بالمائة، وكل وحدة من الوحدتين المتبقيين بعرض عمود 25 بالمائة. وتتوفر أيضًا الخيارات **25%/50%/25%** و **25%/25%/50%**.
- **16%/16%/67%** – تحتوي كل وحدة من الوحدتين الأولى والثانية على عمود عرض 16 بالمائة ويحتوي العمود الثالث على عرض عمود 67 بالمائة. وتتوفر أيضًا الخيارات **16%/67%/16%** و **67%/16%/16%**.

### <a name="container-with-3-slots-properties"></a>حاوية بخصائص ثلاث فتحات

| اسم الخاصية                   | القيم | ‏‏الوصف |
|---------------------------------|--------|-------------|
| العنوان                         | نص العنوان وعلامة العنوان | يُمكن إضافة عنوان اختياري إلى الحاوية. |
| تكوين منفذ عرض صغير جدًا | **33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%**, أو **67%/16%/16%** | تُحدد هذه الخاصية التخطيط لمنافذ العرض الصغيرة جدًا. |
| تكوين منفذ عرض صغير   | **33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%**, أو **67%/16%/16%** | تُحدد هذه الخاصية التخطيط لمنافذ العرض الصغيرة، مثل الأجهزة المحمولة. |
| تكوين منفذ عرض متوسط  | **33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%**, أو **67%/16%/16%** | تُحدد هذه الخاصية التخطيط لمنافذ العرض المتوسطة، مثل الأجهزة اللوحية. |
| تكوين منفذ عرض كبير   | **33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%**, أو **67%/16%/16%** | تُحدد هذه الخاصية التخطيط لمنافذ العرض الكبيرة، مثل أجهزة الكمبيوتر. |

## <a name="add-a-container-module-to-a-page"></a>إضافة وحدة حاوية إلى صفحة

لإضافة وحدة مُشغل حاوية إلى صفحة جديدة وتعيين الخصائص المطلوبة، اتبع الخطوات التالية.

1. انتقل إلى **القوالب**، ثم حدد **جديد** لإنشاء قالب جديد.
1. في مربع الحوار **قالب جديد**، تحت **اسم القالب**، أدخل **قالب الحاوية**، ثم حدد **موافق**.
1. في فتحة **النص الأساسي‬‬‏‫**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.
1. في مربع الحوار **تحديد وحدات**، حدد وحدة **الصفحة الافتراضية**، ثم حدد **موافق**.
1. حدد **حفظ**، وحدد **إنهاء التحرير** لإيداع القالب، ثم حدد **نشر** لنشره. 
1. انتقل إلى **الصفحات**، ثم حدد **جديد** لإنشاء صفحة جديدة.
1. في مربع الحوار **إنشاء صفحة جديدة**، تحت **اسم الصفحة**، أدخل **صفحة الحاوية**، ثم حدد **التالي**.
1. ضمن **اختيار قالب**، حدد **قالب الحاوية** الذي أنشأته، ثم حدد **التالي**.
1. ضمن **اختيار تخطيط**، حدد تخطيط صفحة (على سبيل المثال، **تخطيط مرن**)، ثم حدد **التالي**.
1. ضمن **مراجعة وإنهاء**، راجع تكوين الصفحة. إذا احتجت إلى تحرير معلومات الصفحة، فحدد **السابق**. إذا كانت معلومات الصفحة صحيحة، فحدد **إنشاء صفحة**. 
1. في الفتحة **الرئيسية** للصفحة الجديدة، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة‬‏‫**.
1. في مربع الحوار **تحديد وحدات**، حدد وحدة **الحاوية‬‏‎**، ثم حدد **موافق**.
1. في جزء الخصائص لوحدة الحاوية، قم بتعيين خاصية **عدد الأعمدة** إلى **1** وخاصية **العرض** إلى **ملء الحاوية**.
1. في فتحة **الحاوية‬‬‏‫**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.
1. في مربع الحوار **تحديد وحدات**، حدد وحدة **كتلة المحتوى‬**، ثم حدد **موافق**.
1. في جزء الخصائص لوحدة كتلة المحتوى، قم بتكوين العنوان والصورة والتخطيط.
1. حدد **حفظ**، ثم حدد **معاينة** لمعاينة الصفحة. يجب أن تُشاهد وحدة ميزة واحدة تتناسب مع عرض وحدة الحاوية.
1. في جزء الخصائص لوحدة الحاوية، قم بتغيير قيمة خاصية **عدد الأعمدة** إلى **3**.
1. أضف وحدتين لكتلة المحتوى‬ إلى وحدة الحاوية، وقم بتكوينهما.
1. حدد **حفظ**، ثم حدد **معاينة** لمعاينة الصفحة. يجب أن تشاهد الآن ثلاث وحدات كتلة محتوى تظهر جنبًا إلى جنب.
1. بعد تحقيق التخطيط الذي تريده، حدد **إنهاء التحرير** لإيداع الصفحة، ثم حدد **نشر** لنشرها.

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة حول مكتبة الوحدات النمطية](starter-kit-overview.md)

[وحدة أككورديون](add-accordion.md)

[وحدة علامة تبويب](add-tab.md)

[وحدة دوارة](add-carousel.md)

[وحدة كتلة النص](add-content-rich-block.md)

[الوحدة النمطية لصندوق الشراء](add-buy-box.md)

[الوحدة النمطية لعربة التسوق](add-cart-module.md)

[الوحدة النمطية للسداد مع الخروج](add-checkout-module.md)

[وحدة نمطية للرؤوس](author-header-module.md)

[وحدة التذييل](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
