---
title: لماذا لا يمكنني عكس هذه المعاملة؟
description: تصف هذه المقالة الأسباب المختلفة التي يتعذر من خلالها عكس المعاملات. كما يسرد حلول لهذه المشكلة.
author: kweekley
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-07-21
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9a8b26584b1a9b82440583db693cd14daa580e22
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876171"
---
# <a name="why-cant-i-reverse-this-transaction"></a>لماذا لا يمكنني عكس هذه المعاملة؟

[!include [banner](../includes/banner.md)]

تصف هذه المقالة الأسباب المختلفة التي يتعذر من خلالها عكس المعاملات. كما يسرد حلول لهذه المشكلة.

## <a name="symptom"></a>العَرَضْ

قد تواجه المؤسسات حالات حيث يجب عكس حركة قاموا بنشرها. في بعض الأحيان، سيمنعهم النظام من عكس هذه المعاملات. يمكن أن يطالب هذا السلوك سؤالين:

- لماذا لا يمكنني عكس المعاملة؟
- كيف تؤثر ميزة انعكاس الكتلة على هذا السلوك؟

## <a name="resolution"></a>الحل

يجب أن تستوفي المعاملات معايير محددة قبل أن يمكن عكسها. توفر المقاطع المتبقية من هذه المقالة التحقق من صحة كل وحدة نمطية. بالرغم من تركيز هذه المقالة على المعاملات في Microsoft Dynamics 365 Finance، يمكن تطبيق بعض المفاهيم والتحقق من الصحة على تطبيقات أخرى، مثل Dynamics 365 Supply Chain Management.

بالإضافة إلى ذلك، قد يؤثر المكان الذي يتم عكس الحركة فيه على ما إذا كان يمكن عكسها. على سبيل المثال، يمكن عكس دفع المورد الذي يتم ترحيلها كشيك فقط من قسم **الشيكات** في صفحة الحركة للحسابات البنكية. لا يمكن عكسه من صفحة **حركات الإيصال** في دفتر الأستاذ العام.

إذا تم تشغيل ميزة **عكس شامل مستندات متعددة** (تعرف أيضا باسم ميزة العكس الشامل) في مساحة عمل **إدارة الميزات**، فإنه يؤثر على عدد المعاملات التي يمكن عكسها ومكان عكسها. توفر هذه الميزة ميزتين عند تشغيلها:

- بالنسبة لبعض أنواع الحركات، يمكن تحديد أكثر من حركة واحدة في المرة الواحدة وعكسها من دفتر اليومية الذي تم ترحيلها منه، أو من صفحة **حركات الإيصال**. ومع ذلك، يجب أن تكون الحركات الفردية قابلة للعكس قبل تشغيل الميزة. قبل تقديم هذه الميزة، كان لا بد من عكس المعاملات واحدة في كل مرة.
- يمكن عكس *بعض* حركات دفتر الأستاذ الفرعي من دفتر اليومية (دفتر اليومية العام) أو صفحة **حركات الإيصال**. ليس من الضروري عكسها من صفحة دفتر الأستاذ الفرعي. على سبيل المثال، يمكن في السابق عكس دفتر يومية فاتورة المورد فقط من صفحة **حركات المورد**. ومع ذلك، يمكن الآن عكسه من جانب دفتر الأستاذ العام أيضا، من دفتر اليومية أو صفحة **حركات الإيصال**. يشرح كل قسم من هذه المقالة أنواع الحركات التي لا تنطبق عليها هذه الميزة.

**لا** تمكن ميزة العكس الشامل من عكس المزيد من أنواع المعاملات. إذا تعذر عكس نوع الحركة مسبقا، فلا يزال يتعذر عكسه بعد تشغيل الميزة. على سبيل المثال، لا يمكن عكس فواتير مورد أمر الشراء، بغض النظر عما إذا كانت ميزة الإلغاء الشامل قيد التشغيل أم لا.

لمزيد من المعلومات حول ميزة العكس الشامل، راجع [عكس ترحيل دفتر اليومية](reverse-journal-posting.md).

## <a name="general-ledger"></a>دفتر الأستاذ العام

يتم إدخال تعديلات دفتر الأستاذ العام فقط باستخدام حسابات دفتر الأستاذ. لذلك، تحديث دفتر الأستاذ العام فقط.

إذا تم إيقاف تشغيل ميزة العكس الشامل، يمكن عكس معظم تعديلات دفتر الأستاذ العام بشكل فردي من صفحة **حركات \<main account\>** لدفتر الأستاذ (**LedgerTransAccount**). (يختلف العنوان الدقيق للصفحة، وفقا للحساب الرئيسي المحدد.) تعرض الصفحة كل حركة تم ترحيلها إلى الحساب الرئيسي. يتم فتحه عادة من صفحة **قائمة رصيد المراجعة**، أو عن طريق تحديد **الحركات** في صفحة **حركات الإيصال**.

إذا تم تشغيل ميزة إلغاء الكتلة، يمكن الآن عكس إيصال دفتر الأستاذ العام أو أكثر من صفحة **حركات الإيصال**، ومن دفتر اليومية الذي تم ترحيل الحركة منه. الاستثناءات هي إعادة تقييم العملة الأجنبية لدفتر الأستاذ العام، والدمج، وحركات إقفال نهاية السنة. يتم عكس هذه الحركات من الصفحات التي تم تشغيل إغلاق نهاية السنة منها.

### <a name="reasons-why-transactions-cant-be-reversed"></a>أسباب تعذر عكس المعاملات

لا يمكن عكس الحركات للأسباب التالية:

- دفتر اليومية العام:

    - الفترة المالية معلقة أو مغلقة بشكل دائم:

        - إذا كان تاريخ التراجع في فترة مالية غير مفتوحة، فلا يمكن عكس الحركة.
        - إذا كانت الحركة تدعم إدخال تاريخ عكس، يمكن عكس الحركة عن طريق تغيير تاريخ الإلغاء إلى فترة مفتوحة.

    - تم تشغيل عملية إغلاق نهاية العام:

        - تاريخ المحاسبة للحركة هو في السنة المالية التي تم من خلال إغلاق نهاية السنة. على الرغم من أن الفترة في السنة المالية قد تظل مفتوحة، إلا أنه لا يمكن عكس الحركة إذا تم تشغيل عملية إغلاق نهاية السنة للسنة المالية. السنة المالية لها حالة مختلفة عن الفترات التي فيها.
        - يمكن عكس إغلاق نهاية السنة، ومن ثم يمكن عكس الحركة. وقد لا يكون هذا النهج خيارا. قد يكون من الأسهل إدخال حركة معكوسة يدويا في فترة مفتوحة إما للسنة المالية المغلقة أو السنة المالية التالية، اعتمادا على حالة عملية الإغلاق المالي. إذا تم ترحيل حركة جديدة إلى فترة مفتوحة من السنة المالية التي تم من خلال عملية إغلاق نهاية السنة، يجب تشغيل إغلاق نهاية السنة مرة أخرى.

    - إن عكس الحركة قيد التنفيذ بالفعل:

        - إذا كانت الحركة قيد التراجع، يجب إكمال هذه العملية. لا يمكن القيام بعملية عكس منفصلة. 
        - بعد اكتمال الإلغاء، يمكن عكس الحركة المعكوسة مرة أخرى (أي يمكن عكس الإلغاء).

    - تسوية دفتر الأستاذ:

        - إذا تمت تسوية سطر أو أكثر من الحركة باستخدام المهمة الدورية **تسويات دفتر الأستاذ** (**دفتر الأستاذ العام \> المهام الدورية \> تسويات دفتر الأستاذ**)، بحيث يكون السجل موجودا في جدول LedgerTransSettlement، فلا يمكن عكس الحركة.
        - يمكن عكس تسوية دفتر الأستاذ، ومن ثم يمكن عكس الإيصال.

    - بين شركات شقيقة:

        - إذا كانت الحركة عبارة عن حركة بين الشركات الشقيقة، فلا يمكن عكسها.
        - الحركة **ليست** حركة بين الشركات الشقيقة، ولكن يتم ترحيلها إلى حساب رئيسي "مستحق" أو "مستحق من" تم تعريفه في صفحة **الإعداد بين الشركات الشقيقة**.

    - الاستحقاقات:

        - إذا تم عكس إيصال دفتر الأستاذ العام المستحق، سيتم عكس الإدخال المستحق وكافة حركات الاستحقاق الفرعية المقابلة.
        - لا يمكن عكس الحركات الفرعية الفردية للتراكم.

- دفتر يومية إقرار الإيرادات:

    - تعذر عكس إقرار الإيرادات.
    - عندما يتم التعرف على الإيراد من خلال دفتر يومية إقرار الإيراد، يتم ترحيل الإيصال فقط إلى حسابات دفتر الأستاذ. لذلك، في صفحات مثل **حركات الإيصال**، تظهر الحركات كما لو كانت إدخالات دفتر الأستاذ العام فقط.

- إعادة تقييم العملة الأجنبية:

    - يمكن عكس حركات إعادة تقييم العملات الأجنبية، ولكن فقط من صفحة **إعادة تقييم العملة الأجنبية** في دفتر الأستاذ العام التي تم تشغيل إعادة التقييم منها.
    - لا يمكن إكمال الإلغاء إلا إذا تم ترحيلها إلى فترة مالية مفتوحة.

- توحيد:

    - يمكن عكس حركات التوحيد، ولكن فقط من صفحة **حركات التوحيد**.
    - لا يمكن إكمال الإلغاء إلا إذا تم ترحيلها إلى فترة مالية مفتوحة.

- إقفال نهاية السنة:

    - يمكن عكس حركات إقفال نهاية السنة (حركات الإغلاق والفتح) بهذه الطرق:

        - إذا تم إيقاف تشغيل ميزة تحسينات إقفال نهاية السنة لدفتر الأستاذ العام، حدد الخيار **التراجع عن الإغلاق السابق** في مربع الحوار **إغلاق نهاية السنة**.
        - إذا تم تشغيل ميزة تحسينات نهاية السنة لدفتر الأستاذ العام، حدد سجلات الشركة والسنة المالية التي تم إنشاؤها لإغلاق نهاية السنة في صفحة **إغلاق نهاية السنة**، ثم حدد **عكس إغلاق نهاية السنة**.

    - لاحظ أن عكس إغلاق نهاية السنة يحذف حركات الإغلاق والفتح فعليا. لا يتم ترحيل الإيصال المعكوس أبدا.

## <a name="accounts-payable"></a>الحسابات الدائنة

تقوم أنواع متعددة من الحركات بتحديث دفتر الأستاذ الفرعي للحسابات الدائنة. وتشمل الأمثلة فواتير المورد ودفاتر يومية فواتير المورد وتقارير المصروفات.

إذا تم إيقاف تشغيل ميزة إلغاء الكتلة، يمكن عكس الحركات بشكل فردي من صفحة **حركات المورد** للفواتير أو صفحة **الحساب البنكي** لمدفوعات الشيكات.

إذا تم تشغيل ميزة الإلغاء الشامل، يمكن الآن عكس حركات الحسابات الدائنة أو أكثر من صفحة **حركات الإيصال**، ومن دفتر اليومية الذي تم ترحيل الحركة منه. ومع ذلك، لا يزال يمكن عكس مدفوعات المورد فقط من الحساب البنكي. بالإضافة إلى ذلك، لا يمكن عكس حركات المورد من صفحة **حركات \<main account\>** لدفتر الأستاذ. يمكن عكسها فقط من صفحة **حركات الإيصال**.

لاحظ أنه لا يمكن عكس بعض المعاملات على الإطلاق. وتشمل الأمثلة فواتير مورد أمر الشراء ومدفوعات المورد الإلكترونية.

### <a name="reasons-why-vouchers-cant-be-reversed"></a>أسباب تعذر عكس الإيصالات

لا يمكن عكس الإيصالات للأسباب التالية:

- الفترة المالية معلقة أو مغلقة:

    - إذا كان تاريخ التراجع في فترة مالية غير مفتوحة، فلا يمكن عكس الحركة.
    - إذا كانت الحركة تدعم إدخال تاريخ عكس، يمكن عكس الحركة عن طريق تغيير تاريخ الإلغاء إلى فترة مفتوحة.

- تم تشغيل عملية إغلاق نهاية العام لدفتر الأستاذ العام:

    - تاريخ المحاسبة للحركة هو في السنة المالية التي تم من خلال إغلاق نهاية السنة في دفتر الأستاذ العام. على الرغم من أن الفترة في السنة المالية قد تظل مفتوحة، إلا أنه لا يمكن عكس الحركة إذا تم تشغيل عملية إغلاق نهاية السنة للسنة المالية. السنة المالية لها حالة مختلفة عن الفترات التي فيها.
    - يمكن عكس إغلاق نهاية السنة، ومن ثم يمكن عكس الحركة. وقد لا يكون هذا النهج خيارا. قد يكون من الأسهل إدخال حركة معكوسة يدويا في فترة مفتوحة إما للسنة المالية المغلقة أو السنة المالية التالية، اعتمادا على حالة عملية الإغلاق المالي. إذا تم ترحيل حركة جديدة إلى فترة مفتوحة من السنة المالية التي تم من خلال عملية إغلاق نهاية السنة، يجب تشغيل إغلاق نهاية السنة مرة أخرى.

- لم يتم تحويل إدخال دفتر يومية دفتر الأستاذ الفرعي إلى دفتر الأستاذ العام:

    - ينطبق هذا السبب فقط على فواتير المورد غير أمر الشراء.
    - استخدم صفحة **إدخالات دفتر يومية بدفتر الأستاذ الفرعي التي لم يتم تحويلها بعد** لنقل الإدخال إلى دفتر الأستاذ العام. يمكن بعد ذلك عكس فاتورة المورد غير أمر الشراء من صفحة **حركات المورد**.

- التسوية:

    - تتم تسوية الحركة (مثل فاتورة أو دفع) أو وضع علامة للتسوية.

        - يمكنك التحقق مما إذا كانت الحركة قد تمت تسويتها أو تم وضع علامة للتسوية من خلال تحديد **عرض التسويات** أو **التسوية \> سجل التسوية** في صفحة **حركات المورد**.
        - يمكنك أيضا عكس تسوية من صفحة **حركات المورد** (**تسوية \> التراجع عن التسوية**) إذا كان يجب عكس إحدى الحركات.

- يحتوي الإيصال على أكثر من حركة دفتر الأستاذ الفرعي التي تم إدخالها باستخدام رقم الإيصال نفسه (إصدار إيصال واحد).
- لم تتم الموافقة على الفاتورة:

    - إذا لم يتم تحديد خانة الاختيار **الموافقة** في الفاتورة، فلا يمكن عكس الفاتورة.

        - في هذه الحالة، لا تشير الموافقة إلى الموافقات في عملية سير العمل، بل إلى خيار **الموافقة** على الفاتورة. يستخدم هذا الخيار لمنع دفع فاتورة. يتم استخدامه عادة لفواتير سجل فواتير المورد.

- الحركة في وعاء الفواتير:

    - لا يمكن عكس فاتورة في التجمع مباشرة من صفحة **حركات المورد**. بدلا من ذلك، يجب عكسه من خلال عملية الإلغاء في صفحة **دفتر يومية الموافقة على الفاتورة**.

- تحتوي الحركة على فاتورة أصل تم تصحيحها (التعريب الهندي).
- الحركة لها حالة تفويض **الفاتورة المحولة**.
- يتم استخدام الحركة لتسوية ضريبة جزئية.
- تحتوي الحركة على حساب مورد ولكن يتم عكسها من صفحة غير صحيحة، مثل للصفحة **الحركات \<main account\>**:

    - كما يوحي هذا السبب، حتى عند تشغيل ميزة الانتكاسات الشامل، يمكن عكس بعض معاملات دفتر الأستاذ الفرعي فقط من صفحات معينة.

### <a name="types-of-transactions-that-cant-be-reversed"></a>أنواع الحركات التي لا يمكن عكسها

لا يمكن عكس الأنواع التالية للحركات:

- إعادة تقييم العملة الأجنبية:

    - على عكس إعادة تقييم العملة الأجنبية في دفتر الأستاذ العام، لا يمكن عكس الحسابات المدينة وإعادة تقييم الحسابات المستحقة الدفع بالعملات الأجنبية. بدلا من ذلك، يجب تشغيل إعادة التقييم مرة أخرى باستخدام تاريخ الفاتورة. في هذه الحالة، تستخدم إعادة التقييم سعر الصرف من تاريخ الفاتورة، وترفع بشكل أساسي الربح أو الخسارة غير المحققة إلى 0 (صفر). ولذلك، تشبه النتيجة نتيجة عكس إعادة التقييم السابقة. ومع ذلك، لاحظ أنه لن يتم عكس نفس المبلغ إذا تم تغيير سعر الصرف الافتراضي في الفاتورة.

- فاتورة مورد أمر الشراء:

    - يجب إنشاء إشعار دائن لعكس فاتورة المورد. لمزيد من المعلومات حول كيفية إنشاء حركة معكوسة، راجع [إنشاء أمر إرجاع شراء](../../supply-chain/procurement/tasks/create-purchase-return-order.md).

- سند إذني
- خطاب اعتماد البنك لشحنة التصدير

## <a name="accounts-receivable"></a>الحسابات المدينة

تقوم أنواع متنوعة من الحركات بتحديث دفاتر الأستاذ الفرعي للحسابات المدينة. وتشمل الأمثلة فواتير العملاء من أوامر التوريد وفواتير العملاء التي يتم إدخالها من خلال دفتر اليومية العام وفواتير النص الحر ومدفوعات العملاء والشطب.

إذا تم إيقاف تشغيل ميزة الإلغاء الشامل، يمكن عكس الحركات بشكل فردي من صفحة **حركات العميل** للفواتير أو صفحة **الحسابات البنكية** لمدفوعات الشيكات. للحصول على معلومات عن كيفية عكس الدفع، راجع [قسم إدارة النقد والبنوك](cant-reverse-transctns.md#cash-and-bank-management) لاحقًا في هذه المقالة.

إذا تم تشغيل ميزة الإلغاء الشامل، يمكن الآن عكس حركات الحسابات المدينة أو أكثر من صفحة **حركات الإيصال**، ومن دفتر اليومية الذي تم ترحيل الحركة منه. ومع ذلك، لا يزال من الممكن عكس الودائع فقط من الحساب المصرفي، ويمكن عكس الفواتير النصية المجانية فقط من الصفحة الأصلية (إذا تم تشغيل الميزة التي تسمح بالتصحيحات). بالإضافة إلى ذلك، لا يمكن عكس حركات العميل من صفحة **حركات \<main account\>** لدفتر الأستاذ. لكن يمكن عكسها فقط من صفحة **حركات الإيصال**.

لاحظ أنه لا يمكن عكس بعض المعاملات على الإطلاق. وتشمل الأمثلة فواتير العملاء أمر التوريد والشطب.

### <a name="reasons-why-transactions-cant-be-reversed"></a>أسباب تعذر عكس المعاملات

لا يمكن عكس الحركات للأسباب التالية:

- الفترة المالية معلقة أو مغلقة بشكل دائم:

    - إذا كان تاريخ التراجع في فترة مالية غير مفتوحة، فلا يمكن عكس الحركة.
    - إذا كانت الحركة تدعم إدخال تاريخ عكس، يمكن عكس الحركة عن طريق تغيير تاريخ الإلغاء إلى فترة مفتوحة.

- تم تشغيل عملية إغلاق نهاية العام لدفتر الأستاذ العام:

    - تاريخ المحاسبة للحركة هو في السنة المالية التي تم من خلال إغلاق نهاية السنة لدفتر الأستاذ العام. على الرغم من أن الفترة في السنة المالية قد تظل مفتوحة، إلا أنه لا يمكن عكس الحركة إذا تم تشغيل عملية إغلاق نهاية السنة للسنة المالية. السنة المالية لها حالة مختلفة عن الفترات التي فيها.
    - يمكن عكس إغلاق نهاية السنة، ومن ثم يمكن عكس الحركة. وقد لا يكون هذا النهج خيارا. قد يكون من الأسهل إدخال حركة معكوسة يدويا في فترة مفتوحة إما للسنة المالية المغلقة أو السنة المالية التالية، اعتمادا على حالة عملية الإغلاق المالي. إذا تم ترحيل حركة جديدة إلى فترة مفتوحة من السنة المالية التي تم من خلال عملية إغلاق نهاية السنة، يجب تشغيل إغلاق نهاية السنة مرة أخرى.

- لم يتم تحويل إدخال دفتر يومية دفتر الأستاذ الفرعي إلى دفتر الأستاذ العام:

    - ينطبق هذا السبب فقط على فواتير النص الحر.
    - استخدم صفحة **إدخالات دفتر يومية بدفتر الأستاذ الفرعي التي لم يتم تحويلها بعد** لنقل الإدخال إلى دفتر الأستاذ العام. يمكن بعد ذلك عكس فاتورة النص الحر أو تصحيحها إذا تم تمكين وظيفة التصحيحات.

- التسوية:

    - تتم تسوية الحركة (مثل فاتورة أو دفع) أو وضع علامة للتسوية.

        - يمكنك التحقق مما إذا كانت الحركة قد تمت تسويتها أو تم وضع علامة للتسوية من خلال تحديد **عرض التسويات** أو **التسوية \> سجل التسوية** في صفحة **حركات العميل**.
        - يمكنك أيضا عكس تسوية من صفحة **حركات العميل** (**تسوية \> التراجع عن التسوية**) إذا كان يجب عكس إحدى الحركات.

- تحتوي المعاملة على أكثر من حركة دفتر الأستاذ الفرعي التي تم إدخالها باستخدام رقم الإيصال نفسه (إصدار إيصال واحد).
- لم تتم الموافقة على الفاتورة:

    - إذا لم يتم تحديد خانة الاختيار **الموافقة** في الفاتورة، فلا يمكن عكس الفاتورة.

        - في هذه الحالة، لا تشير الموافقة إلى الموافقات في عملية سير العمل، بل إلى خيار **الموافقة** على الإيصال. يستخدم هذا الخيار لمنع دفع فاتورة. على الرغم من أن هذا الخيار يستخدم عادة في الحسابات الدائنة، إلا أنه متوفر أيضا لفواتير الحسابات المدينة التي يتم إدخالها من خلال دفاتر اليومية.

- تحتوي الحركة على فاتورة أصل تم تصحيحها (التعريب الهندي).
- تحتوي الحركة على حساب عميل ولكن يتم عكسها من صفحة غير صحيحة، مثل للصفحة **الحركات \<main account\>**:

    - كما يوحي هذا السبب، حتى عند تشغيل ميزة الانتكاسات الشامل، يمكن عكس بعض معاملات دفتر الأستاذ الفرعي فقط من صفحات معينة.

### <a name="types-of-transactions-that-cant-be-reversed"></a>أنواع الحركات التي لا يمكن عكسها

لا يمكن عكس الأنواع التالية للحركات:

- إعادة تقييم العملة الأجنبية:

    - على عكس إعادة تقييم العملة الأجنبية في دفتر الأستاذ العام، لا يمكن عكس الحسابات المدينة وإعادة تقييم الحسابات المستحقة الدفع بالعملات الأجنبية. بدلا من ذلك، يجب تشغيل إعادة التقييم مرة أخرى باستخدام تاريخ الفاتورة. في هذه الحالة، تستخدم إعادة التقييم سعر الصرف من تاريخ الفاتورة، وترفع بشكل أساسي الربح أو الخسارة غير المحققة إلى 0 (صفر). ولذلك، تشبه النتيجة نتيجة عكس إعادة التقييم السابقة. ومع ذلك، لاحظ أنه لن يتم عكس نفس المبلغ إذا تم تغيير سعر الصرف الافتراضي في الفاتورة.

- حركة تم ضبط اقتطاع الضريبة عليها
- فاتورة العميل لأمر المبيعات:

    - يجب إنشاء إشعار دائن أو عائد لعكس الحركة. للحصول على معلومات حول كيفية إنشاء الحركة المعكوسة، راجع [عوائد المبيعات](../../supply-chain/warehousing/sales-returns.md).

- الكمبيالة
- تسجيل حركات النقد
- تعديل متقدم
- إشعار الفائدة
- خطاب التحصيلات
- خطاب اعتماد البنك
- شحنة التصدير
- دفتر يومية إقرار الإيرادات:

    - عندما يتم التعرف على الإيراد من خلال دفتر يومية إقرار الإيراد، يتم ترحيل الإيصالات فقط إلى حسابات دفتر الأستاذ. لذلك، تظهر كما لو كانت إدخالات دفتر الأستاذ العام فقط. لا يمكن عكس هذه الإدخالات، لأنه لن يتم إعادة فتح جدول الإيرادات للتعرف على الأرباح مرة أخرى.

## <a name="cash-and-bank-management"></a>إدارة النقد والبنوك

تقوم عدة أنواع من الحركات بتحديث دفتر الأستاذ الفرعي للبنك من خلال دفتر اليومية العام. وتشمل الأمثلة مدفوعات المورد ومدفوعات العملاء والتحويلات المصرفية.

إذا تم إيقاف تشغيل ميزة الإلغاء الشامل، يمكن عكس الحركات بشكل فردي من صفحة **الحسابات البنكية** للشيكات والإيداعات أو من صفحة **حركات العميل** لمدفوعات العميل.

إذا تم تشغيل ميزة الإلغاء الشامل، يمكن الآن عكس حركات المدفوعات أو أكثر من صفحة **حركات الإيصال**، ومن دفتر اليومية الذي تم ترحيل الحركة منه. ومع ذلك، لا يزال يمكن عكس الإيداعات فقط من الحساب البنكي. بالإضافة إلى ذلك، لا يمكن عكس حركات البنك من صفحة **حركات \<main account\>** لدفتر الأستاذ. لكن يمكن عكسها فقط من صفحة **حركات الإيصال**.

لاحظ أنه لا يمكن عكس بعض المعاملات على الإطلاق. وتشمل الأمثلة مدفوعات المورد الإلكترونية.

### <a name="reasons-why-transactions-cant-be-reversed"></a>أسباب تعذر عكس المعاملات

لا يمكن عكس الحركات للأسباب التالية:

- الفترة المالية معلقة أو مغلقة بشكل دائم:

    - إذا كان تاريخ التراجع في فترة مالية غير مفتوحة، فلا يمكن عكس الحركة.
    - إذا كانت الحركة تدعم إدخال تاريخ عكس، يمكن عكس الحركة عن طريق تغيير تاريخ الإلغاء إلى فترة مفتوحة.

- تم تشغيل عملية إغلاق نهاية العام لدفتر الأستاذ العام:

    - تاريخ المحاسبة للحركة هو في السنة المالية التي تم من خلال إغلاق نهاية السنة لدفتر الأستاذ العام. على الرغم من أن الفترة في السنة المالية قد تظل مفتوحة، إلا أنه لا يمكن عكس الحركة إذا تم تشغيل عملية إغلاق نهاية السنة للسنة المالية. السنة المالية لها حالة مختلفة عن الفترات التي فيها.
    - يمكن عكس إغلاق نهاية السنة، ومن ثم يمكن عكس الحركة. وقد لا يكون هذا النهج خيارا. قد يكون من الأسهل إدخال حركة معكوسة يدويا في فترة مفتوحة إما للسنة المالية المغلقة أو السنة المالية التالية، اعتمادا على حالة عملية الإغلاق المالي. إذا تم ترحيل حركة جديدة إلى فترة مفتوحة من السنة المالية التي تم من خلال عملية إغلاق نهاية السنة، يجب تشغيل إغلاق نهاية السنة مرة أخرى.

- التسوية:

    - تتم تسوية الحركة (الدفع) أو وضع علامة للتسوية.

        - يمكنك التحقق مما إذا كانت الحركة قد تمت تسويتها أو تم وضع علامة للتسوية من خلال تحديد **عرض التسويات** أو **التسوية \> سجل التسوية** في صفحة **حركات المورد** أو **حركات العميل**.
        - يمكنك أيضا عكس تسوية من صفحة **حركات المورد** أو **حركات العميل** (**تسوية \> التراجع عن التسوية**) إذا كان يجب عكس إحدى الحركات.

- تحتوي المعاملة على أكثر من حركة دفتر الأستاذ الفرعي التي تم إدخالها باستخدام رقم الإيصال نفسه (إصدار إيصال واحد).
- الحركات الوسيطة:

    - إذا كانت الحركة مرتبطة بدفعة مؤقتة، فلا يمكن عكسها.
    - إذا كان يجب عكس الدفعة الجسرية، يجب مسح الدفعة أولا من الحساب المؤقت إلى البنك. ويمكن بعد ذلك عكس مسار الدفعة، شريطة أن تستوفي معايير التحقق الأخرى.

- تحتوي الحركة على حساب بنكي، ولكن يتم عكسها من **الحركات \<main account\>** للصفحة أو من دفتر الأستاذ الفرعي غير صحيح، مثل حسابات القبض أو الحسابات الدائنة:

    - كما يوحي هذا السبب، حتى عند تشغيل ميزة الانتكاسات الشامل، يمكن عكس بعض معاملات دفتر الأستاذ الفرعي فقط من صفحات معينة.

- إعادة تقييم العملة الأجنبية للبنك:

    - يمكن عكس إعادة تقييم العملة الأجنبية للبنك. ومع ذلك، قد يتم منع الإلغاء إذا قمت بإكمال خطوات الإلغاء خارج الترتيب الزمني. على سبيل المثال، إذا قمت بتشغيل إعادة التقييم في مارس وأبريل، لا يمكن عكس إعادة تقييم مارس حتى يتم عكس إعادة تقييم أبريل.

### <a name="types-of-transactions-that-cant-be-reversed"></a>أنواع الحركات التي لا يمكن عكسها

لا يمكن عكس الأنواع التالية للحركات:

- مدفوعات الموردين التي تم إجراؤها كتحويلات إلكترونية للأموال (EFTs)
- السندات الإذنية
- الكمبيالات

## <a name="fixed-assets"></a>الأصول الثابتة

تقوم عدة أنواع من الحركات بتحديث دفتر الأستاذ الفرعي للأصول الثابتة. وتشمل الأمثلة عمليات الاستحواذ والإهلاك.

إذا تم إيقاف تشغيل ميزة إلغاء الكتلة، يمكن عكس الحركات بشكل فردي من صفحة **حركات المورد**، أو من صفحة **حركات الأصول الثابتة**، أو من تأجير الأصول، وفقا لنوع الحركة.

إذا تم تشغيل ميزة الإلغاء الشامل، يمكن الآن عكس حركات الأصل الثابت أو أكثر من صفحة **حركات الإيصال**، ومن دفتر اليومية الذي تم ترحيل الحركة منه.

### <a name="reasons-why-transactions-cant-be-reversed"></a>أسباب تعذر عكس المعاملات

لا يمكن عكس الحركات للأسباب التالية:

- الفترة المالية معلقة أو مغلقة بشكل دائم:

    - إذا كان تاريخ التراجع في فترة مالية غير مفتوحة، فلا يمكن عكس الحركة.
    - إذا كانت الحركة تدعم إدخال تاريخ عكس، يمكن عكس الحركة عن طريق تغيير تاريخ الإلغاء إلى فترة مفتوحة.

- تم تشغيل عملية إغلاق نهاية العام لدفتر الأستاذ العام:

    - تاريخ المحاسبة للحركة هو في السنة المالية التي تم من خلال إغلاق نهاية السنة في دفتر الأستاذ العام. على الرغم من أن الفترة في السنة المالية قد تظل مفتوحة، إلا أنه لا يمكن عكس الحركة إذا تم تشغيل عملية إغلاق نهاية السنة للسنة المالية. السنة المالية لها حالة مختلفة عن الفترات التي فيها.
    - يمكن عكس إغلاق نهاية السنة، ومن ثم يمكن عكس الحركة. وقد لا يكون هذا النهج خيارا. قد يكون من الأسهل إدخال حركة معكوسة يدويا في فترة مفتوحة إما للسنة المالية المغلقة أو السنة المالية التالية، اعتمادا على حالة عملية الإغلاق المالي. إذا تم ترحيل حركة جديدة إلى فترة مفتوحة من السنة المالية التي تم من خلال عملية إغلاق نهاية السنة، يجب تشغيل إغلاق نهاية السنة مرة أخرى.

- عمليات الاستحواذ:

    - إذا حدث الامتلاك في فاتورة مورد أمر شراء، فيجب أن يتم الإلغاء عن طريق إدخال إشعار دائن للمورد. لمزيد من المعلومات حول كيفية إدخال حركة العكس، راجع [إنشاء أمر إرجاع شراء](../../supply-chain/procurement/tasks/create-purchase-return-order.md).
    - حدث الاستحواذ في حركة مشروع.
    - لا يمكن عكس عملية الاستحواذ بعد ترحيل الإهلاك للأصل. يجب عكس الإهلاك قبل أن يتم عكس عملية الاستحواذ.
    - إذا لم تكن حالة نموذج القيمة أو دفتر الإهلاك لأصل ثابت مفتوحة، فلا يمكن عكس الحركة.

- عمليات التصرف في الأصول:

    - يتم التخلص من خلال فاتورة النص الحر:

        - يتم حظر تصحيح فاتورة النص الحر إذا كانت تحتوي على أصل ثابت. ومع ذلك، إذا تم التخلص من الأصل من خلال دفتر يومية، يمكن عكس فاتورة النص الحر من سجل الأصول الثابتة.

    - إذا لم تكن حالة نموذج القيمة أو دفتر الإهلاك لأصل ثابت مفتوحة، فلا يمكن عكس الحركة.

- الإهلاك:

    - **يمكن** عكس الإهلاك إذا تم ترحيل الإهلاك اللاحق أيضا. ومع ذلك، سوف تتلقى تحذيرا، لأن هذا الأسلوب ليس أفضل الممارسات.
    - إذا لم تكن حالة نموذج القيمة أو دفتر الإهلاك لأصل ثابت مفتوحة، فلا يمكن عكس الحركة.

- توجد حركات (أو حركات عكسية) لأحد الأصول ودفاتر الأصول المحددة لتاريخ حركة الإيصال أو في وقت لاحق.
- تحتوي الحركة على حساب أصل، ولكن يتم عكسها من **الحركات \<main account\>** للصفحة أو من دفتر الأستاذ الفرعي غير صحيح، مثل حسابات القبض أو الحسابات الدائنة:

    - كما يوحي هذا السبب، حتى عند تشغيل ميزة الانتكاسات الشامل، يمكن عكس بعض معاملات دفتر الأستاذ الفرعي فقط من صفحات معينة.
    - إذا حدث استحواذ على فاتورة مورد أمر شراء غير أو دفتر يومية فاتورة مورد، يمكن عكسه فقط من صفحة **حركات المورد** في الحسابات الدائنة.
    - إذا تم الحصول على أصل من تأجير الأصول، يمكن عكسه من صفحة **حركات الخصوم** في تأجير الأصول.
