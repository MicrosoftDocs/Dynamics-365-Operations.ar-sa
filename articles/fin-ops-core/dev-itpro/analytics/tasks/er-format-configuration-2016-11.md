---
title: التقارير الإلكترونية - إنشاء تكوين تنسيق (نوفمبر 2016)
description: يشرح هذا الموضوع كيف يمكن لمستخدم يؤدي دور مسؤول النظام أو مطور التقارير الإلكترونية إنشاء تكوين تنسيق لإنشاء التقارير الإلكترونية.
author: NickSelin
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af2899da843967bfaaa8f3c66906fc8e3765b573
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142491"
---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="f4344-103">التقارير الإلكترونية - إنشاء تكوين تنسيق (نوفمبر 2016)</span><span class="sxs-lookup"><span data-stu-id="f4344-103">ER Create a format configuration (November 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f4344-104">يشرح هذا الموضوع كيف يمكن لمستخدم يؤدي دور مسؤول النظام أو مطور التقارير الإلكترونية إنشاء تكوين تنسيق لإنشاء التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="f4344-104">This topic explains how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="f4344-105">وسيحدد هذا التكوين تنسيق المستندات الإلكترونية المستخدمة لمعالجة المدفوعات.</span><span class="sxs-lookup"><span data-stu-id="f4344-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="f4344-106">في هذا المثال، ستقوم بإنشاء تكوين تنسيق لشركة عينة، .Litware, Inc. ولإكمال هذه الخطوات، يجب عليك أولاً إكمال الخطوات المذكورة في الإجراء "تعيين النموذج لمصادر البيانات المحددة".</span><span class="sxs-lookup"><span data-stu-id="f4344-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the "Map model to selected datasources" procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="f4344-107">قم بإنشاء تكوين تنسيق جديد</span><span class="sxs-lookup"><span data-stu-id="f4344-107">Create a new format configuration</span></span>
1. <span data-ttu-id="f4344-108">انتقل إلى **إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني**‬.</span><span class="sxs-lookup"><span data-stu-id="f4344-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="f4344-109">انقر فوق **تكوينات إعداد التقارير‬**.</span><span class="sxs-lookup"><span data-stu-id="f4344-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="f4344-110">في الشجرة، حدد **المدفوعات (نموذج مبسط)**.</span><span class="sxs-lookup"><span data-stu-id="f4344-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="f4344-111">انقر فوق **إنشاء تكوين** لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="f4344-111">Click **Create configuration** to open the drop dialog.</span></span>

 > [!NOTE]
 > <span data-ttu-id="f4344-112">إذا لم يظهر الخيار **إنشاء تكوين**، فعليك تكوين وضع التصميم في صفحة **معلمات ‏‫إعداد التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="f4344-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
 
5. <span data-ttu-id="f4344-113">في الحقل **جديد**، أدخل **التنسيق استناداً إلى نموذج الدفع الخاص بنموذج البيانات**.</span><span class="sxs-lookup"><span data-stu-id="f4344-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="f4344-114">في الحقل **الاسم**، اكتب **BACS (وهمية من المملكة المتحدة)**.</span><span class="sxs-lookup"><span data-stu-id="f4344-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="f4344-115">في حقل **الوصف**، اكتب **تنسيق دفع المورد BACS (وهمية من المملكة المتحدة)**.</span><span class="sxs-lookup"><span data-stu-id="f4344-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="f4344-116">يتم تلقائيًا إدخال موفر التكوين النشط هنا.</span><span class="sxs-lookup"><span data-stu-id="f4344-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="f4344-117">سيكون هذا الموفر قادرًا على المحافظة على هذا التكوين.</span><span class="sxs-lookup"><span data-stu-id="f4344-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="f4344-118">باستطاعة موفرين آخرين استخدام هذا التكوين، ولكن لن يكون باستطاعتهم المحافظة عليه.</span><span class="sxs-lookup"><span data-stu-id="f4344-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="f4344-119">يمكن تعريف تنسيق معين لوثيقة إلكترونية.</span><span class="sxs-lookup"><span data-stu-id="f4344-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="f4344-120">اترك هذا الحقل فارغاً إذا كنت تريد تحديد تنسيق في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="f4344-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="f4344-121">في الحقل **تعريف نموذج البيانات**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f4344-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="f4344-122">وانقر فوق **إنشاء تكوين**.</span><span class="sxs-lookup"><span data-stu-id="f4344-122">Click **Create configuration**.</span></span> <span data-ttu-id="f4344-123">تم إنشاء تكوين جديد.</span><span class="sxs-lookup"><span data-stu-id="f4344-123">A new configuration has been created.</span></span> <span data-ttu-id="f4344-124">يمكن استخدام الإصدار التمهيدي لتخزين تنسيق التصميم لإدارة الوثائق الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="f4344-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="f4344-125">تصميم تنسيق مستند إلكتروني</span><span class="sxs-lookup"><span data-stu-id="f4344-125">Design the format of an electronic document</span></span>
1. <span data-ttu-id="f4344-126">انقر فوق **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="f4344-126">Click **Designer**.</span></span>
2. <span data-ttu-id="f4344-127">انقر فوق **إضافة جذر** لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="f4344-127">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="f4344-128">في الشجرة، حدد **Common\File**.</span><span class="sxs-lookup"><span data-stu-id="f4344-128">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="f4344-129">في حقل **الاسم**، اكتب **Xml**.</span><span class="sxs-lookup"><span data-stu-id="f4344-129">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="f4344-130">في حقل **الترميز**، اكتب **UTF-8**.</span><span class="sxs-lookup"><span data-stu-id="f4344-130">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="f4344-131">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f4344-131">Click **OK**.</span></span>
7. <span data-ttu-id="f4344-132">النقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="f4344-132">Click **Add**.</span></span>
8. <span data-ttu-id="f4344-133">في الشجرة، **XML\العنصر**.</span><span class="sxs-lookup"><span data-stu-id="f4344-133">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="f4344-134">في الحقل **الاسم**، اكتب **رسالة**.</span><span class="sxs-lookup"><span data-stu-id="f4344-134">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="f4344-135">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f4344-135">Click **OK**.</span></span>
11. <span data-ttu-id="f4344-136">في الشجرة، حدد **Xml\الرسالة**.</span><span class="sxs-lookup"><span data-stu-id="f4344-136">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="f4344-137">انقر فوق **إضافة عنصر**.</span><span class="sxs-lookup"><span data-stu-id="f4344-137">Click **Add Element**.</span></span>
13. <span data-ttu-id="f4344-138">في حقل **الاسم**، اكتب **تاريخ المعالجة**.</span><span class="sxs-lookup"><span data-stu-id="f4344-138">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="f4344-139">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f4344-139">Click **OK**.</span></span>
15. <span data-ttu-id="f4344-140">انقر فوق **إضافة عنصر**.</span><span class="sxs-lookup"><span data-stu-id="f4344-140">Click **Add Element**.</span></span>
16. <span data-ttu-id="f4344-141">في حقل الاسم، اكتب **MessageId**.</span><span class="sxs-lookup"><span data-stu-id="f4344-141">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="f4344-142">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f4344-142">Click **OK**.</span></span>
18. <span data-ttu-id="f4344-143">انقر فوق **إضافة عنصر**.</span><span class="sxs-lookup"><span data-stu-id="f4344-143">Click **Add Element**.</span></span>
19. <span data-ttu-id="f4344-144">في حقل **الاسم**، اكتب **دفعات**.</span><span class="sxs-lookup"><span data-stu-id="f4344-144">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="f4344-145">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f4344-145">Click **OK**.</span></span>
21. <span data-ttu-id="f4344-146">في الشجرة، حدد **Xml\الرسالة\المدفوعات**.</span><span class="sxs-lookup"><span data-stu-id="f4344-146">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="f4344-147">انقر فوق **إضافة عنصر**.</span><span class="sxs-lookup"><span data-stu-id="f4344-147">Click **Add Element**.</span></span>
23. <span data-ttu-id="f4344-148">في الحقل **الاسم**، اكتب **الصنف**.</span><span class="sxs-lookup"><span data-stu-id="f4344-148">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="f4344-149">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f4344-149">Click **OK**.</span></span>
25. <span data-ttu-id="f4344-150">في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف**.</span><span class="sxs-lookup"><span data-stu-id="f4344-150">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="f4344-151">النقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="f4344-151">Click **Add**.</span></span>
27. <span data-ttu-id="f4344-152">في الشجرة، حدد **XML\سمة**.</span><span class="sxs-lookup"><span data-stu-id="f4344-152">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="f4344-153">في حقل الاسم، اكتب **المعرف**.</span><span class="sxs-lookup"><span data-stu-id="f4344-153">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="f4344-154">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f4344-154">Click **OK**.</span></span>
30. <span data-ttu-id="f4344-155">النقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="f4344-155">Click **Add**.</span></span>
31. <span data-ttu-id="f4344-156">في الشجرة، **XML\العنصر**.</span><span class="sxs-lookup"><span data-stu-id="f4344-156">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="f4344-157">في حقل الاسم، اكتب **المورّد**.</span><span class="sxs-lookup"><span data-stu-id="f4344-157">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="f4344-158">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f4344-158">Click **OK**.</span></span>
34. <span data-ttu-id="f4344-159">في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\المورّد**.</span><span class="sxs-lookup"><span data-stu-id="f4344-159">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="f4344-160">انقر فوق **إضافة عنصر**.</span><span class="sxs-lookup"><span data-stu-id="f4344-160">Click **Add Element**.</span></span>
36. <span data-ttu-id="f4344-161">في الحقل "الاسم"، اكتب **الاسم**.</span><span class="sxs-lookup"><span data-stu-id="f4344-161">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="f4344-162">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f4344-162">Click **OK**.</span></span>
38. <span data-ttu-id="f4344-163">انقر فوق **إضافة عنصر**.</span><span class="sxs-lookup"><span data-stu-id="f4344-163">Click **Add Element**.</span></span>
39. <span data-ttu-id="f4344-164">في الحقل **الاسم**، اكتب **البنك**.</span><span class="sxs-lookup"><span data-stu-id="f4344-164">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="f4344-165">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f4344-165">Click **OK**.</span></span>
41. <span data-ttu-id="f4344-166">في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\المورّد\البنك**.</span><span class="sxs-lookup"><span data-stu-id="f4344-166">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="f4344-167">انقر فوق **إضافة عنصر**.</span><span class="sxs-lookup"><span data-stu-id="f4344-167">Click **Add Element**.</span></span>
43. <span data-ttu-id="f4344-168">في الحقل **الاسم**، اكتب **RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="f4344-168">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="f4344-169">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f4344-169">Click **OK**.</span></span>
45. <span data-ttu-id="f4344-170">انقر فوق **إضافة عنصر**.</span><span class="sxs-lookup"><span data-stu-id="f4344-170">Click **Add Element**.</span></span>
46. <span data-ttu-id="f4344-171">في الحقل **الاسم**، اكتب **AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="f4344-171">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="f4344-172">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f4344-172">Click **OK**.</span></span>
48. <span data-ttu-id="f4344-173">في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\المورّد**.</span><span class="sxs-lookup"><span data-stu-id="f4344-173">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="f4344-174">انقر فوق **نسخ**.</span><span class="sxs-lookup"><span data-stu-id="f4344-174">Click **Copy**.</span></span>
50. <span data-ttu-id="f4344-175">في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف**.</span><span class="sxs-lookup"><span data-stu-id="f4344-175">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="f4344-176">انقر فوق **لصق**.</span><span class="sxs-lookup"><span data-stu-id="f4344-176">Click **Paste**.</span></span>
52. <span data-ttu-id="f4344-177">في الحقل **الاسم**، اكتب **الممول‬**.</span><span class="sxs-lookup"><span data-stu-id="f4344-177">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="f4344-178">في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف**.</span><span class="sxs-lookup"><span data-stu-id="f4344-178">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="f4344-179">انقر فوق **إضافة عنصر**.</span><span class="sxs-lookup"><span data-stu-id="f4344-179">Click **Add Element**.</span></span>
55. <span data-ttu-id="f4344-180">في الحقل **الاسم**، اكتب **العملة**.</span><span class="sxs-lookup"><span data-stu-id="f4344-180">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="f4344-181">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f4344-181">Click **OK**.</span></span>
57. <span data-ttu-id="f4344-182">انقر فوق **إضافة عنصر**.</span><span class="sxs-lookup"><span data-stu-id="f4344-182">Click **Add Element**.</span></span>
58. <span data-ttu-id="f4344-183">في الحقل **الاسم**، اكتب **الوصف**.</span><span class="sxs-lookup"><span data-stu-id="f4344-183">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="f4344-184">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f4344-184">Click **OK**.</span></span>
60. <span data-ttu-id="f4344-185">انقر فوق **إضافة عنصر**.</span><span class="sxs-lookup"><span data-stu-id="f4344-185">Click **Add Element**.</span></span>
61. <span data-ttu-id="f4344-186">في الحقل "الاسم"، اكتب **TransDate**.</span><span class="sxs-lookup"><span data-stu-id="f4344-186">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="f4344-187">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f4344-187">Click **OK**.</span></span>
63. <span data-ttu-id="f4344-188">انقر فوق **إضافة عنصر**.</span><span class="sxs-lookup"><span data-stu-id="f4344-188">Click **Add Element**.</span></span>
64. <span data-ttu-id="f4344-189">في الحقل "الاسم"، اكتب **المبلغ**.</span><span class="sxs-lookup"><span data-stu-id="f4344-189">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="f4344-190">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f4344-190">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="f4344-191">إعداد مكونات التنسيق لتعيينها لعناصر نماذج البيانات</span><span class="sxs-lookup"><span data-stu-id="f4344-191">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="f4344-192">في الشجرة، حدد **Xml\الرسالة\ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="f4344-192">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="f4344-193">انقر فوق **إضافة** لفتح مربع حوار الإسقاط.</span><span class="sxs-lookup"><span data-stu-id="f4344-193">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="f4344-194">في الشجرة، حدد **النص\DateTime**.</span><span class="sxs-lookup"><span data-stu-id="f4344-194">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="f4344-195">في الحقل **التنسيق**، اكتب **yyyy-MM-dd**.</span><span class="sxs-lookup"><span data-stu-id="f4344-195">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="f4344-196">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f4344-196">Click **OK**.</span></span>
6. <span data-ttu-id="f4344-197">في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\TransDate**.</span><span class="sxs-lookup"><span data-stu-id="f4344-197">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="f4344-198">انقر فوق **إضافة التاريخ والوقت**.</span><span class="sxs-lookup"><span data-stu-id="f4344-198">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="f4344-199">في الحقل **التنسيق**، اكتب **yyyy-MM-dd**.</span><span class="sxs-lookup"><span data-stu-id="f4344-199">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="f4344-200">في الحقل نوع **التاريخ والوقت**، حدد **التاريخ**.</span><span class="sxs-lookup"><span data-stu-id="f4344-200">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="f4344-201">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f4344-201">Click **OK**.</span></span>
11. <span data-ttu-id="f4344-202">في الشجرة، حدد **Xml\الرسالة\MessageId**.</span><span class="sxs-lookup"><span data-stu-id="f4344-202">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="f4344-203">انقر فوق **إضافة** لفتح مربع حوار الإسقاط.</span><span class="sxs-lookup"><span data-stu-id="f4344-203">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="f4344-204">في الشجرة، حدد **نص\سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="f4344-204">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="f4344-205">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f4344-205">Click **OK**.</span></span>
15. <span data-ttu-id="f4344-206">في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\المورّد\الاسم**.</span><span class="sxs-lookup"><span data-stu-id="f4344-206">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="f4344-207">انقر فوق **إضافة سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="f4344-207">Click **Add String**.</span></span>
17. <span data-ttu-id="f4344-208">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f4344-208">Click **OK**.</span></span>
18. <span data-ttu-id="f4344-209">في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\المورّد\البنك\RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="f4344-209">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="f4344-210">انقر فوق **إضافة سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="f4344-210">Click **Add String**.</span></span>
20. <span data-ttu-id="f4344-211">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f4344-211">Click **OK**.</span></span>
21. <span data-ttu-id="f4344-212">في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\المورّد\البنك\AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="f4344-212">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="f4344-213">انقر فوق **إضافة سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="f4344-213">Click **Add String**.</span></span>
23. <span data-ttu-id="f4344-214">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f4344-214">Click **OK**.</span></span>
24. <span data-ttu-id="f4344-215">في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\الممول\الاسم**.</span><span class="sxs-lookup"><span data-stu-id="f4344-215">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="f4344-216">انقر فوق **إضافة سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="f4344-216">Click **Add String**.</span></span>
26. <span data-ttu-id="f4344-217">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f4344-217">Click **OK**.</span></span>
27. <span data-ttu-id="f4344-218">في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\الممول\البنك\RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="f4344-218">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="f4344-219">انقر فوق **إضافة سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="f4344-219">Click **Add String**.</span></span>
29. <span data-ttu-id="f4344-220">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f4344-220">Click **OK**.</span></span>
30. <span data-ttu-id="f4344-221">في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\الممول\البنك\AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="f4344-221">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="f4344-222">انقر فوق **إضافة سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="f4344-222">Click **Add String**.</span></span>
32. <span data-ttu-id="f4344-223">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f4344-223">Click **OK**.</span></span>
33. <span data-ttu-id="f4344-224">في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\العملة**.</span><span class="sxs-lookup"><span data-stu-id="f4344-224">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="f4344-225">انقر فوق **إضافة سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="f4344-225">Click **Add String**.</span></span>
35. <span data-ttu-id="f4344-226">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f4344-226">Click **OK**.</span></span>
36. <span data-ttu-id="f4344-227">في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\الوصف**.</span><span class="sxs-lookup"><span data-stu-id="f4344-227">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="f4344-228">انقر فوق **إضافة سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="f4344-228">Click **Add String**.</span></span>
38. <span data-ttu-id="f4344-229">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f4344-229">Click **OK**.</span></span>
39. <span data-ttu-id="f4344-230">في الشجرة، حدد **Xml\الرسالة\المدفوعات\الصنف\المبلغ**.‬</span><span class="sxs-lookup"><span data-stu-id="f4344-230">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="f4344-231">انقر فوق **إضافة سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="f4344-231">Click **Add String**.</span></span>
41. <span data-ttu-id="f4344-232">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f4344-232">Click **OK**.</span></span>
42. <span data-ttu-id="f4344-233">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="f4344-233">Click **Save**.</span></span>
43. <span data-ttu-id="f4344-234">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f4344-234">Close the page.</span></span>
