---
title: لا يتم تحديث قيمة التأخير عند إعادة جدولة أمر مخطط
description: لا يتم تحديث قيمة التأخير عند إعادة جدولة أمر مخطط
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 566702913774cf002ab38e367f690a479d968657
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475495"
---
# <a name="the-delay-value-isnt-updated-when-you-reschedule-a-planned-order"></a>لا يتم تحديث قيمة التأخير عند إعادة جدولة أمر مخطط

## <a name="symptoms"></a>العلامات

لا يتم تحديث قيمة التأخير عند إعادة جدولة أمر مخطط.

## <a name="resolution"></a>الحل

لتحديث تاخير الأوامر المخططة ، افتح مربع الحوار **أعاده الجدولة** للأمر المخطط. في علامة التبويب السريعة **تقسيم**، تأكد من تعيين الخيار **إجراء التقسيم بعد إعادة الجدولة** على القيمة *نعم*.
