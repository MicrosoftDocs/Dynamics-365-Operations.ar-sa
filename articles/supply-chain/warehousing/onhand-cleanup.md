---
title: مهمة تنظيف الإدخالات المتاحة في إدارة المستودع‬‏‫
description: يصف هذا المقال مهمة تنظيف الإدخالات المتاحة في إدارة المستودع‬‏‫، مما يساعد على تحسين أداء النظام عن طريق التعرف على السجلات ذات الصلة ولكن غير المطلوبة وحذفها.
author: perlynne
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-04-03
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: df20f00a639d237bf8446f24a2ad4cbbfcf36615
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334374"
---
# <a name="warehouse-management-on-hand-entries-cleanup-job"></a>مهمة تنظيف الإدخالات المتاحة في إدارة المستودع‬‏‫

[!include [banner](../includes/banner.md)]

يتأثر أداء الاستعلامات المستخدمة لحساب المخزون الفعلي بعدد السجلات الموجودة في الجداول المعنية. ثمة طريقة لتحسين الأداء وهي تقليل عدد السجلات التي يجب أن تأخذها قاعدة البيانات في الاعتبار.

Tتصف مقالته مهمة تنظيف الإدخالات الفعلية ، والتي تحذف السجلات غير الضرورية في ملف `InventSum` و `WHSInventReserve` الجداول. تقوم هذان الجدولان بتخزين المعلومات الموجودة للأصناف التي تم تمكينها لمعالجة إدارة المستودع. (يُشار إلى هذه الأصناف باسم أصناف WMS.) قد يؤدي حذف هذه السجلات إلى تحسين أداء عمليات حساب القيم الفعلية.

## <a name="what-the-cleanup-job-does"></a>ما تقوم به مهمة التنظيف

تؤدي مهمة تنظيف الإدخالات الفعلية إلى حذف أي سجلات في ملف `WHSInventReserve` و `InventSum` الجداول حيث تكون جميع قيم الحقول *0* (صفر). ويمكن حذف هذه السجلات لأنها لا تساهم في المعلومات الفعلية. تقوم الوظيفة بحذف السجلات التي تقع تحت مستوى **الموقع** فقط.

إذا تم السماح بالمخزون السالب الفعلي، فقد لا تتمكن مهمة التنظيف من حذف كافة الإدخالات ذات الصلة. يعود سبب هذا التقييد إلى أنه يتعين على المهمة السماح بسيناريو معين حيث تتضمن لوحة ترخيص أرقامًا تسلسلية متعددة، وأصبح أحد هذه الأرقام سالبًا. على سبيل المثال، سيكون لدى النظام صفر متاح على مستوى لوحة الترخيص عندما يكون لدى لوحة الترخيص +1 قطع من الرقم التسلسلي 1 و–1 من الرقم التسلسلي 2. لهذا السيناريو الخاص، تجري المهمة أولاً عملية حذف واسعة النطاق، حيث تحاول إجراء الحذف من المستويات الدنيا أولاً.

## <a name="schedule-and-configure-the-cleanup-job"></a>جدولة مهمة التنظيف وتكوينها

تتوفر مهمة تنظيف الإدخالات المتاحة في **إدارة المخزون \> المهام الدورية \> التنظيف \> تنظيف الإدخالات المتاحة في إدارة المستودع**. استخدم إعدادات المهمة القياسية للتحكم في نطاق وجدول تشغيل المهمة. علاوةً على ذلك، يتم توفير الإعدادات التالية:

- **الحذف في حالة عدم التحديث لهذا العدد من الأيام‬** – أدخل الحد الأدنى لعدد الأيام التي يجب أن تنتظر خلالها المهمة قبل أن تحذف الإدخالات المتاحة التي انخفضت كميتها إلى الصفر. استخدم هذا الإعداد للمساعدة في تقليل مخاطر حذف الإدخالات المتاحة التي لا تزال قيد الاستخدام. إذا أردت حدوث عملية التنظيف في أقرب وقت ممكن، فيمكنك إدخال *0* (صفر) أو ترك الحقل فارغًا.
- **الحد الأقصى لوقت التنفيذ (بالساعات)** - أدخل الحد الأقصى لوقت التنفيذ لمهمة التنظيف، بالساعات. إذا لم تكتمل المهمة قبل مرور هذه الفترة، فستحفظ العمل الذي اكتمل حتى الآن ثم تُغلق نفسها. تعتبر هذه الإمكانية ذات صلة بشكل خاص فيما يتعلق بعمليات التنفيذ حيث يكون استخدام المخزون شديد الأهمية. في هذه الحالات، يجب جدولة المهمة بحيث تعمل في الأوقات التي يكون فيها حل النظام خفيفًا قدر الإمكان. إذا أردت متابعة تشغيل الوظيفة الدُفعية حتى اكتمالها، فيمكنك إما إدخال *0* (صفر) أو ترك الحقل فارغًا. يتوفر هذا الإعداد فقط إذا كانت الميزة ذات الصلة [قيد التشغيل في النظام](#max-execution-time).

وعلى الرغم من أنه يمكنك تشغيل المهمة أثناء ساعات العمل العادية، إلا أنه المستحسن تشغيلها خارج ساعات العمل. وبهذه الطريقة، يمكنك منع التعارضات التي يمكن أن تحدث إذا كان المستخدم يستخدم سجلاً يجري تنظيفه أيضًا.

إذا حاولت المهمة حذف سجل لأحد العناصر بينما هذا السجل قيد الاستخدام من قبل مستخدم آخر، فسيحدث خطأ توقف تام إما لمهمة التنظيف أو المستخدم.

عند تشغيل المهمة، يكون حجم الالتزام فيها 100. بمعنى آخر، ستحاول الالتزام مرة واحدة لكل 100 عملية حذف. ومع ذلك، ولأن بعض عمليات الحذف تستند إلى مجموعة، فقد تكون هناك سيناريوهات يمكن فيها حذف أكثر من 100 سجل في نفس العملية. وبالتالي، قد تحدث في بعض الأحيان عمليات تصعيد التأمين.

## <a name="possible-user-impact"></a>التأثير المحتمل على المستخدم

قد يتأثر المستخدمون إذا قامت مهمة تنظيف الإدخالات المتاحة بحذف كافة السجلات لمستوى معين (مثل مستوى لوحة الترخيص). في هذه الحالة، قد لا تعمل الوظيفة التي تسمح برؤية أن المخزون كان متاحًا في السابق في لوحة ترخيص كما هو متوقع، لأن الإدخالات المتاحة ذات الصلة لم تعد متوفرة. يمكن، على سبيل المثال، التجربة في المواقف التالية:

- في **القائمة** الفعلية، عندما يقوم المستخدم بإلغاء تحديد الشرط **كميه \<\>0** أو تحديد **الحركات المغلقة** في الحالة في **إعدادات عرض الابعاد**.
- في تقرير **المخزون الفعلي بواسطة ابعاد المخزون** للفترات الماضية، عندما يقوم المستخدم بتعيين معلمه **من التاريخ**.

ومع ذلك، فان تحسين الأداء الذي توفره مهمة التنظيف يجب ان يكون لهذه الخسائر الصغيرة في الوظيفة.

## <a name="make-the-maximum-execution-time-setting-available"></a><a name="max-execution-time"></a>جعل إعداد الحد الأقصى لوقت التنفيذ متوفرًا

يتوفر الإعداد **الحد الأقصى لوقت التنفيذ** فقط عندما تكون الميزة *الحد الأقصى لوقت التنفيذ لوظيفة تنظيف المستودعات المتاحة لإدارة المستودعات* قيد التشغيل. اعتبارًا من الإصدار 10.0.25 من Supply Chain Management، يتم تشغيل هذه الميزة افتراضيًا. بإمكان المسؤولين تشغيل هذه الوظيفة أو إيقاف تشغيلها عن طريق البحث عن ميزة *الحد الأقصى لوقت التنفيذ لوظيفة تنظيف المستودعات المتاحة لإدارة المستودعات‬* في مساحة عمل [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]