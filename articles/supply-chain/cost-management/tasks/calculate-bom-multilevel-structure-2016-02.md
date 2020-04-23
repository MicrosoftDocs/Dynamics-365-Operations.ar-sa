---
title: حساب قائمة مكونات الصنف باستخدام هيكل متعدد المستويات (فبراير 2016)
description: يوضح هذا الإجراء كيفية حساب تكلفة المنتج النهائي باستخدام عملية تحديد إجمالي المكونات المطلوبة‬ متعددة المستويات يوجد أساسها في كشف التكاليف.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog, BOMCalcTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f4f3e20d483e2184366c4ee6eb179e12d2e2492e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214336"
---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016"></a><span data-ttu-id="3f3da-103">حساب قائمة مكونات الصنف باستخدام هيكل متعدد المستويات (فبراير 2016)</span><span class="sxs-lookup"><span data-stu-id="3f3da-103">Calculate a BOM by using a multilevel structure (February 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3f3da-104">يوضح هذا الإجراء كيفية حساب تكلفة المنتج النهائي باستخدام عملية تحديد إجمالي المكونات المطلوبة‬ متعددة المستويات يوجد أساسها في كشف التكاليف.</span><span class="sxs-lookup"><span data-stu-id="3f3da-104">This procedure shows how to calculate the cost of a finished product by using multilevel explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="3f3da-105">إنها المهمة السابعة في سلسلة حسابات قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="3f3da-105">It is the seventh task in the BOM calculation series.</span></span> <span data-ttu-id="3f3da-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USMF.‬</span><span class="sxs-lookup"><span data-stu-id="3f3da-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="3f3da-107">انتقل إلى إدارة معلومات المنتج > المنتجات > المنتجات الصادرة.</span><span class="sxs-lookup"><span data-stu-id="3f3da-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="3f3da-108">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="3f3da-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3f3da-109">حدد المنتج BOM_1.</span><span class="sxs-lookup"><span data-stu-id="3f3da-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="3f3da-110">في جزء الإجراءات، انقر فوق "إدارة التكاليف‬".</span><span class="sxs-lookup"><span data-stu-id="3f3da-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="3f3da-111">انقر فوق "سعر الصنف".</span><span class="sxs-lookup"><span data-stu-id="3f3da-111">Click Item price.</span></span>
5. <span data-ttu-id="3f3da-112">انقر فوق "حساب تكلفة الصنف".</span><span class="sxs-lookup"><span data-stu-id="3f3da-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="3f3da-113">قد تحتاج إلى النقر فوق علامة القطع (...) لرؤية هذا الخيار في القائمة العلوية.</span><span class="sxs-lookup"><span data-stu-id="3f3da-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="3f3da-114">في حقل "‏‫إصدار محاسبة التكاليف‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3f3da-114">In the Costing version field, enter or select a value.</span></span>
    * <span data-ttu-id="3f3da-115">حدد إصدار محاسبة التكاليف 20، لأنه نوع تكلفة مخططة ووضع عملية تحديد إجمالي المكونات المطلوبة‬ متعدد المستويات.</span><span class="sxs-lookup"><span data-stu-id="3f3da-115">Select Costing version 20, because it's Planned cost type and Explosion mode is Multilevel.</span></span>   <span data-ttu-id="3f3da-116">يُستخدم وضع عملية تحديد إجمالي المكونات المطلوبة‬ متعدد المستويات للتكاليف المخططة والمحاكاة.</span><span class="sxs-lookup"><span data-stu-id="3f3da-116">The Multilevel explosion mode is for planned costs and simulations.</span></span> <span data-ttu-id="3f3da-117">ولا يتم استخدامه للتكلفة القياسية.</span><span class="sxs-lookup"><span data-stu-id="3f3da-117">It is not used for standard cost.</span></span>  
7. <span data-ttu-id="3f3da-118">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="3f3da-118">Click OK.</span></span>
8. <span data-ttu-id="3f3da-119">انقر فوق "عرض تفاصيل الحساب"ز</span><span class="sxs-lookup"><span data-stu-id="3f3da-119">Click View calculation details.</span></span>
    * <span data-ttu-id="3f3da-120">قد تحتاج إلى النقر فوق علامة القطع (...) لرؤية هذا الخيار في القائمة العلوية.</span><span class="sxs-lookup"><span data-stu-id="3f3da-120">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  <span data-ttu-id="3f3da-121">في هذه الحالة، لاحظ كيف تم حساب BOM_2 مع مراعاة المواد الخام والعملية والمصروفات بإجمالي 29,40 بدلاً من التكلفة القياسية من 10 التي تم تنشيطها في دليل المهمة الأول في هذه السلسلة.</span><span class="sxs-lookup"><span data-stu-id="3f3da-121">In this case, notice how BOM_2 has been calculated taking into account the raw material, process, and overhead with a total of 29,40 instead of the standard cost of 10 that was activated in the initial task guide in this series.</span></span>  
9. <span data-ttu-id="3f3da-122">انقر فوق علامة تبويب "كشف التكاليف".</span><span class="sxs-lookup"><span data-stu-id="3f3da-122">Click the Costing sheet tab.</span></span>
    * <span data-ttu-id="3f3da-123">بالانتقال إلى علامة تبويب "كشف التكاليف"، يتبين أن الإجماليات حسب مجموعة التكاليف تختلف مقارنة بالحساب الذي تم في دليل المهمة السابق.</span><span class="sxs-lookup"><span data-stu-id="3f3da-123">Moving to the Costing sheet tab, the totals per cost group are different compared to the calculation done in previous task guide.</span></span>  
10. <span data-ttu-id="3f3da-124">في حقل "المستوى" حدد "متعدد".</span><span class="sxs-lookup"><span data-stu-id="3f3da-124">In the Level field, select 'Multi'.</span></span>
    * <span data-ttu-id="3f3da-125">عند تحديد "متعدد"، يتم تصنيف التكاليف حسب تركيب BOM_2، حيث يشتق الرقم 10 من مجموعة التكاليف M1 (ITEM_C)، ويشتق 15,60 من تصنيعه حيث مجموعة التكاليف هي L2.</span><span class="sxs-lookup"><span data-stu-id="3f3da-125">When selecting Multi, the costs are classified according to the composition of BOM_2, where 10 is derived from the M1 cost group (ITEM_C), and 15,60 is derived from its manufacturing where the cost group is L2.</span></span> <span data-ttu-id="3f3da-126">قد تختلف أيضًا التكاليف غير المباشرة.</span><span class="sxs-lookup"><span data-stu-id="3f3da-126">Indirect costs also vary.</span></span>  
11. <span data-ttu-id="3f3da-127">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3f3da-127">Close the page.</span></span>
12. <span data-ttu-id="3f3da-128">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3f3da-128">Close the page.</span></span>

