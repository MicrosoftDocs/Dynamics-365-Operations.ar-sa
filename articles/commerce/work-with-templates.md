---
title: العمل مع القوالب
description: يصف هذا المقال كيفية العمل مع القوالب في Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 02/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: cbe9d103da9c86dcf3aad54ec036282d2bb3faca
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282670"
---
# <a name="work-with-templates"></a>العمل مع القوالب

[!include [banner](includes/banner.md)]

يصف هذا المقال كيفية العمل مع القوالب في Microsoft Dynamics 365 Commerce.

كما تمت مناقشته في [نظرة عامة على القوالب والتخطيطات](templates-layouts-overview.md)، تحدد القوالب مجموعة من الخيارات المتوفرة للمؤلفين المذكورين. تعتبر القوالب مفيدة لفريق تأليف الويب الخاص بالمؤسسة لأسباب عديدة، ويمكن أن تساعد القوالب المبنية على كل الأهداف التالية:

- قم بتبسيط تجربة التأليف لأدوار محرر المحتوى اليومي.

    - قم بتصفية خيارات الوحدة النمطية بحيث يتم فقط إظهار الوحدات ذات الصلة لمقطع صفحة محدد. (على سبيل المثال، يمكن تكوين مقطع التسويق للقالب لتصفية الوحدات غير المرتبطة التي ينبغي عدم استخدامها أبدًا في ذلك السياق، والتي ستعمل على تعقيد مهام تأليف المحتوى فقط إذا كانت معروضة).
    - قم بتكوين إعداد الوحدة النمطية الافتراضي للمساعدة على تحسين كفاءة التأليف.
    - قم بتحديد أجزاء الصفحة الافتراضية للمساعدة على تحسين كفاءة التأليف. (على سبيل المثال، ستظهر أجزاء الرأس والتذييل في قالب تلقائيًا على كل صفحة في الاتجاه الآخر).

- اجعل مواقع المؤسسة مرتبطة بالعلامة التجارية عن طريق تحديد مجموعة معتمدة من خيارات ترتيب الوحدة النمطية وتكوينها.

    > [!TIP] 
    > تمد مواقع التجارة الإلكترونية الناجحة العملاء بأنماط تصميم تجربة المستخدم (UX) الخاصة بالعلامة التجارية المألوفة والقابلة للتكرار. باستخدام القوالب، فإنك تساعد في التحكم في التناسق عبر الموقع.

- قم بتحسين درجات تحسين محرك البحث (SEO) بتأكيد بيانات التعريف وتعريفات الصفحة التي تم تعريفها برمجيًا والقابلة للتكرار.

> [!NOTE]
> على الرغم من أنه يتم تصميم القوالب للتحكم في التناسق عبر أحد المواقع، إلا أنه يمكن تكوينها نظريًا بحيث لا تفرض أي تناسق. يمكن للمسؤولين عن العلامة التجارية والموقع تحديد أي مستوى من الاختلاف للصفحات على الموقع الخاص بهم. على سبيل المثال، يمكن ترك القالب مفتوحًا بالكامل، حتى يتمكن مؤلفو المحتوى من إنشاء أي تصميم للصفحة يختارونه. في هذه الحالة، لا تكون أي من الميزات الموجودة في القائمة السابقة قابلة للتطبيق.

## <a name="modify-a-template"></a>تعديل قالب

يتم تعديل القوالب باستخدام محرر القالب.

لفتح محرر القالب في منشئ موقع Commerce، اتبع إحدى الخطوات التالية:

- في جزء التنقل الخاص بالموقع الخاص بك، حدد **قوالب**، ثم حدد القالب المطلوب تعديله.
- في محرر الصفحة الخاص بالصفحة الموجودة، حدد العقدة العليا في شجرة المخطط التفصيلي على اليسار. ثم في جزء الخصائص الموجود على اليمين، حدد **تحرير القالب**.

تعرض طريقة العرض الشجرة للمخطط التفصيلي على اليسار خيارات الوحدة النمطية وبنياتها المتوفرة للتخطيطات والصفحات التابعة. عندما تقوم بتحديد وحدة نمطية في شجرة المخطط التفصيلي، فإنه يمكنك عرض خصائص القالب الخاصة بالوحدة النمطية المحددة في جزء الخصائص على الجانب الأيمن. إن بعض هذه الخصائص فريدة لتحرير القالب. يصف الجدول التالي هذه الخصائص.

| اسم الخاصية | ‏‏الوصف |
|---|---|
| الحد الأدنى لمرات الحدوث | تحدد هذه الخاصية الحد الأدنى لعدد التكرارات للوحدة النمطية المحددة. على سبيل المثال، إذا قمت بتعيين القيمة على **1**، تكون الوحدة النمطية مطلوبة للمؤلفين المذكورين، بينما إذا تم تعيين القيمة على **0** (صفر)، فإن الوحدة النمطية تكون اختيارية. |
| الحد الأقصى لمرات الحدوث | تحدد هذه الخاصية الحد الأقصى لعدد التكرارات للوحدة النمطية المحددة. على سبيل المثال، إذا تم تعيين القيمة على **1**، فإنه يمكن إضافة الوحدة النمطية مرة واحدة فقط. |
| الحد الأدنى للوحدات النمطية (الحاويات) | بالنسبة للوحدات النمطية التي تحتوي على وحدات نمطية أخرى (أي، *لوحدات الحاويات النمطية*)، تُحدد هذه الخاصية العدد الأدنى من الوحدات النمطية الإجمالية التي ينبغي إضافتها كعناصر فرعية. على سبيل المثال، بالنسبة للوحدة النمطية الدوارة، فإنه قد يتم تعيين القيمة على رقم أكبر من 1. |
| الحد الأقصى للوحدات النمطية (الحاويات) | بالنسبة لوحدات الحاويات النمطية، تحدد هذه الخاصية العدد الأقصى للوحدات النمطية الإجمالية التي يجب إضافتها كعناصر تابعة. على سبيل المثال، بالنسبة للوحدة النمطية الدوارة، فإنه قد يتم تعيين القيمة على رقم أقل من 10. |
| مؤَّمن | يظهر عنصر التحكم المنطقي **المؤمن** بجانب كافة خصائص الوحدة النمطية الأساسية. إنه يتيح لمؤلف القالب تأمين إعداد الوحدة النمطية في القالب. لا يمكن تجاوز إعداد الوحدة النمطية المؤمن بواسطة أية تخطيطات أو صفحات فرعية. وتصبح قيمة خاصية قابلة للتحرير بشكل مركزي لكل التخطيطات والصفحات التي تستخدم القالب. |

## <a name="create-a-new-template"></a>إنشاء قالب جديد

لإنشاء قالب جديد في منشئ الموقع، اتبع الخطوات التالية.

1. في جزء التنقل الخاص بالموقع الخاص بك، حدد **قوالب** لفتح طريقة عرض مفتش القالب.
1. حدد **قالب جديد**.
1. في مربع حوار إنشاء القالب، أدخل اسمًا ووصفًا للقالب. سيتم عرض القيم التي تقوم بإدخالها للمؤلفين عند قيامهم بإنشاء صفحات جديدة. وبالتالي، أدخل بيانات التعريف التي ستكون مفيدة لمؤلفي الصفحة. على سبيل المثال، أدخل **استخدام هذا القالب لإنشاء صفحات تسويق عامة** كالوصف. يمكن تحرير بيانات التعريف هذه في وقت لاحق.
1. حدد **موافق** لإنشاء القالب الجديد وفتح محرر القالب. يعرض محرر القالب شجرة مخطط تفصيلي على اليسار وجزء الخاصية على اليمين.
1. في شجرة المخطط التفصيلي، قم بتوسيع العقد وحدد فتحة **رأس HTML**.
1. في حالة عدم وجود أية وحدات نمطية في هذه الفتحة حتى الآن، حدد زر علامة الحذف (**...**)، ثم حدد **إضافة وحدة نمطية**.
1. في مربع الحوار **إضافة وحدة نمطية**، حدد **ملخص الصفحة الافتراضية**، ثم حدد **موافق**.
1. في شجرة المخطط التفصيلي، حدد الوحدة النمطية الجديدة، ثم في جزء الخصائص، أدخل أية إعدادات افتراضية ينبغي تكوينها تلقائيًا لكافة صفحات القالب التابعة. إذا لم تكن تريد أية إعدادات افتراضية، فاترك القيم فارغة.
1. في شجرة المخطط التفصيلي، حدد الفتحة **النص الأصلي**، حدد زر علامة الحذف، ثم حدد **إضافة وحدة نمطية**.
1. حدد الوحدة النمطية لحاوية الصفحة (قد يكون هناك خيار واحد فقط)، ثم حدد **موافق**.

ضمن وحدة الحاوية النمطية للصفحة الجديدة، فإنك سترى مجموعة جديدة من الفتحات (**الرأس** و **الجزء الرئيسي** وهكذا). وهنا، يمكنك إضافة خيارات الوحدة النمطية التي سيتم توفيرها للمؤلفين عند إنشاء صفحات من هذا القالب وتكوينها. بشكل افتراضي، إذا لم تقم بإضافة أية وحدات نمطيه إلى فتحة، فإنه يتم دعم كافة أنواع الوحدات النمطية المتوفرة لتلك الفتحة.

أصبح القالب الآن صالحًا تقنيًا، ويمكن حفظه وإيداعه واستخدامه لإنشاء صفحات جديدة. ومع ذلك، تصف المقاطع الثلاثة التالية بعض الإعدادات الافتراضية الأخرى التي قد ترغب في تكوينها أولاً.

## <a name="add-a-header-and-a-footer"></a>إضافة رأس وتذييل

إذا كان موقعك يحتوي على جزء رأس، فاتبع هذه الخطوات في منشئ الموقع لإضافة رأس وتذييل لقالب.

1. في شجرة المخطط التفصيلي، قم بتوسيع فتحة **النص الأصلي** والوحدة النمطية للصفحة الفرعية.
1. حدد فتحة **الرأس**.
1. حدد زر علامة الحذف لفتحة **الرأس**، ثم حدد **إضافة جزء**.
1. ابحث عن جزء الرأس للموقع الخاص بك وحدده، ثم حدد **موافق**.

ستقوم الآن كافة الصفحات التي تستخدم القالب بتوريث جزء الرأس هذا تلقائيًا.

إذا لم يكن الموقع يحتوي على جزء رأس بعد، راجع [إنشاء جزء](work-with-fragments.md#create-a-fragment) للحصول على معلومات عن كيفية إنشائه، ثم أكمل الإجراء السابق.

## <a name="change-the-template-theme"></a>تغيير سمة القالب

لتعيين النسق الافتراضي لكافة الصفحات التي تستخدم قالب ما، اتبع هذه الخطوات في منشئ الموقع.

1. في شجرة المخطط التفصيلي الخاصة بالصفحة الموجودة على اليسار، قم بتوسيع الفتحة **النص الأصلي**.
1. في فتحة **النص الأساسي**، حدد وحدة حاوية نمطية لصفحة (على سبيل المثال، **الصفحة الافتراضية**).
1. في جزء الخصائص على اليمين، في حقل **السمة**، حدد سمة.

بشكل افتراضي، ستقوم كافة الصفحات الجديدة الآن باستخدام السمة المحددة. لمنع الصفحات من تجاوز هذا الإعداد عند مستوى التخطيط أو الصفحة، قم بتعيين عنصر التحكم المنطقي **المؤمن** إلى **حقيقي**.

## <a name="add-a-script-to-a-template"></a>إضافة برنامج نصي إلى قالب

يمكنك إضافة عناصر **&lt;برنامج نصي&gt;** HTML تحتوي على JavaScript إلى القالب الخاص بك. بهذه الطريقة، يمكنك توفير سلوكيات البرنامج النصي الافتراضية لأقسام رأس HTML وبداية النص الأصلي ونهاية النص الأصلي للصفحات.

لإضافة برنامج نصي إلى قالب في منشئ الموقع، اتبع الخطوات التالية.

1. في شجرة المخطط التفصيلي الموجودة على اليمين، حدد الفتحة التي تريد إضافة عنصر **&lt; البرنامج النصي &gt;** (على سبيل المثال، رأس HTML أو بداية النص الأصلي أو نهاية النص الأصلي).
1. حدد زر علامة الحذف للفتحة، ثم حدد **إضافة وحدة نمطية**.
1. في مربع الحوار **إضافة وحدة نمطية**، حدد الوحدة النمطية لبرنامج نصي (على سبيل المثال، **برنامج نصي خارجي** أو **برنامج نصي مضمن**).
1. في جزء الخصائص على اليمين، في عنصر تحكم خاصية البرنامج النصي المناسب (على سبيل المثال، **برنامج نصي مضمن** أو **علامات البرنامج النصي**)، أدخل البرنامج النصي الخاص بك.
1. في جزء الخصائص، أدخل أية إعدادات اختيارية أخرى تريد تكوينها.

> [!TIP]
> إذا كنت تريد إعادة استخدام أية وحدات البرنامج النصي لقوالب أخرى، فإنه يمكنك تحويلها إلى أجزاء. بهذه الطريقة، يمكنك المساعدة في جعل عملية التأليف أكثر فعالية، وأن تقوم بمركزة عملية التحديث. للحصول على معلومات حول كيفية تحويل الوحدة النمطية لبرنامج نصي إلى جزء، راجع [حفظ تكوين وحدة نمطية موجودة كجزء](work-with-fragments.md#save-an-existing-module-configuration-as-a-fragment).

## <a name="save-check-in-preview-and-publish-a-template"></a>حفظ قالب وإيداعه ومعاينته ونشره

لحفظ قالب وإيداعه في منشئ الموقع، اتبع الخطوات التالية.

1. حدد **حفظ** في أعلى محرر القالب. لا تؤثر التغييرات المحفوظة على الصفحات اللاحقة حتى يتم إيداعها.
1. حدد **إنهاء التحرير**. تكون التغييرات الخاصة بك قابلة للاكتشاف الآن لعمليات سير العمل اللاحقة.

لمعاينة التغييرات الخاصة بك، فإما أن تقوم بفتح صفحة موجودة تستخدم القالب أو إنشاء صفحة جديدة من القالب.

بعد الانتهاء من معاينة التغييرات التي تمت على القالب، اتبع إحدى هذه الخطوات لنشر القالب على موقعك المباشر:

* انتقل إلى **القوالب**، حدد القالب، ثم حدد **نشر**.
* حدد اسم المخطط لفتح محرر التخطيط، ثم حدد **نشر**.
* انشر صفحة تشير إلى القالب غير المنشور. يتم نشر القالب تلقائيًا.

> [!WARNING]
> عند نشر قالب، أو أي عنصر نظام إدارة محتوى آخر (CMS)، فإنه يمكن اكتشافه على الإنترنت. لا تقم بنشر المستندات أو الأصول حتى تكون مستعدًا لجعلها عامة. إن إصدارات المستندات التي تم حفظها وإيداعها، ولكن لم يتم نشرها حتى الآن، تكون قابلة للاكتشاف فقط لمستخدمي النظام المصادقين.

## <a name="rename-a-template"></a>إعادة تسمية قالب

لإعادة تسمية قالب موجود في منشئ الموقع، اتبع الخطوات التالية.

1. في جزء التنقل الأيمن، حدد **القوالب**.
1. حدد اسم القالب الذي تريد إعادة تسميته.
1. حدد **تحرير** لبدء تحرير القالب. لا يمكنك تحرير قالب إذا كان هناك شخص آخر يقوم بتحريره.
1. في جزء خصائص القالب، حدد رمز القلم الموجود بجوار اسم القالب.
1. قم بتحرير اسم القالب كما تقتضي الحاجة.
1. حدد علامة الاختيار لتأكيد تغيير الاسم.
1. حدد **إنهاء التحرير**.

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على القوالب والتخطيطات](templates-layouts-overview.md)

[العمل مع التخطيطات سابقة الإعداد](work-with-layouts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
