---
title: "إعداد ملف تعريف نظرة عامة على وصول الصنف"
description: "تركز هذه المهمة على إعداد ملف تعريف النظرة العامة على الوصول."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 24945597255c29abbe8eb1d60a6cbca51e0498be
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="7b861-103">إعداد ملف تعريف نظرة عامة على وصول الصنف</span><span class="sxs-lookup"><span data-stu-id="7b861-103">Set up an item arrival overview profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7b861-104">تركز هذه المهمة على إعداد ملف تعريف النظرة العامة على الوصول.</span><span class="sxs-lookup"><span data-stu-id="7b861-104">This task focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="7b861-105">إن ملف تعريف النظرة العامة على الوصول عبارة عن مجموعة من القواعد التي سيتم تطبيقها عند فتح صفحة "نظرة عامة على الوصول" من قِبل المستخدم.</span><span class="sxs-lookup"><span data-stu-id="7b861-105">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="7b861-106">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="7b861-106">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="7b861-107">يقوم موظف الاستلام عادةً بتنفيذ هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="7b861-107">This procedure would typically be carried out by a receiving clerk.</span></span>





1. <span data-ttu-id="7b861-108">انتقل إلى إدارة المخزون > إعداد > توزيع > ملفات تعريف النظرة العامة على الوصول‬.</span><span class="sxs-lookup"><span data-stu-id="7b861-108">Go to Inventory management > Setup > Distribution > Arrival overview profiles.</span></span>
2. <span data-ttu-id="7b861-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="7b861-109">Click New.</span></span>
    * <span data-ttu-id="7b861-110">نظرًا لأنك ستعمل دائماً في نفس المستودع في تفريغ حمولات الشاحنات الكاملة، يجب عليك إنشاء ملف تعريف نظرة عامة حول الوصول لتبسيط عملية تسجيل الأصناف المستلمة.</span><span class="sxs-lookup"><span data-stu-id="7b861-110">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="7b861-111">في الحقل "اسم ملف تعريف النظرة العامة حول الوصول"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="7b861-111">In the Arrival overview profile name field, type a value.</span></span>
4. <span data-ttu-id="7b861-112">في الحقل "إظهار البنود"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="7b861-112">In the Show lines field, select an option.</span></span>
    * <span data-ttu-id="7b861-113">حدد البنود المطلوب إظهارها لعمليات الاستلام:   الكل – إظهار جميع البنود، بصرف النظر عن الحالة.</span><span class="sxs-lookup"><span data-stu-id="7b861-113">Select which lines to show for the receipts:   All – Show all lines, regardless of status.</span></span>   <span data-ttu-id="7b861-114">جارية-إظهار البنود الخاصة بعمليات الاستلام التي يكون فيها تقدم العملية مكتمل أو جزئي.</span><span class="sxs-lookup"><span data-stu-id="7b861-114">In progress – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="7b861-115">وهذا يعني أنه بالنسبة لكل بند، تم تسجيل إما كل الكمية أو جزء منها في دفتر يومية الوصول.</span><span class="sxs-lookup"><span data-stu-id="7b861-115">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   <span data-ttu-id="7b861-116">غير مكتملة-إظهار البنود الخاصة بعمليات الاستلام التي يكون فيها تقدم العملية "لم يبدأ بعد أو جزئي".</span><span class="sxs-lookup"><span data-stu-id="7b861-116">Not complete – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="7b861-117">وهذا يعني أنه بالنسبة لكل بند، لم يتم تسجيل أي شيء من الكمية أو أنه قد تم تسجيل جزء منها فقط في دفتر يومية الوصول.</span><span class="sxs-lookup"><span data-stu-id="7b861-117">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  
5. <span data-ttu-id="7b861-118">قم بتوسيع القسم "خيارات الوصول" أو طيه.</span><span class="sxs-lookup"><span data-stu-id="7b861-118">Expand or collapse the Arrival options section.</span></span>
6. <span data-ttu-id="7b861-119">في الحقل "الأيام التالية"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="7b861-119">In the Days forward field, type a value.</span></span>
    * <span data-ttu-id="7b861-120">يؤدي هذا إلى تعيين عامل تصفية لإظهار بنود الإيصال المتوقع استلامها خلال الأيام القليلة القادمة (اعتماداً على الرقم الذي قمت بتعيينه).</span><span class="sxs-lookup"><span data-stu-id="7b861-120">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="7b861-121">في الحقل "الأيام السابقة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="7b861-121">In the Days back field, type a value.</span></span>
    * <span data-ttu-id="7b861-122">يؤدي هذا إلى تعيين عامل تصفية لإظهار بنود الإيصال المتوقع استلامها منذ عدة أيام سابقة.</span><span class="sxs-lookup"><span data-stu-id="7b861-122">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="7b861-123">في الحقل "المستودع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="7b861-123">In the Warehouses field, type a value.</span></span>
    * <span data-ttu-id="7b861-124">قم بإجراء التصفية بمستودع واحد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="7b861-124">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="7b861-125">في الحقل "وضع التسليم"، حدد قيمة.</span><span class="sxs-lookup"><span data-stu-id="7b861-125">In the Mode of delivery field, select a value.</span></span>
    * <span data-ttu-id="7b861-126">يؤدي هذا الإجراء إلى تعيين عامل تصفية ليتم إظهار بنود الإيصال التي تم تسليمها في هذا الوضع فقط.</span><span class="sxs-lookup"><span data-stu-id="7b861-126">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="7b861-127">في حقل "الاسم"، حدد WHS.</span><span class="sxs-lookup"><span data-stu-id="7b861-127">In the Name field, select WHS.</span></span>
11. <span data-ttu-id="7b861-128">في حقل "المستودع"، حدد المستودع 24.</span><span class="sxs-lookup"><span data-stu-id="7b861-128">In the Warehouse field, select warehouse 24.</span></span>
    * <span data-ttu-id="7b861-129">وهذا هو المستودع الافتراضي الذي سيتم استخدامه لبنود الإيصال المسجلة التي تستخدم ملف التعريف هذا.</span><span class="sxs-lookup"><span data-stu-id="7b861-129">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="7b861-130">في حقل "الموقع"، حدد "باب تحميل البضائع".</span><span class="sxs-lookup"><span data-stu-id="7b861-130">In the Location field, select Baydoor.</span></span>
    * <span data-ttu-id="7b861-131">وهذا هو الموقع الافتراضي الذي سيتم استخدامه لبنود الإيصال المسجلة التي تستخدم ملف التعريف هذا.</span><span class="sxs-lookup"><span data-stu-id="7b861-131">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="7b861-132">قم بتوسيع قسم "تفاصيل استعلام الوصول" أو طيّه.</span><span class="sxs-lookup"><span data-stu-id="7b861-132">Expand or collapse the Arrival query details section.</span></span>
14. <span data-ttu-id="7b861-133">في حقل "قيد الموقع"، حدد الموقع 2.</span><span class="sxs-lookup"><span data-stu-id="7b861-133">In the Restrict to site field, select site 2.</span></span>
    * <span data-ttu-id="7b861-134">يؤدي هذا الإجراء إلى تعيين عامل تصفية ليتم إظهار بنود الإيصال الموجودة في هذا الموقع فقط.</span><span class="sxs-lookup"><span data-stu-id="7b861-134">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="7b861-135">عيّن خيار "أوامر الشراء" إلى "نعم".</span><span class="sxs-lookup"><span data-stu-id="7b861-135">Set the Purchase orders option to Yes.</span></span>
    * <span data-ttu-id="7b861-136">حدد بنود الإيصال من أوامر الشراء.</span><span class="sxs-lookup"><span data-stu-id="7b861-136">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="7b861-137">عيّن خيار "أوامر التحويل" إلى "نعم".</span><span class="sxs-lookup"><span data-stu-id="7b861-137">Set the Transfer orders option to Yes.</span></span>
    * <span data-ttu-id="7b861-138">حدد بنود الإيصال من أوامر التحويل.</span><span class="sxs-lookup"><span data-stu-id="7b861-138">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="7b861-139">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="7b861-139">Click Save.</span></span>
18. <span data-ttu-id="7b861-140">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7b861-140">Close the page.</span></span>

