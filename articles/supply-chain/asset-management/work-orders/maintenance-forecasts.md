---
title: تنبؤات متطلبات الصيانة
description: يشرح هذا الموضوع تنبؤات متطلبات الصيانة في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderForecastToJournals, EntAssetWorkOrderForecast
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b5cf1a634ef5ab60707cf471ef017ec167e3013f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263652"
---
# <a name="maintenance-forecasts"></a><span data-ttu-id="5490a-103">تنبؤات متطلبات الصيانة</span><span class="sxs-lookup"><span data-stu-id="5490a-103">Maintenance forecasts</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="5490a-104">عندما تقوم بإنشاء أمر عمل، تقوم بإنشاء وظائف أمر عمل لديها أصول وأنواع مهام الصيانة ذات صلة.</span><span class="sxs-lookup"><span data-stu-id="5490a-104">When you create a work order, you create work order jobs that have related assets and maintenance job types.</span></span> <span data-ttu-id="5490a-105">وعندما تحدد نوع مهمة صيانة تحتوي على تنبؤات بمتطلبات الصيانة، يتم نسخ التنبؤات إلى أمر العمل بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="5490a-105">When you select a maintenance job type that contains maintenance forecasts, the forecasts are automatically copied to the work order.</span></span>

<span data-ttu-id="5490a-106">يمكنك إضافة بنود التنبؤ إلى أمر العمل أو حذفها من أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="5490a-106">You might be able to add forecast lines to a work order or delete them from a work order.</span></span> <span data-ttu-id="5490a-107">يحدد إعداد حالة دورة حياة أمر العمل ونوع المشروع المرتبط وقواعد المرحلة المرتبطة بنوع المشروع ما إذا كان باستطاعتك إضافة بنود تنبؤ أو تحريرها.</span><span class="sxs-lookup"><span data-stu-id="5490a-107">The setup of the work order lifecycle state, the related project type, and the stage rules that are related to the project type determine whether you can add or edit forecast lines.</span></span> <span data-ttu-id="5490a-108">لمزيد من المعلومات حول حالات دورة حياة أمر العمل ومراحل المشروع ذات الصلة، راجع [التنبؤات، أوامر العمل، والمشاريع](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span><span class="sxs-lookup"><span data-stu-id="5490a-108">For more information about work order lifecycle states and related project stages, see [Forecasts, work orders, and projects](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

1. <span data-ttu-id="5490a-109">حدد **إدارة الأصول** > **مشترك** > **أوامر العمل** > **جميع أوامر العمل** أو **أوامر العمل النشطة**.</span><span class="sxs-lookup"><span data-stu-id="5490a-109">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="5490a-110">حدد أمر العمل في القائمة، ثم جزء الإجراءات من علامة التبويب **أمر العمل** ، مجموعة **المشروع** ، حدد **التنبؤ**.</span><span class="sxs-lookup"><span data-stu-id="5490a-110">Select the work order in the list, and then, on the Action Pane > **Work order** tab > the **Project** group, select **Forecast**.</span></span> <span data-ttu-id="5490a-111">تُظهر صفحة **التنبؤ بمتطلبات صيانة أمر العمل** ، بنود التنبؤ من نوع مهمة الصيانة المحددة في وظيفة أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="5490a-111">The **Work order maintenance forecast** page shows forecast lines from the maintenance job type that is selected on the work order job.</span></span>


## <a name="add-an-hours-forecast-to-a-work-order"></a><span data-ttu-id="5490a-112">إضافة ساعات التنبؤ إلى أمر العمل</span><span class="sxs-lookup"><span data-stu-id="5490a-112">Add an hours forecast to a work order</span></span>

1. <span data-ttu-id="5490a-113">في صفحة **التنبؤ بمتطلبات صيانة أمر العمل** ، حدد وظيفة أمر العمل لإضافة تنبؤ اليه.</span><span class="sxs-lookup"><span data-stu-id="5490a-113">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

2. <span data-ttu-id="5490a-114">في علامة التبويب السريعة **الساعات** ، حدد **إضافة** لإنشاء بند جديد.</span><span class="sxs-lookup"><span data-stu-id="5490a-114">On the **Hours** FastTab, select **Add** to create a new line.</span></span>

3. <span data-ttu-id="5490a-115">حدد فئة في حقل **الفئة** .</span><span class="sxs-lookup"><span data-stu-id="5490a-115">In the **Category** field, select a category.</span></span>

4. <span data-ttu-id="5490a-116">أدخل عدد الساعات التي تم التنبؤ بها في حقل **الساعات** .</span><span class="sxs-lookup"><span data-stu-id="5490a-116">In the **Hours** field, enter the number of forecasted hours.</span></span>

5. <span data-ttu-id="5490a-117">في حقل **خاصية البند** ، حدد نوع المصاريف التي ينبغي استخدامها في البند.</span><span class="sxs-lookup"><span data-stu-id="5490a-117">In the **Line property** field, select the type of charge that should be used on the line.</span></span>


## <a name="add-an-items-forecast-to-a-work-order"></a><span data-ttu-id="5490a-118">إضافة تنبؤات الأصناف إلى أمر عمل</span><span class="sxs-lookup"><span data-stu-id="5490a-118">Add an items forecast to a work order</span></span>

<span data-ttu-id="5490a-119">توجد ثلاث طرق لإضافة أصناف إلى التنبؤ بمتطلبات صيانة أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="5490a-119">There are three ways to add items to a work order maintenance forecast.</span></span> <span data-ttu-id="5490a-120">يمكنك إنشاء بنود للأصناف (قطع الغيار) غير المضمنة في قائمة قطع الغيار أو قائمة مكونات صنف (BOM) الأصل، ويمكنك تحديد قطع غيار من قائمة قطع الغيار الموافق عليها، أو يمكنك تحديد أصناف من قائمة مكونات صنف (BOM) الأصل.</span><span class="sxs-lookup"><span data-stu-id="5490a-120">You can create lines for items (spare parts) that aren't included on the spare parts list or the asset bill of materials (BOM), you can select spare parts from the approved spare parts list, or you can select items from the asset BOM.</span></span>

- <span data-ttu-id="5490a-121">في صفحة **التنبؤ بمتطلبات صيانة أمر العمل** ، حدد وظيفة أمر العمل لإضافة تنبؤ اليه.</span><span class="sxs-lookup"><span data-stu-id="5490a-121">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

- <span data-ttu-id="5490a-122">في علامة التبويب السريعة‬ **الأصناف** ، أضف أصنافًا إلى التنبؤ بمتطلبات الصيانة باستخدام الطريقة المناسبة.</span><span class="sxs-lookup"><span data-stu-id="5490a-122">On the **Items** FastTab, add items to the maintenance forecast by using the appropriate method.</span></span>

<span data-ttu-id="5490a-123">لإنشاء بند جديد لقطعة غيار غير موجودة على قائمة قطع الغيار أو قائمة مكونات صنف (BOM) الأصل، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="5490a-123">To create a line for a spare part that isn't on the spare parts list or the asset BOM, follow these steps:</span></span>

1. <span data-ttu-id="5490a-124">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="5490a-124">Select **Add**.</span></span>
2. <span data-ttu-id="5490a-125">في الحقل **رقم الصنف**، حدد الصنف.</span><span class="sxs-lookup"><span data-stu-id="5490a-125">In the **Item number** field, select the item.</span></span>
3. <span data-ttu-id="5490a-126">في حقل **‏‫كمية المبيعات** ، أدخل الكمية.</span><span class="sxs-lookup"><span data-stu-id="5490a-126">In the **Sales quantity** field, enter the quantity.</span></span>
4. <span data-ttu-id="5490a-127">في حقل **الوحدة** ، حدد وحدة قياس الكمية.</span><span class="sxs-lookup"><span data-stu-id="5490a-127">In the **Unit** field, select the unit of measure for the quantity.</span></span>
5. <span data-ttu-id="5490a-128">في الحقلين **سعر التكلفة** و **العملة** ، أدخل القيم المناسبة.</span><span class="sxs-lookup"><span data-stu-id="5490a-128">In the **Cost price** and **Currency** fields, enter appropriate values.</span></span>
6. <span data-ttu-id="5490a-129">في حقل **خاصيه البند** ، حدد خاصية البند.</span><span class="sxs-lookup"><span data-stu-id="5490a-129">In the **Line property** field, select a line property.</span></span>
7. <span data-ttu-id="5490a-130">لتغيير قائمة الأبعاد المعروضة في بنود الصنف، حدد **المخزون** > **عرض الأبعاد**‬، ثم قم بتعيين الخيار **حفظ الإعداد** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="5490a-130">To change the list of dimensions that is shown on the item lines, select **Inventory** > **Display dimensions**, select the dimensions, and then set the **Save setup** option to **Yes**.</span></span>

<span data-ttu-id="5490a-131">لإضافة قطع غيار من قائمة قطع الغيار المعتمدة، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="5490a-131">To add a spare part from an approved spare parts list, follow these steps:</span></span>

1. <span data-ttu-id="5490a-132">حدد **إضافة قطع غيار**.</span><span class="sxs-lookup"><span data-stu-id="5490a-132">Select **Add spare parts**.</span></span>
2. <span data-ttu-id="5490a-133">حدد قطعه الغيار، وقم بتحرير المعلومات ذات الصلة كما طلبت.</span><span class="sxs-lookup"><span data-stu-id="5490a-133">Select the spare part, and edit the related information as you require.</span></span>
3. <span data-ttu-id="5490a-134">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5490a-134">Select **OK**.</span></span>

<span data-ttu-id="5490a-135">لإضافة صنف من قائمة مكونات صنف BOM الأصل، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="5490a-135">To add an item from the asset BOM, follow these steps:</span></span>

1. <span data-ttu-id="5490a-136">حدد **إضافة أصناف من قائمة مكونات الصنف**.</span><span class="sxs-lookup"><span data-stu-id="5490a-136">Select **Add BOM items**.</span></span>
2. <span data-ttu-id="5490a-137">حدد الصنف، وقم بتحرير المعلومات ذات الصلة كما طلبت.</span><span class="sxs-lookup"><span data-stu-id="5490a-137">Select the item, and edit the related information as you require.</span></span>
3. <span data-ttu-id="5490a-138">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5490a-138">Select **OK**.</span></span>

<span data-ttu-id="5490a-139">للحصول على نظرة عامة حول مكان استخدام الصنف على البند المحدد، بالنسبة إلى الأصول والإعدادات الافتراضية لنوع مهمة الصيانة وقطع الغيار وأوامر العمل في إدارة الأصول، حدد **مكان استخدام الصنف**.</span><span class="sxs-lookup"><span data-stu-id="5490a-139">To get an overview that shows where the item on the selected line is used in relation to assets, maintenance job type defaults, spare parts, and work orders in Asset Management, select **Item where used**.</span></span> <span data-ttu-id="5490a-140">لمزيد من المعلومات حول هذه النظرة العامة، راجع [الصنف المُستخدم](../controlling-and-reporting/item-where-used.md).</span><span class="sxs-lookup"><span data-stu-id="5490a-140">For more information about this overview, see [Item where used](../controlling-and-reporting/item-where-used.md).</span></span>


## <a name="add-an-expense-forecast-to-a-work-order"></a><span data-ttu-id="5490a-141">إضافة تنبؤ بالمصروفات إلى أمر عمل</span><span class="sxs-lookup"><span data-stu-id="5490a-141">Add an expense forecast to a work order</span></span>

1. <span data-ttu-id="5490a-142">في صفحة **التنبؤ بمتطلبات صيانة أمر العمل** ، حدد وظيفة أمر العمل لإضافة تنبؤ اليه.</span><span class="sxs-lookup"><span data-stu-id="5490a-142">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

2. <span data-ttu-id="5490a-143">في علامة التبويب السريعة **المصروفات** ، حدد **إضافة** لإنشاء بند.</span><span class="sxs-lookup"><span data-stu-id="5490a-143">On the **Expense** FastTab, select **Add** to create a line.</span></span>

3. <span data-ttu-id="5490a-144">حدد فئة في حقل **الفئة** .</span><span class="sxs-lookup"><span data-stu-id="5490a-144">In the **Category** field, select a category.</span></span>

4. <span data-ttu-id="5490a-145">في حقل **الكمية**، ثم أدخل الكمية.</span><span class="sxs-lookup"><span data-stu-id="5490a-145">In the **Quantity** field, enter the quantity.</span></span>

5. <span data-ttu-id="5490a-146">أدخل القيم المناسبة في الحقول **سعر التكلفة**، و **عملة المبيعات**، و **سعر المبيعات** .</span><span class="sxs-lookup"><span data-stu-id="5490a-146">In the **Cost price**, **Sales currency**, and **Sales price** fields, enter appropriate values.</span></span>

6. <span data-ttu-id="5490a-147">في حقل **خاصية البند** ، حدد نوع المصاريف التي ينبغي استخدامها في البند.</span><span class="sxs-lookup"><span data-stu-id="5490a-147">In the **Line property** field, select the type of charge that should be used on the line.</span></span>

>[!NOTE]
><span data-ttu-id="5490a-148">تُظهر علامة التبويب السريعة **إجمالي التنبؤات بمتطلبات الصيانة** ، نظرة عامة حول عدد البنود التي تم إنشاؤها، لوظيفة أمر العمل المحدد ولأمر العمل، على كل علامة تبويب سريعة.</span><span class="sxs-lookup"><span data-stu-id="5490a-148">The **Maintenance forecast totals** FastTab shows an overview of the number of lines that have been created, for the selected work order job and for the work order, on each FastTab.</span></span> <span data-ttu-id="5490a-149">كما يمكنك الاطلاع على إجمالي ساعات العمل التي تم التنبؤ بها لوظيفة أمر العمل ولأمر العمل.</span><span class="sxs-lookup"><span data-stu-id="5490a-149">It also shows the total forecasted work hours for the work order job and the work order.</span></span>

<span data-ttu-id="5490a-150">يوضح الرسم التوضيحي المبين أدناه مثال لصفحة **التنبؤ بمتطلبات صيانة أمر العمل‬**.</span><span class="sxs-lookup"><span data-stu-id="5490a-150">The illustration below shows an example of the **Work order maintenance forecast** page.</span></span>

![الشكل 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a><span data-ttu-id="5490a-152">التحديث التلقائي لتنبؤات أمر العمل</span><span class="sxs-lookup"><span data-stu-id="5490a-152">Automatic update of work order forecasts</span></span>

<span data-ttu-id="5490a-153">إذا تم تحديث تكاليف الساعة وتكاليف الأصناف والمصروفات في وحدات نمطية أخرى في Microsoft Dynamics 365 for Finance and Operations، يمكنك تحديث أي تغييرات في تنبؤات أوامر العمل في إدارة الأصول بشكل تلقائي لتعكس هذه التغييرات.</span><span class="sxs-lookup"><span data-stu-id="5490a-153">If hour costs, item costs, and expenses are updated in other modules in Microsoft Dynamics 365 for Finance and Operations, work order forecasts in Asset Management can automatically be updated to reflect those changes.</span></span> <span data-ttu-id="5490a-154">تساعد هذه الإمكانية على ضمان استخدام أحدث أسعار التكلفة في تنبؤات أوامر العمل في كل الأوقات.</span><span class="sxs-lookup"><span data-stu-id="5490a-154">This capability helps guarantee that the latest cost prices are always used in your work order forecasts.</span></span> <span data-ttu-id="5490a-155">ويمكنك أيضًا إجراء تحديثات مماثلة لـ [تنبؤات نوع مهمة الصيانة](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span><span class="sxs-lookup"><span data-stu-id="5490a-155">You can also do similar updates for [maintenance job type forecasts](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span></span>

1. <span data-ttu-id="5490a-156">حدد **إدارة الأصول** > **دوري** > **تنبؤ** > **تحديث تنبؤ بأمر العمل**.</span><span class="sxs-lookup"><span data-stu-id="5490a-156">Select **Asset management** > **Periodic** > **Forecast** > **Update work order forecast**.</span></span>

2. <span data-ttu-id="5490a-157">في مربع حوار **تحديث تنبؤ أمر العمل** ، على علامة التبويب السريع **‏‫السجلات المطلوب تضمينها‬** ، يمكنك إضافة تحديدات تتعلق بأوامر عمل أو وظائف أمر عمل معينة، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="5490a-157">In the **Update work order forecast** dialog, on the **Records to include** FastTab, you can add selections regarding specific work orders or work order jobs, as you require.</span></span> <span data-ttu-id="5490a-158">انقر فوق **عامل التصفية** لإجراء التحديدات ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="5490a-158">Click **Filter** to make the relevant selections.</span></span>

3. <span data-ttu-id="5490a-159">في علامة التبويب السريعة **تشغيل في الخلفية‬**، يمكنك إعداد التحديث التلقائي كوظيفة دفعية، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="5490a-159">On the **Run in the background** FastTab, you can set up the automatic update as a batch job, as you require.</span></span>

4. <span data-ttu-id="5490a-160">حدد **موافق** لبدء تحديث التنبؤ.</span><span class="sxs-lookup"><span data-stu-id="5490a-160">Select **OK** to start the forecast update.</span></span>


<span data-ttu-id="5490a-161">يوضح الرسم التوضيحي المبين أدناه مثال لمربع حوار **تحديث تنبؤ أمر العمل‬** .</span><span class="sxs-lookup"><span data-stu-id="5490a-161">The illustration below shows an example of the **Update work order forecast** dialog.</span></span>

![الشكل 2](media/07-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]