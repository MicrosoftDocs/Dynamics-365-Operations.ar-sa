---
title: تهيئة مستويات المخزون في المستودع
description: يوضح هذا الإجراء كيفية تحديث المخزون المتاح يدوياً باستخدام دفتر يومية حركة مخزون.
author: perlynne
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalMovement, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6934fc8142a589532cbd9d360ca0f8276456b20e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011537"
---
# <a name="initialize-stock-levels-in-the-warehouse"></a><span data-ttu-id="54398-103">تهيئة مستويات المخزون في المستودع</span><span class="sxs-lookup"><span data-stu-id="54398-103">Initialize stock levels in the warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="54398-104">يوضح هذا الإجراء كيفية تحديث المخزون المتاح يدوياً باستخدام دفتر يومية حركة مخزون.</span><span class="sxs-lookup"><span data-stu-id="54398-104">This procedure shows you how to get the on-hand inventory updated manually using an Inventory movement journal.</span></span> <span data-ttu-id="54398-105">(ومن الممكن أيضا تحديث المخزون المتاح عن طريق استيراد الحركات في وحدات البيانات.) يمكنك تشغيل هذا الدليل في شركة بيانات العرض التقديمي USMF حيث تتوفر جميع المتطلبات الأساسية مثل اسم دفتر اليومية وإعداد الصنف وملفات تعريف الترحيل والحسابات.</span><span class="sxs-lookup"><span data-stu-id="54398-105">(It's also possible to update on-hand inventory by importing transactions in data entities.) You can run this guide in demo data company USMF where all the prerequisites like journal name, item setup, posting profiles, and accounts are available.</span></span> <span data-ttu-id="54398-106">يقترح هذا الدليل قيمًا معينة للصنف والأبعاد المستخدمة.</span><span class="sxs-lookup"><span data-stu-id="54398-106">The guide suggests specific values for the item and dimensions that are used.</span></span> <span data-ttu-id="54398-107">إذا اخترتَ عنصرًا مختلفًا، فقد تحتاجُ إلى إدخال قيم لأبعاد مختلفة.</span><span class="sxs-lookup"><span data-stu-id="54398-107">If you choose a different item, you may need to enter values for different dimensions.</span></span>

1. <span data-ttu-id="54398-108">انتقل إلى إدارة المخزون > إدخالات دفتر اليومية > الأصناف > الحركة.</span><span class="sxs-lookup"><span data-stu-id="54398-108">Go to Inventory management > Journal entries > Items > Movement.</span></span>
2. <span data-ttu-id="54398-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="54398-109">Click New.</span></span>
3. <span data-ttu-id="54398-110">في الحقل "الاسم"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="54398-110">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="54398-111">حدد IMov "حركية الأصناف".</span><span class="sxs-lookup"><span data-stu-id="54398-111">Select IMov.</span></span>
    * <span data-ttu-id="54398-112">من المفيد استخدام قوالب أسماء دفاتر يوميات مختلفة للأغراض التجارية المختلفة.</span><span class="sxs-lookup"><span data-stu-id="54398-112">It's a good practice to use different journal name templates for the different business purposes.</span></span>  
5. <span data-ttu-id="54398-113">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="54398-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="54398-114">في الحقل "الحساب المقابل"، حدد القيم "140200".</span><span class="sxs-lookup"><span data-stu-id="54398-114">In the Offset account field, specify the values '140200'.</span></span>
    * <span data-ttu-id="54398-115">يعتبر هذا هو الحساب المقابل الذي سيكون الحساب الافتراضي لبنود دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="54398-115">This is the offset account that will be the default account on the journal lines.</span></span> <span data-ttu-id="54398-116">من الممكن تجاوز الحساب الافتراضي لتعيين حسابات مقابلة مختلف لكل بند.</span><span class="sxs-lookup"><span data-stu-id="54398-116">It's possible to override the default to assign different offset accounts per line.</span></span>  
7. <span data-ttu-id="54398-117">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="54398-117">Click OK.</span></span>
8. <span data-ttu-id="54398-118">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="54398-118">Click New.</span></span>
9. <span data-ttu-id="54398-119">في الحقل "رقم الصنف"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="54398-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="54398-120">حدد الصنف A0001.</span><span class="sxs-lookup"><span data-stu-id="54398-120">Select item A0001.</span></span>
11. <span data-ttu-id="54398-121">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="54398-121">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="54398-122">انقر فوق علامة التبويب "أبعاد المخزون".</span><span class="sxs-lookup"><span data-stu-id="54398-122">Click the Inventory dimensions tab.</span></span>
13. <span data-ttu-id="54398-123">في الحقل "الموقع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="54398-123">In the Site field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="54398-124">حدد الموقع 1.</span><span class="sxs-lookup"><span data-stu-id="54398-124">Select site 1.</span></span>
15. <span data-ttu-id="54398-125">في الحقل "المستودع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="54398-125">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="54398-126">حديد المستودع 13.</span><span class="sxs-lookup"><span data-stu-id="54398-126">Select warehouse 13.</span></span>
17. <span data-ttu-id="54398-127">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="54398-127">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="54398-128">في الحقل "الموقع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="54398-128">In the Location field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="54398-129">حدد الموقع 13.</span><span class="sxs-lookup"><span data-stu-id="54398-129">Select location 13.</span></span>
20. <span data-ttu-id="54398-130">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="54398-130">In the Quantity field, enter a number.</span></span>
21. <span data-ttu-id="54398-131">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="54398-131">Click Save.</span></span>
22. <span data-ttu-id="54398-132">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="54398-132">Click Post.</span></span>
23. <span data-ttu-id="54398-133">قم بتحديد خانة اختيار "نقل جميع أخطاء الترحيل إلى دفتر يومية جديد" أو إلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="54398-133">Check or uncheck the Transfer all posting errors to a new journal check box.</span></span>
    * <span data-ttu-id="54398-134">إذا قمت بتمكين هذا الخيار، سيتم نسخ أي بنود يفشل ترحيلها إلى دفتر يومية جديد.</span><span class="sxs-lookup"><span data-stu-id="54398-134">If you enable this option, any lines that fail to post will be copied to a new journal.</span></span> <span data-ttu-id="54398-135">يمكنك استخدام المعلومات في السجل لتصحيح المشكلات ثم إعادة ترحيل البنود.</span><span class="sxs-lookup"><span data-stu-id="54398-135">You can use the information in the log to correct the issues and then re-post the lines.</span></span>  
24. <span data-ttu-id="54398-136">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="54398-136">Click OK.</span></span>
25. <span data-ttu-id="54398-137">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="54398-137">Close the page.</span></span>
26. <span data-ttu-id="54398-138">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="54398-138">Close the page.</span></span>

