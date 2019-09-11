---
title: التنبؤات وأوامر العمل والمشاريع
description: يشرح هذا الموضوع التنبؤات وتكامل أمر العمل مع الوحدة النمطية "إدارة المشاريع ومحاسبتها" في إدارة الأصول.
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
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
ms.openlocfilehash: 5e986d139ac9d0a7729bb9787f05332bcc09f59b
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886806"
---
# <a name="forecasts-work-orders-and-projects"></a><span data-ttu-id="041db-103">التنبؤات وأوامر العمل والمشاريع</span><span class="sxs-lookup"><span data-stu-id="041db-103">Forecasts, work orders, and projects</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="041db-104">في إدارة الأصول، يتم التكامل مع الوحدة النمطية **إدارة المشاريع ومحاسبتها** لتحسين مراقبة التكاليف‬ مما يسمح للمستخدمين بتعقب التكاليف على تنبؤات أنواع مهام الصيانة ووظائف أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="041db-104">In Asset Management, integration to the **Project management and accounting** module is done to optimize cost control, allowing users to track costs on maintenance job type forecasts and work order jobs.</span></span>

<span data-ttu-id="041db-105">لتتبع تنبؤات أنواع مهام الصيانة، تحتاج إلى إعدادين:</span><span class="sxs-lookup"><span data-stu-id="041db-105">To track maintenance job type forecasts, two settings must be made:</span></span>

1. <span data-ttu-id="041db-106">حدد مشروعًا في **إدارة الأصول** > **الإعداد** > **محددات إدارة الأصول‬** > ارتباط **الأصول** > علامة التبويب السريعة **المشروع** > الحقل **مشروع التنبؤ بمتطلبات الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="041db-106">Select a project in **Asset management** > **Setup** > **Asset management parameters** > **Assets** link > **Project** FastTab > **Maintenance forecast project** field.</span></span>

2. <span data-ttu-id="041db-107">في **الإعدادات الافتراضية لأنواع مهام الصيانة‬‏‫**، عندما تنشئ بندًا افتراضيًا لنوع مهمة الصيانة، يتم إنشاء رقم نشاط للبند بشكل تلقائي (**إدارة الأصول** > **الإعداد** > **المهام** > **الإعدادات الافتراضية لأنواع مهام الصيانة**).</span><span class="sxs-lookup"><span data-stu-id="041db-107">In **Maintenance job type defaults**, when you create a mainteance job type default line, an activity number is automatically created for the line (**Asset management** > **Setup** > **Jobs** > **Maintenance job type defaults**).</span></span>

<span data-ttu-id="041db-108">هناك غرضان لتنبؤات أنواع مهام الصيانة: يمكنك تتبع التكاليف على تنبؤات أنواع مهام الصيانة في الوحدة النمطية **إدارة المشاريع ومحاسبتها**.</span><span class="sxs-lookup"><span data-stu-id="041db-108">Maintenance job type forecasts serve two purposes: You are able to track costs on maintenance job type forecasts in the **Project management and accounting** module.</span></span> <span data-ttu-id="041db-109">علاوة على ذلك، تُنقل تنبؤات أنواع مهام الصيانة بشكل تلقائي إلى مشروع وظيفة أمر عمل عند تحديد نوع مهمة صيانة على وظيفة أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="041db-109">Furthermore, forecasts are automatically transferred to a work order job project when you select a maintenance job type on a work order job.</span></span>

<span data-ttu-id="041db-110">لتتبع التكاليف على وظائف أوامر العمل، يجب أولاً إعداد مشاريع أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="041db-110">To track costs on work order jobs, you must first set up work order projects.</span></span> <span data-ttu-id="041db-111">يمكنك مراجعة القسم [إعداد مشروع أمر العمل‬](../setup-for-work-orders/work-order-project-setup.md) للحصول على وصف للإجراء.</span><span class="sxs-lookup"><span data-stu-id="041db-111">Refer to the [Work order project setup](../setup-for-work-orders/work-order-project-setup.md) section for a description of the procedure.</span></span>

## <a name="work-order-job-projects"></a><span data-ttu-id="041db-112">مشاريع وظائف أمر العمل</span><span class="sxs-lookup"><span data-stu-id="041db-112">Work order job projects</span></span>

<span data-ttu-id="041db-113">عند إنشاء وظيفة أمر عمل على أمر عمل، يتحدد مشروع أمر العمل بواسطة إعداد المشروع الرئيسي لأوامر العمل في **إدارة الأصول** > **الإعداد** > **أوامر العمل** > **إعداد المشروع**.</span><span class="sxs-lookup"><span data-stu-id="041db-113">When you create a work order job on a work order, the work order project is determined by the setup of the parent project for work orders in **Asset management** > **Setup** > **Work orders** > **Project setup**.</span></span>

<span data-ttu-id="041db-114">يتم إنشاء مشاريع وظائف أمر العمل باستخدام تركيبة من معلومات أمر العمل التالية:</span><span class="sxs-lookup"><span data-stu-id="041db-114">Work order job projects are created by using a combination of the following work order information:</span></span>

- <span data-ttu-id="041db-115">نوع أمر العمل المحدد على أمر العمل</span><span class="sxs-lookup"><span data-stu-id="041db-115">The Work order type selected on the work order</span></span> 
- <span data-ttu-id="041db-116">موقع العمل المرتبط بالأصل على وظيفة أمر العمل</span><span class="sxs-lookup"><span data-stu-id="041db-116">The functional location related to the asset on the work order job</span></span>
- <span data-ttu-id="041db-117">نوع الأصل المرتبط بالأصل على وظيفة أمر العمل</span><span class="sxs-lookup"><span data-stu-id="041db-117">The Asset type related to the asset on the work order job</span></span>  
- <span data-ttu-id="041db-118">وقت البدء والانتهاء المتوقعين المحددين على أمر العمل</span><span class="sxs-lookup"><span data-stu-id="041db-118">The Expected start and end time set on the work order</span></span>  

<span data-ttu-id="041db-119">من المحتمل ألا يتم العثور على جميع المعلومات المذكورة أعلاه على أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="041db-119">It is possible that not all of the information mentioned above is found on a work order.</span></span> <span data-ttu-id="041db-120">وبالتالي، يتم البحث عن المشروع الرئيسي لأمر العمل باستخدام التركيبات المتوفرة من البيانات وتحديد معرف المشروع الذي يتوافق مع بيانات أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="041db-120">Therefore, the search for a work order parent project is done by using the available combination of data and selecting the project ID that corresponds with work order data.</span></span>

<span data-ttu-id="041db-121">مثال: في الشكل الموضح أدناه، يعني إعداد نوع الأصل "محرك الشاحنة" أن كل وظيفة أمر عمل تم إنشاؤها مع نوع الأصل هذا ستكون عبارة عن مشروع فرعي لمعرف المشروع "000186".</span><span class="sxs-lookup"><span data-stu-id="041db-121">Example: In the figure below, the setup of asset type "Truck Engine" means that every work order job created with that asset type will be a sub project of Project ID "000186".</span></span>

![الشكل 1](media/01-integration-to-pma.png)

<span data-ttu-id="041db-123">الغرض من معرف المشروع على وظيفة أمر العمل ورقم النشاط ذي الصلة (**إدارة الأصول** > **عام** > **أوامر العمل** > **جميع أوامر العمل** > حدد أمر عمل في القائمة > علامة التبويب السريعة **تفاصيل البنود** > حقل **معرف المشروع** وحقل **رقم النشاط**)، هو تعقب التكاليف ذات الصلة بوظيفة أمر العمل، والأصل المحدد على وظيفة أمر العمل في الوحدة النمطية **إدارة المشاريع ومحاسبتها**.</span><span class="sxs-lookup"><span data-stu-id="041db-123">The purpose of the project ID on the work order job, and the related activity number (**Asset management** > **Common** > **Work orders** > **All Work orders** > select work order in list > **Line details** FastTab > **Project ID** field and **Activity number** field), is to track costs related to the work order job, and the asset selected on the work order job, in the **Project management and accounting** module.</span></span> 

<span data-ttu-id="041db-124">في الشكل الموضح أدناه، يمكنك رؤية نظرة عامة رسومية على مشاريع أمر العمل وأنشطة المشاريع ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="041db-124">In the figure below, you see a graphic overview of work order projects and related project activities.</span></span>

![الشكل 2](media/02-integration-to-pma.png)

<span data-ttu-id="041db-126">عند إنشاء وظيفة أمر عمل جديدة على أمر عمل، يتم إنشاء مشروع أمر عمل للمهمة بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="041db-126">When a new work order job is created on a work order, a work order project is automatically created for the job.</span></span> <span data-ttu-id="041db-127">ويتم تحويل الأبعاد المالية للأصل المرتبط بوظيفة أمر العمل إلى مشروع أمر العمل بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="041db-127">The financial dimensions for the asset related to the work order job are automatically transferred to the work order project.</span></span> <span data-ttu-id="041db-128">يتضمن نشاط المشروع الذي تم إنشاؤه لوظيفة أمر العمل المعلومات المرتبطة به فيما يتعلق بنوع مهمة الصيانة ومتغير نوع مهمة الصيانة والمعاملات.</span><span class="sxs-lookup"><span data-stu-id="041db-128">The project activity created for a work order job has related information attached to it regarding maintenance job type, maintenance job type variant, and trade.</span></span> <span data-ttu-id="041db-129">وتكون هذه البيانات مفيدة إذا قمت، على سبيل المثال، بإنشاء أمر شراء من أمر عمل (راجع [التدبير](../work-orders/procurement.md))، أو إذا استخدمت الوحدة النمطية **إدارة المشاريع ومحاسبتها‬** لتسجيل الوقت.</span><span class="sxs-lookup"><span data-stu-id="041db-129">Those data are useful if, for example, you create a purchase order from a work order (see [Procurement](../work-orders/procurement.md)), or if you use the **Project management and accounting** module for time registration.</span></span>  

<span data-ttu-id="041db-130">إذا تم تثبيت الأصل في موقع وعمل، وتم تثبيت هذا الأصل لاحقًا في موقع عمل آخر، فسيتم تحديث الأبعاد المالية المرتبطة بموقع العمل الجديد على الأصل بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="041db-130">If the asset was installed on a functional location, and that asset is later installed on another functional location, the financial dimensions related to the new functional location is automatically updated on the asset.</span></span> <span data-ttu-id="041db-131">وبالتالي، عندما تنشئ وظيفة أمر عمل للأصل، يحصل مشروع أمر العمل الخاص بوظيفة أمر العمل بشكل تلقائي على الأبعاد المالية التي ترتبط الآن بالأصل.</span><span class="sxs-lookup"><span data-stu-id="041db-131">Subsequently, when you create a work order job for the asset, the work order project for the work order job automatically gets the financial dimensions that are now related to the asset.</span></span> <span data-ttu-id="041db-132">وهذا يعني أنك عندما تستخدم مواقع العمل، من الممكن تعقب التكاليف دائمًا على مواقع العمل التي تم تثبيت الأصل عليها في في وقت.</span><span class="sxs-lookup"><span data-stu-id="041db-132">This means that when you use functional locations, costs can always be tracked on the functional locations on which an asset was installed at any given time.</span></span> <span data-ttu-id="041db-133">ويضمن التحديث التلقائي للأبعاد المالية إمكانية التتبع الكامل لتكاليف مراقبة المشروع وإعداد التقارير الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="041db-133">The automatic update of financial dimensions ensures complete traceability of costs for project controlling and reporting.</span></span>  


## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a><span data-ttu-id="041db-134">مشاريع أمر العمل وحالات دورة حياة أمر العمل ومراحل المشروع وأنواع المشاريع</span><span class="sxs-lookup"><span data-stu-id="041db-134">Work order projects, work order lifecycle states, project stages, and project types</span></span>

<span data-ttu-id="041db-135">لضمان الاستخدام الصحيح لحالات دورة حياة أمر العمل ومراحل المشروع ذات الصلة على أوامر العمل، يجب أن تأخذ في الاعتبار التبعيات بالنسبة إلى الوحدة النمطية **إدارة المشاريع ومحاسبتها**:</span><span class="sxs-lookup"><span data-stu-id="041db-135">To ensure correct use of work order lifecycle states and related project stages on work orders, consider the dependencies in relation to the **Project management and accounting** module:</span></span>

- <span data-ttu-id="041db-136">في الوحدة النمطية **إدارة المشاريع ومحاسبتها**، يتم إعداد مراحل المشروع على أنواع المشاريع في **محددات إدارة المشاريع ومحاسبتها‬**.</span><span class="sxs-lookup"><span data-stu-id="041db-136">In the **Project management and accounting** module, project stages are set up on project types in **Project management and accounting parameters**.</span></span>  
- <span data-ttu-id="041db-137">في **محددات إدارة المشاريع ومحاسبتها‬**، تذكر ضرورية تحديد خانات الاختيار التابعة لمراحل المشاريع ذات الصلة لجميع أنواع المشاريع التي ستستخدمها.</span><span class="sxs-lookup"><span data-stu-id="041db-137">In **Project management and accounting parameters**, remember to select relevant project stage check boxes for all the project types you are going to use.</span></span> <span data-ttu-id="041db-138">في الشكل الموضح أدناه، تم إنشاء خمس مراحل **تم إنشاؤه** - **مقدر** - **مجدول** - **قيد المعالجة** - **منتهي‬** لأنواع المشاريع "الوقت والمادة‬" و"داخلي".</span><span class="sxs-lookup"><span data-stu-id="041db-138">In the figure below, five stages **Created** - **Estimated** - **Scheduled** - **In process** - **Finished** have been selected for the project types "Time and material" and "Internal".</span></span> <span data-ttu-id="041db-139">وتعتبر هذه المراحل الخمس ذات صلة بمهام الصيانة الداخلية ومهام صيانة الخدمة.</span><span class="sxs-lookup"><span data-stu-id="041db-139">Those five stages are relevant for both internal maintenance and service maintenance jobs.</span></span>  
- <span data-ttu-id="041db-140">في **إدارة الأصول**، تتحدد أنواع المشاريع بواسطة مجموعات المشاريع التي تقوم بإعدادها في النموذج **إعداد مشروع أمر العمل** > الارتباط **مجموعة المشاريع**.</span><span class="sxs-lookup"><span data-stu-id="041db-140">In **Asset Management**, project types are defined by the project groups you set up in the **Work order project setup** form > **Project group** link.</span></span>  
- <span data-ttu-id="041db-141">يتم استخدام إعداد مجموعات المشاريع في **إعداد مشروع أمر العمل** عند إنشاء أوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="041db-141">The project groups setup in **Work order project setup** are used when you create work orders.</span></span> <span data-ttu-id="041db-142">عند إنشاء أمر عمل، يتم إنشاء مشروع أمر عمل لأمر العمل بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="041db-142">When a work order is created, a work order project is automatically created for the work order.</span></span>  
- <span data-ttu-id="041db-143">يجب أن يكون لكل حالة من حالات دورة حياة أمر العمل مرحلة مشروع مرتبطة بها.</span><span class="sxs-lookup"><span data-stu-id="041db-143">Work order lifecycle states must each have a related project stage.</span></span>  
- <span data-ttu-id="041db-144">يجب تحديد مرحلة المشروع المرتبطة بحالة دورة حياة أمر العمل كمرحلة نشطة لمجموعة المشاريع المحددة في مشروع أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="041db-144">The project stage related to a work order lifecycle state must be defined as an active stage for the project group defined in the work order project.</span></span> <span data-ttu-id="041db-145">ويتم إنشاء مشروع أمر العمل على أمر العمل بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="041db-145">The work order project is automatically created on a work order.</span></span>  
- <span data-ttu-id="041db-146">عند إنشاء أمر عمل جديد، يستند التخصيص التلقائي لمشروع أمر العمل على الإعداد في **إعداد مشروع أمر العمل** (**إدارة الأصول** > **الإعداد** > **أوامر العمل** > **إعداد المشروع**).</span><span class="sxs-lookup"><span data-stu-id="041db-146">When you create a new work order, the automatic allocation of a work order project is based on the setup in **Work order project setup** (**Asset management** > **Setup** > **Work orders** > **Project setup**).</span></span>  

<span data-ttu-id="041db-147">تظهر في الأشكال أدناه الاقترانات بين مجموعات مشاريع أوامر العمل وأنواع المشاريع ذات الصلة ومراحل المشاريع وحالات دورة حياة أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="041db-147">Associations between work order project groups, related project types, project stages, and work order lifecycle states are shown in the figures below.</span></span>  

![الشكل 3](media/03-integration-to-pma.png)

![الشكل 4](media/04-integration-to-pma.png)

![الشكل 5](media/05-integration-to-pma.png)

<span data-ttu-id="041db-151">يمكنك مراجعة [إعداد مشروع أمر العمل](../setup-for-work-orders/work-order-project-setup.md) فيما يتعلق بكيفية إعداد مشاريع أمر العمل، و [حالات دورة حياة أمر العمل](../setup-for-work-orders/work-order-lifecycle-states.md) فيما يتعلق بكيفية إنشاء حالات دورة حياة أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="041db-151">Refer to [Work order project setup](../setup-for-work-orders/work-order-project-setup.md) regarding how to set up work order projects, and to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) regarding how to create work order lifecycle states.</span></span>

<span data-ttu-id="041db-152">يعرض الشكل أدناه نظرة عامة رسومية على مشاريع مختلفة تم إنشاؤها في الوحدة النمطية **إدارة الأصول** للسماح بالتكامل مع الوحدة النمطية **إدارة المشاريع ومحاسبتها**، بالإضافة إلى عمليات العمل التي ترتبط المشاريع بها.</span><span class="sxs-lookup"><span data-stu-id="041db-152">The figure below shows a graphic overview of the various projects that are created in the **Asset management** module to allow integration with the **Project management and accounting** module, as well as the work processes to which the projects are related.</span></span>

![الشكل 6](media/06-integration-to-pma.png)

