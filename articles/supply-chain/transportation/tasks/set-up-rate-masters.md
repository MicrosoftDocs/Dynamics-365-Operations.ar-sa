---
title: إعداد السجلات الرئيسية للأسعار
description: يوضح هذا الإجراء كيفية إعداد سجل رئيسي للأسعار.
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 462bfce89fa77c8830a93a22b0dd6c8c8fb2cde6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "344905"
---
# <a name="set-up-rate-masters"></a><span data-ttu-id="cc9cd-103">إعداد السجلات الرئيسية للأسعار</span><span class="sxs-lookup"><span data-stu-id="cc9cd-103">Set up rate masters</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cc9cd-104">يوضح هذا الإجراء كيفية إعداد سجل رئيسي للأسعار.</span><span class="sxs-lookup"><span data-stu-id="cc9cd-104">This procedure shows you how to set up a rate master.</span></span> <span data-ttu-id="cc9cd-105">تقوم إدارة اللوجستيات عادة بإعداد السجلات الرئيسية للأسعار، وفقًا للعقود الموقعة مع شركات النقل.</span><span class="sxs-lookup"><span data-stu-id="cc9cd-105">The logistic manager usually sets up rate masters, depending on the contracts signed with the carriers.</span></span> <span data-ttu-id="cc9cd-106">في هذا السيناريو، سيتم إعداد سجل رئيسي للأسعار لشركة نقل جوي.</span><span class="sxs-lookup"><span data-stu-id="cc9cd-106">In this scenario you will set up a rate master for an air carrier.</span></span> <span data-ttu-id="cc9cd-107">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="cc9cd-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-rate-master"></a><span data-ttu-id="cc9cd-108">إعداد السجل الرئيسي للأسعار‬</span><span class="sxs-lookup"><span data-stu-id="cc9cd-108">Set up rate master</span></span>
1. <span data-ttu-id="cc9cd-109">انتقل إلى إدارة النقل > إعداد > التقييم‬ > السجل الرئيسي للأسعار.</span><span class="sxs-lookup"><span data-stu-id="cc9cd-109">Go to Transportation management > Setup > Rating > Rate master.</span></span>
2. <span data-ttu-id="cc9cd-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="cc9cd-110">Click New.</span></span>
3. <span data-ttu-id="cc9cd-111">في الحقل "السعر الرئيسي‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="cc9cd-111">In the Rate master field, type a value.</span></span>
4. <span data-ttu-id="cc9cd-112">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="cc9cd-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="cc9cd-113">في الحقل "معرف بيانات تعريف التقييم‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="cc9cd-113">In the Rating metadata ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="cc9cd-114">سيحدد معرف بيانات تعريف التقييم‬ البيانات اللازمة للسجل الرئيسي للأسعار‬، كما سيحدد بيانات التعريف المتوقعة من قبل محرك TMS باستخدام السجل الرئيسي للأسعار هذا.</span><span class="sxs-lookup"><span data-stu-id="cc9cd-114">The rating metadata ID will determine the data needed for the rate master, as it defines the metadata expected by the TMS engine using this rate master.</span></span>  
6. <span data-ttu-id="cc9cd-115">لهذا المثال، حدد الخيار P2P.</span><span class="sxs-lookup"><span data-stu-id="cc9cd-115">For this example, select the P2P option</span></span>
7. <span data-ttu-id="cc9cd-116">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="cc9cd-116">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="cc9cd-117">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="cc9cd-117">Click Save.</span></span>

## <a name="set-up-rate-base"></a><span data-ttu-id="cc9cd-118">إعداد قاعدة الأسعار</span><span class="sxs-lookup"><span data-stu-id="cc9cd-118">Set up rate base</span></span>
1. <span data-ttu-id="cc9cd-119">انقر فوق "قاعدة الأسعار‬"</span><span class="sxs-lookup"><span data-stu-id="cc9cd-119">Click Rate base.</span></span>
    * <span data-ttu-id="cc9cd-120">تحدد قاعدة الأسعار سعر الناقل، ويمكن استخدامها لإعداد بنية التعريفة إذ تقوم بتنظيم الأسعار في نقاط التوقف المحددة في أصل التوقف‬.</span><span class="sxs-lookup"><span data-stu-id="cc9cd-120">The rate base determines the rate of the carrier, and can be used to set up a tariff structure as it structures the rates in the breakpoints defined in the break master.</span></span>  
2. <span data-ttu-id="cc9cd-121">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="cc9cd-121">Click New.</span></span>
3. <span data-ttu-id="cc9cd-122">في الحقل "قاعدة الأسعار‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="cc9cd-122">In the Rate base field, type a value.</span></span>
4. <span data-ttu-id="cc9cd-123">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="cc9cd-123">In the Name field, type a value.</span></span>
5. <span data-ttu-id="cc9cd-124">في الحقل "التوقف الرئيسي‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="cc9cd-124">In the Break master field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="cc9cd-125">تستخدم أصول التوقف لتعريف بنية التسعير ونقاط التوقف الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="cc9cd-125">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="cc9cd-126">تستخدم بنية التسعير التسعير المتدرج الذي يستند إلى الأبعاد الفعلية.</span><span class="sxs-lookup"><span data-stu-id="cc9cd-126">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
6. <span data-ttu-id="cc9cd-127">على سبيل المثال، استخدم الوزن</span><span class="sxs-lookup"><span data-stu-id="cc9cd-127">For this example, use weight</span></span>
7. <span data-ttu-id="cc9cd-128">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="cc9cd-128">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="cc9cd-129">بدّل توسيع المقطع "تفاصيل".</span><span class="sxs-lookup"><span data-stu-id="cc9cd-129">Toggle the expansion of the Details section.</span></span>
9. <span data-ttu-id="cc9cd-130">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="cc9cd-130">Click New.</span></span>
10. <span data-ttu-id="cc9cd-131">في الحقل "الرمز البريدي لمكان التسليم من‬"، اكتب "30301".</span><span class="sxs-lookup"><span data-stu-id="cc9cd-131">In the Drop-off Postal Code From field, type '30301'.</span></span>
11. <span data-ttu-id="cc9cd-132">في الحقل "الرمز البريدي لمكان التسليم إلى‬"، اكتب "30318".</span><span class="sxs-lookup"><span data-stu-id="cc9cd-132">In the Drop-off Postal Code To field, type '30318'.</span></span>
12. <span data-ttu-id="cc9cd-133">في الحقل "بلد/منطقة مكان التسليم "، اكتب "USA".</span><span class="sxs-lookup"><span data-stu-id="cc9cd-133">In the Drop-off Country Region field, type 'USA'.</span></span>
13. <span data-ttu-id="cc9cd-134">في الحقل <1.00 رطل"، اكتب "100".</span><span class="sxs-lookup"><span data-stu-id="cc9cd-134">In the <1.00 Lbs field, type '100'.</span></span>
    * <span data-ttu-id="cc9cd-135">أدرج معدلاً بالأرطال إذا كان إجمالي وزن الحمولة أقل من رطل واحد.</span><span class="sxs-lookup"><span data-stu-id="cc9cd-135">Insert the rate per lbs if the total weight of the load is less than 1 pound.</span></span>  
14. <span data-ttu-id="cc9cd-136">في < الحقل "5.00 رطل"، اكتب "300".</span><span class="sxs-lookup"><span data-stu-id="cc9cd-136">In the <5.00 Lbs field, type '300'.</span></span>
    * <span data-ttu-id="cc9cd-137">أدرج معدلاً بالأرطال إذا كان إجمالي وزن الحمولة أقل من 5 أرطال.</span><span class="sxs-lookup"><span data-stu-id="cc9cd-137">Insert the rate per lbs if the total weight of the load is less than 5 pounds.</span></span>  
15. <span data-ttu-id="cc9cd-138">في < الحقل "20.00 رطل"، اكتب "500".</span><span class="sxs-lookup"><span data-stu-id="cc9cd-138">In the <20.00 Lbs field, type '500'.</span></span>
    * <span data-ttu-id="cc9cd-139">أدرج معدلاً بالأرطال إذا كان إجمالي وزن الحمولة أقل من 20 رطلاً.</span><span class="sxs-lookup"><span data-stu-id="cc9cd-139">Insert the rate per lbs if the total weight of the load is less than 20 pounds.</span></span>  
16. <span data-ttu-id="cc9cd-140">في < الحقل "100.00 رطل"، اكتب "1000".</span><span class="sxs-lookup"><span data-stu-id="cc9cd-140">In the <100.00 Lbs field, type '1000'.</span></span>
    * <span data-ttu-id="cc9cd-141">أدرج معدلاً بالأرطال إذا كان إجمالي وزن الحمولة أقل من 100 رطل.</span><span class="sxs-lookup"><span data-stu-id="cc9cd-141">Insert the rate per lbs if the total weight of the load is less than 100 pounds.</span></span>  
17. <span data-ttu-id="cc9cd-142">في < الحقل "1,000.00 رطل"، اكتب "3000".</span><span class="sxs-lookup"><span data-stu-id="cc9cd-142">In the <1,000.00 Lbs field, type '3000'.</span></span>
    * <span data-ttu-id="cc9cd-143">أدرج معدلاً بالأرطال إذا كان إجمالي وزن الحمولة أقل من 1000 رطل.</span><span class="sxs-lookup"><span data-stu-id="cc9cd-143">Insert the rate per lbs if the total weight of the load is less than 1000 pounds.</span></span>  
18. <span data-ttu-id="cc9cd-144">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="cc9cd-144">Click Save.</span></span>
19. <span data-ttu-id="cc9cd-145">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cc9cd-145">Close the page.</span></span>

## <a name="assign-rate-base"></a><span data-ttu-id="cc9cd-146">تعيين قاعدة الأسعار</span><span class="sxs-lookup"><span data-stu-id="cc9cd-146">Assign rate base</span></span>
1. <span data-ttu-id="cc9cd-147">بدّل توسيع المقطع "تعيينات أسس الأسعار‬".</span><span class="sxs-lookup"><span data-stu-id="cc9cd-147">Toggle the expansion of the Rate base assignments section.</span></span>
2. <span data-ttu-id="cc9cd-148">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="cc9cd-148">Click New.</span></span>
    * <span data-ttu-id="cc9cd-149">لديك تعيينات قاعدة أسعار متعددة لكل سجل رئيسي للأسعار.</span><span class="sxs-lookup"><span data-stu-id="cc9cd-149">You can have several rate base assignments for each rate master.</span></span> <span data-ttu-id="cc9cd-150">هذا يجعل من الممكن إنشاء عدة نقاط أسعار مختلفة لكل شركة بحسب الوجهات أو الخدمات أو قواعد الأسعار المختلفة.</span><span class="sxs-lookup"><span data-stu-id="cc9cd-150">This makes it possible to create several different price points for each carrier depending on destinations, services, or different rate bases.</span></span> <span data-ttu-id="cc9cd-151">في هذا الإجراء سيتم إنشاء تعيين قاعدة أسعار واحد فقط.</span><span class="sxs-lookup"><span data-stu-id="cc9cd-151">In this procedure you will only create one rate base assignment.</span></span>  
3. <span data-ttu-id="cc9cd-152">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="cc9cd-152">In the Name field, type a value.</span></span>
4. <span data-ttu-id="cc9cd-153">في الحقل "قاعدة الأسعار"، انقر فوق زر القائمة المنسدلة لفتح البحث.‬</span><span class="sxs-lookup"><span data-stu-id="cc9cd-153">In the Rate base field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="cc9cd-154">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="cc9cd-154">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="cc9cd-155">في الحقل "الخدمة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="cc9cd-155">In the Service field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="cc9cd-156">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="cc9cd-156">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="cc9cd-157">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="cc9cd-157">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="cc9cd-158">في الحقل "الرمز البريدي لمكان الانتقاء‬"، اكتب "98052".</span><span class="sxs-lookup"><span data-stu-id="cc9cd-158">In the Pick-up Postal Code field, type '98052'.</span></span>
    * <span data-ttu-id="cc9cd-159">حدد الرمز البريدي الذي يجب أن يكون تعيين قاعدة الأسعار هذا صالحًا منه.</span><span class="sxs-lookup"><span data-stu-id="cc9cd-159">Specify which postal code this rate base assignment should be valid from.</span></span>    
10. <span data-ttu-id="cc9cd-160">في الحقل "البلد/المنطقة لمكان الانتقاء"، اكتب "USA".</span><span class="sxs-lookup"><span data-stu-id="cc9cd-160">In the Pick-up Country Region field, type 'USA'.</span></span>
11. <span data-ttu-id="cc9cd-161">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="cc9cd-161">Click Save.</span></span>

