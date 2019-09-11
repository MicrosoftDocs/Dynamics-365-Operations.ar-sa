---
title: إقفال شامل للفترة المالية
description: يظهر هذا الموضوع كيفية وضع فترة قيد الاحتجاز أو إقفال فترة بشكل دائم على أكثر من كيان قانوني واحد في المرة الواحدة.
author: aprilolson
manager: AnnBe
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 398a62e575010501291af3016553fc72fbc891de
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914620"
---
# <a name="mass-financial-period-close"></a><span data-ttu-id="e6c7d-103">إقفال شامل للفترة المالية</span><span class="sxs-lookup"><span data-stu-id="e6c7d-103">Mass financial period close</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e6c7d-104">يظهر هذا الموضوع كيفية وضع فترة قيد الاحتجاز أو إقفال فترة بشكل دائم على أكثر من كيان قانوني واحد في المرة الواحدة.</span><span class="sxs-lookup"><span data-stu-id="e6c7d-104">This topic shows how to place a period on hold or permanently close a period or more than one legal entity at a time.</span></span> <span data-ttu-id="e6c7d-105">وبالإضافة إلى ذلك، سوف تظهر المهمة كيفية تقييد الترحيل لمجموعة مستخدمين إلى وحدات نمطية معينة.</span><span class="sxs-lookup"><span data-stu-id="e6c7d-105">In addition, the task will show how to restrict user group posting to specific modules.</span></span>

1. <span data-ttu-id="e6c7d-106">في جزء التنقل، انتقل إلى **الوحدات النمطية > دفتر الأستاذ العام > إقفال الفترة‬ > تقويمات دفتر الأستاذ‬**.</span><span class="sxs-lookup"><span data-stu-id="e6c7d-106">In the navigation pane, go to **Modules > General ledger > Period close > Ledger calendars**.</span></span> <span data-ttu-id="e6c7d-107">لاحظ أن قائمة الكيانات القانونية المعروضة تعتمد على التقويم المالي المحدد في الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e6c7d-107">Note that the list of legal entities displayed is dependent on the fiscal calendar selected on the page.</span></span> <span data-ttu-id="e6c7d-108">ستظهر فقط الكيانات القانونية التي تستخدم التقويم المالي المحدد.</span><span class="sxs-lookup"><span data-stu-id="e6c7d-108">Only legal entities using the selected fiscal calendar will display.</span></span>
2. <span data-ttu-id="e6c7d-109">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="e6c7d-109">Select **Edit**.</span></span>
3. <span data-ttu-id="e6c7d-110">حدد الفترة التي تريد تعديل حالتها.</span><span class="sxs-lookup"><span data-stu-id="e6c7d-110">Select the period for which you want to modify the status.</span></span>
4. <span data-ttu-id="e6c7d-111">حدد الكيانات القانونية التي تريد تحديث حالتها.</span><span class="sxs-lookup"><span data-stu-id="e6c7d-111">Select the legal entities for which you want to update the status.</span></span> <span data-ttu-id="e6c7d-112">يمكنك تحديد كافة الكيانات القانونية بسرعة عن طريق تحديد علامة الاختيار في الجانب العلوي الأيمن من الشبكة.</span><span class="sxs-lookup"><span data-stu-id="e6c7d-112">You can quickly select all legal entities by selecting the check mark on the upper left side of the grid.</span></span>  
5. <span data-ttu-id="e6c7d-113">حدد **تحديث الوصول للوحدة النمطية** لتعريف وصول الترحيل إلى وحدة نمطية محددة.</span><span class="sxs-lookup"><span data-stu-id="e6c7d-113">Select **Update module access** to define the posting access to a selected module.</span></span> <span data-ttu-id="e6c7d-114">يمكن أيضًا تحديث حالة الوحدة النمطية الواحدة تلو الأخرى عن طريق تحرير السجلات الموجودة في الشبكة.</span><span class="sxs-lookup"><span data-stu-id="e6c7d-114">The module status can also be updated one-by-one by editing the records in the grid.</span></span> <span data-ttu-id="e6c7d-115">يُعتبر الزر مفيدًا عندما تريد تحديث سجلات كيانات قانونية متعددة بسرعة.</span><span class="sxs-lookup"><span data-stu-id="e6c7d-115">The button is useful when you want to quickly update multiple legal entity records.</span></span>  
6. <span data-ttu-id="e6c7d-116">في الوحدة النمطية **التطبيق**، حدد الوحدة النمطية التي ترغب في تحديث حالتها.</span><span class="sxs-lookup"><span data-stu-id="e6c7d-116">In the **Application** module, select the module that you want to update the status.</span></span> <span data-ttu-id="e6c7d-117">انقر فوق **تحديد**.</span><span class="sxs-lookup"><span data-stu-id="e6c7d-117">Click **Select**.</span></span>
7. <span data-ttu-id="e6c7d-118">في "مستوى **الوصول**، حدد **الكل** أو **بلا** أو مجموعة مستخدمين محددة.</span><span class="sxs-lookup"><span data-stu-id="e6c7d-118">In the **Access** level, select **All**, **None**, or a specific user group.</span></span> <span data-ttu-id="e6c7d-119">انقر فوق **تحديد**.</span><span class="sxs-lookup"><span data-stu-id="e6c7d-119">Click **Select**.</span></span> <span data-ttu-id="e6c7d-120">تشير "الكل" إلى أن جميع المستخدمين الذين يحق لهم الوصول إلى الوحدة النمطية يمكنهم الترحيل إذا كانت الفترة مفتوحة.</span><span class="sxs-lookup"><span data-stu-id="e6c7d-120">All indicates all users with edit access to the module can post if the period is open.</span></span> <span data-ttu-id="e6c7d-121">يشير الخيار "بلا" إلى أنه يتعذر على المستخدمين الترحيل إلى الوحدة النمطية إذا كانت الفترة مفتوحة.</span><span class="sxs-lookup"><span data-stu-id="e6c7d-121">None indicates that users cannot post to the module if the period is open.</span></span> <span data-ttu-id="e6c7d-122">تشير "مجموعة مستخدمين محددة" إلى أنه يستطيع المستخدمون في المجموعة فقط الترحيل إلى الوحدة النمطية إذا كانت الفترة مفتوحة.</span><span class="sxs-lookup"><span data-stu-id="e6c7d-122">A specific user group indicates only users in the group are able to post to the module if the period is open.</span></span>  
8. <span data-ttu-id="e6c7d-123">حدد **تحديث**.</span><span class="sxs-lookup"><span data-stu-id="e6c7d-123">Select **Update**.</span></span>
9. <span data-ttu-id="e6c7d-124">حدد فترة أخرى لتحديث الحالة.</span><span class="sxs-lookup"><span data-stu-id="e6c7d-124">Select another period to update the status.</span></span>
10. <span data-ttu-id="e6c7d-125">حدد الكيانات القانونية التي تريد تحديث حالة الفترة لها.</span><span class="sxs-lookup"><span data-stu-id="e6c7d-125">Select the legal entites for which you want to update the period status.</span></span>
11. <span data-ttu-id="e6c7d-126">حدد **تحديث حالة الفترة‬**، وعيّن الحالة إلى **قيد الانتظار** أو **مفتوح‬** أو **تم الإقفال بشكل دائم**.</span><span class="sxs-lookup"><span data-stu-id="e6c7d-126">Select **Update period status** and set the status of **On hold**, **Open**, or **Permanently closed**.</span></span> <span data-ttu-id="e6c7d-127">تشير الحالة**مفتوح** إلى أنه يمكن الترحيل إلى الفترة، بشرط توفر الوصول للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="e6c7d-127">**Open** indicates the period can be posted to, provided the user has access.</span></span> <span data-ttu-id="e6c7d-128">تشير الحالة **قيد الانتظار** إلى أنه يتعذر الترحيل إلى الفترة، ولكن يمكن إعادة فتح الفترة.</span><span class="sxs-lookup"><span data-stu-id="e6c7d-128">**On hold** means the period cannot be posted to, but the period can be reopened.</span></span> <span data-ttu-id="e6c7d-129">تشير الحالة **تم الإقفال بشكل دائم** أن الفترة مقفلة ولا يمكن إعادة فتحها إطلاقًا.</span><span class="sxs-lookup"><span data-stu-id="e6c7d-129">**Permanently closed** means the period is closed and can never be opened.</span></span> <span data-ttu-id="e6c7d-130">لا يمكن ترحيل التسويات.</span><span class="sxs-lookup"><span data-stu-id="e6c7d-130">Adjustments cannot be posted.</span></span> <span data-ttu-id="e6c7d-131">لا يوصَى بتعيين فترة إلى **تم الإقفال بشكل دائم‬** إلا عند اكتمال جميع التسويات والمراجعات.</span><span class="sxs-lookup"><span data-stu-id="e6c7d-131">We do not recommend setting a period to **Permanently closed** until all adjustments and audits are complete.</span></span>  
12. <span data-ttu-id="e6c7d-132">حدد **تحديث**.</span><span class="sxs-lookup"><span data-stu-id="e6c7d-132">Select **Update**.</span></span>

