---
title: نظرة عامة على توصيات المنتجات
description: يوفر هذا المقال معلومات عامة حول توصيات المنتج. تسمح توصيات المنتجات للعملاء بالبحث عن المنتجات التي يريدونها بسهولة وسرعة، وحتى المنتجات التي لم يرغبون بشراءها.
author: Moonma
ms.date: 05/26/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2cb62638e89dd9cd7c01739244d808f664b3f3b1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867722"
---
# <a name="product-recommendations-overview"></a>نظرة عامة على توصيات المنتجات

[!include [banner](includes/banner.md)]

يمكن استخدام تطبيق Microsoft Dynamics 365 Commerce لعرض توصيات المنتجات على موقع التجارة الإلكترونية و جهاز نقطة البيع (POS).‬ توصيات المنتجات هي الأصناف التي قد يهتم بها العميل. وتعتمد التوصيات على اتجهات الشراء للعملاء الآخرين في المتاجر التقليدية أو المتاجر الأخرى على الإنترنت .

تسمح توصيات المنتجات للعملاء بالعثور بسهولة وسرعة عن المنتجات التي يرغبون في الحصول عليها مع الاستمتاع بتجربة مفيدة. يمكن استخدام البيع التكميلي والإضافي‬ لمساعدة العملاء في العثور على المنتجات الإضافية التي لم يكن لديهم النية في شرائها في الأصل. عند استخدام التوصيات لتحسين اكتشاف المنتج، يمكنها إنشاء المزيد من فرص التحويل، والمساعدة على زيادة عائد المبيعات، وحتى زيادة مستوى رضا العميل والاحتفاظ به.

في التجارة الإلكترونية، يتم تشغيل توصيات المنتجات بواسطة تقنيات التعلم الآلي لتوصيات Microsoft على نطاق واسع.

تعد هذه الخدمة وظيفة إضافية إلى Dynamics 365 Commerce. لمزيد من المعلومات، قم بتنزيل [دليل ترخيص Microsoft Dynamics 365 الأخير](https://go.microsoft.com/fwlink/?LinkId=866544).


## <a name="recommendation-service"></a>خدمة التوصيات

تستخدم خدمه توصيات المنتجات تقنيات الذكاء الاصطناعي والتعلم الآلي (AI-ML) بالطريقة التالية:

- يتم استخراج البيانات بالتنسيق المطلوب من خلال خدمة التوصيات من قاعدة البيانات التشغيلية في تطبيق Commerce ويتم إرسالها إلى Azure Data Lake Storage أو مخزن الكيانات.
- تستخدم خدمة التوصيات البيانات المخزنة لتدريب نماذج التوصيات للقوائم ‫‬‏‫**أشخاص معجبون به أيضًا‬‏‫**، و **الأغراض التي يتم شراؤها معًا كثيرًا**‬‏‫ و **جديد** و **الأفضل مبيعًا**‬‏‫ و **المتداول**.

## <a name="scenarios"></a>السيناريوهات

يتم توفير توصيات المنتج للسيناريوهات التالية:

- **في أي صفحة من صفحات المتجر للاستعراض أو للصفحة المنتقل اليها في التجارة الإلكترونية:** إذا كان العملاء أو شركاء المتجر يزورون إحدى صفحات المتجر، فيمكن لمحرك التوصيات اقتراح المنتجات في القوائم **جديد**، و **الأكثر مبيعًا**، و **المتداول**.
- **في صفحة تفاصيل المنتج:** إذا كان العملاء أو شركاء المتجر يزورون صفحة **تفاصيل المنتج**، يقوم جهاز التوصيات باقتراح الأصناف الإضافية التي غالبًا ما يتم شراؤها. تظهر هذه الأصناف في قائمة **‬‏‫أشخاص معجبون به أيضًا**.
- **في صفحة الحركة أو صفحة السداد مع الخروج:** يقوم محرك التوصيات باقتراح الأصناف، استنادا إلى إجمالي قائمة الأصناف في السلة. تظهر هذه الأصناف في قائمة **الأغراض التي يتم شراؤها معًا كثيرًا**.
- **التوصيات المخصصة:** يمكن للتجار تزويد العملاء الذين سجلوا الدخول بقائمة **العناصر المقترحة لك**، بالإضافة إلى الوظائف الجديدة التي تسمح بتخصيص وحدات سيناريو القائمة الموجودة استنادا إلى هذا العميل. لمعرفة المزيد، راجع [تمكين التوصيات المخصصة.](personalized-recommendations.md).

### <a name="types-of-product-recommendations"></a>أنواع توصيات المنتجات

يصف الجدول التالي مختلف أنواع توصيات المنتجات التلقائية المتوفرة لبائعي التجزئة لتنفيذها في حل Dynamics 365 Commerce عبر [الوحدة النمطية مجموعة منتجات‬](product-collection-module-overview.md). بإمكان بائعي التجزئة أيضًا عرض النتائج المخصصة لمستخدم سجل دخوله إذا اختار مؤلف الموقع هذا الخيار.

| الوحدة النمطية لمجموعة المنتجات  | النوع | ‏‏الوصف |
|----------------------------|------|-------------|
| القيمة الجديدة                        | حسابي | تعرض هذه الوحدة قائمة بأحدث المنتجات التي تم تصنيفها مؤخرًا إلى القنوات والكتالوجات. |
| الأعلى مبيعًا               | حسابي | تعرض هذه الوحدة النمطية قائمة بالمنتجات التي تم تصنيفها حسب أعلى عدد من المبيعات. |
| المتصدر                   | حسابي | تعرض هذه الوحدة قائمة بالمنتجات ذات الأداء الأعلى لفترة معينة، وقد تم ترتيبها حسب أعلى رقم مبيعات.  |
| منتجات يتكرر شراؤها معًا | AI-ML | توصي هذه الوحدة النمطية بقائمة المنتجات التي يتم عادة شراؤها مع محتويات سلة التسوق الحالية للعملاء. |
| أعجب الأشخاص أيضًا بـ           | AI-ML | توصي هذه الوحدة النمطية بمنتجات لمنتج أولي معين استنادًا إلى أنماط الشراء لدى العميل. |
| العناصر المقترحة              | AI-ML | توصي هذه الوحدة النمطية بقائمة مخصصة للمنتجات استنادًا إلى أنماط الشراء الخاصة بالمستخدم الذي سجل دخوله. بالنسبة لمستخدم ضيف، سيتم طي هذه القائمة. |

## <a name="additional-resources"></a>الموارد الإضافية

[تمكين Azure Data Lake Storage في بيئة Dynamics 365 Commerce](enable-adls-environment.md)

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
