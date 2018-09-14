--- 
title: "إنشاء نموذج تكوين منتج"
description: "يوضح هذا الإجراء كيفية إنشاء نموذج تكوين منتج وإدخال المعلومات الأساسية مثل السمات والمكونات الفرعية."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: a5b3d19c680e14fe4074314a95937d30d4ad2c7a
ms.contentlocale: ar-sa
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-product-configuration-model"></a><span data-ttu-id="1036e-103">إنشاء نموذج تكوين منتج</span><span class="sxs-lookup"><span data-stu-id="1036e-103">Create a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1036e-104">يوضح هذا الإجراء كيفية إنشاء نموذج تكوين منتج وإدخال المعلومات الأساسية مثل السمات والمكونات الفرعية.</span><span class="sxs-lookup"><span data-stu-id="1036e-104">This procedure shows how to create a product configuration model and enter basic information such as attributes and subcomponents.</span></span> <span data-ttu-id="1036e-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="1036e-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-model"></a><span data-ttu-id="1036e-106">إنشاء طراز منتج</span><span class="sxs-lookup"><span data-stu-id="1036e-106">Create a product model</span></span>
1. <span data-ttu-id="1036e-107">انقر فوق "تعريف نموذج متغير المنتج"ز</span><span class="sxs-lookup"><span data-stu-id="1036e-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="1036e-108">انقر فوق "نماذج تكوين المنتجات".</span><span class="sxs-lookup"><span data-stu-id="1036e-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="1036e-109">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="1036e-109">Click New.</span></span>
4. <span data-ttu-id="1036e-110">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1036e-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="1036e-111">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1036e-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="1036e-112">في الحقل "إستراتيجية الحلول"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="1036e-112">In the Solver strategy field, select an option.</span></span>
    * <span data-ttu-id="1036e-113">تحدد إستراتيجية الحلول كيفية معالجة القيود في نموذج تكوين منتج يستند إلى القيود".</span><span class="sxs-lookup"><span data-stu-id="1036e-113">The solver strategy determines how the constraints in a constraint-based product configuration model are processed.</span></span> <span data-ttu-id="1036e-114">قد يؤثر هذا التحديد على أداء نموذج تكوين المنتج.</span><span class="sxs-lookup"><span data-stu-id="1036e-114">This selection can have an impact on the performance of the product configuration model.</span></span>  
7. <span data-ttu-id="1036e-115">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1036e-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="1036e-116">يمثل عنصر الجذر نموذج تكوين المنتج، ولكن يمكن استخدامه أيضًا في نماذج المنتجات الأخرى.</span><span class="sxs-lookup"><span data-stu-id="1036e-116">The root component represents the product configuration model, but it can also be used in other product models.</span></span>  
8. <span data-ttu-id="1036e-117">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="1036e-117">Click OK.</span></span>
9. <span data-ttu-id="1036e-118">في الحقل "إعادة استخدام التكوينات"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="1036e-118">In the Reuse configurations field, select an option.</span></span>
    * <span data-ttu-id="1036e-119">إذا تم تعيين معلمة تكوينات إعادة الاستخدام على "نعم"، سيتحقق النظام من التكوينات المتطابقة بعد كل جلسة عمل تكوين ويعيد استخدامها إذا تم العثور على تطابق تام.</span><span class="sxs-lookup"><span data-stu-id="1036e-119">If the reuse configurations parameter is set to Yes, the system will check for identical configurations after each configuration session and reuse if an exact match is found.</span></span>  

## <a name="add-attributes"></a><span data-ttu-id="1036e-120">إضافة سمات</span><span class="sxs-lookup"><span data-stu-id="1036e-120">Add attributes</span></span>
1. <span data-ttu-id="1036e-121">قم بتوسيع القسم "السمات".</span><span class="sxs-lookup"><span data-stu-id="1036e-121">Expand the Attributes section.</span></span>
2. <span data-ttu-id="1036e-122">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="1036e-122">Click Add.</span></span>
3. <span data-ttu-id="1036e-123">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="1036e-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="1036e-124">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1036e-124">In the Name field, type a value.</span></span>
5. <span data-ttu-id="1036e-125">في الحقل "اسم الحلول"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1036e-125">In the Solver name field, type a value.</span></span>
    * <span data-ttu-id="1036e-126">يُستخدم اسم "الحلول" بواسطة أداة حل القيود لمكون المنتج.</span><span class="sxs-lookup"><span data-stu-id="1036e-126">The Solver name is used by the constraint solver of the product configurator.</span></span> <span data-ttu-id="1036e-127">يجب أن لا تتضمن مسافات أو أحرف خاصة ما عدا _ (الشرطة السفلية).</span><span class="sxs-lookup"><span data-stu-id="1036e-127">It must not include spaces or special characters except _ (underscore).</span></span>  
6. <span data-ttu-id="1036e-128">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1036e-128">In the Description field, type a value.</span></span>
    * <span data-ttu-id="1036e-129">يُعرض نص الوصف لمستخدم تكوين ومن ثم يعمل كمساعدة في تحديد قيمة السمة المناسبة.</span><span class="sxs-lookup"><span data-stu-id="1036e-129">The description text is displayed to the configuration user and can therefore serve as help in selecting the right attribute value.</span></span>  
7. <span data-ttu-id="1036e-130">في الحقل "نوع السمة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="1036e-130">In the Attribute type field, enter or select a value.</span></span>
    * <span data-ttu-id="1036e-131">يحدد نوع السمة القيم المتوفرة للسمة.</span><span class="sxs-lookup"><span data-stu-id="1036e-131">The attribute type determines which values are available for the attribute.</span></span>  
8. <span data-ttu-id="1036e-132">حدد خانة الاختيار "تضمين في إعادة الاستخدام".</span><span class="sxs-lookup"><span data-stu-id="1036e-132">Select the Include in reuse check box.</span></span>
    * <span data-ttu-id="1036e-133">لا يتوفر هذا الخيار إلا عند تحديد خيار "إعادة استخدام التكوينات".</span><span class="sxs-lookup"><span data-stu-id="1036e-133">This option is only available when the Reuse configurations option is selected.</span></span> <span data-ttu-id="1036e-134">يعني تضمين السمة في خانة اختيار إعادة الاستخدام أنه سيتم النظر بهذه السمة عندما يبحث النظام عن تطابق تام.</span><span class="sxs-lookup"><span data-stu-id="1036e-134">Including the attribute in the reuse check box means that this attribute will be considered when the system is looking for an exact match.</span></span>  

## <a name="add-subcomponents"></a><span data-ttu-id="1036e-135">إضافة المكونات الفرعية</span><span class="sxs-lookup"><span data-stu-id="1036e-135">Add subcomponents</span></span>
1. <span data-ttu-id="1036e-136">قم بتوسيع القسم "المكونات الفرعية".</span><span class="sxs-lookup"><span data-stu-id="1036e-136">Expand the Subcomponents section.</span></span>
2. <span data-ttu-id="1036e-137">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="1036e-137">Click Add.</span></span>
3. <span data-ttu-id="1036e-138">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="1036e-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="1036e-139">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1036e-139">In the Name field, type a value.</span></span>
5. <span data-ttu-id="1036e-140">في الحقل "اسم الحلول"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1036e-140">In the Solver name field, type a value.</span></span>
6. <span data-ttu-id="1036e-141">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1036e-141">In the Description field, type a value.</span></span>
7. <span data-ttu-id="1036e-142">في الحقل "المكون"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="1036e-142">In the Component field, enter or select a value.</span></span>
    * <span data-ttu-id="1036e-143">يجب أن يعمل كل مكون فرعي كتعريف لمكون مرجعي.</span><span class="sxs-lookup"><span data-stu-id="1036e-143">Each subcomponent must reference a component definition.</span></span> <span data-ttu-id="1036e-144">يدعم هذا التصميم المكونات القابلة للاستخدام ويضمن أنه بمجرد تحديد مكون، يمكن استخدامه في العديد من نماذج المنتج.</span><span class="sxs-lookup"><span data-stu-id="1036e-144">This design supports reusable components and ensures that once a component has been defined it can be used in many product models.</span></span>  
8. <span data-ttu-id="1036e-145">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="1036e-145">Click Save.</span></span>
9. <span data-ttu-id="1036e-146">انقر فوق "تفاصيل بنود قائمة مكونات الصنف".</span><span class="sxs-lookup"><span data-stu-id="1036e-146">Click BOM line details.</span></span>
    * <span data-ttu-id="1036e-147">يتيح نموذج تفاصيل بند قائمة مكونات الصنف‬ للمستخدم تحديد الخصائص المطلوبة للمكون الفرعي.</span><span class="sxs-lookup"><span data-stu-id="1036e-147">The BOM line details form enables the user to select the required properties for the subcomponent.</span></span> <span data-ttu-id="1036e-148">ويمكن تحديد قيمة ثابتة لكل خاصية أو تعيينها إلى سمة.</span><span class="sxs-lookup"><span data-stu-id="1036e-148">Each property can be given a fixed value or mapped to an attribute.</span></span> <span data-ttu-id="1036e-149">يؤدي التعيين إلى سمة ما في حصول خاصية بند قائمة مكونات الصنف على قيم مختلفة وفقًا لتحديد التكوين.</span><span class="sxs-lookup"><span data-stu-id="1036e-149">Mapping to an attribute will result in the BOM line property getting different values depending on the configuration selection.</span></span>  
10. <span data-ttu-id="1036e-150">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="1036e-150">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="1036e-151">يمثل كل مكون فرعي أصل المنتج القابلة للتكوين باستخدام تقنية التكوين المستند إلى قيد.</span><span class="sxs-lookup"><span data-stu-id="1036e-151">Each subcomponent represents a configurable product master with constraint-based configuration technology.</span></span> <span data-ttu-id="1036e-152">يتم إنشاء المرجع من خلال رقم الصنف.</span><span class="sxs-lookup"><span data-stu-id="1036e-152">The reference is made through the item number.</span></span>  
11. <span data-ttu-id="1036e-153">حدد خانة الاختيار "تعيين".</span><span class="sxs-lookup"><span data-stu-id="1036e-153">Select the Set check box.</span></span>
12. <span data-ttu-id="1036e-154">حدد "نعم" في الحقل "حساب".</span><span class="sxs-lookup"><span data-stu-id="1036e-154">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="1036e-155">يضمن تعيين خيار الحساب أن المنتج سيتم تضمينه عند تشغيل حساب تكلفة للمنتج.</span><span class="sxs-lookup"><span data-stu-id="1036e-155">Setting the calculation option ensures that the product will be included when running a cost calculation for the product.</span></span>  
13. <span data-ttu-id="1036e-156">انقر فوق علامة التبويب "إعداد".</span><span class="sxs-lookup"><span data-stu-id="1036e-156">Click the Setup tab.</span></span>
14. <span data-ttu-id="1036e-157">حدد خانة الاختيار "تعيين".</span><span class="sxs-lookup"><span data-stu-id="1036e-157">Select the Set check box.</span></span>
15. <span data-ttu-id="1036e-158">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="1036e-158">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="1036e-159">يحدد الحقل "الكمية" كمية هذا المنتج التي سيتم استهلاكها في المنتج المكون.</span><span class="sxs-lookup"><span data-stu-id="1036e-159">The quantity field determines how much of this product will be consumed in the configured product.</span></span>  
16. <span data-ttu-id="1036e-160">حدد خانة الاختيار "تعيين".</span><span class="sxs-lookup"><span data-stu-id="1036e-160">Select the Set check box.</span></span>
17. <span data-ttu-id="1036e-161">في الحقل "حسب السلسلة"، ادخل اسمًا.</span><span class="sxs-lookup"><span data-stu-id="1036e-161">In the Per series field, enter a number.</span></span>
18. <span data-ttu-id="1036e-162">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="1036e-162">Click OK.</span></span>


