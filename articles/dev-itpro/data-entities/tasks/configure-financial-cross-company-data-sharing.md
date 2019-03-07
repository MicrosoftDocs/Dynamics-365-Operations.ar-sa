---
title: ‏‫تكوين مشاركة البيانات المالية عبر الشركة‬
description: يوضح هذا الإجراء كيفية تكوين التعارضات وتمكينها والتحقق من صحتها وحلها عند مشاركة البيانات بين الشركات.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportRnr, DMFExecutionHistoryWorkspace, DMFExecutionHistorySummary, DMFExecutionHistoryEntities,  SysDataSharingConfiguration, SysDataSharingDiscrepencies
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 784a925fa06148cad780b494c88b9a7af1809c9d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "357831"
---
# <a name="configure-financial-cross-company-data-sharing"></a><span data-ttu-id="ea3e2-103">‏‫تكوين مشاركة البيانات المالية عبر الشركة‬</span><span class="sxs-lookup"><span data-stu-id="ea3e2-103">Configure financial cross-company data sharing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ea3e2-104">يوضح هذا الإجراء كيفية تكوين التعارضات وتمكينها والتحقق من صحتها وحلها عند مشاركة البيانات بين الشركات.</span><span class="sxs-lookup"><span data-stu-id="ea3e2-104">This procedure shows how to configure, enable, validate, and resolve conflicts when sharing data between companies.</span></span> <span data-ttu-id="ea3e2-105">إنها تستخدم شركة USMF وقالب مشاركة البيانات المالية.</span><span class="sxs-lookup"><span data-stu-id="ea3e2-105">It uses the USMF company and the Financial data sharing template.</span></span>



<span data-ttu-id="ea3e2-106">يتطلب دليل المهام هذا الإصدار 7.1 أو أحدث من النظام الأساسي Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="ea3e2-106">This task guide requires Dynamics AX platform 7.1 or later.</span></span>

1. <span data-ttu-id="ea3e2-107">انتقل إلى إدارة النظام > مساحات العمل > إدارة البيانات.</span><span class="sxs-lookup"><span data-stu-id="ea3e2-107">Go to System administration > Workspaces > Data management.</span></span>
2. <span data-ttu-id="ea3e2-108">انقر فوق "استيراد".</span><span class="sxs-lookup"><span data-stu-id="ea3e2-108">Click Import.</span></span>
3. <span data-ttu-id="ea3e2-109">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ea3e2-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="ea3e2-110">في الحقل تنسيق بيانات المصدر، حدد نوع الحزمة.</span><span class="sxs-lookup"><span data-stu-id="ea3e2-110">In the Source data format field, select the Package type.</span></span>
    * <span data-ttu-id="ea3e2-111">انقر فوق تحميل.</span><span class="sxs-lookup"><span data-stu-id="ea3e2-111">Click Upload.</span></span> <span data-ttu-id="ea3e2-112">انتقل إلى موقع ملف حزمة قالب المشاركة للبيانات المالية وحدد هذا الملف.</span><span class="sxs-lookup"><span data-stu-id="ea3e2-112">Navigate to the location of the Financial data sharing template package file and select that file.</span></span>  
5. <span data-ttu-id="ea3e2-113">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="ea3e2-113">Click Save.</span></span>
6. <span data-ttu-id="ea3e2-114">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="ea3e2-114">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="ea3e2-115">قم بتحديد سياسة مشاركة البيانات التي تم إنشاؤها للتو.</span><span class="sxs-lookup"><span data-stu-id="ea3e2-115">Select the data sharing policy that was just created.</span></span>  
7. <span data-ttu-id="ea3e2-116">انقر فوق "استيراد".</span><span class="sxs-lookup"><span data-stu-id="ea3e2-116">Click Import.</span></span>
8. <span data-ttu-id="ea3e2-117">انقر فوق "إغلاق".</span><span class="sxs-lookup"><span data-stu-id="ea3e2-117">Click Close.</span></span>
9. <span data-ttu-id="ea3e2-118">قم بتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ea3e2-118">Refresh the page.</span></span>
10. <span data-ttu-id="ea3e2-119">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ea3e2-119">Close the page.</span></span>
11. <span data-ttu-id="ea3e2-120">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ea3e2-120">Close the page.</span></span>
12. <span data-ttu-id="ea3e2-121">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ea3e2-121">Close the page.</span></span>
13. <span data-ttu-id="ea3e2-122">انتقل إلى إدارة النظام > إعداد > تكوين مشاركة البيانات عبر الشركات.</span><span class="sxs-lookup"><span data-stu-id="ea3e2-122">Go to System administration > Setup > Configure cross-company data sharing.</span></span>
14. <span data-ttu-id="ea3e2-123">في القائمة، ابحث عن أيام الدفع وحددها.</span><span class="sxs-lookup"><span data-stu-id="ea3e2-123">In the list, find and select Payment days.</span></span>
15. <span data-ttu-id="ea3e2-124">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="ea3e2-124">Click Add.</span></span>
16. <span data-ttu-id="ea3e2-125">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="ea3e2-125">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="ea3e2-126">في الحقل "الشركة"، اكتب "USSI".</span><span class="sxs-lookup"><span data-stu-id="ea3e2-126">In the Company field, type 'USSI'.</span></span>
18. <span data-ttu-id="ea3e2-127">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="ea3e2-127">Click Add.</span></span>
19. <span data-ttu-id="ea3e2-128">في الحقل "الشركة"، اكتب "USMF".</span><span class="sxs-lookup"><span data-stu-id="ea3e2-128">In the Company field, type 'USMF'.</span></span>
20. <span data-ttu-id="ea3e2-129">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="ea3e2-129">Click Save.</span></span>
21. <span data-ttu-id="ea3e2-130">انقر فوق "تمكين".</span><span class="sxs-lookup"><span data-stu-id="ea3e2-130">Click Enable.</span></span>
22. <span data-ttu-id="ea3e2-131">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="ea3e2-131">Click Yes.</span></span>
23. <span data-ttu-id="ea3e2-132">انقر فوق العثور على مشكلات المشاركة.</span><span class="sxs-lookup"><span data-stu-id="ea3e2-132">Click Find sharing issues.</span></span>
24. <span data-ttu-id="ea3e2-133">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="ea3e2-133">Click Yes.</span></span>
25. <span data-ttu-id="ea3e2-134">انقر فوق تحديث قيمة الحقل.</span><span class="sxs-lookup"><span data-stu-id="ea3e2-134">Click Update field value.</span></span>
26. <span data-ttu-id="ea3e2-135">انقر فوق استخدام قيمة من الشركة 1.</span><span class="sxs-lookup"><span data-stu-id="ea3e2-135">Click Use value from company 1.</span></span>
27. <span data-ttu-id="ea3e2-136">قم بتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ea3e2-136">Refresh the page.</span></span>
28. <span data-ttu-id="ea3e2-137">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ea3e2-137">Close the page.</span></span>

