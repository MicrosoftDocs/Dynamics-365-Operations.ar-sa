---
title: قواعد سياسة التدقيق
description: يمكنك استخدام سياسات التدقيق لتقييم تقارير المصروفات، وفواتير المورد، وأوامر الشراء للتأكد من امتثالها لقواعد السياسة التي تقوم بإنشائها. يتم تشغيل كل القواعد المقترنة بسياسة التدقيق في الوضع الدفعي، ووفقا للجدول الزمني الذي تحدده.  كل قاعدة سياسة هي مثال على نوع قاعدة السياسة. لكل نوع قاعدة السياسة، يمكن تنشيط قاعدة سياسة واحدة فقط في المرة الواحدة.
author: panolte
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.custom: 12991
ms.assetid: 8d787017-71dc-418f-b8c2-4ea9763d9978
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 998d4dbabec74528b4acb9e797faef0c449e7c28
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021231"
---
# <a name="audit-policy-rules"></a><span data-ttu-id="1fabc-106">قواعد سياسة التدقيق</span><span class="sxs-lookup"><span data-stu-id="1fabc-106">Audit policy rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1fabc-107">يمكنك استخدام سياسات التدقيق لتقييم تقارير المصروفات، وفواتير المورد، وأوامر الشراء للتأكد من امتثالها لقواعد السياسة التي تقوم بإنشائها.</span><span class="sxs-lookup"><span data-stu-id="1fabc-107">You can use audit policies to evaluate expense reports, vendor invoices, and purchase orders to make sure that they comply with policy rules that you create.</span></span> <span data-ttu-id="1fabc-108">يتم تشغيل كل القواعد المقترنة بسياسة التدقيق في الوضع الدفعي، ووفقا للجدول الزمني الذي تحدده.</span><span class="sxs-lookup"><span data-stu-id="1fabc-108">All of the rules that are associated with an audit policy are run in batch mode, according to a schedule that you specify.</span></span>  <span data-ttu-id="1fabc-109">كل قاعدة سياسة هي مثال على نوع قاعدة السياسة.</span><span class="sxs-lookup"><span data-stu-id="1fabc-109">Each policy rule is an instance of a policy rule type.</span></span> <span data-ttu-id="1fabc-110">لكل نوع قاعدة السياسة، يمكن تنشيط قاعدة سياسة واحدة فقط في المرة الواحدة.</span><span class="sxs-lookup"><span data-stu-id="1fabc-110">For each policy rule type, only one policy rule can be active at a time.</span></span> 

<a name="queries-and-query-types"></a><span data-ttu-id="1fabc-111">الاستعلامات وأنواع الاستعلامات</span><span class="sxs-lookup"><span data-stu-id="1fabc-111">Queries and query types</span></span>
-----------------------

<span data-ttu-id="1fabc-112">عند إنشاء قاعدة سياسة تدقيق، يجب أولاً تحديد نوع قاعدة السياسة.</span><span class="sxs-lookup"><span data-stu-id="1fabc-112">When you create an audit policy rule, you first select a policy rule type.</span></span> <span data-ttu-id="1fabc-113">نوع قاعدة السياسة يحدد أي من استعلامات ‏‫شجرة مكونات البرنامج‬ (AOT) وسيتم استخدامه كنقطة بداية لإنشاء قاعدة السياسة.</span><span class="sxs-lookup"><span data-stu-id="1fabc-113">The policy rule type specifies the Application Object Tree (AOT) query to use as the starting point for creating the policy rule.</span></span> <span data-ttu-id="1fabc-114">كما يحدد نوع الاستعلام ﻻستخدامه في قاعدة السياسة أيضا.</span><span class="sxs-lookup"><span data-stu-id="1fabc-114">It also specifies the query type to use for the policy rule.</span></span> <span data-ttu-id="1fabc-115">يشير هذا الاستعلام إلى مستند المصدر الذي تم تعريف نوع قاعدة السياسة له.</span><span class="sxs-lookup"><span data-stu-id="1fabc-115">The query determines the source document that the policy rule evaluates.</span></span> <span data-ttu-id="1fabc-116">أيضا يعين الحقول في مستند المصدر التي تقوم بتعريف كل من الكيان القانوني والتاريخ المطلوب استخدامه للتدقيق في الوثائق المحددة.</span><span class="sxs-lookup"><span data-stu-id="1fabc-116">It also specifies the fields in the source document that identify both the legal entity and the date to use when documents are selected for audit.</span></span> <span data-ttu-id="1fabc-117">يتحكم نوع الاستعلام في الحقول الافتراضية في صفحة الاستعلام وفي صفحة قاعدة سياسة التدقيق.</span><span class="sxs-lookup"><span data-stu-id="1fabc-117">The query type controls the default fields in the query page and in the Audit policy rule page.</span></span> <span data-ttu-id="1fabc-118">يسرد الجدول التالي أنواع الاستعلامات المتاحة لسياسة التدقيق.</span><span class="sxs-lookup"><span data-stu-id="1fabc-118">The following table shows the query types that are available for audit policy rules.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1fabc-119">نوع الاستعلام</span><span class="sxs-lookup"><span data-stu-id="1fabc-119">Query type</span></span></th>
<th><span data-ttu-id="1fabc-120">الغرض</span><span class="sxs-lookup"><span data-stu-id="1fabc-120">Purpose</span></span></th>
<th><span data-ttu-id="1fabc-121">معلومات إضافية</span><span class="sxs-lookup"><span data-stu-id="1fabc-121">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1fabc-122">مشروط</span><span class="sxs-lookup"><span data-stu-id="1fabc-122">Conditional</span></span></td>
<td><span data-ttu-id="1fabc-123">تقييم سمات مستند المصدر مقابل قيم معينة.</span><span class="sxs-lookup"><span data-stu-id="1fabc-123">Evaluate source document attributes against specified values.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fabc-124">مجمَّع</span><span class="sxs-lookup"><span data-stu-id="1fabc-124">Aggregate</span></span></td>
<td><span data-ttu-id="1fabc-125">تقييم مستندات المصادر المتعددة أو سطور مستند المصدر مقابل قاعدة سياسة متعددة بتجميع قيم رقمية.</span><span class="sxs-lookup"><span data-stu-id="1fabc-125">Evaluate multiple source documents or source document lines against a policy rule by aggregating numeric values.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fabc-126">أخذ عينات</span><span class="sxs-lookup"><span data-stu-id="1fabc-126">Sampling</span></span></td>
<td><span data-ttu-id="1fabc-127">حدد نسبة مئوية محددة من مستندات المصدر لتقييم انتهاكات السياسات عشوائياً.</span><span class="sxs-lookup"><span data-stu-id="1fabc-127">Randomly select a specified percentage of the source documents to evaluate for policy violations.</span></span></td>
<td><span data-ttu-id="1fabc-128">عند تحديد هذا الخيار، استخدم صفحة قاعدة سياسة التدقيق لتحديد النسبة المئوية للوثائق المُختارة عشوائياً للتدقيق.</span><span class="sxs-lookup"><span data-stu-id="1fabc-128">When you select this option, use the Audit policy rule page to specify the percentage of documents to randomly select for audit.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fabc-129">مكرر</span><span class="sxs-lookup"><span data-stu-id="1fabc-129">Duplicate</span></span></td>
<td><span data-ttu-id="1fabc-130">تقييم مستندات المصدر لتحديد ما إذا كانت تحتوي على إدخالات مكررة في الحقول المحددة.</span><span class="sxs-lookup"><span data-stu-id="1fabc-130">Evaluate source documents to determine whether they contain duplicate entries in specified fields.</span></span></td>
<td><span data-ttu-id="1fabc-131">عند تحديد هذا الخيار، استخدم صفحة قاعدة سياسة التدقيق لتحديد عدد الأيام المطلوب إضافتها إلى بداية نطاق تاريخ تحديد المستند، عندما يتم تقييم المستندات لإدخالات مكررة.</span><span class="sxs-lookup"><span data-stu-id="1fabc-131">When you select this option, use the Audit policy rule page to specify the number of days to add to the start of the document selection date range when documents are evaluated for duplicate entries.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fabc-132">بحث عن قائمة</span><span class="sxs-lookup"><span data-stu-id="1fabc-132">List search</span></span></td>
<td><span data-ttu-id="1fabc-133">تقييم مستندات المصدر لكيانات محددة.</span><span class="sxs-lookup"><span data-stu-id="1fabc-133">Evaluate source documents for specific entities.</span></span></td>
<td><span data-ttu-id="1fabc-134">وتقوم وثيقة الجذر للاستعلام بتحديد المستند الذي يتم تدقيقه.</span><span class="sxs-lookup"><span data-stu-id="1fabc-134">The root document of the query defines the document that is being audited.</span></span> <span data-ttu-id="1fabc-135">يجب أن يكون الاستعلام استعلام قائمة يتضمن مرجعًا إلى الجدول dirpartytable.</span><span class="sxs-lookup"><span data-stu-id="1fabc-135">The query must be a list query that includes a reference to the dirpartytable table.</span></span> <span data-ttu-id="1fabc-136">يمكن استخدام هذا الخيار فقط مع استعلامات AOT:</span><span class="sxs-lookup"><span data-stu-id="1fabc-136">This option can be used only with the following AOT queries:</span></span>
<ul>
<li><span data-ttu-id="1fabc-137"><span class="ui">AuditPolicyExpenseList</span> (الموظفون المراقبون بتقرير المصروفات)</span><span class="sxs-lookup"><span data-stu-id="1fabc-137"><span class="ui">AuditPolicyExpenseList</span> (Expense report monitored employees)</span></span></li>
<li><span data-ttu-id="1fabc-138"><span class="ui">AuditPolicyPurchList</span> (الموردون المراقبون في أمر الشراء)</span><span class="sxs-lookup"><span data-stu-id="1fabc-138"><span class="ui">AuditPolicyPurchList</span> (Purchase order monitored vendors)</span></span></li>
<li><span data-ttu-id="1fabc-139"><span class="ui">AuditPolicyVendInvoiceList</span> (الموردون المراقبون في فاتورة المورد)</span><span class="sxs-lookup"><span data-stu-id="1fabc-139"><span class="ui">AuditPolicyVendInvoiceList</span> (Vendor invoice monitored vendors)</span></span></li>
</ul>
<span data-ttu-id="1fabc-140">عند تحديد هذا الخيار، حدد الكيانات المُراقبَّة في صفحة قاعدة سياسة التدقيق.</span><span class="sxs-lookup"><span data-stu-id="1fabc-140">When you select this option, specify the monitored entities in the Audit policy rule page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fabc-141">بحث بالكلمة الأساسية</span><span class="sxs-lookup"><span data-stu-id="1fabc-141">Keyword search</span></span></td>
<td><span data-ttu-id="1fabc-142">تقييم مستندات المصدر لتحديد ما إذا كانت تحتوي على كلمات معينة.</span><span class="sxs-lookup"><span data-stu-id="1fabc-142">Evaluate source documents to determine whether they contain certain words.</span></span></td>
<td><span data-ttu-id="1fabc-143">عند تحديد هذا الخيار، أدخل الكلمات للبحث عنها في صفحة قاعدة سياسة التدقيق.</span><span class="sxs-lookup"><span data-stu-id="1fabc-143">When you select this option, enter the words to look for in the Audit policy rule page.</span></span> <span data-ttu-id="1fabc-144">كما تتضمن صفحة قاعدة سياسة التدقيق الخيارات التي تسمح لك بتحديد الجداول والحقول لتقييم الكلمات التي أدخلتها.</span><span class="sxs-lookup"><span data-stu-id="1fabc-144">The Audit policy rule page also includes options that let you specify the tables and fields to evaluate for the words you entered.</span></span></td>
</tr>
</tbody>
</table>

## <a name="common-parameters"></a><span data-ttu-id="1fabc-145">معلمات شائعة:</span><span class="sxs-lookup"><span data-stu-id="1fabc-145">Common parameters</span></span>
<span data-ttu-id="1fabc-146">كل قواعد السياسة الخاصة بسياسة تدقيق معينة تتشارك في نفس معلمات الدُفعة ونفس نطاق تاريخ تحديد المستند نفسه.</span><span class="sxs-lookup"><span data-stu-id="1fabc-146">All of the policy rules for a particular audit policy share the same batch parameters and the same document selection date range.</span></span> <span data-ttu-id="1fabc-147">هذه المعلمات محددة للسياسة في صفحة الخيارات الإضافية.</span><span class="sxs-lookup"><span data-stu-id="1fabc-147">These parameters are specified for the policy in the Additional options page.</span></span>



<a name="additional-resources"></a><span data-ttu-id="1fabc-148">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="1fabc-148">Additional resources</span></span>
--------

<span data-ttu-id="1fabc-149">[تدقيق انتهاكات السياسة والحالات](audit-policy-violations-cases.md)
[تحديد سياسات التدقيق‬ للمستندات المصدر](tasks/define-audit-policies-source-documents.md)</span><span class="sxs-lookup"><span data-stu-id="1fabc-149">[Audit policy violations and cases](audit-policy-violations-cases.md)
[Define audit policies for source documents](tasks/define-audit-policies-source-documents.md)</span></span>


