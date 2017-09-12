---
title: "تعريفات الترحيل"
description: "توفر هذه المقالة معلومات حول تعريفات الترحيل وكيفية تعريفها وربطها. للحصول على مستندات وأنواع الترحيل المدعومة، يمكنك استخدام ملفات تعريف الترحيل بدلاً من ملفات تعريف الترحيل لتصنيف الحسابات الرئيسية والأبعاد المالية في الإدخالات المحاسبية."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans, LedgerParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15741
ms.assetid: 1495e7e0-2e39-464c-8da9-f55b1ca1c6bb
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 9c49e4abe28078f62f46b4eea4e22a268339b569
ms.contentlocale: ar-sa
ms.lasthandoff: 06/29/2017


---

# <a name="posting-definitions"></a><span data-ttu-id="f640a-104">تعريفات الترحيل</span><span class="sxs-lookup"><span data-stu-id="f640a-104">Posting definitions</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f640a-105">توفر هذه المقالة معلومات حول تعريفات الترحيل وكيفية تعريفها وربطها.</span><span class="sxs-lookup"><span data-stu-id="f640a-105">This article provides information about posting definitions, and how to define and link them.</span></span> <span data-ttu-id="f640a-106">للحصول على مستندات وأنواع الترحيل المدعومة، يمكنك استخدام ملفات تعريف الترحيل بدلاً من ملفات تعريف الترحيل لتصنيف الحسابات الرئيسية والأبعاد المالية في الإدخالات المحاسبية.</span><span class="sxs-lookup"><span data-stu-id="f640a-106">For supported posting types and documents, you can use posting definitions instead of posting profiles to classify main accounts and financial dimensions on accounting entries.</span></span>

<span data-ttu-id="f640a-107">للحصول على مستندات وأنواع الترحيل المدعومة، يمكنك استخدام ملفات تعريف الترحيل بدلاً من ملفات تعريف الترحيل لتصنيف الحسابات الرئيسية والأبعاد المالية في الإدخالات المحاسبية.</span><span class="sxs-lookup"><span data-stu-id="f640a-107">For supported posting types and documents, you can use posting definitions instead of posting profiles to classify main accounts and financial dimensions on accounting entries.</span></span> <span data-ttu-id="f640a-108">ويمكنك عرض أنواع الترحيل والمستندات المدعومة في صفحة **تعريفات ترحيل الحركة**.</span><span class="sxs-lookup"><span data-stu-id="f640a-108">You can view the supported documents and posting types on the **Transaction posting definitions** page.</span></span> 

<span data-ttu-id="f640a-109">ولبدء استخدام تعريفات الترحيل، حدد خيار **استخدام تعريفات الترحيل** في صفحة **معلمات دفتر الأستاذ العام**.</span><span class="sxs-lookup"><span data-stu-id="f640a-109">To start using posting definitions, select the **Use posting definitions** option on the **General ledger parameters** page.</span></span> <span data-ttu-id="f640a-110">وحتى عند استخدام تعريفات الترحيل، يجب عليك الاستمرار في تحديد ملفات تعريف الترحيل للإدخالات الناشئة والمستندات وأنواع الترحيل المدعومة.</span><span class="sxs-lookup"><span data-stu-id="f640a-110">Even when you use posting definitions, you must still define posting profiles for the originating entries and non-supported posting types and documents.</span></span> 

<span data-ttu-id="f640a-111">ويجب عليك استخدام تعريفات الترحيل لتمكين محاسبة الالتزامات لأوامر الشراء ومحاسبة الالتزامات المسبقة لطلبات الشراء.</span><span class="sxs-lookup"><span data-stu-id="f640a-111">You must use posting definitions in order to enable encumbrance accounting for purchase orders and pre-encumbrance accounting for purchase requisitions.</span></span>

## <a name="defining-posting-definitions"></a><span data-ttu-id="f640a-112">تحديد تعريفات الترحيل</span><span class="sxs-lookup"><span data-stu-id="f640a-112">Defining posting definitions</span></span>
<span data-ttu-id="f640a-113">استخدم صفحة**تعريفات الترحيل** لتحديد معايير التطابق وتحديد الإدخالات التي يجب إنشاؤها عند حدوث مطابقة.</span><span class="sxs-lookup"><span data-stu-id="f640a-113">Use the **Posting definitions** page to specify the match criteria and define the entries that should be generated when a match occurs.</span></span> <span data-ttu-id="f640a-114">ويتم تقييم معايير المطابقة للإدخالات الناشئة كتوزيعات محاسبة.</span><span class="sxs-lookup"><span data-stu-id="f640a-114">The match criteria are evaluated for the originating entries as accounting distributions.</span></span> 

<span data-ttu-id="f640a-115">وفي صفحة **تعريفات الترحيل**، يمكنك تعيين أرقام الأولوية لبنود الإدخال للتحكم في الترتيب الذي يتم فيه تقييم البنود.</span><span class="sxs-lookup"><span data-stu-id="f640a-115">On the **Posting definitions** page, you can also assign priority numbers to entry lines to control the order in which the lines are evaluated.</span></span> <span data-ttu-id="f640a-116">ويتم تقييم البنود التي لها رقم الأولوية الأقل أولاً.</span><span class="sxs-lookup"><span data-stu-id="f640a-116">The lines that have the lowest priority number are evaluated first.</span></span> <span data-ttu-id="f640a-117">على سبيل المثال، يتم تقييم كافة البنود التي لها أولوية 1، ثم البنود التي لها أولوية 2، وهكذا.</span><span class="sxs-lookup"><span data-stu-id="f640a-117">For example, all lines that have a priority of 1 are evaluated, and then lines that have a priority of 2, and so on.</span></span> <span data-ttu-id="f640a-118">وعندما يتم العثور على مطابقة، فإنه يتم تجاهل معايير المطابقة الأخرى.</span><span class="sxs-lookup"><span data-stu-id="f640a-118">When a match is found, the other match criteria are ignored.</span></span> <span data-ttu-id="f640a-119">بالإضافة إلى ذلك، لا تؤدي سوى المعايير الموجودة في المجموعة التي تطابق الحركة الأصلية إلى إنشاء إدخالات تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="f640a-119">Additionally, only the criteria in the group that match the originating transaction create generated entries.</span></span> 

<span data-ttu-id="f640a-120">ويمكنك التحقق من صحة تعريفات الترحيل الخاص بك باستخدام معالج **اختبار تعريف الترحيل**.</span><span class="sxs-lookup"><span data-stu-id="f640a-120">You can validate your posting definitions by using the **Test posting definition** wizard.</span></span> <span data-ttu-id="f640a-121">وبعد قيامك بتحديد نموذج إدخال أصلي لتعريف ترحيل، سترى الإدخالات التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="f640a-121">After you define a sample originating entry for a posting definition, you'll see the generated entries.</span></span> 

<span data-ttu-id="f640a-122">ويمكنك استخدام إصدارات تعريفات الترحيل جنبا إلى جنب مع تواريخ السريان.</span><span class="sxs-lookup"><span data-stu-id="f640a-122">You can use posting definition versions together with effective dates.</span></span> <span data-ttu-id="f640a-123">على سبيل المثال، يمكنك إنشاء إصدار مستقبلي من تعريف ترحيل للترحيل إلى حساب دفتر أستاذ آخر في سنة مالية جديدة.</span><span class="sxs-lookup"><span data-stu-id="f640a-123">For example, you can create a future version of a posting definition to post to a different ledger account in a new fiscal year.</span></span> 

<span data-ttu-id="f640a-124">واستخدم صفحة **تعريفات ترحيل الحركات** لتعيين تعريفات الترحيل لأنواع الحركات.</span><span class="sxs-lookup"><span data-stu-id="f640a-124">Use the **Transaction posting definitions** page to assign posting definitions to transaction types.</span></span>

## <a name="linking-posting-definitions"></a><span data-ttu-id="f640a-125">ربط تعريفات الترحيل</span><span class="sxs-lookup"><span data-stu-id="f640a-125">Linking posting definitions</span></span>
<span data-ttu-id="f640a-126">يمكنك الربط من تعريف ترحيل واحد إلى آخر عندما تقوم بإنشاء تعريفات الترحيل.</span><span class="sxs-lookup"><span data-stu-id="f640a-126">You can link from one posting definition to another when you create posting definitions.</span></span> <span data-ttu-id="f640a-127">وتُوضع معايير التعريف التي قمت بربطها في الاعتبار فيما بعد، بالإضافة إلى معايير تعريف الترحيل الحالي.</span><span class="sxs-lookup"><span data-stu-id="f640a-127">The criteria for the definition that you linked to are then considered in addition to the criteria for the current posting definition.</span></span> <span data-ttu-id="f640a-128">وتساعد هذه الميزة على توفير الوقت، إذ لا تحتاج إلى إعادة إدخال المعايير في علامة التبويب السريع **إدخالات** في صفحة **تعريفات الترحيل** لتعريف الترحيل الحالي، إذا قمت بإدخال البنود مسبقاً لتعريف آخر.</span><span class="sxs-lookup"><span data-stu-id="f640a-128">This feature helps save you time, because you don't have to reenter criteria on the **Entries** FastTab on the **Posting definitions** page for the current posting definition if you already entered those lines for another definition.</span></span> 

<span data-ttu-id="f640a-129">وفي الرسومات التخطيطية أو الجداول، قم بتضمين أية ارتباطات قد تستخدمها.</span><span class="sxs-lookup"><span data-stu-id="f640a-129">In the diagrams or tables, include any links that you might use.</span></span> <span data-ttu-id="f640a-130">ولتجنب تعارضات مع تعريف الترحيل الحالي، تأكد من أن تكون البنود في أي تعريفات ترحيل تقوم بالارتباط بها فريدة.</span><span class="sxs-lookup"><span data-stu-id="f640a-130">To avoid conflicts with the current posting definition, make sure that the lines in any posting definitions that you link to are unique.</span></span> 

<span data-ttu-id="f640a-131">تنطبق القيود التالية عند قيامك بإنشاء ارتباطات في تعريفات الترحيل:</span><span class="sxs-lookup"><span data-stu-id="f640a-131">The following restrictions apply when you create links in posting definitions:</span></span>

-   <span data-ttu-id="f640a-132">وقد يكون تعريف الترحيل المحدد ارتباطًا إلى تعريف ترحيل آخر أو يمكن الارتباط به من تعريف ترحيل آخر، ولكن ليس كلاهما.</span><span class="sxs-lookup"><span data-stu-id="f640a-132">A given posting definition can either link to another posting definition or be linked to from another posting definition, but not both.</span></span> <span data-ttu-id="f640a-133">ومع ذلك، يمكن لتعريف ترحيل الارتباط بتعريفات ترحيل عديدة.</span><span class="sxs-lookup"><span data-stu-id="f640a-133">However, a posting definition can link to multiple posting definitions.</span></span>
-   <span data-ttu-id="f640a-134">ويمكنك إعداد الارتباطات فقط بين تعريفات الترحيل الموجودة في نفس الوحدة.</span><span class="sxs-lookup"><span data-stu-id="f640a-134">You can set up links only among posting definitions that are in the same module.</span></span>
-   <span data-ttu-id="f640a-135">ويمكنك تعيين تعريف ترحيل لأي نوع حركة، ولكن يجب أن يكون نوع الحركة في الوحدة النمطية نفسها كتعريف ترحيل.</span><span class="sxs-lookup"><span data-stu-id="f640a-135">You can assign a posting definition to any transaction type, but the transaction type must be in the same module as the posting definition.</span></span> <span data-ttu-id="f640a-136">استخدم صفحة **تعريفات ترحيل الحركات** لمعرفة الوحدة التي يوجد فيها نوع الحركة.</span><span class="sxs-lookup"><span data-stu-id="f640a-136">Use the **Transaction posting definitions** page to see what module a transaction type is in.</span></span>


<span data-ttu-id="f640a-137">‏‫لمزيد من المعلومات، راجع [‬‏‫أمثلة تعريفات الترحيل](example-posting-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="f640a-137">For more information, see [Posting definitions examples](example-posting-definitions.md).</span></span> 



