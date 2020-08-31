---
title: تمكين Azure Data Lake Storage في بيئة Dynamics 365 Commerce
description: يوضح هذا الموضوع كيفية تمكين واختبار Azure Data Lake Storage لبيئة Dynamics 365 Commerce، وهو عبارة عن شرط أساسي لتمكين توصيات المنتج.
author: bebeale
manager: AnnBe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 27e4f1c751ee865b0df536f3c1912cb1d8946032
ms.sourcegitcommit: 8905d7a7a010e451c5435086480f66650ec54926
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/06/2020
ms.locfileid: "3664992"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a>تمكين Azure Data Lake Storage في بيئة Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

يوضح هذا الموضوع كيفية تمكين واختبار Azure Data Lake Storage لبيئة Dynamics 365 Commerce، وهو عبارة عن شرط أساسي لتمكين توصيات المنتج.

## <a name="overview"></a>نظرة عامة

في الحل Dynamics 365 Commerce، يتم تعقب كل المنتجات والحركات في مخزن كيانات البيئة. لتمكين وصول هذه البيانات لخدمات Dynamics 365 الأخرى، مثل تحليلات البيانات والمعلومات المهنية والتوصيات المخصصة، من الضروري توصيل البيئة بحل Azure Data Lake Storage Gen 2 الذي يملكه العميل.

مع تكوين Azure Data Lake Storage لبيئة، يتم إجراء نسخ متطابق لكل البيانات الضرورية من مخزن الوحدات وهي لا تزال محمية وخاضعة لمراقبة العميل.

في حالة تمكين توصيات المنتجات‬ أو التوصيات المخصصة أيضًا في البيئة، سيتم منح مكدس توصيات المنتجات إمكانية الوصول إلى المجلد المخصص في Azure Data Lake Storage لاسترداد بيانات العميل وحساب التوصيات استنادًا إليه.

## <a name="prerequisites"></a>المتطلبات الأساسية

يحتاج العملاء إلى تكوين Azure Data Lake Storage في أحد اشتراكات Azure التي يملكونها. لا يتناول هذا الموضوع شراء اشتراك Azure أو إعداد حساب تخزين تم تمكين Azure Data Lake Storage له.

لمزيد من المعلومات حول Azure Data Lake Storage، راجع [ وثائق Azure Data Lake Storage Gen2](https://azure.microsoft.com/pricing/details/storage/data-lake).
  
## <a name="configuration-steps"></a>خطوات التكوين

يغطي هذا القسم خطوات التكوين الضرورية لتمكين Azure Data Lake Storage في بيئة ما كما يتعلق بتوصيات المنتجات.
للحصول على نظرة عامة أكثر عمقًا للخطوات المطلوبة لتمكين Azure Data Lake Storage، راجع [جعل مخزن الكيانات‬ متوفرًا كـ Data Lake‬](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).

### <a name="enable-azure-data-lake-storage-in-the-environment"></a>تمكين Azure Data Lake Storage في البيئة

1. سجل الدخول إلى مدخل المكتب الخلفي للبيئة.
1. ابحث عن **معلمات النظام** وانتقل إلى علامة التبويب **اتصالات البيانات**. 
1. عيِّن **تمكين تكامل Data Lake** على **نعم**.
1. عيِّن **تحديث Data Lake بشكل تدريجي** على **نعم**.
1. ثم أدخل المعلومات المطلوبة التالية:
    1. **معرف التطبيق** // **سر التطبيق** // **اسم DNS** - مطلوب للاتصال ب KeyVault حيث يتم تخزين سر Azure Data Lake Storage.
    1. **اسم السر** - اسم السر المخزن في KeyVault والمستخدم للمصادقة مع Azure Data Lake Storage.
1. احفظ التغييرات في الجزء العلوي الأيمن من الصفحة.

تعرض الصورة التالية مثالاً لتكوين Azure Data Lake Storage.

![مثال لتكوين Azure Data Lake Storage](./media/exampleADLSConfig1.png)

### <a name="test-the-azure-data-lake-storage-connection"></a>اختبار اتصال Azure Data Lake Storage

1. اختبار الاتصال بـ KeyVault باستخدام ارتباط **اختبار Azure Key Vault**.
1. اختبر اتصال Azure Data Lake Storage باستخدام ارتباط **اختبار Azure Storage**.

> [!NOTE]
> في حالة فشل الاختبارات، تحقق مرة أخرى من صحة كل معلومات KeyVault المضافة أعلاه، ثم حاول مرة أخرى.

بمجرد نجاح اختبارات الاتصال، يجب تمكين التحديث التلقائي لمخزن الوحدات.

لتمكين التحديث التلقائي لمخزن الكيانات، اتبع الخطوات التالية.

1. ابحث عن **مخزن الكيانات**.
1. في القائمة الموجودة على اليمين، انتقل إلى إدخال **RetailSales**، وحدد **تحرير**.
1. تأكد من تعيين **تم تمكين التحديث التلقائي** على القيمة **نعم**، وحدد **تحديث**، ثم حدد **حفظ**.

تعرض الصورة التالية مثالاً لمخزن الكيانات مع تمكين التحديث التلقائي.

![مثال على مخزن الكيانات مع تمكين التحديث التلقائي](./media/exampleADLSConfig2.png)

تم الآن تكوين Azure Data Lake Storage للبيئة. 

في حالة عدم الاكتمال بالفعل، اتبع الخطوات [لتمكين توصيات المنتج والتخصيص](enable-product-recommendations.md) للبيئة.

## <a name="additional-resources"></a>الموارد الإضافية

[جعل مخزن الكيانات‬ متوفرًا كـ Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[نظرة عامة على توصيات المنتجات](product-recommendations.md)

[تمكين توصيات المنتجات](enable-product-recommendations.md)

[تمكين التوصيات المخصصة](personalized-recommendations.md)

[إلغاء الاشتراك في التوصيات المخصصة](personalization-gdpr.md)

[تمكين توصيات "تسوق منتجات تبدو مماثلة"](shop-similar-looks.md)

[إضافة توصيات المنتجات على نقطة البيع](product.md)

[إضافة توصيات إلى شاشة المعاملة](add-recommendations-control-pos-screen.md)

[إدارة نتائج توصيات الذكاء الاصطناعي والتعلم الآلي (AI-ML)](modify-product-recommendation-results.md)

[إنشاء توصيات مختارة يدويًا](create-editorial-recommendation-lists.md)

[إنشاء توصيات بواسطة بيانات العرض التوضيحي](product-recommendations-demo-data.md)

[الأسئلة المتداولة حول توصيات المنتجات](faq-recommendations.md)
