---
title: الميزات التي تمت إزالتها أو إهمالها في Dynamics 365 Commerce
description: يصف هذا الموضوع الميزات التي تمت إزالتها أو تلك المخطط لإزالتها من Dynamics 365 Commerce.
author: josaw
manager: AnnBe
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: c47c5430a8f5d67e13c95db609a95d5ad66933ae
ms.sourcegitcommit: a8b6cd799eddaf5be9aec9ea3c2b55e2c3231652
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/05/2020
ms.locfileid: "3335266"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>الميزات التي تمت إزالتها أو إهمالها في Dynamics 365 Commerce

[!include [banner](../includes/banner.md)]

يصف هذا الموضوع الميزات التي تمت إزالتها أو تلك المخطط لإزالتها من Dynamics 365 Commerce.

- لم تعد ميزة *تمت الإزالة* متوفرة في المنتج.
- لا توجد ميزة *المهملة* في التطوير النشط وقد يتم إزالتها في تحديثات مستقبلية.

تهدف هذه القائمة إلى مساعدتك في مراعاة ميزات الإزالة وعمليات الإهلاك للتخطيط الخاص بك. 

> [!NOTE]
> يمكن العثور على معلومات مفصلة حول الكائنات في تطبيقات Finance and Operations [التقارير المرجعية التقنية](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). يمكنك مقارنة إصدارات مختلفة من هذه التقارير لمعرفة المزيد حول الكائنات التي تم تغييرها أو التي تمت إزالتها من كل إصدار من تطبيقات Finance and Operations.

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a>ميزات تمت إزالتها أو إهمالها في الإصدار 10.0.10 من Commerce
### <a name="pos-operation-803---picking-and-receiving"></a>عملية نقطة البيع 803 - الانتقاء والاستلام
|   |  |
|------------|--------------------|
| **سبب الإهلاك/الإزالة** | جارٍ إهمال عمليات الانتقاء والاستلام نظرا لإعاده التصميم الجديد للعملية. |
| **هل تم الاستبدال بميزة أخرى؟**   | نعم. ويتم استبدالها بعمليتي POS جديدتين: العملية الداخلية (804) والعملية الخارجية (805).|
| **مناطق المنتجات المتأثرة**         | تطبيق نقطة البيع (POS) |
| **خيارات النشر**              | ‏‏الكل |
| **الحالة**                         | مهمل: بدءًا من الإصدار 10.0.10، لن تتلقي عملية الانتقاء والاستلام إيه تحديثات لميزات جديدة. سيتم اجراء إصلاحات الأخطاء الهامه فقط لهذه العملية في الإصدارات المستقبلية. ويتم تشجيع كافة العملاء علي الانتقال إلى [العمليات الداخلية](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) و [العمليات الخارجية](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation)، والتي ستستمر في أن تكون جزءا من مخطط المنتج طويل الأجل. |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a>ميزات تمت إزالتها أو إهمالها في الإصدار 10.0.7 من Commerce
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a>واجهات API لـ Commerce GetProductAvailabilities و GetAvailableInventoryNearby
|   |  |
|------------|--------------------|
| **سبب الإهلاك/الإزالة** | تم إنشاء واجهة API محسّنة جديدة لتحل محل واجهات برمجة التطبيقات GetProductAvailabilities و GetAvailableInventoryNearby. |
| **هل تم الاستبدال بميزة أخرى؟**   | نعم: يتم استبداله بواجهات GetEstimatedAvailabilty وGetEstimatedProductWarehouseAvailability. |
| **مناطق المنتجات المتأثرة**         | SDK لتطبيق التجارة الإلكترونية |
| **خيارات النشر**              | ‏‏الكل |
| **الحالة**                         | مهمل: بدءا من الإصدار 10.0.7 ، لن يكون هناك استثمارات هندسية لـ GetProductAvailabilities وGetAvailableInventoryNearby. يجب تحويل المؤسسات التي تستخدم واجهات برمجه التطبيقات (APIs) هذه في عمليات توزيع التجارة الإلكترونية إلى واجهات برمجة تطبيقات GetEstimatedAvailabilty وGetEstimatedProductWarehouseAvailability الجديدة وتمكين [ميزة حساب إتاحة المنتج المحسنة](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>الإعلانات السابقة حول الميزات التي تمت إزالتها أو إهمالها
لمعرفه المزيد حول الميزات التي تمت إزالتها أو إهمالها في الإصدارات السابقة، راجع [‏‫الميزات التي تمت إزالتها أو إهمالها في الإصدارات السابقة‬](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).
