---
title: لا يمكنك تأكيد الشحنة لأن العميل معلق
description: لا يمكنك تأكيد الشحنة لأن العميل معلق.
author: GalynaFedorova
ms.date: 07/30/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 801778fc8f04b106bf168a3dcd5a89767a837740
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344254"
---
# <a name="you-cant-confirm-a-shipment-because-the-customer-is-on-hold"></a>لا يمكنك تأكيد الشحنة لأن العميل معلق

رمز الخطأ: WAX:CustomerOnHoldShipmentCannotBeConfirmed

## <a name="symptoms"></a>العلامات

عند محاولة التاكيد علي أحدي الشحنات، يعرض النظام رسالة الخطا التالية:

> الشحنة %1 لا يمكن تأكيدها نظراً لأن العميل في وضع الانتظار لـ %2.

وبالتالي، لا يمكنك تاكيد الشحن للتحميل.

## <a name="cause"></a>السبب

حساب العميل للحمولة أو الشحنة معلق. لذلك، تمنع حالة العميل تأكيد الشحن.

## <a name="resolution"></a>الحل

استخدم الإجراء التالي لإلغاء حظر حساب العميل.

1. انتقل إلى **الحسابات المدينة \> العملاء \> كافة العملاء**.
1. افتح حساب العميل الذي لا يمكن تأكيد الشحنة له.
1. في علامة التبويب السريعة **الائتمان والتحصيلات**، قم بتعيين حقل **الفواتير والتسليم قيد الانتظار** إلى *لا*.
1. كرر هذا الإجراء لجميع العملاء المحظورين للحمل.
