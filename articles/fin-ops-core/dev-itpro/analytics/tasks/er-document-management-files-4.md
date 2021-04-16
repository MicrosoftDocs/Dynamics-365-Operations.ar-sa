---
title: تستخدم التقارير الإلكترونية ملفات إدارة المستندات في مخرجات التنسيق‬ (الجزء 4 - تشغيل التنسيق)
description: يوضح هذا الموضوع كيفيه تكوين تنسيق التقارير الكترونيه لاستخدام ملفات أداره المستندات في إخراج ER. (جزء 4)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenInvoicesListPage, CustInvoiceJournal, SalesTable, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f7a7c9705d8b53ef13cd3faf13290f3f1b1d1c43
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749107"
---
# <a name="er-use-document-management-files-in-format-outputs-part-4---run-format"></a><span data-ttu-id="68e7b-104">تستخدم التقارير الإلكترونية ملفات إدارة المستندات في مخرجات التنسيق‬ (الجزء 4 - تشغيل التنسيق)</span><span class="sxs-lookup"><span data-stu-id="68e7b-104">ER Use Document Management files in format outputs (Part 4 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="68e7b-105">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لاستخدام ملفات إدارة المستندات (مرفقات) في مخرجات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="68e7b-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="68e7b-106">يمكن تنفيذ هذه الخطوات في شركة DEMF.</span><span class="sxs-lookup"><span data-stu-id="68e7b-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="68e7b-107">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "التقارير الإلكترونية - استخدام ملفات إدارة المستندات في مخرجات التنسيق (الجزء 3: إنشاء التنسيق)".</span><span class="sxs-lookup"><span data-stu-id="68e7b-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 3: Create format)" procedure.</span></span>

<span data-ttu-id="68e7b-108">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="68e7b-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a><span data-ttu-id="68e7b-109">إضافة المرفقات الضرورية لأمر مبيعات من فاتورة واحدة</span><span class="sxs-lookup"><span data-stu-id="68e7b-109">Add necessary attachments for sales order of a single invoice</span></span>
1. <span data-ttu-id="68e7b-110">انتقل إلى الحسابات المدينة > الفواتير > فواتير العملاء المفتوحة.</span><span class="sxs-lookup"><span data-stu-id="68e7b-110">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="68e7b-111">استخدم عامل التصفية السريع للبحث عن السجلات.</span><span class="sxs-lookup"><span data-stu-id="68e7b-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="68e7b-112">على سبيل المثال، قم بإجراء التصفية على حقل "الفاتورة" بالقيمة "CIV-000148".</span><span class="sxs-lookup"><span data-stu-id="68e7b-112">For example, filter on the Invoice field with a value of 'CIV-000148'.</span></span>
    * <span data-ttu-id="68e7b-113">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="68e7b-113">CIV-000148</span></span>  
3. <span data-ttu-id="68e7b-114">انقر لتتبع ارتباط الفاتورة المحددة.</span><span class="sxs-lookup"><span data-stu-id="68e7b-114">Click to follow the selected invoice's link.</span></span>
    * <span data-ttu-id="68e7b-115">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="68e7b-115">CIV-000148</span></span>  
4. <span data-ttu-id="68e7b-116">انقر لتتبع الارتباط الموجود في الحقل "أمر المبيعات".</span><span class="sxs-lookup"><span data-stu-id="68e7b-116">Click to follow the link in the Sales order field.</span></span>
    * <span data-ttu-id="68e7b-117">000148</span><span class="sxs-lookup"><span data-stu-id="68e7b-117">000148</span></span>  
5. <span data-ttu-id="68e7b-118">في حقل "الأسطر أو العنوان‬"، حدد خيار "العنوان".</span><span class="sxs-lookup"><span data-stu-id="68e7b-118">In the Lines or header field, select the option of Header.</span></span>
    * <span data-ttu-id="68e7b-119">حدد "الرأس" للإشارة إلى أن هذا سيكون الهدف لإضافة مرفقات.</span><span class="sxs-lookup"><span data-stu-id="68e7b-119">Select Header to indicate that this will be the target for adding attachments.</span></span>  
6. <span data-ttu-id="68e7b-120">انقر فوق "إرفاق".</span><span class="sxs-lookup"><span data-stu-id="68e7b-120">Click Attach.</span></span>
    * <span data-ttu-id="68e7b-121">أضف بعض الملفات كمرفقات لأمر المبيعات هذا.</span><span class="sxs-lookup"><span data-stu-id="68e7b-121">Add a few files as attachments for this sales order.</span></span> <span data-ttu-id="68e7b-122">استخدم ملفات من أنواع المستندات المعتمدة من قبل "إدارة المستندات" (مع ملحقات أسماء الملفات DOCX وDPF وXML وJPG وغير ذلك).</span><span class="sxs-lookup"><span data-stu-id="68e7b-122">Use the files of the document types that are supported by the Document Management (with file extensions DOCX, DPF, XML, JPG, etc.).</span></span> <span data-ttu-id="68e7b-123">استعرض وحدد الملفات المطلوب إرفاقها ثم معالجتها بالفاتورة المرتبطة في رسالة التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="68e7b-123">Browse and select files to be attached and further processed with the related invoice in the ER electronic message.</span></span>  
7. <span data-ttu-id="68e7b-124">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="68e7b-124">Click New.</span></span>
8. <span data-ttu-id="68e7b-125">انقر فوق "ملف".</span><span class="sxs-lookup"><span data-stu-id="68e7b-125">Click File.</span></span>
9. <span data-ttu-id="68e7b-126">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="68e7b-126">Click New.</span></span>
10. <span data-ttu-id="68e7b-127">انقر فوق "ملف".</span><span class="sxs-lookup"><span data-stu-id="68e7b-127">Click File.</span></span>
11. <span data-ttu-id="68e7b-128">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="68e7b-128">Close the page.</span></span>
12. <span data-ttu-id="68e7b-129">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="68e7b-129">Close the page.</span></span>
13. <span data-ttu-id="68e7b-130">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="68e7b-130">Close the page.</span></span>
14. <span data-ttu-id="68e7b-131">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="68e7b-131">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="68e7b-132">تشغيل التقرير المصمم للفاتورة المحددة</span><span class="sxs-lookup"><span data-stu-id="68e7b-132">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="68e7b-133">انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.</span><span class="sxs-lookup"><span data-stu-id="68e7b-133">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="68e7b-134">في الشجرة، قم بتوسيع "نموذج فاتورة العميل".</span><span class="sxs-lookup"><span data-stu-id="68e7b-134">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="68e7b-135">في الشجرة، قم بتوسيع "نموذج فاتورة العميل‬/نموذج فاتورة العميل‬ (مخصص)".</span><span class="sxs-lookup"><span data-stu-id="68e7b-135">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="68e7b-136">في الشجرة، حدد "نموذج فاتورة العميل‬/نموذج فاتورة العميل‬ (مخصص)/رسالة نموذج فاتورة إلكترونية."</span><span class="sxs-lookup"><span data-stu-id="68e7b-136">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="68e7b-137">انقر فوق "تشغيل".</span><span class="sxs-lookup"><span data-stu-id="68e7b-137">Click Run.</span></span>
6. <span data-ttu-id="68e7b-138">وسّع المقطع "السجلات المطلوب تضمينها‬ ()".</span><span class="sxs-lookup"><span data-stu-id="68e7b-138">Expand the Records to include () section.</span></span>
7. <span data-ttu-id="68e7b-139">انقر فوق "عامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="68e7b-139">Click Filter.</span></span>
8. <span data-ttu-id="68e7b-140">حدد الصف لحقل دفتر يومية فاتورة العميل وأمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="68e7b-140">Select the row of the Customer invoice journal and the Sales order field.</span></span>
9. <span data-ttu-id="68e7b-141">في الحقل "المعايير، اكتب ''000148".</span><span class="sxs-lookup"><span data-stu-id="68e7b-141">In the Criteria field, type '000148'.</span></span>
    * <span data-ttu-id="68e7b-142">في حقل معايير "أمر المبيعات"، اكتب رقم الأمر 000148.</span><span class="sxs-lookup"><span data-stu-id="68e7b-142">In the criteria "Sales order" field, type the order number 000148.</span></span>  
10. <span data-ttu-id="68e7b-143">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="68e7b-143">Click OK.</span></span>
11. <span data-ttu-id="68e7b-144">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="68e7b-144">Click OK.</span></span>
    * <span data-ttu-id="68e7b-145">اعمل على مراجعة المخرجات المنشأة.</span><span class="sxs-lookup"><span data-stu-id="68e7b-145">Review the generated output.</span></span> <span data-ttu-id="68e7b-146">لاحظ أنه قد تم إنشاء عقده XML واحدة لكل مرفق.</span><span class="sxs-lookup"><span data-stu-id="68e7b-146">Note that for each attachment a single XML node has been created.</span></span> <span data-ttu-id="68e7b-147">تتم تعبئة محتوى المرفقات في مخرجات XML بالتنسيق النصي MIME (base64).</span><span class="sxs-lookup"><span data-stu-id="68e7b-147">The attachment's content is populated to the XML output in MIME (base64) text format.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]