---
title: تنزيل تكوينات التقارير الإلكترونية من Lifecycle Services
description: يوضح هذا الموضوع كيفية تنزيل تكوينات التقارير الإلكترونية من Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 14f0f2b1a4d63101d432b1361379c61a70ac9345
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271173"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="6e59c-103">تنزيل تكوينات إعداد التقارير الإلكترونية من Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="6e59c-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e59c-104">يشرح هذا الموضوع كيفية تنزيل أحدث إصدار من [تكوينات التقارير الإلكترونية](general-electronic-reporting.md#Configuration) من [مكتبة الأصول المشتركة](../lifecycle-services/asset-library.md) في Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="6e59c-104">This topic explains how to download the newest version of [Electronic reporting (ER) configurations](general-electronic-reporting.md#Configuration) from the [Shared asset library](../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6e59c-105">إن استخدام LCS كمستودع تخزين لتكوينات التقارير الإلكترونية يكون [مهملاً](../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span><span class="sxs-lookup"><span data-stu-id="6e59c-105">The use of LCS as a storage repository for ER configurations is being [deprecated](../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span></span> <span data-ttu-id="6e59c-106">لمزيد من المعلومات، [إهلاك تخزين Regulatory Configuration Service (RCS) – Lifecycle Services (LCS)](../../../finance/localizations/rcs-lcs-repo-dep-faq.md)</span><span class="sxs-lookup"><span data-stu-id="6e59c-106">For more information, see [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span></span>

1. <span data-ttu-id="6e59c-107">سجّل دخولك إلى التطبيق باستخدام أحد الأدوار التالية:</span><span class="sxs-lookup"><span data-stu-id="6e59c-107">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="6e59c-108">مطور إعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="6e59c-108">Electronic reporting developer</span></span>
    - <span data-ttu-id="6e59c-109">مستشار وظيفي لإعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="6e59c-109">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="6e59c-110">مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="6e59c-110">System administrator</span></span>

2. <span data-ttu-id="6e59c-111">انتقل إلى **إدارة المؤسسة** &gt; **مساحات العمل** &gt; **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="6e59c-111">Go to **Organization administration** &gt; **Workspaces** &gt; **Electronic reporting**.</span></span>
3. <span data-ttu-id="6e59c-112">في مقطع **موفرو التكوين**، حدد لوحة **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="6e59c-112">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4. <span data-ttu-id="6e59c-113">على لوحة **Microsoft**، حدد **مستودعات**.</span><span class="sxs-lookup"><span data-stu-id="6e59c-113">On the **Microsoft** tile, select **Repositories**.</span></span>

    <span data-ttu-id="6e59c-114">[![لوحة Microsoft في صفحة تكوينات الترجمة](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="6e59c-114">[![Microsoft tile on the Localization configurations page](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>

5. <span data-ttu-id="6e59c-115">في صفحة **مستودعات التكوين**، في الشبكة، حدد المستودع الموجود من النوع **LCS**.</span><span class="sxs-lookup"><span data-stu-id="6e59c-115">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="6e59c-116">إذا لم يظهر هذا المستودع في الشبكة، فاتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="6e59c-116">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="6e59c-117">حدد **إضافة** لإضافة مستودع.</span><span class="sxs-lookup"><span data-stu-id="6e59c-117">Select **Add** to add a repository.</span></span>
    2. <span data-ttu-id="6e59c-118">حدد **LCS** كنوع المستودع.</span><span class="sxs-lookup"><span data-stu-id="6e59c-118">Select **LCS** as the repository type.</span></span>
    3. <span data-ttu-id="6e59c-119">حدد **إنشاء مستودع**.</span><span class="sxs-lookup"><span data-stu-id="6e59c-119">Select **Create repository**.</span></span>
    4. <span data-ttu-id="6e59c-120">إذا تمت مطالبتك بالتخويل، فاتبع الإرشادات التي تظهر على الشاشة.</span><span class="sxs-lookup"><span data-stu-id="6e59c-120">If you're prompted about authorization, follow the on-screen instructions.</span></span>
    5. <span data-ttu-id="6e59c-121">قم بإدخال اسم ووصف للمستودع.</span><span class="sxs-lookup"><span data-stu-id="6e59c-121">Enter a name and description for the repository.</span></span>
    6. <span data-ttu-id="6e59c-122">حدد **موافق** لتأكيد إدخال المستودع الجديد.</span><span class="sxs-lookup"><span data-stu-id="6e59c-122">Select **OK** to confirm the new repository entry.</span></span>
    7. <span data-ttu-id="6e59c-123">في الشبكة، حدد المستودع الجديد من النوع **LCS‎**.</span><span class="sxs-lookup"><span data-stu-id="6e59c-123">In the grid, select the new repository of the **LCS** type.</span></span>

6. <span data-ttu-id="6e59c-124">حدد **فتح** لعرض قائمة تكوينات التقارير الإلكترونية للمستودع المحدد.</span><span class="sxs-lookup"><span data-stu-id="6e59c-124">Select **Open** to view the list of ER configurations for the selected repository.</span></span>

    <span data-ttu-id="6e59c-125">[![صفحة مستودعات التكوين](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="6e59c-125">[![Configuration repositories page](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>

    > [!TIP]
    > <span data-ttu-id="6e59c-126">إذا واجهت مشكلة في الوصول إلى مستودع LCS لتنزيل التكوينات من مكتبة الأصول المشتركة في LCS، فيمكنك تنزيل التكوينات من [المستودع العمومي](er-download-configurations-global-repo.md) بدلاً من ذلك.</span><span class="sxs-lookup"><span data-stu-id="6e59c-126">If you have trouble accessing the LCS repository to download configurations from the Shared asset library in LCS, you can download configurations from the [Global repository](er-download-configurations-global-repo.md) instead.</span></span>

7. <span data-ttu-id="6e59c-127">في شجرة التكوينات في الجزء الأيمن، حدد تكوين التقارير الإلكترونية المطلوب.</span><span class="sxs-lookup"><span data-stu-id="6e59c-127">In the configurations tree in the left pane, select the required ER configuration.</span></span>
8. <span data-ttu-id="6e59c-128">على علامة التبويب السريعة **إصدارات**، حدد الإصدار المطلوب لتكوين التقارير الإلكترونية المحدد.</span><span class="sxs-lookup"><span data-stu-id="6e59c-128">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9. <span data-ttu-id="6e59c-129">حدد **استيراد** لتنزيل الإصدار المحدد من LCS إلى المثيل الحالي.</span><span class="sxs-lookup"><span data-stu-id="6e59c-129">Select **Import** to download the selected version from LCS to the current instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6e59c-130">لا يتوفر الزر **استيراد** لإصدارات تكوينات التقارير الإلكترونية الموجودة في المثيل الحالي.</span><span class="sxs-lookup"><span data-stu-id="6e59c-130">The **Import** button is unavailable for ER configuration versions that are already present in the current instance.</span></span>

    <span data-ttu-id="6e59c-131">[![صفحة مستودع التكوين](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="6e59c-131">[![Configuration repository page](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="6e59c-132">استنادًا إلى إعدادات التقارير الإلكترونية، يتم التحقق من صحة التكوينات بعد استيرادها.</span><span class="sxs-lookup"><span data-stu-id="6e59c-132">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="6e59c-133">قد يتم إعلامك بأي مشكلات عدم التوافق التي يتم اكتشافها.</span><span class="sxs-lookup"><span data-stu-id="6e59c-133">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="6e59c-134">يجب حل هذه المشكلات قبل أن تتمكن من استخدام إصدار التكوين المستورد.</span><span class="sxs-lookup"><span data-stu-id="6e59c-134">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="6e59c-135">لمزيد من المعلومات، راجع قائمة المواضيع ذات الصلة لهذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="6e59c-135">For more information, see the list of related topics for this topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6e59c-136">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="6e59c-136">Additional resources</span></span>

[<span data-ttu-id="6e59c-137">نظرة عامة على إعداد التقارير الإلكترونية (ER)</span><span class="sxs-lookup"><span data-stu-id="6e59c-137">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="6e59c-138">تنزيل تكوينات التقارير الإلكترونية من المستودع العمومي لخدمة التكوين</span><span class="sxs-lookup"><span data-stu-id="6e59c-138">Download ER configurations from the Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
