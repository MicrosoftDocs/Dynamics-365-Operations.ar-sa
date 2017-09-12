--- 
title: "إعداد دفاتر الإهلاك "
description: "سيقوم دليل المهمة هذا بإنشاء دفتر إهلاك جديد ويقرنه بمجموعة أصول ثابتة."
author: saraschi2
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: d2001da7b3487a07a91abd406f74558916ac9f23
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-depreciation-books"></a><span data-ttu-id="67a74-103">إعداد دفاتر الإهلاك </span><span class="sxs-lookup"><span data-stu-id="67a74-103">Set up depreciation books</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="67a74-104">سيقوم دليل المهمة هذا بإنشاء دفتر إهلاك جديد ويقرنه بمجموعة أصول ثابتة.</span><span class="sxs-lookup"><span data-stu-id="67a74-104">This task guide will create a new depreciation book and associate it with a fixed asset group.</span></span>  <span data-ttu-id="67a74-105">إنه يستخدم دور المحاسب وبيانات العرض التوضيحي في الكيان القانوني USMF.</span><span class="sxs-lookup"><span data-stu-id="67a74-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-depreciation-book"></a><span data-ttu-id="67a74-106">إنشاء دفتر إهلاك</span><span class="sxs-lookup"><span data-stu-id="67a74-106">Create a depreciation book</span></span>
1. <span data-ttu-id="67a74-107">انتقل إلى الأصول الثابتة > إعداد > دفاتر الإهلاك.</span><span class="sxs-lookup"><span data-stu-id="67a74-107">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="67a74-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="67a74-108">Click New.</span></span>
3. <span data-ttu-id="67a74-109">في الحقل "دفتر الإهلاك"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="67a74-109">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="67a74-110">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="67a74-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="67a74-111">حدد خانة الاختيار "حساب الإهلاك‬" أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="67a74-111">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="67a74-112">في الحقل "ملف تعريف الإهلاك"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="67a74-112">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="67a74-113">في القائمة، ابحث عن ملف تعريف الإهلاك المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="67a74-113">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="67a74-114">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="67a74-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="67a74-115">في الحقل "ملف تعريف الإهلاك البديل"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="67a74-115">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="67a74-116">في القائمة، حدد ملف تعريف الإهلاك المطلوب.</span><span class="sxs-lookup"><span data-stu-id="67a74-116">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="67a74-117">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="67a74-117">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="67a74-118">حدد ملف تعريف الإهلاك الاستثنائي‬ لاستخدامه في إهلاك إضافي لأصل ما في ظروف غير عادية.</span><span class="sxs-lookup"><span data-stu-id="67a74-118">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="67a74-119">على سبيل المثال، قد تستخدم هذا الملف لتسجيل الإهلاك الناتج عن كارثة طبيعية.</span><span class="sxs-lookup"><span data-stu-id="67a74-119">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="67a74-120">حدد خانة الاختيار "إنشاء تسويات الإهلاك التي لها تسويات أساسية‬" أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="67a74-120">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="67a74-121">في الحقل "التقويم"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="67a74-121">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="67a74-122">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="67a74-122">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="67a74-123">إقران دفتر الإهلاك بمجموعة أصول ثابتة</span><span class="sxs-lookup"><span data-stu-id="67a74-123">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="67a74-124">انقر فوق "مجموعات الأصول الثابتة".</span><span class="sxs-lookup"><span data-stu-id="67a74-124">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="67a74-125">في الحقل "مجموعة الأصول الثابتة‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="67a74-125">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="67a74-126">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="67a74-126">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="67a74-127">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="67a74-127">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="67a74-128">في الحقل "قواعد الإهلاك‬‬"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="67a74-128">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="67a74-129">في الحقل "مدة الخدمة‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="67a74-129">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="67a74-130">لاحظ أنه يتم حساب قيمة الحقل "فترات الإهلاك" بعد تعيين مدة الخدمة.</span><span class="sxs-lookup"><span data-stu-id="67a74-130">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  


