---
title: إعداد سياسات فواتير المورِّدين
description: يتم تشغيل سياسات فاتورة المورّد عند ترحيل فاتورة مورّد باستخدام صفحة "فاتورة المورّد" وعند فتح صفحة "مخالفات سياسة فاتورة المورّد"‬.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b424eee7c91ef1085c98828c0d5e5cf674717a81
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "323170"
---
# <a name="set-up-vendor-invoice-policies"></a><span data-ttu-id="2cbc8-103">إعداد سياسات فواتير المورِّدين</span><span class="sxs-lookup"><span data-stu-id="2cbc8-103">Set up vendor invoice policies</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2cbc8-104">يتم تشغيل سياسات فاتورة المورّد عند ترحيل فاتورة مورّد باستخدام صفحة "فاتورة المورّد" وعند فتح صفحة "مخالفات سياسة فاتورة المورّد"‬.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-104">Vendor invoice policies are run when you post a vendor invoice by using the Vendor invoice page and when you open the vendor invoice Policy violations page.</span></span> <span data-ttu-id="2cbc8-105">يمكنك أيضًا تكوين سير عمل فاتورة المورّد لتشغيل سياسات فواتير المورّدين في كل وقت تقوم فيه بإرسال فاتورة إلى سير العمل.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-105">You can also configure the vendor invoice workflow to run vendor invoice policies every time that you submit an invoice to workflow.</span></span> 

<span data-ttu-id="2cbc8-106">لا تنطبق سياسات فواتير المورّدين على الفواتير التي تم إنشاؤها في سجل الفواتير‬ أو دفتر يومية الفواتير‬.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-106">Vendor invoice policies do not apply to invoices that were created in the invoice register or invoice journal.</span></span> 

<span data-ttu-id="2cbc8-107">لا تستخدم عملية التحقق من مطابقة الفاتورة سياسات فواتير المورِّدين‬، ولكن يتم إعدادها بدلاً من ذلك في صفحة "محددات الحسابات الدائنة‬".</span><span class="sxs-lookup"><span data-stu-id="2cbc8-107">Invoice matching validation does not use vendor invoice policies, but is instead set up in the Accounts payable parameters page.</span></span>

<span data-ttu-id="2cbc8-108">يستخدم هذا التسجيل شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-108">This recording uses the USMF demo company.</span></span> <span data-ttu-id="2cbc8-109">قد ينفذ دور مدير الحسابات الدائنة أو دور مدير الحسابات‬ هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-109">The accounts payable manager or accounting manager role would perform these steps.</span></span> <span data-ttu-id="2cbc8-110">قبل أن تبدأ، تأكد من تحديد مفتاح تكوين مطابقة الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-110">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span>


## <a name="prepare-to-create-vendor-invoice-policies"></a><span data-ttu-id="2cbc8-111">التحضير لإنشاء سياسات فواتير المورّدين</span><span class="sxs-lookup"><span data-stu-id="2cbc8-111">Prepare to create vendor invoice policies</span></span>
1. <span data-ttu-id="2cbc8-112">انتقل إلى الحسابات الدائنة > إعداد > محددات الحسابات الدائنة.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-112">Go to Accounts payable > Setup > Accounts payable parameters.</span></span>
2. <span data-ttu-id="2cbc8-113">انقر فوق علامة التبويب "التحقق من صحة الفواتير".</span><span class="sxs-lookup"><span data-stu-id="2cbc8-113">Click the Invoice validation tab.</span></span>
3. <span data-ttu-id="2cbc8-114">حدد أو امسح خانة الاختيار "التحديث التلقائي لحالة رأس الفاتورة‬".</span><span class="sxs-lookup"><span data-stu-id="2cbc8-114">Select or clear the Automatically update invoice header status check box.</span></span>
4. <span data-ttu-id="2cbc8-115">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-115">Click OK.</span></span>
5. <span data-ttu-id="2cbc8-116">في الحقل "ترحيل الفاتورة التي بها اختلافات"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-116">In the Post invoice with discrepancies field, select an option.</span></span>
6. <span data-ttu-id="2cbc8-117">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-117">Close the page.</span></span>
7. <span data-ttu-id="2cbc8-118">انتقل إلى الحسابات الدائنة > إعداد السياسة > سياسات فواتير المورّدين.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-118">Go to Accounts payable > Policy setup > Vendor invoice policies.</span></span>
8. <span data-ttu-id="2cbc8-119">انقر فوق "المحددات".</span><span class="sxs-lookup"><span data-stu-id="2cbc8-119">Click Parameters.</span></span>
9. <span data-ttu-id="2cbc8-120">انقر فوق btnAdd.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-120">Click btnAdd.</span></span>
10. <span data-ttu-id="2cbc8-121">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-121">Close the page.</span></span>

## <a name="create-policy-rule-types-for-vendor-invoices"></a><span data-ttu-id="2cbc8-122">إنشاء أنواع قواعد سياسات لفواتير المورّدين</span><span class="sxs-lookup"><span data-stu-id="2cbc8-122">Create policy rule types for vendor invoices</span></span>
1. <span data-ttu-id="2cbc8-123">انتقل إلى الحسابات الدائنة > إعداد السياسة > أنواع قاعدة سياسة فاتورة المورّد‬.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-123">Go to Accounts payable > Policy setup > Vendor invoice policy rule types.</span></span>
2. <span data-ttu-id="2cbc8-124">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="2cbc8-124">Click New.</span></span>
3. <span data-ttu-id="2cbc8-125">في الحقل "اسم القاعدة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-125">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="2cbc8-126">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-126">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2cbc8-127">في الحقل "اسم الاستعلام"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-127">In the Query name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="2cbc8-128">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-128">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="2cbc8-129">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-129">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="2cbc8-130">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="2cbc8-130">Click Save.</span></span>
9. <span data-ttu-id="2cbc8-131">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-131">Close the page.</span></span>

## <a name="define-a-vendor-invoice-policy"></a><span data-ttu-id="2cbc8-132">تعريف سياسة فاتورة المورّد</span><span class="sxs-lookup"><span data-stu-id="2cbc8-132">Define a vendor invoice policy</span></span>
1. <span data-ttu-id="2cbc8-133">انتقل إلى الحسابات الدائنة > إعداد السياسة > سياسات فواتير المورّدين.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-133">Go to Accounts payable > Policy setup > Vendor invoice policies.</span></span>
2. <span data-ttu-id="2cbc8-134">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="2cbc8-134">Click New.</span></span>
3. <span data-ttu-id="2cbc8-135">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-135">In the Name field, type a value.</span></span>
4. <span data-ttu-id="2cbc8-136">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-136">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2cbc8-137">قم بتوسيع المقطع "مؤسسات السياسات‬" أو طيّه.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-137">Expand or collapse the Policy organizations section.</span></span>
6. <span data-ttu-id="2cbc8-138">في الشجرة، حدد '"Contoso Entertainment System USA".</span><span class="sxs-lookup"><span data-stu-id="2cbc8-138">In the tree, select 'Contoso Entertainment System USA'.</span></span>
7. <span data-ttu-id="2cbc8-139">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-139">Click Add.</span></span>
8. <span data-ttu-id="2cbc8-140">قم بتوسيع المقطع "قواعد السياسة‬" أو طيّه.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-140">Expand or collapse the Policy rules section.</span></span>
9. <span data-ttu-id="2cbc8-141">انقر فوق "إنشاء قاعدة السياسة".</span><span class="sxs-lookup"><span data-stu-id="2cbc8-141">Click Create policy rule.</span></span>
10. <span data-ttu-id="2cbc8-142">في الحقل "وصف قاعدة السياسة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-142">In the Policy rule description field, type a value.</span></span>
11. <span data-ttu-id="2cbc8-143">انقر فوق "عامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="2cbc8-143">Click Filter.</span></span>
12. <span data-ttu-id="2cbc8-144">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-144">Click Add.</span></span>
13. <span data-ttu-id="2cbc8-145">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-145">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="2cbc8-146">في الحقل "الجدول‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-146">In the Table field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="2cbc8-147">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-147">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="2cbc8-148">في الحقل "جدول مشتق"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-148">In the Derived table field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="2cbc8-149">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-149">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="2cbc8-150">في حقل "الحقل"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-150">In the Field field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="2cbc8-151">في حقل "الحقل" اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-151">In the Field field, type a value.</span></span>
20. <span data-ttu-id="2cbc8-152">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-152">Close the page.</span></span>
21. <span data-ttu-id="2cbc8-153">في الحقل "المعايير"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-153">In the Criteria field, type a value.</span></span>
22. <span data-ttu-id="2cbc8-154">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="2cbc8-154">Click OK.</span></span>
23. <span data-ttu-id="2cbc8-155">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="2cbc8-155">Click OK.</span></span>
24. <span data-ttu-id="2cbc8-156">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-156">Close the page.</span></span>
25. <span data-ttu-id="2cbc8-157">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-157">Close the page.</span></span>

