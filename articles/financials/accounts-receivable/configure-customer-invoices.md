---
title: "إنشاء فاتورة عميل"
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 77772
ms.assetid: 00b4b40c-1576-4098-9aed-ac376fdeb8c5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2a668e390935e157d9fc7f0ef597f25c2a7b9950
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---

# <a name="create-a-customer-invoice"></a><span data-ttu-id="58f36-102">إنشاء فاتورة عميل</span><span class="sxs-lookup"><span data-stu-id="58f36-102">Create a customer invoice</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="58f36-103">**فاتورة عميل لأمر المبيعات** هي فاتورة ترتبط بعملية بيع وتعطيها مؤسسة لعميل.</span><span class="sxs-lookup"><span data-stu-id="58f36-103">A **customer invoice for a sales order** is a bill that is related to a sale, and that an organization gives to a customer.</span></span> <span data-ttu-id="58f36-104">ويتم إنشاء هذا النوع من فاتورة العميل استنادًا إلى أمر المبيعات، الذي يتضمن بنود الأوامر وأرقام الأصناف.</span><span class="sxs-lookup"><span data-stu-id="58f36-104">This type of customer invoice is created based on a sales order, which includes order lines and item numbers.</span></span> <span data-ttu-id="58f36-105">ويتم تحديد أرقام الأصناف وترحيلها في دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="58f36-105">Item numbers are specified and posted in the ledger.</span></span> <span data-ttu-id="58f36-106">ولا تتوفر إدخالات دفتر اليومية في دفتر الأستاذ الفرعي لفاتورة عميل لأمر مبيعات.‬</span><span class="sxs-lookup"><span data-stu-id="58f36-106">Subledger journal entries aren't available for a customer invoice for a sales order.</span></span> <span data-ttu-id="58f36-107">للحصول على مزيد من المعلومات، راجع [إنشاء فواتير أوامر المبيعات‬](tasks/create-sales-order-invoices.md).</span><span class="sxs-lookup"><span data-stu-id="58f36-107">For more information, see [Create sales order invoices](tasks/create-sales-order-invoices.md).</span></span>

<span data-ttu-id="58f36-108">ولا ترتبط **فاتورة النص الحر** بأمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="58f36-108">A **free text invoice** isn't related to a sales order.</span></span> <span data-ttu-id="58f36-109">ولكنها تحتوي على بنود الأمر التي تتضمن حسابات دفتر الأستاذ وأوصاف النص الحر ومبلغ المبيعات الذي تقوم بإدخاله.</span><span class="sxs-lookup"><span data-stu-id="58f36-109">It contains order lines that include ledger accounts, free-text descriptions, and a sales amount that you enter.</span></span> <span data-ttu-id="58f36-110">ولا يمكنك إدخال رقم الصنف في نوع الفاتورة هذا.</span><span class="sxs-lookup"><span data-stu-id="58f36-110">You can't enter an item number on this kind of invoice.</span></span> <span data-ttu-id="58f36-111">يجب إدخال معلومات ضريبة المبيعات الصحيحة.</span><span class="sxs-lookup"><span data-stu-id="58f36-111">You must enter the appropriate sales tax information.</span></span> <span data-ttu-id="58f36-112">وتتم الإشارة إلى حساب رئيسي للبيع في كل بند فاتورة تقوم بتوزيعها على عدة حسابات دفتر أستاذ بالنقر فوق **توزيع المبالغ** في صفحة **فاتورة النص الحر**.</span><span class="sxs-lookup"><span data-stu-id="58f36-112">A main account for the sale is indicated on each invoice line, which you can distribute to multiple ledger accounts by clicking **Distribute amounts** on the **Free text invoice** page.</span></span> <span data-ttu-id="58f36-113">وبالإضافة إلى ذلك، يتم ترحيل رصيد العميل إلى حساب الملخص من ملف تعريف الترحيل المستخدم لفاتورة النص الحر.</span><span class="sxs-lookup"><span data-stu-id="58f36-113">Additionally, the customer balance is posted to the summary account from the posting profile that is used for the free text invoice.</span></span>

<span data-ttu-id="58f36-114">لمزيد من المعلومات، راجع: </span><span class="sxs-lookup"><span data-stu-id="58f36-114">For more information see:</span></span>

[<span data-ttu-id="58f36-115">إنشاء فاتورة نص حر</span><span class="sxs-lookup"><span data-stu-id="58f36-115">Create a free text invoice</span></span>](tasks/create-free-text-invoice.md)

[<span data-ttu-id="58f36-116">إنشاء قالب نص حر</span><span class="sxs-lookup"><span data-stu-id="58f36-116">Create a free text template</span></span>](tasks/create-free-text-invoice-template.md)

[<span data-ttu-id="58f36-117">‏‫تعيين قالب فاتورة ذات نص حر إلى عميل</span><span class="sxs-lookup"><span data-stu-id="58f36-117">Assign a free text invoice tempate to a customer</span></span>](tasks/assign-free-text-invoice-template-customer.md)

[<span data-ttu-id="58f36-118">إنشاء وترحيل فواتير النص الحر المكررة</span><span class="sxs-lookup"><span data-stu-id="58f36-118">Generate and post recurring free text invoices</span></span>](tasks/post-recurring-free-text-invoices.md)


<span data-ttu-id="58f36-119">**الفاتورة المبدئية** هي فاتورة يتم إعدادها كتقدير لمبالغ الفاتورة الفعلية قبل ترحيل الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="58f36-119">A **pro forma invoice** is an invoice that is prepared as an estimate of the actual invoice amounts before the invoice is posted.</span></span> <span data-ttu-id="58f36-120">ويمكنك طباعة فاتورة مبدئية لفاتورة عميل لفاتورة مبيعات أو لفاتورة النص الحر.</span><span class="sxs-lookup"><span data-stu-id="58f36-120">You can print a pro forma invoice either for a customer invoice for a sales order or for a free text invoice.</span></span>

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-sales-orders"></a><span data-ttu-id="58f36-121">ترحيل وطباعة فواتير عملاء فردية استناداً إلى أوامر التوريد</span><span class="sxs-lookup"><span data-stu-id="58f36-121">Post and print individual customer invoices that are based on sales orders</span></span>
<span data-ttu-id="58f36-122">استخدم هذا العملية لإنشاء فاتورة تستند إلى أمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="58f36-122">Use this process to create an invoice that is based on a sales order.</span></span> <span data-ttu-id="58f36-123">ويمكنك القيام بذلك إذا قررت عمل فاتورة للعميل قبل تسليم السلع أو الخدمات.</span><span class="sxs-lookup"><span data-stu-id="58f36-123">You might do this if you decide to invoice the customer before you deliver the goods or services.</span></span> 

<span data-ttu-id="58f36-124">عندما تقوم بترحيل الفاتورة، يتم تحديث كمية **باقي الفاتورة** لكل صنف من خلال إجمالي الكميات التي تمت فوترتها من أمر الشراء المحدد.</span><span class="sxs-lookup"><span data-stu-id="58f36-124">When you post an invoice, the **Invoice remainder** quantity for each item is updated with the total of the invoiced quantities from the selected sales order.</span></span> <span data-ttu-id="58f36-125">وإذا كان كلُّ من كمية **باقي الفاتورة** وكمية **تسليم البافي**لكافة الأصناف في أمر المبيعات تساوي 0 (صفر)، فإنه يتم تغيير حالة أمر المبيعات إلى **مفوتر**.</span><span class="sxs-lookup"><span data-stu-id="58f36-125">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the sales order are 0 (zero), the status of the sales order is changed to **Invoiced**.</span></span> <span data-ttu-id="58f36-126">وإذا كانت كمية **باقي القاتورة** لا تساوي 0 (صفر)، فإن حالة أمر المبيعات تبقى دون تغيير، ويمكن إدخال الفواتير الإضافية لها.</span><span class="sxs-lookup"><span data-stu-id="58f36-126">If the **Invoice remainder** quantity isn't 0 (zero), the status of the sales order remains unchanged, and additional invoices can be entered for it.</span></span>

<span data-ttu-id="58f36-127">ويمكنك عرض حالة أوامر المبيعات في صفحة قائمة **كل أوامر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="58f36-127">You can view the status of the sales orders on the **All sales orders** list page.</span></span> <span data-ttu-id="58f36-128">استخدم صفحة قائمة **فواتير العملاء المفتوحة** لعرض الفواتير التي قمت بترحيلها.</span><span class="sxs-lookup"><span data-stu-id="58f36-128">Use the **Open customer invoices** list page to view the invoices that you posted.</span></span>

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-packing-slips-and-the-date"></a><span data-ttu-id="58f36-129">ترحيل وطباعة فواتير عملاء فردية استناداً إلى قوائم محتويات الشحنات والتاريخ</span><span class="sxs-lookup"><span data-stu-id="58f36-129">Post and print individual customer invoices that are based on packing slips and the date</span></span>
<span data-ttu-id="58f36-130">استخدم هذه العملية عند ترحيل إيصال تعبئة واحد أو أكثر لأمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="58f36-130">Use this process when one or more packing slips have been posted for the sales order.</span></span> <span data-ttu-id="58f36-131">تستند فاتورة العميل إلى قوائم محتويات الشحنات وتعكس الكميات الموجودة بها.</span><span class="sxs-lookup"><span data-stu-id="58f36-131">The customer invoice is based on these packing slips and reflects the quantities from them.</span></span> <span data-ttu-id="58f36-132">وتعتمد المعلومات المالية للفاتورة على المعلومات التي يتم إدخالها عند ترحيلك للفاتورة.</span><span class="sxs-lookup"><span data-stu-id="58f36-132">The financial information for the invoice is based on the information that is entered when you post the invoice.</span></span> 

<span data-ttu-id="58f36-133">يمكنك إنشاء فاتورة عميل بناءً على أصناف بنود كشف التعبئة التي تم شحنها حتى تاريخه، حتى وإن لم يتم بعد شحن كل الأصناف الخاصة بأمر توريد معين.</span><span class="sxs-lookup"><span data-stu-id="58f36-133">You can create a customer invoice that is based on the packing slip line items that have been shipped to date, even if all the items for a particular sales order haven't yet been shipped.</span></span> <span data-ttu-id="58f36-134">وقد تقوم بذلك مثلاً في حالة قيام كيانك القانوني بإصدار فاتورة واحدة لكل عميل كل شهر حيث تغطي كل عمليات التسليم التي تقوم بشحنها أثناء الشهر.</span><span class="sxs-lookup"><span data-stu-id="58f36-134">You might do this if, for example, your legal entity issues one invoice per customer per month that covers all the deliveries that you ship during that month.</span></span> <span data-ttu-id="58f36-135">ويمثل كل كشف تعبئة عملية تسليم جزئية أو كلية للأصناف الموجودة في أمر التوريد.</span><span class="sxs-lookup"><span data-stu-id="58f36-135">Each packing slip represents a partial or complete delivery of the items on the sales order.</span></span> 

<span data-ttu-id="58f36-136">وعند قيامك بترحيل الفاتورة، يتم تحديث كمية **باقي الفاتورة** لكل صنف من الأصناف بإجمالي الكميات التي تم تسليمها من كشوف التعبئة المحددة.</span><span class="sxs-lookup"><span data-stu-id="58f36-136">When you post the invoice, the **Invoice remainder** quantity for each item is updated with the total of the delivered quantities from the selected packing slips.</span></span> <span data-ttu-id="58f36-137">وإذا كان كلُّ من كمية **باقي الفاتورة** وكمية **تسليم البافي**لكافة الأصناف في أمر المبيعات تساوي 0 (صفر)، فإنه يتم تغيير حالة أمر المبيعات إلى **مفوتر**.</span><span class="sxs-lookup"><span data-stu-id="58f36-137">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the sales order are 0 (zero), the status of the sales order is changed to **Invoiced**.</span></span> <span data-ttu-id="58f36-138">وإذا كانت كمية **باقي القاتورة** لا تساوي 0 (صفر)، فإن حالة أمر المبيعات تبقى دون تغيير، ويمكن إدخال الفواتير الإضافية لها.</span><span class="sxs-lookup"><span data-stu-id="58f36-138">If the **Invoice remainder** quantity isn't 0 (zero), the status of the sales order remains unchanged, and additional invoices can be entered for it.</span></span> 

<span data-ttu-id="58f36-139">يتم تحديث حركات المخزون برقم الفاتورة، ويتم تغيير الحالة في حقل **حالة البند** في أمر المبيعات إلى **مفوترة**.</span><span class="sxs-lookup"><span data-stu-id="58f36-139">Inventory transactions are updated with the invoice number, and the status in the **Line status** field on the sales order is changed to **Invoiced**.</span></span> 

<span data-ttu-id="58f36-140">واعرض حالة أوامر المبيعات في صفحة قائمة **كل أوامر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="58f36-140">View the status of the sales orders in the **All sales orders** list page.</span></span>

## <a name="consolidate-sales-orders-or-packing-slips-for-posting"></a><span data-ttu-id="58f36-141">تجميع أوامر التوريد أو إيصالات التعبئة للترحيل</span><span class="sxs-lookup"><span data-stu-id="58f36-141">Consolidate sales orders or packing slips for posting</span></span>
<span data-ttu-id="58f36-142">تستخدم هذه العملية عندما يكون أمر مبيعات واحد أو أكثر جاهزًا للفوترة، وتريد دمجها في فاتورة واحدة.</span><span class="sxs-lookup"><span data-stu-id="58f36-142">Use this process when one or more sales orders are ready to be invoiced, and you want to consolidate them into a single invoice.</span></span> 

<span data-ttu-id="58f36-143">ويمكنك تحديد العديد من الفواتير في صفحة قائمة **أمر المبيعات**، ثم استخدام **إنشاء الفواتير** لتجميعها.</span><span class="sxs-lookup"><span data-stu-id="58f36-143">You can select multiple invoices on the **Sales order** list page and then use **Generate invoices** to consolidate them.</span></span> <span data-ttu-id="58f36-144">في صفحة **ترحيل الفاتورة**، يمكنك تغيير إعداد **ملخص الأمر** للتلخيص حسب رقم الأمر (حيث يوجد العديد من إيصالات التعبئة المتعددة لأمر مبيعات واحد) أو حسب حساب الفاتورة (حيث يوجد العديد من أوامر المبيعات لحساب فاتورة واحدة).</span><span class="sxs-lookup"><span data-stu-id="58f36-144">On the **Posting invoice** page, you can change the **Summary order** setting to summarize by order number (where there are multiple packing slips for a single sales order) or by invoice account (where there are multiple sales orders for a single invoice account).</span></span> <span data-ttu-id="58f36-145">استخدم الزر **ترتيب** لتجميع أوامر المبيعات في فاتورة واحدة، استناداً إلى إعدادات **ملخص الأمر**.</span><span class="sxs-lookup"><span data-stu-id="58f36-145">Use the **Arrange** button to consolidate sales orders into single invoices, based on the **Summary order** settings.</span></span>

## <a name="additional-settings-that-change-the-posting-behavior"></a><span data-ttu-id="58f36-146">الإعدادات الإضافية تغير سلوك الترحيل</span><span class="sxs-lookup"><span data-stu-id="58f36-146">Additional settings that change the posting behavior</span></span>
<span data-ttu-id="58f36-147">تقوم الحقول التالية بتغيير سلوك عملية الترحيل.</span><span class="sxs-lookup"><span data-stu-id="58f36-147">The following fields change the behavior of the posting process.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="58f36-148">الحقل</span><span class="sxs-lookup"><span data-stu-id="58f36-148">Field</span></span></th>
<th><span data-ttu-id="58f36-149">الوصف</span><span class="sxs-lookup"><span data-stu-id="58f36-149">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="58f36-150">الكمية</span><span class="sxs-lookup"><span data-stu-id="58f36-150">Quantity</span></span></td>
<td><span data-ttu-id="58f36-151">يستخدم لتحديد الكميات التي سيتأسس عليها ترحيل المستند.</span><span class="sxs-lookup"><span data-stu-id="58f36-151">Select the quantities to base the posting of the document on.</span></span> <span data-ttu-id="58f36-152">وتختلف الخيارات المتوفرة استنادًا إلى نوع المستند الذي تقوم بترحيله، مثل إيصال تعبئة أو فاتورة.</span><span class="sxs-lookup"><span data-stu-id="58f36-152">The options that are available vary, depending on the type of document that you are posting, such as a packing slip or an invoice.</span></span>
<ul>
<li><span data-ttu-id="58f36-153"><strong>التسليم الآن</strong> -حدد كل الكميات التي تم إدخالها في حقل <strong>التسليم الآن</strong>.</span><span class="sxs-lookup"><span data-stu-id="58f36-153"><strong>Deliver now</strong> – Select all quantities that are entered in the <strong>Deliver now</strong> field.</span></span> <span data-ttu-id="58f36-154">استخدم هذا الخيار لتأكيد أمر جزئي أو تسليمه.</span><span class="sxs-lookup"><span data-stu-id="58f36-154">Use this option to confirm or deliver a partial order.</span></span></li>
<li><span data-ttu-id="58f36-155"><strong>الكمية المنتقاة</strong> – حدد كل الكميات التي تم انتقاؤها.</span><span class="sxs-lookup"><span data-stu-id="58f36-155"><strong>Picked</strong> – Select all quantities that have been picked.</span></span></li>
<li><span data-ttu-id="58f36-156"><strong>الكل</strong> – حدد كل كميات أمر المبيعات التي لم يتم تحديثها بعد حسب نوع المستند الحالي.</span><span class="sxs-lookup"><span data-stu-id="58f36-156"><strong>All</strong> – Select all quantities on the sales order that haven't yet been updated by the current document type.</span></span></li>
<li><span data-ttu-id="58f36-157"><strong>إيصال التعبئة</strong> – حدد كل الكميات التي تم تحديثها حسب إيصال التعبئة.</span><span class="sxs-lookup"><span data-stu-id="58f36-157"><strong>Packing slip</strong> – Select all quantities that have been updated by a packing slip.</span></span></li>
<li><span data-ttu-id="58f36-158"><strong>الكمية المنتقاة والمنتجات غير المخزّنة</strong> – حدد كل الكميات التي تم انتقاؤها وكل كميات المنتجات التي لم يتم تخزينها.</span><span class="sxs-lookup"><span data-stu-id="58f36-158"><strong>Picked quantity and not stocked products</strong> – Select all quantities that have been picked and all product quantities that aren't stocked.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="58f36-159">الترحيل</span><span class="sxs-lookup"><span data-stu-id="58f36-159">Posting</span></span></td>
<td><ul>
<li><span data-ttu-id="58f36-160">حدد هذا الخيار لتسجيل دفتر يومية أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="58f36-160">Select this option to journalize the sales order.</span></span></li>
<li><span data-ttu-id="58f36-161">وقم بإلغاء تحديد هذا الخيار لطباعة أمر مبيعات مبدئي.</span><span class="sxs-lookup"><span data-stu-id="58f36-161">Clear this option to print a pro forma sales order.</span></span> <span data-ttu-id="58f36-162"><strong>ملاحظة:</strong> إذا قمت بعمل اتفاقية لجدول دفع، لا يظهر جدول الدفع في أمر المبيعات المبدئي.</span><span class="sxs-lookup"><span data-stu-id="58f36-162"><strong>Note:</strong> If you made an agreement for a payment schedule, the payment schedule isn't shown on the pro forma sales order.</span></span> <span data-ttu-id="58f36-163">وتظهر جداول الدفع فقط في أوامر المبيعات الفعلية.</span><span class="sxs-lookup"><span data-stu-id="58f36-163">Payment schedules are shown only on actual sales orders.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="58f36-164">التحديد لاحقًا</span><span class="sxs-lookup"><span data-stu-id="58f36-164">Late selection</span></span></td>
<td><span data-ttu-id="58f36-165">حدد هذا الخيار لتقديم الاستعلام المحدد لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="58f36-165">Select this option to apply the selected query later.</span></span> <span data-ttu-id="58f36-166">وهذا الخيار يُستخدم لوظائف الدُفعات.</span><span class="sxs-lookup"><span data-stu-id="58f36-166">This option is used for batch jobs.</span></span> <span data-ttu-id="58f36-167">ويتم إجراء الاستعلام عند تشغيل وظيفة الدُفعة.</span><span class="sxs-lookup"><span data-stu-id="58f36-167">The query is run when the batch job is run.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="58f36-168">خفض الكمية</span><span class="sxs-lookup"><span data-stu-id="58f36-168">Reduce quantity</span></span></td>
<td><span data-ttu-id="58f36-169">حدد هذا الخيار لخفض الكمية التي تم تسليمها تلقائيًا عندما يتم ترحيل المستند، بحيث تساوي الكمية التي تم تسليمها المخزون المتاح.</span><span class="sxs-lookup"><span data-stu-id="58f36-169">Select this option to automatically reduce the delivered quantity when the document is posted, so that the delivered quantity equals the available inventory.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="58f36-170">طباعة</span><span class="sxs-lookup"><span data-stu-id="58f36-170">Print</span></span></td>
<td><span data-ttu-id="58f36-171">حدد وقت طباعة المستندات:</span><span class="sxs-lookup"><span data-stu-id="58f36-171">Select when to print documents:</span></span>
<ul>
<li><span data-ttu-id="58f36-172"><strong>حاليًا</strong> – طباعة المستندات بعد تحديث كل فاتورة.</span><span class="sxs-lookup"><span data-stu-id="58f36-172"><strong>Current</strong> – Print documents after each invoice has been updated.</span></span></li>
<li><span data-ttu-id="58f36-173"><strong>بعد</strong> – طباعة المستندات بعد تحديث كافة الفواتير.</span><span class="sxs-lookup"><span data-stu-id="58f36-173"><strong>After</strong> – Print documents after all the invoices have been updated.</span></span></li>
</ul><span data-ttu-id="58f36-174">
<strong>ملاحظة:</strong> يتوفر حقل <strong>الطباعة</strong> فقط، إذا قمت بتحديد خيار <strong>طباعة الفاتورة</strong> أو <strong>تأكيد الطباعة</strong> أو <strong>طباعة قائمة الانتقاء</strong> أو <strong>طباعة إيصال التعبئة</strong>.</span><span class="sxs-lookup"><span data-stu-id="58f36-174">
<strong>Note:</strong> The <strong>Print</strong> field is available only if you select the <strong>Print invoice</strong>, <strong>Print confirmation</strong>, <strong>Print picking list</strong>, or <strong>Print packing slip</strong> option.</span></span> <span data-ttu-id="58f36-175">على سبيل المثال، في صفحة <strong>فرز النماذج</strong>، قمتَ بإعداد النظام لفرز المعلومات بواسطة حساب الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="58f36-175">For example, on the <strong>Form sorting</strong> page, you have set up the system to sort the information by invoice account.</span></span> <span data-ttu-id="58f36-176">ويمكنك بعد ذلك تحديد <strong>بعد</strong> لطباعة المستندات الموجودة في دُفعة تم فرزها حسب حساب الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="58f36-176">You can then select <strong>After</strong> to print the documents in a batch that is sorted by invoice account.</span></span> <span data-ttu-id="58f36-177">وخلاف ذلك، تتم طباعة المستندات قبل اكتمال المعالجة، ولا يتم فرز المستندات بالترتيب المحدد في صفحة <strong>فرز النماذج</strong>.</span><span class="sxs-lookup"><span data-stu-id="58f36-177">Otherwise, the documents are printed before processing is completed, and the documents aren't sorted in the order that is specified on the <strong>Form sorting</strong> page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="58f36-178">طباعة الفاتورة</span><span class="sxs-lookup"><span data-stu-id="58f36-178">Print invoice</span></span></td>
<td><span data-ttu-id="58f36-179">حدد هذا الخيار لطباعة الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="58f36-179">Select this option to print the invoice.</span></span> <span data-ttu-id="58f36-180">إذا تم إيقاف تشغيل هذا الخيار، يمكنك ترحيل فاتورة دون طباعتها.</span><span class="sxs-lookup"><span data-stu-id="58f36-180">If this option is turned off, you can post an invoice without printing it.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="58f36-181">إرسال بريد إلكتروني</span><span class="sxs-lookup"><span data-stu-id="58f36-181">Send e-mail</span></span></td>
<td><span data-ttu-id="58f36-182">حدد هذا الخيار لإرسال فاتورة أمر مبيعات للعميل كمرفق بريد إلكتروني بعد ترحيل الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="58f36-182">Select this option to send the invoice for a sales order to the customer as an email attachment after the invoice is posted.</span></span> <span data-ttu-id="58f36-183">ويتم إرسال المرفقات كملفات PDF وXML.</span><span class="sxs-lookup"><span data-stu-id="58f36-183">Attachments are sent as PDF and XML files.</span></span> <span data-ttu-id="58f36-184">ويتوفر هذا الخيار فقط إذا قمت بتحديد <strong>تمكين CFD (الفواتير الإلكترونية)</strong> في صفحة <strong>معلمات الفاتورة الإلكترونية</strong>.</span><span class="sxs-lookup"><span data-stu-id="58f36-184">This option is available only if you select the <strong>Enable CFD (electronic invoices)</strong> option on the <strong>Electronic invoice parameters</strong> page.</span></span> <span data-ttu-id="58f36-185"><strong>ملاحظة:</strong> (المكسيك) لا يتوفر عنصر التحكم هذا إلا للكيانات القانونية الذي يوجد عنوانها الرئيسي في المكسيك.</span><span class="sxs-lookup"><span data-stu-id="58f36-185"><strong>Note:</strong> (MEX) This control is available only to legal entities whose primary address is in Mexico.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="58f36-186">استخدام وجهة إدارة الطباعة</span><span class="sxs-lookup"><span data-stu-id="58f36-186">Use print management destination</span></span></td>
<td><span data-ttu-id="58f36-187">حدد هذا الخيار لاستخدام إعدادات الطباعة المحددة للحركة أو المستند أو الوحدة في صفحة <strong>إعداد إدارة الطباعة</strong>.</span><span class="sxs-lookup"><span data-stu-id="58f36-187">Select this option to use the print settings that are specified for the transaction, document, or module on the <strong>Print management setup</strong> page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="58f36-188">فحص الحد الائتماني</span><span class="sxs-lookup"><span data-stu-id="58f36-188">Check credit limit</span></span></td>
<td><span data-ttu-id="58f36-189">حدد المعلومات التي يجب تحليلها عند فحص حد الائتمان.</span><span class="sxs-lookup"><span data-stu-id="58f36-189">Select the information that should be analyzed when a credit limit check is performed.</span></span>
<ul>
<li><span data-ttu-id="58f36-190"><strong>لا شيء</strong> – لا توجد متطلبات تتعلق بفحص حد الائتمان.</span><span class="sxs-lookup"><span data-stu-id="58f36-190"><strong>None</strong> – There is no requirement for the credit limit check.</span></span></li>
<li><span data-ttu-id="58f36-191"><strong>Balance</strong> – يتم فحص حد الائتمان في مقابل رصيد العميل.</span><span class="sxs-lookup"><span data-stu-id="58f36-191"><strong>Balance</strong> – The credit limit is checked against the customer balance.</span></span></li>
<li><span data-ttu-id="58f36-192"><strong>الرصيد + إيصال التعبئة أو إيصال استلام المنتجات</strong> – يتم فحص حد الائتمان في مقابل رصيد العميل وعمليات التسليم.</span><span class="sxs-lookup"><span data-stu-id="58f36-192"><strong>Balance + packing slip or product receipt</strong> – The credit limit is checked against the customer balance and deliveries.</span></span></li>
<li><span data-ttu-id="58f36-193"><strong>الرصيد+الكل</strong> – يتم فحص حد الائتمان في مقابل رصيد العميل وعمليات التسليم والأوامر المفتوحة.</span><span class="sxs-lookup"><span data-stu-id="58f36-193"><strong>Balance+All</strong> – The credit limit is checked against the customer balance, deliveries, and open orders.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="58f36-194">تصحيح الائتمان</span><span class="sxs-lookup"><span data-stu-id="58f36-194">Credit correction</span></span></td>
<td><span data-ttu-id="58f36-195">حدد هذا الخيار لعرض إشعار الدائن على أنه قيمة مدينة في حركات الإيصالات.</span><span class="sxs-lookup"><span data-stu-id="58f36-195">Select this option to display the credit note as a debit in the voucher transactions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="58f36-196">الكمية الدائنة المتبقية</span><span class="sxs-lookup"><span data-stu-id="58f36-196">Credit remaining quantity</span></span></td>
<td><span data-ttu-id="58f36-197">إذا كنت تقوم بترحيل إشعار دائن، فقم بتحديد هذا الخيار للاحتفاظ بالكمية المتبقية في الأمر.</span><span class="sxs-lookup"><span data-stu-id="58f36-197">If you're posting a credit note, select this option to keep the remaining quantity on order.</span></span> <span data-ttu-id="58f36-198">أما في حالة إلغاء تحديد هذا الخيار، فإنه يتم تعيين الكمية المتبقية إلى 0 (صفر).</span><span class="sxs-lookup"><span data-stu-id="58f36-198">If this option is cleared, the remaining quantity is set to 0 (zero).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="58f36-199">تحديث ملخص لـ</span><span class="sxs-lookup"><span data-stu-id="58f36-199">Summary update for</span></span></td>
<td><span data-ttu-id="58f36-200">حدد الطريقة التي يجب بها تلخيص أوامر المبيعات المتعددة.</span><span class="sxs-lookup"><span data-stu-id="58f36-200">Select how multiple sales orders should be summarized:</span></span>
<ul>
<li><span data-ttu-id="58f36-201"><strong>لا شيء</strong> – عدم تلخيص أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="58f36-201"><strong>None</strong> – Don't summarize sales orders.</span></span> <span data-ttu-id="58f36-202">على سبيل المثال، سيتم إنشاء فاتورة منفصلة لكل أمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="58f36-202">For example, a separate invoice will be created for each sales order.</span></span></li>
<li><span data-ttu-id="58f36-203"><strong>حساب الفاتورة</strong> – تلخيص كافة الأوامر المحددة وفقًا للمعايير المحددة في صفحة <strong>معلمات تحديث الملخص</strong>.</span><span class="sxs-lookup"><span data-stu-id="58f36-203"><strong>Invoice account</strong> – Summarize all selected orders, based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span></li>
<li><span data-ttu-id="58f36-204"><strong>أمر</strong> – تلخيص مجموعة محددة من الأوامر في أمر واحد تقوم بتحديده.</span><span class="sxs-lookup"><span data-stu-id="58f36-204"><strong>Order</strong> – Summarize a selected range of orders into one order that you specify.</span></span> <span data-ttu-id="58f36-205">ويتم تلخيص الأوامر وفقًا للمعايير التي تم إعدادها في صفحة <strong>معلمات تحديث الملخص</strong>.</span><span class="sxs-lookup"><span data-stu-id="58f36-205">The orders are summarized based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span> <span data-ttu-id="58f36-206">وإذا قمت بتحديد هذا الخيار، فيجب عليك تحديد حقل <strong>أمر المبيعات</strong>.</span><span class="sxs-lookup"><span data-stu-id="58f36-206">If you select this option, you must select a value in the <strong>Sales order</strong> field.</span></span></li>
<li><span data-ttu-id="58f36-207"><strong>الملخص التلقائي</strong> – في حالة تحديد تحديثات الملخص في صفحة <strong>تحديث الملخص</strong>، فقم بتلخيص جميع الأوامر المحددة، استنادًا إلى المعايير التي تم إعدادها في صفحة <strong>معلمات تحديث الملخص</strong>.</span><span class="sxs-lookup"><span data-stu-id="58f36-207"><strong>Automatic summary</strong> – If summary updates have been specified on the <strong>Summary update</strong> page, summarize all selected orders, based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span> <span data-ttu-id="58f36-208">وإذا لم يتم تحديد تحديثات الملخص، فإنه يتم ترحيل الأمر بشكل منفصل.</span><span class="sxs-lookup"><span data-stu-id="58f36-208">If summary updates haven't been specified, the order is posted separately.</span></span></li>
<li><span data-ttu-id="58f36-209"><strong>إيصال التعبئة</strong> – تلخيص مجموعة محددة من الأوامر في فاتورة واحدة لكل إيصال تعبئة.</span><span class="sxs-lookup"><span data-stu-id="58f36-209"><strong>Packing slip</strong> – Summarize a selected range of orders into one invoice for each packing slip.</span></span> <span data-ttu-id="58f36-210">لا يتوفر هذا الخيار إلا إذا تم تحديد <strong>إيصال التعبئة</strong> في حقل <strong>الكمية</strong>.</span><span class="sxs-lookup"><span data-stu-id="58f36-210">This option is available only if <strong>Packing slip</strong> is selected in the <strong>Quantity</strong> field.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>






