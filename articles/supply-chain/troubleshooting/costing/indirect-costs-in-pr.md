---
title: يشتمل تقرير التكلفة غير المباشرة قيد التنفيذ على أوامر الإنتاج المحذوفة
description: يقدم تقرير التكلفة غير المباشرة قيد التنفيذ معلومات حول أوامر الإنتاج التي تتم معالجتها جزئيًا وحذفها فيما بعد.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdIndirectCostInProgress
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 707fa9bb30129c3656e10c6756dee770a7712e65
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026236"
---
# <a name="the-indirect-costs-in-process-report-includes-deleted-production-orders"></a>يشتمل تقرير التكلفة غير المباشرة قيد التنفيذ على أوامر الإنتاج المحذوفة

رقم KB: 4612748

## <a name="symptoms"></a>العلامات

يقدم تقرير **التكلفة غير المباشرة قيد التنفيذ** معلومات حول أوامر الإنتاج التي تتم معالجتها جزئيًا وحذفها فيما بعد.

## <a name="resolution"></a>الدقة

عند عكس أمر إنتاج، فإنك تقوم أيضًا بعكس كافة حركات أمر الإنتاج ذلك. عند حذف أمر الإنتاج، تستمر جداول دفتر الأستاذ الفرعي ودفتر الأستاذ العام في كافة الحركات المرتبطة به. ستعرض التقارير الحركات في جداول دفتر الأستاذ الفرعي. بالنسبة لأمر الإنتاج المحدد، يجب أن يكون صافي القيمة 0.00.
