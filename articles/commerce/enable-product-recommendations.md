---
title: تمكين توصيات المنتجات
description: يوضح هذا الموضوع كيفية عمل توصيات المنتج التي تستند إلى التعلم الآلي القائم على الذكاء الاصطناعي (AI-ML) المتوفرة لعملاء Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 08/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4a7be82b3a40aba621693f080ff41767fdaea474
ms.sourcegitcommit: 98061a5d096ff4b9078d1849e2ce6dd7116408d1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2021
ms.locfileid: "7466306"
---
# <a name="enable-product-recommendations"></a>تمكين توصيات المنتجات

[!include [banner](includes/banner.md)]

يوضح هذا الموضوع كيفية عمل توصيات المنتج التي تستند إلى التعلم الآلي القائم على الذكاء الاصطناعي (AI-ML) المتوفرة لعملاء Microsoft Dynamics 365 Commerce. لمزيد من المعلومات حول قوائم توصيات المنتجات، راجع [‏‫نظرة عامة على توصيات المنتجات‬](product-recommendations.md)

## <a name="recommendations-pre-check"></a>توصيات قبل الفحص

1. تأكد من أن لديك ترخيص صالح لتوصيات Dynamics 365 Commerce.
1. تأكد من أن متجر الكيانات متصل بحساب Azure Data Lake Storage Gen2 مملوك لعميل. لمزيد من المعلومات، راجع [التأكد من شراء Azure Data Lake Storage والتحقق منه في البيئة بنجاح](enable-ADLS-environment.md).
1. التأكد من أن تكوين الهوية في Azure AD يحتوي على إدخال للتوصيات. توجد أدناه معلومات اضافيه حول كيفية تنفيذ هذا الإجراء.
1. تأكد من أنه تمت جدولة تحديث متجر الكيانات يومياً إلى Azure Data Lake Storage Gen2. لمزيد من المعلومات، راجع [التأكد من تعيين التنفيذ التلقائي لتحديث مخزن الكيانات](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).
1. تمكين قياسات RetailSale لمتجر الكيانات. لمعرفة المزيد عن إعداد هذه العملية، راجع [التعامل مع المقاييس](/dynamics365/ai/customer-insights/pm-measures).

بعد اكتمال الخطوات المذكورة أعلاه، ستكون جاهزًا لتمكين التوصيات.

## <a name="azure-ad-identity-configuration"></a>تكوين الهوية في Azure AD

هذه الخطوة مطلوبة فقط للعملاء الذين يقومون بتشغيل تكوين خدمة تأجير البنية التحتية (IaaS). يصبح تكوين هوية Azure AD تلقائياً للعملاء الذين يعملون على Azure Service Fabric، لكن يوصى بأن تتحقق من أنه تم تكوين الإعداد كما هو متوقع.

### <a name="setup"></a>الإعداد

1. في المركز الرئيسي لـ Commerce، ابحث عن صفحة **تطبيقات Azure Active Directory**.
1. تحقق من وجود إدخال لـ **RecommendationSystemApplication-1**. في حالة عدم وجود أي إدخال، قم بإنشاء واحد باستخدام المعلومات التالية:

    - **معرف العميل**: d37b07e8-dd1c-4514-835d-8b918e6f9727
    - **الاسم‏‎**: RecommendationSystemApplication-1
    - **معرف المستخدم**: RetailServiceAccount

1. احفظ الصفحة وإغلاقها. 

## <a name="turn-on-recommendations"></a>تشغيل التوصيات

لتشغيل توصيات المنتج‬، اتبع الخطوات التالية.

1. في المركز الرئيسي لـ Commerce ، ابحث عن **إدارة الميزات**.
1. حدد **الكل** للاطلاع على قائمة الميزات المتاحة. 
1. في مربع البحث، ادخل **التوصيات**.
1. حدد ميزة **توصيات المنتج**.
1. في جزء خصائص **توصيات المنتج** ، حدد **تمكين الآن**.

![تشغيل التوصيات.](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> - يبدأ الإجراء أعلاه عملية إنشاء قوائم توصيات المنتج. قد تحتاج إلى عدة ساعات قبل أن تصبح القوائم متوفرة ويمكن عرضها في نقطة البيع أو في Dynamics 365 Commerce.
> - لا يقوم هذا التكوين بتمكين كافة ميزات التوصيات. يتم التحكم في الميزات المتقدمة مثل التوصيات الشخصية و"تسوق أشكال مماثلة" و"تسوق وصف مماثل" بواسطة إدخالات إدارة الميزات المخصصة. لمزيد من المعلومات حول تمكين هذه الميزات في المركز الرئيسي لـ Commerce، راجع [تمكين التوصيات الشخصية](personalized-recommendations.md)، و[تمكين توصيات "تسوق أشكال مماثلة"](shop-similar-looks.md)، و[تمكين توصيات "تسوق وصف مماثل"](shop-similar-description.md).

## <a name="configure-recommendation-list-parameters"></a>تكوين معلمات قائمة التوصيات

بشكل افتراضي، توفر قائمة توصيات المنتج المستندة إلى AI-ML، قيم مقترحة. يمكنك تغيير القيم المقترحة الافتراضية لتناسب تدفق أعمالك. لمعرفة المزيد حول كيفية تغيير المعلمات الافتراضية، انتقل إلى [‏‫إدارة نتائج توصيات المنتجات المستندة إلى AI-ML‬](modify-product-recommendation-results.md).

## <a name="include-recommendations-in-e-commerce-experiences"></a>تضمين التوصيات في تجارب التجارة الإلكترونية

بعد تمكين التوصيات في المركز الرئيسي لـ Commerce، تصبح الوحدات النمطية لـ Commerce المستخدمة لعرض نتائج التوصيات الخاصة بتجارب التجارة الإلكترونية جاهزه ليتم تكوينها. لمزيد من المعلومات، راجع [وحدات مجموعة المنتجات](product-collection-module-overview.md).

## <a name="show-recommendations-on-pos-devices"></a>إظهار التوصيات على أجهزة نقاط البيع

بعد تمكين التوصيات في المركز الرئيسي لـ Commerce، يجب إضافة لوحة التوصيات إلى شاشة التحكم في نقطة البيع بواسطة أداة التخطيط. لمعرفه المزيد حول هذه العملية، راجع [إضافة عنصر تحكم التوصيات إلى شاشة الحركات على أجهزة نقطة البيع](add-recommendations-control-pos-screen.md). 

## <a name="enable-personalized-recommendations"></a>تمكين التوصيات المخصصة

وفي Dynamics 365 Commerce، يمكن لبائعي التجزئة إجراء توصيات للمنتجات الشخصية (والتي تعرف أيضا بالتخصيص) المتوفرة. وبهذه الطريقة، يمكن دمج التوصيات الشخصية في تجربه العميل عبر الإنترنت وفي نقطه البيع. عند تشغيل وظيفة إضفاء الطابع الشخصي، يمكن للنظام ربط معلومات الشراء والمنتج الخاصة بالمستخدم لإنشاء توصيات منتج إينديفيدواليزيد.

لمعرفة المزيد حول كيفية تلقي توصيات مخصصة، راجع [تمكين التوصيات المخصصة](personalized-recommendations.md).

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على توصيات المنتجات](product-recommendations.md)

[تمكين Azure Data Lake Storage في بيئة Dynamics 365 Commerce](enable-adls-environment.md)

[تمكين التوصيات المخصصة](personalized-recommendations.md)

[تمكين توصيات "تسوق منتجات تبدو مماثلة"](shop-similar-looks.md)

[إلغاء الاشتراك في التوصيات المخصصة](personalization-gdpr.md)

[إضافة توصيات المنتجات على نقطة البيع](product.md)

[إضافة توصيات إلى شاشة المعاملة](add-recommendations-control-pos-screen.md)

[إدارة نتائج توصيات الذكاء الاصطناعي والتعلم الآلي (AI-ML)](modify-product-recommendation-results.md)

[إنشاء توصيات مختارة يدويًا](create-editorial-recommendation-lists.md)

[إنشاء توصيات بواسطة بيانات العرض التوضيحي](product-recommendations-demo-data.md)

[الأسئلة المتداولة حول توصيات المنتجات](faq-recommendations.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
