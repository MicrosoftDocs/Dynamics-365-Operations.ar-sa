---
title: لم يتم تحديث حقل تاريخ الاختبار الأخير عند إنشاء أوامر الجودة المتعددة
description: لم يتم تحديث حقل تاريخ الاختبار الأخير عند إنشاء أوامر الجودة المتعددة.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f796bdaa88d32b1c58dd8a4bca19f0ce4f3943d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026246"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a>لم يتم تحديث حقل تاريخ الاختبار الأخير عند إنشاء أوامر الجودة المتعددة

رقم KB: 4612803

## <a name="symptoms"></a>العلامات

لم يتم تحديث حقل **تاريخ الاختبار الأخير** عند إنشاء أوامر الجودة المتعددة.

## <a name="resolution"></a>الدقة

يعمل النظام كما هو مصمم. آخر تاريخ تم اختباره غير مرتبط بأوامر الجودة. ويقوم بتخزين التاريخ الذي تم فيه شراء البضائع المنتهية لأول مرة أو تصنيعها. يتم استخدام هذا التاريخ لحساب تاريخ إشعار الصلاحية لفترة الصلاحية.
