--- 
title: "‏‫تكوين مشاركة البيانات المالية عبر الشركة‬"
description: "يوضح هذا الإجراء كيفية تكوين التعارضات وتمكينها والتحقق من صحتها وحلها عند مشاركة البيانات بين الشركات."
author: aprilolson
manager: AnnBe
ms.date: 06/22/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: margoc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 779722bd3acd10a85b089a4d30757b62293ea4e4
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="configure-financial-cross-company-data-sharing"></a><span data-ttu-id="da10a-103">‏‫تكوين مشاركة البيانات المالية عبر الشركة‬</span><span class="sxs-lookup"><span data-stu-id="da10a-103">Configure financial cross-company data sharing</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="da10a-104">يوضح هذا الإجراء كيفية تكوين التعارضات وتمكينها والتحقق من صحتها وحلها عند مشاركة البيانات بين الشركات.</span><span class="sxs-lookup"><span data-stu-id="da10a-104">This procedure shows how to configure, enable, validate, and resolve conflicts when sharing data between companies.</span></span> <span data-ttu-id="da10a-105">إنها تستخدم شركة USMF وقالب مشاركة البيانات المالية.</span><span class="sxs-lookup"><span data-stu-id="da10a-105">It uses the USMF company and the Financial data sharing template.</span></span>



<span data-ttu-id="da10a-106">يتطلب دليل المهام هذا النظام الأساسي Dynamics AX 7.1 أو أحدث.</span><span class="sxs-lookup"><span data-stu-id="da10a-106">This task guide requires Dynamics AX platform 7.1 or later.</span></span>

1. <span data-ttu-id="da10a-107">انتقل إلى إدارة النظام > مساحات العمل > إدارة البيانات.</span><span class="sxs-lookup"><span data-stu-id="da10a-107">Go to System administration > Workspaces > Data management.</span></span>
2. <span data-ttu-id="da10a-108">انقر فوق "استيراد".</span><span class="sxs-lookup"><span data-stu-id="da10a-108">Click Import.</span></span>
3. <span data-ttu-id="da10a-109">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="da10a-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="da10a-110">في الحقل تنسيق بيانات المصدر، حدد نوع الحزمة.</span><span class="sxs-lookup"><span data-stu-id="da10a-110">In the Source data format field, select the Package type.</span></span>
    * <span data-ttu-id="da10a-111">انقر فوق تحميل.</span><span class="sxs-lookup"><span data-stu-id="da10a-111">Click Upload.</span></span> <span data-ttu-id="da10a-112">انتقل إلى موقع ملف حزمة قالب المشاركة للبيانات المالية وحدد هذا الملف.</span><span class="sxs-lookup"><span data-stu-id="da10a-112">Navigate to the location of the Financial data sharing template package file and select that file.</span></span>  
5. <span data-ttu-id="da10a-113">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="da10a-113">Click Save.</span></span>
6. <span data-ttu-id="da10a-114">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="da10a-114">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="da10a-115">قم بتحديد سياسة مشاركة البيانات التي تم إنشاؤها للتو.</span><span class="sxs-lookup"><span data-stu-id="da10a-115">Select the data sharing policy that was just created.</span></span>  
7. <span data-ttu-id="da10a-116">انقر فوق "استيراد".</span><span class="sxs-lookup"><span data-stu-id="da10a-116">Click Import.</span></span>
8. <span data-ttu-id="da10a-117">انقر فوق "إغلاق".</span><span class="sxs-lookup"><span data-stu-id="da10a-117">Click Close.</span></span>
9. <span data-ttu-id="da10a-118">قم بتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="da10a-118">Refresh the page.</span></span>
10. <span data-ttu-id="da10a-119">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="da10a-119">Close the page.</span></span>
11. <span data-ttu-id="da10a-120">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="da10a-120">Close the page.</span></span>
12. <span data-ttu-id="da10a-121">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="da10a-121">Close the page.</span></span>
13. <span data-ttu-id="da10a-122">انتقل إلى إدارة النظام > إعداد > تكوين مشاركة البيانات عبر الشركات.</span><span class="sxs-lookup"><span data-stu-id="da10a-122">Go to System administration > Setup > Configure cross-company data sharing.</span></span>
14. <span data-ttu-id="da10a-123">في القائمة، ابحث عن أيام الدفع وحددها.</span><span class="sxs-lookup"><span data-stu-id="da10a-123">In the list, find and select Payment days.</span></span>
15. <span data-ttu-id="da10a-124">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="da10a-124">Click Add.</span></span>
16. <span data-ttu-id="da10a-125">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="da10a-125">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="da10a-126">في الحقل "الشركة"، اكتب "USSI".</span><span class="sxs-lookup"><span data-stu-id="da10a-126">In the Company field, type 'USSI'.</span></span>
18. <span data-ttu-id="da10a-127">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="da10a-127">Click Add.</span></span>
19. <span data-ttu-id="da10a-128">في الحقل "الشركة"، اكتب "USMF".</span><span class="sxs-lookup"><span data-stu-id="da10a-128">In the Company field, type 'USMF'.</span></span>
20. <span data-ttu-id="da10a-129">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="da10a-129">Click Save.</span></span>
21. <span data-ttu-id="da10a-130">انقر فوق "تمكين".</span><span class="sxs-lookup"><span data-stu-id="da10a-130">Click Enable.</span></span>
22. <span data-ttu-id="da10a-131">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="da10a-131">Click Yes.</span></span>
23. <span data-ttu-id="da10a-132">انقر فوق العثور على مشكلات المشاركة.</span><span class="sxs-lookup"><span data-stu-id="da10a-132">Click Find sharing issues.</span></span>
24. <span data-ttu-id="da10a-133">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="da10a-133">Click Yes.</span></span>
25. <span data-ttu-id="da10a-134">انقر فوق تحديث قيمة الحقل.</span><span class="sxs-lookup"><span data-stu-id="da10a-134">Click Update field value.</span></span>
26. <span data-ttu-id="da10a-135">انقر فوق استخدام قيمة من الشركة 1.</span><span class="sxs-lookup"><span data-stu-id="da10a-135">Click Use value from company 1.</span></span>
27. <span data-ttu-id="da10a-136">قم بتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="da10a-136">Refresh the page.</span></span>
28. <span data-ttu-id="da10a-137">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="da10a-137">Close the page.</span></span>


