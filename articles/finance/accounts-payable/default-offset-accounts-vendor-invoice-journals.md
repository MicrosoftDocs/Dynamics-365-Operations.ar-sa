---
title: الحسابات المقابلة الافتراضية لدفاتر يومية فواتير المورد وواعتماد الفاتورة
description: سيساعدك هذا الموضوع في تحديد مكان تعيين الحسابات الافتراضية لدفاتر يومية الفاتورة.
author: abruer
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3b2ad808d5008d9a4b2d3ee975d15fa1ee13ed7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003468"
---
# <a name="default-offset-accounts-for-vendor-invoice-and-invoice-approval-journals"></a>الحسابات المقابلة الافتراضية لدفاتر يومية فواتير المورد وواعتماد الفاتورة

[!include [banner](../includes/banner.md)]

يتم استخدام الحسابات المقابلة الافتراضية في صفحات دفاتر يومية فاتورة المورد التالية:

-   دفتر يومية الفواتير
-   دفتر يومية الموافقة على الفواتير

استخدم الجدول التالي للمساعدة في تحديد مكان تعيين الحسابات الافتراضية لدفاتر يومية الفاتورة.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>قم بإعداد الحسابات الافتراضية هنا</th>
<th>المكان الذي يتم فيه توفير الحسابات الافتراضية</th>
<th>مدى تأثير هذا الخيار على المعالجة</th>
<th>متى يجب استخدام هذا الخيار</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>مجموعة الموردين</strong> – إعداد الحسابات المقابلة الافتراضية لمجموعات الموردين في صفحة <strong>إعداد الحساب الافتراضي</strong>، التي يمكنك فتحها من صفحة <strong>مجموعات الموردين</strong>.</td>
<td><ul>
<li>حساب المورّد</li>
<li>إدخالات دفتر اليومية لحسابات الموردين في مجموعة الموردين، إذا لم يتم تحديد الحسابات الافتراضية لحسابات الموردين</li>
</ul></td>
<td>يتم عرض الحسابات المقابلة الافتراضية لمجموعات الموردين باعتبارها الحسابات المقابلة الافتراضية للموردين في صفحة <strong>إعداد الحساب الافتراضي</strong>. ويمكنك فتح هذه الصفحة من صفحة قائمة <strong>كافة الموردين</strong>.</td>
<td>استخدم هذا الخيار إذا كنت عادةً ما تدفع لنفس أنواع الأشياء من نفس مجموعات الموردين على مر الزمن.</td>
</tr>
<tr class="even">
<td><strong>حساب المورد</strong> – إعداد الحسابات الافتراضية لحسابات الموردين في صفحة <strong>إعداد الحساب الافتراضي</strong>، التي يمكنك فتحها من صفحة <strong>الموردين</strong>.</td>
<td>إدخالات دفتر اليومية لحساب المورد</td>
<td>يتم عرض الحسابات المقابلة الافتراضية لحسابات المورد كحسابات مقابلة افتراضية لإدخالات دفتر اليومية لحساب المورد.</td>
<td>استخدم هذا الخيار إذا كنت عادةً ما تدفع لنفس أنواع الأشياء من نفس الموردين على مر الزمن.</td>
</tr>
<tr class="odd">
<td><strong>أسماء دفاتر اليومية</strong> – إعداد الحسابات المقابلة الافتراضية لدفاتر اليومية في صفحة <strong>أسماء دفاتر اليومية</strong>. حدد خيار <strong>الحساب المقابل الثابت</strong>. لاحظ أنه لا يمكنك تعيين الحسابات المقابلة الافتراضية في أسماء دفاتر اليومية، إذا كان نوع دفتر اليومية لأسماء دفاتر اليومية هو <strong>سجل الفواتير</strong> أو <strong>الموافقة</strong>.</td>
<td><ul>
<li>حدد رأس دفتر يومية يستخدم اسم دفتر اليومية</li>
<li>إدخالات دفتر اليومية في دفاتر اليومية التي تستخدم اسم دفتر اليومية</li>
</ul></td>
<td>في حالة تحديد خيار <strong>الحساب المقابل الثابت</strong> في صفحة <strong>أسماء دفاتر اليومية</strong>، يتجاوز الحساب المقابل لاسم دفتر اليومية الحساب المقابل الافتراضي للمورد أو مجموعة الموردين.</td>
<td>استخدم هذا الخيار لإعداد دفاتر اليومية للتكاليف المحددة والمصروفات التي تقيد على حسابات معينة، بغض النظر عمن هو المورد أو مجموعة الموردين التي ينتمي إليها المورد.</td>
</tr>
<tr class="even">
<td><strong>أسماء دفاتر اليومية</strong> – إعداد الحسابات المقابلة الافتراضية لدفاتر اليومية في صفحة <strong>أسماء دفاتر اليومية</strong>. قم بإلغاء تحديد خيار <strong>الحساب المقابل الثابت</strong>. لاحظ أنه لا يمكنك تعيين الحسابات المقابلة الافتراضية في أسماء دفاتر اليومية، إذا كان نوع دفتر اليومية لأسماء دفاتر اليومية هو <strong>سجل الفواتير</strong> أو <strong>الموافقة</strong>.</td>
<td><ul>
<li>رأس دفتر اليومية</li>
<li>إدخالات دفتر اليومية في دفاتر اليومية التي تستخدم اسم دفتر اليومية</li>
</ul></td>
<td>يتم استخدام هذه الإدخالات الافتراضية في صفحات رأس دفتر اليومية، ويتم استخدام الحساب المقابل في صفحة رأس دفتر اليومية كإدخال افتراضي في صفحات إيصال دفتر اليومية. لا يتم استخدام الحسابات الافتراضية من صفحة <strong>أسماء دفاتر اليومية</strong> إلا إذا لم يتم إعداد الحسابات الافتراضية لحساب المورد.</td>
<td>استخدم هذا الخيار لإعداد حسابات افتراضية يتم استخدامها إذا لم يتم تعيين الحساب المقابل الافتراضي للمورّد.</td>
</tr>
<tr class="odd">
<td><strong>رأس دفتر اليومية</strong> – قم بإعداد الحساب المقابل الافتراضي لدفتر يومية كإدخال افتراضي في صفحات إيصال دفتر اليومية. لاحظ أنه لا يمكنك تعيين الحسابات المقابلة الافتراضية في رأس دفتر اليومية، إذا كان نوع دفتر اليومية لأسماء دفاتر اليومية هو <strong>سجل الفواتير</strong> أو <strong>الموافقة</strong>.</td>
<td>إدخالات دفتر اليومية في دفتر اليومية</td>
<td>قم بإعداد الحساب المقابل الافتراضي لدفتر يومية مستخدم كإدخال افتراضي في صفحات إيصال دفتر اليومية.</td>
<td>استخدم هذا الخيار للمساعدة في تسريع إدخال البيانات إذا كان لمعظم الإدخالات في دفتر يومية نفس الحساب المقابل.</td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]