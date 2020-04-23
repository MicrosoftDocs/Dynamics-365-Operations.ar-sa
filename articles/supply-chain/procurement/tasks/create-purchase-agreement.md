---
title: إنشاء اتفاقية شراء
description: يُرشدك هذا الموضوع عبر عملية إنشاء اتفاقية شراء.
author: mkirknel
manager: tfehr
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1edfd4e56910376d0596eec5eff2af888f7dc98d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207728"
---
# <a name="create-a-purchase-agreement"></a><span data-ttu-id="40130-103">إنشاء اتفاقية شراء</span><span class="sxs-lookup"><span data-stu-id="40130-103">Create a purchase agreement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="40130-104">يُرشدك هذا الموضوع عبر عملية إنشاء اتفاقية شراء.</span><span class="sxs-lookup"><span data-stu-id="40130-104">This topic guides you through the creation of a purchase agreement.</span></span> <span data-ttu-id="40130-105">يتم إجراء هذا عادة عن طريق إدارة الشراء.</span><span class="sxs-lookup"><span data-stu-id="40130-105">This would typically be done by a purchasing manager.</span></span> <span data-ttu-id="40130-106">يمكنك استخدام هذا الإجراء في شركة بيانات العرض التقديمي USMF، أو في البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="40130-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="40130-107">تحتاجُ إلى إعداد تصنيفات اتفاقيات الشراء قبل البدء.</span><span class="sxs-lookup"><span data-stu-id="40130-107">You need to have set up purchase agreement classifications before you start.</span></span> <span data-ttu-id="40130-108">بمجرد إنشاء اتفاقية يمكنك استخدامها عند إنشاء أمر مبيعات، وسيؤدي هذا إلى نسخ شروط اتفاقية الشراء للرأس وأي بنود في الأمر متأثرة بالاتفاقية.</span><span class="sxs-lookup"><span data-stu-id="40130-108">Once you've created an agreement you can use it when you create a PO, and this will copy the purchase agreement conditions to the header and to any lines in the order that are affected by the agreement.</span></span>


## <a name="create-a-new-purchase-agreement"></a><span data-ttu-id="40130-109">إنشاء اتفاقية شراء جديدة</span><span class="sxs-lookup"><span data-stu-id="40130-109">Create a new purchase agreement</span></span>
1. <span data-ttu-id="40130-110">انتقل إلى **جزء التنقل > الوحدات النمطية > التدبير والتوريد > اتفاقيات الشراء > اتفاقيات الشراء**.</span><span class="sxs-lookup"><span data-stu-id="40130-110">Go to **Navigation pane > Modules > Procurement and sourcing > Purchase agreements > Purchase agreements**.</span></span>
2. <span data-ttu-id="40130-111">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="40130-111">Click **New**.</span></span>
3. <span data-ttu-id="40130-112">في الحقل **حساب المورّد**، حدد القائمة المنسدلة وحدد صف السجل المطلوب.</span><span class="sxs-lookup"><span data-stu-id="40130-112">In the **Vendor account** field, select the drop-down menu and select the row of the desired record.</span></span>
4. <span data-ttu-id="40130-113">في الحقل **تصنيف اتفاقية الشراء‬**، حدد القائمة المنسدلة وحدد صف السجل المطلوب.</span><span class="sxs-lookup"><span data-stu-id="40130-113">In the **Purchase agreement classification** field, select the drop-down menu and select the row of the desired record.</span></span>
5. <span data-ttu-id="40130-114">قم بتوسيع علامة التبويب السريعة **عام**.</span><span class="sxs-lookup"><span data-stu-id="40130-114">Expand the **General** FastTab.</span></span>
6. <span data-ttu-id="40130-115">في الحقل **تاريخ انتهاء الصلاحية**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="40130-115">In the **Expiration date** field, enter a date.</span></span>

    - <span data-ttu-id="40130-116">سيتم تعيين تاريخ الانتهاء الصلاحية هذا كتاريخ افتراضي لجميع بنود الالتزام وسيحدد مدة صلاحية كل التزام معين.</span><span class="sxs-lookup"><span data-stu-id="40130-116">This expiration date will be the default for all commitment lines and will determine how long each specific commitment is valid.</span></span>  

7. <span data-ttu-id="40130-117">في الحقل **عنوان المستند**، اكتب اسمًا لاتفاقية الشراء.</span><span class="sxs-lookup"><span data-stu-id="40130-117">In the **Document title** field, type a name for your purchase agreement.</span></span>

    - <span data-ttu-id="40130-118">اترك الحقل **الالتزام الافتراضي** معينًا إلى **الالتزام بكمية المنتج** (أو قم بتغييره إذا لم يكن معينًا إلى هذا الخيار).</span><span class="sxs-lookup"><span data-stu-id="40130-118">Leave the **Default commitment** field set to **Product quantity commitment** (or change it if it's not set to this).</span></span>  
    - <span data-ttu-id="40130-119">تحدد قيمة الالتزام الافتراضية الخيارات المتعلقة ببنود الاتفاقية.</span><span class="sxs-lookup"><span data-stu-id="40130-119">The default commitment value determines your options on the agreement lines.</span></span> <span data-ttu-id="40130-120">إذا كنت بحاجة إلى نوع التزام جديد عندما تقوم بإنشاء بنود الاتفاقية، فستحتاج إلى تغيير الالتزام الافتراضي بالرأس.</span><span class="sxs-lookup"><span data-stu-id="40130-120">If you need a new commitment type when you're creating the agreement lines, you need to change the default commitment on the header.</span></span> <span data-ttu-id="40130-121">وهناك 4 أنواع من الالتزامات: **الالتزام بكمية المنتج** -لكمية معينة من المنتج؛ **الالتزام بقيمة المنتج** - لمبلغ من عملة معينة خاص بمنتج؛ **الالتزام بقيمة فئة المنتج** - لمبلغ من عملة معينة في فئة تدبير قد يكون المبلغ فيها لصنف خاص بالكتالوج أو صنف غير خاص بالكتالوج؛ **الالتزام بالقيمة** - لمبلغ من عملة معينة يمكن أن يفي به أي منتج أو أية فئة تدبير.</span><span class="sxs-lookup"><span data-stu-id="40130-121">There are 4 types of commitments: **Product quantity commitment** - for a specific quantity of a product; **Product value commitment** - for a specific currency amount of a product; **Product category value commitment** - for a specific currency amount in a procurement category where the amount can be for a catalog item or a non-catalog item; **Value commitment** - for a specific currency amount which can be fulfilled by any product or by any procurement category.</span></span>  

8. <span data-ttu-id="40130-122">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="40130-122">Select **OK**.</span></span>

## <a name="add-a-commitment"></a><span data-ttu-id="40130-123">إضافة التزام</span><span class="sxs-lookup"><span data-stu-id="40130-123">Add a commitment</span></span>
1. <span data-ttu-id="40130-124">حدد **إضافة بند**.</span><span class="sxs-lookup"><span data-stu-id="40130-124">Select **Add line**.</span></span>
2. <span data-ttu-id="40130-125">في الحقل **رقم الصنف**، انقر فوق السجل المطلوب من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="40130-125">In the **Item number** field, select the desired record from the drop-down menu.</span></span>
3. <span data-ttu-id="40130-126">في الحقل **الكمية**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="40130-126">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="40130-127">هذا هو إجمالي الكمية التي وافقتَ على شراءها من المورد.</span><span class="sxs-lookup"><span data-stu-id="40130-127">This is the total quantity that you have agreed to buy from your vendor.</span></span>  
4. <span data-ttu-id="40130-128">في حقل **سعر الوحدة**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="40130-128">In the **Unit price** field, enter a number.</span></span>
5. <span data-ttu-id="40130-129">قم بتوسيع قسم **تفاصيل البند**.</span><span class="sxs-lookup"><span data-stu-id="40130-129">Expand the **Line details** section.</span></span>
6. <span data-ttu-id="40130-130">قم بتعيين الخيار **الحد الأقصى مفروض** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="40130-130">Set the **Max is enforced** option to **Yes**.</span></span> <span data-ttu-id="40130-131">يقيد الخيار **الحد الأقصى مفروض** استخدام الالتزام.</span><span class="sxs-lookup"><span data-stu-id="40130-131">The **Max is enforced** option limits the use of the commitment.</span></span> <span data-ttu-id="40130-132">لا يمكنك شراء كمية تتجاوز الكمية المحددة في الحقل **الكمية** للبند.</span><span class="sxs-lookup"><span data-stu-id="40130-132">You can only purchase up to the quantity that's specified in the **Quantity** field for the line.</span></span>  

## <a name="add-header-conditions"></a><span data-ttu-id="40130-133">إضافة شروط للرأس</span><span class="sxs-lookup"><span data-stu-id="40130-133">Add header conditions</span></span>
1. <span data-ttu-id="40130-134">في جزء الإجراءات، حدد **خيارات**.</span><span class="sxs-lookup"><span data-stu-id="40130-134">On the Action Pane, select **Options**.</span></span>
2. <span data-ttu-id="40130-135">حدد **تغيير طريقة العرض**.</span><span class="sxs-lookup"><span data-stu-id="40130-135">Select **Change view**.</span></span>
3. <span data-ttu-id="40130-136">حدد **طريقة عرض الرأس**.</span><span class="sxs-lookup"><span data-stu-id="40130-136">Select **Header view**.</span></span>
4. <span data-ttu-id="40130-137">قم بتوسيع مقطع **الشروط**.</span><span class="sxs-lookup"><span data-stu-id="40130-137">Expand the **Terms** section.</span></span>
5. <span data-ttu-id="40130-138">في حقل **طريقة الدفع**، حدد السجل المطلوب في القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="40130-138">In the **Method of payment** field, select the desired record in the drop-down menu.</span></span> <span data-ttu-id="40130-139">تُعرض شروط الدفع من حساب المورد هنا بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="40130-139">The payment terms from the vendor account are shown here by default.</span></span>  
6. <span data-ttu-id="40130-140">في حقل **طريقة التسليم**، حدد السجل المطلوب في القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="40130-140">In the **Mode of delivery** field, select the desired record in the drop-down menu.</span></span>
7. <span data-ttu-id="40130-141">في الحقل **شروط التسليم**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="40130-141">In the **Delivery terms** field, select the drop-down button to open the lookup.</span></span>

## <a name="confirm-and-activate-the-agreement"></a><span data-ttu-id="40130-142">تأكيد الاتفاقية وتفعيلها</span><span class="sxs-lookup"><span data-stu-id="40130-142">Confirm and activate the agreement</span></span>
1. <span data-ttu-id="40130-143">في جزء الإجراءات، انقر فوق **اتفاقية الشراء**.</span><span class="sxs-lookup"><span data-stu-id="40130-143">On the Action Pane, select **Purchase agreement**.</span></span>
2. <span data-ttu-id="40130-144">حدد **تأكيد**.</span><span class="sxs-lookup"><span data-stu-id="40130-144">Select **Confirmation**.</span></span> <span data-ttu-id="40130-145">قم بتعيين الخيار **تمييز الاتفاقية كاتفاقية فعالة** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="40130-145">Set the **Mark agreement as effective** option to **Yes**.</span></span>  
3. <span data-ttu-id="40130-146">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="40130-146">Select **OK**.</span></span>
4. <span data-ttu-id="40130-147">في جزء الإجراءات، انقر فوق **اتفاقية الشراء**.</span><span class="sxs-lookup"><span data-stu-id="40130-147">On the Action Pane, select **Purchase agreement**.</span></span>
5. <span data-ttu-id="40130-148">حدد **تأكيدات اتفاقية الشراء**.</span><span class="sxs-lookup"><span data-stu-id="40130-148">Select **Purchase agreement confirmations**.</span></span> <span data-ttu-id="40130-149">يتيح لك الخيار **المعاينة/الطباعة** إنشاء مستند لاتفاقية الشراء التي يمكن عندئذٍ طباعتها أو إرسالها إلى المورّد.</span><span class="sxs-lookup"><span data-stu-id="40130-149">The **Preview/Print** option allows you to generate a document for the purchase agreement which you can then print or send to the vendor.</span></span> <span data-ttu-id="40130-150">في حالة تحديث الاتفاقية لاحقًا وإعادة تأكيدها، فسيُعرض كلا الإصدارين هنا.</span><span class="sxs-lookup"><span data-stu-id="40130-150">If you update the agreement later on and re-confirm it, both versions will be shown here.</span></span>  
6. <span data-ttu-id="40130-151">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="40130-151">Close the page.</span></span>

