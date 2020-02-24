---
title: إعداد قناة عبر الإنترنت
description: يوضح هذا الموضوع كيفية إنشاء قناة جديدة عبر الإنترنت في Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 9b7a2b8fd157df8b39e9e227d188a3802cacb4e3
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002417"
---
# <a name="set-up-an-online-channel"></a><span data-ttu-id="d2241-103">إعداد قناة عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="d2241-103">Set up an online channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d2241-104">يوضح هذا الموضوع كيفية إنشاء قناة جديدة عبر الإنترنت في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d2241-104">This topic describes how to create a new online channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d2241-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="d2241-105">Overview</span></span>

<span data-ttu-id="d2241-106">يدعم Dynamics 365 Commerce عدة قنوات بيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="d2241-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="d2241-107">وتتضمن قنوات البيع بالتجزئة هذه المتاجر على إنترنت، ومراكز الاتصال، ومتاجر البيع بالتجزئة (تعرف أيضًا بالمتاجر التقليدية).</span><span class="sxs-lookup"><span data-stu-id="d2241-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="d2241-108">تمنح المتاجر على الإنترنت للعملاء خيار شراء المنتجات من متجر عبر الإنترنت تابع لبائع التجزئة عبر الإنترنت بالإضافة إلى متاجره للبيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="d2241-108">Online stores give customers the option of purchasing products from the retailer's online store in addition to its retail stores.</span></span>

<span data-ttu-id="d2241-109">لإنشاء متجر عبر الإنترنت في Commerce، يجب أولاً إنشاء قناة عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="d2241-109">To create an online store in Commerce, you must first create an online channel.</span></span> 

<span data-ttu-id="d2241-110">قبل إنشاء قناة جديدة عبر الإنترنت، تأكد من إكمال [المتطلبات الأساسية لإعداد قناة](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="d2241-110">Before you create a new online channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-online-channel"></a><span data-ttu-id="d2241-111">إنشاء قناة جديدة عبر الإنترنت وتكوينها</span><span class="sxs-lookup"><span data-stu-id="d2241-111">Create and configure a new online channel</span></span>

<span data-ttu-id="d2241-112">لإنشاء قناة جديدة عبر الإنترنت وتكوينها، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="d2241-112">To create and configure a new online channel, follow these steps.</span></span>

1. <span data-ttu-id="d2241-113">في جزء التنقل، انتقل إلى **الوحدات \> القنوات \> المتاجر عبر الإنترنت**.</span><span class="sxs-lookup"><span data-stu-id="d2241-113">In the navigation pane, go to **Modules \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="d2241-114">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="d2241-114">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d2241-115">في حقل **الاسم** أدخل اسمًا للقناة الجديدة.</span><span class="sxs-lookup"><span data-stu-id="d2241-115">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="d2241-116">في القائمة المنسدلة **الكيان القانوني**، أدخل الكيان القانوني المناسب.</span><span class="sxs-lookup"><span data-stu-id="d2241-116">In the **Legal entity** drop-down, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="d2241-117">في القائمة‏‎ المنسدلة **المستودع**، أدخل المستودع المناسب.</span><span class="sxs-lookup"><span data-stu-id="d2241-117">In the **Warehouse** drop-down, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="d2241-118">في الحقل **المنطقة الزمنية للمتجر**، حدد المنطقة الزمنية المناسبة.</span><span class="sxs-lookup"><span data-stu-id="d2241-118">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="d2241-119">في حقل **العملة**، حدد العملة المناسبة.</span><span class="sxs-lookup"><span data-stu-id="d2241-119">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="d2241-120">في حقل **العميل الافتراضي**، أدخل عميل افتراضي صالح.</span><span class="sxs-lookup"><span data-stu-id="d2241-120">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="d2241-121">في حقل **دفتر عناوين العميل‬**، أدخل دفتر عناوين صالحًا.</span><span class="sxs-lookup"><span data-stu-id="d2241-121">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="d2241-122">في الحقل **ملف تعريف الوظائف**، حدد ملف تعريف الوظائف، إن أمكن.</span><span class="sxs-lookup"><span data-stu-id="d2241-122">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="d2241-123">في الحقل **ملف تعريف الإخطار بالبريد الإلكتروني**، أدخل ملف تعريف إخطار بالبريد الإلكتروني صالحًا.</span><span class="sxs-lookup"><span data-stu-id="d2241-123">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="d2241-124">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="d2241-124">On the action pane, select **Save**.</span></span>

<span data-ttu-id="d2241-125">توضح الصورة التالية إنشاء جديدة عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="d2241-125">The following image shows the creation of a new online channel.</span></span>

![قناة جديدة عبر الإنترنت](media/channel-setup-online-1.png)

<span data-ttu-id="d2241-127">تعرض الصورة التالية مثالاً لقناة عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="d2241-127">The following image shows an example online channel.</span></span>

![مثال لقناة عبر الإنترنت](media/channel-setup-online-2.png)

## <a name="set-up-languages"></a><span data-ttu-id="d2241-129">إعداد اللغات</span><span class="sxs-lookup"><span data-stu-id="d2241-129">Set up languages</span></span>

<span data-ttu-id="d2241-130">إذا كان موقع التجارة الإلكترونية سيعتمد لغات متعددة، فعليك توسيع قسم **اللغات** وإضافة المزيد من اللغات حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="d2241-130">If your e-Commerce site will support multiple languages, expand the **Languages** section and add additional languages as needed.</span></span>

## <a name="set-up-payment-account"></a><span data-ttu-id="d2241-131">إعداد حساب الدفع</span><span class="sxs-lookup"><span data-stu-id="d2241-131">Set up payment account</span></span>

<span data-ttu-id="d2241-132">من خلال القسم **حساب الدعم**، يمكنك إضافة موفر دفع خارجي.</span><span class="sxs-lookup"><span data-stu-id="d2241-132">From within the **Payment account** section, you can add a third-party payment provider.</span></span> <span data-ttu-id="d2241-133">للحصول على معلومات حول إعداد موصل الدفع Adyen، راجع [موصل دفع Dynamics 365 لـ Adyen‬](../retail/dev-itpro/adyen-connector.md).</span><span class="sxs-lookup"><span data-stu-id="d2241-133">For information on settting up an Adyen payment connector, see [Dynamics 365 Payment Connector for Adyen](../retail/dev-itpro/adyen-connector.md).</span></span>

## <a name="additional-channel-set-up"></a><span data-ttu-id="d2241-134">إعداد إضافي للقناة</span><span class="sxs-lookup"><span data-stu-id="d2241-134">Additional channel set up</span></span>

<span data-ttu-id="d2241-135">تتضمن المهام الإضافية المطلوبة لإعداد قناة عبر الإنترنت إعداد طرق الدفع وأوضاع التسليم وتعيين مجموعة التنفيذ‬.</span><span class="sxs-lookup"><span data-stu-id="d2241-135">Additional tasks required for online channel setup include setting up payment methods, modes of delivery, and the fulfillment group assignment.</span></span>

<span data-ttu-id="d2241-136">تُظهر الصورة التالية خيارات إعداد **أوضاع التسليم** و**طرق الدفع** و**تعيين مجموعة التنفيذ** على علامة تبويب **الإعداد‏‎**.</span><span class="sxs-lookup"><span data-stu-id="d2241-136">The following image shows **Modes of delivery**, **Payment methods**, and **Fulfillment group assignment** setup options on the **Set up** tab.</span></span>

![إجراءات إعداد إضافية لقناة عبر الإنترنت](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="d2241-138">إعداد طرق الدفع</span><span class="sxs-lookup"><span data-stu-id="d2241-138">Set up payment methods</span></span>

<span data-ttu-id="d2241-139">لإعداد طرق الدفع، لكل نوع دفع معتمد على هذه القناة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="d2241-139">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="d2241-140">في جزء الإجراءات، حدد علامة التبويب **الإعداد**، ثم حدد **طرق الدفع**.</span><span class="sxs-lookup"><span data-stu-id="d2241-140">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="d2241-141">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="d2241-141">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d2241-142">في جزء التنقل، حدد طريقة الدفع المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="d2241-142">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="d2241-143">في القسم **عام**، أدخل **اسم العملية**، وقم بتكوين أي إعدادات أخرى مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="d2241-143">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="d2241-144">قم بتكوين أي إعدادات إضافية مطلوبة لنوع الدفع.</span><span class="sxs-lookup"><span data-stu-id="d2241-144">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="d2241-145">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="d2241-145">On the action pane, select **Save**.</span></span>

<span data-ttu-id="d2241-146">تعرض الصورة التالية مثالاً عن طريقة الدفع النقدي.</span><span class="sxs-lookup"><span data-stu-id="d2241-146">The following image shows an example of a cash payment method.</span></span>

![أمثلة عن طرق الدفع](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="d2241-148">إعداد أوضاع التسليم</span><span class="sxs-lookup"><span data-stu-id="d2241-148">Set up modes of delivery</span></span>

<span data-ttu-id="d2241-149">يمكنك الاطلاع على أوضاع التسليم التي تم تكوينها عن طريق تحديد **أوضاع التسليم** من علامة التبويب **الإعداد** على **جزء الإجراءات**.</span><span class="sxs-lookup"><span data-stu-id="d2241-149">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="d2241-150">لتغيير وضع التسليم أو إضافته، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="d2241-150">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="d2241-151">في جزء التنقل، انتقل إلى **الوحدات \> إدارة المخزون \> أوضاع التسليم**.</span><span class="sxs-lookup"><span data-stu-id="d2241-151">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="d2241-152">في جزء الإجراءات، حدد **جديد** لإنشاء وضع تسليم جديد، أو حدد وضعًا موجودًا.</span><span class="sxs-lookup"><span data-stu-id="d2241-152">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="d2241-153">في قسم **قنوات البيع بالتجزئة**، حدد **إضافة بند** لإضافة القناة.</span><span class="sxs-lookup"><span data-stu-id="d2241-153">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="d2241-154">تؤدي إضافة قنوات باستخدام عقد المؤسسة بدلاً من إضافة كل قناة بشكل فردي إلى تنظيم عملية إضافة القنوات.</span><span class="sxs-lookup"><span data-stu-id="d2241-154">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="d2241-155">تعرض الصورة التالية مثالاً لوضع التسليم.</span><span class="sxs-lookup"><span data-stu-id="d2241-155">The following image shows an example of a mode of delivery.</span></span>

![إعداد أوضاع التسليم](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="d2241-157">إعداد تعيين مجموعة تنفيذ</span><span class="sxs-lookup"><span data-stu-id="d2241-157">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="d2241-158">لإعداد تعيين مجموعة تنفيذ، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="d2241-158">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="d2241-159">في جزء الإجراءات، حدد علامة التبويب **الإعداد**، ثم حدد **تعيين مجموعة تنفيذ**.</span><span class="sxs-lookup"><span data-stu-id="d2241-159">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="d2241-160">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="d2241-160">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d2241-161">في القائمة المنسدلة **مجموعة التنفيذ‬**، حدد مجموعة تنفيذ.</span><span class="sxs-lookup"><span data-stu-id="d2241-161">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="d2241-162">في القائمة المنسدلة **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="d2241-162">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="d2241-163">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="d2241-163">On the action pane, select **Save**.</span></span>

<span data-ttu-id="d2241-164">تعرض الصورة التالية مثالاً لإعداد تعيين مجموعة تنفيذ.</span><span class="sxs-lookup"><span data-stu-id="d2241-164">The following image shows an example of a fulfillment group assignment setup.</span></span>

![إعداد تعيين مجموعة تنفيذ](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a><span data-ttu-id="d2241-166">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="d2241-166">Additional resources</span></span>

[<span data-ttu-id="d2241-167">نظرة عامة على القنوات</span><span class="sxs-lookup"><span data-stu-id="d2241-167">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="d2241-168">المتطلبات الأساسية‬ لإعداد قناة</span><span class="sxs-lookup"><span data-stu-id="d2241-168">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="d2241-169">إعداد قناة بيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="d2241-169">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="d2241-170">إعداد قناة مركز اتصال</span><span class="sxs-lookup"><span data-stu-id="d2241-170">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="d2241-171">موصل دفع Dynamics 365 لـ Adyen</span><span class="sxs-lookup"><span data-stu-id="d2241-171">Dynamics 365 Payment Connector for Adyen</span></span>](../retail/dev-itpro/adyen-connector.md)
