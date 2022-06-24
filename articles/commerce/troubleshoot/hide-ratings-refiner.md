---
title: تظهر "مدقق التصنيفات" على نتائج البحث وصفحات الفئات عند عدم تمكين حل التقييمات والمراجعات
description: يوفر هذا المقال إرشادات استكشاف الأخطاء وإصلاحها حول كيفية إخفاء مدقق التصنيفات في صفحات نتائج البحث والفئات عند عدم تمكين حل التقييمات والمراجعات في Microsoft Dynamics 365 Commerce لأحد مواقع التجارة الإلكترونية.
author: gvrmohanreddy
manager: annbe
ms.date: 09/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: c35e176fc5673de194a81a3a4694a83f7bc9aa00
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885048"
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
