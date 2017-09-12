--- 
title: " إنشاء الأبعاد المالية لثنوات البيع بالتجزئة وتكوين قيم الأبعاد في المتاجر"
description: "يتناول هذا الإجراء إنشاء بعد مالي لقنوات البيع بالتجزئة بقيم الأبعاد والخطوات لتكوين قيم الأبعاد المالية في متاجر البيع بالتجزئة."
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
ms.openlocfilehash: 56b586e971cfd4684f3c0b259270cc8b31521ac9
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="create-financial-dimensions-for-retail-channels-and-configure-dimension-values-on-stores"></a><span data-ttu-id="d4c6c-103"> إنشاء الأبعاد المالية لثنوات البيع بالتجزئة وتكوين قيم الأبعاد في المتاجر</span><span class="sxs-lookup"><span data-stu-id="d4c6c-103">Create financial dimensions for Retail channels and configure dimension values on stores</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="d4c6c-104">يتناول هذا الإجراء إنشاء بعد مالي لقنوات البيع بالتجزئة بقيم الأبعاد والخطوات لتكوين قيم الأبعاد المالية في متاجر البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="d4c6c-104">This procedure walks through creating a retail channel financial dimension with dimension values and steps to configure financial dimension values on retail stores.</span></span> <span data-ttu-id="d4c6c-105">لا يتضمن الموضوع خطوات أخرى ذات صلة، مثل إنشاء مجموعات الأبعاد وبُنى الحسابات.</span><span class="sxs-lookup"><span data-stu-id="d4c6c-105">The topic does not include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="d4c6c-106">ويستخدم هذا الإجراء شركة USRT في بيانات العرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="d4c6c-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="d4c6c-107">انتقل إلى دفتر الأستاذ العام > دليل الحسابات > الأبعاد > الأبعاد المالية.</span><span class="sxs-lookup"><span data-stu-id="d4c6c-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="d4c6c-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="d4c6c-108">Click New.</span></span>
3. <span data-ttu-id="d4c6c-109">في حقل "‏‫استخدام القيم من‬"، حدد "قنوات البيع بالتجزئة".</span><span class="sxs-lookup"><span data-stu-id="d4c6c-109">In the Use values from field, select 'Retail channels'.</span></span>
4. <span data-ttu-id="d4c6c-110">في حقل "‏‫اسم البُعد‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d4c6c-110">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="d4c6c-111">انقر فوق تنشيط.</span><span class="sxs-lookup"><span data-stu-id="d4c6c-111">Click Activate.</span></span>
6. <span data-ttu-id="d4c6c-112">انقر فوق "إغلاق".</span><span class="sxs-lookup"><span data-stu-id="d4c6c-112">Click Close.</span></span>
7. <span data-ttu-id="d4c6c-113">انقر فوق تنشيط.</span><span class="sxs-lookup"><span data-stu-id="d4c6c-113">Click Activate.</span></span>
8. <span data-ttu-id="d4c6c-114">انقر فوق "قيم الأبعاد".</span><span class="sxs-lookup"><span data-stu-id="d4c6c-114">Click Dimension values.</span></span>
9. <span data-ttu-id="d4c6c-115">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d4c6c-115">Close the page.</span></span>
10. <span data-ttu-id="d4c6c-116">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="d4c6c-116">Click Save.</span></span>
11. <span data-ttu-id="d4c6c-117">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d4c6c-117">Close the page.</span></span>
12. <span data-ttu-id="d4c6c-118">انتقل إلى البيع بالتجزئة والتجارة > القنوات > متاجر البيع بالتجزئة > جميع متاجر البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="d4c6c-118">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
13. <span data-ttu-id="d4c6c-119">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d4c6c-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="d4c6c-120">بدّل توسيع المقطع "الأبعاد المالية‬".</span><span class="sxs-lookup"><span data-stu-id="d4c6c-120">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="d4c6c-121">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="d4c6c-121">Click Edit.</span></span>
16. <span data-ttu-id="d4c6c-122">في حقل "Retailchannel‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="d4c6c-122">In the Retailchannel field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="d4c6c-123">في القائمة، ابحث عن قيمة البُعد وحددها للمتجر الذي يتم تحديثه.</span><span class="sxs-lookup"><span data-stu-id="d4c6c-123">In the list, find and select the dimension value for the store being updated.</span></span>
18. <span data-ttu-id="d4c6c-124">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d4c6c-124">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="d4c6c-125">في الحقل "CostCenter"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="d4c6c-125">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="d4c6c-126">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="d4c6c-126">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="d4c6c-127">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d4c6c-127">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="d4c6c-128">في الحقل "القسم"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="d4c6c-128">In the Department field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="d4c6c-129">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="d4c6c-129">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="d4c6c-130">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d4c6c-130">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="d4c6c-131">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="d4c6c-131">Click Save.</span></span>


