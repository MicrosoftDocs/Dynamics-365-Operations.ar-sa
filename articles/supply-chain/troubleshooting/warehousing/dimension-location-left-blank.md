---
title: لا يمكن أن يكون موقع البعد فارغاً في حالة تعيين الرقم المسلسل
description: إذا تلقيت هذا الخطأ أثناء تأكيد الشحن بعد إنشاء أمر تحويل لصنف تسلسلي، فسيكون حقل موقع الاستلام الافتراضي فارغاً.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6f58c72438d5d1d93e59e46525debd65d44d9a76
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475508"
---
# <a name="error-when-confirming-shipment-after-creating-a-transfer-order-for-a-serial-item"></a>حدث خطأ عند تأكيد الشحنة بعد إنشاء أمر تحويل لصنف تسلسلي

## <a name="symptoms"></a>العلامات

إذا قمت بإنشاء أمر لصنف مسلسل باستخدام مستودع تم تمكين إدارة المستودعات المتقدمة (WMS) له، ثم بعد اكتمال العمل حاولت تأكيد الشحن، فإنك تتلقى رسالة الخطأ التالية:

> لا يمكن أن يكون موقع البعد فارغاً في حالة تعيين الرقم المسلسل للبعد.

## <a name="cause"></a>السبب

هذا يحدث لأن حقل **موقع الاستلام الافتراضي** فارغ لمستودع البضائع قيد النقل للمستودع "من".

## <a name="resolution"></a>الحل

لحل هذه المشكلة ، حدد موقع استلام افتراضي في مخزن البضاعة بالطريق. تأكد من أن هذا الموقع يتم التحكم فيه من لوحة ترخيص.
