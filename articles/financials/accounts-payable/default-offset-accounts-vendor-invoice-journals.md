---
title: "الحسابات المقابلة الافتراضية لدفاتر يومية فواتير المورد ودفاتر يومية اعتماد الفاتورة"
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c2b62eafc71b5d1ad4eaaf252efd1dcbb97b86f3
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---

# <a name="default-offset-accounts-for-vendor-invoice-journals-and-invoice-approval-journals"></a><span data-ttu-id="4c3dd-102">الحسابات المقابلة الافتراضية لدفاتر يومية فواتير المورد ودفاتر يومية اعتماد الفاتورة</span><span class="sxs-lookup"><span data-stu-id="4c3dd-102">Default offset accounts for vendor invoice journals and invoice approval journals</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="4c3dd-103">يتم استخدام الحسابات المقابلة الافتراضية في صفحات دفاتر يومية فاتورة المورد التالية:</span><span class="sxs-lookup"><span data-stu-id="4c3dd-103">Default offset accounts are used on the following vendor invoice journal pages:</span></span>

-   <span data-ttu-id="4c3dd-104">دفتر يومية الفواتير</span><span class="sxs-lookup"><span data-stu-id="4c3dd-104">Invoice journal</span></span>
-   <span data-ttu-id="4c3dd-105">دفتر يومية الموافقة على الفواتير</span><span class="sxs-lookup"><span data-stu-id="4c3dd-105">Invoice approval journal</span></span>

<span data-ttu-id="4c3dd-106">استخدم الجدول التالي للمساعدة في تحديد مكان تعيين الحسابات الافتراضية لدفاتر يومية الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="4c3dd-106">Use the following table to help decide where you should assign default accounts for invoice journals.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4c3dd-107">قم بإعداد الحسابات الافتراضية هنا</span><span class="sxs-lookup"><span data-stu-id="4c3dd-107">Set up default accounts here</span></span></th>
<th><span data-ttu-id="4c3dd-108">المكان الذي يتم فيه توفير الحسابات الافتراضية</span><span class="sxs-lookup"><span data-stu-id="4c3dd-108">Where default accounts are provided</span></span></th>
<th><span data-ttu-id="4c3dd-109">مدى تأثير هذا الخيار على المعالجة</span><span class="sxs-lookup"><span data-stu-id="4c3dd-109">How this option affects processing</span></span></th>
<th><span data-ttu-id="4c3dd-110">متى يجب استخدام هذا الخيار</span><span class="sxs-lookup"><span data-stu-id="4c3dd-110">When you should use this option</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4c3dd-111"><strong>مجموعة الموردين</strong> – إعداد الحسابات المقابلة الافتراضية لمجموعات الموردين في صفحة <strong>إعداد الحساب الافتراضي</strong>، التي يمكنك فتحها من صفحة <strong>مجموعات الموردين</strong>.</span><span class="sxs-lookup"><span data-stu-id="4c3dd-111"><strong>Vendor group</strong> – Set up default offset accounts for vendor groups on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendor groups</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="4c3dd-112">حساب المورّد</span><span class="sxs-lookup"><span data-stu-id="4c3dd-112">Vendor account</span></span></li>
<li><span data-ttu-id="4c3dd-113">إدخالات دفتر اليومية لحسابات الموردين في مجموعة الموردين، إذا لم يتم تحديد الحسابات الافتراضية لحسابات الموردين</span><span class="sxs-lookup"><span data-stu-id="4c3dd-113">Journal entries for vendor accounts in the vendor group, if default accounts aren’t specified for vendor accounts</span></span></li>
</ul></td>
<td><span data-ttu-id="4c3dd-114">يتم عرض الحسابات المقابلة الافتراضية لمجموعات الموردين باعتبارها الحسابات المقابلة الافتراضية للموردين في صفحة <strong>إعداد الحساب الافتراضي</strong>.</span><span class="sxs-lookup"><span data-stu-id="4c3dd-114">The default offset accounts for vendor groups are shown as default offset accounts for vendors on the <strong>Default account setup</strong> page.</span></span> <span data-ttu-id="4c3dd-115">ويمكنك فتح هذه الصفحة من صفحة قائمة <strong>كافة الموردين</strong>.</span><span class="sxs-lookup"><span data-stu-id="4c3dd-115">You can open this page from the <strong>All vendors</strong> list page.</span></span></td>
<td><span data-ttu-id="4c3dd-116">استخدم هذا الخيار إذا كنت عادةً ما تدفع لنفس أنواع الأشياء من نفس مجموعات الموردين على مر الزمن.</span><span class="sxs-lookup"><span data-stu-id="4c3dd-116">Use this option if you typically pay for the same types of things from the same vendor groups over time.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c3dd-117"><strong>حساب المورد</strong> – إعداد الحسابات الافتراضية لحسابات الموردين في صفحة <strong>إعداد الحساب الافتراضي</strong>، التي يمكنك فتحها من صفحة <strong>الموردين</strong>.</span><span class="sxs-lookup"><span data-stu-id="4c3dd-117"><strong>Vendor account</strong> – Set up default accounts for vendor accounts on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendors</strong> page.</span></span></td>
<td><span data-ttu-id="4c3dd-118">إدخالات دفتر اليومية لحساب المورد</span><span class="sxs-lookup"><span data-stu-id="4c3dd-118">Journal entries for the vendor account</span></span></td>
<td><span data-ttu-id="4c3dd-119">يتم عرض الحسابات المقابلة الافتراضية لحسابات المورد كحسابات مقابلة افتراضية لإدخالات دفتر اليومية لحساب المورد.</span><span class="sxs-lookup"><span data-stu-id="4c3dd-119">The default offset accounts for vendor accounts are shown as default offset accounts for journal entries for the vendor account.</span></span></td>
<td><span data-ttu-id="4c3dd-120">استخدم هذا الخيار إذا كنت عادةً ما تدفع لنفس أنواع الأشياء من نفس الموردين على مر الزمن.</span><span class="sxs-lookup"><span data-stu-id="4c3dd-120">Use this option if you typically pay for the same types of things from the same vendors over time.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c3dd-121"><strong>أسماء دفاتر اليومية</strong> – إعداد الحسابات المقابلة الافتراضية لدفاتر اليومية في صفحة <strong>أسماء دفاتر اليومية</strong>.</span><span class="sxs-lookup"><span data-stu-id="4c3dd-121"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="4c3dd-122">حدد خيار <strong>الحساب المقابل الثابت</strong>.</span><span class="sxs-lookup"><span data-stu-id="4c3dd-122">Select the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="4c3dd-123">لاحظ أنه لا يمكنك تعيين الحسابات المقابلة الافتراضية في أسماء دفاتر اليومية، إذا كان نوع دفتر اليومية لأسماء دفاتر اليومية هو <strong>سجل الفواتير</strong> أو <strong>الموافقة</strong>.</span><span class="sxs-lookup"><span data-stu-id="4c3dd-123">Note that you can't specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="4c3dd-124">حدد رأس دفتر يومية يستخدم اسم دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="4c3dd-124">Journal header that uses the journal name</span></span></li>
<li><span data-ttu-id="4c3dd-125">إدخالات دفتر اليومية في دفاتر اليومية التي تستخدم اسم دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="4c3dd-125">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="4c3dd-126">في حالة تحديد خيار <strong>الحساب المقابل الثابت</strong> في صفحة <strong>أسماء دفاتر اليومية</strong>، يتجاوز الحساب المقابل لاسم دفتر اليومية الحساب المقابل الافتراضي للمورد أو مجموعة الموردين.</span><span class="sxs-lookup"><span data-stu-id="4c3dd-126">If the <strong>Fixed offset account</strong> option on the <strong>Journal names</strong> page is selected, the offset account for the journal name overrides the default offset account for the vendor or vendor group.</span></span></td>
<td><span data-ttu-id="4c3dd-127">استخدم هذا الخيار لإعداد دفاتر اليومية للتكاليف المحددة والمصروفات التي تقيد على حسابات معينة، بغض النظر عمن هو المورد أو مجموعة الموردين التي ينتمي إليها المورد.</span><span class="sxs-lookup"><span data-stu-id="4c3dd-127">Use this option to set up journals for specific costs and expenses that are charged to specific accounts, regardless of the vendor or the vendor group that the vendor belongs to.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c3dd-128"><strong>أسماء دفاتر اليومية</strong> – إعداد الحسابات المقابلة الافتراضية لدفاتر اليومية في صفحة <strong>أسماء دفاتر اليومية</strong>.</span><span class="sxs-lookup"><span data-stu-id="4c3dd-128"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="4c3dd-129">قم بإلغاء تحديد خيار <strong>الحساب المقابل الثابت</strong>.</span><span class="sxs-lookup"><span data-stu-id="4c3dd-129">Clear the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="4c3dd-130">لاحظ أنه لا يمكنك تعيين الحسابات المقابلة الافتراضية في أسماء دفاتر اليومية، إذا كان نوع دفتر اليومية لأسماء دفاتر اليومية هو <strong>سجل الفواتير</strong> أو <strong>الموافقة</strong>.</span><span class="sxs-lookup"><span data-stu-id="4c3dd-130">Note that you can't specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="4c3dd-131">رأس دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="4c3dd-131">Journal header</span></span></li>
<li><span data-ttu-id="4c3dd-132">إدخالات دفتر اليومية في دفاتر اليومية التي تستخدم اسم دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="4c3dd-132">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="4c3dd-133">يتم استخدام هذه الإدخالات الافتراضية في صفحات رأس دفتر اليومية، ويتم استخدام الحساب المقابل في صفحة رأس دفتر اليومية كإدخال افتراضي في صفحات إيصال دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="4c3dd-133">These default entries are used on journal header pages, and the offset account on the journal header page is used as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="4c3dd-134">لا يتم استخدام الحسابات الافتراضية من صفحة <strong>أسماء دفاتر اليومية</strong> إلا إذا لم يتم إعداد الحسابات الافتراضية لحساب المورد.</span><span class="sxs-lookup"><span data-stu-id="4c3dd-134">Default accounts from the <strong>Journal names </strong>page are used only if default accounts aren’t set up for the vendor account.</span></span></td>
<td><span data-ttu-id="4c3dd-135">استخدم هذا الخيار لإعداد حسابات افتراضية التي يتم استخدامها عندما لا يتم تعيين الحساب المقابل الافتراضي للمورد.</span><span class="sxs-lookup"><span data-stu-id="4c3dd-135">Use this option to set up default accounts that are used when a default vendor offset account isn't assigned.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c3dd-136"><strong>رأس دفتر اليومية</strong> – قم بإعداد الحساب المقابل الافتراضي لدفتر يومية كإدخال افتراضي في صفحات إيصال دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="4c3dd-136"><strong>Journal header</strong> – Set up a default offset account for a journal as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="4c3dd-137">لاحظ أنه لا يمكنك تعيين الحسابات المقابلة الافتراضية في رأس دفتر اليومية، إذا كان نوع دفتر اليومية لأسماء دفاتر اليومية هو <strong>سجل الفواتير</strong> أو <strong>الموافقة</strong>.</span><span class="sxs-lookup"><span data-stu-id="4c3dd-137">Note that you can't specify default offset accounts on the journal header if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><span data-ttu-id="4c3dd-138">إدخالات دفتر اليومية في دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="4c3dd-138">Journal entries in the journal</span></span></td>
<td><span data-ttu-id="4c3dd-139">قم بإعداد الحساب المقابل الافتراضي لدفتر يومية مستخدم كإدخال افتراضي في صفحات إيصال دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="4c3dd-139">The default offset account for a journal is used as the default entry on the journal voucher pages.</span></span></td>
<td><span data-ttu-id="4c3dd-140">استخدم هذا الخيار للمساعدة في تسريع إدخال البيانات إذا كان لمعظم الإدخالات في دفتر يومية نفس الحساب المقابل.</span><span class="sxs-lookup"><span data-stu-id="4c3dd-140">Use this option to help speed up data entry if most entries in a journal have the same offset account.</span></span></td>
</tr>
</tbody>
</table>






