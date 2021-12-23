---
title: التكامل مع أنظمة تنفيذ التصنيع التابعة لجهات خارجية
description: يشرح هذا الموضوع كيف يمكنك دمج Microsoft Dynamics 365 Supply Chain Management مع نظام تنفيذ التصنيع لجهة خارجية (MES).
author: t-benebo
ms.date: 10/01/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-10-01
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 43814023474d44b8c95bae087c7b6a4d52d21471
ms.sourcegitcommit: 7cbd53617af179a0de74aae30c149edc95e86684
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/06/2021
ms.locfileid: "7891916"
---
# <a name="integrate-with-third-party-manufacturing-execution-systems"></a>التكامل مع أنظمة تنفيذ التصنيع التابعة لجهات خارجية

[!include [banner](../includes/banner.md)]

تستخدم بعض مؤسسات التصنيع التي تستخدم Microsoft Dynamics 365 Supply Chain Management الوظائف الأصلية في Dynamics 365 للتحكم في أنشطة التصنيع الخاصة بها للآلات والمعدات والموظفين. ومع ذلك، فإن مؤسسات التصنيع الأخرى، خاصة تلك التي لديها متطلبات تصنيع متقدمة، تستخدم نظام تنفيذ التصنيع لطرف ثالث (MES) بدلاً من ذلك. قد تختار المؤسسات حل MES لجهة خارجية لأنه، على سبيل المثال، مصمم خصيصًا للصناعة الرأسية الخاصة بهم.

في الحل المتكامل، يتم تبادل البيانات آليًا بالكامل ويحدث في الوقت الفعلي تقريبًا. لذلك، يتم الاحتفاظ بالبيانات محدثة في كلا النظامين، ولا يلزم إدخال بيانات يدويًا. على سبيل المثال، عند تسجيل استهلاك المواد في MES، يضمن التكامل تسجيل نفس الاستهلاك أيضًا في Dynamics 365. لذلك، تتوفر سجلات المخزون الحديثة لعمليات مهمة أخرى، مثل التخطيط والمبيعات.

يجعل الحل من الاندماج أسرع وأسهل وأرخص تكلفة لمستخدمي Supply Chain Management مع الأنظمة MES التابعة لجهات خارجية. يقدم الميزات التالية:

- واجهات وأحداث العمل التي تدعم [عمليات تنفيذ التصنيع الرئيسية](#processes-available-for-mes-integration)
- لوحة معلومات مركزية حيث يمكنك تتبع محفوظات معالجة الحدث واستكشاف الأخطاء وإصلاحها وإصلاح العمليات التي تفشل

يوضح الرسم التوضيحي التالي مجموعة نموذجية من أحداث الأعمال والعمليات والرسائل التي يتم تبادلها في حل متكامل.

![سيناريو التكامل النموذجي.](media/3p-mes-scenario.png "سيناريو التكامل النموذجي.")

## <a name="turn-on-the-mes-integration-feature"></a>تشغيل ميزة تكامل MES

قبل أن تتمكن من استخدام هذه الميزة، يجب تشغيلها في النظام. بإمكان المسؤولين استخدام إعدادات [دارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها. في مساحة عمل **إدارة الميزات**، تكون هذه الميزة مدرجة بالطريقة التالية:

- **الوحدة النمطية:** *التحكم بالإنتاج*
- **اسم الميزة:** *تكامل أنظمة تنفيذ التصنيع*

## <a name="processes-available-for-mes-integration"></a>العمليات المتاحة لتكامل MES

يمكنك تمكين أي من العمليات التالية أو جميعها للتكامل.

| اسم العملية | Description |
|---|---|
| تحرير أوامر الإنتاج وتغيير حالة أمر الإنتاج وأحداث العمل | توفر هذه العملية حدثًا تجاريًا يمكن أن تستمع إليه MES، للحصول على معلومات حول أوامر الإنتاج التي ينبغي إنتاجها. من المتوقع مشاركة البيانات المرجعية المتعلقة بأمر الإنتاج من Supply Chain Management إلى MES من خلال بروتوكول البيانات المفتوحة (OData) أو كيانات البيانات. |
| بدء أمر الإنتاج | توفر هذه العملية لـ Supply Chain Management معلومات حول أوامر الإنتاج التي يتم بدء تشغيلها باستخدام MES. يضمن أن كلا النظامين لهما عرض محدث لجميع أنشطة التصنيع. |
| الإبلاغ عن الكمية المنتجة أو الملغاة | توفر هذه العملية لـ Supply Chain Management معلومات حول كميات البضائع والخطأ التي يتم الإبلاغ عنها في وظيفة الإنتاج باستخدام MES. إنه يضمن أن المشرفين على أرض المتجر لديهم عرض محدث لتقدم خطة الإنتاج. |
| الإبلاغ عن استهلاك المواد | توفر هذه العملية لـ Supply Chain Management معلومات من MES حول كميات المواد المستهلكة. إنه يجعل سجلات المخزون المحدثة متاحة للعمليات الهامة الأخرى، مثل التخطيط والمبيعات. |
| الإبلاغ عن الوقت المستغرق في العملية | تزود هذه العملية Supply Chain Management بمعلومات حول الوقت المستخدم لعملية معينة. |
| إنهاء أمر الإنتاج | تُعلم هذه العملية Supply Chain Management بأن MES قد قامت بتحديث أمر الإنتاج إلى حالته النهائية *منتهي*. تشير هذه الحالة إلى أنه لن يتم إنتاج المزيد من الكميات في أمر الإنتاج. |

## <a name="monitor-incoming-messages"></a>مراقبة الرسائل الواردة

لمراقبة الرسائل الواردة إلى النظام، افتح صفحة **تكامل أنظمة تنفيذ التصنيع**. هناك، يمكنك عرض المشكلات ومعالجتها واستكشاف الأخطاء وإصلاحها.

## <a name="call-the-api"></a>استدعاء API

للاتصال بواجهة برمجة تطبيقات تكامل MES، أرسل طلب `POST` إلى عنوان URL لنقطة النهاية التالية:

`/api/services/SysMessageServices/SysMessageService/SendMessage`

يجب أن يكون نص الطلب الذي ترسله مشابهًا للمثال التالي. قم باستبدال قيم `_companyId`، و`_messageType`، و`_messageContent` على النحو المطلوب. للحصول على معلومات حول أنواع الرسائل المختلفة التي تدعمها API وكيفية تصميم محتواها، راجع القسم التالي.

```json
{
    "_companyId": "USMF",
    "_messageQueue": "JmgMES3P",
    "_messageType": "ProdProductionOrderReportFinished",
    "_messageContent":
    "{\"ProductionOrderNumber\": \"P000123\", \"ReportFinishedLines\": [{\"ItemNumber\": \"A0001\", \"ReportedGoodQuantity\": 10, \"ReportAsFinishedDate\": \"2021-01-01\"}]}"
}
```

## <a name="api-message-types-and-content"></a>أنواع رسائل API ومحتوياتها

يصف هذا القسم كل نوع من أنواع الرسائل التي يمكن تبادلها من خلال واجهة برمجة تطبيقات تكامل MES.

### <a name="start-production-order-message"></a>رسالة بدء أمر الإنتاج

بالنسبة إلى رسالة *بدء أمر الإنتاج*، تكون قيمة `_messageType` هي `ProdProductionOrderStart`. يوضح الجدول التالي الحقول التي تدعمها هذه الرسالة.

| اسم الحقل | Status | النوع |
|---|---|---|
| `ProductionOrderNumber` | إلزامي | سلسلة |
| `StartedQuantity` | اختياري | حقيقي |
| `StartedDate` | اختياري | التاريخ |
| `AutomaticBOMConsumptionRule` | اختياري | التعداد (FlushingPrincip \| دائمًا \| أبدًا) |

### <a name="report-as-finished-message"></a>رسالة الإبلاغ عنها كمنتهية

بالنسبة لرسالة *الإبلاغ عنها كمنتهية*، تكون قيمة `_messageType` هي `ProdProductionOrderReportFinished`. يوضح الجدول التالي الحقول التي تدعمها هذه الرسالة.

| اسم الحقل | Status | النوع |
|---|---|---|
| `ProductionOrderNumber` | إلزامي | سلسلة |
| `ReportFinishedLines` | إلزامي | قائمة السطور (واحد على الأقل)، يحتوي كل منها على الحمولة الموضحة في الجدول التالي |

يعرض الجدول التالي الحقول التي يدعمها كل سطر في قسم `ReportFinishedLines` من رسالة `ProdProductionOrderReportFinished`.

| اسم الحقل | Status | النوع |
|---|---|---|
| `LineNumber` | اختياري | حقيقي |
| `ItemNumber` | اختياري | سلسلة|
| `ProductionType` | اختياري | التعداد (MainItem \| الصيغة \| BOM \| Co_Product \| By_Product \| لا شيء)، قابل للتوسيع |
| `ReportedErrorQuantity` | اختياري | حقيقي|
| `ReportedGoodQuantity` | اختياري | حقيقي|
| `ReportedErrorCatchWeightQuantity` | اختياري | حقيقي |
| `ReportedGoodCatchWeightQuantity` | اختياري | حقيقي |
| `AcceptError` | اختياري |منطقي |
| `ErrorCause` | اختياري | التعداد (لا شيء \| المواد \| الجهاز \| OperatingStaff)، قابل للتوسيع |
| `ExecutedDateTime` | اختياري | التاريخ/الوقت |
| `ReportAsFinishedDate` | اختياري | التاريخ |
| `AutomaticBOMConsumptionRule` | اختياري | التعداد (FlushingPrincip \| دائمًا \| أبدًا) |
| `AutomaticRouteConsumptionRule` | اختياري |التعداد (RouteDependent \| دائمًا \| أبدًا) |
| `RespectFlushingPrincipleDuringOverproduction` | اختياري | منطقي |
| `ProductionJournalNameId` | اختياري | سلسلة |
| `PickingListProductionJournalNameId` | اختياري | سلسلة|
| `RouteCardProductionJournalNameId` | اختياري | سلسلة |
| `FromOperationNumber` | اختياري | عدد صحيح|
| `ToOperationNumber` | اختياري | عدد صحيح|
| `InventoryLotId` | اختياري | سلسلة |
| `BaseValue` | اختياري | سلسلة |
| `EndJob` | اختياري | منطقي |
| `EndPickingList` | اختياري | منطقي |
| `EndRouteCard` | اختياري | منطقي |
| `PostNow` | اختياري | منطقي |
| `AutoUpdate` | اختياري | منطقي |
| `ProductColorId` | اختياري | سلسلة|
| `ProductConfigurationId` | اختياري | سلسلة |
| `ProductSizeId` | اختياري | سلسلة |
| `ProductStyleId` | اختياري | سلسلة |
| `ProductVersionId` | اختياري | سلسلة |
| `ItemBatchNumber` | اختياري | سلسلة |
| `ProductSerialNumber` | اختياري | سلسلة |
| `LicensePlateNumber` | اختياري | سلسلة |
| `InventoryStatusId` | اختياري | سلسلة |
| `ProductionWarehouseId` | اختياري | سلسلة |
| `ProductionSiteId` | اختياري | سلسلة |
| `ProductionWarehouseLocationId` | اختياري | سلسلة |
| `InventoryDimension1` إلى `InventoryDimension12` | اختياري | سلسلة |

تتطلب الأبعاد الـ 12 القابلة للتوسيع (`InventoryDimension1` حتى `InventoryDimension12`) تخصيصًا ولا يتم استخدامها دائمًا. لمزيد من المعلومات حول هذه الأبعاد، راجع [إضافة أبعاد مخزون جديدة من خلال التوسيع](../../fin-ops-core/dev-itpro/extensibility/inventory-dimensions.md)

### <a name="material-consumption-picking-list-message"></a>رسالة استهلاك المواد (قائمة الانتقاء)

بالنسبة إلى رسالة *استهلاك المواد (قائمة الانتقاء)*، تكون قيمة `_messageType` هي `ProdProductionOrderPickingList`. يوضح الجدول التالي الحقول التي تدعمها هذه الرسالة.

| اسم الحقل | Status | النوع |
|---|---|---|
| `ProductionOrderNumber` | إلزامي | سلسلة |
| `JournalNameId` | اختياري | سلسلة |
| `PickingListLines` | إلزامي | قائمة السطور (واحد على الأقل)، يحتوي كل منها على الحمولة الموضحة في الجدول التالي |

يعرض الجدول التالي الحقول التي يدعمها كل سطر في قسم `PickingListLines` من رسالة `ProdProductionOrderPickingList`.

| اسم الحقل | Status | النوع |
|---|---|---|
| `ItemNumber` | إلزامي | سلسلة |
| `ConsumptionBOMQuantity` | اختياري | حقيقي |
| `ProposalBOMQuantity` | اختياري | حقيقي |
| `ScrapBOMQuantity` | اختياري | حقيقي |
| `BOMUnitSymbol` | اختياري | سلسلة |
| `ConsumptionInventoryQuantity` | اختياري | حقيقي |
| `ProposalInventoryQuantity` | اختياري | حقيقي |
| `ConsumptionCatchWeightQuantity` | اختياري | حقيقي |
| `ProposalCatchWeightQuantity` | اختياري | حقيقي |
| `ConsumptionDate` | اختياري | التاريخ |
| `OperationNumber` | اختياري | عدد صحيح |
| `LineNumber` | اختياري | حقيقي |
| `PositionNumber` | اختياري | سلسلة |
| `IsConsumptionEnded` | اختياري | منطقي |
| `ErrorCause` | اختياري | التعداد (لا شيء \| المواد \| الجهاز \| OperatingStaff)، قابل للتوسيع |

### <a name="time-used-for-operation-route-card-message"></a>رسالة الوقت المستخدم للتشغيل (بطاقة الطريق)

بالنسبة إلى رسالة *الوقت المستخدم للتشغيل (بطاقة الطريق)*، تكون قيمة `_messageType` هي `ProdProductionOrderRouteCard`. يوضح الجدول التالي الحقول التي تدعمها هذه الرسالة.

| اسم الحقل | Status | النوع |
|---|---|---|
| `ProductionOrderNumber` | إلزامي | سلسلة |
| `JournalNameId` | اختياري | سلسلة |
| `RouteCardLines` | إلزامي | قائمة السطور (واحد على الأقل)، يحتوي كل منها على الحمولة الموضحة في الجدول التالي |

يعرض الجدول التالي الحقول التي يدعمها كل سطر في قسم `RouteCardLines` من رسالة `ProdProductionOrderRouteCard`.

| اسم الحقل | Status | النوع |
|---|---|---|
| `OperationNumber` | إلزامي | عدد صحيح |
| `OperationPriority` | اختياري | التعداد (أساسي \| ثانوي1 \| ثانوي2 \| ... \| ثانوي20) |
| `OperationId` | اختياري | سلسلة |
| `OperationsResourceId` | اختياري | سلسلة |
| `Worker` | اختياري | سلسلة |
| `HoursRouteCostCategoryId` | اختياري | سلسلة |
| `QuantityRouteCostCategoryId` | اختياري | سلسلة |
| `HourlyRate` | اختياري | حقيقي |
| `Hours` | اختياري | حقيقي |
| `GoodQuantity` | اختياري | حقيقي |
| `ErrorQuantity` | اختياري | حقيقي |
| `CatchWeightGoodQuantity` | اختياري | حقيقي |
| `CatchWeightErrorQuantity` | اختياري | حقيقي |
| `QuantityPrice` | اختياري | حقيقي |
| `ProcessingPercentage` | اختياري | حقيقي |
| `ConsumptionDate` | اختياري | التاريخ |
| `TaskType` | اختياري | التعداد (QueueBefore \| الإعداد \| العملية \| التداخل \| النقل \| QueueAfter \| العبء) |
| `ErrorCause` | اختياري | التعداد (لا شيء \| المواد \| الجهاز \| OperatingStaff)، قابل للتوسيع |
| `OperationCompleted` | اختياري | منطقي |
| `BOMConsumption` | اختياري | منطقي |
| `ReportAsFinished` | اختياري | منطقي |

### <a name="end-production-order-message"></a>رسالة انتهاء أمر الإنتاج

بالنسبة إلى رسالة *انتهاء أمر الإنتاج*، تكون قيمة `_messageType` هي `ProdProductionOrderEnd`. يوضح الجدول التالي الحقول التي تدعمها هذه الرسالة.

| اسم الحقل | Status | النوع |
|---|---|---|
| `ProductionOrderNumber` | إلزامي | سلسلة |
| `ExecutedDateTime` | اختياري | التاريخ/الوقت |
| `EndedDate` | اختياري | التاريخ |
| `UseTimeAndAttendanceCost` | اختياري | منطقي |
| `AutoReportAsFinished` | اختياري | منطقي |
| `AutoUpdate` | اختياري | منطقي |

## <a name="receive-feedback-about-the-state-of-a-message"></a>تلقي ملاحظات حول حالة الرسالة

بعد أن ترسل MES رسالة إلى Supply Chain Management، قد يكون من المناسب لإدارة سلسلة التوريد إرجاع ملاحظات حول حالة الرسالة. فيما يلي بعض الأمثلة على الحالات التي قد يكون فيها هذا السلوك ملائمًا:

- لا يوجد شخص مسؤول عن الإشراف المستمر على تكامل MES.
- يريد الشخص المسؤول عن الإشراف على تكامل MES أن يتم إخطاره عبر البريد الإلكتروني عند فشل إحدى الرسائل، حتى يعلموا أنه يتعين عليهم اتخاذ إجراء.
- يجب أن تعرض MES رسالة خطأ لإبلاغ عامل المتجر أو أي شخص من قسم تكنولوجيا المعلومات بأنه يتعين عليهم اتخاذ إجراء.
- يجب أن تعيد MES حساب جدول الأمر بعد أن تتلقى رسالة فشل (على سبيل المثال، بسبب فشل بدء أمر الإنتاج).

في هذه الحالات، يمكنك الاستفادة من ميزة التنبيه القياسية في Supply Chain Management. للحصول على معلومات حول كيفية عمل التنبيهات القياسية، راجع الموارد التالية:

- موضوع التعليمات: [نظرة عامة على التنبيهات](../../fin-ops-core/fin-ops/get-started/alerts-overview.md)
- الفيديو: [خيارات قواعد التنبيهات في Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=cpzimwOjicM&ab_channel=MicrosoftDynamics365)

على سبيل المثال، يمكنك إعداد التنبيهات التالية لتقديم ملاحظات حول حالة الرسالة:

- قم بإنشاء حدث عمل ("إرسال خارجيًا") يتم استخدامه عندما تكون الرسالة *فاشلة*.
- أرسل إشعارًا وبريدًا إلكترونيًا إلى مسؤول تكنولوجيا المعلومات أو مدير طابق الإنتاج.
