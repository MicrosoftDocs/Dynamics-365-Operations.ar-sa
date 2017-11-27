---
title: "الخصومات النقدية"
description: "يتم إعداد الخصومات النقدية وتتم مشاركتها لكل من الحسابات الدائنة والحسابات المدينة.  يمكن تعريف الخصم النقدي المتوفر على فاتورة العميل أو فاتورة المورّد، وسيتم أخذه إذا تم دفع الفاتورة في غضون تاريخ الخصم النقدي."
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3741
ms.assetid: c25f9d85-2702-46aa-8e61-0b4886e069b3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 9960af8c4961a42e7e829077da40bcbbf3bc71c2
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="cash-discounts"></a><span data-ttu-id="79f24-104">الخصومات النقدية</span><span class="sxs-lookup"><span data-stu-id="79f24-104">Cash discounts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="79f24-105">يتم إعداد الخصومات النقدية وتتم مشاركتها لكل من الحسابات الدائنة والحسابات المدينة.</span><span class="sxs-lookup"><span data-stu-id="79f24-105">Cash discounts are setup and shared for Accounts payable and Accounts receivable.</span></span>  <span data-ttu-id="79f24-106">يمكن تعريف الخصم النقدي المتوفر على فاتورة العميل أو فاتورة المورّد، وسيتم أخذه إذا تم دفع الفاتورة في غضون تاريخ الخصم النقدي.</span><span class="sxs-lookup"><span data-stu-id="79f24-106">The cash discount available can be defined on the customer invoice or vendor invoice, and will be taken if the invoice is paid within the cash discount date.</span></span> 

<a name="cash-discounts"></a><span data-ttu-id="79f24-107">الخصومات النقدية</span><span class="sxs-lookup"><span data-stu-id="79f24-107">Cash discounts</span></span>
--------------

<span data-ttu-id="79f24-108">يمكن إنشاء الخصومات النقدية للموردين أو العملاء في صفحة الخصومات النقدية.</span><span class="sxs-lookup"><span data-stu-id="79f24-108">Cash discounts for both customers or vendors can be created in the Cash discounts page.</span></span> <span data-ttu-id="79f24-109">ويمكنك أيضًا تحديد، باستخدام حقل كود الخصم التالي، سلسلة من الخصومات النقدية التي تلي بعضها البعض عند انتهاء تاريخ صلاحية تواريخ الخصم النقدي السابقة.</span><span class="sxs-lookup"><span data-stu-id="79f24-109">You can also define, by using the Next discount code field, a series of cash discounts that succeed each other as previous cash discount dates expire.</span></span> <span data-ttu-id="79f24-110">ولمزيد من المعلومات، راجع "مثال: سلسلة من الخصومات النقدية" لاحقاً في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="79f24-110">For more information, see “Example: Series of cash discounts” later in this topic.</span></span> <span data-ttu-id="79f24-111">وإذا تم إدخال الفاتورة أو حركة الدائن (دفع أو إشعار دائن) أو كليهما بعملة خلاف عملة المحاسبة للكيان القانوني، فإنه يتم حساب الخصم النقدي باستخدام سعر الصرف استناداً إلى تاريخ الدفع أو الإشعار الدائن.</span><span class="sxs-lookup"><span data-stu-id="79f24-111">If the invoice, credit transaction (either a payment or a credit note), or both are entered in a currency other than the accounting currency of the legal entity, the cash discount is calculated using the exchange rate based on the date of the payment or credit note.</span></span> <span data-ttu-id="79f24-112">وإذا تم إدخال مستند الفاتورة والائتمان في كيانات قانونية مختلفة، وفي حالة اختلاف عملات المحاسبة للكيانات القانونية، فإنه يتم أخذ سعر الصرف من الكيان القانوني الخاص بالفاتورة، اعتبارًا من تاريخ مستند الائتمان.</span><span class="sxs-lookup"><span data-stu-id="79f24-112">If the invoice and credit document are entered in different legal entities, and if the accounting currencies for the legal entities differ, the exchange rate is taken from the legal entity of the invoice, as of the date of the credit document.</span></span> <span data-ttu-id="79f24-113">ولمزيد من المعلومات، راجع "مثال: أسعار الصرف للخصومات النقدية" لاحقاً في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="79f24-113">For more information, see “Example: Exchange rates for cash discounts” later in this topic.</span></span>
<span data-ttu-id="79f24-114">أمر التعيين الافتراضي لحساب الخصم النقدي الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="79f24-114">Defaulting order of cash discount main account</span></span>
----------------------------------------------

<span data-ttu-id="79f24-115">إذا تمت تسوية فاتورة في موعدها للحصول على خصم نقدي، يتم ترحيل الخصم النقدي تلقائيًا إلى الحساب الرئيسي للخصم النقدي وفقًا لأولويات التعيين الافتراضي التالية:</span><span class="sxs-lookup"><span data-stu-id="79f24-115">If an invoice is settled in time to obtain a cash discount, the cash discount is automatically posted to a cash discount main account according to the following defaulting priority:</span></span>
1.  <span data-ttu-id="79f24-116">الحساب الرئيسي المحدد في حقل حساب الخصم النقدي البديل في صفحة تسوية الحركات المفتوحة للعميل أو صفحة تسوية الحركات المفتوحة للمورد.</span><span class="sxs-lookup"><span data-stu-id="79f24-116">The main account specified in the Alternative cash discount account field on the customer Settle open transactions page or the vendor Settle open transactions page.</span></span>
2.  <span data-ttu-id="79f24-117">الحساب الرئيسي المحدد في حقل الخصم النقدي للعميل أو حقل الخصم النقدي للمورد في مجموعة ترحيل دفتر الأستاذ التي تم تعيينها إلى كود ضريبة المبيعات في الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="79f24-117">The main account specified in the Customer cash discount field or the Vendor cash discount field of the ledger posting group that is assigned to the sales tax code of the invoice.</span></span> <span data-ttu-id="79f24-118">قم بإعداد مجموعات ترحيل دفتر الأستاذ في صفحة مجموعات ترحيل دفتر الأستاذ وتعيين أكواد ضريبة المبيعات في صفحة أكواد ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="79f24-118">Set up ledger posting groups on the Ledger posting groups page and assign them to sales tax codes in the Sales tax codes page.</span></span>
3.  <span data-ttu-id="79f24-119">حساب الترحيل الرئيسي في صفحة الخصومات النقدية في حقل الحساب الرئيسي لخصومات العميل أو حقل الحساب الرئيسي لخصومات الموردين لكود الخصم النقدي الموجود في الفاتورة التي تمت تسويتها.</span><span class="sxs-lookup"><span data-stu-id="79f24-119">The main posting account on the Cash discounts page in either the Main account for customer discounts field or the Main account for vendor discounts field for the cash discount code that is on the settled invoice.</span></span>
4.  <span data-ttu-id="79f24-120">الحساب الرئيسي للخصومات النقدية، كما هو محدد في صفحة حسابات الحركات التلقائية.</span><span class="sxs-lookup"><span data-stu-id="79f24-120">The main account for cash discounts, as defined in the Accounts for automatic transactions page.</span></span>

## <a name="example-series-of-cash-discounts"></a><span data-ttu-id="79f24-121"> مثال: سلسلة الخصومات النقدية</span><span class="sxs-lookup"><span data-stu-id="79f24-121">Example: Series of cash discounts</span></span>
<span data-ttu-id="79f24-122">قم بإعداد ثلاثة أكواد خصومات نقدية كالتالي:</span><span class="sxs-lookup"><span data-stu-id="79f24-122">Set up three cash discount codes as follows:</span></span>
-   <span data-ttu-id="79f24-123">كود 5D10% - خصم نقدي قيمته 10% عند سداد المبلغ خلال 5 أيام.</span><span class="sxs-lookup"><span data-stu-id="79f24-123">Code 5D10% – A cash discount of 10% when the amount is paid within 5 days.</span></span>
-   <span data-ttu-id="79f24-124">كود 10D5% - خصم نقدي قيمته 5% عند سداد المبلغ خلال 10 أيام.</span><span class="sxs-lookup"><span data-stu-id="79f24-124">Code 10D5% – A cash discount of 5% when the amount is paid within 10 days.</span></span>
-   <span data-ttu-id="79f24-125">كود 14D2% - خصم نقدي قيمته 2% عند سداد المبلغ خلال 14 أيام.</span><span class="sxs-lookup"><span data-stu-id="79f24-125">Code 14D2% – A cash discount of 2% when the amount is paid within 14 days.</span></span>

<span data-ttu-id="79f24-126">في حقل كود الخصم التالي:</span><span class="sxs-lookup"><span data-stu-id="79f24-126">In the Next discount code field:</span></span>
-   <span data-ttu-id="79f24-127">للكود 5D10%، اختر 10D5%.</span><span class="sxs-lookup"><span data-stu-id="79f24-127">For the 5D10% code, select 10D5%.</span></span>
-   <span data-ttu-id="79f24-128">للكود 10D5%، اختر 14D2%.</span><span class="sxs-lookup"><span data-stu-id="79f24-128">For the 10D5% code, select 14D2%.</span></span>
-   <span data-ttu-id="79f24-129">للحصول على كود 14D2%، اترك حقل كود الخصم التالي فارغًا.</span><span class="sxs-lookup"><span data-stu-id="79f24-129">For the 14D2% code, leave the Next discount code field blank.</span></span>

<span data-ttu-id="79f24-130">تلي الخصومات النقدية الثلاثة بعضها البعض عندما يتجاوز تاريخ الدفع السابق تاريخ الخصم النقدي في الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="79f24-130">The three cash discounts succeed each other as the payment date exceeds the previous cash discount date on the invoice.</span></span> <span data-ttu-id="79f24-131">ويتم منح خصم نقدي واحد فقط عند دفع الفاتورة، استناداً إلى تاريخ الخصم النقدي الذي تتم تلبيته في تسلسل الخصومات النقدية.</span><span class="sxs-lookup"><span data-stu-id="79f24-131">Only one cash discount is granted when the invoice is paid, based on which cash discount date is meet in the sequence of cash discounts.</span></span>

## <a name="example-exchange-rates-for-cash-discounts"></a><span data-ttu-id="79f24-132"> مثال: أسعار الصرف للخصومات النقدية</span><span class="sxs-lookup"><span data-stu-id="79f24-132">Example: Exchange rates for cash discounts</span></span>
<span data-ttu-id="79f24-133">عملة المحاسبة للكيان القانوني هو اليورو وأسعار الصرف التالية محددة للدولار الأمريكي:</span><span class="sxs-lookup"><span data-stu-id="79f24-133">Your legal entity’s accounting currency is EUR and the following exchange rates are specified for USD:</span></span>
-   <span data-ttu-id="79f24-134">1 فبراير = 110</span><span class="sxs-lookup"><span data-stu-id="79f24-134">February 1 = 110</span></span>
-   <span data-ttu-id="79f24-135">1 مارس = 80</span><span class="sxs-lookup"><span data-stu-id="79f24-135">March 1 = 80</span></span>

<span data-ttu-id="79f24-136">‏‫يتم ترحيل فاتورة بمبلغ 1000 دولار أمريكي بشروط خصم نقدي 20D2% في 15 شباط/فبراير.</span><span class="sxs-lookup"><span data-stu-id="79f24-136">An invoice for 1000 USD with cash discount terms of 20D2% is posted on February 15.</span></span> <span data-ttu-id="79f24-137">ومبلغ عملة المحاسبة للفاتورة يبلغ 1100 يورو.‬</span><span class="sxs-lookup"><span data-stu-id="79f24-137">The accounting currency amount of the invoice is 1100 EUR.</span></span> <span data-ttu-id="79f24-138">تتم تسوية دفعة بمبلغ 980 دولاراً بالفاتورة في 1 مارس.</span><span class="sxs-lookup"><span data-stu-id="79f24-138">A payment for 980 USD is settled with the invoice on March 1.</span></span> <span data-ttu-id="79f24-139">ومبلغ الخصم النقدي يساوي 20 دولاراً أمريكياً.‬</span><span class="sxs-lookup"><span data-stu-id="79f24-139">The cash discount amount is 20 USD.</span></span> <span data-ttu-id="79f24-140">مبلغ عملة المحاسبة للدفع هو 784 يورو.</span><span class="sxs-lookup"><span data-stu-id="79f24-140">The accounting currency amount of the payment is 784 EUR.</span></span> <span data-ttu-id="79f24-141">يتم حساب مبلغ عملة المحاسبة للخصم النقدي باستخدام سعر الصرف اعتبارًا من 1 آذار/مارس: 20 \* 80‏ / 100 = 16 يورو.</span><span class="sxs-lookup"><span data-stu-id="79f24-141">The accounting currency amount of the cash discount is calculated by using the exchange rate as of March 1: 20 \* 80 / 100 = 16 EUR.</span></span>
| <span data-ttu-id="79f24-142">**ملاحظة**</span><span class="sxs-lookup"><span data-stu-id="79f24-142">**Note**</span></span>                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79f24-143">إذا تم تحديد خيار حساب الخصومات النقدية للمدفوعات الجزئية في صفحتي معلمات الحسابات المدينة أو معلمات الحسابات الدائنة، فإنه يتم استخدام سعر الصرف المعمول به في تاريخ استخدام كل دفعة جزئية.</span><span class="sxs-lookup"><span data-stu-id="79f24-143">If the Calculate cash discounts for partial payments option is selected in the Accounts receivable parameters or Accounts payable parameters pages, the exchange rate that is in effect on the date of each partial payment is used.</span></span> |

 
=

 




