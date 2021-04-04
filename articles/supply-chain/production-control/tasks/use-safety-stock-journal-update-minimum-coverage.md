---
title: استخدام دفتر يومية المخزون الاحتياطي لتحديث الحد الأدنى للتغطية
description: يوضح هذا الإجراء كيفية حساب مقترحات الحد الأدنى للتغطية استنادًا إلى الحركات السابقة، ثم تحديث تغطية الصنف بواسطة المقترحات.
author: ChristianRytt
manager: tfehr
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 95dec1dba97923e58cfb603434a01cab6f66a3de
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252788"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a><span data-ttu-id="5c13d-103">استخدام دفتر يومية المخزون الاحتياطي لتحديث الحد الأدنى للتغطية</span><span class="sxs-lookup"><span data-stu-id="5c13d-103">Use the safety stock journal to update minimum coverage</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5c13d-104">يوضح هذا الإجراء كيفية حساب مقترحات الحد الأدنى للتغطية استنادًا إلى الحركات السابقة، ثم تحديث تغطية الصنف بواسطة المقترحات.</span><span class="sxs-lookup"><span data-stu-id="5c13d-104">This procedure shows how to calculate minimum coverage proposals based on historical transactions and then update the item coverage with the proposals.</span></span> <span data-ttu-id="5c13d-105">ويتم ذلك باستخدام دفتر يومية المخزون الاحتياطي.</span><span class="sxs-lookup"><span data-stu-id="5c13d-105">This is done using the safety stock journal.</span></span> <span data-ttu-id="5c13d-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USMF.‬</span><span class="sxs-lookup"><span data-stu-id="5c13d-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="5c13d-107">هذه المهمة مخصصة لمخطط الإنتاج، للمساعدة في الحفاظ على الحد الأدنى للتغطية.</span><span class="sxs-lookup"><span data-stu-id="5c13d-107">This task is intended for the production planner, to help maintain minimum coverage.</span></span>


## <a name="create-a-new-safety-stock-journal-name"></a><span data-ttu-id="5c13d-108">إنشاء اسم دفتر يومية مخزون احتياطي جديد</span><span class="sxs-lookup"><span data-stu-id="5c13d-108">Create a new safety stock journal name</span></span>
1. <span data-ttu-id="5c13d-109">في **جزء التنقل**، انتقل إلى **الوحدات النمطية > التخطيط الرئيسي > الإعداد > أسماء دفتر يومية المخزون الاحتياطي‬**.</span><span class="sxs-lookup"><span data-stu-id="5c13d-109">In the **Navigation pane**, go to **Master planning > Setup > Safety stock journal names**.</span></span>
2. <span data-ttu-id="5c13d-110">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="5c13d-110">Click **New**.</span></span>
3. <span data-ttu-id="5c13d-111">في حقل **الاسم، اكتب مواد**.</span><span class="sxs-lookup"><span data-stu-id="5c13d-111">In the **Name** field, type 'Material'.</span></span>
4. <span data-ttu-id="5c13d-112">في حقل **الوصف**، اكتب "مواد".</span><span class="sxs-lookup"><span data-stu-id="5c13d-112">In the **Description** field, type 'Material'.</span></span>
5. <span data-ttu-id="5c13d-113">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="5c13d-113">Close the page.</span></span>

## <a name="create-a-safety-stock-journal"></a><span data-ttu-id="5c13d-114">إنشاء دفتر يومية المخزون الاحتياطي</span><span class="sxs-lookup"><span data-stu-id="5c13d-114">Create a safety stock journal</span></span>
1. <span data-ttu-id="5c13d-115">في **جزء التنقل**، انتقل إلى **التخطيط الرئيسي > التخطيط الرئيسي > تشغيل > حساب المخزون الاحتياطي‬‬**.</span><span class="sxs-lookup"><span data-stu-id="5c13d-115">In the **Navigation pane**, go to **Master planning > Master planning > Run > Safety stock calculation**.</span></span>
2. <span data-ttu-id="5c13d-116">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="5c13d-116">Click **New**.</span></span>
3. <span data-ttu-id="5c13d-117">في الحقل **الاسم** أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="5c13d-117">In the **Name** field, enter or select a value.</span></span> <span data-ttu-id="5c13d-118">حدد اسم دفتر يومية المخزون الاحتياطي الذي قمت بإنشائه، على سبيل المثال، المواد.</span><span class="sxs-lookup"><span data-stu-id="5c13d-118">Select the safety stock journal name that you created, for example, Material.</span></span>  
4. <span data-ttu-id="5c13d-119">انقر فوق **إنشاء بنود**.</span><span class="sxs-lookup"><span data-stu-id="5c13d-119">Click **Create lines**.</span></span>
5. <span data-ttu-id="5c13d-120">في الحقل **من تاريخ**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="5c13d-120">In the **From date** field, enter a date.</span></span>  
6. <span data-ttu-id="5c13d-121">في الحقل **إلى تاريخ**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="5c13d-121">In the **To date** field, enter a date.</span></span>
7. <span data-ttu-id="5c13d-122">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5c13d-122">Click **OK**.</span></span> <span data-ttu-id="5c13d-123">سيؤدي ذلك إلى إنشاء بنود للأبعاد التي تحتوي على حركات المخزون.</span><span class="sxs-lookup"><span data-stu-id="5c13d-123">This will create lines for the dimensions that have inventory transactions.</span></span>  

## <a name="calculate-proposal"></a><span data-ttu-id="5c13d-124">مقترح الحساب</span><span class="sxs-lookup"><span data-stu-id="5c13d-124">Calculate proposal</span></span>
1. <span data-ttu-id="5c13d-125">انقر فوق **مقترح الحساب**.</span><span class="sxs-lookup"><span data-stu-id="5c13d-125">Click **Calculate proposal**.</span></span>
2. <span data-ttu-id="5c13d-126">حدد الخيار **استخدام متوسط الإصدار أثناء وقت الإنتاج**.</span><span class="sxs-lookup"><span data-stu-id="5c13d-126">Select the **Use average issue during lead time** option.</span></span>
3. <span data-ttu-id="5c13d-127">عيّن **معامل الضرب** إلى "10".</span><span class="sxs-lookup"><span data-stu-id="5c13d-127">Set **Multiplication factor** to '10'.</span></span> <span data-ttu-id="5c13d-128">يتم استخدام عامل الضرب لضبط المقترح.</span><span class="sxs-lookup"><span data-stu-id="5c13d-128">The Multiply factor is used to adjust the proposal.</span></span> <span data-ttu-id="5c13d-129">نظرًا لوجود عدد قليل من الحركات في بيانات العرض التوضيحي، ستحتاج إلى تعيين العامل للحصول على مقترح واقعي.</span><span class="sxs-lookup"><span data-stu-id="5c13d-129">Because demo data only has a few transactions, you will need to set the factor to get a realistic proposal.</span></span>  
4. <span data-ttu-id="5c13d-130">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5c13d-130">Click **OK**.</span></span> <span data-ttu-id="5c13d-131">قم بالتمرير للأسفل للعثور على M0002 وM0003.</span><span class="sxs-lookup"><span data-stu-id="5c13d-131">Scroll down to find M0002 and M0003.</span></span> <span data-ttu-id="5c13d-132">اعرض عمود **الحد الأدنى للكمية المحسوبة**.</span><span class="sxs-lookup"><span data-stu-id="5c13d-132">View the **Calculated minimum** quantity column.</span></span>   

## <a name="update-minimum-quantity"></a><span data-ttu-id="5c13d-133">تحديث الحد الأدنى للكمية</span><span class="sxs-lookup"><span data-stu-id="5c13d-133">Update minimum quantity</span></span>
1. <span data-ttu-id="5c13d-134">في الحقل **الحد الأدنى الجديد للكمية‬**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="5c13d-134">In the **New minimum quantity** field, enter a number.</span></span> <span data-ttu-id="5c13d-135">حدّث "الحد الأدنى الجديد للكمية‬" بحيث تتطابق الكمية مع القيمة في "الحد الأدنى للكمية المحسوبة‬".</span><span class="sxs-lookup"><span data-stu-id="5c13d-135">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="5c13d-136">إذا كانت قيمة الحد الأدنى للكمية المحسوبة‬ صفرًا، فيمكنك إدخال القيمة المستقبلية المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="5c13d-136">If the Calculated minimum is zero,  you can enter the desired future value.</span></span> <span data-ttu-id="5c13d-137">على سبيل المثال، يمكنك إدخال الحد الأدنى للكمية المحسوبة‬ في هذا الحقل للصنف M0002 ومستودعه 12.</span><span class="sxs-lookup"><span data-stu-id="5c13d-137">For example, you can enter the Calculated minimum quantity in this field for M0002 that has warehouse 12.</span></span>  
2. <span data-ttu-id="5c13d-138">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="5c13d-138">In the list, find and select the desired record.</span></span> <span data-ttu-id="5c13d-139">على سبيل المثال، يمكنك تحديد M0002 ومستودعه 12.</span><span class="sxs-lookup"><span data-stu-id="5c13d-139">For example, you can select M0002 that has warehouse 12.</span></span>  
3. <span data-ttu-id="5c13d-140">في الحقل **الحد الأدنى الجديد للكمية‬**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="5c13d-140">In the **New minimum quantity** field, enter a number.</span></span> <span data-ttu-id="5c13d-141">حدّث "الحد الأدنى الجديد للكمية‬" بحيث تتطابق الكمية مع القيمة في "الحد الأدنى للكمية المحسوبة‬".</span><span class="sxs-lookup"><span data-stu-id="5c13d-141">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="5c13d-142">إذا كانت قيمة الحد الأدنى للكمية المحسوبة‬ صفرًا، فيمكنك إدخال القيمة المستقبلية المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="5c13d-142">If the Calculated minimum is zero you can enter the desired future value.</span></span>  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a><span data-ttu-id="5c13d-143">ترحيل الحد الأدنى الجديد للكمية والتحقق من صحته</span><span class="sxs-lookup"><span data-stu-id="5c13d-143">Post the new minimum quantity and validate the result</span></span>
1. <span data-ttu-id="5c13d-144">انقر فوق **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="5c13d-144">Click **Post**.</span></span>
2. <span data-ttu-id="5c13d-145">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5c13d-145">Click **OK**.</span></span>
3. <span data-ttu-id="5c13d-146">انقر لمتابعة الارتباط في الحقل **رقم الصنف**.</span><span class="sxs-lookup"><span data-stu-id="5c13d-146">Click to follow the link in the **Item number** field.</span></span>
4. <span data-ttu-id="5c13d-147">انقر لمتابعة الارتباط في الحقل **رقم الصنف**.</span><span class="sxs-lookup"><span data-stu-id="5c13d-147">Click to follow the link in the **Item number** field.</span></span>
5. <span data-ttu-id="5c13d-148">في **جزء الإجراءات**، انقر فوق الخطة.</span><span class="sxs-lookup"><span data-stu-id="5c13d-148">On the **Action Pane**, click Plan.</span></span>
6. <span data-ttu-id="5c13d-149">انقر فوق **تغطية الصنف‬**.</span><span class="sxs-lookup"><span data-stu-id="5c13d-149">Click **Item coverage**.</span></span> <span data-ttu-id="5c13d-150">لاحظ أنه تم تحديث **الحد الأدنى للكمية**‬ بواسطة الحد الأدنى الجديد للكمية من دفتر يومية المخزون الاحتياطي.</span><span class="sxs-lookup"><span data-stu-id="5c13d-150">Notice that the **Minimum quantity** has been updated with the new minimum quantity from the safety stock journal.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]