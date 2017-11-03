---
title: "أبعاد كائن التكاليف"
description: "عندما تقوم بتحليل التكاليف، يمكنك استخدام أبعاد عنصر التكلفة لتحديد المكان الذي تتدفق إليه التكاليف. ويمكنك استخدام أبعاد كائن التكلفة لتحديد المكان حيث يجب تعيين التكاليف. يوفر هذا الموضوع معلومات حول أبعاد كائن التكلفة."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimensionMember
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 223174
ms.assetid: 2a1cdd35-30cb-41e7-9506-67fd04a537c5
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8195b776e5d46485172c9f5550ab4ed6d8623dfc
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="cost-object-dimensions"></a><span data-ttu-id="66325-105">أبعاد كائن التكاليف</span><span class="sxs-lookup"><span data-stu-id="66325-105">Cost object dimensions</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="66325-106">عندما تقوم بتحليل التكاليف، يمكنك استخدام أبعاد عنصر التكلفة لتحديد المكان الذي تتدفق إليه التكاليف.</span><span class="sxs-lookup"><span data-stu-id="66325-106">When you analyze costs, you use cost element dimensions to determine where costs flow to.</span></span> <span data-ttu-id="66325-107">ويمكنك استخدام أبعاد كائن التكلفة لتحديد المكان حيث يجب تعيين التكاليف.</span><span class="sxs-lookup"><span data-stu-id="66325-107">You use cost object dimensions to determine where you should assign costs.</span></span> <span data-ttu-id="66325-108">يوفر هذا الموضوع معلومات حول أبعاد كائن التكلفة.</span><span class="sxs-lookup"><span data-stu-id="66325-108">This topic provides information about cost object dimensions.</span></span>

<span data-ttu-id="66325-109">بإمكان كائن التكلفة أن يكون أي نوع كائن تريد تقديره أو توزيع تكاليفه أو قياسه بشكل مباشر.</span><span class="sxs-lookup"><span data-stu-id="66325-109">A cost object can be any type of object that you want to estimate, allocate costs to, or measure directly.</span></span> <span data-ttu-id="66325-110">وتتضمن كائنات التكلفة النموذجية المنتجات والمشاريع والموارد والأقسام ومراكز التكلفة والمناطق الجغرافية.</span><span class="sxs-lookup"><span data-stu-id="66325-110">Typical cost objects include products, projects, resources, departments, cost centers, and geographical regions.</span></span> <span data-ttu-id="66325-111">تستخدم الإدارة كائنات التكلفة لتحديد التكاليف وأيضًا لتعزيز تحليل الربحية.</span><span class="sxs-lookup"><span data-stu-id="66325-111">Management uses cost objects to quantify costs and also to drive profitability analysis.</span></span>

## <a name="cost-object-dimensions-and-cost-object-dimension-members"></a><span data-ttu-id="66325-112">أبعاد كائن التكلفة وأعضاء أبعاد كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="66325-112">Cost object dimensions and cost object dimension members</span></span>
<span data-ttu-id="66325-113">تُعرف كائنات التكلفة بالاسم *أبعاد كائن التكلفة*.</span><span class="sxs-lookup"><span data-stu-id="66325-113">Cost objects are known as *cost object dimensions*.</span></span> <span data-ttu-id="66325-114">بعد أن تحدد الكيان الذي يجب أن يرجع إليه بُعد كائن التكلفة، يجب تحديد قيم الأبعاد الفردية أو استيرادها إلى محاسبة التكاليف من أنظمة مصادر أخرى.</span><span class="sxs-lookup"><span data-stu-id="66325-114">After you’ve decided which entity the cost object dimension should refer to, you must specify the individual dimension values or import them into Cost accounting from other source systems.</span></span> <span data-ttu-id="66325-115">تُعرف قيم الأبعاد الفردية هذه بالاسم *أعضاء أبعاد كائن التكلفة*.</span><span class="sxs-lookup"><span data-stu-id="66325-115">These individual dimension values are known as *cost object dimension members*.</span></span> <span data-ttu-id="66325-116">على سبيل المثال، تريد استخدام البعد المالي الذي يسمى مركز التكلفة كبُعد كائن التكلفة.</span><span class="sxs-lookup"><span data-stu-id="66325-116">For example, you want to use the financial dimension that is named Cost center as the cost object dimension.</span></span> <span data-ttu-id="66325-117">للاطلاع على كيفية تدفق التكاليف إلى مراكز التكلفة الفردية، يجب عليك استيراد أعضاء أبعاد كائن التكلفة.</span><span class="sxs-lookup"><span data-stu-id="66325-117">To see how costs flow to the individual cost centers, you must import the cost object dimension members.</span></span> <span data-ttu-id="66325-118">وفي هذه الحالة، تكون أعضاء أبعاد كائن تكلفة مراكز التكلفة الفعلية، مثل المبيعات والإنتاج والإدارة والمواقع الجغرافية.</span><span class="sxs-lookup"><span data-stu-id="66325-118">In this case, the cost object dimension members are the actual cost centers, such as Sales, Production, Administration, and Geographic locations.</span></span> <span data-ttu-id="66325-119">تظهر لقطة الشاشة التالية مثالاً لمراكز التكلفة كبعد كائن التكلفة مع مراكز التكلفة الفعلية الخاصة به كأعضاء أبعاد كائن التكلفة.</span><span class="sxs-lookup"><span data-stu-id="66325-119">The following screenshot shows an example of Cost Centers as the cost object dimension with its actual cost centers as cost object dimension members.</span></span> 

<span data-ttu-id="66325-120">[![أبعاد كائن التكلفة](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="66325-120">[![cost-object-dimensions](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)</span></span>

## <a name="import-cost-object-dimension-members-through-data-connectors"></a><span data-ttu-id="66325-121">استيراد أعضاء أبعاد كائن التكلفة من خلال موصلات البيانات</span><span class="sxs-lookup"><span data-stu-id="66325-121">Import cost object dimension members through data connectors</span></span>
<span data-ttu-id="66325-122">لتسهيل عملية استيراد أعضاء أبعاد كائن التكلفة، استخدم موصلات البيانات لاسترداد القيم من الكيانات التي تريد استخدامها كأبعاد كائن التكلفة.</span><span class="sxs-lookup"><span data-stu-id="66325-122">To make the import of cost object dimension members easier, you use data connectors to retrieve the values from the entities that you want to use as cost object dimensions.</span></span> <span data-ttu-id="66325-123">ويمكنك استخدام موصلات البيانات المنشأة مسبقًا أو موصلات البيانات المخصصة التق تقوم أنت بإنشائها.</span><span class="sxs-lookup"><span data-stu-id="66325-123">You can use either the pre-built data connectors or custom data connectors that you build.</span></span>




