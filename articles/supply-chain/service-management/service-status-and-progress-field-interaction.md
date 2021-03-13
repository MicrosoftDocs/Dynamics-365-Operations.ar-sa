---
title: تفاعل حقل التقدم وحالة الخدمة
description: في نموذج أوامر الخدمة، يعرض حقل التقدم الموجود بالبيانات الرئيسية حالة أمر الخدمة بأكمله، وتبين الحالة حالة بنود أمر الخدمة الفردية.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 314ca8c325205bd8f489daf46498e9586603eaf3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010437"
---
# <a name="service-status-and-progress-field-interaction"></a><span data-ttu-id="6a702-103">تفاعل حقل التقدم وحالة الخدمة</span><span class="sxs-lookup"><span data-stu-id="6a702-103">Service status and progress field interaction</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="6a702-104">في نموذج **أوامر الخدمة**، يعكس حقل **التقدم** الموجود بالبيانات الرئيسية حالة أمر الخدمة بأكمله، وتبين **الحالة** حالة بنود أمر الخدمة الفردية.</span><span class="sxs-lookup"><span data-stu-id="6a702-104">In the **Service orders** form, the **Progress** field on the service order header reflects the status of the whole service order, and the **Status** reports the status of individual service order lines.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6a702-105">التقدم</span><span class="sxs-lookup"><span data-stu-id="6a702-105">Progress</span></span></p></th>
<th><p><span data-ttu-id="6a702-106">حالة البند 1</span><span class="sxs-lookup"><span data-stu-id="6a702-106">Line 1 Status</span></span></p></th>
<th><p><span data-ttu-id="6a702-107">حالة البند 2</span><span class="sxs-lookup"><span data-stu-id="6a702-107">Line 2 Status</span></span></p></th>
<th><p><span data-ttu-id="6a702-108">حالة البند 3</span><span class="sxs-lookup"><span data-stu-id="6a702-108">Line 3 Status</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6a702-109"><strong>قيد التنفيذ</strong></span><span class="sxs-lookup"><span data-stu-id="6a702-109"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="6a702-110"><strong>تم الإنشاء</strong></span><span class="sxs-lookup"><span data-stu-id="6a702-110"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="6a702-111"><strong>تم الإنشاء</strong></span><span class="sxs-lookup"><span data-stu-id="6a702-111"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="6a702-112"><strong>تم الإنشاء</strong></span><span class="sxs-lookup"><span data-stu-id="6a702-112"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a702-113"><strong>قيد التنفيذ</strong></span><span class="sxs-lookup"><span data-stu-id="6a702-113"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="6a702-114"><strong>مُلغى</strong></span><span class="sxs-lookup"><span data-stu-id="6a702-114"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="6a702-115"><strong>تم الإنشاء</strong></span><span class="sxs-lookup"><span data-stu-id="6a702-115"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="6a702-116"><strong>تم الإنشاء</strong></span><span class="sxs-lookup"><span data-stu-id="6a702-116"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a702-117"><strong>قيد التنفيذ</strong></span><span class="sxs-lookup"><span data-stu-id="6a702-117"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="6a702-118"><strong>تم الإنشاء</strong></span><span class="sxs-lookup"><span data-stu-id="6a702-118"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="6a702-119"><strong>مُلغى</strong></span><span class="sxs-lookup"><span data-stu-id="6a702-119"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="6a702-120"><strong>مُرحَّل</strong></span><span class="sxs-lookup"><span data-stu-id="6a702-120"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a702-121"><strong>مُلغى</strong></span><span class="sxs-lookup"><span data-stu-id="6a702-121"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="6a702-122"><strong>مُلغى</strong></span><span class="sxs-lookup"><span data-stu-id="6a702-122"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="6a702-123"><strong>مُلغى</strong></span><span class="sxs-lookup"><span data-stu-id="6a702-123"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="6a702-124"><strong>مُلغى</strong></span><span class="sxs-lookup"><span data-stu-id="6a702-124"><strong>Canceled</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a702-125"><strong>مُرحَّل</strong></span><span class="sxs-lookup"><span data-stu-id="6a702-125"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="6a702-126"><strong>مُرحَّل</strong></span><span class="sxs-lookup"><span data-stu-id="6a702-126"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="6a702-127"><strong>مُرحَّل</strong></span><span class="sxs-lookup"><span data-stu-id="6a702-127"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="6a702-128"><strong>مُرحَّل</strong></span><span class="sxs-lookup"><span data-stu-id="6a702-128"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a702-129"><strong>مُرحَّل</strong></span><span class="sxs-lookup"><span data-stu-id="6a702-129"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="6a702-130"><strong>مُرحَّل</strong></span><span class="sxs-lookup"><span data-stu-id="6a702-130"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="6a702-131"><strong>مُلغى</strong></span><span class="sxs-lookup"><span data-stu-id="6a702-131"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="6a702-132"><strong>مُلغى</strong></span><span class="sxs-lookup"><span data-stu-id="6a702-132"><strong>Canceled</strong></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6a702-133">تكون حالة تقدم أمر الخدمة هي قيد المعالجة إذا كانت كافة البنود بالحالة **تم الإنشاء**؛ كما تظل الحالة قيد المعالجة إذا كانت بعض البنود بالحالة **مُلغى** أو **مُرحل**.</span><span class="sxs-lookup"><span data-stu-id="6a702-133">The progress of a service order is in process if all lines have the status **Created**; it is still in process if some of the lines have a status of **Canceled** or **Posted**.</span></span>

<span data-ttu-id="6a702-134">في حالة تحديد كل البند موجود في أمر الخدمة باعتباره **مرحل**، يكون مستوى تقدم حالة الأمر هو **مرحل**.</span><span class="sxs-lookup"><span data-stu-id="6a702-134">If all lines in a service order are marked as **Posted**, the progress of the status order is **Posted**.</span></span> <span data-ttu-id="6a702-135">إذا كانت بعض البنود بالحالة **مرحل** والبعض الآخر بالحالة **ملغى**، يظل مستوى التقدم هو **مرحل**.</span><span class="sxs-lookup"><span data-stu-id="6a702-135">If some lines are **Posted** and some are **Canceled**, the progress is still **Posted**.</span></span>

  


