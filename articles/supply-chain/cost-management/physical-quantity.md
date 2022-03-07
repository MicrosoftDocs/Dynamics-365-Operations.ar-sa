---
title: قيم كائن المخزون
description: توفر هذه المقالة معلومات حول كيفية حساب قيم كائن المخزون.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: daa36dad4009cc25b89363dcff6b4496205522e3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421254"
---
# <a name="inventory-object-values"></a>قيم كائن المخزون

[!include [banner](../includes/banner.md)]

توفر هذه المقالة معلومات حول كيفية حساب قيم كائن المخزون. 

تتيح لك وظائف جديدة باسم **الكمية الفعلية** مشاهدة قيم كائن المخزون المحدد. 

ويمثل كائن التكلفة مستوى الكيان حيث يتم إجراء محاسبة المخزون. لمزيد من المعلومات حول كائنات التكلفة، راجع [كائنات التكلفة](cost-object.md). 

‏‫ولمشاهدة قيم كائن مخزون محدد، انقر فوق **الكمية الفعلية** في صفحة **كائن التكلفة**. وإليك كيفية حساب قيمة كائن المخزون: 

كائن المخزون.القيمة = كائن المخزون.متوسط تكلفة الوحدة × كائن المخزون.الكمية 

يوضح المثال التالي كيفية حساب قيم كائن مخزون وكائن تكلفة. تم تسجيل حدثي استلام منتجات في الصنف أ:

-   إيصال استلام المنتج 1: الكمية = 100 قطعة، مبلغ = 1000.00 دولار، الموقع = 1، المستودع = 11، رقم الدُفعة = B1
-   إيصال استلام المنتج 2: الكمية = 50 قطعة، مبلغ = 800.00 دولار، الموقع = 1، المستودع = 11، رقم الدُفعة = B2

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
<td>و</td>
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



<a name="additional-resources"></a>الموارد الإضافية
--------

[كائنات التكلفة](cost-object.md)

[إدخالات التكلفة](cost-entries.md)

[الميزات الجديدة والمتغيرة](../../fin-and-ops/get-started/whats-new-changed.md)



