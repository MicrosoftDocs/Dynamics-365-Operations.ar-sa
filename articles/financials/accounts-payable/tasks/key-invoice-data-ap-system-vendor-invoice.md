--- 
title: "بيانات الفاتورة الرئيسية في الحسابات الدائنة باستخدام فاتورة المورد"
description: "سيساعدك دليل المهمة هذا على إنشاء فاتورة مورّد من أمر شراء وعرض نتائج مطابقة أمر الشراء والإيصال والفاتورة (مطابقة ثلاثية)."
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: fcec579b295852a46723fb115a3a7bc356e5b80a
ms.contentlocale: ar-sa
ms.lasthandoff: 08/07/2018

---
# <a name="key-invoice-data-into-accounts-payable-using-a-vendor-invoice"></a><span data-ttu-id="bbf7d-103">بيانات الفاتورة الرئيسية في الحسابات الدائنة باستخدام فاتورة المورد</span><span class="sxs-lookup"><span data-stu-id="bbf7d-103">Key invoice data into accounts payable using a vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bbf7d-104">سيساعدك دليل المهمة هذا على إنشاء فاتورة مورّد من أمر شراء وعرض نتائج مطابقة أمر الشراء والإيصال والفاتورة (مطابقة ثلاثية).</span><span class="sxs-lookup"><span data-stu-id="bbf7d-104">This task guide will help you create a vendor invoice from a purchase order and view the results of matching the purchase order, receipt, and invoice (3 way matching).</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="bbf7d-105">إنشاء أمر شراء</span><span class="sxs-lookup"><span data-stu-id="bbf7d-105">Create a purchase order</span></span>
1. <span data-ttu-id="bbf7d-106">انتقل إلى الحسابات الدائنة > أوامر الشراء > جميع أوامر الشراء.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-106">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="bbf7d-107">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="bbf7d-107">Click New.</span></span>
3. <span data-ttu-id="bbf7d-108">في الحقل "حساب المورّد‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-108">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="bbf7d-109">ابحث عن مورّد لتحديده.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-109">Find a vendor to select.</span></span> <span data-ttu-id="bbf7d-110">على سبيل المثال، انتقل لأسفل إلى US-104.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-110">For example, scroll down to US-104.</span></span>
5. <span data-ttu-id="bbf7d-111">حدد المورّد US-104.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-111">Select vendor US-104.</span></span>
6. <span data-ttu-id="bbf7d-112">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-112">Click OK.</span></span>
7. <span data-ttu-id="bbf7d-113">في الحقل "رقم الصنف"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-113">In the Item number field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="bbf7d-114">حدد صنف المخزون.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-114">Select an inventory item.</span></span> <span data-ttu-id="bbf7d-115">على سبيل المثال، حدد رقم الصنف 1000.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-115">For example, select item number 1000.</span></span>
9. <span data-ttu-id="bbf7d-116">قم بتوسيع المقطع "تفاصيل البند" أو طيّه.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-116">Expand or collapse the Line details section.</span></span>
10. <span data-ttu-id="bbf7d-117">انقر فوق علامة التبويب "إعداد".</span><span class="sxs-lookup"><span data-stu-id="bbf7d-117">Click the Setup tab.</span></span>
    * <span data-ttu-id="bbf7d-118">يمكنك تجاوز سياسة المطابقة لاستخدام عدم المطابقة أو سياسة المطابقة الثنائية أو سياسة المطابقة الثلاثية.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-118">You can override the matching policy to use no matching, 2-way matching, or 3-way matching.</span></span>  
11. <span data-ttu-id="bbf7d-119">قم بتوسيع المقطع "تفاصيل البند" أو طيّه.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-119">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="bbf7d-120">في جزء الإجراءات، انقر فوق "شراء".</span><span class="sxs-lookup"><span data-stu-id="bbf7d-120">On the Action Pane, click Purchase.</span></span>
13. <span data-ttu-id="bbf7d-121">انقر فوق "تأكيد".</span><span class="sxs-lookup"><span data-stu-id="bbf7d-121">Click Confirm.</span></span>

## <a name="receive-the-products"></a><span data-ttu-id="bbf7d-122">استلام المنتجات</span><span class="sxs-lookup"><span data-stu-id="bbf7d-122">Receive the products</span></span>
1. <span data-ttu-id="bbf7d-123">في جزء الإجراءات، انقر فوق "استلام".</span><span class="sxs-lookup"><span data-stu-id="bbf7d-123">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="bbf7d-124">انقر فوق "إيصال استلام المنتجات".</span><span class="sxs-lookup"><span data-stu-id="bbf7d-124">Click Product receipt.</span></span>
3. <span data-ttu-id="bbf7d-125">في حقل "إيصال استلام المنتجات"، أدخل رقم إيصال استلام المنتجات.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-125">In the Product receipt field, enter the product receipt number.</span></span> <span data-ttu-id="bbf7d-126">على سبيل المثال، أدخل PR123.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-126">For example, enter PR123.</span></span>
4. <span data-ttu-id="bbf7d-127">انقر فوق "موافق" لترحيل إيصال استلام المنتجات.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-127">Click OK to post the product receipt.</span></span>
5. <span data-ttu-id="bbf7d-128">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-128">Close the page.</span></span>

## <a name="create-a-vendor-invoice"></a><span data-ttu-id="bbf7d-129">إنشاء فاتورة المورّد</span><span class="sxs-lookup"><span data-stu-id="bbf7d-129">Create a vendor invoice</span></span>
1. <span data-ttu-id="bbf7d-130">انتقل إلى الحسابات الدائنة > أوامر الشراء > أوامر الشراء التي تم استلامها ولم تتم فوترتها‬.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-130">Go to Accounts payable > Purchase orders > Purchase orders received but not invoiced.</span></span>
2. <span data-ttu-id="bbf7d-131">حدد أمر الشراء الذي أنشأته.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-131">Select the purchase order that you created.</span></span>
3. <span data-ttu-id="bbf7d-132">في جزء الإجراءات، انقر فوق "فاتورة".</span><span class="sxs-lookup"><span data-stu-id="bbf7d-132">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="bbf7d-133">انقر فوق "فاتورة".</span><span class="sxs-lookup"><span data-stu-id="bbf7d-133">Click Invoice.</span></span>
5. <span data-ttu-id="bbf7d-134">في حقل "الرقم"، قم بإدخال رقم الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-134">In the Number field, enter the invoice number.</span></span>
6. <span data-ttu-id="bbf7d-135">في حقل وصف الفاتورة، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-135">In the Invoice description field, type a value.</span></span>
7. <span data-ttu-id="bbf7d-136">في حقل تاريخ الفاتورة، قم بإدخال تاريخ.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-136">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="bbf7d-137">في حقل "سعر الوحدة"، أدخل 1200.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-137">In the Unit price field, enter 1200.</span></span>
9. <span data-ttu-id="bbf7d-138">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="bbf7d-138">Click Add line.</span></span>
10. <span data-ttu-id="bbf7d-139">في الحقل "رقم الصنف"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-139">In the Item number field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="bbf7d-140">في القائمة، ابحث عن رقم صنف تكلفة التثبيت.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-140">In the list, find the installation charge item number.</span></span> <span data-ttu-id="bbf7d-141">على سبيل المثال، S0001</span><span class="sxs-lookup"><span data-stu-id="bbf7d-141">For example, S0001</span></span>
12. <span data-ttu-id="bbf7d-142">حدد رقم صنف تكلفة التثبيت.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-142">Select the installation charge item number.</span></span>
    * <span data-ttu-id="bbf7d-143">لاحظ أن المطابقة لم يتم تنفيذها منذ قيامك بإدخال التغييرات.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-143">Note that matching has not been performed since you made the changes.</span></span>  
13. <span data-ttu-id="bbf7d-144">انقر فوق تحديث حالة المطابقة.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-144">Click Update match status.</span></span>
14. <span data-ttu-id="bbf7d-145">في جزء الإجراءات، انقر فوق "مراجعة".</span><span class="sxs-lookup"><span data-stu-id="bbf7d-145">On the Action Pane, click Review.</span></span>
15. <span data-ttu-id="bbf7d-146">انقر فوق "تفاصيل المطابقة".</span><span class="sxs-lookup"><span data-stu-id="bbf7d-146">Click Matching details.</span></span>
    * <span data-ttu-id="bbf7d-147">لا حاجة إلى مطابقة البند الجديد حتى تبقى الحالة "لم يتم التنفيذ‬".</span><span class="sxs-lookup"><span data-stu-id="bbf7d-147">The new line with services does not need to be matched so the status stays "Not performed".</span></span>  
16. <span data-ttu-id="bbf7d-148">حدد إيصال استلام المنتجات لصنف المخزون الذي تلقيته.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-148">Select the product receipt for the inventory item that you received.</span></span>
    * <span data-ttu-id="bbf7d-149">تمت مطابقة البند مع إيصال استلام المنتج، ولكن يوجد عدم تطابق في السعر أو الكمية وهذا سبب الفشل.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-149">The line with the product receipt was matched but there is a mismatch of quantity or price so it fails.</span></span>  
17. <span data-ttu-id="bbf7d-150">في حقل "سعر الوحدة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-150">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="bbf7d-151">الآن بعد أن أصبح سعر الوحدة مطابقًا، تم تحديث الحالة إلى "تم الاجتياز‬".</span><span class="sxs-lookup"><span data-stu-id="bbf7d-151">Now that the unit price matches, the status is updated to Passed.</span></span> <span data-ttu-id="bbf7d-152">إذا كانت سياستك تسمح بوجود اختلافات أو إذا كانت المطابقة عبارة عن مجرد تحذير، فلا يزال بإمكانك ترحيل الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-152">If your policy allows discrepancies or if matching is only a warning, you can still post the invoice.</span></span>  
18. <span data-ttu-id="bbf7d-153">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-153">Close the page.</span></span>
19. <span data-ttu-id="bbf7d-154">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="bbf7d-154">Click Post.</span></span>
20. <span data-ttu-id="bbf7d-155">وقم بغلق النموذج.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-155">Close the form.</span></span>
    * <span data-ttu-id="bbf7d-156">لاحظ أن أمر الشراء لم يعد مدرجًا على أنه تم استلامه ولكن بدون فوترة.‬</span><span class="sxs-lookup"><span data-stu-id="bbf7d-156">Note that the purchase order is no longer listed as received but not invoiced.</span></span>  


