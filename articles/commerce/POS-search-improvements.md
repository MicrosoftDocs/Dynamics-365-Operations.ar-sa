---
title: البحث عن المنتجات والعملاء في نقطة البيع (POS)
description: يوفر هذا الموضوع نظرة عامة حول التحسينات التي تم إدخالها على وظيفة البحث عن المنتجات والعملاء في Dynamics 365 Commerce.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 07/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Retail April 2017 update
ms.openlocfilehash: 1de8373471ff8187bd476305c9ed0b26beaa52d5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965268"
---
# <a name="product-search-and-customer-search-in-the-point-of-sale-pos"></a>البحث عن المنتجات والعملاء في نقطة البيع (POS)

[!include [banner](includes/banner.md)]

توفر نقطة البيع الحديثة (MPOS) ونقطة بيع المجموعة‬ (CPOS) ميزة بحث سهلة الاستخدام للمنتجات والعملاء. نظرًا لأن شريط البحث يقع دومًا في الجزء العلوي من نافذتي MPOS وCPOS، يستطيع الموظفون البحث بسرعة عن المنتجات والعملاء.

يستطيع الموظفون البحث عن المنتجات في عمليات الفرز والكتالوجات المقترنة بالمتجر الحالي. كما يمكنهم البحث في عمليات الفرز والكتالوجات المقترنة بأي متجر آخر في الشركة. وبالتالي، يستطيع موظفو الكاشير بيع وإرجاع المنتجات خارج عملية الفرز في المتجر. وبشكل مماثل، يستطيع الموظفون البحث عن العملاء الذين يرتبطون بالمتجر الحالي أو أي متجر آخر في الشركة. بالإضافة إلى ذلك، يستطيع الموظفون البحث عن العملاء الذين يرتبطون بشركة أخرى في المؤسسة الأصل.

## <a name="product-search"></a>البحث عن منتج

بشكل افتراضي، تتم عمليات البحث عن المنتجات في عملية الفرز في المتجر. ويعرف البحث من هذا النوع باسم *بحث محلي عن منتج*. ومع ذلك، يستطيع الموظفون بسهولة التبديل إلى أي كتالوج يرتبط بالمتجر الحالي، أو يمكنه البحث في متجر آخر. ويعرف البحث من هذا النوع باسم *بحث عن منتج عن بُعد*. لتغيير الكتالوج، حدد زر **الفئات** على الجانب الأيمن الصفحة. في أعلى الجزء الذي يظهر، حدد زر **تغيير الكتالوج**، ثم حدد أحد الكتالوجات المتوفرة لاستعراضه. سوف يبحث النظام عن المنتجات في الكتالوج المحدد.

في صفحة **تغيير الكتالوج**، يستطيع الموظفون تحديد أي متجر بسهولة، أو يمكنهم البحث عن المنتجات عبر جميع المتاجر.

![تغيير الكتالوج](./media/Changecatalog.png "تغيير الكتالوج")

تقوم عملية البحث المحلية عن منتج بالبحث ضمن خصائص المنتج التالية:

- رقم المنتج
- اسم المنتج
- ‏‏الوصف
- الأبعاد
- الكود الشريطي
- اسم البحث

### <a name="enhancements-to-local-product-searches"></a>تحسينات عمليات البحث المحلية عن المنتج

تجربة عمليات البحث المحلية عن المنتج تتسم الآن بمزيد من السهولة. تم إجراء التحسينات التالية:

- تمت إضافة قوائم منسدلة للمنتجات والعملاء إلى شريط البحث، لتمكين الموظفين من تحديد **المنتج** أو **العميل** قبل القيام بعملية البحث. بشكل افتراضي، يكون خيار **المنتج** محددًا، كما هو موضح في الشكل التالي.
- بالنسبة إلى عمليات البحث التي تستخدم كلمات أساسية متعددة (وهذا يعني عمليات البحث التي تستخدم مصطلحات البحث)، باستطاعة بائعي التجزئة تكوين ما إذا كانت نتائج البحث تتضمن النتائج التي تتطابق مع *أي* مصطلح بحث أو فقط النتائج التي تتطابق مع *كافة* مصطلحات البحث. يتوفر إعداد هذه الوظيفة في ملف تعريف وظيفة نقطة البيع، ضمن مجموعة جديدة تُسمى **البحث عن منتج**. الإعداد الافتراضي هو **مطابقة أي مصطلح بحث‬**. وهذا الإعداد هو أيضًا الإعداد الموصى به. عند استخدام إعداد **مطابقة أي مصطلح بحث**، يتم إرجاع كافة المنتجات التي تطابق جزئيًا أو كليًا مصطلح بحث واحد أو أكثر كنتائج. يتم تلقائياً فرز هذه النتائج بترتيب تصاعدي للمنتجات التي تحتوي على أكثر تطابقات الكلمات الأساسية (كاملة أو جزئية).

    يؤدي استخدام الإعداد **مطابقة جميع مصطلحات البحث‬** إلى إرجاع فقط المنتجات التي تتطابق مع جميع شروط البحث (بشكل كامل أو جزئي). ويعتبر هذا الإعداد مفيدًا عندما تكون أسماء المنتجات طويلة، ويحتاج الموظفون إلى رؤية منتجات محددة فقط في نتائج البحث. ومع ذلك، يحتوي هذا النوع من البحث على نوعين من القيود:

    - تجري عملية البحث على خصائص منتجات فردية. على سبيل المثال، يتم إرجاع فقط المنتجات التي تحتوي على جميع الكلمات الأساسية المستخدمة للبحث في خاصية منتج واحدة على الأقل.
    - لا يتم البحث في الأبعاد.

- باستطاعة بائعي التجزئة الآن تكون عملية البحث عن المنتج لإظهار الاقتراحات بينما يكتب المستخدمون أسماء المنتجات. يتوفر إعداد جديد لهذه الوظيفة في ملف تعريف وظيفة نقطة البيع، ضمن مجموعة تُسمى **البحث عن منتج**. يسمى هذا الإعداد **إظهار اقتراحات البحث أثناء الكتابة**. باستطاعة هذه الوظيفة أن تساعد الموظفين على العثور على المنتج الذي يقومون بالبحث عنه، إذ لا يحتاجون إلى كتابة الاسم الكامل يدويًا.
- تبحث الآن خوارزمية البحث عن المنتج أيضًا عن مصطلحات البحث في خاصية **اسم البحث** للمنتج.

![اقتراحات المنتجات](./media/Productsuggestions.png "اقتراحات المنتجات")

## <a name="customer-search"></a>البحث عن عميل

تُستخدم عملية البحث عن عميل للعثور على عملاء لأغراض مختلفة. على سبيل المثال، قد يحتاج موظف الكاشير إلى عرض قائمة الأمنيات أو سجل الشراء الخاص بعميل ما، أو إضافة العميل إلى حركة. تتطابق خوارزمية البحث مع مصطلحات البحث للقيم الموجودة في خصائص العميل التالية:

- الاسم
- عنوان البريد الإلكتروني
- رقم الهاتف
- رقم بطاقة الولاء
- العنوان
- رقم الحساب

من بين هذه الخصائص، يوفر الاسم أعلى مرونة لعمليات البحث بكلمات أساسية متعددة، نظرًا لإرجاع الخوارزمية لكل العملاء المطابقين لأي من الكلمات الأساسية التي تم البحث باستخدامها. يظهر العملاء الذين يطابقون معظم الكلمات الأساسية في الجزء العلوي من النتائج. بإمكان هذا السلوك مساعدة الصرافين عند إجراء عمليات بحث بكتابة الاسم الكامل، ولكن تم تبديل اسم العائلة والاسم الأول أثناء إدخال البيانات الأولية. ولكن، لأسباب تتعلق بالأداء، تحتفظ كل الخصائص الأخرى بترتيب البحث بالكلمات الأساسية. لذا، في حالة عدم تطابق ترتيب كلمات البحث الأساسية وترتيب تخزين البيانات، لن يتم إرجاع أي نتائج.

بشكل افتراضي، تتم عملية البحث عن عميل على دفاتر عناوين العملاء المرتبطة بالمتجر. ويعرف البحث من هذا النوع باسم *بحث محلي عن عميل*. ومع ذلك، باستطاعة الموظفين أيضًا البحث عن العملاء بشكل عمومي. بمعنى آخر، باستطاعتهم البحث عبر المتاجر الخاصة بالشركة وكافة الكيانات القانونية الأخرى. ويعرف البحث من هذا النوع باسم *بحث عن عميل عن بُعد*.

لإجراء بحث عمومي، باستطاعة الموظفين تحديد الزر **تصفية النتائج‬** في أسفل الصفحة، ثم تحديد الخيار **بحث في كل المتاجر**، كما هو موضح في الشكل التالي. في هذه الحالة، لا يتم إرجاع العملاء فحسب، بل يتم أيضًا إرجاع كافة أنواع الجهات التي تعد جزءًا من أي دفتر عناوين في المقار الرئيسية. تتضمن هذه الجهات العاملين والموردين وجهات الاتصال والمنافسين.

> [!NOTE]
> لإرجاع النتائج، يجب إدخال أربعة أحرف كحد أدنى لإجراء بحث عن عميل عن بُعد.

في البحث عن عميل عن بُعد، لا يظهر معرف العميل للعملاء من كيانات قانونية أخرى، نظرًا لعدم إنشاء معرف عميل لتلك الجهات في الشركة الحالية. ومع ذلك، إذا قام أحد الموظفين بفتح صفحة تفاصيل العميل، فسينشئ النظام تلقائيًا معرف عميل للجهة وسيقوم أيضًا بإقران دفاتر عناوين عميل المتجر بالعميل. وبالتالي، سيكون العميل مرئيًا في عمليات بحث المتجر المحلية التي تتم في وقت لاحق.

![البحث عن عميل عالمي](./media/Globalcustomersearch.png "البحث عن عميل عالمي")

### <a name="enhancements-to-local-customer-search"></a>تحسينات عملية البحث المحلية عن العميل

تم تبسيط عمليات البحث التي تعتمد على رقم الهاتف. تتجاهل عمليات البحث هذه الآن الأحرف الخاصة، مثل المسافات والشُرط والأقواس، التي تمت إضافتها عند إنشاء العميل. ولذلك، لا يلزم موظفي الكاشير القلق بشأن تنسيق رقم الهاتف عند البحث. على سبيل المثال، إذا تم إدخال رقم هاتف العميل على الشكل **123-456-7890**، فباستطاعة موظف الكاشير البحث عن العميل عن طريق كتابة **1234567890**، أو عن طريق إدخال الأرقام الأولى القليلة من رقم الهاتف.

> [!NOTE]
> قد يكون لدى العميل أرقام هواتف متعددة وعناوين بريد إلكتروني متعددة. تبحث خوارزمية بحث العملاء أيضًا من خلال عناوين البريد الإلكتروني وأرقام الهواتف الثانوية هذه، ولكن صفحة نتائج بحث العميل تعرض فقط عنوان البريد الإلكتروني ورقم الهاتف الأساسيين فقط. قد يتسبب هذا في حدوث التباس معين لأن نتائج العميل المرتجعة لن تُظهر رقم الهاتف أو عنوان البريد الإلكتروني الذي يتم البحث عنه. نحن نخصص لتحسين شاشة نتائج بحيث لإظهار هذه المعلومات في إصدار مستقبلي.

يمكن أن يكون البحث التقليدي عن العملاء مستهلكاً للوقت، نظراً لأنه يقوم بالبحث في عدة حقول. يمكن للصرافين الآن بدلاً من ذلك البحث في خاصية عميل واحدة، مثل الاسم أو عنوان البريد الإلكتروني أو رقم الهاتف. تُعرف الخصائص التي تستخدمها خوارزمية البحث عن العميل إجماليًا باسم *معايير البحث عن العميل*. يستطيع مسؤول النظام بسهولة تكوين معيار واحد أو أكثر كاختصارات ستظهر في نقطة البيع. نظراً لأن البحث يقتصر على معيار واحد، يتم عرض نتائج البحث ذات الصلة فقط، ويكون الأداء أفضل بكثير من أداء البحث القياسي عن العملاء. يبين الرسم التوضيحي التالي اختصارات البحث عن العملاء في نقطة البيع.

![اختصارات البحث عن العميل](./media/SearchShortcutsPOS.png "اختصارات البحث عن العميل")

لتعيين معايير البحث كاختصارات، يجب على المسؤول فتح صفحة **معلمات التجارة** في Commerce، ثم تحديد جميع المعايير التي يجب أن تظهر كاختصارات على علامة التبويب **معايير البحث في نقطة البيع**.

![تكوين اختصارات البحث](./media/ConfigureShortcutsAX.png "تكوين اختصارات البحث")

> [!NOTE]
> إذا قمت بإضافة عدد كبير جداً من الاختصارات، سوف تزدحم القائمة ا7لمنسدلة على شريط البحث في نقطة البيع، وربما تتأثر خبرة البحث لدى الموظف بذلك. من المستحسن أن تقوم فقط بإضافة العديد من الاختصارات كما تريد.

يحدد حقل **ترتيب العرض** الترتيب الذي تظهر به الاختصارات في نقطة البيع. المعايير التي تظهر هي الخصائص المبتكرة التي تستخدمها خوارزمية البحث عن العميل للبحث عن العملاء. ومع ذلك، يستطيع الشركاء إضافة خصائص مخصصة كاختصارات بحث. لإضافة خصائص مخصصة كاختصارات بحث، يجب على مسؤول النظام توسيع التعداد القابل للتوسيع (تعداد) الذي يتم استخدامه لمعايير البحث عن العملاء، ثم تمييز الخصائص المخصصة للشريك كاختصارات. الشركاء مسؤولون عن كتابة الكود للبحث عن النتائج عند استخدام اختصارات لوحة المفاتيح المخصصة الخاصة بهم لعمليات البحث.

> [!NOTE]
> لا تؤثر خاصية مخصصة تمت إضافتها إلى التعداد على خوارزمية البحث القياسية عن العملاء. بتعبير آخر، لن تبحث خوارزمية البحث عن العملاء في الخاصية المخصصة. يستطيع المستخدمون استخدام خاصية مخصصة لعمليات البحث فقط، إذا تمت إضافة هذه الخاصية المخصصة كاختصار، أو إذا تم تجاوز خوارزمية البحث الافتراضية.

في الإصدار القادم من Commerce، سيتمكن بائعو التجزئة من تعيين وضع البحث الافتراضي للعميل في نقطة البيع على **بحث في كل المتاجر**‬‏. يمكن أن يكون هذا التكوين مفيدًا في السيناريوهات التي يجب فيها البحث فورًا عن العملاء الذين تم إنشاؤهم خارج نقطة البيع (علي سبيل المثال، قبل حتى تشغيل مهمة التوزيع). سيتوفر خيار جديد وهو **وضع البحث الافتراضي للعميل** في ملف تعريف وظيفة نقطة البيع. عيِّن الخيار على **تشغيل** لتعيين وضع البحث الافتراضي على **بحث في كل المتاجر**. ستقوم كل محاولة من محاولات البحث للعميل بعد ذلك بإجراء مكالمة فورية للمقر الرئيسي.

للمساعدة تجنب مشكلات الأداء غير المتوقعة ، يتم إخفاء هذا التكوين خلف علامة إصدارات التقييم الموجودة باسم **CUSTOMERSEARCH_ENABLE_DEFAULTSEARCH_FLIGHTING**. لذا، لإظهار واجهة المستخدم (UI) إعداد **وضع بحث العميل الافتراضي**، يجب إنشاء بائع التجزئة بطاقة دعم لاختبار قبول المستخدم (UAT) وبيئة الإنتاج. بعد استلام البطاقة، سيعمل فريق الهندسة مع بائع التجزئة للتأكد من إجراء بائع التجزئة للاختبار في البيئات غير المنتجة الخاصة به لتقييم الأداء وتطبيق أي تحسينات مطلوبة.



[!INCLUDE[footer-include](../includes/footer-banner.md)]