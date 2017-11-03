---
title: "عقود المشاريع"
description: "تصف هذه المقالة عقود المشاريع التي يمكنك إنشاؤها لمختلف أنواع المشاريع ومصادر التمويل وكيفية إدارة العقود وفوترة عملاء المشاريع في Microsoft Dynamics 365 for Finance and Operations, Enterprise edition، كما تقدم أمثلة لهذه العقود."
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7a69036327c6e818c1d4a3da72ee2f4c2d19cfcd
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="project-contracts"></a><span data-ttu-id="cce60-103">عقود المشروع</span><span class="sxs-lookup"><span data-stu-id="cce60-103">Project contracts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="cce60-104">تصف هذه المقالة عقود المشاريع التي يمكنك إنشاؤها لمختلف أنواع المشاريع ومصادر التمويل وكيفية إدارة العقود وفوترة عملاء المشاريع في Microsoft Dynamics 365 for Finance and Operations, Enterprise edition، كما تقدم أمثلة لهذه العقود.</span><span class="sxs-lookup"><span data-stu-id="cce60-104">This article describes and provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

<span data-ttu-id="cce60-105">يحدد نوع المشروع الذي تقوم بإنشائه لعقد مشروع الطريقة المستخدمة لفوترة عملاء المشروع.</span><span class="sxs-lookup"><span data-stu-id="cce60-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="cce60-106">ويمكنك تغيير عقد مشروع والمشروع المرتبط، ولكن لا يمكنك تغيير نوع المشروع.</span><span class="sxs-lookup"><span data-stu-id="cce60-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="cce60-107">وباستخدام عقد مشروع، يمكنك فوترة مشروع واحد أو عدة مشاريع في الوقت ذاته.</span><span class="sxs-lookup"><span data-stu-id="cce60-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="cce60-108">وكذلك يساعدك عقد المشروع على التأكد من تطبيق إجراء فوترة موحَّد لكل مشروع فرعي في بنية المشروع.</span><span class="sxs-lookup"><span data-stu-id="cce60-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="cce60-109">ويجب أن يكون كل مشروع سيتم فوترته مقترنًا بعقد مشروع.</span><span class="sxs-lookup"><span data-stu-id="cce60-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="cce60-110">وتنطبق الإعدادات الخاصة بعقد المشروع على جميع المشاريع والمشاريع الفرعية المقترنة بعقد المشروع.</span><span class="sxs-lookup"><span data-stu-id="cce60-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="cce60-111">يمكن لعقد المشروع تحديد مصدر واحد أو أكثر من مصادر التمويل.</span><span class="sxs-lookup"><span data-stu-id="cce60-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="cce60-112">ولذلك، يمكنك تقسيم الفوترة بين ممولين متعددين، وإعداد حدود للتمويل حتى لا يتم إصدار فاتورة مصادر التمويل بأكثر من المبلغ المحدد، وتكوين قواعد التمويل لتقاضي النفقات.</span><span class="sxs-lookup"><span data-stu-id="cce60-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="cce60-113">تمويل عقود المشروع</span><span class="sxs-lookup"><span data-stu-id="cce60-113">Funding for project contracts</span></span>
<span data-ttu-id="cce60-114">تحدد بعض عقود المشروع أن الأطراف المتعددة تشارك مسؤولية تمويل تكاليف المشروع.</span><span class="sxs-lookup"><span data-stu-id="cce60-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="cce60-115">فيما يلي بعض الأمثلة:</span><span class="sxs-lookup"><span data-stu-id="cce60-115">Here are some examples:</span></span>

-   <span data-ttu-id="cce60-116">يطلب عميل كبير يمتلك أقسام متعددة تقسيم تمويل المشروع حسب القسم.</span><span class="sxs-lookup"><span data-stu-id="cce60-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="cce60-117">تشارك شركتك تكاليف مشروع كبير مع مؤسسة خارجية.</span><span class="sxs-lookup"><span data-stu-id="cce60-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="cce60-118">يتم تمويل مشروع طرق بشكل مشترك بين بلديتين.</span><span class="sxs-lookup"><span data-stu-id="cce60-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="cce60-119">يتم تمويل مشروع جسر بمنحه حكومية وشركة خاصة.</span><span class="sxs-lookup"><span data-stu-id="cce60-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="cce60-120">في Finance and Operations، يمكنك تقسيم الفوترة لحركة واحدة أو مشروع بأكمله بين عملاء أو منح أو مؤسسات متعددة.</span><span class="sxs-lookup"><span data-stu-id="cce60-120">In Finance and Operations, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="cce60-121">وفي المشاريع التي تحتوي على العديد من الممولين، تُسمى جميع الأطراف المساهمة في تمويل مشروع التمويل المتقدم مصادر التمويل.</span><span class="sxs-lookup"><span data-stu-id="cce60-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="cce60-122">وبعد تحديد العميل أو المؤسسة أو المنحة كمصدر للتمويل، يمكن تعيينها لواحد أو أكثر من قواعد التمويل.</span><span class="sxs-lookup"><span data-stu-id="cce60-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="cce60-123">وتتضمن قواعد التمويل المعايير التي تحدد كيفية تخصيص المصاريف لمختلف مصادر التمويل لمشروع.</span><span class="sxs-lookup"><span data-stu-id="cce60-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="cce60-124">ولأن الأصناف المخزنة، مثل تلك التي تظهر في طلبات الشراء وأوامر الشراء، لا يمكن تقسيمها، لا يمكن تقسيم مبلغ التكلفة بين مصادر التمويل المتعددة في وقت التوزيع.</span><span class="sxs-lookup"><span data-stu-id="cce60-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="cce60-125">وبالتالي، تظل قيمة مصدر التمويل 0 (صفر) حتى يتم ترحيل إصدار المخزون.</span><span class="sxs-lookup"><span data-stu-id="cce60-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="cce60-126">وعندما يتم ترحيل إصدار المخزون، يتم توزيع مبلغ التكلفة وفقًا لقواعد توزيع الحساب للمشروع.</span><span class="sxs-lookup"><span data-stu-id="cce60-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="cce60-127">فيما يلي بعض الخطوات التي يمكنك اتخاذها لتسهيل عملية تقسيم الفواتير بين مصادر تمويل متعددة:</span><span class="sxs-lookup"><span data-stu-id="cce60-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="cce60-128">تحديد أن كافة الحركات التي تم إدخالها لمشروع تستخدم نفس عملة المبيعات كعقد المشروع.</span><span class="sxs-lookup"><span data-stu-id="cce60-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="cce60-129">إعداد حدود التمويل، بحيث لا تتم فوترة مصدر تمويل أكبر من مبلغ محدد تجاه مشروع.</span><span class="sxs-lookup"><span data-stu-id="cce60-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="cce60-130">تكوين قواعد التمويل وحدود التمويل لكل عامل، وصنف، وفئة، ومجموعة فئات، ونوع الحركة (أو كافة أنواع الحركات).</span><span class="sxs-lookup"><span data-stu-id="cce60-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="cce60-131">تحديد تواريخ بدء وانتهاء اختيارية لتحديد الفترة التي يتكون فيها كل قاعدة تمويل صالحة.</span><span class="sxs-lookup"><span data-stu-id="cce60-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="cce60-132">تحديد النسبة المئوية التي يكون كل مصدر تمويل مسؤول عنها.</span><span class="sxs-lookup"><span data-stu-id="cce60-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="cce60-133">تحديد مصدر التمويل المسؤول عن تقريب الفروق ناتجة من عمليات حساب توزيع التمويل.</span><span class="sxs-lookup"><span data-stu-id="cce60-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="cce60-134">إعداد القواعد التي تحدد كيفية فوترة تكاليف المشروع لعملاء خارجيين وتحميلها على المؤسسات الداخلية.</span><span class="sxs-lookup"><span data-stu-id="cce60-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="cce60-135">تسجيل الحركات في حساب تمويل قيد الانتظار حتى يمكن الحصول على تمويل إضافي أو حتى تقرر تحمل التكاليف داخليًا.</span><span class="sxs-lookup"><span data-stu-id="cce60-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="cce60-136">لتحديد مجموعة الضرائب المراد إقرانها بحركة، يتم البحث في المشروع لتعيين مجموعة ضريبة.</span><span class="sxs-lookup"><span data-stu-id="cce60-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="cce60-137">وإذا لم يتم تعيين مجموعة ضريبة على مستوى المشروع، يتم البحث في عقد المشروع.</span><span class="sxs-lookup"><span data-stu-id="cce60-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="cce60-138">مثال: مصادر تمويل متعددة (بسيطة)</span><span class="sxs-lookup"><span data-stu-id="cce60-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="cce60-139">يوفر الجدول التالي سيناريوهات لإدارة توزيع التمويل بين مصادر تمويل متعددة.</span><span class="sxs-lookup"><span data-stu-id="cce60-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="cce60-140">وتستند هذه السيناريوهات إلى الافتراضات التالية:</span><span class="sxs-lookup"><span data-stu-id="cce60-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="cce60-141">تتم مراعاة إعدادات الأولوية في توزيع الأموال قبل تطبيق معايير قاعدة التمويل الأخرى.</span><span class="sxs-lookup"><span data-stu-id="cce60-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="cce60-142">لم يتم تحديد نطاق تاريخ لتحديد فترة د عندما تكون قاعدة التمويل صالحة.</span><span class="sxs-lookup"><span data-stu-id="cce60-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cce60-143"><strong>السيناريو</strong></span><span class="sxs-lookup"><span data-stu-id="cce60-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="cce60-144"><strong>مصدر التمويل </strong></span><span class="sxs-lookup"><span data-stu-id="cce60-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="cce60-145"><strong>النسبة المئوية للتوزيع </strong></span><span class="sxs-lookup"><span data-stu-id="cce60-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="cce60-146"><strong>أولوية التوزيع </strong></span><span class="sxs-lookup"><span data-stu-id="cce60-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cce60-147">تحتاج إلى توزيع التكاليف إلى مصدر تمويل واحد حتى يتم استنفاد أمواله، وتوزيع التكاليف إلى مصدر تمويل ثاني حتى تُستنفد أمواله، وأخيراً تخصيص التكاليف المتبقية مصدر تمويل ثالث.</span><span class="sxs-lookup"><span data-stu-id="cce60-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="cce60-148">التمويل　المصدر　1</span><span class="sxs-lookup"><span data-stu-id="cce60-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="cce60-149">التمويل　المصدر　2</span><span class="sxs-lookup"><span data-stu-id="cce60-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="cce60-150">التمويل　المصدر　3</span><span class="sxs-lookup"><span data-stu-id="cce60-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="cce60-151">100%</span><span class="sxs-lookup"><span data-stu-id="cce60-151">100%</span></span></li>
<li><span data-ttu-id="cce60-152">100%</span><span class="sxs-lookup"><span data-stu-id="cce60-152">100%</span></span></li>
<li><span data-ttu-id="cce60-153">100%</span><span class="sxs-lookup"><span data-stu-id="cce60-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="cce60-154">1</span><span class="sxs-lookup"><span data-stu-id="cce60-154">1</span></span></li>
<li><span data-ttu-id="cce60-155">2</span><span class="sxs-lookup"><span data-stu-id="cce60-155">2</span></span></li>
<li><span data-ttu-id="cce60-156">3</span><span class="sxs-lookup"><span data-stu-id="cce60-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cce60-157">تحتاج إلى تخصيص 25 في المائة من التكاليف لمصدر تمويل واحد و75 في المائة من التكاليف لمصدر تمويل ثاني.</span><span class="sxs-lookup"><span data-stu-id="cce60-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="cce60-158">وعند استنفاد أيٍّ من مصادر التمويل هذه، تحتاج إلى دفع التكاليف المتبقية من مصدر التمويل الثالث.</span><span class="sxs-lookup"><span data-stu-id="cce60-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="cce60-159">التمويل　المصدر　1</span><span class="sxs-lookup"><span data-stu-id="cce60-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="cce60-160">التمويل　المصدر　2</span><span class="sxs-lookup"><span data-stu-id="cce60-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="cce60-161">التمويل　المصدر　3</span><span class="sxs-lookup"><span data-stu-id="cce60-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="cce60-162">75%</span><span class="sxs-lookup"><span data-stu-id="cce60-162">75%</span></span></li>
<li><span data-ttu-id="cce60-163">25%</span><span class="sxs-lookup"><span data-stu-id="cce60-163">25%</span></span></li>
<li><span data-ttu-id="cce60-164">100%</span><span class="sxs-lookup"><span data-stu-id="cce60-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="cce60-165">1</span><span class="sxs-lookup"><span data-stu-id="cce60-165">1</span></span></li>
<li><span data-ttu-id="cce60-166">1</span><span class="sxs-lookup"><span data-stu-id="cce60-166">1</span></span></li>
<li><span data-ttu-id="cce60-167">2</span><span class="sxs-lookup"><span data-stu-id="cce60-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cce60-168">تحتاج إلى تخصيص 25 في المائة من التكاليف لمصدر تمويل واحد و75 في المائة من التكاليف لمصدر تمويل ثاني.</span><span class="sxs-lookup"><span data-stu-id="cce60-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="cce60-169">وعند استنفاد أيٍّ من مصادر التمويل هذه، تحتاج إلى تقسيم التكاليف المتبقية بين مصدر تمويل ثالث ومصدر تمويل رابع.</span><span class="sxs-lookup"><span data-stu-id="cce60-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="cce60-170">التمويل　المصدر　1</span><span class="sxs-lookup"><span data-stu-id="cce60-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="cce60-171">التمويل　المصدر　2</span><span class="sxs-lookup"><span data-stu-id="cce60-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="cce60-172">التمويل　المصدر　3</span><span class="sxs-lookup"><span data-stu-id="cce60-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="cce60-173">التمويل　المصدر　4</span><span class="sxs-lookup"><span data-stu-id="cce60-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="cce60-174">75%</span><span class="sxs-lookup"><span data-stu-id="cce60-174">75%</span></span></li>
<li><span data-ttu-id="cce60-175">25%</span><span class="sxs-lookup"><span data-stu-id="cce60-175">25%</span></span></li>
<li><span data-ttu-id="cce60-176">50%</span><span class="sxs-lookup"><span data-stu-id="cce60-176">50%</span></span></li>
<li><span data-ttu-id="cce60-177">50%</span><span class="sxs-lookup"><span data-stu-id="cce60-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="cce60-178">1</span><span class="sxs-lookup"><span data-stu-id="cce60-178">1</span></span></li>
<li><span data-ttu-id="cce60-179">1</span><span class="sxs-lookup"><span data-stu-id="cce60-179">1</span></span></li>
<li><span data-ttu-id="cce60-180">2</span><span class="sxs-lookup"><span data-stu-id="cce60-180">2</span></span></li>
<li><span data-ttu-id="cce60-181">2</span><span class="sxs-lookup"><span data-stu-id="cce60-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cce60-182">تحتاج إلى تخصيص نسبة الـ 25 في المائة الأولى من التكاليف لمصدر تمويل واحد والبقية إلى مصدر تمويل ثاني.</span><span class="sxs-lookup"><span data-stu-id="cce60-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="cce60-183">التمويل　المصدر　1</span><span class="sxs-lookup"><span data-stu-id="cce60-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="cce60-184">التمويل　المصدر　2</span><span class="sxs-lookup"><span data-stu-id="cce60-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="cce60-185">25%</span><span class="sxs-lookup"><span data-stu-id="cce60-185">25%</span></span></li>
<li><span data-ttu-id="cce60-186">100%</span><span class="sxs-lookup"><span data-stu-id="cce60-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="cce60-187">1</span><span class="sxs-lookup"><span data-stu-id="cce60-187">1</span></span></li>
<li><span data-ttu-id="cce60-188">2</span><span class="sxs-lookup"><span data-stu-id="cce60-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="cce60-189">مثال: مصادر تمويل متعددة (معقدة)</span><span class="sxs-lookup"><span data-stu-id="cce60-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="cce60-190">لديك ثلاثة مصادر تمويل تريد استخدامها بالترتيب التالي:</span><span class="sxs-lookup"><span data-stu-id="cce60-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="cce60-191">استخدام مصدر التمويل 2  ومصادر التمويل 3 بالتساوي حتى يتم استنفاد مصدر التمويل 2.</span><span class="sxs-lookup"><span data-stu-id="cce60-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="cce60-192">مواصلة استخدام مصدر تمويل 3 حتى يتم استنفاد.</span><span class="sxs-lookup"><span data-stu-id="cce60-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="cce60-193">استخدام مصدر التمويل 1 بعد استنفاد مصدر التمويل 3.</span><span class="sxs-lookup"><span data-stu-id="cce60-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="cce60-194">بعد تحقيق هذا الهدف، يجب عليك القيام بما يلي:</span><span class="sxs-lookup"><span data-stu-id="cce60-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="cce60-195">إعداد حدود التمويل لمصدر التمويل 2 ومصدر التمويل 3، للمبالغ ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="cce60-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="cce60-196">إنشاء قواعد التمويل التالية:</span><span class="sxs-lookup"><span data-stu-id="cce60-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="cce60-197">القاعدة 1 (الأولوية 1): تخصيص 50 في المائة من الحركات لمصدر التمويل 2 و50 في المائة لمصدر التمويل 3.</span><span class="sxs-lookup"><span data-stu-id="cce60-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="cce60-198">القاعدة 2 (الأولوية 2): تخصيص 100 في المائة من الحركات لمصدر التمويل 3.</span><span class="sxs-lookup"><span data-stu-id="cce60-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="cce60-199">القاعدة 3 (الأولوية 3): تخصيص 100 في المائة من الحركات لمصدر التمويل 1.</span><span class="sxs-lookup"><span data-stu-id="cce60-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="cce60-200">يعمل هذا الإعداد لأنه يتم التحقق من حركات مقابل القواعد والحدود لتحديد ما إذا كان أي منها ينطبق على الحركة.</span><span class="sxs-lookup"><span data-stu-id="cce60-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="cce60-201">وإذا لم يتم تطبيق أي قواعد أو حدود معينة على الحركة، يتم تطبيق قاعدة كافة الحركات.</span><span class="sxs-lookup"><span data-stu-id="cce60-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="cce60-202">وتتطابق قاعدة كافة الحركات مع كافة الحركات.</span><span class="sxs-lookup"><span data-stu-id="cce60-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="cce60-203">وإذا تم العثور على قاعدة تطابق حركة، يتم تطبيق النسبة المئوية التي خُصصت في تلك القاعدة أولاً، لكن فقط بعد فحص المطابقات مقابل أي حدود تم إعدادها.</span><span class="sxs-lookup"><span data-stu-id="cce60-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="cce60-204">وإذا تم استيفاء حد، وتم استنفاد أموال مصدر تمويل، فإنه يتم تجاهل قاعدة التمويل المقترنة بحد التمويل، ويبحث البرنامج عن القاعدة التالية التي تنطبق.</span><span class="sxs-lookup"><span data-stu-id="cce60-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="cce60-205">وفي بعض الحالات، يمكن تخصيص جزء من الحركة فقط ضمن قاعدة.</span><span class="sxs-lookup"><span data-stu-id="cce60-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="cce60-206">وقد يحدث ذلك بسبب بلوغ حد عندما يتم توزيع الحركة.</span><span class="sxs-lookup"><span data-stu-id="cce60-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="cce60-207">وفي هذه الحالة، يتم تخصيص مقدار معين فقط وفقًا لتلك القاعدة، مثل 50 في المائة لكل مصدر من مصادر التمويل.</span><span class="sxs-lookup"><span data-stu-id="cce60-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="cce60-208">وفي هذه الحالة في القاعدة 1, الموضحة سابقًا في هذا القسم.</span><span class="sxs-lookup"><span data-stu-id="cce60-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="cce60-209">ويُخصص الباقي طبقاً للقاعدة التالية في التسلسل.</span><span class="sxs-lookup"><span data-stu-id="cce60-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="cce60-210">يفحص الجدول التالي هذا السيناريو بمزيد من التفصيل.</span><span class="sxs-lookup"><span data-stu-id="cce60-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cce60-211"><strong>التركيز </strong></span><span class="sxs-lookup"><span data-stu-id="cce60-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="cce60-212"><strong>التفاصيل</strong></span><span class="sxs-lookup"><span data-stu-id="cce60-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cce60-213">قواعد التمويل</span><span class="sxs-lookup"><span data-stu-id="cce60-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="cce60-214">القاعدة 1 (الأولوية 1): كافة الحركات.</span><span class="sxs-lookup"><span data-stu-id="cce60-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="cce60-215">تخصيص مصدر التمويل 2  بنسبة 50% ومصدر التمويل 3 بنسبة 50%.</span><span class="sxs-lookup"><span data-stu-id="cce60-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="cce60-216">القاعدة 2 (الأولوية 2): كافة الحركات.</span><span class="sxs-lookup"><span data-stu-id="cce60-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="cce60-217">تخصيص مصدر التمويل 3 بنسبة 100%.</span><span class="sxs-lookup"><span data-stu-id="cce60-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="cce60-218">القاعدة 3 (الأولوية 2): كافة الحركات.</span><span class="sxs-lookup"><span data-stu-id="cce60-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="cce60-219">تخصيص مصدر التمويل 1 بنسبة 100%.</span><span class="sxs-lookup"><span data-stu-id="cce60-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cce60-220">حدود التمويل</span><span class="sxs-lookup"><span data-stu-id="cce60-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="cce60-221">حد مصدر التمويل 1 = 10,000.00</span><span class="sxs-lookup"><span data-stu-id="cce60-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="cce60-222">حد مصدر التمويل 2 = 500.00</span><span class="sxs-lookup"><span data-stu-id="cce60-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="cce60-223">حد مصدر التمويل 3 = 750.00</span><span class="sxs-lookup"><span data-stu-id="cce60-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cce60-224">الحركة 1</span><span class="sxs-lookup"><span data-stu-id="cce60-224">Transaction 1</span></span></td>
<td><span data-ttu-id="cce60-225"><strong>مبلغ الحركة:</strong> 100.00<strong>التمويل:</strong> يتم دفع الحركة وفقًا للقاعدة 1 فقط، لأن الحركة يتم دفعها بالكامل بعد تطبيق القاعدة 1.</span><span class="sxs-lookup"><span data-stu-id="cce60-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="cce60-226">ويتم تمويل الحركة بالتساوي بين مصدر التمويل 2 ومصدر التمويل 3.</span><span class="sxs-lookup"><span data-stu-id="cce60-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="cce60-227">مصدر التمويل 2: 50.00</span><span class="sxs-lookup"><span data-stu-id="cce60-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="cce60-228">مصدر التمويل 3: 50.00</span><span class="sxs-lookup"><span data-stu-id="cce60-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cce60-229">الحركة 2</span><span class="sxs-lookup"><span data-stu-id="cce60-229">Transaction 2</span></span></td>
<td><span data-ttu-id="cce60-230"><strong>مبلغ الحركة:</strong> 5,000.00<strong>التمويل:</strong> يتم دفع الحركة وفقًا لكافة القواعد الثلاثة.<strong>القاعدة 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="cce60-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.<strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="cce60-231">مصدر التمويل 2: 450.00</span><span class="sxs-lookup"><span data-stu-id="cce60-231">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="cce60-232">مصدر التمويل 3: 450.00</span><span class="sxs-lookup"><span data-stu-id="cce60-232">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="cce60-233">
<strong>القاعدة 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="cce60-233">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="cce60-234">مصدر التمويل 3: 250.00 (= 750.00 – 50.00 – 450.00)</span><span class="sxs-lookup"><span data-stu-id="cce60-234">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="cce60-235">
<strong>القاعدة 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="cce60-235">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="cce60-236">مصدر التمويل 1: 3850.00 (= 5000.00 – 450.00 – 450.00 – 250.00)</span><span class="sxs-lookup"><span data-stu-id="cce60-236">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cce60-237">مجموع الأموال التي يتم توزيعها لكل مصدر من مصادر التمويل</span><span class="sxs-lookup"><span data-stu-id="cce60-237">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="cce60-238">مصدر التمويل 1: 3850.00</span><span class="sxs-lookup"><span data-stu-id="cce60-238">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="cce60-239">مصدر التمويل 2: 500.00</span><span class="sxs-lookup"><span data-stu-id="cce60-239">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="cce60-240">مصدر التمويل 3: 750.00</span><span class="sxs-lookup"><span data-stu-id="cce60-240">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="cce60-241">قواعد الفوترة</span><span class="sxs-lookup"><span data-stu-id="cce60-241">Billing rules</span></span>
<span data-ttu-id="cce60-242">عند التفاوض على عقد مشروع مع أحد العملاء، تقوم بتحديد كيف ومتى يمكنك فوترة العميل للعمل المنفَّذ بإحدى المشروعات.</span><span class="sxs-lookup"><span data-stu-id="cce60-242">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="cce60-243">وبعد إعداد عقد المشروع والمشروع، يمكنك إعداد قواعد الفوترة للمشروع.</span><span class="sxs-lookup"><span data-stu-id="cce60-243">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="cce60-244">تستند قواعد الفوترة إلى شروط المشروع المحددة في عقد المشروع.</span><span class="sxs-lookup"><span data-stu-id="cce60-244">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="cce60-245">تعتمد قواعد الفوترة التي يمكنك إنشاؤها على الشروط الموجودة في عقد المشروع ونوع المشروع -مثل الوقت والمواد أو السعر الثابت- والذي تقوم بإقرانه بقاعدة الفوترة.</span><span class="sxs-lookup"><span data-stu-id="cce60-245">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="cce60-246">يمكنك إنشاء أكثر من قاعدة فوترة لعقد مشروع.</span><span class="sxs-lookup"><span data-stu-id="cce60-246">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="cce60-247">يمكنك أيضًا تعيين قاعدة فوترة لمشروعات متعددة مقترنة بنفس عقد المشروع ولها شروط فوترة مماثلة.</span><span class="sxs-lookup"><span data-stu-id="cce60-247">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="cce60-248">ويمكنك إعداد أنواع قواعد الفوترة التالية:</span><span class="sxs-lookup"><span data-stu-id="cce60-248">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="cce60-249">**وحدة التسليم** – فاتورة عميل عند إتمام وحدة تسليم.</span><span class="sxs-lookup"><span data-stu-id="cce60-249">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="cce60-250">تُحدد وحدات التسليم في العقد.</span><span class="sxs-lookup"><span data-stu-id="cce60-250">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="cce60-251">**التقدم** – فوترة العميل عند إكمال نسبة محددة من المشروع.</span><span class="sxs-lookup"><span data-stu-id="cce60-251">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="cce60-252">يمكنك إعداد قاعدة فوترة لحساب النسبة المئويةللعمل المكتمل تلقائيًا، أو يمكنك يدويًا حساب النسبة المئوية للعمل المكتمل والمبلغ لفوترة العميل.</span><span class="sxs-lookup"><span data-stu-id="cce60-252">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="cce60-253">**المرحلة الرئيسية** - فوترة عميل للمبلغ الكامل للمرحلة الرئيسية للمشروع عند الوصول إلى المرحلة الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="cce60-253">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="cce60-254">**الرسوم** - فوترة العميل عن الخدمات بالإضافة إلى الرسم الإداري، الذي عادةً ما يكون نسبة مئوية من تكاليف الخدمات.</span><span class="sxs-lookup"><span data-stu-id="cce60-254">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="cce60-255">**الوقت والمواد** – فوترة العميل عن قيمة الوقت والمواد المستخدمة في مشروع.</span><span class="sxs-lookup"><span data-stu-id="cce60-255">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="cce60-256">لكل أنواع قواعد الفوترة، يمكنك تحديد النسبة المئوية للاحتفاظ للخصم من فواتير العملاء حتى يبلغ المشروع المرحلة المتفق عليها.</span><span class="sxs-lookup"><span data-stu-id="cce60-256">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="cce60-257">يتم تحديد النسبة المئوية للاحتفاظ من المدفوعات في عقد المشروع.</span><span class="sxs-lookup"><span data-stu-id="cce60-257">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="cce60-258">ويتم حساب المبلغ وطرحه من القيمة الإجمالية للبنود في فاتورة عميل.</span><span class="sxs-lookup"><span data-stu-id="cce60-258">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="cce60-259">وفي قواعد فوترة **الوقت والمواد** و**التقدم**، يمكنك تعيين الفئات الخاضعة للرسوم.</span><span class="sxs-lookup"><span data-stu-id="cce60-259">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="cce60-260">تشير الفئات الخاضعة للرسوم للحركات التي يجب تضمينها في فواتير العميل.</span><span class="sxs-lookup"><span data-stu-id="cce60-260">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="cce60-261">عندما تكون مستعدًا لفوترة العميل، يتم حساب مبلغ الفاتورة للمشروع بناءً على قواعد الفوترة، ويتم إنشاء مقترح فاتورة مشروع.</span><span class="sxs-lookup"><span data-stu-id="cce60-261">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="cce60-262">توفر الأقسام التالية أمثلة لتوضيح كيفية إعداد قواعد فوترة لمشروع وإدارتها.</span><span class="sxs-lookup"><span data-stu-id="cce60-262">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="cce60-263">مثال: إنشاء قاعدة فوترة استنادًا إلى عدد الوحدات التي تم تسليمها</span><span class="sxs-lookup"><span data-stu-id="cce60-263">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="cce60-264">تُبرم المؤسسة اتفاقية لتوفير ما مجموعة خمس دورات تدريبية لموظفين العميل بتكلفة قدرها 10000 لكل دورة تدريبية.</span><span class="sxs-lookup"><span data-stu-id="cce60-264">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="cce60-265">تقوم بفوترة العميل في نهاية كل جلسة تدريب.</span><span class="sxs-lookup"><span data-stu-id="cce60-265">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="cce60-266">وعند إعداد قواعد الفوترة للعقد، تستخدم القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="cce60-266">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="cce60-267">وحدة التسليم هي جلسة تدريب واحدة.</span><span class="sxs-lookup"><span data-stu-id="cce60-267">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="cce60-268">سعر الوحدة هو 10000 لكل جلسة تدريب.</span><span class="sxs-lookup"><span data-stu-id="cce60-268">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="cce60-269">العدد الإجمالي للوحدات هو خمس جلسات تدريب.</span><span class="sxs-lookup"><span data-stu-id="cce60-269">The total number of units is five training sessions.</span></span>

<span data-ttu-id="cce60-270">عند الانتهاء من جلسة تدريب واحدة، يمكنك إنشاء فاتورة بقيمة 10000 للوحدة الأولى التي تم تسليمها، وإرسال الفاتورة إلى العميل.</span><span class="sxs-lookup"><span data-stu-id="cce60-270">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="cce60-271">مثال: إنشاء قاعدة فوترة استنادًا إلى نسبة مئوية محددة من إتمام المشروع (الحساب اليدوي)</span><span class="sxs-lookup"><span data-stu-id="cce60-271">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="cce60-272">تٌبرم المؤسسة وهي شركة استشارات برمجية اتفاقًا مع أحد العملاء لتطوير جزء من المنتج الذي يعمل العميل على تطويره.</span><span class="sxs-lookup"><span data-stu-id="cce60-272">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="cce60-273">وتوافق مؤسستك على تسليم الكود البرمجي الخاص بالمنتج على مدى فترة من ستة أشهر.</span><span class="sxs-lookup"><span data-stu-id="cce60-273">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="cce60-274">يوافق العميل على دفع مبلغ إجمالي بقيمة 100000 لمؤسستك مقابل العمل المنفَّذ.</span><span class="sxs-lookup"><span data-stu-id="cce60-274">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="cce60-275">يمكنك إنشاء قاعدة فوترة لفوترة العميل استنادًا إلى النسبة مئوية للعمل المنفَّذ في المشروع كما هو محدد في العقد.</span><span class="sxs-lookup"><span data-stu-id="cce60-275">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="cce60-276">في نهاية الشهر الأول، تعقد اجتماعًا مع العميل لتحديد النسبة المئوية للعمل المنفَّذ.</span><span class="sxs-lookup"><span data-stu-id="cce60-276">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="cce60-277">وبعد قيامك والعميل بمراجعة المشروع، تقرر أن المشروع قد اكتمل بنسة 15 بالمائة.</span><span class="sxs-lookup"><span data-stu-id="cce60-277">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="cce60-278">تقوم بإنشاء فاتورة بمبلغ 15000 (15 في المائة من 100000) وإرسالها إلى العميل.</span><span class="sxs-lookup"><span data-stu-id="cce60-278">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="cce60-279">مثال: إنشاء قاعدة فوترة استنادًا إلى نسبة مئوية محددة من إتمام المشروع (الحساب التلقائي)</span><span class="sxs-lookup"><span data-stu-id="cce60-279">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="cce60-280">وتوافق مؤسستك، وهي شركة تطوير برامج، على تطوير حزمة محاسبة رواتب لعميل بمبلغ 30000.</span><span class="sxs-lookup"><span data-stu-id="cce60-280">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="cce60-281">يوافق العميل على الدفع لمؤسستك على أساس النسبة المئوية للعمل المنفَّذ.</span><span class="sxs-lookup"><span data-stu-id="cce60-281">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="cce60-282">تقدِّر تكاليف المشروع بقيمة 20000.</span><span class="sxs-lookup"><span data-stu-id="cce60-282">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="cce60-283">ويحدد عقد المشروع فئات العمل لاستخدامها في عملية الفوترة.</span><span class="sxs-lookup"><span data-stu-id="cce60-283">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="cce60-284">وتقوم بإعداد قواعد الفوترة التي تقوم بحساب مبالغ الفاتورة تلقائيًا لنسبة العمل التي تم إكمالها لكل فئة.</span><span class="sxs-lookup"><span data-stu-id="cce60-284">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="cce60-285">تقوم بإعداد موازنة لكل فئة:</span><span class="sxs-lookup"><span data-stu-id="cce60-285">You set up a budget for each category:</span></span>

-   <span data-ttu-id="cce60-286">**التطوير** – تبلغ التكلفة 15000 والإيرادات 20000.</span><span class="sxs-lookup"><span data-stu-id="cce60-286">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="cce60-287">**التركيب** – تبلغ التكلفة 5000 والإيرادات 10000</span><span class="sxs-lookup"><span data-stu-id="cce60-287">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="cce60-288">عند إنشاء فاتورة عميل لأول مرة، يتم حساب مبلغ الفاتورة تلقائيًا استنادًا إلى المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="cce60-288">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="cce60-289">بعد شهر، يقدم العامل بالمشروع جدولاً زمنيًا للمشروع.</span><span class="sxs-lookup"><span data-stu-id="cce60-289">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="cce60-290">تكلفة ساعات العامل 5000 للتطوير و1000 للتركيب.</span><span class="sxs-lookup"><span data-stu-id="cce60-290">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="cce60-291">اكتملت أعمال التطوير بنسبة 33 بالمائة (تبلغ التكلفة الفعلية 5000، وتكلفة الموازنة 15000)، بينما اكتملت أعمال التركيب بنسبة 20 بالمائة (تبلغ التكلفة الفعلية 1000، وتكلفة الموازنة 5000).</span><span class="sxs-lookup"><span data-stu-id="cce60-291">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="cce60-292">تم حساب مبلغ الفاتورة بقيمة 8667 تلقائيًا (33 بالمائة من 20000 + 20 بالمائة من 10000).</span><span class="sxs-lookup"><span data-stu-id="cce60-292">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="cce60-293">تقوم بإنشاء فاتورة بمبلغ 8667 وإرسالها إلى العميل.</span><span class="sxs-lookup"><span data-stu-id="cce60-293">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="cce60-294">مثال: إنشاء قاعدة فوترة استنادًا إلى المراحل الرئيسية المتفق عليها</span><span class="sxs-lookup"><span data-stu-id="cce60-294">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="cce60-295">توافق مؤسستك، وهي شركة استشارات إدارية، على إجراء بحث للسوق حول منتج استهلاكي ينوي العميل بيعه.</span><span class="sxs-lookup"><span data-stu-id="cce60-295">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="cce60-296">يوافق العميل على الاستعانة بخدماتك لمدة ثلاثة شهور، ابتداءً من مارس، ويوافق على دفع مبلغ 50000 لمؤسستك.</span><span class="sxs-lookup"><span data-stu-id="cce60-296">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="cce60-297">يتكون المشروع من ثلاث مراحل رئيسية:</span><span class="sxs-lookup"><span data-stu-id="cce60-297">The project has three milestones:</span></span>

-   <span data-ttu-id="cce60-298">المرحلة الرئيسية الأولى: تجميع بيانات المستهلك – 31 مارس</span><span class="sxs-lookup"><span data-stu-id="cce60-298">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="cce60-299">المرحلة الرئيسية الثانية: تحليل بيانات المستهلك – 30 أبريل</span><span class="sxs-lookup"><span data-stu-id="cce60-299">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="cce60-300">المرحلة الرئيسية الثالثة: تقديم اقتراح بنسبة نجاح المنتج – 31 مايو</span><span class="sxs-lookup"><span data-stu-id="cce60-300">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="cce60-301">يوافق العميل على دفع مبلغ 10000 للمؤسسة عن المرحلة الرئيسية الأولى و20000 للمرحلتين الثانية والثالثة.</span><span class="sxs-lookup"><span data-stu-id="cce60-301">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="cce60-302">عند إعداد عقد المشروع، توافق على فوترة العميل استنادًا إلى المرحلة الرئيسية المكتملة.</span><span class="sxs-lookup"><span data-stu-id="cce60-302">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="cce60-303">يتضمن إعداد قاعدة الفوترة الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="cce60-303">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="cce60-304">تحديد المراحل الرئيسية للمشروع.</span><span class="sxs-lookup"><span data-stu-id="cce60-304">Define the project milestones.</span></span>
-   <span data-ttu-id="cce60-305">قم بتحديد مبلغ فوترة العميل عند إتمام كل مرحلة رئيسية.</span><span class="sxs-lookup"><span data-stu-id="cce60-305">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="cce60-306">عند اكتمال المرحلة الرئيسية الأولى في 31 مارس، قم بوضع علامة على المرحلة الرئيسية كمكتملة، ثم قم بإنشاء فاتورة بمبلغ 10000 لإرسالها للعميل.</span><span class="sxs-lookup"><span data-stu-id="cce60-306">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="cce60-307">ولا يمكنك إنشاء فاتورة لمرحلة رئيسية حتى تقوم بوضع علامة على المرحلة الرئيسية على أنها مكتملة.</span><span class="sxs-lookup"><span data-stu-id="cce60-307">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="cce60-308">مثال: إنشاء قاعدة فوترة استنادًا إلى الخدمات بالإضافة إلى الرسوم الإدارية</span><span class="sxs-lookup"><span data-stu-id="cce60-308">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="cce60-309">توافق مؤسستك، وهي شركة استشارات إدارة، على إجراء أبحاث السوق لتقييم جدوى منتج يقوم العميل، وهو شركة 
بيع بالتجزئة، بتطويره.</span><span class="sxs-lookup"><span data-stu-id="cce60-309">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="cce60-310">وتنص شروط الاتفاقية على أنك ستقدم خدمات أكفأ ثلاثة استشاريين إداريين سيقومون بإجراء البحث على أساس الوقت والمواد.</span><span class="sxs-lookup"><span data-stu-id="cce60-310">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="cce60-311">كما يوافق العميل أيضًا على دفع 100 لكل ساعة، بالإضافة إلى أي رسوم إدارية أخرى تبلغ 10 بالمائة مقابل ساعات الاستشارات التي تتم إضافة تكلفتها إلى المشروع.</span><span class="sxs-lookup"><span data-stu-id="cce60-311">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="cce60-312">وعند إعداد عقد المشروع، قم بإنشاء قاعدة فوترة لإضافة رسم إداري بنسبة 10 بالمائة إلى ساعات الاستشارات التي تتم إضافتها تكلفتها للمشروع.</span><span class="sxs-lookup"><span data-stu-id="cce60-312">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="cce60-313">عند إنشاء فاتورة للعميل، يتم فوترة العميل برسم إداري بنسبة 10 بالمائة، بالإضافة إلى تكلفة ساعات الاستشارات.</span><span class="sxs-lookup"><span data-stu-id="cce60-313">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="cce60-314">على سبيل المثال، إذا عمل الاستشاريين الثلاثة لمدة 200 ساعة بالمشروع، يتم إنشاء فاتورة تبلغ 22000 باستخدام الحساب التالي:</span><span class="sxs-lookup"><span data-stu-id="cce60-314">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="cce60-315">200 ساعة بمبلغ 100 لكل ساعة = 20000</span><span class="sxs-lookup"><span data-stu-id="cce60-315">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="cce60-316">رسوم إدارية بنسبة 10 بالمائة = 2000</span><span class="sxs-lookup"><span data-stu-id="cce60-316">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="cce60-317">إجمالي مبلغ الفاتورة = 22000</span><span class="sxs-lookup"><span data-stu-id="cce60-317">Total invoice amount = 22,000</span></span>

<span data-ttu-id="cce60-318">إذا كانت الرسوم خاضعة للضريبة بالنسبة لعميل، وقمت بتحديد مجموعة ضريبة مبيعات في عقد المشروع، فيتم إدخال مجموعة ضريبة المبيعات تلقائيًا في قاعدة فوترة الرسوم.</span><span class="sxs-lookup"><span data-stu-id="cce60-318">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="cce60-319">مثال: إنشاء قاعدة فوترة لقيمة الوقت والمواد</span><span class="sxs-lookup"><span data-stu-id="cce60-319">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="cce60-320">وتوافق مؤسستك، وهي شركة استشارات برمجية، على توفير خمسة مستشارين فنيين للعمل في مشروع تطوير برامج لأحد العملاء للخمسة أشهر القادمة.</span><span class="sxs-lookup"><span data-stu-id="cce60-320">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="cce60-321">يوافق العميل على سداد 150 لكل ساعة استشارية وتكلفة ‏‫التجهيزات المكتبية‬.</span><span class="sxs-lookup"><span data-stu-id="cce60-321">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="cce60-322">ترسل مؤسستك فاتورة إلى العميل في نهاية كل شهر.</span><span class="sxs-lookup"><span data-stu-id="cce60-322">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="cce60-323">عند إعداد عقد المشروع، توافق على فوترة العميل شهريًا استنادًا إلى الوقت والمواد المستخدمة في المشروع.</span><span class="sxs-lookup"><span data-stu-id="cce60-323">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="cce60-324">يمكنك إنشاء قاعدة فوترة تتضمن المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="cce60-324">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="cce60-325">الفترة الزمنية للعقد ستة أشهر.</span><span class="sxs-lookup"><span data-stu-id="cce60-325">The contract period is six months.</span></span>
-   <span data-ttu-id="cce60-326">يتم حساب وقت الاستشارات بمعدل 150 بالساعة.</span><span class="sxs-lookup"><span data-stu-id="cce60-326">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="cce60-327">تتم فوترة التجهيزات المكتبية بتكلفة، والتكلفة الإجمالية للمشروع لا تتجاوز 10000 للمشروع.</span><span class="sxs-lookup"><span data-stu-id="cce60-327">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="cce60-328">تقوم بإنشاء فاتورة للعميل في نهاية كل شهر تقويمي أثناء المشروع.</span><span class="sxs-lookup"><span data-stu-id="cce60-328">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="cce60-329">خلال الشهر الأول، يسجِّل الاستشاريون إجمالي 800 ساعة بالمشروع.</span><span class="sxs-lookup"><span data-stu-id="cce60-329">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="cce60-330">تكلفة التجهيزات المكتبية التي يتم تحميلها للمشروع 2000.</span><span class="sxs-lookup"><span data-stu-id="cce60-330">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="cce60-331">ولذلك، في نهاية الشهر، يمكنك إنشاء فاتورة بقيمة 122000، محسوبة كعدد 800 ساعة بسعر 150 لكل ساعة، بالإضافة إلى مبلغ 2000 للتجهيزات المكتبية.</span><span class="sxs-lookup"><span data-stu-id="cce60-331">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>




