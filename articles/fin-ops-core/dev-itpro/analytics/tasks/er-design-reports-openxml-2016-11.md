---
title: التقارير الإلكترونية - تصميم تكوين لإنشاء التقارير بتنسيق OPENXML (نوفمبر 2016)
description: يصف هذا الموضوع كيفيه إنشاء تكوين اعداد التقارير الكترونيه الجديد الذي يحتوي علي قالب لإنشاء مستندات إلكترونيه بتنسيق OPENXML.
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERModelGroupByFunctionEditor, VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0f23748f6f1d2c3045b1dc69d8e46821f67da593
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944258"
---
# <a name="er-design-a-configuration-for-generating-reports-in-openxml-format-november-2016"></a><span data-ttu-id="1c3b5-103">التقارير الإلكترونية - تصميم تكوين لإنشاء التقارير بتنسيق OPENXML (نوفمبر 2016)</span><span class="sxs-lookup"><span data-stu-id="1c3b5-103">ER Design a configuration for generating reports in OPENXML format (November 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1c3b5-104">يشرح هذا الموضوع كيف يمكن لمستخدم يؤدي دور مسؤول النظام أو مطور التقارير الإلكترونية إنشاء تكوين تقارير إلكترونية جديد يحتوي على قالب لإنشاء المستندات الإلكترونية بتنسيق OPENXML.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-104">This topic explains how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="1c3b5-105">سيتم استخدام هذا التكوين لمعالجة مدفوعات المورد.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-105">This configuration will be used for processing vendor payments.</span></span>

<span data-ttu-id="1c3b5-106">في هذا المثال، ستقوم بإنشاء تكوين لشركة نمودجية، .Litware, Inc ويمكن تنفيذ هذه الخطوات في شركة GBSI.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>

<span data-ttu-id="1c3b5-107">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "إنشاء موفر تكوين ووضع علامة عليه على أنه نشط".</span><span class="sxs-lookup"><span data-stu-id="1c3b5-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span> <span data-ttu-id="1c3b5-108">كما يجب أن يكون لديك ملف Excel سيتم استيراده عند إنشاء القالب.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-108">You must also have an Excel file which will be imported when creating the template.</span></span> <span data-ttu-id="1c3b5-109">يمكن الوصول إلى هذا الملف من [قالب تقرير الدفع](https://download.microsoft.com/download/3/f/0/3f0658b2-042c-43cf-a776-0f4c7f7cfe4e/SampleVendPaymWsReport.xlsx).</span><span class="sxs-lookup"><span data-stu-id="1c3b5-109">This file can be accessed from the [Template of Payment Report](https://download.microsoft.com/download/3/f/0/3f0658b2-042c-43cf-a776-0f4c7f7cfe4e/SampleVendPaymWsReport.xlsx).</span></span>


## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="1c3b5-110">تحميل تكوين نموذج بيانات الدفعات</span><span class="sxs-lookup"><span data-stu-id="1c3b5-110">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="1c3b5-111">في جزء التنقل، انتقل إلى **الوحدات النمطية > إدارة المؤسسة > مساحات العمل > التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-111">In the navigation pane, go to **Modules > Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="1c3b5-112">في القائمة، ضع علامة على موفر تكوين الشركة النموذجية، Litware, Inc. إذا لم تشاهد موفر التكوين هذا، فيجب أولاً إكمال الخطوات المذكورة في الإجراء [إنشاء موفري التكوين ووضع علامة عليهم على أنهم نشيطون](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="1c3b5-112">In the list, mark the configuration provider for sample company, Litware, Inc. If you don't see this configuration provider, you must first complete the steps in [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="1c3b5-113">حدد **تعيين كنشط**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-113">Select **Set active**.</span></span>
4. <span data-ttu-id="1c3b5-114">حدد **المستودعات**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-114">Select **Repositories**.</span></span> <span data-ttu-id="1c3b5-115">حدد مستودعًا لنوع موارد Operations، إذا كان متوفرًا.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-115">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="1c3b5-116">إذا كان متوفرًا، قم بتخطي الخطوات التالية حول إنشاء مستودع جديد.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-116">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="1c3b5-117">حدد **إضافة** لفتح مربع الحوار المنسدل.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-117">Select **Add** to open the drop dialog.</span></span>
6. <span data-ttu-id="1c3b5-118">في الحقل **نوع مستودع التكوين**، أدخل `Operations resourcesdd`.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-118">In the **Configuration repository type** field, enter `Operations resourcesdd`.</span></span>
7. <span data-ttu-id="1c3b5-119">حدد **إنشاء مستودع**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-119">Select **Create repository**.</span></span>
8. <span data-ttu-id="1c3b5-120">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-120">Select **OK**.</span></span>
9. <span data-ttu-id="1c3b5-121">حدد **فتح**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-121">Select **Open**.</span></span>
10. <span data-ttu-id="1c3b5-122">في الشجرة، حدد **نموذج الدفع**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-122">In the tree, select **Payment model**.</span></span>
11. <span data-ttu-id="1c3b5-123">حدد **استيراد**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-123">Select **Import**.</span></span> <span data-ttu-id="1c3b5-124">قم باستيراد نموذج البيانات هذا.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-124">Import this data model.</span></span> <span data-ttu-id="1c3b5-125">سيتم استخدامه كمصدر بيانات في تكوين تنسيق جديد.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-125">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="1c3b5-126">قم بتخطي هذه الخطوة إذا لم يتم استيراد هذا التكوين الفعل.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-126">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="1c3b5-127">حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-127">Select **Yes**.</span></span>
13. <span data-ttu-id="1c3b5-128">قم بإغلاق الصفحات حتى تعود إلى صفحة التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-128">Close the pages until you return to the Electronic reporting page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="1c3b5-129">قم بإنشاء تكوين تنسيق جديد</span><span class="sxs-lookup"><span data-stu-id="1c3b5-129">Create a new format configuration</span></span>
1. <span data-ttu-id="1c3b5-130">حدد **تكوينات إعداد التقارير‬**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-130">Select **Reporting configurations**.</span></span>
2. <span data-ttu-id="1c3b5-131">في الشجرة، حدد **نموذج الدفع**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-131">In the tree, select **Payment model**.</span></span>
3. <span data-ttu-id="1c3b5-132">حدد **إنشاء تكوين** لفتح مربع الحوار المنسدل.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-132">Select **Create configuration** to open the drop dialog.</span></span>
4. <span data-ttu-id="1c3b5-133">في الحقل **جديد**، أدخل `Format based on data model PaymentModel`.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-133">In the **New** field, enter `Format based on data model PaymentModel`.</span></span> <span data-ttu-id="1c3b5-134">ثم بإنشاء تنسيق يستند إلى نموذج البيانات "PaymentModel".</span><span class="sxs-lookup"><span data-stu-id="1c3b5-134">Create a format that is based on the PaymentModel data model.</span></span>
5. <span data-ttu-id="1c3b5-135">في حقل **الاسم**، اكتب `Sample worksheet report`.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-135">In the **Name** field, type `Sample worksheet report`.</span></span> <span data-ttu-id="1c3b5-136">تقرير ورقة العمل للعينة</span><span class="sxs-lookup"><span data-stu-id="1c3b5-136">Sample worksheet report</span></span>  
6. <span data-ttu-id="1c3b5-137">في حقل **الوصف**، اكتب `Sample worksheet report for vendors' payments`.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-137">In the **Description** field, type `Sample worksheet report for vendors' payments`.</span></span> <span data-ttu-id="1c3b5-138">تقرير ورقة عمل عينة لدفعات الموردين.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-138">Sample worksheet report for vendors' payments.</span></span>  
7. <span data-ttu-id="1c3b5-139">في الحقل **تعريف نموذج البيانات**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-139">In the **Data model definition** field, enter or select a value.</span></span> <span data-ttu-id="1c3b5-140">حدد تعريف **CustomerCreditTransferInitiation**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-140">Select the **CustomerCreditTransferInitiation** definition.</span></span>  
8. <span data-ttu-id="1c3b5-141">حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-141">Select **Create configuration**.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="1c3b5-142">تصميم مستند جديد بتنسيق ورقة عمل OPENXML</span><span class="sxs-lookup"><span data-stu-id="1c3b5-142">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="1c3b5-143">في الشجرة، حدد **نموذج الدفع\تقرير ورقة عمل نموذجي**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-143">In the tree, select **Payment model\Sample worksheet report**.</span></span>
2. <span data-ttu-id="1c3b5-144">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-144">Select **Designer**.</span></span>
3. <span data-ttu-id="1c3b5-145">في جزء الإجراءات، حدد **استيراد**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-145">On the Action Pane, select **Import**.</span></span>
4. <span data-ttu-id="1c3b5-146">حدد **استيراد من Excel**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-146">Select **Import from Excel**.</span></span>
5. <span data-ttu-id="1c3b5-147">حدد **المرفقات**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-147">Select **Attachments**.</span></span> <span data-ttu-id="1c3b5-148">قم بإرفاق مستند Excel كقالب.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-148">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="1c3b5-149">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-149">Select **New**.</span></span>
7. <span data-ttu-id="1c3b5-150">حدد **ملف**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-150">Select **File**.</span></span> <span data-ttu-id="1c3b5-151">قم بالإشارة إلى ملف Excel الموجود.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-151">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="1c3b5-152">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-152">Close the page.</span></span>
9. <span data-ttu-id="1c3b5-153">في حقل **القالب**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-153">In the **Template** field, enter or select a value.</span></span> <span data-ttu-id="1c3b5-154">حدد ملف Excel المرفق ليتم استخدامه كقالب.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-154">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="1c3b5-155">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-155">Select **OK**.</span></span> <span data-ttu-id="1c3b5-156">لاحظ أنه تم إنشاء مكونات تنسيق التقارير الإلكترونية في تنسيق التصميم الذي يستند إلى هيكل مستند MS Excel المرجعي (نطاقات مسماة).</span><span class="sxs-lookup"><span data-stu-id="1c3b5-156">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="1c3b5-157">إنشاء مصدر بيانات جديد لحساب الإجماليات حسب أكواد العملة</span><span class="sxs-lookup"><span data-stu-id="1c3b5-157">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="1c3b5-158">حدد علامة التبويب **تعيين**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-158">Select the **Mapping** tab.</span></span>
2. <span data-ttu-id="1c3b5-159">حدد **إضافة جذر** لفتح مربع الحوار المنسدل.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-159">Select **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="1c3b5-160">في الشجرة، حدد **وظائف\تجميع حسب**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-160">In the tree, select **Functions\Group by**.</span></span>
4. <span data-ttu-id="1c3b5-161">في حقل **الاسم**، اكتب `PaymentByCurrency`.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-161">In the **Name** field, type `PaymentByCurrency`.</span></span>
5. <span data-ttu-id="1c3b5-162">حدد **تحرير تجميع حسب**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-162">Select **Edit group by**.</span></span>
6. <span data-ttu-id="1c3b5-163">في الشجرة، قم بتوسيع **النموذج**، ثم حدد **النموذج\المدفوعات‏‎‏‎**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-163">In the tree, expand **model**, then select **model\Payments**.</span></span>
7. <span data-ttu-id="1c3b5-164">حدد **إضافة حقل إلى**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-164">Select **Add field to**.</span></span>
8. <span data-ttu-id="1c3b5-165">حدد **ما يتم تجميعه**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-165">Select **What to group**.</span></span>
9. <span data-ttu-id="1c3b5-166">في الشجرة، قم بتوسيع **النموذج\المدفوعات‏‎**، ثم حدد **النموذج\المدفوعات‏‎‏‎\العملة**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-166">In the tree, expand **model\Payments**, then select **model\Payments\Currency**.</span></span>
10. <span data-ttu-id="1c3b5-167">حدد **إضافة حقل إلى**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-167">Select **Add field to**.</span></span>
11. <span data-ttu-id="1c3b5-168">حدد **الحقول المجمعة**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-168">Select **Grouped fields**.</span></span>
12. <span data-ttu-id="1c3b5-169">في الشجرة، حدد **النموذج\المدفوعات‏‎‏‎\المبلغ المحدد في الإرشادات(InstructedAmount)**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-169">In the tree, select **model\Payments\Instructed Amount(InstructedAmount)**.</span></span>
13. <span data-ttu-id="1c3b5-170">حدد **إضافة حقل إلى**، ثم حدد **حقول التجميع**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-170">Select **Add field to**, then select **Aggregation fields**.</span></span>
14. <span data-ttu-id="1c3b5-171">في الحقل **الأسلوب**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-171">In the **Method** field, select an option.</span></span> <span data-ttu-id="1c3b5-172">حدد دالة **التجميع SUM**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-172">Select the **SUM aggregation** function.</span></span>  
15. <span data-ttu-id="1c3b5-173">في حقل **الاسم**، اكتب `TotalInstructuredAmount`.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-173">In the **Name** field, type `TotalInstructuredAmount`.</span></span>
16. <span data-ttu-id="1c3b5-174">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-174">Select **Save**.</span></span>
17. <span data-ttu-id="1c3b5-175">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-175">Close the page.</span></span>
18. <span data-ttu-id="1c3b5-176">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-176">Select **OK**.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="1c3b5-177">تعيين مكونات التنسيق بمصادر البيانات</span><span class="sxs-lookup"><span data-stu-id="1c3b5-177">Map format components to data sources</span></span>
1. <span data-ttu-id="1c3b5-178">في الشجرة، حدد **النموذج\المدفوعات‏‎‏‎\الطرف البادئ‬(InitiatingParty)\الاسم** و **Excel\ReportHeader\CompanyName**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-178">In the tree, select **model\Payments\Initiating Party(InitiatingParty)\Name** and **Excel\ReportHeader\CompanyName**.</span></span>
2. <span data-ttu-id="1c3b5-179">حدد **ربط**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-179">Select **Bind**.</span></span>
3. <span data-ttu-id="1c3b5-180">في الشجرة، حدد **النموذج\المدفوعات‏‎‏‎\الدائن‬\التعريف\معرف المصدر‬(SourceID)** و **Excel\PaymLines\VendAccountName**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-180">In the tree, select **model\Payments\Creditor\Identification\Source ID(SourceID)** and **Excel\PaymLines\VendAccountName**.</span></span>
4. <span data-ttu-id="1c3b5-181">حدد **ربط**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-181">Select **Bind**.</span></span>
5. <span data-ttu-id="1c3b5-182">في الشجرة، حدد **النموذج\المدفوعات\الدائن‬\الاسم** و **Excel\PaymLines\VendName**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-182">In the tree, select **model\Payments\Creditor\Name** and **Excel\PaymLines\VendName**.</span></span>
6. <span data-ttu-id="1c3b5-183">حدد **ربط**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-183">Select **Bind**.</span></span>
7. <span data-ttu-id="1c3b5-184">في الشجرة، حدد **النموذج\المدفوعات\وكيل دائن‬(CreditorAgent)‬\الاسم** و **Excel\PaymLines\Bank**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-184">In the tree, select **model\Payments\Creditor Agent(CreditorAgent)\Name** and **Excel\PaymLines\Bank**.</span></span>
8. <span data-ttu-id="1c3b5-185">حدد **ربط**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-185">Select **Bind**.</span></span>
9. <span data-ttu-id="1c3b5-186">في الشجرة، حدد **النموذج\المدفوعات\وكيل دائن‬(CreditorAgent)‬\رقم التوجيه(RoutingNumber)** و **Excel\PaymLines\RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-186">In the tree, select **model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)** and **Excel\PaymLines\RoutingNumber**.</span></span>
10. <span data-ttu-id="1c3b5-187">حدد **ربط**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-187">Select **Bind**.</span></span>
11. <span data-ttu-id="1c3b5-188">في الشجرة، حدد **النموذج\المدفوعات\حساب الدائن(CreditorAccount)\تعريف\رقم** و **Excel\PaymLines\AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-188">In the tree, select **model\Payments\Creditor Account(CreditorAccount)\Identification\Number** and **Excel\PaymLines\AccountNumber**.</span></span>
12. <span data-ttu-id="1c3b5-189">حدد **ربط**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-189">Select **Bind**.</span></span>
13. <span data-ttu-id="1c3b5-190">في الشجرة، حدد **النموذج\المدفوعات\المبلغ المحدد في الإرشادات(InstructedAmount)** و **Excel\PaymLines\Debit**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-190">In the tree, select **model\Payments\Instructed Amount(InstructedAmount)** and **Excel\PaymLines\Debit**.</span></span>
14. <span data-ttu-id="1c3b5-191">حدد **ربط**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-191">Select **Bind**.</span></span>
15. <span data-ttu-id="1c3b5-192">في الشجرة، حدد **النموذج\المدفوعات\العملة** و **Excel\PaymLines\Currency‎**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-192">In the tree, select **model\Payments\Currency** and **Excel\PaymLines\Currency**.</span></span>
16. <span data-ttu-id="1c3b5-193">حدد **ربط**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-193">Select **Bind**.</span></span>
17. <span data-ttu-id="1c3b5-194">في الشجرة، حدد **PaymentByCurrency\مجمعة\العملة** و **Excel\SummaryLines\SummaryCurrency**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-194">In the tree, select **PaymentByCurrency\grouped\Currency** and **Excel\SummaryLines\SummaryCurrency**.</span></span>
18. <span data-ttu-id="1c3b5-195">حدد **ربط**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-195">Select **Bind**.</span></span>
19. <span data-ttu-id="1c3b5-196">في الشجرة، حدد **PaymentByCurrency\مجمعة\TotalInstructuredAmount** و **Excel\SummaryLines\SummaryAmount**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-196">In the tree, select **PaymentByCurrency\aggregated\TotalInstructuredAmount** and **Excel\SummaryLines\SummaryAmount**.</span></span>
20. <span data-ttu-id="1c3b5-197">حدد **ربط**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-197">Select **Bind**.</span></span>
21. <span data-ttu-id="1c3b5-198">في الشجرة، حدد **PaymentByCurrency** و **Excel\SummaryLines**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-198">In the tree, select **PaymentByCurrency** and **Excel\SummaryLines**.</span></span>
22. <span data-ttu-id="1c3b5-199">حدد **ربط**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-199">Select **Bind**.</span></span>
23. <span data-ttu-id="1c3b5-200">في الشجرة، حدد **النموذج\المدفوعات** و **Excel\PaymLines‎**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-200">In the tree, select **model\Payments** and **Excel\PaymLines**.</span></span>
24. <span data-ttu-id="1c3b5-201">حدد **ربط**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-201">Select **Bind**.</span></span>
25. <span data-ttu-id="1c3b5-202">حدد **حفظ** ثم قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-202">Select **Save**, then close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="1c3b5-203">استخدام التكوين الذي تم إنشاؤه لمعالجة المدفوعات</span><span class="sxs-lookup"><span data-stu-id="1c3b5-203">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="1c3b5-204">حدد **تغيير الحالة**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-204">Select **Change status**.</span></span>
2. <span data-ttu-id="1c3b5-205">حدد **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-205">Select **Complete**.</span></span>
3. <span data-ttu-id="1c3b5-206">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-206">Select **OK**.</span></span>
4. <span data-ttu-id="1c3b5-207">في جزء التنقل، انتقل إلى **الوحدات النمطية‬ > حسابات دائنة > إعداد المدفوعات‬ > طرق الدفع‬**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-207">In the navigation pane, go to **Modules > Accounts payable > Payment setup > Methods of payment**.</span></span>
5. <span data-ttu-id="1c3b5-208">استخدم عامل التصفية السريع لإجراء التصفية على حقل **طريقة الدفع** مع القيمة **إلكتروني**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-208">Use the Quick Filter to filter on the **Method of payment** field with a value of **Electronic**.</span></span>
6. <span data-ttu-id="1c3b5-209">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-209">Select **Edit**.</span></span>
7. <span data-ttu-id="1c3b5-210">وسّع قسم **تنسيقات الملفات**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-210">Expand the **File formats** section.</span></span>
8. <span data-ttu-id="1c3b5-211">حدد **نعم** في الحقل **التقارير الإلكترونية العامة**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-211">Select **Yes** in the **Generic electronic reporting** field.</span></span>
9. <span data-ttu-id="1c3b5-212">أدخل قيمة أو حددها في الحقل **تصدير تكوين التنسيق‬**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-212">In the **Export format configuration** field, enter or select a value.</span></span> <span data-ttu-id="1c3b5-213">حدد تكوين **تقرير ورقة عمل العينة**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-213">Select the **Sample worksheet report** configuration.</span></span>  
10. <span data-ttu-id="1c3b5-214">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-214">Select **Save**.</span></span>
11. <span data-ttu-id="1c3b5-215">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-215">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="1c3b5-216">استخدم التكوين الذي تم إنشاؤه لاختبار معالجة دفاتر يومية الدفعات</span><span class="sxs-lookup"><span data-stu-id="1c3b5-216">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="1c3b5-217">في جزء التنقل، انتقل إلى **الوحدات النمطية > الحسابات الدائنة > المدفوعات > دفتر يومية المدفوعات‬**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-217">In the navigation pane, go to **Modules > Accounts payable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="1c3b5-218">حدد **جديد** لإنشاء دفتر يوميات مدفوعات جديد.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-218">Select **New** to create a new payment journal.</span></span>
3. <span data-ttu-id="1c3b5-219">في حقل **الاسم**، اكتب **VendPay**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-219">In the **Name** field, type **VendPay**.</span></span>
4. <span data-ttu-id="1c3b5-220">حدد **البنود**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-220">Select **Lines**.</span></span>
5. <span data-ttu-id="1c3b5-221">في حقل **الحساب**، حدد القيم `GB_SI_000001`.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-221">In the **Account** field, specify the values `GB_SI_000001`.</span></span>
6. <span data-ttu-id="1c3b5-222">عيّن **مدين‬** إلى `1000`.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-222">Set **Debit** to `1000`.</span></span>
7. <span data-ttu-id="1c3b5-223">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-223">Select **New**.</span></span>
8. <span data-ttu-id="1c3b5-224">في حقل **الحساب**، حدد القيم `GB_SI_000005`.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-224">In the **Account** field, specify the values `GB_SI_000005`.</span></span>
9. <span data-ttu-id="1c3b5-225">عيّن **مدين‬** إلى `2000`.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-225">Set **Debit** to `2000`.</span></span>
10. <span data-ttu-id="1c3b5-226">في الحقل **العملة**، اكتب `EUR`.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-226">In the **Currency** field, type `EUR`.</span></span>
11. <span data-ttu-id="1c3b5-227">في الحقل **الحساب المقابل**، حدد القيم `GBSI OPER`.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-227">In the **Offset account** field, specify the values `GBSI OPER`.</span></span>
12. <span data-ttu-id="1c3b5-228">في حقل **طريقة الدفع**، اكتب `Electronic`.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-228">In the **Method of payment** field, type `Electronic`.</span></span>
13. <span data-ttu-id="1c3b5-229">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-229">Select **Save**.</span></span>
14. <span data-ttu-id="1c3b5-230">حدد **إنشاء المدفوعات**.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-230">Select **Generate payments**.</span></span>
15. <span data-ttu-id="1c3b5-231">في حقل **طريقة الدفع**، اكتب `Electronic`.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-231">In the **Method of payment** field, type `Electronic`.</span></span>
16. <span data-ttu-id="1c3b5-232">في حقل **اسم الملف**، اكتب `Payments`.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-232">In the **File name** field, type `Payments`.</span></span>
17. <span data-ttu-id="1c3b5-233">في الحقل **حساب بنكي**، اكتب `GBSI OPER`.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-233">In the **Bank account** field, type `GBSI OPER`.</span></span>
18. <span data-ttu-id="1c3b5-234">حدد **موافق**، ثم حدد **موافق** من جديد.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-234">Select **OK**, then select **OK** again.</span></span> <span data-ttu-id="1c3b5-235">قم بمراجعة ورقة العمل التي تم إنشاؤها، بما في ذلك تفاصيل بنود الدفع بالإضافة إلى الإجماليات لكل كود عملة مستخدم في رسالة الدفع هذه.</span><span class="sxs-lookup"><span data-stu-id="1c3b5-235">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
