---
title: لا توجد قيمة "من تاريخ" في علامة التبويب "الأسعار النشطة" لصفحة أسعار الأصناف
description: لا توجد قيمة "من تاريخ" في علامة التبويب "الأسعار النشطة" لصفحة أسعار الأصناف.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dd13f6a3e5ce3c894e96f420358d337f2e43dba
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026250"
---
# <a name="there-is-no-from-date-value-on-the-active-prices-tab-of-the-item-price-page"></a><span data-ttu-id="748d8-103">لا توجد قيمة "من تاريخ" في علامة التبويب "الأسعار النشطة" لصفحة أسعار الأصناف</span><span class="sxs-lookup"><span data-stu-id="748d8-103">There is no From date value on the Active prices tab of the Item price page</span></span>

<span data-ttu-id="748d8-104">رقم KB: 4613548</span><span class="sxs-lookup"><span data-stu-id="748d8-104">KB number: 4613548</span></span>

## <a name="symptoms"></a><span data-ttu-id="748d8-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="748d8-105">Symptoms</span></span>

<span data-ttu-id="748d8-106">لا توجد قيمة **من تاريخ** في علامة التبويب **الأسعار النشطة** للصفحة **سعر الصنف**.</span><span class="sxs-lookup"><span data-stu-id="748d8-106">There is no **From date** value on the **Active prices** tab of the **Item price** page.</span></span>

## <a name="resolution"></a><span data-ttu-id="748d8-107">الدقة</span><span class="sxs-lookup"><span data-stu-id="748d8-107">Resolution</span></span>

<span data-ttu-id="748d8-108">لا يتم تحويل القيمة **من تاريخ** (تاريخ السريان) التي تم تعيينها في السعر المعلق إلى السعر النشط.</span><span class="sxs-lookup"><span data-stu-id="748d8-108">The **From date** value (effective date) that is set on the pending price isn't transferred to the active price.</span></span>

<span data-ttu-id="748d8-109">وعندما يتم إدخال سجل تكلفة الصنف أولاً، يكون بحالة *معلق* وتاريخ سريان محدد.</span><span class="sxs-lookup"><span data-stu-id="748d8-109">When an item cost record is first entered, it has a status of *Pending* and an intended effective date.</span></span> <span data-ttu-id="748d8-110">وعندما تقوم بتنشيط سجل تكاليف الصنف، يتم تحديث الحالة إلى *نشطة*، وتاريخ السريان إلى تاريخ التنشيط.</span><span class="sxs-lookup"><span data-stu-id="748d8-110">When you activate the item cost record, the status is updated to *Active*, and the effective date is updated to the activation date.</span></span> <span data-ttu-id="748d8-111">وبالتالي، يكون تاريخ تنشيط السعر النشط دائمًا هو التاريخ الفعلي للتنشيط.</span><span class="sxs-lookup"><span data-stu-id="748d8-111">Therefore, the active price's activation date is always the actual date of the activation.</span></span>

<span data-ttu-id="748d8-112">لمزيد من المعلومات، راجع [نظرة عامة حول إصدارات التكلفة](../../cost-management/costing-versions.md).</span><span class="sxs-lookup"><span data-stu-id="748d8-112">For more information, see [Costing versions overview](../../cost-management/costing-versions.md).</span></span>
