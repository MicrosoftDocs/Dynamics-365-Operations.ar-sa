---
title: "تعاون المورد مع موردين خارجيين"
description: "يصف هذا الموضوع كيف يستطيع وكلاء الشراء التعاون مع الموردين الخارجيين لتبادل المعلومات حول أوامر الشراء ومخزون الشحن."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: cbd099403f48b502ca74bcb38ae12decedb8f2da
ms.contentlocale: ar-sa
ms.lasthandoff: 07/27/2017

---

# <a name="vendor-collaboration-with-external-vendors"></a>تعاون المورد مع موردين خارجيين

[!include[banner](../includes/banner.md)]


يصف هذا الموضوع كيف يستطيع وكلاء الشراء التعاون مع الموردين الخارجيين لتبادل المعلومات حول أوامر الشراء ومخزون الشحن.

تستهدف الوحدة النمطية **تعاون المورد** الموردين ممن ليس لديهم تكامل التبادل الإلكتروني للبيانات (EDI) مع Microsoft Dynamics 365 for Finance and Operations. إنه تسمح للموردين بالعمل مع معلومات أوامر الشراء والفواتير ومخزون الشحن. يصف هذا الموضوع كيف يمكنك التعاون مع الموردين الخارجيين الذين يستخدمون واجهة تعاون المورد للعمل مع أوامر الشراء ومخزون الشحن. ويصف أيضًا كيفية تمكين مورد معين من استخدام واجهة تعاون المورد، وكيفية تعريف المعلومات التي ستظهر لكافة الموردين، عند استجابتهم لأمر شراء. لمزيد من المعلومات حول الأمور التي يمكن للموردين الخارجيين القيام بها في واجهة تعاون المورد، راجع [تعاون المورد مع العملاء](vendor-collaboration-work-customers-dynamics-365-operations.md).  

لمزيد من المعلومات حول كيفية استخدام الموردين واجهة تعاون الموردين في عمليات الفوترة، راجع [مساحة عمل فوترة تعاون المورد](/dynamics365/unified-operations/financials/accounts-payable/vendor-portal-invoicing-workspace). لمزيد من المعلومات حول كيفية توفير مستخدمين جدد لتعاون المورد، راجع [إدارة مستخدمي تعاون المورد](manage-vendor-collaboration-users.md).

لمزيد من المعلومات حول كيفية استخدام الموردين واجهة تعاون الموردين في عمليات الفوترة، راجع [مساحة عمل فوترة تعاون المورد](/dynamics365/unified-operations/financials/accounts-payable/vendor-portal-invoicing-workspace). 

لمزيد من المعلومات حول كيفية توفير مستخدمين جدد لتعاون المورد، راجع [إدارة مستخدمي تعاون المورد](manage-vendor-collaboration-users.md).

## <a name="define-the-information-that-is-shown-to-vendors-when-they-respond-to-pos"></a>تعريف المعلومات التي تظهر للموردين عند استجابتهم لأوامر الشراء
عندما يستجيب الموردون لأمر شراء ترسله لهم، سوف يشاهدون مربع رسالة حيث يجب عليهم تأكيد رغبتهم في قبول أمر الشراء أو رفضه أو قبوله مع بعض التغييرات. بما أن المعلومات التي يجب عرضها للمورد في هذه المرحلة قد تكون خاصة بأعمالك، يمكنك تحديد النص الذي سيظهر على كل واحدة من رسائل التأكيد الثلاث. على سبيل المثال، بإمكان النص إعلام المورد عن الخطوات المقبلة في العملية، أو عن الأحكام والشروط.  

لتعريف النص الذي يظهر في الاستجابة لأمر الشراء:

1.  افتح الصفحة **تقديم المعلومات للموردين بالاستجابة لأوامر الشراء‬**.
2.  حدد أحد أنواع الاستجابة.
3.  انقر فوق **تحرير**.
4.  أدخل المعلومات التي تريد أن يراها الموردون في المربع **رسالة المعلومات**.

إذا توجب عليك إضافة رسائل بأكثر من لغة واحدة، فعليك إنشاء رسائل منفصلة وتحديد أكواد اللغة المناسبة لك واحدة منها. ستكون الرسالة التي تظهر للمورد باللغة التي يستخدمها.

## <a name="set-the-vendor-collaboration-options-for-a-specific-vendor"></a>تعيين خيارات تعاون المورد لمورد محدد
تم تكوين الإعدادات العامة لتعاون المورد في Finance and Operations من قِبل المسؤول. على سبيل المثال، سيحدد المسؤول أدوار الأمان المتوفرة لكافة الموردين الذين تتعاون معهم. وهناك أيضًا بعض الإعدادات التي يمكنها أن تختلف باختلاف حساب المورد، ويجب عليك تعيين هذه الإعدادات:
-   تمكين تعاون المورد.
-   تقرير إن كنت تريد أن يرى المورد معلومات السعر.

### <a name="enable-vendor-collaboration"></a>تمكين تعاون المورد

قبل إنشاء حسابات المستخدمين لمورد خارجي، يجب تكوين حساب المورد للسماح لهم باستخدام تعاون المورد. للقيام بذلك، قم بتعيين الحقل **تنشيط التعاون** إلى نشط على علامة التبويب **عام** في صفحة **الموردون**. هناك خياران لك:

-   **نشط (تم تأكيد أمر الشراء تلقائيًا)‬**- يتم تأكيد أوامر الشراء تلقائيًا عندما يقبلها المورد من دون إجراء تغييرات.
-   **نشط (لم يتم تأكيد أمر الشراء تلقائيًا)‬**- يلزم تأكيد أوامر الشراء يدويًا من قبل المؤسسة، بعد أن يقبلها المورد.

### <a name="decide-whether-you-want-the-vendor-to-see-price-information"></a>تقرير إن كنت تريد أن يرى المورد معلومات السعر

إذا أردت مشاركة معلومات السعر مثل سعر الوحدة والخصومات والتكاليف عبر واجهة تعاون المورد، فيجب تعيين الخيار **أسعار/مبلغ ‏‏أوامر الشراء‬** إلى **نعم** على حساب المورد. يتوفر هذا الخيار في علامة التبويب **القيم الافتراضية لأمر الشراء‬**.

## <a name="work-with-pos-when-using-vendor-collaboration"></a>العمل مع أوامر الشراء عند استخدام تعاون المورد
### <a name="sending-a-po-to-the-vendor"></a>إرسال أمر شراء إلى مورد

يتم إعداد أوامر الشراء في Finance and Operations. عندما يكون أمر الشراء بحالة **معتمد**، سترسله إلى المورد باستخدام الإجراء **إرسال للتأكيد‬** في صفحة **أمر الشراء**. تتغير حالة أمر الشراء إلى **قيد المراجعة الخارجية‬**. بعد أن يتم إرسال أمر الشراء، يمكنك رؤيته في لصفحة **أوامر الشراء لمراجعة** في واجهة تعاون المورد. باستطاعة المورد عندئذٍ قبول الأمر أو رفضه أو اقتراح تغييرات عليه. باستطاعة المورّد أيضًا إضافة تعليقات لتوصيل معلومات مثل التغييرات على أمر الشراء. وإذا كنت تريد لفت انتباه المورّد إلى أمر شراء جديد، فيمكنك أيضًا استخدام نظام إدارة الطباعة لإرسال أمر الشراء عن طريق البريد الإلكتروني.

### <a name="confirmation-and-acceptance-of-the-po-by-the-vendor"></a>تأكيد أمر الشراء وقبوله من قِبل المورد

عندما يقبل المورد أمر الشراء، قد يتم تأكيد أمر الشراء تلقائيًا، أو قد يحتاج إلى تأكيده يدويًا. وهذا يتوقف على ما إذا تم تعيين الحقل **تنشيط المورد** إلى **نشط (تم تأكيد أمر الشراء تلقائيًا)** أو إلى **نشط (لم يتم تأكيد أمر الشراء تلقائيًا)** للمورد.  

يبين الجدول التالي تبادل المعلومات النموذجي، استنادًا إلى كيفية استجابة المورد عند إرسال أمر شراء له للتأكيد:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>استجابة المورد</strong></td>
<td><strong>النتيجة</strong></td>
</tr>
<tr class="even">
<td>المورد <strong>يقبل</strong> الأمر. يتم تكوين Finance and Operations لتأكيد أوامر الشراء تلقائيًا عندما يقبلها المورّد.</td>

<td>يتم تحديث حالة الأمر إلى <strong>مؤكد</strong>. إذا منع شيء ما تحديث الأمر، فستبقى مع ذلك استجابة المورّد مسجلة على أن الأمر <strong>مقبول‬</strong>، ولكن حالة أمر الشراء تبقى <strong>قيد المراجعة الخارجية</strong>. 

يتم تحديث أمر الشراء المرسل إلى المورد وحالته **قيد المراجعة الخارجية** بواسطة تواريخ التسليم المؤكدة في البنود. يبدأ التحديث إصدارًا جديدًا سيتم تلقائيًا تحديثه إلى الحالة **مؤكد**. عندما يتم تأكيد أمر الشراء، سوف يظهر في واجهة تعاون المورد.</td>
</tr>
<tr class="odd">
<td>المورد <strong>يقبل</strong> الأمر. لا يتم تكوين Finance and Operations لتأكيد أوامر الشراء تلقائيًا عندما يقبلها المورّد.</td>
<td>يتم تسجيل استجابة المورّد على أن الأمر <strong>مقبول</strong>، ولكن حالة أمر الشراء تبقى <strong>قيد المراجعة الخارجية</strong>.

يتم تحديث أمر الشراء المرسل إلى المورد وحالته **قيد المراجعة الخارجية** بواسطة تواريخ التسليم المؤكدة في البنود. يبدأ التحديث إصدارًا جديدًا سيتم تلقائيًا تعيينه إلى الحالة **قيد المراجعة الخارجية**. ستتمكن بعد ذلك من تأكيد أمر الشراء يدويًا.</td>

</tr>
<tr class="even">
<td>المورد <strong>يرفض</strong> الأمر.</td>
<td>يتم تسجيل استجابة المورّد على أن الأمر <strong>مرفوض</strong>، ولكن حالة أمر الشراء تبقى <strong>قيد المراجعة الخارجية</strong>. يتم تلقي الرفض مع ملاحظة المورد.</td>
</tr>
<tr class="odd">
<td>المورِّد <strong>يقبل الأمر مع بعض التغييرات</strong>. ويتم اقتراح التغييرات على مستوى البنود.‬ من الممكن قبول أو رفض بنود فردية. وتشمل التغييرات الأخرى المحتملة:
<ul>
<li>تغيير التواريخ أو الكميات.</li>
<li>تقسيم البنود للحصول على كميات أو تواريخ تسليم مختلفة.</li>
<li>استبدال صنف ما.</li>
</ul>
لا يمكن تغيير معلومات السعر والتكاليف من قِبل المورد. ويمكن تقديم الاقتراحات المتعلقة بإدخال تغييرات على هذه المعلومات باستخدام الملاحظات.</td>
<td>يتم تسجيل استجابة المورّد على أنها <strong>تم القبول مع التغييرات</strong>، وتبقى حالة أمر الشراء <strong>قيد المراجعة الخارجية</strong>. تظهر الحالات أنواع التغييرات التي اقترحها المورد. لمزيد من المعلومات حول الاستهلاك التلقائي للتغييرات، انظر المقطع أدناه حول كيفية تحديث أمر الشراء عندما يقترح المورد إدخال بعض التغييرات. </td>
</tr>
</tbody>
</table>

‏‫يمكنك استخدام مساحة عمل **إعداد أمر** **الشراء** لمراقبة أوامر الشراء التي استجاب لها المورد. تتضمن مساحة العمل هذه قائمتين تحتويان على أوامر شراء بحالة **قيد المراجعة الخارجية**:

-   قيد المراجعة الخارجية تتطلب إجراءً.
-   ‏‫قيد المراجعة الخارجية‬ في انتظار استجابة المورد.

### <a name="changing-a-po"></a>تغيير أمر شراء

لتغيير أمر شراء تمت الاستجابة له، يجب إرسال إصدار جديد من أمر الشراء إلى المورد. سيتضمن أمر الشراء الجديد لاحقة إصدار تشير إلى أنه إصدار معدّل من أمر شراء تم إرساله في وقت سابق. تسمح لك الصفحة **محفوظات تأكيد مورِّد أمر الشراء‬** كما تسمح للموردين بتعقب محفوظات كل أمر. يبقى إصدار أمر الشراء الذي تم تأكيده في السابق في قائمة أوامر الشراء المؤكدة حتى يتم تأكيد أمر الشراء الجديد.

### <a name="cancelling-a-po"></a>إلغاء أمر شراء

عندما تقوم بإلغاء أمر شراء، تتغير الحالة إلى **معتمد‬**. يجب عليك إعادة إرسال أمر الشراء إلى المورّد عبر مدخل المورّد، بحيث يتمكن المورّد من تأكيد الإلغاء أو رفضه. بعد تأكيد الإلغاء، يظهر أمر الشراء في قائمة المورّد الخاصة بأوامر الشراء التي تم تأكيدها على أنها **ملغاة**.

### <a name="adding-attachments-to-a-po"></a>إضافة مرفقات إلى أمر شراء

يمكنك إضافة مرفقات مثل الملفات والصور والملاحظات إلى أمر الشراء باستخدام نظام إدارة المستندات. ستكون المرفقات المضافة من النوع **خارجي** مرئية للمورد عندما ترسل له أمر الشراء.

## <a name="update-the-po-when-a-vendor-suggests-changes"></a>تحديث أمر الشراء عندما يقترح المورد إدخال بعض التغييرات
عندما يستجيب المورد لأمر الشراء ويقترح إدخال بعض التغييرات، ستكون الخطوة التالية العمل على معالجة الاستجابة.
في **مساحة عمل إعداد عداد أمر الشراء**، وفي قائمة "تتطلب المراجعة الخارجية إجراءً‬"، يمكنك تحديد أمر شراء استجاب له المورد كمقبول مع تغييرات. في قائمة "تتطلب المراجعة الخارجية إجراءً‬"، يمكنك أيضًا الانتقال إلى استجابة المورد. على الاستجابة، يستطيع المورد تغيير المعلومات التالية على الرأس.
 
-   مرجع مستند المورد
-   وضع التسليم
-   شروط التسليم
-   تاريخ التسليم المؤكد

باستطاعة المورد أيضًا إضافة ملاحظة أو مرفق

في البنود، يستطيع المورد تغيير الكمية وتواريخ التسليم وإضافة الملاحظات والمرفقات ورفض بند واستبدال بند بمنتج آخر تم إدخاله كنص وتقسيم بند إلى عمليات تسليم متعددة. استنادًا إلى التغييرات التي اقترحها المورد، ستكون حالات البند مختلفة:
    
-   **تم القبول مع التغييرات**
-   **مرفوض**
-   **تم الاستبدال** في هذه الحالة سيضاف بند إضافي حالته **استبدال**.
-   **مؤكد‬** تقسيم الجدول‬ في هذه الحالة ستضاف بنود إضافية حالتها **بنود الجدول‬**.

إذا لم يتضمن البند أي تغييرات، فستكون حالة البند **مقبول**.

في الاستجابة، يمكنك رؤية حالات البنود التي تمت الإشارة إليها في السابق والتي تشير إلى أنواع التغييرات التي أجراها بالمورد. بالإضافة إلى ذلك، تظهر كافة الحقول التي تم تغييرها بخط غامق لمساعدتك في التعرف على التغييرات.

يمكنك تحديث أمر شراء بالنقر فوق إجراء **معالجة تحديث أمر الشراء** في الاستجابة أو بند واحد في كل مرة. يسمح لك مؤشر، **هل تمت معالجة تحديث أمر الشراء؟‬**، على الرأس والبنود بمعرفة ما إذا كان النظام قد قام بمعالجة الرأس أو البنود لتحديث أمر الشراء بأية تغييرات محتملة نشأت عن الاستجابة. يمكنك تشغيل عملية **معالجة تحديث أمر الشراء** مرة واحدة فقط لكل رأس أو بند.

لا يمكن تحديث كافة التغييرات المقترحة على أمر شراء. في أمر الشراء، يمكن تحديث فقط التحديثات في الرأس والتحديثات في التواريخ والكميات بشكل تلقائي. بالنسبة إلى التغييرات الأخرى، يجب عليك تحديث أمر الشراء يدويًا. في هذه الحالة، يعرض مؤشر **هل تمت معالجة تحديث أمر الشراء؟‬** خيار **التحديث اليدوي**. هناك مثال عن التغيير الذي يجب معالجته يدويًا وهو عند قيام المورد باقتراح تقسيم بند في جدول.

سيتضمن بند حالته **مقبول** تاريخ تسليم مؤكد سيتم تحديثه على أمر الشراء عندما تقوم بتنفيذ **معالجة تحديث أمر الشراء**. لن يتم نقل الملاحظات والمرفقات بشكل تلقائي إلى أمر الشراء الحالي. لاحظ أنك عندما تقوم بتحديث أمر الشراء الحالي عن طريق إجراء **معالجة تحديث أمر الشراء**، لن يعاد تقيم الاتفاقيات التجارية على بنود أمر الشراء.


## <a name="po-statuses-and-versions"></a>حالات وإصدارات أمر الشراء
يصف هذا القسم الحالات المختلفة التي قد يمر بها أمر شراء وصولاً إلى وقت تأكيدها. كما يصف المرحلة حيث يمكن جعل الإصدارات الجديدة من الشراء متوفرة للمورد. يختلف السلوك، بحسب ما إذا كنت تستخدم إدارة التغييرات لأوامر الشراء. 

### <a name="versions-and-statuses-if-you-dont-use-change-management"></a>الإصدارات والحالات إذا لم تستخدم إدارة التغييرات

يُظهر الجدول التالي مثالاً على التغييرات في الحالة والإصدار التي قد يمر بها أمر الشراء.

|                                                                          |                                                                                                                                                              |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **إجراء**                                                               | **الحالة والإصدار**                                                                                                                                       |
| تم إنشاء الإصدار الأولى لأمر الشراء في Finance and Operations. | الحالة هي **معتمد**.                                                                                                                                  |
| يتم إرسال أمر الشراء إلى المورد.                                            | يتم تسجيل إصدار في واجهة تعاون المورد، وتتغير الحالة إلى **قيد المراجعة الخارجية‬**.                                          |
| يرسل المورد الاستجابة **تم القبول مع التغييرات‬**.                  | تبقى الحالة **قيد المراجعة الخارجية**.                                                                                                                  |
| ستجري بعض التغييرات المطلوبة من قِبل المورّد.                  | تتغير الحالة إلى **معتمد**.                                                                                                                        |
| ترسل الإصدار الجديد من أمر الشراء إلى المورد.                        | يتم تسجيل الإصدار الجديد في واجهة تعاون المورد، وتتغير الحالة إلى **قيد المراجعة الخارجية‬**.                                      |
| يقبل المورد الإصدار الجديد من أمر الشراء.                            | تبقى الحالة **قيد المراجعة الخارجية**إلا إذا تم تكوين حساب المورد لتعيين أمر الشراء تلقائيًا إلى الحالة **مؤكد** عند قبوله. |


لا يتعيّن على الموردين تأكيد أمر الشراء باستخدام واجهة تعاون المورد. يمكنهم أيضًا إرسال رسالة بريد إلكتروني أو التبليغ عن موافقتهم على أمر الشراء عبر قنوات أخرى. يمكنك عندئذٍ تأكيد الأمر يدويًا في Finance and Operations. في هذه الحالة، سوف تتلقى تحذيرًا يفيد بأنه قد تم تأكيد الأمر حتى لو لم يكن هناك استجابة من المورّد. ويظهر أمر الشراء عندئذٍ في محفوظات التأكيد كأمر مؤكد مفتوح ليس لديه أية استجابات. ولن يتوفر للمورد خيار تأكيد أمر الشراء أو رفضه.  


>[!NOTE]
>يكون إصدار أمر الشراء المتوفر لعمليات أخرى في Dynamics 365 for Finance and Operations الإصدار الأحدث دائمًا، حتى لو لم يكن هذا الإصدار مسجلاً بعد في واجهة تعاون المورد.

### <a name="versions-and-statuses-if-you-use-change-management"></a>الإصدارات والحالات إذا استخدمت إدارة التغييرات

إذا قمت بتمكين إدارة التغييرات لأوامر شراء، فسيمر أمر الشراء عبر سير عمل الموافقة للوصول إلى الحالة **معتمد**. ولا تظهر هذه العملية للمورد.  

يُظهر الجدول التالي مثالاً على التغييرات في الحالة والإصدار التي قد يمر بها أمر الشراء عند تشغيل إدارة التغييرات. يتم تسجيل الإصدار عندما تتم الموافقة على أمر الشراء، وليس عندما يتم إرسال أمر الشراء إلى المورد أو تأكيده.

|                                                                          |                                                                                                                                                              |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **إجراء**                                                               | **الحالة والإصدار**                                                                                                                                       |
| تم إنشاء الإصدار الأولى لأمر الشراء في Finance and Operations.      | الحالة هي **مسودة**.  |
| يتم إرسال أمر الشراء إلى عملية الموافقة. (عملية الموافقة عبارة عن عملية داخلية لا يتدخل فيها المورد.)                                                           | تتغيّر الحالة من **مسودة‬** إلى **قيد المراجعة‬** إلى **اعتماد** إذا لم يتم رفض أمر الشراء أثناء عملية الموافقة. يتم تسجيل أمر الشراء المعتمد كإصدار.           | 
| يتم إرسال أمر الشراء إلى المورد                                                            | يتم تسجيل الإصدار في واجهة تعاون المورد، وتتغير الحالة إلى **قيد المراجعة الخارجية‬**.      |
| ستقوم بإدخال بعض التغييرات المطلوبة من قبل المورد، إما يدويًا أو باستخدام الإجراء في الاستجابة لتحديث أمر الشراء.                                                            | تتغير الحالة مرة أخرى إلى **مسودة**.     |
|يتم إرسال أمر الشراء إلى عملية الموافقة مرة أخرى.                                                |  تتغيّر الحالة من **مسودة‬** إلى **قيد المراجعة‬** إلى **اعتماد** إذا لم يتم رفض أمر الشراء أثناء عملية الموافقة. بدلاً من ذلك، يمكن تكوين النظام بحيث لا تحتاج تغييرات محددة في الحقل إلى إعادة الموافقة. وفي هذه الحالة، تتغير الحالة إلى **مسودة** أولاً، ثم يتم تحديثها بشكل تلقائي إلى **معتمد**. يتم تسجيل أمر الشراء المعتمد كإصدار جديد.                                         |
|ترسل الإصدار الجديد من أمر الشراء إلى المورد.                                                |  يتم تسجيل الإصدار الجديد في واجهة تعاون المورد، وتتغير الحالة إلى **قيد المراجعة الخارجية‬**.                                         |
|يوافق المورّد على الإصدار الجديد من أمر الشراء.                                                |  تتغير الحالة إلى **مؤكد**، إما تلقائياً أو عندما تتلقى الاستجابة من المورّد ثم تؤكد أمر الشراء. |

## <a name="share-information-about-consignment-inventory"></a>مشاركة معلومات حول مخزون الشحن
إذا كنت تستخدم مخزون الشحن، فباستطاعة الموردين استخدام واجهة تعاون المورد لعرض المعلومات في الصفحات التالية:

-   **أوامر الشراء التي تستهلك مخزون الشحن‬** - يتم إنشاء أوامر الشراء لمخزون الشحن عندما تتغير ملكية المخزون من المورد إلى شركتك. يتم ترحيل إيصال استلام المنتجات في نفس الوقت. تظهر أوامر شراء الشحن هذه فقط في صفحة **أوامر الشراء التي تستهلك مخزون الشحن**. لا يتم تضمينها في صفحة **كافة أوامر الشراء المؤكدة‬** في الوحدة النمطية **تعاون المورد**.
-   **المنتجات التي تم استلامها من مخزون الشحن‬** -تذكر هذه الصفحة كافة الحركات حيث انتقلت ملكية المنتجات من المورد إلى شركتك. باستطاعة الموردين استخدام هذه المعلومات لفوترة العميل.
-   **مخزون الشحن الفعلي‬** - تعرض هذه الصفحة مخزون الشحن الفعلي‬ الذي يملكه المورد والذي تم استلامه في مستودعك.




