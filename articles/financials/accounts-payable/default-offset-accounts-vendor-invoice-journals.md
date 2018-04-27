---
title: "الحسابات المقابلة الافتراضية لدفاتر يومية فواتير المورد ودفاتر يومية اعتماد الفاتورة"
description: "سيساعدك هذا الموضوع في تحديد مكان تعيين الحسابات الافتراضية لدفاتر يومية الفاتورة."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 90b24e8e00a78c122e0f7c712a694c9c62bd4824
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---

# <a name="default-offset-accounts-for-vendor-invoice-journals-and-invoice-approval-journals"></a><span data-ttu-id="70921-103">الحسابات المقابلة الافتراضية لدفاتر يومية فواتير المورد ودفاتر يومية اعتماد الفاتورة</span><span class="sxs-lookup"><span data-stu-id="70921-103">Default offset accounts for vendor invoice journals and invoice approval journals</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="70921-104">يتم استخدام الحسابات المقابلة الافتراضية في صفحات دفاتر يومية فاتورة المورد التالية:</span><span class="sxs-lookup"><span data-stu-id="70921-104">Default offset accounts are used on the following vendor invoice journal pages:</span></span>

-   <span data-ttu-id="70921-105">دفتر يومية الفواتير</span><span class="sxs-lookup"><span data-stu-id="70921-105">Invoice journal</span></span>
-   <span data-ttu-id="70921-106">دفتر يومية الموافقة على الفواتير</span><span class="sxs-lookup"><span data-stu-id="70921-106">Invoice approval journal</span></span>

<span data-ttu-id="70921-107">استخدم الجدول التالي للمساعدة في تحديد مكان تعيين الحسابات الافتراضية لدفاتر يومية الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="70921-107">Use the following table to help decide where you should assign default accounts for invoice journals.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="70921-108">قم بإعداد الحسابات الافتراضية هنا</span><span class="sxs-lookup"><span data-stu-id="70921-108">Set up default accounts here</span></span></th>
<th><span data-ttu-id="70921-109">المكان الذي يتم فيه توفير الحسابات الافتراضية</span><span class="sxs-lookup"><span data-stu-id="70921-109">Where default accounts are provided</span></span></th>
<th><span data-ttu-id="70921-110">مدى تأثير هذا الخيار على المعالجة</span><span class="sxs-lookup"><span data-stu-id="70921-110">How this option affects processing</span></span></th>
<th><span data-ttu-id="70921-111">متى يجب استخدام هذا الخيار</span><span class="sxs-lookup"><span data-stu-id="70921-111">When you should use this option</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="70921-112"><strong>مجموعة الموردين</strong> – إعداد الحسابات المقابلة الافتراضية لمجموعات الموردين في صفحة <strong>إعداد الحساب الافتراضي</strong>، التي يمكنك فتحها من صفحة <strong>مجموعات الموردين</strong>.</span><span class="sxs-lookup"><span data-stu-id="70921-112"><strong>Vendor group</strong> – Set up default offset accounts for vendor groups on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendor groups</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="70921-113">حساب المورّد</span><span class="sxs-lookup"><span data-stu-id="70921-113">Vendor account</span></span></li>
<li><span data-ttu-id="70921-114">إدخالات دفتر اليومية لحسابات الموردين في مجموعة الموردين، إذا لم يتم تحديد الحسابات الافتراضية لحسابات الموردين</span><span class="sxs-lookup"><span data-stu-id="70921-114">Journal entries for vendor accounts in the vendor group, if default accounts aren’t specified for vendor accounts</span></span></li>
</ul></td>
<td><span data-ttu-id="70921-115">يتم عرض الحسابات المقابلة الافتراضية لمجموعات الموردين باعتبارها الحسابات المقابلة الافتراضية للموردين في صفحة <strong>إعداد الحساب الافتراضي</strong>.</span><span class="sxs-lookup"><span data-stu-id="70921-115">The default offset accounts for vendor groups are shown as default offset accounts for vendors on the <strong>Default account setup</strong> page.</span></span> <span data-ttu-id="70921-116">ويمكنك فتح هذه الصفحة من صفحة قائمة <strong>كافة الموردين</strong>.</span><span class="sxs-lookup"><span data-stu-id="70921-116">You can open this page from the <strong>All vendors</strong> list page.</span></span></td>
<td><span data-ttu-id="70921-117">استخدم هذا الخيار إذا كنت عادةً ما تدفع لنفس أنواع الأشياء من نفس مجموعات الموردين على مر الزمن.</span><span class="sxs-lookup"><span data-stu-id="70921-117">Use this option if you typically pay for the same types of things from the same vendor groups over time.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70921-118"><strong>حساب المورد</strong> – إعداد الحسابات الافتراضية لحسابات الموردين في صفحة <strong>إعداد الحساب الافتراضي</strong>، التي يمكنك فتحها من صفحة <strong>الموردين</strong>.</span><span class="sxs-lookup"><span data-stu-id="70921-118"><strong>Vendor account</strong> – Set up default accounts for vendor accounts on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendors</strong> page.</span></span></td>
<td><span data-ttu-id="70921-119">إدخالات دفتر اليومية لحساب المورد</span><span class="sxs-lookup"><span data-stu-id="70921-119">Journal entries for the vendor account</span></span></td>
<td><span data-ttu-id="70921-120">يتم عرض الحسابات المقابلة الافتراضية لحسابات المورد كحسابات مقابلة افتراضية لإدخالات دفتر اليومية لحساب المورد.</span><span class="sxs-lookup"><span data-stu-id="70921-120">The default offset accounts for vendor accounts are shown as default offset accounts for journal entries for the vendor account.</span></span></td>
<td><span data-ttu-id="70921-121">استخدم هذا الخيار إذا كنت عادةً ما تدفع لنفس أنواع الأشياء من نفس الموردين على مر الزمن.</span><span class="sxs-lookup"><span data-stu-id="70921-121">Use this option if you typically pay for the same types of things from the same vendors over time.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70921-122"><strong>أسماء دفاتر اليومية</strong> – إعداد الحسابات المقابلة الافتراضية لدفاتر اليومية في صفحة <strong>أسماء دفاتر اليومية</strong>.</span><span class="sxs-lookup"><span data-stu-id="70921-122"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="70921-123">حدد خيار <strong>الحساب المقابل الثابت</strong>.</span><span class="sxs-lookup"><span data-stu-id="70921-123">Select the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="70921-124">لاحظ أنه لا يمكنك تعيين الحسابات المقابلة الافتراضية في أسماء دفاتر اليومية، إذا كان نوع دفتر اليومية لأسماء دفاتر اليومية هو <strong>سجل الفواتير</strong> أو <strong>الموافقة</strong>.</span><span class="sxs-lookup"><span data-stu-id="70921-124">Note that you can&#39;t specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="70921-125">حدد رأس دفتر يومية يستخدم اسم دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="70921-125">Journal header that uses the journal name</span></span></li>
<li><span data-ttu-id="70921-126">إدخالات دفتر اليومية في دفاتر اليومية التي تستخدم اسم دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="70921-126">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="70921-127">في حالة تحديد خيار <strong>الحساب المقابل الثابت</strong> في صفحة <strong>أسماء دفاتر اليومية</strong>، يتجاوز الحساب المقابل لاسم دفتر اليومية الحساب المقابل الافتراضي للمورد أو مجموعة الموردين.</span><span class="sxs-lookup"><span data-stu-id="70921-127">If the <strong>Fixed offset account</strong> option on the <strong>Journal names</strong> page is selected, the offset account for the journal name overrides the default offset account for the vendor or vendor group.</span></span></td>
<td><span data-ttu-id="70921-128">استخدم هذا الخيار لإعداد دفاتر اليومية للتكاليف المحددة والمصروفات التي تقيد على حسابات معينة، بغض النظر عمن هو المورد أو مجموعة الموردين التي ينتمي إليها المورد.</span><span class="sxs-lookup"><span data-stu-id="70921-128">Use this option to set up journals for specific costs and expenses that are charged to specific accounts, regardless of the vendor or the vendor group that the vendor belongs to.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70921-129"><strong>أسماء دفاتر اليومية</strong> – إعداد الحسابات المقابلة الافتراضية لدفاتر اليومية في صفحة <strong>أسماء دفاتر اليومية</strong>.</span><span class="sxs-lookup"><span data-stu-id="70921-129"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="70921-130">قم بإلغاء تحديد خيار <strong>الحساب المقابل الثابت</strong>.</span><span class="sxs-lookup"><span data-stu-id="70921-130">Clear the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="70921-131">لاحظ أنه لا يمكنك تعيين الحسابات المقابلة الافتراضية في أسماء دفاتر اليومية، إذا كان نوع دفتر اليومية لأسماء دفاتر اليومية هو <strong>سجل الفواتير</strong> أو <strong>الموافقة</strong>.</span><span class="sxs-lookup"><span data-stu-id="70921-131">Note that you can&#39;t specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="70921-132">رأس دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="70921-132">Journal header</span></span></li>
<li><span data-ttu-id="70921-133">إدخالات دفتر اليومية في دفاتر اليومية التي تستخدم اسم دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="70921-133">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="70921-134">يتم استخدام هذه الإدخالات الافتراضية في صفحات رأس دفتر اليومية، ويتم استخدام الحساب المقابل في صفحة رأس دفتر اليومية كإدخال افتراضي في صفحات إيصال دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="70921-134">These default entries are used on journal header pages, and the offset account on the journal header page is used as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="70921-135">لا يتم استخدام الحسابات الافتراضية من صفحة <strong>أسماء دفاتر اليومية</strong> إلا إذا لم يتم إعداد الحسابات الافتراضية لحساب المورد.</span><span class="sxs-lookup"><span data-stu-id="70921-135">Default accounts from the <strong>Journal names </strong>page are used only if default accounts aren’t set up for the vendor account.</span></span></td>
<td><span data-ttu-id="70921-136">استخدم هذا الخيار لإعداد حسابات افتراضية التي يتم استخدامها عندما لا يتم تعيين الحساب المقابل الافتراضي للمورد.</span><span class="sxs-lookup"><span data-stu-id="70921-136">Use this option to set up default accounts that are used when a default vendor offset account isn&#39;t assigned.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70921-137"><strong>رأس دفتر اليومية</strong> – قم بإعداد الحساب المقابل الافتراضي لدفتر يومية كإدخال افتراضي في صفحات إيصال دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="70921-137"><strong>Journal header</strong> – Set up a default offset account for a journal as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="70921-138">لاحظ أنه لا يمكنك تعيين الحسابات المقابلة الافتراضية في رأس دفتر اليومية، إذا كان نوع دفتر اليومية لأسماء دفاتر اليومية هو <strong>سجل الفواتير</strong> أو <strong>الموافقة</strong>.</span><span class="sxs-lookup"><span data-stu-id="70921-138">Note that you can&#39;t specify default offset accounts on the journal header if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><span data-ttu-id="70921-139">إدخالات دفتر اليومية في دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="70921-139">Journal entries in the journal</span></span></td>
<td><span data-ttu-id="70921-140">قم بإعداد الحساب المقابل الافتراضي لدفتر يومية مستخدم كإدخال افتراضي في صفحات إيصال دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="70921-140">The default offset account for a journal is used as the default entry on the journal voucher pages.</span></span></td>
<td><span data-ttu-id="70921-141">استخدم هذا الخيار للمساعدة في تسريع إدخال البيانات إذا كان لمعظم الإدخالات في دفتر يومية نفس الحساب المقابل.</span><span class="sxs-lookup"><span data-stu-id="70921-141">Use this option to help speed up data entry if most entries in a journal have the same offset account.</span></span></td>
</tr>
</tbody>
</table>






