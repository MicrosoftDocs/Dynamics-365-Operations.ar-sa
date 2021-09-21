---
title: التسليم المباشر غير قادر على المعالجة لمستودع تم تمكين WMS عليه
description: إذا تم تمكين WMS للمستودع، فإنه لا يدعم التسليم المباشر. لاستخدام التسليم المباشر، يجب تحديد صنف ومستودع لم يتم تمكين WMS له.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 090e17091e9fb92c2065679bb9b04637214e2eea
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475524"
---
# <a name="direct-delivery-not-able-to-process-for-wms-enabled-warehouse"></a>التسليم المباشر غير قادر على معالجة لمستودع تم تمكين WMS عليه

## <a name="symptoms"></a>العلامات

في حالة إضافة صنف إلى بند مبيعات للتسليم المباشر من مستودع تم تمكينه لإدارة المستودعات (WMS)، تظهر رسالة الخطأ التالية عند تحديث بند المبيعات:

> التسليم المباشر غير قادر على معالجة المستودع 1% نظراً لأنه تم تمكين إدارة المستودعات له. الرجاء تحديد مستودع آخر لم يتم تمكين إدارة المستودعات له.

## <a name="resolution"></a>الحل

قامت Microsoft بتقييم هذه المشكلة وقامت بتحديد انها قيد ميزه. حاليا ، لا يدعم WMS التسليم المباشر. التالي ، لاستخدام التسليم المباشر ، يجب تحديد صنف ومستودع غير WMS.
