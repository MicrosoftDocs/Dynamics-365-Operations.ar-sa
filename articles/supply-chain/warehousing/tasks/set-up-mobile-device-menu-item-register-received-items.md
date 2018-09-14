--- 
title: "إعداد صنف قائمة الأجهزة المحمولة لتسجيل الأصناف المستلمة"
description: "تركز هذه المهمة على إعداد عنصر قائمة جهاز محمول."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFMenuItem, WHSRFMenu
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 3cab7eced20111b82afabe69b6f994333b16209a
ms.contentlocale: ar-sa
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-a-mobile-device-menu-item-to-register-received-items"></a><span data-ttu-id="a97bb-103">إعداد صنف قائمة الأجهزة المحمولة لتسجيل الأصناف المستلمة</span><span class="sxs-lookup"><span data-stu-id="a97bb-103">Set up a mobile device menu item to register received items</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a97bb-104">تركز هذه المهمة على إعداد عنصر قائمة جهاز محمول.</span><span class="sxs-lookup"><span data-stu-id="a97bb-104">This task focuses on the setup of a mobile device menu item.</span></span> <span data-ttu-id="a97bb-105">يتم استخدام عنصر القائمة هذا لتسجيل استلام الأصناف المطلوبة عن طريق أوامر الشراء.</span><span class="sxs-lookup"><span data-stu-id="a97bb-105">This menu item is used for registration of the receipt of items ordered via purchase orders.</span></span> 

<span data-ttu-id="a97bb-106">ويمكنك استخدام هذا الدليل في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="a97bb-106">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="a97bb-107">هذا الإجراء مخصص لمدير المستودعات.</span><span class="sxs-lookup"><span data-stu-id="a97bb-107">This procedure is intended for the warehouse manager.</span></span>


## <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="a97bb-108">إنشاء عنصر قائمة جهاز محمول</span><span class="sxs-lookup"><span data-stu-id="a97bb-108">Create a mobile device menu item</span></span>
1. <span data-ttu-id="a97bb-109">انتقل إلى إدارة المستودعات > إعداد > الجهاز المحمول > عناصر قائمة الجهاز المحمول.</span><span class="sxs-lookup"><span data-stu-id="a97bb-109">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="a97bb-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="a97bb-110">Click New.</span></span>
3. <span data-ttu-id="a97bb-111">في الحقل "اسم عنصر القائمة‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="a97bb-111">In the Menu item name field, type a value.</span></span>
    * <span data-ttu-id="a97bb-112">هذا هو المعرف الفريد لعنصر قائمة الجهاز المحمول هذا.</span><span class="sxs-lookup"><span data-stu-id="a97bb-112">This is the unique identifier for this mobile device menu item.</span></span> <span data-ttu-id="a97bb-113">على سبيل المثال، يمكنك كتابة "تسجيل أمر الشراء الخاص بي".</span><span class="sxs-lookup"><span data-stu-id="a97bb-113">For example, you could type 'My PO registration'.</span></span>  
4. <span data-ttu-id="a97bb-114">في الحقل "المسمى الوظيفي"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="a97bb-114">In the Title field, type a value.</span></span>
    * <span data-ttu-id="a97bb-115">هذا هو العنوان الذي سيُعرض للمستخدم على الجهاز المحمول.</span><span class="sxs-lookup"><span data-stu-id="a97bb-115">This is the title, which will be displayed to the user on the mobile device.</span></span> <span data-ttu-id="a97bb-116">على سبيل المثال، يمكنك كتابة "تسجيل أمر الشراء".</span><span class="sxs-lookup"><span data-stu-id="a97bb-116">For example, you could type 'PO registration'.</span></span>  
5. <span data-ttu-id="a97bb-117">في الحقل "الوضع"، حدد "العمل".</span><span class="sxs-lookup"><span data-stu-id="a97bb-117">In the Mode field, select 'Work'.</span></span>
    * <span data-ttu-id="a97bb-118">سيؤدي تسجيل الكميات الفعلية المستلمة لبند أمر شراء إلى إنشاء عمل نقل الأصناف من منطقة الاستلام إلى المخزون.</span><span class="sxs-lookup"><span data-stu-id="a97bb-118">Registration of on-hand quantities received for a purchase order line will create work to move the items from the receiving area into the inventory.</span></span> <span data-ttu-id="a97bb-119">لن يتم إنشاء العمل حتى يتم تسجيل الأصناف.</span><span class="sxs-lookup"><span data-stu-id="a97bb-119">Work isn’t created until the items are registered.</span></span>  <span data-ttu-id="a97bb-120">ولهذا السبب، اترك الخيار "استخدام العمل الموجود" معينًا على "لا".</span><span class="sxs-lookup"><span data-stu-id="a97bb-120">Therefore, leave the Use existing work option set to No.</span></span>  
6. <span data-ttu-id="a97bb-121">قم بتوسيع أو طي المقطع "عام".</span><span class="sxs-lookup"><span data-stu-id="a97bb-121">Expand or collapse the General section.</span></span>
7. <span data-ttu-id="a97bb-122">في الحقل "عملية إنشاء العمل"، حدد "استلام صنف أمر الشراء".</span><span class="sxs-lookup"><span data-stu-id="a97bb-122">In the Work creation process field, select 'Purchase order item receiving'.</span></span>
    * <span data-ttu-id="a97bb-123">يجب تعريف بند أمر شراء بشكل فريد قبل التمكّن من تسجيل "المتاح" في المستودع.</span><span class="sxs-lookup"><span data-stu-id="a97bb-123">A purchase order line must be uniquely identified before on-hand can be registered in the warehouse.</span></span> <span data-ttu-id="a97bb-124">في هذا السيناريو، سيسجل الجهاز المحمول رقم أمر الشراء ورقم الصنف، وسيسمح هذا للنظام بتعريف بند أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="a97bb-124">In this scenario, the mobile device will register the purchase order number and item number, and this will allow the system to identify the PO line.</span></span> <span data-ttu-id="a97bb-125">سيتم إنشاء عمل التخزين ويمكن انتقاؤه بواسطة عامل آخر.</span><span class="sxs-lookup"><span data-stu-id="a97bb-125">Put away work will be created and can be picked up by another worker.</span></span>    <span data-ttu-id="a97bb-126">يحدد أسلوب إنشاء العمل الذي تحدُده الحقول التي ستصبح متاحة في علامة التبويب السريعة "عام".</span><span class="sxs-lookup"><span data-stu-id="a97bb-126">The work creation method that you select determines which fields become available on the General fast tab.</span></span>  
    * <span data-ttu-id="a97bb-127">إذا حددتَ الخيار "استخدام البيانات الافتراضية"، سيتم تمكين زر "البيانات الافتراضي".</span><span class="sxs-lookup"><span data-stu-id="a97bb-127">If you select the Use default data option, the Default data button is enabled.</span></span> <span data-ttu-id="a97bb-128">يمكنك تحديد هذا الخيار هنا لعرض البيانات التي يحتاج إليها أحد العمال في عمله اليومي عادة، بحيث تُعرض هذه القيم على الجهاز المحمول.</span><span class="sxs-lookup"><span data-stu-id="a97bb-128">Here you can select fields to display data that a worker typically needs in their daily work, so that these values are shown on the mobile device.</span></span>  
    * <span data-ttu-id="a97bb-129">تعمل معلمة تجميع لوحات الترخيص بالاشتراك مع مجموعة تسلسلات الوحدات التي تم تعيينها للصنف الذي يتم استلامه.</span><span class="sxs-lookup"><span data-stu-id="a97bb-129">The License plate grouping parameter  works in combination with the unit sequence group that’s assigned to the item that’s being received.</span></span> <span data-ttu-id="a97bb-130">يمكنك تحديد ما إذا كان يجب تجميع إيصالات الكميات الأقل من أو الأكثر من بالتة واحدة في لوحة ترخيص واحدة أو تقسيمها إلى لوحة ترخيص منفصلة لكل وحدة.</span><span class="sxs-lookup"><span data-stu-id="a97bb-130">You can specify whether receipts of less than or more than one pallet should be grouped into one license plate, or divided into a separate license plate for each unit.</span></span>  
    * <span data-ttu-id="a97bb-131">إذا قمت بتحديد الخيار "إنشاء لوحة ترخيص"، سيؤدي هذا إلى إنشاء رقم لوحة ترخيص فريد استناداً إلى تحديد التسلسل الرقمي.</span><span class="sxs-lookup"><span data-stu-id="a97bb-131">If you select the Generate license plate  option, this generates a unique license plate number based on the number sequence selection.</span></span>   
    * <span data-ttu-id="a97bb-132">ويمكنك تحديد القالب الذي سيتم استخدامه عند إنشاء العمل.</span><span class="sxs-lookup"><span data-stu-id="a97bb-132">You can select the template that will be used when work is created.</span></span> <span data-ttu-id="a97bb-133">على سبيل المثال، إذا قمت بتسجيل صنف لأمر شراء، سيتم إنشاء عمل التخزين استناداً إلى قالب العمل.</span><span class="sxs-lookup"><span data-stu-id="a97bb-133">For example, if you register an item for a purchase order, the put away work will be generated based on the work template.</span></span> <span data-ttu-id="a97bb-134">إذا لم تحدد قالب عمل هنا، سعيّن النظام قالبًا يستند إلى معايير الاستعلام المرتبطة بالقوالب.</span><span class="sxs-lookup"><span data-stu-id="a97bb-134">If you don’t select a work template here, the system will assign a template based on the query criteria that are associated with the templates.</span></span>  
    * <span data-ttu-id="a97bb-135">إذا تم عرض رموز الإرجاع على الجهاز المحمول، سيتمكن العمال من تقييم حالة الأصناف أو جودتها وتحديد الرمز المناسب.</span><span class="sxs-lookup"><span data-stu-id="a97bb-135">If disposition codes are displayed on the mobile device, workers can evaluate the status or quality of the items, and select the appropriate code.</span></span> <span data-ttu-id="a97bb-136">تحدد قواعد رمز الإرجاع ما إذا كانت الأصناف ستصبح متوفرة لعمليات مستودع أخرى.</span><span class="sxs-lookup"><span data-stu-id="a97bb-136">The rules for  the disposition code determine whether the items will be available to other warehouse processes.</span></span> <span data-ttu-id="a97bb-137">كما تحدد القواعد أيضًا توجيه الموقع الذي سيُستخدم للعمل الذي يتم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="a97bb-137">The rules also determine which location directive is used for the work that’s created.</span></span>   
    * <span data-ttu-id="a97bb-138">إذا حددتَ رموز إرجاع الدفعة، سيستطيع العمال تقييم حالة دفعة أو جودتها وتحديد رمز الإرجاع المناسب.</span><span class="sxs-lookup"><span data-stu-id="a97bb-138">If you select the Batch disposition codes option, workers can evaluate the status or quality of a batch, and select the appropriate disposition code.</span></span>  <span data-ttu-id="a97bb-139">تُحدد القواعد المعينة برمز إرجاع الدفعة ما إذا كانت الدُفعة ستكون متوفرة لعمليات مستودع أخرى.</span><span class="sxs-lookup"><span data-stu-id="a97bb-139">The rules that are set on the batch disposition code determine whether the batch will be available to other warehouse processes.</span></span>  
    * <span data-ttu-id="a97bb-140">إذا قمت بتحديد خيار "طباعة التسميات"، ستتم طباعة تسمية لوحة ترخيص تلقائياً عند استلام الأصناف.</span><span class="sxs-lookup"><span data-stu-id="a97bb-140">If you select the Print labels option a license plate label will be printed automatically when items are received.</span></span>  
8. <span data-ttu-id="a97bb-141">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="a97bb-141">Click Save.</span></span>
9. <span data-ttu-id="a97bb-142">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a97bb-142">Close the page.</span></span>

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a><span data-ttu-id="a97bb-143">إضافة عنصر القائمة إلى قائمة جهاز محمول</span><span class="sxs-lookup"><span data-stu-id="a97bb-143">Add the menu item to a mobile device menu</span></span>
1. <span data-ttu-id="a97bb-144">انتقل إلى إدارة المستودعات > إعداد > جهاز محمول > قائمة الجهاز المحمول.</span><span class="sxs-lookup"><span data-stu-id="a97bb-144">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
2. <span data-ttu-id="a97bb-145">استخدم عامل التصفية السريع بالحقل "الاسم" بالقيمة "الوارد".</span><span class="sxs-lookup"><span data-stu-id="a97bb-145">Use the Quick Filter to filter on the Name field with a value of 'inbound'.</span></span>
3. <span data-ttu-id="a97bb-146">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="a97bb-146">Click Edit.</span></span>
4. <span data-ttu-id="a97bb-147">في الشجرة، حدد "في شجرة القوائم والعناصر المتاحة، حدد عنصر القائمة الذي أنشأتَه من قبل".</span><span class="sxs-lookup"><span data-stu-id="a97bb-147">In the tree, select 'In the Available menu's and items tree, select the menu item that you created before.'.</span></span>
    * <span data-ttu-id="a97bb-148">حدد عنصر القائمة الذي أنشأتَه سابقًا.</span><span class="sxs-lookup"><span data-stu-id="a97bb-148">Select the menu item that you created before.</span></span>  
5. <span data-ttu-id="a97bb-149">انقر فوق المتجه لليمين.</span><span class="sxs-lookup"><span data-stu-id="a97bb-149">Click on the arrow that points to the right.</span></span>
6. <span data-ttu-id="a97bb-150">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="a97bb-150">Click Save.</span></span>
7. <span data-ttu-id="a97bb-151">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a97bb-151">Close the page.</span></span>


