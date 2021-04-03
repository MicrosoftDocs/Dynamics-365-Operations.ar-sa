---
title: إنشاء سياسة المرتجعات والمبالغ المستردة لقناه وتحديثها
description: يوضح هذا الموضوع كيفيه اعداد النهج المرتجعات والمبالغ المستردة لقناه.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.openlocfilehash: 03e46a7f8d110bd9ef3b353b150116bbf8a70ad5
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478106"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a><span data-ttu-id="4be99-103">إنشاء وتحديث سياسة للمرتجعات والمبالغ المستردة لقناة</span><span class="sxs-lookup"><span data-stu-id="4be99-103">Create and update a returns and refunds policy for a channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4be99-104">يقوم سياسة إرجاع القناة في Dynamics 365 Commerce بتمكين بائعي التجزئة من تعيين عمليات تنفيذ يستطيع فيها مقدمو الدفعات معالجه إرجاع علي جهاز نقطه بيع (POS).</span><span class="sxs-lookup"><span data-stu-id="4be99-104">The channel return policy in Dynamics 365 Commerce enables retailers to set enforcements on which payment tenders can be allowed for processing a return on a point of sale (POS) device.</span></span>  

<span data-ttu-id="4be99-105">يوضح هذا الموضوع الخطوات اللازمة لإعداد سياسة المرتجعات والمبالغ المستردة لقناه.</span><span class="sxs-lookup"><span data-stu-id="4be99-105">This topic describes the steps to set up a returns and refunds policy for a channel.</span></span>

<span data-ttu-id="4be99-106">نطاق السياسة محدود حاليا بتعيين مقدمي الدفع الذي يمكن السماح بهم لأحدي القنةات.</span><span class="sxs-lookup"><span data-stu-id="4be99-106">The scope of the policy is currently limited to setting the payment tenders that can be allowed for a channel.</span></span> <span data-ttu-id="4be99-107">تستند القائمة "مسموح" علي طرق الدفع المستخدمة لاجراء الشراء.</span><span class="sxs-lookup"><span data-stu-id="4be99-107">The "allowed" list is based on the payment methods used to make the purchase.</span></span> <span data-ttu-id="4be99-108">على سبيل المثال:</span><span class="sxs-lookup"><span data-stu-id="4be99-108">For example:</span></span>

- <span data-ttu-id="4be99-109">في حاله اجراء عمليه شراء باستخدام بطاقة الهدايا ، فان نهج المتجر هو معالجه المبالغ المستردة فقط لبطاقة الهدايا الجديدة أو لتقديم ائتمان المتجر.</span><span class="sxs-lookup"><span data-stu-id="4be99-109">If a purchase was made using a gift card, the store policy is to process refunds only to a new gift card or to give store credit.</span></span> 
- <span data-ttu-id="4be99-110">إذا تم اجراء عمليه بيع بالنقد ، ستكون الخيارات التي يتم السماح بها لمبلغ مرتجع هي النقد وبطاقة الهدايا وحساب العميل ولكن بدون بطاقة ائتمان.</span><span class="sxs-lookup"><span data-stu-id="4be99-110">If a sale is made using cash, the options allowed for refund are cash, gift card, and customer account, but not credit card.</span></span> 


## <a name="enable-return-policy"></a><span data-ttu-id="4be99-111">تمكين سياسة الإرجاع</span><span class="sxs-lookup"><span data-stu-id="4be99-111">Enable return policy</span></span>

<span data-ttu-id="4be99-112">لتمكين وظيفة سياسة إرجاع القناة، قم بما يلي:</span><span class="sxs-lookup"><span data-stu-id="4be99-112">To enable the channel return policy functionality, do the following:</span></span>

1. <span data-ttu-id="4be99-113">انتقل إلى مساحة عمل **إدارة الميزات** في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4be99-113">Go to the **Feature Management** workspace in Dynamics 365 Commerce.</span></span>
2. <span data-ttu-id="4be99-114">ابحث عن ميزة **تمكين سياسات إرجاع القنوات** في قائمه أسماء الميزات.</span><span class="sxs-lookup"><span data-stu-id="4be99-114">Search for the **Enable channel return policies** feature in the list of feature names.</span></span>
3. <span data-ttu-id="4be99-115">حدد **تمكين الآن**.</span><span class="sxs-lookup"><span data-stu-id="4be99-115">Select **Enable now**.</span></span> 

## <a name="configure-return-policy"></a><span data-ttu-id="4be99-116">تكوين سياسة الإرجاع</span><span class="sxs-lookup"><span data-stu-id="4be99-116">Configure return policy</span></span>

<span data-ttu-id="4be99-117">اتبع الخطوات التالية لتكوين سياسة إرجاع لمتجر البيع بالتجزئة أو قناه البيع بالتجزئة عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="4be99-117">Follow these steps to configure a return policy for a retail store or online retail channel.</span></span>

1. <span data-ttu-id="4be99-118">انتقل إلى  **البيع بالتجزئة والتجارة** \> **إعداد القناة** \> **المرتجعات** \> **سياسة إرجاع القناة**.</span><span class="sxs-lookup"><span data-stu-id="4be99-118">Go to **Retail and Commerce** \> **Channel Setup** \> **Returns** \> **Channel return policy**.</span></span>

2. <span data-ttu-id="4be99-119">حدد **جديد** لإنشاء قالب سياسة إرجاع جديد.</span><span class="sxs-lookup"><span data-stu-id="4be99-119">Select **New** to create a new return policy template.</span></span> <span data-ttu-id="4be99-120">لاستخدام قالب موجود، حدد القالب في الجزء الأيمن.</span><span class="sxs-lookup"><span data-stu-id="4be99-120">To use an existing template, select the template in the left pane.</span></span> <span data-ttu-id="4be99-121">بالنسبة للقوالب الجديدة ، أضف اسما ووصفا يساعد في التعرف علي النهج عند تطبيقه علي القناة.</span><span class="sxs-lookup"><span data-stu-id="4be99-121">For new templates, add a name and description that will help you identify the policy when it is being applied to the channel.</span></span>

   <span data-ttu-id="4be99-122">![إضافة سياسة إرجاع جديدة](media/Return-policy-page1.png "إضافة سياسة إرجاع جديدة")</span><span class="sxs-lookup"><span data-stu-id="4be99-122">![Add new return policy](media/Return-policy-page1.png "Add new return rolicy")</span></span>
     
   
3. <span data-ttu-id="4be99-123">في قسم **طرق دفع المبلغ المستردة المسموح بها**، حدد مقدمي دفع الإرجاع **المسموح بهم** والمحددين لكل طريقه دفع.</span><span class="sxs-lookup"><span data-stu-id="4be99-123">In the **Allowed refund payment methods** section, define **Allowed** return payment tenders that are specific to each payment method.</span></span>
   <span data-ttu-id="4be99-124">![إضافة طرق الدفع](media/Return-policy-page2.PNG "تعيين طرق الدفع المسموح بها لكل نوع دفع")</span><span class="sxs-lookup"><span data-stu-id="4be99-124">![Add payment methods](media/Return-policy-page2.PNG "Set allowed payment methods per payment type")</span></span>
   
    > [!IMPORTANT]
    > - <span data-ttu-id="4be99-125">يتم اشتقاق طرق الدفع من طرق الدفع المعينة للمؤسسة.</span><span class="sxs-lookup"><span data-stu-id="4be99-125">The payment methods are derived from the payment methods set for the organization.</span></span>
    > - <span data-ttu-id="4be99-126">ستؤدي أضافه نوع طريقه دفع الإرجاع المسموح به لكل طريقه دفع مدرجه إلى التاكد من امكانيه اجراء الإرجاع إلى نوع طريقه دفع الإرجاع المسموح به.</span><span class="sxs-lookup"><span data-stu-id="4be99-126">Adding an allowed return tender type for each listed payment method will ensure that returns can be made to the allowed return tender type.</span></span>
    
4. <span data-ttu-id="4be99-127">اربط قالب سياسة الدفع بالمتاجر حيث سيتم استخدامه.</span><span class="sxs-lookup"><span data-stu-id="4be99-127">Associate the return policy template with the stores where it will be used.</span></span> <span data-ttu-id="4be99-128">حدد **إضافة** في علامة التبويب **قنوات البيع بالتجزئة** وقم بإقران القنوات المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="4be99-128">Select **Add** in the **Retail Channels** tab and associate the available channels.</span></span> 

    - <span data-ttu-id="4be99-129">في مربع الحوار **اختيار عُقد المؤسسة‬**، حدد المتاجر والمناطق والمؤسسات التي يجب ربط القالب بها.</span><span class="sxs-lookup"><span data-stu-id="4be99-129">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>
    - <span data-ttu-id="4be99-130">يمكن ربط قالب سياسة إرجاع واحد بكل متجر.</span><span class="sxs-lookup"><span data-stu-id="4be99-130">Only one return policy template can be associated with each store.</span></span>
    - <span data-ttu-id="4be99-131">استخدم أزرار الأسهم لتحديد المتاجر أو المناطق أو المؤسسات.</span><span class="sxs-lookup"><span data-stu-id="4be99-131">Use the arrow buttons to select stores, regions, or organizations.</span></span>
    - <span data-ttu-id="4be99-132">سيكون تاريخ سريان السياسة هو التاريخ الذي يتم فيه تطبيق السياسات علي القناات ومهام القناات التي يتم تشغيلها.</span><span class="sxs-lookup"><span data-stu-id="4be99-132">The effective date on the policy will be the date on which the policies are applied to the channels and the channel jobs are run.</span></span> 

    <span data-ttu-id="4be99-133">![اختيار مربع حوار عُقد المؤسسة](media/Return-policy-page3.PNG "اختيار مربع حوار عُقد المؤسسة")</span><span class="sxs-lookup"><span data-stu-id="4be99-133">![Choose organization nodes dialog box](media/Return-policy-page3.PNG "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="4be99-134">في صفحة **جدول التوزيع**، قم بتشغيل المهمة **1070** لجعل سياسة إرجاع القناة متوفرة لنقطه البيع.</span><span class="sxs-lookup"><span data-stu-id="4be99-134">On the **Distribution schedule** page, run the **1070** job to make the channel return policy available to the POS.</span></span>

## <a name="preview-the-channel-return-policy-in-the-pos"></a><span data-ttu-id="4be99-135">معاينه سياسة إرجاع القناة في نقطه البيع</span><span class="sxs-lookup"><span data-stu-id="4be99-135">Preview the channel return policy in the POS</span></span>

<span data-ttu-id="4be99-136">اتبع الخطوات الواردة في أحد الامثله التالية لعرض أنواع طرق دفع الإرجاع المسموح بها في نقطه البيع.</span><span class="sxs-lookup"><span data-stu-id="4be99-136">Follow the steps in either of the following examples to view the allowed return tender types in POS.</span></span>

1. <span data-ttu-id="4be99-137">سجل الدخول إلى نقطه البيع ككاشير أو مدير.</span><span class="sxs-lookup"><span data-stu-id="4be99-137">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="4be99-138">ضمن **الوردية والدرج**، حدد **إظهار دفتر اليومية**.</span><span class="sxs-lookup"><span data-stu-id="4be99-138">Under **Shift and Drawer**, select **Show journal**.</span></span>
3. <span data-ttu-id="4be99-139">حدد الحركة التي تعد جزءا من الإرجاع.</span><span class="sxs-lookup"><span data-stu-id="4be99-139">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="4be99-140">حدد الأصناف التي سيتم الدفع بالمبلغ المرتجع ، ثم اختر طريقه الدفع.</span><span class="sxs-lookup"><span data-stu-id="4be99-140">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="4be99-141">إذا كانت طريقه دفع الدفع المحددة موجودة في قائمه أنواع طرق دفع العائد المسموح بها ، فيمكن للكاشير إكمال الحركة.</span><span class="sxs-lookup"><span data-stu-id="4be99-141">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="4be99-142">في حاله عدم السماح بطريقه دفع الدفع المحددة ، يتم عرض رسالة خطا.</span><span class="sxs-lookup"><span data-stu-id="4be99-142">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="4be99-143">حدد **المبلغ المستحق** لعرض قائمه بكافة أنواع طرق دفع الإرجاع المسموح بها.</span><span class="sxs-lookup"><span data-stu-id="4be99-143">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="4be99-144">-أو -</span><span class="sxs-lookup"><span data-stu-id="4be99-144">-or-</span></span>

1. <span data-ttu-id="4be99-145">سجل الدخول إلى نقطه البيع ككاشير أو مدير.</span><span class="sxs-lookup"><span data-stu-id="4be99-145">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="4be99-146">حدد **حركة الإرجاع** وأدخل معرف الإيصال باستخدام الفحص الخاص بالكود الشريطي أو بالإدخال اليدوي.</span><span class="sxs-lookup"><span data-stu-id="4be99-146">Select **Return Transaction** and enter the receipt ID using a barcode scan or by manual entry.</span></span> 
3. <span data-ttu-id="4be99-147">حدد الحركة التي تعد جزءا من الإرجاع.</span><span class="sxs-lookup"><span data-stu-id="4be99-147">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="4be99-148">حدد الأصناف التي سيتم الدفع بالمبلغ المرتجع ، ثم اختر طريقه الدفع.</span><span class="sxs-lookup"><span data-stu-id="4be99-148">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="4be99-149">إذا كانت طريقه دفع الدفع المحددة موجودة في قائمه أنواع طرق دفع العائد المسموح بها ، فيمكن للكاشير إكمال الحركة.</span><span class="sxs-lookup"><span data-stu-id="4be99-149">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="4be99-150">في حاله عدم السماح بطريقه دفع الدفع المحددة ، يتم عرض رسالة خطا.</span><span class="sxs-lookup"><span data-stu-id="4be99-150">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="4be99-151">حدد **المبلغ المستحق** لعرض قائمه بكافة أنواع طرق دفع الإرجاع المسموح بها.</span><span class="sxs-lookup"><span data-stu-id="4be99-151">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="4be99-152">![المبلغ المسترد غير مسموح به](media/Return-policy-page6.png "نوع المبلغ المسترد غير مسموح به")</span><span class="sxs-lookup"><span data-stu-id="4be99-152">![Refund not allowed](media/Return-policy-page6.png "Refund type not allowed")</span></span>



<span data-ttu-id="4be99-153">![قائمة طرق الدفع](media/Return-policy-page5.PNG "أنواع المبلغ المسترد المسموح بها")</span><span class="sxs-lookup"><span data-stu-id="4be99-153">![List of payment methods](media/Return-policy-page5.PNG "Refund types allowed")</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
