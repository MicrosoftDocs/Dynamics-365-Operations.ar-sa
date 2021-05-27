---
title: طلبات الفئات من الموردين
description: يصف هذا الموضوع كيف يمكن للموردين طلب فئات تدبير لحسابهم. كما يصف عملية الموافقة التي يتم إكمالها بواسطة مندوبين التدبير.
author: kamaybac
ms.date: 04/19/2021
ms.topic: article
ms.search.form: VendRequestNewCategory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1951f85f84c3b8b2d42f49d5f464d90d410ebfa2
ms.sourcegitcommit: 51cad1ce3ed44ebf7eb9bdf553ee2df4c1f03135
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/10/2021
ms.locfileid: "6015941"
---
# <a name="category-requests-from-vendors"></a><span data-ttu-id="ade72-104">طلبات الفئات من الموردين</span><span class="sxs-lookup"><span data-stu-id="ade72-104">Category requests from vendors</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ade72-105">تتيح عملية طلب الفئة للموردين طلب ربط فئات تدبير جديدة بحساباتهم.</span><span class="sxs-lookup"><span data-stu-id="ade72-105">The category request process lets vendors request that new procurement categories be associated with their account.</span></span> <span data-ttu-id="ade72-106">يمكن بعد ذلك استخدام فئات التدبير هذه من خلال عمليات التدبير وتحديد الموارد ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="ade72-106">Those procurement categories can then be used by the related procurement and sourcing processes.</span></span> <span data-ttu-id="ade72-107">(لمزيد من المعلومات، راجع [نظرة عامة على فئات التدبير](procurement-catalogs.md).)</span><span class="sxs-lookup"><span data-stu-id="ade72-107">(For more information, see [Procurement catalogs overview](procurement-catalogs.md).)</span></span>

<span data-ttu-id="ade72-108">يتم بدء طلبات الفئات بواسطة الموردين في مساحة عمل **معلومات المورد**.</span><span class="sxs-lookup"><span data-stu-id="ade72-108">Category requests are initiated by vendors in the **Vendor information** workspace.</span></span> <span data-ttu-id="ade72-109">ويتم بعد ذلك إرسالها إلى وكالتك للمراجعة والموافقة.</span><span class="sxs-lookup"><span data-stu-id="ade72-109">They are then submitted to your agency for review and approval.</span></span> <span data-ttu-id="ade72-110">تتم إضافة الفئات المعتمدة إلى قائمة فئات التدبير لحساب المورد.</span><span class="sxs-lookup"><span data-stu-id="ade72-110">Approved categories are added to the list of procurement categories for the vendor's account.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="ade72-111">تشغيل الميزة في النظام</span><span class="sxs-lookup"><span data-stu-id="ade72-111">Turn on the feature in your system</span></span>

<span data-ttu-id="ade72-112">إذا لم يتضمن نظامك بالفعل الميزة الموضحة في هذا الموضوع ، فانتقل إلى [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)، وقم بتشغيل ميزة *السماح للموردين بالتقدم بطلب للحصول على فئات التدبير من خلال تعاون الموردين*.</span><span class="sxs-lookup"><span data-stu-id="ade72-112">If your system doesn't already include the feature that is described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Allow vendors to apply for procurement categories through vendor collaboration* feature.</span></span>

<span data-ttu-id="ade72-113">بعد تشغيل الميزة ، لا يزال بإمكانك إضافة فئات تدبير يدويًا إلى حسابات الموردين.</span><span class="sxs-lookup"><span data-stu-id="ade72-113">After the feature is turned on, you can still manually add procurement categories to vendor accounts.</span></span> <span data-ttu-id="ade72-114">لمزيد من المعلومات، راجع [الموافقة على الموردين لفئات تدبير محددة](tasks/approve-vendors-specific-procurement-categories.md).</span><span class="sxs-lookup"><span data-stu-id="ade72-114">For information, see [Approve vendors for specific procurement categories](tasks/approve-vendors-specific-procurement-categories.md).</span></span>

## <a name="vendor-collaboration-requirements"></a><span data-ttu-id="ade72-115">متطلبات تعاون الموردين</span><span class="sxs-lookup"><span data-stu-id="ade72-115">Vendor collaboration requirements</span></span>

<span data-ttu-id="ade72-116">قبل أن يتمكن المورد من التفاعل مع طلبات الفئات ، يجب إعداده لتعاون المورد.</span><span class="sxs-lookup"><span data-stu-id="ade72-116">Before a vendor can interact with category requests, it must be set up for vendor collaboration.</span></span>

<span data-ttu-id="ade72-117">يجب أن يكون لدى المورد مستخدم واحد على الأقل لتعاون المورد.</span><span class="sxs-lookup"><span data-stu-id="ade72-117">The vendor must have at least one vendor collaboration user.</span></span> <span data-ttu-id="ade72-118">يمكن فقط لمستخدمي المورد الذين لديهم دور أمان *مسؤول المورد (خارجي)* إنشاء طلبات الفئات وإرسالها.</span><span class="sxs-lookup"><span data-stu-id="ade72-118">Only vendor users with the *Vendor admin (external)* security role can create and submit category requests.</span></span>

<span data-ttu-id="ade72-119">لمزيد من المعلومات، راجع [إعداد وصيانة تعاون المورّد](set-up-maintain-vendor-collaboration.md).</span><span class="sxs-lookup"><span data-stu-id="ade72-119">For more information, see [Set up and maintain vendor collaboration](set-up-maintain-vendor-collaboration.md).</span></span>

## <a name="set-up-the-vendor-category-request-workflow"></a><span data-ttu-id="ade72-120">إعداد سير عمل طلب فئة المورد</span><span class="sxs-lookup"><span data-stu-id="ade72-120">Set up the Vendor category request workflow</span></span>

<span data-ttu-id="ade72-121">يجب إعداد سير عمل *طلب فئة المورد* في عمليات سير عمل التدبير وتحديد الموارد.</span><span class="sxs-lookup"><span data-stu-id="ade72-121">The *Vendor category request* workflow must be set up in the procurement and sourcing workflows.</span></span> <span data-ttu-id="ade72-122">سيقوم الموردون بإرسال طلبات فئات جديدة يمكنك مراجعتها والموافقة عليها.</span><span class="sxs-lookup"><span data-stu-id="ade72-122">Vendors will submit new category requests that you can review and approve.</span></span> <span data-ttu-id="ade72-123">تتم إضافة فئات التدبير المطلوبة إلى حساب المورّد بعد الموافقة على طلب الفئة.</span><span class="sxs-lookup"><span data-stu-id="ade72-123">Requested procurement categories are added to a vendor account after a category request is approved.</span></span>

<span data-ttu-id="ade72-124">يوضح المثال التالي كيفية إعداد سير عمل *طلب فئة المورد* التي تشتمل على معتمد واحد.</span><span class="sxs-lookup"><span data-stu-id="ade72-124">The following example shows how to set up a simple *Vendor category request* workflow that has a single approver.</span></span> <span data-ttu-id="ade72-125">يجب عليك مراجعة عملياتك الداخلية لتحديد إعداد سير العمل المناسب لوكالتك.</span><span class="sxs-lookup"><span data-stu-id="ade72-125">You must review your internal processes to determine the appropriate workflow setup for your agency.</span></span>

1. <span data-ttu-id="ade72-126">انتقل إلى **التدبير والتوريد‬ \> الإعداد \> عمليات سير عمل التدبير والتوريد**.</span><span class="sxs-lookup"><span data-stu-id="ade72-126">Go to **Procurement and sourcing \> Setup \> Procurement and sourcing workflows**.</span></span>
1. <span data-ttu-id="ade72-127">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="ade72-127">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="ade72-128">في مربع الحوار، حدد **سير عمل طلب فئة المورد** لفتح محرر سير العمل.</span><span class="sxs-lookup"><span data-stu-id="ade72-128">In the dialog box, select **Vendor category request workflow** to open the workflow editor.</span></span>
1. <span data-ttu-id="ade72-129">قم بتسجيل الدخول إلى محرر سير العمل.</span><span class="sxs-lookup"><span data-stu-id="ade72-129">Sign in to the workflow editor.</span></span>
1. <span data-ttu-id="ade72-130">في "جزء الإجراءات"، حدد **الخصائص**.</span><span class="sxs-lookup"><span data-stu-id="ade72-130">On the Action Pane, select **Properties**.</span></span>
1. <span data-ttu-id="ade72-131">في صفحة **الخصائص** لسير العمل، في حقل **تعليمات الإرسال**، أدخل نص التعليمات.</span><span class="sxs-lookup"><span data-stu-id="ade72-131">On the **Properties** page for the workflow, in the **Submission instructions** field, enter instruction text.</span></span> <span data-ttu-id="ade72-132">ستكون التعليمات مرئية للموردين عند قيامهم بإرسال طلب فئة.</span><span class="sxs-lookup"><span data-stu-id="ade72-132">The instructions will be visible to vendors when they submit a category request.</span></span>
1. <span data-ttu-id="ade72-133">أغلق صفحة **الخصائص**.</span><span class="sxs-lookup"><span data-stu-id="ade72-133">Close the **Properties** page.</span></span>
1. <span data-ttu-id="ade72-134">اسحب عنصر سير عمل **الموافقة على طلب الفئة الجديدة** على اللوحة.</span><span class="sxs-lookup"><span data-stu-id="ade72-134">Drag the **Approve new category request** workflow element onto the canvas.</span></span>
1. <span data-ttu-id="ade72-135">اسحب ارتباطًا من عنصر سير عمل **البدء** إلى عنصر سير عمل **الموافقة على طلب الفئة الجديد**.</span><span class="sxs-lookup"><span data-stu-id="ade72-135">Drag a link from the **Start** workflow element to the **Approve new category request** workflow element.</span></span>
1. <span data-ttu-id="ade72-136">اسحب ارتباطًا من عنصر سير عمل **الموافقة على طلب الفئة الجديد** إلى عنصر سير عمل **الإنهاء**.</span><span class="sxs-lookup"><span data-stu-id="ade72-136">Drag a link from the **Approve new category request** workflow element to the **End** workflow element.</span></span>
1. <span data-ttu-id="ade72-137">اضغط ضغطًا مزدوجًا (أو انقر نقرًا مزدوجًا) فوق عنصر سير عمل **الموافقة على طلب الفئة الجديد**.</span><span class="sxs-lookup"><span data-stu-id="ade72-137">Double-tap (or double-click) the **Approve new category request** workflow element.</span></span>
1. <span data-ttu-id="ade72-138">حدد واضغط (أو انقر بزر الماوس الأيمن) على عنصر سير عمل **الخطوة 1**، ثم حدد **الخصائص**.</span><span class="sxs-lookup"><span data-stu-id="ade72-138">Select and hold (or right-click) the **Step 1** workflow element, and then select **Properties**.</span></span>
1. <span data-ttu-id="ade72-139">في صفحة **الخصائص** لعنصر سير العمل، في حقل **موضوع عنصر العمل**، أدخل نص الموضوع.</span><span class="sxs-lookup"><span data-stu-id="ade72-139">On the **Properties** page for the workflow element, in the **Work item subject** field, enter subject text.</span></span> <span data-ttu-id="ade72-140">سيظهر هذا النص كقيمة حقل **الموضوع** في صفحة **عناصر العمل المعينة لي**.</span><span class="sxs-lookup"><span data-stu-id="ade72-140">This text will be shown as the value of the **Subject** field on the **Work items assigned to me** page.</span></span>
1. <span data-ttu-id="ade72-141">في حقل **تعليمات عنصر العمل**، أدخل نص التعليمات.</span><span class="sxs-lookup"><span data-stu-id="ade72-141">In the **Work item instructions** field, enter instruction text.</span></span> <span data-ttu-id="ade72-142">ستكون التعليمات مرئية للموافقين عند تحديد **سير العمل** في جزء الإجراءات الخاص بطلب الفئة.</span><span class="sxs-lookup"><span data-stu-id="ade72-142">The instructions will be visible to approvers when they select **Workflow** on the Action Pane of a category request.</span></span>
1. <span data-ttu-id="ade72-143">في الجزء الأيمن، حدد **التعيين**.</span><span class="sxs-lookup"><span data-stu-id="ade72-143">In the left pane, select **Assignment**.</span></span>
1. <span data-ttu-id="ade72-144">في علامة التبويب **نوع التعيين**، قم بتعيين **تعيين مستخدمين لعنصر سير العمل هذا** إلى *المستخدم*.</span><span class="sxs-lookup"><span data-stu-id="ade72-144">On the **Assignment type** tab, set **Assign users to this workflow element** to *User*.</span></span>
1. <span data-ttu-id="ade72-145">في علامة تبويب **المستخدم**، في قائمة **المستخدمين المتوفرين**، حدد موافقًا.</span><span class="sxs-lookup"><span data-stu-id="ade72-145">On the **User** tab, in the **Available users** list, select an approver.</span></span> <span data-ttu-id="ade72-146">على سبيل المثال، حدد مستخدمًا في قسم التدبير.</span><span class="sxs-lookup"><span data-stu-id="ade72-146">For example, select a user in the Procurement department.</span></span>
1. <span data-ttu-id="ade72-147">حدد زر السهم الأيمن (**\>**) لنقل المعتمد إلى قائمة **المستخدمين المحددين**.</span><span class="sxs-lookup"><span data-stu-id="ade72-147">Select the right arrow button (**\>**) to move the approver to the **Selected users** list.</span></span>
1. <span data-ttu-id="ade72-148">أغلق صفحة **الخصائص**.</span><span class="sxs-lookup"><span data-stu-id="ade72-148">Close the **Properties** page.</span></span>
1. <span data-ttu-id="ade72-149">حدد **حفظ وإغلاق**.</span><span class="sxs-lookup"><span data-stu-id="ade72-149">Select **Save and close**.</span></span>
1. <span data-ttu-id="ade72-150">في حقل **ملاحظات الإصدار**، أدخل ملاحظات حول سير العمل.</span><span class="sxs-lookup"><span data-stu-id="ade72-150">In the **Version notes** field, enter notes about the workflow.</span></span>
1. <span data-ttu-id="ade72-151">حدد **موافق** لحفظ سير العمل.</span><span class="sxs-lookup"><span data-stu-id="ade72-151">Select **OK** to save the workflow.</span></span>
1. <span data-ttu-id="ade72-152">إذا كنت مستعدًا لبدء اختبار سير العمل، حدد **تنشيط الإصدار الجديد**.</span><span class="sxs-lookup"><span data-stu-id="ade72-152">If you're ready to start to test the workflow, select **Activate the new version**.</span></span> <span data-ttu-id="ade72-153">بخلاف ذلك، حدد **عدم تنشيط الإصدار الجديد**.</span><span class="sxs-lookup"><span data-stu-id="ade72-153">Otherwise, select **Do not activate the new version**.</span></span>
1. <span data-ttu-id="ade72-154">حدد **موافق** لإكمال إعداد سير العمل.</span><span class="sxs-lookup"><span data-stu-id="ade72-154">Select **OK** to complete the workflow setup.</span></span>

> [!TIP]
> <span data-ttu-id="ade72-155">إذا كانت وكالتك لا تتطلب الموافقة على طلبات الفئات، فيجب عليك تكوين سير العمل للموافقة التلقائية.</span><span class="sxs-lookup"><span data-stu-id="ade72-155">If your agency doesn't require approval of category requests, you should configure the workflow for automatic approval.</span></span>

<span data-ttu-id="ade72-156">لمزيد من المعلومات حول كيفية إعداد عمليات سير العمل، راجع [نظرة عامة حول نظام سير العمل](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md).</span><span class="sxs-lookup"><span data-stu-id="ade72-156">For more information about how to set up workflows, see [Workflow system overview](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md).</span></span>

## <a name="create-and-submit-a-category-request"></a><span data-ttu-id="ade72-157">إنشاء طلب فئة وإرساله</span><span class="sxs-lookup"><span data-stu-id="ade72-157">Create and submit a category request</span></span>

<span data-ttu-id="ade72-158">يصف هذا القسم كيفية قيام الموردين باستخدام مساحة عمل **معلومات المورد** لإنشاء طلبات الفئات وتحريرها وعرضها وإرسالها.</span><span class="sxs-lookup"><span data-stu-id="ade72-158">This section describes how vendors can use the **Vendor information** workspace to create, edit, view, and submit category requests.</span></span>

### <a name="start-a-new-request"></a><span data-ttu-id="ade72-159">بدء طلب جديد</span><span class="sxs-lookup"><span data-stu-id="ade72-159">Start a new request</span></span>

<span data-ttu-id="ade72-160">لبدء طلب فئة جديد، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="ade72-160">To start a new category request, follow these steps.</span></span>

1. <span data-ttu-id="ade72-161">في مساحة عمل **معلومات المورد**، حدد تجانب **طلبات الفئات**.</span><span class="sxs-lookup"><span data-stu-id="ade72-161">In the **Vendor information** workspace, select the **Category requests** tile.</span></span>
1. <span data-ttu-id="ade72-162">في صفحة **طلبات الفئات**، في جزء الإجراء، حدد **طلب فئة جديد**.</span><span class="sxs-lookup"><span data-stu-id="ade72-162">On the **Category requests** page, on the Action Pane, select **New category request**.</span></span>
1. <span data-ttu-id="ade72-163">في مربع حوار **طلب فئة جديد**، ابحث عن الفئة التي تريد تطبيقها لها من خلال التنقل في الشجرة و/أو استخدام عامل التصفية في أعلى القائمة.</span><span class="sxs-lookup"><span data-stu-id="ade72-163">In the **New category request** dialog box, find the category that you want to apply for by navigating the tree and/or using the filter at the top of the list.</span></span> <span data-ttu-id="ade72-164">حدد خانة الاختيار لكل فئة ذات صلة.</span><span class="sxs-lookup"><span data-stu-id="ade72-164">Select the checkbox for each relevant category.</span></span>

    <span data-ttu-id="ade72-165">لاحظ النقاط التالية:</span><span class="sxs-lookup"><span data-stu-id="ade72-165">Note the following points:</span></span>

    - <span data-ttu-id="ade72-166">يتم عرض الفئات النشطة حاليًا في حساب المورد الخاص بك على أنها محددة ولا يمكن إزالتها.</span><span class="sxs-lookup"><span data-stu-id="ade72-166">Categories that are currently active on your vendor account are shown as selected and can't be removed.</span></span>
    - <span data-ttu-id="ade72-167">يمكنك طلب فئات تدبير متعددة في طلب فئة واحد.</span><span class="sxs-lookup"><span data-stu-id="ade72-167">You can request multiple procurement categories in a single category request.</span></span>

1. <span data-ttu-id="ade72-168">حدد **موافق** لإنشاء طلب المسودة.</span><span class="sxs-lookup"><span data-stu-id="ade72-168">Select **OK** to create the draft request.</span></span>

    <span data-ttu-id="ade72-169">يظهر الآن طلب مسودة جديد في صفحة **طلبات الفئات**.</span><span class="sxs-lookup"><span data-stu-id="ade72-169">The new draft request now appears on the **Category requests** page.</span></span>

1. <span data-ttu-id="ade72-170">افتح طلب المسودة الجديد لمراجعته وتحريره كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="ade72-170">Open the new draft request to review and edit it as required.</span></span>

    - <span data-ttu-id="ade72-171">لعرض قائمة الفئات المضمنة حاليًا في الطلب، حدد علامة التبويب السريع **الفئات المطلوبة**.</span><span class="sxs-lookup"><span data-stu-id="ade72-171">To view the list of categories that are currently included in the request, select the **Requested categories** FastTab.</span></span>
    - <span data-ttu-id="ade72-172">لعرض الفئات النشطة، افتح مربع الحقائق **الفئات النشطة** على الجانب الأيسر من الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ade72-172">To view your active categories, open the **Active categories** FactBox on the right side of the page.</span></span>
    - <span data-ttu-id="ade72-173">لإضافة فئة للطلب، حدد **إضافة** من شريط الأدوات في علامة التبويب السريع **الفئات المطلوبة**.</span><span class="sxs-lookup"><span data-stu-id="ade72-173">To add a category to the request, select **Add** on the toolbar on the **Requested categories** FastTab.</span></span>
    - <span data-ttu-id="ade72-174">لإزالة فئة من الطلب، حدد الفئة في علامة التبويب السريع **الفئات المطلوبة**، ثم حدد **إزالة** على شريط الأدوات.</span><span class="sxs-lookup"><span data-stu-id="ade72-174">To remove a category from the request, select the category on the **Requested categories** FastTab, and then select **Remove** on the toolbar.</span></span>
    - <span data-ttu-id="ade72-175">لإرفاق مستند بالطلب، حدد **المرفقات** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="ade72-175">To attach a document to the request, select **Attachments** on the Action Pane.</span></span> <span data-ttu-id="ade72-176">ستكون المستندات المرفقة متوفرة للموافقين عند مراجعتهم طلب الفئة.</span><span class="sxs-lookup"><span data-stu-id="ade72-176">Attached documents will be available to approvers when they review the category request.</span></span>
    - <span data-ttu-id="ade72-177">لإزالة مستند مرفق من الطلب، حدد **المرفقات** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="ade72-177">To remove an attached document from the request, select **Attachments** on the Action Pane.</span></span> <span data-ttu-id="ade72-178">حدد المستند المراد إزالته، ثم حدد **حذف** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="ade72-178">Select the document to remove, and then select **Delete** on the Action Pane.</span></span>

1. <span data-ttu-id="ade72-179">إذا كنت مستعدًا لإرسال الطلب، فحدد **إرسال** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="ade72-179">If you're ready to submit the request, select **Submit** on the Action Pane.</span></span> <span data-ttu-id="ade72-180">بخلاف ذلك، ما عليك سوى إغلاق الصفحة وتخطي الخطوات المتبقية لهذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="ade72-180">Otherwise, just close the page and skip the remaining steps of this procedure.</span></span> <span data-ttu-id="ade72-181">يمكنك بعد ذلك الرجوع إلى الطلب فيما بعد.</span><span class="sxs-lookup"><span data-stu-id="ade72-181">You can then return to the request later.</span></span>
1. <span data-ttu-id="ade72-182">اقرأ أيًّا من تعليمات الإرسال التي تظهر، ثم حدد **إرسال**.</span><span class="sxs-lookup"><span data-stu-id="ade72-182">Read any submission instructions that appear, and then select **Submit**.</span></span>
1. <span data-ttu-id="ade72-183">في مربع **التعليق**، أدخل أي معلومات إضافية مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="ade72-183">In the **Comment** box, enter any additional information that is required.</span></span> <span data-ttu-id="ade72-184">وحدد بعد ذلك **إرسال** لإكمال الطلب.</span><span class="sxs-lookup"><span data-stu-id="ade72-184">Then select **Submit** to complete the request.</span></span>

### <a name="edit-a-draft-or-recalled-request"></a><span data-ttu-id="ade72-185">تحرير مسودة أو طلب مسترجع</span><span class="sxs-lookup"><span data-stu-id="ade72-185">Edit a draft or recalled request</span></span>

<span data-ttu-id="ade72-186">لتحرير طلب فئة مسودة أو تم استدعاؤه، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="ade72-186">To edit a draft or recalled category request, follow these steps.</span></span>

1. <span data-ttu-id="ade72-187">في مساحة عمل **معلومات المورد**، حدد تجانب **طلبات الفئات**.</span><span class="sxs-lookup"><span data-stu-id="ade72-187">In the **Vendor information** workspace, select the **Category requests** tile.</span></span>
1. <span data-ttu-id="ade72-188">حدد طلب المسودة أو الذي تم استدعاؤه لفتحه.</span><span class="sxs-lookup"><span data-stu-id="ade72-188">Select the draft or recalled request to open it.</span></span>
1. <span data-ttu-id="ade72-189">قم بتحرير الطلب كما هو مطلوب ، ثم قم بإغلاقه أو إرساله كما هو موضح في الإجراء السابق.</span><span class="sxs-lookup"><span data-stu-id="ade72-189">Edit the request as required, and then either close it or submit it as described in the previous procedure.</span></span>

### <a name="submit-a-draft-or-recalled-request"></a><span data-ttu-id="ade72-190">إرسال طلب مسودة أو تم استدعاؤه</span><span class="sxs-lookup"><span data-stu-id="ade72-190">Submit a draft or recalled request</span></span>

<span data-ttu-id="ade72-191">لإرسال طلب فئة مسودة أو تم استدعاؤه، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="ade72-191">To submit a draft or recalled category request, follow these steps.</span></span>

1. <span data-ttu-id="ade72-192">في مساحة عمل **معلومات المورد**، حدد تجانب **طلبات الفئات**.</span><span class="sxs-lookup"><span data-stu-id="ade72-192">In the **Vendor information** workspace, select the **Category requests** tile.</span></span>
1. <span data-ttu-id="ade72-193">حدد الطلب المسودة أو الذي تم استدعاؤها والذي ترغب في إرساله.</span><span class="sxs-lookup"><span data-stu-id="ade72-193">Select the draft or recalled request that you want to submit.</span></span>
1. <span data-ttu-id="ade72-194">في "جزء الإجراءات"، حدد **إرسال**.</span><span class="sxs-lookup"><span data-stu-id="ade72-194">On the Action Pane, select **Submit**.</span></span>
1. <span data-ttu-id="ade72-195">اقرأ أيًّا من تعليمات الإرسال التي تظهر، ثم حدد **إرسال**.</span><span class="sxs-lookup"><span data-stu-id="ade72-195">Read any submission instructions that appear, and then select **Submit**.</span></span>
1. <span data-ttu-id="ade72-196">في مربع **التعليق**، أدخل أي معلومات إضافية مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="ade72-196">In the **Comment** box, enter any additional information that is required.</span></span> <span data-ttu-id="ade72-197">وحدد بعد ذلك **إرسال** لإكمال الطلب.</span><span class="sxs-lookup"><span data-stu-id="ade72-197">Then select **Submit** to complete the request.</span></span>

    <span data-ttu-id="ade72-198">يتم تغيير حالة طلب الفئة إلى إحدى القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="ade72-198">The status of the category request is changed to one of the following values:</span></span>

    - <span data-ttu-id="ade72-199">_مراجعة معلقة‬_ – الطلب موجود في سير العمل.</span><span class="sxs-lookup"><span data-stu-id="ade72-199">_Pending review_ – The request is in the workflow.</span></span>
    - <span data-ttu-id="ade72-200">_في انتظار الموافقة_ – الموافقة مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="ade72-200">_Pending approval_ – Approval is required.</span></span>

### <a name="recall-a-submitted-request-that-hasnt-yet-been-approved"></a><span data-ttu-id="ade72-201">استدعاء طلب مرسل لم تتم الموافقة عليه بعد</span><span class="sxs-lookup"><span data-stu-id="ade72-201">Recall a submitted request that hasn't yet been approved</span></span>

<span data-ttu-id="ade72-202">لاستدعاء طلب فئة تم إرساله ولكن لم تتم الموافقة عليه بعد ، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="ade72-202">To recall a category request that has been submitted but hasn't yet been approved, follow these steps.</span></span>

1. <span data-ttu-id="ade72-203">في مساحة عمل **معلومات المورد**، حدد تجانب **طلبات الفئات**.</span><span class="sxs-lookup"><span data-stu-id="ade72-203">In the **Vendor information** workspace, select the **Category requests** tile.</span></span>
1. <span data-ttu-id="ade72-204">حدد الطلب المعلق الذي تريد استدعاؤه.</span><span class="sxs-lookup"><span data-stu-id="ade72-204">Select the pending request that you want to recall.</span></span>
1. <span data-ttu-id="ade72-205">في "جزء الإجراءات"، حدد **استدعاء**.</span><span class="sxs-lookup"><span data-stu-id="ade72-205">On the Action Pane, select **Recall**.</span></span>
1. <span data-ttu-id="ade72-206">في مربع **إدخال تعليق**، أدخل أي معلومات إضافية مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="ade72-206">In the **Enter a comment** box, enter any additional information that is required.</span></span> <span data-ttu-id="ade72-207">وحدد بعد ذلك **إرسال** لإكمال الطلب.</span><span class="sxs-lookup"><span data-stu-id="ade72-207">Then select **Submit** to complete the request.</span></span>

    <span data-ttu-id="ade72-208">تم تغيير حالة طلب الفئة إلى _ملغى_.</span><span class="sxs-lookup"><span data-stu-id="ade72-208">The status of the category request is changed to _Canceled_.</span></span> <span data-ttu-id="ade72-209">سيبقى الطلب بهذه الحالة حتى تقوم بحذفه أو إعادة إرساله.</span><span class="sxs-lookup"><span data-stu-id="ade72-209">The request will remain in this status until you delete or resubmit it.</span></span>

### <a name="delete-a-draft-or-recalled-request"></a><span data-ttu-id="ade72-210">حذف طلب مسودة أو تم استدعاؤه</span><span class="sxs-lookup"><span data-stu-id="ade72-210">Delete a draft or recalled request</span></span>

<span data-ttu-id="ade72-211">لحذف طلب فئة مسودة أو تم استدعاؤه، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="ade72-211">To delete a draft or recalled category request, follow these steps.</span></span>

1. <span data-ttu-id="ade72-212">في مساحة عمل **معلومات المورد**، حدد تجانب **طلبات الفئات**.</span><span class="sxs-lookup"><span data-stu-id="ade72-212">In the **Vendor information** workspace, select the **Category requests** tile.</span></span>
1. <span data-ttu-id="ade72-213">حدد الطلب المسودة أو الذي تم استدعاؤها والذي ترغب في حذفه.</span><span class="sxs-lookup"><span data-stu-id="ade72-213">Select the draft or recalled request that you want to delete.</span></span>
1. <span data-ttu-id="ade72-214">في جزء الإجراءات، حدد **حذف**.</span><span class="sxs-lookup"><span data-stu-id="ade72-214">On the Action Pane, select **Delete**.</span></span>
1. <span data-ttu-id="ade72-215">حدد **نعم** لتأكيد الحذف.</span><span class="sxs-lookup"><span data-stu-id="ade72-215">Select **Yes** to confirm the deletion.</span></span>

### <a name="view-completed-requests"></a><span data-ttu-id="ade72-216">عرض الطلبات المكتملة</span><span class="sxs-lookup"><span data-stu-id="ade72-216">View completed requests</span></span>

<span data-ttu-id="ade72-217">لعرض الطلبات المكتملة ، افتح مساحة عمل **معلومات المورد** وحدد تجانب **طلبات الفئات**.</span><span class="sxs-lookup"><span data-stu-id="ade72-217">To view completed requests, open the **Vendor information** workspace and select the **Category requests** tile.</span></span> <span data-ttu-id="ade72-218">ستكون لطلبات الفئات التي تم إكمالها إحدى الحالات التالية:</span><span class="sxs-lookup"><span data-stu-id="ade72-218">Category requests that have been completed will have one of the following statuses:</span></span>

- <span data-ttu-id="ade72-219">_تمت الموافقة_ – تمت الموافقة على الطلب.</span><span class="sxs-lookup"><span data-stu-id="ade72-219">_Approved_ – The request was approved.</span></span> <span data-ttu-id="ade72-220">لعرض الفئات المضافة حديثًا، قم بالرجوع إلى مساحة عمل **معلومات المورد**، ثم افتح القائمة المنسدلة **مزيد من التفاصيل** في الجزء الأيمن، ثم حدد **الفئات**.</span><span class="sxs-lookup"><span data-stu-id="ade72-220">To view the newly added categories, go back to the **Vendor information** workspace, open the **More details** drop-down list in the left pane, and then select **Categories**.</span></span>
- <span data-ttu-id="ade72-221">_تم الرفض_ – تم رفض الطلب.</span><span class="sxs-lookup"><span data-stu-id="ade72-221">_Rejected_ – The request was rejected.</span></span> <span data-ttu-id="ade72-222">يمكنك إنشاء طلب فئة جديد كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="ade72-222">You can create a new category request as required.</span></span>

## <a name="review-category-requests"></a><span data-ttu-id="ade72-223">مراجعة طلبات الفئات</span><span class="sxs-lookup"><span data-stu-id="ade72-223">Review category requests</span></span>

<span data-ttu-id="ade72-224">يشرح هذا القسم كيفية الموافقة على طلبات الفئات التي أرسلها المورّدون ورفضها وتفويضها، وكيفية عرض الطلبات المكتملة.</span><span class="sxs-lookup"><span data-stu-id="ade72-224">This section explains how to approve, reject, and delegate category requests that vendors submitted, and how to view completed requests.</span></span> <span data-ttu-id="ade72-225">إجراءات سير العمل هذه مخصصة لطلب الفئة بالكامل.</span><span class="sxs-lookup"><span data-stu-id="ade72-225">These workflow actions are for the whole category request.</span></span>

### <a name="view-category-requests"></a><span data-ttu-id="ade72-226">عرض طلبات الفئات</span><span class="sxs-lookup"><span data-stu-id="ade72-226">View category requests</span></span>

<span data-ttu-id="ade72-227">لعرض طلبات الفئات، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="ade72-227">To view category requests, follow these steps.</span></span>

1. <span data-ttu-id="ade72-228">انتقل إلى **التدبير والتوريد \> الموردين \> طلبات تعاون الموردين \> طلبات الفئات**.</span><span class="sxs-lookup"><span data-stu-id="ade72-228">Go to **Procurement and sourcing \> Vendors \> Vendor collaboration requests \> Category requests**.</span></span>

    <span data-ttu-id="ade72-229">تظهر صفحة **طلبات الفئات**.</span><span class="sxs-lookup"><span data-stu-id="ade72-229">The **Category requests** page appears.</span></span> <span data-ttu-id="ade72-230">تُظهر طريقة عرض الصفحة الافتراضية طلبات الفئات التي لها حالة *إجراء معلق*.</span><span class="sxs-lookup"><span data-stu-id="ade72-230">The default page view shows category requests that have a status of *Pending action*.</span></span>

1. <span data-ttu-id="ade72-231">لعرض كل الطلبات، حدد *الكل* في حقل **إظهار الطلبات**.</span><span class="sxs-lookup"><span data-stu-id="ade72-231">To view all requests, select *All* in the **Show requests** field.</span></span>
1. <span data-ttu-id="ade72-232">افتح طلبًا لمراجعته وتحريره كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="ade72-232">Open a request to review and edit it as required.</span></span>

    - <span data-ttu-id="ade72-233">لعرض قائمة الفئات المضمنة حاليًا في الطلب، حدد علامة التبويب السريع **الفئات المطلوبة**.</span><span class="sxs-lookup"><span data-stu-id="ade72-233">To view the list of categories that are currently included in the request, select the **Requested categories** FastTab.</span></span>
    - <span data-ttu-id="ade72-234">لعرض الفئات النشطة، افتح مربع الحقائق **الفئات النشطة** على الجانب الأيسر من الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ade72-234">To view the active categories, open the **Active categories** FactBox on the right side of the page.</span></span>
    - <span data-ttu-id="ade72-235">في حالة إرسال المستندات، يعرض زر **المرفقات** (مشبك الورق) في جزء الإجراءات، يُظهر عدد المستندات المرفقة.</span><span class="sxs-lookup"><span data-stu-id="ade72-235">If documents were submitted, the  **Attachments** (paper clip) button on the Action Pane shows a count of the attached documents.</span></span> <span data-ttu-id="ade72-236">لعرض المستندات المرفقة، حدد زر **المرفقات**.</span><span class="sxs-lookup"><span data-stu-id="ade72-236">To view attached documents, select the **Attachments** button.</span></span> <span data-ttu-id="ade72-237">حدد بعد ذلك المستند المراد عرضه وحدد **فتح** لعرضه.</span><span class="sxs-lookup"><span data-stu-id="ade72-237">Then select the document to view and select **Open** to view it.</span></span>
    - <span data-ttu-id="ade72-238">لإرفاق مستند بالطلب، حدد **المرفقات** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="ade72-238">To attach a document to the request, select **Attachments** on the Action Pane.</span></span> <span data-ttu-id="ade72-239">ستكون المستندات المرفقة متوفرة للموافقين عند مراجعتهم طلب الفئة.</span><span class="sxs-lookup"><span data-stu-id="ade72-239">Attached documents will be available to approvers when they review the category request.</span></span>
    - <span data-ttu-id="ade72-240">لإزالة مستند مرفق من الطلب، حدد **المرفقات** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="ade72-240">To remove an attached document from the request, select **Attachments** on the Action Pane.</span></span> <span data-ttu-id="ade72-241">حدد المستند المراد إزالته، ثم حدد **حذف** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="ade72-241">Select the document to remove, and then select **Delete** on the Action Pane.</span></span>
    - <span data-ttu-id="ade72-242">لعرض محفوظات سير العمل، حدد **سير العمل** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="ade72-242">To view the workflow history, select **Workflow** on the Action Pane.</span></span> <span data-ttu-id="ade72-243">في خيارات سير العمل، حدد **المزيد** ثم **محفوظات سير العمل**.</span><span class="sxs-lookup"><span data-stu-id="ade72-243">In the workflow options, select **More** and then **Workflow history**.</span></span> <span data-ttu-id="ade72-244">تظهر صفحة **محفوظات سير العمل**.</span><span class="sxs-lookup"><span data-stu-id="ade72-244">The **Workflow history** page appears.</span></span>

### <a name="approve-a-pending-category-request"></a><span data-ttu-id="ade72-245">الموافقة على طلب فئة معلق</span><span class="sxs-lookup"><span data-stu-id="ade72-245">Approve a pending category request</span></span>

<span data-ttu-id="ade72-246">للموافقة على طلب فئة معلق، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="ade72-246">To approve a pending category request, follow these steps.</span></span>

1. <span data-ttu-id="ade72-247">انتقل إلى **التدبير والتوريد \> الموردين \> طلبات تعاون الموردين \> طلبات الفئات**.</span><span class="sxs-lookup"><span data-stu-id="ade72-247">Go to **Procurement and sourcing \> Vendors \> Vendor collaboration requests \> Category requests**.</span></span>
1. <span data-ttu-id="ade72-248">حدد الطلب المعلق المراد الموافقة عليه.</span><span class="sxs-lookup"><span data-stu-id="ade72-248">Select the pending request to approve.</span></span>
1. <span data-ttu-id="ade72-249">راجع طلب الفئة.</span><span class="sxs-lookup"><span data-stu-id="ade72-249">Review the category request.</span></span>
1. <span data-ttu-id="ade72-250">اختياري: ضمن علامة التبويب السريع **عام**، في حقل **كود السبب**، حدد كود السبب.</span><span class="sxs-lookup"><span data-stu-id="ade72-250">Optional: On the **General** FastTab, in the **Reason code** field, select a reason code.</span></span> <span data-ttu-id="ade72-251">ثم في حقل **تعليق السبب**، أدخل تعليقًا على كود السبب.</span><span class="sxs-lookup"><span data-stu-id="ade72-251">Then, in the **Reason comment** field, enter a comment about the reason code.</span></span>
1. <span data-ttu-id="ade72-252">في جزء الإجراءات، حدد **سير العمل**.</span><span class="sxs-lookup"><span data-stu-id="ade72-252">On the Action Pane, select **Workflow**.</span></span>
1. <span data-ttu-id="ade72-253">في خيارات سير العمل ، حدد **موافقة**.</span><span class="sxs-lookup"><span data-stu-id="ade72-253">In the workflow options, select **Approve**.</span></span>
1. <span data-ttu-id="ade72-254">في حقل **التعليق**، أدخل أي معلومات إضافية مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="ade72-254">In the **Comment** field, enter any additional information that is required.</span></span> <span data-ttu-id="ade72-255">وحدد بعد ذلك **موافقة** لإكمال الطلب.</span><span class="sxs-lookup"><span data-stu-id="ade72-255">Then select **Approve** to complete the request.</span></span>

    <span data-ttu-id="ade72-256">تم تغيير حالة طلب الفئة إلى _تمت الموافقة عليه_، وتمت إضافة فئات التدبير إلى حساب المورد.</span><span class="sxs-lookup"><span data-stu-id="ade72-256">The status of the category request is changed to _Approved_, and the procurement categories are added to the vendor account.</span></span>

### <a name="reject-a-pending-category-request"></a><span data-ttu-id="ade72-257">رفض طلب فئة معلق</span><span class="sxs-lookup"><span data-stu-id="ade72-257">Reject a pending category request</span></span>

<span data-ttu-id="ade72-258">لرفض طلب فئة معلق، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="ade72-258">To reject a pending category request, follow these steps.</span></span>

1. <span data-ttu-id="ade72-259">انتقل إلى **التدبير والتوريد \> الموردين \> طلبات تعاون الموردين \> طلبات الفئات**.</span><span class="sxs-lookup"><span data-stu-id="ade72-259">Go to **Procurement and sourcing \> Vendors \> Vendor collaboration requests \> Category requests**.</span></span>
1. <span data-ttu-id="ade72-260">حدد الطلب المعلق المراد رفضه.</span><span class="sxs-lookup"><span data-stu-id="ade72-260">Select the pending request to reject.</span></span>
1. <span data-ttu-id="ade72-261">راجع طلب الفئة.</span><span class="sxs-lookup"><span data-stu-id="ade72-261">Review the category request.</span></span>
1. <span data-ttu-id="ade72-262">في جزء الإجراءات، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="ade72-262">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="ade72-263">ضمن علامة التبويب السريع **عام**، في حقل **كود السبب**، حدد كود السبب.</span><span class="sxs-lookup"><span data-stu-id="ade72-263">On the **General** FastTab, in the **Reason code** field, select a reason code.</span></span> <span data-ttu-id="ade72-264">ثم في حقل **تعليق السبب**، أدخل تعليقًا على كود السبب.</span><span class="sxs-lookup"><span data-stu-id="ade72-264">Then, in the **Reason comment** field, enter a comment about the reason code.</span></span>
1. <span data-ttu-id="ade72-265">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="ade72-265">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="ade72-266">في جزء الإجراءات، حدد **سير العمل**.</span><span class="sxs-lookup"><span data-stu-id="ade72-266">On the Action Pane, select **Workflow**.</span></span>
1. <span data-ttu-id="ade72-267">في خيارات سير العمل، حدد **المزيد** ثم **رفض**.</span><span class="sxs-lookup"><span data-stu-id="ade72-267">In the workflow options, select **More** and then **Reject**.</span></span>
1. <span data-ttu-id="ade72-268">في حقل **التعليق**، أدخل أي معلومات إضافية مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="ade72-268">In the **Comment** field, enter any additional information that is required.</span></span> <span data-ttu-id="ade72-269">وحدد بعد ذلك **رفض** لإكمال الطلب.</span><span class="sxs-lookup"><span data-stu-id="ade72-269">Then select **Reject** to complete the request.</span></span>

    <span data-ttu-id="ade72-270">تم تغيير حالة طلب الفئة إلى _مرفوض_.</span><span class="sxs-lookup"><span data-stu-id="ade72-270">The status of the category request is changed to _Rejected_.</span></span> <span data-ttu-id="ade72-271">وفي هذه المرحلة، يمكن للمورد إنشاء طلب فئة جديد كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="ade72-271">At this point, the vendor can create a new category request as required.</span></span>

### <a name="delegate-a-pending-category-request"></a><span data-ttu-id="ade72-272">رفض طلب فئة معلق</span><span class="sxs-lookup"><span data-stu-id="ade72-272">Delegate a pending category request</span></span>

<span data-ttu-id="ade72-273">لتفويض طلب فئة معلق لمستخدم آخر، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="ade72-273">To delegate a pending category request to another user, follow these steps.</span></span>

1. <span data-ttu-id="ade72-274">انتقل إلى **التدبير والتوريد \> الموردين \> طلبات تعاون الموردين \> طلبات الفئات**.</span><span class="sxs-lookup"><span data-stu-id="ade72-274">Go to **Procurement and sourcing \> Vendors \> Vendor collaboration requests \> Category requests**.</span></span>
1. <span data-ttu-id="ade72-275">حدد الطلب المعلق الذي تريد الموافقة عليه.</span><span class="sxs-lookup"><span data-stu-id="ade72-275">Select the pending request that you want to approve.</span></span>
1. <span data-ttu-id="ade72-276">في جزء الإجراءات، حدد **سير العمل**.</span><span class="sxs-lookup"><span data-stu-id="ade72-276">On the Action Pane, select **Workflow**.</span></span>
1. <span data-ttu-id="ade72-277">في خيارات سير العمل، حدد **المزيد** ثم **تفويض**.</span><span class="sxs-lookup"><span data-stu-id="ade72-277">In the workflow options, select **More** and then **Delegate**.</span></span>
1. <span data-ttu-id="ade72-278">في حقل **المستخدم**، حدد المستخدم الذي سيتم تعيين طلب الفئة إليه للمراجعة.</span><span class="sxs-lookup"><span data-stu-id="ade72-278">In the **User** field, select the user to assign the category request to for review.</span></span>
1. <span data-ttu-id="ade72-279">في حقل **التعليق**، أدخل أي معلومات إضافية مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="ade72-279">In the **Comment** field, enter any additional information that is required.</span></span>
1. <span data-ttu-id="ade72-280">حدد **تفويض** لإكمال التفويض.</span><span class="sxs-lookup"><span data-stu-id="ade72-280">Select **Delegate** to complete the delegation.</span></span> <span data-ttu-id="ade72-281">يمكن للمستخدم المحدد مراجعة طلب الفئة الآن.</span><span class="sxs-lookup"><span data-stu-id="ade72-281">The selected user can now review the category request.</span></span>

### <a name="view-procurement-categories-for-a-vendor"></a><span data-ttu-id="ade72-282">عرض فئات التدبير لمورد</span><span class="sxs-lookup"><span data-stu-id="ade72-282">View procurement categories for a vendor</span></span>

<span data-ttu-id="ade72-283">لعرض فئات التدبير لمورّد بعد الموافقة على طلب فئة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="ade72-283">To view procurement categories for a vendor after a category request is approved, follow these steps.</span></span>

1. <span data-ttu-id="ade72-284">انتقل إلى ‏‫**التدبير والتوريد \> الموردون \> جميع الموردين**.</span><span class="sxs-lookup"><span data-stu-id="ade72-284">Go to **Procurement and sourcing \> Vendors \> All vendors**.</span></span>
1. <span data-ttu-id="ade72-285">في صفحة **جميع الموردين**، حدد المورد الذي ترغب في عرض فئات التدبير له.</span><span class="sxs-lookup"><span data-stu-id="ade72-285">On the **All vendors** page, select the vendor that you want to view procurement categories for.</span></span>
1. <span data-ttu-id="ade72-286">في جزء الاجراء، افتح علامة التبويب **عام** ومن مجموعة **الإعداد**، حدد **الفئات**.</span><span class="sxs-lookup"><span data-stu-id="ade72-286">On the Action Pane, open the **General** tab and, from the **Set up** group, select **Categories**.</span></span>

    <span data-ttu-id="ade72-287">تظهر صفحة **الفئات**.</span><span class="sxs-lookup"><span data-stu-id="ade72-287">The **Categories** page appears.</span></span> <span data-ttu-id="ade72-288">تعرض علامة التبويب السريع **تدبير** فئات التدبير التي تمت إضافتها من خلال طلب الفئة.</span><span class="sxs-lookup"><span data-stu-id="ade72-288">The **Procurement** FastTab shows procurement categories that were added through the category request.</span></span>

1. <span data-ttu-id="ade72-289">في علامة التبويب السريع **التدبير**، يمكنك إجراء تغييرات إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="ade72-289">On the **Procurement** FastTab, you can make changes if needed.</span></span> <span data-ttu-id="ade72-290">على سبيل المثال، يمكنك تعيين حقل **حاله فئة المورد** إلى _مفضل_.</span><span class="sxs-lookup"><span data-stu-id="ade72-290">For example, you can set the **Vendor category status** field to _Preferred_.</span></span>
