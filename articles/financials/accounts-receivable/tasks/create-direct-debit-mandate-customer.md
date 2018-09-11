--- 
title: "إنشاء تفويض خصم مباشر لعميل"
description: "توضح هذه المهمة كيفية إنشاء تفويض خصم مباشر واستخدامه في الفاتورة."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 4b3d9e10e176879a6c474ec0bff513c6008bc3a9
ms.contentlocale: ar-sa
ms.lasthandoff: 09/11/2018

---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a><span data-ttu-id="b8fb7-103">إنشاء تفويض خصم مباشر لعميل</span><span class="sxs-lookup"><span data-stu-id="b8fb7-103">Create a direct debit mandate for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b8fb7-104">توضح هذه المهمة كيفية إنشاء تفويض خصم مباشر واستخدامه في الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="b8fb7-104">This task guide demonstrates how to create a direct debit mandate and use it on an invoice.</span></span>


## <a name="create-a-bank-account"></a><span data-ttu-id="b8fb7-105">إنشاء حساب بنكي</span><span class="sxs-lookup"><span data-stu-id="b8fb7-105">Create a bank account</span></span>
1. <span data-ttu-id="b8fb7-106">انتقل إلى الحسابات المدينة > العملاء > كافة العملاء‬.</span><span class="sxs-lookup"><span data-stu-id="b8fb7-106">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="b8fb7-107">على سبيل المثال، حدد US-001</span><span class="sxs-lookup"><span data-stu-id="b8fb7-107">For example, select US-001</span></span>
3. <span data-ttu-id="b8fb7-108">في جزء الإجراءات، انقر فوق "العميل".</span><span class="sxs-lookup"><span data-stu-id="b8fb7-108">On the Action Pane, click Customer.</span></span>
4. <span data-ttu-id="b8fb7-109">انتقل إلى "الحسابات البنكية".</span><span class="sxs-lookup"><span data-stu-id="b8fb7-109">Click Bank accounts.</span></span>
5. <span data-ttu-id="b8fb7-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="b8fb7-110">Click New.</span></span>
6. <span data-ttu-id="b8fb7-111">في الحقل "الحساب البنكي"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b8fb7-111">In the Bank account field, type a value.</span></span>
7. <span data-ttu-id="b8fb7-112">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b8fb7-112">In the Name field, type a value.</span></span>
8. <span data-ttu-id="b8fb7-113">في الحقل "IBAN‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b8fb7-113">In the IBAN field, type a value.</span></span>
9. <span data-ttu-id="b8fb7-114">في الحقل "العملة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b8fb7-114">In the Currency field, type a value.</span></span>
10. <span data-ttu-id="b8fb7-115">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="b8fb7-115">Click Save.</span></span>
11. <span data-ttu-id="b8fb7-116">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b8fb7-116">Close the page.</span></span>
12. <span data-ttu-id="b8fb7-117">انتقل إلى إدارة النقد والبنوك > الحسابات البنكية > الحسابات البنكية.</span><span class="sxs-lookup"><span data-stu-id="b8fb7-117">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
13. <span data-ttu-id="b8fb7-118">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="b8fb7-118">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="b8fb7-119">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="b8fb7-119">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="b8fb7-120">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="b8fb7-120">Click Edit.</span></span>
16. <span data-ttu-id="b8fb7-121">‏‫قم بتوسيع المقطع "تعريف إضافي".</span><span class="sxs-lookup"><span data-stu-id="b8fb7-121">Expand the Additional identification section.</span></span>
17. <span data-ttu-id="b8fb7-122">في حقل "‏‫معرف الدين المباشر‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b8fb7-122">In the Direct debit ID field, type a value.</span></span>
18. <span data-ttu-id="b8fb7-123">في الحقل "IBAN‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b8fb7-123">In the IBAN field, type a value.</span></span>
19. <span data-ttu-id="b8fb7-124">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b8fb7-124">Close the page.</span></span>
20. <span data-ttu-id="b8fb7-125">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b8fb7-125">Close the page.</span></span>

## <a name="define-the-electronic-payment-method"></a><span data-ttu-id="b8fb7-126">تحديد طريقة الدفع الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="b8fb7-126">Define the electronic payment method</span></span>
1. <span data-ttu-id="b8fb7-127">انتقل إلى الحسابات المدينة > إعداد الدفعات > طرق الدفع.</span><span class="sxs-lookup"><span data-stu-id="b8fb7-127">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="b8fb7-128">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="b8fb7-128">Click New.</span></span>
3. <span data-ttu-id="b8fb7-129">في الحقل "طريقة الدفع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b8fb7-129">In the Method of payment field, type a value.</span></span>
4. <span data-ttu-id="b8fb7-130">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b8fb7-130">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b8fb7-131">يجب أن يكون الدفع الإلكتروني نوع الدفع لطريقة دفع تفويض الخصم المباشر.</span><span class="sxs-lookup"><span data-stu-id="b8fb7-131">The payment type for a direct debit mandate method of payment must be Electronic payment.</span></span>
6. <span data-ttu-id="b8fb7-132">حدد "نعم" في الحقل "مطلوب تفويض‬".</span><span class="sxs-lookup"><span data-stu-id="b8fb7-132">Select Yes in the Require mandate field.</span></span>
7. <span data-ttu-id="b8fb7-133">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b8fb7-133">Close the page.</span></span>

## <a name="add-a-direct-debit-mandate-to-a-customer"></a><span data-ttu-id="b8fb7-134">إضافة تفويض خصم مباشر إلى عميل</span><span class="sxs-lookup"><span data-stu-id="b8fb7-134">Add a direct debit mandate to a customer.</span></span>
1. <span data-ttu-id="b8fb7-135">انتقل إلى الحسابات المدينة > العملاء > كافة العملاء‬.</span><span class="sxs-lookup"><span data-stu-id="b8fb7-135">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="b8fb7-136">على سبيل المثال، حدد US-001</span><span class="sxs-lookup"><span data-stu-id="b8fb7-136">For example, select US-001</span></span>
3. <span data-ttu-id="b8fb7-137">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="b8fb7-137">Click Edit.</span></span>
4. <span data-ttu-id="b8fb7-138">وسّع المقطع "القيم الافتراضية للدفع‬".</span><span class="sxs-lookup"><span data-stu-id="b8fb7-138">Expand the Payment defaults section.</span></span>
5. <span data-ttu-id="b8fb7-139">في الحقل "أسلوب الدفع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="b8fb7-139">In the Method of payment field, enter or select a value.</span></span>
6. <span data-ttu-id="b8fb7-140">وسّع المقطع "القيم الافتراضية للدفع‬".</span><span class="sxs-lookup"><span data-stu-id="b8fb7-140">Expand the Payment defaults section.</span></span>
7. <span data-ttu-id="b8fb7-141">وسّع المقطع "تفويضات الخصم المباشر‬".</span><span class="sxs-lookup"><span data-stu-id="b8fb7-141">Expand the Direct debit mandates section.</span></span>
8. <span data-ttu-id="b8fb7-142">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="b8fb7-142">Click Add.</span></span>
9. <span data-ttu-id="b8fb7-143">في الحقل "الحساب البنكي‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="b8fb7-143">In the Bank account field, enter or select a value.</span></span>
10. <span data-ttu-id="b8fb7-144">في الحقل "‏‫الحساب البنكي للدائن‬‬‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="b8fb7-144">In the Creditor bank account field, enter or select a value.</span></span>
11. <span data-ttu-id="b8fb7-145">أدخل عدد الدفعات التي تتوقع معالجتها لهذا التفويض.</span><span class="sxs-lookup"><span data-stu-id="b8fb7-145">Enter the number of payments that you expect to process for this mandate.</span></span>
12. <span data-ttu-id="b8fb7-146">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="b8fb7-146">Click OK.</span></span>
13. <span data-ttu-id="b8fb7-147">انقر فوق طباعة.</span><span class="sxs-lookup"><span data-stu-id="b8fb7-147">Click Print.</span></span>
14. <span data-ttu-id="b8fb7-148">انقر فوق "تقرير التفويض".</span><span class="sxs-lookup"><span data-stu-id="b8fb7-148">Click Mandate report.</span></span>
15. <span data-ttu-id="b8fb7-149">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b8fb7-149">Close the page.</span></span>
16. <span data-ttu-id="b8fb7-150">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="b8fb7-150">Click Edit.</span></span>
17. <span data-ttu-id="b8fb7-151">في الحقل "تاريخ التوقيع"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="b8fb7-151">In the Signature date field, enter a date.</span></span>
18. <span data-ttu-id="b8fb7-152">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="b8fb7-152">Click Yes.</span></span>
19. <span data-ttu-id="b8fb7-153">أدخل موقع توقيع التفويض.</span><span class="sxs-lookup"><span data-stu-id="b8fb7-153">Enter the location where the mandate was signed.</span></span>
20. <span data-ttu-id="b8fb7-154">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="b8fb7-154">Click OK.</span></span>
21. <span data-ttu-id="b8fb7-155">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b8fb7-155">Close the page.</span></span>

## <a name="create-a-free-text-invoice-with-mandate"></a><span data-ttu-id="b8fb7-156">إنشاء فاتورة نص حر مع تفويض</span><span class="sxs-lookup"><span data-stu-id="b8fb7-156">Create a free text invoice with mandate</span></span>
1. <span data-ttu-id="b8fb7-157">انتقل إلى الحسابات المدينة > الفواتير > جميع الفواتير بنص حر‬.</span><span class="sxs-lookup"><span data-stu-id="b8fb7-157">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="b8fb7-158">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="b8fb7-158">Click New.</span></span>
3. <span data-ttu-id="b8fb7-159">حدد العميل الذي تريد إضافة التفويض إليه.</span><span class="sxs-lookup"><span data-stu-id="b8fb7-159">Select the customer that you added the mandate to.</span></span>
4. <span data-ttu-id="b8fb7-160">في الحقل "معرف الأمر الرسمي للخصم المباشر"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="b8fb7-160">In the Direct debit mandate ID field, enter or select a value.</span></span>


