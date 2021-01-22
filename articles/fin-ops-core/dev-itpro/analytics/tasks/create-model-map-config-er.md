---
title: إنشاء تكوينات لتعيين نماذج التقارير الإلكترونية
description: استخدم هذا الإجراء لتصميم تكوين جديد لتعيين نموذج التقارير الإلكترونية، واستخدم وظائف التقارير الإلكترونية المدمجة لإجراء حسابات مجمعة فعالة.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c6ba23af5f7eb517cc58994e54e918b2a305da17
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142145"
---
# <a name="create-electronic-reporting-er-model-mapping-configurations"></a><span data-ttu-id="2013e-103">إنشاء تكوينات لتعيين نماذج التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="2013e-103">Create Electronic reporting (ER) model mapping configurations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2013e-104">استخدم هذا الإجراء لتصميم تكوين جديد لتعيين نموذج التقارير الإلكترونية، واستخدم وظائف التقارير الإلكترونية المدمجة لإجراء حسابات مجمعة فعالة.</span><span class="sxs-lookup"><span data-stu-id="2013e-104">Use this procedure to design a new Electronic reporting (ER) model mapping configuration and use built-in ER functions for efficient aggregate calculations.</span></span> <span data-ttu-id="2013e-105">في هذا الإجراء، ستقوم بإنشاء تكوين لشركة نموذجية، وهي Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="2013e-105">In this procedure, you will create a configuration for sample company, Litware, Inc.</span></span> 

<span data-ttu-id="2013e-106">تم إنشاء هذا الإجراء للاستخدامات مع الدور المعين سواء كان مسؤول النظام أو مطور التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="2013e-106">This procedure is created for uses with the assigned role of System administrator or Electronic reporting developer.</span></span>

<span data-ttu-id="2013e-107">يمكن إتمام هذه الخطوات باستخدام أي مجموعة بيانات.</span><span class="sxs-lookup"><span data-stu-id="2013e-107">These steps can be completed using any dataset.</span></span> <span data-ttu-id="2013e-108">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "إنشاء موفر تكوين ووضع علامة عليه على أنه نشط".</span><span class="sxs-lookup"><span data-stu-id="2013e-108">To complete these steps, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active."</span></span>

1. <span data-ttu-id="2013e-109">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="2013e-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="2013e-110">تأكد من وجود موفر التكوين للشركة النموذجية "Litware, Inc." ومن وضع علامة عليه كنشط.</span><span class="sxs-lookup"><span data-stu-id="2013e-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="2013e-111">إذا لم تشاهد موفر التكوين هذا، فيجب أولاً إكمال الخطوات المذكورة في الإجراء، "إنشاء موفر تكوين ووضع علامة عليه على أنه نشط‬".</span><span class="sxs-lookup"><span data-stu-id="2013e-111">If you don't see this configuration provider, complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>  
2. <span data-ttu-id="2013e-112">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="2013e-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="2013e-113">انقر فوق "إظهار عوامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="2013e-113">Click Show filters.</span></span>
4. <span data-ttu-id="2013e-114">في حقل "الاسم"، أدخل قيمة عامل التصفية "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي" واستخدم عامل التصفية "يبدأ بـ".</span><span class="sxs-lookup"><span data-stu-id="2013e-114">In the "Name" field, enter the filter value, "Intrastat" and use the filter operator "begins with".</span></span>
    * <span data-ttu-id="2013e-115">طبّق عامل التصفية هذا للبحث عن تكوين نموذج بيانات نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="2013e-115">Apply this filter to find the 'Intrastat' data model configuration.</span></span> <span data-ttu-id="2013e-116">قد يكون هذا النموذج موجودًا في شجرة التكوينات.</span><span class="sxs-lookup"><span data-stu-id="2013e-116">This model may already exist in the configurations tree.</span></span> <span data-ttu-id="2013e-117">إذا كان موجودًا، فيمكنك تخطي المهمة الفرعية التالية.</span><span class="sxs-lookup"><span data-stu-id="2013e-117">If it does, skip the next sub-task.</span></span>   

## <a name="get-the-intrastat-model-configuration-provided-by-microsoft"></a><span data-ttu-id="2013e-118">الحصول على تكوين نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي الذي توفره Microsoft</span><span class="sxs-lookup"><span data-stu-id="2013e-118">Get the Intrastat model configuration provided by Microsoft</span></span>
1. <span data-ttu-id="2013e-119">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2013e-119">Close the page.</span></span>
2. <span data-ttu-id="2013e-120">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2013e-120">Close the page.</span></span>
3. <span data-ttu-id="2013e-121">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="2013e-121">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
4. <span data-ttu-id="2013e-122">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="2013e-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2013e-123">حدد لوحة "موفر Microsoft".</span><span class="sxs-lookup"><span data-stu-id="2013e-123">Select the Microsoft provider tile.</span></span>  
5. <span data-ttu-id="2013e-124">انقر فوق "المستودعات".</span><span class="sxs-lookup"><span data-stu-id="2013e-124">Click Repositories.</span></span>
    * <span data-ttu-id="2013e-125">انقر فوق "المستودعات‬" على لوحة موفر Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2013e-125">Click Repositories in the Microsoft provider tile.</span></span>  
6. <span data-ttu-id="2013e-126">انقر فوق "إظهار عوامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="2013e-126">Click Show filters.</span></span>
7. <span data-ttu-id="2013e-127">في حقل "نوع الاسم"، أدخل قيمة عامل التصفية "موارد" واستخدم عامل التصفية "يحتوي".</span><span class="sxs-lookup"><span data-stu-id="2013e-127">In the "Type name" field, enter the filter value, "resources" and use the filter operator "contains".</span></span> 
8. <span data-ttu-id="2013e-128">انقر فوق "فتح".</span><span class="sxs-lookup"><span data-stu-id="2013e-128">Click Open.</span></span>
9. <span data-ttu-id="2013e-129">في الشجرة، حدد "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي".</span><span class="sxs-lookup"><span data-stu-id="2013e-129">In the tree, select 'Intrastat model'.</span></span>
10. <span data-ttu-id="2013e-130">انقر فوق "استيراد".</span><span class="sxs-lookup"><span data-stu-id="2013e-130">Click Import.</span></span>
11. <span data-ttu-id="2013e-131">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="2013e-131">Click Yes.</span></span>
    * <span data-ttu-id="2013e-132">لقد قمت باستيراد تكوين نموذج التقارير الإلكترونية الذي يحتوي على نموذج البيانات الذي ستستخدمه لاستكشاف كيفية استخدام وظائف التقارير الإلكترونية الجديدة.</span><span class="sxs-lookup"><span data-stu-id="2013e-132">You imported the ER model configuration that contains the data model that you will use to explore how the new ER functionality can be used.</span></span>  
12. <span data-ttu-id="2013e-133">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2013e-133">Close the page.</span></span>
13. <span data-ttu-id="2013e-134">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2013e-134">Close the page.</span></span>
14. <span data-ttu-id="2013e-135">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="2013e-135">Click Reporting configurations.</span></span>

## <a name="add-a-new-model-mapping-configuration"></a><span data-ttu-id="2013e-136">إضافة تكوين تعيين نموذج جديد</span><span class="sxs-lookup"><span data-stu-id="2013e-136">Add a new model mapping configuration</span></span>
1. <span data-ttu-id="2013e-137">في الشجرة، حدد "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي".</span><span class="sxs-lookup"><span data-stu-id="2013e-137">In the tree, select 'Intrastat model'.</span></span>
2. <span data-ttu-id="2013e-138">انقر فوق "إنشاء تكوين" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="2013e-138">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="2013e-139">في الحقل "جديد"، أدخل "تعيين النموذج استنادًا إلى نموذج بيانات نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي".</span><span class="sxs-lookup"><span data-stu-id="2013e-139">In the New field, enter 'Model Mapping based on data model Intrastat'.</span></span>
4. <span data-ttu-id="2013e-140">في حقل "الاسم"، اكتب "تعيين نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي".</span><span class="sxs-lookup"><span data-stu-id="2013e-140">In the Name field, type 'Intrastat sample mapping'.</span></span>
    * <span data-ttu-id="2013e-141">تعيين نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي</span><span class="sxs-lookup"><span data-stu-id="2013e-141">Intrastat sample mapping</span></span>  
5. <span data-ttu-id="2013e-142">وانقر فوق إنشاء تكوين.</span><span class="sxs-lookup"><span data-stu-id="2013e-142">Click Create configuration.</span></span>
