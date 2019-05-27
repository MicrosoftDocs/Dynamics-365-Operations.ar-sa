---
title: إنشاء قاعدة كانبان جديدة عن طريق تكرار قاعدة كانبان الموجودة
description: ويركز هذا الإجراء على إنشاء نسخة مكررة من قاعدة كانبان موجودة.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, InventItemIdLookupSimple
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7f72dbca0debf9e6a03ee700a979d4f4c110f819
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1559844"
---
# <a name="create-a-new-kanban-rule-by-duplicating-an-existing-kanban-rule"></a><span data-ttu-id="e0317-103">إنشاء قاعدة كانبان جديدة عن طريق تكرار قاعدة كانبان الموجودة</span><span class="sxs-lookup"><span data-stu-id="e0317-103">Create a new kanban rule by duplicating an existing kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e0317-104">ويركز هذا الإجراء على إنشاء نسخة مكررة من قاعدة كانبان موجودة.</span><span class="sxs-lookup"><span data-stu-id="e0317-104">This procedure focuses on creating a duplicate of an existing kanban rule.</span></span> <span data-ttu-id="e0317-105">وهذا مفيد إذا كنت تريد إنشاء قواعد كانبان جديدة تستند إلى قواعد كانبان الموجودة.</span><span class="sxs-lookup"><span data-stu-id="e0317-105">This is useful if you want to create new kanban rules based on existing kanban rules.</span></span> <span data-ttu-id="e0317-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="e0317-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="e0317-107">هذا الإجراء مخصص لمهندس العمليات أو مدير تدفق القيم عند تحضيرهم لإنتاج تدفق عمل مغيَّر أو قاعدة تزويد جديدة.</span><span class="sxs-lookup"><span data-stu-id="e0317-107">This procedure is intended for the process engineer or the value stream manager as they prepare production for a changed production flow or a new replenishment rule.</span></span>


## <a name="select-a-kanban-rule"></a><span data-ttu-id="e0317-108">حدد "قاعدة كانبان".</span><span class="sxs-lookup"><span data-stu-id="e0317-108">Select a kanban rule</span></span>
1. <span data-ttu-id="e0317-109">انتقل إلى قواعد كانبان.</span><span class="sxs-lookup"><span data-stu-id="e0317-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="e0317-110">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e0317-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e0317-111">حدد "قاعدة كانبان 000017 للمنتج M0006".</span><span class="sxs-lookup"><span data-stu-id="e0317-111">Select kanban rule 000017 for Product M0006.</span></span>  

## <a name="duplicate-a-kanban-rule"></a><span data-ttu-id="e0317-112">تكرار قاعدة كانبان</span><span class="sxs-lookup"><span data-stu-id="e0317-112">Duplicate a kanban rule</span></span>
1. <span data-ttu-id="e0317-113">انقر فوق "تكرار قاعدة كانبان".</span><span class="sxs-lookup"><span data-stu-id="e0317-113">Click Duplicate kanban rule.</span></span>
    * <span data-ttu-id="e0317-114">عند تكرار قاعدة كانبان، من الممكن تغيير تحديد النوع والتواريخ والأنشطة والمنتج.</span><span class="sxs-lookup"><span data-stu-id="e0317-114">When duplicating a kanban rule, it is possible to change type, dates, activities, and the product selection.</span></span> <span data-ttu-id="e0317-115">قم بتغيير المنتج المخصص لهذا الإجراء في الخطوة التالية.</span><span class="sxs-lookup"><span data-stu-id="e0317-115">Change the product for this procedure in the next step.</span></span>  
2. <span data-ttu-id="e0317-116">في الحقل "المنتج"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="e0317-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="e0317-117">حدد "M0007".</span><span class="sxs-lookup"><span data-stu-id="e0317-117">Select M0007.</span></span>  
3. <span data-ttu-id="e0317-118">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="e0317-118">Click OK.</span></span>
    * <span data-ttu-id="e0317-119">لاحظ أنه يتم إنشاء نسخة مكررة قاعدة كانبان 000017.</span><span class="sxs-lookup"><span data-stu-id="e0317-119">Note that a duplicate of kanban rule 000017 is created.</span></span>    

