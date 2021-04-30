---
title: سياسة مرنة لحجز البعد على مستوى المستودع
description: يصف هذا الموضوع نهج حجز المخزون الذي يجب علي الشركات التي تقوم ببيع المنتجات التي تتبع المجموعات وتشغيل التجهيزات الخاصة به كعمليات ممكنة ل WMS-بحجز مجموعات محدده لأوامر توريد العميل ، حتى وان كان التدرج الهرمي للحجز الذي يتم المرتبطة بالمنتجات لا تسمح بحجز الدفعات الخاصة.
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReservationHierarchy, WHSWorkTrans, WHSWorkInventTrans, WHSInventTableReservationHierarchy, WHSReservationHierarchyCreate, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 13b81459fe3449a90839dac7637118f09afe2e55
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910223"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a><span data-ttu-id="9544d-103">سياسة مرنة لحجز البعد على مستوى المستودع</span><span class="sxs-lookup"><span data-stu-id="9544d-103">Flexible warehouse-level dimension reservation policy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9544d-104">عندما يكون التدرج الهرمي لحجز المخزون لنوع *الدفعة-أدناه\[الموقع\]* مقترنًا بالمنتجات والشركات التي تبيع منتجات تتبع الدُفعات وتدير لوجستياتها كعمليات يتم تمكينها لـ Microsoft Dynamics 365 لا يستطيع نظام إدارة المستودع (WMS) حجز دفعات محددة من هذه المنتجات لأوامر مبيعات العملاء.</span><span class="sxs-lookup"><span data-stu-id="9544d-104">When an inventory reservation hierarchy of the *Batch-below\[location\]* type is associated with products, businesses that sell batch-tracked products and run their logistics as operations that are enabled for the Microsoft Dynamics 365 Warehouse Management System (WMS) can't reserve specific batches of those products for customer sales orders.</span></span>

<span data-ttu-id="9544d-105">بطريقة مماثلة، لا يمكن حجز ألواح ترخيص محددة لمنتجات على أوامر المبيعات عندما تكون هذه المنتجات مرتبطة بالتدرج الهرمي الافتراضي للحجز.</span><span class="sxs-lookup"><span data-stu-id="9544d-105">In a similar way, specific license plates can't be reserved for products on sales orders when those products are associated with the default reservation hierarchy.</span></span>

<span data-ttu-id="9544d-106">يصف هذا الموضوع سياسة حجز المخزون الذي يتيح لهذه الأعمال حجز دُفعات أو لوحات ترخيص معينة، حتى عندما تكون المنتجات مقترنة بتدرج هرمي للحجز *الدفعة-أدناه\[الموقع\]*.</span><span class="sxs-lookup"><span data-stu-id="9544d-106">This topic describes the inventory reservation policy that lets these businesses reserve specific batches or license plates, even when the products are associated with a *Batch-below\[location\]* reservation hierarchy.</span></span>

## <a name="inventory-reservation-hierarchy"></a><span data-ttu-id="9544d-107">التدرجات الهرمية لحجز المخزون</span><span class="sxs-lookup"><span data-stu-id="9544d-107">Inventory reservation hierarchy</span></span>

<span data-ttu-id="9544d-108">يلخص هذا المقطع التدرج الهرمي لحجز المخزون الموجود.</span><span class="sxs-lookup"><span data-stu-id="9544d-108">This section summarizes the existing inventory reservation hierarchy.</span></span>

<span data-ttu-id="9544d-109">يفرض التسلسل الهرمي لحجز المخزون أنه، فيما يتعلق بأبعاد التخزين، يحمل أمر الطلب الأبعاد الإلزامية للموقع والمستودع وحالة المخزون.</span><span class="sxs-lookup"><span data-stu-id="9544d-109">The inventory reservation hierarchy dictates that, as far as storage dimensions are concerned, the demand order carries the mandatory dimensions of site, warehouse, and inventory status.</span></span> <span data-ttu-id="9544d-110">بمعنى آخر، الأبعاد الإلزامية هي جميع الأبعاد الموجودة فوق بُعد الموقع في التسلسل الهرمي للحجز، بينما يكون منطق المستودع مسؤولاً عن تعيين موقع للكميات المطلوبة وحجز الموقع.</span><span class="sxs-lookup"><span data-stu-id="9544d-110">In other words, the mandatory dimensions are all the dimensions above the location dimension in the reservation hierarchy, while the warehouse logic is responsible for assigning a location to the requested quantities and reserving the location.</span></span> <span data-ttu-id="9544d-111">في التفاعلات بين أمر الطلب وعمليات المستودع، من المتوقع أن يشير أمر الطلب إلى المكان الذي يجب أن يتم فيه شحن الأمر من (أي الموقع والمستودع).</span><span class="sxs-lookup"><span data-stu-id="9544d-111">In the interactions between the demand order and the warehouse operations, the demand order is expected to indicate where the order must be shipped from (that is, what site and warehouse).</span></span> <span data-ttu-id="9544d-112">وبعد ذلك يعتمد المستودع علي المنطق الخاص به للعثور علي الكمية المطلوبة في المستودع المحلي.</span><span class="sxs-lookup"><span data-stu-id="9544d-112">The warehouse then relies on its logic to find the required quantity in the warehouse premises.</span></span>

<span data-ttu-id="9544d-113">ومع ذلك ، لكي تعكس نموذج التشغيل الخاص بالاعمال ، يتم عرض ابعاد التعقب (المجموعة والأرقام المسلسلة) لمزيد من المرونة.</span><span class="sxs-lookup"><span data-stu-id="9544d-113">However, to reflect the operational model of the business, tracking dimensions (batch and serial numbers) are subject to more flexibility.</span></span> <span data-ttu-id="9544d-114">يمكن للتسلسل الهرمي لحجز المخزون استيعاب السيناريوهات التي تنطبق فيها الشروط التالية:</span><span class="sxs-lookup"><span data-stu-id="9544d-114">An inventory reservation hierarchy can accommodate scenarios where the following conditions apply:</span></span>

- <span data-ttu-id="9544d-115">يعتمد العمل علي عمليات المستودع الخاصة به لأداره انتقاء الكميات التي تحتوي علي المجموعة أو الأرقام المسلسلة *بعد* العثور علي الكميات في مساحة التخزين التي يتم تخزينها.</span><span class="sxs-lookup"><span data-stu-id="9544d-115">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers *after* the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="9544d-116">عاده ما يشار إلى هذا النموذج كـ *الدفعة-أدناه\[الموقع\]* أو *تسلسلي-أدناه\[الموقع\]*.</span><span class="sxs-lookup"><span data-stu-id="9544d-116">This model is often referred to as *Batch-below\[location\]* or *Serial-below\[location\]*.</span></span> <span data-ttu-id="9544d-117">ويستخدم عاده عندما لا يكون تعريف مجموعة المنتجات أو الرقم المسلسل مهما للعملاء الذين يقومون بتقديم الطلب مع الشركة الموردة.</span><span class="sxs-lookup"><span data-stu-id="9544d-117">It's typically used when a product's batch or serial number identification isn't important to the customers who place the demand with the selling company.</span></span>
- <span data-ttu-id="9544d-118">يعتمد العمل علي عمليات المستودع الخاصة به لأداره انتقاء الكميات التي تحتوي علي المجموعة أو الأرقام المسلسلة *قبل* العثور علي الكميات في مساحة التخزين التي يتم تخزينها.</span><span class="sxs-lookup"><span data-stu-id="9544d-118">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers *before* the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="9544d-119">إذا كانت أرقام الدُفعات أو الأرقام التسلسلية ضرورية كجزء من مواصفات أمر العميل، فسيتم تسجيلها في أمر الطلب، ولا يُسمح لعمليات المستودع التي تعثر على الكميات في المستودع بتغييرها.</span><span class="sxs-lookup"><span data-stu-id="9544d-119">If batch or serial numbers are necessary as part of a customer's order specification, they are recorded on the demand order, and the warehouse operations that find the quantities in the warehouse aren't allowed to change them.</span></span> <span data-ttu-id="9544d-120">يشار إلى هذا النموذج كـ *الدفعة-أعلاه\[الموقع\]* أو *تسلسلي-أعلاه\[الموقع\]*.</span><span class="sxs-lookup"><span data-stu-id="9544d-120">This model is referred to as *Batch-above\[location\]* or *Serial-above\[location\]*.</span></span> <span data-ttu-id="9544d-121">نظرًا لأن الأبعاد الموجودة أعلاه هي المتطلبات المحددة للطلبات التي يجب الوفاء بها، فلن يقوم منطق المستودع بتخصيصها.</span><span class="sxs-lookup"><span data-stu-id="9544d-121">Because the dimensions above location are the specific requirements for the demands that must be fulfilled, the warehouse logic won't allocate them.</span></span> <span data-ttu-id="9544d-122">**يجب** تحديد هذه الأبعاد دائمًا في أمر الطلب أو في الحجوزات ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="9544d-122">These dimensions **must** always be specified on the demand order or in the related reservations.</span></span>

<span data-ttu-id="9544d-123">في هذه السيناريوهات ، يكون التحدي هو انه يمكن تعيين تسلسل هرمي واحد فقط لحجز المخزون لكل منتج تم إصداره.</span><span class="sxs-lookup"><span data-stu-id="9544d-123">In these scenarios, the challenge is that only one inventory reservation hierarchy can be assigned to each released product.</span></span> <span data-ttu-id="9544d-124">التالي ، بالنسبة إلى WMS لمعالجة الأصناف المتتبعة، بعد أن يحدد تعيين التدرج الهرمي متى يتم حجز المجموعة أو الرقم المسلسل (أما عند أخذ أمر الطلب أو أثناء عمل الانتقاء الخاص بالمستودع)، لا يمكن تغيير هذا التوقيت على أساس المؤقت.</span><span class="sxs-lookup"><span data-stu-id="9544d-124">Therefore, for the WMS to handle tracked items, after the hierarchy assignment determines when the batch or serial number should be reserved (either when the demand order is taken or during the warehouse picking work), this timing can't be changed on an ad-hoc basis.</span></span>

## <a name="flexible-reservation-for-batch-tracked-items"></a><span data-ttu-id="9544d-125">حجز مرن للأصناف التي يتم تعقبها للدفعة</span><span class="sxs-lookup"><span data-stu-id="9544d-125">Flexible reservation for batch-tracked items</span></span>

### <a name="business-scenario"></a><span data-ttu-id="9544d-126">سيناريو الأعمال</span><span class="sxs-lookup"><span data-stu-id="9544d-126">Business scenario</span></span>

<span data-ttu-id="9544d-127">في هذا السيناريو، تستخدم إحدى الشركات استراتيجية مخزون حيث يتم تعقب البضائع المنتهية حسب أرقام المجموعات.</span><span class="sxs-lookup"><span data-stu-id="9544d-127">In this scenario, a company uses an inventory strategy where finished goods are tracked by batch numbers.</span></span> <span data-ttu-id="9544d-128">تستخدم هذه الشركة أيضا حمل العمل WMS.</span><span class="sxs-lookup"><span data-stu-id="9544d-128">This company also uses the WMS workload.</span></span> <span data-ttu-id="9544d-129">نظرا لأن حمل العمل هذا يستخدم منطق مجهز بشكل جيد لتخطيط عمليات الشحن والشحن وتشغيلها للأصناف التي تم تمكين المجموعة بها،يتم إقران معظم الأصناف المنتهية بالتسلسل الهرمي الخاص بحجز المخزون *الدفعة-أدناه\[الموقع\]*.</span><span class="sxs-lookup"><span data-stu-id="9544d-129">Because this workload has well-equipped logic for planning and running warehouse picking and shipping operations for batch-enabled items, most of the finished items are associated with a *Batch-below\[location\]* inventory reservation hierarchy.</span></span> <span data-ttu-id="9544d-130">تعد ميزة هذا النوع من الإعداد التشغيلي بأن القرارات (التي تعتبر قرارات حجز فاعلية) حول المجموعات التي سيتم انتقاؤها ومكان وضعها في المستودع يتم تأجيلها حتى تبدأ عمليات انتقاء المستودع.</span><span class="sxs-lookup"><span data-stu-id="9544d-130">The advantage of this type of operational setup is that decisions (which are effectively reservation decisions) about which batches to pick and where to put them in the warehouse are postponed until the warehouse picking operations start.</span></span> <span data-ttu-id="9544d-131">ولا يتم اجراؤها عند وضع أمر العميل.</span><span class="sxs-lookup"><span data-stu-id="9544d-131">They aren't made when the customer's order is placed.</span></span>

<span data-ttu-id="9544d-132">على الرغم من أن التدرج الهرمي لحجز *الدفعة-أدناه\[الموقع\]* يعمل بشكل جيد، يتطلب العديد من العملاء الذين تم تأسيسهم للشركة وجود نفس المجموعة التي تم شراؤها مسبقا عند قيامهم بإعادة ترتيب المنتجات.</span><span class="sxs-lookup"><span data-stu-id="9544d-132">Although the *Batch-below\[location\]* reservation hierarchy serves the company's business goals well, many of the company's established customers require the same batch that they previously purchased when they reorder products.</span></span> <span data-ttu-id="9544d-133">التالي، فإن الشركة تبحث عن مرونة في الطريقة التي تتم بها معالجة قواعد الحجز، وذلك وفقا لطلب العملاء لنفس الصنف، تحدث السلوكيات التالية:</span><span class="sxs-lookup"><span data-stu-id="9544d-133">Therefore, the company is looking for flexibility in the way that the batch reservation rules are handled, so that, depending on the customers' demand for the same item, the following behaviors occur:</span></span>

- <span data-ttu-id="9544d-134">يمكن تسجيل رقم المجموعة وحجزها عند أخذ الطلب بواسطة معالج المبيعات، ولا يمكن تغييره أثناء عمليات المستودع و/أو القيام بذلك من قبل طلبات أخرى.</span><span class="sxs-lookup"><span data-stu-id="9544d-134">A batch number can be recorded and reserved when the order is taken by the sales processor, and it can't be changed during warehouse operations and/or taken by other demands.</span></span> <span data-ttu-id="9544d-135">ويضمن هذا السلوك شحن رقم المجموعة التي تم طلبها إلى العميل.</span><span class="sxs-lookup"><span data-stu-id="9544d-135">This behavior helps guarantee that the batch number that was ordered is shipped to the customer.</span></span>
- <span data-ttu-id="9544d-136">إذا كان رقم المجموعة غير هام للعميل، يمكن أن تحدد عمليات المستودع رقم مجموعة أثناء العمل التصنيعي، بعد إجراء تسجيل أمر التوريد والحجز.</span><span class="sxs-lookup"><span data-stu-id="9544d-136">If the batch number isn't important to the customer, the warehouse operations can determine a batch number during picking work, after sales order registration and reservation have been done.</span></span>

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a><span data-ttu-id="9544d-137">السماح بحجز مجموعة محددة في أمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="9544d-137">Allowing reservation of a specific batch on the sales order</span></span>

<span data-ttu-id="9544d-138">لاستيعاب المرونة المطلوبة في سلوك حجز الدفعات للأصناف المقترنة بالتسلسل الهرمي لحجز المخزون *الدفعة-أدناه\[الموقع\]*، يجب على مديري المخزون تحديد خانة الاختيار **السماح بالحجز عند الطلب** لمستوى **رقم الدفعة** في صفحة **التدرجات الهرمية لحجز المخزون**.</span><span class="sxs-lookup"><span data-stu-id="9544d-138">To accommodate the desired flexibility in the batch reservation behavior for items that are associated with a *Batch-below\[location\]* inventory reservation hierarchy, inventory managers must select the **Allow reservation on demand order** check box for the **Batch number** level on the **Inventory reservation hierarchies** page.</span></span>

![صيانة جدول التدرج الهرمي لحجز المخزون](media/Flexible-inventory-reservation-hierarchy.png)

<span data-ttu-id="9544d-140">عند تحديد **مستوى رقم** المجموعة في التدرج الهرمي، يتم تحديد كافة الأبعاد الموجودة **أعلى** هذا المستوى والمستوى المحدد تلقائيا.</span><span class="sxs-lookup"><span data-stu-id="9544d-140">When the **Batch number** level in the hierarchy is selected, all dimensions above that level and up through the **Location** level will be automatically selected.</span></span> <span data-ttu-id="9544d-141">(بشكل افتراضي، يتم تحديد **كافة الأبعاد فوق مستوى الموقع** بشكل مسبق.) ويعكس هذا السلوك المنطق الذي يتم فيه أيضا حجز كافة الأبعاد الموجودة في النطاق بين رقم المجموعة والموقع تلقائيا بعد حجز رقم مجموعة محدد في بند الأمر.</span><span class="sxs-lookup"><span data-stu-id="9544d-141">(By default, all dimensions above the **Location** level are preselected.) This behavior reflects the logic where all dimensions in the range between the batch number and location are also automatically reserved after you reserve a specific batch number on the order line.</span></span>

> [!NOTE]
> <span data-ttu-id="9544d-142">يتم **تطبيق خانة الاختيار السماح بالحجز حسب طلب** الطلب فقط على مستويات التدرج الهرمي للحجز الموجودة أسفل بعد موقع المستودع.</span><span class="sxs-lookup"><span data-stu-id="9544d-142">The **Allow reservation on demand order** check box applies only to reservation hierarchy levels that are below the warehouse location dimension.</span></span>
>
> <span data-ttu-id="9544d-143">المستويان المفتوحان في التدرج الهرمي لسياسة الحجز المرن هما فقط **رقم الدُفعة** و **لوحة الترخيص**.</span><span class="sxs-lookup"><span data-stu-id="9544d-143">**Batch number** and **License plate** are the only levels in the hierarchy that are open for the flexible reservation policy.</span></span> <span data-ttu-id="9544d-144">بمعنى آخر ، لا يمكنك تحديد خانة الاختيار **السماح بالحجز حسب الطلب** **للموقع** أو **الرقم التسلسلي**.</span><span class="sxs-lookup"><span data-stu-id="9544d-144">In other words, you can't select the **Allow reservation on demand order** check box for the **Location** or **Serial number** level.</span></span>
>
> <span data-ttu-id="9544d-145">إذا تضمن التدرج الهرمي للحجز بُعد الرقم المسلسل (والذي يجب أن يكون أقل من مستوى **رقم الدفعة**) وإذا قمت بتشغيل الحجز الخاص بالدفعة لرقم الدُفعة، فسيستمر النظام في التعامل مع حجز الرقم التسلسلي وعمليات الانتقاء، بناءً على القواعد التي تنطبق على سياسة حجز *تسلسلي-أدناه\[الموقع\]*.</span><span class="sxs-lookup"><span data-stu-id="9544d-145">If your reservation hierarchy includes the serial number dimension (which must always be below the **Batch number** level), and if you've turned on batch-specific reservation for the batch number, the system will continue to handle serial number reservation and picking operations, based on the rules that apply to the *Serial-below\[location\]* reservation policy.</span></span>

<span data-ttu-id="9544d-146">في أي وقت، يمكنك السماح بالحجز الخاص بالدفعة لتدرج هرمي حجز *دفعة-أدناه\[الموقع\]* موجود في عملية التوزيع الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="9544d-146">At any point, you can allow batch-specific reservation for an existing *Batch-below\[location\]* reservation hierarchy in your deployment.</span></span> <span data-ttu-id="9544d-147">لن يؤثر هذا التغيير على أية عمليات حجز وعمل مستودع مفتوح تم إنشاؤه قبل حدوث التغيير.</span><span class="sxs-lookup"><span data-stu-id="9544d-147">This change won't affect any reservations and open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="9544d-148">ومع ذلك **، لا يمكن إلغاء تحديد** خانة الاختيار السماح بالحجز حسب أمر **الطلب** إذا **كانت** حركات **المخزون الخاصة بنوع المشكلة الفعلية المحجوزة أو المحجوزة أو المطلوبة** موجودة لصنف واحد أو أكثر من الأصناف المرتبطة بتسلسل الحجز هذا.</span><span class="sxs-lookup"><span data-stu-id="9544d-148">However, the **Allow reservation on demand order** check box can't be cleared if inventory transactions of the **Reserved ordered**, **Reserved physical**, or **Ordered** issue type exist for one or more items that are associated with that reservation hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="9544d-149">إذا لم يسمح التدرج الهرمي للحجز الموجود بالصنف بمواصفات التشغيلة في الأمر، فيمكنك إعادة تعيينه إلى تدرج الحجز الذي يسمح بمواصفات المجموعة، بشرط أن تكون بنية مستوى التدرج الهرمي هي نفسها في كلا التدرجات الهرمية.</span><span class="sxs-lookup"><span data-stu-id="9544d-149">If an item's existing reservation hierarchy doesn't allow batch specification on the order, you can reassign it to a reservation hierarchy that does allow batch specification, provided that the hierarchy level structure is the same in both hierarchies.</span></span> <span data-ttu-id="9544d-150">استخدم وظيفة **تغيير التدرج الهرمي** للحجز للأصناف لإجراء إعادة التعيين.</span><span class="sxs-lookup"><span data-stu-id="9544d-150">Use the **Change reservation hierarchy for items** function to do the reassignment.</span></span> <span data-ttu-id="9544d-151">قد يكون هذا التغيير متعلقا عندما ترغب في منع حجز المجموعات المرنة لمجموعة فرعية من الأصناف التي تتبع المجموعة ولكن مع السماح لها بالحفاظ علي بقية قائمة مشاريع المنتج.</span><span class="sxs-lookup"><span data-stu-id="9544d-151">This change might be relevant when you want to prevent flexible batch reservation for a subset of batch-tracked items but allow it for the rest of the product portfolio.</span></span>

<span data-ttu-id="9544d-152">بغض النظر عما إذا كنت قد قمت بتحديد خانة الاختيار **السماح بالحجز حسب أمر الطلب**، إذا كنت لا ترغب في حجز رقم دُفعة محدد للصنف في بند أمر، فإن منطق عمليات المستودع الافتراضي صالح لتدرج هرمي حجز *الدفعة-أدناه\[الموقع\]* سيظل صالحًا.</span><span class="sxs-lookup"><span data-stu-id="9544d-152">Regardless of whether you've selected the **Allow reservation on demand order** check box, if you don't want to reserve a specific batch number for the item on an order line, default warehouse operations logic that is valid for a *Batch-below\[location\]* reservation hierarchy will still apply.</span></span>

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a><span data-ttu-id="9544d-153">حجز رقم مجموعة محدد لأمر عميل</span><span class="sxs-lookup"><span data-stu-id="9544d-153">Reserve a specific batch number for a customer order</span></span>

<span data-ttu-id="9544d-154">بعد إعداد تدرج هرمي حجز مخزون *الدفعة-أدناه\[الموقع\]* لصنف تم تعقبه لدفعة للسماح بحجز أرقام دُفعات معينة في أوامر المبيعات، يمكن لمعالجات أوامر المبيعات أن تأخذ أوامر العميل لنفس الصنف بإحدى الطرق التالية، بناءً على طلب العميل:</span><span class="sxs-lookup"><span data-stu-id="9544d-154">After a batch-tracked item's *Batch-below\[location\]* inventory reservation hierarchy is set up to allow reservation of specific batch numbers on sales orders, sales order processors can take customer orders for the same item in one of the following ways, depending on the customer's request:</span></span>

- <span data-ttu-id="9544d-155">**ادخل تفاصيل الأمر بدون تحديد رقم** المجموعة - يجب استخدام هذه الطريقة عندما لا تكون مواصفات المجموعة الخاصة بالمنتج مهمة للعميل.</span><span class="sxs-lookup"><span data-stu-id="9544d-155">**Enter order details without specifying a batch number** – This approach should be used when the product's batch specification isn't important to the customer.</span></span> <span data-ttu-id="9544d-156">كافة العمليات الموجودة المقترنة بمعالجة أمر من هذا النوع يظل النظام بدون تغيير.</span><span class="sxs-lookup"><span data-stu-id="9544d-156">All existing processes that are associated with handling an order of this type in the system remain unchanged.</span></span> <span data-ttu-id="9544d-157">لا توجد اعتبارات إضافية مطلوبة في جزء المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="9544d-157">No additional considerations are required on the part of users.</span></span>
- <span data-ttu-id="9544d-158">**ادخل تفاصيل الأمر وقم بحجز رقم مجموعة معين** - يجب استخدام هذا الأسلوب عندما يطلب العميل مجموعة معينة.</span><span class="sxs-lookup"><span data-stu-id="9544d-158">**Enter order details and reserve a specific batch number** – This approach should be used when the customer requests a specific batch.</span></span> <span data-ttu-id="9544d-159">وعادة ما يقوم العملاء بطلب مجموعة محددة عند إعاده طلب المنتج الذي تم شراؤه سابقا.</span><span class="sxs-lookup"><span data-stu-id="9544d-159">Typically, customers will request a specific batch when they are reordering a product that they previously purchased.</span></span> <span data-ttu-id="9544d-160">ويشار إلى هذا النوع من الحجز الخاص بالدفعة *بالحجز المرتبط بالأمر*.</span><span class="sxs-lookup"><span data-stu-id="9544d-160">This type of batch-specific reservation is referred to as *order-committed reservation*.</span></span>

<span data-ttu-id="9544d-161">وتكون المجموعة التالية من القواعد صالحة عند معالجة الكميات، ويتم تخصيص رقم مجموعة لأمر محدد:</span><span class="sxs-lookup"><span data-stu-id="9544d-161">The following set of rules is valid when quantities are processed, and a batch number is committed to a specific order:</span></span>

- <span data-ttu-id="9544d-162">للسماح بحجز رقم مجموعة محدد لصنف ضمن سياسة الحجز *الدفعة-أدناه\[الموقع\]*، يجب على النظام حجز كل الأبعاد خلال الموقع.</span><span class="sxs-lookup"><span data-stu-id="9544d-162">To allow reservation of a specific batch number for an item under the *Batch-below\[location\]* reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="9544d-163">يتضمن هذا النطاق عادة بُعد لوح الترخيص.</span><span class="sxs-lookup"><span data-stu-id="9544d-163">This range typically includes the license plate dimension.</span></span>
- <span data-ttu-id="9544d-164">لا يتم استخدام توجيهات المواقع عند إنشاء انتقاء العمل لبند المبيعات الذي يستخدم حجز المجموعات المرتبطة بالأمر.</span><span class="sxs-lookup"><span data-stu-id="9544d-164">Location directives aren't used when picking work is created for a sales line that uses order-committed batch reservation.</span></span>
- <span data-ttu-id="9544d-165">وأثناء معالجة المستودع للعمل بالنسبة للدفعات المرتبطة بالأمر، لا يسمح للمستخدم أو النظام بتغيير رقم المجموعة.</span><span class="sxs-lookup"><span data-stu-id="9544d-165">During warehouse processing of work for order-committed batches, neither the user nor the system is allowed to change the batch number.</span></span> <span data-ttu-id="9544d-166">(تتضمن هذه المعالجة معالجة الاستثناء.)</span><span class="sxs-lookup"><span data-stu-id="9544d-166">(This processing includes exception handling.)</span></span>

<span data-ttu-id="9544d-167">يوضح المثال التالي تدفق نهاية إلى نهاية.</span><span class="sxs-lookup"><span data-stu-id="9544d-167">The following example shows the end-to-end flow.</span></span>

## <a name="example-scenario-batch-number-allocation"></a><span data-ttu-id="9544d-168">السيناريو المثال: تخصيص رقم الدُفعة</span><span class="sxs-lookup"><span data-stu-id="9544d-168">Example scenario: Batch number allocation</span></span>

<span data-ttu-id="9544d-169">بالنسبة إلى هذا العرض التوضيحي، يجب تثبيت بيانات العرض التوضيحي، ويجب استخدام شركة بيانات العرض التوضيحي **USMF‎**.</span><span class="sxs-lookup"><span data-stu-id="9544d-169">For this example, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><a name="Example-batch-allocation"></a><span data-ttu-id="9544d-170">إعداد تدرج هرمي لحجز مخزون للسماح بحجز خاص بمجموعة</span><span class="sxs-lookup"><span data-stu-id="9544d-170">Set up an inventory reservation hierarchy to allow batch-specific reservation</span></span>

1. <span data-ttu-id="9544d-171">الانتقال إلى **إدارة المخزون** \> **إعداد** \> **المخزون \> ‏‫التدرج الهرمي للحجز‬**.</span><span class="sxs-lookup"><span data-stu-id="9544d-171">Go to **Warehouse management** \> **Setup** \> **Inventory \> Reservation hierarchy**.</span></span>
2. <span data-ttu-id="9544d-172">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="9544d-172">Select **New**.</span></span>
3. <span data-ttu-id="9544d-173">في حقل **الاسم** أدخل اسمًا (على سبيل المثال، **BatchFlex**).</span><span class="sxs-lookup"><span data-stu-id="9544d-173">In the **Name** field, enter a name (for example, **BatchFlex**).</span></span>
4. <span data-ttu-id="9544d-174">في الحقل **الوصف**، ادخل وصفا (على سبيل المثال، **المجموعة الموجودة أسفل المرونة**).</span><span class="sxs-lookup"><span data-stu-id="9544d-174">In the **Description** field, enter a description (for example, **Batch below flexible**).</span></span>
5. <span data-ttu-id="9544d-175">في الحقل **المحدد**، حدد **الرقم المسلسل** و **المالك**، ثم حدد زر السهم الأيسر لنقلهم إلى الحقل **المتوفر**.</span><span class="sxs-lookup"><span data-stu-id="9544d-175">In the **Selected** field, select **Serial number** and **Owner**, and then select the left arrow button to move them to the **Available** field.</span></span>
6. <span data-ttu-id="9544d-176">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="9544d-176">Select **OK**.</span></span>
7. <span data-ttu-id="9544d-177">في الصف الخاص بمستوى بعد **رقم المجموعة**، حدد خانة الاختيار **السماح بالحجز عند الطلب**.</span><span class="sxs-lookup"><span data-stu-id="9544d-177">In the row for the **Batch number** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="9544d-178">يتم تحديد **لوحة الترخيص** ومستويات **الموقع** تلقائيا، ولا يمكنك إلغاء تحديد خانات الاختيار الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="9544d-178">The **License plate** and **Location** levels are automatically selected, and you can't clear the check boxes for them.</span></span>
8. <span data-ttu-id="9544d-179">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="9544d-179">Select **Save**.</span></span>

### <a name="create-a-new-released-product"></a><span data-ttu-id="9544d-180">إنشاء منتج جديد صادر</span><span class="sxs-lookup"><span data-stu-id="9544d-180">Create a new released product</span></span>

1. <span data-ttu-id="9544d-181">قم بتعيين معلمات البيانات الرئيسية الثلاثة الخاصة بالمنتج باستخدام هذه القيم:</span><span class="sxs-lookup"><span data-stu-id="9544d-181">Set the product's three master data parameters by using these values:</span></span>

    - <span data-ttu-id="9544d-182">وفي الحقل **مجموعة أبعاد التخزين**، حدد **مستودع**.</span><span class="sxs-lookup"><span data-stu-id="9544d-182">In the **Storage dimension group** field, select **Ware**.</span></span>
    - <span data-ttu-id="9544d-183">في الحقل **تتبع مجموعة الأبعاد**، حدد **الدفعة المادية**.</span><span class="sxs-lookup"><span data-stu-id="9544d-183">In the **Tracking dimension group** field, select **Batch-Phy**.</span></span>
    - <span data-ttu-id="9544d-184">في حقل **تدرج الحجز**، حدد **BatchFlex**.</span><span class="sxs-lookup"><span data-stu-id="9544d-184">In the **Reservation hierarchy** field, select **BatchFlex**.</span></span>

2. <span data-ttu-id="9544d-185">قم بإنشاء رقمين للمجموعة مثل **B11** و **B22**.</span><span class="sxs-lookup"><span data-stu-id="9544d-185">Create two batch numbers, such as **B11** and **B22**.</span></span>
3. <span data-ttu-id="9544d-186">أضافه كميات الأصناف إلى المخزون الفعلي من خلال استخدام القيم التالية.</span><span class="sxs-lookup"><span data-stu-id="9544d-186">Add item quantities to on-hand stock by using the following values.</span></span>

    | <span data-ttu-id="9544d-187">المستودع</span><span class="sxs-lookup"><span data-stu-id="9544d-187">Warehouse</span></span> | <span data-ttu-id="9544d-188">رقم الدُفعة</span><span class="sxs-lookup"><span data-stu-id="9544d-188">Batch number</span></span> | <span data-ttu-id="9544d-189">الموقع</span><span class="sxs-lookup"><span data-stu-id="9544d-189">Location</span></span> | <span data-ttu-id="9544d-190">لوحة الترخيص</span><span class="sxs-lookup"><span data-stu-id="9544d-190">License plate</span></span> | <span data-ttu-id="9544d-191">الكمية</span><span class="sxs-lookup"><span data-stu-id="9544d-191">Quantity</span></span> |
    |-----------|--------------|----------|---------------|----------|
    | <span data-ttu-id="9544d-192">24</span><span class="sxs-lookup"><span data-stu-id="9544d-192">24</span></span>        | <span data-ttu-id="9544d-193">B11</span><span class="sxs-lookup"><span data-stu-id="9544d-193">B11</span></span>          | <span data-ttu-id="9544d-194">BULK-001</span><span class="sxs-lookup"><span data-stu-id="9544d-194">BULK-001</span></span> | <span data-ttu-id="9544d-195">لا‬‬ شيء</span><span class="sxs-lookup"><span data-stu-id="9544d-195">None</span></span>          | <span data-ttu-id="9544d-196">10</span><span class="sxs-lookup"><span data-stu-id="9544d-196">10</span></span>       |
    | <span data-ttu-id="9544d-197">24</span><span class="sxs-lookup"><span data-stu-id="9544d-197">24</span></span>        | <span data-ttu-id="9544d-198">B11</span><span class="sxs-lookup"><span data-stu-id="9544d-198">B11</span></span>          | <span data-ttu-id="9544d-199">FL-001</span><span class="sxs-lookup"><span data-stu-id="9544d-199">FL-001</span></span>   | <span data-ttu-id="9544d-200">LP11</span><span class="sxs-lookup"><span data-stu-id="9544d-200">LP11</span></span>          | <span data-ttu-id="9544d-201">10</span><span class="sxs-lookup"><span data-stu-id="9544d-201">10</span></span>       |
    | <span data-ttu-id="9544d-202">24</span><span class="sxs-lookup"><span data-stu-id="9544d-202">24</span></span>        | <span data-ttu-id="9544d-203">B22</span><span class="sxs-lookup"><span data-stu-id="9544d-203">B22</span></span>          | <span data-ttu-id="9544d-204">FL-002</span><span class="sxs-lookup"><span data-stu-id="9544d-204">FL-002</span></span>   | <span data-ttu-id="9544d-205">LP22</span><span class="sxs-lookup"><span data-stu-id="9544d-205">LP22</span></span>          | <span data-ttu-id="9544d-206">10</span><span class="sxs-lookup"><span data-stu-id="9544d-206">10</span></span>       |

### <a name="enter-sales-order-details"></a><a name="sales-order-details"></a><span data-ttu-id="9544d-207">إدخال تفاصيل أمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="9544d-207">Enter sales order details</span></span>

1. <span data-ttu-id="9544d-208">انتقل إلى **المبيعات والتسويق** \> **أوامر المبيعات** \> **كافة أوامر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="9544d-208">Go to **Sales and marketing** \> **Sales orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="9544d-209">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="9544d-209">Select **New**.</span></span>
3. <span data-ttu-id="9544d-210">في البيانات الرئيسية لأمر التوريد ، في الحقل **حساب العميل**، أدخل **US-003**.</span><span class="sxs-lookup"><span data-stu-id="9544d-210">On the sales order header, in the **Customer account** field, enter **US-003**.</span></span>
4. <span data-ttu-id="9544d-211">أضف سطرًا لمنتج مُنتهِ، وادخل **10** ككمية.</span><span class="sxs-lookup"><span data-stu-id="9544d-211">Add a line for the new item, and enter **10** as the quantity.</span></span> <span data-ttu-id="9544d-212">تأكد من تعيين الحقل **الكمية** على **24**.</span><span class="sxs-lookup"><span data-stu-id="9544d-212">Make sure that the **Warehouse** field is set to **24**.</span></span>
5. <span data-ttu-id="9544d-213">في علامة التبويب السريعة **بنود أمر التوريد**، حدد **المخزون**، ثم في المجموعة **الصيانة**، حدد **حجز المجموعة**.</span><span class="sxs-lookup"><span data-stu-id="9544d-213">On the **Sales order lines** FastTab, select **Inventory**, and then, in the **Maintain** group, select **Batch reservation**.</span></span> <span data-ttu-id="9544d-214">تقوم **صفحه حجز** المجموعات بعرض قائمة بالمجموعات المتوفرة للحجز الخاص ببند الأمر.</span><span class="sxs-lookup"><span data-stu-id="9544d-214">The **Batch reservation** page shows a list of batches that are available for reservation for the order line.</span></span> <span data-ttu-id="9544d-215">بالنسبة لهذا المثال، فإنه يعرض كمية بمقدار **20** لرقم المجموعة **B11** وكمية **10** لرقم المجموعة **B22** .</span><span class="sxs-lookup"><span data-stu-id="9544d-215">For this example, it shows a quantity of **20** for batch number **B11** and a quantity of **10** for batch number **B22**.</span></span> <span data-ttu-id="9544d-216">لاحظ أنه لا يمكن الوصول إلى صفحة **حجز الدفعة** من بند إذا كان الصنف الموجود في هذا البند مقترنا بحجز التدرج الهرمي *الدفعة-أدناه\[الموقع\]* ما لم يتم إعداده للسماح بالحجز الخاص بالدفعة.</span><span class="sxs-lookup"><span data-stu-id="9544d-216">Note that the **Batch reservation** page cannot be accessed from a line if the item on that line is associated with *Batch-below\[location\]* reservation hierarchy unless it is set up to allow batch-specific reservation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9544d-217">لحجز مجموعة محددة لأمر توريد، يجب استخدام الصفحة **حجز المجموعة**.</span><span class="sxs-lookup"><span data-stu-id="9544d-217">To reserve a specific batch for a sales order, you must use the **Batch reservation** page.</span></span>
    >
    > <span data-ttu-id="9544d-218">إذا أدخلت رقم الدُفعة مباشرةً في بند أمر المبيعات، فسيعمل النظام كما لو أنك أدخلت قيمة دُفعة معينة لبند خاضع لسياسة حجز *الدفعة-أدناه\[الموقع\]*.</span><span class="sxs-lookup"><span data-stu-id="9544d-218">If you enter the batch number directly on the sales order line, the system will behave as though you entered a specific batch value for an item that is subject to the *Batch-below\[location\]* reservation policy.</span></span> <span data-ttu-id="9544d-219">عند حفظ البند، ستتلقى رسالة تحذير.</span><span class="sxs-lookup"><span data-stu-id="9544d-219">When you save the line, you will receive a warning message.</span></span> <span data-ttu-id="9544d-220">إذا قمت بالتاكيد علي انه يجب تحديد رقم المجموعة مباشره علي سطر الأمر، فلن تتم معالجه البند بواسطة منطق إدارة المستودع العادي.</span><span class="sxs-lookup"><span data-stu-id="9544d-220">If you confirm that the batch number should be specified directly on the order line, the line won't be handled by the regular warehouse management logic.</span></span>
    >
    > <span data-ttu-id="9544d-221">إذا قمت بحجز الكمية من صفحة **الحجز**، لن يتم حجز أي دُفعة محددة، وسيتبع تنفيذ عمليات المستودعات للبند القواعد المطبقة بموجب سياسة حجز *الدفعة-أدناه\[الموقع\]*.</span><span class="sxs-lookup"><span data-stu-id="9544d-221">If you reserve the quantity from the **Reservation** page, no specific batch will be reserved, and the execution of warehouse operations for the line will follow the rules that are applicable under the *Batch-below\[location\]* reservation policy.</span></span>

    <span data-ttu-id="9544d-222">بشكل عام، تعمل هذه الصفحة ويتم التفاعل معها بنفس الطريقة للعناصر التي لها تدرج هرمي للحجز مرتبط بالنوع *الدفعة-أعلاه\[الموقع\]*.</span><span class="sxs-lookup"><span data-stu-id="9544d-222">In general, this page works and is interacted with in the same way for items that have an associated reservation hierarchy of the *Batch-above\[location\]* type.</span></span> <span data-ttu-id="9544d-223">ومع ذلك، يتم تطبيق الاستثناءات التالية:</span><span class="sxs-lookup"><span data-stu-id="9544d-223">However, the following exceptions apply:</span></span>

    - <span data-ttu-id="9544d-224">تعرض علامة التبويب السريعة **أرقام المجموعات التي تم تنفيذها لبند المصدر** أرقام المجموعات التي تم حجزها لبند الأمر.</span><span class="sxs-lookup"><span data-stu-id="9544d-224">The **Batch numbers committed to source line** FastTab shows the batch numbers that are reserved for the order line.</span></span> <span data-ttu-id="9544d-225">ستظهر قيم المجموعات في الشبكة خلال دورة الاستيفاء لسطر الأمر، بما في ذلك مراحل معالجة المستودع.</span><span class="sxs-lookup"><span data-stu-id="9544d-225">The batch values in the grid will be shown throughout the fulfillment cycle of the order line, including the warehouse processing stages.</span></span> <span data-ttu-id="9544d-226">وعلي النقيض، في علامة التبويب السريعة **النظرة العامة**، يتم عرض حجز بند الأمر العادي (أي ، الحجز الذي يتم إنجازه للابعاد الموجودة اعلي مستوي **الموقع**) في الشبكة حتى النقطة التي يتم فيها إنشاء عمل المستودع.</span><span class="sxs-lookup"><span data-stu-id="9544d-226">By contrast, on the **Overview** FastTab, regular order line reservation (that is, reservation that is done for the dimensions above the **Location** level) is shown in the grid up to the point when warehouse work is created.</span></span> <span data-ttu-id="9544d-227">ثم يقوم كيان العمل بعد ذلك بالحفاظ علي حجز البند ، ولا يظهر حجز البند بعد ذلك في الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9544d-227">The work entity then takes over the line reservation, and the line reservation no longer appears on the page.</span></span> <span data-ttu-id="9544d-228">تساعد علامة التبويب السريعة **أرقام المجموعات التي تم تنفيذها علي بند المصدر** على التأكد من أن معالج أمر التوريد يمكنه عرض أرقام المجموعات التي تم تنفيذها لأمر العميل في أي مرحلة أثناء الفوترة.</span><span class="sxs-lookup"><span data-stu-id="9544d-228">The **Batch numbers committed to source line** FastTab helps guarantee that the sales order processor can view the batch numbers that were committed to the customer's order at any point during its lifecycle, up through invoicing.</span></span>
    - <span data-ttu-id="9544d-229">بالإضافة إلى القيام بحجز مجموعة محدده، يمكن للمستخدم تحديد الموقع الخاص بالمجموعة ولوحه الترخيص يدويا بدلا من السماح للنظام بتحديدها تلقائيا.</span><span class="sxs-lookup"><span data-stu-id="9544d-229">In addition to reserving a specific batch, a user can manually select the batch's specific location and license plate instead of letting the system automatically select them.</span></span> <span data-ttu-id="9544d-230">ترتبط هذه الامكانيه بتصميم آلية حجز المجموعة الملتزم بها الأمر.</span><span class="sxs-lookup"><span data-stu-id="9544d-230">This capability is related to the design of the order-committed batch reservation mechanism.</span></span> <span data-ttu-id="9544d-231">كما ذكرنا سابقًا، عندما يكون رقم الدُفعة محجوزًا لصنف ضمن سياسة حجز *الدفعة-أدناه\[الموقع\]*، يجب أن يحتفظ النظام بجميع الأبعاد خلال الموقع.</span><span class="sxs-lookup"><span data-stu-id="9544d-231">As was mentioned earlier, when a batch number is reserved for an item under the *Batch-below\[location\]* reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="9544d-232">التالي، سيحمل عمل المستودع نفس أبعاد التخزين التي تم حجزها بواسطة المستخدمين الذين قاموا بالعمل مع الأوامر، وقد لا يمثلون دائما موضع تخزين الأصناف الملائم ، أو حتى الممكن ، لعمليات الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="9544d-232">Therefore, warehouse work will carry the same storage dimensions that were reserved by the users who worked with the orders, and it might not always represent the item storage placement that is convenient, or even possible, for picking operations.</span></span> <span data-ttu-id="9544d-233">إذا كانت معالجه الأمر علي علم بقيود المستودع ، فقد يرغبون في تحديد المواقع المحددة ولوحات الترخيص يدويا عند حجزها لأحدي المجموعات.</span><span class="sxs-lookup"><span data-stu-id="9544d-233">If order processors are aware of the warehouse constraints, they might want to manually select the specific locations and license plates when they reserve a batch.</span></span> <span data-ttu-id="9544d-234">في هذه الحالة ، يجب أن يستخدم المستخدم وظيفة **ابعاد العرض** في راس الصفحة ، ويجب أن يضيف لوحه الموقع والترخيص الشبكة في على علامة التبويب السريعة **النظرة العامة**.</span><span class="sxs-lookup"><span data-stu-id="9544d-234">In this case, the user must use the **Display dimensions** functionality on the page header, and must add the location and license plate in the grid on the **Overview** FastTab.</span></span>

6. <span data-ttu-id="9544d-235">في الصفحة **حجز المجموعة**، حدد بندا لمجموعة **B11**، ثم حدد **حجز البند**.</span><span class="sxs-lookup"><span data-stu-id="9544d-235">On the **Batch reservation** page, select the line for batch **B11**, and then select **Reserve line**.</span></span> <span data-ttu-id="9544d-236">لا يوجد منطق مخصص لتعيين المواقع ولوحات الترخيص اثناء الحجز التلقائي.</span><span class="sxs-lookup"><span data-stu-id="9544d-236">There is no designated logic for assigning locations and license plates during automatic reservation.</span></span> <span data-ttu-id="9544d-237">يمكنك إدخال الكمية يدويا في حقل **الحجز**.</span><span class="sxs-lookup"><span data-stu-id="9544d-237">You can manually enter the quantity in the **Reservation** field.</span></span> <span data-ttu-id="9544d-238">لاحظ انه يتم في علامة التبويب السريعة **الأرقام الدفعيه التي تم تنفيذها لبند المصدر** عرض مجموعة **B11** بالحالة **منفذ.**</span><span class="sxs-lookup"><span data-stu-id="9544d-238">Notice that, on the **Batch numbers committed to source line** FastTab, batch **B11** is shown as **Committed**.</span></span>

    ![تنفيذ رقم دفعه معين لبند أمر التوريد في صفحه حجز الدفعات](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > <span data-ttu-id="9544d-240">يمكن القيام بحجز الكمية في بند أمر التوريد عبر مجموعات متعددة.</span><span class="sxs-lookup"><span data-stu-id="9544d-240">Reservation of the quantity on a sales order line can be done across multiple batches.</span></span> <span data-ttu-id="9544d-241">المثل ، يمكن القيام بحجز نفس الدفعة مقابل المواقع المتعددة ولوحات الترخيص (في حالة تمكين لوحات الترخيص للمواقع).</span><span class="sxs-lookup"><span data-stu-id="9544d-241">Likewise, reservation of the same batch can be done against multiple locations and license plates (if license plates are enabled for the locations).</span></span>
    >
    > <span data-ttu-id="9544d-242">يمكن أيضا أن يكون حجز مجموعة محدده للكمية في بند أمر التوريد جزئيا.</span><span class="sxs-lookup"><span data-stu-id="9544d-242">Reservation of a specific batch for the quantity on a sales order line can also be partial.</span></span> <span data-ttu-id="9544d-243">على سبيل المثال ، يمكن حجز إجمالي الكمية 100 من الوحدات بحيث يتم التزام بمجموعة معينه إلى 20 وحده ، بينما يتم حجز 80 وحده في مستويات الموقع والمستودع لآيه مجموعة متاحه.</span><span class="sxs-lookup"><span data-stu-id="9544d-243">For example, the total quantity of 100 units can be reserved so that a specific batch is committed to 20 units, whereas 80 units are reserved at the site and warehouse levels for any available batch.</span></span> <span data-ttu-id="9544d-244">في هذه الحالة ، سيقوم WMS بمعالجه عمليات الانتقاء باستخدام بندين منفصلين من أسطر العمل.</span><span class="sxs-lookup"><span data-stu-id="9544d-244">In this case, the WMS will handle picking operations by using two separate work lines.</span></span>

7. <span data-ttu-id="9544d-245">انتقل إلى **إدارة معلومات المنتج** \> **المنتجات** \> **المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="9544d-245">Go to **Product information management** \> **Products** \> **Released products**.</span></span> <span data-ttu-id="9544d-246">حدد الصنف، ثم حدد **إدارة المخزون**\>**عرض**\>**الحركات**.</span><span class="sxs-lookup"><span data-stu-id="9544d-246">Select your item, and then select **Manage inventory** \> **View** \> **Transactions**.</span></span>

    ![الحجز المرتبط بالأمر كنوع حركه مخزون](media/Inventory-transactions-for-order-committed-reservation.png)

8. <span data-ttu-id="9544d-248">مراجعه حركات المخزون الخاصة بالصنف والمرتبطة بحجز بند أمر التوريد.</span><span class="sxs-lookup"><span data-stu-id="9544d-248">Review the item's inventory transactions that are related to the sales order line reservation.</span></span>

    - <span data-ttu-id="9544d-249">حركه يتم تعيين الحقل **المرجع** بها إلى **أمر المبيعات** ويتم تعيين حقل **الإصدار** على القيمة **الفعلية المحجوزة** تمثل حجز بند الأمر لابعاد المخزون فوق مستوى **الموقع**.</span><span class="sxs-lookup"><span data-stu-id="9544d-249">A transaction where the **Reference** field is set to **Sales order** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the inventory dimensions above the **Location** level.</span></span> <span data-ttu-id="9544d-250">ووفقا للتسلسل الهرمي لحجز مخزون الصنف ، فان هذه الابعاد هي الموقع والمستودع وحالة المخزون.</span><span class="sxs-lookup"><span data-stu-id="9544d-250">According to the item's inventory reservation hierarchy, those dimensions are site, warehouse, and inventory status.</span></span>
    - <span data-ttu-id="9544d-251">حركه يتم تعيين الحقل **المرجع** بها إلى **الحجز بواسطة الأمر** ويتم تعيين حقل **الإصدار** على القيمة **الفعلية المحجوزة** تمثل حجز بند الأمر لدفعة معينة وجميع أبعاد المخزون فوقها.</span><span class="sxs-lookup"><span data-stu-id="9544d-251">A transaction where the **Reference** field is set to **Order-committed reservation** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the specific batch and all inventory dimensions above it.</span></span> <span data-ttu-id="9544d-252">ووفقا للتسلسل الهرمي لحجز مخزون الصنف، فان هذه الابعاد هي الموقع ورقم الدفعة.</span><span class="sxs-lookup"><span data-stu-id="9544d-252">According to the item's inventory reservation hierarchy, those dimensions are batch number and location.</span></span> <span data-ttu-id="9544d-253">في هذا المثال، يكون **Bulk-001.**</span><span class="sxs-lookup"><span data-stu-id="9544d-253">In this example, the location is **Bulk-001**.</span></span>

9. <span data-ttu-id="9544d-254">في رأس أمر المبيعات، حدد **المستودع** \> **الإجراءات‏‎** \> **إصدار إلى المستودع**.</span><span class="sxs-lookup"><span data-stu-id="9544d-254">On the sales order header, select **Warehouse** \> **Actions** \> **Release to warehouse**.</span></span> <span data-ttu-id="9544d-255">يتم الآن إرسال بند الأمر، ويتم إنشاء تحميل وعمل.</span><span class="sxs-lookup"><span data-stu-id="9544d-255">The order line is now waved, and a load and work are created.</span></span>

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="9544d-256">مراجعه عمل المستودع الذي يحتوي على أرقام الدفعات المخصصة للأمر ومعالجتها</span><span class="sxs-lookup"><span data-stu-id="9544d-256">Review and process warehouse work that has order-committed batch numbers</span></span>

1. <span data-ttu-id="9544d-257">في علامة التبويب السريعة **بنود أمر المبيعات**، حدد **المستودع**\>**تفاصيل العمل**.</span><span class="sxs-lookup"><span data-stu-id="9544d-257">On the **Sales order lines** FastTab, select **Warehouse** \> **Work details**.</span></span>

    <span data-ttu-id="9544d-258">يحتوي العمل الذي يقوم بمعالجه عمليه الانتقاء لكميات الدفعة التي يتم تنفيذها علي بند أمر التوريد علي الخصائص التالية:</span><span class="sxs-lookup"><span data-stu-id="9544d-258">The work that handles the picking operation for batch quantities that are committed to the sales order line has the following characteristics:</span></span>

    - <span data-ttu-id="9544d-259">لإنشاء العمل ، يستخدم النظام قوالب العمل وليس توجيهات المواقع.</span><span class="sxs-lookup"><span data-stu-id="9544d-259">To create work, the system uses work templates but not location directives.</span></span> <span data-ttu-id="9544d-260">سيتم تطبيق كافة الإعدادات القياسية التي تم تحديدها لقوالب العمل ، مثل العدد الأقصى لبنود الانتقاء أو وحده قياس معينه ، لتحديد الوقت الذي ينبغي فيه إنشاء عمل جديد.</span><span class="sxs-lookup"><span data-stu-id="9544d-260">All the standard settings that are defined for work templates, such as a maximum number of pick lines or a specific unit of measure, will be applied to determine when new work should be created.</span></span> <span data-ttu-id="9544d-261">ومع ذلك ، لا يتم التعامل مع القواعد المقترنة بتوجيهات المواقع لتعريف مواقع الانتقاء ، نظرا لان الحجز المرتبط بالأمر يحدد بالفعل كافة ابعاد المخزون.</span><span class="sxs-lookup"><span data-stu-id="9544d-261">However, the rules that are associated with location directives for identifying pick locations aren't considered, because the order-committed reservation already specifies all the inventory dimensions.</span></span> <span data-ttu-id="9544d-262">وتتضمن ابعاد المخزون هذه الابعاد علي مستوي تخزين المستودع.</span><span class="sxs-lookup"><span data-stu-id="9544d-262">Those inventory dimensions include the dimensions at the warehouse storage level.</span></span> <span data-ttu-id="9544d-263">التالي ، يرث العمل تلك الابعاد دون الحاجة إلى استشاره توجيهات المواقع.</span><span class="sxs-lookup"><span data-stu-id="9544d-263">Therefore, the work inherits those dimensions without having to consult location directives.</span></span>
    - <span data-ttu-id="9544d-264">لا يتم إظهار رقم المجموعة في بند الانتقاء (كما هو الحال بالنسبة لبند العمل الذي تم إنشاؤه للصنف الذي يشتمل على تسلسل الحجز *الدفعة-أعلى\[الموقع\]*). بدلا من ذلك، يتم عرض رقم المجموعة "من" وكافة ابعاد التخزين الأخرى في حركه مخزون العمل الخاصة ببند العمل المشار اليها من حركات المخزون المرتبطة.</span><span class="sxs-lookup"><span data-stu-id="9544d-264">The batch number isn't shown on the pick line (as is the case for the work line that is created for an item that has an associated *Batch-above\[location\]* reservation hierarchy.) Instead, the "from" batch number and all other storage dimensions are shown on the work line's work inventory transaction that is referenced from the associated inventory transactions.</span></span>

        ![حركه مخزون المستودع للعمل الذي ينتج عن الحجز المرتبط بالطلبات](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - <span data-ttu-id="9544d-266">بعد إنشاء العمل، تتم إزالة حركة المخزون الخاصة بالصنف التي تم تعيين حقل **المرجع** فيها إلى **الحجز المرتبط بالأمر**.</span><span class="sxs-lookup"><span data-stu-id="9544d-266">After work is created, the item's inventory transaction where the **Reference** field is set to **Order-committed reservation** is removed.</span></span> <span data-ttu-id="9544d-267">حركة المخزون التي تم تعيين الحقل **المرجع** بها على **عمل** تحتفظ الآن بالحجز الفعلي علي كافة ابعاد المخزون الخاصة بالكمية.</span><span class="sxs-lookup"><span data-stu-id="9544d-267">The inventory transaction where the **Reference** field is set to **Work** now holds the physical reservation on all the quantity's inventory dimensions.</span></span>

        <span data-ttu-id="9544d-268">يمكن أن تتابع عمليات المستودع معالجه تنفيذ العمل بالطريقة المعتادة.</span><span class="sxs-lookup"><span data-stu-id="9544d-268">Warehouse operations can proceed to handle execution of the work in the usual manner.</span></span> <span data-ttu-id="9544d-269">ومع ذلك، ستقوم الإرشادات الموجودة علي الجهاز المحمول بإرشاد العامل لانتقاء رقم مجموعة معين.</span><span class="sxs-lookup"><span data-stu-id="9544d-269">However, the instructions on the mobile device will instruct the worker to pick a specific batch number.</span></span> <span data-ttu-id="9544d-270">في بيئات المستودعات حيث تكون المواقع عبارة عن لوحه ترخيص – يتم التحكم بها ، بعد وصول أحد العاملين إلى موقع يقوم بتخزين نفس المجموعة علي ألواح ترخيص متعددة ، فانه يمكنه الانتقاء من اي لوحه ترخيص غير محجوزه بالفعل (على سبيل المثال ، بواسطة آخر الحجز أو الاعمال المرتبطة بالطلبات التي تنشا من حجز من هذا النوع.)</span><span class="sxs-lookup"><span data-stu-id="9544d-270">In warehouse environments where locations are license plate–controlled, after a worker reaches a location that stores the same batch on multiple license plates, he or she can pick from any license plate that isn't already reserved (for example, by another order-committed reservation or work that originates from a reservation of that type.)</span></span>

        <span data-ttu-id="9544d-271">وفي حالة تشغيله للانتقاء من الموقع المحدد في بند العمل ، يمكن لمشغلي المستودع استخدام أحد الإجراءات التالية لأعاده توجيه انتقاء المجموعة المحددة من موقع أكثر ملاءمة:</span><span class="sxs-lookup"><span data-stu-id="9544d-271">If it turns out to be impractical to pick from the location that is specified on the work line, the warehouse operators can use one of the following actions to redirect picking of the specific batch from a more convenient location:</span></span>

        - <span data-ttu-id="9544d-272">إجراء **تجاوز الموقع** القياسي علي جهاز محمول (شريطة تمكين الإعداد الخاص بالعامل الخاص بالمستودع **السماح بتجاوز موقع الالتقاط**)</span><span class="sxs-lookup"><span data-stu-id="9544d-272">The standard **Override location** action on a mobile device (provided that the warehouse worker's **Allow pick location override** setting is enabled)</span></span>
        - <span data-ttu-id="9544d-273">إجراء **تغيير الموقع** في الصفحة **تفاصيل قائمة العمل**.</span><span class="sxs-lookup"><span data-stu-id="9544d-273">The **Change location** action on the **Work list details** page.</span></span> 

2. <span data-ttu-id="9544d-274">علي الجهاز المحمول ، قم بإنهاء الانتقاء ووضع العمل.</span><span class="sxs-lookup"><span data-stu-id="9544d-274">On the mobile device, finish picking and putting the work.</span></span>

    <span data-ttu-id="9544d-275">يتم الآن انتقاء الكمية **10** لرقم الدفعة **B11** لبند أمر المبيعات ووضعها في موقع **باب تحميل البضائع**.</span><span class="sxs-lookup"><span data-stu-id="9544d-275">The quantity of **10** for batch number **B11** is now picked for the sales order line and put in the **Baydoor** location.</span></span> <span data-ttu-id="9544d-276">في هذه المرحلة، يكون جاهزا ليتم تحميله علي الشاحنة وإرساله إلى عنوان العميل.</span><span class="sxs-lookup"><span data-stu-id="9544d-276">At this point, it's ready to be loaded onto the truck and dispatched to the customer's address.</span></span>

## <a name="flexible-license-plate-reservation"></a><span data-ttu-id="9544d-277">الحجز المرن للوحة الترخيص</span><span class="sxs-lookup"><span data-stu-id="9544d-277">Flexible license plate reservation</span></span>

### <a name="business-scenario"></a><span data-ttu-id="9544d-278">سيناريو الأعمال</span><span class="sxs-lookup"><span data-stu-id="9544d-278">Business scenario</span></span>

<span data-ttu-id="9544d-279">في هذا السيناريو، تستخدم إحدى الشركات إدارة المستودعات ومعالجة العمل، وتعالج ، وتعالج تخطيط الحِمل على مستوى البالتات/الحاويات الفردية خارج Supply Chain Management قبل إنشاء العمل.</span><span class="sxs-lookup"><span data-stu-id="9544d-279">In this scenario, a company uses warehouse management and work processing, and handles load planning at the level of individual pallets/containers outside Supply Chain Management before work is created.</span></span> <span data-ttu-id="9544d-280">يتم تمثيل هذه الحاويات بواسطة لوحات الترخيص في أبعاد المخزون.</span><span class="sxs-lookup"><span data-stu-id="9544d-280">These containers are represented by license plates in the inventory dimensions.</span></span> <span data-ttu-id="9544d-281">وبالتالي، بالنسبة إلى هذا الأسلوب، يجب تعيين لوحات ترخيص معينة بشكل مسبق إلى بنود أوامر المبيعات قبل تنفيذ عمل الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="9544d-281">Therefore, for this approach, specific license plates must be pre-assigned to sales order lines before picking work is done.</span></span> <span data-ttu-id="9544d-282">تبحث الشركة عن المرونة في الطريقة التي تتم بها معالجة قواعد حجز لوحة الترخيص، بحيث تحدث السلوكيات التالية:</span><span class="sxs-lookup"><span data-stu-id="9544d-282">The company is looking for flexibility in the way that the license plate reservation rules are handled, so that the following behaviors occur:</span></span>

- <span data-ttu-id="9544d-283">يمكن تسجيل لوحة الترخيص وحجزها عند أخذ الطلب بواسطة معالج المبيعات، ولا يمكن أخذها من قبل طلبات أخرى.</span><span class="sxs-lookup"><span data-stu-id="9544d-283">A license plate can be recorded and reserved when the order is taken by the sales processor, and it can't be taken by other demands.</span></span> <span data-ttu-id="9544d-284">يضمن هذا السلوك شحن لوحة الترخيص التي تم تخطيطها إلى العميل.</span><span class="sxs-lookup"><span data-stu-id="9544d-284">This behavior helps guarantee that the license plate that was planned is shipped to the customer.</span></span>
- <span data-ttu-id="9544d-285">إذا لم يتم تعيين لوحة الترخيص إلى بند أمر المبيعات فبإمكان موظفي المستودع تحديد لوحة ترخيص أثناء عمل الانتقاء، بعد اكتمال تسجيل أمر المبيعات وحجزه.</span><span class="sxs-lookup"><span data-stu-id="9544d-285">If the license plate isn't already assigned to a sales order line, warehouse personnel can select a license plate during picking work, after sales order registration and reservation are completed.</span></span>

### <a name="turn-on-flexible-license-plate-reservation"></a><span data-ttu-id="9544d-286">تشغيل الحجز المرن للوحة الترخيص</span><span class="sxs-lookup"><span data-stu-id="9544d-286">Turn on flexible license plate reservation</span></span>

<span data-ttu-id="9544d-287">قبل أن تتمكن من استخدام الحجز المرن للوحة الترخيص، يجب تشغيل ميزتين في النظام.</span><span class="sxs-lookup"><span data-stu-id="9544d-287">Before you can use flexible license plate reservation, two features must be turned on in your system.</span></span> <span data-ttu-id="9544d-288">بإمكان المسؤولين استخدام إعدادات [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة هاتين الميزتين وتشغيلهما إذا كانتا مطلوبتين.</span><span class="sxs-lookup"><span data-stu-id="9544d-288">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="9544d-289">يجب تشغيل الميزات بالترتيب التالي:</span><span class="sxs-lookup"><span data-stu-id="9544d-289">You must turn on the features in the following order:</span></span>

1. <span data-ttu-id="9544d-290">**اسم الميزة:** *حجز مرنة للأبعاد على مستوى المستودع*</span><span class="sxs-lookup"><span data-stu-id="9544d-290">**Feature name:** *Flexible warehouse-level dimension reservation*</span></span>
1. <span data-ttu-id="9544d-291">**اسم الميزة:** *حجز مرن للوحة الترخيص الملتزمة بالأمر*</span><span class="sxs-lookup"><span data-stu-id="9544d-291">**Feature name:** *Flexible order-committed license plate reservation*</span></span>

### <a name="reserve-a-specific-license-plate-on-the-sales-order"></a><span data-ttu-id="9544d-292">حجز لوحة ترخيص معينة على أمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="9544d-292">Reserve a specific license plate on the sales order</span></span>

<span data-ttu-id="9544d-293">لتمكين حجز لوحة الترخيص على أمر، يجب تحديد خانة الاختيار **السماح بالحجز حساب الطلب** على مستوى **لوحة الترخيص** في صفحة **التدرجات الهرمية لحجز المخزون** للتدرج الهرمي المقترنة بالصنف ذي الصلة.</span><span class="sxs-lookup"><span data-stu-id="9544d-293">To enable license plate reservation on an order, you must select the **Allow reservation on demand order** check box for the **License plate** level on the **Inventory reservation hierarchies** page for the hierarchy that is associated with the relevant item.</span></span>

![صفحة التدرجات الهرمية لحجز المخزون للتدرج الهرمي للحجز المرن للوحة الترخيص](media/Flexible-LP-reservation-hierarchy.png)

<span data-ttu-id="9544d-295">يمكنك تمكين حجز لوحة الترخيص على الأمر في أي نقطة في عملية النشر.</span><span class="sxs-lookup"><span data-stu-id="9544d-295">You can enable license plate reservation on the order at any point in your deployment.</span></span> <span data-ttu-id="9544d-296">لن يؤثر هذا التغيير على أية حجز أو عمل مستودع مفتوح تم إنشاؤه قبل حدوث التغيير.</span><span class="sxs-lookup"><span data-stu-id="9544d-296">This change won't affect any reservations or open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="9544d-297">ومع ذلك، لا يمكنك مسح خانة الاختيار **السماح بالحجز حسب الطلب** في حال وجود حركات مخزون صادرة مفتوحة لديها حالة المشكلة *تحت الطلب* أو *المطلوب المحجوز‬* أو *الفعلي المحجوز* لصنف أو أكثر يقترن بهذا التدرج الهرمي للحجز.</span><span class="sxs-lookup"><span data-stu-id="9544d-297">However, you can't clear the **Allow reservation on demand order** check box if open outbound inventory transactions that have an issue status of *On order*, *Reserved ordered*, or *Reserved physical* exist for one or more items that are associated with that reservation hierarchy.</span></span>

<span data-ttu-id="9544d-298">حتى في حالة تحديد خانة الاختيار **السماح بالحجز حسب الطلب** لمستوى **لوحة الترخيص**، يبقى من الممكن *عدم* حجز لوحة ترخيص محددة على الأمر.</span><span class="sxs-lookup"><span data-stu-id="9544d-298">Even if the **Allow reservation on demand order** check box is selected for the **License plate** level, it's still possible *not* to reserve a specific license plate on the order.</span></span> <span data-ttu-id="9544d-299">في هذه الحالة، يتم تطبيق منطق عمليات المستودع الافتراضي الصالح للتدرج الهرمي للحجز.</span><span class="sxs-lookup"><span data-stu-id="9544d-299">In this case, the default warehouse operations logic that is valid for the reservation hierarchy applies.</span></span>

<span data-ttu-id="9544d-300">لحجز لوحة ترخيص معينة، يجب عليك استخدام عملية [Open Data Protocol (OData)](../../fin-ops-core/dev-itpro/data-entities/odata.md).</span><span class="sxs-lookup"><span data-stu-id="9544d-300">To reserve a specific license plate, you must use an [Open Data Protocol (OData)](../../fin-ops-core/dev-itpro/data-entities/odata.md) process.</span></span> <span data-ttu-id="9544d-301">في التطبيق، يمكنك إجراء هذا الحجز مباشرة من أمر مبيعات باستخدام خيار **الحجوزات الملتزمة بالطلب لكل لوحة ترخيص** في أمر **فتح في Excel**.</span><span class="sxs-lookup"><span data-stu-id="9544d-301">In the application, you can do this reservation directly from a sales order by using the **Order-committed reservations per license plate** option of the **Open in Excel** command.</span></span> <span data-ttu-id="9544d-302">في بيانات الكيان المفتوحة في الوظيفة الإضافية من Excel، يجب إدخال البيانات التالية ذات الصلة بالحجز ثم تحديد **نشر** لإرسال البيانات مرة أخرى إلى Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="9544d-302">In the entity data that is opened in the Excel add-in, you must enter the following reservation-related data and then select **Publish** to send the data back to Supply Chain Management:</span></span>

- <span data-ttu-id="9544d-303">المرجع (قيمة *أمر المبيعات* مدعومة فقط.)</span><span class="sxs-lookup"><span data-stu-id="9544d-303">Reference (Only the *Sales order* value is supported.)</span></span>
- <span data-ttu-id="9544d-304">رقم الأمر (يمكن اشتقاق القيمة من الشحنة.)</span><span class="sxs-lookup"><span data-stu-id="9544d-304">Order number (The value can be derived from the lot.)</span></span>
- <span data-ttu-id="9544d-305">كود الشحنة</span><span class="sxs-lookup"><span data-stu-id="9544d-305">Lot ID</span></span>
- <span data-ttu-id="9544d-306">لوحة الترخيص</span><span class="sxs-lookup"><span data-stu-id="9544d-306">License plate</span></span>
- <span data-ttu-id="9544d-307">الكمية</span><span class="sxs-lookup"><span data-stu-id="9544d-307">Quantity</span></span>

<span data-ttu-id="9544d-308">إذا كان من الضروري حجز لوحة ترخيص معينة لصنف يتم تعقبه بواسطة دُفعة، فاستخدم الصفحة **حجز الدفعات**، كما جاء وصفه في القسم [إدخال تفاصيل أمر المبيعات](#sales-order-details).</span><span class="sxs-lookup"><span data-stu-id="9544d-308">If you must reserve a specific license plate for a batch-tracked item, use the **Batch reservation** page, as described in the [Enter sales order details](#sales-order-details) section.</span></span>

<span data-ttu-id="9544d-309">عند معالجة بند أمر المبيعات الذي يستخدم حجز لوحة الترخيص الملتزمة بالأمر بواسطة عمليات المستودع، لا يتم استخدام توجيهات المواقع.</span><span class="sxs-lookup"><span data-stu-id="9544d-309">When the sales order line that uses an order-committed license plate reservation is processed by warehouse operations, location directives aren't used.</span></span>

<span data-ttu-id="9544d-310">إذا كان صنف عمل المستودع يتكون من بنود تساوي بالته كاملة ولديه كميات ملتزمة للوحة الترخيص، فيمكنك تحسين عملية الانتقاء من خلال استخدام عنصر قائمة جهاز محمول حيث تم تعيين الخيار **معالجة حسب لوحة الترخيص** إلى *نعم*.</span><span class="sxs-lookup"><span data-stu-id="9544d-310">If a warehouse work item consists of lines that equal a complete pallet and have license plate–committed quantities, you can optimize the picking process by using a mobile device menu item where the **Handle by license plate** option is set to *Yes*.</span></span> <span data-ttu-id="9544d-311">بإمكان عامل المستودع بعد ذلك فحص لوحة الترخيص لإكمال الانتقاء بدلاً من أن يحتاج إلى مسح الأصناف من العمل الواحد تلو الآخر.</span><span class="sxs-lookup"><span data-stu-id="9544d-311">A warehouse worker can then scan a license plate to complete a pick instead of having to scan the items from the work one by one.</span></span>

![عنصر قائمة الجهاز المحمول حيث تم تعيين الخيار "معالجة حسب لوحة الترخيص" إلى "نعم"](media/Handle-by-LP-menu-item.png)

<span data-ttu-id="9544d-313">لأن الوظيفة **معالجة حسب لوحة الترخيص** لا تدعم العمل الذي يغطي بالتات متعددة، فمن الأفضل وجود عنصر عمل منفصل للوحات الترخيص المختلفة.</span><span class="sxs-lookup"><span data-stu-id="9544d-313">Because the **Handle by license plate** functionality doesn't support work that covers multiple pallets, it's better to have a separate work item for different license plates.</span></span> <span data-ttu-id="9544d-314">لاستخدام هذا الأسلوب، أضف الحقل **معرف لوحة ترخيص ملتزمة بالأوامر** كفاصل رأس عمل في صفحة **قالب العمل**.</span><span class="sxs-lookup"><span data-stu-id="9544d-314">To use this approach, add the **Order-committed license plate ID** field as a work header break on the **Work template** page.</span></span>

> [!NOTE]
> <span data-ttu-id="9544d-315">بالنسبة لعمليه إنشاء العمل المرتبطة بالأمر، سيتم تعيين قيمه "بعد المخزون المرتبط بالطلب" إلى بنود عمل الانتقاء، ولن يمكن عرض قيمه لوح الترخيص مباشره.</span><span class="sxs-lookup"><span data-stu-id="9544d-315">For the order-committed work creation process, an "order-committed inventory dimension" value will be assigned to the picking work lines, and it won't be possible to view the license plate value directly.</span></span> <span data-ttu-id="9544d-316">يتم دعم العمليه *الموجهة بواسطة المستخدم* فقط عند إعداد عنصر قائمه الجهاز المحمول.</span><span class="sxs-lookup"><span data-stu-id="9544d-316">Only the *User directed* process is supported when setting up a mobile device menu item.</span></span>

## <a name="example-scenario-set-up-and-process-an-order-committed-license-plate-reservation"></a><span data-ttu-id="9544d-317">السيناريو المثال: إعداد ومعالجة حجز لوحة ترخيص ملتزمة بالأمر</span><span class="sxs-lookup"><span data-stu-id="9544d-317">Example scenario: Set up and process an order-committed license plate reservation</span></span>

<span data-ttu-id="9544d-318">يُظهر هذا السيناريو كيفية إعداد ومعالجة حجز لوحة ترخيص ملتزمة بالأمر.</span><span class="sxs-lookup"><span data-stu-id="9544d-318">This scenario shows how to set up and process an order-committed license plate reservation.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="9544d-319">جعل بيانات العرض التوضيحي متاحة</span><span class="sxs-lookup"><span data-stu-id="9544d-319">Make demo data available</span></span>

<span data-ttu-id="9544d-320">يشير السيناريو إلى قيم وسجلات مضمنة في بيانات العرض التوضيحي القياسية المتوفرة لـ Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9544d-320">This scenario refers to values and records that are included in the standard demo data that is provided for Supply Chain Management.</span></span> <span data-ttu-id="9544d-321">وبالتالي، إذا أردت العمل عبر هذا السيناريو باستخدام القيم المتوفرة هنا، فتأكد من العمل على بيئة حيث تم تثبيت بيانات العرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="9544d-321">If you want to work through the scenario by using the values that are provided here, be sure to work on an environment where the demo data is installed.</span></span> <span data-ttu-id="9544d-322">بالإضافة إلى ذلك، عيّن الكيان القانوني إلى **USMF** قبل البدء.</span><span class="sxs-lookup"><span data-stu-id="9544d-322">Additionally, set the legal entity to **USMF** before you begin.</span></span>

### <a name="create-an-inventory-reservation-hierarchy-that-allows-for-license-plate-reservation"></a><span data-ttu-id="9544d-323">إنشاء تدرج هرمي لحجز المخزون يسمح بحجز لوحة الترخيص</span><span class="sxs-lookup"><span data-stu-id="9544d-323">Create an inventory reservation hierarchy that allows for license plate reservation</span></span>

1. <span data-ttu-id="9544d-324">انتقل إلى **إدارة المستودعات \> إعداد \> المخزون \> التدرج الهرمي للحجز**.</span><span class="sxs-lookup"><span data-stu-id="9544d-324">Go to **Warehouse management \> Setup \> Inventory \> Reservation hierarchy**.</span></span>
1. <span data-ttu-id="9544d-325">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="9544d-325">Select **New**.</span></span>
1. <span data-ttu-id="9544d-326">في حقل **الاسم** أدخل قيمة (على سبيل المثال، *FlexibleLP*).</span><span class="sxs-lookup"><span data-stu-id="9544d-326">In the **Name** field, enter a value (for example, *FlexibleLP*).</span></span>
1. <span data-ttu-id="9544d-327">في الحقل **الوصف**، ادخل قيمة (على سبيل المثال، *حجز LP مرن*).</span><span class="sxs-lookup"><span data-stu-id="9544d-327">In the **Description** field, enter a value (for example, *Flexible LP reservation*).</span></span>
1. <span data-ttu-id="9544d-328">في القائمة **محدد**، حدد **رقم الدُفعة** و **الرقم التسلسلي** و **المالك**.</span><span class="sxs-lookup"><span data-stu-id="9544d-328">In the **Selected** list, select **Batch number**, **Serial number**, and **Owner**.</span></span>
1. <span data-ttu-id="9544d-329">حدد زر **إزالة** ![سهم للخلف](media/backward-button.png) لنقل السجلات المحددة إلى قائمة **متوفرة**.</span><span class="sxs-lookup"><span data-stu-id="9544d-329">Select the **Remove** button ![backward arrow](media/backward-button.png) to move the selected records to the **Available** list.</span></span>
1. <span data-ttu-id="9544d-330">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="9544d-330">Select **OK**.</span></span>
1. <span data-ttu-id="9544d-331">في الصف على مستوى بعد **لوحة الترخيص**، حدد خانة الاختيار **السماح بالحجز حسب الطلب**.</span><span class="sxs-lookup"><span data-stu-id="9544d-331">In the row for the **License plate** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="9544d-332">يتم تحديد مستوى **الموقع** تلقائيًا، ولا يمكنك إلغاء تحديد خانة الاختيار التابعة له.</span><span class="sxs-lookup"><span data-stu-id="9544d-332">The **Location** level is automatically selected, and you can't clear the check box for it.</span></span>
1. <span data-ttu-id="9544d-333">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="9544d-333">Select **Save**.</span></span>

### <a name="create-two-released-products"></a><span data-ttu-id="9544d-334">إنشاء منتجين صادرين</span><span class="sxs-lookup"><span data-stu-id="9544d-334">Create two released products</span></span>

1. <span data-ttu-id="9544d-335">انتقل إلى **إدارة معلومات المنتج‬ \> المنتجات \> المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="9544d-335">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="9544d-336">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="9544d-336">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="9544d-337">في مربع الحوار **منتج صادر جديد**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="9544d-337">In the **New released product** dialog box, set the following values:</span></span>

    - <span data-ttu-id="9544d-338">**رقم المنتج:** *الصنف1*</span><span class="sxs-lookup"><span data-stu-id="9544d-338">**Product number:** *Item1*</span></span>
    - <span data-ttu-id="9544d-339">**رقم الصنف:** *الصنف1*</span><span class="sxs-lookup"><span data-stu-id="9544d-339">**Item number:** *Item1*</span></span>
    - <span data-ttu-id="9544d-340">**مجموعة نماذج الصنف:** *FIFO*</span><span class="sxs-lookup"><span data-stu-id="9544d-340">**Item model group:** *FIFO*</span></span>
    - <span data-ttu-id="9544d-341">**مجموعة الأصناف:** *صوت*</span><span class="sxs-lookup"><span data-stu-id="9544d-341">**Item group:** *Audio*</span></span>
    - <span data-ttu-id="9544d-342">**مجموعة أبعاد التخزين:** *Ware*</span><span class="sxs-lookup"><span data-stu-id="9544d-342">**Storage dimension group:** *Ware*</span></span>
    - <span data-ttu-id="9544d-343">**مجموعة أبعاد التعقب:** *بلا*</span><span class="sxs-lookup"><span data-stu-id="9544d-343">**Tracking dimension group:** *None*</span></span>
    - <span data-ttu-id="9544d-344">**التدرج الهرمي للحجز:** *FlexibleLP*</span><span class="sxs-lookup"><span data-stu-id="9544d-344">**Reservation hierarchy:** *FlexibleLP*</span></span>

1. <span data-ttu-id="9544d-345">حدد **موافق** لإنشاء المنتج وإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="9544d-345">Select **OK** to create the product and close the dialog box.</span></span>
1. <span data-ttu-id="9544d-346">يفتح المنتج الجديد.</span><span class="sxs-lookup"><span data-stu-id="9544d-346">The new product is opened.</span></span> <span data-ttu-id="9544d-347">في علامة التبويب السريعة **المستودع**، عيّن الحقل **معرف مجموعة تسلسل الوحدة** إلى *ea*.</span><span class="sxs-lookup"><span data-stu-id="9544d-347">On the **Warehouse** FastTab, set the **Unit sequence group ID** field to *ea*.</span></span>
1. <span data-ttu-id="9544d-348">كرر الخطوات السابقة لإنشاء منتج ثان له نفس الإعدادات، ولكن قم بتعيين حقلي **رقم المنتج** و **رقم الصنف** إلى *الصنف 2*.</span><span class="sxs-lookup"><span data-stu-id="9544d-348">Repeat the previous steps to create a second product that has the same settings, but set the **Product number** and **Item number** fields to *Item2*.</span></span>
1. <span data-ttu-id="9544d-349">في جزء الإجراءات، في علامة التبويب **إدارة المخزون**، في المجموعة **عرض**، حدد **المخزون الفعلي**.</span><span class="sxs-lookup"><span data-stu-id="9544d-349">On the Action Pane, on the **Manage inventory** tab, in the **View** group, select **On-hand inventory**.</span></span> <span data-ttu-id="9544d-350">ثم حدد **تسوية الكمية**.</span><span class="sxs-lookup"><span data-stu-id="9544d-350">Then select **Quantity adjustment**.</span></span>
1. <span data-ttu-id="9544d-351">قم بتسوية المخزون الفعلي للأصناف الجديدة كما هو محدد في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="9544d-351">Adjust the on-hand inventory of the new items as specified in the following table.</span></span>

    | <span data-ttu-id="9544d-352">العنصر</span><span class="sxs-lookup"><span data-stu-id="9544d-352">Item</span></span>  | <span data-ttu-id="9544d-353">المستودع</span><span class="sxs-lookup"><span data-stu-id="9544d-353">Warehouse</span></span> | <span data-ttu-id="9544d-354"> الموقع</span><span class="sxs-lookup"><span data-stu-id="9544d-354">Location</span></span> | <span data-ttu-id="9544d-355">لوحة الترخيص</span><span class="sxs-lookup"><span data-stu-id="9544d-355">License plate</span></span> | <span data-ttu-id="9544d-356">الكمية</span><span class="sxs-lookup"><span data-stu-id="9544d-356">Quantity</span></span> |
    |-------|-----------|----------|---------------|----------|
    | <span data-ttu-id="9544d-357">الصنف1</span><span class="sxs-lookup"><span data-stu-id="9544d-357">Item1</span></span> | <span data-ttu-id="9544d-358">24</span><span class="sxs-lookup"><span data-stu-id="9544d-358">24</span></span>        | <span data-ttu-id="9544d-359">FL-010</span><span class="sxs-lookup"><span data-stu-id="9544d-359">FL-010</span></span>   | <span data-ttu-id="9544d-360">LP01</span><span class="sxs-lookup"><span data-stu-id="9544d-360">LP01</span></span>          | <span data-ttu-id="9544d-361">10</span><span class="sxs-lookup"><span data-stu-id="9544d-361">10</span></span>       |
    | <span data-ttu-id="9544d-362">الصنف1</span><span class="sxs-lookup"><span data-stu-id="9544d-362">Item1</span></span> | <span data-ttu-id="9544d-363">24</span><span class="sxs-lookup"><span data-stu-id="9544d-363">24</span></span>        | <span data-ttu-id="9544d-364">FL-011</span><span class="sxs-lookup"><span data-stu-id="9544d-364">FL-011</span></span>   | <span data-ttu-id="9544d-365">LP02</span><span class="sxs-lookup"><span data-stu-id="9544d-365">LP02</span></span>          | <span data-ttu-id="9544d-366">10</span><span class="sxs-lookup"><span data-stu-id="9544d-366">10</span></span>       |
    | <span data-ttu-id="9544d-367">الصنف2</span><span class="sxs-lookup"><span data-stu-id="9544d-367">Item2</span></span> | <span data-ttu-id="9544d-368">24</span><span class="sxs-lookup"><span data-stu-id="9544d-368">24</span></span>        | <span data-ttu-id="9544d-369">FL-010</span><span class="sxs-lookup"><span data-stu-id="9544d-369">FL-010</span></span>   | <span data-ttu-id="9544d-370">LP01</span><span class="sxs-lookup"><span data-stu-id="9544d-370">LP01</span></span>          | <span data-ttu-id="9544d-371">5</span><span class="sxs-lookup"><span data-stu-id="9544d-371">5</span></span>        |
    | <span data-ttu-id="9544d-372">الصنف2</span><span class="sxs-lookup"><span data-stu-id="9544d-372">Item2</span></span> | <span data-ttu-id="9544d-373">24</span><span class="sxs-lookup"><span data-stu-id="9544d-373">24</span></span>        | <span data-ttu-id="9544d-374">FL-011</span><span class="sxs-lookup"><span data-stu-id="9544d-374">FL-011</span></span>   | <span data-ttu-id="9544d-375">LP02</span><span class="sxs-lookup"><span data-stu-id="9544d-375">LP02</span></span>          | <span data-ttu-id="9544d-376">5</span><span class="sxs-lookup"><span data-stu-id="9544d-376">5</span></span>        |

    > [!NOTE]
    > <span data-ttu-id="9544d-377">يجب إنشاء لوحتي الترخيص واستخدام المواقع التي تسمح بالأصناف المختلطة، مثل *FL-010* و *FL-011*.</span><span class="sxs-lookup"><span data-stu-id="9544d-377">You must create the two license plates and use locations that allow for mixed items, such as *FL-010* and *FL-011*.</span></span>

### <a name="create-a-sales-order-and-reserve-a-specific-license-plate"></a><span data-ttu-id="9544d-378">إنشاء أمر مبيعات وحجز لوحة ترخيص معينة</span><span class="sxs-lookup"><span data-stu-id="9544d-378">Create a sales order and reserve a specific license plate</span></span>

1. <span data-ttu-id="9544d-379">انتقل إلى **المبيعات والتسويق \> أوامر المبيعات \> كافة أوامر المبيعات‬**.</span><span class="sxs-lookup"><span data-stu-id="9544d-379">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="9544d-380">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="9544d-380">Select **New**.</span></span>
1. <span data-ttu-id="9544d-381">في مربع الحوار **إنشاء أمر المبيعات**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="9544d-381">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="9544d-382">**حساب العميل:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="9544d-382">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="9544d-383">**المستودع:** *24*</span><span class="sxs-lookup"><span data-stu-id="9544d-383">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="9544d-384">حدد **موافق** لإغلاق مربع الحوار **إنشاء أمر مبيعات** وافتح أمر المبيعات الجديد.</span><span class="sxs-lookup"><span data-stu-id="9544d-384">Select **OK** to close the **Create sales order** dialog box and open the new sales order.</span></span>
1. <span data-ttu-id="9544d-385">على علامة التبويب السريعة **بنود أمر المبيعات**، أضف بندًا لديه الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="9544d-385">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="9544d-386">**رقم الصنف:** *الصنف1*</span><span class="sxs-lookup"><span data-stu-id="9544d-386">**Item number:** *Item1*</span></span>
    - <span data-ttu-id="9544d-387">**الكمية:** *10*</span><span class="sxs-lookup"><span data-stu-id="9544d-387">**Quantity:** *10*</span></span>

1. <span data-ttu-id="9544d-388">أضف بند أمر مبيعات ثان لديه الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="9544d-388">Add a second sales order line that has the following settings:</span></span>

    - <span data-ttu-id="9544d-389">**رقم الصنف:** *الصنف2*</span><span class="sxs-lookup"><span data-stu-id="9544d-389">**Item number:** *Item2*</span></span>
    - <span data-ttu-id="9544d-390">**الكمية:** *5*</span><span class="sxs-lookup"><span data-stu-id="9544d-390">**Quantity:** *5*</span></span>

1. <span data-ttu-id="9544d-391">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="9544d-391">Select **Save**.</span></span>
1. <span data-ttu-id="9544d-392">على علامة التبويب السريعة **تفاصيل البند**، على علامة التبويب **إعداد**، سجل قيمة **كود الشحنة** لكل بند.</span><span class="sxs-lookup"><span data-stu-id="9544d-392">On the **Line details** FastTab, on the **Setup** tab, make a note of the **Lot ID** value for each line.</span></span> <span data-ttu-id="9544d-393">ستكون هذه القيم مطلوبة أثناء حجز لوحات ترخيص محددة.</span><span class="sxs-lookup"><span data-stu-id="9544d-393">These values will be required during reservation of specific license plates.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9544d-394">لحجز لوحة ترخيص محددة، يجب استخدام كيان البيانات **حجوزات ملتزمة بالأوامر لكل لوحة ترخيص**.</span><span class="sxs-lookup"><span data-stu-id="9544d-394">To reserve a specific license plate, you must use the **Order-committed reservations per license plate** data entity.</span></span> <span data-ttu-id="9544d-395">لحجز صنف يتم تعقبه بواسطة دُفعة على لوحة ترخيص معينة، يمكنك أيضًا استخدام الصفحة **حجز الدفعات**، كما جاء وصفه في القسم [إدخال تفاصيل أمر المبيعات](#sales-order-details).</span><span class="sxs-lookup"><span data-stu-id="9544d-395">To reserve a batch-tracked item on a specific license plate, you can also use the **Batch reservation** page, as described in the [Enter sales order details](#sales-order-details) section.</span></span>
    >
    > <span data-ttu-id="9544d-396">إذا أدخلت لوحة الترخيص مباشرة في بند أمر المبيعات وأكدته للنظام، فلن يتم استخدام معالجة إدارة المستودعات للبند.</span><span class="sxs-lookup"><span data-stu-id="9544d-396">If you enter the license plate directly on the sales order line and confirm it to the system, warehouse management processing won't be used for the line.</span></span>

1. <span data-ttu-id="9544d-397">حدد **فتح في Microsoft Office**، وحدد **حجوزات ملتزمة بالأوامر لكل لوحة ترخيص**، وقم بتنزيل الملف.</span><span class="sxs-lookup"><span data-stu-id="9544d-397">Select **Open in Microsoft Office**, select **Order-committed reservations per license plate**, and download the file.</span></span>
1. <span data-ttu-id="9544d-398">افتح الملف الذي تم تنزيله في Excel، وحدد **تمكين التحرير** لتمكين تشغيل وظيفة Excel الإضافية.</span><span class="sxs-lookup"><span data-stu-id="9544d-398">Open the downloaded file in Excel, and select **Enable editing** to enable the Excel add-in to run.</span></span>
1. <span data-ttu-id="9544d-399">إذا كنت تقوم بتشغيل وظيفة Excel الإضافية للمرة الأولى، فحدد **الثقة بهذه الوظيفة الإضافية**.</span><span class="sxs-lookup"><span data-stu-id="9544d-399">If you're running the Excel add-in for the first time, select **Trust this Add-in**.</span></span>
1. <span data-ttu-id="9544d-400">في حالة مطالبتك بتسجيل الدخول، حدد **تسجيل الدخول**، وبعد ذلك سجّل الدخول باستخدام نفس بيانات الاعتماد التي استخدمتها لتسجيل الدخول إلى Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9544d-400">If you're prompted to sign in, select **Sign in**, and then sign in by using the same credentials that you used to sign in to Supply Chain Management.</span></span>
1. <span data-ttu-id="9544d-401">لحجز صنف في لوحة ترخيص معينة، في وظيفة Excel الإضافية، حدد **جديد** لإضافة بند حجز ، ثم عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="9544d-401">To reserve an item on a specific license plate, in the Excel add-in, select **New** to add a reservation line, and then set the following values:</span></span>

    - <span data-ttu-id="9544d-402">**كود الشحنة:** أدخل قيمة **كود الشحنة** التي عثرت عليها لبند أمر المبيعات في *الصنف1*.</span><span class="sxs-lookup"><span data-stu-id="9544d-402">**Lot ID:** Enter the **Lot ID** value that you found for the sales order line for *Item1*.</span></span>
    - <span data-ttu-id="9544d-403">**لوحة الترخيص:** *LP02*</span><span class="sxs-lookup"><span data-stu-id="9544d-403">**License plate:** *LP02*</span></span>
    - <span data-ttu-id="9544d-404">**ReservedInventoryQuantity:** *10*</span><span class="sxs-lookup"><span data-stu-id="9544d-404">**ReservedInventoryQuantity:** *10*</span></span>

1. <span data-ttu-id="9544d-405">حدد **جديد** لإضافة بند حجز آخر، ثم قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="9544d-405">Select **New** to add another reservation line, and set the following values:</span></span>

    - <span data-ttu-id="9544d-406">**كود الشحنة:** أدخل قيمة **كود الشحنة** التي عثرت عليها لبند أمر المبيعات في *الصنف2*.</span><span class="sxs-lookup"><span data-stu-id="9544d-406">**Lot ID:** Enter the **Lot ID** value you found for the sales order line for *Item2*.</span></span>
    - <span data-ttu-id="9544d-407">**لوحة الترخيص:** *LP02*</span><span class="sxs-lookup"><span data-stu-id="9544d-407">**License plate:** *LP02*</span></span>
    - <span data-ttu-id="9544d-408">**ReservedInventoryQuantity:** *5*</span><span class="sxs-lookup"><span data-stu-id="9544d-408">**ReservedInventoryQuantity:** *5*</span></span>

1. <span data-ttu-id="9544d-409">في وظيفة Excel الإضافية، حدد **نشر** لإرسال البيانات مرة أخرى إلى Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9544d-409">In the Excel add-in, select **Publish** to send the data back to Supply Chain Management.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9544d-410">سيظهر بند الحجز في النظام فقط في حال اكتمال النشر من دون أخطاء.</span><span class="sxs-lookup"><span data-stu-id="9544d-410">The reservation line will appear in the system only if publishing is completed without errors.</span></span>

1. <span data-ttu-id="9544d-411">عد إلى Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9544d-411">Go back to Supply Chain Management.</span></span> 
1. <span data-ttu-id="9544d-412">لمراجعة حجز الصنف، على علامة التبويب السريعة **بنود أمر المبيعات**، على قائمة **المخزون**، حدد **المحافظة على \> الحجز**.</span><span class="sxs-lookup"><span data-stu-id="9544d-412">To review the item's reservation, on the **Sales order lines** FastTab, on the **Inventory** menu, select **Maintain \> Reservation**.</span></span> <span data-ttu-id="9544d-413">لاحظ أنه بالنسبة إلى بند أمر المبيعات *الصنف1*، المخزون *10* محجوز ولبند أمر المبيعات *الصنف2*، المخزون *5* محجوز.</span><span class="sxs-lookup"><span data-stu-id="9544d-413">Notice that, for the sales order line for *Item1*, inventory of *10* is reserved, and for the sales order line for *Item2*, inventory of *5* is reserved.</span></span>
1. <span data-ttu-id="9544d-414">لمراجعة حركات المخزون المرتبطة بحجز بنود أمر المبيعات، على علامة التبويب السريعة **بنود أمر المبيعات**، في قائمة **المخزون**، حدد **عرض \> الحركات‏‎**.</span><span class="sxs-lookup"><span data-stu-id="9544d-414">To review inventory transactions that are related to the sales order line reservation, on the **Sales order lines** FastTab, on the **Inventory** menu, select **View \> Transactions**.</span></span> <span data-ttu-id="9544d-415">لاحظ وجود حركتين مرتبطتين بالحجز: إحداهما حيث تم تعيين حقل **المرجع** إلى *أمر المبيعات* وأخرى حيث تم تعيين حقل **المرجع** إلى *حجز ملتزم بالأمر*.</span><span class="sxs-lookup"><span data-stu-id="9544d-415">Notice that there are two transactions that are related to the reservation: one where the **Reference** field is set to *Sales order* and one where the **Reference** field is set to *Order-committed reservation*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9544d-416">حركة حيث تم تعيين حقل **المرجع** إلى *أمر المبيعات* تمثل حجز بند الأمر لأبعاد المخزون فوق مستوى **الموقع** (حالة الموقع والمستودع والمخزون).</span><span class="sxs-lookup"><span data-stu-id="9544d-416">A transaction where the **Reference** field is set to *Sales order* represents the order line reservation for inventory dimensions that are above the **Location** level (site, warehouse, and inventory status).</span></span> <span data-ttu-id="9544d-417">حركة حيث تم تعيين حقل **المرجع** إلى *حجز ملتزم بالأمر* تمثل حجز بند الأمر للوحة الترخيص المعينة والموقع المعين.</span><span class="sxs-lookup"><span data-stu-id="9544d-417">A transaction where the **Reference** field is set to *Order-committed reservation* represents the order line reservation for the specific license plate and location.</span></span>

1. <span data-ttu-id="9544d-418">لإصدار أمر المبيعات، في جزء الإجراءات، ضمن علامة التبويب **المستودع**، في مجموعة **الإجراءات**، حدد **إصدار إلى مستودع**.</span><span class="sxs-lookup"><span data-stu-id="9544d-418">To release the sales order, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

### <a name="review-and-process-warehouse-work-with-order-committed-license-plates-assigned"></a><span data-ttu-id="9544d-419">مراجعة ومعالجة عمل المستودع مع لوحات الترخيص المعينة الملتزمة بالأوامر</span><span class="sxs-lookup"><span data-stu-id="9544d-419">Review and process warehouse work with order-committed license plates assigned</span></span>

1. <span data-ttu-id="9544d-420">في علامة التبويب السريعة **بنود أمر المبيعات**، في قائمة **المستودع**، حدد **تفاصيل العمل**.</span><span class="sxs-lookup"><span data-stu-id="9544d-420">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Work details**.</span></span>

    <span data-ttu-id="9544d-421">بعد الانتهاء من عملية الحجز لمجموعة معينة، لا يستخدم النظام توجيهات الموقع عندما ينشئ العمل لأمر المبيعات الذي يستخدم حجز لوحة الترخيص.</span><span class="sxs-lookup"><span data-stu-id="9544d-421">As when reservation is done for a specific batch, the system doesn't use location directives when it creates the work for the sales order that uses license plate reservation.</span></span> <span data-ttu-id="9544d-422">لأن الحجز الذي الملتزم بالأمر يحدد كافة أبعاد المخزون، بما في ذلك الموقع، لا يلزم استخدام توجيهات المواقع، بسبب إدخال أبعاد المخزون فقط في العمل.</span><span class="sxs-lookup"><span data-stu-id="9544d-422">Because the order-committed reservation specifies all the inventory dimensions, including the location, location directives don't have to be used, because those inventory dimensions are just entered in the work.</span></span> <span data-ttu-id="9544d-423">إنها تظهر في القسم **من أبعاد المخزون** في صفحة **حركات مخزون العمل**.</span><span class="sxs-lookup"><span data-stu-id="9544d-423">They are shown in the **From inventory dimensions** section on the **Work inventory transactions** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9544d-424">بعد إنشاء العمل، تتم إزالة حركة المخزون الخاصة بالصنف التي تم تعيين حقل **المرجع** فيها إلى *الحجز الملتزم بالأمر*.</span><span class="sxs-lookup"><span data-stu-id="9544d-424">After the work is created, the item's inventory transaction where the **Reference** field is set to *Order-committed reservation* is removed.</span></span> <span data-ttu-id="9544d-425">حركة المخزون التي تم تعيين الحقل **المرجع** بها على *عمل* تحتفظ الآن بالحجز الفعلي علي كافة ابعاد المخزون الخاصة بالكمية.</span><span class="sxs-lookup"><span data-stu-id="9544d-425">The inventory transaction where the **Reference** field is set to *Work* now holds the physical reservation for all the quantity's inventory dimensions.</span></span>

1. <span data-ttu-id="9544d-426">على الجهاز المحمول، قم بإنهاء انتقاء وتخزين العمل باستخدام عنصر قائمة حيث خانة الاختيار **معالجة حسب لوحة الترخيص** محددة.</span><span class="sxs-lookup"><span data-stu-id="9544d-426">On the mobile device, finish picking and putting the work by using a menu item where the **Handle by license plate** check box is selected.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9544d-427">تساعدك وظيفة **معالجة حسب لوحة الترخيص** على معالجة لوحة الترخيص بأكملها.</span><span class="sxs-lookup"><span data-stu-id="9544d-427">The **Handle by license plate** functionality helps you process the whole license plate.</span></span> <span data-ttu-id="9544d-428">إذا كان من الضروري معالجة جزء من لوحة الترخيص، فلا يمكنك استخدام هذه الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="9544d-428">If you must process part of the license plate, you can't use this functionality.</span></span>
    >
    > <span data-ttu-id="9544d-429">ننصح بوجود أمر عمل منفصل لكل لوحة ترخيص.</span><span class="sxs-lookup"><span data-stu-id="9544d-429">We recommend that you have separate work generated for each license plate.</span></span> <span data-ttu-id="9544d-430">لتحقيق هذه النتيجة، استخدم ميزة **فواصل رؤوس العمل** في صفحة **قالب العمل**.</span><span class="sxs-lookup"><span data-stu-id="9544d-430">To achieve this result, use the **Work header breaks** feature on the **Work template** page.</span></span>

    <span data-ttu-id="9544d-431">تم الآن انتقاء لوحة الترخيص *LP02* لبنود أمر العمل وتخزينها في الموقع *Baydoor*.</span><span class="sxs-lookup"><span data-stu-id="9544d-431">License plate *LP02* is now picked for sales order lines and put to the *Baydoor* location.</span></span> <span data-ttu-id="9544d-432">في هذه المرحلة، تكون جاهزة لتحميلها وإرسالها إلى العميل.</span><span class="sxs-lookup"><span data-stu-id="9544d-432">At this point, it's ready to be loaded and dispatched to the customer.</span></span>

## <a name="exception-handling-of-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="9544d-433">معالجة استثنائية لعمل المستودع الذي يحتوي على أرقام الدفعات المخصصة للأمر</span><span class="sxs-lookup"><span data-stu-id="9544d-433">Exception handling of warehouse work that has order-committed batch numbers</span></span>

<span data-ttu-id="9544d-434">يعمل المستودع الخاص بأرقام أمر الانتقاء-المخصصة إلى نفس معالجه استثناء المستودع القياسي والإجراءات الخاصة به كعمل عادي.</span><span class="sxs-lookup"><span data-stu-id="9544d-434">Warehouse work for picking order-committed batch numbers is subject to the same standard warehouse exception handling and actions as regular work.</span></span> <span data-ttu-id="9544d-435">بشكل عام ، يمكن إلغاء العمل المفتوح أو سطر العمل، حيث يمكن مقاطعته لان موقع المستخدم ممتلئ، ويمكن أن يتم انتقاؤه بشكل قصير، ويمكن تحديثه بسبب الحركة.</span><span class="sxs-lookup"><span data-stu-id="9544d-435">In general, the open work or work line can be canceled, it can be interrupted because a user location is full, it can be short-picked, and it can be updated because of a movement.</span></span> <span data-ttu-id="9544d-436">بالمثل ، يمكن تقليل الكمية المنتقاة للعمل التي تم إكمالها بالفعل، أو يمكن عكس العمل.</span><span class="sxs-lookup"><span data-stu-id="9544d-436">Likewise, the picked quantity of work that has already been completed can be reduced, or the work can be reversed.</span></span>

<span data-ttu-id="9544d-437">يتم تطبيق قاعده المفتاح التالية علي كافة إجراءات معالجه الاستثناءات هذه: لا يمكن استبدال رقم المجموعة التي تم حجزها للعميل برقم مجموعة مختلف ، ولكن لا يمكن تغيير ابعاد التخزين الخاصة به (لوحه الموقع والترخيص) من خلال اي منهما التحديث اليدوي بواسطة المستخدم أو التحديث التلقائي بواسطة النظام.</span><span class="sxs-lookup"><span data-stu-id="9544d-437">The following key rule is applied to all these exception handling actions: the batch number that was reserved for the customer can never be replaced with a different batch number, but its storage dimensions (location and license plate) can be changed through either a manual update by the user or an automatic update by the system.</span></span> <span data-ttu-id="9544d-438">ويعتمد التحديث التلقائي علي نفس التعيين العشوائي لابعاد التخزين التي يتم تطبيقها عند حجز مجموعة معينه تلقائيا ولكن لم يتم تحديد أية ابعاد للتخزين.</span><span class="sxs-lookup"><span data-stu-id="9544d-438">The automatic update is based on the same random assignment of storage dimensions that applied when a specific batch was automatically reserved but no storage dimensions were specified.</span></span>

### <a name="example-scenario"></a><span data-ttu-id="9544d-439">سيناريو كمثال</span><span class="sxs-lookup"><span data-stu-id="9544d-439">Example scenario</span></span>

<span data-ttu-id="9544d-440">مثال عن هذا السيناريو هو موقف حيث تم إكمال العمل سابقا يتم إلغاء انتقائها باستخدام وظيفة **تقليل الكمية المنتقاة**.</span><span class="sxs-lookup"><span data-stu-id="9544d-440">An example of this scenario is a situation where previously completed work is being unpicked by using the **Reduce picked quantity** function.</span></span> <span data-ttu-id="9544d-441">يفترض هذا المثال أنك قمت بالفعل بإكمال الخطوات الموضحة في [السيناريو المثال: تخصيص رقم الدُفعة](#Example-batch-allocation).</span><span class="sxs-lookup"><span data-stu-id="9544d-441">This example assumes that you've already completed the steps that are described in [Example scenario: Batch number allocation](#Example-batch-allocation).</span></span> <span data-ttu-id="9544d-442">ويستمر من هذا المثال.</span><span class="sxs-lookup"><span data-stu-id="9544d-442">It continues from that example.</span></span>

1. <span data-ttu-id="9544d-443">انتقال إلى **إدارة المستودعات**\>**أحمال**\>**جميع الأحمال**.</span><span class="sxs-lookup"><span data-stu-id="9544d-443">Go to **Warehouse management** \> **Loads** \> **Active loads**.</span></span>
2. <span data-ttu-id="9544d-444">حدد الحمل الذي تم إنشاؤه فيما يتعلق بشحنه أمر التوريد الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="9544d-444">Select the load that was created in connection with the shipment of your sales order.</span></span>
3. <span data-ttu-id="9544d-445">من بنود علامة التبويب السريعة **سطور أمر التحميل**، حدد **تقليل الكمية المنتقاة**.</span><span class="sxs-lookup"><span data-stu-id="9544d-445">From the **Load order lines** FastTab, select **Reduce picked quantity**.</span></span>
4. <span data-ttu-id="9544d-446">في الصفحة **تقليل الكمية المنتقاة** في الحقل **نقل إلى الموقع** ، حدد **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="9544d-446">On the **Reduce picked quantity** page, in the **Move to location** field, select **FL-001**.</span></span>
5. <span data-ttu-id="9544d-447">في الحقل **الانتقال إلى لوحة الترخيص**، حدد **LP33**.</span><span class="sxs-lookup"><span data-stu-id="9544d-447">In the **Move to license plate** field, select **LP33**.</span></span>
6. <span data-ttu-id="9544d-448">في الشبكة، في الحقل **كميه المخزون التي سيتم إلغاء انتقائها**، أدخل **10.**</span><span class="sxs-lookup"><span data-stu-id="9544d-448">In the grid, in the **Inventory quantity to unpick** field, enter **10**.</span></span>
7. <span data-ttu-id="9544d-449">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="9544d-449">Select **OK**.</span></span>

<span data-ttu-id="9544d-450">وفيما يلي نتائج إجراء إلغاء الانتقاء:</span><span class="sxs-lookup"><span data-stu-id="9544d-450">Here are the results of the unpicking action:</span></span>

- <span data-ttu-id="9544d-451">تم تعيين حالة العمل الذي تم إغلاقه مسبقا إلى **ملغى**.</span><span class="sxs-lookup"><span data-stu-id="9544d-451">The status of the previously closed work is set to **Canceled**.</span></span>
- <span data-ttu-id="9544d-452">يتم إنشاء العمل الجديد لنوع **حركه المخزون** للكمية التي تم إلغاء انتقاؤها والتي تبلغ **10** بالنسبة لرقم الدفعة **B11**.</span><span class="sxs-lookup"><span data-stu-id="9544d-452">New work of the **Inventory movement** type is created for the unpicked quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="9544d-453">يمثل هذا العمل الانتقال من موقع **باب تحميل البضائع** إلى لوحه الترخيص **LP33** في الموقع **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="9544d-453">This work represents the movement from the **Baydoor** location to license plate **LP33** in location **FL-001**.</span></span> <span data-ttu-id="9544d-454">تم تعيين الحقل إلى الحالة **مغلق**.</span><span class="sxs-lookup"><span data-stu-id="9544d-454">The status is set to **Closed**.</span></span>
- <span data-ttu-id="9544d-455">قام النظام باعاده حجز رقم المجموعة الذي تم طلبه في الأصل، ويقوم بتعيين معرفات لوحات الترخيص والموقع.</span><span class="sxs-lookup"><span data-stu-id="9544d-455">The system re-reserves the batch number that was originally ordered, and assigns the location and license plate IDs.</span></span> <span data-ttu-id="9544d-456">(هذه العملية مكافئه لتشغيل وظيفة **البند الاحتياطي** لسطر الأمر الخاص برقم دفعه معين).</span><span class="sxs-lookup"><span data-stu-id="9544d-456">(This process is equivalent to running the **Reserve line** function for the order line for a given batch number).</span></span> <span data-ttu-id="9544d-457">ونتيجة لذلك، يتم عرض الدفعة **B11** كما تم تنفيذها في علامة التبويب السريعة **أرقام المجموعات التي تم التزام بها علي الخط المصدر** في صفحة  **حجز الدفعة** ويحتوي الحقل **الحجز** على الكمية **10** لرقم الدفعة **B11**.</span><span class="sxs-lookup"><span data-stu-id="9544d-457">As a result, batch **B11** is shown as committed on the **Batch numbers committed to source line** FastTab of the **Batch reservation** page, and the **Reservation** field contains a quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="9544d-458">بالإضافة إلى ذلك يتم تعيين حقل **الموقع** على **FL-001** ويتم تعيين **لوحة الترخيص** على **LP11**.</span><span class="sxs-lookup"><span data-stu-id="9544d-458">Additionally, the **Location** field is set to **FL-001**, and the **License plate** field is set to **LP11**.</span></span> <span data-ttu-id="9544d-459">(يمكنك أضافه هذه الحقول إلى الشبكة إذا لم تكن مرئية.)</span><span class="sxs-lookup"><span data-stu-id="9544d-459">(You can add these fields to the grid if they aren't visible.)</span></span>

<span data-ttu-id="9544d-460">توفر الجداول التالية نظره عامه توضح كيفيه قيام النظام بمعالجه حجز المجموعات المرتبطة بالأمر لإجراءات مستودع معينه.</span><span class="sxs-lookup"><span data-stu-id="9544d-460">The following tables provide an overview that shows how the system handles order-committed batch reservation for specific warehouse actions.</span></span> <span data-ttu-id="9544d-461">لتفسير المحتوي في الجداول ، افترض انه يتم تشغيل كل إجراء للمستودع في سياق عمل المستودع الموجود الذي ينتج عن حجز المجموعة المرتبطة بالأمر ، أو أن تنفيذ كل إجراء مستودع يؤثر علي العمل من هذا النوع.</span><span class="sxs-lookup"><span data-stu-id="9544d-461">To interpret the content in the tables, assume that each warehouse action is run in the context of existing warehouse work that originates from an order-committed batch reservation, or that execution of each warehouse action affects work of that type.</span></span>

> [!NOTE]
> <span data-ttu-id="9544d-462">في هذه الجداول ، يشير العمود "الكمية المجمعة" إلى ما إذا كانت كميه المجموعة متوفرة بالإضافة إلى الكمية التي تم حجزها بالفعل بالنسبة لعمليات الحجز المرتبطة بالأمر أو المحجوزة بالفعل بواسطة عمل المستودع الذي تنشا من عمليات الحجز لذلك النوع.</span><span class="sxs-lookup"><span data-stu-id="9544d-462">In these tables, the "Batch quantity is available" column indicates whether a batch quantity is available in addition to the quantity that is either already reserved for the current order-committed reservations or already reserved by the warehouse work that originates from reservations of that type.</span></span>

#### <a name="override-the-pick-location-on-the-open-work"></a><span data-ttu-id="9544d-463">تجاوز موقع الانتقاء في العمل المفتوح</span><span class="sxs-lookup"><span data-stu-id="9544d-463">Override the pick location on the open work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9544d-464">معلمة الإعداد الرئيسية</span><span class="sxs-lookup"><span data-stu-id="9544d-464">Key setup parameter</span></span></th>
<th><span data-ttu-id="9544d-465">كمية الدفعة متاحة</span><span class="sxs-lookup"><span data-stu-id="9544d-465">Batch quantity is available</span></span></th>
<th><span data-ttu-id="9544d-466">خطوات المستخدم الاساسيه</span><span class="sxs-lookup"><span data-stu-id="9544d-466">Key user steps</span></span></th>
<th><span data-ttu-id="9544d-467">عمل المستودع</span><span class="sxs-lookup"><span data-stu-id="9544d-467">Warehouse work</span></span></th>
<th><span data-ttu-id="9544d-468">حجز المجموعة المرتبطة بالأمر</span><span class="sxs-lookup"><span data-stu-id="9544d-468">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="9544d-469">تم تمكين خيار <strong>السماح بتجاوز موقع الانتقاء</strong> علي العامل.</span><span class="sxs-lookup"><span data-stu-id="9544d-469">The <strong>Allow pick location override</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="9544d-470">نعم</span><span class="sxs-lookup"><span data-stu-id="9544d-470">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="9544d-471">حدد عنصر القائمة <strong>تجاوز الموقع</strong> في تطبيق إدارة المستودع للأجهزة المحمولة عند بدء عمل الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="9544d-471">Select the <strong>Override location</strong> menu item on the Warehouse Management mobile app when you start picking work.</span></span></li>
<li><span data-ttu-id="9544d-472">حدد <strong>اقتراح</strong>.</span><span class="sxs-lookup"><span data-stu-id="9544d-472">Select <strong>Suggest</strong>.</span></span></li>
<li><span data-ttu-id="9544d-473">قم بتاكيد الموقع الجديد المقترح بناء علي توفر كميه الدفعة.</span><span class="sxs-lookup"><span data-stu-id="9544d-473">Confirm the new location that is suggested based on batch quantity availability.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="9544d-474">تحدث الإجراءات التالية في العمل الحالي:</span><span class="sxs-lookup"><span data-stu-id="9544d-474">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="9544d-475">ويتم تحديث الموقع الموجود في بند الانتقاء في الموقع الجديد.</span><span class="sxs-lookup"><span data-stu-id="9544d-475">The location on the pick line is updated to the new location.</span></span> <span data-ttu-id="9544d-476">(إذا كان الموقع لوحه ترخيص – يتم التحكم به ، يتم تعيين لوحه ترخيص عشوائية لحركه مخزون العمل ، ويمكن للعامل الانتقاء من اي لوحه ترخيص بالكمية المتاحة.)</span><span class="sxs-lookup"><span data-stu-id="9544d-476">(If the location is license plate–controlled, a random license plate is assigned to the work inventory transaction, and the worker can pick from any license plate that has available quantity.)</span></span></li>
<li><span data-ttu-id="9544d-477">في حالة العثور علي الكمية في أكثر من لوحه ترخيص واحده في الموقع الجديد ، يتم تقسيم بند الانتقاء الأصلي إلى بنود متعددة لمطابقه كل لوحه ترخيص.</span><span class="sxs-lookup"><span data-stu-id="9544d-477">If the quantity is found on more than one license plate in the new location, the original pick line is split into multiple lines to match each license plate.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="9544d-478">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="9544d-478">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9544d-479">لا</span><span class="sxs-lookup"><span data-stu-id="9544d-479">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="9544d-480">حدد عنصر القائمة <strong>تجاوز الموقع</strong> في تطبيق إدارة المستودع للأجهزة المحمولة عند بدء عمل الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="9544d-480">Select the <strong>Override location</strong> menu item on the Warehouse Management mobile app when you start picking work.</span></span></li>
<li><span data-ttu-id="9544d-481">ادخل موقعا يدويا.</span><span class="sxs-lookup"><span data-stu-id="9544d-481">Manually enter a location.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="9544d-482">إجراء <strong>تجاوز الموقع</strong> غير ممكن.</span><span class="sxs-lookup"><span data-stu-id="9544d-482">The <strong>Override location</strong> action isn't possible.</span></span> <span data-ttu-id="9544d-483">وهو يفشل ويتم عرض خطا.</span><span class="sxs-lookup"><span data-stu-id="9544d-483">It fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="9544d-484">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="9544d-484">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a><span data-ttu-id="9544d-485">الزر الكامل – تقسيم بند العمل نظرا لتجاوز الحد الأقصى لموقع المستخدم</span><span class="sxs-lookup"><span data-stu-id="9544d-485">Full button – Split a work line because of overflow on the user location</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9544d-486">معلمة الإعداد الرئيسية</span><span class="sxs-lookup"><span data-stu-id="9544d-486">Key setup parameter</span></span></th>
<th><span data-ttu-id="9544d-487">كمية الدفعة متاحة</span><span class="sxs-lookup"><span data-stu-id="9544d-487">Batch quantity is available</span></span></th>
<th><span data-ttu-id="9544d-488">خطوات المستخدم الاساسيه</span><span class="sxs-lookup"><span data-stu-id="9544d-488">Key user steps</span></span></th>
<th><span data-ttu-id="9544d-489">عمل المستودع</span><span class="sxs-lookup"><span data-stu-id="9544d-489">Warehouse work</span></span></th>
<th><span data-ttu-id="9544d-490">حجز المجموعة المرتبطة بالأمر</span><span class="sxs-lookup"><span data-stu-id="9544d-490">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9544d-491">يتم <strong>تمكين خيار السماح</strong> بتقسيم العمل في عنصر القائمة جهاز المحمول.</span><span class="sxs-lookup"><span data-stu-id="9544d-491">The <strong>Allow splitting of work</strong> option is enabled on the mobile device menu item.</span></span></td>
<td><span data-ttu-id="9544d-492">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="9544d-492">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="9544d-493">حدد عنصر القائمة <strong>كامل</strong> في تطبيق إدارة المستودع للأجهزة المحمولة عند معالجة عمل الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="9544d-493">Select the <strong>Full</strong> menu item on the Warehouse Management mobile app when you process picking work.</span></span></li>
<li><span data-ttu-id="9544d-494">في الحقل <strong>كميه الانتقاء</strong>، ادخل كميه جزئيه من الانتقاء المطلوب للاشاره إلى القدرة الكاملة.</span><span class="sxs-lookup"><span data-stu-id="9544d-494">In the <strong>Pick Qty</strong> field, enter a partial quantity of the required pick to indicate the full capacity.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="9544d-495">وفي العمل الحالي ، يتم تحديث الكمية إلى الكمية المتبقية التي يجب انتقاؤها.</span><span class="sxs-lookup"><span data-stu-id="9544d-495">On the current work, the quantity is updated to the remaining quantity that must be picked.</span></span></li>
<li><span data-ttu-id="9544d-496">يتم إنشاء العمل الجديد للكمية المنتقية وإغلاقه.</span><span class="sxs-lookup"><span data-stu-id="9544d-496">New work for the picked quantity is created and closed.</span></span></li>
</ul></td>
<td><span data-ttu-id="9544d-497">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="9544d-497">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a><span data-ttu-id="9544d-498">تقليل الكمية المنتقاة للعمل المكتمل (من التحميل)</span><span class="sxs-lookup"><span data-stu-id="9544d-498">Reduce the picked quantity of completed work (from a load)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9544d-499">معلمة الإعداد الرئيسية</span><span class="sxs-lookup"><span data-stu-id="9544d-499">Key setup parameter</span></span></th>
<th><span data-ttu-id="9544d-500">كمية الدفعة متاحة</span><span class="sxs-lookup"><span data-stu-id="9544d-500">Batch quantity is available</span></span></th>
<th><span data-ttu-id="9544d-501">خطوات المستخدم الاساسيه</span><span class="sxs-lookup"><span data-stu-id="9544d-501">Key user steps</span></span></th>
<th><span data-ttu-id="9544d-502">عمل المستودع</span><span class="sxs-lookup"><span data-stu-id="9544d-502">Warehouse work</span></span></th>
<th><span data-ttu-id="9544d-503">حجز المجموعة المرتبطة بالأمر</span><span class="sxs-lookup"><span data-stu-id="9544d-503">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="9544d-504">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="9544d-504">Not applicable</span></span></td>
<td><span data-ttu-id="9544d-505">‏‏نعم</span><span class="sxs-lookup"><span data-stu-id="9544d-505">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="9544d-506">افتح صفحه <strong>تقليل الكمية المنتقاة</strong> من بند التحميل.</span><span class="sxs-lookup"><span data-stu-id="9544d-506">Open the <strong>Reduce picked quantity</strong> page from the load line.</span></span></li>
<li><span data-ttu-id="9544d-507">إدخال الكمية الكاملة المراد انتقاؤها.</span><span class="sxs-lookup"><span data-stu-id="9544d-507">Enter the full quantity to unpick.</span></span></li>
<li><span data-ttu-id="9544d-508">حدد لوحة الترخيص/الموقع "تحريك إلى".</span><span class="sxs-lookup"><span data-stu-id="9544d-508">Select a "move to" location/license plate.</span></span></li>
</ol>
</td>
<td>
<ul> 
<li><span data-ttu-id="9544d-509">تم إلغاء العمل المرتبط ببند التحميل.</span><span class="sxs-lookup"><span data-stu-id="9544d-509">Work that is associated with the load line is canceled.</span></span></li>
<li><span data-ttu-id="9544d-510">يتم إنشاء العمل الجديد لحركة المخزون وإغلاقه.</span><span class="sxs-lookup"><span data-stu-id="9544d-510">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="9544d-511">تمت إعاده حجز الكمية لنفس المجموعة.</span><span class="sxs-lookup"><span data-stu-id="9544d-511">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="9544d-512">يقوم النظام بتعيين الموقع ولوحه الترخيص عشوائيا (إذا كان الموقع لوحه ترخيص – يتم التحكم به) حيث تكون الكمية متاحه.</span><span class="sxs-lookup"><span data-stu-id="9544d-512">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9544d-513">لا</span><span class="sxs-lookup"><span data-stu-id="9544d-513">No</span></span></td>
<td><span data-ttu-id="9544d-514">راجع الصف السابق.</span><span class="sxs-lookup"><span data-stu-id="9544d-514">See the previous row.</span></span></td>
<td><span data-ttu-id="9544d-515">راجع الصف السابق.</span><span class="sxs-lookup"><span data-stu-id="9544d-515">See the previous row.</span></span></td>
<td><span data-ttu-id="9544d-516">يتم أعاده حجز الكمية لنفس المجموعة، ولنفس الموقع ولوحه الترخيص (إذا كان الموقع عبارة عن لوحه ترخيص – يتم التحكم به) والتي تم إدخالها اثناء إلغاء الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="9544d-516">The quantity is re-reserved for the same batch, and for the same location and license plate (if the location is license plate–controlled) that were entered during unpicking.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a><span data-ttu-id="9544d-517">نقل صنف داخل مستودع</span><span class="sxs-lookup"><span data-stu-id="9544d-517">Move an item within a warehouse</span></span>

> [!NOTE]
> <span data-ttu-id="9544d-518">لا ينطبق إجراء المستودع الا علي حركه نوع **عمليه إنشاء العمل**، وليس للحركة بواسطة القالب.</span><span class="sxs-lookup"><span data-stu-id="9544d-518">This warehouse action is applicable only to movement of the **Work creation process** type, not to movement by template.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9544d-519">معلمة الإعداد الرئيسية</span><span class="sxs-lookup"><span data-stu-id="9544d-519">Key setup parameter</span></span></th>
<th><span data-ttu-id="9544d-520">كمية الدفعة متاحة</span><span class="sxs-lookup"><span data-stu-id="9544d-520">Batch quantity is available</span></span></th>
<th><span data-ttu-id="9544d-521">خطوات المستخدم الاساسيه</span><span class="sxs-lookup"><span data-stu-id="9544d-521">Key user steps</span></span></th>
<th><span data-ttu-id="9544d-522">عمل المستودع</span><span class="sxs-lookup"><span data-stu-id="9544d-522">Warehouse work</span></span></th>
<th><span data-ttu-id="9544d-523">حجز المجموعة المرتبطة بالأمر</span><span class="sxs-lookup"><span data-stu-id="9544d-523">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="9544d-524">يتم تمكين خيار <strong>السماح بنقل المخزون مع العمل المقترن</strong> علي العامل.</span><span class="sxs-lookup"><span data-stu-id="9544d-524">The <strong>Allow movement of inventory with associated work</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="9544d-525">نعم</span><span class="sxs-lookup"><span data-stu-id="9544d-525">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="9544d-526">ابدأ حركة في تطبيق إدارة المستودع للأجهزة المحمولة.</span><span class="sxs-lookup"><span data-stu-id="9544d-526">Start a movement on the Warehouse Management mobile app.</span></span></li>
<li><span data-ttu-id="9544d-527">أدخل موقعي البداية والنهاية.</span><span class="sxs-lookup"><span data-stu-id="9544d-527">Enter "from" and "to" locations.</span></span></li>
</ol></td>
<td>
<ul>
<li><span data-ttu-id="9544d-528">وفي كل العمل الموجود الذي يتاثر بالنقل ، يتم تحديث موقع الانتقاء إلى الموقع "إلى" الجديد.</span><span class="sxs-lookup"><span data-stu-id="9544d-528">On all existing work that is affected by the move, the pick location is updated to the new "to" location.</span></span></li>
<li><span data-ttu-id="9544d-529">يتم إنشاء العمل الجديد لحركة المخزون وإغلاقه.</span><span class="sxs-lookup"><span data-stu-id="9544d-529">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="9544d-530">تتم أعاده حجز كافة عمليات الحجز الموجودة التي تاثرت بحركة الكمية من الموقع المحدد لنفس المجموعة.</span><span class="sxs-lookup"><span data-stu-id="9544d-530">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch.</span></span> <span data-ttu-id="9544d-531">يقوم النظام بتعيين الموقع ولوحه الترخيص عشوائيا (إذا كان الموقع لوحه ترخيص – يتم التحكم به) حيث تكون الكمية متاحه.</span><span class="sxs-lookup"><span data-stu-id="9544d-531">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9544d-532">لا</span><span class="sxs-lookup"><span data-stu-id="9544d-532">No</span></span></td>
<td><span data-ttu-id="9544d-533">راجع الصف السابق.</span><span class="sxs-lookup"><span data-stu-id="9544d-533">See the previous row.</span></span></td>
<td><span data-ttu-id="9544d-534">راجع الصف السابق.</span><span class="sxs-lookup"><span data-stu-id="9544d-534">See the previous row.</span></span></td>
<td><span data-ttu-id="9544d-535">يتم أعاده حجز كافة عمليات الحجز الموجودة التي تاثرت بحركة الكمية من الموقع المحدد لنفس المجموعة ، وللموقع الجديد "إلى" ولوحه الترخيص (إذا كان الموقع لوحه الترخيص-التي يتم التحكم بها).</span><span class="sxs-lookup"><span data-stu-id="9544d-535">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch, and for the new "to" location and license plate (if the location is license plate–controlled).</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a><span data-ttu-id="9544d-536">حجز الكمية المنتقاة للعمل المكتمل (من التحميل أو الموجة)</span><span class="sxs-lookup"><span data-stu-id="9544d-536">Reverse the picked quantity of completed work (from a load or a wave)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9544d-537">معلمة الإعداد الرئيسية</span><span class="sxs-lookup"><span data-stu-id="9544d-537">Key setup parameter</span></span></th>
<th><span data-ttu-id="9544d-538">كمية الدفعة متاحة</span><span class="sxs-lookup"><span data-stu-id="9544d-538">Batch quantity is available</span></span></th>
<th><span data-ttu-id="9544d-539">خطوات المستخدم الاساسيه</span><span class="sxs-lookup"><span data-stu-id="9544d-539">Key user steps</span></span></th>
<th><span data-ttu-id="9544d-540">عمل المستودع</span><span class="sxs-lookup"><span data-stu-id="9544d-540">Warehouse work</span></span></th>
<th><span data-ttu-id="9544d-541">حجز المجموعة المرتبطة بالأمر</span><span class="sxs-lookup"><span data-stu-id="9544d-541">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'><span data-ttu-id="9544d-542">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="9544d-542">Not applicable</span></span></td>
<td><span data-ttu-id="9544d-543">‏‏نعم</span><span class="sxs-lookup"><span data-stu-id="9544d-543">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="9544d-544">افتح صفحه <strong>العمل العكسي</strong>.</span><span class="sxs-lookup"><span data-stu-id="9544d-544">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="9544d-545">في الصفحة طلب ، حدد الخيار <strong>ترك العناصر في الموقع الحالي</strong>.</span><span class="sxs-lookup"><span data-stu-id="9544d-545">On the request page, select the <strong>Leave items at current location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="9544d-546">تم إلغاء العمل المرتبط بالتحميل.</span><span class="sxs-lookup"><span data-stu-id="9544d-546">All work that is associated with the load is canceled.</span></span></td>
<td><span data-ttu-id="9544d-547">تمت إعاده حجز الكمية لنفس المجموعة.</span><span class="sxs-lookup"><span data-stu-id="9544d-547">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="9544d-548">يقوم النظام بتعيين الموقع ولوحه الترخيص عشوائيا (إذا كان الموقع لوحه ترخيص – يتم التحكم به) حيث تكون الكمية متاحه.</span><span class="sxs-lookup"><span data-stu-id="9544d-548">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9544d-549">لا</span><span class="sxs-lookup"><span data-stu-id="9544d-549">No</span></span></td>
<td><span data-ttu-id="9544d-550">راجع الصف السابق.</span><span class="sxs-lookup"><span data-stu-id="9544d-550">See the previous row.</span></span></td>
<td><span data-ttu-id="9544d-551">راجع الصف السابق.</span><span class="sxs-lookup"><span data-stu-id="9544d-551">See the previous row.</span></span></td>
<td><span data-ttu-id="9544d-552">يتم أعاده حجز الكمية لنفس المجموعة ، وللوح الموقع والترخيص الذي تم فيه ترك الكمية عند إلغاء.</span><span class="sxs-lookup"><span data-stu-id="9544d-552">The quantity is re-reserved for the same batch, and for the location and license plate where the quantity was left upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9544d-553">‏‏نعم</span><span class="sxs-lookup"><span data-stu-id="9544d-553">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="9544d-554">افتح صفحه <strong>العمل العكسي</strong>.</span><span class="sxs-lookup"><span data-stu-id="9544d-554">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="9544d-555">في الصفحة طلب ، حدد الخيار <strong>تعيين العناصر للموقع الحالي</strong>.</span><span class="sxs-lookup"><span data-stu-id="9544d-555">On the request page, select the <strong>Assign items to this location</strong> option.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="9544d-556">تم إلغاء العمل الحالي.</span><span class="sxs-lookup"><span data-stu-id="9544d-556">The current work is canceled.</span></span></li>
<li><span data-ttu-id="9544d-557">يتم إنشاء العمل الجديد لحركة المخزون وإغلاقه.</span><span class="sxs-lookup"><span data-stu-id="9544d-557">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="9544d-558">تمت إعاده حجز الكمية لنفس المجموعة.</span><span class="sxs-lookup"><span data-stu-id="9544d-558">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="9544d-559">يقوم النظام بتعيين الموقع ولوحه الترخيص عشوائيا (إذا كان الموقع لوحه ترخيص – يتم التحكم به) حيث تكون الكمية متاحه.</span><span class="sxs-lookup"><span data-stu-id="9544d-559">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9544d-560">لا</span><span class="sxs-lookup"><span data-stu-id="9544d-560">No</span></span></td>
<td><span data-ttu-id="9544d-561">راجع الصف السابق.</span><span class="sxs-lookup"><span data-stu-id="9544d-561">See the previous row.</span></span></td>
<td><span data-ttu-id="9544d-562">راجع الصف السابق.</span><span class="sxs-lookup"><span data-stu-id="9544d-562">See the previous row.</span></span></td>
<td><span data-ttu-id="9544d-563">يتم أعاده حجز الكمية لنفس المجموعة ، وللوح الموقع والترخيص الذي تم فيه تعيين الكمية عند إلغاء.</span><span class="sxs-lookup"><span data-stu-id="9544d-563">The quantity is re-reserved for the same batch, and for the location and license plate that the quantity was assigned to upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9544d-564">نعم/لا</span><span class="sxs-lookup"><span data-stu-id="9544d-564">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="9544d-565">افتح صفحه <strong>العمل العكسي</strong>.</span><span class="sxs-lookup"><span data-stu-id="9544d-565">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="9544d-566">في الصفحة طلب ، حدد الخيار <strong>نقل العناصر إلى هذا الموقع</strong>.</span><span class="sxs-lookup"><span data-stu-id="9544d-566">On the request page, select the <strong>Move items to this location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="9544d-567">العكس غير معتمد.</span><span class="sxs-lookup"><span data-stu-id="9544d-567">Reversal isn't supported.</span></span></td>
<td><span data-ttu-id="9544d-568">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="9544d-568">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9544d-569">نعم/لا</span><span class="sxs-lookup"><span data-stu-id="9544d-569">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="9544d-570">افتح صفحه <strong>العمل العكسي</strong>.</span><span class="sxs-lookup"><span data-stu-id="9544d-570">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="9544d-571">في الصفحة طلب ، حدد الخيار <strong>نقل العناصر على أساس موجهات الموقع</strong>.</span><span class="sxs-lookup"><span data-stu-id="9544d-571">On the request page, select the <strong>Move items based on location directives</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="9544d-572">العكس غير معتمد.</span><span class="sxs-lookup"><span data-stu-id="9544d-572">Reversal isn't supported.</span></span> </td>
<td><span data-ttu-id="9544d-573">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="9544d-573">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a><span data-ttu-id="9544d-574">قصور انتقاء الكمية – تسجيل الكمية بأنها لم يتم العثور عليها فعليا في لوحه الترخيص/الموقع اثناء إجراء عمل الانتقاء</span><span class="sxs-lookup"><span data-stu-id="9544d-574">Short-pick a quantity – Register the quantity as physically not found at the location/license plate while you perform picking work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9544d-575">معلمة الإعداد الرئيسية</span><span class="sxs-lookup"><span data-stu-id="9544d-575">Key setup parameter</span></span></th>
<th><span data-ttu-id="9544d-576">كمية الدفعة متاحة</span><span class="sxs-lookup"><span data-stu-id="9544d-576">Batch quantity is available</span></span></th>
<th><span data-ttu-id="9544d-577">خطوات المستخدم الاساسيه</span><span class="sxs-lookup"><span data-stu-id="9544d-577">Key user steps</span></span></th>
<th><span data-ttu-id="9544d-578">عمل المستودع</span><span class="sxs-lookup"><span data-stu-id="9544d-578">Warehouse work</span></span></th>
<th><span data-ttu-id="9544d-579">حجز المجموعة المرتبطة بالأمر</span><span class="sxs-lookup"><span data-stu-id="9544d-579">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="9544d-580">تم إعداد استثناء عمل لنوع <strong>الانتقاء القصير</strong> حيث <strong>إعادة توزيع الصنف</strong> = <strong>لا شيء</strong> و <strong>وتسوية المخزون</strong> = <strong>نعم</strong> و <strong>إزالة عمليات الحجز</strong> = <strong>لا</strong>.</span><span class="sxs-lookup"><span data-stu-id="9544d-580">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span></td>
<td><span data-ttu-id="9544d-581">نعم</span><span class="sxs-lookup"><span data-stu-id="9544d-581">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="9544d-582">حدد عنصر القائمة <strong>Shortpick</strong> في تطبيق إدارة المستودع للأجهزة المحمولة عند معالجة عمل الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="9544d-582">Select the <strong>Shortpick</strong> menu item on the Warehouse Management mobile app when you run picking work.</span></span></li>
<li><span data-ttu-id="9544d-583">في حقل <strong>كمية الانتقاء</strong>، أدخل <strong>0</strong> (صفرًا).</span><span class="sxs-lookup"><span data-stu-id="9544d-583">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="9544d-584">في حقل <strong>السبب</strong>، أدخل <strong>لا توجد إعادة توزيع</strong>.</span><span class="sxs-lookup"><span data-stu-id="9544d-584">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="9544d-585">يتم إغلاق العمل الحالي، وتكون الكمية المنتقاة هي 0 (صفر).</span><span class="sxs-lookup"><span data-stu-id="9544d-585">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="9544d-586">يتم إنشاء حركه مخزون لنوع <strong>الجرد</strong>  ونوع الإصدار <strong>مباع</strong> ليمثل التعديل.</span><span class="sxs-lookup"><span data-stu-id="9544d-586">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="9544d-587">تمت إعاده حجز الكمية لنفس المجموعة.</span><span class="sxs-lookup"><span data-stu-id="9544d-587">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="9544d-588">يقوم النظام بتعيين الموقع ولوحه الترخيص عشوائيا (إذا كان الموقع لوحه ترخيص – يتم التحكم به) حيث تكون الكمية متاحه.</span><span class="sxs-lookup"><span data-stu-id="9544d-588">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9544d-589">لا</span><span class="sxs-lookup"><span data-stu-id="9544d-589">No</span></span></td>
<td><span data-ttu-id="9544d-590">راجع الصف السابق.</span><span class="sxs-lookup"><span data-stu-id="9544d-590">See the previous row.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="9544d-591">فشل إجراء الانتقاء القصير، ويتم عرض خطأ.</span><span class="sxs-lookup"><span data-stu-id="9544d-591">The short-picking action fails, and an error is thrown.</span></span></li>
<li><span data-ttu-id="9544d-592">يظل العمل الحالي مفتوحا.</span><span class="sxs-lookup"><span data-stu-id="9544d-592">The current work remains open.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="9544d-593">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="9544d-593">Not applicable</span></span></td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="9544d-594">تم إعداد استثناء عمل لنوع <strong>الانتقاء القصير</strong> حيث <strong>إعادة توزيع الصنف</strong> = <strong>‎لا شيء</strong>، و <strong>تسوية المخزون</strong> = <strong>نعم</strong>، و <strong>‎إزالة عمليات الحجوزات</strong> = <strong>نعم</strong>.</span><span class="sxs-lookup"><span data-stu-id="9544d-594">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span></td>
<td><span data-ttu-id="9544d-595">نعم</span><span class="sxs-lookup"><span data-stu-id="9544d-595">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="9544d-596">حدد عنصر القائمة <strong>Shortpick</strong> في تطبيق إدارة المستودع للأجهزة المحمولة عند معالجة عمل الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="9544d-596">Select the <strong>Shortpick</strong> menu item on the Warehouse Management mobile app when you run picking work.</span></span></li>
<li><span data-ttu-id="9544d-597">في حقل <strong>كمية الانتقاء</strong>، أدخل <strong>0</strong> (صفرًا).</span><span class="sxs-lookup"><span data-stu-id="9544d-597">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="9544d-598">في حقل <strong>السبب</strong>، أدخل <strong>لا توجد إعادة توزيع</strong>.</span><span class="sxs-lookup"><span data-stu-id="9544d-598">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="9544d-599">يتم إغلاق العمل الحالي، وتكون الكمية المنتقاة هي 0 (صفر).</span><span class="sxs-lookup"><span data-stu-id="9544d-599">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="9544d-600">يتم إنشاء حركه مخزون لنوع <strong>الجرد</strong>  ونوع الإصدار <strong>مباع</strong> ليمثل التعديل.</span><span class="sxs-lookup"><span data-stu-id="9544d-600">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="9544d-601">تتم أعاده حجز كافة عمليات الحجز الموجودة التي تاثرت بتسوية الكمية في موقع الانتقاء القصير المعاد حجزه لنفس المجموعة.</span><span class="sxs-lookup"><span data-stu-id="9544d-601">All existing reservations that are affected by the quantity adjustment in the short-picked location are re-reserved for the same batch.</span></span> <span data-ttu-id="9544d-602">يقوم النظام بتعيين الموقع ولوحه الترخيص عشوائيا (إذا كان الموقع لوحه ترخيص – يتم التحكم به) حيث تكون الكمية متاحه.</span><span class="sxs-lookup"><span data-stu-id="9544d-602">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9544d-603">لا</span><span class="sxs-lookup"><span data-stu-id="9544d-603">No</span></span></td>
<td><span data-ttu-id="9544d-604">راجع الصف السابق.</span><span class="sxs-lookup"><span data-stu-id="9544d-604">See the previous row.</span></span></td>
<td><span data-ttu-id="9544d-605">راجع الصف السابق.</span><span class="sxs-lookup"><span data-stu-id="9544d-605">See the previous row.</span></span></td>
<td><span data-ttu-id="9544d-606">تمت إزالة جميع الحجوزات الحالية المتأثرة بتسوية الكمية في موقع الانتقاء القصير.</span><span class="sxs-lookup"><span data-stu-id="9544d-606">All existing reservations that are affected by the quantity adjustment in the short-picked location are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9544d-607">تم إعداد استثناء عمل لنوع <strong>الانتقاء القصير</strong> حيث <strong>إعادة توزيع الصنف</strong> = <strong>يدوي</strong>، و <strong>تسوية المخزون</strong> = <strong>نعم</strong>, و <strong>‎إزالة عمليات الحجوزات</strong> = <strong>لا/نعم</strong>.</span><span class="sxs-lookup"><span data-stu-id="9544d-607">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No/Yes</strong>.</span></span> <span data-ttu-id="9544d-608">بالإضافة إلى ذلك ، يتم تمكين الخيار <strong>السماح بإعادة توزيع العناصر اليدوية</strong> علي العامل.</span><span class="sxs-lookup"><span data-stu-id="9544d-608">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="9544d-609">نعم</span><span class="sxs-lookup"><span data-stu-id="9544d-609">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="9544d-610">حدد عنصر القائمة <strong>Shortpick</strong> في تطبيق إدارة المستودع للأجهزة المحمولة عند معالجة عمل الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="9544d-610">Select the <strong>Shortpick</strong> menu item on the Warehouse Management mobile app when you run picking work.</span></span></li>
<li><span data-ttu-id="9544d-611">في حقل <strong>كمية الانتقاء القصير</strong>، أدخل <strong>0</strong> (صفرًا).</span><span class="sxs-lookup"><span data-stu-id="9544d-611">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="9544d-612">في الحقل <strong>السبب</strong>، حدد<strong>الانتقاء القصير مع إعادة التوزيع اليدوية</strong>.</span><span class="sxs-lookup"><span data-stu-id="9544d-612">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="9544d-613">حدد لوحه الترخيص/الموقع في القائمة.</span><span class="sxs-lookup"><span data-stu-id="9544d-613">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="9544d-614">تحدث الإجراءات التالية في العمل الحالي:</span><span class="sxs-lookup"><span data-stu-id="9544d-614">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="9544d-615">يتم إغلاق بند الانتقاء، وتكون الكمية المنتقاة هي 0 (صفر).</span><span class="sxs-lookup"><span data-stu-id="9544d-615">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="9544d-616">تم إلغاء بند الإدخال.</span><span class="sxs-lookup"><span data-stu-id="9544d-616">The put line is canceled.</span></span></li>
<li><span data-ttu-id="9544d-617">يتم إنشاء بند انتقاء جديد.</span><span class="sxs-lookup"><span data-stu-id="9544d-617">A new pick line is created.</span></span> <span data-ttu-id="9544d-618">ويستخدم الموقع/لوحه الترخيص التي قام المستخدم بتحديدها.</span><span class="sxs-lookup"><span data-stu-id="9544d-618">It uses the location/license plate that the user selected.</span></span></li>
<li><span data-ttu-id="9544d-619">يتم إنشاء بند إدخال جديد.</span><span class="sxs-lookup"><span data-stu-id="9544d-619">A new put line is created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="9544d-620">يتم إنشاء حركه مخزون لنوع <strong>الجرد</strong>  ونوع الإصدار <strong>مباع</strong> ليمثل التعديل.</span><span class="sxs-lookup"><span data-stu-id="9544d-620">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="9544d-621">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="9544d-621">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9544d-622">تم إعداد استثناء عمل لنوع <strong>الانتقاء القصير</strong> حيث <strong>إعادة توزيع الصنف</strong> = <strong>يدوي</strong> و <strong>تسوية المخزون</strong> = <strong>نعم</strong> و <strong>إزالة عمليات الحجوزات</strong> = <strong>لا</strong>.</span><span class="sxs-lookup"><span data-stu-id="9544d-622">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span> <span data-ttu-id="9544d-623">بالإضافة إلى ذلك ، يتم تمكين الخيار <strong>السماح بإعادة توزيع العناصر اليدوية</strong> علي العامل.</span><span class="sxs-lookup"><span data-stu-id="9544d-623">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="9544d-624">لا</span><span class="sxs-lookup"><span data-stu-id="9544d-624">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="9544d-625">حدد عنصر القائمة <strong>Shortpick</strong> في تطبيق إدارة المستودع للأجهزة المحمولة عند معالجة عمل الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="9544d-625">Select the <strong>Shortpick</strong> menu item on the Warehouse Management mobile app when you run picking work.</span></span></li>
<li><span data-ttu-id="9544d-626">في حقل <strong>كمية الانتقاء القصير</strong>، أدخل <strong>0</strong> (صفرًا).</span><span class="sxs-lookup"><span data-stu-id="9544d-626">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="9544d-627">في الحقل <strong>السبب</strong>، حدد<strong>الانتقاء القصير مع إعادة التوزيع اليدوية</strong>.</span><span class="sxs-lookup"><span data-stu-id="9544d-627">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="9544d-628">فشل إجراء الانتقاء القصير، ويتم عرض خطأ.</span><span class="sxs-lookup"><span data-stu-id="9544d-628">The short-picking action fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="9544d-629">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="9544d-629">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9544d-630">تم إعداد استثناء عمل لنوع <strong>الانتقاء القصير</strong> حيث <strong>إعادة توزيع الصنف</strong> = <strong>يدوي</strong> و <strong>تسوية المخزون</strong> = <strong>نعم</strong> و <strong>إزالة عمليات الحجوزات</strong> = <strong>نعم</strong>.</span><span class="sxs-lookup"><span data-stu-id="9544d-630">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span> <span data-ttu-id="9544d-631">بالإضافة إلى ذلك ، يتم تمكين الخيار <strong>السماح بإعادة توزيع العناصر اليدوية</strong> علي العامل.</span><span class="sxs-lookup"><span data-stu-id="9544d-631">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="9544d-632">لا</span><span class="sxs-lookup"><span data-stu-id="9544d-632">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="9544d-633">حدد عنصر القائمة <strong>Shortpick</strong> في تطبيق إدارة المستودع للأجهزة المحمولة عند معالجة عمل الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="9544d-633">Select the <strong>Shortpick</strong> menu item on the Warehouse Management mobile app when you run picking work.</span></span></li>
<li><span data-ttu-id="9544d-634">في حقل <strong>كمية الانتقاء القصير</strong>، أدخل <strong>0</strong> (صفرًا).</span><span class="sxs-lookup"><span data-stu-id="9544d-634">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="9544d-635">في الحقل <strong>السبب</strong>، حدد<strong>الانتقاء القصير مع إعادة التوزيع اليدوية</strong>.</span><span class="sxs-lookup"><span data-stu-id="9544d-635">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="9544d-636">حدد لوحه الترخيص/الموقع في القائمة.</span><span class="sxs-lookup"><span data-stu-id="9544d-636">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="9544d-637">تحدث الإجراءات التالية في العمل الحالي:</span><span class="sxs-lookup"><span data-stu-id="9544d-637">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="9544d-638">يتم إغلاق بند الانتقاء، وتكون الكمية المنتقاة هي 0 (صفر).</span><span class="sxs-lookup"><span data-stu-id="9544d-638">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="9544d-639">تم إلغاء بند الإدخال.</span><span class="sxs-lookup"><span data-stu-id="9544d-639">The put line is canceled.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="9544d-640">يتم إنشاء حركه مخزون لنوع <strong>الجرد</strong>  ونوع الإصدار <strong>مباع</strong> ليمثل التعديل.</span><span class="sxs-lookup"><span data-stu-id="9544d-640">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="9544d-641">تمت إزالة جميع الحجوزات الحالية المتأثرة بتسوية الكمية في موقع/لوحة ترخيص الانتقاء القصير.</span><span class="sxs-lookup"><span data-stu-id="9544d-641">All existing reservations that are affected by the quantity adjustment in the short-picked location/license plate are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9544d-642">تم إعداد استثناء عمل لنوع <strong>الانتقاء القصير</strong> حيث <strong>إعادة توزيع الصنف</strong> = <strong>تلقائي</strong> و <strong>تسوية المخزون</strong> = <strong>نعم/لا</strong> و <strong>‎إزالة عمليات الحجوزات</strong> = <strong>نعم/لا</strong>.</span><span class="sxs-lookup"><span data-stu-id="9544d-642">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Automatic</strong>, <strong>Adjust inventory</strong> = <strong>Yes/No</strong>, and <strong>Remove reservations</strong> = <strong>Yes/No</strong>.</span></span></td>
<td><span data-ttu-id="9544d-643">غير قابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="9544d-643">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="9544d-644">حدد عنصر القائمة <strong>Shortpick</strong> في تطبيق إدارة المستودع للأجهزة المحمولة عند معالجة عمل الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="9544d-644">Select the <strong>Shortpick</strong> menu item on the Warehouse Management mobile app when you run picking work.</span></span></li>
<li><span data-ttu-id="9544d-645">في حقل <strong>كمية الانتقاء القصير</strong>، أدخل <strong>0</strong> (صفرًا).</span><span class="sxs-lookup"><span data-stu-id="9544d-645">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="9544d-646">في الحقل <strong>السبب</strong>، حدد<strong>الانتقاء القصير مع إعادة التوزيع التلقائية</strong>.</span><span class="sxs-lookup"><span data-stu-id="9544d-646">In the <strong>Reason</strong> field, select <strong>Short Picking with automatic reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="9544d-647">الانتقاء القصير الذي يتضمن إعادة التوزيع تلقائيا غير مدعوم.</span><span class="sxs-lookup"><span data-stu-id="9544d-647">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
<td><span data-ttu-id="9544d-648">الانتقاء القصير الذي يتضمن إعادة التوزيع تلقائيا غير مدعوم.</span><span class="sxs-lookup"><span data-stu-id="9544d-648">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a><span data-ttu-id="9544d-649">تغيير حالة المخزون</span><span class="sxs-lookup"><span data-stu-id="9544d-649">Change the inventory status</span></span>

> [!NOTE]
> <span data-ttu-id="9544d-650">يمكن تنفيذ إجراء المستودع هذا من نقاط إدخال متعددة.</span><span class="sxs-lookup"><span data-stu-id="9544d-650">This warehouse action can be performed from multiple entry points.</span></span> <span data-ttu-id="9544d-651">يستخدم المثال الموضح هنا إجراء **تغيير حالة المخزون** في الصفحة **الفعلية حسب الموقع**</span><span class="sxs-lookup"><span data-stu-id="9544d-651">The example that is shown here uses **Inventory status change** action on the **On-hand by location** page.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9544d-652">معلمة الإعداد الرئيسية</span><span class="sxs-lookup"><span data-stu-id="9544d-652">Key setup parameter</span></span></th>
<th><span data-ttu-id="9544d-653">كمية الدفعة متاحة</span><span class="sxs-lookup"><span data-stu-id="9544d-653">Batch quantity is available</span></span></th>
<th><span data-ttu-id="9544d-654">خطوات المستخدم الاساسيه</span><span class="sxs-lookup"><span data-stu-id="9544d-654">Key user steps</span></span></th>
<th><span data-ttu-id="9544d-655">عمل المستودع</span><span class="sxs-lookup"><span data-stu-id="9544d-655">Warehouse work</span></span></th>
<th><span data-ttu-id="9544d-656">حجز المجموعة المرتبطة بالأمر</span><span class="sxs-lookup"><span data-stu-id="9544d-656">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="9544d-657">في علامة التبويب<strong> المستودع</strong>، في سجل <strong> المستودع</strong> ، يتم تعيين الحقل<strong> حجوزات الازاله والعلامات</strong> إلى <strong>عمليات الحجز</strong> أو <strong>العلامات والحجوزات.</strong></span><span class="sxs-lookup"><span data-stu-id="9544d-657">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>Reservations</strong> or <strong>Markings and reservations</strong>.</span></span></td>
<td><span data-ttu-id="9544d-658">‏‏نعم</span><span class="sxs-lookup"><span data-stu-id="9544d-658">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="9544d-659">حدد موقعًا معينًا.</span><span class="sxs-lookup"><span data-stu-id="9544d-659">Select a specific location.</span></span></li>
<li><span data-ttu-id="9544d-660">حدد البند الذي يحتوي علي أحد الأصناف والمواقع والتراخيص المحددة (إذا كان الموقع لوحه ترخيص – يتم التحكم به).</span><span class="sxs-lookup"><span data-stu-id="9544d-660">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="9544d-661">حدد <strong>تغيير حالة المخزون</strong>.</span><span class="sxs-lookup"><span data-stu-id="9544d-661">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="9544d-662">قم بتعيين حقل <strong>حالة المخزون</strong> إلى <strong>"تجميد</strong>".</span><span class="sxs-lookup"><span data-stu-id="9544d-662">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="9544d-663">لا يسمح بإجراء تغييرات علي حالة المخزون للكميات المحجوزة للعمل.</span><span class="sxs-lookup"><span data-stu-id="9544d-663">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="9544d-664">تمت إعاده حجز الكمية لنفس المجموعة.</span><span class="sxs-lookup"><span data-stu-id="9544d-664">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="9544d-665">يقوم النظام بتعيين الموقع ولوحه الترخيص عشوائيا (إذا كان الموقع لوحه ترخيص – يتم التحكم به) حيث تكون الكمية متاحه.</span><span class="sxs-lookup"><span data-stu-id="9544d-665">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></li>
<li><span data-ttu-id="9544d-666">يتم إنشاء حركتي مخزون بنوع <strong>تغيير حالة المخزون</strong> لتمثيل التغيير في بعد حالة المخزون.</span><span class="sxs-lookup"><span data-stu-id="9544d-666">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="9544d-667">يتم إنشاء حركه مخزون لنوع <strong>تامين المخزون</strong> ونوع الإصدار <strong>الفعلي المحجوز</strong> لتمثيل حجز الكمية المحظورة.</span><span class="sxs-lookup"><span data-stu-id="9544d-667">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="9544d-668">لا</span><span class="sxs-lookup"><span data-stu-id="9544d-668">No</span></span></td>
<td><span data-ttu-id="9544d-669">راجع الصف السابق.</span><span class="sxs-lookup"><span data-stu-id="9544d-669">See the previous row.</span></span></td>
<td><span data-ttu-id="9544d-670">لا يسمح بإجراء تغييرات علي حالة المخزون للكميات المحجوزة للعمل.</span><span class="sxs-lookup"><span data-stu-id="9544d-670">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="9544d-671">تمت إزاله الحجز.</span><span class="sxs-lookup"><span data-stu-id="9544d-671">The reservation is removed.</span></span></li>
<li><span data-ttu-id="9544d-672">يتم إنشاء حركتي مخزون بنوع <strong>تغيير حالة المخزون</strong> لتمثيل التغيير في بعد حالة المخزون.</span><span class="sxs-lookup"><span data-stu-id="9544d-672">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="9544d-673">يتم إنشاء حركه مخزون لنوع <strong>تامين المخزون</strong> ونوع الإصدار <strong>الفعلي المحجوز</strong> لتمثيل حجز الكمية المحظورة.</span><span class="sxs-lookup"><span data-stu-id="9544d-673">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="9544d-674">في علامة التبويب <strong>المستودع</strong>، في سجل <strong>المستودع</strong>، يتم تعيين الحقل <strong>حجوزات الازاله والعلامات</strong> إلى <strong>لا شيء</strong>.</span><span class="sxs-lookup"><span data-stu-id="9544d-674">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>None</strong>.</span></span></td>
<td><span data-ttu-id="9544d-675">‏‏نعم</span><span class="sxs-lookup"><span data-stu-id="9544d-675">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="9544d-676">حدد موقعًا معينًا.</span><span class="sxs-lookup"><span data-stu-id="9544d-676">Select a specific location.</span></span></li>
<li><span data-ttu-id="9544d-677">حدد البند الذي يحتوي علي أحد الأصناف والمواقع والتراخيص المحددة (إذا كان الموقع لوحه ترخيص – يتم التحكم به).</span><span class="sxs-lookup"><span data-stu-id="9544d-677">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="9544d-678">حدد <strong>تغيير حالة المخزون</strong>.</span><span class="sxs-lookup"><span data-stu-id="9544d-678">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="9544d-679">قم بتعيين حقل <strong>حالة المخزون</strong> إلى <strong>"تجميد</strong>".</span><span class="sxs-lookup"><span data-stu-id="9544d-679">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="9544d-680">لا يسمح بإجراء تغييرات علي حالة المخزون للكميات المحجوزة للعمل.</span><span class="sxs-lookup"><span data-stu-id="9544d-680">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="9544d-681">تمت إعاده حجز الكمية لنفس المجموعة.</span><span class="sxs-lookup"><span data-stu-id="9544d-681">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="9544d-682">يقوم النظام بتعيين الموقع ولوحه الترخيص عشوائيا (إذا كان الموقع لوحه ترخيص – يتم التحكم به) حيث تكون الكمية متاحه.</span><span class="sxs-lookup"><span data-stu-id="9544d-682">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9544d-683">لا</span><span class="sxs-lookup"><span data-stu-id="9544d-683">No</span></span></td>
<td><span data-ttu-id="9544d-684">راجع الصف السابق.</span><span class="sxs-lookup"><span data-stu-id="9544d-684">See the previous row.</span></span></td>
<td><span data-ttu-id="9544d-685">لا يسمح بإجراء تغييرات علي حالة المخزون للكميات المحجوزة للعمل.</span><span class="sxs-lookup"><span data-stu-id="9544d-685">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="9544d-686">لا يسمح بتغييرات حالة المخزون.</span><span class="sxs-lookup"><span data-stu-id="9544d-686">Inventory status changes aren't allowed.</span></span></td>
</tr>
</tbody>
</table>

## <a name="limitations"></a><span data-ttu-id="9544d-687">قيود</span><span class="sxs-lookup"><span data-stu-id="9544d-687">Limitations</span></span>

- <span data-ttu-id="9544d-688">لا تدعم وظيفة حجز بعد علي مستوي المستودع المرن الميزات التالية:</span><span class="sxs-lookup"><span data-stu-id="9544d-688">The flexible warehouse-level dimension reservation functionality doesn't support the following features:</span></span>

    - <span data-ttu-id="9544d-689">أداره وزن التقاط</span><span class="sxs-lookup"><span data-stu-id="9544d-689">Catch weight management</span></span>
    - <span data-ttu-id="9544d-690">مخزون سالب مادي</span><span class="sxs-lookup"><span data-stu-id="9544d-690">Physical negative inventory</span></span>
    - <span data-ttu-id="9544d-691">الحجز مقابل التوريد المطلوب</span><span class="sxs-lookup"><span data-stu-id="9544d-691">Reservation against ordered supply</span></span>
    - <span data-ttu-id="9544d-692">أوامر التحويل وانتقاء المادة الخام</span><span class="sxs-lookup"><span data-stu-id="9544d-692">Transfer orders and raw material picking</span></span>

- <span data-ttu-id="9544d-693">تشتمل قاعده دمج الحاوية للتعبئة حسب الوحدة الموجهة عليها علي قيود.</span><span class="sxs-lookup"><span data-stu-id="9544d-693">The container consolidation rule for packing by directive unit has limitations.</span></span> <span data-ttu-id="9544d-694">بالنسبة لعمليات الحجز المرتبطة بالطلبات ، نوصي بعدم استخدام قوالب بنيه الحاوية حيث تم تمكين الحزم حسب حقل **الوحدة الموجهة**.</span><span class="sxs-lookup"><span data-stu-id="9544d-694">For order-committed reservations, we recommend that you not use container build templates where the **Pack by directive unit** field is enabled.</span></span> <span data-ttu-id="9544d-695">في التصميم الحالي ، لا يتم استخدام توجيهات المواقع عند إنشاء عمل المستودع.</span><span class="sxs-lookup"><span data-stu-id="9544d-695">In the current design, location directives aren't used when warehouse work is created.</span></span> <span data-ttu-id="9544d-696">وبالتالي، يتم تطبيق أدنى وحدة في مجموعة تسلسل الوحدة (وحدة المخزون) اثناء خطوة الموجة التعبئة في الحاويات.</span><span class="sxs-lookup"><span data-stu-id="9544d-696">Therefore, only the lowest unit in the unit sequence group (the inventory unit) is applied during the containerization wave step.</span></span>

## <a name="see-also"></a><span data-ttu-id="9544d-697">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="9544d-697">See also</span></span>

- [<span data-ttu-id="9544d-698">أرقام الدُفعات في إدارة المستودعات</span><span class="sxs-lookup"><span data-stu-id="9544d-698">Batch numbers in Warehouse management</span></span>](/dynamicsax-2012/appuser-itpro/batch-numbers-in-warehouse-management)
- [<span data-ttu-id="9544d-699">حجز نفس الدُفعة لأمر مبيعات</span><span class="sxs-lookup"><span data-stu-id="9544d-699">Reserve the same batch for a sales order</span></span>](../sales-marketing/reserve-same-batch-sales-order.md)
- [<span data-ttu-id="9544d-700">انتقاء الدُفعة الأقدم على جهاز محمول</span><span class="sxs-lookup"><span data-stu-id="9544d-700">Pick oldest batch on a mobile device</span></span>](pick-oldest-batch.md)
- [<span data-ttu-id="9544d-701">تأكيد لوحة الترخيص والدُفعة</span><span class="sxs-lookup"><span data-stu-id="9544d-701">Batch and license plate confirmation</span></span>](batch-and-license-plate-confirmation.md)
- [<span data-ttu-id="9544d-702">استكشاف الأخطاء في عمليات الحجز بإدارة المستودعات وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="9544d-702">Troubleshoot reservations in warehouse management</span></span>](troubleshoot-warehouse-reservations.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]