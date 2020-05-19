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
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a><span data-ttu-id="7fbef-103">الميزات التي تمت إزالتها أو إهمالها في Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="7fbef-103">Removed or deprecated features in Dynamics 365 Commerce</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7fbef-104">يصف هذا الموضوع الميزات التي تمت إزالتها أو تلك المخطط لإزالتها من Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7fbef-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Commerce.</span></span>

- <span data-ttu-id="7fbef-105">لم تعد ميزة *تمت الإزالة* متوفرة في المنتج.</span><span class="sxs-lookup"><span data-stu-id="7fbef-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="7fbef-106">لا توجد ميزة *المهملة* في التطوير النشط وقد يتم إزالتها في تحديثات مستقبلية.</span><span class="sxs-lookup"><span data-stu-id="7fbef-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="7fbef-107">تهدف هذه القائمة إلى مساعدتك في مراعاة ميزات الإزالة وعمليات الإهلاك للتخطيط الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="7fbef-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="7fbef-108">يمكن العثور على معلومات مفصلة حول الكائنات في تطبيقات Finance and Operations [التقارير المرجعية التقنية](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="7fbef-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="7fbef-109">يمكنك مقارنة إصدارات مختلفة من هذه التقارير لمعرفة المزيد حول الكائنات التي تم تغييرها أو التي تمت إزالتها من كل إصدار من تطبيقات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7fbef-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a><span data-ttu-id="7fbef-110">ميزات تمت إزالتها أو إهمالها في الإصدار 10.0.10 من Commerce</span><span class="sxs-lookup"><span data-stu-id="7fbef-110">Features removed or deprecated in the Commerce 10.0.10 release</span></span>
### <a name="pos-operation-803---picking-and-receiving"></a><span data-ttu-id="7fbef-111">عملية نقطة البيع 803 - الانتقاء والاستلام</span><span class="sxs-lookup"><span data-stu-id="7fbef-111">POS operation 803 - Picking and receiving</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="7fbef-112">**سبب الإهلاك/الإزالة**</span><span class="sxs-lookup"><span data-stu-id="7fbef-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="7fbef-113">جارٍ إهمال عمليات الانتقاء والاستلام نظرا لإعاده التصميم الجديد للعملية.</span><span class="sxs-lookup"><span data-stu-id="7fbef-113">Picking and receiving operations is being deprecated due to new operation redesign.</span></span> |
| <span data-ttu-id="7fbef-114">**هل تم الاستبدال بميزة أخرى؟**</span><span class="sxs-lookup"><span data-stu-id="7fbef-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="7fbef-115">نعم.</span><span class="sxs-lookup"><span data-stu-id="7fbef-115">Yes.</span></span> <span data-ttu-id="7fbef-116">ويتم استبدالها بعمليتي POS جديدتين: العملية الداخلية (804) والعملية الخارجية (805).</span><span class="sxs-lookup"><span data-stu-id="7fbef-116">It is replaced by two new POS operations: inbound operation (804) and outbound operation (805).</span></span>|
| <span data-ttu-id="7fbef-117">**مناطق المنتجات المتأثرة**</span><span class="sxs-lookup"><span data-stu-id="7fbef-117">**Product areas affected**</span></span>         | <span data-ttu-id="7fbef-118">تطبيق نقطة البيع (POS)</span><span class="sxs-lookup"><span data-stu-id="7fbef-118">Point of sale (POS) application</span></span> |
| <span data-ttu-id="7fbef-119">**خيارات النشر**</span><span class="sxs-lookup"><span data-stu-id="7fbef-119">**Deployment option**</span></span>              | <span data-ttu-id="7fbef-120">‏‏الكل</span><span class="sxs-lookup"><span data-stu-id="7fbef-120">All</span></span> |
| <span data-ttu-id="7fbef-121">**الحالة**</span><span class="sxs-lookup"><span data-stu-id="7fbef-121">**Status**</span></span>                         | <span data-ttu-id="7fbef-122">مهمل: بدءًا من الإصدار 10.0.10، لن تتلقي عملية الانتقاء والاستلام إيه تحديثات لميزات جديدة.</span><span class="sxs-lookup"><span data-stu-id="7fbef-122">Deprecated: As of release 10.0.10, the picking and receiving operation will no longer receive any new feature updates.</span></span> <span data-ttu-id="7fbef-123">سيتم اجراء إصلاحات الأخطاء الهامه فقط لهذه العملية في الإصدارات المستقبلية.</span><span class="sxs-lookup"><span data-stu-id="7fbef-123">Only critical bug fixes will be done for this operation in future releases.</span></span> <span data-ttu-id="7fbef-124">ويتم تشجيع كافة العملاء علي الانتقال إلى [العمليات الداخلية](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) و [العمليات الخارجية](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation)، والتي ستستمر في أن تكون جزءا من مخطط المنتج طويل الأجل.</span><span class="sxs-lookup"><span data-stu-id="7fbef-124">All customers are encouraged to move to the new [Inbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) and [Outbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), which will continue to be part of our long-term product roadmap.</span></span> |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a><span data-ttu-id="7fbef-125">ميزات تمت إزالتها أو إهمالها في الإصدار 10.0.7 من Commerce</span><span class="sxs-lookup"><span data-stu-id="7fbef-125">Features removed or deprecated in the Commerce 10.0.7 release</span></span>
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a><span data-ttu-id="7fbef-126">واجهات API لـ Commerce GetProductAvailabilities و GetAvailableInventoryNearby</span><span class="sxs-lookup"><span data-stu-id="7fbef-126">Commerce GetProductAvailabilities and GetAvailableInventoryNearby API's</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="7fbef-127">**سبب الإهلاك/الإزالة**</span><span class="sxs-lookup"><span data-stu-id="7fbef-127">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="7fbef-128">تم إنشاء واجهة API محسّنة جديدة لتحل محل واجهات برمجة التطبيقات GetProductAvailabilities و GetAvailableInventoryNearby.</span><span class="sxs-lookup"><span data-stu-id="7fbef-128">New optimized APIs have been created to replace the GetProductAvailabilities and GetAvailableInventoryNearby APIs.</span></span> |
| <span data-ttu-id="7fbef-129">**هل تم الاستبدال بميزة أخرى؟**</span><span class="sxs-lookup"><span data-stu-id="7fbef-129">**Replaced by another feature?**</span></span>   | <span data-ttu-id="7fbef-130">نعم: يتم استبداله بواجهات GetEstimatedAvailabilty وGetEstimatedProductWarehouseAvailability.</span><span class="sxs-lookup"><span data-stu-id="7fbef-130">Yes: It is replaced by GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs.</span></span> |
| <span data-ttu-id="7fbef-131">**مناطق المنتجات المتأثرة**</span><span class="sxs-lookup"><span data-stu-id="7fbef-131">**Product areas affected**</span></span>         | <span data-ttu-id="7fbef-132">SDK لتطبيق التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="7fbef-132">e-Commerce application SDK</span></span> |
| <span data-ttu-id="7fbef-133">**خيارات النشر**</span><span class="sxs-lookup"><span data-stu-id="7fbef-133">**Deployment option**</span></span>              | <span data-ttu-id="7fbef-134">‏‏الكل</span><span class="sxs-lookup"><span data-stu-id="7fbef-134">All</span></span> |
| <span data-ttu-id="7fbef-135">**الحالة**</span><span class="sxs-lookup"><span data-stu-id="7fbef-135">**Status**</span></span>                         | <span data-ttu-id="7fbef-136">مهمل: بدءا من الإصدار 10.0.7 ، لن يكون هناك استثمارات هندسية لـ GetProductAvailabilities وGetAvailableInventoryNearby.</span><span class="sxs-lookup"><span data-stu-id="7fbef-136">Deprecated: As of release 10.0.7, there will no longer be engineering investments made for GetProductAvailabilities and GetAvailableInventoryNearby.</span></span> <span data-ttu-id="7fbef-137">يجب تحويل المؤسسات التي تستخدم واجهات برمجه التطبيقات (APIs) هذه في عمليات توزيع التجارة الإلكترونية إلى واجهات برمجة تطبيقات GetEstimatedAvailabilty وGetEstimatedProductWarehouseAvailability الجديدة وتمكين [ميزة حساب إتاحة المنتج المحسنة](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="7fbef-137">Organizations that use these APIs in their e-Commerce deployments should convert to the new GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs and enable the [Optimized product availability calculation feature](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).</span></span>  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="7fbef-138">الإعلانات السابقة حول الميزات التي تمت إزالتها أو إهمالها</span><span class="sxs-lookup"><span data-stu-id="7fbef-138">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="7fbef-139">لمعرفه المزيد حول الميزات التي تمت إزالتها أو إهمالها في الإصدارات السابقة، راجع [‏‫الميزات التي تمت إزالتها أو إهمالها في الإصدارات السابقة‬](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="7fbef-139">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).</span></span>
