--- 
title: "معالجة خطابات التحصيل"
description: "يوضح هذا الإجراء كيفية إنشاء وطباعة وترحيل خطابات التحصيل."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPosting, SysQueryForm, CustCollectionLetterNote
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: a1bdf9528b52daa7bb719ea5a751a01e56a8c963
ms.contentlocale: ar-sa
ms.lasthandoff: 09/14/2018

---
# <a name="process-collection-letters"></a><span data-ttu-id="52992-103">معالجة خطابات التحصيل</span><span class="sxs-lookup"><span data-stu-id="52992-103">Process collection letters</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="52992-104">يوضح هذا الإجراء كيفية إنشاء وطباعة وترحيل خطابات التحصيل.</span><span class="sxs-lookup"><span data-stu-id="52992-104">This procedure shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="52992-105">تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="52992-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="52992-106">إعداد تسلسل خطاب تحصيل بملف تعريف الترحيل</span><span class="sxs-lookup"><span data-stu-id="52992-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="52992-107">انتقل إلى التحصيلات والائتمان‬ > إعداد > ملفات تعريف ترحيل العميل‬.</span><span class="sxs-lookup"><span data-stu-id="52992-107">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
2. <span data-ttu-id="52992-108">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="52992-108">Click Edit.</span></span>
    * <span data-ttu-id="52992-109">حدد تسلسل خطاب التحصيل من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="52992-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="52992-110">إذا كنت لا تريد إنشاء خطابات تحصيل للحركات باستخدام ملف تعريف الترحيل هذا، فاترك الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="52992-110">If you do not want generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
    * <span data-ttu-id="52992-111">تسمح لك علامة التبويب "‏‫تقييدات الجداول"‬ بتغيير الطريقة التي تتم بها معالجة خطابات التحصيل.</span><span class="sxs-lookup"><span data-stu-id="52992-111">The table restriction tab allows you to change the way that collection letters are processed.</span></span> <span data-ttu-id="52992-112">إذا تم تعيين هذا الحقل إلى "نعم"، فسيتم إنشاء خطابات التحصيل لملف تعريف الترحيل هذا.</span><span class="sxs-lookup"><span data-stu-id="52992-112">If this field is set to Yes, then collection letters will be created for this posting profile.</span></span>  
3. <span data-ttu-id="52992-113">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="52992-113">Close the page.</span></span>

## <a name="create-collection-letters"></a><span data-ttu-id="52992-114">إنشاء خطابات تحصيل</span><span class="sxs-lookup"><span data-stu-id="52992-114">Create collection letters</span></span>
1. <span data-ttu-id="52992-115">انتقل إلى الائتمان والتحصيلات‬ > خطاب التحصيل > إنشاء خطابات التحصيل.</span><span class="sxs-lookup"><span data-stu-id="52992-115">Go to Credit and collections > Collection letter > Create collection letters.</span></span>
    * <span data-ttu-id="52992-116">يجب تحديد أنواع الحركات التي سيتم تحصيل الخطابات لها.</span><span class="sxs-lookup"><span data-stu-id="52992-116">You must select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="52992-117">سيتم تضمين كافة الحركات المفتوحة لهذه الأنواع في الحساب.</span><span class="sxs-lookup"><span data-stu-id="52992-117">All of the open transactions for these types will be included in the calculation.</span></span>  
2. <span data-ttu-id="52992-118">حدد خيارًا في حقل "خطاب التحصيل‬".</span><span class="sxs-lookup"><span data-stu-id="52992-118">In the Collection letter field, select an option.</span></span>
3. <span data-ttu-id="52992-119">أدخل تاريخ خطاب التحصيل.</span><span class="sxs-lookup"><span data-stu-id="52992-119">Enter the date of the collection letter.</span></span>
    * <span data-ttu-id="52992-120">هناك اثنين من خيارات ملف تعريف الترحيل:   الحساب – استخدم ملف تعريف الترحيل الذي تم تعيينه إلى حساب العميل لكل إشعار فائدة.</span><span class="sxs-lookup"><span data-stu-id="52992-120">There are two posting profile options:   Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   <span data-ttu-id="52992-121">تحديد – استخدم ملف تعريف الترحيل الذي تحدده في الحقل "ملف تعريف الترحيل".</span><span class="sxs-lookup"><span data-stu-id="52992-121">Select – Use the posting profile that you select in the Posting profile field.</span></span>  
    * <span data-ttu-id="52992-122">حدد ملف تعريف ترحيل إذا قمت بتغيير "استخدام ملف تعريف الترحيل من" إلى "تحديد".</span><span class="sxs-lookup"><span data-stu-id="52992-122">Select a posting profile if you changed "Use posting profile from" to "Select".</span></span>  
4. <span data-ttu-id="52992-123">وسّع المقطع "السجلات المطلوب تضمينها‬".</span><span class="sxs-lookup"><span data-stu-id="52992-123">Expand the Records to include section.</span></span>
5. <span data-ttu-id="52992-124">انقر فوق "عامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="52992-124">Click Filter.</span></span>
6. <span data-ttu-id="52992-125">في حقل "المعايير"، أدخل "معرف العميل".</span><span class="sxs-lookup"><span data-stu-id="52992-125">In the Criteria field, In the Criteria field, enter a Customer ID.</span></span> <span data-ttu-id="52992-126">على سبيل المثال، أدخل "US-001".</span><span class="sxs-lookup"><span data-stu-id="52992-126">For example, enter 'US-001'..</span></span>
7. <span data-ttu-id="52992-127">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="52992-127">Click OK.</span></span>
8. <span data-ttu-id="52992-128">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="52992-128">Click OK.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="52992-129">طباعة خطابات التحصيل</span><span class="sxs-lookup"><span data-stu-id="52992-129">Print collection letters</span></span>
1. <span data-ttu-id="52992-130">انتقل إلى ‏‫الائتمان والتحصيلات > خطاب التحصيل > ‏‫مراجعة خطابات التحصيل ومعالجتها‬.</span><span class="sxs-lookup"><span data-stu-id="52992-130">Go to Credit and collections > Collection letter > Review and process collection letters.</span></span>
2. <span data-ttu-id="52992-131">في الحقل "الحالة"، حدد "‏‫تم الإنشاء".</span><span class="sxs-lookup"><span data-stu-id="52992-131">In the Status field, select 'Created'.</span></span>
3. <span data-ttu-id="52992-132">في حقل "الطابعة"، حدد "عدم الطباعة".</span><span class="sxs-lookup"><span data-stu-id="52992-132">In the Printed field, select 'Not printed'.</span></span>
4. <span data-ttu-id="52992-133">انقر فوق طباعة.</span><span class="sxs-lookup"><span data-stu-id="52992-133">Click Print.</span></span>
5. <span data-ttu-id="52992-134">انقر فوق إشعار خطاب التحصيل.</span><span class="sxs-lookup"><span data-stu-id="52992-134">Click Collection letter note.</span></span>
6. <span data-ttu-id="52992-135">وسّع المقطع "السجلات المطلوب تضمينها‬".</span><span class="sxs-lookup"><span data-stu-id="52992-135">Expand the Records to include section.</span></span>
7. <span data-ttu-id="52992-136">أدخل تاريخ الإيقاف للترحيلات.</span><span class="sxs-lookup"><span data-stu-id="52992-136">Enter the cutoff date for postings</span></span>
8. <span data-ttu-id="52992-137">انقر فوق "موافق" لطباعة خطاب التحصيل.</span><span class="sxs-lookup"><span data-stu-id="52992-137">Click OK to print the collection letter.</span></span>

## <a name="post-the-collection-letter"></a><span data-ttu-id="52992-138">ترحيل خطاب التحصيل</span><span class="sxs-lookup"><span data-stu-id="52992-138">Post the collection letter</span></span>
1. <span data-ttu-id="52992-139">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="52992-139">Click Post.</span></span>
2. <span data-ttu-id="52992-140">أدخل تاريخ الترحيل لخطاب التحصيل.</span><span class="sxs-lookup"><span data-stu-id="52992-140">Enter the posting date for the collection letter.</span></span>
3. <span data-ttu-id="52992-141">وسّع المقطع "السجلات المطلوب تضمينها‬".</span><span class="sxs-lookup"><span data-stu-id="52992-141">Expand the Records to include section.</span></span>
4. <span data-ttu-id="52992-142">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="52992-142">Click OK.</span></span>
5. <span data-ttu-id="52992-143">في الحقل "الحالة"، حدد "‏‫مرحل‬".</span><span class="sxs-lookup"><span data-stu-id="52992-143">In the Status field, select 'Posted'.</span></span>
6. <span data-ttu-id="52992-144">في حقل "مطبوع"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="52992-144">In the Printed field, select an option.</span></span>


