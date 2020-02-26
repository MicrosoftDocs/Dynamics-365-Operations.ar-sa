---
title: تمكين ADLS في بيئة Dynamics 365 Commerce
description: يوضح هذا الموضوع كيفية تمكين واختبار Azure Data Lake Storage (ADLS) لإحدى بيئات Dynamics 365 Commerce، والتي تعتبر متطلبًا أساسيًا لتمكين توصيات المنتج.
author: bebeale
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: 068eb522bd44e02dd31d3337a051691a956637fc
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/04/2020
ms.locfileid: "3025221"
---
# <a name="enable-adls-in-a-dynamics-365-commerce-environment"></a>تمكين ADLS في بيئة Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

يوضح هذا الموضوع كيفية تمكين واختبار Azure Data Lake Storage (ADLS) لإحدى بيئات Dynamics 365 Commerce، والتي تعتبر متطلبًا أساسيًا لتمكين توصيات المنتج.

## <a name="overview"></a>نظرة عامة

في الحل Dynamics 365 Commerce، يتم تعقب كل المنتجات والحركات في مخزن كيانات البيئة. لتمكين وصول هذه البيانات لخدمات Dynamics 365 الأخرى، مثل تحليلات البيانات والمعلومات المهنية والتوصيات المخصصة، من الضروري توصيل البيئة بحل Azure Data Lake Storage (ADLS) المملوك للعميل من الجيل الثاني.

بتكوين ADLS لإحدى البيئات، يتم إجراء نسخًا متطابقًا لكل البيانات الضرورية من مخزن الوحدات أثناء حمايتها والاحتفاظ بها في تحكم العميل.

في حالة تمكين توصيات المنتج أو التوصيات المخصصة أيضًا في البيئة، سيتم منح مكدس توصيات المنتجات إمكانية الوصول إلى المجلد المخصص في ADLS لاسترداد بيانات العميل وحساب التوصيات استنادًا إليه.

## <a name="prerequisites"></a>المتطلبات الأساسية

يحتاج العملاء إلى تكوين ADLS في أحد اشتراكات Azure التي يملكونها. لا يتناول هذا الموضوع شراء اشتراك Azure أو إعداد حساب تخزين تم تمكين ADLS له.

لمزيد من المعلومات حول ADLS، راجع [وثائق ADLS الرسمية](https://azure.microsoft.com/pricing/details/storage/data-lake).
  
## <a name="configuration-steps"></a>خطوات التكوين

يتناول هذا القسم خطوات التكوين الضرورية لتمكين ADLS في إحدى البيئات.

### <a name="enable-adls-in-the-environment"></a>تمكين ADLS في البيئة

1. سجل الدخول إلى مدخل المكتب الخلفي للبيئة.
1. ابحث عن **معلمات النظام** وانتقل إلى علامة التبويب **اتصالات البيانات**. 
1. عيِّن **تمكين تكامل Data Lake** على **نعم**.
1. عيِّن **تحديث Data Lake بشكل تدريجي** على **نعم**.
1. ثم أدخل المعلومات المطلوبة التالية:
    1. **معرف التطبيق** // **سر التطبيق** // **اسم DNS** - المطلوب للاتصال ب KeyVault حيث يتم تخزين سر ADLS.
    1. **الاسم السري** - الاسم السري المخزن في KeyVault والمستخدم للمصادقة مع ADLS.
1. احفظ التغييرات في الجزء العلوي الأيمن من الصفحة.

تعرض الصورة التالية مثالاً لتكوين ADLS.

![مثال لتكوين ADLS](./media/exampleADLSConfig1.png)

### <a name="test-the-adls-connection"></a>اختبار اتصال ADLS

1. اختبار الاتصال بـ KeyVault باستخدام ارتباط **اختبار Azure Key Vault**.
1. اختبار الاتصال بـ ADLS باستخدام ارتباط **اختبار Azure Storage**.

> [!NOTE]
> في حالة فشل الاختبارات، تحقق مرة أخرى من صحة كل معلومات KeyVault المضافة أعلاه، ثم حاول مرة أخرى.

بمجرد نجاح اختبارات الاتصال، يجب تمكين التحديث التلقائي لمخزن الوحدات.

لتمكين التحديث التلقائي لمخزن الكيانات، اتبع الخطوات التالية.

1. ابحث عن **مخزن الكيانات**.
1. في القائمة الموجودة علي اليمين، انتقل إلى إدخال **RetailSales**، وحدد **تحرير**.
1. تأكد من تعيين **تم تمكين التحديث التلقائي** على القيمة **نعم**، وحدد **تحديث**، ثم حدد **حفظ**.

تعرض الصورة التالية مثالاً لمخزن الكيانات مع تمكين التحديث التلقائي.

![مثال على مخزن الكيانات مع تمكين التحديث التلقائي](./media/exampleADLSConfig2.png)

تم تكوين ADLS الآن للبيئة. 

في حالة عدم الاكتمال بالفعل، اتبع الخطوات [لتمكين توصيات المنتج والتخصيص](enable-product-recommendations.md) للبيئة.

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على توصيات المنتجات](product-recommendations.md)

[تمكين توصيات المنتجات](enable-product-recommendations.md)

[إضافة قوائم توصيات المنتجات إلى الصفحات](add-reco-list-to-page.md)

[إضافة عنصر تحكم في التوصيات إلى شاشة الحركة على أجهزة نقطة البيع (POS)](../retail/add-recommendations-control-pos-screen.md?toc=/dynamics365/commerce/toc.json)


