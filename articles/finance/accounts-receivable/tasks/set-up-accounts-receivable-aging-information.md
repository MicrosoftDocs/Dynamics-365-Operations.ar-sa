---
title: إعداد وإنشاء معلومات تقادم الحسابات المدينة
description: سوف يساعدك هذا الدليل في إعداد تعريف فترة تقادم، وأرصدة العميل القديمة‬، وعرض الأرصدة في قائمة الأرصدة المتقادم‬ة وصفحة التحصيلات‬.
author: mikefalkner
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustVendReportInterval, CustAgingSnapshot, CustCollectionsPoolsListPage, CustCollections
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 19b60d5fcfba995d08f12d0548f41a0c3d2781fb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012076"
---
# <a name="set-up-and-generate-accounts-receivable-aging-information"></a><span data-ttu-id="43b81-103">إعداد وإنشاء معلومات تقادم الحسابات المدينة</span><span class="sxs-lookup"><span data-stu-id="43b81-103">Set up and generate accounts receivable aging information</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="43b81-104">سوف يساعدك هذا الدليل في إعداد تعريف فترة تقادم، وأرصدة العميل القديمة‬، وعرض الأرصدة في قائمة الأرصدة المتقادم‬ة وصفحة التحصيلات‬.</span><span class="sxs-lookup"><span data-stu-id="43b81-104">This guide will help you set up an aging period definition, age customer balances, and view balances in the Aged balance list and the Collections page.</span></span> <span data-ttu-id="43b81-105">يستخدم هذا التسجيل شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="43b81-105">This recording uses the USMF demo company.</span></span>


## <a name="create-an-aging-period-definition"></a><span data-ttu-id="43b81-106">إنشاء تعريف فترة تقادم</span><span class="sxs-lookup"><span data-stu-id="43b81-106">Create an aging period definition</span></span>
1. <span data-ttu-id="43b81-107">انتقل إلى **جزء التنقل > الوحدات النمطية‬ > عمليات التحصيل والائتمان‬ > الإعداد > تعريفات فترة التقادم**.</span><span class="sxs-lookup"><span data-stu-id="43b81-107">Go to **Navigation pane > Modules > Credit and collections > Setup > Aging period definitions**.</span></span>
2. <span data-ttu-id="43b81-108">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="43b81-108">Click **New**.</span></span>
3. <span data-ttu-id="43b81-109">في الحقل **تعريف فترة التقادم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="43b81-109">In the **Aging period definition** field, type a value.</span></span>
4. <span data-ttu-id="43b81-110">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="43b81-110">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="43b81-111">انقر فوق **الإضافة بالأسفل**‬ لإدراج فترة تقادم جديدة.</span><span class="sxs-lookup"><span data-stu-id="43b81-111">Click **Add below** to insert a new aging period.</span></span>
6. <span data-ttu-id="43b81-112">في الحقل **الفترة**، أدخل الوصف لإظهار تقارير التقادم.</span><span class="sxs-lookup"><span data-stu-id="43b81-112">In the **Period** field, enter the description to show on aging reports.</span></span>
7. <span data-ttu-id="43b81-113">في حقل **الوحدة**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="43b81-113">In the **Unit** field, enter a number.</span></span>
8. <span data-ttu-id="43b81-114">في الحقل **الفاصل الزمني‬**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="43b81-114">In the **Interval** field, select an option.</span></span> <span data-ttu-id="43b81-115">تطابق فترة دفتر الأستاذ فترة تقويم دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="43b81-115">Ledger period matches the period to your ledger calendar.</span></span> <span data-ttu-id="43b81-116">يحدد اليوم والأسبوع والشهر وربع السنة والسنوات حجم الفاصل الزمني حسب نوع التاريخ.</span><span class="sxs-lookup"><span data-stu-id="43b81-116">Day, week, month, quarter and years define the size of the interval by date type.</span></span> <span data-ttu-id="43b81-117">يؤدي تحديد الخيار "غير محدد‬" إلى تحديد كافة الحركات قبل الفترة السابقة أو بعدها، استنادًا إلى ما إذا كانت الفترة هي الأولى أو الأخيرة.</span><span class="sxs-lookup"><span data-stu-id="43b81-117">Unlimited selects all transactions before or after the previous period, depending on whether it is the first or last period.</span></span>  
9. <span data-ttu-id="43b81-118">في الحقل **مؤشر فترة التقادم**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="43b81-118">In the **Aging indicator** field, select an option.</span></span>
10. <span data-ttu-id="43b81-119">حدد الفترة في أعلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="43b81-119">Select the period at the top of the grid.</span></span> <span data-ttu-id="43b81-120">حدّث الوصف لوصف الفترة الأقدم في تعريف فترة التقادم</span><span class="sxs-lookup"><span data-stu-id="43b81-120">Update the description to describe the oldest period in the aging period definition</span></span>
11. <span data-ttu-id="43b81-121">في الحقل **الفترة**، أدخل الوصف الجديد لفترة التقادم.</span><span class="sxs-lookup"><span data-stu-id="43b81-121">In the **Period** field, enter the new description of the aging period.</span></span>
12. <span data-ttu-id="43b81-122">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="43b81-122">Close the page.</span></span>

## <a name="age-the-balances"></a><span data-ttu-id="43b81-123">تقادم الأرصدة</span><span class="sxs-lookup"><span data-stu-id="43b81-123">Age the balances</span></span>
1. <span data-ttu-id="43b81-124">انتقل إلى **التحصيلات والائتمان‬ > المهام الدورية > أرصدة العميل القديمة**‬.</span><span class="sxs-lookup"><span data-stu-id="43b81-124">Go to **Credit and collections > Periodic tasks > Age customer balances**.</span></span>
2. <span data-ttu-id="43b81-125">في حقل **تعريف فترة التقادم**، حدد تعريف فترة التقادم الذي قمت بإنشائه.</span><span class="sxs-lookup"><span data-stu-id="43b81-125">In the **Aging period definition** field, select the aging period definition that you created.</span></span>
    + <span data-ttu-id="43b81-126">يمكنك إنشاء لقطة نشطة واحدة لكل تعريف فترة تقادم.</span><span class="sxs-lookup"><span data-stu-id="43b81-126">You can have one active snapshot for each aging period definition.</span></span>  
    + <span data-ttu-id="43b81-127">تتم معالجة كافة العملاء بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="43b81-127">All customers are processed by default.</span></span> <span data-ttu-id="43b81-128">يمكنك استخدام هذا التحديد لحساب مجموعة تحصيلات واحدة للعملاء.</span><span class="sxs-lookup"><span data-stu-id="43b81-128">You can use this selection to calculate a single collections pool of customers.</span></span>  
    + <span data-ttu-id="43b81-129">حدد التاريخ من الحركة التي ستستخدمها للتقادم.</span><span class="sxs-lookup"><span data-stu-id="43b81-129">Select the date from the transaction that you will use for the aging.</span></span>  
    + <span data-ttu-id="43b81-130">حدد تاريخ "بدءًا من‬" للتقادم.</span><span class="sxs-lookup"><span data-stu-id="43b81-130">Select an "as of" date for aging.</span></span> <span data-ttu-id="43b81-131">التاريخ الافتراضي هو اليوم، ولكن إذا قمت بتغيير هذا الحقل إلى تاريخ "محدد"، فستكون قادرًا على اختيار التاريخ الذي تريده.</span><span class="sxs-lookup"><span data-stu-id="43b81-131">The default is today but, if you change this field to Selected date, you will be able to pick the date that you want.</span></span> <span data-ttu-id="43b81-132">لمعالجة الدُفعة، استخدم تاريخ اليوم.</span><span class="sxs-lookup"><span data-stu-id="43b81-132">For batch processing, use Today's date.</span></span>  
3. <span data-ttu-id="43b81-133">وسّع نطاق **الشركة**.</span><span class="sxs-lookup"><span data-stu-id="43b81-133">Expand the **Company** range.</span></span> <span data-ttu-id="43b81-134">يمكنك تحديد الشركات التي سيتم تضمينها في اللقطة.</span><span class="sxs-lookup"><span data-stu-id="43b81-134">You can select the companies that will be included in the snapshot.</span></span> <span data-ttu-id="43b81-135">تم تحديد الشركة الحالية بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="43b81-135">The current company is selected by default.</span></span>
4. <span data-ttu-id="43b81-136">انقر فوق **موافق** لمعالجة اللقطة.</span><span class="sxs-lookup"><span data-stu-id="43b81-136">Click **Ok** to process the snapshot.</span></span> <span data-ttu-id="43b81-137">سوف يستغرق الأمر بعض الوقت، لذا انتظر حتى اختفاء المنزلق‬ وتحقق من وجود رسالة في مركز الرسائل.</span><span class="sxs-lookup"><span data-stu-id="43b81-137">It will take some time so wait for the slider to disappear and check the message center for a message.</span></span>

## <a name="view-the-balances-on-the-aged-balances-list-and-on-the-collection-page"></a><span data-ttu-id="43b81-138">عرض الأرصدة في قائمة الأرصدة القديمة وصفحة التحصيلات</span><span class="sxs-lookup"><span data-stu-id="43b81-138">View the balances on the Aged balances list and on the Collection page</span></span>
1. <span data-ttu-id="43b81-139">انتقل إلى **التحصيلات والائتمان > التحصيلات > الأرصدة المتقادمة**.</span><span class="sxs-lookup"><span data-stu-id="43b81-139">Go to **Credit and collections > Collections > Aged balances**.</span></span> <span data-ttu-id="43b81-140">تعرض صفحة القائمة أرصدة العميل.</span><span class="sxs-lookup"><span data-stu-id="43b81-140">The list page shows the balances for the customer.</span></span> <span data-ttu-id="43b81-141">تعرض أيقونة التقادم فترة التقادم للحركة الأقدم.</span><span class="sxs-lookup"><span data-stu-id="43b81-141">The aging icon shows the aging period for the oldest transaction.</span></span>  
2. <span data-ttu-id="43b81-142">حدد عميلاً له رصيد.</span><span class="sxs-lookup"><span data-stu-id="43b81-142">Select a customer with a balance.</span></span>
3. <span data-ttu-id="43b81-143">وسّع منطقة مربع **حقائق التقادم** لعرض الأرصدة المتقادمة.</span><span class="sxs-lookup"><span data-stu-id="43b81-143">Expand the **Aging fact** box area to view the aged balances.</span></span> <span data-ttu-id="43b81-144">يؤخذ تعريف فترة التقادم لمربع الحقائق من تعريف فترة التقادم الافتراضية المحددة في المحددات.</span><span class="sxs-lookup"><span data-stu-id="43b81-144">The aging period definition for the fact box is taken from the default aging period definition specified in the parameters.</span></span> <span data-ttu-id="43b81-145">يمكنك تغيير ذلك باستخدام القائمة "تحصيل‬".</span><span class="sxs-lookup"><span data-stu-id="43b81-145">You can change it using the Collect menu.</span></span>  

