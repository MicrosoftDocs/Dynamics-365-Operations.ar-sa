---
title: دعم ميزة الضريبة لأوامر التحويل
description: يوضح هذا الموضوع الدعم الجديد لميزه الضريبة لأوامر التحويل باستخدام خدمه حساب الضريبة.
author: kailiang
ms.date: 03/10/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 55597e4f0f40677e793b4c182e4b0ced01057751
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832551"
---
# <a name="tax-feature-support-for-transfer-orders"></a><span data-ttu-id="257f2-103">دعم ميزة الضريبة لأوامر التحويل</span><span class="sxs-lookup"><span data-stu-id="257f2-103">Tax feature support for transfer orders</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="257f2-104">يوفر هذا الموضوع معلومات حول حساب الضريبة وتكامل الترحيل في أوامر التحويل.</span><span class="sxs-lookup"><span data-stu-id="257f2-104">This topic provides information about tax calculation and posting integration in transfer orders.</span></span> <span data-ttu-id="257f2-105">تتيح هذه الوظيفة اعداد حساب ضريبة وترحيلها في أوامر التحويل الخاصة بتحويلات المخزون.</span><span class="sxs-lookup"><span data-stu-id="257f2-105">This functionality lets you set up tax calculation and posting in transfer orders for stock transfers.</span></span> <span data-ttu-id="257f2-106">بموجب لوائح ضريبة القيمة المضافة (VAT) الخاصة بالاتحاد الأوروبي (EU)، تعتبر تحويلات الأسهم التوريد داخل المجتمع وعمليات الاستحواذ داخل المجتمع.</span><span class="sxs-lookup"><span data-stu-id="257f2-106">Under European Union (EU) value-added tax (VAT) regulations, stock transfers are considered intra-community supply and intra-community acquisitions.</span></span>

<span data-ttu-id="257f2-107">لتكوين هذه الوظيفة واستخدامها، يجب إكمال ثلاث خطوات أساسيه:</span><span class="sxs-lookup"><span data-stu-id="257f2-107">To configure and use this functionality, you must complete three main steps:</span></span>

1. <span data-ttu-id="257f2-108">**إعداد RCS:** في Regulatory Configuration Service، قم بإعداد ميزة الضرائب وأكواد الضرائب وقابلية تطبيق أكواد الضرائب لتحديد رمز الضريبة في أوامر التحويل.</span><span class="sxs-lookup"><span data-stu-id="257f2-108">**RCS setup:** In Regulatory Configuration Service, set up the tax feature, tax codes, and tax codes applicability for tax code determination in transfer orders.</span></span>
2. <span data-ttu-id="257f2-109">**إعداد Finance:** في Microsoft Dynamics 365 Finance، قم بتشغيل ميزة **الضريبة في أمر التحويل**، وقم بإعداد معلمات خدمة الضرائب للمخزون، وقم بإعداد معلمات الضرائب الأساسية.</span><span class="sxs-lookup"><span data-stu-id="257f2-109">**Finance setup:** In Microsoft Dynamics 365 Finance, turn on the **Tax in transfer order** feature, set up the tax service parameters for inventory, and set up core tax parameters.</span></span>
3. <span data-ttu-id="257f2-110">**إعداد المخزون:** قم باعداد تكوين المخزون لحركات أمر التحويل.</span><span class="sxs-lookup"><span data-stu-id="257f2-110">**Inventory setup:** Set up the inventory configuration for transfer order transactions.</span></span>

## <a name="set-up-rcs-for-tax-and-transfer-order-transactions"></a><span data-ttu-id="257f2-111">اعداد RCS لحركات أوامر التحويل والضريبة</span><span class="sxs-lookup"><span data-stu-id="257f2-111">Set up RCS for tax and transfer order transactions</span></span>

<span data-ttu-id="257f2-112">اتبع هذه الخطوات لاعداد الضريبة المضمنة في أمر تحويل.</span><span class="sxs-lookup"><span data-stu-id="257f2-112">Follow these steps to set up the tax that is involved in a transfer order.</span></span> <span data-ttu-id="257f2-113">في المثال الموضح هنا، يكون أمر التحويل من هولندا إلى بلجيكا.</span><span class="sxs-lookup"><span data-stu-id="257f2-113">In the example that is shown here, the transfer order is from the Netherlands to Belgium.</span></span>

1. <span data-ttu-id="257f2-114">في صفحة **ميزات الضريبة**، في علامة التبويب **الإصدارات**، حدد إصدار ميزة مسودة، ثم حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="257f2-114">On the **Tax features** page, on the **Versions** tab, select the draft feature version, and then select **Edit**.</span></span>

    ![تحديد تحرير](../media/image1.png)

2. <span data-ttu-id="257f2-116">في صفحة **إعداد ميزات الضريبة**، في علامة التبويب **أكواد الضرائب**، وحدد **إضافة** لإنشاء أكواد ضريبة جديدة.</span><span class="sxs-lookup"><span data-stu-id="257f2-116">On the **Tax features setup** page, on the **Tax codes** tab, select **Add** to create new tax codes.</span></span> <span data-ttu-id="257f2-117">في هذا المثال، يتم إنشاء ثلاثة أكواد ضريبية: **NL-Exempt**، و **BE-RC-21**، و **BE-RC+21**.</span><span class="sxs-lookup"><span data-stu-id="257f2-117">For this example, three tax codes are created: **NL-Exempt**, **BE-RC-21**, and **BE-RC+21**.</span></span>

    - <span data-ttu-id="257f2-118">عندما يتم شحن أمر تحويل من مستودع في هولندا، فإنه يتم تطبيق رمز ضريبة القيمة المضافة الهولندي المُعفى من ضريبة القيمة المضافة (**NL-Exempt**).</span><span class="sxs-lookup"><span data-stu-id="257f2-118">When a transfer order is shipped from a warehouse in the Netherlands, the Netherlands VAT exempted tax code (**NL-Exempt**) is applied.</span></span>
      
        <span data-ttu-id="257f2-119">أنشئ كود الضريبة **NL-Exempt**.</span><span class="sxs-lookup"><span data-stu-id="257f2-119">Create the tax code **NL-Exempt**.</span></span>
        1. <span data-ttu-id="257f2-120">حدد **إضافة**، وأدخل **NL-Exempt** في حقل **كود الضريبة**.</span><span class="sxs-lookup"><span data-stu-id="257f2-120">Select **Add**, enter **NL-Exempt** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="257f2-121">حدد **حسب المبلغ الصافي** في حقل **مكون الضريبة**.</span><span class="sxs-lookup"><span data-stu-id="257f2-121">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="257f2-122">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="257f2-122">Select **Save**.</span></span>
        4. <span data-ttu-id="257f2-123">حدد **إضافة** في جدول **المعدل**.</span><span class="sxs-lookup"><span data-stu-id="257f2-123">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="257f2-124">قم بتبديل **معفى** إلى **نعم** في قسم **عام**.</span><span class="sxs-lookup"><span data-stu-id="257f2-124">Swtich **Is Exempt** to **Yes** in the **General** section.</span></span>

        ![كود ضريبة NL-Exempt](../media/image2.png)

    - <span data-ttu-id="257f2-126">عند استلام أمر تحويل في مستودع بلجيكا، يتم تطبيق آلية الاحتساب العكسي باستخدام أكواد الضرائب **BE-RC-21** و **BE-RC+21**.</span><span class="sxs-lookup"><span data-stu-id="257f2-126">When a transfer order is received at a Belgium warehouse, the reverse charge mechanism is applied by using the **BE-RC-21** and **BE-RC+21** tax codes.</span></span>
        
        <span data-ttu-id="257f2-127">أنشئ كود الضريبة **BE-RC-21**.</span><span class="sxs-lookup"><span data-stu-id="257f2-127">Create the tax code **BE-RC-21**.</span></span>      
        1. <span data-ttu-id="257f2-128">حدد **إضافة**، وأدخل **BE-RC-21** في حقل **كود الضريبة**.</span><span class="sxs-lookup"><span data-stu-id="257f2-128">Select **Add**, enter **BE-RC-21** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="257f2-129">حدد **حسب المبلغ الصافي** في حقل **مكون الضريبة**.</span><span class="sxs-lookup"><span data-stu-id="257f2-129">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="257f2-130">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="257f2-130">Select **Save**.</span></span>
        4. <span data-ttu-id="257f2-131">حدد **إضافة** في جدول **المعدل**.</span><span class="sxs-lookup"><span data-stu-id="257f2-131">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="257f2-132">أدخل **-21** في حقل **معدل الضريبة**.</span><span class="sxs-lookup"><span data-stu-id="257f2-132">Enter **-21** in the **Tax Rate** field.</span></span>
        6. <span data-ttu-id="257f2-133">قم بتبديل **رسوم عكسية** إلى **نعم** في قسم **عام**.</span><span class="sxs-lookup"><span data-stu-id="257f2-133">Swtich **Is Reverse Charge** to **Yes** in the **General** section.</span></span>
        7. <span data-ttu-id="257f2-134">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="257f2-134">Select **Save**.</span></span>

        ![كود الضريبة BE-RC-21 للرسوم العكسية](../media/image3.png)
        
        <span data-ttu-id="257f2-136">أنشئ كود الضريبة **BE-RC+21**.</span><span class="sxs-lookup"><span data-stu-id="257f2-136">Create the tax code **BE-RC+21**.</span></span>
        1. <span data-ttu-id="257f2-137">حدد **إضافة**، وأدخل **BE-RC-21** في حقل **كود الضريبة**.</span><span class="sxs-lookup"><span data-stu-id="257f2-137">Select **Add**, enter **BE-RC-21** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="257f2-138">حدد **حسب المبلغ الصافي** في حقل **مكون الضريبة**.</span><span class="sxs-lookup"><span data-stu-id="257f2-138">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="257f2-139">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="257f2-139">Select **Save**.</span></span>
        4. <span data-ttu-id="257f2-140">حدد **إضافة** في جدول **المعدل**.</span><span class="sxs-lookup"><span data-stu-id="257f2-140">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="257f2-141">أدخل **21** في حقل **معدل الضريبة**.</span><span class="sxs-lookup"><span data-stu-id="257f2-141">Enter **21** in the **Tax Rate** field.</span></span>
        6. <span data-ttu-id="257f2-142">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="257f2-142">Select **Save**.</span></span>

        ![كود الضريبة BE-RC+21 للرسوم العكسية](../media/image4.png)

3. <span data-ttu-id="257f2-144">حدد إمكانية تطبيق أكواد الضرائب.</span><span class="sxs-lookup"><span data-stu-id="257f2-144">Define the applicability of the tax codes.</span></span>

    1. <span data-ttu-id="257f2-145">حدد **إدارة الأعمدة**، ثم حدد الاعمده التي ينبغي استخدامها لإنشاء جدول التطبيق.</span><span class="sxs-lookup"><span data-stu-id="257f2-145">Select **Manage columns**, and then select columns that should be used to build the applicability table.</span></span>

        > [!NOTE]
        > <span data-ttu-id="257f2-146">تأكد من إضافة عمودي **عملية الأعمال** و **اتجاهات الضرائب** إلى الجدول.</span><span class="sxs-lookup"><span data-stu-id="257f2-146">Be sure to add the **Business process** and **Tax directions** columns to the table.</span></span> <span data-ttu-id="257f2-147">ويكون كلا العمودين أساسيين لوظيفة الضرائب في أوامر التحويل.</span><span class="sxs-lookup"><span data-stu-id="257f2-147">Both columns are essential to the functionality for tax in transfer orders.</span></span>

    2. <span data-ttu-id="257f2-148">أضف قواعد إمكانية التطبيق.</span><span class="sxs-lookup"><span data-stu-id="257f2-148">Add applicability rules.</span></span> <span data-ttu-id="257f2-149">لا تترك حقول **أكواد الضريبة**، **مجموعة الضريبة**، و **مجموعة ضرائب الصنف** فارغة.</span><span class="sxs-lookup"><span data-stu-id="257f2-149">Don't leave the **Tax codes**, **Tax group**, and **Item tax group** fields blank.</span></span>
        
        <span data-ttu-id="257f2-150">أضف قاعدة جديدة لشحن أمر التحويل.</span><span class="sxs-lookup"><span data-stu-id="257f2-150">Add a new rule for transfer order shipment.</span></span>
        1. <span data-ttu-id="257f2-151">حدد **إضافة** في جدول **قواعد إمكانية التطبيق**.</span><span class="sxs-lookup"><span data-stu-id="257f2-151">Select **Add** in the **Applicability rules** table.</span></span>
        2. <span data-ttu-id="257f2-152">في حقل **عملية الأعمال**، حدد **المخزون** لجعل القاعدة قابلة للتطبيق لأمر تحويل.</span><span class="sxs-lookup"><span data-stu-id="257f2-152">In the **Business process** field, select **Inventory** to make the rule applicable for a transfer order.</span></span>
        3. <span data-ttu-id="257f2-153">في حقل **الشحن من البلد/المنطقة**، أدخل **NLD**.</span><span class="sxs-lookup"><span data-stu-id="257f2-153">In the **Ship From Country/Region** field, enter **NLD**.</span></span>
        4. <span data-ttu-id="257f2-154">في حقل **الشحن إلى البلد/المنطقة**، أدخل **BEL**.</span><span class="sxs-lookup"><span data-stu-id="257f2-154">In the **Ship To Country/Region** field, enter **BEL**.</span></span>
        5. <span data-ttu-id="257f2-155">في حقل **اتجاه الضريبة**، حدد **إخراج** لجعل القاعدة قابلة للتطبيق على شحنة أمر التحويل.</span><span class="sxs-lookup"><span data-stu-id="257f2-155">In the **Tax direction** field, select **Output** to make the rule applicable to transfer order shipment.</span></span>
        6. <span data-ttu-id="257f2-156">في حقل **أكواد الضرائب**، حدد **NL-Exempt**.</span><span class="sxs-lookup"><span data-stu-id="257f2-156">In the **Tax codes** field, select **NL-Exempt**.</span></span>
        7. <span data-ttu-id="257f2-157">في حقل **مجموعة الضريبة** و **مجموعة ضرائب الصنف**، أدخل مجموعة ضريبة المبيعات ذات الصلة ومجموعة ضريبة مبيعات الأصناف المحددة في نظام Finance الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="257f2-157">In the **Tax Group** field and the **Item Tax Group**, enter the related sales tax group and item sales tax group which are defined in your Finance system.</span></span>
        
        <span data-ttu-id="257f2-158">أضف قاعدة أخرى لاستلام أمر التحويل.</span><span class="sxs-lookup"><span data-stu-id="257f2-158">Add another rule for transfer order receipt.</span></span>
        1. <span data-ttu-id="257f2-159">حدد **إضافة** في جدول **قواعد إمكانية التطبيق**.</span><span class="sxs-lookup"><span data-stu-id="257f2-159">Select **Add** in the **Applicability rules** table.</span></span>
        2. <span data-ttu-id="257f2-160">في حقل **عملية الأعمال**، حدد **المخزون** لجعل القاعدة قابلة للتطبيق لأمر تحويل.</span><span class="sxs-lookup"><span data-stu-id="257f2-160">In the **Business process** field, select **Inventory** to make the rule applicable for a transfer order.</span></span>
        3. <span data-ttu-id="257f2-161">في حقل **الشحن من البلد/المنطقة**، أدخل **NLD**.</span><span class="sxs-lookup"><span data-stu-id="257f2-161">In the **Ship From Country/Region** field, enter **NLD**.</span></span>
        4. <span data-ttu-id="257f2-162">في حقل **الشحن إلى البلد/المنطقة**، أدخل **BEL**.</span><span class="sxs-lookup"><span data-stu-id="257f2-162">In the **Ship To Country/Region** field, enter **BEL**.</span></span>
        5. <span data-ttu-id="257f2-163">في حقل **اتجاه الضريبة**، حدد **إدخال** لجعل القاعدة قابلة للتطبيق على استلام أمر التحويل.</span><span class="sxs-lookup"><span data-stu-id="257f2-163">In the **Tax direction** field, select **Input** to make the rule applicable to transfer order receipt.</span></span>
        6. <span data-ttu-id="257f2-164">في حقل **أكواد الضرائب**، حدد **BE-RC+21** و **BE-RC-21**.</span><span class="sxs-lookup"><span data-stu-id="257f2-164">In the **Tax codes** field, select **BE-RC+21** and **BE-RC-21**.</span></span>
        7. <span data-ttu-id="257f2-165">في حقل **مجموعة الضريبة** و **مجموعة ضرائب الصنف**، أدخل مجموعة ضريبة المبيعات ذات الصلة ومجموعة ضريبة مبيعات الأصناف المحددة في نظام Finance الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="257f2-165">In the **Tax Group** field and the **Item Tax Group**, enter the related sales tax group and item sales tax group which are defined in your Finance system.</span></span>

        ![قواعد قابلية التطبيق](../media/image5.png)

4. <span data-ttu-id="257f2-167">أكمل وانشر إصدار الميزة الضريبية الجديد.</span><span class="sxs-lookup"><span data-stu-id="257f2-167">Complete and publish the new tax feature version.</span></span>

    <span data-ttu-id="257f2-168">[![تغيير حالة الإصدار الجديد](../media/image6.png)](../media/image6.png)</span><span class="sxs-lookup"><span data-stu-id="257f2-168">[![Changing the status of the new version](../media/image6.png)](../media/image6.png)</span></span>

## <a name="set-up-finance-for-transfer-order-transactions"></a><span data-ttu-id="257f2-169">إعداد Finance لحركات أوامر التحويل</span><span class="sxs-lookup"><span data-stu-id="257f2-169">Set up Finance for transfer order transactions</span></span>

<span data-ttu-id="257f2-170">اتبع هذه الخطوات لتمكين وإعداد الضرائب لأوامر التحويل.</span><span class="sxs-lookup"><span data-stu-id="257f2-170">Follow these steps to enable and set up taxes for transfer orders.</span></span>

1. <span data-ttu-id="257f2-171">في Finance، انتقل إلى **مساحات العمل** \> **إدارة الميزات**.</span><span class="sxs-lookup"><span data-stu-id="257f2-171">In Finance, go to **Workspaces** \> **Feature management**.</span></span>
2. <span data-ttu-id="257f2-172">في القائمة، ابحث عن وحدد ميزة **الضريبة في أمر التحويل**، ثم حدد **تمكين الآن** لتشغيلها.</span><span class="sxs-lookup"><span data-stu-id="257f2-172">In the list, find and select the **Tax in transfer order** feature, and then select **Enable now** to turn it on.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="257f2-173">تعتمد ميزة **الضريبة في أمر التحويل** على خدمة الضرائب بشكل كامل.</span><span class="sxs-lookup"><span data-stu-id="257f2-173">The **Tax in transfer order** feature is fully dependent on the tax service.</span></span> <span data-ttu-id="257f2-174">لذلك، لا يمكن تشغيلها إلا بعد تثبيت خدمة الضرائب.</span><span class="sxs-lookup"><span data-stu-id="257f2-174">Therefore, it can be turned on only after you've installed the tax service.</span></span>

    ![ميزة الضريبة في أمر التحويل](../media/image7.png)

3. <span data-ttu-id="257f2-176">قم بتمكين خدمة الضرائب، ثم حدد عملية أعمال **المخزون**.</span><span class="sxs-lookup"><span data-stu-id="257f2-176">Enable the tax service, and select the **Inventory** business process.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="257f2-177">يجب إكمال هذه الخطوة لكل كيان قانوني في Finance حيث تريد توفير خدمة الضرائب ووظيفة الضريبة في أوامر التحويل.</span><span class="sxs-lookup"><span data-stu-id="257f2-177">You must complete this step for each legal entity in Finance where you want the tax service and the functionality for tax in transfer orders to be available.</span></span>

    1. <span data-ttu-id="257f2-178">انتقل إلى **الضريبة** \> **إعداد** \> **تكوين الضريبة** \> **إعداد خدمة الضرائب**.</span><span class="sxs-lookup"><span data-stu-id="257f2-178">Go to **Tax** \> **Setup** \> **Tax configuration** \> **Tax service setup**.</span></span>
    2. <span data-ttu-id="257f2-179">في حقل **عملية الأعمال**، حدد **المخزون**.</span><span class="sxs-lookup"><span data-stu-id="257f2-179">In the **Business process** field, select **Inventory**.</span></span>

    ![تعيين حقل عملية الأعمال](../media/image8.png)

4. <span data-ttu-id="257f2-181">تحقق من إعداد آلية الرسوم العكسية.</span><span class="sxs-lookup"><span data-stu-id="257f2-181">Verify that the reverse charge mechanism is set up.</span></span> <span data-ttu-id="257f2-182">انتقل إلى **دفتر الأستاذ العام** \> **إعداد** \> **المعلمات**، ثم في علامة التبويب **الرسوم العكسية**، تحقق من تعيين خيار **تمكين الرسوم العكسية** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="257f2-182">Go to **General ledger** \> **Setup** \> **Parameters**, and then, on the **Reverse charge** tab, verify that the **Enable reverse charge** option is set to **Yes**.</span></span>

    ![خيار تمكين الرسوم العكسية](../media/image9.png)

5. <span data-ttu-id="257f2-184">تحقق من إعداد أكواد الضرائب ومجموعات الضرائب ومجموعات ضريبة الأصناف وأرقام تسجيل ضريبة القيمة المضافة ذات الصلة في Finance وفقًا لإرشادات خدمة الضرائب.</span><span class="sxs-lookup"><span data-stu-id="257f2-184">Verify that the related tax codes, tax groups, item tax groups, and VAT registration numbers have been set up in Finance according to the tax service guidance.</span></span>
6. <span data-ttu-id="257f2-185">قم بإعداد حساب النقل المؤقت.</span><span class="sxs-lookup"><span data-stu-id="257f2-185">Set up an interim transit account.</span></span> <span data-ttu-id="257f2-186">هذه الخطوة مطلوبة فقط عندما تكون الضريبة التي يتم تطبيقها على أمر التحويل غير قابلة للتطبيق على آلية معفاة من الضرائب أو آلية الاحتساب العكسي.</span><span class="sxs-lookup"><span data-stu-id="257f2-186">This step is required only when the tax that is applied to a transfer order isn't applicable to a tax exempted or reverse charge mechanism.</span></span>

    1. <span data-ttu-id="257f2-187">انتقل إلى **الضريبة** \> **إعداد** \> **ضريبة المبيعات** \> **مجموعات ترحيل دتر الأستاذ**.</span><span class="sxs-lookup"><span data-stu-id="257f2-187">Go to **Tax** \> **Setup** \> **Sales tax** \> **Ledger posting groups**.</span></span>
    2. <span data-ttu-id="257f2-188">في حقل **النقل المؤقت**، حدد حساب دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="257f2-188">In the **Interim transit** field, select a ledger account.</span></span>

    ![تحديد حساب النقل المؤقت](../media/image10.png)

## <a name="set-up-basic-inventory-for-transfer-order-transactions"></a><span data-ttu-id="257f2-190">إعداد المخزون الأساسي لحركات أوامر التحويل</span><span class="sxs-lookup"><span data-stu-id="257f2-190">Set up basic inventory for transfer order transactions</span></span>

<span data-ttu-id="257f2-191">اتبع هذه الخطوات لإعداد المخزون الأساسي لتمكين حركات أمر التحويل.</span><span class="sxs-lookup"><span data-stu-id="257f2-191">Follow these steps to set up basic inventory to enable transfer order transactions.</span></span>

1. <span data-ttu-id="257f2-192">أنشئ مواقع الشحن من والشحن إلى المستودعات الخاصة بك في بلدان أو مناطق مختلفة، وإضافة العنوان الأساسي لكل موقع.</span><span class="sxs-lookup"><span data-stu-id="257f2-192">Create ship-from and ship-to sites for your warehouses in different countries or regions, and add the primary address for each site.</span></span>

    1. <span data-ttu-id="257f2-193">انتقل إلى **إدارة المستودع** \> **الإعداد** \> **المستودع** \> **المواقع**.</span><span class="sxs-lookup"><span data-stu-id="257f2-193">Go to **Warehouse management** \> **Setup** \> **Warehouse** \> **Sites**.</span></span>
    2. <span data-ttu-id="257f2-194">حدد **جديد** لإنشاء الموقع الذي ستقوم بتعيينه لمستودع لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="257f2-194">Select **New** to create the site that you will assign to a warehouse later.</span></span>
    3. <span data-ttu-id="257f2-195">كرر الخطوة 2 لكافة المواقع الأخرى التي يجب إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="257f2-195">Repeat step 2 for all the other sites that you must create.</span></span>

    > [!NOTE]
    > <span data-ttu-id="257f2-196">يجب تسمية أحد المواقع التي تقوم بإنشائها **نقل**.</span><span class="sxs-lookup"><span data-stu-id="257f2-196">One of the sites that you create should be named **Transit**.</span></span> <span data-ttu-id="257f2-197">في الخطوات اللاحقة من هذا الإجراء، ستقوم بتعيين هذا الموقع إلى مستودع النقل، بحيث يمكن ترحيل إيصالات المخزون المتعلقة بالضرائب في حركات "الشحن" و "الاستلام" لأوامر التحويل.</span><span class="sxs-lookup"><span data-stu-id="257f2-197">In later steps of this procedure, you will assign this site to the transit warehouse, so that tax-related inventory vouchers can be posted in "ship" and "receive" transactions for transfer orders.</span></span> <span data-ttu-id="257f2-198">عنوان موقع النقل غير ذي صلة بحساب الضرائب.</span><span class="sxs-lookup"><span data-stu-id="257f2-198">The address of the transit site is irrelevant to tax calculation.</span></span> <span data-ttu-id="257f2-199">وبالتالي، يمكنك تركه فارغًا.</span><span class="sxs-lookup"><span data-stu-id="257f2-199">Therefore, you can leave it blank.</span></span>

    ![إعداد المواقع](../media/image11.png)

2. <span data-ttu-id="257f2-201">إنشاء مستودعات الشحن للشحن من والنقل والشحن إلى.</span><span class="sxs-lookup"><span data-stu-id="257f2-201">Create ship-from, transit, and ship-to warehouses.</span></span> <span data-ttu-id="257f2-202">ستتجاوز أي معلومات عنوان يتم الاحتفاظ بها في المستودع عنوان الموقع أثناء حساب الضريبة.</span><span class="sxs-lookup"><span data-stu-id="257f2-202">Any address information that is maintained in a warehouse will override the site address during tax calculation.</span></span>

    1. <span data-ttu-id="257f2-203">انتقل إلى **إدارة المستودعات** \> **إعداد** \> **مستودع** \> **مستودعات**.</span><span class="sxs-lookup"><span data-stu-id="257f2-203">Go to **Warehouse management** \> **Setup** \> **Warehouse** \> **Warehouses**.</span></span>
    2. <span data-ttu-id="257f2-204">حدد **جديد** لإنشاء مستودع، وتخصيصه للموقع المقابل.</span><span class="sxs-lookup"><span data-stu-id="257f2-204">Select **New** to create a warehouse, and assign it to the corresponding site.</span></span>
    3. <span data-ttu-id="257f2-205">كرر الخطوة 2 لإنشاء مستودع لكل موقع كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="257f2-205">Repeat step 2 to create a warehouse for each site as required.</span></span>

    ![إعداد المستودعات](../media/image12.png)

    > [!NOTE]
    > <span data-ttu-id="257f2-207">بالنسبة للشحن من المستودع، يجب تحديد مستودع النقل في حقل **مستودع النقل** لحركات أوامر النقل.</span><span class="sxs-lookup"><span data-stu-id="257f2-207">For a ship-from warehouse, a transit warehouse must be selected in the **Transit warehouse** field for transfer order transactions.</span></span>
    >
    > ![تحديد مستودع نقل](../media/image13.png)

3. <span data-ttu-id="257f2-209">تحقق من إعداد تكوين ترحيل المخزون لحركات أمر التحويل.</span><span class="sxs-lookup"><span data-stu-id="257f2-209">Verify that the inventory posting configuration is set up for transfer order transactions.</span></span>

    1. <span data-ttu-id="257f2-210">انتقل إلى **إدارة المخزون** \> **إعداد** \> **ترحيل** \> **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="257f2-210">Go to **Inventory management** \> **Setup** \> **Posting** \> **Posting**.</span></span>
    2. <span data-ttu-id="257f2-211">في علامة التبويب **المخزون**، تحقق من إعداد حساب دفتر أستاذ لكل من ترحيل **إصدار المخزون** و **إيصال استلام المخزون**.</span><span class="sxs-lookup"><span data-stu-id="257f2-211">On the **Inventory** tab, verify that a ledger account is set up for both **Inventory issue** and **Inventory receipt** posting.</span></span>

        ![إعداد إصدار مخزون وترحيل إيصال استلام المخزون](../media/image14.png)

    3. <span data-ttu-id="257f2-213">تحقق من إعداد حساب دفتر الأستاذ لترحيل **المدفوعات بين الوحدات**.</span><span class="sxs-lookup"><span data-stu-id="257f2-213">Verify that a ledger account is set up for **Inter-unit payable** posting.</span></span>

        ![إعداد ترحيل المدفوعات بين الوحدات](../media/image15.png)

    4. <span data-ttu-id="257f2-215">تحقق من إعداد حساب دفتر الأستاذ لترحيل **المستحقات بين الوحدات**.</span><span class="sxs-lookup"><span data-stu-id="257f2-215">Verify that a ledger account is set up for **Inter-unit receivable** posting.</span></span>

        ![إعداد ترحيل المستحقات بين الوحدات](../media/image16.png)
