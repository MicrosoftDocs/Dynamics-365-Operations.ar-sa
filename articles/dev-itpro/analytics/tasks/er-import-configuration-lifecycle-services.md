--- 
title: "استيراد تكوين من Lifecycle Services للتقارير الإلكترونية (ER)"
description: "تشرح الخطوات التالية كيف يمكن لمستخدم له دور مسؤول النظام أو مطور التقارير الإلكترونية استيراد إصدار جديد من تكوين التقارير الإلكترونية من Microsoft Lifecycle Services (LCS)."
author: NickSelin
manager: AnnBe
ms.date: 05/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 9eb4f54897c84b98828c927f0f93613583fd4599
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="import-a-configuration-from-lifecycle-services-for-electronic-reporting-er"></a><span data-ttu-id="f2412-103">استيراد تكوين من Lifecycle Services للتقارير الإلكترونية (ER)</span><span class="sxs-lookup"><span data-stu-id="f2412-103">Import a configuration from Lifecycle Services for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f2412-104">تشرح الخطوات التالية كيف يمكن لمستخدم له دور مسؤول النظام أو مطور التقارير الإلكترونية استيراد إصدار جديد من تكوين التقارير الإلكترونية من Microsoft Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="f2412-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="f2412-105">في هذا المثال، ستقوم بتحديد الإصدار المطلوب من تكوين التقارير الإلكترونية واستيراده إلى الشركة النموذجية Litware, Inc. يمكن تنفيذ هذه الخطوات في أي شركة نظرًا لمشاركة تكوينات التقارير الإلكترونية بين الشركات.</span><span class="sxs-lookup"><span data-stu-id="f2412-105">In this example, you will select the desired version of the ER configuration and import it for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="f2412-106">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "تحميل تكوين التقارير الإلكترونية داخل Lifecycle Services".</span><span class="sxs-lookup"><span data-stu-id="f2412-106">To complete these steps, you must first complete the steps in the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="f2412-107">يتم أيضًا الوصول إلى LCS المطلوب لإكمال هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="f2412-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="f2412-108">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="f2412-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="f2412-109">انقر فوق "التكوينات".</span><span class="sxs-lookup"><span data-stu-id="f2412-109">Click Configurations.</span></span>

## <a name="delete-a-shared-version-of-data-model-configuration"></a><span data-ttu-id="f2412-110">حذف الإصدار المشترك من تكوين نموذج البيانات</span><span class="sxs-lookup"><span data-stu-id="f2412-110">Delete a shared version of data model configuration</span></span>
1. <span data-ttu-id="f2412-111">في الشجرة، حدد "تكوين نموذج مبسط".</span><span class="sxs-lookup"><span data-stu-id="f2412-111">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="f2412-112">تم إنشاء الإصدار الأول لتكوين طراز بيانات العينة ونشرها على LCS أثناء الإجراء "تحميل تكوين التقرير الإلكتروني داخل Life Services".</span><span class="sxs-lookup"><span data-stu-id="f2412-112">The first version of a sample data model configuration has been created and published to LCS during the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="f2412-113">في هذا الإجراء، يمكنك حذف هذا الإصدار لتكوين التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="f2412-113">In this procedure, you will delete this version of the ER configuration.</span></span> <span data-ttu-id="f2412-114">سيتم استيراد هذا الإصدار من تكوين عينة نموذج البيانات في وقت لاحق من LCS.</span><span class="sxs-lookup"><span data-stu-id="f2412-114">This version of a sample data model configuration will be imported later from LCS.</span></span>  
2. <span data-ttu-id="f2412-115">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="f2412-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f2412-116">حدد إصدار هذا التكوين الذي يكون في الحالة "مشتركة".</span><span class="sxs-lookup"><span data-stu-id="f2412-116">Select the version of this configuration that is in the ‘Shared’ status.</span></span> <span data-ttu-id="f2412-117">تشير هذه الحالة إلى أن التكوين تم نشره على LCS.</span><span class="sxs-lookup"><span data-stu-id="f2412-117">This status indicates that the configuration has been published to LCS.</span></span>  
3. <span data-ttu-id="f2412-118">انقر فوق "تغيير الحالة".</span><span class="sxs-lookup"><span data-stu-id="f2412-118">Click Change status.</span></span>
4. <span data-ttu-id="f2412-119">انقر فوق "إيقاف".</span><span class="sxs-lookup"><span data-stu-id="f2412-119">Click Discontinue.</span></span>
    * <span data-ttu-id="f2412-120">قم بتغيير حالة الإصدار المحدد من "مشترك" إلى "إيقاف" لجعله متوفرًا للحذف.</span><span class="sxs-lookup"><span data-stu-id="f2412-120">Change the status of the selected version from ‘Shared’ to ‘Discontinued’ to make it available for deletion.</span></span>  
5. <span data-ttu-id="f2412-121">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="f2412-121">Click OK.</span></span>
6. <span data-ttu-id="f2412-122">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="f2412-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f2412-123">حدد إصدار هذا التكوين الذي يحتوي على حالة "إيقاف".</span><span class="sxs-lookup"><span data-stu-id="f2412-123">Select the version of this configuration that has a status of ‘Discontinued’.</span></span>  
7. <span data-ttu-id="f2412-124">انقر فوق حذف.</span><span class="sxs-lookup"><span data-stu-id="f2412-124">Click Delete.</span></span>
8. <span data-ttu-id="f2412-125">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="f2412-125">Click Yes.</span></span>
    * <span data-ttu-id="f2412-126">لاحظ أن إصدار المسودة 2 من تكوين نموذج البيانات المحدد هو الإصدار الوحيد المتوفر.</span><span class="sxs-lookup"><span data-stu-id="f2412-126">Note that the only draft version 2 of the selected data model configuration is available.</span></span>  
9. <span data-ttu-id="f2412-127">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f2412-127">Close the page.</span></span>

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a><span data-ttu-id="f2412-128">استيراد الإصدار المشترك لتكوين نموذج البيانات من LCS</span><span class="sxs-lookup"><span data-stu-id="f2412-128">Import a shared version of data model configuration from LCS</span></span>
1. <span data-ttu-id="f2412-129">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="f2412-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="f2412-130">افتح قائمة بالمستودعات لموفر تكوين شركة ‘Litware, Inc.’</span><span class="sxs-lookup"><span data-stu-id="f2412-130">Open the list of repositories for the ‘Litware, Inc.’</span></span> <span data-ttu-id="f2412-131">موفر التكوين.</span><span class="sxs-lookup"><span data-stu-id="f2412-131">configuration provider.</span></span>  
2. <span data-ttu-id="f2412-132">انقر فوق "المستودعات".</span><span class="sxs-lookup"><span data-stu-id="f2412-132">Click Repositories.</span></span>
3. <span data-ttu-id="f2412-133">انقر فوق "فتح".</span><span class="sxs-lookup"><span data-stu-id="f2412-133">Click Open.</span></span>
    * <span data-ttu-id="f2412-134">حدد مستودع LCS وافتحه.</span><span class="sxs-lookup"><span data-stu-id="f2412-134">Select the LCS repository and open it.</span></span>  
4. <span data-ttu-id="f2412-135">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="f2412-135">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="f2412-136">حدد الإصدار الأول "لتكوين نموذج العينة" في قائمة الإصدارات.</span><span class="sxs-lookup"><span data-stu-id="f2412-136">Select the first version of the 'Sample model configuration' in the versions list.</span></span>  
5. <span data-ttu-id="f2412-137">انقر فوق "استيراد".</span><span class="sxs-lookup"><span data-stu-id="f2412-137">Click Import.</span></span>
6. <span data-ttu-id="f2412-138">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="f2412-138">Click Yes.</span></span>
    * <span data-ttu-id="f2412-139">قم بتأكيد استيراد الإصدار المحدد من LCS.</span><span class="sxs-lookup"><span data-stu-id="f2412-139">Confirm the import of the selected version from LCS .</span></span>  
    * <span data-ttu-id="f2412-140">لاحظ أن رسالة المعلومات (أعلى النموذج) تؤكد على نجاح استيراد الإصدار المحدد.</span><span class="sxs-lookup"><span data-stu-id="f2412-140">Note that the information message (above the form) confirms the successful completion of the import of the selected version.</span></span>  
7. <span data-ttu-id="f2412-141">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f2412-141">Close the page.</span></span>
8. <span data-ttu-id="f2412-142">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f2412-142">Close the page.</span></span>
9. <span data-ttu-id="f2412-143">انقر فوق "التكوينات".</span><span class="sxs-lookup"><span data-stu-id="f2412-143">Click Configurations.</span></span>
10. <span data-ttu-id="f2412-144">في الشجرة، حدد "تكوين نموذج مبسط".</span><span class="sxs-lookup"><span data-stu-id="f2412-144">In the tree, select 'Sample model configuration'.</span></span>
11. <span data-ttu-id="f2412-145">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="f2412-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f2412-146">حدد إصدار هذا التكوين الذي يحتوي على حالة "مشترك".</span><span class="sxs-lookup"><span data-stu-id="f2412-146">Select the version of this configuration that has a status of ‘Shared’.</span></span>  
    * <span data-ttu-id="f2412-147">لاحظ الإصدار المشترك 1 من تكوين نموذج البيانات المحدد متوفر هو أيضًا.</span><span class="sxs-lookup"><span data-stu-id="f2412-147">Note that the shared version 1 of the selected data model configuration is available now as well.</span></span>  


