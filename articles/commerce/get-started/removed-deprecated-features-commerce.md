---
title: الميزات التي تمت إزالتها أو إهمالها في Dynamics 365 Commerce
description: يصف هذا الموضوع الميزات التي تمت إزالتها أو تلك المخطط لإزالتها من Dynamics 365 Commerce.
author: josaw
manager: AnnBe
ms.date: 06/10/2020
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
ms.openlocfilehash: 64241ef1c25359c7b3b305c4e8f2b24de7e8f5e4
ms.sourcegitcommit: cf709f1421a0bf66ecea493088ecb4eb08004187
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/12/2020
ms.locfileid: "3443908"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a><span data-ttu-id="9211a-103">الميزات التي تمت إزالتها أو إهمالها في Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="9211a-103">Removed or deprecated features in Dynamics 365 Commerce</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9211a-104">يصف هذا الموضوع الميزات التي تمت إزالتها أو تلك المخطط لإزالتها من Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9211a-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Commerce.</span></span>

- <span data-ttu-id="9211a-105">لم تعد ميزة *تمت الإزالة* متوفرة في المنتج.</span><span class="sxs-lookup"><span data-stu-id="9211a-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="9211a-106">لا توجد ميزة *المهملة* في التطوير النشط وقد يتم إزالتها في تحديثات مستقبلية.</span><span class="sxs-lookup"><span data-stu-id="9211a-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="9211a-107">تهدف هذه القائمة إلى مساعدتك في مراعاة ميزات الإزالة وعمليات الإهلاك للتخطيط الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="9211a-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="9211a-108">يمكن العثور على معلومات مفصلة حول الكائنات في تطبيقات Finance and Operations [التقارير المرجعية التقنية](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="9211a-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="9211a-109">يمكنك مقارنة إصدارات مختلفة من هذه التقارير لمعرفة المزيد حول الكائنات التي تم تغييرها أو التي تمت إزالتها من كل إصدار من تطبيقات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9211a-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-commerce-10011-release"></a><span data-ttu-id="9211a-110">ميزات تمت إزالتها أو إهمالها في الإصدار 10.0.11 من Commerce</span><span class="sxs-lookup"><span data-stu-id="9211a-110">Features removed or deprecated in the Commerce 10.0.11 release</span></span>
### <a name="data-action-hooks"></a><span data-ttu-id="9211a-111">ربط إجراءات البيانات</span><span class="sxs-lookup"><span data-stu-id="9211a-111">Data action hooks</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="9211a-112">**سبب الإهلاك/الإزالة**</span><span class="sxs-lookup"><span data-stu-id="9211a-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="9211a-113">تم إهمال ميزه ربط إجراءات البيانات بسبب مشاكل في الأداء.</span><span class="sxs-lookup"><span data-stu-id="9211a-113">The data action hooks feature has been deprecated due to performance issues.</span></span> |
| <span data-ttu-id="9211a-114">**هل تم الاستبدال بميزة أخرى؟**</span><span class="sxs-lookup"><span data-stu-id="9211a-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="9211a-115">يوصى بدلا من ذلك استخدام [‏‫عمليات تجاوز إجراءات البيانات‬](../e-commerce-extensibility/data-action-overrides.md) لتعديل منطق تسلسل العمل في طبقه إجراء البيانات.</span><span class="sxs-lookup"><span data-stu-id="9211a-115">It is recommended to instead use [data action overrides](../e-commerce-extensibility/data-action-overrides.md) to modify business logic in the data action layer.</span></span>|
| <span data-ttu-id="9211a-116">**مناطق المنتجات المتأثرة**</span><span class="sxs-lookup"><span data-stu-id="9211a-116">**Product areas affected**</span></span>         | <span data-ttu-id="9211a-117">إجراءات بيانات قابلية توسعة التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="9211a-117">E-Commerce extensibility data actions</span></span> |
| <span data-ttu-id="9211a-118">**خيارات النشر**</span><span class="sxs-lookup"><span data-stu-id="9211a-118">**Deployment option**</span></span>              | <span data-ttu-id="9211a-119">‏‏الكل</span><span class="sxs-lookup"><span data-stu-id="9211a-119">All</span></span> |
| <span data-ttu-id="9211a-120">**الحالة**</span><span class="sxs-lookup"><span data-stu-id="9211a-120">**Status**</span></span>                         | <span data-ttu-id="9211a-121">مهمل: اعتبارًا من إصدار 10.0.11</span><span class="sxs-lookup"><span data-stu-id="9211a-121">Deprecated: As of release 10.0.11</span></span> |

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a><span data-ttu-id="9211a-122">ميزات تمت إزالتها أو إهمالها في الإصدار 10.0.10 من Commerce</span><span class="sxs-lookup"><span data-stu-id="9211a-122">Features removed or deprecated in the Commerce 10.0.10 release</span></span>
### <a name="pos-operation-803---picking-and-receiving"></a><span data-ttu-id="9211a-123">عملية نقطة البيع 803 - الانتقاء والاستلام</span><span class="sxs-lookup"><span data-stu-id="9211a-123">POS operation 803 - Picking and receiving</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="9211a-124">**سبب الإهلاك/الإزالة**</span><span class="sxs-lookup"><span data-stu-id="9211a-124">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="9211a-125">جارٍ إهمال عمليات الانتقاء والاستلام نظرا لإعاده التصميم الجديد للعملية.</span><span class="sxs-lookup"><span data-stu-id="9211a-125">Picking and receiving operations is being deprecated due to new operation redesign.</span></span> |
| <span data-ttu-id="9211a-126">**هل تم الاستبدال بميزة أخرى؟**</span><span class="sxs-lookup"><span data-stu-id="9211a-126">**Replaced by another feature?**</span></span>   | <span data-ttu-id="9211a-127">نعم.</span><span class="sxs-lookup"><span data-stu-id="9211a-127">Yes.</span></span> <span data-ttu-id="9211a-128">ويتم استبدالها بعمليتي POS جديدتين: العملية الداخلية (804) والعملية الخارجية (805).</span><span class="sxs-lookup"><span data-stu-id="9211a-128">It is replaced by two new POS operations: inbound operation (804) and outbound operation (805).</span></span>|
| <span data-ttu-id="9211a-129">**مناطق المنتجات المتأثرة**</span><span class="sxs-lookup"><span data-stu-id="9211a-129">**Product areas affected**</span></span>         | <span data-ttu-id="9211a-130">تطبيق نقطة البيع (POS)</span><span class="sxs-lookup"><span data-stu-id="9211a-130">Point of sale (POS) application</span></span> |
| <span data-ttu-id="9211a-131">**خيارات النشر**</span><span class="sxs-lookup"><span data-stu-id="9211a-131">**Deployment option**</span></span>              | <span data-ttu-id="9211a-132">‏‏الكل</span><span class="sxs-lookup"><span data-stu-id="9211a-132">All</span></span> |
| <span data-ttu-id="9211a-133">**الحالة**</span><span class="sxs-lookup"><span data-stu-id="9211a-133">**Status**</span></span>                         | <span data-ttu-id="9211a-134">مهمل: بدءًا من الإصدار 10.0.10، لن تتلقي عملية الانتقاء والاستلام إيه تحديثات لميزات جديدة.</span><span class="sxs-lookup"><span data-stu-id="9211a-134">Deprecated: As of release 10.0.10, the picking and receiving operation will no longer receive any new feature updates.</span></span> <span data-ttu-id="9211a-135">سيتم اجراء إصلاحات الأخطاء الهامه فقط لهذه العملية في الإصدارات المستقبلية.</span><span class="sxs-lookup"><span data-stu-id="9211a-135">Only critical bug fixes will be done for this operation in future releases.</span></span> <span data-ttu-id="9211a-136">ويتم تشجيع كافة العملاء علي الانتقال إلى [العمليات الداخلية](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) و [العمليات الخارجية](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation)، والتي ستستمر في أن تكون جزءا من مخطط المنتج طويل الأجل.</span><span class="sxs-lookup"><span data-stu-id="9211a-136">All customers are encouraged to move to the new [Inbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) and [Outbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), which will continue to be part of our long-term product roadmap.</span></span> |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a><span data-ttu-id="9211a-137">ميزات تمت إزالتها أو إهمالها في الإصدار 10.0.7 من Commerce</span><span class="sxs-lookup"><span data-stu-id="9211a-137">Features removed or deprecated in the Commerce 10.0.7 release</span></span>
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a><span data-ttu-id="9211a-138">واجهات API لـ Commerce GetProductAvailabilities و GetAvailableInventoryNearby</span><span class="sxs-lookup"><span data-stu-id="9211a-138">Commerce GetProductAvailabilities and GetAvailableInventoryNearby API's</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="9211a-139">**سبب الإهلاك/الإزالة**</span><span class="sxs-lookup"><span data-stu-id="9211a-139">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="9211a-140">تم إنشاء واجهة API محسّنة جديدة لتحل محل واجهات برمجة التطبيقات GetProductAvailabilities و GetAvailableInventoryNearby.</span><span class="sxs-lookup"><span data-stu-id="9211a-140">New optimized APIs have been created to replace the GetProductAvailabilities and GetAvailableInventoryNearby APIs.</span></span> |
| <span data-ttu-id="9211a-141">**هل تم الاستبدال بميزة أخرى؟**</span><span class="sxs-lookup"><span data-stu-id="9211a-141">**Replaced by another feature?**</span></span>   | <span data-ttu-id="9211a-142">نعم: يتم استبداله بواجهات GetEstimatedAvailabilty وGetEstimatedProductWarehouseAvailability.</span><span class="sxs-lookup"><span data-stu-id="9211a-142">Yes: It is replaced by GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs.</span></span> |
| <span data-ttu-id="9211a-143">**مناطق المنتجات المتأثرة**</span><span class="sxs-lookup"><span data-stu-id="9211a-143">**Product areas affected**</span></span>         | <span data-ttu-id="9211a-144">SDK لتطبيق التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="9211a-144">e-Commerce application SDK</span></span> |
| <span data-ttu-id="9211a-145">**خيارات النشر**</span><span class="sxs-lookup"><span data-stu-id="9211a-145">**Deployment option**</span></span>              | <span data-ttu-id="9211a-146">‏‏الكل</span><span class="sxs-lookup"><span data-stu-id="9211a-146">All</span></span> |
| <span data-ttu-id="9211a-147">**الحالة**</span><span class="sxs-lookup"><span data-stu-id="9211a-147">**Status**</span></span>                         | <span data-ttu-id="9211a-148">مهمل: بدءا من الإصدار 10.0.7 ، لن يكون هناك استثمارات هندسية لـ GetProductAvailabilities وGetAvailableInventoryNearby.</span><span class="sxs-lookup"><span data-stu-id="9211a-148">Deprecated: As of release 10.0.7, there will no longer be engineering investments made for GetProductAvailabilities and GetAvailableInventoryNearby.</span></span> <span data-ttu-id="9211a-149">يجب تحويل المؤسسات التي تستخدم واجهات برمجه التطبيقات (APIs) هذه في عمليات توزيع التجارة الإلكترونية إلى واجهات برمجة تطبيقات GetEstimatedAvailabilty وGetEstimatedProductWarehouseAvailability الجديدة وتمكين [ميزة حساب إتاحة المنتج المحسنة](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="9211a-149">Organizations that use these APIs in their e-Commerce deployments should convert to the new GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs and enable the [Optimized product availability calculation feature](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).</span></span>  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="9211a-150">الإعلانات السابقة حول الميزات التي تمت إزالتها أو إهمالها</span><span class="sxs-lookup"><span data-stu-id="9211a-150">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="9211a-151">لمعرفه المزيد حول الميزات التي تمت إزالتها أو إهمالها في الإصدارات السابقة، راجع [‏‫الميزات التي تمت إزالتها أو إهمالها في الإصدارات السابقة‬](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="9211a-151">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).</span></span>
