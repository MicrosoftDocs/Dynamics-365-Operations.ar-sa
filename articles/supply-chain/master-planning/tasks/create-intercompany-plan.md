---
title: إنشاء خطة بين الشركات الشقيقة
description: يوضح هذا الإجراء كيفية إنشاء خطة بين الشركات شقيقة.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 194bb78eed5a673030f7cead031cf286cddbe77c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845199"
---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="5ba1c-103">إنشاء خطة بين الشركات الشقيقة</span><span class="sxs-lookup"><span data-stu-id="5ba1c-103">Create an intercompany plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5ba1c-104">يوضح هذا الإجراء كيفية إنشاء خطة بين الشركات شقيقة.</span><span class="sxs-lookup"><span data-stu-id="5ba1c-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="5ba1c-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="5ba1c-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="5ba1c-106">إعداد مجموعة تخطيط بين الشركات الشقيقة</span><span class="sxs-lookup"><span data-stu-id="5ba1c-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="5ba1c-107">انتقل إلى "مجموعات التخطيط بين الشركات الشقيقة".</span><span class="sxs-lookup"><span data-stu-id="5ba1c-107">Go to Intercompany planning groups.</span></span>
    * <span data-ttu-id="5ba1c-108">التخطيط الرئيسي‬ > الإعداد > مجموعات التخطيط بين الشركات الشقيقة.</span><span class="sxs-lookup"><span data-stu-id="5ba1c-108">Master planning > Setup > Intercompany planning groups</span></span>  
2. <span data-ttu-id="5ba1c-109">استخدم عامل التصفية السريع للبحث عن السجلات.</span><span class="sxs-lookup"><span data-stu-id="5ba1c-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="5ba1c-110">على سبيل المثال، قم بإجراء التصفية على حقل الاسم بقيمة '10'.</span><span class="sxs-lookup"><span data-stu-id="5ba1c-110">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="5ba1c-111">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="5ba1c-111">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="5ba1c-112">انقر فوق حذف.</span><span class="sxs-lookup"><span data-stu-id="5ba1c-112">Click Delete.</span></span>
    * <span data-ttu-id="5ba1c-113">تُعد هذه الخطوة ضرورية من أجل تقصير تشغيل التخطيط بين الشركات الشقيقة.</span><span class="sxs-lookup"><span data-stu-id="5ba1c-113">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="5ba1c-114">سيقوم التخطيط بين الشركات الشقيقة بتشغيل التخطيط الرئيسي في كل الشركات في مجموعة تخطيط، بدءًا من تسلسل الجدولة الأدنى.</span><span class="sxs-lookup"><span data-stu-id="5ba1c-114">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="5ba1c-115">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="5ba1c-115">Click Yes.</span></span>
6. <span data-ttu-id="5ba1c-116">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="5ba1c-116">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="5ba1c-117">إنشاء خطة بين الشركات الشقيقة</span><span class="sxs-lookup"><span data-stu-id="5ba1c-117">Create an intercompany plan</span></span>
1. <span data-ttu-id="5ba1c-118">انقر فوق "تخطيط رئيسي بين الشركات الشقيقة".</span><span class="sxs-lookup"><span data-stu-id="5ba1c-118">Click Intercompany master planning.</span></span>
    * <span data-ttu-id="5ba1c-119">ويتم هذا على مساحة عمل التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="5ba1c-119">This is on the Master planning workspace.</span></span>  
2. <span data-ttu-id="5ba1c-120">في الحقل "مجموعة التخطيط بين الشركات الشقيقة‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="5ba1c-120">In the Intercompany planning group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="5ba1c-121">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="5ba1c-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="5ba1c-122">حدد مجموعة التخطيط بين الشركات الشقيقة 10.</span><span class="sxs-lookup"><span data-stu-id="5ba1c-122">Select intercompany planning group 10.</span></span>  
4. <span data-ttu-id="5ba1c-123">في الحقل "عدد تكرارات التخطيط بين الشركات الشقيقة"، أدخل "2".</span><span class="sxs-lookup"><span data-stu-id="5ba1c-123">In the Number of intercompany planning iterations field, enter '2'.</span></span>
    * <span data-ttu-id="5ba1c-124">هناك عضوان في مجموعة التخطيط بين الشركات الشقيقة 10.</span><span class="sxs-lookup"><span data-stu-id="5ba1c-124">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="5ba1c-125">من أجل نشر التأخيرات من الشركة المصدر (USMF) إلى شركة العميل (DEMF)، سوف تحتاج إلى تشغيل التخطيط بين الشقيقة في الشركتين مرتين.</span><span class="sxs-lookup"><span data-stu-id="5ba1c-125">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="5ba1c-126">سيقوم التكرار الأول بنشر الطلب وتحديد حالات التأخير في الشركة المصدر (USMF).</span><span class="sxs-lookup"><span data-stu-id="5ba1c-126">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="5ba1c-127">أما التكرار الثاني فسيقوم بنشر التأخيرات من USMF إلى DEMF.</span><span class="sxs-lookup"><span data-stu-id="5ba1c-127">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
5. <span data-ttu-id="5ba1c-128">في الحقل "التكرار الأول‬"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="5ba1c-128">In the First iteration field, select an option.</span></span>
6. <span data-ttu-id="5ba1c-129">في الحقل "التكرار الأول‬"، حدد "إعادة إنشاء‬".</span><span class="sxs-lookup"><span data-stu-id="5ba1c-129">In the First iteration field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="5ba1c-130">في الحقل "التكرارات اللاحقة‬‬"، حدد "إعادة إنشاء‬"‬.</span><span class="sxs-lookup"><span data-stu-id="5ba1c-130">In the Subsequent iterations field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="5ba1c-131">في الحقل "عدد السلاسل"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="5ba1c-131">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="5ba1c-132">يمثل هذا عدد السلاسل المتوازية التي تستخدم للتخطيط.</span><span class="sxs-lookup"><span data-stu-id="5ba1c-132">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="5ba1c-133">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="5ba1c-133">Click OK.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="5ba1c-134">عرض نتيجة الخطة</span><span class="sxs-lookup"><span data-stu-id="5ba1c-134">View the result of the plan</span></span>
1. <span data-ttu-id="5ba1c-135">في الحقل "الخطة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="5ba1c-135">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="5ba1c-136">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="5ba1c-136">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="5ba1c-137">انقر فوق ارتباط StaticPlan.</span><span class="sxs-lookup"><span data-stu-id="5ba1c-137">Click the link for StaticPlan.</span></span> <span data-ttu-id="5ba1c-138">عليك أن تكون في شركة USMF.</span><span class="sxs-lookup"><span data-stu-id="5ba1c-138">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="5ba1c-139">انقر فوق "الأوامر المخططة".</span><span class="sxs-lookup"><span data-stu-id="5ba1c-139">Click Planned orders.</span></span>

