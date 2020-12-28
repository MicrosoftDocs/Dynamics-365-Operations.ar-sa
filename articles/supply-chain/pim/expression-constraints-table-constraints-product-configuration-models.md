---
title: قيود التعبير وقيود الجدول في نماذج تكوين المنتج
description: يصف هذا الموضوع استخدام قيود التعبير وقيود الجدول. تتحكم القيود في قيم السمات التي يمكن تحديدها عند تكوين المنتجات لأمر المبيعات أو عرض أسعار المبيعات أو أمر الشراء أو أمر الإنتاج. يمكنك استخدام قيود التعبير أو قيود الجدول، اعتمادًا على الطريقة التي تفضل بها إنشاء القيود.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCGlobalTableConstraintEdit, PCProductConfigurationModelDetails, PCTableConstraintAttachAttributeTree, PCTableConstraintDefinition
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: be9d9ae48d21db077928ba7bd5615fea47ea5181
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421566"
---
# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a><span data-ttu-id="0022a-105">قيود التعبير وقيود الجدول في نماذج تكوين المنتج</span><span class="sxs-lookup"><span data-stu-id="0022a-105">Expression constraints and table constraints in product configuration models</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0022a-106">يصف هذا الموضوع استخدام قيود التعبير وقيود الجدول.</span><span class="sxs-lookup"><span data-stu-id="0022a-106">This topic describes the use of expression constraints and table constraints.</span></span> <span data-ttu-id="0022a-107">تتحكم القيود في قيم السمات التي يمكن تحديدها عند تكوين المنتجات لأمر المبيعات أو عرض أسعار المبيعات أو أمر الشراء أو أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="0022a-107">Constraints control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="0022a-108">يمكنك استخدام قيود التعبير أو قيود الجدول، اعتمادًا على الطريقة التي تفضل بها إنشاء القيود.</span><span class="sxs-lookup"><span data-stu-id="0022a-108">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> 

<span data-ttu-id="0022a-109">يتم استخدام القيود للتحكم في قيم السمات التي يمكن تحديدها عند تكوين المنتجات لأمر المبيعات أو عرض أسعار المبيعات أو أمر الشراء أو أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="0022a-109">Constraints are used to control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="0022a-110">يمكنك استخدام قيود التعبير أو قيود الجدول، اعتمادًا على الطريقة التي تفضل بها إنشاء القيود.</span><span class="sxs-lookup"><span data-stu-id="0022a-110">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span>

## <a name="what-are-expression-constraints"></a><span data-ttu-id="0022a-111">ما هي قيود التعبير؟</span><span class="sxs-lookup"><span data-stu-id="0022a-111">What are expression constraints?</span></span>
<span data-ttu-id="0022a-112">تتسم قيود التعبير بتعبير يستخدم الدالات والمعامِلات الحسابية المنطقية.</span><span class="sxs-lookup"><span data-stu-id="0022a-112">Expression constraints are characterized by an expression that uses arithmetic and Boolean operators and functions.</span></span> <span data-ttu-id="0022a-113">تتم كتابة قيد تعبير لمكون محدد في نموذج تكوين منتج.</span><span class="sxs-lookup"><span data-stu-id="0022a-113">An expression constraint is written for a specific component in a product configuration model.</span></span> <span data-ttu-id="0022a-114">لا يمكن إعادة استخدامها بواسطة أو بالمشاركة مع مكون آخر.</span><span class="sxs-lookup"><span data-stu-id="0022a-114">It can't be reused by or shared with another component.</span></span> <span data-ttu-id="0022a-115">ومع ذلك، يمكن لقيود التعبير لمكون الإشارة إلى سمات المكونات الفرعية للمكون.</span><span class="sxs-lookup"><span data-stu-id="0022a-115">However, the expression constraints for a component can reference attributes of the component's subcomponents.</span></span>

## <a name="what-are-table-constraints"></a><span data-ttu-id="0022a-116">ما هي قيود الجدول؟</span><span class="sxs-lookup"><span data-stu-id="0022a-116">What are table constraints?</span></span>
<span data-ttu-id="0022a-117">تسرد قيود الجدول مجموعات القيم المسموح بها للسمات عندما تقوم بتكوين منتج.</span><span class="sxs-lookup"><span data-stu-id="0022a-117">Table constraints list the combinations of values that are allowed for attributes when you configure a product.</span></span> <span data-ttu-id="0022a-118">يمكن استخدام تعريفات قيود الجدول بشكل عام.</span><span class="sxs-lookup"><span data-stu-id="0022a-118">Table constraint definitions can be used generically.</span></span> <span data-ttu-id="0022a-119">عند إنشاء قيد جدول لمكون في نموذج تكوين منتج، حدد تعريف قيد جدول.</span><span class="sxs-lookup"><span data-stu-id="0022a-119">When you create a table constraint for a component in a product configuration model, you select a table constraint definition.</span></span> <span data-ttu-id="0022a-120">لإنشاء المجموعات المسموح بها، تقوم بإضافة سمات الأنواع المحددة للمكونات.</span><span class="sxs-lookup"><span data-stu-id="0022a-120">To create the combinations that are allowed, you add attributes of specific types to the components.</span></span> <span data-ttu-id="0022a-121">يحتوي كل نوع سمة على قيمة محددة.</span><span class="sxs-lookup"><span data-stu-id="0022a-121">Each attribute type has a specific value.</span></span>

### <a name="example-of-a-table-constraint"></a><span data-ttu-id="0022a-122">مثال على قيد جدول</span><span class="sxs-lookup"><span data-stu-id="0022a-122">Example of a table constraint</span></span>

<span data-ttu-id="0022a-123">يوضح هذا المثال كيفية تحديد تكوين مكبر صوت لألوان الكابينة محددة والأجزاء الأمامية.</span><span class="sxs-lookup"><span data-stu-id="0022a-123">This example shows how you can limit the configuration of a speaker to specific cabinet finishes and fronts.</span></span> <span data-ttu-id="0022a-124">يعرض الجدول الأول ألوان الكابينة والأجزاء الأمامية المتوفرة بشكل عام للتكوين.</span><span class="sxs-lookup"><span data-stu-id="0022a-124">The first table shows the cabinet finishes and fronts that are generally available for configuration.</span></span> <span data-ttu-id="0022a-125">ويتم تحديد القيم لنوعي السمات **لون الكابينة** و **الشبكة الأمامية**.</span><span class="sxs-lookup"><span data-stu-id="0022a-125">The values are defined for the **Cabinet finish** and **Front grill** attribute types.</span></span>

| <span data-ttu-id="0022a-126">نوع السمة</span><span class="sxs-lookup"><span data-stu-id="0022a-126">Attribute type</span></span> | <span data-ttu-id="0022a-127">القيم</span><span class="sxs-lookup"><span data-stu-id="0022a-127">Values</span></span>                      |
|----------------|-----------------------------|
| <span data-ttu-id="0022a-128">لون الكابينة</span><span class="sxs-lookup"><span data-stu-id="0022a-128">Cabinet finish</span></span> | <span data-ttu-id="0022a-129">أسود، وبلوطي، وروزوود، وأبيض</span><span class="sxs-lookup"><span data-stu-id="0022a-129">Black, Oak, Rosewood, White</span></span> |
| <span data-ttu-id="0022a-130">الشبكة الأمامية</span><span class="sxs-lookup"><span data-stu-id="0022a-130">Front grill</span></span>    | <span data-ttu-id="0022a-131">أسود، ومعدني، وأبيض</span><span class="sxs-lookup"><span data-stu-id="0022a-131">Black, Metal, White</span></span>         |

<span data-ttu-id="0022a-132">يُظهر الجدول التالي هذا المجموعات المحددة من قِبل قيد الجدول **اللون واللمسة النهائية**.</span><span class="sxs-lookup"><span data-stu-id="0022a-132">The next table shows the combinations that are defined by the **Color and finish** table constraint.</span></span> <span data-ttu-id="0022a-133">باستخدام هذا القيد في الجدول، يمكنك تكوين مكبر صوت بلون بلوطي وشبكة سوداء، ولون روزوود وشبكة بيضاء، وهكذا.</span><span class="sxs-lookup"><span data-stu-id="0022a-133">By using this table constraint, you can configure a speaker that has an oak finish and a black grill, a Rosewood finish and a white grill, and so on.</span></span>

| <span data-ttu-id="0022a-134">إنهاء</span><span class="sxs-lookup"><span data-stu-id="0022a-134">Finish</span></span>         | <span data-ttu-id="0022a-135">الشبكة</span><span class="sxs-lookup"><span data-stu-id="0022a-135">Grill</span></span>                       |
|----------------|-----------------------------|
| <span data-ttu-id="0022a-136">بلوطي</span><span class="sxs-lookup"><span data-stu-id="0022a-136">Oak</span></span>            | <span data-ttu-id="0022a-137">أسود</span><span class="sxs-lookup"><span data-stu-id="0022a-137">Black</span></span>                       |
| <span data-ttu-id="0022a-138">روزوود</span><span class="sxs-lookup"><span data-stu-id="0022a-138">Rosewood</span></span>       | <span data-ttu-id="0022a-139">أبيض</span><span class="sxs-lookup"><span data-stu-id="0022a-139">White</span></span>                       |
| <span data-ttu-id="0022a-140">أبيض</span><span class="sxs-lookup"><span data-stu-id="0022a-140">White</span></span>          | <span data-ttu-id="0022a-141">أسود</span><span class="sxs-lookup"><span data-stu-id="0022a-141">Black</span></span>                       |
| <span data-ttu-id="0022a-142">أبيض</span><span class="sxs-lookup"><span data-stu-id="0022a-142">White</span></span>          | <span data-ttu-id="0022a-143">أبيض</span><span class="sxs-lookup"><span data-stu-id="0022a-143">White</span></span>                       |
| <span data-ttu-id="0022a-144">أسود</span><span class="sxs-lookup"><span data-stu-id="0022a-144">Black</span></span>          | <span data-ttu-id="0022a-145">أسود</span><span class="sxs-lookup"><span data-stu-id="0022a-145">Black</span></span>                       |
| <span data-ttu-id="0022a-146">أسود</span><span class="sxs-lookup"><span data-stu-id="0022a-146">Black</span></span>          | <span data-ttu-id="0022a-147">معدني</span><span class="sxs-lookup"><span data-stu-id="0022a-147">Metal</span></span>                       | 

<span data-ttu-id="0022a-148">يمكنك إنشاء قيود جدول إما محددة بواسطة المستخدم أو محددة بواسطة النظام.</span><span class="sxs-lookup"><span data-stu-id="0022a-148">You can create system-defined and user-defined table constraints.</span></span> <span data-ttu-id="0022a-149">لمزيد من المعلومات، راجع [قيود الجدول المحددة من قِبل النظام والمحددة من قِبل المستخدم](system-defined-user-defined-table-constraints.md).</span><span class="sxs-lookup"><span data-stu-id="0022a-149">For more information, see [System-defined and user-defined table constraints](system-defined-user-defined-table-constraints.md).</span></span>

## <a name="what-syntax-should-be-used-to-write-constraints"></a><span data-ttu-id="0022a-150">‏‫ما بنية الجملة التي يجب استخدامها لكتابة القيود؟</span><span class="sxs-lookup"><span data-stu-id="0022a-150">What syntax should be used to write constraints?</span></span>
<span data-ttu-id="0022a-151">يجب عليك استخدام بنية جملة لغة تصميم التحسين (OML) عند كتابة القيود.</span><span class="sxs-lookup"><span data-stu-id="0022a-151">You must use Optimization Modeling Language (OML) syntax when you write constraints.</span></span> <span data-ttu-id="0022a-152">يستخدم النظام أداة حل القيود Microsoft Solver Foundation لحل القيود.</span><span class="sxs-lookup"><span data-stu-id="0022a-152">The system uses Microsoft Solver Foundation constraint solver to solve the constraints.</span></span>

## <a name="should-i-use-table-constraints-or-expression-constraints"></a><span data-ttu-id="0022a-153">هل يجب استخدام قيود الجدول أو قيود التعبير؟</span><span class="sxs-lookup"><span data-stu-id="0022a-153">Should I use table constraints or expression constraints?</span></span>
<span data-ttu-id="0022a-154">يمكنك استخدام قيود التعبير أو قيود الجدول، اعتمادًا على الطريقة التي تفضل بها إنشاء القيود.</span><span class="sxs-lookup"><span data-stu-id="0022a-154">You can use either expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> <span data-ttu-id="0022a-155">يمكنك إنشاء قيد جدول كمصفوفة، بينما يكون قيد التعبير عبارة فردية.</span><span class="sxs-lookup"><span data-stu-id="0022a-155">You build a table constraint as a matrix, whereas an expression constraint is an individual statement.</span></span> <span data-ttu-id="0022a-156">عندما تقوم بتكوين منتج، فلا يهم نوع القيد المستخدَم.</span><span class="sxs-lookup"><span data-stu-id="0022a-156">When you configure a product, it doesn't matter what kind of constraint is used.</span></span> <span data-ttu-id="0022a-157">يعرض المثال التالي مدى اختلاف الطريقتين.</span><span class="sxs-lookup"><span data-stu-id="0022a-157">The following example shows how the two methods differ.</span></span>  

<span data-ttu-id="0022a-158">عند قيامك بتكوين منتج باستخدام إعدادات القيود التالية، يتم السماح بهذه المجموعات:</span><span class="sxs-lookup"><span data-stu-id="0022a-158">When you configure a product by using the following constraint setups, these combinations are allowed:</span></span>

-   <span data-ttu-id="0022a-159">منتج باللون الأسود، وبحجم 30 أو 50</span><span class="sxs-lookup"><span data-stu-id="0022a-159">A product in the color Black, and in size 30 or 50</span></span>
-   <span data-ttu-id="0022a-160">منتج باللون الأحمر، وبحجم 20</span><span class="sxs-lookup"><span data-stu-id="0022a-160">A product in the color Red and in size 20</span></span>

### <a name="table-constraint-setup"></a><span data-ttu-id="0022a-161">إعداد قيد الجدول</span><span class="sxs-lookup"><span data-stu-id="0022a-161">Table constraint setup</span></span>

| <span data-ttu-id="0022a-162">اللون</span><span class="sxs-lookup"><span data-stu-id="0022a-162">Color</span></span> | <span data-ttu-id="0022a-163">الحجم</span><span class="sxs-lookup"><span data-stu-id="0022a-163">Size</span></span> |
|-------|------|
| <span data-ttu-id="0022a-164">أسود</span><span class="sxs-lookup"><span data-stu-id="0022a-164">Black</span></span> | <span data-ttu-id="0022a-165">30</span><span class="sxs-lookup"><span data-stu-id="0022a-165">30</span></span>   |
| <span data-ttu-id="0022a-166">أسود</span><span class="sxs-lookup"><span data-stu-id="0022a-166">Black</span></span> | <span data-ttu-id="0022a-167">50</span><span class="sxs-lookup"><span data-stu-id="0022a-167">50</span></span>   |
| <span data-ttu-id="0022a-168">أحمر</span><span class="sxs-lookup"><span data-stu-id="0022a-168">Red</span></span>   | <span data-ttu-id="0022a-169">20</span><span class="sxs-lookup"><span data-stu-id="0022a-169">20</span></span>   |

### <a name="expression-constraint-setup"></a><span data-ttu-id="0022a-170">إعداد قيد التعبير</span><span class="sxs-lookup"><span data-stu-id="0022a-170">Expression constraint setup</span></span>

<span data-ttu-id="0022a-171">(لون == "أسود" و (حجم == "30" | حجم == "50")) | (لون == "أحمر" وحجم = "20")</span><span class="sxs-lookup"><span data-stu-id="0022a-171">(Color == "Black" & (size == "30" | size == "50")) | (color == "Red" & size = "20")</span></span>

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a><span data-ttu-id="0022a-172">هل يجب استخدام المعامِلات أو تدوين الحرف المزيد عند كتابة قيود التعبير؟</span><span class="sxs-lookup"><span data-stu-id="0022a-172">Should I use operators or infix notation when I write expression constraints?</span></span>
<span data-ttu-id="0022a-173">يمكنك كتابة قيد تعبير إما باستخدام تدوين الحروف المزيدة أو معامِلات البادئات المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="0022a-173">You can write an expression constraint by using either the available prefix operators or infix notation.</span></span> <span data-ttu-id="0022a-174">لا يمكنك استخدام تدوين الحروف المزيدة لمعامِلات ‏‫القيمة **المطلقة**، و **الحد الأدنى**، و **الحد الأقصى**.</span><span class="sxs-lookup"><span data-stu-id="0022a-174">For the **Min**, **Max**, and **Abs** operators, you can't use infix notation.</span></span> <span data-ttu-id="0022a-175">ويتم تضمين هذه المعامِلات كمعامِلات قياسية في معظم لغات البرمجة.</span><span class="sxs-lookup"><span data-stu-id="0022a-175">These operators are included as standard operators in most programming languages.</span></span>

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a><span data-ttu-id="0022a-176">ما هي المعامِلات وتدوينات الحروف المزيدة التي يمكن استخدامها عند كتابة قيود التعبير؟</span><span class="sxs-lookup"><span data-stu-id="0022a-176">What operators and infix notation can I use when I write expression constraints?</span></span>
<span data-ttu-id="0022a-177">تسرد الجداول التالية المعامِلات وتدوينات الحروف المزيدة التي يمكنك استخدامها عند كتابة قيد تعبير لمكون في نموذج تكوين منتج.</span><span class="sxs-lookup"><span data-stu-id="0022a-177">The following tables list the operators and infix notation that you can use when you write an expression constraint for a component in a product configuration model.</span></span> <span data-ttu-id="0022a-178">في الأمثلة الواردة في هذا الجدول الأول، يمكنك الاطلاع على كيفية كتابة تعبير باستخدام المعامِلات أو تدوينات الحروف المزيدة.</span><span class="sxs-lookup"><span data-stu-id="0022a-178">The examples in the first table show how to write an expression by using either infix notation or operators.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0022a-179">عامل تشغيل</span><span class="sxs-lookup"><span data-stu-id="0022a-179">Operator</span></span></th>
<th><span data-ttu-id="0022a-180">الوصف</span><span class="sxs-lookup"><span data-stu-id="0022a-180">Description</span></span></th>
<th><span data-ttu-id="0022a-181">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="0022a-181">Syntax</span></span></th>
<th><span data-ttu-id="0022a-182">أمثلة</span><span class="sxs-lookup"><span data-stu-id="0022a-182">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0022a-183">يعني</span><span class="sxs-lookup"><span data-stu-id="0022a-183">Implies</span></span></td>
<td><span data-ttu-id="0022a-184">يكون هذا الأمر صحيحًا إذا كان الشرط الأول خاطئًا، والشرط الثاني صحيح، أو كليهما.</span><span class="sxs-lookup"><span data-stu-id="0022a-184">This is true if the first condition is false, the second condition is true, or both.</span></span></td>
<td><span data-ttu-id="0022a-185">يعني [a أو b]، الحرف المزيد: a -: b</span><span class="sxs-lookup"><span data-stu-id="0022a-185">Implies[a, b], infix: a -: b</span></span></td>
<td><ul>
<li><span data-ttu-id="0022a-186"><strong>عامل التشغيل:</strong> يتضمن[x‏ != 0، y &gt;=‏ 0]</span><span class="sxs-lookup"><span data-stu-id="0022a-186"><strong>Operator:</strong> Implies[x != 0, y &gt;= 0]</span></span></li>
<li><span data-ttu-id="0022a-187"><strong>تدوين الحرف المزيد:</strong> x‏ != 0 -‏: y &gt;=‏ 0</span><span class="sxs-lookup"><span data-stu-id="0022a-187"><strong>Infix notation:</strong> x != 0 -: y &gt;= 0</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0022a-188">و</span><span class="sxs-lookup"><span data-stu-id="0022a-188">And</span></span></td>
<td><span data-ttu-id="0022a-189">يكون هذا الأمر صحيحًا فقط إذا تحققت جميع الشروط.</span><span class="sxs-lookup"><span data-stu-id="0022a-189">This is true only if all conditions are true.</span></span> <span data-ttu-id="0022a-190">إذا كان عدد الشروط هو 0 (صفر)، ينتج قيمة <strong>صحيحة</strong>.</span><span class="sxs-lookup"><span data-stu-id="0022a-190">If the number of conditions is 0 (zero), it produces <strong>True</strong>.</span></span></td>
<td><span data-ttu-id="0022a-191">And[args], الحرف المزيد: a &amp; b &amp; ... &amp; z</span><span class="sxs-lookup"><span data-stu-id="0022a-191">And[args], infix: a &amp; b &amp; ... &amp; z</span></span></td>
<td><ul>
<li><span data-ttu-id="0022a-192"><strong>عامل التشغيل:</strong> And[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="0022a-192"><strong>Operator:</strong> And[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="0022a-193"><strong>تدوين الحرف المزيد:</strong> x‏ == 2 &amp; y &lt;=‏ 2</span><span class="sxs-lookup"><span data-stu-id="0022a-193"><strong>Infix notation:</strong> x == 2 &amp; y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0022a-194">أو</span><span class="sxs-lookup"><span data-stu-id="0022a-194">Or</span></span></td>
<td><span data-ttu-id="0022a-195">يكون هذا الأمر صحيحًا إذا كان أي شرط صحيح.</span><span class="sxs-lookup"><span data-stu-id="0022a-195">This is true if any condition is true.</span></span> <span data-ttu-id="0022a-196">إذا كان عدد الشروط هو 0 (صفر)، تنتج قيمة <strong>خاطئة</strong>.</span><span class="sxs-lookup"><span data-stu-id="0022a-196">If the number of conditions is 0 (zero), it produces <strong>False</strong>.</span></span></td>
<td><span data-ttu-id="0022a-197">Or[args], الحرف المزيد: a | b | ... | z</span><span class="sxs-lookup"><span data-stu-id="0022a-197">Or[args], infix: a | b | ... | z</span></span></td>
<td><ul>
<li><span data-ttu-id="0022a-198"><strong>عامل التشغيل:</strong> Or[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="0022a-198"><strong>Operator:</strong> Or[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="0022a-199"><strong>تدوين الحرف المزيد:</strong> x =‏=‏ 2 | y &lt;=‏ 2</span><span class="sxs-lookup"><span data-stu-id="0022a-199"><strong>Infix notation:</strong> x == 2 | y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0022a-200">زائد</span><span class="sxs-lookup"><span data-stu-id="0022a-200">Plus</span></span></td>
<td><span data-ttu-id="0022a-201">وهذا يلخص الشروط.</span><span class="sxs-lookup"><span data-stu-id="0022a-201">This sums its conditions.</span></span> <span data-ttu-id="0022a-202">إذا كان عدد الشروط هو 0 (صفر)، تنتج قيمة <strong>0</strong>.</span><span class="sxs-lookup"><span data-stu-id="0022a-202">If the number of conditions is 0 (zero), it produces <strong>0</strong>.</span></span></td>
<td><span data-ttu-id="0022a-203">Plus[args], الحرف المزيد: a + b + ... + z</span><span class="sxs-lookup"><span data-stu-id="0022a-203">Plus[args], infix: a + b + ... + z</span></span></td>
<td><ul>
<li><span data-ttu-id="0022a-204"><strong>عامل التشغيل:</strong> زائد[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="0022a-204"><strong>Operator:</strong> Plus[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="0022a-205"><strong>تدوين الحرف المزيد:</strong> x + y + 2 =‏=‏ z</span><span class="sxs-lookup"><span data-stu-id="0022a-205"><strong>Infix notation:</strong> x + y + 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0022a-206">ناقص</span><span class="sxs-lookup"><span data-stu-id="0022a-206">Minus</span></span></td>
<td><span data-ttu-id="0022a-207">هذا يناقض الوسيطة.</span><span class="sxs-lookup"><span data-stu-id="0022a-207">This negates its argument.</span></span> <span data-ttu-id="0022a-208">يجب أن يكون به شرط واحد فقط.</span><span class="sxs-lookup"><span data-stu-id="0022a-208">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="0022a-209">Minus[expr], الحرف المزيد: -expr</span><span class="sxs-lookup"><span data-stu-id="0022a-209">Minus[expr], infix: -expr</span></span></td>
<td><ul>
<li><span data-ttu-id="0022a-210"><strong>عامل التشغيل:</strong> ناقص[x] == y</span><span class="sxs-lookup"><span data-stu-id="0022a-210"><strong>Operator:</strong> Minus[x] == y</span></span></li>
<li><span data-ttu-id="0022a-211"><strong>تدوين الحرف المزيد:</strong> -x =‏=‏ y</span><span class="sxs-lookup"><span data-stu-id="0022a-211"><strong>Infix notation:</strong> -x == y</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0022a-212">Abs</span><span class="sxs-lookup"><span data-stu-id="0022a-212">Abs</span></span></td>
<td><span data-ttu-id="0022a-213">وهذا يأخذ القيمة المطلقة من شرطها.</span><span class="sxs-lookup"><span data-stu-id="0022a-213">This takes the absolute value of its condition.</span></span> <span data-ttu-id="0022a-214">يجب أن يكون به شرط واحد فقط.</span><span class="sxs-lookup"><span data-stu-id="0022a-214">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="0022a-215">Abs[expr]</span><span class="sxs-lookup"><span data-stu-id="0022a-215">Abs[expr]</span></span></td>
<td><span data-ttu-id="0022a-216"><strong>عامل التشغيل:</strong> Abs[x]</span><span class="sxs-lookup"><span data-stu-id="0022a-216"><strong>Operator:</strong> Abs[x]</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0022a-217">الأوقات</span><span class="sxs-lookup"><span data-stu-id="0022a-217">Times</span></span></td>
<td><span data-ttu-id="0022a-218">يأخذ هذا المنتج من شروطه.</span><span class="sxs-lookup"><span data-stu-id="0022a-218">This takes the product of its conditions.</span></span> <span data-ttu-id="0022a-219">إذا كان عدد الشروط هو 0 (صفر)، تنتج قيمة <strong>1</strong>.</span><span class="sxs-lookup"><span data-stu-id="0022a-219">If the number of conditions is 0 (zero), it produces <strong>1</strong>.</span></span></td>
<td><span data-ttu-id="0022a-220">Times[args], الحرف الزائد: a \* b \* ... \* z</span><span class="sxs-lookup"><span data-stu-id="0022a-220">Times[args], infix: a \* b \* ... \* z</span></span></td>
<td><ul>
<li><span data-ttu-id="0022a-221"><strong>عامل التشغيل:</strong> Times[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="0022a-221"><strong>Operator:</strong> Times[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="0022a-222"><strong>تدوين الحرف المزيد:</strong> x \* y \* 2 =‏=‏ z</span><span class="sxs-lookup"><span data-stu-id="0022a-222"><strong>Infix notation:</strong> x \* y \* 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0022a-223">القدرة</span><span class="sxs-lookup"><span data-stu-id="0022a-223">Power</span></span></td>
<td><span data-ttu-id="0022a-224">يأخذ هذا قيمة أُسية.</span><span class="sxs-lookup"><span data-stu-id="0022a-224">This takes an exponential.</span></span> <span data-ttu-id="0022a-225">تنطبق هذه القيمة الأُسية من اليمين لليسار.</span><span class="sxs-lookup"><span data-stu-id="0022a-225">It applies exponentiation from right to left.</span></span> <span data-ttu-id="0022a-226">(وبمعنى آخر، إنها مجمَّعة إلى اليمين). وبالتالي، فإن <strong>Power[a, b, c]</strong> يعادل <strong>Power[a, Power[b, c]]</strong>.</span><span class="sxs-lookup"><span data-stu-id="0022a-226">(In other words, it&#39;s right-associative.) Therefore, <strong>Power[a, b, c]</strong> is equivalent to <strong>Power[a, Power[b, c]]</strong>.</span></span> <span data-ttu-id="0022a-227"><strong>Power</strong> يمكن استخدامه فقط إذا كان الأس بقيمة موجبة.</span><span class="sxs-lookup"><span data-stu-id="0022a-227"><strong>Power</strong> can be used only if the exponent is a positive constant.</span></span></td>
<td><span data-ttu-id="0022a-228">Power[args], الحرف المزيد: a ^ b ^ ... ^ z</span><span class="sxs-lookup"><span data-stu-id="0022a-228">Power[args], infix: a ^ b ^ ... ^ z</span></span></td>
<td><ul>
<li><span data-ttu-id="0022a-229"><strong>عامل التشغيل:</strong> Power[x, 2] == y</span><span class="sxs-lookup"><span data-stu-id="0022a-229"><strong>Operator:</strong> Power[x, 2] == y</span></span></li>
<li><span data-ttu-id="0022a-230"><strong>تدوين الحرف المزيد:</strong> x ^ 2 =‏=‏ y</span><span class="sxs-lookup"><span data-stu-id="0022a-230"><strong>Infix notation:</strong> x ^ 2 == y</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0022a-231">الحد الأقصى</span><span class="sxs-lookup"><span data-stu-id="0022a-231">Max</span></span></td>
<td><span data-ttu-id="0022a-232">ينتج عن هذا الأمر الشرط الأكبر.</span><span class="sxs-lookup"><span data-stu-id="0022a-232">This produces the largest condition.</span></span> <span data-ttu-id="0022a-233">إذا كان عدد الشروط هو 0 (صفر)، تنتج قيمة <strong>لانهائية</strong>.</span><span class="sxs-lookup"><span data-stu-id="0022a-233">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="0022a-234">Max[args]</span><span class="sxs-lookup"><span data-stu-id="0022a-234">Max[args]</span></span></td>
<td><span data-ttu-id="0022a-235"><strong>عامل التشغيل:</strong> الحد الأقصى[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="0022a-235"><strong>Operator:</strong> Max[x, y, 2] == z</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0022a-236">دقيقة</span><span class="sxs-lookup"><span data-stu-id="0022a-236">Min</span></span></td>
<td><span data-ttu-id="0022a-237">ينتج عن هذا الأمر الشرط الأصغر.</span><span class="sxs-lookup"><span data-stu-id="0022a-237">This produces the smallest condition.</span></span> <span data-ttu-id="0022a-238">إذا كان عدد الشروط هو 0 (صفر)، تنتج قيمة <strong>لانهائية</strong>.</span><span class="sxs-lookup"><span data-stu-id="0022a-238">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="0022a-239">Min[args]</span><span class="sxs-lookup"><span data-stu-id="0022a-239">Min[args]</span></span></td>
<td><span data-ttu-id="0022a-240"><strong>عامل التشغيل:</strong> الحد الأدنى[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="0022a-240"><strong>Operator:</strong> Min[x, y, 2] == z</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0022a-241">ليس</span><span class="sxs-lookup"><span data-stu-id="0022a-241">Not</span></span></td>
<td><span data-ttu-id="0022a-242">ينتج عن هذا الأمر العكس المنطقي للشرط.</span><span class="sxs-lookup"><span data-stu-id="0022a-242">This produces the logical inverse of its condition.</span></span> <span data-ttu-id="0022a-243">يجب أن يكون به شرط واحد فقط.</span><span class="sxs-lookup"><span data-stu-id="0022a-243">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="0022a-244">Not[expr], الحرف المزيد: !expr</span><span class="sxs-lookup"><span data-stu-id="0022a-244">Not[expr], infix: !expr</span></span></td>
<td><ul>
<li><span data-ttu-id="0022a-245"><strong>عامل التشغيل:</strong> Not[x] &amp; Not[y == 3]</span><span class="sxs-lookup"><span data-stu-id="0022a-245"><strong>Operator:</strong> Not[x] &amp; Not[y == 3]</span></span></li>
<li><span data-ttu-id="0022a-246"><strong>تدوين الحرف المزيد:</strong> !‏x!‏(y =‏= 3)</span><span class="sxs-lookup"><span data-stu-id="0022a-246"><strong>Infix notation:</strong> !x!(y == 3)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0022a-247">توضح الأمثلة في الجدول التالي كيفية كتابة تدوين الحرف المزيد.</span><span class="sxs-lookup"><span data-stu-id="0022a-247">The examples in the next table show how to write infix notation.</span></span>


|  <span data-ttu-id="0022a-248">تدوين الحرف المزيد</span><span class="sxs-lookup"><span data-stu-id="0022a-248">Infix notation</span></span>   |                                          <span data-ttu-id="0022a-249">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="0022a-249">Description</span></span>                                          |
|-------------------|-----------------------------------------------------------------------------------------------|
|     <span data-ttu-id="0022a-250">x + y + z</span><span class="sxs-lookup"><span data-stu-id="0022a-250">x + y + z</span></span>     |                                           <span data-ttu-id="0022a-251">الجمع</span><span class="sxs-lookup"><span data-stu-id="0022a-251">Addition</span></span>                                            |
|    <span data-ttu-id="0022a-252">x \* y \* z</span><span class="sxs-lookup"><span data-stu-id="0022a-252">x \* y \* z</span></span>    |                                        <span data-ttu-id="0022a-253">الضرب</span><span class="sxs-lookup"><span data-stu-id="0022a-253">Multiplication</span></span>                                         |
|       <span data-ttu-id="0022a-254">x - y</span><span class="sxs-lookup"><span data-stu-id="0022a-254">x - y</span></span>       | <span data-ttu-id="0022a-255">يتم تحويل الطرح الثنائي مثل الإضافة الثنائية بقيمة ثانية سالبة.</span><span class="sxs-lookup"><span data-stu-id="0022a-255">Binary subtraction is translated the same as binary addition where there is a negated second.</span></span> |
|     <span data-ttu-id="0022a-256">x ^ y ^ z</span><span class="sxs-lookup"><span data-stu-id="0022a-256">x ^ y ^ z</span></span>     |                          <span data-ttu-id="0022a-257">العلامة الأسية بالتجميع الصحيح</span><span class="sxs-lookup"><span data-stu-id="0022a-257">Exponentiation that has right associativity</span></span>                          |
|        <span data-ttu-id="0022a-258">!x</span><span class="sxs-lookup"><span data-stu-id="0022a-258">!x</span></span>         |                                          <span data-ttu-id="0022a-259">قيمة غير منطقية</span><span class="sxs-lookup"><span data-stu-id="0022a-259">Boolean not</span></span>                                          |
|      <span data-ttu-id="0022a-260">x -: y</span><span class="sxs-lookup"><span data-stu-id="0022a-260">x -: y</span></span>       |                                      <span data-ttu-id="0022a-261">تضمين منطقي</span><span class="sxs-lookup"><span data-stu-id="0022a-261">Boolean implication</span></span>                                      |
|         <span data-ttu-id="0022a-262">x</span><span class="sxs-lookup"><span data-stu-id="0022a-262">x</span></span>         |                                               <span data-ttu-id="0022a-263">y</span><span class="sxs-lookup"><span data-stu-id="0022a-263">y</span></span>                                               |
|     <span data-ttu-id="0022a-264">x & y & z</span><span class="sxs-lookup"><span data-stu-id="0022a-264">x & y & z</span></span>     |                                          <span data-ttu-id="0022a-265">قيمة and منطقية</span><span class="sxs-lookup"><span data-stu-id="0022a-265">Boolean and</span></span>                                          |
|    <span data-ttu-id="0022a-266">x =‏=‏ y =‏=‏ z</span><span class="sxs-lookup"><span data-stu-id="0022a-266">x == y == z</span></span>    |                                           <span data-ttu-id="0022a-267">التساوي</span><span class="sxs-lookup"><span data-stu-id="0022a-267">Equality</span></span>                                            |
|    <span data-ttu-id="0022a-268">x !=‏ y !=‏ z</span><span class="sxs-lookup"><span data-stu-id="0022a-268">x != y != z</span></span>    |                                           <span data-ttu-id="0022a-269">محدد</span><span class="sxs-lookup"><span data-stu-id="0022a-269">Distinct</span></span>                                            |
|  <span data-ttu-id="0022a-270">x &lt; y &lt; z</span><span class="sxs-lookup"><span data-stu-id="0022a-270">x &lt; y &lt; z</span></span>  |                                           <span data-ttu-id="0022a-271">أقل من  </span><span class="sxs-lookup"><span data-stu-id="0022a-271">Less than</span></span>                                           |
|  <span data-ttu-id="0022a-272">x &gt; y &gt; z</span><span class="sxs-lookup"><span data-stu-id="0022a-272">x &gt; y &gt; z</span></span>  |                                         <span data-ttu-id="0022a-273">أكبر من</span><span class="sxs-lookup"><span data-stu-id="0022a-273">Greater than</span></span>                                          |
| <span data-ttu-id="0022a-274">x &lt;=‏‏ y &lt;=‏‏ z</span><span class="sxs-lookup"><span data-stu-id="0022a-274">x &lt;= y &lt;= z</span></span> |                                     <span data-ttu-id="0022a-275">أقل من أو يساوي</span><span class="sxs-lookup"><span data-stu-id="0022a-275">Less than or equal to</span></span>                                     |
| <span data-ttu-id="0022a-276">x &gt;=‏ y &gt;=‏ z</span><span class="sxs-lookup"><span data-stu-id="0022a-276">x &gt;= y &gt;= z</span></span> |                                   <span data-ttu-id="0022a-277">أكبر من أو يساوي</span><span class="sxs-lookup"><span data-stu-id="0022a-277">Greater than or equal to</span></span>                                    |
|        <span data-ttu-id="0022a-278">(x)</span><span class="sxs-lookup"><span data-stu-id="0022a-278">(x)</span></span>        |                           <span data-ttu-id="0022a-279">تتجاوز الأقواس الأسبقية الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="0022a-279">Parentheses override default precedence.</span></span>                            |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a><span data-ttu-id="0022a-280">لماذا لم يتم التحقق من صحة قيود التعبير لدي بشكل صحيح؟</span><span class="sxs-lookup"><span data-stu-id="0022a-280">Why aren't my expression constraints validated correctly?</span></span>
<span data-ttu-id="0022a-281">لا يمكنك استخدام الكلمات الرئيسية المحجوزة كأسماء أدوات الحلول للسمات أو المكونات أو المكونات الفرعية في نموذج تكوين منتج.</span><span class="sxs-lookup"><span data-stu-id="0022a-281">You can't use reserved keywords as solver names for attributes, components, or subcomponents in a product configuration model.</span></span><span data-ttu-id="0022a-282"> فيما يلي قائمة بالكلمات الأساسية المحجوزة التي لا يمكن استخدامها:</span><span class="sxs-lookup"><span data-stu-id="0022a-282"> Here is a list of the reserved keywords that you can't use:</span></span>

-   <span data-ttu-id="0022a-283">الحد الأقصى</span><span class="sxs-lookup"><span data-stu-id="0022a-283">Ceiling</span></span>
-   <span data-ttu-id="0022a-284">العنصر</span><span class="sxs-lookup"><span data-stu-id="0022a-284">Element</span></span>
-   <span data-ttu-id="0022a-285">متساوٍ</span><span class="sxs-lookup"><span data-stu-id="0022a-285">Equal</span></span>
-   <span data-ttu-id="0022a-286">الأرضية</span><span class="sxs-lookup"><span data-stu-id="0022a-286">Floor</span></span>
-   <span data-ttu-id="0022a-287">إذا</span><span class="sxs-lookup"><span data-stu-id="0022a-287">If</span></span>
-   <span data-ttu-id="0022a-288">أقل</span><span class="sxs-lookup"><span data-stu-id="0022a-288">Less</span></span>
-   <span data-ttu-id="0022a-289">أكبر</span><span class="sxs-lookup"><span data-stu-id="0022a-289">Greater</span></span>
-   <span data-ttu-id="0022a-290">يعني</span><span class="sxs-lookup"><span data-stu-id="0022a-290">Implies</span></span>
-   <span data-ttu-id="0022a-291">السجل</span><span class="sxs-lookup"><span data-stu-id="0022a-291">Log</span></span>
-   <span data-ttu-id="0022a-292">الحد الأقصى</span><span class="sxs-lookup"><span data-stu-id="0022a-292">Max</span></span>
-   <span data-ttu-id="0022a-293">دقيقة</span><span class="sxs-lookup"><span data-stu-id="0022a-293">Min</span></span>
-   <span data-ttu-id="0022a-294">ناقص</span><span class="sxs-lookup"><span data-stu-id="0022a-294">Minus</span></span>
-   <span data-ttu-id="0022a-295">زائد</span><span class="sxs-lookup"><span data-stu-id="0022a-295">Plus</span></span>
-   <span data-ttu-id="0022a-296">القدرة</span><span class="sxs-lookup"><span data-stu-id="0022a-296">Power</span></span>
-   <span data-ttu-id="0022a-297">الأوقات</span><span class="sxs-lookup"><span data-stu-id="0022a-297">Times</span></span>
-   <span data-ttu-id="0022a-298">الجزء</span><span class="sxs-lookup"><span data-stu-id="0022a-298">Slot</span></span>
-   <span data-ttu-id="0022a-299">الطراز</span><span class="sxs-lookup"><span data-stu-id="0022a-299">Model</span></span>
-   <span data-ttu-id="0022a-300">القرار</span><span class="sxs-lookup"><span data-stu-id="0022a-300">Decision</span></span>
-   <span data-ttu-id="0022a-301">الهدف</span><span class="sxs-lookup"><span data-stu-id="0022a-301">Goal</span></span>


<a name="additional-resources"></a><span data-ttu-id="0022a-302">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="0022a-302">Additional resources</span></span>
--------

[<span data-ttu-id="0022a-303">قم بإنشاء قيد تعبير</span><span class="sxs-lookup"><span data-stu-id="0022a-303">Create an expression constraint</span></span>](tasks/add-expression-constraint-product-configuration-model.md)

[<span data-ttu-id="0022a-304">إضافة عملية حسابية إلى نموذج تكوين منتج</span><span class="sxs-lookup"><span data-stu-id="0022a-304">Add a calculation to a product configuration model</span></span>](tasks/add-calculation-product-configuration-model.md)



