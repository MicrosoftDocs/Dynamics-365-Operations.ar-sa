---
title: نظرة عامة على إدارة الجودة
description: يصف هذا الموضوع كيفية استخدام إدارة الجودة في Dynamics 365 Supply Chain Management للمساعدة في تحسين جودة المنتج في سلسلة التوريد.
author: perlynne
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 711ce21d0e522a737e6307e7de1889c8badd5ce0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005217"
---
# <a name="quality-management-overview"></a>نظرة عامة على إدارة الجودة

[!include [banner](../includes/banner.md)]

يصف هذا الموضوع كيفية استخدام إدارة الجودة في Dynamics 365 Supply Chain Management للمساعدة في تحسين جودة المنتج في سلسلة التوريد.

ويمكن أن تساعدك إدارة الجودة في إدارة تنظيم أوقات الإنتاج عندما تتعامل مع المنتجات غير المتوافقة، بغض النظر عن نقطة الأصل. ولأن أنواع التشخيص مرتبطة بالإبلاغ عن التصحيحات، بإمكان Supply Chain Management جدولة المهام لحل المشاكل ومنع تكرارها.

وبالإضافة إلى وظيفة إدارة عدم التوافق، تتضمن إدارة الجودة وظيفة تعقب المشكلات حسب نوع المشكلة (حتى المشكلات الداخلية،) ولتحديد الحلول قصيرة الأجل أو طويلة الأجل. وتوفر إحصاءات مؤشرات الأداء الرئيسية (KPIs) رؤية في مشاكل عدم التوافق التي حدثت مسبقاً والحلول التي تم تطبيقها لتصحيحها. ويمكنك استخدام البيانات التاريخية للمساعدة على مراجعة فعالية تدابير الجودة التي تم اتخاذها سابقًا لتحديد التدابير المناسبة في المستقبل.

عند إعداد اقتران جودة، يمكن لتطبيق Supply Chain Management إنشاء أوامر الجودة لمختلف الأعمال والأحداث والشروط. ويمكن لاقتران الجودة تغطية صنف محدد أو مجموعة محددة من الأصناف أو كافة الأصناف.

## <a name="examples-of-the-use-of-quality-management"></a>أمثلة على استخدام إدارة الجودة
تتسم إدارة الجودة بالمرونة ويمكن تنفيذها بطرق مختلفة للوفاء بمتطلبات مستويات محددة من عمليات سلاسل التوريد. توضح الأمثلة التالية الاستخدامات المحتملة لهذه الميزات:

-   بدء عملية مراقبة الجودة، استناداً إلى معايير محددة مسبقاً (عند تسجيل المستودع لأمر شراء من مورد معين) تلقائياً.
-   حظر المخزون أثناء الفحص لمنع استخدام المخزون غير المعتمد (الحظر الكامل لكميات أمر الشراء).
-   استخدام عينات الصنف كجزء من اقتران الجودة لتحديد كمية المخزون الفعلي الحالي الذي يجب فحصه. يمكن أن يستند أخذ العينات إلى كميات ثابتة أو نسبة مئوية أو لوحة الترخيص الكاملة.

> [!NOTE]
> تعمل ميزة _إدارة الجودة لعمليات المستودع_ على توسيع قدرات إدارة الجودة. إذا كنت تستخدم هذه الميزة، فراجع [إدارة الجودة لعمليات المستودع](quality-management-for-warehouses-processes.md) للحصول على أمثلة حول كيفية عمل إدارة الجودة عند تمكينها.

-   إنشاء أوامر الجودة لإيصالات الاستلام الجزئية. لإنشاء أمر جودة يستند إلى الكمية التي تم استلامها فعليًا مع أمر ما، يجب عليك تحديد خانة الاختيار **حسب الكمية المحدثة** في النموذج **أخذ عينات للصنف**.
-   إنشاء أنواع الاختبار التي تتضمن الحد الأدنى، والحد الأقصى، وقيم الاختبار المستهدفة، وإجراء اختبار النوعية مقابل الكمية الذي له نتائج تحقق محددة مسبقًا.
-   تحديد مستوى جودة مقبول (AQL) للتحكم في تفاوتات قياس الجودة.
-   تحديد الموارد التي تتطلب عملية فحص، مثل منطقة اختبار وأدوات الاختبار.

## <a name="working-with-quality-associations"></a>العمل مع عمليات اقتران الجودة
يمكن ربط عملية الأعمال التي تستخدم اقتران جودة بمستندات مصدر مختلفة، مثل أوامر الشراء أو أوامر المبيعات أو أوامر الإنتاج.

كما يقوم كل سجل من سجلات عمليات اقتران الجودة بتعريف مجموعة الاختبارات ومستوى الجودة المقبول (AQL) وعينة خطة تنطبق على أوامر الجودة التي يتم إنشاؤها. ويجب تحديد سجل اقتران جودة لكل فرق في عملية تجارية. على سبيل المثال، يمكنك إعداد اقتران جودة يقوم بإنشاء أمر جودة عند تحديث إيصال استلام منتج أمر شراء. واستنادًا إلى إعداد خطة التنفيذ، يمكن حظر عملية التشغيل نفسها، بينما هناك أمر جودة مفتوح، أو يمكن خظر العمليات التالية، مثل فوترة أمر الشراء.

**ملاحظة:** أثناء وجود أوامر الجودة المفتوحة، يتم حظر إصدار كميات المخزون تلقائياً. واستناداً إلى إعداد **الحظر الكامل** في صفحة **عينات الصنف**، تكون الكمية هي أما الكمية الموجودة في أمر الجودة أو الكمية الموجودة في بند المستند المصدر.

وفي عملية أعمال محددة، يحدد سجل اقتران الجودة الحدث والظروف التي يتم إنشاء أمر جودة لها. ويمكن أن تكون الظروف خاصة بموقع أو كيان قانوني. ويمكن إنشاء أمر الجودة الذي يتضمن اختبارات تحديد القدرة فقط عند توفر مخزون للحدث.

توضح الأمثلة التالية كيفية تعريف سجل اقتران الجودة بالنسبة للتباينات في كل عملية تجارية. وتم أيضًا تلخيص الأمثلة في الرسم التخطيطي التالي من حيث الأحداث والشروط التي تم تعريفها عن طريق سجل اقتران الجودة.

<table>
<tbody>
<tr>
<th>نوع المرجع</th>
<th>نوع الحدث</th>
<th>التنفيذ</th>
<th>حظر الحدث</th>
<th>مرجع المستند</th>
</tr>
<tr>
<td>المخزون</td>
<td>غير قابل للتطبيق</td>
<td>غير قابل للتطبيق</td>
<td>بلا</td>
<td>‏‏الكل</td>
</tr>
<tr>
<td rowspan="7">المبيعات</td>
<td rowspan="4">تمت جدولة عملية الانتقاء</td>
<td rowspan="4">قبل</td>
<td>بلا</td>
<td rowspan="22">معرف محدد أو المجموعة أو الكل فقط</td>
</tr>
<tr>
<td>عملية الانتقاء</td>
</tr>
<tr>
<td>إيصال التعبئة</td>
</tr>
<tr>
<td>الفاتورة</td>
</tr>
<tr>
<td rowspan="3">إيصال التعبئة</td>
<td rowspan="3">قبل</td>
<td>بلا</td>
</tr>
<tr>
<td>إيصال التعبئة</td>
</tr>
<tr>
<td>الفاتورة</td>
</tr>
<tr>
<td rowspan="15">شراء</td>
<td rowspan="7">قائمة إيصالات الاستلام</td>
<td rowspan="4">قبل</td>
<td>بلا</td>
</tr>
<tr>
<td>قائمة إيصالات الاستلام</td>
</tr>
<tr>
<td>إيصال استلام المنتجات</td>
</tr>
<tr>
<td>الفاتورة</td>
</tr>
<tr>
<td rowspan="3">بعد</td>
<td>بلا</td>
</tr>
<tr>
<td>إيصال استلام المنتجات</td>
</tr>
<tr>
<td>الفاتورة</td>
</tr>
<tr>
<td rowspan="3">تسجيل</td>
<td rowspan="3">غير قابل للتطبيق</td>
<td>بلا</td>
</tr>
<tr>
<td>إيصال استلام المنتجات</td>
</tr>
<tr>
<td>الفاتورة</td>
</tr>
<tr>
<td rowspan="5">إيصال استلام المنتجات</td>
<td rowspan="3">قبل</td>
<td>بلا</td>
</tr>
<tr>
<td>إيصال استلام المنتجات</td>
</tr>
<tr>
<td>الفاتورة</td>
</tr>
<tr>
<td rowspan="2">بعد</td>
<td>بلا</td>
</tr>
<tr>
<td>الفاتورة</td>
</tr>
<tr>
<td rowspan="8">الإنتاج</td>
<td rowspan="3">تسجيل</td>
<td rowspan="3">غير قابل للتطبيق</td>
<td>بلا</td>
<td rowspan="12">‏‏الكل</td>
</tr>
<tr>
<td>الإبلاغ كمنتهٍ</td>
</tr>
<tr>
<td>نهاية</td>
</tr>
<tr>
<td rowspan="5">الإبلاغ كمنتهٍ</td>
<td rowspan="3">قبل</td>
<td>بلا</td>
</tr>
<tr>
<td>الإبلاغ كمنتهٍ</td>
</tr>
<tr>
<td>نهاية</td>
</tr>
<tr>
<td rowspan="2">بعد</td>
<td>بلا</td>
</tr>
<tr>
<td>نهاية</td>
</tr>
<tr>
<td rowspan="4">العزل</td>
<td rowspan="3">الإبلاغ كمنتهٍ</td>
<td rowspan="2">قبل</td>
<td>الإبلاغ كمنتهٍ</td>
</tr>
<tr>
<td>نهاية</td>
</tr>
<tr>
<td>بعد</td>
<td>نهاية</td>
</tr>
<tr>
<td>نهاية</td>
<td>قبل</td>
<td>نهاية</td>
</tr>
<tr>
<td rowspan="3">مسار العمليات</td>
<td rowspan="3">الإبلاغ كمنتهٍ</td>
<td rowspan="2">قبل</td>
<td>بلا</td>
<td rowspan="3">المعرف الخاص، والمجموعة، أو الكل، والمورد المحدد، أو المجموعة، أو الكل</td>
</tr>
<tr>
<td>الإبلاغ كمنتهٍ</td>
</tr>
<tr>
<td>بعد</td>
<td>بلا</td>
</tr>
<tr>
<td rowspan="3">إنتاج المنتج المساعد</td>
<td>تسجيل</td>
<td>غير قابل للتطبيق</td>
<td rowspan="3">بلا</td>
<td rowspan="3">‏‏الكل</td>
</tr>
<tr>
<td rowspan="2">الإبلاغ كمنتهٍ</td>
<td>قبل</td>
</tr>
<tr>
<td>بعد</td>
</tr>
</tbody>
</table>

يوفر الجدول التالي مزيدًا من المعلومات حول كيفية إنشاء أوامر الجودة لأنواع معينة من العمليات.
<div class="tableSection">

<table>
<tbody>
<tr>
<th>نوع العملية</th>
<th>عند إمكانية إنشاء أوامر الجودة تلقائياً</th>
<th>وقت إمكانية إنشاء أوامر الجودة في حالة تطلب اختبار تحديد القدرات</th>
<th>معلومات الظروف</th>
<th>معلومات الإنشاء اليدوي</th>
</tr>
<tr>
<td>أمر شراء</td>
<td>قبل أو بعد ترحيل قائمة عمليات الاستلام أو استلام المنتج للمادة التي تم استلامها</td>
<td>بعد ترحيل إيصال استلام المنتج للمواد التي تم استلامها، لأن المواد يجب أن تتوفر لإجراء اختبار تحديد القدرات</td>
<td>وقد تعكس الحاجة لأمر الجودة موقع أو صنف أو مورد بعينه أو مجموعة من هذه الشروط.</td>
<td>ويمكن لأمر الجودة الذي يتم إنشاؤه يدويًا والذي يشير لأمر شراء أن يستخدم معلومات واردة في سجل اقتران الجودة، مثل خطة أخذ عينات الاختبار.</td>
</tr>
<tr>
<td>أمر إدخال مخزن العزل</td>
<td>قبل أو بعد الإبلاغ عن أمر العزل كمنتهٍ أو مكتمل</td>
<td>لا يمكن إنشاء أوامر الجودة التي تتطلب إجراء اختبارات تحديد القدرة. ويُفترض أن تتولى وظيفة أمر العزل التخلص من المواد التي تم إتلافها.</td>
<td>وقد تعكس الحاجة لأمر الجودة موقع أو صنف أو مورد بعينه أو مجموعة من هذه الشروط.</td>
<td>ويمكن لأمر الجودة الذي يتم إنشاؤه يدويًا والذي يشير لأمر عزل أن يستخدم معلومات واردة في سجل اقتران الجودة، مثل خطة أخذ عينات الاختبار.</td>
</tr>
<tr>
<td>أمر مبيعات</td>
<td>قبل تحديث عملية الانتقاء المجدولة أو إيصال التعبئة للأصناف التي يتم شحنها</td>
<td>في أي خطوة</td>
<td>قد تعكس الحاجة إلى أمر الجودة موقعًا أو صنفًا أو عميلاً بعينه أو مجموعة من هذه الشروط.</td>
<td>ويمكن لأمر الجودة الذي يتم إنشاؤه يدويًا والذي يشير لأمر مبيعات أن يستخدم معلومات واردة في سجل اقتران الجودة، مثل خطة أخذ عينات الاختبار.</td>
</tr>
<tr>
<td>أمر الإنتاج</td>
<td>قبل أو بعد الإبلاغ عن الكمية المنتهية لأمر الإنتاج</td>
<td>بعد الإبلاغ عن الكمية المنتهية لأمر الإنتاج</td>
<td>قد تعكس الحاجة إلى أمر الجودة موقعًا أو صنفًا بعينه أو مجموعة من هذه الشروط.</td>
<td>ويمكن لأمر الجودة الذي يتم إنشاؤه يدويًا والذي يشير لأمر إنتاج أن يستخدم معلومات واردة في سجل اقتران الجودة، مثل خطة أخذ عينات الاختبار.</td>
</tr>
<tr>
<td>أمر الإنتاج الذي يشتمل على عملية مسار</td>
<td>قبل أو بعد انتهاء تقرير لعملية</td>
<td>بعد الإبلاغ عن انتهاء الإنتاج للعملية الأخيرة</td>
<td>وقد تعكس الحاجة إلى أمر الجودة موقعًا أو صنفًا أو مورد عمليات أو مجموعة من هذه الشروط.</td>
<td>ويمكن لأمر الجودة الذي يتم إنشاؤه يدويًا والذي يشير لعملية مسار أن يستخدم معلومات واردة في سجل اقتران الجودة، مثل خطة أخذ عينات الاختبار.</td>
</tr>
<tr>
<td>المخزون</td>
<td>لا يمكن إنشاء أمر الجودة تلقائيًا لإحدى الحركات الواردة في دفتر يومية المخزون أو لحركات أمر التحويل.</td>
<td></td>
<td></td>
<td>يجب إنشاء أمر جودة يدويًا لكمية مخزون الصنف. المخزون الفعلي المتوفر مطلوب.</td>
</tr>
</tbody>
</table>

## <a name="quality-order-auto-generation-examples"></a>أمثلة الإنشاء التلقائي لأمر الجودة

### <a name="purchasing"></a>الشراء

في الشراء، إذا قمت بتعيين حقل **نوع الحدث** إلى **إيصال استلام المنتجات** وحقل **التنفيذ** إلى **بعد** في صفحة **عمليات اقتران الجودة** ، فسوف تحصل على النتائج التالية: 

- إذا تم تعيين خيار **حسب الكمية المُحدثة** إلى **نعم**، يتم إنشاء أمر الجودة لكل إيصال في مقابل أمر الشراء، بناءً على الكمية المستلمة والإعدادات الموجودة في أخذ عينات الصنف. في كل مرة يتم فيها استلام كمية مقابل أمر الشراء، يتم إنشاء أوامر جودة جديدة بناءً على الكمية المستلمة حديثًا.
- إذا تم تعيين خيار **حسب الكمية المُحدثة** إلى **لا**، يتم إنشاء أمر الجودة لأول إيصال في مقابل أمر الشراء، بناءً على الكمية المستلمة. بالإضافة إلى ذلك، يتم إنشاء أمر جودة واحد أو أكثر بناءً على الكمية المتبقية، وذلك بناءً على أبعاد التعقب. لا يتم إنشاء أوامر الجودة لعمليات الاستلام اللاحقة مقابل أمر الشراء.

### <a name="production"></a>الإنتاج

في الإنتاج، إذا قمت بتعيين حقل **نوع الحدث** إلى **الإبلاغ كمنته** وحقل **التنفيذ** إلى **بعد** في صفحة **عمليات اقتران الجودة** ، فسوف تحصل على النتائج التالية:

- إذا تم تعيين خيار **حسب الكمية المُحدثة** إلى **نعم**، يتم إنشاء أمر الجودة بناءً على كل كمية منتهية والإعدادات الموجودة في أخذ عينات الصنف. في كل مرة يتم فيها الإبلاغ عن كمية كمنتهي مقابل أمر الإنتاج، يتم إنشاء أوامر جودة جديدة بناءً على الكمية المنتهية حديثًا. يتناسق منطق الإنشاء هذا مع الشراء.
- إذا تم تعيين خيار **حسب الكمية المُحدثة** إلى **لا**، يتم إنشاء أمر الجودة في أول مرة يتم الإبلاغ فيها عن منتج كمنتهي، بناءً على الكمية المنتهية. بالإضافة إلى ذلك، يتم إنشاء أمر جودة واحد أو أكثر بناءً على الكمية المتبقية، وذلك بناءً على أبعاد التعقب لأخذ عينات الصنف. لا يتم إنشاء أوامر الجودة للكميات المنتهية اللاحقة.

<table>
<tbody>
<tr>
<th>مواصفات الجودة</th>
<th>حسب الكمية المحدثة</th>
<th>حسب بُعد التعقب</th>
<th>النتيجة</th>
</tr>
<tr>
<td>النسبة: 10%</td>
<td>‏‏نعم</td>
<td>
<p>رقم الدُفعة: لا</p>
<p>الرقم التسلسلي: لا</p>
</td>
<td>
<p>كمية الطلب: 100</p>
<ol>
<li>الإبلاغ كمنته لنسبة 30
<ul>
<li>أمر الجودة رقم 1 من 3 (10% من 30%)</li>
</ul>
</li>
<li>الإبلاغ كمنته لنسبة 70
<ul>
<li>أمر الجودة رقم 2 لـ 7 (10%من كمية الأمر المتبقية، والتي تساوي 70 في هذه الحالة)</li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td>كمية ثابتة: 1</td>
<td>لا</td>
<td>
<p>رقم الدُفعة: لا</p>
<p>الرقم التسلسلي: لا</p>
</td>
<td>كمية الطلب: 100
<ol>
<li>الإبلاغ كمنته لنسبة 30
<ul>
<li>أمر الجودة رقم 1 لـ 1 (للكمية الأولى التي تم الإبلاغ عنها كمنتهِ، والتي لها قيمة ثابتة 1).</li>
<li>أمر الجودة رقم 2 لـ 1 (للكمية الأولى المتبقية، والتي لا يزال لها قيمة ثابتة 1).</li>
</ul>
</li>
<li>الإبلاغ كمنته لـ 10
<ul>
<li>لم يتم إنشاء أوامر جودة.</li>
</ul>
</li>
<li>الإبلاغ كمنته لـ 60
<ul>
<li>لم يتم إنشاء أوامر جودة.</li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td>كمية ثابتة: 1</td>
<td>‏‏نعم</td>
<td>
<p>رقم الدفعة: نعم</p>
<p>الرقم التسلسلي: نعم</p>
</td>
<td>
<p>كمية الطلب: 10</p>
<ol>
<li>الإبلاغ كمنته لـ 3: 1 للدفعة b1، مسلسل s1؛ 1 للدفعة b2، مسلسل s2؛ و1 للدفعة b3 والمسلسل s3
<ul>
<li>أمر الجودة رقم 1 لـ1 من الدفعة رقم b1، مسلسل s1</li>
<li>أمر الجودة رقم 2 لـ1 من الدفعة رقم b2، مسلسل s2</li>
<li>أمر الجودة رقم 3 لـ1 من الدفعة رقم b3، مسلسل s3</li>
</ul>
</li>
<li>الإبلاغ كمنتهِ لـ 2: 1 للدفعة b4 والمسلسل s4 و1 للدفعة b5 والمسلسل s5
<ul>
<li>أمر الجودة رقم 4 لـ1 من الدفعة رقم b4، مسلسل s4</li>
<li>أمر الجودة رقم 5 لـ1 من الدفعة رقم b5، مسلسل s5</li>
</ul>
</li>
</ol>
<p><strong>ملاحظة:</strong> يُمكن إعادة استخدام الدفعة.</p>
</td>
</tr>
<tr>
<td>كمية ثابتة: 2</td>
<td>لا</td>
<td>
<p>رقم الدفعة: نعم</p>
<p>الرقم التسلسلي: نعم</p>
</td>
<td>
<p>كمية الطلب: 10</p>
<ol>
<li>الإبلاغ كمنته لـ 4: 1 للدفعة b1، المسلسل s1؛ 1 للدفعة b2، المسلسل s2؛ 1 للدفعة b3 والمسلسل s3 و1 للدفعة b4 والمسلسل s4
<ul>
<li>أمر الجودة رقم 1 لـ1 من الدفعة رقم b1، مسلسل s1</li>
<li>أمر الجودة رقم 2 لـ1 من الدفعة رقم b2، مسلسل s2</li>
<li>أمر الجودة رقم 3 لـ1 من الدفعة رقم b3، مسلسل s3</li>
<li>أمر الجودة رقم 4 لـ1 من الدفعة رقم b4، مسلسل s4</li>
</ul>
<ul>
<li>أمر الجودة رقم 5 لـ 2، دون الإشارة إلى دفعة ورقم مسلسل</li>
</ul>
</li>
<li>الإبلاغ كمنتهِ لـ 6: 1 للدفعة b5 ومسلسل s5؛ 1 للدفعة b6 ومسلسل s6؛ 1 للدفعة b7 ومسلسل s7؛ و1 للدفعة b8 ومسلسل 8s؛ و1 للدفعة b9 ومسلسل s9؛ و1 للدفعة b10 ومسلسل s10
<ul>
<li>لم يتم إنشاء أوامر جودة.</li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

> [!NOTE]
> تضيف ميزة *إدارة الجودة لعمليات المستودع* إمكانيات معالجة أمر الجودة مع تعيين الإنتاج من **نوع الحدث** إلى *الإبلاغ كمنته* وتعيين **التنفيذ** إلى *بعد*، وتعيين عمليات الشراء من **نوع الحدث** إلى *التسجيل*. لمزيد من التفاصيل، راجع [إدارة الجودة لعمليات المستودعات](quality-management-for-warehouses-processes.md).

## <a name="quality-management-pages"></a>صفحات إدارة الجودة
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>الصفحة</th>
<th>‏‏الوصف</th>
<th>مثال</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>عمليات اقتران الجودة</td>
<td>راجع الأقسام السابقة في هذه المقالة.</td>
<td>يحدد اقتران الجودة كافة المعلومات التالية لأمر جودة يتم إنشاؤه:
<ul>
<li>حدث الحركة</li>
<li>مجموعة الاختبارات التي يجب إجراؤها على الأصناف</li>
<li>مستوى الجودة المقبول (AQL)</li>
<li>خطة أخذ العينات</li>
</ul>
يجب عليك تحديد اقتران جودة لكل فرق في العملية التجارية التي تتطلب إنشاء تلقائي لأوامر الجودة. على سبيل المثال، يمكن إنشاء أمر الجودة في عمليات الأعمال لأوامر الشراء، وأوامر العزل، وأوامر المبيعات، وأوامر الإنتاج.</td>
</tr>
<tr class="even">
<td>الاختبارات</td>
<td>استخدم هذه الصفحة لتحديد الاختبارات الفردية وعرضها والتي تحدد ما إذا كانت منتجاتك تفي بمواصفات الجودة أم لا. ويمكنك تعيين واحد أو أكثر من الاختبارات الفردية لمجموعة اختبار. وفي هذه الحالة، يمكنك أيضًا تحديد المعلومات الخاصة بالاختبار، مثل قيم القياس المقبولة. يتم استخدام قيم القياس للاختبارات الكمية، ويتم استخدام متغيرات الاختبار لاختبارات الجودة.
<ul>
<li>يشتمل الاختبار الكمي على نوع اختبار <strong>عدد صحيح</strong> أو <strong>كسر</strong>، ويشتمل أيضًا على وحدة قياس معيَّنة. يتم التعبير عن مواصفات الجودة ونتائج الاختبارات كأرقام.</li>
<li>يشتمل الاختبار النوعي على نوع اختبار <strong>الخيار</strong>. وتتطلب الاختبارات النوعية معلومات إضافية حول متغير الاختبار الذي يتم قياسه وخياراته العديدة. يتم التعبير عن مواصفات الجودة ونتائج الاختبارات حسب النتيجة.</li>
</ul></td>
<td>تقوم إحدى شركات التصنيع بإجراء اختبارين على المادة التي تم شراؤها وهما اختبار كمي حول جودة المادة واختبار نوعي حول حدوث تلف في التعبئة. وتحدد الشركة معلومات إضافية حول الاختبار النوعي لتحديد متغير الاختبار (التعبئة التالفة) ونتائجه. تستخدم الشركة صفحة <strong>مجموعات الاختبار</strong> لتعيين الاختبارين لمجموعة اختبارات وتحديد المعلومات الخاصة بالاختبار. يتم تعيين مجموعة الاختبار إلى أمر الجودة بحيث يمكن للشركة تقديم تقرير بنتائج الاختبار لكلا الاختبارين.</td>
</tr>
<tr class="odd">
<td>مجموعات الاختبار</td>
<td>استخدم هذه الصفحة لإعداد مجموعات الاختبار والاختبارات الفردية، والتي يتم تعيينها إلى مجموعة اختبار، وتحريرها وعرضها. يعرض الجزء العلوي مجموعات الاختبار، ويعرض الجزء السفلي الاختبارات التي يتم تعيينها إلى مجموعة اختبار محددة. تقوم بتعيين نُهج متعددة إلى مجموعة اختبار، بما في ذلك خطة أخذ عينات و"مستوى الجودة المقبول "(AQL) ومتطلب لاختبار تحديد القدرة. وعند تعيين اختبار فردي إلى مجموعة اختبار، يمكنك تحديد معلومات إضافية، مثل التسلسل والوثائق وتواريخ الصلاحية. وفي الاختبار الكمي، تتضمن المعلومات التي تحددها قيم القياس المقبولة أيضًا. أما في الاختبار النوعي، تتضمن المعلومات متغير الاختبار والنتيجة الافتراضية. وتحدد مجموعة الاختبار التي تم تعيينها لأمر جودة مجموعة الاختبارات الافتراضية التي يجب إجراؤها على الصنف المحدد. ومع ذلك، يمكن إضافة أو حذف أو تغيير الاختبارات في أمر الجودة. يتم الإعلام عن نتائج كل اختبار في أمر الجودة.</td>
<td>تقوم شركة تصنيع بتعريف مجموعة اختبار لكل تباين في إرشادات الجودة الخاصة بها. تعكس مجموعات الاختبار المتنوعة فروقًا في خطط أخذ العينات ومجموعات الاختبارات التي تحتاج لإجرائها معًا ومستوى الجودة المقبول (AQL) والعوامل الأخرى. وفي الاختبارات الكمية، هناك أيضًا اختلافات في قيم القياس المقبولة. ولفرض إرشادات الجودة الخاصة بها، تقوم الشركة بتعيين مجموعة اختبار لكل قاعدة لإنشاء أوامر الجودة تلقائياً في صفحة <strong>عمليات اقتران الجودة</strong>، وتقوم أيضًا بتعيين مجموعة اختبار لأوامر الجودة التي يتم إنشاؤها يدوياً.</td>
</tr>
<tr class="even">
<td>مجموعات جودة الصنف</td>
<td>استخدم هذه الصفحة لإعداد وتحرير وعرض الأصناف المخصصة لمجموعة الجودة أو مجموعات الجودة المخصصة للصنف. تمثل مجموعة الجودة متطلبات الاختبار الشائعة للأصناف. وبعد تحديد متطلبات الاختبار في صفحة <strong>مجموعات الاختبار</strong>، يمكنك تحديد القواعد لإنشاء أوامر الجودة تلقائياً. ولتبسيط العملية، لا يلزمك تحديد قواعد للأصناف الفردية. وبدلاً من ذلك، يمكنك تحديد قواعد لمجموعة جودة، من خلال استخدام صفحة <strong>عمليات اقتران الجودة</strong>. ويمكنك أيضًا استخدام صفحة <strong>مجموعات جودة الصنف</strong> لمجموعة جودة محددة لتعيين الأصناف ذات الصلة لهذه المجموعة. ويمكنك أيضًا استخدام صفحة <strong>مجموعات جودة الصنف</strong> لصنف محدد لتعيين مجموعات الجودة ذات الصلة لهذا الصنف.</td>
<td>تقوم الشركة المصنعة بشراء العديد من المواد الخام المتعددة التي لها نفس متطلبات الاختبار الخاصة بالفحص الوارد. وتحدد الشركة مجموعة الجودة، ثم تقوم بتعيين أرقام الأصناف المرتبطة بالمواد الخام إلى تلك المجموعة. ولاحقاً، تشتري الشركة نوعًا جديدًا من المواد الخام له نفس متطلبات الاختبارات. وبدلاً من إعداد متطلبات الاختبار الجديدة للمواد الجديدة، تضيف الشركة رقم الصنف للمواد الجديدة إلى مجموعة الجودة الموجودة. كما تنتج نفس شركة التصنيع الأصناف التي تشتمل على نفس متطلبات اختبارات الإنتاج وتقوم بشحن الأصناف التي تشتمل على نفس متطلبات اختبارات ما قبل الشحن. وتحدد الشركة مجموعتي جودة إضافيتين، ثم تقوم بتعيين أرقام الأصناف ذات الصلة لكل مجموعة.</td>
</tr>
<tr class="odd">
<td>متغيرات الاختبار</td>
<td>استخدم هذه الصفحة لتحديد وعرض المتغيرات المرتبطة باختبار جودة. وبالنسبة لكل متغير، تقوم بتحديد النتائج العديدة التي تمثل الخيارات الممكنة. ويمكنك تحديد الاختبارات في صفحة <strong>الاختبارات</strong>. وبالنسبة لاختبارات الجودة، يجب عليك تعيين نوع الاختبار إلى <strong>الخيار</strong>. واستخدم صفحة <strong>مجموعات الاختبارات</strong> لتعيين متغير اختبار لكل اختبار فردي.</td>
<td>شركة تصنيع تنتج حلوى، تقوم بإجراء اختبار فحص للمنتج المنتهي. ويشتمل اختبار الفحص هذا على متغيرات متعددة. ومن بين هذه المتغيرات الطعم، وتكون النتائج المحتملة لهذا المتغير جيدة وسيئة. أما المتغير الثاني فهو اللون، وتكون النتائج المحتملة له داكن جدًا أو فاتح جدًا أو صحيح.</td>
</tr>
<tr class="even">
<td>نتائج متغير الاختبار.</td>
<td>استخدم هذه الصفحة لإعداد نتائج الاختبار الممكنة وتحريرها وعرضها لأحد متغيرات الاختبار المرتبطة باختبار الجودة. وللحصول على كل نتيجة، تقوم بتعيين حالة <strong>نجاح</strong> أو <strong>فشل</strong>. يجب تعريف المتغير ونتائجه الخاصة بكل اختبار جودة الذي يتم تحديده في صفحة <strong>الاختبارات</strong>. (بالنسبة لاختبارات الجودة، يتم تعيين نوع الاختبار إلى <strong>الخيار</strong> في صفحة <strong>الاختبارات‬‏‫</strong>.) ‏‫استخدم صفحة <strong>مجموعات الاختبارات</strong> لتعيين متغير اختبار والنتيجة الافتراضية لاختبار جودة فردي.‬</td>
<td>شركة تصنيع تنتج حلوى، تقوم بإجراء اختبار فحص للمنتج المنتهي. ويشتمل اختبار الفحص هذا على متغيرات متعددة. ومن بين هذه المتغيرات الطعم، وتكون النتائج المحتملة لهذا المتغير جيدة وسيئة. أما المتغير الثاني فهو اللون، وتكون النتائج المحتملة له داكن جدًا أو فاتح جدًا أو صحيح. ويتم تعيين حالة <strong>نجاح</strong> أو <strong>فشل</strong> لكل نتيجة. أثناء اختبار الفحص الخاص بكل متغير، يقوم المفتش بالإعلام عن نتيجة الاختبار عن طريق تحديد إحدى النتائج.</td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a>الموارد الإضافية
--------

[عمليات إدارة الجودة](quality-management-processes.md)

[إدارة عدم المطابقة](enable-nonconformance-management.md)

[إدارة الجودة لعمليات المستودعات](quality-management-for-warehouses-processes.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]