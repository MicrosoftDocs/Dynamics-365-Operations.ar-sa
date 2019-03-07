---
title: طلبات للتكاليف القياسية
description: يوضح هذا الموضوع الخطوات الأساسية لاستخدام التكاليف المعيارية.
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventStdCostConv, CostingVersion
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d5a4a4e49ef1cee923011ddab24497c65f85c1e3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "359073"
---
# <a name="prerequisites-for-standard-costs"></a><span data-ttu-id="b164f-103">طلبات للتكاليف القياسية</span><span class="sxs-lookup"><span data-stu-id="b164f-103">Prerequisites for standard costs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b164f-104">يوضح هذا الموضوع الخطوات الأساسية لاستخدام التكاليف المعيارية.</span><span class="sxs-lookup"><span data-stu-id="b164f-104">This topic describes the basic steps for using standard costs.</span></span> <span data-ttu-id="b164f-105">تعتمد الخطوات التالية على عمليات الشركة.</span><span class="sxs-lookup"><span data-stu-id="b164f-105">Subsequent steps depend on the company's operations.</span></span> <span data-ttu-id="b164f-106">على سبيل المثال، تختلف الخطوات لبيئة غير التصنيع، بيئة تصنيع لا تستخدم التوجيهات، وبيئة التصنيع التي تستخدم التوجيهات.</span><span class="sxs-lookup"><span data-stu-id="b164f-106">For example, the steps differ for a nonmanufacturing environment, a manufacturing environment that doesn't use routings, and a manufacturing environment that uses routings.</span></span> 

<span data-ttu-id="b164f-107">لإعداد التكاليف المعيارية، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="b164f-107">To set up standard costs, follow these steps.</span></span>

<span data-ttu-id="b164f-108">**1. أنشئ مجموعة نموذج صنف للتكاليف المعيارية.**</span><span class="sxs-lookup"><span data-stu-id="b164f-108">**1. Create an item model group for standard costs.**</span></span>

<span data-ttu-id="b164f-109">استخدم صفحة **مجموعات نماذج الأصناف** لإنشاء مجموعة جديدة للتكاليف المعيارية، وتعيين نموذج مخزون لـ **التكلفة المعيارية**.</span><span class="sxs-lookup"><span data-stu-id="b164f-109">Use the **Item model groups** page to create a new group for standard costs, and assign an inventory model of **Standard cost**.</span></span> <span data-ttu-id="b164f-110">يجب أن يكون المعرف الخاص بمجموعة نموذج الصنف ذا معنى، مثل **التكلفة المعيارية**.</span><span class="sxs-lookup"><span data-stu-id="b164f-110">The identifier for the item model group should be meaningful, such as **Std Cost**.</span></span> <span data-ttu-id="b164f-111">حدد خانات الاختيار للإشارة إلى أنه يجب على المجموعة السماح بالمخزون السلبي المالي، وكذلك ترحيل المخزون المادي، وترحيل المخزون المالي.</span><span class="sxs-lookup"><span data-stu-id="b164f-111">Select the check boxes to indicate that the group should allow financial negative inventory, and that it should post physical inventory and financial inventory.</span></span> <span data-ttu-id="b164f-112">وسوف يتم تعيين مجموعة التكلفة المعيارية هذه للأصناف.</span><span class="sxs-lookup"><span data-stu-id="b164f-112">This standard cost group will be assigned to items.</span></span>

<span data-ttu-id="b164f-113">**2. حدد حسابات دفتر الأستاذ المتعلقة بمتغيرات التكلفة المعيارية.**</span><span class="sxs-lookup"><span data-stu-id="b164f-113">**2. Define ledger accounts that are related to standard cost variances.**</span></span> 

<span data-ttu-id="b164f-114">استخدم صفحة **مخطط الحسابات** لتحديد حسابات دفتر الأستاذ المتعلقة بمتغيرات التكلفة المعيارية.</span><span class="sxs-lookup"><span data-stu-id="b164f-114">Use the **Chart of accounts** page to define ledger accounts that are related to standard cost variances.</span></span> <span data-ttu-id="b164f-115">ويجب تحديد حسابات دفتر الأستاذ هذه قبل التمكن من تعيينها في صفحة **الترحيل**.</span><span class="sxs-lookup"><span data-stu-id="b164f-115">These ledger accounts must be defined before they can be assigned on the **Posting** page.</span></span> <span data-ttu-id="b164f-116">حيث يمكن أن تعكس حسابات دفتر الأستاذ مجموعات الصنف ومجموعات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="b164f-116">The ledger accounts can reflect item groups and cost groups.</span></span>

<span data-ttu-id="b164f-117">**3. قم بتعيين حسابات دفتر الأستاذ لعمليات ترحيل الأصناف المتعلقة بمتغيرات التكلفة القياسية.**</span><span class="sxs-lookup"><span data-stu-id="b164f-117">**3. Assign ledger accounts to item postings that are related to standard cost variances.**</span></span> 

<span data-ttu-id="b164f-118">استخدم صفحة **الترحيل** لتعيين حسابات دفتر الأستاذ المتعلقة بمتغيرات التكلفة القياسية.</span><span class="sxs-lookup"><span data-stu-id="b164f-118">Use the **Posting** page to assign the ledger accounts that are related to standard cost variances.</span></span> <span data-ttu-id="b164f-119">ويمكنك تحديد حساب دفتر الأستاذ للمتغير بواسطة الصنف (أو مجموعة الصنف) وبواسطة مجموعة التكلفة (أو نوع مجموعة التكلفة)، أو يمكنك تحديد تطبيق حساب دفتر الأستاذ على كافة الأصناف وكافة مجموعات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="b164f-119">You can specify a variance's ledger account by item (or item group) and by cost group (or cost group type), or you can specify that the ledger account applies to all items and all cost groups.</span></span> <span data-ttu-id="b164f-120">وتتوافق هذه الخيارات مع علاقات التكلفة للجداول والمجموعات وجميع ذلك.</span><span class="sxs-lookup"><span data-stu-id="b164f-120">These options correspond to cost relations for tables, groups, and all.</span></span> 

<span data-ttu-id="b164f-121">قبل تحديد قواعد ترحيل الصنف، استخدم صفحة **مجموعات الحركات** لتمكين علاقات التكاليف (للجداول والمجموعات والكل).</span><span class="sxs-lookup"><span data-stu-id="b164f-121">Before you define the item posting rules, use the **Transaction combinations** page to enable cost relations (for tables, groups, and all).</span></span>

<span data-ttu-id="b164f-122">**4. قم بتحديد محددات المخزون المتعلقة بالتكاليف المعيارية.**</span><span class="sxs-lookup"><span data-stu-id="b164f-122">**4. Define inventory parameters that are related to standard costs.**</span></span> 

-  <span data-ttu-id="b164f-123">استخدم علامة **محاسبة المخزون** في صفحة **إعداد سياسات محاسبة المخزون > المعلمات** لتحديد معلمتين للتحكم في التكلفة ترتبطان بالتكاليف المعيارية.</span><span class="sxs-lookup"><span data-stu-id="b164f-123">Use the **Inventory accounting** tab on the **Inventory accounting policies setup > Parameters** page to define two cost control parameters that are related to standard costs.</span></span>

    -  <span data-ttu-id="b164f-124">في حقل **تصنيف التكاليف**، حدد **لا شيء** أو **دفتر الأستاذ الفرعي**.</span><span class="sxs-lookup"><span data-stu-id="b164f-124">In the **Cost breakdown** field, select **None** or **Sub ledger**.</span></span> <span data-ttu-id="b164f-125">إذا قمت بتحديد **دفتر الأستاذ الفرعي**، يكون تصنيف التكلفة هو تصنيف تكلفة *نشط*.</span><span class="sxs-lookup"><span data-stu-id="b164f-125">If you select **Sub ledger**, the cost breakdown is an *active* cost breakdown.</span></span> <span data-ttu-id="b164f-126">يُعد تصنيف التكاليف النشط ضروريًا لحساب تقسيم مجموعة التكاليف والاحتفاظ بها وعرضها عبر بنية منتج متعددة المستويات للأصناف ذات التكلفة المعيارية.</span><span class="sxs-lookup"><span data-stu-id="b164f-126">An active cost breakdown is critical for calculating, retaining, and viewing cost group segmentation across a multilevel product structure for standard cost items.</span></span> <span data-ttu-id="b164f-127">عندما يكون تصنيف التكلفة نشطًا، يُمكنك الإعلام عن المخزون والأعمال تحت التنفيذ وتكلفة السلع المبيعة لكل مجموعة تكاليف في مستوى واحد أو مستويات متعددة أو في التنسيق الإجمالي.</span><span class="sxs-lookup"><span data-stu-id="b164f-127">When the cost breakdown is active, you can report and analyze inventory, work in process (WIP), and cost of goods sold (COGS) per cost group in a single-level, multilevel, or total format.</span></span> <span data-ttu-id="b164f-128">عندما يكون تصنيف التكلفة نشطًا، إذا قمت بتنشيط تكلفة صنف، فسيتم تخزين تقسيم مجموعة التكلفة في سجل تكلفة الصنف.</span><span class="sxs-lookup"><span data-stu-id="b164f-128">When the cost breakdown is active, if you activate a manufactured item's cost, the cost group segmentation will be stored in the item's cost record.</span></span> 

    -  <span data-ttu-id="b164f-129">إذا قمت بتحديد **بلا**، فلن يتم الاحتفاظ بتقسيم مجموعة التكلفة لأصناف التكلفة المعيارية.</span><span class="sxs-lookup"><span data-stu-id="b164f-129">If you select **None**, cost group segmentation won't be maintained for standard cost items.</span></span> <span data-ttu-id="b164f-130">بمعنى آخر، سيتم حساب التكلفة المعيارية لصنف مصنع والاحتفاظ بها كمبلغ واحد، دون تقسيم مجموعة التكلفة.</span><span class="sxs-lookup"><span data-stu-id="b164f-130">In other words, a manufactured item's standard cost will be calculated and maintained as a single amount, without cost group segmentation.</span></span> <span data-ttu-id="b164f-131">سيتم تجميع مساهمات التكلفة للمكونات التي تم تصنيعها في المبلغ الواحد.</span><span class="sxs-lookup"><span data-stu-id="b164f-131">The cost contributions of manufactured components will be aggregated into the single amount.</span></span>

-  <span data-ttu-id="b164f-132">في حقل **نسب الفرق بالنسبة للإعداد القياسي**، حدد **ملخص** أو **حسب مجموعة التكاليف‬**.</span><span class="sxs-lookup"><span data-stu-id="b164f-132">In the **Variances to standard** field, select **Summarized** or **Per cost group**.</span></span> <span data-ttu-id="b164f-133">إذا حددت **حسب مجموعة التكاليف**، يمكّنك تحديد نسب الفرق في أسعار الشراء ونسب الفرق في الإنتاج حسب مجموعة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="b164f-133">If you select **Per cost group**, you can identify purchase price variances and production variances by cost group.</span></span> <span data-ttu-id="b164f-134">كما يمكنك تحديد الأنواع الأربعة لنسب الفرق في الإنتاج: حجم الدفعة، والكمية، والسعر، ونسب الفرق في الإحلال.</span><span class="sxs-lookup"><span data-stu-id="b164f-134">You can also identify the four types of production variances: the lot size, quantity, price, and substitution variances.</span></span> <span data-ttu-id="b164f-135">إذا حددت **ملخص**، فإنه لا يمكنك تحديد نسب الفرق حسب مجموعة التكاليف، كما أنه لا يُمكنك تحديد الأنواع الأربعة لنسب الفرق في الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="b164f-135">If you select **Summarized**, you can't identify variances by cost group, and you can't identify the four types of production variances.</span></span> <span data-ttu-id="b164f-136">يمكنك فقط عرض نسب الفرق الملخصة في تسعير الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="b164f-136">You can just view a summarized production variance.</span></span>

-  <span data-ttu-id="b164f-137">ويعمل النهج الخاص بنسبة الفرق بالنسبة إلى المعيار بشكل مستقل عن نهج تصنيف التكاليف.</span><span class="sxs-lookup"><span data-stu-id="b164f-137">The policy about variance to standard works independently of the cost breakdown policy.</span></span> <span data-ttu-id="b164f-138">بمعنى آخر أنه يمكنك تحديد نهج تصنيف تكاليف **للاشيء**، وتحديد نسب الفرق لكل مجموعة تكاليف، وذلك حتى تظل نسب الفرق في الإنتاج حسب مجموعة التكاليف قابلةً للتسجيل.</span><span class="sxs-lookup"><span data-stu-id="b164f-138">In other words, you can select a cost breakdown policy of **None** and select variances per cost group, so that production variances by cost group will still be captured.</span></span>

<span data-ttu-id="b164f-139">**5. أنشئ إصدارات تكلفة للتكاليف المعيارية.**</span><span class="sxs-lookup"><span data-stu-id="b164f-139">**5. Create costing versions for standard costs.**</span></span> 

<span data-ttu-id="b164f-140">استخدم صفحة **إعداد إصدار حساب التكلفة‬** لإنشاء إصدار واحد أو أكثر من إصدارات التكاليف للتكاليف المعيارية.</span><span class="sxs-lookup"><span data-stu-id="b164f-140">Use the **Costing version setup** page to create one or more costing versions for standard costs.</span></span> <span data-ttu-id="b164f-141">ويجب تعيين كل إصدار تكلفة حسب نوع تكلفة **التكلفة المعيارية** بالإضافة إلى السماح بتضمين المحتوى لبيانات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="b164f-141">Each costing version must be designated by a costing type of **Standard cost** and must allow content to include cost data.</span></span>

<span data-ttu-id="b164f-142">**6. 6. قم بإعداد عميل حالي لاستخدام التكاليف المعيارية.**</span><span class="sxs-lookup"><span data-stu-id="b164f-142">**6. Prepare an existing customer to use standard costs.**</span></span> 

<span data-ttu-id="b164f-143">ويتعين على العملاء الذين يرغبون في تغيير الأصناف الحالية الخاصة بهم إلى نموذج مخزون تكلفة معيارية استخدام صفحة **عمليات تحويل التكلفة المعيارية**.</span><span class="sxs-lookup"><span data-stu-id="b164f-143">Customers who want to change their existing items to a standard cost inventory model must use the **Standard cost conversions** page.</span></span>


<a name="related-topics"></a><span data-ttu-id="b164f-144">مواضيع مرتبطة</span><span class="sxs-lookup"><span data-stu-id="b164f-144">Related topics</span></span>
--------

[<span data-ttu-id="b164f-145">نظرة عامة حول تحويل التكاليف القياسية</span><span class="sxs-lookup"><span data-stu-id="b164f-145">Standard cost conversion overview</span></span>](standard-cost-conversion-overview.md)

### <a name="blogs"></a><span data-ttu-id="b164f-146">المدونات</span><span class="sxs-lookup"><span data-stu-id="b164f-146">Blogs</span></span>

#### <a name="community-blogs"></a><span data-ttu-id="b164f-147">مدونات المجتمعات</span><span class="sxs-lookup"><span data-stu-id="b164f-147">Community blogs</span></span>

- [<span data-ttu-id="b164f-148">كيفية إعداد التكاليف القياسية للمواد المباشرة في Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b164f-148">How to set up standard costs for direct materials in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/06/07/how-to-set-up-standard-costs-for-direct-materials-in-dynamics-365-for-finance-and-operations)
- [<span data-ttu-id="b164f-149">تكاليف العمالة المباشرة القياسية في Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b164f-149">Standard direct labor costs in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/07/16/standard-direct-labor-cost-in-dynamics-365-for-finance-and-operations)
