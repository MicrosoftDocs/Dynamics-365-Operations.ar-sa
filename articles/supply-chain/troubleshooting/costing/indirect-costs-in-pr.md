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
# <a name="the-indirect-costs-in-process-report-includes-deleted-production-orders"></a><span data-ttu-id="ff64c-103">يشتمل تقرير التكلفة غير المباشرة قيد التنفيذ على أوامر الإنتاج المحذوفة</span><span class="sxs-lookup"><span data-stu-id="ff64c-103">The Indirect costs in process report includes deleted production orders</span></span>

<span data-ttu-id="ff64c-104">رقم KB: 4612748</span><span class="sxs-lookup"><span data-stu-id="ff64c-104">KB number: 4612748</span></span>

## <a name="symptoms"></a><span data-ttu-id="ff64c-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="ff64c-105">Symptoms</span></span>

<span data-ttu-id="ff64c-106">يقدم تقرير **التكلفة غير المباشرة قيد التنفيذ** معلومات حول أوامر الإنتاج التي تتم معالجتها جزئيًا وحذفها فيما بعد.</span><span class="sxs-lookup"><span data-stu-id="ff64c-106">The **Indirect costs in process** report presents information about production orders that were partially processed and later deleted.</span></span>

## <a name="resolution"></a><span data-ttu-id="ff64c-107">الدقة</span><span class="sxs-lookup"><span data-stu-id="ff64c-107">Resolution</span></span>

<span data-ttu-id="ff64c-108">عند عكس أمر إنتاج، فإنك تقوم أيضًا بعكس كافة حركات أمر الإنتاج ذلك.</span><span class="sxs-lookup"><span data-stu-id="ff64c-108">When you reverse a production order, you also reverse all the transactions of that production order.</span></span> <span data-ttu-id="ff64c-109">عند حذف أمر الإنتاج، تستمر جداول دفتر الأستاذ الفرعي ودفتر الأستاذ العام في كافة الحركات المرتبطة به.</span><span class="sxs-lookup"><span data-stu-id="ff64c-109">When you delete the production order, the subledger tables and general ledger persist all transactions that are related to it.</span></span> <span data-ttu-id="ff64c-110">ستعرض التقارير الحركات في جداول دفتر الأستاذ الفرعي.</span><span class="sxs-lookup"><span data-stu-id="ff64c-110">The reports will show the transactions in the subledger tables.</span></span> <span data-ttu-id="ff64c-111">بالنسبة لأمر الإنتاج المحدد، يجب أن يكون صافي القيمة 0.00.</span><span class="sxs-lookup"><span data-stu-id="ff64c-111">For the specific production order, the net value should be 0.00.</span></span>
