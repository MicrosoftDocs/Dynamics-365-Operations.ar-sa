---
title: بيانات الفاتورة الرئيسية في نظام الحسابات الدائنة باستخدام ‏‫وعاء الفواتير‬
description: سيعرض لك دليل المهام هذا كيفية استخدام سجل الفواتير لإنشاء الفواتير.
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6b870613512a8f4a5c19a0a05cd72b35ea32861b
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843198"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a><span data-ttu-id="aac97-103">بيانات الفاتورة الرئيسية في نظام الحسابات الدائنة باستخدام ‏‫وعاء الفواتير‬</span><span class="sxs-lookup"><span data-stu-id="aac97-103">Key invoice data into the AP system using invoice pool</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="aac97-104">سيعرض لك دليل المهام هذا كيفية استخدام سجل الفواتير لإنشاء الفواتير.</span><span class="sxs-lookup"><span data-stu-id="aac97-104">This task guide will show you how to use the invoice register to create invoices.</span></span>  <span data-ttu-id="aac97-105">بعد ذلك، استخدم وعاء الفواتير لمطابقة الفاتورة مع أمر شراء ووضع الصيغة النهائية للمصروفات في صفحة فاتورة المورّد.</span><span class="sxs-lookup"><span data-stu-id="aac97-105">Then use the invoice pool to match the invoice to a purchase order and finalize the expense in the vendor invoice page.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="aac97-106">إنشاء أمر شراء</span><span class="sxs-lookup"><span data-stu-id="aac97-106">Create a purchase order</span></span>
1. <span data-ttu-id="aac97-107">انتقل إلى الحسابات الدائنة > أوامر الشراء > أوامر الشراء.</span><span class="sxs-lookup"><span data-stu-id="aac97-107">Go to Accounts payable > Purchase orders > Purchase orders.</span></span>
2. <span data-ttu-id="aac97-108">انقر فوق "جديد" لإنشاء أمر شراء.</span><span class="sxs-lookup"><span data-stu-id="aac97-108">Click New to create a purchase order.</span></span>
3. <span data-ttu-id="aac97-109">في الحقل "حساب المورّد‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="aac97-109">In the Vendor account field, click the drop down button to open the lookup.</span></span>
4. <span data-ttu-id="aac97-110">حدد المورد من القائمة.</span><span class="sxs-lookup"><span data-stu-id="aac97-110">Select the vendor from the list.</span></span> <span data-ttu-id="aac97-111">على سبيل المثال، المورّد 1001.</span><span class="sxs-lookup"><span data-stu-id="aac97-111">For example, vendor 1001.</span></span>
5. <span data-ttu-id="aac97-112">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="aac97-112">Click OK.</span></span>
6. <span data-ttu-id="aac97-113">في الحقل "رقم الصنف"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="aac97-113">In the Item number field, click the drop down button to open the lookup.</span></span>
7. <span data-ttu-id="aac97-114">ابحث عن رقم صنف الخدمات في القائمة.</span><span class="sxs-lookup"><span data-stu-id="aac97-114">Find the services item number in the list.</span></span> <span data-ttu-id="aac97-115">على سبيل المثال، حدد S0001.</span><span class="sxs-lookup"><span data-stu-id="aac97-115">For example, select S0001.</span></span>
8. <span data-ttu-id="aac97-116">انقر فوق رقم الصنف وحدده.</span><span class="sxs-lookup"><span data-stu-id="aac97-116">Click on the item number and select it.</span></span>
    * <span data-ttu-id="aac97-117">يبلغ صافي المبلغ 75.00.</span><span class="sxs-lookup"><span data-stu-id="aac97-117">The net amount is 75.00.</span></span>  <span data-ttu-id="aac97-118">وهذا هو المبلغ الذي سنتوقعه على الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="aac97-118">That is the amount that we will expect on the invoice.</span></span>  
9. <span data-ttu-id="aac97-119">في جزء الإجراءات، انقر فوق "شراء‬".</span><span class="sxs-lookup"><span data-stu-id="aac97-119">On the action pane, click Purchase.</span></span>
10. <span data-ttu-id="aac97-120">انقر فوق "تأكيد".</span><span class="sxs-lookup"><span data-stu-id="aac97-120">Click Confirm.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="aac97-121">إنشاء فاتورة وترحيلها</span><span class="sxs-lookup"><span data-stu-id="aac97-121">Create and post and invoice</span></span>
1. <span data-ttu-id="aac97-122">انتقل إلى الحسابات الدائنة > الفواتير > سجل الفواتير.</span><span class="sxs-lookup"><span data-stu-id="aac97-122">Go to Accounts payable > Invoices > Invoice register.</span></span>
2. <span data-ttu-id="aac97-123">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="aac97-123">Click New.</span></span>
3. <span data-ttu-id="aac97-124">افتح البحث لتحديد اسم سجل الفواتير الذي تريد استخدامه.</span><span class="sxs-lookup"><span data-stu-id="aac97-124">Open the lookup to select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="aac97-125">حدد اسم سجل الفواتير الذي تريد استخدامه.</span><span class="sxs-lookup"><span data-stu-id="aac97-125">Select the name of the invoice register that you want to use.</span></span>
5. <span data-ttu-id="aac97-126">انقر فوق "البنود‬" لفتح السجل وإدخال بنود المصروفات.</span><span class="sxs-lookup"><span data-stu-id="aac97-126">Click on Lines to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="aac97-127">في البحث، حدد مورّدًا.</span><span class="sxs-lookup"><span data-stu-id="aac97-127">In the lookup, select a vendor.</span></span> <span data-ttu-id="aac97-128">على سبيل المثال، انقر فوق المورّد 1001.</span><span class="sxs-lookup"><span data-stu-id="aac97-128">For example, click on vendor 1001.</span></span>
7. <span data-ttu-id="aac97-129">في الحقل "الفاتورة"، أدخل رقم الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="aac97-129">In the Invoice field, enter the invoice number.</span></span>
8. <span data-ttu-id="aac97-130">في حقل "الوصف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="aac97-130">In the Description field, type a value.</span></span>
9. <span data-ttu-id="aac97-131">في الحقل "دائن"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="aac97-131">In the Credit field, enter a number.</span></span>
10. <span data-ttu-id="aac97-132">في الحقل "أمر الشراء"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="aac97-132">In the Purchase order field, click the drop down button to open the lookup.</span></span>
11. <span data-ttu-id="aac97-133">حدد أمر الشراء الذي أنشأته سابقًا.</span><span class="sxs-lookup"><span data-stu-id="aac97-133">Select the purchase order that you created earlier.</span></span>
12. <span data-ttu-id="aac97-134">في الحقل "تمت الموافقة بواسطة‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="aac97-134">In the Approved by field, click the drop down button to open the lookup.</span></span>
13. <span data-ttu-id="aac97-135">ميّز أحد المعتمِدين ثم انقر فوق "تحديد" لتحديده.</span><span class="sxs-lookup"><span data-stu-id="aac97-135">Highlight an approver and click Select to select that approver.</span></span>
14. <span data-ttu-id="aac97-136">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="aac97-136">Click Post.</span></span>
15. <span data-ttu-id="aac97-137">وقم بغلق النموذج.</span><span class="sxs-lookup"><span data-stu-id="aac97-137">Close the form.</span></span>
16. <span data-ttu-id="aac97-138">وقم بغلق النموذج.</span><span class="sxs-lookup"><span data-stu-id="aac97-138">Close the form.</span></span>

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a><span data-ttu-id="aac97-139">افتح فاتورة من الوعاء وطابقها مع أمر شراء لإكمال عملية الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="aac97-139">Open an invoice from the pool and match it to a purchase order to complete the invoice process</span></span>
1. <span data-ttu-id="aac97-140">انتقل إلى الحسابات الدائنة > الفواتير > وعاء الفواتير‬.</span><span class="sxs-lookup"><span data-stu-id="aac97-140">Go to Accounts payable > Invoices > Invoice pool.</span></span>
2. <span data-ttu-id="aac97-141">انقر فوق "أمر الشراء" لإنشاء فاتورة مورّد من الفاتورة في الوعاء.</span><span class="sxs-lookup"><span data-stu-id="aac97-141">Click Purchase order to create a vendor invoice from the invoice in the pool.</span></span>
3. <span data-ttu-id="aac97-142">حدد الفاتورة التي تريد مراجعتها.</span><span class="sxs-lookup"><span data-stu-id="aac97-142">Select the invoice that you want to review.</span></span>
4. <span data-ttu-id="aac97-143">انقر فوق "تحديث حالة المطابقة‬" لإكمال المطابقة.</span><span class="sxs-lookup"><span data-stu-id="aac97-143">Click Update match status to complete the matching.</span></span>
5. <span data-ttu-id="aac97-144">في جزء الإجراءات، انقر فوق "خيارات".</span><span class="sxs-lookup"><span data-stu-id="aac97-144">On the action pane, click Options.</span></span>
6. <span data-ttu-id="aac97-145">انقر فوق "تغيير طريقة العرض‬".</span><span class="sxs-lookup"><span data-stu-id="aac97-145">Click Change view.</span></span>
7. <span data-ttu-id="aac97-146">انقر فوق "عرض الشبكة".</span><span class="sxs-lookup"><span data-stu-id="aac97-146">Click Grid view.</span></span>
8. <span data-ttu-id="aac97-147">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="aac97-147">Click Post.</span></span>
9. <span data-ttu-id="aac97-148">وقم بغلق النموذج.</span><span class="sxs-lookup"><span data-stu-id="aac97-148">Close the form.</span></span>
10. <span data-ttu-id="aac97-149">انتقل إلى الحسابات الدائنة > المورّدون > المورّدون.</span><span class="sxs-lookup"><span data-stu-id="aac97-149">Go to Accounts payable > Vendors > Vendors.</span></span>
11. <span data-ttu-id="aac97-150">حدد المورّد الذي كان على أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="aac97-150">Select the vendor that was on the purchase order.</span></span> <span data-ttu-id="aac97-151">على سبيل المثال، حدد المورّد 1001.</span><span class="sxs-lookup"><span data-stu-id="aac97-151">For example, select vendor 1001.</span></span>
12. <span data-ttu-id="aac97-152">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="aac97-152">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="aac97-153">في جزء الإجراءات، انقر فوق "المورّد".</span><span class="sxs-lookup"><span data-stu-id="aac97-153">On the action pane, click Vendor.</span></span>
14. <span data-ttu-id="aac97-154">انقر فوق "الحركات".</span><span class="sxs-lookup"><span data-stu-id="aac97-154">Click Transactions.</span></span>
15. <span data-ttu-id="aac97-155">حدد الفاتورة التي قمت بإنشائها.</span><span class="sxs-lookup"><span data-stu-id="aac97-155">Select the invoice that you created.</span></span>
    * <span data-ttu-id="aac97-156">تم عكس استحقاق سجل الفواتير وترحيله إلى حساب المصروفات الملائم.</span><span class="sxs-lookup"><span data-stu-id="aac97-156">The invoice register accrual was reversed and posted to the appropriate expense account.</span></span>  

