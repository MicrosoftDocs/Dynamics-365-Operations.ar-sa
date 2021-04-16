---
title: ترحيل دفاتر اليومية الدورية
description: دفاتر اليومية الدورية تسمى في بعض الأحيان دفاتر اليومية المتكررة بسبب تكرار المبلع والنص وغير ذلك من المعلومات في كل مرة يتم فيها استرجاع دفتر اليومية الدوري.
author: aprilolson
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransPeriodic, LedgerJournalTransDaily
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1dacf7f21d147b780d57b0e7a61b11d78d30fa52
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834394"
---
# <a name="post-periodic-journals"></a><span data-ttu-id="02360-103">ترحيل دفاتر اليومية الدورية</span><span class="sxs-lookup"><span data-stu-id="02360-103">Post periodic journals</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="02360-104">دفاتر اليومية الدورية تسمى في بعض الأحيان دفاتر اليومية المتكررة بسبب تكرار المبلع والنص وغير ذلك من المعلومات في كل مرة يتم فيها استرجاع دفتر اليومية الدوري.</span><span class="sxs-lookup"><span data-stu-id="02360-104">Periodic journals are sometimes called recurring journals because the amount, text, and other information are repeated each time that the periodic journal is retrieved.</span></span> <span data-ttu-id="02360-105">عند إنشاء دفتر اليومية الدوري، ستحدد الفاصل الزمني للتكرار، مثل الأيام أو الشهور.</span><span class="sxs-lookup"><span data-stu-id="02360-105">When you create the periodic journal, you specify the period interval for the recurrence, such as days or months.</span></span> <span data-ttu-id="02360-106">سينشئ دليل المهمة هذا دفتر يومية دوريًا مع تكرار شهري.</span><span class="sxs-lookup"><span data-stu-id="02360-106">This task guide will create a periodic journal with a monthly recurrence.</span></span>

1. <span data-ttu-id="02360-107">انتقل إلى جزء التنقل **> الوحدات النمطية > دفتر الأستاذ العام > مهام دورية‬ > تسجيل دفتر اليومية‬**.</span><span class="sxs-lookup"><span data-stu-id="02360-107">Go to **Navigation pane > Modules > General ledger > Periodic tasks > Periodic journals**.</span></span>
2. <span data-ttu-id="02360-108">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="02360-108">Click **New**.</span></span>
3. <span data-ttu-id="02360-109">في الحقل **الاسم** أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="02360-109">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="02360-110">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="02360-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="02360-111">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="02360-111">In the **Description** field, type a value.</span></span> <span data-ttu-id="02360-112">سيكون الوصف اسم دفتر اليومية الدوري عند استرجاعه في وقت لاحق، لذا إدخال اسم ذي صلة له.</span><span class="sxs-lookup"><span data-stu-id="02360-112">The description will be the name of the Periodic journal when retrieved later so make sure to give it a relevant name.</span></span>
6. <span data-ttu-id="02360-113">في **جزء الإجراءات**، انقر فوق **البنود**.</span><span class="sxs-lookup"><span data-stu-id="02360-113">On the **Action pane**, click **Lines**.</span></span> <span data-ttu-id="02360-114">يتضمن دفتر اليومية الدوري عادة الكثير من بنود دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="02360-114">A periodic journal will typically include several journal lines.</span></span> <span data-ttu-id="02360-115">غير أن دليل المهمة هذا سيضيف بندًا واحدًا فقط.</span><span class="sxs-lookup"><span data-stu-id="02360-115">this task guide will however only add one line.</span></span>
7. <span data-ttu-id="02360-116">في حقل **التاريخ**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="02360-116">In the **Date** field, enter a date.</span></span> <span data-ttu-id="02360-117">يحتوي حقل **التاريخ** على تاريخ الترحيل لعملية التحويل التالية إلى دفتر اليومية اليومي.</span><span class="sxs-lookup"><span data-stu-id="02360-117">The **Date** field contains the posting date for the next transfer to the daily journal.</span></span> <span data-ttu-id="02360-118">بالنسبة إلى دفاتر اليومية التي يتم استرجاعها كل شهر، من المستحسن استخدام التاريخ في الشهر عند ترحيله، عادة التاريخ الأول أو الأخير في الفترة الزمنية.</span><span class="sxs-lookup"><span data-stu-id="02360-118">For journals that will be retrieved each month it is recommended to use the date in the month when it will be posted, typically the first or last date in the period.</span></span> <span data-ttu-id="02360-119">يمكن ترك حقل "التاريخ" فارغًا وإعطاء تاريخ عند استرجاع دفتر اليومية، باستخدام حقل التاريخ الفارغ.</span><span class="sxs-lookup"><span data-stu-id="02360-119">It is possible to leave the Date field blank and to give a date when the journal is retrieved, using the Empty date field.</span></span> <span data-ttu-id="02360-120">يتم تحديث الحقل تلقائيًا وفق التاريخ المتكرر التالي عندما يتم استرجاع المعاملات.</span><span class="sxs-lookup"><span data-stu-id="02360-120">The field is automatically updated to the next recurring date when transactions are retrieved.</span></span> 
8. <span data-ttu-id="02360-121">في حقل **الحساب**، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="02360-121">In the **Account** field, specify the desired values.</span></span>
9. <span data-ttu-id="02360-122">في حقل **الوصف** ، حدد القيمة.</span><span class="sxs-lookup"><span data-stu-id="02360-122">In the **Description** field, select a value.</span></span>
10. <span data-ttu-id="02360-123">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="02360-123">Close the page.</span></span>
11. <span data-ttu-id="02360-124">في الحقل **مدين** ، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="02360-124">In the **Debit** field, enter a number.</span></span>
12. <span data-ttu-id="02360-125">في الحقل **حساب مقابل**، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="02360-125">In the **Offset account** field, specify the desired values.</span></span>
13. <span data-ttu-id="02360-126">في الحقل **الوحدة** ، حدد "الأشهر".</span><span class="sxs-lookup"><span data-stu-id="02360-126">In the **Unit** field, select 'Months'.</span></span>
14. <span data-ttu-id="02360-127">في الحقل **عدد الوحدات** ، أدخل "1".</span><span class="sxs-lookup"><span data-stu-id="02360-127">In the **Number of units** field, enter '1'.</span></span>
15. <span data-ttu-id="02360-128">في الحقل **آخر تاريخ‬** ، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="02360-128">In the **Last date** field, enter a date.</span></span> <span data-ttu-id="02360-129">سيؤدي إدخال آخر تاريخ في الفترة السابقة إلى منع إنشاء دفتر اليومية المتكرر عن طريق الخطأ في فترة البدء غير الصحيحة.</span><span class="sxs-lookup"><span data-stu-id="02360-129">Entering last date in the preceding period will prevent that the recurring journal by mistake is created in the wrong starting period.</span></span> <span data-ttu-id="02360-130">سيتم بعد ذلك تحديث آخر تاريخ في كل مرة يتم فيها استرجاع دفتر اليومية الدوري.</span><span class="sxs-lookup"><span data-stu-id="02360-130">Last date will later on be updated each time the periodic journal is retrieved.</span></span> 
16. <span data-ttu-id="02360-131">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="02360-131">Click **Save**.</span></span>
17. <span data-ttu-id="02360-132">انتقل إلى **جزء التنقل > الوحدات النمطية > دفتر الأستاذ العام > إدخالات دفتر اليومية > دفاتر اليومية العامة‬**.</span><span class="sxs-lookup"><span data-stu-id="02360-132">Go to **Navigation pane > Modules > General ledger > Journal entries > General journals**.</span></span>
18. <span data-ttu-id="02360-133">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="02360-133">Click **New**.</span></span>
19. <span data-ttu-id="02360-134">في الحقل **الاسم** أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="02360-134">In the **Name** field, enter or select a value.</span></span>
20. <span data-ttu-id="02360-135">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="02360-135">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="02360-136">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="02360-136">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="02360-137">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="02360-137">In the **Description** field, type a value.</span></span>
23. <span data-ttu-id="02360-138">في **جزء الإجراءات**، انقر فوق **البنود**.</span><span class="sxs-lookup"><span data-stu-id="02360-138">On the **Action pane**, click **Lines**.</span></span>
24. <span data-ttu-id="02360-139">انقر فوق **التحكم في دفتر اليومية‬‬**، في **جزء الإجراءات**.</span><span class="sxs-lookup"><span data-stu-id="02360-139">On the **Action pane**, click **Period journal**.</span></span>
25. <span data-ttu-id="02360-140">انقر فوق **استرجاع دفتر اليومية**.</span><span class="sxs-lookup"><span data-stu-id="02360-140">Click **Retrieve journal**.</span></span>
26. <span data-ttu-id="02360-141">في الحقل **إلى تاريخ**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="02360-141">In the **To date** field, enter a date.</span></span> <span data-ttu-id="02360-142">يعمل الخيار **إلى ‏‏تاريخ** بمثابة تاريخ الانقطاع لبنود الإيصال الدورية.</span><span class="sxs-lookup"><span data-stu-id="02360-142">The **To date** serves as the cutoff date for the periodic voucher lines.</span></span> <span data-ttu-id="02360-143">استنادًا إلى إعداد التكرار، قد يتم تضمين "آخر تاريخ" و"إلى تاريخ" على البند نفسه أكثر من مرة في دفتر اليومية الناتج.</span><span class="sxs-lookup"><span data-stu-id="02360-143">Based on the recurrence setting, the Last date and To date the same line might be included more than once in the resulting journal.</span></span> <span data-ttu-id="02360-144">يتم تحديث التاريخ تلقائيًا استنادًا إلى تاريخ الجلسة في المرة الأخيرة التي تم فيها تحويل البند الدوري إلى دفتر يومية.</span><span class="sxs-lookup"><span data-stu-id="02360-144">To date is automatically updated based on  session date of the last time the periodic line was transferred to a journal.</span></span> 
27. <span data-ttu-id="02360-145">في الحقل **رقم دفتر اليومية الدوري** ، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="02360-145">In the **Periodic journal number** field, enter or select a value.</span></span>
28. <span data-ttu-id="02360-146">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="02360-146">In the list, click the link in the selected row.</span></span>
29. <span data-ttu-id="02360-147">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="02360-147">Click **OK**.</span></span> <span data-ttu-id="02360-148">يمكن الآن مراجعة دفتر يومية الفترة‬ أو الموافقة عليه أو ترحيله تبعًا للمتطلبات والإعداد.</span><span class="sxs-lookup"><span data-stu-id="02360-148">The period journal can now be reviewed, approved or posted depending on requirement and setup.</span></span>   


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]