--- 
title: " تكوين معالجة بطاقة الائتمان"
description: "يتناول هذا الإجراء كيفية عرض قائمة بممولي خدمات الدفع وكيفية تكوين حساب مدفوعات للحسابات المدينة."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c8e7bfbf6b51aca9cf8a7f800ac7db22c0330d00
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="configure-credit-card-processing"></a><span data-ttu-id="514f3-103"> تكوين معالجة بطاقة الائتمان</span><span class="sxs-lookup"><span data-stu-id="514f3-103">Configure credit card processing</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="514f3-104">يتناول هذا الإجراء كيفية عرض قائمة بممولي خدمات الدفع وكيفية تكوين حساب مدفوعات للحسابات المدينة.</span><span class="sxs-lookup"><span data-stu-id="514f3-104">This procedure walks through how to view the list of payment providers and how to configure a payment account for accounts receivable.</span></span> <span data-ttu-id="514f3-105">يستخدم هذا الإجراء شركة USRT في بيانات العرض التوضيحي‬ وهو مخصص للمسؤولين ومتخصصي تكنولوجيا المعلومات.</span><span class="sxs-lookup"><span data-stu-id="514f3-105">This procedure uses the USRT company in demo data and is intended for Administrators and IT Professionals.</span></span>


## <a name="view-a-list-of-payment-providers"></a><span data-ttu-id="514f3-106">عرض قائمة بممولي خدمات الدفع</span><span class="sxs-lookup"><span data-stu-id="514f3-106">View a list of payment providers</span></span>
1. <span data-ttu-id="514f3-107">انتقل إلى الحسابات المدينة > إعداد المدفوعات‬ > ‏‫خدمات الدفع‬.</span><span class="sxs-lookup"><span data-stu-id="514f3-107">Go to Accounts receivable > Payments setup > Payment services.</span></span>
2. <span data-ttu-id="514f3-108">انقر فوق عرض الممولين المتوفرين.</span><span class="sxs-lookup"><span data-stu-id="514f3-108">Click View available providers.</span></span>

## <a name="configure-payment-account"></a><span data-ttu-id="514f3-109">تكوين حساب المدفوعات</span><span class="sxs-lookup"><span data-stu-id="514f3-109">Configure payment account</span></span>
1. <span data-ttu-id="514f3-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="514f3-110">Click New.</span></span>
2. <span data-ttu-id="514f3-111">في حقل "خدمة الدفع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="514f3-111">In the Payment service field, type a value.</span></span>
3. <span data-ttu-id="514f3-112">في حقل "‏‫موصل المدفوعات‬"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="514f3-112">In the Payment connector field, select an option.</span></span>
4. <span data-ttu-id="514f3-113">قم بتبديل التوسيع لقسم "‏‫حساب خدمة الدفع".</span><span class="sxs-lookup"><span data-stu-id="514f3-113">Toggle the expansion of the Payment service account section.</span></span>
5. <span data-ttu-id="514f3-114">في حقل "‏‫البيئة:"، اكتب "PROD".</span><span class="sxs-lookup"><span data-stu-id="514f3-114">In the Environment: field, type 'PROD'.</span></span>
6. <span data-ttu-id="514f3-115">انقر فوق أنواع بطاقات الائتمان.</span><span class="sxs-lookup"><span data-stu-id="514f3-115">Click Credit card types.</span></span>
7. <span data-ttu-id="514f3-116">في حقل "‏‫دفتر يومية المدفوعات‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="514f3-116">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="514f3-117">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="514f3-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="514f3-118">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="514f3-118">Click Add.</span></span>
10. <span data-ttu-id="514f3-119">في الحقل "العملة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="514f3-119">In the Currency field, type a value.</span></span>
11. <span data-ttu-id="514f3-120">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="514f3-120">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="514f3-121">في حقل "‏‫دفتر يومية المدفوعات‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="514f3-121">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="514f3-122">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="514f3-122">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="514f3-123">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="514f3-123">Click Add.</span></span>
15. <span data-ttu-id="514f3-124">في الحقل "العملة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="514f3-124">In the Currency field, type a value.</span></span>
16. <span data-ttu-id="514f3-125">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="514f3-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="514f3-126">يمكنك تكرار هذه الخطوات للعديد من أنواع البطاقات التي تحتاجها.</span><span class="sxs-lookup"><span data-stu-id="514f3-126">You can repeat these steps for as many card types as you need.</span></span>  
17. <span data-ttu-id="514f3-127">في حقل "‏‫دفتر يومية المدفوعات‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="514f3-127">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="514f3-128">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="514f3-128">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="514f3-129">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="514f3-129">Click Add.</span></span>
20. <span data-ttu-id="514f3-130">في الحقل "العملة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="514f3-130">In the Currency field, type a value.</span></span>
21. <span data-ttu-id="514f3-131">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="514f3-131">Click Save.</span></span>
22. <span data-ttu-id="514f3-132">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="514f3-132">Close the page.</span></span>
23. <span data-ttu-id="514f3-133">انقر فوق "التحقق من الصحة‬".</span><span class="sxs-lookup"><span data-stu-id="514f3-133">Click Validate.</span></span>
24. <span data-ttu-id="514f3-134">انقر فوق المعالج الافتراضي لخانة الاختيار بطاقات الائتمان الجديدة.</span><span class="sxs-lookup"><span data-stu-id="514f3-134">Click the Default processor for new credit cards checkbox.</span></span>
25. <span data-ttu-id="514f3-135">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="514f3-135">Click Save.</span></span>


