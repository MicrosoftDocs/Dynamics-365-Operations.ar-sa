---
title: إعداد شركات الشحن
description: يصف هذا الموضوع كيفية إعداد شركة الشحن‬ وتعريف تفاصيل مثل الخدمة ووضع الشحن وطريقة الدفع للنقل وقيود النقل وسعر الشحن.
author: ShylaThompson
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSShippingCarrierCustomerAccount,TMSCarrier
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 124f7473cbdae8890f74115d461603f50cc58be8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004867"
---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="ef002-103">إعداد شركات الشحن</span><span class="sxs-lookup"><span data-stu-id="ef002-103">Set up shipping carriers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ef002-104">يصف هذا الموضوع كيفية إعداد شركة الشحن‬ وتعريف تفاصيل مثل الخدمة ووضع الشحن وطريقة الدفع للنقل وقيود النقل وسعر الشحن.</span><span class="sxs-lookup"><span data-stu-id="ef002-104">This topic shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="ef002-105">بإمكان منسق النقل عندئذٍ تعيين شركة شحن إلى حمولة صادرة أو واردة.</span><span class="sxs-lookup"><span data-stu-id="ef002-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="ef002-106">إنشاء شركة شحن جديدة</span><span class="sxs-lookup"><span data-stu-id="ef002-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="ef002-107">انتقل إلى **جزء التنقل > إدارة النقل > الإعداد > شركات النقل > شركات الشحن**.</span><span class="sxs-lookup"><span data-stu-id="ef002-107">Go to **Navigation pane > Modules > Transportation management > Setup > Carriers > Shipping carriers**.</span></span>
2. <span data-ttu-id="ef002-108">حدد **جديد** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="ef002-108">Select **New** on the Action Pane.</span></span>
3. <span data-ttu-id="ef002-109">في الحقل **شركة الشحن‬**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ef002-109">In the **Shipping carrier** field, type a value.</span></span>
4. <span data-ttu-id="ef002-110">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ef002-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="ef002-111">في الحقل **الوضع**، حدد خيارًا من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="ef002-111">In the **Mode** field, select an option from the drop-down menu.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="ef002-112">ملء المعلومات العامة لشركة الشحن</span><span class="sxs-lookup"><span data-stu-id="ef002-112">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="ef002-113">بدّل توسيع المقطع  **نظرة عامة‬**.</span><span class="sxs-lookup"><span data-stu-id="ef002-113">Toggle the expansion of the **Overview** section.</span></span>
2. <span data-ttu-id="ef002-114">حدد خانة الاختيار **تنشيط شركة الشحن** أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="ef002-114">Check or uncheck the **Activate shipping carrier** checkbox.</span></span>
3. <span data-ttu-id="ef002-115">في الحقل **حساب المورّد**، حدد خيارًا من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="ef002-115">In the **Vendor account** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="ef002-116">حدد حساب المورّد الذي تريد تعيين شركة الشحن له.</span><span class="sxs-lookup"><span data-stu-id="ef002-116">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="ef002-117">في الحقل **نوع طريقة الدفع للنقل**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="ef002-117">In the **Transportation tender type** field, select an option.</span></span> <span data-ttu-id="ef002-118">حدد **يدوي** لاستخدام الصفحة "طريقة الدفع للنقل‬"، أو حدد **EDI** لتحديث طريقة الدفع باستخدام التبادل الإلكتروني للبيانات (EDI).</span><span class="sxs-lookup"><span data-stu-id="ef002-118">Select **Manual** to use the Transportation Tender page, or select **EDI** to update the tender by using Electronic Data Interchange (EDI).</span></span>  
5. <span data-ttu-id="ef002-119">حدد خانة الاختيار **تنشيط تقييم شركة النقل‬‬** أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="ef002-119">Check or uncheck the **Activate carrier rating** checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="ef002-120">إنشاء الخدمات الضرورية لشركة الشحن</span><span class="sxs-lookup"><span data-stu-id="ef002-120">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="ef002-121">بدّل توسيع المقطع **الخدمات‬**.</span><span class="sxs-lookup"><span data-stu-id="ef002-121">Toggle the expansion of the **Services** section.</span></span>
2. <span data-ttu-id="ef002-122">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="ef002-122">Select **New**.</span></span>
3. <span data-ttu-id="ef002-123">في الحقل **خدمة الناقل**‬‬، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ef002-123">In the **Carrier service** field, type a value.</span></span>
4. <span data-ttu-id="ef002-124">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ef002-124">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="ef002-125">في الحقل **أسلوب النقل‬**، حدد خيارًا من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="ef002-125">In the **Transportation method** field, select an option from the drop-down menu.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="ef002-126">إعداد عنوان الناقل (اختياري)</span><span class="sxs-lookup"><span data-stu-id="ef002-126">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="ef002-127">بدّل التوسيع لمقطع **العناوين**.</span><span class="sxs-lookup"><span data-stu-id="ef002-127">Toggle the expansion of the **Addresses** section.</span></span>
2. <span data-ttu-id="ef002-128">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="ef002-128">Select **New**.</span></span>
3. <span data-ttu-id="ef002-129">في الحقل **الاسم أو الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ef002-129">In the **Name or description** field, type a value.</span></span>
4. <span data-ttu-id="ef002-130">في الحقل **البلد/المنطقة**، حدد خيارًا من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="ef002-130">In the **Country/region** field, select an option from the drop-down menu.</span></span>
5. <span data-ttu-id="ef002-131">في الحقل **الرمز البريدي**، حدد خيارًا من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="ef002-131">In the **ZIP/postal code** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="ef002-132">في الحقل **الشارع**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ef002-132">In the **Street** field, type a value.</span></span>
7. <span data-ttu-id="ef002-133">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ef002-133">Select **OK**.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="ef002-134">إعداد ملف تعريف التقييم لشركة الشحن</span><span class="sxs-lookup"><span data-stu-id="ef002-134">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="ef002-135">بدّل توسيع المقطع **ملفات تعريف التقييم‬‬**.</span><span class="sxs-lookup"><span data-stu-id="ef002-135">Toggle the expansion of the **Rating profiles** section.</span></span>
2. <span data-ttu-id="ef002-136">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="ef002-136">Select **New**.</span></span>
3. <span data-ttu-id="ef002-137">في الحقل **ملف تعريف التقييم‬**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ef002-137">In the **Rating profile** field, type a value.</span></span>
4. <span data-ttu-id="ef002-138">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ef002-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="ef002-139">في الحقل **الموقع**، حدد خيارًا من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="ef002-139">In the **Site** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="ef002-140">في الحقل **المستودع**، حدد خيارًا من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="ef002-140">In the **Warehouse** field, select an option from the drop-down menu.</span></span>
7. <span data-ttu-id="ef002-141">في الحقل **محرك الأسعار**، حدد خيارًا من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="ef002-141">In the **Rate engine** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="ef002-142">حدد محرك الأسعار‬ المتوافق مع العقد المبرم مع شركة الشحن.</span><span class="sxs-lookup"><span data-stu-id="ef002-142">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
8. <span data-ttu-id="ef002-143">في الحقل **السجل الرئيسي للأسعار‬**، حدد خيارًا من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="ef002-143">In the **Rate master** field, select an option from the drop-down menu.</span></span>
9. <span data-ttu-id="ef002-144">في الحقل **محرك وقت الانتقال‬**، حدد خيارًا من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="ef002-144">In the **Transit time engine** field, select an option from the drop-down menu.</span></span>
10. <span data-ttu-id="ef002-145">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="ef002-145">Select **Save**.</span></span>

