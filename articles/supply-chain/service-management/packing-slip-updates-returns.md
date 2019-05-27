---
title: تحديثات كشف التعبئة للمرتجعات
description: قبل استلام الأصناف المرتجعة في المخزون، يجب تحديث كشف التعبئة الخاص بالأمر الذي تنتمي إليه هذا الأصناف.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4aba61e6acf5fb959917da9ddea94c21fe1460d1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552874"
---
# <a name="packing-slip-updates-for-returns"></a><span data-ttu-id="e4260-103">تحديثات كشف التعبئة للمرتجعات</span><span class="sxs-lookup"><span data-stu-id="e4260-103">Packing slip updates for returns</span></span>  

[!include [banner](../includes/banner.md)]


<span data-ttu-id="e4260-104">قبل استلام الأصناف المرتجعة في المخزون، يجب تحديث كشف التعبئة الخاص بالأمر الذي تنتمي إليه هذا الأصناف.</span><span class="sxs-lookup"><span data-stu-id="e4260-104">Before returned items can be received into inventory, the packing slip for the order to which they belong must be updated.</span></span> <span data-ttu-id="e4260-105">ويشبه التحديث إلى الحركة المالية عملية تحديث الفاتورة، وتعد عملية تحديث كشف التعبئة التحديث المادي لسجل المخزون؛ ما يعني أنه يحول التكاليف إلى المخزون.</span><span class="sxs-lookup"><span data-stu-id="e4260-105">Just as the invoice update process is the update to the financial transaction, the packing slip update process is the physical update of the inventory record, which means that it commits the changes to inventory.</span></span> <span data-ttu-id="e4260-106">عندما يتعلق الأمر بالمرتجعات، يتم تنفيذ الخطوات التي تم تعيينها لإجراء الإرجاع أثناء تحديث إيصال التعبئة.</span><span class="sxs-lookup"><span data-stu-id="e4260-106">In the case of returns, the steps that are assigned to the disposition action are implemented during the packing slip update.</span></span>

<span data-ttu-id="e4260-107">يمكن معالجة تحديث كشف التعبئة في دفتر يومية وصول الصنف أو في أمر الإرجاع.</span><span class="sxs-lookup"><span data-stu-id="e4260-107">The packing slip update can be processed in either the item arrival journal or the return order.</span></span>

<span data-ttu-id="e4260-108">وفي إطار عملية ترحيل كشف التعبئة، يمكن ربط رقم مرجع كشف التعبئة من مستندات الشحن الخاصة بالعميل مع بنود الأمر.</span><span class="sxs-lookup"><span data-stu-id="e4260-108">As part of the process for posting packing slips, the packing slip reference number from the customer’s shipping documents can be associated with the order lines.</span></span> <span data-ttu-id="e4260-109">يعتبر هذا الاقتران اختياريًا وكمرجع فقط.</span><span class="sxs-lookup"><span data-stu-id="e4260-109">This association is optional and for reference only.</span></span> <span data-ttu-id="e4260-110">ولا ينشئ أية تحديثات خاصة بالحركات‬.</span><span class="sxs-lookup"><span data-stu-id="e4260-110">It does not create any transactional updates.</span></span>

<span data-ttu-id="e4260-111">إذا لم تصل كافة الأصناف المرتجعة المتوقعة، فيجب عليك تضمين الكمية التي تم استلامها في تحديث كشف التعبئة فقط.</span><span class="sxs-lookup"><span data-stu-id="e4260-111">If not all of the expected return items have arrived, you should include only the quantity that has been received in the packing slip update.</span></span> <span data-ttu-id="e4260-112">ودع الأصناف المتبقية على الأمر حتى تصل باقي شحنة المرتجعات.</span><span class="sxs-lookup"><span data-stu-id="e4260-112">Leave the remaining items on the order until the rest of the return shipment has arrived.</span></span>

<span data-ttu-id="e4260-113">إذا تم إرسال صنف مرة أخرى من الفحص إلى قسم الشحن والاستلام، كما يكون الأمر عندما لا يعلم المفتش أين يقوم بتخزين الصنف في المخزون، عندئذٍ يجب تحديث كشف التعبئة المقابل وذلك للتسجيل الصحيح والعمل على كود الترتيب الذي يتم تحديده كنتيجة للفحص.</span><span class="sxs-lookup"><span data-stu-id="e4260-113">If an item is sent back from quarantine to the Shipping and Receiving department, such as when the quarantine inspector does not know where to store the item in inventory, the corresponding packing slip must be updated to correctly register and act on the disposition code that is specified as a result of the quarantine.</span></span>

<span data-ttu-id="e4260-114">عندما تقوم بتحديث كشف تعبئة لصنف مرتجع من اتفاقية مبيعات، يتم تحديث التزام اتفاقية المبيعات لهذا الصنف تلقائياً ليعكس التغيير في الكمية أو المبلغ.</span><span class="sxs-lookup"><span data-stu-id="e4260-114">When you update a packing slip for a returned item that is from a sales agreement, the sales agreement commitment for that item is automatically updated to reflect the change in the quantity or the amount.</span></span> 

## <a name="see-also"></a><span data-ttu-id="e4260-115">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="e4260-115">See also</span></span>

[<span data-ttu-id="e4260-116">إجراء تحديثات الفاتورة للمرتجعات</span><span class="sxs-lookup"><span data-stu-id="e4260-116">Perform invoice updates for returns</span></span>](perform-invoice-updates-for-returns.md)

  


