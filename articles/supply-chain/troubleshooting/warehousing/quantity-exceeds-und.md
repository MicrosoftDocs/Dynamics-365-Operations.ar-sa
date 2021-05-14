---
title: لا يمكنك تاكيد الشحنة نظرا لان الكمية تتجاوز النسبة المئوية للتسليم بالنقص.
description: لا يمكنك تاكيد الشحنة نظرا لان الكمية تتجاوز النسبة المئوية للتسليم بالنقص.
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
ms.openlocfilehash: 5339b9d800f7454e2a00c230a8d5deca3979c074
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938411"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-underdelivery-percentage"></a>لا يمكنك تاكيد الشحنة نظرا لان الكمية تتجاوز النسبة المئوية للتسليم بالنقص.

رمز الخطأ: WAX1687

## <a name="symptoms"></a>العلامات

عند محاولة التاكيد علي أحدي الشحنات، يعرض النظام رسالة الخطا التالية:

> تعذر تأكيد الشحنة للحمل %1 لأن كميه الصنف %2 تتجاوز النسبة المئوية التي تم تحديدها للتسليم الناقص.

وبالتالي، لا يمكنك تاكيد الشحن للتحميل.

## <a name="cause"></a>السبب

تم انتقاء كميه التحميل أو الشحن جزئيا فقط. الكمية الحالية اقل من الكمية المنتقية بالنسبة المئوية التي تتجاوز النسبة المئوية للتسليم بالنقص.

## <a name="resolution"></a>الدقة

لإصلاح هذه المشكلة، أكمل إحدى المهام التالية:

- يستخدم في تعيين كميه بند التحميل.
- قم بتعيين النسبة المئوية للتسليم بالنقص.

### <a name="set-the-load-line-quantity"></a>يستخدم في تعيين كميه بند التحميل

لتعيين كمية بند الحمل، اتبع هذه الخطوات.

1. انتقل إلى **إدارة المستودعات \> الأحمال‏‎ \> جميع الأحمال‏‎**.
1. حدد الحمل الذي لا يمكن تأكيد الشحنة له.
1. في علامة التبويب السريعة، **بنود الحمل**، حدد بند الحمل للعنصر الذي يتجاوز النسبة المئوية للتسليم الناقص.
1. في علامة التبويب السريعة **تفاصيل البنود**، حدد **أمر**.
1. في حقل **الكمية**، عيّن القيمة إلى الكمية المنتقاة (أي إلى قيمة **كمية العمل الذي تم إنشاؤه**)، بحيث يمكن أن يحدث تأكيد الشحنة.

### <a name="set-the-underdelivery-percentage"></a>قم بتعيين النسبة المئوية للتسليم بالنقص

لتعيين النسبة المئوية للتسليم الناقص، اتبع هذه الخطوات.

1. انتقل إلى **إدارة المستودعات \> الأحمال‏‎ \> جميع الأحمال‏‎**.
1. حدد الحمل الذي لا يمكن تأكيد الشحنة له.
1. في علامة التبويب السريعة، **بنود الحمل**، حدد بند الحمل للعنصر الذي يتجاوز النسبة المئوية للتسليم الناقص.
1. في علامة التبويب السريعة **تفاصيل البنود**، حدد **عام**.
1. في حقل **التسليم الناقص**، عيّن القيمة إلى نسبة مئوية أكبر تستوعب الكمية التي تم انتقاؤها مقابل كمية التحميل، بحيث يمكن تأكيد الشحنة.
