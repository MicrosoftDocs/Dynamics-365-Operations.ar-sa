---
title: يجب تحديد لوحة الترخيص لهذا الموقع
description: إذا تلقيت هذا الخطأ بعد إنشاء أمر تحويل لمستودع تم تمكين WMS عليه، فسيكون موقع الاستلام الافتراضي فارغاً لمستودع البضائع قيد النقل‬.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2e562ad2b41dd149f215adc83bd2d54e55dccc05
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475439"
---
# <a name="license-plate-specification-error-when-confirming-shipment-for-a-transfer-order"></a>حدث خطأ في مواصفات لوحة الترخيص عند تأكيد الشحن لأمر التحويل

## <a name="symptoms"></a>العلامات

إذا قمت بإنشاء أمر تحويل باستخدام مستودع تمت تمكين إدارة المستودعات المتقدمة (WMS) له، ثم حاولت تأكيد الشحنة بعد اكتمال العمل، فقد تتلقى رسالة الخطأ التالية:

> يجب تحديد لوحة الترخيص لهذا الموقع.

## <a name="cause"></a>السبب

هذا يحدث لأن حقل **موقع الاستلام الافتراضي** فارغ لمستودع البضائع قيد النقل للمستودع "من".

## <a name="resolution"></a>الحل

لحل هذه المشكلة ، حدد موقع استلام افتراضي في مخزن البضاعة بالطريق. تأكد من أن هذا الموقع يتم التحكم فيه من لوحة ترخيص.
