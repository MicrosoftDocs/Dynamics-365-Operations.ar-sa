--- 
title: "إعداد سياسات للتدرج الهرمي لفئات التدبير"
description: "استخدم هذا الإجراء لإعداد قواعد طلب المنتجات الموجودة في إحدى الفئات."
author: mkirknel
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicyListPage, SysPolicy, ProcCategoryAccessPolicyRule, ProcCategoryPolicyRule, EcoResCategorySingleLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 1c5e4b70897af5e45350d1b3766fc1d303a36ea1
ms.contentlocale: ar-sa
ms.lasthandoff: 09/11/2018

---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a><span data-ttu-id="0854f-103">إعداد سياسات للتدرج الهرمي لفئات التدبير</span><span class="sxs-lookup"><span data-stu-id="0854f-103">Set up policies for procurement category hierarchies</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0854f-104">استخدم هذا الإجراء لإعداد قواعد طلب المنتجات الموجودة في إحدى الفئات.</span><span class="sxs-lookup"><span data-stu-id="0854f-104">Use this procedure to set up rules for ordering products in a category.</span></span> <span data-ttu-id="0854f-105">تم تحديد القواعد لسياسة شراء معينة.</span><span class="sxs-lookup"><span data-stu-id="0854f-105">The rules are defined for a specific purchasing policy.</span></span> <span data-ttu-id="0854f-106">تحدد قاعدة الوصول إلى الفئة فئات التدبير التي يستطيع الموظفون الوصول إليها عندما يقومون بإنشاء طلب.</span><span class="sxs-lookup"><span data-stu-id="0854f-106">The category access rule controls which procurement categories employees have access to when they create a requisition.</span></span> <span data-ttu-id="0854f-107">عند إنشاء طلب، تتحدد سياسة الشراء وقاعدة الوصول إلى الفئة التي يجب تطبيقها استنادًا إلى الكيان القانوني والوحدة التشغيلية التي ينتمي الموظف إليها.</span><span class="sxs-lookup"><span data-stu-id="0854f-107">When a requisition is being created, the purchasing policy and category access rule that should be applied are determined by the legal entity and the operational unit that the employee belongs to.</span></span> <span data-ttu-id="0854f-108">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="0854f-108">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="0854f-109">يقوم مدير المشتريات عادةً بتنفيذ هذه المهمة.</span><span class="sxs-lookup"><span data-stu-id="0854f-109">This task would typically be carried out by a purchasing manager.</span></span>


## <a name="find-the-procurement-policy"></a><span data-ttu-id="0854f-110">البحث عن سياسة التدبير</span><span class="sxs-lookup"><span data-stu-id="0854f-110">Find the procurement policy</span></span>
1. <span data-ttu-id="0854f-111">انتقل إلى التدبير وتحديد الموارد > إعداد > السياسات > سياسات الشراء.</span><span class="sxs-lookup"><span data-stu-id="0854f-111">Go to Procurement and sourcing > Setup > Policies > Purchasing policies.</span></span>
2. <span data-ttu-id="0854f-112">انقر فوق الارتباط الموجود في سياسة USMF لسياسة التدبير.</span><span class="sxs-lookup"><span data-stu-id="0854f-112">Click the link on the Procurement Policy USMF policy.</span></span>
    * <span data-ttu-id="0854f-113">هذه هي السياسة التي ستضيف قاعدة إليها.</span><span class="sxs-lookup"><span data-stu-id="0854f-113">This is the policy that you’ll add a rule to.</span></span> <span data-ttu-id="0854f-114">يجب أن تكون سياسة نشطة.</span><span class="sxs-lookup"><span data-stu-id="0854f-114">It must be an Active policy.</span></span>  

## <a name="create-a-category-access-rule"></a><span data-ttu-id="0854f-115">إنشاء قاعدة وصول إلى الفئة</span><span class="sxs-lookup"><span data-stu-id="0854f-115">Create a category access rule</span></span>
1. <span data-ttu-id="0854f-116">حدد قاعدة سياسة الوصول إلى الفئة.</span><span class="sxs-lookup"><span data-stu-id="0854f-116">Select the Category access policy rule.</span></span>
    * <span data-ttu-id="0854f-117">إذا كان الزر "إنشاء قاعدة السياسة" خافتًا، فيعود سبب ذلك إلى وجود قاعدة سياسة نشطة للوصول إلى الفئة.</span><span class="sxs-lookup"><span data-stu-id="0854f-117">If the Create policy rule button is dimmed, it’s because there’s already an active policy rule for Category access.</span></span> <span data-ttu-id="0854f-118">تحقق من حقلي "تاريخ السريان" و"تاريخ انتهاء الصلاحية" لتحديد السياسة النشطة، ثم حددها، وانقر فوق "إيقاف قاعدة السياسة‬".</span><span class="sxs-lookup"><span data-stu-id="0854f-118">Check the Effective and Expiration date fields to determine which it is, then select it, and click Retire policy rule.</span></span> <span data-ttu-id="0854f-119">إذا توفر الزر "إنشاء قاعدة السياسة‬"، فلا يلزم القيام بأي شيء.</span><span class="sxs-lookup"><span data-stu-id="0854f-119">If the Create policy rule button is available, you don’t need to do anything.</span></span>  
2. <span data-ttu-id="0854f-120">انقر فوق "إنشاء قاعدة السياسة".</span><span class="sxs-lookup"><span data-stu-id="0854f-120">Click Create policy rule.</span></span>
3. <span data-ttu-id="0854f-121">في الحقل "تاريخ السريان"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="0854f-121">In the Effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="0854f-122">يجب أن لا يتداخل الوقت مع قاعدة أخرى نشطة بالفعل.</span><span class="sxs-lookup"><span data-stu-id="0854f-122">The time must not overlap with another rule that’s already active.</span></span>  
    * <span data-ttu-id="0854f-123">حدد فئة ستنطبق القاعدة عليها.</span><span class="sxs-lookup"><span data-stu-id="0854f-123">Select a category that the rule will apply to.</span></span> <span data-ttu-id="0854f-124">قم بتدوين هذه الفئة – ستحتاجها فيما بعد.</span><span class="sxs-lookup"><span data-stu-id="0854f-124">Make a note of which category this is – you’ll need it later.</span></span> <span data-ttu-id="0854f-125">وعند تحديد فئة، تتم أيضًا إضافة الفئة (الفئات) الأصلية الخاصة بها إلى قائمة "الفئات المحددة".</span><span class="sxs-lookup"><span data-stu-id="0854f-125">When you select a category, its parent category or categories will also be added to the Selected categories list.</span></span>  
    * <span data-ttu-id="0854f-126">إذا أردت تطبيق القاعدة على كافة الفئات الفرعية للفئة المحددة، فحدد خانة الاختيار "تضمين الفئات الفرعية".</span><span class="sxs-lookup"><span data-stu-id="0854f-126">If you want the rule to apply to all subcategories of the selected category, select the Include subcategories check box.</span></span>  
4. <span data-ttu-id="0854f-127">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="0854f-127">Click Add.</span></span>
    * <span data-ttu-id="0854f-128">إذا قمت بتعيين الخيار "تضمين قاعدة الأصل" إلى "نعم"، فسيتم أيضًا تعيين قاعدة السياسة التي حددتها لفئة رئيسية إلى فئاتها الفرعية، إذا لم يتم تحديد قاعدة سياسة للفئات الفرعية.</span><span class="sxs-lookup"><span data-stu-id="0854f-128">If you set the Include parent rule option to Yes, the policy rule that you define for a parent category is also assigned to its child categories, if no policy rule has been defined for the child categories.</span></span>  
5. <span data-ttu-id="0854f-129">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="0854f-129">Click OK.</span></span>

## <a name="create-a-category-policy-rule"></a><span data-ttu-id="0854f-130">إنشاء قاعدة سياسة الفئة</span><span class="sxs-lookup"><span data-stu-id="0854f-130">Create a category policy rule</span></span>
1. <span data-ttu-id="0854f-131">حدد قاعدة سياسة الفئة</span><span class="sxs-lookup"><span data-stu-id="0854f-131">Select the Category policy rule</span></span>
    * <span data-ttu-id="0854f-132">إذا كان الزر "إنشاء قاعدة السياسة‬" خافتًا، فحدد قاعدة السياسة النشطة، ثم انقر فوق "إيقاف قاعدة السياسة‬".</span><span class="sxs-lookup"><span data-stu-id="0854f-132">If the Create policy rule button is dimmed, select the active policy rule, and then click Retire policy rule.</span></span>  
2. <span data-ttu-id="0854f-133">انقر فوق "إنشاء قاعدة السياسة".</span><span class="sxs-lookup"><span data-stu-id="0854f-133">Click Create policy rule.</span></span>
3. <span data-ttu-id="0854f-134">في الحقل "تاريخ السريان"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="0854f-134">In the Effective date field, enter a date and time.</span></span>
4. <span data-ttu-id="0854f-135">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="0854f-135">Click Add.</span></span>
5. <span data-ttu-id="0854f-136">حدد نفس الفئة المستخدمة لقاعدة الوصول إلى الفئة.</span><span class="sxs-lookup"><span data-stu-id="0854f-136">Select the same category that you used for the Category access rule.</span></span>
6. <span data-ttu-id="0854f-137">في الحقل "تحديد المورِّد‬"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="0854f-137">In the Vendor selection field, select an option.</span></span>
    * <span data-ttu-id="0854f-138">حدد قاعدة للتحكم في أنواع المورّدين الذين يمكن اختيارهم للفئة عند إنشاء طلبات الشراء.</span><span class="sxs-lookup"><span data-stu-id="0854f-138">Select a rule to control which kind of vendors can be selected for the category when requisitions are created.</span></span>  
7. <span data-ttu-id="0854f-139">انقر فوق "إغلاق".</span><span class="sxs-lookup"><span data-stu-id="0854f-139">Click Close.</span></span>
    * <span data-ttu-id="0854f-140">تتعلق قواعد السياسة التي حددتها بطلبات من النوع "استهلاك".</span><span class="sxs-lookup"><span data-stu-id="0854f-140">The policy rules that you have defined have been for requisitions of type Consumption.</span></span> <span data-ttu-id="0854f-141">إذا أردت تحديد سياسات لطلبات من النوع "تزويد"، فيمكنك إنشاء قاعدة لنوع قاعدة السياسة المسمى "قاعدة سياسة الوصول لفئة التزويد‬".</span><span class="sxs-lookup"><span data-stu-id="0854f-141">If you wanted to define policies for requisitions of type Replenishment, you would create a rule for the Policy rule type called “Replenishment category access policy rule”.</span></span>  


