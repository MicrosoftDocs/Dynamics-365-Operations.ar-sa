---
title: وظيفة مصمم BOM
description: يوضح هذا المقال كيفية استخدام صفحة مصمم قائمة مكونات الصنف لتصميم هياكل شجرة قائمة مكونات الصنف واستخدامها.
author: johanhoffmann
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMDesigner, BOMDesignerSetup, BOMDesignerFilterDialog, BOMDesignerBOMVersion, BOMChangeLine
audience: Application User
ms.reviewer: kamaybac
ms.custom: 20981
ms.assetid: 2b92eec1-d28c-4965-9086-939c77b3c62b
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2fda2b1d835afdcf06a50528748861fecc6792f8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844191"
---
# <a name="bom-designer-functionality"></a>وظيفة مصمم BOM

[!include [banner](../includes/banner.md)]

يوضح هذا المقال كيفية استخدام صفحة مصمم قائمة مكونات الصنف لتصميم هياكل شجرة قائمة مكونات الصنف واستخدامها. يمكنك النقر فوق "إعداد" لتحديد تكوينات مختلفة وتعيين المعلومات التي تظهر في عرضها في بنود الشجرة.

عندما تقوم بفتح صفحة **مصمم قائمة مكونات الصنف** من صفحة **المنتجات التي تم إصدارها**، فإنها تعرض التسلسل الهرمي لقوائم مكونات الصنف التي تكون نشطة ويتم اعتمادها للصنف المحدد، وموقع الأمر الافتراضي للصنف، والتاريخ الفعلي.  

وانقر فوق **عامل تصفية** لتغيير التحديد الأولى في طريقة العرض. وعن طريق تعيين قاعدة العرض إلى **المحددة/النشطة أو المحددة**، يمكنك تحديد إصدارات قائمة مكونات الصنف أو المسار الفردية المُراد استخدامها في طريقة العرض. ويمكنك تحديد إصدارات قائمة مكونات الصنف غير المعتمدة وغير النشطة لإظهارها أو الاحتفاظ بها في مصمم قائمة مكونات الصنف.  

**ملاحظة:** إذا قمت بفتح مصمم قائمة مكونات الصنف من صفحة قائمة **قائمة مكونات الصنف**، فإنه لا يعرض معلومات المسار. وحاليًا، يُعد تحديد إصدار قائمة مكونات الصنف أو المسار خاصية لإصدار قائمة مكونات الصنف والمسار، وينطبق على كافة مثيلات مصمم قائمة مكونات الصنف.  

تصف الأقسام التالية الوظائف المتوفرة في علامات التبويب المختلفة لمصمم قائمة مكونات الصنف.

## <a name="analyzing-a-bom-structure-by-using-the-bom-designer"></a>تحليل بنية قائمة مكونات الصنف باستخدام مصمم قائمة مكونات الصنف.
يشتمل مصمم قائمة مكونات الصنف على قسمين:

-   طريقة عرض الشجرة لبنية قائمة مكونات الصنف.
-   قسم التفاصيل، الذي يعرض تفاصيل البيانات المحددة. عند قيامك بتحديد عقده في طريقة عرض الشجرة، يتم تحديث علامات التبويب السريع في قسم التفاصيل بناءً على هذه العقدة:
    -   **تفاصيل بند قائمة مكونات الصنف** – عرض تفاصيل بند قائمة مكونات الصنف المحدد في طريقة عرض الشجرة.
    -   **بيانات الصنف** – عرض تفاصيل الصنف الرئيسي أو الصنف الذي يُستخدم في العقدة المحددة. يمكنك النقر فوق **تحرير المنتج الصادر** للاحتفاظ بالصنف المحدد.
    -   **قائمة مكونات الصنف** – عرض رأس قائمة مكونات الصنف المرتبطة بالعقدة المحددة.
    -   **المسار** – عرض رأس المسار المرتبط بالعقدة المحددة.
    -   **عمليات المسار** – عرض معاينة لعمليات المسار. عند تحديد بند قائمة مكونات الصنف الذي تم تعيينه لعملية بعينها، يتم وضع علامة على هذه العملية باعتبارها **المكون المطلوب في العمليات**.

## <a name="selecting-a-bom-and-route"></a>تحديد قائمة مكونات الصنف والمسار
يتم عرض عامل التصفية الذي يتم استخدامه لقائمة مكونات الصنف والمسار في رأس مصمم قائمة مكونات الصنف. ويمكنك تغيير عامل التصفية باستخدام مربع الحوار **عامل تصفية**. يصف الجدول التالي الحقول الموجودة في مربع الحوار هذا.

<table>
<thead>
<tr class="header">
<th>الحقل</th>
<th>الوصف</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>أبعاد المنتجات</td>
<td>إذا كان المنتج النهائي المحدد عبارة عن أصل منتج، فيمكنك تحديد أبعاد منتج نشطة للاختيار الرئيسي. <strong>ملاحظة:</strong> إذا فتحت مصمم قائمة مكونات الصنف‬ لمنتج ليس عبارة عن أصل منتج، فلا يمكن تحديد أبعاد المنتج في مربع الحوار <strong>تصفية‏‎</strong>.</td>
</tr>
<tr class="even">
<td>الموقع</td>
<td>قم بتغيير الموقع الذي يتم عرض شجرة قائمة مكونات الصنف له. الموقع الافتراضي هو موقع المخزون الافتراضي للصنف المنتهي.</td>
</tr>
<tr class="odd">
<td>قاعدة العرض</td>
<td>حدد قاعدة عرض الإصدار التي تنطبق على بنية قائمة مكونات الصنف الحالية والمسار الحالي:
<ul>
<li>عند تعيين القاعدة إلى <strong>نشطة أو محددة/نشطة</strong>، فسيتم العثور على إصدار قائمة مكونات الصنف أو المسار الصالح لهذا التاريخ.</li>
<li>وعند تعيين القاعدة إلى <strong>المحددة/النشطة أو المحددة</strong>، يمكنك تحديد إصدار قائمة مكونات الصنف أو إصدار المسار بالنقر فوق <strong>قائمة مكونات الصنف</strong> &gt; <strong>إصدارات قائمة مكونات الصنف</strong> أو <strong>المسار</strong> &gt; <strong>إصدارات المسار</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>تاريخ الإصدار</td>
<td>يتيح إدخال تاريخ الإصدار  الخاص بشجرة المواد والمسار. يحدد الإصدار إصدار قائمة مكونات الصنف الذي يتم استخدامه في تاريخ محدد، كما هو معين بواسطة تواريخ الإصدار الموجودة في إعداد إصدار قائمة مكونات الصنف.</td>
</tr>
<tr class="odd">
<td>من الكمية</td>
<td>قم بتصفية الإصدارات عن طريق تحديد قيمة معينة من الكمية. إذا قمت بتعيين قيمة، يمكن تحديد إصدارات مختلفة لقائمة مكونات الصنف والمسار.</td>
</tr>
<tr class="even">
<td>إظهار الصالح فقط</td>
<td>عند قيامك تحديد خانة الاختيار، تعرض بنية الشجرة بنود قائمة مكونات الصنف التي لها تواريخ صالحة فقط. انقر بزر الماوس الأيمن أو انقر نقرًا مزدوجًا فوق بند قائمة مكونات الصنف لفتح صفحة <strong>تحرير بند قائمة مكونات الصنف</strong>، حيث يمكنك مشاهدة تواريخ الصلاحية الخاصة ببند قائمة مكونات الصنف هذا.</td>
</tr>
</tbody>
</table>

عند استخدام مصمم قائمة مكونات الصنف لمراجعة قائمة مكونات الصنف التي تتألف من واحد أو أكثر من مستويات الأصناف الوهمية، يمتد المسار المرتبط بالصنف الأعلى عادةً ليشمل التسلسل الهرمي لقائمة مكونات الصنف بالكامل. ولتبسيط النظرة العامة، يمكنك تأمين المسار ذي المستوى الأعلى في العرض عن طريق النقر فوق **طريقة عرض** &gt; **تأمين المسار**. ولإلغاء تأمين المسار، انقر فوق **طريقة عرض** &gt; **إلغاء تأمين المسار**.

## <a name="adding-and-editing-boms-and-bom-lines"></a>إضافة وتحرير قوائم مكونات الصنف وبنودها
استخدام وظائف **بنود قائمة مكونات الصنف** أو **قائمة مكونات الصنف** لتعديل بنود قائمة مكونات الصنف أو قائمة مكونات الصنف. وعندما تحدد عقده في الشجرة، يحدد نوع العقدة الوظائف المتوفرة.

| الوظيفة                            | ‏‏الوصف                                                                                               | نوع العقدة والشروط                                                                                                                                                                                                                                                                       |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| بنود قائمة مكونات الصنف &gt; تحرير                 | فتح مربع حوار حيث يمكنك تحرير سمات بنود قائمة مكونات الصنف.                                             | تتوفر هذه الوظيفة عند تحديد عقده بند قائمة مكونات الصنف.                                                                                                                                                                                                                                   |
| بنود قائمة مكونات الصنف &gt; حذف               | حذف بند قائمة مكونات الصنف من قائمة مكونات الصنف المحددة.                                                                  | تتوفر هذه الوظيفة عند تحديد عقده بند قائمة مكونات الصنف، وعدم تأمين قائمة مكونات الصنف ضد التحرير.                                                                                                                                                                                             |
| بنود قائمة مكونات الصنف &gt; إضافة قبل البند      | افتح مربع حوار حيث يمكنك تحديد منتج متغير لتضمينه قبل بند قائمة مكونات الصنف المحدد.         | تتوفر هذه الوظيفة عند تحديد عقده بند قائمة مكونات الصنف.                                                                                                                                                                                                                                   |
| بنود قائمة مكونات الصنف &gt; إضافة إلى قائمة مكونات الصنف لمكون | افتح مربع حوار حيث يمكنك تحديد منتج متغير لتضمينه في نهاية قبل بند قائمة مكونات الصنف المحدد.       | تتوفر هذه الوظيفة عندما تشتمل العقده المحددة على قائمة مكونات صنف محددة. أما إذا لم تتوفر هذه الوظيفة، قد يكون إصدار قائمة مكونات الصنف مفقودًا لمتغير الصنف المحدد. وفي هذه الحالة، يمكنك النقر فوق **قائمة مكونات الصنف** &gt; **إنشاء إصدار** لإنشاء الإصدار المفقود للعقدة المحددة. |
| بنود قائمة مكونات الصنف &gt; إضافة بعد البند       | افتح مربع حوار حيث يمكنك تحديد منتج متغير لتضمينه بعد بند قائمة مكونات الصنف المحدد.          | تتوفر هذه الوظيفة عند تحديد عقده بند قائمة مكونات الصنف.                                                                                                                                                                                                                                   |
| قائمة مكونات الصنف &gt; إنشاء إصدار             | قم بإنشاء إصدار قائمة مكونات صنف أو قائمة مكونات صنف جديدة لمتغير المنتج الخاص يالعقدة المحددة.                             | تتوفر هذه الوظيفة عند ربط عقدة بند قائمة مكونات الصنف الذي تم تحديده لأي صنف يحتوي على نوع الإنتاج **قائمة مكونات الصنف** أو **المعادلة**.                                                                                                                                                  |
| قائمة مكونات الصنف &gt; الحساب                | افتح مربع حوار حيث يمكنك حساب التكلفة أو سعر المبيعات لمتغير المنتج المحدد. | تتوفر هذه الوظيفة عندما ترتبط العقدة المحددة بإصدار قائمة مكونات صنف.                                                                                                                                                                                                         |
| قائمة مكونات الصنف &gt; التحقق                      | تحقق من صحة وافحص قائمة مكونات الصنف المحددة.                                                                      | تتوفر هذه الوظيفة عندما ترتبط العقدة المحددة بإصدار قائمة مكونات صنف.                                                                                                                                                                                                         |

## <a name="configuring-the-tree-view"></a>تكوين طريقة عرض الشجرة
انقر فوق **الإعداد** لتخصيص المعلومات التي يتم عرضها في طريقة عرض الشجرة لمصمم قائمة مكونات الصنف.

| مجموعة الحقول | الوصف                                                                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| قائمة مكونات الصنف         | استخدم خانات الاختيار لتحديد المعايير التي يتم عرضها في بنية الشجرة. ويقوم مصمم قائمة مكونات الصنف بعرض المعايير التي تم تحديدها في أسفل كلٍّ من علامتي التبويب. |
| المسار       | استخدم خانات الاختيار لتحديد المعايير التي يتم عرضها للمسارات.                                                                                    |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]