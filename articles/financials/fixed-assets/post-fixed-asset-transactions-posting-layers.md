---
title: ترحيل حركات الأصول الثابتة إلى طبقات الترحيل
description: تقدم هذه المقالة نظرة عامة حول وظيفة طبقة الترحيل لحركات الأصول الثابتة.
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 22feb15a1891c57576a5809f4ff3f4d089c6dfa4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556314"
---
# <a name="post-fixed-asset-transactions-to-posting-layers"></a><span data-ttu-id="f839c-103">ترحيل حركات الأصول الثابتة إلى طبقات الترحيل</span><span class="sxs-lookup"><span data-stu-id="f839c-103">Post fixed asset transactions to posting layers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f839c-104">تقدم هذه المقالة نظرة عامة حول وظيفة طبقة الترحيل لحركات الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="f839c-104">This article gives an overview of posting layer functionality for fixed asset transactions.</span></span>

<span data-ttu-id="f839c-105">غالبًا ما يتم إهلاك الأصول الثابتة بطرق مختلفة لأهداف متعددة.</span><span class="sxs-lookup"><span data-stu-id="f839c-105">A fixed asset is often depreciated in different ways for different purposes.</span></span> <span data-ttu-id="f839c-106">فحساب الإهلاك للأغراض الضريبية يتم باستخدام القواعد الضريبية الحالية لتحقيق أعلى إهلاك ممكن قبل الضرائب، إلا أنه يتم حساب الإهلاك بهدف إعداد التقارير وفقًا للقوانين والمعايير المحاسبية.</span><span class="sxs-lookup"><span data-stu-id="f839c-106">Depreciation for tax purposes is calculated by using current tax rules to achieve the highest possible depreciation before taxes, but depreciation for reporting purposes is calculated according to accounting laws and standards.</span></span> <span data-ttu-id="f839c-107">ويتم حساب الأنواع المتعددة للإهلاك وتسجيلها بشكل منفصل في طبقات الترحيل.</span><span class="sxs-lookup"><span data-stu-id="f839c-107">The various kinds of depreciation are calculated and recorded separately in the posting layers.</span></span>

<span data-ttu-id="f839c-108">يتم إعداد كل دفتر مرفق بأصل ثابت لطبقة ترحيل معينة ذات هدف إهلاك إجمالي.</span><span class="sxs-lookup"><span data-stu-id="f839c-108">Each book that is attached to a fixed asset is set up for a particular posting layer that has an overall depreciation objective.</span></span> <span data-ttu-id="f839c-109">هناك عشر طبقات ترحيل: الحالية والعمليات والضرائب وسبع طبقات مخصصة.</span><span class="sxs-lookup"><span data-stu-id="f839c-109">There are ten posting layers: Current, Operations, Tax, and seven Custom layers.</span></span> <span data-ttu-id="f839c-110">يمكنك أيضًا تعطيل الترحيل إلى دفتر الأستاذ العام عبر تعيين الحقل الترحيل إلى دفتر الأستاذ العام‬ إلى لا.</span><span class="sxs-lookup"><span data-stu-id="f839c-110">You can also disable posting to the general ledger for the book by setting the Post to general ledger field to No.</span></span> <span data-ttu-id="f839c-111">يتم عندئذٍ تعيين حقل طبقة الترحيل إلى بلا‬ بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="f839c-111">The Posting layer field is then automatically set to None.</span></span> <span data-ttu-id="f839c-112">تُستخدم عادة الدفاتر التي لا يتم ترحيلها إلى دفتر الأستاذ العام لأغراض إعداد التقارير الضريبية.</span><span class="sxs-lookup"><span data-stu-id="f839c-112">Typically, books that don’t post to the general ledger are used for tax reporting purposes.</span></span> <span data-ttu-id="f839c-113">يمنحك هذا النهج مرونة إضافية لحذف الحركات السابقة الخاصة بدفتر الأصول نظرًا لعدم ربطها بدفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="f839c-113">This approach gives you the additional flexibility to delete historical transactions for the asset book, because they haven’t been committed to the general ledger.</span></span>

<span data-ttu-id="f839c-114">يتم تعريف دفاتر يومية الأصول الثابتة التي باستخدام صفحة أسماء دفاتر اليومية في دفتر الأستاذ العام > إعداد دفتر اليومية > أسماء دفاتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="f839c-114">Fixed asset journals are defined by using the Journal names page at General ledger > Journal setup > Journal names.</span></span> <span data-ttu-id="f839c-115">ويتم تعريف كل دفتر يومية يمكنك ترحيل الإهلاك فيه حسب اسم دفتر يوميته لطبقة ترحيل واحدة فقط.</span><span class="sxs-lookup"><span data-stu-id="f839c-115">Each journal that you can post depreciations in is defined by its journal name for only one posting layer.</span></span> <span data-ttu-id="f839c-116">لا يمكن تغيير طبقة الترحيل في دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="f839c-116">The posting layer in the journal can’t be changed.</span></span> <span data-ttu-id="f839c-117">من شأن هذا القيد أن يساعد على ضمان إبقاء الحركات الخاصة بكل طبقة ترحيل منفصلة عن الأخرى.</span><span class="sxs-lookup"><span data-stu-id="f839c-117">This restriction helps guarantee that transactions for each posting layer are kept separate.</span></span> <span data-ttu-id="f839c-118">وينبغي إنشاء اسم دفتر يومية واحد على الأقل لكل طبقة ترحيل.</span><span class="sxs-lookup"><span data-stu-id="f839c-118">At least one journal name must be created for each posting layer.</span></span> <span data-ttu-id="f839c-119">إذا كنت تستخدم دفاتر لا يتم ترحيلها إلى دفتر الأستاذ العام، فيجب أيضًا إنشاء دفتر يومية حيث تم تعيين طبقة الترحيل إلى بلا.</span><span class="sxs-lookup"><span data-stu-id="f839c-119">If you’re using books that don’t post to the general ledger, you must also create a journal where the posting layer is set to None.</span></span>

<span data-ttu-id="f839c-120">يمكنك تعيين حسابات دفتر الأستاذ لحركات الأصول الثابتة في صفحة ملفات تعريف دفتر الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="f839c-120">You can designate ledger accounts for fixed asset transactions on the Fixed asset posting profiles page.</span></span> <span data-ttu-id="f839c-121">لكل ملف تعريف ترحيل، يجب تحديد نوع المعاملة والكتاب ذي الصلة، ثم تعيين حسابات دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="f839c-121">For each posting profile, you must select the relevant transaction type and book, and then designate the ledger accounts.</span></span> <span data-ttu-id="f839c-122">قم بإعداد سجل ملف تعريف ترحيل لكل دفتر سيتم ترحيله إلى دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="f839c-122">Set up a posting profile record for each book that will post to the general ledger.</span></span>

> [!NOTE] 
> <span data-ttu-id="f839c-123">باستخدام الدفاتر المشتقة، يمكنك ترحيل الحركات إلى طبقات ترحيل مختلفة في نفس الوقت.</span><span class="sxs-lookup"><span data-stu-id="f839c-123">By using derived books, you can post transactions to different posting layers at the same time.</span></span> <span data-ttu-id="f839c-124">ستقوم بإنشاء حركات للدفتر الأساسي في دفتر يومية حيث تتطابق طبقة الترحيل مع طبقة ترحيل الدفتر.</span><span class="sxs-lookup"><span data-stu-id="f839c-124">You create the transactions of the primary book in a journal where the posting layer corresponds to the book posting layer.</span></span> <span data-ttu-id="f839c-125">وأثناء إجراء الترحيل، سيتم ترحيل حركات الدفاتر المشتقة إلى طبقات الترحيل المناسبة.</span><span class="sxs-lookup"><span data-stu-id="f839c-125">During posting, the derived book transactions are posted to the appropriate posting layers.</span></span>

<span data-ttu-id="f839c-126">لمزيد من المعلومات، راجع [الدفاتر المشتقة](derived-books.md) و[الترحيل باستخدام الدفاتر المشتقة](post-derived-value-models.md).</span><span class="sxs-lookup"><span data-stu-id="f839c-126">For more information see, [Derived books](derived-books.md) and [Posting with derived books](post-derived-value-models.md).</span></span>



