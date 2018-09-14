--- 
title: "ترحيل دفاتر اليومية الدورية"
description: "دفاتر اليومية الدورية تسمى في بعض الأحيان دفاتر اليومية المتكررة بسبب تكرار المبلع والنص وغير ذلك من المعلومات في كل مرة يتم فيها استرجاع دفتر اليومية الدوري."
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, LedgerJournalTransPeriodic, LedgerJournalTransDaily
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: deae523d922e1d6a4f7bb05433e9b1568c9c1ee9
ms.contentlocale: ar-sa
ms.lasthandoff: 09/14/2018

---
# <a name="post-periodic-journals"></a><span data-ttu-id="c8f98-103">ترحيل دفاتر اليومية الدورية</span><span class="sxs-lookup"><span data-stu-id="c8f98-103">Post periodic journals</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c8f98-104">دفاتر اليومية الدورية تسمى في بعض الأحيان دفاتر اليومية المتكررة بسبب تكرار المبلع والنص وغير ذلك من المعلومات في كل مرة يتم فيها استرجاع دفتر اليومية الدوري.</span><span class="sxs-lookup"><span data-stu-id="c8f98-104">Periodic journals are sometimes called recurring journals because the amount, text, and other information are repeated each time that the periodic journal is retrieved.</span></span> <span data-ttu-id="c8f98-105">عند إنشاء دفتر اليومية الدوري، ستحدد الفاصل الزمني للتكرار، مثل الأيام أو الشهور.</span><span class="sxs-lookup"><span data-stu-id="c8f98-105">When you create the periodic journal, you specify the period interval for the recurrence, such as days or months.</span></span> <span data-ttu-id="c8f98-106">سينشئ دليل المهمة هذا دفتر يومية دوريًا مع تكرار شهري.</span><span class="sxs-lookup"><span data-stu-id="c8f98-106">This task guide will create a periodic journal with a monthly recurrence.</span></span>



1. <span data-ttu-id="c8f98-107">انتقل إلى دفتر الأستاذ العام > المهام الدورية > دفاتر يومية دورية.</span><span class="sxs-lookup"><span data-stu-id="c8f98-107">Go to General ledger > Periodic tasks > Periodic journals.</span></span>
2. <span data-ttu-id="c8f98-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="c8f98-108">Click New.</span></span>
3. <span data-ttu-id="c8f98-109">في الحقل "الاسم"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c8f98-109">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="c8f98-110">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c8f98-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="c8f98-111">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c8f98-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="c8f98-112">سيكون الوصف اسم دفتر اليومية الدوري عند استرجاعه في وقت لاحق، لذا إدخال اسم ذي صلة له.</span><span class="sxs-lookup"><span data-stu-id="c8f98-112">The description will be the name of the Periodic journal when retrieved later so make sure to give it a relevant name.</span></span>  
6. <span data-ttu-id="c8f98-113">انقر فوق البنود.</span><span class="sxs-lookup"><span data-stu-id="c8f98-113">Click Lines.</span></span>
    * <span data-ttu-id="c8f98-114">يتضمن دفتر اليومية الدوري عادة الكثير من بنود دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="c8f98-114">A periodic journal will typically include several journal lines.</span></span> <span data-ttu-id="c8f98-115">غير أن دليل المهمة هذا سيضيف بندًا واحدًا فقط.</span><span class="sxs-lookup"><span data-stu-id="c8f98-115">this task guide will however only add one line.</span></span>  
7. <span data-ttu-id="c8f98-116">في حقل "التاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="c8f98-116">In the Date field, enter a date.</span></span>
    * <span data-ttu-id="c8f98-117">يحتوي حقل "التاريخ" على تاريخ الترحيل لعملية التحويل التالية إلى دفتر اليومية اليومي.</span><span class="sxs-lookup"><span data-stu-id="c8f98-117">The Date field contains the posting date for the next transfer to the daily journal.</span></span> <span data-ttu-id="c8f98-118">بالنسبة إلى دفاتر اليومية التي يتم استرجاعها كل شهر، من المستحسن استخدام التاريخ في الشهر عند ترحيله، عادة التاريخ الأول أو الأخير في الفترة الزمنية.</span><span class="sxs-lookup"><span data-stu-id="c8f98-118">For journals that will be retrieved each month it is recommended to use the date in the month when it will be posted, typically the first or last date in the period.</span></span> <span data-ttu-id="c8f98-119">يمكن ترك حقل "التاريخ" فارغًا وإعطاء تاريخ عند استرجاع دفتر اليومية، باستخدام حقل التاريخ الفارغ.</span><span class="sxs-lookup"><span data-stu-id="c8f98-119">It is possible to leave the Date field blank and to give a date when the journal is retrieved, using the Empty date field.</span></span>    <span data-ttu-id="c8f98-120">يتم تحديث الحقل تلقائيًا وفق التاريخ المتكرر التالي عندما يتم استرجاع المعاملات.</span><span class="sxs-lookup"><span data-stu-id="c8f98-120">The field is automatically updated to the next recurring date when transactions are retrieved.</span></span>  
8. <span data-ttu-id="c8f98-121">في حقل "الحساب"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c8f98-121">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="c8f98-122">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c8f98-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="c8f98-123">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c8f98-123">Close the page.</span></span>
11. <span data-ttu-id="c8f98-124">في الحقل "مدين"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="c8f98-124">In the Debit field, enter a number.</span></span>
12. <span data-ttu-id="c8f98-125">في الحقل "حساب مقابل"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c8f98-125">In the Offset account field, specify the desired values.</span></span>
13. <span data-ttu-id="c8f98-126">في حقل "الوحدة"، حدد "الأشهر".</span><span class="sxs-lookup"><span data-stu-id="c8f98-126">In the Unit field, select 'Months'.</span></span>
14. <span data-ttu-id="c8f98-127">في الحقل "عدد الوحدات"، أدخل "1".</span><span class="sxs-lookup"><span data-stu-id="c8f98-127">In the Number of units field, enter '1'.</span></span>
15. <span data-ttu-id="c8f98-128">في الحقل "آخر تاريخ‬"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="c8f98-128">In the Last date field, enter a date.</span></span>
    * <span data-ttu-id="c8f98-129">سيؤدي إدخال آخر تاريخ في الفترة السابقة إلى منع إنشاء دفتر اليومية المتكرر عن طريق الخطأ في فترة البدء غير الصحيحة.</span><span class="sxs-lookup"><span data-stu-id="c8f98-129">Entering last date in the preceding period will prevent that the recurring journal by mistake is created in the wrong starting period.</span></span> <span data-ttu-id="c8f98-130">سيتم بعد ذلك تحديث آخر تاريخ في كل مرة يتم فيها استرجاع دفتر اليومية الدوري.</span><span class="sxs-lookup"><span data-stu-id="c8f98-130">Last date will later on be updated each time the periodic journal is retrieved.</span></span>  
16. <span data-ttu-id="c8f98-131">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="c8f98-131">Click Save.</span></span>
17. <span data-ttu-id="c8f98-132">انتقل إلى لوحة المعلومات الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="c8f98-132">Go to Default dashboard.</span></span>
18. <span data-ttu-id="c8f98-133">انتقل إلى دفتر الأستاذ العام > إدخالات دفتر اليومية > دفاتر اليومية العامة‬.</span><span class="sxs-lookup"><span data-stu-id="c8f98-133">Go to General ledger > Journal entries > General journals.</span></span>
19. <span data-ttu-id="c8f98-134">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="c8f98-134">Click New.</span></span>
20. <span data-ttu-id="c8f98-135">في الحقل "الاسم"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c8f98-135">In the Name field, enter or select a value.</span></span>
21. <span data-ttu-id="c8f98-136">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c8f98-136">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="c8f98-137">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c8f98-137">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="c8f98-138">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c8f98-138">In the Description field, type a value.</span></span>
24. <span data-ttu-id="c8f98-139">انقر فوق البنود.</span><span class="sxs-lookup"><span data-stu-id="c8f98-139">Click Lines.</span></span>
25. <span data-ttu-id="c8f98-140">انقر فوق "دفتر يومية الفترة".</span><span class="sxs-lookup"><span data-stu-id="c8f98-140">Click Period journal.</span></span>
26. <span data-ttu-id="c8f98-141">انقر فوق "استرجاع دفتر اليومية‬".</span><span class="sxs-lookup"><span data-stu-id="c8f98-141">Click Retrieve journal.</span></span>
27. <span data-ttu-id="c8f98-142">في الحقل "إلى تاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="c8f98-142">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="c8f98-143">يعمل الخيار "إلى ‏‏تاريخ‬" بمثابة تاريخ الانقطاع لبنود الإيصال الدورية.</span><span class="sxs-lookup"><span data-stu-id="c8f98-143">The To date serves as the cutoff date for the periodic voucher lines.</span></span> <span data-ttu-id="c8f98-144">استنادًا إلى إعداد التكرار، قد يتم تضمين "آخر تاريخ" و"إلى تاريخ" على البند نفسه أكثر من مرة في دفتر اليومية الناتج.</span><span class="sxs-lookup"><span data-stu-id="c8f98-144">Based on the recurrence setting, the Last date and To date the same line might be included more than once in the resulting journal.</span></span> <span data-ttu-id="c8f98-145">يتم تحديث التاريخ تلقائيًا استنادًا إلى تاريخ الجلسة في المرة الأخيرة التي تم فيها تحويل البند الدوري إلى دفتر يومية.</span><span class="sxs-lookup"><span data-stu-id="c8f98-145">To date is automatically updated based on  session date of the last time the periodic line was transferred to a journal.</span></span>  
28. <span data-ttu-id="c8f98-146">في الحقل "رقم دفتر اليومية الدوري"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c8f98-146">In the Periodic journal number field, enter or select a value.</span></span>
29. <span data-ttu-id="c8f98-147">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c8f98-147">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="c8f98-148">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c8f98-148">Click OK.</span></span>
    * <span data-ttu-id="c8f98-149">يمكن الآن مراجعة دفتر يومية الفترة‬ أو الموافقة عليه أو ترحيله تبعًا للمتطلبات والإعداد.</span><span class="sxs-lookup"><span data-stu-id="c8f98-149">The period journal can now be reviewed, approved or posted depending on requirement and setup.</span></span>  


