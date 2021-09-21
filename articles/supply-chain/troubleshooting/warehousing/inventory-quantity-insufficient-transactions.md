---
title: يتعذر تحديث كمية المخزون نظرًا لعدم وجود حركات كافية
description: كمية المخزون -1% لا يمكن تحديثها نظراً لعدم وجود حركات مخزون كافية للصنف %2 الذي يتضمن الأبعاد المحددة.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 88130a969039dd741c8ea4fbaabe81acf0e6fb6a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475423"
---
# <a name="system-cant-update-inventory-quantity-because-of-insufficient-transactions"></a>يتعذر على النظام تحديث كمية المخزون نظرًا لعدم وجود حركات كافية

## <a name="symptoms"></a>العلامات

قد تحدث هذه المشكلة في حاله عدم تمكن النظام من تحديث كميه مخزون نظرا لعدم وجود حركات مخزون كافيه بالابعاد المحددة. سوف تتلقى رسالة الخطأ التالية:

> تعذر تحديثكميه المخزون - %1 بسبب عدم كفاية حركات المخزون الخاصة بالصنف %2 ذي حجم الابعاد = %3، اللون = %4، الإضافات = %5، الموقع = %6، المستودع = %7، الموقع = %8، حاله المخزون = متاح، لوح الترخيص = %9، رقم المجموعة = %10 لمعرف المرجع %11 في معرف الشحنة %12.

## <a name="resolution"></a>الحل

تاكد من عدم قيام إيه حركات مخزون بالفعل بحجز الكمية. علي سبيل المثال ، قد تقوم هذه الحركات بفتح أوامر الجودة أو سجلات حظر المخزون أو أوامر المخرجات.
