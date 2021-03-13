---
title: حساب قائمة مكونات الصنف باستخدام هيكل أحادي المستوى (فبراير 2016)
description: يوضح هذا الإجراء كيفية حساب تكلفة المنتج النهائي باستخدام عملية تحديد إجمالي المكونات المطلوبة‬ أحادية المستوى يوجد أساسها في كشف التكاليف.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 36f908e02c996c0d0a636fd9295b84fcc16b6b63
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011762"
---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016"></a><span data-ttu-id="859e6-103">حساب قائمة مكونات الصنف باستخدام هيكل أحادي المستوى (فبراير 2016)</span><span class="sxs-lookup"><span data-stu-id="859e6-103">Calculate a BOM by using a single level structure (February 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="859e6-104">يوضح هذا الإجراء كيفية حساب تكلفة المنتج النهائي باستخدام عملية تحديد إجمالي المكونات المطلوبة‬ أحادية المستوى يوجد أساسها في كشف التكاليف.</span><span class="sxs-lookup"><span data-stu-id="859e6-104">This procedure shows how to calculate the cost of a finished product by using single level explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="859e6-105">إنها المهمة السادسة في سلسلة حسابات قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="859e6-105">This is the sixth task in the BOM calculation series.</span></span> <span data-ttu-id="859e6-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USMF.‬</span><span class="sxs-lookup"><span data-stu-id="859e6-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="859e6-107">انتقل إلى "المنتجات الصادرة‬".</span><span class="sxs-lookup"><span data-stu-id="859e6-107">Go to Released products.</span></span>
2. <span data-ttu-id="859e6-108">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="859e6-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="859e6-109">حدد المنتج BOM_1.</span><span class="sxs-lookup"><span data-stu-id="859e6-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="859e6-110">في جزء الإجراءات، انقر فوق "إدارة التكاليف‬".</span><span class="sxs-lookup"><span data-stu-id="859e6-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="859e6-111">انقر فوق "سعر الصنف".</span><span class="sxs-lookup"><span data-stu-id="859e6-111">Click Item price.</span></span>
5. <span data-ttu-id="859e6-112">انقر فوق "حساب تكلفة الصنف".</span><span class="sxs-lookup"><span data-stu-id="859e6-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="859e6-113">قد تحتاج إلى النقر فوق علامة القطع (...) لرؤية هذا الخيار في القائمة العلوية.</span><span class="sxs-lookup"><span data-stu-id="859e6-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="859e6-114">في الحقل "إصدار محاسبة التكاليف"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="859e6-114">In the Costing version field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="859e6-115">بالنسبة إلى هذا العرض التوضيحي، حدد 10.</span><span class="sxs-lookup"><span data-stu-id="859e6-115">For this demo, select 10.</span></span> <span data-ttu-id="859e6-116">هذا هو إصدار محاسبة التكاليف نفسه المستخدم لإضافة سعر التكلفة إلى المكونات.</span><span class="sxs-lookup"><span data-stu-id="859e6-116">This is the same costing version used for adding the cost price to the components.</span></span>  
7. <span data-ttu-id="859e6-117">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="859e6-117">Click OK.</span></span>
8. <span data-ttu-id="859e6-118">انقر فوق "عرض تفاصيل الحساب"ز</span><span class="sxs-lookup"><span data-stu-id="859e6-118">Click View calculation details.</span></span>
    * <span data-ttu-id="859e6-119">قد تحتاج إلى النقر فوق علامة القطع (...) لرؤية هذا الخيار في القائمة العلوية.</span><span class="sxs-lookup"><span data-stu-id="859e6-119">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>    <span data-ttu-id="859e6-120">إليك تركيب التكلفة:  \*    يشتق 10 من ITEM_A، و10 من ITEM_B, 10 من BOM_2.</span><span class="sxs-lookup"><span data-stu-id="859e6-120">Here's the composition of the cost:  \*    10 is derived from ITEM_A, 10 from ITEM_B, 10 from BOM_2.</span></span> <span data-ttu-id="859e6-121">وفي هذه الحالة لا توجد تفاصيل لـ BOM_2 حيث تم إدخالها كتكلفة معيارية من 10 لكن ذلك لم يتم من خلال الحساب.</span><span class="sxs-lookup"><span data-stu-id="859e6-121">In this case there are no details for BOM_2 because it was entered as a standard cost of 10 but not done through calculation.</span></span>  <span data-ttu-id="859e6-122">\*  يشتق 7 من وقت الإعداد، وهو تكلفة ثابتة، ويشتق 7 إضافي من عملية وقت التشغيل (العملية).</span><span class="sxs-lookup"><span data-stu-id="859e6-122">\*    7 is derived from the setup time, which is a constant cost, and additional 7 is derived from the run-time operation (Process).</span></span>  <span data-ttu-id="859e6-123">\*   هناك أيضًا مبالغ أخرى تتطابق مع التكاليف غير المباشرة.</span><span class="sxs-lookup"><span data-stu-id="859e6-123">\*    There are also other amounts that correspond to indirect costs.</span></span>  
9. <span data-ttu-id="859e6-124">@SysTaskRecorder:_RequestClose</span><span class="sxs-lookup"><span data-stu-id="859e6-124">@SysTaskRecorder:_RequestClose</span></span>

