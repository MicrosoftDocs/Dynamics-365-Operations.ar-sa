---
title: قيود التعبير وقيود الجدول في نماذج تكوين المنتج
description: يصف هذا المقال استخدام قيود التعبير وقيود الجدول. تتحكم القيود في قيم السمات التي يمكن تحديدها عند تكوين المنتجات لأمر المبيعات أو عرض أسعار المبيعات أو أمر الشراء أو أمر الإنتاج. يمكنك استخدام قيود التعبير أو قيود الجدول، اعتمادًا على الطريقة التي تفضل بها إنشاء القيود.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PCGlobalTableConstraintEdit, PCProductConfigurationModelDetails, PCTableConstraintAttachAttributeTree, PCTableConstraintDefinition
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e504f6996b401e72792d910c8df74bb9611c4d60
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895543"
---
# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a>قيود التعبير وقيود الجدول في نماذج تكوين المنتج

[!include [banner](../includes/banner.md)]

يصف هذا المقال استخدام قيود التعبير وقيود الجدول. تتحكم القيود في قيم السمات التي يمكن تحديدها عند تكوين المنتجات لأمر المبيعات أو عرض أسعار المبيعات أو أمر الشراء أو أمر الإنتاج. يمكنك استخدام قيود التعبير أو قيود الجدول، اعتمادًا على الطريقة التي تفضل بها إنشاء القيود. 

يتم استخدام القيود للتحكم في قيم السمات التي يمكن تحديدها عند تكوين المنتجات لأمر المبيعات أو عرض أسعار المبيعات أو أمر الشراء أو أمر الإنتاج. يمكنك استخدام قيود التعبير أو قيود الجدول، اعتمادًا على الطريقة التي تفضل بها إنشاء القيود.

## <a name="what-are-expression-constraints"></a>ما هي قيود التعبير؟
تتسم قيود التعبير بتعبير يستخدم الدالات والمعامِلات الحسابية المنطقية. تتم كتابة قيد تعبير لمكون محدد في نموذج تكوين منتج. لا يمكن إعادة استخدامها بواسطة أو بالمشاركة مع مكون آخر. ومع ذلك، يمكن لقيود التعبير لمكون الإشارة إلى سمات المكونات الفرعية للمكون.

## <a name="what-are-table-constraints"></a>ما هي قيود الجدول؟
تسرد قيود الجدول مجموعات القيم المسموح بها للسمات عندما تقوم بتكوين منتج. يمكن استخدام تعريفات قيود الجدول بشكل عام. عند إنشاء قيد جدول لمكون في نموذج تكوين منتج، حدد تعريف قيد جدول. لإنشاء المجموعات المسموح بها، تقوم بإضافة سمات الأنواع المحددة للمكونات. يحتوي كل نوع سمة على قيمة محددة.

### <a name="example-of-a-table-constraint"></a>مثال على قيد جدول

يوضح هذا المثال كيفية تحديد تكوين مكبر صوت لألوان الكابينة محددة والأجزاء الأمامية. يعرض الجدول الأول ألوان الكابينة والأجزاء الأمامية المتوفرة بشكل عام للتكوين. ويتم تحديد القيم لنوعي السمات **لون الكابينة** و **الشبكة الأمامية**.

| نوع السمة | القيم                      |
|----------------|-----------------------------|
| لون الكابينة | أسود، وبلوطي، وروزوود، وأبيض |
| الشبكة الأمامية    | أسود، ومعدني، وأبيض         |

يُظهر الجدول التالي هذا المجموعات المحددة من قِبل قيد الجدول **اللون واللمسة النهائية**. باستخدام هذا القيد في الجدول، يمكنك تكوين مكبر صوت بلون بلوطي وشبكة سوداء، ولون روزوود وشبكة بيضاء، وهكذا.

| إنهاء         | الشبكة                       |
|----------------|-----------------------------|
| بلوطي            | أسود                       |
| روزوود       | أبيض                       |
| أبيض          | أسود                       |
| أبيض          | أبيض                       |
| أسود          | أسود                       |
| أسود          | معدني                       | 

يمكنك إنشاء قيود جدول إما محددة بواسطة المستخدم أو محددة بواسطة النظام. لمزيد من المعلومات، راجع [قيود الجدول المحددة من قِبل النظام والمحددة من قِبل المستخدم](system-defined-user-defined-table-constraints.md).

## <a name="what-syntax-should-be-used-to-write-constraints"></a>‏‫ما بنية الجملة التي يجب استخدامها لكتابة القيود؟
يجب عليك استخدام بنية جملة لغة تصميم التحسين (OML) عند كتابة القيود. يستخدم النظام أداة حل القيود Microsoft Solver Foundation لحل القيود.

## <a name="should-i-use-table-constraints-or-expression-constraints"></a>هل يجب استخدام قيود الجدول أو قيود التعبير؟
يمكنك استخدام قيود التعبير أو قيود الجدول، اعتمادًا على الطريقة التي تفضل بها إنشاء القيود. يمكنك إنشاء قيد جدول كمصفوفة، بينما يكون قيد التعبير عبارة فردية. عندما تقوم بتكوين منتج، فلا يهم نوع القيد المستخدَم. يعرض المثال التالي مدى اختلاف الطريقتين.  

عند قيامك بتكوين منتج باستخدام إعدادات القيود التالية، يتم السماح بهذه المجموعات:

-   منتج باللون الأسود، وبحجم 30 أو 50
-   منتج باللون الأحمر، وبحجم 20

### <a name="table-constraint-setup"></a>إعداد قيد الجدول

| اللون | الحجم |
|-------|------|
| أسود | 30   |
| أسود | 50   |
| أحمر   | 20   |

### <a name="expression-constraint-setup"></a>إعداد قيد التعبير

(لون == "أسود" و (حجم == "30" | حجم == "50")) | (لون == "أحمر" وحجم = "20")

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a>هل يجب استخدام المعامِلات أو تدوين الحرف المزيد عند كتابة قيود التعبير؟
يمكنك كتابة قيد تعبير إما باستخدام تدوين الحروف المزيدة أو معامِلات البادئات المتوفرة. لا يمكنك استخدام تدوين الحروف المزيدة لمعامِلات ‏‫القيمة **المطلقة**، و **الحد الأدنى**، و **الحد الأقصى**. ويتم تضمين هذه المعامِلات كمعامِلات قياسية في معظم لغات البرمجة.

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a>ما هي المعامِلات وتدوينات الحروف المزيدة التي يمكن استخدامها عند كتابة قيود التعبير؟
تسرد الجداول التالية المعامِلات وتدوينات الحروف المزيدة التي يمكنك استخدامها عند كتابة قيد تعبير لمكون في نموذج تكوين منتج. في الأمثلة الواردة في هذا الجدول الأول، يمكنك الاطلاع على كيفية كتابة تعبير باستخدام المعامِلات أو تدوينات الحروف المزيدة.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>المعامل</th>
<th>‏‏الوصف‬</th>
<th>بناء الجملة</th>
<th>أمثلة</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>يعني</td>
<td>إذا كان الشرط a صحيحًا، فطبّق القيد b.</td>
<td>يعني [a أو b]، الحرف المزيد: a -: b</td>
<td><ul>
<li><strong>عامل التشغيل:</strong> يتضمن[x‏ != 0، y &gt;=‏ 0]</li>
<li><strong>تدوين الحرف المزيد:</strong> x‏ != 0 -‏: y &gt;=‏ 0</li>
</ul></td>
</tr>
<tr class="even">
<td>و</td>
<td>يكون هذا الأمر صحيحًا فقط إذا تحققت جميع الشروط. إذا كان عدد الشروط هو 0 (صفر)، ينتج قيمة <strong>صحيحة</strong>.</td>
<td>And‏[args]، الحرف المزيد: a &amp; b &amp; ... &amp; z</td>
<td><ul>
<li><strong>عامل التشغيل:</strong> And‏[x‏ == 2، y &lt;=‏ 2]</li>
<li><strong>تدوين الحرف المزيد:</strong> x‏ == 2 &amp; y &lt;=‏ 2</li>
</ul></td>
</tr>
<tr class="odd">
<td>أو</td>
<td>يكون هذا الأمر صحيحًا إذا كان أي شرط صحيح. إذا كان عدد الشروط هو 0 (صفر)، تنتج قيمة <strong>خاطئة</strong>.</td>
<td>Or‏[args]، الحرف المزيد: a‏ | b |‏ ... | z</td>
<td><ul>
<li><strong>عامل التشغيل:</strong> Or‏[x‏ == 2، y &lt;=‏ 2]</li>
<li><strong>تدوين الحرف المزيد:</strong> x =‏=‏ 2 | y &lt;=‏ 2</li>
</ul></td>
</tr>
<tr class="even">
<td>زائد</td>
<td>وهذا يلخص الشروط. إذا كان عدد الشروط هو 0 (صفر)، تنتج قيمة <strong>0</strong>.</td>
<td>Plus‏[args]، الحرف المزيد: a‏ + b‏ + ... + z</td>
<td><ul>
<li><strong>عامل التشغيل:</strong> زائد[x،‏ y،‏ 2] =‏=‏ z</li>
<li><strong>تدوين الحرف المزيد:</strong> x + y + 2 =‏=‏ z</li>
</ul></td>
</tr>
<tr class="odd">
<td>ناقص</td>
<td>هذا يناقض الوسيطة. يجب أن يكون به شرط واحد فقط.</td>
<td>Minus‏[expr]، الحرف المزيد: -expr</td>
<td><ul>
<li><strong>عامل التشغيل:</strong> ناقص[x] =‏=‏ y</li>
<li><strong>تدوين الحرف المزيد:</strong> -x =‏=‏ y</li>
</ul></td>
</tr>
<tr class="even">
<td>القيمة المطلقة</td>
<td>وهذا يأخذ القيمة المطلقة من شرطها. يجب أن يكون به شرط واحد فقط.</td>
<td>Abs‏[expr]</td>
<td><strong>عامل التشغيل:</strong> Abs‏[x]</td>
</tr>
<tr class="odd">
<td>الأوقات</td>
<td>يأخذ هذا المنتج من شروطه. إذا كان عدد الشروط هو 0 (صفر)، تنتج قيمة <strong>1</strong>.</td>
<td>Times[args], الحرف الزائد: a * b * ... * z</td>
<td><ul>
<li><strong>عامل التشغيل:</strong> أوقات[x،‏ y،‏ 2] =‏=‏ z</li>
<li><strong>تدوين الحرف المزيد:</strong> x * y * 2 == z</li>
</ul></td>
</tr>
<tr class="even">
<td>القدرة</td>
<td>يأخذ هذا قيمة أُسية. تنطبق هذه القيمة الأُسية من اليمين لليسار. (وبمعنى آخر، إنها مجمَّعة إلى اليمين). وبالتالي، فإن <strong>Power[a, b, c]</strong> يعادل <strong>Power[a, Power[b, c]]</strong>. <strong>Power</strong> يمكن استخدامه فقط إذا كان الأس بقيمة موجبة.</td>
<td>Power‏[args]، الحرف المزيد: a ^ b ^ ... ^ z</td>
<td><ul>
<li><strong>عامل التشغيل:</strong> Power[x،‏ 2] =‏=‏ y</li>
<li><strong>تدوين الحرف المزيد:</strong> x ^ 2 =‏=‏ y</li>
</ul></td>
</tr>
<tr class="odd">
<td>الحد الأقصى</td>
<td>ينتج عن هذا الأمر الشرط الأكبر. إذا كان عدد الشروط هو 0 (صفر)، تنتج قيمة <strong>لانهائية</strong>.</td>
<td>Max‏[args]</td>
<td><strong>عامل التشغيل:</strong> الحد الأقصى[x،‏ y،‏ 2] =‏=‏ z</td>
</tr>
<tr class="even">
<td>الحد الأدنى</td>
<td>ينتج عن هذا الأمر الشرط الأصغر. إذا كان عدد الشروط هو 0 (صفر)، تنتج قيمة <strong>لانهائية</strong>.</td>
<td>Min‏[args]</td>
<td><strong>عامل التشغيل:</strong> الحد الأدنى[x،‏‏ y،‏‏ 2] =‏=‏ z</td>
</tr>
<tr class="odd">
<td>ليس</td>
<td>ينتج عن هذا الأمر العكس المنطقي للشرط. يجب أن يكون به شرط واحد فقط.</td>
<td>Not‏[expr]، الحرف المزيد: !expr</td>
<td><ul>
<li><strong>عامل التشغيل:</strong> Not‏[x] &amp; Not‏[y =‏=‏ 3]</li>
<li><strong>تدوين الحرف المزيد:</strong> !‏x!‏(y =‏= 3)</li>
</ul></td>
</tr>
</tbody>
</table>

توضح الأمثلة في الجدول التالي كيفية كتابة تدوين الحرف المزيد.


|  تدوين الحرف المزيد   |                                          ‏‏الوصف                                          |
|-------------------|-----------------------------------------------------------------------------------------------|
|     x + y + z     |                                           الجمع                                            |
|    x \* y \* z    |                                        الضرب                                         |
|       x - y       | يتم تحويل الطرح الثنائي مثل الإضافة الثنائية بقيمة ثانية سالبة. |
|     x ^ y ^ z     |                          العلامة الأسية بالتجميع الصحيح                          |
|        !x         |                                          قيمة غير منطقية                                          |
|      x -: y       |                                      تضمين منطقي                                      |
|         x         |                                               y                                               |
|     x & y & z     |                                          قيمة and منطقية                                          |
|    x =‏=‏ y =‏=‏ z    |                                           التساوي                                            |
|    x !=‏ y !=‏ z    |                                           محدد                                            |
|  x &lt; y &lt; z  |                                           أقل من                                             |
|  x &gt; y &gt; z  |                                         أكبر من                                          |
| x &lt;=‏‏ y &lt;=‏‏ z |                                     أقل من أو يساوي                                     |
| x &gt;=‏ y &gt;=‏ z |                                   أكبر من أو يساوي                                    |
|        (x)        |                           تتجاوز الأقواس الأسبقية الافتراضية.                            |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a>لماذا لم يتم التحقق من صحة قيود التعبير لدي بشكل صحيح؟
لا يمكنك استخدام الكلمات الرئيسية المحجوزة كأسماء أدوات الحلول للسمات أو المكونات أو المكونات الفرعية في نموذج تكوين منتج. فيما يلي قائمة بالكلمات الأساسية المحجوزة التي لا يمكن استخدامها:

-   الحد الأقصى
-   العنصر
-   متساوٍ
-   الأرضية
-   إذا
-   أقل
-   أكبر
-   يعني
-   السجل
-   الحد الأقصى
-   دقيقة
-   ناقص
-   زائد
-   القدرة
-   الأوقات
-   الجزء
-   الطراز
-   القرار
-   الهدف


## <a name="additional-resources"></a>الموارد الإضافية

[قم بإنشاء قيد تعبير](tasks/add-expression-constraint-product-configuration-model.md)

[إضافة عملية حسابية إلى نموذج تكوين منتج](tasks/add-calculation-product-configuration-model.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
