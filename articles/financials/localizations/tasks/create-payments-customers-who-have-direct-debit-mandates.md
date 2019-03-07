---
title: إنشاء مدفوعات لعميل لديه ‏‫تفويضات الخصم المباشر‬
description: يوضح هذا الإجراء كيفية إنشاء ملف دفع دين مباشر ISO20022 لعميل تم تكوين دين مباشر له ولديه فاتورة للدفع.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice, CustTableLookup, CustPostInvoiceJob, LedgerJournalTable, LedgerJournalTransCustPaym, SysQueryForm, CustPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6781ac38fff6344bfc9546c3ffd2253fb3ef712c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "342122"
---
# <a name="create-payments-for-a-customer-who-have-direct-debit-mandates"></a><span data-ttu-id="81f62-103">إنشاء مدفوعات لعميل لديه ‏‫تفويضات الخصم المباشر‬</span><span class="sxs-lookup"><span data-stu-id="81f62-103">Create payments for a customer who have direct debit mandates</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="81f62-104">يوضح هذا الإجراء كيفية إنشاء ملف دفع دين مباشر ISO20022 لعميل تم تكوين دين مباشر له ولديه فاتورة للدفع.</span><span class="sxs-lookup"><span data-stu-id="81f62-104">This procedure shows how to generate an ISO20022 direct debit payment file for a customer who has direct debit configured and an invoice to be paid.</span></span> <span data-ttu-id="81f62-105">يُعد إنشاء الفاتورة وترحيلها عملية اختيارية.</span><span class="sxs-lookup"><span data-stu-id="81f62-105">Creating and posting an invoice is optional.</span></span> <span data-ttu-id="81f62-106">بدلاً من وجود فاتورة يجب دفعها، يمكنك تحديد تفويض في دفتر اليومية قبل إنشاء ملف الدفع، لدعم سيناريو الدفع المقدم من قِبل العميل.</span><span class="sxs-lookup"><span data-stu-id="81f62-106">Instead of having an invoice to be paid you can select a mandate in a journal prior to generating a payment file, to support a customer prepayment scenario.</span></span>



<span data-ttu-id="81f62-107">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي DEMF.</span><span class="sxs-lookup"><span data-stu-id="81f62-107">The demo data company used to create this procedure is DEMF.</span></span>



<span data-ttu-id="81f62-108">هذا هو الإجراء الخامس من ضمن خمسة إجراءات هدفها توضيح عملية معالجة مدفوعات العميل باستخدام تكوينات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="81f62-108">This is the fifth of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span> <span data-ttu-id="81f62-109">قبل إتمام هذه المهمة، يجب إتمام المهام السابقة.</span><span class="sxs-lookup"><span data-stu-id="81f62-109">Before you can complete this task, you must complete the earlier tasks.</span></span> <span data-ttu-id="81f62-110">يجب عليك أولاً استيراد تكوينات التقارير الإلكترونية لدفع العميل، وتكوين طرق الدفع، وإعداد معلومات شركتك والعميل.</span><span class="sxs-lookup"><span data-stu-id="81f62-110">You must first import customer payment electronic reporting configurations, configure method of payments, and set up your company and customer information.</span></span> 


## <a name="post-a-free-text-invoice-with-direct-debit-information"></a><span data-ttu-id="81f62-111">ترحيل فاتورة نص حر بمعلومات الخصم المباشر</span><span class="sxs-lookup"><span data-stu-id="81f62-111">Post a free text invoice with direct debit information</span></span>
1. <span data-ttu-id="81f62-112">انتقل إلى الحسابات المدينة > الفواتير > جميع الفواتير بنص حر‬.</span><span class="sxs-lookup"><span data-stu-id="81f62-112">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="81f62-113">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="81f62-113">Click New.</span></span>
3. <span data-ttu-id="81f62-114">في الحقل "حساب العميل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="81f62-114">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="81f62-115">على سبيل المثال، حدد DE-010</span><span class="sxs-lookup"><span data-stu-id="81f62-115">For example, select DE-010.</span></span>  
4. <span data-ttu-id="81f62-116">في الحقل "أسلوب الدفع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="81f62-116">In the Method of payment field, enter or select a value.</span></span>
    * <span data-ttu-id="81f62-117">على سبيل المثال،</span><span class="sxs-lookup"><span data-stu-id="81f62-117">For example.</span></span> <span data-ttu-id="81f62-118">حدد "إلكتروني".</span><span class="sxs-lookup"><span data-stu-id="81f62-118">select Electronic.</span></span>  
5. <span data-ttu-id="81f62-119">في الحقل "معرف الأمر الرسمي للخصم المباشر"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="81f62-119">In the Direct debit mandate ID field, enter or select a value.</span></span>
6. <span data-ttu-id="81f62-120">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="81f62-120">Click Add line.</span></span>
7. <span data-ttu-id="81f62-121">في حقل "الوصف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="81f62-121">In the Description field, type a value.</span></span>
8. <span data-ttu-id="81f62-122">في حقل "الحساب الرئيسي"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="81f62-122">In the Main account field, specify the desired values.</span></span>
9. <span data-ttu-id="81f62-123">في حقل "سعر الوحدة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="81f62-123">In the Unit price field, enter a number.</span></span>
10. <span data-ttu-id="81f62-124">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="81f62-124">Click Post.</span></span>
11. <span data-ttu-id="81f62-125">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="81f62-125">Click OK.</span></span>

## <a name="create-a-payment"></a><span data-ttu-id="81f62-126">إنشاء دفع</span><span class="sxs-lookup"><span data-stu-id="81f62-126">Create a payment</span></span>
1. <span data-ttu-id="81f62-127">انتقل إلى الحسابات المدينة > المدفوعات‬ > دفتر يومية المدفوعات‬‬.</span><span class="sxs-lookup"><span data-stu-id="81f62-127">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="81f62-128">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="81f62-128">Click New.</span></span>
3. <span data-ttu-id="81f62-129">في الحقل "الاسم"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="81f62-129">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="81f62-130">انقر فوق البنود.</span><span class="sxs-lookup"><span data-stu-id="81f62-130">Click Lines.</span></span>
5. <span data-ttu-id="81f62-131">انقر فوق "مقترح الدفع".</span><span class="sxs-lookup"><span data-stu-id="81f62-131">Click Payment proposal.</span></span>
6. <span data-ttu-id="81f62-132">انقر فوق "إنشاء مقترح دفع".</span><span class="sxs-lookup"><span data-stu-id="81f62-132">Click Create payment proposal.</span></span>
7. <span data-ttu-id="81f62-133">وسّع المقطع "السجلات المطلوب تضمينها‬".</span><span class="sxs-lookup"><span data-stu-id="81f62-133">Expand the Records to include section.</span></span>
8. <span data-ttu-id="81f62-134">انقر فوق "عامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="81f62-134">Click Filter.</span></span>
9. <span data-ttu-id="81f62-135">في القائمة، حدد صف الجدول "حركات العميل" وحقل "طريقة الدفع".</span><span class="sxs-lookup"><span data-stu-id="81f62-135">In the list, select the row for the Customer transactions table and the Method of payment field.</span></span>
    * <span data-ttu-id="81f62-136">يمكنك تطبيق أية معايير لتحديد حركات العميل للدفع.</span><span class="sxs-lookup"><span data-stu-id="81f62-136">You can apply any criteria for selecting customer transactions to pay.</span></span> <span data-ttu-id="81f62-137">لهذا المثال، استخدم "إلكتروني" كطريقة دفع لتصفية الحركات.</span><span class="sxs-lookup"><span data-stu-id="81f62-137">For this example, use Electronic as a method of payment to filter transactions.</span></span>  
10. <span data-ttu-id="81f62-138">في الحقل "المعايير‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="81f62-138">In the Criteria field, enter or select a value.</span></span>
11. <span data-ttu-id="81f62-139">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="81f62-139">Click OK.</span></span>
12. <span data-ttu-id="81f62-140">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="81f62-140">Click OK.</span></span>
13. <span data-ttu-id="81f62-141">انقر فوق "إنشاء مدفوعات".</span><span class="sxs-lookup"><span data-stu-id="81f62-141">Click Create payments.</span></span>

## <a name="generate-a-payment-file"></a><span data-ttu-id="81f62-142">إنشاء ملف دفع</span><span class="sxs-lookup"><span data-stu-id="81f62-142">Generate a payment file</span></span>

