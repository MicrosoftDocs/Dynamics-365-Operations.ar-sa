---
title: تكوين BOPIS في بيئة تقييم Dynamics 365 Commerce
description: يوضح هذا الموضوع كيف تكون الشراء عبر الإنترنت والانتقاء في المتجر (BOPIS) في بيئة تقييم Microsoft Dynamics 365 Commerce بعد توفيرها.
author: rubendel
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: rubendel
ms.search.validFrom: 2020-04-20
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 56319035ac092a376f0766c20eee71af6256b6f9
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936900"
---
# <a name="configure-bopis-in-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="d614d-103">تكوين BOPIS (الشراء عبر الإنترنت والاستلام في المتجر) في بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="d614d-103">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d614d-104">يوضح هذا الموضوع كيفية تكوين الشراء عبر الإنترنت والانتقاء في المتجر (BOPIS) في بيئة تقييم Microsoft Dynamics 365 Commerce بعد توفيرها.</span><span class="sxs-lookup"><span data-stu-id="d614d-104">This topic explains how to configure buy online, pickup in store (BOPIS) in a Microsoft Dynamics 365 Commerce evaluation environment after the environment has been provisioned.</span></span>

## <a name="prerequisite"></a><span data-ttu-id="d614d-105">المتطلب الأساسي</span><span class="sxs-lookup"><span data-stu-id="d614d-105">Prerequisite</span></span>

<span data-ttu-id="d614d-106">استكمل الإجراءات في هذا الموضوع فقط بعد توفير بيئة تقييم Commerce وتكوينها.</span><span class="sxs-lookup"><span data-stu-id="d614d-106">Complete the procedures in this topic only after your Commerce evaluation environment has been provisioned and configured.</span></span> <span data-ttu-id="d614d-107">لمزيد من المعلومات حول توفير وتكوين البيئة الخاصة بك، راجع [توفير بيئة تقييم Dynamics 365 Commerce](provisioning-guide.md) و[تكوين بيئة تقييم Dynamics 365 Commerce](./cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="d614d-107">For information about how to provision and configure your environment, see [Provision a Dynamics 365 Commerce evaluation environment](provisioning-guide.md) and [Configure a Dynamics 365 Commerce evaluation environment](./cpe-post-provisioning.md).</span></span>

<span data-ttu-id="d614d-108">بعد توفير بيئة معاينة Commerce وتكوينها من البداية إلى النهائية، يمكنك استخدام هذا الموضوع لتكوين سيناريوهات BOPIS.</span><span class="sxs-lookup"><span data-stu-id="d614d-108">After your Commerce environment has been provisioned and configured end to end, you can use this topic to enable BOPIS scenarios.</span></span>

## <a name="configure-the-pos"></a><span data-ttu-id="d614d-109">تكوين نقطة البيع (POS)</span><span class="sxs-lookup"><span data-stu-id="d614d-109">Configure the POS</span></span>

### <a name="configure-modern-pos"></a><span data-ttu-id="d614d-110">تكوين Modern POS</span><span class="sxs-lookup"><span data-stu-id="d614d-110">Configure Modern POS</span></span>

<span data-ttu-id="d614d-111">تحتاج سيناريوهات BOPIS التي تتضمن الدفع ببطاقة ائتمان إلى محطة أجهزة.</span><span class="sxs-lookup"><span data-stu-id="d614d-111">BOPIS scenarios that involve a credit card payment require a hardware station.</span></span> <span data-ttu-id="d614d-112">ويتم دمج محطة الأجهزة في Modern POS لعملاء Windows وAndroid.</span><span class="sxs-lookup"><span data-stu-id="d614d-112">The hardware station is built into Modern POS for Windows and Android clients.</span></span> <span data-ttu-id="d614d-113">إذا كنت تستخدم Cloud POS أو Modern POS لـ iOS، فيجب إقران عميل نقطة البيع (POS) مع محطة أجهزة مشتركة.</span><span class="sxs-lookup"><span data-stu-id="d614d-113">If you're using Cloud POS or Modern POS for iOS, the point of sale (POS) client must be paired with a shared hardware station.</span></span> <span data-ttu-id="d614d-114">يشرح هذا الموضوع كيفية تكوين BOPIS لعملاء Windows وAndroid.</span><span class="sxs-lookup"><span data-stu-id="d614d-114">This topic explains how to configure BOPIS for Windows and Android clients.</span></span> <span data-ttu-id="d614d-115">للحصول على مزيد من المعلومات حول كيفية إعداد محطة أجهزة مشتركة، راجع [تكوين محطة أجهزة Retail وتثبيتها](./retail-hardware-station-configuration-installation.md).</span><span class="sxs-lookup"><span data-stu-id="d614d-115">For information about how to set up a shared hardware station, see [Configure and install Retail hardware station](./retail-hardware-station-configuration-installation.md).</span></span>

1. <span data-ttu-id="d614d-116">انتقل إلى **Retail and Commerce \> إعداد قناة \> إعداد POS \> السجلات**.</span><span class="sxs-lookup"><span data-stu-id="d614d-116">Go to **Retail and Commerce \> Channel setup \> POS setup \> Registers**.</span></span>
2. <span data-ttu-id="d614d-117">حدد السجل **SANFRAN-5**، ثم حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="d614d-117">Select register **SANFRAN-5**, and then select **Edit**.</span></span>
3. <span data-ttu-id="d614d-118">قم بتغيير القيمة لحقل **ملف تعريف الجهاز** من **HW002** إلى **HW001**، ثم حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="d614d-118">Change the value of the **Hardware profile** field from **HW002** to **HW001**, and then select **Save**.</span></span>
4. <span data-ttu-id="d614d-119">لمزامنة التغييرات، انتقل إلى **Retail and Commerce \> تكنولوجيا معلومات Retail and Commerce \> جدول التوزيع**.</span><span class="sxs-lookup"><span data-stu-id="d614d-119">To synchronize the changes, go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
5. <span data-ttu-id="d614d-120">حدد جدول التوزيع **1090**، ثم في جزء الإجراء، حدد **تشغيل الآن**.</span><span class="sxs-lookup"><span data-stu-id="d614d-120">Select distribution schedule **1090**, and then, on the Action Pane, select **Run now**.</span></span>
6. <span data-ttu-id="d614d-121">حدد **نعم** ثم **موافق** لبدء مزامنة البيانات.</span><span class="sxs-lookup"><span data-stu-id="d614d-121">Select **Yes** and then **OK** to initiate data synchronization.</span></span> 

### <a name="install-modern-pos"></a><span data-ttu-id="d614d-122">تثبيت Modern POS</span><span class="sxs-lookup"><span data-stu-id="d614d-122">Install Modern POS</span></span>

1. <span data-ttu-id="d614d-123">انتقل إلى **Retail and Commerce \> إعداد قناة \> إعداد POS \> الأجهزة**.</span><span class="sxs-lookup"><span data-stu-id="d614d-123">Go to **Retail and Commerce \> Channel setup \> POS setup \> Devices**.</span></span>
2. <span data-ttu-id="d614d-124">حدد الجهاز **SANFRANCIS-5**.</span><span class="sxs-lookup"><span data-stu-id="d614d-124">Select device **SANFRANCIS-5**.</span></span>
3. <span data-ttu-id="d614d-125">في جزء الإجراء، حدد **تنزيل**، ثم حدد **ملف التكوين**.</span><span class="sxs-lookup"><span data-stu-id="d614d-125">On the Action Pane, select **Download**, and then select **Configuration file**.</span></span>
4. <span data-ttu-id="d614d-126">حدد **تنزيل**، ثم حدد **Retail Modern POS**.</span><span class="sxs-lookup"><span data-stu-id="d614d-126">Select **Download**, and then select **Retail Modern POS**.</span></span> 
5. <span data-ttu-id="d614d-127">عند تنزيل ملف **ModernPOSSetup.exe**، حدد **فتح ملف**.</span><span class="sxs-lookup"><span data-stu-id="d614d-127">When download of the **ModernPOSSetup.exe** file is completed, select **Open file**.</span></span>

    ![فتح ملف](./dev-itpro/media/PAYMENTS/openfile.png)

6. <span data-ttu-id="d614d-129">حدد **التالي** للانتقال خلال عملية التثبيت.</span><span class="sxs-lookup"><span data-stu-id="d614d-129">Select **Next** to go through the installation process.</span></span> <span data-ttu-id="d614d-130">عند استكمال عملية التثبيت، حدد **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="d614d-130">When installation is completed, select **Close**.</span></span>

### <a name="activate-modern-pos"></a><span data-ttu-id="d614d-131">تنشيط Modern POS</span><span class="sxs-lookup"><span data-stu-id="d614d-131">Activate Modern POS</span></span>

1. <span data-ttu-id="d614d-132">في سطح مكتب Windows، حدد زر **بدء**، ثم أدخل **Retail Modern POS**.</span><span class="sxs-lookup"><span data-stu-id="d614d-132">On the Windows desktop, select the **Start** button, and enter **Retail Modern POS**.</span></span>
2. <span data-ttu-id="d614d-133">حدد تطبيق **Retail Modern POS** لبدء التنشيط.</span><span class="sxs-lookup"><span data-stu-id="d614d-133">Select the **Retail Modern POS** application to initiate activation.</span></span>
3. <span data-ttu-id="d614d-134">حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="d614d-134">Select **Next**.</span></span> <span data-ttu-id="d614d-135">يحب أن تكون حقول **عنوان URL للخادم** و **معرف الجهاز** و **رقم التسجيل** مملوءة مسبقًا بالمعلومات من ملف التكوين الذي قمت بتنزيله في الإجراء السابق.</span><span class="sxs-lookup"><span data-stu-id="d614d-135">The **Server URL**, **Device ID**, and **Register number** fields should be preset by using information from the configuration file that you downloaded in the previous procedure.</span></span>
4. <span data-ttu-id="d614d-136">حدد **تنشيط**.</span><span class="sxs-lookup"><span data-stu-id="d614d-136">Select **Activate**.</span></span>
5. <span data-ttu-id="d614d-137">يظهر مربع حوار المصادقة.</span><span class="sxs-lookup"><span data-stu-id="d614d-137">An authentication dialog box appears.</span></span> <span data-ttu-id="d614d-138">حدد الحساب الذي يستخدم عنوان البريد الإلكتروني الذي كان مرتبطًا في السابق بالعامل **000713 - Andrew Collette**.</span><span class="sxs-lookup"><span data-stu-id="d614d-138">Select the account that uses the email address that was previously associated with worker **000713 - Andrew Collette**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d614d-139">إذا لم تكن قد قمت بربط عامل بهويتك، فسيكون التنشيط غير ناجح.</span><span class="sxs-lookup"><span data-stu-id="d614d-139">If you haven't yet associated a worker with your identity, activation will be unsuccessful.</span></span> <span data-ttu-id="d614d-140">في هذه الحالة، اتبع الخطوات تحت قسم "ربط عامل بهويتك" في الموضوع [تكوين بيئة تقييم Dynamics 365 Commerce](cpe-post-provisioning.md#associate-a-worker-with-your-identity).</span><span class="sxs-lookup"><span data-stu-id="d614d-140">In this case, follow the steps under the "Associate a worker with your identity" section in the [Configure a Dynamics 365 Commerce evaluation environment](cpe-post-provisioning.md#associate-a-worker-with-your-identity) topic.</span></span>
    
6. <span data-ttu-id="d614d-141">عندما مطالبتك بالسماح للمؤسسة بإدارة الجهاز، حدد **هذا التطبيق فقط**.</span><span class="sxs-lookup"><span data-stu-id="d614d-141">When you're prompted to let your organization manage the device, select **This app only**.</span></span>
7. <span data-ttu-id="d614d-142">عند استكمال عملية التنشيط، حدد **الشروع في العمل**.</span><span class="sxs-lookup"><span data-stu-id="d614d-142">When activation is completed, select **Get started**.</span></span>

### <a name="enable-bopis-in-modern-pos"></a><span data-ttu-id="d614d-143">تمكين BOPIS في Modern POS</span><span class="sxs-lookup"><span data-stu-id="d614d-143">Enable BOPIS in Modern POS</span></span>

1. <span data-ttu-id="d614d-144">سجل الدخول إلى Modern POS باستخدام **000713** كمعرف مستخدم و **123** ككلمة المرور.</span><span class="sxs-lookup"><span data-stu-id="d614d-144">Sign in to Modern POS by using **000713** as the operator ID and **123** as the password.</span></span>
2. <span data-ttu-id="d614d-145">أثناء تشغيل الفيديو التقديمي للإرشادات التفصيلية، حدد خانتي اختيار في الزاوية السفلية اليسرى لمربع الحوار، ثم أغلق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="d614d-145">While the introductory walkthrough video is playing, select the two check boxes in the lower-left corner of the dialog box, and then close the dialog box.</span></span>
3. <span data-ttu-id="d614d-146">إذا لم تتم مطالبتك بإغلاق الوردية، فقم بالتمرير إلى اليمين على صفحة **الترحيب**، وحدد **إغلاق الوردية**، ثم سجل مرة أخرى الدخول إلى نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="d614d-146">If you aren't prompted to close the shift, scroll to the right on the **Welcome** page, select **Close shift**, and then sign back in to the POS.</span></span>
4. <span data-ttu-id="d614d-147">بعد أن تسجل الدخول، عند مطالبتك، حدد **تنفيذ عملية غير متعلقة بالدرج**.</span><span class="sxs-lookup"><span data-stu-id="d614d-147">After you're signed in, when you're prompted, select **Perform a non-drawer operation**.</span></span>
5. <span data-ttu-id="d614d-148">في صفحة **الترحيب**، قم بالتمرير إلى اليمين، وحدد عملية **تحديد محطة الأجهزة**.</span><span class="sxs-lookup"><span data-stu-id="d614d-148">On the **Welcome** page, scroll to the right, and select the **Select hardware station** operation.</span></span>
6. <span data-ttu-id="d614d-149">حدد **إدارة**، وقم بتعيين خيار **استخدام محطة الأجهزة** إلى **تشغيل**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d614d-149">Select **Manage**, set the **Use hardware station** option to **On**, and then select **OK**.</span></span>
7. <span data-ttu-id="d614d-150">سجل خروجك من نقطة البيع، ثم سجل دخولك مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="d614d-150">Sign out of the POS, and then sign back in.</span></span>
8. <span data-ttu-id="d614d-151">بعد أن تسجل الدخول، حدد **فتح وردية جديدة**، ثم حدد **الدرج**.</span><span class="sxs-lookup"><span data-stu-id="d614d-151">After you're signed in, select **Open a new shift**, and then select **Drawer**.</span></span>

## <a name="complete-a-bopis-scenario"></a><span data-ttu-id="d614d-152">استكمال سيناريو BOPIS</span><span class="sxs-lookup"><span data-stu-id="d614d-152">Complete a BOPIS scenario</span></span>

### <a name="create-a-storefront-order-for-in-store-pickup"></a><span data-ttu-id="d614d-153">إنشاء أمر واجهة متجر للانتقاء في المتجر</span><span class="sxs-lookup"><span data-stu-id="d614d-153">Create a storefront order for in-store pickup</span></span>

1. <span data-ttu-id="d614d-154">انتقل إلى عنوان URL الذي حددته في خطوة [تهيئة التجارة الإلكترونية](./provisioning-guide.md#initialize-e-commerce) أثناء تكوين البيئة.</span><span class="sxs-lookup"><span data-stu-id="d614d-154">Go to the URL that you specified in the [Initialize e-Commerce](./provisioning-guide.md#initialize-e-commerce) step during environment configuration.</span></span>
2. <span data-ttu-id="d614d-155">حدد أحد العناصر، وحدد **إضافة إلى عربة التسوق**.</span><span class="sxs-lookup"><span data-stu-id="d614d-155">Select an item, and select **Add to cart**.</span></span>
3. <span data-ttu-id="d614d-156">في صفحة حقيبة التسوق، حدد **التقاط هذا** لسطر الأمر الذي أضفته للتو.</span><span class="sxs-lookup"><span data-stu-id="d614d-156">On the shopping bag page, select **Pick this up** for the order line that you just added.</span></span>
4. <span data-ttu-id="d614d-157">في مربع حوار **تحديد متجر**، أدخل **سان فرانسيسكو**، ثم حدد زر **بحث**.</span><span class="sxs-lookup"><span data-stu-id="d614d-157">In the **Select a store** dialog box, enter **San Francisco**, and then select the **Search** button.</span></span>
5. <span data-ttu-id="d614d-158">في قائمة النتائج، ابحث عن متجر سان فرانسيسكو وحدد **التقاط هنا**.</span><span class="sxs-lookup"><span data-stu-id="d614d-158">In the list of results, find the San Francisco store, and select **Pick up here**.</span></span>
6. <span data-ttu-id="d614d-159">في صفحة حقيبة التسوق، حدد **سداد مع الخروج كضيف**.</span><span class="sxs-lookup"><span data-stu-id="d614d-159">On the shopping bag page, select **Checkout as Guest**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="d614d-160">للمتابعة في عملية السداد مع الخروج، يجب أن تقبل إشعار ملفات تعريف الارتباط.</span><span class="sxs-lookup"><span data-stu-id="d614d-160">To continue with checkout, you must accept the cookie notice.</span></span> <span data-ttu-id="d614d-161">يظهر هذا الإشعار كلافتة أعلى صفحة السداد مع الخروج.</span><span class="sxs-lookup"><span data-stu-id="d614d-161">This notice appears as a banner at the top of the checkout page.</span></span>

7. <span data-ttu-id="d614d-162">بالنسبة لطريقة الدفع عبر بطاقة الائتمان، أدخل التفاصيل التالية:</span><span class="sxs-lookup"><span data-stu-id="d614d-162">For the credit card payment method, enter the following details:</span></span>

    - <span data-ttu-id="d614d-163">**اسم حامل البطاقة:**: أدخل أي اسم.</span><span class="sxs-lookup"><span data-stu-id="d614d-163">**Cardholder name:** Enter any name.</span></span>
    - <span data-ttu-id="d614d-164">**رقم البطاقة:** أدخل **4111-1111-1111-1111**.</span><span class="sxs-lookup"><span data-stu-id="d614d-164">**Card number:** Enter **4111-1111-1111-1111**.</span></span>
    - <span data-ttu-id="d614d-165">**تاريخ انتهاء الصلاحية:** أدخل **10/20**.</span><span class="sxs-lookup"><span data-stu-id="d614d-165">**Expiration date:** Enter **10/20**.</span></span>
    - <span data-ttu-id="d614d-166">**رمز قيمة التحقق من صحة بطاقة الائتمان (CVV):** أدخل **737**.</span><span class="sxs-lookup"><span data-stu-id="d614d-166">**Card verification value (CVV) code:** Enter **737**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="d614d-167">لا تحاول أبدا، تحت أي ظرف من الظروف، استخدام معلومات بطاقة الائتمان الفعلية في موقع الاختبار.</span><span class="sxs-lookup"><span data-stu-id="d614d-167">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

8. <span data-ttu-id="d614d-168">تابع عملية السداد مع الخروج من خلال إدخال تفاصيل عنوان الفوترة، ثم حدد **حفظ واستمرار**.</span><span class="sxs-lookup"><span data-stu-id="d614d-168">Continue with checkout by entering details of the billing address, and then select **Save and continue**.</span></span>
9. <span data-ttu-id="d614d-169">عندما يكون الأمر جاهزًا للتقديم، حدد **سداد مع الخروج**.</span><span class="sxs-lookup"><span data-stu-id="d614d-169">When the order is ready to be placed, select **Checkout**.</span></span>

### <a name="synchronize-online-orders-to-the-back-office"></a><span data-ttu-id="d614d-170">مزامنة الأوامر على الإنترنت مع مكتب الدعم</span><span class="sxs-lookup"><span data-stu-id="d614d-170">Synchronize online orders to the back office</span></span>

<span data-ttu-id="d614d-171">لمزيد من المعلومات حول كيفية مزامنة الطلبات على الإنترنت، راجع [نشر المبيعات على الإنترنت والمدفوعات](./tasks/posting-online-sales-payments.md).</span><span class="sxs-lookup"><span data-stu-id="d614d-171">For information about how to synchronize online orders, see [Posting of online sales and payments](./tasks/posting-online-sales-payments.md).</span></span>

### <a name="pick-up-an-order-in-the-store"></a><span data-ttu-id="d614d-172">التقاط أمر من المتجر</span><span class="sxs-lookup"><span data-stu-id="d614d-172">Pick up an order in the store</span></span>

1. <span data-ttu-id="d614d-173">سجل الدخول إلى نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="d614d-173">Sign in to the POS.</span></span>
2. <span data-ttu-id="d614d-174">في شاشة **الترحيب**، حدد **استيفاء الأمر**</span><span class="sxs-lookup"><span data-stu-id="d614d-174">On the **Welcome** screen, select **Order fulfillment**</span></span>
3. <span data-ttu-id="d614d-175">في قائمة العناصر للالتقاط، حدد السطر من الأمر الذي تم تقديمه على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="d614d-175">In the list of items for pickup, select the line from the order that was placed online.</span></span>
4. <span data-ttu-id="d614d-176">أثناء تحديد سطر الأمر، حدد **التقاط**.</span><span class="sxs-lookup"><span data-stu-id="d614d-176">While the order line is selected, select **Pick up**.</span></span>

    <span data-ttu-id="d614d-177">تتم إضافة عنصر السطر إلى شاشة المعاملة، ويظهر **$0.00** كالرصيد المستحق.</span><span class="sxs-lookup"><span data-stu-id="d614d-177">The line item is added to the transaction screen, and **$0.00** is shown as the balance that is due.</span></span>

5. <span data-ttu-id="d614d-178">حدد الرصيد المستحق بقية **$0.00**، أو حدد أي طريقة دفع لختام المعاملة.</span><span class="sxs-lookup"><span data-stu-id="d614d-178">Select the balance due of **$0.00**, or select any payment method to conclude the transaction.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="d614d-179">استكشاف الأخطاء وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="d614d-179">Troubleshooting</span></span>

### <a name="online-orders-that-are-retrieved-in-the-pos-have-a-non-zero-balance-due"></a><span data-ttu-id="d614d-180">الطلبات على الإنترنت التي تم استردادها في نقطة البيع برصيد مستحق غير صفر</span><span class="sxs-lookup"><span data-stu-id="d614d-180">Online orders that are retrieved in the POS have a non-zero balance due</span></span>

<span data-ttu-id="d614d-181">عند استرداد طلب للانتقاء في المتجر، إذا كان الرصيد المستحق ليس 0 (صفر)، تأكد من أنه يجري استخدام Modern POS، وأن محطة الأجهزة نشطة.</span><span class="sxs-lookup"><span data-stu-id="d614d-181">When an order is retrieved for in-store pickup, if the balance due isn't 0 (zero), make sure that Modern POS is being used, and that the hardware station is active.</span></span> <span data-ttu-id="d614d-182">في حالة استخدام Cloud POS أو Modern POS for iOS، تأكد من أن محطة الأجهزة نشطة.</span><span class="sxs-lookup"><span data-stu-id="d614d-182">If Cloud POS or Modern POS for iOS is being used, make sure that a shared hardware station is active.</span></span> <span data-ttu-id="d614d-183">بعض أشكال محطات الأجهزة النشطة تكون مطلوبة لاسترداد المدفوعات التي تتم عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="d614d-183">Some form of active hardware station is required to retrieve payments that were made online.</span></span>

### <a name="general-issues-with-payment-capture"></a><span data-ttu-id="d614d-184">المشكلات العامة مع التقاط الدفع</span><span class="sxs-lookup"><span data-stu-id="d614d-184">General issues with payment capture</span></span>

<span data-ttu-id="d614d-185">مع كافة المشكلات العامة، يجب دائمًا أن تراجع سجلات الأحداث الخاصة بـ Modern POS محطة الأجهزة لـ Internet Information Services (IIS) كخطوة أولى.</span><span class="sxs-lookup"><span data-stu-id="d614d-185">For all general issues, you should always consult the Modern POS or Internet Information Services (IIS) Hardware Station event logs as a first step.</span></span> <span data-ttu-id="d614d-186">يمكنك العثور على هذه السجلات تحت العُقد التالية في سجل أحداث Windows:</span><span class="sxs-lookup"><span data-stu-id="d614d-186">You can find these logs under the following nodes in the Windows event log:</span></span>

- <span data-ttu-id="d614d-187">سجلات الخدمات والتطبيقات \> Microsoft \> Dynamics \> Commerce-ModernPOS</span><span class="sxs-lookup"><span data-stu-id="d614d-187">Application and Services Logs \> Microsoft \> Dynamics \> Commerce-ModernPOS</span></span>
- <span data-ttu-id="d614d-188">سجلات الخدمات والتطبيقات \> Microsoft \> Dynamics \> Commerce-محطة الأجهزة</span><span class="sxs-lookup"><span data-stu-id="d614d-188">Application and Services Logs \> Microsoft \> Dynamics \> Commerce-Hardware Station</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d614d-189">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="d614d-189">Additional resources</span></span>

[<span data-ttu-id="d614d-190">نظرة عامة على بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="d614d-190">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="d614d-191">توفير بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="d614d-191">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="d614d-192">تكوين الميزات الاختيارية لبيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="d614d-192">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="d614d-193">الأسئلة الشائعة حول بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="d614d-193">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="d614d-194">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="d614d-194">Microsoft Lifecycle Services (LCS)</span></span>](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="d614d-195">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="d614d-195">Retail Cloud Scale Unit (RCSU)</span></span>](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="d614d-196">مدخل Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="d614d-196">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="d614d-197">موقع ويب Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="d614d-197">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="d614d-198">موصل مدفوعات Adyen</span><span class="sxs-lookup"><span data-stu-id="d614d-198">Adyen payment connector</span></span>](./dev-itpro/adyen-connector.md?tabs=8-1-3)

[<span data-ttu-id="d614d-199">حفظ وسائل الدفع عبر الإنترنت باستخدام موصل Adyen</span><span class="sxs-lookup"><span data-stu-id="d614d-199">Saving online payment instruments with the Adyen connector</span></span>](./dev-itpro/adyen-connector-listpi.md)

[<span data-ttu-id="d614d-200">نظرة عامة على مدفوعات القنوات متعددة الاتجاهات</span><span class="sxs-lookup"><span data-stu-id="d614d-200">Omni-channel payments overview</span></span>](./omni-channel-payments.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]