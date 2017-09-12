--- 
title: "إنشاء تكوين تنسيق للتقارير الإلكترونية (ER)"
description: "تشرح الخطوات التالية كيف يمكن لمستخدم بدور مسؤول النظام أو مطور التقارير الإلكترونية إنشاء تكوين تنسيق لإنشاء التقارير الإلكترونية."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
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
ms.openlocfilehash: 04817d1f1851e43679995641e8b0ff99edaa83ad
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-format-configuration-for-electronic-reporting-er"></a><span data-ttu-id="d92c4-103">إنشاء تكوين تنسيق للتقارير الإلكترونية (ER)</span><span class="sxs-lookup"><span data-stu-id="d92c4-103">Create a format configuration for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d92c4-104">تشرح الخطوات التالية كيف يمكن لمستخدم بدور مسؤول النظام أو مطور التقارير الإلكترونية إنشاء تكوين تنسيق لإنشاء التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="d92c4-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="d92c4-105">وسيحدد هذا التكوين تنسيق المستندات الإلكترونية المستخدمة لمعالجة المدفوعات.</span><span class="sxs-lookup"><span data-stu-id="d92c4-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="d92c4-106">في هذا المثال، ستقوم بإنشاء تكوين تنسيق لشركة عينة، .Litware, Inc. ولإكمال هذه الخطوات، يجب عليك أولاً إكمال الخطوات المذكورة في الإجراء "تعيين النموذج لمصادر البيانات المحددة".</span><span class="sxs-lookup"><span data-stu-id="d92c4-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="d92c4-107">قم بإنشاء تكوين تنسيق جديد</span><span class="sxs-lookup"><span data-stu-id="d92c4-107">Create a new format configuration</span></span>
1. <span data-ttu-id="d92c4-108">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="d92c4-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="d92c4-109">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="d92c4-109">Click Reporting configurations.</span></span>
3. <span data-ttu-id="d92c4-110">في الشجرة، حدد "المدفوعات (نموذج مبسط)".</span><span class="sxs-lookup"><span data-stu-id="d92c4-110">In the tree, select 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="d92c4-111">انقر فوق "إنشاء تكوين" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="d92c4-111">Click Create configuration to open the drop dialog.</span></span>
5. <span data-ttu-id="d92c4-112">في الحقل "جديد"، أدخل 'التنسيق استناداً إلى نموذج الدفع الخاص بنموذج البيانات".</span><span class="sxs-lookup"><span data-stu-id="d92c4-112">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
6. <span data-ttu-id="d92c4-113">في الحقل "الاسم"، اكتب BACS (وهمية من المملكة المتحدة).</span><span class="sxs-lookup"><span data-stu-id="d92c4-113">In the Name field, type 'BACS (UK fictitious)'.</span></span>
    * <span data-ttu-id="d92c4-114">BACS (وهمية من المملكة المتحدة)</span><span class="sxs-lookup"><span data-stu-id="d92c4-114">BACS (UK fictitious)</span></span>  
7. <span data-ttu-id="d92c4-115">في حقل "الوصف"، اكتب "تنسيق دفع المورد BACS (وهمية من المملكة المتحدة)".</span><span class="sxs-lookup"><span data-stu-id="d92c4-115">In the Description field, type 'BACS vendor payment format (UK fictitious)'.</span></span>
    * <span data-ttu-id="d92c4-116">تنسيق دفع مورد BACS (وهمية من المملكة المتحدة)</span><span class="sxs-lookup"><span data-stu-id="d92c4-116">BACS vendor payment format (UK fictitious)</span></span>  
    * <span data-ttu-id="d92c4-117">يتم تلقائيًا إدخال موفر التكوين النشط هنا.</span><span class="sxs-lookup"><span data-stu-id="d92c4-117">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="d92c4-118">سيكون هذا الموفر قادرًا على المحافظة على هذا التكوين.</span><span class="sxs-lookup"><span data-stu-id="d92c4-118">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="d92c4-119">باستطاعة موفرين آخرين استخدام هذا التكوين، ولكن لن يكون باستطاعتهم المحافظة عليه.</span><span class="sxs-lookup"><span data-stu-id="d92c4-119">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="d92c4-120">يمكن تعريف تنسيق معين لوثيقة إلكترونية.</span><span class="sxs-lookup"><span data-stu-id="d92c4-120">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="d92c4-121">اترك هذا الحقل فارغاً إذا كنت تريد تحديد تنسيق في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="d92c4-121">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="d92c4-122">في الحقل "تعريف نموذج البيانات"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="d92c4-122">In the Data model definition field, enter or select a value.</span></span>
9. <span data-ttu-id="d92c4-123">وانقر فوق إنشاء تكوين.</span><span class="sxs-lookup"><span data-stu-id="d92c4-123">Click Create configuration.</span></span>
    * <span data-ttu-id="d92c4-124">تم إنشاء تكوين جديد.</span><span class="sxs-lookup"><span data-stu-id="d92c4-124">A new configuration has been created.</span></span> <span data-ttu-id="d92c4-125">يمكن استخدام الإصدار التمهيدي لتخزين تنسيق التصميم لإدارة الوثائق الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="d92c4-125">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-format-of-electronic-document"></a><span data-ttu-id="d92c4-126">تصميم تنسيق المستند الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="d92c4-126">Design format of electronic document</span></span>
1. <span data-ttu-id="d92c4-127">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="d92c4-127">Click Designer.</span></span>
2. <span data-ttu-id="d92c4-128">انقر فوق "إضافة جذر" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="d92c4-128">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="d92c4-129">في الشجرة، حدد "Common\File".</span><span class="sxs-lookup"><span data-stu-id="d92c4-129">In the tree, select 'Common\File'.</span></span>
4. <span data-ttu-id="d92c4-130">في الحقل "الاسم"، اكتب "Xml".</span><span class="sxs-lookup"><span data-stu-id="d92c4-130">In the Name field, type 'Xml'.</span></span>
    * <span data-ttu-id="d92c4-131">Xml</span><span class="sxs-lookup"><span data-stu-id="d92c4-131">Xml</span></span>  
5. <span data-ttu-id="d92c4-132">في الحقل"الترميز"، اكتب "UTF-8".</span><span class="sxs-lookup"><span data-stu-id="d92c4-132">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="d92c4-133">UTF-8</span><span class="sxs-lookup"><span data-stu-id="d92c4-133">UTF-8</span></span>  
6. <span data-ttu-id="d92c4-134">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d92c4-134">Click OK.</span></span>
7. <span data-ttu-id="d92c4-135">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="d92c4-135">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="d92c4-136">في الشجرة، حدد XML/العنصر".</span><span class="sxs-lookup"><span data-stu-id="d92c4-136">In the tree, select 'XML\Element'.</span></span>
9. <span data-ttu-id="d92c4-137">في الحقل "الاسم"، اكتب "رسالة".</span><span class="sxs-lookup"><span data-stu-id="d92c4-137">In the Name field, type 'Message'.</span></span>
    * <span data-ttu-id="d92c4-138">الرسالة</span><span class="sxs-lookup"><span data-stu-id="d92c4-138">Message</span></span>  
10. <span data-ttu-id="d92c4-139">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d92c4-139">Click OK.</span></span>
11. <span data-ttu-id="d92c4-140">في الشجرة، حدد "Xml\الرسالة".</span><span class="sxs-lookup"><span data-stu-id="d92c4-140">In the tree, select 'Xml\Message'.</span></span>
12. <span data-ttu-id="d92c4-141">انقر فوق "إضافة عنصر".</span><span class="sxs-lookup"><span data-stu-id="d92c4-141">Click Add Element.</span></span>
13. <span data-ttu-id="d92c4-142">في الحقل "الاسم"، اكتب "تاريخ المعالجة".</span><span class="sxs-lookup"><span data-stu-id="d92c4-142">In the Name field, type 'ProcessingDate'.</span></span>
    * <span data-ttu-id="d92c4-143">ProcessingDate</span><span class="sxs-lookup"><span data-stu-id="d92c4-143">ProcessingDate</span></span>  
14. <span data-ttu-id="d92c4-144">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d92c4-144">Click OK.</span></span>
15. <span data-ttu-id="d92c4-145">انقر فوق "إضافة عنصر".</span><span class="sxs-lookup"><span data-stu-id="d92c4-145">Click Add Element.</span></span>
16. <span data-ttu-id="d92c4-146">في الحقل "الاسم"، اكتب "رسالة".</span><span class="sxs-lookup"><span data-stu-id="d92c4-146">In the Name field, type 'MessageId'.</span></span>
    * <span data-ttu-id="d92c4-147">MessageId</span><span class="sxs-lookup"><span data-stu-id="d92c4-147">MessageId</span></span>  
17. <span data-ttu-id="d92c4-148">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d92c4-148">Click OK.</span></span>
18. <span data-ttu-id="d92c4-149">انقر فوق "إضافة عنصر".</span><span class="sxs-lookup"><span data-stu-id="d92c4-149">Click Add Element.</span></span>
19. <span data-ttu-id="d92c4-150">في الحقل "الاسم، اكتب "دفعات".‬</span><span class="sxs-lookup"><span data-stu-id="d92c4-150">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="d92c4-151">المدفوعات</span><span class="sxs-lookup"><span data-stu-id="d92c4-151">Payments</span></span>  
20. <span data-ttu-id="d92c4-152">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d92c4-152">Click OK.</span></span>
21. <span data-ttu-id="d92c4-153">في الشجرة، حدد "Xml\الرسالة\المدفوعات".</span><span class="sxs-lookup"><span data-stu-id="d92c4-153">In the tree, select 'Xml\Message\Payments'.</span></span>
22. <span data-ttu-id="d92c4-154">انقر فوق "إضافة عنصر".</span><span class="sxs-lookup"><span data-stu-id="d92c4-154">Click Add Element.</span></span>
23. <span data-ttu-id="d92c4-155">في الحقل "الاسم" اكتب "الصنف".</span><span class="sxs-lookup"><span data-stu-id="d92c4-155">In the Name field, type 'Item'.</span></span>
    * <span data-ttu-id="d92c4-156">الصنف</span><span class="sxs-lookup"><span data-stu-id="d92c4-156">Item</span></span>  
24. <span data-ttu-id="d92c4-157">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d92c4-157">Click OK.</span></span>
25. <span data-ttu-id="d92c4-158">في الشجرة، حدد "Xml\الرسالة\المدفوعات\الصنف".</span><span class="sxs-lookup"><span data-stu-id="d92c4-158">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
26. <span data-ttu-id="d92c4-159">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="d92c4-159">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="d92c4-160">في الشجرة، حدد "XML\سمة".</span><span class="sxs-lookup"><span data-stu-id="d92c4-160">In the tree, select 'XML\Attribute'.</span></span>
28. <span data-ttu-id="d92c4-161">في الحقل "الاسم"، اكتب "المعرف".</span><span class="sxs-lookup"><span data-stu-id="d92c4-161">In the Name field, type 'Id'.</span></span>
    * <span data-ttu-id="d92c4-162">معرف</span><span class="sxs-lookup"><span data-stu-id="d92c4-162">Id</span></span>  
29. <span data-ttu-id="d92c4-163">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d92c4-163">Click OK.</span></span>
30. <span data-ttu-id="d92c4-164">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="d92c4-164">Click Add to open the drop dialog.</span></span>
31. <span data-ttu-id="d92c4-165">في الشجرة، حدد XML/العنصر".</span><span class="sxs-lookup"><span data-stu-id="d92c4-165">In the tree, select 'XML\Element'.</span></span>
32. <span data-ttu-id="d92c4-166">في الحقل "الاسم"، اكتب "المورد".</span><span class="sxs-lookup"><span data-stu-id="d92c4-166">In the Name field, type 'Vendor'.</span></span>
    * <span data-ttu-id="d92c4-167">المورِد</span><span class="sxs-lookup"><span data-stu-id="d92c4-167">Vendor</span></span>  
33. <span data-ttu-id="d92c4-168">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d92c4-168">Click OK.</span></span>
34. <span data-ttu-id="d92c4-169">في الشجرة، حدد "Xml\الرسالة\المدفوعات\الصنف\المورّد".</span><span class="sxs-lookup"><span data-stu-id="d92c4-169">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
35. <span data-ttu-id="d92c4-170">انقر فوق "إضافة عنصر".</span><span class="sxs-lookup"><span data-stu-id="d92c4-170">Click Add Element.</span></span>
36. <span data-ttu-id="d92c4-171">في الحقل "الاسم"، اكتب "الاسم".</span><span class="sxs-lookup"><span data-stu-id="d92c4-171">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="d92c4-172">الاسم</span><span class="sxs-lookup"><span data-stu-id="d92c4-172">Name</span></span>  
37. <span data-ttu-id="d92c4-173">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d92c4-173">Click OK.</span></span>
38. <span data-ttu-id="d92c4-174">انقر فوق "إضافة عنصر".</span><span class="sxs-lookup"><span data-stu-id="d92c4-174">Click Add Element.</span></span>
39. <span data-ttu-id="d92c4-175">في الحقل "الاسم"، اكتب "البنك".</span><span class="sxs-lookup"><span data-stu-id="d92c4-175">In the Name field, type 'Bank'.</span></span>
    * <span data-ttu-id="d92c4-176">البنك</span><span class="sxs-lookup"><span data-stu-id="d92c4-176">Bank</span></span>  
40. <span data-ttu-id="d92c4-177">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d92c4-177">Click OK.</span></span>
41. <span data-ttu-id="d92c4-178">في الشجرة، حدد "Xml\الرسالة\المدفوعات\الصنف\المورّد\البنك".</span><span class="sxs-lookup"><span data-stu-id="d92c4-178">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
42. <span data-ttu-id="d92c4-179">انقر فوق "إضافة عنصر".</span><span class="sxs-lookup"><span data-stu-id="d92c4-179">Click Add Element.</span></span>
43. <span data-ttu-id="d92c4-180">في الحقل "الاسم"، اكتب "RoutingNumber".</span><span class="sxs-lookup"><span data-stu-id="d92c4-180">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="d92c4-181">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="d92c4-181">RoutingNumber</span></span>  
44. <span data-ttu-id="d92c4-182">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d92c4-182">Click OK.</span></span>
45. <span data-ttu-id="d92c4-183">انقر فوق "إضافة عنصر".</span><span class="sxs-lookup"><span data-stu-id="d92c4-183">Click Add Element.</span></span>
46. <span data-ttu-id="d92c4-184">في الحقل "الاسم"، اكتب "AccountNumber".</span><span class="sxs-lookup"><span data-stu-id="d92c4-184">In the Name field, type 'AccountNumber'.</span></span>
    * <span data-ttu-id="d92c4-185">AccountNumber</span><span class="sxs-lookup"><span data-stu-id="d92c4-185">AccountNumber</span></span>  
47. <span data-ttu-id="d92c4-186">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d92c4-186">Click OK.</span></span>
48. <span data-ttu-id="d92c4-187">في الشجرة، حدد "Xml\الرسالة\المدفوعات\الصنف\المورّد".</span><span class="sxs-lookup"><span data-stu-id="d92c4-187">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
49. <span data-ttu-id="d92c4-188">انقر فوق نسخ.</span><span class="sxs-lookup"><span data-stu-id="d92c4-188">Click Copy.</span></span>
50. <span data-ttu-id="d92c4-189">في الشجرة، حدد "Xml\الرسالة\المدفوعات\الصنف".</span><span class="sxs-lookup"><span data-stu-id="d92c4-189">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="d92c4-190">انقر فوق "لصق".</span><span class="sxs-lookup"><span data-stu-id="d92c4-190">Click Paste.</span></span>
52. <span data-ttu-id="d92c4-191">في الحقل "الاسم"، اكتب "الممول".</span><span class="sxs-lookup"><span data-stu-id="d92c4-191">In the Name field, type 'Payer'.</span></span>
    * <span data-ttu-id="d92c4-192">الممول</span><span class="sxs-lookup"><span data-stu-id="d92c4-192">Payer</span></span>  
53. <span data-ttu-id="d92c4-193">في الشجرة، حدد "Xml\الرسالة\المدفوعات\الصنف".</span><span class="sxs-lookup"><span data-stu-id="d92c4-193">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
54. <span data-ttu-id="d92c4-194">انقر فوق "إضافة عنصر".</span><span class="sxs-lookup"><span data-stu-id="d92c4-194">Click Add Element.</span></span>
55. <span data-ttu-id="d92c4-195">في الحقل "الاسم"، اكتب "العملة".</span><span class="sxs-lookup"><span data-stu-id="d92c4-195">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="d92c4-196">العملة</span><span class="sxs-lookup"><span data-stu-id="d92c4-196">Currency</span></span>  
56. <span data-ttu-id="d92c4-197">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d92c4-197">Click OK.</span></span>
57. <span data-ttu-id="d92c4-198">انقر فوق "إضافة عنصر".</span><span class="sxs-lookup"><span data-stu-id="d92c4-198">Click Add Element.</span></span>
58. <span data-ttu-id="d92c4-199">في الحقل "الاسم"، اكتب "الوصف".</span><span class="sxs-lookup"><span data-stu-id="d92c4-199">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="d92c4-200">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="d92c4-200">Description</span></span>  
59. <span data-ttu-id="d92c4-201">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d92c4-201">Click OK.</span></span>
60. <span data-ttu-id="d92c4-202">انقر فوق "إضافة عنصر".</span><span class="sxs-lookup"><span data-stu-id="d92c4-202">Click Add Element.</span></span>
61. <span data-ttu-id="d92c4-203">في الحقل "الاسم"، اكتب "TransDate".</span><span class="sxs-lookup"><span data-stu-id="d92c4-203">In the Name field, type 'TransDate'.</span></span>
    * <span data-ttu-id="d92c4-204">TransDate</span><span class="sxs-lookup"><span data-stu-id="d92c4-204">TransDate</span></span>  
62. <span data-ttu-id="d92c4-205">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d92c4-205">Click OK.</span></span>
63. <span data-ttu-id="d92c4-206">انقر فوق "إضافة عنصر".</span><span class="sxs-lookup"><span data-stu-id="d92c4-206">Click Add Element.</span></span>
64. <span data-ttu-id="d92c4-207">في الحقل "الاسم"، اكتب "المبلغ".</span><span class="sxs-lookup"><span data-stu-id="d92c4-207">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="d92c4-208">المبلغ</span><span class="sxs-lookup"><span data-stu-id="d92c4-208">Amount</span></span>  
65. <span data-ttu-id="d92c4-209">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d92c4-209">Click OK.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="d92c4-210">إعداد مكونات التنسيق لتعيينها لعناصر نماذج البيانات</span><span class="sxs-lookup"><span data-stu-id="d92c4-210">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="d92c4-211">في الشجرة، حدد "Xml\الرسالة\ProcessingDate".</span><span class="sxs-lookup"><span data-stu-id="d92c4-211">In the tree, select 'Xml\Message\ProcessingDate'.</span></span>
2. <span data-ttu-id="d92c4-212">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="d92c4-212">Click Add to open the drop dialog.</span></span>
3. <span data-ttu-id="d92c4-213">في الشجرة، حدد "النص\DateTime".</span><span class="sxs-lookup"><span data-stu-id="d92c4-213">In the tree, select 'Text\DateTime'.</span></span>
4. <span data-ttu-id="d92c4-214">في الحقل "التنسيق"، اكتب "السنة-الشهر-اليوم".</span><span class="sxs-lookup"><span data-stu-id="d92c4-214">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="d92c4-215">yyyy-MM-dd</span><span class="sxs-lookup"><span data-stu-id="d92c4-215">yyyy-MM-dd</span></span>  
5. <span data-ttu-id="d92c4-216">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d92c4-216">Click OK.</span></span>
6. <span data-ttu-id="d92c4-217">في الشجرة، حدد "Xml\الرسالة\المدفوعات\الصنف\TransDate".</span><span class="sxs-lookup"><span data-stu-id="d92c4-217">In the tree, select 'Xml\Message\Payments\Item\TransDate'.</span></span>
7. <span data-ttu-id="d92c4-218">انقر فوق إضافة التاريخ والوقت.</span><span class="sxs-lookup"><span data-stu-id="d92c4-218">Click Add DateTime.</span></span>
8. <span data-ttu-id="d92c4-219">في الحقل "التنسيق"، اكتب "السنة-الشهر-اليوم".</span><span class="sxs-lookup"><span data-stu-id="d92c4-219">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="d92c4-220">yyyy-MM-dd</span><span class="sxs-lookup"><span data-stu-id="d92c4-220">yyyy-MM-dd</span></span>  
9. <span data-ttu-id="d92c4-221">في الحقل "نوع التاريخ/الوقت‬"، حدد "التاريخ".</span><span class="sxs-lookup"><span data-stu-id="d92c4-221">In the DateTime type field, select 'Date'.</span></span>
10. <span data-ttu-id="d92c4-222">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d92c4-222">Click OK.</span></span>
11. <span data-ttu-id="d92c4-223">في الشجرة، حدد "Xml\الرسالة\MessageId".</span><span class="sxs-lookup"><span data-stu-id="d92c4-223">In the tree, select 'Xml\Message\MessageId'.</span></span>
12. <span data-ttu-id="d92c4-224">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="d92c4-224">Click Add to open the drop dialog.</span></span>
13. <span data-ttu-id="d92c4-225">في الشجرة، حدد "Text\String".</span><span class="sxs-lookup"><span data-stu-id="d92c4-225">In the tree, select 'Text\String'.</span></span>
14. <span data-ttu-id="d92c4-226">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="d92c4-226">Click OK.</span></span>
15. <span data-ttu-id="d92c4-227">في الشجرة، حدد "Xml\الرسالة\المدفوعات\الصنف\المورّد\الاسم".</span><span class="sxs-lookup"><span data-stu-id="d92c4-227">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name'.</span></span>
16. <span data-ttu-id="d92c4-228">انقر فوق "إضافة سلسلة".</span><span class="sxs-lookup"><span data-stu-id="d92c4-228">Click Add String.</span></span>
17. <span data-ttu-id="d92c4-229">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="d92c4-229">Click OK.</span></span>
18. <span data-ttu-id="d92c4-230">في الشجرة، حدد "Xml\الرسالة\المدفوعات\الصنف\المورّد\البنك\RoutingNumber".</span><span class="sxs-lookup"><span data-stu-id="d92c4-230">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber'.</span></span>
19. <span data-ttu-id="d92c4-231">انقر فوق "إضافة سلسلة".</span><span class="sxs-lookup"><span data-stu-id="d92c4-231">Click Add String.</span></span>
20. <span data-ttu-id="d92c4-232">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="d92c4-232">Click OK.</span></span>
21. <span data-ttu-id="d92c4-233">في الشجرة، حدد "Xml\الرسالة\المدفوعات\الصنف\المورّد\البنك\AccountNumber".</span><span class="sxs-lookup"><span data-stu-id="d92c4-233">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber'.</span></span>
22. <span data-ttu-id="d92c4-234">انقر فوق "إضافة سلسلة".</span><span class="sxs-lookup"><span data-stu-id="d92c4-234">Click Add String.</span></span>
23. <span data-ttu-id="d92c4-235">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="d92c4-235">Click OK.</span></span>
24. <span data-ttu-id="d92c4-236">في الشجرة، حدد "Xml\الرسالة\المدفوعات\الصنف\الممول\الاسم".</span><span class="sxs-lookup"><span data-stu-id="d92c4-236">In the tree, select 'Xml\Message\Payments\Item\Payer\Name'.</span></span>
25. <span data-ttu-id="d92c4-237">انقر فوق "إضافة سلسلة".</span><span class="sxs-lookup"><span data-stu-id="d92c4-237">Click Add String.</span></span>
26. <span data-ttu-id="d92c4-238">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="d92c4-238">Click OK.</span></span>
27. <span data-ttu-id="d92c4-239">في الشجرة، حدد "Xml\الرسالة\المدفوعات\الصنف\الممول\البنك\RoutingNumber".</span><span class="sxs-lookup"><span data-stu-id="d92c4-239">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber'.</span></span>
28. <span data-ttu-id="d92c4-240">انقر فوق "إضافة سلسلة".</span><span class="sxs-lookup"><span data-stu-id="d92c4-240">Click Add String.</span></span>
29. <span data-ttu-id="d92c4-241">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="d92c4-241">Click OK.</span></span>
30. <span data-ttu-id="d92c4-242">في الشجرة، حدد "Xml\الرسالة\المدفوعات\الصنف\الممول\البنك\AccountNumber".‬</span><span class="sxs-lookup"><span data-stu-id="d92c4-242">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber'.</span></span>
31. <span data-ttu-id="d92c4-243">انقر فوق "إضافة سلسلة".</span><span class="sxs-lookup"><span data-stu-id="d92c4-243">Click Add String.</span></span>
32. <span data-ttu-id="d92c4-244">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="d92c4-244">Click OK.</span></span>
33. <span data-ttu-id="d92c4-245">في الشجرة، حدد "Xml\الرسالة\المدفوعات\الصنف\العملة".</span><span class="sxs-lookup"><span data-stu-id="d92c4-245">In the tree, select 'Xml\Message\Payments\Item\Currency'.</span></span>
34. <span data-ttu-id="d92c4-246">انقر فوق "إضافة سلسلة".</span><span class="sxs-lookup"><span data-stu-id="d92c4-246">Click Add String.</span></span>
35. <span data-ttu-id="d92c4-247">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="d92c4-247">Click OK.</span></span>
36. <span data-ttu-id="d92c4-248">في الشجرة، حدد "Xml\الرسالة\المدفوعات\الصنف\الوصف".‬</span><span class="sxs-lookup"><span data-stu-id="d92c4-248">In the tree, select 'Xml\Message\Payments\Item\Description'.</span></span>
37. <span data-ttu-id="d92c4-249">انقر فوق "إضافة سلسلة".</span><span class="sxs-lookup"><span data-stu-id="d92c4-249">Click Add String.</span></span>
38. <span data-ttu-id="d92c4-250">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="d92c4-250">Click OK.</span></span>
39. <span data-ttu-id="d92c4-251">في الشجرة، حدد "Xml\الرسالة\المدفوعات\الصنف\المبلغ".‬</span><span class="sxs-lookup"><span data-stu-id="d92c4-251">In the tree, select 'Xml\Message\Payments\Item\Amount'.</span></span>
40. <span data-ttu-id="d92c4-252">انقر فوق "إضافة سلسلة".</span><span class="sxs-lookup"><span data-stu-id="d92c4-252">Click Add String.</span></span>
41. <span data-ttu-id="d92c4-253">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="d92c4-253">Click OK.</span></span>
42. <span data-ttu-id="d92c4-254">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="d92c4-254">Click Save.</span></span>
43. <span data-ttu-id="d92c4-255">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d92c4-255">Close the page.</span></span>


