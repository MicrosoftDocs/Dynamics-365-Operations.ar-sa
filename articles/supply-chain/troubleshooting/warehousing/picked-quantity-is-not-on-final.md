---
title: لا يمكنك تاكيد شحنه نظرا لأنه لم يتم انتقاء الأصناف
description: لا يمكنك تاكيد شحنه نظرا لأنه لم يتم انتقاء الأصناف
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 23a517e7769dc86ebec30e4f17c62172a6ad8801
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938413"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a>لا يمكنك تاكيد شحنه نظرا لأنه لم يتم انتقاء الأصناف

رمز الخطأ: LoadNotPickedAndMovedToFinalShippingLocation

## <a name="symptoms"></a>العلامات

عند محاولة التاكيد علي أحدي الشحنات، يعرض النظام رسالة الخطا التالية:

> لم يتم انتقاء بعض الأصناف اللازمة لحمل العمل %1 ولا نقلها إلى موقع الشحن النهائي.

وبالتالي، لا يمكنك تاكيد الشحن للتحميل.

## <a name="cause"></a>السبب

لا يمكن تاكيد التحميل أو الشحن في حالته الحالية لان أحدي الحالات التالية قد تكون موجودة:

- لم يتم بعد انتقاء العمل ذي الصلة ونقله إلى موقع الشحن النهائي.
- لا تتطابق كميه العمل المنتقية مع كميه العمل التي تم إنشاؤها في بند التحميل.

## <a name="resolution"></a>الدقة

تحقق من أوامر التوريد أو أوامر التحويل ذات الصلة الخاصة بالحمل أو الشحن. تاكد من اكتمال كافة الاعمال ذات الصلة في موقع الشحن النهائي، وان الكميات متطابقة.

1. انتقل إلى **إدارة المستودعات \> الأحمال‏‎ \> جميع الأحمال‏‎**.
1. حدد الحمل الذي لا يمكن تأكيد الشحنة له.
1. في علامة التبويب السريعة **بنود الحمل**، حدد بند الحمل.
1. دون ملاحظه قيمة حقل **الكمية التي أنشاهأ العمل**.
1. في جزء الإجراءات، في علامة التبويب **الأحمال**، في مجموعة **المعلومات ذات الصلة**، حدد **العمل**.
1. تحقق من اكتمال العمل في موقع الشحن النهائي، وان كميه العمل المنتقية تطابق كميه العمل التي تم إنشاؤها في بند التحميل.
1. قم بتكرار هذا الاجراء لكافة بنود التحميل للتاكد من استيفاء كافة المعايير.
