---
title: مراقبة التكلفة والتاريخ
description: يشرح هذا الموضوع مراقبة التكلفة والتاريخ في إدارة الأصول.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetBICostControlWorkspace, EntAssetWorkOrderDateControl, EntAssetWorkOrderForecastCostInfoPart, EntAssetMaintenanceCostTrans, EntAssetWorkOrderDateControlCalcDialog, EntAssetCostControl, EntAssetCostObjectCalendar, EntAssetWorkOrderCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d6f0a155b38b1d732d17bd2f964677862ff363e2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808654"
---
# <a name="cost-and-date-control"></a><span data-ttu-id="31bc0-103">مراقبة التكلفة والتاريخ</span><span class="sxs-lookup"><span data-stu-id="31bc0-103">Cost and date control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="31bc0-104">في إدارة الأصول، يمكنك حساب التكاليف للحصول عل نظرة عامة على التكاليف الفعلية مقارنةً بتكاليف الموازنة على الأصول ومواقع العمل وأوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="31bc0-104">In Asset Management, you can calculate costs to get an overview of actual costs compared to budget costs on assets, functional locations, and work orders.</span></span> <span data-ttu-id="31bc0-105">تستند التكاليف الفعلية إلى الحركات المرحّلة.</span><span class="sxs-lookup"><span data-stu-id="31bc0-105">Actual costs are based on posted transactions.</span></span> 

<span data-ttu-id="31bc0-106">يمكنك أيضًا حساب التاريخ إذا أردت مقارنة تواريخ البدء والانتهاء المجدولة مع تواريخ البدء والانتهاء الفعلية في أوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="31bc0-106">You can also make a date calculation if you want to compare scheduled start and end dates to actual start and end dates on work orders.</span></span>

## <a name="cost-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="31bc0-107">مراقبة تكلفة الأصول ومواقع العمل وأوامر العمل</span><span class="sxs-lookup"><span data-stu-id="31bc0-107">Cost control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="31bc0-108">تعتبر العمليات الحسابية التي يتم تنفيذها للأصول ومواقع العمل وأوامر العمل مماثلة تقريبًا.</span><span class="sxs-lookup"><span data-stu-id="31bc0-108">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="31bc0-109">الفرق الوحيد هو أنه يمكنك أيضًا تضمين أصول فرعية ومواقع فرعية في حسابك فيما يتعلق بالأصول ومواقع العمل.</span><span class="sxs-lookup"><span data-stu-id="31bc0-109">The only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="31bc0-110">التاريخ هو تاريخ الحركة عندما تم إنشاء التسجيل.</span><span class="sxs-lookup"><span data-stu-id="31bc0-110">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="31bc0-111">انقر فوق **إدارة الأصول** > **استعلامات** > **الأصول‏‎** > **مراقبة تكلفة الأصول** أو **مراقبة تكلفة موقع العمل** أو **إدارة الأصول** > **استعلامات‏‎** > **أوامر العمل** > **مراقبة تكلفة أمر العمل**.</span><span class="sxs-lookup"><span data-stu-id="31bc0-111">Click **Asset management** > **Inquiries** > **Assets** > **Asset cost control** or **Functional location cost control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order cost control**.</span></span>

2. <span data-ttu-id="31bc0-112">في مربع الحوار **مراقبة تكلفة الأصول** / **مراقبة تكلفة موقع العمل** / **مراقبة تكلفة أمر العمل** ، حدد فترة لحسابها.</span><span class="sxs-lookup"><span data-stu-id="31bc0-112">In the **Asset cost control** / **Functional location cost control** / **Work order cost control** dialog, select a time range to be calculated.</span></span>

3. <span data-ttu-id="31bc0-113">إذا لزم الأمر، حدد مجموعة أبعاد مالية لتضمينها في الحساب.</span><span class="sxs-lookup"><span data-stu-id="31bc0-113">If required, select a financial dimension set to be included in the calculation.</span></span>

4. <span data-ttu-id="31bc0-114">حدد "نعم" على زر التبديل **تخطي الصفر** إذا لم ترغب في إظهار النتائج ذات تكلفة صفرية.</span><span class="sxs-lookup"><span data-stu-id="31bc0-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="31bc0-115">يمكنك استخدام حقل **المستوى** للإشارة إلى مستوى التفصيل الذي ترغب فيه في بنود مراقبة التكاليف فيما يتعلق بمواقع العمل.</span><span class="sxs-lookup"><span data-stu-id="31bc0-115">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="31bc0-116">على سبيل المثال، إذا قمت بإدراج الرقم "1" في الحقل، وكان لديك تدرجًا هرميًا لموقع عمل متعدد المستويات، فستظهر جميع بنود مراقبة تكاليف أخطاء الأصول لموقع عمل في المستوى العلوي، وبالتالي فإن الساعات على البند قد تُضاف من مواقع عمل موجودة في مستوى أدنى.</span><span class="sxs-lookup"><span data-stu-id="31bc0-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="31bc0-117">إذا قمت بإدراج الرقم "0" في حقل **المستوى**، فسترى نتيجة مفصلة تعرض جميع بنود مراقبة التكلفة على جميع مستويات مواقع العمل التي ترتبط بها.</span><span class="sxs-lookup"><span data-stu-id="31bc0-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all cost control lines on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="31bc0-118">حدد "نعم" على زر التبديل **إظهار التكلفة الإلزامية المفتوحة** إذا أردت تضمين ذلك في الحساب.</span><span class="sxs-lookup"><span data-stu-id="31bc0-118">Select "Yes" on the **Show open committed cost** toggle button if you want to include that column in the calculation.</span></span>

7. <span data-ttu-id="31bc0-119">حدد "نعم" على زر التبديل **تضمين الأصول الفرعية** لإظهار التكاليف المرتبطة بالأصول الفرعية كبنود منفصلة.</span><span class="sxs-lookup"><span data-stu-id="31bc0-119">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="31bc0-120">إذا كنت ترغب في تقييد البحث، فيمكنك تحديد أصول / مواقع عمل / أوامر عمل معينة على علامة التبويب السريعة **السجلات المطلوب تضمينها‬**.</span><span class="sxs-lookup"><span data-stu-id="31bc0-120">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="31bc0-121">انقر فوق **موافق** لبدء الحساب.</span><span class="sxs-lookup"><span data-stu-id="31bc0-121">Click **OK** to start the calculation.</span></span>

    <span data-ttu-id="31bc0-122">يعرض الشكل أدناه مثالاً لمربع الحوار **مراقبة تكلفة الأصول**.</span><span class="sxs-lookup"><span data-stu-id="31bc0-122">The figure below shows an example of the **Asset cost control** dialog.</span></span>

    ![مربع حوار مراقبة تكلفة الأصول](media/01-controlling-and-reporting.png)

10. <span data-ttu-id="31bc0-124">في صفحة **مراقبة تكلفة الأصول** ، انقر فوق الأزرار **تجميع حسب** لإظهار مستوى التفاصيل المطلوب للحساب.</span><span class="sxs-lookup"><span data-stu-id="31bc0-124">On the **Asset cost control** page, click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="31bc0-125">يتم تمييز أزرار **تجميع حسب** المحددة.</span><span class="sxs-lookup"><span data-stu-id="31bc0-125">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="31bc0-126">انقر فوق زر لتنشيطه أو إلغاء تنشيطه.</span><span class="sxs-lookup"><span data-stu-id="31bc0-126">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="31bc0-127">مثال</span><span class="sxs-lookup"><span data-stu-id="31bc0-127">Example</span></span>

<span data-ttu-id="31bc0-128">تعرض لقطة الشاشة أدناه مثالاً لنتائج الحساب في **مراقبة تكلفة الأصول**.</span><span class="sxs-lookup"><span data-stu-id="31bc0-128">The screenshot below shows an example of calculation results in **Asset cost control**.</span></span>

- <span data-ttu-id="31bc0-129">يعرض حقل **الموازنة‏‎ الأصلية** تكاليف الموازنة من تنبؤ أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="31bc0-129">The **Original budget** field shows budget costs from the work order forecast.</span></span> 
- <span data-ttu-id="31bc0-130">يعرض حقل **التكلفة الإلزامية** المبلغ الإجمال للمصروفات التي ألزم الكيان القانوني نفسه بدفعها.</span><span class="sxs-lookup"><span data-stu-id="31bc0-130">The **Committed cost** field shows the total amount of expenses that a legal entity has committed itself to pay.</span></span> 
- <span data-ttu-id="31bc0-131">يعرض حقل **التكلفة الإلزامية المفتوحة** التزامات السداد للأصناف والساعات والخدمات التي طلبتها أو استلمتها ولكن لم يتم دفعها بعد.</span><span class="sxs-lookup"><span data-stu-id="31bc0-131">The **Open committed cost** field shows commitments to pay for items, hours, and services you have ordered or received but not yet paid for.</span></span> 
- <span data-ttu-id="31bc0-132">يعرض حقل **التكلفة الفعلية** التكاليف ذات الصلة بعد ترحيل كافة تسجيلات الاستهلاك.</span><span class="sxs-lookup"><span data-stu-id="31bc0-132">The **Actual cost** field shows related costs after all consumption registrations have been posted.</span></span>

![مثال على نتائج الحساب في مراقبة تكلفة الأصول](media/02-controlling-and-reporting.png)

<span data-ttu-id="31bc0-134">ثمة طريقة أخرى لحساب التكلفة وهي إجراء تحديدات متعددة للأصول في **كل الأصول** أو **الأصول‏‎ النشطة**.</span><span class="sxs-lookup"><span data-stu-id="31bc0-134">Another way of making a cost calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="31bc0-135">انقر بعد ذلك فوق زر **مراقبة التكاليف‬** على علامة التبويب **عام**. في مربع الحوار‏‎ **مراقبة تكلفة الأصول**، يتم إدراج الأصول المحددة بشكل تلقائي في حقل **الأصل** على علامة التبويب السريعة **السجلات المطلوب تضمينها‬**.</span><span class="sxs-lookup"><span data-stu-id="31bc0-135">Then, you click the **Cost control** button on the **General** tab. In the **Asset cost control** dialog, the selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="31bc0-136">انقر فوق **موافق**، فيظهر حساب التكلفة للأصول المحددة.</span><span class="sxs-lookup"><span data-stu-id="31bc0-136">Click **OK**, and a cost calculation for the selected assets is shown.</span></span> <span data-ttu-id="31bc0-137">يمكن تنفيذ الإجراء نفسه لمواقع العمل في **جميع مواقع العمل** أو **مواقع العمل النشطة** ولأوامر العمل في **جميع أوامر العمل** أو **أوامر العمل النشطة**.</span><span class="sxs-lookup"><span data-stu-id="31bc0-137">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>


## <a name="work-order-date-control"></a><span data-ttu-id="31bc0-138">التحكم في تاريخ أمر العمل</span><span class="sxs-lookup"><span data-stu-id="31bc0-138">Work order date control</span></span>

<span data-ttu-id="31bc0-139">استخدم هذه الصفحة للحصول على نظرة عامة حول تواريخ البدء والانتهاء المتوقعة مقارنةً بتواريخ البدء والانتهاء الفعلية في أوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="31bc0-139">Use this page to get an overview of expected start and end dates compared to actual start and end dates on work orders.</span></span>

1. <span data-ttu-id="31bc0-140">انقر فوق **إدارة الأصول** > **استعلامات‏‎** > **أوامر العمل** > **مراقبة تاريخ أمر العمل**.</span><span class="sxs-lookup"><span data-stu-id="31bc0-140">Click **Asset management** > **Inquiries** > **Work orders** > **Work order date control**.</span></span>

2. <span data-ttu-id="31bc0-141">انقر فوق **حساب**.</span><span class="sxs-lookup"><span data-stu-id="31bc0-141">Click **Calculate**.</span></span>

3. <span data-ttu-id="31bc0-142">حدد موقع عمل في حقل **موقع العمل**.</span><span class="sxs-lookup"><span data-stu-id="31bc0-142">Select a functional location in the **Functional location** field.</span></span>

4. <span data-ttu-id="31bc0-143">أدخل الفترة التي تريد إجراء حساب لها في الحقلين **من تاريخ** و **إلى تاريخ** .</span><span class="sxs-lookup"><span data-stu-id="31bc0-143">Insert the range for which you want to make the calculation in the **From date** and **To date** fields.</span></span> <span data-ttu-id="31bc0-144">سوف يتم تضمين كافة أوامر العمل التي لها تاريخ بدء متوقع ضمن النطاق.</span><span class="sxs-lookup"><span data-stu-id="31bc0-144">All work orders with expected start date within the range will be included.</span></span>

5. <span data-ttu-id="31bc0-145">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="31bc0-145">Click **OK**.</span></span>

6. <span data-ttu-id="31bc0-146">انقر على الأزرار **تجميع حسب** لإظهار مستوى التفاصيل المطلوب للحساب.</span><span class="sxs-lookup"><span data-stu-id="31bc0-146">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="31bc0-147">يتم تمييز أزرار **تجميع حسب** المحددة.</span><span class="sxs-lookup"><span data-stu-id="31bc0-147">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="31bc0-148">انقر فوق زر لتنشيطه أو إلغاء تنشيطه.</span><span class="sxs-lookup"><span data-stu-id="31bc0-148">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="31bc0-149">مثال</span><span class="sxs-lookup"><span data-stu-id="31bc0-149">Example</span></span>

<span data-ttu-id="31bc0-150">تعرض لقطة الشاشة أدناه مثالاً لنتائج الحساب في **مراقبة تاريخ أمر العمل**.</span><span class="sxs-lookup"><span data-stu-id="31bc0-150">The screenshot below shows an example of calculation results in **Work order date control**.</span></span>

- <span data-ttu-id="31bc0-151">يظهر الحقل **متوسط تأخير البدء** الفرق بالأيام بين تاريخ البدء المجدول لأمر عمل مقارنةً بتاريخ البدء الفعلي.</span><span class="sxs-lookup"><span data-stu-id="31bc0-151">The **Avg. start delay** field shows the difference in days between scheduled start date for a work order compared to actual start date.</span></span> <span data-ttu-id="31bc0-152">على سبيل المثال، إذا كان تاريخ البدء الفعلي يومين قبل تاريخ البدء المجدول، فسيظهر "-2" في هذا الحقل.</span><span class="sxs-lookup"><span data-stu-id="31bc0-152">If, for example, the actual start date was two days before the scheduled start date, "-2" will be displayed in this field.</span></span>  
- <span data-ttu-id="31bc0-153">يظهر الحقل **متوسط تأخير الانتهاء** الفرق بالأيام بين تاريخ الانتهاء‏‎ المجدول لأمر عمل مقارنةً بتاريخ الانتهاء‏‎ الفعلي.</span><span class="sxs-lookup"><span data-stu-id="31bc0-153">The **Avg. end delay** field shows the difference in days between scheduled end date for a work order compared to actual end date.</span></span> <span data-ttu-id="31bc0-154">على سبيل المثال، إذا كان تاريخ الانتهاء‏‎ الفعلي ثلاثة أيام بعد تاريخ الانتهاء‏‎ المجدول، فسيظهر "3" في هذا الحقل.</span><span class="sxs-lookup"><span data-stu-id="31bc0-154">If, for example, the actual end date was three days after the scheduled end date, "3" will be displayed in this field.</span></span>  
- <span data-ttu-id="31bc0-155">تعرض حقول **مرات الحدوث‬** عدد المرات التي تحدث فيها انحرافات الوقت بالنسبة إلى تاريخ البدء الفعلي وتاريخ البدء المجدول، وتاريخ الانتهاء الفعلي وتاريخ الانتهاء المجدول على أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="31bc0-155">The **Occurrences** fields show the number of times deviations occur in relation to scheduled and actual start date, and scheduled and actual end date on the work order.</span></span>

![مثال على نتائج الحساب في مراقبة تاريخ أمر العمل](media/03-controlling-and-reporting.png)




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]