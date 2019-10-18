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
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186131"
---
# <a name="create-sales-tax-transactions-on-documents"></a><span data-ttu-id="d10da-103">إنشاء حركات ضريبة المبيعات في المستندات</span><span class="sxs-lookup"><span data-stu-id="d10da-103">Create sales tax transactions on documents</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d10da-104">يتم حساب ضريبة المبيعات على المستندات عن طريق توفير مجموعة ضريبة المبيعات ومجموعة ضرائب المبيعات للأصناف‬ على بنود المستند.</span><span class="sxs-lookup"><span data-stu-id="d10da-104">Sales tax on documents is calculated by providing a Sales tax group and an Item sales tax group on document lines.</span></span> <span data-ttu-id="d10da-105">وهذه تأتي بشكل افتراضي من البيانات الرئيسية، ولكن يمكن تغييرها يدويًا إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="d10da-105">These default from master data but can be changed manually if necessary.</span></span> <span data-ttu-id="d10da-106">يمكن التحقق من ضريبة المبيعات المحسوبة على مستوى البند والمستند.</span><span class="sxs-lookup"><span data-stu-id="d10da-106">The calculated sales tax can be checked on a line and document level.</span></span> <span data-ttu-id="d10da-107">تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="d10da-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="d10da-108">انتقل إلى الحسابات المدينة > الأوامر > كافة أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="d10da-108">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="d10da-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="d10da-109">Click New.</span></span>
3. <span data-ttu-id="d10da-110">في الحقل "حساب العميل"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="d10da-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="d10da-111">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="d10da-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="d10da-112">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d10da-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="d10da-113">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="d10da-113">Click OK.</span></span>
7. <span data-ttu-id="d10da-114">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d10da-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="d10da-115">في الحقل "رقم الصنف"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="d10da-115">In the Item number field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="d10da-116">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d10da-116">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="d10da-117">في حقل "سعر الوحدة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="d10da-117">In the Unit price field, enter a number.</span></span>
11. <span data-ttu-id="d10da-118">قم بتوسيع المقطع "تفاصيل البند" أو طيّه.</span><span class="sxs-lookup"><span data-stu-id="d10da-118">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="d10da-119">انقر فوق علامة التبويب "إعداد".</span><span class="sxs-lookup"><span data-stu-id="d10da-119">Click the Setup tab.</span></span>
13. <span data-ttu-id="d10da-120">في الحقل "مجموعة ضرائب المبيعات للأصناف‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="d10da-120">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="d10da-121">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="d10da-121">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="d10da-122">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d10da-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="d10da-123">انقر فوق "الماليات‬".</span><span class="sxs-lookup"><span data-stu-id="d10da-123">Click Financials.</span></span>
17. <span data-ttu-id="d10da-124">انقر فوق "ضريبة المبيعات".</span><span class="sxs-lookup"><span data-stu-id="d10da-124">Click Sales tax.</span></span>
18. <span data-ttu-id="d10da-125">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d10da-125">Click OK.</span></span>
19. <span data-ttu-id="d10da-126">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="d10da-126">Click Add line.</span></span>
20. <span data-ttu-id="d10da-127">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d10da-127">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="d10da-128">في الحقل "رقم الصنف"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="d10da-128">In the Item number field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="d10da-129">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="d10da-129">In the list, find and select the desired record.</span></span>
23. <span data-ttu-id="d10da-130">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d10da-130">In the list, click the link in the selected row.</span></span>
24. <span data-ttu-id="d10da-131">في حقل "سعر الوحدة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="d10da-131">In the Unit price field, enter a number.</span></span>
25. <span data-ttu-id="d10da-132">في الحقل "مجموعة ضرائب المبيعات للأصناف‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="d10da-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
26. <span data-ttu-id="d10da-133">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="d10da-133">In the list, find and select the desired record.</span></span>
27. <span data-ttu-id="d10da-134">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d10da-134">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="d10da-135">في جزء الإجراءات، انقر فوق "بيع‬".</span><span class="sxs-lookup"><span data-stu-id="d10da-135">On the Action Pane, click Sell.</span></span>
29. <span data-ttu-id="d10da-136">انقر فوق "ضريبة المبيعات".</span><span class="sxs-lookup"><span data-stu-id="d10da-136">Click Sales tax.</span></span>
30. <span data-ttu-id="d10da-137">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d10da-137">Click OK.</span></span>

