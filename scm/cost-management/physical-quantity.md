---
title: "قيم الكائن المخزون"
description: "توفر هذه المقالة معلومات حول كيفية حساب قيم كائن المخزون."
author: YuyuScheller
manager: AnnBe
ms.date: 2015-12-07 09 - 09 - 05
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 8898d5d91ffb4f73ea68f1251e1a99440e81bcd4
ms.lasthandoff: 03/29/2017


---

# <a name="inventory-object-values"></a>قيم الكائن المخزون

توفر هذه المقالة معلومات حول كيفية حساب قيم كائن المخزون. 

وظائف جديدة تسمى * * الكمية الفعلية * * تمكنك من رؤية قيم كائن مخزون محدد. ويمثل كائن التكلفة مستوى الكيان حيث يتم إجراء محاسبة المخزون. لمزيد من المعلومات حول كائنات التكلفة، راجع [كائنات التكلفة](cost-object.md). لمشاهدة قيم كائن مخزون محدد، انقر فوق **الكمية الفعلية** على **كائن التكلفة** الصفحة. وإليك كيفية حساب قيمة المخزون الكائن: كائن المخزون. القيمة = التكلفة الكائن. متوسط تكلفة الوحدة × المخزون الكائن. الكمية المثال التالي يوضح كيفية حساب قيم كائن مخزون وكائن تكلفة. تم تسجيل حدثي استلام منتجات في الصنف أ:

-   إيصال استلام المنتجات 1: الكمية = 100 أجهزة الكمبيوتر.، مبلغ = $1,000.00، موقع = 1، المستودع = 11، "رقم الدفعة" = ب 1
-   إيصال استلام المنتجات 2: الكمية = 50 أجهزة الكمبيوتر.، مبلغ = $800.00، موقع = 1، المستودع = 11، "رقم الدفعة" = ب 2

يعرض الجدول التالي نتيجة عملية الحساب لكائن تكلفة. يمكنك عرض النتيجة في صفحة **كائن التكلفة**.

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th>نوع الكائن</th>
<th>رقم العنصر</th>
<th>الموقع</th>
<th>الكمية</th>
<th>وحدة المخزون</th>
<th>القيمة</th>
<th>متوسط تكلفة الوحدة</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>كائن التكلفة</td>
<td>أ</td>
<td>1</td>
<td>150</td>
<td>أجزاء</td>
<td><p>1800.00 دولار</p></td>
<td><p>12.00 دولارًا</p></td>
</tr>
</tbody>
</table>

يعرض الجدول التالي نتيجة عملية الحساب لكائن مخزون. يمكنك عرض النتيجة بالنقر فوق **الكمية الفعلية** في صفحة **كائن التكلفة**.

<table style="width:100%;">
<colgroup>
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
</colgroup>
<thead>
<tr class="header">
<th>نوع الكائن</th>
<th>رقم العنصر</th>
<th>الموقع</th>
<th>المستودع</th>
<th>رقم الدُفعة</th>
<th>الكمية</th>
<th>وحدة المخزون</th>
<th>القيمة</th>
<th>متوسط تكلفة الوحدة</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>كائن المخزون</td>
<td>أ</td>
<td>1</td>
<td>11</td>
<td>ب1</td>
<td>100</td>
<td>أجزاء</td>
<td><p>1200.00 دولار</p></td>
<td><p>12.00 دولارًا</p></td>
</tr>
<tr class="even">
<td>كائن المخزون</td>
<td>أ</td>
<td>1</td>
<td>11</td>
<td>ب2</td>
<td>50</td>
<td>أجزاء</td>
<td><p>600.00 دولار</p></td>
<td><p>12.00 دولارًا</p></td>
</tr>
</tbody>
</table>



<a name="see-also"></a>راجع أيضًا
--------

[Cost objects](cost-object.md)

[Cost entries](cost-entries.md)

[ما هو جديد والمتغيرة في Microsoft Dynamics AX](/dynamics365/operations/dev-itpro/get-started/whats-new-changed)


