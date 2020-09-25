---
title: إنشاء مشروع جديد
description: يقدم هذا الموضوع معلومات حول كيفية إنشاء مشروع جديد.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c8c52b8c1c86ea2f6e03cf439ba5930f1006ab4f
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760463"
---
# <a name="create-a-new-project"></a><span data-ttu-id="36121-103">إنشاء مشروع جديد</span><span class="sxs-lookup"><span data-stu-id="36121-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="36121-104">أكمل الخطوات التالية لإنشاء مشروع جديد.</span><span class="sxs-lookup"><span data-stu-id="36121-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="36121-105">في صفحة **إدارة المشاريع**، حدد **مشروع جديد**، وأدخل القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="36121-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="36121-106">**نوع المشروع:** الوقت والمواد‬</span><span class="sxs-lookup"><span data-stu-id="36121-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="36121-107">**اسم المشروع:** المرحلة 2 من ترقية XYZ</span><span class="sxs-lookup"><span data-stu-id="36121-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="36121-108">**مجموعة المشروع:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="36121-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="36121-109">**معرف عقد المشروع:** 00000002</span><span class="sxs-lookup"><span data-stu-id="36121-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="36121-110">حدد **إنشاء المشروع**.</span><span class="sxs-lookup"><span data-stu-id="36121-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="36121-111">تعيين مورد لمشروع</span><span class="sxs-lookup"><span data-stu-id="36121-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="36121-112">في صفحة **العاملون**، في قائمة **العاملون**، حدد سجل العامل الذي سبق لك إعداد الاختصاصات له، وافتح سجل العامل.</span><span class="sxs-lookup"><span data-stu-id="36121-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="36121-113">في جزء الإجراءات، على علامة تبويب **المشروع**، في المجموعة **إعداد**، حدد **تعيين المشاريع**.</span><span class="sxs-lookup"><span data-stu-id="36121-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="36121-114">في صفحة **تعيينات مشاريع التحقق من صحة المورد‬**، على علامة تبويب **المشاريع**، في الحقل **إضافة المشروع إلى مشاريع محددة**، قم بإجراء التصفية على مشروع **المرحلة 2 من ترقية XYZ**.</span><span class="sxs-lookup"><span data-stu-id="36121-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="36121-115">في جزء **المشاريع المتبقية**، حدد مشروعًا، ثم حدد زر السهم لإضافته إلى جزء **المشاريع المحددة**.</span><span class="sxs-lookup"><span data-stu-id="36121-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="36121-116">يمكنك أيضًا تعيين فئات لأحد الموارد، كما تقتضي الحاجة.</span><span class="sxs-lookup"><span data-stu-id="36121-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="36121-117">نوع الفئة هو **تكلفة** أو **إيراد**.</span><span class="sxs-lookup"><span data-stu-id="36121-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="36121-118">يتحدد نوع الفئة بواسطة مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="36121-118">The category type is determined by your organization.</span></span> <span data-ttu-id="36121-119">إذا لم يتم تعيين أي فئات للمورد، فسوف يبحث Finance عن الفئة الافتراضية على أسعار الساعة للتكلفة والإيراد.</span><span class="sxs-lookup"><span data-stu-id="36121-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="36121-120">عداد موارد المشروع وخصائص الأدوار‬</span><span class="sxs-lookup"><span data-stu-id="36121-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="36121-121">بإمكان مدير المشروع استخدام وظيفة تعيين موارد المشروع لإنشاء الأدوار المطلوبة للمشروع.</span><span class="sxs-lookup"><span data-stu-id="36121-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="36121-122">يمكن استخدام الأدوار إذا كانت الموارد المؤكدة ما زالت غير معروفة عند حجز الموارد.</span><span class="sxs-lookup"><span data-stu-id="36121-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="36121-123">يمكن عكس الأدوار بشكل مؤقت كموارد مخططة، بحيث تتمكن من متابعة مراحل تخطيط المشروع.</span><span class="sxs-lookup"><span data-stu-id="36121-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="36121-124">[![مثال لدور](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="36121-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="36121-125">**السيناريو:** تم توظيف Contoso لإكمال مشروع وقت ومواد له ميثاق مشروع معتمد.</span><span class="sxs-lookup"><span data-stu-id="36121-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="36121-126">ما زال مدير المشروع المبتدئ يعمل على إكمال نطاق المشروع.</span><span class="sxs-lookup"><span data-stu-id="36121-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="36121-127">ويعمل مدير الموارد حاليًا على تعريف الموارد المحددة التي سيتم حجزها للعمل في المشروع الجديد.</span><span class="sxs-lookup"><span data-stu-id="36121-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="36121-128">نظرًا لطبيعة المشروع الحساسة، طلبت الجهة الراعية للمشروع دور مدير مشروع أول كأحد الأدوار.</span><span class="sxs-lookup"><span data-stu-id="36121-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="36121-129">يتعيّن على مدير الموارد الحصول على المورد الجديد وتعريف الدور في النظام، إذا ما احتاج مدير المشروع المبتدئ إلى معلومات حول المورد أثناء تخطيط المشروع.</span><span class="sxs-lookup"><span data-stu-id="36121-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="36121-130">تظهر الخطوات التالية كيف يمكن لمدير الموارد إعداد دور مدير المشروع الأول وربط خصائص المورد به.</span><span class="sxs-lookup"><span data-stu-id="36121-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="36121-131">في وقت لاحق، يمكن استخدام الدور للبحث عن الموارد المتاحة التي تطابق اختصاصات المورد المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="36121-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="36121-132">في صفحة **إعداد الأدوار**، حدد **جديد**، وأدخل القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="36121-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="36121-133">**معرف الدور:** مدير مشروع أول</span><span class="sxs-lookup"><span data-stu-id="36121-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="36121-134">**الوصف:** مدير مشروع أول</span><span class="sxs-lookup"><span data-stu-id="36121-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="36121-135">حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="36121-135">Select **Create**.</span></span>
3. <span data-ttu-id="36121-136">حدد دور **مدير مشروع أول**، ثم حدد **تكوين الخصائص**.</span><span class="sxs-lookup"><span data-stu-id="36121-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="36121-137">في حقل **نوع الخاصية**، حدد **المهارة‬**.</span><span class="sxs-lookup"><span data-stu-id="36121-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="36121-138">في حقل **الخصائص المتوفرة**، أدخل نوع المهارة التي تبحث عنها.</span><span class="sxs-lookup"><span data-stu-id="36121-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="36121-139">في حقل **نوع الخاصية**، حدد **الشهادة**.</span><span class="sxs-lookup"><span data-stu-id="36121-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="36121-140">في حقل **الخصائص المتوفرة**، أدخل نوع الشهادة التي تبحث عنها.</span><span class="sxs-lookup"><span data-stu-id="36121-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="36121-141">تعيين مورد مشروع لمشروع</span><span class="sxs-lookup"><span data-stu-id="36121-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="36121-142">في صفحة **كافة المشاريع**، حدد المشروع **المرحلة 2 من ترقية XYZ**.</span><span class="sxs-lookup"><span data-stu-id="36121-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="36121-143">في علامة التبويب **فريق المشروع وجدولته**، حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="36121-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="36121-144">في حقل **الدور**، حدد **عضو الفريق**.</span><span class="sxs-lookup"><span data-stu-id="36121-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="36121-145">حدد **حجز من التقويم**.</span><span class="sxs-lookup"><span data-stu-id="36121-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="36121-146">في صفحة **توفر الموارد**، حدد **عرض الإعدادات**.</span><span class="sxs-lookup"><span data-stu-id="36121-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="36121-147">في صفحة **ضبط إعدادات العرض**، أدخل القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="36121-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="36121-148">**طريقة عرض تنسيق نطاق التاريخ:** اليوم</span><span class="sxs-lookup"><span data-stu-id="36121-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="36121-149">**عرض أوصاف التوافر:** نعم</span><span class="sxs-lookup"><span data-stu-id="36121-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="36121-150">**عرض القدرة المتبقية:** نعم</span><span class="sxs-lookup"><span data-stu-id="36121-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="36121-151">في قائمة الموارد، حدد موردًا.</span><span class="sxs-lookup"><span data-stu-id="36121-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="36121-152">حدد **حجز العمالة المحدد‬** و**قدرة كاملة**.</span><span class="sxs-lookup"><span data-stu-id="36121-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="36121-153">تعيين مورد إلى دور افتراضي</span><span class="sxs-lookup"><span data-stu-id="36121-153">Assign a resource to a default role</span></span>

<span data-ttu-id="36121-154">لمساعدة المشروع أو المورد، يستطيع المدراء التنقل لأسفل على الموارد التي يمكن حجزها لمشروع.</span><span class="sxs-lookup"><span data-stu-id="36121-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="36121-155">يمكنك إقران دور افتراضي مع مورد موجود أو مورد تم الحصول عليه مؤخرًا.</span><span class="sxs-lookup"><span data-stu-id="36121-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="36121-156">على سبيل المثال، عندما تم التعاقد مع دانيال، كان لديه الخبرة والمهارات اللازمة لملء دور محلل الأعمال.</span><span class="sxs-lookup"><span data-stu-id="36121-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="36121-157">عيّن مدير الموارد هذا الدور كدور دانيال الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="36121-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="36121-158">لذلك، إضافة إدارة الموارد دانيال إلى مجموعة من محللي الأعمال المتاحين للعمل على المشاريع.</span><span class="sxs-lookup"><span data-stu-id="36121-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="36121-159">أثناء حجز المورد، بإمكان مدراء المشاريع تصفية موارد الدور المتاحة للعمل على المشاريع.</span><span class="sxs-lookup"><span data-stu-id="36121-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="36121-160">وبإمكانهم استخدام هذه المعلومات كمعيار وحيد عند تنفيذ تحليل قرار متعدد المعايير أثناء تنفيذ المورد.</span><span class="sxs-lookup"><span data-stu-id="36121-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="36121-161">ويمكنهم أيضًا إضافة خصائص الموارد الأخرى إلى عامل التصفية للبحث عن الموارد التي تتمتع بمهارات وتعليم وخبرات معينة للعمل على مشروع محدد.</span><span class="sxs-lookup"><span data-stu-id="36121-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="36121-162">**السيناريو:** بدأ العمل على مشروع تمت الموافقة عليه، وتم حجز دور مدير المشروع القيادي كمورد مقرر في مرحلة تخطيط المشروع.</span><span class="sxs-lookup"><span data-stu-id="36121-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="36121-163">اكتسب الآن مدير الموارد موردًا لتنفيذ دور مدير المشروع القيادي.</span><span class="sxs-lookup"><span data-stu-id="36121-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="36121-164">في **قائمة الموارد**، حدد **عادل حجار**.</span><span class="sxs-lookup"><span data-stu-id="36121-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="36121-165">في صفحة **دور المورد**، حدد **جديد**، وأدخل القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="36121-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="36121-166">**السريان:** أدخل التاريخ الحالي.</span><span class="sxs-lookup"><span data-stu-id="36121-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="36121-167">**انتهاء الصلاحية:** أدخل **أبدًا‬**.</span><span class="sxs-lookup"><span data-stu-id="36121-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="36121-168">**الدور:** أدخل **مدير مشروع أول**.</span><span class="sxs-lookup"><span data-stu-id="36121-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="36121-169">حدد **حفظ** ثم قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="36121-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="36121-170">على علامة تبويب **الاختصاصات**، أضف المهارة **ProjectMgmt** والشهادة **‎PMP**.</span><span class="sxs-lookup"><span data-stu-id="36121-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>
