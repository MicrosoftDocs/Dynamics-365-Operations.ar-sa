---
title: بيانات الفاتورة الرئيسية في الحسابات الدائنة باستخدام فاتورة المورد
description: سيساعدك دليل المهمة هذا على إنشاء فاتورة مورّد من أمر شراء وعرض نتائج مطابقة أمر الشراء والإيصال والفاتورة (مطابقة ثلاثية).
author: abruer
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines, VendEditInvoice, InventItemIdLookupSimple, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 20a058eb17bcab11056c91ab3570d6cd5b84b631
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227198"
---
# <a name="key-invoice-data-in-ap-using-a-vendor-invoice"></a><span data-ttu-id="cfdbd-103">بيانات الفاتورة الرئيسية في الحسابات الدائنة باستخدام فاتورة المورد</span><span class="sxs-lookup"><span data-stu-id="cfdbd-103">Key invoice data in AP using a vendor invoice</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cfdbd-104">سيساعدك دليل المهمة هذا على إنشاء فاتورة مورّد من أمر شراء وعرض نتائج مطابقة أمر الشراء والإيصال والفاتورة (مطابقة ثلاثية).</span><span class="sxs-lookup"><span data-stu-id="cfdbd-104">This task guide will help you create a vendor invoice from a purchase order and view the results of matching the purchase order, receipt, and invoice (3 way matching).</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="cfdbd-105">إنشاء أمر شراء</span><span class="sxs-lookup"><span data-stu-id="cfdbd-105">Create a purchase order</span></span>
1. <span data-ttu-id="cfdbd-106">في جزء التنقل، انتقل إلى **الوحدات النمطية > الحسابات الدائنة‬ > أوامر الشراء > جميع أوامر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-106">In the Navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
2. <span data-ttu-id="cfdbd-107">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-107">Click **New**.</span></span>
3. <span data-ttu-id="cfdbd-108">في الحقل **حساب المورّد‬**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-108">In the **Vendor account** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="cfdbd-109">ابحث عن مورّد لتحديده.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-109">Find a vendor to select.</span></span> <span data-ttu-id="cfdbd-110">على سبيل المثال، انتقل لأسفل إلى US-104.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-110">For example, scroll down to US-104.</span></span>
5. <span data-ttu-id="cfdbd-111">حدد المورّد US-104.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-111">Select vendor US-104.</span></span>
6. <span data-ttu-id="cfdbd-112">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-112">Click **OK**.</span></span>
7. <span data-ttu-id="cfdbd-113">في الحقل **رقم الصنف**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-113">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="cfdbd-114">حدد صنف المخزون.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-114">Select an inventory item.</span></span> <span data-ttu-id="cfdbd-115">على سبيل المثال، حدد رقم الصنف 1000.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-115">For example, select item number 1000.</span></span>
9. <span data-ttu-id="cfdbd-116">قم بتوسيع علامة التبويب السريعة **تفاصيل البند**.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-116">Expand the **Line details** fastTab.</span></span>
10. <span data-ttu-id="cfdbd-117">انقر فوق علامة التبويب **الإعداد**. يمكنك تجاوز سياسة المطابقة لاستخدام عدم المطابقة أو سياسة المطابقة الثنائية أو سياسة المطابقة الثلاثية.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-117">Click the **Setup** tab. You can override the matching policy to use no matching, 2-way matching, or 3-way matching.</span></span>  
11. <span data-ttu-id="cfdbd-118">في جزء الإجراءات، انقر فوق **شراء‬**.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-118">On the Action Pane, click **Purchase**.</span></span>
12. <span data-ttu-id="cfdbd-119">انقر فوق **تأكيد**.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-119">Click **Confirm**.</span></span>

## <a name="receive-the-products"></a><span data-ttu-id="cfdbd-120">استلام المنتجات</span><span class="sxs-lookup"><span data-stu-id="cfdbd-120">Receive the products</span></span>
1. <span data-ttu-id="cfdbd-121">في جزء الإجراءات، **انقر فوق استلام**.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-121">On the Action Pane, click **Receive**.</span></span>
2. <span data-ttu-id="cfdbd-122">انقر فوق **إيصال استلام المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-122">Click **Product receipt**.</span></span>
3. <span data-ttu-id="cfdbd-123">في حقل **إيصال استلام المنتجات**، أدخل رقم إيصال استلام المنتجات.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-123">In the **Product receipt** field, enter the product receipt number.</span></span> <span data-ttu-id="cfdbd-124">على سبيل المثال، أدخل PR123.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-124">For example, enter PR123.</span></span>
4. <span data-ttu-id="cfdbd-125">انقر فوق **موافق** لترحيل إيصال استلام المنتجات.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-125">Click **OK** to post the product receipt.</span></span>
5. <span data-ttu-id="cfdbd-126">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-126">Close the page.</span></span>

## <a name="create-a-vendor-invoice"></a><span data-ttu-id="cfdbd-127">إنشاء فاتورة المورّد</span><span class="sxs-lookup"><span data-stu-id="cfdbd-127">Create a vendor invoice</span></span>
1. <span data-ttu-id="cfdbd-128">في جزء التنقل، انتقل إلى **الوحدات النمطية > الحسابات الدائنة‬ > أوامر الشراء > أوامر الشراء التي تم استلامها ولم تتم فوترتها‬**.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-128">In the Navigation pane, go to **Modules > Accounts payable > Purchase orders > Purchase orders received but not invoiced**.</span></span>
2. <span data-ttu-id="cfdbd-129">حدد أمر الشراء الذي أنشأته.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-129">Select the purchase order that you created.</span></span>
3. <span data-ttu-id="cfdbd-130">في جزء الإجراءات، انقر فوق **الفاتورة**.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-130">On the Action Pane, click **Invoice**.</span></span>
4. <span data-ttu-id="cfdbd-131">انقر فوق **الفاتورة‏‎**.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-131">Click **Invoice**.</span></span>
5. <span data-ttu-id="cfdbd-132">في حقل **الرقم**، أدخل رقم الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-132">In the **Number** field, enter the invoice number.</span></span>
6. <span data-ttu-id="cfdbd-133">في حقل **وصف الفاتورة**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-133">In the **Invoice description** field, type a value.</span></span>
7. <span data-ttu-id="cfdbd-134">في الحقل **تاريخ الفاتورة**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-134">In the **Invoice date** field, enter a date.</span></span>
8. <span data-ttu-id="cfdbd-135">في حقل **سعر الوحدة**، أدخل 1200.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-135">In the **Unit price** field, enter 1200.</span></span>
9. <span data-ttu-id="cfdbd-136">انقر فوق **إضافة بند**.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-136">Click **Add line**.</span></span>
10. <span data-ttu-id="cfdbd-137">في الحقل **رقم الصنف**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-137">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="cfdbd-138">في القائمة، ابحث عن رقم صنف تكلفة التثبيت.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-138">In the list, find the installation charge item number.</span></span> <span data-ttu-id="cfdbd-139">على سبيل المثال، S0001</span><span class="sxs-lookup"><span data-stu-id="cfdbd-139">For example, S0001</span></span>
12. <span data-ttu-id="cfdbd-140">حدد رقم صنف تكلفة التثبيت.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-140">Select the installation charge item number.</span></span> <span data-ttu-id="cfdbd-141">لاحظ أن المطابقة لم يتم تنفيذها منذ قيامك بإدخال التغييرات.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-141">Note that matching has not been performed since you made the changes.</span></span>  
13. <span data-ttu-id="cfdbd-142">انقر فوق **تحديث حالة المطابقة**.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-142">Click **Update match status**.</span></span>
14. <span data-ttu-id="cfdbd-143">في جزء الإجراءات، انقر فوق **مراجعة**.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-143">On the Action Pane, click **Review**.</span></span>
15. <span data-ttu-id="cfdbd-144">انقر فوق **تفاصيل المطابقة**.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-144">Click **Matching details**.</span></span> <span data-ttu-id="cfdbd-145">لا حاجة إلى مطابقة البند الجديد حتى تبقى الحالة "لم يتم التنفيذ‬".</span><span class="sxs-lookup"><span data-stu-id="cfdbd-145">The new line with services does not need to be matched so the status stays "Not performed".</span></span>  
16. <span data-ttu-id="cfdbd-146">حدد إيصال استلام المنتجات لصنف المخزون الذي تلقيته.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-146">Select the product receipt for the inventory item that you received.</span></span> <span data-ttu-id="cfdbd-147">تمت مطابقة البند مع إيصال استلام المنتج، ولكن يوجد عدم تطابق في السعر أو الكمية وهذا سبب الفشل.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-147">The line with the product receipt was matched but there is a mismatch of quantity or price so it fails.</span></span>  
17. <span data-ttu-id="cfdbd-148">في حقل **سعر الوحدة**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-148">In the **Unit price** field, enter a number.</span></span> <span data-ttu-id="cfdbd-149">الآن بعد أن أصبح سعر الوحدة مطابقًا، تم تحديث الحالة إلى "تم الاجتياز‬".</span><span class="sxs-lookup"><span data-stu-id="cfdbd-149">Now that the unit price matches, the status is updated to Passed.</span></span> <span data-ttu-id="cfdbd-150">إذا كانت سياستك تسمح بوجود اختلافات أو إذا كانت المطابقة عبارة عن مجرد تحذير، فلا يزال بإمكانك ترحيل الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-150">If your policy allows discrepancies or if matching is only a warning, you can still post the invoice.</span></span>  
18. <span data-ttu-id="cfdbd-151">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-151">Close the page.</span></span>
19. <span data-ttu-id="cfdbd-152">انقر فوق **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-152">Click **Post**.</span></span>
20. <span data-ttu-id="cfdbd-153">وقم بغلق النموذج.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-153">Close the form.</span></span> <span data-ttu-id="cfdbd-154">لاحظ أن أمر الشراء لم يعد مدرجًا على أنه تم استلامه ولكن بدون فوترة.‬</span><span class="sxs-lookup"><span data-stu-id="cfdbd-154">Note that the purchase order is no longer listed as received but not invoiced.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]