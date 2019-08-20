---
title: إنشاء حركات ضريبة المبيعات في المستندات
description: يتم حساب ضريبة المبيعات على المستندات عن طريق توفير مجموعة ضريبة المبيعات ومجموعة ضرائب المبيعات للأصناف‬ على بنود المستند.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 653b93744f5b891655cade0cb669d34179fca9cd
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846525"
---
# <a name="create-sales-tax-transactions-on-documents"></a><span data-ttu-id="26df5-103">إنشاء حركات ضريبة المبيعات في المستندات</span><span class="sxs-lookup"><span data-stu-id="26df5-103">Create sales tax transactions on documents</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="26df5-104">يتم حساب ضريبة المبيعات على المستندات عن طريق توفير مجموعة ضريبة المبيعات ومجموعة ضرائب المبيعات للأصناف‬ على بنود المستند.</span><span class="sxs-lookup"><span data-stu-id="26df5-104">Sales tax on documents is calculated by providing a Sales tax group and an Item sales tax group on document lines.</span></span> <span data-ttu-id="26df5-105">وهذه تأتي بشكل افتراضي من البيانات الرئيسية، ولكن يمكن تغييرها يدويًا إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="26df5-105">These default from master data but can be changed manually if necessary.</span></span> <span data-ttu-id="26df5-106">يمكن التحقق من ضريبة المبيعات المحسوبة على مستوى البند والمستند.</span><span class="sxs-lookup"><span data-stu-id="26df5-106">The calculated sales tax can be checked on a line and document level.</span></span> <span data-ttu-id="26df5-107">تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="26df5-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="26df5-108">انتقل إلى الحسابات المدينة > الأوامر > كافة أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="26df5-108">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="26df5-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="26df5-109">Click New.</span></span>
3. <span data-ttu-id="26df5-110">في الحقل "حساب العميل"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="26df5-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="26df5-111">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="26df5-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="26df5-112">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="26df5-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="26df5-113">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="26df5-113">Click OK.</span></span>
7. <span data-ttu-id="26df5-114">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="26df5-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="26df5-115">في الحقل "رقم الصنف"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="26df5-115">In the Item number field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="26df5-116">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="26df5-116">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="26df5-117">في حقل "سعر الوحدة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="26df5-117">In the Unit price field, enter a number.</span></span>
11. <span data-ttu-id="26df5-118">قم بتوسيع المقطع "تفاصيل البند" أو طيّه.</span><span class="sxs-lookup"><span data-stu-id="26df5-118">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="26df5-119">انقر فوق علامة التبويب "إعداد".</span><span class="sxs-lookup"><span data-stu-id="26df5-119">Click the Setup tab.</span></span>
13. <span data-ttu-id="26df5-120">في الحقل "مجموعة ضرائب المبيعات للأصناف‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="26df5-120">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="26df5-121">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="26df5-121">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="26df5-122">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="26df5-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="26df5-123">انقر فوق "الماليات‬".</span><span class="sxs-lookup"><span data-stu-id="26df5-123">Click Financials.</span></span>
17. <span data-ttu-id="26df5-124">انقر فوق "ضريبة المبيعات".</span><span class="sxs-lookup"><span data-stu-id="26df5-124">Click Sales tax.</span></span>
18. <span data-ttu-id="26df5-125">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="26df5-125">Click OK.</span></span>
19. <span data-ttu-id="26df5-126">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="26df5-126">Click Add line.</span></span>
20. <span data-ttu-id="26df5-127">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="26df5-127">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="26df5-128">في الحقل "رقم الصنف"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="26df5-128">In the Item number field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="26df5-129">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="26df5-129">In the list, find and select the desired record.</span></span>
23. <span data-ttu-id="26df5-130">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="26df5-130">In the list, click the link in the selected row.</span></span>
24. <span data-ttu-id="26df5-131">في حقل "سعر الوحدة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="26df5-131">In the Unit price field, enter a number.</span></span>
25. <span data-ttu-id="26df5-132">في الحقل "مجموعة ضرائب المبيعات للأصناف‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="26df5-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
26. <span data-ttu-id="26df5-133">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="26df5-133">In the list, find and select the desired record.</span></span>
27. <span data-ttu-id="26df5-134">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="26df5-134">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="26df5-135">في جزء الإجراءات، انقر فوق "بيع‬".</span><span class="sxs-lookup"><span data-stu-id="26df5-135">On the Action Pane, click Sell.</span></span>
29. <span data-ttu-id="26df5-136">انقر فوق "ضريبة المبيعات".</span><span class="sxs-lookup"><span data-stu-id="26df5-136">Click Sales tax.</span></span>
30. <span data-ttu-id="26df5-137">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="26df5-137">Click OK.</span></span>

