---
title: إعداد قواعد عمولات المبيعات
description: يوضح هذا الإجراء كيفية إعداد حساب عمولة المبيعات والتعقب وتمكينهما.
author: omulvad
manager: tfehr
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CommissionCustomerGroup, CommissionItemGroup, CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, CommissionCalc, InventPosting, CustTable, EcoResProductDetailsExtended, CommissionEmplSalesGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab352e1174dbee65f676c5b9bae45f2947dbcd6f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232244"
---
# <a name="set-up-sales-commission-rules"></a><span data-ttu-id="433a6-103">إعداد قواعد عمولات المبيعات</span><span class="sxs-lookup"><span data-stu-id="433a6-103">Set up sales commission rules</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="433a6-104">يوضح هذا الإجراء كيفية إعداد حساب عمولة المبيعات والتعقب وتمكينهما.</span><span class="sxs-lookup"><span data-stu-id="433a6-104">This procedure shows you how to set up and enable sales commission calculation and tracking.</span></span> <span data-ttu-id="433a6-105">يوضح الإجراء كيفية إنشاء كل من مجموعات عمولات العملاء والأصناف ثم كيفية ربط عميل ومنتج محددين بكل مجموعة معنية.</span><span class="sxs-lookup"><span data-stu-id="433a6-105">The procedure shows how to create both customer and item commission groups, and then how to link a selected customer and product to the respective groups.</span></span> <span data-ttu-id="433a6-106">ثم تُستخدم هذه المجموعات في إعداد حساب العمولة لإنشاء مجموعة عملاء وأصناف ومندوبي مبيعات يجب أن مطابقتها بأمر المبيعات لتخويل أفراد المبيعات للحصول على عمولة.</span><span class="sxs-lookup"><span data-stu-id="433a6-106">Those groups are then used in the commission calculation setup to create a customer, item, and sales representatives combination that must be matched by the sales order to entitle the sales people to a commission.</span></span> <span data-ttu-id="433a6-107">يُعد إنشاء مجموعات عمولات العملاء والأصناف عملية اختيارية، كما يمكن أيضا حساب العمولة للعميل و/أو العنصر الفردي.</span><span class="sxs-lookup"><span data-stu-id="433a6-107">Creating customer and item commission groups are optional, as the calculation of commission can also be done for an individual customer and/or item.</span></span> <span data-ttu-id="433a6-108">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF أو باستخدام بياناتك الخاصة.</span><span class="sxs-lookup"><span data-stu-id="433a6-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-commission-groups-and-commission-rates"></a><span data-ttu-id="433a6-109">إعداد مجموعات العمولات ونسب العمولات</span><span class="sxs-lookup"><span data-stu-id="433a6-109">Set up commission groups and commission rates</span></span>
1. <span data-ttu-id="433a6-110">انتقل إلى **جزء التنقل > الوحدات النمطية > المبيعات والتسويق > العمولات > مجموعات العملاء للعمولة**.</span><span class="sxs-lookup"><span data-stu-id="433a6-110">Go to **Navigation pane > Modules > Sales and marketing > Commissions > Customer groups for commission**.</span></span>
2. <span data-ttu-id="433a6-111">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="433a6-111">Select **New**.</span></span>
3. <span data-ttu-id="433a6-112">في الحقل **المجموعة**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="433a6-112">In the **Group** field, type a value.</span></span>
4. <span data-ttu-id="433a6-113">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="433a6-113">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="433a6-114">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="433a6-114">Select **Save**.</span></span>
6. <span data-ttu-id="433a6-115">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="433a6-115">Close the page.</span></span>
7. <span data-ttu-id="433a6-116">انتقل إلى **جزء التنقل > الوحدات النمطية > المبيعات والتسويق > العمولات > ‏‫مجموعات الأصناف‬**.</span><span class="sxs-lookup"><span data-stu-id="433a6-116">Go to **Navigation pane > Modules > Sales and marketing > Commissions > Item groups**.</span></span>
8. <span data-ttu-id="433a6-117">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="433a6-117">Select **New**.</span></span>
9. <span data-ttu-id="433a6-118">في الحقل **المجموعة**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="433a6-118">In the **Group** field, type a value.</span></span>
10. <span data-ttu-id="433a6-119">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="433a6-119">In the **Name** field, type a value.</span></span>
11. <span data-ttu-id="433a6-120">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="433a6-120">Select **Save**.</span></span>
12. <span data-ttu-id="433a6-121">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="433a6-121">Close the page.</span></span>
13. <span data-ttu-id="433a6-122">انتقل إلى **المبيعات والتسويق > العمولات > مجموعات المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="433a6-122">Go to **Sales and marketing > Commissions > Sales groups**.</span></span>
    - <span data-ttu-id="433a6-123">تحدد مجموعات مبيعات العمولة الموظفين في أدوار مندوب المبيعات المؤهلين لتلقي عمولة عندما يشتري عميل مرتبط ضمن مجموعة المبيعات ذات الصلة أصناف معينة.</span><span class="sxs-lookup"><span data-stu-id="433a6-123">A Commission sales group specifies the employees in sales representative roles who are eligible to receive a commission when a customer associated with the relevant sales group buys certain items.</span></span>  
    - <span data-ttu-id="433a6-124">في شركة بيانات العرض التوضيحي USMF، هناك مجموعة مبيعات تُسمى "مندوبي المبيعات- الولايات المتحدة."</span><span class="sxs-lookup"><span data-stu-id="433a6-124">In the USMF demo data company, there is a sales group called "Sales reps US."</span></span>  
14. <span data-ttu-id="433a6-125">في **جزء الإجراءات**، حدد **عام**.</span><span class="sxs-lookup"><span data-stu-id="433a6-125">On the **Action Pane**, select **General**.</span></span>
15. <span data-ttu-id="433a6-126">انقر فوق **مندوب المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="433a6-126">Click **Sales rep.**.</span></span> <span data-ttu-id="433a6-127">تعرض الصفحة مندوب المبيعات قائمة مندوبي مبيعات الشركة المقترنين بمجموعة عمولات محددة.</span><span class="sxs-lookup"><span data-stu-id="433a6-127">The Sales rep. page displays a list of the company's sales people who are associated with a specific commission group.</span></span> <span data-ttu-id="433a6-128">ويمكنك تعيين مندوبي مبيعات متعددين لنفس المجموعة وتحديد حصتهم ذات الصلة من رسوم العمولة الإجمالية كقيمة نسبة مئوية.</span><span class="sxs-lookup"><span data-stu-id="433a6-128">You can assign multiple sales representatives to the same group and define their respective share of the total commission fee as a percentage value.</span></span> <span data-ttu-id="433a6-129">يجب إلا يتجاوز إجمالي حصة العمولة لكافة الموظفين 100.</span><span class="sxs-lookup"><span data-stu-id="433a6-129">The total commission share across all employees must not exceed 100.</span></span> 
16. <span data-ttu-id="433a6-130">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="433a6-130">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="433a6-131">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="433a6-131">Select **Edit**.</span></span>
18. <span data-ttu-id="433a6-132">قم بتعيين **حصة العمولة** على "50".</span><span class="sxs-lookup"><span data-stu-id="433a6-132">Set **Commission share** to '50'.</span></span>
19. <span data-ttu-id="433a6-133">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="433a6-133">Click **New**.</span></span>
20. <span data-ttu-id="433a6-134">في الحقل **الاسم**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="433a6-134">In the **Name** field, click the drop-down button to open the lookup.</span></span>
21. <span data-ttu-id="433a6-135">استخدم **عامل التصفية السريع** للبحث عن السجلات.</span><span class="sxs-lookup"><span data-stu-id="433a6-135">Use the **Quick Filter** to find records.</span></span> <span data-ttu-id="433a6-136">على سبيل المثال، قم بإجراء التصفية بالحقل "الاسم" باستخدام قيمة "سوزان بيرك".</span><span class="sxs-lookup"><span data-stu-id="433a6-136">For example, filter on the Name field with a value of 'Susan Burk'.</span></span>
22. <span data-ttu-id="433a6-137">انقر فوق **تحديد**.</span><span class="sxs-lookup"><span data-stu-id="433a6-137">Click **Select**.</span></span>
23. <span data-ttu-id="433a6-138">قم بتعيين **حصة العمولة** على "50".</span><span class="sxs-lookup"><span data-stu-id="433a6-138">Set **Commission share** to '50'.</span></span>
24. <span data-ttu-id="433a6-139">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="433a6-139">Click **Save**.</span></span>
25. <span data-ttu-id="433a6-140">انتقل إلى **المبيعات والتسويق > العمولات > حساب العمولات**.</span><span class="sxs-lookup"><span data-stu-id="433a6-140">Go to **Sales and marketing > Commissions > Commission calculation**.</span></span> <span data-ttu-id="433a6-141">في الصفحة **حساب العمولة** تقوم بتحديد نسبة العمولة التي سيحصل عليها الموظف مقابل حركة مبيعات عندما تحتوي على المجموعة المحددة مسبقًا المؤلفة من العميل والمنتج.</span><span class="sxs-lookup"><span data-stu-id="433a6-141">In the **Commission calculation** page, you define the commission rate that the employee is to receive for a sales transaction when it contains the pre-set combination of customer and product.</span></span> <span data-ttu-id="433a6-142">وكجزء من إعداد نسبة العمولة، يجب تحديد أساس حساب العمولة وما إذا كان يجب أن يضمن الخصومات أو يستثنيها.</span><span class="sxs-lookup"><span data-stu-id="433a6-142">As part of the commission rate setup, you must specify the commission calculation basis and whether it should include or exclude discounts.</span></span> <span data-ttu-id="433a6-143">ويمكنك أيضًا إدخال فترة صلاحية عندما تكون نسبة العمولة نشطة.</span><span class="sxs-lookup"><span data-stu-id="433a6-143">You can also enter a validity period for when the commission rate is active.</span></span>  
26. <span data-ttu-id="433a6-144">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="433a6-144">Click **New**.</span></span>
27. <span data-ttu-id="433a6-145">في الحقل **كود الصنف**، حدد "مجموعة".</span><span class="sxs-lookup"><span data-stu-id="433a6-145">In the **Item code** field, select 'Group'.</span></span>
28. <span data-ttu-id="433a6-146">في الحقل **علاقة الصنف**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="433a6-146">In the **Item relation** field, click the drop-down button to open the lookup.</span></span>
29. <span data-ttu-id="433a6-147">في القائمة، ابحث عن المجموعة التي أنشأتها سابقًا وحددها.</span><span class="sxs-lookup"><span data-stu-id="433a6-147">In the list, find and select the group that you created earlier.</span></span>
30. <span data-ttu-id="433a6-148">في الحقل **كود العميل**، حدد "مجموعة".</span><span class="sxs-lookup"><span data-stu-id="433a6-148">In the **Customer code** field, select 'Group'.</span></span>
31. <span data-ttu-id="433a6-149">في الحقل **علاقة العميل**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="433a6-149">In the **Customer relation** field, click the drop-down button to open the lookup.</span></span>
32. <span data-ttu-id="433a6-150">في القائمة، حدد المجموعة التي تريد قم بإعدادها سابقًا.</span><span class="sxs-lookup"><span data-stu-id="433a6-150">In the list, select the group that you set up earlier.</span></span>
33. <span data-ttu-id="433a6-151">في الحقل **علاقة مندوب المبيعات** انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="433a6-151">In the **Sales rep. relation** field, click the drop-down button to open the lookup.</span></span>
34. <span data-ttu-id="433a6-152">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="433a6-152">In the list, find and select the desired record.</span></span>
    - <span data-ttu-id="433a6-153">حافظ على خيار "قبل خصم البند".</span><span class="sxs-lookup"><span data-stu-id="433a6-153">Keep the "Before line discount" option.</span></span>  
    - <span data-ttu-id="433a6-154">حافظ على خيار "الإيراد" كأساس لحساب قيمة العمولة.</span><span class="sxs-lookup"><span data-stu-id="433a6-154">Keep the "Revenue" option as the basis for commission value calculation.</span></span>    
35. <span data-ttu-id="433a6-155">في الحقل "النسبة المئوية للعمولة، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="433a6-155">In the Commission percentage field, enter a number.</span></span>
36. <span data-ttu-id="433a6-156">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="433a6-156">Click **Save**.</span></span>

## <a name="setting-up-commission-posting"></a><span data-ttu-id="433a6-157">إعداد ترحيل العمولات</span><span class="sxs-lookup"><span data-stu-id="433a6-157">Setting up commission posting</span></span>
1. <span data-ttu-id="433a6-158">انتقل إلى **‏‫جزء التنقل‬ > المبيعات والتسويق > العمولات > ترحيل العمولات**.</span><span class="sxs-lookup"><span data-stu-id="433a6-158">Go to **Navigation pane  > Sales and marketing > Commissions > Commission posting**.</span></span> <span data-ttu-id="433a6-159">تُدفع رسوم العمولات للموظفين ولذلك يجب إعدادها للتأكد من صحة الترحيل المالي إلى الحسابات الملائمة في **دفتر الأستاذ العام**.</span><span class="sxs-lookup"><span data-stu-id="433a6-159">Commission fees are payable to the employees and must therefore be set up to ensure correct financial posting to the appropriate accounts in the **General ledger**.</span></span> <span data-ttu-id="433a6-160">يتم هذا في الصفحة **ترحيل العمولة**.</span><span class="sxs-lookup"><span data-stu-id="433a6-160">This is done in the **Commission posting** page.</span></span> <span data-ttu-id="433a6-161">قم بمراجعة الإعداد المتوفر في الشركة الحالية.</span><span class="sxs-lookup"><span data-stu-id="433a6-161">Review the setup that is available for the current company.</span></span> <span data-ttu-id="433a6-162">عادة، يتم ترحيل مبالغ العمولات إلى حساب مصروفات مخصص حجم العمولات وتكون مقابلة لحساب دائن مخصص.</span><span class="sxs-lookup"><span data-stu-id="433a6-162">Typically, the commission amounts are posted to a dedicated expense account and are offset to a dedicated payable account.</span></span> <span data-ttu-id="433a6-163">إذا لم يتوفر لديك إعداد قواعد ترحيل العمولات، فسيفشل النظام في إكمال فوترة أمر مبيعات له عمولات مؤهلة.</span><span class="sxs-lookup"><span data-stu-id="433a6-163">If you don't have the commission posting rules set up, the system will fail to complete invoicing of a sales order which has eligible commissions.</span></span>  
2. <span data-ttu-id="433a6-164">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="433a6-164">Close the page.</span></span>

## <a name="assign-a-commission-group-to-a-customer-and-a-product"></a><span data-ttu-id="433a6-165">تعيين مجموعة عمولات لعميل ومنتج</span><span class="sxs-lookup"><span data-stu-id="433a6-165">Assign a commission group to a customer and a product</span></span>
1. <span data-ttu-id="433a6-166">انتقل إلى **جزء التنقل > الوحدات النمطية > المبيعات والتسويق > العملاء > كافة العملاء**.</span><span class="sxs-lookup"><span data-stu-id="433a6-166">Go to **Navigation pane > Modules > Sales and marketing > Customers > All customers**.</span></span>
2. <span data-ttu-id="433a6-167">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="433a6-167">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="433a6-168">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="433a6-168">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="433a6-169">انقر فوق **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="433a6-169">Click **Edit**.</span></span>
5. <span data-ttu-id="433a6-170">‎قم بتوسيع القسم **إعدادات أوامر المبيعات الافتراضية**.</span><span class="sxs-lookup"><span data-stu-id="433a6-170">Expand the **Sales order defaults** section.</span></span>
6. <span data-ttu-id="433a6-171">في الحقل **مجموعة العمولات**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="433a6-171">In the **Commission group** field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="433a6-172">في القائمة، حدد المجموعة التي أنشأتَها سابقًا.</span><span class="sxs-lookup"><span data-stu-id="433a6-172">In the list, select the group that you created earlier.</span></span>
8. <span data-ttu-id="433a6-173">في الحقل **مجموعة المبيعات**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="433a6-173">In the **Sales group** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="433a6-174">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="433a6-174">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="433a6-175">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="433a6-175">Click **Save**.</span></span>
11. <span data-ttu-id="433a6-176">‏‫انتقل إلى ‬**جزء التنقل > الوحدات > إدارة معلومات المنتج > المنتجات > المنتجات الصادرة‬** .</span><span class="sxs-lookup"><span data-stu-id="433a6-176">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
12. <span data-ttu-id="433a6-177">استخدم **عامل التصفية** للبحث عن السجلات.</span><span class="sxs-lookup"><span data-stu-id="433a6-177">Use the **Filter** to find records.</span></span> <span data-ttu-id="433a6-178">على سبيل المثال، قم بإجراء التصفية بالحقل "رقم الصنف" باستخدام القيمة "0020".</span><span class="sxs-lookup"><span data-stu-id="433a6-178">For example, filter on the Item number field with a value of 'T0020 '.</span></span>
13. <span data-ttu-id="433a6-179">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="433a6-179">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="433a6-180">انقر فوق **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="433a6-180">Click **Edit**.</span></span>
15. <span data-ttu-id="433a6-181">‎قم بتوسيع القسم **البيع**.</span><span class="sxs-lookup"><span data-stu-id="433a6-181">Expand the **Sell** section.</span></span>
16. <span data-ttu-id="433a6-182">في الحقل **مجموعة العمولات**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="433a6-182">In the **Commission group** field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="433a6-183">في القائمة، حدد مجموعة العمولات التي أنشأتَها سابقًا.</span><span class="sxs-lookup"><span data-stu-id="433a6-183">In the list, select the commission group that you created earlier.</span></span>
18. <span data-ttu-id="433a6-184">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="433a6-184">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]