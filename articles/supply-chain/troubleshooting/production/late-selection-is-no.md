---
title: عدم مراعاة التحديد المتأخر عند إعادة تعيين أوامر الإنتاج عبر وظيفة دفعة
description: عند استخدام وظيفة دفعة متكررة لإعادة تعيين حالة أمر إنتاج، لا يتم مراعاة التحديدات المتأخرة.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e53198f427f4060421a4f0078277682c43db1320
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026229"
---
# <a name="late-selection-isnt-respected-when-production-orders-are-reset-via-a-batch-job"></a><span data-ttu-id="41cc3-103">عدم مراعاة التحديد المتأخر عند إعادة تعيين أوامر الإنتاج عبر وظيفة دفعة</span><span class="sxs-lookup"><span data-stu-id="41cc3-103">Late selection isn't respected when production orders are reset via a batch job</span></span>

<span data-ttu-id="41cc3-104">رقم KB: 4614634</span><span class="sxs-lookup"><span data-stu-id="41cc3-104">KB number: 4614634</span></span>

## <a name="symptoms"></a><span data-ttu-id="41cc3-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="41cc3-105">Symptoms</span></span>

<span data-ttu-id="41cc3-106">عند استخدام وظيفة دفعة متكررة لإعادة تعيين حالة أمر إنتاج، لا يتم مراعاة التحديدات المتأخرة.</span><span class="sxs-lookup"><span data-stu-id="41cc3-106">When you use a recurring batch job to reset the status of a production order, late selections aren't respected.</span></span>

## <a name="resolution"></a><span data-ttu-id="41cc3-107">الدقة</span><span class="sxs-lookup"><span data-stu-id="41cc3-107">Resolution</span></span>

<span data-ttu-id="41cc3-108">لا يدعم التصميم الحالي استخدام التحديدات المتأخرة لعملية *إعادة تعيين الحالة*.</span><span class="sxs-lookup"><span data-stu-id="41cc3-108">The current design doesn't support the use of late selections for the *Reset status* process.</span></span>
