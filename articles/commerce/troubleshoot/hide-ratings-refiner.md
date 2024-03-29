---
title: تظهر "مدقق التصنيفات" على نتائج البحث وصفحات الفئات عند عدم تمكين حل التقييمات والمراجعات
description: يوفر هذا المقال إرشادات استكشاف الأخطاء وإصلاحها حول كيفية إخفاء مدقق التصنيفات في صفحات نتائج البحث والفئات عند عدم تمكين حل التقييمات والمراجعات في Microsoft Dynamics 365 Commerce لأحد مواقع التجارة الإلكترونية.
author: gvrmohanreddy
ms.date: 09/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.22
manager: annbe
ms.openlocfilehash: 28a3cefd6aab81f5e7907bda457763f2306e5a1d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267367"
---
# <a name="ratings-refiner-appears-on-search-results-and-category-pages-when-the-ratings-and-reviews-solution-isnt-enabled"></a>تظهر "مدقق التصنيفات" على نتائج البحث وصفحات الفئات عند عدم تمكين حل التقييمات والمراجعات

[!include [banner](../includes/banner.md)]

يوفر هذا المقال إرشادات استكشاف الأخطاء وإصلاحها حول كيفية إخفاء مدقق التصنيفات في صفحات نتائج البحث والفئات عند عدم تمكين حل التقييمات والمراجعات في Microsoft Dynamics 365 Commerce لأحد مواقع التجارة الإلكترونية.

## <a name="description"></a>الوصف

يظهر مدقق التصنيفات في صفحات نتائج البحث والفئات في قناة التجارة الإلكترونية التي لا تستخدم حل التقييمات والمراجعات.

## <a name="resolution"></a>الحل

### <a name="enable-the-hide-rating-setting-in-commerce-site-builder"></a>تمكين إعداد إخفاء التصنيف في منشئ موقع التجارة

لتمكين إعداد **إخفاء التصنيف** في منشئ المواقع التجارية، حتى يتم إخفاء مدقق التصنيفات في "نتائج البحث" و"صفحات الفئات"، اتبع الخطوات التالية.

1. انتقل إلى **إعدادات الموقع \> الملحقات**.
1. ضمن **التصنيفات والمراجعات**، حدد خانة الاختيار **إخفاء التقييم**.
1. حدد **حفظ ونشر**.

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على التقييمات والمراجعات](../ratings-reviews-overview.md)

[الموافقة على استخدام التقييمات والمراجعات](../opt-in-ratings-reviews.md)
