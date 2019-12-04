---
title: الجرد الدوري
description: تصف هذه المقالة كيفية استخدام الجرد الدوري مع حل التخزين المتوفر في إدارة المستودعات. لا تنطبق هذه المقالة على حل التخزين المتوفر في إدارة المخزون.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSCycleCountThreshold, WHSWorkTableListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 50671
ms.assetid: 49f5c431-b043-4170-aa24-b7d5d1ee063e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d7ec95b230c5ea17f208bc1288c10fce15631a5d
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813042"
---
# <a name="cycle-counting"></a><span data-ttu-id="d9694-104">الجرد الدوري</span><span class="sxs-lookup"><span data-stu-id="d9694-104">Cycle counting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d9694-105">تصف هذه المقالة كيفية استخدام الجرد الدوري مع حل التخزين المتوفر في إدارة المستودعات.</span><span class="sxs-lookup"><span data-stu-id="d9694-105">This article describes how you can use cycle counting with the warehousing solution that is available in Warehouse management.</span></span> <span data-ttu-id="d9694-106">لا تنطبق هذه المقالة على حل التخزين المتوفر في إدارة المخزون.</span><span class="sxs-lookup"><span data-stu-id="d9694-106">This article doesn't apply to the warehousing solution that's available in Inventory management.</span></span>

<span data-ttu-id="d9694-107">الجرد الدوري هو معالجة المستودع التي يمكنك استخدامها للتدقيق في أصناف المخزون الفعلي.</span><span class="sxs-lookup"><span data-stu-id="d9694-107">Cycle counting is a warehouse process that you can use to audit on-hand inventory items.</span></span> <span data-ttu-id="d9694-108">يمكن وصف عملية الجرد الدوري في ثلاث خطوات:</span><span class="sxs-lookup"><span data-stu-id="d9694-108">The cycle counting process can be described in three steps:</span></span>

1.  <span data-ttu-id="d9694-109">**إنشاء عمل الجرد الدوري** – يمكن إنشاء عمل الجرد الدوري تلقائيًا استنادًا إلى محددات الحد المسموح للأصناف أو باستخدام خطة جرد دوري.</span><span class="sxs-lookup"><span data-stu-id="d9694-109">**Create cycle counting work** – Cycle counting work can be created automatically, based on threshold parameters for items or by using a cycle counting plan.</span></span> <span data-ttu-id="d9694-110">أو، يمكنك إنشاء عمل الجرد الدوري يدويًا باستخدام محددات المستودع أو الصنف في صفحة **عمل الجرد الدوري حسب الصنف** أو صفحة **عمل الجرد الدوري حسب الموقع**.</span><span class="sxs-lookup"><span data-stu-id="d9694-110">Alternatively, you can manually create cycle counting work by using the item or warehouse parameters on the **Cycle count work by item** page or the **Cycle count work by location** page.</span></span>
2.  <span data-ttu-id="d9694-111">**معالجة الجرد الدوري** – بعد إنشاء عمل الجرد الدوري، ستقوم بتنفيذه بجرد الأصناف في موقع المستودع، ثم استخدام جهاز محمول لإدخال النتيجة في Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d9694-111">**Process the cycle count** – After cycle counting work is created, you do the cycle counting work by counting items in a warehouse location and then using a mobile device to enter the result in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="d9694-112">بدلاً من ذلك، يمكنك حساب الأصناف في موقع مستودع دون إنشاء دورة جرد للعمل.</span><span class="sxs-lookup"><span data-stu-id="d9694-112">Alternatively, you can count items in a warehouse location without creating cycle counting work.</span></span> <span data-ttu-id="d9694-113">يشار إلى هذه العملية  ب*نقطة الجرد الدوري*.</span><span class="sxs-lookup"><span data-stu-id="d9694-113">This process is referred to as *spot cycle counting*.</span></span>
3.  <span data-ttu-id="d9694-114">**حل الفروقات في قيمة الجرد** – بعد الجرد الدوري، ستكون الأصناف التي تتضمن فروقات في قيمة الجرد بحالة العمل **مراجعة معلقة‬** في صفحة **العمل بالكامل‬**.</span><span class="sxs-lookup"><span data-stu-id="d9694-114">**Resolve differences in the counted value** – After a cycle count, any items that have differences in the counted value will have a work status of **Pending review** on the **All work** page.</span></span> <span data-ttu-id="d9694-115">يمكنك حل هذه الفروقات في صفحة **عمل الجرد الدوري قيد انتظار المراجعة‬**.</span><span class="sxs-lookup"><span data-stu-id="d9694-115">You can resolve these differences on the **Cycle count work pending review** page.</span></span>

<span data-ttu-id="d9694-116">يبين الرسم التوضيحي التالي عملية الجرد الدوري.</span><span class="sxs-lookup"><span data-stu-id="d9694-116">The following illustration shows the cycle counting process.</span></span> ![معالجة التدفق للجرد الدوري](./media/performcyclecountinginawarehouselocation.jpg)

## <a name="cycle-counting-prerequisites"></a><span data-ttu-id="d9694-118">متطلبات الجرد الدوري الأساسية</span><span class="sxs-lookup"><span data-stu-id="d9694-118">Cycle counting prerequisites</span></span>
<span data-ttu-id="d9694-119">يعرض الجدول التالي المتطلبات الأساسية التي يجب أن تكون موجودة قبل أن تتمكن من استخدام الجرد الدوري.</span><span class="sxs-lookup"><span data-stu-id="d9694-119">The following table shows the prerequisites that must be in place before you can use cycle counting.</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d9694-120">المتطلب الأساسي</span><span class="sxs-lookup"><span data-stu-id="d9694-120">Prerequisite</span></span></th>
<th><span data-ttu-id="d9694-121">الوصف</span><span class="sxs-lookup"><span data-stu-id="d9694-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d9694-122">صنف</span><span class="sxs-lookup"><span data-stu-id="d9694-122">Item</span></span></td>
<td><span data-ttu-id="d9694-123">يجب أن يكون الصنف متاحًا لعمليات إدارة المستودعات.</span><span class="sxs-lookup"><span data-stu-id="d9694-123">The item must be enabled for warehouse management processes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9694-124">المستودع</span><span class="sxs-lookup"><span data-stu-id="d9694-124">Warehouse</span></span></td>
<td><span data-ttu-id="d9694-125">يجب أن يكون المستودع متاحًا لعمليات إدارة المستودعات.</span><span class="sxs-lookup"><span data-stu-id="d9694-125">The warehouse must be enabled for warehouse management processes.</span></span> <span data-ttu-id="d9694-126">لتمكين المستودع لعمليات إدارة المستودع، في صفحة <strong>المستودعات</strong> حدد المستودع، ثم حدد الخيار <strong>استخدام عمليات إدارة المستودعات‬</strong>.</span><span class="sxs-lookup"><span data-stu-id="d9694-126">To enable the warehouse for warehouse management processes, on the <strong>Warehouses</strong> page, select the warehouse, and then select the <strong>Use warehouse management processes</strong> option.</span></span> <span data-ttu-id="d9694-127">لتمكين العاملين من نقل البالتات أثناء عملية جرد دوري، على علامة التبويب السريعة <strong>إدارة المستودعات‬</strong>، حدد الخيار <strong>السماح بتحركات البالتة أثناء الجرد الدوري‬</strong>.</span><span class="sxs-lookup"><span data-stu-id="d9694-127">To enable workers to move pallets during a cycle count, on the <strong>Warehouse management</strong> FastTab, select the <strong>Allow pallet moves during cycle counting</strong> option.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9694-128">أوعية العمل</span><span class="sxs-lookup"><span data-stu-id="d9694-128">Work pools</span></span></td>
<td><span data-ttu-id="d9694-129">اختياري: يمكنك إنشاء وعاء عمل لفصل عمل المستودع، استنادًا إلى نوع العمل (في هذه الحالة، عمل الجرد الدوري).</span><span class="sxs-lookup"><span data-stu-id="d9694-129">Optional: Create a work pool to segregate the warehouse work, based on the type of work (in this case, cycle counting work).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9694-130">المواقع</span><span class="sxs-lookup"><span data-stu-id="d9694-130">Locations</span></span></td>
<td><span data-ttu-id="d9694-131">تمكين الجرد الدوري للمواقع.</span><span class="sxs-lookup"><span data-stu-id="d9694-131">Enable cycle counting for locations.</span></span> <span data-ttu-id="d9694-132">لتمكين الجرد الدوري لموقع المستودع، في صفحة <strong>ملفات تعريف الموقع‬</strong>، حدد الخيار <strong>السماح بالجرد الدوري‬</strong>.</span><span class="sxs-lookup"><span data-stu-id="d9694-132">To enable cycle counting for a warehouse location, on the <strong>Location profiles</strong> page, select the <strong>Allow cycle counting</strong> option.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9694-133">محددات إدارة المستودعات</span><span class="sxs-lookup"><span data-stu-id="d9694-133">Warehouse management parameters</span></span></td>
<td><span data-ttu-id="d9694-134">إعداد محددات الجرد الدوري</span><span class="sxs-lookup"><span data-stu-id="d9694-134">Set up parameters for cycle counting.</span></span> <span data-ttu-id="d9694-135">في صفحة <strong>محددات إدارة المستودعات‬</strong>، حدد رمز نوع التسوية الافتراضي ومعرف فئة العمل وأولوية العمل للجرد الدوري.</span><span class="sxs-lookup"><span data-stu-id="d9694-135">On the <strong>Warehouse management parameters</strong> page, specify the default adjustment type code, work class ID, and work priority for cycle counting.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9694-136">جهاز محمول</span><span class="sxs-lookup"><span data-stu-id="d9694-136">Mobile device</span></span></td>
<td><ul>
<li><span data-ttu-id="d9694-137">أنشئ عناصر قائمة لأحد الطرق التالية في صفحة <strong>عناصر قائمة الجهاز المحمول</strong>:</span><span class="sxs-lookup"><span data-stu-id="d9694-137">Create a menu item for one of the following methods on the <strong>Mobile device menu items</strong> page:</span></span>
<ul>
<li><span data-ttu-id="d9694-138">الجرد الدوري الموجه من قبل المستخدم</span><span class="sxs-lookup"><span data-stu-id="d9694-138">User directed cycle counting</span></span></li>
<li><span data-ttu-id="d9694-139">الجرد الدوري الموجه من قبل النظام</span><span class="sxs-lookup"><span data-stu-id="d9694-139">System directed cycle counting</span></span></li>
<li><span data-ttu-id="d9694-140">تجميع الجرد الدوري</span><span class="sxs-lookup"><span data-stu-id="d9694-140">Cycle count grouping</span></span></li>
<li><span data-ttu-id="d9694-141">الجرد الدوري الفوري</span><span class="sxs-lookup"><span data-stu-id="d9694-141">Spot cycle counting</span></span></li>
</ul>
</li>
<li><span data-ttu-id="d9694-142">قم بإعداد قائمة للجهاز المحمول.</span><span class="sxs-lookup"><span data-stu-id="d9694-142">Set up a menu for the mobile device.</span></span></li>
<li><span data-ttu-id="d9694-143">أنشئ حساب مستخدم عمل وعيّن قائمة الجهاز المحمول إلى معرف مستخدم العمل.</span><span class="sxs-lookup"><span data-stu-id="d9694-143">Create a work user account, and assign a mobile device menu to the work user ID.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9694-144">مهمة الإعداد المرتبطة</span><span class="sxs-lookup"><span data-stu-id="d9694-144">Related setup task</span></span></td>
<td><span data-ttu-id="d9694-145">إعداد خطة جرد دوري لموقع مستودع.</span><span class="sxs-lookup"><span data-stu-id="d9694-145">Set up a cycle counting plan for a warehouse location.</span></span></td>
</tr>
</tbody>
</table>

## <a name="automatically-create-cycle-counting-work"></a><span data-ttu-id="d9694-146">إنشاء عمل جرد دوري تلقائيًا</span><span class="sxs-lookup"><span data-stu-id="d9694-146">Automatically create cycle counting work</span></span>
<span data-ttu-id="d9694-147">هناك طريقتان لجدولة الإنشاء المتكرر لعمل الجرد الدوري: إعداد حدود الجرد الدوري أو إعداد خطط الجرد الدوري.</span><span class="sxs-lookup"><span data-stu-id="d9694-147">There are two ways to schedule recurring creation of cycle counting work: set up cycle counting thresholds or set up cycle counting plans.</span></span>

-   <span data-ttu-id="d9694-148">يشير حد الجرد الدوري لحد النسبة المئوية أو كمية أصناف المخزون.</span><span class="sxs-lookup"><span data-stu-id="d9694-148">A cycle counting threshold indicates the quantity or percentage limit of inventory items.</span></span> <span data-ttu-id="d9694-149">يتم إنشاء عمل جرد دوري تلقائيًا عند الوصول إلى الحد.</span><span class="sxs-lookup"><span data-stu-id="d9694-149">Cycle counting work is automatically created when the threshold limit is reached.</span></span>
-   <span data-ttu-id="d9694-150">تنشئ خطة الجرد الدوري عمل الجرد الدوري إما على الفور أو عبر وظيفة دفعية.</span><span class="sxs-lookup"><span data-stu-id="d9694-150">A cycle counting plan creates cycle counting work either immediately or periodically through a batch job.</span></span> <span data-ttu-id="d9694-151">يحتوي بند عمل الجرد، عند إنشاء عمل الجرد الدوري، على معلومات حول الموقع الذي سيتم جرده.</span><span class="sxs-lookup"><span data-stu-id="d9694-151">When cycle counting work is created, the counting work line includes information about the location to count.</span></span> <span data-ttu-id="d9694-152">لن يكون المخزون الفعلي المقترن بهذا الموقع محظورًا، وبالتالي سيكون متوفرًا للحجز والمعالجة الصادرة على الرغم من وجود عمل جرد مفتوح.</span><span class="sxs-lookup"><span data-stu-id="d9694-152">The on-hand inventory that is associated with this location isn't blocked, and is therefore available for reservation and outbound processing, even though open counting work exists.</span></span>

### <a name="create-cycle-counting-work-based-on-threshold-parameters-for-items"></a><span data-ttu-id="d9694-153">إنشاء عمل جرد دوري استنادًا إلى محددات الحد المسموح للأصناف</span><span class="sxs-lookup"><span data-stu-id="d9694-153">Create cycle counting work, based on threshold parameters for items</span></span>

<span data-ttu-id="d9694-154">يمكن إنشاء عمل الجرد الدوري عندما يكون عدد الأصناف أقل من قيمة حد مسموح معين في موقع ما.</span><span class="sxs-lookup"><span data-stu-id="d9694-154">Cycle counting work can be created when the number of items falls below a specific threshold value in a location.</span></span> <span data-ttu-id="d9694-155">‏‫على سبيل المثال، هناك 60 صنفًا في موقع حيث الحد المسموح للجرد الدوري هو 40.</span><span class="sxs-lookup"><span data-stu-id="d9694-155">For example, there are 60 items in a location that has a cycle counting threshold of 40.</span></span> <span data-ttu-id="d9694-156">أثناء حركة أمر مبيعات، يتم انتقاء 25 صنفًا من الموقع ويتم وضعها في موقع مرحلي.‬</span><span class="sxs-lookup"><span data-stu-id="d9694-156">During a sales order transaction, 25 items are picked from the location and put in a staging location.</span></span> <span data-ttu-id="d9694-157">وبما أن عدد الأصناف الجديدة، وهو 35، أقل من كمية الحد المسموح، يتم إنشاء عمل الجرد الدوري تلقائيًا للموقع.</span><span class="sxs-lookup"><span data-stu-id="d9694-157">Because the new item count, 35, is less than the threshold quantity, cycle counting work is automatically created for the location.</span></span>

### <a name="schedule-cycle-counting-work"></a><span data-ttu-id="d9694-158">جدولة الجرد الدوري للعمل</span><span class="sxs-lookup"><span data-stu-id="d9694-158">Schedule cycle counting work</span></span>

<span data-ttu-id="d9694-159">يمكنك جدولة خطة الجرد الدوري لإنشاء عمل الجرد الدوري فورًا أو بشكل دوري.</span><span class="sxs-lookup"><span data-stu-id="d9694-159">You can schedule cycle counting plans to create cycle counting work immediately or periodically.</span></span> <span data-ttu-id="d9694-160">من خلال إعداد خطط الجرد الدوري، يمكنك التحكم في وعاء العمل الذي تم إنشاء عمل الجرد الدوري له والحد الأقصى لعدد عمليات الجرد الدوري التي تم إنشاؤها للأصناف الموجودة في مواقع مختلفة وعدد الأيام قبل أن يتم جرد موقع المستودع مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="d9694-160">By setting up cycle counting plans, you can control the work pool that cycle counting work is created for, the maximum number of cycle counts that are created for items in different locations, and the number of days before a warehouse location is counted again.</span></span> <span data-ttu-id="d9694-161">على سبيل المثال، يتوفر أحد الأصناف في ثلاثة مواقع في المستودع، ويتم تعيين الحد الأقصى لعدد عمليات الجرد الدوري إلى **2**.</span><span class="sxs-lookup"><span data-stu-id="d9694-161">For example, an item is available in three locations in the warehouse, and the maximum number of cycle counts is set to **2**.</span></span> <span data-ttu-id="d9694-162">في هذه الحالة، عندما تقوم بتشغيل خطة الجرد الدوري، سيتم بإنشاء عمليتي جرد دوري للموقعين حيث يوجد الصنف.</span><span class="sxs-lookup"><span data-stu-id="d9694-162">In this case, when you run the cycle counting plan, two cycle counts are created for the two locations where the item is present.</span></span> <span data-ttu-id="d9694-163">وكمثال آخر، يمكنك تعيين عدد الأيام بين عمليات الجرد الدوري إلى **5**.</span><span class="sxs-lookup"><span data-stu-id="d9694-163">As another example, you set the number of days between cycle counts to **5**.</span></span> <span data-ttu-id="d9694-164">في هذه الحالة، يتم إنشاء عمل جرد دوري كل خمسة أيام.</span><span class="sxs-lookup"><span data-stu-id="d9694-164">In this case, cycle counting work is created every five days.</span></span> <span data-ttu-id="d9694-165">ومع ذلك، إذا تمت معالجة عمل الجرد الدوري في اليوم الثالث، فسيتم إنشاء عمل الجرد الدوري التالي بعد مرور خمسة أيام على معالجة آخر جرد دوري، في اليوم الثامن.</span><span class="sxs-lookup"><span data-stu-id="d9694-165">However, if cycle counting work is processed on day 3, the next cycle counting work will be created five days after the last cycle counting was processed, on day 8.</span></span>

## <a name="create-cycle-counting-work-manually"></a><span data-ttu-id="d9694-166">إنشاء جرد دوري للعمل يدويًا</span><span class="sxs-lookup"><span data-stu-id="d9694-166">Create cycle counting work manually</span></span>
<span data-ttu-id="d9694-167">لإنشاء عمل الجرد الدوري يدويًا، يمكنك استخدام صفحة **عمل الجرد الدوري حسب الصنف‬** أو **عمل الجرد الدوري حسب الموقع**.</span><span class="sxs-lookup"><span data-stu-id="d9694-167">To create cycle counting work manually, you can use the **Cycle count work by item** or **Cycle count work by location** page.</span></span> <span data-ttu-id="d9694-168">يمكنك تعيين الحدد الأقصى لعدد عمليات الجرد الدوري المطلوب إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="d9694-168">You can specify the maximum number of cycle counts to create.</span></span> <span data-ttu-id="d9694-169">على سبيل المثال، إذا عيّن مدير المستودع قيمة من **5**، فسيتم إنشاء عمل جرد دوري لخمسة مواقع، حتى لو كان الصنف موجودًا في 10 مواقع.</span><span class="sxs-lookup"><span data-stu-id="d9694-169">For example, if the warehouse manager specifies a value of **5**, cycle counting work is created for five locations, even if the item is present in 10 locations.</span></span> <span data-ttu-id="d9694-170">يمكنك أيضًا تحديد معرف وعاء عمل لتعيين معرفات عمل الجرد الدوري التي تم إنشاؤها له.</span><span class="sxs-lookup"><span data-stu-id="d9694-170">You can also select a work pool ID to assign the cycle counting work IDs that are created to.</span></span> <span data-ttu-id="d9694-171">عندما تتم معالجة معرف وعاء عمل للجرد الدوري، ستتم معالجة معرفات عمل الجرد الدوري المعينة إلى وعاء العمل كمجموعة.</span><span class="sxs-lookup"><span data-stu-id="d9694-171">When a work pool ID is processed for cycle counting, the cycle counting work IDs that are assigned to the work pool are processed as a group.</span></span>

## <a name="perform-a-cycle-count-by-using-a-mobile-device"></a><span data-ttu-id="d9694-172">إجراء عملية جرد دوري باستخدام جهاز محمول</span><span class="sxs-lookup"><span data-stu-id="d9694-172">Perform a cycle count by using a mobile device</span></span>
<span data-ttu-id="d9694-173">هناك عدة طرق لمعالجة عمل الجرد الدوري باستخدام Supply Chain Management على جهاز محمول:</span><span class="sxs-lookup"><span data-stu-id="d9694-173">There are several methods for processing cycle counting work by using Supply Chain Management on a mobile device:</span></span>

-   <span data-ttu-id="d9694-174">**موجه من قبل المستخدم** – بإمكان العام تحديد معرف عمل الجرد الدوري حالته **مفتوح**.</span><span class="sxs-lookup"><span data-stu-id="d9694-174">**User directed** – The worker can specify a cycle counting work ID that has a status of **Open**.</span></span>
-   <span data-ttu-id="d9694-175">**موجه من قبل النظام** – يعيّن Supply Chain Management معرف عمل جرد دوري إلى العامل.</span><span class="sxs-lookup"><span data-stu-id="d9694-175">**System directed** – Supply Chain Management assigns a cycle counting work ID to the worker.</span></span>
-   <span data-ttu-id="d9694-176">**تجميع الجرد الدوري** – بإمكان العامل تجميع معرفات عمل الجرد الدوري الخاصة بموقع أو منطقة أو وعاء عمل محدد.</span><span class="sxs-lookup"><span data-stu-id="d9694-176">**Cycle count grouping** – The worker can group cycle counting work IDs that are specific to a particular location, zone, or work pool.</span></span>
-   <span data-ttu-id="d9694-177">**الجرد الدوري الفوري‬** – بإمكان العامل جرد الأصناف في موقع مستودع في أي وقت، من دون إنشاء عمل جرد دوري.</span><span class="sxs-lookup"><span data-stu-id="d9694-177">**Spot cycle counting** – The worker can count items in a warehouse location at any time, without creating cycle counting work.</span></span> <span data-ttu-id="d9694-178">لتنفيذ الجرد الدوري الفوري‬ في موقع، يقوم العامل بإدخال معرف الموقع.</span><span class="sxs-lookup"><span data-stu-id="d9694-178">To perform spot cycle counting in a location, the worker enters the location ID.</span></span>

<span data-ttu-id="d9694-179">يُظهر المثال التالي كيفية تنفيذ جرد دوري فوري باستخدام جهاز محمول.</span><span class="sxs-lookup"><span data-stu-id="d9694-179">The following example shows how you can perform spot cycle counting by using a mobile device.</span></span> <span data-ttu-id="d9694-180">تختلف التعليمات التي يراها العامل على الجهاز، وفقًا لإعداد عنصر القائمة لعملية الجرد الدوري الفوري.</span><span class="sxs-lookup"><span data-stu-id="d9694-180">The instructions that the worker sees on the device vary, depending on the setup of the menu item for spot cycle counting.</span></span>

1.  <span data-ttu-id="d9694-181">على جهاز محمول، حدد قائمة الأصناف لمعالجة نقطة جرد دوري للعمل.</span><span class="sxs-lookup"><span data-stu-id="d9694-181">On the mobile device, select the menu item to process spot cycle counting work.</span></span>
2.  <span data-ttu-id="d9694-182">سجّل الموقع الذي تريد إجراء جرد دوري فوري له.</span><span class="sxs-lookup"><span data-stu-id="d9694-182">Register the location to perform spot cycle counting for.</span></span>
3.  <span data-ttu-id="d9694-183">سجّل وأكد رقم الصنف وكمية الصنف التي تم جردها.</span><span class="sxs-lookup"><span data-stu-id="d9694-183">Register and confirm the item number and the counted item quantity.</span></span> <span data-ttu-id="d9694-184">**ملاحظة:** يتم تحديث عمل الجرد الدوري إما إلى **مراجعة معلقة‬** أو **مغلق** في صفحة **العمل بالكامل**، بحسب المحددات التي تم تعيينها في صفحة **العامل**.</span><span class="sxs-lookup"><span data-stu-id="d9694-184">**Note:** The status of the cycle counting work is updated to either **Pending review** or **Closed** on the **All work** page, depending on the parameters that are set on the **Worker** page.</span></span>
4.  <span data-ttu-id="d9694-185">اختياري: كرر الخطوة 3 للأصناف المتبقية في الموقع، وتأكد من عدم وجود أي أصناف إضافية متوفرة للجرد.</span><span class="sxs-lookup"><span data-stu-id="d9694-185">Optional: Repeat step 3 for the remaining items in the location, and confirm that no additional items are available for counting.</span></span>

## <a name="resolve-cycle-counting-differences"></a><span data-ttu-id="d9694-186">حل فروقات الجرد الدوري</span><span class="sxs-lookup"><span data-stu-id="d9694-186">Resolve cycle counting differences</span></span>
<span data-ttu-id="d9694-187">يحدث الفرق في الجرد الدوري في السيناريوهات التالية إذا تم تعيين الخيار **عبارة عن مشرف على الجرد الدوري** إلى **لا** لمعرف مستخدم العمل:</span><span class="sxs-lookup"><span data-stu-id="d9694-187">A cycle counting difference occurs in the following scenarios if the **Is a cycle count supervisor** option is set to **No** for a work user ID:</span></span>

-   <span data-ttu-id="d9694-188">لا تقع قيمة الجرد ضمن حدود الانحراف المحددة في حقل **أقصى حد للنسبة المئوية‬** أو **أقصى حد للكمية‬** في صفحة **مستخدمو العمل‬**.</span><span class="sxs-lookup"><span data-stu-id="d9694-188">The counted value isn't within the deviation limits that are specified in the **Maximum percentage limit** or **Maximum quantity limit** fields on the **Work users** page.</span></span> <span data-ttu-id="d9694-189">‏‫على سبيل المثال، كمية المخزون الفعلي في الموقع هي 50 وحد الانحراف لمستخدم العمل هو 10،</span><span class="sxs-lookup"><span data-stu-id="d9694-189">For example, the on-hand inventory quantity in a location is 50, and the deviation limit for the work user is 10.</span></span> <span data-ttu-id="d9694-190">وإذا أدخل مستخدم العمل قيمة لا تقع بين 40 و60، فسيحدث فرق.‬</span><span class="sxs-lookup"><span data-stu-id="d9694-190">If the work user enters a value that isn't between 40 and 60, a difference occurs.</span></span>
-   <span data-ttu-id="d9694-191">تختلف قيمة الجرد عن كمية المخزون الفعلي ولا يتم تعيين حدود الانحراف.</span><span class="sxs-lookup"><span data-stu-id="d9694-191">The counted value differs from the on-hand inventory quantity, and no deviation limits are set.</span></span>

<span data-ttu-id="d9694-192">يمكنك ضبط الفروقات في قيمة الجرد ثم قبول قيمة الجرد في صفحة **تعليق مراجعة الجرد الدوري‬**.</span><span class="sxs-lookup"><span data-stu-id="d9694-192">You can adjust differences in the counted value and then accept the counted value on the **Cycle count pending review** page.</span></span> <span data-ttu-id="d9694-193">يمكن التحقق من الجرد المعدل لكمية الصنف في صفحة **الفعلي حسب الموقع‬**.</span><span class="sxs-lookup"><span data-stu-id="d9694-193">You can verify the modified count of the item quantity on the **On hand by location** page.</span></span> <span data-ttu-id="d9694-194">يتم رفض قيمة الجرد إذا تعذرت الموافقة على الفرق.</span><span class="sxs-lookup"><span data-stu-id="d9694-194">The counted value is rejected if the difference can't be approved.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d9694-195">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="d9694-195">Additional resources</span></span>
[<span data-ttu-id="d9694-196">إعداد الأجهزة المحمولة لعمل المستودع</span><span class="sxs-lookup"><span data-stu-id="d9694-196">Set up mobile devices for warehouse work</span></span>](configure-mobile-devices-warehouse.md)



