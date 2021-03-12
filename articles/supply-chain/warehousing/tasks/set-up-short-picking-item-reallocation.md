---
title: إعداد إعادة توزيع الأصناف للانتقاء القصير
description: يوضح هذا الموضوع كيفية تمكين العاملين في المستودع من العثور بسرعة على مواقع بديلة في حال عدم وجود مخزون كافٍ في الموقع الذي تم توجيههم إليه.
author: ShylaThompson
manager: tfehr
ms.date: 06/29/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker, WHSLocationWithWorkException
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab8baf846d65e6fefe9ca575b5af5a2dbceac666
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976878"
---
# <a name="set-up-short-picking-item-reallocation"></a><span data-ttu-id="9e8a4-103">إعداد إعادة توزيع الأصناف للانتقاء القصير</span><span class="sxs-lookup"><span data-stu-id="9e8a4-103">Set up short picking item reallocation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9e8a4-104">يوضح هذا الإجراء كيفية تمكين العاملين في المستودع من العثور بسرعة على مواقع بديلة في حال عدم وجود مخزون كافٍ في الموقع الذي تم توجيههم إليه.</span><span class="sxs-lookup"><span data-stu-id="9e8a4-104">This procedure shows how to enable warehouse workers to quickly find alternative locations if there isn’t sufficient inventory at the location they’ve been directed to.</span></span> 

<span data-ttu-id="9e8a4-105">يتم التحكم في عملية إعادة التوزيع بواسطة **استثناءالعمل** ويستخدمه **عامل** المستودع.</span><span class="sxs-lookup"><span data-stu-id="9e8a4-105">The reallocation process is controlled by a **Work exception** and used by the warehouse **worker.**</span></span>

<span data-ttu-id="9e8a4-106">يمكن استخدام عمليات إعادة التوزيع التلقائية أو اليدوية أو كليهما:</span><span class="sxs-lookup"><span data-stu-id="9e8a4-106">It is possible to use Automatic, Manual, or both reallocation processes:</span></span>

- <span data-ttu-id="9e8a4-107">إعادة التوزيع التلقائية - يتم استخدام توجيهات الموقع لتحديد ما إذا كانت البضائع متوفرة في موقع آخر أم لا.</span><span class="sxs-lookup"><span data-stu-id="9e8a4-107">Automatic reallocation - Location directives are used to determine if the goods are available at another location.</span></span> <span data-ttu-id="9e8a4-108">إن أمكن ، سيتم تحديث العمل ويتم توجيه مستخدم المستودع إلى الموقع البديل.</span><span class="sxs-lookup"><span data-stu-id="9e8a4-108">If possible, the work will be updated and the warehouse user will be directed to the alternative location.</span></span>
- <span data-ttu-id="9e8a4-109">إعادة التوزيع اليدوي - يتيح لمستخدم المستودع التحديد من موقع واحد أو أكثر باستخدام كميات البضائع غير المحجوزة.</span><span class="sxs-lookup"><span data-stu-id="9e8a4-109">Manual reallocation - Allows the warehouse user to select from one or more locations with unreserved quantities of goods.</span></span> 
- <span data-ttu-id="9e8a4-110">تلقائي ويدوي - إذا كان النظام غير قادر على تنفيذ إعادة التوزيع التلقائي، والمواقع متوفرة مع وجود كميات غير محجوزة، ستتم مطالبة المستخدم بتحديد موقع.</span><span class="sxs-lookup"><span data-stu-id="9e8a4-110">Automatic and manual - If the system is unable to perform an automatic reallocation, and locations are available with unreserved quantities, the user will be prompted to select a location.</span></span>

## <a name="set-up-work-exceptions"></a><span data-ttu-id="9e8a4-111">إعداد استثناءات العمل</span><span class="sxs-lookup"><span data-stu-id="9e8a4-111">Set up work exceptions</span></span>
<span data-ttu-id="9e8a4-112">من الممكن تعريف عدة استثناءات عمل بواسطة سياسات إعادة توزيع أصناف مختلفة لتمكين العامل في المستودع من اختيار واحد بالاستناد إلى احتياجات الشحن التي يقوم بمعالجتها.</span><span class="sxs-lookup"><span data-stu-id="9e8a4-112">It's possible to define several work exceptions with different item reallocation policies to enable the warehouse worker to choose one based on the needs of the shipment that they are processing.</span></span>

<span data-ttu-id="9e8a4-113">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="9e8a4-113">The USMF demo data company was used to create this procedure.</span></span>

1. <span data-ttu-id="9e8a4-114">في **جزء التنقل**، انتقل إلى **إدارة المستودعات > الإعداد > العمل > استثناءات العمل**.</span><span class="sxs-lookup"><span data-stu-id="9e8a4-114">In the **Navigation pane**, go to **Warehouse management > Setup > Work > Work exceptions**.</span></span>
2. <span data-ttu-id="9e8a4-115">انقر فوق **جديد**</span><span class="sxs-lookup"><span data-stu-id="9e8a4-115">Click **New**</span></span> 
3. <span data-ttu-id="9e8a4-116">اكتب قيمة في حقل **كود استثناء العمل**.</span><span class="sxs-lookup"><span data-stu-id="9e8a4-116">In the **Work exception code** field, type a value.</span></span> <span data-ttu-id="9e8a4-117">سيكون هذا هو عنوان هذا الاستثناء.</span><span class="sxs-lookup"><span data-stu-id="9e8a4-117">This will be the title of this exception .</span></span> <span data-ttu-id="9e8a4-118">على سبيل المثال، دليل الانتقاء القصير.</span><span class="sxs-lookup"><span data-stu-id="9e8a4-118">For example, Short picking manual.</span></span>
4. <span data-ttu-id="9e8a4-119">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="9e8a4-119">In the **Description** field, type a value.</span></span> <span data-ttu-id="9e8a4-120">سيكون هذا وصفًا موجزًا لاستخدام هذا الاستثناء.</span><span class="sxs-lookup"><span data-stu-id="9e8a4-120">This will be a short description of the usage of this exception.</span></span> <span data-ttu-id="9e8a4-121">على سبيل المثال، انتقاء قصير - صنف غير متوفر.</span><span class="sxs-lookup"><span data-stu-id="9e8a4-121">For example, Short picking - item not available.</span></span>
5. <span data-ttu-id="9e8a4-122">في الحقل نوع **الاستثناء**، حدد **انتقاء قصير**.</span><span class="sxs-lookup"><span data-stu-id="9e8a4-122">In the **Exception** type field, select **Short pick**.</span></span>
6. <span data-ttu-id="9e8a4-123">حدد خانة الاختيار **تعديل المخزون**.</span><span class="sxs-lookup"><span data-stu-id="9e8a4-123">Select the **Adjust inventory** check box.</span></span> <span data-ttu-id="9e8a4-124">في حالة اختياره، ستتم تسوية المخزون بشكل تلقائي إلى 0 في موقع الانتقاء القصير.</span><span class="sxs-lookup"><span data-stu-id="9e8a4-124">If selected, inventory will automatically be adjusted to 0 at the short picked location.</span></span>
7. <span data-ttu-id="9e8a4-125">في حقل **كود نوع التسوية الافتراضي‬**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="9e8a4-125">In the **Default adjustment type code** field, enter or select a value.</span></span> <span data-ttu-id="9e8a4-126">على سبيل المثال، في USMF يمكنك تحديد **Remove Res Adj Out**. يحتوي كل كود نوع تسوية على أربعة خصائص: الاسم والوصف واسم دفتر يومية المخزون و **إزالة عمليات الحجز**.</span><span class="sxs-lookup"><span data-stu-id="9e8a4-126">For example, in USMF you can select **Remove Res Adj Out**. Each Adjustment type code contains four characteristics: name, description, inventory journal name, and **Remove reservations**.</span></span> <span data-ttu-id="9e8a4-127">في حالة تمكين **إزالة عمليات الحجز**، ستتم إزالة عمليات الحجز لبند الأمر قصير الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="9e8a4-127">If **Remove reservations** is enabled, the short-picked order line's reservations will be removed.</span></span>  
8. <span data-ttu-id="9e8a4-128">في حقل **إعادة توزيع الصنف**، حدد قيمة مثل، يدوي.</span><span class="sxs-lookup"><span data-stu-id="9e8a4-128">In the **Item reallocation** field, select a value, such as Manual.</span></span> <span data-ttu-id="9e8a4-129">إذا قمت بتحديد "يدوي"، أو "تلقائي ويدوي"، يجب تمكين عامل المستودع لاستخدام إعادة التوزيع اليدوي.</span><span class="sxs-lookup"><span data-stu-id="9e8a4-129">If you select Manual, or Automatic and Manual, the warehouse worker needs to be enabled to use manual reallocation.</span></span>

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a><span data-ttu-id="9e8a4-130">إعداد عامل لاستخدام إعادة التوزيع الأصناف يدويًا</span><span class="sxs-lookup"><span data-stu-id="9e8a4-130">Set up a worker to use manual item reallocation</span></span>

<span data-ttu-id="9e8a4-131">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="9e8a4-131">The USMF demo data company was used to create this procedure.</span></span>

1. <span data-ttu-id="9e8a4-132">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9e8a4-132">Close the page.</span></span>
2. <span data-ttu-id="9e8a4-133">في **جزء التنقل**، انتقل إلى **إدارة المستودعات > الإعداد > العامل**.</span><span class="sxs-lookup"><span data-stu-id="9e8a4-133">In the **Navigation pane**, go to **Warehouse management > Setup > Worker**.</span></span>
3. <span data-ttu-id="9e8a4-134">انقر فوق **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="9e8a4-134">Click **Edit**.</span></span>
4. <span data-ttu-id="9e8a4-135">في القائمة، حدد العامل.</span><span class="sxs-lookup"><span data-stu-id="9e8a4-135">In the list, select worker.</span></span> <span data-ttu-id="9e8a4-136">على سبيل المثال، جوليا فونديربورك.</span><span class="sxs-lookup"><span data-stu-id="9e8a4-136">For example, Julia Funderburk.</span></span>
5. <span data-ttu-id="9e8a4-137">وسّع علامة التبويب السريعة **المستخدمون**.</span><span class="sxs-lookup"><span data-stu-id="9e8a4-137">Expand the **Users** FastTab.</span></span>
6. <span data-ttu-id="9e8a4-138">في القائمة، حدد **معرف المستخدم**.</span><span class="sxs-lookup"><span data-stu-id="9e8a4-138">In the list, select a **User ID**.</span></span> <span data-ttu-id="9e8a4-139">على سبيل المثال، 24.</span><span class="sxs-lookup"><span data-stu-id="9e8a4-139">For example, 24.</span></span>
7. <span data-ttu-id="9e8a4-140">وسّع علامة التبويب السريعة **العمل**.</span><span class="sxs-lookup"><span data-stu-id="9e8a4-140">Expand the **Work** FastTab.</span></span>
8. <span data-ttu-id="9e8a4-141">حدد **نعم** في حقل **‏‫السماح بإعادة توزيع الأصناف يدويًا‬**.</span><span class="sxs-lookup"><span data-stu-id="9e8a4-141">Select **Yes** in the **Allow manual item reallocation** field.</span></span>
