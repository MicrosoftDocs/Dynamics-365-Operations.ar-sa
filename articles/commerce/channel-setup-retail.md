---
title: إعداد قناة بيع بالتجزئة
description: يوضح هذا الموضوع كيفية إنشاء قناة بيع بالتجزئة جديدة في Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3f1f5dc2c8402d9b6b68a049f804932812eb74c0
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937524"
---
# <a name="set-up-a-retail-channel"></a><span data-ttu-id="55889-103">إعداد قناة البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="55889-103">Set up a retail channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="55889-104">يوضح هذا الموضوع كيفية إنشاء قناة بيع بالتجزئة جديدة في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="55889-104">This topic describes how to create a new retail channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="55889-105">يدعم Dynamics 365 Commerce عدة قنوات بيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="55889-105">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="55889-106">وتتضمن قنوات البيع بالتجزئة هذه المتاجر على إنترنت، ومراكز الاتصال، ومتاجر البيع بالتجزئة (تعرف أيضًا بالمتاجر التقليدية).</span><span class="sxs-lookup"><span data-stu-id="55889-106">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="55889-107">يمكن أن يكون لكل قناة متجر للبيع بالتجزئة طرق الدفع ومجموعات الأسعار وسجلات نقطة البيع (POS) وحسابات الإيرادات والمصروفات وفريق العمل الخاص بها.</span><span class="sxs-lookup"><span data-stu-id="55889-107">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="55889-108">ويجب إعداد كل هذه العناصر قبل إمكانية إنشاء قناة لمتجر البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="55889-108">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="55889-109">قبل إنشاء قناة بيع بالتجزئة، تأكد من اتباع [المتطلبات الأساسية للقناة](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="55889-109">Before a retail channel is created, ensure you follow the [channel prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-retail-channel"></a><span data-ttu-id="55889-110">إنشاء قناة بيع بالتجزئة جديدة وتكوينها</span><span class="sxs-lookup"><span data-stu-id="55889-110">Create and configure a new retail channel</span></span>

1. <span data-ttu-id="55889-111">في جزء التنقل، انتقل إلى **الوحدات \> القنوات \> المتاجر‬\> جميع المتاجر‬**.</span><span class="sxs-lookup"><span data-stu-id="55889-111">In the navigation pane, go to **Modules \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="55889-112">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="55889-112">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="55889-113">في حقل **الاسم** أدخل اسمًا للقناة الجديدة.</span><span class="sxs-lookup"><span data-stu-id="55889-113">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="55889-114">في حقل **رقم المتجر**، أدخل رقمًا فريدُا للمتجر.</span><span class="sxs-lookup"><span data-stu-id="55889-114">In the **Store number** field, provide a unique store number.</span></span> <span data-ttu-id="55889-115">بإمكان الرقم أن يكون أبجديًا رقميًا ويتكون من 10 احرف بحدٍ أقصى.</span><span class="sxs-lookup"><span data-stu-id="55889-115">The number can be alphanumeric with a maximum of 10 characters.</span></span>
1. <span data-ttu-id="55889-116">في القائمة المنسدلة **الكيان القانوني**، أدخل الكيان القانوني المناسب.</span><span class="sxs-lookup"><span data-stu-id="55889-116">In the **Legal entity** drop-down list, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="55889-117">في القائمة‏‎ المنسدلة **المستودع**، أدخل المستودع المناسب.</span><span class="sxs-lookup"><span data-stu-id="55889-117">In the **Warehouse** drop-down list, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="55889-118">في الحقل **المنطقة الزمنية للمتجر**، حدد المنطقة الزمنية المناسبة.</span><span class="sxs-lookup"><span data-stu-id="55889-118">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="55889-119">في القائمة المنسدلة **مجموعة ضريبة المبيعات‬**، حدد مجموعه ضريبة مبيعات مناسبة للمتجر.</span><span class="sxs-lookup"><span data-stu-id="55889-119">In the **Sales tax group** drop-down list, select an appropriate sales tax group for the store.</span></span>
1. <span data-ttu-id="55889-120">في حقل **العملة**، حدد العملة المناسبة.</span><span class="sxs-lookup"><span data-stu-id="55889-120">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="55889-121">في حقل **دفتر عناوين العميل‬**، أدخل دفتر عناوين صالحًا.</span><span class="sxs-lookup"><span data-stu-id="55889-121">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="55889-122">في حقل **العميل الافتراضي**، أدخل عميل افتراضي صالح.</span><span class="sxs-lookup"><span data-stu-id="55889-122">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="55889-123">في الحقل **ملف تعريف الوظائف**، حدد ملف تعريف الوظائف، إن أمكن.</span><span class="sxs-lookup"><span data-stu-id="55889-123">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="55889-124">في الحقل **ملف تعريف الإخطار بالبريد الإلكتروني**، أدخل ملف تعريف إخطار بالبريد الإلكتروني صالحًا.</span><span class="sxs-lookup"><span data-stu-id="55889-124">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="55889-125">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="55889-125">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="55889-126">توضح الصورة التالية إنشاء قناة بيع بالتجزئة جديدة.</span><span class="sxs-lookup"><span data-stu-id="55889-126">The following image shows the creation of a new retail channel.</span></span>

![قناة بيع بالتجزئة جديدة](media/channel-setup-retail-1.png)

<span data-ttu-id="55889-128">تعرض الصورة التالية مثالاً لقناة بيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="55889-128">The following image shows an example retail channel.</span></span>

![مثال قناة البيع بالتجزئة](media/channel-setup-retail-2.png)

## <a name="other-settings"></a><span data-ttu-id="55889-130">إعدادات أخرى</span><span class="sxs-lookup"><span data-stu-id="55889-130">Other settings</span></span>

<span data-ttu-id="55889-131">هناك الكثير من الإعدادات الاختيارية الأخرى التي يمكنك تعيينها في القسمين **كشف الحساب/الإقفال‬** و **متنوع‬**، استنادًا إلى احتياجات متجر البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="55889-131">There are numerous other optional settings that can be set in the **Statement/closing** and **Miscellaneous** sections, based on the needs of the retail store.</span></span>

<span data-ttu-id="55889-132">بالإضافة إلى ذلك، راجع [تخطيطات الشاشة الخاصة بنقطة البيع (POS)](pos-screen-layouts.md) للحصول على معلومات حول إعداد تخطيط الشاشة الافتراضية في القسم **تخطيط الشاشة** والقسم [تكوين Retail Hardware Station وتثبيتها‬](retail-hardware-station-configuration-installation.md) للحصول على معلومات الإعداد حول **محطات الأجهزة‬**.</span><span class="sxs-lookup"><span data-stu-id="55889-132">In addition, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information on setting up the default screen layout in the **Screen layout** section and [Configure and install Retail hardware station](retail-hardware-station-configuration-installation.md) for setup information about the **Hardware stations** section.</span></span>

<span data-ttu-id="55889-133">تعرض الصورة التالية مثالاً لتكوبن إعداد قناة بيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="55889-133">The following image shows an example retail channel setup configuration.</span></span>

![مثال عن تكوين قناة البيع بالتجزئة](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a><span data-ttu-id="55889-135">إعداد إضافي للقناة</span><span class="sxs-lookup"><span data-stu-id="55889-135">Additional channel set up</span></span>

<span data-ttu-id="55889-136">هناك عناصر إضافية يجب إعدادها للقناة ويمكن العثور عليها في جزء الإجراءات ضمن قسم **الإعداد**.</span><span class="sxs-lookup"><span data-stu-id="55889-136">There are additional items that need to be set up for a channel that can be found on the Action Pane under the **Set up** section.</span></span>

<span data-ttu-id="55889-137">تتضمن المهام الإضافية المطلوبة لإعداد القناة عبر الإنترنت إعداد طرق الدفع وإقرار النقدية وأوضاع التسليم وحساب الإيرادات/المصروفات والأقسام وتعيين مجموعه التنفيذ والخزائن‬.</span><span class="sxs-lookup"><span data-stu-id="55889-137">Additional tasks required for online channel setup include setting up payment methods, cash declaration, modes of delivery, income/expense account, sections, the fulfillment group assignment, and safes.</span></span>

<span data-ttu-id="55889-138">تعرض الصورة التالية خيارات إضافية لإعداد قناة البيع بالتجزئة على علامة تبويب **الإعداد**.</span><span class="sxs-lookup"><span data-stu-id="55889-138">The following image shows various additional retail channel setup options on the **Set up** tab.</span></span>

![إعداد القناة](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="55889-140">إعداد طرق الدفع</span><span class="sxs-lookup"><span data-stu-id="55889-140">Set up payment methods</span></span>

<span data-ttu-id="55889-141">لإعداد طرق الدفع، لكل نوع دفع معتمد على هذه القناة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="55889-141">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="55889-142">في جزء الإجراءات، حدد علامة التبويب **الإعداد**، ثم حدد **طرق الدفع**.</span><span class="sxs-lookup"><span data-stu-id="55889-142">On the Action Pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="55889-143">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="55889-143">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="55889-144">في جزء التنقل، حدد طريقة الدفع المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="55889-144">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="55889-145">في القسم **عام**، أدخل **اسم العملية**، وقم بتكوين أي إعدادات أخرى مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="55889-145">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="55889-146">قم بتكوين أي إعدادات إضافية مطلوبة لنوع الدفع.</span><span class="sxs-lookup"><span data-stu-id="55889-146">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="55889-147">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="55889-147">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="55889-148">تعرض الصورة التالية مثالاً عن طريقة الدفع النقدي.</span><span class="sxs-lookup"><span data-stu-id="55889-148">The following image shows an example of a cash payment method.</span></span>

![أمثلة عن طرق الدفع](media/channel-setup-retail-5.png)

### <a name="set-up-cash-declaration"></a><span data-ttu-id="55889-150">إعداد إقرار النقدية</span><span class="sxs-lookup"><span data-stu-id="55889-150">Set up cash declaration</span></span>

1. <span data-ttu-id="55889-151">في جزء الإجراءات، حدد علامة التبويب **الإعداد**، ثم حدد **إقرار النقدية**.</span><span class="sxs-lookup"><span data-stu-id="55889-151">On the Action Pane, select the **Set Up** tab, and then select **Cash declaration**.</span></span>
1. <span data-ttu-id="55889-152">في جزء الإجراءات، حدد‏‎ **جديد**، ثم أنشئ جميع الفئات النقدية من **العملة المعدنية** و **العملة الورقية‬** القابلة للتطبيق.</span><span class="sxs-lookup"><span data-stu-id="55889-152">On the Action Pane, select **New**, and then create all **Coin** and **Note** denominations that are applicable.</span></span>

<span data-ttu-id="55889-153">تعرض الصورة التالية مثالاً عن إقرار النقدية‬.</span><span class="sxs-lookup"><span data-stu-id="55889-153">The following image shows an example of a cash declaration.</span></span>

![إعداد الإقرارات النقدية](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="55889-155">إعداد أوضاع التسليم</span><span class="sxs-lookup"><span data-stu-id="55889-155">Set up modes of delivery</span></span>

<span data-ttu-id="55889-156">يمكنك الاطلاع على أوضاع التسليم التي تم تكوينها عن طريق تحديد **أوضاع التسليم** من علامة تبويب **الإعداد** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="55889-156">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the Action Pane.</span></span>  

<span data-ttu-id="55889-157">لتغيير وضع التسليم أو إضافته، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="55889-157">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="55889-158">في جزء التنقل، انتقل إلى **الوحدات \> إدارة المخزون \> أوضاع التسليم**.</span><span class="sxs-lookup"><span data-stu-id="55889-158">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="55889-159">في جزء الإجراءات، حدد **جديد** لإنشاء وضع تسليم جديد، أو حدد وضعًا موجودًا.</span><span class="sxs-lookup"><span data-stu-id="55889-159">On the Action Pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="55889-160">في قسم **قنوات البيع بالتجزئة**، حدد **إضافة بند** لإضافة القناة.</span><span class="sxs-lookup"><span data-stu-id="55889-160">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="55889-161">تؤدي إضافة قنوات باستخدام عقد المؤسسة بدلاً من إضافة كل قناة بشكل فردي إلى تنظيم عملية إضافة القنوات.</span><span class="sxs-lookup"><span data-stu-id="55889-161">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="55889-162">تعرض الصورة التالية مثالاً لوضع التسليم.</span><span class="sxs-lookup"><span data-stu-id="55889-162">The following image shows an example of a mode of delivery.</span></span>

![إعداد أوضاع التسليم](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a><span data-ttu-id="55889-164">إعداد حساب الإيرادات/المصروفات</span><span class="sxs-lookup"><span data-stu-id="55889-164">Set up income/expense account</span></span>

<span data-ttu-id="55889-165">لإعداد إعداد حساب الإيرادات/المصروفات‬، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="55889-165">To set up income/expense account, follow these steps.</span></span>

1. <span data-ttu-id="55889-166">في جزء الإجراءات، حدد علامة التبويب **الإعداد**، ثم حدد **حساب الإيرادات/المصروفات**.</span><span class="sxs-lookup"><span data-stu-id="55889-166">On the Action Pane, select the **Set Up** tab, and then select **Income/Expense account**.</span></span>
1. <span data-ttu-id="55889-167">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="55889-167">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="55889-168">ضمن **الاسم**، أدخل اسمًا.</span><span class="sxs-lookup"><span data-stu-id="55889-168">Under **Name**, enter a name.</span></span>
1. <span data-ttu-id="55889-169">ضمن **اسم البحث**، أدخل اسمًا للبحث.</span><span class="sxs-lookup"><span data-stu-id="55889-169">Under **Search name**, enter a search name.</span></span>
1. <span data-ttu-id="55889-170">ضمن **نوع الحساب**، أدخل نوع الحساب.</span><span class="sxs-lookup"><span data-stu-id="55889-170">Under **Account type**, enter the account type.</span></span>
1. <span data-ttu-id="55889-171">أدخل نص **سطر الرسالة 1** و **سطر الرسالة 2** و **نص القسيمة‬ 1** و **نص القسيمة‬ 2** حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="55889-171">Enter text for **Message line 1**, **Message line 2**, **Slip text 1**, and **Slip text 2** as needed.</span></span>
1. <span data-ttu-id="55889-172">ضمن **الترحيل**، أدخل معلومات الترحيل.</span><span class="sxs-lookup"><span data-stu-id="55889-172">Under **Posting**, enter posting information.</span></span>
1. <span data-ttu-id="55889-173">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="55889-173">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="55889-174">تعرض الصورة التالية مثالاً لحساب الإيرادات/المصروفات.</span><span class="sxs-lookup"><span data-stu-id="55889-174">The following image shows an example of an income/expense account.</span></span>

![إعداد حسابات الإيرادات/المصروفات](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a><span data-ttu-id="55889-176">إعداد الأقسام</span><span class="sxs-lookup"><span data-stu-id="55889-176">Set up sections</span></span>

<span data-ttu-id="55889-177">لإعداد الأقسام‬، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="55889-177">To set up sections, follow these steps.</span></span>

1. <span data-ttu-id="55889-178">في جزء الإجراءات، حدد علامة التبويب **الإعداد**، ثم انقر فوق **الأقسام**.</span><span class="sxs-lookup"><span data-stu-id="55889-178">On the Action Pane, select the **Set Up** tab and click **Sections**.</span></span>
1. <span data-ttu-id="55889-179">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="55889-179">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="55889-180">ضمن **رقم القسم**، أدخل رقم القسم‏‎.</span><span class="sxs-lookup"><span data-stu-id="55889-180">Under **Section number**, enter a section number.</span></span>
1. <span data-ttu-id="55889-181">ضمن **الوصف** ، ادخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="55889-181">Under **Description**, enter a description.</span></span>
1. <span data-ttu-id="55889-182">ضمن **حجم القسم**، أدخل حجم القسم‏‎.</span><span class="sxs-lookup"><span data-stu-id="55889-182">Under **Section size**, enter a section size.</span></span>
1. <span data-ttu-id="55889-183">قم بتكوين إعدادات إضافية في **عام** و **إحصاءات المبيعات‬** حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="55889-183">Configure additional settings for **General** and **Sales statistics** as needed.</span></span>
1. <span data-ttu-id="55889-184">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="55889-184">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="55889-185">إعداد تعيين مجموعة تنفيذ</span><span class="sxs-lookup"><span data-stu-id="55889-185">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="55889-186">لإعداد تعيين مجموعة تنفيذ، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="55889-186">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="55889-187">في جزء الإجراءات، حدد علامة التبويب **الإعداد**، ثم حدد **تعيين مجموعة تنفيذ**.</span><span class="sxs-lookup"><span data-stu-id="55889-187">On the Action Pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="55889-188">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="55889-188">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="55889-189">في القائمة المنسدلة **مجموعة التنفيذ‬**، حدد مجموعة تنفيذ.</span><span class="sxs-lookup"><span data-stu-id="55889-189">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="55889-190">في القائمة المنسدلة **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="55889-190">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="55889-191">في جزء الإجراءات، حدد **حفظ**</span><span class="sxs-lookup"><span data-stu-id="55889-191">On the Action Pane, select **Save**</span></span>

<span data-ttu-id="55889-192">تعرض الصورة التالية مثالاً لإعداد تعيين مجموعة تنفيذ.</span><span class="sxs-lookup"><span data-stu-id="55889-192">The following image shows an example of a fulfillment group assignment setup.</span></span>

![إعداد تعيينات مجموعة تنفيذ](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a><span data-ttu-id="55889-194">إعداد الخزائن</span><span class="sxs-lookup"><span data-stu-id="55889-194">Set up safes</span></span>

<span data-ttu-id="55889-195">لإعداد الخزائن، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="55889-195">To set up safes, follow these steps.</span></span>

1. <span data-ttu-id="55889-196">في جزء الإجراءات، حدد علامة التبويب **الإعداد**، ثم انقر فوق **الخزائن**.</span><span class="sxs-lookup"><span data-stu-id="55889-196">On the Action Pane, select the **Set Up** tab and click **Safes**.</span></span>
1. <span data-ttu-id="55889-197">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="55889-197">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="55889-198">أدخل اسمًا للخزانة.</span><span class="sxs-lookup"><span data-stu-id="55889-198">Enter a name for the safe.</span></span>
1. <span data-ttu-id="55889-199">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="55889-199">On the Action Pane, select **Save**.</span></span>

### <a name="ensure-unique-transaction-ids"></a><span data-ttu-id="55889-200">التأكد من معرفات الحركات الفريدة</span><span class="sxs-lookup"><span data-stu-id="55889-200">Ensure unique transaction IDs</span></span>

<span data-ttu-id="55889-201">اعتبارًا من إصدار Commerce رقم 10.0.18، تكون معرفات الحركات التي تم إنشاؤها لنقطة البيع (POS) متسلسلة وتتضمن الأجزاء التالية:</span><span class="sxs-lookup"><span data-stu-id="55889-201">As of the Commerce version 10.0.18 , transaction IDs generated for the point of sale (POS) are sequential and include the following parts:</span></span>

- <span data-ttu-id="55889-202">جزء ثابت، وهو سلسلة من معرف المتجر ومعرف الوحدة الطرفية.</span><span class="sxs-lookup"><span data-stu-id="55889-202">A fixed part, which is a concatenation of store ID and terminal ID.</span></span> 
- <span data-ttu-id="55889-203">جزء تسلسلي، وهو تسلسل رقمي.</span><span class="sxs-lookup"><span data-stu-id="55889-203">A sequential part, which is a number sequence.</span></span> 

<span data-ttu-id="55889-204">بشكل خاص، يكون التنسيق *{store} - {terminal} -{numbersequence}*.</span><span class="sxs-lookup"><span data-stu-id="55889-204">Specifically, the format is *{store}-{terminal}-{numbersequence}*.</span></span> 

<span data-ttu-id="55889-205">نظرا لأنه يمكن إنشاء معرفات الحركات في أوضاع متصلة وغير متصلة، فقد تم إنشاء مثيلات لمعرفات الحركات المكررة.</span><span class="sxs-lookup"><span data-stu-id="55889-205">Because transaction IDs can be generated in offline and online modes, there have been instances of duplicate transaction IDs being generated.</span></span> <span data-ttu-id="55889-206">تتطلب إزالة معرفات الحركات المكررة إصلاحًا يدويًا للبيانات.</span><span class="sxs-lookup"><span data-stu-id="55889-206">Eliminating duplicate transaction IDs requires a lot of manual data fixing.</span></span> 

<span data-ttu-id="55889-207">باستخدام إصدار Commerce رقم 10.0.19، تم تحديث تنسيق معرف الحركة لإزالة الجزء المتسلسل ويستخدم بدلاً من ذلك رقمًا مكونًا من 13 رقمًا تم إنشاؤه عن طريق حساب الوقت بالمللي ثانية منذ عام 1970.</span><span class="sxs-lookup"><span data-stu-id="55889-207">With Commerce version 10.0.19, the transaction ID format has been updated to remove the sequential part and instead uses a 13-digit number generated by calculating the time in milliseconds since 1970.</span></span> <span data-ttu-id="55889-208">وبهذا التغيير، يكون تنسيق معرف الحركة الجديد هو *{store}-{terminal}-{millisecondsSince1970}*.</span><span class="sxs-lookup"><span data-stu-id="55889-208">With this change, the new transaction ID format is *{store}-{terminal}-{millisecondsSince1970}*.</span></span> <span data-ttu-id="55889-209">يجعل هذا التحديث معرف الحركة غير متسلسل ويضمن أن تكون معرفات الحركات فريدة دائمًا.</span><span class="sxs-lookup"><span data-stu-id="55889-209">This update makes the transaction ID non-sequential and ensures that transaction IDs are always unique.</span></span> 

> [!NOTE]
> <span data-ttu-id="55889-210">معرّفات الحركات مخصصة لاستخدام النظام الداخلي فقط، لذلك لا يلزم أن تكون متسلسلة.</span><span class="sxs-lookup"><span data-stu-id="55889-210">Transaction IDs are meant for internal system use only, so they are not required to be sequential.</span></span> <span data-ttu-id="55889-211">ومع ذلك، تتطلب العديد من البلدان أن تكون معرفات الإيصالات مسلسلة.</span><span class="sxs-lookup"><span data-stu-id="55889-211">However, many countries require receipt IDs to be sequential.</span></span>

<span data-ttu-id="55889-212">يمكن تمكين ميزة تنسيق معرف الحركة الجديد من مساحة عمل **إدارة الميزات**.</span><span class="sxs-lookup"><span data-stu-id="55889-212">The new transaction ID format feature can be enabled from the **Feature management** workspace.</span></span> 

<span data-ttu-id="55889-213">لتمكين استخدام معرفات الحركات الجديدة، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="55889-213">To enable the use of new transaction IDs, follow these steps:</span></span>

1. <span data-ttu-id="55889-214">في Commerce headquarters، انتقل إلى **إدارة النظام \> مساحات العمل \> إدارة الميزات**.</span><span class="sxs-lookup"><span data-stu-id="55889-214">In Commerce headquarters, go to **System administration \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="55889-215">قم بالتصفية لوحدة "البيع بالتجزئة والتجارة".</span><span class="sxs-lookup"><span data-stu-id="55889-215">Filter for the "retail and commerce" module.</span></span>
1. <span data-ttu-id="55889-216">ابحث عن اسم ميزة **تمكين معرف الحركة الجديد لتجنب تكرار معرفات الحركات**.</span><span class="sxs-lookup"><span data-stu-id="55889-216">Search for the **Enable new transaction id to avoid duplicate transaction ids** feature name.</span></span>
1. <span data-ttu-id="55889-217">حدد الميزة، ثم حدد **تمكين الآن** في الجانب الأيمن.</span><span class="sxs-lookup"><span data-stu-id="55889-217">Select the feature, and then select **Enable Now** in the right pane.</span></span>  
1. <span data-ttu-id="55889-218">انتقل إلى **البيع بالتجزئة والتجارة \> تكنولوجيا معلومات البيع بالتجزئة والتجارة \> جدول التوزيع**.</span><span class="sxs-lookup"><span data-stu-id="55889-218">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="55889-219">قم بتشغيل وظيفتي **تكوين قناة 1070** و **مسجل مهام نقطة بيع 1170** لمزامنة الميزة الممكّنة مع المتاجر.</span><span class="sxs-lookup"><span data-stu-id="55889-219">Run the **1070 Channel configuration** and **1170 POS task recorder** jobs to synchronize the enabled feature to the stores.</span></span>
1. <span data-ttu-id="55889-220">بعد إرسال التغييرات إلى المتاجر ، يجب إغلاق وحدات نقاط البيع الطرفية وإعادة فتحها لاستخدام تنسيق معرف الحركة الجديد.</span><span class="sxs-lookup"><span data-stu-id="55889-220">After the changes have been sent to the stores, POS terminals must be closed and reopened to use the new transaction ID format.</span></span> 

> [!NOTE]
> <span data-ttu-id="55889-221">بعد تمكين ميزه تنسيق معرف الحركة الجديد، لن تتمكن من تعطيل هذه الميزة.</span><span class="sxs-lookup"><span data-stu-id="55889-221">After the new transaction ID format feature is enabled, you will not be able to disable this feature.</span></span> <span data-ttu-id="55889-222">إذا كان يجب تعطيلها، فيُرجى الاتصال بدعم Commerce.</span><span class="sxs-lookup"><span data-stu-id="55889-222">If it must be disabled, please contact Commerce Support.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="55889-223">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="55889-223">Additional resources</span></span>

[<span data-ttu-id="55889-224">نظره عامة حول القنوات</span><span class="sxs-lookup"><span data-stu-id="55889-224">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="55889-225">المتطلبات الأساسية لإعداد القناة</span><span class="sxs-lookup"><span data-stu-id="55889-225">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="55889-226">إعداد قناة عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="55889-226">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="55889-227">إعداد قناة مركز اتصال</span><span class="sxs-lookup"><span data-stu-id="55889-227">Set up a call center channel</span></span>](channel-setup-callcenter.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
