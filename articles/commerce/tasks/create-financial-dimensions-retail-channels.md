---
title: إنشاء الأبعاد المالية لقنوات البيع بالتجزئة وتكوين قيم الأبعاد في المتاجر
description: يتناول هذا الإجراء إنشاء بعد مالي لقنوات التجارة بقيم الأبعاد والخطوات لتكوين قيم الأبعاد المالية في المتاجر.
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
ms.openlocfilehash: ea36732023092f714b3a783d98b512c0fea7dade
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141397"
---
# <a name="create-financial-dimensions-for-retail-channels-and-configure-dimension-values-on-stores"></a><span data-ttu-id="71952-103">إنشاء الأبعاد المالية لقنوات البيع بالتجزئة وتكوين قيم الأبعاد في المتاجر</span><span class="sxs-lookup"><span data-stu-id="71952-103">Create financial dimensions for retail channels and configure dimension values on stores</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="71952-104">يتناول هذا الإجراء إنشاء بعد مالي لقنوات التجارة بقيم الأبعاد والخطوات لتكوين قيم الأبعاد المالية في المتاجر.</span><span class="sxs-lookup"><span data-stu-id="71952-104">This procedure walks through creating a commerce channel financial dimension with dimension values and steps to configure financial dimension values on stores.</span></span> <span data-ttu-id="71952-105">لا يتضمن الموضوع خطوات أخرى ذات صلة، مثل إنشاء مجموعات الأبعاد وبُنى الحسابات.</span><span class="sxs-lookup"><span data-stu-id="71952-105">The topic does not include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="71952-106">ويستخدم هذا الإجراء شركة USRT في بيانات العرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="71952-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="71952-107">انتقل إلى دفتر الأستاذ العام > دليل الحسابات > الأبعاد > الأبعاد المالية.</span><span class="sxs-lookup"><span data-stu-id="71952-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="71952-108">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="71952-108">Click New.</span></span>
3. <span data-ttu-id="71952-109">في حقل "‏‫استخدام القيم من‬"، حدد "قنوات Commerce".</span><span class="sxs-lookup"><span data-stu-id="71952-109">In the Use values from field, select 'Commerce channels'.</span></span>
4. <span data-ttu-id="71952-110">في حقل "‏‫اسم البُعد‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="71952-110">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="71952-111">انقر فوق تنشيط.</span><span class="sxs-lookup"><span data-stu-id="71952-111">Click Activate.</span></span>
6. <span data-ttu-id="71952-112">انقر فوق "إغلاق".</span><span class="sxs-lookup"><span data-stu-id="71952-112">Click Close.</span></span>
7. <span data-ttu-id="71952-113">انقر فوق تنشيط.</span><span class="sxs-lookup"><span data-stu-id="71952-113">Click Activate.</span></span>
8. <span data-ttu-id="71952-114">انقر فوق "قيم الأبعاد".</span><span class="sxs-lookup"><span data-stu-id="71952-114">Click Dimension values.</span></span>
9. <span data-ttu-id="71952-115">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="71952-115">Close the page.</span></span>
10. <span data-ttu-id="71952-116">انقر فوق حفظ.</span><span class="sxs-lookup"><span data-stu-id="71952-116">Click Save.</span></span>
11. <span data-ttu-id="71952-117">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="71952-117">Close the page.</span></span>
12. <span data-ttu-id="71952-118">انتقل إلى Retail and Commerce > القنوات > المتاجر > جميع المتاجر.</span><span class="sxs-lookup"><span data-stu-id="71952-118">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
13. <span data-ttu-id="71952-119">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="71952-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="71952-120">بدّل توسيع المقطع "الأبعاد المالية‬".</span><span class="sxs-lookup"><span data-stu-id="71952-120">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="71952-121">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="71952-121">Click Edit.</span></span>
16. <span data-ttu-id="71952-122">في الحقل "قناة التجارة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="71952-122">In the Commerce channel field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="71952-123">في القائمة، ابحث عن قيمة البُعد وحددها للمتجر الذي يتم تحديثه.</span><span class="sxs-lookup"><span data-stu-id="71952-123">In the list, find and select the dimension value for the store being updated.</span></span>
18. <span data-ttu-id="71952-124">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="71952-124">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="71952-125">في الحقل "CostCenter"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="71952-125">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="71952-126">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="71952-126">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="71952-127">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="71952-127">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="71952-128">في الحقل "القسم"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="71952-128">In the Department field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="71952-129">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="71952-129">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="71952-130">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="71952-130">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="71952-131">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="71952-131">Click Save.</span></span>

