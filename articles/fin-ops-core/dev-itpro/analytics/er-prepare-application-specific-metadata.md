---
title: إعداد بيانات تعريف خاصة بالتطبيق لـ RCS وER
description: يشرح هذا الموضوع كيفية إعداد بيانات التعريف الخاصة بالتطبيق لـ Regulatory configuration service (RCS) والتقارير الإلكترونية (ER).
author: NickSelin
manager: AnnBe
ms.date: 04/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: f15b78d3ed5b4df47540f9f89cc69c0b535a7241
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680184"
---
# <a name="prepare-application-specific-metadata-for-rcs-and-er"></a>إعداد بيانات تعريف خاصة بالتطبيق لـ RCS وER

[!include[banner](../includes/banner.md)]

يقدم لك هذا الموضوع أمثلة على المهام التالية:

- [تحضير بيانات تعريف التطبيق التي يمكن استخدامها في RCS](#prepare-application-metadata-that-can-be-used-in-rcs)
- [الوصول إلى بيانات تعريف التطبيق باستخدام تكوين ER](#access-application-metadata-by-using-an-er-configuration)
- [الوصول إلى بيانات تعريف التطبيق باستخدام التطبيقات المتصلة](#access-application-metadata-by-using-connected-applications)

## <a name="prepare-application-metadata-that-can-be-used-in-rcs"></a>تحضير بيانات تعريف التطبيق التي يمكن استخدامها في RCS

يوضح الإجراء التالي كيفية قيام مستخدم يؤدي دور **مسؤول النظام** أو **مطور التقارير الإلكتروني** بإنشاء تكوين التقارير الإلكترونية الذي يحتوي على بيانات تعريف للتطبيق، ويتم استخدامه لتصميم تكوينات تعيين نموذج التقارير الإلكترونية في Regulatory configuration service (RCS). يتم استخدام مثال تكوين تعيين لنموذج (ER) الذي تم إنشاؤه في هذا المثال للوصول إلى حركات التجارية الخارجية.

في هذا المثال، ستحتاج إلى استخدام RCS لتصميم حل التقارير الإلكترونية الذي سيتم استخدامه لإنشاء مستندات إلكترونية تحتوي على معلومات من مجال أعمال التجارة الخارجية. لتحديد التعيين بين نموذج بيانات ER ومصادر البيانات المطلوبة، يجب أن يكون لديك حق الوصول إلى بيانات تعريف التطبيق في RCS. بالتالي، كجزء من عملية تصميم حل ER، يجب تكوين بيانات تعريف ER جديدة تحتوي على جميع بيانات التعريف المطلوبة حاليًا من أجل إنشاء تقارير ER لمجال الأعمال المحدد.

> [!NOTE]
> في هذا المثال، ستقوم بإنشاء تكوين لشركة نموذجية، .Litware, Inc ويمكن تنفيذ هذه الخطوات في أي شركة.

1. انتقل إلى **إدارة المؤسسة \> مساحات العمل \> إعداد التقارير الإلكترونية**.
2. تأكد من وجود موفر التكوين للشركة النموذجية "Litware, Inc." ومن وضع علامة عليه كـ **نشط**. إذا لم تشاهد موفر التكوين هذا، فيجب أولاً إكمال الإجراء [إنشاء موفري التكوين ووضع علامة عليهم على أنهم نشيطون‬](tasks/er-configuration-provider-mark-it-active-2016-11.md). 
3. حدد **تكوينات بيانات التعريف**.
4. حدد **إنشاء التكوين**.
5. في مربع الحوار المنسدل، في الحقل **الاسم**، ادخل اسمًا. بالنسبة لهذا المثال، أدخل **بيانات تعريف التجارة الخارجية**.
6. حدد **إنشاء التكوين**.
7. حدد **المصمم**.
8. حدد **إضافة**.

    > [!NOTE]
    > يمكنك تحديد كافة بيانات التعريف إما للتطبيق بالكامل أو للنماذج أو الوحدات النمطية المحددة. وفي كلتا الحالتين، يجب مراعاة أنه ستتم إضافة بيانات التعريف التالية تلقائيا: جداول السجلات والتعدادات وأنواع البيانات الملحقة (EDT). عندما تكون هناك أنواع إضافية من بيانات التعريف مطلوبة، فيجب إضافتها يدويًا.

    يجب إضافة بعض بيانات التعريف المرتبطة بحركات التجارية الخارجية وتحديد عناصر بيانات التعريف يدويًا.

9. حدد **إضافة مصدر بيانات \>** سجلات جدول.
10. قم بالتصفية حسب قيمة **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي** في حقل **الاسم**.
11. حدد سجل جدول **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي**.
12. حدد **موافق**.

    يجب إضافة معلومات بيانات التعريف الخاصة بجدول سجلات نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.

13. في الشجرة، حدد **سجلات جدول نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\> \>العلاقات\> IntrastatCommodity (سجلات جدول EcoResCategory)**.
14. حدد **إضافة بيانات التعريف**.

    > [!NOTE]
    > يجب إضافة بيانات التعريف حول العلاقات المطلوبة لجدول السجلات المحدد يدويا.

15. حدد **إضافة مصدر البيانات**.
16. حدد **التعداد**.
17. قم بالتصفية حسب القيمة **IntrastatDirection** في حقل **الاسم**.
18. حدد سجل تعداد **IntrastatDirection**.
19. حدد **موافق**.
20. حدد **حفظ**.
21. قم بإغلاق الصفحة.
22. أكمل الإصدار التمهيدي من تكوين بيانات التعريف:

    1. حدد **حالة التغيير \> مكتمل**.
    2. حدد **موافق**.
    3. حدد الإصدار المكتمل 1.

23. صدّر النسخة المكتملة من تكوين بيانات التعريف من التطبيق كملف XML:

    1. حدد **تبادل \> تصدير كملف XML**.
    2. حدد **موافق**.

يتم حفظ تكوين بيانات تعريف ER الذي قمت بإنشائه كملف **Foreign trade metadata.xml**. يمكنك الآن استيراده إلى RCS، بحيث يمكن استخدامه كمصدر لبيانات التعريف الخاصة بمجال أعمال التجارية الخارجية. استنادا إلى هذه المعلومات، يمكنك تحديد التعيين بين بيانات تعريف التطبيق ونموذج بيانات ER.

## <a name="access-application-metadata-by-using-an-er-configuration"></a>الوصول إلى بيانات تعريف التطبيق باستخدام تكوين ER

يوضح الإجراء التالي كيف يمكن لمستخدم RCS الذي يتمتع بدور **مسؤول النظام** أو **مطور التقارير الإلكترونية** تصميم تعيين نموذج ER جديد باستخدام بيانات التعريف من التطبيق. سيتم الوصول إلى بيانات تعريف التطبيق باستخدام تكوين بيانات تعريف ER الذي يحتوي على عينة من مجموعة بيانات التعريف للوصول إلى حركات التجارة الخارجية.

قبل إكمال هذا الإجراء، يجب أن تستكمل أولا الإجراءات التالية:

- [إنشاء موفري التكوين ووضع علامة نشط عليهم](tasks/er-configuration-provider-mark-it-active-2016-11.md)
- [تحضير بيانات تعريف التطبيق التي يمكن استخدامها في RCS](#prepare-application-metadata-that-can-be-used-in-rcs)

1. انتقل إلى **كافة مساحات العمل \> التقارير الإلكترونية**.
2. تأكد من وجود موفر التكوين للشركة النموذجية "Litware, Inc." ومن وضع علامة عليه كـ **نشط**. إذا لم تشاهد موفر التكوين هذا، فيجب أولاً إكمال الإجراء [إنشاء موفري التكوين ووضع علامة عليهم على أنهم نشيطون‬](tasks/er-configuration-provider-mark-it-active-2016-11.md). 
3. استورد تكوين بيانات تعريف التقارير الإلكترونية الذي يحتوي على بيانات التعريف للتطبيق، والذي تم تكوينه لإنشاء مستندات إلكترونية لمجال أعمال التجارة الخارجية. لقد قمت بإنشاء تكوين بيانات تعريف ER هذا وتصديره كملف XML في إجراء [تحضير بيانات تعريف التطبيق التي يمكن استخدامها في RCS](#prepare-application-metadata-that-can-be-used-in-rcs) سابقًا في هذا الموضوع.

    1. حدد **تكوينات بيانات التعريف**.
    2. حدد **تبادل**.
    3. حدد **تحميل من ملف XML**.
    4. استعرض لتحديد ملف **Foreign trade metadata.xml**.
    5. حدد **موافق**.
    6. قم بإغلاق الصفحة.

4. إنشاء تكوين نموذج البيانات:

    1. حدد **تكوينات إعداد التقارير‬**.
    2. حدد **إنشاء التكوين**.
    3. في مربع الحوار المنسدل، في الحقل **الاسم**، أدخل **نموذج التجارة الخارجية**.
    4. حدد **إنشاء التكوين**.
    5. حدد **المصمم**.
    6. حدد **جديد** لفتح مربع حوار الإسقاط‬.

        1. في حقل **الاسم**، اكتب **الجذر‬**.
        2. حدد **إضافة**.
    
    7. حدد **جديد** لفتح مربع حوار الإسقاط‬.

        1. في حقل **الاسم**، اكتب **الحركة**.
        2. في حقل **نوع الصنف**، حدد **قائمة سجلات**.
        3. حدد **إضافة**.
 
    8. حدد **جديد** لفتح مربع حوار الإسقاط‬.

        1. في حقل **الاسم**، اكتب **كود السلعة**.
        2. في الحقل **نوع الصنف**، حدد **سلسلة**.
        3. حدد **إضافة**.

    9. حدد **جديد** لفتح مربع حوار الإسقاط‬.

        1. في حقل الاسم، اكتب **المبلغ المفوتر**.
        2. في الحقل **نوع الصنف**، حدد **حقيقي**.
        3. حدد **إضافة**.

    10. حدد **جديد** لفتح مربع حوار الإسقاط‬.

        1. في حقل **الاسم**، اكتب **التاريخ**.
        2. في الحقل **نوع الصنف**، حدد **تاريخ**.
        3. حدد **إضافة**.
 
    11. حدد **إضافة \> مرجع الجذر**.
    12. حدد **موافق**.
    13. حدد **حفظ**.
    14. قم بإغلاق الصفحة.
    15. حدد **حالة التغيير \> مكتمل**.
    16. حدد **موافق**.

5. إنشاء تكوين لتعيين نموذج:

    1. حدد **إنشاء التكوين**.
    2. في مربع الحوار المنسدل، في لحقل **جديد**، أدخل **تعيين نموذج استنادًا إلى نموذج بيانات التجارة الخارجية**.
    3. في حقل **الاسم**، اكتب **تعيين تجارة خارجية**.
    4. حدد **إنشاء التكوين**.
    5. في علامة التبويب السريعة **المتطلبات الأساسية**، حدد **تحرير**.
    6. حدد **جديد**.
    7. في حقل **نوع مكون المتطلبات الأساسية**، حدد **التكوين.**
    8. حدد تكوين **بيانات تعريف التجارة الخارجية**.
    9. حدد **حفظ**. لاحظ أنه تتم إضافة المرجع إلى الإصدار 1 من تكوين **بيانات تعريف التجارة الخارجية**. سيتم توفير بيانات تعريف التطبيق من هذا التكوين بينما سيتم تصميم تعيين النموذج.
    10. قم بإغلاق الصفحة.
    11. حدد **المصمم**.
    12. حدد **المصمم**.
    13. في الشجرة، حدد **Dynamics 365 for Operations \> سجلات الجدول**.
    14. حدد **إضافة جذر**.
    15. في الحقل **الاسم**، أدخل **‏‫نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬**.
    16. حدد سجلات جدول **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي**.
    17. حدد **موافق**.

        > [!NOTE]
        > تم عرض الجدولين فقط نظرًا لأنه تمت إضافة جدولين فقط إلى مجموعة بيانات التعريف المستخدمة حاليًا.

    18. حدد **ربط**.
    19. في الشجرة، حدد **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي \> AmountMST**.
    20. في الشجرة، حدد **الحركة = نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي \> المبلغ المفوتر**.
    21. حدد **ربط**.
    22. في الشجرة، حدد **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\>تاريخ الحركة**.
    23. في الشجرة، حدد **الحركة = نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\>التاريخ**.
    24. حدد **ربط**.
    25. في الشجرة، حدد **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي\> \>العلاقات \> IntrastatCommodity\> الكود**.
    26. في الشجرة، حدد **الحركة = نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي \> كود السلعة**.
    27. حدد **ربط**.
    28. حدد **التحقق من الصحة**.

        > [!NOTE]
        > بعد اكتمال التحقق من الصحة، تكون نجحت في ربط عناصر نموذج البيانات بعناصر مصادر البيانات التي تم وصفها باستخدام تفاصيل بيانات تعريف التطبيق من تكوين بيانات تعريف ER المشار إليها.

    29. حدد **حفظ**.

يمكنك توسيع مجموعة بيانات التعريف الموجودة في التطبيق، بحسب الحاجة. ويمكنك بعد ذلك تصدير الإصدار الجديد المكتمل من تكوين بيانات تعريف التقارير الإلكترونية، واستيراده إلى RCS وتحديث المتطلبات الأساسية لتكوين تعيين النموذج المكون للإشارة إصدار جديد من تكوين بيانات التعريف المستوردة.

> [!NOTE]
> تعتبر هذه الطريقة للحصول على معلومات حول بيانات تعريف التطبيق الوحيدة المتوفرة للتطبيقات المنشورة محليًا (أي، عند استخدام نموذج نشر بيانات العمل المحلية \[LBD\] أو في الموقع المحلي المستخدم للتطبيق).

## <a name="access-application-metadata-by-using-connected-applications"></a>الوصول إلى بيانات تعريف التطبيق باستخدام التطبيقات المتصلة

يوضح الإجراء التالي كيف يمكن لمستخدم RCS الذي يؤدي بدور **مسؤول النظام** أو **مطور التقارير الإلكترونية** تصميم تعيين نموذج تقارير إلكترونية جديد باستخدام بيانات تعريف التطبيق. سيتم الوصول إلى بيانات تعريف التطبيق عبر الإنترنت باستخدام التطبيق المتصل بـ RCS. سيتم تكوين مثال لتعيين نموذج ER للوصول إلى حركات التجارة الخارجية.

لإكمال هذا الإجراء، يجب أولاً إكمال الإجراء [‏‫إنشاء موفري التكوين ووضع علامة عليهم على أنهم نشيطون](tasks/er-configuration-provider-mark-it-active-2016-11.md) في RCS. في حالة عدم إكمال الإجراء [الوصول إلى بيانات تعريف التطبيق باستخدام تكوين ER‬](#access-application-metadata-by-using-an-er-configuration) الموضح سابقًا في هذا الموضوع، اذهب إلى  صفحة [إرشادات مهام إعداد التقارير لـ Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) لتنزيل ملفات تكوين ER التالية مقدمًا وحفظها محليًا: **Foreign trade metadata.xml** و **Foreign trade model.xml** و **Foreign trade mapping.xml**.


### <a name="get-required-er-configurations"></a>الحصول على تكوينات ER المطلوبة

إذا أكملت بالفعل الإجراء [‏‫الوصول إلى بيانات تعريف التطبيق باستخدام تكوين ER](#access-application-metadata-by-using-an-er-configuration) الذي تم توضيحه سابقًا في هذا الموضوع، فلديك بالفعل جميع تكوينات ER المطلوبة (بيانات تعريف التجارة الخارجية والنموذج وتكوينات التعيين) في مثيل RCS الحالي. في تلك الحالة، يمكنك تخطي هذا الإجراء.

1. انتقل إلى **كافة مساحات العمل \> التقارير الإلكترونية**.
2. حدد **تكوينات إعداد التقارير‬**.
3. حمّل ملفات تكوين **Foreign trade metadata.xml** و **Foreign trade model.xml** و **Foreign trade mapping.xml** مع تكرار سلسلة الخطوات التالية لكل منها:

    1. حدد **تبادل**.
    2. حدد **تحميل من ملف XML**.
    3. حدد **استعراض**، وحدد ملفًا.
    4. حدد **موافق**.

### <a name="register-the-connection-with-the-application"></a>تسجيل الاتصال مع التطبيق

1. انتقل إلى **كافة مساحات العمل \> التقارير الإلكترونية**.
2. حدد **التطبيقات المتصلة**.
3. تأكد من أن التطبيق الذي تم تكوينه يستند إلى Microsoft Azureوأنه يمكن لمستخدمي RCS الوصول إليه بشكل عام. يجب أن يكون لدى مستخدم RCS الحالي إمكانية الوصول إلى التطبيق المكون وتسجيله كمستخدم لهذا التطبيق ويشغل دورًا يعطيه امتيازات للوصول إلى بيانات تعريف التطبيق.
4. حدد **جديد**.
5. في حقل **الاسم**، أدخل **MyConnectedApp** كاسم التطبيق المتصل.
6. في حقل **التطبيق**، حدد عنوان URL للتطبيق.
7. في حقل **المستأجر**، حدد موفر للتطبيق.
8. حدد **حفظ**. 
9. عند التحقق من الاتصال بالتطبيق الذي تم تكوينه، في صفحة **الاتصال بالتطبيق البعيد** حدد ارتباط **حدد هنا للاتصال بالتطبيق البعيد المحدد**. 
10. حدد **التحقق من الاتصال** للتحقق من صحة الوصول إلى التطبيق الذي تم تكوينه.
11. حدد **إغلاق**.

بعد استكمال هذا الإجراء ونجاح التحقق من صحة الاتصال، سيتم تحديث تفاصيل الإصدار والمستأجر للتطبيق الذي سيتم تكوينه في الشبكة الحالية.

### <a name="review-the-existing-model-mapping-configuration"></a>مراجعة التكوين لتعيين نموذج موجود

1. انتقل إلى **كافة مساحات العمل \> التقارير الإلكترونية**.
2. حدد **تكوينات إعداد التقارير‬**.
3. في الشجرة، حدد **نموذج التجارة الخارجية \> تعيين التجارة الخارجية**.
4. حدد علامة التبويب السريعة **المتطلبات الأساسية**.

    > [!NOTE]
    > حاليًا، يشير هذا التعيين إلى تكوين بيانات التعريف. سيتم توفير بيانات تعريف التطبيق من هذا التكوين بينما سيتم تصميم تعيين هذا النموذج.

4. حدد **المصمم**.
5. حدد **المصمم**.
6. في الشجرة، حدد **Dynamics 365 for Operations \> سجلات الجدول**.
7. حدد **إضافة جذر**.
8. في الحقل **الجدول**، أدخل قيمة أو حددها.

    > [!NOTE]
    > حاليًا، يشير هذا التعيين إلى تكوين بيانات التعريف. سيتم توفير بيانات تعريف التطبيق من هذا التكوين بينما سيتم تصميم تعيين هذا النموذج.

9. حدد **إلغاء الأمر**.

### <a name="assign-the-connected-application-to-a-model-mapping"></a>تخصيص تطبيق متصل لتعيين النموذج

1. حدد **تحرير**.
2. في **حقل التطبيق المتصل**، حدد تطبيق **MyConnectedApp**.

    > [!NOTE]
    > يشير هذا التعيين إلى بيانات التعريف للتطبيق المتصل المحدد. إذا أشار نفس التعيين إلى تكوين بيانات التعريف والتطبيق المتصل في نفس الوقت، سيتم استخدام بيانات التعريف الخاصة بالتطبيق المتصل.

3. حدد **المصمم**.
4. حدد **المصمم**.
5. في الشجرة، حدد **Dynamics 365 for Operations \> سجلات الجدول**.
6. حدد **إضافة جذر**.
7. في الحقل **الجدول**، أدخل قيمة أو حددها.

    > [!NOTE]
    > في هذه النقطة، تم عرض أكثر من جدولين للتطبيق، لأن هذا التعيين يستخدم كافة بيانات التعريف للتطبيق المتصل التي تم تعيينها له.

8. حدد **إلغاء الأمر**.
9. حدد **التحقق من الصحة**.

لقد قمنا الآن بربط عناصر نموذج البيانات مع عناصر مصادر البيانات التي تم وصفها باستخدام تفاصيل بيانات تعريف التطبيق المتصل التي تم تخصيصها لهذا التعيين.

عندما يلزم تقييم تعيين هذا النموذج باستخدام بيانات التعريف الخاصة بتطبيق من إصدار مختلف، قم بتسجيل تطبيق متصل آخر، قم تخصيصه إلى تعيين النموذج هذا، وتحقق منه مقابل بيانات التعريف الجديدة.

## <a name="additional-resources"></a>الموارد الإضافية

بدلا من ذلك، يمكنك تشغيل دليل المهمة **تحضير بيانات تعريف التطبيق التي يمكن استخدامها في RCS** في التطبيق بالإضافة إلى دلائل مهام **الوصول إلى بيانات تعريف التطبيق باستخدام تكوين التقارير الإلكترونية** و **الوصول إلى بيانات تعريف التطبيق باستخدام التطبيقات المتصلة**. يمكن تحميل دلائل المهام هذه من صفحة [دلائل مهام التقارير الإلكترونية لـ Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]