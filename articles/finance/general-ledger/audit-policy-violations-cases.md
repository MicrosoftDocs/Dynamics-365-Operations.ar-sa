---
title: تدقيق انتهاكات السياسة والحالات
description: تشرح هذه المقالة كيفية إنشاء حالات التدقيق من انتهاكات قواعد سياسة التدقيق. وتتضمن أيضًا معلومات حول مختلف الطرق التي تتبعها سياسة التدقيق لاستخدام نطاق تاريخ تحديد المستند.
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13091
ms.assetid: e0e66c6d-c396-4a9d-b3b6-3641d130fdc0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d14894d331037033b27fac3fd7ff98c5521eaf98
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439906"
---
# <a name="audit-policy-violations-and-cases"></a><span data-ttu-id="6dba0-104">تدقيق انتهاكات السياسة والحالات</span><span class="sxs-lookup"><span data-stu-id="6dba0-104">Audit policy violations and cases</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6dba0-105">تشرح هذه المقالة كيفية إنشاء حالات التدقيق من انتهاكات قواعد سياسة التدقيق.</span><span class="sxs-lookup"><span data-stu-id="6dba0-105">The article explains how audit cases are generated from violations of audit policy rules.</span></span> <span data-ttu-id="6dba0-106">وتتضمن أيضًا معلومات حول مختلف الطرق التي تتبعها سياسة التدقيق لاستخدام نطاق تاريخ تحديد المستند.</span><span class="sxs-lookup"><span data-stu-id="6dba0-106">It also includes information about the various ways that audit policies use the document selection date range.</span></span>

<a name="how-audit-cases-are-generated"></a><span data-ttu-id="6dba0-107">كيفية إنشاء حالات التدقيق</span><span class="sxs-lookup"><span data-stu-id="6dba0-107">How audit cases are generated</span></span>
-----------------------------

<span data-ttu-id="6dba0-108">يتم استخدام سياسات التدقيق لتحديد تقارير المصروفات، وأوامر الشراء، وفواتير المورد التي لا تتوافق مع قواعد العمل التي تحددها وتكونها كقواعد سياسة تدقيق.</span><span class="sxs-lookup"><span data-stu-id="6dba0-108">Audit policies are used to identify expense reports, purchase orders, and vendor invoices that don't comply with business rules that you define and configure as audit policy rules.</span></span> 

<span data-ttu-id="6dba0-109">ويتم تشغيل سياسات التدقيق في وضع دُفعة.</span><span class="sxs-lookup"><span data-stu-id="6dba0-109">Audit policies are run in batch mode.</span></span> <span data-ttu-id="6dba0-110">وعند تشغيل "سياسة تدقيق"، يتم تشغيل كافة قواعد السياسة التي هي جزء من تلك السياسة في نفس الوقت.</span><span class="sxs-lookup"><span data-stu-id="6dba0-110">When you run an audit policy, all the policy rules that are part of that policy are run at the same time.</span></span>

<span data-ttu-id="6dba0-111">تقوم كل قاعدة سياسة بتقييم مجموعة من المستندات.</span><span class="sxs-lookup"><span data-stu-id="6dba0-111">Each policy rule evaluates a set of documents.</span></span> <span data-ttu-id="6dba0-112">وتحدد قاعدة السياسة المستندات الموجودة في نطاق تاريخ تحديد المستند والتي تتطابق مع المعايير المحددة.</span><span class="sxs-lookup"><span data-stu-id="6dba0-112">The policy rule selects documents that are in the document selection date range and that match the specified criteria.</span></span> <span data-ttu-id="6dba0-113">على سبيل المثال، قد تحدد قاعدة سياسة واحدة تقارير المصروفات التي تشتمل على وجبات تتجاوز مبلغ 50.00.</span><span class="sxs-lookup"><span data-stu-id="6dba0-113">For example, one policy rule might select expense reports that have meals that exceed 50.00.</span></span> <span data-ttu-id="6dba0-114">وقد تحدد قاعدة سياسة أخرى فواتير المورد التي تُدفع لمورد محدد.</span><span class="sxs-lookup"><span data-stu-id="6dba0-114">Another policy rule might select vendor invoices that are payable to a specific vendor.</span></span> <span data-ttu-id="6dba0-115">وبالنسبة لكل مستند محدد في المجموعة، يتم إنشاء انتهاك.</span><span class="sxs-lookup"><span data-stu-id="6dba0-115">For each document that is selected in the set, a violation is generated.</span></span> <span data-ttu-id="6dba0-116">وهذا الانتهاك عبارة عن سجل بأن مستند معين، مثل فاتورة 12345، لا تتوافق مع سياسة القاعدة.</span><span class="sxs-lookup"><span data-stu-id="6dba0-116">That violation is a record that a particular document, such as invoice 12345, doesn't comply with the policy rule.</span></span> 

<span data-ttu-id="6dba0-117">ويتم تجميع سجلات انتهاك التدقيق المتعددة وإقرانها بحالات التدقيق.</span><span class="sxs-lookup"><span data-stu-id="6dba0-117">Multiple audit violation records are grouped together and associated with audit cases.</span></span> <span data-ttu-id="6dba0-118">وبشكل افتراضي، يتم تجميع الحالات لكل سياسة تدقيق حسب قاعدة سياسة التدقيق.</span><span class="sxs-lookup"><span data-stu-id="6dba0-118">By default, cases for each audit policy are grouped by audit policy rule.</span></span> <span data-ttu-id="6dba0-119">وإذا كنت تفضل ذلك، يمكنك تحديد معايير التجميع الأخرى باستخدام صفحة **معايير تجميع الحالات**.</span><span class="sxs-lookup"><span data-stu-id="6dba0-119">If you prefer, you can select other grouping criteria by using the **Case grouping criteria** page.</span></span> <span data-ttu-id="6dba0-120">‏‫على سبيل المثال، يمكنك تجميع رؤوس المصروفات بواسطة فواتير المورد ومعرف المشروع حسب حساب المورد.</span><span class="sxs-lookup"><span data-stu-id="6dba0-120">For example, you can group expense headers by project ID and vendor invoices by vendor account.</span></span> <span data-ttu-id="6dba0-121">وفي هذه الحالة، سيتم تجميع جميع انتهاكات رأس المصروفات التي لها نفس معرف المشروع في نفس الحالة، وسيتم تجميع كافة فواتير المورد المشتملة على حساب المورد نفسه في الحالة نفسها.‬</span><span class="sxs-lookup"><span data-stu-id="6dba0-121">In this case, all expense header violations that have the same project ID will be grouped in the same case, and all vendor invoices that have the same vendor account will be grouped in the same case.</span></span> 

> [!NOTE]
> <span data-ttu-id="6dba0-122">بالنسبة لقواعد سياسة التدقيق التي تستند إلى نوع الاستعلام **المتكرر**، لا يتم تجميع الانتهاكات بواسطة سياسة القاعدة أو المعايير التي تم تحديدها في صفحة **معايير تجميع الحالات**.</span><span class="sxs-lookup"><span data-stu-id="6dba0-122">For audit policy rules that are based on a **Duplicate** query type, violations aren't grouped by policy rule or by the criteria that are specified on the **Case grouping criteria** page.</span></span> <span data-ttu-id="6dba0-123">وبدلاً من ذلك، يتم تجميعها حسب المعايير المضمنة في قاعدة سياسة التدقيق.</span><span class="sxs-lookup"><span data-stu-id="6dba0-123">Instead, they are grouped by the criteria that are built into the audit policy rule.</span></span> <span data-ttu-id="6dba0-124">على سبيل المثال، في حالة قيام قاعدة سياسة بتقييم تقارير المصروفات للمصروفات المتكررة بنفس المبلغ، ومعرف التاجر، والتاريخ، فستكون جميع المصروفات التي لها نفس القيم في تلك الحقول حالة واحدة.</span><span class="sxs-lookup"><span data-stu-id="6dba0-124">For example, if a policy rule evaluates expense reports for duplicate expenses of the same amount, merchant ID, and date, all expenses that have the same values in those fields will be one case.</span></span> <span data-ttu-id="6dba0-125">وستكون أي مصروفات تشتمل على قيم مختلفة حالة منفصلة.</span><span class="sxs-lookup"><span data-stu-id="6dba0-125">Any expenses that have different values will be a separate case.</span></span>

<span data-ttu-id="6dba0-126">بعد أن يتم إنشاء حالات التدقيق، تتم معالجتها باستخدام عمليات نموذجية لإدارة الحالة.</span><span class="sxs-lookup"><span data-stu-id="6dba0-126">After the audit cases have been generated, they are handled by using the typical processes for case management.</span></span>

## <a name="document-selection-date-ranges"></a><span data-ttu-id="6dba0-127">نطاقات تواريخ تحديد المستندات</span><span class="sxs-lookup"><span data-stu-id="6dba0-127">Document selection date ranges</span></span>
<span data-ttu-id="6dba0-128">عند تشغيل سياسة تدقيق، تحديد كل قاعدة سياسة المستندات من النوع المحدد والمشتملة على تاريخ يوجد في نطاق تاريخ تحديد المستندات.</span><span class="sxs-lookup"><span data-stu-id="6dba0-128">When an audit policy is run, each policy rule selects documents of the specified type that have a date that is in the document selection date range.</span></span> <span data-ttu-id="6dba0-129">ويتم تحديد نطاق تاريخ تحديد المستند في صفحة **الخيارات إضافية**.</span><span class="sxs-lookup"><span data-stu-id="6dba0-129">The document selection date range is specified on the **Additional options** page.</span></span> <span data-ttu-id="6dba0-130">وتشتمل العديد من المستندات على أكثر من تاريخ واحد مرتبط بها.</span><span class="sxs-lookup"><span data-stu-id="6dba0-130">Many documents have more than one date associated with them.</span></span> <span data-ttu-id="6dba0-131">ويتم تحديد حقل التاريخ الذي تستخدمه قاعدة سياسة التدقيق في صفحة **نوع قاعدة السياسة**.</span><span class="sxs-lookup"><span data-stu-id="6dba0-131">The date field that the audit policy rule uses is specified on the **Policy rule type** page.</span></span>

<span data-ttu-id="6dba0-132">وفيما يلي بعض الطرق الأخرى التي تستخدم بها سياسة تدقيق نطاق تاريخ تحديد المستند:</span><span class="sxs-lookup"><span data-stu-id="6dba0-132">Here are some other ways that an audit policy uses the document selection date range:</span></span>

-   <span data-ttu-id="6dba0-133">تستخدم السياسة إصدار كل قاعدة سياسة سارية في اليوم الأخير من نطاق تاريخ تحديد المستند.</span><span class="sxs-lookup"><span data-stu-id="6dba0-133">The policy uses the version of each policy rule that is effective on the last day of the document selection date range.</span></span> <span data-ttu-id="6dba0-134">ويمكنك عرض التواريخ الفعالة لكل قاعدة سياسة في صفحة قائمة **سياسات التدقيق**.</span><span class="sxs-lookup"><span data-stu-id="6dba0-134">You can view the effective dates for each policy rule on the **Audit policies** list page.</span></span>
-   <span data-ttu-id="6dba0-135">تستخدم السياسة عقدات المؤسسات المقترنة بالسياسة في اليوم الأخير من نطاق تاريخ تحديد المستند.</span><span class="sxs-lookup"><span data-stu-id="6dba0-135">The policy uses the organization nodes that are associated with the policy on the last day of the document selection date range.</span></span> <span data-ttu-id="6dba0-136">لا تظهر سوى عقدات المؤسسة المقترنة حاليًا بهذه السياسة في صفحة قائمة **سياسات التدقيق**.</span><span class="sxs-lookup"><span data-stu-id="6dba0-136">Only the organization nodes that are currently associated with the policy appear on the **Audit policies** list page.</span></span>
-   <span data-ttu-id="6dba0-137">وبالنسبة لقواعد السياسة التي تستند إلى صفحة استعلام **البحث في قائمة**، تقوم السياسة بتقييم المستندات للكيانات المراقبة التي تكون فعالة في اليوم الأخير من نطاق تاريخ تحديد المستند.</span><span class="sxs-lookup"><span data-stu-id="6dba0-137">For policy rules that are based on a **List search** query type, the policy evaluates documents for monitored entities that are effective on the last day of the document selection date range.</span></span>


<span data-ttu-id="6dba0-138">‏‫لمزيد من المعلومات، راجع [قواعد سياسة التدقيق](audit-policy-rules.md)</span><span class="sxs-lookup"><span data-stu-id="6dba0-138">For more information, see [Audit policy rules](audit-policy-rules.md)</span></span>



