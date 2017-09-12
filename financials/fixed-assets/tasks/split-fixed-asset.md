--- 
title: "تقسيم أصل ثابت"
description: "سيقوم دليل المهمة هذا بتقسيم نسبة مئوية من دفتر الأصول إلى دفتر أصول جديد."
author: saraschi2
manager: AnnBe
ms.date: 10/19/2016
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
ms.openlocfilehash: b4c1b39bcae1fa3830f3a217d1ad89e84cd72134
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="2c79b-103">تقسيم أصل ثابت</span><span class="sxs-lookup"><span data-stu-id="2c79b-103">Split a fixed asset</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2c79b-104">سيقوم دليل المهمة هذا بتقسيم نسبة مئوية من دفتر الأصول إلى دفتر أصول جديد.</span><span class="sxs-lookup"><span data-stu-id="2c79b-104">This task guide will split a percentage of one asset book to a new asset book.</span></span>  <span data-ttu-id="2c79b-105">إنه يستخدم دور المحاسب وبيانات العرض التوضيحي USMF.‬</span><span class="sxs-lookup"><span data-stu-id="2c79b-105">It uses the Accountant role and USMF demo data.</span></span>


## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="2c79b-106">إنشاء أصل ثابت جديد</span><span class="sxs-lookup"><span data-stu-id="2c79b-106">Create a new fixed asset</span></span>
1. <span data-ttu-id="2c79b-107">انتقل إلى الأصول الثابتة > الأصول الثابتة > الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="2c79b-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="2c79b-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="2c79b-108">Click New.</span></span>
3. <span data-ttu-id="2c79b-109">في حقل "مجموعة الأصول الثابتة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2c79b-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="2c79b-110">لاحظ رقم الأصل الثابت لاستخدامه في عملية التقسيم لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="2c79b-110">Note the fixed asset number to use in the split process later.</span></span>
5. <span data-ttu-id="2c79b-111">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2c79b-111">In the Name field, type a value.</span></span>
6. <span data-ttu-id="2c79b-112">وقم بغلق النموذج.</span><span class="sxs-lookup"><span data-stu-id="2c79b-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="2c79b-113">تقسيم أصل ثابت</span><span class="sxs-lookup"><span data-stu-id="2c79b-113">Split a fixed asset</span></span>
1. <span data-ttu-id="2c79b-114">في القائمة، ابحث عن الأصل الثابت المراد تقسيمه وحدده.</span><span class="sxs-lookup"><span data-stu-id="2c79b-114">In the list, find and select the fixed asset to split.</span></span>
2. <span data-ttu-id="2c79b-115">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="2c79b-115">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="2c79b-116">انقر فوق "الدفاتر".</span><span class="sxs-lookup"><span data-stu-id="2c79b-116">Click Books.</span></span>
    * <span data-ttu-id="2c79b-117">حدد الدفتر لتقسيمه إلى الأصل الجديد.</span><span class="sxs-lookup"><span data-stu-id="2c79b-117">Select the book to split to the new asset.</span></span>  
4. <span data-ttu-id="2c79b-118">انقر فوق "الوظائف".</span><span class="sxs-lookup"><span data-stu-id="2c79b-118">Click Functions.</span></span>
5. <span data-ttu-id="2c79b-119">انقر فوق "تقسيم أصل ثابت‬".</span><span class="sxs-lookup"><span data-stu-id="2c79b-119">Click Split fixed asset.</span></span>
6. <span data-ttu-id="2c79b-120">في حقل "إلى الأصل الثابت‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2c79b-120">In the To fixed asset field, enter or select a value.</span></span>
7. <span data-ttu-id="2c79b-121">في الحقل "إلى دفتر‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="2c79b-121">In the To book field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="2c79b-122">في حقل "‏‫تاريخ الحركة"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="2c79b-122">In the Transaction date field, enter a date.</span></span>
9. <span data-ttu-id="2c79b-123">في الحقل "النسبة‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="2c79b-123">In the Percent field, enter a number.</span></span>
10. <span data-ttu-id="2c79b-124">في الحقل "اسم دفتر اليومية"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2c79b-124">In the Journal name field, enter or select a value.</span></span>
11. <span data-ttu-id="2c79b-125">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="2c79b-125">Click OK.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="2c79b-126">ترحيل حركة دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="2c79b-126">Post the journal transaction</span></span>
1. <span data-ttu-id="2c79b-127">انتقل إلى الأصول الثابتة > إدخالات دفتر اليومية‬ > دفتر يومية الأصول الثابتة‬.</span><span class="sxs-lookup"><span data-stu-id="2c79b-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="2c79b-128">في القائمة، حدد دفتر اليومية الذي تم إنشاؤه بواسطة عملية التقسيم.</span><span class="sxs-lookup"><span data-stu-id="2c79b-128">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="2c79b-129">انقر فوق البنود.</span><span class="sxs-lookup"><span data-stu-id="2c79b-129">Click Lines.</span></span>
    * <span data-ttu-id="2c79b-130">تحقق من بنود دفتر اليومية التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="2c79b-130">Verify the journal lines created.</span></span>  <span data-ttu-id="2c79b-131">يتم إنشاء حركة تسوية الاستحواذ للأصل الأولي لإنقاص القيمة بالنسبة المئوية المحددة أثناء عملية التقسيم.</span><span class="sxs-lookup"><span data-stu-id="2c79b-131">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>  <span data-ttu-id="2c79b-132">يتم إنشاء حركة استحواذ للأصل الجديد بالمبلغ نفسه.</span><span class="sxs-lookup"><span data-stu-id="2c79b-132">An Acquisition transaction is created for the new asset for the same amount.</span></span>  
4. <span data-ttu-id="2c79b-133">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="2c79b-133">Click Post.</span></span>


