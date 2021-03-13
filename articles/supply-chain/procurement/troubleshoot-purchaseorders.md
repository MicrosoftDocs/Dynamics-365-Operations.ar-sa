---
title: استكشاف أخطاء أوامر الشراء وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع أوامر الشراء.
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
ms.openlocfilehash: 7b65c23fc7ac04fc30c0001bee9541a475026018
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007481"
---
# <a name="troubleshoot-purchase-orders"></a><span data-ttu-id="8aaea-103">استكشاف أخطاء أوامر الشراء وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="8aaea-103">Troubleshoot purchase orders</span></span>

<span data-ttu-id="8aaea-104">يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع أوامر الشراء.</span><span class="sxs-lookup"><span data-stu-id="8aaea-104">This topic describes how to fix issues that you might encounter while you work with purchase orders.</span></span>

## <a name="an-action-can-be-completed-only-after-the-line-number-is-fully-distributed"></a><span data-ttu-id="8aaea-105">يمكن إكمال الإجراء فقط بعد توزيع رقم البند بشكل كامل.</span><span class="sxs-lookup"><span data-stu-id="8aaea-105">An action can be completed only after the line number is fully distributed.</span></span>

<span data-ttu-id="8aaea-106">قد تحدث هذه المشكلة بسبب عدم الاتساق في توزيعات أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="8aaea-106">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="8aaea-107">لحل هذه المشكلة وإعادة تعيين أمر الشراء إلى الحالة *مسودة*، انتقل إلى **التدبير والتوريد \> المهام الدورية \> تنظيف \> إعادة تعيين توزيع أمر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="8aaea-107">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="8aaea-108">لمزيد من المعلومات، راجع منشور المدونة التالي: [حل أخطاء توزيع أمر الشراء في Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="8aaea-108">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="when-purchase-orders-are-imported-through-data-management-purchase-order-line-numbers-dont-follow-the-increment-that-defined-in-system-parameters"></a><span data-ttu-id="8aaea-109">عند استيراد أوامر الشراء من خلال إدارة البيانات، لن تتبع بنود أمر الشراء الزيادة التي تم تحديدها في معلمات النظام.</span><span class="sxs-lookup"><span data-stu-id="8aaea-109">When purchase orders are imported through data management, purchase order line numbers don't follow the increment that defined in system parameters.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8aaea-110">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="8aaea-110">Issue description</span></span>

<span data-ttu-id="8aaea-111">بشكل افتراضي، لا تستخدم أرقام البنود المُنشأة بشكل تلقائي لبنود أوامر الشراء المستوردة عبر كيان البيانات *بنود أمر الشراء V2* زيادة رقم بند النظام المحددة في معلمات النظام.</span><span class="sxs-lookup"><span data-stu-id="8aaea-111">By default, automatically generated line numbers for purchase order lines that are imported through the *Purchase order lines V2* data entity don't use the system line number increment that is specified in system parameters.</span></span> <span data-ttu-id="8aaea-112">إذا أنشأت أمر شراء بشكل يدوي وأضفت البنود عبر واجهة المستخدم (UI)، يتم زيادة أرقام البنود بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="8aaea-112">If you manually create a purchase order and add lines through the user interface (UI), the line numbers are incremented correctly.</span></span> <span data-ttu-id="8aaea-113">ومع ذلك، إذا كنت تستخدم إطار عمل إدارة البيانات (DMF)، فإنها لن تزداد بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="8aaea-113">However, if you use the Data management framework (DMF), they aren't incremented correctly.</span></span>

<span data-ttu-id="8aaea-114">تحدث هذه المشكلة لأن النظام يستخدم أسلوب إطار عمل إدارة البيانات (DMF) لتعيين أرقام البنود إذا لم تكن أرقام البنود معينة في الكيان المستورد، وذلك عند استيراد البنود عبر DMF.</span><span class="sxs-lookup"><span data-stu-id="8aaea-114">This issue occurs because, when you import lines via DMF, if line numbers aren't already assigned in the imported entity, the system uses DMF's method for assigning them.</span></span> <span data-ttu-id="8aaea-115">تقوم هذه الطريقة دائمًا بزيادة أرقام البنود بمقدار رقم واحد.</span><span class="sxs-lookup"><span data-stu-id="8aaea-115">That method always increments line numbers by one.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="8aaea-116">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="8aaea-116">Issue workaround</span></span>

<span data-ttu-id="8aaea-117">تأكد من أن أرقام البنود المطلوبة معطاة بالفعل في حقول أرقام بنود كيان البيانات عندما تستورد بنود أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="8aaea-117">Make sure that the desired line numbers are already given in the data entity line number fields when you import the purchase order lines.</span></span> <span data-ttu-id="8aaea-118">في هذه الحالة، لن يستبدل DMF أرقام البنود.</span><span class="sxs-lookup"><span data-stu-id="8aaea-118">In this case, DMF won't overwrite the line numbers.</span></span>

## <a name="a-default-tax-group-and-a-default-cash-discount-arent-filled-in-from-the-invoice-account"></a><span data-ttu-id="8aaea-119">لا يتم ملء مجموعة الضرائب الافتراضية والخصم النقدي الافتراضي من حساب الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="8aaea-119">A default tax group and a default cash discount aren't filled in from the invoice account.</span></span>

<span data-ttu-id="8aaea-120">إذا كنت تستخدم حساب فاتورة يختلف عن حساب العميل، فلن يتم ملء مجموعة الضرائب الافتراضية والخصم النقدي الافتراضي من حساب الفاتورة عند إنشاء أمر شراء.</span><span class="sxs-lookup"><span data-stu-id="8aaea-120">If you're using an invoice account that differs from the customer account, a default tax group and a default cash discount aren't filled in from the invoice account when a purchase order is created.</span></span>

<span data-ttu-id="8aaea-121">يتم هذا السلوك بسبب التصميم.</span><span class="sxs-lookup"><span data-stu-id="8aaea-121">This behavior is by design.</span></span> <span data-ttu-id="8aaea-122">تعتمد القيم الافتراضية لمجموعة الضرائب والخصومات النقدية ومعلومات السعر الأخرى إلى حساب العميل، وليس حساب الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="8aaea-122">The default values for the tax group, cash discounts, and other price information are based on the customer account, not the invoice account.</span></span>

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a><span data-ttu-id="8aaea-123">أتلقى الخطأ "لم يتم تعيين مرجع الكائن" أثناء تأكيد أمر الشراء، أو حدث الاستثناء "تم طرح استثناء بواسطة هدف استدعاء أثناء ترحيل فواتير المورّد.</span><span class="sxs-lookup"><span data-stu-id="8aaea-123">I receive an "Object reference not set" error during purchase order confirmation, or an "Exception has been thrown by the target of an invocation" exception occurs during vendor invoice posting.</span></span>

<span data-ttu-id="8aaea-124">قد تحدث هذه المشكلة بسبب عدم الاتساق في توزيعات أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="8aaea-124">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="8aaea-125">لحل هذه المشكلة وإعادة تعيين أمر الشراء إلى الحالة *مسودة*، انتقل إلى **التدبير والتوريد \> المهام الدورية \> تنظيف \> إعادة تعيين توزيع أمر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="8aaea-125">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="8aaea-126">لمزيد من المعلومات، راجع منشور المدونة التالي: [حل أخطاء توزيع أمر الشراء في Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="8aaea-126">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a><span data-ttu-id="8aaea-127">هناك زيادة أو نقص في التوزيع في توزيع محاسبي واحد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="8aaea-127">One or more accounting distributions are either over-distributed or under-distributed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8aaea-128">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="8aaea-128">Issue description</span></span>

<span data-ttu-id="8aaea-129">تتلقي رسالة الخطأ التالية: "هناك زيادة أو نقص في التوزيع في توزيع محاسبي واحد أو أكثر."</span><span class="sxs-lookup"><span data-stu-id="8aaea-129">You receive the following error: "One or more accounting distributions is either over-distributed or under-distributed."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8aaea-130">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="8aaea-130">Issue resolution</span></span>

<span data-ttu-id="8aaea-131">قد تحدث هذه المشكلة بسبب عدم الاتساق في توزيعات أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="8aaea-131">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="8aaea-132">لحل هذه المشكلة وإعادة تعيين أمر الشراء إلى الحالة *مسودة*، انتقل إلى **التدبير والتوريد \> المهام الدورية \> تنظيف \> إعادة تعيين توزيع أمر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="8aaea-132">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="8aaea-133">لمزيد من المعلومات، راجع منشور المدونة التالي: [حل أخطاء توزيع أمر الشراء في Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="8aaea-133">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="can-i-show-only-purchase-orders-that-i-created"></a><span data-ttu-id="8aaea-134">هل يمكنني إظهار فقط أوامر الشراء التي قمت بإنشائها؟</span><span class="sxs-lookup"><span data-stu-id="8aaea-134">Can I show only purchase orders that I created?</span></span>

<span data-ttu-id="8aaea-135">هذه الوظيفة غير متوفرة حاليًا.</span><span class="sxs-lookup"><span data-stu-id="8aaea-135">This functionality isn't currently available.</span></span>

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a><span data-ttu-id="8aaea-136">هل يمكنني حجز المخزون وإنشاء حركات مقابل مخزون مسجل في أمر شراء؟</span><span class="sxs-lookup"><span data-stu-id="8aaea-136">Can I reserve inventory and create transactions against registered inventory on a purchase order?</span></span>

### <a name="issue-description"></a><span data-ttu-id="8aaea-137">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="8aaea-137">Issue description</span></span>

<span data-ttu-id="8aaea-138">حتى عندما تكون حالة الأصناف *مسجلة* على أمر شراء، لا يزال بإمكانك حجز المخزون.</span><span class="sxs-lookup"><span data-stu-id="8aaea-138">Even when items are in a *Registered* state on a purchase order, you can still reserve the inventory.</span></span> <span data-ttu-id="8aaea-139">بمعنىً آخر، يمكنك إنشاء حركات في مقابل المخزون المسجل.</span><span class="sxs-lookup"><span data-stu-id="8aaea-139">In other words, you can create transactions against the registered inventory.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="8aaea-140">إعادة إنتاج المشكلة</span><span class="sxs-lookup"><span data-stu-id="8aaea-140">Reproduce the issue</span></span>

<span data-ttu-id="8aaea-141">يعرض الإجراء التالي إحدى الطرق لإعادة إنتاج المشكلة.</span><span class="sxs-lookup"><span data-stu-id="8aaea-141">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="8aaea-142">إنشاء أمر شراء.</span><span class="sxs-lookup"><span data-stu-id="8aaea-142">Create a purchase order.</span></span>
2. <span data-ttu-id="8aaea-143">تسجيل بند أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="8aaea-143">Register the purchase order line.</span></span>
3. <span data-ttu-id="8aaea-144">لاحظ أنه يمكنك إنشاء حجوزات أو حركات في مقابل المخزون المسجل.</span><span class="sxs-lookup"><span data-stu-id="8aaea-144">Notice that you can generate reservations or transactions against the registered inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8aaea-145">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="8aaea-145">Issue resolution</span></span>

<span data-ttu-id="8aaea-146">يتم هذا السلوك بسبب التصميم.</span><span class="sxs-lookup"><span data-stu-id="8aaea-146">This behavior is by design.</span></span> <span data-ttu-id="8aaea-147">الأمر المتوقع هو ان الأصناف المسجلة قد وصلت فعليًا إلى المستودع أو المخزون، وأنها بالتالي متاحة للحجز.</span><span class="sxs-lookup"><span data-stu-id="8aaea-147">The expectation is that the registered items have physically arrived in the warehouse or inventory, and that they are therefore available for reservation.</span></span>

## <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a><span data-ttu-id="8aaea-148">لا تعكس أوامر الشراء إعدادات اللغة الخاصة بالكيان القانوني.</span><span class="sxs-lookup"><span data-stu-id="8aaea-148">Purchase orders don't reflect the language settings of the legal entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8aaea-149">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="8aaea-149">Issue description</span></span>

<span data-ttu-id="8aaea-150">يظهر اسم المنتج في أمر الشراء بلغة النظام بدلاً من اللغة التي تم تعيينها للكيان القانوني حيث تم إنشاء أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="8aaea-150">The product name on a purchase order is shown in the system language instead of the language that is set for the legal entity where the purchase order was created.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="8aaea-151">إعادة إنتاج المشكلة</span><span class="sxs-lookup"><span data-stu-id="8aaea-151">Reproduce the issue</span></span>

<span data-ttu-id="8aaea-152">يعرض الإجراء التالي إحدى الطرق لإعادة إنتاج المشكلة.</span><span class="sxs-lookup"><span data-stu-id="8aaea-152">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="8aaea-153">قم بتعيين لغة النظام إلى *EN-US* (US English).</span><span class="sxs-lookup"><span data-stu-id="8aaea-153">Set the system language to *EN-US* (US English).</span></span>
1. <span data-ttu-id="8aaea-154">تأكد من وجود منتج حيث تتم المحافظة على اللغتين *EN-US* و *DE* (German) للترجمات واسم المنتج.</span><span class="sxs-lookup"><span data-stu-id="8aaea-154">Make sure that there is a product where the *EN-US* and *DE* (German) languages are maintained for translations of the product name.</span></span>
1. <span data-ttu-id="8aaea-155">قم بتغيير لغة الكيان القانوني إلى *DE*.</span><span class="sxs-lookup"><span data-stu-id="8aaea-155">Change the language of a legal entity to *DE*.</span></span>
1. <span data-ttu-id="8aaea-156">في الكيان القانوني حيث تم تعيين *DE‎* كلغة، أنشئ أمر شراء يتضمن المنتج.</span><span class="sxs-lookup"><span data-stu-id="8aaea-156">In the legal entity where *DE* is set as the language, create a purchase order that includes the product.</span></span>
1. <span data-ttu-id="8aaea-157">لاحظ استمرار ظهور اسم المنتج باللغة US English (لغة النظام).</span><span class="sxs-lookup"><span data-stu-id="8aaea-157">Notice that the product name is still shown in US English (the system language).</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8aaea-158">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="8aaea-158">Issue resolution</span></span>

<span data-ttu-id="8aaea-159">يتم هذا السلوك بسبب التصميم.</span><span class="sxs-lookup"><span data-stu-id="8aaea-159">This behavior is by design.</span></span> <span data-ttu-id="8aaea-160">على أوامر الشراء، يظهر المنتج دائمًا بلغة النظام.</span><span class="sxs-lookup"><span data-stu-id="8aaea-160">On purchase orders, the product is always shown in the system language.</span></span> <span data-ttu-id="8aaea-161">يتم استخدام لغة أمر الشراء عند إنشاء دفتر يومية التأكيد.</span><span class="sxs-lookup"><span data-stu-id="8aaea-161">The purchase order language is used when a confirmation journal is created.</span></span>

## <a name="the-approved-vendor-list-by-product-entity-doesnt-allow-the-effective-date-to-be-changed"></a><span data-ttu-id="8aaea-162">لا تسمح قائمة المورّدين المعتمدين حسب كيان المنتج بتغيير تاريخ السريان.</span><span class="sxs-lookup"><span data-stu-id="8aaea-162">The Approved vendor list by product entity doesn't allow the effective date to be changed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8aaea-163">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="8aaea-163">Issue description</span></span>

<span data-ttu-id="8aaea-164">هناك منتج لديه مورّد معتمد لديه، على سبيل المثال، تاريخ السريان 11 يناير 2018 (*01/11/2018*)، وتاريخ انتهاء الصلاحية *إطلاقًا*.</span><span class="sxs-lookup"><span data-stu-id="8aaea-164">A product has an approved vendor that has, for example, an effective date of January 11, 2018 (*01/11/2018*), and an expiration date of *Never*.</span></span> <span data-ttu-id="8aaea-165">إذا حاولت تغيير تاريخ السريان إلى 10 يناير 2018 (*01/10/2018*)، أو 12 يناير 2018 (*01/12/2018*)، تتلقى رسالة الخطأ التالية:</span><span class="sxs-lookup"><span data-stu-id="8aaea-165">If you try to change the effective date to January 10, 2018 (*01/10/2018*), or January 12, 2018 (*01/12/2018*), you receive the following error:</span></span>

> <span data-ttu-id="8aaea-166">لا يمكن إنشاء سجل في قائمة المورّدين المعتمدين (PdsApproveVendorList).</span><span class="sxs-lookup"><span data-stu-id="8aaea-166">Cannot create a record in Approved supplier list (PdsApproveVendorList).</span></span> <span data-ttu-id="8aaea-167">يجب أن تكون قيمة "انتهاء الصلاحية" أكبر من قيمة "ساري المفعول‬" أو مساوية لها.</span><span class="sxs-lookup"><span data-stu-id="8aaea-167">The 'Expiration' value needs to be greater than or equal to the 'Effective' value.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8aaea-168">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="8aaea-168">Issue resolution</span></span>

<span data-ttu-id="8aaea-169">يمكنك فقط تمديد الفترة التي تم خلالها الموافقة على المورّد.</span><span class="sxs-lookup"><span data-stu-id="8aaea-169">You can only extend the period that the vendor is approved for.</span></span> <span data-ttu-id="8aaea-170">تطبيق القواعد التالية:</span><span class="sxs-lookup"><span data-stu-id="8aaea-170">The following rules apply:</span></span>

- <span data-ttu-id="8aaea-171">لتغيير تاريخ السريان بحيث يقع قبل أي من السجلات الموجودة (الفترات) الخاصة بمورّد الصنف، يجب أن يكون تاريخ انتهاء صلاحية الفترة الجديدة قبل كافة تواريخ انتهاء الصلاحية في السجلات الموجودة.</span><span class="sxs-lookup"><span data-stu-id="8aaea-171">To change the effective date so that it's earlier than any of the existing records (periods) for the item vendor, the expiration date of the new period must be before all the expiration dates in the existing records.</span></span>
- <span data-ttu-id="8aaea-172">لتغيير تاريخ انتهاء الصلاحية بحيث يقع بعد أي من الفترات الموجودة، يجب أن يقع تاريخ السريان بعد تاريخ انتهاء الصلاحية الأخير في أي سجل موجود.</span><span class="sxs-lookup"><span data-stu-id="8aaea-172">To change the expiration date so that it's later than any of the existing periods, the effective date must be after the latest expiration date in any existing record.</span></span>
- <span data-ttu-id="8aaea-173">لتقليل الفترة الإجمالية التي تمت الموافقة على المورّد خلالها، يجب حذف السجلات الموجودة أو تعديلها.</span><span class="sxs-lookup"><span data-stu-id="8aaea-173">To reduce the overall period that the vendor is approved for, you must delete or modify existing records.</span></span> <span data-ttu-id="8aaea-174">أو، يمكنك استخدام مفتاح **الاقتطاع** خلال عملية الاستيراد.</span><span class="sxs-lookup"><span data-stu-id="8aaea-174">Alternatively, you can use the **truncate** switch during import.</span></span> <span data-ttu-id="8aaea-175">يقوم هذا المفتاح بحذف كافة السجلات الموجودة في الجدول للمورّدين المعتمدين حسب الصنف.</span><span class="sxs-lookup"><span data-stu-id="8aaea-175">This switch deletes all existing records in the table for approved vendors by item.</span></span>

<span data-ttu-id="8aaea-176">بالنسبة لسيناريو المثال الموضح في وصف المشكلة، حيث للسجل تاريخ السريان *01/11/2018* وتاريخ انتهاء الصلاحية *إطلاقًا*، يمكنك استيراد سجل جديد لديه تاريخ السريان *01/10/2018* وتاريخ انتهاء الصلاحية *إطلاقًا‏‎*.</span><span class="sxs-lookup"><span data-stu-id="8aaea-176">For the example scenario that is described in the issue description, where a record has an effective date of *01/11/2018* and an expiration date of *Never*, you can import a new record that has an effective date of *01/10/2018* and an expiration date of *Never*.</span></span> <span data-ttu-id="8aaea-177">ومع ذلك، لا يمكنك تقليل الفترة بحيث يتم تحديث تاريخ السريان إلى *01/12/2018* عبر إدارة البيانات.</span><span class="sxs-lookup"><span data-stu-id="8aaea-177">However, you can't reduce the period so that the effective date is updated to *01/12/2018* via data management.</span></span> <span data-ttu-id="8aaea-178">يجب إجراء هذا التغيير من خلال واجهة المستخدم.</span><span class="sxs-lookup"><span data-stu-id="8aaea-178">You must make this change through the UI.</span></span>

## <a name="after-i-change-the-delivery-address-on-a-purchase-order-header-the-delivery-name-isnt-synced"></a><span data-ttu-id="8aaea-179">بعد قيامي بتغيير عنوان التسليم على رأس أمر الشراء، لا تتم مزامنة اسم التسليم.</span><span class="sxs-lookup"><span data-stu-id="8aaea-179">After I change the delivery address on a purchase order header, the delivery name isn't synced.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8aaea-180">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="8aaea-180">Issue description</span></span>

<span data-ttu-id="8aaea-181">يتم تحديث العنوان الموجود على رأس أمر الشراء إلى عنوان ليس عنوان تسليم.</span><span class="sxs-lookup"><span data-stu-id="8aaea-181">The address on the header of a purchase order is updated to an address that isn't a delivery address.</span></span> <span data-ttu-id="8aaea-182">علي الرغم من تحديث العنوان على أمر الشراء، لا يتم تحديث اسم التسليم استنادًا إلى العنوان المحدّث.</span><span class="sxs-lookup"><span data-stu-id="8aaea-182">Although the address is updated on the purchase order, the delivery name isn't updated based on the updated address.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8aaea-183">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="8aaea-183">Issue resolution</span></span>

<span data-ttu-id="8aaea-184">يتم هذا السلوك بسبب التصميم.</span><span class="sxs-lookup"><span data-stu-id="8aaea-184">This behavior is by design.</span></span> <span data-ttu-id="8aaea-185">يجب تصنيف العنوان المحدد كعنوان تسليم.</span><span class="sxs-lookup"><span data-stu-id="8aaea-185">The selected address must be classified as a delivery address.</span></span> <span data-ttu-id="8aaea-186">وبخلاف ذلك، لا يتم تحديث اسم التسليم استنادًا إلى العنوان المحدد.</span><span class="sxs-lookup"><span data-stu-id="8aaea-186">Otherwise, the delivery name isn't updated based on the selected address.</span></span>

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a><span data-ttu-id="8aaea-187">هل يمكنني العثور على المستخدم الذي قام بإلغاء أمر الشراء؟</span><span class="sxs-lookup"><span data-stu-id="8aaea-187">Can I find the user who canceled a purchase order?</span></span>

<span data-ttu-id="8aaea-188">يتم تعقب هذه المعلومات فقط إذا كان أمر الشراء يخضع لإدارة التغيير.</span><span class="sxs-lookup"><span data-stu-id="8aaea-188">This information is tracked only if the purchase order is subject to change management.</span></span> <span data-ttu-id="8aaea-189">إذا كنت تستخدم إدارة التغيير، فيمكنك معرفة من هي الجهة التي أرسلت التغيير (الإلغاء) ووافقت عليه.</span><span class="sxs-lookup"><span data-stu-id="8aaea-189">If you use change management, you can see who submitted the change (the cancellation), and who approved it.</span></span>
