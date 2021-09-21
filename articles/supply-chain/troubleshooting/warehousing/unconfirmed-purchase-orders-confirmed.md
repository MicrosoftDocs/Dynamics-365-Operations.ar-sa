---
title: تحديث مهمة إيصالات استلام المنتجات تؤكد الأوامر غير المؤكدة
description: بعد القيام بتشغيل تحديث إيصالات استلام المنتجات، يقوم النظام بتأكيد الأوامر غير المؤكدة التي تكون حالتها مسجلة. تعرف على الميزة التي تعمل على إصلاح هذه المشكلة.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 171a978efc6b55b92f429381e72036cb1b3296c6
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475437"
---
# <a name="unconfirmed-purchase-orders-are-confirmed-after-running-update-product-receipts"></a>يتم تأكيد أوامر الشراء غير المؤكدة بعد تشغيل تحديث إيصالات استلام المنتجات

## <a name="symptoms"></a>العلامات

بعد تشغيل المهمة الدورية *تحديث إيصالات استلام المنتجات*، يقوم النظام تلقائيا بتاكيد أوامر الشراء غير المؤكدة التي لها حاله حركه المخزون *المسجلة*.

## <a name="resolution"></a>الحل

تعمل ميزه معالجه التحميل الواردة الجديدة، *عبر استلام كميات التحميل*، علي إصلاح هذه المشكلة. لتشغيل هذه الميزة، انتقل إلى مساحة عمل [إدارة الميزات](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) وقم بتشغيل الميزات التالية بالترتيب المسرد:

1. إقران حركات مخزون أمر الشراء بحمل العمل
2. استلام زائد لكميات حمل العمل

لمزيد من المعلومات ، راجع [ترحيل كميات المنتج المسجلة مقابل أوامر الشراء](/dynamics365/supply-chain/warehousing/inbound-load-handling).
