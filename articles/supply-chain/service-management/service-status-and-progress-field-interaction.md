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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a94f2df6a4ddb71a29ff951dfe38618ac7762783
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975478"
---
# <a name="service-status-and-progress-field-interaction"></a>تفاعل حقل التقدم وحالة الخدمة 

[!include [banner](../includes/banner.md)]


في نموذج **أوامر الخدمة** ، يعكس حقل **التقدم** الموجود بالبيانات الرئيسية حالة أمر الخدمة بأكمله، وتبين **الحالة** حالة بنود أمر الخدمة الفردية.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>التقدم</p></th>
<th><p>حالة البند 1</p></th>
<th><p>حالة البند 2</p></th>
<th><p>حالة البند 3</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>قيد التنفيذ</strong></p></td>
<td><p><strong>تم الإنشاء</strong></p></td>
<td><p><strong>تم الإنشاء</strong></p></td>
<td><p><strong>تم الإنشاء</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>قيد التنفيذ</strong></p></td>
<td><p><strong>مُلغى</strong></p></td>
<td><p><strong>تم الإنشاء</strong></p></td>
<td><p><strong>تم الإنشاء</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>قيد التنفيذ</strong></p></td>
<td><p><strong>تم الإنشاء</strong></p></td>
<td><p><strong>مُلغى</strong></p></td>
<td><p><strong>مُرحَّل</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>مُلغى</strong></p></td>
<td><p><strong>مُلغى</strong></p></td>
<td><p><strong>مُلغى</strong></p></td>
<td><p><strong>مُلغى</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>مُرحَّل</strong></p></td>
<td><p><strong>مُرحَّل</strong></p></td>
<td><p><strong>مُرحَّل</strong></p></td>
<td><p><strong>مُرحَّل</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>مُرحَّل</strong></p></td>
<td><p><strong>مُرحَّل</strong></p></td>
<td><p><strong>مُلغى</strong></p></td>
<td><p><strong>مُلغى</strong></p></td>
</tr>
</tbody>
</table>


تكون حالة تقدم أمر الخدمة هي قيد المعالجة إذا كانت كافة البنود بالحالة **تم الإنشاء** ؛ كما تظل الحالة قيد المعالجة إذا كانت بعض البنود بالحالة **مُلغى** أو **مُرحل** .

في حالة تحديد كل البند موجود في أمر الخدمة باعتباره **مرحل** ، يكون مستوى تقدم حالة الأمر هو **مرحل** . إذا كانت بعض البنود بالحالة **مرحل** والبعض الآخر بالحالة **ملغى** ، يظل مستوى التقدم هو **مرحل** .

  


