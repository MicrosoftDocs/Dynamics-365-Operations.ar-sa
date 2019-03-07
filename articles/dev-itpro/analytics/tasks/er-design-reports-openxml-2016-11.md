---
title: التقارير الإلكترونية - تصميم تكوين لإنشاء التقارير بتنسيق OPENXML (نوفمبر 2016)
description: تشرح الخطوات التالية كيف يمكن لمستخدم بدور مسؤول النظام أو مطور التقارير الإلكترونية إنشاء تكوين تقارير إلكترونية جديد يحتوي على قالب لإنشاء المستندات الإلكترونية بتنسيق OPENXML.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERModelGroupByFunctionEditor, VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3e6b6b16f202af051ccff02051eb438ea49ff6da
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "326643"
---
# <a name="er-design-a-configuration-for-generating-reports-in-openxml-format-november-2016"></a><span data-ttu-id="21fc0-103">التقارير الإلكترونية - تصميم تكوين لإنشاء التقارير بتنسيق OPENXML (نوفمبر 2016)</span><span class="sxs-lookup"><span data-stu-id="21fc0-103">ER Design a configuration for generating reports in OPENXML format (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="21fc0-104">تشرح الخطوات التالية كيف يمكن لمستخدم بدور مسؤول النظام أو مطور التقارير الإلكترونية إنشاء تكوين تقارير إلكترونية جديد يحتوي على قالب لإنشاء المستندات الإلكترونية بتنسيق OPENXML.</span><span class="sxs-lookup"><span data-stu-id="21fc0-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="21fc0-105">سيتم استخدام هذا التكوين لمعالجة مدفوعات المورد.</span><span class="sxs-lookup"><span data-stu-id="21fc0-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="21fc0-106">في هذا المثال، ستقوم بإنشاء تكوين لشركة نمودجية، .Litware, Inc ويمكن تنفيذ هذه الخطوات في شركة GBSI.</span><span class="sxs-lookup"><span data-stu-id="21fc0-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="21fc0-107">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "إنشاء موفر تكوين ووضع علامة عليه على أنه نشط".</span><span class="sxs-lookup"><span data-stu-id="21fc0-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="21fc0-108">كما يجب أن يكون لديك ملف Excel سيتم استيراده عند إنشاء القالب.</span><span class="sxs-lookup"><span data-stu-id="21fc0-108">You must also have an Excel file which will be imported when creating the template.</span></span> <span data-ttu-id="21fc0-109">يمكن الوصول إلى هذا الملف من [قالب تقرير الدفع](https://go.microsoft.com/fwlink/?linkid=862266).</span><span class="sxs-lookup"><span data-stu-id="21fc0-109">This file can be accessed from the [Template of Payment Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span>


## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="21fc0-110">تحميل تكوين نموذج بيانات الدفعات</span><span class="sxs-lookup"><span data-stu-id="21fc0-110">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="21fc0-111">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="21fc0-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="21fc0-112">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="21fc0-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="21fc0-113">حدد موفر تكوين الشركة النموذجية، Litware, Inc. إذا لم تشاهد موفر التكوين هذا، فيجب أولاً إكمال الخطوات المذكورة في الإجراء "إنشاء موفر تكوين ووضع علامة عليه على أنه نشط‬".</span><span class="sxs-lookup"><span data-stu-id="21fc0-113">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="21fc0-114">انقر فوق "تعيين كنشط".</span><span class="sxs-lookup"><span data-stu-id="21fc0-114">Click Set active.</span></span>
4. <span data-ttu-id="21fc0-115">انقر فوق "المستودعات".</span><span class="sxs-lookup"><span data-stu-id="21fc0-115">Click Repositories.</span></span>
    * <span data-ttu-id="21fc0-116">حدد مستودعًا لنوع موارد Operations، إذا كان متوفرًا.</span><span class="sxs-lookup"><span data-stu-id="21fc0-116">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="21fc0-117">إذا كان متوفرًا، قم بتخطي الخطوات التالية حول إنشاء مستودع جديد.</span><span class="sxs-lookup"><span data-stu-id="21fc0-117">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="21fc0-118">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="21fc0-118">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="21fc0-119">في الحقل "نوع مستودع التكوين"، أدخل "موارد العمليات".</span><span class="sxs-lookup"><span data-stu-id="21fc0-119">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="21fc0-120">انقر فوق إنشاء مستودع.</span><span class="sxs-lookup"><span data-stu-id="21fc0-120">Click Create repository.</span></span>
8. <span data-ttu-id="21fc0-121">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="21fc0-121">Click OK.</span></span>
9. <span data-ttu-id="21fc0-122">انقر فوق "فتح".</span><span class="sxs-lookup"><span data-stu-id="21fc0-122">Click Open.</span></span>
10. <span data-ttu-id="21fc0-123">في الشجرة، حدد "نموذج الدفع".</span><span class="sxs-lookup"><span data-stu-id="21fc0-123">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="21fc0-124">انقر فوق "استيراد".</span><span class="sxs-lookup"><span data-stu-id="21fc0-124">Click Import.</span></span>
    * <span data-ttu-id="21fc0-125">قم باستيراد نموذج البيانات هذا.</span><span class="sxs-lookup"><span data-stu-id="21fc0-125">Import this data model.</span></span> <span data-ttu-id="21fc0-126">سيتم استخدامه كمصدر بيانات في تكوين تنسيق جديد.</span><span class="sxs-lookup"><span data-stu-id="21fc0-126">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="21fc0-127">قم بتخطي هذه الخطوة إذا لم يتم استيراد هذا التكوين الفعل.</span><span class="sxs-lookup"><span data-stu-id="21fc0-127">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="21fc0-128">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="21fc0-128">Click Yes.</span></span>
13. <span data-ttu-id="21fc0-129">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="21fc0-129">Close the page.</span></span>
14. <span data-ttu-id="21fc0-130">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="21fc0-130">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="21fc0-131">قم بإنشاء تكوين تنسيق جديد</span><span class="sxs-lookup"><span data-stu-id="21fc0-131">Create a new format configuration</span></span>
1. <span data-ttu-id="21fc0-132">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="21fc0-132">Click Reporting configurations.</span></span>
2. <span data-ttu-id="21fc0-133">في الشجرة، حدد "نموذج الدفع".</span><span class="sxs-lookup"><span data-stu-id="21fc0-133">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="21fc0-134">انقر فوق "إنشاء تكوين" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="21fc0-134">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="21fc0-135">في الحقل "جديد"، أدخل 'التنسيق استناداً إلى نموذج الدفع الخاص بنموذج البيانات".</span><span class="sxs-lookup"><span data-stu-id="21fc0-135">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="21fc0-136">ثم بإنشاء تنسيق يستند إلى نموذج البيانات "PaymentModel".</span><span class="sxs-lookup"><span data-stu-id="21fc0-136">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="21fc0-137">في الحقل "الاسم"، اكتب "تقرير ورقة عمل العينة".</span><span class="sxs-lookup"><span data-stu-id="21fc0-137">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="21fc0-138">تقرير ورقة العمل للعينة</span><span class="sxs-lookup"><span data-stu-id="21fc0-138">Sample worksheet report</span></span>  
6. <span data-ttu-id="21fc0-139">في الحقل "الوصف"، اكتب تقرير ورقة عمل عينة لدقعات الموردين".</span><span class="sxs-lookup"><span data-stu-id="21fc0-139">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="21fc0-140">تقرير ورقة عمل عينة لدفعات الموردين.</span><span class="sxs-lookup"><span data-stu-id="21fc0-140">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="21fc0-141">في الحقل "تعريف نموذج البيانات"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="21fc0-141">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="21fc0-142">حدد تعريف "CustomerCreditTransferInitiation".</span><span class="sxs-lookup"><span data-stu-id="21fc0-142">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="21fc0-143">وانقر فوق إنشاء تكوين.</span><span class="sxs-lookup"><span data-stu-id="21fc0-143">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="21fc0-144">تصميم مستند جديد بتنسيق ورقة عمل OPENXML</span><span class="sxs-lookup"><span data-stu-id="21fc0-144">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="21fc0-145">في الشجرة، حدد "Payment model\Sample worksheet report".</span><span class="sxs-lookup"><span data-stu-id="21fc0-145">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="21fc0-146">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="21fc0-146">Click Designer.</span></span>
3. <span data-ttu-id="21fc0-147">في جزء الإجراءات، انقر فوق "استيراد".</span><span class="sxs-lookup"><span data-stu-id="21fc0-147">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="21fc0-148">انقر فوق استيراد من "Excel".</span><span class="sxs-lookup"><span data-stu-id="21fc0-148">Click Import from Excel.</span></span>
5. <span data-ttu-id="21fc0-149">انقر فوق "المرفقات".</span><span class="sxs-lookup"><span data-stu-id="21fc0-149">Click Attachments.</span></span>
    * <span data-ttu-id="21fc0-150">قم بإرفاق مستند Excel كقالب.</span><span class="sxs-lookup"><span data-stu-id="21fc0-150">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="21fc0-151">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="21fc0-151">Click New.</span></span>
7. <span data-ttu-id="21fc0-152">انقر فوق "ملف".</span><span class="sxs-lookup"><span data-stu-id="21fc0-152">Click File.</span></span>
    * <span data-ttu-id="21fc0-153">قم بالإشارة إلى ملف Excel الموجود.</span><span class="sxs-lookup"><span data-stu-id="21fc0-153">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="21fc0-154">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="21fc0-154">Close the page.</span></span>
9. <span data-ttu-id="21fc0-155">في حقل "القالب"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="21fc0-155">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="21fc0-156">حدد ملف Excel المرفق ليتم استخدامه كقالب.</span><span class="sxs-lookup"><span data-stu-id="21fc0-156">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="21fc0-157">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="21fc0-157">Click OK.</span></span>
    * <span data-ttu-id="21fc0-158">لاحظ أنه تم إنشاء مكونات تنسيق التقارير الإلكترونية في تنسيق التصميم الذي يستند إلى هيكل مستند MS Excel المرجعي (نطاقات مسماة).</span><span class="sxs-lookup"><span data-stu-id="21fc0-158">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="21fc0-159">إنشاء مصدر بيانات جديد لحساب الإجماليات حسب أكواد العملة</span><span class="sxs-lookup"><span data-stu-id="21fc0-159">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="21fc0-160">انقر فوق علامة التبويب "التعيين".</span><span class="sxs-lookup"><span data-stu-id="21fc0-160">Click the Mapping tab.</span></span>
2. <span data-ttu-id="21fc0-161">انقر فوق "إضافة جذر" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="21fc0-161">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="21fc0-162">في الشجرة، حدد "Functions\Group by".</span><span class="sxs-lookup"><span data-stu-id="21fc0-162">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="21fc0-163">في الحقل "اسم"، اكتب "PaymentByCurrency".</span><span class="sxs-lookup"><span data-stu-id="21fc0-163">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="21fc0-164">PaymentByCurrency</span><span class="sxs-lookup"><span data-stu-id="21fc0-164">PaymentByCurrency</span></span>  
5. <span data-ttu-id="21fc0-165">انقر فوق تحرير تجميع حسب.</span><span class="sxs-lookup"><span data-stu-id="21fc0-165">Click Edit group by.</span></span>
6. <span data-ttu-id="21fc0-166">في الشجرة ، قم بتوسيع "النموذج"</span><span class="sxs-lookup"><span data-stu-id="21fc0-166">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="21fc0-167">في الشجرة، حدد "النموذج/المدفوعات".</span><span class="sxs-lookup"><span data-stu-id="21fc0-167">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="21fc0-168">انقر فوق إضافة حقل إلى.</span><span class="sxs-lookup"><span data-stu-id="21fc0-168">Click Add field to.</span></span>
9. <span data-ttu-id="21fc0-169">انقر فوق ما يتم تجميعه.</span><span class="sxs-lookup"><span data-stu-id="21fc0-169">Click What to group.</span></span>
10. <span data-ttu-id="21fc0-170">في الشجرة، قم بتوسيع "النموذج/المدفوعات".</span><span class="sxs-lookup"><span data-stu-id="21fc0-170">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="21fc0-171">في الشجرة، حدد "model\Payments\Currency".</span><span class="sxs-lookup"><span data-stu-id="21fc0-171">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="21fc0-172">انقر فوق إضافة حقل إلى.</span><span class="sxs-lookup"><span data-stu-id="21fc0-172">Click Add field to.</span></span>
13. <span data-ttu-id="21fc0-173">انقر فوق "الحقول مجمعَة".</span><span class="sxs-lookup"><span data-stu-id="21fc0-173">Click Grouped fields.</span></span>
14. <span data-ttu-id="21fc0-174">في الشجرة، حدد "model\Payments\Instructed Amount(InstructedAmount)".</span><span class="sxs-lookup"><span data-stu-id="21fc0-174">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="21fc0-175">انقر فوق إضافة حقل إلى.</span><span class="sxs-lookup"><span data-stu-id="21fc0-175">Click Add field to.</span></span>
16. <span data-ttu-id="21fc0-176">انقر فوق حقول التجميع.</span><span class="sxs-lookup"><span data-stu-id="21fc0-176">Click Aggregation fields.</span></span>
17. <span data-ttu-id="21fc0-177">في الحقل "الأسلوب‬"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="21fc0-177">In the Method field, select an option.</span></span>
    * <span data-ttu-id="21fc0-178">حدد دالة التجميع SUM.</span><span class="sxs-lookup"><span data-stu-id="21fc0-178">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="21fc0-179">في الحقل "اسم"، اكتب "TotalInstructuredAmount".</span><span class="sxs-lookup"><span data-stu-id="21fc0-179">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="21fc0-180">TotalInstructuredAmount</span><span class="sxs-lookup"><span data-stu-id="21fc0-180">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="21fc0-181">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="21fc0-181">Click Save.</span></span>
20. <span data-ttu-id="21fc0-182">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="21fc0-182">Close the page.</span></span>
21. <span data-ttu-id="21fc0-183">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="21fc0-183">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="21fc0-184">تعيين مكونات التنسيق بمصادر البيانات</span><span class="sxs-lookup"><span data-stu-id="21fc0-184">Map format components to data sources</span></span>
1. <span data-ttu-id="21fc0-185">في الشجرة ، قم بتوسيع "النموذج"</span><span class="sxs-lookup"><span data-stu-id="21fc0-185">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="21fc0-186">في الشجرة، قم بتوسيع "النموذج/المدفوعات".</span><span class="sxs-lookup"><span data-stu-id="21fc0-186">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="21fc0-187">في الشجرة، قم بتوسيع "model\Payments\Initiating Party(InitiatingParty)".</span><span class="sxs-lookup"><span data-stu-id="21fc0-187">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="21fc0-188">في الشجرة، حدد "model\Payments\Initiating Party(InitiatingParty)\Name".</span><span class="sxs-lookup"><span data-stu-id="21fc0-188">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="21fc0-189">في الشجرة، قم بتوسيع "Excel\ReportHeader".</span><span class="sxs-lookup"><span data-stu-id="21fc0-189">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="21fc0-190">في الشجرة، حدد "Excel\ReportHeader\CompanyName".</span><span class="sxs-lookup"><span data-stu-id="21fc0-190">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="21fc0-191">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="21fc0-191">Click Bind.</span></span>
8. <span data-ttu-id="21fc0-192">في الشجرة، قم بتوسيع "النموذج/المدفوعات/الدائن".</span><span class="sxs-lookup"><span data-stu-id="21fc0-192">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="21fc0-193">في الشجرة، قم بتوسيع "model\Payments\Creditor\Identification".</span><span class="sxs-lookup"><span data-stu-id="21fc0-193">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="21fc0-194">في الشجرة، حدد "model\Payments\Creditor\Identification\Source ID(SourceID)".</span><span class="sxs-lookup"><span data-stu-id="21fc0-194">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="21fc0-195">في الشجرة، قم بتوسيع "Excel\PaymLines".</span><span class="sxs-lookup"><span data-stu-id="21fc0-195">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="21fc0-196">في الشجرة، حدد "Excel\PaymLines\VendAccountName".</span><span class="sxs-lookup"><span data-stu-id="21fc0-196">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="21fc0-197">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="21fc0-197">Click Bind.</span></span>
14. <span data-ttu-id="21fc0-198">في الشجرة، حدد "النموذج/المدفوعات/الدائن/الاسم".</span><span class="sxs-lookup"><span data-stu-id="21fc0-198">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="21fc0-199">في الشجرة، حدد "Excel\PaymLines\VendName".</span><span class="sxs-lookup"><span data-stu-id="21fc0-199">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="21fc0-200">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="21fc0-200">Click Bind.</span></span>
17. <span data-ttu-id="21fc0-201">في الشجرة، قم بتوسيع "model\Payments\Creditor Agent(CreditorAgent)".</span><span class="sxs-lookup"><span data-stu-id="21fc0-201">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="21fc0-202">في الشجرة، حدد "model\Payments\Creditor Agent(CreditorAgent)\Name".</span><span class="sxs-lookup"><span data-stu-id="21fc0-202">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="21fc0-203">في الشجرة، حدد "Excel\PaymLines\Bank".</span><span class="sxs-lookup"><span data-stu-id="21fc0-203">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="21fc0-204">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="21fc0-204">Click Bind.</span></span>
21. <span data-ttu-id="21fc0-205">في الشجرة، حدد "model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)".</span><span class="sxs-lookup"><span data-stu-id="21fc0-205">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="21fc0-206">في الشجرة، حدد "Excel\PaymLines\RoutingNumber".</span><span class="sxs-lookup"><span data-stu-id="21fc0-206">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="21fc0-207">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="21fc0-207">Click Bind.</span></span>
24. <span data-ttu-id="21fc0-208">في الشجرة ، قم بتوسيع "النموذج/المدفوعات/حساب الدائن(CreditorAccount)".</span><span class="sxs-lookup"><span data-stu-id="21fc0-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="21fc0-209">في الشجرة ، قم بتوسيع "النموذج/المدفوعات/حساب الدائن(CreditorAccount)/هوية".</span><span class="sxs-lookup"><span data-stu-id="21fc0-209">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="21fc0-210">في الشجرة، حدد "model\Payments\Creditor Account(CreditorAccount)\Identification\Number".</span><span class="sxs-lookup"><span data-stu-id="21fc0-210">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="21fc0-211">في الشجرة، حدد "Excel\PaymLines\AccountNumber".</span><span class="sxs-lookup"><span data-stu-id="21fc0-211">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="21fc0-212">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="21fc0-212">Click Bind.</span></span>
29. <span data-ttu-id="21fc0-213">في الشجرة، حدد "model\Payments\Instructed Amount(InstructedAmount)".</span><span class="sxs-lookup"><span data-stu-id="21fc0-213">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="21fc0-214">في الشجرة، حدد "Excel\PaymLines\Debit".</span><span class="sxs-lookup"><span data-stu-id="21fc0-214">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="21fc0-215">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="21fc0-215">Click Bind.</span></span>
32. <span data-ttu-id="21fc0-216">في الشجرة، قم بتوسيع "النموذج/المدفوعات/الدائن".</span><span class="sxs-lookup"><span data-stu-id="21fc0-216">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="21fc0-217">في الشجرة ، قم بتوسيع "النموذج/المدفوعات/حساب الدائن(CreditorAccount)".</span><span class="sxs-lookup"><span data-stu-id="21fc0-217">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="21fc0-218">في الشجرة، قم بتوسيع "model\Payments\Creditor Agent(CreditorAgent)".</span><span class="sxs-lookup"><span data-stu-id="21fc0-218">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="21fc0-219">في الشجرة، حدد "model\Payments\Currency".</span><span class="sxs-lookup"><span data-stu-id="21fc0-219">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="21fc0-220">في الشجرة، حدد "Excel\PaymLines\العملة".</span><span class="sxs-lookup"><span data-stu-id="21fc0-220">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="21fc0-221">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="21fc0-221">Click Bind.</span></span>
38. <span data-ttu-id="21fc0-222">في الشجرة، قم بتوسيع "PaymentByCurrency".</span><span class="sxs-lookup"><span data-stu-id="21fc0-222">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="21fc0-223">في الشجرة، قم بتوسيع "PaymentByCurrency\grouped".</span><span class="sxs-lookup"><span data-stu-id="21fc0-223">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="21fc0-224">في الشجرة، حدد "PaymentByCurrency\grouped\Currency".</span><span class="sxs-lookup"><span data-stu-id="21fc0-224">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="21fc0-225">في الشجرة، قم بتوسيع "Excel\SummaryLines".</span><span class="sxs-lookup"><span data-stu-id="21fc0-225">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="21fc0-226">في الشجرة، حدد "Excel\SummaryLines\SummaryCurrency".</span><span class="sxs-lookup"><span data-stu-id="21fc0-226">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="21fc0-227">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="21fc0-227">Click Bind.</span></span>
44. <span data-ttu-id="21fc0-228">في الشجرة، قم بتوسيع "PaymentByCurrency\aggregated".</span><span class="sxs-lookup"><span data-stu-id="21fc0-228">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="21fc0-229">في الشجرة، حدد "PaymentByCurrency\aggregated\TotalInstructuredAmount".</span><span class="sxs-lookup"><span data-stu-id="21fc0-229">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="21fc0-230">في الشجرة، حدد "Excel\SummaryLines\SummaryAmount".</span><span class="sxs-lookup"><span data-stu-id="21fc0-230">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="21fc0-231">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="21fc0-231">Click Bind.</span></span>
48. <span data-ttu-id="21fc0-232">في الشجرة، حدد "PaymentByCurrency".</span><span class="sxs-lookup"><span data-stu-id="21fc0-232">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="21fc0-233">في الشجرة، حدد "Excel\SummaryLines".</span><span class="sxs-lookup"><span data-stu-id="21fc0-233">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="21fc0-234">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="21fc0-234">Click Bind.</span></span>
51. <span data-ttu-id="21fc0-235">في الشجرة، حدد "النموذج/المدفوعات".</span><span class="sxs-lookup"><span data-stu-id="21fc0-235">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="21fc0-236">في الشجرة، حدد "Excel\PaymLines".</span><span class="sxs-lookup"><span data-stu-id="21fc0-236">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="21fc0-237">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="21fc0-237">Click Bind.</span></span>
54. <span data-ttu-id="21fc0-238">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="21fc0-238">Click Save.</span></span>
55. <span data-ttu-id="21fc0-239">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="21fc0-239">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="21fc0-240">استخدام التكوين الذي تم إنشاؤه لمعالجة المدفوعات</span><span class="sxs-lookup"><span data-stu-id="21fc0-240">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="21fc0-241">انقر فوق "تغيير الحالة".</span><span class="sxs-lookup"><span data-stu-id="21fc0-241">Click Change status.</span></span>
2. <span data-ttu-id="21fc0-242">انقر فوق "مكتمل".</span><span class="sxs-lookup"><span data-stu-id="21fc0-242">Click Complete.</span></span>
3. <span data-ttu-id="21fc0-243">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="21fc0-243">Click OK.</span></span>
4. <span data-ttu-id="21fc0-244">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="21fc0-244">Close the page.</span></span>
5. <span data-ttu-id="21fc0-245">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="21fc0-245">Close the page.</span></span>
6. <span data-ttu-id="21fc0-246">انتقل إلى الحسابات المدينة > إعداد الدفع‬ > طرق الدفع.</span><span class="sxs-lookup"><span data-stu-id="21fc0-246">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="21fc0-247">استخدم عامل التصفية السريع لإجراء التصفية على حقل "طريقة الدفع" مع القيمة "إلكتروني".</span><span class="sxs-lookup"><span data-stu-id="21fc0-247">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="21fc0-248">إلكتروني</span><span class="sxs-lookup"><span data-stu-id="21fc0-248">Electronic</span></span>  
8. <span data-ttu-id="21fc0-249">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="21fc0-249">Click Edit.</span></span>
9. <span data-ttu-id="21fc0-250">وسّع قسم المقطع "تنسيقات الملفات".</span><span class="sxs-lookup"><span data-stu-id="21fc0-250">Expand the File formats section.</span></span>
10. <span data-ttu-id="21fc0-251">حدد "نعم" في الحقل "التقارير الإلكترونية العامة‬".</span><span class="sxs-lookup"><span data-stu-id="21fc0-251">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="21fc0-252">في الحقل "تصدير تكوين التنسيق‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="21fc0-252">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="21fc0-253">قم بتحديد تكوين "تقرير ورقة عمل العينة".</span><span class="sxs-lookup"><span data-stu-id="21fc0-253">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="21fc0-254">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="21fc0-254">Click Save.</span></span>
13. <span data-ttu-id="21fc0-255">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="21fc0-255">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="21fc0-256">استخدم التكوين الذي تم إنشاؤه لاختبار معالجة دفاتر يومية الدفعات</span><span class="sxs-lookup"><span data-stu-id="21fc0-256">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="21fc0-257">انتقل إلى الحسابات الدائنة > المدفوعات‬ > دفتر يومية المدفوعات‬‬.</span><span class="sxs-lookup"><span data-stu-id="21fc0-257">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="21fc0-258">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="21fc0-258">Click New.</span></span>
    * <span data-ttu-id="21fc0-259">إنشاء دفتر يومية مدفوعات جديد.</span><span class="sxs-lookup"><span data-stu-id="21fc0-259">Create a new payment journal.</span></span>  
3. <span data-ttu-id="21fc0-260">في حقل "الاسم"، اكتب "VendPay".</span><span class="sxs-lookup"><span data-stu-id="21fc0-260">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="21fc0-261">VendPay</span><span class="sxs-lookup"><span data-stu-id="21fc0-261">VendPay</span></span>  
4. <span data-ttu-id="21fc0-262">انقر فوق البنود.</span><span class="sxs-lookup"><span data-stu-id="21fc0-262">Click Lines.</span></span>
5. <span data-ttu-id="21fc0-263">في حقل "الحساب"، حدد القيم "GB_SI_000001".</span><span class="sxs-lookup"><span data-stu-id="21fc0-263">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="21fc0-264">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="21fc0-264">GB_SI_000001</span></span>  
6. <span data-ttu-id="21fc0-265">تعيين الخصم على "1000".</span><span class="sxs-lookup"><span data-stu-id="21fc0-265">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="21fc0-266">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="21fc0-266">Click New.</span></span>
8. <span data-ttu-id="21fc0-267">في حقل "الحساب"، حدد القيم "GB_SI_000005".</span><span class="sxs-lookup"><span data-stu-id="21fc0-267">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="21fc0-268">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="21fc0-268">GB_SI_000005</span></span>  
9. <span data-ttu-id="21fc0-269">تعيين الخصم على "2000".</span><span class="sxs-lookup"><span data-stu-id="21fc0-269">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="21fc0-270">في الحقل "العملة"، اكتب "EUR".</span><span class="sxs-lookup"><span data-stu-id="21fc0-270">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="21fc0-271">يورو</span><span class="sxs-lookup"><span data-stu-id="21fc0-271">EUR</span></span>  
11. <span data-ttu-id="21fc0-272">في الحقل "الحساب المقابل"، حدد القيم "GBSI OPER".</span><span class="sxs-lookup"><span data-stu-id="21fc0-272">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="21fc0-273">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="21fc0-273">GBSI OPER</span></span>  
12. <span data-ttu-id="21fc0-274">في الحقل "طريقة الدفع"، اكتب "إلكتروني".</span><span class="sxs-lookup"><span data-stu-id="21fc0-274">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="21fc0-275">إلكتروني</span><span class="sxs-lookup"><span data-stu-id="21fc0-275">Electronic</span></span>  
13. <span data-ttu-id="21fc0-276">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="21fc0-276">Click Save.</span></span>
14. <span data-ttu-id="21fc0-277">انقر فوق إنشاء مدفوعات.</span><span class="sxs-lookup"><span data-stu-id="21fc0-277">Click Generate payments.</span></span>
15. <span data-ttu-id="21fc0-278">في الحقل "طريقة الدفع"، اكتب "إلكتروني".</span><span class="sxs-lookup"><span data-stu-id="21fc0-278">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="21fc0-279">إلكتروني</span><span class="sxs-lookup"><span data-stu-id="21fc0-279">Electronic</span></span>  
16. <span data-ttu-id="21fc0-280">في حقل "اسم الملف"، اكتب "دفعات".</span><span class="sxs-lookup"><span data-stu-id="21fc0-280">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="21fc0-281">على سبيل المثال، اكتب "دفعات".</span><span class="sxs-lookup"><span data-stu-id="21fc0-281">For example, type Payments.</span></span>  
17. <span data-ttu-id="21fc0-282">في الحقل "حساب البنك"، اكتب "GBSI OPER".</span><span class="sxs-lookup"><span data-stu-id="21fc0-282">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="21fc0-283">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="21fc0-283">GBSI OPER</span></span>  
18. <span data-ttu-id="21fc0-284">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="21fc0-284">Click OK.</span></span>
19. <span data-ttu-id="21fc0-285">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="21fc0-285">Click OK.</span></span>
    * <span data-ttu-id="21fc0-286">قم بمراجعة ورقة العمل التي تم إنشاؤها، بما في ذلك تفاصيل بنود الدفع بالإضافة إلى الإجماليات لكل كود عملة مستخدم في رسالة الدفع هذه.</span><span class="sxs-lookup"><span data-stu-id="21fc0-286">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  

