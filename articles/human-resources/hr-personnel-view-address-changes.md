---
title: عرض تغييرات العناوين وإدارتها
description: يوضح هذا الموضوع كيف يمكنك عرض تغييرات العناوين وإدارتها في Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 08/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-07
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 751e903b011b74fad584a1a22b574134610aa3d2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051751"
---
# <a name="view-and-manage-address-changes"></a><span data-ttu-id="c4c55-103">عرض تغييرات العناوين وإدارتها</span><span class="sxs-lookup"><span data-stu-id="c4c55-103">View and manage address changes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="c4c55-104">يوضح هذا الموضوع كيفية عرض تغييرات العناوين وإدارتها في صفحة **تحرير التفاصيل الشخصية** للخدمة الذاتية للموظف أو صفحة تفاصيل **العامل** في Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="c4c55-104">This topic explains how you can view and manage address changes in the Employee self-service **Edit personal details** page or the **Worker** details page in Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="c4c55-105">ترغب مؤسسات كثيرة في قيام الموظفين بإدارة بيانتهم الشخصية الخاصة من خلال تجربة الخدمة الذاتية.</span><span class="sxs-lookup"><span data-stu-id="c4c55-105">Many organizations want employees to manage their own personal details through a self-service experience.</span></span> <span data-ttu-id="c4c55-106">يمكنك السماح للمستخدمين بتحديث عنوانهم في مساحة عمل **الخدمة الذاتية للموظف‬**.</span><span class="sxs-lookup"><span data-stu-id="c4c55-106">You can allow users to update their address in the **Employee self service** workspace.</span></span> <span data-ttu-id="c4c55-107">يمكنك عندئذ مراقبة هذه التغييرات في مساحة عمل **إدارة العاملين**.</span><span class="sxs-lookup"><span data-stu-id="c4c55-107">You can then monitor these changes in the **Personnel management** workspace.</span></span> <span data-ttu-id="c4c55-108">لاستخدام هذه الميزة، يجب تحديد عدد الأيام التي ترغب في عرض التغييرات بها في الصفحة **معلمات الموارد البشرية**.</span><span class="sxs-lookup"><span data-stu-id="c4c55-108">To use this feature, you must specify the number of days that you want to view changes in the **Human resources parameters** page.</span></span>

## <a name="configure-address-change-parameters"></a><span data-ttu-id="c4c55-109">تكوين معلمات تغيير العنوان</span><span class="sxs-lookup"><span data-stu-id="c4c55-109">Configure address change parameters</span></span>

<span data-ttu-id="c4c55-110">لتكوين عدد الأيام التي تريد فيها ظهور تغييرات العناوين في مساحة عمل **إدارة العاملين**، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="c4c55-110">To configure the number of days that you want address changes to appear in the **Personnel management** workspace, follow these steps:</span></span>

1. <span data-ttu-id="c4c55-111">في جزء التنقل، حدد **إدارة العاملين**.</span><span class="sxs-lookup"><span data-stu-id="c4c55-111">On the navigation pane, select **Personnel management**.</span></span>

2. <span data-ttu-id="c4c55-112">حدد **الارتباطات**.</span><span class="sxs-lookup"><span data-stu-id="c4c55-112">Select **Links**.</span></span>

3. <span data-ttu-id="c4c55-113">حدد **معلمات الموارد البشرية**.</span><span class="sxs-lookup"><span data-stu-id="c4c55-113">Select **Human resources parameters**.</span></span>

4. <span data-ttu-id="c4c55-114">في الحقل **عدد الأيام** تحت  **تغيير العنوان**، أدخل عدد الأيام التي تريد أن تظهر فيها تغييرات العناوين في مساحة عمل **إدارة العاملين**.</span><span class="sxs-lookup"><span data-stu-id="c4c55-114">In the **Number of days** field under **Address change**, enter the number of days that you want address changes to appear in the **Personnel management** workspace.</span></span>

5. <span data-ttu-id="c4c55-115">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c4c55-115">Close the page.</span></span>

## <a name="create-or-change-an-employee-address"></a><span data-ttu-id="c4c55-116">إنشاء عنوان موظف أو تغييره</span><span class="sxs-lookup"><span data-stu-id="c4c55-116">Create or change an employee address</span></span>

<span data-ttu-id="c4c55-117">بإمكان الموظفين تحديث عناوينهم في مساحة عمل **الخدمة الذاتية للموظف‬**.</span><span class="sxs-lookup"><span data-stu-id="c4c55-117">Employees can update their own address in the **Employee self service** workspace.</span></span> <span data-ttu-id="c4c55-118">لإنشاء عنوان أو تغييره، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="c4c55-118">Follow these steps to create or change an address:</span></span>

1. <span data-ttu-id="c4c55-119">في الصفحة الرئيسية، حدد الإطار المتجانب **الخدمة الذاتية للموظف**.</span><span class="sxs-lookup"><span data-stu-id="c4c55-119">Select the **Employee self-service** tile on your home page.</span></span>

2. <span data-ttu-id="c4c55-120">حدد **تحرير التفاصيل الشخصية**.</span><span class="sxs-lookup"><span data-stu-id="c4c55-120">Select **Edit personal details**.</span></span>

3. <span data-ttu-id="c4c55-121">حدد **إضافة** لإضافة عنوان.</span><span class="sxs-lookup"><span data-stu-id="c4c55-121">To add an address, select **Add**.</span></span> <span data-ttu-id="c4c55-122">لتحديث عنوان موجود، حدد العنوان من القائمة ثم حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="c4c55-122">To update an existing address, select the address from the list and then select **Edit**.</span></span>

4. <span data-ttu-id="c4c55-123">أدخل **الاسم أو الوصف**.</span><span class="sxs-lookup"><span data-stu-id="c4c55-123">Enter the **Name or description**.</span></span>

5. <span data-ttu-id="c4c55-124">حدد مربع القائمة المنسدلة **الهدف** ثم حدد نوع العنوان.</span><span class="sxs-lookup"><span data-stu-id="c4c55-124">Select the **Purpose** drop-down box and then select the type of address.</span></span>

6. <span data-ttu-id="c4c55-125">أدخل **البلد/المنطقة**.</span><span class="sxs-lookup"><span data-stu-id="c4c55-125">Enter the **Country/region**.</span></span>

7. <span data-ttu-id="c4c55-126">أدخل **الرمز البريدي**.</span><span class="sxs-lookup"><span data-stu-id="c4c55-126">Enter the **ZIP/postal code**.</span></span>

8. <span data-ttu-id="c4c55-127">أدخل **الشارع**.</span><span class="sxs-lookup"><span data-stu-id="c4c55-127">Enter the **Street**.</span></span>

9. <span data-ttu-id="c4c55-128">أدخل **المدينة** و **الولاية** و **المقاطعة**.</span><span class="sxs-lookup"><span data-stu-id="c4c55-128">Enter the **City**, **State**, and **County**.</span></span> <span data-ttu-id="c4c55-129">يتم عادةً تعيين هذه الحقول بشكل تلقائي استنادًا إلى حقل **الرمز البريدي**.</span><span class="sxs-lookup"><span data-stu-id="c4c55-129">Typically, these fields are automatically set based on the **ZIP/postal code** field.</span></span>

10. <span data-ttu-id="c4c55-130">اختياريًا، حدد الحقل **أساسي** للإشارة إلى عنوان أساسي.</span><span class="sxs-lookup"><span data-stu-id="c4c55-130">Optionally, select the **Primary** field to indicate a primary address.</span></span> <span data-ttu-id="c4c55-131">يمكن تمييز عنوان واحد فقط كعنوان أساسي.</span><span class="sxs-lookup"><span data-stu-id="c4c55-131">Only one address can be marked as the primary.</span></span> <span data-ttu-id="c4c55-132">إذا تم تمييز عنوان آخر كعنوان أساسي، فستحتاج إلى تأكيد رغبتك في استخدام هذا العنوان كعنوان أساسي.</span><span class="sxs-lookup"><span data-stu-id="c4c55-132">If another address is already marked as the primary address, you'll need to confirm that you want to use this address as the primary.</span></span>

11. <span data-ttu-id="c4c55-133">اختياريًا، حدد الحقل **خاص** للإشارة إلى أن العنوان هو عنوان خاص.</span><span class="sxs-lookup"><span data-stu-id="c4c55-133">Optionally, select the **Private** field to indicate that the address is private.</span></span> <span data-ttu-id="c4c55-134">يمكن فقط للمستخدمين الذين يمتلكون إذنًا صريحًا بعرض معلومات العنوان الخاص عرض هذا العنوان.</span><span class="sxs-lookup"><span data-stu-id="c4c55-134">Only users with explicit permission to view private address information can view this address.</span></span>

12. <span data-ttu-id="c4c55-135">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c4c55-135">Select **OK**.</span></span>

## <a name="create-or-change-a-worker-address"></a><span data-ttu-id="c4c55-136">إنشاء عنوان العامل أو تغييره</span><span class="sxs-lookup"><span data-stu-id="c4c55-136">Create or change a worker address</span></span>

<span data-ttu-id="c4c55-137">يمكنك تحديث عنوان في مساحة عمل **إدارة العاملين**.</span><span class="sxs-lookup"><span data-stu-id="c4c55-137">You can update an address in the **Personnel management** workspace.</span></span> <span data-ttu-id="c4c55-138">لإنشاء عنوان أو تغييره، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="c4c55-138">Follow these steps to create or change an address:</span></span>

1. <span data-ttu-id="c4c55-139">في مساحة عمل **إدارة العاملين**، حدد **ارتباطات**، ثم حدد **العاملون**.</span><span class="sxs-lookup"><span data-stu-id="c4c55-139">In the **Personnel management** workspace, select **Links**, and then select **Workers**.</span></span>

3. <span data-ttu-id="c4c55-140">حدد العامل، ثم حدد **العناوين**.</span><span class="sxs-lookup"><span data-stu-id="c4c55-140">Select the worker, and then select **Addresses**.</span></span>

3. <span data-ttu-id="c4c55-141">حدد **إضافة** لإضافة عنوان.</span><span class="sxs-lookup"><span data-stu-id="c4c55-141">To add an address, select **Add**.</span></span> <span data-ttu-id="c4c55-142">لتحديث عنوان موجود، حدد العنوان من القائمة ثم حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="c4c55-142">To update an existing address, select the address from the list and then select **Edit**.</span></span>

4. <span data-ttu-id="c4c55-143">أدخل **الاسم أو الوصف**.</span><span class="sxs-lookup"><span data-stu-id="c4c55-143">Enter the **Name or description**.</span></span>

5. <span data-ttu-id="c4c55-144">حدد مربع القائمة المنسدلة **الهدف** ثم حدد نوع العنوان.</span><span class="sxs-lookup"><span data-stu-id="c4c55-144">Select the **Purpose** drop-down box and then select the type of address.</span></span>

6. <span data-ttu-id="c4c55-145">أدخل **البلد/المنطقة**.</span><span class="sxs-lookup"><span data-stu-id="c4c55-145">Enter the **Country/region**.</span></span>

7. <span data-ttu-id="c4c55-146">أدخل **الرمز البريدي**.</span><span class="sxs-lookup"><span data-stu-id="c4c55-146">Enter the **ZIP/postal code**.</span></span>

8. <span data-ttu-id="c4c55-147">أدخل **الشارع**.</span><span class="sxs-lookup"><span data-stu-id="c4c55-147">Enter the **Street**.</span></span>

9. <span data-ttu-id="c4c55-148">أدخل **المدينة** و **الولاية** و **المقاطعة**.</span><span class="sxs-lookup"><span data-stu-id="c4c55-148">Enter the **City**, **State**, and **County**.</span></span> <span data-ttu-id="c4c55-149">يتم عادةً تعيين هذه الحقول بشكل تلقائي استنادًا إلى حقل **الرمز البريدي**.</span><span class="sxs-lookup"><span data-stu-id="c4c55-149">Typically, these fields are automatically set based on the **ZIP/postal code** field.</span></span>

10. <span data-ttu-id="c4c55-150">اختياريًا، حدد الحقل **أساسي** للإشارة إلى عنوان أساسي.</span><span class="sxs-lookup"><span data-stu-id="c4c55-150">Optionally, select the **Primary** field to indicate a primary address.</span></span> <span data-ttu-id="c4c55-151">يمكن تمييز عنوان واحد فقط كعنوان أساسي.</span><span class="sxs-lookup"><span data-stu-id="c4c55-151">Only one address can be marked as the primary.</span></span> <span data-ttu-id="c4c55-152">إذا تم تمييز عنوان آخر كعنوان أساسي، فستحتاج إلى تأكيد رغبتك في استخدام هذا العنوان كعنوان أساسي.</span><span class="sxs-lookup"><span data-stu-id="c4c55-152">If another address is already marked as the primary address, you'll need to confirm that you want to use this address as the primary.</span></span>

11. <span data-ttu-id="c4c55-153">اختياريًا، حدد الحقل **خاص** للإشارة إلى أن العنوان هو عنوان خاص.</span><span class="sxs-lookup"><span data-stu-id="c4c55-153">Optionally, select the **Private** field to indicate that the address is private.</span></span> <span data-ttu-id="c4c55-154">يمكن فقط للمستخدمين الذين يمتلكون إذنًا صريحًا بعرض معلومات العنوان الخاص عرض هذا العنوان.</span><span class="sxs-lookup"><span data-stu-id="c4c55-154">Only users with explicit permission to view private address information can view this address.</span></span>

12. <span data-ttu-id="c4c55-155">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c4c55-155">Select **OK**.</span></span>
 
## <a name="create-a-future-change-for-an-address"></a><span data-ttu-id="c4c55-156">إنشاء تغيير مستقبلي لعنوان</span><span class="sxs-lookup"><span data-stu-id="c4c55-156">Create a future change for an address</span></span>

<span data-ttu-id="c4c55-157">في بعض الحالات، قد تحتاج إلى تحديث عنوان لتغييره في المستقبل.</span><span class="sxs-lookup"><span data-stu-id="c4c55-157">In some cases, you might want to update an address to change in the future.</span></span> <span data-ttu-id="c4c55-158">على سبيل المثال، قد يكون هذا مفيدًا إذا كان سيتم نقل الموظف في اليوم 15 من الشهر التالي.</span><span class="sxs-lookup"><span data-stu-id="c4c55-158">For example, this would be useful if an employee is moving on the 15th of the following month.</span></span>

1. <span data-ttu-id="c4c55-159">افتح الصفحة **إدارة العناوين** عن طريق تحديد **مزيد من الخيارات > خيارات متقدمة** من أي شبكة عناوين.</span><span class="sxs-lookup"><span data-stu-id="c4c55-159">Open the **Manage addresses** page by selecting **More options > Advanced** from any address grid.</span></span>

2. <span data-ttu-id="c4c55-160">حدد **جديد** لإنشاء عنوان جديد.</span><span class="sxs-lookup"><span data-stu-id="c4c55-160">Select **New** to create a new address.</span></span>

3. <span data-ttu-id="c4c55-161">أدخل تفاصيل العنوان.</span><span class="sxs-lookup"><span data-stu-id="c4c55-161">Enter the details of the address.</span></span>

4. <span data-ttu-id="c4c55-162">حدد علامة التبويب السريعة **عام**.</span><span class="sxs-lookup"><span data-stu-id="c4c55-162">Select the **General** FastTab.</span></span>

5. <span data-ttu-id="c4c55-163">في الحقل **تاريخ السريان**، حدد تاريخ سريان العنوان الجديد.</span><span class="sxs-lookup"><span data-stu-id="c4c55-163">In the **Effective date** field, select the date the new address will be effective.</span></span>

6. <span data-ttu-id="c4c55-164">في الحقل **تاريخ انتهاء الصلاحية**، حدد التاريخ الذي سيتوقف فيه سريان العنوان.</span><span class="sxs-lookup"><span data-stu-id="c4c55-164">In the **Expiration date** field, optionally select when the address will no longer be effective.</span></span>

7. <span data-ttu-id="c4c55-165">قم بإغلاق الصفحات.</span><span class="sxs-lookup"><span data-stu-id="c4c55-165">Close the pages.</span></span>

## <a name="view-and-monitor-address-changes"></a><span data-ttu-id="c4c55-166">عرض تغييرات العناوين ومراقبتها</span><span class="sxs-lookup"><span data-stu-id="c4c55-166">View and monitor address changes</span></span>

<span data-ttu-id="c4c55-167">بإمكان العاملين في الموارد البشرية عرض تغييرات العناوين ومراقبتها من مساحة عمل **إدارة العاملين**.</span><span class="sxs-lookup"><span data-stu-id="c4c55-167">HR personnel can view and monitor address changes from the **Personnel management** workspace.</span></span> <span data-ttu-id="c4c55-168">لعرض تغييرات العناوين، افتح الإطار المتجانب **إدارة العاملين** من **الصفحة الرئيسية**.</span><span class="sxs-lookup"><span data-stu-id="c4c55-168">To view the address changes, open the **Personnel management** tile from the **Home** page.</span></span> <span data-ttu-id="c4c55-169">تظهر تغييرات العنوان على تجانب في الزاوية العلوية اليمني.</span><span class="sxs-lookup"><span data-stu-id="c4c55-169">The address changes display on a tile in the upper-right corner.</span></span> <span data-ttu-id="c4c55-170">يعرض الرقم الموجود فوق **تغييرات العناوين** عدد التغييرات في العناوين التي حدثت في عدد الأيام المحدد في صفحة **معلمات الموارد البشرية**.</span><span class="sxs-lookup"><span data-stu-id="c4c55-170">The number above **Address changes** shows how many address changes occurred in the number of days specified in the **Human resources parameters** page.</span></span> 

<span data-ttu-id="c4c55-171">عند تحديد تجانب **تغييرات العناوين**، تعرض صفحة جديدة تفاصيل أي تغييرات في العناوين.</span><span class="sxs-lookup"><span data-stu-id="c4c55-171">When you select the **Address changes** tile, a new page displays the details of any address changes.</span></span> <span data-ttu-id="c4c55-172">يمكنك بشكل اختياري تحديد **تضمين تغييرات العناوين المستقبلية** في الزاوية العلوية اليمني لعرض تغييرات العناوين مع تاريخ في المستقبل.</span><span class="sxs-lookup"><span data-stu-id="c4c55-172">You can optionally select **Include future address changes** in the upper-right corner to display address changes with a future date.</span></span>

> [!NOTE]
> <span data-ttu-id="c4c55-173">إذا كنت ترغب في تلقي تنبيه أو بريد إلكتروني حول تغييرات العناوين هذه، فيمكنك إنشاء قاعدة تنبيه جديدة في علامة التبويب **خيارات** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="c4c55-173">If you want to receive an alert or email about these address changes, you can create a new alert rule on the **Options** tab in the Action Pane.</span></span> <span data-ttu-id="c4c55-174">لمزيد من المعلومات حول قواعد التنبيه، راجع [إنشاء قواعد تنبيه](../fin-ops-core/fin-ops/get-started/create-alerts.md).</span><span class="sxs-lookup"><span data-stu-id="c4c55-174">For more information about alert rules, see [Create alert rules](../fin-ops-core/fin-ops/get-started/create-alerts.md).</span></span><br><br>

> <span data-ttu-id="c4c55-175">إذا كنت ترغب في تكوين سير عمل لتغييرات العناوين، فيمكنك تحديد الخيار **الإرسال خارجيًا‬‏‫** على قاعدة التنبيه، ثم استخدام Power Automate لتشغيل حدث الأعمال وتكوين سير عمل.</span><span class="sxs-lookup"><span data-stu-id="c4c55-175">If you want to configure a workflow for the address changes, you can select the **Send externally** option on your alert rule, and then use Power Automate to trigger the business event and configure a workflow.</span></span> <span data-ttu-id="c4c55-176">لمزيد من المعلومات، راجع [التنبيهات كأحداث أعمال](../fin-ops-core/fin-ops/get-started/create-alerts.md#alerts-as-business-events).</span><span class="sxs-lookup"><span data-stu-id="c4c55-176">For more information, see [Alerts as business events](../fin-ops-core/fin-ops/get-started/create-alerts.md#alerts-as-business-events).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]