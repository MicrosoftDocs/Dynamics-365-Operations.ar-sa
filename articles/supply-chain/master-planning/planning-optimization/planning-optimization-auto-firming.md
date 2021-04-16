---
title: التأكيد التلقائي مع تحسين التخطيط
description: يشرح هذا الموضوع كيفيه استخدام التاكيد التلقائي مع تحسين التخطيط.
author: ChristianRytt
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 3542e343de29c9fd9d19ed99cab4b4eebacd2899
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812993"
---
# <a name="autofirming-with-planning-optimization"></a><span data-ttu-id="63107-103">التأكيد التلقائي مع تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="63107-103">Autofirming with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="63107-104">يتيح لك التاكيد التلقائي تاكيد (اي ، إصدار) الأوامر المخططة كجزء من عمليه التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="63107-104">Automatic firming lets you firm (that is, release) planned orders as part of the master planning process.</span></span> <span data-ttu-id="63107-105">عند تاكيد الأوامر المخططة ، يتم تحويلها إلى أوامر شراء فعليه أو أوامر تحويل أو أوامر إنتاج.</span><span class="sxs-lookup"><span data-stu-id="63107-105">When planned orders are firmed, they are transformed into actual purchase orders, transfer orders, or production orders.</span></span> <span data-ttu-id="63107-106">عند استخدام تحسين التخطيط ، يتم تاكيد الأوامر المخططة اثناء تشغيل التخطيط الرئيسي عندما يكون تاريخ الأمر (اي تاريخ البدء) خلال فتره الحد الزمني للتاكيد.</span><span class="sxs-lookup"><span data-stu-id="63107-106">When Planning Optimization is used, planned orders are firmed during a master planning run when the order date (that is, the start date) is within the time fence for firming.</span></span>

> [!NOTE]
> <span data-ttu-id="63107-107">ويمكن أن يحدث التأكيد التلقائي لأمر الشراء المخطط فقط إذا كان الصنف مقترنًا بمورِّد.</span><span class="sxs-lookup"><span data-stu-id="63107-107">Auto-firming of a planned purchase order can occur only if the item is associated with a vendor.</span></span>
> 
> <span data-ttu-id="63107-108">ستُظهر الطلبات المشتقة المؤكدة (أوامر الشراء الخاصة بالعقود من الباطن) حالة *قيد المراجعة* عندما يتم تمكين تعقب تغيير الحالة.</span><span class="sxs-lookup"><span data-stu-id="63107-108">Firmed derived orders (subcontract purchase orders) will show a status of *In-review* when case change tracking is enabled.</span></span>

## <a name="turn-on-autofirming"></a><span data-ttu-id="63107-109">تشغيل التاكيد التلقائي</span><span class="sxs-lookup"><span data-stu-id="63107-109">Turn on autofirming</span></span>

<span data-ttu-id="63107-110">لتشغيل التأكيد التلقائي‬، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="63107-110">To turn on autofirming, follow these steps.</span></span>

1. <span data-ttu-id="63107-111">في مساحة عمل **إدارة الميزات**، في علامة التبويب **جديد**، حدد **التأكيد التلقائي لتحسين التخطيط** في القائمة.</span><span class="sxs-lookup"><span data-stu-id="63107-111">In the **Feature management** workspace, on the **New** tab, select **Auto-firming for Planning Optimization** in the list.</span></span> <span data-ttu-id="63107-112">إذا لم تظهر الميزة على علامة التبويب **جديد**، فانظر إلى علامتي التبويب **غير ممكن** و **الكل**.</span><span class="sxs-lookup"><span data-stu-id="63107-112">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="63107-113">حدد **تمكين الآن**.</span><span class="sxs-lookup"><span data-stu-id="63107-113">Select **Enable now**.</span></span> <span data-ttu-id="63107-114">بدلاً من ذلك، حدد **جدولة**، ثم حدد الوقت الذي تريد فيه تشغيل الميزة.</span><span class="sxs-lookup"><span data-stu-id="63107-114">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

## <a name="set-up-the-firming-time-fence"></a><span data-ttu-id="63107-115">إعداد الحد الزمني للتأكيد</span><span class="sxs-lookup"><span data-stu-id="63107-115">Set up the firming time fence</span></span>

<span data-ttu-id="63107-116">يتم حساب الحد الزمني للتأكيد بداية من تاريخ تشغيل التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="63107-116">The firming time fence is calculated forward from the master planning run date.</span></span> <span data-ttu-id="63107-117">يتم تحديده بعدد أيام السماح الذي تقوم بإدخاله.</span><span class="sxs-lookup"><span data-stu-id="63107-117">It's defined by the number of days that you enter.</span></span> <span data-ttu-id="63107-118">يمكنك التحكم في الحد الزمني للتاكيد بالطرق التالية:</span><span class="sxs-lookup"><span data-stu-id="63107-118">You can control the firming time fence in the following ways:</span></span>

- <span data-ttu-id="63107-119">لتحديد الحد الافتراضي لوقت التأكيد لأحدي مجموعات التغطية، انتقل إلى **التخطيط الرئيسي** \> **الإعداد** \> **التغطية** \> **مجموعات التغطية**، وحدد مجموعة تغطية.</span><span class="sxs-lookup"><span data-stu-id="63107-119">To define the default firming time fence for a coverage group, go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage groups**, and select a coverage group.</span></span> <span data-ttu-id="63107-120">ثم من علامة التبويب السريعة **آخر**، في حقل **الحد الزمني للتأكيد التلقائي (الأيام)**، أدخل عدد الأيام.</span><span class="sxs-lookup"><span data-stu-id="63107-120">Then, on the **Other** FastTab, in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="63107-121">للكتابة فوق الحد الزمني للتأكيد المحدد لمجموعة التغطية الخاصة بصنف معين، انتقل إلى **إدارة معلومات المنتج** \> **المنتجات الصادرة**، ثم من جزء الإجراء، حدد **خطة**، ثم حدد **تغطية العنصر**.</span><span class="sxs-lookup"><span data-stu-id="63107-121">To overwrite the firming time fence that is defined for the coverage group for a specific item, go to **Product information management** \> **Released products**, then from the Action Pane select **Plan** and then select **Item coverage**.</span></span> <span data-ttu-id="63107-122">ثم، في علامة التبويب **عام**، حدد **تجاوز الحد الزمني** وفي حقل **الحد الزمني للتأكيد التلقائي (الأيام)**، أدخل عدد الأيام.</span><span class="sxs-lookup"><span data-stu-id="63107-122">Then, on the **General** tab, select **Override time fence** and in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="63107-123">للكتابة فوق الحد الزمني للتأكيد المحدد لمجموعة التغطية وتغطيه الصنف لخطة رئيسيه معينه، انتقل إلى **التخطيط الرئيسي** \> **إعداد** \>**الخطط الرئيسية**، وحدد خطة رئيسيه.</span><span class="sxs-lookup"><span data-stu-id="63107-123">To overwrite the firming time fence that is defined for the coverage group and item coverage for a specific master plan, go to **Master planning** \> **Setup** \> **Master plans**, and select a Master plan.</span></span> <span data-ttu-id="63107-124">ثم في علامة التبويب السريعة **الحد الزمني بالأيام**، قم بتعيين **تأكيد** إلى **نعم**، وأدخل عدد الأيام.</span><span class="sxs-lookup"><span data-stu-id="63107-124">Then, on the **Time fence in days** FastTab, set **Firming** to **Yes**, and enter the number of days.</span></span>

<span data-ttu-id="63107-125">في حالة تشغيل التاكيد التلقائي لتشغيل التخطيط الرئيسي الذي يستخدم تحسين التخطيط ، تتم عمليه التاكيد التلقائي وفقا لإعداد التاكيد التلقائي.</span><span class="sxs-lookup"><span data-stu-id="63107-125">If autofirming is turned on for a master planning run that uses Planning Optimization, the autofirming process is done according to the autofirming setup.</span></span> <span data-ttu-id="63107-126">في حالة عدم تشغيل التاكيد التلقائي، أو في حالة بدء التخطيط من صفحة **صافي المتطلبات**، يتم تخطي عمليه التأكيد التلقائي.</span><span class="sxs-lookup"><span data-stu-id="63107-126">If autofirming isn't turned on, or if planning is started from the **Net requirements** page, the autofirming process is skipped.</span></span>

## <a name="planning-optimization-vs-the-built-in-supply-chain-management-planning-engine"></a><span data-ttu-id="63107-127">تحسين التخطيط مقابل محرك تخطيط Supply Chain Management المضمن</span><span class="sxs-lookup"><span data-stu-id="63107-127">Planning Optimization vs. the built-in Supply Chain Management planning engine</span></span>

<span data-ttu-id="63107-128">يمكن استخدام كل من تحسين التخطيط ومحرك التخطيط المضمن في Microsoft Dynamics 365 Supply Chain Management للطلبات المخططة للتأكيد التلقائي.</span><span class="sxs-lookup"><span data-stu-id="63107-128">Both Planning Optimization and the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management can be used to autofirm planned orders.</span></span> <span data-ttu-id="63107-129">ومع ذلك، توجد بعض الاختلافات الهامة.</span><span class="sxs-lookup"><span data-stu-id="63107-129">However, there are some important differences.</span></span> <span data-ttu-id="63107-130">على سبيل المثال ، بينما يستخدم تحسين التخطيط تاريخ الأمر (اي ، تاريخ البدء) لتحديد الأوامر المخططة التي سيتم تاكيدها ، يستخدم محرك تخطيط Supply Chain Management المضمن تاريخ الطلب (أي تاريخ الانتهاء).</span><span class="sxs-lookup"><span data-stu-id="63107-130">For example, whereas Planning Optimization uses the order date (that is, the start date) to determine which planned orders to firm, the built-in Supply Chain Management planning engine uses the requirement date (that is, the end date).</span></span> <span data-ttu-id="63107-131">وفيما يلي ملخص للاختلافات.</span><span class="sxs-lookup"><span data-stu-id="63107-131">Here is a summary of the differences.</span></span>

<span data-ttu-id="63107-132">**تحسين التخطيط**</span><span class="sxs-lookup"><span data-stu-id="63107-132">**Planning Optimization**</span></span>

- <span data-ttu-id="63107-133">ويعتمد التاكيد التلقائي على تاريخ الأمر (تاريخ البدء).</span><span class="sxs-lookup"><span data-stu-id="63107-133">Autofirming is based on the order date (start date).</span></span>
- <span data-ttu-id="63107-134">ونظرا لان تاريخ الأمر (تاريخ البدء) يقوم بتشغيل التاكيد، فلن تكون بحاجه إلى التفكير في زمن وصول البضاعة كجزء من الحد الزمني للتاكيد.</span><span class="sxs-lookup"><span data-stu-id="63107-134">Because the order date (start date) triggers the firming, you don't have to consider the lead time as part of the firming time fence.</span></span>
- <span data-ttu-id="63107-135">إذا كنت ترغب في تاكيد كافة الأوامر التي يجب أن تبدا خلال الأسبوع الحالي ، فيجب أن يكون الحد الزمني للتاكيد هو أسبوع واحد.</span><span class="sxs-lookup"><span data-stu-id="63107-135">If you want to firm all orders that must start during the current week, the firming time fence must be one week.</span></span>

<span data-ttu-id="63107-136">**محرك تخطيط Supply Chain Management المضمن**</span><span class="sxs-lookup"><span data-stu-id="63107-136">**Built-in Supply Chain Management planning engine**</span></span>

- <span data-ttu-id="63107-137">ويعتمد التاكيد التلقائي على تاريخ الطلب (تاريخ الانتهاء).</span><span class="sxs-lookup"><span data-stu-id="63107-137">Autofirming is based on the requirement date (end date).</span></span>
- <span data-ttu-id="63107-138">للمساعدة في ضمان تاكيد الأوامر في الوقت المستحق ، يجب أن يكون الحد الزمني للتاكيد أطول من زمن وصول البضاعة.</span><span class="sxs-lookup"><span data-stu-id="63107-138">To help guarantee that orders are firmed in due time, the firming time fence must be longer than the lead time.</span></span>
- <span data-ttu-id="63107-139">إذا كنت ترغب في تاكيد كافة الأوامر التي يجب أن تبدا خلال الأسبوع الحالي ، فيجب أن يكون الحد الزمني هو زمن الوصول بالإضافة إلى أسبوع واحد.</span><span class="sxs-lookup"><span data-stu-id="63107-139">If you want to firm all orders that must start during the current week, the firming time fence must be the lead time plus one week.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
