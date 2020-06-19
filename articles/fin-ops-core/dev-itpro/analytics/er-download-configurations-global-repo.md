---
title: تنزيل تكوينات التقارير الإلكترونية من المستودع العمومي لخدمة التكوين
description: يشرح هذا الموضوع كيفية تنزيل تكوينات التقارير الإلكترونية من المستودع العمومي لخدمة التكوين.
author: NickSelin
manager: AnnBe
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: ed31cdee74c9db26ba76ed263b5e0578cd04bc3d
ms.sourcegitcommit: 7816902b59aa61d9183d54b50a86e282661e3971
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/02/2020
ms.locfileid: "3421692"
---
# <a name="download-er-configurations-from-the-global-repository-of-configuration-service"></a><span data-ttu-id="0daec-103">تنزيل تكوينات التقارير الإلكترونية من المستودع العمومي لخدمة التكوين</span><span class="sxs-lookup"><span data-stu-id="0daec-103">Download ER configurations from the Global repository of Configuration service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0daec-104">يشرح هذا الموضوع كيفية تنزيل [تكوينات التقارير الإلكترونية](general-electronic-reporting.md#Configuration) من المستودع العمومي لخدمة التكوين.</span><span class="sxs-lookup"><span data-stu-id="0daec-104">This topic explains how to download [Electronic reporting (ER) configurations](general-electronic-reporting.md#Configuration) from the Global repository of configuration service.</span></span> <span data-ttu-id="0daec-105">لمزيد من المعلومات، راجع [Microsoft Dynamics 365 for Finance and Operations -‏ Regulatory Services، خدمة التكوين](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span><span class="sxs-lookup"><span data-stu-id="0daec-105">For more information, see [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, Configuration service](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span></span>

## <a name="open-configurations-repository"></a><span data-ttu-id="0daec-106">فتح مستودع التكوينات</span><span class="sxs-lookup"><span data-stu-id="0daec-106">Open configurations repository</span></span>

1. <span data-ttu-id="0daec-107">سجّل دخولك إلى تطبيق Dynamics 365 Finance باستخدام أحد الأدوار التالية:</span><span class="sxs-lookup"><span data-stu-id="0daec-107">Sign in to the Dynamics 365 Finance application using one of the following roles:</span></span>

    - <span data-ttu-id="0daec-108">مطور إعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="0daec-108">Electronic reporting developer</span></span>
    - <span data-ttu-id="0daec-109">مستشار وظيفي لإعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="0daec-109">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="0daec-110">مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="0daec-110">System administrator</span></span>

2. <span data-ttu-id="0daec-111">انتقل إلى **إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني**‬.</span><span class="sxs-lookup"><span data-stu-id="0daec-111">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
3. <span data-ttu-id="0daec-112">في مقطع **موفرو التكوين**، حدد لوحة **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="0daec-112">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
3. <span data-ttu-id="0daec-113">على لوحة **Microsoft**، حدد **مستودعات**.</span><span class="sxs-lookup"><span data-stu-id="0daec-113">On the **Microsoft** tile, select **Repositories**.</span></span>

    ![مساحة عمل إعداد التقارير الإلكترونية](./media/er-download-configurations-global-repo-er-workspace.png)

4. <span data-ttu-id="0daec-115">في صفحة **مستودعات التكوين**، في الشبكة، حدد المستودع الموجود من النوع **عمومي**.</span><span class="sxs-lookup"><span data-stu-id="0daec-115">On the **Configuration repositories** page, in the grid, select the existing repository of the **Global** type.</span></span> <span data-ttu-id="0daec-116">إذا لم يظهر هذا المستودع في الشبكة، فاتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="0daec-116">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="0daec-117">حدد **إضافة** لإضافة مستودع جديد.</span><span class="sxs-lookup"><span data-stu-id="0daec-117">Select **Add** to add a new repository.</span></span>
    2. <span data-ttu-id="0daec-118">حدد **عمومي** كنوع مستودع، ثم حدد **إنشاء مستودع**.</span><span class="sxs-lookup"><span data-stu-id="0daec-118">Select **Global** as the repository type, and then select **Create repository**.</span></span>
    3. <span data-ttu-id="0daec-119">اتبع الإرشادات التخويل، إذا طلب منك ذلك.</span><span class="sxs-lookup"><span data-stu-id="0daec-119">If prompted, follow the authorization instructions.</span></span>
    4. <span data-ttu-id="0daec-120">أدخل اسمًا ووصفًا للمستودع، ثم حدد **موافق** لتأكيد إدخال المستودع الجديد.</span><span class="sxs-lookup"><span data-stu-id="0daec-120">Enter a name and description for the repository and then select **OK** to confirm the new repository entry.</span></span>
    5. <span data-ttu-id="0daec-121">في الشبكة، حدد المستودع الجديد من النوع **عمومي‎**.</span><span class="sxs-lookup"><span data-stu-id="0daec-121">In the grid, select the new repository of the **Global** type.</span></span>

5. <span data-ttu-id="0daec-122">حدد **فتح** لعرض قائمة تكوينات التقارير الإلكترونية للمستودع المحدد.</span><span class="sxs-lookup"><span data-stu-id="0daec-122">Select **Open** to view the list of ER configurations for the selected repository.</span></span>

    ![صفحة مستودعات التكوين](./media/er-download-configurations-global-repo-repositories-list.png)

## <a name="import-a-single-configuration"></a><span data-ttu-id="0daec-124">استيراد تكوين واحد</span><span class="sxs-lookup"><span data-stu-id="0daec-124">Import a single configuration</span></span>

1. <span data-ttu-id="0daec-125">في صفحة **مستودعات التكوين**، في شجرة التكوينات، حدد تكوين التقارير الإلكترونية المطلوب.</span><span class="sxs-lookup"><span data-stu-id="0daec-125">On the **Configuration repositories** page, in the configurations tree, select the ER configuration that you want.</span></span>
2. <span data-ttu-id="0daec-126">على علامة التبويب السريعة **إصدارات**، حدد الإصدار المطلوب لتكوين التقارير الإلكترونية المحدد.</span><span class="sxs-lookup"><span data-stu-id="0daec-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
3. <span data-ttu-id="0daec-127">حدد **استيراد** لتنزيل الإصدار المحدد من المستودع العمومي إلى مثيل Finance and Operations الحالي.</span><span class="sxs-lookup"><span data-stu-id="0daec-127">Select **Import** to download the selected version from Global repository to the current Finance instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0daec-128">لا يتوفر الزر **استيراد** لإصدارات تكوينات التقارير الإلكترونية الموجودة في مثيل Finance الحالي.</span><span class="sxs-lookup"><span data-stu-id="0daec-128">The **Import** button is unavailable for ER configuration versions that are already present in the current Finance instance.</span></span>

    ![صفحة مستودع التكوين](./media/er-download-configurations-global-repo-repository-content.png)

## <a name="import-filtered-configurations"></a><span data-ttu-id="0daec-130">استيراد تكوينات تمت تصفيتها</span><span class="sxs-lookup"><span data-stu-id="0daec-130">Import filtered configurations</span></span>

1. <span data-ttu-id="0daec-131">في الصفحة **مستودعات التكوين**، في شجره التكوينات، قم بتوسيع علامة التبويب السريعة **عامل التصفية**.</span><span class="sxs-lookup"><span data-stu-id="0daec-131">On the **Configuration repositories** page, in the configurations tree, expand the **Filter** FastTab.</span></span>
2. <span data-ttu-id="0daec-132">في شبكة **العلامات**، أضف أي علامات.</span><span class="sxs-lookup"><span data-stu-id="0daec-132">In the **Tags** grid, add any tags that are needed.</span></span>
3. <span data-ttu-id="0daec-133">في الحقل **إمكانية التطبيق على البلد/المنطقة** حدد رموز البلدان/المنطقة المناسبة، ثم حدد **تطبيق عامل التصفية**.</span><span class="sxs-lookup"><span data-stu-id="0daec-133">In the **Country/region applicability** field, select the appropriate country/region codes, and then select  **Apply filter**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0daec-134">تعرض علامة التبويب السريعة **التكوينات** جميع التكوينات التي تفي بشروط التحديد المعينة.</span><span class="sxs-lookup"><span data-stu-id="0daec-134">The **Configurations** FastTab shows all the configurations that satisfy the specified selection conditions.</span></span>

4. <span data-ttu-id="0daec-135">على علامة التبويب السريعة **التكوينات**، حدد **استيراد** لتنزيل التكوينات التي تمت تصفيتها من المستودع العمومي إلى المثيل الحالي.</span><span class="sxs-lookup"><span data-stu-id="0daec-135">On the **Configurations** FastTab, select **Import** to download the filtered configurations from the Global repository to the current instance.</span></span>
5. <span data-ttu-id="0daec-136">على علامة التبويب السريعة **التكوينات**، حدد **إعادة تعيين عامل التصفية** لتنظيف شروط التحديد المعينة.</span><span class="sxs-lookup"><span data-stu-id="0daec-136">On the **Configurations** FastTab, select **Reset filter** to clean up the specified selection conditions.</span></span>

    ![صفحة مستودع التكوين](./media/er-download-configurations-global-repo-filtered-configurations.png)

> [!NOTE]
> <span data-ttu-id="0daec-138">استنادًا إلى إعدادات التقارير الإلكترونية، يتم التحقق من صحة التكوينات بعد استيرادها.</span><span class="sxs-lookup"><span data-stu-id="0daec-138">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="0daec-139">قد يتم إعلامك بأي مشكلات عدم التوافق التي يتم اكتشافها.</span><span class="sxs-lookup"><span data-stu-id="0daec-139">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="0daec-140">قبل أن تتمكن من استخدام إصدار التكوين المستورد، يجب حل المشاكل.</span><span class="sxs-lookup"><span data-stu-id="0daec-140">Before you can use the imported configuration version, you must resolve the issues.</span></span> <span data-ttu-id="0daec-141">لمزيد من المعلومات، راجع قائمة الموارد ذات الصلة لهذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="0daec-141">For more information, see the list of related resources for this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="0daec-142">يمكن تكوين تكوينات التقارير الإلكترونية على أنها تعتمد على تكوينات أخرى.</span><span class="sxs-lookup"><span data-stu-id="0daec-142">ER configurations can be configured as being dependent on other configurations.</span></span> <span data-ttu-id="0daec-143">وبالتالي، قد يتم استيراد تكوينات أخرى، إلى جانب تكوين محدد، بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="0daec-143">Therefore, along with a selected configuration, other configurations might be automatically imported.</span></span> <span data-ttu-id="0daec-144">لمزيد من المعلومات حول تبعيات التكوين، راجع [تحديد تبعية تكوينات التقارير الإلكترونية (ER) على مكونات أخرى‬](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md).</span><span class="sxs-lookup"><span data-stu-id="0daec-144">For more about configuration dependencies, see [Define the dependency of ER configurations on other components](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0daec-145">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="0daec-145">Additional resources</span></span>

[<span data-ttu-id="0daec-146">نظرة عامة على إعداد التقارير الإلكترونية (ER)</span><span class="sxs-lookup"><span data-stu-id="0daec-146">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
