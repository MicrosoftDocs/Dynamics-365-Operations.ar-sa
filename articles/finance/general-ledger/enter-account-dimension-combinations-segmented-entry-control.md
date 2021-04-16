---
title: إدخال مجموعات الحسابات والأبعاد (عنصر تحكم في الإدخال المقسم)
description: توضح هذه المقالة كيفية إدخال مجموعات الحسابات والأبعاد أو حسابات دفتر الأستاذ. يُشار في أغلب الأحيان إلى تجربة الإدخال بعنصر التحكم في الإدخال المقسم.
author: aprilolson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure
audience: Application User
ms.reviewer: roschlom
ms.custom: 14071
ms.assetid: e6fce826-c403-4d91-a78b-e9a58c44ac03
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 21a67e4760e870b4d0a576523cbece0db5fa1923
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837976"
---
# <a name="enter-account-and-dimension-combinations-segmented-entry-control"></a><span data-ttu-id="3d6ae-104">إدخال مجموعات الحسابات والأبعاد (عنصر تحكم في الإدخال المقسم)</span><span class="sxs-lookup"><span data-stu-id="3d6ae-104">Enter account and dimension combinations (segmented entry control)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3d6ae-105">توضح هذه المقالة كيفية إدخال مجموعات الحسابات والأبعاد أو حسابات دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="3d6ae-105">This article describes how to enter account and dimension combinations or ledger accounts.</span></span> <span data-ttu-id="3d6ae-106">يُشار في أغلب الأحيان إلى تجربة الإدخال بعنصر التحكم في الإدخال المقسم.</span><span class="sxs-lookup"><span data-stu-id="3d6ae-106">The entry experience is often referred to as segmented entry control.</span></span>

<span data-ttu-id="3d6ae-107">يقوم المستخدمون بإدخال مجموعات الحسابات والأبعاد في العديد من الصفحات، مثل صفحات دفاتر اليومية العامة، وإعداد الموازنة، وتعريفات الترحيل.</span><span class="sxs-lookup"><span data-stu-id="3d6ae-107">Users enter account and dimension combinations on various pages, such as pages for general journals, budgeting, and posting definitions.</span></span> <span data-ttu-id="3d6ae-108">وتعتمد مجموعات الحسابات والأبعاد الصالحة على بنيات الحسابات التي تم تعيينها لدفتر الأستاذ والقواعد المتقدمة التي تم تعيينها لبنيات الحسابات.</span><span class="sxs-lookup"><span data-stu-id="3d6ae-108">The valid account and dimension combinations depend on the account structures that are assigned to the ledger and the advanced rules that are assigned to the account structures.</span></span> <span data-ttu-id="3d6ae-109">وعند قيام المستخدمين بإدخال مجموعة، يمكنهم إما إدخال القيم يدوياً أو الاستفادة من خبرة بحث غنية.</span><span class="sxs-lookup"><span data-stu-id="3d6ae-109">When users enter a combination, they can either manually type the values or take advantage of a rich, lookup experience.</span></span> <span data-ttu-id="3d6ae-110">عند إدخال الحقل، يمكنك البدء في الكتابة وسيبحث عن القيمة والوصف.</span><span class="sxs-lookup"><span data-stu-id="3d6ae-110">When you enter the field, you can start to type and it will search the value and the description.</span></span> <span data-ttu-id="3d6ae-111">على سبيل المثال، إذا قمت بكتابة 180، فسيبحث أي قيمة تبدأ بمجموعة الأرقام تلك.</span><span class="sxs-lookup"><span data-stu-id="3d6ae-111">For example, if you type 180 it will search any value that begins with that number combination.</span></span> <span data-ttu-id="3d6ae-112">أو قد تقوم بكتابة نقد، وسيبحث أي قيمة لها وصف يبدأ بنقد.</span><span class="sxs-lookup"><span data-stu-id="3d6ae-112">Or you may type Cash and it will search any value that has a description that begins with Cash.</span></span> <span data-ttu-id="3d6ae-113">يمكنك أيضًا استخدام أحرف بدل، مثل \*نقد أو \*180 للبحث إذا كانت القيمة أو الوصف يحتوي على معايير البحث.</span><span class="sxs-lookup"><span data-stu-id="3d6ae-113">You can also use a wildcard, such as \*Cash or \*180 to search if the value or description contain the search criteria.</span></span> 

<span data-ttu-id="3d6ae-114">يصف الجدول التالي اختصارات لوحة المفاتيح التي يمكن استخدامها عند إغلاق البحث.</span><span class="sxs-lookup"><span data-stu-id="3d6ae-114">The following table describes the keyboard shortcuts that can be used when the lookup is closed.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3d6ae-115">اختصار لوحة المفاتيح</span><span class="sxs-lookup"><span data-stu-id="3d6ae-115">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="3d6ae-116">الإجراء</span><span class="sxs-lookup"><span data-stu-id="3d6ae-116">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3d6ae-117">Alt + سهم لأسفل</span><span class="sxs-lookup"><span data-stu-id="3d6ae-117">Alt+Down Arrow</span></span></td>
<td><span data-ttu-id="3d6ae-118">فتح البحث.</span><span class="sxs-lookup"><span data-stu-id="3d6ae-118">Open the lookup.</span></span> <span data-ttu-id="3d6ae-119">إذا قمت بالضغط على Alt + سهم لأسفل لمرة ثانية، ينتقل التركيز إلى الشرائح في القائمة المنبثقة.</span><span class="sxs-lookup"><span data-stu-id="3d6ae-119">If you press Alt+Down Arrow a second time, the focus moves to the segments in the flyout.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="3d6ae-120">Enter وShift+Enter</span><span class="sxs-lookup"><span data-stu-id="3d6ae-120">Enter and Shift+Enter</span></span></li>
<li><span data-ttu-id="3d6ae-121">محدد دليل الحسابات</span><span class="sxs-lookup"><span data-stu-id="3d6ae-121">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="3d6ae-122">السهم لليسار والسهم لليمين</span><span class="sxs-lookup"><span data-stu-id="3d6ae-122">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="3d6ae-123">الانتقال إلى الشريحة التالية أو السابقة</span><span class="sxs-lookup"><span data-stu-id="3d6ae-123">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d6ae-124">علامة تبويب</span><span class="sxs-lookup"><span data-stu-id="3d6ae-124">Tab</span></span></td>
<td><span data-ttu-id="3d6ae-125">الانتقال إلى الحقل التالي في الشبكة.</span><span class="sxs-lookup"><span data-stu-id="3d6ae-125">Move to the next field in the grid.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3d6ae-126">يصف الجدول التالي اختصارات لوحة المفاتيح التي يمكن استخدامها عند فتح البحث.</span><span class="sxs-lookup"><span data-stu-id="3d6ae-126">The following table describes the keyboard shortcuts that can be used when the lookup is open.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3d6ae-127">اختصار لوحة المفاتيح</span><span class="sxs-lookup"><span data-stu-id="3d6ae-127">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="3d6ae-128">الإجراء</span><span class="sxs-lookup"><span data-stu-id="3d6ae-128">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3d6ae-129">Esc</span><span class="sxs-lookup"><span data-stu-id="3d6ae-129">Esc</span></span></td>
<td><span data-ttu-id="3d6ae-130">إغلاق البحث.</span><span class="sxs-lookup"><span data-stu-id="3d6ae-130">Close the lookup.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="3d6ae-131">سهم لأعلى وسهم لأسفل</span><span class="sxs-lookup"><span data-stu-id="3d6ae-131">Up Arrow and Down Arrow</span></span></li>
<li><span data-ttu-id="3d6ae-132">Page Up وPage Down</span><span class="sxs-lookup"><span data-stu-id="3d6ae-132">Page Up and Page Down</span></span></li>
<li><span data-ttu-id="3d6ae-133">Home وEnd</span><span class="sxs-lookup"><span data-stu-id="3d6ae-133">Home and End</span></span></li>
</ul></td>
<td><span data-ttu-id="3d6ae-134">انتقل إلى القيمة السابقة أو التالية في القوائم أو مجموعة القيم السابقة أو التالية أو العنصر الأول أو الأخير في البحث.</span><span class="sxs-lookup"><span data-stu-id="3d6ae-134">Move to the previous or next value in the lists, to the previous or next group of values, or to the first or last element in the lookup.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="3d6ae-135">محدد دليل الحسابات</span><span class="sxs-lookup"><span data-stu-id="3d6ae-135">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="3d6ae-136">السهم لليسار والسهم لليمين</span><span class="sxs-lookup"><span data-stu-id="3d6ae-136">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="3d6ae-137">الانتقال إلى الشريحة التالية أو السابقة</span><span class="sxs-lookup"><span data-stu-id="3d6ae-137">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d6ae-138">علامة تبويب</span><span class="sxs-lookup"><span data-stu-id="3d6ae-138">Tab</span></span></td>
<td><span data-ttu-id="3d6ae-139">الانتقال إلى الحقل التالي في الشبكة.</span><span class="sxs-lookup"><span data-stu-id="3d6ae-139">Move to the next field in the grid.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d6ae-140">Alt+W</span><span class="sxs-lookup"><span data-stu-id="3d6ae-140">Alt+W</span></span></td>
<td><span data-ttu-id="3d6ae-141">قم بالتبديل بين <strong>إظهار الكل</strong> و<strong>إظهار الصالح</strong>.</span><span class="sxs-lookup"><span data-stu-id="3d6ae-141">Switch between <strong>Show all</strong> and <strong>Show valid</strong>.</span></span></td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]