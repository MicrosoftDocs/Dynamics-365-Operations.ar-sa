--- 
title: "تشغيل التنسيقات لاستخدام ملفات إدارة المستندات في مخرجات التقارير الإلكترونية"
description: "تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لاستخدام ملفات إدارة المستندات في مخرجات التقارير الإلكترونية."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenInvoicesListPage, CustInvoiceJournal, SalesTable, ERSolutionTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: e87dbb0fa890f4d554c3e2ff09566fb2b1f3206b
ms.contentlocale: ar-sa
ms.lasthandoff: 09/14/2018

---
# <a name="run-formats-to-use-document-management-files-in-er-output"></a><span data-ttu-id="e69cd-103">تشغيل التنسيقات لاستخدام ملفات إدارة المستندات في مخرجات التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="e69cd-103">Run formats to use Document Management files in ER output</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e69cd-104">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لاستخدام ملفات إدارة المستندات (مرفقات) في مخرجات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="e69cd-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="e69cd-105">يمكن تنفيذ هذه الخطوات في شركة DEMF.</span><span class="sxs-lookup"><span data-stu-id="e69cd-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="e69cd-106">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "التقارير الإلكترونية - استخدام ملفات إدارة المستندات في مخرجات التنسيق (الجزء 3: إنشاء التنسيق)".</span><span class="sxs-lookup"><span data-stu-id="e69cd-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 3: Create format)” procedure.</span></span>

<span data-ttu-id="e69cd-107">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="e69cd-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a><span data-ttu-id="e69cd-108">إضافة المرفقات الضرورية لأمر مبيعات من فاتورة واحدة</span><span class="sxs-lookup"><span data-stu-id="e69cd-108">Add necessary attachments for sales order of a single invoice</span></span>
1. <span data-ttu-id="e69cd-109">انتقل إلى الحسابات المدينة > الفواتير > فواتير العملاء المفتوحة.</span><span class="sxs-lookup"><span data-stu-id="e69cd-109">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="e69cd-110">استخدم عامل التصفية السريع للبحث عن السجلات.</span><span class="sxs-lookup"><span data-stu-id="e69cd-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="e69cd-111">على سبيل المثال، قم بإجراء التصفية على حقل "الفاتورة" بالقيمة "CIV-000148".</span><span class="sxs-lookup"><span data-stu-id="e69cd-111">For example, filter on the Invoice field with a value of 'CIV-000148'.</span></span>
    * <span data-ttu-id="e69cd-112">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="e69cd-112">CIV-000148</span></span>  
3. <span data-ttu-id="e69cd-113">انقر لتتبع ارتباط الفاتورة المحددة.</span><span class="sxs-lookup"><span data-stu-id="e69cd-113">Click to follow the selected invoice’s link.</span></span>
    * <span data-ttu-id="e69cd-114">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="e69cd-114">CIV-000148</span></span>  
4. <span data-ttu-id="e69cd-115">انقر لتتبع الارتباط الموجود في الحقل "أمر المبيعات".</span><span class="sxs-lookup"><span data-stu-id="e69cd-115">Click to follow the link in the Sales order field.</span></span>
    * <span data-ttu-id="e69cd-116">000148</span><span class="sxs-lookup"><span data-stu-id="e69cd-116">000148</span></span>  
5. <span data-ttu-id="e69cd-117">في حقل "الأسطر أو العنوان‬"، حدد خيار "العنوان".</span><span class="sxs-lookup"><span data-stu-id="e69cd-117">In the Lines or header field, select the option of Header.</span></span>
    * <span data-ttu-id="e69cd-118">حدد "الرأس" للإشارة إلى أن هذا سيكون الهدف لإضافة مرفقات.</span><span class="sxs-lookup"><span data-stu-id="e69cd-118">Select Header to indicate that this will be the target for adding attachments.</span></span>  
6. <span data-ttu-id="e69cd-119">انقر فوق "إرفاق".</span><span class="sxs-lookup"><span data-stu-id="e69cd-119">Click Attach.</span></span>
    * <span data-ttu-id="e69cd-120">أضف بعض الملفات كمرفقات لأمر المبيعات هذا.</span><span class="sxs-lookup"><span data-stu-id="e69cd-120">Add a few files as attachments for this sales order.</span></span> <span data-ttu-id="e69cd-121">استخدم ملفات من أنواع المستندات المعتمدة من قبل "إدارة المستندات" (مع ملحقات أسماء الملفات DOCX وDPF وXML وJPG وغير ذلك).</span><span class="sxs-lookup"><span data-stu-id="e69cd-121">Use the files of the document types that are supported by the Document Management (with file extensions DOCX, DPF, XML, JPG, etc.).</span></span> <span data-ttu-id="e69cd-122">استعرض وحدد الملفات المطلوب إرفاقها ثم معالجتها بالفاتورة المرتبطة في رسالة التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="e69cd-122">Browse and select files to be attached and further processed with the related invoice in the ER electronic message.</span></span>  
7. <span data-ttu-id="e69cd-123">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="e69cd-123">Click New.</span></span>
8. <span data-ttu-id="e69cd-124">انقر فوق "ملف".</span><span class="sxs-lookup"><span data-stu-id="e69cd-124">Click File.</span></span>
9. <span data-ttu-id="e69cd-125">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="e69cd-125">Click New.</span></span>
10. <span data-ttu-id="e69cd-126">انقر فوق "ملف".</span><span class="sxs-lookup"><span data-stu-id="e69cd-126">Click File.</span></span>
11. <span data-ttu-id="e69cd-127">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e69cd-127">Close the page.</span></span>
12. <span data-ttu-id="e69cd-128">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e69cd-128">Close the page.</span></span>
13. <span data-ttu-id="e69cd-129">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e69cd-129">Close the page.</span></span>
14. <span data-ttu-id="e69cd-130">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e69cd-130">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="e69cd-131">تشغيل التقرير المصمم للفاتورة المحددة</span><span class="sxs-lookup"><span data-stu-id="e69cd-131">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="e69cd-132">انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.</span><span class="sxs-lookup"><span data-stu-id="e69cd-132">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="e69cd-133">في الشجرة، قم بتوسيع "نموذج فاتورة العميل".</span><span class="sxs-lookup"><span data-stu-id="e69cd-133">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="e69cd-134">في الشجرة، قم بتوسيع "نموذج فاتورة العميل‬/نموذج فاتورة العميل‬ (مخصص)".</span><span class="sxs-lookup"><span data-stu-id="e69cd-134">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="e69cd-135">في الشجرة، حدد "نموذج فاتورة العميل‬/نموذج فاتورة العميل‬ (مخصص)/رسالة نموذج فاتورة إلكترونية."</span><span class="sxs-lookup"><span data-stu-id="e69cd-135">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="e69cd-136">انقر فوق "تشغيل".</span><span class="sxs-lookup"><span data-stu-id="e69cd-136">Click Run.</span></span>
6. <span data-ttu-id="e69cd-137">وسّع المقطع "السجلات المطلوب تضمينها‬ ()".</span><span class="sxs-lookup"><span data-stu-id="e69cd-137">Expand the Records to include () section.</span></span>
7. <span data-ttu-id="e69cd-138">انقر فوق "عامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="e69cd-138">Click Filter.</span></span>
8. <span data-ttu-id="e69cd-139">حدد الصف لحقل دفتر يومية فاتورة العميل وأمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="e69cd-139">Select the row of the Customer invoice journal and the Sales order field.</span></span>
9. <span data-ttu-id="e69cd-140">في الحقل "المعايير، اكتب ''000148".</span><span class="sxs-lookup"><span data-stu-id="e69cd-140">In the Criteria field, type '000148'.</span></span>
    * <span data-ttu-id="e69cd-141">في حقل معايير "أمر المبيعات"، اكتب رقم الأمر 000148.</span><span class="sxs-lookup"><span data-stu-id="e69cd-141">In the criteria “Sales order” field, type the order number 000148.</span></span>  
10. <span data-ttu-id="e69cd-142">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="e69cd-142">Click OK.</span></span>
11. <span data-ttu-id="e69cd-143">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="e69cd-143">Click OK.</span></span>
    * <span data-ttu-id="e69cd-144">اعمل على مراجعة المخرجات المنشأة.</span><span class="sxs-lookup"><span data-stu-id="e69cd-144">Review the generated output.</span></span> <span data-ttu-id="e69cd-145">لاحظ أنه قد تم إنشاء عقده XML واحدة لكل مرفق.</span><span class="sxs-lookup"><span data-stu-id="e69cd-145">Note that for each attachment a single XML node has been created.</span></span> <span data-ttu-id="e69cd-146">تتم تعبئة محتوى المرفقات في مخرجات XML بالتنسيق النصي MIME (base64).</span><span class="sxs-lookup"><span data-stu-id="e69cd-146">The attachment’s content is populated to the XML output in MIME (base64) text format.</span></span>  


