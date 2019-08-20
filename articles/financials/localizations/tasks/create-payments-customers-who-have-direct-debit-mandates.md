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
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1959904befc62c32a8da185729f13525db27d4b
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848912"
---
# <a name="create-payments-for-a-customer-who-have-direct-debit-mandates"></a><span data-ttu-id="17957-103">إنشاء مدفوعات لعميل لديه ‏‫تفويضات الخصم المباشر‬</span><span class="sxs-lookup"><span data-stu-id="17957-103">Create payments for a customer who have direct debit mandates</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="17957-104">يوضح هذا الإجراء كيفية إنشاء ملف دفع دين مباشر ISO20022 لعميل تم تكوين دين مباشر له ولديه فاتورة للدفع.</span><span class="sxs-lookup"><span data-stu-id="17957-104">This procedure shows how to generate an ISO20022 direct debit payment file for a customer who has direct debit configured and an invoice to be paid.</span></span> <span data-ttu-id="17957-105">يُعد إنشاء الفاتورة وترحيلها عملية اختيارية.</span><span class="sxs-lookup"><span data-stu-id="17957-105">Creating and posting an invoice is optional.</span></span> <span data-ttu-id="17957-106">بدلاً من وجود فاتورة يجب دفعها، يمكنك تحديد تفويض في دفتر اليومية قبل إنشاء ملف الدفع، لدعم سيناريو الدفع المقدم من قِبل العميل.</span><span class="sxs-lookup"><span data-stu-id="17957-106">Instead of having an invoice to be paid you can select a mandate in a journal prior to generating a payment file, to support a customer prepayment scenario.</span></span>



<span data-ttu-id="17957-107">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي DEMF.</span><span class="sxs-lookup"><span data-stu-id="17957-107">The demo data company used to create this procedure is DEMF.</span></span>



<span data-ttu-id="17957-108">هذا هو الإجراء الخامس من ضمن خمسة إجراءات هدفها توضيح عملية معالجة مدفوعات العميل باستخدام تكوينات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="17957-108">This is the fifth of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span> <span data-ttu-id="17957-109">قبل إتمام هذه المهمة، يجب إتمام المهام السابقة.</span><span class="sxs-lookup"><span data-stu-id="17957-109">Before you can complete this task, you must complete the earlier tasks.</span></span> <span data-ttu-id="17957-110">يجب عليك أولاً استيراد تكوينات التقارير الإلكترونية لدفع العميل، وتكوين طرق الدفع، وإعداد معلومات شركتك والعميل.</span><span class="sxs-lookup"><span data-stu-id="17957-110">You must first import customer payment electronic reporting configurations, configure method of payments, and set up your company and customer information.</span></span> 


## <a name="post-a-free-text-invoice-with-direct-debit-information"></a><span data-ttu-id="17957-111">ترحيل فاتورة نص حر بمعلومات الخصم المباشر</span><span class="sxs-lookup"><span data-stu-id="17957-111">Post a free text invoice with direct debit information</span></span>
1. <span data-ttu-id="17957-112">انتقل إلى الحسابات المدينة > الفواتير > جميع الفواتير ذات نص حر‬.</span><span class="sxs-lookup"><span data-stu-id="17957-112">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="17957-113">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="17957-113">Click New.</span></span>
3. <span data-ttu-id="17957-114">في الحقل "حساب العميل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="17957-114">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="17957-115">على سبيل المثال، حدد DE-010</span><span class="sxs-lookup"><span data-stu-id="17957-115">For example, select DE-010.</span></span>  
4. <span data-ttu-id="17957-116">في الحقل "أسلوب الدفع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="17957-116">In the Method of payment field, enter or select a value.</span></span>
    * <span data-ttu-id="17957-117">على سبيل المثال،</span><span class="sxs-lookup"><span data-stu-id="17957-117">For example.</span></span> <span data-ttu-id="17957-118">حدد "إلكتروني".</span><span class="sxs-lookup"><span data-stu-id="17957-118">select Electronic.</span></span>  
5. <span data-ttu-id="17957-119">في الحقل "معرف الأمر الرسمي للخصم المباشر"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="17957-119">In the Direct debit mandate ID field, enter or select a value.</span></span>
6. <span data-ttu-id="17957-120">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="17957-120">Click Add line.</span></span>
7. <span data-ttu-id="17957-121">في حقل "الوصف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="17957-121">In the Description field, type a value.</span></span>
8. <span data-ttu-id="17957-122">في حقل "الحساب الرئيسي"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="17957-122">In the Main account field, specify the desired values.</span></span>
9. <span data-ttu-id="17957-123">في حقل "سعر الوحدة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="17957-123">In the Unit price field, enter a number.</span></span>
10. <span data-ttu-id="17957-124">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="17957-124">Click Post.</span></span>
11. <span data-ttu-id="17957-125">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="17957-125">Click OK.</span></span>

## <a name="create-a-payment"></a><span data-ttu-id="17957-126">إنشاء دفع</span><span class="sxs-lookup"><span data-stu-id="17957-126">Create a payment</span></span>
1. <span data-ttu-id="17957-127">انتقل إلى الحسابات المدينة > المدفوعات‬ > دفتر يومية المدفوعات‬‬.</span><span class="sxs-lookup"><span data-stu-id="17957-127">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="17957-128">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="17957-128">Click New.</span></span>
3. <span data-ttu-id="17957-129">في الحقل "الاسم"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="17957-129">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="17957-130">انقر فوق البنود.</span><span class="sxs-lookup"><span data-stu-id="17957-130">Click Lines.</span></span>
5. <span data-ttu-id="17957-131">انقر فوق "مقترح الدفع".</span><span class="sxs-lookup"><span data-stu-id="17957-131">Click Payment proposal.</span></span>
6. <span data-ttu-id="17957-132">انقر فوق "إنشاء مقترح دفع".</span><span class="sxs-lookup"><span data-stu-id="17957-132">Click Create payment proposal.</span></span>
7. <span data-ttu-id="17957-133">وسّع المقطع "السجلات المطلوب تضمينها‬".</span><span class="sxs-lookup"><span data-stu-id="17957-133">Expand the Records to include section.</span></span>
8. <span data-ttu-id="17957-134">انقر فوق "عامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="17957-134">Click Filter.</span></span>
9. <span data-ttu-id="17957-135">في القائمة، حدد صف الجدول "حركات العميل" وحقل "طريقة الدفع".</span><span class="sxs-lookup"><span data-stu-id="17957-135">In the list, select the row for the Customer transactions table and the Method of payment field.</span></span>
    * <span data-ttu-id="17957-136">يمكنك تطبيق أية معايير لتحديد حركات العميل للدفع.</span><span class="sxs-lookup"><span data-stu-id="17957-136">You can apply any criteria for selecting customer transactions to pay.</span></span> <span data-ttu-id="17957-137">لهذا المثال، استخدم "إلكتروني" كطريقة دفع لتصفية الحركات.</span><span class="sxs-lookup"><span data-stu-id="17957-137">For this example, use Electronic as a method of payment to filter transactions.</span></span>  
10. <span data-ttu-id="17957-138">في الحقل "المعايير‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="17957-138">In the Criteria field, enter or select a value.</span></span>
11. <span data-ttu-id="17957-139">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="17957-139">Click OK.</span></span>
12. <span data-ttu-id="17957-140">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="17957-140">Click OK.</span></span>
13. <span data-ttu-id="17957-141">انقر فوق "إنشاء مدفوعات".</span><span class="sxs-lookup"><span data-stu-id="17957-141">Click Create payments.</span></span>

## <a name="generate-a-payment-file"></a><span data-ttu-id="17957-142">إنشاء ملف دفع</span><span class="sxs-lookup"><span data-stu-id="17957-142">Generate a payment file</span></span>

