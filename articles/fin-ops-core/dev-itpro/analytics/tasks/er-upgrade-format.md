---
title: ترقية التنسيق باعتماد إصدار أساسي جديد لهذا التنسيق في ER
description: يوضح هذا الموضوع كيفيه صيانة تكوين تنسيق للتقارير الكترونيه (ER).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b76fb09ff961a3100b6a4bf890c1b12e6a0a2771
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092556"
---
# <a name="er-upgrade-your-format-by-adopting-a-new-base-version-of-that-format"></a><span data-ttu-id="04882-103">ترقية التنسيق باعتماد إصدار أساسي جديد لهذا التنسيق في ER</span><span class="sxs-lookup"><span data-stu-id="04882-103">ER Upgrade your format by adopting a new, base version of that format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="04882-104">تشرح الخطوات التالية كيف يمكن لمستخدم بدور مسؤول النظام أو مطور التقارير الإلكترونية الحفاظ على تكوين تنسيق التقارير الإلكترونية (ER).</span><span class="sxs-lookup"><span data-stu-id="04882-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can maintain an Electronic reporting (ER) format configuration.</span></span> <span data-ttu-id="04882-105">يوضح هذا الإجراء كيف يمكن إنشاء إصدار مخصص لتنسيق استنادًا إلى التنسيق المستلم من موفر التكوين (CP).</span><span class="sxs-lookup"><span data-stu-id="04882-105">This procedure explains how a custom version of a format can be created based on the format received from a configuration provider (CP).</span></span> <span data-ttu-id="04882-106">وهو يوضح أيضًا كيفية اعتماد إصدار أساسي جديد لهذا التنسيق.</span><span class="sxs-lookup"><span data-stu-id="04882-106">It also explains how to adopt a new, base version of that format.</span></span>

<span data-ttu-id="04882-107">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في إجراءات "إنشاء موفر تكوين ووضع علامة عليه كنشط" "واستخدام تنسيق تم إنشاؤه لإنشاء المستندات الإلكترونية للدفعات".</span><span class="sxs-lookup"><span data-stu-id="04882-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" and "Use created format to generate electronic documents for payments" procedures.</span></span> <span data-ttu-id="04882-108">يمكن تنفيذ هذه الخطوات في شركة GBSI.</span><span class="sxs-lookup"><span data-stu-id="04882-108">These steps can be performed in the GBSI company.</span></span>

## <a name="select-format-configuration-for-customization"></a><span data-ttu-id="04882-109">تحديد تكوين التنسيق للتخصيص</span><span class="sxs-lookup"><span data-stu-id="04882-109">Select format configuration for customization</span></span>
1. <span data-ttu-id="04882-110">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="04882-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="04882-111">في هذا المثال، ستعمل الشركة النموذجية Litware, Inc. (https://www.litware.com) كموفر تكوين يدعم تكوينات التنسيق للدفعات الإلكترونية لبلد بعينه.</span><span class="sxs-lookup"><span data-stu-id="04882-111">In this example, sample company Litware, Inc. (https://www.litware.com) will act as a configuration provider that supports format configurations for electronic payments for a particular country.</span></span>    <span data-ttu-id="04882-112">سوف تعمل الشركة النموذجية Proseware, Inc. (http://www.proseware.com) كمستهلك لتكوين التنسيق الذي تقدمه شركة Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="04882-112">Sample company Proseware, Inc. (http://www.proseware.com) will act as a consumer of the format configuration that Litware, Inc. provided.</span></span> <span data-ttu-id="04882-113">تستخدم Proseware, Inc. تنسيقات في مناطق معينة في ذلك البلد.</span><span class="sxs-lookup"><span data-stu-id="04882-113">Proseware, Inc. uses formats in certain regions of that country.</span></span>  
2. <span data-ttu-id="04882-114">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="04882-114">Click Reporting configurations.</span></span>
3. <span data-ttu-id="04882-115">انقر فوق "إظهار عوامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="04882-115">Click Show filters.</span></span>
4. <span data-ttu-id="04882-116">طبّق عوامل التصفية التالية: أدخل قيمة عامل التصفية "BACS (وهمي في المملكة المتحدة)‬" في حقل "الاسم" باستخدام مشغل عامل التصفية "يبدأ بـ".</span><span class="sxs-lookup"><span data-stu-id="04882-116">Apply the following filters: Enter a filter value of "BACS (UK fictitious)" on the "Name" field using the "begins with" filter operator.</span></span>
  
    <span data-ttu-id="04882-117">تكوين التنسيق المحدد BACS (وهمي في المملكة المتحدة) مملوك من قِبل الموفر Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="04882-117">The selected format configuration BACS (UK fictitious) is owned by provider Litware, Inc.</span></span>  

5. <span data-ttu-id="04882-118">انقر فوق "إظهار عوامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="04882-118">Click Show filters.</span></span>
6. <span data-ttu-id="04882-119">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="04882-119">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="04882-120">سيتم استخدام إصدار التنسيق مع الحالة "مكتملة" بواسطة Proseware, Inc. للتخصيص.</span><span class="sxs-lookup"><span data-stu-id="04882-120">The version of the format with the status of Completed will be used by Proseware, Inc. for customization.</span></span>  

## <a name="create-a-new-configuration-for-your-custom-format-of-electronic-document"></a><span data-ttu-id="04882-121">إنشاء تكوين جديد للتنسيق المخصص الخاص بك لمستند إلكتروني</span><span class="sxs-lookup"><span data-stu-id="04882-121">Create a new configuration for your custom format of electronic document</span></span>
<span data-ttu-id="04882-122">تلقت Proseware, Inc. الإصدار 1.1 من تكوين تنسيق BACS (وهمي في المملكة المتحدة) الذي يحتوي على التنسيق الأولي لإنشاء مستندات الدفع الإلكتروني من شركة .Litware, Inc وفقًا لاشتراك الخدمة.</span><span class="sxs-lookup"><span data-stu-id="04882-122">Proseware, Inc. received version 1.1 of BACS (UK fictitious) configuration that contains the initial format to generate electronic payment documents from Litware, Inc. in accordance to their service subscription.</span></span> <span data-ttu-id="04882-123">تريد Proseware, Inc. بدء استخدام ذلك كمعيار لبلدها، ولكن يلزم إجراء بعض التخصيصات لدعم متطلبات إقليمية محددة.</span><span class="sxs-lookup"><span data-stu-id="04882-123">Proseware, Inc. wants to start using this as a standard for their country but some customization is required to support specific regional requirements.</span></span> <span data-ttu-id="04882-124">تريد Proseware, Inc. أيضًا أن تبقى قادرة على ترقية تنسيق مخصص بمجرد ظهور إصدار جديد منه (مع تغييرات لدعم متطلبات جديدة خاصة بالبلد) من شركة Litware, Inc. وتريد تنفيذ هذه الترقية بأقل تكلفة.</span><span class="sxs-lookup"><span data-stu-id="04882-124">Proseware, Inc. also wants to keep the ability to upgrade a custom format as soon as a new version of it (with changes to support new country-specific requirements) comes from Litware, Inc. and they want to perform this upgrade with the lowest cost.</span></span>  

<span data-ttu-id="04882-125">للقيام بذلك، تحتاج Proseware, Inc. إلى إنشاء تكوين باستخدام تكوينات Litware, Inc. لتنسيق BACS (وهمي في المملكة المتحدة) كأساس.‬</span><span class="sxs-lookup"><span data-stu-id="04882-125">To do this, Proseware, Inc. needs to create a configuration using the Litware, Inc. configuration BACS (UK fictitious) as a base.</span></span>  

1. <span data-ttu-id="04882-126">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="04882-126">Close the page.</span></span>
2. <span data-ttu-id="04882-127">حدد Proseware, Inc. لتحويلها إلى موفر نشط.</span><span class="sxs-lookup"><span data-stu-id="04882-127">Select Proseware, Inc. to make it an active provider.</span></span>
3. <span data-ttu-id="04882-128">انقر فوق "تعيين كنشط".</span><span class="sxs-lookup"><span data-stu-id="04882-128">Click Set active.</span></span>
4. <span data-ttu-id="04882-129">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="04882-129">Click Reporting configurations.</span></span>
5. <span data-ttu-id="04882-130">في الشجرة، قم بتوسيع "المدفوعات (نموذج مبسط)".</span><span class="sxs-lookup"><span data-stu-id="04882-130">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="04882-131">في الشجرة، حدد "Payments (simplified model)\BACS (UK fictitious)".</span><span class="sxs-lookup"><span data-stu-id="04882-131">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>

    <span data-ttu-id="04882-132">حدد تكوين BACS (وهمي المملكة المتحدة) من Litware, Inc. ستستخدم Proseware, Inc. الإصدار 1.1 كأساس للإصدار المخصص.</span><span class="sxs-lookup"><span data-stu-id="04882-132">Select the BACS (UK fictitious) configuration from Litware, Inc. Proseware, Inc. will use version 1.1 as a base for the custom version.</span></span>  

7. <span data-ttu-id="04882-133">انقر فوق "إنشاء تكوين" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="04882-133">Click Create configuration to open the drop dialog.</span></span>

    <span data-ttu-id="04882-134">يسمح لك ذلك بإنشاء تكوين جديد لتنسيق دفع مخصص.</span><span class="sxs-lookup"><span data-stu-id="04882-134">This lets you create a new configuration for a custom payment format.</span></span>  

8. <span data-ttu-id="04882-135">في الحقل "جديد"، أدخل 'اشتقاق من اسم: BACS (وهمي في المملكة المتحدة)، .Litware, Inc".</span><span class="sxs-lookup"><span data-stu-id="04882-135">In the New field, enter 'Derive from Name: BACS (UK fictitious), Litware, Inc.'.</span></span>

    <span data-ttu-id="04882-136">حدد الخيار "اشتقاق" لتأكيد استخدام BACS (وهمي في المملكة المتحدة) كأساس لإنشاء إصدار مخصص.</span><span class="sxs-lookup"><span data-stu-id="04882-136">Select the Derive option to confirm the usage of BACS (UK fictitious) as the base for creating the custom version.</span></span>  

9. <span data-ttu-id="04882-137">في الحقل "الاسم"، اكتب "BACS (مخصص وهمي في المملكة المتحدة)".</span><span class="sxs-lookup"><span data-stu-id="04882-137">In the Name field, type 'BACS (UK fictitious custom)'.</span></span>
10. <span data-ttu-id="04882-138">في حقل "الوصف"، اكتب "دفع مورد BACS (مخصص وهمي في المملكة المتحدة)".</span><span class="sxs-lookup"><span data-stu-id="04882-138">In the Description field, type 'BACS vendor payment (UK fictitious custom)'.</span></span>

    <span data-ttu-id="04882-139">يتم تلقائيًا إدخال موفر التكوين النشط (.Proseware, Inc) هنا.</span><span class="sxs-lookup"><span data-stu-id="04882-139">The active configuration provider (Proseware, Inc.) is automatically entered here.</span></span> <span data-ttu-id="04882-140">سيكون هذا الموفر قادرًا على المحافظة على هذا التكوين.</span><span class="sxs-lookup"><span data-stu-id="04882-140">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="04882-141">باستطاعة موفرين آخرين استخدام هذا التكوين، ولكن لن يكون باستطاعتهم المحافظة عليه.</span><span class="sxs-lookup"><span data-stu-id="04882-141">Other providers can use this configuration, but will not be able to maintain it.</span></span>  

11. <span data-ttu-id="04882-142">وانقر فوق إنشاء تكوين.</span><span class="sxs-lookup"><span data-stu-id="04882-142">Click Create configuration.</span></span>

## <a name="customize-your-format-for-the-electronic-document"></a><span data-ttu-id="04882-143">تخصيص تنسيق المستند الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="04882-143">Customize your format for the electronic document</span></span>
1. <span data-ttu-id="04882-144">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="04882-144">Click Designer.</span></span>
2. <span data-ttu-id="04882-145">انقر فوق "توسيع/طي".</span><span class="sxs-lookup"><span data-stu-id="04882-145">Click Expand/collapse.</span></span>
3. <span data-ttu-id="04882-146">انقر فوق "توسيع/طي".</span><span class="sxs-lookup"><span data-stu-id="04882-146">Click Expand/collapse.</span></span>
4. <span data-ttu-id="04882-147">في الشجرة، حدد "Xml\الرسالة\المدفوعات\الصنف\المورّد\البنك".</span><span class="sxs-lookup"><span data-stu-id="04882-147">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
5. <span data-ttu-id="04882-148">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="04882-148">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="04882-149">في الشجرة، حدد XML/العنصر".</span><span class="sxs-lookup"><span data-stu-id="04882-149">In the tree, select 'XML\Element'.</span></span>
7. <span data-ttu-id="04882-150">في الحقل "الاسم، اكتب "IBAN".</span><span class="sxs-lookup"><span data-stu-id="04882-150">In the Name field, type 'IBAN'.</span></span>
8. <span data-ttu-id="04882-151">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="04882-151">Click OK.</span></span>
9. <span data-ttu-id="04882-152">في الشجرة، حدد "Xml\الرسالة\المدفوعات\الصنف\المورّد\البنك\IBAN".</span><span class="sxs-lookup"><span data-stu-id="04882-152">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\IBAN'.</span></span>
10. <span data-ttu-id="04882-153">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="04882-153">Click Add to open the drop dialog.</span></span>
11. <span data-ttu-id="04882-154">في الشجرة، حدد "Text\String".</span><span class="sxs-lookup"><span data-stu-id="04882-154">In the tree, select 'Text\String'.</span></span>
12. <span data-ttu-id="04882-155">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="04882-155">Click OK.</span></span>
13. <span data-ttu-id="04882-156">في الشجرة، حدد "Xml\الرسالة\المدفوعات\الصنف\المورّد\الاسم\السلسلة".</span><span class="sxs-lookup"><span data-stu-id="04882-156">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
14. <span data-ttu-id="04882-157">في الحقل "الحد الأقصى للطول"، أدخل "60".</span><span class="sxs-lookup"><span data-stu-id="04882-157">In the Maximum length field, enter '60'.</span></span>
15. <span data-ttu-id="04882-158">انقر فوق علامة التبويب "التعيين".</span><span class="sxs-lookup"><span data-stu-id="04882-158">Click the Mapping tab.</span></span>
16. <span data-ttu-id="04882-159">في الشجرة، قم بتوسيع "النموذج"</span><span class="sxs-lookup"><span data-stu-id="04882-159">In the tree, expand 'model'.</span></span>
17. <span data-ttu-id="04882-160">في الشجرة، قم بتوسيع "النموذج/المدفوعات".</span><span class="sxs-lookup"><span data-stu-id="04882-160">In the tree, expand 'model\Payments'.</span></span>
18. <span data-ttu-id="04882-161">في الشجرة، قم بتوسيع "النموذج/المدفوعات/الدائن".</span><span class="sxs-lookup"><span data-stu-id="04882-161">In the tree, expand 'model\Payments\Creditor'.</span></span>
19. <span data-ttu-id="04882-162">في الشجرة، قم بتوسيع "النموذج/المدفوعات/الدائن/الحساب".</span><span class="sxs-lookup"><span data-stu-id="04882-162">In the tree, expand 'model\Payments\Creditor\Account'.</span></span>
20. <span data-ttu-id="04882-163">في الشجرة، حدد "النموذج\المدفوعات\الدائن\الحساب\IBAN".</span><span class="sxs-lookup"><span data-stu-id="04882-163">In the tree, select 'model\Payments\Creditor\Account\IBAN'.</span></span>
21. <span data-ttu-id="04882-164">في الشجرة، حدد "Xml\الرسالة\المدفوعات\الصنف = model.Payments\المورّد\البنك\IBAN\السلسلة'.</span><span class="sxs-lookup"><span data-stu-id="04882-164">In the tree, select 'Xml\Message\Payments\Item =  model.Payments\Vendor\Bank\IBAN\String'.</span></span>
22. <span data-ttu-id="04882-165">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="04882-165">Click Bind.</span></span>
23. <span data-ttu-id="04882-166">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="04882-166">Click Save.</span></span>

## <a name="validate-the-customized-format"></a><span data-ttu-id="04882-167">التحقق من صحة التنسيق المخصص</span><span class="sxs-lookup"><span data-stu-id="04882-167">Validate the customized format</span></span>
1. <span data-ttu-id="04882-168">انقر فوق "التحقق من الصحة‬".</span><span class="sxs-lookup"><span data-stu-id="04882-168">Click Validate.</span></span>

    <span data-ttu-id="04882-169">تحقق من صحة تخطيط التنسيق المخصص وتغييرات تخطيط البيانات للتأكد من أن كافة الروابط على ما يرام.</span><span class="sxs-lookup"><span data-stu-id="04882-169">Validate the customized format layout and data mapping changes to make sure that all bindings are okay.</span></span>  

2. <span data-ttu-id="04882-170">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="04882-170">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-the-custom-format-configuration"></a><span data-ttu-id="04882-171">تغيير حالة الإصدار الحالي لتكوين التنسيق المخصص</span><span class="sxs-lookup"><span data-stu-id="04882-171">Change the status of the current version of the custom format configuration</span></span>
<span data-ttu-id="04882-172">قم بتغيير حالة تكوين التنسيق المصمم من "مسودة" إلى "مكتمل" لجعله متوفرًا لإنشاء مستند الدفع.</span><span class="sxs-lookup"><span data-stu-id="04882-172">Change the status of the designed format configuration from Draft to Completed to make it available for payment document generation.</span></span>  

1. <span data-ttu-id="04882-173">انقر فوق "تغيير الحالة".</span><span class="sxs-lookup"><span data-stu-id="04882-173">Click Change status.</span></span>

    <span data-ttu-id="04882-174">لاحظ أن الإصدار الحالي للتكوين المحدد في حالة "مسودة".</span><span class="sxs-lookup"><span data-stu-id="04882-174">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="04882-175">انقر فوق "مكتمل".</span><span class="sxs-lookup"><span data-stu-id="04882-175">Click Complete.</span></span>
3. <span data-ttu-id="04882-176">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="04882-176">In the Description field, type a value.</span></span>
4. <span data-ttu-id="04882-177">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="04882-177">Click OK.</span></span>
5. <span data-ttu-id="04882-178">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="04882-178">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="04882-179">لاحظ أنه يتم حفظ التكوين الذي يتم إنشاؤه باسم "الإصدار المكتمل 1.1.1".</span><span class="sxs-lookup"><span data-stu-id="04882-179">Note that the created configuration is saved as completed version 1.1.1.</span></span> <span data-ttu-id="04882-180">وهذا يعني أنه الإصدار 1 من التنسيق المخصص BACS (وهمي في المملكة المتحدة)، الذي يستند إلى الإصدار 1 من تنسيق BACS (وهمي في المملكة المتحدة)، الذي يستند إلى الإصدار 1 من نموذج بيانات الدفعات (نموذج مبسط).</span><span class="sxs-lookup"><span data-stu-id="04882-180">This means it is version 1 of the custom BACS (UK fictitious custom) format, which is based on version 1 of the BACS (UK fictitious) format, which is based on version 1 of the Payments (simplified model) data model.</span></span>  

## <a name="test-the-customized-format-to-generate-payment-files"></a><span data-ttu-id="04882-181">اختبار تنسيق مخصص لإنشاء ملفات الدفعات</span><span class="sxs-lookup"><span data-stu-id="04882-181">Test the customized format to generate payment files</span></span>
<span data-ttu-id="04882-182">أكمل الخطوات المذكورة في الإجراء "استخدام التنسيق الذي تم إنشاؤه لإنشاء مستندات إلكترونية للدفعات" في جلسة Finance and Operations موازية.</span><span class="sxs-lookup"><span data-stu-id="04882-182">Complete the steps in the "Use created format to generate electronic documents for payments" procedure in a parallel Finance and Operations session.</span></span> <span data-ttu-id="04882-183">حدد تنسيق BACS (مخصص وهمي في المملكة المتحدة) في معلمات أسلوب الدفع الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="04882-183">Select the BACS (UK fictitious custom) format in electronic payment method parameters.</span></span> <span data-ttu-id="04882-184">تأكد من احتواء ملف الدفع الذي تم إنشاؤه على عقدة XML المقدم حديثًا مما يمثل كود IBAN وفقًا للمتطلبات الإقليمية.</span><span class="sxs-lookup"><span data-stu-id="04882-184">Make sure that the created payment file contains the recently introduced XML node presenting IBAN code in accordance to regional requirements.</span></span>  

## <a name="update-the-existing-country-specific-configuration"></a><span data-ttu-id="04882-185">تحديث التكوين الحالي الخاص بالدولة</span><span class="sxs-lookup"><span data-stu-id="04882-185">Update the existing country-specific configuration</span></span>
<span data-ttu-id="04882-186">تحتاج Litware, Inc. إلى تحديث تكوين BACS (وهمي في المملكة المتحدة) واعتماد متطلبات بلد جديدة لإدارة تنسيق المستند الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="04882-186">Litware, Inc. needs to update the BACS (UK fictitious) configuration and adopt new country requirements for managing the format of the electronic document.</span></span> <span data-ttu-id="04882-187">لاحقاً، سيتم تضمين ذلك في الإصدار الجديد لهذا التكوين الذي سيتم تقديمه لمشتركي الخدمة، بما في ذلك Proseware, Inc.</span><span class="sxs-lookup"><span data-stu-id="04882-187">Later, this will be enclosed in a new version of this configuration that will be offered for service subscribers, including Proseware, Inc.</span></span>  

<span data-ttu-id="04882-188">في العمليات المتعلقة بتوفير الخدمة الفعلية ،يمكن استيراد كل إصدار جديد لـ BACS (وهمي من المملكة المتحدة) عن طريق Proseware, Inc. من مستودع LCS لتكوينات Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="04882-188">In real service provision related processes, each new version of BACS (UK fictitious) can be imported by Proseware, Inc. from Litware, Inc. configurations' LCS repository.</span></span> <span data-ttu-id="04882-189">في هذا الإجراء سنقوم بمحاكاة هذا عن طريق تحديث BACS (وهمي في المملكة المتحدة) نيابة عن موفر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="04882-189">In this procedure we will simulate this by updating BACS (UK fictitious) on behalf of a service provider.</span></span>  

1. <span data-ttu-id="04882-190">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="04882-190">Close the page.</span></span>
2. <span data-ttu-id="04882-191">حدد Litware, inc. .</span><span class="sxs-lookup"><span data-stu-id="04882-191">Select Litware, inc. provider.</span></span>
3. <span data-ttu-id="04882-192">انقر فوق "تعيين كنشط".</span><span class="sxs-lookup"><span data-stu-id="04882-192">Click Set active.</span></span>
4. <span data-ttu-id="04882-193">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="04882-193">Click Reporting configurations.</span></span>
5. <span data-ttu-id="04882-194">في الشجرة، قم بتوسيع "المدفوعات (نموذج مبسط)".</span><span class="sxs-lookup"><span data-stu-id="04882-194">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="04882-195">في الشجرة، حدد "Payments (simplified model)\BACS (UK fictitious)".</span><span class="sxs-lookup"><span data-stu-id="04882-195">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>

    <span data-ttu-id="04882-196">سيتم تحديد إصدار المسودة المملوك لشركة .Litware, Inc موفر BACS (وهمي في المملكة المتحدة) لإظهار التغييرات لدعم متطلبات جديدة الخاصة بالدولة.</span><span class="sxs-lookup"><span data-stu-id="04882-196">The draft version owned by Litware, Inc. provider BACS (UK fictitious) is selected to bring in changes to support new country-specific requirements.</span></span>  

## <a name="localize-the-base-format-of-the-electronic-document"></a><span data-ttu-id="04882-197">ترجمة التنسيق الأساسي للمستند الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="04882-197">Localize the base format of the electronic document</span></span>
<span data-ttu-id="04882-198">افترض وجود بعض المتطلبات الجديدة الخاصة بالبلد والتي من المقرر دعمها بواسطة Litware, Inc.:</span><span class="sxs-lookup"><span data-stu-id="04882-198">Assume that there are new country-specific requirements to be supported by Litware, Inc.:</span></span>  

- <span data-ttu-id="04882-199">قيمة لرمز SWIFT البنكي لحساب الدائن في كل حركة دفع.</span><span class="sxs-lookup"><span data-stu-id="04882-199">A value for the creditor's bank SWIFT code in each payment transaction.</span></span>
- <span data-ttu-id="04882-200">حد من 100 حرفًا لطول النص لاسم المورد في إنشاء ملف.</span><span class="sxs-lookup"><span data-stu-id="04882-200">A limit of 100 characters for the length of text for the vendor's name in a generating file.</span></span>  
- <span data-ttu-id="04882-201">متطلبات جديدة خاصة بالدولة</span><span class="sxs-lookup"><span data-stu-id="04882-201">New country-specific requirements</span></span>  
- <span data-ttu-id="04882-202">حدد إصدار المسودة للتكوين المطلوب لتقديم التغييرات المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="04882-202">Select the draft version of the desired configuration to introduce required changes.</span></span>  


1. <span data-ttu-id="04882-203">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="04882-203">Click Designer.</span></span>
2. <span data-ttu-id="04882-204">انقر فوق "توسيع/طي".</span><span class="sxs-lookup"><span data-stu-id="04882-204">Click Expand/collapse.</span></span>
3. <span data-ttu-id="04882-205">انقر فوق "توسيع/طي".</span><span class="sxs-lookup"><span data-stu-id="04882-205">Click Expand/collapse.</span></span>
4. <span data-ttu-id="04882-206">في الشجرة، حدد "Xml\الرسالة\المدفوعات\الصنف\المورّد\البنك".</span><span class="sxs-lookup"><span data-stu-id="04882-206">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
5. <span data-ttu-id="04882-207">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="04882-207">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="04882-208">في الشجرة، حدد XML/العنصر".</span><span class="sxs-lookup"><span data-stu-id="04882-208">In the tree, select 'XML\Element'.</span></span>
7. <span data-ttu-id="04882-209">في الحقل "الاسم"، اكتب "SWIFT".</span><span class="sxs-lookup"><span data-stu-id="04882-209">In the Name field, type 'SWIFT'.</span></span>
8. <span data-ttu-id="04882-210">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="04882-210">Click OK.</span></span>
9. <span data-ttu-id="04882-211">في الشجرة، حدد "Xml\الرسالة\المدفوعات\الصنف\المورّد\البنك\SWIFT".</span><span class="sxs-lookup"><span data-stu-id="04882-211">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\SWIFT'.</span></span>
10. <span data-ttu-id="04882-212">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="04882-212">Click Add to open the drop dialog.</span></span>
11. <span data-ttu-id="04882-213">في الشجرة، حدد "Text\String".</span><span class="sxs-lookup"><span data-stu-id="04882-213">In the tree, select 'Text\String'.</span></span>
12. <span data-ttu-id="04882-214">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="04882-214">Click OK.</span></span>
13. <span data-ttu-id="04882-215">في الشجرة، حدد "Xml\الرسالة\المدفوعات\الصنف\المورّد\الاسم\السلسلة".</span><span class="sxs-lookup"><span data-stu-id="04882-215">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
14. <span data-ttu-id="04882-216">في الحقل "الحد الأقصى للطول"، أدخل "100".</span><span class="sxs-lookup"><span data-stu-id="04882-216">In the Maximum length field, enter '100'.</span></span>
15. <span data-ttu-id="04882-217">انقر فوق علامة التبويب "التعيين".</span><span class="sxs-lookup"><span data-stu-id="04882-217">Click the Mapping tab.</span></span>
16. <span data-ttu-id="04882-218">في الشجرة، قم بتوسيع "النموذج"</span><span class="sxs-lookup"><span data-stu-id="04882-218">In the tree, expand 'model'.</span></span>
17. <span data-ttu-id="04882-219">في الشجرة، قم بتوسيع "النموذج/المدفوعات".</span><span class="sxs-lookup"><span data-stu-id="04882-219">In the tree, expand 'model\Payments'.</span></span>
18. <span data-ttu-id="04882-220">في الشجرة، قم بتوسيع "النموذج/المدفوعات/الدائن".</span><span class="sxs-lookup"><span data-stu-id="04882-220">In the tree, expand 'model\Payments\Creditor'.</span></span>
19. <span data-ttu-id="04882-221">في الشجرة، قم بتوسيع "النموذج/المدفوعات/الدائن/الوكيل".</span><span class="sxs-lookup"><span data-stu-id="04882-221">In the tree, expand 'model\Payments\Creditor\Agent'.</span></span>
20. <span data-ttu-id="04882-222">في الشجرة، حدد "النموذج\المدفوعات\الدائن\الوكيل\SWIFT".</span><span class="sxs-lookup"><span data-stu-id="04882-222">In the tree, select 'model\Payments\Creditor\Agent\SWIFT'.</span></span>
21. <span data-ttu-id="04882-223">في الشجرة، حدد "Xml\الرسالة\المدفوعات\الصنف = model.Payments\المورّد\البنك\SWIFT\السلسلة'.</span><span class="sxs-lookup"><span data-stu-id="04882-223">In the tree, select 'Xml\Message\Payments\Item =  model.Payments\Vendor\Bank\SWIFT\String'.</span></span>
22. <span data-ttu-id="04882-224">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="04882-224">Click Bind.</span></span>
23. <span data-ttu-id="04882-225">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="04882-225">Click Save.</span></span>

## <a name="validate-the-localized-format"></a><span data-ttu-id="04882-226">التحقق من صحة التنسيق المترجم</span><span class="sxs-lookup"><span data-stu-id="04882-226">Validate the localized format</span></span>
1. <span data-ttu-id="04882-227">انقر فوق "التحقق من الصحة‬".</span><span class="sxs-lookup"><span data-stu-id="04882-227">Click Validate.</span></span>
2. <span data-ttu-id="04882-228">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="04882-228">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-the-base-format-configuration"></a><span data-ttu-id="04882-229">تغيير حالة الإصدار الحالي لتكوين التنسيق الأساسي</span><span class="sxs-lookup"><span data-stu-id="04882-229">Change the status of the current version of the base format configuration</span></span>
<span data-ttu-id="04882-230">قم بتغيير حالة تكوين التنسيق الأساسي المحدث من "مسودة" إلى "مكتمل" لجعله متوفرًا لإنشاء مستندات الدفع وتحديثات تكوينات التنسيق المشتقة منه.</span><span class="sxs-lookup"><span data-stu-id="04882-230">Change the status of the updated base format configuration from Draft to Completed to make it available for generation of payment documents and updates of format configurations derived from it.</span></span>  

1. <span data-ttu-id="04882-231">انقر فوق "تغيير الحالة".</span><span class="sxs-lookup"><span data-stu-id="04882-231">Click Change status.</span></span>

    <span data-ttu-id="04882-232">لاحظ أن الإصدار الحالي للتكوين المحدد في حالة "مسودة".</span><span class="sxs-lookup"><span data-stu-id="04882-232">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="04882-233">انقر فوق "مكتمل".</span><span class="sxs-lookup"><span data-stu-id="04882-233">Click Complete.</span></span>
3. <span data-ttu-id="04882-234">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="04882-234">In the Description field, type a value.</span></span>
4. <span data-ttu-id="04882-235">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="04882-235">Click OK.</span></span>
5. <span data-ttu-id="04882-236">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="04882-236">In the list, find and select the desired record.</span></span>

## <a name="change-the-base-version-for-the-custom-format-configuration"></a><span data-ttu-id="04882-237">تغيير الإصدار الأساسي لتكوين التنسيق المخصص</span><span class="sxs-lookup"><span data-stu-id="04882-237">Change the base version for the custom format configuration</span></span>

<span data-ttu-id="04882-238">يتم إعلام Proseware, Inc. بأن الإصدار الجديد 1.2 لتكوين BACS (وهمي في المملكة المتحدة) متوفر لإنشاء مستندات الدفع الإلكتروني وفقًا للمتطلبات المعلن عنها مؤخرًا الخاصة بالبلد.</span><span class="sxs-lookup"><span data-stu-id="04882-238">Proseware, Inc. is informed that a new version 1.2 of BACS (UK fictitious) configuration is available to generate electronic payment documents in accordance to recently announced country-specific requirements.</span></span> <span data-ttu-id="04882-239">تريد Proseware, Inc. أن تبدأ استخدامه كمعيار للبلد.</span><span class="sxs-lookup"><span data-stu-id="04882-239">Proseware, Inc. wants to start using it as a standard for the country.</span></span>  

<span data-ttu-id="04882-240">لإجراء ذلك، تحتاج Proseware, Inc. إلى تغيير إصدار التكوين الأساسي للتكوين المخصص BACS (مخصص وهمي في المملكة المتحدة).</span><span class="sxs-lookup"><span data-stu-id="04882-240">To do this, Proseware, Inc. needs to change the base configuration version for the custom configuration BACS (UK fictitious custom).</span></span> <span data-ttu-id="04882-241">بدلاً من الإصدار 1.1 من BACS (وهمي في المملكة المتحدة) الذي يستخدم الإصدار 1.2 الجديد.</span><span class="sxs-lookup"><span data-stu-id="04882-241">Instead of version 1.1 of BACS (UK fictitious) use new version 1.2.</span></span>  

1. <span data-ttu-id="04882-242">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="04882-242">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="04882-243">حدد الموفر Proseware, Inc. لتمييزه كموفر نشط.</span><span class="sxs-lookup"><span data-stu-id="04882-243">Select the Proseware, Inc. provider to mark it as active.</span></span>
3. <span data-ttu-id="04882-244">انقر فوق "تعيين كنشط".</span><span class="sxs-lookup"><span data-stu-id="04882-244">Click Set active.</span></span>
4. <span data-ttu-id="04882-245">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="04882-245">Click Reporting configurations.</span></span>
5. <span data-ttu-id="04882-246">في الشجرة، قم بتوسيع "المدفوعات (نموذج مبسط)".</span><span class="sxs-lookup"><span data-stu-id="04882-246">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="04882-247">في الشجرة، قم بتوسيع "Payments (simplified model)\BACS (UK fictitious)".</span><span class="sxs-lookup"><span data-stu-id="04882-247">In the tree, expand 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>
7. <span data-ttu-id="04882-248">في الشجرة، حدد "Payments (simplified model)\BACS (UK fictitious)\BACS (UK fictitious custom)".</span><span class="sxs-lookup"><span data-stu-id="04882-248">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)\BACS (UK fictitious custom)'.</span></span>

    <span data-ttu-id="04882-249">حدد التكوين BACS (مخصص وهمي في المملكة المتحدة)، المملوك من قبل Proseware, Inc.</span><span class="sxs-lookup"><span data-stu-id="04882-249">Select the BACS (UK fictitious custom) configuration, which is owned by Proseware, Inc.</span></span>  

    <span data-ttu-id="04882-250">استخدم إصدار المسودة للتكوين المحدد لتقديم التغييرات المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="04882-250">Use the draft version of the selected configuration to introduce required changes.</span></span>  

8. <span data-ttu-id="04882-251">انقر فوق "تغيير العنوان الأساسي.</span><span class="sxs-lookup"><span data-stu-id="04882-251">Click Rebase.</span></span>

    <span data-ttu-id="04882-252">حدد الإصدار الجديد 1.2 من التكوين الأساسي ليتم استخدامه كقاعدة جديدة لتحديث التكوين.</span><span class="sxs-lookup"><span data-stu-id="04882-252">Select the new version 1.2 of the base configuration to be applied as a new base for updating the configuration.</span></span>  

9. <span data-ttu-id="04882-253">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="04882-253">Click OK.</span></span>

    <span data-ttu-id="04882-254">لاحظ أنه تم اكتشاف بعض التعارضات بين دمج الإصدار المخصص والإصدار الأساسي الجديد مما يمثل بعض تغييرات التنسيق التي لا يمكن دمجها تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="04882-254">Note that some conflicts have been discovered between merging the custom version and a new base version representing some format changes that can't be merged automatically.</span></span>  

## <a name="resolve-rebase-conflicts"></a><span data-ttu-id="04882-255">حل تعارضات تغيير العنوان الأساسي</span><span class="sxs-lookup"><span data-stu-id="04882-255">Resolve rebase conflicts</span></span>
1. <span data-ttu-id="04882-256">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="04882-256">Click Designer.</span></span>
    
    <span data-ttu-id="04882-257">لاحظ أنه يتعذر حل التغييرات التي تطرأ على حد طول نص اسم المورد تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="04882-257">Note that changes to the vendor's name text length limit couldn't be resolved automatically.</span></span> <span data-ttu-id="04882-258">لذلك، يتم تقديم هذا كقائمة تعارضات.</span><span class="sxs-lookup"><span data-stu-id="04882-258">Therefore, this is presented in a conflicts list.</span></span> <span data-ttu-id="04882-259">لكل تعارض من النوع "تحديث"، تتوافر الخيارات التالية: - تطبيق قيمة أساسية سابقة (الزر فوق الشبكة) لإظهار قيمة الإصدار الأساسي السابق (0 في هذه الحالة).</span><span class="sxs-lookup"><span data-stu-id="04882-259">For each conflict of type Update, the following options are available:  - Apply a prior base value (button on top of the grid) to bring in the previous base version value (0 in our case).</span></span>  <span data-ttu-id="04882-260">- تطبيق قيمة أساسية (الزر فوق الشبكة) لإظهار قيمة الإصدار الأساسي الجديد (100 الحالة الخاصة بنا).</span><span class="sxs-lookup"><span data-stu-id="04882-260">- Apply a base value (button on top of the grid) to bring in the new base version value (100 in our case).</span></span>  <span data-ttu-id="04882-261">- الاحتفاظ بقيمتك الخاصة (مخصص) (60 في هذه الحالة).</span><span class="sxs-lookup"><span data-stu-id="04882-261">- Keep your own (custom) value (60 in our case).</span></span>  <span data-ttu-id="04882-262">انقر فوق تطبيق القيمة الأساسية لتطبيق حد معين للدولة يبلغ 100 حرفًا لطول نص اسم المورد.</span><span class="sxs-lookup"><span data-stu-id="04882-262">Click Apply base value to apply a country-specific limit of 100 characters for vendor's name text length.</span></span>  

    <span data-ttu-id="04882-263">لاحظ أن .Proseware, Inc و.Litware, Inc لديهما الإصدارات المحلية والمخصصة لهذا التنسيق باستخدام أكواد IBAN وSWIFT مع المكونات ذات الصلة التي يتم دمجها تلقائيًا بإدارة التنسيق.</span><span class="sxs-lookup"><span data-stu-id="04882-263">Note that Proseware, Inc. and Litware, Inc. have custom and local versions of this format using IBAN and SWIFT codes with related components that are automatically merged in the managing format.</span></span>  

2. <span data-ttu-id="04882-264">انقر فوق تطبيق القيمة الأساسية.</span><span class="sxs-lookup"><span data-stu-id="04882-264">Click Apply base value.</span></span>

    <span data-ttu-id="04882-265">انقر فوق تطبيق القيمة الأساسية لتطبيق الحد المعين للدولة البالغ 100 حرفًا لأسماء الموردين.</span><span class="sxs-lookup"><span data-stu-id="04882-265">Click Apply base value to apply the country-specific limit of 100 characters for vendor names.</span></span>  

3. <span data-ttu-id="04882-266">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="04882-266">Click Save.</span></span>

    <span data-ttu-id="04882-267">سيعمل حفظ التنسيق على إزالة التعارضات المحلولة من قائمة التعارضات.</span><span class="sxs-lookup"><span data-stu-id="04882-267">Saving the format will remove resolved conflicts from the conflicts list.</span></span>  

4. <span data-ttu-id="04882-268">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="04882-268">Close the page.</span></span>

## <a name="change-the-status-of-the-new-version-of-the-custom-format-configuration"></a><span data-ttu-id="04882-269">تغيير حالة الإصدار الجديد لتكوين التنسيق المخصص</span><span class="sxs-lookup"><span data-stu-id="04882-269">Change the status of the new version of the custom format configuration</span></span>
1. <span data-ttu-id="04882-270">انقر فوق "تغيير الحالة".</span><span class="sxs-lookup"><span data-stu-id="04882-270">Click Change status.</span></span>

    <span data-ttu-id="04882-271">قم بتغيير حالة تكوين التنسيق المخصص والمحدث من "مسودة" إلى "مكتمل".</span><span class="sxs-lookup"><span data-stu-id="04882-271">Change the status of the updated, custom format configuration from Draft to Completed.</span></span> <span data-ttu-id="04882-272">سيؤدي ذلك إلى يجعل تكوين التنسيق متاحًا لإنشاء مستندات الدفع.</span><span class="sxs-lookup"><span data-stu-id="04882-272">This will make the format configuration available for generating payment documents.</span></span> <span data-ttu-id="04882-273">لاحظ أن الإصدار الحالي للتكوين المحدد في حالة "مسودة".</span><span class="sxs-lookup"><span data-stu-id="04882-273">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="04882-274">انقر فوق "مكتمل".</span><span class="sxs-lookup"><span data-stu-id="04882-274">Click Complete.</span></span>
3. <span data-ttu-id="04882-275">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="04882-275">In the Description field, type a value.</span></span>
4. <span data-ttu-id="04882-276">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="04882-276">Click OK.</span></span>

    <span data-ttu-id="04882-277">لاحظ أنه يتم حفظ التكوين الذي تم إنشاؤه كإصدار مكتمل النسخة 1.2.2: تنسيق الإصدار 2 من BACS الأساسية (مخصص وهمي في المملكة المتحدة)، الذي يستند إلى تنسيق الإصدار 2 من BACS الأساسية (وهمي في المملكة المتحدة)، الذي يستند إلى نموذج بيانات الإصدار 1 من الدفعات (النموذج المبسط).</span><span class="sxs-lookup"><span data-stu-id="04882-277">Note that the created configuration is saved as completed version 1.2.2: version 2 of base BACS (UK fictitious custom) format, which is based on version 2 of base BACS (UK fictitious) format, which is based on version 1 of Payments (simplified model) data model.</span></span>  

## <a name="test-the-customized-format-for-payment-files-generation"></a><span data-ttu-id="04882-278">اختبار التنسيق المخصص لإنشاء ملفات الدفعات</span><span class="sxs-lookup"><span data-stu-id="04882-278">Test the customized format for payment files generation</span></span>
<span data-ttu-id="04882-279">أكمل الخطوات المذكورة في الإجراء "استخدام التنسيق الذي تم إنشاؤه لإنشاء مستندات إلكترونية للدفعات" في جلسة Finance and Operations موازية.</span><span class="sxs-lookup"><span data-stu-id="04882-279">Complete the steps in the "Use created format to generate electronic documents for payments" procedure in parallel Finance and Operations session.</span></span> <span data-ttu-id="04882-280">حدد تنسيق BACS (مخصص وهمي في المملكة المتحدة) الذي تم إنشاؤه في معلمات أسلوب الدفع الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="04882-280">Select the created 'BACS (UK fictitious custom)' format in electronic payment method parameters.</span></span> <span data-ttu-id="04882-281">تأكد من احتواء ملف الدفع الذي تم إنشاؤه على عقدة Proseware, Inc. XML المقدمة حديثًا التي تقدم كود IBAN وفقًا للمتطلبات الإقليمية.</span><span class="sxs-lookup"><span data-stu-id="04882-281">Make sure that the created payment file contains recently introduced by Proseware, Inc. XML node presenting IBAN account code in accordance to regional requirements.</span></span> <span data-ttu-id="04882-282">يجب أن يحتوي الملف أيضًا على عقدة Litware, Inc. XML المقدمة حديثًا التي تقدم كود البنك SWIFT وفقًا لمتطلبات البلد.</span><span class="sxs-lookup"><span data-stu-id="04882-282">The file also should contain the recently introduced by Litware, Inc. XML node presenting SWIFT bank code in accordance to country requirements.</span></span>  

