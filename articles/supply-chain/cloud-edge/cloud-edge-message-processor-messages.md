---
title: رسائل معالج الرسالة
description: يوفر هذا الموضوع معلومات حول ميزة رسائل معالج الرسائل لأحمال عمل وحدة القياس.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysMessageProcessorMessage, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 03d8cad743ac2b2b1e7b2832b8272ca3dbf5a163
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021045"
---
# <a name="message-processor-messages"></a>رسائل معالج الرسالة

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

تُستخدم رسائل معالج الرسائل عند تشغيل وحدات القياس السحابية والحافة لـ [أحمال عمل التصنيع](cloud-edge-workload-manufacturing.md) و[أحمال عمل إدارة المستودع](cloud-edge-workload-warehousing.md).

يتم تبادل قدر كبير من البيانات بين المحور وبيئات نشر وحدة القياس لإبقائها متزامنة، ولكن سيتم معالجة عدد قليل فقط من عمليات تبادل البيانات هذه بواسطة *معالج الرسائل*. يمكنك عرض الرسائل التي تمت معالجتها بواسطة معالج الرسائل بالانتقال إلى **إدارة النظام > معالج الرسائل > رسائل معالج الرسائل**.

## <a name="message-grid-columns-and-filters"></a>أعمده وعوامل تصفية شبكه الرسائل

يمكنك استخدام الحقول الموجودة أعلى صفحة **رسائل معالج الرسائل** للمساعدة في العثور على أي رسائل معينة تبحث عنها. تطابق معظم عوامل التصفية هذه عناوين الأعمدة في شبكة الرسائل. تتوفر عوامل التصفية وعناوين الأعمده التالية:

- **نوع الرسالة** – يحدد نوع الرسالة.
- **قائمة انتظار الرسائل** – تحدد اسم قائمة الانتظار التي ستتم معالجة الرسالة فيها. يتم توفير قوائم الانتظار التالية:
  - *وحدة القياس إلى المركز*
  - *وحده مقياس تنفيذ المركز إلى المستودع*
  - *المركز لوحدة قياس تنفيذ التصنيع*
- **حالة الرسالة** – تحدد حالة الرسالة. تتوفر الحالات التالية:
  - *في قائمة الانتظار* – الرسالة جاهزة للمعالجة بواسطة معالج الرسائل.
  - *تمت المعالجة* – تمت معالجة الرسالة بنجاح بواسطة معالج الرسائل.
  - *تم الإلغاء* – تمت معالجة الرسالة ولكن فشلت المعالجة.
- **محتوى الرسالة** – يقوم عامل التصفية هذا بالبحث عن نص كامل لمحتوى الرسالة. (لا يظهر محتوى الرسالة في الشبكة.) يعامل عامل التصفية الرموز الخاصة (مثل "-") على أنها مسافات، ويعامل جميع أحرف المسافات كعوامل تشغيل OR منطقية. T = على سبيل المثال، هذا يعني أنك إذا كنت تبحث عن قيمة `journalid` محددة تساوي "USMF-123456"، سيجد النظام جميع الرسائل التي تحتوي على "USMF" أو "123456"، والتي من المحتمل أن تكون قائمة طويلة. ولذلك، من الأفضل إدخال "123456" فقط لأن ذلك سيؤدي إلى نتائج أكثر تحديدًا.

## <a name="example-message-type-request-inventory-adjustment-financial-update"></a>مثال لنوع الرسالة: طلب تحديث مالي لتسوية المخزون

على سبيل المثال، يتم استخدام **نوع الرسالة** *طلب تحديث مالي لتسوية المخزون* لإنشاء ونشر دفتر يومية جرد على المركز عندما يستخدم عامل تطبيق المستودع من أجل [تسجيل تسوية مخزون](cloud-edge-warehouse-inventory-adjustment.md) في حمل عمل إدارة مستودع وحدة القياس. لأن هذه العملية المحددة تنشأ من وحدة قياس، فإن **قائمة انتظار الرسائل** ستعرض قيمة *وحدة القياس للمركز*.

بالنسبة لنوع الرسالة هذا، يسجل حمل عمل وحدة القياس الرسالة كجزء من عملية تسوية مخزون تطبيق المستودع. يتم بعد ذلك نقل بيانات الرسالة إلى الموزع كجزء من نفس العملية المستخدمة في [بنية Commerce data exchange](../../commerce/commerce-architecture.md). سيتم تحديث الرسالة لعرض **حالة الرسالة** كـ *في قائمة الانتظار*. ثم يحاول معالج الرسائل معالجة الرسالة ويقوم بتحديث **حالة الرسالة** إلى *تمت المعالجة* في حالة النجاح أو *تم الإلغاء* في حالة الفشل.

## <a name="view-the-message-log-message-content-and-details"></a>عرض سجل الرسائل ومحتوى الرسائل والتفاصيل

يمكنك العثور على معلومات مفصلة حول رسالة عن طريق تحديدها في الشبكة ثم فتح علامة التبويب **السجل** أو **محتوى الرسالة** ضمن شبكة الرسائل، حيث يتم عرض كل حدث معالجة.

يعتمد **محتوى الرسالة** على **نوع الرسالة** وبالتالي سيكون له طول نص مختلف. سيبدأ نص محتوى الرسالة النموذجي بـ **{** وسينتهي بـ **}** وبينهما يكون له أسماء حقول مثل `journalId` متبوعة بـ **:** وقيمة مثل *USMF-123456*.

يتضمن شريط الأدوات الموجود في علامة التبويب **السجل** الأزرار التالية:

- **السجل** – يعرض نتائج المعالجة. هذا مفيد بشكل خاص لفهم أسباب فشل معالجة الرسائل التي تحتوي على **نتيجة معالجة** بالحالة *فاشلة*.
- **مجموعة** – يمكن تشغيل عمليات معالجة الرسائل المتعددة كجزء من نفس عملية الدفعة. حدد هذا الزر لعرض هذه البيانات التفصيلية. على سبيل المثال، يمكنك معرفة ما إذا كانت التبعيات موجودة والتي تتطلب من النظام معالجة رسائل معينة في تسلسل معين.

## <a name="message-processor-batch-job"></a>وظيفة دفعة معالج الرسائل

عند تشغيل سحابة ونشر الحافة، يتم إلغاء وظيفة دفعة *معالج الرسائل* تلقائيًا عند إنشاء رسالة جديدة للمعالجة، لذا لن تحتاج إلى جدولة هذه المهمة يدويًا.

وإذا لزم الأمر، يمكنك الوصول إلى وظيفة الدفعة بواسطة الانتقال إلى **إدارة النظام > معالج الرسائل > معالج الرسائل**.

## <a name="manually-process-or-cancel-a-message"></a>معالجة رسالة أو إلغاؤها يدويًا

إذا لزم الأمر، يمكنك معالجه رسالة أو إلغاؤها يدويًا، وذلك وفقًا لحالتها الحالية. للقيام بذلك، حدد الرسالة الموجودة في الشبكة ثم حدد **معالجة** أو **إلغاء الأمر** في جزء الإجراءات

## <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a>إعداد أحداث العمل لتسليم تنبيهات لنتائج المعالجة الفاشلة

بالإضافة إلى أن تصفية قيمة **حالة الرسالة** *تم إلغاؤها* للاستعلام عن الرسائل الفاشلة، يمكنك إعداد [أحداث الأعمال](../../fin-ops-core/dev-itpro/business-events/home-page.md) في المركز لتنبيهك إلى نتائج المعالجة الفاشلة. للقيام بذلك، قم بتنشيط حدث العمل المسمى *تمت معالجة رسالة معالج الرسائل* في صفحة **كتالوج أحداث الأعمال** (**إدارة النظام > الإعداد > أحداث الأعمال > كتالوج أحداث الأعمال**).

كجزء من عملية التنشيط، سيتم إرشادك لتحديد ما إذا كان الحدث خاصًا بواحد أو جميع الكيانات القانونية وتقديم **اسم النهاية**، الذي يجب تحديده أولاً.

>[!NOTE]
> في حالة تعيين **عند حدوث حدث أعمال** إلى *Microsoft Power Automate* (بدلاً من *HTTPS*، مثلاً)، فسيتم إنشاء **اسم نقطة النهاية** تلقائيًا في Supply Chain Management استنادًا إلى إعداد *Microsoft Power Automate*.

### <a name="microsoft-power-automate-example"></a>مثال لـ Microsoft Power Automate

في هذا المثال، استخدم **عند حدوث حدث أعمال** مع قيام *Microsoft Power Automate* بإرسال رسائل البريد الإلكتروني التي تحتوي على رسائل InfoLog والارتباطات التشعبية لفتح صفحة **رسائل معالج الرسائل** للحصول على رسالة فاشلة محددة في توزيع المركز. إذا لزم الأمر، يمكنك إضافة منطق إضافي لإرسال الإشعارات بالتوازي باستخدام قنوات مختلفة والتحكم في المستلمين بناءً على بيانات الحدث.

1. في [Power Automate](https://preview.flow.microsoft.com)، أنشئ تدفقًا سحابيًا تلقائيًا جديدًا لمشغل التدفق **عند حدوث حدث عمل - تطبيق Fin & Ops ‏(Dynamics 365)** متبوعةً بخطوتي **تحليل JSON** و **إرسال رسالة بريد إلكتروني**، كما هو مبين في الرسو التوضيحي التالي.

    :::image type="content" source="./media/cloud-edge-power-automate-example1.png" alt-text="تدفق السحابة التلقائي في Power Automate":::

1. في خطوة **عند حدوث حدث أعمال**، يمكنك البحث أو إدخال **مثيل** المركز متبوعًا بـ **الفئة** ثم **حدث الأعمال** *تمت معالجة رسالة معالج الرسائل*، كما هو مبين في الرسم التوضيحي التالي.

    :::image type="content" source="./media/cloud-edge-power-automate-example2.png" alt-text="Power Automate خطوة عند حدوث حدث أعمال":::

1. بالنسبة لخطوة **تحليل JSON**، أدخل **المخطط** الذي يحدد الحقول الموسعة. يمكنك استخدام خيار *تنزيل المخطط* في صفحة **كتالوج أحداث الأعمال** في Supply Chain Management أو ابدأ باللصق في مثال نص المخطط. يتم توفير نص المثال هذا بعد الرسم التوضيحي التالي.

    :::image type="content" source="./media/cloud-edge-power-automate-example3.png" alt-text="Power Automate خطوة تحليل JSON":::

    ```json
    {
        "properties": {
            "BusinessEventId": {
                "type": "string"
            },
            "ControlNumber": {
                "type": "integer"
            },
            "EventId": {
                "type": "string"
            },
            "EventTime": {
                "type": "string"
            },
            "MajorVersion": {
                "type": "integer"
            },
            "MessageContent": {
                "type": "string"
            },
            "MessageDestinationCompanyId": {
                "type": "string"
            },
            "MessageDestinationOperationalSiteId": {
                "type": "string"
            },
            "MessageDestinationWarehouseId": {
                "type": "string"
            },
            "MessageDestinationWorkloadName": {
                "type": "string"
            },
            "MessageInfolog": {
                "type": "string"
            },
            "MessageProcessingResult": {
                "type": "string"
            },
            "MessageProcessingResultLabel": {
                "type": "string"
            },
            "MessageProcessorMessagePageUrl": {
                "type": "string"
            },
            "MessageQueue": {
                "type": "string"
            },
            "MessageQueueLabel": {
                "type": "string"
            },
            "MessageSourceCompanyId": {
                "type": "string"
            },
            "MessageSourceOperationalSiteId": {
                "type": "string"
            },
            "MessageSourceWarehouseId": {
                "type": "string"
            },
            "MessageSourceWorkloadName": {
                "type": "string"
            },
            "MessageState": {
                "type": "string"
            },
            "MessageStateLabel": {
                "type": "string"
            },
            "MessageType": {
                "type": "string"
            },
            "MessageTypeLabel": {
                "type": "string"
            },
            "MinorVersion": {
                "type": "integer"
            }
        },
        "type": "object"
    }
    ```

1. في خطوة **إرسال رسالة بريد إلكتروني**، يمكنك تحديد الحقول الفردية أو البدء بلصق مثال نص البريد الإلكتروني في حقل **المحتوى**. يتم توفير هذا المثال بعد الرسم التوضيحي التالي.

    :::image type="content" source="./media/cloud-edge-power-automate-example4.png" alt-text="خطة إرسال رسالة بريد إلكتروني في Power Automate":::

    ```plaintext
    Message queue: @{body('Parse_JSON')?['MessageQueue']}
    Message queue label: @{body('Parse_JSON')?['MessageQueueLabel']}
    Message type: @{body('Parse_JSON')?['MessageQueueType']}
    Message type label: @{body('Parse_JSON')?['MessageQueueTypeLabel']}
    Message content: @{body('Parse_JSON')?['MessageContent']}
    Message state: @{body('Parse_JSON')?['MessageState']}
    Message state label: @{body('Parse_JSON')?['MessageStateLabel']}
    Message processing result: @{body('Parse_JSON')?['MessageProcessingResult']}
    Message processing result label: @{body('Parse_JSON')?['MessageProcessingResultLabel']}
    Message infolog: @{body('Parse_JSON')?['MessageInfolog']}
    Message source company ID: @{body('Parse_JSON')?['MessageSourceCompanyId']}
    Message source workload name: @{body('Parse_JSON')?['MessageSourceWorkloadName']}
    Message source site ID: @{body('Parse_JSON')?['MessageSourceOperationalSiteId']}
    Message source warehouse ID: @{body('Parse_JSON')?['MessageSourceWarehouseId']}
    Message destination company ID: @{body('Parse_JSON')?['MessageDestinationCompanyId']}
    Message destination workload name: @{body('Parse_JSON')?['MessageDestinationWorkloadName']}
    Message destination site ID: @{body('Parse_JSON')?['MessageDestinationOperationalSiteId']}
    Message destination warehouse ID: @{body('Parse_JSON')?['MessageDestinationWarehouseId']}
    Message processor message page URL: @{body('Parse_JSON')?['MessageProcessorMessagePageUrl']}
    ```

1. عند حفظ حدث العمل، سيتم تنشيطه تلقائيًا ويكون جاهزًا للاستخدام كجزء من Supply Chain Management.
