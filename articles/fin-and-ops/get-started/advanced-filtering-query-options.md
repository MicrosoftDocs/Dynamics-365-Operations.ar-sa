---
title: التصفية المتقدمة وبنية الاستعلام
description: يوضح هذا الموضوع خيارات التصفية والاستعلام التي تتوفر عند استخدام مربع الحوار التصفية/الفرز المتقدم أو عامل تشغيل تطابق في جزء عامل التصفية أو عوامل تصفية عناوين أعمدة الشبكة.
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 01a508e97721099f92b9167dfdfa1b9669b9341c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546998"
---
# <a name="advanced-filtering-and-query-syntax"></a>التصفية المتقدمة وبنية الاستعلام

[!include [banner](../includes/banner.md)]

يوضح هذا الموضوع خيارات التصفية والاستعلام التي تتوفر عند استخدام مربع الحوار التصفية/الفرز المتقدم أو عامل تشغيل **تطابق** في جزء عامل التصفية أو عوامل تصفية عناوين أعمدة الشبكة.

## <a name="advanced-query-syntax"></a>‏‫بنية الاستعلام المتقدمة

<table>
<thead>
<tr>
<th>بناء الجملة</th>
<th>وصف الحرف</th>
<th>الوصف</th>
<th>مثال</th>
</tr>
</thead>
<tbody>
<tr>
<td><em>قيمة</em></td>
<td>مساوية للقيمة التي تم إدخالها</td>
<td>اكتب القيمة التي ترغب في البحث عنها.</td>
<td><strong>أشرف</strong> يتم البحث عن &quot;أشرف&quot;.</td>
</tr>
<tr>
<td>!<em>القيمة‬</em> (علامة التعجب)</td>
<td>غير مساوية للقيمة التي تم إدخالها</td>
<td>اكتب علامة تعجب، ثم القيمة لاستبعادها.</td>
<td><strong>!أشرف</strong> يتم البحث عن كل القيم ما عدا &quot;أشرف&quot;.</td>
</tr>
<tr>
<td><em>القيمة من</em>..<em>القيمة إلى</em> (نقطة مزدوجة)‬</td>
<td>بين القيمتين اللتين تم الفصل بينهما بنقطتين مزدوجتين</td>
<td>اكتب القيمة من، ثم نقطتين، ثم قيمة إلى.</td>
<td><strong>1..10</strong> يتم البحث عن جميع القيم من 1 وحتى 10. ومع ذلك، في حقل السلسلة <strong>أ..ج</strong>، يتم البحث عن جميع القيم التي تبدأ بـ &quot;أ&quot; و&quot;ب&quot;، والقيم المساوية تمامًا لـ &quot;ج&quot;. على سبيل المثال، لن يبحث هذا الاستعلام عن &quot;جأ&quot;. للبحث عن جميع القيم بدءًا من &quot;أ<em>&quot; وحتى &quot;ج</em>&quot;، اكتب <strong>أ..د</strong>.</td>
</tr>
<tr>
<td>..<em>القيمة</em> (نقطة مزدوجة)</td>
<td>أقل من أو تساوي القيمة التي تم إدخالها</td>
<td>اكتب النقطتين ثم القيمة.</td>
<td><strong>..1000</strong> يتم البحث عن أي رقم أقل من 1000 أو مساوٍ له، على سبيل المثال، &quot;100&quot;، و&quot;999.95&quot;، و&quot;1000&quot;.</td>
</tr>
<tr>
<td><em>القيمة</em>.. (نقاط مزدوجة)</td>
<td>أكبر من القيمة التي تم إدخالها أو مساوية لها</td>
<td>اكتب القيمة ثم النقطتين.</td>
<td><strong>1000..</strong> يتم البحث عن أي رقم أكبر من 1000 أو مساوٍ له، على سبيل المثال، &quot;1000&quot;، و&quot;1000.01&quot;، و&quot;1000000&quot;.</td>
</tr>
<tr>
<td>&gt;<em>القيمة</em> (علامة أكبر من)</td>
<td>أكبر من القيمة التي تم إدخالها</td>
<td>اكتب علامة أكبر من (<strong>&gt;</strong>) ثم القيمة.</td>
<td><strong>&gt;1000</strong> يتم البحث عن أي رقم أكبر من 1000، على سبيل المثال، &quot;1000.01&quot;، و&quot;20000&quot;، و&quot;1000000&quot;.</td>
</tr>
<tr>
<td>&lt;<em>القيمة</em> (علامة أصغر من)</td>
<td>أقل من القيمة التي تم إدخالها</td>
<td>اكتب علامة أقل من (<strong>&lt;</strong>) ثم القيمة.</td>
<td><strong>&lt;1000</strong> يتم البحث عن أي رقم أصغر من 1000، على سبيل المثال، &quot;999.99&quot;، و&quot;1&quot;، و&quot;-200&quot;.</td>
</tr>
<tr>
<td><em>القيمة</em>* (العلامة النجمية)</td>
<td>تبدأ من القيمة التي تم إدخالها</td>
<td>اكتب قيمة البدء ثم علامة نجمية (<strong>*</strong>).</td>
<td><strong>س*</strong> يتم البحث عن أية سلسلة تبدأ بـ &quot;س&quot;، مثل &quot;ستوكهولم&quot;، و&quot;سيدني&quot;، و&quot;سان فرانسيسكو&quot;.</td>
</tr>
<tr>
<td>*<em>القيمة</em> (العلامة النجمية)</td>
<td>الانتهاء بالقيمة التي تم إدخالها</td>
<td>اكتب علامة النجمة ثم قيمة الانتهاء.</td>
<td><strong>*شرق</strong> يتم البحث عن أي سلسلة تنتهي بـ &quot;شرق&quot;، مثل &quot;شمال شرق&quot; و&quot;جنوب شرق&quot;.</td>
</tr>
<tr>
<td>*<em>القيمة</em>* (العلامة النجمية)</td>
<td>تحتوي على القيمة التي تم إدخالها</td>
<td>اكتب علامة النجمة ثم القيمة ثم علامة نجمة أخرى.</td>
<td><strong>*رق*</strong> يتم البحث عن أي سلسلة تحتوي على &quot;رق&quot;، مثل &quot;شمال شرق&quot; و&quot;جنوب شرق&quot;.</td>
</tr>
<tr>
<td>؟ (علامة استفهام)</td>
<td>وجود حرف واحد أو أكثر غير معروف</td>
<td>اكتب علامة استفهام في موضع الحرف غير المعروف في القيمة.</td>
<td><strong>أش؟ف</strong> يتم البحث عن &quot;أشرف&quot; و&quot;أشراف&quot;.</td>
</tr>
<tr>
<td><em>قيمة</em>،<em>قيمة</em> (فاصلة)</td>
<td>مطابقة القيم التي تم الفصل بينها بفواصل.</td>
<td>اكتب كافة المعايير، وافصلها ياستخدام الفواصل.</td>
<td><strong>A, D, F, G</strong> يبحث تمامًا عن &quot;أ&quot; و&quot;د&quot; و&quot;ز&quot; و&quot;ح&quot;. <strong>10, 20, 30, 100</strong> يبحث تمامًا عن &quot;10 و20 و30 و100&quot;.</td>
</tr>
<tr>
<td>(<span class="code">عبارة SQL</span>) (عبارة SQL بين قوسين)</td>
<td>مطابقة استعلام محدد</td>
<td>اكتب استعلامًا على هيئة عبارة SQL بين قوسين.</td>
<td><strong><span class="code">(مصدر البيانات.اسم الحقل != &quot;A&quot;)</span></strong></td>
</tr>
<tr>
<td>ث</td>
<td>تاريخ اليوم</td>
<td>اكتب <strong>T</strong>.</td>
<td><strong>T</strong> تطابق تاريخ اليوم (today's date).</td>
</tr>
<tr>
<td>(methodName(parameters‏‏)‏) (طريقة <strong>SysQueryRangeUtil</strong> بين قوسين)</td>
<td>مطابقة القيمة أو نطاق القيم المحددة من قِبل المعلمات لطريقة <strong>SysQueryRangeUtil</strong></td>
<td>اكتب طريقة <strong>SysQueryRangeUtil</strong> التي تشتمل على معلمات تحدد قيمة أو نطاق القيم. </td>
<td>
<ol>
<li>انقر فوق <strong>الحسابات المدينة</strong> &gt; <strong>الفواتير</strong> &gt; <strong>فواتير العملاء المفتوحة</strong>.</li>
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
<thead>
<tr>
<th>الأسلوب</th>
<th>الوصف</th>
<th>مثال</th>
</tr>
</thead>
<tbody>
<tr>
<td>اليوم (_‏‏relativeDays=0)</td>
<td>ابحث عن تاريخ بالنسبة لتاريخ الجلسة. تشير القيم الإيجابية إلى التواريخ المستقبلية، وتشير القيم السالبة إلى تواريخ في الماضي.</td>
<td>
<ul>
<li><strong>الغد</strong> – أدخل<strong>(يوم (1))</strong>.</li>
<li><strong>اليوم</strong> – أدخل <strong>(يوم (0))</strong>.</li>
<li><strong>الأمس</strong> – أدخل <strong>(يوم (-1))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>نطاق الأيام (_relativeDaysFrom=0, _relativeDaysTo=0)</td>
<td>ابحث عن نطاق تواريخ بالنسبة لتاريخ الجلسة. تشير القيم الإيجابية إلى التواريخ المستقبلية، وتشير القيم السالبة إلى تواريخ في الماضي.</td>
<td>
<ul>
<li><strong>آخر 30 يومًا</strong> – أدخل <strong>(نطاق الأيام (-30,0))</strong>.</li>
<li><strong>الـ 30 يومًا السابقة والـ 30 يومًا التالية </strong> – أدخل <strong>(نطاق الأيام (-30,30))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</td>
<td>البحث عن كافة التواريخ بعد التاريخ النسبي المحدد.</td>
<td>
<ul>
<li><strong>أكثر من 30 يومًا من الآن</strong> – أدخل <strong>(GreaterThanDate(30))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>GreaterThanUtcNow ()</td>
<td>البحث عن كافة إدخالات التاريخ/الوقت بعد الوقت الحالي.</td>
<td>
<ul>
<li><strong>كل التواريخ/الأوقات المستقبلية</strong> – أدخل <strong>(GreaterThanUtcNow())</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</td>
<td>البحث عن كافة التواريخ قبل التاريخ النسبي المحدد.</td>
<td>
<ul>
<li><strong>أقل من سبعة أيام من الآن</strong> – أدخل <strong>(LessThanDate(7))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>LessThanUtcNow ()</td>
<td>البحث عن كافة إدخالات التاريخ/الوقت قبل الوقت الحالي.</td>
<td>
<ul>
<li><strong>كافة التواريخ/الأوقات السابقة</strong> – أدخل <strong>(LessThanUtcNow())</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>نطاق الأشهر (_relativeFrom=0, _relativeTo=0)</td>
<td>البحث عن مجموعة من التواريخ، على أساس الأشهر بالنسبة للشهر الحالي.</td>
<td>
<ul>
<li><strong>الشهران السابقان</strong> – أدخل <strong>(MonthRange(-2,0))</strong>.</li>
<li><strong>الأشهر الثلاثة المقبلة</strong> – أدخل <strong>(MonthRange(0,3))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>نطاق السنوات (_relativeFrom=0, _relativeTo=0)</td>
<td>ابحث عن مجموعة من التواريخ، على أساس السنوات بالنسبة للسنة الحالية.</td>
<td>
<ul>
<li><strong>السنة القادمة</strong> – أدخل<strong>(YearRange(0, 1))</strong>.</li>
<li><strong>السنة السابقة</strong> – أدخل <strong>(YearRange(-1,0))</strong>.</li>
</ul>
</td>
</tr>
</tbody>
</table>
