---
title: "نظرة عامة على الوصول"
description: "يوفر هذا الموضوع معلومات حول ميزة النظرة العامة على الوصول. تعتبر الصفحة &quot;نظرة عامة على الوصول&quot; جزءًا من هذه الميزة وتوفر نظرة عامة على كافة العناصر التي من المتوقع أن تصل كأصناف واردة."
author: YuyuScheller
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WMSArrivalOverview, WMSArrivalOverviewProfile, WMSJournalTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: c1b6077ac32b6a7c30f9d9c9d0fa0eb93cf63bf6
ms.contentlocale: ar-sa
ms.lasthandoff: 04/25/2017


---

# <a name="arrival-overview"></a>نظرة عامة على الوصول

[!include[banner](../includes/banner.md)]


يوفر هذا الموضوع معلومات حول ميزة النظرة العامة على الوصول. تعتبر الصفحة "نظرة عامة على الوصول" جزءًا من هذه الميزة وتوفر نظرة عامة على كافة العناصر التي من المتوقع أن تصل كأصناف واردة.

توفر الصفحة **نظرة عامة على الوصول** نظرة عامة على جميع الأصناف الواردة المتوقعة. وتُظهر أيضًا عمليات الوصول التي يمكن تهيئتها استنادًا إلى النظرة العامة. يركز هذا الموضوع على عملية الاستلام.

## <a name="business-scenario"></a>سيناريو العمل
خذ في الاعتبار السيناريو التالي في العمليات الواردة. 

[![سيناريو العمل](./media/arrival-overview-scenario.png)](./media/arrival-overview-scenario.png) 

سامي، موظف الاستقبال، يريد معرفة الأصناف التي من المتوقع استلامها في اليوم الحالي. في الصفحة **نظرة عامة على الوصول**، يستطيع سامي الحصول على نظرة عامة على المهام الحالية، وتقديرًا أوليًا للكميات، والحجم والوزن، ومختلف أنواع الأوامر وغير ذلك. في وقت لاحق، تصل عملية تسليم تصل إلى أحد الأرصفة الداخلية، ويتلقى سامي قائمة بالتسليم. في الصفحة **نظرة عامة على الوصول**، يستطيع سامي تنفيذ المهام التالية:

-   تحديد أمر الاستلام المطابق، وتسجيل عملية الاستلام على أنها **قيد التقدم**. يتم تلقائيًا إنشاء البنود المطلوبة للتسجيل، ويمكن مراقبة الإيصال، على الرغم من عدم ترحيل الحركات بعد على أنها **مسجلة**.
-   الوصول إلى مرجع دفتر يومية الوصول المناسب (أي، دفتر يومية **وصول الصنف** أو دفتر يومية **مدخلات الإنتاج**)، وتحديد دفاتر اليومية الجاهزة لتحديث استلام المنتج.

## <a name="arrival-overview-page"></a>صفحة النظرة العامة على الوصول
لفتح الصفحة **نظرة عامة على الوصول**، انقر فوق **إدارة المخزون** &gt; **الأوامر الواردة** &gt; **نظرة عامة على الوصول**. يمكنك عرض قائمة بالأوامر التي من المتوقع أن يتم استلامها. تم تقسيم النظرة العامة إلى رأس وبنود. وتم تجميع معلومات الرأس حسب نوع الأمر وتاريخ الاستلام المتوقع ووجهة التسليم. عندما يتم تحديد بند رأس للوصول، يتم تحديد كافة بنود التفاصيل المتعلقة بمرجع الإيصال للوصول في جزء تفاصيل البند من الصفحة. عند ترحيل كافة بنود دفتر اليومية المرتبطة، لا تظهر هذه المعلومات.

### <a name="arrival-overview-profiles"></a>ملفات تعريف النظرة العامة على الوصول

توفر الصفحة **نظرة عامة على الوصول** نظرة عامة على الأصناف المتوقع وصولها وتاريخ وصولها المتوقع. كجزء من عملية الوصول، يمكن استخدام عدة مجموعات من الإعدادات الشخصية. يمكن للمستخدمين الفرديين تعريف إعداداتهم الشخصية في صفحة **ملفات تعريف النظرة العامة على الوصول**.

### <a name="set-up-item-arrival"></a>إعداد وصول الصنف

يرغب سامي، في هذا المثال، في إعداد كمبيوتر جديد في موقع سيتم استخدامه لاستلام البضائع المنتهية التي تأتي من الإنتاج في الموقع 1. في الصفحة **ملفات تعريف النظرة العامة على الوصول**، يقوم سامي بإنشاء إعداد جديد يسمى **إنتاج الموقع 1** ويحدد الإعدادات التالية.

1.  على علامة التبويب السريعة **خيارات الوصول**، في مجموعة الحقول **النطاق**، أدخل معلومات حول فترة الأيام والمستودعات لتضمينها في النظرة العامة.
2.  على علامة التبويب السريعة **خيارات الوصول**، في مجموعة حقول **دفتر اليومية**، أدخل المستودع المستلم والموقع واسم دفتر اليومية (وصول الصنف/مدخلات الإنتاج).
3.  على علامة التبويب السريعة **تفاصيل استعلام الوصول**، في مجموعة الحقول **الموقع**، في الحقل **قيد الموقع** ، أدخل موقعًا لتقييد العرض في منطقة النظرة العامة.
4.  على علامة التبويب السريعة **تفاصيل استعلام الوصول**، في مجموعة الحقول **أنواع الحركات المعروضة**، قم بتعيين الخيار **أوامر الإنتاج** إلى **نعم**.
5.  على علامة التبويب السريعة **تفاصيل استعلام الوصول**، في مجموعة الحقول **متنوعة**، قم بتعيين الخيار **تحديث عند بدء التشغيل** إلى **نعم** إذا كان يجب تحديث العرض تلقائيًا عند بدء التشغيل. قم بتعيين الخيار **التحديث عند تغيير النطاق** إلى **نعم** إذا كان يجب أن يتم تلقائيًا تحديث العرض عند حدوث تغيير في قيم النطاق‏‎.

بالنسبة إلى هذا المثال، تم تعيين الحقل **اسم ملف تعريف النظرة العامة على الوصول** على علامة التبويب السريعة **خيارات الوصول** في الصفحة **نظرة عامة على الوصول** إلى **إنتاج الموقع 1**.

### <a name="prerequisites-for-arrival-journals"></a>المتطلبات الأساسية لدفاتر يومية الوصول

لإنشاء دفاتر يومية الوصول بشكل تلقائي من الصفحة **نظرة عامة على الوصول**، يجب عليك تحديد المعلومات المناسبة في مجموعة الحقول **دفتر اليومية** على علامة التبويب السريعة **خيارات الوصول**.

-   يجب تحديد اسم دفتر يومية لإنشاء دفتر يومية. 

[![تحديد اسم دفتر اليومية](./media/arrival-overview-journal.png)](./media/arrival-overview-journal.png)

-   إذا حددت القيم الموجودة في حقلي **المستودع** و**الموقع**، فسيتم تطبيق هذه القيم على بنود دفتر اليومية. إذا لم تحدد القيم، فإن النظام يستخدم القيم من البُعد الذي تم تحديده في حركات المخزون.

#### <a name="items-that-are-received-from-one-expected-receipt-order"></a>الأصناف التي تم استلامها من أمر استلام متوقع

على علامة التبويب السريعة **عمليات الاستلام**، يحدد سامي بندًا ثم ينقر فوق **بدء الوصول**. يتم بشكل تلقائي تحديد كافة البنود ذات الصلة الموجودة في النطاق المحدد والتي لديها كمية يجب تسجيلها. يتم إنشاء دفتر يومية وصول الصنف الذي يوجد فيه تطابق بين أمر الاستلام المتوقع ودفتر اليومية. تتم تهيئة الكمية تلقائيًا على كافة البنود التي تم إنشاؤها.

#### <a name="items-that-are-received-from-more-than-one-expected-receipt-order"></a>الأصناف التي تم استلامها من أكثر من أمر استلام متوقع

على علامة التبويب السريعة **عمليات الاستلام**، يحدد سامي عدة بنود ثم ينقر فوق **بدء الوصول**. يتم إنشاء دفتر يومية وصول الصنف الذي يوجد فيه تطابق بين جميع أوامر الاستلام المتوقعة ودفتر اليومية. يتم إنشاء كافة البنود في رأس دفتر يومية وصول صنف واحد، وتتم تهيئة الكمية تلقائيًا.

### <a name="receive-items-from-one-or-more-expected-receipt-orders"></a>استلام أصناف من أمر استلام متوقع واحد أو أكثر

#### <a name="view-information"></a>عرض المعلومات

للحصول على نظرة عامة حول عمليات الاستلام المتوقعة في فترة تاريخ، يدخل سامي المعلومات التالية في الحقول الموجودة على علامة التبويب السريعة **خيارات الوصول**  في الصفحة **نظرة عامة على الوصول**، ثم ينقر فوق **تحديث** لتحديث طريقة العرض:

-   اسم ملف تعريف النظرة العامة على الوصول: **استعلام**
-   إظهار البنود: **الكل**
-   الأيام السابقة: (فارغ)
-   الأيام التالية: **0**
-   المستودعات: **GW وMW**

باستطاعة سامي عرض المعلومات التالية:

-   كافة أوامر الاستلام ذات الصلة لتاريخ النظام وعدد غير محدود من أيام العمل في الماضي منها (**InventTrans.StatusDate** الفاصل الزمني)، وإيصالات الاستلام لمستودعات GW وMW، بغض النظر عن الحالة.
-   معلومات مفصلة حول البنود لأكثر من أمر واحد. باستطاعة سامي GW and MW عدة بنود رأس متعددة في النظرة العامة ثم النقر فوق **إظهار كل المحدد** لعرض كافة المعلومات المناظرة حول تفاصيل البنود لكافة الأوامر المحددة.
-   معلومات حول أمر شراء معين. لإظهار فقط المعلومات المرتبطة برقم مرجعي محدد في النظرة العامة، يستطيع سامي إدخال رقم حساب في الحقل **رقم الحساب** ورقم أمر في حقل **الرقم المرجعي**.
-   نظرة عامة على تسجيل المهام المستحقة لكافة بنود الأمر التي تم إنشاء دفتر يومية وصول أصناف لها ولكن لم يتم ترحيلها بعد. لعرض هذه المعلومات، يستطيع سامي تحديد **قيد التقدم** في الحقل **إظهار البنود‬**.

### <a name="update-journals"></a>تحديث دفاتر اليومية

لتسجيل بند أمر أو أكثر لمعالجته، يستطيع سامي تحديد البنود في شبكة النظرة العامة أو في شبكة البنود، ثم النقر فوق **دفاتر اليومية** &gt; **إظهار عمليات الوصول من عمليات الاستلام**. يتم عرض عناوين وصول الأصناف التي تتطابق مع البنود. لتحديث إيصال استلام منتجات أمر لأصناف مسجلة، يستطيع سامي الوصول إلى رؤوس دفتر يومية وصول الصنف الجاهزة للتحديث. للوصول إلى رؤوس دفتر يومية وصول الصنف هذه، ينقر سامي فوق **دفاتر اليومية** &gt; **دفاتر اليومية الجاهزة لإيصال استلام المنتجات**. يتم عرض كافة بنود الرأس الجاهزة لتحديث إيصال استلام المنتجات في نطاق المستودع المحدد. (لا تتعلق بنود الرأس التي تظهر بفترة الأيام).

### <a name="start-an-arrival-registration"></a>بدء تشغيل تسجيل الوصول

عن طريق تحديد بنود متعددة في الصفحة **نظرة عامة على الوصول**، يستطيع سامي بدء الوصول لأكثر من مرجع إيصال واحد. عندما يقوم بتحديد بند من النظرة العامة على عمليات الاستلام، يتم تحديد تفاصيل البند المقابل. في حالة وجود كمية للتسجيل، سيكون الزر **بدء الوصول** متاحًا. يستطيع سامي استخدام أسلوبين لبدء تسجيل الوصول:

-   لتصفية الصفحة بحيث تعرض فقط السجلات التي تستوفي معايير محددة، في الحقل **مرجع المورد**، امسح رقمًا مرجعيًا من أحد الموردين، مثل الرمز الشريطي الخاص بمذكرة تسليم.
-   في جزء النظرة العامة أو في جزء التفاصيل في الصفحة **نظرة عامة على الوصول**، حدد يدويًا مجموعة من السجلات لتسجيل الوصول. عندئذٍ، عندما ينقر سامي فوق **بدء الوصول**، يتم بشكل تلقائي إنشاء السجلات المحددة في دفتر يومية دفتر وصول الصنف. تتضمن السجلات معلومات حول البنود، ويتم تعيين كافة معلومات الحقل الفريدة.

## <a name="update-arrival-information-and-process-a-product-receipt"></a>تحديث معلومات الوصول ومعالجة إيصال استلام المنتجات
بعد تسجيل كافة السلع، يستطيع مدير المستودع أو مدير الشراء تحديث الأصناف المستلمة بواسطة إيصال استلام المنتجات لإضافة التكلفة الفعلية. لتحديث معلومات الوصول وترحيل إيصال استلام المنتجات، اتبع هذه الخطوات.

1.  انقر فوق **إدارة المخزون** &gt; **الأوامر الواردة** &gt; **نظرة عامة على الوصول**.
2.  في الصفحة **نظرة عامة على الوصول**، انقر فوق **دفاتر اليومية** &gt; **دفاتر اليومية الجاهزة لإيصال استلام المنتجات‬** لعرض قائمة بدفاتر اليومية الجاهزة لتحديث إيصال استلام المنتجات.
3.  حدد دفاتر اليومية التي يجب تحديثها، ثم انقر فوق **الوظائف** &gt; **إيصال استلام المنتجات**.
4.  في الصفحة **ترحيل**، أدخل رقم إيصال استلام المنتجات، إذا لم يكن متوفرًا في دفتر اليومية، ومن ثم انقر فوق **موافق** لمعالجة إيصال استلام المنتجات.

## <a name="summary"></a>ملخص
باستطاعة الصفحة **نظرة عامة على الوصول** مساعدة مدير المستودع والعاملين فيه على تحقيق نظرة عامة على العمل المتوقع الذي يجب تنفيذه كجزء من عملية واردة. ويمكن استخدام الصفحة أيضًا لبدء عملية وصول الصنف، للمساعدة في ضمان تعقب هذه العناصر عند الدخول الأول إلى المستودع.



