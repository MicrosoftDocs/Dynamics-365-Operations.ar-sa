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
ms.openlocfilehash: f9e57cac740a26c6c5b451c92d856e533c6db33e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180819"
---
# <a name="advanced-filtering-and-query-syntax"></a><span data-ttu-id="ce039-103">التصفية المتقدمة وبنية الاستعلام</span><span class="sxs-lookup"><span data-stu-id="ce039-103">Advanced filtering and query syntax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce039-104">يوضح هذا الموضوع خيارات التصفية والاستعلام التي تتوفر عند استخدام مربع الحوار التصفية/الفرز المتقدم أو عامل تشغيل **تطابق** في جزء عامل التصفية أو عوامل تصفية عناوين أعمدة الشبكة.</span><span class="sxs-lookup"><span data-stu-id="ce039-104">This article describes the filtering and query options that are available when you use the Advanced filter/sort dialog or the **matches** operator in the Filter pane or grid column header filters.</span></span>

## <a name="advanced-query-syntax"></a><span data-ttu-id="ce039-105">‏‫بنية الاستعلام المتقدمة</span><span class="sxs-lookup"><span data-stu-id="ce039-105">Advanced query syntax</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ce039-106">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="ce039-106">Syntax</span></span></th>
<th><span data-ttu-id="ce039-107">وصف الحرف</span><span class="sxs-lookup"><span data-stu-id="ce039-107">Character description</span></span></th>
<th><span data-ttu-id="ce039-108">الوصف</span><span class="sxs-lookup"><span data-stu-id="ce039-108">Description</span></span></th>
<th><span data-ttu-id="ce039-109">مثال</span><span class="sxs-lookup"><span data-stu-id="ce039-109">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ce039-110"><em>قيمة</em></span><span class="sxs-lookup"><span data-stu-id="ce039-110"><em>value</em></span></span></td>
<td><span data-ttu-id="ce039-111">مساوية للقيمة التي تم إدخالها</span><span class="sxs-lookup"><span data-stu-id="ce039-111">Equal to the value that is entered</span></span></td>
<td><span data-ttu-id="ce039-112">اكتب القيمة التي ترغب في البحث عنها.</span><span class="sxs-lookup"><span data-stu-id="ce039-112">Type the value to find.</span></span></td>
<td><span data-ttu-id="ce039-113"><strong>أشرف</strong> يتم البحث عن &quot;أشرف&quot;.</span><span class="sxs-lookup"><span data-stu-id="ce039-113"><strong>Smith</strong> finds &quot;Smith&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce039-114">!<em>القيمة‬</em> (علامة التعجب)</span><span class="sxs-lookup"><span data-stu-id="ce039-114">!<em>value</em> (exclamation point)</span></span></td>
<td><span data-ttu-id="ce039-115">غير مساوية للقيمة التي تم إدخالها</span><span class="sxs-lookup"><span data-stu-id="ce039-115">Not equal to the value that is entered</span></span></td>
<td><span data-ttu-id="ce039-116">اكتب علامة تعجب، ثم القيمة لاستبعادها.</span><span class="sxs-lookup"><span data-stu-id="ce039-116">Type an exclamation point and then the value to exclude.</span></span></td>
<td><span data-ttu-id="ce039-117"><strong>!أشرف</strong> يتم البحث عن كل القيم ما عدا &quot;أشرف&quot;.</span><span class="sxs-lookup"><span data-stu-id="ce039-117"><strong>!Smith</strong> finds all values except &quot;Smith&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce039-118"><em>القيمة من</em>..<em>القيمة إلى</em> (نقطة مزدوجة)‬</span><span class="sxs-lookup"><span data-stu-id="ce039-118"><em>from-value</em>..<em>to-value</em> (double period)</span></span></td>
<td><span data-ttu-id="ce039-119">بين القيمتين اللتين تم الفصل بينهما بنقطتين مزدوجتين</span><span class="sxs-lookup"><span data-stu-id="ce039-119">Between the two values that are separated by double periods</span></span></td>
<td><span data-ttu-id="ce039-120">اكتب القيمة من، ثم نقطتين، ثم قيمة إلى.</span><span class="sxs-lookup"><span data-stu-id="ce039-120">Type the from-value, then two periods, and then the to-value.</span></span></td>
<td><span data-ttu-id="ce039-121"><strong>1..10</strong> يتم البحث عن جميع القيم من 1 وحتى 10.</span><span class="sxs-lookup"><span data-stu-id="ce039-121"><strong>1..10</strong> finds all values from 1 through 10.</span></span> <span data-ttu-id="ce039-122">ومع ذلك، في حقل السلسلة <strong>أ..ج</strong>، يتم البحث عن جميع القيم التي تبدأ بـ &quot;أ&quot; و&quot;ب&quot;، والقيم المساوية تمامًا لـ &quot;ج&quot;.</span><span class="sxs-lookup"><span data-stu-id="ce039-122">However, in a string field, <strong>A..C</strong> finds all values that start with &quot;A&quot; and &quot;B&quot;, and values that are exactly equal to &quot;C&quot;.</span></span> <span data-ttu-id="ce039-123">على سبيل المثال، لن يبحث هذا الاستعلام عن &quot;جأ&quot;.</span><span class="sxs-lookup"><span data-stu-id="ce039-123">For example, this query won't find &quot;Ca&quot;.</span></span> <span data-ttu-id="ce039-124">للبحث عن جميع القيم بدءًا من &quot;أ<em>&quot; وحتى &quot;ج</em>&quot;، اكتب <strong>أ..د</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce039-124">To find all values from &quot;A<em>&quot; through &quot;C</em>&quot;, type <strong>A..D</strong>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce039-125">..<em>القيمة</em> (نقطة مزدوجة)</span><span class="sxs-lookup"><span data-stu-id="ce039-125">..<em>value</em> (double period)</span></span></td>
<td><span data-ttu-id="ce039-126">أقل من أو تساوي القيمة التي تم إدخالها</span><span class="sxs-lookup"><span data-stu-id="ce039-126">Less than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="ce039-127">اكتب النقطتين ثم القيمة.</span><span class="sxs-lookup"><span data-stu-id="ce039-127">Type two periods and then the value.</span></span></td>
<td><span data-ttu-id="ce039-128"><strong>..1000</strong> يتم البحث عن أي رقم أقل من 1000 أو مساوٍ له، على سبيل المثال، &quot;100&quot;، و&quot;999.95&quot;، و&quot;1000&quot;.</span><span class="sxs-lookup"><span data-stu-id="ce039-128"><strong>..1000</strong> finds any number that is less than or equal to 1000, such as &quot;100&quot;, &quot;999.95&quot;, and &quot;1,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce039-129"><em>القيمة</em>..</span><span class="sxs-lookup"><span data-stu-id="ce039-129"><em>value</em>..</span></span> <span data-ttu-id="ce039-130">(نقاط مزدوجة)</span><span class="sxs-lookup"><span data-stu-id="ce039-130">(double period)</span></span></td>
<td><span data-ttu-id="ce039-131">أكبر من القيمة التي تم إدخالها أو مساوية لها</span><span class="sxs-lookup"><span data-stu-id="ce039-131">Greater than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="ce039-132">اكتب القيمة ثم النقطتين.</span><span class="sxs-lookup"><span data-stu-id="ce039-132">Type the value and then two periods.</span></span></td>
<td><span data-ttu-id="ce039-133"><strong>1000..</strong></span><span class="sxs-lookup"><span data-stu-id="ce039-133"><strong>1000..</strong></span></span> <span data-ttu-id="ce039-134">يتم البحث عن أي رقم أكبر من 1000 أو مساوٍ له، على سبيل المثال، &quot;1000&quot;، و&quot;1000.01&quot;، و&quot;1000000&quot;.</span><span class="sxs-lookup"><span data-stu-id="ce039-134">finds any number that is greater than or equal to 1000, such as &quot;1,000&quot;, &quot;1,000.01&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce039-135">&gt;<em>القيمة</em> (علامة أكبر من)</span><span class="sxs-lookup"><span data-stu-id="ce039-135">&gt;<em>value</em> (greater than sign)</span></span></td>
<td><span data-ttu-id="ce039-136">أكبر من القيمة التي تم إدخالها</span><span class="sxs-lookup"><span data-stu-id="ce039-136">Greater than the value that is entered</span></span></td>
<td><span data-ttu-id="ce039-137">اكتب علامة أكبر من (<strong>&gt;</strong>) ثم القيمة.</span><span class="sxs-lookup"><span data-stu-id="ce039-137">Type a greater than sign (<strong>&gt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="ce039-138"><strong>&gt;1000</strong> يتم البحث عن أي رقم أكبر من 1000، على سبيل المثال، &quot;1000.01&quot;، و&quot;20000&quot;، و&quot;1000000&quot;.</span><span class="sxs-lookup"><span data-stu-id="ce039-138"><strong>&gt;1000</strong> finds any number that is greater than 1000, such as &quot;1000.01&quot;, &quot;20,000&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce039-139">&lt;<em>القيمة</em> (علامة أصغر من)</span><span class="sxs-lookup"><span data-stu-id="ce039-139">&lt;<em>value</em> (less than sign)</span></span></td>
<td><span data-ttu-id="ce039-140">أقل من القيمة التي تم إدخالها</span><span class="sxs-lookup"><span data-stu-id="ce039-140">Less than the value that is entered</span></span></td>
<td><span data-ttu-id="ce039-141">اكتب علامة أقل من (<strong>&lt;</strong>) ثم القيمة.</span><span class="sxs-lookup"><span data-stu-id="ce039-141">Type a less than sign (<strong>&lt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="ce039-142"><strong>&lt;1000</strong> يتم البحث عن أي رقم أصغر من 1000، على سبيل المثال، &quot;999.99&quot;، و&quot;1&quot;، و&quot;-200&quot;.</span><span class="sxs-lookup"><span data-stu-id="ce039-142"><strong>&lt;1000</strong> finds any number that is less than 1000, such as &quot;999.99&quot;, &quot;1&quot;, and &quot;-200&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce039-143"><em>القيمة</em>\* (العلامة النجمية)</span><span class="sxs-lookup"><span data-stu-id="ce039-143"><em>value</em>\* (asterisk)</span></span></td>
<td><span data-ttu-id="ce039-144">تبدأ من القيمة التي تم إدخالها</span><span class="sxs-lookup"><span data-stu-id="ce039-144">Starting from the value that is entered</span></span></td>
<td><span data-ttu-id="ce039-145">اكتب قيمة البدء ثم علامة نجمية (<strong>\*</strong>).</span><span class="sxs-lookup"><span data-stu-id="ce039-145">Type the starting value and then an asterisk (<strong>\*</strong>).</span></span></td>
<td><span data-ttu-id="ce039-146"><strong>س\*</strong> يتم البحث عن أية سلسلة تبدأ بـ &quot;س&quot;، مثل &quot;ستوكهولم&quot;، و&quot;سيدني&quot;، و&quot;سان فرانسيسكو&quot;.</span><span class="sxs-lookup"><span data-stu-id="ce039-146"><strong>S\*</strong> finds any string that starts with &quot;S&quot;, such as &quot;Stockholm&quot;, &quot;Sydney&quot;, and &quot;San Francisco&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce039-147">\*<em>القيمة</em> (العلامة النجمية)</span><span class="sxs-lookup"><span data-stu-id="ce039-147">\*<em>value</em> (asterisk)</span></span></td>
<td><span data-ttu-id="ce039-148">الانتهاء بالقيمة التي تم إدخالها</span><span class="sxs-lookup"><span data-stu-id="ce039-148">Ending with the value that is entered</span></span></td>
<td><span data-ttu-id="ce039-149">اكتب علامة النجمة ثم قيمة الانتهاء.</span><span class="sxs-lookup"><span data-stu-id="ce039-149">Type an asterisk and then the ending value.</span></span></td>
<td><span data-ttu-id="ce039-150"><strong>\*شرق</strong> يتم البحث عن أي سلسلة تنتهي بـ &quot;شرق&quot;، مثل &quot;شمال شرق&quot; و&quot;جنوب شرق&quot;.</span><span class="sxs-lookup"><span data-stu-id="ce039-150"><strong>\*east</strong> finds any string that ends with &quot;east&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce039-151">*<em>القيمة</em>* (العلامة النجمية)</span><span class="sxs-lookup"><span data-stu-id="ce039-151">*<em>value</em>* (asterisk)</span></span></td>
<td><span data-ttu-id="ce039-152">تحتوي على القيمة التي تم إدخالها</span><span class="sxs-lookup"><span data-stu-id="ce039-152">Containing the value that is entered</span></span></td>
<td><span data-ttu-id="ce039-153">اكتب علامة النجمة ثم القيمة ثم علامة نجمة أخرى.</span><span class="sxs-lookup"><span data-stu-id="ce039-153">Type an asterisk, then a value, and then another asterisk.</span></span></td>
<td><span data-ttu-id="ce039-154"><strong>*رق*</strong> يتم البحث عن أي سلسلة تحتوي على &quot;رق&quot;، مثل &quot;شمال شرق&quot; و&quot;جنوب شرق&quot;.</span><span class="sxs-lookup"><span data-stu-id="ce039-154"><strong>*th*</strong> finds any string that contains &quot;th&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce039-155">؟</span><span class="sxs-lookup"><span data-stu-id="ce039-155">?</span></span> <span data-ttu-id="ce039-156">(علامة استفهام)</span><span class="sxs-lookup"><span data-stu-id="ce039-156">(question mark)</span></span></td>
<td><span data-ttu-id="ce039-157">وجود حرف واحد أو أكثر غير معروف</span><span class="sxs-lookup"><span data-stu-id="ce039-157">Having one or more unknown characters</span></span></td>
<td><span data-ttu-id="ce039-158">اكتب علامة استفهام في موضع الحرف غير المعروف في القيمة.</span><span class="sxs-lookup"><span data-stu-id="ce039-158">Type a question mark at the position of the unknown character in the value.</span></span></td>
<td><span data-ttu-id="ce039-159"><strong>أش؟ف</strong> يتم البحث عن &quot;أشرف&quot; و&quot;أشراف&quot;.</span><span class="sxs-lookup"><span data-stu-id="ce039-159"><strong>Sm?th</strong> finds &quot;Smith&quot; and &quot;Smyth&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce039-160"><em>قيمة</em>،<em>قيمة</em> (فاصلة)</span><span class="sxs-lookup"><span data-stu-id="ce039-160"><em>value</em>,<em>value</em> (comma)</span></span></td>
<td><span data-ttu-id="ce039-161">مطابقة القيم التي تم الفصل بينها بفواصل.</span><span class="sxs-lookup"><span data-stu-id="ce039-161">Matching the values that are separated by commas</span></span></td>
<td><span data-ttu-id="ce039-162">اكتب كافة المعايير، وافصلها ياستخدام الفواصل.</span><span class="sxs-lookup"><span data-stu-id="ce039-162">Type all your criteria, and separate them by using commas.</span></span></td>
<td><span data-ttu-id="ce039-163"><strong>A, D, F, G</strong> يبحث تمامًا عن &quot;أ&quot; و&quot;د&quot; و&quot;ز&quot; و&quot;ح&quot;.</span><span class="sxs-lookup"><span data-stu-id="ce039-163"><strong>A, D, F, G</strong> finds exactly &quot;A&quot;, &quot;D&quot;, &quot;F&quot;, and &quot;G&quot;.</span></span> <span data-ttu-id="ce039-164"><strong>10, 20, 30, 100</strong> يبحث تمامًا عن &quot;10 و20 و30 و100&quot;.</span><span class="sxs-lookup"><span data-stu-id="ce039-164"><strong>10, 20, 30, 100</strong> finds exactly &quot;10, 20, 30, 100&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce039-165">(<span class="code">عبارة SQL</span>) (عبارة SQL بين قوسين)</span><span class="sxs-lookup"><span data-stu-id="ce039-165">(<span class="code">SQL statement</span>) (SQL statement between parentheses)</span></span></td>
<td><span data-ttu-id="ce039-166">مطابقة استعلام محدد</span><span class="sxs-lookup"><span data-stu-id="ce039-166">Matching a defined query</span></span></td>
<td><span data-ttu-id="ce039-167">اكتب استعلامًا على هيئة عبارة SQL بين قوسين.</span><span class="sxs-lookup"><span data-stu-id="ce039-167">Type a query as an SQL statement between parentheses.</span></span></td>
<td><span data-ttu-id="ce039-168"><strong><span class="code">(مصدر البيانات.اسم الحقل != &quot;A&quot;)</span></strong></span><span class="sxs-lookup"><span data-stu-id="ce039-168"><strong><span class="code">(data source.Fieldname != &quot;A&quot;)</span></strong></span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce039-169">ث</span><span class="sxs-lookup"><span data-stu-id="ce039-169">T</span></span></td>
<td><span data-ttu-id="ce039-170">تاريخ اليوم</span><span class="sxs-lookup"><span data-stu-id="ce039-170">Today's date</span></span></td>
<td><span data-ttu-id="ce039-171">اكتب <strong>T</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce039-171">Type <strong>T</strong>.</span></span></td>
<td><span data-ttu-id="ce039-172"><strong>T</strong> تطابق تاريخ اليوم (today's date).</span><span class="sxs-lookup"><span data-stu-id="ce039-172"><strong>T</strong> matches today's date.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce039-173">(methodName(parameters‏‏)‏) (طريقة <strong>SysQueryRangeUtil</strong> بين قوسين)</span><span class="sxs-lookup"><span data-stu-id="ce039-173">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> method between parentheses)</span></span></td>
<td><span data-ttu-id="ce039-174">مطابقة القيمة أو نطاق القيم المحددة من قِبل المعلمات لطريقة <strong>SysQueryRangeUtil</strong></span><span class="sxs-lookup"><span data-stu-id="ce039-174">Matching the value or range of values that are specified by the parameters of the <strong>SysQueryRangeUtil</strong> method</span></span></td>
<td><span data-ttu-id="ce039-175">اكتب طريقة <strong>SysQueryRangeUtil</strong> التي تشتمل على معلمات تحدد قيمة أو نطاق القيم. </span><span class="sxs-lookup"><span data-stu-id="ce039-175">Type a <strong>SysQueryRangeUtil</strong> method that has parameters that specify the value or range of values.</span></span></td>
<td>
<ol>
<li><span data-ttu-id="ce039-176">انقر فوق <strong>الحسابات المدينة</strong> &gt; <strong>الفواتير</strong> &gt; <strong>فواتير العملاء المفتوحة</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce039-176">Click <strong>Accounts receivable</strong> &gt; <strong>Invoices</strong> &gt; <strong>Open customer invoices</strong>.</span></span></li>
<li><span data-ttu-id="ce039-177">اضغط على Ctrl + Shift + F3 لفتح صفحة <strong>الاستعلام</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce039-177">Press Ctrl+Shift+F3 to open the <strong>Inquiry</strong> page.</span></span></li>
<li><span data-ttu-id="ce039-178">في علامة التبويب <strong>نطاق</strong>، انقر فوق <strong>إضافة</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce039-178">On the <strong>Range</strong> tab, click <strong>Add</strong>.</span></span></li>
<li><span data-ttu-id="ce039-179">في حقل <strong>الجدول</strong>، حدد <strong>حركات العملاء المفتوحة</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce039-179">In the <strong>Table</strong> field, select <strong>Open customer transactions</strong>.</span></span></li>
<li><span data-ttu-id="ce039-180">في حقل <strong>المجال</strong>، حدد <strong>تاريخ الاستحقاق</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce039-180">In the <strong>Field</strong> field, select <strong>Due date</strong>.</span></span></li>
<li><span data-ttu-id="ce039-181">في حقل <strong>المعايير</strong>، أدخل <strong>(المعدل السنوي(-2,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce039-181">In the <strong>Criteria</strong> field, enter <strong>(yearRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="ce039-182">وانقر فوق <strong>موافق</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce039-182">Click <strong>OK</strong>.</span></span> <span data-ttu-id="ce039-183">يتم تحديث صفحة القائمة وتسرد الفواتير التي تتطابق مع المعيار الذي حددته.</span><span class="sxs-lookup"><span data-stu-id="ce039-183">The list page is updated and lists the invoices that match the criterion that you entered.</span></span> <span data-ttu-id="ce039-184">في هذا المثال، يتم سرد الفواتير المستحقة في السنتين الماضيتين.</span><span class="sxs-lookup"><span data-stu-id="ce039-184">For this example, invoices that were due in the previous two years are listed.</span></span></li>
</ol>
<span data-ttu-id="ce039-185">راجع الجدول الموجود في القسم التالي للحصول على تفاصيل إضافية عن طرق حساب تاريخ <strong>SysQueryRangeUtil</strong>، والعديد من الأمثلة.</span><span class="sxs-lookup"><span data-stu-id="ce039-185">See the table in the next section for additional details about <strong>SysQueryRangeUtil</strong> date methods, and several examples.</span></span></td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a><span data-ttu-id="ce039-186">الاستعلامات بتواريخ متقدمة التي تستخدم طرق SysQueryRangeUtil</span><span class="sxs-lookup"><span data-stu-id="ce039-186">Advanced date queries that use SysQueryRangeUtil methods</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ce039-187">الأسلوب</span><span class="sxs-lookup"><span data-stu-id="ce039-187">Method</span></span></th>
<th><span data-ttu-id="ce039-188">الوصف</span><span class="sxs-lookup"><span data-stu-id="ce039-188">Description</span></span></th>
<th><span data-ttu-id="ce039-189">مثال</span><span class="sxs-lookup"><span data-stu-id="ce039-189">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ce039-190">اليوم (_‏‏relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="ce039-190">Day (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="ce039-191">ابحث عن تاريخ بالنسبة لتاريخ الجلسة.</span><span class="sxs-lookup"><span data-stu-id="ce039-191">Find a date relative to the session date.</span></span> <span data-ttu-id="ce039-192">تشير القيم الإيجابية إلى التواريخ المستقبلية، وتشير القيم السالبة إلى تواريخ في الماضي.</span><span class="sxs-lookup"><span data-stu-id="ce039-192">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="ce039-193"><strong>الغد</strong> – أدخل<strong>(يوم (1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce039-193"><strong>Tomorrow</strong> – Enter <strong>(Day(1))</strong>.</span></span></li>
<li><span data-ttu-id="ce039-194"><strong>اليوم</strong> – أدخل <strong>(يوم (0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce039-194"><strong>Today</strong> – Enter <strong>(Day(0))</strong>.</span></span></li>
<li><span data-ttu-id="ce039-195"><strong>الأمس</strong> – أدخل <strong>(يوم (-1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce039-195"><strong>Yesterday</strong> – Enter <strong>(Day(-1))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="ce039-196">نطاق الأيام (_relativeDaysFrom=0, _relativeDaysTo=0)</span><span class="sxs-lookup"><span data-stu-id="ce039-196">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span></span></td>
<td><span data-ttu-id="ce039-197">ابحث عن نطاق تواريخ بالنسبة لتاريخ الجلسة.</span><span class="sxs-lookup"><span data-stu-id="ce039-197">Find a range of dates relative to the session date.</span></span> <span data-ttu-id="ce039-198">تشير القيم الإيجابية إلى التواريخ المستقبلية، وتشير القيم السالبة إلى تواريخ في الماضي.</span><span class="sxs-lookup"><span data-stu-id="ce039-198">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="ce039-199"><strong>آخر 30 يومًا</strong> – أدخل <strong>(نطاق الأيام (-30,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce039-199"><strong>Last 30 days</strong> – Enter <strong>(DayRange(-30,0))</strong>.</span></span></li>
<li><span data-ttu-id="ce039-200"><strong>الـ 30 يومًا السابقة والـ 30 يومًا التالية </strong> – أدخل <strong>(نطاق الأيام (-30,30))</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce039-200"><strong>Previous 30 days and next 30 days</strong> – Enter <strong>(DayRange(-30,30))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="ce039-201">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="ce039-201">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="ce039-202">البحث عن كافة التواريخ بعد التاريخ النسبي المحدد.</span><span class="sxs-lookup"><span data-stu-id="ce039-202">Find all dates after the specified relative date.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="ce039-203"><strong>أكثر من 30 يومًا من الآن</strong> – أدخل <strong>(GreaterThanDate(30))</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce039-203"><strong>More than 30 days from now</strong> – Enter <strong>(GreaterThanDate(30))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="ce039-204">GreaterThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="ce039-204">GreaterThanUtcNow ()</span></span></td>
<td><span data-ttu-id="ce039-205">البحث عن كافة إدخالات التاريخ/الوقت بعد الوقت الحالي.</span><span class="sxs-lookup"><span data-stu-id="ce039-205">Find all date/time entries after the current time.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="ce039-206"><strong>كل التواريخ/الأوقات المستقبلية</strong> – أدخل <strong>(GreaterThanUtcNow())</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce039-206"><strong>All future date/times</strong> – Enter <strong>(GreaterThanUtcNow())</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="ce039-207">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="ce039-207">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="ce039-208">البحث عن كافة التواريخ قبل التاريخ النسبي المحدد.</span><span class="sxs-lookup"><span data-stu-id="ce039-208">Find all dates before the specified relative date.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="ce039-209"><strong>أقل من سبعة أيام من الآن</strong> – أدخل <strong>(LessThanDate(7))</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce039-209"><strong>Less than seven days from now</strong> – Enter <strong>(LessThanDate(7))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="ce039-210">LessThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="ce039-210">LessThanUtcNow ()</span></span></td>
<td><span data-ttu-id="ce039-211">البحث عن كافة إدخالات التاريخ/الوقت قبل الوقت الحالي.</span><span class="sxs-lookup"><span data-stu-id="ce039-211">Find all date/time entries before the current time.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="ce039-212"><strong>كافة التواريخ/الأوقات السابقة</strong> – أدخل <strong>(LessThanUtcNow())</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce039-212"><strong>All past date/times</strong> – Enter <strong>(LessThanUtcNow())</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="ce039-213">نطاق الأشهر (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="ce039-213">MonthRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="ce039-214">البحث عن مجموعة من التواريخ، على أساس الأشهر بالنسبة للشهر الحالي.</span><span class="sxs-lookup"><span data-stu-id="ce039-214">Find a range of dates, based on months relative to the current month.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="ce039-215"><strong>الشهران السابقان</strong> – أدخل <strong>(MonthRange(-2,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce039-215"><strong>Previous two months</strong> – Enter <strong>(MonthRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="ce039-216"><strong>الأشهر الثلاثة المقبلة</strong> – أدخل <strong>(MonthRange(0,3))</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce039-216"><strong>Next three months</strong> – Enter <strong>(MonthRange(0,3))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="ce039-217">نطاق السنوات (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="ce039-217">YearRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="ce039-218">ابحث عن مجموعة من التواريخ، على أساس السنوات بالنسبة للسنة الحالية.</span><span class="sxs-lookup"><span data-stu-id="ce039-218">Find a range of dates, based on years relative to the current year.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="ce039-219"><strong>السنة القادمة</strong> – أدخل<strong>(YearRange(0, 1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce039-219"><strong>Next year</strong> – Enter <strong>(YearRange(0, 1))</strong>.</span></span></li>
<li><span data-ttu-id="ce039-220"><strong>السنة السابقة</strong> – أدخل <strong>(YearRange(-1,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce039-220"><strong>Previous year</strong> – Enter <strong>(YearRange(-1,0))</strong>.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>
