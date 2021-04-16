---
title: إعداد وتفويض وتسجيل بطاقة الائتمان
description: توفر هذه المقالة نظرة عامة حول تفويض بطاقة الائتمان في Microsoft Dynamics 365 Finance. وهي تتضمن معلومات حول كيفية إعداد خدمة دفع وإضافة بطاقة ائتمان إلى أمر مبيعات وإلغاء تخويل.
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CreditCardProcessors, CustTable, SalesTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 3041
ms.assetid: 678f6899-bfa5-439b-aaca-b4affcc338ba
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e6b59d54df9427961e2c4fb6f1387646d6fe8dfc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837119"
---
# <a name="credit-card-setup-authorization-and-capture"></a><span data-ttu-id="bd3e5-104">إعداد وتفويض وتسجيل بطاقة الائتمان</span><span class="sxs-lookup"><span data-stu-id="bd3e5-104">Credit card setup, authorization, and capture</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bd3e5-105">توفر هذه المقالة نظرة عامة حول تفويض بطاقة الائتمان في Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="bd3e5-105">This article provides an overview of credit card authorization in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="bd3e5-106">وهي تتضمن معلومات حول كيفية إعداد خدمة دفع وإضافة بطاقة ائتمان إلى أمر مبيعات وإلغاء تخويل.</span><span class="sxs-lookup"><span data-stu-id="bd3e5-106">It includes information about how to set up a payment service, add a credit card to a sales order, and void an authorization.</span></span>

<a name="setting-up-the-credit-card-payment-service"></a><span data-ttu-id="bd3e5-107">إعداد خدمة مدفوعات بطاقة الائتمان</span><span class="sxs-lookup"><span data-stu-id="bd3e5-107">Setting up the credit card payment service</span></span>
------------------------------------------

<span data-ttu-id="bd3e5-108">لاستخدام بطاقات الائتمان، يجب إعداد وتنشيط خدمة دفع في صفحة خدمات الدفع.</span><span class="sxs-lookup"><span data-stu-id="bd3e5-108">To use credit cards, you must set up and activate a payment service on the Payment services page.</span></span> <span data-ttu-id="bd3e5-109">خدمة دفع بمثابة جسر بين الكيان القانوني والبنك الذي يعالج مصاريف بطاقة ائتمان العميل.</span><span class="sxs-lookup"><span data-stu-id="bd3e5-109">A payment service acts as a bridge between your legal entity and the bank that processes a customer's credit card charges.</span></span> <span data-ttu-id="bd3e5-110">ويجب عليك العمل مع موفر بطاقة الائتمان المذكور في حقل رابط الدفع وإعداد حساب لدى هذا الموفر.</span><span class="sxs-lookup"><span data-stu-id="bd3e5-110">You must work with a credit card provider that is listed in the Payment connector field and set up an account with that provider.</span></span> <span data-ttu-id="bd3e5-111">ويجب إعداد الخيارات الأخرى الموجودة في صفحة خدمات الدفع، وإعداد أنواع بطاقات الائتمان لأمريكان إكسبريس، وديسكفري، وماستر كارد، وديسكفري في صفحة أنواع بطاقات الائتمان، وتنشيط الموفر كموفر افتراضي.</span><span class="sxs-lookup"><span data-stu-id="bd3e5-111">You must then set up the other options on the Payment services page, set up credit card types for American Express, Discover, MasterCard, and Discover on the Credit card types page, and activate the provider as the default provider.</span></span> <span data-ttu-id="bd3e5-112">كما يجب اتباع هذه الخطوات لإكمال الإعداد الخاص بك:</span><span class="sxs-lookup"><span data-stu-id="bd3e5-112">You must also follow these steps to complete your setup:</span></span>
-   <span data-ttu-id="bd3e5-113">في صفحة معلمات الحسابات المدينة، حدد المعلمات لاستخدام تفويضات بطاقة الائتمان.</span><span class="sxs-lookup"><span data-stu-id="bd3e5-113">On the Accounts receivable parameters page, specify parameters for using credit card authorizations.</span></span>
-   <span data-ttu-id="bd3e5-114">وفي صفحة شروط الدفع، قم بإعداد شروط الدفع لبطاقات الائتمان.</span><span class="sxs-lookup"><span data-stu-id="bd3e5-114">On the Terms of payment page, set up payment terms for credit cards.</span></span> <span data-ttu-id="bd3e5-115">وفي حقل نوع الدفع، حدد بطاقة الائتمان.</span><span class="sxs-lookup"><span data-stu-id="bd3e5-115">In the Payment type field, select Credit card.</span></span>
-   <span data-ttu-id="bd3e5-116">في صفحة بطاقات ائتمان العميل، أدخل معلومات بطاقة الائتمان للعملاء.</span><span class="sxs-lookup"><span data-stu-id="bd3e5-116">On the Customer credit cards page, enter credit card information for customers.</span></span>

## <a name="adding-a-new-credit-card"></a><span data-ttu-id="bd3e5-117">إضافة بطاقة ائتمان جديدة</span><span class="sxs-lookup"><span data-stu-id="bd3e5-117">Adding a new credit card</span></span>
<span data-ttu-id="bd3e5-118">يمكنك إنشاء سجلات بطاقة ائتمان جديدة في صفحة العملاء باستخدام العميل، والإعداد، وبطاقة الائتمان.</span><span class="sxs-lookup"><span data-stu-id="bd3e5-118">You can create new credit card records on the Customers page by using Customer, Set up, Credit card.</span></span> <span data-ttu-id="bd3e5-119">كما يمكنك إنشاء سجلات بطاقة الائتمان عند إدخال أوامر المبيعات في صفحة أمر المبيعات، باستخدام الإدارة، والعميل، وبطاقة الائتمان، والسجل.</span><span class="sxs-lookup"><span data-stu-id="bd3e5-119">You can also create credit card records when you enter sales orders on the Sales order page, by using Manage, Customer, Credit card, Register.</span></span>

<a name="adding-a-credit-card-to-a-sales-order"></a><span data-ttu-id="bd3e5-120">إضافة بطاقة ائتمان إلى أمر مبيعات</span><span class="sxs-lookup"><span data-stu-id="bd3e5-120">Adding a credit card to a sales order</span></span>
-------------------------------------

<span data-ttu-id="bd3e5-121">يمكنك إضافة بطاقة ائتمان إلى أمر مبيعات عن طريق تحديد بطاقة ائتمان في البحث عن بطاقة الائتمان في علامة التبويب السريع السعر والخصومات في صفحة أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="bd3e5-121">You can add a credit card to a sales order by selecting a credit card in the credit card lookup on the Price and discounts FastTab on the Sales order page.</span></span> <span data-ttu-id="bd3e5-122">ولبدء عملية التفويض، في "جزء الإجراءات"، ضمن علامة التبويب إدارة، حدد بطاقة الائتمان وتفويض.</span><span class="sxs-lookup"><span data-stu-id="bd3e5-122">To start the authorization process, on the Action Pane, on the Manage tab, select Credit card and Authorize.</span></span>

<a name="authorizing-a-credit-card"></a><span data-ttu-id="bd3e5-123">تفويض بطاقة ائتمان</span><span class="sxs-lookup"><span data-stu-id="bd3e5-123">Authorizing a credit card</span></span>
-------------------------

<span data-ttu-id="bd3e5-124">عند تفويض بطاقة الائتمان، يتم التحقق من رقم البطاقة واسم حامل البطاقة، كما يتم التأكيد على الرصيد الدائن المتوفر.</span><span class="sxs-lookup"><span data-stu-id="bd3e5-124">When a credit card is authorized, the card number and cardholder's name are verified, and the available credit balance is confirmed.</span></span> <span data-ttu-id="bd3e5-125">وبشكل اختياري، يتم التحقق من صحة قيمة التحقق من البطاقة وعنوان حامل البطاقة.</span><span class="sxs-lookup"><span data-stu-id="bd3e5-125">Optionally, the card verification value and the cardholder’s address are verified.</span></span> <span data-ttu-id="bd3e5-126">ويتم بعد ذلك تقليل الرصيد الدائن المتوفر الخاص بالعميل بمقدار مبلغ الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="bd3e5-126">The customer's available credit balance is then reduced by the amount of the invoice.</span></span> <span data-ttu-id="bd3e5-127">وتقوم خدمة الدفع بإرسال معلومات تفيد أنه تم اعتماد بطاقة الائتمان أو رفضها.</span><span class="sxs-lookup"><span data-stu-id="bd3e5-127">The payment service sends information that the credit card has been approved or declined.</span></span> <span data-ttu-id="bd3e5-128">وعند فوترة أمر المبيعات، يتم حساب بطاقة الائتمان (تسجيلها) لمبلغ الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="bd3e5-128">When the sales order is invoiced, the credit card is charged (captured) for the invoice amount.</span></span>

### <a name="card-verification-value"></a><span data-ttu-id="bd3e5-129">قيمة التحقق من البطاقة</span><span class="sxs-lookup"><span data-stu-id="bd3e5-129">Card verification value</span></span>

<span data-ttu-id="bd3e5-130">يمكنك طلب قيمة التحقق من البطاقة الذي يُشار إليها أحياناً بكود الأمان للبطاقة.</span><span class="sxs-lookup"><span data-stu-id="bd3e5-130">You can require the card verification value, which is sometimes referred to as the card's security code.</span></span> <span data-ttu-id="bd3e5-131">وبالنسبة إلى أمريكان إكسبريس، هذه قيمة تتكون من أربعة أرقام.</span><span class="sxs-lookup"><span data-stu-id="bd3e5-131">For American Express, this is a four-digit value.</span></span> <span data-ttu-id="bd3e5-132">وبالنسبة إلى ديسكفري، وماستر كارد، والتأشيرة، إنها قيمة مكونة من ثلاثة أرقام.</span><span class="sxs-lookup"><span data-stu-id="bd3e5-132">For Discover, MasterCard, and Visa, it is a three-digit value.</span></span>

### <a name="address-verification"></a><span data-ttu-id="bd3e5-133">التحقق من العنوان</span><span class="sxs-lookup"><span data-stu-id="bd3e5-133">Address verification</span></span>

<span data-ttu-id="bd3e5-134">يتم دائماً إرسال معلومات التحقق من صحة العنوان إلى موفر الدفع.</span><span class="sxs-lookup"><span data-stu-id="bd3e5-134">Address verification information is always sent to the payment provider.</span></span> <span data-ttu-id="bd3e5-135">‏‫ويمكنك تحديد كمية المعلومات المطلوبة لحركة ليتم قبوله.</span><span class="sxs-lookup"><span data-stu-id="bd3e5-135">You can decide how much information is required for a transaction to be accepted.</span></span> <span data-ttu-id="bd3e5-136">ويجب التأكد من التحقق مع الموفر الخاص بك لتحديد ما إذا كان يقبل هذه المعلومات.‬</span><span class="sxs-lookup"><span data-stu-id="bd3e5-136">Be sure to check with your provider to determine whether it accepts this information.</span></span> <span data-ttu-id="bd3e5-137">فيما يلي خيارات التحقق من صحة العنوان:</span><span class="sxs-lookup"><span data-stu-id="bd3e5-137">Here are the options for address verification:</span></span>
-   <span data-ttu-id="bd3e5-138">**قبول الحركة دائماً** - قبول الحركة، بغض النظر عن نتائج التحقق من صحة العنوان.</span><span class="sxs-lookup"><span data-stu-id="bd3e5-138">**Always accept transaction** – Accept the transaction, regardless of address verification results.</span></span>
-   <span data-ttu-id="bd3e5-139">**حامل الحساب** – مقارنة اسم حامل البطاقة من الحركة بمعلومات شركة بطاقة الائتمان.</span><span class="sxs-lookup"><span data-stu-id="bd3e5-139">**Account holder** – Compare the cardholder's name from the transaction with the credit card company’s information.</span></span>
-   <span data-ttu-id="bd3e5-140">**عنوان الفوترة** – مقارنة اسم حامل البطاقة وعنوان الفوترة الخاص به من الحركة المشتملة على معلومات شركة بطاقة الائتمان.</span><span class="sxs-lookup"><span data-stu-id="bd3e5-140">**Billing address** – Compare the cardholder's name and billing address from the transaction with the credit card company’s information.</span></span>
-   <span data-ttu-id="bd3e5-141">**الرمز البريدي للفاتورة‬** – مقارنة اسم حامل البطاقة، وعنوان الفوترة، والرمز البريدي من الحركة المشتملة على معلومات شركة بطاقة الائتمان.</span><span class="sxs-lookup"><span data-stu-id="bd3e5-141">**Billing postal code** – Compare the cardholder's name, billing address, and postal code from the transaction with the credit card company’s information.</span></span>

## <a name="data-support"></a><span data-ttu-id="bd3e5-142">دعم البيانات</span><span class="sxs-lookup"><span data-stu-id="bd3e5-142">Data support</span></span>
<span data-ttu-id="bd3e5-143">بالنسبة إلى كل نوع بطاقة ائتمان مدعوم، يمكنك تحديد مستوى دعم البيانات.</span><span class="sxs-lookup"><span data-stu-id="bd3e5-143">For each credit card type that is supported, you can specify the level of data support.</span></span> <span data-ttu-id="bd3e5-144">ويتحكم المستوى في كم المعلومات المتعلقة بحركة ويتم تحويلها إلى خدمة الدفع.</span><span class="sxs-lookup"><span data-stu-id="bd3e5-144">The level controls how much information about a transaction is transferred to the payment service.</span></span> <span data-ttu-id="bd3e5-145">وتأكد من مراجعة الموفر الخاص بك لتحديد ما إذا كان يمكن أن يوفر هذه المعلومات.</span><span class="sxs-lookup"><span data-stu-id="bd3e5-145">Be sure to check with your provider to determine whether it can provide this information.</span></span> <span data-ttu-id="bd3e5-146">فيما يلي خيارات لمستوى دعم البيانات:</span><span class="sxs-lookup"><span data-stu-id="bd3e5-146">Here are the options for the level of data support:</span></span>
-   <span data-ttu-id="bd3e5-147">**المستوى 1** – نقل تاريخ الحركة، ومبلغ الحركة، والوصف.</span><span class="sxs-lookup"><span data-stu-id="bd3e5-147">**Level 1** – Transfer the transaction date, transaction amount, and description.</span></span>
-   <span data-ttu-id="bd3e5-148">**المستوى 2** – نقل المعلومات من المستوى 1، بالإضافة إلى عناوين الشحن والتاجر، والمعلومات الضريبية.</span><span class="sxs-lookup"><span data-stu-id="bd3e5-148">**Level 2** – Transfer all Level 1 information, plus the shipping and merchant addresses, and tax information.</span></span>
-   <span data-ttu-id="bd3e5-149">**المستوى 3** – نقل جميع معلومات المستوى 2، بالإضافة إلى معلومات بند الأمر.</span><span class="sxs-lookup"><span data-stu-id="bd3e5-149">**Level 3** – Transfer all Level 2 information, plus order line information.</span></span>

## <a name="partial-payments"></a><span data-ttu-id="bd3e5-150">المدفوعات الجزئية</span><span class="sxs-lookup"><span data-stu-id="bd3e5-150">Partial payments</span></span>
<span data-ttu-id="bd3e5-151">‏‫إذا قمت بشحن جزء من أمر، يتم تسجيل مبلغ الأمر الجزئي، ويتم إغلاق التفويض، الذي توفر لمبلغ الأمر بالكامل،</span><span class="sxs-lookup"><span data-stu-id="bd3e5-151">If you ship part of an order, the amount of the partial order is captured, and the authorization, which was for the amount of the whole order, is closed.</span></span> <span data-ttu-id="bd3e5-152">ويتم فيما بعد إرسال تفويض جديد للمبلغ المتبقي من الأمر الذي لم يتم شحنه.‬</span><span class="sxs-lookup"><span data-stu-id="bd3e5-152">A new authorization is then submitted for the remaining amount of the order that hasn't been shipped.</span></span>

## <a name="voiding-an-authorization"></a><span data-ttu-id="bd3e5-153">إلغاء تفويض </span><span class="sxs-lookup"><span data-stu-id="bd3e5-153">Voiding an authorization</span></span>
<span data-ttu-id="bd3e5-154">لإلغاء تفويض بطاقة الائتمان، يمكنك تغيير طريقة الدفع لطريقة أخرى لا تحتوي على نوع بطاقة الائتمان.</span><span class="sxs-lookup"><span data-stu-id="bd3e5-154">To void a credit card authorization, you can change the method of payment to another method that doesn't have a type of Credit card.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]