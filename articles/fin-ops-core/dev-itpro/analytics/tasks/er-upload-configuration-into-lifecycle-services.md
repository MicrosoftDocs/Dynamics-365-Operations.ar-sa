---
title: تحميل تكوين إلى Lifecycle Services
description: يشرح هذا الموضوع كيف يمكن لمستخدم له دور مسؤول النظام أو مطور التقارير الإلكترونية إنشاء إصدار جديد من تكوين التقارير الإلكترونية وتحميله إلى Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
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
ms.openlocfilehash: c43bad3ee2530a454de718a0a7da4d1e468a4af4
ms.sourcegitcommit: 9857d5cbdc0ab2fc9db049ac5ad118fc2b29bedc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/14/2020
ms.locfileid: "3810681"
---
# <a name="upload-a-configuration-into-lifecycle-services"></a><span data-ttu-id="c0aaf-103">تحميل تكوين إلى Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="c0aaf-103">Upload a configuration into Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c0aaf-104">يشرح هذا الموضوع كيف يمكن لمستخدم له دور مسؤول النظام أو مطور التقارير الإلكترونية إنشاء إصدار جديد من [تكوين التقارير الإلكترونية](../general-electronic-reporting.md#Configuration) وتحميله إلى [مكتبة الأصول على مستوى المشروع](../../lifecycle-services/asset-library.md) في Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="c0aaf-104">This topic explains how a user in the System administrator or Electronic reporting developer role can create a new [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) and upload it into the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="c0aaf-105">في هذا المثال، ستقوم بإنشاء تكوين وتحميله إلى LCS لشركة نموذجية تحمل الاسم Litware, Inc. يمكن إكمال هذه الخطوات في أي شركة نظرًا لمشاركة تكوينات التقارير الإلكترونية بين الشركات.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-105">In this example, you will create a configuration and upload it into LCS for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="c0aaf-106">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الموضوع [إنشاء موفري التكوين ووضع علامة نشط عليهم‬](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="c0aaf-106">To complete these steps, you must first complete the steps in [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="c0aaf-107">يجب أن يتوفر أيضًا الوصول إلى LCS.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-107">Access to LCS is also required.</span></span>

1. <span data-ttu-id="c0aaf-108">سجّل دخولك إلى التطبيق باستخدام أحد الأدوار التالية:</span><span class="sxs-lookup"><span data-stu-id="c0aaf-108">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="c0aaf-109">مطور إعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="c0aaf-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="c0aaf-110">مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="c0aaf-110">System administrator</span></span>

2. <span data-ttu-id="c0aaf-111">انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-111">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="c0aaf-112">حدد **Litware, Inc.**، وضع علامة **نشط** عليها.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-112">Select **Litware, Inc.**, and mark it as **Active**.</span></span>
4. <span data-ttu-id="c0aaf-113">حدد **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-113">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="c0aaf-114">تأكد من أن مستخدم Dynamics 365 Finance الحالي عضو في مشروع LCS الذي يحتوي على [مكتبة الأصول](../../lifecycle-services/asset-library.md#asset-library-support) المستخدمة لاستيراد تكوينات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-114">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the [Asset library](../../lifecycle-services/asset-library.md#asset-library-support) that is used to import ER configurations.</span></span>
>
> <span data-ttu-id="c0aaf-115">لا يمكنك الوصول إلى مشروع LCS من مستودع تقارير إلكترونية يمثل مجالاً مختلفًا عن المجال المستخدم في Finance.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-115">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="c0aaf-116">إذا حاولت القيام بذلك، ستظهر قائمة فارغة بمشاريع LCS، ولن تتمكن من استيراد تكوينات التقارير الإلكترونية من مكتبة الأصول على مستوى المشروع في LCS.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-116">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="c0aaf-117">للوصول إلى مكتبات الأصول على مستوى المشروع من مستودع تقارير إلكترونية يُستخدم لاستيراد تكوينات التقارير الإلكترونية، سجل دخولك إلى Finance باستخدام بيانات اعتماد المستخدم الذي ينتمي إلى المستأجر (المجال) الذي تم تزويد مثيل Finance الحالي له.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-117">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="c0aaf-118">إنشاء تكوين نموذج بيانات جديد</span><span class="sxs-lookup"><span data-stu-id="c0aaf-118">Create a new data model configuration</span></span>

1. <span data-ttu-id="c0aaf-119">انتقل إلى **إدارة المؤسسة \> التقارير الإلكترونية \> التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-119">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="c0aaf-120">في صفحة **التكوينات**، حدد **إنشاء تكوين** لفتح مربع حوار القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-120">On the **Configurations** page, select **Create configuration** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="c0aaf-121">في هذا المثال، ستقوم بإنشاء تكوين يحتوي على نموذج بيانات للمستندات الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-121">In this example, you will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="c0aaf-122">سيتم تحميل تكوين نموذج البيانات هذا في LCS لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-122">This data model configuration will be uploaded into LCS later.</span></span>

3. <span data-ttu-id="c0aaf-123">في الحقل **الاسم**، أدخل **تكوين نموذج العينة**.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-123">In the **Name** field, enter **Sample model configuration**.</span></span>
4. <span data-ttu-id="c0aaf-124">في الحقل **الوصف**، أدخل **تكوين نموذج العينة**.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-124">In the **Description** field, enter **Sample model configuration**.</span></span>
5. <span data-ttu-id="c0aaf-125">حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-125">Select **Create configuration**.</span></span>
6. <span data-ttu-id="c0aaf-126">حدد **مصمم النموذج**.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-126">Select **Model designer**.</span></span>
7. <span data-ttu-id="c0aaf-127">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-127">Select **New**.</span></span>
8. <span data-ttu-id="c0aaf-128">في حقل **الاسم**، أدخل **نقطة الإدخال**.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-128">In the **Name** field, enter **Entry point**.</span></span>
9. <span data-ttu-id="c0aaf-129">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-129">Select **Add**.</span></span>
10. <span data-ttu-id="c0aaf-130">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-130">Select **Save**.</span></span>
11. <span data-ttu-id="c0aaf-131">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-131">Close the page.</span></span>
12. <span data-ttu-id="c0aaf-132">حدد **تغيير الحالة**.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-132">Select **Change status**.</span></span>
13. <span data-ttu-id="c0aaf-133">حدد **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-133">Select **Complete**.</span></span>
14. <span data-ttu-id="c0aaf-134">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-134">Select **OK**.</span></span>
15. <span data-ttu-id="c0aaf-135">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-135">Close the page.</span></span>

## <a name="register-a-new-repository"></a><span data-ttu-id="c0aaf-136">تسجيل مستودع جديد</span><span class="sxs-lookup"><span data-stu-id="c0aaf-136">Register a new repository</span></span>

1. <span data-ttu-id="c0aaf-137">انتقل إلى **إدارة المؤسسة \> مساحات العمل \> إعداد التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-137">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="c0aaf-138">في القسم **موفرو التكوين**، حدد لوحة **Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-138">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="c0aaf-139">على لوحة **Litware, Inc.**، حدد **مستودعات**.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-139">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="c0aaf-140">يمكنك الآن فتح قائمة المستودعات لموفر تكوين Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-140">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="c0aaf-141">حدد **إضافة** لفتح مربع حوار القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-141">Select **Add** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="c0aaf-142">يمكنك الآن إضافة مستودع جديد.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-142">You can now add a new repository.</span></span>

5. <span data-ttu-id="c0aaf-143">في الحقل **الدخول إلى مستودع التكوين**، حدد **LCS**.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-143">In the **Configuration repository enter** field, select **LCS**.</span></span>
6. <span data-ttu-id="c0aaf-144">حدد **إنشاء مستودع**.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-144">Select **Create repository**.</span></span>
7. <span data-ttu-id="c0aaf-145">في الحقل **المشروع**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-145">In the **Project** field, enter or select a value.</span></span>

    <span data-ttu-id="c0aaf-146">لهذا المثال، حدد مشروع LCS المطلوب.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-146">For this example, select the desired LCS project.</span></span> <span data-ttu-id="c0aaf-147">يجب أن يكون لديك [حق الوصول](#accessconditions) إلى المشروع.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-147">You must have [access](#accessconditions) to the project.</span></span>

8. <span data-ttu-id="c0aaf-148">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-148">Select **OK**.</span></span>

    <span data-ttu-id="c0aaf-149">أكمل إدخال مستودع جديد.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-149">Complete a new repository entry.</span></span>

9. <span data-ttu-id="c0aaf-150">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-150">In the list, mark the selected row.</span></span>

    <span data-ttu-id="c0aaf-151">لهذا المثال، حدد سجل مستودع **LCS**.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-151">For this example, select the **LCS** repository record.</span></span>

    <span data-ttu-id="c0aaf-152">لاحظ أن المستودع المسجل مميز بعلامة بواسطة الموفر الحالي.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-152">Note that a registered repository is marked by the current provider.</span></span> <span data-ttu-id="c0aaf-153">بمعنى آخر، يمكن وضع التكوينات التي يملكها هذا الموفر فقط في هذا المستودع وبالتالي يتم تحميلها إلى مشروع LCS المحدد.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-153">In other words, only configurations that are owned by that provider can be put in this repository and therefore uploaded into the selected LCS project.</span></span>

10. <span data-ttu-id="c0aaf-154">حدد **فتح**.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-154">Select **Open**.</span></span>

    <span data-ttu-id="c0aaf-155">أنت تفتح المستودع لعرض قائمة تكوينات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-155">You open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="c0aaf-156">ستكون القائمة فارغة إذا لم يكن قد تم بعد استخدام المشروع المحدد لمشاركة تكوينات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-156">If the selected project hasn't yet been used for ER configurations sharing, the list will be empty.</span></span>

11. <span data-ttu-id="c0aaf-157">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-157">Close the page.</span></span>
12. <span data-ttu-id="c0aaf-158">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-158">Close the page.</span></span>

## <a name="upload-a-configuration-into-lcs"></a><span data-ttu-id="c0aaf-159">تحميل تكوين إلى LCS</span><span class="sxs-lookup"><span data-stu-id="c0aaf-159">Upload a configuration into LCS</span></span>

1. <span data-ttu-id="c0aaf-160">انتقل إلى **إدارة المؤسسة \> التقارير الإلكترونية \> التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-160">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="c0aaf-161">في صفحة **التكوينات**، في شجرة التكوينات، حدد **تكوين نموذج العينة‬**.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-161">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="c0aaf-162">يجب عليك تحديد تكوين مُنشأ تم إكماله.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-162">You must select a created configuration that has been already completed.</span></span>

3. <span data-ttu-id="c0aaf-163">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-163">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="c0aaf-164">لهذا المثال، حدد إصدار التكوين المحدد بالحالة **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-164">For this example, select the version of the selected configuration that has a status of **Completed**.</span></span>

4. <span data-ttu-id="c0aaf-165">حدد **تغيير الحالة**.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-165">Select **Change status**.</span></span>
5. <span data-ttu-id="c0aaf-166">حدد **مشاركة**.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-166">Select **Share**.</span></span>

    <span data-ttu-id="c0aaf-167">يتم تغيير حالة التكوين من **مكتمل** إلى **مشترك** عند نشر التكوين في LCS.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-167">The status of the configuration is changed from **Completed** to **Shared** when the configuration is published in LCS.</span></span>

6. <span data-ttu-id="c0aaf-168">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-168">Select **OK**.</span></span>
7. <span data-ttu-id="c0aaf-169">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-169">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="c0aaf-170">لهذا المثال، حدد إصدار التكوين بالحالة **مشترك**.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-170">For this example, select the configuration version that has a status of **Shared**.</span></span>

    <span data-ttu-id="c0aaf-171">لاحظ أنه تم تغيير حالة الإصدار المحدد من **مكتمل** إلى **مشترك**.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-171">Note that the status of the selected version was changed from **Completed** to **Shared**.</span></span>

8. <span data-ttu-id="c0aaf-172">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-172">Close the page.</span></span>
9. <span data-ttu-id="c0aaf-173">حدد **المستودعات**.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-173">Select **Repositories**.</span></span>

    <span data-ttu-id="c0aaf-174">يمكنك الآن فتح قائمة المستودعات لموفر تكوين Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-174">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

10. <span data-ttu-id="c0aaf-175">حدد **فتح**.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-175">Select **Open**.</span></span>

    <span data-ttu-id="c0aaf-176">لهذا المثال، حدد مستودع **LCS** وافتحه.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-176">For this example, select the **LCS** repository, and open it.</span></span>

    <span data-ttu-id="c0aaf-177">لاحظ أن التكوين المحدد يظهر كأصل مشروع LCS المحدد.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-177">Notice that the selected configuration is shown as an asset of the selected LCS project.</span></span>

11. <span data-ttu-id="c0aaf-178">افتح LCS من خلال الانتقال إلى <https://lcs.dynamics.com>.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-178">Open LCS by going to <https://lcs.dynamics.com>.</span></span>
12. <span data-ttu-id="c0aaf-179">افتح مشروعًا تم استخدامه في وقت سابق لتسجيل المستودع.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-179">Open a project that was used earlier for repository registration.</span></span>
13. <span data-ttu-id="c0aaf-180">افتح مكتبة الأصول الخاصة بالمشروع.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-180">Open the Asset library of the project.</span></span>
14. <span data-ttu-id="c0aaf-181">حدد نوع الأصل **تكوين GER**.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-181">Select the **GER configuration** asset type.</span></span>

    <span data-ttu-id="c0aaf-182">يجب أن يكون تكوين التقارير الإلكترونية الذي قمت بتحميله مدرجًا.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-182">The ER configuration that you uploaded should be listed.</span></span>

    <span data-ttu-id="c0aaf-183">لاحظ أنه يمكن استيراد تكوين LCS الذي تم تحميله إلى مثيل آخر إذا كان باستطاعة الموفرين الوصول إلى مشروع LCS هذا.</span><span class="sxs-lookup"><span data-stu-id="c0aaf-183">Note that the uploaded LCS configuration can be imported into another instance if providers have access to this LCS project.</span></span>
