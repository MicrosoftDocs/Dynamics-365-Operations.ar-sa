--- 
title: "إنشاء أصناف قرض"
description: "إن أصناف القرض هي السجلات التي تساعدك على تعقب العناصر الفعلية، مثل الهواتف أو أجهزة الكمبيوتر، التي تقوم شركتك بإعارتها للعاملين."
author: kherr75
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 65655283c70c99b5d64289b319ecc69f6e414221
ms.contentlocale: ar-sa
ms.lasthandoff: 07/27/2017

---
# <a name="create-loan-items"></a><span data-ttu-id="5d64e-103">إنشاء أصناف قرض</span><span class="sxs-lookup"><span data-stu-id="5d64e-103">Create loan items</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5d64e-104">إن أصناف القرض هي السجلات التي تساعدك على تعقب العناصر الفعلية، مثل الهواتف أو أجهزة الكمبيوتر، التي تقوم شركتك بإعارتها للعاملين.</span><span class="sxs-lookup"><span data-stu-id="5d64e-104">Loan items are records that help you track physical items, such as phones or computers, that your company lends to workers.</span></span> <span data-ttu-id="5d64e-105">يجب أن يكون لكل عنصر فعلي صنف قرض مناظر.</span><span class="sxs-lookup"><span data-stu-id="5d64e-105">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="5d64e-106">يجب أن يصف كل سجل من سجلات أصناف القرض ما الذي يتم إقراضه والشخص المسؤول عن القرض وعدد الأيام التي يمكن إقراض الصنف فيها.</span><span class="sxs-lookup"><span data-stu-id="5d64e-106">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can be on loan.</span></span> <span data-ttu-id="5d64e-107">يمكنك إنشاء أصناف قرض متعددة، مثل المفاتيح أو بطاقات الدخول أو الزي الموحد، في نفس الوقت.</span><span class="sxs-lookup"><span data-stu-id="5d64e-107">You can create multiple loan items, such as keys, access cards, or uniforms, at the same time.</span></span> <span data-ttu-id="5d64e-108">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="5d64e-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-loan-types"></a><span data-ttu-id="5d64e-109">إنشاء أنواع القروض</span><span class="sxs-lookup"><span data-stu-id="5d64e-109">Create Loan types</span></span>
1. <span data-ttu-id="5d64e-110">انتقل إلى الموارد البشرية > العاملون > أصناف القرض > أنواع القرض.</span><span class="sxs-lookup"><span data-stu-id="5d64e-110">Go to Human resources > Workers > Loan items > Loan types.</span></span>
2. <span data-ttu-id="5d64e-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="5d64e-111">Click New.</span></span>
3. <span data-ttu-id="5d64e-112">في الحقل "نوع القرض"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="5d64e-112">In the Loan type field, type a value.</span></span>
4. <span data-ttu-id="5d64e-113">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="5d64e-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="5d64e-114">أدخل عدد الأيام الممكنة لتجاوز الأصناف التي تم تعيينها لنوع القرض هذا.</span><span class="sxs-lookup"><span data-stu-id="5d64e-114">Enter the number of days that items assigned to this loan type can be overdue.</span></span> 
6. <span data-ttu-id="5d64e-115">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="5d64e-115">Click Save.</span></span>
7. <span data-ttu-id="5d64e-116">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="5d64e-116">Close the page.</span></span>
8. <span data-ttu-id="5d64e-117">قم بتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="5d64e-117">Refresh the page.</span></span>

## <a name="create-loan-items"></a><span data-ttu-id="5d64e-118">إنشاء أصناف القرض</span><span class="sxs-lookup"><span data-stu-id="5d64e-118">Create Loan items</span></span>
1. <span data-ttu-id="5d64e-119">انتقل إلى الموارد البشرية > العاملون > أصناف القرض > أصناف القرض‬.</span><span class="sxs-lookup"><span data-stu-id="5d64e-119">Go to Human resources > Workers > Loan items > Loan items.</span></span>
2. <span data-ttu-id="5d64e-120">انقر فوق "إنشاء أصناف القرض‬".</span><span class="sxs-lookup"><span data-stu-id="5d64e-120">Click Create loan items.</span></span>
3. <span data-ttu-id="5d64e-121">في حقل الكمية</span><span class="sxs-lookup"><span data-stu-id="5d64e-121">In the Qty.</span></span> <span data-ttu-id="5d64e-122">، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="5d64e-122">field, enter a number.</span></span>
4. <span data-ttu-id="5d64e-123">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="5d64e-123">In the Description field, type a value.</span></span>
5. <span data-ttu-id="5d64e-124">في الحقل "نوع القرض"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="5d64e-124">In the Loan type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="5d64e-125">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="5d64e-125">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="5d64e-126">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="5d64e-126">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="5d64e-127">يستخدم لإدخال عدد الأيام المسموح بإقراض الصنف فيها.</span><span class="sxs-lookup"><span data-stu-id="5d64e-127">Enter the number of days the item can be on loan.</span></span>
    * <span data-ttu-id="5d64e-128">يتم حساب القيمة الافتراضية للحقل "إرجاع مخطط‬" في صفحة "المعدات المقترضة‬" باعتبارها التاريخ الحالي زائد هذا الرقم.</span><span class="sxs-lookup"><span data-stu-id="5d64e-128">The default value for the Planned return field on the Loaned equipment page is calculated as the current date plus this number.</span></span>  
9. <span data-ttu-id="5d64e-129">في الحقل "الشخص المسؤول‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="5d64e-129">In the Person in charge field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="5d64e-130">انقر فوق تحديد.</span><span class="sxs-lookup"><span data-stu-id="5d64e-130">Click Select.</span></span>
11. <span data-ttu-id="5d64e-131">في الحقل "‏‫قيمة البداية‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="5d64e-131">In the Starting value field, enter a number.</span></span>
12. <span data-ttu-id="5d64e-132">في الحقل "الفاصل الزمني"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="5d64e-132">In the Interval field, enter a number.</span></span>
13. <span data-ttu-id="5d64e-133">في الحقل "التنسيق"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="5d64e-133">In the Format field, type a value.</span></span>
    * <span data-ttu-id="5d64e-134">على سبيل المثال، إذا كان رقم البدء لصنف القرص هو 10، فأدخل رمزي الأرقام (##) في الحقل "تنسيق".</span><span class="sxs-lookup"><span data-stu-id="5d64e-134">For example, if the starting number for a loan item is 10, enter two number symbols symbols in the Format field.</span></span>  
14. <span data-ttu-id="5d64e-135">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="5d64e-135">Click OK.</span></span>
15. <span data-ttu-id="5d64e-136">قم بتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="5d64e-136">Refresh the page.</span></span>


