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
ms.openlocfilehash: 817802f1f2ad3ab07f35c28d3e833a14cd02cf8b9705c576325dc83933a0c6de
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751759"
---
# <a name="the-indirect-costs-in-process-report-includes-deleted-production-orders"></a>يشتمل تقرير التكلفة غير المباشرة قيد التنفيذ على أوامر الإنتاج المحذوفة

رقم KB: 4612748

## <a name="symptoms"></a>العلامات

يقدم تقرير **التكلفة غير المباشرة قيد التنفيذ** معلومات حول أوامر الإنتاج التي تتم معالجتها جزئيًا وحذفها فيما بعد.

## <a name="resolution"></a>الدقة

عند عكس أمر إنتاج، فإنك تقوم أيضًا بعكس كافة حركات أمر الإنتاج ذلك. عند حذف أمر الإنتاج، تستمر جداول دفتر الأستاذ الفرعي ودفتر الأستاذ العام في كافة الحركات المرتبطة به. ستعرض التقارير الحركات في جداول دفتر الأستاذ الفرعي. بالنسبة لأمر الإنتاج المحدد، يجب أن يكون صافي القيمة 0.00.
