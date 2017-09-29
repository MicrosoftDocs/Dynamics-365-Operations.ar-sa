--- 
title: "إقران مؤشر وقود بشركة نقل كرسوم إضافية"
description: "يوضح هذا الدليل كيفية إنشاء المهام الإضافية والتكلفة الإضافية لشركة الشحن‬ والسجل الرئيسي للتكاليف الإضافية للوقود‬ وإقرانها بمؤشر وقود الناقل‬ مع ناقل."
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
ms.openlocfilehash: a2b8534231c5fa50b1e0f709e09d318bb8202a43
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="associate-a-fuel-index-with-a-carrier-as-an-accessorial-charge"></a><span data-ttu-id="298fc-103">إقران مؤشر وقود بشركة نقل كرسوم إضافية</span><span class="sxs-lookup"><span data-stu-id="298fc-103">Associate a fuel index with a carrier as an accessorial charge</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="298fc-104">يوضح هذا الدليل كيفية إنشاء المهام الإضافية والتكلفة الإضافية لشركة الشحن‬ والسجل الرئيسي للتكاليف الإضافية للوقود‬ وإقرانها بمؤشر وقود الناقل‬ مع ناقل.</span><span class="sxs-lookup"><span data-stu-id="298fc-104">This guide shows how to create an accessorial assignment, carrier accessorial charge, accessorial master for fuel surcharge, and associate a carrier fuel index with a carrier.</span></span> <span data-ttu-id="298fc-105">تحتاج إلى إعداد مؤشر وقود الناقل قبل تشغيل هذا الدليل.</span><span class="sxs-lookup"><span data-stu-id="298fc-105">You need to have set up a carrier fuel index before you run this guide.</span></span> <span data-ttu-id="298fc-106">يمكنك استخدام الدليل "إعداد مؤشر وقود الناقل‬‬" للقيام بذلك.</span><span class="sxs-lookup"><span data-stu-id="298fc-106">You can use the “Set up a carrier fuel index” guide to do this.</span></span> <span data-ttu-id="298fc-107">عادة ما يتم تنفيذ هذه المهام من قِبل إدارة اللوجستيات‬.</span><span class="sxs-lookup"><span data-stu-id="298fc-107">These setup tasks are typically done by a Logistics manager.</span></span> <span data-ttu-id="298fc-108">بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="298fc-108">The demo data used to create this procedure is USMF.</span></span>


## <a name="create-an-accessorial-master"></a><span data-ttu-id="298fc-109">إنشاء سجل رئيسي إضافي</span><span class="sxs-lookup"><span data-stu-id="298fc-109">Create an accessorial master</span></span>
1. <span data-ttu-id="298fc-110">انتقل إلى إدارة النقل > إعداد > التقييم‬ > الأصول الإضافية.</span><span class="sxs-lookup"><span data-stu-id="298fc-110">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="298fc-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="298fc-111">Click New.</span></span>
3. <span data-ttu-id="298fc-112">في الحقل "الأصول الإضافية‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="298fc-112">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="298fc-113">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="298fc-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="298fc-114">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="298fc-114">Click Save.</span></span>

## <a name="create-a-carrier-accessorial-charge"></a><span data-ttu-id="298fc-115">إنشاء التكلفة الإضافية لشركة الشحن</span><span class="sxs-lookup"><span data-stu-id="298fc-115">Create a carrier accessorial charge</span></span>
1. <span data-ttu-id="298fc-116">انتقل إلى إدارة النقل > إعداد > التقييم‬ > التكاليف الإضافية لشركة النقل‬.</span><span class="sxs-lookup"><span data-stu-id="298fc-116">Go to Transportation management > Setup > Rating > Carrier accessorial charges.</span></span>
2. <span data-ttu-id="298fc-117">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="298fc-117">Click New.</span></span>
3. <span data-ttu-id="298fc-118">في الحقل "معرف شركة النقل الإضافية‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="298fc-118">In the Carrier accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="298fc-119">في الحقل "شركة الشحن "، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="298fc-119">In the Shipping carrier field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="298fc-120">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="298fc-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="298fc-121">في هذا المثال، اختر "شركة النقل".</span><span class="sxs-lookup"><span data-stu-id="298fc-121">In this example, choose Truck Carrier.</span></span>  
6. <span data-ttu-id="298fc-122">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="298fc-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="298fc-123">‏‫في الحقل "خدمة الناقل‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.‬</span><span class="sxs-lookup"><span data-stu-id="298fc-123">In the Carrier service field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="298fc-124">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="298fc-124">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="298fc-125">في الحقل "الأصل الإضافي‬‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="298fc-125">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="298fc-126">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="298fc-126">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="298fc-127">في هذا المثال، اختر الأصل الإضافي الذي أنشأته مؤخرًا.‬</span><span class="sxs-lookup"><span data-stu-id="298fc-127">In this example, choose the newly created Accessorial master.</span></span>  
11. <span data-ttu-id="298fc-128">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="298fc-128">Click Save.</span></span>

## <a name="create-an-accessorial-assignment"></a><span data-ttu-id="298fc-129">إنشاء مهمة إضافية</span><span class="sxs-lookup"><span data-stu-id="298fc-129">Create an accessorial assignment</span></span>
1. <span data-ttu-id="298fc-130">انقر فوق "المهام الإضافية".</span><span class="sxs-lookup"><span data-stu-id="298fc-130">Click Accessorial assignments.</span></span>
2. <span data-ttu-id="298fc-131">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="298fc-131">Click New.</span></span>
3. <span data-ttu-id="298fc-132">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="298fc-132">In the Name field, type a value.</span></span>
4. <span data-ttu-id="298fc-133">بدّل توسيع المقطع "المعايير".</span><span class="sxs-lookup"><span data-stu-id="298fc-133">Toggle the expansion of the Criteria section.</span></span>
    * <span data-ttu-id="298fc-134">في المعايير، يمكنك اختيار تطبيق التكاليف الإضافية للوقود‬ دائمًا أو في هذا المثال اختيار تطبيقها فقط داخل منطقة معينة.</span><span class="sxs-lookup"><span data-stu-id="298fc-134">In the criteria, you can choose to always apply the fuel surcharge or for this example choose that it only applies within a certain region.</span></span>  
5. <span data-ttu-id="298fc-135">في الحقل "الرمز البريدي من"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="298fc-135">In the ZIP/postal code from field, type a value.</span></span>
6. <span data-ttu-id="298fc-136">في الحقل "الرمز البريدي إلى"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="298fc-136">In the ZIP/postal code to field, type a value.</span></span>
7. <span data-ttu-id="298fc-137">بدّل توسيع المقطع "الحساب".</span><span class="sxs-lookup"><span data-stu-id="298fc-137">Toggle the expansion of the Calculation section.</span></span>
    * <span data-ttu-id="298fc-138">في مقطع الحساب، يمكنك تحديد كيفية حساب التكاليف الإضافية للوقود‬.</span><span class="sxs-lookup"><span data-stu-id="298fc-138">In the calculation section you can specify how to calculate the fuel surcharge.</span></span> <span data-ttu-id="298fc-139">يعتمد هذا الحساب على الوحدة الإضافية‬ التي اخترتها كأساس للحساب.</span><span class="sxs-lookup"><span data-stu-id="298fc-139">This calculation depends on the Accessorial unit that you chose as the base for your calculation.</span></span>  
8. <span data-ttu-id="298fc-140">في الحقل "نوع الرسوم الإضافية‬"، حدد "التكاليف الإضافية للوقود‬".</span><span class="sxs-lookup"><span data-stu-id="298fc-140">In the Accessorial fee type field, select 'Fuel surcharge'.</span></span>
9. <span data-ttu-id="298fc-141">في الحقل "الوحدة الإضافية‬"، حدد "المسافة المقطوعة بالأميال‬".</span><span class="sxs-lookup"><span data-stu-id="298fc-141">In the Accessorial unit field, select 'Mileage'.</span></span>
10. <span data-ttu-id="298fc-142">في الحقل "المنطقة‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="298fc-142">In the Region field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="298fc-143">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="298fc-143">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="298fc-144">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="298fc-144">Click Save.</span></span>

## <a name="update-the-carrier-rating-profile"></a><span data-ttu-id="298fc-145">تحديث ملف تعريف تصنيف شركة الشحن</span><span class="sxs-lookup"><span data-stu-id="298fc-145">Update the carrier rating profile</span></span>
1. <span data-ttu-id="298fc-146">انتقل إلى إدارة النقل > الإعداد > شركات النقل > شركات الشحن.</span><span class="sxs-lookup"><span data-stu-id="298fc-146">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="298fc-147">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="298fc-147">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="298fc-148">بدّل توسيع المقطع "ملفات تعريف التقييم‬‬".</span><span class="sxs-lookup"><span data-stu-id="298fc-148">Toggle the expansion of the Rating profiles section.</span></span>
4. <span data-ttu-id="298fc-149">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="298fc-149">Click Edit.</span></span>
5. <span data-ttu-id="298fc-150">في الحقل "مؤشر وقود الناقل‬‬‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="298fc-150">In the Carrier fuel index field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="298fc-151">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="298fc-151">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="298fc-152">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="298fc-152">Click Save.</span></span>


