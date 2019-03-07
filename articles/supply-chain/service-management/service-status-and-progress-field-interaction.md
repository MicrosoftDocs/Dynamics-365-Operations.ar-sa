---
title: تفاعل حقل التقدم وحالة الخدمة
description: في نموذج أوامر الخدمة، يعرض حقل التقدم الموجود بالبيانات الرئيسية حالة أمر الخدمة بأكمله، وتبين الحالة حالة بنود أمر الخدمة الفردية.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2dd7b5160149a38dd62535901c1225bf704f404d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "346124"
---
# <a name="service-status-and-progress-field-interaction"></a><span data-ttu-id="a72a5-103">تفاعل حقل التقدم وحالة الخدمة</span><span class="sxs-lookup"><span data-stu-id="a72a5-103">Service status and progress field interaction</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a72a5-104">في نموذج **أوامر الخدمة**، يعكس حقل **التقدم** الموجود بالبيانات الرئيسية حالة أمر الخدمة بأكمله، وتبين **الحالة** حالة بنود أمر الخدمة الفردية.</span><span class="sxs-lookup"><span data-stu-id="a72a5-104">In the **Service orders** form, the **Progress** field on the service order header reflects the status of the whole service order, and the **Status** reports the status of individual service order lines.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a72a5-105">التقدم</span><span class="sxs-lookup"><span data-stu-id="a72a5-105">Progress</span></span></p></th>
<th><p><span data-ttu-id="a72a5-106">حالة البند 1</span><span class="sxs-lookup"><span data-stu-id="a72a5-106">Line 1 Status</span></span></p></th>
<th><p><span data-ttu-id="a72a5-107">حالة البند 2</span><span class="sxs-lookup"><span data-stu-id="a72a5-107">Line 2 Status</span></span></p></th>
<th><p><span data-ttu-id="a72a5-108">حالة البند 3</span><span class="sxs-lookup"><span data-stu-id="a72a5-108">Line 3 Status</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a72a5-109"><strong>قيد التنفيذ</strong></span><span class="sxs-lookup"><span data-stu-id="a72a5-109"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="a72a5-110"><strong>تم الإنشاء</strong></span><span class="sxs-lookup"><span data-stu-id="a72a5-110"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="a72a5-111"><strong>تم الإنشاء</strong></span><span class="sxs-lookup"><span data-stu-id="a72a5-111"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="a72a5-112"><strong>تم الإنشاء</strong></span><span class="sxs-lookup"><span data-stu-id="a72a5-112"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a72a5-113"><strong>قيد التنفيذ</strong></span><span class="sxs-lookup"><span data-stu-id="a72a5-113"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="a72a5-114"><strong>مُلغى</strong></span><span class="sxs-lookup"><span data-stu-id="a72a5-114"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="a72a5-115"><strong>تم الإنشاء</strong></span><span class="sxs-lookup"><span data-stu-id="a72a5-115"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="a72a5-116"><strong>تم الإنشاء</strong></span><span class="sxs-lookup"><span data-stu-id="a72a5-116"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a72a5-117"><strong>قيد التنفيذ</strong></span><span class="sxs-lookup"><span data-stu-id="a72a5-117"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="a72a5-118"><strong>تم الإنشاء</strong></span><span class="sxs-lookup"><span data-stu-id="a72a5-118"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="a72a5-119"><strong>مُلغى</strong></span><span class="sxs-lookup"><span data-stu-id="a72a5-119"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="a72a5-120"><strong>مُرحَّل</strong></span><span class="sxs-lookup"><span data-stu-id="a72a5-120"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a72a5-121"><strong>مُلغى</strong></span><span class="sxs-lookup"><span data-stu-id="a72a5-121"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="a72a5-122"><strong>مُلغى</strong></span><span class="sxs-lookup"><span data-stu-id="a72a5-122"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="a72a5-123"><strong>مُلغى</strong></span><span class="sxs-lookup"><span data-stu-id="a72a5-123"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="a72a5-124"><strong>مُلغى</strong></span><span class="sxs-lookup"><span data-stu-id="a72a5-124"><strong>Canceled</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a72a5-125"><strong>مُرحَّل</strong></span><span class="sxs-lookup"><span data-stu-id="a72a5-125"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="a72a5-126"><strong>مُرحَّل</strong></span><span class="sxs-lookup"><span data-stu-id="a72a5-126"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="a72a5-127"><strong>مُرحَّل</strong></span><span class="sxs-lookup"><span data-stu-id="a72a5-127"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="a72a5-128"><strong>مُرحَّل</strong></span><span class="sxs-lookup"><span data-stu-id="a72a5-128"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a72a5-129"><strong>مُرحَّل</strong></span><span class="sxs-lookup"><span data-stu-id="a72a5-129"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="a72a5-130"><strong>مُرحَّل</strong></span><span class="sxs-lookup"><span data-stu-id="a72a5-130"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="a72a5-131"><strong>مُلغى</strong></span><span class="sxs-lookup"><span data-stu-id="a72a5-131"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="a72a5-132"><strong>مُلغى</strong></span><span class="sxs-lookup"><span data-stu-id="a72a5-132"><strong>Canceled</strong></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a72a5-133">تكون حالة تقدم أمر الخدمة هي قيد المعالجة إذا كانت كافة البنود بالحالة **تم الإنشاء**؛ كما تظل الحالة قيد المعالجة إذا كانت بعض البنود بالحالة **مُلغى** أو **مُرحل**.</span><span class="sxs-lookup"><span data-stu-id="a72a5-133">The progress of a service order is in process if all lines have the status **Created**; it is still in process if some of the lines have a status of **Canceled** or **Posted**.</span></span>

<span data-ttu-id="a72a5-134">في حالة تحديد كل البند موجود في أمر الخدمة باعتباره **مرحل**، يكون مستوى تقدم حالة الأمر هو **مرحل**.</span><span class="sxs-lookup"><span data-stu-id="a72a5-134">If all lines in a service order are marked as **Posted**, the progress of the status order is **Posted**.</span></span> <span data-ttu-id="a72a5-135">إذا كانت بعض البنود بالحالة **مرحل** والبعض الآخر بالحالة **ملغى**، يظل مستوى التقدم هو **مرحل**.</span><span class="sxs-lookup"><span data-stu-id="a72a5-135">If some lines are **Posted** and some are **Canceled**, the progress is still **Posted**.</span></span>

  


