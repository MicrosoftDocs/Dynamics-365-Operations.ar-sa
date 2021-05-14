---
title: إنشاء نموذج تكوين منتج
description: يوضح هذا الإجراء كيفية إنشاء نموذج تكوين منتج وإدخال المعلومات الأساسية مثل السمات والمكونات الفرعية.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2cb9e33d7bab6ca9cd378ec40baa796d1a933ece
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921355"
---
# <a name="create-a-product-configuration-model"></a><span data-ttu-id="1d23b-103">إنشاء نموذج تكوين منتج</span><span class="sxs-lookup"><span data-stu-id="1d23b-103">Create a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1d23b-104">يوضح هذا الإجراء كيفية إنشاء نموذج تكوين منتج وإدخال المعلومات الأساسية مثل السمات والمكونات الفرعية.</span><span class="sxs-lookup"><span data-stu-id="1d23b-104">This procedure shows how to create a product configuration model and enter basic information such as attributes and subcomponents.</span></span> <span data-ttu-id="1d23b-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="1d23b-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-model"></a><span data-ttu-id="1d23b-106">إنشاء طراز منتج</span><span class="sxs-lookup"><span data-stu-id="1d23b-106">Create a product model</span></span>

1. <span data-ttu-id="1d23b-107">انتقل إلى **إدارة معلومات المنتج \> المنتجات \> نماذج تكوين المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="1d23b-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="1d23b-108">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="1d23b-108">Select **New**.</span></span>
1. <span data-ttu-id="1d23b-109">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1d23b-109">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="1d23b-110">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1d23b-110">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="1d23b-111">في حقل **إستراتيجية الحلول**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="1d23b-111">In the **Solver strategy** field, select an option.</span></span>
    * <span data-ttu-id="1d23b-112">تحدد إستراتيجية الحلول كيفية معالجة القيود في نموذج تكوين منتج يستند إلى القيود".</span><span class="sxs-lookup"><span data-stu-id="1d23b-112">The solver strategy determines how the constraints in a constraint-based product configuration model are processed.</span></span> <span data-ttu-id="1d23b-113">قد يؤثر هذا التحديد على أداء نموذج تكوين المنتج.</span><span class="sxs-lookup"><span data-stu-id="1d23b-113">This selection can have an impact on the performance of the product configuration model.</span></span>  
1. <span data-ttu-id="1d23b-114">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1d23b-114">In the **Name** field, type a value.</span></span>
    * <span data-ttu-id="1d23b-115">يمثل عنصر الجذر نموذج تكوين المنتج، ولكن يمكن استخدامه أيضًا في نماذج المنتجات الأخرى.</span><span class="sxs-lookup"><span data-stu-id="1d23b-115">The root component represents the product configuration model, but it can also be used in other product models.</span></span>  
1. <span data-ttu-id="1d23b-116">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="1d23b-116">Select **OK**.</span></span>
1. <span data-ttu-id="1d23b-117">في حقل **إعادة استخدام التكوينات**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="1d23b-117">In the **Reuse configurations** field, select an option.</span></span>
    * <span data-ttu-id="1d23b-118">إذا تم تعيين معلمة تكوينات إعادة الاستخدام على "نعم"، سيتحقق النظام من التكوينات المتطابقة بعد كل جلسة عمل تكوين ويعيد استخدامها إذا تم العثور على تطابق تام.</span><span class="sxs-lookup"><span data-stu-id="1d23b-118">If the reuse configurations parameter is set to Yes, the system will check for identical configurations after each configuration session and reuse if an exact match is found.</span></span>  

## <a name="add-attributes"></a><span data-ttu-id="1d23b-119">إضافة سمات</span><span class="sxs-lookup"><span data-stu-id="1d23b-119">Add attributes</span></span>

1. <span data-ttu-id="1d23b-120">قم بتوسيع قسم **السمات**.</span><span class="sxs-lookup"><span data-stu-id="1d23b-120">Expand the **Attributes** section.</span></span>
2. <span data-ttu-id="1d23b-121">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="1d23b-121">Select **Add**.</span></span>
3. <span data-ttu-id="1d23b-122">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="1d23b-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="1d23b-123">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1d23b-123">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="1d23b-124">في حقل **اسم الحل**، أدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="1d23b-124">In the **Solver name** field, type a value.</span></span>
    * <span data-ttu-id="1d23b-125">يُستخدم اسم الحل بواسطة أداة حل القيود لمكون المنتج.</span><span class="sxs-lookup"><span data-stu-id="1d23b-125">The solver name is used by the constraint solver of the product configurator.</span></span> <span data-ttu-id="1d23b-126">يجب أن لا تتضمن مسافات أو أحرف خاصة ما عدا _ (الشرطة السفلية).</span><span class="sxs-lookup"><span data-stu-id="1d23b-126">It must not include spaces or special characters except _ (underscore).</span></span>  
6. <span data-ttu-id="1d23b-127">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1d23b-127">In the **Description** field, type a value.</span></span>
    * <span data-ttu-id="1d23b-128">يُعرض نص الوصف لمستخدم تكوين ومن ثم يعمل كمساعدة في تحديد قيمة السمة المناسبة.</span><span class="sxs-lookup"><span data-stu-id="1d23b-128">The description text is displayed to the configuration user and can therefore serve as help in selecting the right attribute value.</span></span>  
7. <span data-ttu-id="1d23b-129">في حقل **نوع السمة**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="1d23b-129">In the **Attribute type** field, enter or select a value.</span></span>
    * <span data-ttu-id="1d23b-130">يحدد نوع السمة القيم المتوفرة للسمة.</span><span class="sxs-lookup"><span data-stu-id="1d23b-130">The attribute type determines which values are available for the attribute.</span></span>  
8. <span data-ttu-id="1d23b-131">حدد خانة الاختيار **تضمين في إعادة الاستخدام**.</span><span class="sxs-lookup"><span data-stu-id="1d23b-131">Select the **Include in reuse** check box.</span></span>
    * <span data-ttu-id="1d23b-132">لا يتوفر هذا الخيار إلا عند تحديد خيار "إعادة استخدام التكوينات".</span><span class="sxs-lookup"><span data-stu-id="1d23b-132">This option is only available when the Reuse configurations option is selected.</span></span> <span data-ttu-id="1d23b-133">يعني تضمين السمة في خانة اختيار إعادة الاستخدام أنه سيتم النظر بهذه السمة عندما يبحث النظام عن تطابق تام.</span><span class="sxs-lookup"><span data-stu-id="1d23b-133">Including the attribute in the reuse check box means that this attribute will be considered when the system is looking for an exact match.</span></span>  

## <a name="add-subcomponents"></a><span data-ttu-id="1d23b-134">إضافة المكونات الفرعية</span><span class="sxs-lookup"><span data-stu-id="1d23b-134">Add subcomponents</span></span>

1. <span data-ttu-id="1d23b-135">قم بتوسيع قسم **المكونات الفرعية**.</span><span class="sxs-lookup"><span data-stu-id="1d23b-135">Expand the **Subcomponents** section.</span></span>
2. <span data-ttu-id="1d23b-136">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="1d23b-136">Select **Add**.</span></span>
3. <span data-ttu-id="1d23b-137">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="1d23b-137">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="1d23b-138">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1d23b-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="1d23b-139">في حقل **اسم الحل**، أدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="1d23b-139">In the **Solver name** field, type a value.</span></span>
6. <span data-ttu-id="1d23b-140">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1d23b-140">In the **Description** field, type a value.</span></span>
7. <span data-ttu-id="1d23b-141">في حقل **المكون**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="1d23b-141">In the **Component** field, enter or select a value.</span></span>
    * <span data-ttu-id="1d23b-142">يجب أن يعمل كل مكون فرعي كتعريف لمكون مرجعي.</span><span class="sxs-lookup"><span data-stu-id="1d23b-142">Each subcomponent must reference a component definition.</span></span> <span data-ttu-id="1d23b-143">يدعم هذا التصميم المكونات القابلة للاستخدام ويضمن أنه بمجرد تحديد مكون، يمكن استخدامه في العديد من نماذج المنتج.</span><span class="sxs-lookup"><span data-stu-id="1d23b-143">This design supports reusable components and ensures that once a component has been defined it can be used in many product models.</span></span>  
8. <span data-ttu-id="1d23b-144">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="1d23b-144">Select **Save**.</span></span>
9. <span data-ttu-id="1d23b-145">حدد **تفاصيل بند قائمة مكونات الصنف**.</span><span class="sxs-lookup"><span data-stu-id="1d23b-145">Select **BOM line details**.</span></span>
    * <span data-ttu-id="1d23b-146">يتيح نموذج تفاصيل بند قائمة مكونات الصنف‬ للمستخدم تحديد الخصائص المطلوبة للمكون الفرعي.</span><span class="sxs-lookup"><span data-stu-id="1d23b-146">The BOM line details form enables the user to select the required properties for the subcomponent.</span></span> <span data-ttu-id="1d23b-147">ويمكن تحديد قيمة ثابتة لكل خاصية أو تعيينها إلى سمة.</span><span class="sxs-lookup"><span data-stu-id="1d23b-147">Each property can be given a fixed value or mapped to an attribute.</span></span> <span data-ttu-id="1d23b-148">يؤدي التعيين إلى سمة ما في حصول خاصية بند قائمة مكونات الصنف على قيم مختلفة وفقًا لتحديد التكوين.</span><span class="sxs-lookup"><span data-stu-id="1d23b-148">Mapping to an attribute will result in the BOM line property getting different values depending on the configuration selection.</span></span>  
10. <span data-ttu-id="1d23b-149">في الحقل **رقم الصنف**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="1d23b-149">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="1d23b-150">يمثل كل مكون فرعي أصل المنتج القابلة للتكوين باستخدام تقنية التكوين المستند إلى قيد.</span><span class="sxs-lookup"><span data-stu-id="1d23b-150">Each subcomponent represents a configurable product master with constraint-based configuration technology.</span></span> <span data-ttu-id="1d23b-151">يتم إنشاء المرجع من خلال رقم الصنف.</span><span class="sxs-lookup"><span data-stu-id="1d23b-151">The reference is made through the item number.</span></span>  
11. <span data-ttu-id="1d23b-152">حدد خانة الاختيار **تعيين**.</span><span class="sxs-lookup"><span data-stu-id="1d23b-152">Select the **Set** check box.</span></span>
12. <span data-ttu-id="1d23b-153">حدد **نعم** في حقل **الحساب**.</span><span class="sxs-lookup"><span data-stu-id="1d23b-153">Select **Yes** in the **Calculation** field.</span></span>
    * <span data-ttu-id="1d23b-154">يضمن تعيين خيار الحساب أن المنتج سيتم تضمينه عند تشغيل حساب تكلفة للمنتج.</span><span class="sxs-lookup"><span data-stu-id="1d23b-154">Setting the calculation option ensures that the product will be included when running a cost calculation for the product.</span></span>  
13. <span data-ttu-id="1d23b-155">حدد علامة التبويب **الإعداد**.</span><span class="sxs-lookup"><span data-stu-id="1d23b-155">Select the **Setup** tab.</span></span>
14. <span data-ttu-id="1d23b-156">حدد خانة الاختيار **تعيين**.</span><span class="sxs-lookup"><span data-stu-id="1d23b-156">Select the **Set** check box.</span></span>
15. <span data-ttu-id="1d23b-157">في الحقل **الكمية**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="1d23b-157">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="1d23b-158">يحدد الحقل "الكمية" كمية هذا المنتج التي سيتم استهلاكها في المنتج المكون.</span><span class="sxs-lookup"><span data-stu-id="1d23b-158">The quantity field determines how much of this product will be consumed in the configured product.</span></span>  
16. <span data-ttu-id="1d23b-159">حدد خانة الاختيار **تعيين**.</span><span class="sxs-lookup"><span data-stu-id="1d23b-159">Select the **Set** check box.</span></span>
17. <span data-ttu-id="1d23b-160">في حقل **حسب السلسلة**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="1d23b-160">In the **Per series** field, enter a number.</span></span>
18. <span data-ttu-id="1d23b-161">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="1d23b-161">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]