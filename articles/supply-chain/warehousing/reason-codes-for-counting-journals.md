---
title: "أكواد الأسباب لجرد المخزون"
description: "يصف هذا الموضوع كيفية إعداد وتطبيق أكواد الأسباب لمهام الجرد."
author: Mirzaab
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCountingReasonCodePolicy
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: fe01425fa236655731e6e0723f3a1e57c05035cc
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---

# <a name="reason-codes-for-inventory-counting"></a>أكواد الأسباب لجرد المخزون

[!include [banner](../includes/banner.md)]

تتيح لك أكواد الأسباب تحليل نتائج عملية الجرد وأي تناقضات تحدث أثناء العملية. يمكنك تحديد سبب القيام بالجرد، مثل بالتة مكسورة أو تعديل مخزون يستند إلى نماذج المخزون.

## <a name="recommendation"></a>التوصيات

قبل إعداد النظام، نوصي بأن تقوم بتحديد استراتيجية للعمل مع أكواد الأسباب. على سبيل المثال، حاول الإجابة عن الأسئلة التالية:

- هل يجب أن تكون أكواد الأسباب إلزامية في المستودعات؟
- هل يجب أن تكون أكواد الأسباب إلزامية أو اختيارية في بعض الأصناف؟
- كم عدد أكواد الأسباب التي تتطلبها؟
- كيف يجب على مستخدمي الماسحات الضوئية للأكواد الشريطية استخدام أكواد الأسباب؟ هل يجب أن تكون أكواد الأسباب محددة مسبقًا أو إلزامية أو غير قابلة للتحرير؟
- هل يتطلب العاملون في المستودع سلوك كود سبب مختلفًا في الماسحات الضوئية للأجهزة المحمولة؟ إذا كانت الإجابة بنعم، يمكنك إنشاء مزيد من أصناف القائمة وتعيينها إلى أشخاص مختلفين.

## <a name="where-reason-codes-apply"></a>مواضع تطبيق أكواد الأسباب

يمكنك إنشاء العديد من سياسات أكواد الأسباب، ويمكن لكل سياسة كود سبب أن تشتمل على سياستي أكواد أسباب للجرد. يمكن استخدام سياسات أكواد أسباب الجرد على مستوى المستودع أو مستوى الصنف.

## <a name="set-up-reason-code-policies"></a>إعداد سياسات أكواد الأسباب

1. حدد **إدارة المخزون**\>**الإعداد**\>**المخزون**\>**سياسات أكواد أسباب الجرد**، وقم بإنشاء سياسة كود سبب جديدة.
2. في حقل **نوع كود سبب الجرد**، حدد إما **إلزامي** أو **اختياري** لتحديد ما إذا كان يجب أن يكون تحديد كود سبب خيارًا اختياريًا أو إلزاميًا في أحد دفاتر يومية الجرد التالية:

    - الجرد الدوري (الجهاز المحمول)
    - الجرد الفوري (الجهاز المحمول)
    - جرد الحدود (الجهاز المحمول)
    - التسوية الواردة (الجهاز المحمول)
    - التسوية الصادرة (الجهاز المحمول)
    - دفتر يومية الجرد (عميل غني)

يمكنك أيضًا إعداد أكواد الأسباب للمستودعات الفردية وللمنتجات. يمكن لإعداد كود السبب للمنتجات تجاهل الإعداد للمستودعات.

## <a name="mandatory-reason-codes"></a>أكواد الأسباب الإلزامية

في حالة تعيين معلمة **إلزامية** في التكوين الخاص بأكواد الأسباب للمستودعات أو للأصناف، لا يمكن إكمال دفتر يومية الجرد وإغلاقه حتى يتوفر كود سبب.

### <a name="set-up-reason-codes-for-warehouses"></a>إعداد أكواد الأسباب للمستودعات

1. حدد **إدارة المخزون** \> **الإعداد** \> **تصنيف المخزون** \> **المستودعات**.
2. في علامة التبويب **المستودع**، في حقل **سياسة كود سبب الجرد**، حدد أحد الخيارات التالية:

    - **فارغ** - يتم استخدام المعلمة التي يتم إعدادها للصنف لتحديد ما إذا كانت دفاتر يومية الجرد إلزامية للمنتج.
    - **إلزامي** - كود سبب مطلوب دائمًا في دفاتر يومية الجرد للمستودع.
    - **اختياري** - كود سبب غير مطلوب دائمًا في دفاتر يومية الجرد للمستودع.

### <a name="set-up-reason-codes-for-products"></a>إعداد أكواد الأسباب للمنتجات

1. حدد **إدارة معلومات المنتج** \> **المنتجات** \> **المنتجات الصادرة**.
2. في علامة التبويب **المنتج**، حدد **سياسة كود سبب الجرد**، ثم حدد أحد الخيارات التالية:

    - **فارغ** - يتم استخدام المعلمة التي يتم إعدادها للمستودع لتحديد ما إذا كانت دفاتر يومية الجرد إلزامية للمنتج.
    - **إلزامي** - كود سبب مطلوب دائمًا في دفاتر يومية الجرد للمنتج. يتجاوز هذا الإعداد أي إعداد كود سبب عند مستوى المستودع.
    - **اختياري** - كود سبب غير مطلوب دائمًا في دفاتر يومية الجرد للمنتج. يتجاوز هذا الإعداد أي إعداد كود سبب عند مستوى المستودع.

### <a name="use-reason-codes-in-counting-journals"></a>استخدم أكواد الأسباب في دفاتر يومية الجرد

في دفتر يومية جرد، يمكنك إضافة أكواد الأسباب لعدد الأنواع التالية:

- جرد دوري
- جرد فوري
- جرد الحدود
- تسوية واردة
- تسوية صادرة

تتم إضافة أكواد الأسباب إلى بنود دفتر اليومية في دفاتر يومية الجرد من نوع **دفتر يومية الجرد**.

1. حدد **إدارة المخزون** \> **إدخالات دفتر اليومية** \> **جرد الأصناف** \> **الجرد**.
2. في تفاصيل بنود دفتر يومية الجرد، في حقل **كود سبب الجرد**، حدد أحد الخيارات.

### <a name="view-the-counting-history-as-its-recorded-by-reason-codes"></a>عرض محفوظات الجرد كما هي مسجلة بواسطة أكواد الأسباب

- حدد **إدارة المخزون**\>**الاستعلامات والتقارير**\>**محفوظات الجرد**، ثم في حقل **كود سبب الجرد**، اعرض محفوظات الجرد التي تم تسجيلها من خلال كود سبب.

### <a name="use-a-reason-code-for-a-quantity-adjustment"></a>استخدام كود سبب لتسوية كمية

1. في صفحة **المخزون الفعلى**، حدد **تسوية كمية**. يمكنك فتح صفحة **المخزون الفعلى** بعدة طرق. على سبيل المثال، حدد **إدارة المخزون** \> **الاستعلامات والتقارير** \> **المخزون الفعلي**.
2. حدد **تسوية كمية**، ثم في حقل **كود سبب الجرد**، حدد كود سبب.

### <a name="configure-reason-codes-for-mobile-device-menu-items"></a>تكوين أكواد الأسباب لعناصر قائمة الأجهزة المحمولة

يمكنك تكوين أكواد الأسباب لأي نوع من الجرد على عنصر قائمة جهاز محمول. يتضمن التكوين الخاص بعنصر قائمة الجهاز المحمول المعلومات التالية:

- ما إذا كان يتم إظهار كود السبب لعامل الجهاز المحمول خلال عملية الجرد.
- كود السبب الافتراضي الذي يظهر في عنصر قائمة جهاز محمول.
- ما إذا كان بإمكان المستخدم تحرير كود السبب.

### <a name="set-up-reason-codes-on-a-mobile-device"></a>إعداد أكواد الأسباب على جهاز محمول

1. حدد **إدارة المستودعات** \> **الإعداد** \> **الجهاز المحمول** \> **عناصر الجهاز المحمول**.
2. في علامة التبويب **الجرد الدوري**، حدد **جرد دوري**.
3. في حقل **كود السبب الافتراضي للجرد**، قم بتعيين كود السبب الافتراضي الذي يجب أن يتم تسجيله عندما يتم إجراء الجرد باستخدام عنصر قائمة جهاز محمول.
4. في حقل **عرض كود سبب الجرد**، حدد **بند** لإظهار كود السبب بعد أن يتم تسجيل كل نسبة فرق. بدلاً من ذلك، حدد **إخفاء** إذا كان يجب إلا يتم إظهار كود السبب.
5. قم بتعيين خيار **تحرير كود سبب الجرد** إلى إما **نعم** أو **لا**. إذا قمت بتعيين هذا الخيار **نعم**، يستطيع العامل تحرير كود السبب عندما يظهر على الجهاز المحمول خلال عملية الجرد.

> [!NOTE]
> يمكن تمكين الزر **جرد دوري**على أي عنصر قائمة جهاز محمول حيث يمكن القيام بالجرد. يتضمن المثال عناصر القائمة لعمليات الجرد الفوري والعمل الموجه من قِبل المستخدم والعمل الموجه بواسطة النظام.

## <a name="cycle-count-approvals"></a>الموافقات على الجرد الدوري

قبل أن تتم الموافقة على عملية جرد، يمكن للمستخدم تغيير كود السبب المرتبط بالحساب. عندما تتم الموافقة على الحساب، يتم إدخال كود السبب في بنود دفتر يومية الجرد.

### <a name="modify-cycle-count-approvals"></a>تعديل الموافقات على الجرد الدوري

1. حدد **إدارة المستودعات**\>**جرد دوري**\>**مراجعة عمل الجرد الدوري المعلق**.
2. حدد **جرد دوري**، ثم في حقل **كود السبب**، حدد كود سبب جديدًا.

### <a name="modify-the-mobile-device-menu-item-for-adjustment-in-and-adjustment-out"></a>تعديل عنصر قائمة الجهاز المحمول للتسوية الواردة والتسوية الصادرة

1. حدد **إدارة المستودعات**\>**الإعداد**\>**الجهاز المحمول**\>**عناصر قائمة الجهاز المحمول**، ثم قم بتحديد **التسوية الواردة والصادرة**.
2. قم بتعيين الخيار **استخدام العمل الموجود** إلى **لا**.
3. في حقل **عملية إنشاء العمل**، حدد **التسوية الواردة**.

ستتم إضافة الحقول التالية إلى عنصر قائمة الجهاز المحمول عند تحديد **التسوية الواردة** أو **التسوية الصادرة** أثناء عملية إنشاء العمل:

- كود سبب الجرد الافتراضي
- عرض كود سبب الجرد
- تحرير كود سبب الجرد
