---
title: "تعاون المورد مع موردين خارجيين"
description: "يصف هذا الموضوع كيف يستطيع وكلاء الشراء التعاون مع الموردين الخارجيين لتبادل المعلومات حول أوامر الشراء ومخزون الشحن."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: d585ae0716a4bd9c3531e8639cd7c6b3cab780ac
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-collaboration-with-external-vendors"></a>تعاون المورد مع موردين خارجيين

[!include[banner](../includes/banner.md)]


يصف هذا الموضوع كيف يستطيع وكلاء الشراء التعاون مع الموردين الخارجيين لتبادل المعلومات حول أوامر الشراء ومخزون الشحن.

تستهدف الوحدة النمطية **تعاون المورد** الموردين ممن ليس لديهم تكامل التبادل الإلكتروني للبيانات (EDI) مع Microsoft Dynamics 365 for Operations. إنه تسمح للموردين بالعمل مع معلومات أوامر الشراء والفواتير ومخزون الشحن. يصف هذا الموضوع كيف يمكنك التعاون مع الموردين الخارجيين الذين يستخدمون واجهة تعاون المورد للعمل مع أوامر الشراء ومخزون الشحن. ويصف أيضًا كيفية تمكين مورد معين من استخدام واجهة تعاون المورد، وكيفية تعريف المعلومات التي ستظهر لكافة الموردين، عند استجابتهم لأمر شراء. لمزيد من المعلومات حول الأمور التي يمكن للموردين الخارجيين القيام بها في واجهة تعاون المورد، راجع [تعاون المورد مع العملاء](vendor-collaboration-work-customers-dynamics-365-operations.md).  

لمزيد من المعلومات حول كيفية استخدام الموردين واجهة تعاون الموردين في عمليات الفوترة، راجع [مساحة عمل فوترة تعاون المورد](/dynamics365/operations/financials/accounts-payable/vendor-portal-invoicing-workspace). لمزيد من المعلومات حول كيفية توفير مستخدمين جدد لتعاون المورد، راجع [إدارة مستخدمي تعاون المورد](manage-vendor-collaboration-users.md).

## <a name="define-the-information-shown-to-vendors-when-they-respond-to-pos"></a>تعريف المعلومات التي تظهر للموردين عند استجابتهم لأوامر الشراء
عندما يستجيب الموردون لأمر شراء ترسله لهم، سوف يشاهدون مربع حوار حيث يجب عليهم تأكيد رغبتهم في قبول أمر الشراء أو رفضه أو قبوله مع بعض التغييرات. قد تكون المعلومات التي يجب عرضها للمورد في هذه المرحلة خاصة بأعمالك، لكي تتمكن من تحديد النص الذي سيظهر على كل واحدة من رسائل التأكيد الثلاث. على سبيل المثال، بإمكان النص إعلام المورد عن الخطوات المقبلة في العملية، أو عن الأحكام والشروط.  

لتعريف النص الذي يظهر في الاستجابة لأمر الشراء:

1.  افتح الصفحة **تقديم المعلومات للموردين بالاستجابة لأوامر الشراء‬**.
2.  حدد أحد أنواع الاستجابة.
3.  انقر فوق **تحرير.**
4.  أدخل المعلومات التي تريد أن يراها الموردون في المربع **رسالة المعلومات**.

إذا أردت إضافة رسائل بأكثر من لغة واحدة، فعليك إنشاء رسائل منفصلة مع أكواد اللغة المناسبة. ستظهر الرسالة للمورد باللغة التي يستخدمها.

## <a name="set-the-vendor-collaboration-options-for-a-specific-vendor"></a>تعيين خيارات تعاون المورد لمورد محدد
يتم تكوين الإعدادات العامة لتعاون المورد في Dynamics 365 for Operations من قِبل المسؤول. على سبيل المثال، ستحدد هذه الإعدادات أدوار الأمان المتوفرة لكافة الموردين الذين تتعاون معهم. وهناك أيضًا بعض الإعدادات التي قد تختلف باختلاف حساب المورد، ويجب عليك تعيينها:

-   تمكين تعاون المورد.
-   تقرير إن كنت تريد أن يرى المورد معلومات السعر.

### <a name="enable-vendor-collaboration"></a>تمكين تعاون المورد

قبل إنشاء حسابات المستخدمين لمورد خارجي، يجب تكوين حساب المورد للسماح لهم باستخدام تعاون المورد. للقيام بذلك، قم بتعيين الحقل **تنشيط التعاون** إلى نشط على علامة التبويب **عام** في صفحة **الموردون**. هناك خياران لك:

-   **نشط (تم تأكيد أمر الشراء تلقائيًا)‬ **- يتم تأكيد أوامر الشراء تلقائيًا عندما يقبلها المورد من دون إجراء تغييرات.
-   **نشط (لم يتم تأكيد أمر الشراء تلقائيًا)‬ **- يلزم تأكيد أوامر الشراء يدويًا من قبل المؤسسة، بعد أن يقبلها المورد.

### <a name="decide-whether-you-want-the-vendor-to-see-price-information"></a>تقرير إن كنت تريد أن يرى المورد معلومات السعر

إذا أردت مشاركة معلومات السعر مثل سعر الوحدة والخصومات والتكاليف عبر واجهة تعاون المورد، فيجب تعيين الخيار **أسعار/مبلغ ‏‏أوامر الشراء‬** إلى **نعم** على حساب المورد. يتوفر هذا الخيار في علامة التبويب **القيم الافتراضية لأمر الشراء‬**.

## <a name="work-with-pos-when-using-vendor-collaboration"></a>العمل مع أوامر الشراء عند استخدام تعاون المورد
### <a name="sending-a-po-to-the-vendor"></a>إرسال أمر شراء إلى مورد

يتم إعداد أوامر الشراء في Dynamics 365 for Operations. عندما يكون أمر الشراء بحالة **معتمد**، سترسله إلى المورد باستخدام الإجراء **إرسال للتأكيد‬ **في صفحة **أمر الشراء**. تتغير حالة أمر الشراء إلى **قيد المراجعة الخارجية‬**. بعد إرسال أمر الشراء، سيتمكن المورد من رؤيته في صفحة **أوامر الشراء للمراجعة‬** في واجهة تعاون المورد، حيث يمكنه قبول الأمر أو رفضه أو اقتراح إدخال بعض التغييرات عليه. باستطاعة المورّد أيضًا إضافة تعليقات لتوصيل معلومات مثل التغييرات على أمر الشراء. وإذا كنت تريد لفت انتباه المورّد إلى أمر شراء جديد، فيمكنك أيضًا استخدام نظام إدارة الطباعة لإرسال أمر الشراء عن طريق البريد الإلكتروني.

### <a name="confirmation-and-acceptance-of-the-po-by-the-vendor"></a>تأكيد أمر الشراء وقبوله من قِبل المورد

عندما يقبل المورد أمر الشراء، قد يتم تأكيد أمر الشراء تلقائيًا، أو قد يحتاج إلى تأكيده يدويًا. وهذا يتوقف على ما إذا تم تعيين الحقل **تنشيط المورد **إلى **نشط (تم تأكيد أمر الشراء تلقائيًا)** للمورد، أو إلى **نشط (لم يتم تأكيد أمر الشراء تلقائيًا)**.  

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
<td>المورد <strong>يقبل</strong> الأمر. تم تكوين Dynamics 365 for Operations لتأكيد أوامر الشراء تلقائيًا عندما يقبلها المورّد.</td>
<td>يتم تحديث حالة الأمر إلى <strong>مؤكد</strong>. إذا منع شيء ما تحديث الأمر، فستبقى مع ذلك استجابة المورّد مسجلة على أن الأمر <strong>مقبول‬</strong>، ولكن حالة أمر الشراء تبقى <strong>قيد المراجعة الخارجية</strong>.</td>
</tr>
<tr class="odd">
<td>المورد <strong>يقبل</strong> الأمر. لم يتم تكوين Dynamics 365 for Operations لتأكيد أوامر الشراء تلقائيًا عندما يقبلها المورّد.</td>
<td>يتم تسجيل استجابة المورّد على أن الأمر <strong>مقبول</strong>، ولكن حالة أمر الشراء تبقى <strong>قيد المراجعة الخارجية</strong>.</td>
</tr>
<tr class="even">
<td>المورد <strong>يرفض</strong> الأمر.</td>
<td>يتم تسجيل استجابة المورّد على أن الأمر <strong>مرفوض</strong>، ولكن حالة أمر الشراء تبقى <strong>قيد المراجعة الخارجية</strong>. يتم تلقي الرفض مع ملاحظة الموردين.</td>
</tr>
<tr class="odd">
<td>المورِّد <strong>يقبل الأمر مع بعض التغييرات</strong>. ويتم اقتراح التغييرات على مستوى البنود.‬ من الممكن قبول أو رفض بنود فردية. وتشمل التغييرات الأخرى المحتملة:
<ul>
<li>تغيير التواريخ أو الكميات.</li>
<li>تقسيم البنود للحصول على كميات أو تواريخ تسليم مختلفة.</li>
<li>استبدال صنف ما.</li>
</ul>
لا يمكن تغيير معلومات السعر والتكاليف من قِبل المورد. ويمكن تقديم الاقتراحات المتعلقة بإدخال تغييرات على هذه المعلومات باستخدام الملاحظات.</td>
<td>يتم تسجيل استجابة المورّد على أنها <strong>تم القبول مع التغييرات</strong>، <strong></strong> وتبقى حالة أمر الشراء <strong>قيد المراجعة الخارجية</strong>.</td>
</tr>
</tbody>
</table>

‏‫يمكنك استخدام مساحة عمل **إعداد أمر الشراء****** لمراقبة أوامر الشراء التي استجاب لها المورد. تتضمن مساحة العمل هذه قائمتين تحتويان على أوامر شراء بحالة **قيد المراجعة الخارجية**:

-   قيد المراجعة الخارجية تتطلب إجراءً.
-   ‏‫قيد المراجعة الخارجية‬ في انتظار استجابة المورد.

### <a name="changing-a-po"></a>تغيير أمر شراء

عندما تحتاج إلى تغيير أمر شراء تمت الاستجابة له، سترسل إصدارًا جديدًا من أمر الشراء إلى المورد. سيتضمن أمر الشراء الجديد لاحقة إصدار تشير إلى أنه إصدار معدّل من أمر شراء تم إرساله في وقت سابق. تسمح لك الصفحة **محفوظات تأكيد مورِّد أمر الشراء‬** كما تسمح للموردين بتعقب محفوظات كل أمر. يبقى إصدار أمر الشراء الذي تم تأكيده في السابق في قائمة أوامر الشراء المؤكدة حتى يتم تأكيد أمر الشراء الجديد.

### <a name="cancelling-a-po"></a>إلغاء أمر شراء

عندما تقوم بإلغاء أمر شراء، تتغير الحالة إلى **معتمد‬**. يجب عليك إعادة إرسال أمر الشراء إلى المورّد عبر مدخل المورّد، بحيث يتمكن المورّد من تأكيد الإلغاء أو رفضه. بعد تأكيد الإلغاء، يظهر أمر الشراء في قائمة المورّد الخاصة بأوامر الشراء التي تم تأكيدها على أنها **ملغاة**.

### <a name="adding-attachments-to-a-po"></a>إضافة مرفقات إلى أمر شراء

يمكنك إضافة مرفقات مثل الملفات والصور والملاحظات إلى أمر الشراء باستخدام نظام إدارة المستندات. ستكون المرفقات المضافة مع تقييد من النوع **خارجي** مرئية للمورد عندما ترسل له أمر الشراء.

## <a name="purchase-order-statuses-and-versions"></a>حالات وإصدارات أمر الشراء
يصف هذا القسم الحالات المختلفة التي قد يمر بها أمر الشراء وصولاً إلى وقت تأكيده، كما يصف المرحلة التي ستكون فيها الإصدارات الجديدة من أمر الشراء متوفرة للمورد. هناك اختلافات في هذا الصدد، وهذا يتوقف على ما إذا كنت تستخدم إدارة التغييرات لأوامر الشراء. 

### <a name="versions-and-statuses-if-you-dont-use-change-management"></a>الإصدارات والحالات إذا لم تستخدم إدارة التغييرات

يُظهر الجدول التالي مثالاً على التغييرات في الحالة والإصدار التي قد يمر بها أمر الشراء.

|                                                                          |                                                                                                                                                              |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **إجراء**                                                               | **الحالة والإصدار**                                                                                                                                       |
| يتم إنشاء الإصدار الأولى لأمر الشراء في Dynamics 365 for Operations. | الحالة هي **معتمد**.                                                                                                                                  |
| يتم إرسال أمر الشراء إلى المورد.                                            | يتم تسجيل إصدار في واجهة تعاون المورد، وتتغير الحالة إلى **قيد المراجعة الخارجية‬**.                                          |
| يرسل المورد الاستجابة **تم القبول مع التغييرات‬**.                  | تبقى الحالة **قيد المراجعة الخارجية**.                                                                                                                  |
| ستجري بعض التغييرات المطلوبة من قِبل المورّد.                  | تتغير الحالة إلى **معتمد**.                                                                                                                        |
| ترسل الإصدار الجديد من أمر الشراء إلى المورد.                        | يتم تسجيل الإصدار الجديد في واجهة تعاون المورد، وتتغير الحالة إلى **قيد المراجعة الخارجية‬**.                                      |
| يقبل المورد الإصدار الجديد من أمر الشراء.                            | تبقى الحالة **قيد المراجعة الخارجية **إلا إذا تم تكوين حساب المورد لتعيين أمر الشراء تلقائيًا إلى الحالة **مؤكد** عند قبوله. |

لا يتعيّن على الموردين تأكيد أمر الشراء باستخدام واجهة تعاون المورد. يمكنهم أيضًا إرسال رسالة بريد إلكتروني أو التبليغ عن موافقتهم على أمر الشراء عبر قنوات أخرى. يمكنك عندئذٍ تأكيد الأمر يدويًا في Dynamics 365 for Operations. إذا فعلت ذلك، فتتلقى تحذيرًا يفيد بأنه قد تم تأكيد الأمر حتى لو لم يكن هناك استجابة من المورد. ويظهر أمر الشراء عندئذٍ في محفوظات التأكيد كأمر مؤكد مفتوح ليس لديه أية استجابات. ولن يتوفر للمورد خيار تأكيد أمر الشراء أو رفضه.  

**ملاحظة:** يكون إصدار أمر الشراء المتوفر لعمليات أخرى في Dynamics 365 for Operations الإصدار الأحدث دائمًا، حتى لو لم يكن هذا الإصدار مسجلاً بعد في واجهة تعاون المورد.

### <a name="versions-and-statuses-if-you-use-change-management"></a>الإصدارات والحالات إذا استخدمت إدارة التغييرات

إذا قمت بتمكين إدارة التغييرات لأوامر شراء، فسيمر أمر الشراء عبر سير عمل الموافقة للوصول إلى الحالة **معتمد**. ولا تظهر هذه العملية للمورد.  

يُظهر الجدول التالي مثالاً على التغييرات في الحالة والإصدار التي قد يمر بها أمر الشراء عند تشغيل إدارة التغييرات. يتم تسجيل الإصدار عندما تتم الموافقة على أمر الشراء، وليس عندما يتم إرسال أمر الشراء إلى المورد أو تأكيده.

|                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **إجراء**                                                                                                    | **الحالة والإصدار**                                                                                                                                                                                                                                                                                                                                                                      |
| يتم إنشاء الإصدار الأولى لأمر الشراء في Dynamics 365 for Operations.                                      | الحالة هي **مسودة**.                                                                                                                                                                                                                                                                                                                                                                    |
| يتم إرسال أمر الشراء إلى عملية الموافقة. (هذه عملية داخلية لا يتدخل فيها المورد.) | تتغيّر الحالة من **مسودة‬** إلى **قيد المراجعة‬** إلى **اعتماد** إذا لم يتم رفض أمر الشراء أثناء عملية الموافقة. يتم تسجيل أمر الشراء المعتمد كإصدار.                                                                                                                                                                                                                     |
| يتم إرسال أمر الشراء إلى المورد                                                                                  | يتم تسجيل الإصدار في واجهة تعاون المورد، وتتغير الحالة إلى **قيد المراجعة الخارجية‬**.                                                                                                                                                                                                                                                                       |
| ستجري بعض التغييرات المطلوبة من قِبل المورّد.                                                       | تتغير الحالة مرة أخرى إلى **مسودة**.                                                                                                                                                                                                                                                                                                                                                    |
| يتم إرسال أمر الشراء إلى عملية الموافقة مرة أخرى.                                                            | تتغيّر الحالة من **مسودة‬** إلى **قيد المراجعة‬** إلى **اعتماد** إذا لم يتم رفض أمر الشراء أثناء عملية الموافقة. بدلاً من ذلك، يمكن تكوين النظام بحيث لا تحتاج تغييرات محددة في الحقل إلى إعادة الموافقة. وفي هذه الحالة، تتغير الحالة إلى **مسودة** أولاً، ثم يتم تحديثها بشكل تلقائي إلى **معتمد**. يتم تسجيل أمر الشراء المعتمد كإصدار جديد. |
| ترسل الإصدار الجديد من أمر الشراء إلى المورد.                                                             | يتم تسجيل الإصدار الجديد في واجهة تعاون المورد، وتتغير الحالة إلى **قيد المراجعة الخارجية‬**.                                                                                                                                                                                                                                                                   |
| يوافق المورّد على الإصدار الجديد من أمر الشراء.                                                                | تتغير الحالة إلى **مؤكد**، إما تلقائياً أو عندما تتلقى الاستجابة من المورّد ثم تؤكد أمر الشراء.                                                                                                                                                                                                                                                     |

## <a name="share-information-about-consignment-inventory"></a>مشاركة معلومات حول مخزون الشحن
إذا كنت تستخدم مخزون الشحن، فباستطاعة الموردين استخدام واجهة تعاون المورد لعرض المعلومات في الصفحات التالية:

-   **أوامر الشراء التي تستهلك مخزون الشحن‬** - يتم إنشاء أوامر الشراء لمخزون الشحن عندما تتغير ملكية المخزون من المورد إلى شركتك. يتم ترحيل إيصال استلام المنتجات في نفس الوقت. تظهر أوامر شراء الشحن هذه فقط في صفحة **أوامر الشراء التي تستهلك مخزون الشحن**. لا يتم تضمينها في صفحة **كافة أوامر الشراء المؤكدة‬** في الوحدة النمطية **تعاون المورد**.
-   **المنتجات التي تم استلامها من مخزون الشحن‬** -تذكر هذه الصفحة كافة الحركات حيث انتقلت ملكية المنتجات من المورد إلى شركتك. باستطاعة الموردين استخدام هذه المعلومات لفوترة العميل.
-   **مخزون الشحن الفعلي‬** - تعرض هذه الصفحة مخزون الشحن الفعلي‬ الذي يملكه المورد والذي تم استلامه في مستودعك.




