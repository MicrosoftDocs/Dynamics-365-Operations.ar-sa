---
title: إنشاء طلب للاستهلاك
description: يوضح لك هذا الإجراء عملية إنشاء طلب.
author: mkirknel
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e81ca3966cf7dae88468ccf107b52b8c3d7b323d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560633"
---
# <a name="create-a-requisition-for-consumption"></a><span data-ttu-id="a883c-103">إنشاء طلب للاستهلاك</span><span class="sxs-lookup"><span data-stu-id="a883c-103">Create a requisition for consumption</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a883c-104">يوضح لك هذا الإجراء عملية إنشاء طلب.</span><span class="sxs-lookup"><span data-stu-id="a883c-104">This procedure walks you through the process of creating a requisition.</span></span> <span data-ttu-id="a883c-105">وهو يوضح لك الطرق المختلفة للبحث عن المنتجات في كتالوج التدبير وكيفية إضافة منتج غير موجودة في الكتالوج.</span><span class="sxs-lookup"><span data-stu-id="a883c-105">It shows you different ways to search for products in your procurement catalog and how to add a product that isn’t in your catalog.</span></span> <span data-ttu-id="a883c-106">قبل البدء في هذا الإجراء، يجب أن يكون لديك نهج شراء تم إعداد الاستهلاك به كنوع الطلب الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="a883c-106">Before you start this procedure, you must have a purchasing policy set up with Consumption as the default type of requisition.</span></span> <span data-ttu-id="a883c-107">يمكنك استعراض هذا الإجراء في شركة بيانات العرض التوضيحي USMF، أو باستخدام البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="a883c-107">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="a883c-108">لا يمكن تنفيذ الإجراء إلا بواسطة بملف تعريف مستخدم تم إعداده كعامل.</span><span class="sxs-lookup"><span data-stu-id="a883c-108">The procedure can only be carried out by a user profile that is set up as worker.</span></span>  <span data-ttu-id="a883c-109">عادة ما يتم تنفيذ هذه المهمة بواسطة أحد الموظفين.</span><span class="sxs-lookup"><span data-stu-id="a883c-109">This task would normally be carried out by an employee.</span></span> <span data-ttu-id="a883c-110">سيتيح لك دور أمان التوظيف للموظف تنفيذ المهام، أو إذا كنت تستخدم USMF، يجب تسجيل الدخول إلى Alicia.</span><span class="sxs-lookup"><span data-stu-id="a883c-110">The Employee employ security role will allow you to carry out the tasks, or if you’re using USMF, you can log in as Alicia.</span></span>


## <a name="create-a-new-requisition"></a><span data-ttu-id="a883c-111">إنشاء طلب جديد</span><span class="sxs-lookup"><span data-stu-id="a883c-111">Create a new requisition</span></span>
1. <span data-ttu-id="a883c-112">انتقل إلى التدبير والتوريد > طلبات الشراء > طلبات الشراء التي أعددتُها.</span><span class="sxs-lookup"><span data-stu-id="a883c-112">Go to Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me.</span></span>
2. <span data-ttu-id="a883c-113">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="a883c-113">Click New.</span></span>
3. <span data-ttu-id="a883c-114">في الحقل "الاسم"، حدد اسمًا للطلب.</span><span class="sxs-lookup"><span data-stu-id="a883c-114">In the Name field, give the requisition a name.</span></span>
4. <span data-ttu-id="a883c-115">في الحقل "تاريخ الطلب، أدخل تاريخاً.</span><span class="sxs-lookup"><span data-stu-id="a883c-115">In the Requested date field, enter a date.</span></span>
    * <span data-ttu-id="a883c-116">بشكل افتراضي، يُنسخ التاريخ المطلوب والتاريخ المحاسبي لبنود طلب الشراء.</span><span class="sxs-lookup"><span data-stu-id="a883c-116">By default, the requested date and accounting date are copied to the purchase requisition lines.</span></span> <span data-ttu-id="a883c-117">يمكن أن تتغير على مستوى البند.</span><span class="sxs-lookup"><span data-stu-id="a883c-117">They can be changed at the line level.</span></span> <span data-ttu-id="a883c-118">التاريخ المطلوب هو تاريخ التسليم المطلوب.</span><span class="sxs-lookup"><span data-stu-id="a883c-118">The requested date is the requested delivery date.</span></span>  
5. <span data-ttu-id="a883c-119">في الحقل "تاريخ المحاسبة" أدخل تاريخاً.</span><span class="sxs-lookup"><span data-stu-id="a883c-119">In the Accounting date field, enter a date.</span></span>
    * <span data-ttu-id="a883c-120">يتم استخدام التاريخ المحاسبي لتسجيل القيد المحاسبي في دفتر الأستاذ العام، وللتحقق من صحة ما إذا كانت الاعتمادات المالية متاحة أم لا.</span><span class="sxs-lookup"><span data-stu-id="a883c-120">The accounting date is used to record the accounting entry in the general ledger, and to validate whether budget funds are available.</span></span>  
6. <span data-ttu-id="a883c-121">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="a883c-121">Click OK.</span></span>
7. <span data-ttu-id="a883c-122">في الحقل "السبب"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="a883c-122">In the Reason field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a883c-123">بشكل افتراضي، يظهر سبب تبرير العمل الذي قمت بتحديده لبنود طلب الشراء، ولكن يمكنك تغييره على مستوى البند.</span><span class="sxs-lookup"><span data-stu-id="a883c-123">By default, the business justification reason that you select appears for the purchase requisition lines, but you can change it at the line level.</span></span>    
8. <span data-ttu-id="a883c-124">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="a883c-124">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="a883c-125">تحديد السبب</span><span class="sxs-lookup"><span data-stu-id="a883c-125">Select the reason</span></span>
10. <span data-ttu-id="a883c-126">في حقل "التفاصيل" أدخل مبررات أكثر وصفية للطلب</span><span class="sxs-lookup"><span data-stu-id="a883c-126">In the details field enter a more descriptive justification for the requisition</span></span>

## <a name="add-a-line-to-the-requisition"></a><span data-ttu-id="a883c-127">إضافة بند إلى الطلب</span><span class="sxs-lookup"><span data-stu-id="a883c-127">Add a line to the requisition</span></span>
1. <span data-ttu-id="a883c-128">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="a883c-128">Click Add line.</span></span>
    * <span data-ttu-id="a883c-129">هناك طريقتان لإضافة بنود إلى طلب الشراء.</span><span class="sxs-lookup"><span data-stu-id="a883c-129">There are two ways of adding lines to the purchase requisition.</span></span> <span data-ttu-id="a883c-130">إذا كنت تعرف رقم المنتج بالفعل أو كنت تعرف فعلا أنك تطلب منتجًا غير موجود في كتالوج المنتجات، فيمكنك إضافة البند مباشرة باستخدام الخيار "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="a883c-130">If you already know the product number or you already  know that you are requesting a product that is not in the product catalog, then you can add the line directly with "Add line".</span></span> <span data-ttu-id="a883c-131">والطريقة الأخرى هي استخدام "إضافة منتجات" حيث يمكنك استخدام البحث والتصفية للبحث عن أصناف في كتالوج المنتجات.</span><span class="sxs-lookup"><span data-stu-id="a883c-131">The other way is to use "Add products" where you can use searching and filtering to find items in the product catalog.</span></span>    
2. <span data-ttu-id="a883c-132">انقر فوق الصف الذي قمت بإنشائه للتو.</span><span class="sxs-lookup"><span data-stu-id="a883c-132">Click on the row you just created.</span></span>
    * <span data-ttu-id="a883c-133">الطالب هو العامل الذي قام بطلب الطلب.</span><span class="sxs-lookup"><span data-stu-id="a883c-133">The requester is the worker that has requested the requisition.</span></span>   
    * <span data-ttu-id="a883c-134">بشكل افتراضي، يكون الشخص الذي يجهز الطلب هو العامل الذي طلبه.</span><span class="sxs-lookup"><span data-stu-id="a883c-134">By default the person preparing the requisition is the worker who has requested it.</span></span> <span data-ttu-id="a883c-135">يجب عليك الحصول على إذن لإعداد بند طلب نيابة عن عامل آخر.</span><span class="sxs-lookup"><span data-stu-id="a883c-135">You have to be given permission to prepare a requisition line on behalf of another worker.</span></span> <span data-ttu-id="a883c-136">إذا كانت لديك هذه الأذونات، فسيتم عرض العاملين آخرين في هذا البحث.</span><span class="sxs-lookup"><span data-stu-id="a883c-136">If you have such permissions then the other workers will show up in this lookup.</span></span>  
3. <span data-ttu-id="a883c-137">في الحقل "رقم الصنف" اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="a883c-137">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="a883c-138">تتقيد العناصر المتوفرة للاختيار بسياسة الوصول إلى الكتالوج وكتالوج للكيان القانوني للشراء.</span><span class="sxs-lookup"><span data-stu-id="a883c-138">The items that are available for you to choose are limited by the category access policy and the procurement catalog for the buying legal entity.</span></span>   
4. <span data-ttu-id="a883c-139">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="a883c-139">In the Quantity field, enter a number.</span></span>

## <a name="add-more-products-to-the-requisition"></a><span data-ttu-id="a883c-140">إضافة المزيد من منتجات إلى الطلب</span><span class="sxs-lookup"><span data-stu-id="a883c-140">Add more products to the requisition</span></span>
1. <span data-ttu-id="a883c-141">انقر فوق "إضافة المنتجات".</span><span class="sxs-lookup"><span data-stu-id="a883c-141">Click Add products.</span></span>
    * <span data-ttu-id="a883c-142">هذا هو الخيار الذي يمكنك من خلاله البحث عن المنتجات في كتالوج المنتجات.</span><span class="sxs-lookup"><span data-stu-id="a883c-142">This is the option where you can search for products in the product catalog.</span></span>    
2. <span data-ttu-id="a883c-143">في الحقل "البحث عن عقدة التدبير"، اكتب الجزء الأول من اسم الفئة التي تبحث عنها، ثم انقر فوق "إدخال".</span><span class="sxs-lookup"><span data-stu-id="a883c-143">In the Find procurement category node field, type the first part of the name of the category that you are looking for, and then click Enter.</span></span>
    * <span data-ttu-id="a883c-144">على سبيل المثال، اكتب حاسب.</span><span class="sxs-lookup"><span data-stu-id="a883c-144">For example, type comput.</span></span>  
3. <span data-ttu-id="a883c-145">استخدم الاختصار InvokeDefaultButton.</span><span class="sxs-lookup"><span data-stu-id="a883c-145">Use the InvokeDefaultButton shortcut.</span></span>
4. <span data-ttu-id="a883c-146">استخدم عامل التصفية لتصفية قائمة المنتجات في الفئة المحددة.</span><span class="sxs-lookup"><span data-stu-id="a883c-146">Use the Filter to filter the list of products in the selected category.</span></span>
5. <span data-ttu-id="a883c-147">حدد بطاقة المنتج الذين تريد إضافتها للطلب.</span><span class="sxs-lookup"><span data-stu-id="a883c-147">Select the product card that you want to add to the requisition.</span></span>
6. <span data-ttu-id="a883c-148">انقر فوق "إضافة إلى البنود".</span><span class="sxs-lookup"><span data-stu-id="a883c-148">Click Add to lines.</span></span>
7. <span data-ttu-id="a883c-149">في الحقل "الكمية"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="a883c-149">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="a883c-150">في الحقل "البحث عن عقدة التدبير"، اكتب الجزء الأول من اسم الفئة التي تبحث عنها، ثم انقر فوق "إدخال".</span><span class="sxs-lookup"><span data-stu-id="a883c-150">In the Find procurement category node field, type the first part of the name of the category that you are looking for, and then click Enter.</span></span>
    * <span data-ttu-id="a883c-151">على سبيل المثال، اكتب قلم تم (أقلام التمييز).</span><span class="sxs-lookup"><span data-stu-id="a883c-151">For example, type High (highlighters).</span></span>  
9. <span data-ttu-id="a883c-152">استخدم الاختصار InvokeDefaultButton.</span><span class="sxs-lookup"><span data-stu-id="a883c-152">Use the InvokeDefaultButton shortcut.</span></span>
10. <span data-ttu-id="a883c-153">انقر فوق "إضافة منتج غير مدرج في القائمة للبنود" لإضافة منتج غير مدرج في القائمة في كتالوج التدبير.</span><span class="sxs-lookup"><span data-stu-id="a883c-153">Click Add unlisted product to lines to add a product that’s not listed in the procurement catalog.</span></span>
11. <span data-ttu-id="a883c-154">في الحقل "اسم المنتج"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="a883c-154">In the Product name field, type a value.</span></span>
12. <span data-ttu-id="a883c-155">في الحقل "الوحدة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="a883c-155">In the Unit field, type a value.</span></span>
13. <span data-ttu-id="a883c-156">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="a883c-156">Click OK.</span></span>
14. <span data-ttu-id="a883c-157">في الحقل "وصف الصنف"، أضف وصفًا للمنتج.</span><span class="sxs-lookup"><span data-stu-id="a883c-157">In the Item description field, add a description of the product.</span></span>
15. <span data-ttu-id="a883c-158">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="a883c-158">In the Quantity field, enter a number.</span></span>
16. <span data-ttu-id="a883c-159">في حقل "سعر الوحدة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="a883c-159">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="a883c-160">إذا كنت تعرف السعر لمورد معين (السعر الذي تحدده في الحقل "حساب المورد") ثم يمكن إدخال هذا السعر</span><span class="sxs-lookup"><span data-stu-id="a883c-160">If you know the price for a particular vendor (that you select in the vendor account field) then that price can be entered</span></span>   
17. <span data-ttu-id="a883c-161">في الحقل "حساب المورّد‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="a883c-161">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a883c-162">يعتمد الموردون المتوفرون في هذا الحقل على سياسات الشراء وحالة المورد بالنسبة لفئة التدبير الحالية.</span><span class="sxs-lookup"><span data-stu-id="a883c-162">The vendors that are available in this field depend on the purchasing policies and the status that the vendor has for the current procurement category.</span></span> <span data-ttu-id="a883c-163">وكبديل لتحديد مورد هنا، يمكنك النقر فوق الزر "اقتراح مورد".</span><span class="sxs-lookup"><span data-stu-id="a883c-163">As an alternative to selecting a vendor here, you can click the Suggest vendor button.</span></span>    
18. <span data-ttu-id="a883c-164">في القائمة، حدد المورد الذي تريد استخدامه.</span><span class="sxs-lookup"><span data-stu-id="a883c-164">In the list, select the vendor you want to use.</span></span>
19. <span data-ttu-id="a883c-165">في الحقل "رقم الصنف الخارجي" اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="a883c-165">In the External item number field, type a value.</span></span>
    * <span data-ttu-id="a883c-166">وهذا رقم مرجعي للمنتج الذي يعرف بواسطة المورد.</span><span class="sxs-lookup"><span data-stu-id="a883c-166">This is a reference number for the product that is known by the vendor.</span></span> <span data-ttu-id="a883c-167">على سبيل المثال، قد يكون هذا رقم الصنف الخاص بالمنتج في كتالوج المورد الخاص.</span><span class="sxs-lookup"><span data-stu-id="a883c-167">For example, this could be the item number of the product in the vendor's own catalog.</span></span>  
20. <span data-ttu-id="a883c-168">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="a883c-168">Click OK.</span></span>

## <a name="distribute-amounts"></a><span data-ttu-id="a883c-169">توزيع المبالغ</span><span class="sxs-lookup"><span data-stu-id="a883c-169">Distribute amounts</span></span>
1. <span data-ttu-id="a883c-170">انقر فوق "الماليات‬".</span><span class="sxs-lookup"><span data-stu-id="a883c-170">Click Financials.</span></span>
2. <span data-ttu-id="a883c-171">انقر فوق "توزيع المبالغ".</span><span class="sxs-lookup"><span data-stu-id="a883c-171">Click Distribute amounts.</span></span>
    * <span data-ttu-id="a883c-172">توضح هذه العملية كيفية توزيع التكلفة للبند الأول بين حسابين.</span><span class="sxs-lookup"><span data-stu-id="a883c-172">This process shows you how to distribute the cost for the first line between 2 accounts.</span></span> <span data-ttu-id="a883c-173">كما يمكن إجراء ذلك لاحقاً عندما يكون الطلب قيد المراجعة.</span><span class="sxs-lookup"><span data-stu-id="a883c-173">This can also be done later when the requisition is in review.</span></span>  
3. <span data-ttu-id="a883c-174">انقر فوق "تقسيم" لإنشاء بند توزيع جديد.</span><span class="sxs-lookup"><span data-stu-id="a883c-174">Click Split to create a new distribution line.</span></span>
4. <span data-ttu-id="a883c-175">في الحقل "حساب دفتر الأستاذ" حدد مركز التكلفة الأول الذي ينبغي أن يخصص له جزء من التكلفة.</span><span class="sxs-lookup"><span data-stu-id="a883c-175">In the Ledger account field select the first cost center that should take part of the cost.</span></span>
5. <span data-ttu-id="a883c-176">حدد "بند التوزيع الآخر".</span><span class="sxs-lookup"><span data-stu-id="a883c-176">Select the other distribution line.</span></span>
6. <span data-ttu-id="a883c-177">في الحقل "حساب دفتر الأستاذ" حدد مركز التكلفة الآخر.</span><span class="sxs-lookup"><span data-stu-id="a883c-177">In the Ledger account field specify the other cost center.</span></span>
7. <span data-ttu-id="a883c-178">انقر فوق "التوزيع بشكل متساوٍ".</span><span class="sxs-lookup"><span data-stu-id="a883c-178">Click Distribute equally.</span></span>
8. <span data-ttu-id="a883c-179">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a883c-179">Close the page.</span></span>

## <a name="view-line-details"></a><span data-ttu-id="a883c-180">عرض تفاصيل البند</span><span class="sxs-lookup"><span data-stu-id="a883c-180">View line details</span></span>
1. <span data-ttu-id="a883c-181">بدّل توسيع المقطع "تفاصيل البنود‬‬".</span><span class="sxs-lookup"><span data-stu-id="a883c-181">Toggle the expansion of the Line details section.</span></span>

## <a name="submit-the-requisition"></a><span data-ttu-id="a883c-182">إرسال الطلب</span><span class="sxs-lookup"><span data-stu-id="a883c-182">Submit the requisition</span></span>
1. <span data-ttu-id="a883c-183">انقر فوق "سير العمل" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="a883c-183">Click Workflow to open the drop dialog.</span></span>
2. <span data-ttu-id="a883c-184">انقر فوق تقديم.</span><span class="sxs-lookup"><span data-stu-id="a883c-184">Click Submit.</span></span>
3. <span data-ttu-id="a883c-185">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a883c-185">Close the page.</span></span>
4. <span data-ttu-id="a883c-186">في الحقل "التعليق"، اكتب ملاحظة للموافق على الطلب.</span><span class="sxs-lookup"><span data-stu-id="a883c-186">In the Comment field, type a note for the approver of the requisition.</span></span>
5. <span data-ttu-id="a883c-187">انقر فوق تقديم.</span><span class="sxs-lookup"><span data-stu-id="a883c-187">Click Submit.</span></span>
6. <span data-ttu-id="a883c-188">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a883c-188">Close the page.</span></span>
7. <span data-ttu-id="a883c-189">قم بتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a883c-189">Refresh the page.</span></span>

