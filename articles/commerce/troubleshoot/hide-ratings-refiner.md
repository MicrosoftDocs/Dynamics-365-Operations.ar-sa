---
title: تظهر "مدقق التصنيفات" على نتائج البحث وصفحات الفئات عند عدم تمكين حل التقييمات والمراجعات
description: يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها حول كيفية إخفاء مدقق التصنيفات في صفحات نتائج البحث والفئات عند عدم تمكين حل التقييمات والمراجعات في Microsoft Dynamics 365 Commerce لأحد مواقع التجارة الإلكترونية.
author: gvrmohanreddy
manager: annbe
ms.date: 09/02/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: f3438d12f4ffd06b07cbef724cda8fa490a5f4eb
ms.sourcegitcommit: d420b96d37093c26f0e99c548f036eb49a15ec30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/03/2021
ms.locfileid: "7472563"
---
# <a name="ratings-refiner-appears-on-search-results-and-category-pages-when-the-ratings-and-reviews-solution-isnt-enabled"></a>تظهر "مدقق التصنيفات" على نتائج البحث وصفحات الفئات عند عدم تمكين حل التقييمات والمراجعات

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها حول كيفية إخفاء مدقق التصنيفات في صفحات نتائج البحث والفئات عند عدم تمكين حل التقييمات والمراجعات في Microsoft Dynamics 365 Commerce لأحد مواقع التجارة الإلكترونية.

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
