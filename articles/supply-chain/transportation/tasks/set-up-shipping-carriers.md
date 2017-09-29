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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e27be049bebd63c9266029b8981874417a9f0a8c
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="e81c7-103">إعداد شركات الشحن</span><span class="sxs-lookup"><span data-stu-id="e81c7-103">Set up shipping carriers</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e81c7-104">يصف هذا الإجراء كيفية إعداد شركة الشحن‬ وتعريف تفاصيل مثل الخدمة ووضع الشحن وطريقة الدفع للنقل وقيود النقل وسعر الشحن.</span><span class="sxs-lookup"><span data-stu-id="e81c7-104">This procedure shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="e81c7-105">بإمكان منسق النقل عندئذٍ تعيين شركة شحن إلى حمولة صادرة أو واردة.</span><span class="sxs-lookup"><span data-stu-id="e81c7-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="e81c7-106">إنشاء شركة شحن جديدة</span><span class="sxs-lookup"><span data-stu-id="e81c7-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="e81c7-107">انتقل إلى إدارة النقل > الإعداد > شركات النقل > شركات الشحن.</span><span class="sxs-lookup"><span data-stu-id="e81c7-107">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="e81c7-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="e81c7-108">Click New.</span></span>
3. <span data-ttu-id="e81c7-109">في الحقل "شركة الشحن‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e81c7-109">In the Shipping carrier field, type a value.</span></span>
4. <span data-ttu-id="e81c7-110">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e81c7-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="e81c7-111">في الحقل "الوضع‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e81c7-111">In the Mode field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="e81c7-112">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e81c7-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="e81c7-113">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e81c7-113">In the list, click the link in the selected row.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="e81c7-114">ملء المعلومات العامة لشركة الشحن</span><span class="sxs-lookup"><span data-stu-id="e81c7-114">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="e81c7-115">بدّل توسيع المقطع "نظرة عامة‬".</span><span class="sxs-lookup"><span data-stu-id="e81c7-115">Toggle the expansion of the Overview section.</span></span>
2. <span data-ttu-id="e81c7-116">حدد خانة الاختيار "تنشيط شركة الشحن‬" أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="e81c7-116">Check or uncheck the Activate shipping carrier checkbox.</span></span>
3. <span data-ttu-id="e81c7-117">في الحقل "المورّد‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e81c7-117">In the Vendor field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="e81c7-118">حدد حساب المورّد الذي تريد تعيين شركة الشحن له.</span><span class="sxs-lookup"><span data-stu-id="e81c7-118">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="e81c7-119">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e81c7-119">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="e81c7-120">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e81c7-120">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="e81c7-121">في الحقل "نوع طريقة الدفع للنقل"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="e81c7-121">In the Transportation tender type field, select an option.</span></span>
    * <span data-ttu-id="e81c7-122">حدد "يدوي" لاستخدام الصفحة "طريقة الدفع للنقل‬"، أو حدد "EDI" لتحديث طريقة الدفع باستخدام التبادل الإلكتروني للبيانات (EDI).</span><span class="sxs-lookup"><span data-stu-id="e81c7-122">Select Manual to use the Transportation Tender page, or select EDI to update the tender by using Electronic Data Interchange (EDI).</span></span>  
7. <span data-ttu-id="e81c7-123">حدد خانة الاختيار "تنشيط تقييم شركة النقل‬‬" أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="e81c7-123">Check or uncheck the Activate carrier rating checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="e81c7-124">إنشاء الخدمات الضرورية لشركة الشحن</span><span class="sxs-lookup"><span data-stu-id="e81c7-124">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="e81c7-125">بدّل توسيع المقطع "الخدمات‬".</span><span class="sxs-lookup"><span data-stu-id="e81c7-125">Toggle the expansion of the Services section.</span></span>
2. <span data-ttu-id="e81c7-126">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="e81c7-126">Click New.</span></span>
3. <span data-ttu-id="e81c7-127">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e81c7-127">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="e81c7-128">في الحقل "خدمة الناقل‬‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e81c7-128">In the Carrier service field, type a value.</span></span>
5. <span data-ttu-id="e81c7-129">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e81c7-129">In the Name field, type a value.</span></span>
6. <span data-ttu-id="e81c7-130">في الحقل "أسلوب النقل‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e81c7-130">In the Transportation method field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="e81c7-131">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e81c7-131">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="e81c7-132">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e81c7-132">In the list, click the link in the selected row.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="e81c7-133">إعداد عنوان الناقل (اختياري)</span><span class="sxs-lookup"><span data-stu-id="e81c7-133">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="e81c7-134">بدّل التوسيع لمقطع "العناوين".</span><span class="sxs-lookup"><span data-stu-id="e81c7-134">Toggle the expansion of the Addresses section.</span></span>
2. <span data-ttu-id="e81c7-135">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="e81c7-135">Click New.</span></span>
3. <span data-ttu-id="e81c7-136">في الحقل "الاسم أو الوصف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e81c7-136">In the Name or description field, type a value.</span></span>
4. <span data-ttu-id="e81c7-137">في الحقل "البلد/المنطقة‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e81c7-137">In the Country/region field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="e81c7-138">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e81c7-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="e81c7-139">في الحقل "الرمز البريدي"، انقر فوق زر القائمة المنسدلة لفتح البحث.‬</span><span class="sxs-lookup"><span data-stu-id="e81c7-139">In the ZIP/postal code field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="e81c7-140">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e81c7-140">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="e81c7-141">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e81c7-141">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="e81c7-142">في الحقل "الشارع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e81c7-142">In the Street field, type a value.</span></span>
10. <span data-ttu-id="e81c7-143">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="e81c7-143">Click OK.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="e81c7-144">إعداد ملف تعريف التقييم لشركة الشحن</span><span class="sxs-lookup"><span data-stu-id="e81c7-144">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="e81c7-145">بدّل توسيع المقطع "ملفات تعريف التقييم‬‬".</span><span class="sxs-lookup"><span data-stu-id="e81c7-145">Toggle the expansion of the Rating profiles section.</span></span>
2. <span data-ttu-id="e81c7-146">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="e81c7-146">Click New.</span></span>
3. <span data-ttu-id="e81c7-147">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e81c7-147">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="e81c7-148">في الحقل "ملف تعريف التقييم‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e81c7-148">In the Rating profile field, type a value.</span></span>
5. <span data-ttu-id="e81c7-149">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e81c7-149">In the Name field, type a value.</span></span>
6. <span data-ttu-id="e81c7-150">في الحقل "الموقع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e81c7-150">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="e81c7-151">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e81c7-151">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="e81c7-152">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e81c7-152">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="e81c7-153">في الحقل "المستودع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e81c7-153">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="e81c7-154">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e81c7-154">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="e81c7-155">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e81c7-155">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="e81c7-156">في الحقل "محرك الأسعار‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.‬</span><span class="sxs-lookup"><span data-stu-id="e81c7-156">In the Rate engine field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="e81c7-157">حدد محرك الأسعار‬ المتوافق مع العقد المبرم مع شركة الشحن.</span><span class="sxs-lookup"><span data-stu-id="e81c7-157">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
13. <span data-ttu-id="e81c7-158">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e81c7-158">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="e81c7-159">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e81c7-159">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="e81c7-160">في الحقل "السعر الرئيسي‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.‬</span><span class="sxs-lookup"><span data-stu-id="e81c7-160">In the Rate master field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="e81c7-161">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e81c7-161">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="e81c7-162">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e81c7-162">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="e81c7-163">في الحقل "محرك وقت الانتقال‬‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.‬</span><span class="sxs-lookup"><span data-stu-id="e81c7-163">In the Transit time engine field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="e81c7-164">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e81c7-164">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="e81c7-165">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="e81c7-165">Click Save.</span></span>


