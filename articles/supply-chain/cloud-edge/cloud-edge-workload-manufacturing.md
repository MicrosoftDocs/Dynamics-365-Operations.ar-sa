---
title: أحمال تنفيذ التصنيع لوحدات مقياس السحابة والحافة
description: يصف هذا الموضوع كيفيه عمل التصنيع في تنفيذ الاعمال مع وحدات مقياس السحابة والحافة.
author: cabeln
manager: ''
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 08c46655d3966ad1433935318c5e60667dd10bb6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967748"
---
# <a name="manufacturing-execution-workloads-for-cloud-and-edge-scale-units"></a>أحمال تنفيذ التصنيع لوحدات مقياس السحابة والحافة

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> لا يتم دعم بعض وظائف الاعمال بشكل كامل في المعاينة العامة عند استخدام حمل العمل على وحدات القياس.

في تنفيذ عمليه التصنيع ، تقوم وحدات السحابة والحافة بتسليم الإمكانيات التالية ، حتى إذا لم تكن وحدات الحافة متصلة بالمركز:

- ويمكن لمشرفي حاله العمل ومشرفي حاله العمل الوصول إلى خطه الإنتاج الجاهزة.
- يمكن لعوامل تشغيل الجهاز الحفاظ علي الخطة محدثه عن طريق تشغيل وظائف التصنيع المنفصلة وعمليات التصنيع.
- يمكن لمشرف حاله العمل تسويه خطه التشغيل.
- يمكن للعاملين الوصول إلى الوقت والحضور لبدء العمل وإنهاء العمل علي الحافة ، وذلك لضمان حساب دفع العامل الصحيح.

يصف هذا الموضوع كيفيه عمل التصنيع في تنفيذ الاعمال مع وحدات مقياس السحابة والحافة.

## <a name="the-manufacturing-lifecycle"></a>دوره حياه التصنيع

كما يوضح الرسم التوضيحي التالي ، تنقسم دوره حياه التصنيع إلى ثلاث مراحل: *التخطيط* و *التنفيذ* و *الإنهاء*.

[![مراحل تنفيذ التصنيع عند استخدام بيئة واحده](media/mes-phases.png "مراحل تنفيذ التصنيع عند استخدام بيئة واحده")](media/mes-phases-large.png)

تتضمن مرحله _الخطة_ تعريف المنتج والتخطيط وإنشاء الأمر وجدولته وإصداره. تشير خطوه الإصدار إلى الانتقال من مرحله _التخطيط_ إلى مرحله _التنفيذ_. عند إصدار أمر إنتاج ، ستكون وظائف أمر الإنتاج مرئية في حاله الإنتاج وتكون جاهزه للتنفيذ.

عند وضع علامة علي مهمة إنتاج كمكتملة ، فانها تنتقل من مرحله _التنفيذ_ إلى مرحلة _الإنهاء_. في مرحله _الإنهاء_، تمر التسجيلات من مرحله *التنفيذ* خلال سير عمل الاعتماد ، حيث يتم حسابها واعتمادها وتحويلها. وفي هذه المرحلة ، يتم إكمال أمر الإنتاج. التالي ، يتم إنشاء أساس الدفع الخاص بالعاملين.

## <a name="splitting-the-execute-phase-into-a-separate-workload"></a>تقسيم مرحله "التنفيذ" إلى حمل عمل منفصل

كما يوضح الرسم التوضيحي التالي ، عند استخدام وحدات المقياس، يتم تقسيم مرحله _التنفيذ_ كحمل عمل منفصل.

[![مراحل تنفيذ التصنيع عند استخدام وحدات المقياس](media/mes-phases-workloads.png "مراحل تنفيذ التصنيع عند استخدام وحدات المقياس")](media/mes-phases-workloads-large.png)

ينتقل الآن الطراز من تثبيت مفرد المثيل إلى طراز يستند إلى وحدات المحور والمقياس. تعمل مرحلتا _التخطيط_ و _الإنهاء_ كعمليات المكتب الخلفي علي المركز، ويتم تشغيل حمل العمل الخاص بتنفيذ التصنيع علي وحدات المقياس. يتم نقل البيانات بشكل غير متزامن بين المركز ووحدات القياس.

عند إصدار أمر إنتاج في المركز، يتم تحويل كافة البيانات المطلوبة لمعالجه وظائف الإنتاج إلى وحده القياس. وتشتمل هذه البيانات علي أوامر الإنتاج ومسارات الإنتاج وقائمة مكونات الصنف والمنتجات. يتم أيضا تحويل البيانات غير المرتبطة بامر الإنتاج (مثل الانشطه غير المباشرة وأكواد الغياب ومحددات الإنتاج) من المركز إلى وحده المقياس. وكقاعده ، يمكن إنشاء البيانات التي تنشا من المركز والتي تم تحويلها إلى وحده القياس علي المركز فقط. علي سبيل المثال ، لا يمكن إنشاء كود غياب جديد أو نشاط غير مباشر علي وحده المقياس، يمكن استخدامها فقط للتسجيل. يتم بعد ذلك تحويل التسجيلات التي تم اجراؤها علي وحده القياس اثناء التنفيذ إلى المركز، حيث تتم معالجه الموافقة علي الوقت والحضور والمخزون والتحديثات المالية.

## <a name="manufacturing-execution-tasks-that-can-be-run-on-workloads"></a>مهام تنفيذ التصنيع التي يمكن تشغيلها علي أحمال العمل

يمكن تشغيل مهام تنفيذ التصنيع التالية علي أحمال العمل حاليا عند استخدام وحدات القياس:

- بدء العمل وتسجيل الدخول وإنهاء العمل والغياب
- بدء الوظيفة
- مجموعة الوظائف
- تقرير التقدم
- التبليغ عن الخردة
- نشاط غير مباشر
- مقاطعة

## <a name="working-with-manufacturing-execution-workloads-on-the-hub"></a>العمل مع أحمال تنفيذ التصنيع علي المركز

عاده ، يتم تشغيل العمليات المطلوبة لتشغيل أحمال التنفيذ التصنيعية تلقائيا للاحتفاظ بالمركز ولكافة وحدات المقياس في المزامنة ، حسب الحاجة. ومع ذلك ، إذا كانت لديك مشكله ، فيمكنك تشغيل معالجه التسجيلات الاوليه التي تم استلامها من أحمال العمل و/أو التحقق من سجل معالجه التسجيل.

### <a name="manually-process-raw-registrations"></a>معالجه التسجيلات الاوليه يدويا

يتم تشغيل وظيفة المجموعة في Supply Chain Management تلقائيا لمعالجه كافة التسجيلات التي تم استلامها من أحمال العمل. تقوم هذه الوظيفة بإنشاء دفاتر يوميه الإنتاج المطلوبة وإدخالات لوجبوك عند معالجه تسجيل لمهمة مكتملة في حمل العمل.

علي الرغم من ان المهمة عاده ما تعمل تلقائيا ، الا انه يمكن تشغيلها يدويا في اي وقت عن طريق تسجيل الدخول إلى المركز والانتقال إلى **التحكم في الإنتاج \> المهام الدورية \> أداره حمل العمل في المكتب الخلفي\> معالجة عمليات التسجيل الأولي**.

### <a name="check-the-raw-registration-processing-log"></a>التحقق من سجل معالجه التسجيل الاولي

لمراجعه سجل معالجه التسجيل ، قم بتسجيل الدخول إلى المركز ، ثم انتقل إلى **التحكم في الإنتاج \>المهام الدورية \> إدارة حمل العمل في المكتب الخلفي \>سجل معالجه التسجيل الاولي**. تعرض الصفحة **سجل معالجه التسجيل الاولي** قائمه بالتسجيلات الاوليه التي تمت معالجتها وحاله كل تسجيل.

![صفحة سجل معالجه التسجيل الاولي](media/mes-processing-log.png "صفحة سجل معالجه التسجيل الاولي")

يمكنك العمل علي اي تسجيل في القائمة وذلك بتحديده ثم تحديد أحد الأزرار التالية في جزء الإجراءات:

- **العملية** – معالجه التسجيل المحدد يدويا. يمكن ان يكون هذا الاجراء مفيدا في حاله عدم تشغيل مهمة _معالجة التسجيلات الاوليه_ أو في حاله فشلها.
- **إلغاء الأمر** – يستخدم للغاء التسجيل المحدد.

## <a name="working-with-manufacturing-execution-workloads-on-a-scale-unit"></a>العمل مع أحمال تنفيذ التصنيع علي وحدة المقياس

عاده ، يتم تشغيل العمليات المطلوبة لتشغيل أحمال التنفيذ التصنيعية تلقائيا للاحتفاظ بالمركز ولكافة وحدات المقياس في المزامنة ، حسب الحاجة. ومع ذلك ، إذا كنت تواجه مشكله، فيمكنك التحقق من سجلات الأوامر التي تمت معالجتها علي وحده قياس أو تشغيل مهمة _معالج رسائل مركز التصنيع إلى وحدة القياس_ يدويًا.

### <a name="view-the-history-of-manufacturing-jobs-that-have-been-processed-on-a-scale-unit"></a>عرض تاريخ مهام التصنيع التي تمت معالجتها علي وحده قياس

لمراجعه سجلات مهام التصنيع التي تمت معالجتها علي وحده قياس ، قم بتسجيل الدخول إلى جهاز وحده القياس ، ثم انتقل إلى **التحكم في الإنتاج\> المهام الدورية \> إدارة حمل العمل في المكتب الخلفي \> سجل معالجة مهام التصنيع**. تعرض صفحه **سجلات معالجه مهام التصنيع** سجل المعالجة الخاص بأوامر الإنتاج في وحده القياس. يمكنك العمل علي اي أمر إنتاج في القائمة وذلك بتحديده ثم تحديد أحد الأزرار التالية في جزء الإجراءات:

- **المعالجة** – معالجه أمر الإنتاج المحدد يدويا.
- **إلغاء الأمر** – يستخدم لإلغاء أمر الإنتاج المحدد.

### <a name="manufacturing-hub-to-scale-unit-message-processor-job"></a>مهمة معالج رسائل مركز التصنيع إلى وحدة القياس

تقوم مهمة _معالج رسائل مركز التصنيع إلى وحدة القياس_ بمعالجه البيانات من المركز إلى وحده القياس. يتم بدء هذه الوظيفة تلقائيا عند نشر حمل العمل الخاص بتنفيذ التصنيع. ومع ذلك ، يمكن تشغيلها يدويا في اي وقت عن طريق الانتقال إلى **التحكم في الإنتاج \> المهام الدورية \> إدارة حمل العمل في المكتب الخلفي \> معالج رسائل مركز التصنيع إلى وحدة القياس**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]