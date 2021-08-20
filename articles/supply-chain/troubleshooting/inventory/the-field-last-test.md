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
ms.openlocfilehash: 46523c55f4fd42b0985397752f0c62a3e1a55e177f2308e20b7064e339758269
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742018"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a>لم يتم تحديث حقل تاريخ الاختبار الأخير عند إنشاء أوامر الجودة المتعددة

رقم KB: 4612803

## <a name="symptoms"></a>العلامات

لم يتم تحديث حقل **تاريخ الاختبار الأخير** عند إنشاء أوامر الجودة المتعددة.

## <a name="resolution"></a>الدقة

يعمل النظام كما هو مصمم. آخر تاريخ تم اختباره غير مرتبط بأوامر الجودة. ويقوم بتخزين التاريخ الذي تم فيه شراء البضائع المنتهية لأول مرة أو تصنيعها. يتم استخدام هذا التاريخ لحساب تاريخ إشعار الصلاحية لفترة الصلاحية.
