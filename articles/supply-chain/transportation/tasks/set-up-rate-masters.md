---
title: إعداد السجلات الرئيسية للأسعار
description: يوضح هذا الإجراء كيفية إعداد سجل رئيسي للأسعار.
author: ShylaThompson
manager: tfehr
ms.date: 10/16/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSBreakMaster,TMSRateMaster,TMSRateMasterBase,TMSRateBaseType, TMSRouteWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 77629cbaec4c4d4608b8941e55ab23a106d38727
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233597"
---
# <a name="set-up-rate-masters"></a><span data-ttu-id="0f481-103">إعداد السجلات الرئيسية للأسعار</span><span class="sxs-lookup"><span data-stu-id="0f481-103">Set up rate masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0f481-104">يوضح هذا الإجراء كيفية إعداد سجل رئيسي للأسعار.</span><span class="sxs-lookup"><span data-stu-id="0f481-104">This procedure shows you how to set up a rate master.</span></span> <span data-ttu-id="0f481-105">تقوم إدارة اللوجستيات عادة بإعداد السجلات الرئيسية للأسعار، وفقًا للعقود الموقعة مع شركات النقل.</span><span class="sxs-lookup"><span data-stu-id="0f481-105">The logistic manager usually sets up rate masters, depending on the contracts signed with the carriers.</span></span> <span data-ttu-id="0f481-106">في هذا السيناريو، سيتم إعداد سجل رئيسي للأسعار لشركة نقل جوي.</span><span class="sxs-lookup"><span data-stu-id="0f481-106">In this scenario you will set up a rate master for an air carrier.</span></span> <span data-ttu-id="0f481-107">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="0f481-107">The demo data company used to create this procedure is USMF.</span></span>

## <a name="set-up-break-master"></a><span data-ttu-id="0f481-108">إعداد السجل الرئيسي للفاصل</span><span class="sxs-lookup"><span data-stu-id="0f481-108">Set up break master</span></span>

1. <span data-ttu-id="0f481-109">**انتقل إلى إدارة النقل > إعداد > التقييم‬ > السجل الرئيسي للفاصل**.</span><span class="sxs-lookup"><span data-stu-id="0f481-109">Go to **Transportation management > Setup > Rating > Break master**.</span></span> <span data-ttu-id="0f481-110">تستخدم أصول التوقف لتعريف بنية التسعير ونقاط التوقف الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="0f481-110">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="0f481-111">تستخدم بنية التسعير التسعير المتدرج الذي يستند إلى الأبعاد الفعلية.</span><span class="sxs-lookup"><span data-stu-id="0f481-111">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
1. <span data-ttu-id="0f481-112">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="0f481-112">Select **New**.</span></span>
1. <span data-ttu-id="0f481-113">في حقل **السجل الرئيسي للفاصل**، أدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="0f481-113">In the **Break master** field, enter a value.</span></span>
1. <span data-ttu-id="0f481-114">في حقل **الاسم**، أدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="0f481-114">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="0f481-115">في الحقل **نوع البيانات**، حدد نوع البيانات.</span><span class="sxs-lookup"><span data-stu-id="0f481-115">In the **Data type** field, select the data type.</span></span>
1. <span data-ttu-id="0f481-116">في الحقل **مقارنه**، ادخل نوع المقارنة المطلوبة (استخدام عوامل التشغيل).</span><span class="sxs-lookup"><span data-stu-id="0f481-116">In the **Comparison** field, enter the kind of comparison requested (using operators).</span></span>
1. <span data-ttu-id="0f481-117">في الحقل **وحدة الفاصل**، أدخل قيمة وحدة الفاصل.</span><span class="sxs-lookup"><span data-stu-id="0f481-117">In the **Break unit** field, enter the break unit.</span></span>
1. <span data-ttu-id="0f481-118">في القسم **التفاصيل**، قم بإنشاء أكبر عدد من الفواصل حسب الحاجة لبنيه التسعير.</span><span class="sxs-lookup"><span data-stu-id="0f481-118">In the **Details** section, create as many breaks as needed for the pricing structure.</span></span>
1. <span data-ttu-id="0f481-119">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="0f481-119">Select **Save**.</span></span>

## <a name="set-up-rate-master"></a><span data-ttu-id="0f481-120">إعداد السجل الرئيسي للأسعار‬</span><span class="sxs-lookup"><span data-stu-id="0f481-120">Set up rate master</span></span>

1. <span data-ttu-id="0f481-121">انتقل إلى **إدارة النقل > إعداد > التقييم‬ > السجل الرئيسي للأسعار**.</span><span class="sxs-lookup"><span data-stu-id="0f481-121">Go to **Transportation management > Setup > Rating > Rate master**.</span></span>
1. <span data-ttu-id="0f481-122">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="0f481-122">Select **New**.</span></span>
1. <span data-ttu-id="0f481-123">في الحقل **السجل الرئيسي للسعر**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0f481-123">In the **Rate master** field, type a value.</span></span>
1. <span data-ttu-id="0f481-124">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0f481-124">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="0f481-125">في الحقل **معرف بيانات تعريف التقييم‬**، حدد زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="0f481-125">In the **Rating metadata ID** field, select the drop-down button to open the lookup.</span></span> <span data-ttu-id="0f481-126">سيحدد معرف بيانات تعريف التقييم‬ البيانات اللازمة للسجل الرئيسي للأسعار‬، كما سيحدد بيانات التعريف المتوقعة من قبل محرك إدارة النقل باستخدام السجل الرئيسي للأسعار هذا.</span><span class="sxs-lookup"><span data-stu-id="0f481-126">The rating metadata ID will determine the data needed for the rate master, as it defines the metadata expected by the transportation management engine using this rate master.</span></span>  
1. <span data-ttu-id="0f481-127">لهذا المثال، حدد الخيار P2P.</span><span class="sxs-lookup"><span data-stu-id="0f481-127">For this example, select the P2P option.</span></span> <span data-ttu-id="0f481-128">وقد تم تعريفها بالفعل في بيانات العرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="0f481-128">This is already defined in the demo data.</span></span>
1. <span data-ttu-id="0f481-129">في القائمة، حدد الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="0f481-129">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="0f481-130">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="0f481-130">Select **Save**.</span></span>

## <a name="set-up-rate-base"></a><span data-ttu-id="0f481-131">إعداد قاعدة الأسعار</span><span class="sxs-lookup"><span data-stu-id="0f481-131">Set up rate base</span></span>

1. <span data-ttu-id="0f481-132">حدد **قاعدة الأسعار**.</span><span class="sxs-lookup"><span data-stu-id="0f481-132">Select **Rate base**.</span></span>
    * <span data-ttu-id="0f481-133">تحدد قاعدة الأسعار سعر الناقل، ويمكن استخدامها لإعداد بنية التعريفة إذ تقوم بتنظيم الأسعار في نقاط التوقف المحددة في أصل التوقف‬.</span><span class="sxs-lookup"><span data-stu-id="0f481-133">The rate base determines the rate of the carrier, and can be used to set up a tariff structure as it structures the rates in the breakpoints defined in the break master.</span></span>  
2. <span data-ttu-id="0f481-134">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="0f481-134">Select **New**.</span></span>
3. <span data-ttu-id="0f481-135">في الحقل **قاعدة الأسعار‬**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0f481-135">In the **Rate base** field, type a value.</span></span>
4. <span data-ttu-id="0f481-136">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0f481-136">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="0f481-137">في الحقل **السجل الرئيسي للفاصل**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="0f481-137">In the **Break master** field, select the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="0f481-138">تستخدم أصول التوقف لتعريف بنية التسعير ونقاط التوقف الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="0f481-138">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="0f481-139">تستخدم بنية التسعير التسعير المتدرج الذي يستند إلى الأبعاد الفعلية.</span><span class="sxs-lookup"><span data-stu-id="0f481-139">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
6. <span data-ttu-id="0f481-140">على سبيل المثال، استخدم الوزن.</span><span class="sxs-lookup"><span data-stu-id="0f481-140">For this example, use weight.</span></span> <span data-ttu-id="0f481-141">وقد تم تعريفها بالفعل في بيانات العرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="0f481-141">This is already defined in the demo data.</span></span>
7. <span data-ttu-id="0f481-142">في القائمة، حدد الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="0f481-142">In the list, select the link in the highlighted row.</span></span>
8. <span data-ttu-id="0f481-143">قم بتوسيع القسم **التفاصيل**.</span><span class="sxs-lookup"><span data-stu-id="0f481-143">Expand the **Details** section.</span></span>
9. <span data-ttu-id="0f481-144">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="0f481-144">Select **New**.</span></span>
10. <span data-ttu-id="0f481-145">في الحقل **الرمز البريدي لمكان التسليم من‬**، اكتب "30301".</span><span class="sxs-lookup"><span data-stu-id="0f481-145">In the **Drop-off Postal Code From** field, type "30301".</span></span>
11. <span data-ttu-id="0f481-146">في الحقل **الرمز البريدي لمكان التسليم إلى**، اكتب "30318".</span><span class="sxs-lookup"><span data-stu-id="0f481-146">In the **Drop-off Postal Code To** field, type "30318".</span></span>
12. <span data-ttu-id="0f481-147">في الحقل **بلد/منطقة مكان التسليم**، اكتب "USA".</span><span class="sxs-lookup"><span data-stu-id="0f481-147">In the **Drop-off Country Region** field, type "USA".</span></span>
13. <span data-ttu-id="0f481-148">في الحقل **<1.00 رطل**، اكتب "100".</span><span class="sxs-lookup"><span data-stu-id="0f481-148">In the **<1.00 Lbs** field, type "100".</span></span>
    * <span data-ttu-id="0f481-149">أدرج معدلاً بالأرطال إذا كان إجمالي وزن الحمولة أقل من 1 رطل.</span><span class="sxs-lookup"><span data-stu-id="0f481-149">Insert the rate per pounds if the total weight of the load is less than 1 pound.</span></span>  
14. <span data-ttu-id="0f481-150">في الحقل **<5.00 رطل**، اكتب "300".</span><span class="sxs-lookup"><span data-stu-id="0f481-150">In the **<5.00 Lbs** field, type "300".</span></span>
    * <span data-ttu-id="0f481-151">أدرج معدلاً بالأرطال إذا كان إجمالي وزن الحمولة أقل من 5 أرطال.</span><span class="sxs-lookup"><span data-stu-id="0f481-151">Insert the rate per pounds if the total weight of the load is less than 5 pounds.</span></span>  
15. <span data-ttu-id="0f481-152">في الحقل **<20.00 رطل**، اكتب "500".</span><span class="sxs-lookup"><span data-stu-id="0f481-152">In the **<20.00 Lbs** field, type "500".</span></span>
    * <span data-ttu-id="0f481-153">أدرج معدلاً بالأرطال إذا كان إجمالي وزن الحمولة أقل من 20 أرطال.</span><span class="sxs-lookup"><span data-stu-id="0f481-153">Insert the rate per pounds if the total weight of the load is less than 20 pounds.</span></span>  
16. <span data-ttu-id="0f481-154">في الحقل **<100.00 رطل**، اكتب "1000".</span><span class="sxs-lookup"><span data-stu-id="0f481-154">In the **<100.00 Lbs** field, type "1000".</span></span>
    * <span data-ttu-id="0f481-155">أدرج معدلاً بالأرطال إذا كان إجمالي وزن الحمولة أقل من 100 أرطال.</span><span class="sxs-lookup"><span data-stu-id="0f481-155">Insert the rate per pounds if the total weight of the load is less than 100 pounds.</span></span>  
17. <span data-ttu-id="0f481-156">في الحقل **<1,000.00 رطل**، اكتب "3000".</span><span class="sxs-lookup"><span data-stu-id="0f481-156">In the **<1,000.00 Lbs** field, type "3000".</span></span>
    * <span data-ttu-id="0f481-157">أدرج معدلاً بالأرطال إذا كان إجمالي وزن الحمولة أقل من 1000 أرطال.</span><span class="sxs-lookup"><span data-stu-id="0f481-157">Insert the rate per pounds if the total weight of the load is less than 1000 pounds.</span></span>  
18. <span data-ttu-id="0f481-158">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="0f481-158">Select **Save**.</span></span>
19. <span data-ttu-id="0f481-159">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0f481-159">Close the page.</span></span>

## <a name="assign-rate-base"></a><span data-ttu-id="0f481-160">تعيين قاعدة الأسعار</span><span class="sxs-lookup"><span data-stu-id="0f481-160">Assign rate base</span></span>

1. <span data-ttu-id="0f481-161">قم بتوسيع القسم **تعيينات قاعدة الأسعار**.</span><span class="sxs-lookup"><span data-stu-id="0f481-161">Expand the **Rate base assignments** section.</span></span>
2. <span data-ttu-id="0f481-162">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="0f481-162">Select **New**.</span></span>
    * <span data-ttu-id="0f481-163">لديك تعيينات قاعدة أسعار متعددة لكل سجل رئيسي للأسعار.</span><span class="sxs-lookup"><span data-stu-id="0f481-163">You can have several rate base assignments for each rate master.</span></span> <span data-ttu-id="0f481-164">هذا يجعل من الممكن إنشاء عدة نقاط أسعار مختلفة لكل شركة بحسب الوجهات أو الخدمات أو قواعد الأسعار المختلفة.</span><span class="sxs-lookup"><span data-stu-id="0f481-164">This makes it possible to create several different price points for each carrier depending on destinations, services, or different rate bases.</span></span> <span data-ttu-id="0f481-165">في هذا الإجراء سيتم إنشاء تعيين قاعدة أسعار واحد فقط.</span><span class="sxs-lookup"><span data-stu-id="0f481-165">In this procedure you will only create one rate base assignment.</span></span>  
3. <span data-ttu-id="0f481-166">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0f481-166">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="0f481-167">في الحقل **قاعدة الأسعار‬**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="0f481-167">In the **Rate base** field, select the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="0f481-168">في القائمة، حدد الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="0f481-168">In the list, select the link in the highlighted row.</span></span>
6. <span data-ttu-id="0f481-169">في الحقل **إلخدمة‬**، حدد زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="0f481-169">In the **Service** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="0f481-170">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="0f481-170">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="0f481-171">في القائمة، حدد الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="0f481-171">In the list, select the link in the highlighted row.</span></span>
9. <span data-ttu-id="0f481-172">في الحقل **الرمز البريدي لمكان الانتقاء‬**، اكتب "98052".</span><span class="sxs-lookup"><span data-stu-id="0f481-172">In the **Pick-up Postal Code** field, type "98052".</span></span>
    * <span data-ttu-id="0f481-173">حدد الرمز البريدي الذي يجب أن يكون تعيين قاعدة الأسعار هذا صالحًا منه.</span><span class="sxs-lookup"><span data-stu-id="0f481-173">Specify which postal code this rate base assignment should be valid from.</span></span>
10. <span data-ttu-id="0f481-174">في الحقل **البلد/المنطقة لمكان الانتقاء**، اكتب "USA".</span><span class="sxs-lookup"><span data-stu-id="0f481-174">In the **Pick-up Country Region** field, type "USA".</span></span>
11. <span data-ttu-id="0f481-175">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="0f481-175">Select **Save**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]