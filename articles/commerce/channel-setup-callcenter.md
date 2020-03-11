---
title: إعداد قناة مركز اتصال
description: يوضح هذا الموضوع كيفية إنشاء قناة مركز اتصال جديدة في Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 42448bd54c00b8642b158f422e17d2b46ee25579
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057869"
---
# <a name="set-up-a-call-center-channel"></a><span data-ttu-id="dfa34-103">إعداد قناة مركز اتصال</span><span class="sxs-lookup"><span data-stu-id="dfa34-103">Set up a call center channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="dfa34-104">يوضح هذا الموضوع كيفية إنشاء قناة مركز اتصال جديدة في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="dfa34-104">This topic describes how to create a new call center channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="dfa34-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="dfa34-105">Overview</span></span>

<span data-ttu-id="dfa34-106">في Dynamics 365 Commerce، يعتبر مركز الاتصال نوع قناة يمكن تعريفها في التطبيق.</span><span class="sxs-lookup"><span data-stu-id="dfa34-106">In Dynamics 365 Commerce, a call center is a type of channel that can be defined in the application.</span></span> <span data-ttu-id="dfa34-107">من شأن تحديد قناة لكيانات مركز الاتصال أن يسمح للنظام بربط بيانات معينة والإعدادات الافتراضية لمعالجة الأوامر بأوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="dfa34-107">Defining a channel for your call center entities allows the system to tie specific data and order processing defaults to sales orders.</span></span> <span data-ttu-id="dfa34-108">بإمكان شركة تعريف قنوات مراكز اتصال متعددة في Commerce.</span><span class="sxs-lookup"><span data-stu-id="dfa34-108">A company can define multiple call center channels in Commerce.</span></span> 

<span data-ttu-id="dfa34-109">قبل إنشاء قناة مركز اتصال جديدة، تأكد من إكمال [المتطلبات الأساسية لإعداد قناة](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="dfa34-109">Before you create a new call center channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-call-center-channel"></a><span data-ttu-id="dfa34-110">إنشاء قناة مركز اتصال جديدة وتكوينها</span><span class="sxs-lookup"><span data-stu-id="dfa34-110">Create and configure a new call center channel</span></span>

<span data-ttu-id="dfa34-111">لإنشاء قناة مركز اتصال جديدة وتكوينها، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="dfa34-111">To create and configure a new call center channel, follow these steps.</span></span>

1. <span data-ttu-id="dfa34-112">في جزء التنقل، انتقل إل **الوحدات \> القنوات \> مراكز الاتصال \> جميع مراكز الاتصال**.</span><span class="sxs-lookup"><span data-stu-id="dfa34-112">In the navigation pane, go to **Modules \> Channels \> Call centers \> All call centers**.</span></span>
1. <span data-ttu-id="dfa34-113">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="dfa34-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="dfa34-114">في حقل **الاسم** أدخل اسمًا للقناة الجديدة.</span><span class="sxs-lookup"><span data-stu-id="dfa34-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="dfa34-115">حدد **الكيان القانوني** المناسب من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="dfa34-115">Select the appropriate **Legal entity** from the drop down.</span></span>
1. <span data-ttu-id="dfa34-116">حدد **المستودع** المناسب من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="dfa34-116">Select the appropriate **Warehouse** location from the drop down.</span></span>
1. <span data-ttu-id="dfa34-117">في حقل **العميل الافتراضي**، أدخل عميل افتراضي صالح.</span><span class="sxs-lookup"><span data-stu-id="dfa34-117">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="dfa34-118">في الحقل **ملف تعريف الإخطار بالبريد الإلكتروني**، أدخل ملف تعريف إخطار بالبريد الإلكتروني صالحًا.</span><span class="sxs-lookup"><span data-stu-id="dfa34-118">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="dfa34-119">قدم كود معلومات **تجاوز السعر**.</span><span class="sxs-lookup"><span data-stu-id="dfa34-119">Provide a **Price override** info code.</span></span> <span data-ttu-id="dfa34-120">قد تحتاج إلى إنشاء كود معلومات لهذا أولاً.</span><span class="sxs-lookup"><span data-stu-id="dfa34-120">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="dfa34-121">قدم كود معلومات **كود الانتظار**.</span><span class="sxs-lookup"><span data-stu-id="dfa34-121">Provide a **Hold code** info code.</span></span> <span data-ttu-id="dfa34-122">قد تحتاج إلى إنشاء كود معلومات لهذا أولاً.</span><span class="sxs-lookup"><span data-stu-id="dfa34-122">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="dfa34-123">قدم كود معلومات **الائتمان**.</span><span class="sxs-lookup"><span data-stu-id="dfa34-123">Provide a **Credit** info code.</span></span> <span data-ttu-id="dfa34-124">قد تحتاج إلى إنشاء كود معلومات لهذا أولاً.</span><span class="sxs-lookup"><span data-stu-id="dfa34-124">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="dfa34-125">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="dfa34-125">Select **Save**.</span></span>

<span data-ttu-id="dfa34-126">توضح الصورة التالية إنشاء قناة مركز اتصال جديدة.</span><span class="sxs-lookup"><span data-stu-id="dfa34-126">The following image shows the creation of a new call center channel.</span></span>

![قناة مركز اتصال جديدة](media/channel-setup-callcenter-1.png)

<span data-ttu-id="dfa34-128">تعرض الصورة التالية مثالاً لقناة مركز اتصال.</span><span class="sxs-lookup"><span data-stu-id="dfa34-128">The following image shows an example call center channel.</span></span>

![مثال قناة مركز اتصال](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a><span data-ttu-id="dfa34-130">إعداد إضافي للقناة</span><span class="sxs-lookup"><span data-stu-id="dfa34-130">Additional channel setup</span></span>

<span data-ttu-id="dfa34-131">تتضمن المهام الإضافية المطلوبة لإعداد قناة مركز الاتصال إعداد طرق الدفع وأوضاع التسليم.</span><span class="sxs-lookup"><span data-stu-id="dfa34-131">Additional tasks required for call center channel setup include setting up payment methods and modes of delivery.</span></span>

<span data-ttu-id="dfa34-132">تُظهر الصورة التالية خيارات إعداد **أوضاع التسليم** و**طرق الدفع** على علامة تبويب **الإعداد**.</span><span class="sxs-lookup"><span data-stu-id="dfa34-132">The following image shows **Modes of delivery** and **Payment methods** set up options on the **Set up** tab.</span></span>

![إجراءات إعداد إضافية لقناة مركز الاتصال](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="dfa34-134">إعداد طرق الدفع</span><span class="sxs-lookup"><span data-stu-id="dfa34-134">Set up payment methods</span></span>

<span data-ttu-id="dfa34-135">لإعداد طرق الدفع، لكل نوع دفع معتمد على هذه القناة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="dfa34-135">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="dfa34-136">في جزء الإجراءات، حدد علامة التبويب **الإعداد**، ثم حدد **طرق الدفع**.</span><span class="sxs-lookup"><span data-stu-id="dfa34-136">On the action pane, select the **Set up** tab, and then select **Payment methods**.</span></span>
1. <span data-ttu-id="dfa34-137">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="dfa34-137">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="dfa34-138">في جزء التنقل، حدد طريقة الدفع المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="dfa34-138">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="dfa34-139">في القسم **عام**، أدخل **اسم العملية**، وقم بتكوين أي إعدادات أخرى مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="dfa34-139">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="dfa34-140">قم بتكوين أي إعدادات إضافية مطلوبة لنوع الدفع.</span><span class="sxs-lookup"><span data-stu-id="dfa34-140">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="dfa34-141">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="dfa34-141">On the action pane, select **Save**.</span></span>

<span data-ttu-id="dfa34-142">تعرض الصورة التالية مثالاً عن طريقة الدفع النقدي.</span><span class="sxs-lookup"><span data-stu-id="dfa34-142">The following image shows an example of a cash payment method.</span></span>

![أمثلة عن طرق الدفع](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="dfa34-144">إعداد أوضاع التسليم</span><span class="sxs-lookup"><span data-stu-id="dfa34-144">Set up modes of delivery</span></span>

<span data-ttu-id="dfa34-145">يمكنك الاطلاع على أوضاع التسليم التي تم تكوينها عن طريق تحديد **أوضاع التسليم** من علامة التبويب **الإعداد** على **جزء الإجراءات**.</span><span class="sxs-lookup"><span data-stu-id="dfa34-145">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="dfa34-146">لتغيير وضع التسليم أو إضافته، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="dfa34-146">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="dfa34-147">في جزء التنقل، انتقل إلى **الوحدات \> إدارة المخزون \> أوضاع التسليم**.</span><span class="sxs-lookup"><span data-stu-id="dfa34-147">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="dfa34-148">في جزء الإجراءات، حدد **جديد** لإنشاء وضع تسليم جديد، أو حدد وضعًا موجودًا.</span><span class="sxs-lookup"><span data-stu-id="dfa34-148">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="dfa34-149">في قسم **قنوات البيع بالتجزئة**، حدد **إضافة بند** لإضافة القناة.</span><span class="sxs-lookup"><span data-stu-id="dfa34-149">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="dfa34-150">تؤدي إضافة قنوات باستخدام عقد المؤسسة بدلاً من إضافة كل قناة بشكل فردي إلى تنظيم عملية إضافة القنوات.</span><span class="sxs-lookup"><span data-stu-id="dfa34-150">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="dfa34-151">تعرض الصورة التالية مثالاً لوضع التسليم.</span><span class="sxs-lookup"><span data-stu-id="dfa34-151">The following image shows an example of a mode of delivery.</span></span>

![إعداد أوضاع التسليم](media/channel-setup-retail-7.png)

## <a name="additional-resources"></a><span data-ttu-id="dfa34-153">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="dfa34-153">Additional resources</span></span>

[<span data-ttu-id="dfa34-154">المتطلبات الأساسية‬ لإعداد قناة</span><span class="sxs-lookup"><span data-stu-id="dfa34-154">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="dfa34-155">وظيفة مبيعات مركز الاتصال</span><span class="sxs-lookup"><span data-stu-id="dfa34-155">Call center sales functionality</span></span>](call-center-functionality.md)

[<span data-ttu-id="dfa34-156">إعداد خيارات معالجة أوامر مركز الاتصال</span><span class="sxs-lookup"><span data-stu-id="dfa34-156">Set up call center order processing options</span></span>](set-up-order-processing-options.md)

[<span data-ttu-id="dfa34-157">كتالوجات مركز الاتصال</span><span class="sxs-lookup"><span data-stu-id="dfa34-157">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="dfa34-158">إعداد تنبيهات الاحتيال والعمل باستخدامها</span><span class="sxs-lookup"><span data-stu-id="dfa34-158">Set up and work with fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="dfa34-159">إعداد برامج الاستمرارية لمراكز الاتصال</span><span class="sxs-lookup"><span data-stu-id="dfa34-159">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)
