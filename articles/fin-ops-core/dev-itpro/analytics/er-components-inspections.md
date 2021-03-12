---
title: فحص مكون التقارير الإلكترونية الذي تم تكوينه لمنع مشكلات وقت التشغيل
description: يشرح هذا الموضوع كيفية فحص مكونات التقارير الإلكترونية (التقارير الإلكترونية) المكونة لمنع مشكلات وقت التشغيل التي قد تحدث.
author: NickSelin
manager: AnnBe
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4ba696fb7a8d9083d11cc29953cf1340a581afcf
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797331"
---
# <a name="inspect-the-configured-er-component-to-prevent-runtime-issues"></a><span data-ttu-id="57bb3-103">فحص مكون التقارير الإلكترونية الذي تم تكوينه لمنع مشكلات وقت التشغيل</span><span class="sxs-lookup"><span data-stu-id="57bb3-103">Inspect the configured ER component to prevent runtime issues</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="57bb3-104">كل [تنسيق تقرير إلكتروني (التقارير الإلكترونية)](general-electronic-reporting.md) [تم تكوينه](general-electronic-reporting.md#FormatComponentOutbound) و[تعيين النموذج](general-electronic-reporting.md#data-model-and-model-mapping-components) يمكن [التحقق منه](er-fillable-excel.md#validate-an-er-format) في وقت التصميم.</span><span class="sxs-lookup"><span data-stu-id="57bb3-104">Every configured [Electronic reporting (ER)](general-electronic-reporting.md) [format](general-electronic-reporting.md#FormatComponentOutbound) and [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) component can be [validated](er-fillable-excel.md#validate-an-er-format) at design time.</span></span> <span data-ttu-id="57bb3-105">أثناء هذا التحقق من الصحة، يتم إجراء فحص تناسق للمساعدة في منع مشكلات وقت التشغيل التي قد تحدث، مثل أخطاء التنفيذ وتدهور الأداء.</span><span class="sxs-lookup"><span data-stu-id="57bb3-105">During this validation, a consistency check runs to help prevent runtime issues that might occur, such as execution errors and performance degradation.</span></span> <span data-ttu-id="57bb3-106">لكل مشكله تم العثور عليها، يتم توفير مسار العنصر المتسبب في حدوث مشكلات.</span><span class="sxs-lookup"><span data-stu-id="57bb3-106">For every issue found, the check provides the path of a problematic element.</span></span> <span data-ttu-id="57bb3-107">بالنسبة لبعض المشكلات، يتوفر إصلاح تلقائي.</span><span class="sxs-lookup"><span data-stu-id="57bb3-107">For some issues, an automatic fix is available.</span></span>

<span data-ttu-id="57bb3-108">بشكل افتراضي، يتم تطبيق التحقق تلقائيًا في الحالات التالية لتكوين التقارير الإلكترونية الذي يحتوي على مكونات التقارير الإلكترونية المذكورة سابقًا:</span><span class="sxs-lookup"><span data-stu-id="57bb3-108">By default, the validation is automatically applied in the following cases for an ER configuration that contains the previously mentioned ER components:</span></span>

- <span data-ttu-id="57bb3-109">يمكنك [استيراد](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) إصدار [جديد](general-electronic-reporting.md#component-versioning)من تكوين التقارير الإلكترونية إلى مثيل Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="57bb3-109">You [import](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) a new [version](general-electronic-reporting.md#component-versioning) of an ER configuration into your instance of Microsoft Dynamics 365 Finance.</span></span>
- <span data-ttu-id="57bb3-110">وتقوم بتغيير [حالة](general-electronic-reporting.md#component-versioning) تكوين التقارير الإلكتروني القابل للتحرير من **مسودة** إلى **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-110">You change the [status](general-electronic-reporting.md#component-versioning) of the editable ER configuration from **Draft** to **Completed**.</span></span>
- <span data-ttu-id="57bb3-111">يمكنك [إعادة تعريف](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase) تكوين تقارير إلكترونية قابل للتحرير عن طريق استخدام إصدار أساسي جديد.</span><span class="sxs-lookup"><span data-stu-id="57bb3-111">You [rebase](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase) an editable ER configuration by applying a new base version.</span></span>

<span data-ttu-id="57bb3-112">يمكنك تشغيل هذا التحقق بشكل صريح.</span><span class="sxs-lookup"><span data-stu-id="57bb3-112">You can explicitly run this validation.</span></span> <span data-ttu-id="57bb3-113">حدد أحد الخيارات الثلاثة التالية، واتبع الخطوات المتوفرة:</span><span class="sxs-lookup"><span data-stu-id="57bb3-113">Select one of the following three options, and follow the steps that are provided:</span></span>

- <span data-ttu-id="57bb3-114">الخيار 1:</span><span class="sxs-lookup"><span data-stu-id="57bb3-114">Option 1:</span></span>

    1. <span data-ttu-id="57bb3-115">انتقل إلى **إدارة المؤسسة \> التقارير الإلكترونية \> التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-115">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
    2. <span data-ttu-id="57bb3-116">في شجره التكوينات الموجودة في الجزء الأيمن، حدد تكوين التقارير الإلكترونية المطلوب الذي يحتوي علي التنسيق الخاص ب التقارير الإلكترونية أو مكون تعيين نموذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="57bb3-116">In the configurations tree in the left pane, select the desired ER configuration that contains the ER format or ER model mapping component.</span></span>
    3. <span data-ttu-id="57bb3-117">على علامة التبويب السريعة **إصدارات**، حدد الإصدار المطلوب لتكوين التقارير الإلكترونية المحدد.</span><span class="sxs-lookup"><span data-stu-id="57bb3-117">On the **Versions** FastTab, select the desired version of the selected ER configuration.</span></span>
    4. <span data-ttu-id="57bb3-118">في جزء الإجراءات، حدد **التحقق**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-118">On the Action Pane, select **Validate**.</span></span>

- <span data-ttu-id="57bb3-119">الخيار 2، لتنسيق التقارير الإلكترونية:</span><span class="sxs-lookup"><span data-stu-id="57bb3-119">Option 2, for an ER format:</span></span>

    1. <span data-ttu-id="57bb3-120">انتقل إلى **إدارة المؤسسة \> التقارير الإلكترونية \> التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-120">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
    2. <span data-ttu-id="57bb3-121">في شجره التكوينات الموجودة في الجزء الأيمن، حدد تكوين التقارير الإلكترونية المطلوب الذي يحتوي على مكون تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="57bb3-121">In the configurations tree in the left pane, select the desired ER configuration that contains the ER format component.</span></span>
    3. <span data-ttu-id="57bb3-122">على علامة التبويب السريعة **إصدارات**، حدد الإصدار المطلوب لتكوين التقارير الإلكترونية المحدد.</span><span class="sxs-lookup"><span data-stu-id="57bb3-122">On the **Versions** FastTab, select the desired version of the selected ER configuration.</span></span>
    4. <span data-ttu-id="57bb3-123">في جزء الإجراءات، حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-123">On the Action Pane, select **Designer**.</span></span>
    5. <span data-ttu-id="57bb3-124">في صفحة **مصمم التنسيق**، في جزء الإجراءات، حدد **تحقق من الصحة**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-124">On the **Format designer** page, on the Action Pane, select **Validate**.</span></span>

- <span data-ttu-id="57bb3-125">الخيار 3، لتعيين نموذج التقارير الإلكترونية:</span><span class="sxs-lookup"><span data-stu-id="57bb3-125">Option 3, for an ER model mapping:</span></span>

    1. <span data-ttu-id="57bb3-126">انتقل إلى **إدارة المؤسسة \> التقارير الإلكترونية \> التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-126">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
    2. <span data-ttu-id="57bb3-127">في شجره التكوينات الموجودة في الجزء الأيمن، حدد تكوين التقارير الإلكترونية المطلوب الذي يحتوي على مكون تعيين نموذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="57bb3-127">In the configurations tree in the left pane, select the desired ER configuration that contains the ER model mapping component.</span></span>
    3. <span data-ttu-id="57bb3-128">على علامة التبويب السريعة **إصدارات**، حدد الإصدار المطلوب لتكوين التقارير الإلكترونية المحدد.</span><span class="sxs-lookup"><span data-stu-id="57bb3-128">On the **Versions** FastTab, select the desired version of the selected ER configuration.</span></span>
    4. <span data-ttu-id="57bb3-129">في جزء الإجراءات، حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-129">On the Action Pane, select **Designer**.</span></span>
    5. <span data-ttu-id="57bb3-130">في صفحة **تعيين النموذج إلى مصدر البيانات** في جزء الإجراءات، حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-130">On the **Model to datasource mapping** page, on the Action Pane, select **Designer**.</span></span>
    6. <span data-ttu-id="57bb3-131">في صفحة **مصمم تعيين النموذج** في جزء الإجراءات، حدد **التحقق من الصحة**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-131">On the **Model mapping designer** page, on the Action Pane, select **Validate**.</span></span>

<span data-ttu-id="57bb3-132">لتخطي التحقق من الصحة عند استيراد التكوين، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="57bb3-132">To skip the validation when the configuration is imported, follow these steps.</span></span>

1. <span data-ttu-id="57bb3-133">انتقل إلى **إدارة المؤسسة \> التقارير الإلكترونية \> التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-133">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="57bb3-134">في صفحة **التكوينات**، في جزء الإجراءات، في علامة التبويب **التكوينات**، في مجموعة **الإعدادات المتقدمة**، حدد **معلمات المستخدمين**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-134">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="57bb3-135">قم بتعيين الخيار **التحقق من صحة التكوين بعد الاستيراد** إلى **لا**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-135">Set the **Validate the configuration after importing** option to **No**.</span></span>

<span data-ttu-id="57bb3-136">لتخطي عمليه التحقق من الصحة عند تغيير حاله الإصدار أو إعادة تعريفه، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="57bb3-136">To skip the validation when you change or rebase the version's status, follow these steps.</span></span>

1. <span data-ttu-id="57bb3-137">انتقل إلى **إدارة المؤسسة \> التقارير الإلكترونية \> التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-137">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="57bb3-138">في صفحة **التكوينات**، في جزء الإجراءات، في علامة التبويب **التكوينات**، في مجموعة **الإعدادات المتقدمة**، حدد **معلمات المستخدمين**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-138">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="57bb3-139">قم بتعيين خيار **تخطي التحقق من الصحة عند تغيير حاله التكوين وإعادة تعريفه** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-139">Set the **Skip validation at configuration's status change and rebase** option to **Yes**.</span></span>

<span data-ttu-id="57bb3-140">يستخدم التقارير الإلكترونية الفئات التالية لتجميع عمليات فحص التناسق:</span><span class="sxs-lookup"><span data-stu-id="57bb3-140">ER uses the following categories to group consistency check inspections:</span></span>

- <span data-ttu-id="57bb3-141">**إمكانية التنفيذ** – عمليات فحص التي تكشف عن المشكلات الحرجة التي قد تحدث في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="57bb3-141">**Executability** – Inspections that detect critical issues that might happen at runtime.</span></span> <span data-ttu-id="57bb3-142">وغالبا ما تكون هذه المشكلات في مستوى **الخطأ**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-142">These issues are mostly at an **Error** level.</span></span> 
- <span data-ttu-id="57bb3-143">**الأداء** – عمليات الفحص التي تكشف عن المشكلات التي قد تتسبب في تنفيذ غير فعال لمكونات التقارير الإلكترونية التي تم تكوينها.</span><span class="sxs-lookup"><span data-stu-id="57bb3-143">**Performance** – Inspections that detect issues that might cause inefficient execution of configured ER components.</span></span> <span data-ttu-id="57bb3-144">وغالبا ما تكون هذه المشكلات في مستوى **التحذير**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-144">These issues are mostly at a **Warning** level.</span></span>
- <span data-ttu-id="57bb3-145">**تكامل البيانات** – عمليات الفحص التي تكشف عن المشكلات التي قد تتسبب في فقد البيانات أو مشكلات وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="57bb3-145">**Data integrity** – Inspections that detect issues that might cause data loss or runtime issues.</span></span> <span data-ttu-id="57bb3-146">وغالبا ما تكون هذه المشكلات في مستوى **التحذير**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-146">These issues are mostly at a **Warning** level.</span></span>

## <a name="list-of-inspections"></a><span data-ttu-id="57bb3-147">قائمه عمليات الفحص</span><span class="sxs-lookup"><span data-stu-id="57bb3-147">List of inspections</span></span>

<span data-ttu-id="57bb3-148">يوفر الجدول التالي نظرة عامة على عمليات الفحص التي توفرها التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="57bb3-148">The following table provides an overview of the inspections that ER provides.</span></span> <span data-ttu-id="57bb3-149">لمزيد من المعلومات حول عمليات الفحص هذه، استخدم الارتباطات الموجودة في العمود الأول للانتقال إلى الأقسام ذات الصلة لهذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="57bb3-149">For more information about these inspections, use the links in the first column to go to the relevant sections of this topic.</span></span> <span data-ttu-id="57bb3-150">توضح هذه المقاطع أنواع المكونات التي يوفرها التقارير الإلكترونية عمليات الفحص الخاصة بمكونات التقارير الإلكترونية وكيفيه أعاده تكوينها للمساعدة علي منع حدوث المشكلات.</span><span class="sxs-lookup"><span data-stu-id="57bb3-150">Those sections explain the types of components that ER provides inspections for and how you can reconfigure ER components to help prevent issues.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="57bb3-151">الاسم</span><span class="sxs-lookup"><span data-stu-id="57bb3-151">Name</span></span></th>
<th><span data-ttu-id="57bb3-152">‏‏الفئة</span><span class="sxs-lookup"><span data-stu-id="57bb3-152">Category</span></span></th>
<th><span data-ttu-id="57bb3-153">المستوى</span><span class="sxs-lookup"><span data-stu-id="57bb3-153">Level</span></span></th>
<th><span data-ttu-id="57bb3-154">الرسالة</span><span class="sxs-lookup"><span data-stu-id="57bb3-154">Message</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="57bb3-155"><a href='#i1'>نوع التحويل</a></span><span class="sxs-lookup"><span data-stu-id="57bb3-155"><a href='#i1'>Type conversion</a></span></span></td>
<td><span data-ttu-id="57bb3-156">إمكانية التنفيذ</span><span class="sxs-lookup"><span data-stu-id="57bb3-156">Executability</span></span></td>
<td><span data-ttu-id="57bb3-157">‏‏خطأ</span><span class="sxs-lookup"><span data-stu-id="57bb3-157">Error</span></span></td>
<td>
<p><span data-ttu-id="57bb3-158">لا يمكن تحويل التعبير من النوع &lt;type&gt;إلى حقل من نوع &lt;type&gt;.</span><span class="sxs-lookup"><span data-stu-id="57bb3-158">Cannot convert expression of type &lt;type&gt; to field of type &lt;type&gt;.</span></span></p>
<p><span data-ttu-id="57bb3-159"><b>خطأ في وقت التشغيل</b>: استثناء من نوع</span><span class="sxs-lookup"><span data-stu-id="57bb3-159"><b>Runtime error:</b> Exception for type</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="57bb3-160"><a href='#i2'>توافق النوع</a></span><span class="sxs-lookup"><span data-stu-id="57bb3-160"><a href='#i2'>Type compatibility</a></span></span></td>
<td><span data-ttu-id="57bb3-161">إمكانية التنفيذ</span><span class="sxs-lookup"><span data-stu-id="57bb3-161">Executability</span></span></td>
<td><span data-ttu-id="57bb3-162">‏‏خطأ</span><span class="sxs-lookup"><span data-stu-id="57bb3-162">Error</span></span></td>
<td>
<p><span data-ttu-id="57bb3-163">لا يمكن استخدام التعبير المكون كرابط لعنصر التنسيق الحالي إلى مصدر بيانات حيث يقوم هذا التعبير بإرجاع قيمه نوع البيانات &lt;النوع&gt; الذي يتجاوز نطاق أنواع البيانات المعتمدة من قبل عنصر التنسيق الحالي من نوع &lt;النوع&gt;.</span><span class="sxs-lookup"><span data-stu-id="57bb3-163">The configured expression cannot be used as the binding of the current format element to a data source as this expression returns value of the data type &lt;type&gt; that is beyond the scope of data types that are supported by the current format element of type &lt;type&gt;.</span></span></p>
<p><span data-ttu-id="57bb3-164"><b>خطأ في وقت التشغيل</b>: استثناء من نوع</span><span class="sxs-lookup"><span data-stu-id="57bb3-164"><b>Runtime error:</b> Exception of type</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="57bb3-165"><a href='#i3'>عنصر التكوين مفقود</a></span><span class="sxs-lookup"><span data-stu-id="57bb3-165"><a href='#i3'>Missing configuration element</a></span></span></td>
<td><span data-ttu-id="57bb3-166">إمكانية التنفيذ</span><span class="sxs-lookup"><span data-stu-id="57bb3-166">Executability</span></span></td>
<td><span data-ttu-id="57bb3-167">‏‏خطأ</span><span class="sxs-lookup"><span data-stu-id="57bb3-167">Error</span></span></td>
<td>
<p><span data-ttu-id="57bb3-168">لم يتم العثور على المسار &lt;المسار&gt;.</span><span class="sxs-lookup"><span data-stu-id="57bb3-168">Path not found &lt;path&gt;.</span></span></p>
<p><span data-ttu-id="57bb3-169"><b>خطأ في وقت التشغيل:</b> لم يتم العثور على عنصر &lt;مسار&gt; التكوين</span><span class="sxs-lookup"><span data-stu-id="57bb3-169"><b>Runtime error:</b> Element of the configuration &lt;path&gt; not found</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="57bb3-170"><a href='#i4'>إمكانية تنفيذ تعبير باستخدام وظيفة التصفية</a></span><span class="sxs-lookup"><span data-stu-id="57bb3-170"><a href='#i4'>Executability of an expression with FILTER function</a></span></span></td>
<td><span data-ttu-id="57bb3-171">إمكانية التنفيذ</span><span class="sxs-lookup"><span data-stu-id="57bb3-171">Executability</span></span></td>
<td><span data-ttu-id="57bb3-172">‏‏خطأ</span><span class="sxs-lookup"><span data-stu-id="57bb3-172">Error</span></span></td>
<td>
<p><span data-ttu-id="57bb3-173">قائمة تعبير وظيفة التصفية غير قابلة للاستعلام.</span><span class="sxs-lookup"><span data-stu-id="57bb3-173">The list expression of FILTER function is not queryable.</span></span></p>
<p><span data-ttu-id="57bb3-174"><b>خطأ في وقت التشغيل:</b> التصفية غير مدعومة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-174"><b>Runtime error:</b> Filtering is not supported.</span></span> <span data-ttu-id="57bb3-175">تحقق من صحة التكوين للحصول على مزيد من التفاصيل حول ذلك.</span><span class="sxs-lookup"><span data-stu-id="57bb3-175">Validate the configuration to get more details about this.</span></span></p>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="57bb3-176"><a href='#i5'>إمكانية تنفيذ مصدر بيانات التجميع حسب</a></span><span class="sxs-lookup"><span data-stu-id="57bb3-176"><a href='#i5'>Executability of a GROUPBY data source</a></span></span></td>
<td><span data-ttu-id="57bb3-177">إمكانية التنفيذ</span><span class="sxs-lookup"><span data-stu-id="57bb3-177">Executability</span></span></td>
<td><span data-ttu-id="57bb3-178">‏‏خطأ</span><span class="sxs-lookup"><span data-stu-id="57bb3-178">Error</span></span></td>
<td><span data-ttu-id="57bb3-179">لا يدعم المسار &lt;المسار&gt; الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="57bb3-179">Path &lt;path&gt; does not support querying.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57bb3-180">إمكانية التنفيذ</span><span class="sxs-lookup"><span data-stu-id="57bb3-180">Executability</span></span></td>
<td><span data-ttu-id="57bb3-181">‏‏خطأ</span><span class="sxs-lookup"><span data-stu-id="57bb3-181">Error</span></span></td>
<td>
<p><span data-ttu-id="57bb3-182">لا يمكن تنفيذ وظيفة "التجميع حسب" بواسطة الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="57bb3-182">Group by function cannot be executed with query.</span></span></p>
<p><span data-ttu-id="57bb3-183"><b>خطأ في وقت التشغيل:</b> لا يمكن تنفيذ وظيفة "التجميع حسب" باستخدام الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="57bb3-183"><b>Runtime error:</b> Group by function can't be executed with query.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="57bb3-184"><a href='#i6'>إمكانية تنفيذ مصدر بيانات الانضمام</a></span><span class="sxs-lookup"><span data-stu-id="57bb3-184"><a href='#i6'>Executability of a JOIN data source</a></span></span></td>
<td><span data-ttu-id="57bb3-185">إمكانية التنفيذ</span><span class="sxs-lookup"><span data-stu-id="57bb3-185">Executability</span></span></td>
<td><span data-ttu-id="57bb3-186">‏‏خطأ</span><span class="sxs-lookup"><span data-stu-id="57bb3-186">Error</span></span></td>
<td>
<p><span data-ttu-id="57bb3-187">لا يمكن الانضمام إلى &lt;مسار&gt; قائمة ليس عامل تصفية في الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="57bb3-187">Cannot join a list &lt;path&gt; that is not a filter in query.</span></span></p>
<p><span data-ttu-id="57bb3-188"><b>خطأ في وقت التشغيل:</b> يجب أن يكون مصدر البيانات المنضم للوظيفة عبارة عن حقل محسوب لتعبير عامل التصفية تم استدعاؤه بشكل غير صحيح.</span><span class="sxs-lookup"><span data-stu-id="57bb3-188"><b>Runtime error:</b> Function Joined datasource should be a filter expression calculated field has been incorrectly called.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="57bb3-189"><a href='#i7'>تفضيل وظيفة التصفية مقابل المكان</a></span><span class="sxs-lookup"><span data-stu-id="57bb3-189"><a href='#i7'>Preferability of FILTER vs WHERE function</a></span></span></td>
<td><span data-ttu-id="57bb3-190">الأداء</span><span class="sxs-lookup"><span data-stu-id="57bb3-190">Performance</span></span></td>
<td><span data-ttu-id="57bb3-191">تحذير</span><span class="sxs-lookup"><span data-stu-id="57bb3-191">Warning</span></span></td>
<td><span data-ttu-id="57bb3-192">يفضل استخدام وظيفة التصفية للتعبير عن المكان من منظور الأداء.</span><span class="sxs-lookup"><span data-stu-id="57bb3-192">Using FILTER function for the expression is preferable than WHERE from the performance perspective.</span></span> <span data-ttu-id="57bb3-193">حدد إصلاح لاستبداله تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="57bb3-193">Select Fix to replace it automatically.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57bb3-194"><a href='#i8'>تفضيل وظيفة ALLITEMSQUERY مقابل ALLITEMS</a></span><span class="sxs-lookup"><span data-stu-id="57bb3-194"><a href='#i8'>Preferability of ALLITEMSQUERY vs ALLITEMS function</a></span></span></td>
<td><span data-ttu-id="57bb3-195">الأداء</span><span class="sxs-lookup"><span data-stu-id="57bb3-195">Performance</span></span></td>
<td><span data-ttu-id="57bb3-196">تحذير</span><span class="sxs-lookup"><span data-stu-id="57bb3-196">Warning</span></span></td>
<td><span data-ttu-id="57bb3-197">يفضل استخدام وظيفة ALLITEMSQUERY للتعبير عن ALLITEMS من منظور الأداء.</span><span class="sxs-lookup"><span data-stu-id="57bb3-197">Using ALLITEMSQUERY function for the expression is preferable than ALLITEMS from the performance perspective.</span></span> <span data-ttu-id="57bb3-198">حدد إصلاح لاستبداله تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="57bb3-198">Select Fix to replace it automatically.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57bb3-199"><a href='#i9'>اعتبار حالات القائمة الفارغة</a></span><span class="sxs-lookup"><span data-stu-id="57bb3-199"><a href='#i9'>Consideration of empty list cases</a></span></span></td>
<td><span data-ttu-id="57bb3-200">إمكانية التنفيذ</span><span class="sxs-lookup"><span data-stu-id="57bb3-200">Executability</span></span></td>
<td><span data-ttu-id="57bb3-201">تحذير</span><span class="sxs-lookup"><span data-stu-id="57bb3-201">Warning</span></span></td>
<td>
<p><span data-ttu-id="57bb3-202">لا يحتوي &lt;مسار&gt; القائمة علي اي تحقق من حاله القائمة الفارغة، فقد يتسبب في حدوث خطا في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="57bb3-202">List &lt;path&gt; does not have any check for empty list case, it can result an error at run time.</span></span> <span data-ttu-id="57bb3-203">أضف فحصًا لحالة القائمة الفارغة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-203">Add a check for empty list case.</span></span></p>
<p><span data-ttu-id="57bb3-204"><b>خطأ في وقت التشغيل:</b>القائمة فارغة في &lt;المسار&gt;</span><span class="sxs-lookup"><span data-stu-id="57bb3-204"><b>Runtime error:</b> List is empty at &lt;path&gt;</span></span></p>
<p><span data-ttu-id="57bb3-205"><b><a href='#i9a'>مشكلة محتملة</a>:</b> يتم ملء الخط مرة واحدة بينما يحتوي مصدر البيانات الذي يتم ملؤه منه على سجلات متعددة</span><span class="sxs-lookup"><span data-stu-id="57bb3-205"><b><a href='#i9a'>Potential issue</a>:</b> Line is getting populated once while a data source it is populated from contains multiple records</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="57bb3-206"><a href='#i10'>إمكانية تنفيذ تعبير باستخدام وظيفة التصفية (التخزين المؤقت)</a></span><span class="sxs-lookup"><span data-stu-id="57bb3-206"><a href='#i10'>Executability of an expression with FILTER function (caching)</a></span></span></td>
<td><span data-ttu-id="57bb3-207">إمكانية التنفيذ</span><span class="sxs-lookup"><span data-stu-id="57bb3-207">Executability</span></span></td>
<td><span data-ttu-id="57bb3-208">‏‏خطأ</span><span class="sxs-lookup"><span data-stu-id="57bb3-208">Error</span></span></td>
<td>
<p><span data-ttu-id="57bb3-209">لا يمكن تطبيق وظيفة التصفية على النوع المحدد من مصدر البيانات.</span><span class="sxs-lookup"><span data-stu-id="57bb3-209">FILTER function cannot be applied to the selected type of data source.</span></span> <span data-ttu-id="57bb3-210">لا ينطبق مصدر بيانات نوع سجلات الجدول الا في حاله عدم تخزينه مؤقتا ولم يقم باضافه مصادر البيانات المتداخلة يدويا.</span><span class="sxs-lookup"><span data-stu-id="57bb3-210">A data source of the Table records type is applicable only when it is not cached and has no manually added nested data sources.</span></span></p>
<p><span data-ttu-id="57bb3-211"><b>خطأ في وقت التشغيل:</b> التصفية غير مدعومة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-211"><b>Runtime error:</b> Filtering is not supported.</span></span> <span data-ttu-id="57bb3-212">تحقق من صحة التكوين للحصول على مزيد من التفاصيل حول ذلك.</span><span class="sxs-lookup"><span data-stu-id="57bb3-212">Validate the configuration to get more details about this.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="57bb3-213"><a href='#i11'>الربط مفقود</a></span><span class="sxs-lookup"><span data-stu-id="57bb3-213"><a href='#i11'>Missing binding</a></span></span></td>
<td><span data-ttu-id="57bb3-214">إمكانية التنفيذ</span><span class="sxs-lookup"><span data-stu-id="57bb3-214">Executability</span></span></td>
<td><span data-ttu-id="57bb3-215">تحذير</span><span class="sxs-lookup"><span data-stu-id="57bb3-215">Warning</span></span></td>
<td>
<p><span data-ttu-id="57bb3-216">لا يحتوي المسار &lt;المسار&gt; على اي ربط بأي مصدر بيانات باستخدام تعيين النموذج.</span><span class="sxs-lookup"><span data-stu-id="57bb3-216">Path &lt;path&gt; has no binding to any datasource in using model's mapping.</span></span></p>
<p><span data-ttu-id="57bb3-217"><b>خطأ في وقت التشغيل:</b> لم يتم العثور على المسار &lt;المسار&gt;</span><span class="sxs-lookup"><span data-stu-id="57bb3-217"><b>Runtime error:</b> Path &lt;path&gt; is not bound</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="57bb3-218"><a href='#i12'>قالب غير مرتبط</a></span><span class="sxs-lookup"><span data-stu-id="57bb3-218"><a href='#i12'>Not linked template</a></span></span></td>
<td><span data-ttu-id="57bb3-219">تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="57bb3-219">Data integrity</span></span></td>
<td><span data-ttu-id="57bb3-220">تحذير</span><span class="sxs-lookup"><span data-stu-id="57bb3-220">Warning</span></span></td>
<td><span data-ttu-id="57bb3-221">&lt;اسم&gt; الملف غير مرتبط بأي مكونات ملف وستتم ازالته بعد تغيير حاله إصدار التكوين.</span><span class="sxs-lookup"><span data-stu-id="57bb3-221">File &lt;name&gt; is linked to no file components and will be removed after changing status of configuration version.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57bb3-222"><a href='#i13'>تنسيق غير متزامن</a></span><span class="sxs-lookup"><span data-stu-id="57bb3-222"><a href='#i13'>Not synced format</a></span></span></td>
<td><span data-ttu-id="57bb3-223">تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="57bb3-223">Data integrity</span></span></td>
<td><span data-ttu-id="57bb3-224">تحذير</span><span class="sxs-lookup"><span data-stu-id="57bb3-224">Warning</span></span></td>
<td><span data-ttu-id="57bb3-225">الاسم المحدد &lt;اسن المكون&gt; غير موجود في ورقه عمل Excel &lt;اسم الورقة&gt;</span><span class="sxs-lookup"><span data-stu-id="57bb3-225">Defined name &lt;component name&gt; does not exist in Excel sheet &lt;sheet name&gt;</span></span></td>
</tr>
</tbody>
</table>

## <a name="type-conversion"></a><a id="i1"></a><span data-ttu-id="57bb3-226">نوع التحويل</span><span class="sxs-lookup"><span data-stu-id="57bb3-226">Type conversion</span></span>

<span data-ttu-id="57bb3-227">يقوم التقارير الإلكترونية بالتحقق مما إذا كان نوع بيانات حقل نموذج البيانات متوافقا مع نوع البيانات لتعبير تم تكوينه كرابط لهذا الحقل.</span><span class="sxs-lookup"><span data-stu-id="57bb3-227">ER checks whether the data type of a data model field is compatible with the data type of an expression that is configured as the binding of that field.</span></span> <span data-ttu-id="57bb3-228">في حاله عدم توافق أنواع البيانات، يحدث خطا في التحقق من الصحة في مصمم تعيين نموذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="57bb3-228">If the data types are incompatible, a validation error occurs in the ER model-mapping designer.</span></span> <span data-ttu-id="57bb3-229">تنص الرسالة التي تلقيتها علي انه لا يمكن للتقارير الإلكترونية تحويل تعبير من نوع A إلى حقل من النوع B.</span><span class="sxs-lookup"><span data-stu-id="57bb3-229">The message that you receive states that ER can't convert an expression of type A to a field of type B.</span></span>

<span data-ttu-id="57bb3-230">توضح الخطوات التالية كيفيه حدوث هذه المشكلة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-230">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="57bb3-231">أبدا في تكوين نموذج البيانات الخاص ب التقارير الإلكترونية ومكونات تعيين نموذج التقارير الإلكترونية في نفس الوقت.</span><span class="sxs-lookup"><span data-stu-id="57bb3-231">Start to configure the ER data model and the ER model-mapping components simultaneously.</span></span>
2. <span data-ttu-id="57bb3-232">في شجره نموذج البيانات، قم باضافه حقل يسمي **X** وحدد **عدد صحيح** كنوع البيانات.</span><span class="sxs-lookup"><span data-stu-id="57bb3-232">In the data model tree, add a field that is named **X**, and select **Integer** as the data type.</span></span>

    ![الحقل X ونوع البيانات الصحيح الذي تمت اضافته إلى شجره وضع البيانات في صفحه نموذج البيانات](./media/er-components-inspections-01.png)

3. <span data-ttu-id="57bb3-234">في جزء مصادر بيانات تعيين النموذج، أضف مصدر بيانات من نوع **الحقل المحسوب**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-234">In the model-mapping data sources pane, add a data source of the **Calculated field** type.</span></span>
4. <span data-ttu-id="57bb3-235">قم بتسميه مصدر البيانات الجديد **Y**، وقم بتكوينه بحيث يحتوي علي التعبير `INTVALUE(100)`.</span><span class="sxs-lookup"><span data-stu-id="57bb3-235">Name the new data source **Y**, and configure it so that it contains the expression `INTVALUE(100)`.</span></span>
5. <span data-ttu-id="57bb3-236">اربط **X** بـ **Y**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-236">Bind **X** to **Y**.</span></span>
6. <span data-ttu-id="57bb3-237">في مصمم نموذج البيانات، قم بتغيير نوع البيانات للحقل **X** من **العدد الصحيح** إلى **Int64**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-237">In the data model designer, change the data type of the **X** field from **Integer** to **Int64**.</span></span>
7. <span data-ttu-id="57bb3-238">حدد **التحقق من الصحة** لفحص مكون تعيين النموذج القابل للتحرير في صفحه **مصمم تعيين النموذج**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-238">Select **Validate** to inspect the editable model-mapping component on the **Model mapping designer** page.</span></span>

    ![التحقق من صحة مكون تعيين النموذج القابل للتحرير في صفحه مصمم تعيين النموذج.](./media/er-components-inspections-01.gif)

8. <span data-ttu-id="57bb3-240">حدد **التحقق من الصحة** لفحص مكون تعيين النموذج الخاص بتكوين التقارير الإلكترونية المحدد على صفحة **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-240">Select **Validate** to inspect the model-mapping component of the selected ER configuration on the **Configurations** page.</span></span>

    ![تحقق من الصحة لفحص مكون تعيين النموذج في صفحه التكوينات](./media/er-components-inspections-01a.png)

9. <span data-ttu-id="57bb3-242">لاحظ حدوث خطا في التحقق من الصحة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-242">Notice that a validation error occurs.</span></span> <span data-ttu-id="57bb3-243">وتوضح الرسالة أن قيمه نوع **العدد الصحيح** التي يرجع إليها تعبير `INTVALUE(100)` لمصدر البيانات **Y** لا يمكن تخزينها في حقل نموذج البيانات **X** لنوع **Int64**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-243">The message states that the value of the **Integer** type that the `INTVALUE(100)` expression of the **Y** data source returns can't be stored in the **X** data model field of the **Int64** type.</span></span>

<span data-ttu-id="57bb3-244">يبين الرسم التوضيحي التالي خطا وقت التشغيل الذي يحدث إذا تجاهلت التحذير وحدد **تشغيل** لتشغيل تنسيق مكون لاستخدام تعيين النموذج.</span><span class="sxs-lookup"><span data-stu-id="57bb3-244">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run a format that is configured to use the model-mapping.</span></span>

![أخطاء وقت التشغيل في صفحة مصمم التنسيق](./media/er-components-inspections-01b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="57bb3-246">الحل التلقائي</span><span class="sxs-lookup"><span data-stu-id="57bb3-246">Automatic resolution</span></span>

<span data-ttu-id="57bb3-247">لا يتوفر اي خيار لإصلاح هذه المشكلة تلقائيا.</span><span class="sxs-lookup"><span data-stu-id="57bb3-247">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="57bb3-248">الحل اليدوي</span><span class="sxs-lookup"><span data-stu-id="57bb3-248">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="57bb3-249">خيار 1</span><span class="sxs-lookup"><span data-stu-id="57bb3-249">Option 1</span></span>

<span data-ttu-id="57bb3-250">يجب تحديث بنيه نموذج البيانات عن طريق تغيير نوع بيانات حقل نموذج البيانات بحيث يطابق نوع البيانات الخاص بالتعبير الذي تم تكوينه للربط الخاص بهذا الحقل.</span><span class="sxs-lookup"><span data-stu-id="57bb3-250">Update the data model structure by changing the data type of the data model field so that it matches the data type of the expression that is configured for the binding of that field.</span></span> <span data-ttu-id="57bb3-251">بالنسبة للمثال السابق، يجب ان يتم تغيير نوع بيانات حقل **X** مرة أخرى إلى **عدد صحيح**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-251">For the preceding example, the data type of the **X** field must be changed back to **Integer**.</span></span>

#### <a name="option-2"></a><span data-ttu-id="57bb3-252">خيار 2</span><span class="sxs-lookup"><span data-stu-id="57bb3-252">Option 2</span></span>

<span data-ttu-id="57bb3-253">تحديث تعيين النموذج من خلال تغيير تعبير مصدر البيانات المرتبط بحقل نموذج البيانات.</span><span class="sxs-lookup"><span data-stu-id="57bb3-253">Update the model-mapping by changing the expression of the data source that is bound with the data model field.</span></span> <span data-ttu-id="57bb3-254">بالنسبة للمثال السابق، يجب تغيير تعبير مصدر البيانات **Y** إلى `INT64VALUE(100)`.</span><span class="sxs-lookup"><span data-stu-id="57bb3-254">For the preceding example, the expression of the **Y** data source must be changed to `INT64VALUE(100)`.</span></span>

## <a name="type-compatibility"></a><a id="i2"></a><span data-ttu-id="57bb3-255">توافق النوع</span><span class="sxs-lookup"><span data-stu-id="57bb3-255">Type compatibility</span></span>

<span data-ttu-id="57bb3-256">يتحقق التقارير الإلكترونية مما إذا كان نوع البيانات لعنصر التنسيق متوافقًا مع نوع بيانات التعبير الذي تم تكوينه كربط لعنصر التنسيق هذا.</span><span class="sxs-lookup"><span data-stu-id="57bb3-256">ER checks whether the data type of a format element is compatible with the data type of an expression that is configured as the binding of that format element.</span></span> <span data-ttu-id="57bb3-257">إذا كانت أنواع البيانات غير متوافقة، فسيحدث خطأ في التحقق من الصحة في مصمم عمليات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="57bb3-257">If the data types are incompatible, a validation error occurs in the ER Operations designer.</span></span> <span data-ttu-id="57bb3-258">تنص الرسالة التي تتلقاها على أنه لا يمكن استخدام التعبير المكون كربط لعنصر التنسيق الحالي بمصدر بيانات، لأن التعبير يُرجع قيمة من نوع البيانات A خارج نطاق أنواع البيانات المدعومة بواسطة عنصر التنسيق الحالي من النوع B.</span><span class="sxs-lookup"><span data-stu-id="57bb3-258">The message that you receive states that the configured expression can't be used as the binding of the current format element to a data source, because the expression returns a value of data type A that is beyond the scope of the data types that are supported by the current format element of type B.</span></span>

<span data-ttu-id="57bb3-259">توضح الخطوات التالية كيفيه حدوث هذه المشكلة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-259">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="57bb3-260">ابدأ في تكوين نموذج بيانات التقارير الإلكترونية ومكونات تنسيق التقارير الإلكترونية في وقت واحد.</span><span class="sxs-lookup"><span data-stu-id="57bb3-260">Start to configure the ER data model and the ER format components simultaneously.</span></span>
2. <span data-ttu-id="57bb3-261">في شجره نموذج البيانات، قم باضافه حقل يسمي **X** وحدد **عدد صحيح** كنوع البيانات.</span><span class="sxs-lookup"><span data-stu-id="57bb3-261">In the data model tree, add a field that is named **X**, and select **Integer** as the data type.</span></span>
3. <span data-ttu-id="57bb3-262">في شجره بنية التنسيق، أضف عنصر تنسيق من النوع **العددي**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-262">In the format structure tree, add a format element of the **Numeric** type.</span></span>
4. <span data-ttu-id="57bb3-263">قم بتسمية عنصر التنسيق الجديد **Y**. في حقل **النوع الرقمي**، حدد **عدد صحيح** كنوع البيانات.</span><span class="sxs-lookup"><span data-stu-id="57bb3-263">Name the new format element **Y**. In the **Numeric type** field, select **Integer** as the data type.</span></span>
5. <span data-ttu-id="57bb3-264">اربط **X** بـ **Y**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-264">Bind **X** to **Y**.</span></span>
6. <span data-ttu-id="57bb3-265">في شجره بنيه التنسيق، قم بتغيير نوع البيانات الخاص بعنصر التنسيق **Y** من **العدد الصحيح** إلى **Int64**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-265">In the format structure tree, change the data type of the **Y** format element from **Integer** to **Int64**.</span></span>
7. <span data-ttu-id="57bb3-266">حدد **التحقق من الصحة** لفحص مكون التنسيق القابل للتحرير في صفحة **مصمم التنسيق**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-266">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![التحقق من توافق النوع علي صفحه مصمم التنسيق](./media/er-components-inspections-02.gif)

8. <span data-ttu-id="57bb3-268">لاحظ حدوث خطا في التحقق من الصحة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-268">Notice that a validation error occurs.</span></span> <span data-ttu-id="57bb3-269">وتوضح الرسالة ان التعبير المكون يمكنه قبول قيم **Int64** فقط.</span><span class="sxs-lookup"><span data-stu-id="57bb3-269">The message states that the configured expression can accept only **Int64** values.</span></span> <span data-ttu-id="57bb3-270">لذلك، لا يمكن إدخال قيمه حقل نموذج بيانات **X** الخاص بنوع **العدد الصحيح** في عنصر التنسيق **Y**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-270">Therefore, the value of the **X** data model field of the **Integer** type can't be entered in the **Y** format element.</span></span>

### <a name="automatic-resolution"></a><span data-ttu-id="57bb3-271">الحل التلقائي</span><span class="sxs-lookup"><span data-stu-id="57bb3-271">Automatic resolution</span></span>

<span data-ttu-id="57bb3-272">لا يتوفر اي خيار لإصلاح هذه المشكلة تلقائيا.</span><span class="sxs-lookup"><span data-stu-id="57bb3-272">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="57bb3-273">الحل اليدوي</span><span class="sxs-lookup"><span data-stu-id="57bb3-273">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="57bb3-274">خيار 1</span><span class="sxs-lookup"><span data-stu-id="57bb3-274">Option 1</span></span>

<span data-ttu-id="57bb3-275">قم بتحديث بنية التنسيق عن طريق تغيير نوع البيانات الخاص بعنصر التنسيق **العددي** بحيث يطابق نوع بيانات التعبير الذي تم تكوينه لربط هذا العنصر.</span><span class="sxs-lookup"><span data-stu-id="57bb3-275">Update the format structure by changing the data type of the **Numeric** format element so that it matches the data type of the expression that you configured for the binding of that element.</span></span> <span data-ttu-id="57bb3-276">في المثال السابق، يجب تغيير قيمة **النوع العددي** الخاص بعنصر التنسيق **X** مرة أخرى إلى **العدد الصحيح**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-276">In the preceding example, the **Numeric type** value of the **X** format element must be changed back to **Integer**.</span></span>

#### <a name="option-2"></a><span data-ttu-id="57bb3-277">خيار 2</span><span class="sxs-lookup"><span data-stu-id="57bb3-277">Option 2</span></span>

<span data-ttu-id="57bb3-278">قم بتحديث تعيين التنسيق الخاص بعنصر التنسيق **X** من خلال تغيير التعبير من `model.X` إلى `INT64VALUE(model.X)`.</span><span class="sxs-lookup"><span data-stu-id="57bb3-278">Update the format mapping of the **X** format element by changing the expression from `model.X` to `INT64VALUE(model.X)`.</span></span>

## <a name="missing-configuration-element"></a><a id="i3"></a><span data-ttu-id="57bb3-279">عنصر التكوين مفقود</span><span class="sxs-lookup"><span data-stu-id="57bb3-279">Missing configuration element</span></span>

<span data-ttu-id="57bb3-280">يقوم التقارير الإلكترونية بالتحقق مما إذا كانت تعبيرات الربط تحتوي علي مصادر البيانات التي تم تكوينها في مكونات التقارير الإلكترونية القابلة للتحرير ام لا.</span><span class="sxs-lookup"><span data-stu-id="57bb3-280">ER checks whether the binding expressions contain only data sources that are configured in the editable ER component.</span></span> <span data-ttu-id="57bb3-281">لكل ربط يحتوي علي مصدر بيانات مفقود في مكونات التقارير الإلكترونية القابلة للتحرير، يحدث خطا في التحقق من الصحة في "مصمم العمليات" الخاص ب التقارير الإلكترونية أو مصمم تعيين نموذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="57bb3-281">For every binding that contains a data source that is missing in the editable ER component, a validation error occurs in the ER Operations designer or the ER model-mapping designer.</span></span>

<span data-ttu-id="57bb3-282">توضح الخطوات التالية كيفيه حدوث هذه المشكلة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-282">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="57bb3-283">أبدا في تكوين نموذج البيانات الخاص ب التقارير الإلكترونية ومكونات تعيين نموذج التقارير الإلكترونية في نفس الوقت.</span><span class="sxs-lookup"><span data-stu-id="57bb3-283">Start to configure the ER data model and the ER model-mapping components simultaneously.</span></span>
2. <span data-ttu-id="57bb3-284">في شجره نموذج البيانات، قم باضافه حقل يسمي **X** وحدد **عدد صحيح** كنوع البيانات.</span><span class="sxs-lookup"><span data-stu-id="57bb3-284">In the data model tree, add a field that is named **X**, and select **Integer** as the data type.</span></span>

    ![شجرة نموذج البيانات مع حقل X ونوع بيانات عدد صحيح في صفحة نموذج البيانات](./media/er-components-inspections-01.png)

3. <span data-ttu-id="57bb3-286">في جزء مصادر بيانات تعيين النموذج، أضف مصدر بيانات من نوع **الحقل المحسوب**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-286">In the model-mapping data sources pane, add a data source of the **Calculated field** type.</span></span>
4. <span data-ttu-id="57bb3-287">قم بتسميه مصدر البيانات الجديد **Y**، وقم بتكوينه بحيث يحتوي علي التعبير `INTVALUE(100)`.</span><span class="sxs-lookup"><span data-stu-id="57bb3-287">Name the new data source **Y**, and configure it so that it contains the expression `INTVALUE(100)`.</span></span>
5. <span data-ttu-id="57bb3-288">اربط **X** بـ **Y**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-288">Bind **X** to **Y**.</span></span>
6. <span data-ttu-id="57bb3-289">في مصمم تعيين النموذج، في جزء مصادر البيانات، احذف مصدر بيانات **Y**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-289">In the model-mapping designer, in the data sources pane, delete the **Y** data source.</span></span>
7. <span data-ttu-id="57bb3-290">حدد **التحقق من الصحة** لفحص مكون تعيين النموذج القابل للتحرير في صفحه **مصمم تعيين النموذج**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-290">Select **Validate** to inspect the editable model-mapping component on the **Model mapping designer** page.</span></span>

    ![افحص مكون تعيين نموذج التقارير الإلكترونية القابل للتحرير في صفحة مصمم خرائط النموذج](./media/er-components-inspections-03.gif)

8. <span data-ttu-id="57bb3-292">لاحظ حدوث خطا في التحقق من الصحة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-292">Notice that a validation error occurs.</span></span> <span data-ttu-id="57bb3-293">وتوضح الرسالة أن ربط حقل نموذج البيانات **X** يحتوي على المسار الذي يشير إلى مصدر بيانات **Y**، ولكن لم يتم العثور على مصدر البيانات هذا.</span><span class="sxs-lookup"><span data-stu-id="57bb3-293">The message states that the binding of the **X** data model field contains the path that refers to the **Y** data source, but this data source isn't found.</span></span>

### <a name="automatic-resolution"></a><span data-ttu-id="57bb3-294">الحل التلقائي</span><span class="sxs-lookup"><span data-stu-id="57bb3-294">Automatic resolution</span></span>

<span data-ttu-id="57bb3-295">حدد **إلغاء الربط** لحل هذه المشكلة تلقائيا عن طريق أزاله ربط مصدر البيانات المفقود.</span><span class="sxs-lookup"><span data-stu-id="57bb3-295">Select **Unbind** to automatically fix this issue by removing the missing data source binding.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="57bb3-296">الحل اليدوي</span><span class="sxs-lookup"><span data-stu-id="57bb3-296">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="57bb3-297">خيار 1</span><span class="sxs-lookup"><span data-stu-id="57bb3-297">Option 1</span></span>

<span data-ttu-id="57bb3-298">قم بإلغاء ربط حقل نموذج البيانات **X** لإيقاف الإشارة إلى مصدر بيانات **Y** غير الموجود.</span><span class="sxs-lookup"><span data-stu-id="57bb3-298">Unbind the **X** data model field to stop referring to the nonexistent **Y** data source.</span></span>

#### <a name="option-2"></a><span data-ttu-id="57bb3-299">خيار 2</span><span class="sxs-lookup"><span data-stu-id="57bb3-299">Option 2</span></span>

<span data-ttu-id="57bb3-300">في جزء مصادر البيانات لمصمم تعيين نموذج التقارير الإلكترونية، أضف مصدر بيانات **Y** مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="57bb3-300">In the data sources pane of the ER model-mapping designer, add the **Y** data source again.</span></span>

## <a name="executability-of-an-expression-with-filter-function"></a><a id="i4"></a><span data-ttu-id="57bb3-301">إمكانية تنفيذ تعبير باستخدام وظيفة التصفية</span><span class="sxs-lookup"><span data-stu-id="57bb3-301">Executability of an expression with FILTER function</span></span>

<span data-ttu-id="57bb3-302">يتم استخدام وظيفة [تصفية](er-functions-list-filter.md) التقارير الإلكترونية المضمنة للوصول إلى جداول التطبيق أو طرق العرض أو كيانات البيانات عن طريق وضع استدعاء SQL مفرد للحصول علي البيانات المطلوبة كقائمه سجلات.</span><span class="sxs-lookup"><span data-stu-id="57bb3-302">The built-in [FILTER](er-functions-list-filter.md) ER function is used to access application tables, views, or data entities by placing a single SQL call to get the required data as a list of records.</span></span> <span data-ttu-id="57bb3-303">يتم استخدام مصدر بيانات من نوع **قائمة السجلات** كوسيطة لهذه الوظيفة ويحدد مصدر التطبيق الخاص بالاستدعاء.</span><span class="sxs-lookup"><span data-stu-id="57bb3-303">A data source of the **Record list** type is used as an argument of this function and specifies the application source for the call.</span></span> <span data-ttu-id="57bb3-304">يقوم التقارير الإلكترونية بالتحقق مما إذا كان من الممكن إنشاء استعلام SQL مباشر إلى مصدر بيانات يشار إليه في وظيفة `FILTER` أو لا.</span><span class="sxs-lookup"><span data-stu-id="57bb3-304">ER checks whether a direct SQL query can be established to a data source that is referred to in the `FILTER` function.</span></span> <span data-ttu-id="57bb3-305">في حاله تعذر إنشاء الاستعلام المباشر، يحدث خطا في التحقق من الصحة في مصمم تعيين نموذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="57bb3-305">If a direct query can't be established, a validation error occurs in the ER model-mapping designer.</span></span> <span data-ttu-id="57bb3-306">توضح الرسالة التي تتلقاها ان تعبير التقارير الإلكترونية الذي يتضمن وظيفة `FILTER` لا يمكن تشغيله في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="57bb3-306">The message that you receive states that the ER expression that includes the `FILTER` function can't be run at runtime.</span></span> 

<span data-ttu-id="57bb3-307">توضح الخطوات التالية كيفيه حدوث هذه المشكلة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-307">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="57bb3-308">ابدأ بتكوين مكون تعيين نموذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="57bb3-308">Start to configure the ER model-mapping component.</span></span>
2. <span data-ttu-id="57bb3-309">أضف مصدر بيانات من نوع **Dynamics 365 for Operations \\ سجلات الجداول**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-309">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="57bb3-310">قم بتسمية مصدر البيانات الجديد **المورد**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-310">Name the new data source **Vendor**.</span></span> <span data-ttu-id="57bb3-311">في حقل **الجدول**، حدد **VendTable** لتحديد أن مصدر البيانات سيطلب الجدول VendTable.</span><span class="sxs-lookup"><span data-stu-id="57bb3-311">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
4. <span data-ttu-id="57bb3-312">أضف مصدر بيانات من نوع **الحقل المحسوب**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-312">Add a data source of the **Calculated field** type.</span></span>
5. <span data-ttu-id="57bb3-313">قم بتسميه مصدر البيانات الجديد **FilteredVendor**، وقم بتكوينه بحيث يحتوي علي التعبير `FILTER(Vendor, Vendor.AccountNum="US-101")`.</span><span class="sxs-lookup"><span data-stu-id="57bb3-313">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, Vendor.AccountNum="US-101")`.</span></span>
6. <span data-ttu-id="57bb3-314">حدد **التحقق من الصحة** لفحص مكون تعيين النموذج القابل للتحرير علي صفحة **مصمم تعيين النموذج** والتحقق من إمكانية الاستعلام عن تعبير `FILTER(Vendor, Vendor.AccountNum="US-101")` في مصدر بيانات **المورد**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-314">Select **Validate** to inspect the editable model-mapping component on the **Model mapping designer** page and verify that the `FILTER(Vendor, Vendor.AccountNum="US-101")` expression in the **Vendor** data source can be queried.</span></span>
7. <span data-ttu-id="57bb3-315">قم بتعديل مصدر بيانات **المورد** عن طريق أضافه حقل متداخل لـ **نوع الحقل المحسوب** للحصول علي رقم حساب المورد الذي تم اقتطاعه.</span><span class="sxs-lookup"><span data-stu-id="57bb3-315">Modify the **Vendor** data source by adding a nested field of the **Calculated field** type to get the trimmed vendor account number.</span></span>
8. <span data-ttu-id="57bb3-316">قم بتسميه الحقل المتداخل الجديد **$AccNumber**، وقم بتكوينه بحيث يحتوي علي التعبير `TRIM(Vendor.AccountNum)`.</span><span class="sxs-lookup"><span data-stu-id="57bb3-316">Name the new nested field **$AccNumber**, and configure it so that it contains the expression `TRIM(Vendor.AccountNum)`.</span></span>
9. <span data-ttu-id="57bb3-317">حدد **التحقق من الصحة** لفحص مكون تعيين النموذج القابل للتحرير علي صفحة **مصمم تعيين النموذج** والتحقق من إمكانية الاستعلام عن تعبير `FILTER(Vendor, Vendor.AccountNum="US-101")` في مصدر بيانات **المورد**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-317">Select **Validate** to inspect the editable model-mapping component on the **Model mapping designer** page and verify that the `FILTER(Vendor, Vendor.AccountNum="US-101")` expression in the **Vendor** data source can be queried.</span></span>

    ![التحقق من امكانيه الاستعلام عن التعبير في صفحه مصمم تعيين النموذج](./media/er-components-inspections-04.gif)

10. <span data-ttu-id="57bb3-319">لاحظ حدوث خطا في التحقق من الصحة، نظرا لان مصدر بيانات **المورد** يحتوي علي حقل متداخل من نوع **الحقل المحسوب** الذي لا يسمح بترجمة تعبير مصدر البيانات **FilteredVendor** إلى عبارة SQL المباشرة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-319">Notice that a validation error occurs, because the **Vendor** data source contains a nested field of the **Calculated field** type that doesn't allow the expression of the **FilteredVendor** data source to be translated to the direct SQL statement.</span></span>

<span data-ttu-id="57bb3-320">يبين الرسم التوضيحي التالي خطا وقت التشغيل الذي يحدث إذا تجاهلت التحذير وحدد **تشغيل** لتشغيل تنسيق مكون لاستخدام تعيين النموذج.</span><span class="sxs-lookup"><span data-stu-id="57bb3-320">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run a format that is configured to use the model-mapping.</span></span>

![أخطاء وقت التشغيل التي تحدث عند تشغيل التنسيق القابل للتحرير علي صفحه مصمم التنسيق](./media/er-components-inspections-04a.png)

### <a name="automatic-resolution"></a><span data-ttu-id="57bb3-322">الحل التلقائي</span><span class="sxs-lookup"><span data-stu-id="57bb3-322">Automatic resolution</span></span>

<span data-ttu-id="57bb3-323">لا يتوفر اي خيار لإصلاح هذه المشكلة تلقائيا.</span><span class="sxs-lookup"><span data-stu-id="57bb3-323">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="57bb3-324">الحل اليدوي</span><span class="sxs-lookup"><span data-stu-id="57bb3-324">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="57bb3-325">خيار 1</span><span class="sxs-lookup"><span data-stu-id="57bb3-325">Option 1</span></span>

<span data-ttu-id="57bb3-326">بدلا من أضافه حقل متداخل من نوع **الحقل المحسوب** إلى مصدر بيانات **المورد**، قم باضافه الحقل المتداخل **$AccNumber** إلى مصدر بيانات **FilteredVendor**، وقم بتكوينه بحيث يحتوي على التعبير `TRIM(FilteredVendor.AccountNum)`.</span><span class="sxs-lookup"><span data-stu-id="57bb3-326">Instead of adding a nested field of the **Calculated field** type to the **Vendor** data source, add the **$AccNumber** nested field to the **FilteredVendor** data source, and configure it so that it contains the expression `TRIM(FilteredVendor.AccountNum)`.</span></span> <span data-ttu-id="57bb3-327">وبهذه الطريقة، يمكن تشغيل التعبير `FILTER(Vendor, Vendor.AccountNum="US-101")` في مستوي SQL وحساب الحقل المتداخل **$AccNumber** بعد ذلك.</span><span class="sxs-lookup"><span data-stu-id="57bb3-327">In this way, the `FILTER(Vendor, Vendor.AccountNum="US-101")` expression can be run at the SQL level and calculate the **$AccNumber** nested field afterward.</span></span>

#### <a name="option-2"></a><span data-ttu-id="57bb3-328">خيار 2</span><span class="sxs-lookup"><span data-stu-id="57bb3-328">Option 2</span></span>

<span data-ttu-id="57bb3-329">قم بتغيير التعبير الخاص بمصدر بيانات **FilteredVendor** من `FILTER(Vendor, Vendor.AccountNum="US-101")`إلى `WHERE(Vendor, Vendor.AccountNum="US-101")`.</span><span class="sxs-lookup"><span data-stu-id="57bb3-329">Change the expression of the **FilteredVendor** data source from `FILTER(Vendor, Vendor.AccountNum="US-101")` to `WHERE(Vendor, Vendor.AccountNum="US-101")`.</span></span> <span data-ttu-id="57bb3-330">لا نوصي بتغيير التعبير الخاص بأحد الجداول الذي يحتوي علي حجم كبير من البيانات (جدول المعاملات)، وذلك لأنه سيتم إحضار كافة السجلات، سيتم اجراء تحديد السجلات المطلوبة في الذاكرة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-330">We don't recommend that you change the expression for a table that has a large volume of data (transactional table), because all records will be fetched, and selection of the required records will be done in memory.</span></span> <span data-ttu-id="57bb3-331">لذلك، يمكن ان يتسبب هذا الأسلوب في ضعف الأداء.</span><span class="sxs-lookup"><span data-stu-id="57bb3-331">Therefore, this approach can cause poor performance.</span></span> <span data-ttu-id="57bb3-332">لمزيد من المعلومات، راجع [وظيفة التقارير الإلكترونية للمكان](er-functions-list-where.md).</span><span class="sxs-lookup"><span data-stu-id="57bb3-332">For more information, see [WHERE ER function](er-functions-list-where.md).</span></span>

## <a name="executability-of-a-groupby-data-source"></a><a id="i5"></a><span data-ttu-id="57bb3-333">إمكانية تنفيذ مصدر بيانات التجميع حسب</span><span class="sxs-lookup"><span data-stu-id="57bb3-333">Executability of a GROUPBY data source</span></span>

<span data-ttu-id="57bb3-334">يقسم مصدر البيانات **التجميع حسب** نتيجة الاستعلام إلى مجموعات من السجلات، عاده لغرض اجراء تجميع واحد أو أكثر في كل مجموعه.</span><span class="sxs-lookup"><span data-stu-id="57bb3-334">The **GROUPBY** data source divides the query result into groups of records, usually for the purpose of doing one or more aggregations on each group.</span></span> <span data-ttu-id="57bb3-335">يمكن تكوين كل مصدر بيانات **التجميع حسب** بحيث يتم تشغيله اما في مستوي قاعده البيانات أو في الذاكرة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-335">Every **GROUPBY** data source can be configured so that it's run either at the database level or in memory.</span></span> <span data-ttu-id="57bb3-336">عند تكوين مصدر بيانات **التجميع حسب** بحيث يتم تشغيله علي مستوي قاعده البيانات، تقوم التقارير الإلكترونية بالتحقق مما إذا كان من الممكن تاسيس استعلام SQL مباشر إلى مصدر بيانات يتم الاشاره اليه في مصدر البيانات هذا أو لا.</span><span class="sxs-lookup"><span data-stu-id="57bb3-336">When a **GROUPBY** data source is configured so that it's run at the database level, ER checks whether a direct SQL query can be established to a data source that is referred to in that data source.</span></span> <span data-ttu-id="57bb3-337">في حاله تعذر إنشاء الاستعلام المباشر، يحدث خطا في التحقق من الصحة في مصمم تعيين نموذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="57bb3-337">If a direct query can't be established, a validation error occurs in the ER model-mapping designer.</span></span> <span data-ttu-id="57bb3-338">توضح الرسالة التي تتلقاها انه لا يمكن تشغيل مصدر بيانات **التجميع حسب** المكون في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="57bb3-338">The message that you receive states that the configured **GROUPBY** data source can't be run at runtime.</span></span>

<span data-ttu-id="57bb3-339">توضح الخطوات التالية كيفيه حدوث هذه المشكلة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-339">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="57bb3-340">ابدأ بتكوين مكون تعيين نموذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="57bb3-340">Start to configure the ER model-mapping component.</span></span>
2. <span data-ttu-id="57bb3-341">أضف مصدر بيانات من نوع **Dynamics 365 for Operations \\ سجلات الجداول**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-341">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="57bb3-342">قم بتسمية مصدر البيانات الجديد **Trans**. في حقل **الجدول**، حدد **VendTrans** لتحديد أن مصدر البيانات هذا سيطلب جدول VendTrans.</span><span class="sxs-lookup"><span data-stu-id="57bb3-342">Name the new data source **Trans**. In the **Table** field, select **VendTrans** to specify that this data source will request the VendTrans table.</span></span>
4. <span data-ttu-id="57bb3-343">أضف مصدر بيانات من نوع **التجميع حسب**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-343">Add a data source of the **Group by** type.</span></span>
5. <span data-ttu-id="57bb3-344">قم بتسميه مصدر البيانات الجديد **GroupedTrans**، ثم قم بتكوينه بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="57bb3-344">Name the new data source **GroupedTrans**, and configure it in the following way:</span></span>

    - <span data-ttu-id="57bb3-345">حدد مصدر بيانات **الحركة** كمصدر للسجلات التي يجب تجميعها.</span><span class="sxs-lookup"><span data-stu-id="57bb3-345">Select the **Trans** data source as the source of records that should be grouped.</span></span>
    - <span data-ttu-id="57bb3-346">في حقل **موقع التنفيذ**، حدد **استعلام** لتحديد انك تريد تشغيل مصدر البيانات هذا على مستوي قاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="57bb3-346">In the **Execution location** field, select **Query** to specify that you want to run this data source at the database level.</span></span>

    ![تكوين مصدر البيانات على صفحه تحرير معلمات "التجميع حسب"](./media/er-components-inspections-05a.gif)

6. <span data-ttu-id="57bb3-348">حدد **التحقق من الصحة** لفحص مكون تعيين النموذج القابل للتحرير على صفحة **مصمم تعيين النموذج** وتحقق من إمكانية الاستعلام عن مصدر بيانات **GroupedTrans**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-348">Select **Validate** to inspect the editable model-mapping component on the **Model mapping designer** page and verify that the configured **GroupedTrans** data source can be queried.</span></span>
7. <span data-ttu-id="57bb3-349">قم بتعديل مصدر بيانات **الحركة** عن طريق أضافه حقل متداخل **لنوع الحقل المحسوب** للحصول علي رقم حساب المورد الذي تم اقتطاعه.</span><span class="sxs-lookup"><span data-stu-id="57bb3-349">Modify the **Trans** data source by adding a nested field of the **Calculated field** type to get the trimmed vendor account number.</span></span>
8. <span data-ttu-id="57bb3-350">قم بتسميه مصدر البيانات الجديد **$AccNumber**، وقم بتكوينه بحيث يحتوي علي التعبير `TRIM(Trans.AccountNum)`.</span><span class="sxs-lookup"><span data-stu-id="57bb3-350">Name the new data source **$AccNumber**, and configure it so that it contains the expression `TRIM(Trans.AccountNum)`.</span></span>

    ![تكوين مصدر البيانات في صفحة مصمم تعيين النموذج](./media/er-components-inspections-05a.png)

9. <span data-ttu-id="57bb3-352">حدد **التحقق من الصحة** لفحص مكون تعيين النموذج القابل للتحرير على صفحة **مصمم تعيين النموذج** وتحقق من إمكانية الاستعلام عن مصدر بيانات **GroupedTrans**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-352">Select **Validate** to inspect the editable model-mapping component on the **Model mapping designer** page and verify that the configured **GroupedTrans** data source can be queried.</span></span>

    ![التحقق من صحة المكون رسم الخرائط نموذج التقارير الإلكترونية والتحقق من مصدر البيانات التي تم تكوينها، GroupedTrans يمكن الاستعلام على الصفحة مصمم الخرائط نموذج](./media/er-components-inspections-05b.png)

10. <span data-ttu-id="57bb3-354">لاحظ حدوث خطا في التحقق من الصحة، نظرا لان مصدر بيانات **الحركة** يحتوي علي حقل متداخل من نوع **الحقل المحسوب** الذي لا يسمح بترجمة استدعاء مصدر البيانات **GroupedTrans** إلى عبارة SQL المباشرة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-354">Notice that a validation error occurs, because the **Trans** data source contains a nested field of the **Calculated field** type that doesn't allow the call for the **GroupedTrans** data source to be translated to the direct SQL statement.</span></span>

<span data-ttu-id="57bb3-355">يبين الرسم التوضيحي التالي خطا وقت التشغيل الذي يحدث إذا تجاهلت التحذير وحدد **تشغيل** لتشغيل تنسيق مكون لاستخدام تعيين النموذج.</span><span class="sxs-lookup"><span data-stu-id="57bb3-355">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run a format that is configured to use the model-mapping.</span></span>

![أخطاء وقت التشغيل التي تحدث عند تجاهل التحذير في صفحة مصمم التنسيق](./media/er-components-inspections-05c.png)

### <a name="automatic-resolution"></a><span data-ttu-id="57bb3-357">الحل التلقائي</span><span class="sxs-lookup"><span data-stu-id="57bb3-357">Automatic resolution</span></span>

<span data-ttu-id="57bb3-358">لا يتوفر اي خيار لإصلاح هذه المشكلة تلقائيا.</span><span class="sxs-lookup"><span data-stu-id="57bb3-358">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="57bb3-359">الحل اليدوي</span><span class="sxs-lookup"><span data-stu-id="57bb3-359">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="57bb3-360">خيار 1</span><span class="sxs-lookup"><span data-stu-id="57bb3-360">Option 1</span></span>

<span data-ttu-id="57bb3-361">بدلا من أضافه حقل متداخل من نوع **الحقل المحسوب** إلى مصدر بيانات **الحركة**، أضف الحقل المتداخل **$AccNumber** لعنصر **GroupedTrans.lines** الخاص بمصدر بيانات **GroupedTrans**، وقم بتكوينه بحيث يحتوي على التعبير `TRIM(GroupedTrans.lines.AccountNum)`.</span><span class="sxs-lookup"><span data-stu-id="57bb3-361">Instead of adding a nested field of the **Calculated field** type to the **Trans** data source, add the **$AccNumber** nested field for the **GroupedTrans.lines** item of the **GroupedTrans** data source, and configure it so that it contains the expression `TRIM(GroupedTrans.lines.AccountNum)`.</span></span> <span data-ttu-id="57bb3-362">وبهذه الطريقة، يمكن تشغيل مصدر البيانات **GroupedTrans** في مستوي SQL وحساب الحقل المتداخل **$AccNumber** بعد ذلك.</span><span class="sxs-lookup"><span data-stu-id="57bb3-362">In this way, the **GroupedTrans** data source can be run at the SQL level and calculate the **$AccNumber** nested field afterward.</span></span>

#### <a name="option-2"></a><span data-ttu-id="57bb3-363">خيار 2</span><span class="sxs-lookup"><span data-stu-id="57bb3-363">Option 2</span></span>

<span data-ttu-id="57bb3-364">قم بتغيير قيمة حقل **موقع التنفيذ** لمصدر بيانات **GroupedTrans** من **الاستعلام** إلى **في الذاكرة**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-364">Change the value of the **Execution location** field for the **GroupedTrans** data source from **Query** to **In memory**.</span></span> <span data-ttu-id="57bb3-365">لا نوصي بتغيير قيمة الجدول الذي يحتوي على حجم كبير من البيانات (جدول المعاملات)، لأنه سيتم جلب جميع السجلات، وسيتم الجمع والتجميع في الذاكرة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-365">We don't recommend that you change the value for a table that has a large volume of data (transactional table), because all records will be fetched, and grouping and aggregation will be done in memory.</span></span> <span data-ttu-id="57bb3-366">لذلك، يمكن ان يتسبب هذا الأسلوب في ضعف الأداء.</span><span class="sxs-lookup"><span data-stu-id="57bb3-366">Therefore, this approach can cause poor performance.</span></span>

## <a name="executability-of-a-join-data-source"></a><a id="i6"></a><span data-ttu-id="57bb3-367">إمكانية تنفيذ مصدر بيانات الانضمام</span><span class="sxs-lookup"><span data-stu-id="57bb3-367">Executability of a JOIN data source</span></span>

<span data-ttu-id="57bb3-368">يقوم مصدر بيانات [الانضمام](er-join-data-sources.md) بدمج السجلات من جدولي قاعده بيانات أو أكثر استنادا إلى الحقول المرتبطة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-368">The [JOIN](er-join-data-sources.md) data source combines records from two or more database tables, based on related fields.</span></span> <span data-ttu-id="57bb3-369">يمكن تكوين كل مصدر بيانات **انضمام** بحيث يتم تشغيله اما في مستوي قاعده البيانات أو في الذاكرة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-369">Every **JOIN** data source can be configured so that it's run either at the database level or in memory.</span></span> <span data-ttu-id="57bb3-370">عند تكوين مصدر بيانات **الانضمام** بحيث يتم تشغيله علي مستوي قاعده البيانات، تقوم التقارير الإلكترونية بالتحقق مما إذا كان من الممكن تاسيس استعلام SQL مباشر إلى مصادر بيانات يتم الاشاره اليها في مصدر البيانات هذا أو لا.</span><span class="sxs-lookup"><span data-stu-id="57bb3-370">When a **JOIN** data source is configured so that it's run at the database level, ER checks whether a direct SQL query can be established to data sources that are referred to in that data source.</span></span> <span data-ttu-id="57bb3-371">إذا تعذر إنشاء استعلام SQL مباشر باستخدام مصدر بيانات مرجعي واحد على الأقل، فسيحدث خطأ في التحقق من الصحة في مصمم تعيين نموذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="57bb3-371">If a direct SQL query can't be established with at least one referenced data source, a validation error occurs in the ER model-mapping designer.</span></span> <span data-ttu-id="57bb3-372">توضح الرسالة التي تتلقاها انه لا يمكن تشغيل مصدر بيانات **الانضمام** المكون في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="57bb3-372">The message that you receive states that the configured **JOIN** data source can't be run at runtime.</span></span>

<span data-ttu-id="57bb3-373">توضح الخطوات التالية كيفيه حدوث هذه المشكلة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-373">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="57bb3-374">ابدأ بتكوين مكون تعيين نموذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="57bb3-374">Start to configure the ER model-mapping component.</span></span>
2. <span data-ttu-id="57bb3-375">أضف مصدر بيانات من نوع **Dynamics 365 for Operations \\ سجلات الجداول**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-375">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="57bb3-376">قم بتسمية مصدر البيانات الجديد **المورد**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-376">Name the new data source **Vendor**.</span></span> <span data-ttu-id="57bb3-377">في حقل **الجدول**، حدد **VendTable** لتحديد أن مصدر البيانات سيطلب الجدول VendTable.</span><span class="sxs-lookup"><span data-stu-id="57bb3-377">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
4. <span data-ttu-id="57bb3-378">أضف مصدر بيانات من نوع **Dynamics 365 for Operations \\ سجلات الجداول**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-378">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
5. <span data-ttu-id="57bb3-379">قم بتسمية مصدر البيانات الجديد **Trans**. في حقل **الجدول**، حدد **VendTrans** لتحديد أن مصدر البيانات هذا سيطلب جدول VendTrans.</span><span class="sxs-lookup"><span data-stu-id="57bb3-379">Name the new data source **Trans**. In the **Table** field, select **VendTrans** to specify that this data source will request the VendTrans table.</span></span>
6. <span data-ttu-id="57bb3-380">أضف مصدر بيانات من نوع **الحقل المحسوب** كحقل متداخل لمصدر بيانات **المورد**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-380">Add a data source of the **Calculated field** type as the nested field of the **Vendor** data source.</span></span>
7. <span data-ttu-id="57bb3-381">قم بتسميه مصدر البيانات الجديد **FilteredTrans**، وقم بتكوينه بحيث يحتوي علي التعبير `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`.</span><span class="sxs-lookup"><span data-stu-id="57bb3-381">Name the new data source **FilteredTrans**, and configure it so that it contains the expression `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`.</span></span>
8. <span data-ttu-id="57bb3-382">أضف مصدر بيانات من نوع **الانضمام**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-382">Add a data source of the **Join** type.</span></span>
9. <span data-ttu-id="57bb3-383">قم بتسميه مصدر البيانات الجديد **JoinedList**، ثم قم بتكوينه بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="57bb3-383">Name the new data source **JoinedList**, and configure it in the following way:</span></span>

    1. <span data-ttu-id="57bb3-384">أضف مصدر بيانات **المورد** كمجموعه السجلات الاولي المراد الانضمام اليها.</span><span class="sxs-lookup"><span data-stu-id="57bb3-384">Add the **Vendor** data source as the first set of records to join.</span></span>
    2. <span data-ttu-id="57bb3-385">أضف مصدر بيانات **Vendor.FilteredTrans** كمجموعه السجلات الثانية المراد الانضمام اليها.</span><span class="sxs-lookup"><span data-stu-id="57bb3-385">Add the **Vendor.FilteredTrans** data source as the second set of records to join.</span></span> <span data-ttu-id="57bb3-386">حدد **داخلي** باعتباره النوع.</span><span class="sxs-lookup"><span data-stu-id="57bb3-386">Select **INNER** as the type.</span></span>
    3. <span data-ttu-id="57bb3-387">في حقل **التنفيذ**، حدد **استعلام** لتحديد انك تريد تشغيل مصدر البيانات هذا على مستوي قاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="57bb3-387">In the **Execute** field, select **Query** to specify that you want to run this data source at the database level.</span></span>

    ![تكوين مصدر البيانات في صفحة مصمم الانضمام](./media/er-components-inspections-06a.gif)

10. <span data-ttu-id="57bb3-389">حدد **التحقق من الصحة** لفحص مكون تعيين النموذج القابل للتحرير على صفحة **مصمم تعيين النموذج** وتحقق من إمكانية الاستعلام عن مصدر بيانات **JoinedList**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-389">Select **Validate** to inspect the editable model-mapping component on the **Model mapping designer** page and verify that the configured **JoinedList** data source can be queried.</span></span>
11. <span data-ttu-id="57bb3-390">قم بتغيير التعبير الخاص بمصدر بيانات **Vendor.FilteredTrans** من `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`إلى `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)`.</span><span class="sxs-lookup"><span data-stu-id="57bb3-390">Change the expression of the **Vendor.FilteredTrans** data source from `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)` to `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)`.</span></span>
12. <span data-ttu-id="57bb3-391">حدد **التحقق من الصحة** لفحص مكون تعيين النموذج القابل للتحرير على صفحة **مصمم تعيين النموذج** وتحقق من إمكانية الاستعلام عن مصدر بيانات **JoinedList**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-391">Select **Validate** to inspect the editable model-mapping component on the **Model mapping designer** page and verify that the configured **JoinedList** data source can be queried.</span></span>

    ![تحقق من صحة مكون تعيين النموذج القابل للتحرير وتحقق من إمكانية الاستعلام عن مصدر بيانات القائمة المنضمة في صفحة مصمم تعيين النموذج](./media/er-components-inspections-06b.png)

13. <span data-ttu-id="57bb3-393">لاحظ حدوث خطأ في التحقق من الصحة، لأن التعبير عن مصدر بيانات **Vendor.FilteredTrans** لا يمكن ترجمته إلى استدعاء SQL المباشر.</span><span class="sxs-lookup"><span data-stu-id="57bb3-393">Notice that a validation error occurs, because the expression of the **Vendor.FilteredTrans** data source can't be translated to the direct SQL call.</span></span> <span data-ttu-id="57bb3-394">بالاضافه إلى ذلك، لا يسمح استدعاء SQL المباشر بترجمة الاستدعاء لمصدر بيانات **JoinedList** إلى عبارة SQL المباشرة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-394">Additionally, the direct SQL call doesn't allow the call for the **JoinedList** data source to be translated to the direct SQL statement.</span></span>

    ![أخطاء وقت التشغيل من فشل التحقق من صحة مصدر بيانات JoinList في صفحة مصمم تعيين النموذج](./media/er-components-inspections-06c.png)

<span data-ttu-id="57bb3-396">يبين الرسم التوضيحي التالي خطا وقت التشغيل الذي يحدث إذا تجاهلت التحذير وحدد **تشغيل** لتشغيل تنسيق مكون لاستخدام تعيين النموذج.</span><span class="sxs-lookup"><span data-stu-id="57bb3-396">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run a format that is configured to use the model-mapping.</span></span>

![تشغيل التنسيق القابل للتحرير علي صفحه مصمم التنسيق](./media/er-components-inspections-06e.png)

### <a name="automatic-resolution"></a><span data-ttu-id="57bb3-398">الحل التلقائي</span><span class="sxs-lookup"><span data-stu-id="57bb3-398">Automatic resolution</span></span>

<span data-ttu-id="57bb3-399">لا يتوفر اي خيار لإصلاح هذه المشكلة تلقائيا.</span><span class="sxs-lookup"><span data-stu-id="57bb3-399">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="57bb3-400">الحل اليدوي</span><span class="sxs-lookup"><span data-stu-id="57bb3-400">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="57bb3-401">خيار 1</span><span class="sxs-lookup"><span data-stu-id="57bb3-401">Option 1</span></span>

<span data-ttu-id="57bb3-402">قم بتغيير تعبير مصدر بيانات **Vendor.FilteredTrans** من `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)` مرة أخرى إلى `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`، عند إرشادك إلى التحذير.</span><span class="sxs-lookup"><span data-stu-id="57bb3-402">Change the expression of the **Vendor.FilteredTrans** data source from `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)` back to `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`, as the warning advised.</span></span>

![تعبير محدث لمصدر البيانات في صفحة مصمم تعيين النموذج](./media/er-components-inspections-06d.png)

#### <a name="option-2"></a><span data-ttu-id="57bb3-404">خيار 2</span><span class="sxs-lookup"><span data-stu-id="57bb3-404">Option 2</span></span>

<span data-ttu-id="57bb3-405">قم بتغيير قيمة حقل **التنفيذ** لمصدر بيانات **JoinedList** من **الاستعلام** إلى **في الذاكرة**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-405">Change the value of the **Execute** field for the **JoinedList** data source from **Query** to **In memory**.</span></span> <span data-ttu-id="57bb3-406">لا نوصي بتغيير قيمة الجدول الذي يحتوي على حجم كبير من البيانات (جدول المعاملات)، لأنه سيتم جلب جميع السجلات، وسيتم الانضمام في الذاكرة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-406">We don't recommend that you change the value for a table that has a large volume of data (transactional table), because all records will be fetched, and the join occurs in memory.</span></span> <span data-ttu-id="57bb3-407">لذلك، يمكن ان يتسبب هذا الأسلوب في ضعف الأداء.</span><span class="sxs-lookup"><span data-stu-id="57bb3-407">Therefore, this approach can cause poor performance.</span></span> <span data-ttu-id="57bb3-408">يظهر تحذير التحقق من الصحة لاعلامك بهذه المخاطرة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-408">A validation warning is shown to inform you about this risk.</span></span>

## <a name="preferability-of-filter-vs-where-function"></a><a id="i7"></a><span data-ttu-id="57bb3-409">تفضيل وظيفة التصفية مقابل المكان</span><span class="sxs-lookup"><span data-stu-id="57bb3-409">Preferability of FILTER vs WHERE function</span></span>

<span data-ttu-id="57bb3-410">يتم استخدام وظيفة [تصفية](er-functions-list-filter.md) التقارير الإلكترونية المضمنة للوصول إلى جداول التطبيق أو طرق العرض أو كيانات البيانات عن طريق وضع استدعاء SQL مفرد للحصول علي البيانات المطلوبة كقائمه سجلات.</span><span class="sxs-lookup"><span data-stu-id="57bb3-410">The built-in [FILTER](er-functions-list-filter.md) ER function is used to access application tables, views, or data entities by placing a single SQL call to get the required data as a list of records.</span></span> <span data-ttu-id="57bb3-411">تقوم وظيفة [المكان](er-functions-list-where.md) بجلب كافة السجلات من المصدر المحدد وتقوم بتحديد السجل في الذاكرة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-411">The [WHERE](er-functions-list-where.md) function fetches all records from the given source and does record selection in memory.</span></span> <span data-ttu-id="57bb3-412">يتم استخدام مصدر بيانات من نوع **قائمة السجلات** كوسيطة لكلٍّ من الوظيفتين ويحدد مصدرًا للحصول على السجلات.</span><span class="sxs-lookup"><span data-stu-id="57bb3-412">A data source of the **Record list** type is used as an argument of both functions and specifies a source for getting records.</span></span> <span data-ttu-id="57bb3-413">يقوم التقارير الإلكترونية بالتحقق مما إذا كان من الممكن إنشاء استدعاء SQL مباشر إلى مصدر بيانات يشار إليه في وظيفة **المكان**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-413">ER checks whether a direct SQL call can be established to a data source that is referred to in the **WHERE** function.</span></span> <span data-ttu-id="57bb3-414">في حاله تعذر إنشاء الاستدعاء المباشر، يحدث تحذير في التحقق من الصحة في مصمم تعيين نموذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="57bb3-414">If a direct call can be established, a validation warning occurs in the ER model-mapping designer.</span></span> <span data-ttu-id="57bb3-415">توصي الرسالة التي تظهر لك باستخدام وظيفة **التصفية** بدلاً من وظيفة **المكان** للمساعدة في تحسين الكفاءة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-415">The message that you receive recommends that you use the **FILTER** function instead of the **WHERE** function to help improve efficiency.</span></span>

<span data-ttu-id="57bb3-416">توضح الخطوات التالية كيفيه حدوث هذه المشكلة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-416">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="57bb3-417">ابدأ بتكوين مكون تعيين نموذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="57bb3-417">Start to configure the ER model-mapping component.</span></span>
2. <span data-ttu-id="57bb3-418">أضف مصدر بيانات من نوع **Dynamics 365 for Operations \\ سجلات الجداول**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-418">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="57bb3-419">قم بتسمية مصدر البيانات الجديد **Trans**. في حقل **الجدول**، حدد **VendTrans** لتحديد أن مصدر البيانات هذا سيطلب جدول VendTrans.</span><span class="sxs-lookup"><span data-stu-id="57bb3-419">Name the new data source **Trans**. In the **Table** field, select **VendTrans** to specify that this data source will request the VendTrans table.</span></span>
4. <span data-ttu-id="57bb3-420">أضف مصدر بيانات من نوع **الحقل المحسوب** كحقل متداخل لمصدر بيانات **المورد**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-420">Add a data source of the **Calculated field** type as the nested field of the **Vendor** data source.</span></span>
5. <span data-ttu-id="57bb3-421">قم بتسميه مصدر البيانات الجديد **FilteredTrans**، وقم بتكوينه بحيث يحتوي علي التعبير `WHERE(Trans, Trans.AccountNum="US-101")`.</span><span class="sxs-lookup"><span data-stu-id="57bb3-421">Name the new data source **FilteredTrans**, and configure it so that it contains the expression `WHERE(Trans, Trans.AccountNum="US-101")`.</span></span>
6. <span data-ttu-id="57bb3-422">أضف مصدر بيانات من نوع **Dynamics 365 for Operations \\ سجلات الجداول**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-422">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
7. <span data-ttu-id="57bb3-423">قم بتسمية مصدر البيانات الجديد **المورد**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-423">Name the new data source **Vendor**.</span></span> <span data-ttu-id="57bb3-424">في حقل **الجدول**، حدد **VendTable** لتحديد أن مصدر البيانات سيطلب الجدول VendTable.</span><span class="sxs-lookup"><span data-stu-id="57bb3-424">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
8. <span data-ttu-id="57bb3-425">أضف مصدر بيانات من نوع **الحقل المحسوب**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-425">Add a data source of the **Calculated field** type.</span></span>
9. <span data-ttu-id="57bb3-426">قم بتسميه مصدر البيانات الجديد **FilteredVendor**، وقم بتكوينه بحيث يحتوي علي التعبير `WHERE(Vendor, Vendor.AccountNum="US-101")`.</span><span class="sxs-lookup"><span data-stu-id="57bb3-426">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `WHERE(Vendor, Vendor.AccountNum="US-101")`.</span></span>
10. <span data-ttu-id="57bb3-427">حدد **التحقق من الصحة** لفحص مكون تعيين النموذج القابل للتحرير في صفحه **مصمم تعيين النموذج**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-427">Select **Validate** to inspect the editable model-mapping component on the **Model mapping designer** page.</span></span>

    ![التحقق من الصحة لفحص مكون تعيين النموذج القابل للتحرير في صفحه مصمم تعيين النموذج](./media/er-components-inspections-07a.png)

11. <span data-ttu-id="57bb3-429">لاحظ أن تحذيرات التحقق من الصحة توصي باستخدام وظيفة **التصفية** بدلاً من وظيفة **المكان** لمصدري البيانات **FilteredVendor** و **FilteredTrans**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-429">Notice that validation warnings recommend that you use the **FILTER** function instead of the **WHERE** function for the **FilteredVendor** and **FilteredTrans** data sources.</span></span>

    ![تحذيرات التحقق من الصحة إبداء وظيفة التصفية بدلا من وظيفة المكان في صفحة مصمم تعيين النموذج](./media/er-components-inspections-07b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="57bb3-431">الحل التلقائي</span><span class="sxs-lookup"><span data-stu-id="57bb3-431">Automatic resolution</span></span>

<span data-ttu-id="57bb3-432">حدد **إصلاح** لاستبدال وظيفة **المكان** تلقائيًا بوظيفة **التصفية** في التعبير الخاص بكافة مصادر البيانات التي تظهر في الشبكة في علامة التبويب **تحذيرات** لهذا النوع من الفحص.</span><span class="sxs-lookup"><span data-stu-id="57bb3-432">Select **Fix** to automatically replace the **WHERE** function with the **FILTER** function in the expression of all data sources that appear in the grid on the **Warnings** tab for this type of inspection.</span></span>

<span data-ttu-id="57bb3-433">وبدلاً من ذلك، يمكنك تحديد الصف لأحد التحذيرات الفردية في الشبكة ثم حدد **تم تحديد الإصلاح**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-433">Alternatively, you can select the row for a single warning in the grid and then select **Fix selected**.</span></span> <span data-ttu-id="57bb3-434">في هذه الحالة، يتم تغيير التعبير تلقائيا في مصدر البيانات المذكور في التحذير المحدد.</span><span class="sxs-lookup"><span data-stu-id="57bb3-434">In this case, the expression is automatically changed only in the data source that is mentioned in the selected warning.</span></span>

![حدد إصلاح لاستبدال وظيفة المكان تلقائيًا بوظيفة التصفية في صفحة مصمم تعيين النموذج](./media/er-components-inspections-07c.png)

### <a name="manual-resolution"></a><span data-ttu-id="57bb3-436">الحل اليدوي</span><span class="sxs-lookup"><span data-stu-id="57bb3-436">Manual resolution</span></span>

<span data-ttu-id="57bb3-437">يمكنك ضبط التعبيرات الخاصة بكافة مصادر البيانات المذكورة في شبكه التحقق من الصحة يدويا وذلك باستبدال وظيفة **المكان** بوظيفة **التصفية**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-437">You can manually adjust the expressions of all the data sources in the validation grid by replacing the **WHERE** function with the **FILTER** function.</span></span>

## <a name="preferability-of-allitemsquery-vs-allitems-function"></a><a id="i8"></a><span data-ttu-id="57bb3-438">تفضيل وظيفة ALLITEMSQUERY مقابل ALLITEMS</span><span class="sxs-lookup"><span data-stu-id="57bb3-438">Preferability of ALLITEMSQUERY vs ALLITEMS function</span></span>

<span data-ttu-id="57bb3-439">يتم استخدام وظيفتي التقارير الإلكترونية [ALLITEMS](er-functions-list-allitems.md) و [ALLITEMSQUERY](er-functions-list-allitemsquery.md) المدمجتين للحصول على قيمة **قائمة السجلات** المسطحة التي تحتوي على قائمة السجلات التي تمثل جميع العناصر التي تطابق المسار المحدد.</span><span class="sxs-lookup"><span data-stu-id="57bb3-439">The built-in [ALLITEMS](er-functions-list-allitems.md) and [ALLITEMSQUERY](er-functions-list-allitemsquery.md) ER functions return a flattened **Record list** value that consists of a list of records that represent all items that match the specified path.</span></span> <span data-ttu-id="57bb3-440">يقوم التقارير الإلكترونية بالتحقق مما إذا كان من الممكن إنشاء استدعاء SQL مباشر إلى مصدر بيانات يشار إليه في وظيفة **ALLITEMS**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-440">ER checks whether a direct SQL call can be established to a data source that is referred to in the **ALLITEMS** function.</span></span> <span data-ttu-id="57bb3-441">في حاله تعذر إنشاء الاستدعاء المباشر، يحدث تحذير في التحقق من الصحة في مصمم تعيين نموذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="57bb3-441">If a direct call can be established, a validation warning occurs in the ER model-mapping designer.</span></span> <span data-ttu-id="57bb3-442">توصي الرسالة التي تظهر لك باستخدام وظيفة **ALLITEMSQUERY** بدلاً من وظيفة **ALLITEMS** للمساعدة في تحسين الكفاءة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-442">The message that you receive recommends that you use the **ALLITEMSQUERY** function instead of the **ALLITEMS** function to help improve efficiency.</span></span>

<span data-ttu-id="57bb3-443">توضح الخطوات التالية كيفيه حدوث هذه المشكلة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-443">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="57bb3-444">ابدأ بتكوين مكون تعيين نموذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="57bb3-444">Start to configure the ER model-mapping component.</span></span>
2. <span data-ttu-id="57bb3-445">أضف مصدر بيانات من نوع **Dynamics 365 for Operations \\ سجلات الجداول**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-445">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="57bb3-446">قم بتسمية مصدر البيانات الجديد **المورد**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-446">Name the new data source **Vendor**.</span></span> <span data-ttu-id="57bb3-447">في حقل **الجدول**، حدد **VendTable** لتحديد أن مصدر البيانات سيطلب الجدول VendTable.</span><span class="sxs-lookup"><span data-stu-id="57bb3-447">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
4. <span data-ttu-id="57bb3-448">أضف مصدر بيانات من نوع **الحقل المحسوب** للحصول على سجلات للعديد من الموردين.</span><span class="sxs-lookup"><span data-stu-id="57bb3-448">Add a data source of the **Calculated field** type to get records for several vendors.</span></span>
5. <span data-ttu-id="57bb3-449">قم بتسميه مصدر البيانات الجديد **FilteredVendor**، وقم بتكوينه بحيث يحتوي علي التعبير `FILTER(Vendor, OR(Vendor.AccountNum="US-101",Vendor.AccountNum="US-102"))`.</span><span class="sxs-lookup"><span data-stu-id="57bb3-449">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, OR(Vendor.AccountNum="US-101",Vendor.AccountNum="US-102"))`.</span></span>
6. <span data-ttu-id="57bb3-450">أضف مصدر بيانات من نوع **الحقل المحسوب** للحصول على حركات جميع الموردين الذين تمت تصفيتهم.</span><span class="sxs-lookup"><span data-stu-id="57bb3-450">Add a data source of the **Calculated field** type to get transactions of all filtered vendors.</span></span>
7. <span data-ttu-id="57bb3-451">قم بتسميه مصدر البيانات الجديد **FilteredVendor**، وقم بتكوينه بحيث يحتوي على التعبير `ALLITEMS(FilteredVendor.'<Relations'.'VendTrans.VendTable_AccountNum')`.</span><span class="sxs-lookup"><span data-stu-id="57bb3-451">Name the new data source **FilteredVendorTrans**, and configure it so that it contains the expression `ALLITEMS(FilteredVendor.'<Relations'.'VendTrans.VendTable_AccountNum')`.</span></span>
8. <span data-ttu-id="57bb3-452">حدد **التحقق من الصحة** لفحص مكون تعيين النموذج القابل للتحرير في صفحه **مصمم تعيين النموذج**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-452">Select **Validate** to inspect the editable model-mapping component on the **Model mapping designer** page.</span></span>

    ![صفحة مصمم تعيين النموذج، زر التحقق](./media/er-components-inspections-08a.png)

9. <span data-ttu-id="57bb3-454">لاحظ حدوث تحذير في التحقق من الصحة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-454">Notice that a validation warning occurs.</span></span> <span data-ttu-id="57bb3-455">وتوصيك الرسالة باستخدام وظيفة **ALLITEMSQUERY** بدلاً من وظيفة **ALLITEMS** لمصدر بيانات **FilteredVendorTrans**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-455">The message recommends that you use the **ALLITEMSQUERY** function instead of the **ALLITEMS** function for the **FilteredVendorTrans** data source.</span></span>

    ![تحذير من التحقق من الصحة لاستخدام وظيفة ALLITEMSQUالتقارير الإلكترونيةY بدلاً من وظيفة ALLITEMS في مكون تعيين نموذج التقارير الإلكترونية في صفحة مصمم تعيين النموذج](./media/er-components-inspections-08b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="57bb3-457">الحل التلقائي</span><span class="sxs-lookup"><span data-stu-id="57bb3-457">Automatic resolution</span></span>

<span data-ttu-id="57bb3-458">حدد **إصلاح** لاستبدال وظيفة **ALLITEMS** تلقائيًا بوظيفة **ALLITEMSQUERY** في التعبير الخاص بكافة مصادر البيانات التي تظهر في الشبكة في علامة التبويب **تحذيرات** لهذا النوع من الفحص.</span><span class="sxs-lookup"><span data-stu-id="57bb3-458">Select **Fix** to automatically replace the **ALLITEMS** function with the **ALLITEMSQUERY** function in the expression of all data sources that appear in the grid on the **Warnings** tab for this type of inspection.</span></span>

<span data-ttu-id="57bb3-459">وبدلاً من ذلك، يمكنك تحديد الصف لأحد التحذيرات الفردية في الشبكة ثم حدد **تم تحديد الإصلاح**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-459">Alternatively, you can select the row for a single warning in the grid and then select **Fix selected**.</span></span> <span data-ttu-id="57bb3-460">في هذه الحالة، يتم تغيير التعبير تلقائيا في مصدر البيانات المذكور في التحذير المحدد.</span><span class="sxs-lookup"><span data-stu-id="57bb3-460">In this case, the expression is automatically changed only in the data source that is mentioned in the selected warning.</span></span>

![صفحة مصمم تعيين النموذج، حدد تم تحديد الإصلاح](./media/er-components-inspections-08c.png)

### <a name="manual-resolution"></a><span data-ttu-id="57bb3-462">الحل اليدوي</span><span class="sxs-lookup"><span data-stu-id="57bb3-462">Manual resolution</span></span>

<span data-ttu-id="57bb3-463">يمكنك ضبط التعبيرات الخاصة بكافة مصادر البيانات المذكورة في شبكه التحقق من الصحة يدويا وذلك باستبدال وظيفة **ALLITEMS** بوظيفة **ALLITEMSQUERY**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-463">You can manually adjust the expressions of all the data sources that are mentioned in the validation grid by replacing the **ALLITEMS** function with the **ALLITEMSQUERY** function.</span></span>

## <a name="consideration-of-empty-list-cases"></a><a id="i9"></a><span data-ttu-id="57bb3-464">اعتبار حالات القائمة الفارغة</span><span class="sxs-lookup"><span data-stu-id="57bb3-464">Consideration of empty list cases</span></span>

<span data-ttu-id="57bb3-465">يمكنك تكوين التنسيق الخاص بك أو مكون تعيين النموذج للحصول علي قيمه الحقل لمصدر البيانات الخاص بنوع **قائمة السجلات**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-465">You can configure your ER format or model-mapping component to get the field value of a data source of the **Record list** type.</span></span> <span data-ttu-id="57bb3-466">يقوم التقارير الإلكترونية بفحص ما إذا كان تصميمك يعتبر الحالة التي لا يحتوي فيها مصدر بيانات يسمي علي إيه سجلات (اي انه فارغ)، لتجنب أخطاء وقت التشغيل عند إحضار أحدي القيم من أحد حقول السجلات غير الموجودة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-466">ER checks whether your design considers the case where a data source that is called contains no records (that is, it's empty), to prevent runtime errors when a value is fetched from a field of a nonexistent record.</span></span>

<span data-ttu-id="57bb3-467">توضح الخطوات التالية كيفيه حدوث هذه المشكلة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-467">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="57bb3-468">ابدأ في تكوين نموذج بيانات التقارير الإلكترونية وتعيين نموذج التقارير الإلكترونية ومكونات تنسيق التقارير الإلكترونية في وقت واحد.</span><span class="sxs-lookup"><span data-stu-id="57bb3-468">Start to configure the ER data model, the ER model-mapping, and the ER format components simultaneously.</span></span>
2. <span data-ttu-id="57bb3-469">في شجرة نموذج البيانات، قم باضافه العنصر الجذر المسمى **الجذر 3**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-469">In the data model tree, add a root item that is named **Root3**.</span></span>
3. <span data-ttu-id="57bb3-470">قم بتعديل عنصر **الجذر 3** عن طريق إضافة عنصر متداخل من نوع **قائمة السجلات**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-470">Modify the **Root3** item by adding a nested item of the **Record list** type.</span></span>
4. <span data-ttu-id="57bb3-471">قم بتسمية العنصر المتداخل الجديد **المورد**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-471">Name the new nested item **Vendor**.</span></span>
5. <span data-ttu-id="57bb3-472">قم بتعديل عنصر **المورد** بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="57bb3-472">Modify the **Vendor** item in the following way:</span></span>

    - <span data-ttu-id="57bb3-473">أضف حقلاً متداخلاً من نوع **السلسلة**، وقم بتسميته بـ **اسم**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-473">Add a nested field of the **String** type, and name it **Name**.</span></span>
    - <span data-ttu-id="57bb3-474">أضف حقلاً متداخلاً من نوع **السلسلة**، وقم بتسميته بـ **AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-474">Add a nested field of the **String** type, and name it **AccountNumber**.</span></span>

    ![إضافة حقول متداخلة في صفحة نموذج البيانات](./media/er-components-inspections-09a.png)

6. <span data-ttu-id="57bb3-476">في جزء مصادر بيانات تعيين النموذج، أضف مصدر بيانات من نوع **Dynamics 365 for Operations \\ سجلات الجداول**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-476">In the model-mapping data sources pane, add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
7. <span data-ttu-id="57bb3-477">قم بتسمية مصدر البيانات الجديد **المورد**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-477">Name the new data source **Vendor**.</span></span> <span data-ttu-id="57bb3-478">في حقل **الجدول**، حدد **VendTable** لتحديد أن مصدر البيانات سيطلب الجدول VendTable.</span><span class="sxs-lookup"><span data-stu-id="57bb3-478">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
8. <span data-ttu-id="57bb3-479">أضف مصدر بيانات من نوع **عام \\ معلمة إدخال المستخدم** للبحث عن حساب مورد في مربع حوار وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="57bb3-479">Add a data source of the **General \\ User input parameter** type to search for a vendor account in the runtime dialog box.</span></span>
9. <span data-ttu-id="57bb3-480">قم بتسمية مصدر البيانات الجديد **RequestedAccountNum**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-480">Name the new data source **RequestedAccountNum**.</span></span> <span data-ttu-id="57bb3-481">في حقل **التسمية**، أدخل **رقم حساب المورد**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-481">In the **Label** field, enter **Vendor account number**.</span></span> <span data-ttu-id="57bb3-482">في حقل **اسم نوع بيانات Operations**، اترك القيمة الافتراضية، وهي **الوصف**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-482">In the **Operations data type name** field, leave the default value, **Description**.</span></span>
10. <span data-ttu-id="57bb3-483">أضف مصدر بيانات من نوع **الحقل المحسوب** لتصفية مورد تم الاستعلام عنه.</span><span class="sxs-lookup"><span data-stu-id="57bb3-483">Add a data source of the **Calculated field** type to filter a vendor that is inquired about.</span></span>
11. <span data-ttu-id="57bb3-484">قم بتسميه مصدر البيانات الجديد **FilteredVendor**، وقم بتكوينه بحيث يحتوي علي التعبير `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.</span><span class="sxs-lookup"><span data-stu-id="57bb3-484">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.</span></span>
12. <span data-ttu-id="57bb3-485">اربط عناصر نموذج البيانات بمصادر البيانات التي تم تكوينها بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="57bb3-485">Bind the data model items to configured data sources in the following way:</span></span>

    - <span data-ttu-id="57bb3-486">اربط **FilteredVendor** بـ **المورد**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-486">Bind **FilteredVendor** to **Vendor**.</span></span>
    - <span data-ttu-id="57bb3-487">اربط **FilteredVendor.AccountNum** بـ **Vendor.AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-487">Bind **FilteredVendor.AccountNum** to **Vendor.AccountNumber**.</span></span>
    - <span data-ttu-id="57bb3-488">اربط **FilteredVendor.'name()'** بـ **Vendor.Name**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-488">Bind **FilteredVendor.'name()'** to **Vendor.Name**.</span></span>

    ![ربط عناصر نماذج البيانات في صفحة مصمم تعيين النموذج](./media/er-components-inspections-09b.png)

13. <span data-ttu-id="57bb3-490">في شجرة بنية التنسيق، أضف الأصناف التالية لإنشاء مستند صادر بتنسيق XML الذي يحتوي على تفاصيل المورد:</span><span class="sxs-lookup"><span data-stu-id="57bb3-490">In the format structure tree, add the following items to generate an outbound document in XML format that contains the vendor details:</span></span>

    1. <span data-ttu-id="57bb3-491">أضف عنصر XML الخاص بجذر **العبارة**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-491">Add the **Statement** root XML element.</span></span>
    2. <span data-ttu-id="57bb3-492">بالنسبة إلى عنصر XML لـ **العبارة**، أضف عنصر XML لـ **الطرف** المتداخل.</span><span class="sxs-lookup"><span data-stu-id="57bb3-492">For the **Statement** XML element, add the nested **Party** XML element.</span></span>
    3. <span data-ttu-id="57bb3-493">بالنسبة لعناصر XML **للطرف**، أضف سمات XML المتداخلة التالية:</span><span class="sxs-lookup"><span data-stu-id="57bb3-493">For the **Party** XML element, add the following nested XML attributes:</span></span>

        - <span data-ttu-id="57bb3-494">الاسم</span><span class="sxs-lookup"><span data-stu-id="57bb3-494">Name</span></span>
        - <span data-ttu-id="57bb3-495">AccountNum</span><span class="sxs-lookup"><span data-stu-id="57bb3-495">AccountNum</span></span>

14. <span data-ttu-id="57bb3-496">ربط عناصر التنسيق بمصادر البيانات المتوفرة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="57bb3-496">Bind format elements to provided data sources in the following way:</span></span>

    - <span data-ttu-id="57bb3-497">اربط عنصر تنسيق **العبارة\\الطرف\\الاسم** بحقل مصدر البيانات **model.Vendor.Name**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-497">Bind the **Statement\\Party\\Name** format element to the **model.Vendor.Name** data source field.</span></span>
    - <span data-ttu-id="57bb3-498">اربط عنصر تنسيق **العبارة\\الطرف\\AccountNum** بحقل مصدر البيانات **model.Vendor.AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-498">Bind the **Statement\\Party\\AccountNum** format element to the **model.Vendor.AccountNumber** data source field.</span></span>

15. <span data-ttu-id="57bb3-499">حدد **التحقق من الصحة** لفحص مكون التنسيق القابل للتحرير في صفحة **مصمم التنسيق**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-499">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![التحقق من صحة عناصر التنسيق التي قمت بربطها بمصادر البيانات في صفحة "مصمم التنسيق"](./media/er-components-inspections-09c.png)

16. <span data-ttu-id="57bb3-501">لاحظ حدوث خطا في التحقق من الصحة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-501">Notice that a validation error occurs.</span></span> <span data-ttu-id="57bb3-502">وتنص الرسالة على أنه قد يظهر خطأ لمكونات تنسيق **العبارة\\الطرف\\الاسم** و **العبارة\\الطرف\\AccountNum** في وقت التشغيل إذا كانت قائمة `model.Vendor` فارغة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-502">The message states that an error might be thrown for the configured **Statement\\Party\\Name** and **Statement\\Party\\AccountNum** format components at runtime if the `model.Vendor` list is empty.</span></span>

    ![خطأ في التحقق من الصحة يُعلم بالخطأ المحتمل لمكونات التنسيق المكونة](./media/er-components-inspections-09d.png)

<span data-ttu-id="57bb3-504">يبين الرسم التوضيحي التالي خطا وقت التشغيل الذي يحدث إذا تجاهلت التحذير، حدد **تشغيل** لتشغيل التنسيق، وحدد رقم الحساب للمورد غير الموجود.</span><span class="sxs-lookup"><span data-stu-id="57bb3-504">The following illustration shows the runtime error that occurs if you ignore the warning, select **Run** to run the format, and select the account number of a nonexistent vendor.</span></span> <span data-ttu-id="57bb3-505">لأن المورد المطلوب غير موجود، فستكون قائمة `model.Vendor` فارغة (وهذا يعني أنها لن تحتوي على أي سجلات).</span><span class="sxs-lookup"><span data-stu-id="57bb3-505">Because the requested vendor doesn't exist, the `model.Vendor` list will be empty (that is, it will contain no records).</span></span>

![أخطاء وقت التشغيل لأنها حدثت أثناء تشغيل تعيين التنسيق](./media/er-components-inspections-09e.png)

### <a name="automatic-resolution"></a><span data-ttu-id="57bb3-507">الحل التلقائي</span><span class="sxs-lookup"><span data-stu-id="57bb3-507">Automatic resolution</span></span>

<span data-ttu-id="57bb3-508">بالنسبة للصف المحدد في الشبكة في علامة التبويب **تحذيرات**، يمكنك تحديد **إلغاء الربط**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-508">For the selected row in the grid on the **Warnings** tab, you can select **Unbind**.</span></span> <span data-ttu-id="57bb3-509">يتم تلقائيا إزالة الربط المشار إليه في عمود **المسار** من عناصر التنسيق.</span><span class="sxs-lookup"><span data-stu-id="57bb3-509">The binding that is pointed to in the **Path** column is automatically removed from the format elements.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="57bb3-510">الحل اليدوي</span><span class="sxs-lookup"><span data-stu-id="57bb3-510">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="57bb3-511">خيار 1</span><span class="sxs-lookup"><span data-stu-id="57bb3-511">Option 1</span></span>

<span data-ttu-id="57bb3-512">يمكنك ربط عنصر تنسيق **العبارة\\الطرف\\الاسم** بعنصر مصدر البيانات `model.Vendor`.</span><span class="sxs-lookup"><span data-stu-id="57bb3-512">You can bind the **Statement\\Party\\Name** format element to the `model.Vendor` data source item.</span></span> <span data-ttu-id="57bb3-513">في وقت التشغيل، يستدعي هذا الربط مصدر بيانات `model.Vendor` أولاً.</span><span class="sxs-lookup"><span data-stu-id="57bb3-513">At runtime, this binding calls the `model.Vendor` data source first.</span></span> <span data-ttu-id="57bb3-514">عندما يُرجع `model.Vendor` قائمه سجلات فارغه، لا يتم تشغيل عناصر التنسيق المتداخل.</span><span class="sxs-lookup"><span data-stu-id="57bb3-514">When `model.Vendor` returns an empty record list, the nested format elements aren't run.</span></span> <span data-ttu-id="57bb3-515">لذلك، لا تحدث أي تحذيرات تحقق من الصحة لتكوين التنسيق هذا.</span><span class="sxs-lookup"><span data-stu-id="57bb3-515">Therefore, no validation warnings occur for this format configuration.</span></span>

![ربط عنصر التنسيق بعنصر مصدر البيانات في صفحة مصمم التنسيق](./media/er-components-inspections-09e.gif)

#### <a name="option-2"></a><span data-ttu-id="57bb3-517">خيار 2</span><span class="sxs-lookup"><span data-stu-id="57bb3-517">Option 2</span></span>

<span data-ttu-id="57bb3-518">قم بتغيير ربط عنصر تنسيق **العبارة\\الطرف\\الاسم** من `model.Vendor.Name` إلى `FIRSTORNULL(model.Vendor).Name`.</span><span class="sxs-lookup"><span data-stu-id="57bb3-518">Change the binding of the **Statement\\Party\\Name** format element from `model.Vendor.Name` to `FIRSTORNULL(model.Vendor).Name`.</span></span> <span data-ttu-id="57bb3-519">يقوم الربط المحدث بتحويل السجل الأول لمصدر بيانات `model.Vendor` الخاص بنوع **قائمة السجلات** لمصدر بيانات جديد من نوع **السجل**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-519">The updated binding conditionally converts the first record of the `model.Vendor` data source of the **Record list** type to a new data source of the **Record** type.</span></span> <span data-ttu-id="57bb3-520">يحتوي مصدر البيانات الجديد على نفس مجموعة الحقول.</span><span class="sxs-lookup"><span data-stu-id="57bb3-520">This new data source contains the same set of fields.</span></span>

- <span data-ttu-id="57bb3-521">في حالة توفر سجل واحد على الأقل في مصدر بيانات `model.Vendor`، يتم ملء حقول هذا السجل بقيم الحقول الخاصة بالسجل الأول من مصدر بيانات `model.Vendor`.</span><span class="sxs-lookup"><span data-stu-id="57bb3-521">If at least one record is available in the `model.Vendor` data source, the fields of that record are filled with the values of the fields of the first record of the `model.Vendor` data source.</span></span> <span data-ttu-id="57bb3-522">في هذه الحالة، يقوم الربط المحدث بإرجاع اسم المورد.</span><span class="sxs-lookup"><span data-stu-id="57bb3-522">In this case, the updated binding returns the vendor name.</span></span>
- <span data-ttu-id="57bb3-523">وبخلاف ذلك، يتم ملء كل حقل من السجل الذي يتم إنشاؤه بالقيمة الافتراضية لنوع البيانات الخاص بهذا الحقل.</span><span class="sxs-lookup"><span data-stu-id="57bb3-523">Otherwise, every field of the record that is created is filled with the default value for the data type of that field.</span></span> <span data-ttu-id="57bb3-524">في هذه الحالة، يتم إرجاع السلسلة الفارغة كالقيمة الافتراضية لنوع بيانات **السلسلة**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-524">In this case, the blank string is returned as the default value of the **String** data type.</span></span>

<span data-ttu-id="57bb3-525">ولذلك، لا تحدث أي تحذيرات في التحقق من الصحة لعنصر تنسيق **العبارة\\الطرف\\الاسم** عند ربطه بتعبير `FIRSTORNULL(model.Vendor).Name`.</span><span class="sxs-lookup"><span data-stu-id="57bb3-525">Therefore, no validation warnings occur for the **Statement\\Party\\Name** format element when it's bound to the `FIRSTORNULL(model.Vendor).Name` expression.</span></span>

![الربط المتغير يعمل على حل تحذيرات التحقق من الصحة على صفحة مصمم التنسيق](./media/er-components-inspections-09f.gif)

#### <a name="option-3"></a><span data-ttu-id="57bb3-527">خيار 3</span><span class="sxs-lookup"><span data-stu-id="57bb3-527">Option 3</span></span>

<span data-ttu-id="57bb3-528">إذا كنت تريد تحديد البيانات التي تم إدخالها في مستند مُنشأ بشكل صريح عندما لم يُرجع مصدر بيانات `model.Vendor` لنوع **قائمة السجلات** أي سجلات (النص **غير متوفر** في هذا المثال)، قم بتغيير ربط عنصر تنسيق **العبارة\\الطرف\\الاسم** من `model.Vendor.Name` إلى `IF(NOT(ISEMPTY(model.Vendor)), model.Vendor.Name, "Not available")`.</span><span class="sxs-lookup"><span data-stu-id="57bb3-528">If you want to explicitly specify the data that is entered in a generated document when the `model.Vendor` data source of the **Record list** type returns no records (the text **Not available** in this example), change the binding of the **Statement\\Party\\Name** format element from `model.Vendor.Name` to `IF(NOT(ISEMPTY(model.Vendor)), model.Vendor.Name, "Not available")`.</span></span> <span data-ttu-id="57bb3-529">يمكنك أيضًا استخدام التعبير `IF(COUNT(model.Vendor)=0, model.Vendor.Name, "Not available")`.</span><span class="sxs-lookup"><span data-stu-id="57bb3-529">You can also use the expression `IF(COUNT(model.Vendor)=0, model.Vendor.Name, "Not available")`.</span></span>

### <a name="additional-consideration"></a><a id="i9a"></a><span data-ttu-id="57bb3-530">الاعتبار الإضافي</span><span class="sxs-lookup"><span data-stu-id="57bb3-530">Additional consideration</span></span>

<span data-ttu-id="57bb3-531">يحذرك الفحص أيضًا بشأن مشكلة أخرى محتملة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-531">The inspection also warns you about another potential issue.</span></span> <span data-ttu-id="57bb3-532">بشكل افتراضي، عندما تقوم بربط عناصر تنسيق **العبارة\\الطرف\\الاسم** و **العبارة\\الطرف\\AccountNum** باللحقول المناسبة من مصدر بيانات `model.Vendor` الخاص بنوع **قائمة السجلات**، سيتم تشغيل هذه الروابط وستقوم بنقل قيم الحقول المناسبة للسجل الأول من مصدر بيانات `model.Vendor`، إذا كانت هذه القائمة غير فارغة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-532">By default, as you bind the **Statement\\Party\\Name** and **Statement\\Party\\AccountNum** format elements to the appropriate fields of the `model.Vendor` data source of the **Record list** type, those bindings will be run and will take the values of the appropriate fields of the first record of the `model.Vendor` data source, if that list isn't empty.</span></span>

<span data-ttu-id="57bb3-533">لأنك لم تقم بربط عنصر تنسيق **العبارة\\الطرف** بمصدر بيانات `model.Vendor`، لن يتكرر عنصر **العبارة\\الطرف** لكل سجل من مصدر بيانات `model.Vendor` أثناء تنفيذ التنسيق.</span><span class="sxs-lookup"><span data-stu-id="57bb3-533">Because you haven't bound the **Statement\\Party** format element with the `model.Vendor` data source, the **Statement\\Party** element won't be iterated for every record of the `model.Vendor` data source during format execution.</span></span> <span data-ttu-id="57bb3-534">وبدلا من ذلك، سيتم ملء المستند الذي تم إنشاؤه بمعلومات من السجل الأول فقط في قائمه السجلات، إذا كانت هذه القائمة تحتوي علي سجلات متعددة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-534">Instead, a generated document will be filled with information from only the first record of the record list, if that list contains multiple records.</span></span> <span data-ttu-id="57bb3-535">ولذلك، قد تكون هناك مشكله إذا كان من المقصود بالتنسيق ملء مستند تم إنشاؤه بمعلومات حول جميع الموردين من مصدر بيانات `model.Vendor`.</span><span class="sxs-lookup"><span data-stu-id="57bb3-535">Therefore, there might be an issue if the format is intended to fill a generated document with information about all vendors from the `model.Vendor` data source.</span></span> <span data-ttu-id="57bb3-536">لحل هذه المشكلة، قم بربط عنصر **الكشف\\الطرف** بمصدر بيانات `model.Vendor`.</span><span class="sxs-lookup"><span data-stu-id="57bb3-536">To fix this issue, bind the **Statement\\Party** element with the `model.Vendor` data source.</span></span>

## <a name="executability-of-an-expression-with-filter-function-caching"></a><a id="i10"></a><span data-ttu-id="57bb3-537">إمكانية تنفيذ تعبير باستخدام وظيفة التصفية (التخزين المؤقت)</span><span class="sxs-lookup"><span data-stu-id="57bb3-537">Executability of an expression with FILTER function (caching)</span></span>

<span data-ttu-id="57bb3-538">يتم استخدام وظائف التقارير الإلكترونية المضمنة، بما في ذلك [FILTER](er-functions-list-filter.md) و[ALLITEMSQUERY](er-functions-list-allitemsquery.md) للوصول إلى جداول التطبيق أو طرق العرض أو كيانات البيانات عن طريق وضع استدعاء SQL مفرد للحصول علي البيانات المطلوبة كقائمه سجلات.</span><span class="sxs-lookup"><span data-stu-id="57bb3-538">Several built-in ER functions, including [FILTER](er-functions-list-filter.md) and [ALLITEMSQUERY](er-functions-list-allitemsquery.md), are used to access application tables, views, or data entities by placing a single SQL call to get the required data as a list of records.</span></span> <span data-ttu-id="57bb3-539">يتم استخدام مصدر بيانات من نوع **قائمة السجلات** كوسيطة لكل وظيفة من هذه الوظائف ويحدد مصدر التطبيق الخاص بالاستدعاء.</span><span class="sxs-lookup"><span data-stu-id="57bb3-539">A data source of the **Record list** type is used as an argument of each of these functions and specifies an application source for the call.</span></span> <span data-ttu-id="57bb3-540">يقوم التقارير الإلكترونية بالتحقق مما إذا كان من الممكن إنشاء استدعاء SQL مباشر إلى مصدر بيانات يشار إليه في أحد هذه الوظائف.</span><span class="sxs-lookup"><span data-stu-id="57bb3-540">ER checks whether a direct SQL call can be established to a data source that is referred to in one of these functions.</span></span> <span data-ttu-id="57bb3-541">إذا تعذر إنشاء استدعاء مباشر لأن مصدر البيانات تم تمييزه بأنه [مخزن مؤقتًا](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace)، يحدث خطا في التحقق من الصحة في مصمم تعيين نماذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="57bb3-541">If a direct call can't be established because the data source was marked as [cached](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace), a validation error occurs in the ER model-mapping designer.</span></span> <span data-ttu-id="57bb3-542">تنص الرسالة التي تتلقاها على أنه لا يمكن تشغيل تعبير التقارير الإلكترونية الذي يحتوي على إحدى هذه الوظائف في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="57bb3-542">The message that you receive states that the ER expression that contains one of these functions can't be run at runtime.</span></span>

<span data-ttu-id="57bb3-543">توضح الخطوات التالية كيفيه حدوث هذه المشكلة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-543">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="57bb3-544">ابدأ بتكوين مكون تعيين نموذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="57bb3-544">Start to configure the ER model-mapping component.</span></span>
2. <span data-ttu-id="57bb3-545">أضف مصدر بيانات من نوع **Dynamics 365 for Operations \\ سجلات الجداول**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-545">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="57bb3-546">قم بتسمية مصدر البيانات الجديد **المورد**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-546">Name the new data source **Vendor**.</span></span> <span data-ttu-id="57bb3-547">في حقل **الجدول**، حدد **VendTable** لتحديد أن مصدر البيانات سيطلب الجدول VendTable.</span><span class="sxs-lookup"><span data-stu-id="57bb3-547">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
4. <span data-ttu-id="57bb3-548">أضف مصدر بيانات من نوع **عام \\ معلمة إدخال المستخدم** للبحث عن حساب مورد في مربع حوار وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="57bb3-548">Add a data source of the **General \\ User input parameter** type to search for a vendor account in the runtime dialog box.</span></span>
5. <span data-ttu-id="57bb3-549">قم بتسمية مصدر البيانات الجديد **RequestedAccountNum**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-549">Name the new data source **RequestedAccountNum**.</span></span> <span data-ttu-id="57bb3-550">في حقل **التسمية**، أدخل **رقم حساب المورد**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-550">In the **Label** field, enter **Vendor account number**.</span></span> <span data-ttu-id="57bb3-551">في حقل **اسم نوع بيانات Operations**، اترك القيمة الافتراضية، وهي **الوصف**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-551">In the **Operations data type name** field, leave the default value, **Description**.</span></span>
6. <span data-ttu-id="57bb3-552">أضف مصدر بيانات من نوع **الحقل المحسوب** لتصفية مورد تم الاستعلام عنه.</span><span class="sxs-lookup"><span data-stu-id="57bb3-552">Add a data source of the **Calculated field** type to filter a vendor that is inquired about.</span></span>
7. <span data-ttu-id="57bb3-553">قم بتسميه مصدر البيانات الجديد **FilteredVendor**، وقم بتكوينه بحيث يحتوي علي التعبير `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.</span><span class="sxs-lookup"><span data-stu-id="57bb3-553">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.</span></span>
8. <span data-ttu-id="57bb3-554">ضع علامة على مصدر بيانات **المورد** المكون كمخزن مؤقتًا.</span><span class="sxs-lookup"><span data-stu-id="57bb3-554">Mark the configured **Vendor** data source as cached.</span></span>

    ![تكوين مكون تعيين النموذج القابل للتحرير في صفحه مصمم تعيين النموذج](./media/er-components-inspections-10a.gif)

9. <span data-ttu-id="57bb3-556">حدد **التحقق من الصحة** لفحص مكون تعيين النموذج القابل للتحرير في صفحه **مصمم تعيين النموذج**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-556">Select **Validate** to inspect the editable model-mapping component on the **Model mapping designer** page.</span></span>

    ![التحقق من صحة وظيفة التصفية المطبق علي مصدر بيانات مورد ذاكره التخزين المؤقت في صفحه مصمم تعيين النموذج](./media/er-components-inspections-10a.png)

10. <span data-ttu-id="57bb3-558">لاحظ حدوث خطا في التحقق من الصحة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-558">Notice that a validation error occurs.</span></span> <span data-ttu-id="57bb3-559">توضح الرسالة أنه لا يمكن تطبيق وظيفة **التصفية** على مصدر بيانات **المورد** المخزن مؤقتًا.</span><span class="sxs-lookup"><span data-stu-id="57bb3-559">The message states that the **FILTER** function can't be applied to the cached **Vendor** data source.</span></span>

<span data-ttu-id="57bb3-560">يبين الرسم التوضيحي التالي خطا وقت التشغيل الذي يحدث إذا تجاهلت التحذير وحدد **تشغيل** لتشغيل التنسيق.</span><span class="sxs-lookup"><span data-stu-id="57bb3-560">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run the format.</span></span>

![خطأ وقت التشغيل الذي حدث أثناء تعيين التنسيق يعمل على صفحة مصمم التنسيق](./media/er-components-inspections-10b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="57bb3-562">الحل التلقائي</span><span class="sxs-lookup"><span data-stu-id="57bb3-562">Automatic resolution</span></span>

<span data-ttu-id="57bb3-563">لا يتوفر اي خيار لإصلاح هذه المشكلة تلقائيا.</span><span class="sxs-lookup"><span data-stu-id="57bb3-563">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="57bb3-564">الحل اليدوي</span><span class="sxs-lookup"><span data-stu-id="57bb3-564">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="57bb3-565">خيار 1</span><span class="sxs-lookup"><span data-stu-id="57bb3-565">Option 1</span></span>

<span data-ttu-id="57bb3-566">قم بإزالة علامة **ذاكرة التخزين المؤقت** من مصدر بيانات **المورد**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-566">Remove the **Cache** flag from the **Vendor** data source.</span></span> <span data-ttu-id="57bb3-567">سيصبح مصدر بيانات **FilteredVendor** قابلاً للتنفيذ حينئذٍ، ولكن سيتم الوصول إلى مصدر بيانات **المورد** الذي تمت الإشارة إليه في جدول VendTable في كل مرة يتم فيها استدعاء مصدر بيانات **FilteredVendor**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-567">The **FilteredVendor** data source will then become executable, but the **Vendor** data source that is referred to in the VendTable table will be accessed every time that the **FilteredVendor** data source is called.</span></span>

#### <a name="option-2"></a><span data-ttu-id="57bb3-568">خيار 2</span><span class="sxs-lookup"><span data-stu-id="57bb3-568">Option 2</span></span>

<span data-ttu-id="57bb3-569">قم بتغيير التعبير الخاص بمصدر بيانات **FilteredVendor** من `FILTER(Vendor, Vendor.AccountNum="US-101")`إلى `WHERE(Vendor, Vendor.AccountNum="US-101")`.</span><span class="sxs-lookup"><span data-stu-id="57bb3-569">Change the expression of the **FilteredVendor** data source from `FILTER(Vendor, Vendor.AccountNum="US-101")` to `WHERE(Vendor, Vendor.AccountNum="US-101")`.</span></span> <span data-ttu-id="57bb3-570">في هذه الحالة، سيتم الوصول إلى مصدر بيانات **المورد** المشار إليه في جدول VendTable فقط أثناء الاستدعاء الأول لمصدر بيانات **المورد**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-570">In this case, the **Vendor** data source that is referred to in the VendTable table will be accessed only during the first call of the **Vendor** data source.</span></span> <span data-ttu-id="57bb3-571">ومع ذلك، سيتم إجراء تحديد السجلات في الذاكرة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-571">However, the selection of records will be done in memory.</span></span> <span data-ttu-id="57bb3-572">لذلك، يمكن ان يتسبب هذا الأسلوب في ضعف الأداء.</span><span class="sxs-lookup"><span data-stu-id="57bb3-572">Therefore, this approach can cause poor performance.</span></span>

## <a name="missing-binding"></a><a id="i11"></a><span data-ttu-id="57bb3-573">الربط مفقود</span><span class="sxs-lookup"><span data-stu-id="57bb3-573">Missing binding</span></span>

<span data-ttu-id="57bb3-574">عند تكوين مكون التنسيق الخاص بالتقارير الإلكترونية، يتم عرض نموذج البيانات الأساسي الخاص بالتقارير الإلكترونية كمصدر بيانات افتراضي لتنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="57bb3-574">When you configure an ER format component, the base ER data model is offered as a default data source for the ER format.</span></span> <span data-ttu-id="57bb3-575">عند تشغيل التنسيق المكون لالتقارير الإلكترونية، يتم استخدام [تعيين النموذج الافتراضي](er-country-dependent-model-mapping.md) للنموذج الأساسي لتعبئة نموذج البيانات ببيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="57bb3-575">When the configured ER format is run, the [default model mapping](er-country-dependent-model-mapping.md) for the base model is used to fill the data model with application data.</span></span> <span data-ttu-id="57bb3-576">يعرض مصمم التنسيق الخاص بالتقارير الإلكترونية تحذيرا إذا قمت بربط عنصر تنسيق بعنصر نموذج بيانات غير مرتبط بأي مصدر بيانات في تعيين النموذج المحدد حاليا كتعيين نموذج افتراضي للتنسيق القابل للتحرير.</span><span class="sxs-lookup"><span data-stu-id="57bb3-576">The ER format designer shows a warning if you bind a format element to a data model item that isn't bound to any data source in the model-mapping that is currently selected as the default model-mapping for the editable format.</span></span> <span data-ttu-id="57bb3-577">لا يمكن تشغيل هذا النوع من الربط في وقت التشغيل، لان التنسيق الذي يتم تشغيله لا يمكنه تعبئة عنصر مرتبط ببيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="57bb3-577">This type of binding can't be run at runtime, because the format that runs can't fill a bound element with application data.</span></span> <span data-ttu-id="57bb3-578">ولذلك، يحدث خطأ في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="57bb3-578">Therefore, an error occurs at runtime.</span></span>

<span data-ttu-id="57bb3-579">توضح الخطوات التالية كيفيه حدوث هذه المشكلة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-579">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="57bb3-580">ابدأ في تكوين نموذج بيانات التقارير الإلكترونية وتعيين نموذج التقارير الإلكترونية ومكونات تنسيق التقارير الإلكترونية في وقت واحد.</span><span class="sxs-lookup"><span data-stu-id="57bb3-580">Start to configure the ER data model, the ER model-mapping, and the ER format components simultaneously.</span></span>
2. <span data-ttu-id="57bb3-581">في شجرة نموذج البيانات، قم باضافه العنصر الجذر المسمى **الجذر 3**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-581">In the data model tree, add a root item that is named **Root3**.</span></span>
3. <span data-ttu-id="57bb3-582">قم بتعديل عنصر **الجذر 3** عن طريق إضافة عنصر متداخل جديد من نوع **قائمة السجلات**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-582">Modify the **Root3** item by adding a new nested item of the **Record list** type.</span></span>
4. <span data-ttu-id="57bb3-583">قم بتسمية العنصر المتداخل الجديد **المورد**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-583">Name the new nested item **Vendor**.</span></span>
5. <span data-ttu-id="57bb3-584">قم بتعديل عنصر **المورد** بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="57bb3-584">Modify the **Vendor** item in the following way:</span></span>

    - <span data-ttu-id="57bb3-585">أضف حقلاً متداخلاً من نوع **السلسلة**، وقم بتسميته بـ **اسم**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-585">Add a nested field of the **String** type, and name it **Name**.</span></span>
    - <span data-ttu-id="57bb3-586">أضف حقلاً متداخلاً من نوع **السلسلة**، وقم بتسميته بـ **AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-586">Add a nested field of the **String** type, and name it **AccountNumber**.</span></span>

    ![إضافة حقول متداخلة إلى عنصر المورد في صفحة نموذج البيانات](./media/er-components-inspections-11a.png)

6. <span data-ttu-id="57bb3-588">في جزء مصادر بيانات تعيين النموذج، أضف مصدر بيانات من نوع **Dynamics 365 for Operations \\ سجلات الجداول**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-588">In the model-mapping data sources pane, add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
7. <span data-ttu-id="57bb3-589">قم بتسمية مصدر البيانات الجديد **المورد**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-589">Name the new data source **Vendor**.</span></span> <span data-ttu-id="57bb3-590">في حقل **الجدول**، حدد **VendTable** لتحديد أن مصدر البيانات سيطلب الجدول VendTable.</span><span class="sxs-lookup"><span data-stu-id="57bb3-590">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
8. <span data-ttu-id="57bb3-591">أضف مصدر بيانات من نوع **عام \\ معلمة إدخال المستخدم** للاستعلام عن حساب مورد في مربع حوار وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="57bb3-591">Add a data source of the **General \\ User input parameter** type to inquire about a vendor account in the runtime dialog box.</span></span>
<span data-ttu-id="57bb3-592">9 قم بتسمية مصدر البيانات الجديد **RequestedAccountNum**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-592">9 Name the new data source **RequestedAccountNum**.</span></span> <span data-ttu-id="57bb3-593">في حقل **التسمية**، أدخل **رقم حساب المورد**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-593">In the **Label** field, enter **Vendor account number**.</span></span> <span data-ttu-id="57bb3-594">في حقل **اسم نوع بيانات Operations**، اترك القيمة الافتراضية، وهي **الوصف**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-594">In the **Operations data type name** field, leave the default value, **Description**.</span></span>
10. <span data-ttu-id="57bb3-595">أضف مصدر بيانات من نوع **الحقل المحسوب** لتصفية مورد تم الاستعلام عنه.</span><span class="sxs-lookup"><span data-stu-id="57bb3-595">Add a data source of the **Calculated field** type to filter a vendor that is inquired about.</span></span>
11. <span data-ttu-id="57bb3-596">قم بتسميه مصدر البيانات الجديد **FilteredVendor**، وقم بتكوينه بحيث يحتوي علي التعبير `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.</span><span class="sxs-lookup"><span data-stu-id="57bb3-596">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.</span></span>
12. <span data-ttu-id="57bb3-597">اربط عناصر نموذج البيانات بمصادر البيانات التي تم تكوينها بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="57bb3-597">Bind the data model items to configured data sources in the following way:</span></span>

    - <span data-ttu-id="57bb3-598">اربط **FilteredVendor** بـ **المورد**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-598">Bind **FilteredVendor** to **Vendor**.</span></span>
    - <span data-ttu-id="57bb3-599">اربط **FilteredVendor.AccountNum** بـ **Vendor.AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-599">Bind **FilteredVendor.AccountNum** to **Vendor.AccountNumber**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="57bb3-600">يبقى حقل نموذج بيانات **Vendor.Name** غير مرتبط.</span><span class="sxs-lookup"><span data-stu-id="57bb3-600">The **Vendor.Name** data model field remains unbound.</span></span>

    ![عناصر نموذج البيانات المرتبطة بمصادر البيانات المكونة وعنصر وضع البيانات الموجود في صفحة مصمم تعيين النموذج](./media/er-components-inspections-11b.png)

13. <span data-ttu-id="57bb3-602">في شجرة هيكل التنسيق، أضف العناصر التالية لإنشاء مستند صادر بتنسيق XML يحتوي على تفاصيل البائعين الذين يتم الاستفسار عنهم:</span><span class="sxs-lookup"><span data-stu-id="57bb3-602">In the format structure tree, add the following items to generate an outbound document in XML format that contains the details of the vendors that are inquired about:</span></span>

    1. <span data-ttu-id="57bb3-603">أضف عنصر XML الخاص بجذر **العبارة**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-603">Add the **Statement** root XML element.</span></span>
    2. <span data-ttu-id="57bb3-604">بالنسبة إلى عنصر XML لـ **العبارة**، أضف عنصر XML لـ **الطرف** المتداخل.</span><span class="sxs-lookup"><span data-stu-id="57bb3-604">For the **Statement** XML element, add the nested **Party** XML element.</span></span>
    3. <span data-ttu-id="57bb3-605">بالنسبة لعناصر XML **للطرف**، أضف سمات XML المتداخلة التالية:</span><span class="sxs-lookup"><span data-stu-id="57bb3-605">For the **Party** XML element, add the following nested XML attributes:</span></span>

        - <span data-ttu-id="57bb3-606">الاسم</span><span class="sxs-lookup"><span data-stu-id="57bb3-606">Name</span></span>
        - <span data-ttu-id="57bb3-607">AccountNum</span><span class="sxs-lookup"><span data-stu-id="57bb3-607">AccountNum</span></span>

14. <span data-ttu-id="57bb3-608">ربط عناصر التنسيق بمصادر البيانات المتوفرة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="57bb3-608">Bind the format elements to provided data sources in the following way:</span></span>

    - <span data-ttu-id="57bb3-609">اربط عنصر تنسيق **الكشف\\الطرف** بعنصر مصدر بيانات `model.Vendor`.</span><span class="sxs-lookup"><span data-stu-id="57bb3-609">Bind the **Statement\\Party** format element to the `model.Vendor` data source item.</span></span>
    - <span data-ttu-id="57bb3-610">اربط عنصر تنسيق **العبارة\\الطرف\\الاسم** بحقل مصدر البيانات **model.Vendor.Name**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-610">Bind the **Statement\\Party\\Name** format element to the **model.Vendor.Name** data source field.</span></span>
    - <span data-ttu-id="57bb3-611">اربط عنصر تنسيق **العبارة\\الطرف\\AccountNum** بحقل مصدر البيانات **model.Vendor.AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-611">Bind the **Statement\\Party\\AccountNum** format element to the **model.Vendor.AccountNumber** data source field.</span></span>

15. <span data-ttu-id="57bb3-612">حدد **التحقق من الصحة** لفحص مكون التنسيق القابل للتحرير في صفحة **مصمم التنسيق**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-612">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![التحقق من صحة مكون تنسيق التقارير الإلكترونية في صفحة "مصمم التنسيق"](./media/er-components-inspections-11c.png)

16. <span data-ttu-id="57bb3-614">لاحظ حدوث تحذير في التحقق من الصحة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-614">Notice that a validation warning occurs.</span></span> <span data-ttu-id="57bb3-615">وتنص الرسالة على أن حقل **model.Vendor.Name** غير مرتبط بأي مصدر بيانات في تعيين النموذج الذي تم تكوينه ليتم استخدامه بواسطة التنسيق.</span><span class="sxs-lookup"><span data-stu-id="57bb3-615">The message states that the **model.Vendor.Name** data source field isn't bound to any data source in the model-mapping that is configured to be used by the format.</span></span> <span data-ttu-id="57bb3-616">ولذلك، قد لا يتم ملء عنصر تنسيق **الكشف\\الطرف\\الاسم** في وقت التشغيل، وقد يحدث استثناء في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="57bb3-616">Therefore, the **Statement\\Party\\Name** format element might not be filled at runtime, and a runtime exception might occur.</span></span>

    ![التحقق من صحة مكون تنسيق التقارير الإلكترونية في صفحة "مصمم التنسيق"](./media/er-components-inspections-11d.png)

<span data-ttu-id="57bb3-618">يبين الرسم التوضيحي التالي خطا وقت التشغيل الذي يحدث إذا تجاهلت التحذير وحدد **تشغيل** لتشغيل التنسيق.</span><span class="sxs-lookup"><span data-stu-id="57bb3-618">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run the format.</span></span>

![تشغيل التنسيق القابل للتحرير علي صفحه مصمم التنسيق](./media/er-components-inspections-11e.png)

### <a name="automatic-resolution"></a><span data-ttu-id="57bb3-620">الحل التلقائي</span><span class="sxs-lookup"><span data-stu-id="57bb3-620">Automatic resolution</span></span>

<span data-ttu-id="57bb3-621">لا يتوفر اي خيار لإصلاح هذه المشكلة تلقائيا.</span><span class="sxs-lookup"><span data-stu-id="57bb3-621">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="57bb3-622">الحل اليدوي</span><span class="sxs-lookup"><span data-stu-id="57bb3-622">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="57bb3-623">خيار 1</span><span class="sxs-lookup"><span data-stu-id="57bb3-623">Option 1</span></span>

<span data-ttu-id="57bb3-624">قم بتعديل تعيين النموذج الذي تم تكوينه عن طريق إضافة ربط لحقل مصدر بيانات **model.Vendor.Name**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-624">Modify the configured model-mapping by adding a binding for the **model.Vendor.Name** data source field.</span></span>

#### <a name="option-2"></a><span data-ttu-id="57bb3-625">خيار 2</span><span class="sxs-lookup"><span data-stu-id="57bb3-625">Option 2</span></span>

<span data-ttu-id="57bb3-626">قم بتعديل التنسيق الذي تم تكوينه عن طريق إزالة ربط لعنصر تنسيق **الكشف\\الطرف\\الاسم**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-626">Modify the configured format by removing a binding for the **Statement\\Party\\Name** format element.</span></span>

## <a name="not-linked-template"></a><a id="i12"></a><span data-ttu-id="57bb3-627">قالب غير مرتبط</span><span class="sxs-lookup"><span data-stu-id="57bb3-627">Not linked template</span></span>

<span data-ttu-id="57bb3-628">عند قيامك [يدويًا](er-fillable-excel.md#manual-entry) بتكوين مكون التنسيق الخاص بالتقارير الإلكترونية لاستخدام قالب لإنشاء مستند صادر، يجب عليك إضافة عنصر **ملف\\Excel**، وأضف القالب المطلوب كمرفق للمكون القابل للتحرير، وحدد ذلك المرفق في عنصر **ملف\\Excel**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-628">When you [manually](er-fillable-excel.md#manual-entry) configure an ER format component to use a template to generate an outbound document, you must manually add the **Excel\\File** element, add the required template as an attachment of the editable component, and select that attachment in the added **Excel\\File** element.</span></span> <span data-ttu-id="57bb3-629">بهذه الطريقة، تشير إلى أن العنصر المضاف سوف يملأ القالب المحدد في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="57bb3-629">In this way, you indicate that the added element will fill the selected template at runtime.</span></span> <span data-ttu-id="57bb3-630">عند تكوين إصدار مكون تنسيق في **حالة** [مسودة](general-electronic-reporting.md#component-versioning)، يمكنك إضافة عدة قوالب إلى المكون القابل للتحرير، ثم حدد كل قالب في عنصر **ملف\\Excel** لتشغيل تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="57bb3-630">When you configure a format component version in **Draft** [status](general-electronic-reporting.md#component-versioning), you might add several templates to the editable component, and then select each template in the **Excel\\File** element to run the ER format.</span></span> <span data-ttu-id="57bb3-631">وبهذه الطريقة، يمكنك مشاهده كيفيه تعبئة القوالب المختلفة في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="57bb3-631">In this way, you can see how different templates are filled at runtime.</span></span> <span data-ttu-id="57bb3-632">إذا كان لديك قوالب غير محددة في أي عنصر من عناصر **ملف\\Excel**، يقوم مصمم تنسيق التقارير الإلكترونية بتحذيرك بأن هذه القوالب سيتم حذفها من إصدار مكون التنسيق القابل للتحرير للتقارير الإلكترونية عند تغيير حالتها من **مسودة** إلى **مكتملة**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-632">If you have templates that aren't selected in any **Excel\\File** elements, the ER format designer warns you that those templates will be deleted from the editable ER format component version when its status is changed from **Draft** to **Completed**.</span></span>

<span data-ttu-id="57bb3-633">توضح الخطوات التالية كيفيه حدوث هذه المشكلة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-633">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="57bb3-634">ابدأ بتكوين مكون تعيين تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="57bb3-634">Start to configure the ER format component.</span></span>
2. <span data-ttu-id="57bb3-635">في شجرة بنية التنسيق، أضف عنصر **ملف\\Excel**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-635">In the format structure tree, add the **Excel\\File** element.</span></span>
3. <span data-ttu-id="57bb3-636">بالنسبة لعنصر **ملف\\Excel** الذي أضفته للتو، أضف ملف مصنف Excel، **A.xlsx**، كمرفق.</span><span class="sxs-lookup"><span data-stu-id="57bb3-636">For the **Excel\\File** element that you just added, add an Excel workbook file, **A.xlsx**, as an attachment.</span></span> <span data-ttu-id="57bb3-637">استخدم نوع المستند الذي تم تكوينه في [معلمات التقارير الإلكترونية](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) لتحديد تخزين قوالب تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="57bb3-637">Use the document type that is configured in the [ER parameters](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) to specify the storage of ER format templates.</span></span>
4. <span data-ttu-id="57bb3-638">بالنسبة لعنصر **ملف\\Excel**، أضف ملف مصنف Excel آخر، **B.xlsx**، كمرفق.</span><span class="sxs-lookup"><span data-stu-id="57bb3-638">For the **Excel\\File** element, add another Excel workbook file, **B.xlsx**, as an attachment.</span></span> <span data-ttu-id="57bb3-639">استخدم نفس نوع المستند المستخدم لملف المصنف A.</span><span class="sxs-lookup"><span data-stu-id="57bb3-639">Use the same document type that is used for workbook file A.</span></span>
5. <span data-ttu-id="57bb3-640">في عنصر **ملف\\Excel**، حدد ملف المصنف A.</span><span class="sxs-lookup"><span data-stu-id="57bb3-640">In the **Excel\\File** element, select workbook file A.</span></span>
6. <span data-ttu-id="57bb3-641">حدد **التحقق من الصحة** لفحص مكون التنسيق القابل للتحرير في صفحة **مصمم التنسيق**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-641">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![التحقق من صحة مكون التنسيق القابل للتحرير لملف المصنف في صفحة "مصمم التنسيق"](./media/er-components-inspections-12a.gif)

7. <span data-ttu-id="57bb3-643">لاحظ حدوث تحذير في التحقق من الصحة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-643">Notice that a validation warning occurs.</span></span> <span data-ttu-id="57bb3-644">توضح الرسالة أن ملف المصنف **B.xlsx** غير مرتبط بأي مكونات، وأنه ستتم إزالته بعد تغيير حالة إصدار التكوين.</span><span class="sxs-lookup"><span data-stu-id="57bb3-644">The message states that workbook file **B.xlsx** isn't linked to any components, and that it will be removed after the status of the configuration version is changed.</span></span>

### <a name="automatic-resolution"></a><span data-ttu-id="57bb3-645">الحل التلقائي</span><span class="sxs-lookup"><span data-stu-id="57bb3-645">Automatic resolution</span></span>

<span data-ttu-id="57bb3-646">لا يتوفر اي خيار لإصلاح هذه المشكلة تلقائيا.</span><span class="sxs-lookup"><span data-stu-id="57bb3-646">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="57bb3-647">الحل اليدوي</span><span class="sxs-lookup"><span data-stu-id="57bb3-647">Manual resolution</span></span>

<span data-ttu-id="57bb3-648">قم بتعديل التنسيق الذي تم تكوينه عن طريق إزالة جميع القوالب غير المرتبطة بأي عنصر **ملف\\Excel**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-648">Modify the configured format by removing all templates that aren't linked to any **Excel\\File** element.</span></span>

## <a name="not-synced-format"></a><a id="i13"></a><span data-ttu-id="57bb3-649">تنسيق غير متزامن</span><span class="sxs-lookup"><span data-stu-id="57bb3-649">Not synced format</span></span>

<span data-ttu-id="57bb3-650">عند قيامك [بتكوين](er-fillable-excel.md) مكون تنسيق التقارير الإلكترونية لاستخدام قالب Excel لإنشاء مستند صادر، يمكنك إضافة عنصر **ملف\\Excel** يدويًا، وأضف القالب المطلوب كمرفق للمكون القابل للتحرير، وحدد ذلك المرفق في عنصر **ملف\\Excel**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-650">When you [configure](er-fillable-excel.md) an ER format component to use an Excel template to generate an outbound document, you can manually add the **Excel\\File** element, add the required template as an attachment of the editable component, and select that attachment in the added **Excel\\File** element.</span></span> <span data-ttu-id="57bb3-651">بهذه الطريقة، تشير إلى أن العنصر المضاف سوف يملأ القالب المحدد في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="57bb3-651">In this way, you indicate that the added element will fill the selected template at runtime.</span></span> <span data-ttu-id="57bb3-652">نظرًا لأنه تم تصميم قالب Excel المضاف خارجيًا، فقد يحتوي تنسيق التقارير الإلكترونية القابل للتحرير على أسماء Excel مفقودة من القالب المضاف.</span><span class="sxs-lookup"><span data-stu-id="57bb3-652">Because the added Excel template has been externally designed, the editable ER format might contain Excel names that are missing from the added template.</span></span> <span data-ttu-id="57bb3-653">يحذرك مصمم تنسيق التقارير الإلكترونية من أي تناقضات بين خصائص عناصر تنسيق التقارير الإلكترونية التي تشير إلى الأسماء غير المضمنة في قالب Excel المضاف.</span><span class="sxs-lookup"><span data-stu-id="57bb3-653">The ER format designer warns you about any inconsistencies between the properties of the ER format elements that refer to names that aren't included in the added Excel template.</span></span>

<span data-ttu-id="57bb3-654">توضح الخطوات التالية كيفيه حدوث هذه المشكلة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-654">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="57bb3-655">ابدأ بتكوين مكون تعيين تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="57bb3-655">Start to configure the ER format component.</span></span>
2. <span data-ttu-id="57bb3-656">في شجرة بنية التنسيق، أضف عنصر **ملف\\Excel** **التقرير**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-656">In the format structure tree, add the **Excel\\File** element **Report**.</span></span>
3. <span data-ttu-id="57bb3-657">بالنسبة لعنصر **ملف\\Excel** الذي أضفته للتو، أضف ملف مصنف Excel، **A.xlsx**، كمرفق.</span><span class="sxs-lookup"><span data-stu-id="57bb3-657">For the **Excel\\File** element that you just added, add an Excel workbook file, **A.xlsx**, as an attachment.</span></span> <span data-ttu-id="57bb3-658">استخدم نوع المستند الذي تم تكوينه في [معلمات التقارير الإلكترونية](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) لتحديد تخزين قوالب تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="57bb3-658">Use the document type that is configured in the [ER parameters](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) to specify the storage of ER format templates.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="57bb3-659">تأكد من أن مصنف Excel المضاف لا يحتوي على الاسم **ReportTitle**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-659">Make sure that the added Excel workbook doesn't contain the name **ReportTitle**.</span></span>

4. <span data-ttu-id="57bb3-660">أضف عنصر **خلية\\Excel** التالي **العنوان** باعتباره العنصر المتداخل لعنصر **التقرير**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-660">Add the following **Excel\\Cell** element **Title** as the nested element of the **Report** element.</span></span> <span data-ttu-id="57bb3-661">في حقل **نطاق Excel**، أدخل **ReportTitle**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-661">In the **Excel range** field, enter **ReportTitle**.</span></span>
5. <span data-ttu-id="57bb3-662">حدد **التحقق من الصحة** لفحص مكون التنسيق القابل للتحرير في صفحة **مصمم التنسيق**.</span><span class="sxs-lookup"><span data-stu-id="57bb3-662">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![التحقق من صحة الحقول والعناصر المتداخلة في صفحة مصمم التنسيق](./media/er-components-inspections-13a.png)

6. <span data-ttu-id="57bb3-664">لاحظ حدوث تحذير في التحقق من الصحة.</span><span class="sxs-lookup"><span data-stu-id="57bb3-664">Notice that a validation warning occurs.</span></span> <span data-ttu-id="57bb3-665">تشير الرسالة إلى أن الاسم **ReportTitle** غير موجود في الورقة **Sheet1** الخاصة بقالب Excel الذي تستخدمه.</span><span class="sxs-lookup"><span data-stu-id="57bb3-665">The message states that the name **ReportTitle** doesn't exist on sheet **Sheet1** of the Excel template that you're using.</span></span>

    ![تحذير التحقق من الصحة بأن الاسم ReportTitle غير موجود في Sheet1 الخاصة بقالب Excel](./media/er-components-inspections-13b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="57bb3-667">الحل التلقائي</span><span class="sxs-lookup"><span data-stu-id="57bb3-667">Automatic resolution</span></span>

<span data-ttu-id="57bb3-668">لا يتوفر اي خيار لإصلاح هذه المشكلة تلقائيا.</span><span class="sxs-lookup"><span data-stu-id="57bb3-668">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="57bb3-669">الحل اليدوي</span><span class="sxs-lookup"><span data-stu-id="57bb3-669">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="57bb3-670">خيار 1</span><span class="sxs-lookup"><span data-stu-id="57bb3-670">Option 1</span></span>

<span data-ttu-id="57bb3-671">قم بتعديل التنسيق الذي تم تكوينه عن طريق إزالة جميع العناصر التي تشير إلى أسماء Excel المفقودة من القالب.</span><span class="sxs-lookup"><span data-stu-id="57bb3-671">Modify the configured format by removing all elements that refer to Excel names that are missing from the template.</span></span>

#### <a name="option-2"></a><span data-ttu-id="57bb3-672">خيار 2</span><span class="sxs-lookup"><span data-stu-id="57bb3-672">Option 2</span></span>

<span data-ttu-id="57bb3-673">[قم بتحديث](er-fillable-excel.md#template-import) تنسيق التقارير الإلكترونية القابلة للتحرير عن طريق استيراد قالب Excel.</span><span class="sxs-lookup"><span data-stu-id="57bb3-673">[Update](er-fillable-excel.md#template-import) the editable ER format by importing an Excel template.</span></span> <span data-ttu-id="57bb3-674">بنية تنسيق التقارير الإلكترونية القابلة للتحرير ستتم [مزامنتها](modify-electronic-reporting-format-reapply-excel-template.md) ببنية قالب Excel المستورد.</span><span class="sxs-lookup"><span data-stu-id="57bb3-674">The structure of the editable ER format will be [synced](modify-electronic-reporting-format-reapply-excel-template.md) with the structure of the imported Excel template.</span></span>

### <a name="additional-consideration"></a><span data-ttu-id="57bb3-675">الاعتبار الإضافي</span><span class="sxs-lookup"><span data-stu-id="57bb3-675">Additional consideration</span></span>

<span data-ttu-id="57bb3-676">لمعرفة كيف يمكن مزامنة بنية التنسيق مع قالب تقارير إلكترونية في محرر القالب الخاص بـ [إدارة مستندات الأعمال](er-business-document-management.md)، راجع [تحديث بنية قالب مستند الأعمال](er-bdm-update-structure.md).</span><span class="sxs-lookup"><span data-stu-id="57bb3-676">To learn how the format structure can be synced with an ER template in the template editor of [Business document management](er-business-document-management.md), see [Update the structure of a business document template](er-bdm-update-structure.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="57bb3-677">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="57bb3-677">Additional resources</span></span>

[<span data-ttu-id="57bb3-678">ALLITEMS ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="57bb3-678">ALLITEMS ER function</span></span>](er-functions-list-allitems.md)

[<span data-ttu-id="57bb3-679">ALLITEMSQUERY ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="57bb3-679">ALLITEMSQUERY ER function</span></span>](er-functions-list-allitemsquery.md)

[<span data-ttu-id="57bb3-680">INT64VALUE ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="57bb3-680">INT64VALUE ER function</span></span>](er-functions-conversion-int64value.md)

[<span data-ttu-id="57bb3-681">وظيفة INTVALUE ER  </span><span class="sxs-lookup"><span data-stu-id="57bb3-681">INTVALUE ER function</span></span>](er-functions-conversion-intvalue.md)

[<span data-ttu-id="57bb3-682">FILTER ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="57bb3-682">FILTER ER function</span></span>](er-functions-list-filter.md)

[<span data-ttu-id="57bb3-683">WHERE ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="57bb3-683">WHERE ER function</span></span>](er-functions-list-where.md)

[<span data-ttu-id="57bb3-684">استخدم مصادر بيانات JOIN للحصول على البيانات من جداول التطبيقات المتعددة في تعيينات نماذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="57bb3-684">Use JOIN data sources to get data from multiple application tables in ER model mappings</span></span>](er-join-data-sources.md)

[<span data-ttu-id="57bb3-685">تتبع تنفيذ تنسيقات التقارير الإلكترونية لاستكشاف مشكلات الأداء وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="57bb3-685">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)

[<span data-ttu-id="57bb3-686">نظرة عامة على إدارة مستندات الأعمال</span><span class="sxs-lookup"><span data-stu-id="57bb3-686">Business document management overview</span></span>](er-business-document-management.md)
