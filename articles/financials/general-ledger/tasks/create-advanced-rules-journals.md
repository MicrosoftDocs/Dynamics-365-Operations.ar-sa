---
title: إنشاء قواعد متقدمة لدفاتر اليومية
description: يوضح هذا الإجراء إنشاء قواعد متقدمة لدفاتر اليومية.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalControl, CompanyLookup, LedgerJournalPostControl
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e3fc764a6fa92a050084ae610a11acac46995d2a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "326160"
---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="1d3fd-103">إنشاء قواعد متقدمة لدفاتر اليومية</span><span class="sxs-lookup"><span data-stu-id="1d3fd-103">Create advanced rules for journals</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1d3fd-104">يوضح هذا الإجراء إنشاء قواعد متقدمة لدفاتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="1d3fd-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="1d3fd-105">ويشمل هذا إعداد قيود التحكم في دفتر اليومية وترحيل المستخدم.</span><span class="sxs-lookup"><span data-stu-id="1d3fd-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="1d3fd-106">ويستخدم هذا الإجراء شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="1d3fd-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="1d3fd-107">إعداد التحكم في دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="1d3fd-107">Set up journal control</span></span>
1. <span data-ttu-id="1d3fd-108">انتقل إلى دفتر الأستاذ العام > إعداد دفتر اليومية > أسماء دفاتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="1d3fd-108">Go to General ledger > Journal setup > Journal names.</span></span>
2. <span data-ttu-id="1d3fd-109">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="1d3fd-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="1d3fd-110">انقر فوق "التحكم في دفتر اليومية".</span><span class="sxs-lookup"><span data-stu-id="1d3fd-110">Click Journal control.</span></span>
4. <span data-ttu-id="1d3fd-111">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="1d3fd-111">Click Add.</span></span>
5. <span data-ttu-id="1d3fd-112">في الحقل "حسابات الشركة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="1d3fd-112">In the Company accounts field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="1d3fd-113">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="1d3fd-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="1d3fd-114">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="1d3fd-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="1d3fd-115">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="1d3fd-115">Click Add.</span></span>
9. <span data-ttu-id="1d3fd-116">في الحقل "بنية الحساب"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="1d3fd-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="1d3fd-117">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="1d3fd-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="1d3fd-118">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="1d3fd-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="1d3fd-119">في الحقل "المقطع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="1d3fd-119">In the Segment field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="1d3fd-120">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="1d3fd-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="1d3fd-121">في الحقل "من القيمة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="1d3fd-121">In the From value field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="1d3fd-122">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="1d3fd-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="1d3fd-123">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="1d3fd-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="1d3fd-124">في الحقل "إلى القيمة‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="1d3fd-124">In the To value field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="1d3fd-125">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="1d3fd-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="1d3fd-126">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="1d3fd-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="1d3fd-127">إعداد قيود الترحيل</span><span class="sxs-lookup"><span data-stu-id="1d3fd-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="1d3fd-128">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1d3fd-128">Close the page.</span></span>
2. <span data-ttu-id="1d3fd-129">انقر فوق ‏‏قيود الترحيل.</span><span class="sxs-lookup"><span data-stu-id="1d3fd-129">Click Posting restrictions.</span></span>
3. <span data-ttu-id="1d3fd-130">في "الكيفية المطلوبة لإعداد قيود الترحيل"، حدد "حسب مجموعة المستخدمين".</span><span class="sxs-lookup"><span data-stu-id="1d3fd-130">In the How do you want to set up posting restrictions, select By user group.</span></span>
4. <span data-ttu-id="1d3fd-131">في الشجرة، قم بتحديد خانة الاختيار"المجموعة التي تريد السماح لها بالترحيل لاسم دفتر اليومية هذا."</span><span class="sxs-lookup"><span data-stu-id="1d3fd-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="1d3fd-132">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="1d3fd-132">Click OK.</span></span>

