---
title: إزالة وظيفة كانبان من الجدول
description: يركز هذا الإجراء على إزالة وظيفة كانبان للمعالجة مخططة من الجدول من خلال عكس حالة الوظيفة إلى "غير مخطط".
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, SysLookupMultiSelectGrid, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0236faa9b534678ed232ac3572c8172c62e5241f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210584"
---
# <a name="remove-a-kanban-job-from-the-schedule"></a><span data-ttu-id="ef49c-103">إزالة وظيفة كانبان من الجدول</span><span class="sxs-lookup"><span data-stu-id="ef49c-103">Remove a kanban job from the schedule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ef49c-104">يركز هذا الإجراء على إزالة وظيفة كانبان للمعالجة مخططة من الجدول من خلال عكس حالة الوظيفة إلى "غير مخطط".</span><span class="sxs-lookup"><span data-stu-id="ef49c-104">This procedure focuses on removing a planned process kanban job from the schedule by reverting the job status to Not planned.</span></span> <span data-ttu-id="ef49c-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="ef49c-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ef49c-106">هذا الإجراء مخصص للمشرف على صالة الإنتاج‬ أو مخطط الإنتاج‬.</span><span class="sxs-lookup"><span data-stu-id="ef49c-106">This procedure is intended for the shop floor supervisor or production planner.</span></span>


## <a name="find-a-planned-kanban-job"></a><span data-ttu-id="ef49c-107">البحث عن وظيفة كانبان مخططة</span><span class="sxs-lookup"><span data-stu-id="ef49c-107">Find a planned kanban job</span></span>
1. <span data-ttu-id="ef49c-108">انتقل إلى التحكم بالإنتاج‬ > كانبان > جدولة وظيفة كانبان‬.</span><span class="sxs-lookup"><span data-stu-id="ef49c-108">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="ef49c-109">في الحقل "خلية العمل"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="ef49c-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="ef49c-110">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="ef49c-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ef49c-111">حدد خلية العمل 1250.</span><span class="sxs-lookup"><span data-stu-id="ef49c-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="ef49c-112">انقر فوق تحديد.</span><span class="sxs-lookup"><span data-stu-id="ef49c-112">Click Select.</span></span>
5. <span data-ttu-id="ef49c-113">في الحقل "عرض حالة الوظيفة‬"، حدد "'مجدول".</span><span class="sxs-lookup"><span data-stu-id="ef49c-113">In the Display job status field, select 'Scheduled'.</span></span>

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a><span data-ttu-id="ef49c-114">إزالة وظيفة كانبان المخططة من الجدول</span><span class="sxs-lookup"><span data-stu-id="ef49c-114">Remove the planned kanban job from the schedule</span></span>
1. <span data-ttu-id="ef49c-115">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="ef49c-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ef49c-116">حدد وظيفة حالتها "مخطط"، على سبيل المثال، وظيفة من 19 كانون الأول/ديسمبر 2012.</span><span class="sxs-lookup"><span data-stu-id="ef49c-116">Select a job that has the Planned status, for example, a job from December 19, 2012.</span></span>  
2. <span data-ttu-id="ef49c-117">في جزء "الإجراءات"، انقر فوق "خطة".</span><span class="sxs-lookup"><span data-stu-id="ef49c-117">On the Action Pane, click Plan.</span></span>
3. <span data-ttu-id="ef49c-118">انقر فوق "عكس حالة الوظيفة"</span><span class="sxs-lookup"><span data-stu-id="ef49c-118">Click Revert job status.</span></span>
4. <span data-ttu-id="ef49c-119">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="ef49c-119">Click OK.</span></span>
    * <span data-ttu-id="ef49c-120">سيؤدي ذلك إلى عكس حالة الوظيفة الحالية من 'مخطط' 'غير مخطط' وإزالتها من لوحة المعالجة.</span><span class="sxs-lookup"><span data-stu-id="ef49c-120">This will revert the current job status from 'Planned' to 'Not planned' and remove it from the process board.</span></span>   

