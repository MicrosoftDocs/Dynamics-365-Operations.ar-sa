---
title: إعداد قناة مركز اتصال
description: يوضح هذا الموضوع كيفية إنشاء قناة مركز اتصال جديدة في Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 03/13/2020
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
ms.openlocfilehash: 3f8c47c00b920dae01213d1d241ac8ee6a18d4e3
ms.sourcegitcommit: 776758a0ff95c3c7398986095104d1d2b9814514
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/24/2020
ms.locfileid: "4107174"
---
# <a name="set-up-a-call-center-channel"></a><span data-ttu-id="72e98-103">إعداد قناة مركز اتصال</span><span class="sxs-lookup"><span data-stu-id="72e98-103">Set up a call center channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="72e98-104">يوضح هذا الموضوع كيفية إنشاء قناة مركز اتصال جديدة في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="72e98-104">This topic describes how to create a new call center channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="72e98-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="72e98-105">Overview</span></span>


<span data-ttu-id="72e98-106">في Dynamics 365 Commerce، يعتبر مركز الاتصال نوع قناة Commerce يمكن تعريفها في التطبيق.</span><span class="sxs-lookup"><span data-stu-id="72e98-106">In Dynamics 365 Commerce, a call center is a type of Commerce channel that can be defined in the application.</span></span> <span data-ttu-id="72e98-107">من شأن تحديد قناة لكيانات مركز الاتصال أن يسمح للنظام بربط بيانات معينة والإعدادات الافتراضية لمعالجة الأوامر بأوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="72e98-107">Defining a channel for your call center entities allows the system to tie specific data and order processing defaults to sales orders.</span></span> <span data-ttu-id="72e98-108">بينما تستطيع الشركة تحديد قنوات مراكز اتصالات متعددة في Commerce، من الضروري الإشارة إلى أنه يمكن ربط مستخدم فردي فقط بقناة مركز اتصال.</span><span class="sxs-lookup"><span data-stu-id="72e98-108">While a company can define multiple call center channels in Commerce, it is important to note that an individual user may only be linked to one call center channel.</span></span> 

<span data-ttu-id="72e98-109">قبل إنشاء قناة مركز اتصال جديدة، تأكد من إكمال [المتطلبات الأساسية لإعداد قناة](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="72e98-109">Before you create a new call center channel, ensure that you have completed the [Channel setup prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-call-center-channel"></a><span data-ttu-id="72e98-110">إنشاء قناة مركز اتصال جديدة وتكوينها</span><span class="sxs-lookup"><span data-stu-id="72e98-110">Create and configure a new call center channel</span></span>

<span data-ttu-id="72e98-111">لإنشاء قناة مركز اتصال جديدة وتكوينها، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="72e98-111">To create and configure a new call center channel, follow these steps.</span></span>

1. <span data-ttu-id="72e98-112">في جزء التنقل، انتقل إلى **Retail and Commerce \> القنوات \> مراكز الاتصال \> كافة مراكز الاتصال**.</span><span class="sxs-lookup"><span data-stu-id="72e98-112">In the navigation pane, go to **Retail and Commerce \> Channels \> Call centers \> All call centers**.</span></span>
1. <span data-ttu-id="72e98-113">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="72e98-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="72e98-114">في حقل **الاسم** أدخل اسمًا للقناة الجديدة.</span><span class="sxs-lookup"><span data-stu-id="72e98-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="72e98-115">حدد **الكيان القانوني** المناسب من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="72e98-115">Select the appropriate **Legal entity** from the drop-down.</span></span>
1. <span data-ttu-id="72e98-116">حدد موقع **المستودع** المناسب من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="72e98-116">Select the appropriate **Warehouse** location from the drop-down.</span></span> <span data-ttu-id="72e98-117">سيتم استخدام هذا الموقع كإعداد افتراضي في أوامر المبيعات التي تم إنشاؤها لقناة مركز الاتصال هذا، إلا في حال تم تحديد إعدادات افتراضية أخرى على مستوى الصنف أو العميل.</span><span class="sxs-lookup"><span data-stu-id="72e98-117">This location will be used as the default on sales orders created for this call center channel, unless other defaults have been defined at the customer or item level.</span></span>
1. <span data-ttu-id="72e98-118">في حقل **العميل الافتراضي** ، أدخل عميل افتراضي صالح.</span><span class="sxs-lookup"><span data-stu-id="72e98-118">In the **Default customer** field, provide a valid default customer.</span></span> <span data-ttu-id="72e98-119">تستخدم هذه البيانات للمساعدة في الملء التلقائي للإعدادات الافتراضية عند إنشاء سجلات عملاء جديدة.</span><span class="sxs-lookup"><span data-stu-id="72e98-119">This data is used to assist in autopopulating defaults when new customer records are created.</span></span> <span data-ttu-id="72e98-120">عند إنشاء أوامر مركز اتصال، لا ينصح بإنشاء أوامر للعميل الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="72e98-120">When creating call center orders, it is not advisable to create orders for the default customer.</span></span>
1. <span data-ttu-id="72e98-121">في الحقل **ملف تعريف الإخطار بالبريد الإلكتروني** ، أدخل ملف تعريف إخطار بالبريد الإلكتروني صالحًا.</span><span class="sxs-lookup"><span data-stu-id="72e98-121">In the **Email notification profile** field, provide a valid email notification profile.</span></span> <span data-ttu-id="72e98-122">بينما يتم إنشاء أوامر مركز الاتصال ومعالجتها، يتم استخدام ملف تعريف الإخطار بالبريد الإلكتروني لتشغيل تنبيهات البريد الإلكتروني التلقائية للعملاء مع معلومات حول حالة أوامرهم.</span><span class="sxs-lookup"><span data-stu-id="72e98-122">As call center orders are created and processed, the email notification profile is used to trigger automated email alerts to customers with information about their order status.</span></span>
1. <span data-ttu-id="72e98-123">قدم كود معلومات **تجاوز السعر**.</span><span class="sxs-lookup"><span data-stu-id="72e98-123">Provide a **Price override** info code.</span></span> <span data-ttu-id="72e98-124">قد تحتاج إلى إنشاء كود معلومات لهذا أولاً.</span><span class="sxs-lookup"><span data-stu-id="72e98-124">You may need to create an info code for this first.</span></span> <span data-ttu-id="72e98-125">يوفر كود المعلومات هذا مجموعه أكواد السبب التي ستتم مطالبة المستخدم بالاختيار من بينها عند استخدام وظيفة تجاوز السعر في أمر مركز الاتصال.</span><span class="sxs-lookup"><span data-stu-id="72e98-125">This info code provides the set of reason codes that the user will be prompted to choose from when using the price override functionality on a call center order.</span></span>
1. <span data-ttu-id="72e98-126">قدم كود معلومات **كود الانتظار**.</span><span class="sxs-lookup"><span data-stu-id="72e98-126">Provide a **Hold code** info code.</span></span> <span data-ttu-id="72e98-127">قد تحتاج إلى إنشاء كود معلومات لهذا أولاً.</span><span class="sxs-lookup"><span data-stu-id="72e98-127">You may need to create an info code for this first.</span></span> <span data-ttu-id="72e98-128">يوفر كود المعلومات هذا مجموعه أكواد السبب الاختيارية التي ستتم مطالبة المستخدم بالاختيار من بينها عند وضع أمر قيد الانتظار.</span><span class="sxs-lookup"><span data-stu-id="72e98-128">This info code provides the set of optional reason codes that the user will be prompted to choose from when placing an order on hold.</span></span>
1. <span data-ttu-id="72e98-129">قدم كود معلومات **الائتمان**.</span><span class="sxs-lookup"><span data-stu-id="72e98-129">Provide a **Credit** info code.</span></span> <span data-ttu-id="72e98-130">قد تحتاج إلى إنشاء كود معلومات لهذا أولاً.</span><span class="sxs-lookup"><span data-stu-id="72e98-130">You may need to create an info code for this first.</span></span> <span data-ttu-id="72e98-131">يوفر كود المعلومات هذا مجموعة من أكواد السبب التي يمكن للمستخدم الاختيار من بينها عند استخدام وظيفة ائتمان بالأمر الخاصة بمركز الاتصال لمنج مبالغ مستردة متنوعة للعميل لأسباب تتعلق بخدمه العملاء.</span><span class="sxs-lookup"><span data-stu-id="72e98-131">This info code provides the set of reason codes that the user can choose from when using the order credit functionality of call center to give misc refunds to the customer for customer service reasons.</span></span>
1. <span data-ttu-id="72e98-132">اختياري: إعداد الأبعاد المالية على علامة التبويب السريعة **الأبعاد المالية**.</span><span class="sxs-lookup"><span data-stu-id="72e98-132">Optional: set up financial dimensions on the **Financial dimensions** FastTab.</span></span> <span data-ttu-id="72e98-133">ستكون الأبعاد التي يتم إدخالها هنا الأبعاد الافتراضية عل أي أمر مبيعات يتم إنشاؤه في قناة الاتصال هذه.</span><span class="sxs-lookup"><span data-stu-id="72e98-133">The dimensions entered here will default on any sales order created in this call center channel.</span></span>
1. <span data-ttu-id="72e98-134">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="72e98-134">Click **Save**.</span></span>

<span data-ttu-id="72e98-135">توضح الصورة التالية إنشاء قناة مركز اتصال جديدة.</span><span class="sxs-lookup"><span data-stu-id="72e98-135">The following image shows the creation of a new call center channel.</span></span>

![قناة مركز اتصال جديدة](media/channel-setup-callcenter-1.png)

<span data-ttu-id="72e98-137">تعرض الصورة التالية مثالاً لقناة مركز اتصال.</span><span class="sxs-lookup"><span data-stu-id="72e98-137">The following image shows an example call center channel.</span></span>

![مثال قناة مركز اتصال](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a><span data-ttu-id="72e98-139">إعداد إضافي للقناة</span><span class="sxs-lookup"><span data-stu-id="72e98-139">Additional channel setup</span></span>

<span data-ttu-id="72e98-140">تتضمن المهام الإضافية المطلوبة لإعداد قناة مركز الاتصال إعداد طرق الدفع وأوضاع التسليم.</span><span class="sxs-lookup"><span data-stu-id="72e98-140">Additional tasks required for call center channel setup include setting up payment methods and modes of delivery.</span></span>

<span data-ttu-id="72e98-141">تُظهر الصورة التالية خيارات إعداد **أوضاع التسليم** و **طرق الدفع** على علامة تبويب **الإعداد**.</span><span class="sxs-lookup"><span data-stu-id="72e98-141">The following image shows **Modes of delivery** and **Payment methods** setup options on the **Set up** tab.</span></span>

![إجراءات إعداد إضافية لقناة مركز الاتصال](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="72e98-143">إعداد طرق الدفع</span><span class="sxs-lookup"><span data-stu-id="72e98-143">Set up payment methods</span></span>

<span data-ttu-id="72e98-144">لإعداد طرق الدفع، اتبع الخطوات التالية لكل نوع دفع معتمد على هذه القناة.</span><span class="sxs-lookup"><span data-stu-id="72e98-144">To set up payment methods, follow these steps for each payment type supported on this channel.</span></span> <span data-ttu-id="72e98-145">ستتم مطالبة المستخدمين بالتحديد من طرق الدفع المعرفة مسبقًا لربطها بقناة مركز الاتصال.</span><span class="sxs-lookup"><span data-stu-id="72e98-145">Users will be required to select from pre-defined payment methods to link them to the call center channel.</span></span> <span data-ttu-id="72e98-146">قبل إعداد طرق دفع مركز الاتصال، يجب أولاً إعداد طرق الدفع الرئيسية في **Retail and Commerce \> إعداد القناة \> طرق الدفع \> طرق الدفع**.</span><span class="sxs-lookup"><span data-stu-id="72e98-146">Before setting up your call center payment methods, first set up your master methods of payment in **Retail and Commerce \> Channel setup \> Payment methods \> Payment methods**.</span></span>

1. <span data-ttu-id="72e98-147">في جزء الإجراءات، حدد علامة التبويب **الإعداد** ، ثم حدد **طرق الدفع**.</span><span class="sxs-lookup"><span data-stu-id="72e98-147">On the action pane, select the **Set up** tab, and then select **Payment methods**.</span></span>
1. <span data-ttu-id="72e98-148">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="72e98-148">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="72e98-149">في جزء التنقل، حدد طريقة دفع من طرق الدفع المتوفرة المحددة مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="72e98-149">In the navigation pane, select a payment method from the pre-defined payments available.</span></span>
1. <span data-ttu-id="72e98-150">قم بتكوين أي إعدادات إضافية مطلوبة لنوع الدفع.</span><span class="sxs-lookup"><span data-stu-id="72e98-150">Configure any additional settings as required for the payment type.</span></span> <span data-ttu-id="72e98-151">بالنسبة إلى بطاقات الائتمان أو بطاقات الهدايا أو بطاقات الولاء، هناك حاجة إلى إعداد إضافي عن طريق تحديد وظيفة **إعداد البطاقة**.</span><span class="sxs-lookup"><span data-stu-id="72e98-151">For credit cards, gift cards, or loyalty cards, additional setup is required by selecting the **Card setup** function.</span></span> 
1. <span data-ttu-id="72e98-152">قم بتكوين حسابات الترحيل المناسبة لنوع الدفع في قسم **الترحيل**.</span><span class="sxs-lookup"><span data-stu-id="72e98-152">Configure proper posting accounts for the payment type in the **Posting** section.</span></span>
1. <span data-ttu-id="72e98-153">في جزء الإجراءات، انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="72e98-153">On the action pane, click **Save**.</span></span>

<span data-ttu-id="72e98-154">تعرض الصورة التالية مثالاً عن طريقة الدفع النقدي.</span><span class="sxs-lookup"><span data-stu-id="72e98-154">The following image shows an example of a cash payment method.</span></span>

![أمثلة عن طرق الدفع](media/channel-setup-callcenter-payments.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="72e98-156">إعداد أوضاع التسليم</span><span class="sxs-lookup"><span data-stu-id="72e98-156">Set up modes of delivery</span></span>

<span data-ttu-id="72e98-157">يمكنك الاطلاع على أوضاع التسليم التي تم تكوينها عن طريق تحديد **أوضاع التسليم** من علامة التبويب **الإعداد** على **جزء الإجراءات**.</span><span class="sxs-lookup"><span data-stu-id="72e98-157">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="72e98-158">لتغيير أو إضافة وضع تسليم لربطه بقناة مركز الاتصال، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="72e98-158">To change or add a mode of delivery to be associated to the call center channel, follow these steps.</span></span>

1. <span data-ttu-id="72e98-159">من نموذج أوضاع التسليم في مركز الاتصال، حدد **إدارة أوضاع التسليم**</span><span class="sxs-lookup"><span data-stu-id="72e98-159">From the Call center modes of delivery form, select **Manage modes of delivery**</span></span>
1. <span data-ttu-id="72e98-160">في جزء الإجراءات، حدد **جديد** لإنشاء وضع تسليم جديد، أو حدد وضعًا موجودًا.</span><span class="sxs-lookup"><span data-stu-id="72e98-160">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="72e98-161">في قسم **قنوات البيع بالتجزئة** ، انقر فوق **إضافة بند** لإضافة قناة مركز الاتصال.</span><span class="sxs-lookup"><span data-stu-id="72e98-161">In the **Retail channels** section, click **Add line** to add the call center channel.</span></span> <span data-ttu-id="72e98-162">تؤدي إضافة قنوات باستخدام عقد المؤسسة بدلاً من إضافة كل قناة بشكل فردي إلى تنظيم عملية إضافة القنوات.</span><span class="sxs-lookup"><span data-stu-id="72e98-162">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>
1. <span data-ttu-id="72e98-163">تأكد من تكوين وضع التسليم بواسطة البيانات الموجودة على علامة التبويب السريعة **لمنتجات** وعلامة التبويب السريعة **العناوين**.</span><span class="sxs-lookup"><span data-stu-id="72e98-163">Ensure the mode of delivery has been configured with data on the **Products** FastTab and the **Addresses** FastTab.</span></span> <span data-ttu-id="72e98-164">في حال عدم وجود أي منتجات أو عناوين تسليم صالحة لوضع التسليم، سيؤدي اختيارها اثناء إدخال الأمر إلى حدوث أخطاء.</span><span class="sxs-lookup"><span data-stu-id="72e98-164">If no products or delivery addresses are valid for the mode of delivery, choosing it during order entry will result in errors.</span></span>
1. <span data-ttu-id="72e98-165">بعد إدخال أي تغييرات على تكوين وضع التسليم في مركز الاتصال، يجب تشغيل وظيفة **معالجة أوضاع التسليم** لتحديد مصفوفة التغيير.</span><span class="sxs-lookup"><span data-stu-id="72e98-165">After any changes have been made to the call center mode of delivery configurations, the **Process delivery modes** job must be run to explode the change matrix.</span></span> <span data-ttu-id="72e98-166">يمكن العثور على هذه الوظيفة بالانتقال إلى **Retail and Commerce \> تكنولوجيا معلومات Retail and Commerce \> معالجة أوضاع التسليم**.</span><span class="sxs-lookup"><span data-stu-id="72e98-166">This job can be found by navigating to **Retail and Commerce \> Retail and Commerce IT \> Process delivery modes**.</span></span>

<span data-ttu-id="72e98-167">تعرض الصورة التالية مثالاً لوضع التسليم.</span><span class="sxs-lookup"><span data-stu-id="72e98-167">The following image shows an example of a mode of delivery.</span></span>

![إعداد أوضاع التسليم](media/channel-setup-retail-7.png)

### <a name="set-up-channel-users"></a><span data-ttu-id="72e98-169">إعداد مستخدمي القناة</span><span class="sxs-lookup"><span data-stu-id="72e98-169">Set up channel users</span></span>

<span data-ttu-id="72e98-170">لإنشاء أمر مبيعات مرتبط بقناة مركز الاتصال من Commerce Headquarters، يجب أن يكون المستخدم الذي يقوم بإنشاء أمر المبيعات مرتبطًا بقناة مركز الاتصال.</span><span class="sxs-lookup"><span data-stu-id="72e98-170">To create a sales order that is linked to the call center channel from Commerce Headquarters, the user creating the sales order must be linked to the call center channel.</span></span> <span data-ttu-id="72e98-171">يتعذر على المستخدم ربط أمر المبيعات المنشأ في Commerce Headquarters بقناة مركز الاتصال يدويًا.</span><span class="sxs-lookup"><span data-stu-id="72e98-171">The user cannot manually link a sales order created in Commerce Headquarters to the call center channel.</span></span> <span data-ttu-id="72e98-172">هذا الارتباط منهجي، ويستند إلى علاقة المستخدم بقناة مركز الاتصال.</span><span class="sxs-lookup"><span data-stu-id="72e98-172">The link is systematic, and is based on the user and the user's relationship to the call center channel.</span></span> <span data-ttu-id="72e98-173">يمكن ربط المستخدم بقناة مركز اتصال واحدة فقط.</span><span class="sxs-lookup"><span data-stu-id="72e98-173">A user may only be linked to one call center channel.</span></span>

1. <span data-ttu-id="72e98-174">في جزء الإجراءات، حدد علامة التبويب **القناة** ، ثم حدد **مستخدمو القناة**.</span><span class="sxs-lookup"><span data-stu-id="72e98-174">On the action pane, select the **Channel** tab, and then select **Channel users**.</span></span>
1. <span data-ttu-id="72e98-175">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="72e98-175">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="72e98-176">اختر **معرف مستخدم** موجودًا من قائمة التحديد المنسدلة لربط هذا المستخدم بقناة مركز الاتصال</span><span class="sxs-lookup"><span data-stu-id="72e98-176">Choose an existing **User ID** from the dropdown selection list to link this user to the call center channel</span></span>

<span data-ttu-id="72e98-177">بعد إعداد مستخدم القناة وقيام المستخدم بإنشاء أمر مبيعات جديد في Commerce Headquarters، سيتم ربط أمر المبيعات بقناة مركز الاتصال المرتبطة به.</span><span class="sxs-lookup"><span data-stu-id="72e98-177">After the channel user setup is done and the user creates a new sales order in Commerce Headquarters, the sales order will be linked to their associated call center channel.</span></span> <span data-ttu-id="72e98-178">سيتم تطبيق أي تكوينات لهذه القناة بشكل منهجي على أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="72e98-178">Any configurations for this channel will be applied systematically to the sales order.</span></span> <span data-ttu-id="72e98-179">بإمكان المستخدم تأكيد قناة مركز الاتصال التي يرتبط بها أمر المبيعات من خلال عرض الاسم المرجعي للقناة على رأس أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="72e98-179">A user can confirm which call center channel the sales order is linked to by viewing the channel name reference on the sales order header.</span></span>


### <a name="set-up-price-groups"></a><span data-ttu-id="72e98-180">إعداد مجموعات الأسعار</span><span class="sxs-lookup"><span data-stu-id="72e98-180">Set up price groups</span></span>

<span data-ttu-id="72e98-181">تعتبر مجموعات الأسعار اختيارية، ولكن باستطاعتها، إذا تم استخدامها، التحكم في أسعار المبيعات التي سيتم تقديمها للعملاء عند وضعهم الأوامر في قناة مركز الاتصال.</span><span class="sxs-lookup"><span data-stu-id="72e98-181">Price groups are optional, but if used, can control which sales prices will be offered to customers placing orders in the call center channel.</span></span> <span data-ttu-id="72e98-182">إذا لم يتم تكوين مجموعة أسعار للعميل، أو إذا لم يتم تطبق مجموعات أسعار الكتالوج على أمر المبيعات (باستخدام حقل **معرف كود المصدر** على رأس أمر المبيعات في مركز الاتصال)، فسيتم عندئذٍ استخدام مجموعه أسعار القناة لتحديد أسعار الأصناف.</span><span class="sxs-lookup"><span data-stu-id="72e98-182">If a price group has not been configured for the customer, or if catalog price groups are not being applied to the sales order (using the **Source code ID** field on the call center order header), then the channel price group is used to locate item prices.</span></span> <span data-ttu-id="72e98-183">في حال عدم العثور على مجموعة أسعار في قناة مركز الاتصال، يتم استخدام الأسعار الرئيسية الافتراضية للأصناف.</span><span class="sxs-lookup"><span data-stu-id="72e98-183">If a price group is not found on the call center channel, the default item master prices are used.</span></span> 

<span data-ttu-id="72e98-184">لإعداد مجموعة أسعار، قم بما يلي.</span><span class="sxs-lookup"><span data-stu-id="72e98-184">To set up a price group, do the following.</span></span>

1. <span data-ttu-id="72e98-185">في جزء الإجراءات، انقر فوق علامة التبويب **القناة** ، ثم حدد **مجموعات الأسعار**.</span><span class="sxs-lookup"><span data-stu-id="72e98-185">On the action pane, click the **Channel** tab, and then select **Price groups**.</span></span>
1. <span data-ttu-id="72e98-186">انقر فوق **جديد** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="72e98-186">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="72e98-187">حدد **مجموعة أسعار البيع بالتجزئة‬** من قائمة التحديد المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="72e98-187">Select a **Retail price group** from the dropdown selection list.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="72e98-188">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="72e98-188">Additional resources</span></span>

[<span data-ttu-id="72e98-189">المتطلبات الأساسية لإعداد القناة</span><span class="sxs-lookup"><span data-stu-id="72e98-189">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="72e98-190">وظيفة مبيعات مركز الاتصال</span><span class="sxs-lookup"><span data-stu-id="72e98-190">Call center sales functionality</span></span>](call-center-functionality.md)

[<span data-ttu-id="72e98-191">إعداد خيارات معالجة أوامر مركز الاتصال</span><span class="sxs-lookup"><span data-stu-id="72e98-191">Set up call center order processing options</span></span>](set-up-order-processing-options.md)

[<span data-ttu-id="72e98-192">كتالوجات مركز الاتصال</span><span class="sxs-lookup"><span data-stu-id="72e98-192">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="72e98-193">إعداد تنبيهات الاحتيال والعمل باستخدامها</span><span class="sxs-lookup"><span data-stu-id="72e98-193">Set up and work with fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="72e98-194">إعداد برامج الاستمرارية لمراكز الاتصال</span><span class="sxs-lookup"><span data-stu-id="72e98-194">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)
