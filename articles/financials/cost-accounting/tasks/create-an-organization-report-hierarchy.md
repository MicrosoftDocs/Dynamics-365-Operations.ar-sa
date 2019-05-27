---
title: إنشاء تدرج هرمي لتقارير المنظمة
description: استخدم هذا الإجراء لإنشاء تدرج هرمي للتقرير لإعداد تقارير المؤسسة.
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9a06a67f851e4a73df90f999683d5ea27f38e66
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1543923"
---
# <a name="create-an-organization-report-hierarchy"></a><span data-ttu-id="253c9-103">إنشاء تدرج هرمي لتقارير المنظمة</span><span class="sxs-lookup"><span data-stu-id="253c9-103">Create an organization report hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="253c9-104">استخدم هذا الإجراء لإنشاء تدرج هرمي للتقرير لإعداد تقارير المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="253c9-104">Use this procedure to create a report hierarchy for organization reporting.</span></span> <span data-ttu-id="253c9-105">الغرض من هذا التسجيل هو إرشادك عبر التدرج الهرمي للأبعاد لكي تتمكن من المتابعة حتى يتم إنشاء بنية تقارير المؤسسة بأكملها.</span><span class="sxs-lookup"><span data-stu-id="253c9-105">The purpose of this recording is to guide you through the dimension hierarchy so that you can continue until the whole organization reporting structure is created.</span></span> <span data-ttu-id="253c9-106">يستخدم هذا التسجيل شركة بيانات العرض التوضيحي USP2.</span><span class="sxs-lookup"><span data-stu-id="253c9-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="253c9-107">انتقل إلى محاسبة التكاليف > الأبعاد > التدرجات الهرمية للأبعاد‬.</span><span class="sxs-lookup"><span data-stu-id="253c9-107">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="253c9-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="253c9-108">Click New.</span></span>
3. <span data-ttu-id="253c9-109">في الحقل HierarchyTypeComboBox، حدد "التدرج الهرمي لتصنيف الأبعاد‬".</span><span class="sxs-lookup"><span data-stu-id="253c9-109">In the HierarchyTypeComboBox field, select 'Dimension classification hierarchy'.</span></span>
    * <span data-ttu-id="253c9-110">حدد التدرج الهرمي لتصنيف الأبعاد‬.</span><span class="sxs-lookup"><span data-stu-id="253c9-110">Select Dimension classification hierarchy.</span></span> <span data-ttu-id="253c9-111">يُستخدم نوع ‏‫التدرج الهرمي لتصنيف البعد لتحديد القواعد ولأغراض إعداد التقارير.</span><span class="sxs-lookup"><span data-stu-id="253c9-111">The Dimension classification hierarchy type is used to define rules and for reporting purposes.</span></span> <span data-ttu-id="253c9-112">إنها تدعم كافة الأبعاد، مثل كائنات التكلفة وعناصر التكلفة والأبعاد الإحصائية.</span><span class="sxs-lookup"><span data-stu-id="253c9-112">It supports all dimensions, such as cost objects, cost elements, and statistical dimensions.</span></span>  
4. <span data-ttu-id="253c9-113">انقر فوق "إنشاء".</span><span class="sxs-lookup"><span data-stu-id="253c9-113">Click Create.</span></span>
5. <span data-ttu-id="253c9-114">في حقل "‏‫اسم التدرج الهرمي للبُعد‬‬"، اكتب "مؤسسة USP2".</span><span class="sxs-lookup"><span data-stu-id="253c9-114">In the Dimension hierarchy name field, type 'Oganization USP2'.</span></span>
6. <span data-ttu-id="253c9-115">في حقل "البعد"، أدخل أو حدد قيمة.</span><span class="sxs-lookup"><span data-stu-id="253c9-115">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="253c9-116">حدد مراكز التكلفة.</span><span class="sxs-lookup"><span data-stu-id="253c9-116">Select Cost centers.</span></span>  
7. <span data-ttu-id="253c9-117">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="253c9-117">Click Save.</span></span>
8. <span data-ttu-id="253c9-118">انقر فوق "عرض التدرج الهرمي".</span><span class="sxs-lookup"><span data-stu-id="253c9-118">Click View hierarchy.</span></span>
9. <span data-ttu-id="253c9-119">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="253c9-119">Click New.</span></span>
10. <span data-ttu-id="253c9-120">في الحقل "اسم العقدة"، اكتب "CEO".</span><span class="sxs-lookup"><span data-stu-id="253c9-120">In the Node name field, type 'CEO'.</span></span>
11. <span data-ttu-id="253c9-121">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="253c9-121">Click Save.</span></span>
12. <span data-ttu-id="253c9-122">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="253c9-122">Click New.</span></span>
13. <span data-ttu-id="253c9-123">في الحقل "اسم العقدة"، اكتب "مراكز تكلفة CEO".</span><span class="sxs-lookup"><span data-stu-id="253c9-123">In the Node name field, type 'CEO cost centers'.</span></span>
14. <span data-ttu-id="253c9-124">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="253c9-124">Click Save.</span></span>
15. <span data-ttu-id="253c9-125">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="253c9-125">Click New.</span></span>
16. <span data-ttu-id="253c9-126">في الحقل "اسم العقدة"، اكتب "المنطقة الشرقية".</span><span class="sxs-lookup"><span data-stu-id="253c9-126">In the Node name field, type 'Region East'.</span></span>
17. <span data-ttu-id="253c9-127">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="253c9-127">Click Save.</span></span>
18. <span data-ttu-id="253c9-128">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="253c9-128">Click New.</span></span>
19. <span data-ttu-id="253c9-129">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="253c9-129">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="253c9-130">في الحقل "من عضو البُعد‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="253c9-130">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="253c9-131">حدد عضو البُعد المطابق للعقدة.</span><span class="sxs-lookup"><span data-stu-id="253c9-131">Select the dimension member that corresponds to the node.</span></span>  
21. <span data-ttu-id="253c9-132">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="253c9-132">Click Save.</span></span>
22. <span data-ttu-id="253c9-133">في الشجرة، حدد "مؤسسة USP2\CEO\مراكز تكلفة CEO".</span><span class="sxs-lookup"><span data-stu-id="253c9-133">In the tree, select 'Oganization USP2\CEO\CEO cost centers'.</span></span>
23. <span data-ttu-id="253c9-134">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="253c9-134">Click New.</span></span>
24. <span data-ttu-id="253c9-135">في الحقل "اسم العقدة"، اكتب "المنطقة الغربية".</span><span class="sxs-lookup"><span data-stu-id="253c9-135">In the Node name field, type 'Region West'.</span></span>
25. <span data-ttu-id="253c9-136">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="253c9-136">Click Save.</span></span>
26. <span data-ttu-id="253c9-137">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="253c9-137">Click New.</span></span>
27. <span data-ttu-id="253c9-138">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="253c9-138">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="253c9-139">في الحقل "من عضو البُعد‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="253c9-139">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="253c9-140">حدد عضو البُعد المطابق للعقدة.</span><span class="sxs-lookup"><span data-stu-id="253c9-140">Select the dimension member that corresponds to the node.</span></span>  
29. <span data-ttu-id="253c9-141">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="253c9-141">Click Save.</span></span>
30. <span data-ttu-id="253c9-142">في الشجرة، حدد "مؤسسة USP2\CEO'.</span><span class="sxs-lookup"><span data-stu-id="253c9-142">In the tree, select 'Oganization USP2\CEO'.</span></span>
31. <span data-ttu-id="253c9-143">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="253c9-143">Click New.</span></span>
32. <span data-ttu-id="253c9-144">في الحقل "اسم العقدة"، اكتب "مراكز تكلفة CFO".</span><span class="sxs-lookup"><span data-stu-id="253c9-144">In the Node name field, type 'CFO cost centers'.</span></span>
33. <span data-ttu-id="253c9-145">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="253c9-145">Click Save.</span></span>
34. <span data-ttu-id="253c9-146">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="253c9-146">Click New.</span></span>
35. <span data-ttu-id="253c9-147">في الحقل "اسم العقدة"، اكتب "حملة ترويجية".</span><span class="sxs-lookup"><span data-stu-id="253c9-147">In the Node name field, type 'Marketing campa'.</span></span>
36. <span data-ttu-id="253c9-148">في الحقل "اسم العقدة"، اكتب "حملة ترويجية".</span><span class="sxs-lookup"><span data-stu-id="253c9-148">In the Node name field, type 'Marketing campaign'.</span></span>
37. <span data-ttu-id="253c9-149">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="253c9-149">Click Save.</span></span>
38. <span data-ttu-id="253c9-150">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="253c9-150">Click New.</span></span>
39. <span data-ttu-id="253c9-151">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="253c9-151">In the list, mark the selected row.</span></span>
40. <span data-ttu-id="253c9-152">في الحقل "من عضو البُعد‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="253c9-152">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="253c9-153">حدد عضو البُعد المطابق للعقدة.</span><span class="sxs-lookup"><span data-stu-id="253c9-153">Select the dimension member that corresponds to the node.</span></span>  
41. <span data-ttu-id="253c9-154">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="253c9-154">Click Save.</span></span>
42. <span data-ttu-id="253c9-155">في الشجرة، حدد "مؤسسة USP2‏\CEO\مراكز تكلفة CFO".</span><span class="sxs-lookup"><span data-stu-id="253c9-155">In the tree, select 'Organization USP2\CEO\CFO cost centers'.</span></span>
43. <span data-ttu-id="253c9-156">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="253c9-156">Click New.</span></span>
44. <span data-ttu-id="253c9-157">في الحقل "اسم العقدة"، اكتب "معارض تجارية".</span><span class="sxs-lookup"><span data-stu-id="253c9-157">In the Node name field, type 'Trade shows'.</span></span>
45. <span data-ttu-id="253c9-158">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="253c9-158">Click Save.</span></span>
46. <span data-ttu-id="253c9-159">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="253c9-159">Click New.</span></span>
47. <span data-ttu-id="253c9-160">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="253c9-160">In the list, mark the selected row.</span></span>
48. <span data-ttu-id="253c9-161">في الحقل "من عضو البُعد‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="253c9-161">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="253c9-162">حدد عضو البُعد المطابق للعقدة.</span><span class="sxs-lookup"><span data-stu-id="253c9-162">Select the dimension member that corresponds to the node.</span></span>  
49. <span data-ttu-id="253c9-163">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="253c9-163">Click Save.</span></span>
50. <span data-ttu-id="253c9-164">في الشجرة، حدد "مؤسسة USP2\CEO'.</span><span class="sxs-lookup"><span data-stu-id="253c9-164">In the tree, select 'Oganization USP2\CEO'.</span></span>
51. <span data-ttu-id="253c9-165">في الحقل "اسم العقدة"، اكتب "مراكز تكلفة CIO".</span><span class="sxs-lookup"><span data-stu-id="253c9-165">In the Node name field, type 'CIO cost centers'.</span></span>
52. <span data-ttu-id="253c9-166">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="253c9-166">Click Save.</span></span>
53. <span data-ttu-id="253c9-167">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="253c9-167">Click New.</span></span>
54. <span data-ttu-id="253c9-168">في الحقل "اسم العقدة"، اكتب "مراكز اتصال".</span><span class="sxs-lookup"><span data-stu-id="253c9-168">In the Node name field, type 'Call centers'.</span></span>
55. <span data-ttu-id="253c9-169">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="253c9-169">Click Save.</span></span>
56. <span data-ttu-id="253c9-170">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="253c9-170">Click New.</span></span>
57. <span data-ttu-id="253c9-171">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="253c9-171">In the list, mark the selected row.</span></span>
58. <span data-ttu-id="253c9-172">في الحقل "من عضو البُعد‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="253c9-172">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="253c9-173">حدد عضو البُعد المطابق للعقدة.</span><span class="sxs-lookup"><span data-stu-id="253c9-173">Select the dimension member that corresponds to the node.</span></span>  
59. <span data-ttu-id="253c9-174">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="253c9-174">Click Save.</span></span>

