--- 
title: "إنشاء قاعدة كانبان جديدة عن طريق تكرار قاعدة كانبان الموجودة"
description: "ويركز هذا الإجراء على إنشاء نسخة مكررة من قاعدة كانبان موجودة."
author: ChristianRytt
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d375e6c029e575269f7b9fce8a2eb9ac95717b5c
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-new-kanban-rule-by-duplicating-an-existing-kanban-rule"></a><span data-ttu-id="9fd61-103">إنشاء قاعدة كانبان جديدة عن طريق تكرار قاعدة كانبان الموجودة</span><span class="sxs-lookup"><span data-stu-id="9fd61-103">Create a new kanban rule by duplicating an existing kanban rule</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9fd61-104">ويركز هذا الإجراء على إنشاء نسخة مكررة من قاعدة كانبان موجودة.</span><span class="sxs-lookup"><span data-stu-id="9fd61-104">This procedure focuses on creating a duplicate of an existing kanban rule.</span></span> <span data-ttu-id="9fd61-105">وهذا مفيد إذا كنت تريد إنشاء قواعد كانبان جديدة تستند إلى قواعد كانبان الموجودة.</span><span class="sxs-lookup"><span data-stu-id="9fd61-105">This is useful if you want to create new kanban rules based on existing kanban rules.</span></span> <span data-ttu-id="9fd61-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="9fd61-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="9fd61-107">هذا الإجراء مخصص لمهندس العمليات أو مدير تدفق القيم عند تحضيرهم لإنتاج تدفق عمل مغيَّر أو قاعدة تزويد جديدة.</span><span class="sxs-lookup"><span data-stu-id="9fd61-107">This procedure is intended for the process engineer or the value stream manager as they prepare production for a changed production flow or a new replenishment rule.</span></span>


## <a name="select-a-kanban-rule"></a><span data-ttu-id="9fd61-108">حدد "قاعدة كانبان".</span><span class="sxs-lookup"><span data-stu-id="9fd61-108">Select a kanban rule</span></span>
1. <span data-ttu-id="9fd61-109">انتقل إلى قواعد كانبان.</span><span class="sxs-lookup"><span data-stu-id="9fd61-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="9fd61-110">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="9fd61-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9fd61-111">حدد "قاعدة كانبان 000017 للمنتج M0006".</span><span class="sxs-lookup"><span data-stu-id="9fd61-111">Select kanban rule 000017 for Product M0006.</span></span>  

## <a name="duplicate-a-kanban-rule"></a><span data-ttu-id="9fd61-112">تكرار قاعدة كانبان</span><span class="sxs-lookup"><span data-stu-id="9fd61-112">Duplicate a kanban rule</span></span>
1. <span data-ttu-id="9fd61-113">انقر فوق "تكرار قاعدة كانبان".</span><span class="sxs-lookup"><span data-stu-id="9fd61-113">Click Duplicate kanban rule.</span></span>
    * <span data-ttu-id="9fd61-114">عند تكرار قاعدة كانبان، من الممكن تغيير تحديد النوع والتواريخ والأنشطة والمنتج.</span><span class="sxs-lookup"><span data-stu-id="9fd61-114">When duplicating a kanban rule, it is possible to change type, dates, activities, and the product selection.</span></span> <span data-ttu-id="9fd61-115">قم بتغيير المنتج المخصص لهذا الإجراء في الخطوة التالية.</span><span class="sxs-lookup"><span data-stu-id="9fd61-115">Change the product for this procedure in the next step.</span></span>  
2. <span data-ttu-id="9fd61-116">في الحقل "المنتج"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="9fd61-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="9fd61-117">حدد "M0007".</span><span class="sxs-lookup"><span data-stu-id="9fd61-117">Select M0007.</span></span>  
3. <span data-ttu-id="9fd61-118">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="9fd61-118">Click OK.</span></span>
    * <span data-ttu-id="9fd61-119">لاحظ أنه يتم إنشاء نسخة مكررة قاعدة كانبان 000017.</span><span class="sxs-lookup"><span data-stu-id="9fd61-119">Note that a duplicate of kanban rule 000017 is created.</span></span>    


