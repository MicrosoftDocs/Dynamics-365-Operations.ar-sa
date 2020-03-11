---
title: سياسة مرنة لحجز البعد على مستوى المستودع
description: يصف هذا الموضوع نهج حجز المخزون الذي يجب علي الشركات التي تقوم ببيع المنتجات التي تتبع المجموعات وتشغيل التجهيزات الخاصة به كعمليات ممكنة ل WMS-بحجز مجموعات محدده لأوامر توريد العميل ، حتى وان كان التدرج الهرمي للحجز الذي يتم المرتبطة بالمنتجات لا تسمح بحجز الدفعات الخاصة.
author: omulvad
manager: AnnBe
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReservationHierarchy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: cd6ec1013de757214db99ada02170bb6e2af96c0
ms.sourcegitcommit: f52ddcad105aac4ad2caef709751ff80caf363c0
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/11/2020
ms.locfileid: "3036919"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a><span data-ttu-id="23ef4-103">سياسة مرنة لحجز البعد على مستوى المستودع</span><span class="sxs-lookup"><span data-stu-id="23ef4-103">Flexible warehouse-level dimension reservation policy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="23ef4-104">عندما يكون نوع التسلسل الهرمي الخاص بحجز\[المخزون للنوع "الدفعة تحت الموقع\]" مقترنا بالمنتجات، لا يمكن للشركات التي تقوم Microsoft Dynamics 365ببيع المنتجات التي تتبع المجموعات وتشغيل التجهيزات الخاصة بها لنظام أداره المستودعات (WMS) حجز دفعات محدده لأوامر توريد العميل.</span><span class="sxs-lookup"><span data-stu-id="23ef4-104">When an inventory reservation hierarchy of the "Batch-below\[location\]" type is associated with products, businesses that sell batch-tracked products and run their logistics as operations that are enabled for the Microsoft Dynamics 365 Warehouse Management System (WMS) can't reserve specific batches of those products for customer sales orders.</span></span> <span data-ttu-id="23ef4-105">يصف هذا الموضوع نهج حجز المخزون الذي يتيح لهذه الشركات حجز مجموعات محدده ، حتى عندما تكون المنتجات\[مقترنة بالتدرج الهرمي للحجز الخاص بالمجموعة\].</span><span class="sxs-lookup"><span data-stu-id="23ef4-105">This topic describes the inventory reservation policy that lets these businesses reserve specific batches, even when the products are associated with a "Batch-below\[location\]" reservation hierarchy.</span></span>

## <a name="inventory-reservation-hierarchy"></a><span data-ttu-id="23ef4-106">التدرجات الهرمية لحجز المخزون</span><span class="sxs-lookup"><span data-stu-id="23ef4-106">Inventory reservation hierarchy</span></span>

<span data-ttu-id="23ef4-107">يلخص هذا المقطع التدرج الهرمي لحجز المخزون الموجود.</span><span class="sxs-lookup"><span data-stu-id="23ef4-107">This section summarizes the existing inventory reservation hierarchy.</span></span> <span data-ttu-id="23ef4-108">فهو يركز علي الطريقة التي يتم بها معالجه الأصناف التي يتم تتبعها من قبل التجميع والأصناف التي تتبع التسلسل.</span><span class="sxs-lookup"><span data-stu-id="23ef4-108">It focuses on the way that batch-tracked and serial-tracked items are handled.</span></span>

<span data-ttu-id="23ef4-109">يفرض التدرج الهرمي لحجز المخزون علي المدى القلق لابعاد التخزين ، والتي تكون فيها الابعاد إلزاميه الموقع ، والمستودع ، وحاله المخزون ، حيث يكون منطق المستودع مسؤولا عن تعيين موقع إلى الكميات المطلوبة وحجز الموقع.</span><span class="sxs-lookup"><span data-stu-id="23ef4-109">The inventory reservation hierarchy dictates that, as far as storage dimensions are concerned, the demand order carries the mandatory dimensions of site, warehouse, and inventory status, whereas the warehouse logic is responsible for assigning a location to the requested quantities and reserving the location.</span></span> <span data-ttu-id="23ef4-110">بمعني آخر، في التفاعلات بين أمر الطلب وعمليات المستودع، من المتوقع ان يشير أمر الطلب إلى المكان الذي يجب ان يتم فيه شحن الأمر من (أي الموقع والمستودع).</span><span class="sxs-lookup"><span data-stu-id="23ef4-110">In other words, in the interactions between the demand order and the warehouse operations, the demand order is expected to indicate where the order must be shipped from (that is, what site and warehouse).</span></span> <span data-ttu-id="23ef4-111">وبعد ذلك يعتمد المستودع علي المنطق الخاص به للعثور علي الكمية المطلوبة في المستودع المحلي.</span><span class="sxs-lookup"><span data-stu-id="23ef4-111">The warehouse then relies on its logic to find the required quantity in the warehouse premises.</span></span>

<span data-ttu-id="23ef4-112">ومع ذلك ، لكي تعكس نموذج التشغيل الخاص بالاعمال ، يتم عرض ابعاد التعقب (المجموعة والأرقام المسلسلة) لمزيد من المرونة.</span><span class="sxs-lookup"><span data-stu-id="23ef4-112">However, to reflect the operational model of the business, tracking dimensions (batch and serial numbers) are subject to more flexibility.</span></span> <span data-ttu-id="23ef4-113">يمكن للتسلسل الهرمي لحجز المخزون استيعاب السيناريوهات التي تنطبق فيها الشروط التالية:</span><span class="sxs-lookup"><span data-stu-id="23ef4-113">An inventory reservation hierarchy can accommodate scenarios where the following conditions apply:</span></span>

- <span data-ttu-id="23ef4-114">يعتمد العمل علي عمليات المستودع الخاصة به لأداره انتقاء الكميات التي تحتوي علي المجموعة أو الأرقام المسلسلة بعد العثور علي الكميات في مساحة التخزين التي يتم تخزينها.</span><span class="sxs-lookup"><span data-stu-id="23ef4-114">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers after the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="23ef4-115">عاده ما يشار إلى هذا النموذج *\[بالموقع\]* الدفعي.</span><span class="sxs-lookup"><span data-stu-id="23ef4-115">This model is often referred to as *Batch-below\[location\]*.</span></span> <span data-ttu-id="23ef4-116">ويستخدم عاده عندما لا يكون تعريف مجموعه المنتجات أو الرقم المسلسل مهما للعملاء الذين يقومون بتقديم الطلب مع الشركة الموردة.</span><span class="sxs-lookup"><span data-stu-id="23ef4-116">It's typically used when a product's batch or serial number identification isn't important to the customers who place the demand with the selling company.</span></span>
- <span data-ttu-id="23ef4-117">إذا كانت المجموعة أو الأرقام المسلسلة جزءا من مواصفات أمر العميل ، وتم تسجيلها في أمر الطلب ، يتم تقييد عمليات المستودع التي تقوم بالبحث عن الكميات في المستودع بواسطة الأرقام المطلوبة المحددة ولا يسمح بتغييرها.</span><span class="sxs-lookup"><span data-stu-id="23ef4-117">If batch or serial numbers are part of a customer's order specification, and they are recorded on the demand order, the warehouse operations that find the quantities in the warehouse are constrained by the specific requested numbers and aren't allowed to change them.</span></span> <span data-ttu-id="23ef4-118">يشار إلى هذا النموذج *\[بالموقع\]* الدفعي.</span><span class="sxs-lookup"><span data-stu-id="23ef4-118">This model is referred to as *Batch-above\[location\]*.</span></span>

<span data-ttu-id="23ef4-119">في هذه السيناريوهات ، يكون التحدي هو انه يمكن تعيين تسلسل هرمي واحد فقط لحجز المخزون لكل منتج تم إصداره.</span><span class="sxs-lookup"><span data-stu-id="23ef4-119">In these scenarios, the challenge is that only one inventory reservation hierarchy can be assigned to each released product.</span></span> <span data-ttu-id="23ef4-120">التالي ، بالنسبة إلى WMS لمعالجة الأصناف المتتبعة، بعد أن يحدد تعيين التدرج الهرمي متى يتم حجز المجموعة أو الرقم المسلسل (أما عند أخذ أمر الطلب أو أثناء عمل الانتقاء الخاص بالمستودع)، لا يمكن تغيير هذا التوقيت على أساس المؤقت.</span><span class="sxs-lookup"><span data-stu-id="23ef4-120">Therefore, for the WMS to handle tracked items, after the hierarchy assignment determines when the batch or serial number should be reserved (either when the demand order is taken or during the warehouse picking work), this timing can't be changed on an ad-hoc basis.</span></span>

## <a name="flexible-reservation-for-batch-tracked-items"></a><span data-ttu-id="23ef4-121">حجز مرن للأصناف التي يتم تعقبها للدفعة</span><span class="sxs-lookup"><span data-stu-id="23ef4-121">Flexible reservation for batch-tracked items</span></span>

### <a name="business-scenario"></a><span data-ttu-id="23ef4-122">سيناريو الأعمال</span><span class="sxs-lookup"><span data-stu-id="23ef4-122">Business scenario</span></span>

<span data-ttu-id="23ef4-123">في هذا السيناريو، تستخدم إحدى الشركات استراتيجية مخزون حيث يتم تعقب البضائع المنتهية حسب أرقام المجموعات.</span><span class="sxs-lookup"><span data-stu-id="23ef4-123">In this scenario, a company uses an inventory strategy where finished goods are tracked by batch numbers.</span></span> <span data-ttu-id="23ef4-124">تستخدم هذه الشركة أيضا حمل العمل WMS.</span><span class="sxs-lookup"><span data-stu-id="23ef4-124">This company also uses the WMS workload.</span></span> <span data-ttu-id="23ef4-125">نظرا لأن حمل العمل هذا يستخدم منطق مجهز بشكل جيد لتخطيط عمليات الشحن والشحن وتشغيلها للأصناف التي تم تمكين المجموعة بها\[،\]يتم إقران معظم الأصناف المنتهية بالتسلسل الهرمي الخاص بحجز المخزون الخاص بالمجموعة.</span><span class="sxs-lookup"><span data-stu-id="23ef4-125">Because this workload has well-equipped logic for planning and running warehouse picking and shipping operations for batch-enabled items, most of the finished items are associated with a "Batch-below\[location\]" inventory reservation hierarchy.</span></span> <span data-ttu-id="23ef4-126">تعد ميزة هذا النوع من الإعداد التشغيلي بأن القرارات (التي تعتبر قرارات حجز فاعلية) حول المجموعات التي سيتم انتقاؤها ومكان وضعها في المستودع يتم تأجيلها حتى تبدأ عمليات انتقاء المستودع.</span><span class="sxs-lookup"><span data-stu-id="23ef4-126">The advantage of this type of operational setup is that decisions (which are effectively reservation decisions) about which batches to pick and where to put them in the warehouse are postponed until the warehouse picking operations start.</span></span> <span data-ttu-id="23ef4-127">ولا يتم اجراؤها عند وضع أمر العميل.</span><span class="sxs-lookup"><span data-stu-id="23ef4-127">They aren't made when the customer's order is placed.</span></span>

<span data-ttu-id="23ef4-128">علي الرغم من أن التسلسل الهرمي للحجز "الدفعة تحت\[الشركة\]" يعمل بشكل جيد، يتطلب العديد من العملاء الذين تم تأسيسهم للشركة وجود نفس المجموعة التي تم شراؤها مسبقا عند قيامهم بإعادة ترتيب المنتجات.</span><span class="sxs-lookup"><span data-stu-id="23ef4-128">Although the "Batch-below\[location\]" reservation hierarchy serves the company's business goals well, many of the company's established customers require the same batch that they previously purchased when they reorder products.</span></span> <span data-ttu-id="23ef4-129">التالي، فإن الشركة تبحث عن مرونة في الطريقة التي تتم بها معالجة قواعد الحجز، وذلك وفقا لطلب العملاء لنفس الصنف، تحدث السلوكيات التالية:</span><span class="sxs-lookup"><span data-stu-id="23ef4-129">Therefore, the company is looking for flexibility in the way that the batch reservation rules are handled, so that, depending on the customers' demand for the same item, the following behaviors occur:</span></span>

- <span data-ttu-id="23ef4-130">يمكن تسجيل رقم المجموعة وحجزها عند أخذ الطلب بواسطة معالج المبيعات، ولا يمكن تغييره أثناء عمليات المستودع و/أو القيام بذلك من قبل طلبات أخرى.</span><span class="sxs-lookup"><span data-stu-id="23ef4-130">A batch number can be recorded and reserved when the order is taken by the sales processor, and it can't be changed during warehouse operations and/or taken by other demands.</span></span> <span data-ttu-id="23ef4-131">ويضمن هذا السلوك شحن رقم المجموعة التي تم طلبها إلى العميل.</span><span class="sxs-lookup"><span data-stu-id="23ef4-131">This behavior helps guarantee that the batch number that was ordered is shipped to the customer.</span></span>
- <span data-ttu-id="23ef4-132">إذا كان رقم المجموعة غير هام للعميل، يمكن أن تحدد عمليات المستودع رقم مجموعة أثناء العمل التصنيعي، بعد إجراء تسجيل أمر التوريد والحجز.</span><span class="sxs-lookup"><span data-stu-id="23ef4-132">If the batch number isn't important to the customer, the warehouse operations can determine a batch number during picking work, after sales order registration and reservation have been done.</span></span>

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a><span data-ttu-id="23ef4-133">السماح بحجز مجموعة محددة في أمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="23ef4-133">Allowing reservation of a specific batch on the sales order</span></span>

<span data-ttu-id="23ef4-134">لاستيعاب المرونة المطلوبة في سلوك حجز الدفعات للأصناف المقترنة بالتسلسل\[الهرمي لحجز المخزون\]"الدفعة" ، **يجب أن يقوم مديرو** المخزون بتحديد **خانة الاختيار السماح بالحجز حسب الطلب لمستوي رقم** المجموعة في **صفحة التدرجات الهرمية لحجز المخزون**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-134">To accommodate the desired flexibility in the batch reservation behavior for items that are associated with a "Batch-below\[location\]" inventory reservation hierarchy, inventory managers must select the **Allow reservation on demand order** check box for the **Batch number** level on the **Inventory reservation hierarchies** page.</span></span>

![صيانة جدول التدرج الهرمي لحجز المخزون](media/Flexible-inventory-reservation-hierarchy.png)

<span data-ttu-id="23ef4-136">عند تحديد **مستوى رقم** المجموعة في التدرج الهرمي، يتم تحديد كافة الأبعاد الموجودة **أعلى** هذا المستوى والمستوى المحدد تلقائيا.</span><span class="sxs-lookup"><span data-stu-id="23ef4-136">When the **Batch number** level in the hierarchy is selected, all dimensions above that level and up through the **Location** level will be automatically selected.</span></span> <span data-ttu-id="23ef4-137">(بشكل افتراضي، يتم تحديد **كافة الأبعاد فوق مستوى الموقع** بشكل مسبق.) ويعكس هذا السلوك المنطق الذي يتم فيه أيضا حجز كافة الأبعاد الموجودة في النطاق بين رقم المجموعة والموقع تلقائيا بعد حجز رقم مجموعة محدد في بند الأمر.</span><span class="sxs-lookup"><span data-stu-id="23ef4-137">(By default, all dimensions above the **Location** level are preselected.) This behavior reflects the logic where all dimensions in the range between the batch number and location are also automatically reserved after you reserve a specific batch number on the order line.</span></span>

> [!NOTE]
> <span data-ttu-id="23ef4-138">يتم **تطبيق خانة الاختيار السماح بالحجز حسب طلب** الطلب فقط على مستويات التدرج الهرمي للحجز الموجودة أسفل بعد موقع المستودع.</span><span class="sxs-lookup"><span data-stu-id="23ef4-138">The **Allow reservation on demand order** check box applies only to reservation hierarchy levels that are below the warehouse location dimension.</span></span>
>
> <span data-ttu-id="23ef4-139">**رقم** المجموعة هو المستوى الوحيد في التدرج الهرمي المفتوح لنهج الحجز المرن.</span><span class="sxs-lookup"><span data-stu-id="23ef4-139">**Batch number** is the only level in the hierarchy that is open for the flexible reservation policy.</span></span> <span data-ttu-id="23ef4-140">بمعنى آخر ، لا يمكنك تحديد خانه الاختيار **السماح بالحجز حسب الطلب** **للموقع** أو **لوح الترخيص** أو مستوى **الرقم المسلسل**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-140">In other words, you can't select the **Allow reservation on demand order** check box for the **Location**, **License plate**, or **Serial number** level.</span></span>
>
> <span data-ttu-id="23ef4-141">إذا تضمن التدرج الهرمي للحجز بعد الرقم المسلسل (والذي **يجب** ان يكون أقل من مستوى رقم المجموعة)، وإذا قمت بتشغيل الحجز الخاص بالمجموعة لرقم المجموعة، سيتابع النظام معالجة حجز الرقم المسلسل وعمليات الانتقاء\[، وذلك استنادا إلى القواعد التي تنطبق علي نهج الحجز\]</span><span class="sxs-lookup"><span data-stu-id="23ef4-141">If your reservation hierarchy includes the serial number dimension (which must always be below the **Batch number** level), and if you've turned on batch-specific reservation for the batch number, the system will continue to handle serial number reservation and picking operations, based on the rules that apply to the "Serial-below\[location\]" reservation policy.</span></span>

<span data-ttu-id="23ef4-142">عند أي نقطة، يمكنك السماح بالحجز الخاص بالدفعة للتسلسل\[الهرمي للحجز الموجود ضمن المجموعة\]"في عملية التوزيع الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="23ef4-142">At any point, you can allow batch-specific reservation for an existing "Batch-below\[location\]" reservation hierarchy in your deployment.</span></span> <span data-ttu-id="23ef4-143">لن يؤثر هذا التغيير على أية عمليات حجز وعمل مستودع مفتوح تم إنشاؤه قبل حدوث التغيير.</span><span class="sxs-lookup"><span data-stu-id="23ef4-143">This change won't affect any reservations and open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="23ef4-144">ومع ذلك **، لا يمكن إلغاء تحديد** خانة الاختيار السماح بالحجز حسب أمر **الطلب**إذا **كانت**حركات **المخزون الخاصة بنوع المشكلة الفعلية المحجوزة أو المحجوزة أو المطلوبة** موجودة لصنف واحد أو أكثر من الأصناف المرتبطة بتسلسل الحجز هذا.</span><span class="sxs-lookup"><span data-stu-id="23ef4-144">However, the **Allow reservation on demand order** check box can't be cleared if inventory transactions of the **Reserved ordered**, **Reserved physical**, or **Ordered** issue type exist for one or more items that are associated with that reservation hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="23ef4-145">إذا لم يسمح التدرج الهرمي للحجز الموجود بالصنف بمواصفات التشغيلة في الأمر، فيمكنك إعادة تعيينه إلى تدرج الحجز الذي يسمح بمواصفات المجموعة، بشرط ان تكون بنية مستوى التدرج الهرمي هي نفسها في كلا التدرجات الهرمية.</span><span class="sxs-lookup"><span data-stu-id="23ef4-145">If an item's existing reservation hierarchy doesn't allow batch specification on the order, you can reassign it to a reservation hierarchy that does allow batch specification, provided that the hierarchy level structure is the same in both hierarchies.</span></span> <span data-ttu-id="23ef4-146">استخدم وظيفة **تغيير التدرج الهرمي** للحجز للأصناف لإجراء إعادة التعيين.</span><span class="sxs-lookup"><span data-stu-id="23ef4-146">Use the **Change reservation hierarchy for items** function to do the reassignment.</span></span> <span data-ttu-id="23ef4-147">قد يكون هذا التغيير متعلقا عندما ترغب في منع حجز المجموعات المرنة لمجموعة فرعية من الأصناف التي تتبع المجموعة ولكن مع السماح لها بالحفاظ علي بقية قائمة مشاريع المنتج.</span><span class="sxs-lookup"><span data-stu-id="23ef4-147">This change might be relevant when you want to prevent flexible batch reservation for a subset of batch-tracked items but allow it for the rest of the product portfolio.</span></span>

<span data-ttu-id="23ef4-148">بغض النظر عما إذا كنت قد قمت بتحديد **خانة الاختيار السماح بالحجز حسب أمر** الطلب ، فاذا كنت لا ترغب في حجز رقم مجموعة معين للصنف في بند أمر، سيظل\[بالإمكان تطبيق منطق عمليات المستودع الافتراضي الذي يعد صالحا للتسلسل الهرمي للحجز الخاص بالمجموعة\].</span><span class="sxs-lookup"><span data-stu-id="23ef4-148">Regardless of whether you've selected the **Allow reservation on demand order** check box, if you don't want to reserve a specific batch number for the item on an order line, default warehouse operations logic that is valid for a "Batch-below\[location\]" reservation hierarchy will still apply.</span></span>

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a><span data-ttu-id="23ef4-149">حجز رقم مجموعة محدد لأمر عميل</span><span class="sxs-lookup"><span data-stu-id="23ef4-149">Reserve a specific batch number for a customer order</span></span>

<span data-ttu-id="23ef4-150">بعد اعداد الصنف "الدفعات الموجودة\[في\]أسفل الصنف الذي تم تتبعه" للسماح بحجز أرقام مجموعات معينة في أوامر التوريد، يمكن أن تتخذ معالجات أوامر التوريد طلبات العميل لنفس الصنف بأحدي الطرق التالية، وذلك وفقا لطلب العميل:</span><span class="sxs-lookup"><span data-stu-id="23ef4-150">After a batch-tracked item's "Batch-below\[location\]" inventory reservation hierarchy is set up to allow reservation of specific batch numbers on sales orders, sales order processors can take customer orders for the same item in one of the following ways, depending on the customer's request:</span></span>

- <span data-ttu-id="23ef4-151">**ادخل تفاصيل الأمر بدون تحديد رقم** المجموعة - يجب استخدام هذه الطريقة عندما لا تكون مواصفات المجموعة الخاصة بالمنتج مهمة للعميل.</span><span class="sxs-lookup"><span data-stu-id="23ef4-151">**Enter order details without specifying a batch number** – This approach should be used when the product's batch specification isn't important to the customer.</span></span> <span data-ttu-id="23ef4-152">كافة العمليات الموجودة المقترنة بمعالجة أمر من هذا النوع يظل النظام بدون تغيير.</span><span class="sxs-lookup"><span data-stu-id="23ef4-152">All existing processes that are associated with handling an order of this type in the system remain unchanged.</span></span> <span data-ttu-id="23ef4-153">لا توجد اعتبارات إضافية مطلوبة في جزء المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="23ef4-153">No additional considerations are required on the part of users.</span></span>
- <span data-ttu-id="23ef4-154">**ادخل تفاصيل الأمر وقم بحجز رقم مجموعة معين** - يجب استخدام هذا الأسلوب عندما يطلب العميل مجموعة معينة.</span><span class="sxs-lookup"><span data-stu-id="23ef4-154">**Enter order details and reserve a specific batch number** – This approach should be used when the customer requests a specific batch.</span></span> <span data-ttu-id="23ef4-155">وعادة ما يقوم العملاء بطلب مجموعة محددة عند إعاده طلب المنتج الذي تم شراؤه سابقا.</span><span class="sxs-lookup"><span data-stu-id="23ef4-155">Typically, customers will request a specific batch when they are reordering a product that they previously purchased.</span></span> <span data-ttu-id="23ef4-156">ويشار إلى هذا النوع من الحجز الخاص بالدفعة *بالحجز المرتبط بالأمر*.</span><span class="sxs-lookup"><span data-stu-id="23ef4-156">This type of batch-specific reservation is referred to as *order-committed reservation*.</span></span>

<span data-ttu-id="23ef4-157">وتكون المجموعة التالية من القواعد صالحة عند معالجة الكميات، ويتم تخصيص رقم مجموعة لأمر محدد:</span><span class="sxs-lookup"><span data-stu-id="23ef4-157">The following set of rules is valid when quantities are processed, and a batch number is committed to a specific order:</span></span>

- <span data-ttu-id="23ef4-158">للسماح بحجز رقم مجموعة محدد لصنف ضمن نهج الحجز "المجموعة الموجودة أسفل\[المجموعة\]" ، يجب أن يقوم النظام بحجز كافة الأبعاد خلال الموقع.</span><span class="sxs-lookup"><span data-stu-id="23ef4-158">To allow reservation of a specific batch number for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="23ef4-159">يتضمن هذا النطاق عادة بُعد لوح الترخيص.</span><span class="sxs-lookup"><span data-stu-id="23ef4-159">This range typically includes the license plate dimension.</span></span>
- <span data-ttu-id="23ef4-160">لا يتم استخدام توجيهات المواقع عند إنشاء انتقاء العمل لبند المبيعات الذي يستخدم حجز المجموعات المرتبطة بالأمر.</span><span class="sxs-lookup"><span data-stu-id="23ef4-160">Location directives aren't used when picking work is created for a sales line that uses order-committed batch reservation.</span></span>
- <span data-ttu-id="23ef4-161">وأثناء معالجة المستودع للعمل بالنسبة للدفعات المرتبطة بالأمر، لا يسمح للمستخدم أو النظام بتغيير رقم المجموعة.</span><span class="sxs-lookup"><span data-stu-id="23ef4-161">During warehouse processing of work for order-committed batches, neither the user nor the system is allowed to change the batch number.</span></span> <span data-ttu-id="23ef4-162">(تتضمن هذه المعالجة معالجة الاستثناء.)</span><span class="sxs-lookup"><span data-stu-id="23ef4-162">(This processing includes exception handling.)</span></span>

<span data-ttu-id="23ef4-163">يوضح المثال التالي تدفق نهاية إلى نهاية.</span><span class="sxs-lookup"><span data-stu-id="23ef4-163">The following example shows the end-to-end flow.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="23ef4-164">سيناريو كمثال</span><span class="sxs-lookup"><span data-stu-id="23ef4-164">Example scenario</span></span>

<span data-ttu-id="23ef4-165">بالنسبة إلى هذا العرض التوضيحي، يجب تثبيت بيانات العرض التوضيحي، ويجب استخدام شركة بيانات العرض التوضيحي **USMF‎**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-165">For this example, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><span data-ttu-id="23ef4-166">إعداد تدرج هرمي لحجز مخزون للسماح بحجز خاص بمجموعة</span><span class="sxs-lookup"><span data-stu-id="23ef4-166">Set up an inventory reservation hierarchy to allow batch-specific reservation</span></span>

1. <span data-ttu-id="23ef4-167">الانتقال إلى **إدارة المخزون** \> **إعداد** \> **المخزون \> ‏‫التدرج الهرمي للحجز‬**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-167">Go to **Warehouse management** \> **Setup** \> **Inventory \> Reservation hierarchy**.</span></span>
2. <span data-ttu-id="23ef4-168">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-168">Select **New**.</span></span>
3. <span data-ttu-id="23ef4-169">في حقل **الاسم** أدخل اسمًا (على سبيل المثال، **BatchFlex**).</span><span class="sxs-lookup"><span data-stu-id="23ef4-169">In the **Name** field, enter a name (for example, **BatchFlex**).</span></span>
4. <span data-ttu-id="23ef4-170">في الحقل **الوصف**، ادخل وصفا (على سبيل المثال، **المجموعة الموجودة أسفل المرونة**).</span><span class="sxs-lookup"><span data-stu-id="23ef4-170">In the **Description** field, enter a description (for example, **Batch below flexible**).</span></span>
5. <span data-ttu-id="23ef4-171">في الحقل **المحدد**، حدد **الرقم المسلسل** و**المالك**، ثم حدد زر السهم الأيسر لنقلهم إلى الحقل **المتوفر**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-171">In the **Selected** field, select **Serial number** and **Owner**, and then select the left arrow button to move them to the **Available** field.</span></span>
6. <span data-ttu-id="23ef4-172">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-172">Select **OK**.</span></span>
7. <span data-ttu-id="23ef4-173">في الصف الخاص بمستوى بعد **رقم المجموعة**، حدد خانة الاختيار **السماح بالحجز عند الطلب**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-173">In the row for the **Batch number** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="23ef4-174">يتم تحديد **لوحة الترخيص**ومستويات **الموقع** تلقائيا، ولا يمكنك إلغاء تحديد خانات الاختيار الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="23ef4-174">The **License plate** and **Location** levels are automatically selected, and you can't clear the check boxes for them.</span></span>
8. <span data-ttu-id="23ef4-175">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-175">Select **Save**.</span></span>

### <a name="create-a-new-released-product"></a><span data-ttu-id="23ef4-176">إنشاء منتج جديد صادر</span><span class="sxs-lookup"><span data-stu-id="23ef4-176">Create a new released product</span></span>

1. <span data-ttu-id="23ef4-177">قم بتعيين معلمات البيانات الرئيسية الثلاثة الخاصة بالمنتج باستخدام هذه القيم:</span><span class="sxs-lookup"><span data-stu-id="23ef4-177">Set the product's three master data parameters by using these values:</span></span>

    - <span data-ttu-id="23ef4-178">وفي الحقل **مجموعة أبعاد التخزين**، حدد **مستودع**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-178">In the **Storage dimension group** field, select **Ware**.</span></span>
    - <span data-ttu-id="23ef4-179">في الحقل **تتبع مجموعة الأبعاد**، حدد **الدفعة المادية**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-179">In the **Tracking dimension group** field, select **Batch-Phy**.</span></span>
    - <span data-ttu-id="23ef4-180">في حقل **تدرج الحجز**، حدد **BatchFlex**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-180">In the **Reservation hierarchy** field, select **BatchFlex**.</span></span>

2. <span data-ttu-id="23ef4-181">قم بإنشاء رقمين للمجموعة مثل **B11** و**B22**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-181">Create two batch numbers, such as **B11** and **B22**.</span></span>
3. <span data-ttu-id="23ef4-182">أضافه كميات الأصناف إلى المخزون الفعلي من خلال استخدام القيم التالية.</span><span class="sxs-lookup"><span data-stu-id="23ef4-182">Add item quantities to on-hand stock by using the following values.</span></span>

    | <span data-ttu-id="23ef4-183">المستودع</span><span class="sxs-lookup"><span data-stu-id="23ef4-183">Warehouse</span></span> | <span data-ttu-id="23ef4-184">رقم الدُفعة</span><span class="sxs-lookup"><span data-stu-id="23ef4-184">Batch number</span></span> | <span data-ttu-id="23ef4-185">الموقع</span><span class="sxs-lookup"><span data-stu-id="23ef4-185">Location</span></span> | <span data-ttu-id="23ef4-186">لوحة الترخيص</span><span class="sxs-lookup"><span data-stu-id="23ef4-186">License plate</span></span> | <span data-ttu-id="23ef4-187">الكمية</span><span class="sxs-lookup"><span data-stu-id="23ef4-187">Quantity</span></span> |
    |-----------|--------------|----------|---------------|----------|
    | <span data-ttu-id="23ef4-188">24</span><span class="sxs-lookup"><span data-stu-id="23ef4-188">24</span></span>        | <span data-ttu-id="23ef4-189">B11</span><span class="sxs-lookup"><span data-stu-id="23ef4-189">B11</span></span>          | <span data-ttu-id="23ef4-190">BULK-001</span><span class="sxs-lookup"><span data-stu-id="23ef4-190">BULK-001</span></span> | <span data-ttu-id="23ef4-191">لا‬‬ شيء</span><span class="sxs-lookup"><span data-stu-id="23ef4-191">None</span></span>          | <span data-ttu-id="23ef4-192">10</span><span class="sxs-lookup"><span data-stu-id="23ef4-192">10</span></span>       |
    | <span data-ttu-id="23ef4-193">24</span><span class="sxs-lookup"><span data-stu-id="23ef4-193">24</span></span>        | <span data-ttu-id="23ef4-194">B11</span><span class="sxs-lookup"><span data-stu-id="23ef4-194">B11</span></span>          | <span data-ttu-id="23ef4-195">FL-001</span><span class="sxs-lookup"><span data-stu-id="23ef4-195">FL-001</span></span>   | <span data-ttu-id="23ef4-196">LP11</span><span class="sxs-lookup"><span data-stu-id="23ef4-196">LP11</span></span>          | <span data-ttu-id="23ef4-197">10</span><span class="sxs-lookup"><span data-stu-id="23ef4-197">10</span></span>       |
    | <span data-ttu-id="23ef4-198">24</span><span class="sxs-lookup"><span data-stu-id="23ef4-198">24</span></span>        | <span data-ttu-id="23ef4-199">B22</span><span class="sxs-lookup"><span data-stu-id="23ef4-199">B22</span></span>          | <span data-ttu-id="23ef4-200">FL-002</span><span class="sxs-lookup"><span data-stu-id="23ef4-200">FL-002</span></span>   | <span data-ttu-id="23ef4-201">LP22</span><span class="sxs-lookup"><span data-stu-id="23ef4-201">LP22</span></span>          | <span data-ttu-id="23ef4-202">10</span><span class="sxs-lookup"><span data-stu-id="23ef4-202">10</span></span>       |

### <a name="enter-sales-order-details"></a><span data-ttu-id="23ef4-203">إدخال تفاصيل أمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="23ef4-203">Enter sales order details</span></span>

1. <span data-ttu-id="23ef4-204">انتقل إلى **المبيعات والتسويق** \> **أوامر المبيعات** \> **كافة أوامر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-204">Go to **Sales and marketing** \> **Sales orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="23ef4-205">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-205">Select **New**.</span></span>
3. <span data-ttu-id="23ef4-206">في البيانات الرئيسية لأمر التوريد ، في الحقل **حساب العميل**، أدخل **US-003**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-206">On the sales order header, in the **Customer account** field, enter **US-003**.</span></span>
4. <span data-ttu-id="23ef4-207">أضف سطرًا لمنتج مُنتهِ، وادخل **10** ككمية.</span><span class="sxs-lookup"><span data-stu-id="23ef4-207">Add a line for the new item, and enter **10** as the quantity.</span></span> <span data-ttu-id="23ef4-208">تأكد من تعيين الحقل **الكمية** على **24**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-208">Make sure that the **Warehouse** field is set to **24**.</span></span>
5. <span data-ttu-id="23ef4-209">في علامة التبويب السريعة **بنود أمر التوريد**، حدد **المخزون**، ثم في المجموعة **الصيانة**، حدد **حجز المجموعة**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-209">On the **Sales order lines** FastTab, select **Inventory**, and then, in the **Maintain** group, select **Batch reservation**.</span></span> <span data-ttu-id="23ef4-210">تقوم **صفحه حجز** المجموعات بعرض قائمه بالمجموعات المتوفرة للحجز الخاص ببند الأمر.</span><span class="sxs-lookup"><span data-stu-id="23ef4-210">The **Batch reservation** page shows a list of batches that are available for reservation for the order line.</span></span> <span data-ttu-id="23ef4-211">بالنسبة لهذا المثال، فإنه يعرض كمية بمقدار **20** لرقم المجموعة **B11** وكمية **10** لرقم المجموعة **B22** .</span><span class="sxs-lookup"><span data-stu-id="23ef4-211">For this example, it shows a quantity of **20** for batch number **B11** and a quantity of **10** for batch number **B22**.</span></span> <span data-ttu-id="23ef4-212">لاحظ أنه لا يمكن الوصول إلى صفحة **حجز الدفعة** من بند إذا كان الصنف الموجود في هذا السطر مقترنا بالتدرج الهرمي للحجز الموجود\[بالبند "الدفعة\]" ما لم يتم اعداده للسماح بالحجز الخاص بالدفعة.</span><span class="sxs-lookup"><span data-stu-id="23ef4-212">Note that the **Batch reservation** page cannot be accessed from a line if the item on that line is associated with "Batch-below\[location\]" reservation hierarchy unless it is set up to allow batch-specific reservation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="23ef4-213">لحجز مجموعة محددة لأمر توريد، يجب استخدام الصفحة **حجز المجموعة**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-213">To reserve a specific batch for a sales order, you must use the **Batch reservation** page.</span></span>
    >
    > <span data-ttu-id="23ef4-214">إذا قمت بإدخال رقم المجموعة مباشره في بند أمر التوريد ، سيعمل النظام كما لو قمت بإدخال قيمه مجموعه محدده لأحد الأصناف الذي يخضع لنهج الحجز "المجموعة ضمن\[الموقع\]".</span><span class="sxs-lookup"><span data-stu-id="23ef4-214">If you enter the batch number directly on the sales order line, the system will behave as though you entered a specific batch value for an item that is subject to the "Batch-below\[location\]" reservation policy.</span></span> <span data-ttu-id="23ef4-215">عند حفظ البند، ستتلقى رسالة تحذير.</span><span class="sxs-lookup"><span data-stu-id="23ef4-215">When you save the line, you will receive a warning message.</span></span> <span data-ttu-id="23ef4-216">إذا قمت بالتاكيد علي انه يجب تحديد رقم المجموعة مباشره علي سطر الأمر، فلن تتم معالجه البند بواسطة منطق إدارة المستودع العادي.</span><span class="sxs-lookup"><span data-stu-id="23ef4-216">If you confirm that the batch number should be specified directly on the order line, the line won't be handled by the regular warehouse management logic.</span></span>
    >
    > <span data-ttu-id="23ef4-217">إذا قمت بحجز الكمية من صفحة **الحجز**، فلن يتم حجز مجموعه محددة، سيتبع تنفيذ عمليات المستودع للبند القواعد التي تنطبق عليها نهج الحجز\["الدفعات الموجودة في أسفل\]".</span><span class="sxs-lookup"><span data-stu-id="23ef4-217">If you reserve the quantity from the **Reservation** page, no specific batch will be reserved, and the execution of warehouse operations for the line will follow the rules that are applicable under the "Batch-below\[location\]" reservation policy.</span></span>

    <span data-ttu-id="23ef4-218">بشكل عام ، تعمل هذه الصفحة ويتم التفاعل معها بنفس الطريقة التي تعمل بها ويتم التفاعل مع الأصناف التي تحتوي علي تسلسل هرمي مقترن لنوع "المجموعة الموجودة أعلى \[الموقع\]".</span><span class="sxs-lookup"><span data-stu-id="23ef4-218">In general, this page works and is interacted with in the same way that it works and is interacted with for items that have an associated reservation hierarchy of the "Batch-above\[location\]" type.</span></span> <span data-ttu-id="23ef4-219">ومع ذلك، يتم تطبيق الاستثناءات التالية:</span><span class="sxs-lookup"><span data-stu-id="23ef4-219">However, the following exceptions apply:</span></span>

    - <span data-ttu-id="23ef4-220">تعرض علامة التبويب السريعة **أرقام المجموعات التي تم تنفيذها لبند المصدر** أرقام المجموعات التي تم حجزها لبند الأمر.</span><span class="sxs-lookup"><span data-stu-id="23ef4-220">The **Batch numbers committed to source line** FastTab shows the batch numbers that are reserved for the order line.</span></span> <span data-ttu-id="23ef4-221">ستظهر قيم المجموعات في الشبكة خلال دورة الاستيفاء لسطر الأمر، بما في ذلك مراحل معالجة المستودع.</span><span class="sxs-lookup"><span data-stu-id="23ef4-221">The batch values in the grid will be shown throughout the fulfilment cycle of the order line, including the warehouse processing stages.</span></span> <span data-ttu-id="23ef4-222">وعلي النقيض، في علامة التبويب السريعة **النظرة العامة**، يتم عرض حجز بند الأمر العادي (أي ، الحجز الذي يتم إنجازه للابعاد الموجودة اعلي مستوي **الموقع**) في الشبكة حتى النقطة التي يتم فيها إنشاء عمل المستودع.</span><span class="sxs-lookup"><span data-stu-id="23ef4-222">By contrast, on the **Overview** FastTab, regular order line reservation (that is, reservation that is done for the dimensions above the **Location** level) is shown in the grid up to the point when warehouse work is created.</span></span> <span data-ttu-id="23ef4-223">ثم يقوم كيان العمل بعد ذلك بالحفاظ علي حجز البند ، ولا يظهر حجز البند بعد ذلك في الصفحة.</span><span class="sxs-lookup"><span data-stu-id="23ef4-223">The work entity then takes over the line reservation, and the line reservation no longer appears on the page.</span></span> <span data-ttu-id="23ef4-224">تساعد علامة التبويب السريعة **أرقام المجموعات التي تم تنفيذها علي بند المصدر** على التأكد من أن معالج أمر التوريد يمكنه عرض أرقام المجموعات التي تم تنفيذها لأمر العميل في أي مرحلة أثناء الفوترة.</span><span class="sxs-lookup"><span data-stu-id="23ef4-224">The **Batch numbers committed to source line** FastTab helps guarantee that the sales order processor can view the batch numbers that were committed to the customer's order at any point during its lifecycle, up through invoicing.</span></span>
    - <span data-ttu-id="23ef4-225">بالاضافه إلى القيام بحجز مجموعه محدده، يمكن للمستخدم تحديد الموقع الخاص بالمجموعة ولوحه الترخيص يدويا بدلا من السماح للنظام بتحديدها تلقائيا.</span><span class="sxs-lookup"><span data-stu-id="23ef4-225">In addition to reserving a specific batch, a user can manually select the batch's specific location and license plate instead of letting the system automatically select them.</span></span> <span data-ttu-id="23ef4-226">ترتبط هذه الامكانيه بتصميم آلية حجز المجموعة الملتزم بها الأمر.</span><span class="sxs-lookup"><span data-stu-id="23ef4-226">This capability is related to the design of the order-committed batch reservation mechanism.</span></span> <span data-ttu-id="23ef4-227">للسماح بحجز رقم مجموعة محدد لصنف ضمن نهج الحجز "المجموعة الموجودة أسفل\[الموقع\]" ، يجب أن يقوم النظام بحجز كافة الأبعاد خلال الموقع.</span><span class="sxs-lookup"><span data-stu-id="23ef4-227">As was mentioned earlier, when a batch number is reserved for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="23ef4-228">التالي، سيحمل عمل المستودع نفس أبعاد التخزين التي تم حجزها بواسطة المستخدمين الذين قاموا بالعمل مع الأوامر، وقد لا يمثلون دائما موضع تخزين الأصناف الملائم ، أو حتى الممكن ، لعمليات الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="23ef4-228">Therefore, warehouse work will carry the same storage dimensions that were reserved by the users who worked with the orders, and it might not always represent the item storage placement that is convenient, or even possible, for picking operations.</span></span> <span data-ttu-id="23ef4-229">إذا كانت معالجه الأمر علي علم بقيود المستودع ، فقد يرغبون في تحديد المواقع المحددة ولوحات الترخيص يدويا عند حجزها لأحدي المجموعات.</span><span class="sxs-lookup"><span data-stu-id="23ef4-229">If order processors are aware of the warehouse constraints, they might want to manually select the specific locations and license plates when they reserve a batch.</span></span> <span data-ttu-id="23ef4-230">في هذه الحالة ، يجب ان يستخدم المستخدم وظيفة **ابعاد العرض** في راس الصفحة ، ويجب ان يضيف لوحه الموقع والترخيص الشبكة في على علامة التبويب السريعة **النظرة العامة**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-230">In this case, the user must use the **Display dimensions** functionality on the page header, and must add the location and license plate in the grid on the **Overview** FastTab.</span></span>

6. <span data-ttu-id="23ef4-231">في الصفحة **حجز المجموعة**، حدد بندا لمجموعة **B11**، ثم حدد **حجز البند**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-231">On the **Batch reservation** page, select the line for batch **B11**, and then select **Reserve line**.</span></span> <span data-ttu-id="23ef4-232">لا يوجد منطق مخصص لتعيين المواقع ولوحات الترخيص اثناء الحجز التلقائي.</span><span class="sxs-lookup"><span data-stu-id="23ef4-232">There is no designated logic for assigning locations and license plates during automatic reservation.</span></span> <span data-ttu-id="23ef4-233">يمكنك إدخال الكمية يدويا في حقل **الحجز**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-233">You can manually enter the quantity in the **Reservation** field.</span></span> <span data-ttu-id="23ef4-234">لاحظ انه يتم في علامة التبويب السريعة **الأرقام الدفعيه التي تم تنفيذها لبند المصدر** عرض مجموعة **B11** بالحالة **منفذ.**</span><span class="sxs-lookup"><span data-stu-id="23ef4-234">Notice that, on the **Batch numbers committed to source line** FastTab, batch **B11** is shown as **Committed**.</span></span>

    ![تنفيذ رقم دفعه معين لبند أمر التوريد في صفحه حجز الدفعات](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > <span data-ttu-id="23ef4-236">يمكن القيام بحجز الكمية في بند أمر التوريد عبر مجموعات متعددة.</span><span class="sxs-lookup"><span data-stu-id="23ef4-236">Reservation of the quantity on a sales order line can be done across multiple batches.</span></span> <span data-ttu-id="23ef4-237">المثل ، يمكن القيام بحجز نفس الدفعة مقابل المواقع المتعددة ولوحات الترخيص (في حاله تمكين لوحات الترخيص للمواقع).</span><span class="sxs-lookup"><span data-stu-id="23ef4-237">Likewise, reservation of the same batch can be done against multiple locations and license plates (if license plates are enabled for the locations).</span></span>
    >
    > <span data-ttu-id="23ef4-238">يمكن أيضا ان يكون حجز مجموعه محدده للكمية في بند أمر التوريد جزئيا.</span><span class="sxs-lookup"><span data-stu-id="23ef4-238">Reservation of a specific batch for the quantity on a sales order line can also be partial.</span></span> <span data-ttu-id="23ef4-239">علي سبيل المثال ، يمكن حجز إجمالي الكمية 100 من الوحدات بحيث يتم التزام بمجموعه معينه إلى 20 وحده ، بينما يتم حجز 80 وحده في مستويات الموقع والمستودع لآيه مجموعه متاحه.</span><span class="sxs-lookup"><span data-stu-id="23ef4-239">For example, the total quantity of 100 units can be reserved so that a specific batch is committed to 20 units, whereas 80 units are reserved at the site and warehouse levels for any available batch.</span></span> <span data-ttu-id="23ef4-240">في هذه الحالة ، سيقوم WMS بمعالجه عمليات الانتقاء باستخدام بندين منفصلين من أسطر العمل.</span><span class="sxs-lookup"><span data-stu-id="23ef4-240">In this case, the WMS will handle picking operations by using two separate work lines.</span></span>

7. <span data-ttu-id="23ef4-241">انتقل إلى **إدارة معلومات المنتج** \> **المنتجات** \> **المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-241">Go to **Product information management** \> **Products** \> **Released products**.</span></span> <span data-ttu-id="23ef4-242">حدد الصنف، ثم حدد **إدارة المخزون**\>**عرض**\>**الحركات**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-242">Select your item, and then select **Manage inventory** \> **View** \> **Transactions**.</span></span>

    ![الحجز المرتبط بالأمر كنوع حركه مخزون](media/Inventory-transactions-for-order-committed-reservation.png)

8. <span data-ttu-id="23ef4-244">مراجعه حركات المخزون الخاصة بالصنف والمرتبطة بحجز بند أمر التوريد.</span><span class="sxs-lookup"><span data-stu-id="23ef4-244">Review the item's inventory transactions that are related to the sales order line reservation.</span></span>

    - <span data-ttu-id="23ef4-245">حركه يتم تعيين الحقل**المرجع** بها إلى **أمر المبيعات** ويتم تعيين حقل **الإصدار** على القيمة **الفعلية المحجوزة** تمثل حجز بند الأمر لابعاد المخزون فوق مستوى **الموقع**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-245">A transaction where the **Reference** field is set to **Sales order** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the inventory dimensions above the **Location** level.</span></span> <span data-ttu-id="23ef4-246">ووفقا للتسلسل الهرمي لحجز مخزون الصنف ، فان هذه الابعاد هي الموقع والمستودع وحاله المخزون.</span><span class="sxs-lookup"><span data-stu-id="23ef4-246">According to the item's inventory reservation hierarchy, those dimensions are site, warehouse, and inventory status.</span></span>
    - <span data-ttu-id="23ef4-247">حركه يتم تعيين الحقل **المرجع** بها إلى **الحجز بواسطة الأمر** ويتم تعيين حقل **الإصدار** على القيمة **الفعلية المحجوزة** تمثل حجز بند الأمر لدفعة معينة وجميع أبعاد المخزون فوقها.</span><span class="sxs-lookup"><span data-stu-id="23ef4-247">A transaction where the **Reference** field is set to **Order-committed reservation** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the specific batch and all inventory dimensions above it.</span></span> <span data-ttu-id="23ef4-248">ووفقا للتسلسل الهرمي لحجز مخزون الصنف، فان هذه الابعاد هي الموقع ورقم الدفعة.</span><span class="sxs-lookup"><span data-stu-id="23ef4-248">According to the item's inventory reservation hierarchy, those dimensions are batch number and location.</span></span> <span data-ttu-id="23ef4-249">في هذا المثال، يكون **Bulk-001.**</span><span class="sxs-lookup"><span data-stu-id="23ef4-249">In this example, the location is **Bulk-001**.</span></span>

9. <span data-ttu-id="23ef4-250">في رأس أمر المبيعات، حدد **المستودع** \> **الإجراءات‏‎** \> **إصدار إلى المستودع**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-250">On the sales order header, select **Warehouse** \> **Actions** \> **Release to warehouse**.</span></span> <span data-ttu-id="23ef4-251">يتم الآن إرسال بند الأمر، ويتم إنشاء تحميل وعمل.</span><span class="sxs-lookup"><span data-stu-id="23ef4-251">The order line is now waved, and a load and work are created.</span></span>

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="23ef4-252">مراجعه عمل المستودع الذي يحتوي على أرقام الدفعات المخصصة للأمر ومعالجتها</span><span class="sxs-lookup"><span data-stu-id="23ef4-252">Review and process warehouse work that has order-committed batch numbers</span></span>

1. <span data-ttu-id="23ef4-253">في علامة التبويب السريعة **بنود أمر المبيعات**، حدد **المستودع**\>**تفاصيل العمل**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-253">On the **Sales order lines** FastTab, select **Warehouse** \> **Work details**.</span></span>

    <span data-ttu-id="23ef4-254">يحتوي العمل الذي يقوم بمعالجه عمليه الانتقاء لكميات الدفعة التي يتم تنفيذها علي بند أمر التوريد علي الخصائص التالية:</span><span class="sxs-lookup"><span data-stu-id="23ef4-254">The work that handles the picking operation for batch quantities that are committed to the sales order line has the following characteristics:</span></span>

    - <span data-ttu-id="23ef4-255">لإنشاء العمل ، يستخدم النظام قوالب العمل وليس توجيهات المواقع.</span><span class="sxs-lookup"><span data-stu-id="23ef4-255">To create work, the system uses work templates but not location directives.</span></span> <span data-ttu-id="23ef4-256">سيتم تطبيق كافة الإعدادات القياسية التي تم تحديدها لقوالب العمل ، مثل العدد الأقصى لبنود الانتقاء أو وحده قياس معينه ، لتحديد الوقت الذي ينبغي فيه إنشاء عمل جديد.</span><span class="sxs-lookup"><span data-stu-id="23ef4-256">All the standard settings that are defined for work templates, such as a maximum number of pick lines or a specific unit of measure, will be applied to determine when new work should be created.</span></span> <span data-ttu-id="23ef4-257">ومع ذلك ، لا يتم التعامل مع القواعد المقترنة بتوجيهات المواقع لتعريف مواقع الانتقاء ، نظرا لان الحجز المرتبط بالأمر يحدد بالفعل كافة ابعاد المخزون.</span><span class="sxs-lookup"><span data-stu-id="23ef4-257">However, the rules that are associated with location directives for identifying pick locations aren't considered, because the order-committed reservation already specifies all the inventory dimensions.</span></span> <span data-ttu-id="23ef4-258">وتتضمن ابعاد المخزون هذه الابعاد علي مستوي تخزين المستودع.</span><span class="sxs-lookup"><span data-stu-id="23ef4-258">Those inventory dimensions include the dimensions at the warehouse storage level.</span></span> <span data-ttu-id="23ef4-259">التالي ، يرث العمل تلك الابعاد دون الحاجة إلى استشاره توجيهات المواقع.</span><span class="sxs-lookup"><span data-stu-id="23ef4-259">Therefore, the work inherits those dimensions without having to consult location directives.</span></span>
    - <span data-ttu-id="23ef4-260">لا يتم إظهار رقم المجموعة في بند الانتقاء (كما هو الحال بالنسبة لبند العمل الذي تم إنشاؤه للصنف الذي يشتمل على تسلسل الحجز "الدفعة أعلى \[الموقع\]".) بدلا من ذلك ، يتم عرض رقم المجموعة "من" وكافة ابعاد التخزين الأخرى في حركه مخزون العمل الخاصة ببند العمل المشار اليها من حركات المخزون المرتبطة.</span><span class="sxs-lookup"><span data-stu-id="23ef4-260">The batch number isn't shown on the pick line (as is the case for the work line that is created for an item that has an associated "Batch-above\[location\]" reservation hierarchy.) Instead, the "from" batch number and all other storage dimensions are shown on the work line's work inventory transaction that is referenced from the associated inventory transactions.</span></span>

        ![حركه مخزون المستودع للعمل الذي ينتج عن الحجز المرتبط بالطلبات](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - <span data-ttu-id="23ef4-262">بعد إنشاء العمل، تتم إزالة حركة المخزون الخاصة بالصنف التي تم تعيين حقل **المرجع**فيها إلى **الحجز المرتبط بالأمر**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-262">After work is created, the item's inventory transaction where the **Reference** field is set to **Order-committed reservation** is removed.</span></span> <span data-ttu-id="23ef4-263">حركة المخزون التي تم تعيين الحقل**المرجع** بها على **عمل** تحتفظ الآن بالحجز الفعلي علي كافة ابعاد المخزون الخاصة بالكمية.</span><span class="sxs-lookup"><span data-stu-id="23ef4-263">The inventory transaction where the **Reference** field is set to **Work** now holds the physical reservation on all the quantity's inventory dimensions.</span></span>

        <span data-ttu-id="23ef4-264">يمكن ان تتابع عمليات المستودع معالجه تنفيذ العمل بالطريقة المعتادة.</span><span class="sxs-lookup"><span data-stu-id="23ef4-264">Warehouse operations can proceed to handle execution of the work in the usual manner.</span></span> <span data-ttu-id="23ef4-265">ومع ذلك، ستقوم الإرشادات الموجودة علي الجهاز المحمول بإرشاد العامل لانتقاء رقم مجموعه معين.</span><span class="sxs-lookup"><span data-stu-id="23ef4-265">However, the instructions on the mobile device will instruct the worker to pick a specific batch number.</span></span> <span data-ttu-id="23ef4-266">في بيئات المستودعات حيث تكون المواقع عبارة عن لوحه ترخيص – يتم التحكم بها ، بعد وصول أحد العاملين إلى موقع يقوم بتخزين نفس المجموعة علي ألواح ترخيص متعددة ، فانه يمكنه الانتقاء من اي لوحه ترخيص غير محجوزه بالفعل (علي سبيل المثال ، بواسطة آخر الحجز أو الاعمال المرتبطة بالطلبات التي تنشا من حجز من هذا النوع.)</span><span class="sxs-lookup"><span data-stu-id="23ef4-266">In warehouse environments where locations are license plate–controlled, after a worker reaches a location that stores the same batch on multiple license plates, he or she can pick from any license plate that isn't already reserved (for example, by another order-committed reservation or work that originates from a reservation of that type.)</span></span>

        <span data-ttu-id="23ef4-267">وفي حاله تشغيله للانتقاء من الموقع المحدد في بند العمل ، يمكن لمشغلي المستودع استخدام أحد الإجراءات التالية لأعاده توجيه انتقاء المجموعة المحددة من موقع أكثر ملاءمة:</span><span class="sxs-lookup"><span data-stu-id="23ef4-267">If it turns out to be impractical to pick from the location that is specified on the work line, the warehouse operators can use one of the following actions to redirect picking of the specific batch from a more convenient location:</span></span>

        - <span data-ttu-id="23ef4-268">إجراء **تجاوز الموقع** القياسي علي جهاز محمول (شريطة تمكين الإعداد الخاص بالعامل الخاص بالمستودع **السماح بتجاوز موقع الالتقاط**)</span><span class="sxs-lookup"><span data-stu-id="23ef4-268">The standard **Override location** action on a mobile device (provided that the warehouse worker's **Allow pick location override** setting is enabled)</span></span>
        - <span data-ttu-id="23ef4-269">إجراء **تغيير الموقع** في الصفحة **تفاصيل قائمة العمل**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-269">The **Change location** action on the **Work list details** page.</span></span> 

2. <span data-ttu-id="23ef4-270">علي الجهاز المحمول ، قم بإنهاء الانتقاء ووضع العمل.</span><span class="sxs-lookup"><span data-stu-id="23ef4-270">On the mobile device, finish picking and putting the work.</span></span>

    <span data-ttu-id="23ef4-271">يتم الآن انتقاء الكمية **10** لرقم الدفعة **B11** لبند أمر المبيعات ووضعها في موقع **باب تحميل البضائع**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-271">The quantity of **10** for batch number **B11** is now picked for the sales order line and put in the **Baydoor** location.</span></span> <span data-ttu-id="23ef4-272">في هذه المرحلة، يكون جاهزا ليتم تحميله علي الشاحنة وإرساله إلى عنوان العميل.</span><span class="sxs-lookup"><span data-stu-id="23ef4-272">At this point, it's ready to be loaded onto the truck and dispatched to the customer's address.</span></span>

## <a name="exception-handling-of-warehouse-work-thas-has-order-committed-batch-numbers"></a><span data-ttu-id="23ef4-273">معالجة استثنائية لعمل المستودع الذي يحتوي علي أرقام الدفعات المخصصة للأمر</span><span class="sxs-lookup"><span data-stu-id="23ef4-273">Exception handling of warehouse work thas has order-committed batch numbers</span></span>

<span data-ttu-id="23ef4-274">يعمل المستودع الخاص بأرقام أمر الانتقاء-المخصصة إلى نفس معالجه استثناء المستودع القياسي والإجراءات الخاصة به كعمل عادي.</span><span class="sxs-lookup"><span data-stu-id="23ef4-274">Warehouse work for picking order-committed batch numbers is subject to the same standard warehouse exception handling and actions as regular work.</span></span> <span data-ttu-id="23ef4-275">بشكل عام ، يمكن إلغاء العمل المفتوح أو سطر العمل، حيث يمكن مقاطعته لان موقع المستخدم ممتلئ، ويمكن ان يتم انتقاؤه بشكل قصير، ويمكن تحديثه بسبب الحركة.</span><span class="sxs-lookup"><span data-stu-id="23ef4-275">In general, the open work or work line can be canceled, it can be interrupted because a user location is full, it can be short-picked, and it can be updated because of a movement.</span></span> <span data-ttu-id="23ef4-276">بالمثل ، يمكن تقليل الكمية المنتقاة للعمل التي تم إكمالها بالفعل، أو يمكن عكس العمل.</span><span class="sxs-lookup"><span data-stu-id="23ef4-276">Likewise, the picked quantity of work that has already been completed can be reduced, or the work can be reversed.</span></span>

<span data-ttu-id="23ef4-277">يتم تطبيق قاعده المفتاح التالية علي كافة إجراءات معالجه الاستثناءات هذه: لا يمكن استبدال رقم المجموعة التي تم حجزها للعميل برقم مجموعه مختلف ، ولكن لا يمكن تغيير ابعاد التخزين الخاصة به (لوحه الموقع والترخيص) من خلال اي منهما التحديث اليدوي بواسطة المستخدم أو التحديث التلقائي بواسطة النظام.</span><span class="sxs-lookup"><span data-stu-id="23ef4-277">The following key rule is applied to all these exception handling actions: the batch number that was reserved for the customer can never be replaced with a different batch number, but its storage dimensions (location and license plate) can be changed through either a manual update by the user or an automatic update by the system.</span></span> <span data-ttu-id="23ef4-278">ويعتمد التحديث التلقائي علي نفس التعيين العشوائي لابعاد التخزين التي يتم تطبيقها عند حجز مجموعه معينه تلقائيا ولكن لم يتم تحديد أية ابعاد للتخزين.</span><span class="sxs-lookup"><span data-stu-id="23ef4-278">The automatic update is based on the same random assignment of storage dimensions that applied when a specific batch was automatically reserved but no storage dimensions were specified.</span></span>

### <a name="example-scenario"></a><span data-ttu-id="23ef4-279">سيناريو كمثال</span><span class="sxs-lookup"><span data-stu-id="23ef4-279">Example scenario</span></span>

<span data-ttu-id="23ef4-280">مثال عن هذا السيناريو هو موقف حيث تم إكمال العمل سابقا يتم إلغاء انتقائها باستخدام وظيفة **تقليل الكمية المنتقاة**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-280">An example of this scenario is a situation where previously completed work is being unpicked by using the **Reduce picked quantity** function.</span></span> <span data-ttu-id="23ef4-281">ويستمر هذا المثال في المثال السابق في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="23ef4-281">This example continues the previous example in this topic.</span></span>

1. <span data-ttu-id="23ef4-282">انتقال إلى **إدارة المستودعات**\>**أحمال**\>**جميع الأحمال**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-282">Go to **Warehouse management** \> **Loads** \> **Active loads**.</span></span>
2. <span data-ttu-id="23ef4-283">حدد الحمل الذي تم إنشاؤه فيما يتعلق بشحنه أمر التوريد الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="23ef4-283">Select the load that was created in connection with the shipment of your sales order.</span></span>
3. <span data-ttu-id="23ef4-284">من بنود علامة التبويب السريعة **سطور أمر التحميل**، حدد **تقليل الكمية المنتقاة**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-284">From the **Load order lines** FastTab, select **Reduce picked quantity**.</span></span>
4. <span data-ttu-id="23ef4-285">في الصفحة **تقليل الكمية المنتقاة** في الحقل **نقل إلى الموقع** ، حدد **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-285">On the **Reduce picked quantity** page, in the **Move to location** field, select **FL-001**.</span></span>
5. <span data-ttu-id="23ef4-286">في الحقل **الانتقال إلى لوحة الترخيص**، حدد **LP33**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-286">In the **Move to license plate** field, select **LP33**.</span></span>
6. <span data-ttu-id="23ef4-287">في الشبكة، في الحقل **كميه المخزون التي سيتم إلغاء انتقائها**، أدخل **10.**</span><span class="sxs-lookup"><span data-stu-id="23ef4-287">In the grid, in the **Inventory quantity to unpick** field, enter **10**.</span></span>
7. <span data-ttu-id="23ef4-288">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-288">Select **OK**.</span></span>

<span data-ttu-id="23ef4-289">وفيما يلي نتائج اجراء إلغاء الانتقاء:</span><span class="sxs-lookup"><span data-stu-id="23ef4-289">Here are the results of the unpicking action:</span></span>

- <span data-ttu-id="23ef4-290">تم تعيين حالة العمل الذي تم إغلاقه مسبقا إلى **ملغى**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-290">The status of the previously closed work is set to **Canceled**.</span></span>
- <span data-ttu-id="23ef4-291">يتم إنشاء العمل الجديد لنوع**حركه المخزون** للكمية التي تم إلغاء انتقاؤها والتي تبلغ **10** بالنسبة لرقم الدفعة **B11**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-291">New work of the **Inventory movement** type is created for the unpicked quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="23ef4-292">يمثل هذا العمل الانتقال من موقع**باب تحميل البضائع** إلى لوحه الترخيص **LP33** في الموقع **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-292">This work represents the movement from the **Baydoor** location to license plate **LP33** in location **FL-001**.</span></span> <span data-ttu-id="23ef4-293">تم تعيين الحقل إلى الحالة **مغلق**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-293">The status is set to **Closed**.</span></span>
- <span data-ttu-id="23ef4-294">قام النظام باعاده حجز رقم المجموعة الذي تم طلبه في الأصل، ويقوم بتعيين معرفات لوحات الترخيص والموقع.</span><span class="sxs-lookup"><span data-stu-id="23ef4-294">The system re-reserves the batch number that was originally ordered, and assigns the location and license plate IDs.</span></span> <span data-ttu-id="23ef4-295">(هذه العملية مكافئه لتشغيل وظيفة **البند الاحتياطي** لسطر الأمر الخاص برقم دفعه معين).</span><span class="sxs-lookup"><span data-stu-id="23ef4-295">(This process is equivalent to running the **Reserve line** function for the order line for a given batch number).</span></span> <span data-ttu-id="23ef4-296">ونتيجة لذلك، يتم عرض الدفعة**B11** كما تم تنفيذها في علامة التبويب السريعة **أرقام المجموعات التي تم التزام بها علي الخط المصدر**في صفحة  **حجز الدفعة** ويحتوي الحقل **الحجز** على الكمية **10** لرقم الدفعة **B11**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-296">As a result, batch **B11** is shown as committed on the **Batch numbers committed to source line** FastTab of the **Batch reservation** page, and the **Reservation** field contains a quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="23ef4-297">بالاضافه إلى ذلك يتم تعيين حقل**الموقع** على **FL-001** ويتم تعيين**لوحة الترخيص** على **LP11**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-297">Additionally, the **Location** field is set to **FL-001**, and the **License plate** field is set to **LP11**.</span></span> <span data-ttu-id="23ef4-298">(يمكنك أضافه هذه الحقول إلى الشبكة إذا لم تكن مرئية.)</span><span class="sxs-lookup"><span data-stu-id="23ef4-298">(You can add these fields to the grid if they aren't visible.)</span></span>

<span data-ttu-id="23ef4-299">توفر الجداول التالية نظره عامه توضح كيفيه قيام النظام بمعالجه حجز المجموعات المرتبطة بالأمر لإجراءات مستودع معينه.</span><span class="sxs-lookup"><span data-stu-id="23ef4-299">The following tables provide an overview that shows how the system handles order-committed batch reservation for specific warehouse actions.</span></span> <span data-ttu-id="23ef4-300">لتفسير المحتوي في الجداول ، افترض انه يتم تشغيل كل اجراء للمستودع في سياق عمل المستودع الموجود الذي ينتج عن حجز المجموعة المرتبطة بالأمر ، أو ان تنفيذ كل اجراء مستودع يؤثر علي العمل من هذا النوع.</span><span class="sxs-lookup"><span data-stu-id="23ef4-300">To interpret the content in the tables, assume that each warehouse action is run in the context of existing warehouse work that originates from an order-committed batch reservation, or that execution of each warehouse action affects work of that type.</span></span>

> [!NOTE]
> <span data-ttu-id="23ef4-301">في هذه الجداول ، يشير العمود "الكمية المجمعة" إلى ما إذا كانت كميه المجموعة متوفرة بالاضافه إلى الكمية التي تم حجزها بالفعل بالنسبة لعمليات الحجز المرتبطة بالأمر أو المحجوزة بالفعل بواسطة عمل المستودع الذي تنشا من عمليات الحجز لذلك النوع.</span><span class="sxs-lookup"><span data-stu-id="23ef4-301">In these tables, the "Batch quantity is available" column indicates whether a batch quantity is available in addition to the quantity that is either already reserved for the current order-committed reservations or already reserved by the warehouse work that originates from reservations of that type.</span></span>

#### <a name="override-the-pick-location-on-the-open-work"></a><span data-ttu-id="23ef4-302">تجاوز موقع الانتقاء في العمل المفتوح</span><span class="sxs-lookup"><span data-stu-id="23ef4-302">Override the pick location on the open work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="23ef4-303">معلمة الإعداد الرئيسية</span><span class="sxs-lookup"><span data-stu-id="23ef4-303">Key setup parameter</span></span></th>
<th><span data-ttu-id="23ef4-304">كمية الدفعة متاحة</span><span class="sxs-lookup"><span data-stu-id="23ef4-304">Batch quantity is available</span></span></th>
<th><span data-ttu-id="23ef4-305">خطوات المستخدم الاساسيه</span><span class="sxs-lookup"><span data-stu-id="23ef4-305">Key user steps</span></span></th>
<th><span data-ttu-id="23ef4-306">عمل المستودع</span><span class="sxs-lookup"><span data-stu-id="23ef4-306">Warehouse work</span></span></th>
<th><span data-ttu-id="23ef4-307">حجز المجموعة المرتبطة بالأمر</span><span class="sxs-lookup"><span data-stu-id="23ef4-307">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="23ef4-308">تم تمكين خيار <strong>السماح بتجاوز موقع الانتقاء</strong> علي العامل.</span><span class="sxs-lookup"><span data-stu-id="23ef4-308">The <strong>Allow pick location override</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="23ef4-309">‏‏نعم</span><span class="sxs-lookup"><span data-stu-id="23ef4-309">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="23ef4-310">حدد عنصر القائمة <strong>تجاوز الموقع</strong> في Warehouse Mmobile App (WMA) عند بدء عمل الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="23ef4-310">Select the <strong>Override location</strong> menu item on the Warehouse Mmobile App (WMA) when you start picking work.</span></span></li>
<li><span data-ttu-id="23ef4-311">حدد <strong>اقتراح</strong>.</span><span class="sxs-lookup"><span data-stu-id="23ef4-311">Select <strong>Suggest</strong>.</span></span></li>
<li><span data-ttu-id="23ef4-312">قم بتاكيد الموقع الجديد المقترح بناء علي توفر كميه الدفعة.</span><span class="sxs-lookup"><span data-stu-id="23ef4-312">Confirm the new location that is suggested based on batch quantity availability.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="23ef4-313">تحدث الإجراءات التالية في العمل الحالي:</span><span class="sxs-lookup"><span data-stu-id="23ef4-313">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="23ef4-314">ويتم تحديث الموقع الموجود في بند الانتقاء في الموقع الجديد.</span><span class="sxs-lookup"><span data-stu-id="23ef4-314">The location on the pick line is updated to the new location.</span></span> <span data-ttu-id="23ef4-315">(إذا كان الموقع لوحه ترخيص – يتم التحكم به ، يتم تعيين لوحه ترخيص عشوائية لحركه مخزون العمل ، ويمكن للعامل الانتقاء من اي لوحه ترخيص بالكمية المتاحة.)</span><span class="sxs-lookup"><span data-stu-id="23ef4-315">(If the location is license plate–controlled, a random license plate is assigned to the work inventory transaction, and the worker can pick from any license plate that has available quantity.)</span></span></li>
<li><span data-ttu-id="23ef4-316">في حاله العثور علي الكمية في أكثر من لوحه ترخيص واحده في الموقع الجديد ، يتم تقسيم بند الانتقاء الأصلي إلى بنود متعددة لمطابقه كل لوحه ترخيص.</span><span class="sxs-lookup"><span data-stu-id="23ef4-316">If the quantity is found on more than one license plate in the new location, the original pick line is split into multiple lines to match each license plate.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="23ef4-317">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="23ef4-317">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="23ef4-318">لا</span><span class="sxs-lookup"><span data-stu-id="23ef4-318">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="23ef4-319">حدد عنصر القائمة <strong>تجاوز الموقع</strong> في (WMA) عند بدء عمل الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="23ef4-319">Select the <strong>Override location</strong> menu item on the WMA when you start picking work.</span></span></li>
<li><span data-ttu-id="23ef4-320">ادخل موقعا يدويا.</span><span class="sxs-lookup"><span data-stu-id="23ef4-320">Manually enter a location.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="23ef4-321">اجراء <strong>تجاوز الموقع</strong> غير ممكن.</span><span class="sxs-lookup"><span data-stu-id="23ef4-321">The <strong>Override location</strong> action isn't possible.</span></span> <span data-ttu-id="23ef4-322">وهو يفشل ويتم عرض خطا.</span><span class="sxs-lookup"><span data-stu-id="23ef4-322">It fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="23ef4-323">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="23ef4-323">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a><span data-ttu-id="23ef4-324">الزر الكامل – تقسيم بند العمل نظرا لتجاوز الحد الأقصى لموقع المستخدم</span><span class="sxs-lookup"><span data-stu-id="23ef4-324">Full button – Split a work line because of overflow on the user location</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="23ef4-325">معلمة الإعداد الرئيسية</span><span class="sxs-lookup"><span data-stu-id="23ef4-325">Key setup parameter</span></span></th>
<th><span data-ttu-id="23ef4-326">كمية الدفعة متاحة</span><span class="sxs-lookup"><span data-stu-id="23ef4-326">Batch quantity is available</span></span></th>
<th><span data-ttu-id="23ef4-327">خطوات المستخدم الاساسيه</span><span class="sxs-lookup"><span data-stu-id="23ef4-327">Key user steps</span></span></th>
<th><span data-ttu-id="23ef4-328">عمل المستودع</span><span class="sxs-lookup"><span data-stu-id="23ef4-328">Warehouse work</span></span></th>
<th><span data-ttu-id="23ef4-329">حجز المجموعة المرتبطة بالأمر</span><span class="sxs-lookup"><span data-stu-id="23ef4-329">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="23ef4-330">يتم <strong>تمكين خيار السماح</strong> بتقسيم العمل في عنصر القائمة جهاز المحمول.</span><span class="sxs-lookup"><span data-stu-id="23ef4-330">The <strong>Allow splitting of work</strong> option is enabled on the mobile device menu item.</span></span></td>
<td><span data-ttu-id="23ef4-331">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="23ef4-331">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="23ef4-332">حدد عنصر القائمة <strong>كامل</strong> في (WMA) عند معالجة عمل الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="23ef4-332">Select the <strong>Full</strong> menu item on the WMA when you process picking work.</span></span></li>
<li><span data-ttu-id="23ef4-333">في الحقل <strong>كميه الانتقاء</strong>، ادخل كميه جزئيه من الانتقاء المطلوب للاشاره إلى القدرة الكاملة.</span><span class="sxs-lookup"><span data-stu-id="23ef4-333">In the <strong>Pick Qty</strong> field, enter a partial quantity of the required pick to indicate the full capacity.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="23ef4-334">وفي العمل الحالي ، يتم تحديث الكمية إلى الكمية المتبقية التي يجب انتقاؤها.</span><span class="sxs-lookup"><span data-stu-id="23ef4-334">On the current work, the quantity is updated to the remaining quantity that must be picked.</span></span></li>
<li><span data-ttu-id="23ef4-335">يتم إنشاء العمل الجديد للكمية المنتقية وإغلاقه.</span><span class="sxs-lookup"><span data-stu-id="23ef4-335">New work for the picked quantity is created and closed.</span></span></li>
</ul></td>
<td><span data-ttu-id="23ef4-336">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="23ef4-336">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a><span data-ttu-id="23ef4-337">تقليل الكمية المنتقاة للعمل المكتمل (من التحميل)</span><span class="sxs-lookup"><span data-stu-id="23ef4-337">Reduce the picked quantity of completed work (from a load)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="23ef4-338">معلمة الإعداد الرئيسية</span><span class="sxs-lookup"><span data-stu-id="23ef4-338">Key setup parameter</span></span></th>
<th><span data-ttu-id="23ef4-339">كمية الدفعة متاحة</span><span class="sxs-lookup"><span data-stu-id="23ef4-339">Batch quantity is available</span></span></th>
<th><span data-ttu-id="23ef4-340">خطوات المستخدم الاساسيه</span><span class="sxs-lookup"><span data-stu-id="23ef4-340">Key user steps</span></span></th>
<th><span data-ttu-id="23ef4-341">عمل المستودع</span><span class="sxs-lookup"><span data-stu-id="23ef4-341">Warehouse work</span></span></th>
<th><span data-ttu-id="23ef4-342">حجز المجموعة المرتبطة بالأمر</span><span class="sxs-lookup"><span data-stu-id="23ef4-342">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="23ef4-343">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="23ef4-343">Not applicable</span></span></td>
<td><span data-ttu-id="23ef4-344">‏‏نعم</span><span class="sxs-lookup"><span data-stu-id="23ef4-344">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="23ef4-345">افتح صفحه <strong>تقليل الكمية المنتقاة</strong> من بند التحميل.</span><span class="sxs-lookup"><span data-stu-id="23ef4-345">Open the <strong>Reduce picked quantity</strong> page from the load line.</span></span></li>
<li><span data-ttu-id="23ef4-346">إدخال الكمية الكاملة المراد انتقاؤها.</span><span class="sxs-lookup"><span data-stu-id="23ef4-346">Enter the full quantity to unpick.</span></span></li>
<li><span data-ttu-id="23ef4-347">حدد لوحة الترخيص/الموقع "تحريك إلى".</span><span class="sxs-lookup"><span data-stu-id="23ef4-347">Select a "move to" location/license plate.</span></span></li>
</ol>
</td>
<td>
<ul> 
<li><span data-ttu-id="23ef4-348">تم إلغاء العمل المرتبط ببند التحميل.</span><span class="sxs-lookup"><span data-stu-id="23ef4-348">Work that is associated with the load line is canceled.</span></span></li>
<li><span data-ttu-id="23ef4-349">يتم إنشاء العمل الجديد لحركة المخزون وإغلاقه.</span><span class="sxs-lookup"><span data-stu-id="23ef4-349">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="23ef4-350">تمت إعاده حجز الكمية لنفس المجموعة.</span><span class="sxs-lookup"><span data-stu-id="23ef4-350">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="23ef4-351">يقوم النظام بتعيين الموقع ولوحه الترخيص عشوائيا (إذا كان الموقع لوحه ترخيص – يتم التحكم به) حيث تكون الكمية متاحه.</span><span class="sxs-lookup"><span data-stu-id="23ef4-351">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="23ef4-352">لا</span><span class="sxs-lookup"><span data-stu-id="23ef4-352">No</span></span></td>
<td><span data-ttu-id="23ef4-353">راجع الصف السابق.</span><span class="sxs-lookup"><span data-stu-id="23ef4-353">See the previous row.</span></span></td>
<td><span data-ttu-id="23ef4-354">راجع الصف السابق.</span><span class="sxs-lookup"><span data-stu-id="23ef4-354">See the previous row.</span></span></td>
<td><span data-ttu-id="23ef4-355">يتم أعاده حجز الكمية لنفس المجموعة، ولنفس الموقع ولوحه الترخيص (إذا كان الموقع عبارة عن لوحه ترخيص – يتم التحكم به) والتي تم إدخالها اثناء إلغاء الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="23ef4-355">The quantity is re-reserved for the same batch, and for the same location and license plate (if the location is license plate–controlled) that were entered during unpicking.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a><span data-ttu-id="23ef4-356">نقل صنف داخل مستودع</span><span class="sxs-lookup"><span data-stu-id="23ef4-356">Move an item within a warehouse</span></span>

> [!NOTE]
> <span data-ttu-id="23ef4-357">لا ينطبق اجراء المستودع الا علي حركه نوع **عمليه إنشاء العمل**، وليس للحركة بواسطة القالب.</span><span class="sxs-lookup"><span data-stu-id="23ef4-357">This warehouse action is applicable only to movement of the **Work creation process** type, not to movement by template.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="23ef4-358">معلمة الإعداد الرئيسية</span><span class="sxs-lookup"><span data-stu-id="23ef4-358">Key setup parameter</span></span></th>
<th><span data-ttu-id="23ef4-359">كمية الدفعة متاحة</span><span class="sxs-lookup"><span data-stu-id="23ef4-359">Batch quantity is available</span></span></th>
<th><span data-ttu-id="23ef4-360">خطوات المستخدم الاساسيه</span><span class="sxs-lookup"><span data-stu-id="23ef4-360">Key user steps</span></span></th>
<th><span data-ttu-id="23ef4-361">عمل المستودع</span><span class="sxs-lookup"><span data-stu-id="23ef4-361">Warehouse work</span></span></th>
<th><span data-ttu-id="23ef4-362">حجز المجموعة المرتبطة بالأمر</span><span class="sxs-lookup"><span data-stu-id="23ef4-362">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="23ef4-363">يتم تمكين خيار <strong>السماح بنقل المخزون مع العمل المقترن</strong> علي العامل.</span><span class="sxs-lookup"><span data-stu-id="23ef4-363">The <strong>Allow movement of inventory with associated work</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="23ef4-364">‏‏نعم</span><span class="sxs-lookup"><span data-stu-id="23ef4-364">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="23ef4-365">بدء حركه في WMA.</span><span class="sxs-lookup"><span data-stu-id="23ef4-365">Start a movement on the WMA.</span></span></li>
<li><span data-ttu-id="23ef4-366">أدخل موقعي البداية والنهاية.</span><span class="sxs-lookup"><span data-stu-id="23ef4-366">Enter "from" and "to" locations.</span></span></li>
</ol></td>
<td>
<ul>
<li><span data-ttu-id="23ef4-367">وفي كل العمل الموجود الذي يتاثر بالنقل ، يتم تحديث موقع الانتقاء إلى الموقع "إلى" الجديد.</span><span class="sxs-lookup"><span data-stu-id="23ef4-367">On all existing work that is affected by the move, the pick location is updated to the new "to" location.</span></span></li>
<li><span data-ttu-id="23ef4-368">يتم إنشاء العمل الجديد لحركة المخزون وإغلاقه.</span><span class="sxs-lookup"><span data-stu-id="23ef4-368">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="23ef4-369">تتم أعاده حجز كافة عمليات الحجز الموجودة التي تاثرت بحركة الكمية من الموقع المحدد لنفس المجموعة.</span><span class="sxs-lookup"><span data-stu-id="23ef4-369">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch.</span></span> <span data-ttu-id="23ef4-370">يقوم النظام بتعيين الموقع ولوحه الترخيص عشوائيا (إذا كان الموقع لوحه ترخيص – يتم التحكم به) حيث تكون الكمية متاحه.</span><span class="sxs-lookup"><span data-stu-id="23ef4-370">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="23ef4-371">لا</span><span class="sxs-lookup"><span data-stu-id="23ef4-371">No</span></span></td>
<td><span data-ttu-id="23ef4-372">راجع الصف السابق.</span><span class="sxs-lookup"><span data-stu-id="23ef4-372">See the previous row.</span></span></td>
<td><span data-ttu-id="23ef4-373">راجع الصف السابق.</span><span class="sxs-lookup"><span data-stu-id="23ef4-373">See the previous row.</span></span></td>
<td><span data-ttu-id="23ef4-374">يتم أعاده حجز كافة عمليات الحجز الموجودة التي تاثرت بحركة الكمية من الموقع المحدد لنفس المجموعة ، وللموقع الجديد "إلى" ولوحه الترخيص (إذا كان الموقع لوحه الترخيص-التي يتم التحكم بها).</span><span class="sxs-lookup"><span data-stu-id="23ef4-374">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch, and for the new "to" location and license plate (if the location is license plate–controlled).</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a><span data-ttu-id="23ef4-375">حجز الكمية المنتقاة للعمل المكتمل (من التحميل أو الموجة)</span><span class="sxs-lookup"><span data-stu-id="23ef4-375">Reverse the picked quantity of completed work (from a load or a wave)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="23ef4-376">معلمة الإعداد الرئيسية</span><span class="sxs-lookup"><span data-stu-id="23ef4-376">Key setup parameter</span></span></th>
<th><span data-ttu-id="23ef4-377">كمية الدفعة متاحة</span><span class="sxs-lookup"><span data-stu-id="23ef4-377">Batch quantity is available</span></span></th>
<th><span data-ttu-id="23ef4-378">خطوات المستخدم الاساسيه</span><span class="sxs-lookup"><span data-stu-id="23ef4-378">Key user steps</span></span></th>
<th><span data-ttu-id="23ef4-379">عمل المستودع</span><span class="sxs-lookup"><span data-stu-id="23ef4-379">Warehouse work</span></span></th>
<th><span data-ttu-id="23ef4-380">حجز المجموعة المرتبطة بالأمر</span><span class="sxs-lookup"><span data-stu-id="23ef4-380">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'><span data-ttu-id="23ef4-381">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="23ef4-381">Not applicable</span></span></td>
<td><span data-ttu-id="23ef4-382">‏‏نعم</span><span class="sxs-lookup"><span data-stu-id="23ef4-382">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="23ef4-383">افتح صفحه <strong>العمل العكسي</strong>.</span><span class="sxs-lookup"><span data-stu-id="23ef4-383">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="23ef4-384">في الصفحة طلب ، حدد الخيار <strong>ترك العناصر في الموقع الحالي</strong>.</span><span class="sxs-lookup"><span data-stu-id="23ef4-384">On the request page, select the <strong>Leave items at current location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="23ef4-385">تم إلغاء العمل المرتبط بالتحميل.</span><span class="sxs-lookup"><span data-stu-id="23ef4-385">All work that is associated with the load is canceled.</span></span></td>
<td><span data-ttu-id="23ef4-386">تمت إعاده حجز الكمية لنفس المجموعة.</span><span class="sxs-lookup"><span data-stu-id="23ef4-386">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="23ef4-387">يقوم النظام بتعيين الموقع ولوحه الترخيص عشوائيا (إذا كان الموقع لوحه ترخيص – يتم التحكم به) حيث تكون الكمية متاحه.</span><span class="sxs-lookup"><span data-stu-id="23ef4-387">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="23ef4-388">لا</span><span class="sxs-lookup"><span data-stu-id="23ef4-388">No</span></span></td>
<td><span data-ttu-id="23ef4-389">راجع الصف السابق.</span><span class="sxs-lookup"><span data-stu-id="23ef4-389">See the previous row.</span></span></td>
<td><span data-ttu-id="23ef4-390">راجع الصف السابق.</span><span class="sxs-lookup"><span data-stu-id="23ef4-390">See the previous row.</span></span></td>
<td><span data-ttu-id="23ef4-391">يتم أعاده حجز الكمية لنفس المجموعة ، وللوح الموقع والترخيص الذي تم فيه ترك الكمية عند إلغاء.</span><span class="sxs-lookup"><span data-stu-id="23ef4-391">The quantity is re-reserved for the same batch, and for the location and license plate where the quantity was left upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="23ef4-392">‏‏نعم</span><span class="sxs-lookup"><span data-stu-id="23ef4-392">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="23ef4-393">افتح صفحه <strong>العمل العكسي</strong>.</span><span class="sxs-lookup"><span data-stu-id="23ef4-393">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="23ef4-394">في الصفحة طلب ، حدد الخيار <strong>تعيين العناصر للموقع الحالي</strong>.</span><span class="sxs-lookup"><span data-stu-id="23ef4-394">On the request page, select the <strong>Assign items to this location</strong> option.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="23ef4-395">تم إلغاء العمل الحالي.</span><span class="sxs-lookup"><span data-stu-id="23ef4-395">The current work is canceled.</span></span></li>
<li><span data-ttu-id="23ef4-396">يتم إنشاء العمل الجديد لحركة المخزون وإغلاقه.</span><span class="sxs-lookup"><span data-stu-id="23ef4-396">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="23ef4-397">تمت إعاده حجز الكمية لنفس المجموعة.</span><span class="sxs-lookup"><span data-stu-id="23ef4-397">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="23ef4-398">يقوم النظام بتعيين الموقع ولوحه الترخيص عشوائيا (إذا كان الموقع لوحه ترخيص – يتم التحكم به) حيث تكون الكمية متاحه.</span><span class="sxs-lookup"><span data-stu-id="23ef4-398">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="23ef4-399">لا</span><span class="sxs-lookup"><span data-stu-id="23ef4-399">No</span></span></td>
<td><span data-ttu-id="23ef4-400">راجع الصف السابق.</span><span class="sxs-lookup"><span data-stu-id="23ef4-400">See the previous row.</span></span></td>
<td><span data-ttu-id="23ef4-401">راجع الصف السابق.</span><span class="sxs-lookup"><span data-stu-id="23ef4-401">See the previous row.</span></span></td>
<td><span data-ttu-id="23ef4-402">يتم أعاده حجز الكمية لنفس المجموعة ، وللوح الموقع والترخيص الذي تم فيه تعيين الكمية عند إلغاء.</span><span class="sxs-lookup"><span data-stu-id="23ef4-402">The quantity is re-reserved for the same batch, and for the location and license plate that the quantity was assigned to upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="23ef4-403">نعم/لا</span><span class="sxs-lookup"><span data-stu-id="23ef4-403">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="23ef4-404">افتح صفحه <strong>العمل العكسي</strong>.</span><span class="sxs-lookup"><span data-stu-id="23ef4-404">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="23ef4-405">في الصفحة طلب ، حدد الخيار <strong>نقل العناصر إلى هذا الموقع</strong>.</span><span class="sxs-lookup"><span data-stu-id="23ef4-405">On the request page, select the <strong>Move items to this location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="23ef4-406">العكس غير معتمد.</span><span class="sxs-lookup"><span data-stu-id="23ef4-406">Reversal isn't supported.</span></span></td>
<td><span data-ttu-id="23ef4-407">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="23ef4-407">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="23ef4-408">نعم/لا</span><span class="sxs-lookup"><span data-stu-id="23ef4-408">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="23ef4-409">افتح صفحه <strong>العمل العكسي</strong>.</span><span class="sxs-lookup"><span data-stu-id="23ef4-409">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="23ef4-410">في الصفحة طلب ، حدد الخيار <strong>نقل العناصر على أساس موجهات الموقع</strong>.</span><span class="sxs-lookup"><span data-stu-id="23ef4-410">On the request page, select the <strong>Move items based on location directives</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="23ef4-411">العكس غير معتمد.</span><span class="sxs-lookup"><span data-stu-id="23ef4-411">Reversal isn't supported.</span></span> </td>
<td><span data-ttu-id="23ef4-412">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="23ef4-412">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a><span data-ttu-id="23ef4-413">قصور انتقاء الكمية – تسجيل الكمية بأنها لم يتم العثور عليها فعليا في لوحه الترخيص/الموقع اثناء اجراء عمل الانتقاء</span><span class="sxs-lookup"><span data-stu-id="23ef4-413">Short-pick a quantity – Register the quantity as physically not found at the location/license plate while you perform picking work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="23ef4-414">معلمة الإعداد الرئيسية</span><span class="sxs-lookup"><span data-stu-id="23ef4-414">Key setup parameter</span></span></th>
<th><span data-ttu-id="23ef4-415">كمية الدفعة متاحة</span><span class="sxs-lookup"><span data-stu-id="23ef4-415">Batch quantity is available</span></span></th>
<th><span data-ttu-id="23ef4-416">خطوات المستخدم الاساسيه</span><span class="sxs-lookup"><span data-stu-id="23ef4-416">Key user steps</span></span></th>
<th><span data-ttu-id="23ef4-417">عمل المستودع</span><span class="sxs-lookup"><span data-stu-id="23ef4-417">Warehouse work</span></span></th>
<th><span data-ttu-id="23ef4-418">حجز المجموعة المرتبطة بالأمر</span><span class="sxs-lookup"><span data-stu-id="23ef4-418">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="23ef4-419">تم اعداد استثناء عمل لنوع <strong>الانتقاء القصير</strong> حيث <strong>إعادة توزيع الصنف</strong> = <strong>لا شيء</strong> و <strong>وتسوية المخزون</strong> = <strong>نعم</strong> و <strong>إزالة عمليات الحجز</strong> = <strong>لا</strong>.</span><span class="sxs-lookup"><span data-stu-id="23ef4-419">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span></td>
<td><span data-ttu-id="23ef4-420">‏‏نعم</span><span class="sxs-lookup"><span data-stu-id="23ef4-420">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="23ef4-421">حدد عنصر القائمة <strong>انتقاء قصير</strong> في (WMA) عند تشغيل عمل الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="23ef4-421">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="23ef4-422">في حقل <strong>كمية الانتقاء</strong>، أدخل <strong>0</strong> (صفرًا).</span><span class="sxs-lookup"><span data-stu-id="23ef4-422">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="23ef4-423">في حقل <strong>السبب</strong>، أدخل <strong>لا توجد إعادة توزيع</strong>.</span><span class="sxs-lookup"><span data-stu-id="23ef4-423">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="23ef4-424">يتم إغلاق العمل الحالي، وتكون الكمية المنتقاة هي 0 (صفر).</span><span class="sxs-lookup"><span data-stu-id="23ef4-424">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="23ef4-425">يتم إنشاء حركه مخزون لنوع <strong>الجرد</strong>  ونوع الإصدار <strong>مباع</strong> ليمثل التعديل.</span><span class="sxs-lookup"><span data-stu-id="23ef4-425">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="23ef4-426">تمت إعاده حجز الكمية لنفس المجموعة.</span><span class="sxs-lookup"><span data-stu-id="23ef4-426">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="23ef4-427">يقوم النظام بتعيين الموقع ولوحه الترخيص عشوائيا (إذا كان الموقع لوحه ترخيص – يتم التحكم به) حيث تكون الكمية متاحه.</span><span class="sxs-lookup"><span data-stu-id="23ef4-427">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="23ef4-428">لا</span><span class="sxs-lookup"><span data-stu-id="23ef4-428">No</span></span></td>
<td><span data-ttu-id="23ef4-429">راجع الصف السابق.</span><span class="sxs-lookup"><span data-stu-id="23ef4-429">See the previous row.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="23ef4-430">فشل اجراء الانتقاء القصير، ويتم عرض خطأ.</span><span class="sxs-lookup"><span data-stu-id="23ef4-430">The short-picking action fails, and an error is thrown.</span></span></li>
<li><span data-ttu-id="23ef4-431">يظل العمل الحالي مفتوحا.</span><span class="sxs-lookup"><span data-stu-id="23ef4-431">The current work remains open.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="23ef4-432">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="23ef4-432">Not applicable</span></span></td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="23ef4-433">تم اعداد استثناء عمل لنوع <strong>الانتقاء القصير</strong> حيث <strong>إعادة توزيع الصنف</strong> = <strong>‎لا شيء</strong>، و <strong>تسوية المخزون</strong> = <strong>نعم</strong>، و <strong>‎إزالة عمليات الحجوزات</strong> = <strong>نعم</strong>.</span><span class="sxs-lookup"><span data-stu-id="23ef4-433">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span></td>
<td><span data-ttu-id="23ef4-434">‏‏نعم</span><span class="sxs-lookup"><span data-stu-id="23ef4-434">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="23ef4-435">حدد عنصر القائمة <strong>انتقاء قصير</strong> في (WMA) عند تشغيل عمل الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="23ef4-435">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="23ef4-436">في حقل <strong>كمية الانتقاء</strong>، أدخل <strong>0</strong> (صفرًا).</span><span class="sxs-lookup"><span data-stu-id="23ef4-436">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="23ef4-437">في حقل <strong>السبب</strong>، أدخل <strong>لا توجد إعادة توزيع</strong>.</span><span class="sxs-lookup"><span data-stu-id="23ef4-437">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="23ef4-438">يتم إغلاق العمل الحالي، وتكون الكمية المنتقاة هي 0 (صفر).</span><span class="sxs-lookup"><span data-stu-id="23ef4-438">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="23ef4-439">يتم إنشاء حركه مخزون لنوع <strong>الجرد</strong>  ونوع الإصدار <strong>مباع</strong> ليمثل التعديل.</span><span class="sxs-lookup"><span data-stu-id="23ef4-439">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="23ef4-440">تتم أعاده حجز كافة عمليات الحجز الموجودة التي تاثرت بتسوية الكمية في موقع الانتقاء القصير المعاد حجزه لنفس المجموعة.</span><span class="sxs-lookup"><span data-stu-id="23ef4-440">All existing reservations that are affected by the quantity adjustment in the short-picked location are re-reserved for the same batch.</span></span> <span data-ttu-id="23ef4-441">يقوم النظام بتعيين الموقع ولوحه الترخيص عشوائيا (إذا كان الموقع لوحه ترخيص – يتم التحكم به) حيث تكون الكمية متاحه.</span><span class="sxs-lookup"><span data-stu-id="23ef4-441">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="23ef4-442">لا</span><span class="sxs-lookup"><span data-stu-id="23ef4-442">No</span></span></td>
<td><span data-ttu-id="23ef4-443">راجع الصف السابق.</span><span class="sxs-lookup"><span data-stu-id="23ef4-443">See the previous row.</span></span></td>
<td><span data-ttu-id="23ef4-444">راجع الصف السابق.</span><span class="sxs-lookup"><span data-stu-id="23ef4-444">See the previous row.</span></span></td>
<td><span data-ttu-id="23ef4-445">تمت إزالة جميع الحجوزات الحالية المتأثرة بتسوية الكمية في موقع الانتقاء القصير.</span><span class="sxs-lookup"><span data-stu-id="23ef4-445">All existing reservations that are affected by the quantity adjustment in the short-picked location are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="23ef4-446">تم اعداد استثناء عمل لنوع <strong>الانتقاء القصير</strong> حيث <strong>إعادة توزيع الصنف</strong> = <strong>يدوي</strong>، و <strong>تسوية المخزون</strong> = <strong>نعم</strong>, و <strong>‎إزالة عمليات الحجوزات</strong> = <strong>لا/نعم</strong>.</span><span class="sxs-lookup"><span data-stu-id="23ef4-446">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No/Yes</strong>.</span></span> <span data-ttu-id="23ef4-447">بالاضافه إلى ذلك ، يتم تمكين الخيار <strong>السماح بإعادة توزيع العناصر اليدوية</strong> علي العامل.</span><span class="sxs-lookup"><span data-stu-id="23ef4-447">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="23ef4-448">‏‏نعم</span><span class="sxs-lookup"><span data-stu-id="23ef4-448">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="23ef4-449">حدد عنصر القائمة <strong>انتقاء قصير</strong> في (WMA) عند تشغيل عمل الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="23ef4-449">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="23ef4-450">في حقل <strong>كمية الانتقاء القصير</strong>، أدخل <strong>0</strong> (صفرًا).</span><span class="sxs-lookup"><span data-stu-id="23ef4-450">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="23ef4-451">في الحقل <strong>السبب</strong>، حدد<strong>الانتقاء القصير مع إعادة التوزيع اليدوية</strong>.</span><span class="sxs-lookup"><span data-stu-id="23ef4-451">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="23ef4-452">حدد لوحه الترخيص/الموقع في القائمة.</span><span class="sxs-lookup"><span data-stu-id="23ef4-452">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="23ef4-453">تحدث الإجراءات التالية في العمل الحالي:</span><span class="sxs-lookup"><span data-stu-id="23ef4-453">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="23ef4-454">يتم إغلاق بند الانتقاء، وتكون الكمية المنتقاة هي 0 (صفر).</span><span class="sxs-lookup"><span data-stu-id="23ef4-454">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="23ef4-455">تم إلغاء بند الإدخال.</span><span class="sxs-lookup"><span data-stu-id="23ef4-455">The put line is canceled.</span></span></li>
<li><span data-ttu-id="23ef4-456">يتم إنشاء بند انتقاء جديد.</span><span class="sxs-lookup"><span data-stu-id="23ef4-456">A new pick line is created.</span></span> <span data-ttu-id="23ef4-457">ويستخدم الموقع/لوحه الترخيص التي قام المستخدم بتحديدها.</span><span class="sxs-lookup"><span data-stu-id="23ef4-457">It uses the location/license plate that the user selected.</span></span></li>
<li><span data-ttu-id="23ef4-458">يتم إنشاء بند إدخال جديد.</span><span class="sxs-lookup"><span data-stu-id="23ef4-458">A new put line is created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="23ef4-459">يتم إنشاء حركه مخزون لنوع <strong>الجرد</strong>  ونوع الإصدار <strong>مباع</strong> ليمثل التعديل.</span><span class="sxs-lookup"><span data-stu-id="23ef4-459">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="23ef4-460">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="23ef4-460">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="23ef4-461">تم اعداد استثناء عمل لنوع <strong>الانتقاء القصير</strong> حيث <strong>إعادة توزيع الصنف</strong> = <strong>يدوي</strong> و <strong>تسوية المخزون</strong> = <strong>نعم</strong> و <strong>إزالة عمليات الحجوزات</strong> = <strong>لا</strong>.</span><span class="sxs-lookup"><span data-stu-id="23ef4-461">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span> <span data-ttu-id="23ef4-462">بالاضافه إلى ذلك ، يتم تمكين الخيار <strong>السماح بإعادة توزيع العناصر اليدوية</strong> علي العامل.</span><span class="sxs-lookup"><span data-stu-id="23ef4-462">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="23ef4-463">لا</span><span class="sxs-lookup"><span data-stu-id="23ef4-463">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="23ef4-464">حدد عنصر القائمة <strong>انتقاء قصير</strong> في (WMA) عند تشغيل عمل الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="23ef4-464">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="23ef4-465">في حقل <strong>كمية الانتقاء القصير</strong>، أدخل <strong>0</strong> (صفرًا).</span><span class="sxs-lookup"><span data-stu-id="23ef4-465">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="23ef4-466">في الحقل <strong>السبب</strong>، حدد<strong>الانتقاء القصير مع إعادة التوزيع اليدوية</strong>.</span><span class="sxs-lookup"><span data-stu-id="23ef4-466">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="23ef4-467">فشل اجراء الانتقاء القصير، ويتم عرض خطأ.</span><span class="sxs-lookup"><span data-stu-id="23ef4-467">The short-picking action fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="23ef4-468">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="23ef4-468">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="23ef4-469">تم اعداد استثناء عمل لنوع <strong>الانتقاء القصير</strong> حيث <strong>إعادة توزيع الصنف</strong> = <strong>يدوي</strong> و <strong>تسوية المخزون</strong> = <strong>نعم</strong> و <strong>إزالة عمليات الحجوزات</strong> = <strong>نعم</strong>.</span><span class="sxs-lookup"><span data-stu-id="23ef4-469">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span> <span data-ttu-id="23ef4-470">بالاضافه إلى ذلك ، يتم تمكين الخيار <strong>السماح بإعادة توزيع العناصر اليدوية</strong> علي العامل.</span><span class="sxs-lookup"><span data-stu-id="23ef4-470">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="23ef4-471">لا</span><span class="sxs-lookup"><span data-stu-id="23ef4-471">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="23ef4-472">حدد عنصر القائمة <strong>انتقاء قصير</strong> في (WMA) عند تشغيل عمل الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="23ef4-472">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="23ef4-473">في حقل <strong>كمية الانتقاء القصير</strong>، أدخل <strong>0</strong> (صفرًا).</span><span class="sxs-lookup"><span data-stu-id="23ef4-473">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="23ef4-474">في الحقل <strong>السبب</strong>، حدد<strong>الانتقاء القصير مع إعادة التوزيع اليدوية</strong>.</span><span class="sxs-lookup"><span data-stu-id="23ef4-474">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="23ef4-475">حدد لوحه الترخيص/الموقع في القائمة.</span><span class="sxs-lookup"><span data-stu-id="23ef4-475">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="23ef4-476">تحدث الإجراءات التالية في العمل الحالي:</span><span class="sxs-lookup"><span data-stu-id="23ef4-476">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="23ef4-477">يتم إغلاق بند الانتقاء، وتكون الكمية المنتقاة هي 0 (صفر).</span><span class="sxs-lookup"><span data-stu-id="23ef4-477">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="23ef4-478">تم إلغاء بند الإدخال.</span><span class="sxs-lookup"><span data-stu-id="23ef4-478">The put line is canceled.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="23ef4-479">يتم إنشاء حركه مخزون لنوع <strong>الجرد</strong>  ونوع الإصدار <strong>مباع</strong> ليمثل التعديل.</span><span class="sxs-lookup"><span data-stu-id="23ef4-479">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="23ef4-480">تمت إزالة جميع الحجوزات الحالية المتأثرة بتسوية الكمية في موقع/لوحة ترخيص الانتقاء القصير.</span><span class="sxs-lookup"><span data-stu-id="23ef4-480">All existing reservations that are affected by the quantity adjustment in the short-picked location/license plate are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="23ef4-481">تم اعداد استثناء عمل لنوع <strong>الانتقاء القصير</strong> حيث <strong>إعادة توزيع الصنف</strong> = <strong>تلقائي</strong> و <strong>تسوية المخزون</strong> = <strong>نعم/لا</strong> و <strong>‎إزالة عمليات الحجوزات</strong> = <strong>نعم/لا</strong>.</span><span class="sxs-lookup"><span data-stu-id="23ef4-481">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Automatic</strong>, <strong>Adjust inventory</strong> = <strong>Yes/No</strong>, and <strong>Remove reservations</strong> = <strong>Yes/No</strong>.</span></span></td>
<td><span data-ttu-id="23ef4-482">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="23ef4-482">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="23ef4-483">حدد عنصر القائمة <strong>انتقاء قصير</strong> في (WMA) عند تشغيل عمل الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="23ef4-483">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="23ef4-484">في حقل <strong>كمية الانتقاء القصير</strong>، أدخل <strong>0</strong> (صفرًا).</span><span class="sxs-lookup"><span data-stu-id="23ef4-484">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="23ef4-485">في الحقل <strong>السبب</strong>، حدد<strong>الانتقاء القصير مع إعادة التوزيع التلقائية</strong>.</span><span class="sxs-lookup"><span data-stu-id="23ef4-485">In the <strong>Reason</strong> field, select <strong>Short Picking with automatic reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="23ef4-486">الانتقاء القصير الذي يتضمن إعادة التوزيع تلقائيا غير مدعوم.</span><span class="sxs-lookup"><span data-stu-id="23ef4-486">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
<td><span data-ttu-id="23ef4-487">الانتقاء القصير الذي يتضمن إعادة التوزيع تلقائيا غير مدعوم.</span><span class="sxs-lookup"><span data-stu-id="23ef4-487">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a><span data-ttu-id="23ef4-488">تغيير حالة المخزون</span><span class="sxs-lookup"><span data-stu-id="23ef4-488">Change the inventory status</span></span>

> [!NOTE]
> <span data-ttu-id="23ef4-489">يمكن تنفيذ اجراء المستودع هذا من نقاط إدخال متعددة.</span><span class="sxs-lookup"><span data-stu-id="23ef4-489">This warehouse action can be performed from multiple entry points.</span></span> <span data-ttu-id="23ef4-490">يستخدم المثال الموضح هنا اجراء **تغيير حاله المخزون** في الصفحة **الفعلية حسب الموقع**</span><span class="sxs-lookup"><span data-stu-id="23ef4-490">The example that is shown here uses **Inventory status change** action on the **On-hand by location** page.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="23ef4-491">معلمة الإعداد الرئيسية</span><span class="sxs-lookup"><span data-stu-id="23ef4-491">Key setup parameter</span></span></th>
<th><span data-ttu-id="23ef4-492">كمية الدفعة متاحة</span><span class="sxs-lookup"><span data-stu-id="23ef4-492">Batch quantity is available</span></span></th>
<th><span data-ttu-id="23ef4-493">خطوات المستخدم الاساسيه</span><span class="sxs-lookup"><span data-stu-id="23ef4-493">Key user steps</span></span></th>
<th><span data-ttu-id="23ef4-494">عمل المستودع</span><span class="sxs-lookup"><span data-stu-id="23ef4-494">Warehouse work</span></span></th>
<th><span data-ttu-id="23ef4-495">حجز المجموعة المرتبطة بالأمر</span><span class="sxs-lookup"><span data-stu-id="23ef4-495">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="23ef4-496">في علامة التبويب<strong> المستودع</strong>، في سجل <strong> المستودع</strong> ، يتم تعيين الحقل<strong> حجوزات الازاله والعلامات</strong> إلى <strong>عمليات الحجز</strong> أو <strong>العلامات والحجوزات.</strong></span><span class="sxs-lookup"><span data-stu-id="23ef4-496">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>Reservations</strong> or <strong>Markings and reservations</strong>.</span></span></td>
<td><span data-ttu-id="23ef4-497">‏‏نعم</span><span class="sxs-lookup"><span data-stu-id="23ef4-497">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="23ef4-498">حدد موقعًا معينًا.</span><span class="sxs-lookup"><span data-stu-id="23ef4-498">Select a specific location.</span></span></li>
<li><span data-ttu-id="23ef4-499">حدد البند الذي يحتوي علي أحد الأصناف والمواقع والتراخيص المحددة (إذا كان الموقع لوحه ترخيص – يتم التحكم به).</span><span class="sxs-lookup"><span data-stu-id="23ef4-499">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="23ef4-500">حدد <strong>تغيير حالة المخزون</strong>.</span><span class="sxs-lookup"><span data-stu-id="23ef4-500">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="23ef4-501">قم بتعيين حقل <strong>حاله المخزون</strong> إلى <strong>"تجميد</strong>".</span><span class="sxs-lookup"><span data-stu-id="23ef4-501">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="23ef4-502">لا يسمح باجراء تغييرات علي حاله المخزون للكميات المحجوزة للعمل.</span><span class="sxs-lookup"><span data-stu-id="23ef4-502">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="23ef4-503">تمت إعاده حجز الكمية لنفس المجموعة.</span><span class="sxs-lookup"><span data-stu-id="23ef4-503">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="23ef4-504">يقوم النظام بتعيين الموقع ولوحه الترخيص عشوائيا (إذا كان الموقع لوحه ترخيص – يتم التحكم به) حيث تكون الكمية متاحه.</span><span class="sxs-lookup"><span data-stu-id="23ef4-504">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></li>
<li><span data-ttu-id="23ef4-505">يتم إنشاء حركتي مخزون بنوع <strong>تغيير حاله المخزون</strong> لتمثيل التغيير في بعد حاله المخزون.</span><span class="sxs-lookup"><span data-stu-id="23ef4-505">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="23ef4-506">يتم إنشاء حركه مخزون لنوع <strong>تامين المخزون</strong> ونوع الإصدار <strong>الفعلي المحجوز</strong> لتمثيل حجز الكمية المحظورة.</span><span class="sxs-lookup"><span data-stu-id="23ef4-506">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="23ef4-507">لا</span><span class="sxs-lookup"><span data-stu-id="23ef4-507">No</span></span></td>
<td><span data-ttu-id="23ef4-508">راجع الصف السابق.</span><span class="sxs-lookup"><span data-stu-id="23ef4-508">See the previous row.</span></span></td>
<td><span data-ttu-id="23ef4-509">لا يسمح باجراء تغييرات علي حاله المخزون للكميات المحجوزة للعمل.</span><span class="sxs-lookup"><span data-stu-id="23ef4-509">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="23ef4-510">تمت إزاله الحجز.</span><span class="sxs-lookup"><span data-stu-id="23ef4-510">The reservation is removed.</span></span></li>
<li><span data-ttu-id="23ef4-511">يتم إنشاء حركتي مخزون بنوع <strong>تغيير حاله المخزون</strong> لتمثيل التغيير في بعد حاله المخزون.</span><span class="sxs-lookup"><span data-stu-id="23ef4-511">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="23ef4-512">يتم إنشاء حركه مخزون لنوع <strong>تامين المخزون</strong> ونوع الإصدار <strong>الفعلي المحجوز</strong> لتمثيل حجز الكمية المحظورة.</span><span class="sxs-lookup"><span data-stu-id="23ef4-512">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="23ef4-513">في علامة التبويب <strong>المستودع</strong>، في سجل <strong>المستودع</strong>، يتم تعيين الحقل <strong>حجوزات الازاله والعلامات</strong> إلى <strong>لا شيء</strong>.</span><span class="sxs-lookup"><span data-stu-id="23ef4-513">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>None</strong>.</span></span></td>
<td><span data-ttu-id="23ef4-514">‏‏نعم</span><span class="sxs-lookup"><span data-stu-id="23ef4-514">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="23ef4-515">حدد موقعًا معينًا.</span><span class="sxs-lookup"><span data-stu-id="23ef4-515">Select a specific location.</span></span></li>
<li><span data-ttu-id="23ef4-516">حدد البند الذي يحتوي علي أحد الأصناف والمواقع والتراخيص المحددة (إذا كان الموقع لوحه ترخيص – يتم التحكم به).</span><span class="sxs-lookup"><span data-stu-id="23ef4-516">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="23ef4-517">حدد <strong>تغيير حالة المخزون</strong>.</span><span class="sxs-lookup"><span data-stu-id="23ef4-517">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="23ef4-518">قم بتعيين حقل <strong>حاله المخزون</strong> إلى <strong>"تجميد</strong>".</span><span class="sxs-lookup"><span data-stu-id="23ef4-518">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="23ef4-519">لا يسمح باجراء تغييرات علي حاله المخزون للكميات المحجوزة للعمل.</span><span class="sxs-lookup"><span data-stu-id="23ef4-519">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="23ef4-520">تمت إعاده حجز الكمية لنفس المجموعة.</span><span class="sxs-lookup"><span data-stu-id="23ef4-520">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="23ef4-521">يقوم النظام بتعيين الموقع ولوحه الترخيص عشوائيا (إذا كان الموقع لوحه ترخيص – يتم التحكم به) حيث تكون الكمية متاحه.</span><span class="sxs-lookup"><span data-stu-id="23ef4-521">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="23ef4-522">لا</span><span class="sxs-lookup"><span data-stu-id="23ef4-522">No</span></span></td>
<td><span data-ttu-id="23ef4-523">راجع الصف السابق.</span><span class="sxs-lookup"><span data-stu-id="23ef4-523">See the previous row.</span></span></td>
<td><span data-ttu-id="23ef4-524">لا يسمح باجراء تغييرات علي حاله المخزون للكميات المحجوزة للعمل.</span><span class="sxs-lookup"><span data-stu-id="23ef4-524">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="23ef4-525">لا يسمح بتغييرات حاله المخزون.</span><span class="sxs-lookup"><span data-stu-id="23ef4-525">Inventory status changes aren't allowed.</span></span></td>
</tr>
</tbody>
</table>

## <a name="limitations"></a><span data-ttu-id="23ef4-526">قيود</span><span class="sxs-lookup"><span data-stu-id="23ef4-526">Limitations</span></span>

- <span data-ttu-id="23ef4-527">لا تدعم وظيفة حجز بعد علي مستوي المستودع المرن الميزات التالية:</span><span class="sxs-lookup"><span data-stu-id="23ef4-527">The flexible warehouse-level dimension reservation functionality doesn't support the following features:</span></span>

    - <span data-ttu-id="23ef4-528">أداره وزن التقاط</span><span class="sxs-lookup"><span data-stu-id="23ef4-528">Catch weight management</span></span>
    - <span data-ttu-id="23ef4-529">مخزون سالب مادي</span><span class="sxs-lookup"><span data-stu-id="23ef4-529">Physical negative inventory</span></span>
    - <span data-ttu-id="23ef4-530">الحجز مقابل التوريد المطلوب</span><span class="sxs-lookup"><span data-stu-id="23ef4-530">Reservation against ordered supply</span></span>
    - <span data-ttu-id="23ef4-531">أوامر التحويل وانتقاء المادة الخام</span><span class="sxs-lookup"><span data-stu-id="23ef4-531">Transfer orders and raw material picking</span></span>

- <span data-ttu-id="23ef4-532">تشتمل قاعده دمج الحاوية للتعبئة حسب الوحدة الموجهة عليها علي قيود.</span><span class="sxs-lookup"><span data-stu-id="23ef4-532">The container consolidation rule for packing by directive unit has limitations.</span></span> <span data-ttu-id="23ef4-533">بالنسبة لعمليات الحجز المرتبطة بالطلبات ، نوصي بعدم استخدام قوالب بنيه الحاوية حيث تم تمكين الحزم حسب حقل **الوحدة الموجهة**.</span><span class="sxs-lookup"><span data-stu-id="23ef4-533">For order-committed reservations, we recommend that you not use container build templates where the **Pack by directive unit** field is enabled.</span></span> <span data-ttu-id="23ef4-534">في التصميم الحالي ، لا يتم استخدام توجيهات المواقع عند إنشاء عمل المستودع.</span><span class="sxs-lookup"><span data-stu-id="23ef4-534">In the current design, location directives aren't used when warehouse work is created.</span></span> <span data-ttu-id="23ef4-535">التالي ، يتم تطبيق اقل وحده في مجموعه تسلسل الوحدة (وحده المخزون) اثناء الخطوة كونتاينيريزيشن.</span><span class="sxs-lookup"><span data-stu-id="23ef4-535">Therefore, only the lowest unit in the unit sequence group (the inventory unit) is applied during the containerization wave step.</span></span>
