---
title: تمكين توصيات المنتجات
description: يوضح هذا الموضوع كيفية عمل توصيات المنتج التي تستند إلى التعلم الآلي القائم على الذكاء الاصطناعي (AI-ML) المتوفرة لعملاء Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d8a579be5df3c5e7718a6fb4720341f3bd01a64c
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154403"
---
# <a name="enable-product-recommendations"></a>تمكين توصيات المنتجات

[!include [banner](includes/banner.md)]

يوضح هذا الموضوع كيفية عمل توصيات المنتج التي تستند إلى التعلم الآلي القائم على الذكاء الاصطناعي (AI-ML) المتوفرة لعملاء Microsoft Dynamics 365 Commerce. لمزيد من المعلومات حول قوائم توصيات المنتجات، راجع [‏‫نظرة عامة على توصيات المنتجات‬](product-recommendations.md)

## <a name="recommendations-pre-check"></a>توصيات قبل الفحص

قبل التمكين، يرجى ملاحظة أن توصيات المنتج غير مدعومة إلا لعملاء Commerce ممن رحلوا التخزين الخاص بهم إلى باستخدام Azure Data Lake Storage (ADLS). 

لمعرفة خطوات تمكين ADLS، راجع [كيفية تمكين ADLS في بيئة Dynamics 365](enable-ADLS-environment.md).

بالإضافة إلى ذلك، تأكد من تمكين قياسات RetailSale. لمعرفه المزيد حول عملية الإعداد هذه، انتقل إلى [هنا.](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)


## <a name="turn-on-recommendations"></a>تشغيل التوصيات

لتشغيل توصيات المنتج‬، اتبع الخطوات التالية.

1. انتقل إلى ‏‫‏‫**البيع بالتجزئة والتجارة&gt; توصيات المنتج &gt; معلمات التوصية**.
1. في قائمة المعلمات المشتركة، حدد **قوائم التوصيات**.
1. عيّن الخيار **تمكين التوصيات** إلى **نعم**.

![تمكين توصيات المنتجات](./media/enableproductrecommendations.png)

> [!NOTE]
> يبدأ هذا الإجراء عملية إنشاء قوائم توصيات المنتج. قد تكون هناك حاجة إلى عدة ساعات قبل توفر القوائم ويمكن رؤيتها في نقطة البيع (POS) أو في Dynamics 365 Commerce.

## <a name="configure-recommendation-list-parameters"></a>تكوين معلمات قائمة  التوصيات

بشكل افتراضي، توفر قائمة توصيات المنتج المستندة إلى AI-ML، قيم مقترحة. يمكنك تغيير القيم المقترحة الافتراضية لتناسب تدفق أعمالك. لمعرفة المزيد حول كيفية تغيير المعلمات الافتراضية، انتقل إلى [‏‫إدارة نتائج توصيات المنتجات المستندة إلى AI-ML‬](modify-product-recommendation-results.md).

## <a name="show-recommendations-on-pos-devices"></a>إظهار التوصيات على أجهزة نقاط البيع

بعد تمكين التوصيات في مكتب دعم Commerce، يجب إضافة لوحة التوصيات إلى شاشة التحكم في نقطة البيع بواسطة أداة التخطيط. لمعرفه المزيد حول هذه العملية، راجع [إضافة عنصر تحكم التوصيات إلى شاشة الحركات على أجهزة نقطة البيع](add-recommendations-control-pos-screen.md). 

## <a name="enable-personalized-recommendations"></a>تمكين التوصيات المخصصة

لمعرفه المزيد حول كيفية تلقي توصيات مخصصة، راجع [تمكين التوصيات المخصصة](personalized-recommendations.md).

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على توصيات المنتجات](product-recommendations.md)

[تمكين ADLS في بيئة Dynamics 365 Commerce](enable-adls-environment.md)

[تمكين التوصيات المخصصة](personalized-recommendations.md)

[إلغاء الاشتراك في التوصيات المخصصة](personalization-gdpr.md)

[إضافة توصيات المنتجات على نقطة البيع](product.md)

[إضافة توصيات إلى شاشة المعاملة](add-recommendations-control-pos-screen.md)

[إدارة نتائج توصيات الذكاء الاصطناعي والتعلم الآلي (AI-ML)](modify-product-recommendation-results.md)

[إنشاء توصيات مختارة يدويًا](create-editorial-recommendation-lists.md)

[إنشاء توصيات بواسطة بيانات العرض التوضيحي](product-recommendations-demo-data.md)

[الأسئلة المتداولة حول توصيات المنتجات](faq-recommendations.md)

