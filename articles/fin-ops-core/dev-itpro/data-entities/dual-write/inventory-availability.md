---
title: توفر المخزون في الكتابة المزدوجة
description: يوفر هذا الموضوع معلومات حول فحص توفر المخزون في الكتابة المزدوجة.
author: yijialuan
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 9d9b7970720218fbcf2f512345ade672810440b4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748555"
---
# <a name="inventory-availability-in-dual-write"></a><span data-ttu-id="d7527-103">توفر المخزون في الكتابة المزدوجة</span><span class="sxs-lookup"><span data-stu-id="d7527-103">Inventory availability in dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d7527-104">باستخدام توفر المخزون، يمكنك فحص المخزون قبل إضافة منتج إلى صفحة **عروض الأسعار** أو **الأوامر** أو **الفواتير** في Microsoft Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="d7527-104">By using inventory availability, you can check your inventory before you add a product to the **Quotations**, **Orders**, or **Invoices** page in Microsoft Dynamics 365 Sales.</span></span> <span data-ttu-id="d7527-105">على سبيل المثال، يمكنك فحص المخزون وتحديد تاريخ التنفيذ كمهمة أساسية في عملية [العميل المتوقع إلى النقدية](dual-write-prospect-to-cash.md).</span><span class="sxs-lookup"><span data-stu-id="d7527-105">For example, you check inventory and determine a fulfillment date as one key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span>

<span data-ttu-id="d7527-106">إذا لم يكن لديك مخزون كافٍ، فيمكنك تقدير تاريخ التسليم استنادًا إلى عمليات استلام المخزون المتوقعة ومشاكلها.</span><span class="sxs-lookup"><span data-stu-id="d7527-106">If you don't have enough inventory, you can estimate a delivery date, based on projected inventory receipts and issues.</span></span> <span data-ttu-id="d7527-107">يمكنك أيضًا التحقق من معلومات "متوفر حسب التعهد‬" للمنتج، حيث يمكنك العثور على كمية ATP في الحد الزمني المحدد مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="d7527-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the predefined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="d7527-108">المخزون الفعلي</span><span class="sxs-lookup"><span data-stu-id="d7527-108">On-hand inventory</span></span>

<span data-ttu-id="d7527-109">في رأس صفحات **عروض الأسعار** أو **الأوامر** أو **الفواتير** في Dynamics 365 Sales، تمت إضافة زر جديد **المخزون الفعلي**.</span><span class="sxs-lookup"><span data-stu-id="d7527-109">In Dynamics 365 Sales, a new **On-hand Inventory** button has been added to the header of the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="d7527-110">عند النقر فوق الزر، يظهر مربع حوار ويمكنك تحديد الشركة والمنتج الذي تريد فحص مخزونه الفعلي.</span><span class="sxs-lookup"><span data-stu-id="d7527-110">When you select this button, a dialog box appears, where you can specify the company and the product that you want to check the on-hand inventory for.</span></span> <span data-ttu-id="d7527-111">يظهر مربع الحوار هذا نفس المعلومات كـ [مخزون فعلي](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span><span class="sxs-lookup"><span data-stu-id="d7527-111">This dialog box shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span>

<span data-ttu-id="d7527-112">يقوم مربع الحوار بإرجاع معلومات المخزون من Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d7527-112">The dialog box returns the inventory information from Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="d7527-113">تشمل هذه المعلومات الكميات التالية:</span><span class="sxs-lookup"><span data-stu-id="d7527-113">This information includes the following quantities:</span></span>

- <span data-ttu-id="d7527-114">الكمية المتاحة</span><span class="sxs-lookup"><span data-stu-id="d7527-114">On-hand quantity</span></span>
- <span data-ttu-id="d7527-115">الكمية المحجوزة</span><span class="sxs-lookup"><span data-stu-id="d7527-115">Reserved on-hand quantity</span></span>
- <span data-ttu-id="d7527-116">الكمية الفعلية المتوفرة</span><span class="sxs-lookup"><span data-stu-id="d7527-116">Available on-hand quantity</span></span>
- <span data-ttu-id="d7527-117">الكمية المطلوبة</span><span class="sxs-lookup"><span data-stu-id="d7527-117">Ordered quantity</span></span>
- <span data-ttu-id="d7527-118">الكمية تحت الطلب</span><span class="sxs-lookup"><span data-stu-id="d7527-118">On-order quantity</span></span>
- <span data-ttu-id="d7527-119">الكمية المطلوبة المحجوزة</span><span class="sxs-lookup"><span data-stu-id="d7527-119">Reserved ordered quantity</span></span>
- <span data-ttu-id="d7527-120">إجمالي الكمية المتوفرة</span><span class="sxs-lookup"><span data-stu-id="d7527-120">Total available quantity</span></span>

## <a name="atp-information"></a><span data-ttu-id="d7527-121">معلومات ATP</span><span class="sxs-lookup"><span data-stu-id="d7527-121">ATP information</span></span>

<span data-ttu-id="d7527-122">في Sales، تمت إضافة زر **معلومات ATP** جديد إلى أصناف البند في صفحة **عروض الأسعار** و **الأوامر** و **الفواتير**.</span><span class="sxs-lookup"><span data-stu-id="d7527-122">In Sales, a new **ATP Information** button has been added to line items on the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="d7527-123">عند تحديد هذا الزر، يظهر مربع حوار ويمكنك تحديد الشركة والمنتج وموقع المخزون ومستودع المخزون وكمية الأمر.</span><span class="sxs-lookup"><span data-stu-id="d7527-123">When you select this button, a dialog box appears, where you can specify the company, product, inventory site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="d7527-124">لمربع الحوار هذا نفس الإعدادات الموضحة في [‏‫التعهد بالأمر‬](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span><span class="sxs-lookup"><span data-stu-id="d7527-124">This dialog box has the same settings that are described in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span>

<span data-ttu-id="d7527-125">يقوم مربع الحوار بإرجاع معلومات ATP من Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d7527-125">The dialog box returns the ATP information from Supply Chain Management.</span></span> <span data-ttu-id="d7527-126">تشمل هذه المعلومات الكميات التالية:</span><span class="sxs-lookup"><span data-stu-id="d7527-126">This information includes the following quantities:</span></span>

- <span data-ttu-id="d7527-127">كمية ATP</span><span class="sxs-lookup"><span data-stu-id="d7527-127">ATP quantity</span></span>
- <span data-ttu-id="d7527-128">كمية الإيصال</span><span class="sxs-lookup"><span data-stu-id="d7527-128">Receipt quantity</span></span>
- <span data-ttu-id="d7527-129">كمية الإصدار</span><span class="sxs-lookup"><span data-stu-id="d7527-129">Issue quantity</span></span>
- <span data-ttu-id="d7527-130">كمية المخزون الفعلي</span><span class="sxs-lookup"><span data-stu-id="d7527-130">On-hand quantity</span></span>

## <a name="how-it-works"></a><span data-ttu-id="d7527-131">كيف يعمل</span><span class="sxs-lookup"><span data-stu-id="d7527-131">How it works</span></span>

<span data-ttu-id="d7527-132">عند تحديد الزر **المخزون الفعلي** في الصفحة **عروض الأسعار** أو **الأوامر** أو **الفواتير**، يتم اجراء استدعاء ثنائي الكتابة واجهة API **المخزون الفعلي**.</span><span class="sxs-lookup"><span data-stu-id="d7527-132">When you select the **On-hand Inventory** button on the **Quotes**, **Orders**, or **Invoices** page, a live dual-write call is made to the **Onhand inventory** API.</span></span> <span data-ttu-id="d7527-133">تقوم واجهه برمجه التطبيقات بحساب المخزون الفعلي للمنتج المحدد.</span><span class="sxs-lookup"><span data-stu-id="d7527-133">The API calculates the on-hand inventory for the given product.</span></span> <span data-ttu-id="d7527-134">يتم تخزين النتيجة في الجدولين **InventCDSInventoryOnHandRequestEntity** و **InventCDSInventoryOnHandEntryEntity**، ثم تتم كتابتها علي Dataverse حسب الكتابة الثنائية.</span><span class="sxs-lookup"><span data-stu-id="d7527-134">The result is stored in the **InventCDSInventoryOnHandRequestEntity** and **InventCDSInventoryOnHandEntryEntity** tables, and then is written to Dataverse by dual-write.</span></span> <span data-ttu-id="d7527-135">لاستخدام هذه الوظيفة، يجب تشغيل التعيينات ثنائيه الكتابة التالية.</span><span class="sxs-lookup"><span data-stu-id="d7527-135">To use this functionality, you need to run the following dual-write maps.</span></span> <span data-ttu-id="d7527-136">يستخدم هذا الحقل لتخطي المزامنة الاوليه عند تشغيل الخرائط.</span><span class="sxs-lookup"><span data-stu-id="d7527-136">Skip initial synchronization when you run the maps.</span></span>

- <span data-ttu-id="d7527-137">الإدخالات الفعلية لمخزون الاقراص المضغوطة (msdyn_inventoryonhandentries)</span><span class="sxs-lookup"><span data-stu-id="d7527-137">CDS inventory on-hand entries (msdyn_inventoryonhandentries)</span></span>
- <span data-ttu-id="d7527-138">الطلبات المخزون الفعلي CDS (msdyn_inventoryonhandrequests)</span><span class="sxs-lookup"><span data-stu-id="d7527-138">CDS inventory on-hand requests (msdyn_inventoryonhandrequests)</span></span>

## <a name="templates"></a><span data-ttu-id="d7527-139">القوالب</span><span class="sxs-lookup"><span data-stu-id="d7527-139">Templates</span></span>
<span data-ttu-id="d7527-140">تتوفر القوالب التالية لعرض بيانات المخزون الفعلي.</span><span class="sxs-lookup"><span data-stu-id="d7527-140">The following templates are available for the exposing the onhand inventory data.</span></span>

<span data-ttu-id="d7527-141">تطبيقات Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d7527-141">Finance and Operations apps</span></span> | <span data-ttu-id="d7527-142">تطبيق Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="d7527-142">Customer engagement app</span></span> | <span data-ttu-id="d7527-143">الوصف</span><span class="sxs-lookup"><span data-stu-id="d7527-143">Description</span></span> 
---|---|---
[<span data-ttu-id="d7527-144">إدخالات المخزون الفعلي في CDS</span><span class="sxs-lookup"><span data-stu-id="d7527-144">CDS inventory on-hand entries</span></span>](#145) | <span data-ttu-id="d7527-145">msdyn_inventoryonhandentries</span><span class="sxs-lookup"><span data-stu-id="d7527-145">msdyn_inventoryonhandentries</span></span> |
[<span data-ttu-id="d7527-146">طلبات المخزون الفعلي في CDS</span><span class="sxs-lookup"><span data-stu-id="d7527-146">CDS inventory on-hand requests</span></span>](#147) | <span data-ttu-id="d7527-147">msdyn_inventoryonhandrequests</span><span class="sxs-lookup"><span data-stu-id="d7527-147">msdyn_inventoryonhandrequests</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

###  <a name="cds-inventory-on-hand-entries-msdyn_inventoryonhandentries"></a><a name="145"></a><span data-ttu-id="d7527-148">الإدخالات الفعلية لمخزون الاقراص المضغوطة (msdyn_inventoryonhandentries)</span><span class="sxs-lookup"><span data-stu-id="d7527-148">CDS inventory on-hand entries (msdyn_inventoryonhandentries)</span></span>

<span data-ttu-id="d7527-149">يقوم هذا القالب بمزامنة البيانات بين تطبيقات Finance and Operations وDataverse.</span><span class="sxs-lookup"><span data-stu-id="d7527-149">This template synchronizes data between Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="d7527-150">حقل Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d7527-150">Finance and Operations field</span></span> | <span data-ttu-id="d7527-151">نوع التعيين</span><span class="sxs-lookup"><span data-stu-id="d7527-151">Map type</span></span> | <span data-ttu-id="d7527-152">حقل Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="d7527-152">Customer engagement field</span></span> | <span data-ttu-id="d7527-153">قيمة افتراضية</span><span class="sxs-lookup"><span data-stu-id="d7527-153">Default value</span></span>
---|---|---|---
`REQUESTID` | = | `msdyn_request.msdyn_requestid` |
`INVENTORYSITEID` | = | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | = | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`AVAILABLEONHANDQUANTITY` | > | `msdyn_availableonhandquantity` |
`AVAILABLEORDEREDQUANTITY` | > | `msdyn_availableorderedquantity` |
`ONHANDQUANTITY` | > | `msdyn_onhandquantity` |
`ONORDERQUANTITY` | > | `msdyn_onorderquantity` |
`ORDEREDQUANTITY` | > | `msdyn_orderedquantity` |
`RESERVEDONHANDQUANTITY` | > | `msdyn_reservedonhandquantity` |
`RESERVEDORDEREDQUANTITY` | > | `msdyn_reservedorderedquantity` |
`TOTALAVAILABLEQUANTITY` | > | `msdyn_totalavailablequantity` |
`ATPDATE` | = | `msdyn_atpdate` |
`ATPQUANTITY` | > | `msdyn_atpquantity` |
`PROJECTEDISSUEQUANTITY` | > | `msdyn_projectedissuequantity` |
`PROJECTEDONHANDQUANTITY` | > | `msdyn_projectedonhandquantity` |
`PROJECTEDRECEIPTQUANTITY` | > | `msdyn_projectedreceiptquantity` |
`ORDERQUANTITY` | > | `msdyn_orderquantity` |
`UNAVAILABLEONHANDQUANTITY` | > | `msdyn_unavailableonhandquantity` |

###  <a name="cds-inventory-on-hand-requests-msdyn_inventoryonhandrequests"></a><a name="147"></a><span data-ttu-id="d7527-154">الطلبات المخزون الفعلي CDS (msdyn_inventoryonhandrequests)</span><span class="sxs-lookup"><span data-stu-id="d7527-154">CDS inventory on-hand requests (msdyn_inventoryonhandrequests)</span></span>

<span data-ttu-id="d7527-155">يقوم هذا القالب بمزامنة البيانات بين تطبيقات Finance and Operations وDataverse.</span><span class="sxs-lookup"><span data-stu-id="d7527-155">This template synchronizes data between Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="d7527-156">حقل Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d7527-156">Finance and Operations field</span></span> | <span data-ttu-id="d7527-157">نوع التعيين</span><span class="sxs-lookup"><span data-stu-id="d7527-157">Map type</span></span> | <span data-ttu-id="d7527-158">حقل Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="d7527-158">Customer engagement field</span></span> | <span data-ttu-id="d7527-159">قيمة افتراضية</span><span class="sxs-lookup"><span data-stu-id="d7527-159">Default value</span></span>
---|---|---|---
`REQUESTID` | = | `msdyn_requestid` |
`PRODUCTNUMBER` | < | `msdyn_product.msdyn_productnumber` |
`ISATPCALCULATION` | << | `msdyn_isatpcalculation` |
`ORDERQUANTITY` | < | `msdyn_orderquantity` |
`INVENTORYSITEID` | < | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | < | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`REFERENCENUMBER` | < | `msdyn_referencenumber` |
`LINECREATIONSEQUENCENUMBER` | < | `msdyn_linecreationsequencenumber` |






[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]