---
title: استيراد تكوين من Lifecycle Services
description: يوضح هذا الموضوع كيفيه استيراد إصدار جديد من تكوين التقارير الكترونيه (ER) من Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
ms.date: 09/14/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 674d0dc02b4a53e455a15a06fdb7f24ca3036ba3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752354"
---
# <a name="import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="c47c0-103">استيراد تكوين من Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="c47c0-103">Import a configuration from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c47c0-104">يشرح هذا الموضوع كيف يمكن لمستخدم له دور مسؤول النظام أو مطور التقارير الإلكترونية استيراد إصدار جديد من [تكوين التقارير الإلكترونية](../general-electronic-reporting.md#Configuration) من [مكتبة الأصول على مستوى المشروع](../../lifecycle-services/asset-library.md) في Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="c47c0-104">This topic explains how a user in the System administrator or Electronic reporting developer role can import a new version of an [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) from the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="c47c0-105">في هذا المثال، ستقوم بتحديد الإصدار المطلوب من تكوين التقارير الإلكترونية واستيراده إلى الشركة النموذجية التي تحمل الاسم Litware, Inc. يمكن إكمال هذه الخطوات في أي شركة نظرًا لمشاركة تكوينات التقارير الإلكترونية بين الشركات.</span><span class="sxs-lookup"><span data-stu-id="c47c0-105">In this example, you will select the desired version of the ER configuration and import it for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="c47c0-106">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء [تحميل تكوين التقارير الإلكترونية داخل Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span><span class="sxs-lookup"><span data-stu-id="c47c0-106">To complete these steps, you must first complete the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="c47c0-107">يجب أن يتوفر أيضًا الوصول إلى LCS.</span><span class="sxs-lookup"><span data-stu-id="c47c0-107">Access to LCS is also required.</span></span>

1. <span data-ttu-id="c47c0-108">سجّل دخولك إلى التطبيق باستخدام أحد الأدوار التالية:</span><span class="sxs-lookup"><span data-stu-id="c47c0-108">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="c47c0-109">مطور إعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="c47c0-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="c47c0-110">مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="c47c0-110">System administrator</span></span>

2. <span data-ttu-id="c47c0-111">انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="c47c0-111">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="c47c0-112">حدد **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="c47c0-112">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="c47c0-113">تأكد من أن مستخدم Dynamics 365 Finance الحالي عضو في مشروع LCS الذي يحتوي على مكتبة الأصول التي يريد المستخدم [الوصول إليها](../../lifecycle-services/asset-library.md#asset-library-support) لاستيراد تكوينات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="c47c0-113">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the Asset library that the user wants to [access](../../lifecycle-services/asset-library.md#asset-library-support) to import ER configurations.</span></span>
>
> <span data-ttu-id="c47c0-114">لا يمكنك الوصول إلى مشروع LCS من مستودع تقارير إلكترونية يمثل مجالاً مختلفًا عن المجال المستخدم في Finance.</span><span class="sxs-lookup"><span data-stu-id="c47c0-114">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="c47c0-115">إذا حاولت القيام بذلك، ستظهر قائمة فارغة بمشاريع LCS، ولن تتمكن من استيراد تكوينات التقارير الإلكترونية من مكتبة الأصول على مستوى المشروع في LCS.</span><span class="sxs-lookup"><span data-stu-id="c47c0-115">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="c47c0-116">للوصول إلى مكتبات الأصول على مستوى المشروع من مستودع تقارير إلكترونية يُستخدم لاستيراد تكوينات التقارير الإلكترونية، سجل دخولك إلى Finance باستخدام بيانات اعتماد المستخدم الذي ينتمي إلى المستأجر (المجال) الذي تم تزويد مثيل Finance الحالي له.</span><span class="sxs-lookup"><span data-stu-id="c47c0-116">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a><span data-ttu-id="c47c0-117">حذف الإصدار المشترك من تكوين نموذج البيانات</span><span class="sxs-lookup"><span data-stu-id="c47c0-117">Delete a shared version of a data model configuration</span></span>

1. <span data-ttu-id="c47c0-118">في صفحة **التكوينات**، في شجرة التكوينات، حدد **تكوين نموذج العينة‬**.</span><span class="sxs-lookup"><span data-stu-id="c47c0-118">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="c47c0-119">لقد أنشأت الإصدار الأول لتكوين عينة نموذج البيانات ونشرها في LCS عندما أكملت الخطوات المذكورة في [تحميل تكوين إلى Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span><span class="sxs-lookup"><span data-stu-id="c47c0-119">You created the first version of a sample data model configuration and published it to LCS when you completed the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="c47c0-120">في هذا الإجراء، يمكنك حذف هذا الإصدار لتكوين التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="c47c0-120">In this procedure, you will delete that version of the ER configuration.</span></span> <span data-ttu-id="c47c0-121">ثم تقوم باستيراد هذا الإصدار من LCS لاحقًا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="c47c0-121">You will then import that version from LCS later in this topic.</span></span>

2. <span data-ttu-id="c47c0-122">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c47c0-122">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="c47c0-123">لهذا المثال، حدد إصدار التكوين بالحالة **مشترك**.</span><span class="sxs-lookup"><span data-stu-id="c47c0-123">For this example, select the version of the configuration that has a status of **Shared**.</span></span> <span data-ttu-id="c47c0-124">تشير هذه الحالة إلى أن التكوين تم نشره على LCS.</span><span class="sxs-lookup"><span data-stu-id="c47c0-124">This status indicates that the configuration has been published to LCS.</span></span>

3. <span data-ttu-id="c47c0-125">حدد **تغيير الحالة**.</span><span class="sxs-lookup"><span data-stu-id="c47c0-125">Select **Change status**.</span></span>
4. <span data-ttu-id="c47c0-126">حدد **إيقاف**.</span><span class="sxs-lookup"><span data-stu-id="c47c0-126">Select **Discontinue**.</span></span>

    <span data-ttu-id="c47c0-127">من خلال تغيير حالة الإصدار المحدد من **مشترك** إلى **متوقف‬‏‫**، فأنت تجعل الإصدار متوفرًا للحذف.</span><span class="sxs-lookup"><span data-stu-id="c47c0-127">By changing the status of the selected version from **Shared** to **Discontinued**, you make the version available for deletion.</span></span>

5. <span data-ttu-id="c47c0-128">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c47c0-128">Select **OK**.</span></span>
6. <span data-ttu-id="c47c0-129">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c47c0-129">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="c47c0-130">لهذا المثال، حدد إصدار التكوين بالحالة **متوقف‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="c47c0-130">For this example, select the version of the configuration that has a status of **Discontinued**.</span></span>

7. <span data-ttu-id="c47c0-131">حدد **حذف**.</span><span class="sxs-lookup"><span data-stu-id="c47c0-131">Select **Delete**.</span></span>
8. <span data-ttu-id="c47c0-132">حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="c47c0-132">Select **Yes**.</span></span>

    <span data-ttu-id="c47c0-133">لاحظ أن إصدار المسودة 2 من تكوين نموذج البيانات المحدد متوفر الآن.</span><span class="sxs-lookup"><span data-stu-id="c47c0-133">Notice that the only draft version 2 of the selected data model configuration is now available.</span></span>

9. <span data-ttu-id="c47c0-134">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c47c0-134">Close the page.</span></span>

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a><span data-ttu-id="c47c0-135">استيراد الإصدار المشترك لتكوين نموذج البيانات من LCS</span><span class="sxs-lookup"><span data-stu-id="c47c0-135">Import a shared version of a data model configuration from LCS</span></span>

1. <span data-ttu-id="c47c0-136">انتقل إلى **إدارة المؤسسة \> مساحات العمل \> إعداد التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="c47c0-136">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="c47c0-137">في القسم **موفرو التكوين**، حدد لوحة **Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="c47c0-137">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="c47c0-138">على لوحة **Litware, Inc.**، حدد **مستودعات**.</span><span class="sxs-lookup"><span data-stu-id="c47c0-138">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="c47c0-139">يمكنك الآن فتح قائمة المستودعات لموفر تكوين Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="c47c0-139">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="c47c0-140">حدد **فتح**.</span><span class="sxs-lookup"><span data-stu-id="c47c0-140">Select **Open**.</span></span>

    <span data-ttu-id="c47c0-141">لهذا المثال، حدد مستودع **LCS** وافتحه.</span><span class="sxs-lookup"><span data-stu-id="c47c0-141">For this example, select the **LCS** repository, and open it.</span></span> <span data-ttu-id="c47c0-142">يجب أن يكون لديك [حق الوصول ](#accessconditions) إلى مشروع LCS وإلى مكتبة الأصول التي يتم الوصول إليها بواسطة مستودع التقارير الإلكترونية المحدد.</span><span class="sxs-lookup"><span data-stu-id="c47c0-142">You must have [access](#accessconditions) to the LCS project and to the Asset library that is accessed by the selected ER repository.</span></span>

5. <span data-ttu-id="c47c0-143">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c47c0-143">In the list, mark the selected row.</span></span>

    <span data-ttu-id="c47c0-144">لهذا المثال، حدد الإصدار الأول من **تكوين نموذج العينة** في قائمة الإصدارات.</span><span class="sxs-lookup"><span data-stu-id="c47c0-144">For this example, select the first version of **Sample model configuration** in the version list.</span></span>

6. <span data-ttu-id="c47c0-145">حدد **استيراد**.</span><span class="sxs-lookup"><span data-stu-id="c47c0-145">Select **Import**.</span></span>
7. <span data-ttu-id="c47c0-146">حدد **نعم** لتأكيد استيراد الإصدار المحدد من LCS.</span><span class="sxs-lookup"><span data-stu-id="c47c0-146">Select **Yes** to confirm the import of the selected version from LCS.</span></span>

    <span data-ttu-id="c47c0-147">تؤكد رسالة إخبارية استيراد الإصدار المحدد بنجاح.</span><span class="sxs-lookup"><span data-stu-id="c47c0-147">An informational message confirms that the selected version was successfully imported.</span></span>

8. <span data-ttu-id="c47c0-148">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c47c0-148">Close the page.</span></span>
9. <span data-ttu-id="c47c0-149">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c47c0-149">Close the page.</span></span>
10. <span data-ttu-id="c47c0-150">حدد **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="c47c0-150">Select **Configurations**.</span></span>
11. <span data-ttu-id="c47c0-151">في الشجرة، حدد ‏‫**تكوين نموذج العينة**‬.</span><span class="sxs-lookup"><span data-stu-id="c47c0-151">In the tree, select **Sample model configuration**.</span></span>
12. <span data-ttu-id="c47c0-152">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c47c0-152">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="c47c0-153">لهذا المثال، حدد إصدار التكوين بالحالة **مشترك**.</span><span class="sxs-lookup"><span data-stu-id="c47c0-153">For this example, select the version of the configuration that has a status of **Shared**.</span></span>

    <span data-ttu-id="c47c0-154">لاحظ أن الإصدار المشترك 1 من تكوين نموذج البيانات المحدد متوفر الآن أيضًا.</span><span class="sxs-lookup"><span data-stu-id="c47c0-154">Notice that shared version 1 of the selected data model configuration is also available now.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]