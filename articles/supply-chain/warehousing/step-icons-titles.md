---
title: تعيين رموز وعناوين الخطوة لتطبيق الأجهزة المحمولة لـ Warehouse Management
description: يصف هذا المقال كيفية تعيين رموز وعناوين الخطوات لتدفقات المهام الجديدة أو المخصصة لتطبيق الأجهزة المحمولة لـ Warehouse Management.
author: Mirzaab
ms.date: 05/17/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 2ed2baff1851eba488233c050cef1f8f73b6bcee
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067291"
---
# <a name="assign-step-icons-and-titles-for-the-warehouse-management-mobile-app"></a>تعيين رموز وعناوين الخطوة لتطبيق الأجهزة المحمولة لـ Warehouse Management

[!include [banner](../includes/banner.md)]

يصف هذا المقال كيفية تعيين رموز وعناوين الخطوات لتدفقات المهام الجديدة أو المخصصة لتطبيق الأجهزة المحمولة لـ Warehouse Management.

توضح التوضيحات التالية كيفية ظهور رموز وعناوين الخطوات في تطبيق الأجهزة المحمولة لـ Warehouse Management.

![مثال على رمز خطوة وعنوان خطوة في تطبيق الأجهزة المحمولة لـ Warehouse Management.](media/step-icon-example.png "مثال على رمز خطوة وعنوان خطوة في تطبيق الأجهزة المحمولة لـ Warehouse Management")

## <a name="turn-this-feature-on-or-off"></a>تشغيل هذه الميزة أو إيقاف تشغيلها

لاستخدام الوظيفة التي ورد وصفها في هذا المقال، يجب أن تكون الميزة *إعدادات المستخدم والأيقونات وعناوين الخطوات لتطبيق المستودع الجديد‬* قيد التشغيل في النظام. هذه الميزة إلزامية ولا يمكن إيقاف تشغيلها، اعتبارًا من Supply Chain Management 10.0.25. إذا كنت تقوم بتشغيل إصدار أقدم من 10.0.25، فبإمكان المسؤولين تشغيل هذه الوظيفة أو إيقاف تشغيلها عن طريق البحث عن ميزة *إعدادات المستخدم والأيقونات وعناوين الخطوات لتطبيق المستودع الجديد‬* في مساحة عمل [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="standard-step-ids-classes-and-icons"></a>معرفات الخطوات القياسية والفئات والرموز

يتم تعريف كل خطوة في تدفق المهام بمعرف خطوة، ويحتوي كل معرف خطوة على فئة خطوة مقابلة. يتم تحديد رمز الخطوة وعنوانها في كل فئة خطوة.

### <a name="step-ids-and-step-classes"></a><a name="step-ids-classes"></a>معرفات الخطوات و فئات الخطوات

يسرد الجدول التالي كل معرف خطوة متوفر حاليًا، وفئة الخطوة المقابلة له. يتم استخدام اسم عنصر التحكم الخاص بحقل الإدخال الأساسي كمعرف للخطوة.

للحصول على مثال يوضح كيفية استخدام معرفات الخطوات هذه وفئاتها، راجع تطبيق الأسلوب `WHSMobileAppStepInfoBuilder.stepId()` في [المثال: تعيين رموز وعناوين الخطوات للقسم تدفق مخصص](#example) لاحقًا في هذا المقال.

| معرف الخطوة | فئة الخطوة |
|-|-|
| BatchDisposition | WHSMobileAppStepBatchDisposition |
| الناقل | WHSMobileAppStepCarrier |
| CatchWeight | WHSMobileAppStepCatchWeight |
| CatchWeightQtyOutboundWeight | WHSMobileAppStepCatchWeight |
| CatchWeightTag | WHSMobileAppStepCatchWeightTag |
| CatchWeightTagWeight | WHSMobileAppStepCatchWeightTagWeight |
| ChangeWarehouseSuccess | WHSMobileAppStepChangeWarehouseSuccess |
| CheckDigit | WHSMobileAppStepCheckDigit |
| ClusterId | WHSMobileAppStepClusterId |
| ClusterPickQtyVerification | WHSMobileAppStepQtyVerification |
| ClusterPosition | WHSMobileAppStepClusterPosition |
| ConfigId | WHSMobileAppStepConfigId |
| التأكيد | WHSMobileAppStepConfirmation |
| ConsolidateFromLicensePlateId | WHSMobileAppStepConsolidateFromLicensePlateId |
| ConsolidateLPConfirmation | WHSMobileAppStepConsolidateLPConfirmation |
| ConsolidateToLicensePlateId | WHSMobileAppStepConsolidateToLicensePlateId |
| ContainerType | WHSMobileAppStepContainerType |
| CountingReasonCode | WHSMobileAppStepCountingReasonCode |
| CycleCountingAddLPOrFinish | WHSMobileAppStepCycleCountingAddLPOrFinish |
| CycleCountQty1 | WHSMobileAppStepCycleCountQty |
| CycleCountQty2 | WHSMobileAppStepCycleCountQty |
| CycleCountQty3 | WHSMobileAppStepCycleCountQty |
| CycleCountQty4 | WHSMobileAppStepCycleCountQty |
| الترتيب | WHSMobileAppStepDisposition |
| DriverCheckInConfirmation | WHSMobileAppStepDriverCheckInConfirmation |
| DriverCheckInId | WHSMobileAppStepDriverCheckInId |
| DriverCheckOutConfirmation | WHSMobileAppStepDriverCheckOutConfirmation |
| DriverCheckOutId | WHSMobileAppStepDriverCheckOutId |
| ExpDate | WHSMobileAppStepExpDate |
| FromBatchDisposition | WHSMobileAppStepFromBatchDisposition |
| FromInventoryStatus | WHSMobileAppStepInventoryStatusFrom |
| FullQty | WHSMobileAppStepFullQty |
| InboundPut | WHSMobileAppStepInboundPut |
| InventBatchId | WHSMobileAppStepBatch |
| InventColorId | WHSMobileAppStepInventColorId |
| InventLocation | WHSMobileAppStepInventLocation |
| InventLocationId | WHSMobileAppStepWarehouse |
| InventSerialId | WHSMobileAppStepInventSerialId |
| InventSizeId | WHSMobileAppStepInventSizeId |
| InventStatusId | WHSMobileAppStepInventStatus |
| InventStyleId | WHSMobileAppStepInventStyleId |
| InventVersionId | WHSMobileAppStepInventVersionId |
| ItemId | WHSMobileAppStepItem |
| ITMContainerID | ITMMobileAppStepContainerId |
| ITMShipmentID | ITMMobileAppStepShipmentId |
| KanbanCardId | WHSMobileAppStepKanbanCard |
| KanbanCardToEmpty | WHSMobileAppStepKanbanCardToEmpty |
| KanbanOrCardId | WHSMobileAppStepKanbanCard |
| LicensePlateId | WHSMobileAppStepLicensePlate |
| LoadId | WHSMobileAppStepLoadId |
| LocationLicensePlatePosition | WHSMobileAppStepLocationLicensePlatePosition |
| LocOrLP | WHSMobileAppStepLocOrLP |
| LocOrLP_From | WHSMobileAppStepLocOrLPFrom |
| LocOrLP_To | WHSMobileAppStepLocOrLPTo |
| LocOrLPCheck | WHSMobileAppStepLocOrLPCheck |
| LocVerification | WHSMobileAppStepLocVerification |
| LPAdjustIn | WHSMobileAppStepLPAdjustIn |
| LPBreakChildLP | WHSMobileAppStepLPBreakChildLP |
| LPBreakParentLP | WHSMobileAppStepLPBreakParentLP |
| LPBuildChildLP | WHSMobileAppStepLPBuildChildLP |
| LPBuildParentLP | WHSMobileAppStepLPBuildParentLP |
| LPVerification | WHSMobileAppStepLPVerification |
| MergeContainerId | WHSMobileAppStepMergeContainerId |
| MixedLPLineNum | WHSMobileAppStepMixedLPLineNum |
| MobileDeviceQueueMessageCollectionIdentifierId | WHSMobileAppStepSelectOrder |
| MovementConfirmCancel | WHSMobileAppStepMovementConfirmCancel |
| NewCaptureWeight | WHSMobileAppStepCatchWeight |
| NewQty | WHSMobileAppStepNewQty |
| OutboundCatchWeightTag | WHSMobileAppStepCatchWeightTag |
| OutboundPut | WHSMobileAppStepOutboundPut |
| OutboundWeight | WHSMobileAppStepCatchWeight |
| OverridePutNewLocation | WHSMobileAppStepOverridePutNewLocation |
| PieceByPieceConfirmation | WHSMobileAppStepQtyVerification |
| POLineNum | WHSMobileAppStepPOLineNum |
| ‏‫رقم أمر الشراء‬ | WHSMobileAppStepPONum |
| PositionFull | WHSMobileAppStepPositionFull |
| PositionFullQty | WHSMobileAppStepPositionFullQty |
| القوة | WHSMobileAppStepPotency |
| PrinterName | WHSMobileAppStepPrinterName |
| ProdId | WHSMobileAppStepProdId |
| ProdLastPalletConfirmation | WHSMobileAppStepProdLastPalletConfirmation |
| ProductConfirmation | WHSMobileAppStepProductConfirmation |
| ProductionScrapConfirmation | WHSMobileAppStepProductionScrapConfirmation |
| وضع | WHSMobileAppStepPut |
| PutawayClusterId | WHSMobileAppStepPutawayClusterId |
| الكمية | WHSMobileAppStepQty |
| QtyAdjust | WHSMobileAppStepQtyAdjust |
| QtyShort | WHSMobileAppStepQtyShort |
| QtyToConsume | WHSMobileAppStepQtyToConsume |
| QtyToPick | WHSMobileAppStepQtyToPick |
| QtyToPut | WHSMobileAppStepQtyToPut |
| QtyToScrap | WHSMobileAppStepQtyToScrap |
| QtyVerification | WHSMobileAppStepQtyVerification |
| QtyWithScanningLimit | WHSMobileAppStepQtyAdjust |
| ReasonString | WHSMobileAppStepReasonString |
| RecvLocationId | WHSMobileAppStepRecvLocationId |
| RemoveContainerId | WHSMobileAppStepRemoveContainerId |
| ReprintLabelConfirmation | WHSMobileAppStepReprintLabelConfirmation |
| RMANum | WHSMobileAppStepRMANum |
| ShortPickReason | WHSMobileAppStepShortPickReason |
| SortConOrLP | WHSMobileAppStepSortConOrLP |
| SortLicensePlateId | WHSMobileAppStepSortLicensePlateId |
| SortPositionId | WHSMobileAppStepSortPositionId |
| SortVerification | WHSMobileAppStepSortVerification |
| StartLocationId | WHSMobileAppStepStartLocationId |
| StartProdOrderConfirmation | WHSMobileAppStepStartProdOrderConfirmation |
| TargetLicensePlateId | WHSMobileAppStepTargetLicensePlateId |
| TOLineNum | WHSMobileAppStepTOLineNum |
| ToLocation | WHSMobileAppStepToLocation |
| TONum | WHSMobileAppStepTONum |
| ToWarehouse | WHSMobileAppStepWarehouseTo |
| TransportLoadId | WHSMobileAppStepTransportLoadId |
| WaveLabelId | WHSMobileAppStepWaveLabelId |
| WaveLblQty | WHSMobileAppStepWaveLblQty |
| الوزن | WHSMobileAppStepWeight |
| WeightToConsume | WHSMobileAppStepWeightToConsume |
| WHSAdjustmentType | WHSMobileAppStepWHSAdjustmentType |
| WHSReceivingException | WHSMobileAppStepWHSReceivingException |
| WHSWorkException | WHSMobileAppStepWHSWorkException |
| WHSWorkLicensePlateId | WHSMobileAppStepWorkLicensePlateId |
| WMSLocationId | WHSMobileAppStepLocation |
| WorkId | WHSMobileAppStepWorkId |
| WorkIdToCancel | WHSMobileAppStepWorkIdToCancel |
| WorkLPIdPutawayCluster | WHSMobileAppStepWorkLPIdPutawayCluster |
| WorkPoolId | WHSMobileAppStepWorkPoolId |
| ZoneId | WHSMobileAppStepZoneId |

### <a name="available-step-icons"></a><a name="step-icons"></a>رموز الخطوة المتوفرة

يتضمن النظام مجموعة من رموز الخطوة القياسية التي يمكنك استخدامها أيضًا للخطوات المخصصة الخاصة بك. لا يمكنك تحميل رموز الخطوات المخصصة حاليًا. وبالتالي، يجب عليك دائمًا تحديد أحد رموز الخطوة القياسية.

يعرض الجدول التالي كل رمز خطوة قياسية متوفر حاليًا، واسمه.

<table>
<tbody>
<tr>
<td><img src="media/step-icons-about.png" alt="About step icon" title="حول رمز الخطوة"><br>حول</td>
<td><img src="media/step-icons-add-lp.png" alt="Add license plate or item step icon" title="إضافة لوحة ترخيص أو رمز خطوة صنف"><br>AddLpOrItem</td>
<td><img src="media/step-icons-batch-disposition.png" alt="Batch disposition step icon" title="رمز خطوة إرجاع الدفعة"><br>BatchDisposition</td>
<td><img src="media/step-icons-carrier.png" alt="Carrier step icon" title="رمز خطوة الكاريرية"><br>الناقل</td>
</tr>
<tr>
<td><img src="media/step-icons-cw-tag.png" alt="Catch weight tag step icon" title="رمز خطوة العلامة الخاصة بوزن التعبئة"><br>CatchWeightTag</td>
<td><img src="media/step-icons-cw-tag-weight.png" alt="Catch weight tag weight step icon" title="رمز خطوة وزن علامة وزن التعبئة"><br>CatchWeightTagWeight</td>
<td><img src="media/step-icons-check-digit.png" alt="Check digit step icon" title="رمز خطوة رقم الفحص"><br>CheckDigit</td>
<td><img src="media/step-icons-check-in-out.png" alt="Check in or out ID step icon" title="رمز خطوة معرف الإيداع والسحب"><br>CheckInOutId</td>
</tr>
<tr>
<td><img src="media/step-icons-child-lp.png" alt="Child license plate step icon" title="رمز خطوة لوحة الترخيص التابعة"><br>ChildLP</td>
<td><img src="media/step-icons-cluster-id.png" alt="Cluster ID step icon" title="رمز خطوة معرف نظام المجموعة"><br>ClusterId</td>
<td><img src="media/step-icons-cluster-position.png" alt="Cluster position step icon" title="رمز خطوة موضع نظام المجموعة"><br>ClusterPosition</td>
<td><img src="media/step-icons-config-id.png" alt="Config ID step icon" title="رمز تكوين خطوة المعرف"><br>ConfigId</td>
</tr>
<tr>
<td><img src="media/step-icons-configured-field.png" alt="Configured field step icon" title="رمز خطوة الحقل المكون"><br>ConfiguredField</td>
<td><img src="media/step-icons-con-lp.png" alt="Con or LP step icon" title="رمز خطوة التجميع أو لوحة الترخيص"><br>ConOrLP</td>
<td><img src="media/step-icons-consolidate-from-LP.png" alt="Consolidate from license plate ID step icon" title="تجميع من رمز خطوة معرف لوح الترخيص"><br>ConsolidateFromLicensePlateID</td>
<td><img src="media/step-icons-consolidate-to-LP.png" alt="Consolidate to license plate ID step icon" title="تجميع لرمز خطوة معرف لوح الترخيص"><br>ConsolidateToLicensePlateID</td>
</tr>
<tr>
<td><img src="media/step-icons-container-type.png" alt="Container type step icon" title="رمز خطوة نوع الحاوية"><br>ContainerType</td>
<td><img src="media/step-icons-counting.png" alt="Counting step icon" title="رمز خطوة الجرد"><br>الجرد</td>
<td><img src="media/step-icons-counting-reason.png" alt="Counting reason code step icon" title="رمز خطوة كود سبب الجرد"><br>CountingReasonCode</td>
<td><img src="media/step-icons-country-origin.png" alt="Country of origin code step icon" title="رمز خطوة كود بلد المنشأ"><br>CountryOfOrigin</td>
</tr>
<tr>
<td><img src="media/step-icons-disposition.png" alt="Disposition step icon" title="رمز خطوة الإرجاع"><br>الترتيب</td>
<td><img src="media/step-icons-done.png" alt="Done step icon" title="رمز خطوة الإكمال"><br>تم</td>
<td><img src="media/step-icons-driver-check-in-confirmation.png" alt="Driver check in confirmation step icon" title="رمز خطوة تأكيد ‏‫تسجيل دخول السائق‬"><br>DriverCheckInConfirmation</td>
<td><img src="media/step-icons-driver-check-in-id.png" alt="Driver check in ID step icon" title="رمز خطوة معرف ‏‫تسجيل دخول السائق‬"><br>DriverCheckInId</td>
</tr>
<tr>
<td><img src="media/step-icons-driver-check-out-id.png" alt="Driver check out ID step icon" title="رمز خطوة معرف ‏‫تسجيل خروج السائق‬"><br>DriverCheckOutId</td>
<td><img src="media/step-icons-exp-date.png" alt="Expiration date step icon" title="رمز خطوة تاريخ انتهاء الصلاحية"><br>ExpDate</td>
<td><img src="media/step-icons-field.png" alt="Field step icon" title="رمز خطوة الحقل"><br>الحقل</td>
<td><img src="media/step-icons-from-batch.png" alt="From batch disposition step icon" title="رمز خطوة إرجاع من الدفعة"><br>FromBatchDisposition</td>
</tr>
<tr>
<td><img src="media/step-icons-from-inventory-status.png" alt="From inventory status step icon" title="رمز خطوة حالة من المخزون"><br>FromInventoryStatus</td>
<td><img src="media/step-icons-id-attribute.png" alt="ID attribute step icon" title="رمز خطوة سمة المعرف"><br>IdAttribute</td>
<td><img src="media/step-icons-invent-batch-id.png" alt="Inventory batch ID step icon" title="رمز خطوة معرف دفعة المخزون"><br>InventBatchID</td>
<td><img src="media/step-icons-invent-color-id.png" alt="Inventory color ID step icon" title="رمز خطوة معرف لون المخزون"><br>InventColorID</td>
</tr>
<tr>
<td><img src="media/step-icons-invent-location.png" alt="Inventory location step icon" title="رمز خطوة موقع المخزون"><br>InventLocation</td>
<td><img src="media/step-icons-invent-serial-id.png" alt="Inventory serial ID step icon" title="رمز خطوة المعرف التسلسلي للمخزون"><br>InventSerialID</td>
<td><img src="media/step-icons-invent-size-id.png" alt="Inventory size ID step icon" title="رمز خطوة معرف حجم المخزون"><br>InventSizeID</td>
<td><img src="media/step-icons-invent-status-id.png" alt="Inventory status ID step icon" title="رمز خطوة معرف حالة المخزون"><br>InventStatusID</td>
</tr>
<tr>
<td><img src="media/step-icons-invent-style-id.png" alt="Inventory style ID step icon" title="رمز خطوة معرف نمط المخزون"><br>InventStyleID</td>
<td><img src="media/step-icons-invent-version-id.png" alt="Inventory version ID step icon" title="رمز خطوة معرفإصدار المخزون"><br>InventVersionID</td>
<td><img src="media/step-icons-item-id.png" alt="Item ID step icon" title="رمز خطوة معرف الصنف"><br>ItemID</td>
<td><img src="media/step-icons-itm-contianer-id.png" alt="ITM container ID step icon" title="رمز خطوة معرف حاوية ITM"><br>ITMContainerID</td>
</tr>
<tr>
<td><img src="media/step-icons-itm-shipment-id.png" alt="ITM shipment ID step icon" title="رمز خطوة معرف شحن ITM"><br>ITMShipmentID</td>
<td><img src="media/step-icons-kanban-card-id.png" alt="Kanban card ID step icon" title="رمز خطوة معرف بطاقة كانبان"><br>KanbanCardID</td>
<td><img src="media/step-icons-kanban-or-card-id.png" alt="Kanban or card ID step icon" title="رمز خطوة معرف بطاقة أو كانبان"><br>KanbanOrCardID</td>
<td><img src="media/step-icons-license-plate-id.png" alt="License plate ID step icon" title="رمز خطوة معرف لوحة الترخيص"><br>LicensePlateID</td>
</tr>
<tr>
<td><img src="media/step-icons-load-id.png" alt="Load ID step icon" title="رمز خطوة معرف الحمل"><br>LoadId</td>
<td><img src="media/step-icons-location-lp-pos.png" alt="Location license plate position step icon" title="رمز ‏‫خطوة موضع لوحة ترخيص الموقع"><br>LocationLicensePlatePosition</td>
<td><img src="media/step-icons-location-or-lp.png" alt="Location or license plate step icon" title="رمز خطوة لوحة الترخيص أو موقع"><br>LocOrLP</td>
<td><img src="media/step-icons-location-or-lp-check.png" alt="Location or license plate check step icon" title="رمز خطوة فحص لوحة الترخيص أو موقع"><br>LocOrLPCheck</td>
</tr>
<tr>
<td><img src="media/step-icons-location-or-lp-from.png" alt="Location or license plate from step icon" title="رمز فحص لوحة الترخيص أو موقع من خطوة"><br>LocOrLPFrom</td>
<td><img src="media/step-icons-location-or-lp-to.png" alt="Location or license plate to step icon" title="رمز لوحة الترخيص أو موقع لخطوة"><br>LocOrLPTo</td>
<td><img src="media/step-icons-long-process-complete.png" alt="Long process completed step icon" title="رمز خطوة عملية طويلة مكتملة"><br>LongProcessCompleted</td>
<td><img src="media/step-icons-lp-break-parent.png" alt="LP break parent LP step icon" title="رمز خطوة لوحة الترخيص الأصلية لفاصل لوحة الترخيص"><br>LPBreakParentLP</td>
</tr>
<tr>
<td><img src="media/step-icons-merge-container.png" alt="Merge container ID step icon" title="رمز خطوة دمج معرف حاوية"><br>MergeContainerId</td>
<td><img src="media/step-icons-mixed-lp-line.png" alt="Mixed license plate line number step icon" title="رمز خطوة لوحة ترخيص مستخدم مختلطة"><br>MixedLPLineNum</td>
<td><img src="media/step-icons-outbound-weight.png" alt="Outbound weight step icon" title="رمز خطوة الوزن الخارجي"><br>OutboundWeight</td>
<td><img src="media/step-icons-owner.png" alt="Owner step icon" title="رمز خطوة المالك"><br>المالك</td>
</tr>
<tr>
<td><img src="media/step-icons-parent-lp.png" alt="Parent license plate step icon" title="رمز خطوة لوحة الترخيص الأصلية"><br>ParentLP</td>
<td><img src="media/step-icons-please-confirm.png" alt="Please confirm step icon" title="الرجاء التأكيد على رمز الخطوة"><br>PleaseConfirm</td>
<td><img src="media/step-icons-po-line-num.png" alt="Purchase order line number step icon" title="رمز خطوة رقم بند أمر الشراء"><br>POLineNum</td>
<td><img src="media/step-icons-po-num.png" alt="Purchase order number step icon" title="رمز خطوة رقم أمر الشراء"><br>‏‫رقم أمر الشراء‬</td>
</tr>
<tr>
<td><img src="media/step-icons-position-full.png" alt="Position full step icon" title="رمز خطوة موضع كامل"><br>PositionFull</td>
<td><img src="media/step-icons-potency.png" alt="Potency step icon" title="رمز خطوة القوة"><br>القوة</td>
<td><img src="media/step-icons-printer-name.png" alt="Printer name step icon" title="رمز خطوة اسم الطابعة"><br>PrinterName</td>
<td><img src="media/step-icons-prod-id.png" alt="Prod ID step icon" title="رمز خطوة معرف المنتج"><br>ProdId</td>
</tr>
<tr>
<td><img src="media/step-icons-product-confirm.png" alt="Product confirmation step icon" title="رمز خطوة تأكيد المنتج"><br>ProductConfirmation</td>
<td><img src="media/step-icons-put.png" alt="Put step icon" title="وضع رمز الخطوة"><br>وضع</td>
<td><img src="media/step-icons-putaway-cluster-id.png" alt="Putaway cluster ID step icon" title="رمز خطوة معرف نظام مجموعة التخزين"><br>PutawayClusterId</td>
<td><img src="media/step-icons-qty.png" alt="Quantity step icon" title="رمز خطوة الكمية"><br>الكمية</td>
</tr>
<tr>
<td><img src="media/step-icons-qty-adjust-in.png" alt="Quantity adjust in step icon" title="تعديل الكمية في رمز الخطوة"><br>QtyAdjustIn</td>
<td><img src="media/step-icons-qty-short.png" alt="Quantity short step icon" title="رمز خطوة الكمية الصغيرة"><br>QtyShort</td>
<td><img src="media/step-icons-qty-to-consume.png" alt="Quantity to consume step icon" title="رمز خطوة الكمية المطلوب استهلاكها"><br>QtyToConsume</td>
<td><img src="media/step-icons-qty-to-put.png" alt="Quantity to put step icon" title="رمز خطوة الكمية المطلوب وضعها"><br>QtyToPut</td>
</tr>
<tr>
<td><img src="media/step-icons-qty-to-scrap.png" alt="Quantity to scrap step icon" title="رمز خطوة الكمية المطلوب تخريدها"><br>QtyToScrap</td>
<td><img src="media/step-icons-qty-confirmation.png" alt="Quantity confirmation step icon" title="رمز خطوة تأكيد الكمية"><br>QuantityConfirmation</td>
<td><img src="media/step-icons-raf-end-job.png" alt="Report as finished end job step icon" title="رمز خطوة الإبلاغ كوظيفة منتهية"><br>RAFEndJob</td>
<td><img src="media/step-icons-recv-loc-id.png" alt="Receive location ID step icon" title="رمز خطوة معرف موقع الاستلام"><br>RecvLocationID</td>
</tr>
<tr>
<td><img src="media/step-icons-remove-container-id.png" alt="Remove container ID step icon" title="رمز خطوة إزالة معرف حاوية"><br>RemoveContainerID</td>
<td><img src="media/step-icons-rma-no.png" alt="RMA number step icon" title="رمز خطوة رقم RMA"><br>RMANum</td>
<td><img src="media/step-icons-select-order.png" alt="Select order step icon" title="رمز خطوة تحديد الأمر"><br>SelectOrder</td>
<td><img src="media/step-icons-short-pick-reason.png" alt="Short pick reason step icon" title="رمز خطوة سبب انتقاء قصير"><br>ShortPickReason</td>
</tr>
<tr>
<td><img src="media/step-icons-sort-position-id.png" alt="Sort position ID step icon" title="رمز خطوة معرف موضع الفرز"><br>SortPositionId</td>
<td><img src="media/step-icons-target-lp-id.png" alt="Target license plate ID step icon" title="رمز خطوة معرف لوحة الترخيص الهدف"><br>TargetLicensePlateId</td>
<td><img src="media/step-icons-to-line-no.png" alt="To line number step icon" title="رمز خطوة لرقم السطر"><br>ToLineNum</td>
<td><img src="media/step-icons-to-location.png" alt="To location step icon" title="رمز خطوة لموقع"><br>ToLocation</td>
</tr>
<tr>
<td><img src="media/step-icons-to-number.png" alt="To number step icon" title="رمز خطوة لرقم"><br>ToNum</td>
<td><img src="media/step-icons-to-warehouse.png" alt="To warehouse step icon" title="رمز خطوة لمستودع"><br>ToWarehouse</td>
<td><img src="media/step-icons-tranport-load-id.png" alt="Transport load ID step icon" title="رمز خطوة معرف حمل النقل"><br>TransportLoadId</td>
<td><img src="media/step-icons-vendor-batch-id.png" alt="Vendor batch ID step icon" title="رمز خطوة معرف دفعة المورد"><br>VendBatchId</td>
</tr>
<tr>
<td><img src="media/step-icons-wave-label-id.png" alt="Wave label ID step icon" title="رمز خطوة معرف تسمية الموجة"><br>WaveLabelId</td>
<td><img src="media/step-icons-wave-label-qty.png" alt="Wave label quantity step icon" title="رمز خطوة كمية تسمية الموجة"><br>WaveLblQty</td>
<td><img src="media/step-icons-weight.png" alt="Weight step icon" title="رمز خطوة الوزن"><br>الوزن</td>
<td><img src="media/step-icons-weight-to-consume.png" alt="Weight to consume step icon" title="رمز خطوة الوزن المطلوب استهلاكه"><br>WeightToConsume</td>
</tr>
<tr>
<td><img src="media/step-icons-whs-adjustment-type.png" alt="WMS adjustment type step icon" title="رمز خطوة نوع تسوية WMS"><br>WHSAdjustmentType</td>
<td><img src="media/step-icons-whs-receiving-exception.png" alt="WMS receiving exception step icon" title="رمز خطوة استثناء استلام WMS"><br>WHSReceivingException</td>
<td><img src="media/step-icons-wms-location-id.png" alt="WMS location ID step icon" title="رمز خطوة معرف موقع WMS"><br>WMSLocationID</td>
<td><img src="media/step-icons-work-id.png" alt="Work ID step icon" title="رمز خطوة معرف العمل"><br>WorkId</td>
</tr>
<tr>
<td><img src="media/step-icons-work-id-to-cancel.png" alt="Work ID to cancel step icon" title="رمز خطوة إلغاء معرف العمل للإلغاء"><br>WorkIdToCancel</td>
<td><img src="media/step-icons-work-lp-id.png" alt="Work license plate ID step icon" title="رمز خطوة معرف لوحة ترخيص العمل"><br>WorkLicensePlateId</td>
<td><img src="media/step-icons-work-lp-putaway-cluster.png" alt="Work license plate ID putaway cluster step icon" title="رمز خطوة نظام مجموعة تخزين معرف لوحة ترخيص العمل"><br>WorkLPIDPutawayCluster</td>
<td><img src="media/step-icons-work-pool-id.png" alt="Work pool ID step icon" title="رمز خطوة معرف وعاء العمل"><br>WorkPoolID</td>
</tr>
<tr>
<td><img src="media/step-icons-zone-pool-id.png" alt="Zone ID step icon" title="رمز خطوة معرف المنطقة"><br>ZoneID</td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## <a name="example-assign-step-icons-and-titles-for-a-custom-flow"></a><a name="example"></a>مثال: تعيين رموز وعناوين الخطوات لتدفق مخصص

يوضح هذا المثال كيفية إعداد رموز وعناوين الخطوات لتدفق مهمة مخصصة. يتم إنشاء السيناريو على مثال لتدفق مهمة مخصصة يتم تقديمها واستكشافها بمزيد من التفصيل في نشر المدونة التالي: [تخصيص تطبيق المستودع للأجهزة](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app). يعمل تدفق المهام بالطريقة التالية:

1. ويقوم التطبيق بإظهار صفحة تطالب العامل بتقديم معرف حاوية (على سبيل المثال، عن طريق مسح كود شريطي).
1. إذا كان معرف الحاوية صالحًا، يقوم التطبيق بفتح صفحة جديدة تطالب العامل بالوزن. (إذا كان معرف الحاوية غير صالح، يتم إرجاع العامل إلى الصفحة الأولى.)
1. عندما يدخل العامل وزن صالح، يقوم النظام بتخزين الوزن وإرجاع العامل إلى الصفحة الأولى.

يبين الرسم التوضيحي التالي تدفق هذه المهمة.

![الرسم التخطيطي لسير المهمة.](media/step-icons-example-task-flow.png "الرسم التخطيطي لسير المهمة")

### <a name="create-a-step-class-for-the-container-input-page"></a>إنشاء فئة خطوة لصفحة إدخال الحاوية

تتيح صفحة إدخال الحاوية فحص العامل أو إدخال معرف الحاوية.

![صفحة إدخال الحاوية.](media/step-icons-example-container-input.png "صفحة إدخال الحاوية")

في الصفحة "إدخال الحاوية"، اسم عنصر التحكم الخاص بحقل الإدخال هو `ContainerId`. نظرًا لأن اسم عنصر التحكم هذا ليس في [قائمة معرفات الخطوات](#step-ids-classes)، فلن تجد خطوة موجودة تستند إليه. ولذلك، يجب عليك إنشاء فئة خطوة تمثل الخطوة. فيما يلي مثال على ذلك.

```xpp
[WHSMobileAppStepId('ContainerId')]
final internal class WHSMobileAppStepContainerId extends WHSMobileAppStep
{
    private const WHSMobileAppStepIcon PopulationIcon = 'InventBatchID';
    private const WHSMobileAppStepTitle InputNotFilledTitle = "@WAX:WHSMobileAppStepContainerID_InputNotFilled"; //Scan a container
    protected void initValues()
    {
        defaultStepIcon = PopulationIcon;
        defaultStepTitle = InputNotFilledTitle;
    }
}
```

يتم تخزين معرف رمز الخطوة في عضو الفئة `defaultStepIcon`، ويتم تخزين عنوان الخطوة في عضو الفئة `defaultStepTitle`.

لتعيين رمز خطوة، قم بتعيين `defaultStepIcon` لأحد معرفات الرموز التي يتم سردها في القسم [رموز الخطوات المتوفرة](#step-icons) سابقًا في هذا المقال.

### <a name="use-a-standard-or-custom-step-icon-and-title-for-the-weight-input"></a>استخدام رمز خطوة قياسية أو مخصصة وعنوان لإدخال الوزن

تتيح صفحة إدخال الوزن للعامل إدخال وزن.

![صفحة إدخال الوزن.](media/step-icons-example-weight-input.png "صفحة إدخال الوزن")

في الصفحة إدخال الوزن، اسم عنصر التحكم الخاص بحقل الإدخال هو `Weight`، والموجود في [قائمة معرفات الخطوات](#step-ids-classes). لذلك، إذا كان رمز وعنوان الخطوة اللذين يتم تعريفهما في الفئة `WHSMobileAppStepWeight` مقبولان بالنسبة إليك، فلن تحتاج إلى تغيير أي شيء لهذه الخطوة.

ومع ذلك، إذا كنت تفضل استخدام رمز أو عنوان مختلف لهذه الخطوة، فإنه يمكنك منع إما الأسلوب `stepId()` أو الأسلوب `stepInfo()` في فئة المنشئ. يحتوي كل تدفق مهام على منشئ معلومات الخطوة الخاص به.

#### <a name="override-the-stepid-method"></a>منع أسلوب stepId()

يظهر المثال التالي طريقة واحدة يمكنك من خلالها تعديل فئة منشئ بواسطة منع الأسلوب `stepId()`.

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepId stepId()
    {
        WHSMobileAppStepId stepIdLocal = super();
        if (stepIdLocal == 'Weight')
        {
            return 'NewWeight';
        }
        return stepIdLocal;
    }
}
```

ثم تقوم بعد ذلك بإنشاء فئة خطوة للخطوة `NewWeight`. يجب أن يتشابه الرمز مع الرمز الخاص بالمثال `ContainerId` الذي تم إظهاره سابقًا في هذا المقال.

#### <a name="override-the-stepinfo-method"></a>منع أسلوب stepInfo()

يظهر المثال التالي طريقة واحدة يمكنك من خلالها تعديل فئة منشئ بواسطة منع الأسلوب `stepInfo()`.

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepInfo stepInfo()
    {
        if (stepId != 'Weight')
        {
            return super();
        }
        WHSMobileAppStepInfo stepInfo = WHSMobileAppStepInfo::construct();
        stepInfo.parmStepIcon('NewIcon');
        stepInfo.parmStepTitle('NewTitle');
        return stepInfo;
    }
}
```

قم بعد ذلك بإنشاء كائن `WHSMobileAppStepInfo`، وقم بتعيين الرمز و/أو العنوان مباشرة.

## <a name="additional-resources"></a>الموارد الإضافية

- [تثبيت تطبيق إدارة المستودع للأجهزة المحمولة والاتصال به](install-configure-warehouse-management-app.md)
- [إعدادات مستخدم الجهاز المحمول](mobile-device-user-settings.md)
