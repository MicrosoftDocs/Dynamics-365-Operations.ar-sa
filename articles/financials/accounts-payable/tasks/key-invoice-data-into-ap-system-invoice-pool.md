---
title: بيانات الفاتورة الرئيسية في نظام الحسابات الدائنة باستخدام ‏‫وعاء الفواتير‬
description: يصف هذا الموضوع كيفية استخدام السجل لإنشاء الفواتير.
author: abruer
manager: AnnBe
ms.date: 07/31/2019
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
ms.openlocfilehash: f7d72c1d98100d1313109e8b5e55df02e2163174
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867692"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a><span data-ttu-id="584c8-103">بيانات الفاتورة الرئيسية في نظام الحسابات الدائنة باستخدام ‏‫وعاء الفواتير‬</span><span class="sxs-lookup"><span data-stu-id="584c8-103">Key invoice data into the AP system using invoice pool</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="584c8-104">يصف هذا الموضوع كيفية استخدام السجل لإنشاء الفواتير.</span><span class="sxs-lookup"><span data-stu-id="584c8-104">This topic describes how to use the invoice register to create invoices.</span></span> <span data-ttu-id="584c8-105">بعد ذلك، استخدم وعاء الفواتير لمطابقة الفاتورة مع أمر شراء ووضع الصيغة النهائية للمصروفات في صفحة فاتورة المورّد.</span><span class="sxs-lookup"><span data-stu-id="584c8-105">Then use the invoice pool to match the invoice to a purchase order and finalize the expense in the vendor invoice page.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="584c8-106">إنشاء أمر شراء</span><span class="sxs-lookup"><span data-stu-id="584c8-106">Create a purchase order</span></span>
1. <span data-ttu-id="584c8-107">في جزء التنقل، انتقل إلى **الوحدات النمطية > الحسابات الدائنة‬ > أوامر الشراء > أوامر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="584c8-107">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > Purchase orders**.</span></span>
2. <span data-ttu-id="584c8-108">حدد **جديد** لإنشاء أمر شراء.</span><span class="sxs-lookup"><span data-stu-id="584c8-108">Select **New** to create a purchase order.</span></span>
3. <span data-ttu-id="584c8-109">في الحقل **حساب المورّد‬**، حدد مورّدًا من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="584c8-109">In the **Vendor account** field, select a vendor for the drop-down list.</span></span> <span data-ttu-id="584c8-110">على سبيل المثال، حدد المورّد **1001**.</span><span class="sxs-lookup"><span data-stu-id="584c8-110">For example, select vendor **1001**.</span></span>
4. <span data-ttu-id="584c8-111">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="584c8-111">Select **OK**.</span></span>
5. <span data-ttu-id="584c8-112">في الحقل **رقم الصنف**، حدد رقم صنف الخدمات من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="584c8-112">In the **Item number** field, select the services item number in the drop-down list.</span></span> <span data-ttu-id="584c8-113">على سبيل المثال، حدد **S0001**.</span><span class="sxs-lookup"><span data-stu-id="584c8-113">For example, select **S0001**.</span></span> <span data-ttu-id="584c8-114">يبلغ صافي المبلغ 75.00.</span><span class="sxs-lookup"><span data-stu-id="584c8-114">The net amount is 75.00.</span></span>  <span data-ttu-id="584c8-115">وهذا هو المبلغ الذي سنتوقعه على الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="584c8-115">That is the amount that we will expect on the invoice.</span></span>  
6. <span data-ttu-id="584c8-116">في جزء الإجراءات، حدد **شراء**.</span><span class="sxs-lookup"><span data-stu-id="584c8-116">On the action pane, select **Purchase**.</span></span>
7. <span data-ttu-id="584c8-117">حدد **تأكيد**.</span><span class="sxs-lookup"><span data-stu-id="584c8-117">Select **Confirm**.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="584c8-118">إنشاء فاتورة وترحيلها</span><span class="sxs-lookup"><span data-stu-id="584c8-118">Create and post and invoice</span></span>
1. <span data-ttu-id="584c8-119">في جزء التنقل، انتقل إلى **الوحدات النمطية > الحسابات الدائنة > الفواتير > سجل الفواتير**.</span><span class="sxs-lookup"><span data-stu-id="584c8-119">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice register**.</span></span>
2. <span data-ttu-id="584c8-120">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="584c8-120">Select **New**.</span></span>
3. <span data-ttu-id="584c8-121">افتح البحث لتحديد اسم سجل الفواتير الذي تريد استخدامه.</span><span class="sxs-lookup"><span data-stu-id="584c8-121">Open the lookup to select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="584c8-122">حدد اسم سجل الفواتير الذي تريد استخدامه.</span><span class="sxs-lookup"><span data-stu-id="584c8-122">Select the name of the invoice register that you want to use.</span></span>
5. <span data-ttu-id="584c8-123">حدد **البنود‬** لفتح السجل وإدخال بنود المصروفات.</span><span class="sxs-lookup"><span data-stu-id="584c8-123">Select **Lines** to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="584c8-124">في البحث، حدد مورّدًا.</span><span class="sxs-lookup"><span data-stu-id="584c8-124">In the lookup, select a vendor.</span></span> <span data-ttu-id="584c8-125">على سبيل المثال، حدد المورّد **1001**.</span><span class="sxs-lookup"><span data-stu-id="584c8-125">For example, select vendor **1001**.</span></span>
7. <span data-ttu-id="584c8-126">في الحقل **الفاتورة**، أدخل رقم الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="584c8-126">In the **Invoice** field, enter the invoice number.</span></span>
8. <span data-ttu-id="584c8-127">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="584c8-127">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="584c8-128">في الحقل **دائن**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="584c8-128">In the **Credit** field, enter a number.</span></span>
10. <span data-ttu-id="584c8-129">في حقل **أمر الشراء**، افتح القائمة المنسدلة لتحديد أمر الشراء الذي أنشأته في وقت سابق.</span><span class="sxs-lookup"><span data-stu-id="584c8-129">In the **Purchase order** field, open the drop-down list to select the purchase order that you created earlier.</span></span>
11. <span data-ttu-id="584c8-130">في الحقل **تمت الموافقة بواسطة**، قم بتمييز المعتمد في القائمة المنسدلة وانقر فوق **تحديد** لتحديد ذلك المعتمد.</span><span class="sxs-lookup"><span data-stu-id="584c8-130">In the **Approved by** field, highlight an approver in the drop-down list and click **Select** to select that approver.</span></span>
12. <span data-ttu-id="584c8-131">حدد **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="584c8-131">Select **Post**.</span></span>

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a><span data-ttu-id="584c8-132">افتح فاتورة من الوعاء وطابقها مع أمر شراء لإكمال عملية الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="584c8-132">Open an invoice from the pool and match it to a purchase order to complete the invoice process</span></span>
1. <span data-ttu-id="584c8-133">في جزء التنقل، انتقل إلى **الوحدات النمطية > الحسابات الدائنة > الفواتير > وعاء الفواتير**.</span><span class="sxs-lookup"><span data-stu-id="584c8-133">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice pool**.</span></span>
2. <span data-ttu-id="584c8-134">حدد **أمر الشراء** لإنشاء فاتورة مورّد من الفاتورة في الوعاء.</span><span class="sxs-lookup"><span data-stu-id="584c8-134">Select **Purchase order** to create a vendor invoice from the invoice in the pool.</span></span>
3. <span data-ttu-id="584c8-135">حدد الفاتورة التي تريد مراجعتها.</span><span class="sxs-lookup"><span data-stu-id="584c8-135">Select the invoice that you want to review.</span></span>
4. <span data-ttu-id="584c8-136">حدد **تحديث حالة المطابقة‬** لإكمال المطابقة.</span><span class="sxs-lookup"><span data-stu-id="584c8-136">Select **Update match status** to complete the matching.</span></span>
5. <span data-ttu-id="584c8-137">في جزء الإجراءات، حدد **خيارات**.</span><span class="sxs-lookup"><span data-stu-id="584c8-137">On the action pane, select **Options**.</span></span>
6. <span data-ttu-id="584c8-138">حدد **تغيير طريقة العرض**.</span><span class="sxs-lookup"><span data-stu-id="584c8-138">Select **Change view**.</span></span>
7. <span data-ttu-id="584c8-139">حدد **طريقة عرض الشبكة‬**.</span><span class="sxs-lookup"><span data-stu-id="584c8-139">Select **Grid view**.</span></span>
8. <span data-ttu-id="584c8-140">حدد **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="584c8-140">Select **Post**.</span></span>
9. <span data-ttu-id="584c8-141">وقم بغلق النموذج.</span><span class="sxs-lookup"><span data-stu-id="584c8-141">Close the form.</span></span>
10. <span data-ttu-id="584c8-142">في جزء التنقل، انتقل إلى **الوحدات النمطية > الحسابات الدائنة > المورّدون > المورّدون**.</span><span class="sxs-lookup"><span data-stu-id="584c8-142">In the navigation pane, go to **Modules > Accounts payable > Vendors > Vendors**.</span></span>
11. <span data-ttu-id="584c8-143">حدد المورّد الذي كان على أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="584c8-143">Select the vendor that was on the purchase order.</span></span> <span data-ttu-id="584c8-144">على سبيل المثال، حدد المورّد **1001**.</span><span class="sxs-lookup"><span data-stu-id="584c8-144">For example, select vendor **1001**.</span></span>
12. <span data-ttu-id="584c8-145">في جزء الإجراءات، حدد **المورّد**.</span><span class="sxs-lookup"><span data-stu-id="584c8-145">On the action pane, select **Vendor**.</span></span>
13. <span data-ttu-id="584c8-146">حدد **الحركات**.</span><span class="sxs-lookup"><span data-stu-id="584c8-146">Select **Transactions**.</span></span>
14. <span data-ttu-id="584c8-147">حدد الفاتورة التي قمت بإنشائها.</span><span class="sxs-lookup"><span data-stu-id="584c8-147">Select the invoice that you created.</span></span> <span data-ttu-id="584c8-148">تم عكس استحقاق سجل الفواتير وترحيله إلى حساب المصروفات الملائم.</span><span class="sxs-lookup"><span data-stu-id="584c8-148">The invoice register accrual was reversed and posted to the appropriate expense account.</span></span>  

