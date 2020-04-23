---
title: إنشاء خطة بين الشركات الشقيقة
description: يوضح هذا الإجراء كيفية إنشاء خطة بين الشركات شقيقة.
author: ShylaThompson
manager: tfehr
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3a64817f140d8a2302b3b2c2d1e55de103a5bb36
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209687"
---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="3e5df-103">إنشاء خطة بين الشركات الشقيقة</span><span class="sxs-lookup"><span data-stu-id="3e5df-103">Create an intercompany plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3e5df-104">يوضح هذا الإجراء كيفية إنشاء خطة بين الشركات شقيقة.</span><span class="sxs-lookup"><span data-stu-id="3e5df-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="3e5df-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="3e5df-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="3e5df-106">إعداد مجموعة تخطيط بين الشركات الشقيقة</span><span class="sxs-lookup"><span data-stu-id="3e5df-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="3e5df-107">في **جزء التنقل**، انتقل إلى **الوحدات النمطية > التخطيط الرئيسي > الإعداد > مجموعات التخطيط بين الشركات الشقيقة‬**.</span><span class="sxs-lookup"><span data-stu-id="3e5df-107">In the **Navigation pane**, go to **Modules > Master planning > Setup > Intercompany planning groups**.</span></span> 
2. <span data-ttu-id="3e5df-108">استخدم عامل التصفية السريع للبحث عن السجلات.</span><span class="sxs-lookup"><span data-stu-id="3e5df-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="3e5df-109">على سبيل المثال، قم بإجراء التصفية على حقل الاسم بقيمة '10'.</span><span class="sxs-lookup"><span data-stu-id="3e5df-109">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="3e5df-110">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3e5df-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="3e5df-111">انقر فوق **حذف**.</span><span class="sxs-lookup"><span data-stu-id="3e5df-111">Click **Delete**.</span></span> <span data-ttu-id="3e5df-112">تُعد هذه الخطوة ضرورية من أجل تقصير تشغيل التخطيط بين الشركات الشقيقة.</span><span class="sxs-lookup"><span data-stu-id="3e5df-112">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="3e5df-113">سيقوم التخطيط بين الشركات الشقيقة بتشغيل التخطيط الرئيسي في كل الشركات في مجموعة تخطيط، بدءًا من تسلسل الجدولة الأدنى.</span><span class="sxs-lookup"><span data-stu-id="3e5df-113">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="3e5df-114">انقر فوق **نعم**.</span><span class="sxs-lookup"><span data-stu-id="3e5df-114">Click **Yes**.</span></span>
6. <span data-ttu-id="3e5df-115">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3e5df-115">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="3e5df-116">إنشاء خطة بين الشركات الشقيقة</span><span class="sxs-lookup"><span data-stu-id="3e5df-116">Create an intercompany plan</span></span>
1. <span data-ttu-id="3e5df-117">في **جزء التنقل**، انتقل إلى **الوحدات النمطية > التخطيط الرئيسي > مساحات العمل > التخطيط الرئيسي‬**.</span><span class="sxs-lookup"><span data-stu-id="3e5df-117">In the **Navigation pane**, go to **Modules > Master planning > Workspaces > Master planning**.</span></span>
2. <span data-ttu-id="3e5df-118">انقر فوق **تخطيط رئيسي بين الشركات الشقيقة**.</span><span class="sxs-lookup"><span data-stu-id="3e5df-118">Click **Intercompany master planning**.</span></span>  
3. <span data-ttu-id="3e5df-119">في الحقل **مجموعة التخطيط بين الشركات الشقيقة‬**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="3e5df-119">In the **Intercompany planning group** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="3e5df-120">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3e5df-120">In the list, click the link in the selected row.</span></span> <span data-ttu-id="3e5df-121">حدد مجموعة التخطيط بين الشركات الشقيقة 10.</span><span class="sxs-lookup"><span data-stu-id="3e5df-121">Select intercompany planning group 10.</span></span>  
5. <span data-ttu-id="3e5df-122">في الحقل **عدد تكرارات التخطيط بين الشركات الشقيقة**، أدخل '2'.</span><span class="sxs-lookup"><span data-stu-id="3e5df-122">In the **Number of intercompany planning iterations** field, enter '2'.</span></span> <span data-ttu-id="3e5df-123">هناك عضوان في مجموعة التخطيط بين الشركات الشقيقة 10.</span><span class="sxs-lookup"><span data-stu-id="3e5df-123">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="3e5df-124">من أجل نشر التأخيرات من الشركة المصدر (USMF) إلى شركة العميل (DEMF)، سوف تحتاج إلى تشغيل التخطيط بين الشقيقة في الشركتين مرتين.</span><span class="sxs-lookup"><span data-stu-id="3e5df-124">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="3e5df-125">سيقوم التكرار الأول بنشر الطلب وتحديد حالات التأخير في الشركة المصدر (USMF).</span><span class="sxs-lookup"><span data-stu-id="3e5df-125">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="3e5df-126">أما التكرار الثاني فسيقوم بنشر التأخيرات من USMF إلى DEMF.</span><span class="sxs-lookup"><span data-stu-id="3e5df-126">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
6. <span data-ttu-id="3e5df-127">في الحقل **التكرار الأول‬**، حدد "إعادة إنشاء‬".</span><span class="sxs-lookup"><span data-stu-id="3e5df-127">In the **First iteration** field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="3e5df-128">في الحقل **التكرارات اللاحقة‬‬**،  حدد "إعادة إنشاء‬"‬.</span><span class="sxs-lookup"><span data-stu-id="3e5df-128">In the **Subsequent iterations** field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="3e5df-129">في الحقل **عدد السلاسل**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="3e5df-129">In the **Number of threads** field, enter a number.</span></span> <span data-ttu-id="3e5df-130">يمثل هذا عدد السلاسل المتوازية التي تستخدم للتخطيط.</span><span class="sxs-lookup"><span data-stu-id="3e5df-130">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="3e5df-131">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="3e5df-131">Click **OK**.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="3e5df-132">عرض نتيجة الخطة</span><span class="sxs-lookup"><span data-stu-id="3e5df-132">View the result of the plan</span></span>
1. <span data-ttu-id="3e5df-133">في الحقل **الخطة**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="3e5df-133">In the **Plan** field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="3e5df-134">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3e5df-134">In the list, click the link in the selected row.</span></span> <span data-ttu-id="3e5df-135">انقر فوق ارتباط StaticPlan.</span><span class="sxs-lookup"><span data-stu-id="3e5df-135">Click the link for StaticPlan.</span></span> <span data-ttu-id="3e5df-136">عليك أن تكون في شركة USMF.</span><span class="sxs-lookup"><span data-stu-id="3e5df-136">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="3e5df-137">انقر فوق **الأوامر المخططة**.</span><span class="sxs-lookup"><span data-stu-id="3e5df-137">Click **Planned orders**.</span></span>

