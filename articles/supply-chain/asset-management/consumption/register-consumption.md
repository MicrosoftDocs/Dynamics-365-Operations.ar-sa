---
title: تسجيل الاستهلاك
description: يوضح هذا الموضوع كيفية تسجيل الاستهلاك في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderJournal, EntAssetWorkOrderAddSparePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 61aea0261a62df9c029b429f33ba7b357621988b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259976"
---
# <a name="register-consumption"></a><span data-ttu-id="206cd-103">تسجيل الاستهلاك</span><span class="sxs-lookup"><span data-stu-id="206cd-103">Register consumption</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="206cd-104">عند اكتمال مهمة صيانة في أمر العمل، تقضي الخطوة التالية بإجراء تسجيلات الاستهلاك وترحيل دفاتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="206cd-104">When a maintenance job has been completed on a work order, the next step is to make consumption registrations and post the journals.</span></span> <span data-ttu-id="206cd-105">يمكن إجراء تسجيلات على أنواع الاستهلاك التالية: الساعات والأصناف والمصروفات.</span><span class="sxs-lookup"><span data-stu-id="206cd-105">You can make registrations on the following consumption types: Hours, items, and expenses.</span></span> <span data-ttu-id="206cd-106">ويتم تسجيل أنواع الاستهلاك المختلفة وترحيلها في صفحة **دفاتر يومية أمر العمل**.</span><span class="sxs-lookup"><span data-stu-id="206cd-106">The different consumption types are registered and posted on the **Work order journals** page.</span></span> <span data-ttu-id="206cd-107">يتم استخدام إعداد دفتر اليومية في **إدارة الأصول** لإنشاء وترحيل دفاتر يومية منفصلة للساعات والأصناف والمصروفات في الوحدة النمطية **إدارة المشاريع ومحاسبتها‬**.</span><span class="sxs-lookup"><span data-stu-id="206cd-107">The journal setup in **Asset Management** is used for creating and posting separate journals for hours, items, and expenses in the **Project management and accounting** module.</span></span>

<span data-ttu-id="206cd-108">في بعض الحالات، قد تتمكن من إضافة أو حذف بنود التنبؤ في أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="206cd-108">In some cases, you may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="206cd-109">يحدد إعداد حالة دورة حياة أمر العمل ونوع المشروع المرتبط وقواعد المرحلة المرتبطة بنوع المشروع ما إذا كان باستطاعتك إضافة بنود إلى دفتر اليومية أو تحريرها.</span><span class="sxs-lookup"><span data-stu-id="206cd-109">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determine if you are able to add or edit journal lines.</span></span> <span data-ttu-id="206cd-110">اقرأ المزيد حول حالات دورة حياة أمر العمل ومراحل المشروع ذات الصلة في [التنبؤات، أوامر العمل، والمشاريع](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span><span class="sxs-lookup"><span data-stu-id="206cd-110">Read more about work order lifecycle states and related project stages in [Forecasts, work orders, and projects](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

>[!NOTE]
><span data-ttu-id="206cd-111">من الممكن إعداد الترحيل التلقائي لدفاتر اليومية على حالة دورة حياة أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="206cd-111">It is possible to set up automatic posting of journals on a work order lifecycle state.</span></span> <span data-ttu-id="206cd-112">راجع [حالات دورة حياة أمر العمل](../setup-for-work-orders/work-order-lifecycle-states.md) لمزيد من التفاصيل.</span><span class="sxs-lookup"><span data-stu-id="206cd-112">Refer to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) for more information.</span></span>

1. <span data-ttu-id="206cd-113">انقر فوق **إدارة الأصول** > **عام** > **أوامر العمل** > **جميع أوامر العمل** أو **أوامر العمل النشطة**.</span><span class="sxs-lookup"><span data-stu-id="206cd-113">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="206cd-114">حدد أمر العمل، وانقر فوق **دفاتر اليومية**.</span><span class="sxs-lookup"><span data-stu-id="206cd-114">Select the work order, and click **Journals**.</span></span>

3. <span data-ttu-id="206cd-115">انقر فوق **نسخ من التنبؤات** لتحويل أي بنود تنبؤ قد تكون متصلة بأمر العمل.</span><span class="sxs-lookup"><span data-stu-id="206cd-115">Click **Copy from forecast** to transfer any forecast lines that may be connected to the work order.</span></span> <span data-ttu-id="206cd-116">يمكنك تحديد أنواع الاستهلاك التي ترغب في تحويلها.</span><span class="sxs-lookup"><span data-stu-id="206cd-116">You can select which consumption types you want to transfer.</span></span>

4. <span data-ttu-id="206cd-117">وإذا لزم الأمر، يمكنك إضافة المزيد من بنود الاستهلاك على علامة التبويب السريعة وذلك بالنقر فوق **إضافة بند** وملء البيانات على البند.</span><span class="sxs-lookup"><span data-stu-id="206cd-117">If necessary, you can add more consumption lines on the relevant FastTab by clicking **Add line** and filling out data on the line.</span></span>

5. <span data-ttu-id="206cd-118">انقر فوق **التحقق من صحة دفاتر اليومية** للتحقق من صحة بنود دفتر اليومية قبل ترحيلها.</span><span class="sxs-lookup"><span data-stu-id="206cd-118">Click **Validate journals** to validate the journal lines before posting.</span></span>

6. <span data-ttu-id="206cd-119">انقر فوق  **ترحيل دفاتر اليومية** لترحيل بنود دفاتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="206cd-119">Click **Post journals** to post the journal lines.</span></span>

7. <span data-ttu-id="206cd-120">بعد أن تقوم بترحيل دفاتر يومية الاستهلاك، يمكنك تحديث حالة دورة حياة أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="206cd-120">After you've posted the consumption journals, you can update the work order lifecycle state.</span></span> <span data-ttu-id="206cd-121">على سبيل المثال، للإشارة إلى أنه تم إكمال أمر العمل، فإنه يمكنك تحديث حالة دورة الحياة إلى "تم الإنهاء".</span><span class="sxs-lookup"><span data-stu-id="206cd-121">For example, to indicate that the work order has been completed, you can update the lifecycle state to "Ended".</span></span>

    - <span data-ttu-id="206cd-122">في الحقل **إظهار** في أعلى صفحة **دفاتر يومية أمر العمل**، حدد بنود دفتر اليومية التي ترغب في رؤيتها: **الكل**، أو   **غير مرحل**، أو **مرحل**.</span><span class="sxs-lookup"><span data-stu-id="206cd-122">In the **Show** field at the top of the **Work order journals** page, select which journal lines you want to see: **All**, **Not posted**, or **Posted**.</span></span> <span data-ttu-id="206cd-123">توجد علامة اختيار في خانة الاختيار **مرحل** لدفاتر اليومية المرحلة.</span><span class="sxs-lookup"><span data-stu-id="206cd-123">Posted journals have a check mark in the **Posted** check box.</span></span>  
    - <span data-ttu-id="206cd-124">عند إنشاء بنود في دفتر يومية أمر العمل، يتم تحويل دفتر يومية أمر العمل وأبعاد المنتج وأبعاد التعقب ذات الصلة بالصنف إلى بند دفتر اليومية بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="206cd-124">When item lines are created in the work order journal, product dimensions and tracking dimensions related to the item are automatically transferred to the journal line.</span></span>  

<span data-ttu-id="206cd-125">تعرض لقطة الشاشة أدناه مثالا لتسجيلات الساعات والأصناف على أمر عمل في **دفاتر يومية أمر العمل**.</span><span class="sxs-lookup"><span data-stu-id="206cd-125">The screenshot below shows an example of hour and item registrations on a work order in **Work order journals**.</span></span>

![الشكل 1](media/01-consumption.png)


## <a name="split-hours-on-work-orders-with-several-work-order-jobs"></a><span data-ttu-id="206cd-127">تقسيم الساعات على أوامر العمل باستخدام وظائف أوامر عمل متعددة</span><span class="sxs-lookup"><span data-stu-id="206cd-127">Split hours on work orders with several work order jobs</span></span>

<span data-ttu-id="206cd-128">إذا كان أمر العمل يحتوي على عدد كبير من وظائف أمر العمل، فيمكنك تسجيل ساعات العمل باستخدام الوظيفة **تقسيم الساعات**، مما يعني انه يمكن توزيع بند تسجيل ساعة واحد بالتساوي على كل وظيفة أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="206cd-128">If a work order contains several work order jobs, you can register work hours using the **Split hours** functionality, meaning one hour registration line can be distributed evenly on each work order job.</span></span>

1. <span data-ttu-id="206cd-129">انقر فوق **إدارة الأصول** > **عام** > **أوامر العمل** > **جميع أوامر العمل** أو **أوامر العمل النشطة**.</span><span class="sxs-lookup"><span data-stu-id="206cd-129">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="206cd-130">حدد أمر العمل وانقر فوق **دفاتر اليومية**.</span><span class="sxs-lookup"><span data-stu-id="206cd-130">Select the work order and click **Journals**.</span></span>

3. <span data-ttu-id="206cd-131">حدد بند تسجيل الساعات الذي ترغب في تقسيمه، ثم انقر فوق **تقسيم الساعات**.</span><span class="sxs-lookup"><span data-stu-id="206cd-131">Select the hour registration line you want to split, and click **Split hours**.</span></span>

4. <span data-ttu-id="206cd-132">في مربع الحوار **تقسيم الساعات على مهام صيانة أمر العمل**، يظهر اسم العامل الذي سجل دخوله تلقائيًا في حقل **العامل**.</span><span class="sxs-lookup"><span data-stu-id="206cd-132">In the **Split hours on work order maintenance jobs** dialog, the name of the worker who is logged in is automatically shown in the **Worker** field.</span></span> <span data-ttu-id="206cd-133">يمكنك تحديد عامل آخر، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="206cd-133">If required, you can select another worker.</span></span>

5. <span data-ttu-id="206cd-134">حدد فئة لتسجيل الساعات في حقل **الفئة**.</span><span class="sxs-lookup"><span data-stu-id="206cd-134">Select a category for the hour registration in the **Category** field.</span></span>

6. <span data-ttu-id="206cd-135">أدخل عدد ساعات العمل التي سيتم تقسيمها في الحقل **ساعات**.</span><span class="sxs-lookup"><span data-stu-id="206cd-135">Insert number of work hours to be split in the **Hours** field.</span></span>

    ![الشكل 2](media/02-consumption.png)

7. <span data-ttu-id="206cd-137">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="206cd-137">Click **OK**.</span></span>

<span data-ttu-id="206cd-138">*مثال:* في لقطة الشاشة أدناه، تظهر بنود دفتر اليومية لأمر عمل يحتوي على ثلاث مهام خاصة بأمر العمل.</span><span class="sxs-lookup"><span data-stu-id="206cd-138">*Example:* In the screenshot below, journal lines for a work order containing three work order jobs are shown.</span></span> <span data-ttu-id="206cd-139">تم تقسيم البند الأول، الذي يحتوي على ثلاث ساعات عمل، وتم تسجيل ساعة عمل واحدة على كل وظيفة أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="206cd-139">The first line, containing three work hours, has been split, and one work hour is registered on each work order job.</span></span> <span data-ttu-id="206cd-140">بعد إنشاء بنود تسجيل الساعات الثلاثة، تقرر أنت ما يجب القيام به مع بند تسجيل الساعات الأصلي (البند الأول في المثال).</span><span class="sxs-lookup"><span data-stu-id="206cd-140">After the three hour registration lines have been created, you decide what to do with the original hour registration line (the first line in the example).</span></span> <span data-ttu-id="206cd-141">يمكنك الاحتفاظ به كما هو أو حذفه.</span><span class="sxs-lookup"><span data-stu-id="206cd-141">You can keep it as is or delete it.</span></span> 

![الشكل 3](media/03-consumption.png)

## <a name="financial-dimensions-on-consumption-registrations"></a><span data-ttu-id="206cd-143">الأبعاد المالية على تسجيلات الاستهلاك</span><span class="sxs-lookup"><span data-stu-id="206cd-143">Financial dimensions on consumption registrations</span></span>

<span data-ttu-id="206cd-144">عند إجراء تسجيلات استهلاك، تُضاف الأبعاد المالية المرتبطة بأنواع التسجيل المختلفة إلى التسجيلات في تسلسل معين.</span><span class="sxs-lookup"><span data-stu-id="206cd-144">When you make consumption registrations, financial dimensions related to the different registration types are added to the registrations in a specific sequence.</span></span> 

- <span data-ttu-id="206cd-145">*تسجيلات الساعات والمصروفات:* تُضاف أولاً الأبعاد المالية من رأس دفتر اليومية، في حال وجودها.</span><span class="sxs-lookup"><span data-stu-id="206cd-145">*Hour and Expense registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="206cd-146">وبعد ذلك، تُضاف الأبعاد المالية من مشروع أمر العمل ذي الصلة.</span><span class="sxs-lookup"><span data-stu-id="206cd-146">Next, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="206cd-147">وأخيرًا، تُضاف الأبعاد المالية من المورد (العامل).</span><span class="sxs-lookup"><span data-stu-id="206cd-147">Finally, financial dimensions from the resource (worker) are added.</span></span>

- <span data-ttu-id="206cd-148">*تسجيلات الأصناف:* تُضاف أولاً الأبعاد المالية من رأس دفتر اليومية، في حال وجودها.</span><span class="sxs-lookup"><span data-stu-id="206cd-148">*Item registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="206cd-149">ثم تُضاف الأبعاد المالية من مشروع أمر العمل ذي الصلة.</span><span class="sxs-lookup"><span data-stu-id="206cd-149">Then, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="206cd-150">بعد ذلك، تُضاف الأبعاد المالية من الموقع.</span><span class="sxs-lookup"><span data-stu-id="206cd-150">Next, financial dimensions from the site are added.</span></span> <span data-ttu-id="206cd-151">وأخيرًا، تُضاف الأبعاد المالية من الصنف.</span><span class="sxs-lookup"><span data-stu-id="206cd-151">Finally, financial dimensions from the item are added.</span></span>

>[!NOTE]
><span data-ttu-id="206cd-152">بالنسبة إلى كافة أنواع التسجيلات الثلاثة، يتم التحقق من صحة تركيبة الأبعاد المالية، ويتم تجاهل التركيبات غير الصالحة.</span><span class="sxs-lookup"><span data-stu-id="206cd-152">For all three registration types, the financial dimension combination is validated, and invalid combinations are blanked.</span></span> <span data-ttu-id="206cd-153">هذا هو الإعداد القياسي مع تطبيقات Finance and Operations الأخرى.</span><span class="sxs-lookup"><span data-stu-id="206cd-153">This is standard setup with other Finance and Operations apps.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]