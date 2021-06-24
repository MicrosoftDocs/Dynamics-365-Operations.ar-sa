---
title: قيود التعبير وقيود الجدول في نماذج تكوين المنتج
description: يصف هذا الموضوع استخدام قيود التعبير وقيود الجدول. تتحكم القيود في قيم السمات التي يمكن تحديدها عند تكوين المنتجات لأمر المبيعات أو عرض أسعار المبيعات أو أمر الشراء أو أمر الإنتاج. يمكنك استخدام قيود التعبير أو قيود الجدول، اعتمادًا على الطريقة التي تفضل بها إنشاء القيود.
author: cvocph
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PCGlobalTableConstraintEdit, PCProductConfigurationModelDetails, PCTableConstraintAttachAttributeTree, PCTableConstraintDefinition
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 57b0a11fbadd7e39140085eebcaa96b961196f32
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189858"
---
# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a><span data-ttu-id="fb46b-105">قيود التعبير وقيود الجدول في نماذج تكوين المنتج</span><span class="sxs-lookup"><span data-stu-id="fb46b-105">Expression constraints and table constraints in product configuration models</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fb46b-106">يصف هذا الموضوع استخدام قيود التعبير وقيود الجدول.</span><span class="sxs-lookup"><span data-stu-id="fb46b-106">This topic describes the use of expression constraints and table constraints.</span></span> <span data-ttu-id="fb46b-107">تتحكم القيود في قيم السمات التي يمكن تحديدها عند تكوين المنتجات لأمر المبيعات أو عرض أسعار المبيعات أو أمر الشراء أو أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="fb46b-107">Constraints control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="fb46b-108">يمكنك استخدام قيود التعبير أو قيود الجدول، اعتمادًا على الطريقة التي تفضل بها إنشاء القيود.</span><span class="sxs-lookup"><span data-stu-id="fb46b-108">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> 

<span data-ttu-id="fb46b-109">يتم استخدام القيود للتحكم في قيم السمات التي يمكن تحديدها عند تكوين المنتجات لأمر المبيعات أو عرض أسعار المبيعات أو أمر الشراء أو أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="fb46b-109">Constraints are used to control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="fb46b-110">يمكنك استخدام قيود التعبير أو قيود الجدول، اعتمادًا على الطريقة التي تفضل بها إنشاء القيود.</span><span class="sxs-lookup"><span data-stu-id="fb46b-110">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span>

## <a name="what-are-expression-constraints"></a><span data-ttu-id="fb46b-111">ما هي قيود التعبير؟</span><span class="sxs-lookup"><span data-stu-id="fb46b-111">What are expression constraints?</span></span>
<span data-ttu-id="fb46b-112">تتسم قيود التعبير بتعبير يستخدم الدالات والمعامِلات الحسابية المنطقية.</span><span class="sxs-lookup"><span data-stu-id="fb46b-112">Expression constraints are characterized by an expression that uses arithmetic and Boolean operators and functions.</span></span> <span data-ttu-id="fb46b-113">تتم كتابة قيد تعبير لمكون محدد في نموذج تكوين منتج.</span><span class="sxs-lookup"><span data-stu-id="fb46b-113">An expression constraint is written for a specific component in a product configuration model.</span></span> <span data-ttu-id="fb46b-114">لا يمكن إعادة استخدامها بواسطة أو بالمشاركة مع مكون آخر.</span><span class="sxs-lookup"><span data-stu-id="fb46b-114">It can't be reused by or shared with another component.</span></span> <span data-ttu-id="fb46b-115">ومع ذلك، يمكن لقيود التعبير لمكون الإشارة إلى سمات المكونات الفرعية للمكون.</span><span class="sxs-lookup"><span data-stu-id="fb46b-115">However, the expression constraints for a component can reference attributes of the component's subcomponents.</span></span>

## <a name="what-are-table-constraints"></a><span data-ttu-id="fb46b-116">ما هي قيود الجدول؟</span><span class="sxs-lookup"><span data-stu-id="fb46b-116">What are table constraints?</span></span>
<span data-ttu-id="fb46b-117">تسرد قيود الجدول مجموعات القيم المسموح بها للسمات عندما تقوم بتكوين منتج.</span><span class="sxs-lookup"><span data-stu-id="fb46b-117">Table constraints list the combinations of values that are allowed for attributes when you configure a product.</span></span> <span data-ttu-id="fb46b-118">يمكن استخدام تعريفات قيود الجدول بشكل عام.</span><span class="sxs-lookup"><span data-stu-id="fb46b-118">Table constraint definitions can be used generically.</span></span> <span data-ttu-id="fb46b-119">عند إنشاء قيد جدول لمكون في نموذج تكوين منتج، حدد تعريف قيد جدول.</span><span class="sxs-lookup"><span data-stu-id="fb46b-119">When you create a table constraint for a component in a product configuration model, you select a table constraint definition.</span></span> <span data-ttu-id="fb46b-120">لإنشاء المجموعات المسموح بها، تقوم بإضافة سمات الأنواع المحددة للمكونات.</span><span class="sxs-lookup"><span data-stu-id="fb46b-120">To create the combinations that are allowed, you add attributes of specific types to the components.</span></span> <span data-ttu-id="fb46b-121">يحتوي كل نوع سمة على قيمة محددة.</span><span class="sxs-lookup"><span data-stu-id="fb46b-121">Each attribute type has a specific value.</span></span>

### <a name="example-of-a-table-constraint"></a><span data-ttu-id="fb46b-122">مثال على قيد جدول</span><span class="sxs-lookup"><span data-stu-id="fb46b-122">Example of a table constraint</span></span>

<span data-ttu-id="fb46b-123">يوضح هذا المثال كيفية تحديد تكوين مكبر صوت لألوان الكابينة محددة والأجزاء الأمامية.</span><span class="sxs-lookup"><span data-stu-id="fb46b-123">This example shows how you can limit the configuration of a speaker to specific cabinet finishes and fronts.</span></span> <span data-ttu-id="fb46b-124">يعرض الجدول الأول ألوان الكابينة والأجزاء الأمامية المتوفرة بشكل عام للتكوين.</span><span class="sxs-lookup"><span data-stu-id="fb46b-124">The first table shows the cabinet finishes and fronts that are generally available for configuration.</span></span> <span data-ttu-id="fb46b-125">ويتم تحديد القيم لنوعي السمات **لون الكابينة** و **الشبكة الأمامية**.</span><span class="sxs-lookup"><span data-stu-id="fb46b-125">The values are defined for the **Cabinet finish** and **Front grill** attribute types.</span></span>

| <span data-ttu-id="fb46b-126">نوع السمة</span><span class="sxs-lookup"><span data-stu-id="fb46b-126">Attribute type</span></span> | <span data-ttu-id="fb46b-127">القيم</span><span class="sxs-lookup"><span data-stu-id="fb46b-127">Values</span></span>                      |
|----------------|-----------------------------|
| <span data-ttu-id="fb46b-128">لون الكابينة</span><span class="sxs-lookup"><span data-stu-id="fb46b-128">Cabinet finish</span></span> | <span data-ttu-id="fb46b-129">أسود، وبلوطي، وروزوود، وأبيض</span><span class="sxs-lookup"><span data-stu-id="fb46b-129">Black, Oak, Rosewood, White</span></span> |
| <span data-ttu-id="fb46b-130">الشبكة الأمامية</span><span class="sxs-lookup"><span data-stu-id="fb46b-130">Front grill</span></span>    | <span data-ttu-id="fb46b-131">أسود، ومعدني، وأبيض</span><span class="sxs-lookup"><span data-stu-id="fb46b-131">Black, Metal, White</span></span>         |

<span data-ttu-id="fb46b-132">يُظهر الجدول التالي هذا المجموعات المحددة من قِبل قيد الجدول **اللون واللمسة النهائية**.</span><span class="sxs-lookup"><span data-stu-id="fb46b-132">The next table shows the combinations that are defined by the **Color and finish** table constraint.</span></span> <span data-ttu-id="fb46b-133">باستخدام هذا القيد في الجدول، يمكنك تكوين مكبر صوت بلون بلوطي وشبكة سوداء، ولون روزوود وشبكة بيضاء، وهكذا.</span><span class="sxs-lookup"><span data-stu-id="fb46b-133">By using this table constraint, you can configure a speaker that has an oak finish and a black grill, a Rosewood finish and a white grill, and so on.</span></span>

| <span data-ttu-id="fb46b-134">إنهاء</span><span class="sxs-lookup"><span data-stu-id="fb46b-134">Finish</span></span>         | <span data-ttu-id="fb46b-135">الشبكة</span><span class="sxs-lookup"><span data-stu-id="fb46b-135">Grill</span></span>                       |
|----------------|-----------------------------|
| <span data-ttu-id="fb46b-136">بلوطي</span><span class="sxs-lookup"><span data-stu-id="fb46b-136">Oak</span></span>            | <span data-ttu-id="fb46b-137">أسود</span><span class="sxs-lookup"><span data-stu-id="fb46b-137">Black</span></span>                       |
| <span data-ttu-id="fb46b-138">روزوود</span><span class="sxs-lookup"><span data-stu-id="fb46b-138">Rosewood</span></span>       | <span data-ttu-id="fb46b-139">أبيض</span><span class="sxs-lookup"><span data-stu-id="fb46b-139">White</span></span>                       |
| <span data-ttu-id="fb46b-140">أبيض</span><span class="sxs-lookup"><span data-stu-id="fb46b-140">White</span></span>          | <span data-ttu-id="fb46b-141">أسود</span><span class="sxs-lookup"><span data-stu-id="fb46b-141">Black</span></span>                       |
| <span data-ttu-id="fb46b-142">أبيض</span><span class="sxs-lookup"><span data-stu-id="fb46b-142">White</span></span>          | <span data-ttu-id="fb46b-143">أبيض</span><span class="sxs-lookup"><span data-stu-id="fb46b-143">White</span></span>                       |
| <span data-ttu-id="fb46b-144">أسود</span><span class="sxs-lookup"><span data-stu-id="fb46b-144">Black</span></span>          | <span data-ttu-id="fb46b-145">أسود</span><span class="sxs-lookup"><span data-stu-id="fb46b-145">Black</span></span>                       |
| <span data-ttu-id="fb46b-146">أسود</span><span class="sxs-lookup"><span data-stu-id="fb46b-146">Black</span></span>          | <span data-ttu-id="fb46b-147">معدني</span><span class="sxs-lookup"><span data-stu-id="fb46b-147">Metal</span></span>                       | 

<span data-ttu-id="fb46b-148">يمكنك إنشاء قيود جدول إما محددة بواسطة المستخدم أو محددة بواسطة النظام.</span><span class="sxs-lookup"><span data-stu-id="fb46b-148">You can create system-defined and user-defined table constraints.</span></span> <span data-ttu-id="fb46b-149">لمزيد من المعلومات، راجع [قيود الجدول المحددة من قِبل النظام والمحددة من قِبل المستخدم](system-defined-user-defined-table-constraints.md).</span><span class="sxs-lookup"><span data-stu-id="fb46b-149">For more information, see [System-defined and user-defined table constraints](system-defined-user-defined-table-constraints.md).</span></span>

## <a name="what-syntax-should-be-used-to-write-constraints"></a><span data-ttu-id="fb46b-150">‏‫ما بنية الجملة التي يجب استخدامها لكتابة القيود؟</span><span class="sxs-lookup"><span data-stu-id="fb46b-150">What syntax should be used to write constraints?</span></span>
<span data-ttu-id="fb46b-151">يجب عليك استخدام بنية جملة لغة تصميم التحسين (OML) عند كتابة القيود.</span><span class="sxs-lookup"><span data-stu-id="fb46b-151">You must use Optimization Modeling Language (OML) syntax when you write constraints.</span></span> <span data-ttu-id="fb46b-152">يستخدم النظام أداة حل القيود Microsoft Solver Foundation لحل القيود.</span><span class="sxs-lookup"><span data-stu-id="fb46b-152">The system uses Microsoft Solver Foundation constraint solver to solve the constraints.</span></span>

## <a name="should-i-use-table-constraints-or-expression-constraints"></a><span data-ttu-id="fb46b-153">هل يجب استخدام قيود الجدول أو قيود التعبير؟</span><span class="sxs-lookup"><span data-stu-id="fb46b-153">Should I use table constraints or expression constraints?</span></span>
<span data-ttu-id="fb46b-154">يمكنك استخدام قيود التعبير أو قيود الجدول، اعتمادًا على الطريقة التي تفضل بها إنشاء القيود.</span><span class="sxs-lookup"><span data-stu-id="fb46b-154">You can use either expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> <span data-ttu-id="fb46b-155">يمكنك إنشاء قيد جدول كمصفوفة، بينما يكون قيد التعبير عبارة فردية.</span><span class="sxs-lookup"><span data-stu-id="fb46b-155">You build a table constraint as a matrix, whereas an expression constraint is an individual statement.</span></span> <span data-ttu-id="fb46b-156">عندما تقوم بتكوين منتج، فلا يهم نوع القيد المستخدَم.</span><span class="sxs-lookup"><span data-stu-id="fb46b-156">When you configure a product, it doesn't matter what kind of constraint is used.</span></span> <span data-ttu-id="fb46b-157">يعرض المثال التالي مدى اختلاف الطريقتين.</span><span class="sxs-lookup"><span data-stu-id="fb46b-157">The following example shows how the two methods differ.</span></span>  

<span data-ttu-id="fb46b-158">عند قيامك بتكوين منتج باستخدام إعدادات القيود التالية، يتم السماح بهذه المجموعات:</span><span class="sxs-lookup"><span data-stu-id="fb46b-158">When you configure a product by using the following constraint setups, these combinations are allowed:</span></span>

-   <span data-ttu-id="fb46b-159">منتج باللون الأسود، وبحجم 30 أو 50</span><span class="sxs-lookup"><span data-stu-id="fb46b-159">A product in the color Black, and in size 30 or 50</span></span>
-   <span data-ttu-id="fb46b-160">منتج باللون الأحمر، وبحجم 20</span><span class="sxs-lookup"><span data-stu-id="fb46b-160">A product in the color Red and in size 20</span></span>

### <a name="table-constraint-setup"></a><span data-ttu-id="fb46b-161">إعداد قيد الجدول</span><span class="sxs-lookup"><span data-stu-id="fb46b-161">Table constraint setup</span></span>

| <span data-ttu-id="fb46b-162">اللون</span><span class="sxs-lookup"><span data-stu-id="fb46b-162">Color</span></span> | <span data-ttu-id="fb46b-163">الحجم</span><span class="sxs-lookup"><span data-stu-id="fb46b-163">Size</span></span> |
|-------|------|
| <span data-ttu-id="fb46b-164">أسود</span><span class="sxs-lookup"><span data-stu-id="fb46b-164">Black</span></span> | <span data-ttu-id="fb46b-165">30</span><span class="sxs-lookup"><span data-stu-id="fb46b-165">30</span></span>   |
| <span data-ttu-id="fb46b-166">أسود</span><span class="sxs-lookup"><span data-stu-id="fb46b-166">Black</span></span> | <span data-ttu-id="fb46b-167">50</span><span class="sxs-lookup"><span data-stu-id="fb46b-167">50</span></span>   |
| <span data-ttu-id="fb46b-168">أحمر</span><span class="sxs-lookup"><span data-stu-id="fb46b-168">Red</span></span>   | <span data-ttu-id="fb46b-169">20</span><span class="sxs-lookup"><span data-stu-id="fb46b-169">20</span></span>   |

### <a name="expression-constraint-setup"></a><span data-ttu-id="fb46b-170">إعداد قيد التعبير</span><span class="sxs-lookup"><span data-stu-id="fb46b-170">Expression constraint setup</span></span>

<span data-ttu-id="fb46b-171">(لون == "أسود" و (حجم == "30" | حجم == "50")) | (لون == "أحمر" وحجم = "20")</span><span class="sxs-lookup"><span data-stu-id="fb46b-171">(Color == "Black" & (size == "30" | size == "50")) | (color == "Red" & size = "20")</span></span>

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a><span data-ttu-id="fb46b-172">هل يجب استخدام المعامِلات أو تدوين الحرف المزيد عند كتابة قيود التعبير؟</span><span class="sxs-lookup"><span data-stu-id="fb46b-172">Should I use operators or infix notation when I write expression constraints?</span></span>
<span data-ttu-id="fb46b-173">يمكنك كتابة قيد تعبير إما باستخدام تدوين الحروف المزيدة أو معامِلات البادئات المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="fb46b-173">You can write an expression constraint by using either the available prefix operators or infix notation.</span></span> <span data-ttu-id="fb46b-174">لا يمكنك استخدام تدوين الحروف المزيدة لمعامِلات ‏‫القيمة **المطلقة**، و **الحد الأدنى**، و **الحد الأقصى**.</span><span class="sxs-lookup"><span data-stu-id="fb46b-174">For the **Min**, **Max**, and **Abs** operators, you can't use infix notation.</span></span> <span data-ttu-id="fb46b-175">ويتم تضمين هذه المعامِلات كمعامِلات قياسية في معظم لغات البرمجة.</span><span class="sxs-lookup"><span data-stu-id="fb46b-175">These operators are included as standard operators in most programming languages.</span></span>

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a><span data-ttu-id="fb46b-176">ما هي المعامِلات وتدوينات الحروف المزيدة التي يمكن استخدامها عند كتابة قيود التعبير؟</span><span class="sxs-lookup"><span data-stu-id="fb46b-176">What operators and infix notation can I use when I write expression constraints?</span></span>
<span data-ttu-id="fb46b-177">تسرد الجداول التالية المعامِلات وتدوينات الحروف المزيدة التي يمكنك استخدامها عند كتابة قيد تعبير لمكون في نموذج تكوين منتج.</span><span class="sxs-lookup"><span data-stu-id="fb46b-177">The following tables list the operators and infix notation that you can use when you write an expression constraint for a component in a product configuration model.</span></span> <span data-ttu-id="fb46b-178">في الأمثلة الواردة في هذا الجدول الأول، يمكنك الاطلاع على كيفية كتابة تعبير باستخدام المعامِلات أو تدوينات الحروف المزيدة.</span><span class="sxs-lookup"><span data-stu-id="fb46b-178">The examples in the first table show how to write an expression by using either infix notation or operators.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fb46b-179">عامل تشغيل</span><span class="sxs-lookup"><span data-stu-id="fb46b-179">Operator</span></span></th>
<th><span data-ttu-id="fb46b-180">الوصف</span><span class="sxs-lookup"><span data-stu-id="fb46b-180">Description</span></span></th>
<th><span data-ttu-id="fb46b-181">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="fb46b-181">Syntax</span></span></th>
<th><span data-ttu-id="fb46b-182">أمثلة</span><span class="sxs-lookup"><span data-stu-id="fb46b-182">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fb46b-183">يعني</span><span class="sxs-lookup"><span data-stu-id="fb46b-183">Implies</span></span></td>
<td><span data-ttu-id="fb46b-184">يكون هذا الأمر صحيحًا إذا كان الشرط الأول خاطئًا، والشرط الثاني صحيح، أو كليهما.</span><span class="sxs-lookup"><span data-stu-id="fb46b-184">This is true if the first condition is false, the second condition is true, or both.</span></span></td>
<td><span data-ttu-id="fb46b-185">يعني [a أو b]، الحرف المزيد: a -: b</span><span class="sxs-lookup"><span data-stu-id="fb46b-185">Implies[a, b], infix: a -: b</span></span></td>
<td><ul>
<li><span data-ttu-id="fb46b-186"><strong>عامل التشغيل:</strong> يتضمن[x‏ != 0، y &gt;=‏ 0]</span><span class="sxs-lookup"><span data-stu-id="fb46b-186"><strong>Operator:</strong> Implies[x != 0, y &gt;= 0]</span></span></li>
<li><span data-ttu-id="fb46b-187"><strong>تدوين الحرف المزيد:</strong> x‏ != 0 -‏: y &gt;=‏ 0</span><span class="sxs-lookup"><span data-stu-id="fb46b-187"><strong>Infix notation:</strong> x != 0 -: y &gt;= 0</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fb46b-188">و</span><span class="sxs-lookup"><span data-stu-id="fb46b-188">And</span></span></td>
<td><span data-ttu-id="fb46b-189">يكون هذا الأمر صحيحًا فقط إذا تحققت جميع الشروط.</span><span class="sxs-lookup"><span data-stu-id="fb46b-189">This is true only if all conditions are true.</span></span> <span data-ttu-id="fb46b-190">إذا كان عدد الشروط هو 0 (صفر)، ينتج قيمة <strong>صحيحة</strong>.</span><span class="sxs-lookup"><span data-stu-id="fb46b-190">If the number of conditions is 0 (zero), it produces <strong>True</strong>.</span></span></td>
<td><span data-ttu-id="fb46b-191">And‏[args]، الحرف المزيد: a &amp; b &amp; ... &amp; z</span><span class="sxs-lookup"><span data-stu-id="fb46b-191">And[args], infix: a &amp; b &amp; ... &amp; z</span></span></td>
<td><ul>
<li><span data-ttu-id="fb46b-192"><strong>عامل التشغيل:</strong> And‏[x‏ == 2، y &lt;=‏ 2]</span><span class="sxs-lookup"><span data-stu-id="fb46b-192"><strong>Operator:</strong> And[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="fb46b-193"><strong>تدوين الحرف المزيد:</strong> x‏ == 2 &amp; y &lt;=‏ 2</span><span class="sxs-lookup"><span data-stu-id="fb46b-193"><strong>Infix notation:</strong> x == 2 &amp; y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fb46b-194">أو</span><span class="sxs-lookup"><span data-stu-id="fb46b-194">Or</span></span></td>
<td><span data-ttu-id="fb46b-195">يكون هذا الأمر صحيحًا إذا كان أي شرط صحيح.</span><span class="sxs-lookup"><span data-stu-id="fb46b-195">This is true if any condition is true.</span></span> <span data-ttu-id="fb46b-196">إذا كان عدد الشروط هو 0 (صفر)، تنتج قيمة <strong>خاطئة</strong>.</span><span class="sxs-lookup"><span data-stu-id="fb46b-196">If the number of conditions is 0 (zero), it produces <strong>False</strong>.</span></span></td>
<td><span data-ttu-id="fb46b-197">Or‏[args]، الحرف المزيد: a‏ | b |‏ ... | z</span><span class="sxs-lookup"><span data-stu-id="fb46b-197">Or[args], infix: a | b | ... | z</span></span></td>
<td><ul>
<li><span data-ttu-id="fb46b-198"><strong>عامل التشغيل:</strong> Or‏[x‏ == 2، y &lt;=‏ 2]</span><span class="sxs-lookup"><span data-stu-id="fb46b-198"><strong>Operator:</strong> Or[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="fb46b-199"><strong>تدوين الحرف المزيد:</strong> x =‏=‏ 2 | y &lt;=‏ 2</span><span class="sxs-lookup"><span data-stu-id="fb46b-199"><strong>Infix notation:</strong> x == 2 | y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fb46b-200">زائد</span><span class="sxs-lookup"><span data-stu-id="fb46b-200">Plus</span></span></td>
<td><span data-ttu-id="fb46b-201">وهذا يلخص الشروط.</span><span class="sxs-lookup"><span data-stu-id="fb46b-201">This sums its conditions.</span></span> <span data-ttu-id="fb46b-202">إذا كان عدد الشروط هو 0 (صفر)، تنتج قيمة <strong>0</strong>.</span><span class="sxs-lookup"><span data-stu-id="fb46b-202">If the number of conditions is 0 (zero), it produces <strong>0</strong>.</span></span></td>
<td><span data-ttu-id="fb46b-203">Plus‏[args]، الحرف المزيد: a‏ + b‏ + ... + z</span><span class="sxs-lookup"><span data-stu-id="fb46b-203">Plus[args], infix: a + b + ... + z</span></span></td>
<td><ul>
<li><span data-ttu-id="fb46b-204"><strong>عامل التشغيل:</strong> زائد[x،‏ y،‏ 2] =‏=‏ z</span><span class="sxs-lookup"><span data-stu-id="fb46b-204"><strong>Operator:</strong> Plus[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="fb46b-205"><strong>تدوين الحرف المزيد:</strong> x + y + 2 =‏=‏ z</span><span class="sxs-lookup"><span data-stu-id="fb46b-205"><strong>Infix notation:</strong> x + y + 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fb46b-206">ناقص</span><span class="sxs-lookup"><span data-stu-id="fb46b-206">Minus</span></span></td>
<td><span data-ttu-id="fb46b-207">هذا يناقض الوسيطة.</span><span class="sxs-lookup"><span data-stu-id="fb46b-207">This negates its argument.</span></span> <span data-ttu-id="fb46b-208">يجب أن يكون به شرط واحد فقط.</span><span class="sxs-lookup"><span data-stu-id="fb46b-208">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="fb46b-209">Minus‏[expr]، الحرف المزيد: -expr</span><span class="sxs-lookup"><span data-stu-id="fb46b-209">Minus[expr], infix: -expr</span></span></td>
<td><ul>
<li><span data-ttu-id="fb46b-210"><strong>عامل التشغيل:</strong> ناقص[x] =‏=‏ y</span><span class="sxs-lookup"><span data-stu-id="fb46b-210"><strong>Operator:</strong> Minus[x] == y</span></span></li>
<li><span data-ttu-id="fb46b-211"><strong>تدوين الحرف المزيد:</strong> -x =‏=‏ y</span><span class="sxs-lookup"><span data-stu-id="fb46b-211"><strong>Infix notation:</strong> -x == y</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fb46b-212">القيمة المطلقة</span><span class="sxs-lookup"><span data-stu-id="fb46b-212">Abs</span></span></td>
<td><span data-ttu-id="fb46b-213">وهذا يأخذ القيمة المطلقة من شرطها.</span><span class="sxs-lookup"><span data-stu-id="fb46b-213">This takes the absolute value of its condition.</span></span> <span data-ttu-id="fb46b-214">يجب أن يكون به شرط واحد فقط.</span><span class="sxs-lookup"><span data-stu-id="fb46b-214">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="fb46b-215">Abs‏[expr]</span><span class="sxs-lookup"><span data-stu-id="fb46b-215">Abs[expr]</span></span></td>
<td><span data-ttu-id="fb46b-216"><strong>عامل التشغيل:</strong> Abs‏[x]</span><span class="sxs-lookup"><span data-stu-id="fb46b-216"><strong>Operator:</strong> Abs[x]</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fb46b-217">الأوقات</span><span class="sxs-lookup"><span data-stu-id="fb46b-217">Times</span></span></td>
<td><span data-ttu-id="fb46b-218">يأخذ هذا المنتج من شروطه.</span><span class="sxs-lookup"><span data-stu-id="fb46b-218">This takes the product of its conditions.</span></span> <span data-ttu-id="fb46b-219">إذا كان عدد الشروط هو 0 (صفر)، تنتج قيمة <strong>1</strong>.</span><span class="sxs-lookup"><span data-stu-id="fb46b-219">If the number of conditions is 0 (zero), it produces <strong>1</strong>.</span></span></td>
<td><span data-ttu-id="fb46b-220">Times‏[args]، الحرف الزائد: a‏ \* b \* ... ‏\* z</span><span class="sxs-lookup"><span data-stu-id="fb46b-220">Times[args], infix: a \* b \* ... \* z</span></span></td>
<td><ul>
<li><span data-ttu-id="fb46b-221"><strong>عامل التشغيل:</strong> أوقات[x،‏ y،‏ 2] =‏=‏ z</span><span class="sxs-lookup"><span data-stu-id="fb46b-221"><strong>Operator:</strong> Times[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="fb46b-222"><strong>تدوين الحرف المزيد:</strong> x \* y \* 2 =‏=‏ z</span><span class="sxs-lookup"><span data-stu-id="fb46b-222"><strong>Infix notation:</strong> x \* y \* 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fb46b-223">القدرة</span><span class="sxs-lookup"><span data-stu-id="fb46b-223">Power</span></span></td>
<td><span data-ttu-id="fb46b-224">يأخذ هذا قيمة أُسية.</span><span class="sxs-lookup"><span data-stu-id="fb46b-224">This takes an exponential.</span></span> <span data-ttu-id="fb46b-225">تنطبق هذه القيمة الأُسية من اليمين لليسار.</span><span class="sxs-lookup"><span data-stu-id="fb46b-225">It applies exponentiation from right to left.</span></span> <span data-ttu-id="fb46b-226">(وبمعنى آخر، إنها مجمَّعة إلى اليمين). وبالتالي، فإن <strong>Power[a, b, c]</strong> يعادل <strong>Power[a, Power[b, c]]</strong>.</span><span class="sxs-lookup"><span data-stu-id="fb46b-226">(In other words, it&#39;s right-associative.) Therefore, <strong>Power[a, b, c]</strong> is equivalent to <strong>Power[a, Power[b, c]]</strong>.</span></span> <span data-ttu-id="fb46b-227"><strong>Power</strong> يمكن استخدامه فقط إذا كان الأس بقيمة موجبة.</span><span class="sxs-lookup"><span data-stu-id="fb46b-227"><strong>Power</strong> can be used only if the exponent is a positive constant.</span></span></td>
<td><span data-ttu-id="fb46b-228">Power‏[args]، الحرف المزيد: a ^ b ^ ... ^ z</span><span class="sxs-lookup"><span data-stu-id="fb46b-228">Power[args], infix: a ^ b ^ ... ^ z</span></span></td>
<td><ul>
<li><span data-ttu-id="fb46b-229"><strong>عامل التشغيل:</strong> Power[x،‏ 2] =‏=‏ y</span><span class="sxs-lookup"><span data-stu-id="fb46b-229"><strong>Operator:</strong> Power[x, 2] == y</span></span></li>
<li><span data-ttu-id="fb46b-230"><strong>تدوين الحرف المزيد:</strong> x ^ 2 =‏=‏ y</span><span class="sxs-lookup"><span data-stu-id="fb46b-230"><strong>Infix notation:</strong> x ^ 2 == y</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fb46b-231">الحد الأقصى</span><span class="sxs-lookup"><span data-stu-id="fb46b-231">Max</span></span></td>
<td><span data-ttu-id="fb46b-232">ينتج عن هذا الأمر الشرط الأكبر.</span><span class="sxs-lookup"><span data-stu-id="fb46b-232">This produces the largest condition.</span></span> <span data-ttu-id="fb46b-233">إذا كان عدد الشروط هو 0 (صفر)، تنتج قيمة <strong>لانهائية</strong>.</span><span class="sxs-lookup"><span data-stu-id="fb46b-233">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="fb46b-234">Max‏[args]</span><span class="sxs-lookup"><span data-stu-id="fb46b-234">Max[args]</span></span></td>
<td><span data-ttu-id="fb46b-235"><strong>عامل التشغيل:</strong> الحد الأقصى[x،‏ y،‏ 2] =‏=‏ z</span><span class="sxs-lookup"><span data-stu-id="fb46b-235"><strong>Operator:</strong> Max[x, y, 2] == z</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fb46b-236">الحد الأدنى</span><span class="sxs-lookup"><span data-stu-id="fb46b-236">Min</span></span></td>
<td><span data-ttu-id="fb46b-237">ينتج عن هذا الأمر الشرط الأصغر.</span><span class="sxs-lookup"><span data-stu-id="fb46b-237">This produces the smallest condition.</span></span> <span data-ttu-id="fb46b-238">إذا كان عدد الشروط هو 0 (صفر)، تنتج قيمة <strong>لانهائية</strong>.</span><span class="sxs-lookup"><span data-stu-id="fb46b-238">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="fb46b-239">Min‏[args]</span><span class="sxs-lookup"><span data-stu-id="fb46b-239">Min[args]</span></span></td>
<td><span data-ttu-id="fb46b-240"><strong>عامل التشغيل:</strong> الحد الأدنى[x،‏‏ y،‏‏ 2] =‏=‏ z</span><span class="sxs-lookup"><span data-stu-id="fb46b-240"><strong>Operator:</strong> Min[x, y, 2] == z</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fb46b-241">ليس</span><span class="sxs-lookup"><span data-stu-id="fb46b-241">Not</span></span></td>
<td><span data-ttu-id="fb46b-242">ينتج عن هذا الأمر العكس المنطقي للشرط.</span><span class="sxs-lookup"><span data-stu-id="fb46b-242">This produces the logical inverse of its condition.</span></span> <span data-ttu-id="fb46b-243">يجب أن يكون به شرط واحد فقط.</span><span class="sxs-lookup"><span data-stu-id="fb46b-243">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="fb46b-244">Not‏[expr]، الحرف المزيد: !expr</span><span class="sxs-lookup"><span data-stu-id="fb46b-244">Not[expr], infix: !expr</span></span></td>
<td><ul>
<li><span data-ttu-id="fb46b-245"><strong>عامل التشغيل:</strong> Not‏[x] &amp; Not‏[y =‏=‏ 3]</span><span class="sxs-lookup"><span data-stu-id="fb46b-245"><strong>Operator:</strong> Not[x] &amp; Not[y == 3]</span></span></li>
<li><span data-ttu-id="fb46b-246"><strong>تدوين الحرف المزيد:</strong> !‏x!‏(y =‏= 3)</span><span class="sxs-lookup"><span data-stu-id="fb46b-246"><strong>Infix notation:</strong> !x!(y == 3)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="fb46b-247">توضح الأمثلة في الجدول التالي كيفية كتابة تدوين الحرف المزيد.</span><span class="sxs-lookup"><span data-stu-id="fb46b-247">The examples in the next table show how to write infix notation.</span></span>


|  <span data-ttu-id="fb46b-248">تدوين الحرف المزيد</span><span class="sxs-lookup"><span data-stu-id="fb46b-248">Infix notation</span></span>   |                                          <span data-ttu-id="fb46b-249">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="fb46b-249">Description</span></span>                                          |
|-------------------|-----------------------------------------------------------------------------------------------|
|     <span data-ttu-id="fb46b-250">x + y + z</span><span class="sxs-lookup"><span data-stu-id="fb46b-250">x + y + z</span></span>     |                                           <span data-ttu-id="fb46b-251">الجمع</span><span class="sxs-lookup"><span data-stu-id="fb46b-251">Addition</span></span>                                            |
|    <span data-ttu-id="fb46b-252">x \* y \* z</span><span class="sxs-lookup"><span data-stu-id="fb46b-252">x \* y \* z</span></span>    |                                        <span data-ttu-id="fb46b-253">الضرب</span><span class="sxs-lookup"><span data-stu-id="fb46b-253">Multiplication</span></span>                                         |
|       <span data-ttu-id="fb46b-254">x - y</span><span class="sxs-lookup"><span data-stu-id="fb46b-254">x - y</span></span>       | <span data-ttu-id="fb46b-255">يتم تحويل الطرح الثنائي مثل الإضافة الثنائية بقيمة ثانية سالبة.</span><span class="sxs-lookup"><span data-stu-id="fb46b-255">Binary subtraction is translated the same as binary addition where there is a negated second.</span></span> |
|     <span data-ttu-id="fb46b-256">x ^ y ^ z</span><span class="sxs-lookup"><span data-stu-id="fb46b-256">x ^ y ^ z</span></span>     |                          <span data-ttu-id="fb46b-257">العلامة الأسية بالتجميع الصحيح</span><span class="sxs-lookup"><span data-stu-id="fb46b-257">Exponentiation that has right associativity</span></span>                          |
|        <span data-ttu-id="fb46b-258">!x</span><span class="sxs-lookup"><span data-stu-id="fb46b-258">!x</span></span>         |                                          <span data-ttu-id="fb46b-259">قيمة غير منطقية</span><span class="sxs-lookup"><span data-stu-id="fb46b-259">Boolean not</span></span>                                          |
|      <span data-ttu-id="fb46b-260">x -: y</span><span class="sxs-lookup"><span data-stu-id="fb46b-260">x -: y</span></span>       |                                      <span data-ttu-id="fb46b-261">تضمين منطقي</span><span class="sxs-lookup"><span data-stu-id="fb46b-261">Boolean implication</span></span>                                      |
|         <span data-ttu-id="fb46b-262">x</span><span class="sxs-lookup"><span data-stu-id="fb46b-262">x</span></span>         |                                               <span data-ttu-id="fb46b-263">y</span><span class="sxs-lookup"><span data-stu-id="fb46b-263">y</span></span>                                               |
|     <span data-ttu-id="fb46b-264">x & y & z</span><span class="sxs-lookup"><span data-stu-id="fb46b-264">x & y & z</span></span>     |                                          <span data-ttu-id="fb46b-265">قيمة and منطقية</span><span class="sxs-lookup"><span data-stu-id="fb46b-265">Boolean and</span></span>                                          |
|    <span data-ttu-id="fb46b-266">x =‏=‏ y =‏=‏ z</span><span class="sxs-lookup"><span data-stu-id="fb46b-266">x == y == z</span></span>    |                                           <span data-ttu-id="fb46b-267">التساوي</span><span class="sxs-lookup"><span data-stu-id="fb46b-267">Equality</span></span>                                            |
|    <span data-ttu-id="fb46b-268">x !=‏ y !=‏ z</span><span class="sxs-lookup"><span data-stu-id="fb46b-268">x != y != z</span></span>    |                                           <span data-ttu-id="fb46b-269">محدد</span><span class="sxs-lookup"><span data-stu-id="fb46b-269">Distinct</span></span>                                            |
|  <span data-ttu-id="fb46b-270">x &lt; y &lt; z</span><span class="sxs-lookup"><span data-stu-id="fb46b-270">x &lt; y &lt; z</span></span>  |                                           <span data-ttu-id="fb46b-271">أقل من  </span><span class="sxs-lookup"><span data-stu-id="fb46b-271">Less than</span></span>                                           |
|  <span data-ttu-id="fb46b-272">x &gt; y &gt; z</span><span class="sxs-lookup"><span data-stu-id="fb46b-272">x &gt; y &gt; z</span></span>  |                                         <span data-ttu-id="fb46b-273">أكبر من</span><span class="sxs-lookup"><span data-stu-id="fb46b-273">Greater than</span></span>                                          |
| <span data-ttu-id="fb46b-274">x &lt;=‏‏ y &lt;=‏‏ z</span><span class="sxs-lookup"><span data-stu-id="fb46b-274">x &lt;= y &lt;= z</span></span> |                                     <span data-ttu-id="fb46b-275">أقل من أو يساوي</span><span class="sxs-lookup"><span data-stu-id="fb46b-275">Less than or equal to</span></span>                                     |
| <span data-ttu-id="fb46b-276">x &gt;=‏ y &gt;=‏ z</span><span class="sxs-lookup"><span data-stu-id="fb46b-276">x &gt;= y &gt;= z</span></span> |                                   <span data-ttu-id="fb46b-277">أكبر من أو يساوي</span><span class="sxs-lookup"><span data-stu-id="fb46b-277">Greater than or equal to</span></span>                                    |
|        <span data-ttu-id="fb46b-278">(x)</span><span class="sxs-lookup"><span data-stu-id="fb46b-278">(x)</span></span>        |                           <span data-ttu-id="fb46b-279">تتجاوز الأقواس الأسبقية الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="fb46b-279">Parentheses override default precedence.</span></span>                            |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a><span data-ttu-id="fb46b-280">لماذا لم يتم التحقق من صحة قيود التعبير لدي بشكل صحيح؟</span><span class="sxs-lookup"><span data-stu-id="fb46b-280">Why aren't my expression constraints validated correctly?</span></span>
<span data-ttu-id="fb46b-281">لا يمكنك استخدام الكلمات الرئيسية المحجوزة كأسماء أدوات الحلول للسمات أو المكونات أو المكونات الفرعية في نموذج تكوين منتج.</span><span class="sxs-lookup"><span data-stu-id="fb46b-281">You can't use reserved keywords as solver names for attributes, components, or subcomponents in a product configuration model.</span></span> <span data-ttu-id="fb46b-282">فيما يلي قائمة بالكلمات الأساسية المحجوزة التي لا يمكن استخدامها:</span><span class="sxs-lookup"><span data-stu-id="fb46b-282">Here is a list of the reserved keywords that you can't use:</span></span>

-   <span data-ttu-id="fb46b-283">الحد الأقصى</span><span class="sxs-lookup"><span data-stu-id="fb46b-283">Ceiling</span></span>
-   <span data-ttu-id="fb46b-284">العنصر</span><span class="sxs-lookup"><span data-stu-id="fb46b-284">Element</span></span>
-   <span data-ttu-id="fb46b-285">متساوٍ</span><span class="sxs-lookup"><span data-stu-id="fb46b-285">Equal</span></span>
-   <span data-ttu-id="fb46b-286">الأرضية</span><span class="sxs-lookup"><span data-stu-id="fb46b-286">Floor</span></span>
-   <span data-ttu-id="fb46b-287">إذا</span><span class="sxs-lookup"><span data-stu-id="fb46b-287">If</span></span>
-   <span data-ttu-id="fb46b-288">أقل</span><span class="sxs-lookup"><span data-stu-id="fb46b-288">Less</span></span>
-   <span data-ttu-id="fb46b-289">أكبر</span><span class="sxs-lookup"><span data-stu-id="fb46b-289">Greater</span></span>
-   <span data-ttu-id="fb46b-290">يعني</span><span class="sxs-lookup"><span data-stu-id="fb46b-290">Implies</span></span>
-   <span data-ttu-id="fb46b-291">السجل</span><span class="sxs-lookup"><span data-stu-id="fb46b-291">Log</span></span>
-   <span data-ttu-id="fb46b-292">الحد الأقصى</span><span class="sxs-lookup"><span data-stu-id="fb46b-292">Max</span></span>
-   <span data-ttu-id="fb46b-293">دقيقة</span><span class="sxs-lookup"><span data-stu-id="fb46b-293">Min</span></span>
-   <span data-ttu-id="fb46b-294">ناقص</span><span class="sxs-lookup"><span data-stu-id="fb46b-294">Minus</span></span>
-   <span data-ttu-id="fb46b-295">زائد</span><span class="sxs-lookup"><span data-stu-id="fb46b-295">Plus</span></span>
-   <span data-ttu-id="fb46b-296">القدرة</span><span class="sxs-lookup"><span data-stu-id="fb46b-296">Power</span></span>
-   <span data-ttu-id="fb46b-297">الأوقات</span><span class="sxs-lookup"><span data-stu-id="fb46b-297">Times</span></span>
-   <span data-ttu-id="fb46b-298">الجزء</span><span class="sxs-lookup"><span data-stu-id="fb46b-298">Slot</span></span>
-   <span data-ttu-id="fb46b-299">الطراز</span><span class="sxs-lookup"><span data-stu-id="fb46b-299">Model</span></span>
-   <span data-ttu-id="fb46b-300">القرار</span><span class="sxs-lookup"><span data-stu-id="fb46b-300">Decision</span></span>
-   <span data-ttu-id="fb46b-301">الهدف</span><span class="sxs-lookup"><span data-stu-id="fb46b-301">Goal</span></span>


## <a name="additional-resources"></a><span data-ttu-id="fb46b-302">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="fb46b-302">Additional resources</span></span>

[<span data-ttu-id="fb46b-303">قم بإنشاء قيد تعبير</span><span class="sxs-lookup"><span data-stu-id="fb46b-303">Create an expression constraint</span></span>](tasks/add-expression-constraint-product-configuration-model.md)

[<span data-ttu-id="fb46b-304">إضافة عملية حسابية إلى نموذج تكوين منتج</span><span class="sxs-lookup"><span data-stu-id="fb46b-304">Add a calculation to a product configuration model</span></span>](tasks/add-calculation-product-configuration-model.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]