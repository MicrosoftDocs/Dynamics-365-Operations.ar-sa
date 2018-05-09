--- 
title: "تعديل تنسيق من خلال إعادة تطبيق قالب Microsoft Excel للتقارير الإلكترونية (ER)"
description: "لإكمال الخطوات في هذا الإجراء، يجب أولاً إكمال الإجراء \"التقارير الإلكترونية - تصميم تكوين لإنشاء التقارير بتنسيق OPENXML\"."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 8dcf91ea9555da051afc8ed979aee559f937b29d
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---
# <a name="modify-a-format-by-reapplying-a-microsoft-excel-template-for-electronic-reporting-er"></a><span data-ttu-id="a91c8-103">تعديل تنسيق من خلال إعادة تطبيق قالب Microsoft Excel للتقارير الإلكترونية (ER)</span><span class="sxs-lookup"><span data-stu-id="a91c8-103">Modify a format by reapplying a Microsoft Excel template for electronic reporting (ER)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a91c8-104">لإكمال الخطوات في هذا الإجراء، يجب أولاً إكمال الإجراء "التقارير الإلكترونية - تصميم تكوين لإنشاء التقارير بتنسيق OPENXML".</span><span class="sxs-lookup"><span data-stu-id="a91c8-104">To complete the steps in this procedure, you must first complete the procedure, ER - Design a configuration for generating reports in OPENXML format.</span></span>

<span data-ttu-id="a91c8-105">يفسر هذا الإجراء كيفية تعديل تكوين تنسيق التقارير الإلكترونية عن طريق إعادة تطبيق قالب Microsoft Excel الذي تم تعديله.</span><span class="sxs-lookup"><span data-stu-id="a91c8-105">This procedure explains how to modify an Electronic reporting (ER) format configuration by reapplying a Microsoft Excel template that has been modified.</span></span> <span data-ttu-id="a91c8-106">في هذا الإجراء، سوف تستورد قالب Excel معدلاً إلى تكوينات تنسيق التقارير الإلكترونية التي تم إنشاؤها للشركة النموذجية Litware, Inc، ثم تنشئ المستندات الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a91c8-106">In this procedure, you will import a modified Excel template into ER format configurations that have been created for the sample company, Litware, Inc., and then generate electronic documents.</span></span> <span data-ttu-id="a91c8-107">تم تخصيص هذا الإجراء للمستخدمين الذين يؤدون دور مسؤول النظام أو مطور التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a91c8-107">This procedure is intended for users who have the system administrator or electronic reporting developer role.</span></span> <span data-ttu-id="a91c8-108">يمكن إتمام هذه الخطوات باستخدام مجموعة بيانات GBSI.</span><span class="sxs-lookup"><span data-stu-id="a91c8-108">These steps can be completed by using the GBSI dataset.</span></span> <span data-ttu-id="a91c8-109">قبل البدء، اعمل على تنزيل وحفظ الملف، SampleVendPaymWsReport2.xlsx، المدرج في موضوع التعليمات، ثم عدّل تنسيق إعداد التقارير الإلكترونية من خلال إعادة تطبيق قالب Excel (modify-electronic-reporting-format-reapply-excel-template/).</span><span class="sxs-lookup"><span data-stu-id="a91c8-109">Before you begin, download and save the file, SampleVendPaymWsReport2.xlsx, which is listed in the Help topic, Modify Electronic reporting format by reapplying an Excel template (modify-electronic-reporting-format-reapply-excel-template/).</span></span>

1. <span data-ttu-id="a91c8-110">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="a91c8-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="a91c8-111">تأكد من وجود موفر التكوين للشركة النموذجية "Litware, Inc." ومن وضع علامة عليه كنشط.</span><span class="sxs-lookup"><span data-stu-id="a91c8-111">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="a91c8-112">إذا لم تشاهد موفر التكوين هذا، فيجب أولاً إكمال الخطوات المذكورة في الإجراء، "إنشاء موفر تكوين ووضع علامة عليه على أنه نشط‬".</span><span class="sxs-lookup"><span data-stu-id="a91c8-112">If you don’t see this configuration provider, complete the steps in the procedure, Create a configuration provider and mark it as active.</span></span>  

## <a name="select-the-er-format"></a><span data-ttu-id="a91c8-113">تحديد تنسيق التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="a91c8-113">Select the ER format</span></span>
1. <span data-ttu-id="a91c8-114">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="a91c8-114">Click Reporting configurations.</span></span>
2. <span data-ttu-id="a91c8-115">في الشجرة ، قم بتوسيع "نموذج الدفع".</span><span class="sxs-lookup"><span data-stu-id="a91c8-115">In the tree, expand 'Payment model'.</span></span>
3. <span data-ttu-id="a91c8-116">في الشجرة، حدد "Payment model\Sample worksheet report".</span><span class="sxs-lookup"><span data-stu-id="a91c8-116">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
4. <span data-ttu-id="a91c8-117">انقر فوق "المرفقات".</span><span class="sxs-lookup"><span data-stu-id="a91c8-117">Click Attachments.</span></span>
    * <span data-ttu-id="a91c8-118">لاحظ أن ملف Excel، واسمه SampleVendPaymWsReport.xlsx، يُستخدم حاليًا كقالب لمعالجة دفتر يومية المدفوعات.</span><span class="sxs-lookup"><span data-stu-id="a91c8-118">Note that the SampleVendPaymWsReport.xlsx Excel file is currently used as a template for payment journal processing.</span></span>   
5. <span data-ttu-id="a91c8-119">انقر فوق "فتح".</span><span class="sxs-lookup"><span data-stu-id="a91c8-119">Click Open.</span></span>
    * <span data-ttu-id="a91c8-120">انقر فوق "فتح" لاستكشاف تخطيط قالب Excel.</span><span class="sxs-lookup"><span data-stu-id="a91c8-120">Click Open to explore the layout of the Excel template.</span></span>  
    * <span data-ttu-id="a91c8-121">راجع القالب.</span><span class="sxs-lookup"><span data-stu-id="a91c8-121">Review the template.</span></span> <span data-ttu-id="a91c8-122">تذكر أنه يتضمن حاليًا التفاصيل التالية لكل بند من بنود الدفع: رقم حساب المورّد واسم المورّد والبنك ورقم التوجيه ورقم الحساب والمدين والدائن والعملة.</span><span class="sxs-lookup"><span data-stu-id="a91c8-122">Note that it currently includes the following details for each payment line: vendor account number, vendor name, bank, routing number, account number, debit, credit, and currency.</span></span> <span data-ttu-id="a91c8-123">لهذا المثال، نحن نريد توسيع هذه القائمة من خلال إضافة تفاصيل حول تاريخ الدفع.</span><span class="sxs-lookup"><span data-stu-id="a91c8-123">For this example, we want to extend this list by adding details about the payment date.</span></span>   
6. <span data-ttu-id="a91c8-124">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a91c8-124">Close the page.</span></span>

## <a name="reapply-a-new-excel-template-to-er-format"></a><span data-ttu-id="a91c8-125">إعادة تطبيق قالب Excel جديد على تنسيق التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="a91c8-125">Reapply a new Excel template to ER format</span></span>
1. <span data-ttu-id="a91c8-126">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="a91c8-126">Click Designer.</span></span>
    * <span data-ttu-id="a91c8-127">افتح إصدار المسودة لتنسيق التقارير الإلكترونية المحدد لتحريره.</span><span class="sxs-lookup"><span data-stu-id="a91c8-127">Open the draft version of the selected ER format for editing.</span></span>  
2. <span data-ttu-id="a91c8-128">في جزء الإجراءات، انقر فوق "استيراد".</span><span class="sxs-lookup"><span data-stu-id="a91c8-128">On the Action Pane, click Import.</span></span>
3. <span data-ttu-id="a91c8-129">انقر فوق "تحديث من Excel".</span><span class="sxs-lookup"><span data-stu-id="a91c8-129">Click Update from Excel.</span></span>
    * <span data-ttu-id="a91c8-130">انقر فوق "تحديث القالب"، ثم حدد الملف، SampleVendPaymWsReport2.xlsx.</span><span class="sxs-lookup"><span data-stu-id="a91c8-130">Click ‘Update template’, and then select the file, SampleVendPaymWsReport2.xlsx.</span></span>  
    * <span data-ttu-id="a91c8-131">انقر فوق "تحديث القالب" واستعرض للوصل إلى الملف SampleVendPaymWsReport2.xlsx الذي تم تنزيله في وقت سابق.</span><span class="sxs-lookup"><span data-stu-id="a91c8-131">Click Update template and browse to get the downloaded earlier SampleVendPaymWsReport2.xlsx file.</span></span>  
4. <span data-ttu-id="a91c8-132">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="a91c8-132">Click OK.</span></span>
    * <span data-ttu-id="a91c8-133">يتم تطبيق القالب SampleVendPaymWsReport2.xlsx.</span><span class="sxs-lookup"><span data-stu-id="a91c8-133">The SampleVendPaymWsReport2.xlsx template is applied.</span></span> <span data-ttu-id="a91c8-134">تتم مزامنة بنية تنسيق التقارير الإلكترونية مع محتوى القالب، الذي تضاف عناصره إلى تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a91c8-134">The structure of the ER format is synchronized with the content of the template, whose elements are added to the ER format.</span></span> <span data-ttu-id="a91c8-135">تُزال من تعريف التنسيق أي عناصر موجودة في تنسيق التقارير الإلكترونية غير مضمنة في القالب.</span><span class="sxs-lookup"><span data-stu-id="a91c8-135">Any existing elements in the ER format that aren’t included in the template are removed from the format definition.</span></span>  
5. <span data-ttu-id="a91c8-136">في الشجرة، حدد 'Excel'.</span><span class="sxs-lookup"><span data-stu-id="a91c8-136">In the tree, select 'Excel'.</span></span>
    * <span data-ttu-id="a91c8-137">لاحظ أن الحقل "القالب" يحتوي الآن على مرجع إلى القالب الجديد.</span><span class="sxs-lookup"><span data-stu-id="a91c8-137">Note that the Template field now contains a reference to the new template.</span></span>   
6. <span data-ttu-id="a91c8-138">انقر فوق "المرفقات".</span><span class="sxs-lookup"><span data-stu-id="a91c8-138">Click Attachments.</span></span>
7. <span data-ttu-id="a91c8-139">انقر فوق "فتح".</span><span class="sxs-lookup"><span data-stu-id="a91c8-139">Click Open.</span></span>
    * <span data-ttu-id="a91c8-140">انقر فوق "فتح" لاستكشاف تخطيط قالب Excel المعدّل.</span><span class="sxs-lookup"><span data-stu-id="a91c8-140">Click Open to explore the layout of the modified Excel template.</span></span>  
    * <span data-ttu-id="a91c8-141">راجع القالب.</span><span class="sxs-lookup"><span data-stu-id="a91c8-141">Review the template.</span></span> <span data-ttu-id="a91c8-142">لاحظ أنه يحتوي الآن على بند لتاريخ الدفع.</span><span class="sxs-lookup"><span data-stu-id="a91c8-142">Note that it now contains a line for the payment date.</span></span>   
8. <span data-ttu-id="a91c8-143">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a91c8-143">Close the page.</span></span>
9. <span data-ttu-id="a91c8-144">في الشجرة، قم بتوسيع 'Excel'.</span><span class="sxs-lookup"><span data-stu-id="a91c8-144">In the tree, expand 'Excel'.</span></span>
10. <span data-ttu-id="a91c8-145">في الشجرة، قم بتوسيع "Excel\PaymLines".</span><span class="sxs-lookup"><span data-stu-id="a91c8-145">In the tree, expand 'Excel\PaymLines'.</span></span>
11. <span data-ttu-id="a91c8-146">في الشجرة، حدد "Excel\PaymLines\PaymDate".</span><span class="sxs-lookup"><span data-stu-id="a91c8-146">In the tree, select 'Excel\PaymLines\PaymDate'.</span></span>
    * <span data-ttu-id="a91c8-147">لاحظ أن تنسيق التقارير الإلكترونية يحتوي الآن على عنصر إضافي واحد.</span><span class="sxs-lookup"><span data-stu-id="a91c8-147">Note that the ER format now contains one more item.</span></span> <span data-ttu-id="a91c8-148">تمت إضافة خلية، PaymDate، إلى قالب Excel.</span><span class="sxs-lookup"><span data-stu-id="a91c8-148">A cell, PaymDate, has been added to the Excel template.</span></span>  
12. <span data-ttu-id="a91c8-149">انقر فوق علامة التبويب "التعيين".</span><span class="sxs-lookup"><span data-stu-id="a91c8-149">Click the Mapping tab.</span></span>
13. <span data-ttu-id="a91c8-150">في الشجرة ، قم بتوسيع "النموذج"</span><span class="sxs-lookup"><span data-stu-id="a91c8-150">In the tree, expand 'model'.</span></span>
14. <span data-ttu-id="a91c8-151">في الشجرة، قم بتوسيع "النموذج/المدفوعات".</span><span class="sxs-lookup"><span data-stu-id="a91c8-151">In the tree, expand 'model\Payments'.</span></span>
15. <span data-ttu-id="a91c8-152">في الشجرة، حدد "النموذج/المدفوعات/تاريخ الحركة(TransactionDate)".</span><span class="sxs-lookup"><span data-stu-id="a91c8-152">In the tree, select 'model\Payments\Transaction date(TransactionDate)'.</span></span>
16. <span data-ttu-id="a91c8-153">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="a91c8-153">Click Bind.</span></span>
    * <span data-ttu-id="a91c8-154">حدد البيانات المضافة إلى الخلية الجديدة في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="a91c8-154">Specify what data is added to the new cell at runtime.</span></span>  
17. <span data-ttu-id="a91c8-155">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="a91c8-155">Click Save.</span></span>
18. <span data-ttu-id="a91c8-156">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a91c8-156">Close the page.</span></span>

## <a name="enable-the-modified-draft-version-of-the-er-format-for-use-in-payment-journal-processing"></a><span data-ttu-id="a91c8-157">تمكين إصدار المسودة‬ المعدل لتنسيق التقارير الإلكترونية لاستخدامه في معالجة دفتر يومية المدفوعات</span><span class="sxs-lookup"><span data-stu-id="a91c8-157">Enable the modified draft version of the ER format for use in payment journal processing</span></span>
1. <span data-ttu-id="a91c8-158">في جزء الإجراءات، انقر فوق "التكوينات".</span><span class="sxs-lookup"><span data-stu-id="a91c8-158">On the Action Pane, click Configurations.</span></span>
2. <span data-ttu-id="a91c8-159">انقر فوق "محددات المستخدم".</span><span class="sxs-lookup"><span data-stu-id="a91c8-159">Click User parameters.</span></span>
3. <span data-ttu-id="a91c8-160">حدد "نعم" في حقل "تشغيل الإعدادات".</span><span class="sxs-lookup"><span data-stu-id="a91c8-160">Select Yes in the Run settings field.</span></span>
4. <span data-ttu-id="a91c8-161">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="a91c8-161">Click OK.</span></span>
5. <span data-ttu-id="a91c8-162">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="a91c8-162">Click Edit.</span></span>
6. <span data-ttu-id="a91c8-163">حدد "نعم" في حقل "تشغيل المسودة‬".</span><span class="sxs-lookup"><span data-stu-id="a91c8-163">Select Yes in the Run Draft field.</span></span>

## <a name="use-the-modified-draft-version-of-the-er-format-for-payment-journal-processing"></a><span data-ttu-id="a91c8-164">استخدام إصدار المسودة‬ المعدل لتنسيق التقارير الإلكترونية لاستخدامه في معالجة دفتر يومية المدفوعات</span><span class="sxs-lookup"><span data-stu-id="a91c8-164">Use the modified draft version of the ER format for payment journal processing</span></span>
    * <span data-ttu-id="a91c8-165">قم بمراجعة ورقة العمل التي تم إنشاؤها، بما في ذلك التفاصيل الجديدة لبنود الدفع – تاريخ الدفع.</span><span class="sxs-lookup"><span data-stu-id="a91c8-165">Review the created worksheet, including new detail of payment lines – payment date.</span></span>  


