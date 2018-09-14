--- 
title: "إعداد قواعد عمولات المبيعات"
description: "يوضح هذا الإجراء كيفية إعداد حساب عمولة المبيعات والتعقب وتمكينهما."
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CommissionCustomerGroup, CommissionItemGroup, CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, CommissionCalc, InventPosting, CustTable, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 0ed7ec4ca74e4b6863ab2feff7f20de319789038
ms.contentlocale: ar-sa
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-sales-commission-rules"></a><span data-ttu-id="c118d-103">إعداد قواعد عمولات المبيعات</span><span class="sxs-lookup"><span data-stu-id="c118d-103">Set up sales commission rules</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c118d-104">يوضح هذا الإجراء كيفية إعداد حساب عمولة المبيعات والتعقب وتمكينهما.</span><span class="sxs-lookup"><span data-stu-id="c118d-104">This procedure shows you how to set up and enable sales commission calculation and tracking.</span></span> <span data-ttu-id="c118d-105">يوضح الإجراء كيفية إنشاء كل من مجموعات عمولات العملاء والأصناف ثم كيفية ربط عميل ومنتج محددين بكل مجموعة معنية.</span><span class="sxs-lookup"><span data-stu-id="c118d-105">The procedure shows how to create both customer and item commission groups, and then how to link a selected customer and product to the respective groups.</span></span> <span data-ttu-id="c118d-106">ثم تُستخدم هذه المجموعات في إعداد حساب العمولة لإنشاء مجموعة عملاء وأصناف ومندوبي مبيعات يجب أن مطابقتها بأمر المبيعات لتخويل أفراد المبيعات للحصول على عمولة.</span><span class="sxs-lookup"><span data-stu-id="c118d-106">Those groups are then used in the commission calculation setup to create a customer, item, and sales representatives combination that must be matched by the sales order to entitle the sales people to a commission.</span></span> <span data-ttu-id="c118d-107">يُعد إنشاء مجموعات عمولات العملاء والأصناف عملية اختيارية، كما يمكن أيضا حساب العمولة للعميل و/أو العنصر الفردي.</span><span class="sxs-lookup"><span data-stu-id="c118d-107">Creating customer and item commission groups are optional, as the calculation of commission can also be done for an individual customer and/or item.</span></span> <span data-ttu-id="c118d-108">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF أو باستخدام بياناتك الخاصة.</span><span class="sxs-lookup"><span data-stu-id="c118d-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-commission-groups-and-commission-rates"></a><span data-ttu-id="c118d-109">إعداد مجموعات العمولات ونسب العمولات</span><span class="sxs-lookup"><span data-stu-id="c118d-109">Set up commission groups and commission rates</span></span>
1. <span data-ttu-id="c118d-110">انتقل إلى المبيعات والتسويق > العمولات > مجموعات العملاء للعمولة.</span><span class="sxs-lookup"><span data-stu-id="c118d-110">Go to Sales and marketing > Commissions > Customer groups for commission.</span></span>
2. <span data-ttu-id="c118d-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="c118d-111">Click New.</span></span>
3. <span data-ttu-id="c118d-112">في الحقل "المجموعة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c118d-112">In the Group field, type a value.</span></span>
4. <span data-ttu-id="c118d-113">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c118d-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="c118d-114">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="c118d-114">Click Save.</span></span>
6. <span data-ttu-id="c118d-115">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c118d-115">Close the page.</span></span>
7. <span data-ttu-id="c118d-116">انتقل إلى المبيعات والتسويق > العمولات > مجموعات الأصناف.</span><span class="sxs-lookup"><span data-stu-id="c118d-116">Go to Sales and marketing > Commissions > Item groups.</span></span>
8. <span data-ttu-id="c118d-117">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="c118d-117">Click New.</span></span>
9. <span data-ttu-id="c118d-118">في الحقل "المجموعة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c118d-118">In the Group field, type a value.</span></span>
10. <span data-ttu-id="c118d-119">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c118d-119">In the Name field, type a value.</span></span>
11. <span data-ttu-id="c118d-120">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c118d-120">Close the page.</span></span>
12. <span data-ttu-id="c118d-121">انتقل إلى المبيعات والتسويق > العمولات > مجموعات المبيعات.</span><span class="sxs-lookup"><span data-stu-id="c118d-121">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="c118d-122">تحدد مجموعات مبيعات العمولة الموظفين في أدوار مندوب المبيعات المؤهلين لتلقي عمولة عندما يشتري عميل مرتبط ضمن مجموعة المبيعات ذات الصلة أصناف معينة.</span><span class="sxs-lookup"><span data-stu-id="c118d-122">A Commission sales group specifies the employees in sales representative roles who are eligible to receive a commission when a customer associated with the relevant sales group buys certain items.</span></span>  
    * <span data-ttu-id="c118d-123">في شركة بيانات العرض التوضيحي USMF، هناك مجموعة مبيعات تُسمى "مندوبي المبيعات- الولايات المتحدة."</span><span class="sxs-lookup"><span data-stu-id="c118d-123">In the USMF demo data company, there is a sales group called "Sales reps US."</span></span>  
13. <span data-ttu-id="c118d-124">في جزء "الإجراءات"، انقر فوق "عام".</span><span class="sxs-lookup"><span data-stu-id="c118d-124">On the Action Pane, click General.</span></span>
14. <span data-ttu-id="c118d-125">انقر فوق "مندوب المبيعات".</span><span class="sxs-lookup"><span data-stu-id="c118d-125">Click Sales rep..</span></span>
    * <span data-ttu-id="c118d-126">تعرض الصفحة مندوب المبيعات قائمة مندوبي مبيعات الشركة المقترنين بمجموعة عمولات محددة.</span><span class="sxs-lookup"><span data-stu-id="c118d-126">The Sales rep. page displays a list of the company's sales people who are associated with a specific commission group.</span></span> <span data-ttu-id="c118d-127">ويمكنك تعيين مندوبي مبيعات متعددين لنفس المجموعة وتحديد حصتهم ذات الصلة من رسوم العمولة الإجمالية كقيمة نسبة مئوية.</span><span class="sxs-lookup"><span data-stu-id="c118d-127">You can assign multiple sales representatives to the same group and define their respective share of the total commission fee as a percentage value.</span></span> <span data-ttu-id="c118d-128">يجب إلا يتجاوز إجمالي حصة العمولة لكافة الموظفين 100.</span><span class="sxs-lookup"><span data-stu-id="c118d-128">The total commission share across all employees must not exceed 100.</span></span>  
15. <span data-ttu-id="c118d-129">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c118d-129">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="c118d-130">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="c118d-130">Click Edit.</span></span>
17. <span data-ttu-id="c118d-131">قم بتعيين حصة العمولة على "50".</span><span class="sxs-lookup"><span data-stu-id="c118d-131">Set Commission share to '50'.</span></span>
18. <span data-ttu-id="c118d-132">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="c118d-132">Click New.</span></span>
19. <span data-ttu-id="c118d-133">في الحقل "الاسم"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="c118d-133">In the Name field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="c118d-134">استخدم عامل التصفية السريع للبحث عن السجلات.</span><span class="sxs-lookup"><span data-stu-id="c118d-134">Use the Quick Filter to find records.</span></span> <span data-ttu-id="c118d-135">على سبيل المثال، قم بإجراء التصفية بالحقل "الاسم" باستخدام قيمة "سوزان بيرك".</span><span class="sxs-lookup"><span data-stu-id="c118d-135">For example, filter on the Name field with a value of 'Susan Burk'.</span></span>
21. <span data-ttu-id="c118d-136">انقر فوق تحديد.</span><span class="sxs-lookup"><span data-stu-id="c118d-136">Click Select.</span></span>
22. <span data-ttu-id="c118d-137">قم بتعيين حصة العمولة على "50".</span><span class="sxs-lookup"><span data-stu-id="c118d-137">Set Commission share to '50'.</span></span>
23. <span data-ttu-id="c118d-138">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="c118d-138">Click Save.</span></span>
24. <span data-ttu-id="c118d-139">انتقل إلى المبيعات والتسويق > العمولات > حساب العمولات.</span><span class="sxs-lookup"><span data-stu-id="c118d-139">Go to Sales and marketing > Commissions > Commission calculation.</span></span>
    * <span data-ttu-id="c118d-140">في الصفحة "حساب العمولة" تقوم بتحديد نسبة العمولة التي سيحصل عليها الموظف مقابل حركة مبيعات عندما تحتوي على المجموعة المحددة مسبقًا المؤلفة من العميل والمنتج.</span><span class="sxs-lookup"><span data-stu-id="c118d-140">In the Commission calculation page you define the commission rate that the employee is to receive for a sales transaction when it contains the pre-set combination of customer and product.</span></span> <span data-ttu-id="c118d-141">وكجزء من إعداد نسبة العمولة، يجب تحديد أساس حساب العمولة وما إذا كان يجب أن يضمن الخصومات أو يستثنيها.</span><span class="sxs-lookup"><span data-stu-id="c118d-141">As part of the commission rate setup, you must specify the commission calculation basis and whether it should include or exclude discounts.</span></span> <span data-ttu-id="c118d-142">ويمكنك أيضًا إدخال فترة صلاحية عندما تكون نسبة العمولة نشطة.</span><span class="sxs-lookup"><span data-stu-id="c118d-142">You can also enter a validity period for when the commission rate is active.</span></span>  
25. <span data-ttu-id="c118d-143">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="c118d-143">Click New.</span></span>
26. <span data-ttu-id="c118d-144">في الحقل "كود الصنف"، حدد "مجموعة".</span><span class="sxs-lookup"><span data-stu-id="c118d-144">In the Item code field, select 'Group'.</span></span>
27. <span data-ttu-id="c118d-145">في الحقل "علاقة الصنف"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="c118d-145">In the Item relation field, click the drop-down button to open the lookup.</span></span>
28. <span data-ttu-id="c118d-146">في القائمة، ابحث عن المجموعة التي أنشأتها سابقًا وحددها.</span><span class="sxs-lookup"><span data-stu-id="c118d-146">In the list, find and select the group that you created earlier.</span></span>
29. <span data-ttu-id="c118d-147">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c118d-147">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="c118d-148">في الحقل "كود العميل"، حدد "مجموعة".</span><span class="sxs-lookup"><span data-stu-id="c118d-148">In the Customer code field, select 'Group'.</span></span>
31. <span data-ttu-id="c118d-149">في الحقل "علاقة العميل"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="c118d-149">In the Customer relation field, click the drop-down button to open the lookup.</span></span>
32. <span data-ttu-id="c118d-150">في القائمة، حدد المجموعة التي تريد قم بإعدادها سابقًا.</span><span class="sxs-lookup"><span data-stu-id="c118d-150">In the list, select the group that you set up earlier.</span></span>
33. <span data-ttu-id="c118d-151">في الحقل "علاقة مندوب المبيعات" انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="c118d-151">In the Sales rep. relation field, click the drop-down button to open the lookup.</span></span>
34. <span data-ttu-id="c118d-152">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c118d-152">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c118d-153">حافظ على خيار "قبل خصم البند".</span><span class="sxs-lookup"><span data-stu-id="c118d-153">Keep the "Before line discount" option.</span></span>  
    * <span data-ttu-id="c118d-154">حافظ على خيار "الإيراد" كأساس لحساب قيمة العمولة.</span><span class="sxs-lookup"><span data-stu-id="c118d-154">Keep the "Revenue" option as the basis for commission value calculation.</span></span>    
35. <span data-ttu-id="c118d-155">في الحقل "النسبة المئوية للعمولة، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="c118d-155">In the Commission percentage field, enter a number.</span></span>
36. <span data-ttu-id="c118d-156">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="c118d-156">Click Save.</span></span>

## <a name="setting-up-commission-posting"></a><span data-ttu-id="c118d-157">إعداد ترحيل العمولات</span><span class="sxs-lookup"><span data-stu-id="c118d-157">Setting up commission posting</span></span>
1. <span data-ttu-id="c118d-158">انتقل إلى المبيعات والتسويق > العمولات > ترحيل العمولات.</span><span class="sxs-lookup"><span data-stu-id="c118d-158">Go to Sales and marketing > Commissions > Commission posting.</span></span>
    * <span data-ttu-id="c118d-159">تُدفع رسوم العمولات للموظفين ولذلك يجب إعدادها للتأكد من صحة الترحيل المالي إلى الحسابات الملائمة في دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="c118d-159">Commission fees are payable to the employees and must therefore be set up to ensure correct financial posting to the appropriate accounts in the General ledger.</span></span> <span data-ttu-id="c118d-160">يتم هذا في الصفحة "ترحيل العمولة".</span><span class="sxs-lookup"><span data-stu-id="c118d-160">This is done in the Commission posting page.</span></span> <span data-ttu-id="c118d-161">قم بمراجعة الإعداد المتوفر في الشركة الحالية.</span><span class="sxs-lookup"><span data-stu-id="c118d-161">Review the setup that is available for the current company.</span></span> <span data-ttu-id="c118d-162">عادة، يتم ترحيل مبالغ العمولات إلى حساب مصروفات مخصص حجم العمولات وتكون مقابلة لحساب دائن مخصص.</span><span class="sxs-lookup"><span data-stu-id="c118d-162">Typically, the commission amounts are posted to a dedicated expense account and are offset to a dedicated payable account.</span></span> <span data-ttu-id="c118d-163">إذا لم يتوفر لديك إعداد قواعد ترحيل العمولات، فسيفشل النظام في إكمال فوترة أمر مبيعات له عمولات مؤهلة.</span><span class="sxs-lookup"><span data-stu-id="c118d-163">If you don't have the commission posting rules set up, the system will fail to complete invoicing of a sales order which has eligible commissions.</span></span>  
2. <span data-ttu-id="c118d-164">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c118d-164">Close the page.</span></span>

## <a name="assign-a-commission-group-to-a-customer-and-a-product"></a><span data-ttu-id="c118d-165">تعيين مجموعة عمولات لعميل ومنتج</span><span class="sxs-lookup"><span data-stu-id="c118d-165">Assign a commission group to a customer and a product</span></span>
1. <span data-ttu-id="c118d-166">انتقل إلى المبيعات والتسويق > العملاء > جميع العملاء.</span><span class="sxs-lookup"><span data-stu-id="c118d-166">Go to Sales and marketing > Customers > All customers.</span></span>
2. <span data-ttu-id="c118d-167">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c118d-167">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c118d-168">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c118d-168">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="c118d-169">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="c118d-169">Click Edit.</span></span>
5. <span data-ttu-id="c118d-170">قم بتوسيع القسم "إعدادات أوامر المبيعات الافتراضية".</span><span class="sxs-lookup"><span data-stu-id="c118d-170">Expand the Sales order defaults section.</span></span>
6. <span data-ttu-id="c118d-171">في الحقل "مجموعة العمولات"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="c118d-171">In the Commission group field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="c118d-172">في القائمة، حدد المجموعة التي أنشأتَها سابقًا.</span><span class="sxs-lookup"><span data-stu-id="c118d-172">In the list, select the group that you created earlier.</span></span>
8. <span data-ttu-id="c118d-173">في الحقل "مجموعة المبيعات"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="c118d-173">In the Sales group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="c118d-174">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c118d-174">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="c118d-175">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="c118d-175">Click Save.</span></span>
11. <span data-ttu-id="c118d-176">انتقل إلى إدارة معلومات المنتج > المنتجات > المنتجات الصادرة.</span><span class="sxs-lookup"><span data-stu-id="c118d-176">Go to Product information management > Products > Released products.</span></span>
12. <span data-ttu-id="c118d-177">استخدم عامل التصفية السريع للبحث عن السجلات.</span><span class="sxs-lookup"><span data-stu-id="c118d-177">Use the Quick Filter to find records.</span></span> <span data-ttu-id="c118d-178">على سبيل المثال، قم بإجراء التصفية بالحقل "رقم الصنف" باستخدام القيمة "0020".</span><span class="sxs-lookup"><span data-stu-id="c118d-178">For example, filter on the Item number field with a value of 'T0020 '.</span></span>
13. <span data-ttu-id="c118d-179">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c118d-179">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="c118d-180">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="c118d-180">Click Edit.</span></span>
15. <span data-ttu-id="c118d-181">قم بتوسيع القسم "البيع".</span><span class="sxs-lookup"><span data-stu-id="c118d-181">Expand the Sell section.</span></span>
16. <span data-ttu-id="c118d-182">في الحقل "مجموعة العمولات"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="c118d-182">In the Commission group field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="c118d-183">في القائمة، حدد مجموعة العمولات التي أنشأتَها سابقًا.</span><span class="sxs-lookup"><span data-stu-id="c118d-183">In the list, select the commission group that you created earlier.</span></span>


