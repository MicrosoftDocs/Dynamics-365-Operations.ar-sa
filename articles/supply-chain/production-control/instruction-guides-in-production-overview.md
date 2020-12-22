---
title: توفير دلائل الحقيقة المختلطة للعمال العاملين في الإنتاج
description: يوضح هذا الموضوع كيفيه تكامل الوحدة النمطية لإداره الإنتاج في Microsoft Dynamics 365 Supply Chain Management مع Dynamics 365 Guides.
author: cabeln
manager: tfehr
ms.date: 09/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkGuidesManufacturing
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 61943
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: cabeln
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 14645f592275d07a6b633146bb6da35b89c1bf77
ms.sourcegitcommit: 6d2fc497c8a7f49c48e7662995e27b5f8cc10296
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/14/2020
ms.locfileid: "4000968"
---
# <a name="provide-mixed-reality-guides-for-workers-in-production"></a>توفير دلائل الحقيقة المختلطة للعمال العاملين في الإنتاج

سيستفيد العاملون في عمليات الإنتاج من الإرشادات ذات الصلة التي يتم توفيرها في الوقت المناسب في سياق عملهم. يتم تطبيق *الإرشادات* في العديد من مجالات العمل، بما في ذلك: التجميع والخدمة والعمليات والشهادات والأمان. عبر كافة وظائف الاعمال الاساسيه هذه، يمكن ان تساعد إرشادات التدريب الحالية علي تمكين العاملين من تحقيق المزيد والعمل بشكل أفضل.

## <a name="introduction"></a>مقدمة

يمكنك توفير الإرشادات بطرق مختلفه. أحد الانظمه الفعالة يستخدم [Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/).

Dynamics 365 Guides من الممكن ان يساعد في زيادة الموظفين مع التعلم التبادلي. يمكنك تحديد العمليات القياسية بالإرشادات خطوه بخطوه التي ترشد الموظفين إلى الادوات والأجزاء التي تحتاجها وتعرض على الموظفين كيفيه استخدام هذه الادوات في مواقف العمل الفعلية.

يمكنك إرفاق خطوط إرشاد لجوانب متعددة من التحكم في الإنتاج بما في ذلك:

- [الموارد](#resources)
- [مجموعات الموارد](#resource-groups)
- [المنتجات الصادرة](#released-products)
- [التركيبات](#formulas)
- [إصدارات التركيبة](#formula-versions)
- [قائمة مكونات الصنف (BOMs)](#bom)
- [إصدارات BOM](#bom-versions)
- [المسارات](#routes)
- [إصدارات المسارات](#route-versions)
- [‏‏علاقات عمليات المسار](#route-operation-relations)

> [!NOTE]
> يمكنك أيضا إرفاق الدلائل باداره الأصول. لمزيد من المعلومات حول هذا الخيار، راجع [دمج Dynamics 365 Supply Chain Management (إدارة الأصول) مع Dynamics 365 Guides](../asset-management/asset-management-guides-integration.md).

عندما يقوم عامل البند الأول باختيار وظيفة في حاله العمل من خلال Supply Chain Management، يمكن للعامل رؤية [الدلائل ذات الصلة](#logic) على بطاقة الوظيفة. عندما يختار العامل دليلا معينا، يتم عرض شفره QR لذلك الدليل علي الشاشة. ثم يستخدم العامل HoloLens الخاص بهم لمسح شفره الاستجابة السريعة، والتي تعرض الدلائل وتظهر الإرشادات المطلوبة.

تصف الأقسام الفرعية التالية قليل من السيناريوهات المحددة حيث يمكن للشركات عبر الصناعات الاطلاع علي أكبر قيمه عند استخدام الدلائل لتقديم الإرشادات الخاصة بالتصنيع.

### <a name="assembly"></a>التجميع

![استخدام الدلائل في مهام التجميع](media/instruction-guides-hero-assembly.png "استخدام الدلائل في مهام الخدمة")

الإرشادات في عمليات التجميع تظهر العمال الادوات والأجزاء التي تحتاجها وكيفيه استخدامها في مواقف العمل الحقيقي.

ويمكن لمديري الإنتاج إنشاء الدئلال وتعيينها، علي سبيل المثال، بالنسبة [لمسارات الإنتاج ](routes-operations.md)أو [علاقات العمليات](routes-operations.md#operation-relations) أو [ قائمة مكونات الصنف](bill-of-material-bom.md). سيقوم العاملون بالعثور علي الإرشادات المناسبة حول خبره العملية الخاصة بحاله العمل.

### <a name="service"></a>الخدمة

![استخدام الدلائل في مهام الخدمة](media/instruction-guides-hero-service.png "استخدام الدلائل في مهام الخدمة")

تجهيز الفنيين الذين لهم تعليمات ارشاديه في موقع الوظيفة، مما يؤدي إلى إزاله الحاجة إلى جدوله زيارات اضافيه.

يمكن لمديري الخدمة تعيين الدلائل، علي سبيل المثال، [لمنتجات ](../../commerce/product.md)محدده تقودها من خلال إجراءات تقييم الجودة.

### <a name="quality"></a>الكمية

![استخدام الدلائل في مهام ضمان الجودة](media/instruction-guides-hero-quality.png "استخدام الدلائل في مهام ضمان الجودة")

تقوم بتمهيد العمليات الجديدة والتاكد من زيادة التناسق عن طريق تحويل معرفة الموظف إلى أداه قابلة للتكرار.

يمكن لمديري ضمان الجودة تعيين خطوط إرشاد، علي سبيل المثال، [لمنتجات ](../../commerce/product.md)محدده تقودها من خلال إجراءات تقييم الجودة.

### <a name="certifications"></a>الشهادات

![استخدام الدلائل للمهام المتعلقة بالشهادات](media/instruction-guides-hero-certification.png "استخدام الدلائل للمهام المتعلقة بالشهادات")

تاكد من ان كل موظف يفي بالمعايير العالية بسرعة وذلك من خلال تحديد من يحتاج إلى المساعدة و أين.

### <a name="safety"></a>أمان

![استخدام الدلائل في تعليمات أمان العمل](media/instruction-guides-hero-safety.png "استخدام الدلائل في تعليمات أمان العمل")

توفير الإرشادات التي تقود الإجراءات الخطيرة فعليا قبل المحاولة في البيئة الفعلية. من خلال منهج الحقيقة المختلطة، يمكن للعاملين تجربه إجراءات خطيره فعليا.

ويمكن لمديري الإنتاج تقديم إرشادات معالجه مخصصه لمعالجه المواد الخطرة أو لإجراءات معالجه دقيقة عن طريق تعيين الإرشادات إلى [عناصر ](../../commerce/product.md)المنتجات [والمسارات ](routes-operations.md)[والعمليات](routes-operations.md#operation-relations).

## <a name="get-started-with-instructions-and-guides"></a>الشروع في العمل بالإرشادات والدلائل

لتمكين الإرشادات في عمليات الإنتاج، توفر Supply Chain Management تكاملا خارج الصندوق مع Dynamics 365 Guides. يتطلب مثيل تطبيق Guides المرخص والمثبت لبناء وصيانة وتعيين إرشادات الحقيقة المختلطة لأصول الإنتاج والعمل.

### <a name="prerequisites"></a>المتطلبات الأساسية

لاستخدام هذه الميزة، يجب ان يتضمن النظام ما يلي:

- الإصدار 10.0.15 من Dynamics 365 Supply Chain Management أو إصدار لاحق
- [قم بتشغيل الكتابة المزدوجة](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write) لتطبيقات Supply Chain Management apps.
- الإصدار [Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) 400.0.1.48 إصدار لاحق

### <a name="turn-on-the-feature"></a>تشغيل الميزة

لجعل الميزة متوفرة علي النظام، يجب تمكين مفاتيح التكوين الخاصة بها. وتحتاج فقط للقيام بذلك مره واحده. للقيام بذلك، يجب علي المسؤول القيام بما يلي:

1. وضع النظام في وضع الصيانة كما هو موضح في [وضع الصيانة](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. انتقل إلى **إدارة النظام \> الإعداد \> تكوين الترخيص**.
1. قم بتوسيع مقطع **الحقيقة المختلطة** ثم حدد خانه الاختيار **دليل الحقيقة المختلطة**.
1. قم بتوسيع مقطع **إدارة الإنتاج** ، ثم حدد خانة الاختيار **إرشادات الإنتاج**.
1. إيقاف تشغيل وضع الصيانة كما هو موضح في [وضع الصيانة](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
  
## <a name="configure-how-guides-appear-on-the-shop-floor"></a>تكوين كيفيه ظهور الدلائل في صالة الإنتاج

لتكوين طريقه ظهور الدلائل في صالة الإنتاج، انتقل إلى **الحقيقة المختلطة \>Dynamics 365 Guides\>تكوين تكامل الدلائل**.

![تكوين تكامل الدليل للتصنيع](media/instruction-guides-configure-integration.png "تكوين تكامل الدليل للتصنيع")

قم بتعيين الحقول التالية:

- المجال الفرعي لـ **Common Data Service** - يجب أن يعرض هذا الحقل قيمة بالفعل. يحتوي هذا الحقل علي المجال الفرعي لبيئة Common Data Service حيث قمت بإنشاء الدلائل. المجال الفرعي هو الجزء الأول من عنوان URL ويسمي عاده باسم مؤسستك. علي سبيل المثال، إذا كان عنوان URL لـ Common Data Service هو "contoso.crm4.dynamics.com"، فيجب عليك إدخال *contoso* هنا. تستخدم هذه القيمة لإنشاء عناوين الإرشادات الخاصة بك وسيتم ترميزها في رموز QR.
- **حجم كود QR** - تعيين حجم كود QR المقدم. نوصي باختيار الحجم الذي سيملا معظم شاشه العرض، ولكن ليس المزيد. وعاده ما تكون *15* قيمه جيده.
- **مستوى تصحيح الخطأ لكود QR** - تعيين مستوى تفاصيل كود QR. مستوى تفاصيل أعلى تساعد في زيادة موثوقيه الكود، ولكن يجب ان يكون **حجم كود QR الخاص بك** كبيرا بما فيه الكفاية لدعم مستوي التفاصيل المطلوب من قبل مستوي التصحيح المحدد.


> [!TIP]
> - تحتاج احجام أكواد QR الكبيرة جدا بالنسبة لشاشه العرض وقتا أطول ليتم عرضها ثم يتم قياسها لتلائم الشاشة الخاصة بك. ولا توفر هذه الخيارات بعض المزايا.
> - ان احجام أكواد QR الصغيرة جدا قد تقلل من قدرة HoloLens على قراءه الكود بشكل صحيح في بعض البيئات.
> - نوصي باختبار الإعدادات لكل جهاز من الاجهزه التي ستقوم بعرض أكواد QR لمستخدمي HoloLens. اختر الإعدادات التي توفر امكانيه القراءة الكافية في بيئة صالة الإنتاج الخاصة بك.  

## <a name="get-an-overview-of-all-guide-assignments"></a>الحصول علي نظره عامه علي كافة تعيينات الدليل

استخدم الصفحة **كافة الادله** للاطلاع علي قائمه بكافة الادله المتوفرة في مؤسستك وكافة التعيينات لعمليات الإنتاج وموارده. لفتحه، انتقل إلى **الحقيقة المختلطة\>الأدلة \>كافة الادله**. تظهر القائمة في الأعلى كافة الدلائل المتوفرة ويمكنك استخدام الحقل هنا لتصفيه القائمة. تعرض القائمة الموجودة في الأسفل كافة تعيينات الدليل وتوفر شريط أدوات لإدارتها.

![إداره الأدلة](media/instruction-guides-allguides.png "إداره الأدلة")

تصف الأقسام التالية أنواع الكائنات التي يمكنك تعيين أدلة لها. يوفر كل دليل معين إرشادات يتم إرفاقها تلقائيا بوظائف الإنتاج المرتبطة وستكون متوفرة في حاله العمل.

## <a name="associate-a-guide-to-a-resource"></a><a name="resources"></a>اقران دليل بمورد

إضافه دليل إلى [مورد](operations-resources.md) لتقديم الدليل في سياق وظائف الإنتاج ذات الصلة.

### <a name="typical-scenario-using-resources"></a>سيناريوهات نموذجية باستخدام الموارد

علي سبيل المثال، يمكنك إرفاق دليل بأمان الجهاز العام أو إرشادات المعالجة إلى مورد من النوع جهاز. بعد ذلك، سيتوفر الدليل علي كل وظيفة يتم تنفيذها علي الجهاز.

### <a name="add-a-guide-to-a-resource"></a>إضافة دليل إلى مورد

لإضافة دليل إلى مورد:

1. الانتقال إلى **التحكم بالإنتاج \> الإعداد \> الموارد \> الموارد**.
1. من جزء القائمة، حدد المورد الذي ترغب في تعيين دليل اليه.
1. قم بتوسيع علامة التبويب السريعة **الادله المرتبطة**.
1. حدد **إضافه** من شريط الادوات **الادله المرتبطة**. تتم إضافة سطر جديد إلى الشبكة.
1. بالنسبة للسطر الجديد، استخدم القائمة المنسدلة في العمود **الاسم** لاختيار الدليل الذي تريد تعيينه. إذا كان لديك عدد كبير من الادله، فيمكنك تصفيه القائمة للبحث عن القائمة التي تبحث عنها.
    ![إداره الأدلة](media/instruction-guides-allguides.png "إداره الأدلة")

## <a name="associate-a-guide-to-a-resource-group"></a><a name="resource-groups"></a>اقران دليل بمجموعة موارد

يمكنك أضافه دليل إلى [مجموعات الموارد](tasks/define-discrete-manufacturing-resource-group.md)، إذا كنت تستخدمها لأداره مجموعات الاجهزه أو خطوط الإنتاج أو خلايا العمل.

### <a name="typical-scenarios-using-resource-groups"></a>سيناريوهات نموذجية باستخدام مجموعات الموارد

**المثال رقم 1:** لقد قمت بتحديد مجموعه موارد لعده أجهزه من نفس الموديل. بدلا من تعيين دليل إرشادات المعالجة ذات الصلة لموديل الجهاز لكل مورد ذي صله، يمكنك بدلا من ذلك تعيين الدليل إلى مجموعه الموارد التي تعكس موديل الجهاز هذا.

**المثال 2:** لقد قمت بتحديد مجموعه موارد لخليه عمل تحتوي علي أجهزه مختلفه ولديك دليل يوفر إرشادات عامه حول كيفيه الحفاظ علي خليه العمل. ينطبق الدليل علي اي نشاط إنتاج في خليه العمل هذه.

### <a name="add-a-guide-to-a-resource-group"></a>إضافة دليل إلى مجموعة موارد

لإضافة دليل إلى مجموعة موارد:

1. الانتقال إلى **التحكم بالإنتاج \> الإعداد \> الموارد \> مجموعات الموارد**.
1. من جزء القائمة، حدد مجموعة الموارد التي ترغب في تعيين دليل اليها.
1. قم بتوسيع علامة التبويب السريعة **الادله المرتبطة**.
1. حدد **إضافه** من شريط الادوات **الادله المرتبطة**. تتم إضافة سطر جديد إلى الشبكة.
1. بالنسبة للسطر الجديد، استخدم القائمة المنسدلة في العمود **الاسم** لاختيار الدليل الذي تريد تعيينه. إذا كان لديك عدد كبير من الادله، فيمكنك تصفيه القائمة للبحث عن القائمة التي تبحث عنها.
    ![إضافة دليل إلى مجموعة موارد](media/instruction-guides-resourcegroup.png "إضافة دليل إلى مجموعة موارد")

## <a name="associate-a-guide-to-a-released-product"></a><a name="released-products"></a>اقران دليل بمنتج مطروح

يمكنك إضافه دليل إلى اي [منتج تم إصداره](../pim/tasks/create-released-product-single-company.md).

### <a name="typical-scenario-using-released-products"></a>سيناريو نموذجي باستخدام المنتجات التي تم إصدارها

تساعد دلائل مستوى المنتج عمال صالة الإنتاج بالمعلومات المتعلقة بتشغيل أو معالجه منتج أو صنف تم إصداره بعينه.

### <a name="add-a-guide-to-a-released-product"></a>إضافة دليل إلى منتج تم إصداره

لإضافة دليل إلى منتج تم إصداره:

1. انتقل إلى **إدارة معلومات المنتج‬ \> المنتجات \> المنتجات التي تم إصدارها**.
1. افتح المنتج الذي ترغب في تعيين دليل اليه.
1. في جزء الاجراء ، افتح علامة التبويب **المهندس** ومن المجموعة **عرض** ، حدد **الدلائل المقترنة**.
1. تفتح صفحه **الادله** المرتبطة لمنتجك المحدد.
1. حدد **إضافة** في جزء الإجراءات لإضافة صف جديد إلى الشبكة. 
1. بالنسبة للسطر الجديد، استخدم القائمة المنسدلة في العمود **الاسم** لاختيار الدليل الذي تريد تعيينه.
    ![إضافة دليل إلى منتج تم إصداره:](media/instruction-guides-ReleasedProduct-AddGuides.png "إضافة دليل إلى منتج تم إصداره")

## <a name="associate-a-guide-to-a-formula"></a><a name="formulas"></a>اقران دليل بمعادلة

يمكنك إضافه دليل إلى اي [معادلة](bill-of-material-bom.md#formulas-co-products-and-by-products).

### <a name="typical-scenario-using-formulas"></a>سيناريوهات نموذجية باستخدام المعادلات
  
توفر الدلائل على مستوى المعادلات لعمال صالة الإنتاج إرشادات تعامل موجهة في سياق المعادلة أو الوصفة. يمكن أيضا تعيين الادله إلى إصدارات معادلة.

> [!NOTE]
> يمكنك تعيين الإرشاد المناسب لعمليات الإنتاج استنادا إلى المعادلة إلى المسار أو إصدار المسار أو علاقات مسار العمليات.  

> لا يمكن إرفاق الادله حاليا بسطور المعادلة الفردية.

### <a name="add-a-guide-to-a-formula"></a>إضافة دليل إلى معادلة

لإضافة دليل إلى معادلة:

1. انتقل إلى **إدارة معلومات المنتج \> قوائم مكونات الصنف والمعادلات‬ \> المعادلات**.
1. افتح المعادلة التي ترغب في تعيين دليل اليه.
1. افتح علامة التبويب **الراس** أعلى علامة التبويب السريعة العلوية.
1. قم بتوسيع علامة التبويب السريعة **الادله المرتبطة**.
1. حدد **إضافه** من شريط الادوات **الادله المرتبطة**. تتم إضافة سطر جديد إلى الشبكة.
1. بالنسبة للسطر الجديد، استخدم القائمة المنسدلة في العمود **الاسم** لاختيار الدليل الذي تريد تعيينه.
    ![إضافة دليل إلى معادلة:](media/instruction-guides-Formula.png "إضافة دليل إلى معادلة")

## <a name="associate-a-guide-to-a-formula-version"></a><a name="formula-versions"></a>اقران دليل بإصدار معادلة

يمكنك إضافه دليل إلى اي [إصدار معادلة](bill-of-material-bom.md#bom-and-formula-versions).

### <a name="typical-scenario-using-formula-versions"></a>سيناريوهات نموذجية باستخدام إصدارات المعادلات

توفر الادله المرفقة بالإصدار الفردي من المعادلة لعمال صالة الإنتاج تعليمات إرشادية خلال إنتاج هذا الإصدار من وصفة المعادلة.

> [!TIP]
> يمكنك تعيين الإرشاد المناسب لعمليات الإنتاج استنادا إلى إصدار المعادلة إلى مسار أو إصدار المسار أو علاقات عملية المسار.  

> [!NOTE]
> لا يمكن إرفاق الادله حاليا بسطور المعادلة الفردية.

### <a name="add-a-guide-to-a-formula-version"></a>إضافة دليل إلى إصدار معادلة

لإضافة دليل إلى إصدار معادلة:

1. انتقل إلى **إدارة معلومات المنتج \> قوائم مكونات الصنف والمعادلات‬ \> المعادلات**.
1. افتح المعادلة التي تتضمن إصدارا تريد تعيين دليل له.
1. افتح علامة التبويب **الراس** أعلى علامة التبويب السريعة العلوية.
1. في علامة التبويب السريعة **إصدارات المعادلة** ، حدد الإصدار الذي ترغب في تعيين دليل اليه.
1. في شريط الادوات **إصدارات المعادلة** ، حدد **الأدلة المقترنة**.
    ![فتح الادله المقترنة بإصدار معادلة محدد](media/instruction-guides-FormulaVersion.png "فتح الادله المقترنة بإصدار معادلة محدد")
1. تفتح صفحه **الادله المقترنة** لإصدار المعادلة الخاص بك.
1. حدد **إضافة** في جزء الإجراءات لإضافة صف جديد إلى الشبكة. 
1. بالنسبة للسطر الجديد، استخدم القائمة المنسدلة في العمود **الاسم** لاختيار الدليل الذي تريد تعيينه.
    ![إضافة دليل إلى معادلة](media/instruction-guides-FormulaVersionAddGuide.png "إضافة دليل إلى معادلة")

## <a name="associate-a-guide-to-a-bill-of-materials"></a><a name="bom"></a>إقران دليل بقائمه مكونات الصنف

يمكنك أضافه دليل إلى أيه [قائمة مكونات صنف](bill-of-material-bom.md) (BOM).

### <a name="typical-scenario-using-bills-of-materials"></a>سيناريو نموذجي باستخدام قائمه مكونات الصنف

توفر الادله المرتبطة بقائمة مكونات الصنف لعمال صالة الإنتاج إرشادات حول كيفيه تجهيز المواد من قائمة BOM ومعالجتها. يمكن أيضا تعيين الادله إلى إصدارات قائمة BOM.

> [!NOTE]
> لا يمكن إرفاق الادله حاليا بسطور BOM.

### <a name="add-a-guide-to-a-bill-of-materials"></a>إضافة دليل إلى قائمه مكونات الصنف

لإضافة دليل إلى قائمه مكونات الصنف:

1. انتقل إلى **إدارة معلومات الإنتاج \> قائمة مكونات الصنف والمعادلات \> قوائم مكونات الصنف**.
1. افتح قائمة مكونات الصنف التي ترغب في تعيين دليل اليها.
1. افتح علامة التبويب **الراس** أعلى علامة التبويب السريعة العلوية.
1. قم بتوسيع علامة التبويب السريعة **الادله المرتبطة**.
1. حدد **إضافه** من شريط الادوات **الادله المرتبطة**. تتم إضافة سطر جديد إلى الشبكة.
1. بالنسبة للسطر الجديد، استخدم القائمة المنسدلة في العمود **الاسم** لاختيار الدليل الذي تريد تعيينه.
    ![إضافة دليل إلى قائمة BOM](media/instruction-guides-BOM.png "إضافة دليل إلى قائمة BOM")

## <a name="associate-a-guide-to-a-bill-of-materials-version"></a><a name="bom-versions"></a>إقران دليل بإصدار قائمه مكونات الصنف

يمكنك أضافه دليل إلى أي [إصدار قائمة مكونات صنف](bill-of-material-bom.md#bom-and-formula-versions) (BOM).

### <a name="typical-scenario-using-bill-of-materials-versions"></a>سيناريو نموذجي باستخدام إصدارات قائمه مكونات الصنف

توفر الادله المرتبطة بإصدار قائمة مكونات الصنف الفرديه للعاملين في صالة الإنتاج إرشادات توضح كيفيه تجهيز ومعالجه المواد لإصدار قائمة مكونات الصنف تختلف عن قائمة مكونات الصنف العامة أو الإصدارات الأخرى الخاصة بها.

> [!NOTE]
> لا يمكن إرفاق الادله حاليا بسطور BOM.

### <a name="add-a-guide-to-a-bill-of-materials-version"></a>إضافة دليل إلى إصدار قائمه مكونات الصنف

لإضافة دليل إلى إصدار قائمه مكونات الصنف:

1. انتقل إلى **إدارة معلومات الإنتاج \> قائمة مكونات الصنف والمعادلات \> قوائم مكونات الصنف**.
1. افتح قائمة BOM التي تتضمن إصدارا تريد تعيين دليل له.
1. افتح علامة التبويب **الراس** أعلى علامة التبويب السريعة العلوية.
1. في علامة التبويب السريعة **إصدارات BOM** ، حدد الإصدار الذي ترغب في تعيين دليل اليه.
1. في شريط الادوات **إصدارات BOM** ، حدد **الأدلة المقترنة**.
    ![فتح الادله المقترنة بإصدار BOM محدد](media/instruction-guides-BOMVersion.png "فتح الادله المقترنة بإصدار BOM محدد")
1. تفتح صفحه **الادله المقترنة** لإصدار BOM الخاص بك.
1. حدد **إضافة** في جزء الإجراءات لإضافة صف جديد إلى الشبكة.
1. بالنسبة للسطر الجديد، استخدم القائمة المنسدلة في العمود **الاسم** لاختيار الدليل الذي تريد تعيينه.
    ![إضافة دليل إلى إصدار BOM](media/instruction-guides-BOMVersionAddGuide.png "إضافة دليل إلى إصدار BOM")

## <a name="associate-a-guide-to-a-route"></a><a name="routes"></a>اقران دليل بمسار

يمكنك إضافه دليل إلى اي [مسار](routes-operations.md).

### <a name="typical-scenario-using-routes"></a>سيناريوهات نموذجية باستخدام المسارات

وتستخدم المسارات بشكل نموذجي لتحديد كيفيه إنتاج منتج معين تم إصداره علي أساس قائمة مكونات الصنف أو إصدار قائمة مكونات الصنف ومع مجموعه من الموارد أو مجموعات الموارد.

قم بتعيين دليل لأحد المسارات لتوفير إرشادات خطوه بخطوه لعمليه الإنتاج المرتبطة.

### <a name="add-a-guide-to-a-route"></a>إضافة دليل إلى مسار

لإضافة دليل إلى مسار:

1. الانتقال إلى **التحكم في الإنتاج \>كافة المسارات**.
1. افتح المسار الذي ترغب في تعيين دليل اليه.
1. قم بتوسيع علامة التبويب السريعة **الادله المرتبطة**.
1. حدد **إضافه** من شريط الادوات **الادله المرتبطة**. تتم إضافة سطر جديد إلى الشبكة.
1. بالنسبة للسطر الجديد، استخدم القائمة المنسدلة في العمود **الاسم** لاختيار الدليل الذي تريد تعيينه.
    ![إضافة دليل إلى مسار](media/instruction-guides-Route.png "إضافة دليل إلى مسار")

## <a name="associate-a-guide-to-a-route-version"></a><a name="route-versions"></a>اقران دليل بإصدار مسار

يمكنك إضافه دليل إلى اي [إصدار مسار](routes-operations.md#route-versions).

### <a name="typical-scenario-using-route-versions"></a>سيناريوهات نموذجية باستخدام إصدارات المسارات

وعاده ما يتم استخدام إصدارات المسارات لتحديد متغيرات عمليات الإنتاج وفقا لمسار موجود. يمكنك تعيين أدله مختلفه لكل إصدار مسار.

### <a name="add-a-guide-to-a-route-version"></a>إضافة دليل إلى إصدار مسار

لإضافة دليل إلى إصدار مسار:

1. الانتقال إلى **التحكم في الإنتاج \>كافة المسارات**.
1. افتح المسار الذي ترغب في تعيين دليل اليه.
1. في علامة التبويب السريعة **الإصدارات** ، حدد الإصدار الذي ترغب في تعيين دليل اليه.
1. في شريط الادوات **الإصدارات** ، حدد **الأدلة المقترنة**.
    ![فتح الادله المقترنة بإصدار مسار محدد](media/instruction-guides-RouteVersion.png "فتح الادله المقترنة بإصدار مسار محدد")
1. تفتح صفحه **الادله المقترنة** لإصدار BOM الخاص بك.
1. حدد **إضافة** في جزء الإجراءات لإضافة صف جديد إلى الشبكة.
1. بالنسبة للسطر الجديد، استخدم القائمة المنسدلة في العمود **الاسم** لاختيار الدليل الذي تريد تعيينه.
    ![إضافة دليل إلى إصدار مسار](media/instruction-guides-RouteVersionAddGuide.png "إضافة دليل إلى إصدار مسار")

## <a name="associate-a-guide-to-a-route-operation-relation"></a><a name="route-operation-relations"></a>اقران دليل بعلاقة عملية مسار

يمكنك إضافه دليل إلى اي [علاقة عملية مسار](routes-operations.md#operation-relations).

### <a name="typical-scenario-using-route-operation-relations"></a>سيناريو نموذجي باستخدام علاقات عملية المسار

تعد علاقات العملية الطريقة الأكثر تحديدا لأضافه إرشادات لعمليه المنتج والعمليات المرتبطة بها. يمكنك تحديد الإرشادات لكل عمليه في المسار وتحديد دليل مختلف لأي نوع من سياق العلاقة المحدد للتوجيه، مثل الأصناف المحددة والتكوينات والمزيد. كما يمكنك تحديد المراحل الموجودة في العملية التي تنطبق عليها الإرشادات (مثل الاعداد أو الإدراج في قائمة الانتظار أو العمليات أو النقل).

> [!NOTE]
> إذا قمت بتحديد الادله للعديد من علاقات العمليات الخاصة بأحد المسارات، فمن بين تلك الادله، يتم عرض الدليل فقط من العلاقة الأكثر تحديدا في صالة الإنتاج للوظيفة التي تم إنشاؤها.

### <a name="add-a-guide-to-a-route-operation-relation"></a>إضافة دليل بعلاقة عملية مسار

لإضافة دليل بعلاقة عملية مسار:

1. الانتقال إلى **التحكم في الإنتاج \>كافة المسارات**.
1. افتح المسار الذي ترغب في تعيين دليل اليه.
1. في جزء الاجراء، افتح علامة التبويب **المسار** ومن المجموعة **صيانة** ، حدد **تفاصيل المسار**.
1. تفتح صفحه **تفاصيل المسار** للمسار المحدد الخاص بك.
1. في الشبكة العليا، حدد العملية التي ترغب في توفير إرشادات لها.
1. في الشبكة السفلي، حدد علاقة محدده (أو العلاقة العامة **الكل** ).
    ![تحديد عمليه وبعد ذلك علاقة](media/instruction-guides-RouteOperationRelation.png "تحديد عمليه وبعد ذلك علاقة")
1. فوق الشبكة السفلى، افتح علامة التبويب **الدلائل المقترنة**. ![علامة التبويب الدلائل المقترنة](media/instruction-guides-RouteOperationRelation-AddGuide.png "علامة التبويب الدلائل المقترنة")
1. حدد **أضافه** من شريط الادوات الموجود اعلي الشبكة السفلية لأضافه سطر جديد إلى الشبكة.
1. بالنسبة للصف الجديد، استخدم القائمة المنسدلة في العمود **الاسم** لاختيار الدليل الذي تريد تعيينه. في باقي الصف، حدد خانه الاختيار لكل سياق يجب ان يتوفر فيه الدليل المحدد.

> [!NOTE]
> يمكنك أضافه دليل واحد أو أكثر لكل مرحله من العملية.

## <a name="select-guides-from-the-shop-floor-execution-interface"></a>حدد الأدلة من واجهه تنفيذ صالة الإنتاج

عندما يقوم أحد العاملين بفتح قائمه الوظائف في واجهه تنفيذ صالة الإنتاج، تقوم Supply Chain Management بالبحث عن الدلائل ذات الصلة للوظائف المعروضة. استخدم زر **الأدلة** لعرض الادله ذات الصلة.

![زر الأدلة في واجهه تنفيذ صالة الإنتاج](media/instruction-guides-Shopfloor1.png "زر الأدلة في واجهه تنفيذ صالة الإنتاج")

ثم ضع في HoloLens وقم بالوصول إلى الدليل الخاص بواسطة الاطلاع على كود QR وتنشيط الدليل المعني.

![كود QR للوصول إلى الأدلة باستخدام HoloLens](media/instruction-guides-Shopfloor2.png "كود QR للوصول إلى الأدلة باستخدام HoloLens")

## <a name="resolving-the-logic-for-selecting-guides"></a><a name="logic"></a>حل المنطق لتحديد الأدلة

يمكنك أضافه أدله إلى بيانات الإنتاج التالية:

- [الموارد](#resources)
- [مجموعات الموارد](#resource-groups)
- [المنتجات الصادرة](#released-products)
- [التركيبات](#formulas)
- [إصدارات التركيبة](#formula-versions)
- [قائمة مكونات الصنف (BOMs)](#bom)
- [إصدارات BOM](#bom-versions)
- [المسارات](#routes)
- [إصدارات المسارات](#route-versions)
- [‏‏علاقات عمليات المسار](#route-operation-relations)

عندما تقوم Supply Chain Management بإنشاء وظائف لصاله الإنتاج، فانها ستقوم بتجميع الدلائل ذات الصلة من تلك المصادر. دوّن القواعد الهامه التالية.

- إذا قمت بإرفاق إصدار قائمة مكونات الصنف أو إصدار التركيبة بمسار أو أمر إنتاج، سيتم عرض إيه دلائل مرفقه بهذا الإصدار، وكذلك الادله المرتبطة بقائمة مكونات الصنف الاصليه أو المعادلة الخاصة بهذا الإصدار، في الوظيفة.
- إذا قمت بإرفاق إصدار مسار بأمر إنتاج، سيتم عرض إيه دلائل مرفقه بهذا الإصدار، وكذلك الادله المرتبطة بالمسار الاصلي لهذا الإصدار، في الوظيفة.
- إذا قمت بتحديد العديد من علاقات مسارات العمليات التي تتضمن *جميع* دلائل العلاقة والتعيين، سيتم عرض الادله التي من أكثر علاقة محدده للوظيفة.  

![مخطط حول حل الدلائل ذات الصلة](media/instruction-guides-Resolve.png "مخطط حول حل الدلائل ذات الصلة")