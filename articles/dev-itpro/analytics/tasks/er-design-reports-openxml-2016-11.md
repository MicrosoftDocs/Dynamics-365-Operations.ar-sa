--- 
title: "تصميم تكوين لإنشاء تقارير بتنسيق OpenXML للتقارير الإلكترونية (ER)"
description: "تشرح الخطوات التالية كيف يمكن لمستخدم بدور مسؤول النظام أو مطور التقارير الإلكترونية إنشاء تكوين تقارير إلكترونية جديد يحتوي على قالب لإنشاء المستندات الإلكترونية بتنسيق OPENXML."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8bbdbf882f6f73d03be0a036cb975109396e4a0d
ms.openlocfilehash: 09789957839097ba2898544102af908c198090c7
ms.contentlocale: ar-sa
ms.lasthandoff: 11/14/2017

---
# <a name="design-a-configuration-for-generating-reports-in-openxml-format-for-electronic-reporting-er"></a><span data-ttu-id="2bd96-103">تصميم تكوين لإنشاء تقارير بتنسيق OpenXML للتقارير الإلكترونية (ER)</span><span class="sxs-lookup"><span data-stu-id="2bd96-103">Design a configuration for generating reports in OpenXML format for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2bd96-104">تشرح الخطوات التالية كيف يمكن لمستخدم بدور مسؤول النظام أو مطور التقارير الإلكترونية إنشاء تكوين تقارير إلكترونية جديد يحتوي على قالب لإنشاء المستندات الإلكترونية بتنسيق OPENXML.</span><span class="sxs-lookup"><span data-stu-id="2bd96-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="2bd96-105">سيتم استخدام هذا التكوين لمعالجة مدفوعات المورد.</span><span class="sxs-lookup"><span data-stu-id="2bd96-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="2bd96-106">في هذا المثال، ستقوم بإنشاء تكوين لشركة نمودجية، .Litware, Inc ويمكن تنفيذ هذه الخطوات في شركة GBSI.</span><span class="sxs-lookup"><span data-stu-id="2bd96-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="2bd96-107">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "إنشاء موفر تكوين ووضع علامة عليه على أنه نشط".</span><span class="sxs-lookup"><span data-stu-id="2bd96-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="2bd96-108">يجب أيضًا تنزيل الملف من نوع Microsoft Excel وحفظه، [قالب تقرير الدفع](https://go.microsoft.com/fwlink/?linkid=862266).</span><span class="sxs-lookup"><span data-stu-id="2bd96-108">You must also download and save the Microsoft Excel file, [Template of Payment Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span> 

## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="2bd96-109">تحميل تكوين نموذج بيانات الدفعات</span><span class="sxs-lookup"><span data-stu-id="2bd96-109">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="2bd96-110">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="2bd96-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="2bd96-111">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="2bd96-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="2bd96-112">حدد موفر تكوين الشركة النموذجية، Litware, Inc. إذا لم تشاهد موفر التكوين هذا، فيجب أولاً إكمال الخطوات المذكورة في الإجراء "إنشاء موفر تكوين ووضع علامة عليه على أنه نشط‬".</span><span class="sxs-lookup"><span data-stu-id="2bd96-112">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="2bd96-113">انقر فوق "تعيين كنشط".</span><span class="sxs-lookup"><span data-stu-id="2bd96-113">Click Set active.</span></span>
4. <span data-ttu-id="2bd96-114">انقر فوق "المستودعات".</span><span class="sxs-lookup"><span data-stu-id="2bd96-114">Click Repositories.</span></span>
    * <span data-ttu-id="2bd96-115">حدد مستودعًا لنوع موارد Operations، إذا كان متوفرًا.</span><span class="sxs-lookup"><span data-stu-id="2bd96-115">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="2bd96-116">إذا كان متوفرًا، قم بتخطي الخطوات التالية حول إنشاء مستودع جديد.</span><span class="sxs-lookup"><span data-stu-id="2bd96-116">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="2bd96-117">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="2bd96-117">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="2bd96-118">في الحقل "نوع مستودع التكوين"، أدخل "موارد العمليات".</span><span class="sxs-lookup"><span data-stu-id="2bd96-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="2bd96-119">انقر فوق إنشاء مستودع.</span><span class="sxs-lookup"><span data-stu-id="2bd96-119">Click Create repository.</span></span>
8. <span data-ttu-id="2bd96-120">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="2bd96-120">Click OK.</span></span>
9. <span data-ttu-id="2bd96-121">انقر فوق "فتح".</span><span class="sxs-lookup"><span data-stu-id="2bd96-121">Click Open.</span></span>
10. <span data-ttu-id="2bd96-122">في الشجرة، حدد "نموذج الدفع".</span><span class="sxs-lookup"><span data-stu-id="2bd96-122">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="2bd96-123">انقر فوق "استيراد".</span><span class="sxs-lookup"><span data-stu-id="2bd96-123">Click Import.</span></span>
    * <span data-ttu-id="2bd96-124">قم باستيراد نموذج البيانات هذا.</span><span class="sxs-lookup"><span data-stu-id="2bd96-124">Import this data model.</span></span> <span data-ttu-id="2bd96-125">سيتم استخدامه كمصدر بيانات في تكوين تنسيق جديد.</span><span class="sxs-lookup"><span data-stu-id="2bd96-125">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="2bd96-126">قم بتخطي هذه الخطوة إذا لم يتم استيراد هذا التكوين الفعل.</span><span class="sxs-lookup"><span data-stu-id="2bd96-126">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="2bd96-127">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="2bd96-127">Click Yes.</span></span>
13. <span data-ttu-id="2bd96-128">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2bd96-128">Close the page.</span></span>
14. <span data-ttu-id="2bd96-129">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2bd96-129">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="2bd96-130">قم بإنشاء تكوين تنسيق جديد</span><span class="sxs-lookup"><span data-stu-id="2bd96-130">Create a new format configuration</span></span>
1. <span data-ttu-id="2bd96-131">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="2bd96-131">Click Reporting configurations.</span></span>
2. <span data-ttu-id="2bd96-132">في الشجرة، حدد "نموذج الدفع".</span><span class="sxs-lookup"><span data-stu-id="2bd96-132">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="2bd96-133">انقر فوق "إنشاء تكوين" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="2bd96-133">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="2bd96-134">في الحقل "جديد"، أدخل 'التنسيق استناداً إلى نموذج الدفع الخاص بنموذج البيانات".</span><span class="sxs-lookup"><span data-stu-id="2bd96-134">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="2bd96-135">ثم بإنشاء تنسيق يستند إلى نموذج البيانات "PaymentModel".</span><span class="sxs-lookup"><span data-stu-id="2bd96-135">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="2bd96-136">في الحقل "الاسم"، اكتب "تقرير ورقة عمل العينة".</span><span class="sxs-lookup"><span data-stu-id="2bd96-136">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="2bd96-137">تقرير ورقة العمل للعينة</span><span class="sxs-lookup"><span data-stu-id="2bd96-137">Sample worksheet report</span></span>  
6. <span data-ttu-id="2bd96-138">في الحقل "الوصف"، اكتب تقرير ورقة عمل عينة لدقعات الموردين".</span><span class="sxs-lookup"><span data-stu-id="2bd96-138">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="2bd96-139">تقرير ورقة عمل عينة لدفعات الموردين.</span><span class="sxs-lookup"><span data-stu-id="2bd96-139">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="2bd96-140">في الحقل "تعريف نموذج البيانات"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2bd96-140">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="2bd96-141">حدد تعريف "CustomerCreditTransferInitiation".</span><span class="sxs-lookup"><span data-stu-id="2bd96-141">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="2bd96-142">وانقر فوق إنشاء تكوين.</span><span class="sxs-lookup"><span data-stu-id="2bd96-142">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="2bd96-143">تصميم مستند جديد بتنسيق ورقة عمل OPENXML</span><span class="sxs-lookup"><span data-stu-id="2bd96-143">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="2bd96-144">في الشجرة، حدد "Payment model\Sample worksheet report".</span><span class="sxs-lookup"><span data-stu-id="2bd96-144">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="2bd96-145">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="2bd96-145">Click Designer.</span></span>
3. <span data-ttu-id="2bd96-146">في جزء الإجراءات، انقر فوق "استيراد".</span><span class="sxs-lookup"><span data-stu-id="2bd96-146">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="2bd96-147">انقر فوق استيراد من "Excel".</span><span class="sxs-lookup"><span data-stu-id="2bd96-147">Click Import from Excel.</span></span>
5. <span data-ttu-id="2bd96-148">انقر فوق "المرفقات".</span><span class="sxs-lookup"><span data-stu-id="2bd96-148">Click Attachments.</span></span>
    * <span data-ttu-id="2bd96-149">قم بإرفاق مستند Excel كقالب.</span><span class="sxs-lookup"><span data-stu-id="2bd96-149">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="2bd96-150">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="2bd96-150">Click New.</span></span>
7. <span data-ttu-id="2bd96-151">انقر فوق "ملف".</span><span class="sxs-lookup"><span data-stu-id="2bd96-151">Click File.</span></span>
    * <span data-ttu-id="2bd96-152">قم بالإشارة إلى ملف Excel الموجود.</span><span class="sxs-lookup"><span data-stu-id="2bd96-152">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="2bd96-153">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2bd96-153">Close the page.</span></span>
9. <span data-ttu-id="2bd96-154">في حقل "القالب"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2bd96-154">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="2bd96-155">حدد ملف Excel المرفق ليتم استخدامه كقالب.</span><span class="sxs-lookup"><span data-stu-id="2bd96-155">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="2bd96-156">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="2bd96-156">Click OK.</span></span>
    * <span data-ttu-id="2bd96-157">لاحظ أنه تم إنشاء مكونات تنسيق التقارير الإلكترونية في تنسيق التصميم الذي يستند إلى هيكل مستند MS Excel المرجعي (نطاقات مسماة).</span><span class="sxs-lookup"><span data-stu-id="2bd96-157">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="2bd96-158">إنشاء مصدر بيانات جديد لحساب الإجماليات حسب أكواد العملة</span><span class="sxs-lookup"><span data-stu-id="2bd96-158">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="2bd96-159">انقر فوق علامة التبويب "التعيين".</span><span class="sxs-lookup"><span data-stu-id="2bd96-159">Click the Mapping tab.</span></span>
2. <span data-ttu-id="2bd96-160">انقر فوق "إضافة جذر" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="2bd96-160">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="2bd96-161">في الشجرة، حدد "Functions\Group by".</span><span class="sxs-lookup"><span data-stu-id="2bd96-161">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="2bd96-162">في الحقل "اسم"، اكتب "PaymentByCurrency".</span><span class="sxs-lookup"><span data-stu-id="2bd96-162">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="2bd96-163">PaymentByCurrency</span><span class="sxs-lookup"><span data-stu-id="2bd96-163">PaymentByCurrency</span></span>  
5. <span data-ttu-id="2bd96-164">انقر فوق تحرير تجميع حسب.</span><span class="sxs-lookup"><span data-stu-id="2bd96-164">Click Edit group by.</span></span>
6. <span data-ttu-id="2bd96-165">في الشجرة ، قم بتوسيع "النموذج"</span><span class="sxs-lookup"><span data-stu-id="2bd96-165">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="2bd96-166">في الشجرة، حدد "النموذج/المدفوعات".</span><span class="sxs-lookup"><span data-stu-id="2bd96-166">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="2bd96-167">انقر فوق إضافة حقل إلى.</span><span class="sxs-lookup"><span data-stu-id="2bd96-167">Click Add field to.</span></span>
9. <span data-ttu-id="2bd96-168">انقر فوق ما يتم تجميعه.</span><span class="sxs-lookup"><span data-stu-id="2bd96-168">Click What to group.</span></span>
10. <span data-ttu-id="2bd96-169">في الشجرة، قم بتوسيع "النموذج/المدفوعات".</span><span class="sxs-lookup"><span data-stu-id="2bd96-169">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="2bd96-170">في الشجرة، حدد "model\Payments\Currency".</span><span class="sxs-lookup"><span data-stu-id="2bd96-170">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="2bd96-171">انقر فوق إضافة حقل إلى.</span><span class="sxs-lookup"><span data-stu-id="2bd96-171">Click Add field to.</span></span>
13. <span data-ttu-id="2bd96-172">انقر فوق "الحقول مجمعَة".</span><span class="sxs-lookup"><span data-stu-id="2bd96-172">Click Grouped fields.</span></span>
14. <span data-ttu-id="2bd96-173">في الشجرة، حدد "model\Payments\Instructed Amount(InstructedAmount)".</span><span class="sxs-lookup"><span data-stu-id="2bd96-173">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="2bd96-174">انقر فوق إضافة حقل إلى.</span><span class="sxs-lookup"><span data-stu-id="2bd96-174">Click Add field to.</span></span>
16. <span data-ttu-id="2bd96-175">انقر فوق حقول التجميع.</span><span class="sxs-lookup"><span data-stu-id="2bd96-175">Click Aggregation fields.</span></span>
17. <span data-ttu-id="2bd96-176">في الحقل "الأسلوب‬"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="2bd96-176">In the Method field, select an option.</span></span>
    * <span data-ttu-id="2bd96-177">حدد دالة التجميع SUM.</span><span class="sxs-lookup"><span data-stu-id="2bd96-177">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="2bd96-178">في الحقل "اسم"، اكتب "TotalInstructuredAmount".</span><span class="sxs-lookup"><span data-stu-id="2bd96-178">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="2bd96-179">TotalInstructuredAmount</span><span class="sxs-lookup"><span data-stu-id="2bd96-179">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="2bd96-180">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="2bd96-180">Click Save.</span></span>
20. <span data-ttu-id="2bd96-181">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2bd96-181">Close the page.</span></span>
21. <span data-ttu-id="2bd96-182">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="2bd96-182">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="2bd96-183">تعيين مكونات التنسيق بمصادر البيانات</span><span class="sxs-lookup"><span data-stu-id="2bd96-183">Map format components to data sources</span></span>
1. <span data-ttu-id="2bd96-184">في الشجرة ، قم بتوسيع "النموذج"</span><span class="sxs-lookup"><span data-stu-id="2bd96-184">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="2bd96-185">في الشجرة، قم بتوسيع "النموذج/المدفوعات".</span><span class="sxs-lookup"><span data-stu-id="2bd96-185">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="2bd96-186">في الشجرة، قم بتوسيع "model\Payments\Initiating Party(InitiatingParty)".</span><span class="sxs-lookup"><span data-stu-id="2bd96-186">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="2bd96-187">في الشجرة، حدد "model\Payments\Initiating Party(InitiatingParty)\Name".</span><span class="sxs-lookup"><span data-stu-id="2bd96-187">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="2bd96-188">في الشجرة، قم بتوسيع "Excel\ReportHeader".</span><span class="sxs-lookup"><span data-stu-id="2bd96-188">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="2bd96-189">في الشجرة، حدد "Excel\ReportHeader\CompanyName".</span><span class="sxs-lookup"><span data-stu-id="2bd96-189">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="2bd96-190">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="2bd96-190">Click Bind.</span></span>
8. <span data-ttu-id="2bd96-191">في الشجرة، قم بتوسيع "النموذج/المدفوعات/الدائن".</span><span class="sxs-lookup"><span data-stu-id="2bd96-191">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="2bd96-192">في الشجرة، قم بتوسيع "model\Payments\Creditor\Identification".</span><span class="sxs-lookup"><span data-stu-id="2bd96-192">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="2bd96-193">في الشجرة، حدد "model\Payments\Creditor\Identification\Source ID(SourceID)".</span><span class="sxs-lookup"><span data-stu-id="2bd96-193">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="2bd96-194">في الشجرة، قم بتوسيع "Excel\PaymLines".</span><span class="sxs-lookup"><span data-stu-id="2bd96-194">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="2bd96-195">في الشجرة، حدد "Excel\PaymLines\VendAccountName".</span><span class="sxs-lookup"><span data-stu-id="2bd96-195">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="2bd96-196">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="2bd96-196">Click Bind.</span></span>
14. <span data-ttu-id="2bd96-197">في الشجرة، حدد "النموذج/المدفوعات/الدائن/الاسم".</span><span class="sxs-lookup"><span data-stu-id="2bd96-197">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="2bd96-198">في الشجرة، حدد "Excel\PaymLines\VendName".</span><span class="sxs-lookup"><span data-stu-id="2bd96-198">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="2bd96-199">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="2bd96-199">Click Bind.</span></span>
17. <span data-ttu-id="2bd96-200">في الشجرة، قم بتوسيع "model\Payments\Creditor Agent(CreditorAgent)".</span><span class="sxs-lookup"><span data-stu-id="2bd96-200">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="2bd96-201">في الشجرة، حدد "model\Payments\Creditor Agent(CreditorAgent)\Name".</span><span class="sxs-lookup"><span data-stu-id="2bd96-201">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="2bd96-202">في الشجرة، حدد "Excel\PaymLines\Bank".</span><span class="sxs-lookup"><span data-stu-id="2bd96-202">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="2bd96-203">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="2bd96-203">Click Bind.</span></span>
21. <span data-ttu-id="2bd96-204">في الشجرة، حدد "model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)".</span><span class="sxs-lookup"><span data-stu-id="2bd96-204">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="2bd96-205">في الشجرة، حدد "Excel\PaymLines\RoutingNumber".</span><span class="sxs-lookup"><span data-stu-id="2bd96-205">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="2bd96-206">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="2bd96-206">Click Bind.</span></span>
24. <span data-ttu-id="2bd96-207">في الشجرة ، قم بتوسيع "النموذج/المدفوعات/حساب الدائن(CreditorAccount)".</span><span class="sxs-lookup"><span data-stu-id="2bd96-207">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="2bd96-208">في الشجرة ، قم بتوسيع "النموذج/المدفوعات/حساب الدائن(CreditorAccount)/هوية".</span><span class="sxs-lookup"><span data-stu-id="2bd96-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="2bd96-209">في الشجرة، حدد "model\Payments\Creditor Account(CreditorAccount)\Identification\Number".</span><span class="sxs-lookup"><span data-stu-id="2bd96-209">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="2bd96-210">في الشجرة، حدد "Excel\PaymLines\AccountNumber".</span><span class="sxs-lookup"><span data-stu-id="2bd96-210">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="2bd96-211">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="2bd96-211">Click Bind.</span></span>
29. <span data-ttu-id="2bd96-212">في الشجرة، حدد "model\Payments\Instructed Amount(InstructedAmount)".</span><span class="sxs-lookup"><span data-stu-id="2bd96-212">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="2bd96-213">في الشجرة، حدد "Excel\PaymLines\Debit".</span><span class="sxs-lookup"><span data-stu-id="2bd96-213">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="2bd96-214">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="2bd96-214">Click Bind.</span></span>
32. <span data-ttu-id="2bd96-215">في الشجرة، قم بتوسيع "النموذج/المدفوعات/الدائن".</span><span class="sxs-lookup"><span data-stu-id="2bd96-215">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="2bd96-216">في الشجرة ، قم بتوسيع "النموذج/المدفوعات/حساب الدائن(CreditorAccount)".</span><span class="sxs-lookup"><span data-stu-id="2bd96-216">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="2bd96-217">في الشجرة، قم بتوسيع "model\Payments\Creditor Agent(CreditorAgent)".</span><span class="sxs-lookup"><span data-stu-id="2bd96-217">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="2bd96-218">في الشجرة، حدد "model\Payments\Currency".</span><span class="sxs-lookup"><span data-stu-id="2bd96-218">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="2bd96-219">في الشجرة، حدد "Excel\PaymLines\العملة".</span><span class="sxs-lookup"><span data-stu-id="2bd96-219">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="2bd96-220">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="2bd96-220">Click Bind.</span></span>
38. <span data-ttu-id="2bd96-221">في الشجرة، قم بتوسيع "PaymentByCurrency".</span><span class="sxs-lookup"><span data-stu-id="2bd96-221">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="2bd96-222">في الشجرة، قم بتوسيع "PaymentByCurrency\grouped".</span><span class="sxs-lookup"><span data-stu-id="2bd96-222">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="2bd96-223">في الشجرة، حدد "PaymentByCurrency\grouped\Currency".</span><span class="sxs-lookup"><span data-stu-id="2bd96-223">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="2bd96-224">في الشجرة، قم بتوسيع "Excel\SummaryLines".</span><span class="sxs-lookup"><span data-stu-id="2bd96-224">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="2bd96-225">في الشجرة، حدد "Excel\SummaryLines\SummaryCurrency".</span><span class="sxs-lookup"><span data-stu-id="2bd96-225">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="2bd96-226">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="2bd96-226">Click Bind.</span></span>
44. <span data-ttu-id="2bd96-227">في الشجرة، قم بتوسيع "PaymentByCurrency\aggregated".</span><span class="sxs-lookup"><span data-stu-id="2bd96-227">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="2bd96-228">في الشجرة، حدد "PaymentByCurrency\aggregated\TotalInstructuredAmount".</span><span class="sxs-lookup"><span data-stu-id="2bd96-228">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="2bd96-229">في الشجرة، حدد "Excel\SummaryLines\SummaryAmount".</span><span class="sxs-lookup"><span data-stu-id="2bd96-229">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="2bd96-230">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="2bd96-230">Click Bind.</span></span>
48. <span data-ttu-id="2bd96-231">في الشجرة، حدد "PaymentByCurrency".</span><span class="sxs-lookup"><span data-stu-id="2bd96-231">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="2bd96-232">في الشجرة، حدد "Excel\SummaryLines".</span><span class="sxs-lookup"><span data-stu-id="2bd96-232">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="2bd96-233">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="2bd96-233">Click Bind.</span></span>
51. <span data-ttu-id="2bd96-234">في الشجرة، حدد "النموذج/المدفوعات".</span><span class="sxs-lookup"><span data-stu-id="2bd96-234">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="2bd96-235">في الشجرة، حدد "Excel\PaymLines".</span><span class="sxs-lookup"><span data-stu-id="2bd96-235">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="2bd96-236">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="2bd96-236">Click Bind.</span></span>
54. <span data-ttu-id="2bd96-237">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="2bd96-237">Click Save.</span></span>
55. <span data-ttu-id="2bd96-238">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2bd96-238">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="2bd96-239">استخدام التكوين الذي تم إنشاؤه لمعالجة المدفوعات</span><span class="sxs-lookup"><span data-stu-id="2bd96-239">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="2bd96-240">انقر فوق "تغيير الحالة".</span><span class="sxs-lookup"><span data-stu-id="2bd96-240">Click Change status.</span></span>
2. <span data-ttu-id="2bd96-241">انقر فوق "مكتمل".</span><span class="sxs-lookup"><span data-stu-id="2bd96-241">Click Complete.</span></span>
3. <span data-ttu-id="2bd96-242">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="2bd96-242">Click OK.</span></span>
4. <span data-ttu-id="2bd96-243">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2bd96-243">Close the page.</span></span>
5. <span data-ttu-id="2bd96-244">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2bd96-244">Close the page.</span></span>
6. <span data-ttu-id="2bd96-245">انتقل إلى الحسابات المدينة > إعداد الدفع‬ > طرق الدفع.</span><span class="sxs-lookup"><span data-stu-id="2bd96-245">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="2bd96-246">استخدم عامل التصفية السريع لإجراء التصفية على حقل "طريقة الدفع" مع القيمة "إلكتروني".</span><span class="sxs-lookup"><span data-stu-id="2bd96-246">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="2bd96-247">إلكتروني</span><span class="sxs-lookup"><span data-stu-id="2bd96-247">Electronic</span></span>  
8. <span data-ttu-id="2bd96-248">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="2bd96-248">Click Edit.</span></span>
9. <span data-ttu-id="2bd96-249">وسّع قسم المقطع "تنسيقات الملفات".</span><span class="sxs-lookup"><span data-stu-id="2bd96-249">Expand the File formats section.</span></span>
10. <span data-ttu-id="2bd96-250">حدد "نعم" في الحقل "التقارير الإلكترونية العامة‬".</span><span class="sxs-lookup"><span data-stu-id="2bd96-250">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="2bd96-251">في الحقل "تصدير تكوين التنسيق‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2bd96-251">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="2bd96-252">قم بتحديد تكوين "تقرير ورقة عمل العينة".</span><span class="sxs-lookup"><span data-stu-id="2bd96-252">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="2bd96-253">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="2bd96-253">Click Save.</span></span>
13. <span data-ttu-id="2bd96-254">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2bd96-254">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="2bd96-255">استخدم التكوين الذي تم إنشاؤه لاختبار معالجة دفاتر يومية الدفعات</span><span class="sxs-lookup"><span data-stu-id="2bd96-255">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="2bd96-256">انتقل إلى الحسابات الدائنة > المدفوعات‬ > دفتر يومية المدفوعات‬‬.</span><span class="sxs-lookup"><span data-stu-id="2bd96-256">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="2bd96-257">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="2bd96-257">Click New.</span></span>
    * <span data-ttu-id="2bd96-258">إنشاء دفتر يومية مدفوعات جديد.</span><span class="sxs-lookup"><span data-stu-id="2bd96-258">Create a new payment journal.</span></span>  
3. <span data-ttu-id="2bd96-259">في حقل "الاسم"، اكتب "VendPay".</span><span class="sxs-lookup"><span data-stu-id="2bd96-259">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="2bd96-260">VendPay</span><span class="sxs-lookup"><span data-stu-id="2bd96-260">VendPay</span></span>  
4. <span data-ttu-id="2bd96-261">انقر فوق البنود.</span><span class="sxs-lookup"><span data-stu-id="2bd96-261">Click Lines.</span></span>
5. <span data-ttu-id="2bd96-262">في حقل "الحساب"، حدد القيم "GB_SI_000001".</span><span class="sxs-lookup"><span data-stu-id="2bd96-262">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="2bd96-263">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="2bd96-263">GB_SI_000001</span></span>  
6. <span data-ttu-id="2bd96-264">تعيين الخصم على "1000".</span><span class="sxs-lookup"><span data-stu-id="2bd96-264">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="2bd96-265">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="2bd96-265">Click New.</span></span>
8. <span data-ttu-id="2bd96-266">في حقل "الحساب"، حدد القيم "GB_SI_000005".</span><span class="sxs-lookup"><span data-stu-id="2bd96-266">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="2bd96-267">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="2bd96-267">GB_SI_000005</span></span>  
9. <span data-ttu-id="2bd96-268">تعيين الخصم على "2000".</span><span class="sxs-lookup"><span data-stu-id="2bd96-268">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="2bd96-269">في الحقل "العملة"، اكتب "EUR".</span><span class="sxs-lookup"><span data-stu-id="2bd96-269">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="2bd96-270">يورو</span><span class="sxs-lookup"><span data-stu-id="2bd96-270">EUR</span></span>  
11. <span data-ttu-id="2bd96-271">في الحقل "الحساب المقابل"، حدد القيم "GBSI OPER".</span><span class="sxs-lookup"><span data-stu-id="2bd96-271">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="2bd96-272">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="2bd96-272">GBSI OPER</span></span>  
12. <span data-ttu-id="2bd96-273">في الحقل "طريقة الدفع"، اكتب "إلكتروني".</span><span class="sxs-lookup"><span data-stu-id="2bd96-273">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="2bd96-274">إلكتروني</span><span class="sxs-lookup"><span data-stu-id="2bd96-274">Electronic</span></span>  
13. <span data-ttu-id="2bd96-275">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="2bd96-275">Click Save.</span></span>
14. <span data-ttu-id="2bd96-276">انقر فوق إنشاء مدفوعات.</span><span class="sxs-lookup"><span data-stu-id="2bd96-276">Click Generate payments.</span></span>
15. <span data-ttu-id="2bd96-277">في الحقل "طريقة الدفع"، اكتب "إلكتروني".</span><span class="sxs-lookup"><span data-stu-id="2bd96-277">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="2bd96-278">إلكتروني</span><span class="sxs-lookup"><span data-stu-id="2bd96-278">Electronic</span></span>  
16. <span data-ttu-id="2bd96-279">في حقل "اسم الملف"، اكتب "دفعات".</span><span class="sxs-lookup"><span data-stu-id="2bd96-279">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="2bd96-280">على سبيل المثال، اكتب "دفعات".</span><span class="sxs-lookup"><span data-stu-id="2bd96-280">For example, type Payments.</span></span>  
17. <span data-ttu-id="2bd96-281">في الحقل "حساب البنك"، اكتب "GBSI OPER".</span><span class="sxs-lookup"><span data-stu-id="2bd96-281">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="2bd96-282">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="2bd96-282">GBSI OPER</span></span>  
18. <span data-ttu-id="2bd96-283">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="2bd96-283">Click OK.</span></span>
19. <span data-ttu-id="2bd96-284">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="2bd96-284">Click OK.</span></span>
    * <span data-ttu-id="2bd96-285">قم بمراجعة ورقة العمل التي تم إنشاؤها، بما في ذلك تفاصيل بنود الدفع بالإضافة إلى الإجماليات لكل كود عملة مستخدم في رسالة الدفع هذه.</span><span class="sxs-lookup"><span data-stu-id="2bd96-285">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  


