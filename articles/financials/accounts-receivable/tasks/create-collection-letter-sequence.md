--- 
title: "إنشاء تسلسل خطاب تحصيل"
description: "استخدم دليل المهمة هذا لإنشاء تسلسل خطاب تحصيل."
author: mikefalkner
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: d5afab858761e9dc91c4f34790cc550c752fd1d1
ms.contentlocale: ar-sa
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-collection-letter-sequence"></a><span data-ttu-id="66fc4-103">إنشاء تسلسل خطاب تحصيل</span><span class="sxs-lookup"><span data-stu-id="66fc4-103">Create a collection letter sequence</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="66fc4-104">استخدم دليل المهمة هذا لإنشاء تسلسل خطاب تحصيل.</span><span class="sxs-lookup"><span data-stu-id="66fc4-104">Use this task guide to create a collection letter sequence.</span></span> <span data-ttu-id="66fc4-105">تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="66fc4-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="66fc4-106">انتقل إلى ‏‫التحصيلات والائتمان‬ > إعداد > إعداد تسلسل خطاب التحصيل‬.</span><span class="sxs-lookup"><span data-stu-id="66fc4-106">Go to Credit and collections > Setup > Set up collection letter sequence.</span></span>
2. <span data-ttu-id="66fc4-107">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="66fc4-107">Click New.</span></span>
3. <span data-ttu-id="66fc4-108">في الحقل "تسلسل خطاب التحصيل‬"، أدخل معرف تسلسل سيمثل التسلسل.</span><span class="sxs-lookup"><span data-stu-id="66fc4-108">In the Collection letter sequence field, enter a sequence ID that will represent the sequence.</span></span> <span data-ttu-id="66fc4-109">سيتم استخدامه عند إعداد ملف تعريف ترحيل.</span><span class="sxs-lookup"><span data-stu-id="66fc4-109">It will be used when you set up a posting profile.</span></span>
4. <span data-ttu-id="66fc4-110">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="66fc4-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="66fc4-111">شروط الدفع اختيارية.</span><span class="sxs-lookup"><span data-stu-id="66fc4-111">The terms of payment is optional.</span></span> <span data-ttu-id="66fc4-112">إذا قمت بإدخال قيمة هنا، فستستخدم فاتورة رسوم خطاب التحصيل شروط الدفع هذه بدلاً من شروط الدفع التي يتم تخزينها مع العميل.</span><span class="sxs-lookup"><span data-stu-id="66fc4-112">If you enter a value here, the collection letter fee invoice will use these terms of payment instead of the terms of payment stored with the customer.</span></span>  
5. <span data-ttu-id="66fc4-113">في الحقل "كود خطاب التحصيل"، حدد كود خطاب التحصيل الأول الذي تريد إرساله.</span><span class="sxs-lookup"><span data-stu-id="66fc4-113">In the collection letter code field, select the code for the first collection letter that you want to send.</span></span>
    * <span data-ttu-id="66fc4-114">يتم إنشاء خطاب التحصيل الأول وفقًا لتاريخ الاستحقاق على الفاتورة، والقيمة التي تقوم بإدخالها لفترة السماح في الحقل "الأيام" على هذا البند، ومعلومات أخرى تقوم بإدخالها على هذا البند.</span><span class="sxs-lookup"><span data-stu-id="66fc4-114">The first collection letter is created according to the due date on the invoice, the value that you enter for the grace period in the Days field on this line, and other information that you enter on this line.</span></span>  
6. <span data-ttu-id="66fc4-115">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="66fc4-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="66fc4-116">يتم تعيين عملة الرسوم بشكل افتراضي إلى عملة العميل.</span><span class="sxs-lookup"><span data-stu-id="66fc4-116">The currency for the fee defaults to the customer currency.</span></span> <span data-ttu-id="66fc4-117">بإمكان كود العملة هذا أن يكون مختلفًا عن عملة الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="66fc4-117">This currency code can be different than the invoice currency.</span></span>  
7. <span data-ttu-id="66fc4-118">انقر فوق "إضافة" لإضافة خطاب التحصيل التالي الذي سيتم إرساله في التسلسل</span><span class="sxs-lookup"><span data-stu-id="66fc4-118">Click Add to add the next collection letter that will be sent in the sequence</span></span>
    * <span data-ttu-id="66fc4-119">في الكثير من الحالات، يُعد خطاب التحصيل الأول مجرد تحذير.</span><span class="sxs-lookup"><span data-stu-id="66fc4-119">In many cases, the first collection letter is just a warning.</span></span> <span data-ttu-id="66fc4-120">يمكنك إضافة رسوم، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="66fc4-120">You can add fees if needed.</span></span>  
8. <span data-ttu-id="66fc4-121">في الحقل "كود خطاب التحصيل"، حدد كود خطاب التحصيل التالي الذي سيتم إرساله في التسلسل.</span><span class="sxs-lookup"><span data-stu-id="66fc4-121">In the collection letter code field, select the next collection letter that will be sent in the sequence.</span></span>
9. <span data-ttu-id="66fc4-122">في حقل "الوصف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="66fc4-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="66fc4-123">في الحقل "الحساب الرئيسي"، حدد حساب الإيرادات الذي سيتم استخدامه للرسوم.</span><span class="sxs-lookup"><span data-stu-id="66fc4-123">In the main account field, select the revenue account that will be used for fees.</span></span>
11. <span data-ttu-id="66fc4-124">أدخل الرسوم التي سيتم فرضها عند ترحيل خطاب التحصيل هذا.</span><span class="sxs-lookup"><span data-stu-id="66fc4-124">Enter the fee that will be charged when this collection letter is posted.</span></span>
12. <span data-ttu-id="66fc4-125">في الحقل "مجموعة ضرائب المبيعات للأصناف‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="66fc4-125">In the Item sales tax group field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="66fc4-126">حدد مجموعة ضريبة مبيعات الصنف‬ إذا كان يجب حساب ضريبة المبيعات على الرسوم.</span><span class="sxs-lookup"><span data-stu-id="66fc4-126">Select an item sales tax group if sales taxes must be calculated on the fee.</span></span>  
13. <span data-ttu-id="66fc4-127">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="66fc4-127">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="66fc4-128">أدخل الحد الأدنى للرصيد المتأخر المطلوب قبل إرسال خطاب تحصيل.</span><span class="sxs-lookup"><span data-stu-id="66fc4-128">Enter the minimum overdue balance required before a collection letter is sent.</span></span>
15. <span data-ttu-id="66fc4-129">أدخل عدد أيام السماح الذي ستسمح به.</span><span class="sxs-lookup"><span data-stu-id="66fc4-129">Enter the number of grace days that you will allow.</span></span>
    * <span data-ttu-id="66fc4-130">هذا هو عدد الأيام بعد تاريخ الاستحقاق حيث يمكن إنشاء خطاب تحصيل.</span><span class="sxs-lookup"><span data-stu-id="66fc4-130">This is the number of days after the due date that a collection letter can be generated.</span></span> <span data-ttu-id="66fc4-131">يعتمد تاريخ الاستحقاق المستخدم للحساب على موضع خطاب التحصيل في تسلسل خطابات التحصيل:   ⦁    ترتبط فترة السماح لخطاب التحصيل 1 بتاريخ الاستحقاق في الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="66fc4-131">The due date that is used for the calculation depends on the position of the collection letter in the collection letter sequence:   ⦁    The grace period for collection letter 1 is relative to the due date on the invoice.</span></span>  <span data-ttu-id="66fc4-132">⦁ ترتبط فترة السماح لخطابات التحصيل 2 وما فوقها بتاريخ ترحيل خطاب التحصيل السابق أو طباعته، وهذا يتوقف على التحديد في الحقل "تحديث كود خطاب التحصيل‬" في الصفحة "محددات الحسابات المدينة‬".</span><span class="sxs-lookup"><span data-stu-id="66fc4-132">⦁ The grace period for collection letters 2 and higher is relative to the date that the previous collection letter is posted or printed, depending on the selection in the Update collection letter code field in the Accounts receivable parameters page.</span></span>  
16. <span data-ttu-id="66fc4-133">انقر فوق "إضافة" لإضافة خطاب التحصيل الأخير في التسلسل.</span><span class="sxs-lookup"><span data-stu-id="66fc4-133">Click Add to add the last collection letter in the sequence.</span></span>
    * <span data-ttu-id="66fc4-134">يمكنك إضافة ما يصل لغاية خمسة أكواد خطاب تحصيل لتسلسل خطاب التحصيل.</span><span class="sxs-lookup"><span data-stu-id="66fc4-134">You can add up to five collection letter codes for a collection letter sequence.</span></span>  
17. <span data-ttu-id="66fc4-135">في الحقل "كود خطاب التحصيل"، حدد كود خطاب التحصيل التالي الذي سيتم إرساله في التسلسل.</span><span class="sxs-lookup"><span data-stu-id="66fc4-135">In the collection letter code field, select the next collection letter that will be sent in the sequence.</span></span>
18. <span data-ttu-id="66fc4-136">في حقل "الوصف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="66fc4-136">In the Description field, type a value.</span></span>
19. <span data-ttu-id="66fc4-137">في حقل "الحساب الرئيسي"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="66fc4-137">In the Main account field, specify the desired values.</span></span>
20. <span data-ttu-id="66fc4-138">في الحقل "الرسوم بالعملة‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="66fc4-138">In the Fee in currency field, enter a number.</span></span>
21. <span data-ttu-id="66fc4-139">في الحقل "مجموعة ضرائب المبيعات للأصناف‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="66fc4-139">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="66fc4-140">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="66fc4-140">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="66fc4-141">في الحقل "الحد الأدنى للرصيد المتأخر‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="66fc4-141">In the Minimum overdue balance field, enter a number.</span></span>
24. <span data-ttu-id="66fc4-142">في الحقل "الأيام"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="66fc4-142">In the Days field, enter a number.</span></span>
25. <span data-ttu-id="66fc4-143">حدد خانة الاختيار هذه لمنع العميل من إجراء عمليات تسليم وفوترة إضافية.</span><span class="sxs-lookup"><span data-stu-id="66fc4-143">Select this check box to stop the customer from additional deliveries and invoicing.</span></span>
    * <span data-ttu-id="66fc4-144">ولإلغاء حظر الحساب، حدد "لا" في حقل الفوترة والتسليم قيد الانتظار في صفحة العملاء.</span><span class="sxs-lookup"><span data-stu-id="66fc4-144">To unblock the account, select No in the Invoicing and delivery on hold field in the Customers page.</span></span>  
26. <span data-ttu-id="66fc4-145">وسّع علامة التبويب السريعة "ملاحظة".</span><span class="sxs-lookup"><span data-stu-id="66fc4-145">Expand the Note fasttab.</span></span>
27. <span data-ttu-id="66fc4-146">أدخل النص الذي سيظهر على خطاب التحصيل لكود خطاب التحصيل المحدد.</span><span class="sxs-lookup"><span data-stu-id="66fc4-146">Enter the text to appear on the collection letter for the selected collection letter code.</span></span>
    * <span data-ttu-id="66fc4-147">يمكن ترجمة هذا النص إلى لغات متعددة باستخدام القائمة "ترجمات" في أعلى مربع الملاحظة.</span><span class="sxs-lookup"><span data-stu-id="66fc4-147">You can translate this text in to multiple languages using the Translations menu above the note box.</span></span>  


