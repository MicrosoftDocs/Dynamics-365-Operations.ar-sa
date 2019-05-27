---
title: إزالة وظيفة كانبان من الجدول
description: يركز هذا الإجراء على إزالة وظيفة كانبان للمعالجة مخططة من الجدول من خلال عكس حالة الوظيفة إلى "غير مخطط".
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, SysLookupMultiSelectGrid, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b4d994be5c6bb1edc6f0fc64494a19a5babf72ae
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571939"
---
# <a name="remove-a-kanban-job-from-the-schedule"></a><span data-ttu-id="e5bf0-103">إزالة وظيفة كانبان من الجدول</span><span class="sxs-lookup"><span data-stu-id="e5bf0-103">Remove a kanban job from the schedule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e5bf0-104">يركز هذا الإجراء على إزالة وظيفة كانبان للمعالجة مخططة من الجدول من خلال عكس حالة الوظيفة إلى "غير مخطط".</span><span class="sxs-lookup"><span data-stu-id="e5bf0-104">This procedure focuses on removing a planned process kanban job from the schedule by reverting the job status to Not planned.</span></span> <span data-ttu-id="e5bf0-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="e5bf0-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="e5bf0-106">هذا الإجراء مخصص للمشرف على صالة الإنتاج‬ أو مخطط الإنتاج‬.</span><span class="sxs-lookup"><span data-stu-id="e5bf0-106">This procedure is intended for the shop floor supervisor or production planner.</span></span>


## <a name="find-a-planned-kanban-job"></a><span data-ttu-id="e5bf0-107">البحث عن وظيفة كانبان مخططة</span><span class="sxs-lookup"><span data-stu-id="e5bf0-107">Find a planned kanban job</span></span>
1. <span data-ttu-id="e5bf0-108">انتقل إلى التحكم بالإنتاج‬ > كانبان > جدولة وظيفة كانبان‬.</span><span class="sxs-lookup"><span data-stu-id="e5bf0-108">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="e5bf0-109">في الحقل "خلية العمل"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e5bf0-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="e5bf0-110">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e5bf0-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e5bf0-111">حدد خلية العمل 1250.</span><span class="sxs-lookup"><span data-stu-id="e5bf0-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="e5bf0-112">انقر فوق تحديد.</span><span class="sxs-lookup"><span data-stu-id="e5bf0-112">Click Select.</span></span>
5. <span data-ttu-id="e5bf0-113">في الحقل "عرض حالة الوظيفة‬"، حدد "'مجدول".</span><span class="sxs-lookup"><span data-stu-id="e5bf0-113">In the Display job status field, select 'Scheduled'.</span></span>

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a><span data-ttu-id="e5bf0-114">إزالة وظيفة كانبان المخططة من الجدول</span><span class="sxs-lookup"><span data-stu-id="e5bf0-114">Remove the planned kanban job from the schedule</span></span>
1. <span data-ttu-id="e5bf0-115">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e5bf0-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e5bf0-116">حدد وظيفة حالتها "مخطط"، على سبيل المثال، وظيفة من 19 كانون الأول/ديسمبر 2012.</span><span class="sxs-lookup"><span data-stu-id="e5bf0-116">Select a job that has the Planned status, for example, a job from December 19, 2012.</span></span>  
2. <span data-ttu-id="e5bf0-117">في جزء "الإجراءات"، انقر فوق "خطة".</span><span class="sxs-lookup"><span data-stu-id="e5bf0-117">On the Action Pane, click Plan.</span></span>
3. <span data-ttu-id="e5bf0-118">انقر فوق "عكس حالة الوظيفة"</span><span class="sxs-lookup"><span data-stu-id="e5bf0-118">Click Revert job status.</span></span>
4. <span data-ttu-id="e5bf0-119">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="e5bf0-119">Click OK.</span></span>
    * <span data-ttu-id="e5bf0-120">سيؤدي ذلك إلى عكس حالة الوظيفة الحالية من 'مخطط' 'غير مخطط' وإزالتها من لوحة المعالجة.</span><span class="sxs-lookup"><span data-stu-id="e5bf0-120">This will revert the current job status from 'Planned' to 'Not planned' and remove it from the process board.</span></span>   

