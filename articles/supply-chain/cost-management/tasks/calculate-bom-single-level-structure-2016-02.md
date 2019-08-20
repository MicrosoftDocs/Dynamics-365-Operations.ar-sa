---
title: حساب قائمة مكونات الصنف باستخدام هيكل أحادي المستوى (فبراير 2016)
description: يوضح هذا الإجراء كيفية حساب تكلفة المنتج النهائي باستخدام عملية تحديد إجمالي المكونات المطلوبة‬ أحادية المستوى يوجد أساسها في كشف التكاليف.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c1968703c7e9662b5cccdb71d049010bb4bd4534
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836494"
---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016"></a><span data-ttu-id="0d37d-103">حساب قائمة مكونات الصنف باستخدام هيكل أحادي المستوى (فبراير 2016)</span><span class="sxs-lookup"><span data-stu-id="0d37d-103">Calculate a BOM by using a single level structure (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0d37d-104">يوضح هذا الإجراء كيفية حساب تكلفة المنتج النهائي باستخدام عملية تحديد إجمالي المكونات المطلوبة‬ أحادية المستوى يوجد أساسها في كشف التكاليف.</span><span class="sxs-lookup"><span data-stu-id="0d37d-104">This procedure shows how to calculate the cost of a finished product by using single level explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="0d37d-105">إنها المهمة السادسة في سلسلة حسابات قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="0d37d-105">This is the sixth task in the BOM calculation series.</span></span> <span data-ttu-id="0d37d-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USMF.‬</span><span class="sxs-lookup"><span data-stu-id="0d37d-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="0d37d-107">انتقل إلى "المنتجات الصادرة‬".</span><span class="sxs-lookup"><span data-stu-id="0d37d-107">Go to Released products.</span></span>
2. <span data-ttu-id="0d37d-108">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="0d37d-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0d37d-109">حدد المنتج BOM_1.</span><span class="sxs-lookup"><span data-stu-id="0d37d-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="0d37d-110">في جزء الإجراءات، انقر فوق "إدارة التكاليف‬".</span><span class="sxs-lookup"><span data-stu-id="0d37d-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="0d37d-111">انقر فوق "سعر الصنف".</span><span class="sxs-lookup"><span data-stu-id="0d37d-111">Click Item price.</span></span>
5. <span data-ttu-id="0d37d-112">انقر فوق "حساب تكلفة الصنف".</span><span class="sxs-lookup"><span data-stu-id="0d37d-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="0d37d-113">قد تحتاج إلى النقر فوق علامة القطع (...) لرؤية هذا الخيار في القائمة العلوية.</span><span class="sxs-lookup"><span data-stu-id="0d37d-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="0d37d-114">في الحقل "إصدار محاسبة التكاليف"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="0d37d-114">In the Costing version field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="0d37d-115">بالنسبة إلى هذا العرض التوضيحي، حدد 10.</span><span class="sxs-lookup"><span data-stu-id="0d37d-115">For this demo, select 10.</span></span> <span data-ttu-id="0d37d-116">هذا هو إصدار محاسبة التكاليف نفسه المستخدم لإضافة سعر التكلفة إلى المكونات.</span><span class="sxs-lookup"><span data-stu-id="0d37d-116">This is the same costing version used for adding the cost price to the components.</span></span>  
7. <span data-ttu-id="0d37d-117">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="0d37d-117">Click OK.</span></span>
8. <span data-ttu-id="0d37d-118">انقر فوق "عرض تفاصيل الحساب"ز</span><span class="sxs-lookup"><span data-stu-id="0d37d-118">Click View calculation details.</span></span>
    * <span data-ttu-id="0d37d-119">قد تحتاج إلى النقر فوق علامة القطع (...) لرؤية هذا الخيار في القائمة العلوية.</span><span class="sxs-lookup"><span data-stu-id="0d37d-119">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>    <span data-ttu-id="0d37d-120">إليك تركيب التكلفة:  •    يشتق 10 من ITEM_A، و10 من ITEM_B, 10 من BOM_2.</span><span class="sxs-lookup"><span data-stu-id="0d37d-120">Here's the composition of the cost:  •    10 is derived from ITEM_A, 10 from ITEM_B, 10 from BOM_2.</span></span> <span data-ttu-id="0d37d-121">وفي هذه الحالة لا توجد تفاصيل لـ BOM_2 حيث تم إدخالها كتكلفة معيارية من 10 لكن ذلك لم يتم من خلال الحساب.</span><span class="sxs-lookup"><span data-stu-id="0d37d-121">In this case there are no details for BOM_2 because it was entered as a standard cost of 10 but not done through calculation.</span></span>  <span data-ttu-id="0d37d-122">•  يشتق 7 من وقت الإعداد، وهو تكلفة ثابتة، ويشتق 7 إضافي من عملية وقت التشغيل (العملية).</span><span class="sxs-lookup"><span data-stu-id="0d37d-122">•  7 is derived from the setup time, which is a constant cost, and additional 7 is derived from the run-time operation (Process).</span></span>  <span data-ttu-id="0d37d-123">•   هناك أيضًا مبالغ أخرى تتطابق مع التكاليف غير المباشرة.</span><span class="sxs-lookup"><span data-stu-id="0d37d-123">•   There are also other amounts that correspond to indirect costs.</span></span>  
9. <span data-ttu-id="0d37d-124">@SysTaskRecorder:_RequestClose</span><span class="sxs-lookup"><span data-stu-id="0d37d-124">@SysTaskRecorder:_RequestClose</span></span>

