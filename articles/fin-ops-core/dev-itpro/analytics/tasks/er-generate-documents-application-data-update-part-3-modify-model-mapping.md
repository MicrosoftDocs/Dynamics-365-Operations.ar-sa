---
title: تعديل النماذج والتعيينات لإنشاء مستندات تتضمن بيانات التطبيق
description: لإكمال الخطوات المذكورة في هذا الإجراء، يجب عليك أولاً إكمال الإجراء، "التقارير الإلكترونية - إنشاء مستندات بواسطة تحديث بيانات التطبيق (الجزء 2 - إنشاء المستندات)‬".
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4546de2c5c1773aadce0ec084ee7058ff2ae153
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141869"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a><span data-ttu-id="b597a-103">تعديل النماذج والتعيينات لإنشاء مستندات تتضمن بيانات التطبيق</span><span class="sxs-lookup"><span data-stu-id="b597a-103">Modify models and mappings to generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b597a-104">لإكمال الخطوات المذكورة في هذا الإجراء، يجب عليك أولاً إكمال الإجراء، "التقارير الإلكترونية - إنشاء مستندات بواسطة تحديث بيانات التطبيق (الجزء 2 - إنشاء المستندات)‬".</span><span class="sxs-lookup"><span data-stu-id="b597a-104">To complete the steps in this procedure, you must first complete the procedure, "ER Generate documents with application data update (Part 2: Generate documents)".</span></span> 

<span data-ttu-id="b597a-105">توضح الخطوات الواردة في هذا الإجراء كيفية تصميم تكوينات التقارير الإلكترونية لإنشاء مستند إلكتروني وتحديث بيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="b597a-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="b597a-106">في هذا الإجراء، ستقوم بتعديل تكوينات التقارير الإلكترونية لبدء استخدامها لإنشاء المستندات الإلكترونية وتحديث بيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="b597a-106">In this procedure, you will modify the ER configurations to start using them to generate electronic documents and update application data.</span></span> <span data-ttu-id="b597a-107">تم إنشاء هذا الإجراء للمستخدمين الذين لديهم دور مسؤول النظام أو مطور التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="b597a-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="b597a-108">يمكن إتمام هذه الخطوات باستخدام مجموعة بيانات DEMF.</span><span class="sxs-lookup"><span data-stu-id="b597a-108">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-data-model"></a><span data-ttu-id="b597a-109">تعديل نموذج البيانات</span><span class="sxs-lookup"><span data-stu-id="b597a-109">Modify data model</span></span>
1. <span data-ttu-id="b597a-110">انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.</span><span class="sxs-lookup"><span data-stu-id="b597a-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="b597a-111">في الشجرة، حدد "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (نموذج)".</span><span class="sxs-lookup"><span data-stu-id="b597a-111">In the tree, select 'Intrastat (model)'.</span></span>
    * <span data-ttu-id="b597a-112">ستقوم بتوسيع طريقة استخدام نموذج البيانات.</span><span class="sxs-lookup"><span data-stu-id="b597a-112">You will extend how you use the data model.</span></span> <span data-ttu-id="b597a-113">بالإضافة إلى استخدامه كمصدر بيانات لإنشاء تقرير نظام جمع المعلومات التجارية، سيتم استخدام نموذج البيانات لجمع تفاصيل حول عملية إعداد تقارير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="b597a-113">Besides using it as data source to generate the Intrastat report, the data model will be used to collect details about the Intrastat reporting process.</span></span> <span data-ttu-id="b597a-114">سيتم بعد ذلك استخدام التفاصيل لتحديث بيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="b597a-114">The details will then be used to update application data.</span></span>   
3. <span data-ttu-id="b597a-115">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="b597a-115">Click Designer.</span></span>
4. <span data-ttu-id="b597a-116">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="b597a-116">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="b597a-117">في الحقل "عقدة جديدة كـ‬"، أدخل "جذر النموذج‬".</span><span class="sxs-lookup"><span data-stu-id="b597a-117">In the New node as a field, enter 'Model root'.</span></span>
6. <span data-ttu-id="b597a-118">في حقل "الاسم"، اكتب "لتحديث بيانات التطبيق‬".</span><span class="sxs-lookup"><span data-stu-id="b597a-118">In the Name field, type 'For application data update'.</span></span>
    * <span data-ttu-id="b597a-119">لتحديث بيانات التطبيق</span><span class="sxs-lookup"><span data-stu-id="b597a-119">For application data update</span></span>  
7. <span data-ttu-id="b597a-120">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="b597a-120">Click Add.</span></span>
8. <span data-ttu-id="b597a-121">في الشجرة، حدد "لتحديث بيانات التطبيق".</span><span class="sxs-lookup"><span data-stu-id="b597a-121">In the tree, select 'For application data update'.</span></span>
    * <span data-ttu-id="b597a-122">تتم إضافة العنصر الجذر الجديد هذا لتحديد تدفق البيانات لنقل البيانات من تقرير نظام جمع المعلومات التجارية (تستخدم كمصدر بيانات) إلى جداول التطبيق (وجهة التحديث).</span><span class="sxs-lookup"><span data-stu-id="b597a-122">This new root item is added to specify the data flow for moving data from the Intrastat report (used as a data source) to the application tables (the update destination).</span></span> <span data-ttu-id="b597a-123">لاحظ أنه يجب استخدام عناصر جذر مختلفة للحصول على البيانات التي تم ترحيلها إلى المستند الصادر وكذلك للحصول على البيانات من المستند الذي يُستخدم لتحديث بيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="b597a-123">Note that different root items must be used for getting data that is posted to the outgoing document and for getting data from the document that is used to update application data.</span></span>   
9. <span data-ttu-id="b597a-124">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="b597a-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="b597a-125">في حقل "الاسم"، اكتب "رأس الأرشيف".</span><span class="sxs-lookup"><span data-stu-id="b597a-125">In the Name field, type 'Archive header'.</span></span>
    * <span data-ttu-id="b597a-126">رأس الأرشيف</span><span class="sxs-lookup"><span data-stu-id="b597a-126">Archive header</span></span>  
11. <span data-ttu-id="b597a-127">في الحقل "نوع الصنف"، حدد "قائمة سجلات".</span><span class="sxs-lookup"><span data-stu-id="b597a-127">In the Item type field, select 'Record list'.</span></span>
12. <span data-ttu-id="b597a-128">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="b597a-128">Click Add.</span></span>
    * <span data-ttu-id="b597a-129">لأنك ستقوم بإنشاء سجل لكل تقرير ينشأ لنظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي، يجب عليك إنشاء عنصر جديد له.</span><span class="sxs-lookup"><span data-stu-id="b597a-129">Because you will create a record for each Intrastat report that is generated, you must create a new item for that.</span></span>  
13. <span data-ttu-id="b597a-130">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="b597a-130">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="b597a-131">في حقل "الاسم"، اكتب "اسم الملف".</span><span class="sxs-lookup"><span data-stu-id="b597a-131">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="b597a-132">اسم الملف</span><span class="sxs-lookup"><span data-stu-id="b597a-132">File name</span></span>  
15. <span data-ttu-id="b597a-133">في الحقل "نوع الصنف"، حدد "سلسلة".</span><span class="sxs-lookup"><span data-stu-id="b597a-133">In the Item type field, select 'String'.</span></span>
16. <span data-ttu-id="b597a-134">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="b597a-134">Click Add.</span></span>
17. <span data-ttu-id="b597a-135">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="b597a-135">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="b597a-136">في حقل "الاسم"، اكتب "عدد البنود".</span><span class="sxs-lookup"><span data-stu-id="b597a-136">In the Name field, type 'Number of lines'.</span></span>
    * <span data-ttu-id="b597a-137">عدد السطور</span><span class="sxs-lookup"><span data-stu-id="b597a-137">Number of lines</span></span>  
19. <span data-ttu-id="b597a-138">في الحقل "نوع الصنف"، حدد "Integer".</span><span class="sxs-lookup"><span data-stu-id="b597a-138">In the Item type field, select 'Integer'.</span></span>
20. <span data-ttu-id="b597a-139">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="b597a-139">Click Add.</span></span>
    * <span data-ttu-id="b597a-140">قم بإضافة هذا العنصر لكي يمثل عدد حركات نظام جمع المعلومات التجارية التي تم الإبلاغ عنها أثناء عملية إعداد التقارير الحالية.</span><span class="sxs-lookup"><span data-stu-id="b597a-140">Add this item to represent the number of Intrastat transactions that are reported during the current reporting process.</span></span>  
21. <span data-ttu-id="b597a-141">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="b597a-141">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="b597a-142">في حقل "الاسم"، اكتب "بنود الأرشيف".</span><span class="sxs-lookup"><span data-stu-id="b597a-142">In the Name field, type 'Archive lines'.</span></span>
    * <span data-ttu-id="b597a-143">بنود الأرشيف</span><span class="sxs-lookup"><span data-stu-id="b597a-143">Archive lines</span></span>  
23. <span data-ttu-id="b597a-144">في الحقل "نوع الصنف"، حدد "قائمة سجلات".</span><span class="sxs-lookup"><span data-stu-id="b597a-144">In the Item type field, select 'Record list'.</span></span>
24. <span data-ttu-id="b597a-145">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="b597a-145">Click Add.</span></span>
    * <span data-ttu-id="b597a-146">قم بإضافة هذا العنصر لكي يمثل قائمة حركات نظام جمع المعلومات التجارية التي تم الإبلاغ عنها أثناء عملية إعداد التقارير الحالية.</span><span class="sxs-lookup"><span data-stu-id="b597a-146">Add this item to represent the list of Intrastat transactions that are reported during the current reporting process.</span></span>  
25. <span data-ttu-id="b597a-147">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="b597a-147">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="b597a-148">في الحقل "الاسم"، اكتب "المبلغ".</span><span class="sxs-lookup"><span data-stu-id="b597a-148">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="b597a-149">المبلغ</span><span class="sxs-lookup"><span data-stu-id="b597a-149">Amount</span></span>  
27. <span data-ttu-id="b597a-150">في الحقل "نوع الصنف"، حدد "حقيقي".</span><span class="sxs-lookup"><span data-stu-id="b597a-150">In the Item type field, select 'Real'.</span></span>
28. <span data-ttu-id="b597a-151">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="b597a-151">Click Add.</span></span>
29. <span data-ttu-id="b597a-152">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="b597a-152">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="b597a-153">في حقل "الاسم"، اكتب "معرف سجل السلع".</span><span class="sxs-lookup"><span data-stu-id="b597a-153">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="b597a-154">معرف سجل السلع</span><span class="sxs-lookup"><span data-stu-id="b597a-154">Commodity rec id</span></span>  
31. <span data-ttu-id="b597a-155">في الحقل "نوع الصنف"، حدد "Int64".</span><span class="sxs-lookup"><span data-stu-id="b597a-155">In the Item type field, select 'Int64'.</span></span>
32. <span data-ttu-id="b597a-156">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="b597a-156">Click Add.</span></span>
33. <span data-ttu-id="b597a-157">انقر فوق "جديد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="b597a-157">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="b597a-158">في حقل "الاسم"، اكتب "رقم الصنف".</span><span class="sxs-lookup"><span data-stu-id="b597a-158">In the Name field, type 'Item number'.</span></span>
    * <span data-ttu-id="b597a-159">رقم العنصر</span><span class="sxs-lookup"><span data-stu-id="b597a-159">Item number</span></span>  
35. <span data-ttu-id="b597a-160">في الحقل "نوع الصنف"، حدد "سلسلة".</span><span class="sxs-lookup"><span data-stu-id="b597a-160">In the Item type field, select 'String'.</span></span>
36. <span data-ttu-id="b597a-161">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="b597a-161">Click Add.</span></span>
37. <span data-ttu-id="b597a-162">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="b597a-162">Click Save.</span></span>
38. <span data-ttu-id="b597a-163">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b597a-163">Close the page.</span></span>

## <a name="modify-model-mapping"></a><span data-ttu-id="b597a-164">تعديل تعيين النموذج</span><span class="sxs-lookup"><span data-stu-id="b597a-164">Modify model mapping</span></span>
1. <span data-ttu-id="b597a-165">في الشجرة، قم بتوسيع "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (نموذج)".</span><span class="sxs-lookup"><span data-stu-id="b597a-165">In the tree, expand 'Intrastat (model)'.</span></span>
2. <span data-ttu-id="b597a-166">في الشجرة، حدد "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (نموذج)\نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (تعيين)".</span><span class="sxs-lookup"><span data-stu-id="b597a-166">In the tree, select 'Intrastat (model)\Intrastat (mapping)'.</span></span>
    * <span data-ttu-id="b597a-167">قم بتعديل تعيين النموذج الموجود لبدء استخدامه لتحديث بيانات التطبيق ولأرشفة تفاصيل إعداد تقارير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="b597a-167">Modify the existing model mapping to start using it for  the application data update and to archive Intrastat reporting details.</span></span>  
3. <span data-ttu-id="b597a-168">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="b597a-168">Click Designer.</span></span>
4. <span data-ttu-id="b597a-169">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="b597a-169">Click New.</span></span>
5. <span data-ttu-id="b597a-170">في حقل "الاسم"، اكتب "تحديث الأرشيف".</span><span class="sxs-lookup"><span data-stu-id="b597a-170">In the Name field, type 'Update archive'.</span></span>
    * <span data-ttu-id="b597a-171">تحديث الأرشيف</span><span class="sxs-lookup"><span data-stu-id="b597a-171">Update archive</span></span>  
6. <span data-ttu-id="b597a-172">في الحقل "اتجاه"، حدد "إلى الوجهة".</span><span class="sxs-lookup"><span data-stu-id="b597a-172">In the Direction field, select 'To destination'.</span></span>
7. <span data-ttu-id="b597a-173">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="b597a-173">Click Save.</span></span>
    * <span data-ttu-id="b597a-174">يحدد هذا التعيين الجديد تدفق البيانات لنقل البيانات (تفاصيل إعداد تقارير نظام جمع المعلومات التجارية) من نموذج البيانات إلى جداول التطبيق (وجهة التحديث).</span><span class="sxs-lookup"><span data-stu-id="b597a-174">This new mapping specifies the data flow for moving data (Intrastat reporting details) from the data model to the application tables (the update destination).</span></span> <span data-ttu-id="b597a-175">لاحظ أنه يجب استخدام عناصر جذر مختلفة خاصة بالنموذج للحصول على البيانات من التطبيق لعملية إعداد التقارير، وبعد ذلك استخدام البيانات من نموذج البيانات لتحديث بيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="b597a-175">Note that different model's root items must be used to get data from the application for the reporting process and then use the data from data model for the application data update.</span></span>   
8. <span data-ttu-id="b597a-176">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="b597a-176">Click Designer.</span></span>
9. <span data-ttu-id="b597a-177">في الشجرة، حدد "نموذج البيانات\نموذج البيانات".</span><span class="sxs-lookup"><span data-stu-id="b597a-177">In the tree, select 'Data model\Data model'.</span></span>
    * <span data-ttu-id="b597a-178">أضف مصدر البيانات مطلوب.</span><span class="sxs-lookup"><span data-stu-id="b597a-178">Add the required data source.</span></span> <span data-ttu-id="b597a-179">هذا هو نموذج البيانات الذي يحتوي على التفاصيل الخاصة بحركات نظام جمع المعلومات التجارية التي تم الإبلاغ عنها والتي يجب أرشفتها.</span><span class="sxs-lookup"><span data-stu-id="b597a-179">This is the data model that contains details of the reported Intrastat transactions that must be archived.</span></span>  
10. <span data-ttu-id="b597a-180">انقر فوق "إضافة جذر".</span><span class="sxs-lookup"><span data-stu-id="b597a-180">Click Add root.</span></span>
11. <span data-ttu-id="b597a-181">في حقل "الاسم"، اكتب "نموذج".</span><span class="sxs-lookup"><span data-stu-id="b597a-181">In the Name field, type 'model'.</span></span>
    * <span data-ttu-id="b597a-182">النموذج</span><span class="sxs-lookup"><span data-stu-id="b597a-182">model</span></span>  
12. <span data-ttu-id="b597a-183">في حقل "التعريف"، أدخل قيمة "لتحديث بيانات التطبيق" أو حددها.</span><span class="sxs-lookup"><span data-stu-id="b597a-183">In the Definition field, enter or select the value 'For application data update'.</span></span>
    * <span data-ttu-id="b597a-184">لتحديث بيانات التطبيق</span><span class="sxs-lookup"><span data-stu-id="b597a-184">For application data update</span></span>  
13. <span data-ttu-id="b597a-185">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="b597a-185">Click OK.</span></span>
14. <span data-ttu-id="b597a-186">في الشجرة ، قم بتوسيع "النموذج"</span><span class="sxs-lookup"><span data-stu-id="b597a-186">In the tree, expand 'model'.</span></span>
15. <span data-ttu-id="b597a-187">في الشجرة، حدد "الدوال/المحسوب".</span><span class="sxs-lookup"><span data-stu-id="b597a-187">In the tree, select 'Functions\Calculated field'.</span></span>
16. <span data-ttu-id="b597a-188">في الشجرة، حدد "النموذج\رأس الأرشيف".</span><span class="sxs-lookup"><span data-stu-id="b597a-188">In the tree, select 'model\Archive header'.</span></span>
17. <span data-ttu-id="b597a-189">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="b597a-189">Click Add.</span></span>
    * <span data-ttu-id="b597a-190">لأنك ترغب في تعداد حركات نظام جمع المعلومات التجارية التي تم الإبلاغ عنها لأرشفتها، يجب إضافة مصدر البيانات الملائم.</span><span class="sxs-lookup"><span data-stu-id="b597a-190">Because you want to enumerate reported Intrastat transactions for archiving, the appropriate data source must be added.</span></span>  
18. <span data-ttu-id="b597a-191">في حقل "الاسم"، اكتب "البنود التي تم تعدادها‬".</span><span class="sxs-lookup"><span data-stu-id="b597a-191">In the Name field, type 'Enumerated lines'.</span></span>
    * <span data-ttu-id="b597a-192">البنود التي تم تعدادها</span><span class="sxs-lookup"><span data-stu-id="b597a-192">Enumerated lines</span></span>  
19. <span data-ttu-id="b597a-193">انقر فوق "تحرير المعادلة".</span><span class="sxs-lookup"><span data-stu-id="b597a-193">Click Edit formula.</span></span>
20. <span data-ttu-id="b597a-194">في الشجرة، حدد "قائمة\ENUMERATE".</span><span class="sxs-lookup"><span data-stu-id="b597a-194">In the tree, select 'List\ENUMERATE'.</span></span>
21. <span data-ttu-id="b597a-195">انقر فوق "إضافة دالة".</span><span class="sxs-lookup"><span data-stu-id="b597a-195">Click Add function.</span></span>
22. <span data-ttu-id="b597a-196">في الشجرة ، قم بتوسيع "النموذج"</span><span class="sxs-lookup"><span data-stu-id="b597a-196">In the tree, expand 'model'.</span></span>
23. <span data-ttu-id="b597a-197">في الشجرة، قم بتوسيع "النموذج\رأس الأرشيف".</span><span class="sxs-lookup"><span data-stu-id="b597a-197">In the tree, expand 'model\Archive header'.</span></span>
24. <span data-ttu-id="b597a-198">في الشجرة، حدد "النموذج\رأس الأرشيف\بنود الأرشيف".</span><span class="sxs-lookup"><span data-stu-id="b597a-198">In the tree, select 'model\Archive header\Archive lines'.</span></span>
25. <span data-ttu-id="b597a-199">انقر فوق "إضافة مصدر بيانات".</span><span class="sxs-lookup"><span data-stu-id="b597a-199">Click Add data source.</span></span>
26. <span data-ttu-id="b597a-200">في حقل المعادلة، أدخل "ENUMERATE(model.'Archive header'.'Archive lines')".</span><span class="sxs-lookup"><span data-stu-id="b597a-200">In the Formula field, enter 'ENUMERATE(model.'Archive header'.'Archive lines')'.</span></span>
    * <span data-ttu-id="b597a-201">ENUMERATE(النموذج.'رأس الأرشيف'.'بنود الأرشيف')</span><span class="sxs-lookup"><span data-stu-id="b597a-201">ENUMERATE(model.'Archive header'.'Archive lines')</span></span>  
27. <span data-ttu-id="b597a-202">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="b597a-202">Click Save.</span></span>
28. <span data-ttu-id="b597a-203">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b597a-203">Close the page.</span></span>
29. <span data-ttu-id="b597a-204">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="b597a-204">Click OK.</span></span>
30. <span data-ttu-id="b597a-205">انقر فوق "إضافة وجهة".</span><span class="sxs-lookup"><span data-stu-id="b597a-205">Click Add destination.</span></span>
    * <span data-ttu-id="b597a-206">قم بإضافة جداول التطبيق كوجهات مطلوبة تتطلب تحديثات لأرشفة التفاصيل الخاصة بحركات نظام جمع المعلومات التجارية التي تم الإبلاغ عنها.</span><span class="sxs-lookup"><span data-stu-id="b597a-206">Add application tables as required destinations that require updates to archive details of reported Intrastat transactions.</span></span>  
31. <span data-ttu-id="b597a-207">في حقل "الاسم"، اكتب "أرشيف".</span><span class="sxs-lookup"><span data-stu-id="b597a-207">In the Name field, type 'Archive'.</span></span>
    * <span data-ttu-id="b597a-208">الأرشيف</span><span class="sxs-lookup"><span data-stu-id="b597a-208">Archive</span></span>  
32. <span data-ttu-id="b597a-209">في حقل "اسم الجدول"، اكتب "IntrastatArchiveGeneral".</span><span class="sxs-lookup"><span data-stu-id="b597a-209">In the Table name field, type 'IntrastatArchiveGeneral'.</span></span>
    * <span data-ttu-id="b597a-210">IntrastatArchiveGeneral</span><span class="sxs-lookup"><span data-stu-id="b597a-210">IntrastatArchiveGeneral</span></span>  
    * <span data-ttu-id="b597a-211">احتفظ بسجل الإجراء "إدراج" لكي تتمكن من إضافة السجلات أثناء عملية أرشفة التفاصيل الخاصة بكل عمليات إعداد تقارير نظام جمع المعلومات التجارية.</span><span class="sxs-lookup"><span data-stu-id="b597a-211">Keep the record action 'Insert' so you can add records during the detail archiving of each Intrastat reporting process.</span></span>  
33. <span data-ttu-id="b597a-212">حدد "نعم" في حقل "سجل معلومات السجل‬".</span><span class="sxs-lookup"><span data-stu-id="b597a-212">Select Yes in the Record infolog field.</span></span>
    * <span data-ttu-id="b597a-213">حدد "نعم" للحصول على معلومات حول مشكلات تحديث بيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="b597a-213">Select Yes to get information about issues with the application data update.</span></span>  
34. <span data-ttu-id="b597a-214">حدد "نعم" في الحقل "تخطي التحقق من صحة إجراء السجل‬".</span><span class="sxs-lookup"><span data-stu-id="b597a-214">Select Yes in the Skip record action validation field.</span></span>
    * <span data-ttu-id="b597a-215">حدد "نعم" لمنع أخطاء التحقق من الصحة حول الحقل الفارغ "معرف أرشيف نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬".</span><span class="sxs-lookup"><span data-stu-id="b597a-215">Select Yes to suppress validation errors about the empty 'Intrastat archive ID' field.</span></span> <span data-ttu-id="b597a-216">سيتم إجراء ذلك بعد إضافة السجلات، استنادًا إلى إعدادات الأرقام التسلسلية التي تم تكوينها لهذا الجدول في نموذج "محددات التجارة الخارجية".</span><span class="sxs-lookup"><span data-stu-id="b597a-216">This will be done after records are added, based on the sequence number settings that are configured for this table in the Foreign trade parameters form.</span></span>  
35. <span data-ttu-id="b597a-217">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="b597a-217">Click OK.</span></span>
    * <span data-ttu-id="b597a-218">اعمل على ربط عناصر مصدر البيانات المضاف (النموذج المصفى استنادًا إلى العنصر الجذر المحدد) مع عناصر من الوجهة المضافة.</span><span class="sxs-lookup"><span data-stu-id="b597a-218">Bind elements of the added data source (the filtered model based on the selected root item) with elements from the added destination.</span></span>  
36. <span data-ttu-id="b597a-219">في الشجرة، قم بتوسيع ''أرشيف".</span><span class="sxs-lookup"><span data-stu-id="b597a-219">In the tree, expand 'Archive'.</span></span>
37. <span data-ttu-id="b597a-220">في الشجرة، قم بتوسيع "أرشيف‏‎\<علاقات".</span><span class="sxs-lookup"><span data-stu-id="b597a-220">In the tree, expand 'Archive\<Relations'.</span></span>
38. <span data-ttu-id="b597a-221">في الشجرة، قم بتوسيع "أرشيف\<علاقات\IntrastatArchiveDetail".</span><span class="sxs-lookup"><span data-stu-id="b597a-221">In the tree, expand 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
39. <span data-ttu-id="b597a-222">في الشجرة، حدد "أرشيف\<علاقات\IntrastatArchiveDetail\مبلغ(AmountMST)".</span><span class="sxs-lookup"><span data-stu-id="b597a-222">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)'.</span></span>
40. <span data-ttu-id="b597a-223">في الشجرة، قم بتوسيع "النموذج\رأس الأرشيف\البنود التي تم تعدادها‬".</span><span class="sxs-lookup"><span data-stu-id="b597a-223">In the tree, expand 'model\Archive header\Enumerated lines'.</span></span>
41. <span data-ttu-id="b597a-224">في الشجرة، قم بتوسيع "النموذج\رأس الأرشيف\البنود التي تم تعدادها‬\القيمة".</span><span class="sxs-lookup"><span data-stu-id="b597a-224">In the tree, expand 'model\Archive header\Enumerated lines\Value'.</span></span>
42. <span data-ttu-id="b597a-225">في الشجرة، حدد "النموذج\رأس الأرشيف\البنود التي تم تعدادها\القيمة\المبلغ".</span><span class="sxs-lookup"><span data-stu-id="b597a-225">In the tree, select 'model\Archive header\Enumerated lines\Value\Amount'.</span></span>
43. <span data-ttu-id="b597a-226">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="b597a-226">Click Bind.</span></span>
44. <span data-ttu-id="b597a-227">في الشجرة، حدد "أرشيف\<علاقات\IntrastatArchiveDetail\السلع(IntrastatCommodity)'.</span><span class="sxs-lookup"><span data-stu-id="b597a-227">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)'.</span></span>
45. <span data-ttu-id="b597a-228">في الشجرة، حدد "النموذج\رأس الأرشيف\البنود التي تم تعدادها\القيمة\معرف سجل السلع".</span><span class="sxs-lookup"><span data-stu-id="b597a-228">In the tree, select 'model\Archive header\Enumerated lines\Value\Commodity rec id'.</span></span>
46. <span data-ttu-id="b597a-229">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="b597a-229">Click Bind.</span></span>
47. <span data-ttu-id="b597a-230">في الشجرة، حدد "أرشيف\<علاقات\IntrastatArchiveDetail\رقم الصنف(ItemId)".</span><span class="sxs-lookup"><span data-stu-id="b597a-230">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)'.</span></span>
48. <span data-ttu-id="b597a-231">في الشجرة، حدد "النموذج\رأس الأرشيف\البنود التي تم تعدادها\القيمة\رقم الصنف".</span><span class="sxs-lookup"><span data-stu-id="b597a-231">In the tree, select 'model\Archive header\Enumerated lines\Value\Item number'.</span></span>
49. <span data-ttu-id="b597a-232">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="b597a-232">Click Bind.</span></span>
50. <span data-ttu-id="b597a-233">في الشجرة، حدد "أرشيف\<علاقات\IntrastatArchiveDetail\رقم البند(LineNumber)".</span><span class="sxs-lookup"><span data-stu-id="b597a-233">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)'.</span></span>
51. <span data-ttu-id="b597a-234">في الشجرة، حدد "النموذج\رأس الأرشيف\البنود التي تم تعدادها\الرقم".</span><span class="sxs-lookup"><span data-stu-id="b597a-234">In the tree, select 'model\Archive header\Enumerated lines\Number'.</span></span>
52. <span data-ttu-id="b597a-235">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="b597a-235">Click Bind.</span></span>
53. <span data-ttu-id="b597a-236">في الشجرة، حدد "أرشيف\<علاقات\IntrastatArchiveDetail".</span><span class="sxs-lookup"><span data-stu-id="b597a-236">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
54. <span data-ttu-id="b597a-237">في الشجرة، حدد "النموذج\رأس الأرشيف\البنود التي تم تعدادها‬".</span><span class="sxs-lookup"><span data-stu-id="b597a-237">In the tree, select 'model\Archive header\Enumerated lines'.</span></span>
55. <span data-ttu-id="b597a-238">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="b597a-238">Click Bind.</span></span>
56. <span data-ttu-id="b597a-239">في الشجرة، حدد "أرشيف\اسم الملف(FileName)".</span><span class="sxs-lookup"><span data-stu-id="b597a-239">In the tree, select 'Archive\File name(FileName)'.</span></span>
57. <span data-ttu-id="b597a-240">في الشجرة، حدد "نموذج\رأس الأرشيف\اسم الملف".</span><span class="sxs-lookup"><span data-stu-id="b597a-240">In the tree, select 'model\Archive header\File name'.</span></span>
58. <span data-ttu-id="b597a-241">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="b597a-241">Click Bind.</span></span>
59. <span data-ttu-id="b597a-242">في الشجرة، حدد "أرشيف\عدد الأسطر(NumberOfLines)".</span><span class="sxs-lookup"><span data-stu-id="b597a-242">In the tree, select 'Archive\Number of lines(NumberOfLines)'.</span></span>
60. <span data-ttu-id="b597a-243">في الشجرة، حدد "النموذج\رأس الأرشيف\عدد الأسطر‬".</span><span class="sxs-lookup"><span data-stu-id="b597a-243">In the tree, select 'model\Archive header\Number of lines'.</span></span>
61. <span data-ttu-id="b597a-244">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="b597a-244">Click Bind.</span></span>
62. <span data-ttu-id="b597a-245">في الشجرة، حدد "أرشيف".</span><span class="sxs-lookup"><span data-stu-id="b597a-245">In the tree, select 'Archive'.</span></span>
63. <span data-ttu-id="b597a-246">في الشجرة، حدد "النموذج\رأس الأرشيف".</span><span class="sxs-lookup"><span data-stu-id="b597a-246">In the tree, select 'model\Archive header'.</span></span>
64. <span data-ttu-id="b597a-247">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="b597a-247">Click Bind.</span></span>
65. <span data-ttu-id="b597a-248">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="b597a-248">Click Save.</span></span>
66. <span data-ttu-id="b597a-249">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b597a-249">Close the page.</span></span>
67. <span data-ttu-id="b597a-250">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b597a-250">Close the page.</span></span>
