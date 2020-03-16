---
title: الموافقة على فاتورة المحمول
description: يهدف هذا الموضوع إلى توفير نهج عملي لتصميم سيناريوهات المحمول عبر أخذ عمليات الموافقة على فواتير المورّد للمحمول كحالة استخدام.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 88ba96b1d9d2f722528a4a920eabe4ab64304a7a
ms.sourcegitcommit: 4f668b23f5bfc6d6502858850d2ed59d7a79cfbb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/14/2020
ms.locfileid: "3059418"
---
# <a name="mobile-invoice-approvals"></a>الموافقة على فاتورة المحمول

[!include [banner](../includes/banner.md)]

تسمح قدرات المحمول لمستخدمي الشركات بتصميم تجارب المحمول. للسيناريوهات المتقدمة، يسمح النظام الأساسي أيضًا للمطورين بتوسيع القدرات بحسب رغباتهم. وتُعد أفضل وسيلة للتعرف على بعض المفاهيم الجديدة على المحمول الانتقال عبر عملية تصميم بعض السيناريوهات. يهدف هذا الموضوع إلى توفير نهج عملي لتصميم سيناريوهات المحمول عبر أخذ عمليات الموافقة على فواتير المورّد للمحمول كحالة استخدام. من المفترض أن يساعدك هذا الموضوع على تصميم أشكال مختلفة أخرى للسيناريوهات ويمكن أيضًا تطبيقه على سيناريوهات أخرى لا علاقة لها بفواتير المورّد.

<a name="prerequisites"></a>المتطلبات الأساسية
-------------

| المتطلب الأساسي                                                                                            | ‏‏الوصف                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| قبل قراءة دليل المحمول                                                                                |[النظام الأساسي للأجهزة المحمولة](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)                                                                                                  |
| Dynamics 365 Finance                                                                              | بيئة يتوفر فيها الإصدار 1611 والتحديث الثالث للنظام الأساسي (نوفمبر 2016)                   |
| تثبيت الإصلاح العاجل KB 3204341.                                                                              | باستطاعة مسجل المهام تسجيل أمري "إغلاق" بطريق الخطأ لمربعات الحوار ذات القوائم المنسدلة المضمنة في التحديث الثالث للنظام الأساسي (تحديث نوفمبر 2016). |
| تثبيت الإصلاح العاجل KB 3207800.                                                                              | يتيح هذا الإصلاح العاجل عرض المرفقات على عميل المحمول المضمن في التحديث الثالث للنظام الأساسي (تحديث نوفمبر 2016).           |
| تثبيت الإصلاح العاجل KB 3208224.                                                                              | التعليمات البرمجية للتطبيق لطلب الموافقة على فواتير المورّد على المحمول مضمنة في الإصدار 7.0.1 (مايو 2016).                          |
| جهاز يعمل بنظام Android أو iOS أو Windows تم فيه تثبيت تطبيق المحمول. | البحث عن التطبيق في متجر التطبيقات المناسب.                                                                                                                     |

## <a name="introduction"></a>مقدمة
تتطلب عمليات الموافقة على فواتير المحمول‬ للمورّد الإصلاحات العاجلة الثلاثة الموضحة في قسم "المتطلبات الأساسية‬". لا توفر هذه الإصلاحات العاجلة مساحة عمل لعمليات الموافقة على الفواتير. لمعرفة ما هي مساحة العمل في سياق المحمول، اقرأ دليل المحمول المذكور في قسم "المتطلبات الأساسية‬". يجب تصميم مساحة عمل عمليات الموافقة على الفواتير. 

تقوم كل مؤسسة بتنظيم وتعريف عمليات الأعمال الخاصة بفواتير المورّد بشكل مختلف. قبل أن تقوم بتصميم تجربة المحمول لعمليات الموافقة على فواتير المورّد، يجب مراعاة الجوانب التالية من عملية الأعمال. ويمكن استخدام نقاط البيانات هذه إلى أقصى حد ممكن لتحسين تجربة المستخدم على الجهاز.

-   ما هي الحقول من رأس الفاتورة التي سيحتاج المستخدم إلى رؤيتها في تجربة المحمول، وبأي ترتيب؟
-   ما هي الحقول من سطور الفاتورة التي سيحتاج المستخدم إلى رؤيتها في تجربة المحمول، وبأي ترتيب؟‬
-   ما عدد سطور الفاتورة الموجودة في فاتورة؟ يمكنك هنا تطبيق القاعدة 80-20، والتحسين إلى 80 في المائة.
-   هل سيرغب المستخدمون في رؤية التوزيع المحاسبي (أكواد الفواتير) على الجهاز المحمول أثناء المراجعات؟ إذا كان الجواب على هذا السؤال "نعم"، فعليك أخذ الأسئلة التالية في الاعتبار:
    -   ما عدد التوزيعات المحاسبية (السعر المفصل وضريبة المبيعات والمصاريف والتقسيمات وغير ذلك) لبند الفاتورة؟ مرة أخرى، يجب تطبيق القاعدة 80-20.
    -   هل تتضمن الفواتير توزيعات محاسبية على رأس الفاتورة؟ إذا كان الأمر كذلك، فيجب أن تكون هذه التوزيعات المحاسبية متوفرة على الجهاز؟

    > [!NOTE]
    > لا يفسر هذا الموضوع كيفية تحرير التوزيعات المحاسبية، لأن هذه الوظيفة غير معتمدة حاليًا لسيناريوهات المحمول.

-   هل سيحتاج المستخدمون لمشاهدة مرفقات الفاتورة على الجهاز؟

سوف يختلف تصميم تجربة المحمول لعمليات الموافقة على الفواتير، وفقًا للإجابات على هذه الأسئلة. يهدف ذلك إلى تحسين تجربة المستخدم الخاصة بعملية الأعمال على جهاز محمول في مؤسسة. في بقية هذا الموضوع، سوف ننظر إلى شكلين مختلفين من السيناريوهات يستندان إلى أجوبة مختلفة على الأسئلة السابقة. 

كتوجيه عام، عندما تعمل مع مصمم المحمول، تأكد من "نشر" التغييرات لتجنب فقدان التحديثات.

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a>تصميم سيناريو بسيط للموافقة على الفواتير لشركة Contoso
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>سمة السيناريو</th>
<th>الإجابة</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ما هي الحقول من رأس الفاتورة التي سيحتاج المستخدم إلى رؤيتها في تجربة المحمول، وبأي ترتيب؟</td>
<td><ol>
<li>اسم المورّد</li>
<li>إجمالي الفاتورة</li>
<li>حساب الفاتورة</li>
<li>رقم الفاتورة</li>
<li>تاريخ الفاتورة</li>
<li>وصف الفاتورة</li>
<li>تاريخ الاستحقاق</li>
<li>عملة الفاتورة</li>
</ol></td>
</tr>
<tr class="even">
<td>ما هي الحقول من سطور الفاتورة التي سيحتاج المستخدم إلى رؤيتها في تجربة المحمول، وبأي ترتيب؟‬</td>
<td><ol>
<li>فئة التدبير</li>
<li>الكمية</li>
<li>سعر الوحدة</li>
<li>المبلغ الصافي للسطر</li>
<li>مبلغ 1099</li>
</ol></td>
</tr>
<tr class="odd">
<td>ما عدد سطور الفاتورة الموجودة في فاتورة؟ يمكنك هنا تطبيق القاعدة 80-20، والتحسين إلى 80 في المائة.</td>
<td>1</td>
</tr>
<tr class="even">
<td>هل سيرغب المستخدمون في رؤية التوزيع المحاسبي (أكواد الفواتير) على الجهاز المحمول أثناء المراجعات؟</td>
<td>نعم</td>
</tr>
<tr class="odd">
<td>ما عدد التوزيعات المحاسبية (السعر المفصل وضريبة المبيعات والمصاريف وغير ذلك) لبند الفاتورة؟ مرة أخرى، يجب تطبيق القاعدة 80-20.</td>
<td>السعر المفصل: 2 ضريبة المبيعات: 0 المصروفات: 0</td>
</tr>
<tr class="even">
<td>هل تتضمن الفواتير توزيعات محاسبية على رأس الفاتورة؟ إذا كان الأمر كذلك، فيجب أن تكون هذه التوزيعات المحاسبية متوفرة على الجهاز؟</td>
<td>غير مستخدم</td>
</tr>
<tr class="odd">
<td>هل سيحتاج المستخدمون لمشاهدة مرفقات الفاتورة على الجهاز؟</td>
<td>‏‏نعم</td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a>إنشاء مساحة العمل

1.  في المستعرض، قم بتسجيل الدخول إلى التطبيق.
2.  بعد تسجيل الدخول، قم بإلحاق **&mode=mobile** بعنوان URL كما هو مبين في المثال التالي، وحدّث الصفحة: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**
3.  انقر فوق زر **الإعدادات** (الترس) في الجزء العلوي الأيسر من الصفحة، ثم انقر فوق **تطبيق المحمول**. يجب أن يظهر مصمم التطبيق المحمول تمامًا كما يظهر مسجل المهام.
4.  انقر فوق **إضافة** لإنشاء مساحة عمل جديدة. على سبيل المثال، يمكنك تسمية مساحة العمل **موافقاتي**.
5.  أدخل وصفًا.
6.  حدد لون مساحة عمل. سيتم استخدام لون مساحة العمل للنمط العام لتجربة المحمول لمساحة العمل هذه.
7.  حدد أيقونة لمساحة العمل.
8.  انقر فوق **تم**
9.  انقر فوق **نشر مساحة العمل** لحفظ التغييرات

### <a name="vendor-invoices-assigned-to-me"></a>فواتير المورَّد المعينة إلي

صفحة المحمول الأولى التي يجب تصميمها هي قائمة الفواتير التي تم تعيينها للمستخدم لكي يراجعها. لتصميم صفحة المحمول هذه استخدم الصفحة **VendMobileInvoiceAssignedToMeListPage**. قبل إكمال هذا الإجراء، تأكد من تعيين فاتورة مورّد واحد على الأقل لك للمراجعة، ومن وجود توزيعين لبند الفاتورة. هذا الإعداد يفي بمتطلبات هذا السيناريو.

1.  في عنوان URL، استبدل اسم عنصر القائمة بالاسم **VendMobileInvoiceAssignedToMeListPage** لفتح إصدار المحمول لصفحة القائمة **فواتير المورّد المعلقة المعينة إليّ‬** في وحدة **الحسابات الدائنة**. بحسب عدد الفواتير المعينة لك في النظام، ستعرض هذه الصفحة تلك الفواتير. للبحث عن فاتورة معينة، يمكنك استخدام عامل التصفية إلى اليمين. ومع ذلك، لا نحتاج إلى فاتورة معينة لهذا المثال. نحن نحتاج فقط إلى فاتورة معينة لك سوف تسمح لك بتصميم صفحة المحمول. تم تصميم الصفحات الجديدة المتوفرة خصيصًا لتطوير سيناريوهات المحمول لفاتورة المورّد. ولذلك، يجب استخدام هذه الصفحات. يجب أن يكون عنوان URL مماثلاً لعنوان URLالتالي، وبعد أن تقوم بإدخاله، يجب أن تظهر الصفحة المعروضة في الشكل التوضيحي: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile 

    [![فواتير المورد المعلقة المعينة إلى صفحتي](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)
    
2.  انقر فوق زر **الإعدادات** (الترس) في الجزء العلوي الأيسر من الصفحة، ثم انقر فوق **تطبيق المحمول**
3.  حدد مساحة العمل، ثم انقر فوق **تحرير**
4.  انقر فوق **صفحة إضافة** لإنشاء صفحة المحمول الأولى.
5.  أدخل اسمًا، مثل **فواتير المورّد الخاصة بي**، ووصفًا، مثل **فواتير المورّد المعينة إليّ للمراجعة**.
6.  انقر فوق **تم‏‎**.
7.  في مصمم المحمول، على علامة تبويب **الحقول**، انقر فوق **تحديد الحقول‬**. يجب أن تكون الأعمدة في صفحة القائمة مماثلة للشكل التوضيحي التالي. 

    [![أعمدة على صفحة فواتير المورّد المعلقة المعينة إليّ‬](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)
    
8.  أضف الأعمدة المطلوبة من صفحة القائمة التي يجب أن تظهر للمستخدم في صفحة المحمول. الترتيب الذي تستخدمه لإضافة الأعمدة هو الترتيب الذي ستظهر فيه الحقول للمستخدم النهائي. الطريقة الوحيدة لتغيير ترتيب حقول هي إعادة تحديد كافة الحقول. استنادًا إلى متطلبات هذا السيناريو، تعتبر الحقول الثمانية التالية مطلوبة. ومع ذلك، قد يجد بعض المستخدمين أن الحقول الثمانية تشكل كمية كبيرة جدًا من المعلومات على جهاز محمول. ولذلك، سنعرض أهم الحقول فقط في طريقة عرض قائمة المحمول. وستظهر الحقول المتبقية في طريقة عرض التفاصيل التي سوف نصممها لاحقًا. الآن، سوف نقوم بإضافة الحقول التالية. انقر فوق علامة الجمع (**+**) في هذه الأعمدة لإضافتها إلى صفحة المحمول.
    - اسم المورّد
    - إجمالي الفاتورة
    - حساب الفاتورة
    - رقم الفاتورة
    - تاريخ الفاتورة

    بعد إضافة الحقول، يجب أن تشبه صفحة المحمول الشكل التوضيحي التالي. 
    
    [![الصفحة بعد إضافة الحقول](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)

9.  يجب أيضًا إضافة الأعمدة التالية الآن، من أجل تمكين إجراءات سير العمل فيما بعد.
    - إظهار المهمة المكتملة
    - إظهار تفويض المهمة
    - إظهار استدعاء المهمة
    - إظهار رفض المهمة
    - إظهار طلب إكمال المهمة
    - إظهار إعادة إرسال المهمة

10. انقر فوق **تم** لإنهاء وضع التحرير.
11. انقر فوق **السابق** ثم **تم** للخروج من مساحة العمل
12. انقر فوق **نشر مساحة العمل** لحفظ عملك.
13. قم بتمكين **عرض إجماليات الفاتورة على قائمة فواتير المورد المعلقة‬** في معلمات الحسابات الدائنة ضمن **الفاتورة**. تجدر الإشارة إلى أنه فقط من خلال تمكين هذه المعلمة، سيتم حساب إجماليات الفواتير لعرضها في صفحة قائمة فواتير المورد المعلقة. هذه قدرة جديدة كجزء من الإصلاح العاجل 3208224 ضمن المتطلبات الأساسية.

### <a name="vendor-invoice-details"></a>تفصيل فاتورة المورّد

لتصميم صفحة تفاصيل الفاتورة للمحمول، استخدم الصفحة **VendMobileInvoiceHeaderDetails**. لاحظ أنه، استنادًا إلى عدد الفواتير في النظام، تعرض هذه الصفحة الفواتير الأقدم (الفاتورة التي تم إنشاؤها أولاً). للبحث عن فاتورة معينة، يمكنك استخدام عامل التصفية إلى اليمين. ومع ذلك، لا نحتاج إلى فاتورة معينة لهذا المثال. نحن نطلب فقط بعض بيانات الفاتورة لكي نتمكن من تصميم صفحة المحمول. 

[![صفحة سير العمل](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)

1. في عنوان URL، استبدل اسم عنصر القائمة بالاسم **VendMobileInvoiceHeaderDetails** لفتح النموذج

2. افتح مصمم المحمول من زر **الإعدادات** (الترس).

3. انقر فوق الزر **تحرير** لبدء وضع التحرير في مساحة العمل.

4. حدد صفحة **فواتير المورّد الخاصة بي** التي قمت بإنشائها سابقًا، ثم انقر فوق **تحرير**.

5. على علامة تبويب **الحقول**، انقر فوق عنوان العمود **الشبكة**.

6. انقر فوق **‎خصائص &gt; إضافة صفحة**. **ملاحظة:** عندما تنقر فوق العنوان **الشبكة** وتضيف صفحة، تتأسس العلاقة مع صفحة التفاصيل بشكل تلقائي.

7. أدخل عنوان صفحة، مثل **تفاصيل الفاتورة**، ووصفًا، مثل **عرض رأس الفاتورة وتفاصيل البنود**.

8. انقر فوق **تحديد الحقول**. لاحظ أن الترتيب الذي تستخدمه لإضافة الأعمدة هو الترتيب الذي ستظهر فيه الحقول للمستخدم النهائي. الطريقة الوحيدة لتغيير ترتيب حقول هي إعادة تحديد كافة الحقول. 

9. أضف الحقول التالية من الرأس، استنادًا إلى متطلبات هذا السيناريو:
   - اسم المورّد
   - إجمالي الفاتورة
   - حساب الفاتورة
   - رقم الفاتورة
   - تاريخ الفاتورة
   - وصف الفاتورة
   - تاريخ الاستحقاق
   - عملة الفاتورة

10. أضف الحقول التالية من خطوط الشبكة في الصفحة:
    - فئة التدبير
    - الكمية
    - سعر الوحدة
    - المبلغ الصافي للسطر
    - مبلغ 1099

11. بعد إضافة كافة الحقول من الخطوتين السابقتين، انقر فوق **تم**. يجب أن تكون الصفحة مماثلة للشكل التوضيحي التالي.
    
    [![الصفحة بعد إضافة الحقول](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)

12. انقر فوق **تم** لإنهاء وضع التحرير.

13. انقر فوق **السابق** ثم **تم** للخروج من مساحة العمل

14. انقر فوق **نشر مساحة العمل** لحفظ عملك

### <a name="workflow-actions"></a>إجراءات سير العمل

لإضافة إجراءات سير العمل، استخدم صفحة **VendMobileInvoiceHeaderDetails**.  لفتح هذه الصفحة، استبدل اسم عنصر القائمة في URL، كما فعلت سابقًا. ثم افتح مصمم المحمول من زر **الإعدادات** (الترس). اتبع هذه الخطوات لإضافة إجراءات سير العمل في صفحة التفاصيل. من الضروري أن تكون الفواتير المعينة لك في الحالة المناسبة التي تسمح بجعل إجراءات سير العمل التي ستعمل على تصميمها متوفرة لك.

#### <a name="record-workflow-actions"></a>تسجيل إجراءات سير العمل
1.  انقر فوق الزر **تحرير** لبدء وضع التحرير في مساحة العمل.
2.  حدد صفحة **تفاصيل الفاتورة** التي قمت بإنشائها سابقًا، ومن ثم انقر فوق **تحرير**.
3.  على علامة تبويب **الإجراءات**، انقر فوق **إضافة إجراء**.
4.  أدخل عنوان إجراء، مثل **الموافقة**، ووصفًا، مثل **الموافقة على الفاتورة**. لاحظ أن عنوان الإجراء الذي تدخله هنا يصبح اسم الإجراء الذي يظهر للمستخدم في تطبيق المحمول.
5.  انقر فوق **تم**.
6.  انقر فوق **تحديد الحقول**.
7.  انتقل عبر عملية سير العمل في صفحة **VendMobileInvoiceHeaderDetails‎**، وأكمل الإجراء الذي تريد تسجيله. تأكد من إدخال تعليقات سير العمل أثناء هذه العملية، بحيث يتم أيضًا تضمين حقل تعليقات في تجربة المحمول.
8.  بعد أن يتم تشغيل إجراء سير العمل، انقر فوق **تم** لإكمال مهمة تحديد الحقول.
9.  انقر فوق **تم** لإنهاء وضع التحرير.
10. انقر فوق **السابق** ثم **تم** للخروج من مساحة العمل
11. انقر فوق **نشر مساحة العمل** لحفظ عملك
12. كرر الخطوات السابقة لتسجيل كافة إجراءات سير العمل المطلوبة. 

#### <a name="create-a-js-file"></a>إنشاء ملف .js
1. افتح المفكرة أو Microsoft Visual Studio، ثم الصق التعليمات البرمجية التالية. احفظ الملف بصيغة ملف .js. تقوم هذه التعليمات البرمجية بما يلي:
    - إنها تخفي الأعمدة الإضافية المرتبطة بسير العمل التي أضفناها في وقت سابق في صفحة قائمة المحمول. لقد أضفنا هذه الأعمدة لكي يحصل التطبيق على هذه المعلومات في السياق ولكي يتمكن من القيام بالخطوة التالية.
    - استنادًا إلى خطوة سير العمل النشط، تطبق هذه التعليمات البرمجية المنطق لإظهار تلك الإجراءات فقط.

    > [!NOTE]
    > يجب أن يكون اسم الصفحات وعناصر التحكم الأخرى الموجودة في التعليمات البرمجية نفسها الأسماء الموجودة في مساحة العمل.

    ```javascript
    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                       var showRejectControl = Boolean(rejectControl == 1);
                      var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                     metadataService.configureAction('Resubmit', { visible: showResubmitControl });
                   }
                 },
           };
        }
    ```

2.  تحميل ملف التعليمات البرمجية إلى مساحة العمل عن طريق تحديد علامة التبويب **منطق**
3.  انقر فوق **تم** لإنهاء وضع التحرير.
4.  انقر فوق **السابق** ثم **تم** للخروج من مساحة العمل
5.  انقر فوق **نشر مساحة العمل** لحفظ عملك

### <a name="vendor-invoice-attachments"></a>مرفقات فواتير المورّد

1. انقر فوق زر **الإعدادات** (الترس) في الجزء العلوي الأيسر من الصفحة، ثم انقر فوق **تطبيق المحمول**

2. انقر فوق الزر **تحرير** لبدء وضع التحرير في مساحة العمل.

3. حدد صفحة <strong>تفاصيل الفاتورة** التي قمت بإنشائها سابقًا، ثم انقر فوق **تحرير</strong>.

4. عيّن الخيار **إدارة المستندات** إلى **نعم** كما هو موضح أدناه. **ملاحظة:** في حال عدم وجود أي متطلبات تتعلق بإظهار المرفقات على جهاز محمول، يمكنك ترك هذا الخيار معينًا إلى **لا**، وهو الإعداد الافتراضي.
   
   ![إدارة المستندات](./media/docmanagement-216x300.png)

5. انقر فوق **تم** لإنهاء وضع التحرير.

6. انقر فوق **السابق** ثم **تم** للخروج من مساحة العمل

7. انقر فوق **نشر مساحة العمل** لحفظ عملك

### <a name="vendor-invoice-line-distributions"></a>توزيعات بنود فاتورة المورّد

تؤكد متطلبات هذا السيناريو أنه سيكون هناك توزيعات على مستوى البنود فقط، وأن الفاتورة ستتضمن بندًا واحدًا فقط في كل الأوقات. ونظرًا لبساطة هذا السيناريو، يجب أن تكون تجربة المستخدم على الجهاز المحمول بسيطة بما يكفي بحيث لن يحتاج المستخدم إلى التنقل لعدة مستويات للأسفل لعرض التوزيعات. تتضمن فواتير المورّد خيارًا يسمح بعرض كافة توزيعات من رأس الفاتورة. هذه التجربة هي تلك التي نحتاجها لسيناريو المحمول. ولذلك، سوف نستخدم صفحة **VendMobileInvoiceAllDistributionTree** لتصميم هذا الجزء من سيناريو المحمول. 

> [!NOTE] 
> من شأن معرفة المتطلبات أن يساعدنا على تحديد الصفحة المحددة التي يجب استخدامها وكيفية تحسين تجربة المحمول للمستخدم بدقة عند تصميم السيناريو. في السيناريو الثاني، سوف نستخدم صفحة مختلفة لعرض التوزيعات، بسبب اختلاف المتطلبات في ذلك السيناريو.

1.  استبدل اسم عنصر القائمة في URL، كما فعلت سابقًا. يجب أن تشبه الصفحة التي تظهر الشكل التوضيحي التالي.

    [![صفحة كافة التوزيعات](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)

2.  افتح مصمم المحمول من زر **الإعدادات** (الترس).

3.  انقر فوق الزر **تحرير** لبدء وضع التحرير في مساحة العمل. **ملاحظة:** سوف ترى أنه تم إنشاء صفحتين جديدتين تلقائيًا. يقوم النظام بإنشاء هذه الصفحات نظرًا لتشغيل إدارة المستندات في المقطع السابق. يمكنك تجاهل هذه الصفحات الجديدة.

4.  انقر فوق **إضافة صفحة**.

5.  أدخل عنوان صفحة، مثل **عرض المحاسبة**، ووصفًا، مثل **عرض المحاسبة للفاتورة**.

6.  انقر فوق **تم**.

7.  على علامة تبويب **الحقول**، انقر فوق **تحديد حقول**، وحدد الحقول التالية من صفحة التوزيعات وثم انقر فوق **تم**:
    1.  المبلغ
    2.  العملة
    3.  حساب دفتر الأستاذ

    > [!NOTE] 
    > لم نحدد عمود **الوصف** من شبكة التوزيعات، لأن متطلبات هذا السيناريو أكدت أن السعر المفصل هو المبلغ الوحيد الذي سيكون هناك توزيعات له. لذلك، لن يحتاج المستخدم إلى حقل آخر لتحديد نوع المبلغ الذي سيكون التوزيع متعلقًا به. ومع ذلك، في السيناريو التالي، **سوف** نستخدم هذه المعلومات، لأن متطلبات هذا السيناريو تحدد أن أنواع المبالغ الأخرى لديها توزيعات (على سبيل المثال، ضريبة المبيعات).

8.  انقر فوق **تم** لإنهاء وضع التحرير.

9.  انقر فوق **السابق** ثم **تم** للخروج من مساحة العمل

10. انقر فوق **نشر مساحة العمل** لحفظ عملك

#### <a name="adding-navigation-to-view-accounting-page"></a>إضافة التنقل إلى صفحة "عرض المحاسبة"

إن صفحة المحمول **عرض المحاسبة** غير مرتبطة حاليًا بأي من صفحات المحمول التي قمنا بتصميمها حتى الآن. بما أنه يتعين على المستخدم أن يكون قادرًا على الانتقال إلى صفحة **عرض المحاسبة** من صفحة **تفاصيل الفاتورة** على الجهاز المحمول، يجب أن نوفر إمكانية التنقل من صفحة **تفاصيل الفاتورة** إلى صفحة **عرض المحاسبة**. إننا نستخدم منطقًا إضافيًا عبر JavaScript لتأسيس إمكانية التنقل هذه.

1.  افتح ملف.js الذي أنشأته مسبقًا، وأضف البنود المميزة في التعليمات البرمجية التالية. تقوم هذه التعليمات البرمجية بأمرين:
    1.  إنها تساعد على ضمان عدم قدرة المستخدمين على الانتقال مباشرة من مساحة العمل إلى صفحة **عرض المحاسبة**.
    2.  إنها تنشئ عنصر تحكم تنقل من صفحة **تفاصيل الفاتورة** إلى صفحة **عرض المحاسبة**.

    > [!NOTE] 
    > يجب أن يكون اسم الصفحات وعناصر التحكم الأخرى الموجودة في التعليمات البرمجية نفسها الأسماء الموجودة في مساحة العمل.

    ```javascript
    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
                   // Hide pages not applicable for root navigation
                   metadataService.hideNavigation('View-accounting');
                   //Link to view accounting
                   metadataService.addLink('Invoice-details', 'View-accounting', 'View-accounting-nav-control', 'View accounting', true);
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                     var showRejectControl = Boolean(rejectControl == 1);
                       var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                       metadataService.configureAction('Resubmit', { visible: showResubmitControl });
        }
                 },
           };
        }
    ```
    
2.  تحميل ملف التعليمات البرمجية إلى مساحة العمل عن طريق تحديد علامة التبويب **منطق** للكتابة فوق التعليمات البرمجية السابقة
3.  انقر فوق **تم** لإنهاء وضع التحرير.
4.  انقر فوق **السابق** ثم **تم** للخروج من مساحة العمل
5.  انقر فوق **نشر مساحة العمل** لحفظ عملك

### <a name="validation"></a>التحقق من الصحة

من الجهاز المحمول، افتح التطبيق، واتصل بالمثيل الخاص بك. تأكد من تسجيل الدخول إلى الشركة حيث تم تعيين لك فواتير المورّد للمراجعة. يجب أن تكون قادرًا على تنفيذ الإجراءات التالية:

-   رؤية مساحة عمل **موافقاتي**.
-   التنقل في مساحة عمل **موافقاتي** ورؤية صفحة **فواتير المورّد الخاصة بي**.
-   التنقل في صفحة **فواتير المورّد الخاصة بي** ورؤية قائمة الفواتير التي تم تعيينها لك.
-   التنقل في إحدى الفواتير، ورؤية تفاصيل رأس الفاتورة وتفاصيل البنود.
-   في صفحة التفاصيل، رؤية ارتباط إلى المرفقات، واستخدام هذا الارتباط للانتقال إلى قائمة المرفقات وعرض المرفقات.
-   في صفحة التفاصيل، رؤية ارتباط إلى صفحة **عرض المحاسبة**، واستخدام هذا الارتباط للانتقال إلى صفحة التوزيعات وعرض التوزيعات.
-   في صفحة التفاصيل، النقر فوق قائمة **إجراءات** في الجزء السفلي، وتنفيذ إجراءات سير العمل التي تنطبق على خطوة سير العمل.

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a>تصميم سيناريو معقد للموافقة على الفواتير لشركة Fabrikam
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>سمة السيناريو</th>
<th>الإجابة</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ما هي الحقول من رأس الفاتورة التي سيحتاج المستخدم إلى رؤيتها في تجربة المحمول، وبأي ترتيب؟</td>
<td><ol>
<li>اسم المورّد</li>
<li>مبلغ الفاتورة</li>
<li>حساب الفاتورة</li>
<li>رقم الفاتورة</li>
<li>تاريخ الفاتورة</li>
<li>وصف الفاتورة</li>
<li>تاريخ الاستحقاق</li>
<li>عملة الفاتورة</li>
</ol></td>
</tr>
<tr class="even">
<td>ما هي الحقول من سطور الفاتورة التي سيحتاج المستخدم إلى رؤيتها في تجربة المحمول، وبأي ترتيب؟‬</td>
<td><ol>
<li>فئة التدبير</li>
<li>الكمية</li>
<li>سعر الوحدة</li>
<li>المبلغ الصافي للسطر</li>
<li>مبلغ 1099</li>
</ol></td>
</tr>
<tr class="odd">
<td>ما عدد سطور الفاتورة الموجودة في فاتورة؟ يمكنك هنا تطبيق القاعدة 80-20، والتحسين إلى 80 في المائة.</td>
<td>5</td>
</tr>
<tr class="even">
<td>هل سيرغب المستخدمون في رؤية التوزيع المحاسبي (أكواد الفواتير) على الجهاز المحمول أثناء المراجعات؟</td>
<td>نعم</td>
</tr>
<tr class="odd">
<td>ما عدد التوزيعات المحاسبية (السعر المفصل وضريبة المبيعات والمصاريف وغير ذلك) لبند الفاتورة؟ مرة أخرى، يجب تطبيق القاعدة 80-20.</td>
<td>السعر المفصل: 2 ضريبة المبيعات: 2 المصروفات: 2</td>
</tr>
<tr class="even">
<td>هل تتضمن الفواتير توزيعات محاسبية على رأس الفاتورة؟ إذا كان الأمر كذلك، فيجب أن تكون هذه التوزيعات المحاسبية متوفرة على الجهاز؟</td>
<td>غير مستخدم</td>
</tr>
<tr class="odd">
<td>هل سيحتاج المستخدمون لمشاهدة مرفقات الفاتورة على الجهاز؟</td>
<td>نعم</td>
</tr>
</tbody>
</table>

### <a name="next-steps"></a>الخطوات التالية

يمكن تنفيذ الأشكال المختلفة التالية للسيناريو الأول، استنادًا إلى متطلبات السيناريو الثاني. يمكنك استخدام هذا المقطع لتحسين تجربتك في استخدام تطبيقات المحمول.

1.  نظرًا لتوقع المزيد من بنود الفاتورة في السيناريو 2، تساعد التغييرات التالية على التصميم في تحسين تجربة المستخدم على الجهاز المحمول:
    1.  بدلاً من عرض بنود الفاتورة على صفحة "التفاصيل" (كما في السيناريو 1)، باستطاعة المستخدمين اختيار عرض البنود في صفحة محمول منفصلة.
    2.  نظرً لتوقع أكثر من بند فاتورة في هذا السيناريو، إذا تم استخدام صفحة **VendMobileInvoiceAllDistributionTree** لتصميم صفحة التوزيعات للمحمول (كما في السيناريو 1)، فقد يشكل ربط البنود بالتوزيعات مصدر إرباك للمستخدم. ولذلك، استخدم صفحة **VendMobileInvoiceLineDistributionTree‎** لتصميم صفحة التوزيعات.
    3.  ومن الناحية المثالية، ينبغي أن تظهر التوزيعات في سياق بند فاتورة في هذا السيناريو. لذلك، تأكد من أنه باستطاعة المستخدم الانتقال إلى البند لرؤية صفحة التوزيعات. استخدم القدرة على ربط الصفحة لتأسيس عملية تنقل، تمامًا كما فعلت للرأس وصفحة التفاصيل في السيناريو 1.

2.  نظرًا لتوقع أكثر من نوع مبلغ واحد على التوزيعات في السيناريو 2 (رسوم ضريبة المبيعات وغير ذلك)، سيكون من المفيد عرض الوصف الخاص بنوع المبلغ. (لقد حذفنا هذه المعلومات في السيناريو 1.)




