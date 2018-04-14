---
title: "التسلسلات الرقمية"
description: "وتُستخدم التسلسلات الرقمية لإنشاء معرفات فريدة قابلة للقراءة لسجلات البيانات الرئيسية وسجلات الحركة التي تتطلب وجود هذه المعرفات."
author: MargoC
manager: AnnBe
ms.date: 08/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: NumberSequenceTableListPage, NumberSequenceConfiguration
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 15461
ms.assetid: 6e19bd1d-192b-4da2-8573-84f6e1ce98ef
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 58069d79f92ce015fe4b11b50fb3348722bca4f8
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---

# <a name="number-sequences"></a><span data-ttu-id="060cd-103">التسلسلات الرقمية</span><span class="sxs-lookup"><span data-stu-id="060cd-103">Number sequences</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="060cd-104">وتُستخدم التسلسلات الرقمية لإنشاء معرفات فريدة قابلة للقراءة لسجلات البيانات الرئيسية وسجلات الحركة التي تتطلب وجود هذه المعرفات.</span><span class="sxs-lookup"><span data-stu-id="060cd-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require identifiers.</span></span> <span data-ttu-id="060cd-105">ويشار إلى سجل البيانات الرئيسية أو سجل الحركة الذي يتطلب معرفًا *بمرجع*.</span><span class="sxs-lookup"><span data-stu-id="060cd-105">A master data record or transaction record that requires an identifier is referred to as a *reference*.</span></span>

<span data-ttu-id="060cd-106">قبل إنشاء سجلات جديدة لأحد المراجع، يجب أن تقوم بإعداد تسلسل رقمي وإقرانه بالمرجع.</span><span class="sxs-lookup"><span data-stu-id="060cd-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="060cd-107">ونحن ننصح باستخدام الصفحات الموجودة في **إدارة المؤسسة‬** لإعداد التسلسلات الرقمية.</span><span class="sxs-lookup"><span data-stu-id="060cd-107">We recommend that you use the pages in **Organization administration** to set up number sequences.</span></span> <span data-ttu-id="060cd-108">وإذا كانت الإعدادات الخاصة بالوحدة النمطية مطلوبة، فيمكنك استخدام صفحة المحددات في أي وحدة نمطية لتحديد التسلسلات الرقمية للمراجع في تلك الوحدة النمطية.</span><span class="sxs-lookup"><span data-stu-id="060cd-108">If module-specific settings are required, you can use the parameters page in a module to specify number sequences for the references in that module.</span></span> <span data-ttu-id="060cd-109">على سبيل المثال، في **الحسابات المدينة** و**الحسابات الدائنة**, يمكنك إعداد مجموعات تسلسلات رقمية لتخصيص تسلسلات رقمية محددة لعملاء أو مورّدين معينين.</span><span class="sxs-lookup"><span data-stu-id="060cd-109">For example, in **Accounts receivable** and **Accounts payable**, you can set up number sequence groups to allocate specific number sequences to specific customers or vendors.</span></span> 

<span data-ttu-id="060cd-110">عند إعداد تسلسل رقمي، يجب عليك تحديد النطاق، الذي يحدد المؤسسة التي تستخدم التسلسل الرقمي.</span><span class="sxs-lookup"><span data-stu-id="060cd-110">When you set up a number sequence, you must specify a scope, which defines which organization uses the number sequence.</span></span> <span data-ttu-id="060cd-111">ويمكن أن يكون النطاق **مشتركًا** أو **شركة** أو **كيان قانوني** أو **وحدة تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="060cd-111">The scope can be **Shared**, **Company**, **Legal entity**, or **Operating unit**.</span></span> <span data-ttu-id="060cd-112">يمكن دمج نطاقي **الكيان القانوني** و**الشركة** في **فترة التقويم المالي‬** لإنشاء تسلسلات رقمية أكثر تحديدًا.</span><span class="sxs-lookup"><span data-stu-id="060cd-112">**Legal entity** and **Company** scopes can be combined with **Fiscal calendar period** to create even more specific number sequences.</span></span> 

<span data-ttu-id="060cd-113">تتألف تنسيقات التسلسلات الرقمية من مقاطع.</span><span class="sxs-lookup"><span data-stu-id="060cd-113">Number sequence formats consist of segments.</span></span> <span data-ttu-id="060cd-114">ويمكن أن تحتوي التسلسلات الرقمية التي تتضمن نطاقًا غير **مشترك** على مقاطع تتوافق مع النطاق.</span><span class="sxs-lookup"><span data-stu-id="060cd-114">Number sequences with a scope other than **Shared** can contain segments that correspond to the scope.</span></span> <span data-ttu-id="060cd-115">فعلى سبيل المثال، يمكن أن يتضمن تسلسل رقمي بنطاق **الكيان القانوني** مقطع كيان قانوني.</span><span class="sxs-lookup"><span data-stu-id="060cd-115">For example, a number sequence with a scope of **Legal entity** can contain a legal entity segment.</span></span> <span data-ttu-id="060cd-116">وعن طريق تضمين مقطع نطاق في تنسيق التسلسل الرقمي، يمكنك تحديد نطاق سجل معين بالنظر إلى رقمه.</span><span class="sxs-lookup"><span data-stu-id="060cd-116">By including a scope segment in the number sequence format, you can identify the scope of a particular record by looking at its number.</span></span> 

<span data-ttu-id="060cd-117">بالإضافة إلى المقاطع التي تتوافق مع النطاقات، يمكن أن تحتوي تنسيقات التسلسلات الرقمية على مقاطع **ثابتة** و**أبجدية رقمية**.</span><span class="sxs-lookup"><span data-stu-id="060cd-117">In addition to segments that correspond to scopes, number sequence formats can contain **Constant** and **Alphanumeric segments**.</span></span> <span data-ttu-id="060cd-118">ويتضمن المقطع **الثابت** مجموعة من الأحرف أو الأرقام أو الرموز التي لا تتغير.</span><span class="sxs-lookup"><span data-stu-id="060cd-118">A **Constant** segment contains a set of letters, numbers, or symbols that does not change.</span></span> <span data-ttu-id="060cd-119">بينما يتضمن المقطع **الأبجدي الرقمي**مجموعة من الأحرف أو الأرقام التي تزيد في كل مرة يُستخدم فيها رقم ما.</span><span class="sxs-lookup"><span data-stu-id="060cd-119">An **Alphanumeric** segment contains a set of letters or numbers that increment every time that a number is used.</span></span> <span data-ttu-id="060cd-120">استخدم علامة الأرقام (\#) للتعبير عن الأرقام المتزايدة وعلامة العطف (&) للتعبير عن الأحرف المتزايدة.</span><span class="sxs-lookup"><span data-stu-id="060cd-120">Use a number sign (\#) to represent incrementing numbers and an ampersand (&) to represent incrementing letters.</span></span> <span data-ttu-id="060cd-121">على سبيل المثال، يعمل تنسيق \#\#\#\#\#\_2017 على إنشاء التسلسل 00001\_2017،‏ 00002\_2017، وهكذا.</span><span class="sxs-lookup"><span data-stu-id="060cd-121">For example, the format \#\#\#\#\#\_2017 creates the sequence 00001\_2017, 00002\_2017, and so on.</span></span>

<a name="number-sequence-examples"></a><span data-ttu-id="060cd-122">أمثلة على التسلسلات الرقمية</span><span class="sxs-lookup"><span data-stu-id="060cd-122">Number sequence examples</span></span>
------------------------

<span data-ttu-id="060cd-123">تبين الأمثلة التالية كيفية استخدام المقاطع لإنشاء تنسيقات التسلسلات الرقمية.</span><span class="sxs-lookup"><span data-stu-id="060cd-123">The following examples show how to use segments to create number sequence formats.</span></span> <span data-ttu-id="060cd-124">وبشكلٍ خاص، توضح الأمثلة آثار استخدام مقاطع النطاقات.</span><span class="sxs-lookup"><span data-stu-id="060cd-124">In particular, the examples demonstrate the effects of using scope segments.</span></span>

### <a name="expense-report-numbers"></a><span data-ttu-id="060cd-125">أرقام تقارير المصروفات</span><span class="sxs-lookup"><span data-stu-id="060cd-125">Expense report numbers</span></span>

<span data-ttu-id="060cd-126">في المثال التالي، يتم إعداد أرقام تقارير المصروفات للكيان القانوني الذي يحمل عنوان **CS**.</span><span class="sxs-lookup"><span data-stu-id="060cd-126">In the following example, expense report numbers are set up for the legal entity that is titled **CS**.</span></span> 

- <span data-ttu-id="060cd-127">**المجال:** السفر والمصروفات</span><span class="sxs-lookup"><span data-stu-id="060cd-127">**Area:** Travel and expense</span></span> 
- <span data-ttu-id="060cd-128">**المرجع:** رقم تقرير المصروفات</span><span class="sxs-lookup"><span data-stu-id="060cd-128">**Reference:** Expense report number</span></span> 
- <span data-ttu-id="060cd-129">**النطاق:** كيان قانوني</span><span class="sxs-lookup"><span data-stu-id="060cd-129">**Scope:** Legal entity</span></span> 
- <span data-ttu-id="060cd-130">**الكيان القانوني:** CS</span><span class="sxs-lookup"><span data-stu-id="060cd-130">**Legal entity:** CS</span></span>

| <span data-ttu-id="060cd-131">المقاطع</span><span class="sxs-lookup"><span data-stu-id="060cd-131">Segments</span></span>  | <span data-ttu-id="060cd-132">نوع المقطع</span><span class="sxs-lookup"><span data-stu-id="060cd-132">Segment type</span></span> | <span data-ttu-id="060cd-133">القيمة</span><span class="sxs-lookup"><span data-stu-id="060cd-133">Value</span></span>     |
|-----------|--------------|-----------|
| <span data-ttu-id="060cd-134">المقطع 1</span><span class="sxs-lookup"><span data-stu-id="060cd-134">Segment 1</span></span> | <span data-ttu-id="060cd-135">كيان قانوني</span><span class="sxs-lookup"><span data-stu-id="060cd-135">Legal entity</span></span> | <span data-ttu-id="060cd-136">CS</span><span class="sxs-lookup"><span data-stu-id="060cd-136">CS</span></span>        |
| <span data-ttu-id="060cd-137">المقطع 2</span><span class="sxs-lookup"><span data-stu-id="060cd-137">Segment 2</span></span> | <span data-ttu-id="060cd-138">ثابت</span><span class="sxs-lookup"><span data-stu-id="060cd-138">Constant</span></span>     | <span data-ttu-id="060cd-139">-EXPENSE-</span><span class="sxs-lookup"><span data-stu-id="060cd-139">-EXPENSE-</span></span> |
| <span data-ttu-id="060cd-140">المقطع 3</span><span class="sxs-lookup"><span data-stu-id="060cd-140">Segment 3</span></span> | <span data-ttu-id="060cd-141">أبجدي رقمي</span><span class="sxs-lookup"><span data-stu-id="060cd-141">Alphanumeric</span></span> | \#\#\#\#  |

<span data-ttu-id="060cd-142">**مثال على الرقم المنسق**: ‏CS-EXPENSE-0039</span><span class="sxs-lookup"><span data-stu-id="060cd-142">**Example of formatted number**: CS-EXPENSE-0039</span></span> 

<span data-ttu-id="060cd-143">يمكنك إعداد تنسيق تسلسل رقمي مشابه للكيانات القانونية الأخرى.</span><span class="sxs-lookup"><span data-stu-id="060cd-143">You can set up a similar number sequence format for other legal entities.</span></span> <span data-ttu-id="060cd-144">على سبيل المثال، بالنسبة للكيان القانوني المسمى **RW**، إذا قمت بتغيير قيمة مقطع الكيان القانوني فقط، يكون الرقم المنسق هو RW-EXPENSE-0039.</span><span class="sxs-lookup"><span data-stu-id="060cd-144">For example, for a legal entity that is named **RW**, if you change only the value of the legal entity segment, the formatted number is RW-EXPENSE-0039.</span></span> <span data-ttu-id="060cd-145">يمكنك أيضًا تغيير تنسيق التسلسل الرقمي بالكامل للكيانات القانونية الأخرى.</span><span class="sxs-lookup"><span data-stu-id="060cd-145">You can also change the whole number sequence format for other legal entities.</span></span> <span data-ttu-id="060cd-146">على سبيل المثال، يمكنك حذف مقطع نطاق الكيان القانوني لإنشاء رقم منسق مثل Exp-0001.</span><span class="sxs-lookup"><span data-stu-id="060cd-146">For example, you can omit the legal entity scope segment to create a formatted number such as Exp-0001.</span></span>

### <a name="sales-order-numbers"></a><span data-ttu-id="060cd-147">أرقام أوامر المبيعات</span><span class="sxs-lookup"><span data-stu-id="060cd-147">Sales order numbers</span></span>

<span data-ttu-id="060cd-148">في المثال التالي، يتم إعداد أرقام أوامر المبيعات لمعرف الشركة **CEU**.</span><span class="sxs-lookup"><span data-stu-id="060cd-148">In the following example, sales order numbers are set up for the company ID **CEU**.</span></span> 

- <span data-ttu-id="060cd-149">**المجال:** المبيعات</span><span class="sxs-lookup"><span data-stu-id="060cd-149">**Area:** Sales</span></span> 
- <span data-ttu-id="060cd-150">**المرجع:** أمر مبيعات</span><span class="sxs-lookup"><span data-stu-id="060cd-150">**Reference:** Sales order</span></span> 
- <span data-ttu-id="060cd-151">**النطاق:** شركة</span><span class="sxs-lookup"><span data-stu-id="060cd-151">**Scope:** Company</span></span> 
- <span data-ttu-id="060cd-152">**الشركة:** CEU</span><span class="sxs-lookup"><span data-stu-id="060cd-152">**Company:** CEU</span></span>

| <span data-ttu-id="060cd-153">المقاطع</span><span class="sxs-lookup"><span data-stu-id="060cd-153">Segments</span></span>  | <span data-ttu-id="060cd-154">نوع المقطع</span><span class="sxs-lookup"><span data-stu-id="060cd-154">Segment type</span></span> | <span data-ttu-id="060cd-155">القيمة</span><span class="sxs-lookup"><span data-stu-id="060cd-155">Value</span></span>    |
|-----------|--------------|----------|
| <span data-ttu-id="060cd-156">المقطع 1</span><span class="sxs-lookup"><span data-stu-id="060cd-156">Segment 1</span></span> | <span data-ttu-id="060cd-157">ثابت</span><span class="sxs-lookup"><span data-stu-id="060cd-157">Constant</span></span>     | <span data-ttu-id="060cd-158">SO-</span><span class="sxs-lookup"><span data-stu-id="060cd-158">SO-</span></span>      |
| <span data-ttu-id="060cd-159">المقطع 2</span><span class="sxs-lookup"><span data-stu-id="060cd-159">Segment 2</span></span> | <span data-ttu-id="060cd-160">أبجدي رقمي</span><span class="sxs-lookup"><span data-stu-id="060cd-160">Alphanumeric</span></span> | \#\#\#\# |

<span data-ttu-id="060cd-161">**مثال على الرقم المنسق**: ‏SO-0029</span><span class="sxs-lookup"><span data-stu-id="060cd-161">**Example of formatted number**: SO-0029</span></span> 

<span data-ttu-id="060cd-162">على الرغم من عدم تضمين مقطع نطاق في التنسيق، تتم إعادة بدء الترقيم لكل معرف شركة.</span><span class="sxs-lookup"><span data-stu-id="060cd-162">Even though a scope segment is not included in the format, numbering restarts for each company ID.</span></span> <span data-ttu-id="060cd-163">إذا كنت تستخدم نفس التنسيق لكافة معرفات الشركة، يتم استخدام نفس الأرقام في كل شركة.</span><span class="sxs-lookup"><span data-stu-id="060cd-163">If you use the same format for all company IDs, the same numbers are used in each company.</span></span> <span data-ttu-id="060cd-164">على سبيل المثال، يتم استخدام رقم أمر المبيعات SO-0029 في كل شركة.</span><span class="sxs-lookup"><span data-stu-id="060cd-164">For example, sales order number SO-0029 is used in each company.</span></span> <span data-ttu-id="060cd-165">يمكنك أيضًا تغيير تنسيق التسلسل الرقمي بالكامل لمعرفات الشركات الأخرى.</span><span class="sxs-lookup"><span data-stu-id="060cd-165">You can also change the whole number sequence format for other company IDs.</span></span>

### <a name="purchase-requisition-numbers"></a><span data-ttu-id="060cd-166">أرقام طلبات الشراء</span><span class="sxs-lookup"><span data-stu-id="060cd-166">Purchase requisition numbers</span></span>

<span data-ttu-id="060cd-167">في المثال التالي، تكون أرقام طلبات الشراء على مستوى المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="060cd-167">In the following example, purchase requisition numbers are organization-wide.</span></span> 

- <span data-ttu-id="060cd-168">**المجال:** الشراء</span><span class="sxs-lookup"><span data-stu-id="060cd-168">**Area:** Purchase</span></span> 
- <span data-ttu-id="060cd-169">**المرجع:** طلب شراء</span><span class="sxs-lookup"><span data-stu-id="060cd-169">**Reference:** Purchase requisition</span></span> 
- <span data-ttu-id="060cd-170">**النطاق:** مشترك</span><span class="sxs-lookup"><span data-stu-id="060cd-170">**Scope:** Shared</span></span>

| <span data-ttu-id="060cd-171">المقاطع</span><span class="sxs-lookup"><span data-stu-id="060cd-171">Segments</span></span>  | <span data-ttu-id="060cd-172">نوع المقطع</span><span class="sxs-lookup"><span data-stu-id="060cd-172">Segment type</span></span> | <span data-ttu-id="060cd-173">القيمة</span><span class="sxs-lookup"><span data-stu-id="060cd-173">Value</span></span>    |
|-----------|--------------|----------|
| <span data-ttu-id="060cd-174">المقطع 1</span><span class="sxs-lookup"><span data-stu-id="060cd-174">Segment 1</span></span> | <span data-ttu-id="060cd-175">ثابت</span><span class="sxs-lookup"><span data-stu-id="060cd-175">Constant</span></span>     | <span data-ttu-id="060cd-176">Req</span><span class="sxs-lookup"><span data-stu-id="060cd-176">Req</span></span>      |
| <span data-ttu-id="060cd-177">المقطع 2</span><span class="sxs-lookup"><span data-stu-id="060cd-177">Segment 2</span></span> | <span data-ttu-id="060cd-178">أبجدي رقمي</span><span class="sxs-lookup"><span data-stu-id="060cd-178">Alphanumeric</span></span> | \#\#\#\# |

<span data-ttu-id="060cd-179">**مثال على الرقم المنسق**: ‏Req0052</span><span class="sxs-lookup"><span data-stu-id="060cd-179">**Example of formatted number**: Req0052</span></span> 

<span data-ttu-id="060cd-180">لأن النطاق **مشترك**، يتم استخدام تنسيق التسلسل الرقمي عبر المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="060cd-180">Because the scope is **Shared**, the number sequence format is used across the organization.</span></span> <span data-ttu-id="060cd-181">لا يمكنك إعداد تنسيقات تسلسلات رقمية مختلفة لأجزاء مختلفة من المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="060cd-181">You cannot set up different number sequence formats for different parts of the organization.</span></span> 

<a name="performance-considerations-for-number-sequences"></a><span data-ttu-id="060cd-182">اعتبارات الأداء للتسلسلات الرقمية</span><span class="sxs-lookup"><span data-stu-id="060cd-182">Performance considerations for number sequences</span></span>
-----------------------------------------------

<span data-ttu-id="060cd-183">ضع في اعتبارك المعلومات التالية حول كيف يمكن أن يؤثر تكوين التسلسلات الرقمية على أداء النظام قبل إعداد تسلسلات رقمية.</span><span class="sxs-lookup"><span data-stu-id="060cd-183">Consider the following information about how the configuration of number sequences can affect system performance before you set up number sequences.</span></span>

### <a name="continuous-and-non-continuous-number-sequences"></a><span data-ttu-id="060cd-184">التسلسلات الرقمية المتتالية وغير المتتالية</span><span class="sxs-lookup"><span data-stu-id="060cd-184">Continuous and non-continuous number sequences</span></span>

<span data-ttu-id="060cd-185">يمكن أن تكون التسلسلات الرقمية متتالية أو غير متتالية.</span><span class="sxs-lookup"><span data-stu-id="060cd-185">Number sequences can be continuous or non-continuous.</span></span> <span data-ttu-id="060cd-186">لا يتم من خلال التسلسل الرقمي المتتالي تخطي أي أرقام، ولكن لا يجوز استخدام الأرقام بشكلٍ تسلسلي.</span><span class="sxs-lookup"><span data-stu-id="060cd-186">A continuous number sequence does not skip any numbers, but numbers may not be used sequentially.</span></span> <span data-ttu-id="060cd-187">يتم استخدام الأرقام من التسلسلات الرقمية غير المتتالية بشكلٍ تسلسلي، ولكن يجوز للتسلسل الرقمي تخطي أرقام.</span><span class="sxs-lookup"><span data-stu-id="060cd-187">Numbers from a non-continuous number sequence are used sequentially, but the number sequence may skip numbers.</span></span> <span data-ttu-id="060cd-188">على سبيل المثال، إذا ألغى مستخدم حركة، يتم إنشاء رقم، ولكن لا يتم استخدامه.</span><span class="sxs-lookup"><span data-stu-id="060cd-188">For example, if a user cancels a transaction, a number is generated, but not used.</span></span> <span data-ttu-id="060cd-189">في تسلسل رقمي متتالٍ، تتم إعادة تدوير ذلك الرقم في وقتٍ لاحق.</span><span class="sxs-lookup"><span data-stu-id="060cd-189">In a continuous number sequence, that number is recycled later.</span></span> <span data-ttu-id="060cd-190">وفي تسلسل رقمي غير متتالي، لا يتم استخدام الرقم.</span><span class="sxs-lookup"><span data-stu-id="060cd-190">In a non-continuous number sequence, the number is not used.</span></span> 

<span data-ttu-id="060cd-191">تكون التسلسلات الرقمية المتتالية مطلوبة عادةً للمستندات الخارجية، مثل أوامر الشراء وأوامر المبيعات والفواتير.</span><span class="sxs-lookup"><span data-stu-id="060cd-191">Continuous number sequences are typically required for external documents, such as purchase orders, sales orders, and invoices.</span></span> <span data-ttu-id="060cd-192">ومع ذلك، يمكن أن تؤثر التسلسلات الرقمية المتتالية على أوقات استجابة النظام بشكلٍ سلبي لأن النظام يجب أن يطلب رقمًا من قاعدة البيانات في كل مرة يتم فيها إنشاء مستند أو سجل جديد.</span><span class="sxs-lookup"><span data-stu-id="060cd-192">However, continuous number sequences can adversely affect system response times because the system must request a number from the database every time that a new document or record is created.</span></span> 

<span data-ttu-id="060cd-193">إذا كنت تستخدم تسلسلاً رقميًا غير متتالي، يمكنك تمكين **التوزيع المسبق** في علامة التبويب السريع **الأداء** في صفحة **التسلسلات الرقمية**.</span><span class="sxs-lookup"><span data-stu-id="060cd-193">If you use a non-continuous number sequence, you can enable **Preallocation** on the **Performance** FastTab of the **Number sequences** page.</span></span> <span data-ttu-id="060cd-194">عند تحديد كمية أرقام لتخصيصها مسبقًا، يحدد النظام تلك الأرقام ويقوم بتخزينها في الذاكرة.</span><span class="sxs-lookup"><span data-stu-id="060cd-194">When you specify a quantity of numbers to preallocate, the system selects those numbers and stores them in memory.</span></span> <span data-ttu-id="060cd-195">ويتم طلب أرقام جديدة من قاعدة البيانات فقط بعد أن يتم استخدام الكمية المخصصة مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="060cd-195">New numbers are requested from the database only after the preallocated quantity has been used.</span></span> 

<span data-ttu-id="060cd-196">ما لم يكن هناك متطلبات تنظيمية باستخدام التسلسلات الرقمية المتتالية، نوصي باستخدام تسلسلات رقمية غير متتالية لأداء أفضل.</span><span class="sxs-lookup"><span data-stu-id="060cd-196">Unless there is a regulatory requirement that you use continuous number sequences, we recommend that you use non-continuous number sequences for better performance.</span></span>

### <a name="automatic-cleanup-of-number-sequences"></a><span data-ttu-id="060cd-197">التنظيف التلقائي للتسلسلات الرقمية</span><span class="sxs-lookup"><span data-stu-id="060cd-197">Automatic cleanup of number sequences</span></span>

<span data-ttu-id="060cd-198">في حالة انقطاع الطاقة أو حدوث خطأ في تطبيق ما أو وقوع أي عطل آخر غير متوقع، لا يمكن للنظام إعادة تدوير الأرقام تلقائيًا للتسلسلات الرقمية المتتالية.</span><span class="sxs-lookup"><span data-stu-id="060cd-198">In case of a power failure, an application error, or other unexpected failure, the system cannot recycle numbers automatically for continuous number sequences.</span></span> <span data-ttu-id="060cd-199">يمكنك تشغيل عملية التنظيف يدويًا أو تلقائيًا لاسترداد الأرقام المفقودة.</span><span class="sxs-lookup"><span data-stu-id="060cd-199">You can run the cleanup process manually or automatically to recover the lost numbers.</span></span> 

<span data-ttu-id="060cd-200">يجب مراعاة كيفية استخدام الملقم عند التخطيط لعملية التنظيف.</span><span class="sxs-lookup"><span data-stu-id="060cd-200">Carefully consider server usage when you plan the cleanup process.</span></span> <span data-ttu-id="060cd-201">يوصى بإجراء التنظيف كوظيفة مجموعة في غير ساعات الذروة.</span><span class="sxs-lookup"><span data-stu-id="060cd-201">We recommend that you perform the cleanup as a batch job during non-peak hours.</span></span>






