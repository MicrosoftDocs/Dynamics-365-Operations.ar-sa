---
title: التخطيط الرئيسي مع اتفاقيات الشراء التجارية
description: يصف هذا الموضوع كيف يؤدي تحسين التخطيط إلى العثور على المورّد و/أو وقت الإنتاج لأمر مخطط، استنادًا إلى أفضل سعر أو وقت إنتاج يمكن العثور عليه في اتفاقيات الشراء التجارية.
author: ChristianRytt
manager: tfehr
ms.date: 06/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: b302c5ace34a11a53a98c733b59633a11a463bfa
ms.sourcegitcommit: 3fa1e8583003a90ba486f757c3826b139e1b3f73
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/02/2020
ms.locfileid: "3421521"
---
# <a name="master-planning-with-purchase-trade-agreements"></a>التخطيط الرئيسي مع اتفاقيات الشراء التجارية

[!include [banner](../../includes/banner.md)]

يصف هذا الموضوع كيف يؤدي تحسين التخطيط إلى العثور على المورّد و/أو وقت الإنتاج لأمر مخطط، استنادًا إلى أفضل سعر أو وقت إنتاج يمكن العثور عليه بين جميع اتفاقيات الشراء التجارية التي تم تحديدها لمنتج معين.

## <a name="turn-on-the-purchase-trade-agreements-for-planning-optimization-feature"></a>تشغيل ميزة اتفاقيات الشراء التجارية لتحسين التخطيط

قبل أن تتمكن من استخدام هذه الميزة، يجب تشغيلها في النظام. بإمكان المسؤولين استخدام مساحة عمل [إدارة الميزات](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها إذا كانت مطلوبة. هناك، يتم إدراج الميزة بالطريقة التالية:

- **الوحدة:** *التخطيط الرئيسي*
- **اسم الميزة:** *اتفاقيات الشراء التجارية لتحسين التخطيط*

## <a name="prepare-your-system-to-evaluate-purchase-trade-agreements-during-master-planning"></a>إعداد النظام لتقييم اتفاقيات الشراء التجارية أثناء التخطيط الرئيسي

اتبع الخطوات التالية لتكوين النظام لتطبيق ميزة تحسين التخطيط التي تقيّم اتفاقيات الشراء التجارية‬.

1. انتقل إلى **التخطيط الرئيسي \> إعداد \> محددات التخطيط الرئيسي**. في علامة التبويب **الأوامر المخططة**، في قسم **المورّد**، قم بتعيين القيم التالية:

    - **البحث عن الاتفاقيات التجارية** – عيّن هذا الخيار إلى **نعم** لتضمين اتفاقيات الشراء التجارية في التخطيط الرئيسي.
    - **معيار البحث** – حدد العامل الذي ترغب في تحديد أولويته لكل اتفاقيه شراء تجارية: **الحد الأدنى لوقت الإنتاج** أو **أقل سعر للوحدة**.

1. انتقل إلى **التدبير وتحديد الموارد \> إعداد \> الأسعار والخصومات \> تنشيط السعر/الخصم**، وتأكد من تعيين الخيار **المورّد** إلى **نعم**.
1. انتقل إلى **إدارة معلومات المنتج‬ \> إعداد \> مجموعات الأبعاد والمتغيرات \> مجموعات أبعاد التخزين**، ثم حدد مجموعه ابعاد تخزين تنطبق على المنتجات التي يجب على التخطيط الرئيسي تقييم اتفاقيات الشراء التجارية لها. تأكد من أن كل بُعد من أبعاد التخزين في هذه المجموعة لديه علامة اختيار في العمود **لأسعار الشراء‬**. كرر هذه الخطوة لكل مجموعة أبعاد تخزين أخرى ذات صلة.

## <a name="prepare-a-released-product-to-evaluate-purchase-trade-agreements-during-master-planning"></a>إعداد منتج صادر لتقييم اتفاقيات الشراء التجارية أثناء التخطيط الرئيسي

بعد ان يتم إعداد النظام كما ورد في القسم السابق، يجب اتباع الخطوات التالية للتأكد من إعداد كل منتج ترغب في استخدامه مع هذه الميزة بطريقة صحيحة.

1. انتقل إلى **إدارة معلومات المنتج \> المنتجات \> المنتجات الصادرة**، وافتح المنتج الهدف.
1. على علامة التبويب السريع **الشراء**، تأكد من عدم تعيين أي مورّد في حقل **المورّد**.
1. في جزء الإجراءات، على علامة التبويب **الخطة**، في مجموعة **التغطية‏‎**، حدد **تغطية الصنف** لفتح صفحة **تغطية الصنف** للمنتج المحدد. تحقق من الإعدادات التالية:

    - في علامة التبويب **عام**، يمكنك إعداد تجاوزات المورّد. إذا أردت أن تستخدم ميزة تحسين التخطيط اتفاقيات الشراء التجارية لتحديد مورّد، فيجب أن تمنع تجاوز المورّد عن طريق إلغاء تحديد خانة الاختيار **استخدام إعداد محدد**.
    - في علامة التبويب **وقت الإنتاج**، يمكن إعداد تجاوزات وقت الإنتاج. إذا أردت أن تستخدم ميزة تحسين التخطيط اتفاقيات الشراء التجارية لتحديد أوقات الإنتاج، فيجب أن تمنع تجاوز أوقات الإنتاج. قم بإلغاء تحديد خانة الاختيار لكل نوع وقت إنتاج تريد تحديده باستخدام اتفاقيات الشراء التجارية (**الشراء** و/أو **الإنتاج** و/أو **التحويل**).

1. أغلق صفحة **تغطية الصنف** للرجوع إلى صفحة التفاصيل الخاصة بالمنتج المحدد.
1. في جزء الإجراءات، على علامة تبويب **الخطة**، في مجموعة **التنبؤ**، حدد علامة التبويب **التنبؤ بالتوريد** لفتح صفحة **التنبؤ بالتوريد**. تأكد من أن أي صف يظهر هنا لديه قيمة في عمود **حساب المورّد**.
1. أغلق صفحة **التنبؤ بالتوريد** للرجوع إلى صفحة التفاصيل الخاصة بالمنتج المحدد.
1. في جزء الإجراءات، ضمن علامة التبويب **الشراء**، في مجموعة **‏‫الاتفاقيات التجارية**، حدد **عرض الاتفاقيات التجارية**. تأكد من أن جميع اتفاقيات الشراء التجارية ذات الصلة مدرجة. تأكد أيضًا من تعيين الخيار **تجاهل وقت الإنتاج** إلى **لا** لكل اتفاقية حيث تريد أن تستخدم ميزة تحسين التخطيط وقت الإنتاج المحدد لهذه الاتفاقية.
1. في جزء الإجراءات، على علامة تبويب **الخطة**، في مجموعة **إعدادات الأوامر‬‬‏‫‏‎**، حدد **إعدادات الأوامر الافتراضية** لفتح صفحة **إعدادات الأوامر الافتراضية** للمنتج المحدد. على علامة التبويب السريعة **أمر الشراء**، اعرض قيمة الحقل **وقت إنتاج المشتريات**. إذا لم يتم تحديد تجاوز وقت الإنتاج لتغطية الصنف، ستستخدم ميزة تحسين التخطيط هذه القيمة عندما تحدد الاتفاقيات التجارية حيث تم تعيين **تجاهل وقت الإنتاج** إلى **نعم**. وبالتالي، يجب ضبط هذه القيمة حسب الحاجة.
1. كرر هذا الإجراء لكل منتج ذي صلة.

> [!NOTE]
> يجب أن تتطابق العملة في بند اتفاقية الشراء التجارية مع عملة المورّد المحدد. سيتضمن التخطيط الرئيسي معلومات فقط من بنود اتفاقية الشراء التجارية حيث تتطابق العملة مع عملة المورّد.

## <a name="examples-of-how-planning-optimization-finds-vendor-and-lead-times"></a>أمثلة عن كيفية عثور ميزة تحسين التخطيط على المورّدين وأوقات الإنتاج.

يعرض الجدول التالي أمثلة تبيّن كيفية تأثير الإعدادات المتنوعة لمنتج صادر واتفاقيات الشراء التجارية التي تقترن به على القيم التي يتم العثور عليها لأمر الشراء المخطط الناتج. القيم بالتنسيق **الغامق** في العمودين إلى أقصى اليمين هي القيم المحددة بواسطة تحسين التخطيط. القيم بالتنسيق ***الغامق والمائل*** في الأعمدة الأخرى هي الإعدادات التي أنتجت القيم الناتجة لكل صف.

| المنتج الصادر: المورّد | إعدادات الأوامر الافتراضية: وقت الإنتاج | تغطية الصنف: تجاوز المورّد | تغطية الصنف: تجاوز وقت الإنتاج | الاتفاقية التجارية: المورّد | الاتفاقية التجارية: وقت الإنتاج | الاتفاقية التجارية: تجاهل وقت الإنتاج | المورّد الناتج | وقت الإنتاج الناتج |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ***US001*** | ***1*** | لا | لا | US003 | 3 | لا | **US001** | **1** |
| US001 | 1 | ***نعم‏‎: ‏US002*** | ***نعم‏‎‏: 2*** | US003 | 3 | لا | **US002** | **2** |
| *(فارغ)* | 1 | لا | لا | ***US003*** | ***3*** | لا | **US003** | **3** |
| *(فارغ)* | ***1*** | لا | لا | ***US003*** | 3 | ‏‏نعم | **US003** | **1** |
| *(فارغ)* | ***1*** | ***نعم‏‎: ‏US002*** | لا | US003 | 3 | لا | **US002** | **1** |
| *(فارغ)* | ***1*** | ***نعم‏‎: ‏US002*** | لا | US003 | 3 | لا | **US002** | **1** |
| *(فارغ)* | 1 | لا | نعم‏‎‏: 2 | ***US003*** | ***3*** | لا | **US003** | **3** |
| *(فارغ)* | 1 | لا | ***نعم‏‎‏: 2*** | ***US003*** | 3 | ‏‏نعم | **US003** | **2** |

## <a name="additional-resources"></a>الموارد الإضافية

[اتفاقيات الشراء](../../procurement/purchase-agreements.md)