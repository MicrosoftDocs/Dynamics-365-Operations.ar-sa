---
title: تمكين توصيات المنتجات
description: يوضح هذا الموضوع كيفية عمل توصيات المنتج التي تستند إلى التعلم الآلي القائم على الذكاء الاصطناعي (AI-ML) المتوفرة لعملاء Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.openlocfilehash: 59c83409ede5e006ddf030d396934eeb6cd8df76
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010114"
---
# <a name="enable-product-recommendations"></a>تمكين توصيات المنتجات

[!include [banner](includes/banner.md)]

يوضح هذا الموضوع كيفية عمل توصيات المنتج التي تستند إلى التعلم الآلي القائم على الذكاء الاصطناعي (AI-ML) المتوفرة لعملاء Microsoft Dynamics 365 Commerce. لمزيد من المعلومات حول قوائم توصيات المنتجات، راجع [‏‫نظرة عامة على توصيات المنتجات‬](product-recommendations.md)

## <a name="recommendations-pre-check"></a>توصيات قبل الفحص

قبل التمكين، يرجى العلم أن توصيات المنتج غير مدعومة إلا لعملاء Commerce ممن قاموا بترحيل مساحة التخزين باستخدام Azure Data Lake Storage. 

يجب تمكين التكوينات التالية في المكتب الخلفي قبل تمكين التوصيات:

1. تأكد من شراء Azure Data Lake Storage والتحقق منه في البيئة بنجاح. لمزيد من المعلومات، راجع [التأكد من شراء Azure Data Lake Storage والتحقق منه في البيئة بنجاح](enable-ADLS-environment.md).
2. التأكد من تعيين التنفيذ التلقائي لتحديث مخزن الكيانات‬. لمزيد من المعلومات، راجع [التأكد من تعيين التنفيذ التلقائي لتحديث مخزن الكيانات](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).
3. التأكد من أن تكوين الهوية في Azure AD يحتوي على إدخال للتوصيات. توجد أدناه معلومات اضافيه حول كيفية تنفيذ هذا الإجراء.

بالإضافة إلى ذلك، تأكد من تمكين قياسات RetailSale. لمعرفة المزيد عن عملية الإعداد هذه، راجع [التعامل مع المقاييس](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).

## <a name="azure-ad-identity-configuration"></a>تكوين الهوية في Azure AD

هذه الخطوة مطلوبة لجميع العملاء الذين يقومون بتشغيل بنية تحتية على أنها تكوين كخدمة (IaaS). بالنسبة إلى العملاء الذين يقومون بتشغيل Service Fabric (SF)، يجب أن تكون هذه الخطوة تلقائية، وننصح بالتحقق من تكوين الإعداد كما هو متوقع.

### <a name="setup"></a>الإعداد

1. من المكتب الخلفي، ابحث عن صفحة **تطبيقات Azure Active Directory**.
2. تحقق من وجود إدخال لـ "RecommendationSystemApplication-1".

في حال عدم وجود الإدخال، أضف إدخالاً جديدًا يتضمن المعلومات التالية:

- **معرف العميل** - d37b07e8-dd1c-4514-835d-8b918e6f9727
- **الاسم‏‎** - RecommendationSystemApplication-1
- **معرف المستخدم** - RetailServiceAccount

احفظ الصفحة وإغلاقها. 

## <a name="turn-on-recommendations"></a>تشغيل التوصيات

لتشغيل توصيات المنتج‬، اتبع الخطوات التالية.

1. في المركز الرئيسي لـ Commerce ، ابحث عن **إدارة الميزات**.
1. حدد **الكل** للاطلاع على قائمة الميزات المتاحة. 
1. في مربع البحث، ادخل **التوصيات**.
1. حدد ميزة **توصيات المنتج**.
1. في جزء خصائص **توصيات المنتج** ، حدد **تمكين الآن**.

![تشغيل التوصيات](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> يبدأ هذا الإجراء عملية إنشاء قوائم توصيات المنتج. قد تحتاج إلى عدة ساعات قبل أن تصبح القوائم متوفرة ويمكن عرضها في نقطة البيع أو في Dynamics 365 Commerce.

## <a name="configure-recommendation-list-parameters"></a>تكوين معلمات قائمة التوصيات

بشكل افتراضي، توفر قائمة توصيات المنتج المستندة إلى AI-ML، قيم مقترحة. يمكنك تغيير القيم المقترحة الافتراضية لتناسب تدفق أعمالك. لمعرفة المزيد حول كيفية تغيير المعلمات الافتراضية، انتقل إلى [‏‫إدارة نتائج توصيات المنتجات المستندة إلى AI-ML‬](modify-product-recommendation-results.md).

## <a name="show-recommendations-on-pos-devices"></a>إظهار التوصيات على أجهزة نقاط البيع

بعد تمكين التوصيات في مكتب دعم Commerce، يجب إضافة لوحة التوصيات إلى شاشة التحكم في نقطة البيع بواسطة أداة التخطيط. لمعرفه المزيد حول هذه العملية، راجع [إضافة عنصر تحكم التوصيات إلى شاشة الحركات على أجهزة نقطة البيع](add-recommendations-control-pos-screen.md). 

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

