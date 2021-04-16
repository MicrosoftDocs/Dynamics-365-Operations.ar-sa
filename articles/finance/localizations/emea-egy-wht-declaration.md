---
title: إقرار ضريبة الخصم في مصر
description: يوضح هذا الموضوع كيفية تكوين وإنشاء إقرارات ضريبة الخصم لمصر.
author: sndray
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 4e3d68ac003fabaa504ffe81b8bf2f7ff8d7538d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839782"
---
#  <a name="withholding-tax-declaration-for-egypt-eg-00005"></a><span data-ttu-id="1d605-103">إقرار ضريبة الخصم في مصر (EG-00005)</span><span class="sxs-lookup"><span data-stu-id="1d605-103">Withholding tax declaration for Egypt (EG-00005)</span></span>

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

## <a name="overview"></a><span data-ttu-id="1d605-104">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="1d605-104">Overview</span></span>
<span data-ttu-id="1d605-105">يوضح هذا الموضوع كيفية إعداد وإنشاء إقرار ضريبة الخصم ونماذج إقرار ضريبة الخصم 41 و 11 للكيانات القانونية في مصر</span><span class="sxs-lookup"><span data-stu-id="1d605-105">This topic explains how to set up and generate the withholding tax declaration and the withholding tax declaration forms 41 and 11 for legal entities in Egypt</span></span> 

<span data-ttu-id="1d605-106">يجب أن تقوم كافة الكيانات المصرية بإعداد النموذج 41 الذي يلخص كافة الضرائب التي يتم الاحتفاظ بها من الموردين المحليين وموفري الخدمة.</span><span class="sxs-lookup"><span data-stu-id="1d605-106">All Egyptian entities must prepare the form  41 which summarizes all taxes that are retained from local suppliers and service providers.</span></span> <span data-ttu-id="1d605-107">بالإضافة إلى النموذج 41، يجب إنشاء النموذج 11 لتفصيل كافة الاستقطاعات الخاضعة للضرائب من الموفرين الخارجيين.</span><span class="sxs-lookup"><span data-stu-id="1d605-107">In addition to form 41, form 11 must be generated to detail all of the retained taxed from foreign providers.</span></span> 

<span data-ttu-id="1d605-108">يتضمن تقرير **إقرار ضريبة الخصم** في Dynamics 365 Finance التقارير التالية:</span><span class="sxs-lookup"><span data-stu-id="1d605-108">The **Withholding tax declaration** report in Dynamics 365 Finance includes the following reports:</span></span>

- <span data-ttu-id="1d605-109">نموذج الإقرار رقم.</span><span class="sxs-lookup"><span data-stu-id="1d605-109">Declaration form No.</span></span> <span data-ttu-id="1d605-110">41</span><span class="sxs-lookup"><span data-stu-id="1d605-110">41</span></span>
- <span data-ttu-id="1d605-111">نموذج الإقرار رقم.</span><span class="sxs-lookup"><span data-stu-id="1d605-111">Declaration form No.</span></span> <span data-ttu-id="1d605-112">11</span><span class="sxs-lookup"><span data-stu-id="1d605-112">11</span></span>
    
    
## <a name="prerequisites"></a><span data-ttu-id="1d605-113">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="1d605-113">Prerequisites</span></span>
<span data-ttu-id="1d605-114">يجب أن يكون العنوان الرئيسي للكيان القانوني في مصر.</span><span class="sxs-lookup"><span data-stu-id="1d605-114">The primary address of the legal entity must be in Egypt.</span></span>
<span data-ttu-id="1d605-115">في مساحة عمل **إدارة الميزات**، يجب تمكين الميزات التالية:</span><span class="sxs-lookup"><span data-stu-id="1d605-115">In the **Feature management** workspace, the following feature must be enabled:</span></span>

   - <span data-ttu-id="1d605-116">**ضريبة الخصم العمومية**</span><span class="sxs-lookup"><span data-stu-id="1d605-116">**Global withholding tax**</span></span>

<span data-ttu-id="1d605-117">لمزيد من المعلومات حول كيفية تمكين الميزات، راجع [نظرة عامة على إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1d605-117">For more information about how to enable features, see [Feature management overview.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)</span></span>

1. <span data-ttu-id="1d605-118">انتقل إلى **الضريبة** > **الإعداد** > **المعلمات** > **معلمات دفتر الأستاذ العام**، ثم في علامة التبويب **ضريبة الخصم**، قم بتعيين خيار **تمكين ضريبة الخصم العامة** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="1d605-118">Go to **Tax** > **Setup** > **Parameters** > **General ledger parameters**, and on the **Withholding tax** tab, set **Enable global withholding tax** to **Yes**.</span></span>
2. <span data-ttu-id="1d605-119">في مساحة عمل **التقارير الإلكترونية**، قم باستيراد تنسيقات التقارير الإلكتروني التالية من المستودع:</span><span class="sxs-lookup"><span data-stu-id="1d605-119">In the **Electronic reporting** workspace, import the following Electronic reporting formats from the repository:</span></span>

    - <span data-ttu-id="1d605-120">إقرار ضريبة الخصم Excel (مصر)</span><span class="sxs-lookup"><span data-stu-id="1d605-120">WHT Declaration Excel (EG)</span></span>

    > [!NOTE]
    > <span data-ttu-id="1d605-121">يعتمد التنسيق أعلاه على **نموذج إقرار الضريبة** ويستخدم **تعيين نموذج إقرار الضريبة**.</span><span class="sxs-lookup"><span data-stu-id="1d605-121">The format above is based on the **Tax declaration model** and uses the **Tax declaration model mapping**.</span></span> <span data-ttu-id="1d605-122">سيتم استيراد هذا التكوين الإضافي تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="1d605-122">This additional configuration is automatically imported.</span></span>

<span data-ttu-id="1d605-123">لمزيد من المعلومات حول كيفية استيراد تكوينات التقارير الإلكترونية، راجع [تنزيل تكوينات التقارير الإلكترونية من Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="1d605-123">For more information about how to import Electronic reporting configurations, see [Download Electronic reporting configurations from Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

## <a name="download-electronic-reporting-configurations"></a><span data-ttu-id="1d605-124">تنزيل تكوينات إعداد التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="1d605-124">Download Electronic reporting configurations</span></span>

<span data-ttu-id="1d605-125">يعتمد تنفيذ نموذج إقرار ضريبة الخصم لمصر على تكوينات التقارير الإلكترونية (ER).</span><span class="sxs-lookup"><span data-stu-id="1d605-125">The implementation of the WHT declaration forms for Egypt is based on Electronic reporting (ER) configurations.</span></span> <span data-ttu-id="1d605-126">لمزيد من المعلومات حول إمكانات ومفاهيم التقارير القابلة للتكوين، راجع [إعداد التقارير الإلكترونية](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="1d605-126">For more information about the capabilities and concepts of configurable reporting, see [Electronic reporting](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).</span></span>

<span data-ttu-id="1d605-127">بالنسبة لبيئات الإنتاج واختبار قبول المستخدم (UAT)، اتبع التعليمات في موضوع [تحميل تكوينات التقارير الإلكترونية من Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="1d605-127">For production and user acceptance testing (UAT) environments, follow the instructions in the topic, [Download Electronic reporting configurations from Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

<span data-ttu-id="1d605-128">لإنشاء إقرارات الخصم في كيان قانوني مصري، يجب تحميل التكوينات التالية:</span><span class="sxs-lookup"><span data-stu-id="1d605-128">To generate the Withholding declarations in an Egyptian legal entity, you need to upload the following configurations:</span></span>

- <span data-ttu-id="1d605-129">نموذج الإقرار الضريبي model.version.82.xml أو إصدار أحدث</span><span class="sxs-lookup"><span data-stu-id="1d605-129">Tax declaration model.version.82.xml or later version</span></span>
- <span data-ttu-id="1d605-130">نموذج الإقرار الضريبي mapping.version.82.133.xml أو إصدار أحدث</span><span class="sxs-lookup"><span data-stu-id="1d605-130">Tax declaration model mapping.version.82.133.xml or a later version</span></span>
- <span data-ttu-id="1d605-131">إقرار ضريبة الخصم Excel (EG).version.82.21 أو إصدار أحدث</span><span class="sxs-lookup"><span data-stu-id="1d605-131">WHT Declaration Excel (EG).version.82.21  or a later version</span></span>

<span data-ttu-id="1d605-132">بعد الانتهاء من تنزيل تكوينات التقارير الإلكترونية (ER) من Lifecycle Services (LCS) أو المستودع العمومي، أكمل الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="1d605-132">After you finish downloading the ER configurations from Lifecycle Services (LCS) or the global repository, complete the following steps.</span></span>

1. <span data-ttu-id="1d605-133">انتقل إلى مساحة عمل **إعداد التقارير الإلكترونية**، حدد الإطار المتجانب **تكوينات إعداد التقارير**.</span><span class="sxs-lookup"><span data-stu-id="1d605-133">Go to the **Electronic reporting** workspace and select the **Reporting configurations** tile.</span></span>
1. <span data-ttu-id="1d605-134">في صفحة **التكوينات**، في جزء الإجراء، حدد **Exchange > تحميل من ملف XML**.</span><span class="sxs-lookup"><span data-stu-id="1d605-134">On the **Configurations** page, on the Action Pane, select **Exchange > Load from XML file**.</span></span>
1. <span data-ttu-id="1d605-135">قم بتحميل كافة الملفات بالترتيب الذي تم سردها به في التعداد النقطي السابق.</span><span class="sxs-lookup"><span data-stu-id="1d605-135">Upload all the files in the order in which they are listed in the previous bullets.</span></span> <span data-ttu-id="1d605-136">بعد تحميل كافة التكوينات، يجب أن تكون شجرة التكوين موجودة في Finance.</span><span class="sxs-lookup"><span data-stu-id="1d605-136">After all of the configurations are uploaded, the configuration tree should be present in Finance.</span></span>

## <a name="set-up-application-specific-parameters"></a><span data-ttu-id="1d605-137">إعداد معلمات خاصة بالتطبيق</span><span class="sxs-lookup"><span data-stu-id="1d605-137">Set up application-specific parameters</span></span>

<span data-ttu-id="1d605-138">يتيح خيار المعلمات الخاصة بالتطبيق للمستخدمين تحديد معايير كيفية تصنيف حركات الضريبة وحسابها في كل بند من التقرير الذي يتم إنشاؤه استنادا إلى تكوين **مجموعة أصناف ضريبة الخصم** أو المعايير الأخرى التي تم تأسيسها في تعريف البحث.</span><span class="sxs-lookup"><span data-stu-id="1d605-138">The application-specific parameters option lets users establish the criteria of how the tax transactions will be classified and calculated in each line of a generated report depending on the configuration of **withholding tax item group** or other criteria established in the definition of lookup.</span></span>

<span data-ttu-id="1d605-139">يحتوي نموذج إقرار الخصم 41 على عمود معين حيث يجب تصنيف حركة ضريبة الخصم وفقًا لتصنيف هيئة الضرائب المسمى **نوع كود الخصم**.</span><span class="sxs-lookup"><span data-stu-id="1d605-139">Withholding declaration form 41 includes a specific column where the withholding tax transaction must be classified in accordance with the tax authority classification named **Discount code type**.</span></span> <span data-ttu-id="1d605-140">بدلا من تضمين هذه التصنيفات الجديدة كبيانات إدخال جديدة عند ترحيل الحركات، سيتم تحديد التصنيفات استنادا إلى عمليات البحث المختلفة الواردة في **التكوينات** > **إعداد المعلمات الخاصة بالتطبيق** > **الإعداد** للوفاء بمتطلبات تقارير ضريبة الخصم لمصر.</span><span class="sxs-lookup"><span data-stu-id="1d605-140">Instead of including these new classifications as new entry data when the transactions are posted, the classifications will be determined based on the different lookups introduced in **Configurations** > **Set up application-specific parameters** > **Setup** to meet the requirements of withholding reports for Egypt.</span></span> 

<span data-ttu-id="1d605-141">يتم استخدام التكوين التالي لتصنيف الحركات في التقرير 41 لنموذج إقرار ضريبة الخصم:</span><span class="sxs-lookup"><span data-stu-id="1d605-141">The following configuration is used to classify the transactions in the Withholding declaration form 41 report:</span></span>

- <span data-ttu-id="1d605-142">**DiscountTaxTypeLookup**-> العمود رقم 18</span><span class="sxs-lookup"><span data-stu-id="1d605-142">**DiscountTaxTypeLookup**-> Column No 18</span></span> 

<span data-ttu-id="1d605-143">أكمل الخطوات التالية لاعداد عمليات البحث المختلفة المستخدمة لإنشاء إقرار ضريبة الخصم وتقارير الدفاتر ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="1d605-143">Complete the following steps to set up the different lookups used to generate the WHT declaration and related books reports.</span></span> 

1. <span data-ttu-id="1d605-144">في مساحة عمل **التقارير الإلكترونية**، حدد **التكوينات** > **الإعداد** لإعداد القواعد لتحديد كيف يتم تصنيف الحركات تقرير إقرار ضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="1d605-144">In the **Electronic reporting** workspace, select **Configurations** > **Setup** to set up the rules to identify how transactions are classified in the WHT declaration report.</span></span> 
2. <span data-ttu-id="1d605-145">حدد الإصدار الحالي، وفي علامة التبويب السريعة **عمليات البحث**، حدد اسم البحث.</span><span class="sxs-lookup"><span data-stu-id="1d605-145">Select the current version, and on the **Lookups** FastTab, select the lookup name.</span></span> <span data-ttu-id="1d605-146">على سبيل المثال، **DiscountTaxTypeLookup**.</span><span class="sxs-lookup"><span data-stu-id="1d605-146">For example, **DiscountTaxTypeLookup**.</span></span> <span data-ttu-id="1d605-147">يحدد هذا البحث قائمة أنواع الخصم المطلوبة من قبل هيئة الضرائب.</span><span class="sxs-lookup"><span data-stu-id="1d605-147">This lookup identifies the list of discount types required by the tax authority.</span></span>
3. <span data-ttu-id="1d605-148">في علامة التبويب السريعة **الشروط**، حدد **إضافة** وفي السطر الجديد في عمود **نتيجة البحث**، حدد السطر المرتبط الذي يمثل التصنيف في **العمود 18**.</span><span class="sxs-lookup"><span data-stu-id="1d605-148">On the **Conditions** FastTab, select **Add** and in the new line in the **Lookup result** column, select the related line that represents the classification in the **Column 18**.</span></span>
4. <span data-ttu-id="1d605-149">في عمود **مجموعة أصناف ضريبة الخصم**، حدد الكود المتعلق المستخدم لتحديد التصنيف.</span><span class="sxs-lookup"><span data-stu-id="1d605-149">In the **Withholding tax item group** column, select the related code that's used to identify the classification.</span></span> <span data-ttu-id="1d605-150">على سبيل المثال، **الخصم المسموح به**.</span><span class="sxs-lookup"><span data-stu-id="1d605-150">For example, **Allowed discount**.</span></span>  
5. <span data-ttu-id="1d605-151">كرر الخطوات 3 و4 لكافة عمليات البحث المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="1d605-151">Repeat steps 3 and 4 for all available lookups.</span></span>
6. <span data-ttu-id="1d605-152">حدد **إضافة** مرة أخرى لتضمين سطر السجل النهائي، وفي عمود **نتيجة البحث**، حدد **غير قابل للتطبيق**.</span><span class="sxs-lookup"><span data-stu-id="1d605-152">Select **Add** again to include the final record line, and in the **Lookup result** column, select **Not applicable**.</span></span> 
7. <span data-ttu-id="1d605-153">في الأعمدة المتبقية، حدد **غير فارغ**.</span><span class="sxs-lookup"><span data-stu-id="1d605-153">In the remaining columns, select **Not blank**.</span></span> 

> [!NOTE]

## <a name="set-up-general-ledger-parameters"></a><span data-ttu-id="1d605-154">إعداد معلمات دفتر الأستاذ العام</span><span class="sxs-lookup"><span data-stu-id="1d605-154">Set up General ledger parameters</span></span>

<span data-ttu-id="1d605-155">لإنشاء تقارير نموذج إقرار ضريبة الخصم بتنسيق Microsoft Excel ، قم بتعريف تنسيق ER في صفحة **معلمات دفتر الأستاذ العام**.</span><span class="sxs-lookup"><span data-stu-id="1d605-155">To generate the WHT declaration form reports in Microsoft Excel, define an ER format on the **General ledger parameters** page.</span></span>

1. <span data-ttu-id="1d605-156">انتقل إلى **الضرائب** > **إعداد** > **معلمات دفتر الأستاذ العام**.</span><span class="sxs-lookup"><span data-stu-id="1d605-156">Go to **Tax** > **Setup** > **General ledger parameters**.</span></span>
2. <span data-ttu-id="1d605-157">في علامة التبويب **ضريبة الخصم**، في الحقل **تعيين تنسيق إقرار ضريبة الخصم**، حدد **إقرار ضريبة الخصم Excel (مصر)**.</span><span class="sxs-lookup"><span data-stu-id="1d605-157">On the **Withholding tax** tab, in the **WHT declaration format mapping** field, select **WHT Declaration Excel (EG)**.</span></span> <span data-ttu-id="1d605-158">إذا تركت الحقل فارغا، سيتم إنشاء تقرير ضريبة المبيعات القياسي بتنسيق SSRS.</span><span class="sxs-lookup"><span data-stu-id="1d605-158">If you leave the field blank, the standard sales tax report will be generated in SSRS format.</span></span>


![نموذج الإقرار](media/egypt-wht-declaration-setup1.png)

## <a name="generate-the-withholding-declaration-forms"></a><span data-ttu-id="1d605-160">إنشاء نماذج إقرار الخصم</span><span class="sxs-lookup"><span data-stu-id="1d605-160">Generate the Withholding declaration forms</span></span>
<span data-ttu-id="1d605-161">تستند عملية إعداد وإرسال نموذج إقرار ضريبة الخصم لفترة محددة إلى حركات ضريبة الخصم التي تم ترحيلها أثناء تنفيذ وظيفة تسوية دفع الضريبة وترحيلها.</span><span class="sxs-lookup"><span data-stu-id="1d605-161">The process of preparing and submitting a Withholding declaration form for a specific period is based on the withholding tax transactions posted during the settle and post payment tax job.</span></span> <span data-ttu-id="1d605-162">لمزيد من المعلومات حول ضريبة الخصم العامة، راجع [ضريبة الخصم العامة](../general-ledger/global-withholding-tax-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1d605-162">For more information about global withholding tax, see [Global withholding tax](../general-ledger/global-withholding-tax-overview.md).</span></span>

<span data-ttu-id="1d605-163">أكمل الخطوات التالية لإنشاء تقرير إقرار الضريبة.</span><span class="sxs-lookup"><span data-stu-id="1d605-163">Complete the following steps to generate the tax declaration report.</span></span>

1. <span data-ttu-id="1d605-164">انتقل إلى **الضريبة** > **الإقرارات** > **ضريبة الخصم** > \**دفع ضريبة الخصم*.</span><span class="sxs-lookup"><span data-stu-id="1d605-164">Go to **Tax** > **Declarations** > **Withholding tax** > \**Withholding tax payment*.</span></span>
2. <span data-ttu-id="1d605-165">حدد فتره التسوية ثم حدد تاريخ البدء للتقرير.</span><span class="sxs-lookup"><span data-stu-id="1d605-165">Select the settlement period and then select the from date for the report.</span></span> 
3. <span data-ttu-id="1d605-166">أدخل تاريخ الحركة، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="1d605-166">Enter the transaction date and then select **OK**.</span></span>
4. <span data-ttu-id="1d605-167">في مربع الحوار الذي يتم فتحه، حدد نوعًا أو أكثر من أنواع النماذج **النموذج رقم 41** أو **النموذج رقم 11** أو **بلا**.</span><span class="sxs-lookup"><span data-stu-id="1d605-167">In the dialog box that opens, select one or more of the form types \*\*Form No 41 \*\*, **Form No 11**, or **None**.</span></span> <span data-ttu-id="1d605-168">إذا قمت بتحديد **بلا**، يتم إنشاء التقرير القياسي.</span><span class="sxs-lookup"><span data-stu-id="1d605-168">If you select **None**, the standard report is generated.</span></span> 
5. <span data-ttu-id="1d605-169">حدد اللغة.</span><span class="sxs-lookup"><span data-stu-id="1d605-169">Select the language.</span></span> <span data-ttu-id="1d605-170">تتم ترجمة كافة التقارير باللغات **الإنجليزية الأمريكية** و **العربية المصرية**.</span><span class="sxs-lookup"><span data-stu-id="1d605-170">All reports are translated in **en-us** and **ar-eg**.</span></span>
6. <span data-ttu-id="1d605-171">أدخل الفرع واسم البنك الذي سيتم فيه دفع مدفوعات الضريبة.</span><span class="sxs-lookup"><span data-stu-id="1d605-171">Enter the branch and name of the bank where the tax payment will be paid.</span></span>
7. <span data-ttu-id="1d605-172">حدد نوع الأعمال ثم أدخل الشيك وأرقام المستندات.</span><span class="sxs-lookup"><span data-stu-id="1d605-172">Select the business type and then enter the check and document numbers.</span></span> 
8. <span data-ttu-id="1d605-173">أدخل نوع الكيان.</span><span class="sxs-lookup"><span data-stu-id="1d605-173">Enter the entity type.</span></span> 
9. <span data-ttu-id="1d605-174">أدخل اسم الشخص المسجل لتعيين النموذج وحدد **موافق** لتأكيد إنشاء التقرير.</span><span class="sxs-lookup"><span data-stu-id="1d605-174">Enter the name of person registered to assign the form and select **OK** to confirm the report generation.</span></span> 

 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]
