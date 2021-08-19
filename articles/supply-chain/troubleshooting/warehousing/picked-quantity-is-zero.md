---
title: لا يمكنك التاكيد علي الشحنة بسبب وجود كميه تساوي صفرا
description: لا يمكنك التاكيد علي الشحنة بسبب وجود كميه تساوي صفرا
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
ms.openlocfilehash: b2f9f8deaca30e318d0393fb1d7911eebf63060ccca83dc6f1de9b04b9e30e11
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712876"
---
# <a name="you-cant-confirm-a-shipment-because-there-is-zero-quantity"></a>لا يمكنك التاكيد علي الشحنة بسبب وجود كميه تساوي صفرا

رمز الخطأ: LoadLineWarningUpdatedToZero

## <a name="symptoms"></a>العلامات

عند محاولة التاكيد علي أحدي الشحنات، يعرض النظام رسالة الخطا التالية:

> تم تحديث بند حمل العمل للعنصر %1 والشحنة %2 للحصول على كمية صفرية بسبب إعداد التسليم الناقص مما يسمح بعدم شحن أي كميات لهذا العنصر.

وبالتالي، لا يمكنك تاكيد الشحن للتحميل.

## <a name="cause"></a>السبب

ويقوم النظام بتقييم ما إذا كانت الكمية المنتقية تقع داخل الحدود المتوقعة، استنادا إلى الكمية المنتقية وكميه البند التي تم انتقاؤها ونسبه التسليم بالنقص. في حاله عثور النظام علي ان الكمية المنتقية في بند التحميل هي 0 (صفر)، لا يمكنك تاكيد الشحنة. علي سبيل المثال، قد تحدث هذه المشكلة في حاله إلغاء العمل، وكانت النسبة المئوية للتسليم بالنقص لبند التحميل هي 100 بالمائة.

## <a name="resolution"></a>الدقة

تحقق من بنود الحمل للتاكد من ان النسبة المئوية للتسليم بالنقص والكميات تتم محاذاتها بالعمل المنتقي.

1. انتقل إلى **إدارة المستودعات \> الأحمال‏‎ \> جميع الأحمال‏‎**.
1. حدد الحمل الذي لا يمكن تأكيد الشحنة له.
1. في علامة التبويب السريعة، **بنود الحمل**، حدد بند الحمل للعنصر الذي يتجاوز النسبة المئوية للتسليم الناقص.
1. قم بتعديل قيمة حقل **تسليم الناقص** أو حقل **الكمية** كما هو مطلوب.

> [!TIP]
> في حاله استمرار عدم إصلاح المشكلة، قد يلزم إكمال المزيد من اعمال الانتقاء لأوامر التوريد أو أوامر التحويل ذات الصلة حتى تتم محاذاة الكمية المتوفرة مع الحمل أو الحمل.
