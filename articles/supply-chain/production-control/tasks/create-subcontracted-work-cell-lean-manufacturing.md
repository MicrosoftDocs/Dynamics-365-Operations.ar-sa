---
title: إنشاء خلية عمل متعاقد عليها من الباطن لـ lean manufacturing
description: لتصميم نموذج متعاقد عليه من الباطن لـ lean manufacturing، يجب عليك إنشاء خلية عمل مرتبطة بالمورّد الذي وفر العمل.
author: cvocph
manager: tfehr
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 236ce97fcf4ca76f07ae5f9308cf45240590b399
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5228529"
---
# <a name="create-a-subcontracted-work-cell-for-lean-manufacturing"></a><span data-ttu-id="f7c02-103">إنشاء خلية عمل متعاقد عليها من الباطن لـ lean manufacturing</span><span class="sxs-lookup"><span data-stu-id="f7c02-103">Create a subcontracted work cell for lean manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f7c02-104">لتصميم نموذج متعاقد عليه من الباطن لـ lean manufacturing، يجب عليك إنشاء خلية عمل مرتبطة بالمورّد الذي وفر العمل.</span><span class="sxs-lookup"><span data-stu-id="f7c02-104">To model subcontracted work for lean manufacturing, you must create a work cell that is associated with the vendor that provides the work.</span></span> <span data-ttu-id="f7c02-105">ترتبط خلية عمل متعاقد عليه من الباطن بالمورّد من خلال ربط مورد بنوع المورّد.</span><span class="sxs-lookup"><span data-stu-id="f7c02-105">A subcontracted work cell is linked to the vendor through the association of a resource of the Vendor type.</span></span> <span data-ttu-id="f7c02-106">إذا قمت بتشغيل هذا التسجيل في شركة العرض التوضيحي USMF، فيمكنك تحديد معرّف حساب المورّد 1002 والموقع 1.</span><span class="sxs-lookup"><span data-stu-id="f7c02-106">If you play this recording in the USMF demo company, you can select vendor account ID 1002 and site 1.</span></span>


## <a name="create-a-vendor-resource"></a><span data-ttu-id="f7c02-107">إنشاء مورد مورّد</span><span class="sxs-lookup"><span data-stu-id="f7c02-107">Create a vendor resource</span></span>
1. <span data-ttu-id="f7c02-108">انتقل إلى "الموارد".</span><span class="sxs-lookup"><span data-stu-id="f7c02-108">Go to Resources.</span></span>
2. <span data-ttu-id="f7c02-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="f7c02-109">Click New.</span></span>
3. <span data-ttu-id="f7c02-110">في الحقل "المورد"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f7c02-110">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="f7c02-111">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f7c02-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f7c02-112">في حقل "النوع"، حدد "المورّد".</span><span class="sxs-lookup"><span data-stu-id="f7c02-112">In the Type field, select 'Vendor'.</span></span>
6. <span data-ttu-id="f7c02-113">في الحقل "المورّد‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f7c02-113">In the Vendor field, click the drop-down button to open the lookup.</span></span>

## <a name="create-the-resource-group"></a><span data-ttu-id="f7c02-114">إنشاء مجموعة موارد</span><span class="sxs-lookup"><span data-stu-id="f7c02-114">Create the resource group</span></span>
1. <span data-ttu-id="f7c02-115">انتقل إلى مجموعات الموارد.</span><span class="sxs-lookup"><span data-stu-id="f7c02-115">Go to Resource groups.</span></span>
2. <span data-ttu-id="f7c02-116">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="f7c02-116">Click New.</span></span>
3. <span data-ttu-id="f7c02-117">في حقل مجموعة "الموارد"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f7c02-117">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="f7c02-118">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f7c02-118">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f7c02-119">في الحقل "الموقع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f7c02-119">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f7c02-120">حدد الموقع التي يجب أن يتم تعيين خلية العمل له.</span><span class="sxs-lookup"><span data-stu-id="f7c02-120">Select the site that the work cell should be allocated to.</span></span> <span data-ttu-id="f7c02-121">من الناحية النظرية، بإمكان الموقع أن يمثل موقعًا فرديًا يتم تشغيله بواسطة مورّد.</span><span class="sxs-lookup"><span data-stu-id="f7c02-121">In theory, a site can represent a single site that is operated by a vendor.</span></span> <span data-ttu-id="f7c02-122">ولكن، في معظم الحالات، يتم تخصيص الموارد المتعاقد عليها من الباطن فقط للموقع الذي طلب العمل المتعاقد عليه من الباطن.</span><span class="sxs-lookup"><span data-stu-id="f7c02-122">However, in most cases, subcontracted resources are just allocated to the site that orders the subcontracted work.</span></span> <span data-ttu-id="f7c02-123">لاحظ أنه من الضروري وجود المستودعات الإدخال والإخراج لخلايا العمل المتعاقد عليه من الباطن في الموقع نفسه.</span><span class="sxs-lookup"><span data-stu-id="f7c02-123">Note that the input and output warehouses of subcontracted work cells must be on the same site.</span></span>  
6. <span data-ttu-id="f7c02-124">في الحقل "الموقع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f7c02-124">In the Site field, type a value.</span></span>
7. <span data-ttu-id="f7c02-125">@SysTaskRecorder:_RequestClose</span><span class="sxs-lookup"><span data-stu-id="f7c02-125">@SysTaskRecorder:_RequestClose</span></span>
8. <span data-ttu-id="f7c02-126">حدد خانة الاختيار "خلية العمل" أو امسحها.</span><span class="sxs-lookup"><span data-stu-id="f7c02-126">Select or clear the Work cell check box.</span></span>
9. <span data-ttu-id="f7c02-127">في الحقل "مستودع الإدخال"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f7c02-127">In the Input warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f7c02-128">حدد المستودع والموقع المستخدمين لتقديم المواد لخلية العمل التي يديرها المورّد.</span><span class="sxs-lookup"><span data-stu-id="f7c02-128">Select the warehouse and location that are used to stage the material for the vendor-managed work cell.</span></span> <span data-ttu-id="f7c02-129">في الكثير من الحالات، يتم تصميم المستودع والموقع باستخدام مستودع منفصل لكل مورّد وموقع لكل خلية عمل.</span><span class="sxs-lookup"><span data-stu-id="f7c02-129">In many cases, the warehouse and location are modeled by using a separate warehouse per vendor and one location per work cell.</span></span>  
10. <span data-ttu-id="f7c02-130">في الحقل "موقع الإدخال"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f7c02-130">In the Input location field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="f7c02-131">في الحقل "مستودع الإخراج"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f7c02-131">In the Output warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f7c02-132">حدد المستودع والموقع حيث يتم ترحيل المواد عند ترحيل الأنشطة المتعاقد عليها من الباطن لخلية العمل.</span><span class="sxs-lookup"><span data-stu-id="f7c02-132">Define the warehouse and location where the material is posted when the subcontracted activities of the work cell are posted.</span></span> <span data-ttu-id="f7c02-133">بإمكان المستودع والموقع أن يكونا في موقع المورّد في حال قيام المورّد بإعداد تقرير عن وظائف كانبان.</span><span class="sxs-lookup"><span data-stu-id="f7c02-133">The warehouse and location can be at the vendor site if the vendor reports the kanban jobs.</span></span> <span data-ttu-id="f7c02-134">بدلاً من ذلك، بإمكان المستودع والموقع أن يكونا الموقع المستلم المقترن بالخطوة التالية من تدفق الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="f7c02-134">Alternatively, the warehouse and location can be the receiving location that is associated with the next step of the production flow.</span></span>  
12. <span data-ttu-id="f7c02-135">في الحقل "موقع الإخراج"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f7c02-135">In the Output location field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="f7c02-136">قم بتوسيع القسم "التقويمات" أو طيه.</span><span class="sxs-lookup"><span data-stu-id="f7c02-136">Expand or collapse the Calendars section.</span></span>
14. <span data-ttu-id="f7c02-137">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="f7c02-137">Click Add.</span></span>
15. <span data-ttu-id="f7c02-138">في الحقل "التقويم"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f7c02-138">In the Calendar field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f7c02-139">قم بإقران تقويم وقت العمل لخلية العمل بمجموعة الموارد.</span><span class="sxs-lookup"><span data-stu-id="f7c02-139">Associate the working time calendar of the work cell with the resource group.</span></span> <span data-ttu-id="f7c02-140">بالنسبة إلى الموارد الضرورية، من المستحسن أن تقوم بتحديد تقويمات محددة تمثل أوقات العمل الدقيقة والقدرات ذات الصلة لخلية العمل أو موقع المورّد.</span><span class="sxs-lookup"><span data-stu-id="f7c02-140">For critical resources, we recommend that you define specific calendars that represent the exact working times and related capacities of the work cell or vendor site.</span></span>  
16. <span data-ttu-id="f7c02-141">قم بتوسيع أو طي مقطع "الموارد".</span><span class="sxs-lookup"><span data-stu-id="f7c02-141">Expand or collapse the Resources section.</span></span>
17. <span data-ttu-id="f7c02-142">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="f7c02-142">Click Add.</span></span>
    * <span data-ttu-id="f7c02-143">يجب أين يتوفر لدى مجموعة الموارد المتعاقد عليها من الباطن موردًا مقترنًا من نوع المورّد يعمل على ربط مجموعة الموارد بحساب المورّد.</span><span class="sxs-lookup"><span data-stu-id="f7c02-143">A subcontracted resource group must have an associated resource of the Vendor type that links the resource group to the vendor account.</span></span>  
18. <span data-ttu-id="f7c02-144">في حقل "المورد"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f7c02-144">In the Resource field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f7c02-145">حدد أو أدخل مورد المورّد الذي أنشأته في المهمة الفرعية السابقة.</span><span class="sxs-lookup"><span data-stu-id="f7c02-145">Select or enter the vendor resource that you created in the previous sub-task.</span></span>  
19. <span data-ttu-id="f7c02-146">‏‫قم بتوسيع القسم "قدرة خلية العمل‬‬" أو طيّه.</span><span class="sxs-lookup"><span data-stu-id="f7c02-146">Expand or collapse the Work cell capacity section.</span></span>
20. <span data-ttu-id="f7c02-147">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="f7c02-147">Click Add.</span></span>
    * <span data-ttu-id="f7c02-148">يجب أن يكون لخلية عمل قدرة محددة.</span><span class="sxs-lookup"><span data-stu-id="f7c02-148">A work cell must have a defined capacity.</span></span> <span data-ttu-id="f7c02-149">في هذا المثال، نقوم بإنشاء قدرة إنتاجية من 100 قطعة لكل يوم عمل قياسي.</span><span class="sxs-lookup"><span data-stu-id="f7c02-149">In this example, we create a throughput capacity of 100 pieces per standard workday.</span></span>  
21. <span data-ttu-id="f7c02-150">في الحقل "نموذج تدفق الإنتاج"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f7c02-150">In the Production flow model field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="f7c02-151">في الحقل "فترة القدرة"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="f7c02-151">In the Capacity period field, select an option.</span></span>
23. <span data-ttu-id="f7c02-152">في الحقل "متوسط كمية الإنتاجية"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="f7c02-152">In the Average throughput quantity field, enter a number.</span></span>
24. <span data-ttu-id="f7c02-153">في الحقل "الوحدة ‬‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f7c02-153">In the Unit field, click the drop-down button to open the lookup.</span></span>
25. <span data-ttu-id="f7c02-154">ResolveChanges الوحدة.</span><span class="sxs-lookup"><span data-stu-id="f7c02-154">ResolveChanges the Unit.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]