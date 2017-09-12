--- 
title: "توسيع نموذج بيانات لاستخدام ملفات إدارة المستندات في مخرجات التنسيق للتقارير الإلكترونية (ER)"
description: "تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لاستخدام ملفات إدارة المستندات (مرفقات) في مخرجات التقارير الإلكترونية."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1a5325dc3a97b9e205b41fe8dae18f43e430daeb
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="extend-data-model-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a><span data-ttu-id="996e2-103">توسيع نموذج بيانات لاستخدام ملفات إدارة المستندات في مخرجات التنسيق للتقارير الإلكترونية (ER)</span><span class="sxs-lookup"><span data-stu-id="996e2-103">Extend data model to use Document Management files in format outputs for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="996e2-104">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لاستخدام ملفات إدارة المستندات (مرفقات) في مخرجات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="996e2-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="996e2-105">يمكن تنفيذ هذه الخطوات في أي شركة.</span><span class="sxs-lookup"><span data-stu-id="996e2-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="996e2-106">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في دليل المهمة "التقارير الإلكترونية - استخدام ملفات إدارة المستندات في مخرجات التنسيق (الجزء 1: إعداد نموذج البيانات").</span><span class="sxs-lookup"><span data-stu-id="996e2-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 1: Prepare data model)” task guide.</span></span>

<span data-ttu-id="996e2-107">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="996e2-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="996e2-108">توسيع نموذج البيانات لتقديم ملفات إدارة المستندات فيه</span><span class="sxs-lookup"><span data-stu-id="996e2-108">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="996e2-109">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="996e2-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="996e2-110">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="996e2-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="996e2-111">في الشجرة، قم بتوسيع "نموذج فاتورة العميل".</span><span class="sxs-lookup"><span data-stu-id="996e2-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="996e2-112">في الشجرة، حدد "نموذج فاتورة العميل‬/نموذج فاتورة العميل‬ (مخصص)".</span><span class="sxs-lookup"><span data-stu-id="996e2-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="996e2-113">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="996e2-113">Click Designer.</span></span>
6. <span data-ttu-id="996e2-114">في الشجرة، حدد "فاتورة العميل(InvoiceCustomer)".</span><span class="sxs-lookup"><span data-stu-id="996e2-114">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="996e2-115">سنقوم بتوسيع نموذج البيانات هذا لعرضه في أية ملفات تم إرفاقها بأمر مبيعات يرتبط بفاتورة تتم معالجتها إلكترونيًا.</span><span class="sxs-lookup"><span data-stu-id="996e2-115">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="996e2-116">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="996e2-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="996e2-117">في حقل "الاسم"، اكتب "مرفقات الفواتير".</span><span class="sxs-lookup"><span data-stu-id="996e2-117">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="996e2-118">مرفقات الفاتورة</span><span class="sxs-lookup"><span data-stu-id="996e2-118">Invoice attachments</span></span>  
9. <span data-ttu-id="996e2-119">في الحقل "نوع الصنف"، حدد "قائمة سجلات".</span><span class="sxs-lookup"><span data-stu-id="996e2-119">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="996e2-120">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="996e2-120">Click Add.</span></span>
11. <span data-ttu-id="996e2-121">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="996e2-121">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="996e2-122">في حقل "الاسم"، اكتب "محتوى الملف".</span><span class="sxs-lookup"><span data-stu-id="996e2-122">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="996e2-123">محتوى الملف</span><span class="sxs-lookup"><span data-stu-id="996e2-123">File content</span></span>  
13. <span data-ttu-id="996e2-124">في الحقل "نوع الصنف"، حدد "الحاوية".</span><span class="sxs-lookup"><span data-stu-id="996e2-124">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="996e2-125">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="996e2-125">Click Add.</span></span>
15. <span data-ttu-id="996e2-126">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="996e2-126">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="996e2-127">في حقل "الاسم"، اكتب "اسم الملف".</span><span class="sxs-lookup"><span data-stu-id="996e2-127">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="996e2-128">اسم الملف</span><span class="sxs-lookup"><span data-stu-id="996e2-128">File name</span></span>  
17. <span data-ttu-id="996e2-129">في الحقل "نوع الصنف"، حدد "سلسلة".</span><span class="sxs-lookup"><span data-stu-id="996e2-129">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="996e2-130">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="996e2-130">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-dynamics-365-for-finance-and-operations-enterprise-edition-data-sources"></a><span data-ttu-id="996e2-131">تعيين عناصر نموذج بيانات جديد إلى مصادر بيانات Dynamics 365 for Finance and Operations, Enterprise edition</span><span class="sxs-lookup"><span data-stu-id="996e2-131">Map new data model elements to Dynamics 365 for Finance and Operations, Enterprise edition data sources</span></span>
1. <span data-ttu-id="996e2-132">انقر فوق "تعيين النموذج لمصدر البيانات".</span><span class="sxs-lookup"><span data-stu-id="996e2-132">Click Map model to datasource.</span></span>
2. <span data-ttu-id="996e2-133">استخدم عامل التصفية السريع لإجراء التصفية باستخدام حقل "التعريف" بالقيمة "InvoiceCustomer".</span><span class="sxs-lookup"><span data-stu-id="996e2-133">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="996e2-134">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="996e2-134">InvoiceCustomer</span></span>  
    * <span data-ttu-id="996e2-135">سنقوم بتعيين عناصر نماذج جديدة إلى مصادر البيانات المناسبة.</span><span class="sxs-lookup"><span data-stu-id="996e2-135">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="996e2-136">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="996e2-136">Click Designer.</span></span>
4. <span data-ttu-id="996e2-137">في الشجرة، حدد "مرفقات الفاتورة‬".</span><span class="sxs-lookup"><span data-stu-id="996e2-137">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="996e2-138">في الشجرة، قم بتوسيع "مرفقات الفاتورة‬".</span><span class="sxs-lookup"><span data-stu-id="996e2-138">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="996e2-139">في الشجرة، حدد "مرفقات الفاتورة\اسم الملف‬".</span><span class="sxs-lookup"><span data-stu-id="996e2-139">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="996e2-140">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="996e2-140">Click Edit.</span></span>
8. <span data-ttu-id="996e2-141">في حقل المعادلة، أدخل 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span><span class="sxs-lookup"><span data-stu-id="996e2-141">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="996e2-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="996e2-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="996e2-143">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="996e2-143">Click Save.</span></span>
10. <span data-ttu-id="996e2-144">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="996e2-144">Close the page.</span></span>
11. <span data-ttu-id="996e2-145">في الشجرة، حدد "مرفقات الفاتورة\محتوى الملف".</span><span class="sxs-lookup"><span data-stu-id="996e2-145">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="996e2-146">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="996e2-146">Click Edit.</span></span>
13. <span data-ttu-id="996e2-147">في حقل المعادلة، أدخل 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span><span class="sxs-lookup"><span data-stu-id="996e2-147">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="996e2-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="996e2-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="996e2-149">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="996e2-149">Click Save.</span></span>
15. <span data-ttu-id="996e2-150">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="996e2-150">Close the page.</span></span>
16. <span data-ttu-id="996e2-151">في الشجرة، حدد "مرفقات الفاتورة‬".</span><span class="sxs-lookup"><span data-stu-id="996e2-151">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="996e2-152">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="996e2-152">Click Edit.</span></span>
18. <span data-ttu-id="996e2-153">في حقل المعادلة، أدخل 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span><span class="sxs-lookup"><span data-stu-id="996e2-153">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="996e2-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="996e2-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="996e2-155">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="996e2-155">Click Save.</span></span>
20. <span data-ttu-id="996e2-156">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="996e2-156">Close the page.</span></span>
21. <span data-ttu-id="996e2-157">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="996e2-157">Click Save.</span></span>
22. <span data-ttu-id="996e2-158">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="996e2-158">Close the page.</span></span>
23. <span data-ttu-id="996e2-159">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="996e2-159">Close the page.</span></span>
24. <span data-ttu-id="996e2-160">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="996e2-160">Close the page.</span></span>
25. <span data-ttu-id="996e2-161">انقر فوق "تغيير الحالة".</span><span class="sxs-lookup"><span data-stu-id="996e2-161">Click Change status.</span></span>
26. <span data-ttu-id="996e2-162">انقر فوق "مكتمل".</span><span class="sxs-lookup"><span data-stu-id="996e2-162">Click Complete.</span></span>
27. <span data-ttu-id="996e2-163">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="996e2-163">Click OK.</span></span>


