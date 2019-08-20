---
title: إنشاء أمر شراء من أمر توريد
description: يوضح لك هذا الإجراء إنشاء أمر شراء يستند إلى أمر مبيعات.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e5d7ce50532fb5bd6723b783d96d756085142e10
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843375"
---
# <a name="create-a-purchase-order-from-a-sales-order"></a><span data-ttu-id="45132-103">إنشاء أمر شراء من أمر توريد</span><span class="sxs-lookup"><span data-stu-id="45132-103">Create a purchase order from a sales order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="45132-104">يوضح لك هذا الإجراء إنشاء أمر شراء يستند إلى أمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="45132-104">This procedure shows you how to create a purchase order that is based on a sales order.</span></span> <span data-ttu-id="45132-105">ثم يتم تعيين كميات المنتج في أمر الشراء ثم يتم تعيينها لتلبية الطلب الخاص بأمر المبيعات الأصلي.</span><span class="sxs-lookup"><span data-stu-id="45132-105">The product's quantities on the purchase order are then designated to fulfill the demand of the originating sales order.</span></span> <span data-ttu-id="45132-106">تُعد تلبية طلب المبيعات بهذه الطريقة بديلاً لطريقة أكثر شمولاً وتحسينًا لتخطيط متطلبات التوزيع.</span><span class="sxs-lookup"><span data-stu-id="45132-106">Fulfilling sales demand this way is an alternative to a more comprehensive and optimized method of Distribution Requirements Planning.</span></span> <span data-ttu-id="45132-107">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF أو باستخدام بياناتك الخاصة.</span><span class="sxs-lookup"><span data-stu-id="45132-107">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="create-a-purchase-order-from-a-sales-order"></a><span data-ttu-id="45132-108">إنشاء أمر شراء من أمر توريد</span><span class="sxs-lookup"><span data-stu-id="45132-108">Create a purchase order from a sales order</span></span>
1. <span data-ttu-id="45132-109">انتقل إلى المبيعات والتسويق > أوامر المبيعات > كافة أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="45132-109">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="45132-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="45132-110">Click New.</span></span>
3. <span data-ttu-id="45132-111">في الحقل "حساب العميل"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="45132-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="45132-112">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="45132-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="45132-113">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="45132-113">Click OK.</span></span>
6. <span data-ttu-id="45132-114">في الحقل "رقم الصنف"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="45132-114">In the Item number field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="45132-115">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="45132-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="45132-116">إذا كنت تستخدم USMF، يمكنك تحديد "D0001".</span><span class="sxs-lookup"><span data-stu-id="45132-116">If you're using USMF, you could select D0001.</span></span>  
8. <span data-ttu-id="45132-117">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="45132-117">In the Quantity field, enter a number.</span></span>
9. <span data-ttu-id="45132-118">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="45132-118">Click Add line.</span></span>
10. <span data-ttu-id="45132-119">في الحقل "رقم الصنف"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="45132-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="45132-120">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="45132-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="45132-121">إذا كنت تستخدم USMF، يمكنك تحديد "T0020".</span><span class="sxs-lookup"><span data-stu-id="45132-121">If you're using USMF, you could select T0020.</span></span>  
12. <span data-ttu-id="45132-122">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="45132-122">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="45132-123">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="45132-123">In the Quantity field, enter a number.</span></span>
14. <span data-ttu-id="45132-124">انقر فوق حفظ.</span><span class="sxs-lookup"><span data-stu-id="45132-124">Click Save.</span></span>
15. <span data-ttu-id="45132-125">في جزء "الإجراءات"، انقر فوق "أمر المبيعات".</span><span class="sxs-lookup"><span data-stu-id="45132-125">On the Action Pane, click Sales order.</span></span>
16. <span data-ttu-id="45132-126">انقر فوق "أمر الشراء".</span><span class="sxs-lookup"><span data-stu-id="45132-126">Click Purchase order.</span></span>
    * <span data-ttu-id="45132-127">تسرد صفحة "إنشاء أمر المبيعات" جميع بنود أوامر المبيعات المفتوحة التي تم نسخها من أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="45132-127">The Create purchase order page lists all the open sales order lines which have been copied from the sales order.</span></span> <span data-ttu-id="45132-128">ويمكنك مراجعة تفاصيل الطلبات، وإذا لزم الأمر، يمكنك تعديل تفاصيل مثل كمية الشراء وشروط تحديد الأسعار قبل إنشاء المشتريات.</span><span class="sxs-lookup"><span data-stu-id="45132-128">You can review the order details, and if required, you can modify selected details such purchase quantity and pricing terms, before you create the purchases.</span></span>  
17. <span data-ttu-id="45132-129">حدد الخيار "تضمين الكل".</span><span class="sxs-lookup"><span data-stu-id="45132-129">Select the Include all option.</span></span>
    * <span data-ttu-id="45132-130">إذا كنت تريد إنشاء أوامر شراء لمجموعة فرعية فقط من بنود أوامر المبيعات، فحدد هذه على حدة.</span><span class="sxs-lookup"><span data-stu-id="45132-130">If you want to generate purchase orders for only a subset of the sales order lines, select these individually.</span></span>  
    * <span data-ttu-id="45132-131">قد يتم ملء الحقل "حساب المورد" أو قد لا يتم ملؤه بالفعل برقم مورد.</span><span class="sxs-lookup"><span data-stu-id="45132-131">The Vendor account field may or may not already be populated with a vendor number.</span></span> <span data-ttu-id="45132-132">إذا تم إعداد المورد الافتراضي للمنتج (على تغطية الصنف المقترن) سيتم نسخ المورد لهذا البند.</span><span class="sxs-lookup"><span data-stu-id="45132-132">If the default vendor is set up for the product (on the associated Item coverage) then this vendor will be copied  to the line.</span></span> <span data-ttu-id="45132-133">وإلا، يجب إدخال مورد يدوياً.</span><span class="sxs-lookup"><span data-stu-id="45132-133">Otherwise, you must enter a vendor manually.</span></span>  <span data-ttu-id="45132-134">في هذا الدليل، بغض النظر عما إذا كان الحقل "حساب المورد" يتضمن قيمة بالفعل أم لا، ستوجهك الخطوات التالية لتحديد مورد جديد مختلف لكل بند.</span><span class="sxs-lookup"><span data-stu-id="45132-134">In this guide, regardless of whether the Vendor account field already contains a value or not, the following steps instruct you to select a new vendor which is different for each line.</span></span>  
18. <span data-ttu-id="45132-135">في الحقل "حساب المورّد‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="45132-135">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="45132-136">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="45132-136">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="45132-137">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="45132-137">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="45132-138">حدد بند الأمر الثاني.</span><span class="sxs-lookup"><span data-stu-id="45132-138">Select the second order line.</span></span>
22. <span data-ttu-id="45132-139">في الحقل "حساب المورّد‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="45132-139">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="45132-140">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="45132-140">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="45132-141">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="45132-141">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="45132-142">انقر فوق "التحقق من الصحة‬".</span><span class="sxs-lookup"><span data-stu-id="45132-142">Click Validate.</span></span>
26. <span data-ttu-id="45132-143">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="45132-143">Click OK.</span></span>
    * <span data-ttu-id="45132-144">تُعلمك الرسالة أنه قد تم إنشاء أمر شراء واحد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="45132-144">The message informs you that one or more purchase orders have been created.</span></span> <span data-ttu-id="45132-145">يقوم النظام بإنشاء أمر شراء منفصل لكل مورد تحدد لبنود أمر المبيعات المحددة.</span><span class="sxs-lookup"><span data-stu-id="45132-145">The system generates a separate purchase order for each vendor that you specified for the sales order lines.</span></span> <span data-ttu-id="45132-146">ويعني هذا أنه إذا قام نفس المورد بتوفير عدة بنود أوامر مبيعات، سيتم إنشاء أمر شراء واحد ببنود متعددة.</span><span class="sxs-lookup"><span data-stu-id="45132-146">This means that if several sales order lines are to be supplied by the same vendor, a single purchase order with multiple lines will be generated.</span></span>  

## <a name="review-purchase-orders-created-from-sales-orders"></a><span data-ttu-id="45132-147">مراجعة أوامر الشراء التي تم إنشاؤها من أوامر المبيعات</span><span class="sxs-lookup"><span data-stu-id="45132-147">Review purchase orders created from sales orders</span></span>
1. <span data-ttu-id="45132-148">في جزء "الإجراءات"، انقر فوق "عام".</span><span class="sxs-lookup"><span data-stu-id="45132-148">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="45132-149">انقر فوق "الأوامر المرتبطة".</span><span class="sxs-lookup"><span data-stu-id="45132-149">Click Related orders.</span></span>
    * <span data-ttu-id="45132-150">تسر الصفحة "الأوامر ذات الصلة" جميع الأوامر التي تم إنشاؤها من أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="45132-150">The Related orders page lists all the orders that were created from the sales order.</span></span> <span data-ttu-id="45132-151">في هذا المثال، هناك أمرا شراء تم إنشاؤهما لموردين مختلفين على التوالي.</span><span class="sxs-lookup"><span data-stu-id="45132-151">In this example, there are two purchase orders generated for two different vendors respectively.</span></span>  
3. <span data-ttu-id="45132-152">انقر للمتابعة إلى الارتباط الموجود في الحقل "أمر الشراء".</span><span class="sxs-lookup"><span data-stu-id="45132-152">Click to follow the link in the Purchase order field.</span></span>
    * <span data-ttu-id="45132-153">يقترن كل بند أمر شراء ببند أمر المبيعات الذي أدى إلى الشراء.</span><span class="sxs-lookup"><span data-stu-id="45132-153">Each purchase order line is associated with the sales order line that led to the purchase.</span></span> <span data-ttu-id="45132-154">تتم الإشارة إلى العلاقة بأمر المبيعات بعلامة التبويب "المنتج" في علامة التبويب السريعة "تفاصيل البند" وفي الحقول "نوع المرجع" و"رقم المرجع" و"شحنة المرجع".</span><span class="sxs-lookup"><span data-stu-id="45132-154">The relation to the sales order is indicated on the Product tab in the Line details FastTab, in the Reference type, Reference number, and Reference lot fields.</span></span>  
4. <span data-ttu-id="45132-155">قم بتوسيع المقطع "تفاصيل البند" أو طيّه.</span><span class="sxs-lookup"><span data-stu-id="45132-155">Expand or collapse the Line details section.</span></span>
5. <span data-ttu-id="45132-156">انقر فوق علامة التبويب "المنتج".</span><span class="sxs-lookup"><span data-stu-id="45132-156">Click the Product tab.</span></span>
    * <span data-ttu-id="45132-157">وتضمن شحنة المرجع أنه يتم تحميل التكاليف من عملية الشراء الحالية على أمر المبيعات المرفق.</span><span class="sxs-lookup"><span data-stu-id="45132-157">The Reference lot guarantees that the costs from the current purchase are charged on the attached sales order.</span></span>  
    * <span data-ttu-id="45132-158">يمكنك التنقل إلى أمر المبيعات الأصلي عن طريق فتح الارتباط في الحقل "رقم المرجع".</span><span class="sxs-lookup"><span data-stu-id="45132-158">You can navigate to the originating sales order by opening the link in the Reference number field.</span></span>  

