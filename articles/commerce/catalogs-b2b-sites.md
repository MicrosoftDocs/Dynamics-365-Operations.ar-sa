---
title: إنشاء كتالوجات Commerce لمواقع B2B
description: يصف هذا الموضوع كيفية إنشاء كتالوجات Commerce لمواقع B2B في Microsoft Dynamics 365 Commerce.
author: ashishmsft
ms.date: 04/28/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 868f6bbeefeb1698bb136d52c09cebf293c95731
ms.sourcegitcommit: 0abc777986112ea2332f5bf0e815b303b952356c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/29/2022
ms.locfileid: "8656823"
---
# <a name="create-commerce-catalogs-for-b2b-sites"></a>إنشاء كتالوجات Commerce لمواقع B2B

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

يصف هذا الموضوع كيفية إنشاء كتالوجات منتجات Commerce لمواقع B2B في Microsoft Dynamics 365 Commerce. للحصول على إجابات عن الأسئلة المتداولة حول كتالوجات Commerce لمواقع B2B، راجع [الأسئلة المتداولة حول كتالوجات Commerce لمواقع B2B](catalogs-b2b-sites-FAQ.md).

> [!NOTE]
> ينطبق هذا الموضوع على الإصدار 10.0.26 من Dynamics 365 Commerce والإصدارات الأحدث.

يمكنك استخدام كتالوجات Commerce لتحديد المنتجات التي تريد عرضها في متاجر B2B عبر الإنترنت عندما تقوم بإنشاء كتالوج، فإنك تحدد المتاجر عبر الإنترنت التي يتم تقديم المنتجات فيها، وتضيف المنتجات التي تريد تضمينها، وتعزز عروض المنتجات عن طريق إضافة تفاصيل ترويج السلع‬. يمكنك إنشاء كتالوجات متعددة لكل متجر B2B عبر الإنترنت.

تسمح لك كتالوجات منتجات Commerce تعريف المعلومات التالية:

- **التدرج الهرمي للتنقل الخاص بالكتالوج** – بإمكان المؤسسات إنشاء بنية فئة مميزة لكتالوجها المعين.
- **بيانات تعريف السمات الخاصة بالكتالوج** – تحتوي السمات على تفاصيل حول أحد المنتجات. من خلال تعيين سمات لفئة من التدرج الهرمي للتنقل، يمكنك تحديد قيم تلك السمات على مستوى المنتجات التي تم تعيينها لهذه الفئة. بإمكان المؤسسات بعد ذلك إكمال هذه المهام:

    - تعريف قيم السمات الخاصة بالكتالوج.
    - التحكم في رؤية السمات على مستوى الكتالوج.
    - تحديد المدققات الخاصة بكتالوج فردي.

- **القنوات** – بإمكان المؤسسات ربط أكثر من قناة B2B واحدة عبر الإنترنت بكتالوج. يتوفر الدعم الشامل للكتالوجات في الوقت الحالي فقط لمتاجر B2B عبر الإنترنت.
- **التدرجات الهرمية للعملاء**– بالنسبة لقناة B2B معينةـ بإمكان للمؤسسات توفير كتالوج محدد لشركاء B2B معينين من خلال ربط التسلسلات التدرجات للعملاء بهذا الكتالوج.
- **مجموعات الأسعار** – يمكنك تكوين الأسعار والعروض الترويجية الخاصة بكتالوج محدد. تُعد هذه القدرة السبب أساسي لتحديد كتالوج لقناة B2B. تمكّن مجموعات الأسعار للكتالوجات المؤسسات من إتاحة المنتجات لمؤسسات B2B المقصودة وتطبيق الأسعار والخصومات المفضلة لديها. بإمكان عملاء B2B الذين يطلبون المنتجات من كتالوج مكوّن الاستفادة من الأسعار الخاصة والعروض الترويجية بعد تسجيل دخولهم إلى موقع B2B في Commerce. لتكوين أسعار كتالوج محددة، حدد **مجموعات الأسعار** من علامة تبويب **الكتالوجات** لربط مجموعة أسعار أو أكثر بالكتالوج. سيتم تطبيق كل الاتفاقيات التجارية ودفاتر يومية تعديل السعر والخصومات المتقدمة التي تم ربطها بمجموعة الأسعار نفسها عندما يقوم العملاء بطلب منتجات من هذا الكتالوج. (تتضمن الخصومات المتقدمة الحد والكمية وخصومات الخلط والمطابقة.) لمزيد من المعلومات حول مجموعات الأسعار، راجع [مجموعات الأسعار](price-management.md#price-groups).

> [!NOTE]
> تتوفر هذه الميزة اعتبارًا من إصدار 10.0.26 من Dynamics 365 Commerce. لتكوين تكوينات خاصة بالكتالوج مثل التدرج الهرمي للتنقل والتدرج الهرمي للعملاء، في Commerce Headquarters، افتح مساحة عمل **إدارة الميزات** (**إدارة النظام \> مساحات العمل \> إدارة الميزات**)، ومكّن الميزة **تمكين استخدام كتالوجات متعددة على قنوات البيع بالتجزئة**، ثم شغّل الوظيفة **1110 CDX**.

## <a name="catalog-process-flow"></a>سير معالجة الكتالوج

تتضمن عملية إنشاء كتالوج ومعالجته أربع خطوات عامة. يمكن العثور على شرح مفصل لكل خطوة في القسم التالي.

1. **[تكوين](#configure-the-catalog)**

    - إقران التدرج الهرمي للتنقل.
    - تحديد تواريخ الانتهاء السارية وتواريخ انتهاء الصلاحية، إذا كانت قابلة للتطبيق.
    - إضافة المنتجات وتصنيفها.
    - ربط مجموعات الأسعار.
    - ربط تدرج هرمي للعملاء بالخاص بمؤسسات B2B. 
    - ربط مجموعة سمات الأبعاد الافتراضية لبعض المدققات مثل الحجم والنمط واللون.
    - تعيين بيانات تعريف السمة.

1. **[التحقق من الصحة](#validate-the-catalog)** – في هذه الخطوة، تقوم بتشغيل قواعد التحقق من الصحة التي تفرض سلوكًا معينًا. فيما يلي بعض الأمثلة:

    - تأكد من عدم وجود أي منتجات غير مصنفة في فئات.
    - تأكد من أن جميع الأصناف المصنفة‬ لكل قناة مرتبطة بكتالوج.

1. **[الموافقة](#approve-the-catalog)**
1. **[جارٍ النشر](#publish-the-catalog)**

## <a name="set-up-the-catalog"></a>إعداد الكتالوج

استخدم المعلومات الموجودة في هذا القسم لإعداد الكتالوج.

### <a name="configure-the-catalog"></a>تكوين الكتالوج

في Commerce Headquarters، انتقل إلى **البيع بالتجزئة والتجارة‬ \> الكتالوجات والتشكيلات \> جميع الكتالوجات‬** لتكوين الكتالوج.

عندما تقوم بإنشاء كتالوج جديد، يجب عليك أولاً ربط بقناة أو أكثر. يمكن استخدام فقط الأصناف المرتبطة [بالتشكيلات](/dynamics365/unified-operations/retail/assortments) في قناتك المحددة عند إنشاء الكتالوج. لربط الكتالوج بقناة واحدة أو أكثر ، حدد **إضافة** ؤ الكتالوج علامة التبويب السريعة **قنوات Commerce** من صفحة **إعداد الكتالوج**.

#### <a name="associate-the-navigation-hierarchy"></a>إقران التدرج الهرمي للتنقل

لإضافة منتجات إلى كتالوج، يجب تحديد تدرج هرمي للتنقل. يدعم التدرج الهرمي للتنقل بنية الفئة للكتالوج. يجب أن تختار أحد لتدرجات الهرمية للتنقل المرتبطة بالقنوات التي حددتها في علامة التبويب السريعة **قنوات Commerce** في صفحة **إعداد الكتالوج**. لربط تدرج هرمي افتراضي للتنقل مع كل قناة من قنواتك، انتقل إلى **البيع بالتجزئة والقنوات \> إعداد القناة \> فئات القناة وسمات المنتج‬**.

#### <a name="specify-time-effective-and-expiration-dates"></a>تحديد تواريخ السريان وانتهاء الصلاحية

لتحديد تواريخ السريان وانتهاء الصلاحية لكتالوج، حدد العقدة العليا في التدرج الهرمي للكتالوج للرجوع إلى طريقة عرض رأس الكتالوج الرئيسي. قم بتكوين تواريخ السريان وانتهاء الصلاحية، كما هو مطلوب، على علامة التبويب السريعة **عام**.

#### <a name="add-and-categorize-products"></a>إضافة المنتجات وتصنيفها

لتكوين المنتجات لإضافتها إلى الكتالوج، في Commerce Headquarters، انتقل إلى **البيع بالتجزئة والتجارة‬ \> الكتالوجات والتشكيلات \> جميع الكتالوجات‬**. ثم على علامة التبويب **الكتالوجات**، حدد **إضافة منتجات**.

أو حدد عقدة في التدرج الهرمي للتنقل. ستتمكن بعد ذلك من إضافة المنتجات مباشرة إلى فئة في الكتالوج.

#### <a name="associate-price-groups"></a>ربط مجموعات الأسعار

لتكوين أسعار خاصة بالكتالوج، يجب ربط مجموعة أسعار واحدة أو أكثر بالكتالوج. لربط مجموعات الأسعار بكتالوج، في Commerce Headquarters، انتقل إلى **البيع بالتجزئة والتجارة‬ \> الكتالوجات والتشكيلات \> جميع الكتالوجات‬**. ثم في علامة التبويب **الكتالوجات**، ضمن **التسعير**، حدد **مجموعات الأسعار**. سيتم تطبيق كل الاتفاقيات التجارية ودفاتر يومية تعديل السعر والخصومات المتقدمة (الحد والكمية وخصومات الخلط والمطابقة) التي تم ربطها بمجموعة الأسعار نفسها عند قيام العملاء بطلب منتجات من الكتالوج.

لمزيد من المعلومات حول مجموعات الأسعار، راجع [مجموعات الأسعار](price-management.md#price-groups).

> [!NOTE]
> لا يمكنك إنشاء مجموعة أسعار جديدة من الصفحة **جميع الكتالوجات**‬ . بدلاً من ذلك، يجب عليك إنشاؤها من الصفحة **جميع مجموعات الأسعار**. ويجب عليك عندئذٍ ربطها بالكتالوج في الصفحة **جميع الكتالوجات**.

#### <a name="associate-a-customer-hierarchy"></a>ربط التدرج الهرمي للعميل

لربط التدرجات الهرمية للعملاء، في Commerce Headquarters، انتقل إلى **البيع بالتجزئة والتجارة‬ \> الكتالوجات والتشكيلات \> جميع الكتالوجات‬**. ثم في علامة التبويب **الكتالوجات**، ضمن **التدرج الهرمي للعميل**، حدد **تعيين التدرجات الهرمية** لربط تدرج هرمي واحد أو أكثر من التدرجات الهرمية للعملاء بالكتالوج.

> [!NOTE]
> لا يمكنك إنشاء تدرج هرمي جديد للعميل من الصفحة **جميع الكتالوجات**‬ . بدلاً من ذلك، يجب عليك إنشاؤه من الصفحة **التدرجات الهرمية للعملاء**. ويجب عليك عندئذٍ ربطها بالكتالوج في الصفحة **جميع الكتالوجات**.

#### <a name="associate-default-dimension-attribute-group-for-refiners-such-as-size-style-and-color"></a>ربط مجموعة سمات الأبعاد الافتراضية لبعض المدققات مثل الحجم والنمط واللون

لربط مجموعة سمات أبعاد افتراضيه لبعض المدققات مثل الحجم والنمط واللون، في Commerce Headquarters، انتقل إلى **البيع بالتجزئة والتجارة \> الكتالوجات والتشكيلات \> جميع الكتالوجات**. ثم في علامة التبويب **الكتالوجات**، ضمن **السمات**، حدد **مجموعات السمات‏‎**.

#### <a name="set-attribute-metadata"></a>تعيين بيانات تعريف السمة

لتكوين بيانات تعريف السمات، في Commerce Headquarters، انتقل إلى **البيع بالتجزئة والتجارة‬ \> الكتالوجات والتشكيلات \> جميع الكتالوجات‬**. ثم في علامة التبويب **الكتالوجات**، ضمن **السمات**، حدد **تعيين بيانات تعريف السمات‏‎**. لتحديد السمات التي يجب أن تكون قابلة للعرض والتنقية، حدد فئة في التدرج الهرمي للتنقل الخاص بالكتالوج المقترن، ثم ضمن **سمات منتجات الكتالوج**، حدد سمة. ثم حدد **إظهار السمة على القناة**. بشكل افتراضي، جميع السمات القابلة للعرض هي قابلة للبحث أيضًا. لجعل السمات قابلة للتنقية بشكل اختياري، حدد **يمكن تنقيتها**.

### <a name="validate-the-catalog"></a>التحقق من صحة الكتالوج

قبل أن يصبح الكتالوج متوفرًا للاستخدام، يجب التحقق من صحته ونشره.

للتحقق من صحة الكتالوج، اتبع هذه الخطوات.

1. في علامة التبويب **الكتالوجات** في صفحة **جميع الكتالوجات**، ضمن **التحقق من الصحة**، حدد **التحقق من صحة الكتالوج** لتشغيل التحقق من الصحة. هذه الخطوة مطلوبة. ستتحقق من دقة الخطوة المطلوبة.
1. حدد **عرض نتائج** للاطلاع على تفاصيل التحقق من الصحة. إذا تم العثور على أخطاء، فيجب تصحيح البيانات ثم تشغيل التحقق من الصحة مرة أخرى حتى اجتيازه.

### <a name="approve-the-catalog"></a>الموافقة على الكتالوج

بعد التحقق من صحة كتالوج، يجب الموافقة عليه.

لبدء سير عمل الموافقة على الكتالوج، اتبع الخطوات التالية.

1. في جزء الإجراءات، في صفحة **جميع الكتالوجات**، جدد **سير العمل \> إرسال‏‎**.
1. انتقل إلى **البيع بالتجزئة والتجارة \> إعداد المقرات الرئيسية \> مهام سير العمل في Commerce** لتكوين الخطوات والمستخدمين المخولين لسير العمل. سيحدد سير العمل الخطوات اللازمة لإدخال الكتالوج في حالة **موافق عليه**.

### <a name="publish-the-catalog"></a>نشر الكتالوج

عندما يصبح الكتالوج في الحالة **موافق عليه**، يمكنك نشره عن طريق تحديد **نشر** في قائمة **الكتالوجات**. بعد أن يصبح الكتالوج في الحالة **منشور**، يمكن استخدامه في إدخال أمر مركز الاتصال وإرسال عمليات الكتالوج. يمكنك نشر كتالوج يدويًا أو باستخدام عملية دُفعية. يحدد تاريخ السريان الذي قمت بتحديده للكتالوج الوقت الذي تكون فيه المنتجات متوفرة في المتجر عبر الإنترنت. يحدد تاريخ انتهاء الصلاحية الذي قمت بتحديده وقت إزالة المنتجات من المتجر عبر الإنترنت.

> [!NOTE]
> يمكنك نشر كتالوج يحتوي على المنتجات التي تحتوي على تحذيرات. ولكن هذه المنتجات لن تظهر في المتجر عبر الإنترنت.

## <a name="additional-resources"></a>الموارد الإضافية

[تأثير قابلية توسعة كتالوجات Commerce لعمليات تخصيص B2B](catalogs-b2b-sites-dev.md)

[الأسئلة المتداولة حول كتالوجات Commerce لمواقع B2B](catalogs-b2b-sites-FAQ.md)