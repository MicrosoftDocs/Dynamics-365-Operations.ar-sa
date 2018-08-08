---
title: "جدولة أمر إنتاج"
description: "يوضح هذا الإجراء كيفية جدولة أمر إنتاج."
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: ed1d4f58acb5cfb46d1ec524bd2b7d252f6dde1d
ms.contentlocale: ar-sa
ms.lasthandoff: 08/07/2018

---
# <a name="schedule-a-production-order"></a><span data-ttu-id="9d2c9-103">جدولة أمر إنتاج</span><span class="sxs-lookup"><span data-stu-id="9d2c9-103">Schedule a production order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9d2c9-104">يوضح هذا الإجراء كيفية جدولة أمر إنتاج.</span><span class="sxs-lookup"><span data-stu-id="9d2c9-104">This procedure shows how to schedule a production order.</span></span> <span data-ttu-id="9d2c9-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="9d2c9-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="9d2c9-106">هذا هو الإجراء الثالث من أصل سبعة إجراءات الذي يشرح دورة حياة أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="9d2c9-106">This is the third procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="schedule-a-production-order"></a><span data-ttu-id="9d2c9-107">جدولة أمر إنتاج</span><span class="sxs-lookup"><span data-stu-id="9d2c9-107">Schedule a production order</span></span>
1. <span data-ttu-id="9d2c9-108">انتقل إلى التحكم بالإنتاج‬ > أوامر الإنتاج > كافة أوامر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="9d2c9-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="9d2c9-109">حدد أمر إنتاج يكون له "الحالة المقدرة".</span><span class="sxs-lookup"><span data-stu-id="9d2c9-109">Select a production order that has the Estimated status.</span></span>  
2. <span data-ttu-id="9d2c9-110">في جزء الإجراءات، انقر فوق "جدول".</span><span class="sxs-lookup"><span data-stu-id="9d2c9-110">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="9d2c9-111">انقر فوق "جدولة الوظائف".</span><span class="sxs-lookup"><span data-stu-id="9d2c9-111">Click Schedule jobs.</span></span>
    * <span data-ttu-id="9d2c9-112">تم تعيين المعلمات للجدولة على هذه الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9d2c9-112">The parameters for scheduling are set up on this page.</span></span> <span data-ttu-id="9d2c9-113">يمكنك إعداد المعلمات لمستخدمين محددين أو لكافة المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="9d2c9-113">You can set up the parameters for specific users or all users.</span></span>  
4. <span data-ttu-id="9d2c9-114">في حقل "اتجاه الجدولة"، حدد "‏‫مستقبلي من اليوم‬".</span><span class="sxs-lookup"><span data-stu-id="9d2c9-114">In the Scheduling direction field, select 'Forward from today'.</span></span>
5. <span data-ttu-id="9d2c9-115">في حقل "تاريخ الجدولة"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="9d2c9-115">In the Scheduling date field, enter a date.</span></span>
6. <span data-ttu-id="9d2c9-116">حدد خانة الاختيار "‏‫قدرة محدودة" أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="9d2c9-116">Select or clear the Finite capacity check box.</span></span>
7. <span data-ttu-id="9d2c9-117">حدد خانة الاختيار "‏‫مواد محدودة" أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="9d2c9-117">Select or clear the Finite material check box.</span></span>
8. <span data-ttu-id="9d2c9-118">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="9d2c9-118">Click OK.</span></span>

## <a name="view-the-scheduling-results"></a><span data-ttu-id="9d2c9-119">عرض نتائج الجدولة</span><span class="sxs-lookup"><span data-stu-id="9d2c9-119">View the scheduling results</span></span>
1. <span data-ttu-id="9d2c9-120">في جزء "الإجراءات"، انقر فوق "أمر إنتاج".</span><span class="sxs-lookup"><span data-stu-id="9d2c9-120">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="9d2c9-121">انقر فوق كافة الوظائف.</span><span class="sxs-lookup"><span data-stu-id="9d2c9-121">Click All jobs.</span></span>
    * <span data-ttu-id="9d2c9-122">تعرض هذه الصفحة الوظائف المجدولة التي قمت بإنشائها للتو.</span><span class="sxs-lookup"><span data-stu-id="9d2c9-122">This page displays the scheduled jobs that you have just generated.</span></span>  
3. <span data-ttu-id="9d2c9-123">قم بتوسيع قسم "الجدولة" أو طيه.</span><span class="sxs-lookup"><span data-stu-id="9d2c9-123">Expand or collapse the Scheduling section.</span></span>
    * <span data-ttu-id="9d2c9-124">في علامة التبويب السريعة "الجدولة"، يمكنك عرض الوقت والتاريخ المجدولين.</span><span class="sxs-lookup"><span data-stu-id="9d2c9-124">On the Scheduling FastTab, you can view the scheduled date and time.</span></span>  
4. <span data-ttu-id="9d2c9-125">انقر فوق "استعلامات".</span><span class="sxs-lookup"><span data-stu-id="9d2c9-125">Click Inquiries.</span></span>
5. <span data-ttu-id="9d2c9-126">انقر فوق القدرة الإنتاجية.</span><span class="sxs-lookup"><span data-stu-id="9d2c9-126">Click Capacity load.</span></span>
    * <span data-ttu-id="9d2c9-127">تعرض صفحة القدرة الإنتاجية القدرة المخزنة من خلال جدولة الوظائف والعدد الإجمالي للساعات المحجوزة حاليًا للمورد وعدد الساعات التي لا تزال متاحة لجدولة وظيفة للمورد.</span><span class="sxs-lookup"><span data-stu-id="9d2c9-127">The Capacity load page displays the capacity that is reserved through job scheduling, the total number of hours that are currently reserved on the resource, and the number of hours that remain available for job scheduling on the resource.</span></span>  
6. <span data-ttu-id="9d2c9-128">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9d2c9-128">Close the page.</span></span>
7. <span data-ttu-id="9d2c9-129">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9d2c9-129">Close the page.</span></span>

