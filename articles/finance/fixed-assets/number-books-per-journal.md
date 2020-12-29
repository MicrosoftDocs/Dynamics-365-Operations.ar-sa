---
title: عدد الدفاتر لكل دفتر يومية
description: يصف هذا الموضوع العلاقة بين دفاتر اليومية ودفاتر الأصول عند إنشاء امتلاك أصل ثابت أو مقترح إهلاك من خلال وظيفة الدُفعة. يمكنك تحديد الحد الأقصى لعدد الدفاتر المضمنة لكل استحواذ وإهلاك.
author: moaamer
manager: Ann Beebe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-19
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d4ba98cefdc0b555eedfaa56b6a3ca4870b5de93
ms.sourcegitcommit: 65f9e2584c0530b1a71655aae09101691726b47f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/01/2020
ms.locfileid: "4650644"
---
# <a name="number-of-books-per-journal"></a><span data-ttu-id="1db46-104">عدد الدفاتر لكل دفتر يومية</span><span class="sxs-lookup"><span data-stu-id="1db46-104">Number of books per journal</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1db46-105">يصف هذا الموضوع العلاقة بين دفاتر اليومية ودفاتر الأصول عند إنشاء امتلاك أصل ثابت أو مقترح إهلاك من خلال وظيفة الدُفعة.</span><span class="sxs-lookup"><span data-stu-id="1db46-105">This topic describes the relationship between journals and asset books when you create a fixed asset acquisition or depreciation proposal through a batch job.</span></span> <span data-ttu-id="1db46-106">يمكنك تحديد الحد الأقصى لعدد الدفاتر المضمنة لكل استحواذ وإهلاك باستخدام الحقول الموجودة في القسم **عدد الدفاتر لكل دفتر يومية** في علامة التبويب **عام** في الصفحة **معلمات الأصول الثابتة** (**الأصول الثابتة \> الإعداد \> معلمات الأصول الثابتة**).</span><span class="sxs-lookup"><span data-stu-id="1db46-106">You can define the maximum number of books that are included for each acquisition and for depreciation by using the fields in the **Number of books per journal** section on the **General** tab of the **Fixed assets parameters** page (**Fixed assets \> Setup \> Fixed assets parameters**).</span></span> <span data-ttu-id="1db46-107">تتيح لك هذه الحقول توزيع عدد دفاتر الأصول لكل دفتر يومية استحواذ ودفتر يومية إهلاك.</span><span class="sxs-lookup"><span data-stu-id="1db46-107">These fields let you distribute the number of asset books per acquisition journal and depreciation journal.</span></span>

<span data-ttu-id="1db46-108">بالنسبة لمقترح الاستحواذ، تكون القيمة الافتراضية عبارة عن دفاتر 10.000 على الأقل.</span><span class="sxs-lookup"><span data-stu-id="1db46-108">For an acquisition proposal, the default value is at least 10,000 books.</span></span> <span data-ttu-id="1db46-109">بالنسبة لمقترح الإهلاك، تكون القيمة الافتراضية عبارة عن دفاتر 2.000 على الأقل.</span><span class="sxs-lookup"><span data-stu-id="1db46-109">For a depreciation proposal, the default value is at least 2,000 books.</span></span>

<span data-ttu-id="1db46-110">على سبيل المثال، في حالة وجود 4.000 من الأصول الثابتة، واقتران دفترين بكل أصل، فانه يتم ترحيل دفتر واحد إلى الطبقة الحالية، ويتم ترحيل الدفتر الآخر إلى طبقة الضريبة.</span><span class="sxs-lookup"><span data-stu-id="1db46-110">For example, if there are 4,000 fixed assets, and two books are associated with each asset, one book will be posted to the current layer, and the other book will be posted to the tax layer.</span></span> <span data-ttu-id="1db46-111">إذا اكتسبت 4.000 من الأصول الثابتة من خلال معالجة الدُفعة، فسوف تحتوي وظيفة الدُفعة التي تقوم بإنشاء دفتر يومية استحواذ الأصل ثابت واحد على دفاتر أصول 4.000.</span><span class="sxs-lookup"><span data-stu-id="1db46-111">If you acquire 4,000 fixed assets through batch processing, the batch job that creates one fixed asset acquisition journal will contain 4,000 asset books.</span></span>

> [!NOTE]
> <span data-ttu-id="1db46-112">سيستمر استخدام دفتر اليومية الذي تم إنشاؤه حتى تكتمل وظيفة الدُفعة.</span><span class="sxs-lookup"><span data-stu-id="1db46-112">The journal that is created will continue to be used until the batch job is completed.</span></span>
>
> <span data-ttu-id="1db46-113">لا يتم تضمين الدفاتر المشتقة في الحد الأقصى لعدد الدفاتر لكل دفتر يومية.</span><span class="sxs-lookup"><span data-stu-id="1db46-113">The derived books aren't included in the maximum number of books per journal.</span></span>

<span data-ttu-id="1db46-114">يمكنك استخدام معالجة الدُفعة لتشغيل الإهلاك لنفس مجموعة الأصول المكتسبة.</span><span class="sxs-lookup"><span data-stu-id="1db46-114">You can use  batch processing to run depreciation for the same set of acquired assets.</span></span> <span data-ttu-id="1db46-115">على سبيل المثال، تقوم وظيفة الدُفعة بإنشاء دفتري يومية إهلاك، يتكون كل منها من دفاتر أصول عددها 2.000.</span><span class="sxs-lookup"><span data-stu-id="1db46-115">For example, a batch job creates two depreciation journals, each of which consists of 2,000 asset books.</span></span> <span data-ttu-id="1db46-116">سيحتوي دفتر اليومية الأول على الدفاتر المقترنة بالأصول الثابتة التي يتم ترقيمها من 1 إلى 2.000.</span><span class="sxs-lookup"><span data-stu-id="1db46-116">The first journal will contain books that are associated with the fixed assets that are numbered 1 through 2,000.</span></span> <span data-ttu-id="1db46-117">ثم سيحتوي دفتر اليومية الثاني على الدفاتر المقترنة بالأصول الثابتة التي يتم ترقيمها من 2.001 إلى 4.000.</span><span class="sxs-lookup"><span data-stu-id="1db46-117">The second journal will then contain books that are associated with the fixed assets that are numbered 2,001 through 4,000.</span></span>

<span data-ttu-id="1db46-118">تستثني وظيفة معالجة الدُفعة الدفاتر المغلقة.</span><span class="sxs-lookup"><span data-stu-id="1db46-118">The batch processing job excludes closed books.</span></span> <span data-ttu-id="1db46-119">على سبيل المثال، في وظيفة الدُفعة للإهلاك، يتم إغلاق 10 دفاتر الأولى من الدفاتر التي يبلغ عددها 2.000.</span><span class="sxs-lookup"><span data-stu-id="1db46-119">For example, in a batch job for depreciation, 10 of the first 2,000 books are closed.</span></span> <span data-ttu-id="1db46-120">في هذه الحالة، سيحتوي دفتر اليومية الأول على الدفاتر المقترنة بالأصول الثابتة التي يتم ترقيمها من 1 إلى 2.011.</span><span class="sxs-lookup"><span data-stu-id="1db46-120">In this case, the first journal will contain books that are associated with the fixed assets that are numbered 1 through 2,011.</span></span> <span data-ttu-id="1db46-121">ثم سيحتوي دفتر اليومية الثاني على الدفاتر المقترنة بالأصول الثابتة التي يتم ترقيمها من 2.012 إلى 4.000.</span><span class="sxs-lookup"><span data-stu-id="1db46-121">The second journal will then contain books that are associated with the fixed assets that are numbered 2,012 through 4,000.</span></span>

<span data-ttu-id="1db46-122">يتم تطبيق الحد الأقصى لعدد الدفاتر إذا كانت معرفات الأصول المكررة غير موجودة في نفس دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="1db46-122">The limit on the number of books is applied if duplicate asset IDs don't exist in the same journal.</span></span> <span data-ttu-id="1db46-123">ومع ذلك، إذا كان معرف الأصل هو نفس معرف الدفتر، فإنه يمكن تجاوز عدد الدفاتر لكل دفتر يومية للاحتفاظ بمعرف الأصل في نفس دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="1db46-123">However, if the asset ID is the same as the book ID, the number of books per journal can be exceeded to keep the asset ID in the same journal.</span></span>

<span data-ttu-id="1db46-124">على سبيل المثال، هناك 5.001 معرفًا من معرفات الأصول الثابتة، ويتم إقران ثلاثة دفاتر بكل معرف أصل ثابت، ويتم ترحيل كل دفتر أصول إلى طبقة الترحيل نفسها.</span><span class="sxs-lookup"><span data-stu-id="1db46-124">For example, there are 5,001 fixed asset IDs, three books are associated with each fixed asset ID, and each asset book is posted to the same posting layer.</span></span> <span data-ttu-id="1db46-125">يمكنك تشغيل إهلاك لمدة ثلاثة أشهر متتالية، دون التلخيص.</span><span class="sxs-lookup"><span data-stu-id="1db46-125">You run depreciation for three consecutive months, without summarization.</span></span> <span data-ttu-id="1db46-126">سيتم إنشاء دفتر يومية الإهلاك من خلال وظيفة الدُفعة، وسيقوم النظام بإنشاء سبعة دفاتر يومية تحتوي على عدد 667 معرفًا من معرفات الأصول الثابتة وثلاثة دفاتر لكل معرف أصل ثابت.</span><span class="sxs-lookup"><span data-stu-id="1db46-126">The depreciation journal will be created through a batch job, and the system will create seven journals that have 667 fixed asset IDs and three books for each fixed asset ID.</span></span> <span data-ttu-id="1db46-127">ستكون النتيجة 2.001 دفترًا.</span><span class="sxs-lookup"><span data-stu-id="1db46-127">The result will be 2,001 books.</span></span> <span data-ttu-id="1db46-128">وبالتالي، في ثلاثة أشهر، سيكون هناك 6.003 بندًا لدفتر اليومية للاحتفاظ بنفس معرفات الأصول في نفس دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="1db46-128">Therefore, in three months, there will be 6,003 journal lines to maintain the same asset IDs in the same journal.</span></span> <span data-ttu-id="1db46-129">سيقوم النظام أيضًا بإنشاء دفتر يومية واحد يحتوي على 332 معرفً من معرفات الأصول الثابتة وثلاثة دفاتر لكل معرف أصل ثابت.</span><span class="sxs-lookup"><span data-stu-id="1db46-129">The system will also create one journal that has 332 fixed asset IDs and three books for each fixed asset ID.</span></span> <span data-ttu-id="1db46-130">في ثلاثة أشهر، سيكون هناك 2.988 سطرًا.</span><span class="sxs-lookup"><span data-stu-id="1db46-130">In three months, there will be 2,988 lines.</span></span>
