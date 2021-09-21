---
title: الكمية غير صالحة للوحدة %1 عند إجراء انتقاء التقسيم
description: عند إجراء انتقاء تقسيم عبر دفعات متعددة، قد تتلقى خطأ يفيد بأن الكمية غير صالحة للوحدة %1. تساعد هذه الصفحة في حل المشكلة.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4627db7400d6ccd81f25f100de4696058ce35c42
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475429"
---
# <a name="quantity-is-not-valid-when-performing-a-split-pick-across-multiple-batches"></a>الكمية غير صالحة عند إجراء انتقاء التقسيم عبر دفعات متعددة

## <a name="symptoms"></a>العلامات

عند محاولة تنفيذ عملية *انتقاء التقسيم* عبر عدة دفعات، قد تستلم رسالة الخطأ التالية:

> الكمية غير صالحة للوحدة %1.

## <a name="resolution"></a>الحل

يجب أن يستخدم عامل المستودع عملية *الانتقاء القصير* في تطبيق Warehouse Management للأجهزة المحمولة. إذا كنت تحاول انتقاء مجموعات متعددة من نفس الموقع، يمكنك أيضا استخدام الخيار **كامل** في التطبيق.
