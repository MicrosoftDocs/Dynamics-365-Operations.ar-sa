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
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 57203a7ddbacd631cbf800fb3a98e35a485cb74f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440095"
---
# <a name="create-an-organization-report-hierarchy"></a><span data-ttu-id="31c41-103">إنشاء تدرج هرمي لتقارير المنظمة</span><span class="sxs-lookup"><span data-stu-id="31c41-103">Create an organization report hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="31c41-104">استخدم هذا الإجراء لإنشاء تدرج هرمي للتقرير لإعداد تقارير المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="31c41-104">Use this procedure to create a report hierarchy for organization reporting.</span></span> <span data-ttu-id="31c41-105">الغرض من هذا التسجيل هو إرشادك عبر التدرج الهرمي للأبعاد لكي تتمكن من المتابعة حتى يتم إنشاء بنية تقارير المؤسسة بأكملها.</span><span class="sxs-lookup"><span data-stu-id="31c41-105">The purpose of this recording is to guide you through the dimension hierarchy so that you can continue until the whole organization reporting structure is created.</span></span> <span data-ttu-id="31c41-106">يستخدم هذا التسجيل شركة بيانات العرض التوضيحي USP2.</span><span class="sxs-lookup"><span data-stu-id="31c41-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="31c41-107">انتقل إلى محاسبة التكاليف > الأبعاد > التدرجات الهرمية للأبعاد‬.</span><span class="sxs-lookup"><span data-stu-id="31c41-107">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="31c41-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="31c41-108">Click New.</span></span>
3. <span data-ttu-id="31c41-109">في الحقل HierarchyTypeComboBox، حدد "التدرج الهرمي لتصنيف الأبعاد‬".</span><span class="sxs-lookup"><span data-stu-id="31c41-109">In the HierarchyTypeComboBox field, select 'Dimension classification hierarchy'.</span></span>
    * <span data-ttu-id="31c41-110">حدد التدرج الهرمي لتصنيف الأبعاد‬.</span><span class="sxs-lookup"><span data-stu-id="31c41-110">Select Dimension classification hierarchy.</span></span> <span data-ttu-id="31c41-111">يُستخدم نوع ‏‫التدرج الهرمي لتصنيف البعد لتحديد القواعد ولأغراض إعداد التقارير.</span><span class="sxs-lookup"><span data-stu-id="31c41-111">The Dimension classification hierarchy type is used to define rules and for reporting purposes.</span></span> <span data-ttu-id="31c41-112">إنها تدعم كافة الأبعاد، مثل كائنات التكلفة وعناصر التكلفة والأبعاد الإحصائية.</span><span class="sxs-lookup"><span data-stu-id="31c41-112">It supports all dimensions, such as cost objects, cost elements, and statistical dimensions.</span></span>  
4. <span data-ttu-id="31c41-113">انقر فوق "إنشاء".</span><span class="sxs-lookup"><span data-stu-id="31c41-113">Click Create.</span></span>
5. <span data-ttu-id="31c41-114">في حقل "‏‫اسم التدرج الهرمي للبُعد‬‬"، اكتب "مؤسسة USP2".</span><span class="sxs-lookup"><span data-stu-id="31c41-114">In the Dimension hierarchy name field, type 'Oganization USP2'.</span></span>
6. <span data-ttu-id="31c41-115">في حقل "البعد"، أدخل أو حدد قيمة.</span><span class="sxs-lookup"><span data-stu-id="31c41-115">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="31c41-116">حدد مراكز التكلفة.</span><span class="sxs-lookup"><span data-stu-id="31c41-116">Select Cost centers.</span></span>  
7. <span data-ttu-id="31c41-117">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="31c41-117">Click Save.</span></span>
8. <span data-ttu-id="31c41-118">انقر فوق "عرض التدرج الهرمي".</span><span class="sxs-lookup"><span data-stu-id="31c41-118">Click View hierarchy.</span></span>
9. <span data-ttu-id="31c41-119">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="31c41-119">Click New.</span></span>
10. <span data-ttu-id="31c41-120">في الحقل "اسم العقدة"، اكتب "CEO".</span><span class="sxs-lookup"><span data-stu-id="31c41-120">In the Node name field, type 'CEO'.</span></span>
11. <span data-ttu-id="31c41-121">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="31c41-121">Click Save.</span></span>
12. <span data-ttu-id="31c41-122">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="31c41-122">Click New.</span></span>
13. <span data-ttu-id="31c41-123">في الحقل "اسم العقدة"، اكتب "مراكز تكلفة CEO".</span><span class="sxs-lookup"><span data-stu-id="31c41-123">In the Node name field, type 'CEO cost centers'.</span></span>
14. <span data-ttu-id="31c41-124">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="31c41-124">Click Save.</span></span>
15. <span data-ttu-id="31c41-125">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="31c41-125">Click New.</span></span>
16. <span data-ttu-id="31c41-126">في الحقل "اسم العقدة"، اكتب "المنطقة الشرقية".</span><span class="sxs-lookup"><span data-stu-id="31c41-126">In the Node name field, type 'Region East'.</span></span>
17. <span data-ttu-id="31c41-127">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="31c41-127">Click Save.</span></span>
18. <span data-ttu-id="31c41-128">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="31c41-128">Click New.</span></span>
19. <span data-ttu-id="31c41-129">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="31c41-129">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="31c41-130">في الحقل "من عضو البُعد‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="31c41-130">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="31c41-131">حدد عضو البُعد المطابق للعقدة.</span><span class="sxs-lookup"><span data-stu-id="31c41-131">Select the dimension member that corresponds to the node.</span></span>  
21. <span data-ttu-id="31c41-132">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="31c41-132">Click Save.</span></span>
22. <span data-ttu-id="31c41-133">في الشجرة، حدد "مؤسسة USP2\CEO\مراكز تكلفة CEO".</span><span class="sxs-lookup"><span data-stu-id="31c41-133">In the tree, select 'Oganization USP2\CEO\CEO cost centers'.</span></span>
23. <span data-ttu-id="31c41-134">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="31c41-134">Click New.</span></span>
24. <span data-ttu-id="31c41-135">في الحقل "اسم العقدة"، اكتب "المنطقة الغربية".</span><span class="sxs-lookup"><span data-stu-id="31c41-135">In the Node name field, type 'Region West'.</span></span>
25. <span data-ttu-id="31c41-136">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="31c41-136">Click Save.</span></span>
26. <span data-ttu-id="31c41-137">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="31c41-137">Click New.</span></span>
27. <span data-ttu-id="31c41-138">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="31c41-138">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="31c41-139">في الحقل "من عضو البُعد‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="31c41-139">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="31c41-140">حدد عضو البُعد المطابق للعقدة.</span><span class="sxs-lookup"><span data-stu-id="31c41-140">Select the dimension member that corresponds to the node.</span></span>  
29. <span data-ttu-id="31c41-141">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="31c41-141">Click Save.</span></span>
30. <span data-ttu-id="31c41-142">في الشجرة، حدد "مؤسسة USP2\CEO'.</span><span class="sxs-lookup"><span data-stu-id="31c41-142">In the tree, select 'Oganization USP2\CEO'.</span></span>
31. <span data-ttu-id="31c41-143">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="31c41-143">Click New.</span></span>
32. <span data-ttu-id="31c41-144">في الحقل "اسم العقدة"، اكتب "مراكز تكلفة CFO".</span><span class="sxs-lookup"><span data-stu-id="31c41-144">In the Node name field, type 'CFO cost centers'.</span></span>
33. <span data-ttu-id="31c41-145">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="31c41-145">Click Save.</span></span>
34. <span data-ttu-id="31c41-146">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="31c41-146">Click New.</span></span>
35. <span data-ttu-id="31c41-147">في الحقل "اسم العقدة"، اكتب "حملة ترويجية".</span><span class="sxs-lookup"><span data-stu-id="31c41-147">In the Node name field, type 'Marketing campa'.</span></span>
36. <span data-ttu-id="31c41-148">في الحقل "اسم العقدة"، اكتب "حملة ترويجية".</span><span class="sxs-lookup"><span data-stu-id="31c41-148">In the Node name field, type 'Marketing campaign'.</span></span>
37. <span data-ttu-id="31c41-149">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="31c41-149">Click Save.</span></span>
38. <span data-ttu-id="31c41-150">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="31c41-150">Click New.</span></span>
39. <span data-ttu-id="31c41-151">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="31c41-151">In the list, mark the selected row.</span></span>
40. <span data-ttu-id="31c41-152">في الحقل "من عضو البُعد‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="31c41-152">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="31c41-153">حدد عضو البُعد المطابق للعقدة.</span><span class="sxs-lookup"><span data-stu-id="31c41-153">Select the dimension member that corresponds to the node.</span></span>  
41. <span data-ttu-id="31c41-154">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="31c41-154">Click Save.</span></span>
42. <span data-ttu-id="31c41-155">في الشجرة، حدد "مؤسسة USP2‏\CEO\مراكز تكلفة CFO".</span><span class="sxs-lookup"><span data-stu-id="31c41-155">In the tree, select 'Organization USP2\CEO\CFO cost centers'.</span></span>
43. <span data-ttu-id="31c41-156">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="31c41-156">Click New.</span></span>
44. <span data-ttu-id="31c41-157">في الحقل "اسم العقدة"، اكتب "معارض تجارية".</span><span class="sxs-lookup"><span data-stu-id="31c41-157">In the Node name field, type 'Trade shows'.</span></span>
45. <span data-ttu-id="31c41-158">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="31c41-158">Click Save.</span></span>
46. <span data-ttu-id="31c41-159">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="31c41-159">Click New.</span></span>
47. <span data-ttu-id="31c41-160">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="31c41-160">In the list, mark the selected row.</span></span>
48. <span data-ttu-id="31c41-161">في الحقل "من عضو البُعد‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="31c41-161">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="31c41-162">حدد عضو البُعد المطابق للعقدة.</span><span class="sxs-lookup"><span data-stu-id="31c41-162">Select the dimension member that corresponds to the node.</span></span>  
49. <span data-ttu-id="31c41-163">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="31c41-163">Click Save.</span></span>
50. <span data-ttu-id="31c41-164">في الشجرة، حدد "مؤسسة USP2\CEO'.</span><span class="sxs-lookup"><span data-stu-id="31c41-164">In the tree, select 'Oganization USP2\CEO'.</span></span>
51. <span data-ttu-id="31c41-165">في الحقل "اسم العقدة"، اكتب "مراكز تكلفة CIO".</span><span class="sxs-lookup"><span data-stu-id="31c41-165">In the Node name field, type 'CIO cost centers'.</span></span>
52. <span data-ttu-id="31c41-166">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="31c41-166">Click Save.</span></span>
53. <span data-ttu-id="31c41-167">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="31c41-167">Click New.</span></span>
54. <span data-ttu-id="31c41-168">في الحقل "اسم العقدة"، اكتب "مراكز اتصال".</span><span class="sxs-lookup"><span data-stu-id="31c41-168">In the Node name field, type 'Call centers'.</span></span>
55. <span data-ttu-id="31c41-169">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="31c41-169">Click Save.</span></span>
56. <span data-ttu-id="31c41-170">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="31c41-170">Click New.</span></span>
57. <span data-ttu-id="31c41-171">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="31c41-171">In the list, mark the selected row.</span></span>
58. <span data-ttu-id="31c41-172">في الحقل "من عضو البُعد‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="31c41-172">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="31c41-173">حدد عضو البُعد المطابق للعقدة.</span><span class="sxs-lookup"><span data-stu-id="31c41-173">Select the dimension member that corresponds to the node.</span></span>  
59. <span data-ttu-id="31c41-174">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="31c41-174">Click Save.</span></span>

