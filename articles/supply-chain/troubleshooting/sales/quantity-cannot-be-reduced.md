---
title: لا يمكن تخفيض الكمية عند إلغاء أمر المبيعات
description: لا يمكن تخفيض الكمية عند إلغاء أمر المبيعات.
author: hja-ms
ms.date: 5/17/2021
ms.topic: troubleshooting
ms.search.form: SalesTable_SalesCancelOrder, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: hja
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1a2cc9c9fd3d085508fc652bc9ee0a352d869dee
ms.sourcegitcommit: a02d3d64c899f8554b74342d5a1856d824bf1abe
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/11/2021
ms.locfileid: "6230826"
---
# <a name="the-quantity-cant-be-reduced-when-a-sales-order-is-canceled"></a><span data-ttu-id="ca116-103">لا يمكن تخفيض الكمية عند إلغاء أمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="ca116-103">The quantity can't be reduced when a sales order is canceled</span></span>

<span data-ttu-id="ca116-104">رمز الخطأ: SYS138831</span><span class="sxs-lookup"><span data-stu-id="ca116-104">Error code: SYS138831</span></span>

## <a name="symptoms"></a><span data-ttu-id="ca116-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="ca116-105">Symptoms</span></span>

<span data-ttu-id="ca116-106">يعرض النظام رسالة الخطأ التالية:</span><span class="sxs-lookup"><span data-stu-id="ca116-106">The system shows the following error message:</span></span>

> <span data-ttu-id="ca116-107">لا يمكن تخفيض الكمية.</span><span class="sxs-lookup"><span data-stu-id="ca116-107">The quantity cannot be reduced.</span></span> <span data-ttu-id="ca116-108">عدد حركات المخزون في الأمر منخفض جدًا نظرًا لأنه تتم الإشارة إلى الكمية أو جزء منها بواسطة أمر إخراج أو أمر إنتاج أو يتم تمييزها بحركات أخرى.</span><span class="sxs-lookup"><span data-stu-id="ca116-108">The number of inventory transactions on order is too low because the quantity or part of it is referenced by an output order or a production order or is marked against other transactions.</span></span>

## <a name="cause"></a><span data-ttu-id="ca116-109">السبب</span><span class="sxs-lookup"><span data-stu-id="ca116-109">Cause</span></span>

<span data-ttu-id="ca116-110">إذا كان العمل يقترن بأمر مبيعات، فلا يمكنك إلغاء أمر المبيعات حتى يتم إلغاء العمل وعكسه.</span><span class="sxs-lookup"><span data-stu-id="ca116-110">If work is associated with a sales order, you can't cancel the sales order until the work is canceled and reversed.</span></span> <span data-ttu-id="ca116-111">ينطبق هذا المتطلب حتى لون كان العمل المرتبط  بأمر  المبيعات مغلقا.</span><span class="sxs-lookup"><span data-stu-id="ca116-111">This requirement applies even if the work that is associated with the sales order is closed.</span></span>

## <a name="resolution"></a><span data-ttu-id="ca116-112">الحل</span><span class="sxs-lookup"><span data-stu-id="ca116-112">Resolution</span></span>

<span data-ttu-id="ca116-113">لإصلاح هذه المشكلة، أكمل المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="ca116-113">To fix this issue, complete the following tasks:</span></span>

1. <span data-ttu-id="ca116-114">قم بإلغاء العمل المفتوح.</span><span class="sxs-lookup"><span data-stu-id="ca116-114">Cancel open work.</span></span>
1. <span data-ttu-id="ca116-115">احذف حمل العمل.</span><span class="sxs-lookup"><span data-stu-id="ca116-115">Delete the load.</span></span>
1. <span data-ttu-id="ca116-116">قم بتقليل الكمية المنتقاة.</span><span class="sxs-lookup"><span data-stu-id="ca116-116">Reduce the picked quantity.</span></span>

### <a name="cancel-open-work"></a><span data-ttu-id="ca116-117">قم بإلغاء العمل المفتوح</span><span class="sxs-lookup"><span data-stu-id="ca116-117">Cancel open work</span></span>

<span data-ttu-id="ca116-118">لإلغاء العمل المفتوح، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="ca116-118">To cancel open work, follow these steps.</span></span>

1. <span data-ttu-id="ca116-119">انتقل إلى **إدارة المستودع \> المهام الدورية \> تنظيف \> إلغاء العمل**.</span><span class="sxs-lookup"><span data-stu-id="ca116-119">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="ca116-120">في حقل **معرف العمل**، حدد معرف العمل الذي تريد إلغاؤه، والذي يحتوي حاليًا على قيمة **حالة العمل** التي تكون *مفتوح* أو *قيد التقدم* أو *تم الإلغاء* أو *تم التجميع* أو *مغلق*.</span><span class="sxs-lookup"><span data-stu-id="ca116-120">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="ca116-121">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ca116-121">Select **OK**.</span></span>
1. <span data-ttu-id="ca116-122">حدد **نعم** لتأكيد رغبتك في إلغاء العمل.</span><span class="sxs-lookup"><span data-stu-id="ca116-122">Select **Yes** to confirm that you want to cancel the work.</span></span>

### <a name="delete-the-load"></a><span data-ttu-id="ca116-123">حذف حمل العمل</span><span class="sxs-lookup"><span data-stu-id="ca116-123">Delete the load</span></span>

<span data-ttu-id="ca116-124">لحذف حمل العمل، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="ca116-124">To delete a load, follow these steps.</span></span>

1. <span data-ttu-id="ca116-125">انتقل إلى **المبيعات والتسويق \> أوامر المبيعات \> كافة أوامر المبيعات‬**.</span><span class="sxs-lookup"><span data-stu-id="ca116-125">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="ca116-126">افتح أمر المبيعات المتعلق.</span><span class="sxs-lookup"><span data-stu-id="ca116-126">Open the relevant sales order.</span></span>
1. <span data-ttu-id="ca116-127">في علامة التبويب السريعة **بنود أمر المبيعات**، حدد **المستودع \> تفاصيل العمل**.</span><span class="sxs-lookup"><span data-stu-id="ca116-127">On the **Sales order lines** FastTab, select **Warehouse \> Work details**.</span></span>
1. <span data-ttu-id="ca116-128">في الصفحة **العمل**، في جزء الإجراءات، في علامة التبويب **العمل**، في المجموعة **العمل**، حدد **إلغاء العمل**.</span><span class="sxs-lookup"><span data-stu-id="ca116-128">On the **Work** page, on the Action Pane, on the **Work** tab, in the **Work** group, select **Cancel work**.</span></span>
1. <span data-ttu-id="ca116-129">تأكد من أنه يتم تعيين الحقل **حالة العمل** إلى *ملغي*.</span><span class="sxs-lookup"><span data-stu-id="ca116-129">Confirm that the **Work status** field is set to *Canceled*.</span></span>
1. <span data-ttu-id="ca116-130">أغلق صفحة **العمل**.</span><span class="sxs-lookup"><span data-stu-id="ca116-130">Close the **Work** page.</span></span>
1. <span data-ttu-id="ca116-131">في الصفحة تفاصيل أمر المبيعات، في علامة التبويب السريعة **‬‏‫بنود أمر المبيعات**، حدد **المستودع \> تفاصيل التحميل**.</span><span class="sxs-lookup"><span data-stu-id="ca116-131">On the sales order details page, on the **Sales order lines** FastTab, select **Warehouse \> Load details**.</span></span>
1. <span data-ttu-id="ca116-132">في جزء الإجراءات، حدد **حذف**.</span><span class="sxs-lookup"><span data-stu-id="ca116-132">On the Action Pane, select **Delete**.</span></span>
1. <span data-ttu-id="ca116-133">حدد **نعم** لتأكيد رغبتك في حذف حمل العمل.</span><span class="sxs-lookup"><span data-stu-id="ca116-133">Select **Yes** to confirm that you want to delete the load.</span></span>
1. <span data-ttu-id="ca116-134">أغلق صفحة **حمل العمل**.</span><span class="sxs-lookup"><span data-stu-id="ca116-134">Close the **Load** page.</span></span>

### <a name="reduce-the-picked-quantity"></a><span data-ttu-id="ca116-135">قم بتقليل الكمية المنتقاة</span><span class="sxs-lookup"><span data-stu-id="ca116-135">Reduce the picked quantity</span></span>

<span data-ttu-id="ca116-136">بعد إلغاء كافة الأعمال، اتبع الخطوات التالية لتقليل الكمية المنتقاة.</span><span class="sxs-lookup"><span data-stu-id="ca116-136">After all work has been canceled, follow these steps to reduce the picked quantity.</span></span>

1. <span data-ttu-id="ca116-137">انتقل إلى **المبيعات والتسويق \> أوامر المبيعات \> كافة أوامر المبيعات‬**.</span><span class="sxs-lookup"><span data-stu-id="ca116-137">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="ca116-138">افتح أمر المبيعات المتعلق.</span><span class="sxs-lookup"><span data-stu-id="ca116-138">Open the relevant sales order.</span></span>
1. <span data-ttu-id="ca116-139">في علامة التبويب السريعة **بنود أوامر المبيعات**، حدد **تحديث البند \> انتقاء** من شريط الأدوات.</span><span class="sxs-lookup"><span data-stu-id="ca116-139">On the **Sales order lines** FastTab, select **Update line \> Pick** from the toolbar.</span></span>
1. <span data-ttu-id="ca116-140">في الصفحة **الانتقاء**، في القسم **الحركات**، حدد البند الذي يتم فيه تعيين الحقل **حالة الإصدار** على *منتقاة*.</span><span class="sxs-lookup"><span data-stu-id="ca116-140">On the **Pick** page, in the **Transactions** section, select the line where the **Issue status** field is set to *Picked*.</span></span>
1. <span data-ttu-id="ca116-141">في القسم **الحركات**، حدد **إضافة بند انتقاء** من شريط الأدوات.</span><span class="sxs-lookup"><span data-stu-id="ca116-141">In the **Transactions** section, select **Add picking line** from the toolbar.</span></span>
1. <span data-ttu-id="ca116-142">في القسم **بنود الانتقاء**، حدد **تأكيد انتقاء الكل** من شريط الأدوات.</span><span class="sxs-lookup"><span data-stu-id="ca116-142">In the **Picking lines** section, select **Confirm pick all** from the toolbar.</span></span>
1. <span data-ttu-id="ca116-143">أغلق صفحة **الانتقاء**.</span><span class="sxs-lookup"><span data-stu-id="ca116-143">Close the **Pick** page.</span></span>
1. <span data-ttu-id="ca116-144">في صفحة تفاصيل أمر المبيعات، في جزء الإجراءات، في علامة التبويب **أمر المبيعات**، في المجموعة **الاحتفاظ**، حدد **إلغاء**.</span><span class="sxs-lookup"><span data-stu-id="ca116-144">On the sales order details page, on the Action Pane, on the **Sales order** tab, in the **Maintain** group, select **Cancel**.</span></span>
1. <span data-ttu-id="ca116-145">حدد **نعم** لتأكيد رغبتك في إلغاء أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="ca116-145">Select **Yes** to confirm that you want to cancel the sales order.</span></span>
