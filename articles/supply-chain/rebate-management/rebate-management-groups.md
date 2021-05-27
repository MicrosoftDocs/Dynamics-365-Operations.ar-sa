---
title: مجموعات إدارة الخصومات
description: يصف هذا الموضوع كيفية إعداد بيانات مجموعات إدارة الخصومات. يمكن استخدام مجموعات أداره الخصم اثناء حسابات الخصومات ويمكن إرفاقها بسجل رئيسي.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: c9e1cadae97bd8f0dea270deaa1a8e09bb28eb4b
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020473"
---
# <a name="rebate-management-groups"></a><span data-ttu-id="e2d18-104">مجموعات إدارة الخصومات</span><span class="sxs-lookup"><span data-stu-id="e2d18-104">Rebate management groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e2d18-105">يمكن ان تعتمد حسابات الخصم والخصم علي المجموعات.</span><span class="sxs-lookup"><span data-stu-id="e2d18-105">Rebate and deduction calculations can be driven by groups.</span></span> <span data-ttu-id="e2d18-106">يمكن إنشاء مجموعات أداره الخصم للعملاء والموردين والأصناف.</span><span class="sxs-lookup"><span data-stu-id="e2d18-106">Rebate management groups can be created for customers, vendors, and items.</span></span> <span data-ttu-id="e2d18-107">يمكن إرفاقها بسجل رئيسي.</span><span class="sxs-lookup"><span data-stu-id="e2d18-107">They can be attached to a master record.</span></span>

## <a name="rebate-management-customer-groups"></a><span data-ttu-id="e2d18-108">مجموعات عملاء إدارة الخصومات</span><span class="sxs-lookup"><span data-stu-id="e2d18-108">Rebate management customer groups</span></span>

<span data-ttu-id="e2d18-109">غالبًا ما يتم إنشاء الحساب لمجموعة من العملاء لسلسلة من الشركات، مثل سلسلة سوبر ماركت أو شركة امتياز.</span><span class="sxs-lookup"><span data-stu-id="e2d18-109">The calculation for a group of customers is often created for a chain of companies, such as a supermarket chain or a franchise company.</span></span> <span data-ttu-id="e2d18-110">عاده ما يرتبط هذا النوع من الحساب بالخصم.</span><span class="sxs-lookup"><span data-stu-id="e2d18-110">This type of calculation is usually related to a rebate.</span></span>

<span data-ttu-id="e2d18-111">غالبا ما يتم حساب الخصم دون الأخذ في الاعتبار من بيع أمر التاهيل.</span><span class="sxs-lookup"><span data-stu-id="e2d18-111">A deduction is often calculated without considering who the qualifying order was sold to.</span></span> <span data-ttu-id="e2d18-112">ومع ذلك، هناك استثناءات.</span><span class="sxs-lookup"><span data-stu-id="e2d18-112">However, there are exceptions.</span></span> <span data-ttu-id="e2d18-113">على سبيل المثال، قد ينشئ المرخص له مخطط خصم حيث ستحصل مجموعة العملاء أ على 4 في المائة، لكن مجموعة العملاء ب ستحصل على 3 في المائة فقط.</span><span class="sxs-lookup"><span data-stu-id="e2d18-113">For example, a licensee might create a deduction scheme where customer group A will receive 4 percent, but customer group B will receive only 3 percent.</span></span>

### <a name="set-up-customer-groups"></a><span data-ttu-id="e2d18-114">إعداد مجموعات العملاء</span><span class="sxs-lookup"><span data-stu-id="e2d18-114">Set up customer groups</span></span>

<span data-ttu-id="e2d18-115">للعمل مع مجموعات عملاء إدارة الخصم، انتقل إلى **إدارة الخصومات \> إعداد مجموعات إدارة الخصومات\> مجموعات العملاء**.</span><span class="sxs-lookup"><span data-stu-id="e2d18-115">To work with Rebate management customer groups, go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span> <span data-ttu-id="e2d18-116">يمكنك استخدام الأزرار الموجودة في جزء الإجراءات لإضافة المجموعات وإزالتها كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="e2d18-116">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="e2d18-117">بالنسبة لكل مجموعة، قم بتعيين الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="e2d18-117">For each group, set the following fields:</span></span>

- <span data-ttu-id="e2d18-118">**مجموعة إدارة الخصومات** – أدخل اسمًا فريدًا للمجموعة.</span><span class="sxs-lookup"><span data-stu-id="e2d18-118">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="e2d18-119">**الوصف** – ادخل وصفا للمجموعة لتوفير مزيد من المعلومات حول كيفيه استخدامه.</span><span class="sxs-lookup"><span data-stu-id="e2d18-119">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-customer-group-assignments"></a><span data-ttu-id="e2d18-120">إدارة تعيينات مجموعات العملاء</span><span class="sxs-lookup"><span data-stu-id="e2d18-120">Manage customer group assignments</span></span>

<span data-ttu-id="e2d18-121">يمكن ان ينتمي كل عميل إلى اي عدد من مجموعات أداره الخصم.</span><span class="sxs-lookup"><span data-stu-id="e2d18-121">Each customer can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="e2d18-122">لعرض أعضاء المجموعة وتعيينهم، يمكنك البدء اما من قائمه المجموعات أو من قائمه العملاء.</span><span class="sxs-lookup"><span data-stu-id="e2d18-122">To view and assign group members, you can start from either the group list or the customer list.</span></span>

<span data-ttu-id="e2d18-123">لعرض العملاء لمجموعه محدده أو اضافتهم أو ازالتهم، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="e2d18-123">To view, add, or remove customers for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="e2d18-124">انتقل إلى **إدارة الخصومات \> إعداد مجموعات إدارة الخصومات \> مجموعات العملاء**.</span><span class="sxs-lookup"><span data-stu-id="e2d18-124">Go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span>
1. <span data-ttu-id="e2d18-125">حدد المجموعة المطلوب إدارتها.</span><span class="sxs-lookup"><span data-stu-id="e2d18-125">Select the group to manage.</span></span>
1. <span data-ttu-id="e2d18-126">في جزء الإجراء، حدد **العملاء**.</span><span class="sxs-lookup"><span data-stu-id="e2d18-126">On the Action Pane, select **Customers**.</span></span> <span data-ttu-id="e2d18-127">تظهر صفحة **مجموعة إدارة الخصومات** وتعرض قائمة العملاء الأعضاء بالفعل في المجموعة المحددة.</span><span class="sxs-lookup"><span data-stu-id="e2d18-127">The **Rebate management groups** page appears and shows a list of customers that are already members of the selected group.</span></span>
1. <span data-ttu-id="e2d18-128">لإضافة عميل جديد إلى المجموعة، حدد **جديد** في جزء الإجراءات لإضافة صف إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="e2d18-128">To add a new customer to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="e2d18-129">ثم قم بتعيين الحقول التالية للصف الجديد:</span><span class="sxs-lookup"><span data-stu-id="e2d18-129">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="e2d18-130">**حساب العميل** – حدد معرف حساب العميل.</span><span class="sxs-lookup"><span data-stu-id="e2d18-130">**Customer account** – Select the customer account ID.</span></span>
    - <span data-ttu-id="e2d18-131">**الاسم** – أدخل اسمًا و / أو وصفًا للعميل.</span><span class="sxs-lookup"><span data-stu-id="e2d18-131">**Name** – Enter a name and/or description of the customer.</span></span>

1. <span data-ttu-id="e2d18-132">لأزاله عميل من المجموعة، حدد العميل، ثم حدد **حذف** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="e2d18-132">To remove a customer from the group, select the customer, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="e2d18-133">لعرض أو إضافة أو إزالة تعيينات المجموعة لعميل محدد، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="e2d18-133">To view, add, or remove group assignments for a selected customer, follow these steps.</span></span>

1. <span data-ttu-id="e2d18-134">انتقل إلى **الحسابات المدينة \> العملاء \> كافة العملاء**.</span><span class="sxs-lookup"><span data-stu-id="e2d18-134">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="e2d18-135">حدد العميل المراد التعامل معه.</span><span class="sxs-lookup"><span data-stu-id="e2d18-135">Select the customer to work with.</span></span>
1. <span data-ttu-id="e2d18-136">في جزء الإجراء، في علامة التبويب **العميل**، في مجموعة **إدارة الخصومات**، حدد **مجموعات إدارة الخصومات**.</span><span class="sxs-lookup"><span data-stu-id="e2d18-136">On the Action Pane, on the **Customer** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="e2d18-137">تظهر صفحة **مجموعة إدارة الخصومات** وتعرض قائمة المجموعات التي ينتمي إليها العميل المحدد بالفعل.</span><span class="sxs-lookup"><span data-stu-id="e2d18-137">The **Rebate management groups** page appears and shows a list of groups that the selected customer already belongs to.</span></span>
1. <span data-ttu-id="e2d18-138">لإضافة العميل إلى مجموعة جديدة، حدد **جديد** في جزء الإجراءات لإضافة صف إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="e2d18-138">To add the customer to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="e2d18-139">ثم قم بتعيين الحقول التالية للصف الجديد:</span><span class="sxs-lookup"><span data-stu-id="e2d18-139">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="e2d18-140">**مجموعه إدارة الخصومات** - حدد المجموعة التي سيتم أضافه العميل اليها.</span><span class="sxs-lookup"><span data-stu-id="e2d18-140">**Rebate management group** – Select the group to add the customer to.</span></span>
    - <span data-ttu-id="e2d18-141">**الوصف** – أدخل وصفًا للمجموعة (على سبيل المثال، لشرح سبب كون العميل عضوًا فيها).</span><span class="sxs-lookup"><span data-stu-id="e2d18-141">**Description** – Enter a description of the group (for example, to explain why the customer is a member of it).</span></span>

1. <span data-ttu-id="e2d18-142">لإزالة عميل من مجموعة، حدد المجموعة، ثم حدد **حذف** في جزء الإجراء.</span><span class="sxs-lookup"><span data-stu-id="e2d18-142">To remove a customer from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="rebate-management-vendor-groups"></a><span data-ttu-id="e2d18-143">مجموعات موردين إدارة الخصومات</span><span class="sxs-lookup"><span data-stu-id="e2d18-143">Rebate management vendor groups</span></span>

<span data-ttu-id="e2d18-144">عاده ما يتم إنشاء حساب لمجموعه من الموردين لمجموعه من نقاط التسليم.</span><span class="sxs-lookup"><span data-stu-id="e2d18-144">The calculation for a group of vendors is often created for a group of delivery points.</span></span> <span data-ttu-id="e2d18-145">عاده ما يرتبط هذا النوع من الحساب بالخصم.</span><span class="sxs-lookup"><span data-stu-id="e2d18-145">This type of calculation is usually related to a rebate.</span></span>

### <a name="set-up-vendor-groups"></a><span data-ttu-id="e2d18-146">إعداد مجموعات الموردين</span><span class="sxs-lookup"><span data-stu-id="e2d18-146">Set up vendor groups</span></span>

<span data-ttu-id="e2d18-147">للعمل مع مجموعات موردين إدارة الخصم، انتقل إلى **إدارة الخصومات \> إعداد مجموعات إدارة الخصومات\> مجموعات الموردين**.</span><span class="sxs-lookup"><span data-stu-id="e2d18-147">To work with Rebate management vendor groups, go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span> <span data-ttu-id="e2d18-148">يمكنك استخدام الأزرار الموجودة في جزء الإجراءات لإضافة المجموعات وإزالتها كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="e2d18-148">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="e2d18-149">بالنسبة لكل مجموعة، قم بتعيين الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="e2d18-149">For each group, set the following fields:</span></span>

- <span data-ttu-id="e2d18-150">**مجموعة إدارة الخصومات** – أدخل اسمًا فريدًا للمجموعة.</span><span class="sxs-lookup"><span data-stu-id="e2d18-150">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="e2d18-151">**الوصف** – ادخل وصفا للمجموعة لتوفير مزيد من المعلومات حول كيفيه استخدامه.</span><span class="sxs-lookup"><span data-stu-id="e2d18-151">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-vendor-group-assignments"></a><span data-ttu-id="e2d18-152">إدارة تعيينات مجموعات الموردين</span><span class="sxs-lookup"><span data-stu-id="e2d18-152">Manage vendor group assignments</span></span>

<span data-ttu-id="e2d18-153">يمكن ان ينتمي كل مورد إلى اي عدد من مجموعات أداره الخصم.</span><span class="sxs-lookup"><span data-stu-id="e2d18-153">Each vendor can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="e2d18-154">لعرض أعضاء المجموعة وتعيينهم، يمكنك البدء اما من قائمه المجموعات أو من قائمه الموردين.</span><span class="sxs-lookup"><span data-stu-id="e2d18-154">To view and assign group members, you can start from either the group list or the vendor list.</span></span>

<span data-ttu-id="e2d18-155">لعرض الموردين لمجموعه محدده أو اضافتهم أو ازالتهم، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="e2d18-155">To view, add, or remove vendors for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="e2d18-156">انتقل إلى **إدارة الخصومات \> إعداد مجموعات إدارة الخصومات \> مجموعات الموردين**.</span><span class="sxs-lookup"><span data-stu-id="e2d18-156">Go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span>
1. <span data-ttu-id="e2d18-157">حدد المجموعة المطلوب إدارتها.</span><span class="sxs-lookup"><span data-stu-id="e2d18-157">Select the group to manage.</span></span>
1. <span data-ttu-id="e2d18-158">في جزء الإجراءات، حدد **المورّدين**.</span><span class="sxs-lookup"><span data-stu-id="e2d18-158">On the Action Pane, select **Vendors**.</span></span> <span data-ttu-id="e2d18-159">تظهر صفحة **مجموعة إدارة الخصومات** وتعرض قائمة الموردين الأعضاء بالفعل في المجموعة المحددة.</span><span class="sxs-lookup"><span data-stu-id="e2d18-159">The **Rebate management groups** page appears and shows a list of vendors that are already members of the selected group.</span></span>
1. <span data-ttu-id="e2d18-160">لإضافة مورد جديد إلى المجموعة، حدد **جديد** في جزء الإجراءات لإضافة صف إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="e2d18-160">To add a new vendor to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="e2d18-161">ثم قم بتعيين الحقول التالية للصف الجديد:</span><span class="sxs-lookup"><span data-stu-id="e2d18-161">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="e2d18-162">**حساب المورد** – حدد معرف حساب المورد.</span><span class="sxs-lookup"><span data-stu-id="e2d18-162">**Vendor account** – Select the vendor account ID.</span></span>
    - <span data-ttu-id="e2d18-163">**الاسم** – أدخل اسمًا و / أو وصفًا للمورد.</span><span class="sxs-lookup"><span data-stu-id="e2d18-163">**Name** – Enter a name and/or description of the vendor.</span></span>

1. <span data-ttu-id="e2d18-164">لأزاله مورد من المجموعة، حدد المورد، ثم حدد **حذف** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="e2d18-164">To remove a vendor from the group, select the vendor, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="e2d18-165">لعرض أو إضافة أو إزالة تعيينات المجموعة لمورد محدد، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="e2d18-165">To view, add, or remove group assignments for a selected vendor, follow these steps.</span></span>

1. <span data-ttu-id="e2d18-166">انتقل إلى **الحسابات الدائنة \> الموردين \> جميع الموردين**.</span><span class="sxs-lookup"><span data-stu-id="e2d18-166">Go to **Accounts payable \> Vendors \> All vendors**.</span></span>
1. <span data-ttu-id="e2d18-167">حدد المورد المراد التعامل معه.</span><span class="sxs-lookup"><span data-stu-id="e2d18-167">Select the vendor to work with.</span></span>
1. <span data-ttu-id="e2d18-168">في جزء الإجراء، في علامة التبويب **المورد**، في مجموعة **إدارة الخصومات**، حدد **مجموعات إدارة الخصومات**.</span><span class="sxs-lookup"><span data-stu-id="e2d18-168">On the Action Pane, on the **Vendor** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="e2d18-169">تظهر صفحة **مجموعة إدارة الخصومات** وتعرض قائمة المجموعات التي ينتمي إليها المورد المحدد بالفعل.</span><span class="sxs-lookup"><span data-stu-id="e2d18-169">The **Rebate management groups** page appears and shows a list of groups that the selected vendor already belongs to.</span></span>
1. <span data-ttu-id="e2d18-170">لإضافة المورد إلى مجموعة جديدة، حدد **جديد** في جزء الإجراءات لإضافة صف إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="e2d18-170">To add the vendor to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="e2d18-171">ثم قم بتعيين الحقول التالية للصف الجديد:</span><span class="sxs-lookup"><span data-stu-id="e2d18-171">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="e2d18-172">**مجموعه إدارة الخصومات** - حدد المجموعة التي سيتم أضافه المورد اليها.</span><span class="sxs-lookup"><span data-stu-id="e2d18-172">**Rebate management group** – Select the group to add the vendor to.</span></span>
    - <span data-ttu-id="e2d18-173">**الوصف** – أدخل وصفًا للمجموعة (على سبيل المثال، لشرح سبب كون المورد عضوًا فيها).</span><span class="sxs-lookup"><span data-stu-id="e2d18-173">**Description** – Enter a description of the group (for example, to explain why the vendor is a member of it).</span></span>

1. <span data-ttu-id="e2d18-174">لإزالة مورد من مجموعة، حدد المجموعة، ثم حدد **حذف** في جزء الإجراء.</span><span class="sxs-lookup"><span data-stu-id="e2d18-174">To remove a vendor from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="item-rebate-groups"></a><span data-ttu-id="e2d18-175">مجموعات الخصم للصنف</span><span class="sxs-lookup"><span data-stu-id="e2d18-175">Item rebate groups</span></span>

<span data-ttu-id="e2d18-176">من خلال تجميع الأصناف، يكون لديك المزيد من المرونة عند حساب التخفيضات والخصومات.</span><span class="sxs-lookup"><span data-stu-id="e2d18-176">By grouping items, you have more flexibility when rebates and deductions are calculated.</span></span> <span data-ttu-id="e2d18-177">غالبًا ما يكون هذا النهج طريقة أكثر فاعلية لإعداد التخفيضات والخصومات للعملاء والموردين.</span><span class="sxs-lookup"><span data-stu-id="e2d18-177">This approach is often a more efficient way to set up rebates and deductions for customers and vendors.</span></span>

### <a name="set-up-item-groups"></a><span data-ttu-id="e2d18-178">إعداد مجموعات الأصناف</span><span class="sxs-lookup"><span data-stu-id="e2d18-178">Set up item groups</span></span>

<span data-ttu-id="e2d18-179">للعمل مع مجموعات أصناف إدارة الخصم، انتقل إلى **إدارة الخصومات \> إعداد مجموعات إدارة الخصومات\> مجموعات الأصناف**.</span><span class="sxs-lookup"><span data-stu-id="e2d18-179">To work with Rebate management item groups, go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span> <span data-ttu-id="e2d18-180">يمكنك استخدام الأزرار الموجودة في جزء الإجراءات لإضافة المجموعات وإزالتها كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="e2d18-180">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="e2d18-181">بالنسبة لكل مجموعة، قم بتعيين الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="e2d18-181">For each group, set the following fields:</span></span>

- <span data-ttu-id="e2d18-182">**مجموعة إدارة الخصومات** – أدخل اسمًا فريدًا للمجموعة.</span><span class="sxs-lookup"><span data-stu-id="e2d18-182">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="e2d18-183">**الوصف** – ادخل وصفا للمجموعة لتوفير مزيد من المعلومات حول كيفيه استخدامه.</span><span class="sxs-lookup"><span data-stu-id="e2d18-183">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-item-group-assignments"></a><span data-ttu-id="e2d18-184">إدارة تعيينات مجموعات الأصناف</span><span class="sxs-lookup"><span data-stu-id="e2d18-184">Manage item group assignments</span></span>

<span data-ttu-id="e2d18-185">يمكن ان ينتمي كل صنف إلى اي عدد من مجموعات أداره الخصم.</span><span class="sxs-lookup"><span data-stu-id="e2d18-185">Each item can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="e2d18-186">لعرض أعضاء المجموعة وتعيينهم، يمكنك البدء اما من قائمه المجموعات أو من قائمه الأصناف.</span><span class="sxs-lookup"><span data-stu-id="e2d18-186">To view and assign group members, you can start from either the group list or the item list.</span></span> <span data-ttu-id="e2d18-187">يمكنك أيضا أضافه أصناف استنادا إلى التدرج الهرمي للفئات الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="e2d18-187">You can also add items based on your category hierarchy.</span></span>

<span data-ttu-id="e2d18-188">لعرض الأصناف أو إضافتها أو إزالتها لمجموعة محددة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="e2d18-188">To view, add, or remove items for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="e2d18-189">انتقل إلى **إدارة الخصومات \> إعداد مجموعات إدارة الخصومات \> مجموعات الأصناف**.</span><span class="sxs-lookup"><span data-stu-id="e2d18-189">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="e2d18-190">حدد المجموعة المطلوب إدارتها.</span><span class="sxs-lookup"><span data-stu-id="e2d18-190">Select the group to manage.</span></span>
1. <span data-ttu-id="e2d18-191">في جزء الإجراءات، حدد **الأصناف**.</span><span class="sxs-lookup"><span data-stu-id="e2d18-191">On the Action Pane, select **Items**.</span></span> <span data-ttu-id="e2d18-192">تظهر صفحة **مجموعة إدارة الخصومات** وتعرض قائمة الأصناف الأعضاء بالفعل في المجموعة المحددة.</span><span class="sxs-lookup"><span data-stu-id="e2d18-192">The **Rebate management groups** page appears and shows a list of items that are already members of the selected group.</span></span>
1. <span data-ttu-id="e2d18-193">لإضافة صنف جديدة إلى المجموعة، حدد **جديد** في جزء الإجراءات لإضافة صف إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="e2d18-193">To add a new item to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="e2d18-194">ثم قم بتعيين الحقول التالية للصف الجديد:</span><span class="sxs-lookup"><span data-stu-id="e2d18-194">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="e2d18-195">**حساب الصنف** – حدد معرف حساب الصنف.</span><span class="sxs-lookup"><span data-stu-id="e2d18-195">**Item account** – Select the item account ID.</span></span>
    - <span data-ttu-id="e2d18-196">**اسم المنتج** – أدخل اسمًا و / أو وصفًا للصنف.</span><span class="sxs-lookup"><span data-stu-id="e2d18-196">**Product name** – Enter a name and/or description of the item.</span></span>

1. <span data-ttu-id="e2d18-197">لأزاله صنف من المجموعة، حدد الصنف، ثم حدد **حذف** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="e2d18-197">To remove an item from the group, select the item, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="e2d18-198">لعرض أو إضافة أو إزالة تعيينات المجموعة لصنف محدد، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="e2d18-198">To view, add, or remove group assignments for a selected item, follow these steps.</span></span>

1. <span data-ttu-id="e2d18-199">انتقل إلى **إدارة معلومات المنتج‬ \> المنتجات \> المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="e2d18-199">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="e2d18-200">حدد الصنف المراد التعامل معه.</span><span class="sxs-lookup"><span data-stu-id="e2d18-200">Select the item to work with.</span></span>
1. <span data-ttu-id="e2d18-201">في جزء الإجراء، في علامة التبويب **المنتج**، في مجموعة **إدارة الخصومات**، حدد **مجموعات إدارة الخصومات**.</span><span class="sxs-lookup"><span data-stu-id="e2d18-201">On the Action Pane, on the **Product** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="e2d18-202">تظهر صفحة **مجموعة إدارة الخصومات** وتعرض قائمة المجموعات التي ينتمي إليها الصنف المحدد بالفعل.</span><span class="sxs-lookup"><span data-stu-id="e2d18-202">The **Rebate management groups** page appears and shows a list of groups that the selected item already belongs to.</span></span>
1. <span data-ttu-id="e2d18-203">لإضافة الصنف إلى مجموعة جديدة، حدد **جديد** في جزء الإجراءات لإضافة صف إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="e2d18-203">To add the item to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="e2d18-204">ثم قم بتعيين الحقول التالية للصف الجديد:</span><span class="sxs-lookup"><span data-stu-id="e2d18-204">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="e2d18-205">**مجموعه إدارة الخصومات** - حدد المجموعة التي سيتم أضافه الصنف اليها.</span><span class="sxs-lookup"><span data-stu-id="e2d18-205">**Rebate management group** – Select the group to add the item to.</span></span>
    - <span data-ttu-id="e2d18-206">**الوصف** – أدخل وصفًا للمجموعة (على سبيل المثال، لشرح سبب كون الصنف عضوًا فيها).</span><span class="sxs-lookup"><span data-stu-id="e2d18-206">**Description** – Enter a description of the group (for example, to explain why the item is a member of it).</span></span>

1. <span data-ttu-id="e2d18-207">لأزاله صنف من مجموعة، حدد المجموعة، ثم حدد **حذف** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="e2d18-207">To remove an item from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="e2d18-208">لإضافة أصناف إلى مجموعة بناءً على التسلسل الهرمي للفئات، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="e2d18-208">To add items to a group based on your category hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="e2d18-209">انتقل إلى **إدارة الخصومات \> إعداد مجموعات إدارة الخصومات \> مجموعات الأصناف**.</span><span class="sxs-lookup"><span data-stu-id="e2d18-209">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="e2d18-210">حدد المجموعة المطلوب إدارتها.</span><span class="sxs-lookup"><span data-stu-id="e2d18-210">Select the group to manage.</span></span>
1. <span data-ttu-id="e2d18-211">في جزء الإجراءات، حدد **إضافة أصناف**.</span><span class="sxs-lookup"><span data-stu-id="e2d18-211">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="e2d18-212">في مربع الحوار **إضافة أصناف**، في حقل **التدرج الهرمي للفئات**، حدد فئة المستوى الأعلى.</span><span class="sxs-lookup"><span data-stu-id="e2d18-212">In the **Add items** dialog box, in the **Category hierarchy** field, select a top-level category.</span></span>
1. <span data-ttu-id="e2d18-213">يتم فتح التدرج الهرمي للأصناف في الجزء الأيمن.</span><span class="sxs-lookup"><span data-stu-id="e2d18-213">The item hierarchy is opened in the left pane.</span></span> <span data-ttu-id="e2d18-214">حدد مستوي التدرج الهرمي الذي تقوم بالبحث عنه.</span><span class="sxs-lookup"><span data-stu-id="e2d18-214">Select the hierarchy level that you're looking for.</span></span> 
1. <span data-ttu-id="e2d18-215">يتم الآن ادراج أصناف من التدرج الهرمي المحدد ومستوي التدرج الهرمي في الجزء الأيسر.</span><span class="sxs-lookup"><span data-stu-id="e2d18-215">Items from the selected hierarchy and hierarchy level are now listed in the right pane.</span></span> <span data-ttu-id="e2d18-216">اتبع هذه الخطوات للعمل مع الجزء:</span><span class="sxs-lookup"><span data-stu-id="e2d18-216">Follow these steps to work with the pane:</span></span>

    - <span data-ttu-id="e2d18-217">حدد خانة الاختيار لكل صنف تريد إضافته.</span><span class="sxs-lookup"><span data-stu-id="e2d18-217">Select the check box for each item that you want to add.</span></span>
    - <span data-ttu-id="e2d18-218">حدد خانه الاختيار في راس الشبكة لتحديد كافة الأصناف المدرجة.</span><span class="sxs-lookup"><span data-stu-id="e2d18-218">Select the check box on the grid header to select all the items that are listed.</span></span>
    - <span data-ttu-id="e2d18-219">حدد الزر **إظهار المحدد** لتصفيه الشبكة بحيث تظهر فقط الأصناف التي قمت بتحديدها حتى الآن.</span><span class="sxs-lookup"><span data-stu-id="e2d18-219">Select the **Show selected** button to filter the grid so that it shows only the items that you've selected so far.</span></span> <span data-ttu-id="e2d18-220">حدد الزر مره أخرى للرجوع إلى القائمة بأكملها.</span><span class="sxs-lookup"><span data-stu-id="e2d18-220">Select the button again to return to the full list.</span></span>

1. <span data-ttu-id="e2d18-221">حدد **موافق** لتطبيق تحديد الصنف علي المجموعة المحددة.</span><span class="sxs-lookup"><span data-stu-id="e2d18-221">Select **OK** to apply your item selection to the selected group.</span></span>
