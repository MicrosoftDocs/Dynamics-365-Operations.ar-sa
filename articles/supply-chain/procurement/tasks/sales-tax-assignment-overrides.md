--- 
title: "تعيين ضريبة المبيعات والتجاوزات"
description: "يوضح هذا الإجراء كيفية تعيين مجموعات ضريبة المبيعات إلى قنوات البيع بالتجزئة."
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 05f3abf7359a9bfb3c708739551498333802dd0c
ms.contentlocale: ar-sa
ms.lasthandoff: 08/07/2018

---
# <a name="sales-tax-assignment-and-overrides"></a><span data-ttu-id="8c4d2-103">تعيين ضريبة المبيعات والتجاوزات</span><span class="sxs-lookup"><span data-stu-id="8c4d2-103">Sales tax assignment and overrides</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8c4d2-104">يوضح هذا الإجراء كيفية تعيين مجموعات ضريبة المبيعات إلى قنوات البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="8c4d2-104">This procedure demonstrates how to assign sales tax groups to retail channels.</span></span> <span data-ttu-id="8c4d2-105">وينقلك هذا الإجراء أيضًا عبر عملية إنشاء تجاوز ضريبة مبيعات جديد وتعيينه إلى مجموعة تجاوز ضريبة مبيعات موجودة.</span><span class="sxs-lookup"><span data-stu-id="8c4d2-105">It also walks through the process of creating a new sales tax override and assigning it to an existing sales tax override group.</span></span> <span data-ttu-id="8c4d2-106">يستخدم هذا الإجراء</span><span class="sxs-lookup"><span data-stu-id="8c4d2-106">This procedure</span></span>

<span data-ttu-id="8c4d2-107">شركة USRT في بيانات العرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="8c4d2-107">uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="8c4d2-108">انتقل إلى البيع بالتجزئة والتجارة > القنوات > متاجر البيع بالتجزئة > جميع متاجر البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="8c4d2-108">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="8c4d2-109">في القائمة، انقر فوق ارتباط "معرف قناة البيع بالتجزئة" للقناة "هيوستن."</span><span class="sxs-lookup"><span data-stu-id="8c4d2-109">In the list, click the Retail Channel ID link for "Houston."</span></span>
3. <span data-ttu-id="8c4d2-110">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="8c4d2-110">Click Edit.</span></span>
    * <span data-ttu-id="8c4d2-111">يحتوي الحقل "مجموعة ضريبة المبيعات" على قائمة بمجموعات ضرائب المبيعات للشركة الحالية.</span><span class="sxs-lookup"><span data-stu-id="8c4d2-111">The "Sales tax group" field contains the list of sales tax groups for the current company.</span></span> <span data-ttu-id="8c4d2-112">المجموعة التي تم تعيينها حاليًا هي مجموعة ضريبة المبيعات العامة "تكساس".</span><span class="sxs-lookup"><span data-stu-id="8c4d2-112">The currently assigned group is a generic "Texas" sales tax group.</span></span> <span data-ttu-id="8c4d2-113">هناك أيضًا مجموعات ضريبة المبيعات لكل من "Washington" و"Washington, King County."</span><span class="sxs-lookup"><span data-stu-id="8c4d2-113">There are also sales tax groups for "Washington" and "Washington, King County."</span></span> <span data-ttu-id="8c4d2-114">بإمكان مجموعات ضريبة المبيعات أن تتضمن الضرائب المعمول بها لمقاطعات متعددة.</span><span class="sxs-lookup"><span data-stu-id="8c4d2-114">Sales tax groups can include applicable taxes for multiple municipalities.</span></span>  
    * <span data-ttu-id="8c4d2-115">يمثّل الحقل "تجاوز ضريبة المبيعات" المكان حيث يمكن تعيين مجموعات تجاوز ضريبة المبيعات إلى القناة.</span><span class="sxs-lookup"><span data-stu-id="8c4d2-115">The "Sales tax override" field is where sales tax override groups can be mapped to the channel.</span></span> <span data-ttu-id="8c4d2-116">يمكن استخدام مجموعات تجاوز ضريبة المبيعات لتجميع تجاوزات ضريبة المبيعات التي تصلح لمتاجر متعددة.</span><span class="sxs-lookup"><span data-stu-id="8c4d2-116">Sales tax override groups can be used to group together sales tax overrides that work for multiple stores.</span></span> <span data-ttu-id="8c4d2-117">بدلاً من تعيين تجاوزات ضريبة المبيعات يدويًا كل تجاوز على حدة، يمكن إنشاء المجموعة وتعيينها مباشرة إلى القنوات لتوفير الوقت.</span><span class="sxs-lookup"><span data-stu-id="8c4d2-117">Rather than manually assigning sales tax overrides one by one, the group can be created and assigned directly to the channels to save time.</span></span>  
4. <span data-ttu-id="8c4d2-118">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="8c4d2-118">Click Save.</span></span>
5. <span data-ttu-id="8c4d2-119">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8c4d2-119">Close the page.</span></span>
6. <span data-ttu-id="8c4d2-120">انتقل إلى البيع بالتجزئة والتجارة > إعداد القناة > ضرائب المبيعات > تجاوزات ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="8c4d2-120">Go to Retail and commerce > Channel setup > Sales taxes > Sales tax overrides.</span></span>
7. <span data-ttu-id="8c4d2-121">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="8c4d2-121">Click New.</span></span>
8. <span data-ttu-id="8c4d2-122">في الحقل "تجاوز ضريبة المبيعات"، أدخل اسمًا للتجاوز الجديد.</span><span class="sxs-lookup"><span data-stu-id="8c4d2-122">In the Sales tax override field, provide a name for your new override.</span></span>
9. <span data-ttu-id="8c4d2-123">في حقل "الوصف"، أدخل وصفًا للتجاوز.</span><span class="sxs-lookup"><span data-stu-id="8c4d2-123">In the Description field, provide a description of the override.</span></span>
10. <span data-ttu-id="8c4d2-124">عيّن الحالة إلى "تمكين".</span><span class="sxs-lookup"><span data-stu-id="8c4d2-124">Set the status to "Enable."</span></span>
11. <span data-ttu-id="8c4d2-125">قم بتوسيع أو طي مقطع "التجاوز".</span><span class="sxs-lookup"><span data-stu-id="8c4d2-125">Expand or collapse the Override section.</span></span>
12. <span data-ttu-id="8c4d2-126">في الحقل "النوع"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="8c4d2-126">In the Type field, select an option.</span></span>
    * <span data-ttu-id="8c4d2-127">يمكن استخدام مجموعات ضرائب المبيعات للأصناف‬ لإبطال ضرائب أصناف محددة تنتمي إلى المجموعة.</span><span class="sxs-lookup"><span data-stu-id="8c4d2-127">Item sales tax groups can be used to override taxes for specific items that belong to the group.</span></span> <span data-ttu-id="8c4d2-128">على سبيل المثال، تُحسب ضرائب المواد الغذائية عادةً بشكل مختلف عن السلع المعمرة، ويحتمل أن يكون لهذه المواد مجموعة ضرائب مبيعات خاصة بها.</span><span class="sxs-lookup"><span data-stu-id="8c4d2-128">For example, food items are typically taxed differently from hard goods, and would likely have their own sales tax group.</span></span>     <span data-ttu-id="8c4d2-129">إن مجموعات ضرائب المبيعات عبارة عن مجموعات ضرائب قابلة للتطبيق على قناة معينة.</span><span class="sxs-lookup"><span data-stu-id="8c4d2-129">Sales tax groups are groups of taxes that are applicable to a particular channel.</span></span> <span data-ttu-id="8c4d2-130">على سبيل المثال، إذا كانت القناة تبيع بالتجزئة ومن شركة إلى شركة، فقد يتم استخدام مجموعات ضرائب مبيعات أصناف مختلفة.</span><span class="sxs-lookup"><span data-stu-id="8c4d2-130">For example, if a channel sells both retail and business-to-business, different items sales tax groups may be used.</span></span> <span data-ttu-id="8c4d2-131">وسيتم تعيين جميع الضرائب المعمول بها على مجموعة ضرائب المبيعات.</span><span class="sxs-lookup"><span data-stu-id="8c4d2-131">All the applicable taxes would be mapped to the sales tax group.</span></span>  
    * <span data-ttu-id="8c4d2-132">يمكنك الآن تحديد "من" و "إلى" الضرائب أو "من مجموعة الضريبة" و"إلى مجموعة الضريبة" لإنشاء تجاوز ضريبة مبيعات خاص بك.</span><span class="sxs-lookup"><span data-stu-id="8c4d2-132">Now you can select the "From" and "To" taxes or "From tax group" and "To tax group" to create your sales tax override.</span></span>    <span data-ttu-id="8c4d2-133">يشير الحقل "من" إلى الضريبة أو مجموعة الضريبة التي يجب تجاوزها.</span><span class="sxs-lookup"><span data-stu-id="8c4d2-133">The "From" field indicates the tax or tax group to be overridden.</span></span> <span data-ttu-id="8c4d2-134">يوفر التجاوز بحسب مجموعة ضرائب المبيعات للأصناف‬ خيارات مختلفة عن التجاوز ب بحسب مجموعة الضريبة.</span><span class="sxs-lookup"><span data-stu-id="8c4d2-134">Overriding by Item sales tax group provides different options than overriding by sales tax group.</span></span>    <span data-ttu-id="8c4d2-135">يمكن إعداد تجاوزات ضريبة المبيعات لتجاوز الضرائب على حركات بأكملها أو على بنود معينة في الحركة.</span><span class="sxs-lookup"><span data-stu-id="8c4d2-135">Sales tax overrides can be set up to override taxes on entire transactions or on particular lines in the transaction.</span></span>  
13. <span data-ttu-id="8c4d2-136">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="8c4d2-136">Click Save.</span></span>
14. <span data-ttu-id="8c4d2-137">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8c4d2-137">Close the page.</span></span>
15. <span data-ttu-id="8c4d2-138">انتقل إلى البيع بالتجزئة والتجارة > إعداد القناة > ضرائب المبيعات > مجموعات تجاوز ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="8c4d2-138">Go to Retail and commerce > Channel setup > Sales taxes > Sales tax override groups.</span></span>
    * <span data-ttu-id="8c4d2-139">في هذه الخطوة، ستعيّن تجاوز ضريبة المبيعات‬ الذي تم إنشاؤه مؤخرًا إلى مجموعة تجاوز ضريبة المبيعات‬ التي تم تعيينها إلى قناة "هيوستن".</span><span class="sxs-lookup"><span data-stu-id="8c4d2-139">In this step you will assigned the newly created sales tax override to the sales tax override group assigned to the Houston channel.</span></span>  
16. <span data-ttu-id="8c4d2-140">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="8c4d2-140">Click Edit.</span></span>
17. <span data-ttu-id="8c4d2-141">قم بتوسيع قسم الإعداد أو طيه.</span><span class="sxs-lookup"><span data-stu-id="8c4d2-141">Expand or collapse the Setup section.</span></span>
18. <span data-ttu-id="8c4d2-142">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="8c4d2-142">Click Add.</span></span>
19. <span data-ttu-id="8c4d2-143">في الحقل "تجاوز ضريبة المبيعات"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="8c4d2-143">In the Sales tax override field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="8c4d2-144">حدد تجاوز ضريبة المبيعات الذي تم إنشاؤه في السابق من القائمة.</span><span class="sxs-lookup"><span data-stu-id="8c4d2-144">Select the previously created sales tax override from the list.</span></span>
21. <span data-ttu-id="8c4d2-145">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="8c4d2-145">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="8c4d2-146">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="8c4d2-146">Click Save.</span></span>


