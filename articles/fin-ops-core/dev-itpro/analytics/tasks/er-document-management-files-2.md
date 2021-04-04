---
title: التقارير الإلكترونية - استخدام ملفات إدارة المستندات في مخرجات التنسيق‬ (الجزء 2 - توسيع نموذج البيانات)
description: يوضح هذا الموضوع كيفيه تكوين تنسيق التقارير الكترونيه (ER) لاستخدام ملفات أداره المستندات (المرفقات) في إخراج ER. (جزء 2)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b47c35790ce04a494b6c58f6e04fa9b829d2ab93
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559763"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2---extend-data-model"></a><span data-ttu-id="e5e63-104">التقارير الإلكترونية - استخدام ملفات إدارة المستندات في مخرجات التنسيق‬ (الجزء 2 - توسيع نموذج البيانات)</span><span class="sxs-lookup"><span data-stu-id="e5e63-104">ER Use Document Management files in format outputs (Part 2 - Extend data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e5e63-105">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق تقارير إلكترونية لاستخدام ملفات إدارة المستندات (مرفقات) في مخرجات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="e5e63-105">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="e5e63-106">يمكن تنفيذ هذه الخطوات في أي شركة.</span><span class="sxs-lookup"><span data-stu-id="e5e63-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="e5e63-107">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في دليل المهمة "التقارير الإلكترونية - استخدام ملفات إدارة المستندات في مخرجات التنسيق (الجزء 1: إعداد نموذج البيانات").</span><span class="sxs-lookup"><span data-stu-id="e5e63-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 1: Prepare data model)" task guide.</span></span>

<span data-ttu-id="e5e63-108">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="e5e63-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="e5e63-109">توسيع نموذج البيانات لتقديم ملفات إدارة المستندات فيه</span><span class="sxs-lookup"><span data-stu-id="e5e63-109">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="e5e63-110">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="e5e63-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="e5e63-111">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="e5e63-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="e5e63-112">في الشجرة، قم بتوسيع "نموذج فاتورة العميل".</span><span class="sxs-lookup"><span data-stu-id="e5e63-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="e5e63-113">في الشجرة، حدد "نموذج فاتورة العميل‬/نموذج فاتورة العميل‬ (مخصص)".</span><span class="sxs-lookup"><span data-stu-id="e5e63-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="e5e63-114">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="e5e63-114">Click Designer.</span></span>
6. <span data-ttu-id="e5e63-115">في الشجرة، حدد "فاتورة العميل(InvoiceCustomer)".</span><span class="sxs-lookup"><span data-stu-id="e5e63-115">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="e5e63-116">سنقوم بتوسيع نموذج البيانات هذا لعرضه في أية ملفات تم إرفاقها بأمر مبيعات يرتبط بفاتورة تتم معالجتها إلكترونيًا.</span><span class="sxs-lookup"><span data-stu-id="e5e63-116">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="e5e63-117">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="e5e63-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="e5e63-118">في حقل "الاسم"، اكتب "مرفقات الفواتير".</span><span class="sxs-lookup"><span data-stu-id="e5e63-118">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="e5e63-119">مرفقات الفاتورة</span><span class="sxs-lookup"><span data-stu-id="e5e63-119">Invoice attachments</span></span>  
9. <span data-ttu-id="e5e63-120">في الحقل "نوع الصنف"، حدد "قائمة سجلات".</span><span class="sxs-lookup"><span data-stu-id="e5e63-120">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="e5e63-121">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="e5e63-121">Click Add.</span></span>
11. <span data-ttu-id="e5e63-122">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="e5e63-122">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="e5e63-123">في حقل "الاسم"، اكتب "محتوى الملف".</span><span class="sxs-lookup"><span data-stu-id="e5e63-123">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="e5e63-124">محتوى الملف</span><span class="sxs-lookup"><span data-stu-id="e5e63-124">File content</span></span>  
13. <span data-ttu-id="e5e63-125">في الحقل "نوع الصنف"، حدد "الحاوية".</span><span class="sxs-lookup"><span data-stu-id="e5e63-125">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="e5e63-126">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="e5e63-126">Click Add.</span></span>
15. <span data-ttu-id="e5e63-127">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="e5e63-127">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="e5e63-128">في حقل "الاسم"، اكتب "اسم الملف".</span><span class="sxs-lookup"><span data-stu-id="e5e63-128">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="e5e63-129">اسم الملف</span><span class="sxs-lookup"><span data-stu-id="e5e63-129">File name</span></span>  
17. <span data-ttu-id="e5e63-130">في الحقل "نوع الصنف"، حدد "سلسلة".</span><span class="sxs-lookup"><span data-stu-id="e5e63-130">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="e5e63-131">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="e5e63-131">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-data-sources"></a><span data-ttu-id="e5e63-132">تعيين عناصر نموذج بيانات جديد إلى مصادر بيانات</span><span class="sxs-lookup"><span data-stu-id="e5e63-132">Map new data model elements to data sources</span></span>
1. <span data-ttu-id="e5e63-133">انقر فوق "تعيين النموذج لمصدر البيانات".</span><span class="sxs-lookup"><span data-stu-id="e5e63-133">Click Map model to datasource.</span></span>
2. <span data-ttu-id="e5e63-134">استخدم عامل التصفية السريع لإجراء التصفية باستخدام حقل "التعريف" بالقيمة "InvoiceCustomer".</span><span class="sxs-lookup"><span data-stu-id="e5e63-134">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="e5e63-135">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="e5e63-135">InvoiceCustomer</span></span>  
    * <span data-ttu-id="e5e63-136">سنقوم بتعيين عناصر نماذج جديدة إلى مصادر البيانات المناسبة.</span><span class="sxs-lookup"><span data-stu-id="e5e63-136">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="e5e63-137">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="e5e63-137">Click Designer.</span></span>
4. <span data-ttu-id="e5e63-138">في الشجرة، حدد "مرفقات الفاتورة‬".</span><span class="sxs-lookup"><span data-stu-id="e5e63-138">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="e5e63-139">في الشجرة، قم بتوسيع "مرفقات الفاتورة‬".</span><span class="sxs-lookup"><span data-stu-id="e5e63-139">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="e5e63-140">في الشجرة، حدد "مرفقات الفاتورة\اسم الملف‬".</span><span class="sxs-lookup"><span data-stu-id="e5e63-140">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="e5e63-141">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="e5e63-141">Click Edit.</span></span>
8. <span data-ttu-id="e5e63-142">في حقل المعادلة، أدخل 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span><span class="sxs-lookup"><span data-stu-id="e5e63-142">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="e5e63-143">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="e5e63-143">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="e5e63-144">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="e5e63-144">Click Save.</span></span>
10. <span data-ttu-id="e5e63-145">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e5e63-145">Close the page.</span></span>
11. <span data-ttu-id="e5e63-146">في الشجرة، حدد "مرفقات الفاتورة\محتوى الملف".</span><span class="sxs-lookup"><span data-stu-id="e5e63-146">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="e5e63-147">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="e5e63-147">Click Edit.</span></span>
13. <span data-ttu-id="e5e63-148">في حقل المعادلة، أدخل 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span><span class="sxs-lookup"><span data-stu-id="e5e63-148">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="e5e63-149">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="e5e63-149">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="e5e63-150">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="e5e63-150">Click Save.</span></span>
15. <span data-ttu-id="e5e63-151">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e5e63-151">Close the page.</span></span>
16. <span data-ttu-id="e5e63-152">في الشجرة، حدد "مرفقات الفاتورة‬".</span><span class="sxs-lookup"><span data-stu-id="e5e63-152">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="e5e63-153">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="e5e63-153">Click Edit.</span></span>
18. <span data-ttu-id="e5e63-154">في حقل المعادلة، أدخل 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span><span class="sxs-lookup"><span data-stu-id="e5e63-154">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="e5e63-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="e5e63-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="e5e63-156">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="e5e63-156">Click Save.</span></span>
20. <span data-ttu-id="e5e63-157">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e5e63-157">Close the page.</span></span>
21. <span data-ttu-id="e5e63-158">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="e5e63-158">Click Save.</span></span>
22. <span data-ttu-id="e5e63-159">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e5e63-159">Close the page.</span></span>
23. <span data-ttu-id="e5e63-160">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e5e63-160">Close the page.</span></span>
24. <span data-ttu-id="e5e63-161">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e5e63-161">Close the page.</span></span>
25. <span data-ttu-id="e5e63-162">انقر فوق "تغيير الحالة".</span><span class="sxs-lookup"><span data-stu-id="e5e63-162">Click Change status.</span></span>
26. <span data-ttu-id="e5e63-163">انقر فوق "مكتمل".</span><span class="sxs-lookup"><span data-stu-id="e5e63-163">Click Complete.</span></span>
27. <span data-ttu-id="e5e63-164">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="e5e63-164">Click OK.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]