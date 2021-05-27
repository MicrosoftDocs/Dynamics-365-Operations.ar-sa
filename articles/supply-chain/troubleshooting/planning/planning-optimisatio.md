---
title: يتم إنشاء أمر الشراء المخطط عندما يكون الشراء موجودًا خلال الأيام السالبة
description: إذا كان الحد الأدنى/الحد الأقصى لكود التغطية، فإن تحسين التخطيط يؤدي إلى إنشاء أمر شراء مخطط عندما يكون الشراء موجودًا خلال الأيام السالبة.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo,MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 826496c2de956ff949dd79ab8aa643053719bf75
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026241"
---
# <a name="planned-purchase-order-is-created-when-a-purchase-exists-within-negative-days"></a><span data-ttu-id="8fb7c-103">يتم إنشاء أمر الشراء المخطط عندما يكون الشراء موجودًا خلال الأيام السالبة</span><span class="sxs-lookup"><span data-stu-id="8fb7c-103">Planned purchase order is created when a purchase exists within negative days</span></span>

<span data-ttu-id="8fb7c-104">رقم KB: 4614298</span><span class="sxs-lookup"><span data-stu-id="8fb7c-104">KB number: 4614298</span></span>

## <a name="symptoms"></a><span data-ttu-id="8fb7c-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="8fb7c-105">Symptoms</span></span>

<span data-ttu-id="8fb7c-106">إذا كان *الحد الأدنى/الحد الأقصى* لكود التغطية، فإن تحسين التخطيط يؤدي إلى إنشاء أمر شراء مخطط عندما يكون الشراء موجودًا خلال الأيام السالبة.</span><span class="sxs-lookup"><span data-stu-id="8fb7c-106">If the coverage code is *Min/max*, Planning Optimization creates a planned purchase order when a purchase exists within negative days.</span></span>

## <a name="resolution"></a><span data-ttu-id="8fb7c-107">الدقة</span><span class="sxs-lookup"><span data-stu-id="8fb7c-107">Resolution</span></span>

<span data-ttu-id="8fb7c-108">لا يدعم تحسين التخطيط الأيام السالبة.</span><span class="sxs-lookup"><span data-stu-id="8fb7c-108">Planning Optimization doesn't support negative days.</span></span> <span data-ttu-id="8fb7c-109">ومع ذلك، فإنه يضمن دومًا أنه لن تتم جدولة الأوامر المخططة خلال زمن وصول البضاعة بالنسبة للتاريخ الحالي.</span><span class="sxs-lookup"><span data-stu-id="8fb7c-109">However, it always ensures that planned orders won't be scheduled within the lead time relative to the current date.</span></span> <span data-ttu-id="8fb7c-110">على سبيل المثال، يكون وقت إنتاج المشتريات 10 أيام، ويتوقع أن يصل أمر الشراء إلى ثمانية أيام بدءًا اليوم.</span><span class="sxs-lookup"><span data-stu-id="8fb7c-110">For example, the purchase lead time is 10 days, and a purchase order is expected to arrive eight days from today.</span></span> <span data-ttu-id="8fb7c-111">في هذه الحالة، سيتم استخدام أمر الشراء كتوريد للطلب الذي يكون خمسة أيام بدءًا من اليوم.</span><span class="sxs-lookup"><span data-stu-id="8fb7c-111">In this case, the purchase order will be used as supply for demand that is five days from today.</span></span>

<span data-ttu-id="8fb7c-112">وبالتالي، نوصي بضبط أوقات الإنتاج المحتمل لتغطية جميع (أو الكل تقريبًا) من وحدات السيناريو الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="8fb7c-112">Therefore, we recommend that you adjust your lead times to cover all (or almost all) of your scenarios.</span></span>
