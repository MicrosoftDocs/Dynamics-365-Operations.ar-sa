--- 
title: "التقارير الإلكترونية - إنشاء تكوين تنسيق (نوفمبر 2016)"
description: "تشرح الخطوات التالية كيف يمكن لمستخدم بدور مسؤول النظام أو مطور التقارير الإلكترونية إنشاء تكوين تنسيق لإنشاء التقارير الإلكترونية."
author: NickSelin
manager: AnnBe
ms.date: 11/27/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f004451a260b5be6c15c3975cd9e63ba9c1a7a2e
ms.openlocfilehash: 6fa5023a29c95ab9f10d8aacd51edc1a06c3c152
ms.contentlocale: ar-sa
ms.lasthandoff: 02/06/2019

---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="7700b-103">التقارير الإلكترونية - إنشاء تكوين تنسيق (نوفمبر 2016)</span><span class="sxs-lookup"><span data-stu-id="7700b-103">ER Create a format configuration (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7700b-104">تشرح الخطوات التالية كيف يمكن لمستخدم بدور مسؤول النظام أو مطور التقارير الإلكترونية إنشاء تكوين تنسيق لإنشاء التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="7700b-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="7700b-105">وسيحدد هذا التكوين تنسيق المستندات الإلكترونية المستخدمة لمعالجة المدفوعات.</span><span class="sxs-lookup"><span data-stu-id="7700b-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="7700b-106">في هذا المثال، ستقوم بإنشاء تكوين تنسيق لشركة عينة، .Litware, Inc. ولإكمال هذه الخطوات، يجب عليك أولاً إكمال الخطوات المذكورة في الإجراء "تعيين النموذج لمصادر البيانات المحددة".</span><span class="sxs-lookup"><span data-stu-id="7700b-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="7700b-107">قم بإنشاء تكوين تنسيق جديد</span><span class="sxs-lookup"><span data-stu-id="7700b-107">Create a new format configuration</span></span>
1. <span data-ttu-id="7700b-108">انتقل إلى **إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني**‬.</span><span class="sxs-lookup"><span data-stu-id="7700b-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="7700b-109">انقر فوق **تكوينات إعداد التقارير‬**.</span><span class="sxs-lookup"><span data-stu-id="7700b-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="7700b-110">في الشجرة، حدد **المدفوعات (نموذج مبسط)**.</span><span class="sxs-lookup"><span data-stu-id="7700b-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="7700b-111">انقر فوق **إنشاء تكوين** لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="7700b-111">Click **Create configuration** to open the drop dialog.</span></span>

 > [!NOTE]
 > <span data-ttu-id="7700b-112">إذا لم يظهر الخيار **إنشاء تكوين**، فعليك تكوين وضع التصميم في صفحة **معلمات ‏‫إعداد التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="7700b-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
 
5. <span data-ttu-id="7700b-113">في الحقل **جديد**، أدخل **التنسيق استناداً إلى نموذج الدفع الخاص بنموذج البيانات**.</span><span class="sxs-lookup"><span data-stu-id="7700b-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="7700b-114">في الحقل **الاسم**، اكتب **BACS (وهمية من المملكة المتحدة)**.</span><span class="sxs-lookup"><span data-stu-id="7700b-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="7700b-115">في حقل **الوصف**، اكتب **تنسيق دفع المورد BACS (وهمية من المملكة المتحدة)**.</span><span class="sxs-lookup"><span data-stu-id="7700b-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="7700b-116">يتم تلقائيًا إدخال موفر التكوين النشط هنا.</span><span class="sxs-lookup"><span data-stu-id="7700b-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="7700b-117">سيكون هذا الموفر قادرًا على المحافظة على هذا التكوين.</span><span class="sxs-lookup"><span data-stu-id="7700b-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="7700b-118">باستطاعة موفرين آخرين استخدام هذا التكوين، ولكن لن يكون باستطاعتهم المحافظة عليه.</span><span class="sxs-lookup"><span data-stu-id="7700b-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="7700b-119">يمكن تعريف تنسيق معين لوثيقة إلكترونية.</span><span class="sxs-lookup"><span data-stu-id="7700b-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="7700b-120">اترك هذا الحقل فارغاً إذا كنت تريد تحديد تنسيق في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="7700b-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="7700b-121">في الحقل **تعريف نموذج البيانات**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="7700b-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="7700b-122">وانقر فوق **إنشاء تكوين**.</span><span class="sxs-lookup"><span data-stu-id="7700b-122">Click **Create configuration**.</span></span> <span data-ttu-id="7700b-123">تم إنشاء تكوين جديد.</span><span class="sxs-lookup"><span data-stu-id="7700b-123">A new configuration has been created.</span></span> <span data-ttu-id="7700b-124">يمكن استخدام الإصدار التمهيدي لتخزين تنسيق التصميم لإدارة الوثائق الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="7700b-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  

 > [!NOTE]
 > <span data-ttu-id="7700b-125">إذا لم يظهر الخيار **إنشاء تكوين**، فعليك تكوين وضع التصميم في صفحة **معلمات ‏‫إعداد التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="7700b-125">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span>


## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="7700b-126">تصميم تنسيق مستند إلكتروني</span><span class="sxs-lookup"><span data-stu-id="7700b-126">Design the format of an electronic document</span></span>
1. <span data-ttu-id="7700b-127">انقر فوق **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="7700b-127">Click **Designer**.</span></span>
2. <span data-ttu-id="7700b-128">انقر فوق **إضافة جذر** لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="7700b-128">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="7700b-129">في الشجرة، حدد **Common\File**.</span><span class="sxs-lookup"><span data-stu-id="7700b-129">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="7700b-130">في حقل **الاسم**، اكتب **Xml**.</span><span class="sxs-lookup"><span data-stu-id="7700b-130">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="7700b-131">في حقل **الترميز**، اكتب **UTF-8**.</span><span class="sxs-lookup"><span data-stu-id="7700b-131">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="7700b-132">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7700b-132">Click **OK**.</span></span>
7. <span data-ttu-id="7700b-133">النقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="7700b-133">Click **Add**.</span></span>
8. <span data-ttu-id="7700b-134">في الشجرة، **XML\العنصر**.</span><span class="sxs-lookup"><span data-stu-id="7700b-134">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="7700b-135">في الحقل **الاسم**، اكتب **رسالة**.</span><span class="sxs-lookup"><span data-stu-id="7700b-135">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="7700b-136">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7700b-136">Click **OK**.</span></span>
11. <span data-ttu-id="7700b-137">في الشجرة، حدد **Xml\الرسالة**.</span><span class="sxs-lookup"><span data-stu-id="7700b-137">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="7700b-138">انقر فوق **إضافة عنصر**.</span><span class="sxs-lookup"><span data-stu-id="7700b-138">Click **Add Element**.</span></span>
13. <span data-ttu-id="7700b-139">في حقل **الاسم**، اكتب **تاريخ المعالجة**.</span><span class="sxs-lookup"><span data-stu-id="7700b-139">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="7700b-140">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7700b-140">Click **OK**.</span></span>
15. <span data-ttu-id="7700b-141">انقر فوق **إضافة عنصر**.</span><span class="sxs-lookup"><span data-stu-id="7700b-141">Click **Add Element**.</span></span>
16. <span data-ttu-id="7700b-142">في حقل الاسم، اكتب **MessageId**.</span><span class="sxs-lookup"><span data-stu-id="7700b-142">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="7700b-143">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7700b-143">Click **OK**.</span></span>
18. <span data-ttu-id="7700b-144">انقر فوق **إضافة عنصر**.</span><span class="sxs-lookup"><span data-stu-id="7700b-144">Click **Add Element**.</span></span>
19. <span data-ttu-id="7700b-145">في حقل **الاسم**، اكتب **دفعات**.</span><span class="sxs-lookup"><span data-stu-id="7700b-145">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="7700b-146">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7700b-146">Click **OK**.</span></span>
21. <span data-ttu-id="7700b-147">في الشجرة، حدد **Xml\الرسالة\المدفوعات**.</span><span class="sxs-lookup"><span data-stu-id="7700b-147">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="7700b-148">انقر فوق **إضافة عنصر**.</span><span class="sxs-lookup"><span data-stu-id="7700b-148">Click **Add Element**.</span></span>
23. <span data-ttu-id="7700b-149">في الحقل **الاسم**، اكتب **الصنف**.</span><span class="sxs-lookup"><span data-stu-id="7700b-149">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="7700b-150">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7700b-150">Click **OK**.</span></span>
25. <span data-ttu-id="7700b-151">في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف**.</span><span class="sxs-lookup"><span data-stu-id="7700b-151">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="7700b-152">النقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="7700b-152">Click **Add**.</span></span>
27. <span data-ttu-id="7700b-153">في الشجرة، حدد **XML\سمة**.</span><span class="sxs-lookup"><span data-stu-id="7700b-153">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="7700b-154">في حقل الاسم، اكتب **المعرف**.</span><span class="sxs-lookup"><span data-stu-id="7700b-154">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="7700b-155">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7700b-155">Click **OK**.</span></span>
30. <span data-ttu-id="7700b-156">النقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="7700b-156">Click **Add**.</span></span>
31. <span data-ttu-id="7700b-157">في الشجرة، **XML\العنصر**.</span><span class="sxs-lookup"><span data-stu-id="7700b-157">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="7700b-158">في حقل الاسم، اكتب **المورّد**.</span><span class="sxs-lookup"><span data-stu-id="7700b-158">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="7700b-159">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7700b-159">Click **OK**.</span></span>
34. <span data-ttu-id="7700b-160">في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\المورّد**.</span><span class="sxs-lookup"><span data-stu-id="7700b-160">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="7700b-161">انقر فوق **إضافة عنصر**.</span><span class="sxs-lookup"><span data-stu-id="7700b-161">Click **Add Element**.</span></span>
36. <span data-ttu-id="7700b-162">في الحقل "الاسم"، اكتب **الاسم**.</span><span class="sxs-lookup"><span data-stu-id="7700b-162">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="7700b-163">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7700b-163">Click **OK**.</span></span>
38. <span data-ttu-id="7700b-164">انقر فوق **إضافة عنصر**.</span><span class="sxs-lookup"><span data-stu-id="7700b-164">Click **Add Element**.</span></span>
39. <span data-ttu-id="7700b-165">في الحقل **الاسم**، اكتب **البنك**.</span><span class="sxs-lookup"><span data-stu-id="7700b-165">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="7700b-166">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7700b-166">Click **OK**.</span></span>
41. <span data-ttu-id="7700b-167">في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\المورّد\البنك**.</span><span class="sxs-lookup"><span data-stu-id="7700b-167">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="7700b-168">انقر فوق **إضافة عنصر**.</span><span class="sxs-lookup"><span data-stu-id="7700b-168">Click **Add Element**.</span></span>
43. <span data-ttu-id="7700b-169">في الحقل **الاسم**، اكتب **RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="7700b-169">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="7700b-170">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7700b-170">Click **OK**.</span></span>
45. <span data-ttu-id="7700b-171">انقر فوق **إضافة عنصر**.</span><span class="sxs-lookup"><span data-stu-id="7700b-171">Click **Add Element**.</span></span>
46. <span data-ttu-id="7700b-172">في الحقل **الاسم**، اكتب **AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="7700b-172">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="7700b-173">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7700b-173">Click **OK**.</span></span>
48. <span data-ttu-id="7700b-174">في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\المورّد**.</span><span class="sxs-lookup"><span data-stu-id="7700b-174">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="7700b-175">انقر فوق **نسخ**.</span><span class="sxs-lookup"><span data-stu-id="7700b-175">Click **Copy**.</span></span>
50. <span data-ttu-id="7700b-176">في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف**.</span><span class="sxs-lookup"><span data-stu-id="7700b-176">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="7700b-177">انقر فوق **لصق**.</span><span class="sxs-lookup"><span data-stu-id="7700b-177">Click **Paste**.</span></span>
52. <span data-ttu-id="7700b-178">في الحقل **الاسم**، اكتب **الممول‬**.</span><span class="sxs-lookup"><span data-stu-id="7700b-178">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="7700b-179">في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف**.</span><span class="sxs-lookup"><span data-stu-id="7700b-179">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="7700b-180">انقر فوق **إضافة عنصر**.</span><span class="sxs-lookup"><span data-stu-id="7700b-180">Click **Add Element**.</span></span>
55. <span data-ttu-id="7700b-181">في الحقل **الاسم**، اكتب **العملة**.</span><span class="sxs-lookup"><span data-stu-id="7700b-181">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="7700b-182">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7700b-182">Click **OK**.</span></span>
57. <span data-ttu-id="7700b-183">انقر فوق **إضافة عنصر**.</span><span class="sxs-lookup"><span data-stu-id="7700b-183">Click **Add Element**.</span></span>
58. <span data-ttu-id="7700b-184">في الحقل **الاسم**، اكتب **الوصف**.</span><span class="sxs-lookup"><span data-stu-id="7700b-184">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="7700b-185">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7700b-185">Click **OK**.</span></span>
60. <span data-ttu-id="7700b-186">انقر فوق **إضافة عنصر**.</span><span class="sxs-lookup"><span data-stu-id="7700b-186">Click **Add Element**.</span></span>
61. <span data-ttu-id="7700b-187">في الحقل "الاسم"، اكتب **TransDate**.</span><span class="sxs-lookup"><span data-stu-id="7700b-187">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="7700b-188">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7700b-188">Click **OK**.</span></span>
63. <span data-ttu-id="7700b-189">انقر فوق **إضافة عنصر**.</span><span class="sxs-lookup"><span data-stu-id="7700b-189">Click **Add Element**.</span></span>
64. <span data-ttu-id="7700b-190">في الحقل "الاسم"، اكتب **المبلغ**.</span><span class="sxs-lookup"><span data-stu-id="7700b-190">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="7700b-191">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7700b-191">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="7700b-192">إعداد مكونات التنسيق لتعيينها لعناصر نماذج البيانات</span><span class="sxs-lookup"><span data-stu-id="7700b-192">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="7700b-193">في الشجرة، حدد **Xml\الرسالة\ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="7700b-193">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="7700b-194">انقر فوق **إضافة** لفتح مربع حوار الإسقاط.</span><span class="sxs-lookup"><span data-stu-id="7700b-194">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="7700b-195">في الشجرة، حدد **النص\DateTime**.</span><span class="sxs-lookup"><span data-stu-id="7700b-195">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="7700b-196">في الحقل **التنسيق**، اكتب **yyyy-MM-dd**.</span><span class="sxs-lookup"><span data-stu-id="7700b-196">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="7700b-197">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7700b-197">Click **OK**.</span></span>
6. <span data-ttu-id="7700b-198">في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\TransDate**.</span><span class="sxs-lookup"><span data-stu-id="7700b-198">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="7700b-199">انقر فوق **إضافة التاريخ والوقت**.</span><span class="sxs-lookup"><span data-stu-id="7700b-199">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="7700b-200">في الحقل **التنسيق**، اكتب **yyyy-MM-dd**.</span><span class="sxs-lookup"><span data-stu-id="7700b-200">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="7700b-201">في الحقل نوع **التاريخ والوقت**، حدد **التاريخ**.</span><span class="sxs-lookup"><span data-stu-id="7700b-201">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="7700b-202">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7700b-202">Click **OK**.</span></span>
11. <span data-ttu-id="7700b-203">في الشجرة، حدد **Xml\الرسالة\MessageId**.</span><span class="sxs-lookup"><span data-stu-id="7700b-203">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="7700b-204">انقر فوق **إضافة** لفتح مربع حوار الإسقاط.</span><span class="sxs-lookup"><span data-stu-id="7700b-204">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="7700b-205">في الشجرة، حدد **نص\سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="7700b-205">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="7700b-206">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7700b-206">Click **OK**.</span></span>
15. <span data-ttu-id="7700b-207">في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\المورّد\الاسم**.</span><span class="sxs-lookup"><span data-stu-id="7700b-207">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="7700b-208">انقر فوق **إضافة سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="7700b-208">Click **Add String**.</span></span>
17. <span data-ttu-id="7700b-209">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7700b-209">Click **OK**.</span></span>
18. <span data-ttu-id="7700b-210">في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\المورّد\البنك\RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="7700b-210">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="7700b-211">انقر فوق **إضافة سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="7700b-211">Click **Add String**.</span></span>
20. <span data-ttu-id="7700b-212">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7700b-212">Click **OK**.</span></span>
21. <span data-ttu-id="7700b-213">في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\المورّد\البنك\AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="7700b-213">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="7700b-214">انقر فوق **إضافة سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="7700b-214">Click **Add String**.</span></span>
23. <span data-ttu-id="7700b-215">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7700b-215">Click **OK**.</span></span>
24. <span data-ttu-id="7700b-216">في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\الممول\الاسم**.</span><span class="sxs-lookup"><span data-stu-id="7700b-216">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="7700b-217">انقر فوق **إضافة سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="7700b-217">Click **Add String**.</span></span>
26. <span data-ttu-id="7700b-218">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7700b-218">Click **OK**.</span></span>
27. <span data-ttu-id="7700b-219">في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\الممول\البنك\RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="7700b-219">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="7700b-220">انقر فوق **إضافة سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="7700b-220">Click **Add String**.</span></span>
29. <span data-ttu-id="7700b-221">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7700b-221">Click **OK**.</span></span>
30. <span data-ttu-id="7700b-222">في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\الممول\البنك\AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="7700b-222">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="7700b-223">انقر فوق **إضافة سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="7700b-223">Click **Add String**.</span></span>
32. <span data-ttu-id="7700b-224">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7700b-224">Click **OK**.</span></span>
33. <span data-ttu-id="7700b-225">في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\العملة**.</span><span class="sxs-lookup"><span data-stu-id="7700b-225">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="7700b-226">انقر فوق **إضافة سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="7700b-226">Click **Add String**.</span></span>
35. <span data-ttu-id="7700b-227">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7700b-227">Click **OK**.</span></span>
36. <span data-ttu-id="7700b-228">في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\الوصف**.</span><span class="sxs-lookup"><span data-stu-id="7700b-228">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="7700b-229">انقر فوق **إضافة سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="7700b-229">Click **Add String**.</span></span>
38. <span data-ttu-id="7700b-230">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7700b-230">Click **OK**.</span></span>
39. <span data-ttu-id="7700b-231">في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\المبلغ**.‬</span><span class="sxs-lookup"><span data-stu-id="7700b-231">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="7700b-232">انقر فوق **إضافة سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="7700b-232">Click **Add String**.</span></span>
41. <span data-ttu-id="7700b-233">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7700b-233">Click **OK**.</span></span>
42. <span data-ttu-id="7700b-234">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="7700b-234">Click **Save**.</span></span>
43. <span data-ttu-id="7700b-235">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7700b-235">Close the page.</span></span>


