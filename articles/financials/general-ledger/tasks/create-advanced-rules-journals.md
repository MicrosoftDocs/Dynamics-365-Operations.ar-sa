--- 
title: "إنشاء قواعد متقدمة لدفاتر اليومية"
description: "يوضح هذا الإجراء إنشاء قواعد متقدمة لدفاتر اليومية."
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalSetup, LedgerJournalControl, CompanyLookup, LedgerJournalPostControl
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: e3fc764a6fa92a050084ae610a11acac46995d2a
ms.contentlocale: ar-sa
ms.lasthandoff: 09/14/2018

---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="f2bde-103">إنشاء قواعد متقدمة لدفاتر اليومية</span><span class="sxs-lookup"><span data-stu-id="f2bde-103">Create advanced rules for journals</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f2bde-104">يوضح هذا الإجراء إنشاء قواعد متقدمة لدفاتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="f2bde-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="f2bde-105">ويشمل هذا إعداد قيود التحكم في دفتر اليومية وترحيل المستخدم.</span><span class="sxs-lookup"><span data-stu-id="f2bde-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="f2bde-106">ويستخدم هذا الإجراء شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="f2bde-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="f2bde-107">إعداد التحكم في دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="f2bde-107">Set up journal control</span></span>
1. <span data-ttu-id="f2bde-108">انتقل إلى دفتر الأستاذ العام > إعداد دفتر اليومية > أسماء دفاتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="f2bde-108">Go to General ledger > Journal setup > Journal names.</span></span>
2. <span data-ttu-id="f2bde-109">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="f2bde-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f2bde-110">انقر فوق "التحكم في دفتر اليومية".</span><span class="sxs-lookup"><span data-stu-id="f2bde-110">Click Journal control.</span></span>
4. <span data-ttu-id="f2bde-111">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="f2bde-111">Click Add.</span></span>
5. <span data-ttu-id="f2bde-112">في الحقل "حسابات الشركة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f2bde-112">In the Company accounts field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="f2bde-113">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="f2bde-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="f2bde-114">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="f2bde-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="f2bde-115">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="f2bde-115">Click Add.</span></span>
9. <span data-ttu-id="f2bde-116">في الحقل "بنية الحساب"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f2bde-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="f2bde-117">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="f2bde-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="f2bde-118">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="f2bde-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="f2bde-119">في الحقل "المقطع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f2bde-119">In the Segment field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="f2bde-120">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="f2bde-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="f2bde-121">في الحقل "من القيمة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f2bde-121">In the From value field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="f2bde-122">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="f2bde-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="f2bde-123">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="f2bde-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="f2bde-124">في الحقل "إلى القيمة‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f2bde-124">In the To value field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="f2bde-125">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="f2bde-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="f2bde-126">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="f2bde-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="f2bde-127">إعداد قيود الترحيل</span><span class="sxs-lookup"><span data-stu-id="f2bde-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="f2bde-128">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f2bde-128">Close the page.</span></span>
2. <span data-ttu-id="f2bde-129">انقر فوق ‏‏قيود الترحيل.</span><span class="sxs-lookup"><span data-stu-id="f2bde-129">Click Posting restrictions.</span></span>
3. <span data-ttu-id="f2bde-130">في "الكيفية المطلوبة لإعداد قيود الترحيل"، حدد "حسب مجموعة المستخدمين".</span><span class="sxs-lookup"><span data-stu-id="f2bde-130">In the How do you want to set up posting restrictions, select By user group.</span></span>
4. <span data-ttu-id="f2bde-131">في الشجرة، قم بتحديد خانة الاختيار"المجموعة التي تريد السماح لها بالترحيل لاسم دفتر اليومية هذا."</span><span class="sxs-lookup"><span data-stu-id="f2bde-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="f2bde-132">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="f2bde-132">Click OK.</span></span>


