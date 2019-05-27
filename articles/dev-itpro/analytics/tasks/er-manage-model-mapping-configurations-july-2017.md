---
title: إدارة تعيينات نماذج التقارير الإلكترونية باستخدام تكوينات تقارير إلكترونية منفصلة
description: تشرح الخطوات التالية كيف يمكن لمستخدم تم تعيينه إلى دور مسؤول النظام أو مطور التقارير الإلكترونية إدارة تعيينات نموذج التقارير الإلكترونية في تكوينات تقارير إلكترونية منفصلة.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 24ca4124d190df94e7ca9ac31c2ea757fe9ff242
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551197"
---
# <a name="manage-er-model-mapping-in-separate-er-configurations"></a><span data-ttu-id="08770-103">إدارة تعيينات نماذج التقارير الإلكترونية باستخدام تكوينات تقارير إلكترونية منفصلة</span><span class="sxs-lookup"><span data-stu-id="08770-103">Manage ER model mapping in separate ER configurations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="08770-104">تشرح الخطوات التالية كيف يمكن لمستخدم تم تعيينه إلى دور مسؤول النظام أو مطور التقارير الإلكترونية إدارة تعيينات نموذج التقارير الإلكترونية في تكوينات تقارير إلكترونية منفصلة.</span><span class="sxs-lookup"><span data-stu-id="08770-104">The following steps explain how a user assigned to the System administrator or Electronic reporting developer role can manage Electronic reporting (ER) model mappings in separate ER configurations.</span></span> <span data-ttu-id="08770-105">في دليل المهام هذا، سوف تنشئ تكوينات التقارير الإلكترونية المطلوبة للشركة النموذجية Litware, Inc. لإكمال دليل المهام هذا، يجب عليك أولاً إكمال الخطوات الموجودة في دليل المهام "التقارير الإلكترونية - إنشاء موفر تكوين ووضع علامة عليه على أنه نشط"‬.</span><span class="sxs-lookup"><span data-stu-id="08770-105">In this task guide, you will create required ER configurations for the sample company, Litware, Inc. To complete this task guide, you must first complete the steps in the task guide, “ER Create a configuration provider” and mark it as active.</span></span> 

<span data-ttu-id="08770-106">نظراً لمشاركة تكوينات التقارير الإلكترونية بين عدة شركات، يمكنك إكمال دليل المهام هذا باستخدام مجموعة بيانات الشركة التي تختارها.</span><span class="sxs-lookup"><span data-stu-id="08770-106">Because ER configurations are shared among companies, you can complete this task guide using the company data set of your choice.</span></span> <span data-ttu-id="08770-107">تتوفر وظيفة دليل المهام هذا إذا قمت بتثبيت أحد الإصلاحات العاجلة التالية: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 للإصدار 7.0 من Dynamics AX أو https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 لإصدار Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="08770-107">The functionality for this task guide is available if you have installed one of the following hotfixes: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 for the Dynamics AX 7.0 version or https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 for the Dynamics 365 for Operations version.</span></span>

1. <span data-ttu-id="08770-108">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="08770-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="08770-109">تحقق من وجود موفر التكوين للشركة النموذجية Litware, Inc. ومن وضع علامة عليه كنشط.</span><span class="sxs-lookup"><span data-stu-id="08770-109">Verify that the configuration provider for the sample company Litware, Inc. is available and marked as active.</span></span> <span data-ttu-id="08770-110">إذا لم تشاهد موفر التكوين هذا، فيجب أولاً إكمال الخطوات المذكورة في دليل المهمة، "إنشاء موفر تكوين ووضع علامة عليه على أنه نشط‬".</span><span class="sxs-lookup"><span data-stu-id="08770-110">If you don’t see this configuration provider, you must first complete the steps in the task guide, Create a configuration provider and mark it as active.</span></span>   

## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="08770-111">إضافة تكوين نموذج تقارير إلكترونية جديد</span><span class="sxs-lookup"><span data-stu-id="08770-111">Add a new ER model configuration</span></span>
1. <span data-ttu-id="08770-112">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="08770-112">Click Reporting configurations.</span></span>
    * <span data-ttu-id="08770-113">أضف تكوين نموذج جديد.</span><span class="sxs-lookup"><span data-stu-id="08770-113">Add a new model configuration.</span></span> <span data-ttu-id="08770-114">يجب أن يكون الاسم فريدًا في شجرة التكوينات.</span><span class="sxs-lookup"><span data-stu-id="08770-114">The name must be unique in the configurations tree.</span></span>  
2. <span data-ttu-id="08770-115">انقر فوق "إنشاء تكوين" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="08770-115">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="08770-116">في الحقل "الاسم"، اكتب "عينة نموذج البيانات‬".</span><span class="sxs-lookup"><span data-stu-id="08770-116">In the Name field, type 'Sample data model'.</span></span>
    * <span data-ttu-id="08770-117">عينة نموذج البيانات</span><span class="sxs-lookup"><span data-stu-id="08770-117">Sample data model</span></span>  
4. <span data-ttu-id="08770-118">وانقر فوق إنشاء تكوين.</span><span class="sxs-lookup"><span data-stu-id="08770-118">Click Create configuration.</span></span>
5. <span data-ttu-id="08770-119">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="08770-119">Click Designer.</span></span>
6. <span data-ttu-id="08770-120">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="08770-120">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="08770-121">في حقل "الاسم" اكتب "الجذر‬".</span><span class="sxs-lookup"><span data-stu-id="08770-121">In the Name field, type 'Root'.</span></span>
    * <span data-ttu-id="08770-122">الجذر</span><span class="sxs-lookup"><span data-stu-id="08770-122">Root</span></span>  
8. <span data-ttu-id="08770-123">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="08770-123">Click Add.</span></span>
9. <span data-ttu-id="08770-124">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="08770-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="08770-125">في الحقل "الاسم"، اكتب "الشركة".</span><span class="sxs-lookup"><span data-stu-id="08770-125">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="08770-126">الشركة</span><span class="sxs-lookup"><span data-stu-id="08770-126">Company</span></span>  
11. <span data-ttu-id="08770-127">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="08770-127">Click Add.</span></span>
12. <span data-ttu-id="08770-128">في حقل "الوصف"، أدخل النص، والوصف الخاص بالكيان القانوني أو الشركة حيث قام مستخدم بتسجيل دخوله أثناء وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="08770-128">In the Description field, enter the text, Description of the legal entity or company in which a user logged at run-time.</span></span> 
    * <span data-ttu-id="08770-129">وصف الكيان القانوني أو الشركة حيث قام المستخدم بتسجيل دخوله أثناء وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="08770-129">Description of the legal entity or company in which a user logged at run-time.</span></span>  
13. <span data-ttu-id="08770-130">انقر فوق "المرجع الجذر".</span><span class="sxs-lookup"><span data-stu-id="08770-130">Click Root reference.</span></span>
14. <span data-ttu-id="08770-131">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="08770-131">Click OK.</span></span>
15. <span data-ttu-id="08770-132">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="08770-132">Click Save.</span></span>
16. <span data-ttu-id="08770-133">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="08770-133">Close the page.</span></span>
17. <span data-ttu-id="08770-134">انقر فوق "تغيير الحالة".</span><span class="sxs-lookup"><span data-stu-id="08770-134">Click Change status.</span></span>
18. <span data-ttu-id="08770-135">انقر فوق "مكتمل".</span><span class="sxs-lookup"><span data-stu-id="08770-135">Click Complete.</span></span>
19. <span data-ttu-id="08770-136">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="08770-136">Click OK.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="08770-137">إضافة تكوين تعيين نموذج جديد للتقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="08770-137">Add a new ER model mapping configuration</span></span>
1. <span data-ttu-id="08770-138">انقر فوق "إنشاء تكوين" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="08770-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="08770-139">في الحقل "جديد"، أدخل "تعيين النموذج استنادًا إلى عينة نموذج البيانات".</span><span class="sxs-lookup"><span data-stu-id="08770-139">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
3. <span data-ttu-id="08770-140">في الحقل "الاسم"، اكتب "تعيين نموذجي".</span><span class="sxs-lookup"><span data-stu-id="08770-140">In the Name field, type 'Sample mapping'.</span></span>
    * <span data-ttu-id="08770-141">تعيين نموذجي</span><span class="sxs-lookup"><span data-stu-id="08770-141">Sample mapping</span></span>  
4. <span data-ttu-id="08770-142">وانقر فوق إنشاء تكوين.</span><span class="sxs-lookup"><span data-stu-id="08770-142">Click Create configuration.</span></span>
5. <span data-ttu-id="08770-143">قم بتوسيع أو طي مقطع "المتطلبات الأساسية‬".</span><span class="sxs-lookup"><span data-stu-id="08770-143">Expand the Prerequisites section.</span></span>
    * <span data-ttu-id="08770-144">لاحظ أن مجموعة المتطلبات الأساسية‬ "عمليات التنفيذ" أضيفت بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="08770-144">Note that the Implementations prerequisites group has been added automatically.</span></span> <span data-ttu-id="08770-145">تحتوي المجموعة على مكون المتطلبات الأساسية الذي يشير إلى تكوين نموذج البيانات الأصل ووضعت عليه علامة "التنفيذ".</span><span class="sxs-lookup"><span data-stu-id="08770-145">The group contains the prerequisite component that refers to the parent data model configuration and is marked as Implementation.</span></span> <span data-ttu-id="08770-146">وهذا يعني أن تكوين تعيين النموذج "تعيين نموذجي" هذا هو بمثابة تنفيذ لنموذج البيانات، عينة نموذج البيانات.</span><span class="sxs-lookup"><span data-stu-id="08770-146">This means that this Sample mapping model mapping configuration is considered the implementation of the data model, Sample data model.</span></span> <span data-ttu-id="08770-147">وبالتالي، سيقوم هذا المكون بإجبار التقارير الإلكترونية على تنزيل تكوين تعيين النموذج، "تعيين نموذجي" من مستودع التقارير الإلكترونية عند تنزيل تكوين النموذج، "عينة نموذج البيانات‬".</span><span class="sxs-lookup"><span data-stu-id="08770-147">Therefore, this component will force ER to download the model mapping configuration, Sample mapping from an ER repository when the model configuration, Sample data model, is downloaded.</span></span>   
6. <span data-ttu-id="08770-148">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="08770-148">Click Designer.</span></span>
    * <span data-ttu-id="08770-149">لاحظ أن تكوين تعيين النموذج الذي تم إنشاؤه يحتوي على تعيين فارغ جديد يحمل الاسم نفسه للتكوين الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="08770-149">Note that the created model mapping configuration contains a new blank mapping with the same name as the created configuration.</span></span> <span data-ttu-id="08770-150">يجب العلم أنه في حال احتواء الطراز الأصل المحدد على تعيينات نموذج، سوف يتم نسخها إلى تكوين تعيين نموذج جديد.</span><span class="sxs-lookup"><span data-stu-id="08770-150">Be aware that when a selected parent model configuration contains model mappings, they will be copied to a new model mapping configuration.</span></span>   
7. <span data-ttu-id="08770-151">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="08770-151">Click Designer.</span></span>
8. <span data-ttu-id="08770-152">في الشجرة، حدد "Dynamics 365 for Operations\الجدول".</span><span class="sxs-lookup"><span data-stu-id="08770-152">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="08770-153">انقر فوق "إضافة جذر".</span><span class="sxs-lookup"><span data-stu-id="08770-153">Click Add root.</span></span>
10. <span data-ttu-id="08770-154">في الحقل "الاسم"، اكتب "الشركة".</span><span class="sxs-lookup"><span data-stu-id="08770-154">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="08770-155">الشركة</span><span class="sxs-lookup"><span data-stu-id="08770-155">Company</span></span>  
11. <span data-ttu-id="08770-156">في الحقل "الجدول"، اكتب "CompanyInfo".</span><span class="sxs-lookup"><span data-stu-id="08770-156">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="08770-157">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="08770-157">CompanyInfo</span></span>  
12. <span data-ttu-id="08770-158">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="08770-158">Click OK.</span></span>
13. <span data-ttu-id="08770-159">في الشجرة، قم بتوسيع "الشركة".</span><span class="sxs-lookup"><span data-stu-id="08770-159">In the tree, expand 'Company'.</span></span>
14. <span data-ttu-id="08770-160">في الشجرة، قم بتوسيع "الشركة\بحث()".</span><span class="sxs-lookup"><span data-stu-id="08770-160">In the tree, expand 'Company\find()'.</span></span>
15. <span data-ttu-id="08770-161">في الشجرة، حدد "الشركة\بحث\()الاسم".</span><span class="sxs-lookup"><span data-stu-id="08770-161">In the tree, select 'Company\find()\Name'.</span></span>
16. <span data-ttu-id="08770-162">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="08770-162">Click Bind.</span></span>
17. <span data-ttu-id="08770-163">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="08770-163">Click Save.</span></span>
18. <span data-ttu-id="08770-164">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="08770-164">Close the page.</span></span>
19. <span data-ttu-id="08770-165">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="08770-165">Close the page.</span></span>
20. <span data-ttu-id="08770-166">في جزء الإجراءات، انقر فوق "التكوينات".</span><span class="sxs-lookup"><span data-stu-id="08770-166">On the Action Pane, click Configurations.</span></span>
21. <span data-ttu-id="08770-167">انقر فوق "محددات المستخدم".</span><span class="sxs-lookup"><span data-stu-id="08770-167">Click User parameters.</span></span>
22. <span data-ttu-id="08770-168">حدد "نعم" في حقل "تشغيل الإعدادات".</span><span class="sxs-lookup"><span data-stu-id="08770-168">Select Yes in the Run settings field.</span></span>
23. <span data-ttu-id="08770-169">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="08770-169">Click OK.</span></span>
24. <span data-ttu-id="08770-170">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="08770-170">Click Edit.</span></span>
25. <span data-ttu-id="08770-171">حدد "نعم" في حقل "تشغيل المسودة‬".</span><span class="sxs-lookup"><span data-stu-id="08770-171">Select Yes in the Run Draft field.</span></span>

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="08770-172">إضافة تكوين تنسيق تقارير إلكترونية جديد</span><span class="sxs-lookup"><span data-stu-id="08770-172">Add a new ER format configuration</span></span>
1. <span data-ttu-id="08770-173">في الشجرة، حدد "عينة نموذج البيانات"</span><span class="sxs-lookup"><span data-stu-id="08770-173">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="08770-174">انقر فوق "إنشاء تكوين" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="08770-174">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="08770-175">في الحقل "جديد"، أدخل "التنسيق المستند إلى نموذج البيانات عينة نموذج البيانات".</span><span class="sxs-lookup"><span data-stu-id="08770-175">In the New field, enter 'Format based on data model Sample data model'.</span></span>
4. <span data-ttu-id="08770-176">في حقل "الاسم"، اكتب "تنسيق نموذجي".</span><span class="sxs-lookup"><span data-stu-id="08770-176">In the Name field, type 'Sample format'.</span></span>
    * <span data-ttu-id="08770-177">تنسيق نموذجي</span><span class="sxs-lookup"><span data-stu-id="08770-177">Sample format</span></span>  
5. <span data-ttu-id="08770-178">وانقر فوق إنشاء تكوين.</span><span class="sxs-lookup"><span data-stu-id="08770-178">Click Create configuration.</span></span>
6. <span data-ttu-id="08770-179">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="08770-179">Click Designer.</span></span>
7. <span data-ttu-id="08770-180">انقر فوق "إضافة جذر" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="08770-180">Click Add root to open the drop dialog.</span></span>
8. <span data-ttu-id="08770-181">في الشجرة، حدد "Text\String".</span><span class="sxs-lookup"><span data-stu-id="08770-181">In the tree, select 'Text\String'.</span></span>
9. <span data-ttu-id="08770-182">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="08770-182">Click OK.</span></span>
10. <span data-ttu-id="08770-183">انقر فوق علامة التبويب "التعيين".</span><span class="sxs-lookup"><span data-stu-id="08770-183">Click the Mapping tab.</span></span>
11. <span data-ttu-id="08770-184">في الشجرة ، قم بتوسيع "النموذج"</span><span class="sxs-lookup"><span data-stu-id="08770-184">In the tree, expand 'model'.</span></span>
12. <span data-ttu-id="08770-185">في الشجرة، حدد "النموذج\الشركة".</span><span class="sxs-lookup"><span data-stu-id="08770-185">In the tree, select 'model\Company'.</span></span>
13. <span data-ttu-id="08770-186">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="08770-186">Click Bind.</span></span>
14. <span data-ttu-id="08770-187">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="08770-187">Click Save.</span></span>
15. <span data-ttu-id="08770-188">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="08770-188">Close the page.</span></span>
    * <span data-ttu-id="08770-189">قم بتشغيل إصدار المسودة للتنسيق الذي تم إنشاؤه لأغراض الاختبار.</span><span class="sxs-lookup"><span data-stu-id="08770-189">Run the draft version of the created format for testing purposes.</span></span>  
16. <span data-ttu-id="08770-190">انقر فوق "تشغيل".</span><span class="sxs-lookup"><span data-stu-id="08770-190">Click Run.</span></span>
    * <span data-ttu-id="08770-191">على علامة التبويب السريعة "الإصدارات"، انقر فوق "تشغيل".</span><span class="sxs-lookup"><span data-stu-id="08770-191">On the Versions FastTab, click Run.</span></span>  
17. <span data-ttu-id="08770-192">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="08770-192">Click OK.</span></span>
    * <span data-ttu-id="08770-193">قم بمراجعة الإخراج الذي يحتوي على اسم الشركة التي سجل المستخدم الذي يقوم بتشغيل تنسيق التكوين هذا دخوله إليها.</span><span class="sxs-lookup"><span data-stu-id="08770-193">Review the output that contains the name of the company in which the user who is running this format configuration is logged into.</span></span> <span data-ttu-id="08770-194">لاحظ أن استخدام تكوين تعيين النموذج الذي تم إنشاؤه يتم بواسطة تكوين التنسيق هذا نظرًا لوجود تكوين متوفر واحد فقط يحتوي على تعيينات النموذج المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="08770-194">Note that the created model mapping configuration is used by this format configuration because there is only one configuration available that contains required model mappings.</span></span>   

## <a name="add-alternative-er-model-mapping-configuration"></a><span data-ttu-id="08770-195">إضافة تكوين تعيين نموذج بديل للتقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="08770-195">Add alternative ER model mapping configuration</span></span>
1. <span data-ttu-id="08770-196">في الشجرة، حدد "عينة نموذج البيانات"</span><span class="sxs-lookup"><span data-stu-id="08770-196">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="08770-197">انقر فوق "إنشاء تكوين" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="08770-197">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="08770-198">في الحقل "جديد"، أدخل "تعيين النموذج استنادًا إلى عينة نموذج البيانات".</span><span class="sxs-lookup"><span data-stu-id="08770-198">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
4. <span data-ttu-id="08770-199">في حقل "الاسم"، اكتب "تعيين نموذجي (بديل)".</span><span class="sxs-lookup"><span data-stu-id="08770-199">In the Name field, type 'Sample mapping (alternative)'.</span></span>
    * <span data-ttu-id="08770-200">تعيين نموذجي (بديل)</span><span class="sxs-lookup"><span data-stu-id="08770-200">Sample mapping (alternative)</span></span>  
5. <span data-ttu-id="08770-201">وانقر فوق إنشاء تكوين.</span><span class="sxs-lookup"><span data-stu-id="08770-201">Click Create configuration.</span></span>
6. <span data-ttu-id="08770-202">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="08770-202">Click Designer.</span></span>
7. <span data-ttu-id="08770-203">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="08770-203">Click Designer.</span></span>
8. <span data-ttu-id="08770-204">في الشجرة، حدد "Dynamics 365 for Operations\الجدول".</span><span class="sxs-lookup"><span data-stu-id="08770-204">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="08770-205">انقر فوق "إضافة جذر".</span><span class="sxs-lookup"><span data-stu-id="08770-205">Click Add root.</span></span>
10. <span data-ttu-id="08770-206">في الحقل "الاسم"، اكتب "الشركة".</span><span class="sxs-lookup"><span data-stu-id="08770-206">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="08770-207">الشركة</span><span class="sxs-lookup"><span data-stu-id="08770-207">Company</span></span>  
11. <span data-ttu-id="08770-208">في الحقل "الجدول"، اكتب "CompanyInfo".</span><span class="sxs-lookup"><span data-stu-id="08770-208">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="08770-209">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="08770-209">CompanyInfo</span></span>  
12. <span data-ttu-id="08770-210">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="08770-210">Click OK.</span></span>
13. <span data-ttu-id="08770-211">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="08770-211">Click Edit.</span></span>
14. <span data-ttu-id="08770-212">في الشجرة، حدد "سلسلة/تسلسل".</span><span class="sxs-lookup"><span data-stu-id="08770-212">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="08770-213">انقر فوق "إضافة دالة".</span><span class="sxs-lookup"><span data-stu-id="08770-213">Click Add function.</span></span>
16. <span data-ttu-id="08770-214">في الشجرة، قم بتوسيع "الشركة".</span><span class="sxs-lookup"><span data-stu-id="08770-214">In the tree, expand 'Company'.</span></span>
17. <span data-ttu-id="08770-215">في الشجرة، قم بتوسيع "الشركة\بحث()".</span><span class="sxs-lookup"><span data-stu-id="08770-215">In the tree, expand 'Company\find()'.</span></span>
18. <span data-ttu-id="08770-216">في الشجرة، حدد "الشركة\بحث\()الاسم".</span><span class="sxs-lookup"><span data-stu-id="08770-216">In the tree, select 'Company\find()\Name'.</span></span>
19. <span data-ttu-id="08770-217">انقر فوق "إضافة مصدر بيانات".</span><span class="sxs-lookup"><span data-stu-id="08770-217">Click Add data source.</span></span>
20. <span data-ttu-id="08770-218">في الحقل "المعادلة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="08770-218">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="08770-219">CONCATENATE(Company.'find()'.Name, ";",</span><span class="sxs-lookup"><span data-stu-id="08770-219">CONCATENATE(Company.'find()'.Name, ";",</span></span>  
21. <span data-ttu-id="08770-220">في الشجرة، حدد "الشركة\بحث()\الشركة(DataArea)'.</span><span class="sxs-lookup"><span data-stu-id="08770-220">In the tree, select 'Company\find()\Company(DataArea)'.</span></span>
22. <span data-ttu-id="08770-221">انقر فوق "إضافة مصدر بيانات".</span><span class="sxs-lookup"><span data-stu-id="08770-221">Click Add data source.</span></span>
23. <span data-ttu-id="08770-222">في الحقل "المعادلة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="08770-222">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="08770-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span><span class="sxs-lookup"><span data-stu-id="08770-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span></span>  
24. <span data-ttu-id="08770-224">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="08770-224">Click Save.</span></span>
25. <span data-ttu-id="08770-225">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="08770-225">Close the page.</span></span>
26. <span data-ttu-id="08770-226">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="08770-226">Click Save.</span></span>
27. <span data-ttu-id="08770-227">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="08770-227">Close the page.</span></span>
28. <span data-ttu-id="08770-228">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="08770-228">Close the page.</span></span>
29. <span data-ttu-id="08770-229">حدد "نعم" في حقل "تشغيل المسودة‬".</span><span class="sxs-lookup"><span data-stu-id="08770-229">Select Yes in the Run Draft field.</span></span>

## <a name="use-an-existing-er-model-mapping-configuration"></a><span data-ttu-id="08770-230">استخدام تكوين تعيين نموذج موجود للتقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="08770-230">Use an existing ER model mapping configuration</span></span>
1. <span data-ttu-id="08770-231">في الشجرة، حدد "عينة نموذج البيانات\تنسيق نموذجي".</span><span class="sxs-lookup"><span data-stu-id="08770-231">In the tree, select 'Sample data model\Sample format'.</span></span>
2. <span data-ttu-id="08770-232">انقر فوق "تشغيل".</span><span class="sxs-lookup"><span data-stu-id="08770-232">Click Run.</span></span>
    * <span data-ttu-id="08770-233">لاحظ أنه لا يمكن تنفيذ إصدار المسودة المحدد من تكوين تنسيق التقارير الإلكترونية نظرًا لوجود أكثر من تكوين تعيين نموذج واحد متوفر لنموذج البيانات غير المحدد الذي تم تحديده كمصدر بيانات لتنسيق التقارير الإلكترونية قيد التشغيل.</span><span class="sxs-lookup"><span data-stu-id="08770-233">Note that the selected draft version of the ER format configuration can’t be executed because there is more than one model mapping configuration available for the undefined data model that has been selected as the data source of the running ER format.</span></span>   
    * <span data-ttu-id="08770-234">بعد ذلك، يمكنك تحديد تكوين تعيين نموذج بديل على غرار ذلك التكوين الذي سيتم استخدام تعيينات النموذج منه كمصادر بيانات لتنسيق التقارير الإلكترونية قيد التشغيل.</span><span class="sxs-lookup"><span data-stu-id="08770-234">Next, you will define the alternative model mapping configuration as the one from which model mappings will be used as data sources for running ER format.</span></span>   
3. <span data-ttu-id="08770-235">في الشجرة، حدد "عينة نموذج البيانات\تعيين نموذجي (بديل)".</span><span class="sxs-lookup"><span data-stu-id="08770-235">In the tree, select 'Sample data model\Sample mapping (alternative)'.</span></span>
4. <span data-ttu-id="08770-236">حدد "نعم" في حقل "الإعداد الافتراضي لتعيين النموذج‬".</span><span class="sxs-lookup"><span data-stu-id="08770-236">Select Yes in the Default for model mapping field.</span></span>
5. <span data-ttu-id="08770-237">في الشجرة، حدد "عينة نموذج البيانات\تنسيق نموذجي".</span><span class="sxs-lookup"><span data-stu-id="08770-237">In the tree, select 'Sample data model\Sample format'.</span></span>
6. <span data-ttu-id="08770-238">انقر فوق "تشغيل".</span><span class="sxs-lookup"><span data-stu-id="08770-238">Click Run.</span></span>
7. <span data-ttu-id="08770-239">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="08770-239">Click OK.</span></span>
    * <span data-ttu-id="08770-240">لاحظ أن استخدام تكوين التعيين الافتراضي يتم بواسطة تكوين التنسيق هذا لإنشاء المستند الإلكتروني (يحتوي الإخراج المنشأ على كود الشركة).</span><span class="sxs-lookup"><span data-stu-id="08770-240">Note that the default model mapping configuration is used by this format configuration for generating the electronic document (the created output contains the company code).</span></span>  

