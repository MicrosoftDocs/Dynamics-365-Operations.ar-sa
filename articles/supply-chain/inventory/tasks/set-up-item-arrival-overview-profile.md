---
title: إعداد ملف تعريف نظرة عامة على وصول الصنف
description: يركز هذا الموضوع على إعداد ملف تعريف النظرة العامة على الوصول.
author: ShylaThompson
manager: tfehr
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 69389dd3a53ffec11116e16512bd038b45eda4d4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421626"
---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="391c5-103">إعداد ملف تعريف نظرة عامة على وصول الصنف</span><span class="sxs-lookup"><span data-stu-id="391c5-103">Set up an item arrival overview profile</span></span>

<span data-ttu-id="391c5-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="391c5-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="391c5-105">يركز هذا الموضوع على إعداد ملف تعريف النظرة العامة على الوصول.</span><span class="sxs-lookup"><span data-stu-id="391c5-105">This topic focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="391c5-106">إن ملف تعريف النظرة العامة على الوصول عبارة عن مجموعة من القواعد التي سيتم تطبيقها عند فتح صفحة "نظرة عامة على الوصول" من قِبل المستخدم.</span><span class="sxs-lookup"><span data-stu-id="391c5-106">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="391c5-107">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="391c5-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="391c5-108">يقوم موظف الاستلام عادةً بتنفيذ هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="391c5-108">This procedure would typically be carried out by a receiving clerk.</span></span>

1. <span data-ttu-id="391c5-109">في جزء التنقل، انتقل إلى **الوحدات النمطية > إدارة المخزون > الإعداد > التوزيع > ملفات تعريف النظرة العامة على الوصول‬**.</span><span class="sxs-lookup"><span data-stu-id="391c5-109">In the navigation pane, go to **Modules > Inventory management > Setup > Distribution > Arrival overview profiles**.</span></span>
2. <span data-ttu-id="391c5-110">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="391c5-110">Select **New**.</span></span> <span data-ttu-id="391c5-111">نظرًا لأنك ستعمل دائماً في نفس المستودع في تفريغ حمولات الشاحنات الكاملة، يجب عليك إنشاء ملف تعريف نظرة عامة حول الوصول لتبسيط عملية تسجيل الأصناف المستلمة.</span><span class="sxs-lookup"><span data-stu-id="391c5-111">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="391c5-112">في الحقل **اسم ملف تعريف النظرة العامة على الوصول**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="391c5-112">In the **Arrival overview profile name** field, type a value.</span></span>
4. <span data-ttu-id="391c5-113">في الحقل **إظهار البنود**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="391c5-113">In the **Show lines** field, select an option.</span></span> <span data-ttu-id="391c5-114">حدد البنود التي تريد إظهارها لعمليات الاستلام:</span><span class="sxs-lookup"><span data-stu-id="391c5-114">Select which lines to show for the receipts:</span></span>  

    - <span data-ttu-id="391c5-115">**الكل** – إظهار كافة البنود، بصرف النظر عن الحالة.</span><span class="sxs-lookup"><span data-stu-id="391c5-115">**All** – Show all lines, regardless of status.</span></span>   
    - <span data-ttu-id="391c5-116">**قيد التقدم** -إظهار البنود الخاصة بعمليات الاستلام التي يكون فيها تقدم العملية مكتمل أو جزئي.</span><span class="sxs-lookup"><span data-stu-id="391c5-116">**In progress** – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="391c5-117">وهذا يعني أنه بالنسبة لكل بند، تم تسجيل إما كل الكمية أو جزء منها في دفتر يومية الوصول.</span><span class="sxs-lookup"><span data-stu-id="391c5-117">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   
    - <span data-ttu-id="391c5-118">**غير مكتملة** - إظهار البنود الخاصة بعمليات الاستلام التي يكون فيها تقدم العملية "بلا" أو "جزئي".</span><span class="sxs-lookup"><span data-stu-id="391c5-118">**Not complete** – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="391c5-119">وهذا يعني أنه بالنسبة لكل بند، لم يتم تسجيل أي شيء من الكمية أو أنه قد تم تسجيل جزء منها فقط في دفتر يومية الوصول.</span><span class="sxs-lookup"><span data-stu-id="391c5-119">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  

5. <span data-ttu-id="391c5-120">قم بتوسيع القسم **خيارات الوصول** أو طيه.</span><span class="sxs-lookup"><span data-stu-id="391c5-120">Expand or collapse the **Arrival options** section.</span></span>
6. <span data-ttu-id="391c5-121">في الحقل **الأيام التالية**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="391c5-121">In the **Days forward** field, type a value.</span></span> <span data-ttu-id="391c5-122">يؤدي هذا إلى تعيين عامل تصفية لإظهار بنود الإيصال المتوقع استلامها خلال الأيام القليلة القادمة (اعتماداً على الرقم الذي قمت بتعيينه).</span><span class="sxs-lookup"><span data-stu-id="391c5-122">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="391c5-123">في الحقل **الأيام السابقة**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="391c5-123">In the **Days back** field, type a value.</span></span> <span data-ttu-id="391c5-124">يؤدي هذا إلى تعيين عامل تصفية لإظهار بنود الإيصال المتوقع استلامها منذ عدة أيام سابقة.</span><span class="sxs-lookup"><span data-stu-id="391c5-124">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="391c5-125">في الحقل **المستودعات**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="391c5-125">In the **Warehouses** field, type a value.</span></span> <span data-ttu-id="391c5-126">قم بإجراء التصفية بمستودع واحد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="391c5-126">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="391c5-127">في الحقل **وضع التسليم**، حدد قيمة</span><span class="sxs-lookup"><span data-stu-id="391c5-127">In the **Mode of delivery** field, select a value.</span></span> <span data-ttu-id="391c5-128">يؤدي هذا الإجراء إلى تعيين عامل تصفية ليتم إظهار بنود الإيصال التي تم تسليمها في هذا الوضع فقط.</span><span class="sxs-lookup"><span data-stu-id="391c5-128">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="391c5-129">في حقل **الاسم**، حدد WHS.</span><span class="sxs-lookup"><span data-stu-id="391c5-129">In the **Name** field, select WHS.</span></span>
11. <span data-ttu-id="391c5-130">في حقل **المستودع**، حدد المستودع 24.</span><span class="sxs-lookup"><span data-stu-id="391c5-130">In the **Warehouse** field, select warehouse 24.</span></span> <span data-ttu-id="391c5-131">وهذا هو المستودع الافتراضي الذي سيتم استخدامه لبنود الإيصال المسجلة التي تستخدم ملف التعريف هذا.</span><span class="sxs-lookup"><span data-stu-id="391c5-131">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="391c5-132">في حقل **الموقع**، حدد **باب تحميل البضائع**.</span><span class="sxs-lookup"><span data-stu-id="391c5-132">In the **Location** field, select **Baydoor**.</span></span> <span data-ttu-id="391c5-133">وهذا هو الموقع الافتراضي الذي سيتم استخدامه لبنود الإيصال المسجلة التي تستخدم ملف التعريف هذا.</span><span class="sxs-lookup"><span data-stu-id="391c5-133">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="391c5-134">قم بتوسيع قسم **تفاصيل استعلام الوصول** أو طيّه.</span><span class="sxs-lookup"><span data-stu-id="391c5-134">Expand or collapse the **Arrival query details** section.</span></span>
14. <span data-ttu-id="391c5-135">في حقل **التقيد بالموقع**، حدد الموقع 2.</span><span class="sxs-lookup"><span data-stu-id="391c5-135">In the **Restrict to site** field, select site 2.</span></span> <span data-ttu-id="391c5-136">يؤدي هذا الإجراء إلى تعيين عامل تصفية ليتم إظهار بنود الإيصال الموجودة في هذا الموقع فقط.</span><span class="sxs-lookup"><span data-stu-id="391c5-136">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="391c5-137">عيّن خيار **أوامر الشراء** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="391c5-137">Set the **Purchase orders** option to **Yes**.</span></span> <span data-ttu-id="391c5-138">حدد بنود الإيصال من أوامر الشراء.</span><span class="sxs-lookup"><span data-stu-id="391c5-138">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="391c5-139">عيّن خيار أوامر **التحويل** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="391c5-139">Set the **Transfer** orders option to **Yes**.</span></span> <span data-ttu-id="391c5-140">حدد بنود الإيصال من أوامر التحويل.</span><span class="sxs-lookup"><span data-stu-id="391c5-140">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="391c5-141">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="391c5-141">Select **Save**.</span></span>
18. <span data-ttu-id="391c5-142">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="391c5-142">Close the page.</span></span>

