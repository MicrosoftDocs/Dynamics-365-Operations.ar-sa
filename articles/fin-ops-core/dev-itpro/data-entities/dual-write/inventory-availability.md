---
title: توفر المخزون في الكتابة المزدوجة
description: يوفر هذا الموضوع معلومات حول فحص توفر المخزون في الكتابة المزدوجة.
author: RamaKrishnamoorthy
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
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 0fded78134b1427e6faea9656e1d3b02b467ae91
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193397"
---
# <a name="inventory-availability-in-dual-write"></a><span data-ttu-id="51bdb-103">توفر المخزون في الكتابة المزدوجة</span><span class="sxs-lookup"><span data-stu-id="51bdb-103">Inventory availability in dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="51bdb-104">باستخدام توفر المخزون، يمكنك فحص المخزون قبل إضافة منتج إلى صفحة **عروض الأسعار** أو **الأوامر** أو **الفواتير** في Microsoft Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="51bdb-104">By using inventory availability, you can check your inventory before you add a product to the **Quotations**, **Orders**, or **Invoices** page in Microsoft Dynamics 365 Sales.</span></span> <span data-ttu-id="51bdb-105">على سبيل المثال، يمكنك فحص المخزون وتحديد تاريخ التنفيذ كمهمة أساسية في عملية [العميل المتوقع إلى النقدية](dual-write-prospect-to-cash.md).</span><span class="sxs-lookup"><span data-stu-id="51bdb-105">For example, you check inventory and determine a fulfillment date as one key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span>

<span data-ttu-id="51bdb-106">إذا لم يكن لديك مخزون كافٍ، فيمكنك تقدير تاريخ التسليم استنادًا إلى عمليات استلام المخزون المتوقعة ومشاكلها.</span><span class="sxs-lookup"><span data-stu-id="51bdb-106">If you don't have enough inventory, you can estimate a delivery date, based on projected inventory receipts and issues.</span></span> <span data-ttu-id="51bdb-107">يمكنك أيضًا التحقق من معلومات "متوفر حسب التعهد‬" للمنتج، حيث يمكنك العثور على كمية ATP في الحد الزمني المحدد مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="51bdb-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the predefined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="51bdb-108">المخزون الفعلي</span><span class="sxs-lookup"><span data-stu-id="51bdb-108">On-hand inventory</span></span>

<span data-ttu-id="51bdb-109">في رأس صفحات **عروض الأسعار** أو **الأوامر** أو **الفواتير** في Dynamics 365 Sales، تمت إضافة زر جديد **المخزون الفعلي**.</span><span class="sxs-lookup"><span data-stu-id="51bdb-109">In Dynamics 365 Sales, a new **On-hand Inventory** button has been added to the header of the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="51bdb-110">عند النقر فوق الزر، يظهر مربع حوار ويمكنك تحديد الشركة والمنتج الذي تريد فحص مخزونه الفعلي.</span><span class="sxs-lookup"><span data-stu-id="51bdb-110">When you select this button, a dialog box appears, where you can specify the company and the product that you want to check the on-hand inventory for.</span></span> <span data-ttu-id="51bdb-111">يظهر مربع الحوار هذا نفس المعلومات كـ [مخزون فعلي](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span><span class="sxs-lookup"><span data-stu-id="51bdb-111">This dialog box shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span>

<span data-ttu-id="51bdb-112">يقوم مربع الحوار بإرجاع معلومات المخزون من Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="51bdb-112">The dialog box returns the inventory information from Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="51bdb-113">تشمل هذه المعلومات الكميات التالية:</span><span class="sxs-lookup"><span data-stu-id="51bdb-113">This information includes the following quantities:</span></span>

- <span data-ttu-id="51bdb-114">الكمية المتاحة</span><span class="sxs-lookup"><span data-stu-id="51bdb-114">On-hand quantity</span></span>
- <span data-ttu-id="51bdb-115">الكمية المحجوزة</span><span class="sxs-lookup"><span data-stu-id="51bdb-115">Reserved on-hand quantity</span></span>
- <span data-ttu-id="51bdb-116">الكمية الفعلية المتوفرة</span><span class="sxs-lookup"><span data-stu-id="51bdb-116">Available on-hand quantity</span></span>
- <span data-ttu-id="51bdb-117">الكمية المطلوبة</span><span class="sxs-lookup"><span data-stu-id="51bdb-117">Ordered quantity</span></span>
- <span data-ttu-id="51bdb-118">الكمية تحت الطلب</span><span class="sxs-lookup"><span data-stu-id="51bdb-118">On-order quantity</span></span>
- <span data-ttu-id="51bdb-119">الكمية المطلوبة المحجوزة</span><span class="sxs-lookup"><span data-stu-id="51bdb-119">Reserved ordered quantity</span></span>
- <span data-ttu-id="51bdb-120">إجمالي الكمية المتوفرة</span><span class="sxs-lookup"><span data-stu-id="51bdb-120">Total available quantity</span></span>

## <a name="atp-information"></a><span data-ttu-id="51bdb-121">معلومات ATP</span><span class="sxs-lookup"><span data-stu-id="51bdb-121">ATP information</span></span>

<span data-ttu-id="51bdb-122">في Sales، تمت إضافة زر **معلومات ATP** جديد إلى أصناف البند في صفحة **عروض الأسعار** و **الأوامر** و **الفواتير**.</span><span class="sxs-lookup"><span data-stu-id="51bdb-122">In Sales, a new **ATP Information** button has been added to line items on the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="51bdb-123">عند تحديد هذا الزر، يظهر مربع حوار ويمكنك تحديد الشركة والمنتج وموقع المخزون ومستودع المخزون وكمية الأمر.</span><span class="sxs-lookup"><span data-stu-id="51bdb-123">When you select this button, a dialog box appears, where you can specify the company, product, inventory site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="51bdb-124">لمربع الحوار هذا نفس الإعدادات الموضحة في [‏‫التعهد بالأمر‬](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span><span class="sxs-lookup"><span data-stu-id="51bdb-124">This dialog box has the same settings that are described in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span>

<span data-ttu-id="51bdb-125">يقوم مربع الحوار بإرجاع معلومات ATP من Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="51bdb-125">The dialog box returns the ATP information from Supply Chain Management.</span></span> <span data-ttu-id="51bdb-126">تشمل هذه المعلومات الكميات التالية:</span><span class="sxs-lookup"><span data-stu-id="51bdb-126">This information includes the following quantities:</span></span>

- <span data-ttu-id="51bdb-127">كمية ATP</span><span class="sxs-lookup"><span data-stu-id="51bdb-127">ATP quantity</span></span>
- <span data-ttu-id="51bdb-128">كمية الإيصال</span><span class="sxs-lookup"><span data-stu-id="51bdb-128">Receipt quantity</span></span>
- <span data-ttu-id="51bdb-129">كمية الإصدار</span><span class="sxs-lookup"><span data-stu-id="51bdb-129">Issue quantity</span></span>
- <span data-ttu-id="51bdb-130">كمية المخزون الفعلي</span><span class="sxs-lookup"><span data-stu-id="51bdb-130">On-hand quantity</span></span>

## <a name="how-it-works"></a><span data-ttu-id="51bdb-131">كيف يعمل</span><span class="sxs-lookup"><span data-stu-id="51bdb-131">How it works</span></span>

<span data-ttu-id="51bdb-132">عند تحديد الزر **المخزون الفعلي** في الصفحة **عروض الأسعار** أو **الأوامر** أو **الفواتير**، يتم اجراء استدعاء ثنائي الكتابة واجهة API **المخزون الفعلي**.</span><span class="sxs-lookup"><span data-stu-id="51bdb-132">When you select the **On-hand Inventory** button on the **Quotes**, **Orders**, or **Invoices** page, a live dual-write call is made to the **Onhand inventory** API.</span></span> <span data-ttu-id="51bdb-133">تقوم واجهه برمجه التطبيقات بحساب المخزون الفعلي للمنتج المحدد.</span><span class="sxs-lookup"><span data-stu-id="51bdb-133">The API calculates the on-hand inventory for the given product.</span></span> <span data-ttu-id="51bdb-134">يتم تخزين النتيجة في الجدولين **InventCDSInventoryOnHandRequestEntity** و **InventCDSInventoryOnHandEntryEntity**، ثم تتم كتابتها علي Dataverse حسب الكتابة الثنائية.</span><span class="sxs-lookup"><span data-stu-id="51bdb-134">The result is stored in the **InventCDSInventoryOnHandRequestEntity** and **InventCDSInventoryOnHandEntryEntity** tables, and then is written to Dataverse by dual-write.</span></span> <span data-ttu-id="51bdb-135">لاستخدام هذه الوظيفة، يجب تشغيل التعيينات ثنائيه الكتابة التالية.</span><span class="sxs-lookup"><span data-stu-id="51bdb-135">To use this functionality, you need to run the following dual-write maps.</span></span> <span data-ttu-id="51bdb-136">يستخدم هذا الحقل لتخطي المزامنة الاوليه عند تشغيل الخرائط.</span><span class="sxs-lookup"><span data-stu-id="51bdb-136">Skip initial synchronization when you run the maps.</span></span>

- <span data-ttu-id="51bdb-137">الإدخالات الفعلية لمخزون الاقراص المضغوطة (msdyn_inventoryonhandentries)</span><span class="sxs-lookup"><span data-stu-id="51bdb-137">CDS inventory on-hand entries (msdyn_inventoryonhandentries)</span></span>
- <span data-ttu-id="51bdb-138">الطلبات المخزون الفعلي CDS (msdyn_inventoryonhandrequests)</span><span class="sxs-lookup"><span data-stu-id="51bdb-138">CDS inventory on-hand requests (msdyn_inventoryonhandrequests)</span></span>

## <a name="templates"></a><span data-ttu-id="51bdb-139">القوالب</span><span class="sxs-lookup"><span data-stu-id="51bdb-139">Templates</span></span>
<span data-ttu-id="51bdb-140">تتوفر القوالب التالية لعرض بيانات المخزون الفعلي.</span><span class="sxs-lookup"><span data-stu-id="51bdb-140">The following templates are available for the exposing the onhand inventory data.</span></span>

<span data-ttu-id="51bdb-141">تطبيقات Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="51bdb-141">Finance and Operations apps</span></span> | <span data-ttu-id="51bdb-142">تطبيق Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="51bdb-142">Customer engagement app</span></span> | <span data-ttu-id="51bdb-143">الوصف</span><span class="sxs-lookup"><span data-stu-id="51bdb-143">Description</span></span> 
---|---|---
[<span data-ttu-id="51bdb-144">إدخالات المخزون الفعلي في CDS</span><span class="sxs-lookup"><span data-stu-id="51bdb-144">CDS inventory on-hand entries</span></span>](#145) | <span data-ttu-id="51bdb-145">msdyn_inventoryonhandentries</span><span class="sxs-lookup"><span data-stu-id="51bdb-145">msdyn_inventoryonhandentries</span></span> |
[<span data-ttu-id="51bdb-146">طلبات المخزون الفعلي في CDS</span><span class="sxs-lookup"><span data-stu-id="51bdb-146">CDS inventory on-hand requests</span></span>](#147) | <span data-ttu-id="51bdb-147">msdyn_inventoryonhandrequests</span><span class="sxs-lookup"><span data-stu-id="51bdb-147">msdyn_inventoryonhandrequests</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

###  <a name="cds-inventory-on-hand-entries-msdyn_inventoryonhandentries"></a><a name="145"></a><span data-ttu-id="51bdb-148">الإدخالات الفعلية لمخزون الاقراص المضغوطة (msdyn_inventoryonhandentries)</span><span class="sxs-lookup"><span data-stu-id="51bdb-148">CDS inventory on-hand entries (msdyn_inventoryonhandentries)</span></span>

<span data-ttu-id="51bdb-149">يقوم هذا القالب بمزامنة البيانات بين تطبيقات Finance and Operations وDataverse.</span><span class="sxs-lookup"><span data-stu-id="51bdb-149">This template synchronizes data between Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="51bdb-150">حقل Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="51bdb-150">Finance and Operations field</span></span> | <span data-ttu-id="51bdb-151">نوع التعيين</span><span class="sxs-lookup"><span data-stu-id="51bdb-151">Map type</span></span> | <span data-ttu-id="51bdb-152">حقل Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="51bdb-152">Customer engagement field</span></span> | <span data-ttu-id="51bdb-153">قيمة افتراضية</span><span class="sxs-lookup"><span data-stu-id="51bdb-153">Default value</span></span>
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

###  <a name="cds-inventory-on-hand-requests-msdyn_inventoryonhandrequests"></a><a name="147"></a><span data-ttu-id="51bdb-154">الطلبات المخزون الفعلي CDS (msdyn_inventoryonhandrequests)</span><span class="sxs-lookup"><span data-stu-id="51bdb-154">CDS inventory on-hand requests (msdyn_inventoryonhandrequests)</span></span>

<span data-ttu-id="51bdb-155">يقوم هذا القالب بمزامنة البيانات بين تطبيقات Finance and Operations وDataverse.</span><span class="sxs-lookup"><span data-stu-id="51bdb-155">This template synchronizes data between Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="51bdb-156">حقل Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="51bdb-156">Finance and Operations field</span></span> | <span data-ttu-id="51bdb-157">نوع التعيين</span><span class="sxs-lookup"><span data-stu-id="51bdb-157">Map type</span></span> | <span data-ttu-id="51bdb-158">حقل Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="51bdb-158">Customer engagement field</span></span> | <span data-ttu-id="51bdb-159">قيمة افتراضية</span><span class="sxs-lookup"><span data-stu-id="51bdb-159">Default value</span></span>
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