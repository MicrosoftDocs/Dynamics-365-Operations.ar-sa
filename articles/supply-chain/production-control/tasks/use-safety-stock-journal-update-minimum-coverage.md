--- 
title: "استخدام دفتر يومية المخزون الاحتياطي لتحديث الحد الأدنى للتغطية"
description: "يوضح هذا الإجراء كيفية حساب مقترحات الحد الأدنى للتغطية استنادًا إلى الحركات السابقة، ثم تحديث تغطية الصنف بواسطة المقترحات."
author: ChristianRytt
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: ad194efd151dab8c8fe5542cb40de2d811fb4b3d
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a><span data-ttu-id="e981c-103">استخدام دفتر يومية المخزون الاحتياطي لتحديث الحد الأدنى للتغطية</span><span class="sxs-lookup"><span data-stu-id="e981c-103">Use the safety stock journal to update minimum coverage</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e981c-104">يوضح هذا الإجراء كيفية حساب مقترحات الحد الأدنى للتغطية استنادًا إلى الحركات السابقة، ثم تحديث تغطية الصنف بواسطة المقترحات.</span><span class="sxs-lookup"><span data-stu-id="e981c-104">This procedure shows how to calculate minimum coverage proposals based on historical transactions and then update the item coverage with the proposals.</span></span> <span data-ttu-id="e981c-105">ويتم ذلك باستخدام دفتر يومية المخزون الاحتياطي.</span><span class="sxs-lookup"><span data-stu-id="e981c-105">This is done using the safety stock journal.</span></span> <span data-ttu-id="e981c-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USMF.‬</span><span class="sxs-lookup"><span data-stu-id="e981c-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="e981c-107">هذه المهمة مخصصة لمخطط الإنتاج، للمساعدة في الحفاظ على الحد الأدنى للتغطية.</span><span class="sxs-lookup"><span data-stu-id="e981c-107">This task is intended for the production planner, to help maintain minimum coverage.</span></span>


## <a name="create-a-new-safety-stock-journal-name"></a><span data-ttu-id="e981c-108">إنشاء اسم دفتر يومية مخزون احتياطي جديد</span><span class="sxs-lookup"><span data-stu-id="e981c-108">Create a new safety stock journal name</span></span>
1. <span data-ttu-id="e981c-109">انتقل إلى "أسماء دفتر يومية المخزون الاحتياطي".</span><span class="sxs-lookup"><span data-stu-id="e981c-109">Go to Safety stock journal names.</span></span>
2. <span data-ttu-id="e981c-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="e981c-110">Click New.</span></span>
3. <span data-ttu-id="e981c-111">في حقل "الاسم"، اكتب "مواد".</span><span class="sxs-lookup"><span data-stu-id="e981c-111">In the Name field, type 'Material'.</span></span>
4. <span data-ttu-id="e981c-112">في حقل "الوصف"، اكتب "مواد".</span><span class="sxs-lookup"><span data-stu-id="e981c-112">In the Description field, type 'Material'.</span></span>
5. <span data-ttu-id="e981c-113">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e981c-113">Close the page.</span></span>

## <a name="create-a-safety-stock-journal"></a><span data-ttu-id="e981c-114">إنشاء دفتر يومية المخزون الاحتياطي</span><span class="sxs-lookup"><span data-stu-id="e981c-114">Create a safety stock journal</span></span>
1. <span data-ttu-id="e981c-115">انتقل إلى "حساب المخزون الاحتياطي".</span><span class="sxs-lookup"><span data-stu-id="e981c-115">Go to Safety stock calculation.</span></span>
2. <span data-ttu-id="e981c-116">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="e981c-116">Click New.</span></span>
3. <span data-ttu-id="e981c-117">في الحقل "الاسم"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="e981c-117">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="e981c-118">حدد اسم دفتر يومية المخزون الاحتياطي الذي قمت بإنشائه، على سبيل المثال، المواد.</span><span class="sxs-lookup"><span data-stu-id="e981c-118">Select the safety stock journal name that you created, for example, Material.</span></span>  
4. <span data-ttu-id="e981c-119">انقر فوق "إنشاء بنود".</span><span class="sxs-lookup"><span data-stu-id="e981c-119">Click Create lines.</span></span>
5. <span data-ttu-id="e981c-120">في الحقل "من تاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="e981c-120">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="e981c-121">عيّن التاريخ إلى "2015-01-02".</span><span class="sxs-lookup"><span data-stu-id="e981c-121">Set the date to '2015-01-02'.</span></span>  
6. <span data-ttu-id="e981c-122">في الحقل "إلى تاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="e981c-122">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="e981c-123">عيّن التاريخ إلى "2015-12-30".</span><span class="sxs-lookup"><span data-stu-id="e981c-123">Set the date to '2015-12-30'.</span></span>  
7. <span data-ttu-id="e981c-124">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="e981c-124">Click OK.</span></span>
    * <span data-ttu-id="e981c-125">سيؤدي ذلك إلى إنشاء بنود للأبعاد التي تحتوي على حركات المخزون.</span><span class="sxs-lookup"><span data-stu-id="e981c-125">This will create lines for the dimensions that have inventory transactions.</span></span>  

## <a name="calculate-proposal"></a><span data-ttu-id="e981c-126">مقترح الحساب</span><span class="sxs-lookup"><span data-stu-id="e981c-126">Calculate proposal</span></span>
1. <span data-ttu-id="e981c-127">انقر فوق "مقترح الحساب".</span><span class="sxs-lookup"><span data-stu-id="e981c-127">Click Calculate proposal.</span></span>
2. <span data-ttu-id="e981c-128">حدد الخيار "استخدام متوسط الإصدار أثناء وقت الإنتاج".</span><span class="sxs-lookup"><span data-stu-id="e981c-128">Select the Use average issue during lead time option.</span></span>
3. <span data-ttu-id="e981c-129">عيّن معامل الضرب إلى "10".</span><span class="sxs-lookup"><span data-stu-id="e981c-129">Set Multiplication factor to '10'.</span></span>
    * <span data-ttu-id="e981c-130">يتم استخدام عامل الضرب لضبط المقترح.</span><span class="sxs-lookup"><span data-stu-id="e981c-130">The Multiply factor is used to adjust the proposal.</span></span> <span data-ttu-id="e981c-131">نظرًا لوجود عدد قليل من الحركات في بيانات العرض التوضيحي، ستحتاج إلى تعيين العامل للحصول على مقترح واقعي.</span><span class="sxs-lookup"><span data-stu-id="e981c-131">Because demo data only has a few transactions, you will need to set the factor to get a realistic proposal.</span></span>  
4. <span data-ttu-id="e981c-132">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="e981c-132">Click OK.</span></span>
    * <span data-ttu-id="e981c-133">قم بالتمرير للأسفل للعثور على M0002 وM0003.</span><span class="sxs-lookup"><span data-stu-id="e981c-133">Scroll down to find M0002 and M0003.</span></span> <span data-ttu-id="e981c-134">اعرض عمود "الحد الأدنى للكمية المحسوبة".</span><span class="sxs-lookup"><span data-stu-id="e981c-134">View the Calculated minimum quantity column.</span></span>   

## <a name="update-minimum-quantity"></a><span data-ttu-id="e981c-135">تحديث الحد الأدنى للكمية</span><span class="sxs-lookup"><span data-stu-id="e981c-135">Update minimum quantity</span></span>
1. <span data-ttu-id="e981c-136">في الحقل "الحد الأدنى الجديد للكمية‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="e981c-136">In the New minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="e981c-137">حدّث "الحد الأدنى الجديد للكمية‬" بحيث تتطابق الكمية مع القيمة في "الحد الأدنى للكمية المحسوبة‬".</span><span class="sxs-lookup"><span data-stu-id="e981c-137">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="e981c-138">إذا كانت قيمة الحد الأدنى للكمية المحسوبة‬ صفرًا، فيمكنك إدخال القيمة المستقبلية المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="e981c-138">If the Calculated minimum is zero,  you can enter the desired future value.</span></span> <span data-ttu-id="e981c-139">على سبيل المثال، يمكنك إدخال الحد الأدنى للكمية المحسوبة‬ في هذا الحقل للصنف M0002 ومستودعه 12.</span><span class="sxs-lookup"><span data-stu-id="e981c-139">For example, you can enter the Calculated minimum quantity in this field for M0002 that has warehouse 12.</span></span>  
2. <span data-ttu-id="e981c-140">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e981c-140">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e981c-141">على سبيل المثال، يمكنك تحديد M0002 ومستودعه 12.</span><span class="sxs-lookup"><span data-stu-id="e981c-141">For example, you can select M0002 that has warehouse 12.</span></span>  
3. <span data-ttu-id="e981c-142">في الحقل "الحد الأدنى الجديد للكمية‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="e981c-142">In the New minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="e981c-143">حدّث "الحد الأدنى الجديد للكمية‬" بحيث تتطابق الكمية مع القيمة في "الحد الأدنى للكمية المحسوبة‬".</span><span class="sxs-lookup"><span data-stu-id="e981c-143">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="e981c-144">إذا كانت قيمة الحد الأدنى للكمية المحسوبة‬ صفرًا، فيمكنك إدخال القيمة المستقبلية المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="e981c-144">If the Calculated minimum is zero you can enter the desired future value.</span></span>  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a><span data-ttu-id="e981c-145">ترحيل الحد الأدنى الجديد للكمية والتحقق من صحته</span><span class="sxs-lookup"><span data-stu-id="e981c-145">Post the new minimum quantity and validate the result</span></span>
1. <span data-ttu-id="e981c-146">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="e981c-146">Click Post.</span></span>
2. <span data-ttu-id="e981c-147">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="e981c-147">Click OK.</span></span>
3. <span data-ttu-id="e981c-148">انقر لمتابعة الارتباط في الحقل "رقم الصنف".</span><span class="sxs-lookup"><span data-stu-id="e981c-148">Click to follow the link in the Item number field.</span></span>
4. <span data-ttu-id="e981c-149">انقر لمتابعة الارتباط في الحقل "رقم الصنف".</span><span class="sxs-lookup"><span data-stu-id="e981c-149">Click to follow the link in the Item number field.</span></span>
5. <span data-ttu-id="e981c-150">في جزء "الإجراءات"، انقر فوق "خطة".</span><span class="sxs-lookup"><span data-stu-id="e981c-150">On the Action Pane, click Plan.</span></span>
6. <span data-ttu-id="e981c-151">انقر فوق "تغطية الصنف‬".</span><span class="sxs-lookup"><span data-stu-id="e981c-151">Click Item coverage.</span></span>
    * <span data-ttu-id="e981c-152">لاحظ أنه تم تحديث الحد الأدنى للكمية‬ بواسطة الحد الأدنى الجديد للكمية من دفتر يومية المخزون الاحتياطي.</span><span class="sxs-lookup"><span data-stu-id="e981c-152">Notice that the Minimum quantity has been updated with the new minimum quantity from the safety stock journal.</span></span>  


