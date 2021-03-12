---
title: إهلاك الأصل الثابت
description: يوفر هذا الموضوع نظرة عامة حول إهلاك الأصول الثابتة.
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus, AssetBookTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 3121
ms.assetid: 98ff891f-e0e2-4184-b618-28107a50851f
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b399ab3df9bddbce8b96752ef344bf93cb2563c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969093"
---
# <a name="fixed-asset-depreciation"></a><span data-ttu-id="93814-103">إهلاك الأصل الثابت</span><span class="sxs-lookup"><span data-stu-id="93814-103">Fixed asset depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="93814-104">يوفر هذا الموضوع نظرة عامة حول إهلاك الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="93814-104">This topic provides an overview of depreciation for fixed assets.</span></span>

<span data-ttu-id="93814-105">الإهلاك هو حركة دورية تؤدي عادة إلى تقليل قيمة الأصل الثابت في الميزانية العمومية، ويتم تحصيله كنفقات في حساب الأرباح والخسائر.</span><span class="sxs-lookup"><span data-stu-id="93814-105">Depreciation is a periodic transaction that typically reduces the value of the fixed asset on the balance sheet, and is charged as an expenditure to a profit and loss account.</span></span> <span data-ttu-id="93814-106">وبالتالي، يتم عادةً استخدام حساب رئيسي لإضافة الإهلاك الدوري في الميزانية العمومية.</span><span class="sxs-lookup"><span data-stu-id="93814-106">Therefore, a main account is typically used to credit the periodic depreciation on the balance sheet.</span></span> <span data-ttu-id="93814-107">والحساب المقابل هو حساب في جزء الأرباح والخسائر في دليل الحسابات.</span><span class="sxs-lookup"><span data-stu-id="93814-107">An offset account is an account in the profit and loss part of the chart of accounts.</span></span>

## <a name="depreciation-adjustment"></a><span data-ttu-id="93814-108">تسوية الإهلاك</span><span class="sxs-lookup"><span data-stu-id="93814-108">Depreciation adjustment</span></span>
<span data-ttu-id="93814-109">عادةً ما يتم فقط ترحيل تصحيح لحركة إهلاك مرّحلة كتسوية إهلاك.</span><span class="sxs-lookup"><span data-stu-id="93814-109">Usually, only a correction to a posted depreciation transaction is posted as a depreciation adjustment.</span></span> <span data-ttu-id="93814-110">وبالتالي، يتم إعداد كلٍّ من الحساب الرئيسي والحساب المقابل تمامًا مثل حسابات الإهلاك.</span><span class="sxs-lookup"><span data-stu-id="93814-110">Therefore, both the main account and the offset account are set up just like the accounts for depreciation.</span></span> <span data-ttu-id="93814-111">بإمكان تسوية الإهلاك أن تكون مبلغًا موجبًا أو سالبًا، ولكن وظيفة الحساب الرئيسي (كحساب ميزانية عمومية) ووظيفة الحساب المقابل (عادةً كحساب الأرباح والخسائر) تبقى هي نفسها.</span><span class="sxs-lookup"><span data-stu-id="93814-111">A depreciation adjustment can be either a positive amount or a negative amount, but the functionality of the main account (as a balance sheet account) and the functionality of the offset account (usually as a profit and loss account) remain the same.</span></span>

## <a name="extraordinary-depreciation"></a><span data-ttu-id="93814-112">الإهلاك الاستثنائي</span><span class="sxs-lookup"><span data-stu-id="93814-112">Extraordinary depreciation</span></span>
<span data-ttu-id="93814-113">يعمل الإهلاك الاستثنائي بطريقة مماثلة لعمل الإهلاك الأساسي.</span><span class="sxs-lookup"><span data-stu-id="93814-113">Extraordinary depreciation works like basic depreciation.</span></span> <span data-ttu-id="93814-114">وبالتالي، يتم استخدام حساب رئيسي لإضافة مبلغ الإهلاك إلى الميزانية العمومية وتقليل قيمة الأصل الثابت.</span><span class="sxs-lookup"><span data-stu-id="93814-114">Therefore, a main account is used to credit the depreciation amount to the balance sheet and reduce the value of the fixed asset.</span></span> <span data-ttu-id="93814-115">والحساب المقابل هو حساب الأرباح والخسائر، حيث يتم تحميل الإهلاك المحسوب للفترة المالية كنفقات.</span><span class="sxs-lookup"><span data-stu-id="93814-115">An offset account is a profit and loss account, where the depreciation that is calculated for the fiscal period is charged as an expenditure.</span></span> 

<span data-ttu-id="93814-116">ويعمل الإهلاك الاستثنائي بطريقة مستقلة عن الإهلاك الأساسي.</span><span class="sxs-lookup"><span data-stu-id="93814-116">Extraordinary depreciation works independently of basic depreciation.</span></span> <span data-ttu-id="93814-117">وعندما يكون الإهلاك الاستثنائي نوع إهلاك منفصلاً، يمكنك ترحيل الإهلاك الاستثنائي وإعداد تقرير عنه بشكل منفصل عن الإهلاك الأساسي.</span><span class="sxs-lookup"><span data-stu-id="93814-117">By having extraordinary depreciation as a separate transaction type, you can post and report the extraordinary depreciation separately from the basic depreciation.</span></span>

## <a name="special-depreciation-allowance"></a><span data-ttu-id="93814-118">بدل الإهلاك الخاص</span><span class="sxs-lookup"><span data-stu-id="93814-118">Special depreciation allowance</span></span>
<span data-ttu-id="93814-119">يمكنك استخدام بدلات الإهلاك الخاص لتحصيل مبالغ إهلاك إضافية خلال السنة الأولى التي يوضع فيها الأصل قيد الخدمة ويتم إهلاكه.</span><span class="sxs-lookup"><span data-stu-id="93814-119">You can use special depreciation allowances to take extra depreciation amounts during the first year that an asset is put in service and depreciated.</span></span> <span data-ttu-id="93814-120">يجب أخذ بدلات الإهلاك الخاص قبل أية حسابات إهلاك أخرى.</span><span class="sxs-lookup"><span data-stu-id="93814-120">Special depreciation allowances must be taken before any other depreciation calculations.</span></span> <span data-ttu-id="93814-121">ولأن بدلات الإهلاك الخاص تكون غير معروفة في أغلب الأحيان حتى وقت لاحق من مدة خدمة الأصل الثابت، فمن الأفضل استخدام هذا النوع من الإهلاك مع دفتر لا يتم ترحيله إلى دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="93814-121">Because special depreciation allowances are often unknown until later in the service life of the fixed asset, it's best to use this type of depreciation with a book that doesn't post to the general ledger.</span></span> <span data-ttu-id="93814-122">يمكنك استخدام الوظيفة الدورية "حذف الحركات التي لم يتم ترحيلها إلى دفتر الأستاذ العام"‬ لحذف محفوظات الحركة لهذه الدفاتر.</span><span class="sxs-lookup"><span data-stu-id="93814-122">You can use the Delete transactions not posted to general ledger periodic function to delete the transaction history for these books.</span></span> <span data-ttu-id="93814-123">ويمكنك عندئذٍ حذف محفوظات الإهلاك الخاصة بدفتر الأصول الثابتة وترحيل بدل الإهلاك الخاص عندما يصبح معروفًا، ثم ترحيل حركات الإهلاك المتبقية للسنة.</span><span class="sxs-lookup"><span data-stu-id="93814-123">You can then delete the depreciation history for the fixed asset book, post the special depreciation allowance when it's known, and then post the remaining depreciation transactions for the year.</span></span> 

<span data-ttu-id="93814-124">يمكنك إنشاء عدد غير محدود من سجلات بدلات الإهلاك الخاص.</span><span class="sxs-lookup"><span data-stu-id="93814-124">You can create an unlimited number of special depreciation allowance records.</span></span> <span data-ttu-id="93814-125">وبعد تعيين هذه السجلات إلى دفتر مجموعة أصول، سيتم تطبيقها على دفتر الأصل.</span><span class="sxs-lookup"><span data-stu-id="93814-125">After you assign those records to an asset group book, they are applied to the asset book.</span></span> 

<span data-ttu-id="93814-126">يتم إدخال بدل الإهلاك الخاص كنسبة مئوية أو مبلغ ثابت.</span><span class="sxs-lookup"><span data-stu-id="93814-126">A special depreciation allowance is entered as either a percentage or a fixed amount.</span></span> <span data-ttu-id="93814-127">وعند ترحيل اقتراحات الإهلاك، يتم ترحيل حركات بدل الإهلاك الخاص إلى الدفتر كحركات منفصلة عن حركات الإهلاك.</span><span class="sxs-lookup"><span data-stu-id="93814-127">When you post depreciation proposals, special depreciation allowance transactions are posted to the book as transactions that are separate from the depreciation transactions.</span></span>

## <a name="depreciation-calendars"></a><span data-ttu-id="93814-128"> تقويمات الإهلاك</span><span class="sxs-lookup"><span data-stu-id="93814-128">Depreciation calendars</span></span>
<span data-ttu-id="93814-129">يحتوي كل دفتر على تقويم يتم استخدامه عند إهلاك الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="93814-129">Each book has a calendar that is used when you depreciate fixed assets.</span></span> <span data-ttu-id="93814-130">بشكل افتراضي، يستخدم الدفتر التقويم المالي لدفتر الأستاذ‬ في حال عدم الإشارة إلى تقويم على دفتر.</span><span class="sxs-lookup"><span data-stu-id="93814-130">By default, if you don't indicate a calendar on the book, the book uses the ledger fiscal calendar.</span></span> <span data-ttu-id="93814-131">يجب تحديد تقويم مالي للدفتر عندما يستخدم ملف تعريف الإهلاك المقترن بالدفتر سنة إهلاك مالية.</span><span class="sxs-lookup"><span data-stu-id="93814-131">You must select a fiscal calendar for a book when the depreciation profile that is associated with the book uses a fiscal depreciation year.</span></span> 

<span data-ttu-id="93814-132">يمكنك إنشاء التقويمات المشتركة باستخدام صفحة **التقويمات المالية** في دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="93814-132">You can create shared calendars by using the **Fiscal calendars** page in General ledger.</span></span>

<span data-ttu-id="93814-133">لمزيد من المعلومات، راجع [أساليب وقواعد الإهلاك](depreciation-methods-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="93814-133">For more information, see [Depreciation methods and conventions](depreciation-methods-conventions.md).</span></span>



