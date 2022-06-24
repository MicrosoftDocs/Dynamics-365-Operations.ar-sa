---
title: تمكين Azure Data Lake Storage في بيئة Dynamics 365 Commerce
description: يوفر هذا المقال إرشادات حول كيفية توصيل حل Azure Data Lake Storage Gen 2 بمتجر الكيانات في بيئات Dynamics 365 Commerce. هذه الخطوة مطلوبة قبل تمكين توصيات المنتج.
author: bebeale
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6e0c84dd6b173a111b70a8adb6036be946149f7c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885161"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a>تمكين Azure Data Lake Storage في بيئة Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

يوفر هذا المقال إرشادات حول كيفية توصيل حل Azure Data Lake Storage Gen2 بمتجر الكيانات في بيئات Dynamics 365 Commerce. هذه الخطوة مطلوبة قبل تمكين توصيات المنتج.

في حل Dynamics 365 Commerce، يتم تجميع البيانات اللازمة لحساب التوصيات والمنتجات والحركات في متجر كيانات البيئة. لتمكين وصول هذه البيانات لخدمات Dynamics 365 الأخرى، مثل تحليلات البيانات والمعلومات المهنية والتوصيات المخصصة، من الضروري توصيل البيئة بحل Azure Data Lake Storage Gen2 الذي يملكه العميل.

بعد اكتمال الخطوات السابقة، يتم تلقائياً نسخ كافة بيانات العميل الموجودة في متجر كيانات البيئة إلى حل Azure Data Lake Storage Gen 2 للعميل. عند تمكين ميزات التوصيات من خلال مساحة عمل إدارة الميزات في المركز الرئيسي لـ Commerce، سيتم منح مكدس التوصيات حق الوصول إلى نفس حل Azure Data Lake Storage Gen2.

أثناء العملية بأكملها تظل بيانات العملاء محمية وتصبح تحت تحكمهم.

## <a name="prerequisites"></a>المتطلبات الأساسية

يجب توصيل متجر كيانات بيئة Dynamics 365 Commerce بحساب Azure Data Lake Gen Storage Gen2 والخدمات المرفقة به.

لمزيد من المعلومات حول Azure Data Lake Storage Gen2وكيفية إعداده، راجع [وثائق Azure Data Lake Storage Gen2الرسمية](https://azure.microsoft.com/pricing/details/storage/data-lake).
  
## <a name="configuration-steps"></a>خطوات التكوين

يغطي هذا القسم خطوات التكوين الضرورية لتمكين Azure Data Lake Storage Gen2في بيئة ما كما يتعلق بتوصيات المنتجات.
للحصول على نظرة عامة أكثر عمقًا للخطوات المطلوبة لتمكين Azure Data Lake Storage Gen2، راجع [جعل متجر الكيانات‬ متوفرًا كـ Data Lake‬](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).

### <a name="enable-azure-data-lake-storage-in-the-environment"></a>تمكين Azure Data Lake Storage في البيئة

1. سجل الدخول إلى مدخل المكتب الخلفي للبيئة.
1. ابحث عن **معلمات النظام** وانتقل إلى علامة التبويب **اتصالات البيانات**. 
1. عيِّن **تمكين تكامل Data Lake** على **نعم**.
1. ثم أدخل المعلومات المطلوبة التالية:
    1. **معرف التطبيق** // **سر التطبيق** // **اسم DNS** - مطلوب للاتصال ب KeyVault حيث يتم تخزين سر Azure Data Lake Storage.
    1. **اسم السر** - اسم السر المخزن في KeyVault والمستخدم للمصادقة مع Azure Data Lake Storage.
1. احفظ التغييرات في الجزء العلوي الأيمن من الصفحة.

تعرض الصورة التالية مثالاً لتكوين Azure Data Lake Storage.

![مثال لتكوين Azure Data Lake Storage.](./media/exampleADLSConfig1.png)

### <a name="test-the-azure-data-lake-storage-connection"></a>اختبار اتصال Azure Data Lake Storage

1. اختبار الاتصال بـ KeyVault باستخدام ارتباط **اختبار Azure Key Vault**.
1. اختبر اتصال Azure Data Lake Storage باستخدام ارتباط **اختبار Azure Storage**.

> [!NOTE]
> في حالة فشل أي من الاختبارات أعلاه، تأكد من صحة جميع معلومات KeyVault المضافة، ثم حاول مرة أخرى.

بمجرد نجاح اختبارات الاتصال، يجب تمكين التحديث التلقائي لمخزن الوحدات.

لتمكين التحديث التلقائي لمخزن الكيانات، اتبع الخطوات التالية.

1. ابحث عن **مخزن الكيانات**.
1. في القائمة الموجودة على اليمين، انتقل إلى إدخال **RetailSales**، وحدد **تحرير**.
1. تأكد من تعيين **تم تمكين التحديث التلقائي** على القيمة **نعم**، وحدد **تحديث**، ثم حدد **حفظ**.

تعرض الصورة التالية مثالاً لمخزن الكيانات مع تمكين التحديث التلقائي.

![مثال على مخزن الكيانات مع تمكين التحديث التلقائي.](./media/exampleADLSConfig2.png)

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
