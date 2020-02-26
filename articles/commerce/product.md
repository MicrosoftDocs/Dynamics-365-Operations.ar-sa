---
title: توصيات المنتجات على نقطة البيع‬
description: ‏‫يصف هذا الموضوع استخدام توصيات المنتج على جهاز نقطه البيع (POS).
author: bebeale
manager: AnnBe
ms.date: 10/01/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: af0273ca1553d5fb371a20b8c96fd9a101f34815
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021523"
---
# <a name="product-recommendations-on-pos"></a>توصيات المنتجات على نقطة البيع

[!include [banner](includes/banner.md)]

‏‫في أساسه، تُعد توصيات المنتج بمثابة أحد تطبيقات الاعمال التحويلية الذي يمتد عبر جميع مساحات البيع بالتجزئة لخلق تجارب اكتشاف منتج غنية وجذابة ومخصصة. لتطبيق هذه الميزة في نقطه البيع، اتبع الخطوات الخاصة [بكيفية إضافة توصيات إلى أجهزة نقطة البيع.](add-recommendations-control-pos-screen.md) 

لمزيد من المعلومات حول ميزات توصيات المنتجات، راجع [نظرة عامة على توصيات المنتجات.](../commerce/product-recommendations.md) 

## <a name="scenarios"></a>السيناريوهات

يتم تمكين توصيات المنتج لسيناريوهات نقطة البيع التالية. تتوافر في نقطة بيع المجموعة (POS) أو نقطة بيع حديثة (MPOS).

1. في صفحة **تفاصيل المنتجات**:

    - إذا قام شريك في المتجر بزيارة صفحة **تفاصيل المنتج** عند النظر في الحركات السابقة عبر القنوات المختلفة، فإن خدمة التوصيات تقترح بنود إضافية والتي من المرجح شرائها معًا.

    [![التوصيات في صفحة تفاصيل المنتج](./media/proddetails.png)](./media/proddetails.png)

2. في صفحة **الحركة**:

    - يقوم محرك التوصيات باقتراح الأصناف التي تستند إلى قائمة الأصناف بأكملها في السلة التي يتم شراؤها بشكل متكرر معًا.

    > [!NOTE]
    > لعرض التوصيات على صفحة **الحركة**، يحتاج تاجر التجزئة إلى تحديث تخطيط الشاشة في Dynamics 365 Commerce. يجب إسقاط عنصر تحكم **التوصيات** داخل صفحة **الحركة** .

    [![التوصيات في صفحة الحركة](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

## <a name="configure-commerce-to-enable-pos-recommendations"></a>تكوين Commerce لتمكين توصيات نقطة البيع

لإعداد توصيات المنتج‬، اتبع هذه الخطوات:

1. تأكد من تحديث الخدمة الخاصة بك **للإصدار 10.0.6.**
2. اتبع الإرشادات حول كيفية [تمكين توصيات المنتج](../commerce/enable-product-recommendations.md) لأعمالك.
3. اختياري: لعرض التوصيات على شاشة الحركة، انتقل إلى **تخطيط الشاشة**، واختر تخطيط الشاشة وابدأ تشغيل **مصمم تخطيط الشاشة**، ثم قم بإفلات عنصر تحكم **التوصيات** حيث تقتضي الحاجة.
4. انتقل إلى **معلمات Commerce**، وحدد **التعلم الآلي**، ثم حدد **نعم** ضمن **تمكين توصيات نقطة البيع**.
5. لمشاهدة التوصيات في نقطة البيع، قم بتشغيل وظيفة التكوين العمومي **1110**. لعكس التغييرات التي تم إجراؤها لمصم تخطيط شاشة نقطة البيع، قم بتشغيل وظيفة تكوين قناة **1070**.

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a>استكشاف الأخطاء وإصلاحها التي يكون لك فيها توصيات منتج مُمكنة بالفعل.

- انتقل إلى **معلمات Commerce‬** \> **قوائم التوصيات** \> **تعطيل توصيات المنتج** وقم بتشغيل **وظيفة التكوين العمومي \[9999\]**. 
- إذا قمت بإضافة **عناصر التحكم في التوصيات** إلى شاشة الحركة الخاصة بك باستخدام **مصمم تخطيط الشاشة**، الرجاء إزالتها أيضًا.
- إذا كانت لديك المزيد من الاستفسارات، وللحصول على المزيد من المعلومات، راجع [الاسئلة المتداولة حول توصيات المنتجات](../commerce/faq-recommendations.md).

## <a name="additional-resources"></a>الموارد الإضافية

[إضافة عنصر تحكم في التوصيات إلى شاشة الحركة على أجهزة نقطة البيع (POS)](add-recommendations-control-pos-screen.md)

[نظرة عامة على توصيات المنتجات](../commerce/product-recommendations.md)

[تمكين توصيات المنتجات](../commerce/enable-product-recommendations.md) 
