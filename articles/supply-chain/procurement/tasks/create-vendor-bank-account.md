---
title: إنشاء حساب بنكي للمورّد
description: يوضح هذا الإجراء كيفية إنشاء حساب بنكي للمورّد.
author: kamaybac
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, LogisticsPostalAddressSingle
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4fcf15d798d2ca8e1d36556fbe2c9603f12d2b03
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812004"
---
# <a name="create-a-vendor-bank-account"></a><span data-ttu-id="d3f36-103">إنشاء حساب بنكي للمورّد</span><span class="sxs-lookup"><span data-stu-id="d3f36-103">Create a vendor bank account</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d3f36-104">يوضح هذا الإجراء كيفية إنشاء حساب بنكي للمورّد.</span><span class="sxs-lookup"><span data-stu-id="d3f36-104">This procedure shows you how to create a bank account for a vendor.</span></span> <span data-ttu-id="d3f36-105">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="d3f36-105">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="d3f36-106">انتقل إلى **جزء التنقل > الوحدات النمطية > التدبير والتوريد > المورّدون‬ > كافة المورّدين‬**.</span><span class="sxs-lookup"><span data-stu-id="d3f36-106">Go to **Navigation pane > Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="d3f36-107">حدد المورّد الذي تريد إنشاء حساب بنكي له، ثم انقر فوق الارتباط على الحقل **معرف حساب المورّد**.</span><span class="sxs-lookup"><span data-stu-id="d3f36-107">Select the vendor that you want to create a bank account for, and then click the link on the **Vendor account ID** field.</span></span>
3. <span data-ttu-id="d3f36-108">في **جزء الإجراءات**، انقر فوق **المورّد**.</span><span class="sxs-lookup"><span data-stu-id="d3f36-108">On the **Action Pane**, click **Vendor**.</span></span>
4. <span data-ttu-id="d3f36-109">انقر فوق **الحسابات البنكية**.</span><span class="sxs-lookup"><span data-stu-id="d3f36-109">Click **Bank accounts**.</span></span>
5. <span data-ttu-id="d3f36-110">انقر فوق **جديد** في **جزء الإجراءات**.</span><span class="sxs-lookup"><span data-stu-id="d3f36-110">On the **Action Pane**, click **New**.</span></span>
6. <span data-ttu-id="d3f36-111">في الحقل **الحساب البنكي**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d3f36-111">In the **Bank account** field, type a value.</span></span> <span data-ttu-id="d3f36-112">سيتم استخدام هذا المعرف لتعريف الحساب البنكي في سجل المورّد.</span><span class="sxs-lookup"><span data-stu-id="d3f36-112">This ID will be used to identify the bank account on the vendor record.</span></span>  
7. <span data-ttu-id="d3f36-113">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d3f36-113">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="d3f36-114">في الحقل **مجموعات بنكية‬**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="d3f36-114">In the **Bank groups** field, enter or select a value.</span></span>
9. <span data-ttu-id="d3f36-115">في الحقل **نوع رقم التوجيه**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="d3f36-115">In the **Routing number type** field, select an option.</span></span> <span data-ttu-id="d3f36-116">هذا هو نوع رقم التوجيه المستخدم للمدفوعات الدولية.</span><span class="sxs-lookup"><span data-stu-id="d3f36-116">This is the type of routing number that's used for international payments.</span></span>  
10. <span data-ttu-id="d3f36-117">في الحقل **رقم الحساب البنكي**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d3f36-117">In the **Bank account number** field, type a value.</span></span>
11. <span data-ttu-id="d3f36-118">في الحقل **كود التحويل الإلكتروني‬**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d3f36-118">In the **SWIFT code** field, type a value.</span></span>
12. <span data-ttu-id="d3f36-119">في الحقل **IBAN‬**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d3f36-119">In the **IBAN** field, type a value.</span></span>
    - <span data-ttu-id="d3f36-120">يجب أن يكون رقم IBAN بالتنسيق الصحيح.</span><span class="sxs-lookup"><span data-stu-id="d3f36-120">The IBAN number must be in the correct format.</span></span> <span data-ttu-id="d3f36-121">على سبيل المثال، يمكنك استخدام DE89370400440532013000.</span><span class="sxs-lookup"><span data-stu-id="d3f36-121">For example, you could use DE89370400440532013000.</span></span>  
    - <span data-ttu-id="d3f36-122">تكون حالة الحساب البنكي "نشط" إذا تم بلوغ تاريخ السريان، ولم يتم تجاوز تاريخ انتهاء الصلاحية.</span><span class="sxs-lookup"><span data-stu-id="d3f36-122">The status of the bank account is Active if the Active date has been reached, and the Expiration date has not been exceeded.</span></span> <span data-ttu-id="d3f36-123">كما يكون الحساب البنكي نشطًا عندما يكون حقل تاريخ السريان وحقل تاريخ انتهاء الصلاحية فارغين.</span><span class="sxs-lookup"><span data-stu-id="d3f36-123">It's also active if both the Active date and Expiration date fields are blank.</span></span> <span data-ttu-id="d3f36-124">إذا كانت التواريخ في حقلي تاريخ السريان وتاريخ انتهاء الصلاحية تواريخ مستقبلية، فلن تكون الدفعات الإلكترونية متوفرة.</span><span class="sxs-lookup"><span data-stu-id="d3f36-124">If the dates in both the Active date and Expiration date fields are in the future electronic payments are not available.</span></span> <span data-ttu-id="d3f36-125">تتوفر أنواع دفعات أخرى ويكون الحساب البنكي نشطًا.</span><span class="sxs-lookup"><span data-stu-id="d3f36-125">Other payment types are available and the bank account is active.</span></span>  
13. <span data-ttu-id="d3f36-126">قم بتوسيع قسم **الإعداد**.</span><span class="sxs-lookup"><span data-stu-id="d3f36-126">Expand the **Setup** section.</span></span>
14. <span data-ttu-id="d3f36-127">في الحقل **كود النص**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d3f36-127">In the **Text code** field, type a value.</span></span> <span data-ttu-id="d3f36-128">يحدد هذا الحقل الكود الذي سيظهر في كشف الحساب البنكي الخاص بالمستلم.</span><span class="sxs-lookup"><span data-stu-id="d3f36-128">This field specifies a code that will appear on the bank statement of the recipient.</span></span>  
15. <span data-ttu-id="d3f36-129">في الحقل **رسالة إلى البنك**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d3f36-129">In the **Message to bank** field, type a value.</span></span>
16. <span data-ttu-id="d3f36-130">في الحقل **مرجع سعر الصرف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d3f36-130">In the **Exchange reference** field, type a value.</span></span> <span data-ttu-id="d3f36-131">هذا هو الرقم المرجعي لأي سعر صرف ذي استحقاق آجل أو ثابت.</span><span class="sxs-lookup"><span data-stu-id="d3f36-131">This is the reference number for any forward-term or fixed-term rate of exchange.</span></span>
17. <span data-ttu-id="d3f36-132">في الحقل **العملة**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="d3f36-132">In the **Currency** field, enter or select a value.</span></span> <span data-ttu-id="d3f36-133">عندما يتم إصدار إشعارات مسبقة، يوفر هذا المقطع نظرة عامة حول حالتها (معلقة أو تمت الموافقة عليها).</span><span class="sxs-lookup"><span data-stu-id="d3f36-133">When prenotes are issued, this section provides an overview of their status (pending or approved).</span></span>  
18. <span data-ttu-id="d3f36-134">وسّع قسم **العنوان**.</span><span class="sxs-lookup"><span data-stu-id="d3f36-134">Expand the **Address** section.</span></span>
19. <span data-ttu-id="d3f36-135">وسّع قسم **الإشعارات المسبقة‬**.</span><span class="sxs-lookup"><span data-stu-id="d3f36-135">Expand the **Prenotes** section.</span></span>
20. <span data-ttu-id="d3f36-136">وسّع قسم **معلومات الاتصال**.</span><span class="sxs-lookup"><span data-stu-id="d3f36-136">Expand the **Contact information** section.</span></span>
21. <span data-ttu-id="d3f36-137">اكتب قيمة في حقل **الهاتف**.</span><span class="sxs-lookup"><span data-stu-id="d3f36-137">In the **Telephone** field, type a value.</span></span>
22. <span data-ttu-id="d3f36-138">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d3f36-138">Close the page.</span></span>
23. <span data-ttu-id="d3f36-139">انقر فوق **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="d3f36-139">Click **Edit**.</span></span>
24. <span data-ttu-id="d3f36-140">وسّع قسم **الدفع**.</span><span class="sxs-lookup"><span data-stu-id="d3f36-140">Expand the **Payment** section.</span></span>
25. <span data-ttu-id="d3f36-141">في حقل **الحساب البنكي**، حدد الحساب الذي أنشأته للتوّ.</span><span class="sxs-lookup"><span data-stu-id="d3f36-141">In the **Bank account** field, select the account that you've just created.</span></span>
26. <span data-ttu-id="d3f36-142">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="d3f36-142">Click **Save**.</span></span> <span data-ttu-id="d3f36-143">قد يتم توارث العنوان من المجموعة البنكية، إذا تم تحديد واحد، أو يمكنك إضافته هنا.</span><span class="sxs-lookup"><span data-stu-id="d3f36-143">The address may be inherited from the bank group, if one is specified, or you can add it here.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]