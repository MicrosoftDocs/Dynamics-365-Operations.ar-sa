---
title: تعمل التقارير الإلكترونية على تحميل تكوين في Lifecycle Services
description: تشرح الخطوات التالية كيف يمكن لمستخدم بدور مسؤول النظام أو مطور التقارير الإلكترونية إنشاء تكوين التقارير الإلكترونية وتحميلها داخل Microsoft Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5def757de8fb9d347f5fd0f828039dad5c989c19
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143263"
---
# <a name="er-upload-a-configuration-into-lifecycle-services"></a><span data-ttu-id="66cd4-103">تعمل التقارير الإلكترونية على تحميل تكوين في Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="66cd4-103">ER Upload a configuration into Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="66cd4-104">تشرح الخطوات التالية كيف يمكن لمستخدم بدور مسؤول النظام أو مطور التقارير الإلكترونية إنشاء تكوين التقارير الإلكترونية وتحميلها داخل Microsoft Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="66cd4-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration and upload it into Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="66cd4-105">في هذا المثال، ستقوم بإنشاء تكوين وتحميله إلى LCS لشركة نموذجية Litware, Inc. يمكن تنفيذ هذه الخطوات في أي شركة نظرًا لمشاركة تكوينات التقارير الإلكترونية بين الشركات.</span><span class="sxs-lookup"><span data-stu-id="66cd4-105">In this example, you will create a configuration and upload it to LCS for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="66cd4-106">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "إنشاء موفر تكوين ووضع علامة عليه على أنه نشط".</span><span class="sxs-lookup"><span data-stu-id="66cd4-106">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span> <span data-ttu-id="66cd4-107">يتم أيضًا الوصول إلى LCS المطلوب لإكمال هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="66cd4-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="66cd4-108">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="66cd4-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="66cd4-109">حدد ".Litware, Inc"</span><span class="sxs-lookup"><span data-stu-id="66cd4-109">Select 'Litware, Inc.'</span></span> <span data-ttu-id="66cd4-110">وقم بتعيينها كنشطة.</span><span class="sxs-lookup"><span data-stu-id="66cd4-110">and set it as active.</span></span>
3. <span data-ttu-id="66cd4-111">انقر فوق "التكوينات".</span><span class="sxs-lookup"><span data-stu-id="66cd4-111">Click Configurations.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="66cd4-112">إنشاء تكوين نموذج بيانات جديد</span><span class="sxs-lookup"><span data-stu-id="66cd4-112">Create a new data model configuration</span></span>
1. <span data-ttu-id="66cd4-113">انقر فوق "إنشاء تكوين" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="66cd4-113">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="66cd4-114">ستقوم بإنشاء تكوين يحتوي على نموذج بيانات للمستندات الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="66cd4-114">You will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="66cd4-115">سيتم تحميل تكوين نموذج البيانات هذا في LCS لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="66cd4-115">This data model configuration will be uploaded into LCS later.</span></span>  
2. <span data-ttu-id="66cd4-116">في الحقل "الاسم"، اكتب "تكوين نموذج عينة".</span><span class="sxs-lookup"><span data-stu-id="66cd4-116">In the Name field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="66cd4-117">تكوين نموذج العينة</span><span class="sxs-lookup"><span data-stu-id="66cd4-117">Sample model configuration</span></span>  
3. <span data-ttu-id="66cd4-118">في حقل "الوصف"، اكتب "تكوين نموذج العينة".</span><span class="sxs-lookup"><span data-stu-id="66cd4-118">In the Description field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="66cd4-119">تكوين نموذج العينة</span><span class="sxs-lookup"><span data-stu-id="66cd4-119">Sample model configuration</span></span>  
4. <span data-ttu-id="66cd4-120">وانقر فوق إنشاء تكوين.</span><span class="sxs-lookup"><span data-stu-id="66cd4-120">Click Create configuration.</span></span>
5. <span data-ttu-id="66cd4-121">انقر فوق "مصمم النموذج".</span><span class="sxs-lookup"><span data-stu-id="66cd4-121">Click Model designer.</span></span>
6. <span data-ttu-id="66cd4-122">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="66cd4-122">Click New.</span></span>
7. <span data-ttu-id="66cd4-123">في الحقل "الاسم"، اكتب "نقطة الإدخال".</span><span class="sxs-lookup"><span data-stu-id="66cd4-123">In the Name field, type 'Entry point'.</span></span>
    * <span data-ttu-id="66cd4-124">نقطة الإدخال</span><span class="sxs-lookup"><span data-stu-id="66cd4-124">Entry point</span></span>  
8. <span data-ttu-id="66cd4-125">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="66cd4-125">Click Add.</span></span>
9. <span data-ttu-id="66cd4-126">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="66cd4-126">Click Save.</span></span>
10. <span data-ttu-id="66cd4-127">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="66cd4-127">Close the page.</span></span>
11. <span data-ttu-id="66cd4-128">انقر فوق "تغيير الحالة".</span><span class="sxs-lookup"><span data-stu-id="66cd4-128">Click Change status.</span></span>
12. <span data-ttu-id="66cd4-129">انقر فوق "مكتمل".</span><span class="sxs-lookup"><span data-stu-id="66cd4-129">Click Complete.</span></span>
13. <span data-ttu-id="66cd4-130">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="66cd4-130">Click OK.</span></span>

## <a name="register-a-new--repository"></a><span data-ttu-id="66cd4-131">تسجيل مستودع جديد</span><span class="sxs-lookup"><span data-stu-id="66cd4-131">Register a new  repository</span></span>
1. <span data-ttu-id="66cd4-132">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="66cd4-132">Close the page.</span></span>
2. <span data-ttu-id="66cd4-133">انقر فوق "المستودعات".</span><span class="sxs-lookup"><span data-stu-id="66cd4-133">Click Repositories.</span></span>
    * <span data-ttu-id="66cd4-134">يتيح لك هذا فتح قائمة المستودعات لموفر تكوين Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="66cd4-134">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
3. <span data-ttu-id="66cd4-135">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="66cd4-135">Click Add to open the drop dialog.</span></span>
    * <span data-ttu-id="66cd4-136">هذا يسمح لك بإضافة مستودع جديد.</span><span class="sxs-lookup"><span data-stu-id="66cd4-136">This allows you to add a new repository.</span></span>  
4. <span data-ttu-id="66cd4-137">في الحقل "نوع مستودع التكوين"، اكتب LCS.</span><span class="sxs-lookup"><span data-stu-id="66cd4-137">In the Configuration repository type field, select LCS.</span></span>
5. <span data-ttu-id="66cd4-138">انقر فوق إنشاء مستودع.</span><span class="sxs-lookup"><span data-stu-id="66cd4-138">Click Create repository.</span></span>
6. <span data-ttu-id="66cd4-139">في الحقل "المشروع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="66cd4-139">In the Project field, enter or select a value.</span></span>
    * <span data-ttu-id="66cd4-140">حدد مشروع LCS المرغوب.</span><span class="sxs-lookup"><span data-stu-id="66cd4-140">Select the desired LCS project.</span></span> <span data-ttu-id="66cd4-141">يجب أن يكون لديك حق الوصول إلى المشروع.</span><span class="sxs-lookup"><span data-stu-id="66cd4-141">You must have access to the project.</span></span>  
7. <span data-ttu-id="66cd4-142">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="66cd4-142">Click OK.</span></span>
    * <span data-ttu-id="66cd4-143">أكمل إدخال مستودع جديد.</span><span class="sxs-lookup"><span data-stu-id="66cd4-143">Complete a new repository entry.</span></span>  
8. <span data-ttu-id="66cd4-144">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="66cd4-144">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="66cd4-145">حدد سجل مستودع LCS.</span><span class="sxs-lookup"><span data-stu-id="66cd4-145">Select the LCS repository record.</span></span>  
    * <span data-ttu-id="66cd4-146">لاحظ أنه يتم وضع مستودع مسجل عن طريق الموفر الحالي مما يعني أنه يمكن وضع التكوينات التي يملكها هذا الموفر فقط في هذا المستودع ونتيجة لذلك، يتم تحميلها في دائرة مشروع LCS المحدد.</span><span class="sxs-lookup"><span data-stu-id="66cd4-146">Note that a registered repository is marked by the current provider meaning that the only configurations owned by that provider can be placed to this repository and, consequently, uploaded into the selected LCS project.</span></span>  
9. <span data-ttu-id="66cd4-147">انقر فوق "فتح".</span><span class="sxs-lookup"><span data-stu-id="66cd4-147">Click Open.</span></span>
    * <span data-ttu-id="66cd4-148">افتح المستودع لعرض قائمة تكوينات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="66cd4-148">Open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="66cd4-149">سيكون فارغًا إذا كان هذا المشروع لم يتم استخدامه لمشاركة تكوينات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="66cd4-149">It will be empty if this project has not yet been used for ER configurations sharing.</span></span>  
10. <span data-ttu-id="66cd4-150">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="66cd4-150">Close the page.</span></span>
11. <span data-ttu-id="66cd4-151">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="66cd4-151">Close the page.</span></span>

## <a name="upload-configuration-into-lcs"></a><span data-ttu-id="66cd4-152">تحميل ملف داخل LCS</span><span class="sxs-lookup"><span data-stu-id="66cd4-152">Upload configuration into LCS</span></span>
1. <span data-ttu-id="66cd4-153">انقر فوق "التكوينات".</span><span class="sxs-lookup"><span data-stu-id="66cd4-153">Click Configurations.</span></span>
2. <span data-ttu-id="66cd4-154">في الشجرة، حدد "تكوين نموذج مبسط".</span><span class="sxs-lookup"><span data-stu-id="66cd4-154">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="66cd4-155">حدد التكوين المنشأ الذي تم اكتماله مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="66cd4-155">Select a created configuration that has been already completed.</span></span>  
3. <span data-ttu-id="66cd4-156">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="66cd4-156">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="66cd4-157">حدد إصدار التكوين المحدد بالحالة "مكتمل".</span><span class="sxs-lookup"><span data-stu-id="66cd4-157">Select the version of the selected configuration with the status of 'Completed'.</span></span>  
4. <span data-ttu-id="66cd4-158">انقر فوق "تغيير الحالة".</span><span class="sxs-lookup"><span data-stu-id="66cd4-158">Click Change status.</span></span>
5. <span data-ttu-id="66cd4-159">انقر فوق "مشاركة".</span><span class="sxs-lookup"><span data-stu-id="66cd4-159">Click Share.</span></span>
    * <span data-ttu-id="66cd4-160">سيتم تغيير حالة التكوين من "مكتمل" إلى "مشترك" عند نشرها في LCS.</span><span class="sxs-lookup"><span data-stu-id="66cd4-160">The configuration status will change from 'Completed' to 'Shared' when it is published in LCS.</span></span>  
6. <span data-ttu-id="66cd4-161">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="66cd4-161">Click OK.</span></span>
7. <span data-ttu-id="66cd4-162">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="66cd4-162">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="66cd4-163">حدد إصدار التكوين مع الحالة "مشترك".</span><span class="sxs-lookup"><span data-stu-id="66cd4-163">Select the configuration version with the status of 'Shared'.</span></span>  
    * <span data-ttu-id="66cd4-164">لاحظ أنه تم تغيير حالة الإصدار المحدد من "مكتملة" إلى "مشتركة".</span><span class="sxs-lookup"><span data-stu-id="66cd4-164">Note that the status of the selected version has changed from 'Completed' to 'Shared'.</span></span>  
8. <span data-ttu-id="66cd4-165">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="66cd4-165">Close the page.</span></span>
9. <span data-ttu-id="66cd4-166">انقر فوق "المستودعات".</span><span class="sxs-lookup"><span data-stu-id="66cd4-166">Click Repositories.</span></span>
    * <span data-ttu-id="66cd4-167">يتيح لك هذا فتح قائمة المستودعات لموفر تكوين Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="66cd4-167">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
10. <span data-ttu-id="66cd4-168">انقر فوق "فتح".</span><span class="sxs-lookup"><span data-stu-id="66cd4-168">Click Open.</span></span>
    * <span data-ttu-id="66cd4-169">حدد مستودع LCS وافتحه.</span><span class="sxs-lookup"><span data-stu-id="66cd4-169">Select the LCS repository and open it.</span></span>  
    * <span data-ttu-id="66cd4-170">لاحظ أنه يتم عرض التكوين المحدد كأصل مشروع LCS المحدد.</span><span class="sxs-lookup"><span data-stu-id="66cd4-170">Note that the selected configuration is shown as an asset of the selected LCS project.</span></span>  
    * <span data-ttu-id="66cd4-171">فتح LCS باستخدام https://lcs.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="66cd4-171">Open LCS using https://lcs.dynamics.com.</span></span> <span data-ttu-id="66cd4-172">افتح مشروع تم استخدامه مسبقًا لتسجيل المستودع وافتح "مكتبة الأصل" لهذا المشروع وتوسيع محتوى نوع أصل "تكوين GER" – سيتوفر تكوين التقارير الإلكترونية التي تم تحميلها.</span><span class="sxs-lookup"><span data-stu-id="66cd4-172">Open a project that was used earlier for repository registration, open the 'Asset library' of this project, and expand the content of the 'GER configuration' asset type – the uploaded ER configuration will be available.</span></span> <span data-ttu-id="66cd4-173">لاحظ أنه يمكن استيراد تكوين LCS الذي تم تحميله إلى مثيل آخر إذا كان باستطاعة الموفرين الوصول إلى مشروع LCS هذا.</span><span class="sxs-lookup"><span data-stu-id="66cd4-173">Note that the uploaded LCS configuration can be imported to another instance if providers have access to this LCS project.</span></span>  

