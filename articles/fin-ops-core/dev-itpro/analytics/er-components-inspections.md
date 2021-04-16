---
title: فحص مكون التقارير الإلكترونية الذي تم تكوينه لمنع مشكلات وقت التشغيل
description: يشرح هذا الموضوع كيفية فحص مكونات التقارير الإلكترونية (التقارير الإلكترونية) المكونة لمنع مشكلات وقت التشغيل التي قد تحدث.
author: NickSelin
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: d164dfe10c9736d8b4529a32ffba765f94ad37d9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753830"
---
# <a name="inspect-the-configured-er-component-to-prevent-runtime-issues"></a><span data-ttu-id="a2847-103">فحص مكون التقارير الإلكترونية الذي تم تكوينه لمنع مشكلات وقت التشغيل</span><span class="sxs-lookup"><span data-stu-id="a2847-103">Inspect the configured ER component to prevent runtime issues</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a2847-104">كل [تنسيق تقرير إلكتروني (التقارير الإلكترونية)](general-electronic-reporting.md) [تم تكوينه](general-electronic-reporting.md#FormatComponentOutbound) و[تعيين النموذج](general-electronic-reporting.md#data-model-and-model-mapping-components) يمكن [التحقق منه](er-fillable-excel.md#validate-an-er-format) في وقت التصميم.</span><span class="sxs-lookup"><span data-stu-id="a2847-104">Every configured [Electronic reporting (ER)](general-electronic-reporting.md) [format](general-electronic-reporting.md#FormatComponentOutbound) and [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) component can be [validated](er-fillable-excel.md#validate-an-er-format) at design time.</span></span> <span data-ttu-id="a2847-105">أثناء هذا التحقق من الصحة، يتم إجراء فحص تناسق للمساعدة في منع مشكلات وقت التشغيل التي قد تحدث، مثل أخطاء التنفيذ وتدهور الأداء.</span><span class="sxs-lookup"><span data-stu-id="a2847-105">During this validation, a consistency check runs to help prevent runtime issues that might occur, such as execution errors and performance degradation.</span></span> <span data-ttu-id="a2847-106">لكل مشكله تم العثور عليها، يتم توفير مسار العنصر المتسبب في حدوث مشكلات.</span><span class="sxs-lookup"><span data-stu-id="a2847-106">For every issue that is found, the check provides the path of a problematic element.</span></span> <span data-ttu-id="a2847-107">بالنسبة لبعض المشكلات، يتوفر إصلاح تلقائي.</span><span class="sxs-lookup"><span data-stu-id="a2847-107">For some issues, an automatic fix is available.</span></span>

<span data-ttu-id="a2847-108">بشكل افتراضي، يتم تطبيق التحقق تلقائيًا في الحالات التالية لتكوين التقارير الإلكترونية الذي يحتوي على مكونات التقارير الإلكترونية المذكورة سابقًا:</span><span class="sxs-lookup"><span data-stu-id="a2847-108">By default, the validation is automatically applied in the following cases for an ER configuration that contains the previously mentioned ER components:</span></span>

- <span data-ttu-id="a2847-109">يمكنك [استيراد](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) إصدار [جديد](general-electronic-reporting.md#component-versioning)من تكوين التقارير الإلكترونية إلى مثيل Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="a2847-109">You [import](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) a new [version](general-electronic-reporting.md#component-versioning) of an ER configuration into your instance of Microsoft Dynamics 365 Finance.</span></span>
- <span data-ttu-id="a2847-110">وتقوم بتغيير [حالة](general-electronic-reporting.md#component-versioning) تكوين التقارير الإلكتروني القابل للتحرير من **مسودة** إلى **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="a2847-110">You change the [status](general-electronic-reporting.md#component-versioning) of the editable ER configuration from **Draft** to **Completed**.</span></span>
- <span data-ttu-id="a2847-111">يمكنك [إعادة تعريف](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase) تكوين تقارير إلكترونية قابل للتحرير عن طريق استخدام إصدار أساسي جديد.</span><span class="sxs-lookup"><span data-stu-id="a2847-111">You [rebase](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase) an editable ER configuration by applying a new base version.</span></span>

<span data-ttu-id="a2847-112">يمكنك تشغيل هذا التحقق بشكل صريح.</span><span class="sxs-lookup"><span data-stu-id="a2847-112">You can explicitly run this validation.</span></span> <span data-ttu-id="a2847-113">حدد أحد الخيارات الثلاثة التالية، واتبع الخطوات المتوفرة:</span><span class="sxs-lookup"><span data-stu-id="a2847-113">Select one of the following three options, and follow the steps that are provided:</span></span>

- <span data-ttu-id="a2847-114">الخيار 1:</span><span class="sxs-lookup"><span data-stu-id="a2847-114">Option 1:</span></span>

    1. <span data-ttu-id="a2847-115">انتقل إلى **إدارة المؤسسة \> التقارير الإلكترونية \> التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="a2847-115">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
    2. <span data-ttu-id="a2847-116">في شجره التكوينات الموجودة في الجزء الأيمن، حدد تكوين التقارير الإلكترونية المطلوب الذي يحتوي علي التنسيق الخاص ب التقارير الإلكترونية أو مكون تعيين نموذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a2847-116">In the configurations tree in the left pane, select the desired ER configuration that contains the ER format or ER model mapping component.</span></span>
    3. <span data-ttu-id="a2847-117">على علامة التبويب السريعة **إصدارات**، حدد الإصدار المطلوب لتكوين التقارير الإلكترونية المحدد.</span><span class="sxs-lookup"><span data-stu-id="a2847-117">On the **Versions** FastTab, select the desired version of the selected ER configuration.</span></span>
    4. <span data-ttu-id="a2847-118">في جزء الإجراءات، حدد **التحقق**.</span><span class="sxs-lookup"><span data-stu-id="a2847-118">On the Action Pane, select **Validate**.</span></span>

- <span data-ttu-id="a2847-119">الخيار 2، لتنسيق التقارير الإلكترونية:</span><span class="sxs-lookup"><span data-stu-id="a2847-119">Option 2, for an ER format:</span></span>

    1. <span data-ttu-id="a2847-120">انتقل إلى **إدارة المؤسسة \> التقارير الإلكترونية \> التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="a2847-120">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
    2. <span data-ttu-id="a2847-121">في شجره التكوينات الموجودة في الجزء الأيمن، حدد تكوين التقارير الإلكترونية المطلوب الذي يحتوي على مكون تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a2847-121">In the configurations tree in the left pane, select the desired ER configuration that contains the ER format component.</span></span>
    3. <span data-ttu-id="a2847-122">على علامة التبويب السريعة **إصدارات**، حدد الإصدار المطلوب لتكوين التقارير الإلكترونية المحدد.</span><span class="sxs-lookup"><span data-stu-id="a2847-122">On the **Versions** FastTab, select the desired version of the selected ER configuration.</span></span>
    4. <span data-ttu-id="a2847-123">في جزء الإجراءات، حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="a2847-123">On the Action Pane, select **Designer**.</span></span>
    5. <span data-ttu-id="a2847-124">في صفحة **مصمم التنسيق**، في جزء الإجراءات، حدد **تحقق من الصحة**.</span><span class="sxs-lookup"><span data-stu-id="a2847-124">On the **Format designer** page, on the Action Pane, select **Validate**.</span></span>

- <span data-ttu-id="a2847-125">الخيار 3، لتعيين نموذج التقارير الإلكترونية:</span><span class="sxs-lookup"><span data-stu-id="a2847-125">Option 3, for an ER model mapping:</span></span>

    1. <span data-ttu-id="a2847-126">انتقل إلى **إدارة المؤسسة \> التقارير الإلكترونية \> التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="a2847-126">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
    2. <span data-ttu-id="a2847-127">في شجره التكوينات الموجودة في الجزء الأيمن، حدد تكوين التقارير الإلكترونية المطلوب الذي يحتوي على مكون تعيين نموذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a2847-127">In the configurations tree in the left pane, select the desired ER configuration that contains the ER model mapping component.</span></span>
    3. <span data-ttu-id="a2847-128">على علامة التبويب السريعة **إصدارات**، حدد الإصدار المطلوب لتكوين التقارير الإلكترونية المحدد.</span><span class="sxs-lookup"><span data-stu-id="a2847-128">On the **Versions** FastTab, select the desired version of the selected ER configuration.</span></span>
    4. <span data-ttu-id="a2847-129">في جزء الإجراءات، حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="a2847-129">On the Action Pane, select **Designer**.</span></span>
    5. <span data-ttu-id="a2847-130">في صفحة **تعيين النموذج إلى مصدر البيانات** في جزء الإجراءات، حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="a2847-130">On the **Model to datasource mapping** page, on the Action Pane, select **Designer**.</span></span>
    6. <span data-ttu-id="a2847-131">في صفحة **مصمم تعيين النموذج** في جزء الإجراءات، حدد **التحقق من الصحة**.</span><span class="sxs-lookup"><span data-stu-id="a2847-131">On the **Model mapping designer** page, on the Action Pane, select **Validate**.</span></span>

<span data-ttu-id="a2847-132">لتخطي التحقق من الصحة عند استيراد التكوين، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="a2847-132">To skip the validation when the configuration is imported, follow these steps.</span></span>

1. <span data-ttu-id="a2847-133">انتقل إلى **إدارة المؤسسة \> التقارير الإلكترونية \> التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="a2847-133">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="a2847-134">في صفحة **التكوينات**، في جزء الإجراءات، في علامة التبويب **التكوينات**، في مجموعة **الإعدادات المتقدمة**، حدد **معلمات المستخدمين**.</span><span class="sxs-lookup"><span data-stu-id="a2847-134">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="a2847-135">قم بتعيين الخيار **التحقق من صحة التكوين بعد الاستيراد** إلى **لا**.</span><span class="sxs-lookup"><span data-stu-id="a2847-135">Set the **Validate the configuration after importing** option to **No**.</span></span>

<span data-ttu-id="a2847-136">لتخطي عمليه التحقق من الصحة عند تغيير حاله الإصدار أو إعادة تعريفه، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="a2847-136">To skip the validation when you change or rebase the version's status, follow these steps.</span></span>

1. <span data-ttu-id="a2847-137">انتقل إلى **إدارة المؤسسة \> التقارير الإلكترونية \> التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="a2847-137">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="a2847-138">في صفحة **التكوينات**، في جزء الإجراءات، في علامة التبويب **التكوينات**، في مجموعة **الإعدادات المتقدمة**، حدد **معلمات المستخدمين**.</span><span class="sxs-lookup"><span data-stu-id="a2847-138">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="a2847-139">قم بتعيين خيار **تخطي التحقق من الصحة عند تغيير حاله التكوين وإعادة تعريفه** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="a2847-139">Set the **Skip validation at configuration's status change and rebase** option to **Yes**.</span></span>

<span data-ttu-id="a2847-140">يستخدم التقارير الإلكترونية الفئات التالية لتجميع عمليات فحص التناسق:</span><span class="sxs-lookup"><span data-stu-id="a2847-140">ER uses the following categories to group consistency check inspections:</span></span>

- <span data-ttu-id="a2847-141">**إمكانية التنفيذ** – عمليات فحص التي تكشف عن المشكلات الحرجة التي قد تحدث في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="a2847-141">**Executability** – Inspections that detect critical issues that might occur at runtime.</span></span> <span data-ttu-id="a2847-142">وغالبا ما تكون هذه المشكلات في مستوى **الخطأ**.</span><span class="sxs-lookup"><span data-stu-id="a2847-142">These issues are mostly at an **Error** level.</span></span> 
- <span data-ttu-id="a2847-143">**الأداء** – عمليات الفحص التي تكشف عن المشكلات التي قد تتسبب في تنفيذ غير فعال لمكونات التقارير الإلكترونية التي تم تكوينها.</span><span class="sxs-lookup"><span data-stu-id="a2847-143">**Performance** – Inspections that detect issues that might cause inefficient execution of configured ER components.</span></span> <span data-ttu-id="a2847-144">وغالبا ما تكون هذه المشكلات في مستوى **التحذير**.</span><span class="sxs-lookup"><span data-stu-id="a2847-144">These issues are mostly at a **Warning** level.</span></span>
- <span data-ttu-id="a2847-145">**تكامل البيانات** – عمليات الفحص التي تكشف عن المشكلات التي قد تتسبب في فقد البيانات أو مشكلات وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="a2847-145">**Data integrity** – Inspections that detect issues that might cause data loss or runtime issues.</span></span> <span data-ttu-id="a2847-146">وغالبا ما تكون هذه المشكلات في مستوى **التحذير**.</span><span class="sxs-lookup"><span data-stu-id="a2847-146">These issues are mostly at a **Warning** level.</span></span>

## <a name="list-of-inspections"></a><span data-ttu-id="a2847-147">قائمه عمليات الفحص</span><span class="sxs-lookup"><span data-stu-id="a2847-147">List of inspections</span></span>

<span data-ttu-id="a2847-148">يوفر الجدول التالي نظرة عامة على عمليات الفحص التي توفرها التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a2847-148">The following table provides an overview of the inspections that ER provides.</span></span> <span data-ttu-id="a2847-149">لمزيد من المعلومات حول عمليات الفحص هذه، استخدم الارتباطات الموجودة في العمود الأول للانتقال إلى الأقسام ذات الصلة لهذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="a2847-149">For more information about these inspections, use the links in the first column to go to the relevant sections of this topic.</span></span> <span data-ttu-id="a2847-150">توضح هذه المقاطع أنواع المكونات التي يوفرها التقارير الإلكترونية عمليات الفحص الخاصة بمكونات التقارير الإلكترونية وكيفيه أعاده تكوينها للمساعدة علي منع حدوث المشكلات.</span><span class="sxs-lookup"><span data-stu-id="a2847-150">Those sections explain the types of components that ER provides inspections for and how you can reconfigure ER components to help prevent issues.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a2847-151">الاسم</span><span class="sxs-lookup"><span data-stu-id="a2847-151">Name</span></span></th>
<th><span data-ttu-id="a2847-152">‏‏الفئة</span><span class="sxs-lookup"><span data-stu-id="a2847-152">Category</span></span></th>
<th><span data-ttu-id="a2847-153">المستوى</span><span class="sxs-lookup"><span data-stu-id="a2847-153">Level</span></span></th>
<th><span data-ttu-id="a2847-154">الرسالة</span><span class="sxs-lookup"><span data-stu-id="a2847-154">Message</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a2847-155"><a href='#i1'>نوع التحويل</a></span><span class="sxs-lookup"><span data-stu-id="a2847-155"><a href='#i1'>Type conversion</a></span></span></td>
<td><span data-ttu-id="a2847-156">إمكانية التنفيذ</span><span class="sxs-lookup"><span data-stu-id="a2847-156">Executability</span></span></td>
<td><span data-ttu-id="a2847-157">‏‏خطأ</span><span class="sxs-lookup"><span data-stu-id="a2847-157">Error</span></span></td>
<td>
<p><span data-ttu-id="a2847-158">لا يمكن تحويل التعبير من النوع &lt;type&gt;إلى حقل من نوع &lt;type&gt;.</span><span class="sxs-lookup"><span data-stu-id="a2847-158">Cannot convert expression of type &lt;type&gt; to field of type &lt;type&gt;.</span></span></p>
<p><span data-ttu-id="a2847-159"><b>خطأ في وقت التشغيل</b>: استثناء من نوع</span><span class="sxs-lookup"><span data-stu-id="a2847-159"><b>Runtime error:</b> Exception for type</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="a2847-160"><a href='#i2'>توافق النوع</a></span><span class="sxs-lookup"><span data-stu-id="a2847-160"><a href='#i2'>Type compatibility</a></span></span></td>
<td><span data-ttu-id="a2847-161">إمكانية التنفيذ</span><span class="sxs-lookup"><span data-stu-id="a2847-161">Executability</span></span></td>
<td><span data-ttu-id="a2847-162">‏‏خطأ</span><span class="sxs-lookup"><span data-stu-id="a2847-162">Error</span></span></td>
<td>
<p><span data-ttu-id="a2847-163">لا يمكن استخدام التعبير المكون كرابط لعنصر التنسيق الحالي إلى مصدر بيانات حيث يقوم هذا التعبير بإرجاع قيمه نوع البيانات &lt;النوع&gt; الذي يتجاوز نطاق أنواع البيانات المعتمدة من قبل عنصر التنسيق الحالي من نوع &lt;النوع&gt;.</span><span class="sxs-lookup"><span data-stu-id="a2847-163">The configured expression cannot be used as the binding of the current format element to a data source as this expression returns value of the data type &lt;type&gt; that is beyond the scope of data types that are supported by the current format element of type &lt;type&gt;.</span></span></p>
<p><span data-ttu-id="a2847-164"><b>خطأ في وقت التشغيل</b>: استثناء من نوع</span><span class="sxs-lookup"><span data-stu-id="a2847-164"><b>Runtime error:</b> Exception of type</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="a2847-165"><a href='#i3'>عنصر التكوين مفقود</a></span><span class="sxs-lookup"><span data-stu-id="a2847-165"><a href='#i3'>Missing configuration element</a></span></span></td>
<td><span data-ttu-id="a2847-166">إمكانية التنفيذ</span><span class="sxs-lookup"><span data-stu-id="a2847-166">Executability</span></span></td>
<td><span data-ttu-id="a2847-167">‏‏خطأ</span><span class="sxs-lookup"><span data-stu-id="a2847-167">Error</span></span></td>
<td>
<p><span data-ttu-id="a2847-168">لم يتم العثور على المسار &lt;المسار&gt;.</span><span class="sxs-lookup"><span data-stu-id="a2847-168">Path not found &lt;path&gt;.</span></span></p>
<p><span data-ttu-id="a2847-169"><b>خطأ في وقت التشغيل:</b> لم يتم العثور على عنصر &lt;مسار&gt; التكوين</span><span class="sxs-lookup"><span data-stu-id="a2847-169"><b>Runtime error:</b> Element of the configuration &lt;path&gt; not found</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="a2847-170"><a href='#i4'>إمكانية تنفيذ تعبير باستخدام وظيفة التصفية</a></span><span class="sxs-lookup"><span data-stu-id="a2847-170"><a href='#i4'>Executability of an expression with FILTER function</a></span></span></td>
<td><span data-ttu-id="a2847-171">إمكانية التنفيذ</span><span class="sxs-lookup"><span data-stu-id="a2847-171">Executability</span></span></td>
<td><span data-ttu-id="a2847-172">‏‏خطأ</span><span class="sxs-lookup"><span data-stu-id="a2847-172">Error</span></span></td>
<td>
<p><span data-ttu-id="a2847-173">قائمة تعبير وظيفة التصفية غير قابلة للاستعلام.</span><span class="sxs-lookup"><span data-stu-id="a2847-173">The list expression of FILTER function is not queryable.</span></span></p>
<p><span data-ttu-id="a2847-174"><b>خطأ في وقت التشغيل:</b> التصفية غير مدعومة.</span><span class="sxs-lookup"><span data-stu-id="a2847-174"><b>Runtime error:</b> Filtering is not supported.</span></span> <span data-ttu-id="a2847-175">تحقق من صحة التكوين للحصول على مزيد من التفاصيل حول ذلك.</span><span class="sxs-lookup"><span data-stu-id="a2847-175">Validate the configuration to get more details about this.</span></span></p>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="a2847-176"><a href='#i5'>إمكانية تنفيذ مصدر بيانات التجميع حسب</a></span><span class="sxs-lookup"><span data-stu-id="a2847-176"><a href='#i5'>Executability of a GROUPBY data source</a></span></span></td>
<td><span data-ttu-id="a2847-177">إمكانية التنفيذ</span><span class="sxs-lookup"><span data-stu-id="a2847-177">Executability</span></span></td>
<td><span data-ttu-id="a2847-178">‏‏خطأ</span><span class="sxs-lookup"><span data-stu-id="a2847-178">Error</span></span></td>
<td><span data-ttu-id="a2847-179">لا يدعم المسار &lt;المسار&gt; الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="a2847-179">Path &lt;path&gt; does not support querying.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2847-180">إمكانية التنفيذ</span><span class="sxs-lookup"><span data-stu-id="a2847-180">Executability</span></span></td>
<td><span data-ttu-id="a2847-181">‏‏خطأ</span><span class="sxs-lookup"><span data-stu-id="a2847-181">Error</span></span></td>
<td>
<p><span data-ttu-id="a2847-182">لا يمكن تنفيذ وظيفة "التجميع حسب" بواسطة الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="a2847-182">Group by function cannot be executed with query.</span></span></p>
<p><span data-ttu-id="a2847-183"><b>خطأ في وقت التشغيل:</b> لا يمكن تنفيذ وظيفة "التجميع حسب" باستخدام الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="a2847-183"><b>Runtime error:</b> Group by function can't be executed with query.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="a2847-184"><a href='#i6'>إمكانية تنفيذ مصدر بيانات الانضمام</a></span><span class="sxs-lookup"><span data-stu-id="a2847-184"><a href='#i6'>Executability of a JOIN data source</a></span></span></td>
<td><span data-ttu-id="a2847-185">إمكانية التنفيذ</span><span class="sxs-lookup"><span data-stu-id="a2847-185">Executability</span></span></td>
<td><span data-ttu-id="a2847-186">‏‏خطأ</span><span class="sxs-lookup"><span data-stu-id="a2847-186">Error</span></span></td>
<td>
<p><span data-ttu-id="a2847-187">لا يمكن الانضمام إلى &lt;مسار&gt; قائمة ليس عامل تصفية في الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="a2847-187">Cannot join a list &lt;path&gt; that is not a filter in query.</span></span></p>
<p><span data-ttu-id="a2847-188"><b>خطأ في وقت التشغيل:</b> يجب أن يكون مصدر البيانات المنضم للوظيفة عبارة عن حقل محسوب لتعبير عامل التصفية تم استدعاؤه بشكل غير صحيح.</span><span class="sxs-lookup"><span data-stu-id="a2847-188"><b>Runtime error:</b> Function Joined datasource should be a filter expression calculated field has been incorrectly called.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="a2847-189"><a href='#i7'>تفضيل وظيفة التصفية مقابل المكان</a></span><span class="sxs-lookup"><span data-stu-id="a2847-189"><a href='#i7'>Preferability of FILTER vs WHERE function</a></span></span></td>
<td><span data-ttu-id="a2847-190">الأداء</span><span class="sxs-lookup"><span data-stu-id="a2847-190">Performance</span></span></td>
<td><span data-ttu-id="a2847-191">تحذير</span><span class="sxs-lookup"><span data-stu-id="a2847-191">Warning</span></span></td>
<td><span data-ttu-id="a2847-192">يفضل استخدام وظيفة التصفية للتعبير عن المكان من منظور الأداء.</span><span class="sxs-lookup"><span data-stu-id="a2847-192">Using FILTER function for the expression is preferable than WHERE from the performance perspective.</span></span> <span data-ttu-id="a2847-193">حدد إصلاح لاستبداله تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="a2847-193">Select Fix to replace it automatically.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2847-194"><a href='#i8'>تفضيل وظيفة ALLITEMSQUERY مقابل ALLITEMS</a></span><span class="sxs-lookup"><span data-stu-id="a2847-194"><a href='#i8'>Preferability of ALLITEMSQUERY vs ALLITEMS function</a></span></span></td>
<td><span data-ttu-id="a2847-195">الأداء</span><span class="sxs-lookup"><span data-stu-id="a2847-195">Performance</span></span></td>
<td><span data-ttu-id="a2847-196">تحذير</span><span class="sxs-lookup"><span data-stu-id="a2847-196">Warning</span></span></td>
<td><span data-ttu-id="a2847-197">يفضل استخدام وظيفة ALLITEMSQUERY للتعبير عن ALLITEMS من منظور الأداء.</span><span class="sxs-lookup"><span data-stu-id="a2847-197">Using ALLITEMSQUERY function for the expression is preferable than ALLITEMS from the performance perspective.</span></span> <span data-ttu-id="a2847-198">حدد إصلاح لاستبداله تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="a2847-198">Select Fix to replace it automatically.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2847-199"><a href='#i9'>اعتبار حالات القائمة الفارغة</a></span><span class="sxs-lookup"><span data-stu-id="a2847-199"><a href='#i9'>Consideration of empty list cases</a></span></span></td>
<td><span data-ttu-id="a2847-200">إمكانية التنفيذ</span><span class="sxs-lookup"><span data-stu-id="a2847-200">Executability</span></span></td>
<td><span data-ttu-id="a2847-201">تحذير</span><span class="sxs-lookup"><span data-stu-id="a2847-201">Warning</span></span></td>
<td>
<p><span data-ttu-id="a2847-202">لا يحتوي &lt;مسار&gt; القائمة علي اي تحقق من حاله القائمة الفارغة، فقد يتسبب في حدوث خطا في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="a2847-202">List &lt;path&gt; does not have any check for empty list case, it can result an error at run time.</span></span> <span data-ttu-id="a2847-203">أضف فحصًا لحالة القائمة الفارغة.</span><span class="sxs-lookup"><span data-stu-id="a2847-203">Add a check for empty list case.</span></span></p>
<p><span data-ttu-id="a2847-204"><b>خطأ في وقت التشغيل:</b>القائمة فارغة في &lt;المسار&gt;</span><span class="sxs-lookup"><span data-stu-id="a2847-204"><b>Runtime error:</b> List is empty at &lt;path&gt;</span></span></p>
<p><span data-ttu-id="a2847-205"><b><a href='#i9a'>مشكلة محتملة</a>:</b> يتم ملء الخط مرة واحدة بينما يحتوي مصدر البيانات الذي يتم ملؤه منه على سجلات متعددة</span><span class="sxs-lookup"><span data-stu-id="a2847-205"><b><a href='#i9a'>Potential issue</a>:</b> Line is getting populated once while a data source it is populated from contains multiple records</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="a2847-206"><a href='#i10'>إمكانية تنفيذ تعبير باستخدام وظيفة التصفية (التخزين المؤقت)</a></span><span class="sxs-lookup"><span data-stu-id="a2847-206"><a href='#i10'>Executability of an expression with FILTER function (caching)</a></span></span></td>
<td><span data-ttu-id="a2847-207">إمكانية التنفيذ</span><span class="sxs-lookup"><span data-stu-id="a2847-207">Executability</span></span></td>
<td><span data-ttu-id="a2847-208">‏‏خطأ</span><span class="sxs-lookup"><span data-stu-id="a2847-208">Error</span></span></td>
<td>
<p><span data-ttu-id="a2847-209">لا يمكن تطبيق وظيفة التصفية على النوع المحدد من مصدر البيانات.</span><span class="sxs-lookup"><span data-stu-id="a2847-209">FILTER function cannot be applied to the selected type of data source.</span></span> <span data-ttu-id="a2847-210">لا ينطبق مصدر بيانات نوع سجلات الجدول الا في حاله عدم تخزينه مؤقتا ولم يقم باضافه مصادر البيانات المتداخلة يدويا.</span><span class="sxs-lookup"><span data-stu-id="a2847-210">A data source of the Table records type is applicable only when it is not cached and has no manually added nested data sources.</span></span></p>
<p><span data-ttu-id="a2847-211"><b>خطأ في وقت التشغيل:</b> التصفية غير مدعومة.</span><span class="sxs-lookup"><span data-stu-id="a2847-211"><b>Runtime error:</b> Filtering is not supported.</span></span> <span data-ttu-id="a2847-212">تحقق من صحة التكوين للحصول على مزيد من التفاصيل حول ذلك.</span><span class="sxs-lookup"><span data-stu-id="a2847-212">Validate the configuration to get more details about this.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="a2847-213"><a href='#i11'>الربط مفقود</a></span><span class="sxs-lookup"><span data-stu-id="a2847-213"><a href='#i11'>Missing binding</a></span></span></td>
<td><span data-ttu-id="a2847-214">إمكانية التنفيذ</span><span class="sxs-lookup"><span data-stu-id="a2847-214">Executability</span></span></td>
<td><span data-ttu-id="a2847-215">تحذير</span><span class="sxs-lookup"><span data-stu-id="a2847-215">Warning</span></span></td>
<td>
<p><span data-ttu-id="a2847-216">لا يحتوي المسار &lt;المسار&gt; على اي ربط بأي مصدر بيانات باستخدام تعيين النموذج.</span><span class="sxs-lookup"><span data-stu-id="a2847-216">Path &lt;path&gt; has no binding to any datasource in using model's mapping.</span></span></p>
<p><span data-ttu-id="a2847-217"><b>خطأ في وقت التشغيل:</b> لم يتم العثور على المسار &lt;المسار&gt;</span><span class="sxs-lookup"><span data-stu-id="a2847-217"><b>Runtime error:</b> Path &lt;path&gt; is not bound</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="a2847-218"><a href='#i12'>قالب غير مرتبط</a></span><span class="sxs-lookup"><span data-stu-id="a2847-218"><a href='#i12'>Not linked template</a></span></span></td>
<td><span data-ttu-id="a2847-219">تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="a2847-219">Data integrity</span></span></td>
<td><span data-ttu-id="a2847-220">تحذير</span><span class="sxs-lookup"><span data-stu-id="a2847-220">Warning</span></span></td>
<td><span data-ttu-id="a2847-221">&lt;اسم&gt; الملف غير مرتبط بأي مكونات ملف وستتم ازالته بعد تغيير حاله إصدار التكوين.</span><span class="sxs-lookup"><span data-stu-id="a2847-221">File &lt;name&gt; is linked to no file components and will be removed after changing status of configuration version.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2847-222"><a href='#i13'>تنسيق غير متزامن</a></span><span class="sxs-lookup"><span data-stu-id="a2847-222"><a href='#i13'>Not synced format</a></span></span></td>
<td><span data-ttu-id="a2847-223">تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="a2847-223">Data integrity</span></span></td>
<td><span data-ttu-id="a2847-224">تحذير</span><span class="sxs-lookup"><span data-stu-id="a2847-224">Warning</span></span></td>
<td><span data-ttu-id="a2847-225">الاسم المحدد &lt;اسن المكون&gt; غير موجود في ورقه عمل Excel &lt;اسم الورقة&gt;</span><span class="sxs-lookup"><span data-stu-id="a2847-225">Defined name &lt;component name&gt; does not exist in Excel sheet &lt;sheet name&gt;</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2847-226"><a href='#i14'>تنسيق غير متزامن</a></span><span class="sxs-lookup"><span data-stu-id="a2847-226"><a href='#i14'>Not synced format</a></span></span></td>
<td><span data-ttu-id="a2847-227">تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="a2847-227">Data integrity</span></span></td>
<td><span data-ttu-id="a2847-228">تحذير</span><span class="sxs-lookup"><span data-stu-id="a2847-228">Warning</span></span></td>
<td>
<p><span data-ttu-id="a2847-229">علامة &lt;عنصر تحكم محتوى word المعلمة&gt; غير موجودة في ملف قالب Word</span><span class="sxs-lookup"><span data-stu-id="a2847-229">&lt;Tagged Word content control&gt; tag does not exist in Word template file</span></span></p>
<p><span data-ttu-id="a2847-230"><b>خطأ وقت التشغيل:</b> &lt;علامة عنصر تحكم محتوى word المعلمة&gt; غير موجودة في ملف قالب Word.</span><span class="sxs-lookup"><span data-stu-id="a2847-230"><b>Runtime error:</b> &lt;Tagged Word content control&gt; tag does not exist in Word template file.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="a2847-231"><a href='#i15'>لا يوجد تعيين افتراضي</a></span><span class="sxs-lookup"><span data-stu-id="a2847-231"><a href='#i15'>No default mapping</a></span></span></td>
<td><span data-ttu-id="a2847-232">تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="a2847-232">Data integrity</span></span></td>
<td><span data-ttu-id="a2847-233">‏‏خطأ</span><span class="sxs-lookup"><span data-stu-id="a2847-233">Error</span></span></td>
<td>
<p><span data-ttu-id="a2847-234">يوجد أكثر من تعيين طراز واحد لنموذج بيانات &lt;اسم النموذج (الواصف الجذر)&gt;في التكوينات &lt;أسماء التكوين المفصولة بفاصلة&gt;.</span><span class="sxs-lookup"><span data-stu-id="a2847-234">More than one model mapping exists for the &lt;model name (root descriptor)&gt; data model in the configurations &lt;configuration names separated by comma&gt;.</span></span> <span data-ttu-id="a2847-235">تعيين أحد التكوينات كإعداد افتراضي</span><span class="sxs-lookup"><span data-stu-id="a2847-235">Set one of the configurations as default</span></span></p>
<p><span data-ttu-id="a2847-236"><b>خطأ وقت التشغيل:</b>يوجد أكثر من تعيين طراز واحد لنموذج بيانات &lt;اسم النموذج (الواصف الجذر)&gt; في التكوينات &lt;أسماء التكوين المفصولة بفاصلة&gt;.</span><span class="sxs-lookup"><span data-stu-id="a2847-236"><b>Runtime error:</b> More than one model mapping exists for the &lt;model name (root descriptor)&gt; data model in the configurations &lt;configuration names separated by comma&gt;.</span></span> <span data-ttu-id="a2847-237">قم بتعيين أحد التكوينات كاعداد افتراضي.</span><span class="sxs-lookup"><span data-stu-id="a2847-237">Set one of the configurations as default.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="a2847-238"><a href='#i16'>إعداد غير متناسق لمكونات الرأس أو التذييل</a></span><span class="sxs-lookup"><span data-stu-id="a2847-238"><a href='#i16'>Inconsistent setting of Header or Footer components</a></span></span></td>
<td><span data-ttu-id="a2847-239">تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="a2847-239">Data integrity</span></span></td>
<td><span data-ttu-id="a2847-240">‏‏خطأ</span><span class="sxs-lookup"><span data-stu-id="a2847-240">Error</span></span></td>
<td>
<p><span data-ttu-id="a2847-241">الرؤوس/التذييل (&lt;نوع المكون: الرأس أو التذييل&gt;) غير متسقة</span><span class="sxs-lookup"><span data-stu-id="a2847-241">Headers/footers (&lt;component type: Header or Footer&gt;) are inconsistent</span></span></p>
<p><span data-ttu-id="a2847-242"><b>وقت التشغيل:</b>يتم استخدام آخر مكون تم تكوينه في وقت التشغيل في حالة تنفيذ إصدار المسودة لتنسيق ER المكون.</span><span class="sxs-lookup"><span data-stu-id="a2847-242"><b>Runtime:</b> The last configured component is used at runtime if the draft version of the configured ER format is executed.</span></span></p>
</td>
</tr>
</tbody>
</table>

## <a name="type-conversion"></a><a id="i1"></a><span data-ttu-id="a2847-243">نوع التحويل</span><span class="sxs-lookup"><span data-stu-id="a2847-243">Type conversion</span></span>

<span data-ttu-id="a2847-244">يقوم التقارير الإلكترونية بالتحقق مما إذا كان نوع بيانات حقل نموذج البيانات متوافقا مع نوع البيانات لتعبير تم تكوينه كرابط لهذا الحقل.</span><span class="sxs-lookup"><span data-stu-id="a2847-244">ER checks whether the data type of a data model field is compatible with the data type of an expression that is configured as the binding of that field.</span></span> <span data-ttu-id="a2847-245">في حاله عدم توافق أنواع البيانات، يحدث خطا في التحقق من الصحة في مصمم تعيين نموذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a2847-245">If the data types are incompatible, a validation error occurs in the ER model mapping designer.</span></span> <span data-ttu-id="a2847-246">تنص الرسالة التي تلقيتها علي انه لا يمكن للتقارير الإلكترونية تحويل تعبير من نوع A إلى حقل من النوع B.</span><span class="sxs-lookup"><span data-stu-id="a2847-246">The message that you receive states that ER can't convert an expression of type A to a field of type B.</span></span>

<span data-ttu-id="a2847-247">توضح الخطوات التالية كيفيه حدوث هذه المشكلة.</span><span class="sxs-lookup"><span data-stu-id="a2847-247">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a2847-248">أبدا في تكوين نموذج البيانات الخاص ب التقارير الإلكترونية ومكونات تعيين نموذج التقارير الإلكترونية في نفس الوقت.</span><span class="sxs-lookup"><span data-stu-id="a2847-248">Start to configure the ER data model and the ER model mapping components simultaneously.</span></span>
2. <span data-ttu-id="a2847-249">في شجره نموذج البيانات، قم باضافه حقل يسمي **X** وحدد **عدد صحيح** كنوع البيانات.</span><span class="sxs-lookup"><span data-stu-id="a2847-249">In the data model tree, add a field that is named **X**, and select **Integer** as the data type.</span></span>

    ![الحقل X ونوع البيانات الصحيح الذي تمت اضافته إلى شجره وضع البيانات في صفحه نموذج البيانات](./media/er-components-inspections-01.png)

3. <span data-ttu-id="a2847-251">في مصمم تعيين النموذج، في جزء **مصادر البيانات**، أضف مصدر بيانات من نوع **الحقل المحسوب**.</span><span class="sxs-lookup"><span data-stu-id="a2847-251">In the model mapping designer, in the **Data sources** pane, add a data source of the **Calculated field** type.</span></span>
4. <span data-ttu-id="a2847-252">قم بتسميه مصدر البيانات الجديد **Y**، وقم بتكوينه بحيث يحتوي علي التعبير `INTVALUE(100)`.</span><span class="sxs-lookup"><span data-stu-id="a2847-252">Name the new data source **Y**, and configure it so that it contains the expression `INTVALUE(100)`.</span></span>
5. <span data-ttu-id="a2847-253">اربط **X** بـ **Y**.</span><span class="sxs-lookup"><span data-stu-id="a2847-253">Bind **X** to **Y**.</span></span>
6. <span data-ttu-id="a2847-254">في مصمم نموذج البيانات، قم بتغيير نوع البيانات للحقل **X** من **العدد الصحيح** إلى **Int64**.</span><span class="sxs-lookup"><span data-stu-id="a2847-254">In the data model designer, change the data type of the **X** field from **Integer** to **Int64**.</span></span>
7. <span data-ttu-id="a2847-255">حدد **التحقق من الصحة** لفحص مكون تعيين النموذج القابل للتحرير في صفحه **مصمم تعيين النموذج**.</span><span class="sxs-lookup"><span data-stu-id="a2847-255">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page.</span></span>

    ![التحقق من صحة مكون تعيين النموذج القابل للتحرير في صفحة مصمم تعيين النموذج](./media/er-components-inspections-01.gif)

8. <span data-ttu-id="a2847-257">حدد **التحقق من الصحة** لفحص مكون تعيين النموذج الخاص بتكوين التقارير الإلكترونية المحدد على صفحة **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="a2847-257">Select **Validate** to inspect the model mapping component of the selected ER configuration on the **Configurations** page.</span></span>

    ![فحص مكون تعيين النموذج في صفحه التكوينات](./media/er-components-inspections-01a.png)

9. <span data-ttu-id="a2847-259">لاحظ حدوث خطا في التحقق من الصحة.</span><span class="sxs-lookup"><span data-stu-id="a2847-259">Notice that a validation error occurs.</span></span> <span data-ttu-id="a2847-260">وتوضح الرسالة أن قيمه نوع **العدد الصحيح** التي يرجع إليها تعبير `INTVALUE(100)` لمصدر البيانات **Y** لا يمكن تخزينها في حقل نموذج البيانات **X** لنوع **Int64**.</span><span class="sxs-lookup"><span data-stu-id="a2847-260">The message states that the value of the **Integer** type that the `INTVALUE(100)` expression of the **Y** data source returns can't be stored in the **X** data model field of the **Int64** type.</span></span>

<span data-ttu-id="a2847-261">يبين الرسم التوضيحي التالي خطا وقت التشغيل الذي يحدث إذا تجاهلت التحذير وحدد **تشغيل** لتشغيل تنسيق مكون لاستخدام تعيين النموذج.</span><span class="sxs-lookup"><span data-stu-id="a2847-261">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run a format that is configured to use the model mapping.</span></span>

![أخطاء وقت التشغيل في صفحة مصمم التنسيق](./media/er-components-inspections-01b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="a2847-263">الحل التلقائي</span><span class="sxs-lookup"><span data-stu-id="a2847-263">Automatic resolution</span></span>

<span data-ttu-id="a2847-264">لا يتوفر اي خيار لإصلاح هذه المشكلة تلقائيا.</span><span class="sxs-lookup"><span data-stu-id="a2847-264">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="a2847-265">الحل اليدوي</span><span class="sxs-lookup"><span data-stu-id="a2847-265">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="a2847-266">خيار 1</span><span class="sxs-lookup"><span data-stu-id="a2847-266">Option 1</span></span>

<span data-ttu-id="a2847-267">يجب تحديث بنيه نموذج البيانات عن طريق تغيير نوع بيانات حقل نموذج البيانات بحيث يطابق نوع البيانات الخاص بالتعبير الذي تم تكوينه للربط الخاص بهذا الحقل.</span><span class="sxs-lookup"><span data-stu-id="a2847-267">Update the data model structure by changing the data type of the data model field so that it matches the data type of the expression that is configured for the binding of that field.</span></span> <span data-ttu-id="a2847-268">بالنسبة للمثال السابق، يجب ان يتم تغيير نوع بيانات حقل **X** مرة أخرى إلى **عدد صحيح**.</span><span class="sxs-lookup"><span data-stu-id="a2847-268">For the preceding example, the data type of the **X** field must be changed back to **Integer**.</span></span>

#### <a name="option-2"></a><span data-ttu-id="a2847-269">خيار 2</span><span class="sxs-lookup"><span data-stu-id="a2847-269">Option 2</span></span>

<span data-ttu-id="a2847-270">تحديث تعيين النموذج من خلال تغيير تعبير مصدر البيانات المرتبط بحقل نموذج البيانات.</span><span class="sxs-lookup"><span data-stu-id="a2847-270">Update the model mapping by changing the expression of the data source that is bound with the data model field.</span></span> <span data-ttu-id="a2847-271">بالنسبة للمثال السابق، يجب تغيير تعبير مصدر البيانات **Y** إلى `INT64VALUE(100)`.</span><span class="sxs-lookup"><span data-stu-id="a2847-271">For the preceding example, the expression of the **Y** data source must be changed to `INT64VALUE(100)`.</span></span>

## <a name="type-compatibility"></a><a id="i2"></a><span data-ttu-id="a2847-272">توافق النوع</span><span class="sxs-lookup"><span data-stu-id="a2847-272">Type compatibility</span></span>

<span data-ttu-id="a2847-273">يتحقق التقارير الإلكترونية مما إذا كان نوع البيانات لعنصر التنسيق متوافقًا مع نوع بيانات التعبير الذي تم تكوينه كربط لعنصر التنسيق هذا.</span><span class="sxs-lookup"><span data-stu-id="a2847-273">ER checks whether the data type of a format element is compatible with the data type of an expression that is configured as the binding of that format element.</span></span> <span data-ttu-id="a2847-274">إذا كانت أنواع البيانات غير متوافقة، فسيحدث خطأ في التحقق من الصحة في مصمم عمليات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a2847-274">If the data types are incompatible, a validation error occurs in the ER Operations designer.</span></span> <span data-ttu-id="a2847-275">تنص الرسالة التي تتلقاها على أنه لا يمكن استخدام التعبير المكون كربط لعنصر التنسيق الحالي بمصدر بيانات، لأن التعبير يُرجع قيمة من نوع البيانات A خارج نطاق أنواع البيانات المدعومة بواسطة عنصر التنسيق الحالي من النوع B.</span><span class="sxs-lookup"><span data-stu-id="a2847-275">The message that you receive states that the configured expression can't be used as the binding of the current format element to a data source, because the expression returns a value of data type A that is beyond the scope of the data types that are supported by the current format element of type B.</span></span>

<span data-ttu-id="a2847-276">توضح الخطوات التالية كيفيه حدوث هذه المشكلة.</span><span class="sxs-lookup"><span data-stu-id="a2847-276">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a2847-277">ابدأ في تكوين نموذج بيانات التقارير الإلكترونية ومكونات تنسيق التقارير الإلكترونية في وقت واحد.</span><span class="sxs-lookup"><span data-stu-id="a2847-277">Start to configure the ER data model and the ER format components simultaneously.</span></span>
2. <span data-ttu-id="a2847-278">في شجره نموذج البيانات، قم باضافه حقل يسمي **X** وحدد **عدد صحيح** كنوع البيانات.</span><span class="sxs-lookup"><span data-stu-id="a2847-278">In the data model tree, add a field that is named **X**, and select **Integer** as the data type.</span></span>
3. <span data-ttu-id="a2847-279">في شجره بنية التنسيق، أضف عنصر تنسيق من النوع **العددي**.</span><span class="sxs-lookup"><span data-stu-id="a2847-279">In the format structure tree, add a format element of the **Numeric** type.</span></span>
4. <span data-ttu-id="a2847-280">قم بتسمية عنصر التنسيق الجديد **Y**. في حقل **النوع الرقمي**، حدد **عدد صحيح** كنوع البيانات.</span><span class="sxs-lookup"><span data-stu-id="a2847-280">Name the new format element **Y**. In the **Numeric type** field, select **Integer** as the data type.</span></span>
5. <span data-ttu-id="a2847-281">اربط **X** بـ **Y**.</span><span class="sxs-lookup"><span data-stu-id="a2847-281">Bind **X** to **Y**.</span></span>
6. <span data-ttu-id="a2847-282">في شجره بنيه التنسيق، قم بتغيير نوع البيانات الخاص بعنصر التنسيق **Y** من **العدد الصحيح** إلى **Int64**.</span><span class="sxs-lookup"><span data-stu-id="a2847-282">In the format structure tree, change the data type of the **Y** format element from **Integer** to **Int64**.</span></span>
7. <span data-ttu-id="a2847-283">حدد **التحقق من الصحة** لفحص مكون التنسيق القابل للتحرير في صفحة **مصمم التنسيق**.</span><span class="sxs-lookup"><span data-stu-id="a2847-283">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![التحقق من توافق النوع علي صفحه مصمم التنسيق](./media/er-components-inspections-02.gif)

8. <span data-ttu-id="a2847-285">لاحظ حدوث خطا في التحقق من الصحة.</span><span class="sxs-lookup"><span data-stu-id="a2847-285">Notice that a validation error occurs.</span></span> <span data-ttu-id="a2847-286">وتوضح الرسالة ان التعبير المكون يمكنه قبول قيم **Int64** فقط.</span><span class="sxs-lookup"><span data-stu-id="a2847-286">The message states that the configured expression can accept only **Int64** values.</span></span> <span data-ttu-id="a2847-287">لذلك، لا يمكن إدخال قيمه حقل نموذج بيانات **X** الخاص بنوع **العدد الصحيح** في عنصر التنسيق **Y**.</span><span class="sxs-lookup"><span data-stu-id="a2847-287">Therefore, the value of the **X** data model field of the **Integer** type can't be entered in the **Y** format element.</span></span>

### <a name="automatic-resolution"></a><span data-ttu-id="a2847-288">الحل التلقائي</span><span class="sxs-lookup"><span data-stu-id="a2847-288">Automatic resolution</span></span>

<span data-ttu-id="a2847-289">لا يتوفر اي خيار لإصلاح هذه المشكلة تلقائيا.</span><span class="sxs-lookup"><span data-stu-id="a2847-289">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="a2847-290">الحل اليدوي</span><span class="sxs-lookup"><span data-stu-id="a2847-290">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="a2847-291">خيار 1</span><span class="sxs-lookup"><span data-stu-id="a2847-291">Option 1</span></span>

<span data-ttu-id="a2847-292">قم بتحديث بنية التنسيق عن طريق تغيير نوع البيانات الخاص بعنصر التنسيق **العددي** بحيث يطابق نوع بيانات التعبير الذي تم تكوينه لربط هذا العنصر.</span><span class="sxs-lookup"><span data-stu-id="a2847-292">Update the format structure by changing the data type of the **Numeric** format element so that it matches the data type of the expression that you configured for the binding of that element.</span></span> <span data-ttu-id="a2847-293">في المثال السابق، يجب تغيير قيمة **النوع العددي** الخاص بعنصر التنسيق **X** مرة أخرى إلى **العدد الصحيح**.</span><span class="sxs-lookup"><span data-stu-id="a2847-293">In the preceding example, the **Numeric type** value of the **X** format element must be changed back to **Integer**.</span></span>

#### <a name="option-2"></a><span data-ttu-id="a2847-294">خيار 2</span><span class="sxs-lookup"><span data-stu-id="a2847-294">Option 2</span></span>

<span data-ttu-id="a2847-295">قم بتحديث تعيين التنسيق الخاص بعنصر التنسيق **X** من خلال تغيير التعبير من `model.X` إلى `INT64VALUE(model.X)`.</span><span class="sxs-lookup"><span data-stu-id="a2847-295">Update the format mapping of the **X** format element by changing the expression from `model.X` to `INT64VALUE(model.X)`.</span></span>

## <a name="missing-configuration-element"></a><a id="i3"></a><span data-ttu-id="a2847-296">عنصر التكوين مفقود</span><span class="sxs-lookup"><span data-stu-id="a2847-296">Missing configuration element</span></span>

<span data-ttu-id="a2847-297">يقوم التقارير الإلكترونية بالتحقق مما إذا كانت تعبيرات الربط تحتوي علي مصادر البيانات التي تم تكوينها في مكونات التقارير الإلكترونية القابلة للتحرير ام لا.</span><span class="sxs-lookup"><span data-stu-id="a2847-297">ER checks whether the binding expressions contain only data sources that are configured in the editable ER component.</span></span> <span data-ttu-id="a2847-298">لكل ربط يحتوي علي مصدر بيانات مفقود في مكونات التقارير الإلكترونية القابلة للتحرير، يحدث خطا في التحقق من الصحة في "مصمم العمليات" الخاص ب التقارير الإلكترونية أو مصمم تعيين نموذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a2847-298">For every binding that contains a data source that is missing in the editable ER component, a validation error occurs in the ER Operations designer or the ER model mapping designer.</span></span>

<span data-ttu-id="a2847-299">توضح الخطوات التالية كيفيه حدوث هذه المشكلة.</span><span class="sxs-lookup"><span data-stu-id="a2847-299">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a2847-300">أبدا في تكوين نموذج البيانات الخاص ب التقارير الإلكترونية ومكونات تعيين نموذج التقارير الإلكترونية في نفس الوقت.</span><span class="sxs-lookup"><span data-stu-id="a2847-300">Start to configure the ER data model and the ER model mapping components simultaneously.</span></span>
2. <span data-ttu-id="a2847-301">في شجره نموذج البيانات، قم باضافه حقل يسمي **X** وحدد **عدد صحيح** كنوع البيانات.</span><span class="sxs-lookup"><span data-stu-id="a2847-301">In the data model tree, add a field that is named **X**, and select **Integer** as the data type.</span></span>

    ![شجرة نموذج البيانات مع حقل X ونوع بيانات عدد صحيح في صفحة نموذج البيانات](./media/er-components-inspections-01.png)

3. <span data-ttu-id="a2847-303">في مصمم تعيين النموذج، في جزء **مصادر البيانات**، أضف مصدر بيانات من نوع **الحقل المحسوب**.</span><span class="sxs-lookup"><span data-stu-id="a2847-303">In the model mapping designer, in the **Data sources** pane, add a data source of the **Calculated field** type.</span></span>
4. <span data-ttu-id="a2847-304">قم بتسميه مصدر البيانات الجديد **Y**، وقم بتكوينه بحيث يحتوي علي التعبير `INTVALUE(100)`.</span><span class="sxs-lookup"><span data-stu-id="a2847-304">Name the new data source **Y**, and configure it so that it contains the expression `INTVALUE(100)`.</span></span>
5. <span data-ttu-id="a2847-305">اربط **X** بـ **Y**.</span><span class="sxs-lookup"><span data-stu-id="a2847-305">Bind **X** to **Y**.</span></span>
6. <span data-ttu-id="a2847-306">في مصمم تعيين النموذج، في جزء **مصادر البيانات**، احذف مصدر بيانات **Y**.</span><span class="sxs-lookup"><span data-stu-id="a2847-306">In the model mapping designer, in the **Data sources** pane, delete the **Y** data source.</span></span>
7. <span data-ttu-id="a2847-307">حدد **التحقق من الصحة** لفحص مكون تعيين النموذج القابل للتحرير في صفحه **مصمم تعيين النموذج**.</span><span class="sxs-lookup"><span data-stu-id="a2847-307">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page.</span></span>

    ![فحص مكون تعيين نموذج التقارير الإلكترونية (ER) القابل للتحرير في صفحة مصمم تعيين النموذج](./media/er-components-inspections-03.gif)

8. <span data-ttu-id="a2847-309">لاحظ حدوث خطا في التحقق من الصحة.</span><span class="sxs-lookup"><span data-stu-id="a2847-309">Notice that a validation error occurs.</span></span> <span data-ttu-id="a2847-310">وتوضح الرسالة أن ربط حقل نموذج البيانات **X** يحتوي على المسار الذي يشير إلى مصدر بيانات **Y**، ولكن لم يتم العثور على مصدر البيانات هذا.</span><span class="sxs-lookup"><span data-stu-id="a2847-310">The message states that the binding of the **X** data model field contains the path that refers to the **Y** data source, but this data source isn't found.</span></span>

### <a name="automatic-resolution"></a><span data-ttu-id="a2847-311">الحل التلقائي</span><span class="sxs-lookup"><span data-stu-id="a2847-311">Automatic resolution</span></span>

<span data-ttu-id="a2847-312">حدد **إلغاء الربط** لحل هذه المشكلة تلقائيا عن طريق أزاله ربط مصدر البيانات المفقود.</span><span class="sxs-lookup"><span data-stu-id="a2847-312">Select **Unbind** to automatically fix this issue by removing the missing data source binding.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="a2847-313">الحل اليدوي</span><span class="sxs-lookup"><span data-stu-id="a2847-313">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="a2847-314">خيار 1</span><span class="sxs-lookup"><span data-stu-id="a2847-314">Option 1</span></span>

<span data-ttu-id="a2847-315">قم بإلغاء ربط حقل نموذج البيانات **X** لإيقاف الإشارة إلى مصدر بيانات **Y** غير الموجود.</span><span class="sxs-lookup"><span data-stu-id="a2847-315">Unbind the **X** data model field to stop referring to the nonexistent **Y** data source.</span></span>

#### <a name="option-2"></a><span data-ttu-id="a2847-316">خيار 2</span><span class="sxs-lookup"><span data-stu-id="a2847-316">Option 2</span></span>

<span data-ttu-id="a2847-317">في مصمم تعيين النموذج، في جزء **مصادر البيانات**، أضف مصدر البيانات **Y** مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="a2847-317">In the model mapping designer, in the **Data sources** pane, add the **Y** data source again.</span></span>

## <a name="executability-of-an-expression-with-filter-function"></a><a id="i4"></a><span data-ttu-id="a2847-318">إمكانية تنفيذ تعبير باستخدام وظيفة التصفية</span><span class="sxs-lookup"><span data-stu-id="a2847-318">Executability of an expression with FILTER function</span></span>

<span data-ttu-id="a2847-319">يتم استخدام وظيفة [تصفية](er-functions-list-filter.md) التقارير الإلكترونية المضمنة للوصول إلى جداول التطبيق أو طرق العرض أو كيانات البيانات عن طريق وضع استدعاء SQL مفرد للحصول علي البيانات المطلوبة كقائمه سجلات.</span><span class="sxs-lookup"><span data-stu-id="a2847-319">The built-in [FILTER](er-functions-list-filter.md) ER function is used to access application tables, views, or data entities by placing a single SQL call to get the required data as a list of records.</span></span> <span data-ttu-id="a2847-320">يتم استخدام مصدر بيانات من نوع **قائمة السجلات** كوسيطة لهذه الوظيفة ويحدد مصدر التطبيق الخاص بالاستدعاء.</span><span class="sxs-lookup"><span data-stu-id="a2847-320">A data source of the **Record list** type is used as an argument of this function and specifies the application source for the call.</span></span> <span data-ttu-id="a2847-321">يقوم التقارير الإلكترونية بالتحقق مما إذا كان من الممكن إنشاء استعلام SQL مباشر إلى مصدر بيانات يشار إليه في وظيفة `FILTER` أو لا.</span><span class="sxs-lookup"><span data-stu-id="a2847-321">ER checks whether a direct SQL query can be established to a data source that is referred to in the `FILTER` function.</span></span> <span data-ttu-id="a2847-322">في حاله تعذر إنشاء الاستعلام المباشر، يحدث خطا في التحقق من الصحة في مصمم تعيين نموذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a2847-322">If a direct query can't be established, a validation error occurs in the ER model mapping designer.</span></span> <span data-ttu-id="a2847-323">توضح الرسالة التي تتلقاها ان تعبير التقارير الإلكترونية الذي يتضمن وظيفة `FILTER` لا يمكن تشغيله في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="a2847-323">The message that you receive states that the ER expression that includes the `FILTER` function can't be run at runtime.</span></span>

<span data-ttu-id="a2847-324">توضح الخطوات التالية كيفيه حدوث هذه المشكلة.</span><span class="sxs-lookup"><span data-stu-id="a2847-324">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a2847-325">ابدأ بتكوين مكون تعيين نموذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a2847-325">Start to configure the ER model mapping component.</span></span>
2. <span data-ttu-id="a2847-326">أضف مصدر بيانات من نوع **Dynamics 365 for Operations \\ سجلات الجداول**.</span><span class="sxs-lookup"><span data-stu-id="a2847-326">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="a2847-327">قم بتسمية مصدر البيانات الجديد **المورد**.</span><span class="sxs-lookup"><span data-stu-id="a2847-327">Name the new data source **Vendor**.</span></span> <span data-ttu-id="a2847-328">في حقل **الجدول**، حدد **VendTable** لتحديد أن مصدر البيانات سيطلب الجدول VendTable.</span><span class="sxs-lookup"><span data-stu-id="a2847-328">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
4. <span data-ttu-id="a2847-329">أضف مصدر بيانات من نوع **الحقل المحسوب**.</span><span class="sxs-lookup"><span data-stu-id="a2847-329">Add a data source of the **Calculated field** type.</span></span>
5. <span data-ttu-id="a2847-330">قم بتسميه مصدر البيانات الجديد **FilteredVendor**، وقم بتكوينه بحيث يحتوي علي التعبير `FILTER(Vendor, Vendor.AccountNum="US-101")`.</span><span class="sxs-lookup"><span data-stu-id="a2847-330">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, Vendor.AccountNum="US-101")`.</span></span>
6. <span data-ttu-id="a2847-331">حدد **التحقق من الصحة** لفحص مكون تعيين النموذج القابل للتحرير علي صفحة **مصمم تعيين النموذج** والتحقق من إمكانية الاستعلام عن تعبير `FILTER(Vendor, Vendor.AccountNum="US-101")` في مصدر بيانات **المورد**.</span><span class="sxs-lookup"><span data-stu-id="a2847-331">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page and verify that the `FILTER(Vendor, Vendor.AccountNum="US-101")` expression in the **Vendor** data source can be queried.</span></span>
7. <span data-ttu-id="a2847-332">قم بتعديل مصدر بيانات **المورد** عن طريق أضافه حقل متداخل لـ **نوع الحقل المحسوب** للحصول علي رقم حساب المورد الذي تم اقتطاعه.</span><span class="sxs-lookup"><span data-stu-id="a2847-332">Modify the **Vendor** data source by adding a nested field of the **Calculated field** type to get the trimmed vendor account number.</span></span>
8. <span data-ttu-id="a2847-333">قم بتسميه الحقل المتداخل الجديد **$AccNumber**، وقم بتكوينه بحيث يحتوي علي التعبير `TRIM(Vendor.AccountNum)`.</span><span class="sxs-lookup"><span data-stu-id="a2847-333">Name the new nested field **$AccNumber**, and configure it so that it contains the expression `TRIM(Vendor.AccountNum)`.</span></span>
9. <span data-ttu-id="a2847-334">حدد **التحقق من الصحة** لفحص مكون تعيين النموذج القابل للتحرير علي صفحة **مصمم تعيين النموذج** والتحقق من إمكانية الاستعلام عن تعبير `FILTER(Vendor, Vendor.AccountNum="US-101")` في مصدر بيانات **المورد**.</span><span class="sxs-lookup"><span data-stu-id="a2847-334">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page and verify that the `FILTER(Vendor, Vendor.AccountNum="US-101")` expression in the **Vendor** data source can be queried.</span></span>

    ![التحقق من إمكانية الاستعلام عن التعبير في صفحة مصمم تعيين النموذج](./media/er-components-inspections-04.gif)

10. <span data-ttu-id="a2847-336">لاحظ حدوث خطا في التحقق من الصحة، نظرا لان مصدر بيانات **المورد** يحتوي علي حقل متداخل من نوع **الحقل المحسوب** الذي لا يسمح بترجمة تعبير مصدر البيانات **FilteredVendor** إلى عبارة SQL المباشرة.</span><span class="sxs-lookup"><span data-stu-id="a2847-336">Notice that a validation error occurs, because the **Vendor** data source contains a nested field of the **Calculated field** type that doesn't allow the expression of the **FilteredVendor** data source to be translated to the direct SQL statement.</span></span>

<span data-ttu-id="a2847-337">يبين الرسم التوضيحي التالي خطا وقت التشغيل الذي يحدث إذا تجاهلت التحذير وحدد **تشغيل** لتشغيل تنسيق مكون لاستخدام تعيين النموذج.</span><span class="sxs-lookup"><span data-stu-id="a2847-337">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run a format that is configured to use the model mapping.</span></span>

![أخطاء وقت التشغيل التي تحدث عند تشغيل التنسيق القابل للتحرير علي صفحه مصمم التنسيق](./media/er-components-inspections-04a.png)

### <a name="automatic-resolution"></a><span data-ttu-id="a2847-339">الحل التلقائي</span><span class="sxs-lookup"><span data-stu-id="a2847-339">Automatic resolution</span></span>

<span data-ttu-id="a2847-340">لا يتوفر اي خيار لإصلاح هذه المشكلة تلقائيا.</span><span class="sxs-lookup"><span data-stu-id="a2847-340">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="a2847-341">الحل اليدوي</span><span class="sxs-lookup"><span data-stu-id="a2847-341">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="a2847-342">خيار 1</span><span class="sxs-lookup"><span data-stu-id="a2847-342">Option 1</span></span>

<span data-ttu-id="a2847-343">بدلا من أضافه حقل متداخل من نوع **الحقل المحسوب** إلى مصدر بيانات **المورد**، قم باضافه الحقل المتداخل **$AccNumber** إلى مصدر بيانات **FilteredVendor**، وقم بتكوينه بحيث يحتوي على التعبير `TRIM(FilteredVendor.AccountNum)`.</span><span class="sxs-lookup"><span data-stu-id="a2847-343">Instead of adding a nested field of the **Calculated field** type to the **Vendor** data source, add the **$AccNumber** nested field to the **FilteredVendor** data source, and configure it so that it contains the expression `TRIM(FilteredVendor.AccountNum)`.</span></span> <span data-ttu-id="a2847-344">وبهذه الطريقة، يمكن تشغيل التعبير `FILTER(Vendor, Vendor.AccountNum="US-101")` في مستوي SQL وحساب الحقل المتداخل **$AccNumber** بعد ذلك.</span><span class="sxs-lookup"><span data-stu-id="a2847-344">In this way, the `FILTER(Vendor, Vendor.AccountNum="US-101")` expression can be run at the SQL level and calculate the **$AccNumber** nested field afterward.</span></span>

#### <a name="option-2"></a><span data-ttu-id="a2847-345">خيار 2</span><span class="sxs-lookup"><span data-stu-id="a2847-345">Option 2</span></span>

<span data-ttu-id="a2847-346">قم بتغيير التعبير الخاص بمصدر بيانات **FilteredVendor** من `FILTER(Vendor, Vendor.AccountNum="US-101")`إلى `WHERE(Vendor, Vendor.AccountNum="US-101")`.</span><span class="sxs-lookup"><span data-stu-id="a2847-346">Change the expression of the **FilteredVendor** data source from `FILTER(Vendor, Vendor.AccountNum="US-101")` to `WHERE(Vendor, Vendor.AccountNum="US-101")`.</span></span> <span data-ttu-id="a2847-347">لا نوصي بتغيير التعبير الخاص بأحد الجداول الذي يحتوي علي حجم كبير من البيانات (جدول المعاملات)، وذلك لأنه سيتم إحضار كافة السجلات، سيتم اجراء تحديد السجلات المطلوبة في الذاكرة.</span><span class="sxs-lookup"><span data-stu-id="a2847-347">We don't recommend that you change the expression for a table that has a large volume of data (transactional table), because all records will be fetched, and selection of the required records will be done in memory.</span></span> <span data-ttu-id="a2847-348">لذلك، يمكن ان يتسبب هذا الأسلوب في ضعف الأداء.</span><span class="sxs-lookup"><span data-stu-id="a2847-348">Therefore, this approach can cause poor performance.</span></span> <span data-ttu-id="a2847-349">لمزيد من المعلومات، راجع [وظيفة التقارير الإلكترونية للمكان](er-functions-list-where.md).</span><span class="sxs-lookup"><span data-stu-id="a2847-349">For more information, see [WHERE ER function](er-functions-list-where.md).</span></span>

## <a name="executability-of-a-groupby-data-source"></a><a id="i5"></a><span data-ttu-id="a2847-350">إمكانية تنفيذ مصدر بيانات التجميع حسب</span><span class="sxs-lookup"><span data-stu-id="a2847-350">Executability of a GROUPBY data source</span></span>

<span data-ttu-id="a2847-351">يقسم مصدر البيانات **التجميع حسب** نتيجة الاستعلام إلى مجموعات من السجلات، عاده لغرض اجراء تجميع واحد أو أكثر في كل مجموعه.</span><span class="sxs-lookup"><span data-stu-id="a2847-351">The **GROUPBY** data source divides the query result into groups of records, usually for the purpose of doing one or more aggregations on each group.</span></span> <span data-ttu-id="a2847-352">يمكن تكوين كل مصدر بيانات **التجميع حسب** بحيث يتم تشغيله اما في مستوي قاعده البيانات أو في الذاكرة.</span><span class="sxs-lookup"><span data-stu-id="a2847-352">Every **GROUPBY** data source can be configured so that it's run either at the database level or in memory.</span></span> <span data-ttu-id="a2847-353">عند تكوين مصدر بيانات **التجميع حسب** بحيث يتم تشغيله علي مستوي قاعده البيانات، تقوم التقارير الإلكترونية بالتحقق مما إذا كان من الممكن تاسيس استعلام SQL مباشر إلى مصدر بيانات يتم الاشاره اليه في مصدر البيانات هذا أو لا.</span><span class="sxs-lookup"><span data-stu-id="a2847-353">When a **GROUPBY** data source is configured so that it's run at the database level, ER checks whether a direct SQL query can be established to a data source that is referred to in that data source.</span></span> <span data-ttu-id="a2847-354">في حاله تعذر إنشاء الاستعلام المباشر، يحدث خطا في التحقق من الصحة في مصمم تعيين نموذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a2847-354">If a direct query can't be established, a validation error occurs in the ER model mapping designer.</span></span> <span data-ttu-id="a2847-355">توضح الرسالة التي تتلقاها انه لا يمكن تشغيل مصدر بيانات **التجميع حسب** المكون في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="a2847-355">The message that you receive states that the configured **GROUPBY** data source can't be run at runtime.</span></span>

<span data-ttu-id="a2847-356">توضح الخطوات التالية كيفيه حدوث هذه المشكلة.</span><span class="sxs-lookup"><span data-stu-id="a2847-356">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a2847-357">ابدأ بتكوين مكون تعيين نموذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a2847-357">Start to configure the ER model mapping component.</span></span>
2. <span data-ttu-id="a2847-358">أضف مصدر بيانات من نوع **Dynamics 365 for Operations \\ سجلات الجداول**.</span><span class="sxs-lookup"><span data-stu-id="a2847-358">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="a2847-359">قم بتسمية مصدر البيانات الجديد **Trans**. في حقل **الجدول**، حدد **VendTrans** لتحديد أن مصدر البيانات هذا سيطلب جدول VendTrans.</span><span class="sxs-lookup"><span data-stu-id="a2847-359">Name the new data source **Trans**. In the **Table** field, select **VendTrans** to specify that this data source will request the VendTrans table.</span></span>
4. <span data-ttu-id="a2847-360">أضف مصدر بيانات من نوع **التجميع حسب**.</span><span class="sxs-lookup"><span data-stu-id="a2847-360">Add a data source of the **Group by** type.</span></span>
5. <span data-ttu-id="a2847-361">قم بتسميه مصدر البيانات الجديد **GroupedTrans**، ثم قم بتكوينه بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="a2847-361">Name the new data source **GroupedTrans**, and configure it in the following way:</span></span>

    - <span data-ttu-id="a2847-362">حدد مصدر بيانات **الحركة** كمصدر للسجلات التي يجب تجميعها.</span><span class="sxs-lookup"><span data-stu-id="a2847-362">Select the **Trans** data source as the source of records that should be grouped.</span></span>
    - <span data-ttu-id="a2847-363">في حقل **موقع التنفيذ**، حدد **استعلام** لتحديد انك تريد تشغيل مصدر البيانات هذا على مستوي قاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="a2847-363">In the **Execution location** field, select **Query** to specify that you want to run this data source at the database level.</span></span>

    ![تكوين مصدر البيانات على صفحه تحرير معلمات "التجميع حسب"](./media/er-components-inspections-05a.gif)

6. <span data-ttu-id="a2847-365">حدد **التحقق من الصحة** لفحص مكون تعيين النموذج القابل للتحرير على صفحة **مصمم تعيين النموذج** وتحقق من إمكانية الاستعلام عن مصدر بيانات **GroupedTrans**.</span><span class="sxs-lookup"><span data-stu-id="a2847-365">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page and verify that the configured **GroupedTrans** data source can be queried.</span></span>
7. <span data-ttu-id="a2847-366">قم بتعديل مصدر بيانات **الحركة** عن طريق أضافه حقل متداخل **لنوع الحقل المحسوب** للحصول علي رقم حساب المورد الذي تم اقتطاعه.</span><span class="sxs-lookup"><span data-stu-id="a2847-366">Modify the **Trans** data source by adding a nested field of the **Calculated field** type to get the trimmed vendor account number.</span></span>
8. <span data-ttu-id="a2847-367">قم بتسميه مصدر البيانات الجديد **$AccNumber**، وقم بتكوينه بحيث يحتوي علي التعبير `TRIM(Trans.AccountNum)`.</span><span class="sxs-lookup"><span data-stu-id="a2847-367">Name the new data source **$AccNumber**, and configure it so that it contains the expression `TRIM(Trans.AccountNum)`.</span></span>

    ![تكوين مصدر البيانات في صفحة مصمم تعيين النموذج](./media/er-components-inspections-05a.png)

9. <span data-ttu-id="a2847-369">حدد **التحقق من الصحة** لفحص مكون تعيين النموذج القابل للتحرير على صفحة **مصمم تعيين النموذج** وتحقق من إمكانية الاستعلام عن مصدر بيانات **GroupedTrans**.</span><span class="sxs-lookup"><span data-stu-id="a2847-369">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page and verify that the configured **GroupedTrans** data source can be queried.</span></span>

    ![التحقق من صحة مكون تعيين نموذج التقارير الإلكترونية (ER) والتحقق من أنه يمكن الاستعلام عن مصدر البيانات GroupedTrans في صفحة مصمم تعيين النموذج](./media/er-components-inspections-05b.png)

10. <span data-ttu-id="a2847-371">لاحظ حدوث خطا في التحقق من الصحة، نظرا لان مصدر بيانات **الحركة** يحتوي علي حقل متداخل من نوع **الحقل المحسوب** الذي لا يسمح بترجمة استدعاء مصدر البيانات **GroupedTrans** إلى عبارة SQL المباشرة.</span><span class="sxs-lookup"><span data-stu-id="a2847-371">Notice that a validation error occurs, because the **Trans** data source contains a nested field of the **Calculated field** type that doesn't allow the call for the **GroupedTrans** data source to be translated to the direct SQL statement.</span></span>

<span data-ttu-id="a2847-372">يبين الرسم التوضيحي التالي خطا وقت التشغيل الذي يحدث إذا تجاهلت التحذير وحدد **تشغيل** لتشغيل تنسيق مكون لاستخدام تعيين النموذج.</span><span class="sxs-lookup"><span data-stu-id="a2847-372">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run a format that is configured to use the model mapping.</span></span>

![أخطاء وقت التشغيل التي تحدث عند تجاهل التحذير في صفحة مصمم التنسيق](./media/er-components-inspections-05c.png)

### <a name="automatic-resolution"></a><span data-ttu-id="a2847-374">الحل التلقائي</span><span class="sxs-lookup"><span data-stu-id="a2847-374">Automatic resolution</span></span>

<span data-ttu-id="a2847-375">لا يتوفر اي خيار لإصلاح هذه المشكلة تلقائيا.</span><span class="sxs-lookup"><span data-stu-id="a2847-375">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="a2847-376">الحل اليدوي</span><span class="sxs-lookup"><span data-stu-id="a2847-376">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="a2847-377">خيار 1</span><span class="sxs-lookup"><span data-stu-id="a2847-377">Option 1</span></span>

<span data-ttu-id="a2847-378">بدلا من أضافه حقل متداخل من نوع **الحقل المحسوب** إلى مصدر بيانات **الحركة**، أضف الحقل المتداخل **$AccNumber** لعنصر **GroupedTrans.lines** الخاص بمصدر بيانات **GroupedTrans**، وقم بتكوينه بحيث يحتوي على التعبير `TRIM(GroupedTrans.lines.AccountNum)`.</span><span class="sxs-lookup"><span data-stu-id="a2847-378">Instead of adding a nested field of the **Calculated field** type to the **Trans** data source, add the **$AccNumber** nested field for the **GroupedTrans.lines** item of the **GroupedTrans** data source, and configure it so that it contains the expression `TRIM(GroupedTrans.lines.AccountNum)`.</span></span> <span data-ttu-id="a2847-379">وبهذه الطريقة، يمكن تشغيل مصدر البيانات **GroupedTrans** في مستوي SQL وحساب الحقل المتداخل **$AccNumber** بعد ذلك.</span><span class="sxs-lookup"><span data-stu-id="a2847-379">In this way, the **GroupedTrans** data source can be run at the SQL level and calculate the **$AccNumber** nested field afterward.</span></span>

#### <a name="option-2"></a><span data-ttu-id="a2847-380">خيار 2</span><span class="sxs-lookup"><span data-stu-id="a2847-380">Option 2</span></span>

<span data-ttu-id="a2847-381">قم بتغيير قيمة حقل **موقع التنفيذ** لمصدر بيانات **GroupedTrans** من **الاستعلام** إلى **في الذاكرة**.</span><span class="sxs-lookup"><span data-stu-id="a2847-381">Change the value of the **Execution location** field for the **GroupedTrans** data source from **Query** to **In memory**.</span></span> <span data-ttu-id="a2847-382">لا نوصي بتغيير قيمة الجدول الذي يحتوي على حجم كبير من البيانات (جدول المعاملات)، لأنه سيتم جلب جميع السجلات، وسيتم الجمع والتجميع في الذاكرة.</span><span class="sxs-lookup"><span data-stu-id="a2847-382">We don't recommend that you change the value for a table that has a large volume of data (transactional table), because all records will be fetched, and grouping and aggregation will be done in memory.</span></span> <span data-ttu-id="a2847-383">لذلك، يمكن ان يتسبب هذا الأسلوب في ضعف الأداء.</span><span class="sxs-lookup"><span data-stu-id="a2847-383">Therefore, this approach can cause poor performance.</span></span>

## <a name="executability-of-a-join-data-source"></a><a id="i6"></a><span data-ttu-id="a2847-384">إمكانية تنفيذ مصدر بيانات الانضمام</span><span class="sxs-lookup"><span data-stu-id="a2847-384">Executability of a JOIN data source</span></span>

<span data-ttu-id="a2847-385">يقوم مصدر بيانات [الانضمام](er-join-data-sources.md) بدمج السجلات من جدولي قاعده بيانات أو أكثر استنادا إلى الحقول المرتبطة.</span><span class="sxs-lookup"><span data-stu-id="a2847-385">The [JOIN](er-join-data-sources.md) data source combines records from two or more database tables, based on related fields.</span></span> <span data-ttu-id="a2847-386">يمكن تكوين كل مصدر بيانات **انضمام** بحيث يتم تشغيله اما في مستوي قاعده البيانات أو في الذاكرة.</span><span class="sxs-lookup"><span data-stu-id="a2847-386">Every **JOIN** data source can be configured so that it's run either at the database level or in memory.</span></span> <span data-ttu-id="a2847-387">عند تكوين مصدر بيانات **الانضمام** بحيث يتم تشغيله علي مستوي قاعده البيانات، تقوم التقارير الإلكترونية بالتحقق مما إذا كان من الممكن تاسيس استعلام SQL مباشر إلى مصادر بيانات يتم الاشاره اليها في مصدر البيانات هذا أو لا.</span><span class="sxs-lookup"><span data-stu-id="a2847-387">When a **JOIN** data source is configured so that it's run at the database level, ER checks whether a direct SQL query can be established to data sources that are referred to in that data source.</span></span> <span data-ttu-id="a2847-388">إذا تعذر إنشاء استعلام SQL مباشر باستخدام مصدر بيانات مرجعي واحد على الأقل، فسيحدث خطأ في التحقق من الصحة في مصمم تعيين نموذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a2847-388">If a direct SQL query can't be established with at least one referenced data source, a validation error occurs in the ER model mapping designer.</span></span> <span data-ttu-id="a2847-389">توضح الرسالة التي تتلقاها انه لا يمكن تشغيل مصدر بيانات **الانضمام** المكون في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="a2847-389">The message that you receive states that the configured **JOIN** data source can't be run at runtime.</span></span>

<span data-ttu-id="a2847-390">توضح الخطوات التالية كيفيه حدوث هذه المشكلة.</span><span class="sxs-lookup"><span data-stu-id="a2847-390">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a2847-391">ابدأ بتكوين مكون تعيين نموذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a2847-391">Start to configure the ER model mapping component.</span></span>
2. <span data-ttu-id="a2847-392">أضف مصدر بيانات من نوع **Dynamics 365 for Operations \\ سجلات الجداول**.</span><span class="sxs-lookup"><span data-stu-id="a2847-392">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="a2847-393">قم بتسمية مصدر البيانات الجديد **المورد**.</span><span class="sxs-lookup"><span data-stu-id="a2847-393">Name the new data source **Vendor**.</span></span> <span data-ttu-id="a2847-394">في حقل **الجدول**، حدد **VendTable** لتحديد أن مصدر البيانات سيطلب الجدول VendTable.</span><span class="sxs-lookup"><span data-stu-id="a2847-394">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
4. <span data-ttu-id="a2847-395">أضف مصدر بيانات من نوع **Dynamics 365 for Operations \\ سجلات الجداول**.</span><span class="sxs-lookup"><span data-stu-id="a2847-395">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
5. <span data-ttu-id="a2847-396">قم بتسمية مصدر البيانات الجديد **Trans**. في حقل **الجدول**، حدد **VendTrans** لتحديد أن مصدر البيانات هذا سيطلب جدول VendTrans.</span><span class="sxs-lookup"><span data-stu-id="a2847-396">Name the new data source **Trans**. In the **Table** field, select **VendTrans** to specify that this data source will request the VendTrans table.</span></span>
6. <span data-ttu-id="a2847-397">أضف مصدر بيانات من نوع **الحقل المحسوب** كحقل متداخل لمصدر بيانات **المورد**.</span><span class="sxs-lookup"><span data-stu-id="a2847-397">Add a data source of the **Calculated field** type as the nested field of the **Vendor** data source.</span></span>
7. <span data-ttu-id="a2847-398">قم بتسميه مصدر البيانات الجديد **FilteredTrans**، وقم بتكوينه بحيث يحتوي علي التعبير `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`.</span><span class="sxs-lookup"><span data-stu-id="a2847-398">Name the new data source **FilteredTrans**, and configure it so that it contains the expression `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`.</span></span>
8. <span data-ttu-id="a2847-399">أضف مصدر بيانات من نوع **الانضمام**.</span><span class="sxs-lookup"><span data-stu-id="a2847-399">Add a data source of the **Join** type.</span></span>
9. <span data-ttu-id="a2847-400">قم بتسميه مصدر البيانات الجديد **JoinedList**، ثم قم بتكوينه بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="a2847-400">Name the new data source **JoinedList**, and configure it in the following way:</span></span>

    1. <span data-ttu-id="a2847-401">أضف مصدر بيانات **المورد** كمجموعه السجلات الاولي المراد الانضمام اليها.</span><span class="sxs-lookup"><span data-stu-id="a2847-401">Add the **Vendor** data source as the first set of records to join.</span></span>
    2. <span data-ttu-id="a2847-402">أضف مصدر بيانات **Vendor.FilteredTrans** كمجموعه السجلات الثانية المراد الانضمام اليها.</span><span class="sxs-lookup"><span data-stu-id="a2847-402">Add the **Vendor.FilteredTrans** data source as the second set of records to join.</span></span> <span data-ttu-id="a2847-403">حدد **داخلي** باعتباره النوع.</span><span class="sxs-lookup"><span data-stu-id="a2847-403">Select **INNER** as the type.</span></span>
    3. <span data-ttu-id="a2847-404">في حقل **التنفيذ**، حدد **استعلام** لتحديد انك تريد تشغيل مصدر البيانات هذا على مستوي قاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="a2847-404">In the **Execute** field, select **Query** to specify that you want to run this data source at the database level.</span></span>

    ![تكوين مصدر البيانات في صفحة مصمم الانضمام](./media/er-components-inspections-06a.gif)

10. <span data-ttu-id="a2847-406">حدد **التحقق من الصحة** لفحص مكون تعيين النموذج القابل للتحرير على صفحة **مصمم تعيين النموذج** وتحقق من إمكانية الاستعلام عن مصدر بيانات **JoinedList**.</span><span class="sxs-lookup"><span data-stu-id="a2847-406">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page and verify that the configured **JoinedList** data source can be queried.</span></span>
11. <span data-ttu-id="a2847-407">قم بتغيير التعبير الخاص بمصدر بيانات **Vendor.FilteredTrans** من `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`إلى `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)`.</span><span class="sxs-lookup"><span data-stu-id="a2847-407">Change the expression of the **Vendor.FilteredTrans** data source from `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)` to `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)`.</span></span>
12. <span data-ttu-id="a2847-408">حدد **التحقق من الصحة** لفحص مكون تعيين النموذج القابل للتحرير على صفحة **مصمم تعيين النموذج** وتحقق من إمكانية الاستعلام عن مصدر بيانات **JoinedList**.</span><span class="sxs-lookup"><span data-stu-id="a2847-408">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page and verify that the configured **JoinedList** data source can be queried.</span></span>

    ![التحقق من صحة مكون تعيين النموذج القابل للتحرير والتحقق من إمكانية الاستعلام عن مصدر بيانات JoinedList في صفحة مصمم تعيين النموذج](./media/er-components-inspections-06b.png)

13. <span data-ttu-id="a2847-410">لاحظ حدوث خطأ في التحقق من الصحة، لأن التعبير عن مصدر بيانات **Vendor.FilteredTrans** لا يمكن ترجمته إلى استدعاء SQL المباشر.</span><span class="sxs-lookup"><span data-stu-id="a2847-410">Notice that a validation error occurs, because the expression of the **Vendor.FilteredTrans** data source can't be translated to the direct SQL call.</span></span> <span data-ttu-id="a2847-411">بالاضافه إلى ذلك، لا يسمح استدعاء SQL المباشر بترجمة الاستدعاء لمصدر بيانات **JoinedList** إلى عبارة SQL المباشرة.</span><span class="sxs-lookup"><span data-stu-id="a2847-411">Additionally, the direct SQL call doesn't allow the call for the **JoinedList** data source to be translated to the direct SQL statement.</span></span>

    ![أخطاء وقت التشغيل من فشل التحقق من صحة مصدر بيانات JoinList في صفحة مصمم تعيين النموذج](./media/er-components-inspections-06c.png)

<span data-ttu-id="a2847-413">يبين الرسم التوضيحي التالي خطا وقت التشغيل الذي يحدث إذا تجاهلت التحذير وحدد **تشغيل** لتشغيل تنسيق مكون لاستخدام تعيين النموذج.</span><span class="sxs-lookup"><span data-stu-id="a2847-413">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run a format that is configured to use the model mapping.</span></span>

![تشغيل التنسيق القابل للتحرير علي صفحه مصمم التنسيق](./media/er-components-inspections-06e.png)

### <a name="automatic-resolution"></a><span data-ttu-id="a2847-415">الحل التلقائي</span><span class="sxs-lookup"><span data-stu-id="a2847-415">Automatic resolution</span></span>

<span data-ttu-id="a2847-416">لا يتوفر اي خيار لإصلاح هذه المشكلة تلقائيا.</span><span class="sxs-lookup"><span data-stu-id="a2847-416">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="a2847-417">الحل اليدوي</span><span class="sxs-lookup"><span data-stu-id="a2847-417">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="a2847-418">خيار 1</span><span class="sxs-lookup"><span data-stu-id="a2847-418">Option 1</span></span>

<span data-ttu-id="a2847-419">قم بتغيير تعبير مصدر بيانات **Vendor.FilteredTrans** من `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)` مرة أخرى إلى `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`، عند إرشادك إلى التحذير.</span><span class="sxs-lookup"><span data-stu-id="a2847-419">Change the expression of the **Vendor.FilteredTrans** data source from `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)` back to `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`, as the warning advised.</span></span>

![تعبير محدث لمصدر البيانات في صفحة مصمم تعيين النموذج](./media/er-components-inspections-06d.png)

#### <a name="option-2"></a><span data-ttu-id="a2847-421">خيار 2</span><span class="sxs-lookup"><span data-stu-id="a2847-421">Option 2</span></span>

<span data-ttu-id="a2847-422">قم بتغيير قيمة حقل **التنفيذ** لمصدر بيانات **JoinedList** من **الاستعلام** إلى **في الذاكرة**.</span><span class="sxs-lookup"><span data-stu-id="a2847-422">Change the value of the **Execute** field for the **JoinedList** data source from **Query** to **In memory**.</span></span> <span data-ttu-id="a2847-423">لا نوصي بتغيير قيمة الجدول الذي يحتوي على حجم كبير من البيانات (جدول المعاملات)، لأنه سيتم جلب جميع السجلات، وسيتم الانضمام في الذاكرة.</span><span class="sxs-lookup"><span data-stu-id="a2847-423">We don't recommend that you change the value for a table that has a large volume of data (transactional table), because all records will be fetched, and the join occurs in memory.</span></span> <span data-ttu-id="a2847-424">لذلك، يمكن ان يتسبب هذا الأسلوب في ضعف الأداء.</span><span class="sxs-lookup"><span data-stu-id="a2847-424">Therefore, this approach can cause poor performance.</span></span> <span data-ttu-id="a2847-425">يظهر تحذير التحقق من الصحة لاعلامك بهذه المخاطرة.</span><span class="sxs-lookup"><span data-stu-id="a2847-425">A validation warning is shown to inform you about this risk.</span></span>

## <a name="preferability-of-filter-vs-where-function"></a><a id="i7"></a><span data-ttu-id="a2847-426">تفضيل وظيفة التصفية مقابل المكان</span><span class="sxs-lookup"><span data-stu-id="a2847-426">Preferability of FILTER vs WHERE function</span></span>

<span data-ttu-id="a2847-427">يتم استخدام وظيفة [تصفية](er-functions-list-filter.md) التقارير الإلكترونية المضمنة للوصول إلى جداول التطبيق أو طرق العرض أو كيانات البيانات عن طريق وضع استدعاء SQL مفرد للحصول علي البيانات المطلوبة كقائمه سجلات.</span><span class="sxs-lookup"><span data-stu-id="a2847-427">The built-in [FILTER](er-functions-list-filter.md) ER function is used to access application tables, views, or data entities by placing a single SQL call to get the required data as a list of records.</span></span> <span data-ttu-id="a2847-428">تقوم وظيفة [المكان](er-functions-list-where.md) بجلب كافة السجلات من المصدر المحدد وتقوم بتحديد السجل في الذاكرة.</span><span class="sxs-lookup"><span data-stu-id="a2847-428">The [WHERE](er-functions-list-where.md) function fetches all records from the given source and does record selection in memory.</span></span> <span data-ttu-id="a2847-429">يتم استخدام مصدر بيانات من نوع **قائمة السجلات** كوسيطة لكلٍّ من الوظيفتين ويحدد مصدرًا للحصول على السجلات.</span><span class="sxs-lookup"><span data-stu-id="a2847-429">A data source of the **Record list** type is used as an argument of both functions and specifies a source for getting records.</span></span> <span data-ttu-id="a2847-430">يقوم التقارير الإلكترونية بالتحقق مما إذا كان من الممكن إنشاء استدعاء SQL مباشر إلى مصدر بيانات يشار إليه في وظيفة **المكان**.</span><span class="sxs-lookup"><span data-stu-id="a2847-430">ER checks whether a direct SQL call can be established to a data source that is referred to in the **WHERE** function.</span></span> <span data-ttu-id="a2847-431">في حاله تعذر إنشاء الاستدعاء المباشر، يحدث تحذير في التحقق من الصحة في مصمم تعيين نموذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a2847-431">If a direct call can be established, a validation warning occurs in the ER model mapping designer.</span></span> <span data-ttu-id="a2847-432">توصي الرسالة التي تظهر لك باستخدام وظيفة **التصفية** بدلاً من وظيفة **المكان** للمساعدة في تحسين الكفاءة.</span><span class="sxs-lookup"><span data-stu-id="a2847-432">The message that you receive recommends that you use the **FILTER** function instead of the **WHERE** function to help improve efficiency.</span></span>

<span data-ttu-id="a2847-433">توضح الخطوات التالية كيفيه حدوث هذه المشكلة.</span><span class="sxs-lookup"><span data-stu-id="a2847-433">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a2847-434">ابدأ بتكوين مكون تعيين نموذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a2847-434">Start to configure the ER model mapping component.</span></span>
2. <span data-ttu-id="a2847-435">أضف مصدر بيانات من نوع **Dynamics 365 for Operations \\ سجلات الجداول**.</span><span class="sxs-lookup"><span data-stu-id="a2847-435">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="a2847-436">قم بتسمية مصدر البيانات الجديد **Trans**. في حقل **الجدول**، حدد **VendTrans** لتحديد أن مصدر البيانات هذا سيطلب جدول VendTrans.</span><span class="sxs-lookup"><span data-stu-id="a2847-436">Name the new data source **Trans**. In the **Table** field, select **VendTrans** to specify that this data source will request the VendTrans table.</span></span>
4. <span data-ttu-id="a2847-437">أضف مصدر بيانات من نوع **الحقل المحسوب** كحقل متداخل لمصدر بيانات **المورد**.</span><span class="sxs-lookup"><span data-stu-id="a2847-437">Add a data source of the **Calculated field** type as the nested field of the **Vendor** data source.</span></span>
5. <span data-ttu-id="a2847-438">قم بتسميه مصدر البيانات الجديد **FilteredTrans**، وقم بتكوينه بحيث يحتوي علي التعبير `WHERE(Trans, Trans.AccountNum="US-101")`.</span><span class="sxs-lookup"><span data-stu-id="a2847-438">Name the new data source **FilteredTrans**, and configure it so that it contains the expression `WHERE(Trans, Trans.AccountNum="US-101")`.</span></span>
6. <span data-ttu-id="a2847-439">أضف مصدر بيانات من نوع **Dynamics 365 for Operations \\ سجلات الجداول**.</span><span class="sxs-lookup"><span data-stu-id="a2847-439">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
7. <span data-ttu-id="a2847-440">قم بتسمية مصدر البيانات الجديد **المورد**.</span><span class="sxs-lookup"><span data-stu-id="a2847-440">Name the new data source **Vendor**.</span></span> <span data-ttu-id="a2847-441">في حقل **الجدول**، حدد **VendTable** لتحديد أن مصدر البيانات سيطلب الجدول VendTable.</span><span class="sxs-lookup"><span data-stu-id="a2847-441">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
8. <span data-ttu-id="a2847-442">أضف مصدر بيانات من نوع **الحقل المحسوب**.</span><span class="sxs-lookup"><span data-stu-id="a2847-442">Add a data source of the **Calculated field** type.</span></span>
9. <span data-ttu-id="a2847-443">قم بتسميه مصدر البيانات الجديد **FilteredVendor**، وقم بتكوينه بحيث يحتوي علي التعبير `WHERE(Vendor, Vendor.AccountNum="US-101")`.</span><span class="sxs-lookup"><span data-stu-id="a2847-443">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `WHERE(Vendor, Vendor.AccountNum="US-101")`.</span></span>
10. <span data-ttu-id="a2847-444">حدد **التحقق من الصحة** لفحص مكون تعيين النموذج القابل للتحرير في صفحه **مصمم تعيين النموذج**.</span><span class="sxs-lookup"><span data-stu-id="a2847-444">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page.</span></span>

    ![فحص مكون تعيين نموذج قابل للتحرير في صفحة مصمم تعيين النموذج](./media/er-components-inspections-07a.png)

11. <span data-ttu-id="a2847-446">لاحظ أن تحذيرات التحقق من الصحة توصي باستخدام وظيفة **التصفية** بدلاً من وظيفة **المكان** لمصدري البيانات **FilteredVendor** و **FilteredTrans**.</span><span class="sxs-lookup"><span data-stu-id="a2847-446">Notice that validation warnings recommend that you use the **FILTER** function instead of the **WHERE** function for the **FilteredVendor** and **FilteredTrans** data sources.</span></span>

    ![توصيات لاستخدام وظيفة FILTER بدلا من وظيفة WHERE في صفحة مصمم تعيين النموذج](./media/er-components-inspections-07b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="a2847-448">الحل التلقائي</span><span class="sxs-lookup"><span data-stu-id="a2847-448">Automatic resolution</span></span>

<span data-ttu-id="a2847-449">حدد **إصلاح** لاستبدال وظيفة **المكان** تلقائيًا بوظيفة **التصفية** في التعبير الخاص بكافة مصادر البيانات التي تظهر في الشبكة في علامة التبويب **تحذيرات** لهذا النوع من الفحص.</span><span class="sxs-lookup"><span data-stu-id="a2847-449">Select **Fix** to automatically replace the **WHERE** function with the **FILTER** function in the expression of all data sources that appear in the grid on the **Warnings** tab for this type of inspection.</span></span>

<span data-ttu-id="a2847-450">وبدلاً من ذلك، يمكنك تحديد الصف لأحد التحذيرات الفردية في الشبكة ثم حدد **تم تحديد الإصلاح**.</span><span class="sxs-lookup"><span data-stu-id="a2847-450">Alternatively, you can select the row for a single warning in the grid and then select **Fix selected**.</span></span> <span data-ttu-id="a2847-451">في هذه الحالة، يتم تغيير التعبير تلقائيا في مصدر البيانات المذكور في التحذير المحدد.</span><span class="sxs-lookup"><span data-stu-id="a2847-451">In this case, the expression is automatically changed only in the data source that is mentioned in the selected warning.</span></span>

![تحديد الإصلاح لاستبدال وظيفة WHERE تلقائيًا بوظيفة FILTER في صفحة مصمم تعيين النموذج](./media/er-components-inspections-07c.png)

### <a name="manual-resolution"></a><span data-ttu-id="a2847-453">الحل اليدوي</span><span class="sxs-lookup"><span data-stu-id="a2847-453">Manual resolution</span></span>

<span data-ttu-id="a2847-454">يمكنك ضبط التعبيرات الخاصة بكافة مصادر البيانات المذكورة في شبكه التحقق من الصحة يدويا وذلك باستبدال وظيفة **المكان** بوظيفة **التصفية**.</span><span class="sxs-lookup"><span data-stu-id="a2847-454">You can manually adjust the expressions of all the data sources in the validation grid by replacing the **WHERE** function with the **FILTER** function.</span></span>

## <a name="preferability-of-allitemsquery-vs-allitems-function"></a><a id="i8"></a><span data-ttu-id="a2847-455">تفضيل وظيفة ALLITEMSQUERY مقابل ALLITEMS</span><span class="sxs-lookup"><span data-stu-id="a2847-455">Preferability of ALLITEMSQUERY vs ALLITEMS function</span></span>

<span data-ttu-id="a2847-456">يتم استخدام وظيفتي التقارير الإلكترونية [ALLITEMS](er-functions-list-allitems.md) و [ALLITEMSQUERY](er-functions-list-allitemsquery.md) المدمجتين للحصول على قيمة **قائمة السجلات** المسطحة التي تحتوي على قائمة السجلات التي تمثل جميع العناصر التي تطابق المسار المحدد.</span><span class="sxs-lookup"><span data-stu-id="a2847-456">The built-in [ALLITEMS](er-functions-list-allitems.md) and [ALLITEMSQUERY](er-functions-list-allitemsquery.md) ER functions return a flattened **Record list** value that consists of a list of records that represent all items that match the specified path.</span></span> <span data-ttu-id="a2847-457">يقوم التقارير الإلكترونية بالتحقق مما إذا كان من الممكن إنشاء استدعاء SQL مباشر إلى مصدر بيانات يشار إليه في وظيفة **ALLITEMS**.</span><span class="sxs-lookup"><span data-stu-id="a2847-457">ER checks whether a direct SQL call can be established to a data source that is referred to in the **ALLITEMS** function.</span></span> <span data-ttu-id="a2847-458">في حاله تعذر إنشاء الاستدعاء المباشر، يحدث تحذير في التحقق من الصحة في مصمم تعيين نموذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a2847-458">If a direct call can be established, a validation warning occurs in the ER model mapping designer.</span></span> <span data-ttu-id="a2847-459">توصي الرسالة التي تظهر لك باستخدام وظيفة **ALLITEMSQUERY** بدلاً من وظيفة **ALLITEMS** للمساعدة في تحسين الكفاءة.</span><span class="sxs-lookup"><span data-stu-id="a2847-459">The message that you receive recommends that you use the **ALLITEMSQUERY** function instead of the **ALLITEMS** function to help improve efficiency.</span></span>

<span data-ttu-id="a2847-460">توضح الخطوات التالية كيفيه حدوث هذه المشكلة.</span><span class="sxs-lookup"><span data-stu-id="a2847-460">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a2847-461">ابدأ بتكوين مكون تعيين نموذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a2847-461">Start to configure the ER model mapping component.</span></span>
2. <span data-ttu-id="a2847-462">أضف مصدر بيانات من نوع **Dynamics 365 for Operations \\ سجلات الجداول**.</span><span class="sxs-lookup"><span data-stu-id="a2847-462">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="a2847-463">قم بتسمية مصدر البيانات الجديد **المورد**.</span><span class="sxs-lookup"><span data-stu-id="a2847-463">Name the new data source **Vendor**.</span></span> <span data-ttu-id="a2847-464">في حقل **الجدول**، حدد **VendTable** لتحديد أن مصدر البيانات سيطلب الجدول VendTable.</span><span class="sxs-lookup"><span data-stu-id="a2847-464">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
4. <span data-ttu-id="a2847-465">أضف مصدر بيانات من نوع **الحقل المحسوب** للحصول على سجلات للعديد من الموردين.</span><span class="sxs-lookup"><span data-stu-id="a2847-465">Add a data source of the **Calculated field** type to get records for several vendors.</span></span>
5. <span data-ttu-id="a2847-466">قم بتسميه مصدر البيانات الجديد **FilteredVendor**، وقم بتكوينه بحيث يحتوي علي التعبير `FILTER(Vendor, OR(Vendor.AccountNum="US-101",Vendor.AccountNum="US-102"))`.</span><span class="sxs-lookup"><span data-stu-id="a2847-466">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, OR(Vendor.AccountNum="US-101",Vendor.AccountNum="US-102"))`.</span></span>
6. <span data-ttu-id="a2847-467">أضف مصدر بيانات من نوع **الحقل المحسوب** للحصول على حركات جميع الموردين الذين تمت تصفيتهم.</span><span class="sxs-lookup"><span data-stu-id="a2847-467">Add a data source of the **Calculated field** type to get the transactions of all filtered vendors.</span></span>
7. <span data-ttu-id="a2847-468">قم بتسميه مصدر البيانات الجديد **FilteredVendor**، وقم بتكوينه بحيث يحتوي على التعبير `ALLITEMS(FilteredVendor.'<Relations'.'VendTrans.VendTable_AccountNum')`.</span><span class="sxs-lookup"><span data-stu-id="a2847-468">Name the new data source **FilteredVendorTrans**, and configure it so that it contains the expression `ALLITEMS(FilteredVendor.'<Relations'.'VendTrans.VendTable_AccountNum')`.</span></span>
8. <span data-ttu-id="a2847-469">حدد **التحقق من الصحة** لفحص مكون تعيين النموذج القابل للتحرير في صفحه **مصمم تعيين النموذج**.</span><span class="sxs-lookup"><span data-stu-id="a2847-469">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page.</span></span>

    ![فحص مكون تعيين نموذج التقارير الإلكترونية (ER) القابل للتحرير في صفحة مصمم تعيين النموذج](./media/er-components-inspections-08a.png)

9. <span data-ttu-id="a2847-471">لاحظ حدوث تحذير في التحقق من الصحة.</span><span class="sxs-lookup"><span data-stu-id="a2847-471">Notice that a validation warning occurs.</span></span> <span data-ttu-id="a2847-472">وتوصيك الرسالة باستخدام وظيفة **ALLITEMSQUERY** بدلاً من وظيفة **ALLITEMS** لمصدر بيانات **FilteredVendorTrans**.</span><span class="sxs-lookup"><span data-stu-id="a2847-472">The message recommends that you use the **ALLITEMSQUERY** function instead of the **ALLITEMS** function for the **FilteredVendorTrans** data source.</span></span>

    ![توصيات لاستخدام وظيفة ALLITEMSQUERY بدلا من وظيفة ALLITEMS في صفحة مصمم تعيين النموذج](./media/er-components-inspections-08b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="a2847-474">الحل التلقائي</span><span class="sxs-lookup"><span data-stu-id="a2847-474">Automatic resolution</span></span>

<span data-ttu-id="a2847-475">حدد **إصلاح** لاستبدال وظيفة **ALLITEMS** تلقائيًا بوظيفة **ALLITEMSQUERY** في التعبير الخاص بكافة مصادر البيانات التي تظهر في الشبكة في علامة التبويب **تحذيرات** لهذا النوع من الفحص.</span><span class="sxs-lookup"><span data-stu-id="a2847-475">Select **Fix** to automatically replace the **ALLITEMS** function with the **ALLITEMSQUERY** function in the expression of all data sources that appear in the grid on the **Warnings** tab for this type of inspection.</span></span>

<span data-ttu-id="a2847-476">وبدلاً من ذلك، يمكنك تحديد الصف لأحد التحذيرات الفردية في الشبكة ثم حدد **تم تحديد الإصلاح**.</span><span class="sxs-lookup"><span data-stu-id="a2847-476">Alternatively, you can select the row for a single warning in the grid and then select **Fix selected**.</span></span> <span data-ttu-id="a2847-477">في هذه الحالة، يتم تغيير التعبير تلقائيا في مصدر البيانات المذكور في التحذير المحدد.</span><span class="sxs-lookup"><span data-stu-id="a2847-477">In this case, the expression is automatically changed only in the data source that is mentioned in the selected warning.</span></span>

![تحديد الإصلاح المحدد في صفحة مصمم تعيين النموذج](./media/er-components-inspections-08c.png)

### <a name="manual-resolution"></a><span data-ttu-id="a2847-479">الحل اليدوي</span><span class="sxs-lookup"><span data-stu-id="a2847-479">Manual resolution</span></span>

<span data-ttu-id="a2847-480">يمكنك ضبط التعبيرات الخاصة بكافة مصادر البيانات المذكورة في شبكه التحقق من الصحة يدويا وذلك باستبدال وظيفة **ALLITEMS** بوظيفة **ALLITEMSQUERY**.</span><span class="sxs-lookup"><span data-stu-id="a2847-480">You can manually adjust the expressions of all the data sources that are mentioned in the validation grid by replacing the **ALLITEMS** function with the **ALLITEMSQUERY** function.</span></span>

## <a name="consideration-of-empty-list-cases"></a><a id="i9"></a><span data-ttu-id="a2847-481">اعتبار حالات القائمة الفارغة</span><span class="sxs-lookup"><span data-stu-id="a2847-481">Consideration of empty list cases</span></span>

<span data-ttu-id="a2847-482">يمكنك تكوين التنسيق الخاص بك أو مكون تعيين النموذج للحصول علي قيمه الحقل لمصدر البيانات الخاص بنوع **قائمة السجلات**.</span><span class="sxs-lookup"><span data-stu-id="a2847-482">You can configure your ER format or model mapping component to get the field value of a data source of the **Record list** type.</span></span> <span data-ttu-id="a2847-483">يقوم التقارير الإلكترونية بفحص ما إذا كان تصميمك يعتبر الحالة التي لا يحتوي فيها مصدر بيانات يسمي علي إيه سجلات (اي انه فارغ)، لتجنب أخطاء وقت التشغيل عند إحضار أحدي القيم من أحد حقول السجلات غير الموجودة.</span><span class="sxs-lookup"><span data-stu-id="a2847-483">ER checks whether your design considers the case where a data source that is called contains no records (that is, it's empty), to prevent runtime errors when a value is fetched from a field of a nonexistent record.</span></span>

<span data-ttu-id="a2847-484">توضح الخطوات التالية كيفيه حدوث هذه المشكلة.</span><span class="sxs-lookup"><span data-stu-id="a2847-484">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a2847-485">ابدأ في تكوين نموذج بيانات التقارير الإلكترونية وتعيين نموذج التقارير الإلكترونية ومكونات تنسيق التقارير الإلكترونية في وقت واحد.</span><span class="sxs-lookup"><span data-stu-id="a2847-485">Start to configure the ER data model, the ER model mapping, and the ER format components simultaneously.</span></span>
2. <span data-ttu-id="a2847-486">في شجرة نموذج البيانات، قم باضافه العنصر الجذر المسمى **الجذر 3**.</span><span class="sxs-lookup"><span data-stu-id="a2847-486">In the data model tree, add a root item that is named **Root3**.</span></span>
3. <span data-ttu-id="a2847-487">قم بتعديل عنصر **الجذر 3** عن طريق إضافة عنصر متداخل من نوع **قائمة السجلات**.</span><span class="sxs-lookup"><span data-stu-id="a2847-487">Modify the **Root3** item by adding a nested item of the **Record list** type.</span></span>
4. <span data-ttu-id="a2847-488">قم بتسمية العنصر المتداخل الجديد **المورد**.</span><span class="sxs-lookup"><span data-stu-id="a2847-488">Name the new nested item **Vendor**.</span></span>
5. <span data-ttu-id="a2847-489">قم بتعديل عنصر **المورد** بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="a2847-489">Modify the **Vendor** item in the following way:</span></span>

    - <span data-ttu-id="a2847-490">أضف حقلاً متداخلاً من نوع **السلسلة**، وقم بتسميته بـ **اسم**.</span><span class="sxs-lookup"><span data-stu-id="a2847-490">Add a nested field of the **String** type, and name it **Name**.</span></span>
    - <span data-ttu-id="a2847-491">أضف حقلاً متداخلاً من نوع **السلسلة**، وقم بتسميته بـ **AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="a2847-491">Add a nested field of the **String** type, and name it **AccountNumber**.</span></span>

    ![إضافة حقول متداخلة في صفحة نموذج البيانات](./media/er-components-inspections-09a.png)

6. <span data-ttu-id="a2847-493">في مصمم تعيين النموذج، في جزء **مصادر البيانات**، أضف مصدر بيانات من نوع **Dynamics 365 for Operations \\سجلات الجدول**.</span><span class="sxs-lookup"><span data-stu-id="a2847-493">In the model mapping designer, in the **Data sources** pane, add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
7. <span data-ttu-id="a2847-494">قم بتسمية مصدر البيانات الجديد **المورد**.</span><span class="sxs-lookup"><span data-stu-id="a2847-494">Name the new data source **Vendor**.</span></span> <span data-ttu-id="a2847-495">في حقل **الجدول**، حدد **VendTable** لتحديد أن مصدر البيانات سيطلب الجدول VendTable.</span><span class="sxs-lookup"><span data-stu-id="a2847-495">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
8. <span data-ttu-id="a2847-496">أضف مصدر بيانات من نوع **عام \\ معلمة إدخال المستخدم** للبحث عن حساب مورد في مربع حوار وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="a2847-496">Add a data source of the **General \\ User input parameter** type to search for a vendor account in the runtime dialog box.</span></span>
9. <span data-ttu-id="a2847-497">قم بتسمية مصدر البيانات الجديد **RequestedAccountNum**.</span><span class="sxs-lookup"><span data-stu-id="a2847-497">Name the new data source **RequestedAccountNum**.</span></span> <span data-ttu-id="a2847-498">في حقل **التسمية**، أدخل **رقم حساب المورد**.</span><span class="sxs-lookup"><span data-stu-id="a2847-498">In the **Label** field, enter **Vendor account number**.</span></span> <span data-ttu-id="a2847-499">في حقل **اسم نوع بيانات Operations**، اترك القيمة الافتراضية، وهي **الوصف**.</span><span class="sxs-lookup"><span data-stu-id="a2847-499">In the **Operations data type name** field, leave the default value, **Description**.</span></span>
10. <span data-ttu-id="a2847-500">أضف مصدر بيانات من نوع **الحقل المحسوب** لتصفية مورد تم الاستعلام عنه.</span><span class="sxs-lookup"><span data-stu-id="a2847-500">Add a data source of the **Calculated field** type to filter a vendor that is inquired about.</span></span>
11. <span data-ttu-id="a2847-501">قم بتسميه مصدر البيانات الجديد **FilteredVendor**، وقم بتكوينه بحيث يحتوي علي التعبير `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.</span><span class="sxs-lookup"><span data-stu-id="a2847-501">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.</span></span>
12. <span data-ttu-id="a2847-502">اربط عناصر نموذج البيانات بمصادر البيانات التي تم تكوينها بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="a2847-502">Bind the data model items to configured data sources in the following way:</span></span>

    - <span data-ttu-id="a2847-503">اربط **FilteredVendor** بـ **المورد**.</span><span class="sxs-lookup"><span data-stu-id="a2847-503">Bind **FilteredVendor** to **Vendor**.</span></span>
    - <span data-ttu-id="a2847-504">اربط **FilteredVendor.AccountNum** بـ **Vendor.AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="a2847-504">Bind **FilteredVendor.AccountNum** to **Vendor.AccountNumber**.</span></span>
    - <span data-ttu-id="a2847-505">اربط **FilteredVendor.'name()'** بـ **Vendor.Name**.</span><span class="sxs-lookup"><span data-stu-id="a2847-505">Bind **FilteredVendor.'name()'** to **Vendor.Name**.</span></span>

    ![ربط عناصر نماذج البيانات في صفحة مصمم تعيين النموذج](./media/er-components-inspections-09b.png)

13. <span data-ttu-id="a2847-507">في شجرة بنية التنسيق، أضف الأصناف التالية لإنشاء مستند صادر بتنسيق XML الذي يحتوي على تفاصيل المورد:</span><span class="sxs-lookup"><span data-stu-id="a2847-507">In the format structure tree, add the following items to generate an outbound document in XML format that contains the vendor details:</span></span>

    1. <span data-ttu-id="a2847-508">أضف عنصر XML الخاص بجذر **العبارة**.</span><span class="sxs-lookup"><span data-stu-id="a2847-508">Add the **Statement** root XML element.</span></span>
    2. <span data-ttu-id="a2847-509">بالنسبة إلى عنصر XML لـ **العبارة**، أضف عنصر XML لـ **الطرف** المتداخل.</span><span class="sxs-lookup"><span data-stu-id="a2847-509">For the **Statement** XML element, add the nested **Party** XML element.</span></span>
    3. <span data-ttu-id="a2847-510">بالنسبة لعناصر XML **للطرف**، أضف سمات XML المتداخلة التالية:</span><span class="sxs-lookup"><span data-stu-id="a2847-510">For the **Party** XML element, add the following nested XML attributes:</span></span>

        - <span data-ttu-id="a2847-511">الاسم</span><span class="sxs-lookup"><span data-stu-id="a2847-511">Name</span></span>
        - <span data-ttu-id="a2847-512">AccountNum</span><span class="sxs-lookup"><span data-stu-id="a2847-512">AccountNum</span></span>

14. <span data-ttu-id="a2847-513">ربط عناصر التنسيق بمصادر البيانات المتوفرة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="a2847-513">Bind format elements to provided data sources in the following way:</span></span>

    - <span data-ttu-id="a2847-514">اربط عنصر تنسيق **العبارة\\الطرف\\الاسم** بحقل مصدر البيانات **model.Vendor.Name**.</span><span class="sxs-lookup"><span data-stu-id="a2847-514">Bind the **Statement\\Party\\Name** format element to the **model.Vendor.Name** data source field.</span></span>
    - <span data-ttu-id="a2847-515">اربط عنصر تنسيق **العبارة\\الطرف\\AccountNum** بحقل مصدر البيانات **model.Vendor.AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="a2847-515">Bind the **Statement\\Party\\AccountNum** format element to the **model.Vendor.AccountNumber** data source field.</span></span>

15. <span data-ttu-id="a2847-516">حدد **التحقق من الصحة** لفحص مكون التنسيق القابل للتحرير في صفحة **مصمم التنسيق**.</span><span class="sxs-lookup"><span data-stu-id="a2847-516">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![التحقق من صحة عناصر التنسيق التي قمت بربطها بمصادر البيانات في صفحة مصمم التنسيق](./media/er-components-inspections-09c.png)

16. <span data-ttu-id="a2847-518">لاحظ حدوث خطا في التحقق من الصحة.</span><span class="sxs-lookup"><span data-stu-id="a2847-518">Notice that a validation error occurs.</span></span> <span data-ttu-id="a2847-519">وتنص الرسالة على أنه قد يظهر خطأ لمكونات تنسيق **العبارة\\الطرف\\الاسم** و **العبارة\\الطرف\\AccountNum** في وقت التشغيل إذا كانت قائمة `model.Vendor` فارغة.</span><span class="sxs-lookup"><span data-stu-id="a2847-519">The message states that an error might be thrown for the configured **Statement\\Party\\Name** and **Statement\\Party\\AccountNum** format components at runtime if the `model.Vendor` list is empty.</span></span>

    ![خطأ في التحقق من الصحة يتعلق بالخطأ المحتمل لمكونات التنسيق المكونة](./media/er-components-inspections-09d.png)

<span data-ttu-id="a2847-521">يبين الرسم التوضيحي التالي خطا وقت التشغيل الذي يحدث إذا تجاهلت التحذير، حدد **تشغيل** لتشغيل التنسيق، وحدد رقم الحساب للمورد غير الموجود.</span><span class="sxs-lookup"><span data-stu-id="a2847-521">The following illustration shows the runtime error that occurs if you ignore the warning, select **Run** to run the format, and select the account number of a nonexistent vendor.</span></span> <span data-ttu-id="a2847-522">لأن المورد المطلوب غير موجود، فستكون قائمة `model.Vendor` فارغة (وهذا يعني أنها لن تحتوي على أي سجلات).</span><span class="sxs-lookup"><span data-stu-id="a2847-522">Because the requested vendor doesn't exist, the `model.Vendor` list will be empty (that is, it will contain no records).</span></span>

![أخطاء وقت التشغيل التي تحدث أثناء تشغيل تعيين التنسيق](./media/er-components-inspections-09e.png)

### <a name="automatic-resolution"></a><span data-ttu-id="a2847-524">الحل التلقائي</span><span class="sxs-lookup"><span data-stu-id="a2847-524">Automatic resolution</span></span>

<span data-ttu-id="a2847-525">بالنسبة للصف المحدد في الشبكة في علامة التبويب **تحذيرات**، يمكنك تحديد **إلغاء الربط**.</span><span class="sxs-lookup"><span data-stu-id="a2847-525">For the selected row in the grid on the **Warnings** tab, you can select **Unbind**.</span></span> <span data-ttu-id="a2847-526">يتم تلقائيا إزالة الربط المشار إليه في عمود **المسار** من عناصر التنسيق.</span><span class="sxs-lookup"><span data-stu-id="a2847-526">The binding that is pointed to in the **Path** column is automatically removed from the format elements.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="a2847-527">الحل اليدوي</span><span class="sxs-lookup"><span data-stu-id="a2847-527">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="a2847-528">خيار 1</span><span class="sxs-lookup"><span data-stu-id="a2847-528">Option 1</span></span>

<span data-ttu-id="a2847-529">يمكنك ربط عنصر تنسيق **العبارة\\الطرف\\الاسم** بعنصر مصدر البيانات `model.Vendor`.</span><span class="sxs-lookup"><span data-stu-id="a2847-529">You can bind the **Statement\\Party\\Name** format element to the `model.Vendor` data source item.</span></span> <span data-ttu-id="a2847-530">في وقت التشغيل، يستدعي هذا الربط مصدر بيانات `model.Vendor` أولاً.</span><span class="sxs-lookup"><span data-stu-id="a2847-530">At runtime, this binding calls the `model.Vendor` data source first.</span></span> <span data-ttu-id="a2847-531">عندما يُرجع `model.Vendor` قائمه سجلات فارغه، لا يتم تشغيل عناصر التنسيق المتداخل.</span><span class="sxs-lookup"><span data-stu-id="a2847-531">When `model.Vendor` returns an empty record list, the nested format elements aren't run.</span></span> <span data-ttu-id="a2847-532">لذلك، لا تحدث أي تحذيرات تحقق من الصحة لتكوين التنسيق هذا.</span><span class="sxs-lookup"><span data-stu-id="a2847-532">Therefore, no validation warnings occur for this format configuration.</span></span>

![ربط عنصر التنسيق بعنصر مصدر البيانات في صفحة مصمم التنسيق](./media/er-components-inspections-09e.gif)

#### <a name="option-2"></a><span data-ttu-id="a2847-534">خيار 2</span><span class="sxs-lookup"><span data-stu-id="a2847-534">Option 2</span></span>

<span data-ttu-id="a2847-535">قم بتغيير ربط عنصر تنسيق **العبارة\\الطرف\\الاسم** من `model.Vendor.Name` إلى `FIRSTORNULL(model.Vendor).Name`.</span><span class="sxs-lookup"><span data-stu-id="a2847-535">Change the binding of the **Statement\\Party\\Name** format element from `model.Vendor.Name` to `FIRSTORNULL(model.Vendor).Name`.</span></span> <span data-ttu-id="a2847-536">يقوم الربط المحدث بتحويل السجل الأول لمصدر بيانات `model.Vendor` الخاص بنوع **قائمة السجلات** لمصدر بيانات جديد من نوع **السجل**.</span><span class="sxs-lookup"><span data-stu-id="a2847-536">The updated binding conditionally converts the first record of the `model.Vendor` data source of the **Record list** type to a new data source of the **Record** type.</span></span> <span data-ttu-id="a2847-537">يحتوي مصدر البيانات الجديد على نفس مجموعة الحقول.</span><span class="sxs-lookup"><span data-stu-id="a2847-537">This new data source contains the same set of fields.</span></span>

- <span data-ttu-id="a2847-538">في حالة توفر سجل واحد على الأقل في مصدر بيانات `model.Vendor`، يتم ملء حقول هذا السجل بقيم الحقول الخاصة بالسجل الأول من مصدر بيانات `model.Vendor`.</span><span class="sxs-lookup"><span data-stu-id="a2847-538">If at least one record is available in the `model.Vendor` data source, the fields of that record are filled with the values of the fields of the first record of the `model.Vendor` data source.</span></span> <span data-ttu-id="a2847-539">في هذه الحالة، يقوم الربط المحدث بإرجاع اسم المورد.</span><span class="sxs-lookup"><span data-stu-id="a2847-539">In this case, the updated binding returns the vendor name.</span></span>
- <span data-ttu-id="a2847-540">وبخلاف ذلك، يتم ملء كل حقل من السجل الذي يتم إنشاؤه بالقيمة الافتراضية لنوع البيانات الخاص بهذا الحقل.</span><span class="sxs-lookup"><span data-stu-id="a2847-540">Otherwise, every field of the record that is created is filled with the default value for the data type of that field.</span></span> <span data-ttu-id="a2847-541">في هذه الحالة، يتم إرجاع السلسلة الفارغة كالقيمة الافتراضية لنوع بيانات **السلسلة**.</span><span class="sxs-lookup"><span data-stu-id="a2847-541">In this case, the blank string is returned as the default value of the **String** data type.</span></span>

<span data-ttu-id="a2847-542">ولذلك، لا تحدث أي تحذيرات في التحقق من الصحة لعنصر تنسيق **العبارة\\الطرف\\الاسم** عند ربطه بتعبير `FIRSTORNULL(model.Vendor).Name`.</span><span class="sxs-lookup"><span data-stu-id="a2847-542">Therefore, no validation warnings occur for the **Statement\\Party\\Name** format element when it's bound to the `FIRSTORNULL(model.Vendor).Name` expression.</span></span>

![الربط المتغير يعمل على حل تحذيرات التحقق من الصحة على صفحة مصمم التنسيق](./media/er-components-inspections-09f.gif)

#### <a name="option-3"></a><span data-ttu-id="a2847-544">خيار 3</span><span class="sxs-lookup"><span data-stu-id="a2847-544">Option 3</span></span>

<span data-ttu-id="a2847-545">إذا كنت تريد تحديد البيانات التي تم إدخالها في مستند مُنشأ بشكل صريح عندما لم يُرجع مصدر بيانات `model.Vendor` لنوع **قائمة السجلات** أي سجلات (النص **غير متوفر** في هذا المثال)، قم بتغيير ربط عنصر تنسيق **العبارة\\الطرف\\الاسم** من `model.Vendor.Name` إلى `IF(NOT(ISEMPTY(model.Vendor)), model.Vendor.Name, "Not available")`.</span><span class="sxs-lookup"><span data-stu-id="a2847-545">If you want to explicitly specify the data that is entered in a generated document when the `model.Vendor` data source of the **Record list** type returns no records (the text **Not available** in this example), change the binding of the **Statement\\Party\\Name** format element from `model.Vendor.Name` to `IF(NOT(ISEMPTY(model.Vendor)), model.Vendor.Name, "Not available")`.</span></span> <span data-ttu-id="a2847-546">يمكنك أيضًا استخدام التعبير `IF(COUNT(model.Vendor)=0, model.Vendor.Name, "Not available")`.</span><span class="sxs-lookup"><span data-stu-id="a2847-546">You can also use the expression `IF(COUNT(model.Vendor)=0, model.Vendor.Name, "Not available")`.</span></span>

### <a name="additional-consideration"></a><a id="i9a"></a><span data-ttu-id="a2847-547">الاعتبار الإضافي</span><span class="sxs-lookup"><span data-stu-id="a2847-547">Additional consideration</span></span>

<span data-ttu-id="a2847-548">يحذرك الفحص أيضًا بشأن مشكلة أخرى محتملة.</span><span class="sxs-lookup"><span data-stu-id="a2847-548">The inspection also warns you about another potential issue.</span></span> <span data-ttu-id="a2847-549">بشكل افتراضي، عندما تقوم بربط عناصر تنسيق **العبارة\\الطرف\\الاسم** و **العبارة\\الطرف\\AccountNum** باللحقول المناسبة من مصدر بيانات `model.Vendor` الخاص بنوع **قائمة السجلات**، سيتم تشغيل هذه الروابط وستقوم بنقل قيم الحقول المناسبة للسجل الأول من مصدر بيانات `model.Vendor`، إذا كانت هذه القائمة غير فارغة.</span><span class="sxs-lookup"><span data-stu-id="a2847-549">By default, as you bind the **Statement\\Party\\Name** and **Statement\\Party\\AccountNum** format elements to the appropriate fields of the `model.Vendor` data source of the **Record list** type, those bindings will be run and will take the values of the appropriate fields of the first record of the `model.Vendor` data source, if that list isn't empty.</span></span>

<span data-ttu-id="a2847-550">لأنك لم تقم بربط عنصر تنسيق **العبارة\\الطرف** بمصدر بيانات `model.Vendor`، لن يتكرر عنصر **العبارة\\الطرف** لكل سجل من مصدر بيانات `model.Vendor` أثناء تنفيذ التنسيق.</span><span class="sxs-lookup"><span data-stu-id="a2847-550">Because you haven't bound the **Statement\\Party** format element with the `model.Vendor` data source, the **Statement\\Party** element won't be iterated for every record of the `model.Vendor` data source during format execution.</span></span> <span data-ttu-id="a2847-551">وبدلا من ذلك، سيتم ملء المستند الذي تم إنشاؤه بمعلومات من السجل الأول فقط في قائمه السجلات، إذا كانت هذه القائمة تحتوي علي سجلات متعددة.</span><span class="sxs-lookup"><span data-stu-id="a2847-551">Instead, a generated document will be filled with information from only the first record of the record list, if that list contains multiple records.</span></span> <span data-ttu-id="a2847-552">ولذلك، قد تكون هناك مشكله إذا كان من المقصود بالتنسيق ملء مستند تم إنشاؤه بمعلومات حول جميع الموردين من مصدر بيانات `model.Vendor`.</span><span class="sxs-lookup"><span data-stu-id="a2847-552">Therefore, there might be an issue if the format is intended to fill a generated document with information about all vendors from the `model.Vendor` data source.</span></span> <span data-ttu-id="a2847-553">لحل هذه المشكلة، قم بربط عنصر **الكشف\\الطرف** بمصدر بيانات `model.Vendor`.</span><span class="sxs-lookup"><span data-stu-id="a2847-553">To fix this issue, bind the **Statement\\Party** element with the `model.Vendor` data source.</span></span>

## <a name="executability-of-an-expression-with-filter-function-caching"></a><a id="i10"></a><span data-ttu-id="a2847-554">إمكانية تنفيذ تعبير باستخدام وظيفة التصفية (التخزين المؤقت)</span><span class="sxs-lookup"><span data-stu-id="a2847-554">Executability of an expression with FILTER function (caching)</span></span>

<span data-ttu-id="a2847-555">يتم استخدام وظائف التقارير الإلكترونية المضمنة، بما في ذلك [FILTER](er-functions-list-filter.md) و[ALLITEMSQUERY](er-functions-list-allitemsquery.md) للوصول إلى جداول التطبيق أو طرق العرض أو كيانات البيانات عن طريق وضع استدعاء SQL مفرد للحصول علي البيانات المطلوبة كقائمه سجلات.</span><span class="sxs-lookup"><span data-stu-id="a2847-555">Several built-in ER functions, including [FILTER](er-functions-list-filter.md) and [ALLITEMSQUERY](er-functions-list-allitemsquery.md), are used to access application tables, views, or data entities by placing a single SQL call to get the required data as a list of records.</span></span> <span data-ttu-id="a2847-556">يتم استخدام مصدر بيانات من نوع **قائمة السجلات** كوسيطة لكل وظيفة من هذه الوظائف ويحدد مصدر التطبيق الخاص بالاستدعاء.</span><span class="sxs-lookup"><span data-stu-id="a2847-556">A data source of the **Record list** type is used as an argument of each of these functions and specifies an application source for the call.</span></span> <span data-ttu-id="a2847-557">يقوم التقارير الإلكترونية بالتحقق مما إذا كان من الممكن إنشاء استدعاء SQL مباشر إلى مصدر بيانات يشار إليه في أحد هذه الوظائف.</span><span class="sxs-lookup"><span data-stu-id="a2847-557">ER checks whether a direct SQL call can be established to a data source that is referred to in one of these functions.</span></span> <span data-ttu-id="a2847-558">إذا تعذر إنشاء استدعاء مباشر لأن مصدر البيانات تم تمييزه بأنه [مخزن مؤقتًا](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace)، يحدث خطا في التحقق من الصحة في مصمم تعيين نماذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a2847-558">If a direct call can't be established because the data source was marked as [cached](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace), a validation error occurs in the ER model mapping designer.</span></span> <span data-ttu-id="a2847-559">تنص الرسالة التي تتلقاها على أنه لا يمكن تشغيل تعبير التقارير الإلكترونية الذي يحتوي على إحدى هذه الوظائف في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="a2847-559">The message that you receive states that the ER expression that contains one of these functions can't be run at runtime.</span></span>

<span data-ttu-id="a2847-560">توضح الخطوات التالية كيفيه حدوث هذه المشكلة.</span><span class="sxs-lookup"><span data-stu-id="a2847-560">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a2847-561">ابدأ بتكوين مكون تعيين نموذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a2847-561">Start to configure the ER model mapping component.</span></span>
2. <span data-ttu-id="a2847-562">أضف مصدر بيانات من نوع **Dynamics 365 for Operations \\ سجلات الجداول**.</span><span class="sxs-lookup"><span data-stu-id="a2847-562">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="a2847-563">قم بتسمية مصدر البيانات الجديد **المورد**.</span><span class="sxs-lookup"><span data-stu-id="a2847-563">Name the new data source **Vendor**.</span></span> <span data-ttu-id="a2847-564">في حقل **الجدول**، حدد **VendTable** لتحديد أن مصدر البيانات سيطلب الجدول VendTable.</span><span class="sxs-lookup"><span data-stu-id="a2847-564">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
4. <span data-ttu-id="a2847-565">أضف مصدر بيانات من نوع **عام \\ معلمة إدخال المستخدم** للبحث عن حساب مورد في مربع حوار وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="a2847-565">Add a data source of the **General \\ User input parameter** type to search for a vendor account in the runtime dialog box.</span></span>
5. <span data-ttu-id="a2847-566">قم بتسمية مصدر البيانات الجديد **RequestedAccountNum**.</span><span class="sxs-lookup"><span data-stu-id="a2847-566">Name the new data source **RequestedAccountNum**.</span></span> <span data-ttu-id="a2847-567">في حقل **التسمية**، أدخل **رقم حساب المورد**.</span><span class="sxs-lookup"><span data-stu-id="a2847-567">In the **Label** field, enter **Vendor account number**.</span></span> <span data-ttu-id="a2847-568">في حقل **اسم نوع بيانات Operations**، اترك القيمة الافتراضية، وهي **الوصف**.</span><span class="sxs-lookup"><span data-stu-id="a2847-568">In the **Operations data type name** field, leave the default value, **Description**.</span></span>
6. <span data-ttu-id="a2847-569">أضف مصدر بيانات من نوع **الحقل المحسوب** لتصفية مورد تم الاستعلام عنه.</span><span class="sxs-lookup"><span data-stu-id="a2847-569">Add a data source of the **Calculated field** type to filter a vendor that is inquired about.</span></span>
7. <span data-ttu-id="a2847-570">قم بتسميه مصدر البيانات الجديد **FilteredVendor**، وقم بتكوينه بحيث يحتوي علي التعبير `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.</span><span class="sxs-lookup"><span data-stu-id="a2847-570">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.</span></span>
8. <span data-ttu-id="a2847-571">ضع علامة على مصدر بيانات **المورد** المكون كمخزن مؤقتًا.</span><span class="sxs-lookup"><span data-stu-id="a2847-571">Mark the configured **Vendor** data source as cached.</span></span>

    ![تكوين مكون تعيين النموذج القابل للتحرير في صفحه مصمم تعيين النموذج](./media/er-components-inspections-10a.gif)

9. <span data-ttu-id="a2847-573">حدد **التحقق من الصحة** لفحص مكون تعيين النموذج القابل للتحرير في صفحه **مصمم تعيين النموذج**.</span><span class="sxs-lookup"><span data-stu-id="a2847-573">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page.</span></span>

    ![التحقق من صحة وظيفة FILTER المطبقة على مصدر بيانات مورد ذاكرة التخزين المؤقت في صفحة مصمم تعيين النموذج](./media/er-components-inspections-10a.png)

10. <span data-ttu-id="a2847-575">لاحظ حدوث خطا في التحقق من الصحة.</span><span class="sxs-lookup"><span data-stu-id="a2847-575">Notice that a validation error occurs.</span></span> <span data-ttu-id="a2847-576">توضح الرسالة أنه لا يمكن تطبيق وظيفة **التصفية** على مصدر بيانات **المورد** المخزن مؤقتًا.</span><span class="sxs-lookup"><span data-stu-id="a2847-576">The message states that the **FILTER** function can't be applied to the cached **Vendor** data source.</span></span>

<span data-ttu-id="a2847-577">يبين الرسم التوضيحي التالي خطا وقت التشغيل الذي يحدث إذا تجاهلت التحذير وحدد **تشغيل** لتشغيل التنسيق.</span><span class="sxs-lookup"><span data-stu-id="a2847-577">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run the format.</span></span>

![خطأ وقت التشغيل الذي يحدث أثناء تشغيل تعيين التنسيق في صفحة مصمم التنسيق](./media/er-components-inspections-10b.png)

### <a name="automatic-resolution&quot;></a><span data-ttu-id=&quot;a2847-579&quot;>الحل التلقائي</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;a2847-579&quot;>Automatic resolution</span></span>

<span data-ttu-id=&quot;a2847-580&quot;>لا يتوفر اي خيار لإصلاح هذه المشكلة تلقائيا.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;a2847-580&quot;>No option to automatically fix this issue is available.</span></span>

### <a name=&quot;manual-resolution&quot;></a><span data-ttu-id=&quot;a2847-581&quot;>الحل اليدوي</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;a2847-581&quot;>Manual resolution</span></span>

#### <a name=&quot;option-1&quot;></a><span data-ttu-id=&quot;a2847-582&quot;>خيار 1</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;a2847-582&quot;>Option 1</span></span>

<span data-ttu-id=&quot;a2847-583&quot;>قم بإزالة علامة **ذاكرة التخزين المؤقت** من مصدر بيانات **المورد**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;a2847-583&quot;>Remove the **Cache** flag from the **Vendor** data source.</span></span> <span data-ttu-id=&quot;a2847-584&quot;>سيصبح مصدر بيانات **FilteredVendor** قابلاً للتنفيذ حينئذٍ، ولكن سيتم الوصول إلى مصدر بيانات **المورد** الذي تمت الإشارة إليه في جدول VendTable في كل مرة يتم فيها استدعاء مصدر بيانات **FilteredVendor**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;a2847-584&quot;>The **FilteredVendor** data source will then become executable, but the **Vendor** data source that is referred to in the VendTable table will be accessed every time that the **FilteredVendor** data source is called.</span></span>

#### <a name=&quot;option-2&quot;></a><span data-ttu-id=&quot;a2847-585&quot;>خيار 2</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;a2847-585&quot;>Option 2</span></span>

<span data-ttu-id=&quot;a2847-586&quot;>قم بتغيير التعبير الخاص بمصدر بيانات **FilteredVendor** من `FILTER(Vendor, Vendor.AccountNum=&quot;US-101")`إلى `WHERE(Vendor, Vendor.AccountNum="US-101")`.</span><span class="sxs-lookup"><span data-stu-id="a2847-586">Change the expression of the **FilteredVendor** data source from `FILTER(Vendor, Vendor.AccountNum="US-101")` to `WHERE(Vendor, Vendor.AccountNum="US-101")`.</span></span> <span data-ttu-id="a2847-587">في هذه الحالة، سيتم الوصول إلى مصدر بيانات **المورد** المشار إليه في جدول VendTable فقط أثناء الاستدعاء الأول لمصدر بيانات **المورد**.</span><span class="sxs-lookup"><span data-stu-id="a2847-587">In this case, the **Vendor** data source that is referred to in the VendTable table will be accessed only during the first call of the **Vendor** data source.</span></span> <span data-ttu-id="a2847-588">ومع ذلك، سيتم إجراء تحديد السجلات في الذاكرة.</span><span class="sxs-lookup"><span data-stu-id="a2847-588">However, the selection of records will be done in memory.</span></span> <span data-ttu-id="a2847-589">لذلك، يمكن ان يتسبب هذا الأسلوب في ضعف الأداء.</span><span class="sxs-lookup"><span data-stu-id="a2847-589">Therefore, this approach can cause poor performance.</span></span>

## <a name="missing-binding"></a><a id="i11"></a><span data-ttu-id="a2847-590">الربط مفقود</span><span class="sxs-lookup"><span data-stu-id="a2847-590">Missing binding</span></span>

<span data-ttu-id="a2847-591">عند تكوين مكون التنسيق الخاص بالتقارير الإلكترونية، يتم عرض نموذج البيانات الأساسي الخاص بالتقارير الإلكترونية كمصدر بيانات افتراضي لتنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a2847-591">When you configure an ER format component, the base ER data model is offered as a default data source for the ER format.</span></span> <span data-ttu-id="a2847-592">عند تشغيل التنسيق المكون لالتقارير الإلكترونية، يتم استخدام [تعيين النموذج الافتراضي](er-country-dependent-model-mapping.md) للنموذج الأساسي لتعبئة نموذج البيانات ببيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="a2847-592">When the configured ER format is run, the [default model mapping](er-country-dependent-model-mapping.md) for the base model is used to fill the data model with application data.</span></span> <span data-ttu-id="a2847-593">يعرض مصمم التنسيق الخاص بالتقارير الإلكترونية تحذيرا إذا قمت بربط عنصر تنسيق بعنصر نموذج بيانات غير مرتبط بأي مصدر بيانات في تعيين النموذج المحدد حاليا كتعيين نموذج افتراضي للتنسيق القابل للتحرير.</span><span class="sxs-lookup"><span data-stu-id="a2847-593">The ER format designer shows a warning if you bind a format element to a data model item that isn't bound to any data source in the model mapping that is currently selected as the default model mapping for the editable format.</span></span> <span data-ttu-id="a2847-594">لا يمكن تشغيل هذا النوع من الربط في وقت التشغيل، لان التنسيق الذي يتم تشغيله لا يمكنه تعبئة عنصر مرتبط ببيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="a2847-594">This type of binding can't be run at runtime, because the format that runs can't fill a bound element with application data.</span></span> <span data-ttu-id="a2847-595">ولذلك، يحدث خطأ في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="a2847-595">Therefore, an error occurs at runtime.</span></span>

<span data-ttu-id="a2847-596">توضح الخطوات التالية كيفيه حدوث هذه المشكلة.</span><span class="sxs-lookup"><span data-stu-id="a2847-596">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a2847-597">ابدأ في تكوين نموذج بيانات التقارير الإلكترونية وتعيين نموذج التقارير الإلكترونية ومكونات تنسيق التقارير الإلكترونية في وقت واحد.</span><span class="sxs-lookup"><span data-stu-id="a2847-597">Start to configure the ER data model, the ER model mapping, and the ER format components simultaneously.</span></span>
2. <span data-ttu-id="a2847-598">في شجرة نموذج البيانات، قم باضافه العنصر الجذر المسمى **الجذر 3**.</span><span class="sxs-lookup"><span data-stu-id="a2847-598">In the data model tree, add a root item that is named **Root3**.</span></span>
3. <span data-ttu-id="a2847-599">قم بتعديل عنصر **الجذر 3** عن طريق إضافة عنصر متداخل جديد من نوع **قائمة السجلات**.</span><span class="sxs-lookup"><span data-stu-id="a2847-599">Modify the **Root3** item by adding a new nested item of the **Record list** type.</span></span>
4. <span data-ttu-id="a2847-600">قم بتسمية العنصر المتداخل الجديد **المورد**.</span><span class="sxs-lookup"><span data-stu-id="a2847-600">Name the new nested item **Vendor**.</span></span>
5. <span data-ttu-id="a2847-601">قم بتعديل عنصر **المورد** بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="a2847-601">Modify the **Vendor** item in the following way:</span></span>

    - <span data-ttu-id="a2847-602">أضف حقلاً متداخلاً من نوع **السلسلة**، وقم بتسميته بـ **اسم**.</span><span class="sxs-lookup"><span data-stu-id="a2847-602">Add a nested field of the **String** type, and name it **Name**.</span></span>
    - <span data-ttu-id="a2847-603">أضف حقلاً متداخلاً من نوع **السلسلة**، وقم بتسميته بـ **AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="a2847-603">Add a nested field of the **String** type, and name it **AccountNumber**.</span></span>

    ![إضافة حقول متداخلة إلى عنصر المورد في صفحة نموذج البيانات](./media/er-components-inspections-11a.png)

6. <span data-ttu-id="a2847-605">في مصمم تعيين النموذج، في جزء **مصادر البيانات**، أضف مصدر بيانات من نوع **Dynamics 365 for Operations \\سجلات الجدول**.</span><span class="sxs-lookup"><span data-stu-id="a2847-605">In the model mapping designer, in the **Data sources** pane, add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
7. <span data-ttu-id="a2847-606">قم بتسمية مصدر البيانات الجديد **المورد**.</span><span class="sxs-lookup"><span data-stu-id="a2847-606">Name the new data source **Vendor**.</span></span> <span data-ttu-id="a2847-607">في حقل **الجدول**، حدد **VendTable** لتحديد أن مصدر البيانات سيطلب الجدول VendTable.</span><span class="sxs-lookup"><span data-stu-id="a2847-607">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
8. <span data-ttu-id="a2847-608">أضف مصدر بيانات من نوع **عام \\ معلمة إدخال المستخدم** للاستعلام عن حساب مورد في مربع حوار وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="a2847-608">Add a data source of the **General \\ User input parameter** type to inquire about a vendor account in the runtime dialog box.</span></span>
9. <span data-ttu-id="a2847-609">قم بتسمية مصدر البيانات الجديد **RequestedAccountNum**.</span><span class="sxs-lookup"><span data-stu-id="a2847-609">Name the new data source **RequestedAccountNum**.</span></span> <span data-ttu-id="a2847-610">في حقل **التسمية**، أدخل **رقم حساب المورد**.</span><span class="sxs-lookup"><span data-stu-id="a2847-610">In the **Label** field, enter **Vendor account number**.</span></span> <span data-ttu-id="a2847-611">في حقل **اسم نوع بيانات Operations**، اترك القيمة الافتراضية، وهي **الوصف**.</span><span class="sxs-lookup"><span data-stu-id="a2847-611">In the **Operations data type name** field, leave the default value, **Description**.</span></span>
10. <span data-ttu-id="a2847-612">أضف مصدر بيانات من نوع **الحقل المحسوب** لتصفية مورد تم الاستعلام عنه.</span><span class="sxs-lookup"><span data-stu-id="a2847-612">Add a data source of the **Calculated field** type to filter a vendor that is inquired about.</span></span>
11. <span data-ttu-id="a2847-613">قم بتسميه مصدر البيانات الجديد **FilteredVendor**، وقم بتكوينه بحيث يحتوي علي التعبير `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.</span><span class="sxs-lookup"><span data-stu-id="a2847-613">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.</span></span>
12. <span data-ttu-id="a2847-614">اربط عناصر نموذج البيانات بمصادر البيانات التي تم تكوينها بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="a2847-614">Bind the data model items to configured data sources in the following way:</span></span>

    - <span data-ttu-id="a2847-615">اربط **FilteredVendor** بـ **المورد**.</span><span class="sxs-lookup"><span data-stu-id="a2847-615">Bind **FilteredVendor** to **Vendor**.</span></span>
    - <span data-ttu-id="a2847-616">اربط **FilteredVendor.AccountNum** بـ **Vendor.AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="a2847-616">Bind **FilteredVendor.AccountNum** to **Vendor.AccountNumber**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a2847-617">يبقى حقل نموذج بيانات **Vendor.Name** غير مرتبط.</span><span class="sxs-lookup"><span data-stu-id="a2847-617">The **Vendor.Name** data model field remains unbound.</span></span>

    ![عناصر نموذج البيانات المرتبطة بمصادر البيانات المكونة وعنصر وضع البيانات الذي يبقى غير مرتبط في صفحة مصمم تعيين النموذج](./media/er-components-inspections-11b.png)

13. <span data-ttu-id="a2847-619">في شجرة هيكل التنسيق، أضف العناصر التالية لإنشاء مستند صادر بتنسيق XML يحتوي على تفاصيل البائعين الذين يتم الاستفسار عنهم:</span><span class="sxs-lookup"><span data-stu-id="a2847-619">In the format structure tree, add the following items to generate an outbound document in XML format that contains the details of the vendors that are inquired about:</span></span>

    1. <span data-ttu-id="a2847-620">أضف عنصر XML الخاص بجذر **العبارة**.</span><span class="sxs-lookup"><span data-stu-id="a2847-620">Add the **Statement** root XML element.</span></span>
    2. <span data-ttu-id="a2847-621">بالنسبة إلى عنصر XML لـ **العبارة**، أضف عنصر XML لـ **الطرف** المتداخل.</span><span class="sxs-lookup"><span data-stu-id="a2847-621">For the **Statement** XML element, add the nested **Party** XML element.</span></span>
    3. <span data-ttu-id="a2847-622">بالنسبة لعناصر XML **للطرف**، أضف سمات XML المتداخلة التالية:</span><span class="sxs-lookup"><span data-stu-id="a2847-622">For the **Party** XML element, add the following nested XML attributes:</span></span>

        - <span data-ttu-id="a2847-623">الاسم</span><span class="sxs-lookup"><span data-stu-id="a2847-623">Name</span></span>
        - <span data-ttu-id="a2847-624">AccountNum</span><span class="sxs-lookup"><span data-stu-id="a2847-624">AccountNum</span></span>

14. <span data-ttu-id="a2847-625">ربط عناصر التنسيق بمصادر البيانات المتوفرة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="a2847-625">Bind the format elements to provided data sources in the following way:</span></span>

    - <span data-ttu-id="a2847-626">اربط عنصر تنسيق **الكشف\\الطرف** بعنصر مصدر بيانات `model.Vendor`.</span><span class="sxs-lookup"><span data-stu-id="a2847-626">Bind the **Statement\\Party** format element to the `model.Vendor` data source item.</span></span>
    - <span data-ttu-id="a2847-627">اربط عنصر تنسيق **العبارة\\الطرف\\الاسم** بحقل مصدر البيانات **model.Vendor.Name**.</span><span class="sxs-lookup"><span data-stu-id="a2847-627">Bind the **Statement\\Party\\Name** format element to the **model.Vendor.Name** data source field.</span></span>
    - <span data-ttu-id="a2847-628">اربط عنصر تنسيق **العبارة\\الطرف\\AccountNum** بحقل مصدر البيانات **model.Vendor.AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="a2847-628">Bind the **Statement\\Party\\AccountNum** format element to the **model.Vendor.AccountNumber** data source field.</span></span>

15. <span data-ttu-id="a2847-629">حدد **التحقق من الصحة** لفحص مكون التنسيق القابل للتحرير في صفحة **مصمم التنسيق**.</span><span class="sxs-lookup"><span data-stu-id="a2847-629">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![التحقق من صحة مكون تنسيق التقارير الإلكترونية (ER) في صفحة مصمم التنسيق](./media/er-components-inspections-11c.png)

16. <span data-ttu-id="a2847-631">لاحظ حدوث تحذير في التحقق من الصحة.</span><span class="sxs-lookup"><span data-stu-id="a2847-631">Notice that a validation warning occurs.</span></span> <span data-ttu-id="a2847-632">وتنص الرسالة على أن حقل **model.Vendor.Name** غير مرتبط بأي مصدر بيانات في تعيين النموذج الذي تم تكوينه ليتم استخدامه بواسطة التنسيق.</span><span class="sxs-lookup"><span data-stu-id="a2847-632">The message states that the **model.Vendor.Name** data source field isn't bound to any data source in the model mapping that is configured to be used by the format.</span></span> <span data-ttu-id="a2847-633">ولذلك، قد لا يتم ملء عنصر تنسيق **الكشف\\الطرف\\الاسم** في وقت التشغيل، وقد يحدث استثناء في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="a2847-633">Therefore, the **Statement\\Party\\Name** format element might not be filled at runtime, and a runtime exception might occur.</span></span>

    ![التحقق من صحة مكون تنسيق التقارير الإلكترونية في صفحة "مصمم التنسيق"](./media/er-components-inspections-11d.png)

<span data-ttu-id="a2847-635">يبين الرسم التوضيحي التالي خطا وقت التشغيل الذي يحدث إذا تجاهلت التحذير وحدد **تشغيل** لتشغيل التنسيق.</span><span class="sxs-lookup"><span data-stu-id="a2847-635">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run the format.</span></span>

![تشغيل التنسيق القابل للتحرير علي صفحه مصمم التنسيق](./media/er-components-inspections-11e.png)

### <a name="automatic-resolution"></a><span data-ttu-id="a2847-637">الحل التلقائي</span><span class="sxs-lookup"><span data-stu-id="a2847-637">Automatic resolution</span></span>

<span data-ttu-id="a2847-638">لا يتوفر اي خيار لإصلاح هذه المشكلة تلقائيا.</span><span class="sxs-lookup"><span data-stu-id="a2847-638">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="a2847-639">الحل اليدوي</span><span class="sxs-lookup"><span data-stu-id="a2847-639">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="a2847-640">خيار 1</span><span class="sxs-lookup"><span data-stu-id="a2847-640">Option 1</span></span>

<span data-ttu-id="a2847-641">قم بتعديل تعيين النموذج الذي تم تكوينه عن طريق إضافة ربط لحقل مصدر بيانات **model.Vendor.Name**.</span><span class="sxs-lookup"><span data-stu-id="a2847-641">Modify the configured model mapping by adding a binding for the **model.Vendor.Name** data source field.</span></span>

#### <a name="option-2"></a><span data-ttu-id="a2847-642">خيار 2</span><span class="sxs-lookup"><span data-stu-id="a2847-642">Option 2</span></span>

<span data-ttu-id="a2847-643">قم بتعديل التنسيق الذي تم تكوينه عن طريق إزالة الربط لعنصر تنسيق **الكشف\\الطرف\\الاسم**.</span><span class="sxs-lookup"><span data-stu-id="a2847-643">Modify the configured format by removing the binding for the **Statement\\Party\\Name** format element.</span></span>

## <a name="not-linked-template"></a><a id="i12"></a><span data-ttu-id="a2847-644">قالب غير مرتبط</span><span class="sxs-lookup"><span data-stu-id="a2847-644">Not linked template</span></span>

<span data-ttu-id="a2847-645">عند قيامك [يدويًا](er-fillable-excel.md#manual-entry) بتكوين مكون التنسيق الخاص بالتقارير الإلكترونية لاستخدام قالب لإنشاء مستند صادر، يجب عليك إضافة عنصر **ملف\\Excel**، وأضف القالب المطلوب كمرفق للمكون القابل للتحرير، وحدد ذلك المرفق في عنصر **ملف\\Excel**.</span><span class="sxs-lookup"><span data-stu-id="a2847-645">When you [manually](er-fillable-excel.md#manual-entry) configure an ER format component to use a template to generate an outbound document, you must manually add the **Excel\\File** element, add the required template as an attachment of the editable component, and select that attachment in the added **Excel\\File** element.</span></span> <span data-ttu-id="a2847-646">بهذه الطريقة، تشير إلى أن العنصر المضاف سوف يملأ القالب المحدد في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="a2847-646">In this way, you indicate that the added element will fill the selected template at runtime.</span></span> <span data-ttu-id="a2847-647">عند تكوين إصدار مكون تنسيق **بالحالة** [مسودة](general-electronic-reporting.md#component-versioning)، يمكنك إضافة عدة قوالب إلى المكون القابل للتحرير ثم تحديد كل قالب في عنصر **ملف\\Excel** لتشغيل تنسيق التقارير الإلكترونية (ER).</span><span class="sxs-lookup"><span data-stu-id="a2847-647">When you configure a format component version in **Draft** [status](general-electronic-reporting.md#component-versioning), you might add several templates to the editable component and then select each template in the **Excel\\File** element to run the ER format.</span></span> <span data-ttu-id="a2847-648">وبهذه الطريقة، يمكنك مشاهده كيفيه تعبئة القوالب المختلفة في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="a2847-648">In this way, you can see how different templates are filled at runtime.</span></span> <span data-ttu-id="a2847-649">إذا كان لديك قوالب غير محددة في أي عنصر من عناصر **ملف\\Excel**، يقوم مصمم تنسيق التقارير الإلكترونية بتحذيرك بأن هذه القوالب سيتم حذفها من إصدار مكون التنسيق القابل للتحرير للتقارير الإلكترونية عند تغيير حالتها من **مسودة** إلى **مكتملة**.</span><span class="sxs-lookup"><span data-stu-id="a2847-649">If you have templates that aren't selected in any **Excel\\File** elements, the ER format designer warns you that those templates will be deleted from the editable ER format component version when its status is changed from **Draft** to **Completed**.</span></span>

<span data-ttu-id="a2847-650">توضح الخطوات التالية كيفيه حدوث هذه المشكلة.</span><span class="sxs-lookup"><span data-stu-id="a2847-650">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a2847-651">ابدأ بتكوين مكون تعيين تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a2847-651">Start to configure the ER format component.</span></span>
2. <span data-ttu-id="a2847-652">في شجرة بنية التنسيق، أضف عنصر **ملف\\Excel**.</span><span class="sxs-lookup"><span data-stu-id="a2847-652">In the format structure tree, add the **Excel\\File** element.</span></span>
3. <span data-ttu-id="a2847-653">بالنسبة لعنصر **ملف\\Excel** الذي أضفته للتو، أضف ملف مصنف Excel، **A.xlsx**، كمرفق.</span><span class="sxs-lookup"><span data-stu-id="a2847-653">For the **Excel\\File** element that you just added, add an Excel workbook file, **A.xlsx**, as an attachment.</span></span> <span data-ttu-id="a2847-654">استخدم نوع المستند الذي تم تكوينه في [معلمات التقارير الإلكترونية](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) لتحديد تخزين قوالب تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a2847-654">Use the document type that is configured in the [ER parameters](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) to specify the storage of ER format templates.</span></span>
4. <span data-ttu-id="a2847-655">بالنسبة لعنصر **ملف\\Excel**، أضف ملف مصنف Excel آخر، **B.xlsx**، كمرفق.</span><span class="sxs-lookup"><span data-stu-id="a2847-655">For the **Excel\\File** element, add another Excel workbook file, **B.xlsx**, as an attachment.</span></span> <span data-ttu-id="a2847-656">استخدم نفس نوع المستند المستخدم لملف المصنف A.</span><span class="sxs-lookup"><span data-stu-id="a2847-656">Use the same document type that is used for workbook file A.</span></span>
5. <span data-ttu-id="a2847-657">في عنصر **ملف\\Excel**، حدد ملف المصنف A.</span><span class="sxs-lookup"><span data-stu-id="a2847-657">In the **Excel\\File** element, select workbook file A.</span></span>
6. <span data-ttu-id="a2847-658">حدد **التحقق من الصحة** لفحص مكون التنسيق القابل للتحرير في صفحة **مصمم التنسيق**.</span><span class="sxs-lookup"><span data-stu-id="a2847-658">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![التحقق من صحة مكون التنسيق القابل للتحرير لملف المصنف في صفحة "مصمم التنسيق"](./media/er-components-inspections-12a.gif)

7. <span data-ttu-id="a2847-660">لاحظ حدوث تحذير في التحقق من الصحة.</span><span class="sxs-lookup"><span data-stu-id="a2847-660">Notice that a validation warning occurs.</span></span> <span data-ttu-id="a2847-661">توضح الرسالة أن ملف المصنف B.xlsx غير مرتبط بأي مكونات، وأنه ستتم إزالته بعد تغيير حالة إصدار التكوين.</span><span class="sxs-lookup"><span data-stu-id="a2847-661">The message states that workbook file B.xlsx isn't linked to any components, and that it will be removed after the status of the configuration version is changed.</span></span>

### <a name="automatic-resolution"></a><span data-ttu-id="a2847-662">الحل التلقائي</span><span class="sxs-lookup"><span data-stu-id="a2847-662">Automatic resolution</span></span>

<span data-ttu-id="a2847-663">لا يتوفر اي خيار لإصلاح هذه المشكلة تلقائيا.</span><span class="sxs-lookup"><span data-stu-id="a2847-663">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="a2847-664">الحل اليدوي</span><span class="sxs-lookup"><span data-stu-id="a2847-664">Manual resolution</span></span>

<span data-ttu-id="a2847-665">قم بتعديل التنسيق الذي تم تكوينه عن طريق إزالة جميع القوالب غير المرتبطة بأي عنصر **ملف\\Excel**.</span><span class="sxs-lookup"><span data-stu-id="a2847-665">Modify the configured format by removing all templates that aren't linked to any **Excel\\File** element.</span></span>

## <a name="not-synced-format"></a><a id="i13"></a><span data-ttu-id="a2847-666">تنسيق غير متزامن</span><span class="sxs-lookup"><span data-stu-id="a2847-666">Not synced format</span></span>

<span data-ttu-id="a2847-667">عند قيامك [بتكوين](er-fillable-excel.md) مكون تنسيق التقارير الإلكترونية لاستخدام قالب Excel لإنشاء مستند صادر، يمكنك إضافة عنصر **ملف\\Excel** يدويًا، وأضف القالب المطلوب كمرفق للمكون القابل للتحرير، وحدد ذلك المرفق في عنصر **ملف\\Excel**.</span><span class="sxs-lookup"><span data-stu-id="a2847-667">When you [configure](er-fillable-excel.md) an ER format component to use an Excel template to generate an outbound document, you can manually add the **Excel\\File** element, add the required template as an attachment of the editable component, and select that attachment in the added **Excel\\File** element.</span></span> <span data-ttu-id="a2847-668">بهذه الطريقة، تشير إلى أن العنصر المضاف سوف يملأ القالب المحدد في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="a2847-668">In this way, you indicate that the added element will fill the selected template at runtime.</span></span> <span data-ttu-id="a2847-669">نظرًا لأنه تم تصميم قالب Excel المضاف خارجيًا، فقد يحتوي تنسيق التقارير الإلكترونية القابل للتحرير على أسماء Excel مفقودة من القالب المضاف.</span><span class="sxs-lookup"><span data-stu-id="a2847-669">Because the added Excel template has been externally designed, the editable ER format might contain Excel names that are missing from the added template.</span></span> <span data-ttu-id="a2847-670">يحذرك مصمم تنسيق التقارير الإلكترونية من أي تناقضات بين خصائص عناصر تنسيق التقارير الإلكترونية التي تشير إلى الأسماء غير المضمنة في قالب Excel المضاف.</span><span class="sxs-lookup"><span data-stu-id="a2847-670">The ER format designer warns you about any inconsistencies between the properties of the ER format elements that refer to names that aren't included in the added Excel template.</span></span>

<span data-ttu-id="a2847-671">توضح الخطوات التالية كيفيه حدوث هذه المشكلة.</span><span class="sxs-lookup"><span data-stu-id="a2847-671">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="a2847-672">ابدأ بتكوين مكون تعيين تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a2847-672">Start to configure the ER format component.</span></span>
2. <span data-ttu-id="a2847-673">في شجرة بنية التنسيق، أضف عنصر **ملف\\Excel** **التقرير**.</span><span class="sxs-lookup"><span data-stu-id="a2847-673">In the format structure tree, add the **Excel\\File** element **Report**.</span></span>
3. <span data-ttu-id="a2847-674">بالنسبة لعنصر **ملف\\Excel** الذي أضفته للتو، أضف ملف مصنف Excel، **A.xlsx**، كمرفق.</span><span class="sxs-lookup"><span data-stu-id="a2847-674">For the **Excel\\File** element that you just added, add an Excel workbook file, **A.xlsx**, as an attachment.</span></span> <span data-ttu-id="a2847-675">استخدم نوع المستند الذي تم تكوينه في [معلمات التقارير الإلكترونية](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) لتحديد تخزين قوالب تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a2847-675">Use the document type that is configured in the [ER parameters](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) to specify the storage of ER format templates.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="a2847-676">تأكد من أن مصنف Excel المضاف لا يحتوي على الاسم **ReportTitle**.</span><span class="sxs-lookup"><span data-stu-id="a2847-676">Make sure that the added Excel workbook doesn't contain the name **ReportTitle**.</span></span>

4. <span data-ttu-id="a2847-677">أضف عنصر **خلية\\Excel** **العنوان** باعتباره العنصر المتداخل لعنصر **التقرير**.</span><span class="sxs-lookup"><span data-stu-id="a2847-677">Add the **Excel\\Cell** element **Title** as a nested element of the **Report** element.</span></span> <span data-ttu-id="a2847-678">في حقل **نطاق Excel**، أدخل **ReportTitle**.</span><span class="sxs-lookup"><span data-stu-id="a2847-678">In the **Excel range** field, enter **ReportTitle**.</span></span>
5. <span data-ttu-id="a2847-679">حدد **التحقق من الصحة** لفحص مكون التنسيق القابل للتحرير في صفحة **مصمم التنسيق**.</span><span class="sxs-lookup"><span data-stu-id="a2847-679">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![التحقق من صحة الحقول والعناصر المتداخلة في صفحة مصمم التنسيق](./media/er-components-inspections-13a.png)

6. <span data-ttu-id="a2847-681">لاحظ حدوث تحذير في التحقق من الصحة.</span><span class="sxs-lookup"><span data-stu-id="a2847-681">Notice that a validation warning occurs.</span></span> <span data-ttu-id="a2847-682">تشير الرسالة إلى أن الاسم **ReportTitle** غير موجود في الورقة **Sheet1** الخاصة بقالب Excel الذي تستخدمه.</span><span class="sxs-lookup"><span data-stu-id="a2847-682">The message states that the name **ReportTitle** doesn't exist on sheet **Sheet1** of the Excel template that you're using.</span></span>

    ![تحذير التحقق من الصحة بأن الاسم ReportTitle غير موجود في Sheet1 الخاصة بقالب Excel](./media/er-components-inspections-13b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="a2847-684">الحل التلقائي</span><span class="sxs-lookup"><span data-stu-id="a2847-684">Automatic resolution</span></span>

<span data-ttu-id="a2847-685">لا يتوفر اي خيار لإصلاح هذه المشكلة تلقائيا.</span><span class="sxs-lookup"><span data-stu-id="a2847-685">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="a2847-686">الحل اليدوي</span><span class="sxs-lookup"><span data-stu-id="a2847-686">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="a2847-687">خيار 1</span><span class="sxs-lookup"><span data-stu-id="a2847-687">Option 1</span></span>

<span data-ttu-id="a2847-688">قم بتعديل التنسيق الذي تم تكوينه عن طريق إزالة جميع العناصر التي تشير إلى أسماء Excel المفقودة من القالب.</span><span class="sxs-lookup"><span data-stu-id="a2847-688">Modify the configured format by removing all elements that refer to Excel names that are missing from the template.</span></span>

#### <a name="option-2"></a><span data-ttu-id="a2847-689">خيار 2</span><span class="sxs-lookup"><span data-stu-id="a2847-689">Option 2</span></span>

<span data-ttu-id="a2847-690">[قم بتحديث](er-fillable-excel.md#template-import) تنسيق التقارير الإلكترونية القابلة للتحرير عن طريق استيراد قالب Excel.</span><span class="sxs-lookup"><span data-stu-id="a2847-690">[Update](er-fillable-excel.md#template-import) the editable ER format by importing an Excel template.</span></span> <span data-ttu-id="a2847-691">بنية تنسيق التقارير الإلكترونية القابلة للتحرير ستتم [مزامنتها](modify-electronic-reporting-format-reapply-excel-template.md) ببنية قالب Excel المستورد.</span><span class="sxs-lookup"><span data-stu-id="a2847-691">The structure of the editable ER format will be [synced](modify-electronic-reporting-format-reapply-excel-template.md) with the structure of the imported Excel template.</span></span>

### <a name="additional-consideration"></a><span data-ttu-id="a2847-692">الاعتبار الإضافي</span><span class="sxs-lookup"><span data-stu-id="a2847-692">Additional consideration</span></span>

<span data-ttu-id="a2847-693">لمعرفة كيف يمكن مزامنة بنية التنسيق مع قالب تقارير إلكترونية في محرر القالب الخاص بـ [إدارة مستندات الأعمال](er-business-document-management.md)، راجع [تحديث بنية قالب مستند الأعمال](er-bdm-update-structure.md).</span><span class="sxs-lookup"><span data-stu-id="a2847-693">To learn how the format structure can be synced with an ER template in the template editor of [Business document management](er-business-document-management.md), see [Update the structure of a business document template](er-bdm-update-structure.md).</span></span>

## <a name="not-synced-with-a-word-template-format"></a><a id="i14"></a><span data-ttu-id="a2847-694">لم تتم المزامنة مع تنسيق قالب Word</span><span class="sxs-lookup"><span data-stu-id="a2847-694">Not synced with a Word template format</span></span>

<span data-ttu-id="a2847-695">عند قيامك [بتكوين](er-fillable-excel.md) مكون تنسيق التقارير الإلكترونية (ER) لاستخدام قالب Word لإنشاء مستند صادر، يمكنك إضافة عنصر **ملف\\Excel** يدويًا، وأضف قالب Word المطلوب كمرفق للمكون القابل للتحرير، وحدد ذلك المرفق في عنصر **ملف\\Excel**.</span><span class="sxs-lookup"><span data-stu-id="a2847-695">When you [configure](er-fillable-excel.md) an ER format component to use a Word template to generate an outbound document, you can manually add the **Excel\\File** element, add the required Word template as an attachment of the editable component, and select that attachment in the added **Excel\\File** element.</span></span>

> [!NOTE]
> <span data-ttu-id="a2847-696">عندما يتم إرفاق مستند Word ، يقدم مصمم التنسيق الخاص بالتقارير الإلكترونية (ER) العنصر القابل للتحرير :ت **ملف\\Word**.</span><span class="sxs-lookup"><span data-stu-id="a2847-696">When the Word document is attached, the ER format designer presents the editable element as **Word\\File**.</span></span>

<span data-ttu-id="a2847-697">بهذه الطريقة، تشير إلى أن العنصر المضاف سوف يملأ القالب المحدد في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="a2847-697">In this way, you indicate that the added element will fill the selected template at runtime.</span></span> <span data-ttu-id="a2847-698">نظرًا لأنه تم تصميم قالب Word المضاف خارجيًا، فقد يحتوي تنسيق التقارير الإلكترونية (ER) القابل للتحرير على مراجع إلى عناصر تحكم محتوى Word مفقودة من القالب المضاف.</span><span class="sxs-lookup"><span data-stu-id="a2847-698">Because the added Word template has been externally designed, the editable ER format might contain references to Word content controls that are missing from the added template.</span></span> <span data-ttu-id="a2847-699">يحذرك مصمم تنسيق التقارير الإلكترونية (ER) من أي تناقضات بين خصائص عناصر تنسيق التقارير الإلكترونية (ER) التي تشير إلى عناصر تحكم المحتوى غير المضمنة في قالب Word المضاف.</span><span class="sxs-lookup"><span data-stu-id="a2847-699">The ER format designer warns you about any inconsistencies between the properties of the ER format elements that refer to content controls that aren't included in the added Word template.</span></span>

<span data-ttu-id="a2847-700">للحصول على مثال يوضح كيفية حدوث هذه المشكلة، راجع [تكوين التنسيق القابل للتحرير لمنع قسم الملخص](er-design-configuration-word-suppress-controls.md#configure-to-suppress-control).</span><span class="sxs-lookup"><span data-stu-id="a2847-700">For an example that shows how this issue might occur, see [Configure the editable format to suppress the summary section](er-design-configuration-word-suppress-controls.md#configure-to-suppress-control).</span></span>

### <a name="automatic-resolution"></a><span data-ttu-id="a2847-701">الحل التلقائي</span><span class="sxs-lookup"><span data-stu-id="a2847-701">Automatic resolution</span></span>

<span data-ttu-id="a2847-702">لا يتوفر اي خيار لإصلاح هذه المشكلة تلقائيا.</span><span class="sxs-lookup"><span data-stu-id="a2847-702">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="a2847-703">الحل اليدوي</span><span class="sxs-lookup"><span data-stu-id="a2847-703">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="a2847-704">خيار 1</span><span class="sxs-lookup"><span data-stu-id="a2847-704">Option 1</span></span>

<span data-ttu-id="a2847-705">قم بتعديل التنسيق الذي تم تكوينه عن طريق حذف المعادلة **تمت الإزالة** من عنصر التنسيق المذكور في تحذير التحقق من الصحة.</span><span class="sxs-lookup"><span data-stu-id="a2847-705">Modify the configured format by deleting the **Removed** formula from the format element that is mentioned in the validation warning.</span></span>

#### <a name="option-2"></a><span data-ttu-id="a2847-706">خيار 2</span><span class="sxs-lookup"><span data-stu-id="a2847-706">Option 2</span></span>

<span data-ttu-id="a2847-707">قم بالتعديل باستخدام قالب Word عن طريق [إضافة](er-design-configuration-word-suppress-controls.md#tag-control)العلامة المطلوبة إلى عنصر تحكم محتوى Word ذي الصلة.</span><span class="sxs-lookup"><span data-stu-id="a2847-707">Modify the using Word template by [adding](er-design-configuration-word-suppress-controls.md#tag-control) the required tag to the relevant Word content control.</span></span>

## <a name="no-default-mapping"></a><a id="i15"></a><span data-ttu-id="a2847-708">لا يوجد تعيين افتراضي</span><span class="sxs-lookup"><span data-stu-id="a2847-708">No default mapping</span></span>

<span data-ttu-id="a2847-709">عند اجراء فحص [الربط المفقود](#i11)، يتم تقييم روابط التنسيق التي تم فحصها مقابل روابط مكون تعيين النموذج المناسب.</span><span class="sxs-lookup"><span data-stu-id="a2847-709">When the [Missing binding](#i11) inspection is done, the inspected format bindings are evaluated against the bindings of the relevant model mapping component.</span></span> <span data-ttu-id="a2847-710">ونظرا لأنه يمكنك استيراد [عدة](./tasks/er-manage-model-mapping-configurations-july-2017.md) تكوينات لتعيين نموذج التقارير الإلكترونية (ER) إلى مثيل Finance، وقد يحتوي كل تكوين على مكون تعيين النموذج القابل للتطبيق، فيجب تحديد تكوين واحد كتكوين افتراضي.</span><span class="sxs-lookup"><span data-stu-id="a2847-710">Because you can import [several](./tasks/er-manage-model-mapping-configurations-july-2017.md) ER model mapping configurations to your Finance instance, and each configuration might contain the applicable model mapping component, one configuration must be selected as the default configuration.</span></span> <span data-ttu-id="a2847-711">خلاف ذلك، عند محاولة تشغيل تنسيق التقارير الإلكترونية (ER) الذي تم فحصه أو تحريره أو التحقق من صحته، سيحدث استثناء، وستتلقى الرسالة التالية: "يوجد أكثر من تعيين واحد للنموذج لنموذج البيانات \<model name (root descriptor)\> في التكوينات \<configuration names separated by comma\>.</span><span class="sxs-lookup"><span data-stu-id="a2847-711">Otherwise, when you try to run, edit, or validate the inspected ER format, an exception will occur, and you will receive the following message: "More than one model mapping exists for the \<model name (root descriptor)\> data model in the configurations \<configuration names separated by comma\>.</span></span> <span data-ttu-id="a2847-712">تعيين أحد التكوينات كإعداد افتراضي."</span><span class="sxs-lookup"><span data-stu-id="a2847-712">Set one of the configurations as default."</span></span>

<span data-ttu-id="a2847-713">للحصول على مثال يوضح كيفية حدوث هذه المشكلة وكيف يمكن إصلاحها، راجع [إدارة تعيينات مشتقة متعددة لجذر نموذج واحد](er-multiple-model-mappings.md).</span><span class="sxs-lookup"><span data-stu-id="a2847-713">For an example that shows how this issue might occur and how it can be fixed, see [Manage several derived mappings for a single model root](er-multiple-model-mappings.md).</span></span>

## <a name="inconsistent-setting-of-header-or-footer-components"></a><a id="i16"></a><span data-ttu-id="a2847-714">إعداد غير متناسق لمكونات الرأس أو التذييل</span><span class="sxs-lookup"><span data-stu-id="a2847-714">Inconsistent setting of Header or Footer components</span></span>

<span data-ttu-id="a2847-715">عند [تكوين](er-fillable-excel.md) مكون تنسيق التقارير الإلكترونية (ER) لاستخدام قالب Excel لإنشاء مستند صادر، يمكنك إضافة مكون **Excel\\الرأس** لتعبئة الرؤوس في أعلى ورقة عمل في مصنف Excel.</span><span class="sxs-lookup"><span data-stu-id="a2847-715">When you [configure](er-fillable-excel.md) an ER format component to use an Excel template to generate an outbound document, you can add the **Excel\\Header** component to fill in headers at the top of a worksheet in an Excel workbook.</span></span> <span data-ttu-id="a2847-716">يمكنك أيضًا إضافة مكون **Excel\\تذييل** لتعبئة التذييلات في أسفل ورقه العمل.</span><span class="sxs-lookup"><span data-stu-id="a2847-716">You can also add the **Excel\\Footer** component to fill in footers at the bottom of a worksheet.</span></span> <span data-ttu-id="a2847-717">لكل مكون **Excel\\رأس** أو **Excel\\تذييل** تضيفه، يجب تعيين الخاصية **مظهر الرأس/التذييل** لتحديد الصفحات التي يتم تشغيل المكون لها.</span><span class="sxs-lookup"><span data-stu-id="a2847-717">For every **Excel\\Header** or **Excel\\Footer** component that you add, you must set the **Header/footer appearance** property to specify the pages that the component is run for.</span></span> <span data-ttu-id="a2847-718">ونظرا لأنه يمكنك تكوين عدة مكونات **Excel\\رأس** أو **Excel\\تذييل** لمكون **ورقة عمل** واحد، ويمكنك إنشاء رؤوس أو تذييلات مختلفة لأنواع مختلفة من الصفحات في ورقه عمل Excel، فيجب أن تقوم بتكوين مكون **Excel\\رأس** أو **Excel\\تذييل** فردي لقيمة محددة لخاصية **مظهر الرأس/التذييل**.</span><span class="sxs-lookup"><span data-stu-id="a2847-718">Because you can configure several **Excel\\Header** or **Excel\\Footer** components for a single **Sheet** component, and you can generate different headers or footers for different type of pages in an Excel worksheet, you must configure a single **Excel\\Header** or **Excel\\Footer** component for a specific value of the **Header/footer appearance** property.</span></span> <span data-ttu-id="a2847-719">إذا تم تكوين أكثر من مكون **Excel\\رأس** أو **Excel\\تذييل** لقيمة محددة لخاصية **مظهر الرأس/التذييل**، فسيحدث خطأ في التحقق من الصحة، وتتلقي رسالة الخطا التالية: "رؤوس الصفحات/تذييلات الصفحات" (&lt;نوع المكون: الراس أو التذييل&gt;) غير متناسقة.</span><span class="sxs-lookup"><span data-stu-id="a2847-719">If more than one **Excel\\Header** or **Excel\\Footer** component is configured for a specific value of the **Header/footer appearance** property, a validation error occurs, and you receive the following error message: "Headers/footers (&lt;component type: Header or Footer&gt;) are inconsistent."</span></span>

### <a name="automatic-resolution"></a><span data-ttu-id="a2847-720">الحل التلقائي</span><span class="sxs-lookup"><span data-stu-id="a2847-720">Automatic resolution</span></span>

<span data-ttu-id="a2847-721">لا يتوفر اي خيار لإصلاح هذه المشكلة تلقائيا.</span><span class="sxs-lookup"><span data-stu-id="a2847-721">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="a2847-722">الحل اليدوي</span><span class="sxs-lookup"><span data-stu-id="a2847-722">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="a2847-723">خيار 1</span><span class="sxs-lookup"><span data-stu-id="a2847-723">Option 1</span></span>

<span data-ttu-id="a2847-724">قم بتعديل التنسيق الذي تم تكوينه عن طريق حذف أحد مكونات **Excel\\الرأس** أو **Excel\\التذييل** غير المتناسقة.</span><span class="sxs-lookup"><span data-stu-id="a2847-724">Modify the configured format by deleting one of the inconsistent **Excel\\Header** or **Excel\\Footer** components.</span></span>

#### <a name="option-2"></a><span data-ttu-id="a2847-725">خيار 2</span><span class="sxs-lookup"><span data-stu-id="a2847-725">Option 2</span></span>

<span data-ttu-id="a2847-726">قم بتعديل قيمة الخاصية الخاصة **مظهر الرأس/التذييل** لأحد مكونات **Excel\\الرأس** أو **Excel\\التذييل** غير المتناسقة.</span><span class="sxs-lookup"><span data-stu-id="a2847-726">Modify the value of the **Header/footer appearance** property for one of the inconsistent **Excel\\Header** or **Excel\\Footer** components.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a2847-727">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="a2847-727">Additional resources</span></span>

[<span data-ttu-id="a2847-728">ALLITEMS ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="a2847-728">ALLITEMS ER function</span></span>](er-functions-list-allitems.md)

[<span data-ttu-id="a2847-729">ALLITEMSQUERY ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="a2847-729">ALLITEMSQUERY ER function</span></span>](er-functions-list-allitemsquery.md)

[<span data-ttu-id="a2847-730">INT64VALUE ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="a2847-730">INT64VALUE ER function</span></span>](er-functions-conversion-int64value.md)

[<span data-ttu-id="a2847-731">وظيفة INTVALUE ER  </span><span class="sxs-lookup"><span data-stu-id="a2847-731">INTVALUE ER function</span></span>](er-functions-conversion-intvalue.md)

[<span data-ttu-id="a2847-732">FILTER ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="a2847-732">FILTER ER function</span></span>](er-functions-list-filter.md)

[<span data-ttu-id="a2847-733">WHERE ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="a2847-733">WHERE ER function</span></span>](er-functions-list-where.md)

[<span data-ttu-id="a2847-734">استخدم مصادر بيانات JOIN للحصول على البيانات من جداول التطبيقات المتعددة في تعيينات نماذج التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a2847-734">Use JOIN data sources to get data from multiple application tables in ER model mappings</span></span>](er-join-data-sources.md)

[<span data-ttu-id="a2847-735">تتبع تنفيذ تنسيقات التقارير الإلكترونية لاستكشاف مشكلات الأداء وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="a2847-735">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)

[<span data-ttu-id="a2847-736">نظرة عامة على إدارة مستندات الأعمال</span><span class="sxs-lookup"><span data-stu-id="a2847-736">Business document management overview</span></span>](er-business-document-management.md)

[<span data-ttu-id="a2847-737">منع عناصر تحكم محتوى Word في التقارير التي تم إنشاؤها</span><span class="sxs-lookup"><span data-stu-id="a2847-737">Suppress Word content controls in generated reports</span></span>](er-design-configuration-word-suppress-controls.md)

[<span data-ttu-id="a2847-738">إدارة تعيينات مشتقة متعددة لجذر نموذج واحد</span><span class="sxs-lookup"><span data-stu-id="a2847-738">Manage several derived mappings for a single model root</span></span>](er-multiple-model-mappings.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
