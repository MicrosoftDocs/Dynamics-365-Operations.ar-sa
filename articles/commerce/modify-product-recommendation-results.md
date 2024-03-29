---
title: ضبط نتائج توصيات المنتجات المستندة إلى AI-ML
description: يوضح هذا المقال كيفية نفصيل نتائج توصيات المنتج التي تستند إلى التعلم الآلي القائم على الذكاء الاصطناعي (AI-ML) مع احتياجات أعمالك.
author: bebeale
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: d74fa013d44e0f113bdf0ce0ca9efeb943926e9f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901692"
---
# <a name="adjust-ai-ml-based-product-recommendation-results"></a>ضبط نتائج توصيات المنتجات المستندة إلى AI-ML


[!include [banner](includes/banner.md)]

يوضح هذا المقال كيفية ضبط نتائج توصيات المنتج التي تستند إلى التعلم الآلي القائم على الذكاء الاصطناعي (AI-ML) بحيث تتلاءم مع احتياجات أعمالك. 

بعد تمكين توصيات المنتج، ستصبح الإعدادات الافتراضية نافذة المفعول؛ أي أن هذه المعلمات ستؤدي دورها لتلبية العديد من الاحتياجات. من الأفضل التخطيط لقضاء بعض الوقت في تقييم ما إذا كانت النتائج تناسب حركه بيع المنتجات أم لا. نقترح عليك تقييم النتائج لأيام قليلة قبل تغيير المعلمات حسب الحاجة قبل الاختبار مرة أخرى. 

## <a name="understanding-recommendation-list-parameters"></a>فهم معلمات قائمة التوصيات

قبل تغيير المعلمات، تعرف على كيفية تأييرها على النتائج أدناه.

### <a name="trending-product-list"></a>فرز منتج التداول

تحتوي قائمة منتجات "التداول" على معلمتين يمكن تغييرهما:

![مثال للمعلمات الافتراضية لقائمة "التداول"](./media/exampletrendingparameters.png)

1. **تضمين منتجات جديدة من آخر X يوم/أيام**- المنتجات التي تمت إضافتها خلال عدد محدد من الأيام قبل إمكانية استخدام التاريخ الحالي لتحديد مرشحي المنتج. تقترح القيمة الافتراضية في الصورة أن المنتجات القديمة التي لها 180 يومًا يمكن استخدامها في قائمة المنتجات المتداولة.
1. **تضمين منتجات جديدة من آخر X يوم/أيام**- المنتجات التي تمت إضافتها خلال عدد محدد من الأيام قبل إمكانية استخدام التاريخ الحالي لطلب المنتجات. تقترح القيمة الافتراضية المذكورة أعلاه أن كافة عمليات الشراء التي تم اجراؤها لأحد المنتجات في آخر 30 يومًا سيتم استخدامها لتحديد موضع المنتج في قائمة المنتجات المتداولة. 

### <a name="best-selling-product-list"></a>قائمة المنتجات "الأفضل مبيعًا"

بناء على أعمالك، تجلب قائمة المنتجات "الأفضل مبيعا" نتائج مختلفة عن المتداول، على الرغم من أنهما يستخدمان بيانات الحركة لطلب المنتجات. ونظرًا لأن المنتجات الأفضل مبيعا ليس لها تاريخ انقطاع استنادا إلى تاريخ الفرز، فإنها تظل تميز المنتجات الشائعة جدًا؛ المنتجات الأقدم التي ربما تم إسقاطها من القائمة المتداولة. 

تحتوي قائمة منتجات "الأفضل مبيعًا" على معلمة واحدة يمكن تغييرها:

![مثال: المعلمة الافتراضية لقائمة منتجات الأفضل مبيعًا.](./media/examplebestsellingparameters.PNG)

1. **تضمين منتجات جديدة من آخر X يوم/أيام**- المنتجات التي تمت إضافتها خلال عدد محدد من الأيام قبل إمكانية استخدام التاريخ الحالي لطلب المنتجات. تقترح القيمة الافتراضية المذكورة أعلاه أن كافة عمليات الشراء التي تم اجراؤها لأحد المنتجات في آخر 30 يومًا سيتم استخدامها لتحديد موضع المنتج في قائمة المنتجات الأفضل مبيعا. 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a>إضافة منتجات أو ازالتها يدويًا من قوائم التوصيات

### <a name="for-new-trending-or-best-selling-lists"></a>بالنسبة لقوائم المنتجات الجديدة أو المتداولة أو الأفضل مبيعاً

1.  انتقل إلى **البيع بالتجزئة والتجارة** > **توصيات المنتج** > **معلمات التوصية**.
1.  في قائمة المعلمات المشتركة، حدد **قوائم التوصيات**.
1.  حدد القائمة التي تريد إضافة أو إزالة منتجات منها.
1.  لإضافة منتجات إلى الجدول، حدد **إضافة بند**. 
1.  ضمن عمود المنتج، ابحث عن منتج حسب **الاسم** أو **رقم المنتج**.

    ![أمثله للبحث عن منتج في قائمة المنتجات الجديدة.](./media/examplenewlistconfiguration1.png)

1.  أسفل عمود نوع البند، حدد خيار من خيارين:
    -   **تضمين** -فرض وجود المنتج في مقدمة القائمة
    -   **استبعاد** – إزالة منتج من الظهور في القائمة
    
    ![مثال على تضمين منتج أو استبعاده من قائمة المنتجات الجديدة.](./media/examplenewlistconfiguration2.png)

1.  سيؤدي تغيير **ترتيب العرض** إلى تغيير الترتيب الذي تظهر المنتجات عنده معلمة كـ **تضمين** في القائمة.
    - إذا كان لمنتجين نفس قيمة **ترتيب العرض**، فقد يختلف الترتيب النهائي لهاتين النتيجتين عن مكتب الدعم.
1.  لإزالة منتجات من الجدول: حدد البند المراد إزالته وحدد **إزالة**.


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a>بالنسبة للقائمتين "أشخاص معجبون به أيضًا‬‏‫" أو "الأغراض التي يتم شراؤها معًا كثيرا"

في سياق قائمة الأغراض التي يتم شراؤها معًا كثيرًا أو قائمة أشخاص معجبون به أيضًا، يتم استخدام تعلم الآلة لتحليل أنماط الشراء الخاصة بالمستهلك للتوصية بالمنتجات المرتبطة التي يتم شراؤها معًا بشكل متكرر لمنتج أساسي فريد. 
 
*المنتج الأساسي* هو المنتج الذي ترغب في إنشاء نتائج له. في سياق ضبط قوائم التوصيات يدويًا، تقوم بإضافة نتائج لهذا المنتج أو إزالتها. 

اتبع هذه الخطوات لإضافة نتائج لمنتج أساسي أو إزالتها يدويًا:
1.  حدد **المنتج الأساسي**. 
1.  أسفل عمود **المنتج**، ابحث عن المنتج حسب **الاسم** أو **رقم المنتج**
![مثال للبحث عن منتج في قائمة الأغراض التي يتم شراؤها معًا كثيرًا‬.](./media/exampleFBTlistconfiguration1.png)
1. أسفل عمود **نوع البند**، حدد خيار من خيارين:
    - **تضمين** -فرض وجود المنتج في مقدمة القائمة
    - **استبعاد** – إزالة منتج من الظهور في القائمة     
![مثال لتضمين أو استبعاد منتج في قائمة الأغراض التي يتم شراؤها معًا كثيرًا‬.](./media/exampleFBTlistconfiguration2.png)
1.  لإزالة منتجات من الجدول: حدد البند المراد إزالته وحدد إزالة.


## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على توصيات المنتجات](product-recommendations.md)

[تمكين Azure Data Lake Storage في بيئة Dynamics 365 Commerce](enable-adls-environment.md)

[تمكين توصيات المنتجات](enable-product-recommendations.md)

[تمكين التوصيات المخصصة](personalized-recommendations.md)

[إلغاء الاشتراك في التوصيات المخصصة](personalization-gdpr.md)

[تمكين توصيات "تسوق منتجات تبدو مماثلة"](shop-similar-looks.md)

[إضافة توصيات المنتجات على نقطة البيع](product.md)

[إضافة توصيات إلى شاشة المعاملة](add-recommendations-control-pos-screen.md)

[إنشاء توصيات مختارة يدويًا](create-editorial-recommendation-lists.md)

[إنشاء توصيات بواسطة بيانات العرض التوضيحي](product-recommendations-demo-data.md)

[الأسئلة المتداولة حول توصيات المنتجات](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]