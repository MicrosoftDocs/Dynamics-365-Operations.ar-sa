--- 
title: "إعداد شركات الشحن"
description: "يصف هذا الإجراء كيفية إعداد شركة الشحن‬ وتعريف تفاصيل مثل الخدمة ووضع الشحن وطريقة الدفع للنقل وقيود النقل وسعر الشحن."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: af23cc5e7018e5ea5aef2ad7cb70b4f4994488cc
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="0b5cb-103">إعداد شركات الشحن</span><span class="sxs-lookup"><span data-stu-id="0b5cb-103">Set up shipping carriers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0b5cb-104">يصف هذا الإجراء كيفية إعداد شركة الشحن‬ وتعريف تفاصيل مثل الخدمة ووضع الشحن وطريقة الدفع للنقل وقيود النقل وسعر الشحن.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-104">This procedure shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="0b5cb-105">بإمكان منسق النقل عندئذٍ تعيين شركة شحن إلى حمولة صادرة أو واردة.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="0b5cb-106">إنشاء شركة شحن جديدة</span><span class="sxs-lookup"><span data-stu-id="0b5cb-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="0b5cb-107">انتقل إلى إدارة النقل > الإعداد > شركات النقل > شركات الشحن.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-107">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="0b5cb-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="0b5cb-108">Click New.</span></span>
3. <span data-ttu-id="0b5cb-109">في الحقل "شركة الشحن‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-109">In the Shipping carrier field, type a value.</span></span>
4. <span data-ttu-id="0b5cb-110">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="0b5cb-111">في الحقل "الوضع‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-111">In the Mode field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="0b5cb-112">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="0b5cb-113">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-113">In the list, click the link in the selected row.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="0b5cb-114">ملء المعلومات العامة لشركة الشحن</span><span class="sxs-lookup"><span data-stu-id="0b5cb-114">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="0b5cb-115">بدّل توسيع المقطع "نظرة عامة‬".</span><span class="sxs-lookup"><span data-stu-id="0b5cb-115">Toggle the expansion of the Overview section.</span></span>
2. <span data-ttu-id="0b5cb-116">حدد خانة الاختيار "تنشيط شركة الشحن‬" أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-116">Check or uncheck the Activate shipping carrier checkbox.</span></span>
3. <span data-ttu-id="0b5cb-117">في الحقل "المورّد‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-117">In the Vendor field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="0b5cb-118">حدد حساب المورّد الذي تريد تعيين شركة الشحن له.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-118">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="0b5cb-119">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-119">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="0b5cb-120">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-120">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="0b5cb-121">في الحقل "نوع طريقة الدفع للنقل"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-121">In the Transportation tender type field, select an option.</span></span>
    * <span data-ttu-id="0b5cb-122">حدد "يدوي" لاستخدام الصفحة "طريقة الدفع للنقل‬"، أو حدد "EDI" لتحديث طريقة الدفع باستخدام التبادل الإلكتروني للبيانات (EDI).</span><span class="sxs-lookup"><span data-stu-id="0b5cb-122">Select Manual to use the Transportation Tender page, or select EDI to update the tender by using Electronic Data Interchange (EDI).</span></span>  
7. <span data-ttu-id="0b5cb-123">حدد خانة الاختيار "تنشيط تقييم شركة النقل‬‬" أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-123">Check or uncheck the Activate carrier rating checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="0b5cb-124">إنشاء الخدمات الضرورية لشركة الشحن</span><span class="sxs-lookup"><span data-stu-id="0b5cb-124">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="0b5cb-125">بدّل توسيع المقطع "الخدمات‬".</span><span class="sxs-lookup"><span data-stu-id="0b5cb-125">Toggle the expansion of the Services section.</span></span>
2. <span data-ttu-id="0b5cb-126">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="0b5cb-126">Click New.</span></span>
3. <span data-ttu-id="0b5cb-127">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-127">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="0b5cb-128">في الحقل "خدمة الناقل‬‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-128">In the Carrier service field, type a value.</span></span>
5. <span data-ttu-id="0b5cb-129">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-129">In the Name field, type a value.</span></span>
6. <span data-ttu-id="0b5cb-130">في الحقل "أسلوب النقل‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-130">In the Transportation method field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="0b5cb-131">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-131">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="0b5cb-132">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-132">In the list, click the link in the selected row.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="0b5cb-133">إعداد عنوان الناقل (اختياري)</span><span class="sxs-lookup"><span data-stu-id="0b5cb-133">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="0b5cb-134">بدّل التوسيع لمقطع "العناوين".</span><span class="sxs-lookup"><span data-stu-id="0b5cb-134">Toggle the expansion of the Addresses section.</span></span>
2. <span data-ttu-id="0b5cb-135">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="0b5cb-135">Click New.</span></span>
3. <span data-ttu-id="0b5cb-136">في الحقل "الاسم أو الوصف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-136">In the Name or description field, type a value.</span></span>
4. <span data-ttu-id="0b5cb-137">في الحقل "البلد/المنطقة‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-137">In the Country/region field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="0b5cb-138">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="0b5cb-139">في الحقل "الرمز البريدي"، انقر فوق زر القائمة المنسدلة لفتح البحث.‬</span><span class="sxs-lookup"><span data-stu-id="0b5cb-139">In the ZIP/postal code field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="0b5cb-140">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-140">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="0b5cb-141">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-141">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="0b5cb-142">في الحقل "الشارع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-142">In the Street field, type a value.</span></span>
10. <span data-ttu-id="0b5cb-143">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="0b5cb-143">Click OK.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="0b5cb-144">إعداد ملف تعريف التقييم لشركة الشحن</span><span class="sxs-lookup"><span data-stu-id="0b5cb-144">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="0b5cb-145">بدّل توسيع المقطع "ملفات تعريف التقييم‬‬".</span><span class="sxs-lookup"><span data-stu-id="0b5cb-145">Toggle the expansion of the Rating profiles section.</span></span>
2. <span data-ttu-id="0b5cb-146">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="0b5cb-146">Click New.</span></span>
3. <span data-ttu-id="0b5cb-147">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-147">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="0b5cb-148">في الحقل "ملف تعريف التقييم‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-148">In the Rating profile field, type a value.</span></span>
5. <span data-ttu-id="0b5cb-149">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-149">In the Name field, type a value.</span></span>
6. <span data-ttu-id="0b5cb-150">في الحقل "الموقع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-150">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="0b5cb-151">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-151">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="0b5cb-152">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-152">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="0b5cb-153">في الحقل "المستودع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-153">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="0b5cb-154">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-154">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="0b5cb-155">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-155">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="0b5cb-156">في الحقل "محرك الأسعار‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.‬</span><span class="sxs-lookup"><span data-stu-id="0b5cb-156">In the Rate engine field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="0b5cb-157">حدد محرك الأسعار‬ المتوافق مع العقد المبرم مع شركة الشحن.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-157">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
13. <span data-ttu-id="0b5cb-158">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-158">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="0b5cb-159">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-159">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="0b5cb-160">في الحقل "السعر الرئيسي‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.‬</span><span class="sxs-lookup"><span data-stu-id="0b5cb-160">In the Rate master field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="0b5cb-161">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-161">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="0b5cb-162">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-162">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="0b5cb-163">في الحقل "محرك وقت الانتقال‬‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.‬</span><span class="sxs-lookup"><span data-stu-id="0b5cb-163">In the Transit time engine field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="0b5cb-164">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="0b5cb-164">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="0b5cb-165">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="0b5cb-165">Click Save.</span></span>


