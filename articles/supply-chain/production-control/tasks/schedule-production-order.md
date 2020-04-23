---
title: جدولة أمر إنتاج
description: يوضح هذا الإجراء كيفية جدولة أمر إنتاج.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob, WrkCtrCapResSum
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: daaf7a593f8ae5185333c33b9e475dfd62358eb8
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210423"
---
# <a name="schedule-a-production-order"></a><span data-ttu-id="de65e-103">جدولة أمر إنتاج</span><span class="sxs-lookup"><span data-stu-id="de65e-103">Schedule a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="de65e-104">يوضح هذا الإجراء كيفية جدولة أمر إنتاج.</span><span class="sxs-lookup"><span data-stu-id="de65e-104">This procedure shows how to schedule a production order.</span></span> <span data-ttu-id="de65e-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="de65e-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="de65e-106">هذا هو الإجراء الثالث من أصل سبعة إجراءات الذي يشرح دورة حياة أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="de65e-106">This is the third procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="schedule-a-production-order"></a><span data-ttu-id="de65e-107">جدولة أمر إنتاج</span><span class="sxs-lookup"><span data-stu-id="de65e-107">Schedule a production order</span></span>
1. <span data-ttu-id="de65e-108">انتقل إلى التحكم بالإنتاج‬ > أوامر الإنتاج > كافة أوامر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="de65e-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="de65e-109">حدد أمر إنتاج يكون له "الحالة المقدرة".</span><span class="sxs-lookup"><span data-stu-id="de65e-109">Select a production order that has the Estimated status.</span></span>  
2. <span data-ttu-id="de65e-110">في جزء الإجراءات، انقر فوق "جدول".</span><span class="sxs-lookup"><span data-stu-id="de65e-110">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="de65e-111">انقر فوق "جدولة الوظائف".</span><span class="sxs-lookup"><span data-stu-id="de65e-111">Click Schedule jobs.</span></span>
    * <span data-ttu-id="de65e-112">تم تعيين المعلمات للجدولة على هذه الصفحة.</span><span class="sxs-lookup"><span data-stu-id="de65e-112">The parameters for scheduling are set up on this page.</span></span> <span data-ttu-id="de65e-113">يمكنك إعداد المعلمات لمستخدمين محددين أو لكافة المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="de65e-113">You can set up the parameters for specific users or all users.</span></span>  
4. <span data-ttu-id="de65e-114">في حقل "اتجاه الجدولة"، حدد "‏‫مستقبلي من اليوم‬".</span><span class="sxs-lookup"><span data-stu-id="de65e-114">In the Scheduling direction field, select 'Forward from today'.</span></span>
5. <span data-ttu-id="de65e-115">في حقل "تاريخ الجدولة"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="de65e-115">In the Scheduling date field, enter a date.</span></span>
6. <span data-ttu-id="de65e-116">حدد خانة الاختيار "‏‫قدرة محدودة" أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="de65e-116">Select or clear the Finite capacity check box.</span></span>
7. <span data-ttu-id="de65e-117">حدد خانة الاختيار "‏‫مواد محدودة" أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="de65e-117">Select or clear the Finite material check box.</span></span>
8. <span data-ttu-id="de65e-118">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="de65e-118">Click OK.</span></span>

## <a name="view-the-scheduling-results"></a><span data-ttu-id="de65e-119">عرض نتائج الجدولة</span><span class="sxs-lookup"><span data-stu-id="de65e-119">View the scheduling results</span></span>
1. <span data-ttu-id="de65e-120">في جزء "الإجراءات"، انقر فوق "أمر إنتاج".</span><span class="sxs-lookup"><span data-stu-id="de65e-120">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="de65e-121">انقر فوق كافة الوظائف.</span><span class="sxs-lookup"><span data-stu-id="de65e-121">Click All jobs.</span></span>
    * <span data-ttu-id="de65e-122">تعرض هذه الصفحة الوظائف المجدولة التي قمت بإنشائها للتو.</span><span class="sxs-lookup"><span data-stu-id="de65e-122">This page displays the scheduled jobs that you have just generated.</span></span>  
3. <span data-ttu-id="de65e-123">قم بتوسيع قسم "الجدولة" أو طيه.</span><span class="sxs-lookup"><span data-stu-id="de65e-123">Expand or collapse the Scheduling section.</span></span>
    * <span data-ttu-id="de65e-124">في علامة التبويب السريعة "الجدولة"، يمكنك عرض الوقت والتاريخ المجدولين.</span><span class="sxs-lookup"><span data-stu-id="de65e-124">On the Scheduling FastTab, you can view the scheduled date and time.</span></span>  
4. <span data-ttu-id="de65e-125">انقر فوق "استعلامات".</span><span class="sxs-lookup"><span data-stu-id="de65e-125">Click Inquiries.</span></span>
5. <span data-ttu-id="de65e-126">انقر فوق القدرة الإنتاجية.</span><span class="sxs-lookup"><span data-stu-id="de65e-126">Click Capacity load.</span></span>
    * <span data-ttu-id="de65e-127">تعرض صفحة القدرة الإنتاجية القدرة المخزنة من خلال جدولة الوظائف والعدد الإجمالي للساعات المحجوزة حاليًا للمورد وعدد الساعات التي لا تزال متاحة لجدولة وظيفة للمورد.</span><span class="sxs-lookup"><span data-stu-id="de65e-127">The Capacity load page displays the capacity that is reserved through job scheduling, the total number of hours that are currently reserved on the resource, and the number of hours that remain available for job scheduling on the resource.</span></span>  
6. <span data-ttu-id="de65e-128">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="de65e-128">Close the page.</span></span>
7. <span data-ttu-id="de65e-129">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="de65e-129">Close the page.</span></span>

