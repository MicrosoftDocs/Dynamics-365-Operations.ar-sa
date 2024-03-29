---
title: تكوين التقييمات والمراجعات
description: يوضح هذا المقال كيفية تكوين موقع التجارة الإلكترونية لإظهار تصنيفات العملاء ومراجعاتها في Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 27b1beddd474a2ca4db73f8e344b2d85934c43b1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276855"
---
# <a name="configure-ratings-and-reviews"></a>تكوين التقييمات والمراجعات

[!include [banner](includes/banner.md)]

يوضح هذا المقال كيفية تكوين موقع التجارة الإلكترونية لإظهار تصنيفات العملاء ومراجعاتها في Microsoft Dynamics 365 Commerce.

تساعد التقييمات والمراجعات على مواقع التجارة الإلكترونية العملاء على التعرف على المنتجات قبل اتخاذ قرار الشراء وذلك من خلال إظهار ما يفكر فيه العملاء الآخرون بشأن هذه المنتجات. بالنسبة لمواقع التجارة الإلكترونية، تعد التصنيفات والمراجعات أيضًا آلية لجمع تعليقات العملاء حول المنتجات. 

## <a name="configure-a-site-to-show-ratings-and-reviews"></a>تكوين موقع لإظهار التقييمات والمراجعات

يتم تكوين قيم التكوين الخاصة بالتقييمات والمراجعات، مثل معرف المستأجر وطول نص المراجعة وطول عنوان المراجعة، على مستوى الموقع. 

لتكوين موقع لإظهار التقييمات والمراجعات، اتبع هذه الخطوات. 

1. الانتقال **إلى الصفحة الرئيسية \> المواقع**.
1. حدد اسم موقعك. 
1. انتقل إلى **إعدادات الموقع \> الملحقات**. 
1. في الحقل **أقصى طول لنص المراجعة**، أدخل الحد الأقصى لعدد الأحرف التي يمكن أن يشتمل عليها نص المراجعة (على سبيل المثال، **1000**). 
1. في الحقل **أقصى طول لعنوان المراجعة**، أدخل الحد الأقصى لعدد الأحرف التي يمكن أن يشتمل عليها عناوين المراجعة (على سبيل المثال، **55**). 
1. حدد **حفظ ونشر**. 

يوضح الرسم التوضيحي التالي كيف يبدو هذا التكوين في Dynamics 365 Commerce.

![تكوين موقع لإظهار التقييمات والمراجعات.](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a>ربط تقييم المنتج بقسم المراجعات في PDP

يتم عرض تقييم المنتج أسفل عنوان المنتج أعلى PDP. يمكن تكوين تصنيف المنتج بحيث يكون مرتبطًا بقسم **المراجعات** لنفس PDP. 

لربط تقييم منتج بقسم **المراجعات** لـ PDP، اتبع الخطوات التالية.

1. افتح قالب PDP. 
1. انتقل إلى **إعدادات الوحدة النمطية لحاوية مربع الشراء**.
1. تحت **مربع الشراء**، حدد **تقييمات المنتج**، ثم حدد خانه الاختيار **ربط النقر بالوحدة النمطية للمراجعات الكاملة** .

يوضح الرسم التوضيحي التالي كيف يبدو هذا التكوين في Dynamics 365 Commerce.

![ربط تقييم المنتج بقسم المراجعات في PDP.](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a>تكوين ارتباط صفحة الخصوصية والسياسة

لتكوين ارتباط صفحة الخصوصية والسياسة، اتبع هذه الخطوات.

1. الانتقال **إلى الصفحة الرئيسية \> المواقع**.
1. حدد اسم موقعك. 
1. انتقل إلى **إعدادات الموقع \> الملحقات**.
1. في علامة التبويب **المسارات** ، وتحت **خصوصية وسياسة RNR**، حدد **إضافة ارتباط**. إذا تم إدخال ارتباط بالفعل وتريد استبداله، فحدد الارتباط. 
1. في مربع الحوار **إضافة ارتباط** ،حدد ارتباط صفحة الخصوصية والسياسة، ثم حدد **موافق**. 
1. حدد **حفظ ونشر**. 

يوضح الرسم التوضيحي التالي كيف يبدو هذا التكوين في Dynamics 365 Commerce.

![تكوين ارتباط صفحة الخصوصية والسياسة.](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="configure-ratings-and-reviews-modules-on-product-details-pages"></a>تكوين الوحدات النمطية للتصنيفات والمراجعات في صفحات تفاصيل المنتج

للحصول على معلومات حول تكوين الوحدات النمطية للتصنيفات والمراجعات على صفحات تفاصيل المنتج، راجع [الوحدات النمطية للتصنيفات والمراجعات](ratings-reviews-modules.md).

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على التقييمات والمراجعات](ratings-reviews-overview.md)

[الموافقة على استخدام التقييمات والمراجعات](opt-in-ratings-reviews.md)

[إدارة التقييمات والمراجعات](manage-reviews.md)

[مزامنة تقييمات المنتجات في Dynamics 365 Retail](sync-product-ratings.md)

[تمكين النشر اليدوي لتقييمات ومراجعات بواسطة المشرف](manual-publish-rating-reviews.md)

[استيراد التقييمات والمراجعات وتصديرها](import-export-reviews.md)

[تكوين مصادقة من خدمة إلى خدمة](service-to-service-auth.md)

[الأسئلة المتداولة حول التقييمات والمراجعات](ratings-reviews-faq.md)

[وحدات التقييمات والمراجعات](ratings-reviews-modules.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
