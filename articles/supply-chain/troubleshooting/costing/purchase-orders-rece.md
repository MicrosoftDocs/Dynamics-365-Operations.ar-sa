---
title: لا تظهر أوامر الشراء التي تم استلامها فعليًا في تقرير إقفال المخزون
description: لا تظهر أوامر الشراء التي تم استلامها فعليًا في تقرير إقفال المخزون للكميات المفتوحة.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventOpenQtyCritical
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 9508d6d75d8ebee7ca10140ed4c4215d7ad1dda7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026235"
---
# <a name="physically-received-purchase-orders-dont-appear-on-the-inventory-closing-report"></a><span data-ttu-id="dd414-103">لا تظهر أوامر الشراء التي تم استلامها فعليًا في تقرير إقفال المخزون</span><span class="sxs-lookup"><span data-stu-id="dd414-103">Physically received purchase orders don't appear on the inventory closing report</span></span>

<span data-ttu-id="dd414-104">رقم KB: 4612595</span><span class="sxs-lookup"><span data-stu-id="dd414-104">KB number: 4612595</span></span>

## <a name="symptoms"></a><span data-ttu-id="dd414-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="dd414-105">Symptoms</span></span>

<span data-ttu-id="dd414-106">لا تظهر أوامر الشراء التي تم استلامها فعليًا في تقرير إقفال المخزون **للكميات المفتوحة**.</span><span class="sxs-lookup"><span data-stu-id="dd414-106">Physically received purchase orders don't appear on the **Check open quantities** inventory closing report.</span></span>

## <a name="resolution"></a><span data-ttu-id="dd414-107">الدقة</span><span class="sxs-lookup"><span data-stu-id="dd414-107">Resolution</span></span>

<span data-ttu-id="dd414-108">يعرض التقرير **كميات المفتوحة** حركات الإصدار التي لا يمكن تسويتها مقابل إيصالات المخزون المحدثة ماليًا اعتبارًا من تاريخ الإقفال المحدد.</span><span class="sxs-lookup"><span data-stu-id="dd414-108">The **Check open quantities** report shows issue transactions that can't be settled against financially updated inventory receipts as of the selected closing date.</span></span> <span data-ttu-id="dd414-109">يمكنك اختيار تضمين إيصالات فعلية في التقرير.</span><span class="sxs-lookup"><span data-stu-id="dd414-109">You can choose to include physical receipts on the report.</span></span> <span data-ttu-id="dd414-110">وفي هذه الحالة، سيتم عرض عمليات الاستلام الفعلية إذا كان بإمكانها تغطية حركات الإصدار التي لا يمكن تسويتها.</span><span class="sxs-lookup"><span data-stu-id="dd414-110">In that case, physical receipts will be shown if they can cover the issue transactions that can't be settled.</span></span> <span data-ttu-id="dd414-111">لمزيد من المعلومات، راجع [‏‫الإعداد لتشغيل إغلاق المخزون](/dynamicsax-2012/appuser-itpro/preparing-to-run-inventory-close).</span><span class="sxs-lookup"><span data-stu-id="dd414-111">For more information, see [Preparing to run inventory close](/dynamicsax-2012/appuser-itpro/preparing-to-run-inventory-close).</span></span>
