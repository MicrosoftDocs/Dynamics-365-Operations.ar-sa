---
title: بيانات العرض التوضيحي لتوصيات منتج القناة متعددة الاتجاهات
description: يهدف هذا المستند إلى توفير إرشادات حول كيفية الاستفادة من توصيات المنتج متعدد القنوات في بيئات مربعات فردية بمستوى 1 باستخدام بيانات العرض التوضيحي المعممة مسبقا.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 81af4c1bb7828c9b346a3ef514d8657e853dcefb
ms.sourcegitcommit: c526cfd1f823df1ff33ded95e599a72f0a15cc5a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2225541"
---
# <a name="omni-channel-product-recommendations-demo-data"></a>بيانات العرض التوضيحي لتوصيات منتج القناة متعددة الاتجاهات

يهدف هذا المستند إلى توفير إرشادات حول كيفية الاستفادة من توصيات المنتج متعدد القنوات في بيئات مربعات فردية بمستوى 1 باستخدام بيانات العرض التوضيحي المعممة مسبقا.

توفر توصيات المنتج متعدد القنوات مجموعة من قوائم المنتجات المرتبة والتي تم إنشاؤها بشكل تحريري أو برمجيًا. يمكن استخدام هذه القوائم في العديد من السيناريوهات، وفقًا لاحتياجات العمل. لمزيد من المعلومات حول قوائم توصيات المنتجات، راجع [نظرة عامة على توصيات المنتجات.](product-recommendaitons-overview.md)

بالنسبة لبيئات المنتجات من المستوي 2 وما أعلي، تُحتسب توصيات منتج البيئات الديناميكية تلقائيًا بناء علي بيانات العملاء.
لا يؤدي استخدام البيانات التوضيحية لتوصيات المنتج إلى تعطيل اي حل توصيات للمنتج تم توفيرها بالفعل في البيئة وآية تكاليف مرتبطة باستخدامها.

بالنسبة لبيئات المستوي 1، تستند توصيات المنتج فقط على بيانات العرض التوضيحي الثابتة المخزنة في ملف csv.

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a>تمكين بيانات العرض التوضيحي لتوصيات المنتج في البيئة

يحتاج العملاء إلى نشر **Dynamics 365 Commerce ملحق العرض التوضيحي للمعاينة** للبيئة المعنية، التي تمكن بيانات العرض التوضيحي لتوصيات المنتج تلقائيًا.

## <a name="default-demo-data"></a>بيانات العرض التوضيحي الافتراضية
تأتي كل بيئة من النوع Onebox مع مجموعه من بيانات العرض التوضيحي لتوصيات المنتج التي تم تحميلها مسبقًا من ملف **‘reco_demo_data.csv’** المفصول بالنقاط، والموجود في نفس مجلد هذا المستند علي خادم Retail.

يتم هيكلة هذه البيانات بمحاذاة الاعمده التالية

| اسم العمود         | إلزامي          | ‏‏الوصف                                                                                                                                 | القيم المحتملة                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| RecoList            | :heavy_check_mark: | إنشاء نوع قائمه توصيات المنتج المحدد التي تشير إليها بيانات العرض التوضيحي منها.                                                    | <ul><li>RecoBestSelling</li><li>RecoNew</li><li>RecoTrending</li><li>RecoCart</li><li>RecoPeopleAlsoBuy</li></ul> |
| OperatingUnitNumber | :heavy_check_mark: | رقم وحدة التشغيل المحددة التي يُتوقع ظهور توصيات المنتج لها.                                        |                                                                              |
| فئة            |                    |    الفئة التي يجب أن يتم إرجاع القائمة المحددة إليها. في حالة عدم تحديد أية فئة، تكون القائمة أعلى ‏‫التدرج الهرمي للتنقل فقط.    |                                                                              |
| SeedItemId          |                    |    بالنسبة للقوائم التي تتطلب إضافة (RecoPeopleAlsoBuy وRecoCart) المنتج، يجب أن تعرض هذه القوائم منتجات إضافية.            |                                                                              |
| ItemIds             | :heavy_check_mark: | وكنتيجة إذا تم إرجاع واحد أو أكثر من المنتجات، يتم الفصل بينهم بالعمة **‘;’**.                                                                  |                                                                              |


## <a name="customize-demo-data"></a>تخصيص بيانات العرض التوضيحي
يمكن للعملاء تحرير بيانات العرض التوضيحي الافتراضية بآيه معلومات حول المنتج والفئة التي تم تكوينها في HQ. بمجرد تحديث الملف CSV، تعكس توصيات المنتج التي يتم إرجاعها للعملاء التغييرات مباشرة.

يحتوي الملحق علي ملف بيانات يسمي RecoMockDataset.csv والذي يسمح للعميل بالتحكم في مجموعه البيانات المستخدمة لتشغيل نتائج توصيات وهمية. يمكن التحكم في اسم الملف من خلال تكوين الملحق باستخدام إعداد **ext.Recommendations.DemoFilePath** . ويؤدي ذلك إلى تمكين العملاء من جعل مجموعات البيانات المتعددة متاحة ويمكن التبديل بينها بسهولة خل التكوين.

```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على توصيات المنتجات](product-recommendations-overview.md)

[تخطيط بيئة](environment-planning.md)