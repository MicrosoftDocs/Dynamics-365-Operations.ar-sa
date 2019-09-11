---
title: أوامر العمل المنشأة يدويًا
description: يوضح هذا الموضوع كيفية إنشاء أوامر العمل يدويًا في إدارة الأصول.
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
ms.openlocfilehash: 261448a134a7c1aacfbb4ea6f954ce03a63c23e2
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875482"
---
# <a name="manually-created-work-orders"></a><span data-ttu-id="32876-103">أوامر العمل المنشأة يدويًا</span><span class="sxs-lookup"><span data-stu-id="32876-103">Manually created work orders</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="32876-104">يمكنك إنشاء أوامر العمل يدويًا باستخدام طريقتين.</span><span class="sxs-lookup"><span data-stu-id="32876-104">You can create work orders manually in two ways:</span></span>

- <span data-ttu-id="32876-105">في **جميع أوامر العمل** أو **أوامر العمل النشطة**</span><span class="sxs-lookup"><span data-stu-id="32876-105">in **All work orders** or **Active work orders**</span></span>  
- <span data-ttu-id="32876-106">في **جميع طلبات الصيانة** أو **طلبات الصيانة النشطة** أو **طلبات الصيانة الخاصة بموقع العمل لدي**.</span><span class="sxs-lookup"><span data-stu-id="32876-106">in **All maintenance requests** or **Active maintenance requests** or **My functional location maintenance requests**</span></span>  

## <a name="create-work-order"></a><span data-ttu-id="32876-107">إنشاء أمر العمل</span><span class="sxs-lookup"><span data-stu-id="32876-107">Create work order</span></span>

1. <span data-ttu-id="32876-108">انقر فوق **إدارة الأصول** > **عام** > **أوامر العمل** > **جميع أوامر العمل** أو **أوامر العمل النشطة**.</span><span class="sxs-lookup"><span data-stu-id="32876-108">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="32876-109">انقر فوق الزر **جديد**.</span><span class="sxs-lookup"><span data-stu-id="32876-109">Click the **New** button.</span></span>

3. <span data-ttu-id="32876-110">في القائمة المنسدلة **إنشاء أمر عمل**، حدد نوع أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="32876-110">In the **Create work order** drop-down, select a work order type.</span></span>

4. <span data-ttu-id="32876-111">حدد وصفًا، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="32876-111">If required, select a description.</span></span>

5. <span data-ttu-id="32876-112">حدد الأصل لأمر العمل بالإضافة إلى نوع مهمة الصيانة.</span><span class="sxs-lookup"><span data-stu-id="32876-112">Select the asset for the work order as well as a maintenance job type.</span></span>

>[!NOTE]
><span data-ttu-id="32876-113">عندما تحدد أصلاً، قد تتوفر ثلاث علامات تبويب: تتضمن علامة تبويب **الأصول الخاصة بي** أصولاً تتعلق بمواقع العمل التي قد يتم تعيينك لها (تم إعدادها في [عاملو الصيانة ومجموعات عاملي الصيانة‬](../setup-for-objects/workers-and-worker-groups.md)).</span><span class="sxs-lookup"><span data-stu-id="32876-113">When you select an asset, three tabs may be available: The **My assets** tab contains assets related to the functional locations to which you (the worker who is logged on the system) may be allocated (set up in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md)).</span></span> <span data-ttu-id="32876-114">إذا لم يتم إعداد أي مواقع عمل على عامل في [عاملو الصيانة ومجموعات عاملي الصيانة‬](../setup-for-objects/workers-and-worker-groups.md)، فلن تكون علامة التبويب **الأصول الخاصة بي** مرئية.</span><span class="sxs-lookup"><span data-stu-id="32876-114">If no functional locations are set up on a worker in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md), the **My assets** tab will not be visible.</span></span> <span data-ttu-id="32876-115">تحتوي علامة التبويب **الأصول النشطة** على قائمة بكافة الأصول التي فيها حالة دورة حياة الأصل بوضع "نشطة".</span><span class="sxs-lookup"><span data-stu-id="32876-115">The **Active assets** tab contains a list of all assets with asset lifecycle state "Active".</span></span> <span data-ttu-id="32876-116">تعرض علامة التبويب **طريقة عرض الأصول** طريقة عرض الشجرة لمواقع العمل والأصول المثبتة على تلك المواقع.</span><span class="sxs-lookup"><span data-stu-id="32876-116">The **Asset view** tab displays a tree view of functional locations and assets installed on those locations.</span></span>

6. <span data-ttu-id="32876-117">إذا لزم الأمر، حدد **متغير نوع مهمة الصيانة** و**المعاملات**.</span><span class="sxs-lookup"><span data-stu-id="32876-117">If required, select **Maintenance job type variant** and **Trade**.</span></span>

7. <span data-ttu-id="32876-118">إذا لزم الأمر، يمكنك تغيير مستوى خدمه أمر العمل‏‎ في حقل **مستوى الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="32876-118">If required, you can change the work order service level in the **Service level** field.</span></span>

8. <span data-ttu-id="32876-119">حدد تاريخي البدء والانتهاء المتوقعين في الحقول ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="32876-119">Select expected start and end dates in the related fields.</span></span>

9. <span data-ttu-id="32876-120">انقر فوق **موافق** لإنشاء أمر عمل جديد.</span><span class="sxs-lookup"><span data-stu-id="32876-120">Click **OK** to create a new work order.</span></span>

10. <span data-ttu-id="32876-121">قم بتحرير أمر العمل في **جميع أوامر العمل**، إذا كان ذلك مطلوبًا.</span><span class="sxs-lookup"><span data-stu-id="32876-121">Edit the work order in **All work orders**, if required.</span></span>

- <span data-ttu-id="32876-122">في **جميع أوامر العمل**، يمكنك إضافة العديد من الأصول إلى أمر عمل في طريقه عرض التفاصيل عن طريق إضافة بنود على علامة التبويب السريعة **مهام صيانة أمر العمل**.</span><span class="sxs-lookup"><span data-stu-id="32876-122">In **All work orders**, You can add several assets to a work order in Details view by adding lines on the **Work order maintenance jobs** FastTab.</span></span> <span data-ttu-id="32876-123">على الأصل، يمكنك تحديد فقط أنواع مهام الصيانة التي تم تحديدها على نوع الأصل المحدد للأصل.</span><span class="sxs-lookup"><span data-stu-id="32876-123">On an asset, you can only select the maintenance job types that are defined on the asset type selected for the asset.</span></span>  
- <span data-ttu-id="32876-124">إذا قمت بتغيير مستوى خدمة الأصل أو مستوى أهمية الأصل بعد استخدامه في أمر عمل (يمكنك مراجعة [مستويات خدمة الأصل](../setup-for-objects/object-priorities.md) و[مستويات أهمية الأصول‬](../setup-for-objects/object-criticalities.md))، لا يتم تحديث مستوى الخدمة أو مستوى الأهمية على أمر العمل وفقًا لذلك.</span><span class="sxs-lookup"><span data-stu-id="32876-124">If you have changed an asset service level or an asset criticality after you have used them on a work order (refer to [Asset service levels](../setup-for-objects/object-priorities.md) and [Asset criticalities](../setup-for-objects/object-criticalities.md)), the service level or criticality on the work order is not updated accordingly.</span></span>
- <span data-ttu-id="32876-125">يُعاد حساب مستوى الأهمية في أمر العمل في كل مرة تتم فيها إضافة بند أمر عمل إلى أمر العمل أو حذفه منه.</span><span class="sxs-lookup"><span data-stu-id="32876-125">Criticality on a work order is re-calculated each time a work order line is added or deleted on the work order.</span></span>
- <span data-ttu-id="32876-126">في **جميع أوامر العمل** طريقة عرض التفاصيل > طريقة عرض **الرأس** علامة التبويب السريع > **الجدول**، يمكنك تحديد مجموعة من عاملي الصيانة المسؤولية أو عامل صيانة مسؤول في الحقلين **مجموعة مسؤولة** أو **مسؤول**.</span><span class="sxs-lookup"><span data-stu-id="32876-126">In **All work orders** Details view > **Header** view > **Schedule** FastTab, you can select a responsible maintenance worker group or a responsible maintenance worker in the **Responsible group** or **Responsible** fields.</span></span> <span data-ttu-id="32876-127">يمكن تغيير هذه الإعدادات طالما كان أمر العمل نشطًا، على سبيل المثال، عندما تتغير حالة دورة حياة أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="32876-127">These settings can be changed as long as the work order is active, for example, when the work order lifecycle state changes.</span></span> <span data-ttu-id="32876-128">يستند التحديد التلقائي الذي تم اجراؤه أثناء إنشاء أمر العمل إلى الإعداد في **عاملو الصيانة المسؤولون**.</span><span class="sxs-lookup"><span data-stu-id="32876-128">The automatic selection made during work order creation is based on the setup in **Responsible maintenance workers**.</span></span> <span data-ttu-id="32876-129">إذا قمت بإضافة أو إزالة وظائف أمر العمل بعد إنشاء أمر العمل وكان الحقل **مجموعة مسؤولة** والحقل **مسؤول** فارغًا عندما تقوم بتحديث أمر العمل، تبحث إدارة الأصول عن التطابق محتمل في نموذج الإعداد لمجموعه من عاملي الصيانة المسؤولين أو عامل صيانة مسؤول.</span><span class="sxs-lookup"><span data-stu-id="32876-129">If you add or remove work order jobs after you have created a work order, and the **Responsible group** field and the **Responsible** field are blank when you update the work order, Asset Management searches for a possible match in the setup form for a responsible maintenance worker group or a responsible maintenance worker.</span></span> <span data-ttu-id="32876-130">إذا كان الحقل **مجموعة مسؤولة‬‏‫** أو **مسؤول** معبأ بشكل مسبق عند تحديث أمر العمل، لا يتم إجراء أي تغييرات.</span><span class="sxs-lookup"><span data-stu-id="32876-130">If the **Responsible group** field or the **Responsible** field is already filled out when you update the work order, no changes are made.</span></span> 

- <span data-ttu-id="32876-131">في **حالة الصيانة**، يمكنك إجراء عملية حسابية للحصول على نظرة عامة حول حمل العمل فيما يتعلق بأوامر العمل الواردة والمكتملة.</span><span class="sxs-lookup"><span data-stu-id="32876-131">In **Maintenance status**, you can make a calculation to get an overview of workload regarding incoming and completed work orders.</span></span>  

- <span data-ttu-id="32876-132">على علامة التبويب السريعة **تفاصيل البنود‬**، يمكنك استخدام الحقلين **خط الطول** و**خط العرض** لإضافة الإحداثيات الجغرافية للأصل المحدد في وظيفة أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="32876-132">On the **Line details** FastTab, use the **Latitude** and **Longitude** fields to add geographic coordinates for the asset selected on the work order job.</span></span>  

## <a name="create-related-work-order"></a><span data-ttu-id="32876-133">إنشاء أمر عمل ذي صلة</span><span class="sxs-lookup"><span data-stu-id="32876-133">Create related work order</span></span>

<span data-ttu-id="32876-134">يمكنك إنشاء أمر عمل مرتبط بأمر عمل موجود إذا كنت ترغب، على سبيل المثال، في العمل مع أوامر العمل الأساسية والثانوية.</span><span class="sxs-lookup"><span data-stu-id="32876-134">You can create a related work order to an existing work order if, for example, you want to work with primary and secondary work orders.</span></span> <span data-ttu-id="32876-135">يستند أمر العمل الجديد إلى وظيفة أمر عمل من أمر عمل موجود.</span><span class="sxs-lookup"><span data-stu-id="32876-135">A new work order is based on a work order job from an existing work order.</span></span>

1. <span data-ttu-id="32876-136">انقر فوق **إدارة الأصول** > **عام** > **أوامر العمل** > **جميع أوامر العمل** أو **أوامر العمل النشطة**.</span><span class="sxs-lookup"><span data-stu-id="32876-136">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="32876-137">حدد أمر العمل الذي تريد إنشاء أمر عمل مرتبط به.</span><span class="sxs-lookup"><span data-stu-id="32876-137">Select the work order for which you want to make a related work order.</span></span>

3. <span data-ttu-id="32876-138">انقر فوق **أمر العمل المرتبط**.</span><span class="sxs-lookup"><span data-stu-id="32876-138">Click **Related work order**.</span></span>

4. <span data-ttu-id="32876-139">في مربع القائمة المنسدلة **إنشاء أمر عمل مرتبط**، حدد وظيفة أمر العمل التي تريد إنشاء أمر العمل المرتبط بها في حقل **وظيفة أمر العمل**.</span><span class="sxs-lookup"><span data-stu-id="32876-139">In the **Create related work order** drop-down dialog, select the work order job for which you want to create a related work order in the **Work order job** field.</span></span>

5. <span data-ttu-id="32876-140">حدد نوع مهمة الصيانة في الحقل **نوع مهمة الصيانة**، وإذا كان مطلوبًا، متغير نوع مهمة الصيانة في الحقلين **نوع متغير وظيفة الصيانة** و**المعاملات**.</span><span class="sxs-lookup"><span data-stu-id="32876-140">Select a maintenance job type in the **Maintenance job type** field and, if required, a related maintenance job type variant and trade in the **Maintenance job type variant** and **Trade** fields.</span></span>

6. <span data-ttu-id="32876-141">إذا كان هذا هو أول أمر عمل مرتبط تقوم بإنشائه، فانقر فوق زر الخيار **أمر عمل جديد**.</span><span class="sxs-lookup"><span data-stu-id="32876-141">If this is the first related work order you make, click the **New work order** radio button.</span></span>

7. <span data-ttu-id="32876-142">حدد **نوع أمر عمل** و**وصفًا** في الحقول المرتبطة.</span><span class="sxs-lookup"><span data-stu-id="32876-142">Select a **Work order type** and a **Description** in the related fields.</span></span>

8. <span data-ttu-id="32876-143">إذا لزم الأمر، غيّر مستوى خدمه أمر العمل‏‎ في حقل **مستوى الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="32876-143">If required, change the work order service level in the **Service level** field.</span></span>

9. <span data-ttu-id="32876-144">أدخل تاريخي البدء والانتهاء المتوقعين في الحقول ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="32876-144">Insert expected start and end dates in the related fields.</span></span>

10. <span data-ttu-id="32876-145">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="32876-145">Click **OK**.</span></span> <span data-ttu-id="32876-146">يظهر أمر العمل المرتبط الجديد في القائمة **جميع أوامر العمل**.</span><span class="sxs-lookup"><span data-stu-id="32876-146">The new related work order is shown in the **All work orders** list.</span></span>

11. <span data-ttu-id="32876-147">إذا قمت بإنشاء أمر عمل مرتبط على أمر عمل لديه أوامر عمل مرتبطة، يمكنك إضافة وظيفة أمر العمل إلى أمر عمل مرتبط.</span><span class="sxs-lookup"><span data-stu-id="32876-147">If you create a related work order on a work order that already has related work orders, you can add the work order job to an already related work order.</span></span> <span data-ttu-id="32876-148">يمكنك القيام بذلك بالنقر فوق الزر **إضافة إلى أمر عمل مرتبط** في الخطوة 6.</span><span class="sxs-lookup"><span data-stu-id="32876-148">This is done by clicking the **Add to related work order** radio button in step 6.</span></span> <span data-ttu-id="32876-149">ثم تحدد أمر العمل المرتبط الذي ترغب في إضافة وظيفة أمر عمل جديدة اليه.</span><span class="sxs-lookup"><span data-stu-id="32876-149">Then you select the related work order to which you want to add a new work order job.</span></span> <span data-ttu-id="32876-150">قم بتحرير الحقول **مستوى الخدمة** و**البدء المتوقع‬** و**الانتهاء المتوقع‬**، كما هو مطلوب، وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="32876-150">Edit the **Service level**, **Expected start**, and **Expected end** fields, as required, and click **OK**.</span></span> <span data-ttu-id="32876-151">تًضاف وظيفة أمر العمل إلى أمر العمل المرتبط الموجود.</span><span class="sxs-lookup"><span data-stu-id="32876-151">The work order job is added to the existing related work order.</span></span>


![الشكل 1](media/03-work-orders.png)

<span data-ttu-id="32876-153">**ملاحظة:** إذا قمت بإعداد قناع أمر عمل مرتبط في **محددات إدارة الأصول‬** > الارتباط **أوامر العمل** الحقل > **قناع أمر العمل المرتبط**، سيتم إنشاء معرفات أوامر العمل وفقًا لإعداد القناع.</span><span class="sxs-lookup"><span data-stu-id="32876-153">**Note:** If you have set up a related work order mask in **Asset management parameters** > **Work orders** link > **Related work order mask** field, work order IDs will be created in accordance with the mask setup.</span></span> <span data-ttu-id="32876-154">إذا لم يتم إعداد قناع أمر عمل مرتبط، سيتم استخدام معرف أمر العمل التالي المتاح لأوامر العمل المرتبطة.</span><span class="sxs-lookup"><span data-stu-id="32876-154">If no related work order mask is set up, the next available work order ID will be used for related work orders.</span></span>

## <a name="copy-work-order"></a><span data-ttu-id="32876-155">نسخ أمر العمل</span><span class="sxs-lookup"><span data-stu-id="32876-155">Copy work order</span></span>

<span data-ttu-id="32876-156">من الممكن إنشاء أمر عمل جديد بسرعة من أمر عمل موجود.</span><span class="sxs-lookup"><span data-stu-id="32876-156">It is possible to quickly create a new work order from an existing work order.</span></span> <span data-ttu-id="32876-157">وتختلف طريقة التعامل هذه مع أوامر العمل عن إنشاء أوامر العمل بالاستناد إلى خطط الصيانة.</span><span class="sxs-lookup"><span data-stu-id="32876-157">This way of working with work orders is different from creating work orders based on maintenance plans.</span></span> <span data-ttu-id="32876-158">من المفيد، على سبيل المثال، وجود أمر عمل يحتوي على عدد كبير من وظائف أمر العمل مع وظائف مختلفة على أصول مختلفة يجب إكمالها في فترات زمنية منتظمة.</span><span class="sxs-lookup"><span data-stu-id="32876-158">It is useful if, for example, you have a work order containing many work order jobs with various jobs on different assets that should be completed at regular intervals.</span></span>

1. <span data-ttu-id="32876-159">انقر فوق **إدارة الأصول** > **عام** > **أوامر العمل** > **جميع أوامر العمل** أو **أوامر العمل النشطة**.</span><span class="sxs-lookup"><span data-stu-id="32876-159">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="32876-160">حدد أمر العمل الذي تريد نسخ المحتوى منه.</span><span class="sxs-lookup"><span data-stu-id="32876-160">Select the work order from which you want to copy content.</span></span>

3. <span data-ttu-id="32876-161">انقر فوق **نسخ أمر العمل**.</span><span class="sxs-lookup"><span data-stu-id="32876-161">Click **Copy work order**.</span></span> <span data-ttu-id="32876-162">يظهر إعداد أمر العمل من أمر العمل المحدد.</span><span class="sxs-lookup"><span data-stu-id="32876-162">The work order setup from the selected work order is shown.</span></span> <span data-ttu-id="32876-163">إذا لزم الأمر، يمكنك تحرير بعض الحقول.</span><span class="sxs-lookup"><span data-stu-id="32876-163">If required, you can edit some of the fields.</span></span>

4. <span data-ttu-id="32876-164">انقر فوق **موافق** لإنشاء أمر العمل الجديد.</span><span class="sxs-lookup"><span data-stu-id="32876-164">Click **OK** to create the new work order.</span></span>

5. <span data-ttu-id="32876-165">قم بتحرير أمر العمل في **جميع أوامر العمل**، إذا كان ذلك مطلوبًا.</span><span class="sxs-lookup"><span data-stu-id="32876-165">Edit the work order in **All work orders**, if required.</span></span>

>[!NOTE]
><span data-ttu-id="32876-166">عند إنشاء أمر العمل الجديد، يتم نسخ بعض المعلومات مباشرة من أمر العمل الموجود.</span><span class="sxs-lookup"><span data-stu-id="32876-166">When the new work order is created, some information is copied directly from the existing work order.</span></span> <span data-ttu-id="32876-167">لا يتم نسخ المعلومات المتعلقة بالتنبؤات والأدوات وقوائم فحص الصيانة وموقع العمل والعناوين والجدولة، ولكن تتم تهيئتها من الإعداد الحالي في إدارة الأصول.</span><span class="sxs-lookup"><span data-stu-id="32876-167">Information regarding forecasts, tools, maintenance checklists, functional location, addresses, and scheduling is not copied, but initialized from the current setup in Asset Management.</span></span> <span data-ttu-id="32876-168">وهذا يعني انه إذا تم إجراء تغييرات على هذه البيانات من وقت إنشاء أمر العمل الأول حتى وقت إنشاء نسخة من أمر العمل، يتم تضمين هذه التغييرات في أمر العمل الجديد الذي قمت بإنشائه.</span><span class="sxs-lookup"><span data-stu-id="32876-168">This means that if changes were made in those data from the time of creation of the first work order until the time you made a copy of the work order, those changes are included in the new work order you have created.</span></span> <span data-ttu-id="32876-169">من الأمثلة التغيرات في التنبؤات أو قوائم فحص الصيانة المحدثة.</span><span class="sxs-lookup"><span data-stu-id="32876-169">Examples are changes in forecasts or updated maintenance checklists.</span></span>


![الشكل 2](media/04-work-orders.png)


## <a name="create-work-order-based-on-a-maintenance-request"></a><span data-ttu-id="32876-171">إنشاء أمر عمل استنادً إلى طلب صيانة</span><span class="sxs-lookup"><span data-stu-id="32876-171">Create work order based on a maintenance request</span></span>

1. <span data-ttu-id="32876-172">انقر فوق **إدارة الأصول** > **عام‏‎** > **طلبات الصيانة** > **جميع طلبات الصيانة** أو **طلبات الصيانة النشطة**.</span><span class="sxs-lookup"><span data-stu-id="32876-172">Click **Asset management** > **Common** > **Maintenance requests** > **All maintenance requests** or **Active maintenance requests**.</span></span>

2. <span data-ttu-id="32876-173">حدد طلب الصيانة الذي ترغب في إنشاء أمر عمل له، ثم انقر فوق **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="32876-173">Select the maintenance request for which you want to create a work order, and click **Edit**.</span></span>

3. <span data-ttu-id="32876-174">في **جميع الطلبات**، انقر فوق **أمر العمل**.</span><span class="sxs-lookup"><span data-stu-id="32876-174">In **All requests**, click **Work order**.</span></span>

4. <span data-ttu-id="32876-175">قم بتعبئة القائمة المنسدلة **أمر العمل**.</span><span class="sxs-lookup"><span data-stu-id="32876-175">Fill out the **Work order** drop-down.</span></span> <span data-ttu-id="32876-176">إذا تم تحديد نوع مهمة صيانة في طلب الصيانة، يمكنك تحديد نوع مهمة صيانة أخرى، إذا كان ذلك مطلوبًا، عند إنشاء أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="32876-176">If a maintenance job type has been selected in the maintenance request, you are able to select another maintenance job type, if required, when you create the work order.</span></span>

5. <span data-ttu-id="32876-177">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="32876-177">Click **OK**.</span></span> <span data-ttu-id="32876-178">سترى رسالة تعلمك بإنشاء أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="32876-178">You will see a message informing you that the work order has been created.</span></span>

6. <span data-ttu-id="32876-179">إذا كنت ترغب في معرفة ما هي أوامر العمل المرتبطة بطلب صيانة، حدد طلب الصيانة في القائمتين **جميع طلبات الصيانة** أو **طلبات الصيانة النشطة**، وانقر فوق الزر **أوامر العمل**.</span><span class="sxs-lookup"><span data-stu-id="32876-179">If you want to see which work orders are connected to a maintenance request, select the maintenance request in the **All maintenance requests** or **Active maintenance requests** lists, and click the **Work orders** button.</span></span>


![الشكل 3](media/05-work-orders.png)


>[!NOTE]
><span data-ttu-id="32876-181">ويمكن أيضًا إنشاء أوامر العمل بشكل تلقائي عن طريق جدولة مهام خطط الصيانة أو إعداد "الإنشاء التلقائي" لخطط الصيانة أو دورات الصيانة على أحد الأصول.</span><span class="sxs-lookup"><span data-stu-id="32876-181">Work orders can also be created automatically by scheduling maintenance plan jobs, or by setting up "Auto create" maintenance plans or maintenance rounds on an asset.</span></span> <span data-ttu-id="32876-182">يتم إنشاء أوامر العمل المنشأة من طلبات الصيانة في **جدول‏‎ الصيانة** مع أنواع مهام الصيانة المحددة في طلبات الصيانة.</span><span class="sxs-lookup"><span data-stu-id="32876-182">Work orders created from maintenance requests in **Maintenance schedule** are created with the maintenance job types selected in the maintenance requests.</span></span>

