---
title: إنشاء قنوات مراكز الاتصال وتحديد سمات القناة
description: ينقلك هذا الإجراء عبر إنشاء قناة جديدة وتحديد سمات القناة.
author: mugunthanm
manager: AnnBe
ms.date: 05/22/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a2f99029195a8b783f0d12990d4e8bab0bb348d7
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140916"
---
# <a name="create-call-center-channels-and-define-channel-attributes"></a><span data-ttu-id="e108c-103">إنشاء قنوات مراكز الاتصال وتحديد سمات القناة</span><span class="sxs-lookup"><span data-stu-id="e108c-103">Create call center channels and define channel attributes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e108c-104">يتناول هذا الإجراء إنشاء قناة تجارية جديدة وتحديد سمات القناة.</span><span class="sxs-lookup"><span data-stu-id="e108c-104">This procedure walks through creating a new commerce channel and defining channel attributes.</span></span> <span data-ttu-id="e108c-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USRT.‬</span><span class="sxs-lookup"><span data-stu-id="e108c-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="e108c-106">هذا الإجراء مخصص لدور تكنولوجيا معلومات التجارة.</span><span class="sxs-lookup"><span data-stu-id="e108c-106">This procedure is intended for the Commerce IT role.</span></span>


## <a name="create-new-store"></a><span data-ttu-id="e108c-107">إنشاء متجر جديد</span><span class="sxs-lookup"><span data-stu-id="e108c-107">Create new store</span></span>
1. <span data-ttu-id="e108c-108">انتقل إلى كافة مساحات العمل > توزيع القنوات.</span><span class="sxs-lookup"><span data-stu-id="e108c-108">Go to All workspaces > Channel deployment.</span></span>
2. <span data-ttu-id="e108c-109">انقر فوق "قناة جديدة".</span><span class="sxs-lookup"><span data-stu-id="e108c-109">Click New channel.</span></span>
3. <span data-ttu-id="e108c-110">انقر فوق "المتجر".</span><span class="sxs-lookup"><span data-stu-id="e108c-110">Click Store.</span></span>
4. <span data-ttu-id="e108c-111">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e108c-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="e108c-112">في حقل "رقم المتجر"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e108c-112">In the Store number field, type a value.</span></span>
6. <span data-ttu-id="e108c-113">في الحقل "المستودع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e108c-113">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="e108c-114">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e108c-114">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="e108c-115">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e108c-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="e108c-116">في حقل "‏‫المنطقة الزمنية للمتجر‬"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="e108c-116">In the Store time zone field, select an option.</span></span>
10. <span data-ttu-id="e108c-117">في الحقل "ملف تعريف القناة‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e108c-117">In the Channel profile field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="e108c-118">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e108c-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="e108c-119">في الحقل "اللغة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e108c-119">In the Language field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="e108c-120">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e108c-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="e108c-121">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e108c-121">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="e108c-122">في الحقل "مجموعة ضريبة المبيعات"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e108c-122">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="e108c-123">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e108c-123">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="e108c-124">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e108c-124">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="e108c-125">في حقل "دفتر عناوين العميل"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e108c-125">In the Customer address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="e108c-126">حدد دفتر العناوين المستخدم لربط العملاء بهذا المتجر.</span><span class="sxs-lookup"><span data-stu-id="e108c-126">Select the address book used to link customers to this store.</span></span>  
19. <span data-ttu-id="e108c-127">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e108c-127">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="e108c-128">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e108c-128">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="e108c-129">انقر فوق تحديد.</span><span class="sxs-lookup"><span data-stu-id="e108c-129">Click Select.</span></span>
22. <span data-ttu-id="e108c-130">في حقل "دفتر عناوين الموظفين"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e108c-130">In the Employee address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="e108c-131">حدد دفتر العناوين المستخدم لربط موظفي الكاشير بهذا المتجر.</span><span class="sxs-lookup"><span data-stu-id="e108c-131">Select the address book used to link cashiers to this channel.</span></span>  
23. <span data-ttu-id="e108c-132">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e108c-132">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="e108c-133">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e108c-133">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="e108c-134">انقر فوق تحديد.</span><span class="sxs-lookup"><span data-stu-id="e108c-134">Click Select.</span></span>
26. <span data-ttu-id="e108c-135">في حقل "‏‫العميل الافتراضي"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e108c-135">In the Default customer field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="e108c-136">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e108c-136">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="e108c-137">قم بتوسيع أو طي مقطع "تخطيط الشاشة".</span><span class="sxs-lookup"><span data-stu-id="e108c-137">Expand or collapse the Screen layout section.</span></span>
29. <span data-ttu-id="e108c-138">في الحقل "معرف تخطيط الشاشة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e108c-138">In the Screen layout ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="e108c-139">حدد شاشة نقطة البيع الافتراضية لهذا المتجر.</span><span class="sxs-lookup"><span data-stu-id="e108c-139">Select the default POS screen layout for this store.</span></span>  
30. <span data-ttu-id="e108c-140">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e108c-140">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="e108c-141">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e108c-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="e108c-142">في جزء الإجراءات، انقر فوق "إعداد".</span><span class="sxs-lookup"><span data-stu-id="e108c-142">On the Action Pane, click Set up.</span></span>
33. <span data-ttu-id="e108c-143">انقر فوق "سمات القناة".</span><span class="sxs-lookup"><span data-stu-id="e108c-143">Click Channel attributes.</span></span>
34. <span data-ttu-id="e108c-144">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="e108c-144">Click New.</span></span>
35. <span data-ttu-id="e108c-145">في الحقل "الاسم"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e108c-145">In the Name field, click the drop-down button to open the lookup.</span></span>
36. <span data-ttu-id="e108c-146">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e108c-146">In the list, find and select the desired record.</span></span>
37. <span data-ttu-id="e108c-147">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e108c-147">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="e108c-148">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="e108c-148">Click Save.</span></span>
39. <span data-ttu-id="e108c-149">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e108c-149">Close the page.</span></span>
40. <span data-ttu-id="e108c-150">في جزء الإجراءات، انقر فوق "إعداد".</span><span class="sxs-lookup"><span data-stu-id="e108c-150">On the Action Pane, click Set up.</span></span>
41. <span data-ttu-id="e108c-151">انقر فوق طرق الدفع.</span><span class="sxs-lookup"><span data-stu-id="e108c-151">Click Payment methods.</span></span>
42. <span data-ttu-id="e108c-152">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="e108c-152">Click New.</span></span>
43. <span data-ttu-id="e108c-153">في الحقل "طريقة الدفع‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e108c-153">In the Payment method field, click the drop-down button to open the lookup.</span></span>
44. <span data-ttu-id="e108c-154">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e108c-154">In the list, click the link in the selected row.</span></span>
45. <span data-ttu-id="e108c-155">قم بتوسيع قسم الترحيل أو طيه.</span><span class="sxs-lookup"><span data-stu-id="e108c-155">Expand or collapse the Posting section.</span></span>
46. <span data-ttu-id="e108c-156">في حقل "‏‫رقم الحساب"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="e108c-156">In the Account number field, specify the desired values.</span></span>
47. <span data-ttu-id="e108c-157">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="e108c-157">Click Save.</span></span>
48. <span data-ttu-id="e108c-158">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e108c-158">Close the page.</span></span>
49. <span data-ttu-id="e108c-159">في جزء الإجراءات، انقر فوق "إعداد".</span><span class="sxs-lookup"><span data-stu-id="e108c-159">On the Action Pane, click Set up.</span></span>
50. <span data-ttu-id="e108c-160">انقر فوق "إقرار النقدية".</span><span class="sxs-lookup"><span data-stu-id="e108c-160">Click Cash declaration.</span></span>
51. <span data-ttu-id="e108c-161">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="e108c-161">Click New.</span></span>
52. <span data-ttu-id="e108c-162">في الحقل "المبلغ بعملة الحركة‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="e108c-162">In the Amount in transaction currency field, enter a number.</span></span>
53. <span data-ttu-id="e108c-163">في الحقل "العملة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e108c-163">In the Currency field, click the drop-down button to open the lookup.</span></span>
54. <span data-ttu-id="e108c-164">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e108c-164">In the list, find and select the desired record.</span></span>
55. <span data-ttu-id="e108c-165">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e108c-165">In the list, click the link in the selected row.</span></span>
56. <span data-ttu-id="e108c-166">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="e108c-166">Click Save.</span></span>
57. <span data-ttu-id="e108c-167">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e108c-167">Close the page.</span></span>
58. <span data-ttu-id="e108c-168">في جزء الإجراءات، انقر فوق "إعداد".</span><span class="sxs-lookup"><span data-stu-id="e108c-168">On the Action Pane, click Set up.</span></span>
59. <span data-ttu-id="e108c-169">انقر فوق "تعيين مجموعة محددات مواقع المتجر‬".</span><span class="sxs-lookup"><span data-stu-id="e108c-169">Click Store locator group assignment.</span></span>
60. <span data-ttu-id="e108c-170">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="e108c-170">Click New.</span></span>
61. <span data-ttu-id="e108c-171">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e108c-171">In the list, mark the selected row.</span></span>
62. <span data-ttu-id="e108c-172">في الحقل "مجموعة محدد المواقع‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e108c-172">In the Locator group field, click the drop-down button to open the lookup.</span></span>
63. <span data-ttu-id="e108c-173">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e108c-173">In the list, find and select the desired record.</span></span>
64. <span data-ttu-id="e108c-174">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e108c-174">In the list, click the link in the selected row.</span></span>
65. <span data-ttu-id="e108c-175">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="e108c-175">Click Save.</span></span>
66. <span data-ttu-id="e108c-176">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e108c-176">Close the page.</span></span>

