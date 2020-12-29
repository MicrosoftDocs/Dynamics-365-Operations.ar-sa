---
title: إعداد دفاتر الإهلاك
description: يمر هذا الإجراء خلال عملية إنشاء دفتر إهلاك جديد وربطه بمجموعة أصول ثابتة.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 03f915fa91e0eeff2f26ab9a60bbd5118317e853
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440020"
---
# <a name="set-up-depreciation-books"></a><span data-ttu-id="d6bc5-103">إعداد دفاتر الإهلاك</span><span class="sxs-lookup"><span data-stu-id="d6bc5-103">Set up depreciation books</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d6bc5-104">يمر هذا الإجراء خلال عملية إنشاء دفتر إهلاك جديد وربطه بمجموعة أصول ثابتة.</span><span class="sxs-lookup"><span data-stu-id="d6bc5-104">This procedure walks through the process of creating a new depreciation book and associate it with a fixed asset group.</span></span> 

## <a name="create-a-depreciation-book"></a><span data-ttu-id="d6bc5-105">إنشاء دفتر إهلاك</span><span class="sxs-lookup"><span data-stu-id="d6bc5-105">Create a depreciation book</span></span>
1. <span data-ttu-id="d6bc5-106">انتقل إلى الأصول الثابتة > إعداد > دفاتر الإهلاك.</span><span class="sxs-lookup"><span data-stu-id="d6bc5-106">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="d6bc5-107">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="d6bc5-107">Click New.</span></span>
3. <span data-ttu-id="d6bc5-108">في الحقل "دفتر الإهلاك"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d6bc5-108">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="d6bc5-109">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d6bc5-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d6bc5-110">حدد خانة الاختيار "حساب الإهلاك‬" أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="d6bc5-110">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="d6bc5-111">في الحقل "ملف تعريف الإهلاك"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="d6bc5-111">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="d6bc5-112">في القائمة، ابحث عن ملف تعريف الإهلاك المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="d6bc5-112">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="d6bc5-113">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d6bc5-113">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="d6bc5-114">في الحقل "ملف تعريف الإهلاك البديل"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="d6bc5-114">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="d6bc5-115">في القائمة، حدد ملف تعريف الإهلاك المطلوب.</span><span class="sxs-lookup"><span data-stu-id="d6bc5-115">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="d6bc5-116">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d6bc5-116">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d6bc5-117">حدد ملف تعريف الإهلاك الاستثنائي‬ لاستخدامه في إهلاك إضافي لأصل ما في ظروف غير عادية.</span><span class="sxs-lookup"><span data-stu-id="d6bc5-117">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="d6bc5-118">على سبيل المثال، قد تستخدم هذا الملف لتسجيل الإهلاك الناتج عن كارثة طبيعية.</span><span class="sxs-lookup"><span data-stu-id="d6bc5-118">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="d6bc5-119">حدد خانة الاختيار "إنشاء تسويات الإهلاك التي لها تسويات أساسية‬" أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="d6bc5-119">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="d6bc5-120">في الحقل "التقويم"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="d6bc5-120">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="d6bc5-121">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d6bc5-121">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="d6bc5-122">إقران دفتر الإهلاك بمجموعة أصول ثابتة</span><span class="sxs-lookup"><span data-stu-id="d6bc5-122">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="d6bc5-123">انقر فوق "مجموعات الأصول الثابتة".</span><span class="sxs-lookup"><span data-stu-id="d6bc5-123">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="d6bc5-124">في الحقل "مجموعة الأصول الثابتة‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="d6bc5-124">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="d6bc5-125">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="d6bc5-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="d6bc5-126">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d6bc5-126">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="d6bc5-127">في الحقل "قواعد الإهلاك‬‬"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="d6bc5-127">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="d6bc5-128">في الحقل "مدة الخدمة‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="d6bc5-128">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="d6bc5-129">لاحظ أنه يتم حساب قيمة الحقل "فترات الإهلاك" بعد تعيين مدة الخدمة.</span><span class="sxs-lookup"><span data-stu-id="d6bc5-129">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  

