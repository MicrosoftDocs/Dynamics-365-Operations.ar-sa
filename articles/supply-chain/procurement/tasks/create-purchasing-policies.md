--- 
title: "إنشاء مناهج الشراء"
description: "يوضح هذا الإجراء كيفية إنشاء سياسات شراء لتتماشى مع عملياتك التجارية الخاصة بالشراء."
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: dd5a62dc1459f1768104eeaea3e71780431e8e79
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---
# <a name="create-purchasing-policies"></a><span data-ttu-id="4592a-103">إنشاء مناهج الشراء</span><span class="sxs-lookup"><span data-stu-id="4592a-103">Create purchasing policies</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4592a-104">يوضح هذا الإجراء كيفية إنشاء سياسات شراء لتتماشى مع عملياتك التجارية الخاصة بالشراء.</span><span class="sxs-lookup"><span data-stu-id="4592a-104">This procedure shows you how to create purchasing policies to align with your business processes for purchasing.</span></span> <span data-ttu-id="4592a-105">قبل أن تتمكن من إنشاء سياسات الشراء، يجب أن تقوم بإعداد محددات سياسة الشراء.</span><span class="sxs-lookup"><span data-stu-id="4592a-105">Before you can create purchasing policies, you must set up the purchasing policy parameters.</span></span> <span data-ttu-id="4592a-106">من الممكن إنشاء سياسة شراء وتعديلها وإيقافها، ولكن لا يمكنك حذف سياسة شراء.</span><span class="sxs-lookup"><span data-stu-id="4592a-106">It’s possible to create, modify, and retire a purchasing policy, but you can’t delete a purchasing policy.</span></span> <span data-ttu-id="4592a-107">يقوم مدير المشتريات عادةً بتنفيذ هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="4592a-107">This procedure would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="4592a-108">يمكنك استخدام هذا الإجراء في شركة بيانات العرض التقديمي USMF، أو في البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="4592a-108">You can use this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-policy-parameters"></a><span data-ttu-id="4592a-109">إعداد محددات السياسة</span><span class="sxs-lookup"><span data-stu-id="4592a-109">Set up policy parameters</span></span>
1. <span data-ttu-id="4592a-110">انتقل إلى "سياسات الشراء".</span><span class="sxs-lookup"><span data-stu-id="4592a-110">Go to Purchasing policies.</span></span>
2. <span data-ttu-id="4592a-111">انقر فوق "المحددات".</span><span class="sxs-lookup"><span data-stu-id="4592a-111">Click Parameters.</span></span>
    * <span data-ttu-id="4592a-112">تنطبق قواعد أسبقية السياسة على مستويات مختلفة في مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="4592a-112">Policy precedence rules apply to different levels in your organization.</span></span> <span data-ttu-id="4592a-113">تتوقف الوحدات التنظيمية المعروضة على التدرج الهرمي التنظيمي، وعلى المستويات في التدرج الهرمي التي تم تعيين غرض التحكم الداخلي للتدبير لها.</span><span class="sxs-lookup"><span data-stu-id="4592a-113">The organizational units that are shown depend on your organizational hierarchy, and on which levels in the hierarchy have been assigned the purpose of Procurement internal control.</span></span> <span data-ttu-id="4592a-114">على سبيل المثال، قد تتضمن مؤسستك كيانات قانونية ومراكز تكلفة ومناطق وأقسام، ولكن قد يكون للبعض منها فقط غرض تدرج هرمي للتحكم الداخلي للتدبير.</span><span class="sxs-lookup"><span data-stu-id="4592a-114">For example, your organization might have legal entities, cost centers, regions, and departments, but it may be that only some of these have a hierarchy purpose of Procurement internal control.</span></span> <span data-ttu-id="4592a-115">بشكل افتراضي، تتوفر المؤسسة من نوع "الشركة".</span><span class="sxs-lookup"><span data-stu-id="4592a-115">As a default, the organization of type Company is available.</span></span>  
3. <span data-ttu-id="4592a-116">انقر فوق علامة التبويب "محددات نوع قاعدة السياسة".</span><span class="sxs-lookup"><span data-stu-id="4592a-116">Click the Policy rule type parameters tab.</span></span>
4. <span data-ttu-id="4592a-117">في الشجرة، حدد "سياسة الشراء/قاعدة التحكم في طلب الشراء‬".</span><span class="sxs-lookup"><span data-stu-id="4592a-117">In the tree, select 'Purchasing policy\Purchase requisition control rule'.</span></span>
    * <span data-ttu-id="4592a-118">حدد ترتيب الأسبقية الخاص بحل السياسة على مستوى السياسة.</span><span class="sxs-lookup"><span data-stu-id="4592a-118">You define the order of precedence for policy resolution at the policy level.</span></span> <span data-ttu-id="4592a-119">ومع ذلك، بالنسبة لبعض أنواع السياسات، يمكنك تجاوز ترتيب الأسبقية الخاص بأنواع قواعد السياسة الفردية.</span><span class="sxs-lookup"><span data-stu-id="4592a-119">However, for some policy types, you can override the order of precedence for individual policy rule types.</span></span> <span data-ttu-id="4592a-120">على سبيل المثال، يمكنك تعريف ترتيب الأسبقية لسياسات الشراء بهذا الترتيب: مركز التكلفة، القسم، الشركة.</span><span class="sxs-lookup"><span data-stu-id="4592a-120">For example, you might define the order of precedence for purchasing policies to be: cost center, department, company.</span></span> <span data-ttu-id="4592a-121">بالنسبة إلى قاعدة سياسة الكتالوج، قد ترغب في أن يكون ترتيب الأسبقية بهذا الترتيب: القسم، مركز التكلفة، الشركة.</span><span class="sxs-lookup"><span data-stu-id="4592a-121">For the catalog policy rule, you might want the order of precedence to be: department, cost center, company.</span></span> <span data-ttu-id="4592a-122">يمكنك تغيير ترتيب الأسبقية فقط لقاعدة سياسة الكتالوج.</span><span class="sxs-lookup"><span data-stu-id="4592a-122">You can change the order of precedence for the Catalog policy rule.</span></span> <span data-ttu-id="4592a-123">عندما يقوم العامل بإنشاء طلب، يتحدد الكتالوج الذي يظهر بالسياسات المرتبطة بقسم العامل، ثم مركز التكلفة، ثم الشركة.</span><span class="sxs-lookup"><span data-stu-id="4592a-123">When a worker creates a requisition, the catalog that is displayed is determined by the policies that are associated with the worker’s department, then their cost center, and then their company.</span></span>  
    * <span data-ttu-id="4592a-124">إذا تم إدراج أكثر من مستوى تنظيمي واحد، فيمكنك استخدام السهمين لأعلى/لأسفل لتعيين ترتيب الأسبقية لقاعدة التحكم في طلب الشراء.</span><span class="sxs-lookup"><span data-stu-id="4592a-124">If there’s more than one organizational level listed, you can use the Up/Down arrows to set the order of precedence for the Purchase requisition control rule.</span></span>  
5. <span data-ttu-id="4592a-125">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="4592a-125">Close the page.</span></span>

## <a name="create-a-new-policy"></a><span data-ttu-id="4592a-126">إنشاء سياسة جديدة</span><span class="sxs-lookup"><span data-stu-id="4592a-126">Create a new policy</span></span>
1. <span data-ttu-id="4592a-127">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="4592a-127">Click New.</span></span>
2. <span data-ttu-id="4592a-128">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="4592a-128">In the Name field, type a value.</span></span>
3. <span data-ttu-id="4592a-129">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="4592a-129">In the Description field, type a value.</span></span>
    * <span data-ttu-id="4592a-130">يمكن تطبيق سياسة شراء واحدة على تدرج هرمي واحد فقط للمؤسسات.</span><span class="sxs-lookup"><span data-stu-id="4592a-130">A single purchasing policy can only apply to one organization hierarchy.</span></span> <span data-ttu-id="4592a-131">على سبيل المثال، يُحتمل وجود تدرج هرمي يسمى "جغرافي" وآخر يسمى "قسم"، ولكل تدرج هرمي سياسة شراء مختلفة عن الآخر.</span><span class="sxs-lookup"><span data-stu-id="4592a-131">For example, you could have one hierarchy called “Geographic” and one called “Department”, and have a different purchasing policy for each.</span></span>  
    * <span data-ttu-id="4592a-132">حدد مؤسسة يجب تطبيق السياسة عليها.</span><span class="sxs-lookup"><span data-stu-id="4592a-132">Select an organization that the policy should apply to.</span></span>  
4. <span data-ttu-id="4592a-133">انقر فوق السهم لإضافة المؤسسة المحددة.</span><span class="sxs-lookup"><span data-stu-id="4592a-133">Click the arrow to add the selected organization.</span></span>
    * <span data-ttu-id="4592a-134">يمكنك تكرار هذه العملية لإضافة المزيد من المؤسسات.</span><span class="sxs-lookup"><span data-stu-id="4592a-134">You can repeat this process to add more organizations.</span></span>  

## <a name="add-a-policy-rule"></a><span data-ttu-id="4592a-135">إضافة قاعدة السياسة</span><span class="sxs-lookup"><span data-stu-id="4592a-135">Add a policy rule</span></span>
1. <span data-ttu-id="4592a-136">في قائمة "نوع قاعدة السياسة"، حدد "قاعدة غرض الطلب".</span><span class="sxs-lookup"><span data-stu-id="4592a-136">In the Policy rule type list, select Requisition purpose rule.</span></span>
    * <span data-ttu-id="4592a-137">ستقوم بإنشاء قاعدة تعيّن غرض الطلب الافتراضي إلى النوع "استهلاك"، ولكنها تسمح بتحديد نوع "التزويد" بدلاً من ذلك.</span><span class="sxs-lookup"><span data-stu-id="4592a-137">You’ll create a rule that sets the default requisition purpose to type Consumption but allows the Replenishment type to be selected instead.</span></span>  
2. <span data-ttu-id="4592a-138">انقر فوق "إنشاء قاعدة السياسة".</span><span class="sxs-lookup"><span data-stu-id="4592a-138">Click Create policy rule.</span></span>
3. <span data-ttu-id="4592a-139">حدد "نعم" في حقل "‏‫السماح بالتجاوز اليدوي‬".</span><span class="sxs-lookup"><span data-stu-id="4592a-139">Select Yes in the Allow manual override field.</span></span>
4. <span data-ttu-id="4592a-140">انقر فوق "إغلاق".</span><span class="sxs-lookup"><span data-stu-id="4592a-140">Click Close.</span></span>
    * <span data-ttu-id="4592a-141">الآن يمكنك إعداد قواعد سياسة أخرى لسياسة الشراء.</span><span class="sxs-lookup"><span data-stu-id="4592a-141">Now you can set up other policy rules for the purchasing policy.</span></span>   <span data-ttu-id="4592a-142">لاحظ أنه لا يمكن لنوع قاعدة سياسة أن يتضمن قواعد متداخلة نشطة في الوقت نفسه ضمن سياسة تدبير واحدة.</span><span class="sxs-lookup"><span data-stu-id="4592a-142">Note that a Policy rule type cannot have overlapping rules that are active at the same time within a single procurement policy.</span></span>  
5. <span data-ttu-id="4592a-143">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="4592a-143">Close the page.</span></span>
6. <span data-ttu-id="4592a-144">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="4592a-144">Close the page.</span></span>


