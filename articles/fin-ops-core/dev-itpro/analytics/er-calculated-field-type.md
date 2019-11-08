---
title: دعم استدعاءات ذات معلمات لمصادر بيانات التقارير الإلكترونية لنوع الحقل المحسوب‬
description: يوفر هذا الموضوع معلومات حول كيفية استخدام نوع الحقل المحسوب لمصادر بيانات التقارير الإلكترونية.
author: NickSelin
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 20d48795b23628bbba2896bf48940936a25e0435
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550074"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a><span data-ttu-id="fc3a7-103">دعم استدعاءات ذات معلمات لمصادر بيانات التقارير الإلكترونية لنوع الحقل المحسوب‬</span><span class="sxs-lookup"><span data-stu-id="fc3a7-103">Support parameterized calls of ER data sources of the Calculated field type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fc3a7-104">يشرح هذا الموضوع كيفية تصميم مصدر بيانات التقارير الإلكترونية باستخدام نوع **الحقل المحسوب**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-104">This topic explains how you can design an Electronic reporting (ER) data source by using the **Calculated field** type.</span></span> <span data-ttu-id="fc3a7-105">قد يحتوي مصدر البيانات هذا على تعبير التقارير الإلكترونية الذي، عند تنفيذه، يمكن التحكم به بواسطة قيم وسيطات المعلمة التي تم تكوينها في الربط الذي يستدعي مصدر البيانات هذا.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-105">This data source may contain an ER expression that, when executed, can be controlled by the values of the parameter arguments that are configured in a binding that calls this data source.</span></span> <span data-ttu-id="fc3a7-106">ومن خلال تكوين استدعاءات ذات معلمات لمصدر البيانات هذا، يمكنك إعادة استخدام مصدر بيانات واحد في العديد من عمليات الربط، مما يقلل العدد الإجمالي لمصادر البيانات التي يجب تكوينها في تعيينات نماذج التقارير الإلكترونية أو تنسيقاتها.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-106">By configuring parameterized calls of such a data source, you can reuse a single data source in many bindings, which reduces the total number of data sources that must be configured in ER model mappings or ER formats.</span></span> <span data-ttu-id="fc3a7-107">ويقوم أيضا بتبسيط مكون التقارير الإلكترونية الذي تم تكوينه، مما يقلل من تكاليف الصيانة وتكلفة الاستخدام من قبل العملاء الآخرين.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-107">It also simplifies the configured ER component, which reduces the maintenance costs and the cost of use by other consumers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="fc3a7-108">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="fc3a7-108">Prerequisites</span></span>
<span data-ttu-id="fc3a7-109">لإكمال الأمثلة في هذا الموضوع، يجب أن يكون لديك الوصول التالي:</span><span class="sxs-lookup"><span data-stu-id="fc3a7-109">To complete the examples in this topic, you must have the following access:</span></span>

- <span data-ttu-id="fc3a7-110">الوصول إلى أحد هذه الأدوار:</span><span class="sxs-lookup"><span data-stu-id="fc3a7-110">Access to one of these roles:</span></span>

    - <span data-ttu-id="fc3a7-111">مطور إعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="fc3a7-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="fc3a7-112">مستشار وظيفي لإعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="fc3a7-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="fc3a7-113">مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="fc3a7-113">System administrator</span></span>

- <span data-ttu-id="fc3a7-114">يمكنك الوصول إلى مثيل Regulatory Configuration Services (RCS) التي تم تزويدها لنفس المستأجر مثل Finance and Operations، لأحد الأدوار التالية:</span><span class="sxs-lookup"><span data-stu-id="fc3a7-114">Access to Regulatory Configuration Services (RCS) that have been provisioned for the same tenant as Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="fc3a7-115">مطور إعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="fc3a7-115">Electronic reporting developer</span></span>
    - <span data-ttu-id="fc3a7-116">مستشار وظيفي لإعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="fc3a7-116">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="fc3a7-117">مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="fc3a7-117">System administrator</span></span>

<span data-ttu-id="fc3a7-118">من [مركز التنزيل لـ Microsoft](https://go.microsoft.com/fwlink/?linkid=874684)، قم بتنزيل الملف المضغوط **دعم استدعاءات ذات معلمات لمصادر بيانات التقارير الإلكترونية لنوع الحقل المحسوب**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-118">From the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684), download the zipped (compressed) file **Support parameterized calls of ER data sources of Calculated field type**.</span></span> <span data-ttu-id="fc3a7-119">ويحتوي على تكوينات التقارير الإلكترونية التالية والتي يجب استخراجها وتخزينها محليًا.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-119">It contains the following ER configurations that must be extracted and stored locally.</span></span>

| <span data-ttu-id="fc3a7-120">**المحتوى**</span><span class="sxs-lookup"><span data-stu-id="fc3a7-120">**Content**</span></span>                           | <span data-ttu-id="fc3a7-121">**اسم الملف**</span><span class="sxs-lookup"><span data-stu-id="fc3a7-121">**File name**</span></span>                                        |
|---------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fc3a7-122">تكوين نموذج عينة بيانات التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="fc3a7-122">Sample ER data model configuration</span></span>    | <span data-ttu-id="fc3a7-123">Model to learn parameterized calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="fc3a7-123">Model to learn parameterized calls.version.1.xml</span></span>     |
| <span data-ttu-id="fc3a7-124">تكوين بيانات تعريف عينة التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="fc3a7-124">Sample ER metadata configuration</span></span>      | <span data-ttu-id="fc3a7-125">Metadata to learn parameterized calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="fc3a7-125">Metadata to learn parameterized calls.version.1.xml</span></span>  |
| <span data-ttu-id="fc3a7-126">تكوين تعيين نموذج عينة التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="fc3a7-126">Sample ER model mapping configuration</span></span> | <span data-ttu-id="fc3a7-127">Mapping to learn parameterized calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="fc3a7-127">Mapping to learn parameterized calls.version.1.1.xml</span></span> |
| <span data-ttu-id="fc3a7-128">تكوين تنسيق عينة التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="fc3a7-128">Sample ER format configuration</span></span>        | <span data-ttu-id="fc3a7-129">Format to learn parameterized calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="fc3a7-129">Format to learn parameterized calls.version.1.1.xml</span></span>  |

## <a name="sign-in-to-your-rcs-instance"></a><span data-ttu-id="fc3a7-130">تسجيل الدخول إلى مثيل RCS</span><span class="sxs-lookup"><span data-stu-id="fc3a7-130">Sign in to your RCS instance</span></span>
<span data-ttu-id="fc3a7-131">في هذا المثال، سوف تنشئ تكوينًا للشركة النموذجية Litware, Inc. في RCS يجب عليك أولاً إكمال الخطوات الموجودة في الإجراء [‏‫إنشاء موفر تكوين ووضع علامة عليه على أنه نشط‬](tasks/er-configuration-provider-mark-it-active-2016-11.md):</span><span class="sxs-lookup"><span data-stu-id="fc3a7-131">In this example, you will create a configuration for the sample company, Litware, Inc. First, in RCS, you must complete the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure:</span></span>

1. <span data-ttu-id="fc3a7-132">في لوحة المعلومات الافتراضية، حدد **‏‫إعداد التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-132">On the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="fc3a7-133">حدد **تكوينات إعداد التقارير‬**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-133">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="fc3a7-134">قم باستيراد التكوينات التي تم تنزيلها إلى RCS بالتسلسل التالي: نموذج البيانات، وبيانات التعريف، وتعيين النموذج، والتنسيق.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-134">Import the downloaded configurations to RCS in the following sequence: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="fc3a7-135">أكمل الخطوات التالية لكل تكوين خاص بإعداد التقارير الإلكترونية:</span><span class="sxs-lookup"><span data-stu-id="fc3a7-135">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="fc3a7-136">حدد **تبادل**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-136">Select **Exchange.**</span></span>
    2. <span data-ttu-id="fc3a7-137">حدد **تحميل من ملف XML**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-137">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="fc3a7-138">حدد **استعراض**، ثم حدد الملف المطلوب لتكوين التقارير الإلكترونية بالتنسيق XML.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-138">Select **Browse**, and then select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="fc3a7-139">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-139">Select **OK.**</span></span>

## <a name="review-the-provided-er-solution"></a><span data-ttu-id="fc3a7-140">مراجعه الحل المتوفر لإعداد التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="fc3a7-140">Review the provided ER solution</span></span>

### <a name="review-model-mapping"></a><span data-ttu-id="fc3a7-141">مراجعة تعيين النموذج</span><span class="sxs-lookup"><span data-stu-id="fc3a7-141">Review model mapping</span></span>

1. <span data-ttu-id="fc3a7-142">في شجرة التكوين، قم بتوسيع محتوى العنصر **نموذج للتعرف على الاستدعاءات ذات معلمات‬**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-142">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="fc3a7-143">حدد **تعيين للتعرف على الاستدعاءات ذات معلمات**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-143">Select **Mapping to learn parameterized calls**.</span></span>
3. <span data-ttu-id="fc3a7-144">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-144">Select **Designer**.</span></span>
4. <span data-ttu-id="fc3a7-145">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-145">Select **Designer**.</span></span>  
   
<span data-ttu-id="fc3a7-146">يتم تصميم تعيين نموذج إعداد التقارير الإلكترونية هذا للقيام بما يلي:</span><span class="sxs-lookup"><span data-stu-id="fc3a7-146">This ER model mapping is designed to do the following:</span></span>

- <span data-ttu-id="fc3a7-147">إحضار قائمة بأكواد الضريبة (مصدر بيانات **الضريبة**) الموجودة في الجدول **TaxTable**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-147">Fetch the list of tax codes (**Tax** data source) residing in the   **TaxTable** table.</span></span>
- <span data-ttu-id="fc3a7-148">إحضار قائمة بحركات الضريبة (مصدر بيانات **الحركة**) الموجودة في الجدول **TaxTrans**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-148">Fetch the list of tax transactions (**Trans** data source) residing in the   **TaxTrans** table:</span></span>
    
    - <span data-ttu-id="fc3a7-149">تجميع قائمة بالحركات التي تم إحضارها (مصدر بيانات **التجميع**) حسب كود الضريبة.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-149">Group the list of fetched transactions (**Gr** data source) by tax code.</span></span>
    - <span data-ttu-id="fc3a7-150">حساب الحركات المجمعة التي تتبع القيم المجمعة حسب كود الضريبة:</span><span class="sxs-lookup"><span data-stu-id="fc3a7-150">Calculate for grouped transactions following aggregated values per   tax code:</span></span>

        - <span data-ttu-id="fc3a7-151">مجموع قيم أساس الضريبة.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-151">Sum of tax base values.</span></span>
        - <span data-ttu-id="fc3a7-152">مجموع قيم الضريبة.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-152">Sum of tax values.</span></span>
        - <span data-ttu-id="fc3a7-153">الحد الأدنى لقيمة معدل الضريبة المطبق.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-153">Minimum value of applied tax rate.</span></span>

<span data-ttu-id="fc3a7-154">يقوم تعيين النموذج في هذا التكوين بتنفيذ نموذج البيانات الأساسي لأي من تنسيقات التقارير الإلكترونية التي تم إنشاؤها لهذا النموذج وتنفيذها في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-154">The model mapping in this configuration implements the base data model for any of the ER formats created for this model and executed in Finance and Operations.</span></span> <span data-ttu-id="fc3a7-155">نتيجة لذلك، يتم كشف محتوى مصادر بيانات **الضريبة** و**التجميع** لتنسيقات التقارير الإلكترونية مثل مصادر البيانات المجردة.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-155">As a result, the content of the **Tax** and **Gr** data sources is exposed for ER formats such as abstract data sources.</span></span>

  ![صفحة مصمم تعيين النموذج التي تعرض مصادر بيانات الضريبة والتجميع](media/er-calculated-field-type-01.png)

5.  <span data-ttu-id="fc3a7-157">أغلق صفحة **مصمم تعيين النموذج**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-157">Close the **Model mapping designer** page.</span></span>
6.  <span data-ttu-id="fc3a7-158">أغلق صفحة **تعيين النموذج**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-158">Close the **Model mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="fc3a7-159">مراجعة التنسيق</span><span class="sxs-lookup"><span data-stu-id="fc3a7-159">Review format</span></span>

1. <span data-ttu-id="fc3a7-160">في شجرة التكوين، قم بتوسيع محتوى العنصر **نموذج للتعرف على الاستدعاءات ذات معلمات‬**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-160">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="fc3a7-161">حدد **تنسيق للتعرف على الاستدعاءات ذات معلمات**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-161">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="fc3a7-162">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-162">Select **Designer**.</span></span> <span data-ttu-id="fc3a7-163">يتم تصميم تنسيق إعداد التقارير الإلكترونية هذا للقيام بما يلي:</span><span class="sxs-lookup"><span data-stu-id="fc3a7-163">This ER format is designed to do the following:</span></span>

  - <span data-ttu-id="fc3a7-164">إنشاء بيان ضريبة بتنسيق XML.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-164">Generate a tax statement in XML format.</span></span>
  - <span data-ttu-id="fc3a7-165">تقديم المستويات التالية لفرض الضرائب في بيان الضريبة: العادي والمخفض ولا شيء.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-165">Present the following levels of taxation in the tax statement: regular, reduced, and none.</span></span>
  - <span data-ttu-id="fc3a7-166">تقديم تفاصيل متعدد في كل مستوى فرض ضرائب، مع وجود عدد مختلف من التفاصيل في كل مستوى.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-166">Present multiple details at each taxation level, having a different number of details in each level.</span></span>

  ![صفحة مصمم التنسيق‬](media/er-calculated-field-type-02.png)

4. <span data-ttu-id="fc3a7-168">حدد **التعيين**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-168">Select **Mapping**.</span></span>
5. <span data-ttu-id="fc3a7-169">قم بتوسيع عناصر **النموذج**، و**البيانات**، و**الملخص**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-169">Expand the **Model**, **Data,** and **Summary** items.</span></span> 

   <span data-ttu-id="fc3a7-170">يحتوي الحقل المحسوب **Model.Data.Summary.Level** على التعبير الذي يقوم بإرجاع كود مستوى فرض الضرائب (**العادي**، أو **المخفض**، أو **لا شيء**، أو **غير ذلك**) كقيمة نصية لأي كود ضريبة يمكن استرجاعه من مصدر البيانات **Model.Data.Summary** في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-170">The calculated field **Model.Data.Summary.Level** contains the expression that returns the code of the taxation level (**Regular**, **Reduced**, **None,** or **Other**) as a text value for any tax code that can be retrieved from the **Model.Data.Summary** data source at run time.</span></span>

  ![صفحة مصمم تنسيق تظهر تفاصيل نموذج لنموذج بيانات لمعرفة الاستدعاءات ذات معلمات](media/er-calculated-field-type-03.png)

6. <span data-ttu-id="fc3a7-172">قم بتوسيع عنصر **Model**.**Data2**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-172">Expand the **Model**.**Data2** item.</span></span>
7. <span data-ttu-id="fc3a7-173">قم بتوسيع عنصر **Model**.**Data2.Summary2**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-173">Expand the **Model**.**Data2.Summary2** item.</span></span>
   
   <span data-ttu-id="fc3a7-174">يتم تكوين مصدر البيانات **Model**.**Data2.Summary2** لتجميع تفاصيل حركة مصدر بيانات **Model.Data.Summary** حسب مستوى فرض الضرائب (الذي يتم إرجاعه بواسطة الحقل المحسوب **Model.Data.Summary.Level**) وحساب التجميعات.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-174">The **Model**.**Data2.Summary2** data source is configured to group the **Model.Data.Summary** data source transaction details by taxation level (returned by the **Model.Data.Summary.Level** calculated field) and compute the aggregations.</span></span>

  ![صفحه مصمم تنسيق تُظهر تفاصيل مصدر بيانات Model.Data2.Summary2](media/er-calculated-field-type-04.png)

8. <span data-ttu-id="fc3a7-176">راجع الحقول المحسوبة **Model**.**Data2.Level1**، و**Model**.**Data2.Level2**، و**Model**.**Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-176">Review the calculated fields **Model**.**Data2.Level1**, **Model**.**Data2.Level2**, and **Model**.**Data2.Level3.**</span></span> <span data-ttu-id="fc3a7-177">يتم استخدام هذه الحقول المحسوبة لتصفية قائمة سجلات **Model**.**Data2.Summary2** وإرجاع السجلات التي تمثل مستوى فرض ضرائب معين فقط.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-177">These calculated fields are used to filter the **Model**.**Data2.Summary2** records list and return only records that represent a particular taxation level.</span></span>
9. <span data-ttu-id="fc3a7-178">أغلق صفحة **مصمم المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-178">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="fc3a7-179">إنشاء تنسيق مشتق</span><span class="sxs-lookup"><span data-stu-id="fc3a7-179">Create a derived format</span></span>
<span data-ttu-id="fc3a7-180">يمكنك تحسين التنسيق المتوفر عن طريق إضافة حقل محسوب واحد لتصفية مستوى فرض الضرائب المطلوب بدلاً من استخدام الحقول الثلاثة الموجودة: **Model**.**Data2.Level1**، و**Model**.**Data2.Level2**، و**Model**.**Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-180">You can improve the provided format by adding one calculated field to filter the required taxation level instead of using the existing three fields: **Model**.**Data2.Level1**, **Model**.**Data2.Level2,** and **Model**.**Data2.Level3**.</span></span> <span data-ttu-id="fc3a7-181">يمكن تحديد مستوى فرض الضرائب المطلوب في الموقع الذي سيتم فيه استدعاء هذا الحقل الجديد المحسوب.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-181">The required taxation level can be specified in the location where this new calculated field will be called.</span></span>

1. <span data-ttu-id="fc3a7-182">في شجرة التكوين، قم بتوسيع محتوى العنصر **نموذج للتعرف على الاستدعاءات ذات معلمات‬**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-182">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="fc3a7-183">حدد **تنسيق للتعرف على الاستدعاءات ذات معلمات**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-183">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="fc3a7-184">حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-184">Select **Create configuration**.</span></span>
4. <span data-ttu-id="fc3a7-185">حدد **اشتقاق من الاسم: تنسيق للتعرف على الاستدعاءات ذات معلمات، Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-185">Select **Derive from Name: Format to learn parameterized calls, Microsoft**.</span></span>
5. <span data-ttu-id="fc3a7-186">في حقل **الاسم**، أدخل **تنسيق للتعرف على الاستدعاءات ذات معلمات (مخصص)**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-186">In the **Name** field, enter **Format to learn parameterized calls (custom)**.</span></span>
6. <span data-ttu-id="fc3a7-187">حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-187">Select **Create configuration.**</span></span>

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a><span data-ttu-id="fc3a7-188">تكوين حقل محسوب ذي معلمات يرجع قائمة سجلات</span><span class="sxs-lookup"><span data-stu-id="fc3a7-188">Configure a parameterized calculated field that returns a list of records</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="fc3a7-189">بدء إضافة حقل محسوب جديد</span><span class="sxs-lookup"><span data-stu-id="fc3a7-189">Start adding a new calculated field</span></span>

1. <span data-ttu-id="fc3a7-190">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-190">Select **Designer**.</span></span>
2. <span data-ttu-id="fc3a7-191">حدد **توسيع/طي** لتوسيع كافة عناصر التنسيق.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-191">Select **Expand/collapse** to expand all format items.</span></span>
3. <span data-ttu-id="fc3a7-192">حدد **التعيين**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-192">Select **Mapping**.</span></span>
4. <span data-ttu-id="fc3a7-193">قم بتوسيع عنصر **النموذج**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-193">Expand the **Model** item.</span></span>
5. <span data-ttu-id="fc3a7-194">حدد عنصر **Model.Data2**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-194">Select the **Model.Data2** item.</span></span>
6. <span data-ttu-id="fc3a7-195">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-195">Select **Add**.</span></span>
7. <span data-ttu-id="fc3a7-196">حدد **الوظائف\\حقل محسوب**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-196">Select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="fc3a7-197">في حقل **الاسم**، أدخل **المستويات**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-197">In the **Name** field, enter **Levels**.</span></span>
9. <span data-ttu-id="fc3a7-198">حدد **تحرير المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-198">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="fc3a7-199">تحديد معلمة لإضافة حقل محسوب</span><span class="sxs-lookup"><span data-stu-id="fc3a7-199">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="fc3a7-200">حدد **معلمات**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-200">Select **Parameters**.</span></span>
2. <span data-ttu-id="fc3a7-201">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-201">Select **New**.</span></span>
3. <span data-ttu-id="fc3a7-202">في حقل **الاسم**، أدخل **مستوى فرض الضرائب**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-202">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="fc3a7-203">في حقل **النوع**، حدد **سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-203">In the **Type** field, select **String**.</span></span>

    <span data-ttu-id="fc3a7-204">يمكن استخدام أنواع البيانات الأولية فقط لتحديد نوع وسيطة المعلمة.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-204">Only primitive data types can be used to specify the type of the parameter’s argument.</span></span> <span data-ttu-id="fc3a7-205">ولهذا لا يمكن استخدام الأنواع **قائمة سجلات**، و**سجل**، و**التعداد** لهذا الغرض.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-205">Therefore, **Record list**, **Record**, and **Enum** types cannot be used for this purpose.</span></span>

    <span data-ttu-id="fc3a7-206">الحد الأقصى لعدد المعلمات التي يمكن تحديدها لحقل محسوب واحد هو 8.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-206">The maximum number of parameters that can be specified for a single calculated field is 8.</span></span>

    ![قائمة مصادر بيانات المعلمات](media/er-calculated-field-type-05.png)

5. <span data-ttu-id="fc3a7-208">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-208">Select **OK**.</span></span>

<span data-ttu-id="fc3a7-209">بإضافة هذه المعلمة، فأنت تحدد الشرط الذي يجب توفره لاستدعاء هذا الحقل المحسوب.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-209">By adding this parameter, you specify the condition that must be in place to call this calculated field.</span></span> <span data-ttu-id="fc3a7-210">عند استدعاء هذا الحقل المحسوب، يجب تحديد وسيطة معلمة **مستوى فرض الضرائب** كقيمة بتنسيق **سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-210">When you call this calculated field, you need to specify the argument of the **Taxation Level** parameter as a value with **String** format.</span></span>

   <span data-ttu-id="fc3a7-211">تأكد من تعريف المعلمات فقط للحقول المحسوبة الموجودة في حاوية (إما **قائمة السجلات**، أو **السجل**، أو **الحاوية**).</span><span class="sxs-lookup"><span data-stu-id="fc3a7-211">Make sure that you define parameters only for those calculated fields that reside in a container (either **Record list**, **Record**, or **Container**).</span></span>

   <span data-ttu-id="fc3a7-212">تتوفر المعلمة المكونة في قائمة مصادر البيانات لهذا الحقل المحسوب.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-212">The configured parameter is available in the list of data sources for this calculated field.</span></span> <span data-ttu-id="fc3a7-213">يمكنك إضافة المعلمة إلى التعبير المكون عن طريق تحديد **إضافة مصدر بيانات**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-213">You can add the parameter to the configured expression by selecting **Add data source**.</span></span>

   ![حقول مصادر البيانات](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="fc3a7-215">تحديد تعبير لإضافة حقل محسوب</span><span class="sxs-lookup"><span data-stu-id="fc3a7-215">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="fc3a7-216">في حقل **المعادلة**، أدخل:</span><span class="sxs-lookup"><span data-stu-id="fc3a7-216">In the **Formula** field, enter:</span></span> 

    <span data-ttu-id="fc3a7-217">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span><span class="sxs-lookup"><span data-stu-id="fc3a7-217">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span></span>
    
2. <span data-ttu-id="fc3a7-218">حدد معلمة **مستوى فرض الضرائب** في قائمة مصادر البيانات.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-218">Select the **Taxation Level** parameter in the list of data sources.</span></span>
3. <span data-ttu-id="fc3a7-219">حدد **إضافة مصدر البيانات**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-219">Select **Add data source**.</span></span>
4. <span data-ttu-id="fc3a7-220">في حقل **المعادلة**، أنجز التعبير كما يلي:</span><span class="sxs-lookup"><span data-stu-id="fc3a7-220">In the **Formula** field, finalize the expression as:</span></span>  

    <span data-ttu-id="fc3a7-221">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span><span class="sxs-lookup"><span data-stu-id="fc3a7-221">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span></span>

5. <span data-ttu-id="fc3a7-222">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-222">Select **Save**.</span></span>

    ![معلومات حقل مصدر البيانات](media/er-calculated-field-type-07.png)

6. <span data-ttu-id="fc3a7-224">أغلق صفحة **مصمم المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-224">Close the **Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="fc3a7-225">إنهاء إضافة حقل محسوب جديد</span><span class="sxs-lookup"><span data-stu-id="fc3a7-225">Finish adding a new calculated field</span></span>

- <span data-ttu-id="fc3a7-226">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-226">Select **OK**.</span></span>

<span data-ttu-id="fc3a7-227">في صفحة **مصمم المعادلة**، يحتاج حقل **المستويات** المحسوب المكوّن ذو معلمات إلى وسيطة **سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-227">On the **Format designer** page, the configured parameterized calculated field **Levels** requires a **String** argument.</span></span>

![قائمة موسعة بمستويات الحقول المحسوبة](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements"></a><span data-ttu-id="fc3a7-229">استخدام الحقل المحسوب المكون لربط عناصر التنسيق</span><span class="sxs-lookup"><span data-stu-id="fc3a7-229">Use the configured calculated field for binding format elements</span></span>

1. <span data-ttu-id="fc3a7-230">حدد **Model.Data2.Levels** لتحديد الحقل المحسوب الذي تم تكوينه.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-230">Select **Model.Data2.Levels** to select the configured calculated field.</span></span>
2. <span data-ttu-id="fc3a7-231">حدد عنصر التنسيق **Statement.Taxation.Regular**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-231">Select the **Statement.Taxation.Regular** format element.</span></span>
3. <span data-ttu-id="fc3a7-232">حدد **ربط**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-232">Select **Bind**.</span></span>
4. <span data-ttu-id="fc3a7-233">حدد **نعم** لتأكيد استبدال مصدر البيانات المستخدم حاليًا، **المستوى1**، بمصدر البيانات الجديد، **المستويات**، في كافة عناصر التنسيق المتداخلة لعنصر التنسيق المحدد.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-233">Select **Yes** to confirm the replacement of the currently used data source, **Level1**, by the new data source, **Levels**, in all nested format elements of the selected format element.</span></span>

    <span data-ttu-id="fc3a7-234">تم إنشاء الربط المطبق كاستدعاء للحقل المحسوب ذي معلمات.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-234">Applied binding has been built as a call of the parameterized calculated field.</span></span> <span data-ttu-id="fc3a7-235">بشكل افتراضي، يتم استخدام اسم عنصر التنسيق المنضم كوسيطة للحقل المحسوب ذي معلمات تحت الشروط التالية:</span><span class="sxs-lookup"><span data-stu-id="fc3a7-235">By default, the name of the bound format element is used as an argument for parameterized calculated field under the following conditions:</span></span>

      - <span data-ttu-id="fc3a7-236">يتم تكوين الحقل المحسوب لاستخدام معلمة واحدة.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-236">The calculated field is configured to use a single parameter.</span></span>
      - <span data-ttu-id="fc3a7-237">يتم تعريف نوع بيانات هذه المعلمة **كسلسلة**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-237">The data type of this parameter is defined as **String**.</span></span>

    <span data-ttu-id="fc3a7-238">عندما يكون اسم عنصر التنسيق المنضم فارغًا، يتم استخدام اسم مصدر البيانات الخاص بهذا العنصر في الربط المطبق.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-238">When the name of the bound format element is blank, the data source name of this element is used in applied binding.</span></span>

5. <span data-ttu-id="fc3a7-239">حدد عنصر التنسيق **Statement.Taxation.Reduced**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-239">Select the **Statement.Taxation.Reduced** format element.</span></span>
6. <span data-ttu-id="fc3a7-240">حدد **ربط**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-240">Select **Bind**.</span></span>
7. <span data-ttu-id="fc3a7-241">حدد **نعم** لتأكيد استبدال مصدر البيانات المستخدم حاليًا، **المستوى2**، بمصدر البيانات الجديد، **المستويات**، في كافة عناصر التنسيق المتداخلة لعنصر التنسيق المحدد.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-241">Select **Yes** to confirm the replacement of the currently used data source, **Level2**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>
8. <span data-ttu-id="fc3a7-242">حدد عنصر التنسيق **Statement.Taxation.None**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-242">Select the **Statement.Taxation.None** format element.</span></span>
9. <span data-ttu-id="fc3a7-243">حدد **ربط**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-243">Select **Bind**.</span></span>
10. <span data-ttu-id="fc3a7-244">حدد **نعم** لتأكيد استبدال مصدر البيانات المستخدم حاليًا، **المستوى3**، بمصدر البيانات الجديد، **المستويات**، في كافة عناصر التنسيق المتداخلة لعنصر التنسيق المحدد.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-244">Select **Yes** to confirm the replacement of the currently used data source, **Level3**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>

   <span data-ttu-id="fc3a7-245">عند تعيين وسيطة الحقل المحسوب ذي المعلمات لعنصر XML الذي يمثل مستوى فرض الضرائب (على سبيل المثال **‎Model.Data2.Levels("Reduced")** كقيمة نصية)، لا تحتاج إلى القيام بنفس الإجراءات لسمات XML المتداخلة — سترث الارتباطات الخاصة بها تلقائيًا قيمة الوسيطة المعرفة في المستوى الأصل (**Model.Data2.Levels.aggregated.Base**، وليس **Model.Data2.Levels("Reduced").aggregated.Base**).</span><span class="sxs-lookup"><span data-stu-id="fc3a7-245">When you specify the argument of the parameterized calculated field for the XML element representing taxation level (for example, **Model.Data2.Levels("Reduced")** as a text value), you don’t need to do the same for nested XML attributes—their bindings will automatically inherit the value of the argument defined on the parent level (**Model.Data2.Levels.aggregated.Base**, not **Model.Data2.Levels("Reduced").aggregated.Base**).</span></span>

<span data-ttu-id="fc3a7-246">الاستدعاءات المتكررة لأي حقل محسوب ذي معلمات غير معتمدة.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-246">Recurrent calls of any parameterized calculated field are not supported.</span></span>

<span data-ttu-id="fc3a7-247">يمكنك تحديد **تحرير المعادلة**، وتغيير الوسيطة المطبقة بشكل افتراضي للحقل المحسوب ذي المعلمات في الربط المحدد.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-247">You can select **Edit formula**, and change the applied-by-default argument of the parameterized calculated field in the selected binding.</span></span> <span data-ttu-id="fc3a7-248">إذا كانت هذه الوسيطة مفقودة، فقد تتسبب في حدوث أخطاء في وقت التشغيل — يتم إعلام المستخدمين بمثل هذا الموقف عند التحقق من صحة التنسيق الحالي.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-248">If this argument is missing, it can cause errors at run time — users are informed about such a situation when the current format is validated.</span></span>

![الإعلام عن تحذير التحقق من الصحة](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a><span data-ttu-id="fc3a7-250">تكوين حقل محسوب ذي معلمات لإرجاع سجل</span><span class="sxs-lookup"><span data-stu-id="fc3a7-250">Configure a parameterized calculated field to return a record</span></span>
<span data-ttu-id="fc3a7-251">عندما يقوم حقل محسوب ذو معلمات بإرجاع سجل، تحتاج إلى دعم ربط الحقول الفردية لهذا السجل بعناصر التنسيق.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-251">When a parameterized calculated field returns a record, you need to support binding of individual fields of this record to format elements.</span></span> <span data-ttu-id="fc3a7-252">في مثل هذه الحالات لن يكون هناك ربط أصلي يحتوي على قيمة وسيطة لاستدعاء حقل محسوب ذي معلمات — يجب تعريف هذه القيمة في ربط حقل سجل واحد.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-252">In such cases there will be no parent binding that contains the value of an argument to call a parameterized calculated field — this value must be defined in the binding of a single record’s field.</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="fc3a7-253">بدء إضافة حقل محسوب جديد</span><span class="sxs-lookup"><span data-stu-id="fc3a7-253">Start adding a new calculated field</span></span>

1. <span data-ttu-id="fc3a7-254">حدد عنصر **Model.Data2**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-254">Select the **Model.Data2** item.</span></span>
2. <span data-ttu-id="fc3a7-255">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-255">Select **Add**.</span></span>
3. <span data-ttu-id="fc3a7-256">حدد **الوظائف\\حقل محسوب**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-256">Select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="fc3a7-257">في حقل **الاسم**، أدخل **‏‫LevelRecord‬**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-257">In the **Name** field, enter **LevelRecord**.</span></span>
5. <span data-ttu-id="fc3a7-258">حدد **تحرير المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-258">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="fc3a7-259">تحديد معلمة لإضافة حقل محسوب</span><span class="sxs-lookup"><span data-stu-id="fc3a7-259">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="fc3a7-260">حدد **معلمات**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-260">Select **Parameters**.</span></span>
2. <span data-ttu-id="fc3a7-261">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-261">Select **New**.</span></span>
3. <span data-ttu-id="fc3a7-262">في حقل **الاسم**، أدخل **مستوى فرض الضرائب**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-262">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="fc3a7-263">في حقل **النوع**، حدد **سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-263">In the **Type** field, select **String**.</span></span>
5. <span data-ttu-id="fc3a7-264">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-264">Select **OK**.</span></span>

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="fc3a7-265">تحديد تعبير لإضافة حقل محسوب</span><span class="sxs-lookup"><span data-stu-id="fc3a7-265">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="fc3a7-266">في حقل **المعادلة**، أدخل ما يلي:</span><span class="sxs-lookup"><span data-stu-id="fc3a7-266">In the **Formula** field, enter the following:</span></span>  
    
    <span data-ttu-id="fc3a7-267">**FIRSTORNULL(\@.Levels(**</span><span class="sxs-lookup"><span data-stu-id="fc3a7-267">**FIRSTORNULL(\@.Levels(**</span></span>

2. <span data-ttu-id="fc3a7-268">حدد المعلمة **مستوى فرض الضرائب**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-268">Select the **Taxation Level** parameter.</span></span>
3. <span data-ttu-id="fc3a7-269">حدد **إضافة مصدر البيانات**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-269">Select **Add data source**.</span></span>
4. <span data-ttu-id="fc3a7-270">في حقل **المعادلة**، قم بإلحاق **'مستوى فرض الضرائب'))** بما أدخلته في الخطوة 1 لإنهاء التعبير إلى:</span><span class="sxs-lookup"><span data-stu-id="fc3a7-270">In the **Formula** field, append **'Taxation Level'))** to what you entered in Step 1 to finalize the expression to:</span></span>  
    
    <span data-ttu-id="fc3a7-271">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span><span class="sxs-lookup"><span data-stu-id="fc3a7-271">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span></span>

5. <span data-ttu-id="fc3a7-272">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-272">Select **Save**.</span></span>
6. <span data-ttu-id="fc3a7-273">أغلق صفحة **مصمم المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-273">Close **the Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="fc3a7-274">إنهاء إضافة حقل محسوب جديد</span><span class="sxs-lookup"><span data-stu-id="fc3a7-274">Finish adding a new calculated field</span></span>

-   <span data-ttu-id="fc3a7-275">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-275">Select **OK**.</span></span>

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a><span data-ttu-id="fc3a7-276">استخدام الحقل المحسوب المكون لربط عناصر التنسيق</span><span class="sxs-lookup"><span data-stu-id="fc3a7-276">Use the configured calculated field to bind format elements</span></span>

1. <span data-ttu-id="fc3a7-277">قم بتوسيع **Model.Data2.LevelRecord** لتحديد الحقل المحسوب الذي تم تكوينه.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-277">Expand **Model.Data2.LevelRecord** to select the configured calculated field.</span></span>
2. <span data-ttu-id="fc3a7-278">قم بتوسيع الحاوية **Model.Data2.LevelRecord.aggregated** للحقل المحسوب الذي تم تكوينه.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-278">Expand the **Model.Data2.LevelRecord.aggregated** container of the configured calculated field.</span></span>
3. <span data-ttu-id="fc3a7-279">حدد الحقل **Model.Data2.LevelRecord.aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-279">Select the **Model.Data2.LevelRecord.aggregated.Base** field.</span></span>
4. <span data-ttu-id="fc3a7-280">حدد عنصر التنسيق **Statement.Taxation.None**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-280">Select the **Statement.Taxation.None** format element.</span></span>
5. <span data-ttu-id="fc3a7-281">حدد **إلغاء الربط**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-281">Select **Unbind**.</span></span>
6. <span data-ttu-id="fc3a7-282">حدد عنصر التنسيق **Statement.Taxation.None.Base**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-282">Select the **Statement.Taxation.None.Base** format element.</span></span>
7. <span data-ttu-id="fc3a7-283">حدد **ربط**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-283">Select **Bind**.</span></span>
8. <span data-ttu-id="fc3a7-284">حدد **تحرير المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-284">Select **Edit formula**.</span></span>
9. <span data-ttu-id="fc3a7-285">قم بتغيير التعبير إلى **Model.Data2.LevelRecord("None").aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-285">Change the expression to **Model.Data2.LevelRecord("None").aggregated.Base**.</span></span>

![التعبير المحدّث](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a><span data-ttu-id="fc3a7-287">إزالة الحقول المحسوبة غير المستخدمة</span><span class="sxs-lookup"><span data-stu-id="fc3a7-287">Remove calculated fields that are not used</span></span>

1. <span data-ttu-id="fc3a7-288">حدد **Model.Data2.Level1**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-288">Select **Model.Data2.Level1**.</span></span>
2. <span data-ttu-id="fc3a7-289">حدد **حذف**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-289">Select **Delete**.</span></span>
3. <span data-ttu-id="fc3a7-290">حدد **Model.Data2.Level2**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-290">Select **Model.Data2.Level2**.</span></span>
4. <span data-ttu-id="fc3a7-291">حدد **حذف**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-291">Select **Delete**.</span></span>
5. <span data-ttu-id="fc3a7-292">حدد **Model.Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-292">Select **Model.Data2.Level3**.</span></span>
6. <span data-ttu-id="fc3a7-293">حدد **حذف**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-293">Select **Delete**.</span></span>
7. <span data-ttu-id="fc3a7-294">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-294">Select **Save**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="fc3a7-295">لقد قمت بإعادة استخدام نفس الحقل المحسوب **Model.Data2.Levels** عدة مرات في روابط التنسيق.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-295">You reused the same calculated field **Model.Data2.Levels** several times in format bindings.</span></span> <span data-ttu-id="fc3a7-296">إن استخدام حقل محسوب واحد والاحتفاظ به أسهل بكثير من تنفيذ ذلك لعدة حقول متشابهة.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-296">It is much easier to use and maintain a single calculated field instead of doing this for multiple similar fields.</span></span>

8. <span data-ttu-id="fc3a7-297">أغلق صفحة **مصمم المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-297">Close the **Format designer** page.</span></span>

## <a name="complete-adjusted-version-of-a-derived-format"></a><span data-ttu-id="fc3a7-298">إكمال الإصدار المعدل لتنسيق مشتق</span><span class="sxs-lookup"><span data-stu-id="fc3a7-298">Complete adjusted version of a derived format</span></span>

1. <span data-ttu-id="fc3a7-299">في علامة التبويب السريعة **الإصدارات**، حدد **تغيير الحالة**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-299">In the **Versions** FastTab, select **Change status**.</span></span>
2. <span data-ttu-id="fc3a7-300">حدد **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-300">Select **Complete**.</span></span>

## <a name="export-completed-version-of-a-derived-format"></a><span data-ttu-id="fc3a7-301">تصدير الإصدار المكتمل لتنسيق مشتق</span><span class="sxs-lookup"><span data-stu-id="fc3a7-301">Export completed version of a derived format</span></span>

1. <span data-ttu-id="fc3a7-302">حدد التنسيق **تنسيق للتعرف على الاستدعاءات ذات معلمات (مخصص)** في شجره التكوينات.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-302">Select **Format to learn parameterized calls (custom)** format in the configurations tree.</span></span>
2. <span data-ttu-id="fc3a7-303">في علامة التبويب السريعة **الإصدارات**، حدد الإصدار المكتمل 1.1.1.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-303">In the **Versions** FastTab, select the completed version 1.1.1.</span></span>
3. <span data-ttu-id="fc3a7-304">حدد **تبادل**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-304">Select **Exchange**.</span></span>
4. <span data-ttu-id="fc3a7-305">حدد **تصدير كملف XML**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-305">Select **Export as XML file**.</span></span>
5. <span data-ttu-id="fc3a7-306">قم بتخزين التكوين الذي تم تنزيله محليًا، بتنسيق XML.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-306">Store the downloaded configuration locally, in XML format.</span></span>

## <a name="test-er-formats"></a><span data-ttu-id="fc3a7-307">اختبار تنسيقات التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="fc3a7-307">Test ER formats</span></span> 
<span data-ttu-id="fc3a7-308">يمكنك تشغيل تنسيقات التقارير الإلكترونية الأولية والمحسنة للتأكد من أن الحقول المحسوبة ذات معلمات والتي تم تكوينها تعمل بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-308">You can run the initial and improved ER formats to make sure that configured parameterized calculated fields work properly.</span></span>

### <a name="import-er-configurations"></a><span data-ttu-id="fc3a7-309">استيراد تكوينات التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="fc3a7-309">Import ER configurations</span></span>
<span data-ttu-id="fc3a7-310">يمكنك استيراد التكوينات التي تمت مراجعتها من RCS باستخدام مستودع التقارير الإلكترونية الخاص بالنوع **RCS**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-310">You can import reviewed configurations from RCS by using the ER repository of the **RCS** type.</span></span> <span data-ttu-id="fc3a7-311">إذا كنت قد قمت بالفعل بالخطوات المذكورة في الموضوع [استيراد تكوينات التقارير الإلكترونية من Regulatory Configuration Services](rcs-download-configurations.md)، فاستخدم مستودع التقارير الإلكترونية المكوّن لاستيراد التكوينات التي تمت مناقشتها سابقًا لبيئتك.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-311">If you already went through the steps in the topic, [Import Electronic reporting configurations from Regulatory Configuration Services](rcs-download-configurations.md), use the configured ER repository to import configurations discussed earlier in this topic to your environment.</span></span> <span data-ttu-id="fc3a7-312">وإلا، فاتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="fc3a7-312">Otherwise, follow these steps:</span></span>

1. <span data-ttu-id="fc3a7-313">حدد الشركة **DEMF** وفي لوحة المعلومات الافتراضية، حدد **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-313">Select the **DEMF** company and on the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="fc3a7-314">حدد **تكوينات إعداد التقارير‬**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-314">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="fc3a7-315">قم باستيراد التكوينات من مركز التنزيل لـ Microsoft بالتسلسل التالي: نموذج البيانات، وتعيين النموذج، والتنسيق.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-315">Import the configurations from Microsoft Download Center in the following sequence: data model, model mapping, format.</span></span> <span data-ttu-id="fc3a7-316">أكمل الخطوات التالية لكل تكوين خاص بإعداد التقارير الإلكترونية:</span><span class="sxs-lookup"><span data-stu-id="fc3a7-316">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="fc3a7-317">حدد **تبادل**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-317">Select **Exchange.**</span></span>
    2. <span data-ttu-id="fc3a7-318">حدد **تحميل من ملف XML**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-318">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="fc3a7-319">حدد **استعراض** لتحديد تكوين التقارير الإلكترونية المطلوب بالتنسيق XML.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-319">Select **Browse** to select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="fc3a7-320">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-320">Select **OK**.</span></span>

4. <span data-ttu-id="fc3a7-321">استيراد ما تم تصديره من RCS الإصدار المكتمل 1.1.1 من التنسيق **تنسيق للتعرف على الاستدعاءات ذات معلمات (مخصص)**:</span><span class="sxs-lookup"><span data-stu-id="fc3a7-321">Import the exported from RCS completed version 1.1.1 of the **Format to learn parameterized calls (custom)** format:</span></span>

    1. <span data-ttu-id="fc3a7-322">حدد **تبادل**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-322">Select **Exchange.**</span></span>
    2. <span data-ttu-id="fc3a7-323">حدد **تحميل من ملف XML**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-323">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="fc3a7-324">حدد **استعراض** لتحديد ملف التنسيق المخزن محليًا **تنسيق للتعرف على الاستدعاءات ذات معلمات (مخصص)** بتنسيق XML.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-324">Select **Browse** to select the locally stored **Format to learn parameterized calls (custom)** file in XML format.</span></span>
    4. <span data-ttu-id="fc3a7-325">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-325">Select **OK**.</span></span>

### <a name="run-er-formats"></a><span data-ttu-id="fc3a7-326">تشغيل تنسيقات التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="fc3a7-326">Run ER formats</span></span>

1. <span data-ttu-id="fc3a7-327">في شجرة التكوين، قم بتوسيع محتوى العنصر **نموذج للتعرف على الاستدعاءات ذات معلمات‬**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-327">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="fc3a7-328">حدد **تنسيق للتعرف على الاستدعاءات ذات معلمات**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-328">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="fc3a7-329">حدد **تشغيل** في الشريط العلوي.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-329">Select **Run** on the top-most ribbon.</span></span>
4. <span data-ttu-id="fc3a7-330">احفظ المخرجات التي تم إنشاؤها محليًا.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-330">Save the locally generated output.</span></span>
5. <span data-ttu-id="fc3a7-331">حدد الصنف **تنسيق للتعرف على الاستدعاءات ذات معلمات (مخصص)**.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-331">Select the **Format to learn parameterized calls (custom)** item.</span></span>
6. <span data-ttu-id="fc3a7-332">حدد **تشغيل** في الشريط العلوي.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-332">Select **Run** on the top-most ribbon.</span></span>
7. <span data-ttu-id="fc3a7-333">احفظ المخرجات التي تم إنشاؤها محليًا.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-333">Save the generated output locally.</span></span> 
8. <span data-ttu-id="fc3a7-334">قارن بين محتويات المخرجات التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-334">Compare the contents of the generated outputs.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fc3a7-335">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="fc3a7-335">Additional resources</span></span>
[<span data-ttu-id="fc3a7-336">مصمم المعادلات في التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="fc3a7-336">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
