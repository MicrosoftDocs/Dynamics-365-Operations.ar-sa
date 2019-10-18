---
title: خطط الصيانة المجدولة
description: يشرح هذا الموضوع كيفية جدولة خطط الصيانة في إدارة الأصول.
author: josaw1
manager: AnnBe
ms.date: 08/27/2019
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
ms.openlocfilehash: 698888533bf503838f455585f61cc7afc7239b05
ms.sourcegitcommit: 6476f27c8d3dced7c2e9a7344a4e378b51a1983e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/27/2019
ms.locfileid: "1922035"
---
# <a name="schedule-maintenance-plans"></a><span data-ttu-id="35031-103">خطط الصيانة المجدولة</span><span class="sxs-lookup"><span data-stu-id="35031-103">Schedule maintenance plans</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="35031-104">تقوم جدوله الصيانة الوقائية بإنشاء إدخالات التقويم على الأصول، استنادًا إلى إعداد خطط الصيانة على الأصول.</span><span class="sxs-lookup"><span data-stu-id="35031-104">Preventive maintenance scheduling generates calendar entries on assets, based on the maintenance plans set up on the assets.</span></span> <span data-ttu-id="35031-105">يمكنك جدوله إدخالات التقويم استنادًا إلى خطط الصيانة وأنواع الأصول والأصول المحددة.</span><span class="sxs-lookup"><span data-stu-id="35031-105">You can schedule calendar entries based on selected maintenance plans, asset types, and assets.</span></span>

1. <span data-ttu-id="35031-106">انقر فوق **إدارة الأصول** > **دوري** > **الصيانة الوقائية** > **جدولة خطط الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="35031-106">Click **Asset management** > **Periodic** > **Preventive maintenance** > **Schedule maintenance plans**.</span></span>

2. <span data-ttu-id="35031-107">يمكنك تحديد فترة زمنية في حقلي **الفترة** و**تكرار الفترة**.</span><span class="sxs-lookup"><span data-stu-id="35031-107">You can select a time interval in the **Period** and **Period frequency** fields.</span></span>

>[!NOTE]
><span data-ttu-id="35031-108">يشير حقلا **الفترة** و**تكرار الفترة** إلى فترة الوقت التي التي تريد فيها إنشاء بنود جدولة الصيانة قبل الفترة المحددة، استنادًا إلى خطط الصيانة التي أنشأتها (استنادًا إلى الوقت أو استنادًا إلى العداد).</span><span class="sxs-lookup"><span data-stu-id="35031-108">The **Period** and **Period frequencey** fields indicate how far ahead in time you want maintenance schedule lines to be created, based on the maintenance plans you have created (time-based or counter-based).</span></span> <span data-ttu-id="35031-109">في الشكل الموجود أدناه، يتم إنشاء بنود جدول الصيانة (= مقترحات أمر العمل) من التاريخ الحالي ولمدة ثلاثة أشهر بعده.</span><span class="sxs-lookup"><span data-stu-id="35031-109">In the figure below, maintenance schedule lines (= work order proposals) are created from the current date and three months onwards.</span></span>

3. <span data-ttu-id="35031-110">حدد "نعم" على زر التبديل **إنشاء تلقائي إذا كان محددًا في البند** إذا كان ينبغي إنشاء أوامر العمل تلقائيًا وفقًا لبند خطة الصيانة.</span><span class="sxs-lookup"><span data-stu-id="35031-110">Select "Yes" on the **Auto create if specified in the line** toggle button if work orders should automatically be created according to the maintenance plan line.</span></span>

>[!NOTE]
><span data-ttu-id="35031-111">إذا تم تعيين زر التبديل هذا إلى "نعم" **و** تم أيضًا تحديد خانة الاختيار *إنشاء تلقائي* على بنود خطط الصيانة في **خطط الصيانة**، فسيتم أيضًا إنشاء أوامر العمل استنادًا إلى بنود خطط الصيانة وبنود جدول الصيانة مع الحالة "تم إنشاء أمر العمل".</span><span class="sxs-lookup"><span data-stu-id="35031-111">If this toggle button is set to "Yes", *and* the **Auto create** check box is also selected on maintenance plan lines in **Maintenance plans**, work orders are created based on the maintenance plan lines, and maintenance schedule lines with status "Work order created" are also created.</span></span> <span data-ttu-id="35031-112">في حالة تحديد خيار واحد فقط (زر التبديل **إنشاء تلقائي إذا كان محددًا في البند‬‏‫** في مربع الحوار هذا أو خانة الاختيار **إنشاء تلقائي** في نموذج **خطط الصيانة**)، يتم إنشاء بنود جدول الصيانة فقط مع الحالة "تم الإنشاء".</span><span class="sxs-lookup"><span data-stu-id="35031-112">If only one option is selected (**Auto create if specified in the line** toggle button in this dialog or **Auto create** check box in **Maintenance plans** form), only maintenance schedule lines are created with status "Created".</span></span> <span data-ttu-id="35031-113">في هذه الحالة، لا يتم إنشاء أوامر عمل.</span><span class="sxs-lookup"><span data-stu-id="35031-113">In that case, no work orders are created.</span></span>

4. <span data-ttu-id="35031-114">يمكن إنشاء إدخالات التقويم استنادًا إلى خطط الصيانة (الوقت والعداد) والأصول وأنواع الأصول ومواقع العمل وأنواع مواقع العمل.</span><span class="sxs-lookup"><span data-stu-id="35031-114">It is possible to generate calendar entries based on maintenance plans (time or counter), assets, asset types, functional locations, and functional location types.</span></span> <span data-ttu-id="35031-115">انقر فوق الزر **تصفية** وقم بإجراء تحديداتك، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="35031-115">Click the **Filter** button and make your selections, if required.</span></span>

- <span data-ttu-id="35031-116">فيما يتعلق بجدولة خطط الصيانة أو مواقع العمل، إذا قمت بتحديث إعداد أنواع الأصول والشركات المصنعة للأصول ونماذج الأصول على خطط الأصول في **جميع مواقع العمل** > علامة التبويب السريعة **خطط الصيانة** بعد جدولة خطط الصيانة، سيتم حذف إدخالات جدول الصيانة المتعلقة بموقع العمل هذا بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="35031-116">Regarding scheduling of maintenance plans on functional locations: If you update the setup of asset types, manufacturers, and models on maintenance plans in **All functional locations** > **Maintenance plans** FastTab after you have scheduled maintenance plans, existing maintenance schedule entries related to that functional location are automatically deleted.</span></span> <span data-ttu-id="35031-117">لإنشاء إدخالات تقويم جديدة، تتوافق مع إعداد خطة الصيانة المحدثة على موقع العمل، يجب تشغيل جدول خطة صيانة جديد لموقع العمل هذا.</span><span class="sxs-lookup"><span data-stu-id="35031-117">In order to create new calendar entries, which correspond with the updated maintenance plan setup on the functional location, you must run a new maintenance plan schedule for that functional location.</span></span> <span data-ttu-id="35031-118">اقرأ المزيد حول إعداد أنواع الأصول والشركات المصنعة والنماذج في مواقع العمل في [إنشاء مواقع عمل](../functional-locations/create-functional-locations.md).</span><span class="sxs-lookup"><span data-stu-id="35031-118">Read more about the setup of asset types, manufacturers, and models on functional locations in [Create functional locations](../functional-locations/create-functional-locations.md).</span></span>

><span data-ttu-id="35031-119">*مثال:* ترغب في إنشاء خطة صيانة لموقع عمل معين، مما يعني أنه سيتم تضمين جميع الأصول التي يتم إعدادها على موقع العمل هذا في وقت معين عندما تقوم بجدولة خطة الصيانة.</span><span class="sxs-lookup"><span data-stu-id="35031-119">*Example:* You want to create a maintenance plan for a specific functional location, meaning all assets set up on that functional location at any given time will be included when you schedule the maintenance plan.</span></span> <span data-ttu-id="35031-120">وفي هذه الحالة، يمكنك إنشاء خطة صيانة وتحديد موقع العمل المعين، ولكن "من دون" إضافة أي أصول في خطة الصيانة.</span><span class="sxs-lookup"><span data-stu-id="35031-120">In that case, you create a maintenance plan and select the specific functional location, but you do NOT add any assets in the maintenance plan.</span></span> <span data-ttu-id="35031-121">والنتيجة هي أنك عندما تجدول خطة الصيانة هذه، سيتم إنشاء بنود جدول الصيانة لجميع الأصول ذات الصلة بموقع العمل في في ذلك الوقت.</span><span class="sxs-lookup"><span data-stu-id="35031-121">The result is that when you schedule that maintenance plan, maintenance schedule lines will be created for all the assets related to the functional location at that time.</span></span>

- <span data-ttu-id="35031-122">إذا قمت بإجراء تغييرات على أنواع الأصول والشركات المصنعة والنماذج في **أنواع الأصول**، فإن هذه التغييرات تؤثر فقط على الأصول الجديدة التي تستخدم نوع الأصل الذي تم تحديثه.</span><span class="sxs-lookup"><span data-stu-id="35031-122">If you make changes to asset types, manufacturers and models in **Asset types**, those changes only affect new assets that use the updated asset type.</span></span> <span data-ttu-id="35031-123">أقرا المزيد حول إعداد نوع الأصل في [أنواع الأصول](../setup-for-objects/object-types.md).</span><span class="sxs-lookup"><span data-stu-id="35031-123">Read more about asset type setup in [Asset types](../setup-for-objects/object-types.md).</span></span>  

5. <span data-ttu-id="35031-124">انقر فوق **موافق** لبدء إنشاء إدخالات جدول الصيانة على الأصول.</span><span class="sxs-lookup"><span data-stu-id="35031-124">Click **OK** to start the generation of maintenance schedule entries on assets.</span></span> <span data-ttu-id="35031-125">ستظهر الإدخالات المُنشأة في صفحة قائمة **جدول الصيانة بكامله**.</span><span class="sxs-lookup"><span data-stu-id="35031-125">The generated entries will be shown in the **All maintenance schedule** list page.</span></span> <span data-ttu-id="35031-126">يبين الرسم التوضيحي التالي مثالاً لمربع حوار **‏‫خطط الصيانة المجدولة‬**.</span><span class="sxs-lookup"><span data-stu-id="35031-126">The following illustration shows an example of the **Schedule maintenance plans** dialog.</span></span>

![الشكل 1](media/09-preventive-maintenance.png)

- <span data-ttu-id="35031-128">في مربع الحوار **جدولة خطط الصيانة**، يمكنك إعداد وظائف دفعية على علامة التبويب السريعة **تشغيل في الخلفية** لإنشاء إدخالات التقويم تلقائيًا في فترات زمنية منتظمة.</span><span class="sxs-lookup"><span data-stu-id="35031-128">In the **Schedule maintenance plans** dialog, you can set up batch jobs on the **Run in the background** FastTab to automatically generate calendar entries at regular intervals.</span></span>  
- <span data-ttu-id="35031-129">عندما تقوم بجدولة الصيانة الوقائية، لن يتم إنشاء بنود جدول الصيانة ذات تاريخ ووقت بدء متوقعين أبكر من تاريخ ووقت النظام.</span><span class="sxs-lookup"><span data-stu-id="35031-129">When you schedule preventive maintenance, maintenance schedule lines with expected start date and time earlier than the system date and time will not be created.</span></span>  

<span data-ttu-id="35031-130">يوفر الشكل أدناه رسمًا توضيحيًا لحساب خطة الصيانة المستندة إلى الوقت.</span><span class="sxs-lookup"><span data-stu-id="35031-130">The figure below provides a graphic illustration of a time-based maintenance plan calculation.</span></span>  

![الشكل 2](media/10-preventive-maintenance.jpg)

<span data-ttu-id="35031-132">فيما يتعلق بخطط الصيانة التي تعتمد على العدادات: في الأرقام أدناه، يتم عرض دورتي تسجيل مختلفتين للعداد.</span><span class="sxs-lookup"><span data-stu-id="35031-132">Regarding counter-based maintenance plans: In the figures below, two different counter registration cycles are shown.</span></span> <span data-ttu-id="35031-133">وهما تستندان إلى خطة صيانة تم إعدادها للأصل "V0001"، حيث من المتوقع أن يقطع الأصل (سيارة) مسافة تبلغ حوالي 2,000 كيلومتر كل شهر.</span><span class="sxs-lookup"><span data-stu-id="35031-133">They are based on a maintenance plan set up for asset "V0001", expecting the asset (a car) to run approx. 2,000 km every month.</span></span>

<span data-ttu-id="35031-134">في المثال الأول، لا يتم بلوغ مسافة 2,000 كيلومتر المتوقعة كل شهر.</span><span class="sxs-lookup"><span data-stu-id="35031-134">In the first example, the expected 2,000 km are not reached every month.</span></span> <span data-ttu-id="35031-135">وفقًا لخطة الصيانة التي تعتمد على العداد، الحد المعين هو 2,000 كيلومتر، مما يعني أنك عندما تقوم بتشغيل جدولة خطة صيانة، يجب إنشاء بند جدول صيانة في كل مرة يتم فيها الوصول إلى حد 2,000 كيلومتر.</span><span class="sxs-lookup"><span data-stu-id="35031-135">According to the counter-based maintenance plan, the threshold is 2,000 km, meaning when you run a maintenance plan scheduling, a maintenance schedule line should be created each time the 2,000-kilometer threshold is reached.</span></span> <span data-ttu-id="35031-136">في المثال 1، توجد 4 بنود تسجيل ولكن تم بلوغ الحد المعين وهو 2,000 كيلومتر مرة واحدة فقط.</span><span class="sxs-lookup"><span data-stu-id="35031-136">In example 1, there are 4 registration lines, but the 2,000-kilometer threshold is only reached once.</span></span> <span data-ttu-id="35031-137">وهذا يعني أنك عندما تقوم بتشغيل خطط صيانة مجدولة لهذا الأصل، على سبيل المثال لفترة ثلاثة أشهر، سيتم نشاء بند واحد فقط لجدول الصيانة.</span><span class="sxs-lookup"><span data-stu-id="35031-137">This means that when you run schedule maintenance plans this asset, for example for a 3-month period, only one maintenance schedule line will be created.</span></span>

<span data-ttu-id="35031-138">في الشكل التالي، يتم تسجيل 2,000 كيلومتر أو أكثر كل شهر.</span><span class="sxs-lookup"><span data-stu-id="35031-138">In the next figure, 2,000 km or more are registered every month.</span></span> <span data-ttu-id="35031-139">وبالتالي، التالي إنشاء ثلاثة بنود صيانة إذا قمت بجدولة خطط الصيانة لهذا الأصل لفترة 3 أشهر.</span><span class="sxs-lookup"><span data-stu-id="35031-139">Therefore, three maintenance lines would be created if you schedule maintenance plans for this asset for a 3-month period.</span></span> 

<span data-ttu-id="35031-140">توضح الأمثلة الموضحة هنا أن جميع تسجيلات العداد التي تمت على أحد الأصول تظهر اتجاهًا يصف مدى استهلاك الأصل.</span><span class="sxs-lookup"><span data-stu-id="35031-140">The examples described here show that all counter registrations made on an asset show a trend describing wear and tear on the asset.</span></span> <span data-ttu-id="35031-141">يُستخدم هذا الاتجاه كأساس حساب عند جدولة خطة الصيانة.</span><span class="sxs-lookup"><span data-stu-id="35031-141">That trend is used as calculation basis at the time of maintenance plan scheduling.</span></span>

![الشكل 3](media/11-preventive-maintenance.png)

![الشكل 4](media/12-preventive-maintenance.png)

