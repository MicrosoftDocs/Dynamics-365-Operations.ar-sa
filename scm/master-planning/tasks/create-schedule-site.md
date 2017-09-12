--- 
title: "إنشاء جدول ما لموقع"
description: "يوضح هذا الإجراء كيفية جدولة أوامر الإنتاج التي لم تبدأ بعد لموقع ما."
author: YuyuScheller
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 775428bf84a752c03c492e764fa9ed576ab64fb8
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-schedule-for-a-site"></a><span data-ttu-id="c67ab-103">إنشاء جدول ما لموقع</span><span class="sxs-lookup"><span data-stu-id="c67ab-103">Create a schedule for a site</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c67ab-104">يوضح هذا الإجراء كيفية جدولة أوامر الإنتاج التي لم تبدأ بعد لموقع ما.</span><span class="sxs-lookup"><span data-stu-id="c67ab-104">This procedure shows how to schedule production orders that are not yet started for a site.</span></span>  <span data-ttu-id="c67ab-105">يتم استخدام شركة بيانات العرض التوضيحي USMF لإكمال هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="c67ab-105">The demo data company USMF is used to complete this procedure.</span></span>


## <a name="identify-production-orders-that-are-not-started"></a><span data-ttu-id="c67ab-106">تحديد أوامر الإنتاج غير المبدوءة</span><span class="sxs-lookup"><span data-stu-id="c67ab-106">Identify production orders that are not started</span></span>
1. <span data-ttu-id="c67ab-107">انتقل إلى التحكم بالإنتاج‬ > أوامر الإنتاج > كافة أوامر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="c67ab-107">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="c67ab-108">استخدم عامل التصفية السريع للبحث عن السجلات.</span><span class="sxs-lookup"><span data-stu-id="c67ab-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="c67ab-109">على سبيل المثال، قم بإجراء التصفية على حقل الموقع بقيمة "1".</span><span class="sxs-lookup"><span data-stu-id="c67ab-109">For example, filter on the Site field with a value of '1'.</span></span>
    * <span data-ttu-id="c67ab-110">1 يمثل موقعًا في USMF.</span><span class="sxs-lookup"><span data-stu-id="c67ab-110">1 represents a site in USMF.</span></span> <span data-ttu-id="c67ab-111">إذا كنت لا تستخدم USMF، حدد موقعًا من الشركة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="c67ab-111">If you are not using USMF, select a site from your own company.</span></span>  
3. <span data-ttu-id="c67ab-112">افتح عامل تصفية عمود الحالة.</span><span class="sxs-lookup"><span data-stu-id="c67ab-112">Open the Status column filter.</span></span>
4. <span data-ttu-id="c67ab-113">استخدم عامل تصفية على حقل "الحالة" بقيمة "مجدول"، باستخدام مشغل عامل تصفية "تمامًا مثل".</span><span class="sxs-lookup"><span data-stu-id="c67ab-113">Apply a filter on the "Status" field, with a value of "Scheduled", using the "is exactly" filter operator.</span></span>

## <a name="create-a-schedule"></a><span data-ttu-id="c67ab-114">إنشاء جدول</span><span class="sxs-lookup"><span data-stu-id="c67ab-114">Create a schedule</span></span>
1. <span data-ttu-id="c67ab-115">في القائمة، قم بوضع علامة أو إلغاء علامة كل الصفوف.</span><span class="sxs-lookup"><span data-stu-id="c67ab-115">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="c67ab-116">في جزء الإجراءات، انقر فوق "جدول".</span><span class="sxs-lookup"><span data-stu-id="c67ab-116">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="c67ab-117">انقر فوق "جدولة الوظائف".</span><span class="sxs-lookup"><span data-stu-id="c67ab-117">Click Schedule jobs.</span></span>
4. <span data-ttu-id="c67ab-118">في الحقل "اتجاه الجدولة"، حدد "العودة للخلف اعتبارًا من تاريخ التسليم".</span><span class="sxs-lookup"><span data-stu-id="c67ab-118">In the Scheduling direction field, select 'Backward from delivery date'.</span></span>
5. <span data-ttu-id="c67ab-119">حدد "لا" في حقل "القدرة المحدودة‬".</span><span class="sxs-lookup"><span data-stu-id="c67ab-119">Select No in the Finite capacity field.</span></span>
6. <span data-ttu-id="c67ab-120">حدد "لا" في حقل "المواد المحدودة‬".</span><span class="sxs-lookup"><span data-stu-id="c67ab-120">Select No in the Finite material field.</span></span>
7. <span data-ttu-id="c67ab-121">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c67ab-121">Click OK.</span></span>
    * <span data-ttu-id="c67ab-122">قد يستغرق هذا الأمر بعض الوقت.</span><span class="sxs-lookup"><span data-stu-id="c67ab-122">This may take a while.</span></span>  

## <a name="view-the-result-of-scheduled-production-orders"></a><span data-ttu-id="c67ab-123">عرض نتائج أوامر الإنتاج المجدولة</span><span class="sxs-lookup"><span data-stu-id="c67ab-123">View the result of scheduled production orders</span></span>
1. <span data-ttu-id="c67ab-124">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c67ab-124">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="c67ab-125">يمكنك وضع علامة على أي صف.</span><span class="sxs-lookup"><span data-stu-id="c67ab-125">You can mark any row.</span></span>  
2. <span data-ttu-id="c67ab-126">في جزء "الإجراءات"، انقر فوق "أمر إنتاج".</span><span class="sxs-lookup"><span data-stu-id="c67ab-126">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="c67ab-127">انقر فوق كافة الوظائف.</span><span class="sxs-lookup"><span data-stu-id="c67ab-127">Click All jobs.</span></span>
    * <span data-ttu-id="c67ab-128">في هذه الصفحة، يمكنك رؤية قائمة المهام.</span><span class="sxs-lookup"><span data-stu-id="c67ab-128">On this page, you can see the list of jobs.</span></span> <span data-ttu-id="c67ab-129">من علامة التبويب "جدولة"، يمكنك رؤية تاريخ البدء وتاريخ الانتهاء لمهمة ما.</span><span class="sxs-lookup"><span data-stu-id="c67ab-129">On the Scheduling tab, you can see the Start date and End date for a job.</span></span>  
4. <span data-ttu-id="c67ab-130">انقر فوق المواد.</span><span class="sxs-lookup"><span data-stu-id="c67ab-130">Click Materials.</span></span>
    * <span data-ttu-id="c67ab-131">في هذه الصفحة، يمكنك رؤية استهلاك المواد المقدر للعمليات على أمر الإنتاج والمخزون المتاح الحالي.</span><span class="sxs-lookup"><span data-stu-id="c67ab-131">On this page, you can see the estimated material consumption for the operations on the production order and the current available inventory.</span></span>  


