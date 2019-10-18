---
title: جدول الصيانة
description: يشرح هذا الموضوع جدول الصيانة في إدارة الأصول.
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
ms.openlocfilehash: af2152b334b51db48b60aa966ab49bf480c29bbc
ms.sourcegitcommit: 6476f27c8d3dced7c2e9a7344a4e378b51a1983e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/27/2019
ms.locfileid: "1922127"
---
# <a name="maintenance-schedule"></a><span data-ttu-id="d4c77-103">جدول الصيانة</span><span class="sxs-lookup"><span data-stu-id="d4c77-103">Maintenance schedule</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="d4c77-104">يحتوي جدول الصيانة على قائمة بكافة خطط الصيانة الوقائية المتوقعة وطلبات الصيانة ودورات الصيانة التي سيتم تنفيذها. ربما تم تحويل بعض بنود الجدول إلى أوامر عمل.</span><span class="sxs-lookup"><span data-stu-id="d4c77-104">The maintenance schedule contains a list of all the expected preventive maintenance plans, maintenance requests, and maintenance rounds to be carried out. Some schedule lines may have been converted to work orders.</span></span>

<span data-ttu-id="d4c77-105">ثمة اختلافات طفيفة بين طرق العرض الأربع لجدول الصيانة، وهذا يتوقف على بنود جدول الصيانة التي ترغب في رؤيتها.</span><span class="sxs-lookup"><span data-stu-id="d4c77-105">The four maintenance schedule views are slightly different, depending on which maintenance schedule lines you want to see.</span></span>

| <span data-ttu-id="d4c77-106">عنصر قائمة</span><span class="sxs-lookup"><span data-stu-id="d4c77-106">Menu item</span></span>                  | <span data-ttu-id="d4c77-107">وصف المحتويات</span><span class="sxs-lookup"><span data-stu-id="d4c77-107">Description of contents</span></span>                                                                                                                                             |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4c77-108">جدول الصيانة بكامله</span><span class="sxs-lookup"><span data-stu-id="d4c77-108">All maintenance schedule</span></span>       | <span data-ttu-id="d4c77-109">تظهر كافة بنود جدول الصيانة.</span><span class="sxs-lookup"><span data-stu-id="d4c77-109">All maintenance schedule lines are shown.</span></span>     |
| <span data-ttu-id="d4c77-110">جدول الأصول لدي</span><span class="sxs-lookup"><span data-stu-id="d4c77-110">My asset schedule</span></span>        | <span data-ttu-id="d4c77-111">تظهر في هذه القائمة كافة بنود جدول الصيانة التي تحتوي على أصول مثبته في مواقع العمل التي ترتبط بها أنت كعامل (الإعداد في [عاملو الصيانة ومجموعات عاملي الصيانة‬](../setup-for-objects/workers-and-worker-groups.md)).</span><span class="sxs-lookup"><span data-stu-id="d4c77-111">All maintenance schedule lines containing assets installed on functional locations to which you are related as a worker (set up in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md)) are shown in this list.</span></span> |
| <span data-ttu-id="d4c77-112">فتح سطور جدول الصيانة</span><span class="sxs-lookup"><span data-stu-id="d4c77-112">Open maintenance schedule lines</span></span> | <span data-ttu-id="d4c77-113">تظهر في هذه القائمة بنود جدول الصيانة بالحالة "تم الإنشاء" - ما يعني انه لم يتم بعد تحويلها إلى أمر عمل أو إهمالها.</span><span class="sxs-lookup"><span data-stu-id="d4c77-113">Maintenance schedule lines with status "Created" - meaning they have not yet been converted to a work order or discarded - are shown in this list.</span></span>                                            |
| <span data-ttu-id="d4c77-114">فتح مجموعات جدول الصيانة</span><span class="sxs-lookup"><span data-stu-id="d4c77-114">Open maintenance schedule pools</span></span> | <span data-ttu-id="d4c77-115">تظهر في هذه القائمة بنود جدول الصيانة المرتبطة بمجموعة أوامر عمل.</span><span class="sxs-lookup"><span data-stu-id="d4c77-115">Maintenance schedule lines related to a work order pool are shown in this list.</span></span>                                                                                                                  |

>[!NOTE]
><span data-ttu-id="d4c77-116">إذا تم تضمين بند جدول صيانة في مجموعات أوامر عمل متعددة، (راجع [مجموعات أوامر العمل](../work-orders/work-order-pools.md))، يظهر سجل واحد لكل مجموعة في **مجموعات جدول الصيانة المفتوحة‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="d4c77-116">If a maintenance schedule line is included in several work order pools (refer to [Work order pools](../work-orders/work-order-pools.md)), one record is shown for each pool in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="d4c77-117">ويتم ذلك لتحسين خيارات التصفية على مجموعات أوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="d4c77-117">This is done to optimize filtering options on work order pools.</span></span>

<span data-ttu-id="d4c77-118">لفتح جدول صيانة:</span><span class="sxs-lookup"><span data-stu-id="d4c77-118">To open a maintenance schedule:</span></span>

1. <span data-ttu-id="d4c77-119">انقر فوق **إدارة الأصول** > **عام‏‎** > **جدول الصيانة** > **جدول الصيانة بكامله** أو **بنود جدول الصيانة المفتوحة** أو **مجموعات جداول الصيانة المفتوحة**.</span><span class="sxs-lookup"><span data-stu-id="d4c77-119">Click **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="d4c77-120">لتحديث جدول الصيانة، انقر فوق **خطة الصيانة** أو **دورات الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="d4c77-120">To update the maintenance schedule, click **Maintenance plan** or **Maintenance rounds**.</span></span> 

3. <span data-ttu-id="d4c77-121">يمكنك تحرير بند جدول الصيانة عن طريق تحديده والنقر فوق **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="d4c77-121">You can edit a maintenance schedule line by selecting it and clicking **Edit**.</span></span> <span data-ttu-id="d4c77-122">على سبيل المثال، يمكنك تحديث مستوى الخدمة أو العامل المسؤول عن مهمة الصيانة بسهولة.</span><span class="sxs-lookup"><span data-stu-id="d4c77-122">For example, you can easily update the service level or the worker responsible for the job.</span></span> <span data-ttu-id="d4c77-123">يمكنك تحرير فقط بنود جدول الصيانة التي لم يتم بعد ربطها بأمر عمل.</span><span class="sxs-lookup"><span data-stu-id="d4c77-123">You can only edit maintenance schedule lines that have not yet been connected to a work order.</span></span>

4. <span data-ttu-id="d4c77-124">يمكنك حذف بند جدول الصيانة عن طريق تحديده في صفحة القائمة والنقر فوق **حذف**.</span><span class="sxs-lookup"><span data-stu-id="d4c77-124">You can delete a maintenance schedule line by selecting it in the list page and clicking **Delete**.</span></span>

5. <span data-ttu-id="d4c77-125">يمكنك تجاهل بند جدول الصيانة عن طريق تحديده في صفحة القائمة والنقر فوق **تجاهل**.</span><span class="sxs-lookup"><span data-stu-id="d4c77-125">You can discard a maintenance schedule line by selecting it in the list page and clicking **Discard**.</span></span> <span data-ttu-id="d4c77-126">تكون هذه الوظيفة مفيدة إذا كان لدى الأصل خطة صيانة من 2,000 كيلومتر وخطة صيانة من 10,000 كيلومتر.</span><span class="sxs-lookup"><span data-stu-id="d4c77-126">This function is useful if, for example, an asset has a 2,000 km maintenance plan and a 10,000 km maintenance plan.</span></span> <span data-ttu-id="d4c77-127">وبعد ذلك، قد ترغب في تجاهل البند الذي تم إنشاؤه من خطة الصيانة 2,000 كيلومتر عندما يحدث في نفس الوقت مع خطة 10,000 كيلومتر و20,000 كيلومتر و30,000 كيلومتر وما إلى ذلك.</span><span class="sxs-lookup"><span data-stu-id="d4c77-127">Then, you may want to discard the line created from the 2,000 km maintenance plan when it coincides with 10,000 km, 20,000 km, 30,000 km, and so on.</span></span> <span data-ttu-id="d4c77-128">إذا قمت بتجاهل بند جدول صيانة مرتبط بخطة صيانة، فلن يظهر هذا البند أبدًا عند جدولة خطة الصيانة هذه.</span><span class="sxs-lookup"><span data-stu-id="d4c77-128">If you discard a maintenance schedule line related to a maintenance plan, that line will never again appear when that maintenance plan is scheduled.</span></span>

6. <span data-ttu-id="d4c77-129">يمكنك تحديد عدد من بنود جدول الصيانة في **جدول الصيانة بكامله** والنقر فوق **مجموعات أوامر العمل**، إذا أردت تضمين كافة البنود المحددة في مجموعة أوامر العمل نفسها.</span><span class="sxs-lookup"><span data-stu-id="d4c77-129">You can select a number of maintenance schedule lines in **All maintenance schedule** and click **Work order pool**, if you want all selected lines to be included in the same work order pool.</span></span>

7. <span data-ttu-id="d4c77-130">يمكنك تحديد عدد من بنود جدول الصيانة في **جدول الصيانة بكامله** أو **بنود جدول الصيانة المفتوحة** أو **مجموعات جداول الصيانة المفتوحة** والنقر فوق **تعديل الجدول** إذا أردت إجراء التعديلات نفسها على عدة بنود.</span><span class="sxs-lookup"><span data-stu-id="d4c77-130">You can select a number of maintenance schedule lines in **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools** and click **Adjust schedule** if you want to make the same adjustments on several lines.</span></span> <span data-ttu-id="d4c77-131">يمكنك تغيير تواريخ البدء والانتهاء المتوقعة ومستوى الخدمة ومجموعة عاملي الصيانة المسؤولين أو عامل الصيانة المسؤول الذي يرتبط ببنود جدول الصيانة المحددة.</span><span class="sxs-lookup"><span data-stu-id="d4c77-131">You can change expected start and end dates, service level, and the responsible maintenance worker group or responsible maintenance worker related to the selected maintenance schedule lines.</span></span>

- <span data-ttu-id="d4c77-132">عند ربط بند جدول صيانة بأمر عمل، سيظهر معرف أمر العمل في حقل **أمر العمل**.</span><span class="sxs-lookup"><span data-stu-id="d4c77-132">When a maintenance schedule line has been related to a work order, the work order ID will be displayed in the **Work order** field.</span></span>  
- <span data-ttu-id="d4c77-133">في طريقة عرض تفاصيل **كل الأصول‬** > علامة التبويب السريعة **خطط صيانة الأصول**، يمكنك تحديد خطط صيانة للأصل.</span><span class="sxs-lookup"><span data-stu-id="d4c77-133">In **All assets** details view > **Asset maintenance plans** FastTab, you can select maintenance plans for the asset.</span></span> <span data-ttu-id="d4c77-134">في وقت لاحق، إذا قمت بحذف بند خطة صيانة متعلق بأصل في **كل الأصول**، فإنك أيضًا تحذف تلقائيًا كل بنود جدول الصيانة ذات الحالة "تم إنشاؤها" والتي تم إنشاؤها استنادًا إلى خطة الصيانة هذه.</span><span class="sxs-lookup"><span data-stu-id="d4c77-134">Later, if you delete a maintenance plan line related to an asset in **All assets**, you also automatically delete all maintenance schedule lines with status "Created" that have been created based on that maintenance plan.</span></span> <span data-ttu-id="d4c77-135">راجع أيضًا [إنشاء أصل](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="d4c77-135">See also [Create an asset](../objects/create-an-object.md).</span></span>

<span data-ttu-id="d4c77-136">يعرض الرسم التوضيحي أدناه صفحة قائمة **جدول الصيانة بكامله**.</span><span class="sxs-lookup"><span data-stu-id="d4c77-136">The illustration below shows the **All maintenance schedule** list page.</span></span>

![الشكل 1](media/16-preventive-maintenance.png)

