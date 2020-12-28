---
title: استكشاف أخطاء أوامر المبيعات وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع أوامر المبيعات.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTable, SalesTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 6e51723915892f465ce09d09ee9ed622bab9451e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421325"
---
# <a name="troubleshoot-sales-orders"></a><span data-ttu-id="a5968-103">استكشاف أخطاء أوامر المبيعات وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="a5968-103">Troubleshoot sales orders</span></span>

<span data-ttu-id="a5968-104">يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="a5968-104">This topic describes how to fix issues that you might encounter while you work with sales orders.</span></span>

## <a name="the-tax-information-isnt-updated-if-i-change-the-location-on-a-sales-order-header"></a><span data-ttu-id="a5968-105">لا يتم تحديث معلومات الضريبة عند تغيير الموقع على رأس أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="a5968-105">The tax information isn't updated if I change the location on a sales order header.</span></span>

### <a name="issue-description"></a><span data-ttu-id="a5968-106">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="a5968-106">Issue description</span></span>

<span data-ttu-id="a5968-107">إذا تم تغيير عنوان الموقع أو المستودع أو عنوان التسليم على رأس امر المبيعات أو على مستوى البنود، فلن يتم تحديث معلومات ضريبة الحالة بشكل تلقائي للبنود.</span><span class="sxs-lookup"><span data-stu-id="a5968-107">If the site, warehouse, or delivery address is changed either on a sales order header or at the line level, the case tax information isn't automatically updated for the lines.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a5968-108">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="a5968-108">Issue resolution</span></span>

<span data-ttu-id="a5968-109">يتم هذا السلوك بسبب التصميم.</span><span class="sxs-lookup"><span data-stu-id="a5968-109">This behavior is by design.</span></span> <span data-ttu-id="a5968-110">تحدث المشكلة بسبب عدم تغيير عنوان التسليم والموقع والمستودع بشكل تلقائي على مستوى البنود.</span><span class="sxs-lookup"><span data-stu-id="a5968-110">The issue occurs because the delivery address, site, and warehouse aren't automatically changed at the line level either.</span></span> <span data-ttu-id="a5968-111">يجب تحديثها يدويًا.</span><span class="sxs-lookup"><span data-stu-id="a5968-111">You must update them manually.</span></span>

## <a name="if-there-are-two-trade-agreements-for-the-same-period-or-overlapping-periods-the-same-agreement-line-is-always-selected"></a><span data-ttu-id="a5968-112">عند وجود  اتفاقيتين  تجاريتين لنفس الفترة أو لفترات متراكبة، يتم دائمًا تحديد بند الاتفاقية نفسها.</span><span class="sxs-lookup"><span data-stu-id="a5968-112">If there are two trade agreements for the same period or overlapping periods, the same agreement line is always selected.</span></span>

### <a name="issue-description"></a><span data-ttu-id="a5968-113">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="a5968-113">Issue description</span></span>

<span data-ttu-id="a5968-114">إذا تم تحديد اتفاقيتين تجاريتين لنفس الفترة أو لفترات متراكبة، يتم دائمًا تحديد الاتفاقية التجارية نفسها في كل مرة عندما تنشئ بنود أمر مبيعات تحتوي على هذه الأصناف.‬</span><span class="sxs-lookup"><span data-stu-id="a5968-114">If two trade agreements are defined for the same period or overlapping periods, the same trade agreement seems to be selected every time when you create sales order lines that contain those items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a5968-115">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="a5968-115">Issue resolution</span></span>

<span data-ttu-id="a5968-116">عند وجود أكثر من اتفاقية تجارية واحد لتاريخ محدد، يتم دائمًا تحديد الاتفاقية التجارية ذات السعر الأقل.</span><span class="sxs-lookup"><span data-stu-id="a5968-116">If there is more than one trade agreement for a given date, the trade agreement that has the lowest price is always selected.</span></span> <span data-ttu-id="a5968-117">لمزيد من المعلومات، قم بتنزيل المستند التقني التالي: [الاتفاقيات التجارية في Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).</span><span class="sxs-lookup"><span data-stu-id="a5968-117">For more information, download the following white paper: [Trade agreements in Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).</span></span>

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a><span data-ttu-id="a5968-118">هل يمكنني ربط أمر شراء  بأمر  مبيعات لتنفيذ الطلب؟</span><span class="sxs-lookup"><span data-stu-id="a5968-118">Can I link a purchase order to a sales order to fulfill demand?</span></span>

<span data-ttu-id="a5968-119">يمكنك إنشاء أمر شراء من أمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="a5968-119">You can create a purchase order from a sales order.</span></span> <span data-ttu-id="a5968-120">لمزيد من المعلومات، راجع [إنشاء أمر شراء من أمر مبيعات](tasks/create-purchase-order-sales-order.md).</span><span class="sxs-lookup"><span data-stu-id="a5968-120">For more information, see [Create a purchase order from a sales order](tasks/create-purchase-order-sales-order.md).</span></span>

## <a name="i-cant-cancel-or-delete-a-return-order-or-a-sales-order"></a><span data-ttu-id="a5968-121">لا يمكنني إلغاء أمر إرجاع أو أمر مبيعات أو حذفه.</span><span class="sxs-lookup"><span data-stu-id="a5968-121">I can't cancel or delete a return order or a sales order.</span></span>

<span data-ttu-id="a5968-122">يمكنك إلغاء أوامر الشراء وأوامر الإرجاع فقط عندما تكون حالتها *مُنشأة*.</span><span class="sxs-lookup"><span data-stu-id="a5968-122">You can cancel only sales orders and return orders that are in a *Created* state.</span></span> <span data-ttu-id="a5968-123">لمزيد من المعلومات، راجع [إلغاء أمر إرجاع](../service-management/cancel-return-order.md).</span><span class="sxs-lookup"><span data-stu-id="a5968-123">For more information, see [Cancel a return order](../service-management/cancel-return-order.md).</span></span>

## <a name="when-i-try-to-cancel-a-sales-order-i-receive-a-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations-error"></a><span data-ttu-id="a5968-124">عندما أحاول إلغاء أمر مبيعات أتلقى رسالة الخطأ " لا يمكن إزالة الحجوزات نظرًا لوجود عمل مُنشأ يعتمد على الحجوزات".‬</span><span class="sxs-lookup"><span data-stu-id="a5968-124">When I try to cancel a sales order, I receive a "Reservations cannot be removed because there is work created which relies on the reservations" error.</span></span>

<span data-ttu-id="a5968-125">إذا كان العمل يقترن بأمر مبيعات، فلا يمكنك إلغاء أمر المبيعات حتى يتم إلغاء العمل وعكسه.</span><span class="sxs-lookup"><span data-stu-id="a5968-125">If work is associated with a sales order, you can't cancel the sales order until the work is canceled and reversed.</span></span> <span data-ttu-id="a5968-126">ينطبق هذا المتطلب حتى لون كان العمل المرتبط  بأمر  المبيعات مغلقا.</span><span class="sxs-lookup"><span data-stu-id="a5968-126">This requirement applies even if the work that is associated with the sales order is closed.</span></span>

<span data-ttu-id="a5968-127">لإصلاح هذه المشكلة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="a5968-127">To fix this issue, follow these steps.</span></span>

1. <span data-ttu-id="a5968-128">قم بإلغاء العمل، وضع المخزون من جديد في الموقع المطلوب.</span><span class="sxs-lookup"><span data-stu-id="a5968-128">Cancel the work, and put inventory back into the desired location.</span></span> <span data-ttu-id="a5968-129">انتقل إلى حمل العمل ذي الصلة لأمر المبيعات، وحدد **تقليل الكمية المنتقاة‬‏‫** على بند حمل العمل أو **إلغاء العمل** على جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="a5968-129">Go to the relevant load of the sales order, and select either **Reduce picked quantity** on the load line or **Reverse work** on the Action Pane.</span></span>

    <span data-ttu-id="a5968-130">أصبحت حالة العمل الآن *مُلغى*، ويتم إنشاء ومعالجة حركة المخزون الجديدة بشكل تلقائي لإعادة وضع المخزون في الموقع الذي ورد وصفه عند الإلغاء.</span><span class="sxs-lookup"><span data-stu-id="a5968-130">The work now has a status of *Canceled*, and new inventory movement work is automatically created and processed to put inventory back into the location that was described at the time of reversal.</span></span>

2. <span data-ttu-id="a5968-131">احذف حمل العمل.</span><span class="sxs-lookup"><span data-stu-id="a5968-131">Delete the load.</span></span> <span data-ttu-id="a5968-132">يتم أيضًا حذف الشحنة.</span><span class="sxs-lookup"><span data-stu-id="a5968-132">The shipment is also deleted.</span></span>
3. <span data-ttu-id="a5968-133">ينبغي الآن أن تكون قادرًا على الانتقال إلى أمر المبيعات وإلغائه.</span><span class="sxs-lookup"><span data-stu-id="a5968-133">You should now be able to go to the sales order and cancel it.</span></span>

## <a name="i-cant-cancel-an-intercompany-purchase-order-that-is-linked-to-a-sales-order"></a><span data-ttu-id="a5968-134">لا يمكنني إلغاء أمر شراء بين الشركات الشقيقة يرتبط بأمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="a5968-134">I can't cancel an intercompany purchase order that is linked to a sales order.</span></span>

### <a name="issue-description"></a><span data-ttu-id="a5968-135">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="a5968-135">Issue description</span></span>

<span data-ttu-id="a5968-136">إذا حاولت إلغاء أمر شراء بين الشركات الشقيقة يرتبط بأمر مبيعات، قد تتلقى رسالة الخطأ التالية "لا يمكن خفض الكمية بسبب تغيير علامة الكمية المحدثة المتبقية ".</span><span class="sxs-lookup"><span data-stu-id="a5968-136">If you try to cancel an intercompany purchase order that is linked to a sales order, you might receive the following error message: "Quantity cannot be reduced because the remaining update quantity changes sign."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a5968-137">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="a5968-137">Issue resolution</span></span>

<span data-ttu-id="a5968-138">تم إصلاح هذه المشكلة في Microsoft Dynamics 365 Supply Chain Management الإصدار 10.0.13.</span><span class="sxs-lookup"><span data-stu-id="a5968-138">This issue was fixed in Microsoft Dynamics 365 Supply Chain Management version 10.0.13.</span></span> <span data-ttu-id="a5968-139">في هذا الإصدار والإصدارات اللاحقة، يمكنك الآن إلغاء أمر الشراء بين الشركات الشقيقة المرتبط بأمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="a5968-139">In that version and later versions, you can now cancel an intercompany purchase order that is linked to a sales order.</span></span>

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a><span data-ttu-id="a5968-140">هل يمكنني استعادة أمر مبيعات مفوتر تم حذفه؟</span><span class="sxs-lookup"><span data-stu-id="a5968-140">Can I restore an invoiced sales order that was deleted?</span></span>

### <a name="issue-description"></a><span data-ttu-id="a5968-141">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="a5968-141">Issue description</span></span>

<span data-ttu-id="a5968-142">تم حذف أمر مبيعات مفوتر عن طريق الخطأ، وترغب في استعادته أو عرض تفاصيله.</span><span class="sxs-lookup"><span data-stu-id="a5968-142">An invoiced sales order was deleted by mistake, and you want to restore it or view its details.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a5968-143">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="a5968-143">Issue resolution</span></span>

<span data-ttu-id="a5968-144">إذا تمت فوترة أمر المبيعات المحذوف، فانتقل إلى **حساب العميل \> الحركات \> المستند الأصلي \> عرض التفاصيل**.</span><span class="sxs-lookup"><span data-stu-id="a5968-144">If the deleted sales order has already been invoiced, go to **Customer account \> Transactions \> Original document \> View details**.</span></span> <span data-ttu-id="a5968-145">ابحث عن الفاتورة التي تبحث عنها، وحددها لعرض تفاصيلها.</span><span class="sxs-lookup"><span data-stu-id="a5968-145">Find the invoice that you're looking for, and select it to view its details.</span></span> <span data-ttu-id="a5968-146">تتضمن هذه التفاصيل مرجع أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="a5968-146">These details include the sales order reference.</span></span> <span data-ttu-id="a5968-147">كما يجب أن تكون قادرًا على الوصول إلى تفاصيل أمر المبيعات من تلك الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a5968-147">You should also be able to access the sales order details from that page.</span></span>

## <a name="the-deadline-of-a-sales-order-header-cant-be-found-in-the-salesorderheaderv2entity-data-entity"></a><span data-ttu-id="a5968-148">يتعذر العثور على الموعد النهائي لرأس أمر المبيعات في كيان البيانات SalesOrderHeaderV2Entity</span><span class="sxs-lookup"><span data-stu-id="a5968-148">The deadline of a sales order header can't be found in the SalesOrderHeaderV2Entity data entity.</span></span>

<span data-ttu-id="a5968-149">حقل الموعد النهائي غير موجود في الكيان *SalesOrderHeaderV2Entity*.</span><span class="sxs-lookup"><span data-stu-id="a5968-149">The deadline field doesn't exist on the *SalesOrderHeaderV2Entity* entity.</span></span>

## <a name="i-must-delete-orphaned-sales-order-records"></a><span data-ttu-id="a5968-150">يجب حذف سجلات أوامر المبيعات المعزولة.</span><span class="sxs-lookup"><span data-stu-id="a5968-150">I must delete orphaned sales order records.</span></span>

<span data-ttu-id="a5968-151">لتنظيف سجلات أوامر المبيعات المعزولة ، قم بتشغيل الوظيفة الدورية *حذف أمر المبيعات* من خلال الانتقال إلى أي من الأماكن التالية:</span><span class="sxs-lookup"><span data-stu-id="a5968-151">To clean up orphaned sales order records, run the *Sales order deletion* periodic job by going to either of the following places:</span></span>

- <span data-ttu-id="a5968-152">المبيعات والتسويق \> المهام الدورية \> تنظيف \> حذف أمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="a5968-152">Sales and marketing \> Periodic tasks \> Clean up \> Delete sales orders</span></span>
- <span data-ttu-id="a5968-153">البيع بالتجزئة والتجارة \> تكنولوجيا معلومات البيع بالتجزئة والتجارة \> تنظيف \> حذف أوامر المبيعات</span><span class="sxs-lookup"><span data-stu-id="a5968-153">Retail and commerce \> Retail and commerce IT \> Clean up \> Delete sales orders</span></span>

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a><span data-ttu-id="a5968-154">هل توجد طريقة لحساب العمولات على الفواتير التي تم ترحيلها؟</span><span class="sxs-lookup"><span data-stu-id="a5968-154">Is there a way to calculate commissions on invoices that have already been posted?</span></span>

<span data-ttu-id="a5968-155">لا تدعم Supply Chain Management في الوقت الحالي حساب العمولات للفواتير المرحّلة.</span><span class="sxs-lookup"><span data-stu-id="a5968-155">Supply Chain Management doesn't currently support the calculation of commissions for posted invoices.</span></span>

## <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a><span data-ttu-id="a5968-156">صنف المجموعة غير مدعوم في عملية بين الشركات الشقيقة.</span><span class="sxs-lookup"><span data-stu-id="a5968-156">A bundle item isn't supported in an intercompany process.</span></span>

<span data-ttu-id="a5968-157">لا يتوفر صنف المجموعة لأمر الشراء لأنك، إذا قمت بفحص بنود أمر المبيعات لصنف المجموعة، ستلاحظ أن الكمية هي *0* (صفر) والحالة هي *ملغى*..</span><span class="sxs-lookup"><span data-stu-id="a5968-157">The bundle item isn't available for the purchase order because, if you examine the sales order lines for the bundle item, you will notice that the quantity is *0* (zero) and the status is *Cancelled*.</span></span> <span data-ttu-id="a5968-158">يتم هذا السلوك بسبب التصميم.</span><span class="sxs-lookup"><span data-stu-id="a5968-158">This behavior is by design.</span></span> <span data-ttu-id="a5968-159">يشتري أمر المبيعات مكونات صنف المجموعة فقط.</span><span class="sxs-lookup"><span data-stu-id="a5968-159">The sales order buys only the components of the bundle item.</span></span> <span data-ttu-id="a5968-160">ولا يشتري صنف المجموعة بحد ذاته.</span><span class="sxs-lookup"><span data-stu-id="a5968-160">It doesn't buy the bundle item itself.</span></span>

<span data-ttu-id="a5968-161">إذا كان من الضروري شراء مجموعة، فعليك أن تأخذ في الاعتبار ما إذا كان يجب وضع علامة عليه كصنف مجموعة، لأن هذه الوظيفة مصممة بالفعل لسيناريوهات التعرف على الإيرادات.</span><span class="sxs-lookup"><span data-stu-id="a5968-161">If you must buy a bundle, consider whether you have to mark it as bundle item, because this functionality is actually designed for revenue recognition scenarios.</span></span> <span data-ttu-id="a5968-162">لمزيد من المعلومات حول أصناف المجموعة، راجع [المجموعات](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).</span><span class="sxs-lookup"><span data-stu-id="a5968-162">For more information about bundle items, see [Bundles](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).</span></span>
