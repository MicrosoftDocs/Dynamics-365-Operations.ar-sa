---
title: لا يمكنك تاكيد الشحنة بسبب العمل غير المكتمل أو المفقود
description: لا يمكنك تاكيد الشحنة بسبب العمل غير المكتمل أو المفقود
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm, WHSContainerCloseDiag_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: beef0909d41e69f3e7bcc1021527be35b7e6fd44
ms.sourcegitcommit: c2c6d687a89bc1534c029109315c23e92865b63b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/31/2021
ms.locfileid: "6123833"
---
# <a name="you-cant-confirm-a-shipment-because-of-incomplete-or-missing-work"></a>لا يمكنك تاكيد الشحنة بسبب العمل غير المكتمل أو المفقود

رمز الخطأ: WAX515

## <a name="symptoms"></a>العلامات

عند محاولة التاكيد علي أحدي الشحنات، يعرض النظام رسالة الخطا التالية:

> تعذر تأكيد شحن الحمولة %1 لأنه يجب إكمال جميع أعمال الحمولة.

وبالتالي، لا يمكنك تاكيد الشحن للتحميل.

## <a name="cause"></a>السبب

الحمولة أو الشحنة في حالة فشل فيها تأكيد الشحنة. قبل أن تتمكن من تأكيد الشحنة، يجب توفر بعض الأعمال على الأقل للحمل، ويجب أن يكون لكل هذا العمل حالة *مقفل* أو *ملغى*.

## <a name="resolution"></a>الدقة

تحقق من أوامر المبيعات أو أوامر التحويل ذات الصلة الخاصة بالحمل أو الشحن، وتاكد من اكتمال كافة الاعمال ذات الصلة أو إلغاؤها.

ويمكنك التعامل مع الشحنات والأحمال في العديد من الصفحات. توفر الأقسام الفرعية التالية أمثله قليله.

### <a name="all-loads-page"></a>صفحة كل الأحمال

1. انتقل إلى **إدارة المستودعات \> الأحمال‏‎ \> جميع الأحمال‏‎**.
1. حدد الحمل الذي لا يمكن تأكيد الشحنة له.
1. في جزء الإجراءات، في علامة التبويب **الأحمال**، في مجموعة **المعلومات ذات الصلة**، حدد **العمل**.
1. افحص حالة كل معرف عمل. تابع كل معرف عمل ليس له حالة *مقفل* أو *ملغي*.
1. عندما تكون حاله كل معرف عمل هي *مقفل* أو *ملغى*، حاول مرة أخرى لتاكيد الشحنة.

### <a name="all-shipments-page"></a>صفحة كل الشحنات

1. انتقل إلى **إدارة المستودعات \> الشحنات \> جميع الشحنات**.
1. حدد الشحنة التي لا يمكن تأكيدها.
1. في جزء الإجراءات، ضمن علامة التبويب **الشحنات**، في مجموعة **العمل**، حدد **تفاصيل العمل**.
1. افحص حالة كل معرف عمل. تابع كل معرف عمل ليس له حالة *مقفل* أو *ملغي*.
1. عندما تكون حاله كل معرف عمل هي *مقفل* أو *ملغى*، حاول مرة أخرى لتاكيد الشحنة.

### <a name="all-work-page"></a>صفحة كل العمل

1. انتقل إلى **إدارة المستودعات \> العمل\> كل العمل**.
1. حدد العمل لرقم الأمر الذي لا يمكن تأكيد الشحنة له.
1. في "جزء الإجراءات"، في علامة التبويب **الشحن**، في مجموعة **الشحن**، حدد **تأكيد الشحن**.
1. افحص حالة كل معرف عمل. تابع كل معرف عمل ليس له حالة *مقفل* أو *ملغي*.
1. عندما تكون حاله كل معرف عمل هي *مقفل* أو *ملغى*، حاول مرة أخرى لتاكيد الشحنة.
