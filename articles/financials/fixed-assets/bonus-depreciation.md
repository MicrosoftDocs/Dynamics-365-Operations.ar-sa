---
title: الإهلاك الإضافي
description: توفر هذه المقالة نظرة عامة على وظيفة إهلاك الإضافي‬.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3621
ms.assetid: 835ec594-744e-461c-a676-1b9abc094173
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e05c0c195ddb948547ae008d050686bbcdc6ed3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "323308"
---
# <a name="bonus-depreciation"></a><span data-ttu-id="f61a4-103">الإهلاك الإضافي</span><span class="sxs-lookup"><span data-stu-id="f61a4-103">Bonus depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f61a4-104">توفر هذه المقالة نظرة عامة على وظيفة إهلاك الإضافي‬.</span><span class="sxs-lookup"><span data-stu-id="f61a4-104">This article provides an overview of the bonus depreciation functionality.</span></span>

<span data-ttu-id="f61a4-105">بالنسبة إلى الإهلاك الإضافي، يمكنك أخذ مبالغ إهلاك زائدة أو إضافية خلال العام الأول الذي يتم فيه وضع الأصل في الخدمة ويتم إهلاكه.</span><span class="sxs-lookup"><span data-stu-id="f61a4-105">For bonus depreciation, you can take extra or bonus depreciation amounts during the first year that the asset is put in service and depreciated.</span></span> <span data-ttu-id="f61a4-106">يجب أخذ الإهلاك الإضافي قبل أية حسابات إهلاك أخرى.</span><span class="sxs-lookup"><span data-stu-id="f61a4-106">Bonus depreciation must be taken before any other depreciation calculations.</span></span> <span data-ttu-id="f61a4-107">ولذلك، من الأفضل استخدام الإهلاك الإضافي مع دفاتر حيث تم تعطيل وظيفة "الترحيل إلى دفتر الأستاذ العام".</span><span class="sxs-lookup"><span data-stu-id="f61a4-107">Therefore, it's best to use bonus depreciation with books where the Post to general ledger functionality is disabled.</span></span> <span data-ttu-id="f61a4-108">يمكنك استخدام الخيار **حذف الحركات التي لم يتم ترحيلها إلى دفتر الأستاذ العام‬** لحذف الحركات التاريخية للدفاتر التي لا يتم ترحيلها إلى دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="f61a4-108">You can use the **Delete transactions not posted to general ledger** option to delete historical transactions for books that don't post to the general ledger.</span></span> <span data-ttu-id="f61a4-109">ويمكنك عندئذٍ استيعاب الإهلاك الإضافي لاحقًا في دورة حياة الأصول عن طريق حذف حركات الإهلاك التي تم ترحيلها مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="f61a4-109">You can then accommodate bonus depreciation later in the asset life cycle by deleting depreciation transactions that were previously posted.</span></span> 

<span data-ttu-id="f61a4-110">يمكن حساب الإهلاك الإضافي باستخدام عملية المقترح أو يمكن إنشاء حركات إهلاك إضافي يدويًا.</span><span class="sxs-lookup"><span data-stu-id="f61a4-110">You can calculate bonus depreciation by using the proposal process, or you can create manual bonus depreciation transactions.</span></span> <span data-ttu-id="f61a4-111">لا يمكنك إنشاء حركات إهلاك إضافي في حالة وجود حركات إهلاك أو حركات تعديل إهلاك لدفتر الأصل هذا.</span><span class="sxs-lookup"><span data-stu-id="f61a4-111">You can't create bonus depreciation transactions if depreciation transactions or depreciation adjustment transactions exist for that asset book.</span></span>

<span data-ttu-id="f61a4-112">وعند استخدام عملية المقترح لحساب الإهلاك الإضافي، يتم تضمين كافة الحركات الإضافية الموجودة في حساب الأساس.</span><span class="sxs-lookup"><span data-stu-id="f61a4-112">When you use the proposal process to calculate bonus depreciation, all existing bonus transactions are included in the calculation of the basis.</span></span> <span data-ttu-id="f61a4-113">ويتضمن الحساب أيضًا أي إهلاكات إضافية سابقة قمت بإدخالها يدويًا للأصل.</span><span class="sxs-lookup"><span data-stu-id="f61a4-113">The calculation also includes any previous bonus depreciations that you manually entered for the asset.</span></span> 

<span data-ttu-id="f61a4-114">إذا تم أخذ أكثر من إهلاك إضافي واحد لأحد الأصول، فستتم مراعاة الأولوية.</span><span class="sxs-lookup"><span data-stu-id="f61a4-114">If more than one bonus depreciation will be taken for an asset, the priority is considered.</span></span> <span data-ttu-id="f61a4-115">يقوم كل إهلاك إضافي بتقليل أساس الأصل للإهلاك الإضافي التالي.</span><span class="sxs-lookup"><span data-stu-id="f61a4-115">Each bonus reduces the asset basis for the next bonus.</span></span> <span data-ttu-id="f61a4-116">لا تؤخذ القيمة الباقية في الاعتبار في أساس الأصل لحسابات الإهلاك الإضافي، ولا يتم تطبيق قواعد الإهلاك على الإهلاك الإضافي.</span><span class="sxs-lookup"><span data-stu-id="f61a4-116">Salvage value isn't considered in the asset basis for bonus depreciation calculations, and the depreciation convention doesn't apply for bonus depreciation.</span></span> 

<span data-ttu-id="f61a4-117">تأهلت حاليًا بعض الممتلكات في الولايات المتحدة لتصبح ممتلكات تنطبق عليها المادة 179.</span><span class="sxs-lookup"><span data-stu-id="f61a4-117">Currently, in the United States, some property qualifies as Section 179 property.</span></span> <span data-ttu-id="f61a4-118">وباستخدام الخصم في القسم 179، يمكنك استرداد التكلفة الكاملة لبعض الممتلكات أو تكلفتها الجزئية، إلى حد معين.</span><span class="sxs-lookup"><span data-stu-id="f61a4-118">By using the Section 179 deduction, you can recover all or part of the cost of some property, up to a limit.</span></span> <span data-ttu-id="f61a4-119">يمكنك استرداد التكلفة عن طريق خصمها خلال السنة عندما تضع الممتلكات قيد الخدمة.</span><span class="sxs-lookup"><span data-stu-id="f61a4-119">You can recover the cost by deducting it in the year when you put the property in service.</span></span>

## <a name="example"></a><span data-ttu-id="f61a4-120">مثال</span><span class="sxs-lookup"><span data-stu-id="f61a4-120">Example</span></span>
<span data-ttu-id="f61a4-121">تقترن الإهلاكات الإضافية التالية تقترن بدفتر أصل:</span><span class="sxs-lookup"><span data-stu-id="f61a4-121">The following bonus depreciations are associated with an asset book:</span></span>

-   <span data-ttu-id="f61a4-122">**المادة 179:** 1,000.00، الأولوية 1</span><span class="sxs-lookup"><span data-stu-id="f61a4-122">**Section 179:** 1,000.00, Priority 1</span></span>
-   <span data-ttu-id="f61a4-123">**منطقة الحرية:** 30 في المائة، الأولوية 2</span><span class="sxs-lookup"><span data-stu-id="f61a4-123">**Liberty Zone:** 30 percent, Priority 2</span></span>

<span data-ttu-id="f61a4-124">تبلغ تكلفة الاستحواذ على الأصل 5,000.00 دولار.</span><span class="sxs-lookup"><span data-stu-id="f61a4-124">The asset acquisition cost is 5,000.00.</span></span> <span data-ttu-id="f61a4-125">عند حساب الإهلاك الإضافي، يكون مبلغ أول إهلاك إضافي 1,000.00 دولار للإهلاك الخاص بالمادة 179.</span><span class="sxs-lookup"><span data-stu-id="f61a4-125">When bonus depreciation is calculated, the first bonus depreciation amount is 1,000.00 for the Section 179 depreciation.</span></span> 

<span data-ttu-id="f61a4-126">ويتم حساب مبلغ الإهلاك الإضافي التالي، لمنطقة الحرية، على الشكل التالي:</span><span class="sxs-lookup"><span data-stu-id="f61a4-126">The next bonus depreciation amount, for the Liberty Zone depreciation, is calculated as follows:</span></span> 

<span data-ttu-id="f61a4-127">تكلفة الاستحواذ – 1000 دولار (الإهلاك الخاص بالمادة 179) × 30 بالمئة = 1.200 دولار</span><span class="sxs-lookup"><span data-stu-id="f61a4-127">Acquisition cost – 1,000 (Section 179 depreciation) × 30 percent = 1,200</span></span> 

<span data-ttu-id="f61a4-128">إذا كان مبلغ الإهلاك الإضافي أكبر من تكلفة الاستحواذ المتبقية، فإن مبلغ الإهلاك الإضافي سيكون ناتج حساب الإهلاك الإضافي أو تكلفة الاستحواذ المتبقية، أيهما أقل.</span><span class="sxs-lookup"><span data-stu-id="f61a4-128">If the bonus depreciation amount is more than the remaining acquisition cost, the bonus depreciation amount is either the result of the bonus depreciation calculation or the remaining acquisition cost, whichever amount is less.</span></span> 

<span data-ttu-id="f61a4-129">إذا كانت تكلفة الاستحواذ المتبقية تساوي صفرًا أو أقل، فلن يتم إنشاء حركات إهلاك إضافي.</span><span class="sxs-lookup"><span data-stu-id="f61a4-129">If the remaining acquisition cost is 0 (zero) or less, bonus depreciation transactions isn't generated.</span></span> 

<span data-ttu-id="f61a4-130">عند حساب الإهلاك الإضافي باستخدام عملية المقترح، فسوف يتم إنشاء حركة إهلاك إضافي لجميع سجلات الإهلاك الإضافي السارية والمقترنة بدفتر الأصل.</span><span class="sxs-lookup"><span data-stu-id="f61a4-130">When bonus depreciation is calculated by using the proposal process, a bonus depreciation transaction is created for all applicable bonus depreciation records that are associated with the asset book.</span></span> 

<span data-ttu-id="f61a4-131">يمكن إنشاء عدد غير محدود من سجلات الإهلاك الإضافي.</span><span class="sxs-lookup"><span data-stu-id="f61a4-131">You can create an unlimited number of bonus depreciation records.</span></span> <span data-ttu-id="f61a4-132">وبعد تعيين هذه السجلات إلى دفتر مجموعة الأصول، سيتم تطبيقها على دفتر الأصل.</span><span class="sxs-lookup"><span data-stu-id="f61a4-132">After you assign those records to the asset group book, they are applied to the asset book.</span></span> 

<span data-ttu-id="f61a4-133">يتم إدخال الإهلاك الإضافي كنسبة مئوية أو مبلغ ثابت.</span><span class="sxs-lookup"><span data-stu-id="f61a4-133">Bonus depreciation is entered as either a percentage or a fixed amount.</span></span> <span data-ttu-id="f61a4-134">عند ترحيل مقترحات إهلاك، يتم ترحيل حركات الإهلاك الإضافي إلى الدفتر كحركات منفصلة عن حركات الإهلاك.</span><span class="sxs-lookup"><span data-stu-id="f61a4-134">When you post depreciation proposals, bonus depreciation transactions are posted to the book as separate transactions from the depreciation transactions.</span></span>



