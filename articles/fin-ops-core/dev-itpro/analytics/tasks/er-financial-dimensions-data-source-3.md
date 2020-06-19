---
title: التقارير الإلكترونية - استخدام الأبعاد المالية كمصدر بيانات (الجزء 3 - تصميم التقرير)
description: تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين نموذج التقارير الإلكترونية لاستخدام الأبعاد المالية كمصدر بيانات للتقارير الإلكترونية.
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cef61787e50561eaac4fd52741ab5f90d9c4171d
ms.sourcegitcommit: d9125c20b21459076e4fd92fd9ebfe2e53a0431b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/27/2020
ms.locfileid: "3406487"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="df6a7-103">التقارير الإلكترونية - استخدام الأبعاد المالية كمصدر بيانات (الجزء 3 - تصميم التقرير)</span><span class="sxs-lookup"><span data-stu-id="df6a7-103">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="df6a7-104">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين نموذج التقارير الإلكترونية لاستخدام الأبعاد المالية كمصدر بيانات للتقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="df6a7-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="df6a7-105">يمكن تنفيذ هذه الخطوات في أي شركة.</span><span class="sxs-lookup"><span data-stu-id="df6a7-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="df6a7-106">لإتمام هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "التقارير الإلكترونية - استخدام الأبعاد المالية كمصدر بيانات (الجزء 2: تعيين النموذج)‬".</span><span class="sxs-lookup"><span data-stu-id="df6a7-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="df6a7-107">تصميم تقرير لتقديم الأبعاد المالية</span><span class="sxs-lookup"><span data-stu-id="df6a7-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="df6a7-108">انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.</span><span class="sxs-lookup"><span data-stu-id="df6a7-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="df6a7-109">في الشجرة، حدد "نموذج الأبعاد المالية".</span><span class="sxs-lookup"><span data-stu-id="df6a7-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="df6a7-110">انقر فوق "إنشاء تكوين" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="df6a7-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="df6a7-111">في الحقل "جديد"، أدخل 'التنسيق المستند إلى نموذج البيانات نموذج الأبعاد المالية".</span><span class="sxs-lookup"><span data-stu-id="df6a7-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="df6a7-112">استخدم النموذج الذي تم إنشاؤه مسبقًا كمصدر بيانات للتقرير الجديد.</span><span class="sxs-lookup"><span data-stu-id="df6a7-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="df6a7-113">في حقل "الاسم"، اكتب "تقرير دفتر يومية دفتر الأستاذ‬".</span><span class="sxs-lookup"><span data-stu-id="df6a7-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="df6a7-114">في الحقل "تعريف نموذج البيانات"، حدد "الإدخال".</span><span class="sxs-lookup"><span data-stu-id="df6a7-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="df6a7-115">وانقر فوق إنشاء تكوين.</span><span class="sxs-lookup"><span data-stu-id="df6a7-115">Click Create configuration.</span></span>
8. <span data-ttu-id="df6a7-116">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="df6a7-116">Click Designer.</span></span>
9. <span data-ttu-id="df6a7-117">انقر فوق "إضافة جذر" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="df6a7-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="df6a7-118">في الشجرة، حدد XML/العنصر".</span><span class="sxs-lookup"><span data-stu-id="df6a7-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="df6a7-119">في حقل "الاسم" اكتب "الجذر‬".</span><span class="sxs-lookup"><span data-stu-id="df6a7-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="df6a7-120">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="df6a7-120">Click OK.</span></span>
13. <span data-ttu-id="df6a7-121">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="df6a7-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="df6a7-122">في الشجرة، حدد "XML\سمة".</span><span class="sxs-lookup"><span data-stu-id="df6a7-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="df6a7-123">في الحقل "الاسم"، اكتب "الشركة".</span><span class="sxs-lookup"><span data-stu-id="df6a7-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="df6a7-124">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="df6a7-124">Click OK.</span></span>
17. <span data-ttu-id="df6a7-125">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="df6a7-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="df6a7-126">في الشجرة، حدد XML/العنصر".</span><span class="sxs-lookup"><span data-stu-id="df6a7-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="df6a7-127">في حقل "الاسم"، اكتب "دفتر اليومية".</span><span class="sxs-lookup"><span data-stu-id="df6a7-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="df6a7-128">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="df6a7-128">Click OK.</span></span>
21. <span data-ttu-id="df6a7-129">في الشجرة، حدد 'الجذر: عنصر XML\دفتر اليومية: عنصر XML'.</span><span class="sxs-lookup"><span data-stu-id="df6a7-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="df6a7-130">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="df6a7-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="df6a7-131">في الشجرة، حدد "XML\سمة".</span><span class="sxs-lookup"><span data-stu-id="df6a7-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="df6a7-132">في حقل "الاسم"، اكتب "الدُفعة".</span><span class="sxs-lookup"><span data-stu-id="df6a7-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="df6a7-133">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="df6a7-133">Click OK.</span></span>
26. <span data-ttu-id="df6a7-134">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="df6a7-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="df6a7-135">في الشجرة، حدد XML/العنصر".</span><span class="sxs-lookup"><span data-stu-id="df6a7-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="df6a7-136">في حقل "الاسم"، اكتب "الحركة".</span><span class="sxs-lookup"><span data-stu-id="df6a7-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="df6a7-137">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="df6a7-137">Click OK.</span></span>
30. <span data-ttu-id="df6a7-138">في الشجرة، حدد "الجذر: عنصر XML\دفتر اليومية: عنصر XML\الحركة: عنصر XML".</span><span class="sxs-lookup"><span data-stu-id="df6a7-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="df6a7-139">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="df6a7-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="df6a7-140">في الشجرة، حدد "XML\سمة".</span><span class="sxs-lookup"><span data-stu-id="df6a7-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="df6a7-141">في حقل "الاسم"، اكتب "الإيصال".</span><span class="sxs-lookup"><span data-stu-id="df6a7-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="df6a7-142">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="df6a7-142">Click OK.</span></span>
35. <span data-ttu-id="df6a7-143">انقر فوق "إضافة سمة".</span><span class="sxs-lookup"><span data-stu-id="df6a7-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="df6a7-144">في حقل "الاسم"، اكتب "التاريخ".</span><span class="sxs-lookup"><span data-stu-id="df6a7-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="df6a7-145">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="df6a7-145">Click OK.</span></span>
38. <span data-ttu-id="df6a7-146">انقر فوق "إضافة سمة".</span><span class="sxs-lookup"><span data-stu-id="df6a7-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="df6a7-147">في الحقل "الاسم"، اكتب "العملة".</span><span class="sxs-lookup"><span data-stu-id="df6a7-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="df6a7-148">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="df6a7-148">Click OK.</span></span>
41. <span data-ttu-id="df6a7-149">انقر فوق "إضافة سمة".</span><span class="sxs-lookup"><span data-stu-id="df6a7-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="df6a7-150">في حقل "الاسم"، اكتب "Dt".</span><span class="sxs-lookup"><span data-stu-id="df6a7-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="df6a7-151">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="df6a7-151">Click OK.</span></span>
44. <span data-ttu-id="df6a7-152">انقر فوق "إضافة سمة".</span><span class="sxs-lookup"><span data-stu-id="df6a7-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="df6a7-153">في حقل "الاسم"، اكتب "Ct".</span><span class="sxs-lookup"><span data-stu-id="df6a7-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="df6a7-154">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="df6a7-154">Click OK.</span></span>
47. <span data-ttu-id="df6a7-155">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="df6a7-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="df6a7-156">في الشجرة، حدد XML/العنصر".</span><span class="sxs-lookup"><span data-stu-id="df6a7-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="df6a7-157">في حقل "الاسم"، اكتب "الأبعاد".</span><span class="sxs-lookup"><span data-stu-id="df6a7-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="df6a7-158">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="df6a7-158">Click OK.</span></span>
51. <span data-ttu-id="df6a7-159">في الشجرة، حدد "الجذر: عنصر XML\دفتر اليومية: عنصر XML\الحركة: عنصر XML\الأبعاد: عنصر XML".</span><span class="sxs-lookup"><span data-stu-id="df6a7-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="df6a7-160">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="df6a7-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="df6a7-161">في الشجرة، حدد "XML\سمة".</span><span class="sxs-lookup"><span data-stu-id="df6a7-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="df6a7-162">في حقل "الاسم"، اكتب "الكود".</span><span class="sxs-lookup"><span data-stu-id="df6a7-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="df6a7-163">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="df6a7-163">Click OK.</span></span>
56. <span data-ttu-id="df6a7-164">انقر فوق "إضافة سمة".</span><span class="sxs-lookup"><span data-stu-id="df6a7-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="df6a7-165">في حقل "الاسم"، اكتب "قيمة".</span><span class="sxs-lookup"><span data-stu-id="df6a7-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="df6a7-166">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="df6a7-166">Click OK.</span></span>
59. <span data-ttu-id="df6a7-167">انقر فوق "إضافة سمة".</span><span class="sxs-lookup"><span data-stu-id="df6a7-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="df6a7-168">في حقل "الاسم"، اكتب "الوصف".</span><span class="sxs-lookup"><span data-stu-id="df6a7-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="df6a7-169">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="df6a7-169">Click OK.</span></span>
<span data-ttu-id="df6a7-170">![صفحة مصمم عمليات التقارير الإلكترونية](../media/er-financial-dimensions-guides-format1.png)</span><span class="sxs-lookup"><span data-stu-id="df6a7-170">![ER Operations designer page](../media/er-financial-dimensions-guides-format1.png)</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="df6a7-171">تعيين عناصر التقرير إلى مصادر بيانات</span><span class="sxs-lookup"><span data-stu-id="df6a7-171">Map report elements to data sources</span></span>
1. <span data-ttu-id="df6a7-172">انقر فوق علامة التبويب "التعيين".</span><span class="sxs-lookup"><span data-stu-id="df6a7-172">Click the Mapping tab.</span></span>
2. <span data-ttu-id="df6a7-173">في الشجرة، قم بتوسيع "النموذج: نموذج البيانات نموذج الأبعاد المالية".</span><span class="sxs-lookup"><span data-stu-id="df6a7-173">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="df6a7-174">في الشجرة، قم بتوسيع "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات".</span><span class="sxs-lookup"><span data-stu-id="df6a7-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="df6a7-175">في الشجرة، قم بتوسيع "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات".</span><span class="sxs-lookup"><span data-stu-id="df6a7-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="df6a7-176">في الشجرة، قم بتوسيع "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات\بيانات الأبعاد: قائمة السجلات".</span><span class="sxs-lookup"><span data-stu-id="df6a7-176">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="df6a7-177">في الشجرة، حدد "الجذر: عنصر XML\دفتر اليومية: عنصر XML\الحركة: عنصر XML\الأبعاد: عنصر XML"\الوصف: سمة XML".</span><span class="sxs-lookup"><span data-stu-id="df6a7-177">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="df6a7-178">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات\بيانات الأبعاد: قائمة السجلات\الوصف: سلسلة".</span><span class="sxs-lookup"><span data-stu-id="df6a7-178">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="df6a7-179">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="df6a7-179">Click Bind.</span></span>
9. <span data-ttu-id="df6a7-180">في الشجرة، حدد "الجذر: عنصر XML\دفتر اليومية: عنصر XML\الحركة: عنصر XML\الأبعاد: عنصر XML"\القيمة: سمة XML".</span><span class="sxs-lookup"><span data-stu-id="df6a7-180">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="df6a7-181">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات\بيانات الأبعاد: قائمة السجلات\الكود: سلسلة".</span><span class="sxs-lookup"><span data-stu-id="df6a7-181">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="df6a7-182">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="df6a7-182">Click Bind.</span></span>
12. <span data-ttu-id="df6a7-183">في الشجرة، حدد "الجذر: عنصر XML\دفتر اليومية: عنصر XML\الحركة: عنصر XML\الأبعاد: عنصر XML"\الكود: سمة XML".</span><span class="sxs-lookup"><span data-stu-id="df6a7-183">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="df6a7-184">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات\بيانات الأبعاد: قائمة السجلات\الاسم: سلسلة".</span><span class="sxs-lookup"><span data-stu-id="df6a7-184">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="df6a7-185">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="df6a7-185">Click Bind.</span></span>
15. <span data-ttu-id="df6a7-186">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات\بيانات الأبعاد: قائمة السجلات".</span><span class="sxs-lookup"><span data-stu-id="df6a7-186">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="df6a7-187">في الشجرة، حدد "الجذر: عنصر XML\دفتر اليومية: عنصر XML\الحركة: عنصر XML\الأبعاد: عنصر XML".</span><span class="sxs-lookup"><span data-stu-id="df6a7-187">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="df6a7-188">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="df6a7-188">Click Bind.</span></span>
18. <span data-ttu-id="df6a7-189">في الشجرة، حدد "الجذر: عنصر XML\دفتر اليومية: عنصر XML\الحركة: عنصر XML\Ct: سمة XML".</span><span class="sxs-lookup"><span data-stu-id="df6a7-189">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="df6a7-190">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات\الائتمان: حقيقي‬".</span><span class="sxs-lookup"><span data-stu-id="df6a7-190">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="df6a7-191">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="df6a7-191">Click Bind.</span></span>
21. <span data-ttu-id="df6a7-192">في الشجرة، حدد "الجذر: عنصر XML\دفتر اليومية: عنصر XML\الحركة: عنصر XML\Dt: سمة XML".</span><span class="sxs-lookup"><span data-stu-id="df6a7-192">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="df6a7-193">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات\الدين: حقيقي‬".</span><span class="sxs-lookup"><span data-stu-id="df6a7-193">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="df6a7-194">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="df6a7-194">Click Bind.</span></span>
24. <span data-ttu-id="df6a7-195">في الشجرة، حدد "الجذر: عنصر XML\دفتر اليومية: عنصر XML\الحركة: عنصر XML\العملة: سمة XML".</span><span class="sxs-lookup"><span data-stu-id="df6a7-195">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="df6a7-196">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات\العملة: سلسلة".</span><span class="sxs-lookup"><span data-stu-id="df6a7-196">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="df6a7-197">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="df6a7-197">Click Bind.</span></span>
27. <span data-ttu-id="df6a7-198">في الشجرة، حدد "الجذر: عنصر XML\دفتر اليومية: عنصر XML\الحركة: عنصر XML\التاريخ: سمة XML".</span><span class="sxs-lookup"><span data-stu-id="df6a7-198">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="df6a7-199">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات\التاريخ: التاريخ".</span><span class="sxs-lookup"><span data-stu-id="df6a7-199">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="df6a7-200">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="df6a7-200">Click Bind.</span></span>
30. <span data-ttu-id="df6a7-201">في الشجرة، حدد "الجذر: عنصر XML\دفتر اليومية: عنصر XML\الحركة: عنصر XML\الإيصال: سمة XML".</span><span class="sxs-lookup"><span data-stu-id="df6a7-201">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="df6a7-202">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات\الإيصال: سلسلة".</span><span class="sxs-lookup"><span data-stu-id="df6a7-202">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="df6a7-203">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="df6a7-203">Click Bind.</span></span>
33. <span data-ttu-id="df6a7-204">في الشجرة، حدد "الجذر: عنصر XML\دفتر اليومية: عنصر XML\الحركة: عنصر XML".</span><span class="sxs-lookup"><span data-stu-id="df6a7-204">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="df6a7-205">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الحركة: قائمة السجلات".</span><span class="sxs-lookup"><span data-stu-id="df6a7-205">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="df6a7-206">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="df6a7-206">Click Bind.</span></span>
36. <span data-ttu-id="df6a7-207">في الشجرة، حدد "الجذر: عنصر XML\دفتر اليومية: عنصر XML\الدُفعة: سمة XML".</span><span class="sxs-lookup"><span data-stu-id="df6a7-207">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="df6a7-208">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات\الدُفعة: سلسلة".</span><span class="sxs-lookup"><span data-stu-id="df6a7-208">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="df6a7-209">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="df6a7-209">Click Bind.</span></span>
39. <span data-ttu-id="df6a7-210">في الشجرة، حدد 'الجذر: عنصر XML\دفتر اليومية: عنصر XML'.</span><span class="sxs-lookup"><span data-stu-id="df6a7-210">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="df6a7-211">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\دفتر اليومية: قائمة السجلات".</span><span class="sxs-lookup"><span data-stu-id="df6a7-211">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="df6a7-212">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="df6a7-212">Click Bind.</span></span>
42. <span data-ttu-id="df6a7-213">في الشجرة، حدد "الجذر: عنصر XML\الشركة: سمة XML".</span><span class="sxs-lookup"><span data-stu-id="df6a7-213">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="df6a7-214">في الشجرة، حدد "النموذج: نموذج الأبعاد المالية لنموذج البيانات\الشركة: سلسلة".</span><span class="sxs-lookup"><span data-stu-id="df6a7-214">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="df6a7-215">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="df6a7-215">Click Bind.</span></span>
45. <span data-ttu-id="df6a7-216">انقر فوق حفظ.</span><span class="sxs-lookup"><span data-stu-id="df6a7-216">Click Save.</span></span>
46. <span data-ttu-id="df6a7-217">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="df6a7-217">Close the page.</span></span>
<span data-ttu-id="df6a7-218">![صفحة مصمم عمليات التقارير الإلكترونية](../media/er-financial-dimensions-guides-format2.png)</span><span class="sxs-lookup"><span data-stu-id="df6a7-218">![ER Operations designer page](../media/er-financial-dimensions-guides-format2.png)</span></span>

