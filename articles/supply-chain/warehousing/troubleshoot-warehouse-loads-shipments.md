---
title: استكشاف أخطاء تحميل الإنشاء والشحنات وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء العمل مع إنشاء حمل العمل والشحنات في Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e9964376a794661058da78152879d2142dd7ec51
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828192"
---
# <a name="troubleshoot-load-building-and-shipments"></a><span data-ttu-id="e96c1-103">استكشاف أخطاء تحميل الإنشاء والشحنات وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="e96c1-103">Troubleshoot load building and shipments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e96c1-104">يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء العمل مع إنشاء حمل العمل والشحنات في Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e96c1-104">This topic describes how to fix common issues that you might encounter while you work with load building and shipments in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-load-line-for-this-order-line-because-it-contains-inventory-dimensions-that-are-invalid"></a><span data-ttu-id="e96c1-105">أتلقى رسالة الخطا التالية: "لا يمكنك إنشاء بند تحميل لسطر الأمر هذا لأنه يحتوي علي ابعاد مخزون غير صالحه..."</span><span class="sxs-lookup"><span data-stu-id="e96c1-105">I receive the following error message: "You can't create a load line for this order line because it contains inventory dimensions that are invalid..."</span></span>

### <a name="issue-description"></a><span data-ttu-id="e96c1-106">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="e96c1-106">Issue description</span></span>

<span data-ttu-id="e96c1-107">وتظهر رسالة الخطا التالية عند محاولة إصدار أمر توريد الإرجاع إلى المستودع:</span><span class="sxs-lookup"><span data-stu-id="e96c1-107">You receive the following error message when you try to release a return sales order to the warehouse:</span></span>

> <span data-ttu-id="e96c1-108">لا يمكنك إنشاء بند تحميل لسطر الأمر هذا لأنه يحتوي علي ابعاد مخزون غير صالحه.</span><span class="sxs-lookup"><span data-stu-id="e96c1-108">You can't create a load line for this order line because it contains inventory dimensions that are invalid.</span></span> <span data-ttu-id="e96c1-109">لا يمكنك الاشاره إلى ابعاد المخزون الموجودة أسفل بعد الموقع في التدرج الهرمي للحجز.</span><span class="sxs-lookup"><span data-stu-id="e96c1-109">You can't reference inventory dimensions that are located below the location dimension in the reservation hierarchy.</span></span> <span data-ttu-id="e96c1-110">تتيح أزاله الابعاد غير الصالحة من سطر الأمر.</span><span class="sxs-lookup"><span data-stu-id="e96c1-110">Remove the invalid dimensions from the order line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e96c1-111">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="e96c1-111">Issue resolution</span></span>

<span data-ttu-id="e96c1-112">لسوء الأسف ، لا يدعم المنتج معالجه التحميل لعمليه إرجاع المبيعات.</span><span class="sxs-lookup"><span data-stu-id="e96c1-112">Unfortunately, the product doesn't support load processing for a sales return process.</span></span> <span data-ttu-id="e96c1-113">التالي ، لا يمكن تحرير أمر الشراء المرتجع إلى المستودع.</span><span class="sxs-lookup"><span data-stu-id="e96c1-113">Therefore, you can't release the return sales order to the warehouse.</span></span>

<span data-ttu-id="e96c1-114">في حركات أمر المبيعات، يمكنك الاشاره إلى ابعاد المخزون الموجودة أسفل بعد **الموقع** في التدرج الهرمي للحجز.</span><span class="sxs-lookup"><span data-stu-id="e96c1-114">On sales order transactions, you can't reference inventory dimensions that are located below the **Location** dimension in the reservation hierarchy.</span></span> <span data-ttu-id="e96c1-115">الحل هو أزاله الابعاد غير الصالحة من سطر الأمر.</span><span class="sxs-lookup"><span data-stu-id="e96c1-115">The resolution is to remove the invalid dimensions from the order line.</span></span>

## <a name="i-receive-the-following-error-message-one-of-the-lines-is-already-on-a-load-unable-to-release-to-warehouse"></a><span data-ttu-id="e96c1-116">أتلقى رسالة الخطا التالية: "أحد البنود قيد التحميل بالفعل.</span><span class="sxs-lookup"><span data-stu-id="e96c1-116">I receive the following error message: "One of the lines is already on a load.</span></span> <span data-ttu-id="e96c1-117">تعذر الإصدار إلى المستودع."</span><span class="sxs-lookup"><span data-stu-id="e96c1-117">Unable to release to warehouse."</span></span>

### <a name="issue-description"></a><span data-ttu-id="e96c1-118">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="e96c1-118">Issue description</span></span>

<span data-ttu-id="e96c1-119">إذا قمت بإنشاء التحميل يدويا ، أو إذا قمت باعداد العملية بحيث يتم إنشاء التحميلات بالفعل قبل حدوث إدخال سطر أمر المبيعات ، فان الافتراض هو ان يتم اجراء الإصدار اللاحق يدويا ، سيتم استخدام المسار والتقدير من الحمل.</span><span class="sxs-lookup"><span data-stu-id="e96c1-119">If you manually create loads, or if you set up the process so that loads are already created before sales order line entry occurs, the assumption is that the subsequent release will be done manually, and that the route and rating from the load will be used.</span></span>

<span data-ttu-id="e96c1-120">في السيناريو المحتمل الآخر ، تحاول القيام بإصدار تلقائي للمستودع ، ولكن فشل عمليه الموجه في إنشاء العمل.</span><span class="sxs-lookup"><span data-stu-id="e96c1-120">In another possible scenario, you're trying to do an automatic release to the warehouse, but the wave process failed to create work.</span></span> <span data-ttu-id="e96c1-121">لذلك ، لا يزال يتم إنشاء شحنه مفتوحة أو عمليه تحميل.</span><span class="sxs-lookup"><span data-stu-id="e96c1-121">Therefore, an open shipment or load is still created.</span></span> <span data-ttu-id="e96c1-122">يقوم الشحن أو التحميل المفتوح بعد ذلك بحظر المحاولات اللاحقة لإصدار الأمر تلقائيا حتى تقوم بحذف الشحنة أو التحميل المفتوح ، أو إعادة معالجة الموجه يدويا.</span><span class="sxs-lookup"><span data-stu-id="e96c1-122">This open shipment or load then blocks subsequent attempts to automatically release the order until you either delete the open shipment or load, or manually reprocess the wave.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e96c1-123">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="e96c1-123">Issue resolution</span></span>

<span data-ttu-id="e96c1-124">يمكنك الإصدار من الصفحة أمر المبيعات ، أو يمكن اجراء الإصدار التلقائي من الصفحة أمر المبيعات الخاص بالإصدار ، وذلك فقط في حاله عدم وجود تحميل قبل الإصدار الخاص بالمستودع.</span><span class="sxs-lookup"><span data-stu-id="e96c1-124">You can release from the sales order page, or automatic release can be done from the release sales order page, only if no load exists before the release to the warehouse.</span></span> <span data-ttu-id="e96c1-125">سيتم تلقائيا إنشاء التحميل بعد معالجه الموجه.</span><span class="sxs-lookup"><span data-stu-id="e96c1-125">The load will automatically be created after the wave is processed.</span></span>

## <a name="i-receive-the-following-error-message-the-delivery-note-correction-cant-be-processed-the-delivery-note-only-contains-items-that-are-subject-to-warehouse-management-processes-as-these-are-not-supported-by-delivery-note-correction"></a><span data-ttu-id="e96c1-126">أتلقى رسالة الخطا التالية: "لا يمكن معالجه تصحيح مذكره التسليم.</span><span class="sxs-lookup"><span data-stu-id="e96c1-126">I receive the following error message: "The delivery note correction can't be processed.</span></span> <span data-ttu-id="e96c1-127">لا تحتوي اشعار التسليم الا علي الأصناف التي تخضع لعمليات أداره المستودع ، لان هذه الأصناف غير معتمده من قبل تصحيح مذكره التسليم."</span><span class="sxs-lookup"><span data-stu-id="e96c1-127">The delivery note only contains items that are subject to warehouse management processes, as these are not supported by Delivery Note correction."</span></span>

### <a name="issue-description"></a><span data-ttu-id="e96c1-128">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="e96c1-128">Issue description</span></span>

<span data-ttu-id="e96c1-129">بعد ترحيل مذكره تسليم ، لا يمكنك إلغاؤها ، لأنه لم يتم توفير الزر **إلغاء**.</span><span class="sxs-lookup"><span data-stu-id="e96c1-129">After you post a delivery note, you can't cancel it, because the **Cancel** button is unavailable.</span></span> <span data-ttu-id="e96c1-130">لا يمكنك أيضا تصحيح مذكرة التسليم.</span><span class="sxs-lookup"><span data-stu-id="e96c1-130">You also can't correct the delivery note.</span></span> <span data-ttu-id="e96c1-131">في حاله المحاولة ، تظهر رسالة الخطا هذه.</span><span class="sxs-lookup"><span data-stu-id="e96c1-131">If you try, you receive this error message.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e96c1-132">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="e96c1-132">Issue resolution</span></span>

<span data-ttu-id="e96c1-133">لتصحيح إيصالات التعبئة التي تم ترحيلها للأصناف التي تم تمكينها لأداره المستودعات المتقدمة (WMS) ، يجب القيام بالترحيل من التحميل ، وليس من الأمر مباشره.</span><span class="sxs-lookup"><span data-stu-id="e96c1-133">To correct posted packing slips for items that are enabled for advanced warehouse management (WMS), you must do the posting from the load, not directly from the order.</span></span>

## <a name="how-can-i-create-work-from-outbound-loads-instead-of-waves"></a><span data-ttu-id="e96c1-134">كيف يمكنني إنشاء عمل من التحميلات الصادرة بدلا من الموجات؟</span><span class="sxs-lookup"><span data-stu-id="e96c1-134">How can I create work from outbound loads instead of waves?</span></span>

### <a name="issue-description"></a><span data-ttu-id="e96c1-135">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="e96c1-135">Issue description</span></span>

<span data-ttu-id="e96c1-136">وفيما يلي أحدي الطرق لأعاده إنتاج هذه المشكلة.</span><span class="sxs-lookup"><span data-stu-id="e96c1-136">Here is one way to reproduce this issue.</span></span>

1. <span data-ttu-id="e96c1-137">قم بإنشاء حمل عمل خارجي باستخدام أمر مبيعات أو أمر نقل.</span><span class="sxs-lookup"><span data-stu-id="e96c1-137">Create an outbound load by using a sales order or transfer order.</span></span>
2. <span data-ttu-id="e96c1-138">قم بإصدار حمل العمل للمستودع.</span><span class="sxs-lookup"><span data-stu-id="e96c1-138">Release the load to the warehouse.</span></span>
3. <span data-ttu-id="e96c1-139">لاحظ انه لم يتم إنشاء عمل انتقاء بعد.</span><span class="sxs-lookup"><span data-stu-id="e96c1-139">Notice that no picking work has yet been generated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e96c1-140">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="e96c1-140">Issue resolution</span></span>

<span data-ttu-id="e96c1-141">إذا كان يجب إنشاء العمل فورا عند إصدار الحمل ، يجب ان تقوم بتكوين قالب الموجه وفقا لذلك.</span><span class="sxs-lookup"><span data-stu-id="e96c1-141">If work must be generated immediately when the load is released, you must configure the wave template accordingly.</span></span> <span data-ttu-id="e96c1-142">في قالب الموجه ، قم بتعيين الخيارات التالية إلى *نعم*:</span><span class="sxs-lookup"><span data-stu-id="e96c1-142">On the wave template, set the following options to *Yes*:</span></span>

- <span data-ttu-id="e96c1-143">جعل إنشاء الموجة تلقائيًا</span><span class="sxs-lookup"><span data-stu-id="e96c1-143">Automate wave creation</span></span>
- <span data-ttu-id="e96c1-144">معالجة الموجة عند الإصدار إلى المستودع</span><span class="sxs-lookup"><span data-stu-id="e96c1-144">Process wave at release to warehouse</span></span>
- <span data-ttu-id="e96c1-145">جعل تحرير الموجة تلقائيًا</span><span class="sxs-lookup"><span data-stu-id="e96c1-145">Automate wave release</span></span>

## <a name="i-cant-re-release-a-partially-shipped-load"></a><span data-ttu-id="e96c1-146">لا يمكنني أعاده إصدار تحميل تم شحنه جزئيا.</span><span class="sxs-lookup"><span data-stu-id="e96c1-146">I can't re-release a partially shipped load.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e96c1-147">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="e96c1-147">Issue description</span></span>

<span data-ttu-id="e96c1-148">لا يمكنك إصدار تحميل تم شحنه جزئيا للمستودع.</span><span class="sxs-lookup"><span data-stu-id="e96c1-148">You can't release a partially shipped load to the warehouse.</span></span> <span data-ttu-id="e96c1-149">عند القيام بالإصدار علي المستودع ، تظهر رسالة "اكتملت العملية" ولكن لا يحدث شيء ، ولا يتم إنشاء اي عمل للكمية المتبقية.</span><span class="sxs-lookup"><span data-stu-id="e96c1-149">When you do the release to the warehouse, an "Operation complete" message appears, but nothing happens, and no work is created for the remaining quantity.</span></span> <span data-ttu-id="e96c1-150">تحدث هذه المشكلة عند استخدام وظيفة تحميل النقل ووجود حجز غير مكتمل.</span><span class="sxs-lookup"><span data-stu-id="e96c1-150">This issue occurs when you use transport load functionality and there is an incomplete reservation.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e96c1-151">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="e96c1-151">Issue resolution</span></span>

<span data-ttu-id="e96c1-152">[مشكلة قاعدة المعارف 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("يمكن أعاده إنشاء موجات لعمليات التحميل التي تم شحنها جزئيا وأعاده معالجتها") تم إصلاحها في [الإصدار 10.0.15](../get-started/whats-new-scm-10-0-15.md).</span><span class="sxs-lookup"><span data-stu-id="e96c1-152">[KB issue 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("Partially shipped loads can be re-waved and re-processed") is fixed in [release 10.0.15](../get-started/whats-new-scm-10-0-15.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]