---
title: تمكين توصيات المنتجات
description: يوضح هذا الموضوع كيفية عمل توصيات المنتج التي تستند إلى التعلم الآلي القائم على الذكاء الاصطناعي (AI-ML) المتوفرة لعملاء Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
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
ms.openlocfilehash: ecda571a356c6968196d09cc19923105cf4544ab
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770129"
---
# <a name="enable-product-recommendations"></a>تمكين توصيات المنتجات

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

يوضح هذا الموضوع كيفية عمل توصيات المنتج التي تستند إلى التعلم الآلي القائم على الذكاء الاصطناعي (AI-ML) المتوفرة لعملاء Microsoft Dynamics 365 Commerce. لمزيد من المعلومات حول قوائم توصيات المنتجات، راجع [‏‫نظرة عامة على توصيات المنتجات‬](product-recommendations.md)

## <a name="recommendations-pre-check"></a>توصيات قبل الفحص
قبل التمكين، يرجى ملاحظ أن توصيات المنتج مدعومة فقط بالنسبة لعملاء F&O الذي يدعم الإصدار 10.0.6 وقد قمت بترحيل التخزين الخاص بهم إلى باستخدام BDL. 

بالإضافة إلى ذلك، تأكد من تمكين قياسات RetailSale. لمعرفه المزيد حول عملية الإعداد هذه، انتقل إلى [هنا.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)


## <a name="turn-on-recommendations"></a>تشغيل التوصيات

لتشغيل توصيات المنتج‬، اتبع الخطوات التالية.

1. انتقل إلى **‏‫‏‫Retail‬‬** &gt; **توصيات المنتج** &gt; **معلمات التوصية**.
1. في قائمه معلمات البيع بالتجزئة المشتركة، حدد **قوائم التوصيات**.
1. عيّن الخيار **تمكين التوصيات** إلى **نعم**.

![تمكين توصيات المنتجات](./media/enableproductrecommendations.png)

> [!NOTE]
> يبدأ هذا الإجراء عملية إنشاء قوائم توصيات المنتج. قد تكون هناك حاجة إلى عدة ساعات قبل توفر القوائم ويمكن رؤيتها في نقطة البيع (POS) أو في Dynamics 365 for Commerce.

## <a name="configure-recommendation-list-parameters"></a>تكوين معلمات قائمه التوصيات
بشكل افتراضي، توفر قائمة توصيات المنتج المستندة إلى AI-ML، قيم مقترحة. يمكنك تغيير القيم المقترحة الافتراضية لتناسب تدفق أعمالك. لمعرفة المزيد حول كيفية تغيير المعلمات الافتراضية، انتقل إلى [‏‫إدارة نتائج توصيات المنتجات المستندة إلى AI-ML‬](modify-product-recommendation-results.md).

## <a name="show-recommendations-on-pos-devices"></a>إظهار التوصيات علي أجهزة نقاط البيع
بعد تمكين التوصيات في مكتب الدعم، يجب إضافة لوحة التوصيات إلى شاشة التحكم في نقطه البيع بواسطة أداة التخطيط. لمعرفه المزيد حول هذه العملية، انتقل إلى [هنا.](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)


## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على توصيات المنتجات](product-recommendations.md)

[إضافة قوائم توصيات المنتجات إلى الصفحات](add-reco-list-to-page.md)

[إضافة لوحة التوصيات إلى أجهزة نقاط البيع](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)


