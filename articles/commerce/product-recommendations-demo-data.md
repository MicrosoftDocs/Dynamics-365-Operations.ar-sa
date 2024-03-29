---
title: إنشاء توصيات بواسطة بيانات العرض التوضيحي
description: يهدف هذا المستند إلى توفير إرشادات حول كيفية الاستفادة من توصيات المنتج متعدد القنوات في بيئات مربعات فردية بمستوى 1 باستخدام بيانات العرض التوضيحي المعممة مسبقا.
author: bebeale
ms.date: 09/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7e3df414b3c16c28b6f5ca04f765d91c1312ada4
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/09/2022
ms.locfileid: "9459958"
---
# <a name="create-recommendations-with-demo-data"></a>إنشاء توصيات بواسطة بيانات العرض التوضيحي

[!include [banner](includes/banner.md)]

يهدف هذا المستند إلى توفير إرشادات حول كيفية الاستفادة من توصيات المنتج متعدد القنوات في بيئات مربعات فردية بمستوى 1 باستخدام بيانات العرض التوضيحي المعممة مسبقا.

توفر توصيات المنتج متعدد القنوات مجموعة من قوائم المنتجات تم إنشاؤها بشكل تحريري أو برمجيًا. يمكن استخدام هذه القوائم في العديد من السيناريوهات، وفقًا لاحتياجات العمل. لمزيد من المعلومات حول قوائم توصيات المنتجات، راجع [‏‫نظرة عامة على توصيات المنتجات‬](product-recommendations.md)

بالنسبة لبيئات المنتجات من المستوي 2 وما أعلي، وبيئات Dynamics 365، تُحتسب توصيات منتج البيئات الديناميكية تلقائيًا بناء على بيانات العملاء. لا يؤدي استخدام البيانات التوضيحية لتوصيات المنتج إلى تعطيل اي حل توصيات للمنتج تم توفيرها بالفعل في البيئة وآية تكاليف مرتبطة باستخدامها.

بالنسبة لبيئات المستوي 1، تستند توصيات المنتج فقط على بيانات العرض التوضيحي الثابتة المخزنة في ملف csv..

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a>تمكين بيانات العرض التوضيحي لتوصيات المنتج في البيئة
لتمكين بيانات العرض التوضيحي لتوصيات المنتج، تحتاج إلى نشر ملحق العرض التوضيحي للمعاينة لـ Dynamics 365 Commerce للبيئة المعينة. يؤدي ذلك إلى تمكين بيانات العرض التوضيحي لتوصيات المنتج تلقائيًا.

## <a name="default-demo-data"></a>بيانات العرض التوضيحي الافتراضية
تأتي كل بيئة من النوع OneBox مع مجموعة من بيانات العرض التوضيحي لتوصيات المنتج التي تم تحميلها مسبقًا من ملف ‘reco_demo_data.csv’ المفصول بوسطة فاصلة، والموجود في Commerce Scale Unit.

يتم هيكلة هذه البيانات بمحاذاة الأعمده التالية.

| اسم العمود         | إلزامي          | ‏‏الوصف                                                                                                                                 | القيم المحتملة                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| RecoList            | :heavy_check_mark: | إنشاء نوع قائمة توصيات المنتج المحدد التي تشير إليها بيانات العرض التوضيحي منها.                                                    | <ul><li>RecoBestSelling</li><li>RecoNew</li><li>RecoTrending</li><li>RecoCart</li><li>RecoPeopleAlsoBuy</li><li>RecoPicks</li><li>RecoSimilarVisual</li><li>RecoSimilarTextual</li></ul> |
| OperatingUnitNumber | :heavy_check_mark: | رقم وحدة التشغيل المحددة التي يُتوقع ظهور توصيات المنتج لها.                                        |                                                                              |
| فئة            |                    |    الفئة التي يجب أن يتم إرجاع القائمة المحددة إليها. في حالة عدم تحديد أية فئة، تكون القائمة أعلى ‏‫التدرج الهرمي للتنقل فقط.    |                                                                              |
| SeedItemId          |                    |    بالنسبة للقوائم التي تتطلب إضافة (RecoPeopleAlsoBuy وRecoCart) المنتج، يجب أن تعرض هذه القوائم منتجات إضافية.            |                                                                              |
| معرف العميل          |                    |    للقوائم التي تتطلب معرف عميل (RecoPicks).  تنطبق القيمة الافتراضية '0' على كافة العملاء.          |                                                                              |
| ItemIds             | :heavy_check_mark: | إرجاع منتج أو أكثر كنتيجة، مفصول بواسطة ';'.                                                                  |                                                                              |

## <a name="customize-demo-data"></a>تخصيص بيانات العرض التوضيحي
يمكنك تحرير بيانات العرض التوضيحي الافتراضية بآيه معلومات حول المنتج والفئة التي تم تكوينها في HQ. بعد تحديث ملف CSV.، تعكس توصيات المنتج التي يتم إرجاعها للعملاء التغييرات مباشرة.

يحتوي الملحق على ملف بيانات يسمي 'RecoMockDataset.csv'، يسمح لك بالتحكم في مجموعة البيانات المستخدمة لتشغيل نتائج توصيات وهمية. يمكن التحكم في اسم الملف من خلال تكوين الملحق باستخدام إعداد **ext.Recommendations.DemoFilePath** . ويؤدي ذلك إلى تمكينك من جعل مجموعات البيانات المتعددة متاحة ويمكن التبديل بينها بسهولة خل التكوين.


```xml
<settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
</settings>
```

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على توصيات المنتجات](product-recommendations.md)

[تمكين Azure Data Lake Storage في بيئة Dynamics 365 Commerce](enable-adls-environment.md)

[تمكين توصيات المنتجات](enable-product-recommendations.md)

[تمكين التوصيات المخصصة](personalized-recommendations.md)

[إلغاء الاشتراك في التوصيات المخصصة](personalization-gdpr.md)

[تمكين توصيات "تسوق منتجات تبدو مماثلة"](shop-similar-looks.md)

[إضافة توصيات المنتجات على نقطة البيع](product.md)

[إضافة توصيات إلى شاشة المعاملة](add-recommendations-control-pos-screen.md)

[إدارة نتائج توصيات الذكاء الاصطناعي والتعلم الآلي (AI-ML)](modify-product-recommendation-results.md)

[إنشاء توصيات مختارة يدويًا](create-editorial-recommendation-lists.md)

[الأسئلة المتداولة حول توصيات المنتجات](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
