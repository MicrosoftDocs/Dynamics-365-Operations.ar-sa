---
title: الموافقة على أوامر الشراء وتأكيدها
description: يصف هذا المقال الحالات التي يمر بها أمر الشراء بعد إنشائه، وتأثير تمكين إدارة التغييرات في أوامر الشراء.
author: GalynaFedorova
ms.date: 04/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchOrderInReview, PurchOrderApproved, PurchOrderInDraft, PurchOrderAssignedToMe, VendPurchOrderJournalListPage, PurchTableWorkflowDropDialog, VendPurchOrderJournal
audience: Application User
ms.reviewer: kamaybac
ms.custom: 93143
ms.assetid: cd12a944-c52c-4579-a301-7abe1d237c72
ms.search.region: Global
ms.search.industry: ''
ms.author: gfedorova
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: af33dbd38b1eb70e79392860e48c6943a4192f78
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016438"
---
# <a name="approve-and-confirm-purchase-orders"></a>الموافقة على أوامر الشراء وتأكيدها

[!include [banner](../includes/banner.md)]

يصف هذا المقال الحالات التي يمر بها أمر الشراء بعد إنشائه، وتأثير تمكين إدارة التغييرات في أوامر الشراء.

يحتاج أمر الشراء، بعد إنشائه، إلى المرور عبر عملية الموافقة. وبعد أن يوافق المورّد على الأمر، يتم تعيين أمر الشراء إلى الحالة **مؤكد**.

## <a name="approval-of-purchase-orders"></a>الموافقة على أوامر الشراء
تكون أوامر الشراء التي لا تستخدم إدارة التغييرات بحالة **تمت الموافقة** فور إنشائها، بينما تكون أوامر الشراء التي تستخدم إدارة التغييرات بحالة **مسودة** عند إنشائها أولاً. يتم دائمًا تعيين أمر الشراء الذي تم إنشاؤه عن طريق تأكيد أمر مخطط من التخطيط الرئيسي إلى حالة **تمت الموافقة**، بغض النظر عن إعدادات إدارة التغييرات. ينشئ أمر الشراء حركات المخزون فقط عندما يصل إلى حالة **تمت الموافقة**. وبالتالي، لا يبدو هذا المخزون متوفرًا للحجز أو التمييز حتى يتم قبول الأمر.

لتمكين إدارة التغييرات لأوامر الشراء، يمكنك تعيين الخيار **تنشيط إدارة التغييرات‬** في صفحة **محددات تحديد الموارد والتدبير**. عند تمكين إدارة التغييرات، ستمر أوامر الشراء عبر سير عمل الموافقة بعد إكمالها. يتضمن Supply Chain Management محرر عملية سير عمل حيث يمكنك تعريف سير عمل لتمثيل عملية الموافقة. وبإمكان سير العمل هذا أن يتضمن قواعد للموافقة التلقائية وقواعد تحدد الجهة التي سيتم تعيينها للموافقة على أوامر شراء معينة وقواعد لتصعيد سير عمل انتظر طويلاً للحصول على الموافقة. يمكنك تمكين عملية إدارة التغييرات لكافة المورّدين أو لمورّدين محددين. ويمكنك أيضًا إعداد العملية بحيث يمكن تجاوزها لأوامر شراء فردية.

عند تمكين إدارة التغييرات، تتنقل أوامر الشراء عبر ست حالات موافقة، من **مسودة‬** إلى **تم الانتهاء‬**. وبعد الموافقة على أمر الشراء، يجب على المستخدمين الذين يرغبون في تعديله استخدام إجراء **طلب التغيير**.

| حالة الموافقة | ‏‏الوصف                                                                      | تمكين طلب التغيير |
|-----------------|----------------------------------------------------------------------------------|---------------------------|
| مبدئي           | أمر الشراء عبارة عن مسودة ولم يتم إرساله للموافقة عليه في سير عمل أمر الشراء.     | لا                        |
| قيد المراجعة       | تم إرسال أمر الشراء للموافقة عليه في سير عمل أمر الشراء. الموافقة معلّقة.       | لا                        |
| تم الرفض        | تم رفض أمر الشراء أثناء عملية الموافقة.                                 | لا                        |
| تمت الموافقة عليه        | تمت الموافقة على أمر الشراء.                                                             | ‏‏نعم                       |
| أوامر المبيعات المؤكدة       | تم تأكيد أمر الشراء. لا يمكن تأكيد أمر الشراء حتى تتم الموافقة عليه.        | ‏‏نعم                       |
| تم الانتهاء       | تم تحويل أمر الشراء إلى نهائي. تم الآن إقفاله من الناحية المالية ويتعذر تغييره بعد الآن. | لا                        |

## <a name="confirming-purchase-orders"></a>تأكيد أوامر الشراء
بإمكان أوامر الشراء بحالة **تمت الموافقة** المرور عبر خطوات إضافية قبل تأكيدها. على سبيل المثال، قد تحتاج إلى إرسال استعلام حول أمر الشراء إلى المورّد للاستفسار عن الأسعار أو الخصومات أو تواريخ التسليم. وفي هذه الحالة، يمكنك تعيين أمر الشراء إلى الحالة **قيد المراجعة الخارجية‬** باستخدام إجراء **استعلام الشراء‬**.

بإمكان المورّدين الذين تم إعدادهم لاستخدام وحدة تعاون المورّدين مراجعة الأوامر في المدخل، والموافقة عليها أو رفضها. وخلال عملية المراجعة هذه، يكون أمر الشراء بحالة **قيد المراجعة الخارجية**. يمكن تكوين وحدة تعاون المورّدين بحيث يؤدي تأكيد من المورّد إلى تأكيد الأمر في Supply Chain Management بشكل تلقائي. أو، يمكنك تأكيد أمر شراء يدويًا بعد تلقي تأكيد من المورّد. وإذا رفض المورّد أمر الشراء، يتم تلقي الرفض إلى جانب سبب الرفض واقتراحات تتعلق بالتغييرات. في هذه الحالة، يبقى أمر الشراء بحالة **قيد المراجعة الخارجية**.

هناك أيضًا خيار يسمح بإنشاء تأكيد مبدئي لأمر شراء قبل معالجة التأكيد الفعلي. ينشئ هذا الخيار فقط تقريرًا يمكنك مشاركته مع المورّد. ولا ينشئ أية معلومات في دفتر اليومية.

بعد أن يوافق المورّد على أمر الشراء، تقضي الخطوة التالية بتسجيل أمر الشراء كما تم الالتزام به. يمكنك إكمال هذه الخطوة باستخدام إجراء **التأكيد** أو الإجراء **تأكيد**. ويؤدي استخدام أي من الخيارين إلى تعيين حالة الموافقة على أمر الشراء إلى **مؤكد**. يؤدي تأكيد الأمر إلى بدء عمليتين إضافية:

-   يتم إنشاء دفتر يومية لتخزين نسخة دقيقة للمعلومات التي تم تأكيدها في النظام. في بعض الأحيان، تحتاج الأوامر إلى تغييرات، ويتم إنشاء دفاتر يومية إضافية بعد تأكيد الأمر المحدّث. تسمح لك دفاتر اليومية هذه بعرض سجل لمختلف إصدارات الأمر التي تم تأكيدها.
-   يتم إنشاء التوزيعات المحاسبية وتحدث عمليات فحص الأوامر والموازنة إذا تم تمكين هذه الوظيفة. في حالة فشل أي عملية فحص، سوف تتلقى رسالة خطأ تفيد بضرورة إجراء تغييرات على أمر الشراء قبل أن يمكن تأكيده مرة أخرى.

قد يطالب المورّد بالحصول على ضمان يتعلق بتوفير الدفع مقابل عملية شراء. هناك العديد من الطرق لتوفير هذا الضمان ضمن عمليات الحسابات الدائنة. على سبيل المثال، يؤدي استخدام الإجراء **دفعة مقدمة** إلى حجز أموال لأمر الشراء، ويتم تسجيل هذه الدفعة المقدمة على أمر الشراء.

## <a name="changing-purchase-orders"></a>تغيير أوامر الشراء
في بعض الحالات، قد تحتاج إلى تغيير أمر شراء بعد وصوله إلى حالة الموافقة **تمت الموافقة** أو **مؤكد**.

إذا تم إنشاء أمر الشراء باستخدام عملية إدارة التغييرات، فيمكنك إجراء تغييرات عبر استدعاء الأمر، أو إذا كان أمر الشراء قد حصل على الموافقة، باستخدام إجراء **طلب التغيير**. في هذه الحالة، تتغير حالة الموافقة لتعود إلى **مسودة**، ويمكنك بعد ذلك تعديل الأمر. بعد الانتهاء من إجراء التغييرات، قد تحتاج إلى إرسال أمر الشراء لإعادة الموافقة عليه. يمكنك تكوين أنواع التغييرات التي تحتاج إلى إعادة الموافقة باستخدام قاعدة السياسة **قاعدة إعادة الموافقة لأوامر الشراء‬** في صفحة **سياسات الشراء**.

إذا تم تسليم جزء من الكمية المطلوبة لبند أمر الشراء، فلا يمكنك تغيير الكمية المطلوبة عندما يكون أمر الشراء في الحالة **مسودة**. ومع ذلك، يمكنك تغيير كمية **تسليم الباقي** على بند أمر الشراء في الحالة **مسودة**.

بعد تأكيد أمر شراء، لن تعود قادرًا على حذفه. ومع ذلك، يمكنك إلغاء إجمالي الكمية أو أية كمية متبقية في أمر الشراء، شرط ألا يكون قد تم استلام الكمية أو فوترتها. ثم يمكنك استخدام الإجراء **إنهاء‬** لمنع مزيد من المعالجة. 


## <a name="canceling-purchase-orders"></a>إلغاء أوامر الشراء

يمكن إلغاء أمر الشراء باستخدام إجراء **إلغاء** في الرأس.

إذا تم تسجيل الكمية أو استلامها أو فوترتها جزئيًا، فإنه يمكنك فقط إلغاء الكمية المتبقية التي لم يتم تسجيلها أو استلامها أو فوترتها. ثم، يتم تخفيض كمية الأمر وفقًا لذلك. عند تحديث الكمية الموجودة بالبند، فإنه يتم تحديث حالة البند أيضًا. على سبيل المثال، تكون الكمية الأصلية في البند هي 5، ويتم استلام كمية من 3. وفي هذه الحالة، يمكن إلغاء اثنين فقط. يتم بعد ذلك تحديث البند إلى حالة **مستلم**.

في حالة إضافة المتبقي من التسليم إلى بند الأمر، وتجاوز الكمية الموجودة في بند الأمر، لا يقم الإجراء **إلغاء** بإلغاء الكمية الزائدة. بدلاً من ذلك، يظل البند في حالة **فتح أمر**، لأنه يحتوي على كمية متبقية. على سبيل المثال، تكون الكمية الأصلية في البند هي 5، والكمية المتبقية هي 7. في حالة إلغاء الأمر ، يتم إلغاء الكمية 5 وتبقى الكمية 2، كما ترى في حركات المخزون.

لإلغاء الكمية بالكامل في بند أمر الشراء، فإنه يجب عليك إلغاء كمية التسليم المتبقية من البند. سيقوم البند حينها بتحديث حالة **ملغي**.

في حالة وجود أمر شراء ضمن إدارة التغييرات، فإنه يجب إرسال أي تغيير، مثل إلغاء الأمر أو المتبقي من التسليم، إلى نظام سير العمل واعتماده قبل أن يتم إكمال العملية ويمكن تحديث حركات المخزون على أنها ملغية.

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على أمر الشراء](purchase-order-overview.md)

[إنشاء أوامر شراء](purchase-order-creation.md)

[إيصال استلام المنتجات في مقابل أوامر الشراء](product-receipt-against-purchase-orders.md)

[نظرة عامة على فواتير المورّدين](../../finance/accounts-payable/vendor-invoices-overview.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]