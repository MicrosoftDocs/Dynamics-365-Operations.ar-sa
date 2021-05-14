---
title: لا يمكنك تأكيد شحنة بسبب مشكلة في التقويم
description: لا يمكنك تأكيد شحنة بسبب مشكلة في التقويم
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
ms.openlocfilehash: f1fccd10d8867252f32b37c77f9a3bad54157bdd
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938415"
---
# <a name="you-cant-confirm-a-shipment-because-of-an-issue-with-the-calendar"></a>لا يمكنك تأكيد شحنة بسبب مشكلة في التقويم

رمز الخطأ: TRX2716

## <a name="symptoms"></a>العلامات

عند محاولة التاكيد علي أحدي الشحنات، يعرض النظام رسالة الخطا التالية:

> يتطلب نوع التقويم %1 أن يتم تسجيل الدخول والخروج للموعد %2.

وبالتالي، لا يمكنك تاكيد الشحن للتحميل.

## <a name="cause"></a>السبب

المواعيد النشطة للتحميل موجودة. على سبيل المثال، هناك قاعدة تتطلب تسجيل وصول السائق. لذلك، يكون الحمل حاليًا في حالة فشل فيها تأكيد الشحن.

## <a name="resolution"></a>الدقة

يجب عليك التحقيق وإصلاح أية مشكلات تتعلق بالمواعيد النشطة المرتبطة بالحمل.

1. انتقل إلى **إدارة المستودعات \> الأحمال‏‎ \> جميع الأحمال‏‎**.
1. حدد الحمل الذي لا يمكن تأكيد الشحنة له.
1. في جزء الإجراء، في علامة تبويب **النقل**، في مجموعة **المواعيد**، حدد **جدولة المواعيد**.
1. اتبع إحدى الخطوات التالية:

    - تأكد من اكتمال تسجيل الوصول/المغادرة للسائق للموعد.
    - أكمل أو ألغِ الموعد.
    - قم بتعطيل خيار **مطلوب تسجيل وصول السائق** لقاعدة المواعيد ذات الصلة.
