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
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: ebbd442c9f69290dc995c05462ca70b554f7d9f2
ms.contentlocale: ar-sa
ms.lasthandoff: 03/26/2018

---
# <a name="extend-data-model-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a><span data-ttu-id="7548d-103">توسيع نموذج بيانات لاستخدام ملفات إدارة المستندات في مخرجات التنسيق للتقارير الإلكترونية (ER)</span><span class="sxs-lookup"><span data-stu-id="7548d-103">Extend data model to use Document Management files in format outputs for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7548d-104">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لاستخدام ملفات إدارة المستندات (مرفقات) في مخرجات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="7548d-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="7548d-105">يمكن تنفيذ هذه الخطوات في أي شركة.</span><span class="sxs-lookup"><span data-stu-id="7548d-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="7548d-106">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في دليل المهمة "التقارير الإلكترونية - استخدام ملفات إدارة المستندات في مخرجات التنسيق (الجزء 1: إعداد نموذج البيانات").</span><span class="sxs-lookup"><span data-stu-id="7548d-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 1: Prepare data model)” task guide.</span></span>

<span data-ttu-id="7548d-107">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="7548d-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="7548d-108">توسيع نموذج البيانات لتقديم ملفات إدارة المستندات فيه</span><span class="sxs-lookup"><span data-stu-id="7548d-108">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="7548d-109">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="7548d-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="7548d-110">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="7548d-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="7548d-111">في الشجرة، قم بتوسيع "نموذج فاتورة العميل".</span><span class="sxs-lookup"><span data-stu-id="7548d-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="7548d-112">في الشجرة، حدد "نموذج فاتورة العميل‬/نموذج فاتورة العميل‬ (مخصص)".</span><span class="sxs-lookup"><span data-stu-id="7548d-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="7548d-113">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="7548d-113">Click Designer.</span></span>
6. <span data-ttu-id="7548d-114">في الشجرة، حدد "فاتورة العميل(InvoiceCustomer)".</span><span class="sxs-lookup"><span data-stu-id="7548d-114">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="7548d-115">سنقوم بتوسيع نموذج البيانات هذا لعرضه في أية ملفات تم إرفاقها بأمر مبيعات يرتبط بفاتورة تتم معالجتها إلكترونيًا.</span><span class="sxs-lookup"><span data-stu-id="7548d-115">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="7548d-116">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="7548d-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="7548d-117">في حقل "الاسم"، اكتب "مرفقات الفواتير".</span><span class="sxs-lookup"><span data-stu-id="7548d-117">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="7548d-118">مرفقات الفاتورة</span><span class="sxs-lookup"><span data-stu-id="7548d-118">Invoice attachments</span></span>  
9. <span data-ttu-id="7548d-119">في الحقل "نوع الصنف"، حدد "قائمة سجلات".</span><span class="sxs-lookup"><span data-stu-id="7548d-119">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="7548d-120">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="7548d-120">Click Add.</span></span>
11. <span data-ttu-id="7548d-121">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="7548d-121">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="7548d-122">في حقل "الاسم"، اكتب "محتوى الملف".</span><span class="sxs-lookup"><span data-stu-id="7548d-122">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="7548d-123">محتوى الملف</span><span class="sxs-lookup"><span data-stu-id="7548d-123">File content</span></span>  
13. <span data-ttu-id="7548d-124">في الحقل "نوع الصنف"، حدد "الحاوية".</span><span class="sxs-lookup"><span data-stu-id="7548d-124">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="7548d-125">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="7548d-125">Click Add.</span></span>
15. <span data-ttu-id="7548d-126">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="7548d-126">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="7548d-127">في حقل "الاسم"، اكتب "اسم الملف".</span><span class="sxs-lookup"><span data-stu-id="7548d-127">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="7548d-128">اسم الملف</span><span class="sxs-lookup"><span data-stu-id="7548d-128">File name</span></span>  
17. <span data-ttu-id="7548d-129">في الحقل "نوع الصنف"، حدد "سلسلة".</span><span class="sxs-lookup"><span data-stu-id="7548d-129">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="7548d-130">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="7548d-130">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-dynamics-365-for-finance-and-operations-data-sources"></a><span data-ttu-id="7548d-131">تعيين عناصر نموذج بيانات جديد إلى مصادر بيانات Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7548d-131">Map new data model elements to Dynamics 365 for Finance and Operations data sources</span></span>
1. <span data-ttu-id="7548d-132">انقر فوق "تعيين النموذج لمصدر البيانات".</span><span class="sxs-lookup"><span data-stu-id="7548d-132">Click Map model to datasource.</span></span>
2. <span data-ttu-id="7548d-133">استخدم عامل التصفية السريع لإجراء التصفية باستخدام حقل "التعريف" بالقيمة "InvoiceCustomer".</span><span class="sxs-lookup"><span data-stu-id="7548d-133">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="7548d-134">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="7548d-134">InvoiceCustomer</span></span>  
    * <span data-ttu-id="7548d-135">سنقوم بتعيين عناصر نماذج جديدة إلى مصادر البيانات المناسبة.</span><span class="sxs-lookup"><span data-stu-id="7548d-135">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="7548d-136">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="7548d-136">Click Designer.</span></span>
4. <span data-ttu-id="7548d-137">في الشجرة، حدد "مرفقات الفاتورة‬".</span><span class="sxs-lookup"><span data-stu-id="7548d-137">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="7548d-138">في الشجرة، قم بتوسيع "مرفقات الفاتورة‬".</span><span class="sxs-lookup"><span data-stu-id="7548d-138">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="7548d-139">في الشجرة، حدد "مرفقات الفاتورة\اسم الملف‬".</span><span class="sxs-lookup"><span data-stu-id="7548d-139">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="7548d-140">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="7548d-140">Click Edit.</span></span>
8. <span data-ttu-id="7548d-141">في حقل المعادلة، أدخل 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span><span class="sxs-lookup"><span data-stu-id="7548d-141">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="7548d-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="7548d-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="7548d-143">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="7548d-143">Click Save.</span></span>
10. <span data-ttu-id="7548d-144">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7548d-144">Close the page.</span></span>
11. <span data-ttu-id="7548d-145">في الشجرة، حدد "مرفقات الفاتورة\محتوى الملف".</span><span class="sxs-lookup"><span data-stu-id="7548d-145">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="7548d-146">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="7548d-146">Click Edit.</span></span>
13. <span data-ttu-id="7548d-147">في حقل المعادلة، أدخل 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span><span class="sxs-lookup"><span data-stu-id="7548d-147">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="7548d-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="7548d-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="7548d-149">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="7548d-149">Click Save.</span></span>
15. <span data-ttu-id="7548d-150">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7548d-150">Close the page.</span></span>
16. <span data-ttu-id="7548d-151">في الشجرة، حدد "مرفقات الفاتورة‬".</span><span class="sxs-lookup"><span data-stu-id="7548d-151">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="7548d-152">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="7548d-152">Click Edit.</span></span>
18. <span data-ttu-id="7548d-153">في حقل المعادلة، أدخل 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span><span class="sxs-lookup"><span data-stu-id="7548d-153">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="7548d-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="7548d-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="7548d-155">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="7548d-155">Click Save.</span></span>
20. <span data-ttu-id="7548d-156">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7548d-156">Close the page.</span></span>
21. <span data-ttu-id="7548d-157">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="7548d-157">Click Save.</span></span>
22. <span data-ttu-id="7548d-158">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7548d-158">Close the page.</span></span>
23. <span data-ttu-id="7548d-159">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7548d-159">Close the page.</span></span>
24. <span data-ttu-id="7548d-160">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7548d-160">Close the page.</span></span>
25. <span data-ttu-id="7548d-161">انقر فوق "تغيير الحالة".</span><span class="sxs-lookup"><span data-stu-id="7548d-161">Click Change status.</span></span>
26. <span data-ttu-id="7548d-162">انقر فوق "مكتمل".</span><span class="sxs-lookup"><span data-stu-id="7548d-162">Click Complete.</span></span>
27. <span data-ttu-id="7548d-163">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="7548d-163">Click OK.</span></span>


