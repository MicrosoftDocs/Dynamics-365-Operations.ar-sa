---
title: " تكوين معالجة بطاقة الائتمان"
description: يتناول هذا الإجراء كيفية عرض قائمة بممولي خدمات الدفع وكيفية تكوين حساب مدفوعات للحسابات المدينة.
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 04ce158a833d04122ee5a724165b06925cea1185
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021487"
---
# <a name="configure-credit-card-processing"></a><span data-ttu-id="feb6d-103"> تكوين معالجة بطاقة الائتمان</span><span class="sxs-lookup"><span data-stu-id="feb6d-103">Configure credit card processing</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="feb6d-104">يتناول هذا الإجراء كيفية عرض قائمة بممولي خدمات الدفع وكيفية تكوين حساب مدفوعات للحسابات المدينة.</span><span class="sxs-lookup"><span data-stu-id="feb6d-104">This procedure walks through how to view the list of payment providers and how to configure a payment account for accounts receivable.</span></span> <span data-ttu-id="feb6d-105">يستخدم هذا الإجراء شركة USRT في بيانات العرض التوضيحي‬ وهو مخصص للمسؤولين ومتخصصي تكنولوجيا المعلومات.</span><span class="sxs-lookup"><span data-stu-id="feb6d-105">This procedure uses the USRT company in demo data and is intended for Administrators and IT Professionals.</span></span>


## <a name="view-a-list-of-payment-providers"></a><span data-ttu-id="feb6d-106">عرض قائمة بممولي خدمات الدفع</span><span class="sxs-lookup"><span data-stu-id="feb6d-106">View a list of payment providers</span></span>
1. <span data-ttu-id="feb6d-107">انتقل إلى الحسابات المدينة > إعداد المدفوعات‬ > ‏‫خدمات الدفع‬.</span><span class="sxs-lookup"><span data-stu-id="feb6d-107">Go to Accounts receivable > Payments setup > Payment services.</span></span>
2. <span data-ttu-id="feb6d-108">انقر فوق عرض الممولين المتوفرين.</span><span class="sxs-lookup"><span data-stu-id="feb6d-108">Click View available providers.</span></span>

## <a name="configure-payment-account"></a><span data-ttu-id="feb6d-109">تكوين حساب المدفوعات</span><span class="sxs-lookup"><span data-stu-id="feb6d-109">Configure payment account</span></span>
1. <span data-ttu-id="feb6d-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="feb6d-110">Click New.</span></span>
2. <span data-ttu-id="feb6d-111">في حقل "خدمة الدفع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="feb6d-111">In the Payment service field, type a value.</span></span>
3. <span data-ttu-id="feb6d-112">في حقل "‏‫موصل المدفوعات‬"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="feb6d-112">In the Payment connector field, select an option.</span></span>
4. <span data-ttu-id="feb6d-113">قم بتبديل التوسيع لقسم "‏‫حساب خدمة الدفع".</span><span class="sxs-lookup"><span data-stu-id="feb6d-113">Toggle the expansion of the Payment service account section.</span></span>
5. <span data-ttu-id="feb6d-114">في حقل "‏‫البيئة:"، اكتب "PROD".</span><span class="sxs-lookup"><span data-stu-id="feb6d-114">In the Environment: field, type 'PROD'.</span></span>
6. <span data-ttu-id="feb6d-115">انقر فوق أنواع بطاقات الائتمان.</span><span class="sxs-lookup"><span data-stu-id="feb6d-115">Click Credit card types.</span></span>
7. <span data-ttu-id="feb6d-116">في حقل "‏‫دفتر يومية المدفوعات‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="feb6d-116">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="feb6d-117">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="feb6d-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="feb6d-118">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="feb6d-118">Click Add.</span></span>
10. <span data-ttu-id="feb6d-119">في الحقل "العملة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="feb6d-119">In the Currency field, type a value.</span></span>
11. <span data-ttu-id="feb6d-120">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="feb6d-120">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="feb6d-121">في حقل "‏‫دفتر يومية المدفوعات‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="feb6d-121">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="feb6d-122">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="feb6d-122">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="feb6d-123">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="feb6d-123">Click Add.</span></span>
15. <span data-ttu-id="feb6d-124">في الحقل "العملة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="feb6d-124">In the Currency field, type a value.</span></span>
16. <span data-ttu-id="feb6d-125">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="feb6d-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="feb6d-126">يمكنك تكرار هذه الخطوات للعديد من أنواع البطاقات التي تحتاجها.</span><span class="sxs-lookup"><span data-stu-id="feb6d-126">You can repeat these steps for as many card types as you need.</span></span>  
17. <span data-ttu-id="feb6d-127">في حقل "‏‫دفتر يومية المدفوعات‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="feb6d-127">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="feb6d-128">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="feb6d-128">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="feb6d-129">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="feb6d-129">Click Add.</span></span>
20. <span data-ttu-id="feb6d-130">في الحقل "العملة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="feb6d-130">In the Currency field, type a value.</span></span>
21. <span data-ttu-id="feb6d-131">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="feb6d-131">Click Save.</span></span>
22. <span data-ttu-id="feb6d-132">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="feb6d-132">Close the page.</span></span>
23. <span data-ttu-id="feb6d-133">انقر فوق "التحقق من الصحة‬".</span><span class="sxs-lookup"><span data-stu-id="feb6d-133">Click Validate.</span></span>
24. <span data-ttu-id="feb6d-134">انقر فوق المعالج الافتراضي لخانة الاختيار بطاقات الائتمان الجديدة.</span><span class="sxs-lookup"><span data-stu-id="feb6d-134">Click the Default processor for new credit cards checkbox.</span></span>
25. <span data-ttu-id="feb6d-135">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="feb6d-135">Click Save.</span></span>
