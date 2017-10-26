--- 
title: "إنشاء أوامر التوريد"
description: "يوضح هذا الإجراء كيفية إنشاء أمر مبيعات."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 4ccd2c4ace41f07dce14498031e3cc29ecb61b1c
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="create-sales-orders"></a><span data-ttu-id="6b5e6-103">إنشاء أوامر التوريد</span><span class="sxs-lookup"><span data-stu-id="6b5e6-103">Create sales orders</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6b5e6-104">يوضح هذا الإجراء كيفية إنشاء أمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-104">This procedure shows you how to create a sales order.</span></span> <span data-ttu-id="6b5e6-105">يمكنك تنفيذ الإجراء في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-105">You can use the procedure in demo data company USMF.</span></span> <span data-ttu-id="6b5e6-106">يتم عادة إنشاء أوامر المبيعات بواسطة معالج أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-106">Sales orders are typically created by a sales order processor.</span></span> 




## <a name="enter-sales-order-header-details"></a><span data-ttu-id="6b5e6-107">إدخال تفاصيل رأس أمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="6b5e6-107">Enter sales order header details</span></span>
1. <span data-ttu-id="6b5e6-108">انتقل إلى المبيعات والتسويق > أوامر المبيعات > كافة أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-108">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="6b5e6-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="6b5e6-109">Click New.</span></span>
3. <span data-ttu-id="6b5e6-110">في الحقل "حساب العميل"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="6b5e6-111">في القائمة، ابحث عن سجل العميل وحدده.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-111">In the list, find and select the customer record.</span></span>
    * <span data-ttu-id="6b5e6-112">لهذا المثال، حدد رقم العميل US-004.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-112">For this example, select customer number US-004.</span></span>  
5. <span data-ttu-id="6b5e6-113">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="6b5e6-114">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="6b5e6-114">Click OK.</span></span>

## <a name="enter-sales-order-line-details"></a><span data-ttu-id="6b5e6-115">إدخال تفاصيل بند أمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="6b5e6-115">Enter sales order line details</span></span>
    * <span data-ttu-id="6b5e6-116">قد تأتي المنتجات التي تبيعها مؤسستك بأشكال مختلفة يتم التمييز بينها من خلال الأبعاد، مثل التكوين واللون والحجم والنمط.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-116">The products sold by your organization may come in variants differentiated by dimensions, such as configuration, color, size, and style.</span></span> <span data-ttu-id="6b5e6-117">علاوةً على ذلك، يمكن إعداد المنتجات لاستخدام أبعاد التخزين، مثل أبعاد الموقع والمستودع والبالتة‬ والرفوف، مثل أرقام المجموعة والأرقام التسلسلية.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-117">Also, products may be set up to use storage dimensions, such as site, warehouse, and pallet, and racking dimensions, such as batch and serial numbers.</span></span> <span data-ttu-id="6b5e6-118">عندما يتم تعيين هذه الأبعاد، يجب تحديد قيم لهذه الأبعاد في بند الأمر.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-118">When these dimensions are assigned, you must select the values for those dimensions on the order line.</span></span> <span data-ttu-id="6b5e6-119">ولتحسين كفاءة إدخال أمر، قد تحتاج إلى إضافة حقول الأبعاد المناظرة لشبكة الأمر.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-119">To improve order entry efficiency, you may want to add the respective dimension fields to the order grid.</span></span>  
1. <span data-ttu-id="6b5e6-120">انقر فوق بند أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-120">Click Sales order line.</span></span>
2. <span data-ttu-id="6b5e6-121">انقر فوق "الأبعاد".</span><span class="sxs-lookup"><span data-stu-id="6b5e6-121">Click Dimensions.</span></span>
    * <span data-ttu-id="6b5e6-122">على سبيل المثال، حدد أبعاد اللون والموقع والمستودع.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-122">For this example, select the Color, Site and Warehouse dimensions.</span></span> <span data-ttu-id="6b5e6-123">وسوف تظهر الأبعاد التي قمت بتحديدها هنا في شبكة أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-123">The dimensions you select here will appear in the sales order grid.</span></span> <span data-ttu-id="6b5e6-124">إذا أردت استمرار تحديداتك، فعيّن خيار "حفظ الإعداد" إلى "نعم".</span><span class="sxs-lookup"><span data-stu-id="6b5e6-124">If you want your selections to persist, set the Save setup option to Yes.</span></span>   
3. <span data-ttu-id="6b5e6-125">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="6b5e6-125">Click OK.</span></span>
4. <span data-ttu-id="6b5e6-126">في الحقل "رقم الصنف"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-126">In the Item number field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="6b5e6-127">لهذا المثال، حدد رقم الصنف T0004.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-127">For this example, select item number T0004.</span></span>
6. <span data-ttu-id="6b5e6-128">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-128">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="6b5e6-129">إذا كان الصنف جزءًا من فئة مبيعات، فسيظهر اسم الصنف تلقائيًا في الحقل "فئة المبيعات".</span><span class="sxs-lookup"><span data-stu-id="6b5e6-129">If the item is part of a sales category, the item name will automatically appear in the Sales category field.</span></span>  
    * <span data-ttu-id="6b5e6-130">إذا احتوت حقول أبعاد منتج على قيمة، فيعود سبب ذلك إلى نسخ القيمة من سجل المنتج حيث تم تعريفها كبعد منتج افتراضي.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-130">If product dimension fields already contain a value, this is because the value was copied from the product record where it is defined as a default product dimension.</span></span> <span data-ttu-id="6b5e6-131">يمكن تغيير القيمة الافتراضية في أي وقت.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-131">You can change the default value at any time.</span></span>   
7. <span data-ttu-id="6b5e6-132">في الحقل "اللون"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-132">In the Color field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="6b5e6-133">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-133">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="6b5e6-134">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-134">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="6b5e6-135">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-135">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="6b5e6-136">إذا تم بيع الصنف في وحدات مختلفة عند شرائه وإنتاجه وتخزينه، وتم تعيين "وحدة قياس مبيعات" في سجل المنتج، فستظهر هذه القيمة في حقل "الوحدة".</span><span class="sxs-lookup"><span data-stu-id="6b5e6-136">If the item is sold in different units than when it’s purchased, produced, and stored, and a sales unit of measure is set on the product record, this value will be shown in the Unit field.</span></span> <span data-ttu-id="6b5e6-137">يمكنك تغيير القيمة في أي وقت.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-137">You can change the value at any time.</span></span>   
    * <span data-ttu-id="6b5e6-138">إذا احتوى حقل "الموقع" على قيمة، فقد تم نسخ القيمة من رأس الأمر أو من إعدادات الأمر المقترنة بالمنتج.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-138">If the Site field already contains a value, the value was copied from the order header or from the order settings that are associated with the product.</span></span> <span data-ttu-id="6b5e6-139">يمكنك تغيير القيمة في أي وقت.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-139">You can change the value at any time.</span></span> <span data-ttu-id="6b5e6-140">إذا كان الحقل فارغًا، فحدد قيمة.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-140">If the field is empty, select a value.</span></span>   
    * <span data-ttu-id="6b5e6-141">إذا احتوى حقل "سعر الوحدة" على قيمة، فقد تم نسخ القيمة من اتفاقية تجارية صالحة أو من سجل المنتج.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-141">If the Unit price field already contains a value, the value was copied from a valid trade agreement, or from the product record.</span></span> <span data-ttu-id="6b5e6-142">(بإمكان سعر الوحدة أن ينشأ أيضًا من اتفاقية بيع، لكن عملية إنشاء أوامر المبيعات من اتفاقيات البيع تختلف عن تلك المعروضة هنا.) إذا كان الحقل فارغًا، فأدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-142">(The unit price can also originate from a sales agreement, but the process for creating sales orders from sales agreements is different to the one shown here.) If the field is empty, enter a value.</span></span>   
    * <span data-ttu-id="6b5e6-143">يحتوي الحقل "الخصم" على مبلغ خصم لكل وحدة منتج.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-143">The Discount field contains a discount amount per product unit.</span></span> <span data-ttu-id="6b5e6-144">لحساب إجمالي مبلغ خصم البند، يتم ضرب قيمة خصم بكمية بند.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-144">To calculate the total line discount amount, the discount value is multiplied by line quantity.</span></span>    <span data-ttu-id="6b5e6-145">إذا احتوى حقل "الخصم" على قيمة، فقد تم نسخ القيمة من اتفاقية تجارية صالحة.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-145">If the Discount field already contains a value, the value was copied from a valid trade agreement.</span></span> <span data-ttu-id="6b5e6-146">إذا كان الحقل فارغًا، وتريد إعطاء العميل خصم بند، فأدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-146">If the field is empty, and you want to give the customer a line discount, enter a value.</span></span>  
    * <span data-ttu-id="6b5e6-147">يحتوي الحقل "نسبة الخصم" على قيمة النسبة مئوية التي يجب استخدامها لخفض إجمالي مبلغ البند.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-147">The Discount percent field contains a percentage value by which the total line gross amount is to be reduced.</span></span>  <span data-ttu-id="6b5e6-148">إذا احتوى الحقل "نسبة الخصم" على قيمة، فقد تم نسخها من اتفاقية تجارية صالحة.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-148">If the Discount percent field already contains a value, it was copied from a valid trade agreement.</span></span> <span data-ttu-id="6b5e6-149">إذا كان الحقل فارغًا، وتريد إعطاء العميل خصم بند، فأدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-149">If the field is empty, and you want to give the customer a line discount, enter a value.</span></span>  
    * <span data-ttu-id="6b5e6-150">يحتوي الحقل "المبلغ الصافي" على قيمة يتم حسابها بناء على كمية البند وسعر الوحدة المعدّل بواسطة الخصومات.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-150">The Net amount field contains a value that is calculated based on the line's quantity and unit price adjusted by discounts.</span></span>  <span data-ttu-id="6b5e6-151">يمكنك تجاوز القيمة المحسوبة إلى أخرى مختلفة.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-151">You can override the calculated value to a different one.</span></span>  

## <a name="review-the-order-totals"></a><span data-ttu-id="6b5e6-152">مراجعة إجماليات الأوامر</span><span class="sxs-lookup"><span data-stu-id="6b5e6-152">Review the order totals</span></span>
1. <span data-ttu-id="6b5e6-153">في جزء "الإجراءات"، انقر فوق "أمر المبيعات".</span><span class="sxs-lookup"><span data-stu-id="6b5e6-153">On the Action Pane, click Sales order.</span></span>
2. <span data-ttu-id="6b5e6-154">انقر فوق "الإجماليات".</span><span class="sxs-lookup"><span data-stu-id="6b5e6-154">Click Totals.</span></span>
    * <span data-ttu-id="6b5e6-155">تعرض صفحة "الإجماليات" تفاصيل حول الأمر بأكمله.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-155">The Totals page displays details about the entire order.</span></span> <span data-ttu-id="6b5e6-156">ويشمل ذلك المبلغ الإجمالي الفرعي، وهو مجموع المبالغ الصافية لكل البنود وقد تم تعديله لخصومات البند النهائية، وإجمالي مبلغ الفاتورة، وهو مبلغ مجموع فرعي تم تعديله للخصم النهائي على مستوى الأمر، وضريبة المبيعات وحالة الحد الائتماني للعميل والمزيد.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-156">This includes the subtotal amount, which is a sum of all line net amounts adjusted for eventual line discounts, the total invoice amount, which is a subtotal amount adjusted for eventual order-level discount, charges, and sales tax, the customer credit limit situation, and more.</span></span>  <span data-ttu-id="6b5e6-157">مبلغ الفاتورة هو المبلغ الذي سيظهر على مستند الفاتورة للعميل.</span><span class="sxs-lookup"><span data-stu-id="6b5e6-157">The invoice amount is the amount that will appear on the customer's invoice document.</span></span>  
3. <span data-ttu-id="6b5e6-158">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="6b5e6-158">Click OK.</span></span>

