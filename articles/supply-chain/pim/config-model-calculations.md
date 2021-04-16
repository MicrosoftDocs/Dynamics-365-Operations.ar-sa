---
title: حسابات نموذج تكوين المنتج
description: يصف هذا الموضوع كيفية إنشاء عمليات حسابية للسمات في نموذج تكوين المنتج
author: t-benebo
ms.date: 03/18/2021
ms.topic: article
ms.search.form: PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-18
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: eaf6264f060d33575740ad38e7a65158baba296b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829608"
---
# <a name="product-configuration-model-calculations"></a><span data-ttu-id="df6b5-103">حسابات نموذج تكوين المنتج</span><span class="sxs-lookup"><span data-stu-id="df6b5-103">Product configuration model calculations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="df6b5-104">يصف هذا الموضوع كيفية إنشاء عمليات حسابية للسمات في نموذج تكوين المنتج.</span><span class="sxs-lookup"><span data-stu-id="df6b5-104">This topic describes how to create calculations for attributes in a product configuration model.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="df6b5-105">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="df6b5-105">Prerequisites</span></span>

<span data-ttu-id="df6b5-106">يتم استخدام العمليات الحسابية بنموذج تكوين منتج لحساب قيم التكوين لمنتج.</span><span class="sxs-lookup"><span data-stu-id="df6b5-106">Calculations are used in a product configuration model to calculate the configuration values for a product.</span></span> <span data-ttu-id="df6b5-107">قبل أن تتمكن من البدء في إعداد الحسابات، يجب أن يكون نموذج تكوين المنتج ذي الصلة موجودًا.</span><span class="sxs-lookup"><span data-stu-id="df6b5-107">Before you can start to set up calculations, the related product configuration model must exist.</span></span> <span data-ttu-id="df6b5-108">للحصول على نظرة عامة على عملية الإعداد لنماذج التكوين والمهام ذات الصلة، راجع [إعداد نموذج تكوين المنتج](set-up-maintain-product-configuration-model.md).</span><span class="sxs-lookup"><span data-stu-id="df6b5-108">For an overview of the setup process for configuration models and the related tasks, see [Set up a product configuration model](set-up-maintain-product-configuration-model.md).</span></span>

## <a name="create-a-calculation"></a><span data-ttu-id="df6b5-109">إنشاء عملية حسابية</span><span class="sxs-lookup"><span data-stu-id="df6b5-109">Create a calculation</span></span>

<span data-ttu-id="df6b5-110">تتكون العملية الحسابية من تعبير وسمة هدف.</span><span class="sxs-lookup"><span data-stu-id="df6b5-110">A calculation consists of an expression and a target attribute.</span></span> <span data-ttu-id="df6b5-111">لمزيد من المعلومات، راجع [أسئلة شائعة حول حسابات نماذج تكوين المنتج](calculate-product-configuration-models.md).</span><span class="sxs-lookup"><span data-stu-id="df6b5-111">For more information, see [Calculations for product configuration models FAQ](calculate-product-configuration-models.md).</span></span>

<span data-ttu-id="df6b5-112">لإنشاء حساب لنموذج منتج موجود، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="df6b5-112">To create a calculation for an existing product model, follow these steps.</span></span>

1. <span data-ttu-id="df6b5-113">انتقل إلى **إدارة معلومات المنتج \> عام \>  نماذج تكوين المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="df6b5-113">Go to **Product information management \> Common \> Product configuration models**.</span></span>
1. <span data-ttu-id="df6b5-114">افتح نموذج تكوين منتج، ثم حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="df6b5-114">Open a product configuration model, and then select **Edit**.</span></span>
1. <span data-ttu-id="df6b5-115">في علامة التبويب السريعة **العمليات الحسابية**، حدد **إضافة** لإضافة عملية حسابية، ثم عيِّن الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="df6b5-115">On the **Calculations** FastTab, select **Add** to add a calculation, and then set the following fields:</span></span>

    - <span data-ttu-id="df6b5-116">**الاسم‏‎** – أدخل اسمًا للعملية الحسابية.</span><span class="sxs-lookup"><span data-stu-id="df6b5-116">**Name** – Enter a name for the calculation.</span></span>
    - <span data-ttu-id="df6b5-117">**الوصف** - أدخل وصفًا للعملية الحسابية.</span><span class="sxs-lookup"><span data-stu-id="df6b5-117">**Description** – Enter a description of the calculation.</span></span>
    - <span data-ttu-id="df6b5-118">**السمة الهدف** - حدد السمة التي تقوم باجراء الحساب لها.</span><span class="sxs-lookup"><span data-stu-id="df6b5-118">**Target attribute** – Select the attribute that you're making the calculation for.</span></span>

1. <span data-ttu-id="df6b5-119">حدد **تحرير التعبير**.</span><span class="sxs-lookup"><span data-stu-id="df6b5-119">Select **Edit expression**.</span></span>
1. <span data-ttu-id="df6b5-120">في مربع الحوار **إدخال حساب**، أضف السمات والعوامل والقيم المطلوبة إلى التعبير.</span><span class="sxs-lookup"><span data-stu-id="df6b5-120">In the **Enter a calculation** dialog box, add the required attributes, operators, and values to the expression.</span></span> <span data-ttu-id="df6b5-121">لمزيد من المعلومات حول كيفية التعامل مع هذه العناصر، راجع [قيود التعبير وقيود الجدول في نماذج تكوين المنتجات](expression-constraints-table-constraints-product-configuration-models.md).</span><span class="sxs-lookup"><span data-stu-id="df6b5-121">For more information about how to work with these elements, see [Expression constraints and table constraints in product configuration models](expression-constraints-table-constraints-product-configuration-models.md).</span></span>
1. <span data-ttu-id="df6b5-122">عندما يكون التعبير الخاص بك جاهزًا، حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="df6b5-122">When your expression is ready, select **OK**.</span></span>

## <a name="calculation-examples"></a><span data-ttu-id="df6b5-123">أمثلة العمليات الحسابية</span><span class="sxs-lookup"><span data-stu-id="df6b5-123">Calculation examples</span></span>

<span data-ttu-id="df6b5-124">يوفر هذا القسم بعض الامثله التي تعرض كيفيه عمل الحسابات.</span><span class="sxs-lookup"><span data-stu-id="df6b5-124">This section provides a few examples that show how calculations work.</span></span>

### <a name="example-1"></a><span data-ttu-id="df6b5-125">مثال1</span><span class="sxs-lookup"><span data-stu-id="df6b5-125">Example 1</span></span>

<span data-ttu-id="df6b5-126">السمة الهدف هي قيمة منطقية، ويستخدم الحساب التعبير الشرطي التالي:</span><span class="sxs-lookup"><span data-stu-id="df6b5-126">The target attribute is Boolean, and the calculation uses the following conditional expression:</span></span>

`If[(decimalAttribute1 / decimalAttribute2) < 1, True, False]`

<span data-ttu-id="df6b5-127">يقوم هذا التعبير بإرجاع قيمة *صواب* للسمة الهدف إذا كانت `decimalAttribute2` أكبر من أو يساوي `decimalAttribute1`.</span><span class="sxs-lookup"><span data-stu-id="df6b5-127">This expression returns a value of *True* to the target attribute if `decimalAttribute2` is greater than or equal to `decimalAttribute1`.</span></span> <span data-ttu-id="df6b5-128">بخلاف ذلك، تقوم بإرجاع قيمة *خطأ*.</span><span class="sxs-lookup"><span data-stu-id="df6b5-128">Otherwise, it returns a value of *False*.</span></span>

### <a name="example-2"></a><span data-ttu-id="df6b5-129">مثال2</span><span class="sxs-lookup"><span data-stu-id="df6b5-129">Example 2</span></span>

<span data-ttu-id="df6b5-130">يستخدم هذا المثال سمة النص `textFixedList` كسمة هدف.</span><span class="sxs-lookup"><span data-stu-id="df6b5-130">This example uses the text attribute `textFixedList` as the target attribute.</span></span> <span data-ttu-id="df6b5-131">تحتوي هذه السمة على القائمة الثابتة التالية.</span><span class="sxs-lookup"><span data-stu-id="df6b5-131">This attribute contains the following fixed list.</span></span>

| <span data-ttu-id="df6b5-132">قيمة</span><span class="sxs-lookup"><span data-stu-id="df6b5-132">Value</span></span> | <span data-ttu-id="df6b5-133">قيمة الحلول</span><span class="sxs-lookup"><span data-stu-id="df6b5-133">Solver value</span></span> |
|---|---|
| <span data-ttu-id="df6b5-134">أ</span><span class="sxs-lookup"><span data-stu-id="df6b5-134">A</span></span> | <span data-ttu-id="df6b5-135">1a</span><span class="sxs-lookup"><span data-stu-id="df6b5-135">1a</span></span> |
| <span data-ttu-id="df6b5-136">B</span><span class="sxs-lookup"><span data-stu-id="df6b5-136">B</span></span> | <span data-ttu-id="df6b5-137">2b</span><span class="sxs-lookup"><span data-stu-id="df6b5-137">2b</span></span> |
| <span data-ttu-id="df6b5-138">C</span><span class="sxs-lookup"><span data-stu-id="df6b5-138">C</span></span> | <span data-ttu-id="df6b5-139">2c</span><span class="sxs-lookup"><span data-stu-id="df6b5-139">2c</span></span> |

<span data-ttu-id="df6b5-140">تظهر اللقطة التالية كيف قد تبدو إعدادات هذه السمة في النظام الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="df6b5-140">The following screenshot shows how the settings for this attribute might look in your system.</span></span>

<span data-ttu-id="df6b5-141">![إعدادات نوع السمة للمثال 2](media/model-calculations-example2.png "إعدادات نوع السمة للمثال 2")</span><span class="sxs-lookup"><span data-stu-id="df6b5-141">![Attribute type settings for example 2](media/model-calculations-example2.png "Attribute type settings for example 2")</span></span>

<span data-ttu-id="df6b5-142">يتم استخدام السمة في العبارة الشرطية التالية:</span><span class="sxs-lookup"><span data-stu-id="df6b5-142">The attribute is used in the following conditional statement:</span></span>

`If[integerAttribute < 150, 0, 2]`

<span data-ttu-id="df6b5-143">إذا كانت `integerAttribute` أقل من 150، تُرجع هذه العبارة القيمة النصية للسجل الأول في القائمة الثابتة، *A*. وبخلاف ذلك، تقوم بإرجاع القيمة النصية للسجل الثالث في القائمة الثابتة، *C*.</span><span class="sxs-lookup"><span data-stu-id="df6b5-143">If `integerAttribute` is less than 150, this statement returns the text value of the first record in the fixed list, *A*. Otherwise, it returns the text value of the third record in the fixed list, *C*.</span></span>

> [!NOTE]
> <span data-ttu-id="df6b5-144">القائمة الثابتة تعادل التعداد الصفري (التعداد)، ويتم الوصول إلى قيمها من خلال قيمة عدد صحيح مناسب.</span><span class="sxs-lookup"><span data-stu-id="df6b5-144">The fixed list is equivalent to a zero-based enumeration (enum), and its values are accessed by the appropriate integer value.</span></span> <span data-ttu-id="df6b5-145">لذلك، تتم مطابقة أول قيمة قائمة ثابتة (*A*) مع *0*، وتتم مطابقة القيمة الثانية (*B*) مع *1*، وتتم مطابقة القيمة الثالثة (*C*) مع *2*.</span><span class="sxs-lookup"><span data-stu-id="df6b5-145">Therefore, the first fixed list value (*A*) is matched to *0*, the second value (*B*) is matched to *1*, and the third value (*C*) is matched to *2*.</span></span>

### <a name="example-3"></a><span data-ttu-id="df6b5-146">المثال الثالث</span><span class="sxs-lookup"><span data-stu-id="df6b5-146">Example 3</span></span>

<span data-ttu-id="df6b5-147">يستخدم هذا المثال سمة النص `textFixedList` من المثال السابق.</span><span class="sxs-lookup"><span data-stu-id="df6b5-147">This example uses the `textFixedList` target attribute from the previous example.</span></span> <span data-ttu-id="df6b5-148">يستخدم أيضًا سمة نص أخرى، `textAttribute`، التي تحتوي علي القائمة الثابتة التالية.</span><span class="sxs-lookup"><span data-stu-id="df6b5-148">It also uses another text attribute, `textAttribute`, that contains the following fixed list.</span></span>

| <span data-ttu-id="df6b5-149">قيمة</span><span class="sxs-lookup"><span data-stu-id="df6b5-149">Value</span></span> | <span data-ttu-id="df6b5-150">قيمة الحلول</span><span class="sxs-lookup"><span data-stu-id="df6b5-150">Solver value</span></span> |
|---|---|
| <span data-ttu-id="df6b5-151">AA</span><span class="sxs-lookup"><span data-stu-id="df6b5-151">AA</span></span> | <span data-ttu-id="df6b5-152">1aa</span><span class="sxs-lookup"><span data-stu-id="df6b5-152">1aa</span></span> |
| <span data-ttu-id="df6b5-153">BB</span><span class="sxs-lookup"><span data-stu-id="df6b5-153">BB</span></span> | <span data-ttu-id="df6b5-154">2bb</span><span class="sxs-lookup"><span data-stu-id="df6b5-154">2bb</span></span> |

<span data-ttu-id="df6b5-155">تظهر اللقطة التالية كيف قد تبدو إعدادات هذه السمة في النظام الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="df6b5-155">The following screenshot shows how the settings for this attribute might look in your system.</span></span>

<span data-ttu-id="df6b5-156">![إعدادات نوع السمة للمثال 3](media/model-calculations-example3.png "إعدادات نوع السمة للمثال 3")</span><span class="sxs-lookup"><span data-stu-id="df6b5-156">![Attribute type settings for example 3](media/model-calculations-example3.png "Attribute type settings for example 3")</span></span>

<span data-ttu-id="df6b5-157">يتم حساب قيمة السمة `textFixedList` باستخدام العبارة الشرطية التالية:</span><span class="sxs-lookup"><span data-stu-id="df6b5-157">The value for the `textFixedList` attribute is calculated by using the following conditional statement:</span></span>

`If[textAttribute == "1aa", 0, 2]`

<span data-ttu-id="df6b5-158">إذا كانت القيمة `textAttribute` تشتمل على قيمة حل تساوي *1aa*، فإن هاذ التعبير يقوم بإرجاع القيمة النصية للسجل الأول في القائمة الثابتة `textFixedList`، *A*. بخلاف ذلك، تقوم بإرجاع القيمة النصية للسجل الثالث في القائمة الثابتة `textFixedList`، *C*.</span><span class="sxs-lookup"><span data-stu-id="df6b5-158">If the `textAttribute` value has a solver value that equals *1aa*, this expression returns the text value of the first record in the `textFixedList` fixed list, *A*. Otherwise, it returns the text value of the third record in the `textFixedList` fixed list, *C*.</span></span>

> [!NOTE]
> - <span data-ttu-id="df6b5-159">يجب ان تستخدم العبارة الشرطية قيمه الحل الخاصة بالسمة</span><span class="sxs-lookup"><span data-stu-id="df6b5-159">The conditional statement must use the solver value of the attribute.</span></span>
> - <span data-ttu-id="df6b5-160">يمكن استخدام سمات نص القائمة الثابتة فقط في العمليات الحسابية.</span><span class="sxs-lookup"><span data-stu-id="df6b5-160">Only fixed-list text attributes can be used in calculations.</span></span>

## <a name="see-also"></a><span data-ttu-id="df6b5-161">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="df6b5-161">See also</span></span>

- [<span data-ttu-id="df6b5-162">‬‏‫الأسئلة المتداولة حول حسابات نماذج تكوين المنتجات</span><span class="sxs-lookup"><span data-stu-id="df6b5-162">Calculations for product configuration models FAQ</span></span>](calculate-product-configuration-models.md)
- [<span data-ttu-id="df6b5-163">إضافة قيد تعبير إلى نموذج تكوين منتج</span><span class="sxs-lookup"><span data-stu-id="df6b5-163">Add an expression constraint to a product configuration model</span></span>](tasks/add-expression-constraint-product-configuration-model.md)
- [<span data-ttu-id="df6b5-164">نظرة عامة على نماذج تكوين المنتجات</span><span class="sxs-lookup"><span data-stu-id="df6b5-164">Product configuration models overview</span></span>](product-configuration-models.md)
