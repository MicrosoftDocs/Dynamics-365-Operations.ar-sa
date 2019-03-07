---
title: التقارير الإلكترونية - استخدام ملفات إدارة المستندات في مخرجات التنسيق‬ (الجزء 2 - توسيع نموذج البيانات)
description: تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لاستخدام ملفات إدارة المستندات (مرفقات) في مخرجات التقارير الإلكترونية.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cb4c58dc86a159a70634c05408a8db471ebcae4c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "320939"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2-extend-data-model"></a><span data-ttu-id="9cc24-103">التقارير الإلكترونية - استخدام ملفات إدارة المستندات في مخرجات التنسيق‬ (الجزء 2: توسيع نموذج البيانات)</span><span class="sxs-lookup"><span data-stu-id="9cc24-103">ER Use Document Management files in format outputs (Part 2: Extend data model)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9cc24-104">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لاستخدام ملفات إدارة المستندات (مرفقات) في مخرجات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="9cc24-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="9cc24-105">يمكن تنفيذ هذه الخطوات في أي شركة.</span><span class="sxs-lookup"><span data-stu-id="9cc24-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="9cc24-106">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في دليل المهمة "التقارير الإلكترونية - استخدام ملفات إدارة المستندات في مخرجات التنسيق (الجزء 1: إعداد نموذج البيانات").</span><span class="sxs-lookup"><span data-stu-id="9cc24-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 1: Prepare data model)” task guide.</span></span>

<span data-ttu-id="9cc24-107">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="9cc24-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="9cc24-108">توسيع نموذج البيانات لتقديم ملفات إدارة المستندات فيه</span><span class="sxs-lookup"><span data-stu-id="9cc24-108">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="9cc24-109">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="9cc24-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="9cc24-110">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="9cc24-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="9cc24-111">في الشجرة، قم بتوسيع "نموذج فاتورة العميل".</span><span class="sxs-lookup"><span data-stu-id="9cc24-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="9cc24-112">في الشجرة، حدد "نموذج فاتورة العميل‬/نموذج فاتورة العميل‬ (مخصص)".</span><span class="sxs-lookup"><span data-stu-id="9cc24-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="9cc24-113">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="9cc24-113">Click Designer.</span></span>
6. <span data-ttu-id="9cc24-114">في الشجرة، حدد "فاتورة العميل(InvoiceCustomer)".</span><span class="sxs-lookup"><span data-stu-id="9cc24-114">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="9cc24-115">سنقوم بتوسيع نموذج البيانات هذا لعرضه في أية ملفات تم إرفاقها بأمر مبيعات يرتبط بفاتورة تتم معالجتها إلكترونيًا.</span><span class="sxs-lookup"><span data-stu-id="9cc24-115">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="9cc24-116">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="9cc24-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="9cc24-117">في حقل "الاسم"، اكتب "مرفقات الفواتير".</span><span class="sxs-lookup"><span data-stu-id="9cc24-117">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="9cc24-118">مرفقات الفاتورة</span><span class="sxs-lookup"><span data-stu-id="9cc24-118">Invoice attachments</span></span>  
9. <span data-ttu-id="9cc24-119">في الحقل "نوع الصنف"، حدد "قائمة سجلات".</span><span class="sxs-lookup"><span data-stu-id="9cc24-119">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="9cc24-120">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="9cc24-120">Click Add.</span></span>
11. <span data-ttu-id="9cc24-121">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="9cc24-121">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="9cc24-122">في حقل "الاسم"، اكتب "محتوى الملف".</span><span class="sxs-lookup"><span data-stu-id="9cc24-122">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="9cc24-123">محتوى الملف</span><span class="sxs-lookup"><span data-stu-id="9cc24-123">File content</span></span>  
13. <span data-ttu-id="9cc24-124">في الحقل "نوع الصنف"، حدد "الحاوية".</span><span class="sxs-lookup"><span data-stu-id="9cc24-124">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="9cc24-125">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="9cc24-125">Click Add.</span></span>
15. <span data-ttu-id="9cc24-126">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="9cc24-126">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="9cc24-127">في حقل "الاسم"، اكتب "اسم الملف".</span><span class="sxs-lookup"><span data-stu-id="9cc24-127">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="9cc24-128">اسم الملف</span><span class="sxs-lookup"><span data-stu-id="9cc24-128">File name</span></span>  
17. <span data-ttu-id="9cc24-129">في الحقل "نوع الصنف"، حدد "سلسلة".</span><span class="sxs-lookup"><span data-stu-id="9cc24-129">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="9cc24-130">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="9cc24-130">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-dynamics-365-for-finance-and-operations-enterprise-edition-data-sources"></a><span data-ttu-id="9cc24-131">تعيين عناصر نموذج بيانات جديد إلى مصادر بيانات Dynamics 365 for Finance and Operations, Enterprise edition</span><span class="sxs-lookup"><span data-stu-id="9cc24-131">Map new data model elements to Dynamics 365 for Finance and Operations, Enterprise edition data sources</span></span>
1. <span data-ttu-id="9cc24-132">انقر فوق "تعيين النموذج لمصدر البيانات".</span><span class="sxs-lookup"><span data-stu-id="9cc24-132">Click Map model to datasource.</span></span>
2. <span data-ttu-id="9cc24-133">استخدم عامل التصفية السريع لإجراء التصفية باستخدام حقل "التعريف" بالقيمة "InvoiceCustomer".</span><span class="sxs-lookup"><span data-stu-id="9cc24-133">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="9cc24-134">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="9cc24-134">InvoiceCustomer</span></span>  
    * <span data-ttu-id="9cc24-135">سنقوم بتعيين عناصر نماذج جديدة إلى مصادر البيانات المناسبة.</span><span class="sxs-lookup"><span data-stu-id="9cc24-135">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="9cc24-136">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="9cc24-136">Click Designer.</span></span>
4. <span data-ttu-id="9cc24-137">في الشجرة، حدد "مرفقات الفاتورة‬".</span><span class="sxs-lookup"><span data-stu-id="9cc24-137">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="9cc24-138">في الشجرة، قم بتوسيع "مرفقات الفاتورة‬".</span><span class="sxs-lookup"><span data-stu-id="9cc24-138">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="9cc24-139">في الشجرة، حدد "مرفقات الفاتورة\اسم الملف‬".</span><span class="sxs-lookup"><span data-stu-id="9cc24-139">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="9cc24-140">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="9cc24-140">Click Edit.</span></span>
8. <span data-ttu-id="9cc24-141">في حقل المعادلة، أدخل 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span><span class="sxs-lookup"><span data-stu-id="9cc24-141">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="9cc24-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="9cc24-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="9cc24-143">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="9cc24-143">Click Save.</span></span>
10. <span data-ttu-id="9cc24-144">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9cc24-144">Close the page.</span></span>
11. <span data-ttu-id="9cc24-145">في الشجرة، حدد "مرفقات الفاتورة\محتوى الملف".</span><span class="sxs-lookup"><span data-stu-id="9cc24-145">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="9cc24-146">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="9cc24-146">Click Edit.</span></span>
13. <span data-ttu-id="9cc24-147">في حقل المعادلة، أدخل 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span><span class="sxs-lookup"><span data-stu-id="9cc24-147">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="9cc24-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="9cc24-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="9cc24-149">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="9cc24-149">Click Save.</span></span>
15. <span data-ttu-id="9cc24-150">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9cc24-150">Close the page.</span></span>
16. <span data-ttu-id="9cc24-151">في الشجرة، حدد "مرفقات الفاتورة‬".</span><span class="sxs-lookup"><span data-stu-id="9cc24-151">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="9cc24-152">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="9cc24-152">Click Edit.</span></span>
18. <span data-ttu-id="9cc24-153">في حقل المعادلة، أدخل 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span><span class="sxs-lookup"><span data-stu-id="9cc24-153">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="9cc24-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="9cc24-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="9cc24-155">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="9cc24-155">Click Save.</span></span>
20. <span data-ttu-id="9cc24-156">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9cc24-156">Close the page.</span></span>
21. <span data-ttu-id="9cc24-157">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="9cc24-157">Click Save.</span></span>
22. <span data-ttu-id="9cc24-158">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9cc24-158">Close the page.</span></span>
23. <span data-ttu-id="9cc24-159">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9cc24-159">Close the page.</span></span>
24. <span data-ttu-id="9cc24-160">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9cc24-160">Close the page.</span></span>
25. <span data-ttu-id="9cc24-161">انقر فوق "تغيير الحالة".</span><span class="sxs-lookup"><span data-stu-id="9cc24-161">Click Change status.</span></span>
26. <span data-ttu-id="9cc24-162">انقر فوق "مكتمل".</span><span class="sxs-lookup"><span data-stu-id="9cc24-162">Click Complete.</span></span>
27. <span data-ttu-id="9cc24-163">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="9cc24-163">Click OK.</span></span>

