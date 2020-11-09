---
title: استكشاف أخطاء الأسعار والخصومات والاتفاقيات والتخفيضات‬ وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع الأسعار والخصومات والاتفاقيات والتخفيضات.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b4349eeba285492202b5df8481b277a06708a4c8
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018203"
---
# <a name="troubleshoot-prices-discounts-agreements-and-rebates"></a><span data-ttu-id="f2da6-103">استكشاف أخطاء الأسعار والخصومات والاتفاقيات والتخفيضات‬ وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="f2da6-103">Troubleshoot prices, discounts, agreements, and rebates</span></span>

<span data-ttu-id="f2da6-104">يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع الأسعار والخصومات والاتفاقيات والتخفيضات.</span><span class="sxs-lookup"><span data-stu-id="f2da6-104">This topic describes how to fix issues that you might encounter while you work with prices, discounts, agreements, and rebates.</span></span>

## <a name="i-cant-link-a-purchase-agreement-to-a-purchase-order-line-after-the-purchase-order-is-created"></a><span data-ttu-id="f2da6-105">لا يمكنني ربط اتفاقية شراء ببند أمر شراء بعد إنشاء أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="f2da6-105">I can't link a purchase agreement to a purchase order line after the purchase order is created.</span></span>

<span data-ttu-id="f2da6-106">يجب ربط اتفاقية شراء ببند أمر شراء عند إنشاء أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="f2da6-106">A purchase agreement must be associated with a purchase order when the purchase order is created.</span></span> <span data-ttu-id="f2da6-107">بخلاف ذلك، لا يمكن ربط بنود أوامر الشراء ببنود اتفاقية الشراء.</span><span class="sxs-lookup"><span data-stu-id="f2da6-107">Otherwise, purchase order lines can't be associated with purchase agreement lines.</span></span>

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a><span data-ttu-id="f2da6-108">ما عمليات التحقق التي تقوم بتشغيل الرسالة "تحديث الأسعار والخصومات التي تم إدخالها يدويًا أو المستند الخارجي"؟</span><span class="sxs-lookup"><span data-stu-id="f2da6-108">What check triggers the "Update prices and discounts entered manually or external document" message?</span></span>

<span data-ttu-id="f2da6-109">عند تغيير تاريخ الشحن، قد تتلقي رسالة تشير إلى "تحديث الأسعار والخصومات التي تم إدخالها يدويًا أو المستند الخارجي".</span><span class="sxs-lookup"><span data-stu-id="f2da6-109">When you change the shipping date, you might receive a message that states, "Update prices and discounts entered manually or external document."</span></span> <span data-ttu-id="f2da6-110">سبب تلقيك هذه الرسالة هو تشغيل اتفاقية تجارية  أو اتفاقية مبيعات مختلفة وقد تتسبب في تغيير في السعر، إذا تغيّر تاريخ الشحن.</span><span class="sxs-lookup"><span data-stu-id="f2da6-110">You receive this message because, if the shipping date is changed, a different trade or sales agreement might be triggered and cause a price change.</span></span> <span data-ttu-id="f2da6-111">من شأن تغيير تاريخ الشحن أن يؤثر أيضًا على جداول المستودع ومعلومات أخرى ذات صلة.</span><span class="sxs-lookup"><span data-stu-id="f2da6-111">A change to the shipping date can also affect warehouse schedules and other related information.</span></span>

<span data-ttu-id="f2da6-112">يتم تشغيل الرسالة عند تغيير أي من التواريخ أو بعض المعلمات الأخرى.</span><span class="sxs-lookup"><span data-stu-id="f2da6-112">The message is triggered whenever any of the dates or some other parameters are changed.</span></span> <span data-ttu-id="f2da6-113">والغرض من الرسالة هو التأكد من انك على علم بتغييرات الأسعار التي يمكنها أن تحدث بسبب هذه التغييرات.</span><span class="sxs-lookup"><span data-stu-id="f2da6-113">The purpose of the message is to make sure that you're aware of price changes that can occur because of those changes.</span></span>

<span data-ttu-id="f2da6-114">الرسالة هي المطالبة بتقييم اتفاقية التجارة (TAE).</span><span class="sxs-lookup"><span data-stu-id="f2da6-114">The message is the trade agreement evaluation (TAE) prompt.</span></span> <span data-ttu-id="f2da6-115">للحصول على وصف كامل، راجع [سياسات تقييم الاتفاقية التجارية](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).</span><span class="sxs-lookup"><span data-stu-id="f2da6-115">For a full description, see [Trade agreement evaluation policies](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).</span></span>

## <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a><span data-ttu-id="f2da6-116">لا يتضمن إيصال استلام أمر الشراء كافة المصروفات.</span><span class="sxs-lookup"><span data-stu-id="f2da6-116">A purchase order receipt doesn't include all charges.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="f2da6-117">إعادة إنتاج المشكلة</span><span class="sxs-lookup"><span data-stu-id="f2da6-117">Reproduce the issue</span></span>

<span data-ttu-id="f2da6-118">يعرض الإجراء التالي إحدى الطرق لإعادة إنتاج المشكلة.</span><span class="sxs-lookup"><span data-stu-id="f2da6-118">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="f2da6-119">في الصفحة **معلمات التدبير والتوريد** ‬‏‫، ضمن علامة التبويب **التسليم** ، تأكد من تعيين الخيار **إنشاء مصروفات على إيصال استلام المنتجات** إلى *نعم*.</span><span class="sxs-lookup"><span data-stu-id="f2da6-119">On the **Procurement and sourcing parameters** page, on the **Delivery** tab, make sure that the **Generate charges on product receipt** option is set to *Yes*.</span></span>
1. <span data-ttu-id="f2da6-120">أنشئ أمر شراء يتضمن مصروفات.</span><span class="sxs-lookup"><span data-stu-id="f2da6-120">Create a purchase order that includes charges.</span></span>
1. <span data-ttu-id="f2da6-121">أكد أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="f2da6-121">Confirm the purchase order.</span></span>
1. <span data-ttu-id="f2da6-122">استلم أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="f2da6-122">Receive the purchase order.</span></span>
1. <span data-ttu-id="f2da6-123">قم بإلقاء نظرة على إجمالي الإيصال، وقارنه بالإجمالي المتوقع.</span><span class="sxs-lookup"><span data-stu-id="f2da6-123">Look at the receipt total, and compare it to the expected total.</span></span>
1. <span data-ttu-id="f2da6-124">لاحظ عدم تضمين كافة المصروفات على إيصال أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="f2da6-124">Notice that not all the charges are included on the purchase order receipt.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f2da6-125">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="f2da6-125">Issue resolution</span></span>

<span data-ttu-id="f2da6-126">يتوقف الحل على الطريقة التي تم بها إعداد المصروفات المتنوعة.</span><span class="sxs-lookup"><span data-stu-id="f2da6-126">The resolution depends on the way that the miscellaneous charges have been set up.</span></span> <span data-ttu-id="f2da6-127">للحصول على معلومات حول كيفية إعداد المصروفات المتنوعة للوفاء بمتطلباتك، راجع منشور المدونة التالي: [ترحيل المصروفات المتنوعة عند استلام المنتجات](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span><span class="sxs-lookup"><span data-stu-id="f2da6-127">For information about how to set up miscellaneous charges to meet your requirements, see the following blog post: [Post misc. charges at time of product receipt](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span></span>

## <a name="trade-agreement-prices-and-discounts-arent-applied-on-sales-or-purchase-order-lines-that-are-imported-through-data-management"></a><span data-ttu-id="f2da6-128">لا يتم تطبيق أسعار الاتفاقية التجارية والخصومات على بنود أمر الشراء أو المبيعات المستوردة عبر إدارة البيانات.</span><span class="sxs-lookup"><span data-stu-id="f2da6-128">Trade agreement prices and discounts aren't applied on sales or purchase order lines that are imported through data management.</span></span>

### <a name="issue-description"></a><span data-ttu-id="f2da6-129">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="f2da6-129">Issue description</span></span>

<span data-ttu-id="f2da6-130">لا يتم تطبيق الاتفاقيات التجارية التي تنطبق على بنود أمر الشراء أو المبيعات على البنود المستوردة عبر إدارة البيانات.</span><span class="sxs-lookup"><span data-stu-id="f2da6-130">Trade agreements that are applicable to sales or purchase order lines aren't applied on lines that are imported through data management.</span></span> <span data-ttu-id="f2da6-131">ومع ذلك، يتم تطبيق نفس الاتفاقيات التجارية على بنود أمر الشراء أو المبيعات التي يتم إنشاؤها يدويًا.</span><span class="sxs-lookup"><span data-stu-id="f2da6-131">However, the same trade agreements are applied on sales or purchase order lines that are manually created.</span></span>

### <a name="reason-for-the-issue"></a><span data-ttu-id="f2da6-132">سبب المشكلة</span><span class="sxs-lookup"><span data-stu-id="f2da6-132">Reason for the issue</span></span>

<span data-ttu-id="f2da6-133">إذا كانت بنود أمر الشراء المستوردة من خلال إدارة البيانات تتضمن معلومات السعر، فلن يعاد تقييم الاتفاقية التجارية لهذه البنود.</span><span class="sxs-lookup"><span data-stu-id="f2da6-133">If purchase order lines that are imported via data management already include price information, the trade agreement won't be reevaluated for those lines.</span></span> <span data-ttu-id="f2da6-134">على سبيل المثال، إذا تم تعيين **النسبة المئوية لخصم البند‬** أو أي من قيم السعر والخصم لبند ما، فلن يتم البحث عن الاتفاقيات التجارية لذلك البند.</span><span class="sxs-lookup"><span data-stu-id="f2da6-134">For example, if **Line discount percentage** or any of the price and discount values is set for a line, then trade agreements will not be looked up for that line.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="f2da6-135">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="f2da6-135">Issue workaround</span></span>

<span data-ttu-id="f2da6-136">هذا السلوك متوقع، وهو مماثل لأوامر الشراء وأوامر المبيعات على حدٍ سواء.</span><span class="sxs-lookup"><span data-stu-id="f2da6-136">This behavior is expected, and is similar for both sales orders and purchase orders.</span></span>

<span data-ttu-id="f2da6-137">لحل هذه المشكلة، استورد بنود أمر الشراء بدون تعيين معلومات السعر.</span><span class="sxs-lookup"><span data-stu-id="f2da6-137">As a workaround, import the purchase order lines without setting any price information.</span></span> <span data-ttu-id="f2da6-138">سيتم بعد ذلك تطبيق الاتفاقيات التجارية، وسيتم تحديث بنود أمر الشراء استنادًا إلى الاتفاقيات التجارية المحددة.</span><span class="sxs-lookup"><span data-stu-id="f2da6-138">The trade agreements will then be applied, and the purchase order lines will be updated based on the defined trade agreements.</span></span>

## <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a><span data-ttu-id="f2da6-139">لا يتم تجميع تخفيضات المورّد استنادًا إلى الفواتير.</span><span class="sxs-lookup"><span data-stu-id="f2da6-139">A vendor rebate isn't cumulated based on invoices.</span></span>

### <a name="issue-description"></a><span data-ttu-id="f2da6-140">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="f2da6-140">Issue description</span></span>

<span data-ttu-id="f2da6-141">إذا كانت الفواتير المرحّلة ذات تواريخ استحقاق مختلفة، فلن تظهر هذه الفواتير في تخفيضات المورّد التي يتم إنشاؤها منها.</span><span class="sxs-lookup"><span data-stu-id="f2da6-141">If invoices that are posted have different due dates, those invoices aren't reflected in vendor rebates that are generated from them.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f2da6-142">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="f2da6-142">Issue resolution</span></span>

<span data-ttu-id="f2da6-143">حسب التصميم، لا تتم مراعاة تاريخ الاستحقاق عندما يتم حساب تخفيض المورّد.</span><span class="sxs-lookup"><span data-stu-id="f2da6-143">By design, the due date isn't considered when the vendor rebate is calculated.</span></span> <span data-ttu-id="f2da6-144">يمكنك تخصيص النظام بحيث يظهر تاريخ الاستحقاق والعلاقة بالفاتورة بشكل أكبر فيما يتعلق بالتخفيض الفعلي للمورّد.</span><span class="sxs-lookup"><span data-stu-id="f2da6-144">Consider customizing the system so that the due date and the relation to the invoice are more apparent with respect to the actual vendor rebate.</span></span>

## <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a><span data-ttu-id="f2da6-145">لا يتم حساب أسعار الوحدات على أوامر الشراء استنادًا إلى تحويل الوحدة.</span><span class="sxs-lookup"><span data-stu-id="f2da6-145">Unit prices on purchase orders aren't calculated based on the unit conversion.</span></span>

### <a name="issue-description"></a><span data-ttu-id="f2da6-146">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="f2da6-146">Issue description</span></span>

<span data-ttu-id="f2da6-147">عند تغيير وحدة في أمر شراء، لا يُعاد حساب أسعار الاتفاقيات التجارية وفقًا لتعريفات تحويل الوحدة.</span><span class="sxs-lookup"><span data-stu-id="f2da6-147">When a unit is changed on a purchase order, trade agreement prices aren't recalculated according to unit conversion definitions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f2da6-148">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="f2da6-148">Issue resolution</span></span>

<span data-ttu-id="f2da6-149">يتم الحصول على الأسعار دائمًا من الاتفاقيات التجارية (أو إعدادات السعر الأخرى في النظام، مثل اتفاقيات البيع أو أسعار الأصناف)، ويتم تعيينها لوحدة.</span><span class="sxs-lookup"><span data-stu-id="f2da6-149">Prices are always obtained from trade agreements (or other price settings in the system, such as sales agreements or item prices), and they are set for a unit.</span></span>

<span data-ttu-id="f2da6-150">إذا تغيّرت الوحدة على بند الأمر، فسيبحث النظام عن سعر للوحدة الجديدة ويطبق هذا السعر.</span><span class="sxs-lookup"><span data-stu-id="f2da6-150">If the unit is changed on an order line, the system looks for a price for the new unit and applies that price.</span></span> <span data-ttu-id="f2da6-151">في حالة عدم العثور على سعر للوحدة، فلن يطبّق النظام أي سعر.</span><span class="sxs-lookup"><span data-stu-id="f2da6-151">If no price is found for the unit, the system doesn't apply a price.</span></span> <span data-ttu-id="f2da6-152">لا يمكن استخدام تحويل الوحدة لإعادة حساب السعر في وحدة أخرى.</span><span class="sxs-lookup"><span data-stu-id="f2da6-152">The unit conversion can't be used to recalculate the price into another unit.</span></span> <span data-ttu-id="f2da6-153">نظريًا، قد لا يساوي السعر لصندوق واحد من عشرة صناديق عشر مرات السعر الخاص بصندوق واحد.</span><span class="sxs-lookup"><span data-stu-id="f2da6-153">Theoretically, the price for one box of ten might not equal ten times the price of one box.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="f2da6-154">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="f2da6-154">Issue workaround</span></span>

<span data-ttu-id="f2da6-155">هناك طريقة لحل هذه المشكلة وهي التأكد من وجود اتفاقيات تجارية للوحدات التي تتوقع استخدامها في بنود الأوامر الخاصة بالصنف.</span><span class="sxs-lookup"><span data-stu-id="f2da6-155">One way to work around this issue is to make sure that there are trade agreements for the units that you expect will be used on order lines for the item.</span></span>

## <a name="currency-conversion-issues-occur-with-trade-agreements"></a><span data-ttu-id="f2da6-156">تحدث مشكلات تحويل العملة في الاتفاقيات التجارية.</span><span class="sxs-lookup"><span data-stu-id="f2da6-156">Currency conversion issues occur with trade agreements.</span></span>

<span data-ttu-id="f2da6-157">لا يُعاد حساب أسعار الاتفاقية التجارية وفقًا للعملة عندما تكون العملة مختلفة على أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="f2da6-157">Trade agreement prices aren't recalculated according to the currency when the currency differs on a purchase order.</span></span>

<span data-ttu-id="f2da6-158">تتيح لك ميزة *العملة العامة* إمكانية تحديد الأسعار والخصومات بعملة واحدة فقط.</span><span class="sxs-lookup"><span data-stu-id="f2da6-158">The *Generic currency* feature lets you define prices and discounts in only one currency.</span></span> <span data-ttu-id="f2da6-159">يمكنك عندئذ التحويل إلى عملات أخرى وفق احتياجاتك.</span><span class="sxs-lookup"><span data-stu-id="f2da6-159">You can then convert to other currencies as you require.</span></span> <span data-ttu-id="f2da6-160">علاوةً على ذلك، بعد إجراء التحويل، يمكن للميزة تطبيق التقريب الذكي بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="f2da6-160">Furthermore, after the conversion is done, the feature can automatically apply smart rounding.</span></span>

## <a name="when-i-open-the-purchase-agreement-page-in-a-line-view-mode-i-cant-personalize-the-page-by-adding-the-price-unit-field-in-the-overview-of-the-line"></a><span data-ttu-id="f2da6-161">عند فتح صفحة اتفاقية الشراء في وضع طريقة عرض البند، لا يمكنني تخصيص الصفحة عبر إضافة حقل سعر الوحدة في النظرة العامة على البند.</span><span class="sxs-lookup"><span data-stu-id="f2da6-161">When I open the Purchase agreement page in a line view mode, I can't personalize the page by adding the Price unit field in the overview of the line.</span></span>

<span data-ttu-id="f2da6-162">لا يمكن تضمين بعض الحقول المشتركة في إطار عمل الاتفاقية في عمليات التخصيص.</span><span class="sxs-lookup"><span data-stu-id="f2da6-162">Some shared fields in the agreement framework can't be included in personalizations.</span></span> <span data-ttu-id="f2da6-163">ويحدث هذا التقييد بسبب نموذج البيانات الذي يتم تنفيذه.</span><span class="sxs-lookup"><span data-stu-id="f2da6-163">This limitation occurs because of the data model that is implemented.</span></span> <span data-ttu-id="f2da6-164">وبالتالي، لا يمكنك تخصيص حقل **وحدة السعر**.</span><span class="sxs-lookup"><span data-stu-id="f2da6-164">Therefore, you can't personalize the **Price unit** field.</span></span>

## <a name="the-maximum-limit-from-a-purchase-agreement-isnt-effective-on-a-purchase-requisition"></a><span data-ttu-id="f2da6-165">لا يسري الحد الأقصى من اتفاقية شراء على طلب شراء.</span><span class="sxs-lookup"><span data-stu-id="f2da6-165">The maximum limit from a purchase agreement isn't effective on a purchase requisition.</span></span>

### <a name="issue-description"></a><span data-ttu-id="f2da6-166">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="f2da6-166">Issue description</span></span>

<span data-ttu-id="f2da6-167">عند ربط طلب شراء باتفاقية شراء، لا يسري الحد الأقصى من اتفاقية الشراء على طلب الشراء.</span><span class="sxs-lookup"><span data-stu-id="f2da6-167">When a purchase requisition is linked to a purchase agreement, the maximum limit from the purchase agreement isn't effective on the purchase requisition.</span></span> <span data-ttu-id="f2da6-168">يتم إدخال معلومات الأسعار الافتراضية بشكل صحيح، ولكن يمكن طلب أكثر من الحد الأقصى من اتفاقية الشراء في طلب الشراء.</span><span class="sxs-lookup"><span data-stu-id="f2da6-168">The default price information is correctly entered, but more than the maximum limit from the purchase agreement can be ordered in the purchase requisition.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f2da6-169">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="f2da6-169">Issue resolution</span></span>

<span data-ttu-id="f2da6-170">هذا السلوك متوقع.</span><span class="sxs-lookup"><span data-stu-id="f2da6-170">This behavior is expected.</span></span> <span data-ttu-id="f2da6-171">نظرًا لعدم الموافقة دائمًا على الطلبات، يجب عدم حجز كمية أو مبلغ على اتفاقية الشراء.</span><span class="sxs-lookup"><span data-stu-id="f2da6-171">Because requisitions aren't always approved, a quantity or amount should not be reserved on the purchase agreement.</span></span> <span data-ttu-id="f2da6-172">والتالي، لن تتمكن من استيفاء الحد الأقصى من اتفاقية الشراء.</span><span class="sxs-lookup"><span data-stu-id="f2da6-172">Therefore, you won't meet the maximum limit from the purchase agreement.</span></span>

## <a name="trade-agreements-can-be-created-from-rejected-rfqs-therefore-the-system-doesnt-prevent-trade-agreement-journals-from-being-created-if-the-rfq-line-hasnt-been-accepted"></a><span data-ttu-id="f2da6-173">يمكن إنشاء الاتفاقيات التجارية من طلبات عروض الأسعار (RFQ)‬ المرفوضة.</span><span class="sxs-lookup"><span data-stu-id="f2da6-173">Trade agreements can be created from rejected RFQs.</span></span> <span data-ttu-id="f2da6-174">وبالتالي، لا يمنع النظام إنشاء دفاتر يومية الاتفاقية التجارية إذا تم قبول بند طلب عرض الأسعار (RFQ)‬.</span><span class="sxs-lookup"><span data-stu-id="f2da6-174">Therefore, the system doesn't prevent trade agreement journals from being created if the RFQ line hasn't been accepted.</span></span>

<span data-ttu-id="f2da6-175">يمكنك إنشاء اتفاقيات تجارية لأي ردود على طلب عرض الأسعار (RFQ)، بغض النظر عما إذا كانت مقبولة أم مرفوضة.</span><span class="sxs-lookup"><span data-stu-id="f2da6-175">You can create trade agreements for any replies for a request for quotation (RFQ), regardless of whether they were accepted or rejected.</span></span> <span data-ttu-id="f2da6-176">لمزيد من المعلومات، راجع [نظرة عامة على طلبات عروض الأسعار (RFQ)](request-quotations.md).</span><span class="sxs-lookup"><span data-stu-id="f2da6-176">For more information, see [Requests for quotation (RFQs) overview](request-quotations.md).</span></span>

