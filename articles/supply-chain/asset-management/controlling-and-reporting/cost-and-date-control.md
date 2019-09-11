---
title: مراقبة التكلفة والتاريخ
description: يشرح هذا الموضوع مراقبة التكلفة والتاريخ في إدارة الأصول.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2bcd1584f6a858f7589387fbfe96267b7c16176a
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918385"
---
# <a name="cost-and-date-control"></a><span data-ttu-id="d90a9-103">مراقبة التكلفة والتاريخ</span><span class="sxs-lookup"><span data-stu-id="d90a9-103">Cost and date control</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="d90a9-104">في إدارة الأصول، يمكنك حساب التكاليف للحصول عل نظرة عامة على التكاليف الفعلية مقارنةً بتكاليف الموازنة على الأصول ومواقع العمل وأوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="d90a9-104">In Asset Management, you can calculate costs to get an overview of actual costs compared to budget costs on assets, functional locations, and work orders.</span></span> <span data-ttu-id="d90a9-105">تستند التكاليف الفعلية إلى الحركات المرحّلة.</span><span class="sxs-lookup"><span data-stu-id="d90a9-105">Actual costs are based on posted transactions.</span></span> <span data-ttu-id="d90a9-106">يمكنك أيضًا حساب التاريخ إذا أردت مقارنة تواريخ البدء والانتهاء المجدولة مع تواريخ البدء والانتهاء الفعلية في أوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="d90a9-106">You can also make a date calculation if you want to compare scheduled start and end dates to actual start and end dates on work orders.</span></span>

## <a name="cost-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="d90a9-107">مراقبة تكلفة الأصول ومواقع العمل وأوامر العمل</span><span class="sxs-lookup"><span data-stu-id="d90a9-107">Cost control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="d90a9-108">تعتبر العمليات الحسابية التي يتم تنفيذها للأصول ومواقع العمل وأوامر العمل مماثلة تقريبًا.</span><span class="sxs-lookup"><span data-stu-id="d90a9-108">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="d90a9-109">الفرق الوحيد هو أنه يمكنك أيضًا تضمين أصول فرعية ومواقع فرعية في حسابك فيما يتعلق بالأصول ومواقع العمل.</span><span class="sxs-lookup"><span data-stu-id="d90a9-109">Only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="d90a9-110">التاريخ هو تاريخ الحركة عندما تم إنشاء التسجيل.</span><span class="sxs-lookup"><span data-stu-id="d90a9-110">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="d90a9-111">انقر فوق **إدارة الأصول** > **استعلامات** > **الأصول‏‎** > **مراقبة تكلفة الأصول** أو **مراقبة تكلفة موقع العمل** أو **إدارة الأصول** > **استعلامات‏‎** > **أوامر العمل** > **مراقبة تكلفة أمر العمل**.</span><span class="sxs-lookup"><span data-stu-id="d90a9-111">Click **Asset management** > **Inquiries** > **Assets** > **Asset cost control** or **Functional location cost control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order cost control**.</span></span>

2. <span data-ttu-id="d90a9-112">في مربع الحوار **مراقبة تكلفة الأصول** / **مراقبة تكلفة موقع العمل** / **مراقبة تكلفة أمر العمل**، حدد فترة لحسابها.</span><span class="sxs-lookup"><span data-stu-id="d90a9-112">In the **Asset cost control** / **Functional location cost control** / **Work order cost control** dialog, select a period to be calculated.</span></span>

3. <span data-ttu-id="d90a9-113">إذا لزم الأمر، حدد مجموعة أبعاد مالية لتضمينها في الحساب.</span><span class="sxs-lookup"><span data-stu-id="d90a9-113">If required, select a financial dimension set to be included in the calculation.</span></span>

4. <span data-ttu-id="d90a9-114">حدد "نعم" على زر التبديل **تخطي الصفر** إذا لم ترغب في إظهار النتائج ذات تكلفة صفرية.</span><span class="sxs-lookup"><span data-stu-id="d90a9-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="d90a9-115">يمكنك استخدام حقل **المستوى** للإشارة إلى مستوى التفصيل الذي ترغب فيه في بنود مراقبة التكاليف فيما يتعلق بمواقع العمل.</span><span class="sxs-lookup"><span data-stu-id="d90a9-115">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> <span data-ttu-id="d90a9-116">على سبيل المثال، إذا قمت بإدراج الرقم "1" في الحقل، وكان لديك تدرجًا هرميًا لموقع عمل متعدد المستويات، فستظهر جميع بنود مراقبة تكاليف أخطاء الأصول لموقع عمل في المستوى العلوي، وبالتالي فإن الساعات على البند قد تُضاف من مواقع عمل موجودة في مستوى أدنى.</span><span class="sxs-lookup"><span data-stu-id="d90a9-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="d90a9-117">إذا قمت بإدراج الرقم "0" في حقل **المستوى**، فسترى نتيجة مفصلة تعرض جميع بنود مراقبة التكلفة على جميع مستويات مواقع العمل التي ترتبط بها.</span><span class="sxs-lookup"><span data-stu-id="d90a9-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all cost control lines on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="d90a9-118">حدد "نعم" على زر التبديل **إظهار التكلفة الإلزامية المفتوحة** إذا أردت تضمين ذلك في الحساب.</span><span class="sxs-lookup"><span data-stu-id="d90a9-118">Select "Yes" on the **Show open committed cost** toggle button if you want to include that column in the calculation.</span></span>

7. <span data-ttu-id="d90a9-119">حدد "نعم" على زر التبديل **تضمين الأصول الفرعية** لإظهار التكاليف المرتبطة بالأصول الفرعية كبنود منفصلة.</span><span class="sxs-lookup"><span data-stu-id="d90a9-119">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="d90a9-120">إذا كنت ترغب في تقييد البحث، فيمكنك تحديد أصول / مواقع عمل / أوامر عمل معينة على علامة التبويب السريعة **السجلات المطلوب تضمينها‬**.</span><span class="sxs-lookup"><span data-stu-id="d90a9-120">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="d90a9-121">انقر فوق **موافق** لبدء الحساب.</span><span class="sxs-lookup"><span data-stu-id="d90a9-121">Click **OK** to start the calculation.</span></span>

<span data-ttu-id="d90a9-122">يعرض الشكل أدناه مثالاً لمربع الحوار **مراقبة تكلفة الأصول**.</span><span class="sxs-lookup"><span data-stu-id="d90a9-122">The figure below shows an example of the **Asset cost control** dialog.</span></span>

![الشكل 1](media/01-controlling-and-reporting.png)

10. <span data-ttu-id="d90a9-124">في مجموعات جزء الإجراءات **تجميع حسب...** في صفحة **مراقبة تكلفة الأصول**، انقر فوق الأزرار المناسبة لعرض مستوى التفاصيل المطلوب للعملية الحسابية.</span><span class="sxs-lookup"><span data-stu-id="d90a9-124">In the **Group by...** action pane groups on the **Asset cost control** page, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="d90a9-125">يتم تمييز أزرار جزء الإجراءات المحددة.</span><span class="sxs-lookup"><span data-stu-id="d90a9-125">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="d90a9-126">انقر فوق زر لتنشيطه أو إلغاء تنشيطه.</span><span class="sxs-lookup"><span data-stu-id="d90a9-126">Click on a button to activate or deactivate it.</span></span>

<span data-ttu-id="d90a9-127">يعرض الشكل أدناه مثالاً لنتائج الحساب في **مراقبة تكلفة الأصول**.</span><span class="sxs-lookup"><span data-stu-id="d90a9-127">The figure below shows an example of calculation results in **Asset cost control**.</span></span>

![الشكل 2](media/02-controlling-and-reporting.png)

<span data-ttu-id="d90a9-129">ثمة طريقة أخرى لحساب التكلفة وهي إجراء تحديدات متعددة للأصول في **كل الأصول** أو **الأصول‏‎ النشطة**.</span><span class="sxs-lookup"><span data-stu-id="d90a9-129">Another way of making a cost calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="d90a9-130">انقر بعد ذلك فوق زر **مراقبة التكاليف‬** على علامة التبويب **عام**. في مربع الحوار‏‎ **مراقبة تكلفة الأصول**، يتم إدراج الأصول المحددة بشكل تلقائي في حقل **الأصل** على علامة التبويب السريعة **السجلات المطلوب تضمينها‬**.</span><span class="sxs-lookup"><span data-stu-id="d90a9-130">Then, you click the **Cost control** button on the **General** tab. In the **Asset cost control** dialog, the selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="d90a9-131">انقر فوق **موافق**، فيظهر حساب التكلفة للأصول المحددة.</span><span class="sxs-lookup"><span data-stu-id="d90a9-131">Click **OK**, and a cost calculation for the selected assets is shown.</span></span> <span data-ttu-id="d90a9-132">يمكن تنفيذ الإجراء نفسه لمواقع العمل في **جميع مواقع العمل** أو **مواقع العمل النشطة** ولأوامر العمل في **جميع أوامر العمل** أو **أوامر العمل النشطة**.</span><span class="sxs-lookup"><span data-stu-id="d90a9-132">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>

>[!NOTE]
><span data-ttu-id="d90a9-133">يعرض حقل **الموازنة‏‎ الأصلية** تكاليف الموازنة من تنبؤ أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="d90a9-133">The **Original budget** field shows budget costs from the work order forecast.</span></span> <span data-ttu-id="d90a9-134">يعرض حقل **التكلفة الإلزامية** المبلغ الإجمال للمصروفات التي ألزم الكيان القانوني نفسه بدفعها.</span><span class="sxs-lookup"><span data-stu-id="d90a9-134">The **Committed cost** field shows the total amount of expenses that a legal entity has committed itself to pay.</span></span> <span data-ttu-id="d90a9-135">يعرض حقل **التكلفة الإلزامية المفتوحة** التزامات السداد للأصناف والساعات والخدمات التي طلبتها أو استلمتها ولكن لم يتم دفعها بعد.</span><span class="sxs-lookup"><span data-stu-id="d90a9-135">The **Open committed cost** field shows commitments to pay for items, hours, and services you have ordered or received but not yet paid for.</span></span> <span data-ttu-id="d90a9-136">عند ترحيل كافة تسجيلات الاستهلاك، يتم تضمين التكاليف ذات الصلة في حقل **التكلفة الفعلية**.</span><span class="sxs-lookup"><span data-stu-id="d90a9-136">When all consumption registrations have been posted, the related costs are included in the **Actual cost** field.</span></span>

## <a name="work-order-date-control"></a><span data-ttu-id="d90a9-137">التحكم في تاريخ أمر العمل</span><span class="sxs-lookup"><span data-stu-id="d90a9-137">Work order date control</span></span>

<span data-ttu-id="d90a9-138">استخدم هذه الصفحة للحصول على نظرة عامة حول تواريخ البدء والانتهاء المتوقعة مقارنةً بتواريخ البدء والانتهاء الفعلية في أوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="d90a9-138">Use this page to get an overview of expected start and end dates compared to actual start and end dates on work orders.</span></span>

1. <span data-ttu-id="d90a9-139">انقر فوق **إدارة الأصول** > **استعلامات‏‎** > **أوامر العمل** > **مراقبة تاريخ أمر العمل**.</span><span class="sxs-lookup"><span data-stu-id="d90a9-139">Click **Asset management** > **Inquiries** > **Work orders** > **Work order date control**.</span></span>

2. <span data-ttu-id="d90a9-140">انقر فوق **حساب**.</span><span class="sxs-lookup"><span data-stu-id="d90a9-140">Click **Calculate**.</span></span>

3. <span data-ttu-id="d90a9-141">حدد موقع عمل في حقل **موقع العمل**.</span><span class="sxs-lookup"><span data-stu-id="d90a9-141">Select a functional location in the **Functional location** field.</span></span>

4. <span data-ttu-id="d90a9-142">أدخل الفترة التي تريد إجراء حساب لها في الحقلين **من تاريخ** و**إلى تاريخ**.</span><span class="sxs-lookup"><span data-stu-id="d90a9-142">Insert the period for which you want to make the calculation in the **From date** and **To date** fields.</span></span> <span data-ttu-id="d90a9-143">سيتم تضمين كافة أوامر العمل التي لها تاريخ بدء متوقع خلال الفترة.</span><span class="sxs-lookup"><span data-stu-id="d90a9-143">All work orders with expected start within the period will be included.</span></span>

5. <span data-ttu-id="d90a9-144">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d90a9-144">Click **OK**.</span></span>

6. <span data-ttu-id="d90a9-145">في مجموعات جزء الإجراءات **تجميع حسب...**، انقر فوق الأزرار ذات الصلة لإظهار مستوى التفاصيل المطلوب للحساب.</span><span class="sxs-lookup"><span data-stu-id="d90a9-145">In the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="d90a9-146">يتم تمييز أزرار جزء الإجراءات المحددة.</span><span class="sxs-lookup"><span data-stu-id="d90a9-146">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="d90a9-147">انقر فوق زر لتنشيطه أو إلغاء تنشيطه.</span><span class="sxs-lookup"><span data-stu-id="d90a9-147">Click on a button to activate or deactivate it.</span></span>

<span data-ttu-id="d90a9-148">يعرض الشكل أدناه مثالاً لنتائج الحساب في **مراقبة تكلفة الأصول**.</span><span class="sxs-lookup"><span data-stu-id="d90a9-148">The figure below shows an example of calculation results in **Work order date control**.</span></span>

![الشكل 3](media/03-controlling-and-reporting.png)

- <span data-ttu-id="d90a9-150">يظهر الحقل **متوسط تأخير البدء** الفرق بالأيام بين تاريخ البدء المجدول لأمر عمل مقارنةً بتاريخ البدء الفعلي.</span><span class="sxs-lookup"><span data-stu-id="d90a9-150">The **Avg. start delay** field shows the difference in days between scheduled start date for a work order compared to actual start date.</span></span> <span data-ttu-id="d90a9-151">على سبيل المثال، إذا كان تاريخ البدء الفعلي يومين قبل تاريخ البدء المجدول، فسيظهر "-2" في هذا الحقل.</span><span class="sxs-lookup"><span data-stu-id="d90a9-151">If, for example, the actual start date was two days before the scheduled start date, "-2" will be displayed in this field.</span></span>  
- <span data-ttu-id="d90a9-152">يظهر الحقل **متوسط تأخير الانتهاء** الفرق بالأيام بين تاريخ الانتهاء‏‎ المجدول لأمر عمل مقارنةً بتاريخ الانتهاء‏‎ الفعلي.</span><span class="sxs-lookup"><span data-stu-id="d90a9-152">The **Avg. end delay** field shows the difference in days between scheduled end date for a work order compared to actual end date.</span></span> <span data-ttu-id="d90a9-153">على سبيل المثال، إذا كان تاريخ الانتهاء‏‎ الفعلي ثلاثة أيام بعد تاريخ الانتهاء‏‎ المجدول، فسيظهر "3" في هذا الحقل.</span><span class="sxs-lookup"><span data-stu-id="d90a9-153">If, for example, the actual end date was three days after the scheduled end date, "3" will be displayed in this field.</span></span>  
- <span data-ttu-id="d90a9-154">تعرض حقول **مرات الحدوث‬** عدد المرات التي تحدث فيها انحرافات الوقت بالنسبة إلى تاريخ البدء الفعلي وتاريخ البدء المجدول، وتاريخ الانتهاء الفعلي وتاريخ الانتهاء المجدول على أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="d90a9-154">The **Occurrences** fields show the number of times deviations occur in relation to scheduled and actual start date, and scheduled and actual end date on the work order.</span></span>

