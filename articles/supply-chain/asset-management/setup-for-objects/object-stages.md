---
title: حالات دورة حياة الأصل
description: يشرح هذا الموضوع حالات دورة حياة الأصل ونماذج دورة الحياة في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetLifecycleModelStateNext, EntAssetObjectLifecycleState, EntAssetLifecycleStateUpdate, EntAssetObjectLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 566036c6361194d910a0fc34bd5d72147585ec4f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421274"
---
# <a name="asset-lifecycle-states"></a><span data-ttu-id="61fa1-103">حالات دورة حياة الأصل</span><span class="sxs-lookup"><span data-stu-id="61fa1-103">Asset lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="61fa1-104">يشرح هذا الموضوع حالات دورة حياة الأصل ونماذج دورة الحياة في إدارة الأصول.</span><span class="sxs-lookup"><span data-stu-id="61fa1-104">This topic explains asset lifecycle states and lifecycle models in Asset Management.</span></span> <span data-ttu-id="61fa1-105">يتم استخدام حالات دورة حياة الأصل لتحديد ما إذا كان الأصل نشطًا أو غير نشط.</span><span class="sxs-lookup"><span data-stu-id="61fa1-105">Asset lifecycle states are used to define whether an asset is active or inactive.</span></span> <span data-ttu-id="61fa1-106">على سبيل المثال، يمكنك إعداد حالات دورة حياة الأصل، مثل **تم الإنشاء** و **نشط** و **تم الإنهاء‬**.</span><span class="sxs-lookup"><span data-stu-id="61fa1-106">For example, you can set up asset lifecycle states such as **Created**, **Active**, and **Terminated**.</span></span>

> [!NOTE]
> - <span data-ttu-id="61fa1-107">ترتبط حالات دورة حياة الطلب بحالات دورة حياة الأصل.</span><span class="sxs-lookup"><span data-stu-id="61fa1-107">Request lifecycle states are linked to asset lifecycle states.</span></span> <span data-ttu-id="61fa1-108">لذلك، عند تغيير طلب إلى حالة دورة حياة طلب جديدة، يتم تغيير الأصل المرفق بالطلب إلى حالة دورة حياة الأصل الجديدة.</span><span class="sxs-lookup"><span data-stu-id="61fa1-108">Therefore, when a request is changed to a new request lifecycle state, the asset that is attached to the request is changed to a new asset lifecycle state.</span></span> <span data-ttu-id="61fa1-109">على سبيل المثال، إذا تغيرت حالة دورة حياة طلب إلى **وارد**، فإن حالة دورة حياة الأصل المرفق ستتغير إلى حالة دورة الحياة المحددة في حقل **حالة دورة الحياة الواردة** على علامة التبويب السريعة **حالة دورة حياة الأصل** في صفحة **نماذج حالة دورة حياة الأصل**.</span><span class="sxs-lookup"><span data-stu-id="61fa1-109">For example, if the lifecycle state of a request is changed to **Inbound**, the lifecycle state of the attached asset is changed to the lifecycle state that is selected in the **Inbound lifecycle state** field on the **Asset lifecycle state** FastTab of the **Asset lifecycle state models** page.</span></span> 


<span data-ttu-id="61fa1-110">يمكن إعداد حالات دورة حياة الأصل في نماذج دورة حياة الأصل، حيث يمكنك تحديد حالات دورة الحياة المطلوبة لأنواع مختلفة من الأصول.</span><span class="sxs-lookup"><span data-stu-id="61fa1-110">Asset lifecycle states can be set up in asset lifecycle models, where you can define the required lifecycle states for various types of assets.</span></span> <span data-ttu-id="61fa1-111">ستقوم أولاً بإعداد حالات دورة الحياة.</span><span class="sxs-lookup"><span data-stu-id="61fa1-111">You first set up lifecycle states.</span></span> <span data-ttu-id="61fa1-112">بعد ذلك، يمكنك إنشاء نموذج دورة حياة وتحديد حالات دورة الحياة له.</span><span class="sxs-lookup"><span data-stu-id="61fa1-112">You then create a lifecycle model and select lifecycle states for it.</span></span>

1. <span data-ttu-id="61fa1-113">حدد **إدارة الأصول** \> **الإعداد** \> **الأصول** \> **حالات دورة الحياة**.</span><span class="sxs-lookup"><span data-stu-id="61fa1-113">Select **Asset management** \> **Setup** \> **Assets** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="61fa1-114">حدد **جديد** لإنشاء حالة دورة حياة أصل جديدة.</span><span class="sxs-lookup"><span data-stu-id="61fa1-114">Select **New** to create a new asset lifecycle state.</span></span>
3. <span data-ttu-id="61fa1-115">في الحقل **حالة دورة الحياة**، أدخل معرفًا لحالة دورة الحياة.</span><span class="sxs-lookup"><span data-stu-id="61fa1-115">In the **Lifecycle state** field, enter the lifecycle state ID.</span></span>
4. <span data-ttu-id="61fa1-116">في حقل **الاسم**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="61fa1-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="61fa1-117">يعرض حقل **نماذج دورة الحياة** عدد نماذج دورة حياة الأصل التي تستخدم حالة دورة الحياة هذه.</span><span class="sxs-lookup"><span data-stu-id="61fa1-117">The **Lifecycle models** field shows the number of asset lifecycle models that use the asset lifecycle state.</span></span>

5. <span data-ttu-id="61fa1-118">عيّن الخيار **نشط** إلى **نعم** إذا كان يجب أن تكون حالة دورة الحياة هذه حالة دورة حياة نشطة (بمعنى آخر، إذا كان يمكن إنشاء أوامر عمل للأصول الموجودة في حالة دورة الحياة هذه).</span><span class="sxs-lookup"><span data-stu-id="61fa1-118">Set the **Active** option to **Yes** if this lifecycle state should be an active lifecycle state (in other words, if work orders can be created for assets that are in this lifecycle state).</span></span>
6. <span data-ttu-id="61fa1-119">عيّن الخيار **حذف بنود التقويم المفتوحة** إلى **نعم** إذا كان يجب حذف بنود تقويم الأصل المفتوحة التي لديها حالة دورة الحياة **تم الإنشاء** عندما تكون في حالة دورة الحياة هذه.</span><span class="sxs-lookup"><span data-stu-id="61fa1-119">Set the **Delete open calendar lines** option to **Yes** if open asset calendar lines that have an asset lifecycle state of **Created** should be deleted when they are in this lifecycle state.</span></span> <span data-ttu-id="61fa1-120">يكون هذا الإعداد مفيدًا إذا كنت ترغب في تنظيف أية جداول صيانة مفتوحة لم تعد ذات صلة بالأصل (على سبيل المثال، إذا لم يعد الأصل نشطًا).</span><span class="sxs-lookup"><span data-stu-id="61fa1-120">This setting is useful if you want to clean up any open maintenance schedules that are no longer relevant for the asset (for example, if the asset is no longer active).</span></span>

> [!NOTE]
> <span data-ttu-id="61fa1-121">ترتبط حالات دورة حياة الأصل ونماذج دورة حياة الأصل وأنواع الأصول ببعضها.</span><span class="sxs-lookup"><span data-stu-id="61fa1-121">Asset lifecycle states, asset lifecycle models, and asset types are related.</span></span> <span data-ttu-id="61fa1-122">ويتم استخدامها بنفس الطريقة التي تستخدم بها حالات دورة حياة أمر العمل ونماذج دورة حياة أمر العمل وأنواع أوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="61fa1-122">They are used in the same way as work order lifecycle states, work order lifecycle models, and work order types.</span></span> 


<span data-ttu-id="61fa1-123">بعد إنشاء حالات دورة حياة الأصل المطلوبة، يمكنك إعداد حالات دورة الحياة في نماذج دورة حياة الأصل.</span><span class="sxs-lookup"><span data-stu-id="61fa1-123">After you've created the required asset lifecycle states, you can set up lifecycle states in asset lifecycle models.</span></span>

1. <span data-ttu-id="61fa1-124">حدد **إدارة الأصول** \> **الإعداد** \> **الأصول** \> **نماذج دورة الحياة**.</span><span class="sxs-lookup"><span data-stu-id="61fa1-124">Select **Asset management** \> **Setup** \> **assets** \> **lifecycle models**.</span></span>
2. <span data-ttu-id="61fa1-125">حدد **جديد** لإنشاء حالة نموذج دورة حياة أصل جديد.</span><span class="sxs-lookup"><span data-stu-id="61fa1-125">Select **New** to create a new asset lifecycle model.</span></span>
3. <span data-ttu-id="61fa1-126">في الحقل **نموذج دورة الحياة**، أدخل معرفًا لنموذج دورة الحياة.</span><span class="sxs-lookup"><span data-stu-id="61fa1-126">In the **Lifecycle model** field, enter the lifecycle model ID.</span></span>
4. <span data-ttu-id="61fa1-127">في حقل **الاسم**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="61fa1-127">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="61fa1-128">يعرض الحقل **حالات دورة الحياة** عدد حالات دورة الحياة المحددة في نموذج دورة الحياة.</span><span class="sxs-lookup"><span data-stu-id="61fa1-128">The **Lifecycle states** field shows the number of asset lifecycle states that are selected in the asset lifecycle model.</span></span> <span data-ttu-id="61fa1-129">يعرض حقل **أنواع الأصول** أنواع الأصول التي تستخدم نموذج دورة الحياة.</span><span class="sxs-lookup"><span data-stu-id="61fa1-129">The **Asset types** field shows the number of asset types that use the lifecycle model.</span></span>

5. <span data-ttu-id="61fa1-130">على علامة التبويب السريعة **حالات دورة الحياة**، حدد حالات دورة الحياة التي يجب تضمينها في نموذج دورة حياة الأصل:</span><span class="sxs-lookup"><span data-stu-id="61fa1-130">On the **Lifecycle states** FastTab, select the asset lifecycle states that should be included in the asset lifecycle model:</span></span>

    - <span data-ttu-id="61fa1-131">لاستخدام حالة دورة حياة للنموذج، حددها في القسم **حالات دورة الحياة المتبقية**، ثم حدد زر السهم إلى اليمين ![سهم إلى اليمين](media/15-setup-for-objects.png) لنقلها إلى القسم **حالات دورة الحياة المحددة**.</span><span class="sxs-lookup"><span data-stu-id="61fa1-131">To use a lifecycle state for the model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/15-setup-for-objects.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="61fa1-132">لاستخدام جميع حالات دورة الحياة المتوفرة للنموذج، حدد الزر **جميع حالات دورة الحياة المتوفرة** ![جميع حالات دورة الحياة المتوفرة](media/20-setup-for-objects.png).</span><span class="sxs-lookup"><span data-stu-id="61fa1-132">To use all the available lifecycle states for the model, select the **All available lifecycle states** button ![All available lifecycle states](media/20-setup-for-objects.png).</span></span> <span data-ttu-id="61fa1-133">يتم نقل جميع حالات دورة الحياة إلى القسم **حالات دورة الحياة المحددة**.</span><span class="sxs-lookup"><span data-stu-id="61fa1-133">All lifecycle states are transferred to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="61fa1-134">لإزالة حالة دورة حياة من النموذج، حددها في القسم **حالات دورة الحياة المحددة**، ثم حدد زر السهم إلى اليسار ![سهم إلى اليسار](media/16-setup-for-objects.png) لنقلها إلى القسم **حالات دورة الحياة المتبقية**.</span><span class="sxs-lookup"><span data-stu-id="61fa1-134">To remove a lifecycle state from the model, select it in the **lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/16-setup-for-objects.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="61fa1-135">حدد **تحديثات حالة دورة الحياة** لتحديد حالات دورة حياة الأصل التي يمكنها أن تتبع حالة دورة حياة محددة.</span><span class="sxs-lookup"><span data-stu-id="61fa1-135">Select **Lifecycle state updates** to define the asset lifecycle states that can follow a selected lifecycle state.</span></span>
7. <span data-ttu-id="61fa1-136">يمكنك استخدام علامة التبويب السريعة **حالة الأصل** إذا كنت تتعامل مع أصول تستلمها لإصلاحها.</span><span class="sxs-lookup"><span data-stu-id="61fa1-136">You use the **Asset state** FastTab if you handle assets that you receive for repair.</span></span> <span data-ttu-id="61fa1-137">في القسم **وارد/صادر**، يمكنك تحديد حالات دورة حياة الأصل للإشارة إلى سير عمل أصل تستلمه لإصلاحه.</span><span class="sxs-lookup"><span data-stu-id="61fa1-137">In the **Inbound/outbound** section, you can select asset lifecycle states to indicate the workflow of an asset that you receive for repair.</span></span> <span data-ttu-id="61fa1-138">إذا قدمت أصولاً مقترضة للعملاء أو الأقسام في قسم **القرض**، يمكنك تحديد حالات دورة الحياة للأصول المقترضة.</span><span class="sxs-lookup"><span data-stu-id="61fa1-138">If you offer loan assets to customers or departments, in the **Loan** section, you can select lifecycle states for loan assets.</span></span>
