---
title: تنبؤات متطلبات الصيانة
description: يشرح هذا الموضوع تنبؤات متطلبات الصيانة في إدارة الأصول.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 383c910b40199f2da863144c6dc85a579d0091e9
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024489"
---
# <a name="maintenance-forecasts"></a><span data-ttu-id="6d200-103">تنبؤات متطلبات الصيانة</span><span class="sxs-lookup"><span data-stu-id="6d200-103">Maintenance forecasts</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="6d200-104">عندما تنشئ أمر عمل، تقوم بإنشاء وظائف أمر العمل مع الأصول وأنواع مهام الصيانة ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="6d200-104">When you create a work order, you create work order jobs with related assets and maintenance job types.</span></span> <span data-ttu-id="6d200-105">وعندما تحدد نوع مهمة صيانة تحتوي على تنبؤات بمتطلبات الصيانة، يتم نسخ التنبؤات إلى أمر العمل بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="6d200-105">When you select a maintenance job type containing maintenance forecasts, the forecasts are automatically copied to the work order.</span></span>

<span data-ttu-id="6d200-106">قد تتمكن من إضافة أو حذف بنود التنبؤ في أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="6d200-106">You may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="6d200-107">يحدد إعداد حالة دورة حياة أمر العمل ونوع المشروع المرتبط وقواعد المرحلة المرتبطة بنوع المشروع ما إذا كان باستطاعتك إضافة بنود التنبؤ أو تحريرها.</span><span class="sxs-lookup"><span data-stu-id="6d200-107">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determines if you are able to add or edit forecast lines.</span></span> 

1. <span data-ttu-id="6d200-108">انقر فوق **إدارة الأصول** > **عام** > **أوامر العمل** > **جميع أوامر العمل** أو **أوامر العمل النشطة**.</span><span class="sxs-lookup"><span data-stu-id="6d200-108">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="6d200-109">حدد أمر العمل في القائمة، وانقر فوق **تنبؤ**.</span><span class="sxs-lookup"><span data-stu-id="6d200-109">Select the work order in the list, and click **Forecast**.</span></span> <span data-ttu-id="6d200-110">في **التنبؤ بمتطلبات صيانة أمر العمل**، تظهر بنود التنبؤ من نوع مهمة الصيانة المحددة في وظيفة أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="6d200-110">In **Work order maintenance forecast**, forecast lines from the maintenance job type selected on the work order job are displayed.</span></span>


## <a name="add-hours-forecast-to-a-work-order"></a><span data-ttu-id="6d200-111">أضافه التنبؤ بالساعات إلى أمر عمل</span><span class="sxs-lookup"><span data-stu-id="6d200-111">Add hours forecast to a work order</span></span>

1. <span data-ttu-id="6d200-112">حدد وظيفة أمر العمل التي تريد إضافة تنبؤ اليها.</span><span class="sxs-lookup"><span data-stu-id="6d200-112">Select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="6d200-113">في علامة التبويب السريعة **الساعات**، انقر فوق **إضافة** لإنشاء بند جديد.</span><span class="sxs-lookup"><span data-stu-id="6d200-113">On the **Hours** FastTab, click **Add** to create a new line.</span></span>

3. <span data-ttu-id="6d200-114">حدد فئة في حقل **الفئة**.</span><span class="sxs-lookup"><span data-stu-id="6d200-114">Select a category in the **Category** field.</span></span>

4. <span data-ttu-id="6d200-115">أدخل عدد الساعات التي تم التنبؤ بها في حقل **الساعات**.</span><span class="sxs-lookup"><span data-stu-id="6d200-115">Insert number of forecasted hours in the **Hours** field.</span></span>

5. <span data-ttu-id="6d200-116">في حقل **خاصية البند**، حدد نوع المصاريف التي سيتم استخدامها في البند.</span><span class="sxs-lookup"><span data-stu-id="6d200-116">In the **Line property** field, select the charge type to be used on the line.</span></span>


## <a name="add-items-forecast-to-a-work-order"></a><span data-ttu-id="6d200-117">أضافه التنبؤ بالأصناف إلى أمر عمل</span><span class="sxs-lookup"><span data-stu-id="6d200-117">Add items forecast to a work order</span></span>

<span data-ttu-id="6d200-118">توجد ثلاث طرق لإضافة أصناف إلى التنبؤ بمتطلبات صيانة أمر عمل: يمكنك إنشاء بنود للأصناف (قطع الغيار) غير المضمنة في قائمه قطع الغيار أو BOM الأصل، ويمكنك تحديد قطع غيار من قائمة قطع الغيار الموافق عليها ويمكنك تحديد أصناف من BOM الأصل.</span><span class="sxs-lookup"><span data-stu-id="6d200-118">There are three ways to add items to a work order maintenance forecast: You can create lines for items (spare parts) that are not included in the spare parts list or asset BOM, you can select spare parts from the approved spare parts list, and you can select items from the asset BOM.</span></span>

1. <span data-ttu-id="6d200-119">حدد وظيفة أمر العمل التي تريد إضافة تنبؤ اليها.</span><span class="sxs-lookup"><span data-stu-id="6d200-119">Select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="6d200-120">حدد علامة التبويب السريعة **الأصناف‬**.</span><span class="sxs-lookup"><span data-stu-id="6d200-120">Select the **Items** FastTab.</span></span>

3. <span data-ttu-id="6d200-121">انقر فوق **إضافة** لإنشاء بند جديد لقطعة غيار غير موجودة على قائمة قطع الغيار أو BOM الأصل.</span><span class="sxs-lookup"><span data-stu-id="6d200-121">Click **Add** to create a new line for a spare part that is not on the spare parts list or the asset BOM list.</span></span>

4. <span data-ttu-id="6d200-122">في الحقل **رقم الصنف**، حدد الصنف.</span><span class="sxs-lookup"><span data-stu-id="6d200-122">Select the item in the **Item number** field.</span></span>

5. <span data-ttu-id="6d200-123">أدخل كمية في حقل **كمية المبيعات**، ثم حدد وحدة الكمية في الحقل **الوحدة**</span><span class="sxs-lookup"><span data-stu-id="6d200-123">Insert quantity in the **Sales quantity** field, and select a quantity unit in the **Unit** field.</span></span>

6. <span data-ttu-id="6d200-124">أدخل سعر التكلفة والعملة في الحقول ذات الصلة، وحدد **خاصية البند**.</span><span class="sxs-lookup"><span data-stu-id="6d200-124">Insert cost price and currency in the relevant fields, and select a **Line property**.</span></span>

7. <span data-ttu-id="6d200-125">إذا أردت تغيير قائمة الأبعاد المعروضة في بنود الصنف، انقر فوق **المخزون** > **عرض الأبعاد‬**، حدد الأبعاد وحدد "نعم" على زر التبديل **حفظ الإعداد**.</span><span class="sxs-lookup"><span data-stu-id="6d200-125">If you want to change the list of dimensions displayed on the item lines, click **Inventory** > **Display dimensions**, select the dimensions, and select "Yes" on the **Save setup** toggle button.</span></span>

8. <span data-ttu-id="6d200-126">إذا أردت إضافة قطعة غيار موافق عليها إلى التنبؤ بمتطلبات الصيانة، فانقر فوق **إضافة قطع غيار**، وحرر المعلومات ذات الصلة إذا لزم الأمر، وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="6d200-126">If you want to add an approved spare part to the maintenance forecast, click **Add spare parts**, select the spare part, edit related information if required, and click **OK**.</span></span>

9. <span data-ttu-id="6d200-127">إذا أردت إضافة أصناف BOM إلى التنبؤ، فانقر فوق **إضافة أصناف BOM**، وحدد الصنف، ثم حرر المعلومات ذات الصلة إذا لزم الأمر، وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="6d200-127">If you want to add asset BOM items to the forecast, click **Add BOM items**, select the item, edit related information if required, and click **OK**.</span></span>

10. <span data-ttu-id="6d200-128">انقر فوق **مكان استخدام الصنف** للحصول على نظرة عامة حول المكان في إدارة الأصول حيث يتم استخدام الصنف على البند المحدد، بالنسبة إلى الأصول والإعدادات الافتراضية لنوع الوظيفة وقطع الغيار وأوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="6d200-128">Click **Item where used** if you want to get an overview of where the item on the selected line is used in Asset Management in relation to assets, maintenance job type defaults, spare parts, and work orders.</span></span> 



## <a name="add-expense-forecast-to-a-work-order"></a><span data-ttu-id="6d200-129">أضافه التنبؤ بالمصروفات إلى أمر عمل</span><span class="sxs-lookup"><span data-stu-id="6d200-129">Add expense forecast to a work order</span></span>

1. <span data-ttu-id="6d200-130">يوضح هذا الموضوع كيفية إضافة تنبؤ بالمصروفات إلى أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="6d200-130">This topic explains how to add an expense forecast to a work order.</span></span> <span data-ttu-id="6d200-131">في الجانب الأيسر من النموذج، حدد وظيفة أمر العمل التي ترغب في إضافة تنبؤ اليها.</span><span class="sxs-lookup"><span data-stu-id="6d200-131">In the left-hand side of the form, select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="6d200-132">حدد علامة التبويب السريعة **المصروفات‬**.</span><span class="sxs-lookup"><span data-stu-id="6d200-132">Select the **Expense** FastTab.</span></span>

3. <span data-ttu-id="6d200-133">انقر فوق **‘إضافة** لإنشاء بند جديد.</span><span class="sxs-lookup"><span data-stu-id="6d200-133">Click **Add** to create a new line.</span></span>

4. <span data-ttu-id="6d200-134">حدد فئة في حقل **الفئة**.</span><span class="sxs-lookup"><span data-stu-id="6d200-134">Select a category in the **Category** field.</span></span>

5. <span data-ttu-id="6d200-135">أدخل الكمية في حقل **الكمية**.</span><span class="sxs-lookup"><span data-stu-id="6d200-135">Insert quantity in the **Quantity** field.</span></span>

6. <span data-ttu-id="6d200-136">أدخل سعر التكلفة وعملة المبيعات وسعر المبيعات في الحقول ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="6d200-136">Insert cost price, sales currency, and sales price in the relevant fields.</span></span>

7. <span data-ttu-id="6d200-137">في حقل **خاصية البند**، حدد نوع المصاريف التي سيتم استخدامها في البند.</span><span class="sxs-lookup"><span data-stu-id="6d200-137">In the **Line property** field, select the charge type to be used on the line.</span></span>

>[!NOTE]
><span data-ttu-id="6d200-138">على علامة التبويب السريعة **إجمالي التنبؤات بمتطلبات الصيانة**، يمكنك عرض نظرة عامة حول عدد البنود التي تم إنشاؤها في كل علامة تبويب، لوظيفة أمر العمل المحددة ولأمر العمل.</span><span class="sxs-lookup"><span data-stu-id="6d200-138">On the **Maintenance forecast totals** FastTab, you can see an overview of the number of lines created on each tab, for the selected work order job and for the work order.</span></span> <span data-ttu-id="6d200-139">كما يمكنك الاطلاع على مجموع ساعات العمل التي تم التنبؤ بها لوظيفة أمر العمل ولأمر العمل.</span><span class="sxs-lookup"><span data-stu-id="6d200-139">Also, you can see a sum of forecasted work hours for the work order job and for the work order.</span></span>

![الشكل 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a><span data-ttu-id="6d200-141">التحديث التلقائي لتنبؤات أمر العمل</span><span class="sxs-lookup"><span data-stu-id="6d200-141">Automatic update of work order forecasts</span></span>

<span data-ttu-id="6d200-142">في إدارة الأصول، يمكنك تحديث أي تغييرات في تنبؤات أوامر العمل بشكل تلقائي فيما يتعلق بتكاليف الساعة وتكاليف الأصناف والمصروفات، التي تم تحديثها في وحدات نمطية أخرى.</span><span class="sxs-lookup"><span data-stu-id="6d200-142">In Asset Management, you can automatically update any changes in work order forecasts regarding hour costs, item costs, and expenses, which have been updated in other modules.</span></span> <span data-ttu-id="6d200-143">يتم ذلك للتأكد من استخدام أحدث أسعار التكلفة في تنبؤات أوامر العمل في كل الأوقات.</span><span class="sxs-lookup"><span data-stu-id="6d200-143">This is done to ensure that the latest cost prices are always used in your work order forecasts.</span></span> <span data-ttu-id="6d200-144">ويمكن أيضًا إجراء تحديثات مماثلة [لتنبؤات أنواع مهام الصيانة](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span><span class="sxs-lookup"><span data-stu-id="6d200-144">It is also possible to make similar updates for [maintenance job type forecasts](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span></span>

1. <span data-ttu-id="6d200-145">انقر فوق **إدارة الأصول** > **دوري** > **تنبؤ** > **تحديث تنبؤ أمر العمل**.</span><span class="sxs-lookup"><span data-stu-id="6d200-145">Click **Asset management** > **Periodic** > **Forecast** > **Update work order forecast**.</span></span>

2. <span data-ttu-id="6d200-146">في مربع حوار القائمة المنسدلة **تحديث تنبؤ أمر العمل**، يمكنك إضافة تحديدات تتعلق بأوامر عمل أو وظائف أمر عمل معينة، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="6d200-146">In the **Update work order forecast** drop-down dialog, you can add selections regarding specific work orders or work order jobs, if required.</span></span> <span data-ttu-id="6d200-147">انقر **تصفية** لإجراء تلك التحديدات.</span><span class="sxs-lookup"><span data-stu-id="6d200-147">Click **Filter** to make those selections.</span></span>

3. <span data-ttu-id="6d200-148">على علامة التبويب السريعة **تشغيل في الخلفية‬**، يمكنك إعداد التحديث التلقائي كوظيفة دفعية، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="6d200-148">If required, you can set up the automatic update as a batch job on the **Run in the background** FastTab.</span></span>

4. <span data-ttu-id="6d200-149">انقر فوق **موافق** لبدء تحديث التنبؤ.</span><span class="sxs-lookup"><span data-stu-id="6d200-149">Click **OK** to start the forecast update.</span></span>


![الشكل 2](media/07-work-orders.png)

