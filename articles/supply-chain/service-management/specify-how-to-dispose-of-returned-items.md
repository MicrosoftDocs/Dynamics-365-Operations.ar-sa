---
title: تحديد كيفية التخلص من الأصناف المرتجعة
description: تحديد كيفية التخلص من الأصناف المرتجعة.
author: sorenva
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3123f49ef5fbd07afa61b035a2f6dd4c0af2ce40
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/03/2022
ms.locfileid: "8679208"
---
# <a name="specify-how-to-dispose-of-returned-items"></a>تحديد كيفية التخلص من الأصناف المرتجعة

[!include [banner](../includes/banner.md)]

عند معالجة أمر إرجاع، عليك تحديد كود سبب إرجاع لتحديد سبب إرجاع المنتج. يجب عليك أيضًا تحديد رمز الإرجاع وإجراء الإرجاع الذي يجب اتخاذه مع المنتج المرتجع ذاته.

يمكن تطبيق كود الترتيب عند إنشاء أمر الإرجاع وتسجيل وصول صنف أو تحديث كشف التعبئة الخاص بوصول صنف وكذلك عند إنهاء أمر إدخال مخزن الفحص.

يمكنك تحديد أية رموز إرجاع ضرورية تحتاجها لدعم عمليات الأعمال. ويوفر الجدول التالي مجموعة من الرموز المستخدمة بشكلٍ نموذجي لتعيين ترتيب صنف مرتجع.

<table>
<colgroup>
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>نوع الترتيب</p></th>
<th><p>الكود العام</p></th>
<th><p>‏‏الوصف</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>التخلص</p></td>
<td><p>SC</p></td>
<td><p>خردة/تالف</p></td>
</tr>
<tr class="even">
<td><p>التخلص</p></td>
<td><p>DC</p></td>
<td><p>التبرع للأعمال الخيرية</p></td>
</tr>
<tr class="odd">
<td><p>التخلص</p></td>
<td><p>TD</p></td>
<td><p>التخلص الخاص بجهة أخرى</p></td>
</tr>
<tr class="even">
<td><p>التخلص</p></td>
<td><p>SL</p></td>
<td><p>المسترد</p></td>
</tr>
<tr class="odd">
<td><p>التخلص</p></td>
<td><p>TS</p></td>
<td><p>مبيعات جهة أخرى (أسواق ثانوية)</p></td>
</tr>
<tr class="even">
<td><p>إصلاح/تعديل</p></td>
<td><p>RW</p></td>
<td><p>إعادة العمل</p></td>
</tr>
<tr class="odd">
<td><p>إصلاح/تعديل</p></td>
<td><p>RF</p></td>
<td><p>جهة إعادة التصنيع/التجديد</p></td>
</tr>
<tr class="even">
<td><p>إصلاح/تعديل</p></td>
<td><p>MD</p></td>
<td><p>تعديل</p></td>
</tr>
<tr class="odd">
<td><p>إصلاح/تعديل</p></td>
<td><p>RP</p></td>
<td><p>تعديل</p></td>
</tr>
<tr class="even">
<td><p>إصلاح/تعديل</p></td>
<td><p>RV</p></td>
<td><p>إرجاع إلى المورّد</p></td>
</tr>
<tr class="odd">
<td><p>أخرى</p></td>
<td><p>AI</p></td>
<td><p>الاستخدام على حالتها</p></td>
</tr>
<tr class="even">
<td><p>آخر</p></td>
<td><p>RS</p></td>
<td><p>إعادة البيع</p></td>
</tr>
<tr class="odd">
<td><p>آخر</p></td>
<td><p>EX</p></td>
<td><p>التبادل</p></td>
</tr>
<tr class="even">
<td><p>آخر</p></td>
<td><p>سيدة</p></td>
<td><p>متنوع</p></td>
</tr>
</tbody>
</table>


عليك تحديد إجراء الترتيب لكل رمز ترتيب تقوم بتحديده. يحدد إجراء الترتيب المعاني الفعلية والمالية لرموز الترتيب. على سبيل المثال، يحدد إجراء الترتيب المعالجة الفعلية للصنف المرتجع، والتأثير المالي للصنف المرتجع، وما إذا كان يجب إرسال صنف استبدال للعميل. يمكنك تحديد عدد غير محدود لرموز الإرجاع وفقًا لاحتياجات العمل الخاصة بك، ولكن يوجد فقط ستة إجراءات ترتيب معرفة مسبقًا يجب أن تحدد منها. ويسرد الجدول التالي إجراءات الترتيب وتعريفاتها.

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>إجراءات الترتيب</p></th>
<th><p>الوصف</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>يضع في الحساب مبلغاً دائناً</strong></p></td>
<td><p>إرجاع الصنف إلى المخزون وائتمان العميل.</p></td>
</tr>
<tr class="even">
<td><p><strong>يضع في الحساب مبلغاً دائناً فقط</strong></p></td>
<td><p>ائتمان العميل بدون السؤال عن أو توقع إرجاع الصنف.</p></td>
</tr>
<tr class="odd">
<td><p><strong>خردة</strong></p></td>
<td><p>تخريد الصنف وائتمان العميل.</p></td>
</tr>
<tr class="even">
<td><p><strong>استبدال وائتمان</strong></p></td>
<td><p>إرجاع الصنف إلى المخزون وإنشاء أمر استبدال وائتمان العميل.</p></td>
</tr>
<tr class="odd">
<td><p><strong>استبدال وتخريد</strong></p></td>
<td><p>تخريد الصنف وإنشاء أمر استبدال وائتمان العميل.</p></td>
</tr>
<tr class="even">
<td><p><strong>إرجاع إلى العميل</strong></p></td>
<td><p>رفض الصنف المرتجع وإعادته إلى العميل.</p></td>
</tr>
</tbody>
</table>

## <a name="select-a-disposition-code-for-a-quarantine-order"></a>تحديد كود توزيع لأمر إدخال مخزن الفحص

1. ‏‫انتقل إلى **إدارة المخزون** \> **دوري‏‎** \> **إدارة الجودة** \> **أوامر إدخال مخزن العزل**.
1. بالنسبة لأمر إدخال مخزن الفحص الموجود، حدد إجراءً من الحقل **رمز الإرجاع** من علامة التبويب **نظرة عامة**.

## <a name="see-also"></a>راجع أيضًا

[أمر إدخال مخزن الفحص (نموذج)](/dynamicsax-2012//quarantine-order-form)

[أكواد الترتيب (نموذج)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
