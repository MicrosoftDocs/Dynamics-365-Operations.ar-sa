---
title: إنشاء تدرج هرمي لمنتج جديد
description: يوضح هذا المقال كيفية إنشاء تدرج هرمي لمنتج جديد في Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 54a29381bb9231766d76b653904339d4bd60c257
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270117"
---
# <a name="create-a-new-product-hierarchy"></a>إنشاء تدرج هرمي لمنتج جديد


[!include [banner](includes/banner.md)]

يوضح هذا المقال كيفية إنشاء تدرج هرمي لمنتج جديد في Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>نظرة عامة

يدعم Dynamics 365 Commerce عدة قنوات بيع بالتجزئة. وتتضمن قنوات البيع بالتجزئة هذه المتاجر على إنترنت، ومراكز الاتصال، ومتاجر البيع بالتجزئة (تعرف أيضًا بالمتاجر التقليدية). يمكن أن يكون لكل قناة متجر للبيع بالتجزئة طرق الدفع ومجموعات الأسعار وسجلات نقطة البيع (POS) وحسابات الإيرادات والمصروفات وفريق العمل الخاص بها. ويجب إعداد كل هذه العناصر قبل إمكانية إنشاء قناة لمتجر البيع بالتجزئة. 

يتم استخدام التدرج الهرمي لمنتج تجاري لتحديد التدرج الهرمي الشامل للمنتجات لمؤسستك. ويمكنك استخدام التدرج الهرمي لمنتج تجاري للترويج للبضائع والتسعير والعروض وإعداد التقارير وتخطيط الفرز. يمكن تعيين تدرج هرمي واحد للمنتجات التجارية لكل مؤسسة.

## <a name="create-and-configure-a-product-hierarchy"></a>إنشاء تدرج هرمي لمنتج وتكوينه

لإنشاء تدرج هرمي للمنتجات التجارية وتكوينه، اتبع الخطوات التالية.

1. في جزء التنقل، انتقل إلى **الوحدات النمطية \> البيع بالتجزئة والتجارة \> المنتجات والفئات \> التدرج الهرمي للمنتج التجاري**.
1. في حالة عدم وجود تدرج هرمي بعد، في **جزء الإجراء**، حدد **جديد** لإنشاء جذر التدرج الهرمي.
1. ضمن **عام**:
    1. في حقل **الاسم**، أدخل اسمًا.
    1. في مربع **الوصف**، أدخل وصفًا.
    1. في المربع **الاسم المألوف**، أدخل اسمًا مألوفًا.
    1. عيِّن الخيار **نشط** على القيمة **نعم**.

## <a name="add-hierarchy-nodes"></a>إضافة عقد التدرج الهرمي

لإضافة عقد التدرج الهرمي، اتبع هذه الخطوات.

1. في جزء الإجراءات، حدد **تحرير التدرج الهرمي للفئات**.
1. حدد العقدة الأصل التي ترغب في إضافة عقدة جديدة إليها، ثم حدد **عقدة فئة جديدة**.
1. في القسم **عام** أدخل **اسم** و **وصف** و **اسم مألوف** و **كلمات أساسية**.
1. ضمن **عام**:
    1. في حقل **الاسم**، أدخل اسمًا.
    1. في مربع **الوصف**، أدخل وصفًا.
    1. في المربع **الاسم المألوف**، أدخل اسمًا مألوفًا.
    1. في المربع **الكلمات الأساسية**، أدخل الكلمات الأساسية ذات الصلة.
    1. في المربع **ترتيب العرض**، أدخل رقمًا لترتيب العرض (اختياري).
1. في جزء الإجراءات، حدد **حفظ**.
1. كرر الخطوات المذكورة أعلاه لإضافة عقد إضافية.

توضح الصورة التالية إنشاء عقدة تدرج هرمي لمنتج جديد.

![إنشاء تدرج هرمي للمنتج.](media/create-product-hierarchy.png)

## <a name="other-settings"></a>إعدادات أخرى

يمكن أيضًا تعيين مجموعات سمات الفئة لكل مجموعة كما هو مطلوب.  

## <a name="additional-resources"></a>الموارد الإضافية

[التدرجات الهرمية لـ ‎commerce](retail-hierarchies.md)

[إدارة المنتجات وفئات المنتجات](category-management-product-creation.md)

[تغيير ترتيب الفرز لكيانات ترويج البضائع](custom-order-categories-nav-retail-prod-hierarchy.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
