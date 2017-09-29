--- 
title: "إنشاء حركات ضريبة المبيعات في المستندات"
description: "يتم حساب ضريبة المبيعات على المستندات عن طريق توفير مجموعة ضريبة المبيعات ومجموعة ضرائب المبيعات للأصناف‬ على بنود المستند."
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 27bf4ba33bd7d22443512d072572b9b1ffc164fa
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="create-sales-tax-transactions-on-documents"></a><span data-ttu-id="7a09a-103">إنشاء حركات ضريبة المبيعات في المستندات</span><span class="sxs-lookup"><span data-stu-id="7a09a-103">Create sales tax transactions on documents</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7a09a-104">يتم حساب ضريبة المبيعات على المستندات عن طريق توفير مجموعة ضريبة المبيعات ومجموعة ضرائب المبيعات للأصناف‬ على بنود المستند.</span><span class="sxs-lookup"><span data-stu-id="7a09a-104">Sales tax on documents is calculated by providing a Sales tax group and an Item sales tax group on document lines.</span></span> <span data-ttu-id="7a09a-105">وهذه تأتي بشكل افتراضي من البيانات الرئيسية، ولكن يمكن تغييرها يدويًا إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="7a09a-105">These default from master data but can be changed manually if necessary.</span></span> <span data-ttu-id="7a09a-106">يمكن التحقق من ضريبة المبيعات المحسوبة على مستوى البند والمستند.</span><span class="sxs-lookup"><span data-stu-id="7a09a-106">The calculated sales tax can be checked on a line and document level.</span></span> <span data-ttu-id="7a09a-107">تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="7a09a-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="7a09a-108">انتقل إلى الحسابات المدينة > الأوامر > كافة أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="7a09a-108">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="7a09a-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="7a09a-109">Click New.</span></span>
3. <span data-ttu-id="7a09a-110">في الحقل "حساب العميل"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="7a09a-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="7a09a-111">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="7a09a-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="7a09a-112">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="7a09a-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="7a09a-113">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="7a09a-113">Click OK.</span></span>
7. <span data-ttu-id="7a09a-114">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="7a09a-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="7a09a-115">في الحقل "رقم الصنف"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="7a09a-115">In the Item number field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="7a09a-116">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="7a09a-116">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="7a09a-117">في حقل "سعر الوحدة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="7a09a-117">In the Unit price field, enter a number.</span></span>
11. <span data-ttu-id="7a09a-118">قم بتوسيع المقطع "تفاصيل البند" أو طيّه.</span><span class="sxs-lookup"><span data-stu-id="7a09a-118">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="7a09a-119">انقر فوق علامة التبويب "إعداد".</span><span class="sxs-lookup"><span data-stu-id="7a09a-119">Click the Setup tab.</span></span>
13. <span data-ttu-id="7a09a-120">في الحقل "مجموعة ضرائب المبيعات للأصناف‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="7a09a-120">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="7a09a-121">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="7a09a-121">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="7a09a-122">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="7a09a-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="7a09a-123">انقر فوق "الماليات‬".</span><span class="sxs-lookup"><span data-stu-id="7a09a-123">Click Financials.</span></span>
17. <span data-ttu-id="7a09a-124">انقر فوق "ضريبة المبيعات".</span><span class="sxs-lookup"><span data-stu-id="7a09a-124">Click Sales tax.</span></span>
18. <span data-ttu-id="7a09a-125">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="7a09a-125">Click OK.</span></span>
19. <span data-ttu-id="7a09a-126">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="7a09a-126">Click Add line.</span></span>
20. <span data-ttu-id="7a09a-127">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="7a09a-127">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="7a09a-128">في الحقل "رقم الصنف"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="7a09a-128">In the Item number field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="7a09a-129">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="7a09a-129">In the list, find and select the desired record.</span></span>
23. <span data-ttu-id="7a09a-130">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="7a09a-130">In the list, click the link in the selected row.</span></span>
24. <span data-ttu-id="7a09a-131">في حقل "سعر الوحدة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="7a09a-131">In the Unit price field, enter a number.</span></span>
25. <span data-ttu-id="7a09a-132">في الحقل "مجموعة ضرائب المبيعات للأصناف‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="7a09a-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
26. <span data-ttu-id="7a09a-133">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="7a09a-133">In the list, find and select the desired record.</span></span>
27. <span data-ttu-id="7a09a-134">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="7a09a-134">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="7a09a-135">في جزء الإجراءات، انقر فوق "بيع‬".</span><span class="sxs-lookup"><span data-stu-id="7a09a-135">On the Action Pane, click Sell.</span></span>
29. <span data-ttu-id="7a09a-136">انقر فوق "ضريبة المبيعات".</span><span class="sxs-lookup"><span data-stu-id="7a09a-136">Click Sales tax.</span></span>
30. <span data-ttu-id="7a09a-137">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="7a09a-137">Click OK.</span></span>


