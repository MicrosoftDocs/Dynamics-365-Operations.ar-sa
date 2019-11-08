---
title: حالات دورة حياة طلب الصيانة
description: يصف هذا الموضوع كيفية إعداد حالات دورة حياة طلب الصيانة في إدارة الأصول.
author: josaw1
manager: AnnBe
ms.date: 07/26/2019
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
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 151db9ca8a121759e39b690ec296b36a18dc1729
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571152"
---
# <a name="maintenance-request-lifecycle-states"></a><span data-ttu-id="817eb-103">حالات دورة حياة طلبات الصيانة</span><span class="sxs-lookup"><span data-stu-id="817eb-103">Maintenance request lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="817eb-104">تحدد حالات دورة حياة طلب الصيانة المراحل التي يمكن أن يمر بها الطلب.</span><span class="sxs-lookup"><span data-stu-id="817eb-104">Maintenance request lifecycle states define the stages that a request can go through.</span></span> <span data-ttu-id="817eb-105">تتضمن الأمثلة **تم إنشاؤه‬** و**نشط** و**منتهٍ‬**.</span><span class="sxs-lookup"><span data-stu-id="817eb-105">Examples include **Created**, **Active**, and **Ended**.</span></span> <span data-ttu-id="817eb-106">عند تحويل طلب صيانة إلى أمر عمل، يجب تحديث حالة دورة حياة طلب الصيانة إلى **منتهٍ** أو **مُغلق** للإشارة إلى أن طلب الصيانة لم يعد نشطًا.</span><span class="sxs-lookup"><span data-stu-id="817eb-106">When a maintenance request is converted to a work order, the maintenance request lifecycle state should be updated to **Ended** or **Closed** to indicate that the maintenance request is no longer active.</span></span> <span data-ttu-id="817eb-107">في صفحة القائمة **جميع طلبات الصيانة**، يمكنك عرض جميع طلبات الصيانة، بغض النظر عن حالة دورة حياتها.</span><span class="sxs-lookup"><span data-stu-id="817eb-107">On the **All maintenance requests** list page, you can view all maintenance requests, regardless of their lifecycle state.</span></span>

## <a name="set-up-maintenance-request-lifecycle-states"></a><span data-ttu-id="817eb-108">إعداد حالات دورة حياة طلب الصيانة</span><span class="sxs-lookup"><span data-stu-id="817eb-108">Set up maintenance request lifecycle states</span></span>

1. <span data-ttu-id="817eb-109">حدد **إدارة الأصول** \> **الإعداد** \> **طلبات الصيانة** \> **حالات دورة الحياة**.</span><span class="sxs-lookup"><span data-stu-id="817eb-109">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="817eb-110">حدد **جديد** لإنشاء حالة دورة حياة طلب صيانة.</span><span class="sxs-lookup"><span data-stu-id="817eb-110">Select **New** to create a maintenance request lifecycle state.</span></span>
3. <span data-ttu-id="817eb-111">في الحقل **حالة دورة الحياة**، أدخل معرفًا لحالة دورة الحياة.</span><span class="sxs-lookup"><span data-stu-id="817eb-111">In the **Lifecycle state** field, enter an ID for the lifecycle state.</span></span>
4. <span data-ttu-id="817eb-112">في حقل **الاسم**، أدخل اسمًا.</span><span class="sxs-lookup"><span data-stu-id="817eb-112">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="817eb-113">على علامة التبويب السريعة **التفاصيل**، يعرض حقل **نماذج دورة الحياة** عدد نماذج دورة حياة طلبات الصيانة التي تستخدم حالة دورة الحياة هذه.</span><span class="sxs-lookup"><span data-stu-id="817eb-113">On the **Details** FastTab, the **Lifecycle models** field shows the number of maintenance request lifecycle models that use this lifecycle state.</span></span>

5. <span data-ttu-id="817eb-114">على علامة التبويب السريعة **عام**، عيّن الخيار **نشط** إلى **نعم** إذا كان من الضروري أن يكون أحد طلبات الصيانة نشطًا أثناء وجوده في حالة دورة الحياة هذه.</span><span class="sxs-lookup"><span data-stu-id="817eb-114">On the **General** FastTab, set the **Active** option to **Yes** if a maintenance request should be active while it's in this lifecycle state.</span></span>
6. <span data-ttu-id="817eb-115">عيّن الخيار **تعيين الانتهاء الفعلي** إلى **نعم** إذا كان يجب إدخال تاريخ ووقت الانتهاء الفعليين على طلب صيانة في حالة دورة الحياة هذه.</span><span class="sxs-lookup"><span data-stu-id="817eb-115">Set he **Set actual end** option to **Yes** if an actual end date and time should automatically be entered on a maintenance request that is in this lifecycle state.</span></span>
7. <span data-ttu-id="817eb-116">عيّن الخيار **إنشاء أمر عمل** إلى **نعم** إذا كان يمكن إنشاء أمر عمل من طلب صيانة في حالة دورة الحياة هذه.</span><span class="sxs-lookup"><span data-stu-id="817eb-116">Set the **Create work order** option to **Yes** if a work order can be created from a maintenance request that is in this lifecycle state.</span></span>
8. <span data-ttu-id="817eb-117">عيّن الخيار **حذف** إلى **نعم** إذا كان يمكن حذف طلب صيانة أثناء وجوده في حالة دورة الحياة هذه.</span><span class="sxs-lookup"><span data-stu-id="817eb-117">Set the **Delete** option to **Yes** if a maintenance request can be deleted while it's in this lifecycle state.</span></span>
9. <span data-ttu-id="817eb-118">على علامة التبويب السريعة **تحديث**، تكون الخيارات **وارد‬** و**صادر** في قسم **الأصل** ذات صلة عند استخدام إصلاح المستودع. عيّن الخيار الملائم إلى **نعم** إذا كانت يجب تحديث حالة دورة حياة الأصول المحددة على طلب صيانة بشكل تلقائي إلى **وارد‬** أو **صادر‏‎** عند تعيين حالة دورة حياة طلب الصيانة لطلب صيانة هذا إلى **وارد** أو **صادر‏‎**.</span><span class="sxs-lookup"><span data-stu-id="817eb-118">On the **Update** FastTab, the **Inbound** and **Outbound** options in the **Asset** section are relevant if you use depot repair.cSet the appropriate option to **Yes** if the asset lifecycle state of assets that are selected on a maintenance request should automatically be updated to **Inbound** or **Outbound** when the maintenance request lifecycle state of that maintenance request is set to **Inbound** or **Outbound**.</span></span>

<span data-ttu-id="817eb-119">يبين الرسم التوضيحي التالي مثالاً لصفحة **حالات دورة حياة طلب الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="817eb-119">The follow illustration shows an example of the **Maintenance request lifecycle states** page.</span></span>

![صفحة حالات دورة حياة طلبات الصيانة](media/02-setup-for-requests.png)

> [!NOTE]
> <span data-ttu-id="817eb-121">ترتبط حالات دورة حياة طلب الصيانة وأنواع ومجموعات حالات دورة الحياة ببعضها، ويتم استخدامها بالطريقة نفسها كحالات دورة حياة أمر عمل وأنواع ومجموعات حالات دورة الحياة.</span><span class="sxs-lookup"><span data-stu-id="817eb-121">Maintenance request lifecycle states, lifecycle state groups, and types are related to, and used in the same way as, work order lifecycle states, lifecycle state groups, and types.</span></span> 

## <a name="set-up-maintenance-request-lifecycle-models"></a><span data-ttu-id="817eb-122">إعداد نماذج دورة حياة طلب الصيانة</span><span class="sxs-lookup"><span data-stu-id="817eb-122">Set up maintenance request lifecycle models</span></span>

<span data-ttu-id="817eb-123">بعد إنشاء حالات دورة الحياة المطلوبة لطلبات الصيانة، يمكن تقسيمها إلى مجموعات حالات دورة حياة أو نماذج دورة حياة.</span><span class="sxs-lookup"><span data-stu-id="817eb-123">After you've created the lifecycle states that are required for your maintenance requests, they can be divided into lifecycle state groups, or lifecycle models.</span></span> <span data-ttu-id="817eb-124">يتم استخدام نماذج دورة حياة طلب الصيانة لإنشاء سير المهام الذي يمكن استخدامه لأنواع مختلفة من طلبات الصيانة.</span><span class="sxs-lookup"><span data-stu-id="817eb-124">Maintenance request lifecycle models are used to create the flow that can be used for different types of maintenance requests.</span></span> <span data-ttu-id="817eb-125">كحد أدنى، يجب إنشاء نموذج دورة حياة طلب صيانة قياسي واحد.</span><span class="sxs-lookup"><span data-stu-id="817eb-125">At a minimum, one standard maintenance request lifecycle model should be created.</span></span>

1. <span data-ttu-id="817eb-126">حدد **إدارة الأصول** \> **الإعداد** \> **طلبات الصيانة** \> **نماذج دورة الحياة**.</span><span class="sxs-lookup"><span data-stu-id="817eb-126">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle models**.</span></span>
2. <span data-ttu-id="817eb-127">حدد **جديد** لإنشاء حالة نموذج دورة حياة طلب صيانة.</span><span class="sxs-lookup"><span data-stu-id="817eb-127">Select **New** to create a maintenance request lifecycle model.</span></span>
3. <span data-ttu-id="817eb-128">في الحقل **نموذج دورة الحياة**، أدخل معرفًا لنموذج دورة الحياة.</span><span class="sxs-lookup"><span data-stu-id="817eb-128">In the **Lifecycle model** field, enter an ID for the lifecycle model.</span></span>
4. <span data-ttu-id="817eb-129">في حقل **الاسم**، أدخل اسمًا.</span><span class="sxs-lookup"><span data-stu-id="817eb-129">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="817eb-130">على علامة التبويب السريعة **التفاصيل**، يعرض حقل **حالات دورة الحياة** عدد حالات دورة الحياة المحددة في نموذج دورة الحياة هذا.</span><span class="sxs-lookup"><span data-stu-id="817eb-130">On the **Details** FastTab, the **Lifecycle states** shows the number of lifecycle states that are selected in this lifecycle model.</span></span> <span data-ttu-id="817eb-131">يعرض الحقل **أنواع طلبات الصيانة**عدد أنواع طلبات الصيانة التي تستخدم نموذج دورة الحياة هذا.</span><span class="sxs-lookup"><span data-stu-id="817eb-131">The **Maintenance request types** field shows the number of maintenance request types that use this lifecycle model.</span></span>

5. <span data-ttu-id="817eb-132">على علامة التبويب السريعة **حالات دورة الحياة**، حدد حالات دورة الحياة التي يجب تضمينها في نموذج دورة الحياة:</span><span class="sxs-lookup"><span data-stu-id="817eb-132">On the **Lifecycle states** FastTab, select the lifecycle states that should be included in the lifecycle model:</span></span>

    - <span data-ttu-id="817eb-133">لتضمين حالة دورة حياة في نموذج دورة الحياة، حددها في القسم **حالات دورة الحياة المتبقية**، ثم حدد زر السهم إلى اليمين ![سهم إلى اليمين](media/03-setup-for-requests.png) لنقلها إلى القسم **حالات دورة الحياة المحددة**.</span><span class="sxs-lookup"><span data-stu-id="817eb-133">To include a lifecycle state in the lifecycle model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/03-setup-for-requests.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="817eb-134">لتضمين جميع حالات دورة الحياة المتوفرة في نموذج دورة الحياة، حدد الزر **تحديد جميع الحالات المتوفرة** ![تحديد جميع الحالات المتوفرة](media/04-setup-for-requests.png).</span><span class="sxs-lookup"><span data-stu-id="817eb-134">To include all the available lifecycle states in the lifecycle model, select the **Select all available states** button ![Select all available states](media/04-setup-for-requests.png).</span></span> <span data-ttu-id="817eb-135">يتم نقل جميع حالات دورة الحياة إلى القسم **حالات دورة الحياة المحددة**.</span><span class="sxs-lookup"><span data-stu-id="817eb-135">All lifecycle states are moved to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="817eb-136">لإزالة حالة دورة حياة من نموذج دورة الحياة، حددها في القسم **حالات دورة الحياة المحددة**، ثم حدد زر السهم إلى اليسار ![سهم إلى اليسار](media/05-setup-for-requests.png) لنقلها إلى القسم **حالات دورة الحياة المتبقية**.</span><span class="sxs-lookup"><span data-stu-id="817eb-136">To remove a lifecycle state from the lifecycle model, select it in the **Lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/05-setup-for-requests.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="817eb-137">على علامة التبويب السريعة **عام**، تعتبر الحقول في قسم **التحديثات** ذات صلة إذا استخدمت إصلاح المستودع,</span><span class="sxs-lookup"><span data-stu-id="817eb-137">On the **General** FastTab, the fields in the **Updates** section are relevant if you use depot repair.</span></span>

    - <span data-ttu-id="817eb-138">في الحقل **حالة دورة حياة الأصل المستلم**، حدد حالة دورة حياة الأصل الذي يجب أن تُحدّث إليه بشكل تلقائي الأصول المحددة على طلب صيانة عند استلامها لإصلاح المستودع.</span><span class="sxs-lookup"><span data-stu-id="817eb-138">In the **Lifecycle state for asset received** field, select the asset lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are received for depot repair.</span></span>
    - <span data-ttu-id="817eb-139">في الحقل **حالة دورة حياة الأصل المسلَّم**، حدد حالة دورة حياة الأصل الذي يجب أن تُحدّث إليه بشكل تلقائي الأصول المحددة على طلب صيانة عند إرجاعها بعد الإصلاح.</span><span class="sxs-lookup"><span data-stu-id="817eb-139">In the **Lifecycle state for asset delivered** field, select the lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are returned after repair.</span></span>

<span data-ttu-id="817eb-140">يبين الرسم التوضيحي التالي مثالاً لصفحة **نماذج دورة حياة طلب الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="817eb-140">The following illustration shows an example of the **Maintenance request lifecycle models** page.</span></span>

![صفحة نماذج دورة حياة طلب الصيانة](media/06-setup-for-requests.png)
