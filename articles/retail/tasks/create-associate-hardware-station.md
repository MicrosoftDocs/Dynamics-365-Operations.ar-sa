---
title: " إنشاء وربط محطة أجهزة"
description: يتناول هذا الإجراء كيفية إنشاء محطة أجهزة جديدة.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailHardwareStation, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 80df4fa663d208e28f5c9b031b6610d29286171c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1548383"
---
# <a name="create-and-associate-a-hardware-station"></a><span data-ttu-id="1ac1b-103"> إنشاء وربط محطة أجهزة</span><span class="sxs-lookup"><span data-stu-id="1ac1b-103">Create and associate a hardware station</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="1ac1b-104">يتناول هذا الإجراء كيفية إنشاء محطة أجهزة جديدة.</span><span class="sxs-lookup"><span data-stu-id="1ac1b-104">This procedure walks through how to create a new hardware station.</span></span> <span data-ttu-id="1ac1b-105">وسيتم إنشاء ملف تعريف لجهاز جديد واستخدامه لإضافة محطات أجهزة جديدة إلى متجر محدد مسبقًا (القناة).</span><span class="sxs-lookup"><span data-stu-id="1ac1b-105">A new hardware profile will be created and used to add new hardware stations to a pre-defined store (channel).</span></span> <span data-ttu-id="1ac1b-106">ويستخدم هذا الإجراء شركة USRT في بيانات العرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="1ac1b-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="1ac1b-107">انتقل إلى أساسيات التجارة > القنوات >...</span><span class="sxs-lookup"><span data-stu-id="1ac1b-107">Go to Commerce essentials > Channels > ..</span></span> <span data-ttu-id="1ac1b-108">> ..</span><span class="sxs-lookup"><span data-stu-id="1ac1b-108">> ..</span></span> <span data-ttu-id="1ac1b-109">> ..</span><span class="sxs-lookup"><span data-stu-id="1ac1b-109">> ..</span></span> <span data-ttu-id="1ac1b-110">> ملفات تعريف ‏‫محطات الأجهزة‬.</span><span class="sxs-lookup"><span data-stu-id="1ac1b-110">> Hardware station profiles.</span></span>
2. <span data-ttu-id="1ac1b-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="1ac1b-111">Click New.</span></span>
3. <span data-ttu-id="1ac1b-112">في حقل "‏‫معرف محطة الأجهزة‬"، اكتب "TestHWProfile".</span><span class="sxs-lookup"><span data-stu-id="1ac1b-112">In the Hardware station ID field, type 'TestHWProfile'.</span></span>
4. <span data-ttu-id="1ac1b-113">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1ac1b-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="1ac1b-114">في حقل "‏‫رقم المنفذ‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="1ac1b-114">In the Port number field, enter a number.</span></span>
6. <span data-ttu-id="1ac1b-115">في حقل "‏‫ملف تعريف الأجهزة‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="1ac1b-115">In the Hardware profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="1ac1b-116">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="1ac1b-116">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="1ac1b-117">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="1ac1b-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="1ac1b-118">في حقل "‏‫اسم الحزمة‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="1ac1b-118">In the Package name field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="1ac1b-119">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="1ac1b-119">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1ac1b-120">هذه هي الحزمة القياسية التي تأتي مع البيئة الجديدة.</span><span class="sxs-lookup"><span data-stu-id="1ac1b-120">This is the standard package that comes with a new environment.</span></span> <span data-ttu-id="1ac1b-121">قد يختلف رقم الإصدار.</span><span class="sxs-lookup"><span data-stu-id="1ac1b-121">The version number may vary.</span></span>  
11. <span data-ttu-id="1ac1b-122">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="1ac1b-122">Click Save.</span></span>
12. <span data-ttu-id="1ac1b-123">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1ac1b-123">Close the page.</span></span>
13. <span data-ttu-id="1ac1b-124">انتقل إلى البيع بالتجزئة والتجارة > القنوات > جميع متاجر البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="1ac1b-124">Go to Retail and commerce > Channels > All retail stores.</span></span>
14. <span data-ttu-id="1ac1b-125">في القائمة، حدد الصف 17.</span><span class="sxs-lookup"><span data-stu-id="1ac1b-125">In the list, select row 17.</span></span>
    * <span data-ttu-id="1ac1b-126">إذا كنت تستخدم شركة بيانات العرض التوضيحي USRT، فهذا هو متجر هيوستن.</span><span class="sxs-lookup"><span data-stu-id="1ac1b-126">If you are using the USRT demo data company, this is the Houston store.</span></span>  
15. <span data-ttu-id="1ac1b-127">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="1ac1b-127">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="1ac1b-128">قم بتبديل التوسيع لقسم ‏‫محطات الأجهزة‬.</span><span class="sxs-lookup"><span data-stu-id="1ac1b-128">Toggle the expansion of the Hardware stations section.</span></span>
17. <span data-ttu-id="1ac1b-129">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="1ac1b-129">Click Add.</span></span>
18. <span data-ttu-id="1ac1b-130">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="1ac1b-130">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="1ac1b-131">في حقل "‏‫معرف ملف التعريف‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="1ac1b-131">In the Profile ID field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="1ac1b-132">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="1ac1b-132">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="1ac1b-133">يجب أن يمثل هذا ملف التعريف لمحطة الأجهزة الجديدة الذي تم إنشاؤه في الخطوات السابقة.</span><span class="sxs-lookup"><span data-stu-id="1ac1b-133">This must be the new hardware station profile that was created in the previous steps.</span></span>  
21. <span data-ttu-id="1ac1b-134">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="1ac1b-134">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="1ac1b-135">في حقل "اسم المضيف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1ac1b-135">In the Host name field, type a value.</span></span>
23. <span data-ttu-id="1ac1b-136">في حقل "‏‫معرف الوحدة الطرفية EFT‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1ac1b-136">In the EFT terminal ID field, type a value.</span></span>
24. <span data-ttu-id="1ac1b-137">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="1ac1b-137">Click Save.</span></span>

