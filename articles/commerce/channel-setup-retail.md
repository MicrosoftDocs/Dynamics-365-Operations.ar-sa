---
title: إعداد قناة بيع بالتجزئة
description: يوضح هذا الموضوع كيفية إنشاء قناة بيع بالتجزئة جديدة في Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 8ac01f36912fa5e8a09bb4f324ef272cec737aa1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002371"
---
# <a name="set-up-a-retail-channel"></a><span data-ttu-id="9bbb9-103">إعداد قناة بيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="9bbb9-103">Set up a retail channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="9bbb9-104">يوضح هذا الموضوع كيفية إنشاء قناة بيع بالتجزئة جديدة في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-104">This topic describes how to create a new retail channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9bbb9-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="9bbb9-105">Overview</span></span>

<span data-ttu-id="9bbb9-106">يدعم Dynamics 365 Commerce عدة قنوات بيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="9bbb9-107">وتتضمن قنوات البيع بالتجزئة هذه المتاجر على إنترنت، ومراكز الاتصال، ومتاجر البيع بالتجزئة (تعرف أيضًا بالمتاجر التقليدية).</span><span class="sxs-lookup"><span data-stu-id="9bbb9-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="9bbb9-108">يمكن أن يكون لكل قناة متجر للبيع بالتجزئة طرق الدفع ومجموعات الأسعار وسجلات نقطة البيع (POS) وحسابات الإيرادات والمصروفات وفريق العمل الخاص بها.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-108">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="9bbb9-109">ويجب إعداد كل هذه العناصر قبل إمكانية إنشاء قناة لمتجر البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-109">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="9bbb9-110">قبل إنشاء قناة بيع بالتجزئة، تأكد من اتباع [المتطلبات الأساسية للقناة](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="9bbb9-110">Before a retail channel is created, ensure you follow the [channel prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-retail-channel"></a><span data-ttu-id="9bbb9-111">إنشاء قناة بيع بالتجزئة جديدة وتكوينها</span><span class="sxs-lookup"><span data-stu-id="9bbb9-111">Create and configure a new retail channel</span></span>

1. <span data-ttu-id="9bbb9-112">في جزء التنقل، انتقل إلى **الوحدات \> القنوات \> المتاجر‬\> جميع المتاجر‬**.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-112">In the navigation pane, go to **Modules \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="9bbb9-113">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="9bbb9-114">في حقل **الاسم** أدخل اسمًا للقناة الجديدة.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="9bbb9-115">في حقل **رقم المتجر**، أدخل رقمًا فريدُا للمتجر.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-115">In the **Store number** field, provide a unique store number.</span></span> <span data-ttu-id="9bbb9-116">بإمكان الرقم أن يكون أبجديًا رقميًا ويتكون من 10 احرف بحدٍ أقصى.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-116">The number can be alphanumeric with a maximum of 10 characters.</span></span>
1. <span data-ttu-id="9bbb9-117">في القائمة المنسدلة **الكيان القانوني**، أدخل الكيان القانوني المناسب.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-117">In the **Legal entity** drop-down list, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="9bbb9-118">في القائمة‏‎ المنسدلة **المستودع**، أدخل المستودع المناسب.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-118">In the **Warehouse** drop-down list, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="9bbb9-119">في الحقل **المنطقة الزمنية للمتجر**، حدد المنطقة الزمنية المناسبة.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-119">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="9bbb9-120">في القائمة المنسدلة **مجموعة ضريبة المبيعات‬**، حدد مجموعه ضريبة مبيعات مناسبة للمتجر.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-120">In the **Sales tax group** drop-down list, select an appropriate sales tax group for the store.</span></span>
1. <span data-ttu-id="9bbb9-121">في حقل **العملة**، حدد العملة المناسبة.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-121">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="9bbb9-122">في حقل **دفتر عناوين العميل‬**، أدخل دفتر عناوين صالحًا.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-122">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="9bbb9-123">في حقل **العميل الافتراضي**، أدخل عميل افتراضي صالح.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-123">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="9bbb9-124">في الحقل **ملف تعريف الوظائف**، حدد ملف تعريف الوظائف، إن أمكن.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-124">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="9bbb9-125">في الحقل **ملف تعريف الإخطار بالبريد الإلكتروني**، أدخل ملف تعريف إخطار بالبريد الإلكتروني صالحًا.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-125">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="9bbb9-126">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-126">On the action pane, select **Save**.</span></span>

<span data-ttu-id="9bbb9-127">توضح الصورة التالية إنشاء قناة بيع بالتجزئة جديدة.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-127">The following image shows the creation of a new retail channel.</span></span>

![قناة بيع بالتجزئة جديدة](media/channel-setup-retail-1.png)

<span data-ttu-id="9bbb9-129">تعرض الصورة التالية مثالاً لقناة بيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-129">The following image shows an example retail channel.</span></span>

![مثال قناة البيع بالتجزئة](media/channel-setup-retail-2.png)

## <a name="other-settings"></a><span data-ttu-id="9bbb9-131">إعدادات أخرى</span><span class="sxs-lookup"><span data-stu-id="9bbb9-131">Other settings</span></span>

<span data-ttu-id="9bbb9-132">هناك الكثير من الإعدادات الاختيارية الأخرى التي يمكنك تعيينها في القسمين **كشف الحساب/الإقفال‬** و**متنوع‬**، استنادًا إلى احتياجات متجر البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-132">There are numerous other optional settings that can be set in the **Statement/closing** and **Miscellaneous** sections, based on the needs of the retail store.</span></span>

<span data-ttu-id="9bbb9-133">بالإضافة إلى ذلك، راجع [تخطيطات الشاشة الخاصة بنقطة البيع (POS)](https://docs.microsoft.com/en-us/dynamics365/retail/pos-screen-layouts?toc=/dynamics365/commerce/toc.json) للحصول على معلومات حول إعداد تخطيط الشاشة الافتراضية في القسم **تخطيط الشاشة** والقسم [تكوين Retail Hardware Station وتثبيتها‬](https://docs.microsoft.com/en-us/dynamics365/retail/retail-hardware-station-configuration-installation) للحصول على معلومات الإعداد حول **محطات الأجهزة‬**.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-133">In addition, see [Screen layouts for the point of sale (POS)](https://docs.microsoft.com/en-us/dynamics365/retail/pos-screen-layouts?toc=/dynamics365/commerce/toc.json) for information on setting up the default screen layout in the **Screen layout** section and [Configure and install Retail hardware station](https://docs.microsoft.com/en-us/dynamics365/retail/retail-hardware-station-configuration-installation) for setup information about the **Hardware stations** section.</span></span>

<span data-ttu-id="9bbb9-134">تعرض الصورة التالية مثالاً لتكوبن إعداد قناة بيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-134">The following image shows an example retail channel setup configuration.</span></span>

![مثال عن تكوين قناة البيع بالتجزئة](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a><span data-ttu-id="9bbb9-136">إعداد إضافي للقناة</span><span class="sxs-lookup"><span data-stu-id="9bbb9-136">Additional channel set up</span></span>

<span data-ttu-id="9bbb9-137">هناك عناصر إضافية يجب إعدادها للقناة ويمكن العثور عليها في **جزء الإجراءات** تحت قسم **الإعداد**.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-137">There are additional items that need to be set up for a channel that can be found on the **Action pane** under the **Set up** section.</span></span>

<span data-ttu-id="9bbb9-138">تتضمن المهام الإضافية المطلوبة لإعداد القناة عبر الإنترنت إعداد طرق الدفع وإقرار النقدية وأوضاع التسليم وحساب الإيرادات/المصروفات والأقسام وتعيين مجموعه التنفيذ والخزائن‬.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-138">Additional tasks required for online channel setup include setting up payment methods, cash declaration, modes of delivery, income/expense account, sections, the fulfillment group assignment, and safes.</span></span>

<span data-ttu-id="9bbb9-139">تعرض الصورة التالية خيارات إضافية لإعداد قناة البيع بالتجزئة على علامة تبويب **الإعداد**.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-139">The following image shows various additional retail channel setup options on the **Set up** tab.</span></span>

![إعداد القناة](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="9bbb9-141">إعداد طرق الدفع</span><span class="sxs-lookup"><span data-stu-id="9bbb9-141">Set up payment methods</span></span>

<span data-ttu-id="9bbb9-142">لإعداد طرق الدفع، لكل نوع دفع معتمد على هذه القناة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-142">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="9bbb9-143">في جزء الإجراءات، حدد علامة التبويب **الإعداد**، ثم حدد **طرق الدفع**.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-143">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="9bbb9-144">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-144">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="9bbb9-145">في جزء التنقل، حدد طريقة الدفع المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-145">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="9bbb9-146">في القسم **عام**، أدخل **اسم العملية**، وقم بتكوين أي إعدادات أخرى مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-146">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="9bbb9-147">قم بتكوين أي إعدادات إضافية مطلوبة لنوع الدفع.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-147">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="9bbb9-148">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-148">On the action pane, select **Save**.</span></span>

<span data-ttu-id="9bbb9-149">تعرض الصورة التالية مثالاً عن طريقة الدفع النقدي.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-149">The following image shows an example of a cash payment method.</span></span>

![أمثلة عن طرق الدفع](media/channel-setup-retail-5.png)

### <a name="set-up-cash-declaration"></a><span data-ttu-id="9bbb9-151">إعداد إقرار النقدية</span><span class="sxs-lookup"><span data-stu-id="9bbb9-151">Set up cash declaration</span></span>

1. <span data-ttu-id="9bbb9-152">في جزء الإجراءات، حدد علامة التبويب **الإعداد**، ثم حدد **إقرار النقدية**.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-152">On the action pane, select the **Set Up** tab, and then select **Cash declaration**.</span></span>
1. <span data-ttu-id="9bbb9-153">في جزء الإجراءات، حدد‏‎ **جديد**، ثم أنشئ جميع الفئات النقدية من **العملة المعدنية** و**العملة الورقية‬** القابلة للتطبيق.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-153">On the action pane, select **New**, and then create all **Coin** and **Note** denominations that are applicable.</span></span>

<span data-ttu-id="9bbb9-154">تعرض الصورة التالية مثالاً عن إقرار النقدية‬.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-154">The following image shows an example of a cash declaration.</span></span>

![إعداد الإقرارات النقدية](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="9bbb9-156">إعداد أوضاع التسليم</span><span class="sxs-lookup"><span data-stu-id="9bbb9-156">Set up modes of delivery</span></span>

<span data-ttu-id="9bbb9-157">يمكنك الاطلاع على أوضاع التسليم التي تم تكوينها عن طريق تحديد **أوضاع التسليم** من علامة التبويب **الإعداد** على **جزء الإجراءات**.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-157">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="9bbb9-158">لتغيير وضع التسليم أو إضافته، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-158">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="9bbb9-159">في جزء التنقل، انتقل إلى **الوحدات \> إدارة المخزون \> أوضاع التسليم**.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-159">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="9bbb9-160">في جزء الإجراءات، حدد **جديد** لإنشاء وضع تسليم جديد، أو حدد وضعًا موجودًا.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-160">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="9bbb9-161">في قسم **قنوات البيع بالتجزئة**، حدد **إضافة بند** لإضافة القناة.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-161">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="9bbb9-162">تؤدي إضافة قنوات باستخدام عقد المؤسسة بدلاً من إضافة كل قناة بشكل فردي إلى تنظيم عملية إضافة القنوات.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-162">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="9bbb9-163">تعرض الصورة التالية مثالاً لوضع التسليم.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-163">The following image shows an example of a mode of delivery.</span></span>

![إعداد أوضاع التسليم](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a><span data-ttu-id="9bbb9-165">إعداد حساب الإيرادات/المصروفات</span><span class="sxs-lookup"><span data-stu-id="9bbb9-165">Set up income/expense account</span></span>

<span data-ttu-id="9bbb9-166">لإعداد إعداد حساب الإيرادات/المصروفات‬، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-166">To set up income/expense account, follow these steps.</span></span>

1. <span data-ttu-id="9bbb9-167">في جزء الإجراءات، حدد علامة التبويب **الإعداد**، ثم حدد **حساب الإيرادات/المصروفات**.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-167">On the action pane, select the **Set Up** tab, and then select **Income/Expense account**.</span></span>
1. <span data-ttu-id="9bbb9-168">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-168">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="9bbb9-169">ضمن **الاسم**، أدخل اسمًا.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-169">Under **Name**, enter a name.</span></span>
1. <span data-ttu-id="9bbb9-170">ضمن **اسم البحث**، أدخل اسمًا للبحث.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-170">Under **Search name**, enter a search name.</span></span>
1. <span data-ttu-id="9bbb9-171">ضمن **نوع الحساب**، أدخل نوع الحساب.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-171">Under **Account type**, enter the account type.</span></span>
1. <span data-ttu-id="9bbb9-172">أدخل نص **سطر الرسالة 1** و**سطر الرسالة 2** و**نص القسيمة‬ 1** و**نص القسيمة‬ 2** حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-172">Enter text for **Message line 1**, **Message line 2**, **Slip text 1**, and **Slip text 2** as needed.</span></span>
1. <span data-ttu-id="9bbb9-173">ضمن **الترحيل**، أدخل معلومات الترحيل.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-173">Under **Posting**, enter posting information.</span></span>
1. <span data-ttu-id="9bbb9-174">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-174">On the action pane, select **Save**.</span></span>

<span data-ttu-id="9bbb9-175">تعرض الصورة التالية مثالاً لحساب الإيرادات/المصروفات.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-175">The following image shows an example of an income/expense account.</span></span>

![إعداد حسابات الإيرادات/المصروفات](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a><span data-ttu-id="9bbb9-177">إعداد الأقسام</span><span class="sxs-lookup"><span data-stu-id="9bbb9-177">Set up sections</span></span>

<span data-ttu-id="9bbb9-178">لإعداد الأقسام‬، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="9bbb9-178">To set up sections, follow these steps.</span></span>

1. <span data-ttu-id="9bbb9-179">في جزء الإجراءات، حدد علامة التبويب **الإعداد**، ثم انقر فوق **الأقسام**.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-179">On the action pane, select the **Set Up** tab and click **Sections**.</span></span>
1. <span data-ttu-id="9bbb9-180">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-180">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="9bbb9-181">ضمن **رقم القسم**، أدخل رقم القسم‏‎.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-181">Under **Section number**, enter a section number.</span></span>
1. <span data-ttu-id="9bbb9-182">ضمن **الوصف** ، ادخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-182">Under **Description**, enter a description.</span></span>
1. <span data-ttu-id="9bbb9-183">ضمن **حجم القسم**، أدخل حجم القسم‏‎.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-183">Under **Section size**, enter a section size.</span></span>
1. <span data-ttu-id="9bbb9-184">قم بتكوين إعدادات إضافية في **عام** و**إحصاءات المبيعات‬** حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-184">Configure additional settings for **General** and **Sales statistics** as needed.</span></span>
1. <span data-ttu-id="9bbb9-185">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-185">On the action pane, select **Save**.</span></span>

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="9bbb9-186">إعداد تعيين مجموعة تنفيذ</span><span class="sxs-lookup"><span data-stu-id="9bbb9-186">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="9bbb9-187">لإعداد تعيين مجموعة تنفيذ، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-187">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="9bbb9-188">في جزء الإجراءات، حدد علامة التبويب **الإعداد**، ثم حدد **تعيين مجموعة تنفيذ**.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-188">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="9bbb9-189">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-189">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="9bbb9-190">في القائمة المنسدلة **مجموعة التنفيذ‬**، حدد مجموعة تنفيذ.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-190">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="9bbb9-191">في القائمة المنسدلة **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-191">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="9bbb9-192">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-192">On the action pane, select **Save**</span></span>

<span data-ttu-id="9bbb9-193">تعرض الصورة التالية مثالاً لإعداد تعيين مجموعة تنفيذ.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-193">The following image shows an example of a fulfillment group assignment setup.</span></span>

![إعداد تعيينات مجموعة تنفيذ](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a><span data-ttu-id="9bbb9-195">إعداد الخزائن</span><span class="sxs-lookup"><span data-stu-id="9bbb9-195">Set up safes</span></span>

<span data-ttu-id="9bbb9-196">لإعداد الخزائن، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="9bbb9-196">To set up safes, follow these steps.</span></span>

1. <span data-ttu-id="9bbb9-197">في جزء الإجراءات، حدد علامة التبويب **الإعداد**، ثم انقر فوق **الخزائن**.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-197">On the action pane, select the **Set Up** tab and click **Safes**.</span></span>
1. <span data-ttu-id="9bbb9-198">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-198">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="9bbb9-199">أدخل اسمًا للخزانة.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-199">Enter a name for the safe.</span></span>
1. <span data-ttu-id="9bbb9-200">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="9bbb9-200">On the action pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9bbb9-201">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="9bbb9-201">Additional resources</span></span>

[<span data-ttu-id="9bbb9-202">نظرة عامة على القنوات</span><span class="sxs-lookup"><span data-stu-id="9bbb9-202">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="9bbb9-203">المتطلبات الأساسية‬ لإعداد قناة</span><span class="sxs-lookup"><span data-stu-id="9bbb9-203">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="9bbb9-204">إعداد قناة عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="9bbb9-204">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="9bbb9-205">إعداد قناة مركز اتصال</span><span class="sxs-lookup"><span data-stu-id="9bbb9-205">Set up a call center channel</span></span>](channel-setup-callcenter.md)

