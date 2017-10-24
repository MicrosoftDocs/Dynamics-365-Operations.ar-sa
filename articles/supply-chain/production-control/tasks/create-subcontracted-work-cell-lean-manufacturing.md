--- 
title: "إنشاء خلية عمل متعاقد عليها من الباطن لـ lean manufacturing"
description: "لتصميم نموذج متعاقد عليه من الباطن لـ lean manufacturing، يجب عليك إنشاء خلية عمل مرتبطة بالمورّد الذي وفر العمل."
author: cvocph
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fc8dc0bc29c6bdb662c46808491abf5395f0be5d
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-subcontracted-work-cell-for-lean-manufacturing"></a><span data-ttu-id="f2512-103">إنشاء خلية عمل متعاقد عليها من الباطن لـ lean manufacturing</span><span class="sxs-lookup"><span data-stu-id="f2512-103">Create a subcontracted work cell for lean manufacturing</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f2512-104">لتصميم نموذج متعاقد عليه من الباطن لـ lean manufacturing، يجب عليك إنشاء خلية عمل مرتبطة بالمورّد الذي وفر العمل.</span><span class="sxs-lookup"><span data-stu-id="f2512-104">To model subcontracted work for lean manufacturing, you must create a work cell that is associated with the vendor that provides the work.</span></span> <span data-ttu-id="f2512-105">ترتبط خلية عمل متعاقد عليه من الباطن بالمورّد من خلال ربط مورد بنوع المورّد.</span><span class="sxs-lookup"><span data-stu-id="f2512-105">A subcontracted work cell is linked to the vendor through the association of a resource of the Vendor type.</span></span> <span data-ttu-id="f2512-106">إذا قمت بتشغيل هذا التسجيل في شركة العرض التوضيحي USMF، فيمكنك تحديد معرّف حساب المورّد 1002 والموقع 1.</span><span class="sxs-lookup"><span data-stu-id="f2512-106">If you play this recording in the USMF demo company, you can select vendor account ID 1002 and site 1.</span></span>


## <a name="create-a-vendor-resource"></a><span data-ttu-id="f2512-107">إنشاء مورد مورّد</span><span class="sxs-lookup"><span data-stu-id="f2512-107">Create a vendor resource</span></span>
1. <span data-ttu-id="f2512-108">انتقل إلى "الموارد".</span><span class="sxs-lookup"><span data-stu-id="f2512-108">Go to Resources.</span></span>
2. <span data-ttu-id="f2512-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="f2512-109">Click New.</span></span>
3. <span data-ttu-id="f2512-110">في الحقل "المورد"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f2512-110">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="f2512-111">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f2512-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f2512-112">في حقل "النوع"، حدد "المورّد".</span><span class="sxs-lookup"><span data-stu-id="f2512-112">In the Type field, select 'Vendor'.</span></span>
6. <span data-ttu-id="f2512-113">في الحقل "المورّد‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f2512-113">In the Vendor field, click the drop-down button to open the lookup.</span></span>

## <a name="create-the-resource-group"></a><span data-ttu-id="f2512-114">إنشاء مجموعة موارد</span><span class="sxs-lookup"><span data-stu-id="f2512-114">Create the resource group</span></span>
1. <span data-ttu-id="f2512-115">انتقل إلى مجموعات الموارد.</span><span class="sxs-lookup"><span data-stu-id="f2512-115">Go to Resource groups.</span></span>
2. <span data-ttu-id="f2512-116">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="f2512-116">Click New.</span></span>
3. <span data-ttu-id="f2512-117">في حقل مجموعة "الموارد"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f2512-117">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="f2512-118">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f2512-118">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f2512-119">في الحقل "الموقع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f2512-119">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f2512-120">حدد الموقع التي يجب أن يتم تعيين خلية العمل له.</span><span class="sxs-lookup"><span data-stu-id="f2512-120">Select the site that the work cell should be allocated to.</span></span> <span data-ttu-id="f2512-121">من الناحية النظرية، بإمكان الموقع أن يمثل موقعًا فرديًا يتم تشغيله بواسطة مورّد.</span><span class="sxs-lookup"><span data-stu-id="f2512-121">In theory, a site can represent a single site that is operated by a vendor.</span></span> <span data-ttu-id="f2512-122">ولكن، في معظم الحالات، يتم تخصيص الموارد المتعاقد عليها من الباطن فقط للموقع الذي طلب العمل المتعاقد عليه من الباطن.</span><span class="sxs-lookup"><span data-stu-id="f2512-122">However, in most cases, subcontracted resources are just allocated to the site that orders the subcontracted work.</span></span> <span data-ttu-id="f2512-123">لاحظ أنه من الضروري وجود المستودعات الإدخال والإخراج لخلايا العمل المتعاقد عليه من الباطن في الموقع نفسه.</span><span class="sxs-lookup"><span data-stu-id="f2512-123">Note that the input and output warehouses of subcontracted work cells must be on the same site.</span></span>  
6. <span data-ttu-id="f2512-124">في الحقل "الموقع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f2512-124">In the Site field, type a value.</span></span>
7. @SysTaskRecorder:_RequestClose
8. <span data-ttu-id="f2512-125">حدد خانة الاختيار "خلية العمل" أو امسحها.</span><span class="sxs-lookup"><span data-stu-id="f2512-125">Select or clear the Work cell check box.</span></span>
9. <span data-ttu-id="f2512-126">في الحقل "مستودع الإدخال"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f2512-126">In the Input warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f2512-127">حدد المستودع والموقع المستخدمين لتقديم المواد لخلية العمل التي يديرها المورّد.</span><span class="sxs-lookup"><span data-stu-id="f2512-127">Select the warehouse and location that are used to stage the material for the vendor-managed work cell.</span></span> <span data-ttu-id="f2512-128">في الكثير من الحالات، يتم تصميم المستودع والموقع باستخدام مستودع منفصل لكل مورّد وموقع لكل خلية عمل.</span><span class="sxs-lookup"><span data-stu-id="f2512-128">In many cases, the warehouse and location are modeled by using a separate warehouse per vendor and one location per work cell.</span></span>  
10. <span data-ttu-id="f2512-129">في الحقل "موقع الإدخال"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f2512-129">In the Input location field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="f2512-130">في الحقل "مستودع الإخراج"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f2512-130">In the Output warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f2512-131">حدد المستودع والموقع حيث يتم ترحيل المواد عند ترحيل الأنشطة المتعاقد عليها من الباطن لخلية العمل.</span><span class="sxs-lookup"><span data-stu-id="f2512-131">Define the warehouse and location where the material is posted when the subcontracted activities of the work cell are posted.</span></span> <span data-ttu-id="f2512-132">بإمكان المستودع والموقع أن يكونا في موقع المورّد في حال قيام المورّد بإعداد تقرير عن وظائف كانبان.</span><span class="sxs-lookup"><span data-stu-id="f2512-132">The warehouse and location can be at the vendor site if the vendor reports the kanban jobs.</span></span> <span data-ttu-id="f2512-133">بدلاً من ذلك، بإمكان المستودع والموقع أن يكونا الموقع المستلم المقترن بالخطوة التالية من تدفق الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="f2512-133">Alternatively, the warehouse and location can be the receiving location that is associated with the next step of the production flow.</span></span>  
12. <span data-ttu-id="f2512-134">في الحقل "موقع الإخراج"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f2512-134">In the Output location field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="f2512-135">قم بتوسيع القسم "التقويمات" أو طيه.</span><span class="sxs-lookup"><span data-stu-id="f2512-135">Expand or collapse the Calendars section.</span></span>
14. <span data-ttu-id="f2512-136">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="f2512-136">Click Add.</span></span>
15. <span data-ttu-id="f2512-137">في الحقل "التقويم"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f2512-137">In the Calendar field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f2512-138">قم بإقران تقويم وقت العمل لخلية العمل بمجموعة الموارد.</span><span class="sxs-lookup"><span data-stu-id="f2512-138">Associate the working time calendar of the work cell with the resource group.</span></span> <span data-ttu-id="f2512-139">بالنسبة إلى الموارد الضرورية، من المستحسن أن تقوم بتحديد تقويمات محددة تمثل أوقات العمل الدقيقة والقدرات ذات الصلة لخلية العمل أو موقع المورّد.</span><span class="sxs-lookup"><span data-stu-id="f2512-139">For critical resources, we recommend that you define specific calendars that represent the exact working times and related capacities of the work cell or vendor site.</span></span>  
16. <span data-ttu-id="f2512-140">قم بتوسيع أو طي مقطع "الموارد".</span><span class="sxs-lookup"><span data-stu-id="f2512-140">Expand or collapse the Resources section.</span></span>
17. <span data-ttu-id="f2512-141">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="f2512-141">Click Add.</span></span>
    * <span data-ttu-id="f2512-142">يجب أين يتوفر لدى مجموعة الموارد المتعاقد عليها من الباطن موردًا مقترنًا من نوع المورّد يعمل على ربط مجموعة الموارد بحساب المورّد.</span><span class="sxs-lookup"><span data-stu-id="f2512-142">A subcontracted resource group must have an associated resource of the Vendor type that links the resource group to the vendor account.</span></span>  
18. <span data-ttu-id="f2512-143">في حقل "المورد"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f2512-143">In the Resource field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f2512-144">حدد أو أدخل مورد المورّد الذي أنشأته في المهمة الفرعية السابقة.</span><span class="sxs-lookup"><span data-stu-id="f2512-144">Select or enter the vendor resource that you created in the previous sub-task.</span></span>  
19. <span data-ttu-id="f2512-145">‏‫قم بتوسيع القسم "قدرة خلية العمل‬‬" أو طيّه.</span><span class="sxs-lookup"><span data-stu-id="f2512-145">Expand or collapse the Work cell capacity section.</span></span>
20. <span data-ttu-id="f2512-146">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="f2512-146">Click Add.</span></span>
    * <span data-ttu-id="f2512-147">يجب أن يكون لخلية عمل قدرة محددة.</span><span class="sxs-lookup"><span data-stu-id="f2512-147">A work cell must have a defined capacity.</span></span> <span data-ttu-id="f2512-148">في هذا المثال، نقوم بإنشاء قدرة إنتاجية من 100 قطعة لكل يوم عمل قياسي.</span><span class="sxs-lookup"><span data-stu-id="f2512-148">In this example, we create a throughput capacity of 100 pieces per standard workday.</span></span>  
21. <span data-ttu-id="f2512-149">في الحقل "نموذج تدفق الإنتاج"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f2512-149">In the Production flow model field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="f2512-150">في الحقل "فترة القدرة"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="f2512-150">In the Capacity period field, select an option.</span></span>
23. <span data-ttu-id="f2512-151">في الحقل "متوسط كمية الإنتاجية"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="f2512-151">In the Average throughput quantity field, enter a number.</span></span>
24. <span data-ttu-id="f2512-152">في الحقل "الوحدة ‬‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="f2512-152">In the Unit field, click the drop-down button to open the lookup.</span></span>
25. <span data-ttu-id="f2512-153">ResolveChanges الوحدة.</span><span class="sxs-lookup"><span data-stu-id="f2512-153">ResolveChanges the Unit.</span></span>


