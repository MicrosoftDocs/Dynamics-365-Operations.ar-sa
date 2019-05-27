---
title: إعداد دفاتر الإهلاك (مايو 2016)
description: سيقوم دليل المهمة هذا بإنشاء دفتر إهلاك جديد ويقرنه بمجموعة أصول ثابتة.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1fd53ea1dff9b116d19c525c5d6967ece0993b6f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566905"
---
# <a name="set-up-depreciation-books-may-2016"></a><span data-ttu-id="fb9b0-103">إعداد دفاتر الإهلاك (مايو 2016)</span><span class="sxs-lookup"><span data-stu-id="fb9b0-103">Set up depreciation books (May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fb9b0-104">سيقوم دليل المهمة هذا بإنشاء دفتر إهلاك جديد ويقرنه بمجموعة أصول ثابتة.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-104">This task guide will create a new depreciation book and associate it with a fixed asset group.</span></span>  <span data-ttu-id="fb9b0-105">إنه يستخدم دور المحاسب وبيانات العرض التوضيحي في الكيان القانوني USMF.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-depreciation-book"></a><span data-ttu-id="fb9b0-106">إنشاء دفتر إهلاك</span><span class="sxs-lookup"><span data-stu-id="fb9b0-106">Create a depreciation book</span></span>
1. <span data-ttu-id="fb9b0-107">انتقل إلى الأصول الثابتة > إعداد > دفاتر الإهلاك.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-107">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="fb9b0-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="fb9b0-108">Click New.</span></span>
3. <span data-ttu-id="fb9b0-109">في الحقل "دفتر الإهلاك"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-109">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="fb9b0-110">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="fb9b0-111">حدد خانة الاختيار "حساب الإهلاك‬" أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-111">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="fb9b0-112">في الحقل "ملف تعريف الإهلاك"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-112">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="fb9b0-113">في القائمة، ابحث عن ملف تعريف الإهلاك المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-113">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="fb9b0-114">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="fb9b0-115">في الحقل "ملف تعريف الإهلاك البديل"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-115">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="fb9b0-116">في القائمة، حدد ملف تعريف الإهلاك المطلوب.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-116">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="fb9b0-117">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-117">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="fb9b0-118">حدد ملف تعريف الإهلاك الاستثنائي‬ لاستخدامه في إهلاك إضافي لأصل ما في ظروف غير عادية.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-118">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="fb9b0-119">على سبيل المثال، قد تستخدم هذا الملف لتسجيل الإهلاك الناتج عن كارثة طبيعية.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-119">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="fb9b0-120">حدد خانة الاختيار "إنشاء تسويات الإهلاك التي لها تسويات أساسية‬" أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-120">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="fb9b0-121">في الحقل "التقويم"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-121">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="fb9b0-122">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-122">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="fb9b0-123">إقران دفتر الإهلاك بمجموعة أصول ثابتة</span><span class="sxs-lookup"><span data-stu-id="fb9b0-123">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="fb9b0-124">انقر فوق "مجموعات الأصول الثابتة".</span><span class="sxs-lookup"><span data-stu-id="fb9b0-124">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="fb9b0-125">في الحقل "مجموعة الأصول الثابتة‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-125">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="fb9b0-126">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-126">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="fb9b0-127">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-127">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="fb9b0-128">في الحقل "قواعد الإهلاك‬‬"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-128">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="fb9b0-129">في الحقل "مدة الخدمة‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-129">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="fb9b0-130">لاحظ أنه يتم حساب قيمة الحقل "فترات الإهلاك" بعد تعيين مدة الخدمة.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-130">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  

