---
title: التأكيد التلقائي مع تحسين التخطيط
description: يشرح هذا الموضوع كيفيه استخدام التاكيد التلقائي مع تحسين التخطيط.
author: ChristianRytt
manager: tfehr
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-30
ms.dyn365.ops.version: AX 10.0.7
ms.openlocfilehash: e412ccbc7c44d41e0a70ef8b5436901e01c671e6
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383678"
---
# <a name="auto-firming-with-planning-optimization"></a><span data-ttu-id="6765d-103">التأكيد التلقائي مع تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="6765d-103">Auto-firming with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6765d-104">يتيح لك التاكيد التلقائي تاكيد (اي ، إصدار) الأوامر المخططة كجزء من عمليه التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="6765d-104">Automatic firming lets you firm (that is, release) planned orders as part of the master planning process.</span></span> <span data-ttu-id="6765d-105">عند تاكيد الأوامر المخططة ، يتم تحويلها إلى أوامر شراء فعليه أو أوامر تحويل أو أوامر إنتاج.</span><span class="sxs-lookup"><span data-stu-id="6765d-105">When planned orders are firmed, they are transformed into actual purchase orders, transfer orders, or production orders.</span></span> <span data-ttu-id="6765d-106">عند استخدام تحسين التخطيط ، يتم تاكيد الأوامر المخططة اثناء تشغيل التخطيط الرئيسي عندما يكون تاريخ الأمر (اي تاريخ البدء) خلال فتره الحد الزمني للتاكيد.</span><span class="sxs-lookup"><span data-stu-id="6765d-106">When Planning Optimization is used, planned orders are firmed during a master planning run when the order date (that is, the start date) is within the time fence for firming.</span></span>

> [!NOTE]
> <span data-ttu-id="6765d-107">ويمكن أن يحدث التأكيد التلقائي لأمر الشراء المخطط فقط إذا كان الصنف مقترنًا بمورِّد.</span><span class="sxs-lookup"><span data-stu-id="6765d-107">Auto-firming of a planned purchase order can occur only if the item is associated with a vendor.</span></span>

## <a name="turn-on-auto-firming"></a><span data-ttu-id="6765d-108">تشغيل التاكيد التلقائي</span><span class="sxs-lookup"><span data-stu-id="6765d-108">Turn on auto-firming</span></span>

<span data-ttu-id="6765d-109">لتشغيل التأكيد التلقائي‬، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="6765d-109">To turn on auto-firming, follow these steps.</span></span>

1. <span data-ttu-id="6765d-110">في مساحة عمل **إدارة الميزات**، في علامة التبويب **جديد**، حدد **التأكيد التلقائي لتحسين التخطيط** في القائمة.</span><span class="sxs-lookup"><span data-stu-id="6765d-110">In the **Feature management** workspace, on the **New** tab, select **Auto-firming for Planning Optimization** in the list.</span></span> <span data-ttu-id="6765d-111">إذا لم تظهر الميزة على علامة التبويب **جديد**، فانظر إلى علامتي التبويب **غير ممكن** و**الكل**.</span><span class="sxs-lookup"><span data-stu-id="6765d-111">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="6765d-112">حدد **تمكين الآن**.</span><span class="sxs-lookup"><span data-stu-id="6765d-112">Select **Enable now**.</span></span> <span data-ttu-id="6765d-113">بدلاً من ذلك، حدد **جدولة**، ثم حدد الوقت الذي تريد فيه تشغيل الميزة.</span><span class="sxs-lookup"><span data-stu-id="6765d-113">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

## <a name="set-up-the-firming-time-fence"></a><span data-ttu-id="6765d-114">إعداد الحد الزمني للتأكيد</span><span class="sxs-lookup"><span data-stu-id="6765d-114">Set up the firming time fence</span></span>

<span data-ttu-id="6765d-115">يتم حساب الحد الزمني للتأكيد بداية من تاريخ تشغيل التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="6765d-115">The firming time fence is calculated forward from the master planning run date.</span></span> <span data-ttu-id="6765d-116">يتم تحديده بعدد أيام السماح الذي تقوم بإدخاله.</span><span class="sxs-lookup"><span data-stu-id="6765d-116">It's defined by the number of days that you enter.</span></span> <span data-ttu-id="6765d-117">يمكنك التحكم في الحد الزمني للتاكيد بالطرق التالية:</span><span class="sxs-lookup"><span data-stu-id="6765d-117">You can control the firming time fence in the following ways:</span></span>

- <span data-ttu-id="6765d-118">لتحديد الحد الافتراضي لوقت التأكيد لأحدي مجموعات التغطية، انتقل إلى **التخطيط الرئيسي** \> **الإعداد** \> **التغطية** \> **مجموعات التغطية**، وحدد مجموعة تغطية.</span><span class="sxs-lookup"><span data-stu-id="6765d-118">To define the default firming time fence for a coverage group, go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage groups**, and select a coverage group.</span></span> <span data-ttu-id="6765d-119">ثم من علامة التبويب السريعة **آخر**، في حقل **الحد الزمني للتأكيد التلقائي (الأيام)**، أدخل عدد الأيام.</span><span class="sxs-lookup"><span data-stu-id="6765d-119">Then, on the **Other** FastTab, in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="6765d-120">للكتابة فوق الحد الزمني للتأكيد المحدد لمجموعة التغطية الخاصة بصنف معين، انتقل إلى **إدارة معلومات المنتج** \> **المنتجات الصادرة**، ثم من جزء الإجراء، حدد **خطة**، ثم حدد **تغطية العنصر**.</span><span class="sxs-lookup"><span data-stu-id="6765d-120">To overwrite the firming time fence that is defined for the coverage group for a specific item, go to **Product information management** \> **Released products**, then from the Action Pane select **Plan** and then select **Item coverage**.</span></span> <span data-ttu-id="6765d-121">ثم، في علامة التبويب **عام**، حدد **تجاوز الحد الزمني** وفي حقل **الحد الزمني للتأكيد التلقائي (الأيام)**، أدخل عدد الأيام.</span><span class="sxs-lookup"><span data-stu-id="6765d-121">Then, on the **General** tab, select **Override time fence** and in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="6765d-122">للكتابة فوق الحد الزمني للتأكيد المحدد لمجموعة التغطية وتغطيه الصنف لخطة رئيسيه معينه، انتقل إلى **التخطيط الرئيسي** \> **إعداد** \>**الخطط الرئيسية**، وحدد خطة رئيسيه.</span><span class="sxs-lookup"><span data-stu-id="6765d-122">To overwrite the firming time fence that is defined for the coverage group and item coverage for a specific master plan, go to **Master planning** \> **Setup** \> **Master plans**, and select a Master plan.</span></span> <span data-ttu-id="6765d-123">ثم في علامة التبويب السريعة **الحد الزمني بالأيام**، قم بتعيين **تجميد** إلى **نعم**، وأدخل عدد الأيام.</span><span class="sxs-lookup"><span data-stu-id="6765d-123">Then, on the **Time fence in days** FastTab, set **Freeze** to **Yes**, and enter the number of days.</span></span>

<span data-ttu-id="6765d-124">في حالة تشغيل التاكيد التلقائي لتشغيل التخطيط الرئيسي الذي يستخدم تحسين التخطيط ، تتم عمليه التاكيد التلقائي وفقا لإعداد التاكيد التلقائي.</span><span class="sxs-lookup"><span data-stu-id="6765d-124">If auto-firming is turned on for a master planning run that uses Planning Optimization, the auto-firming process is done according to the auto-firming setup.</span></span> <span data-ttu-id="6765d-125">في حالة عدم تشغيل التاكيد التلقائي، أو في حالة بدء التخطيط من صفحة **صافي المتطلبات**، يتم تخطي عمليه التأكيد التلقائي.</span><span class="sxs-lookup"><span data-stu-id="6765d-125">If auto-firming isn't turned on, or if planning is started from the **Net requirements** page, the auto-firming process is skipped.</span></span>

## <a name="planning-optimization-vs-the-built-in-supply-chain-management-planning-engine"></a><span data-ttu-id="6765d-126">تحسين التخطيط مقابل محرك تخطيط Supply Chain Management المضمن</span><span class="sxs-lookup"><span data-stu-id="6765d-126">Planning Optimization vs. the built-in Supply Chain Management planning engine</span></span>

<span data-ttu-id="6765d-127">يمكن استخدام كل من تحسين التخطيط ومحرك التخطيط المضمن في Microsoft Dynamics 365 Supply Chain Management للطلبات المخططة للتأكيد التلقائي.</span><span class="sxs-lookup"><span data-stu-id="6765d-127">Both Planning Optimization and the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management can be used to auto-firm planned orders.</span></span> <span data-ttu-id="6765d-128">ومع ذلك، توجد بعض الاختلافات الهامة.</span><span class="sxs-lookup"><span data-stu-id="6765d-128">However, there are some important differences.</span></span> <span data-ttu-id="6765d-129">على سبيل المثال ، بينما يستخدم تحسين التخطيط تاريخ الأمر (اي ، تاريخ البدء) لتحديد الأوامر المخططة التي سيتم تاكيدها ، يستخدم محرك تخطيط Supply Chain Management المضمن تاريخ الطلب (أي تاريخ الانتهاء).</span><span class="sxs-lookup"><span data-stu-id="6765d-129">For example, whereas Planning Optimization uses the order date (that is, the start date) to determine which planned orders to firm, the built-in Supply Chain Management planning engine uses the requirement date (that is, the end date).</span></span> <span data-ttu-id="6765d-130">وفيما يلي ملخص للاختلافات.</span><span class="sxs-lookup"><span data-stu-id="6765d-130">Here is a summary of the differences.</span></span>

<span data-ttu-id="6765d-131">**تحسين التخطيط**</span><span class="sxs-lookup"><span data-stu-id="6765d-131">**Planning Optimization**</span></span>

- <span data-ttu-id="6765d-132">ويعتمد التاكيد التلقائي على تاريخ الأمر (تاريخ البدء).</span><span class="sxs-lookup"><span data-stu-id="6765d-132">Auto-firming is based on the order date (start date).</span></span>
- <span data-ttu-id="6765d-133">ونظرا لان تاريخ الأمر (تاريخ البدء) يقوم بتشغيل التاكيد، فلن تكون بحاجه إلى التفكير في زمن وصول البضاعة كجزء من الحد الزمني للتاكيد.</span><span class="sxs-lookup"><span data-stu-id="6765d-133">Because the order date (start date) triggers the firming, you don't have to consider the lead time as part of the firming time fence.</span></span>
- <span data-ttu-id="6765d-134">إذا كنت ترغب في تاكيد كافة الأوامر التي يجب أن تبدا خلال الأسبوع الحالي ، فيجب أن يكون الحد الزمني للتاكيد هو أسبوع واحد.</span><span class="sxs-lookup"><span data-stu-id="6765d-134">If you want to firm all orders that must start during the current week, the firming time fence must be one week.</span></span>

<span data-ttu-id="6765d-135">**محرك تخطيط Supply Chain Management المضمن**</span><span class="sxs-lookup"><span data-stu-id="6765d-135">**Built-in Supply Chain Management planning engine**</span></span>

- <span data-ttu-id="6765d-136">ويعتمد التاكيد التلقائي على تاريخ الطلب (تاريخ الانتهاء).</span><span class="sxs-lookup"><span data-stu-id="6765d-136">Auto-firming is based on the requirement date (end date).</span></span>
- <span data-ttu-id="6765d-137">للمساعدة في ضمان تاكيد الأوامر في الوقت المستحق ، يجب أن يكون الحد الزمني للتاكيد أطول من زمن وصول البضاعة.</span><span class="sxs-lookup"><span data-stu-id="6765d-137">To help guarantee that orders are firmed in due time, the firming time fence must be longer than the lead time.</span></span>
- <span data-ttu-id="6765d-138">إذا كنت ترغب في تاكيد كافة الأوامر التي يجب أن تبدا خلال الأسبوع الحالي ، فيجب أن يكون الحد الزمني هو زمن الوصول بالإضافة إلى أسبوع واحد.</span><span class="sxs-lookup"><span data-stu-id="6765d-138">If you want to firm all orders that must start during the current week, the firming time fence must be the lead time plus one week.</span></span>
