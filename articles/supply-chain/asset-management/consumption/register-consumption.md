---
title: تسجيل الاستهلاك
description: يوضح هذا الموضوع كيفية تسجيل الاستهلاك في إدارة الأصول.
author: josaw1
manager: AnnBe
ms.date: 08/21/2019
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
ms.openlocfilehash: 7f785b0935b952d6de68fd120a3639077ad124bd
ms.sourcegitcommit: c0b581e4c647b6c47bc14d1d7bfe267832afecba
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/21/2019
ms.locfileid: "1913069"
---
# <a name="register-consumption"></a><span data-ttu-id="dd717-103">تسجيل الاستهلاك</span><span class="sxs-lookup"><span data-stu-id="dd717-103">Register consumption</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="dd717-104">عند اكتمال مهمة صيانة في أمر العمل، تقضي الخطوة التالية بإجراء تسجيلات الاستهلاك وترحيل دفاتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="dd717-104">When a maintenance job has been completed on a work order, the next step is to make consumption registrations and post the journals.</span></span> <span data-ttu-id="dd717-105">يمكن إجراء تسجيلات على أنواع الاستهلاك التالية: الساعات والأصناف والمصروفات.</span><span class="sxs-lookup"><span data-stu-id="dd717-105">You can make registrations on the following consumption types: Hours, items, and expenses.</span></span> <span data-ttu-id="dd717-106">ويتم تسجيل أنواع الاستهلاك المختلفة وترحيلها في صفحة **دفاتر يومية أمر العمل**.</span><span class="sxs-lookup"><span data-stu-id="dd717-106">The different consumption types are registered and posted on the **Work order journals** page.</span></span> <span data-ttu-id="dd717-107">يتم استخدام إعداد دفتر اليومية في **إدارة الأصول** لإنشاء وترحيل دفاتر يومية منفصلة للساعات والأصناف والمصروفات في الوحدة النمطية **إدارة المشاريع ومحاسبتها‬**.</span><span class="sxs-lookup"><span data-stu-id="dd717-107">The journal setup in **Asset Management** is used for creating and posting separate journals for hours, items, and expenses in the **Project management and accounting** module.</span></span>

<span data-ttu-id="dd717-108">قد تتمكن من إضافة أو حذف بنود التنبؤ في أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="dd717-108">You may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="dd717-109">يحدد إعداد حالة دورة حياة أمر العمل ونوع المشروع المرتبط وقواعد المرحلة المرتبطة بنوع المشروع ما إذا كان باستطاعتك إضافة بنود إلى دفتر اليومية أو تحريرها.</span><span class="sxs-lookup"><span data-stu-id="dd717-109">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determine if you are able to add or edit journal lines.</span></span> <span data-ttu-id="dd717-110">اقرأ المزيد حول حالات دورة حياة أمر العمل ومراحل المشروع المرتبطة‏‎ في [التكامل مع إدارة المشاريع ومحاسبتها‬](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span><span class="sxs-lookup"><span data-stu-id="dd717-110">Read more about work order lifecycle states and related project stages in [Integration to project management and accounting](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

>[!NOTE]
><span data-ttu-id="dd717-111">من الممكن إعداد الترحيل التلقائي لدفاتر اليومية على حالة دورة حياة أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="dd717-111">It is possible to set up automatic posting of journals on a work order lifecycle state.</span></span> <span data-ttu-id="dd717-112">راجع [حالات دورة حياة أمر العمل](../setup-for-work-orders/work-order-lifecycle-states.md) لمزيد من التفاصيل.</span><span class="sxs-lookup"><span data-stu-id="dd717-112">Refer to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) for more information.</span></span>

1. <span data-ttu-id="dd717-113">انقر فوق **إدارة الأصول** > **عام** > **أوامر العمل** > **جميع أوامر العمل** أو **أوامر العمل النشطة**.</span><span class="sxs-lookup"><span data-stu-id="dd717-113">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="dd717-114">حدد أمر العمل وانقر فوق **دفاتر اليومية**.</span><span class="sxs-lookup"><span data-stu-id="dd717-114">Select the work order and click **Journals**.</span></span>

3. <span data-ttu-id="dd717-115">انقر فوق **نسخ من التنبؤات** لتحويل أي بنود تنبؤ قد تكون متصلة بأمر العمل.</span><span class="sxs-lookup"><span data-stu-id="dd717-115">Click **Copy from forecast** to transfer any forecast lines that may be connected to the work order.</span></span> <span data-ttu-id="dd717-116">يمكنك تحديد أنواع الاستهلاك التي ترغب في تحويلها.</span><span class="sxs-lookup"><span data-stu-id="dd717-116">You can select which consumption types you want to transfer.</span></span>

4. <span data-ttu-id="dd717-117">وإذا لزم الأمر، يمكنك إضافة المزيد من بنود الاستهلاك على علامة التبويب السريعة وذلك بالنقر فوق **إضافة بند** وملء البيانات على البند.</span><span class="sxs-lookup"><span data-stu-id="dd717-117">If necessary, you can add more consumption lines on the relevant FastTab by clicking **Add line** and filling out data on the line.</span></span>

5. <span data-ttu-id="dd717-118">انقر فوق **التحقق من صحة دفاتر اليومية** للتحقق من صحة بنود دفتر اليومية قبل ترحيلها.</span><span class="sxs-lookup"><span data-stu-id="dd717-118">Click **Validate journals** to validate the journal lines before posting.</span></span>

6. <span data-ttu-id="dd717-119">انقر فوق  **ترحيل دفاتر اليومية** لترحيل بنود دفاتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="dd717-119">Click **Post journals** to post the journal lines.</span></span>

7. <span data-ttu-id="dd717-120">بعد ترحيل دفاتر يومية الاستهلاك، يمكنك تحديث حالة دورة حياة أمر العمل، على سبيل المثال إلى "منتهي" للإشارة إلى إنجاز أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="dd717-120">After you've posted the consumption journals, you can update the work order lifecycle state, for example to "Ended", to indicate that the work order has been completed.</span></span>

- <span data-ttu-id="dd717-121">في الحقل‏‎ **إظهار** الموضوع في أعلى صفحة **دفاتر يومية أمر العمل**، حدد بنود دفتر اليومية التي ترغب في رؤيتها: الكل أو غير مرحل أو مرحل.</span><span class="sxs-lookup"><span data-stu-id="dd717-121">In the **Show** field placed at the top of the **Work order journals** page, select which journal lines you want to see: All, Not posted, or Posted.</span></span> <span data-ttu-id="dd717-122">توجد علامة اختيار في خانة الاختيار **مرحل** لدفاتر اليومية المرحلة.</span><span class="sxs-lookup"><span data-stu-id="dd717-122">Posted journals have a check mark in the **Posted** check box.</span></span>  
- <span data-ttu-id="dd717-123">عند إنشاء بنود في دفتر يومية أمر العمل، يتم تحويل دفتر يومية أمر العمل وأبعاد المنتج وأبعاد التعقب ذات الصلة بالصنف إلى بند دفتر اليومية بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="dd717-123">When item lines are created in the work order journal, product dimensions and tracking dimensions related to the item are automatically transferred to the journal line.</span></span>  

<span data-ttu-id="dd717-124">تعرض لقطة الشاشة أدناه مثالا لتسجيلات الساعات والأصناف على أمر عمل في**دفاتر يومية أمر العمل**.</span><span class="sxs-lookup"><span data-stu-id="dd717-124">The screenshot below shows an example of hour and item registrations on a work order in **Work order journals**.</span></span>

![الشكل 1](media/01-consumption.png)


## <a name="split-hours-on-work-orders-with-several-work-order-jobs"></a><span data-ttu-id="dd717-126">تقسيم الساعات على أوامر العمل باستخدام وظائف أوامر عمل متعددة</span><span class="sxs-lookup"><span data-stu-id="dd717-126">Split hours on work orders with several work order jobs</span></span>

<span data-ttu-id="dd717-127">إذا كان أمر العمل يحتوي على عدد كبير من وظائف أمر العمل، فيمكنك تسجيل ساعات العمل باستخدام الوظيفة **تقسيم الساعات**، مما يعني انه يمكن توزيع بند تسجيل ساعة واحد بالتساوي على كل وظيفة أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="dd717-127">If a work order contains several work order jobs, you can register work hours using the **Split hours** functionality, meaning one hour registration line can be distributed evenly on each work order job.</span></span>

1. <span data-ttu-id="dd717-128">انقر فوق **إدارة الأصول** > **عام** > **أوامر العمل** > **جميع أوامر العمل** أو **أوامر العمل النشطة**.</span><span class="sxs-lookup"><span data-stu-id="dd717-128">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="dd717-129">حدد أمر العمل وانقر فوق **دفاتر اليومية**.</span><span class="sxs-lookup"><span data-stu-id="dd717-129">Select the work order and click **Journals**.</span></span>

3. <span data-ttu-id="dd717-130">حدد بند تسجيل الساعات الذي ترغب في تقسيمه، ثم انقر فوق **تقسيم الساعات**.</span><span class="sxs-lookup"><span data-stu-id="dd717-130">Select the hour registration line you want to split, and click **Split hours**.</span></span>

4. <span data-ttu-id="dd717-131">في مربع الحوار **تقسيم الساعات على مهام صيانة أمر العمل**، يظهر اسم العامل الذي سجل دخوله تلقائيًا في حقل **العامل**.</span><span class="sxs-lookup"><span data-stu-id="dd717-131">In the **Split hours on work order maintenance jobs** dialog, the name of the worker who is logged in is automatically shown in the **Worker** field.</span></span> <span data-ttu-id="dd717-132">يمكنك تحديد عامل آخر، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="dd717-132">If required, you can select another worker.</span></span>

5. <span data-ttu-id="dd717-133">حدد فئة لتسجيل الساعات في حقل **الفئة**.</span><span class="sxs-lookup"><span data-stu-id="dd717-133">Select a category for the hour registration in the **Category** field.</span></span>

6. <span data-ttu-id="dd717-134">أدخل عدد ساعات العمل التي سيتم تقسيمها في الحقل **ساعات**.</span><span class="sxs-lookup"><span data-stu-id="dd717-134">Insert number of work hours to be split in the **Hours** field.</span></span>

![الشكل 2](media/02-consumption.png)

7. <span data-ttu-id="dd717-136">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="dd717-136">Click **OK**.</span></span>

<span data-ttu-id="dd717-137">*مثال:* في لقطة الشاشة أدناه، تظهر بنود دفتر اليومية لأمر عمل يحتوي على ثلاث مهام خاصة بأمر العمل.</span><span class="sxs-lookup"><span data-stu-id="dd717-137">*Example:* In the screenshot below, journal lines for a work order containing three work order jobs are shown.</span></span> <span data-ttu-id="dd717-138">تم تقسيم البند الأول، الذي يحتوي على ثلاث ساعات عمل، وتم تسجيل ساعة عمل واحدة على كل وظيفة أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="dd717-138">The first line, containing three work hours, has been split, and one work hour is registered on each work order job.</span></span> <span data-ttu-id="dd717-139">بعد إنشاء بنود تسجيل الساعات الثلاثة، تقرر أنت ما يجب القيام به مع بند تسجيل الساعات الأصلي (البند الأول في المثال).</span><span class="sxs-lookup"><span data-stu-id="dd717-139">After the three hour registration lines have been created, you decide what to do with the original hour registration line (the first line in the example).</span></span> <span data-ttu-id="dd717-140">يمكنك الاحتفاظ به كما هو أو حذفه.</span><span class="sxs-lookup"><span data-stu-id="dd717-140">You can keep it as is or delete it.</span></span> 

![الشكل 3](media/03-consumption.png)

## <a name="financial-dimensions-on-consumption-registrations"></a><span data-ttu-id="dd717-142">الأبعاد المالية على تسجيلات الاستهلاك</span><span class="sxs-lookup"><span data-stu-id="dd717-142">Financial dimensions on consumption registrations</span></span>

<span data-ttu-id="dd717-143">عند إجراء تسجيلات استهلاك، تُضاف الأبعاد المالية المرتبطة بأنواع التسجيل المختلفة إلى التسجيلات في تسلسل معين.</span><span class="sxs-lookup"><span data-stu-id="dd717-143">When you make consumption registrations, financial dimensions related to the different registration types are added to the registrations in a specific sequence.</span></span> 

<span data-ttu-id="dd717-144">*تسجيلات الساعات والمصروفات:* تُضاف أولاً الأبعاد المالية من رأس دفتر اليومية، في حال وجودها.</span><span class="sxs-lookup"><span data-stu-id="dd717-144">*Hour and Expense registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="dd717-145">وبعد ذلك، تُضاف الأبعاد المالية من مشروع أمر العمل ذي الصلة.</span><span class="sxs-lookup"><span data-stu-id="dd717-145">Next, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="dd717-146">وأخيرًا، تُضاف الأبعاد المالية من المورد (العامل).</span><span class="sxs-lookup"><span data-stu-id="dd717-146">Finally, financial dimensions from the resource (worker) are added.</span></span>

<span data-ttu-id="dd717-147">*تسجيلات الأصناف:* تُضاف أولاً الأبعاد المالية من رأس دفتر اليومية، في حال وجودها.</span><span class="sxs-lookup"><span data-stu-id="dd717-147">*Item registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="dd717-148">ثم تُضاف الأبعاد المالية من مشروع أمر العمل ذي الصلة.</span><span class="sxs-lookup"><span data-stu-id="dd717-148">Then, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="dd717-149">بعد ذلك، تُضاف الأبعاد المالية من الموقع.</span><span class="sxs-lookup"><span data-stu-id="dd717-149">Next, financial dimensions from the site are added.</span></span> <span data-ttu-id="dd717-150">وأخيرًا، تُضاف الأبعاد المالية من الصنف.</span><span class="sxs-lookup"><span data-stu-id="dd717-150">Finally, financial dimensions from the item are added.</span></span>

>[!NOTE]
><span data-ttu-id="dd717-151">بالنسبة إلى كافة أنواع التسجيلات الثلاثة، يتم التحقق من صحة تركيبة الأبعاد المالية، ويتم تجاهل التركيبات غير الصالحة.</span><span class="sxs-lookup"><span data-stu-id="dd717-151">For all three registration types, the financial dimension combination is validated, and invalid combinations are blanked.</span></span> <span data-ttu-id="dd717-152">هذا هو الإعداد القياسي في Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="dd717-152">This is standard setup in Dynamics 365 for Finance and Operations.</span></span>

