---
title: لا تعمل إيصالات استلام المنتجات الملغية على تحديث حالة الحركة إلى مسجل
description: بعد إلغاء إيصالات استلام المنتجات في حمل العمل الوارد، يقوم النظام تلقائيًا بتحديث حالة حركة المخزون من تم الاستلام إلى مطلوب.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c86457d50a7a9ac2a699a0e0a9c7bdf4cd7c67b
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294000"
---
# <a name="canceled-product-receipts-dont-update-transaction-status-to-registered"></a><span data-ttu-id="73d16-103">لا تعمل إيصالات استلام المنتجات الملغية على تحديث حالة الحركة إلى مسجل</span><span class="sxs-lookup"><span data-stu-id="73d16-103">Canceled product receipts don't update transaction status to Registered</span></span>

## <a name="symptoms"></a><span data-ttu-id="73d16-104">العلامات</span><span class="sxs-lookup"><span data-stu-id="73d16-104">Symptoms</span></span>

<span data-ttu-id="73d16-105">بعد أن تقوم بتشغيل إجراء **إلغاء إيصالات استلام المنتجات** في حمل العمل الوارد، يقوم النظام تلقائيًا بتحديث حالة حركة المخزون من *تم الاستلام* إلى *مطلوب*.</span><span class="sxs-lookup"><span data-stu-id="73d16-105">After you run the **Cancel product receipts** action on an inbound load, the system automatically updates the status of inventory transactions from *Received* to *Ordered*.</span></span>

## <a name="resolution"></a><span data-ttu-id="73d16-106">الحل</span><span class="sxs-lookup"><span data-stu-id="73d16-106">Resolution</span></span>

<span data-ttu-id="73d16-107">عند إلغاء إيصالات التعبئة لأحمال العمل الواردة، تظل حالة حركات المخزون *منتقى*.</span><span class="sxs-lookup"><span data-stu-id="73d16-107">When packing slips are canceled for outbound loads, the status of inventory transactions remains *Picked*.</span></span> <span data-ttu-id="73d16-108">ومع ذلك، عندما يتم إلغاء إيصالات استلام المنتجات من حمل العمل الوراد، لا يتم استعادة حالة حركات المخزون إلى *مسجل*.</span><span class="sxs-lookup"><span data-stu-id="73d16-108">However, when product receipts from an inbound load are canceled, the status of inventory transactions isn't restored to *Registered*.</span></span> <span data-ttu-id="73d16-109">لذلك، بعد إلغاء إيصال استلام المنتجات من حمل العمل الوارد، يجب أن يقوم عامل المستودع بإعادة تسجيل كميات الأصناف لأحمال العمل.</span><span class="sxs-lookup"><span data-stu-id="73d16-109">Therefore, after a product receipt from an inbound load is canceled, the warehouse worker must re-register item quantities for the loads.</span></span>

<span data-ttu-id="73d16-110">لمزيد من المعلومات، راجع [تسجيل كميات الأصناف التي تصل إلى حمل العمل الوارد](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).</span><span class="sxs-lookup"><span data-stu-id="73d16-110">For more information, see [Register item quantities that arrive on an inbound load](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).</span></span>
