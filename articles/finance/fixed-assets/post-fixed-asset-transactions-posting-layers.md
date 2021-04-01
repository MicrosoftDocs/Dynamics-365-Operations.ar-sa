---
title: ترحيل حركات الأصول الثابتة إلى طبقات الترحيل
description: تقدم هذه المقالة نظرة عامة حول وظيفة طبقة الترحيل لحركات الأصول الثابتة.
author: moaamer
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9a52374d52b3dcd435c79033d462a2982316a68b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240848"
---
# <a name="post-fixed-asset-transactions-to-posting-layers"></a><span data-ttu-id="6dd1a-103">ترحيل حركات الأصول الثابتة إلى طبقات الترحيل</span><span class="sxs-lookup"><span data-stu-id="6dd1a-103">Post fixed asset transactions to posting layers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6dd1a-104">تقدم هذه المقالة نظرة عامة حول وظيفة طبقة الترحيل لحركات الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="6dd1a-104">This article gives an overview of posting layer functionality for fixed asset transactions.</span></span>

<span data-ttu-id="6dd1a-105">غالبًا ما يتم إهلاك الأصول الثابتة بطرق مختلفة لأهداف متعددة.</span><span class="sxs-lookup"><span data-stu-id="6dd1a-105">A fixed asset is often depreciated in different ways for different purposes.</span></span> <span data-ttu-id="6dd1a-106">فحساب الإهلاك للأغراض الضريبية يتم باستخدام القواعد الضريبية الحالية لتحقيق أعلى إهلاك ممكن قبل الضرائب، إلا أنه يتم حساب الإهلاك بهدف إعداد التقارير وفقًا للقوانين والمعايير المحاسبية.</span><span class="sxs-lookup"><span data-stu-id="6dd1a-106">Depreciation for tax purposes is calculated by using current tax rules to achieve the highest possible depreciation before taxes, but depreciation for reporting purposes is calculated according to accounting laws and standards.</span></span> <span data-ttu-id="6dd1a-107">ويتم حساب الأنواع المتعددة للإهلاك وتسجيلها بشكل منفصل في طبقات الترحيل.</span><span class="sxs-lookup"><span data-stu-id="6dd1a-107">The various kinds of depreciation are calculated and recorded separately in the posting layers.</span></span>

<span data-ttu-id="6dd1a-108">يتم إعداد كل دفتر مرفق بأصل ثابت لطبقة ترحيل معينة ذات هدف إهلاك إجمالي.</span><span class="sxs-lookup"><span data-stu-id="6dd1a-108">Each book that is attached to a fixed asset is set up for a particular posting layer that has an overall depreciation objective.</span></span> <span data-ttu-id="6dd1a-109">هناك عشر طبقات ترحيل: الحالية والعمليات والضرائب وسبع طبقات مخصصة.</span><span class="sxs-lookup"><span data-stu-id="6dd1a-109">There are ten posting layers: Current, Operations, Tax, and seven Custom layers.</span></span> <span data-ttu-id="6dd1a-110">يمكنك أيضًا تعطيل الترحيل إلى دفتر الأستاذ العام عبر تعيين الحقل الترحيل إلى دفتر الأستاذ العام‬ إلى لا.</span><span class="sxs-lookup"><span data-stu-id="6dd1a-110">You can also disable posting to the general ledger for the book by setting the Post to general ledger field to No.</span></span> <span data-ttu-id="6dd1a-111">يتم عندئذٍ تعيين حقل طبقة الترحيل إلى بلا‬ بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="6dd1a-111">The Posting layer field is then automatically set to None.</span></span> <span data-ttu-id="6dd1a-112">تُستخدم عادة الدفاتر التي لا يتم ترحيلها إلى دفتر الأستاذ العام لأغراض إعداد التقارير الضريبية.</span><span class="sxs-lookup"><span data-stu-id="6dd1a-112">Typically, books that don’t post to the general ledger are used for tax reporting purposes.</span></span> <span data-ttu-id="6dd1a-113">يمنحك هذا النهج مرونة إضافية لحذف الحركات السابقة الخاصة بدفتر الأصول نظرًا لعدم ربطها بدفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="6dd1a-113">This approach gives you the additional flexibility to delete historical transactions for the asset book, because they haven’t been committed to the general ledger.</span></span>

<span data-ttu-id="6dd1a-114">يتم تعريف دفاتر يومية الأصول الثابتة التي باستخدام صفحة أسماء دفاتر اليومية في دفتر الأستاذ العام > إعداد دفتر اليومية > أسماء دفاتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="6dd1a-114">Fixed asset journals are defined by using the Journal names page at General ledger > Journal setup > Journal names.</span></span> <span data-ttu-id="6dd1a-115">ويتم تعريف كل دفتر يومية يمكنك ترحيل الإهلاك فيه حسب اسم دفتر يوميته لطبقة ترحيل واحدة فقط.</span><span class="sxs-lookup"><span data-stu-id="6dd1a-115">Each journal that you can post depreciations in is defined by its journal name for only one posting layer.</span></span> <span data-ttu-id="6dd1a-116">لا يمكن تغيير طبقة الترحيل في دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="6dd1a-116">The posting layer in the journal can’t be changed.</span></span> <span data-ttu-id="6dd1a-117">من شأن هذا القيد أن يساعد على ضمان إبقاء الحركات الخاصة بكل طبقة ترحيل منفصلة عن الأخرى.</span><span class="sxs-lookup"><span data-stu-id="6dd1a-117">This restriction helps guarantee that transactions for each posting layer are kept separate.</span></span> <span data-ttu-id="6dd1a-118">وينبغي إنشاء اسم دفتر يومية واحد على الأقل لكل طبقة ترحيل.</span><span class="sxs-lookup"><span data-stu-id="6dd1a-118">At least one journal name must be created for each posting layer.</span></span> <span data-ttu-id="6dd1a-119">إذا كنت تستخدم دفاتر لا يتم ترحيلها إلى دفتر الأستاذ العام، فيجب أيضًا إنشاء دفتر يومية حيث تم تعيين طبقة الترحيل إلى بلا.</span><span class="sxs-lookup"><span data-stu-id="6dd1a-119">If you’re using books that don’t post to the general ledger, you must also create a journal where the posting layer is set to None.</span></span>

<span data-ttu-id="6dd1a-120">يمكنك تعيين حسابات دفتر الأستاذ لحركات الأصول الثابتة في صفحة ملفات تعريف دفتر الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="6dd1a-120">You can designate ledger accounts for fixed asset transactions on the Fixed asset posting profiles page.</span></span> <span data-ttu-id="6dd1a-121">لكل ملف تعريف ترحيل، يجب تحديد نوع المعاملة والكتاب ذي الصلة، ثم تعيين حسابات دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="6dd1a-121">For each posting profile, you must select the relevant transaction type and book, and then designate the ledger accounts.</span></span> <span data-ttu-id="6dd1a-122">قم بإعداد سجل ملف تعريف ترحيل لكل دفتر سيتم ترحيله إلى دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="6dd1a-122">Set up a posting profile record for each book that will post to the general ledger.</span></span>

<span data-ttu-id="6dd1a-123">يمكن إدخال الأصل الثابت في المستندات التي تدعم فقط طبقة الترحيل **الحالية**، مثل **أمر الشراء** أو **فاتورة المورد المعلقة** أو **أمر المبيعات** أو **فاتورة النص الحر**.</span><span class="sxs-lookup"><span data-stu-id="6dd1a-123">The fixed asset can be entered in documents that only support the **Current** posting layer, like **Purchase order**, **Pending vendor invoice**, **Sales order**, or **Free text invoice**.</span></span> <span data-ttu-id="6dd1a-124">أثناء تحديد معرف أصل ثابت في أي من هذه المستندات، تتم تصفية دفتر الأصول إلى الدفتر بطبقة الترحيل **الحالية**، وسيتم ملؤه تلقائيًا، أثناء الترحيل عندما يتحقق النظام من أن طبقة ترحيل الأصل الثابت هي **الحالية**.</span><span class="sxs-lookup"><span data-stu-id="6dd1a-124">While selecting a fixed asset ID in any of those documents the asset book is filtered to the book with **Current** posting layer, and will be filled in automatically, during posting when the system validates that the fixed asset posting layer is **Current**.</span></span> <span data-ttu-id="6dd1a-125">إذا لم يتم إكمال التحقق من الصحة، فإنه سيتم إيقاف عملية الترحيل.</span><span class="sxs-lookup"><span data-stu-id="6dd1a-125">If that validation can't be completed, the posting process will be stopped.</span></span> 

> [!NOTE] 
> <span data-ttu-id="6dd1a-126">باستخدام الدفاتر المشتقة، يمكنك ترحيل الحركات إلى طبقات ترحيل مختلفة في نفس الوقت.</span><span class="sxs-lookup"><span data-stu-id="6dd1a-126">By using derived books, you can post transactions to different posting layers at the same time.</span></span> <span data-ttu-id="6dd1a-127">يتم إنشاء حركات الدفتر الأساسي في دفتر يومية أو مستند مصدر حيث تتطابق طبقة الترحيل مع طبقة ترحيل الدفتر.</span><span class="sxs-lookup"><span data-stu-id="6dd1a-127">The transactions of the primary book are created in a journal or source document where the posting layer corresponds to the book posting layer.</span></span> <span data-ttu-id="6dd1a-128">وأثناء إجراء الترحيل، سيتم ترحيل حركات الدفاتر المشتقة إلى طبقات الترحيل المناسبة.</span><span class="sxs-lookup"><span data-stu-id="6dd1a-128">During posting, the derived book transactions will be posted to the appropriate posting layers.</span></span> 


<span data-ttu-id="6dd1a-129">لمزيد من المعلومات، راجع [الدفاتر المشتقة](derived-books.md) و[الترحيل باستخدام الدفاتر المشتقة](post-derived-value-models.md).</span><span class="sxs-lookup"><span data-stu-id="6dd1a-129">For more information see, [Derived books](derived-books.md) and [Post with derived books](post-derived-value-models.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]