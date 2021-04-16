---
title: ضبط تنسيق ER لإنشاء مستند إلكتروني مخصص
description: يوضح هذا الموضوع كيفية تعديل تنسيق التقارير الإلكترونية (ER) المقدمة من Microsoft بحيث تقوم بإنشاء مستند إلكتروني مخصص.
author: NickSelin
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7355fbb3321a6b5707ab561e88aed2d22cc967cd
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743643"
---
# <a name="adjust-an-er-format-to-generate-a-custom-electronic-document"></a><span data-ttu-id="d59a4-103">ضبط تنسيق ER لإنشاء مستند إلكتروني مخصص</span><span class="sxs-lookup"><span data-stu-id="d59a4-103">Adjust an ER format to generate a custom electronic document</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d59a4-104">توضح الإجراءات الواردة في هذا الموضوع كيفية قيام مستخدم بدور مسؤول النظام أو مستشار وظيفة التقارير الإلكترونية بإجراء هذه المهام:</span><span class="sxs-lookup"><span data-stu-id="d59a4-104">The procedures in this topic explain how a user in the System Administrator or Electronic Reporting Functional Consultant role can perform these tasks:</span></span>

- <span data-ttu-id="d59a4-105">تكوين معلمات [لإطار عمل التقارير الإلكترونية (ER)](general-electronic-reporting.md)</span><span class="sxs-lookup"><span data-stu-id="d59a4-105">Configure parameters for the [Electronic reporting (ER) framework](general-electronic-reporting.md).</span></span>
- <span data-ttu-id="d59a4-106">استيراد تكوينات ER التي يتم توفيرها بواسطة Microsoft واستخدامها لإنشاء ملف دفع أثناء معالجة [مدفوعات المورد](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d59a4-106">Import ER configurations that are provided by Microsoft and used to generate a payment file while a [vendor payment](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md) is being processed.</span></span>
- <span data-ttu-id="d59a4-107">إنشاء إصدار مخصص من تكوين تنسيق ER القياسي الذي يتم توفيره بواسطة Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d59a4-107">Create a custom version of a standard ER format configuration that is provided by Microsoft.</span></span>
- <span data-ttu-id="d59a4-108">تعديل تكوين التنسيق ER المخصص بحيث يقوم بإنشاء ملفات دفع تتوافق مع متطلبات بنك معين.</span><span class="sxs-lookup"><span data-stu-id="d59a4-108">Modify the custom ER format configuration so that it generates payment files that meets the requirements of a specific bank.</span></span>
- <span data-ttu-id="d59a4-109">تبني التغييرات التي يتم إجراؤها على تكوين التنسيق ER القياسي في تكوين تنسيق ER المخصص.</span><span class="sxs-lookup"><span data-stu-id="d59a4-109">Adopt changes that are made to the standard ER format configuration in the custom ER format configuration.</span></span>

<span data-ttu-id="d59a4-110">يمكن إجراء كافة الإجراءات التالية في شركة **GBSI**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-110">All the following procedures can be done in the **GBSI** company.</span></span> <span data-ttu-id="d59a4-111">الترميز غير مطلوب.</span><span class="sxs-lookup"><span data-stu-id="d59a4-111">No coding is required.</span></span>

- [<span data-ttu-id="d59a4-112">تكوين إطار عمل ER</span><span class="sxs-lookup"><span data-stu-id="d59a4-112">Configure the ER framework</span></span>](#ConfigureFramework)

    - [<span data-ttu-id="d59a4-113">تكوين معلمات التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="d59a4-113">Configure ER parameters</span></span>](#ConfigureParameters)
    - [<span data-ttu-id="d59a4-114">تنشيط موفر تكوين ER</span><span class="sxs-lookup"><span data-stu-id="d59a4-114">Activate an ER configuration provider</span></span>](#ActivateProvider)

        - [<span data-ttu-id="d59a4-115">مراجعة قائمة موفري تكوين ER</span><span class="sxs-lookup"><span data-stu-id="d59a4-115">Review the list of ER configuration providers</span></span>](#ReviewProvidersList)
        - [<span data-ttu-id="d59a4-116">إضافة موفر تكوين ER جديد</span><span class="sxs-lookup"><span data-stu-id="d59a4-116">Add a new ER configuration provider</span></span>](#ActivateProvider)
        - [<span data-ttu-id="d59a4-117">تنشيط موفر تكوين ER</span><span class="sxs-lookup"><span data-stu-id="d59a4-117">Activate an ER configuration provider</span></span>](#ActivateAddedProvider)

- [<span data-ttu-id="d59a4-118">استيراد تكوينات تنسيق ER القياسية</span><span class="sxs-lookup"><span data-stu-id="d59a4-118">Import the standard ER format configurations</span></span>](#ImportERSolution1)

    - [<span data-ttu-id="d59a4-119">استيراد تكوينات تنسيق ER القياسية</span><span class="sxs-lookup"><span data-stu-id="d59a4-119">Import the standard ER configurations</span></span>](#ImportERFormat1)
    - [<span data-ttu-id="d59a4-120">مراجعة تكوينات ER المستوردة</span><span class="sxs-lookup"><span data-stu-id="d59a4-120">Review the imported ER configurations</span></span>](#ReviewImportedERSolution)

- [<span data-ttu-id="d59a4-121">تجهيز مدفوعات المورد للمعالجة</span><span class="sxs-lookup"><span data-stu-id="d59a4-121">Prepare a vendor payment for processing</span></span>](#PrepareVendorPayment)

    - [<span data-ttu-id="d59a4-122">إضافة معلومات البنك لحساب مورد</span><span class="sxs-lookup"><span data-stu-id="d59a4-122">Add bank information for a vendor account</span></span>](#AddBankAccount)
    - [<span data-ttu-id="d59a4-123">إدخال مدفوعات المورد</span><span class="sxs-lookup"><span data-stu-id="d59a4-123">Enter a vendor payment</span></span>](#EnterVendorPayment)

- [<span data-ttu-id="d59a4-124">معالجة مدفوعات المورد باستخدام تنسيق ER القياسي</span><span class="sxs-lookup"><span data-stu-id="d59a4-124">Process a vendor payment by using the standard ER format</span></span>](#ProcessVendorPayment1)

    - [<span data-ttu-id="d59a4-125">إعداد طريقة الدفع الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="d59a4-125">Set up the electronic payment method</span></span>](#ConfigureMethodOfPayment1)
    - [<span data-ttu-id="d59a4-126">معالجة مدفوعات مورد</span><span class="sxs-lookup"><span data-stu-id="d59a4-126">Process a vendor payment</span></span>](#ProcessPayment1)

- [<span data-ttu-id="d59a4-127">تخصيص تنسيق ER القياسي</span><span class="sxs-lookup"><span data-stu-id="d59a4-127">Customize the standard ER format</span></span>](#CustomizeProvidedFormat)

    - [<span data-ttu-id="d59a4-128">إنشاء تنسيق مخصص</span><span class="sxs-lookup"><span data-stu-id="d59a4-128">Create a custom format</span></span>](#DeriveProvidedFormat)
    - [<span data-ttu-id="d59a4-129">تحرير تنسيق مخصص</span><span class="sxs-lookup"><span data-stu-id="d59a4-129">Edit a custom format</span></span>](#ConfigureDerivedFormat)
    - [<span data-ttu-id="d59a4-130">تعليم تنسيق مخصص على أنه قابل للتشغيل</span><span class="sxs-lookup"><span data-stu-id="d59a4-130">Mark a custom format as runnable</span></span>](#MarkFormatRunnable)

- [<span data-ttu-id="d59a4-131">معالجة مدفوعات المورد باستخدام تنسيق ER مخصص</span><span class="sxs-lookup"><span data-stu-id="d59a4-131">Process a vendor payment by using the custom ER format</span></span>](#ProcessVendorPayment2)

    - [<span data-ttu-id="d59a4-132">إعداد طريقة الدفع الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="d59a4-132">Set up the electronic payment method</span></span>](#ConfigureMethodOfPayment2)
    - [<span data-ttu-id="d59a4-133">معالجة مدفوعات مورد</span><span class="sxs-lookup"><span data-stu-id="d59a4-133">Process a vendor payment</span></span>](#ProcessPayment2)

- [<span data-ttu-id="d59a4-134">استيراد إصدارات جديدة من تكوينات تنسيق ER القياسية</span><span class="sxs-lookup"><span data-stu-id="d59a4-134">Import new versions of the standard ER format configurations</span></span>](#ImportERSolution2)

    - [<span data-ttu-id="d59a4-135">استيراد إصدارات جديدة من تكوينات ER القياسية</span><span class="sxs-lookup"><span data-stu-id="d59a4-135">Import new versions of the standard ER configurations</span></span>](#ImportERFormat2)
    - [<span data-ttu-id="d59a4-136">مراجعة تكوينات تنسيق ER المستوردة</span><span class="sxs-lookup"><span data-stu-id="d59a4-136">Review the imported ER format configurations</span></span>](#ReviewImportedERFormat)

- [<span data-ttu-id="d59a4-137">تبني التغييرات في الإصدار الجديد من تنسيق مستورد في تنسيق مخصص</span><span class="sxs-lookup"><span data-stu-id="d59a4-137">Adopt the changes in the new version of an imported format in a custom format</span></span>](#AdoptNewBaseVersion)

    - [<span data-ttu-id="d59a4-138">إكمال إصدار المسودة الحالي لتنسيق مخصص</span><span class="sxs-lookup"><span data-stu-id="d59a4-138">Complete the current draft version of a custom format</span></span>](#CompleteDerivedFormat)
    - [<span data-ttu-id="d59a4-139">إعادة تعريف تنسيق مخصص إلى إصدار أساسي جديد</span><span class="sxs-lookup"><span data-stu-id="d59a4-139">Rebase a custom format to a new base version</span></span>](#RebaseDerivedFormat)
    - [<span data-ttu-id="d59a4-140">معالجة مدفوعات المورد باستخدام تنسيق ER معاد تعريفه</span><span class="sxs-lookup"><span data-stu-id="d59a4-140">Process a vendor payment by using a rebased ER format</span></span>](#ProcessPayment3)

- [<span data-ttu-id="d59a4-141">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="d59a4-141">Additional resources</span></span>](#References)

## <a name="configure-the-er-framework"></a><a id="ConfigureFramework"></a><span data-ttu-id="d59a4-142">تكوين إطار عمل ER</span><span class="sxs-lookup"><span data-stu-id="d59a4-142">Configure the ER framework</span></span>

<span data-ttu-id="d59a4-143">كمستخدم بدور المستشار الوظيفي للتقارير الإلكترونية، يجب عليك تكوين مجموعة صغيرة من معلمات ER قبل البدء في استخدام الإطار الأساسي ER لتصميم إصدار مخصص من التنسيق ER القياسي.</span><span class="sxs-lookup"><span data-stu-id="d59a4-143">As a user in the Electronic Reporting Functional Consultant role, you must configure the minimal set of ER parameters before you can start to use the ER framework to design a custom version of a standard ER format.</span></span>

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a><span data-ttu-id="d59a4-144">تكوين معلمات التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="d59a4-144">Configure ER parameters</span></span>

1. <span data-ttu-id="d59a4-145">انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-145">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="d59a4-146">في الصفحة **تكوينات الترجمة**، في قسم **الارتباطات المتعلقة**، حدد **معلمات التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-146">On the **Localization configurations** page, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="d59a4-147">في صفحة **معلمات التقارير الإلكترونية**، على علامة التبويب **عام**، عيّن الخيار **تمكين وضع التصميم** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-147">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="d59a4-148">في علامة التبويب **المرفقات**، عيّن المعلمات التالية:</span><span class="sxs-lookup"><span data-stu-id="d59a4-148">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="d59a4-149">في حقل **التكوينات**، حدد نوع **الملف** لشركة **USMF**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-149">In the **Configurations** field, select the **File** type for the **USMF** company.</span></span>
    - <span data-ttu-id="d59a4-150">في حقول **أرشيف الوظيفة** و **المؤقت** و **الأساس** و **أخرى**، حدد نوع **الملف**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-150">In the **Job archive**, **Temporary**, **Baseline**, and **Others** fields, select the **File** type.</span></span>

<span data-ttu-id="d59a4-151">لمزيد من المعلومات حول معلمات ER ، راجع [تكوين إطار عمل ER](electronic-reporting-er-configure-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d59a4-151">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="d59a4-152">تنشيط موفر تكوين ER</span><span class="sxs-lookup"><span data-stu-id="d59a4-152">Activate an ER configuration provider</span></span>

<span data-ttu-id="d59a4-153">يتم تعليم كل تكوين ER تمت إضافته باعتباره مملوكا لموفر تكوين ER.</span><span class="sxs-lookup"><span data-stu-id="d59a4-153">Every ER configuration that is added is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="d59a4-154">يتم استخدام موفر تكوين ER الذي تم تنشيطه في مساحة عمل **التقارير الإلكترونية** لهذا الغرض.</span><span class="sxs-lookup"><span data-stu-id="d59a4-154">The ER configuration provider that is activated in the **Electronic reporting** workspace is used for this purpose.</span></span> <span data-ttu-id="d59a4-155">بالتالي، يجب عليك تنشيط موفر تكوين ER في مساحة عمل **التقارير الإلكترونية** قبل البدء في إضافة تكوينات ER أو تحريرها.</span><span class="sxs-lookup"><span data-stu-id="d59a4-155">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="d59a4-156">يمكن لمالك تكوين ER فقط تحريره.</span><span class="sxs-lookup"><span data-stu-id="d59a4-156">Only the owner of an ER configuration can edit it.</span></span> <span data-ttu-id="d59a4-157">بالتالي، قبل تحرير تكوين ER، يجب تنشيط موفر تكوين ER المناسب في مساحة عمل **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-157">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a><span data-ttu-id="d59a4-158">مراجعة قائمة موفري تكوين ER</span><span class="sxs-lookup"><span data-stu-id="d59a4-158">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="d59a4-159">انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-159">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="d59a4-160">في الصفحة **تكوينات الترجمة**، في قسم **الارتباطات المتعلقة**، حدد **موفري التكوين** .</span><span class="sxs-lookup"><span data-stu-id="d59a4-160">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="d59a4-161">في صفحة **جدول موفري التكوين**، يتضمن كل سجل موفر اسمًا وعنوان URL فريدين.</span><span class="sxs-lookup"><span data-stu-id="d59a4-161">On the **Configuration provider table** page, each provider record has a unique name and URL.</span></span> <span data-ttu-id="d59a4-162">راجع محتويات هذه الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d59a4-162">Review the contents of this page.</span></span> <span data-ttu-id="d59a4-163">في حالة وجود سجل لـ **Litware, Inc.** (`https://www.litware.com`) بالفعل، فتخطي الإجراء التالي، [إضافة موفر تكوين ER جديد](#ActivateProvider).</span><span class="sxs-lookup"><span data-stu-id="d59a4-163">If a record for **Litware, Inc.** (`https://www.litware.com`) already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="d59a4-164">إضافة موفر تكوين ER جديد</span><span class="sxs-lookup"><span data-stu-id="d59a4-164">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="d59a4-165">انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-165">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="d59a4-166">في الصفحة **تكوينات الترجمة**، في قسم **الارتباطات المتعلقة**، حدد **موفري التكوين** .</span><span class="sxs-lookup"><span data-stu-id="d59a4-166">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="d59a4-167">في صفحة **موفري التكوين**، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-167">On the **Configuration providers** page, select **New**.</span></span>
4. <span data-ttu-id="d59a4-168">في حقل **الاسم**، أدخل **Litware, Inc**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-168">In the **Name** field, enter **Litware, Inc.**</span></span>
5. <span data-ttu-id="d59a4-169">في الحقل **عنوان الإنترنت**، أدخل `https://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="d59a4-169">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
6. <span data-ttu-id="d59a4-170">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-170">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a><span data-ttu-id="d59a4-171">تنشيط موفر تكوين ER</span><span class="sxs-lookup"><span data-stu-id="d59a4-171">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="d59a4-172">انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-172">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="d59a4-173">في صفحة **تكوينات التعريب**، في القسم **موفري التكوين**، حدد تجانب **Litware, Inc.** ثم حدد **تعيين نشط**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-173">On the **Localization configurations** page, in the **Configuration providers** section, select the **Litware, Inc.** tile, and then select **Set active**.</span></span>

<span data-ttu-id="d59a4-174">لمزيد من المعلومات حول موفري تكوين ER، راجع [إنشاء موفري التكوين ووضع علامة عليهم كنشطين](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="d59a4-174">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a><span data-ttu-id="d59a4-175">استيراد تكوينات تنسيق ER القياسية</span><span class="sxs-lookup"><span data-stu-id="d59a4-175">Import the standard ER format configurations</span></span>

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat1"></a><span data-ttu-id="d59a4-176">استيراد تكوينات تنسيق ER القياسية</span><span class="sxs-lookup"><span data-stu-id="d59a4-176">Import the standard ER configurations</span></span>

<span data-ttu-id="d59a4-177">لإضافة تكوينات ER القياسية إلى المثيل الحالي من Microsoft Dynamics 365 Finance، يجب استيرادها من [مستودع](general-electronic-reporting.md#Repository) ERالذي تم تكوينه لهذا المثيل.</span><span class="sxs-lookup"><span data-stu-id="d59a4-177">To add the standard ER configurations to your current instance of Microsoft Dynamics 365 Finance, you must import them from the ER [repository](general-electronic-reporting.md#Repository) that was configured for that instance.</span></span>

1. <span data-ttu-id="d59a4-178">انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-178">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="d59a4-179">في صفحة **تكوينات التعريب**، في قسم **موفري التكوين**، حدد تجانب **Microsoft**، ثم حدد **المستودعات** لعرض قائمة المستودعات الخاصة بموفر Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d59a4-179">On the **Localization configurations** page, in the **Configuration providers** section, select the **Microsoft** tile, and then select **Repositories** to view the list of repositories for the Microsoft provider.</span></span>
3. <span data-ttu-id="d59a4-180">في صفحة **مستودعات التكوين**، حدد المستودع من نوع **عام**، ثم حدد **فتح**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-180">On the **Configuration repositories** page, select the repository of the **Global** type, and then select **Open**.</span></span> <span data-ttu-id="d59a4-181">في حالة مطالبتك بالتخويل للاتصال بخدمة Regulatory Configuration Service، اتبع إرشادات التخويل.</span><span class="sxs-lookup"><span data-stu-id="d59a4-181">If you're prompted for authorization to connect to Regulatory Configuration Service, follow the authorization instructions.</span></span>
4. <span data-ttu-id="d59a4-182">في صفحة **مستودع التكوين**، في شجرة التكوينات في الجزء الأيسر، حدد تكوين تنسيق **BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-182">On the **Configuration repository** page, in the configuration tree in the left pane, select the **BACS (UK)** format configuration.</span></span>
5. <span data-ttu-id="d59a4-183">على علامة التبويب السريعة **إصدارات**، حدد الإصدار **1.1** لتكوين تنسيق ER المحدد.</span><span class="sxs-lookup"><span data-stu-id="d59a4-183">On the **Versions** FastTab, select version **1.1** of the selected ER format configuration.</span></span>
6. <span data-ttu-id="d59a4-184">حدد **استيراد** لتنزيل الإصدار المحدد من المستودع العمومي إلى مثيل Finance الحالي.</span><span class="sxs-lookup"><span data-stu-id="d59a4-184">Select **Import** to download the selected version from the Global repository to the current Finance instance.</span></span>

![صفحة مستودع التكوين](./media/er-quick-start2-import-solution1.png)

> [!TIP]
> <span data-ttu-id="d59a4-186">إذا كانت لديك مشكلة في الوصول إلى [المستودع العمومي](er-download-configurations-global-repo.md)، فيمكنك [تنزيل التكوينات](download-electronic-reporting-configuration-lcs.md) من Microsoft Dynamics Lifecycle Services (LCS) بدلا من ذلك.</span><span class="sxs-lookup"><span data-stu-id="d59a4-186">If you have trouble accessing the [Global repository](er-download-configurations-global-repo.md), you can [download configurations](download-electronic-reporting-configuration-lcs.md) from Microsoft Dynamics Lifecycle Services (LCS) instead.</span></span>

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a><span data-ttu-id="d59a4-187">مراجعة تكوينات ER المستوردة</span><span class="sxs-lookup"><span data-stu-id="d59a4-187">Review the imported ER configurations</span></span>

1. <span data-ttu-id="d59a4-188">انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-188">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="d59a4-189">في الصفحة **تكوينات الترجمة**، في قسم **التكوينات**، حدد تجانب **تكوينات إعداد التقارير** .</span><span class="sxs-lookup"><span data-stu-id="d59a4-189">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="d59a4-190">في صفحة **التكوينات**، في شجرة التكوينات، الجزء الأيسر، وسَّع **نموذج الدفع**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-190">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**.</span></span>
4. <span data-ttu-id="d59a4-191">لاحظ أنه، بالإضافة إلى تنسيق ER **BACS (UK)** المحدد، تم استيراد تكوينات ER الأخرى.</span><span class="sxs-lookup"><span data-stu-id="d59a4-191">Notice that, in addition to the selected **BACS (UK)** ER format, other required ER configurations were imported.</span></span> <span data-ttu-id="d59a4-192">تأكد من توفر تكوينات ER التالية في شجره التكوين:</span><span class="sxs-lookup"><span data-stu-id="d59a4-192">Make sure that the following ER configurations are available in the configuration tree:</span></span>

    - <span data-ttu-id="d59a4-193">**نموذج الدفع** -يحتوي هذا التكوين على مكون ER [نموذج البيانات](general-electronic-reporting.md#data-model-and-model-mapping-components) الذي يمثل بنية البيانات الخاصة بمجال أعمال الدفع.</span><span class="sxs-lookup"><span data-stu-id="d59a4-193">**Payment model** – This configuration contains the [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) ER component that represents the data structure of the payment business domain.</span></span>
    - <span data-ttu-id="d59a4-194">**تعيين نموذج الدفع 1611** – يحتوي هذا التكوين على مكون ER الخاص بـ [تعيين النموذج](general-electronic-reporting.md#data-model-and-model-mapping-components) الذي يوضح كيفية ملء نموذج البيانات ببيانات التطبيق في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="d59a4-194">**Payment model mapping 1611** – This configuration contains the [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) ER component that describes how the data model is filled in with application data at runtime.</span></span>
    - <span data-ttu-id="d59a4-195">**BACS (UK)** – يحتوي هذا التكوين على [التنسيق](general-electronic-reporting.md#FormatComponentOutbound) ومكونات ER لتعيين التنسيق.</span><span class="sxs-lookup"><span data-stu-id="d59a4-195">**BACS (UK)** – This configuration contains the [format](general-electronic-reporting.md#FormatComponentOutbound) and format mapping ER components.</span></span> <span data-ttu-id="d59a4-196">يحدد مكون التنسيق تخطيط التقرير.</span><span class="sxs-lookup"><span data-stu-id="d59a4-196">The format component specifies the report layout.</span></span> <span data-ttu-id="d59a4-197">يحتوي مكون تعيين التنسيق على مصدر بيانات النموذج ويحدد كيفية ملء تخطيط التقرير باستخدام مصدر البيانات هذا في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="d59a4-197">The format mapping component contains the model data source and specifies how the report layout is filled in by using this data source at runtime.</span></span>

![صفحة التكوينات](./media/er-quick-start2-imported-solution1.png)

## <a name="prepare-a-vendor-payment-for-processing"></a><a id="PrepareVendorPayment"></a><span data-ttu-id="d59a4-199">تجهيز مدفوعات المورد للمعالجة</span><span class="sxs-lookup"><span data-stu-id="d59a4-199">Prepare a vendor payment for processing</span></span>

### <a name="add-bank-information-for-a-vendor-account"></a><a id="AddBankAccount"></a><span data-ttu-id="d59a4-200">إضافة معلومات البنك لحساب مورد</span><span class="sxs-lookup"><span data-stu-id="d59a4-200">Add bank information for a vendor account</span></span>

<span data-ttu-id="d59a4-201">يجب إضافة معلومات البنك لحساب مورد والذي ستتم الإشارة إليه لاحقا في عملية دفع مسجلة.</span><span class="sxs-lookup"><span data-stu-id="d59a4-201">You must add bank information for a vendor account that will be referred to later in a registered payment.</span></span>

1. <span data-ttu-id="d59a4-202">انتقل إلى **الحسابات الدائنة** \> **الموردون** \> **كافة الموردين**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-202">Go to **Accounts payable** \> **Vendors** \> **All vendors**.</span></span>
2. <span data-ttu-id="d59a4-203">في صفحة **كافة الموردين**، حدد حساب المورد **GB_SI_000001**، ثم، في جزء الإجراءات، في علامة تبويب **المورد**، في مجموعة **الإعداد**، حدد **الحسابات البنكية**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-203">On the **All vendors** page, select the **GB_SI_000001** vendor account, and then, on the Action Pane, on the **Vendor** tab, in the **Set up** group, select **Bank accounts**.</span></span>
3. <span data-ttu-id="d59a4-204">في صفحة **الحسابات البنكية للمورد**، حدد **جديد**، ثم أدخل المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="d59a4-204">On the **Vendor bank accounts** page, select **New**, and then enter the following information:</span></span>

    1. <span data-ttu-id="d59a4-205">في الحقل **حساب البنك** أدخل **GBP OPER**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-205">In the **Bank account** field, enter **GBP OPER**.</span></span>
    2. <span data-ttu-id="d59a4-206">في حقل **مجموعات البنك**، حدد **BankGBP**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-206">In the **Bank groups** field, select **BankGBP**.</span></span>
    3. <span data-ttu-id="d59a4-207">في الحقل **رقم حساب البنك** أدخل **202015**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-207">In the **Bank account number** field, enter **202015**.</span></span>
    4. <span data-ttu-id="d59a4-208">في حقل **رمز SWIFT**، أدخل <a id="DefineSWIFTCode"></a>**CHASDEFXXXX**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-208">In the **SWIFT code** field, enter <a id="DefineSWIFTCode"></a>**CHASDEFXXXX**.</span></span>
    5. <span data-ttu-id="d59a4-209">في حقل **IBAN**، أدخل **GB33BUKB20201555555555**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-209">In the **IBAN** field, enter **GB33BUKB20201555555555**.</span></span>
    6. <span data-ttu-id="d59a4-210">في حقل **رقم التوجيه**، احتفظ بالقيمة الافتراضية، <a id="DefineRoutingNumber"></a>**123456**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-210">In the **Routing number** field, keep the default value, <a id="DefineRoutingNumber"></a>**123456**.</span></span>

    ![صفحة الحسابات البنكية للمورد](./media/er-quick-start2-bank-account.png)

4. <span data-ttu-id="d59a4-212">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-212">Select **Save**.</span></span>
5. <span data-ttu-id="d59a4-213">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d59a4-213">Close the page.</span></span>
6. <span data-ttu-id="d59a4-214">في صفحة **كافة الموردين**، افتح حساب المورد **GB_SI_000001**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-214">On the **All vendors** page, open the **GB_SI_000001** vendor account.</span></span>
7. <span data-ttu-id="d59a4-215">في صفحة تفاصيل المورد، حدد **تحرير** لجعل الصفحة قابلة للتحرير، إذا كان ذلك مطلوبًا.</span><span class="sxs-lookup"><span data-stu-id="d59a4-215">On the vendor details page, select **Edit** to make the page editable, if required.</span></span>
8. <span data-ttu-id="d59a4-216">في علامة التبويب السريعة **المدفوعات**، في حقل **الحساب البنكي**، حدد **GBP OPER**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-216">On the **Payment** FastTab, in the **Bank account** field, select **GBP OPER**.</span></span>

    ![صفحة تفاصيل المورد](./media/er-quick-start2-bank-account-reference.png)

9. <span data-ttu-id="d59a4-218">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-218">Select **Save**.</span></span>
10. <span data-ttu-id="d59a4-219">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d59a4-219">Close the page.</span></span>

### <a name="enter-a-vendor-payment"></a><a id="EnterVendorPayment"></a><span data-ttu-id="d59a4-220">إدخال مدفوعات المورد</span><span class="sxs-lookup"><span data-stu-id="d59a4-220">Enter a vendor payment</span></span>

<span data-ttu-id="d59a4-221">يجب إدخال مدفوعات مورد جديدة باستخدام [مقترح دفع](https://docs.microsoft.com/dynamics365/finance/accounts-payable/create-vendor-payments-payment-proposal).</span><span class="sxs-lookup"><span data-stu-id="d59a4-221">You must enter a new vendor payment by using a [payment proposal](https://docs.microsoft.com/dynamics365/finance/accounts-payable/create-vendor-payments-payment-proposal).</span></span>

1. <span data-ttu-id="d59a4-222">انتقل إلى **الحسابات الدائنة** \> **المدفوعات** \> **‏‫دفتر يومية المدفوعات للمورد‬**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-222">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="d59a4-223">في صفحة **دفتر يومية المدفوعات للمورد‬**، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-223">On the **Vendor payment journal** page, select **New**.</span></span>
3. <span data-ttu-id="d59a4-224">في حقل **الاسم**، حدد **VendPay**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-224">In the **Name** field, select **VendPay**.</span></span>
4. <span data-ttu-id="d59a4-225">حدد **البنود**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-225">Select **Lines**.</span></span>
5. <span data-ttu-id="d59a4-226">حدد **مقترح الدفع** \> **إنشاء مقترح الدفع**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-226">Select **Payment proposal** \> **Create payment proposal**.</span></span>
6. <span data-ttu-id="d59a4-227">في مربع الحوار **مقترح دفع المورد**، قم بتكوين الشروط لتصفية السجلات الخاصة بحساب المورد **GB_SI_000001** فقط، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-227">In the **Vendor payment proposal** dialog box, configure conditions to filter for records for the **GB_SI_000001** vendor account only, and then select **OK**.</span></span>
7. <span data-ttu-id="d59a4-228">حدد السطر الخاص بفاتورة **00000007_Inv**، ثم حدد **إنشاء دفع**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-228">Select the line for the **00000007_Inv** invoice, and then select **Create payment**.</span></span>

    ![مربع حوار مقترح دفع المورد](./media/er-quick-start2-payment-proposal.png)

8. <span data-ttu-id="d59a4-230">تحقق من أن الدفع الذي تم إدخاله قد تم تكوينه لاستخدام أسلوب الدفع **الإلكتروني**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-230">Verify that the payment that is entered is configured to use the **Electronic** method of payment.</span></span>

    ![صفحة مدفوعات المورد](./media/er-quick-start2-payment-line.png)

## <a name="process-a-vendor-payment-by-using-the-standard-er-format"></a><a id="ProcessVendorPayment1"></a><span data-ttu-id="d59a4-232">معالجة مدفوعات المورد باستخدام تنسيق ER القياسي</span><span class="sxs-lookup"><span data-stu-id="d59a4-232">Process a vendor payment by using the standard ER format</span></span>

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment1"></a><span data-ttu-id="d59a4-233">إعداد طريقة الدفع الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="d59a4-233">Set up the electronic payment method</span></span>

<span data-ttu-id="d59a4-234">يجب تكوين طريقة الدفع الإلكترونية لكي يمكن استخدام تكوين تنسيق ER المستورد.</span><span class="sxs-lookup"><span data-stu-id="d59a4-234">You must configure the electronic method of payment so that it uses the imported ER format configuration.</span></span>

1. <span data-ttu-id="d59a4-235">انتقل إلى **الحسابات الدائنة** \> **إعداد الدفع** \> **طرق الدفع**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-235">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="d59a4-236">في صفحة **طرق الدفع - الموردون**، حدد طريقة الدفع **الإلكترونية** في الجزء الأيمن.</span><span class="sxs-lookup"><span data-stu-id="d59a4-236">On the **Methods of payment - vendors** page, select the **Electronic** method of payment in the left pane.</span></span>
3. <span data-ttu-id="d59a4-237">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-237">Select **Edit**.</span></span>
4. <span data-ttu-id="d59a4-238">في علامة التبويب السريعة **تنسيقات الملف**، قم بتعيين خيار **تنسيق التصدير الإلكتروني العام‬** على **نعم**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-238">On the **File formats** FastTab, set the **General electronic Export format** option to **Yes**.</span></span>
5. <span data-ttu-id="d59a4-239">في حقل **تكوين تنسيق التصدير**، حدد تكوين التنسيق **BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-239">In the **Export format configuration** field, select the **BACS (UK)** format configuration.</span></span>

    ![طرق الدفع - صفحة الموردون](./media/er-quick-start2-method-of-payment1.png)

6. <span data-ttu-id="d59a4-241">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-241">Select **Save**.</span></span>

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment1"></a><span data-ttu-id="d59a4-242">معالجة مدفوعات مورد</span><span class="sxs-lookup"><span data-stu-id="d59a4-242">Process a vendor payment</span></span>

1. <span data-ttu-id="d59a4-243">انتقل إلى **الحسابات الدائنة** \> **المدفوعات** \> **‏‫دفتر يومية المدفوعات للمورد‬**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-243">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="d59a4-244">في صفحة **‏‫دفتر يومية المدفوعات للمورد‬** ، حدد دفتر يومية المدفوعات الذي قمت بإضافته مسبقا، ثم حدد **البنود**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-244">On the **Vendor payment journal** page, select the payment journal that you added earlier, and then select **Lines**.</span></span>
3. <span data-ttu-id="d59a4-245">في صفحة **مدفوعات المورد**، حدد **إنشاء مدفوعات**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-245">On the **Vendor payments** page, select **Generate payments**.</span></span>
4. <span data-ttu-id="d59a4-246">في مربع الحوار **إنشاء مدفوعات**، أدخل المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="d59a4-246">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="d59a4-247">في حقل **طريقة الدفع** حدد **إلكتروني**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-247">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="d59a4-248">في الحقل **حساب البنك** حدد **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-248">In the **Bank account** field, select **GBSI OPER**.</span></span>

5. <span data-ttu-id="d59a4-249">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-249">Select **OK**.</span></span>
6. <span data-ttu-id="d59a4-250">في مربع الحوار **معلمات التقرير الإلكتروني**، قم بتعيين خيار **طباعة تقرير التحكم** إلى **نعم**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-250">In the **Electronic report parameters** dialog box, set the **Print control report** option to **Yes**, and then select **OK**.</span></span>

    ![صفحة حوار معلمات التقرير الإلكتروني](./media/er-quick-start2-payment-dialog1.png)

    > [!NOTE]
    > <span data-ttu-id="d59a4-252">بالإضافة إلى ملف الدفع، يمكنك الآن إنشاء تقرير التحكم.</span><span class="sxs-lookup"><span data-stu-id="d59a4-252">In addition to the payment file, you can now generate the control report.</span></span>

7. <span data-ttu-id="d59a4-253">قم بتنزيل الملف المضغوط من نوع zip، ثم قم باستخراج الملفات التالية منه:</span><span class="sxs-lookup"><span data-stu-id="d59a4-253">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="d59a4-254">تقرير التحكم بتنسيق Excel</span><span class="sxs-lookup"><span data-stu-id="d59a4-254">The control report in Excel format</span></span>
    - <span data-ttu-id="d59a4-255">ملف الدفع بتنسيق TXT</span><span class="sxs-lookup"><span data-stu-id="d59a4-255">The payment file in TXT format</span></span>

        <span data-ttu-id="d59a4-256">لاحظ أنه وفقًا [لبنية](#PositionRoutingNumber) تنسيق ER الموفّر، يبدأ سطر الدفع في الملف الذي تم إنشاؤه برقم التوجيه الذي تم [تحديده](#DefineRoutingNumber) للحساب البنكي المكوّن.</span><span class="sxs-lookup"><span data-stu-id="d59a4-256">Notice that, in accordance with the [structure](#PositionRoutingNumber) of the provided ER format, the payment line in the generated file starts with the routing number that was [defined](#DefineRoutingNumber) for the configured bank account.</span></span>

        ![ملف الدفع بتنسيق TXT](./media/er-quick-start2-payment-file1.png)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a><span data-ttu-id="d59a4-258">تخصيص تنسيق ER القياسي</span><span class="sxs-lookup"><span data-stu-id="d59a4-258">Customize the standard ER format</span></span>

<span data-ttu-id="d59a4-259">بالنسبة للمثال الموضح في هذا القسم، فإنك ترغب في استخدام تكوينات ER التي يتم توفيرها بواسطة Microsoft لإنشاء ملفات دفع المورد بتنسيق BACS، ولكن يجب إضافة تخصيص لدعم متطلبات بنك معين.</span><span class="sxs-lookup"><span data-stu-id="d59a4-259">For the example that is shown in this section, you want to use the ER configurations that are provided by Microsoft to generate vendor payment files in BACS format, but you must add a customization to support the requirements of a specific bank.</span></span> <span data-ttu-id="d59a4-260">كما أنك تريد أن تكون قادرًا على ترقيه التنسيق المخصص عند توفر إصدارات جديدة من تكوينات ER.</span><span class="sxs-lookup"><span data-stu-id="d59a4-260">You also want to be able to upgrade your custom format when new versions of ER configurations become available.</span></span> <span data-ttu-id="d59a4-261">مع ذلك، تريد أن تكون قادرًا على إجراء الترقية بأقل تكلفة.</span><span class="sxs-lookup"><span data-stu-id="d59a4-261">However, you want to be able to do the upgrade at the lowest cost.</span></span>

<span data-ttu-id="d59a4-262">في هذه الحالة، بصفتك مندوب لـ Litware, Inc.، يجب إنشاء (اشتقاق) تكوين تنسيق ER جديد باستخدام التكوين **BACS (UK)** المقدم من Microsoft كأساس.</span><span class="sxs-lookup"><span data-stu-id="d59a4-262">In this case, as the representative of Litware, Inc., you must create (derive) a new ER format configuration by using the **BACS (UK)** Microsoft-provided configuration as a base.</span></span>

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a><span data-ttu-id="d59a4-263">إنشاء تنسيق مخصص</span><span class="sxs-lookup"><span data-stu-id="d59a4-263">Create a custom format</span></span>

1. <span data-ttu-id="d59a4-264">انتقل إلى **إدارة المؤسسة** \> **التقارير الإلكترونية** \> **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-264">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="d59a4-265">في صفحة **التكوينات**، في شجرة التكوينات في الجزء الأيسر، وسَّع **نموذج الدفع**، ثم حدد **BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-265">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK)**.</span></span> <span data-ttu-id="d59a4-266">سوف تستخدم Litware, Inc. الإصدار 1.1 من تكوين تنسيق ER هذا كأساس للإصدار المخصص.</span><span class="sxs-lookup"><span data-stu-id="d59a4-266">Litware, Inc. will use version 1.1 of this ER format configuration as the base for the custom version.</span></span>
3. <span data-ttu-id="d59a4-267">حدد **إنشاء تكوين** لفتح مربع الحوار المنسدل.</span><span class="sxs-lookup"><span data-stu-id="d59a4-267">Select **Create configuration** to open the drop-down dialog box.</span></span> <span data-ttu-id="d59a4-268">يمكنك استخدام مربع الحوار هذا لإنشاء تكوين جديد لتنسيق دفع مخصص.</span><span class="sxs-lookup"><span data-stu-id="d59a4-268">You can use this dialog box to create a new configuration for a custom payment format.</span></span>
4. <span data-ttu-id="d59a4-269">في مجموعة الحقول **الجديدة**، حدد خيار **مشتق من الاسم: BACS (UK), Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-269">In the **New** field group, select the **Derive from Name: BACS (UK), Microsoft** option.</span></span>
5. <span data-ttu-id="d59a4-270">في حقل **الاسم**، أدخل **‏‫BACS (UK مخصص)**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-270">In the **Name** field, enter **BACS (UK custom)**.</span></span>

    ![إنشاء مربع حوار القائمة المنسدلة للتكوين](./media/er-quick-start2-add-derived-format.png)

6. <span data-ttu-id="d59a4-272">حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-272">Select **Create configuration**.</span></span>

<span data-ttu-id="d59a4-273">يتم إنشاء الإصدار 1.1.1 من تكوين تنسيق ER **BACS (UK مخصص)**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-273">Version 1.1.1 of the **BACS (UK custom)** ER format configuration is created.</span></span> <span data-ttu-id="d59a4-274">هذا الإصدار [بالحالة](general-electronic-reporting.md#component-versioning) **مسودة** ويمكن تحريره.</span><span class="sxs-lookup"><span data-stu-id="d59a4-274">This version has a [status](general-electronic-reporting.md#component-versioning) of **Draft** and can be edited.</span></span> <span data-ttu-id="d59a4-275">يطابق المحتوي الحالي لتنسيق ER الخاص بك محتوي التنسيق الذي توفره Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d59a4-275">The current content of your custom ER format matches the content of the format that is provided by Microsoft.</span></span>

![صفحة التكوينات](./media/er-quick-start2-derived-format-configuration1.png)

### <a name="edit-a-custom-format"></a><a id="ConfigureDerivedFormat"></a><span data-ttu-id="d59a4-277">تحرير تنسيق مخصص</span><span class="sxs-lookup"><span data-stu-id="d59a4-277">Edit a custom format</span></span>

<span data-ttu-id="d59a4-278">يجب تكوين التنسيق المخصص الخاص بك بحيث يفي بالمتطلبات الخاصة بالبنك.</span><span class="sxs-lookup"><span data-stu-id="d59a4-278">You must configure your custom format so that it meets bank-specific requirements.</span></span> <span data-ttu-id="d59a4-279">على سبيل المثال، قد يتطلب أحد البنك أن تتضمن ملفات الدفع التي يتم إنشاؤها كود جمعية الاتصالات المالية بين البنوك العالمية (سويفت) للبنك الذي تم تعيينه لدور الوكيل في دفع المورد الذي تمت معالجته.</span><span class="sxs-lookup"><span data-stu-id="d59a4-279">For example, a bank might require that payment files that are generated include the Society for Worldwide Interbank Financial Telecommunication (SWIFT) code of a bank that is assigned the agent role in the processed vendor payment.</span></span> <span data-ttu-id="d59a4-280">أكواد سويفت هي أكواد بنكية دولية تحدد البنوك الخاصة بالعالم.</span><span class="sxs-lookup"><span data-stu-id="d59a4-280">SWIFT codes are international bank codes that identify specific banks worldwide.</span></span> <span data-ttu-id="d59a4-281">وتعرف أيضا بأكواد معرفات البنك (BIC).</span><span class="sxs-lookup"><span data-stu-id="d59a4-281">They are also known as Bank Identifier Codes (BICs).</span></span> <span data-ttu-id="d59a4-282">يجب أن يكون طول كود سويفت 11 حرفًا، ويجب إدخاله في بداية كل سطر دفع في أي ملف دفع تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="d59a4-282">The SWIFT code must be 11 characters long, and it must be entered at the beginning of every payment line in a generated payment file.</span></span>

1. <span data-ttu-id="d59a4-283">انتقل إلى **إدارة المؤسسة** \> **التقارير الإلكترونية** \> **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-283">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="d59a4-284">في صفحة **التكوينات**، في شجرة التكوينات في الجزء الأيسر، وسَّع **نموذج الدفع**، ثم حدد **BACS (UK مخصص)**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-284">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK custom)**.</span></span>
3. <span data-ttu-id="d59a4-285">على علامة التبويب السريعة **إصدارات**، حدد الإصدار **1.1.1** للتكوين المحدد.</span><span class="sxs-lookup"><span data-stu-id="d59a4-285">On the **Versions** FastTab, select version **1.1.1** of the selected configuration.</span></span>
4. <span data-ttu-id="d59a4-286">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-286">Select **Designer**.</span></span>
5. <span data-ttu-id="d59a4-287">في صفحة **مصمم التنسيق**، حدد **إظهار التفاصيل** لعرض مزيد من المعلومات حول عناصر التنسيق.</span><span class="sxs-lookup"><span data-stu-id="d59a4-287">On the **Format designer** page, select **Show details** to view more information about the format elements.</span></span>
6. <span data-ttu-id="d59a4-288">قم بتوسيع ومراجعة العناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="d59a4-288">Expand and review the following elements:</span></span>

    - <span data-ttu-id="d59a4-289">عنصر **BACSReportsFolder** لنوع **المجلد**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-289">The **BACSReportsFolder** element of the **Folder** type.</span></span> <span data-ttu-id="d59a4-290">يتم استخدام هذا العنصر لإنشاء إخراج بتنسيق ZIP.</span><span class="sxs-lookup"><span data-stu-id="d59a4-290">This element is used to generate output in ZIP format.</span></span>
    - <span data-ttu-id="d59a4-291">عنصر **الملف** لنوع **الملف**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-291">The **file** element of the **File** type.</span></span> <span data-ttu-id="d59a4-292">يتم استخدام هذا العنصر لإنشاء ملف دفع بتنسيق TXT.</span><span class="sxs-lookup"><span data-stu-id="d59a4-292">This element is used to generate a payment file in TXT format.</span></span>
    - <span data-ttu-id="d59a4-293">عنصر **الحركات** لنوع **التسلسل**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-293">The **transactions** element of the **Sequence** type.</span></span> <span data-ttu-id="d59a4-294">يتم استخدام هذا العنصر لإنشاء سطر دفع فردي في ملف الدفع.</span><span class="sxs-lookup"><span data-stu-id="d59a4-294">This element is used to generate a single payment line in a payment file.</span></span>
    - <span data-ttu-id="d59a4-295">عنصر **الحركة** لنوع **التسلسل**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-295">The **transaction** element of the **Sequence** type.</span></span> <span data-ttu-id="d59a4-296">يتم استخدام هذا العنصر لإنشاء حقول فردية في ملف دفع فردي.</span><span class="sxs-lookup"><span data-stu-id="d59a4-296">This element is used to generate individual fields of a single payment line.</span></span>

7. <span data-ttu-id="d59a4-297">حدد عنصر **الحركة**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-297">Select the **transaction** element.</span></span>

    ![عنصر الحركة في مصمم عمليات ER](./media/er-quick-start2-derived-format0.png)

    > [!NOTE]
    > <span data-ttu-id="d59a4-299">يتم تكوين التقرير المقدم بحيث <a id="PositionRoutingNumber"></a>يبدأ كل سطر من سطور الدفع برقم التوجيه البنكي.</span><span class="sxs-lookup"><span data-stu-id="d59a4-299">The provided report is configured so that <a id="PositionRoutingNumber"></a>every payment line starts with the bank routing number.</span></span> <span data-ttu-id="d59a4-300">يتم استخدام عنصر التنسيق **vendBankRouteNum** لهذا الغرض.</span><span class="sxs-lookup"><span data-stu-id="d59a4-300">The **vendBankRouteNum** format element is used for this purpose.</span></span> 

8. <span data-ttu-id="d59a4-301">حدد **إضافة**، ثم حدد نوع **سلسلة\\نصية** لعنصر التنسيق الذي تقوم بإضافته:</span><span class="sxs-lookup"><span data-stu-id="d59a4-301">Select **Add**, and then select the **Text\\String** type of the format element that you're adding:</span></span>

    1. <span data-ttu-id="d59a4-302">في حقل **الاسم**، أدخل **vendBankSWIFT**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-302">In the **Name** field, enter **vendBankSWIFT**.</span></span>
    2. <span data-ttu-id="d59a4-303">في حقل **الحد الأقصى للطول**، أدخل **11**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-303">In the **Minimum length** field, enter **11**.</span></span>
    3. <span data-ttu-id="d59a4-304">في حقل **الحد الأقصى للطول**، أدخل **11**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-304">In the **Maximum length** field, enter **11**.</span></span>
    4. <span data-ttu-id="d59a4-305">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-305">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d59a4-306">سيتم استخدام عنصر **vendBankSWIFT** لإدخال كود سويفت لبنك المورد في الملف الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="d59a4-306">The **vendBankSWIFT** element will be used to enter the SWIFT code of a vendor bank in generated files.</span></span>

9. <span data-ttu-id="d59a4-307">في شجرة بنية التنسيق، حدد **vendBankSWIFT**</span><span class="sxs-lookup"><span data-stu-id="d59a4-307">In the format structure tree, select **vendBankSWIFT**.</span></span>
10. <span data-ttu-id="d59a4-308">حدد **تحريك لأعلى** لتحريك عنصر التنسيق المحدد بمقدار مستوى واحد لأعلى.</span><span class="sxs-lookup"><span data-stu-id="d59a4-308">Select **Move up** to move the selected format element up one level.</span></span> <span data-ttu-id="d59a4-309">كرر هذه الخطوة حتى يصبح عنصر **vendBankSWIFT** هو <a id="PositionSWIFTCode"></a>العنصر الأول ضمن عنصر **الحركة الأصلية**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-309">Repeat this step until the **vendBankSWIFT** element is the <a id="PositionSWIFTCode"></a>first element under the parent **transaction** element.</span></span>

    ![vendBankSWIFT كعنصر أول ضمن الحركة في مصمم عمليات ER](./media/er-quick-start2-derived-format1.png)

11. <span data-ttu-id="d59a4-311">بينما ما يزال **vendBankSWIFT** محددًا في شجرة بنية التنسيق، حدد علامة التبويب **تعيين**، ثم قم بتوسيع مصدر بيانات **النموذج**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-311">While the **vendBankSWIFT** is still selected in the format structure tree, select the **Mapping** tab, and then expand the **model** data source.</span></span>
12. <span data-ttu-id="d59a4-312">قم بتوسيع **model.Payment** \> **model.Payment.CreditorAgent**، وحدد حقل مصدر البيانات **model.Payment.CreditorAgent.BICFI**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-312">Expand **model.Payment** \> **model.Payment.CreditorAgent**, and select the **model.Payment.CreditorAgent.BICFI** data source field.</span></span> <span data-ttu-id="d59a4-313">ويعرض حقل مصدر البيانات هذا كود سويفت للبنك الخاص بالمورد والذي تم تعيينه لدور الوكيل في مدفوعات المورد التي تمت معالجتها.</span><span class="sxs-lookup"><span data-stu-id="d59a4-313">This data source field exposes the SWIFT code of a vendor bank that is assigned the agent role in the processed vendor payment.</span></span>
13. <span data-ttu-id="d59a4-314">حدد **ربط**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-314">Select **Bind**.</span></span> <span data-ttu-id="d59a4-315">عنصر التنسيق **vendBankSWIFT** مرتبط الآن بحقل مصدر البيانات **model.Payment.CreditorAgent.BICFI**، لكي يمكن إدخال أكواد سويفت في ملفات الدفع التي تم إنشاؤها</span><span class="sxs-lookup"><span data-stu-id="d59a4-315">The **vendBankSWIFT** format element is now bound with the **model.Payment.CreditorAgent.BICFI** data source field, so that SWIFT codes will be entered in generated payment files.</span></span>

    ![عنصر التنسيق vendBankSWIFT مرتبطة الآن بحقل مصدر البيانات model.Payment.CreditorAgent.BICFI في مصمم عمليات ER](./media/er-quick-start2-derived-format2.png)

14. <span data-ttu-id="d59a4-317">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-317">Select **Save**.</span></span>
15. <span data-ttu-id="d59a4-318">أغلق صفحة المصمم.</span><span class="sxs-lookup"><span data-stu-id="d59a4-318">Close the designer page.</span></span>

### <a name="mark-a-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a><span data-ttu-id="d59a4-319">تعليم تنسيق مخصص على أنه قابل للتشغيل</span><span class="sxs-lookup"><span data-stu-id="d59a4-319">Mark a custom format as runnable</span></span>

<span data-ttu-id="d59a4-320">والآن بعد أن تم إنشاء الإصدار الأول من التنسيق المخصص وأصبح بالحالة **مسودة**، يمكنك تشغيله لأغراض الاختبار.</span><span class="sxs-lookup"><span data-stu-id="d59a4-320">Now that the first version of your custom format has been created and has a status of **Draft**, you can run it for testing purposes.</span></span> <span data-ttu-id="d59a4-321">لتشغيل التقرير، يجب عليك معالجة دفع المورد باستخدام طريقة الدفع التي تشير إلى تنسيق ER المخصص.</span><span class="sxs-lookup"><span data-stu-id="d59a4-321">To run the report, you must process a vendor payment by using the payment method that refers to your custom ER format.</span></span> <span data-ttu-id="d59a4-322">افتراضيًا، عندما تستدعي أحد تنسيقات ER من التطبيق، يتم فقط استخدام الإصدارات التي بالحالة **مكتمل** أو **مشترك** والتي تتم [مراعاتها](general-electronic-reporting.md#component-versioning).</span><span class="sxs-lookup"><span data-stu-id="d59a4-322">By default, when you call an ER format from the application, only versions that have a status of **Completed** or **Shared** are [considered](general-electronic-reporting.md#component-versioning).</span></span> <span data-ttu-id="d59a4-323">يساعد هذا السلوك في منع استخدام تنسيقات ER التي لها تصميمات غير مكتملة.</span><span class="sxs-lookup"><span data-stu-id="d59a4-323">This behavior helps prevent ER formats that have unfinished designs from being used.</span></span> <span data-ttu-id="d59a4-324">مع ذلك، بالنسبة لتشغيل الاختبارات الخاصة بك، يمكنك إجبار التطبيق على استخدام إصدار تنسيق ER بالحالة **مسودة**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-324">However, for your test runs, you can force the application to use the version of your ER format that has a status of **Draft**.</span></span> <span data-ttu-id="d59a4-325">وبهذه الطريقة، يمكنك تعديل إصدار التنسيق الحالي إذا كانت هناك أية تعديلات مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="d59a4-325">In this way, you can adjust the current format version if any modifications are required.</span></span> <span data-ttu-id="d59a4-326">لمزيد من المعلومات، راجع [قابلية التطبيق‬](electronic-reporting-destinations.md#applicability).</span><span class="sxs-lookup"><span data-stu-id="d59a4-326">For more information, see [Applicability](electronic-reporting-destinations.md#applicability).</span></span>

<span data-ttu-id="d59a4-327">لاستخدام إصدار المسودة لتنسيق ER، يجب وضع علامة بوضوح على تنسيق ER.</span><span class="sxs-lookup"><span data-stu-id="d59a4-327">To use the draft version of an ER format, you must explicitly mark the ER format.</span></span>

1. <span data-ttu-id="d59a4-328">انتقل إلى **إدارة المؤسسة** \> **التقارير الإلكترونية** \> **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-328">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="d59a4-329">في صفحة **التكوينات**، في جزء الإجراءات، في علامة التبويب **التكوينات**، في مجموعة **الإعدادات المتقدمة**، حدد **معلمات المستخدمين**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-329">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="d59a4-330">في مربع الحوار **معلمات المستخدم**، قم بتعيين خيارات **إعدادات التشغيل** إلى **نعم**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-330">In the **User parameters** dialog box, set the **Run settings** option to **Yes**, and then select **OK**.</span></span>
4. <span data-ttu-id="d59a4-331">حدد **تحرير** لتجعل الصفحة الحالية قابلة للتحرير، حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="d59a4-331">Select **Edit** to make the current page editable, as required.</span></span>
5. <span data-ttu-id="d59a4-332">في شجره التكوين الموجودة في الجزء الأيمن، حدد **BACS (UK مخصص)**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-332">In the configuration tree in the left pane, select **BACS (UK custom)**.</span></span>
6. <span data-ttu-id="d59a4-333">عيّن الخيار **تشغيل المسودة** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-333">Set the **Run Draft** option to **Yes**.</span></span>

    ![خيار تشغيل المسودة في صفحة التكوينات](./media/er-quick-start2-derived-format-configuration2.png)

## <a name="process-a-vendor-payment-by-using-the-custom-er-format"></a><a id="ProcessVendorPayment2"></a><span data-ttu-id="d59a4-335">معالجة مدفوعات المورد باستخدام تنسيق ER مخصص</span><span class="sxs-lookup"><span data-stu-id="d59a4-335">Process a vendor payment by using the custom ER format</span></span>

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment2"></a><span data-ttu-id="d59a4-336">إعداد طريقة الدفع الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="d59a4-336">Set up the electronic payment method</span></span>

<span data-ttu-id="d59a4-337">يجب تكوين طريقة الدفع الإلكترونية حتى يتم استخدام تنسيق ER المخصص لمعالجة مدفوعات المورد.</span><span class="sxs-lookup"><span data-stu-id="d59a4-337">You must configure the electronic method of payment so that your custom ER format is used to process vendor payments.</span></span>

1. <span data-ttu-id="d59a4-338">انتقل إلى **الحسابات الدائنة** \> **إعداد الدفع** \> **طرق الدفع**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-338">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="d59a4-339">في صفحة **طرق الدفع - الموردون**، حدد طريقة الدفع **الإلكترونية** في الجزء الأيمن.</span><span class="sxs-lookup"><span data-stu-id="d59a4-339">On the **Methods of payment - vendors** page, select the **Electronic** method of payment in the left pane.</span></span>
3. <span data-ttu-id="d59a4-340">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-340">Select **Edit**.</span></span>
4. <span data-ttu-id="d59a4-341">في علامة التبويب السريعة **تنسيق الملف**، قم بتعيين خيار **تنسيق التصدير الإلكتروني العام‬** على **نعم**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-341">On the **File format** FastTab, set the **General electronic export format** option to **Yes**.</span></span>
5. <span data-ttu-id="d59a4-342">في حقل **تكوين تنسيق التصدير**، حدد تكوين التنسيق **BACS (UK مخصص)**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-342">In the **Export format configuration** field, select the **BACS (UK custom)** format configuration.</span></span>

    ![طرق الدفع - صفحة الموردون](./media/er-quick-start2-method-of-payment2.png)

6. <span data-ttu-id="d59a4-344">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-344">Select **Save**.</span></span>

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment2"></a><span data-ttu-id="d59a4-345">معالجة مدفوعات مورد</span><span class="sxs-lookup"><span data-stu-id="d59a4-345">Process a vendor payment</span></span>

1. <span data-ttu-id="d59a4-346">انتقل إلى **الحسابات الدائنة** \> **المدفوعات** \> **‏‫دفتر يومية المدفوعات للمورد‬**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-346">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="d59a4-347">في صفحة **‏‫دفتر يومية المدفوعات للمورد‬**، حدد دفتر يومية المدفوعات الذي قمت بإنشائه سابقًا.</span><span class="sxs-lookup"><span data-stu-id="d59a4-347">On the **Vendor payment journal** page, select the payment journal that you created earlier.</span></span>
3. <span data-ttu-id="d59a4-348">حدد **البنود**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-348">Select **Lines**.</span></span>
4. <span data-ttu-id="d59a4-349">في صفحة **مدفوعات المورد**، أعلى الشبكة، حدد **حالة الدفع** \> **بلا**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-349">On the **Vendor payments** page, above the grid, select **Payment status** \> **None**.</span></span>
5. <span data-ttu-id="d59a4-350">حدد **إنشاء الدفع**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-350">Select **Generate payment**.</span></span>
6. <span data-ttu-id="d59a4-351">في مربع الحوار **إنشاء مدفوعات**، أدخل المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="d59a4-351">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="d59a4-352">في حقل **طريقة الدفع** حدد **إلكتروني**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-352">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="d59a4-353">في الحقل **حساب البنك** حدد **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-353">In the **Bank account** field, select **GBSI OPER**.</span></span>

7. <span data-ttu-id="d59a4-354">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-354">Select **OK**.</span></span>
8. <span data-ttu-id="d59a4-355">في مربع الحوار **معلمات التقرير الإلكتروني**، قم بتعيين خيار **طباعة تقرير التحكم** إلى **نعم**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-355">In the **Electronic report parameters** dialog box, set the **Print control report** option to **Yes**, and then select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d59a4-356">بالإضافة إلى ملف الدفع، يمكنك إنشاء تقرير التحكم فقط.</span><span class="sxs-lookup"><span data-stu-id="d59a4-356">In addition to the payment file, you can generate only the control report.</span></span>

9. <span data-ttu-id="d59a4-357">قم بتنزيل الملف المضغوط من نوع zip، ثم قم باستخراج الملفات التالية منه:</span><span class="sxs-lookup"><span data-stu-id="d59a4-357">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="d59a4-358">تقرير التحكم بتنسيق Excel</span><span class="sxs-lookup"><span data-stu-id="d59a4-358">The control report in Excel format</span></span>
    - <span data-ttu-id="d59a4-359">ملف الدفع بتنسيق TXT</span><span class="sxs-lookup"><span data-stu-id="d59a4-359">The payment file in TXT format</span></span>

        <span data-ttu-id="d59a4-360">لاحظ أنه وفقا للبنية الخاصة بتنسيق ER المخصص، [يبدأ](#PositionSWIFTCode) سطر الدفع في الملف الذي تم إنشاؤه الآن بكود سويفت الذي تم [إدخاله](#DefineSWIFTCode) للحساب البنكي للمورد الذي تمت معالجة الدفع الخاص به.</span><span class="sxs-lookup"><span data-stu-id="d59a4-360">Notice that, in accordance with the structure of your custom ER format, the payment line in the generated file now [starts](#PositionSWIFTCode) with the SWIFT code that was [entered](#DefineSWIFTCode) for the bank account of the vendor whose payment has been processed.</span></span>

        ![ملف الدفع بتنسيق TXT](./media/er-quick-start2-payment-file2.png)

## <a name="import-new-versions-of-the-standard-er-format-configurations"></a><a id="ImportERSolution2"></a><span data-ttu-id="d59a4-362">استيراد إصدارات جديدة من تكوينات تنسيق ER القياسية</span><span class="sxs-lookup"><span data-stu-id="d59a4-362">Import new versions of the standard ER format configurations</span></span>

<span data-ttu-id="d59a4-363">بالنسبة للمثال الموضح في هذا القسم، سوف تتلقى إخطارًا حول مقالة قاعدة المعارف [KB 3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046).</span><span class="sxs-lookup"><span data-stu-id="d59a4-363">For the example that is shown in this section, you receive a notification about Knowledge Base article [KB3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046).</span></span> <span data-ttu-id="d59a4-364">يعلمك هذا الإخطار بالإصدار الجديد من تنسيق ER **BACS (UK مخصص)** الذي تم نشره بواسطة Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d59a4-364">This notification informs you about the new version of the **BACS (UK)** ER format that has been published by Microsoft.</span></span> <span data-ttu-id="d59a4-365">بالإضافة إلى تقرير التحكم، يتيح هذا الإصدار الجديد للمستخدمين إنشاء تقرير إخطار الدفع وتقرير إشعار الحضور بينما تجري معالجة دفع المورد.</span><span class="sxs-lookup"><span data-stu-id="d59a4-365">In addition to the control report, this new version lets users generate the payment advice report and the attending note report while a vendor payment is being processed.</span></span> <span data-ttu-id="d59a4-366">تريد الآن بدء استخدام هذه الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="d59a4-366">You want to start to use that functionality.</span></span>

### <a name="import-new-versions-of-the-standard-er-configurations"></a><a id="ImportERFormat2"></a><span data-ttu-id="d59a4-367">استيراد إصدارات جديدة من تكوينات ER القياسية</span><span class="sxs-lookup"><span data-stu-id="d59a4-367">Import new versions of the standard ER configurations</span></span>

<span data-ttu-id="d59a4-368">لإضافة إصدارات جديدة لتكوينات ER إلى مثيل Finance الحالي، يجب استيرادها من [مستودع](general-electronic-reporting.md#Repository) ERالذي قمت بتكوينه.</span><span class="sxs-lookup"><span data-stu-id="d59a4-368">To add new versions of the ER configurations to the current Finance instance, you must import them from the ER [repository](general-electronic-reporting.md#Repository) that you've configured.</span></span>

1. <span data-ttu-id="d59a4-369">انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-369">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="d59a4-370">في صفحة **تكوينات التعريب**، في قسم **موفري التكوين**، حدد تجانب **Microsoft**، ثم حدد **المستودعات** لعرض قائمة المستودعات الخاصة بموفر Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d59a4-370">On the **Localization configurations** page, in the **Configuration providers** section, select the **Microsoft** tile, and then select **Repositories** to view the list of repositories for the Microsoft provider.</span></span>
3. <span data-ttu-id="d59a4-371">في صفحة **مستودعات التكوين**، حدد المستودع من نوع **عام**، ثم حدد **فتح**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-371">On the **Configuration repositories** page, select the repository of the **Global** type, and then select **Open**.</span></span> <span data-ttu-id="d59a4-372">في حالة مطالبتك بالتخويل للاتصال بخدمة Regulatory Configuration Service، اتبع إرشادات التخويل.</span><span class="sxs-lookup"><span data-stu-id="d59a4-372">If you're prompted for authorization to connect to Regulatory Configuration Service, follow the authorization instructions.</span></span>
4. <span data-ttu-id="d59a4-373">في صفحة **مستودع التكوين**، في شجرة التكوينات في الجزء الأيسر، حدد تكوين تنسيق **BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-373">On the **Configuration repository** page, in the configuration tree in the left pane, select the **BACS (UK)** format configuration.</span></span>
5. <span data-ttu-id="d59a4-374">على علامة التبويب السريعة **إصدارات**، حدد الإصدار **3.3** لتكوين تنسيق ER المحدد.</span><span class="sxs-lookup"><span data-stu-id="d59a4-374">On the **Versions** FastTab, select version **3.3** of the selected ER format configuration.</span></span>
6. <span data-ttu-id="d59a4-375">حدد **استيراد** لتنزيل الإصدار المحدد من المستودع العمومي إلى مثيل Finance الحالي.</span><span class="sxs-lookup"><span data-stu-id="d59a4-375">Select **Import** to download the selected version from the Global repository to the current Finance instance.</span></span>

![صفحة مستودع التكوين](./media/er-quick-start2-import-solution2.png)

> [!TIP]
> <span data-ttu-id="d59a4-377">إذا كانت لديك مشكلة في الوصول إلى [المستودع العمومي](er-download-configurations-global-repo.md)، فيمكنك [تنزيل التكوينات](download-electronic-reporting-configuration-lcs.md) من LCS بدلا من ذلك.</span><span class="sxs-lookup"><span data-stu-id="d59a4-377">If you have trouble accessing the [Global repository](er-download-configurations-global-repo.md), you can [download configurations](download-electronic-reporting-configuration-lcs.md) from LCS instead.</span></span>

### <a name="review-the-imported-er-format-configurations"></a><a id="ReviewImportedERFormat"></a><span data-ttu-id="d59a4-378">مراجعة تكوينات تنسيق ER المستوردة</span><span class="sxs-lookup"><span data-stu-id="d59a4-378">Review the imported ER format configurations</span></span>

1. <span data-ttu-id="d59a4-379">انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-379">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="d59a4-380">في الصفحة **تكوينات الترجمة**، في قسم **التكوينات**، حدد تجانب **تكوينات إعداد التقارير** .</span><span class="sxs-lookup"><span data-stu-id="d59a4-380">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="d59a4-381">في صفحة **التكوينات**، في شجرة التكوينات في الجزء الأيسر، وسَّع **نموذج الدفع**، ثم حدد **BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-381">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK)**.</span></span>
4. <span data-ttu-id="d59a4-382">في علامة التبويب السريعة **الإصدارات**، حدد الإصدار **3.3**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-382">On the **Versions** FastTab, select version **3.3**.</span></span>
5. <span data-ttu-id="d59a4-383">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-383">Select **Designer**.</span></span>
6. <span data-ttu-id="d59a4-384">في صفحة **مصمم التنسيق**، قم بتوسيع عنصر التنسيق **BACSReportsFolder**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-384">On the **Format designer** page, expand the **BACSReportsFolder** format element.</span></span>
7.  <span data-ttu-id="d59a4-385">لاحظ أن الإصدار 3.3 يحتوي على عنصر التنسيق **PaymentAdviceReport** الذي يُستخدم في إنشاء تقرير إخطار الدفع عند معالجة مدفوعات المورد.</span><span class="sxs-lookup"><span data-stu-id="d59a4-385">Notice that version 3.3 contains the **PaymentAdviceReport** format element that is used to generate a payment advice report when a vendor payment is processed.</span></span>

    ![عنصر التنسيق PaymentAdviceReport في مصمم عمليات ER](./media/er-quick-start2-imported-solution2.png)

8. <span data-ttu-id="d59a4-387">أغلق صفحة المصمم.</span><span class="sxs-lookup"><span data-stu-id="d59a4-387">Close the designer page.</span></span>

## <a name="adopt-the-changes-in-the-new-version-of-an-imported-format-in-a-custom-format"></a><a id="AdoptNewBaseVersion"></a><span data-ttu-id="d59a4-388">تبني التغييرات في الإصدار الجديد من تنسيق مستورد في تنسيق مخصص</span><span class="sxs-lookup"><span data-stu-id="d59a4-388">Adopt the changes in the new version of an imported format in a custom format</span></span>

### <a name="complete-the-current-draft-version-of-a-custom-format"></a><a id="CompleteDerivedFormat"></a><span data-ttu-id="d59a4-389">إكمال إصدار المسودة الحالي لتنسيق مخصص</span><span class="sxs-lookup"><span data-stu-id="d59a4-389">Complete the current draft version of a custom format</span></span>

<span data-ttu-id="d59a4-390">إذا كنت تريد الاحتفاظ بالحالة الحالية لتنسيقك المخصص، فقم بإكمال إصدار المسودة 1.1.1 بتغيير حالته من **مسودة** إلى **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-390">If you want to keep the current state of your custom format, complete the draft version 1.1.1 by changing its status from **Draft** to **Completed**.</span></span>

1. <span data-ttu-id="d59a4-391">انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-391">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="d59a4-392">في الصفحة **تكوينات الترجمة**، في قسم **التكوينات**، حدد تجانب **تكوينات إعداد التقارير** .</span><span class="sxs-lookup"><span data-stu-id="d59a4-392">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="d59a4-393">في صفحة **التكوينات**، في شجرة التكوينات في الجزء الأيسر، وسَّع **نموذج الدفع**، ووسِّع **BACS (UK)**، ثم حدد **BACS (UK مخصص)**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-393">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, expand **BACS (UK)**, and then select **BACS (UK custom)**.</span></span>
4. <span data-ttu-id="d59a4-394">في علامة التبويب السريعة **الإصدارات**، حدد **تغيير الحالة** \> **مكتمل**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-394">On the **Versions** FastTab, select **Change status** \> **Complete**, and then select **OK**.</span></span>

<span data-ttu-id="d59a4-395">يتم تغيير حالة الإصدار 1.1.1 من **مسودة** إلى **مكتمل**، ويصبح الإصدار للقراءة فقط.</span><span class="sxs-lookup"><span data-stu-id="d59a4-395">The status of version 1.1.1 is changed from **Draft** to **Completed**, and the version becomes read-only.</span></span> <span data-ttu-id="d59a4-396">تمت إضافة إصدار جديد قابل للتحرير، 1.1.2، بالحالة **مسودة**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-396">A new editable version, 1.1.2, has been added and has a status of **Draft**.</span></span> <span data-ttu-id="d59a4-397">يمكنك استخدام هذا الإصدار لإجراء مزيد من التغييرات في تنسيق ER المخصص.</span><span class="sxs-lookup"><span data-stu-id="d59a4-397">You can use this version to make further changes in your custom ER format.</span></span>

### <a name="rebase-a-custom-format-to-a-new-base-version"></a><a id="RebaseDerivedFormat"></a><span data-ttu-id="d59a4-398">إعادة تعريف تنسيق مخصص إلى إصدار أساسي جديد</span><span class="sxs-lookup"><span data-stu-id="d59a4-398">Rebase a custom format to a new base version</span></span>

<span data-ttu-id="d59a4-399">لبدء استخدام الوظيفة الجديدة الخاصة بالإصدار 3.3 من تنسيق **BACS (UK)** في التخصيص الخاص بك، يجب تغيير إصدار التكوين الأساسي للتكوين المخصص، **BACS (UK مخصص)**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-399">To start to use the new functionality of version 3.3 of the **BACS (UK)** format in your customization, you must change the base configuration version for the custom configuration, **BACS (UK custom)**.</span></span> <span data-ttu-id="d59a4-400">تُعرف هذه العملية باسم [إعادة تعيين الأساس](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase).</span><span class="sxs-lookup"><span data-stu-id="d59a4-400">This process is known as [rebasing](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase).</span></span> <span data-ttu-id="d59a4-401">بدلاً من الإصدار 1.1 من **BACS (UK)**، استخدم الإصدار 3.3.</span><span class="sxs-lookup"><span data-stu-id="d59a4-401">Instead of version 1.1 of **BACS (UK)**, use version 3.3.</span></span>

1. <span data-ttu-id="d59a4-402">انتقل إلى **إدارة المؤسسة** \> **التقارير الإلكترونية** \> **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-402">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="d59a4-403">في صفحة **التكوينات**، في شجرة التكوينات في الجزء الأيسر، وسَّع **نموذج الدفع**، ثم حدد **BACS (UK مخصص)**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-403">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK custom)**.</span></span>
3. <span data-ttu-id="d59a4-404">في علامة التبويب السريعة **الإصدارات**، حدد الإصدار **1.1.2**، ثم حدد **إعادة تعريف**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-404">On the **Versions** FastTab, select version **1.1.2**, and then select **Rebase**.</span></span>
4. <span data-ttu-id="d59a4-405">في مربع الحوار **إعادة تعريف**، في حقل **الإصدار الهدف**، حدد الإصدار **3.3** من التكوين الأساسي لتطبيقه على أنه الأساس الجديد واستخدمه لتحديث التكوين.</span><span class="sxs-lookup"><span data-stu-id="d59a4-405">In the **Rebase** dialog box, in the **Target version** field, select version **3.3** of the base configuration to apply it as the new base and use it to update the configuration.</span></span>

    ![مربع الحوار "إعادة تعريف"](./media/er-quick-start2-rebase1.png)

5. <span data-ttu-id="d59a4-407">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-407">Select **OK**.</span></span>
6. <span data-ttu-id="d59a4-408">لاحظ أنه تم تغيير رقم مسودة الإصدار من **1.1.2** إلى **3.3.2** لعكس التغيير في الإصدار الأساسي.</span><span class="sxs-lookup"><span data-stu-id="d59a4-408">Notice that the number of the draft version has been changed from **1.1.2** to **3.3.2** to reflect the change in the base version.</span></span>

    <span data-ttu-id="d59a4-409">عند دمج الإصدار المخصص والإصدار الأساسي الجديد، قد يتم اكتشاف بعض التعارضات بسبب تغييرات التنسيق التي لا يمكن دمجها تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="d59a4-409">When the custom version and a new base version are merged, some conflicts might be discovered because of format changes that can't be merged automatically.</span></span>

    ![تكوين معاد تعريفه مع وجود تعارضات في صفحة التكوينات](./media/er-quick-start2-rebase2.png)

    <span data-ttu-id="d59a4-411">في حالة اكتشاف تعارضات، يجب حلها يدويًا في مصمم التنسيق.</span><span class="sxs-lookup"><span data-stu-id="d59a4-411">If conflicts are discovered, they must be manually resolved in the format designer.</span></span>

7. <span data-ttu-id="d59a4-412">في علامة التبويب السريعة **الإصدارات**، حدد الإصدار **3.3.2**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-412">On the **Versions** FastTab, select version **3.3.2**.</span></span>
8. <span data-ttu-id="d59a4-413">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-413">Select **Designer**.</span></span>
9. <span data-ttu-id="d59a4-414">في صفحة **مصمم التنسيق**، في علامة التبويب السريعة **التفاصيل**، حدد سجل تعارضات إعادة التعريف، ثم حدد **تطبيق القيمة الأساسية**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-414">On the **Format designer** page, on the **Details** FastTab, select a rebase conflict record, and then select **Apply base value**.</span></span>

    ![سجل تعارضات إعادة التعريف في مصمم عمليات ER](./media/er-quick-start2-rebase3.png)

10. <span data-ttu-id="d59a4-416">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-416">Select **Save**.</span></span>

    <span data-ttu-id="d59a4-417">يجب ألا يظهر سجل تعارضات إعادة التعريف في علامة التبويب السريعة **التفاصيل**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-417">The rebase conflict record should no longer appear on the **Details** FastTab.</span></span>

    ![حل التعارضات في مصمم عمليات ER](./media/er-quick-start2-rebase4.png)

    > [!NOTE]
    > <span data-ttu-id="d59a4-419">لقد قمت بحل التعارض عن طريق التأكيد على أنه يجب استخدام الإصدار 3 من النموذج الأساسي في تنسيق ER هذا.</span><span class="sxs-lookup"><span data-stu-id="d59a4-419">You resolved the conflict by confirming that version 3 of the base model must be used in this ER format.</span></span>

11. <span data-ttu-id="d59a4-420">قم بتوسيع **BACSReportsFolder** \> **الملف** \> **الحركات** \> **الحركة**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-420">Expand **BACSReportsFolder** \> **file** \> **transactions** \> **transaction**.</span></span>
12. <span data-ttu-id="d59a4-421">في علامة التبويب **تعيين**، لاحظ أن الإصدار 3.3.2 لتنسيق ER المخصص يحتوي على كل من التخصيص الخاص بك (عنصر تنسيق **vendBankSWIFT** وارتباطاته) والوظيفة الجديدة للإصدار 3.3 من التنسيق ER الأساسي الذي تم توفيره بواسطة Microsoft (عنصر التنسيق **PaymentAdviceReport** مع العناصر المتداخلة والارتباطات المكونة له).</span><span class="sxs-lookup"><span data-stu-id="d59a4-421">On the **Mapping** tab, notice that version 3.3.2 of your custom ER format contains both your customization (the **vendBankSWIFT** format element and its binding) and the new functionality of version 3.3 of the base ER format that was provided by Microsoft (the **PaymentAdviceReport** format element together with its nested elements and configured bindings).</span></span> <span data-ttu-id="d59a4-422">بعدد قليل من نقرات الماوس، فإنك بذلك تستخدم التعديلات الخاصة بالإصدار الأساسي الجديد عن طريق دمجه مع التخصيص الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="d59a4-422">In just a few mouse clicks, you adopted the modifications of a new base version by merging them with your customization.</span></span>

    ![التنسيق المدمج في مصمم عمليات ER](./media/er-quick-start2-rebase5.png)

13. <span data-ttu-id="d59a4-424">أغلق صفحة المصمم.</span><span class="sxs-lookup"><span data-stu-id="d59a4-424">Close the designer page.</span></span>

> [!NOTE]
> <span data-ttu-id="d59a4-425">يمكن التراجع عن إجراء إعادة التعريف.</span><span class="sxs-lookup"><span data-stu-id="d59a4-425">The rebase action is reversible.</span></span> <span data-ttu-id="d59a4-426">لإلغاء عملية إعادة التعريف هذه، حدد **1.1.1** لتنسيق **BACS (UK مخصص)** في علامة التبويب السريعة **الإصدارات**، ثم حدد **الحصول على هذا الإصدار**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-426">To cancel this rebase, select version **1.1.1** of the **BACS (UK custom)** format on the **Versions** FastTab, and then select **Get this version**.</span></span> <span data-ttu-id="d59a4-427">سيتم بعد ذلك إعادة ترقيم الإصدار 3.3.2 إلى 1.1.2، وستتم مطابقة محتوى إصدار المسودة 1.1.2 مع محتوى الإصدار 1.1.1.</span><span class="sxs-lookup"><span data-stu-id="d59a4-427">Version 3.3.2 will then be renumbered 1.1.2, and the content of draft version 1.1.2 will match the content of version 1.1.1.</span></span>

### <a name="process-a-vendor-payment-by-using-a-rebased-er-format"></a><a id="ProcessPayment3"></a><span data-ttu-id="d59a4-428">معالجة مدفوعات المورد باستخدام تنسيق ER معاد تعريفه</span><span class="sxs-lookup"><span data-stu-id="d59a4-428">Process a vendor payment by using a rebased ER format</span></span>

1. <span data-ttu-id="d59a4-429">انتقل إلى **الحسابات الدائنة** \> **المدفوعات** \> **‏‫دفتر يومية المدفوعات للمورد‬**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-429">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="d59a4-430">في صفحة **‏‫دفتر يومية المدفوعات للمورد‬**، حدد دفتر يومية المدفوعات الذي قمت بإنشائه سابقًا.</span><span class="sxs-lookup"><span data-stu-id="d59a4-430">On the **Vendor payment journal** page, select the payment journal that you created earlier.</span></span>
3. <span data-ttu-id="d59a4-431">حدد **البنود**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-431">Select **Lines**.</span></span>
4. <span data-ttu-id="d59a4-432">في صفحة **مدفوعات المورد**، أعلى الشبكة، حدد **حالة الدفع** \> **بلا**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-432">On the **Vendor payments** page, above the grid, select **Payment status** \> **None**.</span></span>
5. <span data-ttu-id="d59a4-433">حدد **إنشاء الدفع**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-433">Select **Generate payment**.</span></span>
6. <span data-ttu-id="d59a4-434">في مربع الحوار **إنشاء مدفوعات**، أدخل المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="d59a4-434">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="d59a4-435">في حقل **طريقة الدفع** حدد **إلكتروني**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-435">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="d59a4-436">في الحقل **حساب البنك** حدد **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-436">In the **Bank account** field, select **GBSI OPER**.</span></span>

7. <span data-ttu-id="d59a4-437">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-437">Select **OK**.</span></span>
8. <span data-ttu-id="d59a4-438">في مربع الحوار **معلمات التقارير الإلكترونية**، أدخل المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="d59a4-438">In the **Electronic report parameters** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="d59a4-439">قم بتعيين خيار **طباعة تقرير التحكم** على **نعم**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-439">Set the **Print control report** option to **Yes**.</span></span>
    - <span data-ttu-id="d59a4-440">قم بتعيين خيار **طباعة إخطار الدفع** على **نعم**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-440">Set the **Print payment advice** option to **Yes**.</span></span>

    ![مربع حوار معلمات التقرير الإلكتروني](./media/er-quick-start2-payment-dialog2.png)

    > [!NOTE]
    > <span data-ttu-id="d59a4-442">بالإضافة إلى ملف الدفع، يمكنك الآن إنشاء تقرير التحكم وتقرير إخطار الدفع.</span><span class="sxs-lookup"><span data-stu-id="d59a4-442">In addition to the payment file, you can now generate both the control report and the payment advice report.</span></span>

9. <span data-ttu-id="d59a4-443">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d59a4-443">Select **OK**.</span></span>
10. <span data-ttu-id="d59a4-444">قم بتنزيل الملف المضغوط من نوع zip، ثم قم باستخراج الملفات التالية منه:</span><span class="sxs-lookup"><span data-stu-id="d59a4-444">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="d59a4-445">تقرير التحكم بتنسيق Excel</span><span class="sxs-lookup"><span data-stu-id="d59a4-445">The control report in Excel format</span></span>
    - <span data-ttu-id="d59a4-446">تقرير إخطار الدفع بتنسيق Excel</span><span class="sxs-lookup"><span data-stu-id="d59a4-446">The payment advice report in Excel format</span></span>

        ![تقرير إخطار الدفع بتنسيق Excel](./media/er-quick-start2-payment-advice-report.png)

    - <span data-ttu-id="d59a4-448">ملف الدفع بتنسيق TXT</span><span class="sxs-lookup"><span data-stu-id="d59a4-448">The payment file in TXT format</span></span>

        <span data-ttu-id="d59a4-449">لاحظ أن سطر الدفع في الملف الذي تم إنشاؤه يبدأ بكود سويفت الذي تم إدخاله للحساب البنكي للمورد الذي تمت معالجة الدفع الخاص به.</span><span class="sxs-lookup"><span data-stu-id="d59a4-449">Notice that the payment line in the generated file starts  with the SWIFT code that was entered for the bank account of a vendor whose payment has been processed.</span></span>

        ![ملف الدفع بتنسيق TXT](./media/er-quick-start2-payment-file3.png)

## <a name="additional-resources"></a><a id="References"></a><span data-ttu-id="d59a4-451">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="d59a4-451">Additional resources</span></span>

- [<span data-ttu-id="d59a4-452">نظرة عامة حول التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="d59a4-452">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="d59a4-453">تنزيل تكوينات ER من Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="d59a4-453">Download ER configurations from Lifecycle Services</span></span>](download-electronic-reporting-configuration-lcs.md)
- [<span data-ttu-id="d59a4-454">تنزيل تكوينات ER من المستودع العمومي لخدمة التكوين</span><span class="sxs-lookup"><span data-stu-id="d59a4-454">Download ER configurations from Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]