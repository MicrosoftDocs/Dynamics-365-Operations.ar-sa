---
title: إنشاء مدفوعات المورد باستخدام مقترح دفع
description: يوفر هذا الموضوع نظرة عامة حول خيارات مقترحات الدفع ويتضمن بعض الأمثلة التي توضح كيفية عمل مقترحات الدفع.
author: abruer
manager: AnnBe
ms.date: 04/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14312
ms.assetid: 585d5b0b-1b79-4a03-ab18-528918070377
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 57e8ce38241933b16252f1c918b0f763a8f1be08
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176302"
---
# <a name="create-vendor-payments-by-using-a-payment-proposal"></a><span data-ttu-id="3ad5e-103">إنشاء دفعات المورد باستخدام مقترح دفع</span><span class="sxs-lookup"><span data-stu-id="3ad5e-103">Create vendor payments by using a payment proposal</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3ad5e-104">يوفر هذا الموضوع نظرة عامة حول خيارات مقترحات الدفع ويتضمن بعض الأمثلة التي توضح كيفية عمل مقترحات الدفع.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-104">This topic provides an overview of the payment proposal options and includes some examples that show how payment proposals work.</span></span> <span data-ttu-id="3ad5e-105">تُستخدم مقترحات الدفع في الكثير من الأحيان لإنشاء مدفوعات المورّد، إذ يمكن استخدام الاستعلام لتحديد فواتير المورّد للدفع بسرعة، استناداً إلى معايير مثل تاريخ الاستحقاق والخصم النقدي.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-105">Payment proposals are often used to create vendor payments, because the query can be used to quickly select vendor invoices for payment, based on criteria such as the due date and cash discount.</span></span> 

<span data-ttu-id="3ad5e-106">تستخدم المؤسسات في أغلب الأحيان مقترحات الدفع لإنشاء مدفوعات المورد، لأنه يمكن استخدام استعلام مقترح الدفع لتحديد فواتير المورد للدفع بسرعة، استنادًا إلى تاريخ الاستحقاق، والخصم النقدي، ومعايير أخرى.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-106">Organizations often use payment proposals to create vendor payments, because the payment proposal query can be used to quickly select vendor invoices for payment, based on the due date, cash discount, and other criteria.</span></span> 

<span data-ttu-id="3ad5e-107">ويحتوي استعلام مقترح الدفع على علامات تبويب مختلفة، كل منها يحتوي على خيارات مختلفة لتحديد الفواتير للدفع.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-107">The payment proposal query contains various tabs, each of which has different options for selecting invoices to pay.</span></span> <span data-ttu-id="3ad5e-108">تحتوي علامة تبويب **المحددة** على الخيارات التي تستخدمها معظم المؤسسات في أغلب الأحيان.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-108">The **Parameter** tab contains options that a majority of organization use most often.</span></span> <span data-ttu-id="3ad5e-109">في علامة التبويب السريعة **السجلات المطلوب تضمينها**، يمكنك تحديد أي فواتير أو موردين ينبغي تضمينهم للدفع من خلال تحديد نطاقات للخصائص المختلفة.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-109">On the **Records to include** FastTab, you can specify which invoices or vendors to include for payment by defining ranges for various characteristics.</span></span> <span data-ttu-id="3ad5e-110">على سبيل المثال، إذا أردت الدفع فقط لمجموعة محددة من الموردين، فمن ثم يمكنك تحديد عامل تصفية لمجموعة الموردين.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-110">For example, if you want to pay only a specific range of vendors, you can define a filter for the vendor range.</span></span> <span data-ttu-id="3ad5e-111">تستخدم هذه الوظيفة غالبًا لتحديد الفواتير لطريقة دفع معينة.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-111">This functionality is often used to select invoices for a specific of method of payment.</span></span> <span data-ttu-id="3ad5e-112">على سبيل المثال، إذا قمت بتحديد عامل تصفية تكون فيه **طريقة الدفع** = **الشيك**، يتم فقط تحديد الفواتير التي تحتوي على طريقة الدفع هذه للدفع، شريطة أن تفي بالمعايير الأخرى التي تم تحديدها في الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-112">For example, if you define a filter where **Method of payment** = **Check**, only invoices that have that method of payment are selected for payment, provided that they also meet other criteria that are specified in the query.</span></span> <span data-ttu-id="3ad5e-113">تحتوي علامة التبويب **المعلمات المتقدمة** على خيارات إضافية قد لا يكون بعضها مناسباً للمؤسسة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-113">The **Advanced parameters** tab contains additional options, some of which might not be relevant to your organization.</span></span> <span data-ttu-id="3ad5e-114">على سبيل المثال، تتضمن علامة التبويب هذه خيارات لدفع الفواتير للمدفوعات المركزية.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-114">For example, this tab contains the options for paying invoices for centralized payments.</span></span>

## <a name="parameters"></a><span data-ttu-id="3ad5e-115">المعلمات</span><span class="sxs-lookup"><span data-stu-id="3ad5e-115">Parameters</span></span>
-   <span data-ttu-id="3ad5e-116">**تحديد الفواتير بواسطة** – يمكن تحديد الفواتير في نطاق التاريخ بواسطة حقلي**من تاريخ** و **حتى تاريخ** حسب تاريخ الاستحقاق، أو تاريخ الخصم النقدي أو كليهما.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-116">**Select invoices by** – Invoices within the date range that is specified by the **From date** and **To date** fields can be selected by due date, cash discount date, or both.</span></span> <span data-ttu-id="3ad5e-117">وفي حالة استخدام تاريخ الخصم النقدي، يقوم النظام أولًا بالبحث عن الفواتير التي لها تاريخ خصم نقدي بين من تاريخ وإلى تاريخ.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-117">If you use the cash discount date, the system first looks for invoices that have a cash discount date between the from date and to date.</span></span> <span data-ttu-id="3ad5e-118">ويحدد النظام فيما بعد ما إذا كانت الفاتورة مؤهلة للخصم النقدي باستخدام تاريخ الجلسة للتأكد من أن تاريخ الخصم النقدي لم يمر بالفعل.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-118">The system then determines whether the invoice is eligible for the cash discount by using the session date to make sure that the cash discount date hasn’t already passed.</span></span>
-   <span data-ttu-id="3ad5e-119">**من تاريخ** و**حتى تاريخ** – يتم تحديد الفواتير التي تحتوي على تاريخ استحقاق أو تاريخ خصم نقدي في نطاق هذا التاريخ المحدد للدفع.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-119">**From date** and **To date** – Invoices that have a due date or cash discount date within this date range are selected for payment.</span></span>
-   <span data-ttu-id="3ad5e-120">**الحد الأدنى لتاريخ الدفع** -أدخل الحد الأدنى لتاريخ الدفع.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-120">**Minimum payment date** – Enter the minimum payment date.</span></span> <span data-ttu-id="3ad5e-121">على سبيل المثال، من حقلي **من تاريخ** و **إلى تاريخ** حدد نطاقًا من 1 سبتمبر إلى 10 سبتمبر، والحد الأدنى لتاريخ الدفع هو 5 سبتمبر.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-121">For example, the **From date** and **To date** fields specify a range from September 1 to September 10, and the minimum payment date is September 5.</span></span> <span data-ttu-id="3ad5e-122">وفي هذه الحالة، تشتمل كافة الفواتير التي بتاريخ استحقاق من 1 سبتمبر إلى 5 سبتمبر على تاريخ الدفع 5 سبتمبر.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-122">In this case, all invoices that have a due date from September 1 to September 5 have a payment date of September 5.</span></span> <span data-ttu-id="3ad5e-123">ومع ذلك، كافة الفواتير التي بتاريخ استحقاق من 5 سبتمبر إلى 10 سبتمبر تحتوي على تاريخ دفع يساوي تاريخ الاستحقاق لكل فاتورة.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-123">However, all invoices that have a due date from September 5 to September 10 have a payment date that is equal to the due date of each invoice.</span></span>
-   <span data-ttu-id="3ad5e-124">**حد المبلغ** – أدخل الحد الأقصى للمبلغ الإجمالي لكافة المدفوعات.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-124">**Amount limit** – Enter the maximum total amount for all payments.</span></span>
-   <span data-ttu-id="3ad5e-125">**إنشاء المدفوعات بدون معاينة الفاتورة** – إذا تم تعيين هذا الخيار إلى **نعم**، فسيتم إنشاء المدفوعات مباشرةً من صفحة **مدفوعات المورد**.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-125">**Create payments without invoice preview** – If this option is set to **Yes**, payments will be created immediately on the **Vendor payments** page.</span></span> <span data-ttu-id="3ad5e-126">وسيتم تخطي صفحة **مقترح الدفع**.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-126">The **Payment proposal** page will be skipped.</span></span> <span data-ttu-id="3ad5e-127">ولذلك، سيتم إنشاء المدفوعات بشكل أسرع.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-127">Therefore, payments will be created more quickly.</span></span> <span data-ttu-id="3ad5e-128">ولا يزال يمكن تعديل المدفوعات من صفحة **مدفوعات المورد**.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-128">Payments can still be modified from the **Vendor payments** page.</span></span> <span data-ttu-id="3ad5e-129">وبدلاً من ذلك، يمكنك الرجوع إلى صفحة **مقترح الدفع** باستخدام الزر **تحرير الفواتير لدفعة محددة**.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-129">Alternatively, you can return to the **Payment proposal** page by using the **Edit invoices for select payment** button.</span></span>

## <a name="advanced-options"></a><span data-ttu-id="3ad5e-130">خيارات متقدمة</span><span class="sxs-lookup"><span data-stu-id="3ad5e-130">Advanced options</span></span>
- <span data-ttu-id="3ad5e-131">**التحقق من رصيد المورد** – إذا تم تعيين هذا الخيار إلى **نعم**، يتحقق النظام من مورد ليس لديه رصيد مدين قبل أن يتم دفع أي فاتورة.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-131">**Check vendor balance** – If this option is set to **Yes**, the system verifies that a vendor doesn’t have a debit balance before any invoice is paid.</span></span> <span data-ttu-id="3ad5e-132">وإذا كان المورد لديه رصيد مدين، فلا يتم إنشاء أي دفعة.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-132">If a vendor does have a debit balance, no payment is created.</span></span> <span data-ttu-id="3ad5e-133">على سبيل المثال، قد يمتلك المورد مذكرات ائتمان، أو مدفوعات تم ترحيلها ولكن لم تتم تسويتها بعد.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-133">For example, the vendor might have credit memos, or payments that have been posted but haven't been settled yet.</span></span> <span data-ttu-id="3ad5e-134">وفي هذه الحالات، يجب عدم الدفع للمورد.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-134">In these cases, the vendor should not be paid.</span></span> <span data-ttu-id="3ad5e-135">وبدلاً من ذلك، ينبغي أن تتم تسوية مذكرات الائتمان أو المدفوعات في مقابل الفواتير المعلقة.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-135">Instead, the credit memos or payments should be settled against the outstanding invoices.</span></span>
- <span data-ttu-id="3ad5e-136">**حذف المدفوعات السالبة** -يعمل هذا الخيار بطريقة مختلفة، اعتماداً على ما إذا كان يتم إجراء المدفوعات للفواتير الفردية أو لمجموع الفواتير التي تفي بمعايير الدفع.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-136">**Delete negative payments** – This option works differently, depending on whether payments are made for individual invoices or for the sum of invoices that meet the payment criteria.</span></span> <span data-ttu-id="3ad5e-137">يتم تحديد هذا السلوك في طريقة الدفع.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-137">This behavior is defined on the method of payment.</span></span>
- <span data-ttu-id="3ad5e-138">**الدفع لكل فاتورة** – إذا تم تعيين خيار **حذف المدفوعات السالبة** إلى **نعم**، وتوجد ففاتورة لم تتم تسويتها لمورد، فيتم تحديد هذه الفاتورة فقط للدفع.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-138">**Payment for each invoice** – If the **Delete negative payments** option is set to **Yes**, and an unsettled invoice and payment exist for a vendor, only the invoice is selected for payment.</span></span> <span data-ttu-id="3ad5e-139">لا تتم تسوية الدفعة الموجودة في مقابل الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-139">The existing payment isn't settled against the invoice.</span></span> <span data-ttu-id="3ad5e-140">وإذا تم تعيين خيار **حذف المدفوعات السالبة** إلى **لا**، ولم تتم تسوية دفعة وفاتورة، فإنه يتم تحديد كلٍّ من الفاتورة والدفعة للدفع.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-140">If the **Delete negative payments** option is set to **No**, and an invoice and a payment aren't settled, both the invoice and the payment are selected for payment.</span></span> <span data-ttu-id="3ad5e-141">يتم إنشاء دفعة للدفع، ويتم إنشاء استرداد (دفعة سالبة) للدفع.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-141">A payment is created for the payment, and a refund (negative payment) is created for the payment.</span></span>
- <span data-ttu-id="3ad5e-142">**الدفع مقابل مبلغ الفواتير** – إذا تم تعيين خيار **حذف المدفوعات السالبة** إلى **نعم**، وتوجد دفعة لم تتم تسويتها ودفعة لمورد، فإنه يتم تحديد كلٍّ من الفاتورة التي لم تتم تسويتها والدفعة للدفع، وتتم إضافة المبالغ معًا لإنتاج إجمالي مبلغ الدفع.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-142">**Payment for sum of invoices** – If the **Delete negative payments** option is set to **Yes**, and an unsettled invoice and payment exist for a vendor, both the unsettled invoice and the payment are selected for payment, and the amounts are added together to produce the total payment amount.</span></span> <span data-ttu-id="3ad5e-143">يحدث الاستثناء الوحيد إذا أدى المجموع إلى استرداد.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-143">The only exception occurs if the sum results in a refund.</span></span> <span data-ttu-id="3ad5e-144">في هذه الحالة، لا يتم تحديد الفاتورة ولا الدفعة.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-144">In this case, neither the invoice nor the payment is selected.</span></span> <span data-ttu-id="3ad5e-145">وإذا تم تعيين خيار **حذف الدفعات السالبة** إلى **لا**، ولم تتم تسوية فاتورة ودفعة، فإنه يتم تحديد كلٍّ من الفاتورة والدفعة للدفع، وتتم إضافة المبالغ معًا لإنتاج إجمالي مبلغ الدفع.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-145">If the **Delete negative payments** option is set to **No**, and an invoice and a payment aren't settled, both the invoice and the payment are selected for payment, and the amounts are added together to produce the total payment amount.</span></span>
- <span data-ttu-id="3ad5e-146">**طباعة تقرير فقط** – قم تعيين هذا الخيار إلى **نعم** لمشاهدة نتائج مقترح الدفع في تقرير، ولكن بدون إنشاء أية مدفوعات.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-146">**Print report only** – Set this option to **Yes** to see the results of the payment proposal on a report, but without creating any payments.</span></span>
- <span data-ttu-id="3ad5e-147">**تضمين فواتير المورد من كيانات قانونية أخرى‬** – إذا كان لدى المؤسسة الخاصة بك عملية مركزية للدفع، ويجب أن يتضمن مقترح الدفع الفواتير من الكيانات القانونية الأخرى التي يتم تضمينها في معايير البحث، فقم بتعيين هذا الخيار إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-147">**Include vendor invoices from other legal entities** – If your organization has a centralized process for payment, and the payment proposal should include invoices from other legal entities that are included in the search criteria, set this option to **Yes**.</span></span>
- <span data-ttu-id="3ad5e-148">**اقتراح عملية دفع مورد منفصلة لكل كيان قانوني‬** – إذا تم تعيين هذا الخيار إلى **نعم**، يتم إنشاء عملية دفع منفصلة لكل كيان قانوني لكل مورد.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-148">**Propose separate vendor payment per legal entity** – If this option is set to **Yes**, a separate payment is created for each legal entity per vendor.</span></span> <span data-ttu-id="3ad5e-149">المورد في الدفع هو المورد من الفاتورة من كل كيان قانوني.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-149">The vendor on the payment is the vendor from the invoice from each legal entity.</span></span> <span data-ttu-id="3ad5e-150">إذا تم تعيين هذا الخيار إلى **نعم**، وكان لدى المورد نفسه فواتير في العديد من الكيانات القانونية، فإنه يتم إنشاء عملية دفع واحدة للمبلغ الإجمالي للفواتير المحددة.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-150">If this option is set to **No**, and the same vendor has invoices in multiple legal entities, one payment is created for the total amount of the selected invoices.</span></span> <span data-ttu-id="3ad5e-151">المورد في عملية الدفع هو المورد في الكيان القانوني الحالي.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-151">The vendor on the payment is the vendor in the current legal entity.</span></span> <span data-ttu-id="3ad5e-152">إذا لم يوجد حساب المورد في الكيان القانوني الحالي، فإنه يتم استخدام حساب المورد للفاتورة الأولى التي يجب دفعها.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-152">If the vendor account doesn’t exist in the current legal entity, the vendor account of the first invoice that must be paid is used.</span></span>
- <span data-ttu-id="3ad5e-153">**عمله الدفع** - يحدد هذا الحقل العملة التي يتم إنشاء كافة المدفوعات بها.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-153">**Payment currency** – This field specifies the currency that all payments are created in.</span></span> <span data-ttu-id="3ad5e-154">وإذا لم يتم تحديد عملة، فإنه يتم دفع كل فاتورة بعملة الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-154">If a currency isn’t defined, each invoice is paid in the currency of the invoice.</span></span>
- <span data-ttu-id="3ad5e-155">**يوم أسبوع الدفع‬** – أدخل يوم الأسبوع الذي يجب فيه إجراء الدفع.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-155">**Payment weekday** – Enter the day of the week when the payment should be made.</span></span> <span data-ttu-id="3ad5e-156">يتم استخدام هذا الحقل فقط إذا تم إعداد طريقة الدفع لإجمالي الفواتير للدفع في يوم معين من الأسبوع.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-156">This field is used only if the method of payment is set up to total invoices for payment on a specific day of the week.</span></span>
- <span data-ttu-id="3ad5e-157">**نوع حساب مقابل** و **حساب مقابل** – قم بتعيين هذه الحقول لتحديد نوع حساب محدد (مثل **دفتر الأستاذ** أو **البنك**) والحساب المقابل (مثل حساب بنكي معين).</span><span class="sxs-lookup"><span data-stu-id="3ad5e-157">**Offset account type** and **Offset account** – Set these fields to define a specific account type (such as **Ledger** or **Bank**) and offset account (such as a specific bank account).</span></span> <span data-ttu-id="3ad5e-158">وتحدد طريقة الدفع للفاتورة نوع الحساب المقابل الافتراضي والحساب المقابل، ولكن يمكنك استخدام هذه الحقول لتجاوز القيم الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-158">The method of payment for the invoice defines the default offset account type and offset account, but you can use these fields to override the default values.</span></span>
- <span data-ttu-id="3ad5e-159">**تاريخ الدفع الملخص** – يُستخدم فقط عند تعيين حقل **الفترة** على طريقة الدفع إلى **إجمالي**.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-159">**Summarized payment date** – This is only used when the **Period** field on the method of payment is set to **Total**.</span></span> <span data-ttu-id="3ad5e-160">إذا تم تحديد تاريخ، يتم إنشاء كافة المدفوعات في هذا التاريخ.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-160">If a date is defined, all payments are created on this date.</span></span> <span data-ttu-id="3ad5e-161">تم تجاهل حقل **الحد الأدنى لتاريخ الدفع**.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-161">The **Minimum payment date** field is ignored.</span></span>
- <span data-ttu-id="3ad5e-162">**عوامل التصفية الإضافية** – في علامة التبويب السريع **السجلات المُراد تضمينها**، يمكن تحديد مجموعات المعايير الإضافية.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-162">**Additional filters** – On the **Records to include** FastTab, you can define additional ranges of criteria.</span></span> <span data-ttu-id="3ad5e-163">على سبيل المثال، إذا أردت الدفع فقط لمجموعة محددة من الموردين، فمن ثم يمكنك تحديد عامل تصفية لمجموعة الموردين.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-163">For example, if you want to pay only a range of vendors, you can define a filter for the vendor range.</span></span> <span data-ttu-id="3ad5e-164">تستخدم هذه الوظيفة غالبًا لتحديد الفواتير لطريقة دفع معينة.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-164">This functionality is often used to select invoices for a specific of method of payment.</span></span> <span data-ttu-id="3ad5e-165">على سبيل المثال، إذا قمت بتحديد عامل تصفية تكون فيه **طريقة الدفع** = **الشيك**، يتم فقط تحديد الفواتير التي تحتوي على طريقة الدفع هذه للدفع، شريطة أن تفي بالمعايير الأخرى التي تم تحديدها في الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-165">For example, if you define a filter where **Method of payment** = **Check**, only invoices that have that method of payment are selected for payment, provided that they also meet other criteria that are specified in the query.</span></span>

## <a name="scenarios"></a><span data-ttu-id="3ad5e-166">السيناريوهات</span><span class="sxs-lookup"><span data-stu-id="3ad5e-166">Scenarios</span></span>

| <span data-ttu-id="3ad5e-167">المورِد</span><span class="sxs-lookup"><span data-stu-id="3ad5e-167">Vendor</span></span> | <span data-ttu-id="3ad5e-168">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="3ad5e-168">Invoice</span></span> | <span data-ttu-id="3ad5e-169">تاريخ الفاتورة</span><span class="sxs-lookup"><span data-stu-id="3ad5e-169">Invoice date</span></span> | <span data-ttu-id="3ad5e-170">مبلغ الفاتورة</span><span class="sxs-lookup"><span data-stu-id="3ad5e-170">Invoice amount</span></span> | <span data-ttu-id="3ad5e-171">تاريخ الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="3ad5e-171">Due date</span></span> | <span data-ttu-id="3ad5e-172">تاريخ الخصم النقدي</span><span class="sxs-lookup"><span data-stu-id="3ad5e-172">Cash discount date</span></span> | <span data-ttu-id="3ad5e-173">مبلغ الخصم النقدي</span><span class="sxs-lookup"><span data-stu-id="3ad5e-173">Cash discount amount</span></span> |
|--------|---------|--------------|----------------|----------|--------------------|----------------------|
| <span data-ttu-id="3ad5e-174">3050</span><span class="sxs-lookup"><span data-stu-id="3ad5e-174">3050</span></span>   | <span data-ttu-id="3ad5e-175">1001</span><span class="sxs-lookup"><span data-stu-id="3ad5e-175">1001</span></span>    | <span data-ttu-id="3ad5e-176">15 يونيو</span><span class="sxs-lookup"><span data-stu-id="3ad5e-176">June 15</span></span>      | <span data-ttu-id="3ad5e-177">500.00</span><span class="sxs-lookup"><span data-stu-id="3ad5e-177">500.00</span></span>         | <span data-ttu-id="3ad5e-178">15 يوليو</span><span class="sxs-lookup"><span data-stu-id="3ad5e-178">July 15</span></span>  | <span data-ttu-id="3ad5e-179">29 يونيو</span><span class="sxs-lookup"><span data-stu-id="3ad5e-179">June 29</span></span>            | <span data-ttu-id="3ad5e-180">10.00</span><span class="sxs-lookup"><span data-stu-id="3ad5e-180">10.00</span></span>                |
| <span data-ttu-id="3ad5e-181">3050</span><span class="sxs-lookup"><span data-stu-id="3ad5e-181">3050</span></span>   | <span data-ttu-id="3ad5e-182">1002</span><span class="sxs-lookup"><span data-stu-id="3ad5e-182">1002</span></span>    | <span data-ttu-id="3ad5e-183">20 يونيو</span><span class="sxs-lookup"><span data-stu-id="3ad5e-183">June 20</span></span>      | <span data-ttu-id="3ad5e-184">600.00</span><span class="sxs-lookup"><span data-stu-id="3ad5e-184">600.00</span></span>         | <span data-ttu-id="3ad5e-185">20 يوليو</span><span class="sxs-lookup"><span data-stu-id="3ad5e-185">July 20</span></span>  | <span data-ttu-id="3ad5e-186">4 يوليو</span><span class="sxs-lookup"><span data-stu-id="3ad5e-186">July 4</span></span>             | <span data-ttu-id="3ad5e-187">12.00</span><span class="sxs-lookup"><span data-stu-id="3ad5e-187">12.00</span></span>                |
| <span data-ttu-id="3ad5e-188">3075</span><span class="sxs-lookup"><span data-stu-id="3ad5e-188">3075</span></span>   | <span data-ttu-id="3ad5e-189">1003</span><span class="sxs-lookup"><span data-stu-id="3ad5e-189">1003</span></span>    | <span data-ttu-id="3ad5e-190">15 يونيو</span><span class="sxs-lookup"><span data-stu-id="3ad5e-190">June 15</span></span>      | <span data-ttu-id="3ad5e-191">250.00</span><span class="sxs-lookup"><span data-stu-id="3ad5e-191">250.00</span></span>         | <span data-ttu-id="3ad5e-192">29 يونيو</span><span class="sxs-lookup"><span data-stu-id="3ad5e-192">June 29</span></span>  |                    | <span data-ttu-id="3ad5e-193">0.00</span><span class="sxs-lookup"><span data-stu-id="3ad5e-193">0.00</span></span>                 |
| <span data-ttu-id="3ad5e-194">3100</span><span class="sxs-lookup"><span data-stu-id="3ad5e-194">3100</span></span>   | <span data-ttu-id="3ad5e-195">1004</span><span class="sxs-lookup"><span data-stu-id="3ad5e-195">1004</span></span>    | <span data-ttu-id="3ad5e-196">17 يونيو</span><span class="sxs-lookup"><span data-stu-id="3ad5e-196">June 17</span></span>      | <span data-ttu-id="3ad5e-197">100.00</span><span class="sxs-lookup"><span data-stu-id="3ad5e-197">100.00</span></span>         | <span data-ttu-id="3ad5e-198">17 يوليو</span><span class="sxs-lookup"><span data-stu-id="3ad5e-198">July 17</span></span>  | <span data-ttu-id="3ad5e-199">1 يوليو</span><span class="sxs-lookup"><span data-stu-id="3ad5e-199">July 1</span></span>             | <span data-ttu-id="3ad5e-200">1.00</span><span class="sxs-lookup"><span data-stu-id="3ad5e-200">1.00</span></span>                 |

<span data-ttu-id="3ad5e-201">في 1 يوليو، تقوم فوزية بالدفع للموردين.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-201">On July 1, April pays vendors.</span></span> <span data-ttu-id="3ad5e-202">وتستخدم مقترح دفع لمساعدتها في إنجاز هذه المهمة بكفاءة أكبر.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-202">She uses a payment proposal to help her complete this task more efficiently.</span></span>

### <a name="option-1-by-cash-discount"></a><span data-ttu-id="3ad5e-203">الخيار 1: حسب الخصم النقدي</span><span class="sxs-lookup"><span data-stu-id="3ad5e-203">Option 1: By cash discount</span></span>

<span data-ttu-id="3ad5e-204">تحدد فوزية **الخصم النقدي** كنوع المقترح.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-204">April selects **Cash discount** as the proposal type.</span></span> <span data-ttu-id="3ad5e-205">وتقوم بإدخال تاريخ نطاق من 26 يونيو حتى 10 يوليو.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-205">She enters a date range of June 26 to July 10.</span></span> <span data-ttu-id="3ad5e-206">يتم تضمين الفواتير التالية في المقترح:</span><span class="sxs-lookup"><span data-stu-id="3ad5e-206">The following invoices are included in the proposal:</span></span>

-   <span data-ttu-id="3ad5e-207">1002، لأن تاريخ الخصم 4 يوليو موجود في نطاق تواريخ الدفع.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-207">1002, because the discount date of July 4 is in the range of payment dates.</span></span>
-   <span data-ttu-id="3ad5e-208">1004، لأن تاريخ الخصم 1 يوليو موجود في نطاق تواريخ الدفع.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-208">1004, because the discount date of July 1 is in the range of payment dates.</span></span>

<span data-ttu-id="3ad5e-209">لا يتم تضمين الفواتير التالية في المقترح:</span><span class="sxs-lookup"><span data-stu-id="3ad5e-209">The following invoices aren't included in the proposal:</span></span>

-   <span data-ttu-id="3ad5e-210">1001، لأن تاريخ الخصم 29 يونيو قد انقضى، وبالتالي لم تعد هذه الفاتورة مؤهلة للخصم النقدي.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-210">1001, because the discount date of June 29 has already expired, so this invoice is no longer eligible for the cash discount.</span></span>
-   <span data-ttu-id="3ad5e-211">1003، لأن هذه الفاتورة لا تتضمن تاريخ خصم.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-211">1003, because this invoice doesn't have a discount date.</span></span>

### <a name="option-2-by-due-date"></a><span data-ttu-id="3ad5e-212">الخيار 2: حسب تاريخ الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="3ad5e-212">Option 2: By due date</span></span>

<span data-ttu-id="3ad5e-213">تحدد فوزية **لكل تاريخ استحقاق** كنوع المقترح.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-213">April selects **Per due date** as the proposal type.</span></span> <span data-ttu-id="3ad5e-214">وتقوم بإدخال تاريخ نطاق من 26 يونيو حتى 10 يوليو.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-214">She enters a date range of June 26 to July 10.</span></span> <span data-ttu-id="3ad5e-215">يتم تضمين الفواتير التالية في المقترح:</span><span class="sxs-lookup"><span data-stu-id="3ad5e-215">The following invoices are included in the proposal:</span></span>

-   <span data-ttu-id="3ad5e-216">1003، لأن تاريخ الاستحقاق 29 يونيو موجود في نطاق تواريخ الدفع.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-216">1003, because the due date of June 29 is in the range of payment dates.</span></span>

<span data-ttu-id="3ad5e-217">لا يتم تضمين الفواتير التالية في المقترح:</span><span class="sxs-lookup"><span data-stu-id="3ad5e-217">The following invoices aren't included in the proposal:</span></span>

-   <span data-ttu-id="3ad5e-218">1001، لأن تاريخ الاستحقاق 15 يوليو موجود خارج نطاق تواريخ الدفع.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-218">1001, because the due date of July 15 is outside the range of payment dates.</span></span>
-   <span data-ttu-id="3ad5e-219">1002، لأن تاريخ الاستحقاق 20 يوليو موجود خارج نطاق تواريخ الدفع.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-219">1002, because the due date of July 20 is outside the range of payment dates.</span></span>
-   <span data-ttu-id="3ad5e-220">1004، لأن تاريخ الاستحقاق 17 يوليو موجود خارج نطاق تواريخ الدفع.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-220">1004, because the due date of July 17 is outside the range of payment dates.</span></span>

### <a name="option-3-by-due-date-and-cash-discount"></a><span data-ttu-id="3ad5e-221">الخيار 3: حسب تاريخ الاستحقاق والخصم النقدي</span><span class="sxs-lookup"><span data-stu-id="3ad5e-221">Option 3: By due date and cash discount</span></span>

<span data-ttu-id="3ad5e-222">تحدد فوزية **تاريخ الاستحقاق والخصم النقدي** كنوع المقترح.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-222">April selects **Due date and cash discount** as the proposal type.</span></span> <span data-ttu-id="3ad5e-223">وتقوم بإدخال تاريخ نطاق من 26 يونيو حتى 10 يوليو.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-223">She enters a date range of June 26 to July 10.</span></span> <span data-ttu-id="3ad5e-224">يتم تضمين الفواتير التالية في المقترح:</span><span class="sxs-lookup"><span data-stu-id="3ad5e-224">The following invoices are included in the proposal:</span></span>

-   <span data-ttu-id="3ad5e-225">1003، لأن تاريخ الاستحقاق 29 يونيو موجود في نطاق تواريخ الدفع.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-225">1003, because the due date of June 29 is in the range of payment dates.</span></span>
-   <span data-ttu-id="3ad5e-226">1002، لأن تاريخ الخصم 4 يوليو موجود في نطاق تواريخ الدفع.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-226">1002, because the discount date of July 4 is in the range of payment dates.</span></span>
-   <span data-ttu-id="3ad5e-227">1004، لأن تاريخ الخصم 1 يوليو موجود في نطاق تواريخ الدفع.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-227">1004, because the discount date of July 1 is in the range of payment dates.</span></span>

<span data-ttu-id="3ad5e-228">لا يتم تضمين الفواتير التالية في المقترح:</span><span class="sxs-lookup"><span data-stu-id="3ad5e-228">The following invoices aren't included in the proposal:</span></span>

-   <span data-ttu-id="3ad5e-229">1001، لأن تاريخ الخصم 29 يونيو قد انقضى، وبالتالي لم تعد هذه الفاتورة مؤهلة للخصم النقدي، وتاريخ الاستحقاق 15 يوليو موجود أيضًا خارج نطاق التاريخ.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-229">1001, because the discount date of June 29 has already expired, so this invoice is no longer eligible for the cash discount, and the due date of July 15 is also outside the date range.</span></span>

## <a name="country-specific-considerations"></a><span data-ttu-id="3ad5e-230">اعتبارات خاصة بكل بلد</span><span class="sxs-lookup"><span data-stu-id="3ad5e-230">Country specific considerations</span></span>
### <a name="norway"></a><span data-ttu-id="3ad5e-231">النرويج</span><span class="sxs-lookup"><span data-stu-id="3ad5e-231">Norway</span></span>

#### <a name="dimension-control"></a><span data-ttu-id="3ad5e-232">التحكم في البُعد</span><span class="sxs-lookup"><span data-stu-id="3ad5e-232">Dimension control</span></span>

<span data-ttu-id="3ad5e-233">يتيح لك التحكم في البُعد‬ إمكانية التحكم في تجميع البنود التي تم إنشاؤها باستخدام مقترح الدفع وتعيين الأبعاد الافتراضية استنادًا إلى الأبعاد المالية التي يتم استخدامها للفواتير المطبقة.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-233">Dimension control allows you to control grouping of generated lines by payment proposal and set default dimensions based on financial dimensions used for the applied invoices.</span></span> <span data-ttu-id="3ad5e-234">ضمن سياق البلد للنرويج لكل طريقة دفع، توجد علامة تبويب البعد المالي حيث يمكنك تنشيط التحكم في البُعد، فضلا عن تمكين التجميع لكل بُعد.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-234">Under Norwegian country context for each method of payment there is financial dimension tab where you can activate dimension control as well as enable grouping for each dimension.</span></span> <span data-ttu-id="3ad5e-235">الخيارات المحتملة هي:</span><span class="sxs-lookup"><span data-stu-id="3ad5e-235">Possible options are:</span></span>

-   <span data-ttu-id="3ad5e-236">تعطيل حقل **التحكم في البُعد**.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-236">**Dimension control** field is disabled.</span></span> <span data-ttu-id="3ad5e-237">يعمل مقترح الدفع كما في أي بلد آخر.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-237">The payment proposal behaves as for any other country.</span></span>
-   <span data-ttu-id="3ad5e-238">تنشيط حقل **التحكم في البُعد** من دون أي تعريف إضافي للأبعاد.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-238">**Dimension control** field is activated without further defining the dimensions.</span></span> <span data-ttu-id="3ad5e-239">سيتم إنشاء مقترح الدفع من دون مراعاة الأبعاد.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-239">The payment proposal will be created without taking dimensions into consideration.</span></span> <span data-ttu-id="3ad5e-240">لا ترث الحركة المنشأة أي أبعاد من الإدخال المطبق.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-240">The created transaction inherits no dimensions from the applied entry.</span></span>
-   <span data-ttu-id="3ad5e-241">تنشيط حقل **التحكم في البُعد** وتمكين الأبعاد الإضافية.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-241">**Dimension control** field is activated and the further dimensions are enabled.</span></span> <span data-ttu-id="3ad5e-242">يمكنك الآن تعريف كيفية نسخ الأبعاد إلى دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-242">Now you define how the dimensions will be copied to the journal.</span></span> <span data-ttu-id="3ad5e-243">على سبيل المثال: • قم بتحديد خانة الاختيار **BusinessUnit** لإنشاء مقترح دفع لكل وحدة أعمال لطريقة الدفع، • قم بتحديد خانة الاختيارة **CostCenter** لإنشاء مقترح دفع لكل مركز تكلفة لطريقة الدفع.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-243">For example: • Select the **BusinessUnit** check box to create a payment proposal per business unit for the method of payment, • Select the **CostCenter** check box to create a payment proposal per cost center for the method of payment</span></span>

> <span data-ttu-id="3ad5e-244">[</span><span class="sxs-lookup"><span data-stu-id="3ad5e-244">[</span></span>[!NOTE]
> <span data-ttu-id="3ad5e-245">إذا حددت أكثر من بُعد في الخيار الثالث، فسيتم إنشاء مقترح دفع لمجموعة الأبعاد.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-245">If you select more than one dimension in the third option, a payment proposal is created for the dimension combination.</span></span>

#### <a name="bank-account-selection"></a><span data-ttu-id="3ad5e-246">تحديد الحساب البنكي</span><span class="sxs-lookup"><span data-stu-id="3ad5e-246">Bank account selection</span></span>

<span data-ttu-id="3ad5e-247">يمكنك تحديد حساب دفع دين قياسي لكل طريقة دفع بغض النظر عن سياق البلد.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-247">You can define a standard debiting payment account per method of payment regardless country context.</span></span> <span data-ttu-id="3ad5e-248">وسيتم تعيين ذلك في بنود الدفع التي تنشأ بواسطة المقترح.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-248">This will be set in payment lines generated by a proposal.</span></span> <span data-ttu-id="3ad5e-249">باستخدام ميزة الحساب البنكي، يمكنك تحديد عدة حسابات بنكية للدين تُدار بواسطة البعد والعملة أو مجموعة من هذه العناصر لاستخدام حسابات بنكية مختلفة للدين، تبعًا لكل مجموعة.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-249">With the bank account feature, you can define multiple debiting bank accounts managed by dimension and currency or a combination of these to use different debiting bank accounts, depending on each combination.</span></span> <span data-ttu-id="3ad5e-250">يمكنك إعداد هذه المجموعات في صفحة **طرق الدفع** باستخدام زر **الحسابات البنكية** المتوفر لكل طريقة دفع مع **نوع حساب الترحيل** = **البنك‏‎**.</span><span class="sxs-lookup"><span data-stu-id="3ad5e-250">You can set up these combinations in **Methods of payments** page by using the **Bank accounts** button available for each method of payment with **Posting account type** = **Bank**.</span></span>


