---
title: "بناء جملة الاستعلام والتصفية المتقدمة"
description: "توضح هذه المقالة خيارات التصفية والاستعلام التي تتوفر عند استخدام عامل التشغيل &quot;تطابق&quot; في مربع الحوار &quot;عامل التصفية/الفرز المتقدم&quot;."
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysQueryForm
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 5ee7a04572e350a7c08d0418bade6d332aa920c6
ms.lasthandoff: 03/31/2017


---

# <a name="advanced-filtering-and-query-syntax"></a>بناء جملة الاستعلام والتصفية المتقدمة

توضح هذه المقالة خيارات التصفية والاستعلام التي تتوفر عند استخدام عامل التشغيل "تطابق" في مربع الحوار "عامل التصفية/الفرز المتقدم".

<a name="advanced-query-syntax"></a>بناء جملة الاستعلام المتقدمة
---------------------

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>بناء الجملة</th>
<th>وصف الحرف</th>
<th>‏‏الوصف</th>
<th>مثال</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>قيمة</em></td>
<td>مساوية للقيمة التي تم إدخالها</td>
<td>اكتب القيمة التي ترغب في البحث عنها.</td>
<td><strong>السيد</strong> البحث عن &quot;سميث&quot;.</td>
</tr>
<tr class="even">
<td>! <em>قيمة</em> (علامة تعجب)</td>
<td>غير مساوية للقيمة التي تم إدخالها</td>
<td>اكتب علامة تعجب، ثم القيمة لاستبعادها.</td>
<td><strong>! السيد</strong> يبحث عن قيم كافة ما عدا &quot;سميث&quot;.</td>
</tr>
<tr class="odd">
<td><em>القيمة من</em>..<em>القيمة إلى</em> (نقطة مزدوجة)‬</td>
<td>بين القيمتين اللتين تم الفصل بينهما بنقطتين مزدوجتين</td>
<td>اكتب القيمة من، ثم نقطتين، ثم قيمة إلى.</td>
<td><strong>1..10</strong> يبحث عن كافة القيم من 1 إلى 10. ومع ذلك، في حقل سلسلة، <strong>أ. ج</strong> يبحث عن كافة القيم التي تبدأ ب &quot;A&quot; و &quot;ب&quot;، والقيم التي تساوي تماما &quot;ج&quot;. على سبيل المثال، لن يجد هذا الاستعلام &quot;Ca&quot;. للبحث عن قيم كل من &quot;A*&quot; من خلال &quot;ج*&quot;، نوع <strong>أ. D</strong>.</td>
</tr>
<tr class="even">
<td>..<em>القيمة</em> (نقطة مزدوجة)</td>
<td>أقل من أو تساوي القيمة التي تم إدخالها</td>
<td>اكتب النقطتين ثم القيمة.</td>
<td><strong>.. 1000</strong> أي رقم يكون أقل من أو يساوي 1000، مثل &quot;100&quot;، &quot;999.95&quot;، و &quot;1000&quot;.</td>
</tr>
<tr class="odd">
<td><em>القيمة</em>.. (نقاط مزدوجة)</td>
<td>أكبر من القيمة التي تم إدخالها أو مساوية لها</td>
<td>اكتب القيمة ثم النقطتين.</td>
<td><strong>1000..</strong> أي رقم يكون أكبر من أو يساوي 1000، مثل &quot;1000&quot;، &quot;1,000.01&quot;، و &quot;1000000&quot;.</td>
</tr>
<tr class="even">
<td>&gt;<em>قيمة</em> (أكبر من تسجيل)</td>
<td>أكبر من القيمة التي تم إدخالها</td>
<td>اكتب علامة أكبر من (<strong>&gt;</strong>) ومن ثم القيمة.</td>
<td><strong>&gt;1000</strong> أي رقم أكبر من 1000، مثل &quot;1000.01&quot;، &quot;20000&quot;، و &quot;1000000&quot;.</td>
</tr>
<tr class="odd">
<td>&lt;<em>قيمة</em> (أقل من تسجيل)</td>
<td>أقل من القيمة التي تم إدخالها</td>
<td>اكتب أقل من (<strong>&lt;</strong>) ومن ثم القيمة.</td>
<td><strong>&lt;1000</strong> أي رقم هو أقل من 1000، مثل &quot;999.99&quot;، &quot;1&quot;، و &quot;-200&quot;.</td>
</tr>
<tr class="even">
<td><em>قيمة</em>* علامة نجمية (*)</td>
<td>تبدأ من القيمة التي تم إدخالها</td>
<td>اكتب قيمة البداية ثم علامة نجمة (<strong>*</strong>).</td>
<td><strong>S *</strong> بالعثور على أي سلسلة تبدأ ب &quot;S&quot;، مثل &quot;استكهولم&quot;، &quot;سيدني&quot;، و &quot;سان فرانسيسكو&quot;.</td>
</tr>
<tr class="odd">
<td>*<em>value</em> (asterisk)</td>
<td>الانتهاء بالقيمة التي تم إدخالها</td>
<td>اكتب علامة النجمة ثم قيمة الانتهاء.</td>
<td><strong>* شرق</strong> بالعثور على أي سلسلة تنتهي ب &quot;الشرقية&quot;، مثل &quot;شمال شرق&quot; و &quot;جنوب شرق&quot;.</td>
</tr>
<tr class="even">
<td>*<em>قيمة</em>* علامة نجمية (*)</td>
<td>تحتوي على القيمة التي تم إدخالها</td>
<td>اكتب علامة النجمة ثم القيمة ثم علامة نجمة أخرى.</td>
<td><strong>*ال*</strong> بالعثور على أي سلسلة التي تحتوي على &quot;ال&quot;، مثل &quot;شمال شرق&quot; و &quot;جنوب شرق&quot;.</td>
</tr>
<tr class="odd">
<td>؟ (علامة استفهام)</td>
<td>وجود حرف واحد أو أكثر غير معروف</td>
<td>اكتب علامة استفهام في موضع الحرف غير المعروف في القيمة.</td>
<td><strong>رش؟ د</strong> يرى &quot;سميث&quot; و &quot;رشيد&quot;.</td>
</tr>
<tr class="even">
<td><em>قيمة</em>،<em>قيمة</em> (فاصلة)</td>
<td>مطابقة القيم التي تم الفصل بينها بفواصل.</td>
<td>اكتب كافة المعايير، وافصلها ياستخدام الفواصل.</td>
<td><strong>A, D, F, G</strong> finds exactly &quot;A&quot;, &quot;D&quot;, &quot;F&quot;, and &quot;G&quot;. <strong>10، 20 و 30 و 100</strong> يرى تماما &quot;10، 20 و 30 و 100&quot;.</td>
</tr>
<tr class="odd">
<td>(<span class="code">عبارة SQL</span>) (عبارة SQL بين قوسين)</td>
<td>مطابقة استعلام محدد</td>
<td>اكتب استعلامًا على هيئة عبارة SQL بين قوسين.</td>
<td><strong><span class="code">(مصدر البيانات. اسم الحقل! = &quot;A&quot;)</span></strong></td>
</tr>
<tr class="even">
<td>ث</td>
<td>تاريخ اليوم</td>
<td>اكتب <strong>T</strong>.</td>
<td><strong>T</strong> تطابق تاريخ اليوم (today's date).</td>
</tr>
<tr class="odd">
<td>(methodName(parameters‏‏)‏) (طريقة <strong>SysQueryRangeUtil</strong> بين قوسين)</td>
<td>مطابقة القيمة أو نطاق القيم المحددة من قِبل المعلمات لطريقة <strong>SysQueryRangeUtil</strong></td>
<td>اكتب طريقة <strong>SysQueryRangeUtil</strong> التي تشتمل على معلمات تحدد قيمة أو نطاق القيم. </td>
<td><ol>
<li>انقر فوق <strong>الحسابات المدينة</strong>&gt;<strong>فواتير</strong>&gt;<strong>فتح فواتير العملاء</strong>.</li>
<li>اضغط على Ctrl + Shift + F3 لفتح صفحة <strong>الاستعلام</strong>.</li>
<li>في علامة التبويب <strong>نطاق</strong>، انقر فوق <strong>إضافة</strong>.</li>
<li>في حقل <strong>الجدول</strong>، حدد <strong>حركات العملاء المفتوحة</strong>.</li>
<li>في حقل <strong>المجال</strong>، حدد <strong>تاريخ الاستحقاق</strong>.</li>
<li>في حقل <strong>المعايير</strong>، أدخل <strong>(المعدل السنوي(-2,0))</strong>.</li>
<li>وانقر فوق <strong>موافق</strong>. يتم تحديث صفحة القائمة وتسرد الفواتير التي تتطابق مع المعيار الذي حددته. في هذا المثال، يتم سرد الفواتير المستحقة في السنتين الماضيتين.</li>
</ol>
راجع الجدول الموجود في القسم التالي للحصول على تفاصيل إضافية عن طرق حساب تاريخ <strong>SysQueryRangeUtil</strong>، والعديد من الأمثلة.</td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a>الاستعلامات بتواريخ متقدمة التي تستخدم طرق SysQueryRangeUtil
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>الأسلوب</th>
<th>الوصف</th>
<th>مثال</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>اليوم (_‏‏relativeDays=0)</td>
<td>ابحث عن تاريخ بالنسبة لتاريخ الجلسة. تشير القيم الإيجابية إلى التواريخ المستقبلية، وتشير القيم السالبة إلى تواريخ في الماضي.</td>
<td><ul>
<li><strong>الغد</strong> – أدخل<strong>(يوم (1))</strong>.</li>
<li><strong>اليوم</strong> – أدخل <strong>(يوم (0))</strong>.</li>
<li><strong>الأمس</strong> – أدخل <strong>(يوم (-1))</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>نطاق الأيام (_relativeDaysFrom=0, _relativeDaysTo=0)</td>
<td>ابحث عن نطاق تواريخ بالنسبة لتاريخ الجلسة. تشير القيم الإيجابية إلى التواريخ المستقبلية، وتشير القيم السالبة إلى تواريخ في الماضي.</td>
<td><ul>
<li><strong>آخر 30 يومًا</strong> – أدخل <strong>(نطاق الأيام (-30,0))</strong>.</li>
<li><strong>الـ 30 يومًا السابقة والـ 30 يومًا التالية </strong> – أدخل <strong>(نطاق الأيام (-30,30))</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</td>
<td>البحث عن كافة التواريخ بعد التاريخ النسبي المحدد.</td>
<td><ul>
<li><strong>أكثر من 30 يومًا من الآن</strong> – أدخل <strong>(GreaterThanDate(30))</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>GreaterThanUtcNow ()</td>
<td>البحث عن كافة إدخالات التاريخ/الوقت بعد الوقت الحالي.</td>
<td><ul>
<li><strong>كل التواريخ/الأوقات المستقبلية</strong> – أدخل <strong>(GreaterThanUtcNow())</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</td>
<td>البحث عن كافة التواريخ قبل التاريخ النسبي المحدد.</td>
<td><ul>
<li><strong>أقل من سبعة أيام من الآن</strong> – أدخل <strong>(LessThanDate(7))</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>LessThanUtcNow ()</td>
<td>البحث عن كافة إدخالات التاريخ/الوقت قبل الوقت الحالي.</td>
<td><ul>
<li><strong>كافة التواريخ/الأوقات السابقة</strong> – أدخل <strong>(LessThanUtcNow())</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>نطاق الأشهر (_relativeFrom=0, _relativeTo=0)</td>
<td>البحث عن مجموعة من التواريخ، على أساس الأشهر بالنسبة للشهر الحالي.</td>
<td><ul>
<li><strong>الشهران السابقان</strong> – أدخل <strong>(MonthRange(-2,0))</strong>.</li>
<li><strong>الأشهر الثلاثة المقبلة</strong> – أدخل <strong>(MonthRange(0,3))</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>نطاق السنوات (_relativeFrom=0, _relativeTo=0)</td>
<td>ابحث عن مجموعة من التواريخ، على أساس السنوات بالنسبة للسنة الحالية.</td>
<td><ul>
<li><strong>السنة القادمة</strong> – أدخل<strong>(YearRange(0, 1))</strong>.</li>
<li><strong>السنة السابقة</strong> – أدخل <strong>(YearRange(-1,0))</strong>.</li>
</ul></td>
</tr>
</tbody>
</table>




