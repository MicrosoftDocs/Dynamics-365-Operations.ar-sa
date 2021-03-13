---
title: التقارير الإلكترونية - استخدام الأبعاد المالية كمصدر بيانات (الجزء 3 - تصميم التقرير)
description: يوضح هذا الموضوع كيفيه تكوين نموذج التقرير الكتروني (ER) لاستخدام الابعاد المالية كمصدر بيانات لتقارير ER. (جزء 3)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b0d6da96850e04d5e975b3febbfae2737c8a86af
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092290"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="9c77e-104">التقارير الإلكترونية - استخدام الأبعاد المالية كمصدر بيانات (الجزء 3 - تصميم التقرير)</span><span class="sxs-lookup"><span data-stu-id="9c77e-104">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9c77e-105">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين نموذج التقارير الإلكترونية لاستخدام الأبعاد المالية كمصدر بيانات للتقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="9c77e-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="9c77e-106">يمكن تنفيذ هذه الخطوات في أي شركة.</span><span class="sxs-lookup"><span data-stu-id="9c77e-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="9c77e-107">لإتمام هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "التقارير الإلكترونية - استخدام الأبعاد المالية كمصدر بيانات (الجزء 2: تعيين النموذج)‬".</span><span class="sxs-lookup"><span data-stu-id="9c77e-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="9c77e-108">تصميم تقرير لتقديم الأبعاد المالية</span><span class="sxs-lookup"><span data-stu-id="9c77e-108">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="9c77e-109">انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.</span><span class="sxs-lookup"><span data-stu-id="9c77e-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="9c77e-110">في الشجرة، حدد "نموذج الأبعاد المالية".</span><span class="sxs-lookup"><span data-stu-id="9c77e-110">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="9c77e-111">انقر فوق "إنشاء تكوين" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="9c77e-111">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="9c77e-112">في الحقل "جديد"، أدخل 'التنسيق المستند إلى نموذج البيانات نموذج الأبعاد المالية".</span><span class="sxs-lookup"><span data-stu-id="9c77e-112">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="9c77e-113">استخدم النموذج الذي تم إنشاؤه مسبقًا كمصدر بيانات للتقرير الجديد.</span><span class="sxs-lookup"><span data-stu-id="9c77e-113">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="9c77e-114">في حقل "الاسم"، اكتب "تقرير دفتر يومية دفتر الأستاذ‬".</span><span class="sxs-lookup"><span data-stu-id="9c77e-114">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="9c77e-115">في الحقل "تعريف نموذج البيانات"، حدد "الإدخال".</span><span class="sxs-lookup"><span data-stu-id="9c77e-115">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="9c77e-116">وانقر فوق إنشاء تكوين.</span><span class="sxs-lookup"><span data-stu-id="9c77e-116">Click Create configuration.</span></span>
8. <span data-ttu-id="9c77e-117">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="9c77e-117">Click Designer.</span></span>
9. <span data-ttu-id="9c77e-118">انقر فوق "إضافة جذر" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="9c77e-118">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="9c77e-119">في الشجرة، حدد XML/العنصر".</span><span class="sxs-lookup"><span data-stu-id="9c77e-119">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="9c77e-120">في حقل "الاسم" اكتب "الجذر‬".</span><span class="sxs-lookup"><span data-stu-id="9c77e-120">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="9c77e-121">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="9c77e-121">Click OK.</span></span>
13. <span data-ttu-id="9c77e-122">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="9c77e-122">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="9c77e-123">في الشجرة، حدد "XML\سمة".</span><span class="sxs-lookup"><span data-stu-id="9c77e-123">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="9c77e-124">في الحقل "الاسم"، اكتب "الشركة".</span><span class="sxs-lookup"><span data-stu-id="9c77e-124">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="9c77e-125">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="9c77e-125">Click OK.</span></span>
17. <span data-ttu-id="9c77e-126">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="9c77e-126">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="9c77e-127">في الشجرة، حدد XML/العنصر".</span><span class="sxs-lookup"><span data-stu-id="9c77e-127">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="9c77e-128">في حقل "الاسم"، اكتب "دفتر اليومية".</span><span class="sxs-lookup"><span data-stu-id="9c77e-128">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="9c77e-129">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="9c77e-129">Click OK.</span></span>
21. <span data-ttu-id="9c77e-130">في الشجرة، حدد 'الجذر: عنصر XML\دفتر اليومية: عنصر XML'.</span><span class="sxs-lookup"><span data-stu-id="9c77e-130">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="9c77e-131">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="9c77e-131">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="9c77e-132">في الشجرة، حدد "XML\سمة".</span><span class="sxs-lookup"><span data-stu-id="9c77e-132">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="9c77e-133">في حقل "الاسم"، اكتب "الدُفعة".</span><span class="sxs-lookup"><span data-stu-id="9c77e-133">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="9c77e-134">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="9c77e-134">Click OK.</span></span>
26. <span data-ttu-id="9c77e-135">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="9c77e-135">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="9c77e-136">في الشجرة، حدد XML/العنصر".</span><span class="sxs-lookup"><span data-stu-id="9c77e-136">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="9c77e-137">في حقل "الاسم"، اكتب "الحركة".</span><span class="sxs-lookup"><span data-stu-id="9c77e-137">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="9c77e-138">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="9c77e-138">Click OK.</span></span>
30. <span data-ttu-id="9c77e-139">في الشجرة، حدد "الجذر: عنصر XML\دفتر اليومية: عنصر XML\الحركة: عنصر XML".</span><span class="sxs-lookup"><span data-stu-id="9c77e-139">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="9c77e-140">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="9c77e-140">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="9c77e-141">في الشجرة، حدد "XML\سمة".</span><span class="sxs-lookup"><span data-stu-id="9c77e-141">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="9c77e-142">في حقل "الاسم"، اكتب "الإيصال".</span><span class="sxs-lookup"><span data-stu-id="9c77e-142">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="9c77e-143">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="9c77e-143">Click OK.</span></span>
35. <span data-ttu-id="9c77e-144">انقر فوق "إضافة سمة".</span><span class="sxs-lookup"><span data-stu-id="9c77e-144">Click Add Attribute.</span></span>
36. <span data-ttu-id="9c77e-145">في حقل "الاسم"، اكتب "التاريخ".</span><span class="sxs-lookup"><span data-stu-id="9c77e-145">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="9c77e-146">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="9c77e-146">Click OK.</span></span>
38. <span data-ttu-id="9c77e-147">انقر فوق "إضافة سمة".</span><span class="sxs-lookup"><span data-stu-id="9c77e-147">Click Add Attribute.</span></span>
39. <span data-ttu-id="9c77e-148">في الحقل "الاسم"، اكتب "العملة".</span><span class="sxs-lookup"><span data-stu-id="9c77e-148">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="9c77e-149">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="9c77e-149">Click OK.</span></span>
41. <span data-ttu-id="9c77e-150">انقر فوق "إضافة سمة".</span><span class="sxs-lookup"><span data-stu-id="9c77e-150">Click Add Attribute.</span></span>
42. <span data-ttu-id="9c77e-151">في حقل "الاسم"، اكتب "Dt".</span><span class="sxs-lookup"><span data-stu-id="9c77e-151">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="9c77e-152">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="9c77e-152">Click OK.</span></span>
44. <span data-ttu-id="9c77e-153">انقر فوق "إضافة سمة".</span><span class="sxs-lookup"><span data-stu-id="9c77e-153">Click Add Attribute.</span></span>
45. <span data-ttu-id="9c77e-154">في حقل "الاسم"، اكتب "Ct".</span><span class="sxs-lookup"><span data-stu-id="9c77e-154">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="9c77e-155">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="9c77e-155">Click OK.</span></span>
47. <span data-ttu-id="9c77e-156">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="9c77e-156">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="9c77e-157">في الشجرة، حدد XML/العنصر".</span><span class="sxs-lookup"><span data-stu-id="9c77e-157">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="9c77e-158">في حقل "الاسم"، اكتب "الأبعاد".</span><span class="sxs-lookup"><span data-stu-id="9c77e-158">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="9c77e-159">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="9c77e-159">Click OK.</span></span>
51. <span data-ttu-id="9c77e-160">في الشجرة، حدد "الجذر: عنصر XML\دفتر اليومية: عنصر XML\الحركة: عنصر XML\الأبعاد: عنصر XML".</span><span class="sxs-lookup"><span data-stu-id="9c77e-160">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="9c77e-161">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="9c77e-161">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="9c77e-162">في الشجرة، حدد "XML\سمة".</span><span class="sxs-lookup"><span data-stu-id="9c77e-162">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="9c77e-163">في حقل "الاسم"، اكتب "الكود".</span><span class="sxs-lookup"><span data-stu-id="9c77e-163">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="9c77e-164">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="9c77e-164">Click OK.</span></span>
56. <span data-ttu-id="9c77e-165">انقر فوق "إضافة سمة".</span><span class="sxs-lookup"><span data-stu-id="9c77e-165">Click Add Attribute.</span></span>
57. <span data-ttu-id="9c77e-166">في حقل "الاسم"، اكتب "قيمة".</span><span class="sxs-lookup"><span data-stu-id="9c77e-166">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="9c77e-167">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="9c77e-167">Click OK.</span></span>
59. <span data-ttu-id="9c77e-168">انقر فوق "إضافة سمة".</span><span class="sxs-lookup"><span data-stu-id="9c77e-168">Click Add Attribute.</span></span>
60. <span data-ttu-id="9c77e-169">في حقل "الاسم"، اكتب "الوصف".</span><span class="sxs-lookup"><span data-stu-id="9c77e-169">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="9c77e-170">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="9c77e-170">Click OK.</span></span>
<span data-ttu-id="9c77e-171">![صفحة مصمم عمليات التقارير الإلكترونية](../media/er-financial-dimensions-guides-format1.png)</span><span class="sxs-lookup"><span data-stu-id="9c77e-171">![ER Operations designer page](../media/er-financial-dimensions-guides-format1.png)</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="9c77e-172">تعيين عناصر التقرير إلى مصادر بيانات</span><span class="sxs-lookup"><span data-stu-id="9c77e-172">Map report elements to data sources</span></span>
1. <span data-ttu-id="9c77e-173">انقر فوق علامة التبويب "التعيين".</span><span class="sxs-lookup"><span data-stu-id="9c77e-173">Click the Mapping tab.</span></span>
2. <span data-ttu-id="9c77e-174">في الشجرة، قم بتوسيع "النموذج: نموذج البيانات نموذج الأبعاد المالية".</span><span class="sxs-lookup"><span data-stu-id="9c77e-174">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="9c77e-175">في الشجرة، قم بتوسيع "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات".</span><span class="sxs-lookup"><span data-stu-id="9c77e-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="9c77e-176">في الشجرة، قم بتوسيع "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات".</span><span class="sxs-lookup"><span data-stu-id="9c77e-176">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="9c77e-177">في الشجرة، قم بتوسيع "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات\بيانات الأبعاد: قائمة السجلات".</span><span class="sxs-lookup"><span data-stu-id="9c77e-177">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="9c77e-178">في الشجرة، حدد "الجذر: عنصر XML\دفتر اليومية: عنصر XML\الحركة: عنصر XML\الأبعاد: عنصر XML"\الوصف: سمة XML".</span><span class="sxs-lookup"><span data-stu-id="9c77e-178">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="9c77e-179">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات\بيانات الأبعاد: قائمة السجلات\الوصف: سلسلة".</span><span class="sxs-lookup"><span data-stu-id="9c77e-179">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="9c77e-180">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="9c77e-180">Click Bind.</span></span>
9. <span data-ttu-id="9c77e-181">في الشجرة، حدد "الجذر: عنصر XML\دفتر اليومية: عنصر XML\الحركة: عنصر XML\الأبعاد: عنصر XML"\القيمة: سمة XML".</span><span class="sxs-lookup"><span data-stu-id="9c77e-181">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="9c77e-182">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات\بيانات الأبعاد: قائمة السجلات\الكود: سلسلة".</span><span class="sxs-lookup"><span data-stu-id="9c77e-182">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="9c77e-183">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="9c77e-183">Click Bind.</span></span>
12. <span data-ttu-id="9c77e-184">في الشجرة، حدد "الجذر: عنصر XML\دفتر اليومية: عنصر XML\الحركة: عنصر XML\الأبعاد: عنصر XML"\الكود: سمة XML".</span><span class="sxs-lookup"><span data-stu-id="9c77e-184">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="9c77e-185">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات\بيانات الأبعاد: قائمة السجلات\الاسم: سلسلة".</span><span class="sxs-lookup"><span data-stu-id="9c77e-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="9c77e-186">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="9c77e-186">Click Bind.</span></span>
15. <span data-ttu-id="9c77e-187">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات\بيانات الأبعاد: قائمة السجلات".</span><span class="sxs-lookup"><span data-stu-id="9c77e-187">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="9c77e-188">في الشجرة، حدد "الجذر: عنصر XML\دفتر اليومية: عنصر XML\الحركة: عنصر XML\الأبعاد: عنصر XML".</span><span class="sxs-lookup"><span data-stu-id="9c77e-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="9c77e-189">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="9c77e-189">Click Bind.</span></span>
18. <span data-ttu-id="9c77e-190">في الشجرة، حدد "الجذر: عنصر XML\دفتر اليومية: عنصر XML\الحركة: عنصر XML\Ct: سمة XML".</span><span class="sxs-lookup"><span data-stu-id="9c77e-190">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="9c77e-191">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات\الائتمان: حقيقي‬".</span><span class="sxs-lookup"><span data-stu-id="9c77e-191">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="9c77e-192">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="9c77e-192">Click Bind.</span></span>
21. <span data-ttu-id="9c77e-193">في الشجرة، حدد "الجذر: عنصر XML\دفتر اليومية: عنصر XML\الحركة: عنصر XML\Dt: سمة XML".</span><span class="sxs-lookup"><span data-stu-id="9c77e-193">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="9c77e-194">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات\الدين: حقيقي‬".</span><span class="sxs-lookup"><span data-stu-id="9c77e-194">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="9c77e-195">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="9c77e-195">Click Bind.</span></span>
24. <span data-ttu-id="9c77e-196">في الشجرة، حدد "الجذر: عنصر XML\دفتر اليومية: عنصر XML\الحركة: عنصر XML\العملة: سمة XML".</span><span class="sxs-lookup"><span data-stu-id="9c77e-196">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="9c77e-197">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات\العملة: سلسلة".</span><span class="sxs-lookup"><span data-stu-id="9c77e-197">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="9c77e-198">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="9c77e-198">Click Bind.</span></span>
27. <span data-ttu-id="9c77e-199">في الشجرة، حدد "الجذر: عنصر XML\دفتر اليومية: عنصر XML\الحركة: عنصر XML\التاريخ: سمة XML".</span><span class="sxs-lookup"><span data-stu-id="9c77e-199">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="9c77e-200">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات\التاريخ: التاريخ".</span><span class="sxs-lookup"><span data-stu-id="9c77e-200">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="9c77e-201">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="9c77e-201">Click Bind.</span></span>
30. <span data-ttu-id="9c77e-202">في الشجرة، حدد "الجذر: عنصر XML\دفتر اليومية: عنصر XML\الحركة: عنصر XML\الإيصال: سمة XML".</span><span class="sxs-lookup"><span data-stu-id="9c77e-202">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="9c77e-203">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات\الإيصال: سلسلة".</span><span class="sxs-lookup"><span data-stu-id="9c77e-203">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="9c77e-204">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="9c77e-204">Click Bind.</span></span>
33. <span data-ttu-id="9c77e-205">في الشجرة، حدد "الجذر: عنصر XML\دفتر اليومية: عنصر XML\الحركة: عنصر XML".</span><span class="sxs-lookup"><span data-stu-id="9c77e-205">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="9c77e-206">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات".</span><span class="sxs-lookup"><span data-stu-id="9c77e-206">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="9c77e-207">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="9c77e-207">Click Bind.</span></span>
36. <span data-ttu-id="9c77e-208">في الشجرة، حدد "الجذر: عنصر XML\دفتر اليومية: عنصر XML\الدُفعة: سمة XML".</span><span class="sxs-lookup"><span data-stu-id="9c77e-208">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="9c77e-209">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الدُفعة: سلسلة".</span><span class="sxs-lookup"><span data-stu-id="9c77e-209">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="9c77e-210">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="9c77e-210">Click Bind.</span></span>
39. <span data-ttu-id="9c77e-211">في الشجرة، حدد 'الجذر: عنصر XML\دفتر اليومية: عنصر XML'.</span><span class="sxs-lookup"><span data-stu-id="9c77e-211">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="9c77e-212">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات".</span><span class="sxs-lookup"><span data-stu-id="9c77e-212">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="9c77e-213">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="9c77e-213">Click Bind.</span></span>
42. <span data-ttu-id="9c77e-214">في الشجرة، حدد "الجذر: عنصر XML\الشركة: سمة XML".</span><span class="sxs-lookup"><span data-stu-id="9c77e-214">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="9c77e-215">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\الشركة: سلسلة".</span><span class="sxs-lookup"><span data-stu-id="9c77e-215">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="9c77e-216">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="9c77e-216">Click Bind.</span></span>
45. <span data-ttu-id="9c77e-217">انقر فوق حفظ.</span><span class="sxs-lookup"><span data-stu-id="9c77e-217">Click Save.</span></span>
46. <span data-ttu-id="9c77e-218">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9c77e-218">Close the page.</span></span>
<span data-ttu-id="9c77e-219">![صفحة مصمم عمليات التقارير الإلكترونية](../media/er-financial-dimensions-guides-format2.png)</span><span class="sxs-lookup"><span data-stu-id="9c77e-219">![ER Operations designer page](../media/er-financial-dimensions-guides-format2.png)</span></span>

