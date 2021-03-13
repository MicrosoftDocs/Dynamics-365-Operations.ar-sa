---
title: أوامر العمل المنشأة يدويًا
description: يوضح هذا الموضوع كيفية إنشاء أوامر العمل يدويًا في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderTableCreateRelated, EntAssetWorkOrderTableCreate, EntAssetWorkOrderTableCopy
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8c787dbc9889139df76b9b102deb18fce567e382
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/16/2021
ms.locfileid: "5017858"
---
# <a name="manually-created-work-orders"></a><span data-ttu-id="fc585-103">أوامر العمل التي تم إنشاؤها يدويًا</span><span class="sxs-lookup"><span data-stu-id="fc585-103">Manually created work orders</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="fc585-104">يمكنك إنشاء أوامر العمل يدويًا باستخدام طريقتين.</span><span class="sxs-lookup"><span data-stu-id="fc585-104">You can create work orders manually in two ways:</span></span>

- <span data-ttu-id="fc585-105">في صفحة **جميع أوامر العمل** أو **أوامر العمل النشطة**</span><span class="sxs-lookup"><span data-stu-id="fc585-105">On the **All work orders** or **Active work orders** page</span></span> 
- <span data-ttu-id="fc585-106">في صفحة **جميع طلبات الصيانة** أو **طلبات الصيانة النشطة** أو **طلبات الصيانة الخاصة بموقع العمل لدي** .</span><span class="sxs-lookup"><span data-stu-id="fc585-106">On the **All maintenance requests** or **Active maintenance requests** or **My functional location maintenance requests** page</span></span> 

## <a name="create-work-order"></a><span data-ttu-id="fc585-107">إنشاء أمر العمل</span><span class="sxs-lookup"><span data-stu-id="fc585-107">Create work order</span></span>

1. <span data-ttu-id="fc585-108">حدد **إدارة الأصول** > **مشترك** > **أوامر العمل** > **جميع أوامر العمل** أو **أوامر العمل النشطة**.</span><span class="sxs-lookup"><span data-stu-id="fc585-108">Selece **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="fc585-109">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="fc585-109">Select **New**.</span></span>

3. <span data-ttu-id="fc585-110">في مربع الحوار **إنشاء أمر العمل** ، حدد نوع أمر العمل قم بإدخال حقل نوع **أمر العمل** .</span><span class="sxs-lookup"><span data-stu-id="fc585-110">In the **Create work order** dialog, select a work order type in the **Work order type** field.</span></span>

4. <span data-ttu-id="fc585-111">إذا لزم الأمر، حدد **وصف**.</span><span class="sxs-lookup"><span data-stu-id="fc585-111">If required, select a **Description**.</span></span>

5. <span data-ttu-id="fc585-112">حدد الأصل في حقل **الأصل** .</span><span class="sxs-lookup"><span data-stu-id="fc585-112">In the **Asset** field, select the asset.</span></span>

>[!NOTE]
><span data-ttu-id="fc585-113">عند تحديد أحد الأصول، قد تتوفر ثلاث علامات تبويب في القائمة المنسدلة لـ **الأصل** :</span><span class="sxs-lookup"><span data-stu-id="fc585-113">When you select an asset, three tabs might be available in the **Asset** drop-down:</span></span> 

- <span data-ttu-id="fc585-114">**الأصول النشطة** - تحتوي علامة التبويب هذه على قائمة بكافة الأصول التي تكون حالة دورة حياة الأصل فيها "نشطة".</span><span class="sxs-lookup"><span data-stu-id="fc585-114">**Active assets** - This tab contains a list of all assets that have an "Active" asset lifecycle state.</span></span> 
- <span data-ttu-id="fc585-115">**طريقة عرض الأصول** - تعرض علامة التبويب هذه طريقة عرض الشجرة لمواقع العمل والأصول المثبتة على تلك المواقع.</span><span class="sxs-lookup"><span data-stu-id="fc585-115">**Asset view** - This tab displays a tree view of functional locations and the assets installed on them.</span></span>
- <span data-ttu-id="fc585-116">**الأصول الخاصة بي** - تحتوي علامة التبويب هذه على الأصول المرتبطة بمواقع العمل التي يمكن تخصيصها (العامل الذي تم تسجيل دخوله إلى النظام).</span><span class="sxs-lookup"><span data-stu-id="fc585-116">**My assets** - This tab contains assets that are related to the functional locations that you (the worker who is signed in to the system) may be allocated to.</span></span> <span data-ttu-id="fc585-117">(لمزيد من المعلومات حول الإعداد، راجع [عمال الصيانة ومجموعات العاملين](../setup-for-objects/workers-and-worker-groups.md).) في حالة عدم إعداد أية مواقع عمل على عامل في [عاملو ومجموعات عاملي الصيانة](../setup-for-objects/workers-and-worker-groups.md)، فلن تكون علامة التبويب **الأصول الخاصة بي** متاحة.</span><span class="sxs-lookup"><span data-stu-id="fc585-117">(For information about the setup, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).) If no functional locations are set up on a worker in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md), the **My assets** tab isn't available.</span></span> 

6. <span data-ttu-id="fc585-118">حدد نوع مهمة الصيانة لأمر العمل في الحقل **نوع مهمة الصيانة** .</span><span class="sxs-lookup"><span data-stu-id="fc585-118">In the **Maintenance job type** field, select a maintenance job type for the work order.</span></span>

7. <span data-ttu-id="fc585-119">إذا لزم الأمر، حدد **متغير نوع مهمة الصيانة** و **المعاملات**.</span><span class="sxs-lookup"><span data-stu-id="fc585-119">If required, select **Maintenance job type variant** and **Trade**.</span></span>

8. <span data-ttu-id="fc585-120">إذا لزم الأمر، يمكنك تغيير مستوى خدمه أمر العمل‏‎ في حقل **مستوى الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="fc585-120">If required, you can change the work order service level in the **Service level** field.</span></span>

9. <span data-ttu-id="fc585-121">حدد تواريخ **‏‫البدء المتوقع‬** و **‏‫الانتهاء المتوقع‬** في الحقول ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="fc585-121">Select **Expected start** and **Expected end** dates in the related fields.</span></span>

10. <span data-ttu-id="fc585-122">انقر فوق **موافق** لإنشاء أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="fc585-122">Click **OK** to create the work order.</span></span>

11. <span data-ttu-id="fc585-123">في صفحة القائمة **‏‫جميع أوامر العمل‬** ، يمكنك تحرير أمر العمل كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="fc585-123">On the **All work orders** list page, you can edit the work order as you require.</span></span>

<span data-ttu-id="fc585-124">لاحظ النقاط التالية:</span><span class="sxs-lookup"><span data-stu-id="fc585-124">Note the following points:</span></span>

- <span data-ttu-id="fc585-125">في صفحة القائمة **جميع أوامر العمل** ، يمكنك إضافة العديد من الأصول إلى أمر عمل في طريقه عرض التفاصيل عن طريق إضافة بنود على علامة التبويب السريعة **مهام صيانة أمر العمل** .</span><span class="sxs-lookup"><span data-stu-id="fc585-125">In the details view on the **All work orders** list page, you can add several assets to a work order by adding lines on the **Work order maintenance jobs** FastTab.</span></span> <span data-ttu-id="fc585-126">على الأصل، يمكنك تحديد فقط أنواع مهام الصيانة التي تم تحديدها على نوع الأصل المحدد للأصل.</span><span class="sxs-lookup"><span data-stu-id="fc585-126">On an asset, you can select only the maintenance job types that are defined on the asset type that is selected on the asset.</span></span>  

- <span data-ttu-id="fc585-127">إذا قمت بتغيير مستوى خدمة الأصل أو أهمية الأصل بعد استخدامه فعليًا في أمر عمل، فلن يتم تحديث مستوى خدمة الأصل أو أهميته في أمر العمل وفقًا لذلك.</span><span class="sxs-lookup"><span data-stu-id="fc585-127">If you change an asset service level or an asset criticality after you've used the asset on a work order, the service level or criticality on the work order isn't updated accordingly.</span></span> <span data-ttu-id="fc585-128">لمزيد من المعلومات حول مستويات الخدمة والأهمية، راجع [مستويات خدمه الأصل](../setup-for-objects/object-priorities.md) و [أنواع أهمية الأصل](../setup-for-objects/object-criticalities.md).</span><span class="sxs-lookup"><span data-stu-id="fc585-128">For more information about service levels and criticalities, see [Asset service levels](../setup-for-objects/object-priorities.md) and [Asset criticality types](../setup-for-objects/object-criticalities.md).</span></span>

- <span data-ttu-id="fc585-129">يتم إعادة حساب مستوى الأهمية في أمر العمل في كل مرة تتم فيها إضافة وظيفة أمر العمل إلى أمر العمل أو حذفه منه.</span><span class="sxs-lookup"><span data-stu-id="fc585-129">Criticality on a work order is recalculated every time a work order job is added to or deleted from the work order.</span></span>

- <span data-ttu-id="fc585-130">في‏‫ عرض تفاصيل **جميع أوامر العمل** > علامة التبويب **الرأس** > علامة التبويب السريعة **الجدول** ، يمكنك تحديد ‏‫مجموعة عامل الصيانة المسؤولة أو عامل الصيانة المسؤول في الحقلين **المجموعة المسؤولة** أو **المسؤول** .</span><span class="sxs-lookup"><span data-stu-id="fc585-130">In the **All work orders** details view > **Header** tab > **Schedule** FastTab, in the **Responsible group** or **Responsible** field, you can select a responsible maintenance worker group or a responsible maintenance worker.</span></span> <span data-ttu-id="fc585-131">يمكن تغيير هذه الإعدادات عندما يكون أمر العمل نشطًا.</span><span class="sxs-lookup"><span data-stu-id="fc585-131">These settings can be changed while the work order is active.</span></span> <span data-ttu-id="fc585-132">على سبيل المثال، يمكن تغييرها عند تغيير حالة دورة حياة أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="fc585-132">For example, they can be changed when the work order lifecycle state changes.</span></span> <span data-ttu-id="fc585-133">يستند التحديد التلقائي الذي تم اجراؤه أثناء إنشاء أمر العمل إلى الإعداد في صفحة **عاملو الصيانة المسؤولون** .</span><span class="sxs-lookup"><span data-stu-id="fc585-133">The automatic selection that is made during work order creation is based on the setup on the **Responsible maintenance workers** page.</span></span> <span data-ttu-id="fc585-134">إذا قمت بإضافة أو إزالة وظائف أمر العمل بعد إنشاء أمر العمل وإذا كان الحقلين **المجموعة المسؤولة** و **المسؤول** فارغًا عندما تقوم بتحديث أمر العمل، يبحث إدارة الأصول عن التطابق محتمل في صفحة الإعداد لمجموعة عامل الصيانة المسؤولة أو عامل صيانة المسؤول.</span><span class="sxs-lookup"><span data-stu-id="fc585-134">If you add or remove work order jobs after you've created a work order, and if the **Responsible group** and **Responsible** fields are blank when you update the work order, Asset Management tries to find a responsible maintenance worker group or a responsible maintenance worker for a possible match on the setup page.</span></span> <span data-ttu-id="fc585-135">إذا كان الحقلين **المجموعة المسؤولة‬‏‫** أو **المسؤول** معبأ بشكل مسبق عند تحديث أمر العمل، فلا يتم إجراء أي تغييرات.</span><span class="sxs-lookup"><span data-stu-id="fc585-135">If the **Responsible group** or **Responsible** field is already set when you update the work order, no changes are made.</span></span> <span data-ttu-id="fc585-136">للحصول على معلومات حول عاملو الصيانة المسؤولون ومجموعات العامل المسؤول، راجع [عاملو الصيانة المسؤولون‬](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="fc585-136">For more information about responsible maintenance workers and worker groups, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>

- <span data-ttu-id="fc585-137">من صفحة [حالة الصيانة](../controlling-and-reporting/maintenance-status.md) ، يمكنك إجراء عملية حسابية للحصول على نظرة عامة حول حمل العمل فيما يتعلق بأوامر العمل الواردة والمكتملة.</span><span class="sxs-lookup"><span data-stu-id="fc585-137">From the [Maintenance status](../controlling-and-reporting/maintenance-status.md) page, you can do a calculation to get an overview of the workload for incoming and completed work orders.</span></span>  

- <span data-ttu-id="fc585-138">في طريقه عرض التفاصيل لصفحة **جميع أوامر العمل** ، على علامة التبويب السريعة **تفاصيل البند** ، يمكنك استخدام حقلي **الطول** و **العرض** لإضافة الإحداثيات الجغرافية للأصل المحدد في وظيفة أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="fc585-138">In the details view of the **All work orders** page, on the **Line details** FastTab, you can use the **Latitude** and **Longitude** fields to add geographic coordinates for the asset that is selected on the work order job.</span></span>  


## <a name="create-related-work-order"></a><span data-ttu-id="fc585-139">إنشاء أمر عمل ذي صلة</span><span class="sxs-lookup"><span data-stu-id="fc585-139">Create related work order</span></span>

<span data-ttu-id="fc585-140">يمكنك إنشاء أمر عمل يرتبط بأمر العمل الموجود.</span><span class="sxs-lookup"><span data-stu-id="fc585-140">You can create a work order that is related to an existing work order.</span></span> <span data-ttu-id="fc585-141">وتكون هذه الإمكانية مفيدة إذا كنت ترغب على سبيل المثال في تسجيل أوامر عمل أولية وثانوية.</span><span class="sxs-lookup"><span data-stu-id="fc585-141">This capability is useful if, for example, you want to work with primary and secondary work orders.</span></span> <span data-ttu-id="fc585-142">يستند أمر العمل الجديد إلى وظيفة أمر عمل من أمر عمل موجود.</span><span class="sxs-lookup"><span data-stu-id="fc585-142">A new work order is based on a work order job from an existing work order.</span></span>

1. <span data-ttu-id="fc585-143">حدد **إدارة الأصول** > **مشترك** > **أوامر العمل** > **جميع أوامر العمل** أو **أوامر العمل النشطة**.</span><span class="sxs-lookup"><span data-stu-id="fc585-143">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="fc585-144">حدد أمر العمل لإنشاء أمر عمل مرتبط به.</span><span class="sxs-lookup"><span data-stu-id="fc585-144">Select the work order to create a related work order for.</span></span>

3. <span data-ttu-id="fc585-145">في جزء الإجراءات، ضمن علامة التبويب **أمر العمل** ، في مجموعة **‏‫جديد** ، حدد **أمر العمل المرتبط**.</span><span class="sxs-lookup"><span data-stu-id="fc585-145">On the Action Pane, on the **Work order** tab, in the **New** group, select **Related work order**.</span></span>

4. <span data-ttu-id="fc585-146">في مربع حوار **إنشاء أمر عمل مرتبط** ، حدد وظيفة أمر العمل التي تريد إنشاء أمر العمل المرتبط بها في حقل **وظيفة أمر العمل** .</span><span class="sxs-lookup"><span data-stu-id="fc585-146">In the **Create related work order** dialog, in the **Work order job** field, select the work order job to create a related work order for.</span></span>

5. <span data-ttu-id="fc585-147">في الحقل **نوع مهمة الصيانة** ، حدد نوع مهمة الصيانة.</span><span class="sxs-lookup"><span data-stu-id="fc585-147">Select a maintenance job type in the **Maintenance job type** field.</span></span>

6. <span data-ttu-id="fc585-148">في الحقلين **متغير نوع مهمة الصيانة** و **المعاملة‏‎** ، حدد المتغير والمعاملة‏‎ المرتبطة بنوع مهمة الصيانة، كما تقتضي الحاجة.</span><span class="sxs-lookup"><span data-stu-id="fc585-148">Select a related maintenance job type variant and trade in the **Maintenance job type variant** and **Trade** fields, as you require.</span></span>

7. <span data-ttu-id="fc585-149">إذا كان أمر العمل هذا هو أول أمر عمل مرتبط تم إنشاؤه لأمر العمل المحدد، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="fc585-149">If this work order is the first related work order that has been created for the selected work order, follow these steps:</span></span>
    1. <span data-ttu-id="fc585-150">حدد الخيار **أمر عمل جديد** .</span><span class="sxs-lookup"><span data-stu-id="fc585-150">Select the **New work order** option.</span></span>
    2. <span data-ttu-id="fc585-151">في الحقل **نوع أمر العمل** ، حدد نوع أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="fc585-151">In  the **Work order type** field, select a work order type.</span></span>
    3. <span data-ttu-id="fc585-152">في الحقل **الوصف** ، ادخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="fc585-152">In the **Description**, enter a description.</span></span>
    4. <span data-ttu-id="fc585-153">غيّر مستوى خدمة أمر العمل‏‎ في حقل **مستوى الخدمة** إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="fc585-153">In the **Service level** field, change the work order service level as you require.</span></span>
    5. <span data-ttu-id="fc585-154">في الحقلين **‏‫تاريخ البدء المتوقع‬** و **‏‫تاريخ الانتهاء المتوقع** ، حدد تاريخي البدء والانتهاء المتوقعين.</span><span class="sxs-lookup"><span data-stu-id="fc585-154">In the **Expected start** and **Expected end** fields, select the expected start and end dates.</span></span>
    6. <span data-ttu-id="fc585-155">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="fc585-155">Select **OK**.</span></span> <span data-ttu-id="fc585-156">يظهر أمر العمل المرتبط الجديد في صفحة القائمة **جميع أوامر العمل** .</span><span class="sxs-lookup"><span data-stu-id="fc585-156">The new related work order is shown on the **All work orders** list page.</span></span>  

8. <span data-ttu-id="fc585-157">إذا كان أمر العمل الذي تقوم بإنشائه لأمر العمل المرتبط به يحتوي على أوامر عمل مرتبطة بالفعل، اتبع الخطوات التالية لإضافة وظيفة أمر عمل جديدة إلى أمر العمل المرتبط الموجود.</span><span class="sxs-lookup"><span data-stu-id="fc585-157">If the work order that you're creating this related work order for already has related work orders, follow these steps to add a new work order job to an existing related work order:</span></span>
    1. <span data-ttu-id="fc585-158">حدد الخيار **إضافة إلى أمر عمل مرتبط** .</span><span class="sxs-lookup"><span data-stu-id="fc585-158">Select the **Add to related work order** option.</span></span>
    2. <span data-ttu-id="fc585-159">في الحقل **أمر العمل** ، حدد أمر العمل المرتبط الذي ترغب في إضافة وظيفة أمر عمل جديدة اليه.</span><span class="sxs-lookup"><span data-stu-id="fc585-159">In the **Work order** field, select the related work order to add a new work order job to.</span></span>
    3. <span data-ttu-id="fc585-160">غيّر مستوى خدمة أمر العمل‏‎ في حقل **مستوى الخدمة** إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="fc585-160">In the **Service level** field, change the work order service level as you require.</span></span>
    4. <span data-ttu-id="fc585-161">في الحقلين **‏‫تاريخ البدء المتوقع‬** و **‏‫تاريخ الانتهاء المتوقع** ، قم بتغيير تاريخي البدء والانتهاء المتوقعين، كما تقضي الحاجة.</span><span class="sxs-lookup"><span data-stu-id="fc585-161">In the **Expected start** and **Expected end** fields, change the expected start and end dates as you require.</span></span>
    5. <span data-ttu-id="fc585-162">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="fc585-162">Select **OK**.</span></span> <span data-ttu-id="fc585-163">تًضاف وظيفة أمر العمل إلى أمر العمل المرتبط الموجود.</span><span class="sxs-lookup"><span data-stu-id="fc585-163">The work order job is added to the existing related work order.</span></span>

<span data-ttu-id="fc585-164">يوضح الرسم التوضيحي المبين أدناه مثال لمربع حوار **إنشاء أمر عمل مرتبط‬** .</span><span class="sxs-lookup"><span data-stu-id="fc585-164">The illustration below shows an example of the **Create related work order** dialog.</span></span>

![الشكل 1](media/03-work-orders.png)

>[!NOTE]
><span data-ttu-id="fc585-166">إذا قمت بإعداد قناع أمر عمل مرتبط في **معلمات إدارة الأصول‬** > **علامة تبويب أوامر العمل** > حقل **قناع أمر العمل المرتبط** ، يتم إنشاء معرفات أمر العمل وفقًا لإعداد القناع.</span><span class="sxs-lookup"><span data-stu-id="fc585-166">If you've set up a related work order mask in **Asset management parameters** > **Work orders** tab > **Related work order mask** field, work order IDs are created according to the mask setup.</span></span> <span data-ttu-id="fc585-167">إذا لم يتم إعداد قناع أمر عمل مرتبط، يُستخدم معرف أمر العمل التالي المتاح لأوامر العمل المرتبطة.</span><span class="sxs-lookup"><span data-stu-id="fc585-167">If no related work order mask is set up, the next available work order ID is used for related work orders.</span></span>

## <a name="copy-a-work-order"></a><span data-ttu-id="fc585-168">نسخ أمر العمل</span><span class="sxs-lookup"><span data-stu-id="fc585-168">Copy a work order</span></span>

<span data-ttu-id="fc585-169">يمكنك إنشاء أمر عمل جديد بسرعة من أمر عمل موجود.</span><span class="sxs-lookup"><span data-stu-id="fc585-169">You can quickly create a new work order from an existing work order.</span></span> <span data-ttu-id="fc585-170">وتختلف طريقة التعامل هذه مع أوامر العمل عن إنشاء أوامر العمل بالاستناد إلى [خطط الصيانة](../preventive-and-reactive-maintenance/maintenance-plans.md).</span><span class="sxs-lookup"><span data-stu-id="fc585-170">This way of working with work orders differs from the creation of work orders based on [maintenance plans](../preventive-and-reactive-maintenance/maintenance-plans.md).</span></span> <span data-ttu-id="fc585-171">من المفيد، على سبيل المثال، إذا كان أمر العمل يحتوي على عدد كبير من وظائف أمر العمل، ويجب إكمال الوظائف المتغيرة على أصول مختلفة في فترات زمنية منتظمة.</span><span class="sxs-lookup"><span data-stu-id="fc585-171">It's useful if, for example, a work order contains many work order jobs, and the various jobs should be completed on different assets at regular intervals.</span></span>

1. <span data-ttu-id="fc585-172">حدد **إدارة الأصول** > **مشترك** > **أوامر العمل** > **جميع أوامر العمل** أو **أوامر العمل النشطة**.</span><span class="sxs-lookup"><span data-stu-id="fc585-172">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="fc585-173">حدد أمر العمل الذي تريد نسخ المحتوى منه.</span><span class="sxs-lookup"><span data-stu-id="fc585-173">Select the work order to copy content from.</span></span>

3. <span data-ttu-id="fc585-174">في جزء الإجراءات، ضمن علامة التبويب **أمر العمل** ، في مجموعة **‏‫جديد** ، حدد **نسخ مر العمل**.</span><span class="sxs-lookup"><span data-stu-id="fc585-174">On the Action Pane > **Work order** tab > **New** group, select **Copy work order**.</span></span>

4. <span data-ttu-id="fc585-175">يظهر إعداد أمر العمل من أمر العمل المحدد.</span><span class="sxs-lookup"><span data-stu-id="fc585-175">The work order setup from the selected work order is shown.</span></span> <span data-ttu-id="fc585-176">يمكنك تحرير بعض الحقول، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="fc585-176">You can edit some of the fields as you require.</span></span>

5. <span data-ttu-id="fc585-177">حدد **موافق** لإنشاء أمر العمل الجديد.</span><span class="sxs-lookup"><span data-stu-id="fc585-177">Select **OK** to create the new work order.</span></span>

6. <span data-ttu-id="fc585-178">في صفحة القائمة **‏‫جميع أوامر العمل‬** ، يمكنك تحرير أمر العمل كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="fc585-178">On the **All work orders** list page, you can edit the work order as you require.</span></span>

>[!NOTE]
><span data-ttu-id="fc585-179">عند إنشاء أمر العمل الجديد، يتم نسخ بعض المعلومات مباشرة من أمر العمل الموجود.</span><span class="sxs-lookup"><span data-stu-id="fc585-179">When the new work order is created, some information is copied directly from the existing work order.</span></span> <span data-ttu-id="fc585-180">لا يتم نسخ معلومات حول التنبؤات، والأدوات، وقوائم فحص الصيانة، وموقع العمل، والعناوين، والجدولة.</span><span class="sxs-lookup"><span data-stu-id="fc585-180">Information about forecasts, tools, maintenance checklists, functional location, addresses, and scheduling isn't copied.</span></span> <span data-ttu-id="fc585-181">بدلاً من ذلك، تتم تهيئته من الإعداد الحالي في إدارة الأصول.</span><span class="sxs-lookup"><span data-stu-id="fc585-181">Instead, it's initialized from the current setup in Asset Management.</span></span> <span data-ttu-id="fc585-182">وبالتالي، إذا تم تغيير تلك المعلومات بين الوقت الذي تم فيه إنشاء أمر العمل الأول ووقت القيام بنسخه من أمر العمل، سيتم تضمين التغييرات في أمر العمل الجديد.</span><span class="sxs-lookup"><span data-stu-id="fc585-182">Therefore, if that information was changed between the time when the first work order was created and the time when you made a copy of the work order, the changes are included in the new work order.</span></span> <span data-ttu-id="fc585-183">تحتوي الأمثلة على التغيرات في التنبؤات أو التحديثات على قوائم فحص الصيانة.</span><span class="sxs-lookup"><span data-stu-id="fc585-183">Examples include changes to forecasts and updates to maintenance checklists.</span></span>

<span data-ttu-id="fc585-184">يبين الرسم التوضيحي التالي مثالاً لمربع الحوار **نسخ أمر العمل**.</span><span class="sxs-lookup"><span data-stu-id="fc585-184">The illustration below shows an example of the **Copy work order** dialog.</span></span>

![الشكل 2](media/04-work-orders.png)


## <a name="create-a-work-order-based-on-a-maintenance-request"></a><span data-ttu-id="fc585-186">إنشاء أمر عمل استنادً إلى طلب صيانة</span><span class="sxs-lookup"><span data-stu-id="fc585-186">Create a work order based on a maintenance request</span></span>

1. <span data-ttu-id="fc585-187">حدد **إدارة الأصول** > **مشترك‏‎** > **طلبات الصيانة** > **جميع طلبات الصيانة** أو **طلبات الصيانة النشطة**.</span><span class="sxs-lookup"><span data-stu-id="fc585-187">Select **Asset management** > **Common** > **Maintenance requests** > **All maintenance requests** or **Active maintenance requests**.</span></span>

2. <span data-ttu-id="fc585-188">حدد طلب الصيانة الذي ترغب في إنشاء أمر عمل له، ثم انقر فوق **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="fc585-188">Select the maintenance request to create a work order for, and click **Edit**.</span></span>

3. <span data-ttu-id="fc585-189">في جزء الإجراءات، ضمن علامة التبويب **طلب صيانة** ، في مجموعة **‏‫جديد** ، حدد **أمر العمل**.</span><span class="sxs-lookup"><span data-stu-id="fc585-189">On the Action Pane > **Maintenance request** tab > **New** group, select **Work order**.</span></span>

4. <span data-ttu-id="fc585-190">في مربع الحوار **أمر العمل** ، قم بتعيين الحقول.</span><span class="sxs-lookup"><span data-stu-id="fc585-190">In the **Work order** dialog, set the fields.</span></span> <span data-ttu-id="fc585-191">إذا تم تحديد نوع مهمة صيانة في طلب الصيانة، يمكنك تحديد نوع مهمة صيانة أخرى، عند إنشاء أمر العمل، بحسب مقتضى الحال.</span><span class="sxs-lookup"><span data-stu-id="fc585-191">If a maintenance job type has been selected in the maintenance request, you can select a different maintenance job type when you create the work order, as you require.</span></span>

5. <span data-ttu-id="fc585-192">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="fc585-192">Select **OK**.</span></span> <span data-ttu-id="fc585-193">رسالة تُخطرك أنه تم إنشاء أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="fc585-193">A message notifies you that the work order has been created.</span></span>

6. <span data-ttu-id="fc585-194">لعرض أوامر العمل المتصلة بطلب صيانة، حدد طلب الصيانة في صفحة **جميع طلبات الصيانة** أو صفحة القائمة **طلبات الصيانة النشطة** .</span><span class="sxs-lookup"><span data-stu-id="fc585-194">To view the work orders that are connected to a maintenance request, on the **All maintenance requests** or **Active maintenance requests** list page, select the maintenance request.</span></span> <span data-ttu-id="fc585-195">ثم بعد ذلك، في جزء الإجراءات، ضمن علامة التبويب **طلب صيانة** ، في مجموعة **‏‫عرض** ، حدد **أوامر العمل**.</span><span class="sxs-lookup"><span data-stu-id="fc585-195">Then, on the Action Pane, on the **Maintenance request** tab, in the **View** group, select **Work orders**.</span></span>


<span data-ttu-id="fc585-196">يبين الرسم التوضيحي التالي مثالاً لمربع الحوار **إنشاء أمر العمل** .</span><span class="sxs-lookup"><span data-stu-id="fc585-196">The illustration below shows an example of the **Create work order** dialog.</span></span>

![الشكل 3](media/05-work-orders.png)


>[!NOTE]
><span data-ttu-id="fc585-198">إذا كنت ترغب في إنشاء أوامر العمل تلقائيًا، يمكنك جدولة مهام خطط الصيانة، أو يمكنك إعداد "الإنشاء التلقائي" لـ [خطط الصيانة](../preventive-and-reactive-maintenance/maintenance-plans.md) أو [دورات الصيانة](../preventive-and-reactive-maintenance/maintenance-rounds.md) على أحد الأصول.</span><span class="sxs-lookup"><span data-stu-id="fc585-198">If you want work orders to be created automatically, you can schedule maintenance plan jobs, or you can set up "Auto create" [maintenance plans](../preventive-and-reactive-maintenance/maintenance-plans.md) or [maintenance rounds](../preventive-and-reactive-maintenance/maintenance-rounds.md) on an asset.</span></span> <span data-ttu-id="fc585-199">يكون لأوامر العمل المنشأة من طلبات صيانة في صفحة القائمة **جدول الصيانة بكامله** أنواع مهام الصيانة المحددة في طلبات الصيانة.</span><span class="sxs-lookup"><span data-stu-id="fc585-199">Work orders that are created from maintenance requests on the **All maintenance schedule** list page have the maintenance job types that are selected on the maintenance requests.</span></span>

