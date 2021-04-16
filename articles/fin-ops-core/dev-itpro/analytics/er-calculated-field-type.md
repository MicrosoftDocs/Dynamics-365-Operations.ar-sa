---
title: دعم استدعاءات ذات معلمات لمصادر بيانات التقارير الإلكترونية لنوع الحقل المحسوب‬
description: يوفر هذا الموضوع معلومات حول كيفية استخدام نوع الحقل المحسوب لمصادر بيانات التقارير الإلكترونية.
author: NickSelin
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 897133a27f9d3da2f576ce675c0949f824cde881
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749479"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a><span data-ttu-id="63dd5-103">دعم استدعاءات ذات معلمات لمصادر بيانات التقارير الإلكترونية لنوع الحقل المحسوب‬</span><span class="sxs-lookup"><span data-stu-id="63dd5-103">Support parameterized calls of ER data sources of the Calculated field type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="63dd5-104">يشرح هذا الموضوع كيفية تصميم مصدر بيانات التقارير الإلكترونية باستخدام نوع **الحقل المحسوب**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-104">This topic explains how you can design an Electronic reporting (ER) data source by using the **Calculated field** type.</span></span> <span data-ttu-id="63dd5-105">قد يحتوي مصدر البيانات هذا على تعبير التقارير الإلكترونية الذي، عند تنفيذه، يمكن التحكم به بواسطة قيم وسيطات المعلمة التي تم تكوينها في الربط الذي يستدعي مصدر البيانات هذا.</span><span class="sxs-lookup"><span data-stu-id="63dd5-105">This data source may contain an ER expression that, when executed, can be controlled by the values of the parameter arguments that are configured in a binding that calls this data source.</span></span> <span data-ttu-id="63dd5-106">ومن خلال تكوين استدعاءات ذات معلمات لمصدر البيانات هذا، يمكنك إعادة استخدام مصدر بيانات واحد في العديد من عمليات الربط، مما يقلل العدد الإجمالي لمصادر البيانات التي يجب تكوينها في تعيينات نماذج التقارير الإلكترونية أو تنسيقاتها.</span><span class="sxs-lookup"><span data-stu-id="63dd5-106">By configuring parameterized calls of such a data source, you can reuse a single data source in many bindings, which reduces the total number of data sources that must be configured in ER model mappings or ER formats.</span></span> <span data-ttu-id="63dd5-107">ويقوم أيضا بتبسيط مكون التقارير الإلكترونية الذي تم تكوينه، مما يقلل من تكاليف الصيانة وتكلفة الاستخدام من قبل العملاء الآخرين.</span><span class="sxs-lookup"><span data-stu-id="63dd5-107">It also simplifies the configured ER component, which reduces the maintenance costs and the cost of use by other consumers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="63dd5-108">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="63dd5-108">Prerequisites</span></span>
<span data-ttu-id="63dd5-109">لإكمال الأمثلة في هذا الموضوع، يجب أن يكون لديك الوصول التالي:</span><span class="sxs-lookup"><span data-stu-id="63dd5-109">To complete the examples in this topic, you must have the following access:</span></span>

- <span data-ttu-id="63dd5-110">الوصول إلى أحد هذه الأدوار:</span><span class="sxs-lookup"><span data-stu-id="63dd5-110">Access to one of these roles:</span></span>

    - <span data-ttu-id="63dd5-111">مطور إعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="63dd5-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="63dd5-112">مستشار وظيفي لإعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="63dd5-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="63dd5-113">مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="63dd5-113">System administrator</span></span>

- <span data-ttu-id="63dd5-114">يمكنك الوصول إلى Regulatory Configuration Services (RCS) التي تم تزويدها لنفس المستأجر مثل Finance and Operations، لأحد الأدوار التالية:</span><span class="sxs-lookup"><span data-stu-id="63dd5-114">Access to Regulatory Configuration Services (RCS) that have been provisioned for the same tenant as Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="63dd5-115">مطور إعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="63dd5-115">Electronic reporting developer</span></span>
    - <span data-ttu-id="63dd5-116">مستشار وظيفي لإعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="63dd5-116">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="63dd5-117">مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="63dd5-117">System administrator</span></span>

<span data-ttu-id="63dd5-118">يجب عليك أيضًا تنزيل الملفات التالية وتخزينها محليًا.</span><span class="sxs-lookup"><span data-stu-id="63dd5-118">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="63dd5-119">**المحتوى**</span><span class="sxs-lookup"><span data-stu-id="63dd5-119">**Content**</span></span>                           | <span data-ttu-id="63dd5-120">**اسم الملف**</span><span class="sxs-lookup"><span data-stu-id="63dd5-120">**File name**</span></span>                                        |
|---------------------------------------|------------------------------------------------------|
| <span data-ttu-id="63dd5-121">تكوين نموذج عينة بيانات التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="63dd5-121">Sample ER data model configuration</span></span>    | [<span data-ttu-id="63dd5-122">Model to learn parameterized calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="63dd5-122">Model to learn parameterized calls.version.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)     |
| <span data-ttu-id="63dd5-123">تكوين بيانات تعريف عينة التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="63dd5-123">Sample ER metadata configuration</span></span>      | [<span data-ttu-id="63dd5-124">Metadata to learn parameterized calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="63dd5-124">Metadata to learn parameterized calls.version.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |
| <span data-ttu-id="63dd5-125">تكوين تعيين نموذج عينة التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="63dd5-125">Sample ER model mapping configuration</span></span> | [<span data-ttu-id="63dd5-126">Mapping to learn parameterized calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="63dd5-126">Mapping to learn parameterized calls.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="63dd5-127">تكوين تنسيق عينة التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="63dd5-127">Sample ER format configuration</span></span>        | [<span data-ttu-id="63dd5-128">Format to learn parameterized calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="63dd5-128">Format to learn parameterized calls.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |

## <a name="sign-in-to-your-rcs-instance"></a><span data-ttu-id="63dd5-129">تسجيل الدخول إلى مثيل RCS</span><span class="sxs-lookup"><span data-stu-id="63dd5-129">Sign in to your RCS instance</span></span>
<span data-ttu-id="63dd5-130">في هذا المثال، سوف تنشئ تكوينًا للشركة النموذجية Litware, Inc. في RCS يجب عليك أولاً إكمال الخطوات الموجودة في الإجراء [‏‫إنشاء موفري التكوين ووضع علامة عليهم على أنهم نشيطون‬](tasks/er-configuration-provider-mark-it-active-2016-11.md):</span><span class="sxs-lookup"><span data-stu-id="63dd5-130">In this example, you will create a configuration for the sample company, Litware, Inc. First, in RCS, you must complete the steps in the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure:</span></span>

1. <span data-ttu-id="63dd5-131">في لوحة المعلومات الافتراضية، حدد **‏‫إعداد التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-131">On the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="63dd5-132">حدد **تكوينات إعداد التقارير‬**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-132">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="63dd5-133">قم باستيراد التكوينات التي تم تنزيلها إلى RCS بالتسلسل التالي: نموذج البيانات، وبيانات التعريف، وتعيين النموذج، والتنسيق.</span><span class="sxs-lookup"><span data-stu-id="63dd5-133">Import the downloaded configurations to RCS in the following sequence: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="63dd5-134">أكمل الخطوات التالية لكل تكوين خاص بإعداد التقارير الإلكترونية:</span><span class="sxs-lookup"><span data-stu-id="63dd5-134">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="63dd5-135">حدد **تبادل**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-135">Select **Exchange.**</span></span>
    2. <span data-ttu-id="63dd5-136">حدد **تحميل من ملف XML**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-136">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="63dd5-137">حدد **استعراض**، ثم حدد الملف المطلوب لتكوين التقارير الإلكترونية بالتنسيق XML.</span><span class="sxs-lookup"><span data-stu-id="63dd5-137">Select **Browse**, and then select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="63dd5-138">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-138">Select **OK.**</span></span>

## <a name="review-the-provided-er-solution"></a><span data-ttu-id="63dd5-139">مراجعه الحل المتوفر لإعداد التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="63dd5-139">Review the provided ER solution</span></span>

### <a name="review-model-mapping"></a><span data-ttu-id="63dd5-140">مراجعة تعيين النموذج</span><span class="sxs-lookup"><span data-stu-id="63dd5-140">Review model mapping</span></span>

1. <span data-ttu-id="63dd5-141">في شجرة التكوين، قم بتوسيع محتوى العنصر **نموذج للتعرف على الاستدعاءات ذات معلمات‬**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-141">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="63dd5-142">حدد **تعيين للتعرف على الاستدعاءات ذات معلمات**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-142">Select **Mapping to learn parameterized calls**.</span></span>
3. <span data-ttu-id="63dd5-143">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-143">Select **Designer**.</span></span>
4. <span data-ttu-id="63dd5-144">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-144">Select **Designer**.</span></span>  
   
    <span data-ttu-id="63dd5-145">يتم تصميم تعيين نموذج إعداد التقارير الإلكترونية هذا للقيام بما يلي:</span><span class="sxs-lookup"><span data-stu-id="63dd5-145">This ER model mapping is designed to do the following:</span></span>

    - <span data-ttu-id="63dd5-146">إحضار قائمة بأكواد الضريبة (مصدر بيانات **الضريبة**) الموجودة في الجدول **TaxTable**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-146">Fetch the list of tax codes (**Tax** data source) residing in the **TaxTable** table.</span></span>
    - <span data-ttu-id="63dd5-147">إحضار قائمة بحركات الضريبة (مصدر بيانات **الحركة**) الموجودة في الجدول **TaxTrans**:</span><span class="sxs-lookup"><span data-stu-id="63dd5-147">Fetch the list of tax transactions (**Trans** data source) residing in the **TaxTrans** table:</span></span>
    
        - <span data-ttu-id="63dd5-148">تجميع قائمة بالحركات التي تم إحضارها (مصدر بيانات **التجميع**) حسب كود الضريبة.</span><span class="sxs-lookup"><span data-stu-id="63dd5-148">Group the list of fetched transactions (**Gr** data source) by tax code.</span></span>
        - <span data-ttu-id="63dd5-149">حساب الحركات المجمعة التي تتبع القيم المجمعة حسب كود الضريبة:</span><span class="sxs-lookup"><span data-stu-id="63dd5-149">Calculate for grouped transactions following aggregated values per tax code:</span></span>

            - <span data-ttu-id="63dd5-150">مجموع قيم أساس الضريبة.</span><span class="sxs-lookup"><span data-stu-id="63dd5-150">Sum of tax base values.</span></span>
            - <span data-ttu-id="63dd5-151">مجموع قيم الضريبة.</span><span class="sxs-lookup"><span data-stu-id="63dd5-151">Sum of tax values.</span></span>
            - <span data-ttu-id="63dd5-152">الحد الأدنى لقيمة معدل الضريبة المطبق.</span><span class="sxs-lookup"><span data-stu-id="63dd5-152">Minimum value of applied tax rate.</span></span>

    <span data-ttu-id="63dd5-153">يقوم تعيين النموذج في هذا التكوين بتنفيذ نموذج البيانات الأساسي لأي من تنسيقات التقارير الإلكترونية التي تم إنشاؤها لهذا النموذج وتنفيذها في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="63dd5-153">The model mapping in this configuration implements the base data model for any of the ER formats created for this model and executed in Finance and Operations.</span></span> <span data-ttu-id="63dd5-154">نتيجة لذلك، يتم كشف محتوى مصادر بيانات **الضريبة** و **التجميع** لتنسيقات التقارير الإلكترونية مثل مصادر البيانات المجردة.</span><span class="sxs-lookup"><span data-stu-id="63dd5-154">As a result, the content of the **Tax** and **Gr** data sources is exposed for ER formats such as abstract data sources.</span></span>

    ![صفحة مصمم تعيين النموذج التي تعرض مصادر بيانات الضريبة والتجميع](media/er-calculated-field-type-01.png)

5.  <span data-ttu-id="63dd5-156">أغلق صفحة **مصمم تعيين النموذج**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-156">Close the **Model mapping designer** page.</span></span>
6.  <span data-ttu-id="63dd5-157">أغلق صفحة **تعيين النموذج**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-157">Close the **Model mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="63dd5-158">مراجعة التنسيق</span><span class="sxs-lookup"><span data-stu-id="63dd5-158">Review format</span></span>

1. <span data-ttu-id="63dd5-159">في شجرة التكوين، قم بتوسيع محتوى العنصر **نموذج للتعرف على الاستدعاءات ذات معلمات‬**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-159">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="63dd5-160">حدد **تنسيق للتعرف على الاستدعاءات ذات معلمات**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-160">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="63dd5-161">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-161">Select **Designer**.</span></span> <span data-ttu-id="63dd5-162">يتم تصميم تنسيق إعداد التقارير الإلكترونية هذا للقيام بما يلي:</span><span class="sxs-lookup"><span data-stu-id="63dd5-162">This ER format is designed to do the following:</span></span>

    - <span data-ttu-id="63dd5-163">إنشاء بيان ضريبة بتنسيق XML.</span><span class="sxs-lookup"><span data-stu-id="63dd5-163">Generate a tax statement in XML format.</span></span>
    - <span data-ttu-id="63dd5-164">تقديم المستويات التالية لفرض الضرائب في بيان الضريبة: العادي والمخفض ولا شيء.</span><span class="sxs-lookup"><span data-stu-id="63dd5-164">Present the following levels of taxation in the tax statement: regular, reduced, and none.</span></span>
    - <span data-ttu-id="63dd5-165">تقديم تفاصيل متعدد في كل مستوى فرض ضرائب، مع وجود عدد مختلف من التفاصيل في كل مستوى.</span><span class="sxs-lookup"><span data-stu-id="63dd5-165">Present multiple details at each taxation level, having a different number of details in each level.</span></span>

    ![صفحة مصمم التنسيق‬](media/er-calculated-field-type-02.png)

4. <span data-ttu-id="63dd5-167">حدد **التعيين**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-167">Select **Mapping**.</span></span>
5. <span data-ttu-id="63dd5-168">قم بتوسيع عناصر **النموذج**، و **البيانات**، و **الملخص**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-168">Expand the **Model**, **Data,** and **Summary** items.</span></span> 

    <span data-ttu-id="63dd5-169">يحتوي الحقل المحسوب **Model.Data.Summary.Level** على التعبير الذي يقوم بإرجاع كود مستوى فرض الضرائب (**العادي**، أو **المخفض**، أو **لا شيء**، أو **غير ذلك**) كقيمة نصية لأي كود ضريبة يمكن استرجاعه من مصدر البيانات **Model.Data.Summary** في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="63dd5-169">The calculated field **Model.Data.Summary.Level** contains the expression that returns the code of the taxation level (**Regular**, **Reduced**, **None,** or **Other**) as a text value for any tax code that can be retrieved from the **Model.Data.Summary** data source at run time.</span></span>

    ![صفحة مصمم تنسيق تظهر تفاصيل نموذج لنموذج بيانات لمعرفة الاستدعاءات ذات معلمات](media/er-calculated-field-type-03.png)

6. <span data-ttu-id="63dd5-171">قم بتوسيع عنصر **Model**.**Data2**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-171">Expand the **Model**.**Data2** item.</span></span>
7. <span data-ttu-id="63dd5-172">قم بتوسيع عنصر **Model**.**Data2.Summary2**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-172">Expand the **Model**.**Data2.Summary2** item.</span></span>
   
    <span data-ttu-id="63dd5-173">يتم تكوين مصدر البيانات **Model**.**Data2.Summary2** لتجميع تفاصيل حركة مصدر بيانات **Model.Data.Summary** حسب مستوى فرض الضرائب (الذي يتم إرجاعه بواسطة الحقل المحسوب **Model.Data.Summary.Level**) وحساب التجميعات.</span><span class="sxs-lookup"><span data-stu-id="63dd5-173">The **Model**.**Data2.Summary2** data source is configured to group the **Model.Data.Summary** data source transaction details by taxation level (returned by the **Model.Data.Summary.Level** calculated field) and compute the aggregations.</span></span>

    ![صفحه مصمم تنسيق تُظهر تفاصيل مصدر بيانات Model.Data2.Summary2](media/er-calculated-field-type-04.png)

8. <span data-ttu-id="63dd5-175">راجع الحقول المحسوبة **Model**.**Data2.Level1**، و **Model**.**Data2.Level2**، و **Model**.**Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-175">Review the calculated fields **Model**.**Data2.Level1**, **Model**.**Data2.Level2**, and **Model**.**Data2.Level3.**</span></span> <span data-ttu-id="63dd5-176">يتم استخدام هذه الحقول المحسوبة لتصفية قائمة سجلات **Model**.**Data2.Summary2** وإرجاع السجلات التي تمثل مستوى فرض ضرائب معين فقط.</span><span class="sxs-lookup"><span data-stu-id="63dd5-176">These calculated fields are used to filter the **Model**.**Data2.Summary2** records list and return only records that represent a particular taxation level.</span></span>
9. <span data-ttu-id="63dd5-177">أغلق صفحة **مصمم المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-177">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="63dd5-178">إنشاء تنسيق مشتق</span><span class="sxs-lookup"><span data-stu-id="63dd5-178">Create a derived format</span></span>
<span data-ttu-id="63dd5-179">يمكنك تحسين التنسيق المتوفر عن طريق إضافة حقل محسوب واحد لتصفية مستوى فرض الضرائب المطلوب بدلاً من استخدام الحقول الثلاثة الموجودة: **Model**.**Data2.Level1**، و **Model**.**Data2.Level2**، و **Model**.**Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-179">You can improve the provided format by adding one calculated field to filter the required taxation level instead of using the existing three fields: **Model**.**Data2.Level1**, **Model**.**Data2.Level2,** and **Model**.**Data2.Level3**.</span></span> <span data-ttu-id="63dd5-180">يمكن تحديد مستوى فرض الضرائب المطلوب في الموقع الذي سيتم فيه استدعاء هذا الحقل الجديد المحسوب.</span><span class="sxs-lookup"><span data-stu-id="63dd5-180">The required taxation level can be specified in the location where this new calculated field will be called.</span></span>

1. <span data-ttu-id="63dd5-181">في شجرة التكوين، قم بتوسيع محتوى العنصر **نموذج للتعرف على الاستدعاءات ذات معلمات‬**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-181">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="63dd5-182">حدد **تنسيق للتعرف على الاستدعاءات ذات معلمات**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-182">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="63dd5-183">حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-183">Select **Create configuration**.</span></span>
4. <span data-ttu-id="63dd5-184">حدد **اشتقاق من الاسم: تنسيق للتعرف على الاستدعاءات ذات معلمات، Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-184">Select **Derive from Name: Format to learn parameterized calls, Microsoft**.</span></span>
5. <span data-ttu-id="63dd5-185">في حقل **الاسم**، أدخل **تنسيق للتعرف على الاستدعاءات ذات معلمات (مخصص)**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-185">In the **Name** field, enter **Format to learn parameterized calls (custom)**.</span></span>
6. <span data-ttu-id="63dd5-186">حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-186">Select **Create configuration.**</span></span>

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a><span data-ttu-id="63dd5-187">تكوين حقل محسوب ذي معلمات يرجع قائمة سجلات</span><span class="sxs-lookup"><span data-stu-id="63dd5-187">Configure a parameterized calculated field that returns a list of records</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="63dd5-188">بدء إضافة حقل محسوب جديد</span><span class="sxs-lookup"><span data-stu-id="63dd5-188">Start adding a new calculated field</span></span>

1. <span data-ttu-id="63dd5-189">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-189">Select **Designer**.</span></span>
2. <span data-ttu-id="63dd5-190">حدد **توسيع/طي** لتوسيع كافة عناصر التنسيق.</span><span class="sxs-lookup"><span data-stu-id="63dd5-190">Select **Expand/collapse** to expand all format items.</span></span>
3. <span data-ttu-id="63dd5-191">حدد **التعيين**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-191">Select **Mapping**.</span></span>
4. <span data-ttu-id="63dd5-192">قم بتوسيع عنصر **النموذج**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-192">Expand the **Model** item.</span></span>
5. <span data-ttu-id="63dd5-193">حدد عنصر **Model.Data2**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-193">Select the **Model.Data2** item.</span></span>
6. <span data-ttu-id="63dd5-194">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-194">Select **Add**.</span></span>
7. <span data-ttu-id="63dd5-195">حدد **الوظائف\\حقل محسوب**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-195">Select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="63dd5-196">في حقل **الاسم**، أدخل **المستويات**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-196">In the **Name** field, enter **Levels**.</span></span>
9. <span data-ttu-id="63dd5-197">حدد **تحرير المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-197">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="63dd5-198">تحديد معلمة لإضافة حقل محسوب</span><span class="sxs-lookup"><span data-stu-id="63dd5-198">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="63dd5-199">حدد **معلمات**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-199">Select **Parameters**.</span></span>
2. <span data-ttu-id="63dd5-200">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-200">Select **New**.</span></span>
3. <span data-ttu-id="63dd5-201">في حقل **الاسم**، أدخل **مستوى فرض الضرائب**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-201">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="63dd5-202">في حقل **النوع**، حدد **سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-202">In the **Type** field, select **String**.</span></span>

    <span data-ttu-id="63dd5-203">يمكن استخدام أنواع البيانات الأولية فقط لتحديد نوع وسيطة المعلمة.</span><span class="sxs-lookup"><span data-stu-id="63dd5-203">Only primitive data types can be used to specify the type of the parameter’s argument.</span></span> <span data-ttu-id="63dd5-204">ولهذا لا يمكن استخدام الأنواع **قائمة سجلات**، و **سجل**، و **التعداد** لهذا الغرض.</span><span class="sxs-lookup"><span data-stu-id="63dd5-204">Therefore, **Record list**, **Record**, and **Enum** types cannot be used for this purpose.</span></span>

    <span data-ttu-id="63dd5-205">الحد الأقصى لعدد المعلمات التي يمكن تحديدها لحقل محسوب واحد هو 8.</span><span class="sxs-lookup"><span data-stu-id="63dd5-205">The maximum number of parameters that can be specified for a single calculated field is 8.</span></span>

    ![قائمة مصادر بيانات المعلمات](media/er-calculated-field-type-05.png)

5. <span data-ttu-id="63dd5-207">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-207">Select **OK**.</span></span>

<span data-ttu-id="63dd5-208">بإضافة هذه المعلمة، فأنت تحدد الشرط الذي يجب توفره لاستدعاء هذا الحقل المحسوب.</span><span class="sxs-lookup"><span data-stu-id="63dd5-208">By adding this parameter, you specify the condition that must be in place to call this calculated field.</span></span> <span data-ttu-id="63dd5-209">عند استدعاء هذا الحقل المحسوب، يجب تحديد وسيطة معلمة **مستوى فرض الضرائب** كقيمة بتنسيق **سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-209">When you call this calculated field, you need to specify the argument of the **Taxation Level** parameter as a value with **String** format.</span></span>

   <span data-ttu-id="63dd5-210">تأكد من تعريف المعلمات فقط للحقول المحسوبة الموجودة في حاوية (إما **قائمة السجلات**، أو **السجل**، أو **الحاوية**).</span><span class="sxs-lookup"><span data-stu-id="63dd5-210">Make sure that you define parameters only for those calculated fields that reside in a container (either **Record list**, **Record**, or **Container**).</span></span>

   <span data-ttu-id="63dd5-211">تتوفر المعلمة المكونة في قائمة مصادر البيانات لهذا الحقل المحسوب.</span><span class="sxs-lookup"><span data-stu-id="63dd5-211">The configured parameter is available in the list of data sources for this calculated field.</span></span> <span data-ttu-id="63dd5-212">يمكنك إضافة المعلمة إلى التعبير المكون عن طريق تحديد **إضافة مصدر بيانات**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-212">You can add the parameter to the configured expression by selecting **Add data source**.</span></span>

   ![حقول مصادر البيانات](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="63dd5-214">تحديد تعبير لإضافة حقل محسوب</span><span class="sxs-lookup"><span data-stu-id="63dd5-214">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="63dd5-215">في حقل **المعادلة**، أدخل:</span><span class="sxs-lookup"><span data-stu-id="63dd5-215">In the **Formula** field, enter:</span></span> 

    <span data-ttu-id="63dd5-216">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span><span class="sxs-lookup"><span data-stu-id="63dd5-216">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span></span>
    
2. <span data-ttu-id="63dd5-217">حدد معلمة **مستوى فرض الضرائب** في قائمة مصادر البيانات.</span><span class="sxs-lookup"><span data-stu-id="63dd5-217">Select the **Taxation Level** parameter in the list of data sources.</span></span>
3. <span data-ttu-id="63dd5-218">حدد **إضافة مصدر البيانات**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-218">Select **Add data source**.</span></span>
4. <span data-ttu-id="63dd5-219">في حقل **المعادلة**، أنجز التعبير كما يلي:</span><span class="sxs-lookup"><span data-stu-id="63dd5-219">In the **Formula** field, finalize the expression as:</span></span>  

    <span data-ttu-id="63dd5-220">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span><span class="sxs-lookup"><span data-stu-id="63dd5-220">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span></span>

5. <span data-ttu-id="63dd5-221">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-221">Select **Save**.</span></span>

    ![معلومات حقل مصدر البيانات](media/er-calculated-field-type-07.png)

6. <span data-ttu-id="63dd5-223">أغلق صفحة **مصمم المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-223">Close the **Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="63dd5-224">إنهاء إضافة حقل محسوب جديد</span><span class="sxs-lookup"><span data-stu-id="63dd5-224">Finish adding a new calculated field</span></span>

- <span data-ttu-id="63dd5-225">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-225">Select **OK**.</span></span>

<span data-ttu-id="63dd5-226">في صفحة **مصمم المعادلة**، يحتاج حقل **المستويات** المحسوب المكوّن ذو معلمات إلى وسيطة **سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-226">On the **Format designer** page, the configured parameterized calculated field **Levels** requires a **String** argument.</span></span>

![قائمة موسعة بمستويات الحقول المحسوبة](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements&quot;></a><span data-ttu-id=&quot;63dd5-228&quot;>استخدام الحقل المحسوب المكون لربط عناصر التنسيق</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;63dd5-228&quot;>Use the configured calculated field for binding format elements</span></span>

1. <span data-ttu-id=&quot;63dd5-229&quot;>حدد **Model.Data2.Levels** لتحديد الحقل المحسوب الذي تم تكوينه.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;63dd5-229&quot;>Select **Model.Data2.Levels** to select the configured calculated field.</span></span>
2. <span data-ttu-id=&quot;63dd5-230&quot;>حدد عنصر التنسيق **Statement.Taxation.Regular**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;63dd5-230&quot;>Select the **Statement.Taxation.Regular** format element.</span></span>
3. <span data-ttu-id=&quot;63dd5-231&quot;>حدد **ربط**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;63dd5-231&quot;>Select **Bind**.</span></span>
4. <span data-ttu-id=&quot;63dd5-232&quot;>حدد **نعم** لتأكيد استبدال مصدر البيانات المستخدم حاليًا، **المستوى1**، بمصدر البيانات الجديد، **المستويات**، في كافة عناصر التنسيق المتداخلة لعنصر التنسيق المحدد.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;63dd5-232&quot;>Select **Yes** to confirm the replacement of the currently used data source, **Level1**, by the new data source, **Levels**, in all nested format elements of the selected format element.</span></span>

    <span data-ttu-id=&quot;63dd5-233&quot;>تم إنشاء الربط المطبق كاستدعاء للحقل المحسوب ذي معلمات.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;63dd5-233&quot;>Applied binding has been built as a call of the parameterized calculated field.</span></span> <span data-ttu-id=&quot;63dd5-234&quot;>بشكل افتراضي، يتم استخدام اسم عنصر التنسيق المنضم كوسيطة للحقل المحسوب ذي معلمات تحت الشروط التالية:</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;63dd5-234&quot;>By default, the name of the bound format element is used as an argument for parameterized calculated field under the following conditions:</span></span>

      - <span data-ttu-id=&quot;63dd5-235&quot;>يتم تكوين الحقل المحسوب لاستخدام معلمة واحدة.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;63dd5-235&quot;>The calculated field is configured to use a single parameter.</span></span>
      - <span data-ttu-id=&quot;63dd5-236&quot;>يتم تعريف نوع بيانات هذه المعلمة **كسلسلة**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;63dd5-236&quot;>The data type of this parameter is defined as **String**.</span></span>

    <span data-ttu-id=&quot;63dd5-237&quot;>عندما يكون اسم عنصر التنسيق المنضم فارغًا، يتم استخدام اسم مصدر البيانات الخاص بهذا العنصر في الربط المطبق.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;63dd5-237&quot;>When the name of the bound format element is blank, the data source name of this element is used in applied binding.</span></span>

5. <span data-ttu-id=&quot;63dd5-238&quot;>حدد عنصر التنسيق **Statement.Taxation.Reduced**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;63dd5-238&quot;>Select the **Statement.Taxation.Reduced** format element.</span></span>
6. <span data-ttu-id=&quot;63dd5-239&quot;>حدد **ربط**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;63dd5-239&quot;>Select **Bind**.</span></span>
7. <span data-ttu-id=&quot;63dd5-240&quot;>حدد **نعم** لتأكيد استبدال مصدر البيانات المستخدم حاليًا، **المستوى2**، بمصدر البيانات الجديد، **المستويات**، في كافة عناصر التنسيق المتداخلة لعنصر التنسيق المحدد.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;63dd5-240&quot;>Select **Yes** to confirm the replacement of the currently used data source, **Level2**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>
8. <span data-ttu-id=&quot;63dd5-241&quot;>حدد عنصر التنسيق **Statement.Taxation.None**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;63dd5-241&quot;>Select the **Statement.Taxation.None** format element.</span></span>
9. <span data-ttu-id=&quot;63dd5-242&quot;>حدد **ربط**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;63dd5-242&quot;>Select **Bind**.</span></span>
10. <span data-ttu-id=&quot;63dd5-243&quot;>حدد **نعم** لتأكيد استبدال مصدر البيانات المستخدم حاليًا، **المستوى3**، بمصدر البيانات الجديد، **المستويات**، في كافة عناصر التنسيق المتداخلة لعنصر التنسيق المحدد.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;63dd5-243&quot;>Select **Yes** to confirm the replacement of the currently used data source, **Level3**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>

   <span data-ttu-id=&quot;63dd5-244&quot;>عند تعيين وسيطة الحقل المحسوب ذي المعلمات لعنصر XML الذي يمثل مستوى فرض الضرائب (على سبيل المثال **‎Model.Data2.Levels(&quot;Reduced")** كقيمة نصية)، لا تحتاج إلى القيام بنفس الإجراءات لسمات XML المتداخلة — سترث الارتباطات الخاصة بها تلقائيًا قيمة الوسيطة المعرفة في المستوى الأصل (**Model.Data2.Levels.aggregated.Base**، وليس **Model.Data2.Levels("Reduced").aggregated.Base**).</span><span class="sxs-lookup"><span data-stu-id="63dd5-244">When you specify the argument of the parameterized calculated field for the XML element representing taxation level (for example, **Model.Data2.Levels("Reduced")** as a text value), you don’t need to do the same for nested XML attributes—their bindings will automatically inherit the value of the argument defined on the parent level (**Model.Data2.Levels.aggregated.Base**, not **Model.Data2.Levels("Reduced").aggregated.Base**).</span></span>

<span data-ttu-id="63dd5-245">الاستدعاءات المتكررة لأي حقل محسوب ذي معلمات غير معتمدة.</span><span class="sxs-lookup"><span data-stu-id="63dd5-245">Recurrent calls of any parameterized calculated field are not supported.</span></span>

<span data-ttu-id="63dd5-246">يمكنك تحديد **تحرير المعادلة**، وتغيير الوسيطة المطبقة بشكل افتراضي للحقل المحسوب ذي المعلمات في الربط المحدد.</span><span class="sxs-lookup"><span data-stu-id="63dd5-246">You can select **Edit formula**, and change the applied-by-default argument of the parameterized calculated field in the selected binding.</span></span> <span data-ttu-id="63dd5-247">إذا كانت هذه الوسيطة مفقودة، فقد تتسبب في حدوث أخطاء في وقت التشغيل — يتم إعلام المستخدمين بمثل هذا الموقف عند التحقق من صحة التنسيق الحالي.</span><span class="sxs-lookup"><span data-stu-id="63dd5-247">If this argument is missing, it can cause errors at run time — users are informed about such a situation when the current format is validated.</span></span>

![الإعلام عن تحذير التحقق من الصحة](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a><span data-ttu-id="63dd5-249">تكوين حقل محسوب ذي معلمات لإرجاع سجل</span><span class="sxs-lookup"><span data-stu-id="63dd5-249">Configure a parameterized calculated field to return a record</span></span>
<span data-ttu-id="63dd5-250">عندما يقوم حقل محسوب ذو معلمات بإرجاع سجل، تحتاج إلى دعم ربط الحقول الفردية لهذا السجل بعناصر التنسيق.</span><span class="sxs-lookup"><span data-stu-id="63dd5-250">When a parameterized calculated field returns a record, you need to support binding of individual fields of this record to format elements.</span></span> <span data-ttu-id="63dd5-251">في مثل هذه الحالات لن يكون هناك ربط أصلي يحتوي على قيمة وسيطة لاستدعاء حقل محسوب ذي معلمات — يجب تعريف هذه القيمة في ربط حقل سجل واحد.</span><span class="sxs-lookup"><span data-stu-id="63dd5-251">In such cases there will be no parent binding that contains the value of an argument to call a parameterized calculated field — this value must be defined in the binding of a single record’s field.</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="63dd5-252">بدء إضافة حقل محسوب جديد</span><span class="sxs-lookup"><span data-stu-id="63dd5-252">Start adding a new calculated field</span></span>

1. <span data-ttu-id="63dd5-253">حدد عنصر **Model.Data2**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-253">Select the **Model.Data2** item.</span></span>
2. <span data-ttu-id="63dd5-254">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-254">Select **Add**.</span></span>
3. <span data-ttu-id="63dd5-255">حدد **الوظائف\\حقل محسوب**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-255">Select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="63dd5-256">في حقل **الاسم**، أدخل **‏‫LevelRecord‬**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-256">In the **Name** field, enter **LevelRecord**.</span></span>
5. <span data-ttu-id="63dd5-257">حدد **تحرير المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-257">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="63dd5-258">تحديد معلمة لإضافة حقل محسوب</span><span class="sxs-lookup"><span data-stu-id="63dd5-258">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="63dd5-259">حدد **معلمات**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-259">Select **Parameters**.</span></span>
2. <span data-ttu-id="63dd5-260">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-260">Select **New**.</span></span>
3. <span data-ttu-id="63dd5-261">في حقل **الاسم**، أدخل **مستوى فرض الضرائب**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-261">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="63dd5-262">في حقل **النوع**، حدد **سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-262">In the **Type** field, select **String**.</span></span>
5. <span data-ttu-id="63dd5-263">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-263">Select **OK**.</span></span>

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="63dd5-264">تحديد تعبير لإضافة حقل محسوب</span><span class="sxs-lookup"><span data-stu-id="63dd5-264">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="63dd5-265">في حقل **المعادلة**، أدخل ما يلي:</span><span class="sxs-lookup"><span data-stu-id="63dd5-265">In the **Formula** field, enter the following:</span></span>  
    
    <span data-ttu-id="63dd5-266">**FIRSTORNULL(\@.Levels(**</span><span class="sxs-lookup"><span data-stu-id="63dd5-266">**FIRSTORNULL(\@.Levels(**</span></span>

2. <span data-ttu-id="63dd5-267">حدد المعلمة **مستوى فرض الضرائب**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-267">Select the **Taxation Level** parameter.</span></span>
3. <span data-ttu-id="63dd5-268">حدد **إضافة مصدر البيانات**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-268">Select **Add data source**.</span></span>
4. <span data-ttu-id="63dd5-269">في حقل **المعادلة**، قم بإلحاق **'مستوى فرض الضرائب'))** بما أدخلته في الخطوة 1 لإنهاء التعبير إلى:</span><span class="sxs-lookup"><span data-stu-id="63dd5-269">In the **Formula** field, append **'Taxation Level'))** to what you entered in Step 1 to finalize the expression to:</span></span>  
    
    <span data-ttu-id="63dd5-270">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span><span class="sxs-lookup"><span data-stu-id="63dd5-270">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span></span>

5. <span data-ttu-id="63dd5-271">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-271">Select **Save**.</span></span>
6. <span data-ttu-id="63dd5-272">أغلق صفحة **مصمم المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-272">Close **the Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="63dd5-273">إنهاء إضافة حقل محسوب جديد</span><span class="sxs-lookup"><span data-stu-id="63dd5-273">Finish adding a new calculated field</span></span>

-   <span data-ttu-id="63dd5-274">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-274">Select **OK**.</span></span>

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a><span data-ttu-id="63dd5-275">استخدام الحقل المحسوب المكون لربط عناصر التنسيق</span><span class="sxs-lookup"><span data-stu-id="63dd5-275">Use the configured calculated field to bind format elements</span></span>

1. <span data-ttu-id="63dd5-276">قم بتوسيع **Model.Data2.LevelRecord** لتحديد الحقل المحسوب الذي تم تكوينه.</span><span class="sxs-lookup"><span data-stu-id="63dd5-276">Expand **Model.Data2.LevelRecord** to select the configured calculated field.</span></span>
2. <span data-ttu-id="63dd5-277">قم بتوسيع الحاوية **Model.Data2.LevelRecord.aggregated** للحقل المحسوب الذي تم تكوينه.</span><span class="sxs-lookup"><span data-stu-id="63dd5-277">Expand the **Model.Data2.LevelRecord.aggregated** container of the configured calculated field.</span></span>
3. <span data-ttu-id="63dd5-278">حدد الحقل **Model.Data2.LevelRecord.aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-278">Select the **Model.Data2.LevelRecord.aggregated.Base** field.</span></span>
4. <span data-ttu-id="63dd5-279">حدد عنصر التنسيق **Statement.Taxation.None**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-279">Select the **Statement.Taxation.None** format element.</span></span>
5. <span data-ttu-id="63dd5-280">حدد **إلغاء الربط**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-280">Select **Unbind**.</span></span>
6. <span data-ttu-id="63dd5-281">حدد عنصر التنسيق **Statement.Taxation.None.Base**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-281">Select the **Statement.Taxation.None.Base** format element.</span></span>
7. <span data-ttu-id="63dd5-282">حدد **ربط**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-282">Select **Bind**.</span></span>
8. <span data-ttu-id="63dd5-283">حدد **تحرير المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-283">Select **Edit formula**.</span></span>
9. <span data-ttu-id="63dd5-284">قم بتغيير التعبير إلى **Model.Data2.LevelRecord("None").aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-284">Change the expression to **Model.Data2.LevelRecord("None").aggregated.Base**.</span></span>

![التعبير المحدّث](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a><span data-ttu-id="63dd5-286">إزالة الحقول المحسوبة غير المستخدمة</span><span class="sxs-lookup"><span data-stu-id="63dd5-286">Remove calculated fields that are not used</span></span>

1. <span data-ttu-id="63dd5-287">حدد **Model.Data2.Level1**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-287">Select **Model.Data2.Level1**.</span></span>
2. <span data-ttu-id="63dd5-288">حدد **حذف**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-288">Select **Delete**.</span></span>
3. <span data-ttu-id="63dd5-289">حدد **Model.Data2.Level2**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-289">Select **Model.Data2.Level2**.</span></span>
4. <span data-ttu-id="63dd5-290">حدد **حذف**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-290">Select **Delete**.</span></span>
5. <span data-ttu-id="63dd5-291">حدد **Model.Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-291">Select **Model.Data2.Level3**.</span></span>
6. <span data-ttu-id="63dd5-292">حدد **حذف**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-292">Select **Delete**.</span></span>
7. <span data-ttu-id="63dd5-293">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-293">Select **Save**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="63dd5-294">لقد قمت بإعادة استخدام نفس الحقل المحسوب **Model.Data2.Levels** عدة مرات في روابط التنسيق.</span><span class="sxs-lookup"><span data-stu-id="63dd5-294">You reused the same calculated field **Model.Data2.Levels** several times in format bindings.</span></span> <span data-ttu-id="63dd5-295">إن استخدام حقل محسوب واحد والاحتفاظ به أسهل بكثير من تنفيذ ذلك لعدة حقول متشابهة.</span><span class="sxs-lookup"><span data-stu-id="63dd5-295">It is much easier to use and maintain a single calculated field instead of doing this for multiple similar fields.</span></span>

8. <span data-ttu-id="63dd5-296">أغلق صفحة **مصمم المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-296">Close the **Format designer** page.</span></span>

## <a name="complete-adjusted-version-of-a-derived-format"></a><span data-ttu-id="63dd5-297">إكمال الإصدار المعدل لتنسيق مشتق</span><span class="sxs-lookup"><span data-stu-id="63dd5-297">Complete adjusted version of a derived format</span></span>

1. <span data-ttu-id="63dd5-298">في علامة التبويب السريعة **الإصدارات**، حدد **تغيير الحالة**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-298">In the **Versions** FastTab, select **Change status**.</span></span>
2. <span data-ttu-id="63dd5-299">حدد **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-299">Select **Complete**.</span></span>

## <a name="export-completed-version-of-a-derived-format"></a><span data-ttu-id="63dd5-300">تصدير الإصدار المكتمل لتنسيق مشتق</span><span class="sxs-lookup"><span data-stu-id="63dd5-300">Export completed version of a derived format</span></span>

1. <span data-ttu-id="63dd5-301">حدد التنسيق **تنسيق للتعرف على الاستدعاءات ذات معلمات (مخصص)** في شجره التكوينات.</span><span class="sxs-lookup"><span data-stu-id="63dd5-301">Select **Format to learn parameterized calls (custom)** format in the configurations tree.</span></span>
2. <span data-ttu-id="63dd5-302">في علامة التبويب السريعة **الإصدارات**، حدد الإصدار المكتمل 1.1.1.</span><span class="sxs-lookup"><span data-stu-id="63dd5-302">In the **Versions** FastTab, select the completed version 1.1.1.</span></span>
3. <span data-ttu-id="63dd5-303">حدد **تبادل**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-303">Select **Exchange**.</span></span>
4. <span data-ttu-id="63dd5-304">حدد **تصدير كملف XML**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-304">Select **Export as XML file**.</span></span>
5. <span data-ttu-id="63dd5-305">قم بتخزين التكوين الذي تم تنزيله محليًا، بتنسيق XML.</span><span class="sxs-lookup"><span data-stu-id="63dd5-305">Store the downloaded configuration locally, in XML format.</span></span>

## <a name="test-er-formats"></a><span data-ttu-id="63dd5-306">اختبار تنسيقات التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="63dd5-306">Test ER formats</span></span> 
<span data-ttu-id="63dd5-307">يمكنك تشغيل تنسيقات التقارير الإلكترونية الأولية والمحسنة للتأكد من أن الحقول المحسوبة ذات معلمات والتي تم تكوينها تعمل بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="63dd5-307">You can run the initial and improved ER formats to make sure that configured parameterized calculated fields work properly.</span></span>

### <a name="import-er-configurations"></a><span data-ttu-id="63dd5-308">استيراد تكوينات التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="63dd5-308">Import ER configurations</span></span>
<span data-ttu-id="63dd5-309">يمكنك استيراد التكوينات التي تمت مراجعتها من RCS باستخدام مستودع التقارير الإلكترونية الخاص بالنوع **RCS**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-309">You can import reviewed configurations from RCS by using the ER repository of the **RCS** type.</span></span> <span data-ttu-id="63dd5-310">إذا كنت قد قمت بالفعل بالخطوات المذكورة في الموضوع [استيراد تكوينات التقارير الإلكترونية (ER) من Regulatory Configuration Services (RCS)](rcs-download-configurations.md)، فاستخدم مستودع التقارير الإلكترونية المكوّن لاستيراد التكوينات التي تمت مناقشتها سابقًا لبيئتك.</span><span class="sxs-lookup"><span data-stu-id="63dd5-310">If you already went through the steps in the topic, [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](rcs-download-configurations.md), use the configured ER repository to import configurations discussed earlier in this topic to your environment.</span></span> <span data-ttu-id="63dd5-311">وإلا، فاتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="63dd5-311">Otherwise, follow these steps:</span></span>

1. <span data-ttu-id="63dd5-312">حدد الشركة **DEMF** وفي لوحة المعلومات الافتراضية، حدد **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-312">Select the **DEMF** company and on the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="63dd5-313">حدد **تكوينات إعداد التقارير‬**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-313">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="63dd5-314">قم باستيراد التكوينات من مركز التنزيل لـ Microsoft بالتسلسل التالي: نموذج البيانات، وتعيين النموذج، والتنسيق.</span><span class="sxs-lookup"><span data-stu-id="63dd5-314">Import the configurations from Microsoft Download Center in the following sequence: data model, model mapping, format.</span></span> <span data-ttu-id="63dd5-315">أكمل الخطوات التالية لكل تكوين خاص بإعداد التقارير الإلكترونية:</span><span class="sxs-lookup"><span data-stu-id="63dd5-315">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="63dd5-316">حدد **تبادل**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-316">Select **Exchange.**</span></span>
    2. <span data-ttu-id="63dd5-317">حدد **تحميل من ملف XML**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-317">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="63dd5-318">حدد **استعراض** لتحديد تكوين التقارير الإلكترونية المطلوب بالتنسيق XML.</span><span class="sxs-lookup"><span data-stu-id="63dd5-318">Select **Browse** to select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="63dd5-319">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-319">Select **OK**.</span></span>

4. <span data-ttu-id="63dd5-320">استيراد ما تم تصديره من RCS الإصدار المكتمل 1.1.1 من التنسيق **تنسيق للتعرف على الاستدعاءات ذات معلمات (مخصص)**:</span><span class="sxs-lookup"><span data-stu-id="63dd5-320">Import the exported from RCS completed version 1.1.1 of the **Format to learn parameterized calls (custom)** format:</span></span>

    1. <span data-ttu-id="63dd5-321">حدد **تبادل**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-321">Select **Exchange.**</span></span>
    2. <span data-ttu-id="63dd5-322">حدد **تحميل من ملف XML**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-322">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="63dd5-323">حدد **استعراض** لتحديد ملف التنسيق المخزن محليًا **تنسيق للتعرف على الاستدعاءات ذات معلمات (مخصص)** بتنسيق XML.</span><span class="sxs-lookup"><span data-stu-id="63dd5-323">Select **Browse** to select the locally stored **Format to learn parameterized calls (custom)** file in XML format.</span></span>
    4. <span data-ttu-id="63dd5-324">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-324">Select **OK**.</span></span>

### <a name="run-er-formats"></a><span data-ttu-id="63dd5-325">تشغيل تنسيقات التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="63dd5-325">Run ER formats</span></span>

1. <span data-ttu-id="63dd5-326">في شجرة التكوين، قم بتوسيع محتوى العنصر **نموذج للتعرف على الاستدعاءات ذات معلمات‬**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-326">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="63dd5-327">حدد **تنسيق للتعرف على الاستدعاءات ذات معلمات**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-327">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="63dd5-328">حدد **تشغيل** في الشريط العلوي.</span><span class="sxs-lookup"><span data-stu-id="63dd5-328">Select **Run** on the top-most ribbon.</span></span>
4. <span data-ttu-id="63dd5-329">احفظ المخرجات التي تم إنشاؤها محليًا.</span><span class="sxs-lookup"><span data-stu-id="63dd5-329">Save the locally generated output.</span></span>
5. <span data-ttu-id="63dd5-330">حدد الصنف **تنسيق للتعرف على الاستدعاءات ذات معلمات (مخصص)**.</span><span class="sxs-lookup"><span data-stu-id="63dd5-330">Select the **Format to learn parameterized calls (custom)** item.</span></span>
6. <span data-ttu-id="63dd5-331">حدد **تشغيل** في الشريط العلوي.</span><span class="sxs-lookup"><span data-stu-id="63dd5-331">Select **Run** on the top-most ribbon.</span></span>
7. <span data-ttu-id="63dd5-332">احفظ المخرجات التي تم إنشاؤها محليًا.</span><span class="sxs-lookup"><span data-stu-id="63dd5-332">Save the generated output locally.</span></span> 
8. <span data-ttu-id="63dd5-333">قارن بين محتويات المخرجات التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="63dd5-333">Compare the contents of the generated outputs.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="63dd5-334">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="63dd5-334">Additional resources</span></span>

- [<span data-ttu-id="63dd5-335">مصمم المعادلات في التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="63dd5-335">Formula designer in Electronic reporting (ER)</span></span>](general-electronic-reporting-formula-designer.md)
- [<span data-ttu-id="63dd5-336">تحسين أداء حلول التقارير الإلكتروني عن طريق إضافة مصادر بيانات الحقول المحسوبة ذات معلمات</span><span class="sxs-lookup"><span data-stu-id="63dd5-336">Improve performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>](er-calculated-field-ds-performance.md)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]