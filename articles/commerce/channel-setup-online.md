---
title: إعداد قناة عبر الإنترنت
description: يوضح هذا الموضوع كيفية إنشاء قناة جديدة عبر الإنترنت في Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 07/02/2020
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
ms.openlocfilehash: 07225d97af76ea665fa28362cc205c6e8dc4fdf4
ms.sourcegitcommit: 4c6d31f3ebd88212d3d1497a4bba9c64c5300444
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/24/2020
ms.locfileid: "4410043"
---
# <a name="set-up-an-online-channel"></a><span data-ttu-id="bee0c-103">إعداد قناة عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="bee0c-103">Set up an online channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="bee0c-104">يوضح هذا الموضوع كيفية إنشاء قناة جديدة عبر الإنترنت في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="bee0c-104">This topic describes how to create a new online channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="bee0c-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="bee0c-105">Overview</span></span>

<span data-ttu-id="bee0c-106">يدعم Dynamics 365 Commerce عدة قنوات بيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="bee0c-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="bee0c-107">وتتضمن قنوات البيع بالتجزئة هذه المتاجر على إنترنت، ومراكز الاتصال، ومتاجر البيع بالتجزئة (تعرف أيضًا بالمتاجر التقليدية).</span><span class="sxs-lookup"><span data-stu-id="bee0c-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="bee0c-108">تمنح المتاجر على الإنترنت للعملاء خيار شراء المنتجات من متجر عبر الإنترنت تابع لبائع التجزئة عبر الإنترنت بالإضافة إلى متاجره للبيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="bee0c-108">Online stores give customers the option of purchasing products from the retailer's online store in addition to its retail stores.</span></span>

<span data-ttu-id="bee0c-109">لإنشاء متجر عبر الإنترنت في Commerce، يجب أولاً إنشاء قناة عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="bee0c-109">To create an online store in Commerce, you must first create an online channel.</span></span> <span data-ttu-id="bee0c-110">قبل إنشاء قناة جديدة عبر الإنترنت، تأكد من إكمال [المتطلبات الأساسية لإعداد قناة](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="bee0c-110">Before you create a new online channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

<span data-ttu-id="bee0c-111">قبل أن تتمكن من إنشاء موقع جديد، يجب إنشاء متجر واحد على الأقل على الإنترنت في التجارة.</span><span class="sxs-lookup"><span data-stu-id="bee0c-111">Before you can create a new site, at least one online store must be created in Commerce.</span></span> <span data-ttu-id="bee0c-112">لمزيد من المعلومات، راجع [إنشاء موقع تجارة إلكترونية](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="bee0c-112">For more information, see [Create an e-Commerce site](create-ecommerce-site.md).</span></span>

## <a name="create-and-configure-a-new-online-channel"></a><span data-ttu-id="bee0c-113">إنشاء قناة جديدة عبر الإنترنت وتكوينها</span><span class="sxs-lookup"><span data-stu-id="bee0c-113">Create and configure a new online channel</span></span>

<span data-ttu-id="bee0c-114">لإنشاء قناة جديدة عبر الإنترنت وتكوينها، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="bee0c-114">To create and configure a new online channel, follow these steps.</span></span>

1. <span data-ttu-id="bee0c-115">في جزء التنقل، انتقل إلى **الوحدات \> القنوات \> المتاجر عبر الإنترنت**.</span><span class="sxs-lookup"><span data-stu-id="bee0c-115">In the navigation pane, go to **Modules \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="bee0c-116">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="bee0c-116">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="bee0c-117">في حقل **الاسم** أدخل اسمًا للقناة الجديدة.</span><span class="sxs-lookup"><span data-stu-id="bee0c-117">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="bee0c-118">في القائمة المنسدلة **الكيان القانوني**، أدخل الكيان القانوني المناسب.</span><span class="sxs-lookup"><span data-stu-id="bee0c-118">In the **Legal entity** drop-down, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="bee0c-119">في القائمة‏‎ المنسدلة **المستودع**، أدخل المستودع المناسب.</span><span class="sxs-lookup"><span data-stu-id="bee0c-119">In the **Warehouse** drop-down, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="bee0c-120">في الحقل **المنطقة الزمنية للمتجر**، حدد المنطقة الزمنية المناسبة.</span><span class="sxs-lookup"><span data-stu-id="bee0c-120">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="bee0c-121">في حقل **العملة**، حدد العملة المناسبة.</span><span class="sxs-lookup"><span data-stu-id="bee0c-121">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="bee0c-122">في حقل **العميل الافتراضي**، أدخل عميل افتراضي صالح.</span><span class="sxs-lookup"><span data-stu-id="bee0c-122">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="bee0c-123">في حقل **دفتر عناوين العميل‬**، أدخل دفتر عناوين صالحًا.</span><span class="sxs-lookup"><span data-stu-id="bee0c-123">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="bee0c-124">في الحقل **ملف تعريف الوظائف**، حدد ملف تعريف الوظائف، إن أمكن.</span><span class="sxs-lookup"><span data-stu-id="bee0c-124">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="bee0c-125">في الحقل **ملف تعريف الإخطار بالبريد الإلكتروني**، أدخل ملف تعريف إخطار بالبريد الإلكتروني صالحًا.</span><span class="sxs-lookup"><span data-stu-id="bee0c-125">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="bee0c-126">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="bee0c-126">On the action pane, select **Save**.</span></span>

<span data-ttu-id="bee0c-127">توضح الصورة التالية إنشاء جديدة عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="bee0c-127">The following image shows the creation of a new online channel.</span></span>

![قناة جديدة عبر الإنترنت](media/channel-setup-online-1.png)

<span data-ttu-id="bee0c-129">تعرض الصورة التالية مثالاً لقناة عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="bee0c-129">The following image shows an example online channel.</span></span>

![مثال لقناة عبر الإنترنت](media/channel-setup-online-2.png)

## <a name="set-up-languages"></a><span data-ttu-id="bee0c-131">إعداد اللغات</span><span class="sxs-lookup"><span data-stu-id="bee0c-131">Set up languages</span></span>

<span data-ttu-id="bee0c-132">إذا كان موقع التجارة الإلكترونية سيعتمد لغات متعددة، فعليك توسيع قسم **اللغات** وإضافة المزيد من اللغات حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="bee0c-132">If your e-Commerce site will support multiple languages, expand the **Languages** section and add additional languages as needed.</span></span>

## <a name="set-up-payment-account"></a><span data-ttu-id="bee0c-133">إعداد حساب الدفع</span><span class="sxs-lookup"><span data-stu-id="bee0c-133">Set up payment account</span></span>

<span data-ttu-id="bee0c-134">من خلال القسم **حساب الدعم**، يمكنك إضافة موفر دفع خارجي.</span><span class="sxs-lookup"><span data-stu-id="bee0c-134">From within the **Payment account** section, you can add a third-party payment provider.</span></span> <span data-ttu-id="bee0c-135">للحصول على معلومات حول إعداد موصل الدفع Adyen، راجع [موصل دفع Dynamics 365 لـ Adyen‬](../retail/dev-itpro/adyen-connector.md).</span><span class="sxs-lookup"><span data-stu-id="bee0c-135">For information on setting up an Adyen payment connector, see [Dynamics 365 Payment Connector for Adyen](../retail/dev-itpro/adyen-connector.md).</span></span>

## <a name="additional-channel-setup"></a><span data-ttu-id="bee0c-136">إعداد إضافي للقناة</span><span class="sxs-lookup"><span data-stu-id="bee0c-136">Additional channel setup</span></span>

<span data-ttu-id="bee0c-137">تتضمن المهام الإضافية المطلوبة لإعداد قناة عبر الإنترنت إعداد طرق الدفع وأوضاع التسليم وتعيين مجموعة التنفيذ‬.</span><span class="sxs-lookup"><span data-stu-id="bee0c-137">Additional tasks that are required for online channel setup include setting up payment methods, modes of delivery, and the fulfillment group assignment.</span></span>

<span data-ttu-id="bee0c-138">تُظهر الصورة التالية خيارات إعداد **أوضاع التسليم** و **طرق الدفع** و **تعيين مجموعة التنفيذ** على علامة تبويب **الإعداد‏‎**.</span><span class="sxs-lookup"><span data-stu-id="bee0c-138">The following image shows **Modes of delivery**, **Payment methods**, and **Fulfillment group assignment** setup options on the **Set up** tab.</span></span>

![إجراءات إعداد إضافية لقناة عبر الإنترنت](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="bee0c-140">إعداد طرق الدفع</span><span class="sxs-lookup"><span data-stu-id="bee0c-140">Set up payment methods</span></span>

<span data-ttu-id="bee0c-141">لإعداد طرق الدفع، لكل نوع دفع معتمد على هذه القناة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="bee0c-141">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="bee0c-142">في جزء الإجراءات، حدد علامة التبويب **الإعداد**، ثم حدد **طرق الدفع**.</span><span class="sxs-lookup"><span data-stu-id="bee0c-142">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="bee0c-143">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="bee0c-143">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="bee0c-144">في جزء التنقل، حدد طريقة الدفع المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="bee0c-144">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="bee0c-145">في القسم **عام**، أدخل **اسم العملية**، وقم بتكوين أي إعدادات أخرى مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="bee0c-145">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="bee0c-146">قم بتكوين أي إعدادات إضافية مطلوبة لنوع الدفع.</span><span class="sxs-lookup"><span data-stu-id="bee0c-146">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="bee0c-147">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="bee0c-147">On the action pane, select **Save**.</span></span>

<span data-ttu-id="bee0c-148">تعرض الصورة التالية مثالاً عن طريقة الدفع النقدي.</span><span class="sxs-lookup"><span data-stu-id="bee0c-148">The following image shows an example of a cash payment method.</span></span>

![أمثلة عن طرق الدفع](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="bee0c-150">إعداد أوضاع التسليم</span><span class="sxs-lookup"><span data-stu-id="bee0c-150">Set up modes of delivery</span></span>

<span data-ttu-id="bee0c-151">يمكنك الاطلاع على أوضاع التسليم التي تم تكوينها عن طريق تحديد **أوضاع التسليم** من علامة التبويب **الإعداد** على **جزء الإجراءات**.</span><span class="sxs-lookup"><span data-stu-id="bee0c-151">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="bee0c-152">لتغيير وضع التسليم أو إضافته، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="bee0c-152">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="bee0c-153">في جزء التنقل، انتقل إلى **الوحدات \> إدارة المخزون \> أوضاع التسليم**.</span><span class="sxs-lookup"><span data-stu-id="bee0c-153">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="bee0c-154">في جزء الإجراءات، حدد **جديد** لإنشاء وضع تسليم جديد، أو حدد وضعًا موجودًا.</span><span class="sxs-lookup"><span data-stu-id="bee0c-154">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="bee0c-155">في قسم **قنوات البيع بالتجزئة**، حدد **إضافة بند** لإضافة القناة.</span><span class="sxs-lookup"><span data-stu-id="bee0c-155">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="bee0c-156">تؤدي إضافة قنوات باستخدام عقد المؤسسة بدلاً من إضافة كل قناة بشكل فردي إلى تنظيم عملية إضافة القنوات.</span><span class="sxs-lookup"><span data-stu-id="bee0c-156">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="bee0c-157">تعرض الصورة التالية مثالاً لوضع التسليم.</span><span class="sxs-lookup"><span data-stu-id="bee0c-157">The following image shows an example of a mode of delivery.</span></span>

![إعداد أوضاع التسليم](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="bee0c-159">إعداد تعيين مجموعة تنفيذ</span><span class="sxs-lookup"><span data-stu-id="bee0c-159">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="bee0c-160">لإعداد تعيين مجموعة تنفيذ، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="bee0c-160">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="bee0c-161">في جزء الإجراءات، حدد علامة التبويب **الإعداد**، ثم حدد **تعيين مجموعة تنفيذ**.</span><span class="sxs-lookup"><span data-stu-id="bee0c-161">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="bee0c-162">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="bee0c-162">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="bee0c-163">في القائمة المنسدلة **مجموعة التنفيذ‬**، حدد مجموعة تنفيذ.</span><span class="sxs-lookup"><span data-stu-id="bee0c-163">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="bee0c-164">في القائمة المنسدلة **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="bee0c-164">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="bee0c-165">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="bee0c-165">On the action pane, select **Save**.</span></span>

<span data-ttu-id="bee0c-166">تعرض الصورة التالية مثالاً لإعداد تعيين مجموعة تنفيذ.</span><span class="sxs-lookup"><span data-stu-id="bee0c-166">The following image shows an example of a fulfillment group assignment setup.</span></span>

![إعداد تعيين مجموعة تنفيذ](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a><span data-ttu-id="bee0c-168">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="bee0c-168">Additional resources</span></span>

[<span data-ttu-id="bee0c-169">نظرة عامة على القنوات</span><span class="sxs-lookup"><span data-stu-id="bee0c-169">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="bee0c-170">المتطلبات الأساسية‬ لإعداد قناة</span><span class="sxs-lookup"><span data-stu-id="bee0c-170">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="bee0c-171">إعداد قناة بيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="bee0c-171">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="bee0c-172">إعداد قناة مركز اتصال</span><span class="sxs-lookup"><span data-stu-id="bee0c-172">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="bee0c-173">موصل دفع Dynamics 365 لـ Adyen</span><span class="sxs-lookup"><span data-stu-id="bee0c-173">Dynamics 365 Payment Connector for Adyen</span></span>](../retail/dev-itpro/adyen-connector.md)
