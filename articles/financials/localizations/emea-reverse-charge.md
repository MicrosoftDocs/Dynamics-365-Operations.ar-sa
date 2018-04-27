---
title: "ضريبة القيمة المضافة للرسوم العكسية"
description: "يشرح هذا الموضوع كيفية إعداد ضريبة القيمة المضافة (VAT) للرسوم العكسية للمملكة العربية السعودية والدول الأوروبية."
author: epodkolz
manager: AnnBe
ms.date: 04/05/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Saudi Arabia, Spain, Sweden, United Kingdom
ms.author: epodkolz
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 64518e72dd66961108ff905981cd0405355ed130
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---

# <a name="reverse-charge-vat"></a><span data-ttu-id="3defd-103">ضريبة القيمة المضافة للرسوم العكسية</span><span class="sxs-lookup"><span data-stu-id="3defd-103">Reverse charge VAT</span></span>


[!INCLUDE [banner](../includes/banner.md)]


<span data-ttu-id="3defd-104">يشرح هذا الموضوع نهجًا عامًا لإعداد ضريبة القيمة المضافة (VAT) للرسوم العكسية للمملكة العربية السعودية والدول الأوروبية.</span><span class="sxs-lookup"><span data-stu-id="3defd-104">This topic describes a generic approach for setting up reverse charge value-added tax (VAT) for Saudi Arabia and European countries.</span></span>

<span data-ttu-id="3defd-105">الرسوم العكسية عبارة عن مخطط ضريبة ينقل المسؤولية عن المحاسبة وإعداد تقارير ضريبة القيمة المضافة من البائع إلى مشتري السلع و/أو الخدمات.</span><span class="sxs-lookup"><span data-stu-id="3defd-105">Reverse Charge is a tax schema that moves the responsibility for the accounting and reporting of VAT from the seller to the buyer of goods and/or services.</span></span> <span data-ttu-id="3defd-106">ولذلك، يُبلغ مستلمو السلع و/أو الخدمات عن كلٍّ من ضريبة القيمة المضافة للإخراج (بدور البائع) وضريبة القيمة المضافة للإدخال (بدور المشتري) في بيان ضريبة القيمة المضافة.</span><span class="sxs-lookup"><span data-stu-id="3defd-106">Therefore, recipients of goods and/or services report both the output VAT (in the role of a seller) and the input VAT (in the role of a purchaser) on their VAT statement.</span></span>

<span data-ttu-id="3defd-107">في بعض البلدان أو المناطق، يتم تطبيق مخطط "الرسوم العكسية" فقط لبعض السلع و/أو الخدمات، وهناك شروط أو حدود إضافية على كميات المبيعات.</span><span class="sxs-lookup"><span data-stu-id="3defd-107">In some countries or regions, the Reverse Charge schema is implemented only for some goods and/or services, and there are additional conditions or thresholds on sales amounts.</span></span> <span data-ttu-id="3defd-108">في الدول أو المناطق الأخرى، تعتمد المسؤولية عن دفع ضريبة القيمة المضافة على حالة المورد والمشتري.</span><span class="sxs-lookup"><span data-stu-id="3defd-108">In other countries or regions, the responsibility for VAT payment depends on the status of the supplier and the buyer.</span></span> <span data-ttu-id="3defd-109">إذا كان المشتري ملتزمًا بدفع ضريبة القيمة المضافة، فيجب الإشارة إلى هذه الحقيقة بوضوح في الفاتورة التي يُصدرها المورد.</span><span class="sxs-lookup"><span data-stu-id="3defd-109">If the buyer is liable to pay VAT, this fact must be clearly indicated on the invoice that the supplier issues.</span></span> <span data-ttu-id="3defd-110">على سبيل المثال، يجب أن تتضمن الفاتورة كلمات "الرسوم العكسية" ويجب أن تشير إلى المواضع التي تقع ضمن مخطط "الرسوم العكسية".</span><span class="sxs-lookup"><span data-stu-id="3defd-110">For example, the invoice must include the words "Reverse charge" and must indicate which positions are under the Reverse Charge schema.</span></span> 

<span data-ttu-id="3defd-111">لتطبيق الرسوم العكسية، يجب عليك إكمال الإعداد التالي.</span><span class="sxs-lookup"><span data-stu-id="3defd-111">To apply the reverse charge, you must complete the following setup.</span></span>

## <a name="set-up-sales-tax-codes"></a><span data-ttu-id="3defd-112">إعداد أكواد ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="3defd-112">Set up sales tax codes</span></span>
<span data-ttu-id="3defd-113">نوصيك باستخدام أكواد ضريبة مبيعات منفصلة لعمليات المبيعات وعمليات الشراء.</span><span class="sxs-lookup"><span data-stu-id="3defd-113">We recommend that you use separate sales tax codes for sales operations and purchase operations.</span></span>

<table>
<body>
<tr>
<td><span data-ttu-id="3defd-114"><strong>كود ضريبة المبيعات للمبيعات</strong></span><span class="sxs-lookup"><span data-stu-id="3defd-114"><strong>Sales tax code for sales</strong></span></span></td>
<td><span data-ttu-id="3defd-115">أنشئ كود ضريبة مبيعات لعمليات مبيعات الرسوم العكسية (<strong>الضريبة</strong>&gt;<strong>الضرائب غير المباشرة</strong>&gt;<strong>ضريبة مبيعات</strong>&gt;<strong>أكواد ضريبة المبيعات</strong>).</span><span class="sxs-lookup"><span data-stu-id="3defd-115">Create a sales tax code for reverse charge sales operations (<strong>Tax</strong> &gt; <strong>Indirect taxes</strong> &gt; <strong>Sales tax</strong> &gt; <strong>Sales tax codes</strong>).</span></span>
</td>
</tr>
<tr>
<td><span data-ttu-id="3defd-116"><strong>كود ضريبة المبيعات للمشتريات</strong></span><span class="sxs-lookup"><span data-stu-id="3defd-116"><strong>Sales tax code for purchases</strong></span></span></td>
<td><p><span data-ttu-id="3defd-117">أنشئ أكواد ضريبة مبيعات موجبة وسالبة لضريبة القيمة المضافة للرسوم العكسية للمشتريات (<strong>الضريبة</strong>&gt;<strong>الضرائب غير المباشرة</strong>&gt;<strong>ضريبة المبيعات</strong>&gt;<strong>أكواد ضريبة المبيعات</strong>).</span><span class="sxs-lookup"><span data-stu-id="3defd-117">Create positive and negative sales tax codes for the reverse charge VAT for purchases (<strong>Tax</strong> &gt; <strong>Indirect taxes</strong> &gt; <strong>Sales tax</strong> &gt; <strong>Sales tax codes</strong>).</span></span></p>
<ol>
<li><span data-ttu-id="3defd-118">أنشئ كود ضريبة مبيعات يحتوي على قيمة موجبة.</span><span class="sxs-lookup"><span data-stu-id="3defd-118">Create a sales tax code that has a positive value.</span></span></li>
<li><span data-ttu-id="3defd-119">أنشئ كود ضريبة مبيعات يحتوي على قيمة سالبة.</span><span class="sxs-lookup"><span data-stu-id="3defd-119">Create a sales tax code that has a negative value.</span></span> <span data-ttu-id="3defd-120">قم بتعيين خيار <strong>السماح بنسبة مئوية سالبة لضريبة المبيعات</strong> إلى <strong>نعم</strong>.</span><span class="sxs-lookup"><span data-stu-id="3defd-120">Set the <strong>Allow negative sales tax percentage</strong> option to <strong>Yes</strong>.</span></span>
<span data-ttu-id="3defd-121">يجب عليك تعيين كود ضريبة المبيعات الإيجابي لمجموعة ضريبة المبيعات للصنف، وبعد ذلك تعيين مجموعة ضريبة المبيعات للصنف هذه للأصناف التي تخضع لضريبة القيمة المضافة للتكاليف العكسية.</span><span class="sxs-lookup"><span data-stu-id="3defd-121">You must assign this negative sales tax code to an item sales tax group and then assign that item sales tax group to the items that are subject to the reverse charge VAT.</span></span></li>
</ol>
<p><span data-ttu-id="3defd-122">لمزيد من المعلومات، راجع القسم التالي، &quot;إعداد مجموعات ضريبة المبيعات ومجموعات ضريبة مبيعات الصنف.&quot;</span><span class="sxs-lookup"><span data-stu-id="3defd-122">For more information, see the next section, &quot;Set up sales tax groups and item sales tax groups.&quot;</span></span></p>
</td>
</tr>
</tbody>
</table>

## <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><span data-ttu-id="3defd-123">إعداد مجموعات ضريبة المبيعات ومجموعات ضريبة مبيعات الصنف</span><span class="sxs-lookup"><span data-stu-id="3defd-123">Set up sales tax groups and item sales tax groups</span></span>
<span data-ttu-id="3defd-124">نوصيك باستخدام مجموعات ضريبة مبيعات منفصلة لعمليات المبيعات وعمليات الشراء.</span><span class="sxs-lookup"><span data-stu-id="3defd-124">We recommend that you use separate sales tax groups for sales operations and purchase operations.</span></span>

<table>
<tr>
<td><span data-ttu-id="3defd-125"><strong>مجموعة ضريبة مبيعات للمبيعات</strong></span><span class="sxs-lookup"><span data-stu-id="3defd-125"><strong>Sales tax groups for sales</strong></span></span></td>
<td><span data-ttu-id="3defd-126">أنشئ مجموعة ضريبة مبيعات لعمليات المبيعات التي تشتمل على 
رسوم عكسية (<strong>الضريبة</strong>&gt;<strong>الضرائب غير المباشرة</strong>&gt;<strong>ضريبة مبيعات</strong>&gt;<strong>مجموعات ضريبة المبيعات</strong>).</span><span class="sxs-lookup"><span data-stu-id="3defd-126">Create a sales tax group for sales operations that have the reverse charge (<strong>Tax</strong> &gt; <strong>Indirect taxes</strong> &gt; <strong>Sales tax</strong> &gt; <strong>Sales tax groups</strong>).</span></span> <span data-ttu-id="3defd-127">في علامة التبويب <strong>الإعداد</strong>، قم بتضمين كود ضريبة المبيعات للرسوم العكسية في هذه المجموعة.</span><span class="sxs-lookup"><span data-stu-id="3defd-127">On the <strong>Setup</strong> tab, include the sales tax code for the reverse charge in this group.</span></span> <span data-ttu-id="3defd-128">حدد خانتي الاختيار <strong>الإعفاء</strong> و<strong>الرسوم العكسية</strong> لكود ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="3defd-128">Select the <strong>Exempt</strong> and <strong>Reverse charge</strong> check boxes for the sales tax code.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3defd-129"><strong>مجموعة ضريبة المبيعات للمشتريات</strong></span><span class="sxs-lookup"><span data-stu-id="3defd-129"><strong>Sales tax groups for purchases</strong></span></span></td>
<td><span data-ttu-id="3defd-130">أنشئ مجموعة ضريبة مبيعات لعمليات الشراء التي تشتمل على 
رسوم عكسية (<strong>الضريبة</strong>&gt;<strong>الضرائب غير المباشرة</strong>&gt;<strong>ضريبة مبيعات</strong>&gt;<strong>مجموعات ضريبة المبيعات</strong>).</span><span class="sxs-lookup"><span data-stu-id="3defd-130">Create a sales tax group for purchase operations that have the reverse charge (<strong>Tax</strong> &gt; <strong>Indirect taxes</strong> &gt; <strong>Sales tax</strong> &gt; <strong>Sales tax groups</strong>).</span></span> <span data-ttu-id="3defd-131">في علامة التبويب <strong>الإعداد</strong> ، قم بتضمين كلٍّ من أكواد ضريبة المبيعات الموجبة والسالبة في هذه المجموعة.</span><span class="sxs-lookup"><span data-stu-id="3defd-131">On the <strong>Setup</strong> tab, include both positive and negative sales tax codes in this group.</span></span> <span data-ttu-id="3defd-132">حدد خانة الاختيار <strong>الرسوم العكسية</strong> لكود ضريبة المبيعات الذي يحتوي على قيمة سالبة.</span><span class="sxs-lookup"><span data-stu-id="3defd-132">Select the <strong>Reverse charge</strong> check box for the sales tax code that has a negative value.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3defd-133"><strong>مجموعات ضريبة مبيعات الصنف</strong></span><span class="sxs-lookup"><span data-stu-id="3defd-133"><strong>Item sales tax groups</strong></span></span></td>
<td><span data-ttu-id="3defd-134">قم بإنشاء أو تحديث مجموعات ضريبة مبيعات الأصناف باستخدام كود ضريبة المبيعات الذي يحتوي على قيمة سالبة (<strong>الضريبة</strong>&gt;<strong>الضرائب غير المباشرة</strong>&gt;<strong>ضريبة مبيعات</strong>&gt;<strong>مجموعات ضريبة مبيعات الصنف</strong>).</span><span class="sxs-lookup"><span data-stu-id="3defd-134">Create or update the item sales tax group with the sales tax code that has a negative value (<strong>Tax</strong> &gt; <strong>Indirect taxes</strong> &gt; <strong>Sales tax</strong> &gt; <strong>Item sales tax groups</strong>).</span></span> <span data-ttu-id="3defd-135">يجب عليك تعيين مجموعة ضريبة مبيعات الصنف الافتراضية للمنتجات والفئات الخاضعة للرسوم العكسية.</span><span class="sxs-lookup"><span data-stu-id="3defd-135">You must assign the default item sales tax group to the products and categories that are subject to the reverse charge.</span></span></td>
</tr>
</table>

## <a name="set-up-reverse-charge-groups"></a><span data-ttu-id="3defd-136">إعداد مجموعات الرسوم العكسية</span><span class="sxs-lookup"><span data-stu-id="3defd-136">Set up reverse charge groups</span></span>
<span data-ttu-id="3defd-137">في صفحة **مجموعات أصناف الرسوم العكسية** (**ا7لضريبة**&gt;**الإعداد**&gt;**ضريبة المبيعات**&gt;**مجموعات أصناف الرسوم العكسية**)، يمكنك تحديد مجموعات المنتجات أو الخدمات أو المنتجات أو الخدمات الفردية التي يمكن تطبيق الرسوم العكسية لها.</span><span class="sxs-lookup"><span data-stu-id="3defd-137">On the **Reverse charge item groups** page (**Tax** &gt; **Setup** &gt; **Sales tax** &gt; **Reverse charge item groups**), you can define groups of products or services, or individual products or services, that the reverse charge can be applied to.</span></span> <span data-ttu-id="3defd-138">بالنسبة لكل مجموعة أصناف رسوم عكسية، حدد قائمة بالأصناف، ومجموعات الأصناف، وفئات للمبيعات و/أو المشتريات.</span><span class="sxs-lookup"><span data-stu-id="3defd-138">For each reverse charge item group, define the list of items, item groups, and categories for sales and/or purchases.</span></span>

## <a name="set-up-reverse-charge-rules"></a><span data-ttu-id="3defd-139">إعداد قواعد الرسوم العكسية</span><span class="sxs-lookup"><span data-stu-id="3defd-139">Set up reverse charge rules</span></span>
<span data-ttu-id="3defd-140">في صفحة **قواعد الرسوم العكسية** (**الضريبة**&gt;**الإعداد**&gt;**ضريبة المبيعات**&gt;**قواعد الرسوم العكسية**)، يمكنك تحديد قواعد إمكانية التطبيق لأهداف المبيعات والمشتريات.</span><span class="sxs-lookup"><span data-stu-id="3defd-140">On the **Reverse charge rules** page (**Tax** &gt; **Setup** &gt; **Sales tax** &gt; **Reverse charge rules**), you can define the applicability rules for purchase and sales purposes.</span></span> <span data-ttu-id="3defd-141">يمكنك تكوين مجموعة من قواعد إمكانية تطبيق الرسوم العكسية.</span><span class="sxs-lookup"><span data-stu-id="3defd-141">You can configure a set of reverse charge applicability rules.</span></span> <span data-ttu-id="3defd-142">بالنسبة لكل قاعدة، قم بتعيين الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="3defd-142">For each rule, set the following fields:</span></span>

- <span data-ttu-id="3defd-143">**نوع المستند** - حدد **أمر الشراء**، و/أو **دفتر يومية فواتير المورد**، و/أو **أمر المبيعات**، و/أو **فاتورة النص الحر**، و/أو **دفتر يومية فواتير العميل**، و/أو **فاتورة المورد**.</span><span class="sxs-lookup"><span data-stu-id="3defd-143">**Document type** – Select **Purchase order**, **Vendor invoice journal**, **Sales order**, **Free text invoice**, **Customer invoice journal**, and/or **Vendor invoice**.</span></span>
- <span data-ttu-id="3defd-144">**نوع البلد/المنطقة للشريك** -حدد **محلي**، أو **الاتحاد الأوروبي**، أو **خارجي**.</span><span class="sxs-lookup"><span data-stu-id="3defd-144">**Country/region type of the partner** – Select **Domestic**, **EU**, or **Foreign**.</span></span> <span data-ttu-id="3defd-145">بدلاً من ذلك، حدد ما إذا كان يمكن تطبيق القاعدة على كافة الشركاء، بغض النظر عن بلد أو منطقة عنوانهم، وحدد **الكل**.</span><span class="sxs-lookup"><span data-stu-id="3defd-145">Alternatively, if the rule can be applied to all trade partners, regardless of the country or region of their address, select **All**.</span></span>
- <span data-ttu-id="3defd-146">**عنوان التسليم المحلي** - حدد خانة الاختيار هذه لتطبيق القاعدة على عمليات التسليم في نفس البلد أو المنطقة.</span><span class="sxs-lookup"><span data-stu-id="3defd-146">**Domestic delivery address** – Select this check box to apply the rule to deliveries within the same country or region.</span></span> <span data-ttu-id="3defd-147">لا يمكن تحديد خانة الاختيار هذه لنوع المستندات **دفتر يومية فواتير المورد** و**دفتر يومية فواتير العميل**.</span><span class="sxs-lookup"><span data-stu-id="3defd-147">This check box can't be selected for the **Vendor invoice journal** and **Customer invoice journal** document types.</span></span>
- <span data-ttu-id="3defd-148">**مجموعة أصناف الرسوم العكسية** - حدد المجموعة التي يمكن تطبيق القاعدة لها.</span><span class="sxs-lookup"><span data-stu-id="3defd-148">**Reverse charge item group** – Select the group that the rule can be applied to.</span></span>
- <span data-ttu-id="3defd-149">**مبلغ الحد** - يتم تطبيق مخطط "الرسوم العكسية" على فاتورة فقط إذا تجاوزت قيمة الأصناف و/أو الخدمات التي تم تضمينها في مجموعة أصناف الرسوم العكسية الحد الذي تقوم بتحديده هنا.</span><span class="sxs-lookup"><span data-stu-id="3defd-149">**Threshold amount** – The Reverse Charge schema is applied to an invoice only if the value of items and/or services that are included in the reverse charge item group exceeds the limit that you specify here.</span></span>

<span data-ttu-id="3defd-150">يمكنك أيضًا استخدام حقلي **تاريخ سريان** و**تاريخ انتهاء الصلاحية** لتحديد الفترة التي يكون القاعدة خلالها فعالة.</span><span class="sxs-lookup"><span data-stu-id="3defd-150">You can also use the **Effective date** and **Expiration date** fields to define the period when the rule is effective.</span></span>

<span data-ttu-id="3defd-151">بالإضافة إلى ذلك، يمكنك تحديد ما إذا كان يظهر إعلام ويتم تحديث بند المستند بمجموعة ضريبة مبيعات الرسوم العكسية الافتراضية في حالة تحقق شرط بند المستند هذا.</span><span class="sxs-lookup"><span data-stu-id="3defd-151">Additionally, you can specify whether a notification appears and the document line is updated with the default reverse charge sales tax group if the condition for that document line is met.</span></span> <span data-ttu-id="3defd-152">يتوفر الخياران التاليان:</span><span class="sxs-lookup"><span data-stu-id="3defd-152">The following options are available:</span></span>

- <span data-ttu-id="3defd-153">**بلا** - لا يتم تحديث بند المستند.</span><span class="sxs-lookup"><span data-stu-id="3defd-153">**None** – The document line isn't updated.</span></span>
- <span data-ttu-id="3defd-154">**موجه** - يظهر إعلام للتأكيد على أنه يمكن تطبيق الرسوم العكسية.</span><span class="sxs-lookup"><span data-stu-id="3defd-154">**Prompt** – A notification appears to confirm that the reverse charge can be applied.</span></span>
- <span data-ttu-id="3defd-155">**تعيين ** - يتم تحديث بند المستند دون إعلام إضافي.</span><span class="sxs-lookup"><span data-stu-id="3defd-155">**Set** – The document line is updated without additional notification.</span></span>

## <a name="set-up-default-parameters"></a><span data-ttu-id="3defd-156">إعداد المعلمات الافتراضية</span><span class="sxs-lookup"><span data-stu-id="3defd-156">Set up default parameters</span></span>
<span data-ttu-id="3defd-157">لتمكين وظيفة ضريبة القيمة المضافة للرسوم العكسية، في صفحة **محددات دفتر الأستاذ العام**، في علامة التبويب **الرسوم العكسية** ، قم بتعيين خيار **تمكين الرسوم العكسية** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="3defd-157">To enable the functionality for reverse charge VAT, on the **General ledger parameters** page, on the **Reverse charge** tab, set the **Enable reverse charge** option to **Yes**.</span></span> <span data-ttu-id="3defd-158">في حقلي **مجموعة ضريبة مبيعات أوامر الشراء** و**مجموعة ضريبة مبيعات أوامر المبيعات**، حدد مجموعات ضريبة المبيعات الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="3defd-158">In the **Purchase order sales tax group** and **Sales order tax group** fields, select the default sales tax groups.</span></span> <span data-ttu-id="3defd-159">عند الوفاء بشرط إمكانية تطبيق رسوم عكسية، يتم تحديث بند أمر الشراء أو المبيعات بمجموعات ضريبة المبيعات هذه.</span><span class="sxs-lookup"><span data-stu-id="3defd-159">When a reverse charge applicability condition is met, the sales or purchase order line is updated with these sales tax groups.</span></span>

## <a name="reverse-charge-on-a-sales-invoice"></a><span data-ttu-id="3defd-160">الرسوم العكسية في فاتورة مبيعات</span><span class="sxs-lookup"><span data-stu-id="3defd-160">Reverse charge on a sales invoice</span></span>
<span data-ttu-id="3defd-161">بالنسبة للمبيعات ضمن مخطط "الرسوم العكسية"، لا يقوم البائع بتحصيل ضريبة القيمة المضافة.</span><span class="sxs-lookup"><span data-stu-id="3defd-161">For sales under the Reverse Charge schema, the seller doesn't charge VAT.</span></span> <span data-ttu-id="3defd-162">وبدلاً من ذلك، تشير الفاتورة إلى كلا الصنفين الخاضعين لضريبة القيمة المضافة للرسوم العكسية والمبلغ الإجمالي لضريبة القيمة المضافة للرسوم العكسية.</span><span class="sxs-lookup"><span data-stu-id="3defd-162">Instead, the invoice indicates both the items that are subject to the reverse charge VAT and the total amount of the reverse charge VAT.</span></span>

<span data-ttu-id="3defd-163">عند ترحيل فاتورة مبيعات تتشمل على الرسوم العكسية، تشتمل حركات ضريبة المبيعات على اتجاه ضريبة **ضريبة المبيعات مستحقة الدفع** وضريبة المبيعات الصفرية، ويتم تحديد خانة الاختيار **الرسوم العكسية**.</span><span class="sxs-lookup"><span data-stu-id="3defd-163">When a sales invoice that has the reverse charge is posted, the sales tax transactions have the **Sales tax payable** tax direction and zero sales tax, and the **Reverse charge** check box is selected.</span></span>

## <a name="reverse-charge-on-a-purchase-invoice"></a><span data-ttu-id="3defd-164">الرسوم العكسية في فاتورة شراء</span><span class="sxs-lookup"><span data-stu-id="3defd-164">Reverse charge on a purchase invoice</span></span>
<span data-ttu-id="3defd-165">بالنسبة للمشتريات ضمن مخطط "الرسوم العكسية"، يقوم المشتري الذي يتلقى الفاتورة التي تشتمل على الرسوم العكسية بدور مشتري وبائع لأغراض محاسبة ضريبة القيمة المضافة.</span><span class="sxs-lookup"><span data-stu-id="3defd-165">For purchases under the Reverse Charge schema, the purchaser who receives the invoice that has the reverse charge acts as a buyer and a seller for VAT accounting purposes.</span></span>

<span data-ttu-id="3defd-166">عند ترحيل فاتورة شراء تشتمل على الرسوم العكسية، يتم إنشاء حركتي ضريبة مبيعات.</span><span class="sxs-lookup"><span data-stu-id="3defd-166">When a purchase invoice that has the reverse charge is posted, two sales tax transactions are created.</span></span> <span data-ttu-id="3defd-167">تشتمل حركة واحدة على اتجاه ضريبة **ضريبة المبيعات مستحقة القبض**.</span><span class="sxs-lookup"><span data-stu-id="3defd-167">One transaction has the **Sales tax receivable** tax direction.</span></span> <span data-ttu-id="3defd-168">وتشتمل الحركة الأخرى على اتجاه ضريبة **ضريبة المبيعات مستحقة الدفع**، ويتم تحديد خانة الاختيار **الرسوم العكسية**.</span><span class="sxs-lookup"><span data-stu-id="3defd-168">The other transaction has the **Sales tax payable** tax direction, and the **Reverse charge** check box is selected.</span></span>

<span data-ttu-id="3defd-169">في لقطة الشاشة التالية، تشتمل حركة واحدة على اتجاه **ضريبة المبيعات مستحقة القبض**، وتشتمل الحركةه الأخرى على اتجاه **ضريبة المبيعات مستحقة الدفع**.</span><span class="sxs-lookup"><span data-stu-id="3defd-169">In the following screenshot, one transaction has the **Sales tax receivable** direction, and the other transaction has the **Sales tax payable** direction.</span></span> 

![ضريبة المبيعات المرحلة](media/apac-sau-posted-sales-tax.png)

