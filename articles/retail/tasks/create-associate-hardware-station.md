--- 
title: "إنشاء محطات أجهزة"
description: "يتناول هذا الإجراء كيفية إنشاء محطة أجهزة جديدة."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 3551e37c6aae37c01b5cacff8b908faaf75fb3e2
ms.contentlocale: ar-sa
ms.lasthandoff: 08/08/2018

---
# <a name="create-hardware-stations"></a><span data-ttu-id="e7a40-103">إنشاء محطات أجهزة</span><span class="sxs-lookup"><span data-stu-id="e7a40-103">Create hardware stations</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="e7a40-104">يتناول هذا الإجراء كيفية إنشاء محطة أجهزة جديدة.</span><span class="sxs-lookup"><span data-stu-id="e7a40-104">This procedure walks through how to create a new hardware station.</span></span> <span data-ttu-id="e7a40-105">وسيتم إنشاء ملف تعريف لجهاز جديد واستخدامه لإضافة محطات أجهزة جديدة إلى متجر محدد مسبقًا (القناة).</span><span class="sxs-lookup"><span data-stu-id="e7a40-105">A new hardware profile will be created and used to add new hardware stations to a pre-defined store (channel).</span></span> <span data-ttu-id="e7a40-106">ويستخدم هذا الإجراء شركة USRT في بيانات العرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="e7a40-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="e7a40-107">انتقل إلى أساسيات التجارة > القنوات >...</span><span class="sxs-lookup"><span data-stu-id="e7a40-107">Go to Commerce essentials > Channels > ..</span></span> <span data-ttu-id="e7a40-108">> ..</span><span class="sxs-lookup"><span data-stu-id="e7a40-108">> ..</span></span> <span data-ttu-id="e7a40-109">> ..</span><span class="sxs-lookup"><span data-stu-id="e7a40-109">> ..</span></span> <span data-ttu-id="e7a40-110">> ملفات تعريف ‏‫محطات الأجهزة‬.</span><span class="sxs-lookup"><span data-stu-id="e7a40-110">> Hardware station profiles.</span></span>
2. <span data-ttu-id="e7a40-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="e7a40-111">Click New.</span></span>
3. <span data-ttu-id="e7a40-112">في حقل "‏‫معرف محطة الأجهزة‬"، اكتب "TestHWProfile".</span><span class="sxs-lookup"><span data-stu-id="e7a40-112">In the Hardware station ID field, type 'TestHWProfile'.</span></span>
4. <span data-ttu-id="e7a40-113">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e7a40-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="e7a40-114">في حقل "‏‫رقم المنفذ‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="e7a40-114">In the Port number field, enter a number.</span></span>
6. <span data-ttu-id="e7a40-115">في حقل "‏‫ملف تعريف الأجهزة‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e7a40-115">In the Hardware profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="e7a40-116">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e7a40-116">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="e7a40-117">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e7a40-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="e7a40-118">في حقل "‏‫اسم الحزمة‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e7a40-118">In the Package name field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="e7a40-119">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e7a40-119">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e7a40-120">هذه هي الحزمة القياسية التي تأتي مع البيئة الجديدة.</span><span class="sxs-lookup"><span data-stu-id="e7a40-120">This is the standard package that comes with a new environment.</span></span> <span data-ttu-id="e7a40-121">قد يختلف رقم الإصدار.</span><span class="sxs-lookup"><span data-stu-id="e7a40-121">The version number may vary.</span></span>  
11. <span data-ttu-id="e7a40-122">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="e7a40-122">Click Save.</span></span>
12. <span data-ttu-id="e7a40-123">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e7a40-123">Close the page.</span></span>
13. <span data-ttu-id="e7a40-124">انتقل إلى البيع بالتجزئة والتجارة > القنوات > جميع متاجر البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="e7a40-124">Go to Retail and commerce > Channels > All retail stores.</span></span>
14. <span data-ttu-id="e7a40-125">في القائمة، حدد الصف 17.</span><span class="sxs-lookup"><span data-stu-id="e7a40-125">In the list, select row 17.</span></span>
    * <span data-ttu-id="e7a40-126">إذا كنت تستخدم شركة بيانات العرض التوضيحي USRT، فهذا هو متجر هيوستن.</span><span class="sxs-lookup"><span data-stu-id="e7a40-126">If you are using the USRT demo data company, this is the Houston store.</span></span>  
15. <span data-ttu-id="e7a40-127">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e7a40-127">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="e7a40-128">قم بتبديل التوسيع لقسم ‏‫محطات الأجهزة‬.</span><span class="sxs-lookup"><span data-stu-id="e7a40-128">Toggle the expansion of the Hardware stations section.</span></span>
17. <span data-ttu-id="e7a40-129">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="e7a40-129">Click Add.</span></span>
18. <span data-ttu-id="e7a40-130">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e7a40-130">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="e7a40-131">في حقل "‏‫معرف ملف التعريف‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e7a40-131">In the Profile ID field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="e7a40-132">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e7a40-132">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e7a40-133">يجب أن يمثل هذا ملف التعريف لمحطة الأجهزة الجديدة الذي تم إنشاؤه في الخطوات السابقة.</span><span class="sxs-lookup"><span data-stu-id="e7a40-133">This must be the new hardware station profile that was created in the previous steps.</span></span>  
21. <span data-ttu-id="e7a40-134">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e7a40-134">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="e7a40-135">في حقل "اسم المضيف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e7a40-135">In the Host name field, type a value.</span></span>
23. <span data-ttu-id="e7a40-136">في حقل "‏‫معرف الوحدة الطرفية EFT‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e7a40-136">In the EFT terminal ID field, type a value.</span></span>
24. <span data-ttu-id="e7a40-137">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="e7a40-137">Click Save.</span></span>


