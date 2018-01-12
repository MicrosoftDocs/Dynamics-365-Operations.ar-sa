---
title: "إنشاء فاتورة عميل"
description: "**فاتورة عميل لأمر مبيعات** هي فاتورة ترتبط بعملية بيع وتعطيها مؤسسة لعميل."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 77772
ms.assetid: 00b4b40c-1576-4098-9aed-ac376fdeb8c5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 04809337167741c30677844adad8addeaba303bc
ms.openlocfilehash: e91f89f73a39d61883331789128a067de550246c
ms.contentlocale: ar-sa
ms.lasthandoff: 01/12/2018

---

# <a name="create-a-customer-invoice"></a><span data-ttu-id="e6794-103">إنشاء فاتورة عميل</span><span class="sxs-lookup"><span data-stu-id="e6794-103">Create a customer invoice</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e6794-104">**فاتورة عميل لأمر المبيعات** هي فاتورة ترتبط بعملية بيع وتعطيها مؤسسة لعميل.</span><span class="sxs-lookup"><span data-stu-id="e6794-104">A **customer invoice for a sales order** is a bill that is related to a sale, and that an organization gives to a customer.</span></span> <span data-ttu-id="e6794-105">ويتم إنشاء هذا النوع من فاتورة العميل استنادًا إلى أمر المبيعات، الذي يتضمن بنود الأوامر وأرقام الأصناف.</span><span class="sxs-lookup"><span data-stu-id="e6794-105">This type of customer invoice is created based on a sales order, which includes order lines and item numbers.</span></span> <span data-ttu-id="e6794-106">ويتم تحديد أرقام الأصناف وترحيلها في دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="e6794-106">Item numbers are specified and posted in the ledger.</span></span> <span data-ttu-id="e6794-107">ولا تتوفر إدخالات دفتر اليومية في دفتر الأستاذ الفرعي لفاتورة عميل لأمر مبيعات.‬</span><span class="sxs-lookup"><span data-stu-id="e6794-107">Subledger journal entries aren't available for a customer invoice for a sales order.</span></span> <span data-ttu-id="e6794-108">للحصول على مزيد من المعلومات، راجع [إنشاء فواتير أوامر المبيعات‬](tasks/create-sales-order-invoices.md).</span><span class="sxs-lookup"><span data-stu-id="e6794-108">For more information, see [Create sales order invoices](tasks/create-sales-order-invoices.md).</span></span>

<span data-ttu-id="e6794-109">ولا ترتبط **فاتورة النص الحر** بأمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="e6794-109">A **free text invoice** isn't related to a sales order.</span></span> <span data-ttu-id="e6794-110">ولكنها تحتوي على بنود الأمر التي تتضمن حسابات دفتر الأستاذ وأوصاف النص الحر ومبلغ المبيعات الذي تقوم بإدخاله.</span><span class="sxs-lookup"><span data-stu-id="e6794-110">It contains order lines that include ledger accounts, free-text descriptions, and a sales amount that you enter.</span></span> <span data-ttu-id="e6794-111">ولا يمكنك إدخال رقم الصنف في نوع الفاتورة هذا.</span><span class="sxs-lookup"><span data-stu-id="e6794-111">You can't enter an item number on this kind of invoice.</span></span> <span data-ttu-id="e6794-112">يجب إدخال معلومات ضريبة المبيعات الصحيحة.</span><span class="sxs-lookup"><span data-stu-id="e6794-112">You must enter the appropriate sales tax information.</span></span> <span data-ttu-id="e6794-113">وتتم الإشارة إلى حساب رئيسي للبيع في كل بند فاتورة تقوم بتوزيعها على عدة حسابات دفتر أستاذ بالنقر فوق **توزيع المبالغ** في صفحة **فاتورة النص الحر**.</span><span class="sxs-lookup"><span data-stu-id="e6794-113">A main account for the sale is indicated on each invoice line, which you can distribute to multiple ledger accounts by clicking **Distribute amounts** on the **Free text invoice** page.</span></span> <span data-ttu-id="e6794-114">وبالإضافة إلى ذلك، يتم ترحيل رصيد العميل إلى حساب الملخص من ملف تعريف الترحيل المستخدم لفاتورة النص الحر.</span><span class="sxs-lookup"><span data-stu-id="e6794-114">Additionally, the customer balance is posted to the summary account from the posting profile that is used for the free text invoice.</span></span>

<span data-ttu-id="e6794-115">لمزيد من المعلومات، راجع: </span><span class="sxs-lookup"><span data-stu-id="e6794-115">For more information see:</span></span>

[<span data-ttu-id="e6794-116">إنشاء فاتورة نص حر</span><span class="sxs-lookup"><span data-stu-id="e6794-116">Create a free text invoice</span></span>](tasks/create-free-text-invoice.md)

[<span data-ttu-id="e6794-117">إنشاء قالب نص حر</span><span class="sxs-lookup"><span data-stu-id="e6794-117">Create a free text template</span></span>](tasks/create-free-text-invoice-template.md)

[<span data-ttu-id="e6794-118">‏‫تعيين قالب فاتورة ذات نص حر إلى عميل</span><span class="sxs-lookup"><span data-stu-id="e6794-118">Assign a free text invoice template to a customer</span></span>](tasks/assign-free-text-invoice-template-customer.md)

[<span data-ttu-id="e6794-119">إنشاء وترحيل فواتير النص الحر المكررة</span><span class="sxs-lookup"><span data-stu-id="e6794-119">Generate and post recurring free text invoices</span></span>](tasks/post-recurring-free-text-invoices.md)


<span data-ttu-id="e6794-120">**الفاتورة المبدئية** هي فاتورة يتم إعدادها كتقدير لمبالغ الفاتورة الفعلية قبل ترحيل الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="e6794-120">A **pro forma invoice** is an invoice that is prepared as an estimate of the actual invoice amounts before the invoice is posted.</span></span> <span data-ttu-id="e6794-121">ويمكنك طباعة فاتورة مبدئية لفاتورة عميل لفاتورة مبيعات أو لفاتورة النص الحر.</span><span class="sxs-lookup"><span data-stu-id="e6794-121">You can print a pro forma invoice either for a customer invoice for a sales order or for a free text invoice.</span></span>

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-sales-orders"></a><span data-ttu-id="e6794-122">ترحيل وطباعة فواتير عملاء فردية استناداً إلى أوامر التوريد</span><span class="sxs-lookup"><span data-stu-id="e6794-122">Post and print individual customer invoices that are based on sales orders</span></span>
<span data-ttu-id="e6794-123">استخدم هذا العملية لإنشاء فاتورة تستند إلى أمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="e6794-123">Use this process to create an invoice that is based on a sales order.</span></span> <span data-ttu-id="e6794-124">ويمكنك القيام بذلك إذا قررت عمل فاتورة للعميل قبل تسليم السلع أو الخدمات.</span><span class="sxs-lookup"><span data-stu-id="e6794-124">You might do this if you decide to invoice the customer before you deliver the goods or services.</span></span> 

<span data-ttu-id="e6794-125">عندما تقوم بترحيل الفاتورة، يتم تحديث كمية **باقي الفاتورة** لكل صنف من خلال إجمالي الكميات التي تمت فوترتها من أمر الشراء المحدد.</span><span class="sxs-lookup"><span data-stu-id="e6794-125">When you post an invoice, the **Invoice remainder** quantity for each item is updated with the total of the invoiced quantities from the selected sales order.</span></span> <span data-ttu-id="e6794-126">وإذا كان كلُّ من كمية **باقي الفاتورة** وكمية **تسليم البافي**لكافة الأصناف في أمر المبيعات تساوي 0 (صفر)، فإنه يتم تغيير حالة أمر المبيعات إلى **مفوتر**.</span><span class="sxs-lookup"><span data-stu-id="e6794-126">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the sales order are 0 (zero), the status of the sales order is changed to **Invoiced**.</span></span> <span data-ttu-id="e6794-127">وإذا كانت كمية **باقي القاتورة** لا تساوي 0 (صفر)، فإن حالة أمر المبيعات تبقى دون تغيير، ويمكن إدخال الفواتير الإضافية لها.</span><span class="sxs-lookup"><span data-stu-id="e6794-127">If the **Invoice remainder** quantity isn't 0 (zero), the status of the sales order remains unchanged, and additional invoices can be entered for it.</span></span>

<span data-ttu-id="e6794-128">ويمكنك عرض حالة أوامر المبيعات في صفحة قائمة **كل أوامر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="e6794-128">You can view the status of the sales orders on the **All sales orders** list page.</span></span> <span data-ttu-id="e6794-129">استخدم صفحة قائمة **فواتير العملاء المفتوحة** لعرض الفواتير التي قمت بترحيلها.</span><span class="sxs-lookup"><span data-stu-id="e6794-129">Use the **Open customer invoices** list page to view the invoices that you posted.</span></span>

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-packing-slips-and-the-date"></a><span data-ttu-id="e6794-130">ترحيل وطباعة فواتير عملاء فردية استناداً إلى قوائم محتويات الشحنات والتاريخ</span><span class="sxs-lookup"><span data-stu-id="e6794-130">Post and print individual customer invoices that are based on packing slips and the date</span></span>
<span data-ttu-id="e6794-131">استخدم هذه العملية عند ترحيل إيصال تعبئة واحد أو أكثر لأمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="e6794-131">Use this process when one or more packing slips have been posted for the sales order.</span></span> <span data-ttu-id="e6794-132">تستند فاتورة العميل إلى قوائم محتويات الشحنات وتعكس الكميات الموجودة بها.</span><span class="sxs-lookup"><span data-stu-id="e6794-132">The customer invoice is based on these packing slips and reflects the quantities from them.</span></span> <span data-ttu-id="e6794-133">وتعتمد المعلومات المالية للفاتورة على المعلومات التي يتم إدخالها عند ترحيلك للفاتورة.</span><span class="sxs-lookup"><span data-stu-id="e6794-133">The financial information for the invoice is based on the information that is entered when you post the invoice.</span></span> 

<span data-ttu-id="e6794-134">يمكنك إنشاء فاتورة عميل بناءً على أصناف بنود كشف التعبئة التي تم شحنها حتى تاريخه، حتى وإن لم يتم بعد شحن كل الأصناف الخاصة بأمر توريد معين.</span><span class="sxs-lookup"><span data-stu-id="e6794-134">You can create a customer invoice that is based on the packing slip line items that have been shipped to date, even if all the items for a particular sales order haven't yet been shipped.</span></span> <span data-ttu-id="e6794-135">وقد تقوم بذلك مثلاً في حالة قيام كيانك القانوني بإصدار فاتورة واحدة لكل عميل كل شهر حيث تغطي كل عمليات التسليم التي تقوم بشحنها أثناء الشهر.</span><span class="sxs-lookup"><span data-stu-id="e6794-135">You might do this if, for example, your legal entity issues one invoice per customer per month that covers all the deliveries that you ship during that month.</span></span> <span data-ttu-id="e6794-136">ويمثل كل كشف تعبئة عملية تسليم جزئية أو كلية للأصناف الموجودة في أمر التوريد.</span><span class="sxs-lookup"><span data-stu-id="e6794-136">Each packing slip represents a partial or complete delivery of the items on the sales order.</span></span> 

<span data-ttu-id="e6794-137">وعند قيامك بترحيل الفاتورة، يتم تحديث كمية **باقي الفاتورة** لكل صنف من الأصناف بإجمالي الكميات التي تم تسليمها من كشوف التعبئة المحددة.</span><span class="sxs-lookup"><span data-stu-id="e6794-137">When you post the invoice, the **Invoice remainder** quantity for each item is updated with the total of the delivered quantities from the selected packing slips.</span></span> <span data-ttu-id="e6794-138">وإذا كان كلُّ من كمية **باقي الفاتورة** وكمية **تسليم البافي**لكافة الأصناف في أمر المبيعات تساوي 0 (صفر)، فإنه يتم تغيير حالة أمر المبيعات إلى **مفوتر**.</span><span class="sxs-lookup"><span data-stu-id="e6794-138">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the sales order are 0 (zero), the status of the sales order is changed to **Invoiced**.</span></span> <span data-ttu-id="e6794-139">وإذا كانت كمية **باقي القاتورة** لا تساوي 0 (صفر)، فإن حالة أمر المبيعات تبقى دون تغيير، ويمكن إدخال الفواتير الإضافية لها.</span><span class="sxs-lookup"><span data-stu-id="e6794-139">If the **Invoice remainder** quantity isn't 0 (zero), the status of the sales order remains unchanged, and additional invoices can be entered for it.</span></span> 

<span data-ttu-id="e6794-140">يتم تحديث حركات المخزون برقم الفاتورة، ويتم تغيير الحالة في حقل **حالة البند** في أمر المبيعات إلى **مفوترة**.</span><span class="sxs-lookup"><span data-stu-id="e6794-140">Inventory transactions are updated with the invoice number, and the status in the **Line status** field on the sales order is changed to **Invoiced**.</span></span> 

<span data-ttu-id="e6794-141">واعرض حالة أوامر المبيعات في صفحة قائمة **كل أوامر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="e6794-141">View the status of the sales orders in the **All sales orders** list page.</span></span>

## <a name="consolidate-sales-orders-or-packing-slips-for-posting"></a><span data-ttu-id="e6794-142">تجميع أوامر التوريد أو إيصالات التعبئة للترحيل</span><span class="sxs-lookup"><span data-stu-id="e6794-142">Consolidate sales orders or packing slips for posting</span></span>
<span data-ttu-id="e6794-143">تستخدم هذه العملية عندما يكون أمر مبيعات واحد أو أكثر جاهزًا للفوترة، وتريد دمجها في فاتورة واحدة.</span><span class="sxs-lookup"><span data-stu-id="e6794-143">Use this process when one or more sales orders are ready to be invoiced, and you want to consolidate them into a single invoice.</span></span> 

<span data-ttu-id="e6794-144">ويمكنك تحديد العديد من الفواتير في صفحة قائمة **أمر المبيعات**، ثم استخدام **إنشاء الفواتير** لتجميعها.</span><span class="sxs-lookup"><span data-stu-id="e6794-144">You can select multiple invoices on the **Sales order** list page and then use **Generate invoices** to consolidate them.</span></span> <span data-ttu-id="e6794-145">في صفحة **ترحيل الفاتورة**، يمكنك تغيير إعداد **ملخص الأمر** للتلخيص حسب رقم الأمر (حيث يوجد العديد من إيصالات التعبئة المتعددة لأمر مبيعات واحد) أو حسب حساب الفاتورة (حيث يوجد العديد من أوامر المبيعات لحساب فاتورة واحدة).</span><span class="sxs-lookup"><span data-stu-id="e6794-145">On the **Posting invoice** page, you can change the **Summary order** setting to summarize by order number (where there are multiple packing slips for a single sales order) or by invoice account (where there are multiple sales orders for a single invoice account).</span></span> <span data-ttu-id="e6794-146">استخدم الزر **ترتيب** لتجميع أوامر المبيعات في فاتورة واحدة، استناداً إلى إعدادات **ملخص الأمر**.</span><span class="sxs-lookup"><span data-stu-id="e6794-146">Use the **Arrange** button to consolidate sales orders into single invoices, based on the **Summary order** settings.</span></span>

## <a name="additional-settings-that-change-the-posting-behavior"></a><span data-ttu-id="e6794-147">الإعدادات الإضافية تغير سلوك الترحيل</span><span class="sxs-lookup"><span data-stu-id="e6794-147">Additional settings that change the posting behavior</span></span>
<span data-ttu-id="e6794-148">تقوم الحقول التالية بتغيير سلوك عملية الترحيل.</span><span class="sxs-lookup"><span data-stu-id="e6794-148">The following fields change the behavior of the posting process.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e6794-149">الحقل</span><span class="sxs-lookup"><span data-stu-id="e6794-149">Field</span></span></th>
<th><span data-ttu-id="e6794-150">الوصف</span><span class="sxs-lookup"><span data-stu-id="e6794-150">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e6794-151">الكمية</span><span class="sxs-lookup"><span data-stu-id="e6794-151">Quantity</span></span></td>
<td><span data-ttu-id="e6794-152">يستخدم لتحديد الكميات التي سيتأسس عليها ترحيل المستند.</span><span class="sxs-lookup"><span data-stu-id="e6794-152">Select the quantities to base the posting of the document on.</span></span> <span data-ttu-id="e6794-153">وتختلف الخيارات المتوفرة استنادًا إلى نوع المستند الذي تقوم بترحيله، مثل إيصال تعبئة أو فاتورة.</span><span class="sxs-lookup"><span data-stu-id="e6794-153">The options that are available vary, depending on the type of document that you are posting, such as a packing slip or an invoice.</span></span>
<ul>
<li><span data-ttu-id="e6794-154"><strong>التسليم الآن</strong> -حدد كل الكميات التي تم إدخالها في حقل <strong>التسليم الآن</strong>.</span><span class="sxs-lookup"><span data-stu-id="e6794-154"><strong>Deliver now</strong> – Select all quantities that are entered in the <strong>Deliver now</strong> field.</span></span> <span data-ttu-id="e6794-155">استخدم هذا الخيار لتأكيد أمر جزئي أو تسليمه.</span><span class="sxs-lookup"><span data-stu-id="e6794-155">Use this option to confirm or deliver a partial order.</span></span></li>
<li><span data-ttu-id="e6794-156"><strong>الكمية المنتقاة</strong> – حدد كل الكميات التي تم انتقاؤها.</span><span class="sxs-lookup"><span data-stu-id="e6794-156"><strong>Picked</strong> – Select all quantities that have been picked.</span></span></li>
<li><span data-ttu-id="e6794-157"><strong>الكل</strong> – حدد كل كميات أمر المبيعات التي لم يتم تحديثها بعد حسب نوع المستند الحالي.</span><span class="sxs-lookup"><span data-stu-id="e6794-157"><strong>All</strong> – Select all quantities on the sales order that haven't yet been updated by the current document type.</span></span></li>
<li><span data-ttu-id="e6794-158"><strong>إيصال التعبئة</strong> – حدد كل الكميات التي تم تحديثها حسب إيصال التعبئة.</span><span class="sxs-lookup"><span data-stu-id="e6794-158"><strong>Packing slip</strong> – Select all quantities that have been updated by a packing slip.</span></span></li>
<li><span data-ttu-id="e6794-159"><strong>الكمية المنتقاة والمنتجات غير المخزّنة</strong> – حدد كل الكميات التي تم انتقاؤها وكل كميات المنتجات التي لم يتم تخزينها.</span><span class="sxs-lookup"><span data-stu-id="e6794-159"><strong>Picked quantity and not stocked products</strong> – Select all quantities that have been picked and all product quantities that aren't stocked.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6794-160">الترحيل</span><span class="sxs-lookup"><span data-stu-id="e6794-160">Posting</span></span></td>
<td><ul>
<li><span data-ttu-id="e6794-161">حدد هذا الخيار لتسجيل دفتر يومية أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="e6794-161">Select this option to journalize the sales order.</span></span></li>
<li><span data-ttu-id="e6794-162">وقم بإلغاء تحديد هذا الخيار لطباعة أمر مبيعات مبدئي.</span><span class="sxs-lookup"><span data-stu-id="e6794-162">Clear this option to print a pro forma sales order.</span></span> <span data-ttu-id="e6794-163"><strong>ملاحظة:</strong> إذا قمت بعمل اتفاقية لجدول دفع، لا يظهر جدول الدفع في أمر المبيعات المبدئي.</span><span class="sxs-lookup"><span data-stu-id="e6794-163"><strong>Note:</strong> If you made an agreement for a payment schedule, the payment schedule isn't shown on the pro forma sales order.</span></span> <span data-ttu-id="e6794-164">وتظهر جداول الدفع فقط في أوامر المبيعات الفعلية.</span><span class="sxs-lookup"><span data-stu-id="e6794-164">Payment schedules are shown only on actual sales orders.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6794-165">التحديد لاحقًا</span><span class="sxs-lookup"><span data-stu-id="e6794-165">Late selection</span></span></td>
<td><span data-ttu-id="e6794-166">حدد هذا الخيار لتقديم الاستعلام المحدد لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="e6794-166">Select this option to apply the selected query later.</span></span> <span data-ttu-id="e6794-167">وهذا الخيار يُستخدم لوظائف الدُفعات.</span><span class="sxs-lookup"><span data-stu-id="e6794-167">This option is used for batch jobs.</span></span> <span data-ttu-id="e6794-168">ويتم إجراء الاستعلام عند تشغيل وظيفة الدُفعة.</span><span class="sxs-lookup"><span data-stu-id="e6794-168">The query is run when the batch job is run.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6794-169">خفض الكمية</span><span class="sxs-lookup"><span data-stu-id="e6794-169">Reduce quantity</span></span></td>
<td><span data-ttu-id="e6794-170">حدد هذا الخيار لخفض الكمية التي تم تسليمها تلقائيًا عندما يتم ترحيل المستند، بحيث تساوي الكمية التي تم تسليمها المخزون المتاح.</span><span class="sxs-lookup"><span data-stu-id="e6794-170">Select this option to automatically reduce the delivered quantity when the document is posted, so that the delivered quantity equals the available inventory.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6794-171">طباعة</span><span class="sxs-lookup"><span data-stu-id="e6794-171">Print</span></span></td>
<td><span data-ttu-id="e6794-172">حدد وقت طباعة المستندات:</span><span class="sxs-lookup"><span data-stu-id="e6794-172">Select when to print documents:</span></span>
<ul>
<li><span data-ttu-id="e6794-173"><strong>حاليًا</strong> – طباعة المستندات بعد تحديث كل فاتورة.</span><span class="sxs-lookup"><span data-stu-id="e6794-173"><strong>Current</strong> – Print documents after each invoice has been updated.</span></span></li>
<li><span data-ttu-id="e6794-174"><strong>بعد</strong> – طباعة المستندات بعد تحديث كافة الفواتير.</span><span class="sxs-lookup"><span data-stu-id="e6794-174"><strong>After</strong> – Print documents after all the invoices have been updated.</span></span></li>
</ul><span data-ttu-id="e6794-175">
<strong>ملاحظة:</strong> يتوفر حقل <strong>الطباعة</strong> فقط، إذا قمت بتحديد خيار <strong>طباعة الفاتورة</strong> أو <strong>تأكيد الطباعة</strong> أو <strong>طباعة قائمة الانتقاء</strong> أو <strong>طباعة إيصال التعبئة</strong>.</span><span class="sxs-lookup"><span data-stu-id="e6794-175">
<strong>Note:</strong> The <strong>Print</strong> field is available only if you select the <strong>Print invoice</strong>, <strong>Print confirmation</strong>, <strong>Print picking list</strong>, or <strong>Print packing slip</strong> option.</span></span> <span data-ttu-id="e6794-176">على سبيل المثال، في صفحة <strong>فرز النماذج</strong>، قمتَ بإعداد النظام لفرز المعلومات بواسطة حساب الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="e6794-176">For example, on the <strong>Form sorting</strong> page, you have set up the system to sort the information by invoice account.</span></span> <span data-ttu-id="e6794-177">ويمكنك بعد ذلك تحديد <strong>بعد</strong> لطباعة المستندات الموجودة في دُفعة تم فرزها حسب حساب الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="e6794-177">You can then select <strong>After</strong> to print the documents in a batch that is sorted by invoice account.</span></span> <span data-ttu-id="e6794-178">وخلاف ذلك، تتم طباعة المستندات قبل اكتمال المعالجة، ولا يتم فرز المستندات بالترتيب المحدد في صفحة <strong>فرز النماذج</strong>.</span><span class="sxs-lookup"><span data-stu-id="e6794-178">Otherwise, the documents are printed before processing is completed, and the documents aren't sorted in the order that is specified on the <strong>Form sorting</strong> page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6794-179">طباعة الفاتورة</span><span class="sxs-lookup"><span data-stu-id="e6794-179">Print invoice</span></span></td>
<td><span data-ttu-id="e6794-180">حدد هذا الخيار لطباعة الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="e6794-180">Select this option to print the invoice.</span></span> <span data-ttu-id="e6794-181">إذا تم إيقاف تشغيل هذا الخيار، يمكنك ترحيل فاتورة دون طباعتها.</span><span class="sxs-lookup"><span data-stu-id="e6794-181">If this option is turned off, you can post an invoice without printing it.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6794-182">إرسال بريد إلكتروني</span><span class="sxs-lookup"><span data-stu-id="e6794-182">Send e-mail</span></span></td>
<td><span data-ttu-id="e6794-183">حدد هذا الخيار لإرسال فاتورة أمر مبيعات للعميل كمرفق بريد إلكتروني بعد ترحيل الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="e6794-183">Select this option to send the invoice for a sales order to the customer as an email attachment after the invoice is posted.</span></span> <span data-ttu-id="e6794-184">ويتم إرسال المرفقات كملفات PDF وXML.</span><span class="sxs-lookup"><span data-stu-id="e6794-184">Attachments are sent as PDF and XML files.</span></span> <span data-ttu-id="e6794-185">ويتوفر هذا الخيار فقط إذا قمت بتحديد <strong>تمكين CFD (الفواتير الإلكترونية)</strong> في صفحة <strong>معلمات الفاتورة الإلكترونية</strong>.</span><span class="sxs-lookup"><span data-stu-id="e6794-185">This option is available only if you select the <strong>Enable CFD (electronic invoices)</strong> option on the <strong>Electronic invoice parameters</strong> page.</span></span> <span data-ttu-id="e6794-186"><strong>ملاحظة:</strong> (المكسيك) لا يتوفر عنصر التحكم هذا إلا للكيانات القانونية الذي يوجد عنوانها الرئيسي في المكسيك.</span><span class="sxs-lookup"><span data-stu-id="e6794-186"><strong>Note:</strong> (MEX) This control is available only to legal entities whose primary address is in Mexico.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6794-187">استخدام وجهة إدارة الطباعة</span><span class="sxs-lookup"><span data-stu-id="e6794-187">Use print management destination</span></span></td>
<td><span data-ttu-id="e6794-188">حدد هذا الخيار لاستخدام إعدادات الطباعة المحددة للحركة أو المستند أو الوحدة في صفحة <strong>إعداد إدارة الطباعة</strong>.</span><span class="sxs-lookup"><span data-stu-id="e6794-188">Select this option to use the print settings that are specified for the transaction, document, or module on the <strong>Print management setup</strong> page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6794-189">فحص الحد الائتماني</span><span class="sxs-lookup"><span data-stu-id="e6794-189">Check credit limit</span></span></td>
<td><span data-ttu-id="e6794-190">حدد المعلومات التي يجب تحليلها عند فحص حد الائتمان.</span><span class="sxs-lookup"><span data-stu-id="e6794-190">Select the information that should be analyzed when a credit limit check is performed.</span></span>
<ul>
<li><span data-ttu-id="e6794-191"><strong>لا شيء</strong> – لا توجد متطلبات تتعلق بفحص حد الائتمان.</span><span class="sxs-lookup"><span data-stu-id="e6794-191"><strong>None</strong> – There is no requirement for the credit limit check.</span></span></li>
<li><span data-ttu-id="e6794-192"><strong>Balance</strong> – يتم فحص حد الائتمان في مقابل رصيد العميل.</span><span class="sxs-lookup"><span data-stu-id="e6794-192"><strong>Balance</strong> – The credit limit is checked against the customer balance.</span></span></li>
<li><span data-ttu-id="e6794-193"><strong>الرصيد + إيصال التعبئة أو إيصال استلام المنتجات</strong> – يتم فحص حد الائتمان في مقابل رصيد العميل وعمليات التسليم.</span><span class="sxs-lookup"><span data-stu-id="e6794-193"><strong>Balance + packing slip or product receipt</strong> – The credit limit is checked against the customer balance and deliveries.</span></span></li>
<li><span data-ttu-id="e6794-194"><strong>الرصيد+الكل</strong> – يتم فحص حد الائتمان في مقابل رصيد العميل وعمليات التسليم والأوامر المفتوحة.</span><span class="sxs-lookup"><span data-stu-id="e6794-194"><strong>Balance+All</strong> – The credit limit is checked against the customer balance, deliveries, and open orders.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6794-195">تصحيح الائتمان</span><span class="sxs-lookup"><span data-stu-id="e6794-195">Credit correction</span></span></td>
<td><span data-ttu-id="e6794-196">حدد هذا الخيار لعرض إشعار الدائن على أنه قيمة مدينة في حركات الإيصالات.</span><span class="sxs-lookup"><span data-stu-id="e6794-196">Select this option to display the credit note as a debit in the voucher transactions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6794-197">الكمية الدائنة المتبقية</span><span class="sxs-lookup"><span data-stu-id="e6794-197">Credit remaining quantity</span></span></td>
<td><span data-ttu-id="e6794-198">إذا كنت تقوم بترحيل إشعار دائن، فقم بتحديد هذا الخيار للاحتفاظ بالكمية المتبقية في الأمر.</span><span class="sxs-lookup"><span data-stu-id="e6794-198">If you're posting a credit note, select this option to keep the remaining quantity on order.</span></span> <span data-ttu-id="e6794-199">أما في حالة إلغاء تحديد هذا الخيار، فإنه يتم تعيين الكمية المتبقية إلى 0 (صفر).</span><span class="sxs-lookup"><span data-stu-id="e6794-199">If this option is cleared, the remaining quantity is set to 0 (zero).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6794-200">تحديث ملخص لـ</span><span class="sxs-lookup"><span data-stu-id="e6794-200">Summary update for</span></span></td>
<td><span data-ttu-id="e6794-201">حدد الطريقة التي يجب بها تلخيص أوامر المبيعات المتعددة.</span><span class="sxs-lookup"><span data-stu-id="e6794-201">Select how multiple sales orders should be summarized:</span></span>
<ul>
<li><span data-ttu-id="e6794-202"><strong>لا شيء</strong> – عدم تلخيص أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="e6794-202"><strong>None</strong> – Don't summarize sales orders.</span></span> <span data-ttu-id="e6794-203">على سبيل المثال، سيتم إنشاء فاتورة منفصلة لكل أمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="e6794-203">For example, a separate invoice will be created for each sales order.</span></span></li>
<li><span data-ttu-id="e6794-204"><strong>حساب الفاتورة</strong> – تلخيص كافة الأوامر المحددة وفقًا للمعايير المحددة في صفحة <strong>معلمات تحديث الملخص</strong>.</span><span class="sxs-lookup"><span data-stu-id="e6794-204"><strong>Invoice account</strong> – Summarize all selected orders, based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span></li>
<li><span data-ttu-id="e6794-205"><strong>أمر</strong> – تلخيص مجموعة محددة من الأوامر في أمر واحد تقوم بتحديده.</span><span class="sxs-lookup"><span data-stu-id="e6794-205"><strong>Order</strong> – Summarize a selected range of orders into one order that you specify.</span></span> <span data-ttu-id="e6794-206">ويتم تلخيص الأوامر وفقًا للمعايير التي تم إعدادها في صفحة <strong>معلمات تحديث الملخص</strong>.</span><span class="sxs-lookup"><span data-stu-id="e6794-206">The orders are summarized based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span> <span data-ttu-id="e6794-207">وإذا قمت بتحديد هذا الخيار، فيجب عليك تحديد حقل <strong>أمر المبيعات</strong>.</span><span class="sxs-lookup"><span data-stu-id="e6794-207">If you select this option, you must select a value in the <strong>Sales order</strong> field.</span></span></li>
<li><span data-ttu-id="e6794-208"><strong>الملخص التلقائي</strong> – في حالة تحديد تحديثات الملخص في صفحة <strong>تحديث الملخص</strong>، فقم بتلخيص جميع الأوامر المحددة، استنادًا إلى المعايير التي تم إعدادها في صفحة <strong>معلمات تحديث الملخص</strong>.</span><span class="sxs-lookup"><span data-stu-id="e6794-208"><strong>Automatic summary</strong> – If summary updates have been specified on the <strong>Summary update</strong> page, summarize all selected orders, based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span> <span data-ttu-id="e6794-209">وإذا لم يتم تحديد تحديثات الملخص، فإنه يتم ترحيل الأمر بشكل منفصل.</span><span class="sxs-lookup"><span data-stu-id="e6794-209">If summary updates haven't been specified, the order is posted separately.</span></span></li>
<li><span data-ttu-id="e6794-210"><strong>إيصال التعبئة</strong> – تلخيص مجموعة محددة من الأوامر في فاتورة واحدة لكل إيصال تعبئة.</span><span class="sxs-lookup"><span data-stu-id="e6794-210"><strong>Packing slip</strong> – Summarize a selected range of orders into one invoice for each packing slip.</span></span> <span data-ttu-id="e6794-211">لا يتوفر هذا الخيار إلا إذا تم تحديد <strong>إيصال التعبئة</strong> في حقل <strong>الكمية</strong>.</span><span class="sxs-lookup"><span data-stu-id="e6794-211">This option is available only if <strong>Packing slip</strong> is selected in the <strong>Quantity</strong> field.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>






