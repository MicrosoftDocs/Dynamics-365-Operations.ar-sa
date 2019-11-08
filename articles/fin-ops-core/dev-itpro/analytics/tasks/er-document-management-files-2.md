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
ms.openlocfilehash: 24eba0402caefb611a212db19cdb8feafa7c1fee
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550730"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2---extend-data-model"></a><span data-ttu-id="7381a-103">التقارير الإلكترونية - استخدام ملفات إدارة المستندات في مخرجات التنسيق‬ (الجزء 2 - توسيع نموذج البيانات)</span><span class="sxs-lookup"><span data-stu-id="7381a-103">ER Use Document Management files in format outputs (Part 2 - Extend data model)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7381a-104">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لاستخدام ملفات إدارة المستندات (مرفقات) في مخرجات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="7381a-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="7381a-105">يمكن تنفيذ هذه الخطوات في أي شركة.</span><span class="sxs-lookup"><span data-stu-id="7381a-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="7381a-106">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في دليل المهمة "التقارير الإلكترونية - استخدام ملفات إدارة المستندات في مخرجات التنسيق (الجزء 1: إعداد نموذج البيانات").</span><span class="sxs-lookup"><span data-stu-id="7381a-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 1: Prepare data model)” task guide.</span></span>

<span data-ttu-id="7381a-107">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="7381a-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="7381a-108">توسيع نموذج البيانات لتقديم ملفات إدارة المستندات فيه</span><span class="sxs-lookup"><span data-stu-id="7381a-108">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="7381a-109">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="7381a-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="7381a-110">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="7381a-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="7381a-111">في الشجرة، قم بتوسيع "نموذج فاتورة العميل".</span><span class="sxs-lookup"><span data-stu-id="7381a-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="7381a-112">في الشجرة، حدد "نموذج فاتورة العميل‬/نموذج فاتورة العميل‬ (مخصص)".</span><span class="sxs-lookup"><span data-stu-id="7381a-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="7381a-113">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="7381a-113">Click Designer.</span></span>
6. <span data-ttu-id="7381a-114">في الشجرة، حدد "فاتورة العميل(InvoiceCustomer)".</span><span class="sxs-lookup"><span data-stu-id="7381a-114">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="7381a-115">سنقوم بتوسيع نموذج البيانات هذا لعرضه في أية ملفات تم إرفاقها بأمر مبيعات يرتبط بفاتورة تتم معالجتها إلكترونيًا.</span><span class="sxs-lookup"><span data-stu-id="7381a-115">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="7381a-116">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="7381a-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="7381a-117">في حقل "الاسم"، اكتب "مرفقات الفواتير".</span><span class="sxs-lookup"><span data-stu-id="7381a-117">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="7381a-118">مرفقات الفاتورة</span><span class="sxs-lookup"><span data-stu-id="7381a-118">Invoice attachments</span></span>  
9. <span data-ttu-id="7381a-119">في الحقل "نوع الصنف"، حدد "قائمة سجلات".</span><span class="sxs-lookup"><span data-stu-id="7381a-119">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="7381a-120">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="7381a-120">Click Add.</span></span>
11. <span data-ttu-id="7381a-121">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="7381a-121">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="7381a-122">في حقل "الاسم"، اكتب "محتوى الملف".</span><span class="sxs-lookup"><span data-stu-id="7381a-122">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="7381a-123">محتوى الملف</span><span class="sxs-lookup"><span data-stu-id="7381a-123">File content</span></span>  
13. <span data-ttu-id="7381a-124">في الحقل "نوع الصنف"، حدد "الحاوية".</span><span class="sxs-lookup"><span data-stu-id="7381a-124">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="7381a-125">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="7381a-125">Click Add.</span></span>
15. <span data-ttu-id="7381a-126">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="7381a-126">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="7381a-127">في حقل "الاسم"، اكتب "اسم الملف".</span><span class="sxs-lookup"><span data-stu-id="7381a-127">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="7381a-128">اسم الملف</span><span class="sxs-lookup"><span data-stu-id="7381a-128">File name</span></span>  
17. <span data-ttu-id="7381a-129">في الحقل "نوع الصنف"، حدد "سلسلة".</span><span class="sxs-lookup"><span data-stu-id="7381a-129">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="7381a-130">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="7381a-130">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-data-sources"></a><span data-ttu-id="7381a-131">تعيين عناصر نموذج بيانات جديد إلى مصادر بيانات</span><span class="sxs-lookup"><span data-stu-id="7381a-131">Map new data model elements to data sources</span></span>
1. <span data-ttu-id="7381a-132">انقر فوق "تعيين النموذج لمصدر البيانات".</span><span class="sxs-lookup"><span data-stu-id="7381a-132">Click Map model to datasource.</span></span>
2. <span data-ttu-id="7381a-133">استخدم عامل التصفية السريع لإجراء التصفية باستخدام حقل "التعريف" بالقيمة "InvoiceCustomer".</span><span class="sxs-lookup"><span data-stu-id="7381a-133">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="7381a-134">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="7381a-134">InvoiceCustomer</span></span>  
    * <span data-ttu-id="7381a-135">سنقوم بتعيين عناصر نماذج جديدة إلى مصادر البيانات المناسبة.</span><span class="sxs-lookup"><span data-stu-id="7381a-135">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="7381a-136">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="7381a-136">Click Designer.</span></span>
4. <span data-ttu-id="7381a-137">في الشجرة، حدد "مرفقات الفاتورة‬".</span><span class="sxs-lookup"><span data-stu-id="7381a-137">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="7381a-138">في الشجرة، قم بتوسيع "مرفقات الفاتورة‬".</span><span class="sxs-lookup"><span data-stu-id="7381a-138">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="7381a-139">في الشجرة، حدد "مرفقات الفاتورة\اسم الملف‬".</span><span class="sxs-lookup"><span data-stu-id="7381a-139">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="7381a-140">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="7381a-140">Click Edit.</span></span>
8. <span data-ttu-id="7381a-141">في حقل المعادلة، أدخل 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span><span class="sxs-lookup"><span data-stu-id="7381a-141">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="7381a-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="7381a-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="7381a-143">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="7381a-143">Click Save.</span></span>
10. <span data-ttu-id="7381a-144">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7381a-144">Close the page.</span></span>
11. <span data-ttu-id="7381a-145">في الشجرة، حدد "مرفقات الفاتورة\محتوى الملف".</span><span class="sxs-lookup"><span data-stu-id="7381a-145">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="7381a-146">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="7381a-146">Click Edit.</span></span>
13. <span data-ttu-id="7381a-147">في حقل المعادلة، أدخل 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span><span class="sxs-lookup"><span data-stu-id="7381a-147">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="7381a-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="7381a-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="7381a-149">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="7381a-149">Click Save.</span></span>
15. <span data-ttu-id="7381a-150">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7381a-150">Close the page.</span></span>
16. <span data-ttu-id="7381a-151">في الشجرة، حدد "مرفقات الفاتورة‬".</span><span class="sxs-lookup"><span data-stu-id="7381a-151">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="7381a-152">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="7381a-152">Click Edit.</span></span>
18. <span data-ttu-id="7381a-153">في حقل المعادلة، أدخل 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span><span class="sxs-lookup"><span data-stu-id="7381a-153">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="7381a-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="7381a-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="7381a-155">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="7381a-155">Click Save.</span></span>
20. <span data-ttu-id="7381a-156">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7381a-156">Close the page.</span></span>
21. <span data-ttu-id="7381a-157">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="7381a-157">Click Save.</span></span>
22. <span data-ttu-id="7381a-158">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7381a-158">Close the page.</span></span>
23. <span data-ttu-id="7381a-159">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7381a-159">Close the page.</span></span>
24. <span data-ttu-id="7381a-160">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7381a-160">Close the page.</span></span>
25. <span data-ttu-id="7381a-161">انقر فوق "تغيير الحالة".</span><span class="sxs-lookup"><span data-stu-id="7381a-161">Click Change status.</span></span>
26. <span data-ttu-id="7381a-162">انقر فوق "مكتمل".</span><span class="sxs-lookup"><span data-stu-id="7381a-162">Click Complete.</span></span>
27. <span data-ttu-id="7381a-163">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="7381a-163">Click OK.</span></span>

