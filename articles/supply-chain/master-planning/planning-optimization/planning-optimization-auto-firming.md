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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-30
ms.dyn365.ops.version: AX 10.0.7
ms.openlocfilehash: 9106137fe6dd097beea9914cdde541e581946f46
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227784"
---
# <a name="autofirming-with-planning-optimization"></a><span data-ttu-id="dbe66-103">التأكيد التلقائي مع تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="dbe66-103">Autofirming with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dbe66-104">يتيح لك التاكيد التلقائي تاكيد (اي ، إصدار) الأوامر المخططة كجزء من عمليه التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="dbe66-104">Automatic firming lets you firm (that is, release) planned orders as part of the master planning process.</span></span> <span data-ttu-id="dbe66-105">عند تاكيد الأوامر المخططة ، يتم تحويلها إلى أوامر شراء فعليه أو أوامر تحويل أو أوامر إنتاج.</span><span class="sxs-lookup"><span data-stu-id="dbe66-105">When planned orders are firmed, they are transformed into actual purchase orders, transfer orders, or production orders.</span></span> <span data-ttu-id="dbe66-106">عند استخدام تحسين التخطيط ، يتم تاكيد الأوامر المخططة اثناء تشغيل التخطيط الرئيسي عندما يكون تاريخ الأمر (اي تاريخ البدء) خلال فتره الحد الزمني للتاكيد.</span><span class="sxs-lookup"><span data-stu-id="dbe66-106">When Planning Optimization is used, planned orders are firmed during a master planning run when the order date (that is, the start date) is within the time fence for firming.</span></span>

> [!NOTE]
> <span data-ttu-id="dbe66-107">ويمكن أن يحدث التأكيد التلقائي لأمر الشراء المخطط فقط إذا كان الصنف مقترنًا بمورِّد.</span><span class="sxs-lookup"><span data-stu-id="dbe66-107">Auto-firming of a planned purchase order can occur only if the item is associated with a vendor.</span></span>

## <a name="turn-on-autofirming"></a><span data-ttu-id="dbe66-108">تشغيل التاكيد التلقائي</span><span class="sxs-lookup"><span data-stu-id="dbe66-108">Turn on autofirming</span></span>

<span data-ttu-id="dbe66-109">لتشغيل التأكيد التلقائي‬، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="dbe66-109">To turn on autofirming, follow these steps.</span></span>

1. <span data-ttu-id="dbe66-110">في مساحة عمل **إدارة الميزات**، في علامة التبويب **جديد**، حدد **التأكيد التلقائي لتحسين التخطيط** في القائمة.</span><span class="sxs-lookup"><span data-stu-id="dbe66-110">In the **Feature management** workspace, on the **New** tab, select **Auto-firming for Planning Optimization** in the list.</span></span> <span data-ttu-id="dbe66-111">إذا لم تظهر الميزة على علامة التبويب **جديد**، فانظر إلى علامتي التبويب **غير ممكن** و **الكل**.</span><span class="sxs-lookup"><span data-stu-id="dbe66-111">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="dbe66-112">حدد **تمكين الآن**.</span><span class="sxs-lookup"><span data-stu-id="dbe66-112">Select **Enable now**.</span></span> <span data-ttu-id="dbe66-113">بدلاً من ذلك، حدد **جدولة**، ثم حدد الوقت الذي تريد فيه تشغيل الميزة.</span><span class="sxs-lookup"><span data-stu-id="dbe66-113">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

## <a name="set-up-the-firming-time-fence"></a><span data-ttu-id="dbe66-114">إعداد الحد الزمني للتأكيد</span><span class="sxs-lookup"><span data-stu-id="dbe66-114">Set up the firming time fence</span></span>

<span data-ttu-id="dbe66-115">يتم حساب الحد الزمني للتأكيد بداية من تاريخ تشغيل التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="dbe66-115">The firming time fence is calculated forward from the master planning run date.</span></span> <span data-ttu-id="dbe66-116">يتم تحديده بعدد أيام السماح الذي تقوم بإدخاله.</span><span class="sxs-lookup"><span data-stu-id="dbe66-116">It's defined by the number of days that you enter.</span></span> <span data-ttu-id="dbe66-117">يمكنك التحكم في الحد الزمني للتاكيد بالطرق التالية:</span><span class="sxs-lookup"><span data-stu-id="dbe66-117">You can control the firming time fence in the following ways:</span></span>

- <span data-ttu-id="dbe66-118">لتحديد الحد الافتراضي لوقت التأكيد لأحدي مجموعات التغطية، انتقل إلى **التخطيط الرئيسي** \> **الإعداد** \> **التغطية** \> **مجموعات التغطية**، وحدد مجموعة تغطية.</span><span class="sxs-lookup"><span data-stu-id="dbe66-118">To define the default firming time fence for a coverage group, go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage groups**, and select a coverage group.</span></span> <span data-ttu-id="dbe66-119">ثم من علامة التبويب السريعة **آخر**، في حقل **الحد الزمني للتأكيد التلقائي (الأيام)**، أدخل عدد الأيام.</span><span class="sxs-lookup"><span data-stu-id="dbe66-119">Then, on the **Other** FastTab, in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="dbe66-120">للكتابة فوق الحد الزمني للتأكيد المحدد لمجموعة التغطية الخاصة بصنف معين، انتقل إلى **إدارة معلومات المنتج** \> **المنتجات الصادرة**، ثم من جزء الإجراء، حدد **خطة**، ثم حدد **تغطية العنصر**.</span><span class="sxs-lookup"><span data-stu-id="dbe66-120">To overwrite the firming time fence that is defined for the coverage group for a specific item, go to **Product information management** \> **Released products**, then from the Action Pane select **Plan** and then select **Item coverage**.</span></span> <span data-ttu-id="dbe66-121">ثم، في علامة التبويب **عام**، حدد **تجاوز الحد الزمني** وفي حقل **الحد الزمني للتأكيد التلقائي (الأيام)**، أدخل عدد الأيام.</span><span class="sxs-lookup"><span data-stu-id="dbe66-121">Then, on the **General** tab, select **Override time fence** and in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="dbe66-122">للكتابة فوق الحد الزمني للتأكيد المحدد لمجموعة التغطية وتغطيه الصنف لخطة رئيسيه معينه، انتقل إلى **التخطيط الرئيسي** \> **إعداد** \>**الخطط الرئيسية**، وحدد خطة رئيسيه.</span><span class="sxs-lookup"><span data-stu-id="dbe66-122">To overwrite the firming time fence that is defined for the coverage group and item coverage for a specific master plan, go to **Master planning** \> **Setup** \> **Master plans**, and select a Master plan.</span></span> <span data-ttu-id="dbe66-123">ثم في علامة التبويب السريعة **الحد الزمني بالأيام**، قم بتعيين **تأكيد** إلى **نعم**، وأدخل عدد الأيام.</span><span class="sxs-lookup"><span data-stu-id="dbe66-123">Then, on the **Time fence in days** FastTab, set **Firming** to **Yes**, and enter the number of days.</span></span>

<span data-ttu-id="dbe66-124">في حالة تشغيل التاكيد التلقائي لتشغيل التخطيط الرئيسي الذي يستخدم تحسين التخطيط ، تتم عمليه التاكيد التلقائي وفقا لإعداد التاكيد التلقائي.</span><span class="sxs-lookup"><span data-stu-id="dbe66-124">If autofirming is turned on for a master planning run that uses Planning Optimization, the autofirming process is done according to the autofirming setup.</span></span> <span data-ttu-id="dbe66-125">في حالة عدم تشغيل التاكيد التلقائي، أو في حالة بدء التخطيط من صفحة **صافي المتطلبات**، يتم تخطي عمليه التأكيد التلقائي.</span><span class="sxs-lookup"><span data-stu-id="dbe66-125">If autofirming isn't turned on, or if planning is started from the **Net requirements** page, the autofirming process is skipped.</span></span>

## <a name="planning-optimization-vs-the-built-in-supply-chain-management-planning-engine"></a><span data-ttu-id="dbe66-126">تحسين التخطيط مقابل محرك تخطيط Supply Chain Management المضمن</span><span class="sxs-lookup"><span data-stu-id="dbe66-126">Planning Optimization vs. the built-in Supply Chain Management planning engine</span></span>

<span data-ttu-id="dbe66-127">يمكن استخدام كل من تحسين التخطيط ومحرك التخطيط المضمن في Microsoft Dynamics 365 Supply Chain Management للطلبات المخططة للتأكيد التلقائي.</span><span class="sxs-lookup"><span data-stu-id="dbe66-127">Both Planning Optimization and the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management can be used to autofirm planned orders.</span></span> <span data-ttu-id="dbe66-128">ومع ذلك، توجد بعض الاختلافات الهامة.</span><span class="sxs-lookup"><span data-stu-id="dbe66-128">However, there are some important differences.</span></span> <span data-ttu-id="dbe66-129">على سبيل المثال ، بينما يستخدم تحسين التخطيط تاريخ الأمر (اي ، تاريخ البدء) لتحديد الأوامر المخططة التي سيتم تاكيدها ، يستخدم محرك تخطيط Supply Chain Management المضمن تاريخ الطلب (أي تاريخ الانتهاء).</span><span class="sxs-lookup"><span data-stu-id="dbe66-129">For example, whereas Planning Optimization uses the order date (that is, the start date) to determine which planned orders to firm, the built-in Supply Chain Management planning engine uses the requirement date (that is, the end date).</span></span> <span data-ttu-id="dbe66-130">وفيما يلي ملخص للاختلافات.</span><span class="sxs-lookup"><span data-stu-id="dbe66-130">Here is a summary of the differences.</span></span>

<span data-ttu-id="dbe66-131">**تحسين التخطيط**</span><span class="sxs-lookup"><span data-stu-id="dbe66-131">**Planning Optimization**</span></span>

- <span data-ttu-id="dbe66-132">ويعتمد التاكيد التلقائي على تاريخ الأمر (تاريخ البدء).</span><span class="sxs-lookup"><span data-stu-id="dbe66-132">Autofirming is based on the order date (start date).</span></span>
- <span data-ttu-id="dbe66-133">ونظرا لان تاريخ الأمر (تاريخ البدء) يقوم بتشغيل التاكيد، فلن تكون بحاجه إلى التفكير في زمن وصول البضاعة كجزء من الحد الزمني للتاكيد.</span><span class="sxs-lookup"><span data-stu-id="dbe66-133">Because the order date (start date) triggers the firming, you don't have to consider the lead time as part of the firming time fence.</span></span>
- <span data-ttu-id="dbe66-134">إذا كنت ترغب في تاكيد كافة الأوامر التي يجب أن تبدا خلال الأسبوع الحالي ، فيجب أن يكون الحد الزمني للتاكيد هو أسبوع واحد.</span><span class="sxs-lookup"><span data-stu-id="dbe66-134">If you want to firm all orders that must start during the current week, the firming time fence must be one week.</span></span>

<span data-ttu-id="dbe66-135">**محرك تخطيط Supply Chain Management المضمن**</span><span class="sxs-lookup"><span data-stu-id="dbe66-135">**Built-in Supply Chain Management planning engine**</span></span>

- <span data-ttu-id="dbe66-136">ويعتمد التاكيد التلقائي على تاريخ الطلب (تاريخ الانتهاء).</span><span class="sxs-lookup"><span data-stu-id="dbe66-136">Autofirming is based on the requirement date (end date).</span></span>
- <span data-ttu-id="dbe66-137">للمساعدة في ضمان تاكيد الأوامر في الوقت المستحق ، يجب أن يكون الحد الزمني للتاكيد أطول من زمن وصول البضاعة.</span><span class="sxs-lookup"><span data-stu-id="dbe66-137">To help guarantee that orders are firmed in due time, the firming time fence must be longer than the lead time.</span></span>
- <span data-ttu-id="dbe66-138">إذا كنت ترغب في تاكيد كافة الأوامر التي يجب أن تبدا خلال الأسبوع الحالي ، فيجب أن يكون الحد الزمني هو زمن الوصول بالإضافة إلى أسبوع واحد.</span><span class="sxs-lookup"><span data-stu-id="dbe66-138">If you want to firm all orders that must start during the current week, the firming time fence must be the lead time plus one week.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]