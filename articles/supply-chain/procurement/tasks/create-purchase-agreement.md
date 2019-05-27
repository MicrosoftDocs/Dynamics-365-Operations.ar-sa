---
title: إنشاء اتفاقية شراء
description: يُرشدك هذا الإجراء خلال إنشاء اتفاقية شراء.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b317f0a0fc8f198bad9501f325557ac2a4796989
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547619"
---
# <a name="create-a-purchase-agreement"></a><span data-ttu-id="8285f-103">إنشاء اتفاقية شراء</span><span class="sxs-lookup"><span data-stu-id="8285f-103">Create a purchase agreement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8285f-104">يُرشدك هذا الإجراء خلال إنشاء اتفاقية شراء.</span><span class="sxs-lookup"><span data-stu-id="8285f-104">This procedure guides you through the creation of a purchase agreement.</span></span> <span data-ttu-id="8285f-105">يتم إجراء هذا عادة عن طريق إدارة الشراء.</span><span class="sxs-lookup"><span data-stu-id="8285f-105">This would typically be done by a purchasing manager.</span></span> <span data-ttu-id="8285f-106">يمكنك استخدام هذا الإجراء في شركة بيانات العرض التقديمي USMF، أو في البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="8285f-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="8285f-107">تحتاجُ إلى إعداد تصنيفات اتفاقيات الشراء قبل البدء.</span><span class="sxs-lookup"><span data-stu-id="8285f-107">You need to have set up purchase agreement classifications before you start.</span></span> <span data-ttu-id="8285f-108">بمجرد إنشاء اتفاقية يمكنك استخدامها عند إنشاء أمر مبيعات، وسيؤدي هذا إلى نسخ شروط اتفاقية الشراء للرأس وأي بنود في الأمر متأثرة بالاتفاقية.</span><span class="sxs-lookup"><span data-stu-id="8285f-108">Once you've created an agreement you can use it when you create a PO, and this will copy the purchase agreement conditions to the header and to any lines in the order that are affected by the agreement.</span></span>


## <a name="create-a-new-purchase-agreement"></a><span data-ttu-id="8285f-109">إنشاء اتفاقية شراء جديدة</span><span class="sxs-lookup"><span data-stu-id="8285f-109">Create a new purchase agreement</span></span>
1. <span data-ttu-id="8285f-110">انتقل إلى التدبير والتوريد > اتفاقيات الشراء > اتفاقيات الشراء.</span><span class="sxs-lookup"><span data-stu-id="8285f-110">Go to Procurement and sourcing > Purchase agreements > Purchase agreements.</span></span>
2. <span data-ttu-id="8285f-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="8285f-111">Click New.</span></span>
3. <span data-ttu-id="8285f-112">في الحقل "حساب المورّد‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="8285f-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="8285f-113">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="8285f-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="8285f-114">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="8285f-114">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="8285f-115">في الحقل "تصنيف اتفاقيات الشراء"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="8285f-115">In the Purchase agreement classification field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="8285f-116">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="8285f-116">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="8285f-117">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="8285f-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="8285f-118">قم بتوسيع القسم "عام".</span><span class="sxs-lookup"><span data-stu-id="8285f-118">Expand the General section.</span></span>
10. <span data-ttu-id="8285f-119">في الحقل "تاريخ انتهاء الصلاحية"، أدخل تاريخاً.</span><span class="sxs-lookup"><span data-stu-id="8285f-119">In the Expiration date field, enter a date.</span></span>
    * <span data-ttu-id="8285f-120">سيتم تعيين تاريخ الانتهاء الصلاحية هذا كتاريخ افتراضي لجميع بنود الالتزام وسيحدد مدة صلاحية كل التزام معين.</span><span class="sxs-lookup"><span data-stu-id="8285f-120">This expiration date will be the default for all commitment lines and will determine how long each specific commitment is valid.</span></span>  
11. <span data-ttu-id="8285f-121">في الحقل "عنوان المستند"، اكتب اسمًا لاتفاقية الشراء.</span><span class="sxs-lookup"><span data-stu-id="8285f-121">In the Document title field, type a name for your purchase agreement.</span></span>
    * <span data-ttu-id="8285f-122">اترك الحقل "الالتزام الافتراضي" معينًا على الالتزام بكمية المنتج (أو قم بتغييره إذا لم يكن معينًا على هذا.</span><span class="sxs-lookup"><span data-stu-id="8285f-122">Leave the Default commitment field set to Product quantity commitment (or change it if it’s not set to this).</span></span>  
    * <span data-ttu-id="8285f-123">تحدد قيمة الالتزام الافتراضية الخيارات المتعلقة ببنود الاتفاقية.</span><span class="sxs-lookup"><span data-stu-id="8285f-123">The default commitment value determines your options on the agreement lines.</span></span> <span data-ttu-id="8285f-124">إذا كنت بحاجة إلى نوع التزام جديد عندما تقوم بإنشاء بنود الاتفاقية، فستحتاج إلى تغيير الالتزام الافتراضي بالرأس.</span><span class="sxs-lookup"><span data-stu-id="8285f-124">If you need a new commitment type when you’re creating the agreement lines, you need to change the default commitment on the header.</span></span>  <span data-ttu-id="8285f-125">وهناك 4 أنواع من الالتزامات: الالتزام بكمية المنتج-لكمية معينة من المنتج؛ الالتزام بقيمة المنتج-لمبلغ من عملة معينة خاص بمنتج؛ الالتزام بقيمة فئة المنتج-لمبلغ من عملة معينة في فئة تدبير قد يكون المبلغ فيها لصنف خاص بالكتالوج أو صنف غير خاص بالكتالوج؛ الالتزام بالقيمة-لمبلغ من عملة يمكن أن يفي به أي منتج أو أية فئة تدبير.</span><span class="sxs-lookup"><span data-stu-id="8285f-125">There are 4 types of commitments: Product quantity commitment - for a specific quantity of a product; Product value commitment - for a specific currency amount of a product; Product category value commitment - for a specific currency amount in a procurement category where the amount can be for a catalog item or a non-catalog item; Value commitment - for a specific currency amount which can be fulfilled by any product or by any procurement category.</span></span>  
12. <span data-ttu-id="8285f-126">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="8285f-126">Click OK.</span></span>

## <a name="add-a-commitment"></a><span data-ttu-id="8285f-127">إضافة التزام</span><span class="sxs-lookup"><span data-stu-id="8285f-127">Add a commitment</span></span>
1. <span data-ttu-id="8285f-128">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="8285f-128">Click Add line.</span></span>
2. <span data-ttu-id="8285f-129">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="8285f-129">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="8285f-130">في الحقل "رقم الصنف"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="8285f-130">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="8285f-131">حدد المنتجات التي تريد إضافة التزام له.</span><span class="sxs-lookup"><span data-stu-id="8285f-131">Select the product you want to add a commitment for.</span></span>
5. <span data-ttu-id="8285f-132">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="8285f-132">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="8285f-133">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="8285f-133">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="8285f-134">هذا هو إجمالي الكمية التي وافقتَ على شراءها من المورد.</span><span class="sxs-lookup"><span data-stu-id="8285f-134">This is the total quantity that you have agreed to buy from your vendor.</span></span>  
7. <span data-ttu-id="8285f-135">في حقل "سعر الوحدة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="8285f-135">In the Unit price field, enter a number.</span></span>
8. <span data-ttu-id="8285f-136">قم بتوسيع قسم "تفاصيل البند".</span><span class="sxs-lookup"><span data-stu-id="8285f-136">Expand the Line details section.</span></span>
9. <span data-ttu-id="8285f-137">قم بتعيين الخيار "الحد الأقصى مفروض" على "نعم".</span><span class="sxs-lookup"><span data-stu-id="8285f-137">Set the Max is enforced option to Yes.</span></span>
    * <span data-ttu-id="8285f-138">يقيد الخيار "الحد الأقصى مفروض" استخدام الالتزام.</span><span class="sxs-lookup"><span data-stu-id="8285f-138">The Max is enforced option limits the use of the commitment.</span></span> <span data-ttu-id="8285f-139">لا يمكنك شراء كمية تتجاوز الكمية المحددة في الحقل "الكمية" للبند.</span><span class="sxs-lookup"><span data-stu-id="8285f-139">You can only purchase up to the quantity that's specified in the Quantity field for the line.</span></span>  
10. <span data-ttu-id="8285f-140">قم بطي قسم تفاصيل البند.</span><span class="sxs-lookup"><span data-stu-id="8285f-140">Collapse the Line details section.</span></span>

## <a name="add-header-conditions"></a><span data-ttu-id="8285f-141">إضافة شروط للرأس</span><span class="sxs-lookup"><span data-stu-id="8285f-141">Add header conditions</span></span>
1. <span data-ttu-id="8285f-142">في جزء الإجراءات، انقر فوق "خيارات".</span><span class="sxs-lookup"><span data-stu-id="8285f-142">On the Action Pane, click Options.</span></span>
2. <span data-ttu-id="8285f-143">انقر فوق "تغيير طريقة العرض‬".</span><span class="sxs-lookup"><span data-stu-id="8285f-143">Click Change view.</span></span>
3. <span data-ttu-id="8285f-144">انقر فوق "عرض الرأس".</span><span class="sxs-lookup"><span data-stu-id="8285f-144">Click Header view.</span></span>
4. <span data-ttu-id="8285f-145">قم بتوسيع مقطع "الشروط".</span><span class="sxs-lookup"><span data-stu-id="8285f-145">Expand the Terms section.</span></span>
5. <span data-ttu-id="8285f-146">في الحقل "طريقة الدفع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="8285f-146">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="8285f-147">تُعرض شروط الدفع من حساب المورد هنا بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="8285f-147">The payment terms from the vendor account are shown here by default.</span></span>       
6. <span data-ttu-id="8285f-148">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="8285f-148">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="8285f-149">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="8285f-149">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="8285f-150">في الحقل "وضع التسليم"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="8285f-150">In the Mode of delivery field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="8285f-151">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="8285f-151">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="8285f-152">في الحقل "شروط التسليم"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="8285f-152">In the Delivery terms field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="8285f-153">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="8285f-153">In the list, click the link in the selected row.</span></span>

## <a name="confirm-and-activate-the-agreement"></a><span data-ttu-id="8285f-154">تأكيد الاتفاقية وتفعيلها</span><span class="sxs-lookup"><span data-stu-id="8285f-154">Confirm and activate the agreement</span></span>
1. <span data-ttu-id="8285f-155">في جزء الإجراءات، انقر فوق "اتفاقية الشراء".</span><span class="sxs-lookup"><span data-stu-id="8285f-155">On the Action Pane, click Purchase agreement.</span></span>
2. <span data-ttu-id="8285f-156">انقر فوق"تأكيد".</span><span class="sxs-lookup"><span data-stu-id="8285f-156">Click Confirmation.</span></span>
    * <span data-ttu-id="8285f-157">قم بتعيين الخيار "تمييز الاتفاقية كاتفاقية فعالة" على "نعم".</span><span class="sxs-lookup"><span data-stu-id="8285f-157">Set the Mark agreement as effective option to Yes.</span></span>  
3. <span data-ttu-id="8285f-158">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="8285f-158">Click OK.</span></span>
4. <span data-ttu-id="8285f-159">في جزء الإجراءات، انقر فوق "اتفاقية الشراء".</span><span class="sxs-lookup"><span data-stu-id="8285f-159">On the Action Pane, click Purchase agreement.</span></span>
5. <span data-ttu-id="8285f-160">انقر فوق تأكيدات اتفاقيات الشراء.</span><span class="sxs-lookup"><span data-stu-id="8285f-160">Click Purchase agreement confirmations.</span></span>
    * <span data-ttu-id="8285f-161">يتيح لك الخيار "المعاينة/الطباعة" إنشاء مستند لاتفاقية الشراء التي يمكن طباعتها أو إرسالها للمورد بعد هذا.</span><span class="sxs-lookup"><span data-stu-id="8285f-161">The Preview/Print option allows you to generate a document for the purchase agreement which you can then print or send to the vendor.</span></span> <span data-ttu-id="8285f-162">في حالة تحديث الاتفاقية لاحقًا وإعادة تأكيدها، فسيُعرض كلا الإصدارين هنا.</span><span class="sxs-lookup"><span data-stu-id="8285f-162">If you update the agreement later on and re-confirm it, both versions will be shown here.</span></span>  
6. <span data-ttu-id="8285f-163">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8285f-163">Close the page.</span></span>

