---
title: خطأ في حساب تكاليف الإصدار التلقائي أثناء إقفال المخزون
description: في الإصدارات السابقة، ربما تكون قد تلقيت خطأ في حساب تحديد تكاليف الإصدار أثناء إقفال المخزون. تم إصلاح هذه المشكلة.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ae92b7121998d6b1ba2f08ea5736c55637867fbf
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475457"
---
# <a name="backflush-costing-calculation-error-during-inventory-closing"></a>خطأ في حساب تكاليف الإصدار التلقائي أثناء إقفال المخزون

## <a name="symptoms"></a>العلامات

في الإصدارات قبل إصدار 10.0.13 ، إذا كنت لا تستخدم تدفق تكلفه الإنتاج lean ، ستتلقى رسالة التحذير التالية اثناء اقفال المخزون:

> أنت علي وشك تنفيذ إغلاق المخزون بتاريخ %1. لا يوجد تنفيذ لحساب تكاليف الإصدار التلقائي %1 الذي تم تسجيل نهاية الفترة المطابقة. لا تنس تنفيذ حساب تكاليف الإصدار التلقائي بتاريخ %1 التي تطابق نهاية الفترة. قد لا يكون تقييم المخزونات وتكلفة البضائع المبيعة والتباينات صحيحة في دفتر الأستاذ الفرعي أو دفتر الأستاذ العام حتى يتم تنفيذ ذلك.

## <a name="resolution"></a>الحل

تم إصلاح هذه المشكلة في 10.0.13 الطرح والإصدارات الأحدث. للحصول على مزيد من المعلومات، راجع [قاعدة المعارف 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).
