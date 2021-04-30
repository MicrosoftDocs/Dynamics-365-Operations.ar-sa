---
title: عدد الدفاتر لكل دفتر يومية
description: يصف هذا الموضوع العلاقة بين دفاتر اليومية ودفاتر الأصول عند إنشاء امتلاك أصل ثابت أو مقترح إهلاك من خلال وظيفة الدُفعة. يمكنك تحديد الحد الأقصى لعدد الدفاتر المضمنة لكل استحواذ وإهلاك.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-19
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: fb2a25d9e2ffc26f0a37a09cdf3e28a7ca4b84bc
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892397"
---
# <a name="number-of-books-per-journal"></a><span data-ttu-id="6e264-104">عدد الدفاتر لكل دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="6e264-104">Number of books per journal</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e264-105">يصف هذا الموضوع العلاقة بين دفاتر اليومية ودفاتر الأصول عند إنشاء امتلاك أصل ثابت أو مقترح إهلاك من خلال وظيفة الدُفعة.</span><span class="sxs-lookup"><span data-stu-id="6e264-105">This topic describes the relationship between journals and asset books when you create a fixed asset acquisition or depreciation proposal through a batch job.</span></span> <span data-ttu-id="6e264-106">يمكنك تحديد الحد الأقصى لعدد الدفاتر المضمنة لكل استحواذ وإهلاك باستخدام الحقول الموجودة في القسم **عدد الدفاتر لكل دفتر يومية** في علامة التبويب **عام** في الصفحة **معلمات الأصول الثابتة** (**الأصول الثابتة \> الإعداد \> معلمات الأصول الثابتة**).</span><span class="sxs-lookup"><span data-stu-id="6e264-106">You can define the maximum number of books that are included for each acquisition and for depreciation by using the fields in the **Number of books per journal** section on the **General** tab of the **Fixed assets parameters** page (**Fixed assets \> Setup \> Fixed assets parameters**).</span></span> <span data-ttu-id="6e264-107">تتيح لك هذه الحقول توزيع عدد دفاتر الأصول لكل دفتر يومية استحواذ ودفتر يومية إهلاك.</span><span class="sxs-lookup"><span data-stu-id="6e264-107">These fields let you distribute the number of asset books per acquisition journal and depreciation journal.</span></span>

<span data-ttu-id="6e264-108">بالنسبة لمقترح الاستحواذ، تكون القيمة الافتراضية عبارة عن دفاتر 10.000 على الأقل.</span><span class="sxs-lookup"><span data-stu-id="6e264-108">For an acquisition proposal, the default value is at least 10,000 books.</span></span> <span data-ttu-id="6e264-109">بالنسبة لمقترح الإهلاك، تكون القيمة الافتراضية عبارة عن دفاتر 2.000 على الأقل.</span><span class="sxs-lookup"><span data-stu-id="6e264-109">For a depreciation proposal, the default value is at least 2,000 books.</span></span>

<span data-ttu-id="6e264-110">على سبيل المثال، في حالة وجود 4.000 من الأصول الثابتة، واقتران دفترين بكل أصل، فانه يتم ترحيل دفتر واحد إلى الطبقة الحالية، ويتم ترحيل الدفتر الآخر إلى طبقة الضريبة.</span><span class="sxs-lookup"><span data-stu-id="6e264-110">For example, if there are 4,000 fixed assets, and two books are associated with each asset, one book will be posted to the current layer, and the other book will be posted to the tax layer.</span></span> <span data-ttu-id="6e264-111">إذا اكتسبت 4.000 من الأصول الثابتة من خلال معالجة الدُفعة، فسوف تحتوي وظيفة الدُفعة التي تقوم بإنشاء دفتر يومية استحواذ الأصل ثابت واحد على دفاتر أصول 4.000.</span><span class="sxs-lookup"><span data-stu-id="6e264-111">If you acquire 4,000 fixed assets through batch processing, the batch job that creates one fixed asset acquisition journal will contain 4,000 asset books.</span></span>

> [!NOTE]
> <span data-ttu-id="6e264-112">سيستمر استخدام دفتر اليومية الذي تم إنشاؤه حتى تكتمل وظيفة الدُفعة.</span><span class="sxs-lookup"><span data-stu-id="6e264-112">The journal that is created will continue to be used until the batch job is completed.</span></span>
>
> <span data-ttu-id="6e264-113">لا يتم تضمين الدفاتر المشتقة في الحد الأقصى لعدد الدفاتر لكل دفتر يومية.</span><span class="sxs-lookup"><span data-stu-id="6e264-113">The derived books aren't included in the maximum number of books per journal.</span></span>

<span data-ttu-id="6e264-114">يمكنك استخدام معالجة الدُفعة لتشغيل الإهلاك لنفس مجموعة الأصول المكتسبة.</span><span class="sxs-lookup"><span data-stu-id="6e264-114">You can use  batch processing to run depreciation for the same set of acquired assets.</span></span> <span data-ttu-id="6e264-115">على سبيل المثال، تقوم وظيفة الدُفعة بإنشاء دفتري يومية إهلاك، يتكون كل منها من دفاتر أصول عددها 2.000.</span><span class="sxs-lookup"><span data-stu-id="6e264-115">For example, a batch job creates two depreciation journals, each of which consists of 2,000 asset books.</span></span> <span data-ttu-id="6e264-116">سيحتوي دفتر اليومية الأول على الدفاتر المقترنة بالأصول الثابتة التي يتم ترقيمها من 1 إلى 2.000.</span><span class="sxs-lookup"><span data-stu-id="6e264-116">The first journal will contain books that are associated with the fixed assets that are numbered 1 through 2,000.</span></span> <span data-ttu-id="6e264-117">ثم سيحتوي دفتر اليومية الثاني على الدفاتر المقترنة بالأصول الثابتة التي يتم ترقيمها من 2.001 إلى 4.000.</span><span class="sxs-lookup"><span data-stu-id="6e264-117">The second journal will then contain books that are associated with the fixed assets that are numbered 2,001 through 4,000.</span></span>

<span data-ttu-id="6e264-118">تستثني وظيفة معالجة الدُفعة الدفاتر المغلقة.</span><span class="sxs-lookup"><span data-stu-id="6e264-118">The batch processing job excludes closed books.</span></span> <span data-ttu-id="6e264-119">على سبيل المثال، في وظيفة الدُفعة للإهلاك، يتم إغلاق 10 دفاتر الأولى من الدفاتر التي يبلغ عددها 2.000.</span><span class="sxs-lookup"><span data-stu-id="6e264-119">For example, in a batch job for depreciation, 10 of the first 2,000 books are closed.</span></span> <span data-ttu-id="6e264-120">في هذه الحالة، سيحتوي دفتر اليومية الأول على الدفاتر المقترنة بالأصول الثابتة التي يتم ترقيمها من 1 إلى 2.011.</span><span class="sxs-lookup"><span data-stu-id="6e264-120">In this case, the first journal will contain books that are associated with the fixed assets that are numbered 1 through 2,011.</span></span> <span data-ttu-id="6e264-121">ثم سيحتوي دفتر اليومية الثاني على الدفاتر المقترنة بالأصول الثابتة التي يتم ترقيمها من 2.012 إلى 4.000.</span><span class="sxs-lookup"><span data-stu-id="6e264-121">The second journal will then contain books that are associated with the fixed assets that are numbered 2,012 through 4,000.</span></span>

> [!NOTE]
> <span data-ttu-id="6e264-122">إذا كان لديك معرفات أصول ثابتة بفواصل مختلفة (مثل - أو /)، وقمت بإنشاء حركات الأصول الثابتة في وظائف الدُفعات، فيجب تشغيل وظيفة دُفعية منفصلة لكل نوع من الفواصل.</span><span class="sxs-lookup"><span data-stu-id="6e264-122">If you have fixed asset IDs with different separators (such as – or /), and you create fixed asset transactions in batch jobs, you must run a separate batch job for each type of separator.</span></span> <span data-ttu-id="6e264-123">لا يمكن للنظام معالجة فواصل مختلفة في نفس الوظيفة الدفعية.</span><span class="sxs-lookup"><span data-stu-id="6e264-123">The system can't process different separators within the same batch job.</span></span>

<span data-ttu-id="6e264-124">يتم تطبيق الحد الأقصى لعدد الدفاتر إذا كانت معرفات الأصول المكررة غير موجودة في نفس دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="6e264-124">The limit on the number of books is applied if duplicate asset IDs don't exist in the same journal.</span></span> <span data-ttu-id="6e264-125">ومع ذلك، إذا كان معرف الأصل هو نفس معرف الدفتر، فإنه يمكن تجاوز عدد الدفاتر لكل دفتر يومية للاحتفاظ بمعرف الأصل في نفس دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="6e264-125">However, if the asset ID is the same as the book ID, the number of books per journal can be exceeded to keep the asset ID in the same journal.</span></span>

<span data-ttu-id="6e264-126">على سبيل المثال، هناك 5.001 معرفًا من معرفات الأصول الثابتة، ويتم إقران ثلاثة دفاتر بكل معرف أصل ثابت، ويتم ترحيل كل دفتر أصول إلى طبقة الترحيل نفسها.</span><span class="sxs-lookup"><span data-stu-id="6e264-126">For example, there are 5,001 fixed asset IDs, three books are associated with each fixed asset ID, and each asset book is posted to the same posting layer.</span></span> <span data-ttu-id="6e264-127">يمكنك تشغيل إهلاك لمدة ثلاثة أشهر متتالية، دون التلخيص.</span><span class="sxs-lookup"><span data-stu-id="6e264-127">You run depreciation for three consecutive months, without summarizing.</span></span>  <span data-ttu-id="6e264-128">سيتم إنشاء دفتر يومية الإهلاك من خلال وظيفة الدُفعة، وسيقوم النظام بإنشاء سبعة دفاتر يومية تحتوي على عدد 667 معرفًا من معرفات الأصول الثابتة وثلاثة دفاتر لكل معرف أصل ثابت.</span><span class="sxs-lookup"><span data-stu-id="6e264-128">The depreciation journal will be created through a batch job, and the system will create seven journals that have 667 fixed asset IDs and three books for each fixed asset ID.</span></span> <span data-ttu-id="6e264-129">ستكون النتيجة 2.001 دفترًا.</span><span class="sxs-lookup"><span data-stu-id="6e264-129">The result will be 2,001 books.</span></span> <span data-ttu-id="6e264-130">وبالتالي، في ثلاثة أشهر، سيكون هناك 6.003 بندًا لدفتر اليومية للاحتفاظ بنفس معرفات الأصول في نفس دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="6e264-130">Therefore, in three months, there will be 6,003 journal lines to maintain the same asset IDs in the same journal.</span></span> <span data-ttu-id="6e264-131">سيقوم النظام أيضًا بإنشاء دفتر يومية واحد يحتوي على 332 معرفً من معرفات الأصول الثابتة وثلاثة دفاتر لكل معرف أصل ثابت.</span><span class="sxs-lookup"><span data-stu-id="6e264-131">The system will also create one journal that has 332 fixed asset IDs and three books for each fixed asset ID.</span></span> <span data-ttu-id="6e264-132">في ثلاثة أشهر، سيكون هناك 2.988 سطرًا.</span><span class="sxs-lookup"><span data-stu-id="6e264-132">In three months, there will be 2,988 lines.</span></span>

> [!NOTE] 
> <span data-ttu-id="6e264-133">في حالة تشغيل معلمة **تلخيص الإهلاك** عند إنشاء مقترح إهلاك، فلن يكون للقيمة الموجودة في حقل **عدد الدفاتر لكل دفتر يومية -اقتراح الإهلاك** أي تاثير.</span><span class="sxs-lookup"><span data-stu-id="6e264-133">If the **Summarize depreciation** parameter is turned on when you're creating a depreciation proposal, then the value in the **Number of books per journal - Depreciation proposal** field has no effect.</span></span> <span data-ttu-id="6e264-134">في هذه الحالة، يكون عدد الدفاتر لكل دفتر يومية هو 6000، وهو الحد الداخلي المحدد.</span><span class="sxs-lookup"><span data-stu-id="6e264-134">In this case number of books per journal is 6000, which is the internal defined limit.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
