---
title: إعداد وظيفة كانبان عملية عندما تتوفر المواد لخلية العمل
description: تركز هذه المهمة على إعداد وظيفة كانبان عملية عندما تكو جميع المواد متوفرة لخلية العمل.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cd6d5add4d11c917a705e88d10b589e2c43fab89
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206919"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-available-for-the-work-cell"></a><span data-ttu-id="c4380-103">إعداد وظيفة كانبان عملية عندما تتوفر المواد لخلية العمل</span><span class="sxs-lookup"><span data-stu-id="c4380-103">Prepare a process kanban job when materials are available for the work cell</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c4380-104">تركز هذه المهمة على إعداد وظيفة كانبان عملية عندما تكو جميع المواد متوفرة لخلية العمل.</span><span class="sxs-lookup"><span data-stu-id="c4380-104">This task focuses on preparing a process kanban job when all materials are available for the work cell.</span></span> <span data-ttu-id="c4380-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USMF.‬</span><span class="sxs-lookup"><span data-stu-id="c4380-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="c4380-106">هذه المهمة مخصصة لعامل تشغيل الجهاز.</span><span class="sxs-lookup"><span data-stu-id="c4380-106">This task is intended for the machine operator.</span></span>

1. <span data-ttu-id="c4380-107">انتقل إلى "‏‫لوحة كانبان لوظائف المعالجة‬".</span><span class="sxs-lookup"><span data-stu-id="c4380-107">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="c4380-108">في الحقل "خلية العمل"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="c4380-108">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="c4380-109">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c4380-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c4380-110">حدد خلية العمل 1250 وانقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c4380-110">Select work cell 1250 and click OK.</span></span>  
4. <span data-ttu-id="c4380-111">في القائمة، حدد الصف 4.</span><span class="sxs-lookup"><span data-stu-id="c4380-111">In the list, select row 4.</span></span>
    * <span data-ttu-id="c4380-112">في شركة العرض التوضيحي، كانبان 000329 في الصف 4 هو الوظيفة الأولى التي لم تكتمل بعد.</span><span class="sxs-lookup"><span data-stu-id="c4380-112">In the clean demo company, Kanban 000329 in row 4 is the first job that is not completed yet.</span></span>  
5. <span data-ttu-id="c4380-113">بدّل توسيع المقطع قائمة الانتقاء".</span><span class="sxs-lookup"><span data-stu-id="c4380-113">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="c4380-114">تحقق من أن حالة التوريد متاحة لكافة الأصناف الموجودة في قائمة الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="c4380-114">Verify that the supply status is available for all items in the picking list.</span></span>  
    * <span data-ttu-id="c4380-115">إذا تم تحديد وظائف متعددة، فستعرض قائمة الانتقاء مجموع كافة الأصناف المطلوبة للوظائف المحددة.</span><span class="sxs-lookup"><span data-stu-id="c4380-115">If multiple jobs are selected, the picking list will show the sum of all items needed for the selected jobs.</span></span>  
6. <span data-ttu-id="c4380-116">انقر فوق "تحضير‬".</span><span class="sxs-lookup"><span data-stu-id="c4380-116">Click Prepare.</span></span>
    * <span data-ttu-id="c4380-117">تم الآن إكمال عملية التحضير.</span><span class="sxs-lookup"><span data-stu-id="c4380-117">The preparation process is now completed.</span></span> <span data-ttu-id="c4380-118">تشير خانة الاختيار المحددة لكافة الصفوف في قائمة الانتقاء إلى أن حالة التوريد هي "تم الانتقاء".</span><span class="sxs-lookup"><span data-stu-id="c4380-118">The selected check box for all rows in the picking list indicates that the supply status is picked.</span></span>  

