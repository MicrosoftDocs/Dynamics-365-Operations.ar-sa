--- 
title: "إنشاء قنوات مركز الاتصال وتحديد سمات القنوات"
description: "ينقلك هذا الإجراء عبر إنشاء قناة جديدة للبيع بالتجزئة وتحديد سمات القناة."
author: mugunthanm
manager: AnnBe
ms.date: 05/22/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 7ef094535214ecf4c65f95c36a93455446d7e388
ms.contentlocale: ar-sa
ms.lasthandoff: 08/08/2018

---
# <a name="create-call-center-channels-and-define-channel-attributes"></a><span data-ttu-id="5a9b9-103">إنشاء قنوات مركز الاتصال وتحديد سمات القنوات</span><span class="sxs-lookup"><span data-stu-id="5a9b9-103">Create call center channels and define channel attributes</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="5a9b9-104">ينقلك هذا الإجراء عبر إنشاء قناة جديدة للبيع بالتجزئة وتحديد سمات القناة.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-104">This procedure walks through creating a new retail channel and defining channel attributes.</span></span> <span data-ttu-id="5a9b9-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USRT.‬</span><span class="sxs-lookup"><span data-stu-id="5a9b9-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="5a9b9-106">هذا الإجراء مخصص لدور تكنولوجيا معلومات Retail‬.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-106">This procedure is intended for the Retail IT role.</span></span>


## <a name="create-new-store"></a><span data-ttu-id="5a9b9-107">إنشاء متجر جديد</span><span class="sxs-lookup"><span data-stu-id="5a9b9-107">Create new store</span></span>
1. <span data-ttu-id="5a9b9-108">انتقل إلى كافة مساحات العمل > توزيع القنوات.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-108">Go to All workspaces > Channel deployment.</span></span>
2. <span data-ttu-id="5a9b9-109">انقر فوق "قناة جديدة".</span><span class="sxs-lookup"><span data-stu-id="5a9b9-109">Click New channel.</span></span>
3. <span data-ttu-id="5a9b9-110">انقر فوق "المتجر".</span><span class="sxs-lookup"><span data-stu-id="5a9b9-110">Click Store.</span></span>
4. <span data-ttu-id="5a9b9-111">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="5a9b9-112">في حقل "رقم المتجر"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-112">In the Store number field, type a value.</span></span>
6. <span data-ttu-id="5a9b9-113">في الحقل "المستودع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-113">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="5a9b9-114">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-114">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="5a9b9-115">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="5a9b9-116">في حقل "‏‫المنطقة الزمنية للمتجر‬"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-116">In the Store time zone field, select an option.</span></span>
10. <span data-ttu-id="5a9b9-117">في الحقل "ملف تعريف القناة‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-117">In the Channel profile field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="5a9b9-118">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="5a9b9-119">في الحقل "اللغة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-119">In the Language field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="5a9b9-120">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="5a9b9-121">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-121">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="5a9b9-122">في الحقل "مجموعة ضريبة المبيعات"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-122">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="5a9b9-123">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-123">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="5a9b9-124">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-124">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="5a9b9-125">في حقل "دفتر عناوين العميل"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-125">In the Customer address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="5a9b9-126">حدد دفتر العناوين المستخدم لربط العملاء بهذا المتجر.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-126">Select the address book used to link customers to this store.</span></span>  
19. <span data-ttu-id="5a9b9-127">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-127">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="5a9b9-128">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-128">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="5a9b9-129">انقر فوق تحديد.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-129">Click Select.</span></span>
22. <span data-ttu-id="5a9b9-130">في حقل "دفتر عناوين الموظفين"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-130">In the Employee address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="5a9b9-131">حدد دفتر العناوين المستخدم لربط موظفي الكاشير بهذا المتجر.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-131">Select the address book used to link cashiers to this channel.</span></span>  
23. <span data-ttu-id="5a9b9-132">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-132">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="5a9b9-133">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-133">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="5a9b9-134">انقر فوق تحديد.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-134">Click Select.</span></span>
26. <span data-ttu-id="5a9b9-135">في حقل "‏‫العميل الافتراضي"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-135">In the Default customer field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="5a9b9-136">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-136">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="5a9b9-137">قم بتوسيع أو طي مقطع "تخطيط الشاشة".</span><span class="sxs-lookup"><span data-stu-id="5a9b9-137">Expand or collapse the Screen layout section.</span></span>
29. <span data-ttu-id="5a9b9-138">في الحقل "معرف تخطيط الشاشة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-138">In the Screen layout ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="5a9b9-139">حدد شاشة نقطة البيع الافتراضية لهذا المتجر.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-139">Select the default POS screen layout for this store.</span></span>  
30. <span data-ttu-id="5a9b9-140">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-140">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="5a9b9-141">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="5a9b9-142">في جزء الإجراءات، انقر فوق "إعداد".</span><span class="sxs-lookup"><span data-stu-id="5a9b9-142">On the Action Pane, click Set up.</span></span>
33. <span data-ttu-id="5a9b9-143">انقر فوق "سمات القناة".</span><span class="sxs-lookup"><span data-stu-id="5a9b9-143">Click Channel attributes.</span></span>
34. <span data-ttu-id="5a9b9-144">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="5a9b9-144">Click New.</span></span>
35. <span data-ttu-id="5a9b9-145">في الحقل "الاسم"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-145">In the Name field, click the drop-down button to open the lookup.</span></span>
36. <span data-ttu-id="5a9b9-146">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-146">In the list, find and select the desired record.</span></span>
37. <span data-ttu-id="5a9b9-147">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-147">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="5a9b9-148">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="5a9b9-148">Click Save.</span></span>
39. <span data-ttu-id="5a9b9-149">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-149">Close the page.</span></span>
40. <span data-ttu-id="5a9b9-150">في جزء الإجراءات، انقر فوق "إعداد".</span><span class="sxs-lookup"><span data-stu-id="5a9b9-150">On the Action Pane, click Set up.</span></span>
41. <span data-ttu-id="5a9b9-151">انقر فوق طرق الدفع.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-151">Click Payment methods.</span></span>
42. <span data-ttu-id="5a9b9-152">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="5a9b9-152">Click New.</span></span>
43. <span data-ttu-id="5a9b9-153">في الحقل "طريقة الدفع‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-153">In the Payment method field, click the drop-down button to open the lookup.</span></span>
44. <span data-ttu-id="5a9b9-154">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-154">In the list, click the link in the selected row.</span></span>
45. <span data-ttu-id="5a9b9-155">قم بتوسيع قسم الترحيل أو طيه.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-155">Expand or collapse the Posting section.</span></span>
46. <span data-ttu-id="5a9b9-156">في حقل "‏‫رقم الحساب"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-156">In the Account number field, specify the desired values.</span></span>
47. <span data-ttu-id="5a9b9-157">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="5a9b9-157">Click Save.</span></span>
48. <span data-ttu-id="5a9b9-158">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-158">Close the page.</span></span>
49. <span data-ttu-id="5a9b9-159">في جزء الإجراءات، انقر فوق "إعداد".</span><span class="sxs-lookup"><span data-stu-id="5a9b9-159">On the Action Pane, click Set up.</span></span>
50. <span data-ttu-id="5a9b9-160">انقر فوق "إقرار النقدية".</span><span class="sxs-lookup"><span data-stu-id="5a9b9-160">Click Cash declaration.</span></span>
51. <span data-ttu-id="5a9b9-161">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="5a9b9-161">Click New.</span></span>
52. <span data-ttu-id="5a9b9-162">في الحقل "المبلغ بعملة الحركة‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-162">In the Amount in transaction currency field, enter a number.</span></span>
53. <span data-ttu-id="5a9b9-163">في الحقل "العملة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-163">In the Currency field, click the drop-down button to open the lookup.</span></span>
54. <span data-ttu-id="5a9b9-164">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-164">In the list, find and select the desired record.</span></span>
55. <span data-ttu-id="5a9b9-165">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-165">In the list, click the link in the selected row.</span></span>
56. <span data-ttu-id="5a9b9-166">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="5a9b9-166">Click Save.</span></span>
57. <span data-ttu-id="5a9b9-167">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-167">Close the page.</span></span>
58. <span data-ttu-id="5a9b9-168">في جزء الإجراءات، انقر فوق "إعداد".</span><span class="sxs-lookup"><span data-stu-id="5a9b9-168">On the Action Pane, click Set up.</span></span>
59. <span data-ttu-id="5a9b9-169">انقر فوق "تعيين مجموعة محددات مواقع المتجر‬".</span><span class="sxs-lookup"><span data-stu-id="5a9b9-169">Click Store locator group assignment.</span></span>
60. <span data-ttu-id="5a9b9-170">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="5a9b9-170">Click New.</span></span>
61. <span data-ttu-id="5a9b9-171">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-171">In the list, mark the selected row.</span></span>
62. <span data-ttu-id="5a9b9-172">في الحقل "مجموعة محدد المواقع‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-172">In the Locator group field, click the drop-down button to open the lookup.</span></span>
63. <span data-ttu-id="5a9b9-173">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-173">In the list, find and select the desired record.</span></span>
64. <span data-ttu-id="5a9b9-174">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-174">In the list, click the link in the selected row.</span></span>
65. <span data-ttu-id="5a9b9-175">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="5a9b9-175">Click Save.</span></span>
66. <span data-ttu-id="5a9b9-176">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-176">Close the page.</span></span>


