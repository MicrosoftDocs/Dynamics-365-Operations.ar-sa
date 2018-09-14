--- 
title: "إنشاء أصناف قرض"
description: "إن أصناف القرض هي السجلات التي تساعدك على تعقب العناصر الفعلية، مثل الهواتف أو أجهزة الكمبيوتر، التي تقوم شركتك بإعارتها للعاملين."
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmLoanType, DefaultDashboard, HcmLoanItem, HcmWorkerLookUp
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: e17005bda302c58f5a6560fe9c4eda04e918c92f
ms.contentlocale: ar-sa
ms.lasthandoff: 09/14/2018

---
# <a name="create-loan-items"></a><span data-ttu-id="38d58-103">إنشاء أصناف قرض</span><span class="sxs-lookup"><span data-stu-id="38d58-103">Create loan items</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="38d58-104">إن أصناف القرض هي السجلات التي تساعدك على تعقب العناصر الفعلية، مثل الهواتف أو أجهزة الكمبيوتر، التي تقوم شركتك بإعارتها للعاملين.</span><span class="sxs-lookup"><span data-stu-id="38d58-104">Loan items are records that help you track physical items, such as phones or computers, that your company lends to workers.</span></span> <span data-ttu-id="38d58-105">يجب أن يكون لكل عنصر فعلي صنف قرض مناظر.</span><span class="sxs-lookup"><span data-stu-id="38d58-105">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="38d58-106">يجب أن يصف كل سجل من سجلات أصناف القرض ما الذي يتم إقراضه والشخص المسؤول عن القرض وعدد الأيام التي يمكن إقراض الصنف فيها.</span><span class="sxs-lookup"><span data-stu-id="38d58-106">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can be on loan.</span></span> <span data-ttu-id="38d58-107">يمكنك إنشاء أصناف قرض متعددة، مثل المفاتيح أو بطاقات الدخول أو الزي الموحد، في نفس الوقت.</span><span class="sxs-lookup"><span data-stu-id="38d58-107">You can create multiple loan items, such as keys, access cards, or uniforms, at the same time.</span></span> <span data-ttu-id="38d58-108">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="38d58-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-loan-types"></a><span data-ttu-id="38d58-109">إنشاء أنواع القروض</span><span class="sxs-lookup"><span data-stu-id="38d58-109">Create Loan types</span></span>
1. <span data-ttu-id="38d58-110">انتقل إلى الموارد البشرية > العاملون > أصناف القرض > أنواع القرض.</span><span class="sxs-lookup"><span data-stu-id="38d58-110">Go to Human resources > Workers > Loan items > Loan types.</span></span>
2. <span data-ttu-id="38d58-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="38d58-111">Click New.</span></span>
3. <span data-ttu-id="38d58-112">في الحقل "نوع القرض"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="38d58-112">In the Loan type field, type a value.</span></span>
4. <span data-ttu-id="38d58-113">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="38d58-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="38d58-114">أدخل عدد الأيام الممكنة لتجاوز الأصناف التي تم تعيينها لنوع القرض هذا.</span><span class="sxs-lookup"><span data-stu-id="38d58-114">Enter the number of days that items assigned to this loan type can be overdue.</span></span> 
6. <span data-ttu-id="38d58-115">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="38d58-115">Click Save.</span></span>
7. <span data-ttu-id="38d58-116">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="38d58-116">Close the page.</span></span>
8. <span data-ttu-id="38d58-117">قم بتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="38d58-117">Refresh the page.</span></span>

## <a name="create-loan-items"></a><span data-ttu-id="38d58-118">إنشاء أصناف القرض</span><span class="sxs-lookup"><span data-stu-id="38d58-118">Create Loan items</span></span>
1. <span data-ttu-id="38d58-119">انتقل إلى الموارد البشرية > العاملون > أصناف القرض > أصناف القرض‬.</span><span class="sxs-lookup"><span data-stu-id="38d58-119">Go to Human resources > Workers > Loan items > Loan items.</span></span>
2. <span data-ttu-id="38d58-120">انقر فوق "إنشاء أصناف القرض‬".</span><span class="sxs-lookup"><span data-stu-id="38d58-120">Click Create loan items.</span></span>
3. <span data-ttu-id="38d58-121">في الحقل "الكمية‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="38d58-121">In the Qty. field, enter a number.</span></span>
4. <span data-ttu-id="38d58-122">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="38d58-122">In the Description field, type a value.</span></span>
5. <span data-ttu-id="38d58-123">في الحقل "نوع القرض"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="38d58-123">In the Loan type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="38d58-124">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="38d58-124">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="38d58-125">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="38d58-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="38d58-126">يستخدم لإدخال عدد الأيام المسموح بإقراض الصنف فيها.</span><span class="sxs-lookup"><span data-stu-id="38d58-126">Enter the number of days the item can be on loan.</span></span>
    * <span data-ttu-id="38d58-127">يتم حساب القيمة الافتراضية للحقل "إرجاع مخطط‬" في صفحة "المعدات المقترضة‬" باعتبارها التاريخ الحالي زائد هذا الرقم.</span><span class="sxs-lookup"><span data-stu-id="38d58-127">The default value for the Planned return field on the Loaned equipment page is calculated as the current date plus this number.</span></span>  
9. <span data-ttu-id="38d58-128">في الحقل "الشخص المسؤول‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="38d58-128">In the Person in charge field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="38d58-129">انقر فوق تحديد.</span><span class="sxs-lookup"><span data-stu-id="38d58-129">Click Select.</span></span>
11. <span data-ttu-id="38d58-130">في الحقل "‏‫قيمة البداية‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="38d58-130">In the Starting value field, enter a number.</span></span>
12. <span data-ttu-id="38d58-131">في الحقل "الفاصل الزمني"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="38d58-131">In the Interval field, enter a number.</span></span>
13. <span data-ttu-id="38d58-132">في الحقل "التنسيق"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="38d58-132">In the Format field, type a value.</span></span>
    * <span data-ttu-id="38d58-133">على سبيل المثال، إذا كان رقم البدء لصنف القرص هو 10، فأدخل رمزي الأرقام (##) في الحقل "تنسيق".</span><span class="sxs-lookup"><span data-stu-id="38d58-133">For example, if the starting number for a loan item is 10, enter two number symbols symbols in the Format field.</span></span>  
14. <span data-ttu-id="38d58-134">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="38d58-134">Click OK.</span></span>
15. <span data-ttu-id="38d58-135">قم بتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="38d58-135">Refresh the page.</span></span>


