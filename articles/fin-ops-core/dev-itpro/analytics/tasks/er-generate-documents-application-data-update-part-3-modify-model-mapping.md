---
title: تعديل النماذج والتعيينات لإنشاء مستندات تتضمن بيانات التطبيق
description: يصف هذا الموضوع كيفية تصميم تكوينات التقارير الإلكترونية لإنشاء مستند إلكتروني وتحديث بيانات التطبيق. (الجزء 2 - إنشاء المستندات).
author: NickSelin
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 78b1771d0e01702162192ff20c03facbba4f3513
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751596"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a><span data-ttu-id="3ed05-104">تعديل النماذج والتعيينات لإنشاء مستندات تتضمن بيانات التطبيق</span><span class="sxs-lookup"><span data-stu-id="3ed05-104">Modify models and mappings to generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3ed05-105">لإكمال الخطوات المذكورة في هذا الإجراء، يجب عليك أولاً إكمال الإجراء، "التقارير الإلكترونية - إنشاء مستندات بواسطة تحديث بيانات التطبيق (الجزء 2 - إنشاء المستندات)‬".</span><span class="sxs-lookup"><span data-stu-id="3ed05-105">To complete the steps in this procedure, you must first complete the procedure, "ER Generate documents with application data update (Part 2: Generate documents)".</span></span> 

<span data-ttu-id="3ed05-106">توضح الخطوات الواردة في هذا الإجراء كيفية تصميم تكوينات التقارير الإلكترونية لإنشاء مستند إلكتروني وتحديث بيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="3ed05-106">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="3ed05-107">في هذا الإجراء، ستقوم بتعديل تكوينات التقارير الإلكترونية لبدء استخدامها لإنشاء المستندات الإلكترونية وتحديث بيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="3ed05-107">In this procedure, you will modify the ER configurations to start using them to generate electronic documents and update application data.</span></span> <span data-ttu-id="3ed05-108">تم إنشاء هذا الإجراء للمستخدمين الذين لديهم دور مسؤول النظام أو مطور التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="3ed05-108">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="3ed05-109">يمكن إتمام هذه الخطوات باستخدام مجموعة بيانات DEMF.</span><span class="sxs-lookup"><span data-stu-id="3ed05-109">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-data-model"></a><span data-ttu-id="3ed05-110">تعديل نموذج البيانات</span><span class="sxs-lookup"><span data-stu-id="3ed05-110">Modify data model</span></span>
1. <span data-ttu-id="3ed05-111">انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.</span><span class="sxs-lookup"><span data-stu-id="3ed05-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="3ed05-112">في الشجرة، حدد "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (نموذج)".</span><span class="sxs-lookup"><span data-stu-id="3ed05-112">In the tree, select 'Intrastat (model)'.</span></span>
    * <span data-ttu-id="3ed05-113">ستقوم بتوسيع طريقة استخدام نموذج البيانات.</span><span class="sxs-lookup"><span data-stu-id="3ed05-113">You will extend how you use the data model.</span></span> <span data-ttu-id="3ed05-114">بالإضافة إلى استخدامه كمصدر بيانات لإنشاء تقرير نظام جمع المعلومات التجارية، سيتم استخدام نموذج البيانات لجمع تفاصيل حول عملية إعداد تقارير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="3ed05-114">Besides using it as data source to generate the Intrastat report, the data model will be used to collect details about the Intrastat reporting process.</span></span> <span data-ttu-id="3ed05-115">سيتم بعد ذلك استخدام التفاصيل لتحديث بيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="3ed05-115">The details will then be used to update application data.</span></span>   
3. <span data-ttu-id="3ed05-116">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="3ed05-116">Click Designer.</span></span>
4. <span data-ttu-id="3ed05-117">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="3ed05-117">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="3ed05-118">في الحقل "عقدة جديدة كـ‬"، أدخل "جذر النموذج‬".</span><span class="sxs-lookup"><span data-stu-id="3ed05-118">In the New node as a field, enter 'Model root'.</span></span>
6. <span data-ttu-id="3ed05-119">في حقل "الاسم"، اكتب "لتحديث بيانات التطبيق‬".</span><span class="sxs-lookup"><span data-stu-id="3ed05-119">In the Name field, type 'For application data update'.</span></span>
    * <span data-ttu-id="3ed05-120">لتحديث بيانات التطبيق</span><span class="sxs-lookup"><span data-stu-id="3ed05-120">For application data update</span></span>  
7. <span data-ttu-id="3ed05-121">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="3ed05-121">Click Add.</span></span>
8. <span data-ttu-id="3ed05-122">في الشجرة، حدد "لتحديث بيانات التطبيق".</span><span class="sxs-lookup"><span data-stu-id="3ed05-122">In the tree, select 'For application data update'.</span></span>
    * <span data-ttu-id="3ed05-123">تتم إضافة العنصر الجذر الجديد هذا لتحديد تدفق البيانات لنقل البيانات من تقرير نظام جمع المعلومات التجارية (تستخدم كمصدر بيانات) إلى جداول التطبيق (وجهة التحديث).</span><span class="sxs-lookup"><span data-stu-id="3ed05-123">This new root item is added to specify the data flow for moving data from the Intrastat report (used as a data source) to the application tables (the update destination).</span></span> <span data-ttu-id="3ed05-124">لاحظ أنه يجب استخدام عناصر جذر مختلفة للحصول على البيانات التي تم ترحيلها إلى المستند الصادر وكذلك للحصول على البيانات من المستند الذي يُستخدم لتحديث بيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="3ed05-124">Note that different root items must be used for getting data that is posted to the outgoing document and for getting data from the document that is used to update application data.</span></span>   
9. <span data-ttu-id="3ed05-125">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="3ed05-125">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="3ed05-126">في حقل "الاسم"، اكتب "رأس الأرشيف".</span><span class="sxs-lookup"><span data-stu-id="3ed05-126">In the Name field, type 'Archive header'.</span></span>
    * <span data-ttu-id="3ed05-127">رأس الأرشيف</span><span class="sxs-lookup"><span data-stu-id="3ed05-127">Archive header</span></span>  
11. <span data-ttu-id="3ed05-128">في الحقل "نوع الصنف"، حدد "قائمة سجلات".</span><span class="sxs-lookup"><span data-stu-id="3ed05-128">In the Item type field, select 'Record list'.</span></span>
12. <span data-ttu-id="3ed05-129">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="3ed05-129">Click Add.</span></span>
    * <span data-ttu-id="3ed05-130">لأنك ستقوم بإنشاء سجل لكل تقرير ينشأ لنظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي، يجب عليك إنشاء عنصر جديد له.</span><span class="sxs-lookup"><span data-stu-id="3ed05-130">Because you will create a record for each Intrastat report that is generated, you must create a new item for that.</span></span>  
13. <span data-ttu-id="3ed05-131">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="3ed05-131">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="3ed05-132">في حقل "الاسم"، اكتب "اسم الملف".</span><span class="sxs-lookup"><span data-stu-id="3ed05-132">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="3ed05-133">اسم الملف</span><span class="sxs-lookup"><span data-stu-id="3ed05-133">File name</span></span>  
15. <span data-ttu-id="3ed05-134">في الحقل "نوع الصنف"، حدد "سلسلة".</span><span class="sxs-lookup"><span data-stu-id="3ed05-134">In the Item type field, select 'String'.</span></span>
16. <span data-ttu-id="3ed05-135">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="3ed05-135">Click Add.</span></span>
17. <span data-ttu-id="3ed05-136">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="3ed05-136">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="3ed05-137">في حقل "الاسم"، اكتب "عدد البنود".</span><span class="sxs-lookup"><span data-stu-id="3ed05-137">In the Name field, type 'Number of lines'.</span></span>
    * <span data-ttu-id="3ed05-138">عدد السطور</span><span class="sxs-lookup"><span data-stu-id="3ed05-138">Number of lines</span></span>  
19. <span data-ttu-id="3ed05-139">في الحقل "نوع الصنف"، حدد "Integer".</span><span class="sxs-lookup"><span data-stu-id="3ed05-139">In the Item type field, select 'Integer'.</span></span>
20. <span data-ttu-id="3ed05-140">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="3ed05-140">Click Add.</span></span>
    * <span data-ttu-id="3ed05-141">قم بإضافة هذا العنصر لكي يمثل عدد حركات نظام جمع المعلومات التجارية التي تم الإبلاغ عنها أثناء عملية إعداد التقارير الحالية.</span><span class="sxs-lookup"><span data-stu-id="3ed05-141">Add this item to represent the number of Intrastat transactions that are reported during the current reporting process.</span></span>  
21. <span data-ttu-id="3ed05-142">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="3ed05-142">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="3ed05-143">في حقل "الاسم"، اكتب "بنود الأرشيف".</span><span class="sxs-lookup"><span data-stu-id="3ed05-143">In the Name field, type 'Archive lines'.</span></span>
    * <span data-ttu-id="3ed05-144">بنود الأرشيف</span><span class="sxs-lookup"><span data-stu-id="3ed05-144">Archive lines</span></span>  
23. <span data-ttu-id="3ed05-145">في الحقل "نوع الصنف"، حدد "قائمة سجلات".</span><span class="sxs-lookup"><span data-stu-id="3ed05-145">In the Item type field, select 'Record list'.</span></span>
24. <span data-ttu-id="3ed05-146">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="3ed05-146">Click Add.</span></span>
    * <span data-ttu-id="3ed05-147">قم بإضافة هذا العنصر لكي يمثل قائمة حركات نظام جمع المعلومات التجارية التي تم الإبلاغ عنها أثناء عملية إعداد التقارير الحالية.</span><span class="sxs-lookup"><span data-stu-id="3ed05-147">Add this item to represent the list of Intrastat transactions that are reported during the current reporting process.</span></span>  
25. <span data-ttu-id="3ed05-148">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="3ed05-148">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="3ed05-149">في الحقل "الاسم"، اكتب "المبلغ".</span><span class="sxs-lookup"><span data-stu-id="3ed05-149">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="3ed05-150">المبلغ</span><span class="sxs-lookup"><span data-stu-id="3ed05-150">Amount</span></span>  
27. <span data-ttu-id="3ed05-151">في الحقل "نوع الصنف"، حدد "حقيقي".</span><span class="sxs-lookup"><span data-stu-id="3ed05-151">In the Item type field, select 'Real'.</span></span>
28. <span data-ttu-id="3ed05-152">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="3ed05-152">Click Add.</span></span>
29. <span data-ttu-id="3ed05-153">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="3ed05-153">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="3ed05-154">في حقل "الاسم"، اكتب "معرف سجل السلع".</span><span class="sxs-lookup"><span data-stu-id="3ed05-154">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="3ed05-155">معرف سجل السلع</span><span class="sxs-lookup"><span data-stu-id="3ed05-155">Commodity rec id</span></span>  
31. <span data-ttu-id="3ed05-156">في الحقل "نوع الصنف"، حدد "Int64".</span><span class="sxs-lookup"><span data-stu-id="3ed05-156">In the Item type field, select 'Int64'.</span></span>
32. <span data-ttu-id="3ed05-157">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="3ed05-157">Click Add.</span></span>
33. <span data-ttu-id="3ed05-158">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="3ed05-158">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="3ed05-159">في حقل "الاسم"، اكتب "رقم الصنف".</span><span class="sxs-lookup"><span data-stu-id="3ed05-159">In the Name field, type 'Item number'.</span></span>
    * <span data-ttu-id="3ed05-160">رقم العنصر</span><span class="sxs-lookup"><span data-stu-id="3ed05-160">Item number</span></span>  
35. <span data-ttu-id="3ed05-161">في الحقل "نوع الصنف"، حدد "سلسلة".</span><span class="sxs-lookup"><span data-stu-id="3ed05-161">In the Item type field, select 'String'.</span></span>
36. <span data-ttu-id="3ed05-162">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="3ed05-162">Click Add.</span></span>
37. <span data-ttu-id="3ed05-163">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="3ed05-163">Click Save.</span></span>
38. <span data-ttu-id="3ed05-164">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3ed05-164">Close the page.</span></span>

## <a name="modify-model-mapping"></a><span data-ttu-id="3ed05-165">تعديل تعيين النموذج</span><span class="sxs-lookup"><span data-stu-id="3ed05-165">Modify model mapping</span></span>
1. <span data-ttu-id="3ed05-166">في الشجرة، قم بتوسيع "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (نموذج)".</span><span class="sxs-lookup"><span data-stu-id="3ed05-166">In the tree, expand 'Intrastat (model)'.</span></span>
2. <span data-ttu-id="3ed05-167">في الشجرة، حدد "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (نموذج)\نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (تعيين)".</span><span class="sxs-lookup"><span data-stu-id="3ed05-167">In the tree, select 'Intrastat (model)\Intrastat (mapping)'.</span></span>
    * <span data-ttu-id="3ed05-168">قم بتعديل تعيين النموذج الموجود لبدء استخدامه لتحديث بيانات التطبيق ولأرشفة تفاصيل إعداد تقارير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="3ed05-168">Modify the existing model mapping to start using it for  the application data update and to archive Intrastat reporting details.</span></span>  
3. <span data-ttu-id="3ed05-169">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="3ed05-169">Click Designer.</span></span>
4. <span data-ttu-id="3ed05-170">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="3ed05-170">Click New.</span></span>
5. <span data-ttu-id="3ed05-171">في حقل "الاسم"، اكتب "تحديث الأرشيف".</span><span class="sxs-lookup"><span data-stu-id="3ed05-171">In the Name field, type 'Update archive'.</span></span>
    * <span data-ttu-id="3ed05-172">تحديث الأرشيف</span><span class="sxs-lookup"><span data-stu-id="3ed05-172">Update archive</span></span>  
6. <span data-ttu-id="3ed05-173">في الحقل "اتجاه"، حدد "إلى الوجهة".</span><span class="sxs-lookup"><span data-stu-id="3ed05-173">In the Direction field, select 'To destination'.</span></span>
7. <span data-ttu-id="3ed05-174">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="3ed05-174">Click Save.</span></span>
    * <span data-ttu-id="3ed05-175">يحدد هذا التعيين الجديد تدفق البيانات لنقل البيانات (تفاصيل إعداد تقارير نظام جمع المعلومات التجارية) من نموذج البيانات إلى جداول التطبيق (وجهة التحديث).</span><span class="sxs-lookup"><span data-stu-id="3ed05-175">This new mapping specifies the data flow for moving data (Intrastat reporting details) from the data model to the application tables (the update destination).</span></span> <span data-ttu-id="3ed05-176">لاحظ أنه يجب استخدام عناصر جذر مختلفة خاصة بالنموذج للحصول على البيانات من التطبيق لعملية إعداد التقارير، وبعد ذلك استخدام البيانات من نموذج البيانات لتحديث بيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="3ed05-176">Note that different model's root items must be used to get data from the application for the reporting process and then use the data from data model for the application data update.</span></span>   
8. <span data-ttu-id="3ed05-177">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="3ed05-177">Click Designer.</span></span>
9. <span data-ttu-id="3ed05-178">في الشجرة، حدد "نموذج البيانات\نموذج البيانات".</span><span class="sxs-lookup"><span data-stu-id="3ed05-178">In the tree, select 'Data model\Data model'.</span></span>
    * <span data-ttu-id="3ed05-179">أضف مصدر البيانات مطلوب.</span><span class="sxs-lookup"><span data-stu-id="3ed05-179">Add the required data source.</span></span> <span data-ttu-id="3ed05-180">هذا هو نموذج البيانات الذي يحتوي على التفاصيل الخاصة بحركات نظام جمع المعلومات التجارية التي تم الإبلاغ عنها والتي يجب أرشفتها.</span><span class="sxs-lookup"><span data-stu-id="3ed05-180">This is the data model that contains details of the reported Intrastat transactions that must be archived.</span></span>  
10. <span data-ttu-id="3ed05-181">انقر فوق "إضافة جذر".</span><span class="sxs-lookup"><span data-stu-id="3ed05-181">Click Add root.</span></span>
11. <span data-ttu-id="3ed05-182">في حقل "الاسم"، اكتب "نموذج".</span><span class="sxs-lookup"><span data-stu-id="3ed05-182">In the Name field, type 'model'.</span></span>
    * <span data-ttu-id="3ed05-183">النموذج</span><span class="sxs-lookup"><span data-stu-id="3ed05-183">model</span></span>  
12. <span data-ttu-id="3ed05-184">في حقل "التعريف"، أدخل قيمة "لتحديث بيانات التطبيق" أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3ed05-184">In the Definition field, enter or select the value 'For application data update'.</span></span>
    * <span data-ttu-id="3ed05-185">لتحديث بيانات التطبيق</span><span class="sxs-lookup"><span data-stu-id="3ed05-185">For application data update</span></span>  
13. <span data-ttu-id="3ed05-186">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="3ed05-186">Click OK.</span></span>
14. <span data-ttu-id="3ed05-187">في الشجرة ، قم بتوسيع "النموذج"</span><span class="sxs-lookup"><span data-stu-id="3ed05-187">In the tree, expand 'model'.</span></span>
15. <span data-ttu-id="3ed05-188">في الشجرة، حدد "الدوال/المحسوب".</span><span class="sxs-lookup"><span data-stu-id="3ed05-188">In the tree, select 'Functions\Calculated field'.</span></span>
16. <span data-ttu-id="3ed05-189">في الشجرة، حدد "النموذج\رأس الأرشيف".</span><span class="sxs-lookup"><span data-stu-id="3ed05-189">In the tree, select 'model\Archive header'.</span></span>
17. <span data-ttu-id="3ed05-190">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="3ed05-190">Click Add.</span></span>
    * <span data-ttu-id="3ed05-191">لأنك ترغب في تعداد حركات نظام جمع المعلومات التجارية التي تم الإبلاغ عنها لأرشفتها، يجب إضافة مصدر البيانات الملائم.</span><span class="sxs-lookup"><span data-stu-id="3ed05-191">Because you want to enumerate reported Intrastat transactions for archiving, the appropriate data source must be added.</span></span>  
18. <span data-ttu-id="3ed05-192">في حقل "الاسم"، اكتب "البنود التي تم تعدادها‬".</span><span class="sxs-lookup"><span data-stu-id="3ed05-192">In the Name field, type 'Enumerated lines'.</span></span>
    * <span data-ttu-id="3ed05-193">البنود التي تم تعدادها</span><span class="sxs-lookup"><span data-stu-id="3ed05-193">Enumerated lines</span></span>  
19. <span data-ttu-id="3ed05-194">انقر فوق "تحرير المعادلة".</span><span class="sxs-lookup"><span data-stu-id="3ed05-194">Click Edit formula.</span></span>
20. <span data-ttu-id="3ed05-195">في الشجرة، حدد "قائمة\ENUMERATE".</span><span class="sxs-lookup"><span data-stu-id="3ed05-195">In the tree, select 'List\ENUMERATE'.</span></span>
21. <span data-ttu-id="3ed05-196">انقر فوق "إضافة دالة".</span><span class="sxs-lookup"><span data-stu-id="3ed05-196">Click Add function.</span></span>
22. <span data-ttu-id="3ed05-197">في الشجرة ، قم بتوسيع "النموذج"</span><span class="sxs-lookup"><span data-stu-id="3ed05-197">In the tree, expand 'model'.</span></span>
23. <span data-ttu-id="3ed05-198">في الشجرة، قم بتوسيع "النموذج\رأس الأرشيف".</span><span class="sxs-lookup"><span data-stu-id="3ed05-198">In the tree, expand 'model\Archive header'.</span></span>
24. <span data-ttu-id="3ed05-199">في الشجرة، حدد "النموذج\رأس الأرشيف\بنود الأرشيف".</span><span class="sxs-lookup"><span data-stu-id="3ed05-199">In the tree, select 'model\Archive header\Archive lines'.</span></span>
25. <span data-ttu-id="3ed05-200">انقر فوق "إضافة مصدر بيانات".</span><span class="sxs-lookup"><span data-stu-id="3ed05-200">Click Add data source.</span></span>
26. <span data-ttu-id="3ed05-201">في حقل المعادلة، أدخل "ENUMERATE(model.'Archive header'.'Archive lines')".</span><span class="sxs-lookup"><span data-stu-id="3ed05-201">In the Formula field, enter 'ENUMERATE(model.'Archive header'.'Archive lines')'.</span></span>
    * <span data-ttu-id="3ed05-202">ENUMERATE(النموذج.'رأس الأرشيف'.'بنود الأرشيف')</span><span class="sxs-lookup"><span data-stu-id="3ed05-202">ENUMERATE(model.'Archive header'.'Archive lines')</span></span>  
27. <span data-ttu-id="3ed05-203">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="3ed05-203">Click Save.</span></span>
28. <span data-ttu-id="3ed05-204">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3ed05-204">Close the page.</span></span>
29. <span data-ttu-id="3ed05-205">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="3ed05-205">Click OK.</span></span>
30. <span data-ttu-id="3ed05-206">انقر فوق "إضافة وجهة".</span><span class="sxs-lookup"><span data-stu-id="3ed05-206">Click Add destination.</span></span>
    * <span data-ttu-id="3ed05-207">قم بإضافة جداول التطبيق كوجهات مطلوبة تتطلب تحديثات لأرشفة التفاصيل الخاصة بحركات نظام جمع المعلومات التجارية التي تم الإبلاغ عنها.</span><span class="sxs-lookup"><span data-stu-id="3ed05-207">Add application tables as required destinations that require updates to archive details of reported Intrastat transactions.</span></span>  
31. <span data-ttu-id="3ed05-208">في حقل "الاسم"، اكتب "أرشيف".</span><span class="sxs-lookup"><span data-stu-id="3ed05-208">In the Name field, type 'Archive'.</span></span>
    * <span data-ttu-id="3ed05-209">الأرشيف</span><span class="sxs-lookup"><span data-stu-id="3ed05-209">Archive</span></span>  
32. <span data-ttu-id="3ed05-210">في حقل "اسم الجدول"، اكتب "IntrastatArchiveGeneral".</span><span class="sxs-lookup"><span data-stu-id="3ed05-210">In the Table name field, type 'IntrastatArchiveGeneral'.</span></span>
    * <span data-ttu-id="3ed05-211">IntrastatArchiveGeneral</span><span class="sxs-lookup"><span data-stu-id="3ed05-211">IntrastatArchiveGeneral</span></span>  
    * <span data-ttu-id="3ed05-212">احتفظ بسجل الإجراء "إدراج" لكي تتمكن من إضافة السجلات أثناء عملية أرشفة التفاصيل الخاصة بكل عمليات إعداد تقارير نظام جمع المعلومات التجارية.</span><span class="sxs-lookup"><span data-stu-id="3ed05-212">Keep the record action 'Insert' so you can add records during the detail archiving of each Intrastat reporting process.</span></span>  
33. <span data-ttu-id="3ed05-213">حدد "نعم" في حقل "سجل معلومات السجل‬".</span><span class="sxs-lookup"><span data-stu-id="3ed05-213">Select Yes in the Record infolog field.</span></span>
    * <span data-ttu-id="3ed05-214">حدد "نعم" للحصول على معلومات حول مشكلات تحديث بيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="3ed05-214">Select Yes to get information about issues with the application data update.</span></span>  
34. <span data-ttu-id="3ed05-215">حدد "نعم" في الحقل "تخطي التحقق من صحة إجراء السجل‬".</span><span class="sxs-lookup"><span data-stu-id="3ed05-215">Select Yes in the Skip record action validation field.</span></span>
    * <span data-ttu-id="3ed05-216">حدد "نعم" لمنع أخطاء التحقق من الصحة حول الحقل الفارغ "معرف أرشيف نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬".</span><span class="sxs-lookup"><span data-stu-id="3ed05-216">Select Yes to suppress validation errors about the empty 'Intrastat archive ID' field.</span></span> <span data-ttu-id="3ed05-217">سيتم إجراء ذلك بعد إضافة السجلات، استنادًا إلى إعدادات الأرقام التسلسلية التي تم تكوينها لهذا الجدول في نموذج "محددات التجارة الخارجية".</span><span class="sxs-lookup"><span data-stu-id="3ed05-217">This will be done after records are added, based on the sequence number settings that are configured for this table in the Foreign trade parameters form.</span></span>  
35. <span data-ttu-id="3ed05-218">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="3ed05-218">Click OK.</span></span>
    * <span data-ttu-id="3ed05-219">اعمل على ربط عناصر مصدر البيانات المضاف (النموذج المصفى استنادًا إلى العنصر الجذر المحدد) مع عناصر من الوجهة المضافة.</span><span class="sxs-lookup"><span data-stu-id="3ed05-219">Bind elements of the added data source (the filtered model based on the selected root item) with elements from the added destination.</span></span>  
36. <span data-ttu-id="3ed05-220">في الشجرة، قم بتوسيع ''أرشيف".</span><span class="sxs-lookup"><span data-stu-id="3ed05-220">In the tree, expand 'Archive'.</span></span>
37. <span data-ttu-id="3ed05-221">في الشجرة، قم بتوسيع "أرشيف‏‎\<علاقات".</span><span class="sxs-lookup"><span data-stu-id="3ed05-221">In the tree, expand 'Archive\<Relations'.</span></span>
38. <span data-ttu-id="3ed05-222">في الشجرة، قم بتوسيع "أرشيف\<علاقات\IntrastatArchiveDetail".</span><span class="sxs-lookup"><span data-stu-id="3ed05-222">In the tree, expand 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
39. <span data-ttu-id="3ed05-223">في الشجرة، حدد "أرشيف\<علاقات\IntrastatArchiveDetail\مبلغ(AmountMST)".</span><span class="sxs-lookup"><span data-stu-id="3ed05-223">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)'.</span></span>
40. <span data-ttu-id="3ed05-224">في الشجرة، قم بتوسيع "النموذج\رأس الأرشيف\البنود التي تم تعدادها‬".</span><span class="sxs-lookup"><span data-stu-id="3ed05-224">In the tree, expand 'model\Archive header\Enumerated lines'.</span></span>
41. <span data-ttu-id="3ed05-225">في الشجرة، قم بتوسيع "النموذج\رأس الأرشيف\البنود التي تم تعدادها‬\القيمة".</span><span class="sxs-lookup"><span data-stu-id="3ed05-225">In the tree, expand 'model\Archive header\Enumerated lines\Value'.</span></span>
42. <span data-ttu-id="3ed05-226">في الشجرة، حدد "النموذج\رأس الأرشيف\البنود التي تم تعدادها\القيمة\المبلغ".</span><span class="sxs-lookup"><span data-stu-id="3ed05-226">In the tree, select 'model\Archive header\Enumerated lines\Value\Amount'.</span></span>
43. <span data-ttu-id="3ed05-227">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="3ed05-227">Click Bind.</span></span>
44. <span data-ttu-id="3ed05-228">في الشجرة، حدد "أرشيف\<علاقات\IntrastatArchiveDetail\السلع(IntrastatCommodity)'.</span><span class="sxs-lookup"><span data-stu-id="3ed05-228">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)'.</span></span>
45. <span data-ttu-id="3ed05-229">في الشجرة، حدد "النموذج\رأس الأرشيف\البنود التي تم تعدادها\القيمة\معرف سجل السلع".</span><span class="sxs-lookup"><span data-stu-id="3ed05-229">In the tree, select 'model\Archive header\Enumerated lines\Value\Commodity rec id'.</span></span>
46. <span data-ttu-id="3ed05-230">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="3ed05-230">Click Bind.</span></span>
47. <span data-ttu-id="3ed05-231">في الشجرة، حدد "أرشيف\<علاقات\IntrastatArchiveDetail\رقم الصنف(ItemId)".</span><span class="sxs-lookup"><span data-stu-id="3ed05-231">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)'.</span></span>
48. <span data-ttu-id="3ed05-232">في الشجرة، حدد "النموذج\رأس الأرشيف\البنود التي تم تعدادها\القيمة\رقم الصنف".</span><span class="sxs-lookup"><span data-stu-id="3ed05-232">In the tree, select 'model\Archive header\Enumerated lines\Value\Item number'.</span></span>
49. <span data-ttu-id="3ed05-233">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="3ed05-233">Click Bind.</span></span>
50. <span data-ttu-id="3ed05-234">في الشجرة، حدد "أرشيف\<علاقات\IntrastatArchiveDetail\رقم البند(LineNumber)".</span><span class="sxs-lookup"><span data-stu-id="3ed05-234">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)'.</span></span>
51. <span data-ttu-id="3ed05-235">في الشجرة، حدد "النموذج\رأس الأرشيف\البنود التي تم تعدادها\الرقم".</span><span class="sxs-lookup"><span data-stu-id="3ed05-235">In the tree, select 'model\Archive header\Enumerated lines\Number'.</span></span>
52. <span data-ttu-id="3ed05-236">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="3ed05-236">Click Bind.</span></span>
53. <span data-ttu-id="3ed05-237">في الشجرة، حدد "أرشيف\<علاقات\IntrastatArchiveDetail".</span><span class="sxs-lookup"><span data-stu-id="3ed05-237">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
54. <span data-ttu-id="3ed05-238">في الشجرة، حدد "النموذج\رأس الأرشيف\البنود التي تم تعدادها‬".</span><span class="sxs-lookup"><span data-stu-id="3ed05-238">In the tree, select 'model\Archive header\Enumerated lines'.</span></span>
55. <span data-ttu-id="3ed05-239">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="3ed05-239">Click Bind.</span></span>
56. <span data-ttu-id="3ed05-240">في الشجرة، حدد "أرشيف\اسم الملف(FileName)".</span><span class="sxs-lookup"><span data-stu-id="3ed05-240">In the tree, select 'Archive\File name(FileName)'.</span></span>
57. <span data-ttu-id="3ed05-241">في الشجرة، حدد "نموذج\رأس الأرشيف\اسم الملف".</span><span class="sxs-lookup"><span data-stu-id="3ed05-241">In the tree, select 'model\Archive header\File name'.</span></span>
58. <span data-ttu-id="3ed05-242">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="3ed05-242">Click Bind.</span></span>
59. <span data-ttu-id="3ed05-243">في الشجرة، حدد "أرشيف\عدد الأسطر(NumberOfLines)".</span><span class="sxs-lookup"><span data-stu-id="3ed05-243">In the tree, select 'Archive\Number of lines(NumberOfLines)'.</span></span>
60. <span data-ttu-id="3ed05-244">في الشجرة، حدد "النموذج\رأس الأرشيف\عدد الأسطر‬".</span><span class="sxs-lookup"><span data-stu-id="3ed05-244">In the tree, select 'model\Archive header\Number of lines'.</span></span>
61. <span data-ttu-id="3ed05-245">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="3ed05-245">Click Bind.</span></span>
62. <span data-ttu-id="3ed05-246">في الشجرة، حدد "أرشيف".</span><span class="sxs-lookup"><span data-stu-id="3ed05-246">In the tree, select 'Archive'.</span></span>
63. <span data-ttu-id="3ed05-247">في الشجرة، حدد "النموذج\رأس الأرشيف".</span><span class="sxs-lookup"><span data-stu-id="3ed05-247">In the tree, select 'model\Archive header'.</span></span>
64. <span data-ttu-id="3ed05-248">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="3ed05-248">Click Bind.</span></span>
65. <span data-ttu-id="3ed05-249">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="3ed05-249">Click Save.</span></span>
66. <span data-ttu-id="3ed05-250">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3ed05-250">Close the page.</span></span>
67. <span data-ttu-id="3ed05-251">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3ed05-251">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]