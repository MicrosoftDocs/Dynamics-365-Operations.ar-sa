---
title: "‬‏‫الأسئلة المتداولة حول حسابات نماذج تكوين المنتجات"
description: "‏‫يوضح هذا الموضوع حسابات نماذج تكوين المنتج وكيفية استخدام الحسابات مع قيود."
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCConstraintEditor, PCProductConfigurationModelDetails, PCRuntimeConfigurator
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19191
ms.assetid: 8993f9a1-d1c0-49f5-afd3-5e1077ded0fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: cfdf90a03da6cfd6c0e7c59f9cae8f9741d8d520
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---

# <a name="calculations-for-product-configuration-models-faq"></a><span data-ttu-id="4e115-103">‬‏‫الأسئلة المتداولة حول حسابات نماذج تكوين المنتجات</span><span class="sxs-lookup"><span data-stu-id="4e115-103">Calculations for product configuration models FAQ</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="4e115-104">‏‫يوضح هذا الموضوع حسابات نماذج تكوين المنتج وكيفية استخدام الحسابات مع قيود.</span><span class="sxs-lookup"><span data-stu-id="4e115-104">This topic describes calculations for product configuration models and explains how to use calculations together with constraints.</span></span>

<span data-ttu-id="4e115-105">يمكن استخدام حسابات للعمليات الحسابية أو المنطقية.</span><span class="sxs-lookup"><span data-stu-id="4e115-105">Calculations can be used for arithmetic or logical operations.</span></span> <span data-ttu-id="4e115-106">وهي تكمل قيود التعبير في نماذج تكوين المنتج.</span><span class="sxs-lookup"><span data-stu-id="4e115-106">They complement expression constraints in product configuration models.</span></span> <span data-ttu-id="4e115-107">ويمكنك تحديد العمليات الحسابية في صفحة **‏‫تفاصيل نموذج تكوين منتج مستند إلى قيد**، ثم إنشاء تعبيرات للحسابات في محرر التعبير.</span><span class="sxs-lookup"><span data-stu-id="4e115-107">You can define calculations on the **Constraint-based product configuration model details** page and then build expressions for the calculations in the expression editor.</span></span> <span data-ttu-id="4e115-108">لمزيد من المعلومات، راجع "إنشاء العمليات الحسابية".</span><span class="sxs-lookup"><span data-stu-id="4e115-108">For more information, see Create calculations.</span></span>

## <a name="what-is-a-calculation"></a><span data-ttu-id="4e115-109">ما الحساب؟</span><span class="sxs-lookup"><span data-stu-id="4e115-109">What is a calculation?</span></span>
<span data-ttu-id="4e115-110">تُوصف العملية الحسابية بأنها عنصر يمكنك استخدامه في نموذج تكوين منتج.</span><span class="sxs-lookup"><span data-stu-id="4e115-110">A calculation is an element that you can use in a product configuration model.</span></span> <span data-ttu-id="4e115-111">وتُكمل العمليات الحسابية القيود عن طريق تمكينك من استخدام الأرقام العشرية لحساب القيم عن تكوين منتج.</span><span class="sxs-lookup"><span data-stu-id="4e115-111">Calculations complement constraints by letting you use decimal numbers to calculate values when you configure a product.</span></span> <span data-ttu-id="4e115-112">بالإضافة إلى ذلك، تشتمل العمليات الحسابية على مجموعة من عوامل التشغيل المتوفرة أكبر من تلك التي تشتمل عليها القيود.</span><span class="sxs-lookup"><span data-stu-id="4e115-112">Additionally, calculations have a larger set of available operators than constraints have.</span></span>  

<span data-ttu-id="4e115-113">مثل القيد، يقترن الحساب بمكون محدد في نموذج تكوين منتج ولا يمكن إعادة استخدامه بواسطة مكون آخر أو مشاركته مع مكون آخر.</span><span class="sxs-lookup"><span data-stu-id="4e115-113">Like a constraint, a calculation is associated with a specific component in a product configuration model, and can’t be reused by or shared with another component.</span></span> <span data-ttu-id="4e115-114">وهناك اختلاف مهم بين العمليات الحسابية والقيود يتمثل في أن العمليات الحسابية لا غنى عنه (أحادية الاتجاه)، بينما تكون القيود تعريفية (ثنائية الاتجاه).</span><span class="sxs-lookup"><span data-stu-id="4e115-114">One important difference between calculations and constraints is that calculations are imperative (unidirectional), whereas constraints are declarative (bi-directional).</span></span> <span data-ttu-id="4e115-115">لمزيد من المعلومات عن القيود، راجع [قيود التعبير وقيود الجدول](expression-constraints-table-constraints-product-configuration-models.md).</span><span class="sxs-lookup"><span data-stu-id="4e115-115">For more information about constraints, see [Expression constraints and table constraints](expression-constraints-table-constraints-product-configuration-models.md).</span></span>  

<span data-ttu-id="4e115-116">يتكون الحساب من السمة الهدف وتعبير حساب.</span><span class="sxs-lookup"><span data-stu-id="4e115-116">A calculation consists of a target attribute and a calculation expression.</span></span>

## <a name="what-is-a-target-attribute"></a><span data-ttu-id="4e115-117">ما هي السمة الهدف؟</span><span class="sxs-lookup"><span data-stu-id="4e115-117">What is a target attribute?</span></span>
<span data-ttu-id="4e115-118">السمة الهدف هي سمة تتلقى نتيجة العملية الحسابية في تعبير.</span><span class="sxs-lookup"><span data-stu-id="4e115-118">A target attribute is an attribute that receives the result of the calculation expression.</span></span>  

<span data-ttu-id="4e115-119">في التعبير التالي، السمة الهدف هي قياس مفرش:</span><span class="sxs-lookup"><span data-stu-id="4e115-119">In the following expression, the target attribute is a tablecloth measurement:</span></span>  

<span data-ttu-id="4e115-120">**تعبير:** If\[decimalAttribute1 &lt;= decimalAttribute2, True, False\]</span><span class="sxs-lookup"><span data-stu-id="4e115-120">**Expression:** If\[decimalAttribute1 &lt;= decimalAttribute2, True, False\]</span></span>  

<span data-ttu-id="4e115-121">**DecimalAttribute1** هو طول الطاولة و**decimalAttribute2** هو طول المفرش.</span><span class="sxs-lookup"><span data-stu-id="4e115-121">**DecimalAttribute1** is the table length, and **decimalAttribute2** is the tablecloth length.</span></span> <span data-ttu-id="4e115-122">وتكون نتيجة هذا التعبير بالقيمة **صواب** للسمة الهدف إذا كان **decimalAttribute2** أكبر من أو يساوي **decimalAttribute1**.</span><span class="sxs-lookup"><span data-stu-id="4e115-122">The expression returns the value **True** to the target attribute if **decimalAttribute2** is greater than or equal to **decimalAttribute1**.</span></span> <span data-ttu-id="4e115-123">وبخلاف ذلك، تكون نتيجة التعبير بالقيمة **خطأ**.</span><span class="sxs-lookup"><span data-stu-id="4e115-123">Otherwise, the expression returns **False**.</span></span> <span data-ttu-id="4e115-124">ولذلك، قياس المفرش يعد مقبولاً إذا كان طول المفرش يساوي أو يتجاوز طول الطاولة.</span><span class="sxs-lookup"><span data-stu-id="4e115-124">Therefore, the tablecloth measurement is acceptable if the tablecloth length is the same as or exceeds the length of the table.</span></span>

## <a name="what-attribute-types-can-be-set-to-target-attributes"></a><span data-ttu-id="4e115-125">ما هي أنواع السمة التي يمكن تعيينها لسمات الهدف؟</span><span class="sxs-lookup"><span data-stu-id="4e115-125">What attribute types can be set to target attributes?</span></span>
<span data-ttu-id="4e115-126">يمكن تعيين كل أنواع السمات المعتمدة لمكون المنتج لسمات الهدف باستثناء النص بدون قائمة ثابتة.</span><span class="sxs-lookup"><span data-stu-id="4e115-126">All attribute types that the product configurator supports can be set to target attributes, except text without a fixed list.</span></span>

## <a name="can-the-value-of-a-target-attribute-restrict-the-values-of-the-input-attributes-in-a-calculation"></a><span data-ttu-id="4e115-127">هل يمكن لسمة هدف تقييد قيم سمات الإدخال في عملية حسابية؟</span><span class="sxs-lookup"><span data-stu-id="4e115-127">Can the value of a target attribute restrict the values of the input attributes in a calculation?</span></span>
<span data-ttu-id="4e115-128">لا، يمكن لسمة هدف تقييد قيم سمات الإدخال، لأن العمليات الحسابية إحادية الاتجاه.</span><span class="sxs-lookup"><span data-stu-id="4e115-128">No, the value of a target attribute can’t restrict the values of the input attributes, because calculations are unidirectional.</span></span> <span data-ttu-id="4e115-129">ولذلك، يتم تعيين قيمة السمة الهدف بناءً على التغييرات في قيمة سمات الإدخال، ولكن لا يؤثر تغيير في قيمة الهدف على قيمة سمات الإدخال.</span><span class="sxs-lookup"><span data-stu-id="4e115-129">Therefore, the value of the target attribute is set based on changes in the value of the input attributes, but a change in the value of the target doesn’t affect the value of the input attributes.</span></span> <span data-ttu-id="4e115-130">ويختلف هذا السلوك عن سلوك القيود.</span><span class="sxs-lookup"><span data-stu-id="4e115-130">This behavior differs from the behavior for constraints.</span></span> <span data-ttu-id="4e115-131">وتحدث القيود في كلا الاتجاهين.</span><span class="sxs-lookup"><span data-stu-id="4e115-131">Constraints occur in both directions.</span></span>

### <a name="example"></a><span data-ttu-id="4e115-132">مثال</span><span class="sxs-lookup"><span data-stu-id="4e115-132">Example</span></span>

<span data-ttu-id="4e115-133">في التعبير التالي، كان هدف الحساب هو طول كبل طاقة وقيمة الإدخال هي لون:</span><span class="sxs-lookup"><span data-stu-id="4e115-133">In the following expression, the target for the calculation is the length of a power cord, and the input value is a color:</span></span>  

<span data-ttu-id="4e115-134">**التعبير:** \[If Color == "Green", 1.5, 1.0\]</span><span class="sxs-lookup"><span data-stu-id="4e115-134">**Expression:** \[If Color == "Green", 1.5, 1.0\]</span></span>  

<span data-ttu-id="4e115-135">عند القيام بتكوين الصنف، يتم تعيين طول سلك الطاقة إلى **1.5** ‬‏‫ إذا قمت بتحديد **أخضر‬‏‫** كقيمة لسمة اللون.‬</span><span class="sxs-lookup"><span data-stu-id="4e115-135">When you configure the item, the length of the power cord is set to **1.5** if you specify **Green** as the value of color attribute.</span></span> <span data-ttu-id="4e115-136">إذا قمت بتحديد أي لون آخر، يتم تعيين الطول إلى **1.0**.</span><span class="sxs-lookup"><span data-stu-id="4e115-136">If you specify any other color, the length is set to **1.0**.</span></span> <span data-ttu-id="4e115-137">ومع ذلك، نظراً لأن العمليات الحسابية أحادية الاتجاه، لا تقوم العملية الحسابية بتعيين قيمة سمة اللون إلى **أخضر**، إذا قمت بتحديد طول **1.5**.</span><span class="sxs-lookup"><span data-stu-id="4e115-137">However, because calculations are unidirectional, the calculation doesn't set the value of the color attribute to **Green** if you specify a length of **1.5**.</span></span>

## <a name="what-happens-if-a-calculation-has-a-target-attribute-of-the-integer-type-but-a-calculation-generates-a-decimal-number"></a><span data-ttu-id="4e115-138">ماذا يحدث إذا كانت العملية الحسابية تشمل سمة هدف من نوع عدد صحيح ولكن تعطي العملية الحسابية عددًا عشريًا؟</span><span class="sxs-lookup"><span data-stu-id="4e115-138">What happens if a calculation has a target attribute of the integer type but a calculation generates a decimal number?</span></span>
<span data-ttu-id="4e115-139">إذا كان سمة هدف من نوع عدد صحيح، ولكن تُنشئ العملية الحسابية عددًا عشريًا، فإنه يتم إرجاع الجزء الصحيح من النتيجة المحسوبة فقط.</span><span class="sxs-lookup"><span data-stu-id="4e115-139">If a target attribute is of the integer type, but a calculation generates a decimal number, only the integer part of the calculated result is returned.</span></span> <span data-ttu-id="4e115-140">وتتم إزالة الجزء العشري، ولا يتم تقريب النتيجة.</span><span class="sxs-lookup"><span data-stu-id="4e115-140">The decimal part is removed, and the result isn't rounded.</span></span> <span data-ttu-id="4e115-141">على سبيل المثال، يتم عرض نتيجة 12.70 باعتبارها 12.</span><span class="sxs-lookup"><span data-stu-id="4e115-141">For example, a result of 12.70 is shown as 12.</span></span>

## <a name="when-do-calculations-occur"></a><span data-ttu-id="4e115-142">متى تحدث الحسابات؟</span><span class="sxs-lookup"><span data-stu-id="4e115-142">When do calculations occur?</span></span>
<span data-ttu-id="4e115-143">تحدث الحسابات عندما يتم توفير قيمة لكل سمات الإدخال.</span><span class="sxs-lookup"><span data-stu-id="4e115-143">Calculations occur when a value has been provided for all input attributes.</span></span>

## <a name="can-i-overwrite-the-value-that-is-calculated-for-the-target-attribute"></a><span data-ttu-id="4e115-144">هل يمكنك استبدال القيمة التي يتم حسابها للسمة الهدف؟</span><span class="sxs-lookup"><span data-stu-id="4e115-144">Can I overwrite the value that is calculated for the target attribute?</span></span>
<span data-ttu-id="4e115-145">يمكنك استبدال القيمة التي يتم حسابها للسمة الهدف إلا إذا تم تعيين السمة الهدف إلى مخفي أو للقراءة فقط.</span><span class="sxs-lookup"><span data-stu-id="4e115-145">You can overwrite the value that is calculated for the target attribute, unless the target attribute is set as hidden or read-only.</span></span>

## <a name="how-do-i-set-a-target-attribute-as-hidden-or-read-only"></a><span data-ttu-id="4e115-146">كيف يمكنني تعيين سمة هدف كمخفي أو للقراءة فقط؟</span><span class="sxs-lookup"><span data-stu-id="4e115-146">How do I set a target attribute as hidden or read-only?</span></span>
<span data-ttu-id="4e115-147">لتعيين سمة كمخفي أو للقراءة فقط، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="4e115-147">To set an attribute as hidden or read-only, follow these steps.</span></span>

1.  <span data-ttu-id="4e115-148">انقر فوق **إدارة معلومات المنتج** &gt; **عامة** &gt; **نماذج تكوين المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="4e115-148">Click **Product information management** &gt; **Common** &gt; **Product configuration models**.</span></span>
2.  <span data-ttu-id="4e115-149">حدد نموذج تكوين منتج، ثم في "جزء الإجراءات"، انقر فوق **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="4e115-149">Select a product configuration model, and then, on the Action Pane, click **Edit**.</span></span>
3.  <span data-ttu-id="4e115-150">وفي صفحة **تفاصيل نموذج تكوين منتج مستند إلى قيد‬**، حدد السمة لاستخدام سمة هدف.</span><span class="sxs-lookup"><span data-stu-id="4e115-150">On the **Constraint-based product configuration model details** page, select the attribute to use as a target attribute.</span></span>
4.  <span data-ttu-id="4e115-151">وفي علامة التبويب السريع **سمات**، حدد **مخفي** أو **للقراءة فقط**.</span><span class="sxs-lookup"><span data-stu-id="4e115-151">On the **Attributes** FastTab, select **Hidden** or **Read-only**.</span></span>

## <a name="can-a-calculation-overwrite-the-values-that-i-set"></a><span data-ttu-id="4e115-152">هل يمكن لعملية حسابية استبدال القيم التي حددتها؟</span><span class="sxs-lookup"><span data-stu-id="4e115-152">Can a calculation overwrite the values that I set?</span></span>
<span data-ttu-id="4e115-153">لا.</span><span class="sxs-lookup"><span data-stu-id="4e115-153">No.</span></span> <span data-ttu-id="4e115-154">القيم التي تقوم بتعيينها عند تكوين منتج هي القيم التي يتم استخدامها.</span><span class="sxs-lookup"><span data-stu-id="4e115-154">The values that you set when you configure a product are the values that are used.</span></span> <span data-ttu-id="4e115-155">لا يمكن استبدال الحساب الذي يحدث عند تغيير قيم الإدخال في حساب بالقيم التي تقدمها لسمة معينة.</span><span class="sxs-lookup"><span data-stu-id="4e115-155">The calculation that occurs when the input values in a calculation are changed can’t overwrite the values that you provide for a specific attribute.</span></span>

## <a name="what-happens-if-i-remove-an-input-value-in-a-calculation"></a><span data-ttu-id="4e115-156">ماذا يحدث إذا قمت بإزالة قيمة إدخال في حساب؟</span><span class="sxs-lookup"><span data-stu-id="4e115-156">What happens if I remove an input value in a calculation?</span></span>
<span data-ttu-id="4e115-157">إذا قمت بإزالة قيمة إدخال في حساب، يتم أيضًا إزالة قيمة السمة الهدف.</span><span class="sxs-lookup"><span data-stu-id="4e115-157">If you remove an input value in a calculation, the value of the target attribute is also removed.</span></span>

## <a name="why-do-i-receive-an-error-message-that-says-that-my-model-is-in-contradiction"></a><span data-ttu-id="4e115-158">لماذا أحصل على رسالة خطأ تقول بأن هناك تناقض في النموذج الخاص بي؟</span><span class="sxs-lookup"><span data-stu-id="4e115-158">Why do I receive an error message that says that my model is in contradiction?</span></span>
<span data-ttu-id="4e115-159">يتم عرض هذه الرسالة عندما يتضمن حساب خطأ أو عند وجود تناقض في واحد أو أكثر من القيود.</span><span class="sxs-lookup"><span data-stu-id="4e115-159">This message is shown when a calculation includes an error, or when a contradiction exists in one or more constraints.</span></span> <span data-ttu-id="4e115-160">لمزيد من المعلومات عن التناقضات في القيود، راجع [قيود التعبير وقيود الجدول](expression-constraints-table-constraints-product-configuration-models.md).</span><span class="sxs-lookup"><span data-stu-id="4e115-160">For more information about contradictions in constraints, see [Expression constraints and table constraints](expression-constraints-table-constraints-product-configuration-models.md).</span></span> <span data-ttu-id="4e115-161">وفيما يلي بعض الحالات التي يمكن فيها أن تحدث الأخطاء في العمليات الحسابية:</span><span class="sxs-lookup"><span data-stu-id="4e115-161">Here are some situations where errors can occur in calculations:</span></span>

-   <span data-ttu-id="4e115-162">يتم قسمة القيمة على 0 (صفر).</span><span class="sxs-lookup"><span data-stu-id="4e115-162">A value is divided by 0 (zero).</span></span>
-   <span data-ttu-id="4e115-163">يوجد تعارض بين العنصرين التاليين:</span><span class="sxs-lookup"><span data-stu-id="4e115-163">A conflict exists between the following two elements:</span></span>
    -   <span data-ttu-id="4e115-164">القيم المتوفرة لسمة، والتي تتحدد بقيد.</span><span class="sxs-lookup"><span data-stu-id="4e115-164">The values that are available for an attribute and are limited by a constraint</span></span>
    -   <span data-ttu-id="4e115-165">القيمة التي تم إنشاؤها بواسطة عملية حسابية.</span><span class="sxs-lookup"><span data-stu-id="4e115-165">A value that is generated by a calculation</span></span>
-   <span data-ttu-id="4e115-166">القيم التي يتم إرجاعها بواسطة الحساب توجد خارج مجال السمة.</span><span class="sxs-lookup"><span data-stu-id="4e115-166">The values that are returned by the calculation are outside the domain of the attribute.</span></span> <span data-ttu-id="4e115-167">مثال: عدد صحيح من \[1..10\] الذي يتم حسابه إلى 0.</span><span class="sxs-lookup"><span data-stu-id="4e115-167">An example is an integer from \[1..10\] that is calculated to 0.</span></span>

## <a name="why-do-i-receive-an-error-message-even-though-i-successfully-validated-my-product-model"></a><span data-ttu-id="4e115-168">لماذا أحصل على رسالة خطأ على الرغم من أنني تحققت من صحة طراز المنتج الخاص بي بنجاح؟</span><span class="sxs-lookup"><span data-stu-id="4e115-168">Why do I receive an error message even though I successfully validated my product model?</span></span>
<span data-ttu-id="4e115-169">العمليات الحسابية غير مضمنة في التحقق من الصحة.</span><span class="sxs-lookup"><span data-stu-id="4e115-169">Calculations aren't included in the validation.</span></span> <span data-ttu-id="4e115-170">يجب عليك اختبار نموذج تكوين المنتج للبحث عن أخطاء في الحسابات.</span><span class="sxs-lookup"><span data-stu-id="4e115-170">You must test the product configuration model to find errors in calculations.</span></span> <span data-ttu-id="4e115-171">لاختبار نموذج تكوين منتج، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="4e115-171">To test a product configuration model, follow these steps.</span></span>

1.  <span data-ttu-id="4e115-172">انقر فوق **إدارة معلومات المنتج** &gt; **عامة** &gt; **نماذج تكوين المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="4e115-172">Click **Product information management** &gt; **Common** &gt; **Product configuration models**.</span></span>
2.  <span data-ttu-id="4e115-173">حدد نموذج تكوين منتج، ثم في "جزء الإجراءات"، في مجموعة **الإرجاع**، انقر فوق **اختبار**.</span><span class="sxs-lookup"><span data-stu-id="4e115-173">Select a product configuration model, and then, on the Action Pane, in the **Run** group, click **Test**.</span></span>





