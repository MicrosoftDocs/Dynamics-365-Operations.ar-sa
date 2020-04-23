---
title: التنبؤات وأوامر العمل والمشاريع
description: يشرح هذا الموضوع التنبؤات وتكامل أمر العمل مع الوحدة النمطية "إدارة المشاريع ومحاسبتها" في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 08/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3a55564875afa9125ee0dbb808a514f7b4b17b0b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205312"
---
# <a name="forecasts-work-orders-and-projects"></a><span data-ttu-id="27519-103">التنبؤات وأوامر العمل والمشاريع</span><span class="sxs-lookup"><span data-stu-id="27519-103">Forecasts, work orders, and projects</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="27519-104">في إدارة الأصول، يساعد التكامل مع الوحدة النمطية **إدارة المشاريع ومحاسبتها** على تحسين مراقبة التكاليف‬ مما يسمح للمستخدمين بتعقب التكاليف على تنبؤات أنواع مهام الصيانة ووظائف أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="27519-104">In Asset Management, integration with the **Project management and accounting** module helps optimize cost control, so that users can track costs on maintenance job type forecasts and work order jobs.</span></span>

<span data-ttu-id="27519-105">يحتاج تتبع تنبؤات أنواع مهام الصيانة إلى إعدادين:</span><span class="sxs-lookup"><span data-stu-id="27519-105">Tracking of maintenance job type forecasts requires two settings:</span></span>

1. <span data-ttu-id="27519-106">حدد مشروعًا في **إدارة الأصول** > **الإعداد** > **محددات إدارة الأصول‬**، ثم على علامة تبويب **الأصول‬‏‎** > على علامة التبويب السريعة **المشروع**، في حقل **مشروع التنبؤ بمتطلبات الصيانة**، حدد مشروعًا.</span><span class="sxs-lookup"><span data-stu-id="27519-106">Select a project in **Asset management** > **Setup** > **Asset management parameters**, and then, on the **Assets** tab > on the **Project** FastTab, in the **Maintenance forecast project** field, select a project.</span></span>

2. <span data-ttu-id="27519-107">عندما تنشئ بندًا افتراضيًا لنوع مهمة الصيانة، يتم إنشاء رقم نشاط للبند بشكل تلقائي في صفحة **الإعدادات الافتراضية لأنواع مهام الصيانة‬‏‫** (**إدارة الأصول** > **الإعداد** > **المهام** > **الإعدادات الافتراضية لأنواع مهام الصيانة**).</span><span class="sxs-lookup"><span data-stu-id="27519-107">When you create a maintenance job type default line, an activity number is automatically created for the line on the **Maintenance job type defaults** page (**Asset management** > **Setup** > **Jobs** > **Maintenance job type defaults**).</span></span>

<span data-ttu-id="27519-108">تساعد تنبؤات أنواع مهام الصيانة في تحقيق غرضين:</span><span class="sxs-lookup"><span data-stu-id="27519-108">Maintenance job type forecasts serve two purposes:</span></span> 

- <span data-ttu-id="27519-109">يمكنك تتبع التكاليف في تنبؤات أنواع مهام الصيانة في الوحدة النمطية **إدارة المشاريع ومحاسبتها**.</span><span class="sxs-lookup"><span data-stu-id="27519-109">You can track costs on maintenance job type forecasts in the **Project management and accounting** module.</span></span> 
- <span data-ttu-id="27519-110">تُنقل التنبؤات بشكل تلقائي إلى مشروع وظيفة أمر عمل عند تحديد نوع مهمة صيانة على وظيفة أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="27519-110">Forecasts are automatically transferred to a work order job project when you select a maintenance job type on a work order job.</span></span>

<span data-ttu-id="27519-111">لتتبع التكاليف على وظائف أوامر العمل، يجب أولاً إعداد مشاريع أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="27519-111">To track costs on work order jobs, you must first set up work order projects.</span></span> <span data-ttu-id="27519-112">لمزيد من المعلومات، راجع [إعداد مشروع أمر العمل](../setup-for-work-orders/work-order-project-setup.md).</span><span class="sxs-lookup"><span data-stu-id="27519-112">For more information, see [Work order project setup](../setup-for-work-orders/work-order-project-setup.md).</span></span>

## <a name="work-order-job-projects"></a><span data-ttu-id="27519-113">مشاريع وظائف أمر العمل</span><span class="sxs-lookup"><span data-stu-id="27519-113">Work order job projects</span></span>

<span data-ttu-id="27519-114">عند إنشاء وظيفة أمر عمل على أمر عمل، يتحدد مشروع أمر العمل بواسطة إعداد المشروع الرئيسي لأوامر العمل في صفحة **إعداد مشروع أمر العمل** (**إدارة الأصول** > **الإعداد‏‎** > **أوامر العمل** > **إعداد المشروع**).</span><span class="sxs-lookup"><span data-stu-id="27519-114">When you create a work order job on a work order, the work order project is determined by the setup of the parent project for work orders on the **Work order project setup** page (**Asset management** > **Setup** > **Work orders** > **Project setup**).</span></span>

<span data-ttu-id="27519-115">يتم إنشاء مشاريع وظائف أمر العمل باستخدام تركيبة من معلومات أمر العمل التالية:</span><span class="sxs-lookup"><span data-stu-id="27519-115">Work order job projects are created by using a combination of the following work order information:</span></span>

- <span data-ttu-id="27519-116">نوع أمر العمل المحدد على أمر العمل</span><span class="sxs-lookup"><span data-stu-id="27519-116">The work order type selected on the work order</span></span> 
- <span data-ttu-id="27519-117">موقع العمل المرتبط بالأصل على وظيفة أمر العمل</span><span class="sxs-lookup"><span data-stu-id="27519-117">The functional location related to the asset on the work order job</span></span>
- <span data-ttu-id="27519-118">نوع الأصل المرتبط بالأصل على وظيفة أمر العمل</span><span class="sxs-lookup"><span data-stu-id="27519-118">The asset type that is related to the asset on the work order job</span></span>  
- <span data-ttu-id="27519-119">وقت البدء والانتهاء المتوقعين المحددين على أمر العمل</span><span class="sxs-lookup"><span data-stu-id="27519-119">The expected start and end times that are set on the work order</span></span>  

<span data-ttu-id="27519-120">قد لا يتم العثور على بعض هذه المعلومات في أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="27519-120">Some of this information might not be found on a work order.</span></span> <span data-ttu-id="27519-121">وبالتالي، يتم البحث عن المشروع الرئيسي لأمر العمل باستخدام التركيبات المتوفرة من البيانات وتحديد معرف المشروع الذي يتوافق مع بيانات أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="27519-121">Therefore, the search for a work order parent project is done by using the available combination of data and selecting the project ID that corresponds to work order data.</span></span>

<span data-ttu-id="27519-122">على سبيل المثال، في الشكل التوضيحي التالي، وبسبب الطريقة‏‎ التي تم بها إعداد نوع الأصل **محرك شاحنة**، ستكون كل وظيفة أمر عمل يتم إنشاؤها مع نوع الأصل **محرك شاحنة** عبارة عن مشروع فرعي من معرف المشروع 000186.</span><span class="sxs-lookup"><span data-stu-id="27519-122">For example, in the following illustration, because of the way that the **Truck Engine** asset type is set up, every work order job that is created with the **Truck Engine** asset type will be a sub-project of project ID 000186.</span></span>

![الشكل 1](media/01-integration-to-pma.png)

<span data-ttu-id="27519-124">الغرض من معرف المشروع في وظيفة أمر العمل، ورقم النشاط المرتبط، هو تتبع التكاليف المرتبطة بوظيفة أمر العمل، والأصل المحدد عليها، في الوحدة النمطية **إدارة المشاريع ومحاسبتها**.</span><span class="sxs-lookup"><span data-stu-id="27519-124">The purpose of the project ID on the work order job, and the related activity number, is to track costs that are related to the work order job, and the asset that is selected on it, in the **Project management and accounting** module.</span></span> <span data-ttu-id="27519-125">(لعرض معرف المشروع ورقم النشاط، حدد **إدارة الأصول** > **عام** > **أوامر العمل** > **جميع أوامر العمل‬**، ثم حدد أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="27519-125">(To view the project ID and activity number, select **Asset management** > **Common** > **Work orders** > **All work orders**, and then select the work order.</span></span> <span data-ttu-id="27519-126">على علامة التبويب السريعة **تفاصيل البنود‬**، يُظهر الحقل **معرّف المشروع** معرّف المشروع، ويُظهر الحقل **رقم النشاط** رقم النشاط.) لمزيد من المعلومات حول مراقبة التكاليف‬ في إدارة الأصول، راجع [مراقبة التكاليف‬ والتاريخ‬](../controlling-and-reporting/cost-and-date-control.md).</span><span class="sxs-lookup"><span data-stu-id="27519-126">On the **Line details** FastTab, the **Project ID** field shows the project ID, and the **Activity number** field shows the activity number.) For more information about cost control in Asset Management, see [Cost and date control](../controlling-and-reporting/cost-and-date-control.md).</span></span>

<span data-ttu-id="27519-127">يُظهر الشكل التوضيحي التالي نظرة عامة رسومية على مشاريع أمر العمل وأنشطة المشاريع ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="27519-127">The following illustration shows a graphical overview of work order projects and related project activities.</span></span>

![الشكل 2](media/02-integration-to-pma.png)

<span data-ttu-id="27519-129">عند إنشاء وظيفة أمر عمل جديدة على أمر عمل، يتم إنشاء مشروع أمر عمل للمهمة بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="27519-129">When a new work order job is created on a work order, a work order project is automatically created for the job.</span></span> <span data-ttu-id="27519-130">ويتم تحويل الأبعاد المالية للأصل المرتبط بوظيفة أمر العمل إلى مشروع أمر العمل بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="27519-130">The financial dimensions for the asset that is related to the work order job are automatically transferred to the work order project.</span></span>

<span data-ttu-id="27519-131">يشتمل نشاط المشروع الذي تم إنشاؤه لوظيفة أمر العمل على معلومات ذات صلة مرتبطة به.</span><span class="sxs-lookup"><span data-stu-id="27519-131">The project activity that is created for a work order job has related information attached to it.</span></span> <span data-ttu-id="27519-132">وتتعلق هذه المعلومات بنوع مهمة الصيانة ومتغير نوع مهمة الصيانة والمعاملات.</span><span class="sxs-lookup"><span data-stu-id="27519-132">This information is about the maintenance job type, maintenance job type variant, and trade.</span></span> <span data-ttu-id="27519-133">وتكون هذه المعلومات مفيدة إذا قمت، على سبيل المثال، بإنشاء أمر شراء من أمر عمل (راجع [التدبير](../work-orders/procurement.md))، أو إذا استخدمت الوحدة النمطية **إدارة المشاريع ومحاسبتها‬** لتسجيل الوقت.</span><span class="sxs-lookup"><span data-stu-id="27519-133">It's useful if, for example, you create a purchase order from a work order (see [Procurement](../work-orders/procurement.md)), or if you use the **Project management and accounting** module for time registration.</span></span>

<span data-ttu-id="27519-134">إذا تم تثبيت الأصل في موقع وعمل، ولكن تم تثبيته لاحقًا في موقع عمل آخر، فسيتم تحديث الأبعاد المالية المرتبطة بموقع العمل الجديد على الأصل بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="27519-134">If the asset was installed on a functional location but is later installed on a different functional location, the financial dimensions that are related to the new functional location are automatically updated on the asset.</span></span> <span data-ttu-id="27519-135">بعد ذلك، عندما تنشئ وظيفة أمر عمل للأصل، يحصل مشروع أمر العمل الخاص بوظيفة أمر العمل بشكل تلقائي على الأبعاد المالية التي ترتبط الآن بالأصل.</span><span class="sxs-lookup"><span data-stu-id="27519-135">Then, when you create a work order job for the asset, the work order project for the work order job automatically gets the financial dimensions that are now related to the asset.</span></span> <span data-ttu-id="27519-136">وبالتالي، عندما تستخدم مواقع العمل، من الممكن تعقب التكاليف دائمًا على مواقع العمل التي تم تثبيت الأصل عليها في وقت معين.</span><span class="sxs-lookup"><span data-stu-id="27519-136">Therefore, when you use functional locations, costs can always be tracked on the functional locations that an asset was installed on at any given time.</span></span> <span data-ttu-id="27519-137">يساعد التحديث التلقائي للأبعاد المالية على ضمان إمكانية التتبع الكامل لتكاليف مراقبة المشروع وإعداد التقارير الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="27519-137">The automatic update of financial dimensions helps guarantee complete traceability of costs for project control and reporting.</span></span>

## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a><span data-ttu-id="27519-138">مشاريع أمر العمل وحالات دورة حياة أمر العمل ومراحل المشروع وأنواع المشاريع</span><span class="sxs-lookup"><span data-stu-id="27519-138">Work order projects, work order lifecycle states, project stages, and project types</span></span>

<span data-ttu-id="27519-139">للمساعدة في ضمان الاستخدام الصحيح لحالات دورة حياة أمر العمل ومراحل المشروع ذات الصلة على أوامر العمل، يجب أن تأخذ في الاعتبار التبعيات بالنسبة إلى الوحدة النمطية **إدارة المشاريع ومحاسبتها**:</span><span class="sxs-lookup"><span data-stu-id="27519-139">To help guarantee that work order lifecycle states and related project stages on work orders are used correctly, consider the dependencies in relation to the **Project management and accounting** module:</span></span>

- <span data-ttu-id="27519-140">في الوحدة النمطية **إدارة المشاريع ومحاسبتها**، يتم إعداد مراحل المشروع على أنواع المشاريع في صفحة **محددات إدارة المشاريع ومحاسبتها‬**.</span><span class="sxs-lookup"><span data-stu-id="27519-140">In the **Project management and accounting** module, project stages are set up on project types on the **Project management and accounting parameters** page.</span></span>  
- <span data-ttu-id="27519-141">في صفحة **محددات إدارة المشاريع ومحاسبتها‬**، استخدم خانات الاختيار لتحديد مراحل المشاريع ذات الصلة لجميع أنواع المشاريع التي ستستخدمها.</span><span class="sxs-lookup"><span data-stu-id="27519-141">On the **Project management and accounting parameters** page, use the check boxes to select relevant project stages for all the project types that you will use.</span></span> <span data-ttu-id="27519-142">في الأشكال التوضيحية التالية، تم تحديد خمس مراحل (**تم إنشاؤه** و**مقدر‏‎** و**مجدول‏‎** و**قيد المعالجة** و**منتهي‬‏‎**) لأنواع المشاريع **الوقت والمادة** و**داخلي**.</span><span class="sxs-lookup"><span data-stu-id="27519-142">In the following illustrations, five stages (**Created**, **Estimated**, **Scheduled**, **In process**, and **Finished**) have been selected for the **Time and material** and **Internal** project types.</span></span> <span data-ttu-id="27519-143">وتعتبر هذه المراحل الخمس ذات صلة بمهام الصيانة الداخلية ومهام صيانة الخدمة.</span><span class="sxs-lookup"><span data-stu-id="27519-143">Those five stages are relevant to both internal maintenance jobs and service maintenance jobs.</span></span>
- <span data-ttu-id="27519-144">في الوحدة النمطية **إدارة الأصول**، تتحدد أنواع المشاريع بواسطة مجموعات المشاريع التي تقوم بإعدادها في صفحة **إعداد مشروع أمر العمل‬** > علامة التبويب **مجموعة مشاريع** (**إدارة الأصول** > **الإعداد** > **أوامر العمل** > **إعداد المشروع**).</span><span class="sxs-lookup"><span data-stu-id="27519-144">In the **Asset Management** module, project types are defined by the project groups that you set up on the **Work order project setup** page > **Project group** tab (**Asset management** > **Setup** > **Work orders** > **Project setup**).</span></span>  
- <span data-ttu-id="27519-145">يتم استخدام مجموعات المشاريع التي يتم إعدادها في صفحة **إعداد مشروع أمر العمل** عند إنشاء أوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="27519-145">The project groups that are set up on the **Work order project setup** page are used when you create work orders.</span></span> <span data-ttu-id="27519-146">عند إنشاء أمر عمل، يتم إنشاء مشروع أمر عمل لأمر العمل بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="27519-146">When a work order is created, a work order project is automatically created for the work order.</span></span>  
- <span data-ttu-id="27519-147">يجب أن يكون لكل حالة من حالات دورة حياة أمر العمل مرحلة مشروع مرتبطة بها.</span><span class="sxs-lookup"><span data-stu-id="27519-147">Every work order lifecycle state must have a related project stage.</span></span>  
- <span data-ttu-id="27519-148">يجب تحديد مرحلة المشروع المرتبطة بحالة دورة حياة أمر العمل كمرحلة نشطة لمجموعة المشاريع المحددة في مشروع أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="27519-148">The project stage that is related to a work order lifecycle state must be defined as an active stage for the project group that is defined in the work order project.</span></span> <span data-ttu-id="27519-149">ويتم إنشاء مشروع أمر العمل على أمر العمل بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="27519-149">The work order project is automatically created on a work order.</span></span>
- <span data-ttu-id="27519-150">عند إنشاء أمر عمل جديد، يستند التوزيع التلقائي لمشروع أمر العمل إلى الإعداد في صفحة **إعداد مشروع أمر العمل**.</span><span class="sxs-lookup"><span data-stu-id="27519-150">When you create a new work order, the automatic allocation of a work order project is based on the setup on the **Work order project setup** page.</span></span>  

<span data-ttu-id="27519-151">تظهر في الأشكال التوضيحية أدناه الاقترانات بين مجموعات مشاريع أوامر العمل وأنواع المشاريع ذات الصلة ومراحل المشاريع وحالات دورة حياة أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="27519-151">The following illustrations show the associations between work order project groups, related project types, project stages, and work order lifecycle states.</span></span>

![الشكل 3](media/03-integration-to-pma.png)

![الشكل 4](media/04-integration-to-pma.png)

![الشكل 5](media/05-integration-to-pma.png)

<span data-ttu-id="27519-155">لمزيد من المعلومات حول كيفية إعداد مشاريع أوامر العمل، راجع [إعداد مشروع أمر العمل](../setup-for-work-orders/work-order-project-setup.md).</span><span class="sxs-lookup"><span data-stu-id="27519-155">For information about how to set up work order projects, see [Work order project setup](../setup-for-work-orders/work-order-project-setup.md).</span></span> <span data-ttu-id="27519-156">لمزيد من المعلومات حول كيفية إنشاء حالات دورة حياة أمر العمل، راجع [حالات دورة حياة أمر العمل](../setup-for-work-orders/work-order-lifecycle-states.md).</span><span class="sxs-lookup"><span data-stu-id="27519-156">For information about how to create work order lifecycle states, see [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md).</span></span>

<span data-ttu-id="27519-157">يقدم الشكل التوضيحي التالي نظرة عامة رسومية على مختلف المشاريع التي يتم إنشاؤها في الوحدة النمطية **إدارة الأصول** لتمكين التكامل مع الوحدة النمطية **إدارة المشاريع ومحاسبتها**.</span><span class="sxs-lookup"><span data-stu-id="27519-157">The following illustration shows a graphical overview of the various projects that are created in the **Asset management** module to enable integration with the **Project management and accounting** module.</span></span> <span data-ttu-id="27519-158">ويُظهر أيضًا عمليات العمل التي ترتبط بها المشاريع.</span><span class="sxs-lookup"><span data-stu-id="27519-158">It also shows the work processes that the projects are related to.</span></span>

![الشكل 6](media/06-integration-to-pma.png)

