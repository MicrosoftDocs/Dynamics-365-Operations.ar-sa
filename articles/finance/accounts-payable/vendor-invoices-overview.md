---
title: نظرة عامة على فواتير الموردين
description: توفر هذه المقالة معلومات عامة حول فواتير المورد.
author: abruer
ms.date: 02/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 565e45a1c396b9144b4a6437056a0040b2fbde1d
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228740"
---
# <a name="vendor-invoices-overview"></a>نظرة عامة على فواتير المورّدين

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


توفر هذه المقالة معلومات عامة حول فواتير المورد. فواتير المورد هي طلبات للدفع للمنتجات والخدمات. فواتير المورد قد تمثل فاتورة في مقابل خدمات مستمرة، أو يمكنها أن تستند إلى أوامر شراء لأصناف وخدمات معينة.

## <a name="vendor-invoices"></a>فواتير المورد

يتم إنتاج فاتورة المورد من أمر شراء عند تلقي المنتجات أو الخدمات وفقًا لأمر شراء تم وضعه مع أحد الموردين. ‏‫وتحتوي فاتورة المورد على رأس، وبند واحد أو أكثر للأصناف أو الخدمات. وتُكمل فاتورة المورد الدورة من أمر الشراء حتى إيصال استلام المنتجات حتى فاتورة المورد.‬

وعلى الرغم من أن بعض فواتير المورد تتصل بأمر شراء، إلا أن فواتير المورد يمكنها أن تتضمن أيضًا البنود التي لا تتوافق مع بنود أمر الشراء. كما يمكنك إنشاء فواتير المورد غير المرتبطة بأي أمر شراء. قد تمثل فواتير المورد هذه الخدمات الجارية، مثل فاتورة مرافق. لا يلزم الرجوع إلى أمر شراء عند إضافة خدمة جارية.

هناك عدة طرق لإدخال فاتورة مورد:

- ‏‫يتيح لك سجل فواتير المورد إمكانية إدخال الفواتير التي لا تشير إلى أمر شراء بسرعة بحيث يمكنك استحقاق المصروفات. وباستخدام دفتر يومية اعتماد فواتير المورد، يمكنك تحديد هذه الفواتير وترحيلها إلى رصيد المورد لإلغاء الاستحقاق.‬
- ويتيح لك دفتر يومية فاتورة المورد إدخال الفواتير التي لا تشير إلى أمر شراء بسرعة، في خطوة واحدة.
- ومع وعاء فواتير المورد، يتيح لك سجل فواتير المورد إدخال الفواتير لاستحقاق المصروفات بشكل سريع. ويمكنك فتح أوامر الشراء المرتبطة لاحقاً لترحيل فاتورة في مقابل حساب المصروفات.
- تتيح لك صفحتا **فواتير المورد المفتوحة** و **فواتير المورد المعلقة** إنشاء فواتير المورد من أوامر الشراء المؤكدة.

توفر المناقشة التالية المزيد من المعلومات حول كيفية استخدام صفحة **فواتير المورد المفتوحة** أو **فواتير المورد المعلقة** لإنشاء فاتورة مورد من أمر شراء.

## <a name="understanding-invoice-line-quantities"></a>استيعاب كميات بند الفاتورة

عندما تفتح فاتورة مورد من أمر شراء مرتبط، يقوم النظام إنشاء بنود فاتورة من أمر الشراء. وبشكل افتراضي، يأخذ النظام الكميات من كمية إيصال المنتج. ومع ذلك، يمكنك استخدام أي من السلوكيات الافتراضية التالية:

- **كمية الاستلام الآن‬** – استخدم هذا الخيار للشحنات الجزئية. سيتم تعيين القيمة الافتراضية في حقل **الكمية** على الكمية المحددة في حقل **استلام الآن** في أمر الشراء.
- **الكمية المطلوبة** – استخدم هذا الخيار للشحنات الكاملة. سيتم تعيين القيمة الافتراضية في حقل **الكمية** إلى الكمية المحددة في حقل **مطلوب** في أمر الشراء.
- **الكمية المسجلة** – استخدم هذا الخيار إذا كان الصنف يتطلب التسجيل، مثلما ما هو محدد في صفحة **مجموعات نماذج الصنف**. تعد القيمة الافتراضية في حقل **الكمية** كمية التحديث الفعلية التي سبق تسجيلها.
- **كمية إيصال استلام المنتجات** – استخدم هذا الخيار إذا تم استلام إيصال منتج بالفعل للأمر. القيمة الافتراضية في حقل **الكمية** هي الكمية الإجمالية لإيصالات استلام المنتجات المتاحة.
- **الكمية والخدمات المسجلة** – استخدم هذا الخيار إذا تم تسجيل الكميات في دفاتر يومية الوصول للأصناف المخزنة أو الأصناف التي لم يتم تخزينها. هذا الخيار يشمل الخدمات أيضًا، بغض النظر عما إذا كانت مسجلة.

وفي حالة استخدام الكيان القانوني لمطابقة الفاتورة، يمكنك عرض نتائج مطابقة الكمية في عمود **مطابقة كمية إيصال استلام المنتجات**. كما يمكنك استخدام زر **تفاصيل المطابقة** في علامة التبويب **مراجعة** في جزء الإجراءات لعرض نتائج مطابقة الكمية.

## <a name="adding-a-line-that-wasnt-on-the-purchase-order"></a>إضافة بند لم يكن موجودًا في أمر الشراء

يمكنك إضافة بند لم يكن موجودًا في أمر الشراء إلى فاتورة المورد. ويجب عليك تحديد فئة التدبير أو رقم صنف. ويمكنك فيما بعد إضافة الكميات والأسعار والمبالغ إلى البند. سيتم تضمين البند فقط في سياسات مطابقة إجماليات الفواتير.

## <a name="submitting-a-vendor-invoice-for-review"></a>إرسال فاتورة مورد للمراجعة

يمكن أن تستخدم مؤسستك عمليات سير العمل لإدارة عملية مراجعة فواتير الموردين. قد تكون مراجعة سير العمل مطلوبة من أجل رأس القائمة، أو بند الفاتورة، أو كليهما. تنطبق عناصر التحكم في سير العمل على الرأس أو البند، اعتمادًا على موضع التركيز عندما تحدد عنصر التحكم. بدلاً من الزر **ترحيل**، يرسل الزر **إرسال** فاتورة المورد من خلال عملية المراجعة.

### <a name="preventing-invoice-from-being-submitted-to-workflow"></a>منع إرسال الفاتورة إلى سير العمل 

فيما يلي عدة طرق يمكنك من خلالها منع إرسال فاتورة إلى سير عمل.

- **إجمالي الفاتورة لا يساوي الإجمالي المسجل.** سيتلقى المستخدم الذي أرسل الفاتورة تنبيهًا بأن الإجماليات غير متساوية. يمنح هذا التنبيه المستخدم فرصة لتصحيح الأرصدة قبل إعادة إرسال الفاتورة إلى نظام سير العمل. تتوفر هذه الميزة في حاله **عدم تساوي** القيمة الخاصة بالإرسال إلى سير العمل عند إجمالي الفاتورة وإجمالي الفاتورة المسجلة في الصفحة أداره **الميزات** وخيار سير العمل **عند عدم تساوي** إجمالي الفاتورة وإجمالي المسجلة محدده في الصفحة معلمات **الحسابات** الدائنة قيد التشغيل. 
- **تحتوي الفاتورة على تكاليف غير مخصصة.** سيتلقى المستخدم الذي أرسل الفاتورة تنبيهًا بأن الفاتورة بها رسوم غير مخصصة. وبهذه الطريقة ، يمكن للمستخدم تصحيح الفاتورة قبل أعاده إرسالها إلى نظام سير العمل. تتوفر هذه الميزة في حالة تشغيل المعلمة **منع التقديم إلى سير العمل عند وجود مصاريف غير مخصصة في فاتورة المورد** في **إدارة الميزات** و **خيار سير العمل عند وجود رسوم غير مخصصة** في **معلمات الحسابات الدائنة** الصفحة قيد التشغيل.
- **تحتوي الفاتورة على رقم الفاتورة نفسه الموجود على فاتورة أخرى مرحّلة.** سيتلقى المستخدم الذي أرسل الفاتورة تنبيهًا بأنه تم العثور على فاتورة تحتوي على رقم مكرر. يمكن للمستخدم تصحيح الرقم المكرر قبل إعادة إرسال الفاتورة إلى نظام سير العمل. سيظهر التنبيه إذا عند تعيين معلمة **التحقق من رقم الفاتورة المستخدم‬** في الحسابات الدائنة إلى **رفض التكرار**. تتوفر هذه الميزة إذا كانت المعلمة **يحظر الإرسال إلى سير العمل عندما يكون رقم الفاتورة موجودًا بالفعل على فاتورة مرحلة ولم يتم إعداد نظامك لقبول أرقام فواتير مكررة‬** في صفحة **إدارة الميزات** قيد التشغيل.
- **تحتوي الفاتورة على بند حيث تكون كمية الفاتورة أقل من كمية إيصالات استلام المنتجات المطابقة.** سيتلقى المستخدم الذي يرسل الفاتورة أو يحاول نشرها رسالة مفادها أن الكميات غير متساوية. تمنح هذه الرسالة المستخدم فرصة لتصحيح القيم قبل إعادة إرسال الفاتورة إلى نظام سير العمل. تتوفر هذه الميزة في حالة تشغيل المعلمة **حظر ترحيل فواتير المورد وإرسالها إلى سير العمل** في الصفحة **إدارة الميزات** ويتم تشغيل المعلمة **حظر الترحيل والإرسال إلى سير العمل** في الصفحة **معلمات الحسابات الدائنة**.

## <a name="matching-vendor-invoices-to-product-receipts"></a>مطابقة فواتير الموردين بإيصالات استلام المنتجات

يمكنك إدخال معلومات عن فواتير الموردين وحفظها، كما يمكنك مطابقة بنود الفاتورة مع بنود إيصال استلام المنتجات. يمكنك أيضًا مطابقة الكميات الجزئية للبند.

يمكنك إنشاء فاتورة مورد استنادًا إلى أصناف بند إيصال استلام المنتجات التي تم استلامها حتى التاريخ الحالي، حتى ولو كان جميع الأصناف الخاصة بأمر شراء معين لم يتم استلامها بعد. على سبيل المثال، يمكنك استخدام هذا الخيار إذا أرسل المورد فاتورة واحدة كل شهر تغطي جميع التسليمات التي تم شحنها خلال ذلك الشهر. يمثل كل إيصال استلام منتجات تسليمًا جزئيًا أو كاملاً للأصناف الواردة في أمر الشراء.

عندما تكون الفاتورة في سير العمل، يمكن للمعتمد تحديث كميات الفواتير بحيث تتطابق مع القيمة الموجودة في حقل **كمية إيصالات استلام المنتجات التي ستتم مطابقتها**. للقيام بذلك ، حدد الميزة **تحديث كميات الفواتير لمطابقة كميات إيصالات المنتجات في سير العمل**  في مساحة عمل **إدارة الميزات** وحدد **تمكين**. إذا قام أحد المعتمدين في عملية سير العمل بإزالة كافة المطابقات من كافة إيصالات المنتجات من بند الفاتورة، فسيتم حذف بند الفاتورة. في حالة عدم تمكين هذه الميزة، لا يتم تحديث كميات الفواتير الخاصة بالفواتير في سير العمل.

وعند ترحيل الفاتورة، يتم تحديث كمية **باقي الفاتورة** لكل صنف بإجمالي الكميات المستلمة من إيصالات استلام المنتجات المحددة. وإذا كان كلُّ من كمية **باقي الفاتورة** وكمية **تسليم البافي** لكافة الأصناف في أمر الشراء تساوي 0 (صفر)، فإنه يتم تغيير حالة أمر الشراء إلى **مفوتر**. وإذا كانت كمية **باقي الفاتورة** لا تساوي 0 (صفر)، فإن حالة أمر الشراء تبقى دون تغيير، ويمكن إدخال الفواتير الإضافية لها.

يفترض هذا الخيار أن يتم ترحيل إيصال استلام منتجات واحد على الأقل لأمر الشراء. تعتمد فاتورة المورد على إيصالات الاستلام هذه ويعكس الكميات من خلالها. وتعتمد المعلومات المالية للفاتورة على المعلومات التي يتم إدخالها عند ترحيلك للفاتورة.

لمزيد من المعلومات، راجع [تسجيل فاتورة المورّد ومطابقتها بالكمية المستلمة](../accounts-payable/tasks/record-vendor-invoice-match-against-received-quantity.md).

## <a name="configure-an-automated-task-for-vendor-invoice-workflow-to-post-the-vendor-invoice-using-a-batch-job"></a>تكوين مهمة مؤتمتة لسير عمل فاتورة المورد لترحيل فاتورة المورد باستخدام وظيفة دفعية

يمكن إضافة مهمة ترحيل مؤتمتة إلى سير عمل فاتورة المورد بحيث تتم معالجة الفواتير بطريقة دفعية. تسمح عملية ترحيل الفواتير بطريقة دفعية بمتابعة عملية سير العمل من دون الحاجة إلى الانتظار ريثما ينتهي الترحيل، مما يؤدي إلى تحسين الأداء الإجمالي لكافة المهام التي تم إرسالها إلى سير العمل.

لترحيل فاتورة مورد بطريقة دفعية، في صفحة **إدارة الميزات**، قم بتشغيل المعلمة **ترحيل دفعة فاتورة المورد‬**. يتم تكوين عمليات سير عمل فاتورة المورد بالانتقال إلى **حسابات دائنة > الإعداد > عمليات سير عمل الحسابات الدائنة**.

يمكنك رؤية المهمة **ترحيل فاتورة المورد باستخدام دفعة‬** في محرر سير العمل، بصرف النظر عما إذا تم تمكين معلمة الميزة **ترحيل دفعة فاتورة المورد**. إذا لم يتم تمكين معلمة الميزة، لن تتم معالجة فاتورة تحتوي على المعلمة **ترحيل فاتورة المورد باستخدام وظيفة دفعية** في سير العمل حتى يتم تمكين المعلمة. يجب عدم استخدام المهمة **ترحيل فاتورة المورد باستخدام دفعة** في سير العمل نفسه للمهمة المؤتمتة **ترحيل فواتير المورِد**. كما يجب أن تكون المهمة **ترحيل فاتورة المورد باستخدام دفعة‬‏‫** العنصر الأخير في تكوين سير العمل.

يمكنك تحديد عدد الفواتير التي سيتم تضمينها في الدفعة وعدد الساعات التي سيتم انتظارها قبل إعادة جدولة دفعة بالانتقال إلى **حسابات دائنة > الإعداد > معلمات الحسابات الدائنة > الفاتورة > سير عمل الفاتورة**. 

## <a name="working-with-multiple-invoices"></a>العمل مع العديد من الفواتير

يمكنك العمل على فواتير متعددة في الوقت نفسه وترحيلها جميعًا في الوقت نفسه. إذا احتجت إلى إنشاء فواتير متعددة، فاستخدم صفحة **فواتير المورد المعلقة**. وإذا كان يجب عليك ترحيل وطباعة فواتير موردين متعددة، فاستخدم **دفتر يومية اعتماد الفاتورة**. وإذا كنت تستخدم **دفتر يومية اعتماد الفاتورة**، فيجب ترحيل إيصال استلام منتج واحد على الأقل لطلب الشراء وترحيل فاتورة لأمر الشراء في سجل الفاتورة. ترد المعلومات المالية الخاصة بالفاتورة من الفاتورة التي تم ترحيلها في السجل.

## <a name="recovering-vendor-invoices-that-are-being-used"></a>استرداد فواتير المورّد قيد الاستخدام

أثناء استخدام فاتورة مورّد، لا يمكن تحريرها بواسطة مستخدم آخر. ومع ذلك، بإمكان حالة الفاتورة أن تشير في بعض الأحيان إلى أن الفاتورة قيد الاستخدام، على الرغم من عدم تحريرها بطريقة نشطة. على سبيل المثال، من المحتمل أن يكون التطبيق قد توقف عن الاستجابة أثناء تحرير الفاتورة، أو أن أحد المستخدمين ترك الفاتورة مفتوحة في التطبيق عن غير قصد.

يمكنك استخدام الصفحة **استرداد فواتير المورّد** لاسترداد أو إصدار فواتير المورّد التي كانت قيد الاستخدام لمدة تزيد عن أربع ساعات، بحيث يمكن تحريرها. يمكنك فتح هذه الصفحة من بنية تنقل **المهمة الدورية** أو لوحة في مساحة العمل **إدخال فاتورة المورّد**. ستكون الفاتورة متوفرة للتحرير في صفحة **فاتورة المورّد**، بعد استردادها.

يمكنك الوصول إلى الصفحة **استرداد فواتير المورّد** فقط إذا كانت مهمة وامتياز الأمان **استرداد فواتير المورّد قيد الاستخدام‬** معينة لك. بالإضافة إلى ذلك، يجب أن تكون المعلمة **السماح باسترداد فاتورة المورّد** في صفحة **محددات الحسابات الدائنة‬** قيد التشغيل.

## <a name="resetting-the-workflow-status-for-vendor-invoices-from-unrecoverable-to-draft"></a>إعادة تعيين حالة سير العمل لفواتير المورد من غير القابل للاسترداد إلى المسودة

سيكون لمثيل سير العمل الذي توقف بسبب خطأ لا يمكن إصلاحه حالة سير العمل **غير قابل للاسترداد**. عندما تكون حالة سير عمل فاتورة المورد **غير قابلة للاسترداد**، يمكنك تعيينها إلى **مسودة** عن طريق تحديد **استدعاء**. يمكنك تحرير فاتورة المورّد بعد ذلك. تتوفر هذه الميزة في حالة تشغيل معلمة **إعادة تعيين حالة سير عمل فواتير المورد من غير قابل للاسترداد إلى المسودة** في صفحة **إدارة الميزات**.

يمكنك استخدام صفحة **محفوظات سير العمل** لإعادة تعيين حالة سير العمل إلى **مسودة**. يمكنك فتح هذه الصفحة من **فاتورة المورّد** أو من جزء التنقل **عام > استعلامات > سير العمل**. لإعادة تعيين حالة سير العمل إلى **مسودة**، حدد **استدعاء**. يمكنك أيضًا إعادة تعيين حالة سير العمل إلى "مسودة" عن طريق تحديد الإجراء **استدعاء** في صفحة **فاتورة المورّد** أو صفحة **فواتير المورّد‏‎ المعلقة**. بعد إعادة تعيين حالة سير العمل إلى **مسودة**، تصبح متوفرة للتحرير في صفحة **فاتورة المورد**.

## <a name="viewing-the-invoice-total-on-the-pending-vendor-invoices-page"></a>عرض إجمالي الفاتورة في الصفحة "فواتير المورد المعلقة"

يمكنك عرض إجمالي الفاتورة في الصفحة **فواتير المورد المعلقة** عن طريق تمكين المعلمة **عرض إجمالي فاتورة في قائمة فواتير المورد المعلقة** في الصفحة **معلمات الحسابات الدائنة**. 

## <a name="vendor-open-transactions-report"></a>تقرير حركات المورّد المفتوحة

يقدم تقرير **الحركات المفتوحة للمورد** معلومات تفصيليه حول الحركات المفتوحة لكل مورد اعتبارا من التاريخ الذي تقوم بتحديده. وغالبا ما يتم استخدام هذا التقرير اثناء اجراء المراجعة للتحقق من الارصده بين حركات دفتر المورد وحركات حساب دفتر الأستاذ.

بالنسبة لكل حركه ، يتضمن التقرير التفاصيل التالية:

- رقم الفاتورة
- تاريخ الحركة
- رقم الإيصال
- مبلغ الحركة بعمله الحركة وعمله المحاسبة
- رصيد الائتمان بعمله الحركة وعمله المحاسبة
- رصيد المدين بعمله الحركة وعمله المحاسبة
- مبلغ الإجمالي الفرعي بعملة المحاسبة.
- تاريخ استحقاق الدفع

### <a name="filter-the-data-on-the-report"></a>تصفية البيانات المعروضة في التقرير

عند إنشاء التقرير **الحركات المفتوحة للمورد**، تظهر المعلمات الافتراضية التالية. يمكنك استخدامها لتصفية البيانات المضمنة في التقرير.

- **استبعاد التسوية المستقبلية** - حدد خانه الاختيار هذه لاستبعاد الحركات التي تمت تسويتها بعد التاريخ الذي تم إدخاله في الحقل **الحركات المفتوحة لكل**.
- **الحركات المفتوحة لكل** – ادخل تاريخا لتضمين الحركات المفتوحة بدءا من ذلك التاريخ. في حاله عدم إدخال تاريخ ، يتم تعيين هذا الحقل علي الحد الأقصى للتاريخ. (يكون الحد الأقصى للتاريخ هو آخر تاريخ يقبله النظام ، 31 ديسمبر 2154.) وبشكل افتراضي ، في المرة التالية التي يتم فيها تشغيل التقرير ، يتم تعيين هذا الحقل لأخر تاريخ تم إدخاله فيه.

يمكنك استخدام عوامل التصفية الموجودة ضمن الحقل **السجل لتضمين** لمزيد من الحد من بيانات الحركات المضمنة في التقرير.

## <a name="additional-resources"></a>الموارد الإضافية

- [إعداد سياسات فواتير المورِّدين](../accounts-receivable/tasks/set-up-vendor-invoice-policies.md)
- [بيانات الفاتورة الرئيسية في نظام الحسابات الدائنة باستخدام فاتورة المورد](tasks/key-invoice-data-ap-system-vendor-invoice.md)
- [بيانات الفاتورة الرئيسية في الحسابات الدائنة باستخدام ‏‫دفتر يومية الموافقة](tasks/key-invoice-data-into-ap-system-approval-journal.md)
- [بيانات الفاتورة الرئيسية في نظام الحسابات الدائنة باستخدام ‏‫وعاء الفواتير‬](tasks/key-invoice-data-into-ap-system-invoice-pool.md)
- [تسجيل فاتورة مورّد في دفتر يومية الفواتير](tasks/record-vendor-invoice-invoice-journal.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
