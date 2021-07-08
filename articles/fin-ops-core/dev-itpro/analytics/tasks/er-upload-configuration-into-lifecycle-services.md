---
title: تحميل تكوين إلى Lifecycle Services
description: يوضح هذا الموضوع كيفية إنشاء تكوين التقارير الإلكترونية الجديد وتحميله إلى Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
ms.date: 06/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 41a8fcf2592bde4901aba703e0cd124b1155dac6
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270549"
---
# <a name="upload-a-configuration-into-lifecycle-services"></a><span data-ttu-id="6d5b5-103">تحميل تكوين إلى Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="6d5b5-103">Upload a configuration into Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6d5b5-104">يشرح هذا الموضوع كيف يمكن لمستخدم له دور مسؤول النظام أو مطور التقارير الإلكترونية إنشاء إصدار جديد من [تكوين التقارير الإلكترونية](../general-electronic-reporting.md#Configuration) وتحميله إلى [مكتبة الأصول على مستوى المشروع](../../lifecycle-services/asset-library.md) في Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="6d5b5-104">This topic explains how a user in the System administrator or Electronic reporting developer role can create a new [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) and upload it into the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6d5b5-105">إن استخدام LCS كمستودع تخزين لتكوينات التقارير الإلكترونية يكون [مهملاً](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span><span class="sxs-lookup"><span data-stu-id="6d5b5-105">The use of LCS as a storage repository for ER configurations is being [deprecated](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span></span> <span data-ttu-id="6d5b5-106">لمزيد من المعلومات، [إهلاك تخزين Regulatory Configuration Service (RCS) – Lifecycle Services (LCS)](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md)</span><span class="sxs-lookup"><span data-stu-id="6d5b5-106">For more information, see [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span></span>

<span data-ttu-id="6d5b5-107">في هذا المثال، ستقوم بإنشاء تكوين وتحميله إلى LCS لشركة نموذجية تحمل الاسم Litware, Inc. يمكن إكمال هذه الخطوات في أي شركة نظرًا لمشاركة تكوينات التقارير الإلكترونية بين الشركات.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-107">In this example, you will create a configuration and upload it into LCS for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="6d5b5-108">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الموضوع [إنشاء موفري التكوين ووضع علامة نشط عليهم‬](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="6d5b5-108">To complete these steps, you must first complete the steps in [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="6d5b5-109">يجب أن يتوفر أيضًا الوصول إلى LCS.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-109">Access to LCS is also required.</span></span>

1. <span data-ttu-id="6d5b5-110">سجّل دخولك إلى التطبيق باستخدام أحد الأدوار التالية:</span><span class="sxs-lookup"><span data-stu-id="6d5b5-110">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="6d5b5-111">مطور إعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="6d5b5-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="6d5b5-112">مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="6d5b5-112">System administrator</span></span>

2. <span data-ttu-id="6d5b5-113">انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-113">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="6d5b5-114">حدد **Litware, Inc.**، وضع علامة **نشط** عليها.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-114">Select **Litware, Inc.**, and mark it as **Active**.</span></span>
4. <span data-ttu-id="6d5b5-115">حدد **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-115">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="6d5b5-116">تأكد من أن مستخدم Dynamics 365 Finance الحالي عضو في مشروع LCS الذي يحتوي على [مكتبة الأصول](../../lifecycle-services/asset-library.md#asset-library-support) المستخدمة لاستيراد تكوينات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-116">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the [Asset library](../../lifecycle-services/asset-library.md#asset-library-support) that is used to import ER configurations.</span></span>
>
> <span data-ttu-id="6d5b5-117">لا يمكنك الوصول إلى مشروع LCS من مستودع تقارير إلكترونية يمثل مجالاً مختلفًا عن المجال المستخدم في Finance.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-117">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="6d5b5-118">إذا حاولت القيام بذلك، ستظهر قائمة فارغة بمشاريع LCS، ولن تتمكن من استيراد تكوينات التقارير الإلكترونية من مكتبة الأصول على مستوى المشروع في LCS.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-118">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="6d5b5-119">للوصول إلى مكتبات الأصول على مستوى المشروع من مستودع تقارير إلكترونية يُستخدم لاستيراد تكوينات التقارير الإلكترونية، سجل دخولك إلى Finance باستخدام بيانات اعتماد المستخدم الذي ينتمي إلى المستأجر (المجال) الذي تم تزويد مثيل Finance الحالي له.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-119">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="6d5b5-120">إنشاء تكوين نموذج بيانات جديد</span><span class="sxs-lookup"><span data-stu-id="6d5b5-120">Create a new data model configuration</span></span>

1. <span data-ttu-id="6d5b5-121">انتقل إلى **إدارة المؤسسة \> التقارير الإلكترونية \> التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-121">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="6d5b5-122">في صفحة **التكوينات**، حدد **إنشاء تكوين** لفتح مربع حوار القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-122">On the **Configurations** page, select **Create configuration** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="6d5b5-123">في هذا المثال، ستقوم بإنشاء تكوين يحتوي على نموذج بيانات للمستندات الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-123">In this example, you will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="6d5b5-124">سيتم تحميل تكوين نموذج البيانات هذا في LCS لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-124">This data model configuration will be uploaded into LCS later.</span></span>

3. <span data-ttu-id="6d5b5-125">في الحقل **الاسم**، أدخل **تكوين نموذج العينة**.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-125">In the **Name** field, enter **Sample model configuration**.</span></span>
4. <span data-ttu-id="6d5b5-126">في الحقل **الوصف**، أدخل **تكوين نموذج العينة**.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-126">In the **Description** field, enter **Sample model configuration**.</span></span>
5. <span data-ttu-id="6d5b5-127">حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-127">Select **Create configuration**.</span></span>
6. <span data-ttu-id="6d5b5-128">حدد **مصمم النموذج**.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-128">Select **Model designer**.</span></span>
7. <span data-ttu-id="6d5b5-129">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-129">Select **New**.</span></span>
8. <span data-ttu-id="6d5b5-130">في حقل **الاسم**، أدخل **نقطة الإدخال**.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-130">In the **Name** field, enter **Entry point**.</span></span>
9. <span data-ttu-id="6d5b5-131">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-131">Select **Add**.</span></span>
10. <span data-ttu-id="6d5b5-132">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-132">Select **Save**.</span></span>
11. <span data-ttu-id="6d5b5-133">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-133">Close the page.</span></span>
12. <span data-ttu-id="6d5b5-134">حدد **تغيير الحالة**.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-134">Select **Change status**.</span></span>
13. <span data-ttu-id="6d5b5-135">حدد **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-135">Select **Complete**.</span></span>
14. <span data-ttu-id="6d5b5-136">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-136">Select **OK**.</span></span>
15. <span data-ttu-id="6d5b5-137">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-137">Close the page.</span></span>

## <a name="register-a-new-repository"></a><span data-ttu-id="6d5b5-138">تسجيل مستودع جديد</span><span class="sxs-lookup"><span data-stu-id="6d5b5-138">Register a new repository</span></span>

1. <span data-ttu-id="6d5b5-139">انتقل إلى **إدارة المؤسسة \> مساحات العمل \> إعداد التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-139">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="6d5b5-140">في القسم **موفرو التكوين**، حدد لوحة **Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-140">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="6d5b5-141">على لوحة **Litware, Inc.**، حدد **مستودعات**.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-141">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="6d5b5-142">يمكنك الآن فتح قائمة المستودعات لموفر تكوين Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-142">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="6d5b5-143">حدد **إضافة** لفتح مربع حوار القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-143">Select **Add** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="6d5b5-144">يمكنك الآن إضافة مستودع جديد.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-144">You can now add a new repository.</span></span>

5. <span data-ttu-id="6d5b5-145">في الحقل **الدخول إلى مستودع التكوين**، حدد **LCS**.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-145">In the **Configuration repository enter** field, select **LCS**.</span></span>
6. <span data-ttu-id="6d5b5-146">حدد **إنشاء مستودع**.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-146">Select **Create repository**.</span></span>
7. <span data-ttu-id="6d5b5-147">في الحقل **المشروع**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-147">In the **Project** field, enter or select a value.</span></span>

    <span data-ttu-id="6d5b5-148">لهذا المثال، حدد مشروع LCS المطلوب.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-148">For this example, select the desired LCS project.</span></span> <span data-ttu-id="6d5b5-149">يجب أن يكون لديك [حق الوصول](#accessconditions) إلى المشروع.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-149">You must have [access](#accessconditions) to the project.</span></span>

8. <span data-ttu-id="6d5b5-150">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-150">Select **OK**.</span></span>

    <span data-ttu-id="6d5b5-151">أكمل إدخال مستودع جديد.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-151">Complete a new repository entry.</span></span>

9. <span data-ttu-id="6d5b5-152">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-152">In the list, mark the selected row.</span></span>

    <span data-ttu-id="6d5b5-153">لهذا المثال، حدد سجل مستودع **LCS**.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-153">For this example, select the **LCS** repository record.</span></span>

    <span data-ttu-id="6d5b5-154">لاحظ أن المستودع المسجل مميز بعلامة بواسطة الموفر الحالي.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-154">Note that a registered repository is marked by the current provider.</span></span> <span data-ttu-id="6d5b5-155">بمعنى آخر، يمكن وضع التكوينات التي يملكها هذا الموفر فقط في هذا المستودع وبالتالي يتم تحميلها إلى مشروع LCS المحدد.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-155">In other words, only configurations that are owned by that provider can be put in this repository and therefore uploaded into the selected LCS project.</span></span>

10. <span data-ttu-id="6d5b5-156">حدد **فتح**.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-156">Select **Open**.</span></span>

    <span data-ttu-id="6d5b5-157">أنت تفتح المستودع لعرض قائمة تكوينات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-157">You open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="6d5b5-158">ستكون القائمة فارغة إذا لم يكن قد تم بعد استخدام المشروع المحدد لمشاركة تكوينات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-158">If the selected project hasn't yet been used for ER configurations sharing, the list will be empty.</span></span>

11. <span data-ttu-id="6d5b5-159">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-159">Close the page.</span></span>
12. <span data-ttu-id="6d5b5-160">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-160">Close the page.</span></span>

## <a name="upload-a-configuration-into-lcs"></a><span data-ttu-id="6d5b5-161">تحميل تكوين إلى LCS</span><span class="sxs-lookup"><span data-stu-id="6d5b5-161">Upload a configuration into LCS</span></span>

1. <span data-ttu-id="6d5b5-162">انتقل إلى **إدارة المؤسسة \> التقارير الإلكترونية \> التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-162">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="6d5b5-163">في صفحة **التكوينات**، في شجرة التكوينات، حدد **تكوين نموذج العينة‬**.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-163">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="6d5b5-164">يجب عليك تحديد تكوين مُنشأ تم إكماله.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-164">You must select a created configuration that has been already completed.</span></span>

3. <span data-ttu-id="6d5b5-165">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-165">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="6d5b5-166">لهذا المثال، حدد إصدار التكوين المحدد بالحالة **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-166">For this example, select the version of the selected configuration that has a status of **Completed**.</span></span>

4. <span data-ttu-id="6d5b5-167">حدد **تغيير الحالة**.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-167">Select **Change status**.</span></span>
5. <span data-ttu-id="6d5b5-168">حدد **مشاركة**.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-168">Select **Share**.</span></span>

    <span data-ttu-id="6d5b5-169">يتم تغيير حالة التكوين من **مكتمل** إلى **مشترك** عند نشر التكوين في LCS.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-169">The status of the configuration is changed from **Completed** to **Shared** when the configuration is published in LCS.</span></span>

6. <span data-ttu-id="6d5b5-170">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-170">Select **OK**.</span></span>
7. <span data-ttu-id="6d5b5-171">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-171">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="6d5b5-172">لهذا المثال، حدد إصدار التكوين بالحالة **مشترك**.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-172">For this example, select the configuration version that has a status of **Shared**.</span></span>

    <span data-ttu-id="6d5b5-173">لاحظ أنه تم تغيير حالة الإصدار المحدد من **مكتمل** إلى **مشترك**.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-173">Note that the status of the selected version was changed from **Completed** to **Shared**.</span></span>

8. <span data-ttu-id="6d5b5-174">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-174">Close the page.</span></span>
9. <span data-ttu-id="6d5b5-175">حدد **المستودعات**.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-175">Select **Repositories**.</span></span>

    <span data-ttu-id="6d5b5-176">يمكنك الآن فتح قائمة المستودعات لموفر تكوين Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-176">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

10. <span data-ttu-id="6d5b5-177">حدد **فتح**.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-177">Select **Open**.</span></span>

    <span data-ttu-id="6d5b5-178">لهذا المثال، حدد مستودع **LCS** وافتحه.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-178">For this example, select the **LCS** repository, and open it.</span></span>

    <span data-ttu-id="6d5b5-179">لاحظ أن التكوين المحدد يظهر كأصل مشروع LCS المحدد.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-179">Notice that the selected configuration is shown as an asset of the selected LCS project.</span></span>

11. <span data-ttu-id="6d5b5-180">افتح LCS من خلال الانتقال إلى <https://lcs.dynamics.com>.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-180">Open LCS by going to <https://lcs.dynamics.com>.</span></span>
12. <span data-ttu-id="6d5b5-181">افتح مشروعًا تم استخدامه في وقت سابق لتسجيل المستودع.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-181">Open a project that was used earlier for repository registration.</span></span>
13. <span data-ttu-id="6d5b5-182">افتح مكتبة الأصول الخاصة بالمشروع.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-182">Open the Asset library of the project.</span></span>
14. <span data-ttu-id="6d5b5-183">حدد نوع الأصل **تكوين GER**.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-183">Select the **GER configuration** asset type.</span></span>

    <span data-ttu-id="6d5b5-184">يجب أن يكون تكوين التقارير الإلكترونية الذي قمت بتحميله مدرجًا.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-184">The ER configuration that you uploaded should be listed.</span></span>

    <span data-ttu-id="6d5b5-185">لاحظ أنه يمكن استيراد تكوين LCS الذي تم تحميله إلى مثيل آخر إذا كان باستطاعة الموفرين الوصول إلى مشروع LCS هذا.</span><span class="sxs-lookup"><span data-stu-id="6d5b5-185">Note that the uploaded LCS configuration can be imported into another instance if providers have access to this LCS project.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
