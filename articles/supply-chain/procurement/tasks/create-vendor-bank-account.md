--- 
title: "إنشاء حساب بنكي للمورّد"
description: "يوضح هذا الإجراء كيفية إنشاء حساب بنكي للمورّد."
author: mkirknel
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 636bbafc87835f1cfe5de0301e3f020a8ac01a56
ms.contentlocale: ar-sa
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-vendor-bank-account"></a><span data-ttu-id="70f33-103">إنشاء حساب بنكي للمورّد</span><span class="sxs-lookup"><span data-stu-id="70f33-103">Create a vendor bank account</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="70f33-104">يوضح هذا الإجراء كيفية إنشاء حساب بنكي للمورّد.</span><span class="sxs-lookup"><span data-stu-id="70f33-104">This procedure shows you how to create a bank account for a vendor.</span></span> <span data-ttu-id="70f33-105">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="70f33-105">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="70f33-106">انتقل إلى ‏‫التدبير والتوريد > الموردون > جميع الموردين.</span><span class="sxs-lookup"><span data-stu-id="70f33-106">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="70f33-107">حدد المورّد الذي تريد إنشاء حساب بنكي له، ثم انقر فوق الارتباط على معرف حساب المورّد.</span><span class="sxs-lookup"><span data-stu-id="70f33-107">Select the vendor that you want to create a bank account for, and then click the link on the Vendor account ID.</span></span>
3. <span data-ttu-id="70f33-108">في جزء الإجراءات، انقر فوق "المورّد".</span><span class="sxs-lookup"><span data-stu-id="70f33-108">On the Action Pane, click Vendor.</span></span>
4. <span data-ttu-id="70f33-109">انتقل إلى "الحسابات البنكية".</span><span class="sxs-lookup"><span data-stu-id="70f33-109">Click Bank accounts.</span></span>
5. <span data-ttu-id="70f33-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="70f33-110">Click New.</span></span>
6. <span data-ttu-id="70f33-111">في الحقل "الحساب البنكي"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="70f33-111">In the Bank account field, type a value.</span></span>
    * <span data-ttu-id="70f33-112">سيتم استخدام هذا المعرف لتعريف الحساب البنكي في سجل المورّد.</span><span class="sxs-lookup"><span data-stu-id="70f33-112">This ID will be used to identify the bank account on the vendor record.</span></span>  
7. <span data-ttu-id="70f33-113">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="70f33-113">In the Name field, type a value.</span></span>
8. <span data-ttu-id="70f33-114">في الحقل "مجموعات بنكية‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="70f33-114">In the Bank groups field, enter or select a value.</span></span>
9. <span data-ttu-id="70f33-115">في الحقل "نوع رقم التوجيه"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="70f33-115">In the Routing number type field, select an option.</span></span>
    * <span data-ttu-id="70f33-116">هذا هو نوع رقم التوجيه المستخدم للمدفوعات الدولية.</span><span class="sxs-lookup"><span data-stu-id="70f33-116">This is the type of routing number that’s used for international payments.</span></span>  
10. <span data-ttu-id="70f33-117">في الحقل "رقم الحساب البنكي"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="70f33-117">In the Bank account number field, type a value.</span></span>
11. <span data-ttu-id="70f33-118">في الحقل "كود التحويل الإلكتروني‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="70f33-118">In the SWIFT code field, type a value.</span></span>
12. <span data-ttu-id="70f33-119">في الحقل "IBAN‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="70f33-119">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="70f33-120">يجب أن يكون رقم IBAN بالتنسيق الصحيح.</span><span class="sxs-lookup"><span data-stu-id="70f33-120">The IBAN number must be in the correct format.</span></span> <span data-ttu-id="70f33-121">على سبيل المثال، يمكنك استخدام DE89370400440532013000.</span><span class="sxs-lookup"><span data-stu-id="70f33-121">For example, you could use DE89370400440532013000.</span></span>  
    * <span data-ttu-id="70f33-122">تكون حالة الحساب البنكي "نشط" إذا تم بلوغ تاريخ السريان، ولم يتم تجاوز تاريخ انتهاء الصلاحية.</span><span class="sxs-lookup"><span data-stu-id="70f33-122">The status of the bank account is Active if the Active date has been reached, and the Expiration date has not been exceeded.</span></span> <span data-ttu-id="70f33-123">كما يكون الحساب البنكي نشطًا عندما يكون حقل تاريخ السريان وحقل تاريخ انتهاء الصلاحية فارغين.</span><span class="sxs-lookup"><span data-stu-id="70f33-123">It’s also active if both the Active date and Expiration date fields are blank.</span></span> <span data-ttu-id="70f33-124">إذا كانت التواريخ في حقلي تاريخ السريان وتاريخ انتهاء الصلاحية تواريخ مستقبلية، فلن تكون الدفعات الإلكترونية متوفرة.</span><span class="sxs-lookup"><span data-stu-id="70f33-124">If the dates in both the Active date and Expiration date fields are in the future electronic payments are not available.</span></span> <span data-ttu-id="70f33-125">تتوفر أنواع دفعات أخرى ويكون الحساب البنكي نشطًا.</span><span class="sxs-lookup"><span data-stu-id="70f33-125">Other payment types are available and the bank account is active.</span></span>  
13. <span data-ttu-id="70f33-126">قم بتوسيع قسم "الإعداد".</span><span class="sxs-lookup"><span data-stu-id="70f33-126">Expand the Setup section.</span></span>
14. <span data-ttu-id="70f33-127">في الحقل "كود النص‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="70f33-127">In the Text code field, type a value.</span></span>
    * <span data-ttu-id="70f33-128">يحدد هذا الحقل الكود الذي سيظهر في كشف الحساب البنكي الخاص بالمستلم.</span><span class="sxs-lookup"><span data-stu-id="70f33-128">This field specifies a code that will appear on the bank statement of the recipient.</span></span>  
15. <span data-ttu-id="70f33-129">في الحقل "رسالة إلى البنك"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="70f33-129">In the Message to bank field, type a value.</span></span>
16. <span data-ttu-id="70f33-130">في الحقل "مرجع سعر الصرف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="70f33-130">In the Exchange reference field, type a value.</span></span>
    * <span data-ttu-id="70f33-131">هذا هو الرقم المرجعي لأي سعر صرف ذي استحقاق آجل أو ثابت.</span><span class="sxs-lookup"><span data-stu-id="70f33-131">This is the reference number for any forward-term or fixed-term rate of exchange.</span></span>  
17. <span data-ttu-id="70f33-132">في الحقل "العملة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="70f33-132">In the Currency field, enter or select a value.</span></span>
    * <span data-ttu-id="70f33-133">عندما يتم إصدار إشعارات مسبقة، يوفر هذا المقطع نظرة عامة حول حالتها (معلقة أو تمت الموافقة عليها).</span><span class="sxs-lookup"><span data-stu-id="70f33-133">When prenotes are issued, this section provides an overview of their status (pending or approved).</span></span>  
18. <span data-ttu-id="70f33-134">قم بتوسيع المقطع "عنوان".</span><span class="sxs-lookup"><span data-stu-id="70f33-134">Expand the Address section.</span></span>
19. <span data-ttu-id="70f33-135">قم بتوسيع مقطع "الإشعارات المسبقة‬".</span><span class="sxs-lookup"><span data-stu-id="70f33-135">Expand the Prenotes section.</span></span>
20. <span data-ttu-id="70f33-136">‏‫قم بتوسيع المقطع "معلومات الاتصال‬‬".</span><span class="sxs-lookup"><span data-stu-id="70f33-136">Expand the Contact information section.</span></span>
21. <span data-ttu-id="70f33-137">في حقل الهاتف، أدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="70f33-137">In the Telephone field, type a value.</span></span>
22. <span data-ttu-id="70f33-138">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="70f33-138">Close the page.</span></span>
23. <span data-ttu-id="70f33-139">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="70f33-139">Click Edit.</span></span>
24. <span data-ttu-id="70f33-140">قم بتوسيع قسم الدفع.</span><span class="sxs-lookup"><span data-stu-id="70f33-140">Expand the Payment section.</span></span>
25. <span data-ttu-id="70f33-141">في حقل "الحساب البنكي"، حدد الحساب الذي أنشأته للتوّ.</span><span class="sxs-lookup"><span data-stu-id="70f33-141">In the Bank  account field, select the account that you’ve just created.</span></span>
26. <span data-ttu-id="70f33-142">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="70f33-142">Click Save.</span></span>
    * <span data-ttu-id="70f33-143">قد يتم توارث العنوان من المجموعة البنكية، إذا تم تحديد واحد، أو يمكنك إضافته هنا.</span><span class="sxs-lookup"><span data-stu-id="70f33-143">The address may be inherited from the bank group, if one is specified, or you can add it here.</span></span>  


