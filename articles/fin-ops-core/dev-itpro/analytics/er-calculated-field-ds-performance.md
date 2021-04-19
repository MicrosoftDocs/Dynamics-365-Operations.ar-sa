---
title: تحسين أداء حلول التقارير الإلكترونية‬ عن طريق إضافة مصادر بيانات الحقول المحسوبة ذات معلمات
description: يشرح هذا الموضوع كيف يمكنك المساعدة في تحسين أداء حلول التقارير الإلكترونية عن طريق إضافة مصادر بيانات الحقول المحسوبة ذات معلمات.
author: NickSelin
ms.date: 09/02/2020
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
ms.openlocfilehash: 299570d6a94b0f9e7ee7cf490d4c1aeeb86d5716
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749503"
---
# <a name="improve-the-performance-of-er-solutions-by-adding-parameterized-calculated-field-data-sources"></a><span data-ttu-id="6fe1c-103">تحسين أداء حلول التقارير الإلكترونية‬ عن طريق إضافة مصادر بيانات الحقول المحسوبة ذات معلمات</span><span class="sxs-lookup"><span data-stu-id="6fe1c-103">Improve the performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6fe1c-104">يشرح هذا الموضوع كيف يمكنك أخذ [تتبعات الأداء](trace-execution-er-troubleshoot-perf.md) لتنسيقات [التقارير الإلكترونية](general-electronic-reporting.md) التي يتم تشغيلها، ثم استخدام المعلومات من هذه التتبعات للمساعدة في تحسين الأداء عن طريق تكوين مصدر بيانات **حقل محسوب** ذي معلمات.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-104">This topic explains how you can take [performance traces](trace-execution-er-troubleshoot-perf.md) of [Electronic reporting (ER)](general-electronic-reporting.md) formats that are run, and then use the information from those traces to help improve performance by configuring a parameterized **Calculated field** data source.</span></span>

<span data-ttu-id="6fe1c-105">كجزء من عملية تصميم تكوينات التقارير الإلكترونية لإنشاء مستندات إلكترونية، يمكنك تحديد الطريقة المستخدمة لاسترداد البيانات من التطبيق وإدخالها في الإخراج الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-105">As part of the process of designing ER configurations to generate business documents, you define the method that is used to retrieve data from the application and enter it in the generated output.</span></span> <span data-ttu-id="6fe1c-106">ومن خلال تصميم مصدر بيانات تقارير إلكترونية ذي معلمات من نوع **الحقل المحسوب**، يمكنك تقليل عدد استدعاءات قاعدة البيانات، والتخفيف بشكل ملحوظ من الوقت والتكلفة في جمع تفاصيل تنفيذ تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-106">By designing a parametrized ER data source of the **Calculated field** type, you can reduce the number of database calls, and significantly reduce the time and cost that are involved in collecting the details of ER format execution.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6fe1c-107">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="6fe1c-107">Prerequisites</span></span>

- <span data-ttu-id="6fe1c-108">لإكمال الامثله الموجودة في هذا الموضوع، يجب ان يكون لديك حق الوصول إلى [الأدوار](../sysadmin/tasks/assign-users-security-roles.md)التالية:</span><span class="sxs-lookup"><span data-stu-id="6fe1c-108">To complete the examples in this topic, you must have the access to one of the following [roles](../sysadmin/tasks/assign-users-security-roles.md):</span></span>

    - <span data-ttu-id="6fe1c-109">مطور إعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="6fe1c-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="6fe1c-110">مستشار وظيفي لإعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="6fe1c-110">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="6fe1c-111">مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="6fe1c-111">System administrator</span></span>

- <span data-ttu-id="6fe1c-112">يجب تعيين الشركة علي **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-112">The company must be set to **DEMF**.</span></span>
- <span data-ttu-id="6fe1c-113">اتبع الخطوات الموجودة في [الملحق 1](#appendix1) لهذا الموضوع لتنزيل مكونات عينة حل التقارير الإلكترونية من Microsoft المطلوبة لإكمال الأمثلة في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-113">Follow the steps in [Appendix 1](#appendix1) of this topic to download the components of the sample Microsoft ER solution that is required to complete the examples in this topic.</span></span>
- <span data-ttu-id="6fe1c-114">اتبع الخطوات الموجودة في [الملحق 2](#appendix2) لهذا الموضوع لتكوين الحد الأدنى لمجموعة معلمات التقارير الإلكترونية المطلوبة لاستخدام إطار عمل التقارير الإلكترونية للمساعدة في تحسين أداء عينة حل التقارير الإلكترونية من Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-114">Follow the steps in [Appendix 2](#appendix2) of this topic to configure the minimal set of ER parameters that is required to use the ER framework to help improve the performance of the sample Microsoft ER solution.</span></span>

## <a name="import-the-sample-er-solution"></a><span data-ttu-id="6fe1c-115">استيراد عينة حل التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="6fe1c-115">Import the sample ER solution</span></span>

<span data-ttu-id="6fe1c-116">افترض انه يتعين عليك تصميم حل للتقارير الإلكترونية لإنشاء تقرير جديد يُظهر حركات المورّد.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-116">Imagine that you must design an ER solution to generate a new report that shows vendor transactions.</span></span> <span data-ttu-id="6fe1c-117">في الوقت الحالي، يمكنك العثور علي حركات مورّد محدد في صفحة **حركات المورّدين‬** (انتقل إلى **الحسابات الدائنة** \> **المورّدون** \> **جميع المورّدين**، حدد مورّدًا ، ثم على جزء الإجراءات، على علامة تبويب **المورّد** في مجموعة **الحركات**، حدد **الحركات**).</span><span class="sxs-lookup"><span data-stu-id="6fe1c-117">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable** \> **Vendors** \> **All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="6fe1c-118">ومع ذلك، تريد أن تضع معًا جميع حركات المورّدين في مستند إلكتروني واحد بتنسيق XML.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-118">However, you want to have all vendor transactions together in one electronic document in XML format.</span></span> <span data-ttu-id="6fe1c-119">سيتألف هذا الحل من العديد من تكوينات التقارير الإلكترونية التي تحتوي على مكونات نموذج البيانات والتعيين ومكونات التنسيق المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-119">This solution will consist of several ER configurations that contain the required data model, model mapping, and format components.</span></span>

<span data-ttu-id="6fe1c-120">الخطوة الأولى هي استيراد عينة حل التقارير الإلكترونية لإنشاء تقرير لحركات المورّدين.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-120">The first step is to import the sample ER solution to generate a vendor transactions report.</span></span>

1. <span data-ttu-id="6fe1c-121">سجل دخولك إلى مثيل Microsoft Dynamics 365 Finance الذي تم تزويده لشركتك.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-121">Sign in to the instance of Microsoft Dynamics 365 Finance that is provisioned for your company.</span></span>
2. <span data-ttu-id="6fe1c-122">في هذا الموضوع، ستقوم بإنشاء وتعديل تكوينات لعينة الشركة **Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-122">In this topic, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="6fe1c-123">تأكد من إضافة موفر التكوين هذا إلى مثيل Finance ومن وضع علامة عليه كنشط.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-123">Make sure that this configuration provider has been added to your Finance instance and is marked as active.</span></span> <span data-ttu-id="6fe1c-124">لمزيد من المعلومات، راجع [إنشاء موفري التكوين ووضع علامة عليهم كنشطين](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="6fe1c-124">For more information, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="6fe1c-125">في مساحة عمل **إعداد التقارير الإلكترونية**، حدد الإطار المتجانب **تكوينات إعداد التقارير**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-125">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="6fe1c-126">في صفحة **التكوينات**، قم باستيراد تكوينات التقارير الإلكترونية التي قمت بتنزيلها كشرط مسبق إلى Finance، بالترتيب التالي: نموذج البيانات، وبيانات التعريف، وتعيين النموذج، والتنسيق.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-126">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into Finance, in the following order: data model, model mapping, format.</span></span> <span data-ttu-id="6fe1c-127">بالنسبة لكل تكوين، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="6fe1c-127">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="6fe1c-128">في جزء الإجراءات، حدد **التبادل** \> **تحميل من ملف XML**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-128">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
    2. <span data-ttu-id="6fe1c-129">حدد **استعراض**، وحدد الملف المناسب لتكوين التقارير الإلكترونية المطلوب بتنسيق XML.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-129">Select **Browse**, and select the appropriate file for the ER configuration in XML format.</span></span>
    3. <span data-ttu-id="6fe1c-130">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-130">Select **OK**.</span></span>

![التكوينات المستوردة على صفحة التكوينات](./media/er-calculated-field-ds-performance-imported-configurations.png)

## <a name="review-the-sample-er-solution"></a><span data-ttu-id="6fe1c-132">مراجعة عينة حل التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="6fe1c-132">Review the sample ER solution</span></span>

### <a name="review-the-model-mapping"></a><span data-ttu-id="6fe1c-133">مراجعة تعيين النموذج</span><span class="sxs-lookup"><span data-stu-id="6fe1c-133">Review the model mapping</span></span>

1. <span data-ttu-id="6fe1c-134">في صفحة **التكوينات**، في شجرة التكوين، وسَّع **نموذج تحسين الأداء**، ثم حدد **تعيين تحسين الأداء**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-134">On the **Configurations** page, in the configuration tree, expand **Performance improvement model**, and select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="6fe1c-135">في جزء الإجراءات، حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-135">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="6fe1c-136">في صفحة **تعيين النموذج إلى مصدر البيانات** في جزء الإجراءات، حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-136">On the **Model to datasource mapping** page, on the Action Pane, select **Designer**.</span></span>

    <span data-ttu-id="6fe1c-137">يتم تصميم تعيين نموذج إعداد التقارير الإلكترونية لتنفيذ الإجراءات التالية:</span><span class="sxs-lookup"><span data-stu-id="6fe1c-137">This ER model mapping is designed to perform the following actions:</span></span>

    - <span data-ttu-id="6fe1c-138">إحضار قائمة حركات المورّدين المخزنة في الجدول VendTrans (مصدر البيانات **Trans**).</span><span class="sxs-lookup"><span data-stu-id="6fe1c-138">Fetch the list of vendor transactions that are stored in the VendTrans table (**Trans** data source).</span></span>
    - <span data-ttu-id="6fe1c-139">لكل حركة، يمكنك إحضار، من الجدول VendTable، سجل مورّد تم ترحيل الحركة له (مصدر البيانات **\#‎Vend**).</span><span class="sxs-lookup"><span data-stu-id="6fe1c-139">For every transaction, fetch, from the VendTable table, the record of a vendor that the transaction has been posted for (**\#Vend** data source).</span></span>

    > [!NOTE]
    > <span data-ttu-id="6fe1c-140">يتم تكوين مصدر البيانات **\#Vend** لإحضار سجل المورّد المناظر باستخدام علاقة واحد إلى متعدد الموجودة **\@.'\>Relations'.VendTable\_AccountNum**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-140">The **\#Vend** data source is configured to fetch the corresponding vendor record by using the existing many-to-one relation **\@.'\>Relations'.VendTable\_AccountNum**.</span></span>

    <span data-ttu-id="6fe1c-141">يقوم تعيين النموذج في هذا التكوين بتنفيذ نموذج البيانات الأساسي لأي من تنسيقات التقارير الإلكترونية التي تم إنشاؤها لهذا النموذج وتم تشغيلها في Finance.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-141">The model mapping in this configuration implements the base data model for any ER formats that are created for this model and run in Finance.</span></span> <span data-ttu-id="6fe1c-142">نتيجة لذلك، يتم كشف محتوى مصدر البيانات **Trans** لتنسيقات التقارير الإلكترونية مثل مصادر البيانات المجردة **النموذج**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-142">Therefore, the content of the **Trans** data source is exposed for ER formats such as abstract **model** data sources.</span></span>

    ![مصدر البيانات Trans في صفحة مصمم تعيين النموذج](media/er-calculated-field-ds-performance-mapping-1.png)

4. <span data-ttu-id="6fe1c-144">أغلق صفحة **مصمم تعيين النموذج**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-144">Close the **Model mapping designer** page.</span></span>
5. <span data-ttu-id="6fe1c-145">أغلق صفحة **تعيين النموذج إلى مصدر البيانات**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-145">Close the **Model to datasource mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="6fe1c-146">مراجعة التنسيق</span><span class="sxs-lookup"><span data-stu-id="6fe1c-146">Review format</span></span>

1. <span data-ttu-id="6fe1c-147">في صفحة **التكوينات**، في شجرة التكوين، وسَّع **نموذج تحسين الأداء**، ثم حدد **تنسيق تحسين الأداء**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-147">On the **Configurations** page, in the configuration tree, expand **Performance improvement model**, and select **Performance improvement format**.</span></span>
2. <span data-ttu-id="6fe1c-148">في جزء الإجراءات، حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-148">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="6fe1c-149">في الصفحة **مصمم التنسيق**، على علامة التبويب **التعيين**، حدد **توسيع/طي**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-149">On the **Format designer** page, on the **Mapping** tab, select **Expand/Collapse**.</span></span>
4. <span data-ttu-id="6fe1c-150">قم بتوسيع عناصر **النموذج**، و **البيانات**، و **الحركة**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-150">Expand the **Model**, **Data,** and **Transaction** items.</span></span>

    <span data-ttu-id="6fe1c-151">تم تصميم تنسيق التقارير الإلكترونية هذا لإنشاء تقرير حركات المورّد بتنسيق XML.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-151">This ER format is designed to generate a vendor transactions report in XML format.</span></span>

    ![مصادر بيانات التنسيق والروابط المكونة لعناصر التنسيق في صفحة مصمم التنسيق](media/er-calculated-field-ds-performance-format.png)

5. <span data-ttu-id="6fe1c-153">أغلق صفحة **مصمم المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-153">Close the **Format designer** page.</span></span>

## <a name="run-the-sample-er-solution-to-trace-execution"></a><span data-ttu-id="6fe1c-154">تشغيل حل التقارير الإلكترونية لتتبع التنفيذ</span><span class="sxs-lookup"><span data-stu-id="6fe1c-154">Run the sample ER solution to trace execution</span></span>

<span data-ttu-id="6fe1c-155">تخيّل أنك انتهيت من تصميم الإصدار الأول لحل التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-155">Imagine that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="6fe1c-156">وتريد الآن اختبار الحل في مثيل Finance وتحليل أداء التنفيذ.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-156">You now want to test the solution in your Finance instance and analyze the execution performance.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="6fe1c-157">تشغيل تتبع أداء التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="6fe1c-157">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="6fe1c-158">قم بتحديد شركة **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-158">Select the **DEMF** company.</span></span>
2. <span data-ttu-id="6fe1c-159">اتبع الخطوات في [تشغيل تتبع أداء التقارير الإلكترونية‬](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) لإنشاء تتبع أداء أثناء تشغيل تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-159">Follow the steps in [Turn on the ER performance trace](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) to generate a performance trace while an ER format is run.</span></span>

    ![مربع علامة تبويب معلمات المستخدمين](media/er-calculated-field-ds-performance-format-user-parameters.png)

### <a name="run-the-er-format"></a><a id="run-format"></a><span data-ttu-id="6fe1c-161">تشغيل تنسيق التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="6fe1c-161">Run the ER format</span></span>

1. <span data-ttu-id="6fe1c-162">انتقل إلى **إدارة المؤسسة** \> **التقارير الإلكترونية** \> **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-162">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="6fe1c-163">في صفحة **التكوينات**، في شجرة التكوين، حدد **تنسيق تحسين الأداء**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-163">On the **Configurations** page, in the configuration tree, select **Performance improvement format**.</span></span>
3. <span data-ttu-id="6fe1c-164">في جزء الإجراءات، حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-164">On the Action Pane, select **Run**.</span></span>

## <a name="use-the-performance-trace-to-analyze-model-mapping-performance"></a><span data-ttu-id="6fe1c-165">استخدام تتبع الأداء لتحليل أداء تعيين النموذج</span><span class="sxs-lookup"><span data-stu-id="6fe1c-165">Use the performance trace to analyze model mapping performance</span></span>

1. <span data-ttu-id="6fe1c-166">في صفحة **التكوينات**، في شجرة التكوين، حدد **تعيين تحسين الأداء**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-166">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="6fe1c-167">في جزء الإجراءات، حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-167">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="6fe1c-168">في صفحة **تعيينات النموذج** في جزء الإجراءات، حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-168">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="6fe1c-169">في صفحة **مصمم تعيين النموذج**، في جزء الإجراءات، حدد **تتبع الأداء**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-169">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="6fe1c-170">حدد أحدث التتبعات التي تم إنشاؤها، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-170">Select the most recent trace that was generated, and then select **OK**.</span></span>

<span data-ttu-id="6fe1c-171">تتوفر الآن معلومات جديدة تصبح لبعض عناصر مصدر البيانات لتعيين النموذج الحالي:</span><span class="sxs-lookup"><span data-stu-id="6fe1c-171">New information is now available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="6fe1c-172">الوقت الفعلي الذي استغرقه إحضار البيانات باستخدام مصدر البيانات</span><span class="sxs-lookup"><span data-stu-id="6fe1c-172">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="6fe1c-173">نفس الوقت معبر عنه كنسبة مئوية من إجمالي الوقت المستغرق في تشغيل تعيين النموذج بالكامل</span><span class="sxs-lookup"><span data-stu-id="6fe1c-173">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

![تفاصيل وقت التنفيذ على صفحة مصمم تعيين النموذج](./media/er-calculated-field-ds-performance-mapping-2.png)

<span data-ttu-id="6fe1c-175">تُظهر شبكة **إحصائيات الأداء** أن مصدر البيانات **Trans** يستدعي الجدول VendTrans مرة واحدة.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-175">The **Performance statistics** grid shows that the **Trans** data source calls the VendTrans table one time.</span></span> <span data-ttu-id="6fe1c-176">تشير القيمة **\[265\]\[Q:265\]** لمصدر البيانات **Trans** إلى إحضار حركات المورّد 265 من جدول التطبيق وتم إرجاعها إلى نموذج البيانات.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-176">The value **\[265\]\[Q:265\]** of the **Trans** data source indicates that 265 vendor transactions have been fetched from the application table and returned to the data model.</span></span>

<span data-ttu-id="6fe1c-177">وتُظهر أيضًا شبكة **إحصائيات الأداء** أن تعيين النموذج الحالي يكرر طلبات قاعدة البيانات أثناء تشغيل مصدر البيانات **\#Vend**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-177">The **Performance statistics** grid also shows that the current model mapping duplicates database requests while the **\#Vend** data source is run.</span></span> <span data-ttu-id="6fe1c-178">يحدث هذا التكرار للأسباب التالية:</span><span class="sxs-lookup"><span data-stu-id="6fe1c-178">This duplication occurs for the following reasons:</span></span>

- <span data-ttu-id="6fe1c-179">يتم استدعاء جدول المورّد مرتين لكل حركة من حركات المورّد المكررة 265، لإجمالي 530 استدعاء:</span><span class="sxs-lookup"><span data-stu-id="6fe1c-179">The vendor table is called two times for each of the 265 iterated vendor transactions, for a total of 530 calls:</span></span>

    - <span data-ttu-id="6fe1c-180">يتم إجراء استدعاء واحد لإدخال رقم حساب المورّد.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-180">One call is made to enter the vendor account number.</span></span>
    - <span data-ttu-id="6fe1c-181">يتم إجراء استدعاء واحد لإدخال اسم المورّد.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-181">One call is made to enter the vendor name.</span></span>

- <span data-ttu-id="6fe1c-182">ويتم استدعاء جدول المورّد لكل حركة من حركات المورّد المكررة، على الرغم من ترحيل الحركات التي تم إحضارها لخمسة مورّدين فقط.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-182">The vendor table is called for each iterated vendor transaction, even though the fetched transactions have been posted for only five vendors.</span></span> <span data-ttu-id="6fe1c-183">من بين 530 استدعاء، هناك 525 استدعاء مكرر.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-183">Of the 530 calls, 525 are duplicates.</span></span> <span data-ttu-id="6fe1c-184">يبين الرسم التوضيحي التالي الرسالة التي تتلقاها حول الاستدعاءات المكررة (طلبات قواعد البيانات).</span><span class="sxs-lookup"><span data-stu-id="6fe1c-184">The following illustration shows the message that you receive about duplicate calls (database requests).</span></span>

![رسالة حول طلبات قواعد البيانات المكررة في صفحة مصمم تعيينات النماذج](./media/er-calculated-field-ds-performance-mapping-2a.png)

<span data-ttu-id="6fe1c-186">بالنسبة للوقت الإجمالي لتنفيذ تعيين النموذج (ثماني ثوان تقريبًا)، يمكنك الملاحظة أنه تم قضاء 80 بالمئة (ست ثوانٍ تقريبًا) في استرداد القيم من جدول التطبيق VendTable.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-186">Of the total model mapping execution time (approximately eight seconds), notice that more than 80 percent (approximately six seconds) has been spent retrieving values from the VendTable application table.</span></span> <span data-ttu-id="6fe1c-187">هذه النسبة المئوية كبيرة جدًا لسمتين من خمسة مورّدين، مقارنةً بحجم المعلومات من جدول التطبيق VendTrans.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-187">That percentage is too large for two attributes of five vendors, compared with the volume of information from the VendTrans application table.</span></span>

<span data-ttu-id="6fe1c-188">لتقليل عدد الاستدعاء التي يتم اجراؤها للحصول على تفاصيل المورّد لكل حركة، ولتحسين أداء تعيين النموذج، يمكنك استخدام التخزين المؤقت لمصدر البيانات **\#Vend**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-188">To reduce the number of calls that are made to get the vendor details for every transaction, and to improve the performance of the model mapping, you can use caching for the **\#Vend** data source.</span></span>

> [!NOTE]
> <span data-ttu-id="6fe1c-189">سيتم تخزين مصدر البيانات **Trans\\\#Vend** بشكل مؤقت في نطاق الحركة الحالية لمصدر البيانات **Trans** في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-189">The **Trans\\\#Vend** data source will be cached in the scope of the current transaction of the **Trans** data source at runtime.</span></span>

<span data-ttu-id="6fe1c-190">ومن خلال التخزين المؤقت لمصدر البيانات **\#Vend**، ستقوم بتقليل عدد الاستدعاءات المكررة من 525 إلى 260، ولكن دون إزالة التكرار بشكل كامل.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-190">By caching the **\#Vend** data source, you reduce the number of duplicated calls from 525 to 260, but you don't completely eliminate the duplication.</span></span> <span data-ttu-id="6fe1c-191">لإزالة التكرار بشكل كامل، يمكنك تكوين مصدر بيانات جديد ذي معلمات من نوع **الحقل المحسوب**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-191">To completely eliminate duplication, you can configure a new parameterized data source of the **Calculated field** type.</span></span>

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="6fe1c-192">تحسين تعيين النموذج استنادًا إلى المعلومات الواردة من تتبع التنفيذ</span><span class="sxs-lookup"><span data-stu-id="6fe1c-192">Improve the model mapping based on information from the execution trace</span></span>

### <a name="change-the-logic-of-the-model-mapping"></a><span data-ttu-id="6fe1c-193">تغيير منطق تعيين النموذج</span><span class="sxs-lookup"><span data-stu-id="6fe1c-193">Change the logic of the model mapping</span></span>

<span data-ttu-id="6fe1c-194">اتبع الخطوات التالية لاستخدام التخزين المؤقت ومصدر بيانات من نوع **الحقل المحسوب**، للمساعدة على منع الاستدعاءات المكررة لقاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-194">Follow these steps to use caching and a data source of the **Calculated field** type, to help prevent duplicate calls to the database.</span></span>

1. <span data-ttu-id="6fe1c-195">في صفحة **التكوينات**، في شجرة التكوين، حدد **تعيين تحسين الأداء**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-195">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="6fe1c-196">في جزء الإجراءات، حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-196">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="6fe1c-197">في صفحة **تعيينات النموذج** في جزء الإجراءات، حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-197">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="6fe1c-198">في صفحة **مصمم تعيين النموذج**، اتبع هذه الخطوات لإضافة مصدر بيانات من نوع **سجلات الجدول** للوصول إلى السجلات في جدول تطبيق VendTable:</span><span class="sxs-lookup"><span data-stu-id="6fe1c-198">On the **Model mapping designer** page, follow these steps to add a data source of the **Table records** type to access records in the VendTable application table:</span></span>

    1. <span data-ttu-id="6fe1c-199">في الجزء **أنواع مصادر البيانات**، قم بتوسيع **Dynamics 365 for Operations**، وحدد **سجلات البيانات**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-199">In the **Data source types** pane, expand **Dynamics 365 for Operations**, and select **Table records**.</span></span>
    2. <span data-ttu-id="6fe1c-200">حدد **إضافة جذر**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-200">Select **Add root**.</span></span>
    3. <span data-ttu-id="6fe1c-201">في مربع الحوار، في الحقل **الاسم**، أدخل **Vend**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-201">In the dialog box, in the **Name** field, enter **Vend**.</span></span>
    4. <span data-ttu-id="6fe1c-202">في حقل **الجدول**، أدخل **VendTable‎‎**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-202">In the **Table** field, enter **VendTable**.</span></span>
    5. <span data-ttu-id="6fe1c-203">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-203">Select **OK**.</span></span>

5. <span data-ttu-id="6fe1c-204">يمكن تعيين معلمات لاستدعاءات مصادر البيانات من نوع **الحقل المحسوب** الحقل إذا كانت مصادر البيانات هذه موجودة في حاوية.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-204">You can parameterize calls to data sources of the **Calculated field** type only if those data sources reside in a container.</span></span> <span data-ttu-id="6fe1c-205">وبالتالي، اتبع الخطوات التالية لإضافة مصدر بيانات من نوع **الحاوية الفارغة** لاحتواء مصدر بيانات جديد ذي معلمات من نوع **الحقل المحسوب**:</span><span class="sxs-lookup"><span data-stu-id="6fe1c-205">Therefore, follow these steps to add a data source of the **Empty container** type to hold a new parameterized data source of the **Calculated field** type:</span></span>

    1. <span data-ttu-id="6fe1c-206">في الجزء **أنواع مصادر البيانات**، قم بتوسيع **عام** وحدد **حاوية فارغة**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-206">In the **Data source types** pane, expand **General**, and select **Empty container**.</span></span>
    2. <span data-ttu-id="6fe1c-207">حدد **إضافة جذر**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-207">Select **Add root**.</span></span>
    3. <span data-ttu-id="6fe1c-208">في مربع الحوار، في الحقل **الاسم**، أدخل **المربع**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-208">In the dialog box, in the **Name** field, enter **Box**.</span></span>
    3. <span data-ttu-id="6fe1c-209">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-209">Select **OK**.</span></span>

    ![مصدر البيانات مربع في صفحة مصمم تعيين النموذج](./media/er-calculated-field-ds-performance-mapping-3.png)

6. <span data-ttu-id="6fe1c-211">اتبع الخطوات التالية لإضافة مصدر بيانات ذي معلمات من نوع **الحقل المحسوب**:</span><span class="sxs-lookup"><span data-stu-id="6fe1c-211">Follow these steps to add a parameterized data source of the **Calculated field** type:</span></span>

    1. <span data-ttu-id="6fe1c-212">حدد **المربع** في جزء **مصادر البيانات** .</span><span class="sxs-lookup"><span data-stu-id="6fe1c-212">In the **Data sources** pane, select **Box**.</span></span>
    2. <span data-ttu-id="6fe1c-213">في جزء **انواع مصادر البيانات**، قم بتوسيع عنصر **الوظائف**، وحدد **الحقل المحسوب**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-213">In the **Data source types** pane, expand **Functions**, and select **Calculated field**.</span></span>
    3. <span data-ttu-id="6fe1c-214">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-214">Select **Add**.</span></span>
    4. <span data-ttu-id="6fe1c-215">في مربع الحوار، في الحقل **الاسم**، أدخل **Vend**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-215">In the dialog box, in the **Name** field, enter **Vend**.</span></span>
    5. <span data-ttu-id="6fe1c-216">حدد **تحرير المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-216">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="6fe1c-217">في الصفحة **مصمم المعادلة**، حدد **المعلمات** لتحديد المعلمات التي يجب توفيرها عند استدعاء مصدر البيانات هذا.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-217">On the **Formula designer** page, select **Parameters** to specify the parameters that must be provided when this data source is called.</span></span>
    7. <span data-ttu-id="6fe1c-218">في مربع الحوار **المعلمات**، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-218">In the **Parameters** dialog box, select **New**.</span></span>
    8. <span data-ttu-id="6fe1c-219">في حقل **الاسم**، أدخل **parmVendAccNumber**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-219">In the **Name** field, enter **parmVendAccNumber**.</span></span>
    9. <span data-ttu-id="6fe1c-220">في حقل **النوع**، حدد **سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-220">In the **Type** field, select **String**.</span></span>
    10. <span data-ttu-id="6fe1c-221">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-221">Select **OK**.</span></span>
    11. <span data-ttu-id="6fe1c-222">في حقل **المعادلة**، أدخل **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-222">In the **Formula** field, enter **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))**.</span></span>
    12. <span data-ttu-id="6fe1c-223">حدد **حفظ** وأغلق صفحة **مصمم المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-223">Select **Save**, and close the **Formula designer** page.</span></span>
    13. <span data-ttu-id="6fe1c-224">حدد **موافق** لإضافة مصدر البيانات الجديد.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-224">Select **OK** to add the new data source.</span></span>

7. <span data-ttu-id="6fe1c-225">اتبع الخطوات التالية لوضع علامة على مصدر البيانات على أنه مخزن مؤقتًا أثناء التنفيذ:</span><span class="sxs-lookup"><span data-stu-id="6fe1c-225">Follow these steps to mark the added data source as cached during the execution:</span></span>

    1. <span data-ttu-id="6fe1c-226">في جزء **مصادر البيانات**، حدد **Box\\Vend**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-226">In the **Data sources** pane, select **Box\\Vend**.</span></span>
    2. <span data-ttu-id="6fe1c-227">حدد **ذاكرة التخزين المؤقت**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-227">Select **Cache**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6fe1c-228">سيتم تخزين مصدر البيانات **Box\\Vend** بشكل مؤقت في نطاق جميع حركات المورّدين لمصدر البيانات **Trans** في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-228">The **Box\\Vend** data source will be cached in the scope of all vendor transactions of the **Trans** data source at runtime.</span></span>

8. <span data-ttu-id="6fe1c-229">اتبع هذه الخطوات لتحديث مصدر البيانات **Trans\\\#Vend** المتداخل بحيث يستخدم مصدر البيانات **Box\\Vend**:</span><span class="sxs-lookup"><span data-stu-id="6fe1c-229">Follow these steps to update the nested **Trans\\\#Vend** data source so that it uses the **Box\\Vend** data source:</span></span>

    1. <span data-ttu-id="6fe1c-230">في جزء **مصادر البيانات**، قم بتوسيع **Trans** .</span><span class="sxs-lookup"><span data-stu-id="6fe1c-230">In the **Data sources** pane, expand **Trans**.</span></span>
    2. <span data-ttu-id="6fe1c-231">حدد مصدر البيانات **Trans\\\#Vend**، ثم حدد **تحرير** \> **تحرير المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-231">Select the **Trans\\\#Vend** data source, and then select **Edit** \> **Edit formula**.</span></span>
    3. <span data-ttu-id="6fe1c-232">في الصفحة **مصمم المعادلة**، في حقل **المعادلة‏‎**، أدخل **Box.Vend(\@.AccountNum)**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-232">On the **Formula designer** page, in the **Formula** field, enter **Box.Vend(\@.AccountNum)**.</span></span>
    4. <span data-ttu-id="6fe1c-233">حدد **حفظ**، ثم أغلق صفحة **مصمم المعادلة**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-233">Select **Save**, and then close the **Formula designer** page.</span></span>
    5. <span data-ttu-id="6fe1c-234">حدد **موافق** لإكمال التغييرات التي أجريتها في مصدر البيانات المحدد.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-234">Select **OK** to complete your changes to the selected data source.</span></span>

9. <span data-ttu-id="6fe1c-235">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-235">Select **Save**.</span></span>

    ![مصدر البيانات Vend في صفحة مصمم تعيين النموذج](./media/er-calculated-field-ds-performance-mapping-4.png)

10. <span data-ttu-id="6fe1c-237">أغلق صفحة **مصمم تعيين النموذج**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-237">Close the **Model mapping designer** page.</span></span>
11. <span data-ttu-id="6fe1c-238">أغلق صفحة **تعيينات النماذج**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-238">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="6fe1c-239">إكمال الإصدار المعدل من تعيين طراز التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="6fe1c-239">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="6fe1c-240">في صفحة **التكوينات**، في علامة التبويب السريعة **الإصدارات**، حدد الإصدار **1.2** في تكوين **تعيين تحسين الأداء**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-240">On the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance improvement mapping** configuration.</span></span>
2. <span data-ttu-id="6fe1c-241">حدد **تغيير الحالة** \> **إكمال**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-241">Select **Change status** \> **Complete**, and then select **OK**.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="6fe1c-242">تشغيل حل التقارير الإلكترونية المعدل لتتبع التنفيذ</span><span class="sxs-lookup"><span data-stu-id="6fe1c-242">Run the modified ER solution to trace execution</span></span>

<span data-ttu-id="6fe1c-243">كرر الخطوات الموجودة في قسم [تشغيل تنسيق التقارير الإلكترونية](#run-format) من قبل في هذا الموضوع لإنشاء تتبع أداء جديد.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-243">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="use-the-performance-trace-to-analyze-adjustments-to-the-model-mapping"></a><span data-ttu-id="6fe1c-244">استخدام تتبع الأداء لتحليل التعديلات في تعيين النموذج</span><span class="sxs-lookup"><span data-stu-id="6fe1c-244">Use the performance trace to analyze adjustments to the model mapping</span></span> 

1. <span data-ttu-id="6fe1c-245">في صفحة **التكوينات**، في شجرة التكوين، حدد **تعيين تحسين الأداء**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-245">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="6fe1c-246">في جزء الإجراءات، حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-246">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="6fe1c-247">في صفحة **تعيينات النموذج** في جزء الإجراءات، حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-247">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="6fe1c-248">في صفحة **مصمم تعيين النموذج**، في جزء الإجراءات، حدد **تتبع الأداء**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-248">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="6fe1c-249">حدد أحدث التتبعات التي تم إنشاؤها، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-249">Select the most recent trace that was generated, and then select **OK**.</span></span>

<span data-ttu-id="6fe1c-250">لاحظ أن التسويات التي أجريتها على تعيين النموذج قد تقوم بإزالة الاستعلامات المكررة لقاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-250">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="6fe1c-251">يتم أيضًا تقليل عدد الاستدعاءات إلى جداول قاعدة البيانات ومصادر البيانات لتعيين هذا النموذج.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-251">The number of calls to database tables and data sources for this model mapping has also been reduced.</span></span>

![تتبع المعلومات في صفحة مصمم تعيين النموذج 1](./media/er-calculated-field-ds-performance-mapping-5.png)

<span data-ttu-id="6fe1c-253">تم تقليل وقت التنفيذ الإجمالي حوالي 20 مرة (من 8 ثوان إلى حوالي 400 مللي ثانية).</span><span class="sxs-lookup"><span data-stu-id="6fe1c-253">The total execution time has been reduced about 20 times (from about 8 seconds to about 400 milliseconds).</span></span> <span data-ttu-id="6fe1c-254">وبالتالي، تم تحسين أداء حل التقارير الإلكترونية بالكامل.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-254">Therefore, the performance of the whole ER solution has been improved.</span></span>

![تتبع المعلومات في صفحة مصمم تعيين النموذج 2](./media/er-calculated-field-ds-performance-mapping-5a.png)

## <a name="appendix-1-download-the-components-of-the-sample-microsoft-er-solution"></a><a name="appendix1"></a><span data-ttu-id="6fe1c-256">الملحق 1: تنزيل مكونات عينة حل التقارير الإلكترونية من Microsoft</span><span class="sxs-lookup"><span data-stu-id="6fe1c-256">Appendix 1: Download the components of the sample Microsoft ER solution</span></span>

<span data-ttu-id="6fe1c-257">يجب عليك تنزيل الملفات التالية وتخزينها محليًا.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-257">You must download the following files and store them locally.</span></span>

| <span data-ttu-id="6fe1c-258">ملف</span><span class="sxs-lookup"><span data-stu-id="6fe1c-258">File</span></span>                                        | <span data-ttu-id="6fe1c-259">المحتوى</span><span class="sxs-lookup"><span data-stu-id="6fe1c-259">Content</span></span> |
|---------------------------------------------|---------|
| <span data-ttu-id="6fe1c-260">تحسين الأداء model.version.1</span><span class="sxs-lookup"><span data-stu-id="6fe1c-260">Performance improvement model.version.1</span></span>     | [<span data-ttu-id="6fe1c-261">تكوين نموذج عينة بيانات التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="6fe1c-261">Sample ER data model configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="6fe1c-262">تحسين الأداء mapping.version.1.1</span><span class="sxs-lookup"><span data-stu-id="6fe1c-262">Performance improvement mapping.version.1.1</span></span> | [<span data-ttu-id="6fe1c-263">تكوين تعيين نموذج عينة التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="6fe1c-263">Sample ER model mapping configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="6fe1c-264">تحسين الأداء format.version.1.1</span><span class="sxs-lookup"><span data-stu-id="6fe1c-264">Performance improvement format.version.1.1</span></span>  | [<span data-ttu-id="6fe1c-265">تكوين تنسيق عينة التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="6fe1c-265">Sample ER format configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

## <a name="appendix-2-configure-the-er-framework"></a><a name="appendix2"></a><span data-ttu-id="6fe1c-266">الملحق 2: تكوين إطار عمل التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="6fe1c-266">Appendix 2: Configure the ER framework</span></span>

<span data-ttu-id="6fe1c-267">قبل أن تتمكن من بدء استخدام اطار عمل التقارير الإلكترونية لتحسين أداء عينة حل التقارير الإلكترونية من Microsoft‬، يجب عليك تكوين الحد الأدنى لمجموعة معلمات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-267">Before you can start to use the ER framework to improve the performance of the sample Microsoft ER solution, you must configure the minimal set of ER parameters.</span></span>

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a><span data-ttu-id="6fe1c-268">تكوين معلمات التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="6fe1c-268">Configure ER parameters</span></span>

1. <span data-ttu-id="6fe1c-269">انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-269">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="6fe1c-270">في الصفحة **تكوينات الترجمة**، في قسم **الارتباطات المتعلقة**، حدد **معلمات التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-270">On the **Localization configurations** page, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="6fe1c-271">في صفحة **معلمات التقارير الإلكترونية**، على علامة التبويب **عام**، عيّن الخيار **تمكين وضع التصميم** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-271">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="6fe1c-272">في علامة التبويب **المرفقات**، عيّن المعلمات التالية:</span><span class="sxs-lookup"><span data-stu-id="6fe1c-272">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="6fe1c-273">في حقل **التكوينات**، حدد نوع **الملف** لشركة **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-273">In the **Configurations** field, select the **File** type for the **DEMF** company.</span></span>
    - <span data-ttu-id="6fe1c-274">في حقول **أرشيف الوظيفة** و **المؤقت** و **الأساس** و **أخرى**، حدد نوع **الملف**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-274">In the **Job archive**, **Temporary**, **Baseline**, and **Others** fields, select the **File** type.</span></span>

<span data-ttu-id="6fe1c-275">لمزيد من المعلومات حول معلمات ER ، راجع [تكوين إطار عمل ER](electronic-reporting-er-configure-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="6fe1c-275">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="6fe1c-276">تنشيط موفر تكوين ER</span><span class="sxs-lookup"><span data-stu-id="6fe1c-276">Activate an ER configuration provider</span></span>

<span data-ttu-id="6fe1c-277">يتم تعليم كل تكوين ER تمت إضافته باعتباره مملوكا لموفر تكوين ER.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-277">Every ER configuration that is added is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="6fe1c-278">يتم استخدام موفر تكوين ER الذي تم تنشيطه في مساحة عمل **التقارير الإلكترونية** لهذا الغرض.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-278">The ER configuration provider that is activated in the **Electronic reporting** workspace is used for this purpose.</span></span> <span data-ttu-id="6fe1c-279">بالتالي، يجب عليك تنشيط موفر تكوين ER في مساحة عمل **التقارير الإلكترونية** قبل البدء في إضافة تكوينات ER أو تحريرها.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-279">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="6fe1c-280">يمكن لمالك تكوين التقارير الإلكترونية فقط تحرير التكوين.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-280">Only the owner of an ER configuration can edit the configuration.</span></span> <span data-ttu-id="6fe1c-281">بالتالي، قبل تحرير تكوين ER، يجب تنشيط موفر تكوين ER المناسب في مساحة عمل **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-281">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a><span data-ttu-id="6fe1c-282">مراجعة قائمة موفري تكوين ER</span><span class="sxs-lookup"><span data-stu-id="6fe1c-282">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="6fe1c-283">انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-283">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="6fe1c-284">في الصفحة **تكوينات الترجمة**، في قسم **الارتباطات المتعلقة**، حدد **موفري التكوين** .</span><span class="sxs-lookup"><span data-stu-id="6fe1c-284">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="6fe1c-285">في صفحة **جدول موفري التكوين**، يتضمن كل سجل موفر اسمًا وعنوان URL فريدين.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-285">On the **Configuration provider table** page, each provider record has a unique name and URL.</span></span> <span data-ttu-id="6fe1c-286">راجع محتويات هذه الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-286">Review the contents of this page.</span></span> <span data-ttu-id="6fe1c-287">في حالة وجود سجل **Litware, Inc.**، يمكنك تخطي الإجراء التالي [إضافة موفر تكوين تقارير إلكترونية جديد](#ActivateProvider).</span><span class="sxs-lookup"><span data-stu-id="6fe1c-287">If a record for **Litware, Inc.** already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="6fe1c-288">إضافة موفر تكوين ER جديد</span><span class="sxs-lookup"><span data-stu-id="6fe1c-288">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="6fe1c-289">انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-289">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="6fe1c-290">في الصفحة **تكوينات الترجمة**، في قسم **الارتباطات المتعلقة**، حدد **موفري التكوين** .</span><span class="sxs-lookup"><span data-stu-id="6fe1c-290">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="6fe1c-291">في صفحة **موفري التكوين**، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-291">On the **Configuration providers** page, select **New**.</span></span>
4. <span data-ttu-id="6fe1c-292">في حقل **الاسم**، أدخل **Litware, Inc**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-292">In the **Name** field, enter **Litware, Inc.**</span></span>
5. <span data-ttu-id="6fe1c-293">في الحقل **عنوان الإنترنت**، أدخل `https://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-293">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
6. <span data-ttu-id="6fe1c-294">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-294">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a><span data-ttu-id="6fe1c-295">تنشيط موفر تكوين ER</span><span class="sxs-lookup"><span data-stu-id="6fe1c-295">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="6fe1c-296">انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-296">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="6fe1c-297">في صفحة **تكوينات التعريب**، في القسم **موفري التكوين**، حدد تجانب **Litware, Inc.** ثم حدد **تعيين نشط**.</span><span class="sxs-lookup"><span data-stu-id="6fe1c-297">On the **Localization configurations** page, in the **Configuration providers** section, select the **Litware, Inc.** tile, and then select **Set active**.</span></span>

<span data-ttu-id="6fe1c-298">لمزيد من المعلومات حول موفري تكوين ER، راجع [إنشاء موفري التكوين ووضع علامة عليهم كنشطين](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="6fe1c-298">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6fe1c-299">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="6fe1c-299">Additional resources</span></span>

- [<span data-ttu-id="6fe1c-300">نظرة عامة حول التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="6fe1c-300">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="6fe1c-301">تتبع تنفيذ تنسيقات التقارير الإلكترونية لاستكشاف مشكلات الأداء وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="6fe1c-301">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)
- [<span data-ttu-id="6fe1c-302">دعم استدعاءات ذات معلمات لمصادر بيانات التقارير الإلكترونية لنوع الحقل المحسوب‬</span><span class="sxs-lookup"><span data-stu-id="6fe1c-302">Support parameterized calls of ER data sources of the Calculated field type</span></span>](er-calculated-field-type.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]