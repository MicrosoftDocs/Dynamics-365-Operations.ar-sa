---
title: كيانات إنشاء الرحلة
description: يوفر هذا الموضوع معلومات حول كيانات بيانات إنشاء الرحلة، والتي تجمع كيانات البيانات المطلوبة لإنشاء رحلة عمل.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 17f63af3ce1f858ed3e2086fc81c5e17c5e76be0
ms.sourcegitcommit: 611202adaa080250636efabb3b3b32b850d92d04
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/28/2022
ms.locfileid: "8813025"
---
# <a name="voyage-creation-entities"></a>كيانات إنشاء الرحلة

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.28 -->

تجمع كيانات بيانات إنشاء الرحلة معًا كيانات البيانات المطلوبة لإنشاء رحلة عمل. يمكنك أنت أو وكيل الشحن الخاص بك استخدام كيانات البيانات هذه لإنشاء سجلات الرحلة وحاوية الشحن والسجلات وبند الرحلة التي تشير إلى أمر المشتري الحالي أو بنود أوامر النقل.

## <a name="voyages-itmtableentity"></a>الرحلات (ITMTableEntity)

تمثل الرحلة رحلة البضائع الواردة وتعمل كأعلى مستوى تكلفة في تكلفة الوصول. يحتوي على معلومات على مستوى الرأس تتعلق بالسفينة وميناء المنشأ وميناء الوجهة. هذه الوظيفة مدعومة من قِبل كيان `ITMTableEntity`. يسرد الجدول التالي الحقول والتعيينات التي تشكل هذا الكيان.

| Name | التعيين | نوع البيانات | مفتاح | إلزامي |
|---|---|---|---|---|
| وضع التسليم | ITMTable.DlvModeId | Nvarchar(10) | لا | لا |
| موصى به من قِبل الوسيط | ITMTable.ITMBrokerAdvised | التاريخ والوقت | لا | لا |
| موعد العميل | ITMTable.ITMCustomerAppointment | التاريخ والوقت | لا | لا |
| تم التسليم في المستودع | ITMTable.ITMDelAtWarehouse | التاريخ والوقت | لا | لا |
| إرشادات التسليم | ITMTable.ITMDeliveryInstructions | التاريخ والوقت | لا | لا |
| تاريخ المغادرة | ITMTable.ITMDepartureDate | التاريخ والوقت | لا | لا |
| إصدار البضائع | ITMTable.ITMGoodsReleased | التاريخ والوقت | لا | لا |
| تاريخ النقل المحلي | ITMTable.ITMLocalTransportDate | التاريخ والوقت | لا | لا |
| وقت النقل المحلي | ITMTable.ITMLocalTransportTime | الفترة | لا | لا |
| تم إرسال بوليصة الشحن الأصلية | ITMTable.ITMOriginalBOLSebt | التاريخ والوقت | لا | لا |
| تم استلام المستندات الأصلية | ITMTable.ITMOriginalDocsReceived | التاريخ والوقت | لا | لا |
| حالة أمر الشراء | ITMTable.ITMPurchStatus | الفترة | لا | لا |
| تاريخ التحقق | ITMTable.ITMVerificationDate | التاريخ والوقت | لا | لا |
| معرف الإدخال الجمركي | ITMTable.ShipCustomsEntryId | Nvarchar(20) | لا | لا |
| تاريخ الشحن | ITMTable.ShipDate | التاريخ والوقت | لا | لا |
| ‏‏الوصف‬ | ITMTable.ShipDescription | Nvarchar(60) | لا | لا |
| المستندات المستلمة | ITMTable.ShipDocReceived | الفترة | لا | لا |
| تاريخ التسليم المقدّر | ITMTable.ShipEstDlvDate | التاريخ والوقت | لا | لا |
| وقت الوصول المقدّر في مرفأ الشحن | ITMTable.ShipEstPortDate | التاريخ والوقت | لا | لا |
| مرفأ المغادرة | ITMTable.ShipFromPort | Nvarchar(20) | لا | لا |
| بوليصة الشحن الجوي للمنزل/بوليصة الشحن | ITMTable.ShipHAWB | Nvarchar(20) | لا | لا |
| الرحلة البحرية | ITMTable.ShipId | Nvarchar(20) | **نعم** | **نعم** |
| مرجع الحجز | ITMTable.ShipIdExternal | Nvarchar(20) | لا | لا |
| قالب الرحلة | ITMTable.ShipJourneyId | Nvarchar(20) | لا | لا |
| وكيل شحن محلي | ITMTable.ShipLocalForwarder | Nvarchar(20) | لا | لا |
| بوليصة الشحن الجوي الرئيسية/بوليصة الشحن | ITMTable.ShipMAWB | Nvarchar(20) | لا | لا |
| القياس | ITMTable.ShipMeasurement | Numeric(32, 6) | لا | لا |
| وحدة القياس | ITMTable.ShipMeasurementUnit | الفترة | لا | لا |
| عدد البالتات | ITMTable.ShipNoOfPallets | الفترة | لا | لا |
| رحلة بحرية معلّقة | ITMTable.ShipPending | الفترة | لا | لا |
| ملاحظات | ITMTable.ShipRemarks | Nvarchar(MAX) | لا | لا |
| الإيجار | ITMTable.ShipRental | الفترة | لا | لا |
| حالة الرحلة البحرية | ITMTable.ShipStatusId | Nvarchar(20) | لا | لا |
| حساب العدد | ITMTable.ShipTallyInNumber | Nvarchar(20) | لا | لا |
| إلى المرفأ | ITMTable.ShipToPort | Nvarchar(20) | لا | لا |
| تاريخ التقييم | ITMTable.ShipValuationDate | التاريخ والوقت | لا | لا |
| شركة الشحن | ITMTable.ShipVendAccount | Nvarchar(20) | لا | لا |
| الباخرة | ITMTable.ShipVesselId | Nvarchar(20) | لا | **نعم** |
| معرف رحلة بحرية خارجية | ITMTable.ShipVoyage | Nvarchar(20) | لا | لا |

### <a name="number-sequences-for-voyages"></a>التسلسلات الرقمية للرحلات

التسلسل الرقمي المشترك للرحلات يتحكم في تخصيص معرفات الرحلة.

تُستخدم القيمة التي تم تمريرها إلى كيان البيانات على أنها **معرف الرحلة** (`ShipId`) لتحديد سجل موجود للتحديث. في حالة عدم وجود هذا السجل، يعتمد السلوك على ما إذا كان التسلسل الرقمي المعين قد تم تكوينه للسماح بالإدخال اليدوي:

- إذا تم تمكين الإدخال اليدوي، يتم إنشاء سجل جديد يستخدم القيمة التي تم تمريرها.
- إذا لم يتم تمكين الإدخال اليدوي، فسيتم استخدام الرقم التالي في التسلسل الرقمي المخصص بدلاً من القيمة التي تم تمريرها.

أثناء جلسة الاستيراد، يتم الاحتفاظ بقيمة العنصر النائب التي تم استيرادها كمعرف الرحلة. يضمن هذا السلوك تضمين حاوية الشحن وبنود الرحلات التي تشير إلى العنصر النائب في الرحلة، وأنه يتم تحديثها لتعكس القيمة التي تم تعيينها من التسلسل الرقمي.

### <a name="automatic-cost-transactions"></a>حركات التكلفة التلقائية

يمكن إضافة التكاليف التلقائية إلى رحلة من صفحة **التكاليف التلقائية** في Microsoft Dynamics 365 Supply Chain Management (**التكلفة شاملة التفريغ‬‬ \> إعداد التكاليف \> التكاليف التلقائية**). يمكن أيضًا إنشاء سجلات للتكاليف التلقائية باستخدام كيانات بيانات حركات التكلفة لكل منطقة تكلفة تدعمها التكلفة شاملة التفريغ.

يتم تطبيق التكاليف التلقائية التي تم تكوينها في Supply Chain Management على الرحلة عند إنشاء بند رحلة. لن تظهر أي تكاليف مقابل السجل حتى يتم إقران سجل الرأس بمعلومات البند.

## <a name="shipping-containers-itmcontainersentity"></a>حاويات الشحن (ITMContainersEntity)

تمثل حاوية الشحن حاوية مادية يتم نقل البضائع فيها. قد تكون هذه الحاوية المادية حاوية شحن للشحن البحري أو منصة نقالة واحدة للشحن الجوي. تتضمن حاوية الشحن معلومات على مستوى الرأس تتعلق بمعرف حاوية الشحن ورقم الختم ونوع حاوية الشحن. (يوفر نوع حاوية الشحن معلومات البعد.) يتم دعم هذه الوظيفة بواسطة كيان `ITMContainersEntity`. يسرد الجدول التالي الحقول والتعيينات التي تشكل هذا الكيان.

| Name | التعيين | نوع البيانات | مفتاح | إلزامي |
|---|---|---|---|---|
| تاريخ المغادرة | ITMContainers.ITMDepartureDate | التاريخ والوقت | لا | لا |
| تاريخ النقل المحلي | ITMContainers.ITMLocalTransportDate | التاريخ والوقت | لا | لا |
| وقت النقل المحلي | ITMContainers.ITMLocalTransportTime | الفترة | لا | لا |
| الرحلة البحرية الأصلية | ITMContainers.OrigShipId | Nvarchar(20) | لا | لا |
| الوزن الفعلي | ITMContainers.ShipActualWeight | Numeric(32, 6) | لا | لا |
| موصى به من قِبل الوسيط | ITMContainers.ShipBrokerAdvised | التاريخ والوقت | لا | لا |
| حاوية الشحن | ITMContainers.ShipContainerId | Nvarchar(20) | **نعم** | **نعم** |
| نوع حاوية الشحن | ITMContainers.ShipContainerTypeId | Nvarchar(20) | لا | لا |
| نوع الوحدة | ITMContainers.ShipContainerUnitTypeId | Nvarchar(10) | لا | لا |
| تم تحويلها إلى مؤجرة | ITMContainers.ShipConvertedToRental | الفترة | لا | لا |
| موعد العميل | ITMContainers.ShipCustomerAppointment | التاريخ والوقت | لا | لا |
| تاريخ الشحن | ITMContainers.ShipDate | التاريخ والوقت | لا | لا |
| تم التسليم في المستودع | ITMContainers.ShipDelAtWarehouse | التاريخ والوقت | لا | لا |
| إرشادات التسليم | ITMContainers.ShipDeliveryInstructions | التاريخ والوقت | لا | لا |
| تاريخ تطبيق شهادة الفحص | ITMContainers.ShipECAppliedDate | التاريخ والوقت | لا | لا |
| تاريخ انتهاء صلاحية شهادة الفحص | ITMContainers.ShipECExpiryDate | التاريخ والوقت | لا | لا |
| رقم شهادة الفحص | ITMContainers.ShipECNum | Nvarchar(20) | لا | لا |
| تاريخ استلام شهادة الفحص | ITMContainers.ShipECReceivedDate | التاريخ والوقت | لا | لا |
| تاريخ التسليم المقدّر | ITMContainers.ShipEstDlvDate | التاريخ والوقت | لا | لا |
| وقت الوصول المقدّر في مرفأ الشحن | ITMContainers.ShipEstPortDate | التاريخ والوقت | لا | لا |
| تاريخ التحميل المتوقع | ITMContainers.ShipExpectedLoadingDate | التاريخ والوقت | لا | لا |
| مرفأ المغادرة | ITMContainers.ShipFromPort | Nvarchar(20) | لا | لا |
| وصف البضائع | ITMContainers.ShipGoodsDesc | Nvarchar(60) | لا | لا |
| إصدار البضائع | ITMContainers.ShipGoodsReleased | التاريخ والوقت | لا | لا |
| وحدة تعقب GPS | ITMContainers.ShipGPSUnit | Nvarchar(30) | لا | لا |
| بوليصة الشحن الجوي للمنزل/بوليصة الشحن | ITMContainers.ShipHAWB | Nvarchar(20) | لا | لا |
| الرحلة البحرية | ITMContainers.ShipId | Nvarchar(20) | **نعم** | **نعم** |
| قالب الرحلة | ITMContainers.ShipJourneyId | Nvarchar(20) | لا | لا |
| وكيل شحن محلي | ITMContainers.ShipLocalForwarder | Nvarchar(20) | لا | لا |
| القياس | ITMContainers.ShipMeasurement | Numeric(32, 6) | لا | لا |
| وحدة القياس | ITMContainers.ShipMeasurementUnit | الفترة | لا | لا |
| عدد العبوات الكرتونية | ITMContainers.ShipNoOfCartons | Numeric(32, 6) | لا | لا |
| تم إرسال بوليصة الشحن الأصلية | ITMContainers.ShipOriginalBOLSebt | التاريخ والوقت | لا | لا |
| تم استلام المستندات الأصلية | ITMContainers.ShipOriginalDocsReceived | التاريخ والوقت | لا | لا |
| رقم الختم‬ الخاص بنا | ITMContainers.ShipOurSealNum | Nvarchar(20) | لا | لا |
| مستخدم | ITMContainers.ShipPendingUsed | الفترة | لا | لا |
| حالة أمر الشراء | ITMContainers.ShipPurchStatus | الفترة | لا | لا |
| نوع التبريد | ITMContainers.ShipRefrigerationTypeId | Nvarchar(10) | لا | لا |
| ملاحظات | ITMContainers.ShipRemarks | Nvarchar(MAX) | لا | لا |
| الإيجار | ITMContainers.ShipRental | الفترة | لا | لا |
| قابل للإرجاع | ITMContainers.ShipReturnable | الفترة | لا | لا |
| حالة الرحلة البحرية | ITMContainers.ShipStatusId | Nvarchar(20) | لا | لا |
| رقم ختم شركة الشحن | ITMContainers.ShipTheirSealNum | Nvarchar(20) | لا | لا |
| إلى المرفأ | ITMContainers.ShipToPort | Nvarchar(20) | لا | لا |
| تاريخ التحقق | ITMContainers.ShipVerificationDate | التاريخ والوقت | لا | لا |
| الباخرة | ITMContainers.ShipVesselId | Nvarchar(20) | لا | **نعم** |

### <a name="voyage-id-validation"></a>التحقق من صحة معرف الرحلة

لا يتم التحكم في معرف حاوية الشحن من خلال تسلسل رقمي. إنها فريدة فقط في سياق الرحلة التي يتم استخدامها فيها.

إذا تم استخدام كيان حاوية الشحن (`ITMContainersEntity`) بشكل مستقل عن كيان الرحلة (`ITMTableEntity`)، فإن قيمة **معرف الرحلة** (`ShipId`) يجب أن تتطابق مع سجل موجود في جدول الرحلة. بخلاف ذلك، فسيفشل الاستيراد.

إذا تم استخدام كيان حاوية الشحن (`ITMContainersEntity`) وكيان الرحلة (`ITMTableEntity`) كجزء من جلسة الاستيراد نفسها، يجب أن يسبق كيان الرحلة إنشاء حاوية شحن. بخلاف ذلك، لا يمكن التحقق من صحة قيمة **معرف الرحلة** (`ShipId`) بنجاح. إذا تم استخدام قيمة عنصر نائب لقيمة **معرف الرحلة** (`ShipId`)، لا يمكن إنشاء الاقتران إلا إذا تم استخدام نفس العنصر النائب باعتباره قيمة **معرف الرحلة** (`ShipId`) في كيان حاوية الشحن.

### <a name="other-field-validations"></a>عمليات التحقق من صحة الحقول الأخرى

يعرض الجدول التالي الحقول الموجودة في جدول حاوية الشحن (`ITMContainers`) التي تم التحقق من صحتها مقابل جداول إعداد التكلفة شاملة التفريغ. كما يُظهر كيانات بيانات تكلفة البضائع التي يمكن أن يستخدمها وكيل الشحن لقراءة القيم الحالية والتأكد من استلام القيم الصالحة في بيئتك.

| الحقل في جدول ITMContainers | كيان بيانات التكلفة شاملة التفريغ |
|---|---|
| نوع حاوية الشحن | ITMShippingContainerTypeEntity |
| وصف البضائع | ITMGoodsDescriptionEntity |
| نوع التبريد | ITMShippingContainerRefrigerationTypeEntity |

## <a name="folios-itmfolioentity"></a>حافظات الأوراق‬ (ITMFolioEntity)

تمثل حافظة الورق مجموعة من العناصر في حاوية شحن لأغراض البيانات الجمركية. تتضمن حاوية الورق معلومات على مستوى الرأس تتعلق بالمخلص الجمركي ووصفًا للبضائع. هذه الوظيفة مدعومة من قِبل كيان `ITMFolioEntity`. يسرد الجدول التالي الحقول والتعيينات التي تشكل هذا الكيان.

| Name | التعيين | نوع البيانات | مفتاح | إلزامي |
|---|---|---|---|---|
| موصى به من قِبل الوسيط | ITMFolioTable.ShipBrokerAdvised | التاريخ والوقت | لا | لا |
| رقم غرفة مراقبة الشحن | ITMFolioTable.ShipCargoControlNumber | Nvarchar(20) | لا | لا |
| موعد العميل | ITMFolioTable.ShipCustomerAppointment | التاريخ والوقت | لا | لا |
| الوسيط الجمركي | ITMFolioTable.ShipCustomsBroker | Nvarchar(20) | لا | لا |
| معرف الجمارك | ITMFolioTable.ShipCustomsId | Nvarchar(60) | لا | لا |
| الشركة | ITMFolioTable.ShipDataArea | Nvarchar(4) | لا | **نعم** |
| تم التسليم في المستودع | ITMFolioTable.ShipDelAtWarehouse | التاريخ والوقت | لا | لا |
| إرشادات التسليم | ITMFolioTable.ShipDeliveryInstructions | التاريخ والوقت | لا | لا |
| المستندات المستلمة | ITMFolioTable.ShipDocReceived | الفترة | لا | لا |
| تاريخ التسليم المقدّر | ITMFolioTable.ShipEstDlvDate | التاريخ والوقت | لا | لا |
| وقت الوصول المقدّر في مرفأ الشحن | ITMFolioTable.ShipEstPortDate | التاريخ والوقت | لا | لا |
| المصدّر‬ | ITMFolioTable.ShipExporterId | Nvarchar(20) | لا | لا |
| Name | ITMFolioTable.ShipExporterName | Nvarchar(60) | لا | لا |
| تاريخ حافظة الأوراق | ITMFolioTable.ShipFolioDate | التاريخ والوقت | لا | لا |
| حافظة الأوراق | ITMFolioTable.ShipFolioId | Nvarchar(20) | **نعم** | **نعم** |
| مرفأ المغادرة | ITMFolioTable.ShipFromPort | Nvarchar(20) | لا | لا |
| وصف البضائع | ITMFolioTable.ShipGoodsDesc | Nvarchar(60) | لا | لا |
| إصدار البضائع | ITMFolioTable.ShipGoodsReleased | التاريخ والوقت | لا | لا |
| بوليصة الشحن الجوي للمنزل/بوليصة الشحن | ITMFolioTable.ShipHAWB | Nvarchar(20) | لا | لا |
| الرحلة البحرية | ITMFolioTable.ShipId | Nvarchar(20) | لا | **نعم** |
| القياس | ITMFolioTable.ShipMeasurement | Numeric(32, 6) | لا | لا |
| وحدة القياس | ITMFolioTable.ShipMeasurementUnit | الفترة | لا | لا |
| عدد العبوات الكرتونية | ITMFolioTable.ShipNoOfCartons | Numeric(32, 6) | لا | لا |
| تم إرسال بوليصة الشحن الأصلية | ITMFolioTable.ShipOriginalBOLSebt | التاريخ والوقت | لا | لا |
| تم استلام المستندات الأصلية | ITMFolioTable.ShipOriginalDocsReceived | التاريخ والوقت | لا | لا |
| حالة أمر الشراء | ITMFolioTable.ShipPurchStatus | الفترة | لا | لا |
| ملاحظات | ITMFolioTable.ShipRemarks | Nvarchar(MAX) | لا | لا |
| حالة الرحلة البحرية | ITMFolioTable.ShipStatusId | Nvarchar(20) | لا | لا |
| كود التعريفة | ITMFolioTable.ShipTariffCode | Nvarchar(10) | لا | لا |
| إلى المرفأ | ITMFolioTable.ShipToPort | Nvarchar(20) | لا | لا |
| تاريخ التقييم | ITMFolioTable.ShipValuationDate | التاريخ والوقت | لا | لا |
| تاريخ التحقق | ITMFolioTable.ShipVerificationDate | التاريخ والوقت | لا | لا |
| حساب المورد | ITMFolioTable.VendAccount | Nvarchar(20) | لا | لا |

### <a name="number-sequences-for-folios"></a>التسلسلات الرقمية لحافظات الأوراق

التسلسل الرقمي لحافظات الأوراق يتحكم في تخصيص معرفات حافظات الأوراق.

تُستخدم القيمة التي تم تمريرها إلى كيان البيانات على أنها **معرف حافظة الأوراق** (`FolioId`) لتحديد سجل موجود للتحديث. في حالة عدم وجود هذا السجل، يعتمد السلوك على ما إذا كان التسلسل الرقمي المعين قد تم تكوينه للسماح بالإدخال اليدوي:

- إذا تم تمكين الإدخال اليدوي، يتم إنشاء سجل جديد يستخدم القيمة التي تم تمريرها.
- إذا لم يتم تمكين الإدخال اليدوي، فسيتم استخدام الرقم التالي في التسلسل الرقمي المخصص بدلاً من القيمة التي تم تمريرها.

أثناء جلسة الاستيراد، يتم الاحتفاظ بقيمة العنصر النائب التي تم استيرادها كمعرف حافظة الورق. يضمن هذا السلوك أن بنود الرحلة التي تشير إلى العنصر النائب مرتبطة بشكل صحيح، وأن يتم تحديثها لتعكس القيمة التي تم تعيينها من التسلسل الرقمي.

### <a name="field-validations"></a>عمليات التحقق من صحة الحقول

تم التحقق من صحة حقل **وصف البضائع** في جدول حافظات الأوراق (`ITMFolioTable`) في مقابل جدول إعداد التكلفة شاملة التفريغ بنفس الاسم. يمكن لوكيل الشحن استخدام كيان بيانات التكلفة شاملة التفريغ لـ `ITMGoodsDescriptionEntity` لقراءة القيم الحالية والتأكد من تلقي القيم الصالحة في بيئتك.

## <a name="voyage-lines-for-purchase-orders-itmpurchaselineentity"></a>بنود الرحلات لأوامر الشراء (ITMPurchaseLineEntity)

يمثل بند الرحلة بند أمر شراء واحدًا مضمنًا في الرحلة. يتم إنشاء هذه العلاقة من خلال حقلي **رقم أمر الشراء** و **رقم بند الشراء**. يشير بند الرحلة إلى كل سجل سابق تم إنشاؤه للرحلة وحاوية الشحن وحافظة الورق. هذه الوظيفة مدعومة من قِبل كيان `ITMPurchaseLineEntity`. يسرد الجدول التالي الحقول والتعيينات التي تشكل هذا الكيان.

| Name | التعيين | نوع البيانات | مفتاح | إلزامي |
|---|---|---|---|---|
| عملة | ITMLine.CurrencyCode | Nvarchar(3) | لا | لا |
| ‏‫المبلغ الصافي‬ | ITMLine.LineAmountMST | Numeric(32, 6) | لا | لا |
| رقم بند الشراء | ITMLine.RefRecId | Numeric(32, 6) | **نعم** | لا |
| حاوية الشحن | ITMLine.ShipContainerId | الفترة | لا | لا |
| الشركة | ITMLine.ShipDataArea | Nvarchar(20) | **نعم** | لا |
| الكمية المعلن عنها | ITMLine.ShipDeclaredQty | Nvarchar(4) | لا | لا |
| حافظة الأوراق | ITMLine.ShipFolioId | Numeric(32, 6) | لا | لا |
| الرحلة البحرية | ITMLine.ShipId | Nvarchar(20) | **نعم** | لا |
| رقم الصنف | ITMLine.ShipItemId | Nvarchar(20) | لا | لا |
| القياس | ITMLine.ShipMeasurement | Nvarchar(20) | لا | لا |
| وحدة القياس | ITMLine.ShipMeasurementUnit | Numeric(32, 6) | لا | لا |
| عدد العبوات الكرتونية | ITMLine.ShipNoOfCartons | الفترة | لا | لا |
| الموضع | ITMLine.ShipPosition | Numeric(32, 6) | لا | لا |
| Quantity | ITMLine.ShipQty | الفترة | لا | لا |
| رقم أمر الشراء | ITMLine.TransRefId | Numeric(32, 6) | **نعم** | لا |
| الوحدة | ITMLine.UnitId | الفترة | لا | لا |
| Volume | ITMLine.Volume | Nvarchar(10) | لا | لا |
| الوزن | ITMLine.Weight | Numeric(32, 6) | لا | لا |

## <a name="voyage-lines-for-transfer-orders-itmtransferlineentity"></a>بنود الرحلة لأوامر التحويل (ITMTransferLineEntity)

يمثل بند الرحلة بند أمر تحويل واحدًا مضمنًا في الرحلة. يتم إنشاء هذه العلاقة من خلال حقلي **رقم أمر التحويل** و **رقم بند التحويل**. يشير بند الرحلة إلى كل سجل سابق تم إنشاؤه للرحلة وحاوية الشحن وحافظة الورق. هذه الوظيفة مدعومة من قِبل كيان `ITMTransferLineEntity`. يسرد الجدول التالي الحقول والتعيينات التي تشكل هذا الكيان.

| Name | التعيين | نوع البيانات | مفتاح | إلزامي |
|---|---|---|---|---|
| عملة | ITMLine.CurrencyCode | Nvarchar(3) | لا | لا |
| ‏‫المبلغ الصافي‬ | ITMLine.LineAmountMST | Numeric(32, 6) | لا | لا |
| حاوية الشحن | ITMLine.ShipContainerId | الفترة | لا | لا |
| الشركة | ITMLine.ShipDataArea | Nvarchar(20) | **نعم** | لا |
| الكمية المعلن عنها | ITMLine.ShipDeclaredQty | Nvarchar(4) | لا | لا |
| حافظة الأوراق | ITMLine.ShipFolioId | Numeric(32, 6) | لا | لا |
| الرحلة البحرية | ITMLine.ShipId | Nvarchar(20) | **نعم** | لا |
| رقم الصنف | ITMLine.ShipItemId | Nvarchar(20) | لا | لا |
| القياس | ITMLine.ShipMeasurement | Nvarchar(20) | لا | لا |
| وحدة القياس | ITMLine.ShipMeasurementUnit | Numeric(32, 6) | لا | لا |
| عدد العبوات الكرتونية | ITMLine.ShipNoOfCartons | الفترة | لا | لا |
| الموضع | ITMLine.ShipPosition | Numeric(32, 6) | لا | لا |
| Quantity | ITMLine.ShipQty | الفترة | لا | لا |
| رقم بند التحويل | ITMLine.TransferLineNumber | Numeric(32, 6) | **نعم** | لا |
| رقم أمر التحويل | ITMLine.TransRefId | Numeric(32, 6) | **نعم** | لا |
| الوحدة | ITMLine.UnitId | الفترة | لا | لا |
| Volume | ITMLine.Volume | Nvarchar(10) | لا | لا |
| الوزن | ITMLine.Weight | Numeric(32, 6) | لا | لا |

### <a name="reference-table"></a>جدول المراجع

يتم إنشاء بنود الرحلات من خلال اقتران ببند أمر وارد مفتوح. يمكن أن يكون هذا البند في أمر شراء، أو يمكن أن يكون حركة الاستلام في أمر التحويل. يحدد الحقل `RefTableId` في جدول بند الرحلة (`ITMLine`) نوع الأمر المرتبط به البند من خلال الرجوع إلى رقم الجدول. إذا تمت الإشارة إلى أرقام جدول محددة في الجدول حيث يتم إنشاء البيانات، فسيتم تقسيم الكيانات بناءً على هذه القيم.

قيم الجدول المرجعي (`RefTableId`) ونوع الحركة (`TransType`) ضمنية في اختيار إما كيان بند شراء تكلفة الأرض أو كيان بند تحويل التكلفة شاملة التفريغ.

### <a name="validation"></a>التحقق من الصحة

يشير بند الرحلة مباشرةً إلى سجل رحلة، وسجل حاوية شحن، وسجل حافظة ورق. إذا تم استخدام كيان بند الشراء (`ITMPurchaseLinesEntity`) أو كيان بند التحويل (`ITMPurchaseLinesEntity`) بصرف النظر عن الكيانات المستخدمة لإنشاء هذه السجلات المرجعية، فيجب أن تتطابق قيم **معرف الرحلة** (`ShipId`)، و **حاوية الشحن** (`ShipContainerId`)، و **حافظة الورق** (`ShipFolioId`) مع سجل موجود في الجداول المقابلة. بخلاف ذلك، فسيفشل الاستيراد.

إذا تم استخدام أي من الكيانين كجزء من جلسة الاستيراد نفسها، فيجب أن تسبق تلك الكيانات الأخرى إنشاء بند رحلة. بخلاف ذلك، لا يمكن التحقق من صحة القيم بنجاح. إذا تم استخدام قيمة عنصر نائب لرقم حافظة الورق أو السجل، فلا يمكن إنشاء الاقتران إلا إذا تم استخدام نفس العنصر النائب لرقم حافظة الورق أو الرحلة في كيان بند الرحلة.

إذا تم تعيين أمر الشراء أو بند أمر التحويل بالفعل لبند رحلة موجود، فلن يتم إنشاء بند الرحلة الجديد. قبل التمكن من تخصيص بند الأمر لرحلة جديدة، يجب إزالته من رحلته الحالية.

### <a name="order-line-identification"></a>تحديد بند الأمر

تشير بنود الرحلات مباشرةً إلى القيم المرجعية **معرف السجل** (`RefRecId`)، **معرف بُعد المخزون** (`InventDimId`)، و **معرف حركة المخزون** (`InventTransId`). لم يعد من الضروري تضمين هذه القيم عند استخدام كيان البيانات. بدلاً من ذلك، يجب الآن تضمين رقم بند الأمر. يعمل رقم بند الأمر ورقم الأمر معًا على تمكين تحديد كل من هذه القيم المرجعية.

### <a name="voyage-line-quantity"></a>كمية بند الرحلة

نظرًا لأن بند الرحلة مرتبط بشكل مباشر ببند أمر، فإن قيمة **الكمية** (`ShipQty`) التي يتم إدخالها باستخدام الكيان تتطلب تطابق القيم. يتم تشغيل التحقق من الصحة مقابل الكمية في بند أمر الشراء أو بند التحويل. إذا فشل التحقق من الصحة، فلن تتم معالجة السجل.

### <a name="calculated-fields"></a>الحقول المحسوبة

تقبل الحقول المحسوبة **الوزن** و **الحجم** القيم التي يتم تلقيها من خلال كيان البيانات. إذا لم يتم توفير أي قيم، فسيتم استخدام قيم النظام لتحديث هذه الحقول، إذا كانت قيم النظام متاحة. بالنسبة للتكلفة شاملة التفريغ، يتم حساب القيم بالطريقة التالية:

- *الوزن* = *الكمية* × *الوزن الإجمالي للصنف*
- *الحجم* = *الكمية* × (*العمق الإجمالي للصنف* × *الارتفاع الإجمالي للصنف* × *العرض الإجمالي للصنف*)

## <a name="sequencing"></a>التسلسل

بسبب التبعيات بين الجداول، يجب إنشاء سجل الرحلة أولاً. لا يمكن إنشاء بند الرحلة إلا بعد إنشاء الرحلة وحاوية الشحن وحاويات الأوراق.

لإنشاء رحلة بدون تحذيرات التحقق من الصحة، يجب على النظام معالجة الكيانات بالترتيب التالي:

1. الرحلات (`ITMTableEntity`)
1. حاويات الشحن (`ITMContainersEntity`)
1. حافظات الأوراق (`ITMFolioTableEntity`)
1. بنود الرحلات (`ITMPurchaseLinesEntity` أو `ITMTransferLinesEntity`)
