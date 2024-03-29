---
title: فوترة المشاريع
description: توفر هذه المقالة نظرة عامة حول فوترة المشاريع لمشاريع الوقت والمواد والمشاريع ثابتة السعر. وتتضمن معلومات حول مقترحات الفاتورة (الفواتير الأولية) والتحكم في الفواتير والفوترة على الحساب وفوترة المورّد والإشعارات الدائنة.
author: TaylorVH
ms.date: 07/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjInvoiceCashFlow, ProjInvoiceControl, ProjInvoiceListPage, ProjInvoiceProposalDetail, ProjInvoiceProposalListPage
audience: Application User, IT Pro
ms.reviewer: zezhangzhao
ms.custom: 23111
ms.assetid: 1812d6f2-8b34-4258-8f5f-dcf12281547f
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-07-06
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 4af44127d80c943ed9cebeac21d7e9c8372910f3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861665"
---
# <a name="project-invoicing"></a>فوترة المشاريع

[!include [banner](../includes/banner.md)]

توفر هذه المقالة نظرة عامة حول فوترة المشاريع لمشاريع الوقت والمواد والمشاريع ثابتة السعر. وتتضمن معلومات حول مقترحات الفاتورة (الفواتير الأولية) والتحكم في الفواتير والفوترة على الحساب وفوترة المورّد والإشعارات الدائنة.

يحدد نوع المشروع إجراء الفوترة الواجب تطبيقه. ويمكن فقط فوترة نوعي المشروع الخارجيين وهما مشاريع الوقت والمادة والمشاريع ثابتة السعر. ويتم دائمًا إرفاق مشاريع الوقت والمادة والمشاريع ثابتة السعر بعقد المشروع.

-   **المشاريع ثابتة السعر** – يعتمد مبلغ الفاتورة على خطط فوترة الفواتير. ويتم إجراء الفوترة من خلال إعداد على الحساب، والذي يشار إليه أيضًا كخطة فوترة. ويمكن فوترة المشاريع ثابتة السعر حسب المشروع أو عقد المشروع.
-   **مشاريع الوقت والمادة** – يعتمد مبلغ الفاتورة على بنود الحركة التي يتم إدخالها في المشاريع. ويمكن فوترة الحركة حسب المشروع أو حسب عقد المشروع.

وهناك ثلاثة طرق لإرفاق مشاريع الوقت والمادة والمشاريع ثابتة السعر بمشاريع الفواتير:

-   **الفوترة على الحساب** – يمكن فوترة مشاريع الوقت والمادة والمشاريع ثابتة السعر على الحساب. ويتطلب ذلك نوعين من الإعدادات على الحساب، واحد لكل نوع مشروع.
-   **الفوترة في المقطع الدوري** – يمكن من خلال الوظائف الدورية فوترة الحركات عبر المشاريع. وتوفر الوظائف الدورية نظرة عامة للحركات الواجب فوترتها.
-   **باستخدام إشعارات الدائن في الفوترة** – يمكن إنشاء إشعار دائن لكل من مشاريع الوقت والمادة والمشاريع ثابتة السعر.

## <a name="invoice-proposals"></a>مقترحات الفاتورة
قبل إنشاء فاتورة عميل لأحد المشروعات، يمكنك إنشاء فاتورة مبدئية أو مقترح فاتورة. في مقترح فاتورة، يمكن تحديد حركات المشروع لتضمينها في فاتورة مشروع. ويمكنك حينئذٍ مراجعة تفاصيل الفاتورة قبل ترحيل فاتورة المشروع وإرساله إلى العميل أو مصدر التمويل الآخر.

### <a name="creating-invoice-proposals"></a>إنشاء مُقترحات فاتورة

يمكنك إنشاء مقترحات الفاتورة عن طريق تحديد حركة يدويًا من قائمة الحركات المتوفرة الخاصة بمشروع محدد. يمكنك أيضا إعداد قواعد الفوترة التي تحدد متى يتم إنشاء مقترح فاتورة تلقائيًا. على سبيل المثال، يمكنك إنشاء قاعدة فوترة لإنشاء مقترح فاتورة عند العمل على مشروح مكتمل بنسبة 25 و50 و75 و100 بالمئة. 

يمكنك إنشاء مقترحات الفاتورة للحركات التالية:

-   الساعات والمصروفات وحركات المشروع الأخرى
-   المبالغ التي تستقطع بواسطة العملاء على فواتير المشروع السابق
-   إشعارات دائن
-   المبالغ التي يدفعها لك عميل قبل بدء مشروع ما

> [!NOTE]
> تعمل ميزة **تمكين الفرز حسب المورد أثناء إنشاء مقترح فاتورة المشروع** على تمكين تمكين محاسب المشروع لفرز حركات المشروع المتاحة للفوترة حسب المورد عند إنشاء مقترح فاتورة مشروع جديد. ستتضمن الشبكة التي تعرض حركات المشروع المتاحة حقلين منفصلين لكل من **معرف المورد** و **المورد**. تتيح لك هذه الحقول التصفية والفرز على اسم المورد. تكون هذه الميزة متوقفة عن التشغيل بشكل افتراضي. ويمكن تمكينها باستخدام صفحة **إدارة الميزات** (**مساحات العمل> إدارة الميزات**). اتصل بمسؤول النظام للمساعدة في تمكين هذه الميزة.

يمكنك إنشاء حركات الرسوم في مقترح فاتورة. يمكنك أيضا تعديل سعر المبيعات في حركات الساعة والمصروفات والأصناف والرسوم. عند ترحيل مقترح فاتورة، تتم إضافة الحركات والأسعار المحدثة إلى تقارير المشروع وتاريخ الحركة. 

ولإنشاء فواتير عميل متعددة، يجب إنشاء مقترح فاتورة لكل فاتورة. على سبيل المثال، يمكنك إنشاء فواتير بناءً على نوع الحركة. ولتحديد الساعات في فاتورة عميل واحدة وتحديد الأصناف في فاتورة أخرى، يجب إنشاء مقترحات فواتير منفصلة لحركات الساعات وحركات الرسوم. 

في حالة احتواء أحد المشرعات على أكثر من مصدر تمويل واحد، يمكنك إنشاء مقترح فاتورة منفصل لكل مصدر من مصادر التمويل. وفي صفحة **توزيعات قاعدة التمويل**، يمكنك تحديد النسبة المئوية لمبلغ الحركة لتخصيصها لكل مصدر من مصادر التمويل، والمصدر لترحيل الاختلافات التقريبية إليه.

### <a name="creating-customer-invoices-from-invoice-proposals"></a>إنشاء فواتير العملاء من مقترحات الفاتورة

بعد إنشاء مقترح فاتورة وترحيله، يتم إنشاء فاتورة عميل تلقائيًا للحركات التي تم تضمينها في مقترح الفاتورة. 

وقبل ترحل مقترح فاتورة، يمكنك إضافة الحركات إليها أو حذفها منها. على سبيل المثال، يمكنك إزالة حركات المصروفات التي تم ترحيلها إلى أحد المشروعات إلا أنه لا يمكن تحميل رسومها للعميل. 

إذا كانت مؤسستك تتطلب مراجعة مقترحات الفاتورة قبل ترحيلها، فقد يلزم اعتماد مقترح الفاتورة من خلال سير عمل "مراجعة مقترحات فاتورة المشروع‬" قبل ترحيله.

### <a name="view-grant-information-on-project-invoice-list-pages"></a>عرض معلومات المنح في صفحات قوائم فواتير المشروع

بإمكان مستخدمي القطاع العام إضافة **معرف المنحة** و **اسم المنحة** إلى صفحات القائمتين **مقترحات فاتورة المشروع** و **فواتير المشروع**. يتم تمكين هذه الأعمدة باستخدام الميزة **إضافة معلومات المنح في صفحات قوائم فواتير المشروع**. تكون هذه الميزة متوقفة عن التشغيل بشكل افتراضي ويمكن تمكينها في **مساحات العمل > إدارة لميزات**. اتصل بمسؤول النظام للمساعدة في تمكين هذه الميزة.

## <a name="on-account-invoicing"></a>فوترة على الحساب
يستند المبلغ الذي قمت بإدخاله في فاتورة على الحساب لمشروع إلى التوقيت والنسبة المئوية للاكتمال وغيرها من شروط الفوترة الأخرى المحددة في عقد المشروع المرتبط. لا يتم احتساب المبلغ على أساس عدد الساعات أو الأصناف أو المصروفات أو الرسوم أو الحركات الأخرى التي تم ترحيلها إلى مشروع. 

يجب إنشاء حركة على الحساب لمشروع مشروع وقت ومادة‬ أو لمشروع سعر ثابت قبل إضافة حركة على الحساب لإنشاء فاتورة مشروع. وفي الحركة التي تتم على الحساب، أدخل المبلغ لفوترة عميل. لإنشاء فاتورة مشروع لمبلغ، قم بإنشاء فاتورة أولية (اقتراح فاتورة). في اقترح الفاتورة، حدد الحركة على الحساب يمكنك مراجعة معلومات على الحساب في مقترح الفاتورة قبل إنشاء فاتورة مشروع له. 

### <a name="fixed-price-projects"></a>مشاريع ثابتة السعر
للمشاريع ثابتة السعر، تستند حركات على الحساب إلى النقاط الرئيسية المتفق عليها، ووحدة التسليم أو ترتيبات فوترة الإنجاز المحدد في عقد مشروع. يتم إنشاء بند واحد لكل عملية دفع يجب تلقيها من عملاء المشروع. لا يلزم توفر أية خصومات.

### <a name="time-and-material-projects"></a>مشاريع الوقت والمواد

بالنسبة لمشاريع الوقت والمواد، يمكن فاتورة عميل أو مصدر التمويل الآخر بمبلغ الدفع مقدمة باستخدام مقترح فاتورة على الحساب. ادخل الحركات على الحساب كبند واحد. بشكل اختياري، يمكنك إدخال بنود إضافية كخصومات مقابل أي مدفوعات تمت بواسطة العميل. ولإنشاء بنود الخصم، أدخل علامة الطرح قبل المبلغ.

## <a name="invoice-control"></a>مراقبة الفواتير
يمكنك استخدام التحكم في الفاتورة لتعقب الحركات المفوترة وغير المفوترة، وتحليل هذه الحركات مقابل عروض أسعار لطريقة عرض شاملة للمشاريع من مرحلة عرض الأسعار حتى الانتهاء. ويمكنك أن ترى الحركات التي تم تحميلها لمشروع محدد والبنود التي تمت فوترتها. ويمكنك أيضًا عرض الحركات الفردية حتى تتمكن من تعديلها بعد ترحيلها.

## <a name="invoicing-fixed-price-projects"></a>فوترة المشاريع ثابتة السعر
لفوترة مشروع ثابت سعر، يجب عليك تحديد جدول فوترة وإكمال إجراء الفوترة.

### <a name="billing-schedule"></a>جدول الفوترة

يمكنك فوترة المشاريع ثابتة السعر في جدول فوترة. ويتم تحديد جدول الفوترة فيما يتعلق بواحد أو أكثر من الأحداث الرئيسية للمشروع. ولكل مرحلة رئيسية، يمكنك تحديد تاريخ محدد وعملة مبيعات وسعر المبيعات والنشاط. 

على سبيل المثال، يمكنك إعداد جدول الفوترة التالي:

-   20 في المائة عند توقيع عقد المشروع
-   30 بالمائة عند أول عملية تسليم
-   15 بالمائة عند ثاني عملية تسليم
-   35 بالمائة عند التسليم النهائي

### <a name="invoicing-procedure"></a>إجراء الفوترة

عندما تكون المدفوعات المهمة جاهزة للفوترة، استخدم الإجراء لفوترة المبالغ المقيدة على الحساب.

## <a name="vendor-invoicing"></a>إصدار فاتورة المورّد
عندما تطلب صنفًا من مورد وتقوم بتعيين هذا الصنف إلى مشروع، تحدد خاصية البند التي تحددها لبند أمر شراء لهذا الصنف فوترة الصنف المشتري لعميل أو لا. إذا قمت بإعداد خصائص البند الافتراضي، فستظهر للصنف الموجود في بند أمر الشراء (**تفاصيل البنود > المشروع > تفاصيل خاصية البنود**). هناك طريقتان لتعديل خاصية البند:

-   فوترة عميل المشروع للصنف. للقيام بذلك، عيّن خاصية البند للصنف إلى قيمة خاضعة للرسوم في أمر الشراء، ثم قم بفوترة العميل باستخدام طريقة فوترة المشروع الصحيحة.
-   عدم فوترة عميل المشروع للصنف. للقيام بذلك، لا تحدد خاصي البند **خاضع للرسوم** في بند أمر الشراء للصنف. ويمكنك فيما بعد فوترة أمر الشراء ولا يلزم اتخاذ أي إجراء آخر.

> [!NOTE] 
> بنود استبقاء الإصدار بلا رسوم بشكل افتراضي. ويعني ذلك عدم تمكين إمكانية إنشاء مقترح فاتورة لعمليه الاستبقاء التي تم إصدارها.

## <a name="credit-notes"></a>إشعارات دائن
عندما تكون قيمة أحد مبالغ فاتورة العميل سالبة، يتم تصنيف الفاتورة على أنها إشعار دائن. وعند طباعة المستند، تشتمل على العنوان "إشعار الدائن". 

وعندما تقوم بإنشاء إشعار دائن لإضافة مبلغ تمت فوترته مسبقاً، يجب أولاً تحديد المبلغ المفوتر للإضافة. ويمكنك فيما بعد إنشاء إشعار دائن باتباع نفس الإجراء المستخدم لإنشاء فاتورة عميل عادية. أنت تحدد الحركات التي تم ترحيلها من قبل لفاتورة العميل ثم تحرير وإنشاء مقترح إشعار دائن. 

ويمكن أن يشتمل نفس المستند على الحركات التي تم تحديدها للإضافة والحركات الدائنة والحركات التي تم ترحيلها. ويتم تصنيف المستند حينئذٍ بإما فاتورة أو إشعار دائن، وذلك طبقًا لكون المبلغ الإجمالي موجبًا أم سالبًا. 

ولإضافة مبلغ تمت فوترته، يجب أولاً تحديد المبلغ المفوتر المراد إضافته ثم إنشاء إشعار دائن. وتقوم بإشاء إشعار دائن باستخدام نفس الإجراء المستخدم لإنشاء فاتورة عميل. 

يمكنك إنشاء فاتورة بمبلغ سالب حيث تصنف هذه الفاتورة كإشعار دائن. ويتعين عليك تحديد الحركات التي تم ترحيلها من قبل لفاتورة العميل ثم تعديل الحركات لإنشاء إشعار دائن وطباعته. ما لم يكن العنوان الرئيسي للكيان القانوني موجودًا في ألمانيا، فسيكون عنوان الفاتورة هو "فاتورة تصحيحية".





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
