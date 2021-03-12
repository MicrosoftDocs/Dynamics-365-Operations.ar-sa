---
title: استكشاف أخطاء إيصالات استلام المنتجات والفوترة وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع إيصالات استلام المنتجات والفوترة.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 22b1abec0c6dd5f571e604c5c07379b397b8bdaa
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999043"
---
# <a name="troubleshoot-product-receipts-and-invoicing"></a><span data-ttu-id="88df9-103">استكشاف أخطاء إيصالات استلام المنتجات والفوترة وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="88df9-103">Troubleshoot product receipts and invoicing</span></span>

<span data-ttu-id="88df9-104">يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع إيصالات استلام المنتجات والفوترة.</span><span class="sxs-lookup"><span data-stu-id="88df9-104">This topic describes how to fix issues that you might encounter while you work with product receipts and invoicing.</span></span>

## <a name="i-cant-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a><span data-ttu-id="88df9-105">لا يمكنني ترحيل أكثر من فاتورة واحدة لبند أمر شراء لديه أصناف تستند إلى فئة.</span><span class="sxs-lookup"><span data-stu-id="88df9-105">I can't post more than one invoice for a purchase order line that has category-based items.</span></span>

<span data-ttu-id="88df9-106">تكون الكمية إلزامية إذا كنت ترغب في ترحيل الفواتير.</span><span class="sxs-lookup"><span data-stu-id="88df9-106">A quantity is mandatory if you want to post invoices.</span></span> <span data-ttu-id="88df9-107">وبالتالي، إذا تمت فوترة  الكمية الكامل لأحد البنود لمبلغ جزئي فقط، فلن تتمكن من فوترة المبلغ المتبقي على فاتورة أخرى.</span><span class="sxs-lookup"><span data-stu-id="88df9-107">Therefore, if the full quantity of a line has been invoiced for only a partial amount, you won't be able to invoice the remaining amount on another invoice.</span></span>

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a><span data-ttu-id="88df9-108">أتلقى الخطأ "لم يتم تعيين مرجع الكائن" أثناء تأكيد أمر الشراء، أو حدث الاستثناء "تم طرح استثناء بواسطة هدف استدعاء أثناء ترحيل فواتير المورّد.</span><span class="sxs-lookup"><span data-stu-id="88df9-108">I receive an "Object reference not set" error during purchase order confirmation, or an "Exception has been thrown by the target of an invocation" exception occurs during vendor invoice posting.</span></span>

<span data-ttu-id="88df9-109">قد تحدث هذه المشكلة بسبب عدم الاتساق في توزيعات أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="88df9-109">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="88df9-110">لحل هذه المشكلة وإعادة تعيين أمر الشراء إلى الحالة *مسودة*، انتقل إلى **التدبير والتوريد \> المهام الدورية \> تنظيف \> إعادة تعيين توزيع أمر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="88df9-110">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="88df9-111">لمزيد من المعلومات، راجع منشور المدونة التالي: [حل أخطاء توزيع أمر الشراء في Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="88df9-111">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="i-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a><span data-ttu-id="88df9-112">لا يمكن دمج إيصالات استلام منتجات متعددة في أمر شراء واحد.</span><span class="sxs-lookup"><span data-stu-id="88df9-112">I can't consolidate multiple product receipts into a single purchase order.</span></span>

<span data-ttu-id="88df9-113">لا يمكنك دمج إيصالات استلام منتجات متعددة في أمر شراء واحد إذا كانت بنود إيصال استلام المنتجات المختلفة ذات تواريخ محاسبية مختلفة.</span><span class="sxs-lookup"><span data-stu-id="88df9-113">You can't consolidate multiple product receipts into a single purchase order if the different product receipt lines have different accounting dates.</span></span>

<span data-ttu-id="88df9-114">في الإصدارات السابقة من Microsoft Dynamics 365 Supply Chain Management، كان الدمج مسموحًا به في هذه الحالة.</span><span class="sxs-lookup"><span data-stu-id="88df9-114">In earlier versions of Microsoft Dynamics 365 Supply Chain Management, consolidation was allowed in this situation.</span></span> <span data-ttu-id="88df9-115">ومع ذلك، تعتبر الممارسة عرضة للخطأ.</span><span class="sxs-lookup"><span data-stu-id="88df9-115">However, the practice is prone to error.</span></span> <span data-ttu-id="88df9-116">يجب ألا يختلف التاريخ المحاسبي في بنود أمر الشراء التي تم إنشاؤها عن التاريخ المحاسبي الموجود في بنود إيصال استلام المنتجات التي تم إنشاء بنود أمر الشراء منها.</span><span class="sxs-lookup"><span data-stu-id="88df9-116">The accounting date on the purchase order lines that are created should not differ from the accounting date on the product receipt lines that those purchase order lines were created from.</span></span> <span data-ttu-id="88df9-117">(يتطابق التاريخ المحاسبي على بنود أمر الشراء مع التاريخ المحاسبي على  رأس أمر  الشراء.) وبالتالي، لم يعد يُسمح بدمج إيصالات استلام متعددة في أمر شراء واحد.</span><span class="sxs-lookup"><span data-stu-id="88df9-117">(The accounting date on the purchase order lines matches the accounting date on the purchase order header.) Therefore, the consolidation of multiple product receipts into a single purchase orders is no longer allowed.</span></span>

<span data-ttu-id="88df9-118">يتم استخدام التاريخ المحاسبي، على سبيل المثال، لحجوزان الموازنة والالتزام بها.</span><span class="sxs-lookup"><span data-stu-id="88df9-118">The accounting date is used, for example, for budget reservations and encumbrance.</span></span> <span data-ttu-id="88df9-119">وبالتالي، يجب ان يتم الاحتفاظ بها أثناء الانتقال من إيصال استلام المنتجات إلى أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="88df9-119">Therefore, it should be kept during the transition from product receipt to purchase order.</span></span>

## <a name="when-product-receipts-are-canceled-transactions-can-be-posted-to-a-suspended-ledger-account"></a><span data-ttu-id="88df9-120">عند إلغاء إيصالات استلام المنتجات، يمكن ترحيل الحركات إلى حساب دفتر أستاذ معلق.</span><span class="sxs-lookup"><span data-stu-id="88df9-120">When product receipts are canceled, transactions can be posted to a suspended ledger account.</span></span>

### <a name="issue-description"></a><span data-ttu-id="88df9-121">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="88df9-121">Issue description</span></span>

<span data-ttu-id="88df9-122">إذا تم إلغاء إيصال استلام المنتجات، فإن النظام يسمح بترحيل الحركات إلى حسابات دفتر أستاذ معلقة، على الرغم من كون الحسابات الرئيسية معلقة.</span><span class="sxs-lookup"><span data-stu-id="88df9-122">If a product receipt is canceled, the system allows transactions to be posted to suspended ledger accounts, even though the main accounts are suspended.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="88df9-123">إعادة إنتاج المشكلة</span><span class="sxs-lookup"><span data-stu-id="88df9-123">Reproduce the issue</span></span>

<span data-ttu-id="88df9-124">يعرض الإجراء التالي إحدى الطرق لإعادة إنتاج المشكلة.</span><span class="sxs-lookup"><span data-stu-id="88df9-124">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="88df9-125">في الصفحة **معلمات الحسابات الدائنة**‬‏‫، على علامة التبويب **عام**، تأكد من تعيين الخيار **ترحيل إيصال استلام المنتجات إلى دفتر الأستاذ** إلى *نعم*.</span><span class="sxs-lookup"><span data-stu-id="88df9-125">On the **Accounts payable parameters** page, on the **General** tab, make sure that the **Post product receipt in ledger** option is set to *Yes*.</span></span>
1. <span data-ttu-id="88df9-126">أنشئ أمر شراء، وأضف بند أمر لديه كمية من *1,000* لمنتج.</span><span class="sxs-lookup"><span data-stu-id="88df9-126">Create a purchase order, and add an order line that has a quantity of *1,000* for a product.</span></span>
1. <span data-ttu-id="88df9-127">أكد أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="88df9-127">Confirm the purchase order.</span></span>
1. <span data-ttu-id="88df9-128">قم بترحيل إيصال استلام المنتجات وتحقق من الإيصالات.</span><span class="sxs-lookup"><span data-stu-id="88df9-128">Post the product receipt, and check the vouchers.</span></span>
1. <span data-ttu-id="88df9-129">قم بتعليق الحسابين الرئيسين ذي الصلة، *200140* و *140200*.</span><span class="sxs-lookup"><span data-stu-id="88df9-129">Suspend the relevant main accounts, *200140* and *140200*.</span></span>
1. <span data-ttu-id="88df9-130">قم بإلغاء إيصال استلام المنتجات المرحّل.</span><span class="sxs-lookup"><span data-stu-id="88df9-130">Cancel the posted product receipt.</span></span>
1. <span data-ttu-id="88df9-131">لاحظ أنه يمكن ترحيل الحركات إلى حسابات دفتر الأستاذ المعلقة.</span><span class="sxs-lookup"><span data-stu-id="88df9-131">Notice that transactions can be posted to the suspended leger accounts.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="88df9-132">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="88df9-132">Issue resolution</span></span>

<span data-ttu-id="88df9-133">يمكن ترحيل الحركات إلى حسابات دفتر الأستاذ المعلقة عند إلغاء إيصالات استلام المنتجات، لأن هذا السلوك يسمح بالترحيلات الصحيحة.</span><span class="sxs-lookup"><span data-stu-id="88df9-133">Transactions can be posted to the suspended leger accounts when product receipts are canceled, because this behavior allows for correct postings.</span></span>

## <a name="a-product-receipt-voucher-number-is-consumed-even-if-no-financial-voucher-is-generated-during-product-receipt"></a><span data-ttu-id="88df9-134">يتم استهلاك رقم إيصال استلام المنتجات حتى في حالة عدم إنشاء إيصال مالي اثناء استلام المنتجات.</span><span class="sxs-lookup"><span data-stu-id="88df9-134">A product receipt voucher number is consumed even if no financial voucher is generated during product receipt.</span></span>

<span data-ttu-id="88df9-135">إذا تم تعيين الخيار **استحقاق الالتزام على إيصال استلام المنتجات‬** إلى *لا* لمجموعة نماذج الأصناف، لن تحدث أي عمليات ترحيل لدفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="88df9-135">If the **Accrue liability on product receipt** option is set to *No* for the item model group, no postings to the general ledger will occur.</span></span> <span data-ttu-id="88df9-136">ومع ذلك، سيتم تسجيل حدث فعلي لغرض المحاسبة في دفتر الأستاذ الفرعي، ويتطلب ذلك الحدث رقم إيصال.</span><span class="sxs-lookup"><span data-stu-id="88df9-136">However, a physical event will be recorded for the purpose of accounting in a subledger, and that event requires a voucher number.</span></span> <span data-ttu-id="88df9-137">رقم الإيصال هذا هو رقم الإيصال الذي يُشار في حركات المخزون.</span><span class="sxs-lookup"><span data-stu-id="88df9-137">This voucher number is the voucher number that is referenced in the inventory transactions.</span></span>

<span data-ttu-id="88df9-138">ننصحك بتعيين الخيار **استحقاق الالتزام على إيصال استلام المنتجات‬** إلى *نعم*، كما تم وصفه في منشور المدونة التالي: [ترحيل المصروفات المتنوعة عند استلام المنتجات](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span><span class="sxs-lookup"><span data-stu-id="88df9-138">We recommend that you set the **Accrue liability on product receipt** option to *Yes*, as described in the following blog post: [Post Misc. charges at time of product receipt](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span></span>

## <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a><span data-ttu-id="88df9-139">الإعداد "ترحيل إلى حساب مصاريف في دفتر الأستاذ" ليس قيد التشغيل</span><span class="sxs-lookup"><span data-stu-id="88df9-139">The Post to charge account in ledger setting isn't turned on.</span></span>

### <a name="issue-description"></a><span data-ttu-id="88df9-140">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="88df9-140">Issue description</span></span>

<span data-ttu-id="88df9-141">تحدث هذه المشكلة عند فوترة أمر شراء، إذا تم تعيين الخيار **ترحيل إلى حساب مصاريف في دفتر الأستاذ** إلى *نعم* على علامة تبويب **الفاتورة** في صفحة **معلمات الحسابات الدائنة**.</span><span class="sxs-lookup"><span data-stu-id="88df9-141">This issue occurs when a purchase order is invoiced, if the **Post to charge account in ledger** option is set to *Yes* on the **Invoice** tab of the **Accounts payable parameters** page.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="88df9-142">إعادة إنتاج المشكلة</span><span class="sxs-lookup"><span data-stu-id="88df9-142">Reproduce the issue</span></span>

<span data-ttu-id="88df9-143">يعرض الإجراء التالي إحدى الطرق لإعادة إنتاج المشكلة.</span><span class="sxs-lookup"><span data-stu-id="88df9-143">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="88df9-144">انتقل إلى **الحسابات الدائنة \> الإعداد \> محددات الحسابات الدائنة**.</span><span class="sxs-lookup"><span data-stu-id="88df9-144">Go to **Accounts payable \> Setup \> Accounts payable parameters**.</span></span>
1. <span data-ttu-id="88df9-145">من علامة التبويب **الفاتورة**، قم بتعيين الخيار **ترحيل إلى حساب مصاريف في دفتر الأستاذ** إلى *نعم*.</span><span class="sxs-lookup"><span data-stu-id="88df9-145">On the **Invoice** tab, set the **Post to charge account in ledger** option to *Yes*.</span></span>
1. <span data-ttu-id="88df9-146">انتقل إلى **إدارة المخزون \> الإعداد \> الترحيل \> الترحيل**.</span><span class="sxs-lookup"><span data-stu-id="88df9-146">Go to **Inventory management \> Setup \> Posting \> Posting**.</span></span>
1. <span data-ttu-id="88df9-147">في علامة التبويب **أمر الشراء**، تأكد من أنك حذفت جميع البنود في نفقات الشراء الخاصة بالمنتج.</span><span class="sxs-lookup"><span data-stu-id="88df9-147">On the **Purchase order** tab, make sure that you've deleted all the lines in the purchase expenditure for the product.</span></span>
1. <span data-ttu-id="88df9-148">انتقل إلى **الحسابات الدائنة \> أوامر الشراء \> جميع أوامر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="88df9-148">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="88df9-149">إنشاء أمر شراء.</span><span class="sxs-lookup"><span data-stu-id="88df9-149">Create a purchase order.</span></span> <span data-ttu-id="88df9-150">في الحقل **حساب المورّد**، حدد *1001 المستلزمات المكتبية Acme*.</span><span class="sxs-lookup"><span data-stu-id="88df9-150">In the **Vendor account** field, select *1001 Acme Office Supplies*.</span></span>
1. <span data-ttu-id="88df9-151">أضف بند أمر شراء يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="88df9-151">Add a purchase order line that has the following settings:</span></span>

    - <span data-ttu-id="88df9-152">**رقم الصنف:** *D0011 بروجيكتور ليزر*</span><span class="sxs-lookup"><span data-stu-id="88df9-152">**Item number:** *D0011 Laser Projector*</span></span>
    - <span data-ttu-id="88df9-153">**الموقع:** *1*</span><span class="sxs-lookup"><span data-stu-id="88df9-153">**Site:** *1*</span></span>
    - <span data-ttu-id="88df9-154">**المستودع:** *11*</span><span class="sxs-lookup"><span data-stu-id="88df9-154">**Warehouse:** *11*</span></span>
    - <span data-ttu-id="88df9-155">**الكمية:** *4*</span><span class="sxs-lookup"><span data-stu-id="88df9-155">**Quantity:** *4*</span></span>

1. <span data-ttu-id="88df9-156">في جزء الإجراءات، في علامة تبويب **الشراء** في مجموعة **الإجراء**، حدد **تأكيد**.</span><span class="sxs-lookup"><span data-stu-id="88df9-156">On the Action Pane, on the **Purchase** tab, in the **Action** group, select **Confirm**.</span></span>
1. <span data-ttu-id="88df9-157">في جزء الإجراءات، في علامة التبويب **استلام** في المجموعة **إنشاء‬**، حدد **إيصال استلام المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="88df9-157">On the Action Pane, on the **Receive** tab, in the **Generate** group, select **Product receipt**.</span></span>
1. <span data-ttu-id="88df9-158">في مربع الحوار **ترحيل إيصال استلام المنتجات**، في الحقل **إيصال استلام المنتجات**، أدخل رقمًا عشوائيًا، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="88df9-158">In the **Posting product receipt** dialog box, in the **Product receipt** field, enter an arbitrary number, and then select **OK**.</span></span>
1. <span data-ttu-id="88df9-159">في جزء الإجراءات، في علامة التبويب **الفاتورة**، في المجموعة **إنشاء**، حدد **فاتورة**.</span><span class="sxs-lookup"><span data-stu-id="88df9-159">On the Action Pane, on the **Invoice** tab, in the **Generate** group, select **Invoice**.</span></span>
1. <span data-ttu-id="88df9-160">في حقل **الرقم**، أدخل رقمًا عشوائيًا كرقم الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="88df9-160">In the **Number** field, enter an arbitrary number as the invoice number.</span></span>
1. <span data-ttu-id="88df9-161">قم بتحديث حالة المطابقة، ثم قم بالترحيل.</span><span class="sxs-lookup"><span data-stu-id="88df9-161">Update the match status, and post.</span></span>
1. <span data-ttu-id="88df9-162">لاحظ أنك تتلقي الآن رسالة الخطأ التالية عند إنشاء فاتورة من أمر شراء: "رقم الحساب لنوع الحركة "نفقات الشراء" للمنتج غير موجود".</span><span class="sxs-lookup"><span data-stu-id="88df9-162">Notice that you now receive the following error when you generate an invoice from a purchase order: "Account number for transaction type Purchase expenditure for product does not exist."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="88df9-163">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="88df9-163">Issue resolution</span></span>

<span data-ttu-id="88df9-164">يتوقف ذلك على إعدادات المعلمات الخاصة بالفواتير ومجموعات الفواتير.</span><span class="sxs-lookup"><span data-stu-id="88df9-164">This depends on the parameter settings for invoices and invoice groups.</span></span> <span data-ttu-id="88df9-165">لمزيد من المعلومات، راجع منشور المدونة التالي: [محاسبة مصروفات الشراء وتغييرات المخزون](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).</span><span class="sxs-lookup"><span data-stu-id="88df9-165">For more information, see the following blog post: [Accounting for Purchase charge and Stock variation](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).</span></span>
