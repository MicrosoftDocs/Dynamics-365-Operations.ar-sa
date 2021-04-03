---
title: طلبات الشراء
description: يوضح هذا الموضوع كيفيه دعم طلبات الشراء في تحسين أداء التخطيط.
author: ChristianRytt
manager: tfehr
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqPlanSched, ReqGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 20b4012e054a25d7d21c6f017d8ebcf18f6ee28d
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501068"
---
# <a name="purchase-requisitions"></a><span data-ttu-id="f23b5-103">طلبات الشراء</span><span class="sxs-lookup"><span data-stu-id="f23b5-103">Purchase requisitions</span></span>

<span data-ttu-id="f23b5-104">يمكن للتخطيط الرئيسي ان استعاضة طلبات الشراء المعتمدة.</span><span class="sxs-lookup"><span data-stu-id="f23b5-104">Master planning can replenish approved purchase requisitions.</span></span> <span data-ttu-id="f23b5-105">ولذلك ، لتغطيه طلبات الشراء، لن يضطر المستخدمون إلى استخدام سير عمل لإنشاء أوامر شراء.</span><span class="sxs-lookup"><span data-stu-id="f23b5-105">Therefore, to cover purchase requisitions, users don't have to use a workflow to create purchase orders.</span></span> <span data-ttu-id="f23b5-106">وبدلا من ذلك، يمكن تغطيه طلبات الشراء حسب التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="f23b5-106">Instead, purchase requisitions can be covered by master planning.</span></span> <span data-ttu-id="f23b5-107">وبسبب هذه الوظيفة، يمكن ان يقوم طلب الشراء بإنتاج أمر شراء أو أمر تحويل أو أمر إنتاج، وفقا لقيمه **نوع الأمر المخطط** التي تم تعيينها للمنتج المرتبط.</span><span class="sxs-lookup"><span data-stu-id="f23b5-107">Because of this functionality, a purchase requisition can produce a purchase order, a transfer order, or a production order, depending on the **Planned order type** value that is set for the related product.</span></span>

## <a name="enable-master-plans-to-include-requisitions"></a><span data-ttu-id="f23b5-108">تمكين الخطط الرئيسية لتضمين الطلبات</span><span class="sxs-lookup"><span data-stu-id="f23b5-108">Enable master plans to include requisitions</span></span>

<span data-ttu-id="f23b5-109">لتضمين طلبات اثناء حساب التغطية لخطه رئيسيه، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="f23b5-109">To include requisitions during the coverage calculation for a master plan, follow these steps.</span></span>

1. <span data-ttu-id="f23b5-110">انتقل إلى **التخطيط الرئيسي** \> **الإعداد** \> **الخطط** \> **الخطط الرئيسية**.</span><span class="sxs-lookup"><span data-stu-id="f23b5-110">Go to **Master planning** \> **Setup** \> **Plans** \> **Master plans**.</span></span>
1. <span data-ttu-id="f23b5-111">قم بإنشاء أو تحديد خطه رئيسيه.</span><span class="sxs-lookup"><span data-stu-id="f23b5-111">Create or select a master plan.</span></span>
1. <span data-ttu-id="f23b5-112">في علامة التبويب السريعة **عام**، عيّن الخيار **تضمين الطلب** إلى *نعم*.</span><span class="sxs-lookup"><span data-stu-id="f23b5-112">On the **General** FastTab, set the **Include requisitions** option to *Yes*.</span></span>
1. <span data-ttu-id="f23b5-113">كرر الخطوتين 2 و 3 لكل خطه رئيسيه اضافيه ترغب في تضمين الطلبات فيها.</span><span class="sxs-lookup"><span data-stu-id="f23b5-113">Repeat steps 2 and 3 for each additional master plan where you want to include requisitions.</span></span>

## <a name="approved-requisitions-time-fence"></a><span data-ttu-id="f23b5-114">الحد الزمني للطلبات الموافَق عليها</span><span class="sxs-lookup"><span data-stu-id="f23b5-114">Approved requisitions time fence</span></span>

<span data-ttu-id="f23b5-115">*الحد الزمني للطلبات المعتمدة* الذي يؤسس مدي العودة (بالأيام) ، ستشتمل الخطة الرئيسية علي طلب من طلبات الاستعاضة المعتمدة.</span><span class="sxs-lookup"><span data-stu-id="f23b5-115">The *approved requisitions time fence* establishes how far back (in days) a master plan will include demand from approved replenishment requisitions.</span></span> <span data-ttu-id="f23b5-116">يمكنك تعيين حد زمني لطلبات معتمده في كل من مستوي مجموعه التغطية ومستوي الخطة الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="f23b5-116">You can set an approved requisitions time fence at both the coverage group level and the master plan level.</span></span>

### <a name="set-the-approved-requisitions-time-fence-for-a-coverage-group"></a><span data-ttu-id="f23b5-117">تعيين الحد الزمني للطلبات المعتمدة لمجموعه تغطيه</span><span class="sxs-lookup"><span data-stu-id="f23b5-117">Set the approved requisitions time fence for a coverage group</span></span>

1. <span data-ttu-id="f23b5-118">انتقل إلى **التخطيط الرئيسي** \> **الإعداد** \> **التغطية** \> **مجموعات التغطية**.</span><span class="sxs-lookup"><span data-stu-id="f23b5-118">Go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage groups**.</span></span>
1. <span data-ttu-id="f23b5-119">قم بإنشاء مجموعه تغطيه أو تحديدها.</span><span class="sxs-lookup"><span data-stu-id="f23b5-119">Create or select a coverage group.</span></span>
1. <span data-ttu-id="f23b5-120">علي علامة التبويب السريعة **الأخرى**، قم بتعيين حقل **الحد الزمني للطلبات المعتمدة (الأيام)** إلى عدد الأيام التي سيتم تضمينها في الحد الزمني.</span><span class="sxs-lookup"><span data-stu-id="f23b5-120">On the **Other** FastTab, set the **Approved requisitions time fence (days)** field to the number of days to include in the time fence.</span></span>
1. <span data-ttu-id="f23b5-121">كرر الخطوتين 2 و 3 لكل مجموعه تغطيه اضافيه حيث تريد تعيين الحد الزمني للطلبات المعتمدة.</span><span class="sxs-lookup"><span data-stu-id="f23b5-121">Repeat steps 2 and 3 for each additional coverage group where you want to set an approved requisitions time fence.</span></span>

### <a name="set-the-approved-requisitions-time-fence-for-individual-master-plans"></a><span data-ttu-id="f23b5-122">تعيين الحد الزمني للطلبات المعتمدة للخطط الرئيسية الفردية</span><span class="sxs-lookup"><span data-stu-id="f23b5-122">Set the approved requisitions time fence for individual master plans</span></span>

<span data-ttu-id="f23b5-123">عند تعيين الحد الزمني لطلبات معتمده لخطه رئيسيه فرديه، فان الاعداد يتجاوز اعداد الحد الزمني لآيه مجموعه تغطيه قابله للتطبيق.</span><span class="sxs-lookup"><span data-stu-id="f23b5-123">When you set an approved requisitions time fence for an individual master plan, the setting overrides the time fence setting for any applicable coverage group.</span></span>

1. <span data-ttu-id="f23b5-124">انتقل إلى **التخطيط الرئيسي** \> **الإعداد** \> **الخطط** \> **الخطط الرئيسية**.</span><span class="sxs-lookup"><span data-stu-id="f23b5-124">Go to **Master planning** \> **Setup** \> **Plans** \> **Master plans**.</span></span>
1. <span data-ttu-id="f23b5-125">قم بإنشاء أو تحديد خطه رئيسيه.</span><span class="sxs-lookup"><span data-stu-id="f23b5-125">Create or select a master plan.</span></span>
1. <span data-ttu-id="f23b5-126">علي علامة التبويب السريعة **الحدود الزمنية بالأيام**، قم بتعيين حقل **الحد الزمني للطلبات المعتمدة (الأيام)** إلى عدد الأيام التي سيتم تضمينها في الحد الزمني.</span><span class="sxs-lookup"><span data-stu-id="f23b5-126">On the **TIme fences in days** FastTab, set the **Approved requisitions time fence (days)** field to the number of days to include in the time fence.</span></span>
1. <span data-ttu-id="f23b5-127">كرر الخطوتين 2 و 3 لكل خطة رئيسية اضافيه حيث تريد تعيين الحد الزمني للطلبات المعتمدة.</span><span class="sxs-lookup"><span data-stu-id="f23b5-127">Repeat steps 2 and 3 for each additional master plan where you want to set an approved requisitions time fence.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f23b5-128">**قريبا:** الطلبات المعتمدة لم يتم اعتماد حدود الوقت لتحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="f23b5-128">**Coming soon:** Approved requisitions time fences aren't yet supported for Planning Optimization.</span></span> <span data-ttu-id="f23b5-129">وحتى يتم دعمها، سيتم تجاهل كافة القيم التي تقوم بإدخالها في الحقل **الحد الزمني للطلبات المعتمدة (الأيام)**.</span><span class="sxs-lookup"><span data-stu-id="f23b5-129">Until they are supported, all values that you enter in the **Approved requisitions time fence (days)** field will be ignored.</span></span>

## <a name="independent-supply-regardless-of-coverage-code"></a><span data-ttu-id="f23b5-130">التوريد المستقل، بغض النظر عن كود التغطية</span><span class="sxs-lookup"><span data-stu-id="f23b5-130">Independent supply, regardless of coverage code</span></span>

<span data-ttu-id="f23b5-131">تتم تغطيه طلبات الشراء دائما بالأوامر المخططة المستقلة، بغض النظر عن كود التغطية.</span><span class="sxs-lookup"><span data-stu-id="f23b5-131">Purchase requisitions are always covered by independent planned orders, regardless of the coverage code.</span></span> <span data-ttu-id="f23b5-132">يضمن هذا السلوك مسح إمكانية التتبع ومهام سير العمل بين طلبات الشراء وأوامر التزويد.</span><span class="sxs-lookup"><span data-stu-id="f23b5-132">This behavior ensures clear traceability and workflows between purchase requisitions and replenishment orders.</span></span>

### <a name="example-1"></a><span data-ttu-id="f23b5-133">مثال1</span><span class="sxs-lookup"><span data-stu-id="f23b5-133">Example 1</span></span>

<span data-ttu-id="f23b5-134">يتم اعداد المنتج بحيث يكون له قيمه **كود التغطيه** *للحد الأدنى/الأقصى*. وهي تتضمن حالات المخزون والطلب التالية:</span><span class="sxs-lookup"><span data-stu-id="f23b5-134">A product is set up so that it has a **Coverage code** value of *Min/max*. It has the following inventory and requisition statuses:</span></span>

- <span data-ttu-id="f23b5-135">كمية قائمة المخزون المتاح = 10</span><span class="sxs-lookup"><span data-stu-id="f23b5-135">Inventory on-hand quantity = 10.</span></span>
- <span data-ttu-id="f23b5-136">كمية الحد الأدنى لكمية المخزون = 15</span><span class="sxs-lookup"><span data-stu-id="f23b5-136">Minimum inventory quantity = 15.</span></span>
- <span data-ttu-id="f23b5-137">كمية الحد الأقصى لكمية المخزون = 20</span><span class="sxs-lookup"><span data-stu-id="f23b5-137">Maximum inventory quantity = 20.</span></span>
- <span data-ttu-id="f23b5-138">يوجد طلب شراء لقطعه واحده.</span><span class="sxs-lookup"><span data-stu-id="f23b5-138">A purchase requisition for one piece exists.</span></span> <span data-ttu-id="f23b5-139">وهو تاريخ اليوم المطلوب.</span><span class="sxs-lookup"><span data-stu-id="f23b5-139">It has a requested date of today.</span></span>

<span data-ttu-id="f23b5-140">عند تشغيل التخطيط الرئيسي، يتم إنشاء أمرين مخططين: أحدهما لمده 10 قطع لاستعاضة المخزون إلى الحد الأقصى للكمية، والثاني لقطعه واحده لاستعاضة طلب الشراء.</span><span class="sxs-lookup"><span data-stu-id="f23b5-140">When master planning runs, two planned orders are created: one for 10 pieces to replenish inventory to the maximum quantity, and one for one piece to replenish the purchase requisition.</span></span>

### <a name="example-2"></a><span data-ttu-id="f23b5-141">مثال2</span><span class="sxs-lookup"><span data-stu-id="f23b5-141">Example 2</span></span>

<span data-ttu-id="f23b5-142">يتم اعداد المنتج بحيث يكون له قيمه **كود التغطيه** *للحد الأدنى/الأقصى*. وهي تتضمن حالات المخزون والطلب التالية:</span><span class="sxs-lookup"><span data-stu-id="f23b5-142">A product is set up so that it has a **Coverage code** value of *Min/max*. It has the following inventory and requisition statuses:</span></span>

- <span data-ttu-id="f23b5-143">كمية قائمة المخزون المتاح = 17</span><span class="sxs-lookup"><span data-stu-id="f23b5-143">Inventory on-hand quantity = 17.</span></span>
- <span data-ttu-id="f23b5-144">كمية الحد الأدنى لكمية المخزون = 15</span><span class="sxs-lookup"><span data-stu-id="f23b5-144">Minimum inventory quantity = 15.</span></span>
- <span data-ttu-id="f23b5-145">كمية الحد الأقصى لكمية المخزون = 20</span><span class="sxs-lookup"><span data-stu-id="f23b5-145">Maximum inventory quantity = 20.</span></span>
- <span data-ttu-id="f23b5-146">يوجد طلب شراء لقطعه واحده.</span><span class="sxs-lookup"><span data-stu-id="f23b5-146">A purchase requisition for one piece exists.</span></span> <span data-ttu-id="f23b5-147">وهو تاريخ اليوم المطلوب.</span><span class="sxs-lookup"><span data-stu-id="f23b5-147">It has a requested date of today.</span></span>

<span data-ttu-id="f23b5-148">عند تشغيل التخطيط الرئيسي، يتم إنشاء أمر مخطط واحد لقطعه واحده لاستعاضة طلب الشراء.</span><span class="sxs-lookup"><span data-stu-id="f23b5-148">When master planning runs, one planned order for one piece is created to replenish the purchase requisition.</span></span>

### <a name="example-3"></a><span data-ttu-id="f23b5-149">المثال الثالث</span><span class="sxs-lookup"><span data-stu-id="f23b5-149">Example 3</span></span>

<span data-ttu-id="f23b5-150">يتم اعداد أحد المنتجات بحيث يحتوي علي قيمه **كود التغطية** *للفترة* وطول فتره سبعه أيام.</span><span class="sxs-lookup"><span data-stu-id="f23b5-150">A product is set up so that it has a **Coverage code** value of *Period* and a period length of seven days.</span></span> <span data-ttu-id="f23b5-151">وهي تتضمن حالات المخزون وأمر التوريد والطلب التالية:</span><span class="sxs-lookup"><span data-stu-id="f23b5-151">It has the following inventory, sales order, and requisition statuses:</span></span>

- <span data-ttu-id="f23b5-152">كمية قائمة المخزون المتاح = 0</span><span class="sxs-lookup"><span data-stu-id="f23b5-152">Inventory on-hand quantity = 0.</span></span>
- <span data-ttu-id="f23b5-153">يوجد أمر توريد لخمسه أجزاء.</span><span class="sxs-lookup"><span data-stu-id="f23b5-153">A sales order for five pieces exists.</span></span> <span data-ttu-id="f23b5-154">وهو يحتوي علي تاريخ الشحن المتوقع اليوم بالاضافه إلى يوم واحد.</span><span class="sxs-lookup"><span data-stu-id="f23b5-154">It has an expected ship date of today plus one day.</span></span>
- <span data-ttu-id="f23b5-155">يوجد طلب شراء ثلاثة قطع.</span><span class="sxs-lookup"><span data-stu-id="f23b5-155">A purchase requisition for three pieces exists.</span></span> <span data-ttu-id="f23b5-156">وهو تاريخ اليوم المطلوب بالإضافة إلى ثلاثة أيام.</span><span class="sxs-lookup"><span data-stu-id="f23b5-156">It has a requested date of today plus three days.</span></span>

<span data-ttu-id="f23b5-157">عند تشغيل التخطيط الرئيسي، يتم إنشاء أمرين مخططين: أحدهما لمده ثلاثة قطع لاستعاضة طلب الشراء، والثاني لخمس قطع لاستعاضة طلب الأمر.</span><span class="sxs-lookup"><span data-stu-id="f23b5-157">When master planning runs, two planned orders are created: one for three pieces to replenish the purchase requisition and one for five pieces to replenish sales order demand.</span></span>

> [!NOTE]
> <span data-ttu-id="f23b5-158">وبعد تاكيد الأمر المخطط الذي تم تثبيتها مع طلب شراء، يقوم مشغل التخطيط بالاحتفاظ بالسعر المطلوب لطلب الشراء.</span><span class="sxs-lookup"><span data-stu-id="f23b5-158">After a planned order that is pegged to a purchase requisition is firmed, the planning engine keeps the pegging to the purchase requisition.</span></span> <span data-ttu-id="f23b5-159">إذا تم العثور علي الأمر المؤكد لاحقا لكي تفقد بعض الكمية المطلوبة لاستيفاء طلب الشراء، سيقوم النظام بإنشاء أمر مخطط جديد للفرق.</span><span class="sxs-lookup"><span data-stu-id="f23b5-159">If the firmed order is later found to be missing some quantity that is required to fulfill the purchase requisition, the system will create a new planned order for the difference.</span></span>

<span data-ttu-id="f23b5-160">لمزيد من المعلومات حول طلبات الشراء، راجع [نظره عامه علي طلب الشراء](../../procurement/purchase-requisitions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f23b5-160">For more information about purchase requisitions, see [Purchase requisition overview](../../procurement/purchase-requisitions-overview.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]