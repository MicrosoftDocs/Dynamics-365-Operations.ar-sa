---
title: إقفال شامل للفترة المالية
description: يظهر هذا الإجراء كيفية وضع فترة قيد الاحتجاز أو إقفال فترة بشكل دائم على أكثر من كيان قانوني واحد في مرة الواحدة.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2988b7ab0837cc9a3e4f1c4eaf3fe6e219fa721
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "311371"
---
# <a name="mass-financial-period-close"></a><span data-ttu-id="35059-103">إقفال شامل للفترة المالية</span><span class="sxs-lookup"><span data-stu-id="35059-103">Mass financial period close</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="35059-104">يظهر هذا الإجراء كيفية وضع فترة قيد الاحتجاز أو إقفال فترة بشكل دائم على أكثر من كيان قانوني واحد في مرة الواحدة.</span><span class="sxs-lookup"><span data-stu-id="35059-104">This procedure shows how to place a period on hold or permanently close a period or more than one legal entity at a time.</span></span> <span data-ttu-id="35059-105">وبالإضافة إلى ذلك، سوف تظهر المهمة كيفية تقييد الترحيل لمجموعة مستخدمين إلى وحدات نمطية معينة.</span><span class="sxs-lookup"><span data-stu-id="35059-105">In addition, the task will show how to restrict user group posting to specific modules.</span></span>

1. <span data-ttu-id="35059-106">انتقل إلى دفتر الأستاذ العام > إقفال الفترة > تقويمات دفتر الأستاذ‬.</span><span class="sxs-lookup"><span data-stu-id="35059-106">Go to General ledger > Period close > Ledger calendars.</span></span>
    * <span data-ttu-id="35059-107">لاحظ أن قائمة الكيانات القانونية المعروضة تعتمد على التقويم المالي المحدد في الصفحة.</span><span class="sxs-lookup"><span data-stu-id="35059-107">Note that the list of legal entities displayed is dependent on the fiscal calendar selected on the page.</span></span> <span data-ttu-id="35059-108">ستظهر فقط الكيانات القانونية التي تستخدم التقويم المالي المحدد.</span><span class="sxs-lookup"><span data-stu-id="35059-108">Only legal entities using the selected fiscal calendar will display.</span></span>  
2. <span data-ttu-id="35059-109">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="35059-109">Click Edit.</span></span>
3. <span data-ttu-id="35059-110">حدد الفترة التي تريد تعديل حالتها.</span><span class="sxs-lookup"><span data-stu-id="35059-110">Select the period for which you want to modify the status.</span></span>
4. <span data-ttu-id="35059-111">حدد الكيانات القانونية التي تريد تحديث حالتها.</span><span class="sxs-lookup"><span data-stu-id="35059-111">Select the legal entities for which you want to update the status.</span></span>
    * <span data-ttu-id="35059-112">يمكنك تحديد كافة الكيانات القانونية بسرعة عن طريق تحديد علامة الاختيار في الجانب العلوي الأيمن من الشبكة.</span><span class="sxs-lookup"><span data-stu-id="35059-112">You can quickly select all legal entities  by selecting the check mark on the upper left side of the grid.</span></span>  
5. <span data-ttu-id="35059-113">حدد "تحديث الوصول للوحدة النمطية‬" لتعريف وصول الترحيل إلى وحدة نمطية محددة.</span><span class="sxs-lookup"><span data-stu-id="35059-113">Select Update module access to define the posting access to a selected module.</span></span>
    * <span data-ttu-id="35059-114">يمكن أيضًا تحديث حالة الوحدة النمطية الواحدة تلو الأخرى عن طريق تحرير السجلات الموجودة في الشبكة.</span><span class="sxs-lookup"><span data-stu-id="35059-114">The module status can also be updated one-by-one by editing the records in the grid.</span></span> <span data-ttu-id="35059-115">يُعتبر الزر مفيدًا عندما تريد تحديث سجلات كيانات قانونية متعددة بسرعة.</span><span class="sxs-lookup"><span data-stu-id="35059-115">The button is useful when you want to quickly update multiple legal entity records.</span></span>  
6. <span data-ttu-id="35059-116">في "الوحدة النمطية للتطبيق"، حدد الوحدة النمطية التي ترغب في تحديث حالتها.</span><span class="sxs-lookup"><span data-stu-id="35059-116">In the Application module, select the module that you want to update the status.</span></span> <span data-ttu-id="35059-117">انقر فوق تحديد.</span><span class="sxs-lookup"><span data-stu-id="35059-117">Click Select.</span></span>
7. <span data-ttu-id="35059-118">في "مستوى الوصول"، حدد "الكل" أو "بلا" أو مجموعة مستخدمين محددة.</span><span class="sxs-lookup"><span data-stu-id="35059-118">In the Access level, select All, None, or a specific user group.</span></span> <span data-ttu-id="35059-119">انقر فوق تحديد.</span><span class="sxs-lookup"><span data-stu-id="35059-119">Click Select.</span></span>
    * <span data-ttu-id="35059-120">تشير "الكل" إلى أن جميع المستخدمين الذين يحق لهم الوصول إلى الوحدة النمطية يمكنهم الترحيل إذا كانت الفترة مفتوحة.</span><span class="sxs-lookup"><span data-stu-id="35059-120">All indicates all users with edit access to the module can post if the period is open.</span></span> <span data-ttu-id="35059-121">يشير الخيار "بلا" إلى أنه يتعذر على المستخدمين الترحيل إلى الوحدة النمطية إذا كانت الفترة مفتوحة.</span><span class="sxs-lookup"><span data-stu-id="35059-121">None indicates that users cannot post to the module if the period is open.</span></span> <span data-ttu-id="35059-122">تشير "مجموعة مستخدمين محددة" إلى أنه يستطيع المستخدمون في المجموعة فقط الترحيل إلى الوحدة النمطية إذا كانت الفترة مفتوحة.</span><span class="sxs-lookup"><span data-stu-id="35059-122">A specific user group indicates only users in the group are able to post to the module if the period is open.</span></span>  
8. <span data-ttu-id="35059-123">انقر فوق تحديث.</span><span class="sxs-lookup"><span data-stu-id="35059-123">Click Update.</span></span>
9. <span data-ttu-id="35059-124">حدد فترة أخرى لتحديث الحالة.</span><span class="sxs-lookup"><span data-stu-id="35059-124">Select another period to update the status.</span></span>
10. <span data-ttu-id="35059-125">حدد الكيانات القانونية التي تريد تحديث حالة الفترة لها.</span><span class="sxs-lookup"><span data-stu-id="35059-125">Select the legal entites for which you want to update the period status.</span></span>
11. <span data-ttu-id="35059-126">حدد "‏‫تحديث حالة الفترة‬"، وعيّن الحالة إلى "قيد الانتظار" أو "مفتوح‬" أو "تم الإقفال بشكل دائم‬".</span><span class="sxs-lookup"><span data-stu-id="35059-126">Select Update period status and set the status of On hold, Open, or Permanently closed.</span></span>
    * <span data-ttu-id="35059-127">تشر "مفتوحة" إلى أنه يمكن الترحيل إلى الفترة، بشرط توفر الوصول للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="35059-127">Open indicates the period can be posted to, provided the user has access.</span></span> <span data-ttu-id="35059-128">يعني الخيار "قيد الانتظار" إلى أنه يتعذر الترحيل إلى الفترة، ولكن يمكن إعادة فتح الفترة.</span><span class="sxs-lookup"><span data-stu-id="35059-128">On hold means the period cannot be posted to, but the period can be reopened.</span></span> <span data-ttu-id="35059-129">يعني الخيار "تم الإقفال بشكل دائم" أن الفترة مقفلة ولا يمكن إعادة فتحها إطلاقًا.</span><span class="sxs-lookup"><span data-stu-id="35059-129">Permanently closed means the period is closed and can never be opened.</span></span> <span data-ttu-id="35059-130">لا يمكن ترحيل التسويات.</span><span class="sxs-lookup"><span data-stu-id="35059-130">Adjustments cannot be posted.</span></span> <span data-ttu-id="35059-131">لا يوصَى بتعيين فترة إلى "تم الإقفال بشكل دائم‬" إلا عند اكتمال جميع التسويات والمراجعات.</span><span class="sxs-lookup"><span data-stu-id="35059-131">We do not recommend setting a period to Permanently closed until all adjustments and audits are complete.</span></span>  
12. <span data-ttu-id="35059-132">انقر فوق تحديث.</span><span class="sxs-lookup"><span data-stu-id="35059-132">Click Update.</span></span>

