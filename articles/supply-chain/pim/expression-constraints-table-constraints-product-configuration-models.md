---
title: "قيود التعبير وقيود الجدول في نماذج تكوين المنتج"
description: "يصف هذا الموضوع استخدام قيود التعبير وقيود الجدول. تتحكم القيود في قيم السمات التي يمكن تحديدها عند تكوين المنتجات لأمر المبيعات أو عرض أسعار المبيعات أو أمر الشراء أو أمر الإنتاج. يمكنك استخدام قيود التعبير أو قيود الجدول، اعتمادًا على الطريقة التي تفضل بها إنشاء القيود."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCGlobalTableConstraintEdit, PCProductConfigurationModelDetails, PCTableConstraintAttachAttributeTree, PCTableConstraintDefinition
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 7aeb0438182fe177ac83580f03cbb547c79fd08a
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a><span data-ttu-id="80312-105">قيود التعبير وقيود الجدول في نماذج تكوين المنتج</span><span class="sxs-lookup"><span data-stu-id="80312-105">Expression constraints and table constraints in product configuration models</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="80312-106">يصف هذا الموضوع استخدام قيود التعبير وقيود الجدول.</span><span class="sxs-lookup"><span data-stu-id="80312-106">This topic describes the use of expression constraints and table constraints.</span></span> <span data-ttu-id="80312-107">تتحكم القيود في قيم السمات التي يمكن تحديدها عند تكوين المنتجات لأمر المبيعات أو عرض أسعار المبيعات أو أمر الشراء أو أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="80312-107">Constraints control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="80312-108">يمكنك استخدام قيود التعبير أو قيود الجدول، اعتمادًا على الطريقة التي تفضل بها إنشاء القيود.</span><span class="sxs-lookup"><span data-stu-id="80312-108">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> 

<span data-ttu-id="80312-109">يتم استخدام القيود للتحكم في قيم السمات التي يمكن تحديدها عند تكوين المنتجات لأمر المبيعات أو عرض أسعار المبيعات أو أمر الشراء أو أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="80312-109">Constraints are used to control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="80312-110">يمكنك استخدام قيود التعبير أو قيود الجدول، اعتمادًا على الطريقة التي تفضل بها إنشاء القيود.</span><span class="sxs-lookup"><span data-stu-id="80312-110">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span>

## <a name="what-are-expression-constraints"></a><span data-ttu-id="80312-111">ما هي قيود التعبير؟</span><span class="sxs-lookup"><span data-stu-id="80312-111">What are expression constraints?</span></span>
<span data-ttu-id="80312-112">تتسم قيود التعبير بتعبير يستخدم الدالات والمعامِلات الحسابية المنطقية.</span><span class="sxs-lookup"><span data-stu-id="80312-112">Expression constraints are characterized by an expression that uses arithmetic and Boolean operators and functions.</span></span> <span data-ttu-id="80312-113">تتم كتابة قيد تعبير لمكون محدد في نموذج تكوين منتج.</span><span class="sxs-lookup"><span data-stu-id="80312-113">An expression constraint is written for a specific component in a product configuration model.</span></span> <span data-ttu-id="80312-114">لا يمكن إعادة استخدامها بواسطة أو بالمشاركة مع مكون آخر.</span><span class="sxs-lookup"><span data-stu-id="80312-114">It can't be reused by or shared with another component.</span></span> <span data-ttu-id="80312-115">ومع ذلك، يمكن لقيود التعبير لمكون الإشارة إلى سمات المكونات الفرعية للمكون.</span><span class="sxs-lookup"><span data-stu-id="80312-115">However, the expression constraints for a component can reference attributes of the component's subcomponents.</span></span>

## <a name="what-are-table-constraints"></a><span data-ttu-id="80312-116">ما هي قيود الجدول؟</span><span class="sxs-lookup"><span data-stu-id="80312-116">What are table constraints?</span></span>
<span data-ttu-id="80312-117">تسرد قيود الجدول مجموعات القيم المسموح بها للسمات عندما تقوم بتكوين منتج.</span><span class="sxs-lookup"><span data-stu-id="80312-117">Table constraints list the combinations of values that are allowed for attributes when you configure a product.</span></span> <span data-ttu-id="80312-118">يمكن استخدام تعريفات قيود الجدول بشكل عام.</span><span class="sxs-lookup"><span data-stu-id="80312-118">Table constraint definitions can be used generically.</span></span> <span data-ttu-id="80312-119">عند إنشاء قيد جدول لمكون في نموذج تكوين منتج، حدد تعريف قيد جدول.</span><span class="sxs-lookup"><span data-stu-id="80312-119">When you create a table constraint for a component in a product configuration model, you select a table constraint definition.</span></span> <span data-ttu-id="80312-120">لإنشاء المجموعات المسموح بها، تقوم بإضافة سمات الأنواع المحددة للمكونات.</span><span class="sxs-lookup"><span data-stu-id="80312-120">To create the combinations that are allowed, you add attributes of specific types to the components.</span></span> <span data-ttu-id="80312-121">يحتوي كل نوع سمة على قيمة محددة.</span><span class="sxs-lookup"><span data-stu-id="80312-121">Each attribute type has a specific value.</span></span>

### <a name="example-of-a-table-constraint"></a><span data-ttu-id="80312-122">مثال على قيد جدول</span><span class="sxs-lookup"><span data-stu-id="80312-122">Example of a table constraint</span></span>

<span data-ttu-id="80312-123">يوضح هذا المثال كيفية تحديد تكوين مكبر صوت لألوان الكابينة محددة والأجزاء الأمامية.</span><span class="sxs-lookup"><span data-stu-id="80312-123">This example shows how you can limit the configuration of a speaker to specific cabinet finishes and fronts.</span></span> <span data-ttu-id="80312-124">يعرض الجدول الأول ألوان الكابينة والأجزاء الأمامية المتوفرة بشكل عام للتكوين.</span><span class="sxs-lookup"><span data-stu-id="80312-124">The first table shows the cabinet finishes and fronts that are generally available for configuration.</span></span> <span data-ttu-id="80312-125">ويتم تحديد القيم لنوعي السمات **لون الكابينة**و**الشبكة الأمامية**.</span><span class="sxs-lookup"><span data-stu-id="80312-125">The values are defined for the **Cabinet finish** and **Front grill** attribute types.</span></span>

| <span data-ttu-id="80312-126">نوع السمة</span><span class="sxs-lookup"><span data-stu-id="80312-126">Attribute type</span></span> | <span data-ttu-id="80312-127">القيم</span><span class="sxs-lookup"><span data-stu-id="80312-127">Values</span></span>                      |
|----------------|-----------------------------|
| <span data-ttu-id="80312-128">لون الكابينة</span><span class="sxs-lookup"><span data-stu-id="80312-128">Cabinet finish</span></span> | <span data-ttu-id="80312-129">أسود، وبلوطي، وروزوود، وأبيض</span><span class="sxs-lookup"><span data-stu-id="80312-129">Black, Oak, Rosewood, White</span></span> |
| <span data-ttu-id="80312-130">الشبكة الأمامية</span><span class="sxs-lookup"><span data-stu-id="80312-130">Front grill</span></span>    | <span data-ttu-id="80312-131">أسود، ومعدني، وأبيض</span><span class="sxs-lookup"><span data-stu-id="80312-131">Black, Metal, White</span></span>         |

<span data-ttu-id="80312-132">يُظهر الجدول التالي هذا المجموعات المحددة من قِبل قيد الجدول **اللون واللمسة النهائية**.</span><span class="sxs-lookup"><span data-stu-id="80312-132">The next table shows the combinations that are defined by the **Color and finish** table constraint.</span></span> <span data-ttu-id="80312-133">باستخدام هذا القيد في الجدول، يمكنك تكوين مكبر صوت بلون بلوطي وشبكة سوداء، ولون روزوود وشبكة بيضاء، وهكذا.</span><span class="sxs-lookup"><span data-stu-id="80312-133">By using this table constraint, you can configure a speaker that has an oak finish and a black grill, a Rosewood finish and a white grill, and so on.</span></span>

| <span data-ttu-id="80312-134">إنهاء</span><span class="sxs-lookup"><span data-stu-id="80312-134">Finish</span></span>         | <span data-ttu-id="80312-135">الشبكة</span><span class="sxs-lookup"><span data-stu-id="80312-135">Grill</span></span>                       |
|----------------|-----------------------------|
| <span data-ttu-id="80312-136">بلوطي</span><span class="sxs-lookup"><span data-stu-id="80312-136">Oak</span></span>            | <span data-ttu-id="80312-137">أسود</span><span class="sxs-lookup"><span data-stu-id="80312-137">Black</span></span>                       |
| <span data-ttu-id="80312-138">روزوود</span><span class="sxs-lookup"><span data-stu-id="80312-138">Rosewood</span></span>       | <span data-ttu-id="80312-139">أبيض</span><span class="sxs-lookup"><span data-stu-id="80312-139">White</span></span>                       |
| <span data-ttu-id="80312-140">أبيض</span><span class="sxs-lookup"><span data-stu-id="80312-140">White</span></span>          | <span data-ttu-id="80312-141">أسود</span><span class="sxs-lookup"><span data-stu-id="80312-141">Black</span></span>                       |
| <span data-ttu-id="80312-142">أبيض</span><span class="sxs-lookup"><span data-stu-id="80312-142">White</span></span>          | <span data-ttu-id="80312-143">أبيض</span><span class="sxs-lookup"><span data-stu-id="80312-143">White</span></span>                       |
| <span data-ttu-id="80312-144">أسود</span><span class="sxs-lookup"><span data-stu-id="80312-144">Black</span></span>          | <span data-ttu-id="80312-145">أسود</span><span class="sxs-lookup"><span data-stu-id="80312-145">Black</span></span>                       |
| <span data-ttu-id="80312-146">أسود</span><span class="sxs-lookup"><span data-stu-id="80312-146">Black</span></span>          | <span data-ttu-id="80312-147">معدني</span><span class="sxs-lookup"><span data-stu-id="80312-147">Metal</span></span>                       | 

<span data-ttu-id="80312-148">يمكنك إنشاء قيود جدول إما محددة بواسطة المستخدم أو محددة بواسطة النظام.</span><span class="sxs-lookup"><span data-stu-id="80312-148">You can create system-defined and user-defined table constraints.</span></span> <span data-ttu-id="80312-149">لمزيد من المعلومات، راجع [قيود الجدول المحددة من قِبل النظام والمحددة من قِبل المستخدم](system-defined-user-defined-table-constraints.md).</span><span class="sxs-lookup"><span data-stu-id="80312-149">For more information, see [System-defined and user-defined table constraints](system-defined-user-defined-table-constraints.md).</span></span>

## <a name="what-syntax-should-be-used-to-write-constraints"></a><span data-ttu-id="80312-150">‏‫ما بنية الجملة التي يجب استخدامها لكتابة القيود؟</span><span class="sxs-lookup"><span data-stu-id="80312-150">What syntax should be used to write constraints?</span></span>
<span data-ttu-id="80312-151">يجب عليك استخدام بنية جملة لغة تصميم التحسين (OML) عند كتابة القيود.</span><span class="sxs-lookup"><span data-stu-id="80312-151">You must use Optimization Modeling Language (OML) syntax when you write constraints.</span></span> <span data-ttu-id="80312-152">يستخدم النظام أداة حل القيود Microsoft Solver Foundation لحل القيود.</span><span class="sxs-lookup"><span data-stu-id="80312-152">The system uses Microsoft Solver Foundation constraint solver to solve the constraints.</span></span>

## <a name="should-i-use-table-constraints-or-expression-constraints"></a><span data-ttu-id="80312-153">هل يجب استخدام قيود الجدول أو قيود التعبير؟</span><span class="sxs-lookup"><span data-stu-id="80312-153">Should I use table constraints or expression constraints?</span></span>
<span data-ttu-id="80312-154">يمكنك استخدام قيود التعبير أو قيود الجدول، اعتمادًا على الطريقة التي تفضل بها إنشاء القيود.</span><span class="sxs-lookup"><span data-stu-id="80312-154">You can use either expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> <span data-ttu-id="80312-155">يمكنك إنشاء قيد جدول كمصفوفة، بينما يكون قيد التعبير عبارة فردية.</span><span class="sxs-lookup"><span data-stu-id="80312-155">You build a table constraint as a matrix, whereas an expression constraint is an individual statement.</span></span> <span data-ttu-id="80312-156">عندما تقوم بتكوين منتج، فلا يهم نوع القيد المستخدَم.</span><span class="sxs-lookup"><span data-stu-id="80312-156">When you configure a product, it doesn't matter what kind of constraint is used.</span></span> <span data-ttu-id="80312-157">يعرض المثال التالي مدى اختلاف الطريقتين.</span><span class="sxs-lookup"><span data-stu-id="80312-157">The following example shows how the two methods differ.</span></span>  

<span data-ttu-id="80312-158">عند قيامك بتكوين منتج باستخدام إعدادات القيود التالية، يتم السماح بهذه المجموعات:</span><span class="sxs-lookup"><span data-stu-id="80312-158">When you configure a product by using the following constraint setups, these combinations are allowed:</span></span>

-   <span data-ttu-id="80312-159">منتج باللون الأسود، وبحجم 30 أو 50</span><span class="sxs-lookup"><span data-stu-id="80312-159">A product in the color Black, and in size 30 or 50</span></span>
-   <span data-ttu-id="80312-160">منتج باللون الأحمر، وبحجم 20</span><span class="sxs-lookup"><span data-stu-id="80312-160">A product in the color Red and in size 20</span></span>

### <a name="table-constraint-setup"></a><span data-ttu-id="80312-161">إعداد قيد الجدول</span><span class="sxs-lookup"><span data-stu-id="80312-161">Table constraint setup</span></span>

| <span data-ttu-id="80312-162">اللون</span><span class="sxs-lookup"><span data-stu-id="80312-162">Color</span></span> | <span data-ttu-id="80312-163">الحجم</span><span class="sxs-lookup"><span data-stu-id="80312-163">Size</span></span> |
|-------|------|
| <span data-ttu-id="80312-164">أسود</span><span class="sxs-lookup"><span data-stu-id="80312-164">Black</span></span> | <span data-ttu-id="80312-165">30</span><span class="sxs-lookup"><span data-stu-id="80312-165">30</span></span>   |
| <span data-ttu-id="80312-166">أسود</span><span class="sxs-lookup"><span data-stu-id="80312-166">Black</span></span> | <span data-ttu-id="80312-167">50</span><span class="sxs-lookup"><span data-stu-id="80312-167">50</span></span>   |
| <span data-ttu-id="80312-168">أحمر</span><span class="sxs-lookup"><span data-stu-id="80312-168">Red</span></span>   | <span data-ttu-id="80312-169">20</span><span class="sxs-lookup"><span data-stu-id="80312-169">20</span></span>   |

### <a name="expression-constraint-setup"></a><span data-ttu-id="80312-170">إعداد قيد التعبير</span><span class="sxs-lookup"><span data-stu-id="80312-170">Expression constraint setup</span></span>

<span data-ttu-id="80312-171">(لون == "أسود" و (حجم == "30" | حجم == "50")) | (لون == "أحمر" وحجم = "20")</span><span class="sxs-lookup"><span data-stu-id="80312-171">(Color == "Black" & (size == "30" | size == "50")) | (color == "Red" & size = "20")</span></span>

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a><span data-ttu-id="80312-172">هل يجب استخدام المعامِلات أو تدوين الحرف المزيد عند كتابة قيود التعبير؟</span><span class="sxs-lookup"><span data-stu-id="80312-172">Should I use operators or infix notation when I write expression constraints?</span></span>
<span data-ttu-id="80312-173">يمكنك كتابة قيد تعبير إما باستخدام تدوين الحروف المزيدة أو معامِلات البادئات المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="80312-173">You can write an expression constraint by using either the available prefix operators or infix notation.</span></span> <span data-ttu-id="80312-174">لا يمكنك استخدام تدوين الحروف المزيدة لمعامِلات ‏‫القيمة**المطلقة**، و**الحد الأدنى**، و**الحد الأقصى**.</span><span class="sxs-lookup"><span data-stu-id="80312-174">For the **Min**, **Max**, and **Abs** operators, you can't use infix notation.</span></span> <span data-ttu-id="80312-175">ويتم تضمين هذه المعامِلات كمعامِلات قياسية في معظم لغات البرمجة.</span><span class="sxs-lookup"><span data-stu-id="80312-175">These operators are included as standard operators in most programming languages.</span></span>

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a><span data-ttu-id="80312-176">ما هي المعامِلات وتدوينات الحروف المزيدة التي يمكن استخدامها عند كتابة قيود التعبير؟</span><span class="sxs-lookup"><span data-stu-id="80312-176">What operators and infix notation can I use when I write expression constraints?</span></span>
<span data-ttu-id="80312-177">تسرد الجداول التالية المعامِلات وتدوينات الحروف المزيدة التي يمكنك استخدامها عند كتابة قيد تعبير لمكون في نموذج تكوين منتج.</span><span class="sxs-lookup"><span data-stu-id="80312-177">The following tables list the operators and infix notation that you can use when you write an expression constraint for a component in a product configuration model.</span></span> <span data-ttu-id="80312-178">في الأمثلة الواردة في هذا الجدول الأول، يمكنك الاطلاع على كيفية كتابة تعبير باستخدام المعامِلات أو تدوينات الحروف المزيدة.</span><span class="sxs-lookup"><span data-stu-id="80312-178">The examples in the first table show how to write an expression by using either infix notation or operators.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="80312-179">عامل تشغيل</span><span class="sxs-lookup"><span data-stu-id="80312-179">Operator</span></span></th>
<th><span data-ttu-id="80312-180">الوصف</span><span class="sxs-lookup"><span data-stu-id="80312-180">Description</span></span></th>
<th><span data-ttu-id="80312-181">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="80312-181">Syntax</span></span></th>
<th><span data-ttu-id="80312-182">أمثلة</span><span class="sxs-lookup"><span data-stu-id="80312-182">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="80312-183">يعني</span><span class="sxs-lookup"><span data-stu-id="80312-183">Implies</span></span></td>
<td><span data-ttu-id="80312-184">يكون هذا الأمر صحيحًا إذا كان الشرط الأول خاطئًا، والشرط الثاني صحيح، أو كليهما.</span><span class="sxs-lookup"><span data-stu-id="80312-184">This is true if the first condition is false, the second condition is true, or both.</span></span></td>
<td><span data-ttu-id="80312-185">يعني [a أو b]، الحرف المزيد: a -: b</span><span class="sxs-lookup"><span data-stu-id="80312-185">Implies[a, b], infix: a -: b</span></span></td>
<td><ul>
<li><span data-ttu-id="80312-186"><strong>عامل التشغيل:</strong> يتضمن[x‏ != 0، y &gt;=‏ 0]</span><span class="sxs-lookup"><span data-stu-id="80312-186"><strong>Operator:</strong> Implies[x != 0, y &gt;= 0]</span></span></li>
<li><span data-ttu-id="80312-187"><strong>تدوين الحرف المزيد:</strong> x‏ != 0 -‏: y &gt;=‏ 0</span><span class="sxs-lookup"><span data-stu-id="80312-187"><strong>Infix notation:</strong> x != 0 -: y &gt;= 0</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="80312-188">و</span><span class="sxs-lookup"><span data-stu-id="80312-188">And</span></span></td>
<td><span data-ttu-id="80312-189">يكون هذا الأمر صحيحًا فقط إذا تحققت جميع الشروط.</span><span class="sxs-lookup"><span data-stu-id="80312-189">This is true only if all conditions are true.</span></span> <span data-ttu-id="80312-190">إذا كان عدد الشروط هو 0 (صفر)، ينتج قيمة <strong>صحيحة</strong>.</span><span class="sxs-lookup"><span data-stu-id="80312-190">If the number of conditions is 0 (zero), it produces <strong>True</strong>.</span></span></td>
<td><span data-ttu-id="80312-191">And‏[args]، الحرف المزيد: a &amp; b &amp; ... &amp; z</span><span class="sxs-lookup"><span data-stu-id="80312-191">And[args], infix: a &amp; b &amp; ... &amp; z</span></span></td>
<td><ul>
<li><span data-ttu-id="80312-192"><strong>عامل التشغيل:</strong> And‏[x‏ == 2، y &lt;=‏ 2]</span><span class="sxs-lookup"><span data-stu-id="80312-192"><strong>Operator:</strong> And[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="80312-193"><strong>تدوين الحرف المزيد:</strong> x‏ == 2 &amp; y &lt;=‏ 2</span><span class="sxs-lookup"><span data-stu-id="80312-193"><strong>Infix notation:</strong> x == 2 &amp; y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="80312-194">أو</span><span class="sxs-lookup"><span data-stu-id="80312-194">Or</span></span></td>
<td><span data-ttu-id="80312-195">يكون هذا الأمر صحيحًا إذا كان أي شرط صحيح.</span><span class="sxs-lookup"><span data-stu-id="80312-195">This is true if any condition is true.</span></span> <span data-ttu-id="80312-196">إذا كان عدد الشروط هو 0 (صفر)، تنتج قيمة <strong>خاطئة</strong>.</span><span class="sxs-lookup"><span data-stu-id="80312-196">If the number of conditions is 0 (zero), it produces <strong>False</strong>.</span></span></td>
<td><span data-ttu-id="80312-197">Or‏[args]، الحرف المزيد: a‏ | b |‏ ... | z</span><span class="sxs-lookup"><span data-stu-id="80312-197">Or[args], infix: a | b | ... | z</span></span></td>
<td><ul>
<li><span data-ttu-id="80312-198"><strong>عامل التشغيل:</strong> Or‏[x‏ == 2، y &lt;=‏ 2]</span><span class="sxs-lookup"><span data-stu-id="80312-198"><strong>Operator:</strong> Or[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="80312-199"><strong>تدوين الحرف المزيد:</strong> x =‏=‏ 2 | y &lt;=‏ 2</span><span class="sxs-lookup"><span data-stu-id="80312-199"><strong>Infix notation:</strong> x == 2 | y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="80312-200">زائد</span><span class="sxs-lookup"><span data-stu-id="80312-200">Plus</span></span></td>
<td><span data-ttu-id="80312-201">وهذا يلخص الشروط.</span><span class="sxs-lookup"><span data-stu-id="80312-201">This sums its conditions.</span></span> <span data-ttu-id="80312-202">إذا كان عدد الشروط هو 0 (صفر)، تنتج قيمة <strong>0</strong>.</span><span class="sxs-lookup"><span data-stu-id="80312-202">If the number of conditions is 0 (zero), it produces <strong>0</strong>.</span></span></td>
<td><span data-ttu-id="80312-203">Plus‏[args]، الحرف المزيد: a‏ + b‏ + ... + z</span><span class="sxs-lookup"><span data-stu-id="80312-203">Plus[args], infix: a + b + ... + z</span></span></td>
<td><ul>
<li><span data-ttu-id="80312-204"><strong>عامل التشغيل:</strong> زائد[x،‏ y،‏ 2] =‏=‏ z</span><span class="sxs-lookup"><span data-stu-id="80312-204"><strong>Operator:</strong> Plus[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="80312-205"><strong>تدوين الحرف المزيد:</strong> x + y + 2 =‏=‏ z</span><span class="sxs-lookup"><span data-stu-id="80312-205"><strong>Infix notation:</strong> x + y + 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="80312-206">ناقص</span><span class="sxs-lookup"><span data-stu-id="80312-206">Minus</span></span></td>
<td><span data-ttu-id="80312-207">هذا يناقض الوسيطة.</span><span class="sxs-lookup"><span data-stu-id="80312-207">This negates its argument.</span></span> <span data-ttu-id="80312-208">يجب أن يكون به شرط واحد فقط.</span><span class="sxs-lookup"><span data-stu-id="80312-208">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="80312-209">Minus‏[expr]، الحرف المزيد: -expr</span><span class="sxs-lookup"><span data-stu-id="80312-209">Minus[expr], infix: -expr</span></span></td>
<td><ul>
<li><span data-ttu-id="80312-210"><strong>عامل التشغيل:</strong> ناقص[x] =‏=‏ y</span><span class="sxs-lookup"><span data-stu-id="80312-210"><strong>Operator:</strong> Minus[x] == y</span></span></li>
<li><span data-ttu-id="80312-211"><strong>تدوين الحرف المزيد:</strong> -x =‏=‏ y</span><span class="sxs-lookup"><span data-stu-id="80312-211"><strong>Infix notation:</strong> -x == y</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="80312-212">القيمة المطلقة</span><span class="sxs-lookup"><span data-stu-id="80312-212">Abs</span></span></td>
<td><span data-ttu-id="80312-213">وهذا يأخذ القيمة المطلقة من شرطها.</span><span class="sxs-lookup"><span data-stu-id="80312-213">This takes the absolute value of its condition.</span></span> <span data-ttu-id="80312-214">يجب أن يكون به شرط واحد فقط.</span><span class="sxs-lookup"><span data-stu-id="80312-214">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="80312-215">Abs‏[expr]</span><span class="sxs-lookup"><span data-stu-id="80312-215">Abs[expr]</span></span></td>
<td><span data-ttu-id="80312-216"><strong>عامل التشغيل:</strong> Abs‏[x]</span><span class="sxs-lookup"><span data-stu-id="80312-216"><strong>Operator:</strong> Abs[x]</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="80312-217">الأوقات</span><span class="sxs-lookup"><span data-stu-id="80312-217">Times</span></span></td>
<td><span data-ttu-id="80312-218">يأخذ هذا المنتج من شروطه.</span><span class="sxs-lookup"><span data-stu-id="80312-218">This takes the product of its conditions.</span></span> <span data-ttu-id="80312-219">إذا كان عدد الشروط هو 0 (صفر)، تنتج قيمة <strong>1</strong>.</span><span class="sxs-lookup"><span data-stu-id="80312-219">If the number of conditions is 0 (zero), it produces <strong>1</strong>.</span></span></td>
<td><span data-ttu-id="80312-220">Times‏[args]، الحرف الزائد: a‏ * b * ... ‏* z</span><span class="sxs-lookup"><span data-stu-id="80312-220">Times[args], infix: a * b * ... * z</span></span></td>
<td><ul>
<li><span data-ttu-id="80312-221"><strong>عامل التشغيل:</strong> أوقات[x،‏ y،‏ 2] =‏=‏ z</span><span class="sxs-lookup"><span data-stu-id="80312-221"><strong>Operator:</strong> Times[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="80312-222"><strong>تدوين الحرف المزيد:</strong> x * y * 2 =‏=‏ z</span><span class="sxs-lookup"><span data-stu-id="80312-222"><strong>Infix notation:</strong> x * y * 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="80312-223">القدرة</span><span class="sxs-lookup"><span data-stu-id="80312-223">Power</span></span></td>
<td><span data-ttu-id="80312-224">يأخذ هذا قيمة أُسية.</span><span class="sxs-lookup"><span data-stu-id="80312-224">This takes an exponential.</span></span> <span data-ttu-id="80312-225">تنطبق هذه القيمة الأُسية من اليمين لليسار.</span><span class="sxs-lookup"><span data-stu-id="80312-225">It applies exponentiation from right to left.</span></span> <span data-ttu-id="80312-226">‏‫(وبعبارة أخرى، إنها مجمَّعة بالشكل الصحيح).‬ ‏‫ولذلك، <strong>Power‏‏[a،‏ b،‏ c]</strong> يكافئ <strong>Power‏‏[a،‏ Power‏[b،‏ c]]</strong>.</span><span class="sxs-lookup"><span data-stu-id="80312-226">(In other words, it's right-associative.) Therefore, <strong>Power[a, b, c]</strong> is equivalent to <strong>Power[a, Power[b, c]]</strong>.</span></span> <span data-ttu-id="80312-227"><strong>Power</strong> يمكن استخدامه فقط إذا كان الأس بقيمة موجبة.</span><span class="sxs-lookup"><span data-stu-id="80312-227"><strong>Power</strong> can be used only if the exponent is a positive constant.</span></span></td>
<td><span data-ttu-id="80312-228">Power‏[args]، الحرف المزيد: a ^ b ^ ... ^ z</span><span class="sxs-lookup"><span data-stu-id="80312-228">Power[args], infix: a ^ b ^ ... ^ z</span></span></td>
<td><ul>
<li><span data-ttu-id="80312-229"><strong>عامل التشغيل:</strong> Power[x،‏ 2] =‏=‏ y</span><span class="sxs-lookup"><span data-stu-id="80312-229"><strong>Operator:</strong> Power[x, 2] == y</span></span></li>
<li><span data-ttu-id="80312-230"><strong>تدوين الحرف المزيد:</strong> x ^ 2 =‏=‏ y</span><span class="sxs-lookup"><span data-stu-id="80312-230"><strong>Infix notation:</strong> x ^ 2 == y</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="80312-231">الحد الأقصى</span><span class="sxs-lookup"><span data-stu-id="80312-231">Max</span></span></td>
<td><span data-ttu-id="80312-232">ينتج عن هذا الأمر الشرط الأكبر.</span><span class="sxs-lookup"><span data-stu-id="80312-232">This produces the largest condition.</span></span> <span data-ttu-id="80312-233">إذا كان عدد الشروط هو 0 (صفر)، تنتج قيمة <strong>لانهائية</strong>.</span><span class="sxs-lookup"><span data-stu-id="80312-233">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="80312-234">Max‏[args]</span><span class="sxs-lookup"><span data-stu-id="80312-234">Max[args]</span></span></td>
<td><span data-ttu-id="80312-235"><strong>عامل التشغيل:</strong> الحد الأقصى[x،‏ y،‏ 2] =‏=‏ z</span><span class="sxs-lookup"><span data-stu-id="80312-235"><strong>Operator:</strong> Max[x, y, 2] == z</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="80312-236">الحد الأدنى</span><span class="sxs-lookup"><span data-stu-id="80312-236">Min</span></span></td>
<td><span data-ttu-id="80312-237">ينتج عن هذا الأمر الشرط الأصغر.</span><span class="sxs-lookup"><span data-stu-id="80312-237">This produces the smallest condition.</span></span> <span data-ttu-id="80312-238">إذا كان عدد الشروط هو 0 (صفر)، تنتج قيمة <strong>لانهائية</strong>.</span><span class="sxs-lookup"><span data-stu-id="80312-238">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="80312-239">Min‏[args]</span><span class="sxs-lookup"><span data-stu-id="80312-239">Min[args]</span></span></td>
<td><span data-ttu-id="80312-240"><strong>عامل التشغيل:</strong> الحد الأدنى[x،‏‏ y،‏‏ 2] =‏=‏ z</span><span class="sxs-lookup"><span data-stu-id="80312-240"><strong>Operator:</strong> Min[x, y, 2] == z</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="80312-241">ليس</span><span class="sxs-lookup"><span data-stu-id="80312-241">Not</span></span></td>
<td><span data-ttu-id="80312-242">ينتج عن هذا الأمر العكس المنطقي للشرط.</span><span class="sxs-lookup"><span data-stu-id="80312-242">This produces the logical inverse of its condition.</span></span> <span data-ttu-id="80312-243">يجب أن يكون به شرط واحد فقط.</span><span class="sxs-lookup"><span data-stu-id="80312-243">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="80312-244">Not‏[expr]، الحرف المزيد: !expr</span><span class="sxs-lookup"><span data-stu-id="80312-244">Not[expr], infix: !expr</span></span></td>
<td><ul>
<li><span data-ttu-id="80312-245"><strong>عامل التشغيل:</strong> Not‏[x] &amp; Not‏[y =‏=‏ 3]</span><span class="sxs-lookup"><span data-stu-id="80312-245"><strong>Operator:</strong> Not[x] &amp; Not[y == 3]</span></span></li>
<li><span data-ttu-id="80312-246"><strong>تدوين الحرف المزيد:</strong> !‏x!‏(y =‏= 3)</span><span class="sxs-lookup"><span data-stu-id="80312-246"><strong>Infix notation:</strong> !x!(y == 3)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="80312-247">توضح الأمثلة في الجدول التالي كيفية كتابة تدوين الحرف المزيد.</span><span class="sxs-lookup"><span data-stu-id="80312-247">The examples in the next table show how to write infix notation.</span></span>

| <span data-ttu-id="80312-248">تدوين الحرف المزيد</span><span class="sxs-lookup"><span data-stu-id="80312-248">Infix notation</span></span>    | <span data-ttu-id="80312-249">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="80312-249">Description</span></span>                                                                                   |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="80312-250">x + y + z</span><span class="sxs-lookup"><span data-stu-id="80312-250">x + y + z</span></span>         | <span data-ttu-id="80312-251">الجمع</span><span class="sxs-lookup"><span data-stu-id="80312-251">Addition</span></span>                                                                                      |
| <span data-ttu-id="80312-252">x \* y \* z</span><span class="sxs-lookup"><span data-stu-id="80312-252">x \* y \* z</span></span>       | <span data-ttu-id="80312-253">الضرب</span><span class="sxs-lookup"><span data-stu-id="80312-253">Multiplication</span></span>                                                                                |
| <span data-ttu-id="80312-254">x - y</span><span class="sxs-lookup"><span data-stu-id="80312-254">x - y</span></span>             | <span data-ttu-id="80312-255">يتم تحويل الطرح الثنائي مثل الإضافة الثنائية بقيمة ثانية سالبة.</span><span class="sxs-lookup"><span data-stu-id="80312-255">Binary subtraction is translated the same as binary addition where there is a negated second.</span></span> |
| <span data-ttu-id="80312-256">x ^ y ^ z</span><span class="sxs-lookup"><span data-stu-id="80312-256">x ^ y ^ z</span></span>         | <span data-ttu-id="80312-257">العلامة الأسية بالتجميع الصحيح</span><span class="sxs-lookup"><span data-stu-id="80312-257">Exponentiation that has right associativity</span></span>                                                   |
| <span data-ttu-id="80312-258">!x</span><span class="sxs-lookup"><span data-stu-id="80312-258">!x</span></span>                | <span data-ttu-id="80312-259">قيمة غير منطقية</span><span class="sxs-lookup"><span data-stu-id="80312-259">Boolean not</span></span>                                                                                   |
| <span data-ttu-id="80312-260">x -: y</span><span class="sxs-lookup"><span data-stu-id="80312-260">x -: y</span></span>            | <span data-ttu-id="80312-261">تضمين منطقي</span><span class="sxs-lookup"><span data-stu-id="80312-261">Boolean implication</span></span>                                                                           |
| <span data-ttu-id="80312-262">×</span><span class="sxs-lookup"><span data-stu-id="80312-262">x</span></span> | <span data-ttu-id="80312-263">y</span><span class="sxs-lookup"><span data-stu-id="80312-263">y</span></span> | <span data-ttu-id="80312-264">z</span><span class="sxs-lookup"><span data-stu-id="80312-264">z</span></span>         | <span data-ttu-id="80312-265">قيمة or منطقية</span><span class="sxs-lookup"><span data-stu-id="80312-265">Boolean or</span></span>                                                                                    |
| <span data-ttu-id="80312-266">x & y & z</span><span class="sxs-lookup"><span data-stu-id="80312-266">x & y & z</span></span>         | <span data-ttu-id="80312-267">قيمة and منطقية</span><span class="sxs-lookup"><span data-stu-id="80312-267">Boolean and</span></span>                                                                                   |
| <span data-ttu-id="80312-268">x =‏=‏ y =‏=‏ z</span><span class="sxs-lookup"><span data-stu-id="80312-268">x == y == z</span></span>       | <span data-ttu-id="80312-269">التساوي</span><span class="sxs-lookup"><span data-stu-id="80312-269">Equality</span></span>                                                                                      |
| <span data-ttu-id="80312-270">x !=‏ y !=‏ z</span><span class="sxs-lookup"><span data-stu-id="80312-270">x != y != z</span></span>       | <span data-ttu-id="80312-271">محدد</span><span class="sxs-lookup"><span data-stu-id="80312-271">Distinct</span></span>                                                                                      |
| <span data-ttu-id="80312-272">x &lt; y &lt; z</span><span class="sxs-lookup"><span data-stu-id="80312-272">x &lt; y &lt; z</span></span>   | <span data-ttu-id="80312-273">أقل من  </span><span class="sxs-lookup"><span data-stu-id="80312-273">Less than</span></span>                                                                                     |
| <span data-ttu-id="80312-274">x &gt; y &gt; z</span><span class="sxs-lookup"><span data-stu-id="80312-274">x &gt; y &gt; z</span></span>   | <span data-ttu-id="80312-275">أكبر من</span><span class="sxs-lookup"><span data-stu-id="80312-275">Greater than</span></span>                                                                                  |
| <span data-ttu-id="80312-276">x &lt;=‏‏ y &lt;=‏‏ z</span><span class="sxs-lookup"><span data-stu-id="80312-276">x &lt;= y &lt;= z</span></span> | <span data-ttu-id="80312-277">أقل من أو يساوي</span><span class="sxs-lookup"><span data-stu-id="80312-277">Less than or equal to</span></span>                                                                         |
| <span data-ttu-id="80312-278">x &gt;=‏ y &gt;=‏ z</span><span class="sxs-lookup"><span data-stu-id="80312-278">x &gt;= y &gt;= z</span></span> | <span data-ttu-id="80312-279">أكبر من أو يساوي</span><span class="sxs-lookup"><span data-stu-id="80312-279">Greater than or equal to</span></span>                                                                      |
| <span data-ttu-id="80312-280">(x)</span><span class="sxs-lookup"><span data-stu-id="80312-280">(x)</span></span>               | <span data-ttu-id="80312-281">تتجاوز الأقواس الأسبقية الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="80312-281">Parentheses override default precedence.</span></span>                                                      |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a><span data-ttu-id="80312-282">لماذا لم يتم التحقق من صحة قيود التعبير لدي بشكل صحيح؟</span><span class="sxs-lookup"><span data-stu-id="80312-282">Why aren't my expression constraints validated correctly?</span></span>
<span data-ttu-id="80312-283">لا يمكنك استخدام الكلمات الرئيسية المحجوزة كأسماء أدوات الحلول للسمات أو المكونات أو المكونات الفرعية في نموذج تكوين منتج.</span><span class="sxs-lookup"><span data-stu-id="80312-283">You can't use reserved keywords as solver names for attributes, components, or subcomponents in a product configuration model.</span></span> <span data-ttu-id="80312-284">فيما يلي قائمة بالكلمات الأساسية التي لا يمكن استخدامها:‬</span><span class="sxs-lookup"><span data-stu-id="80312-284">Here is a list of the reserved keywords that you can't use:</span></span>

-   <span data-ttu-id="80312-285">الحد الأقصى</span><span class="sxs-lookup"><span data-stu-id="80312-285">Ceiling</span></span>
-   <span data-ttu-id="80312-286">العنصر</span><span class="sxs-lookup"><span data-stu-id="80312-286">Element</span></span>
-   <span data-ttu-id="80312-287">متساوٍ</span><span class="sxs-lookup"><span data-stu-id="80312-287">Equal</span></span>
-   <span data-ttu-id="80312-288">الأرضية</span><span class="sxs-lookup"><span data-stu-id="80312-288">Floor</span></span>
-   <span data-ttu-id="80312-289">إذا</span><span class="sxs-lookup"><span data-stu-id="80312-289">If</span></span>
-   <span data-ttu-id="80312-290">أقل</span><span class="sxs-lookup"><span data-stu-id="80312-290">Less</span></span>
-   <span data-ttu-id="80312-291">أكبر</span><span class="sxs-lookup"><span data-stu-id="80312-291">Greater</span></span>
-   <span data-ttu-id="80312-292">يعني</span><span class="sxs-lookup"><span data-stu-id="80312-292">Implies</span></span>
-   <span data-ttu-id="80312-293">السجل</span><span class="sxs-lookup"><span data-stu-id="80312-293">Log</span></span>
-   <span data-ttu-id="80312-294">الحد الأقصى</span><span class="sxs-lookup"><span data-stu-id="80312-294">Max</span></span>
-   <span data-ttu-id="80312-295">الحد الأدنى</span><span class="sxs-lookup"><span data-stu-id="80312-295">Min</span></span>
-   <span data-ttu-id="80312-296">ناقص</span><span class="sxs-lookup"><span data-stu-id="80312-296">Minus</span></span>
-   <span data-ttu-id="80312-297">زائد</span><span class="sxs-lookup"><span data-stu-id="80312-297">Plus</span></span>
-   <span data-ttu-id="80312-298">القدرة</span><span class="sxs-lookup"><span data-stu-id="80312-298">Power</span></span>
-   <span data-ttu-id="80312-299">الأوقات</span><span class="sxs-lookup"><span data-stu-id="80312-299">Times</span></span>
-   <span data-ttu-id="80312-300">الجزء</span><span class="sxs-lookup"><span data-stu-id="80312-300">Slot</span></span>
-   <span data-ttu-id="80312-301">نموذج</span><span class="sxs-lookup"><span data-stu-id="80312-301">Model</span></span>
-   <span data-ttu-id="80312-302">القرار</span><span class="sxs-lookup"><span data-stu-id="80312-302">Decision</span></span>
-   <span data-ttu-id="80312-303">الهدف</span><span class="sxs-lookup"><span data-stu-id="80312-303">Goal</span></span>


<a name="see-also"></a><span data-ttu-id="80312-304">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="80312-304">See also</span></span>
--------

<span data-ttu-id="80312-305">[إنشاء قيد تعبير (دليل المهام)(tasks/add-expression-constraint-product-configuration-model.md)</span><span class="sxs-lookup"><span data-stu-id="80312-305">[Create an expression constraint (Task guide)(tasks/add-expression-constraint-product-configuration-model.md)</span></span>

[<span data-ttu-id="80312-306">إضافة عملية حسابية إلى نموذج تكوين منتج (دليل المهام)</span><span class="sxs-lookup"><span data-stu-id="80312-306">Add a calculation to a product configuration model (Task guide)</span></span>](tasks/add-calculation-product-configuration-model.md)




