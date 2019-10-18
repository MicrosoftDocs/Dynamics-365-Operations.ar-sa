---
title: عرض التقارير المالية وتصميمها
description: تقدم هذه المقالة التمارين التي تنقلك عبر عرض وإنشاء التقارير المالية لتطبيق Microsoft Dynamics 365 Finance.
author: jcart1106
manager: AnnBe
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReportingSetup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 10814
ms.assetid: cd5f6483-c09b-4c2d-9336-d22eb6ab6e4f
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dc68289514dc3b201b423091c92fa128d3065707
ms.sourcegitcommit: 7bec89b33a56447072d01066af4da473b8092ca8
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/02/2019
ms.locfileid: "2536791"
---
# <a name="view-and-design-financial-reports"></a>عرض التقارير المالية وتصميمها

[!include [banner](../includes/banner.md)]

تقدم هذه المقالة التمارين التي تنقلك عبر عرض وإنشاء التقارير المالية لتطبيق Microsoft Dynamics 365 Finance. تتألف ميزة إعداد التقارير المالية من تجربة عرض داخل التطبيق ومصمم تقارير من نقرة واحدة يتيح لك إنشاء التقارير المالية وتحريرها.

## <a name="exercise-1-generate-and-explore-a-default-financial-report"></a>تمرين 1: إنشاء واستكشاف تقرير مالي افتراضي

في هذا التمرين، ستقوم بإنشاء واستكشاف تقرير افتراضي موجود. ويشمل هذا التقرير كافة الحسابات ويحتوي أيضًا على خصائص (سمات) الحساب للحسابات. ستتنقل ضمن تفاصيل الحركة، واستخدام عوامل تصفية الأبعاد، وتغيير العملة في التقرير. أولاً، سنقوم بتحديث ترتيب عرض الأبعاد للتقارير المالية. يسمح لك هذا باختيار كيفية عرض الأبعاد ليس فقط أثناء تصميم وعرض التقارير المالية.

1. انتقل إلى **تكوين الأبعاد المالية لتكامل التطبيقات‬** ضمن **الأبعاد مخطط الحسابات** في دفتر الأستاذ العام.
2. انقل الأبعاد لتكون في الترتيب التالي:

    1. الحساب الرئيسي
    2. وحدة الأعمال
    3. مركز التكلفة
    4. القسم

    > [!NOTE]
    > من الممكن أن تبقى الأبعاد الأخرى بالترتيب الذي توجد فيه حاليًا.

3. احفظ تكوين البعد. وبعد ذلك، سنقوم بإنشاء تقرير واستكشاف البيانات الموجودة في هذا التقرير.
4. انتقل إلى **التقارير المالية** ضمن **الاستعلامات والتقارير** في دفتر الأستاذ العام.
5. حدد الصف للتقرير المسمى **تفاصيل دفتر الأستاذ العام - الافتراضي**.
6. حدد **تحرير**.

    > [!NOTE]
    > ستتم مطالبتك بتنزيل مصمم التقارير بنقرة واحدة وتسجيل الدخول. واستخدام بيانات الاعتماد الخاصة بك لتسجيل الدخول.

7. قم بتغيير سنة الأساس إلى عام 2012، وحدد **إنشاء**. عند إنشاء تقرير من مصمم التقارير، سيتم فتحه في علامة تبويب جديدة في المستعرض. يمكنك إما استكشاف التقرير في علامة تبويب المستعرض الجديدة، أو الانتقال إلى علامة تبويب المستعرض الأصلية وفتح التقرير من هناك عن طريق تحديده من قائمة **التقارير المالية**.
8. في التقرير المفتوح، حدد أحد المبالغ للتنقل في تفاصيل الحساب الخاص بالتقرير.
9. وبمجرد الوجود في تفاصيل الحساب، حدد حساب مشتمل على البيانات وقم **بالتنقل إلى مستوى حركات التقرير**. وعلى مستوى حركة التقرير، يمكنك مشاهدة الخصائص (السمات) المضمنة في تصميم هذا التقرير. واستنادًا إلى الحركة والحساب، قد يتم عرض بعض أو كافة السمات.
10. إغلاق مستوى حركات التقرير.
11. حدد الحساب نفسه أو حسابًا آخر و**افتح حركات الإيصال.**. تتم تصفية حركات الإيصال للفترة والسنة والحساب + مجموعة أبعاد الحساب المحدد. ومن حركات الإيصال، يمكنك اختيار استكشاف معلومات أخرى حول الحركة.
12. إغلاق حركات الإيصال. داخل تقرير مالي، يمكنك اختيار عرض البيانات لفترة وسنة مختلفة أو بتطبيق أبعاد وسمات مختلفة. ويتم تنفيذ هذا باستخدام **خيارات التقرير**.
13. حدد **خيارات التقرير**.
14. حدد **إضافة عامل تصفية بعد** واختر **وحدة الأعمال**.
15. أدخل 001 في الحقل، وحدد **موافق**. يعرض التقرير الآن البيانات فقط لوحدة الأعمال 001. هذه طريقة عرض مخصصة للتقرير ولا تتوفر للآخرين لعرضها.
16. قم بإغلاق التقرير المصفى. يمكن عرض التقارير المالية بأية عملة تمت إضافتها إلى التطبيق.
17. حدد **العملة**، ثم حدد **اليورو**. يعرض التقرير الآن العملة باليورو. يتم الآن عرض أي أكواد عملة أو رموز عملة مضمنة في تصميم التقرير بالعملة المطبقة. وإذا لم يتم تحديد أي رمز عملة لعملة، فإنه لا يتم عرض رمز العملة.
18. أغلق تقرير **تفاصيل دفتر الأستاذ العام**.
19. أغلق **مصمم التقارير**.

## <a name="exercise-2-add-additional-account-properties-to-a-report-design"></a>التمرين 2: إضافة خصائص الحساب إضافية إلى تصميم التقرير
في هذا التمرين، ستقوم بتعديل تقرير افتراضي موجود. وستقوم بتحديث تعريف الصف لتضمين كافة الحسابات وتعريف العمود بحيث يحتوي على سمات الحساب. وبمجرد اكتمال التحديثات، ستقوم بتوليد التقرير الذي تم إنشاؤه حديثًا وستستكشفه. سنبدأ من قائمة التقارير المالية.

1. انتقل إلى **التقارير المالية** ضمن الاستعلامات والتقارير في دفتر الأستاذ العام.
2. حدد الصف للتقرير المسمى **ميزان المراجعة الملخص - الافتراضي**.
3. حدد **تحرير**. **ميزان المراجعة الملخص – الافتراضي** سيُفتح في مصمم التقارير.
4. حدد **ملف**، ثم **حفظ باسم**، وقم بتسمية التقرير باسم "ميزان المراجعة التفصيلية مع السمات".

    > [!NOTE]
    > في أي وقت يتم فيه إنشاء تقرير جديد في مصمم التقرير، يتم تحديث قائمة التقارير المالية.

5. من تعريف التقرير، حدد رمز تعريف الصف لفتح **ميزان المراجعة – تعريف الصف الافتراضي**.
6. احفظ تعريف الصف باسم **ميزان المراجعة التفصيلية مع السمات**
7. وبوضع المؤشر فوق الصف 50، حدد **تحرير**، ثم **إدراج صفوف من الأبعاد**. يسمح لك إدراج صفوف من الأبعاد باختيار الأبعاد التي تريدها أن تكون موجودة في تعريف الصف. وفي هذا التمرين، سنقوم بإنشاء تعريف الصف باستخدام "الحساب الرئيسي".
8. وتأكد من أن **الحساب الرئيسي** يحتوي على كافة علامات العطف، وحدد **موافق**. يحتوي تعريف الصف الآن على كافة الحسابات الرئيسية للكيان القانوني USMF.
9. قم بالتمرير لأسفل إلى الصف 11110 واحذف الصف 11110.
10. في الصف 11080، حدد **--- (وضع شرطة سفلية تحت المبالغ)**.
11. في الصف 11140، اكتب **إجمالي كافة الحسابات** في العمود ب.
12. وفي العمود C، حدد **الإجمالي** من القائمة المنسدلة.
13. أدخل **50:11080** في العمود د.
14. **احفظ** تعريف الصف. يحتوي تعريف الصف الآن على كافة الحسابات بالإضافة إلى صف مجموع لإضافة كافة الحسابات معًا. وبعد ذلك، سنقوم بتحديث تعريف العمود لتضمين سمات الحساب الإضافية.
15. من تعريف تقرير **ميزان المراجعة التفصيلية مع السمات**، حدد رمز تعريف العمود لفتح تعريف عمود **ميزان المراجعة الملخص – الافتراضي**.
16. احفظ تعريف العمود باسم **ميزان المراجعة التفصيلية مع السمات** يحتوي تعريف العمود على أعمدة البيانات المالية وعمود وصف وأعمدة حساب. وسنقوم بإضافة أعمدة السمات إلى تعريف العمود لتوفير مزيد من التفاصيل حول الحسابات.
17. سوف تُضاف السمات التالية إلى تعريف العمود:

    - رقم دفتر اليومية
    - وصف دفتر اليومية
    - تاريخ الحركة
    - تم الإنشاء بواسطة
    - آخر تعديل بواسطة

18. في العمود الأول، حدد **السمة** كنوع عمود. وبعد ذلك، حدد **رقم دفتر اليومية** كفئة سمة.
19. واصل إضافة الأعمدة إلى السمات المتبقية.
20. في صف **الرأس 2**، قم بإضافة الأوصاف لكل عمود من الأعمدة الجديدة التي تمت إضافتها.
21. احفظ تعريف العمود. والآن بعد أن تم تحديث تعريف الصف وتعريف العمود، سنحتاج إلى إضافتهما إلى تعريف التقرير.
22. من تعريف تقرير **ميزان المراجعة التفصيلية مع السمات**، حدد ميزان المراجعة التفصيلية مع السمات لكلٍّ من تعريف الصف وتعريف العمود.
23. قم قم بتغيير سنة الأساس إلى **2012**.
24. **احفظ** تعريف التقرير و**قم بالإنشاء**. بمجرد الانتهاء من إنشاء التقرير وفتحه، يمكنك استكشاف التقرير كما فعلت في التمرين الأول. تنقل في الحسابات المختلفة لمشاهدة كيفية عرض السمات الإضافية.
25. أغلق تقرير **ميزان المراجعة التفصيلية مع السمات**.
26. أغلق **مصمم التقارير**.

## <a name="exercise-3-create-a-multidimensional-report-using-a-reporting-tree"></a>التمرين 3: إنشاء تقرير متعدد الأبعاد باستخدام شجرة التقارير
في هذا التمرين، ستقوم بتعديل تقرير افتراضي موجود. وستقوم بإنشاء شجرة تقارير وتضيفها إلى إلى تعريف تقرير لإنتاج "بيان دخل القسم/مركز التكلفة". بمجرد اكتمال التحديثات، ستقوم بإنشاء "بيان دخل القسم/مركز التكلفة" وستستكشف التقرير باستخدام شجرة التقارير. سنبدأ من قائمة التقارير المالية.

1. انتقل إلى **التقارير المالية** ضمن الاستعلامات والتقارير في دفتر الأستاذ العام.
2. حدد الصف للتقرير المسمى **بيان الدخل - الافتراضي**.
3. حدد **تحرير**. **بيان الدخل – الافتراضي** سيُفتح في مصمم التقارير.
4. في القائمة **ملف**، أشر إلى **جديد**، ثم انقر فوق **تعريف شجرة التقارير**.
5. في قائمة **تحرير**، انقر فوق **إدراج وحدات التقارير من الأبعاد**.
6. قم بإلغاء تحديد خانات الاختيار لكافة الأبعاد، فيما عدا **مركز التكلفة**.
7. انقر فوق حقل **من بُعد** لبعد مركز التكلفة، وأدخل **007**، ثم اضغط على مفتاح Tab. في حقل **إلى البُعد**، أدخل **018**.
8. **احفظ** الشجرة الناتجة باسم **مراكز التكلفة حسب القسم.** والآن بعد أن تم إنشاء شجرة التقارير، سوف تقوم بتعديل شجرة التقارير لتحتوي على ثلاث وحدات تجميع جديدة؛ Marketing وOperations وRetail.
9. في القائمة **إطار**، انقر فوق **مراكز التكلفة حسب القسم**. (إذا تم إغلاق شجرة التقارير، فحددها من "تعريفات شجرة التقارير" في جزء التنقل.)
10. انقر فوق الوحدة رقم 2، **المعارض التجارية**، وانقر فوق رمز **إدراج وحدة التقارير**.
11. انقر نقراً مزدوجاً فوق عمود الكيان في الصف الفارغ، وحدد **USMF**.
12. أدخل **التسويق** في العمودين ب وج.
13. انقر فوق الوحدة رقم 5، **عمليات الخدمة**، وانقر بزر الماوس الأيمن. **حدد إدراج وحدة التقارير**.
14. كرر الخطوة 11.
15. أدخل **العمليات** في العمودين ب وج.
16. انقر فوق رقم الوحدة الثانية عشر، **المخرج**، وانقر بزر الماوس الأيمن. حدد **إدراج وحدة التقارير**.
17. كرر الخطوة 11.
18. أدخل **البيع بالتجزئة** في العمودين ب وج. ولاحظ أنه يتم عرض وحدات العمليات والتسويق والبيع بالتجزئة في نفس مستوى وحدات التسجيل الحالية. يتم تنظيم الوحدات الجديدة بعد ذلك. ويتم تنظيم وحدات التقارير من خلال خيارات النقر بزر الماوس الأيمن; ترقية وتخفيض، أو عن طريق السحب والإفلات.
19. تحقق من أن الوحدة رقم 3، **المعارض التجارية** نشطة، وانقر بزر الماوس الأيمن.
20. حدد **تخفيض وحدة التقارير**. لاحظ أنه يتم عرض الوحدة الآن كتابع **للتسويق**.
21. انقر فوق الوحدة الرابعة، **حملة تسويقية** وانقر بزر الماوس الأيمن.
22. حدد **تخفيض وحدة التقارير**.
23. انقر فوق **عمليات الخدمة** في العرض الرسومي. اضغط مع الاستمرار على زر الماوس الأيسر أثناء سحب الوحدة إلى **العمليات**. حرر زر الماوس الأيسر لإسقاط الوحدة في تجميع Operation. كرر **الإنتاج، ومراقبة الجودة، واللوجستيات، التدبير، والإدارة**.
24. اجعل **المخرج**، و**سوبر**، و**مركز التسوق**، و**على الإنترنت** تابعة لـ **البيع بالتجزئة** عن طريق أما تخفيضها أو سحبها وإفلاتها.
25. احفظ إعادة التنظيم الناتجة. والآن قمنا بإنشاء وتنظيم شجرة التقارير، ويمكن إضافتها إلى تعريف التقرير.
26. في القائمة **إطار**، حدد **بيان الدخل – الافتراضي** لفتح تعريف التقرير.
27. انقر فوق سهم القائمة المنسدلة **نوع الشجرة**، وحدد **شجرة التقارير**.
28. انقر فوق سهم القائمة المنسدلة للشجرة، وحدد **مراكز التكلفة حسب القسم**.
29. وقم بتغيير سنة الأساس إلى **2012**، و**احفظ** التغييرات وقم **بإنشاء** التقرير. بعد اكتمال عملية إنشاء التقرير وفتحه، يمكنك استكشاف التقرير.
30. حدد القائمة المنسدلة **شجرة التقارير** لعرض وحدات التقارير. وبدلاً من ذلك، يمكنك التنقل في صف التقرير لرؤية كافة الأرصدة الخاصة بجميع وحدات شجرة التقارير.
31. أغلق **بيان الدخل - الافتراضي**.
32. أغلق **مصمم التقارير**.

## <a name="exercise-4-create-a-consolidated-report-using-an-organization-hierarchy"></a>التمرين 4: إنشاء تقرير مجمع باستخدام تدرج هرمي للمؤسسات
في هذا التمرين، ستقوم بتعديل تقرير افتراضي موجود. ستقوم بإضافة تدرج هرمي للمؤسسات في تعريف التقرير لإنتاج ميزانية عمومية وبيان دخل مجمع. وبمجرد اكتمال التحديثات، ستقوم بإنشاء التقرير المدمج واستكشاف التقرير باستخدام شجرة التقارير. سنبدأ من قائمة التقارير المالية.

1. انتقل إلى **التقارير المالية** ضمن الاستعلامات والتقارير في دفتر الأستاذ العام.
2. حدد الصف للتقرير المسمى **الميزانية العمومية وبيان الدخل جنبًا إلى جنب - الافتراضي**.
3. حدد **تحرير**. سيتم فتح **الميزانية العمومية وبيان الدخل جنبًا إلى جنب - الافتراضية** في تصميم التقارير.
4. حدد **ملف** &gt; **حفظ باسم** وقم بتسمية التقرير باسم **بيان الدخل والميزانية العمومية المجمعة جنبًا إلى جنب**.
5. قم بتغيير سنة الأساس إلى 2012.
6. انقر فوق سهم القائمة المنسدلة نوع الشجرة، وحدد **التدرجات الهرمية للمؤسسات**.
7. انقر فوق سهم القائمة المنسدلة الشجرة، وحدد **Contoso Holdings**.
8. احفظ التغييرات وأنشئ التقرير. إذا طُلب منك ذلك، فحدد كافة وحدات التقارير. بعد اكتمال عملية إنشاء التقرير وفتحه، يمكنك استكشاف التقرير.
9. حدد **خيارات التقرير**.
10. حدد **إضافة عامل تصفية بُعد** واختر **القسم**.
11. أدخل **022** في الحقل، وحدد **موافق**.
12. قم بإغلاق التقرير المصفى.
13. حدد القائمة المنسدلة **شجرة التقارير** لعرض وحدات التقارير. وبدلاً من ذلك، يمكنك التنقل في صف التقرير لرؤية كافة الأرصدة الخاصة بجميع وحدات شجرة التقارير.
14. أغلق **بيان الدخل والميزانية العمومية المجمعة جنبًا إلى جنب‬‏‫**.
15. أغلق **مصمم التقارير**.

## <a name="exercise-5-create-a-sidebyside-departmental-report"></a>التمرين 5: إنشاء تقرير الأقسام جنبًا إلى جنب
في هذا التمرين، ستقوم بإنشاء تقرير جديد. والتقرير عبارة عن بيان دخل الأقسام جنبًا إلى جنب. ستستخدم تعريف الصف الحالي، ولكن تُنشئ تعريف تقرير جديدًا وتعريف عمود جديدًا يستخدم عوامل تصفية الأبعاد. سنبدأ من قائمة التقارير المالية.

1. انتقل إلى **التقارير المالية** ضمن الاستعلامات والتقارير في دفتر الأستاذ العام.
2. حدد **جديد**. سيتم فتح مصمم التقارير مع فتح تعريف تقارير فارغ. وستؤدي أول مهمة لك إلى إنشاء تعريف العمود.
3. قم بإنشاء تعريف عمود جديد عن طريق النقر فوق **ملف**، ثم **جديد**، ثم **تعريف العمود**.
4. في **العمود أ**، حدد **DESC** لنوع العمود.
5. في **العمود ب**، حدد **FD** لنوع العمود.
6. انقر نقراً مزدوجاً في حقل **عامل تصفية البُعد**.
7. في إطار **البُعد**، انقر نقراً مزدوجاً فوق عمود **القسم**.
8. في القسم الفردي أو مجموعة أقسام في مربع الحوار، انقر فوق **علامة حذف** للحقل **من** لعرض قائمة بالأقسام.
9. حدد القسم **022**، و**المبيعات والتسويق**، ثم انقر فوق**موافق**.
10. كرر الخطوات من 5 إلى 8 للأقسام من 23 إلى 25.
11. وفي صف **الرأس 2** لكل عمود FD، اكتب أوصاف الأقسام التالية:

    - العمود ب - التسويق والمبيعات
    - العمود ج - العمليات
    - العمود د - المالية
    - العمود ه - تقنية المعلومات

12. احفظ تعريف العمود كأقسام جنبًا إلى جنب. ولأننا نستخدم تعريف صف موجودًا، يمكن تعديل تعريف التقرير الآن لاستخدام تعريف العمود الذي تم إنشاؤه حديثًا وتعريف الصف الموجود.
13. في القائمة **إطار**، حدد **تعريف التقرير الجديد** لفتح تعريف التقرير.
14. حدد **بيان الدخل – الافتراضي** باعتباره تعريف الصف و**الأقسام جنبًا إلى جنب** باعتباره تعريف العمود.
15. احفظ تعريف التقرير كـ **بيان دخل الأقسام جنبًا إلى جنب**.
16. قم قم بتغيير سنة الأساس إلى **2012**.
17. قم بتغيير مستوى التفاصيل إلى **المالية والحساب والحركة**.
18. **احفظ** التغييرات التي أجريتها وقم **بالإنشاء**. وبمجرد اكتمال عملية إنشاء التقرير وفتحه، يمكنك استكشاف التقرير.

## <a name="additional-resources"></a>الموارد الإضافية
[التقارير المالية](../../../finance/general-ledger/financial-reporting-getting-started.md)

[عرض التقارير المالية](../../../finance/general-ledger/view-financial-reports.md)

[مدونة التقارير المالية في Dynamics](http://blogs.msdn.com/b/dynamics_financial_reporting/)