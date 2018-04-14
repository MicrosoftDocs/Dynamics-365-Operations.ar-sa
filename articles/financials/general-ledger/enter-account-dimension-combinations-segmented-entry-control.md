---
title: "إدخال مجموعات الحسابات والأبعاد (عنصر تحكم في الإدخال المقسم)"
description: "توضح هذه المقالة كيفية إدخال مجموعات الحسابات والأبعاد أو حسابات دفتر الأستاذ. يُشار في أغلب الأحيان إلى تجربة الإدخال بعنصر التحكم في الإدخال المقسم."
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionConfigureAccountStructure
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14071
ms.assetid: e6fce826-c403-4d91-a78b-e9a58c44ac03
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 120a28cc9ae8685895400e872cc03e7b6a1c6642
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---

# <a name="enter-account-and-dimension-combinations-segmented-entry-control"></a><span data-ttu-id="fed9f-104">إدخال مجموعات الحسابات والأبعاد (عنصر تحكم في الإدخال المقسم)</span><span class="sxs-lookup"><span data-stu-id="fed9f-104">Enter account and dimension combinations (segmented entry control)</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="fed9f-105">توضح هذه المقالة كيفية إدخال مجموعات الحسابات والأبعاد أو حسابات دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="fed9f-105">This article describes how to enter account and dimension combinations or ledger accounts.</span></span> <span data-ttu-id="fed9f-106">يُشار في أغلب الأحيان إلى تجربة الإدخال بعنصر التحكم في الإدخال المقسم.</span><span class="sxs-lookup"><span data-stu-id="fed9f-106">The entry experience is often referred to as segmented entry control.</span></span>

<span data-ttu-id="fed9f-107">يقوم المستخدمون بإدخال مجموعات الحسابات والأبعاد في العديد من الصفحات، مثل صفحات دفاتر اليومية العامة، وإعداد الموازنة، وتعريفات الترحيل.</span><span class="sxs-lookup"><span data-stu-id="fed9f-107">Users enter account and dimension combinations on various pages, such as pages for general journals, budgeting, and posting definitions.</span></span> <span data-ttu-id="fed9f-108">وتعتمد مجموعات الحسابات والأبعاد الصالحة على بنيات الحسابات التي تم تعيينها لدفتر الأستاذ والقواعد المتقدمة التي تم تعيينها لبنيات الحسابات.</span><span class="sxs-lookup"><span data-stu-id="fed9f-108">The valid account and dimension combinations depend on the account structures that are assigned to the ledger and the advanced rules that are assigned to the account structures.</span></span> <span data-ttu-id="fed9f-109">وعند قيام المستخدمين بإدخال مجموعة، يمكنهم إما إدخال القيم يدوياً أو الاستفادة من خبرة بحث غنية.</span><span class="sxs-lookup"><span data-stu-id="fed9f-109">When users enter a combination, they can either manually type the values or take advantage of a rich, lookup experience.</span></span> <span data-ttu-id="fed9f-110">عند إدخال الحقل، يمكنك البدء في الكتابة وسيبحث عن القيمة والوصف.</span><span class="sxs-lookup"><span data-stu-id="fed9f-110">When you enter the field, you can start to type and it will search the value and the description.</span></span> <span data-ttu-id="fed9f-111">على سبيل المثال، إذا قمت بكتابة 180، فسيبحث أي قيمة تبدأ بمجموعة الأرقام تلك.</span><span class="sxs-lookup"><span data-stu-id="fed9f-111">For example, if you type 180 it will search any value that begins with that number combination.</span></span> <span data-ttu-id="fed9f-112">أو قد تقوم بكتابة نقد، وسيبحث أي قيمة لها وصف يبدأ بنقد.</span><span class="sxs-lookup"><span data-stu-id="fed9f-112">Or you may type Cash and it will search any value that has a description that begins with Cash.</span></span> <span data-ttu-id="fed9f-113">يمكنك أيضًا استخدام أحرف بدل، مثل \*نقد أو \*180 للبحث إذا كانت القيمة أو الوصف يحتوي على معايير البحث.</span><span class="sxs-lookup"><span data-stu-id="fed9f-113">You can also use a wildcard, such as \*Cash or \*180 to search if the value or description contain the search criteria.</span></span> 

<span data-ttu-id="fed9f-114">يصف الجدول التالي اختصارات لوحة المفاتيح التي يمكن استخدامها عند إغلاق البحث.</span><span class="sxs-lookup"><span data-stu-id="fed9f-114">The following table describes the keyboard shortcuts that can be used when the lookup is closed.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fed9f-115">اختصار لوحة المفاتيح</span><span class="sxs-lookup"><span data-stu-id="fed9f-115">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="fed9f-116">الإجراء</span><span class="sxs-lookup"><span data-stu-id="fed9f-116">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fed9f-117">Alt + سهم لأسفل</span><span class="sxs-lookup"><span data-stu-id="fed9f-117">Alt+Down Arrow</span></span></td>
<td><span data-ttu-id="fed9f-118">فتح البحث.</span><span class="sxs-lookup"><span data-stu-id="fed9f-118">Open the lookup.</span></span> <span data-ttu-id="fed9f-119">إذا قمت بالضغط على Alt + سهم لأسفل لمرة ثانية، ينتقل التركيز إلى الشرائح في القائمة المنبثقة.</span><span class="sxs-lookup"><span data-stu-id="fed9f-119">If you press Alt+Down Arrow a second time, the focus moves to the segments in the flyout.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="fed9f-120">Enter وShift+Enter</span><span class="sxs-lookup"><span data-stu-id="fed9f-120">Enter and Shift+Enter</span></span></li>
<li><span data-ttu-id="fed9f-121">محدد دليل الحسابات</span><span class="sxs-lookup"><span data-stu-id="fed9f-121">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="fed9f-122">السهم لليسار والسهم لليمين</span><span class="sxs-lookup"><span data-stu-id="fed9f-122">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="fed9f-123">الانتقال إلى الشريحة التالية أو السابقة</span><span class="sxs-lookup"><span data-stu-id="fed9f-123">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fed9f-124">علامة تبويب</span><span class="sxs-lookup"><span data-stu-id="fed9f-124">Tab</span></span></td>
<td><span data-ttu-id="fed9f-125">الانتقال إلى الحقل التالي في الشبكة.</span><span class="sxs-lookup"><span data-stu-id="fed9f-125">Move to the next field in the grid.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="fed9f-126">يصف الجدول التالي اختصارات لوحة المفاتيح التي يمكن استخدامها عند فتح البحث.</span><span class="sxs-lookup"><span data-stu-id="fed9f-126">The following table describes the keyboard shortcuts that can be used when the lookup is open.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fed9f-127">اختصار لوحة المفاتيح</span><span class="sxs-lookup"><span data-stu-id="fed9f-127">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="fed9f-128">الإجراء</span><span class="sxs-lookup"><span data-stu-id="fed9f-128">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fed9f-129">Esc</span><span class="sxs-lookup"><span data-stu-id="fed9f-129">Esc</span></span></td>
<td><span data-ttu-id="fed9f-130">إغلاق البحث.</span><span class="sxs-lookup"><span data-stu-id="fed9f-130">Close the lookup.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="fed9f-131">سهم لأعلى وسهم لأسفل</span><span class="sxs-lookup"><span data-stu-id="fed9f-131">Up Arrow and Down Arrow</span></span></li>
<li><span data-ttu-id="fed9f-132">Page Up وPage Down</span><span class="sxs-lookup"><span data-stu-id="fed9f-132">Page Up and Page Down</span></span></li>
<li><span data-ttu-id="fed9f-133">Home وEnd</span><span class="sxs-lookup"><span data-stu-id="fed9f-133">Home and End</span></span></li>
</ul></td>
<td><span data-ttu-id="fed9f-134">انتقل إلى القيمة السابقة أو التالية في القوائم أو مجموعة القيم السابقة أو التالية أو العنصر الأول أو الأخير في البحث.</span><span class="sxs-lookup"><span data-stu-id="fed9f-134">Move to the previous or next value in the lists, to the previous or next group of values, or to the first or last element in the lookup.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="fed9f-135">محدد دليل الحسابات</span><span class="sxs-lookup"><span data-stu-id="fed9f-135">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="fed9f-136">السهم لليسار والسهم لليمين</span><span class="sxs-lookup"><span data-stu-id="fed9f-136">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="fed9f-137">الانتقال إلى الشريحة التالية أو السابقة</span><span class="sxs-lookup"><span data-stu-id="fed9f-137">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fed9f-138">علامة تبويب</span><span class="sxs-lookup"><span data-stu-id="fed9f-138">Tab</span></span></td>
<td><span data-ttu-id="fed9f-139">الانتقال إلى الحقل التالي في الشبكة.</span><span class="sxs-lookup"><span data-stu-id="fed9f-139">Move to the next field in the grid.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fed9f-140">Alt+W</span><span class="sxs-lookup"><span data-stu-id="fed9f-140">Alt+W</span></span></td>
<td><span data-ttu-id="fed9f-141">قم بالتبديل بين <strong>إظهار الكل</strong> و<strong>إظهار الصالح</strong>.</span><span class="sxs-lookup"><span data-stu-id="fed9f-141">Switch between <strong>Show all</strong> and <strong>Show valid</strong>.</span></span></td>
</tr>
</tbody>
</table>






