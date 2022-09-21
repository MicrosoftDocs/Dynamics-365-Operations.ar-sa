---
title: إضافة توصيات المنتجات على نقطة البيع
description: ‏‫يصف هذا المقال استخدام توصيات المنتج على جهاز نقطه البيع (POS).
author: bebeale
ms.date: 09/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 170e2bf18aefc79a796620818c7100ff8e6e689a
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460046"
---
# <a name="add-product-recommendations-on-pos"></a>إضافة توصيات المنتجات على نقطة البيع

[!include [banner](includes/banner.md)]

‏‫في أساسه، تُعد توصيات المنتج بمثابة أحد تطبيقات الاعمال التحويلية الذي يمتد عبر جميع مساحات التجارة لخلق تجارب اكتشاف منتج غنية وجذابة ومخصصة. لتطبيق هذه الميزة في نقطه البيع، اتبع الخطوات الخاصة [بكيفية إضافة توصيات إلى أجهزة نقطة البيع.](add-recommendations-control-pos-screen.md) 

لمزيد من المعلومات حول ميزات توصيات المنتجات، راجع [نظرة عامة على توصيات المنتجات.](../commerce/product-recommendations.md) 

## <a name="scenarios"></a>السيناريوهات

يتم تمكين توصيات المنتج لسيناريوهات نقطة البيع التالية. تتوافر في نقطة بيع المجموعة (POS) أو نقطة بيع حديثة (MPOS).

1. في صفحة **تفاصيل المنتجات**:

    - إذا قام شريك في المتجر بزيارة صفحة **تفاصيل المنتج** عند النظر في الحركات السابقة عبر القنوات المختلفة، فإن خدمة التوصيات تقترح بنود إضافية والتي من المرجح شرائها معًا. استنادا إلى الوظائف الاضافيه الخاصة بالخدمة ، يمكن لبائعي التجزئة إظهار **المظهر** المشابه للتسوق والتوصيات **المتشابهة** للمنتجات ، بالاضافه إلى التوصيات الشخصية للمستخدمين الذين لديهم سجل شراء سابق.

    [![التوصيات في صفحة تفاصيل المنتج.](./media/proddetails.png)](./media/proddetails.png)

2. في صفحة **الحركة**:

    - يقوم محرك التوصيات باقتراح الأصناف التي تستند إلى قائمة الأصناف بأكملها في السلة التي يتم شراؤها بشكل متكرر معًا.

    > [!NOTE]
    > لعرض التوصيات على صفحة **الحركة**، يحتاج تاجر التجزئة إلى تحديث تخطيط الشاشة في Dynamics 365 Commerce. يجب إسقاط عنصر تحكم **التوصيات** داخل صفحة **الحركة** .

    [![التوصيات في صفحة الحركة.](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

## <a name="configure-commerce-to-enable-pos-recommendations"></a>تكوين Commerce لتمكين توصيات نقطة البيع 

لاعداد توصيات المنتج ، تاكد من إكمال عمليه التوفير لتوصيات المنتج التجارية من خلال اتباع الخطوات الموضحة في تمكين توصيات [المنتج](../commerce/enable-product-recommendations.md). تظهر التوصيات بشكل افتراضي علي كل من **صفحه تفاصيل** المنتج وصفحه تفاصيل **العميل** بعد إكمال خطوات التقديم وكوكيدت البيانات بنجاح. 

## <a name="add-recommendations-to-the-transaction-screen"></a>إضافة توصيات إلى شاشة المعاملة

1. لأضافه توصيات إلى شاشه الحركة ، اتبع الخطوات الموجودة في [أضافه توصيات علي شاشه](add-recommendations-control-pos-screen.md)الحركة.
1. لعكس التغييرات التي تم اجراؤها في مصمم تخطيط شاشه نقطه البيع ، قم بتشغيل مهمة **تكوين القناة 1070** في Commerce headquarters.

> [!NOTE] 
> إذا كنت ترغب في تمكين توصيات نقطه البيع باستخدام ملف القيم المفصولة بفواصل RecoMock (CSV) ، يجب نشر ملف CSV إلى Microsoft Dynamics مكتبه أصول خدمات Lifecycle Services (LCS) قبل تكوين أداره التخطيط. في حاله استخدام ملف CSV RecoMock ، لا يلزم القيام بتمكين التوصيات. يتوفر ملف CSV لأغراض العرض التوضيحي فقط. من المستحسن للعملاء أو مهندسي الحلول الذين يرغبون في محاكاة مظهر قوائم التوصيات لأغراض العرض التوضيحي دون الحاجة إلى شراء وحده الاحتفاظ بالمخزون الاضافيه (SKU).

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على توصيات المنتجات](product-recommendations.md)

[تمكين Azure Data Lake Storage في بيئة Dynamics 365 Commerce](enable-adls-environment.md)

[تمكين توصيات المنتجات](enable-product-recommendations.md)

[تمكين التوصيات المخصصة](personalized-recommendations.md)

[إلغاء الاشتراك في التوصيات المخصصة](personalization-gdpr.md)

[تمكين توصيات "تسوق منتجات تبدو مماثلة"](shop-similar-looks.md)

[إضافة توصيات إلى شاشة المعاملة](add-recommendations-control-pos-screen.md)

[إدارة نتائج توصيات الذكاء الاصطناعي والتعلم الآلي (AI-ML)](modify-product-recommendation-results.md)

[إنشاء توصيات مختارة يدويًا](create-editorial-recommendation-lists.md)

[إنشاء توصيات بواسطة بيانات العرض التوضيحي](product-recommendations-demo-data.md)

[الأسئلة المتداولة حول توصيات المنتجات](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
