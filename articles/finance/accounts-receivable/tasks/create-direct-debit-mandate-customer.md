---
title: إنشاء تفويض خصم مباشر لعميل
description: توضح هذه المهمة كيفية إنشاء تفويض خصم مباشر واستخدامه في الفاتورة.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f746da0bcf2b1e0cb09af6b5e2ea61938213c924
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991032"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a><span data-ttu-id="49c40-103">إنشاء تفويض خصم مباشر لعميل</span><span class="sxs-lookup"><span data-stu-id="49c40-103">Create a direct debit mandate for a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="49c40-104">توضح هذه المهمة كيفية إنشاء تفويض خصم مباشر واستخدامه في الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="49c40-104">This task guide demonstrates how to create a direct debit mandate and use it on an invoice.</span></span>


## <a name="create-a-bank-account"></a><span data-ttu-id="49c40-105">إنشاء حساب بنكي</span><span class="sxs-lookup"><span data-stu-id="49c40-105">Create a bank account</span></span>
1. <span data-ttu-id="49c40-106">في **جزء التنقل**، انتقل إلى **الوحدات النمطية > الحسابات المدينة > العملاء > كافة العملاء**.</span><span class="sxs-lookup"><span data-stu-id="49c40-106">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="49c40-107">في القائمة، حدد أحد السجلات.</span><span class="sxs-lookup"><span data-stu-id="49c40-107">In the list, select a record.</span></span> <span data-ttu-id="49c40-108">على سبيل المثال، حدد US-001</span><span class="sxs-lookup"><span data-stu-id="49c40-108">For example, select US-001</span></span>
3. <span data-ttu-id="49c40-109">في جزء الإجراءات، انقر فوق **العميل**.</span><span class="sxs-lookup"><span data-stu-id="49c40-109">On the Action Pane, click **Customer**.</span></span>
4. <span data-ttu-id="49c40-110">انقر فوق **الحسابات البنكية**.</span><span class="sxs-lookup"><span data-stu-id="49c40-110">Click **Bank accounts**.</span></span>
5. <span data-ttu-id="49c40-111">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="49c40-111">Click **New**.</span></span>
6. <span data-ttu-id="49c40-112">في الحقل **الحساب البنكي**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="49c40-112">In the **Bank account** field, type a value.</span></span>
7. <span data-ttu-id="49c40-113">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="49c40-113">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="49c40-114">في الحقل **IBAN‬**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="49c40-114">In the **IBAN** field, type a value.</span></span>
9. <span data-ttu-id="49c40-115">في الحقل **العملة**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="49c40-115">In the **Currency** field, type a value.</span></span>
10. <span data-ttu-id="49c40-116">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="49c40-116">Click **Save**.</span></span>
11. <span data-ttu-id="49c40-117">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="49c40-117">Close the page.</span></span>
12. <span data-ttu-id="49c40-118">في **جزء التنقل**، انتقل إلى **الوحدات النمطية > إدارة النقد والبنوك‬ > الحسابات البنكية > الحسابات البنكية**.</span><span class="sxs-lookup"><span data-stu-id="49c40-118">In the **Navigation pane**, go to **Modules > Cash and bank management > Bank accounts > Bank accounts**.</span></span>
13. <span data-ttu-id="49c40-119">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="49c40-119">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="49c40-120">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="49c40-120">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="49c40-121">انقر فوق **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="49c40-121">Click **Edit**.</span></span>
16. <span data-ttu-id="49c40-122">‏‫قم بتوسيع علامة التبويب السريعة **تعريف إضافي**.</span><span class="sxs-lookup"><span data-stu-id="49c40-122">Expand the **Additional identification** fastTab.</span></span>
17. <span data-ttu-id="49c40-123">في حقل ‏**معرف الدين المباشر**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="49c40-123">In the **Direct debit ID** field, type a value.</span></span>
18. <span data-ttu-id="49c40-124">في الحقل **IBAN‬**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="49c40-124">In the **IBAN** field, type a value.</span></span>
19. <span data-ttu-id="49c40-125">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="49c40-125">Close the page.</span></span>
20. <span data-ttu-id="49c40-126">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="49c40-126">Close the page.</span></span>

## <a name="define-the-electronic-payment-method"></a><span data-ttu-id="49c40-127">تحديد طريقة الدفع الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="49c40-127">Define the electronic payment method</span></span>
1. <span data-ttu-id="49c40-128">في **جزء التنقل**، انتقل إلى **الوحدات النمطية‬ > حسابات مدينة‬ > إعداد المدفوعات‬ > طرق الدفع**‬.</span><span class="sxs-lookup"><span data-stu-id="49c40-128">In the **Navigation pane**, go to **Modules > Accounts receivable > Payments setup > Methods of payment**.</span></span>
2. <span data-ttu-id="49c40-129">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="49c40-129">Click **New**.</span></span>
3. <span data-ttu-id="49c40-130">في الحقل **طريقة الدفع**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="49c40-130">In the **Method of payment** field, type a value.</span></span>
4. <span data-ttu-id="49c40-131">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="49c40-131">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="49c40-132">في الحقل **نوع الدفع**، حدد "دفع إلكتروني".</span><span class="sxs-lookup"><span data-stu-id="49c40-132">In the **Payment type** field, enter 'Electronic payment'.</span></span> <span data-ttu-id="49c40-133">يجب أن يكون الدفع الإلكتروني نوع الدفع لطريقة دفع تفويض الخصم المباشر.</span><span class="sxs-lookup"><span data-stu-id="49c40-133">The payment type for a direct debit mandate method of payment must be Electronic payment.</span></span>
6. <span data-ttu-id="49c40-134">حدد "نعم" في الحقل **مطلوب تفويض‬**.</span><span class="sxs-lookup"><span data-stu-id="49c40-134">Select Yes in the **Require mandate** field.</span></span>
7. <span data-ttu-id="49c40-135">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="49c40-135">Close the page.</span></span>

## <a name="add-a-direct-debit-mandate-to-a-customer"></a><span data-ttu-id="49c40-136">إضافة تفويض خصم مباشر إلى عميل</span><span class="sxs-lookup"><span data-stu-id="49c40-136">Add a direct debit mandate to a customer.</span></span>
1. <span data-ttu-id="49c40-137">في **جزء التنقل**، انتقل إلى **الوحدات النمطية > الحسابات المدينة > العملاء > كافة العملاء**.</span><span class="sxs-lookup"><span data-stu-id="49c40-137">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="49c40-138">في القائمة، حدد أحد السجلات.</span><span class="sxs-lookup"><span data-stu-id="49c40-138">In the list, select a record.</span></span> <span data-ttu-id="49c40-139">على سبيل المثال، حدد US-001</span><span class="sxs-lookup"><span data-stu-id="49c40-139">For example, select US-001</span></span>
3. <span data-ttu-id="49c40-140">انقر فوق **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="49c40-140">Click **Edit**.</span></span>
4. <span data-ttu-id="49c40-141">وسّع علامة التبويب السريعة **القيم الافتراضية للدفع‬**.</span><span class="sxs-lookup"><span data-stu-id="49c40-141">Expand the **Payment defaults** fastTab.</span></span>
5. <span data-ttu-id="49c40-142">في الحقل **أسلوب الدفع**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="49c40-142">In the **Method of payment** field, enter or select a value.</span></span>
6. <span data-ttu-id="49c40-143">وسّع علامة التبويب السريعة **القيم الافتراضية للدفع‬**.</span><span class="sxs-lookup"><span data-stu-id="49c40-143">Expand the **Payment defaults** fastTab.</span></span>
7. <span data-ttu-id="49c40-144">وسّع علامة التبويب السريعة **تفويضات الخصم المباشر**.</span><span class="sxs-lookup"><span data-stu-id="49c40-144">Expand the **Direct debit mandates** fastTab.</span></span>
8. <span data-ttu-id="49c40-145">انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="49c40-145">Click **Add**.</span></span>
9. <span data-ttu-id="49c40-146">في الحقل **الحساب البنكي**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="49c40-146">In the **Bank account** field, enter or select a value.</span></span>
10. <span data-ttu-id="49c40-147">أدخل قيمة أو حددها في حقل **الحساب البنكي للدائن**.</span><span class="sxs-lookup"><span data-stu-id="49c40-147">In the **Creditor bank account** field, enter or select a value.</span></span>
11. <span data-ttu-id="49c40-148">أدخل عدد الدفعات التي تتوقع معالجتها لهذا التفويض في حقل **تكرار الدفع‬**.</span><span class="sxs-lookup"><span data-stu-id="49c40-148">In the **Payment frequency** field, enter the number of payments that you expect to process for this mandate.</span></span>
12. <span data-ttu-id="49c40-149">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="49c40-149">Click **OK**.</span></span>
13. <span data-ttu-id="49c40-150">انقر فوق **طباعة**.</span><span class="sxs-lookup"><span data-stu-id="49c40-150">Click **Print**.</span></span>
14. <span data-ttu-id="49c40-151">انقر فوق **تقرير التفويض**.</span><span class="sxs-lookup"><span data-stu-id="49c40-151">Click **Mandate report**.</span></span>
15. <span data-ttu-id="49c40-152">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="49c40-152">Close the page.</span></span>
16. <span data-ttu-id="49c40-153">انقر فوق **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="49c40-153">Click **Edit**.</span></span>
17. <span data-ttu-id="49c40-154">في الحقل **تاريخ التوقيع**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="49c40-154">In the **Signature date** field, enter a date.</span></span>
18. <span data-ttu-id="49c40-155">انقر فوق **نعم**.</span><span class="sxs-lookup"><span data-stu-id="49c40-155">Click **Yes**.</span></span>
19. <span data-ttu-id="49c40-156">أدخل موقع توقيع التفويض.</span><span class="sxs-lookup"><span data-stu-id="49c40-156">Enter the location where the mandate was signed.</span></span>
20. <span data-ttu-id="49c40-157">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="49c40-157">Click **OK**.</span></span>
21. <span data-ttu-id="49c40-158">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="49c40-158">Close the page.</span></span>

## <a name="create-a-free-text-invoice-with-mandate"></a><span data-ttu-id="49c40-159">إنشاء فاتورة نص حر مع تفويض</span><span class="sxs-lookup"><span data-stu-id="49c40-159">Create a free text invoice with mandate</span></span>
1. <span data-ttu-id="49c40-160">في **جزء التنقل**، انتقل إلى **الوحدات النمطية > الحسابات المدينة > الفواتير > جميع فواتير النص الحر**.</span><span class="sxs-lookup"><span data-stu-id="49c40-160">In the **Navigation pane**, go to **Modules > Accounts receivable > Invoices > All free text invoices**.</span></span>
2. <span data-ttu-id="49c40-161">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="49c40-161">Click **New**.</span></span>
3. <span data-ttu-id="49c40-162">حدد العميل الذي تريد إضافة التفويض إليه.</span><span class="sxs-lookup"><span data-stu-id="49c40-162">Select the customer that you added the mandate to.</span></span>
4. <span data-ttu-id="49c40-163">في الحقل **معرف الأمر الرسمي للخصم المباشر**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="49c40-163">In the **Direct debit mandate ID** field, enter or select a value.</span></span>

