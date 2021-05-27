---
title: مدفوعات العميل
description: يوضح هذا الموضوع كيفية إعداد الدفعات المقدمة للعملاء ومعالجتها (والتي تعرف أيضًا بعمليات إيداع العملاء).
author: roschlom
ms.date: 04/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, LedgerJournalTransCustPaym, CustParameters
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3314803b994aed40e5b04d8546a45bd305d48b6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019410"
---
# <a name="customer-prepayments"></a><span data-ttu-id="91e0c-103">مدفوعات العميل</span><span class="sxs-lookup"><span data-stu-id="91e0c-103">Customer prepayments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="91e0c-104">يتم استخدام الدفعات المقدمة للعميل عند استلام الدفع من أحد العملاء، ولكن لا توجد فاتورة يمكن تسوية عملية الدفع على أساسها.</span><span class="sxs-lookup"><span data-stu-id="91e0c-104">Customer prepayments are used when you receive a payment from a customer, but there is no invoice that the payment can be settled against.</span></span> <span data-ttu-id="91e0c-105">يشار إلى أنواع الدفع هذه أيضًا باسم عمليات إيداع العملاء.</span><span class="sxs-lookup"><span data-stu-id="91e0c-105">These types of payments are also referred to as customer deposits.</span></span>

<span data-ttu-id="91e0c-106">وتتكون عملية إعداد الدفعات المقدمة للعميل والعمل معها من الخطوات الأساسية التالية.</span><span class="sxs-lookup"><span data-stu-id="91e0c-106">The process of setting up and working with customer prepayments consists of the following basic steps.</span></span>

1. <span data-ttu-id="91e0c-107">قم بإنشاء ملف تعريف ترحيل خاص بالعميل للدفعات المقدمة.</span><span class="sxs-lookup"><span data-stu-id="91e0c-107">Create a customer posting profile for prepayments.</span></span>
2. <span data-ttu-id="91e0c-108">قم بإعداد المعلمة **ملف تعريف الترحيل مع إيصال يومية الدفعات المقدمة**.</span><span class="sxs-lookup"><span data-stu-id="91e0c-108">Set the **Posting profile with prepayment journal voucher** parameter.</span></span>
3. <span data-ttu-id="91e0c-109">قم بإنشاء دفتر يومية مدفوعات العميل، ثم حدد خانة الاختيار **إيصال دفتر يومية الدفعات المقدمة** في كل بند.</span><span class="sxs-lookup"><span data-stu-id="91e0c-109">Create a customer payment journal, and select the **Prepayment journal voucher** check box on each line.</span></span>
4. <span data-ttu-id="91e0c-110">ترحيل دفتر يومية دفع العميل.</span><span class="sxs-lookup"><span data-stu-id="91e0c-110">Post the customer payment journal.</span></span>
5. <span data-ttu-id="91e0c-111">بعد إنشاء الفاتورة، قم بتسوية الدفعة المقدمة معها باستخدام الصفحة **تسوية حركات مفتوحة**.</span><span class="sxs-lookup"><span data-stu-id="91e0c-111">After an invoice is generated, settle the prepayment with it by using the **Settle open transactions** page.</span></span>

## <a name="create-a-customer-posting-profile-for-prepayments"></a><span data-ttu-id="91e0c-112">قم بإنشاء ملف تعريف ترحيل خاص بالعميل للدفعات المقدمة</span><span class="sxs-lookup"><span data-stu-id="91e0c-112">Create a customer posting profile for prepayments</span></span>

<span data-ttu-id="91e0c-113">عادة، عند قبول الدفعات المقدمة أو الإيداعات من العملاء قبل تسليم البضائع أو الخدمات، أو قبل وجود فاتورة في النظام لديك، ستحتاج إلى تسجيل النقدية كالتزام بدلاً من أصل في مخطط الحسابات.</span><span class="sxs-lookup"><span data-stu-id="91e0c-113">Typically, when you accept prepayments or deposits from your customers before goods or services are delivered, or before an invoice exists in your system, you will want to record the cash as a liability instead of an asset in your chart of accounts.</span></span> <span data-ttu-id="91e0c-114">ومع ذلك، قد تختلف متطلبات تسجيل هذه المبالغ في دفتر الأستاذ العام، وذلك وفقًا لبلدك أو منطقتك.</span><span class="sxs-lookup"><span data-stu-id="91e0c-114">However, the requirements for recording these amounts in your general ledger might differ, depending on your country or region.</span></span> <span data-ttu-id="91e0c-115">لذلك، تأكد من استشارة المحاسبين حول أية لوائح محلية تنطبق عليها.</span><span class="sxs-lookup"><span data-stu-id="91e0c-115">Therefore, be sure to consult your accountants about any local regulations that apply.</span></span>

<span data-ttu-id="91e0c-116">وبصفة عامة، فإن عملية إنشاء ملف تعريف ترحيل يمكن استخدامها للدفعات المقدمة هي نفس عملية إنشاء ملفات تعريف ترحيل أخرى.</span><span class="sxs-lookup"><span data-stu-id="91e0c-116">In general, the process for creating a posting profile that can be used for prepayments is the same as the process for creating other posting profiles.</span></span> <span data-ttu-id="91e0c-117">الفرق الأساسي هو الحساب الرئيسي الذي تحدده في الحقل **حساب الملخص**.</span><span class="sxs-lookup"><span data-stu-id="91e0c-117">The primary difference is the main account that you select in the **Summary account** field.</span></span> <span data-ttu-id="91e0c-118">لمزيد من المعلومات، راجع [ملفات تعريف ترحيل العميل](customer-posting-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="91e0c-118">For more information, see [Customer posting profiles](customer-posting-profiles.md).</span></span>

## <a name="define-parameters-for-customer-prepayments"></a><span data-ttu-id="91e0c-119">تحديد المعلمات للدفعات المقدمة للعميل</span><span class="sxs-lookup"><span data-stu-id="91e0c-119">Define parameters for customer prepayments</span></span>

<span data-ttu-id="91e0c-120">توجد معلمتان للحسابات المدينة الرئيسية والتي يجب وضعها في الاعتبار عند تكوين النظام للدفعات المقدمة للعميل.</span><span class="sxs-lookup"><span data-stu-id="91e0c-120">There are two main Accounts receivable parameters that you must consider when you configure the system for customer prepayments.</span></span> <span data-ttu-id="91e0c-121">اتبع هذه الخطوات لتكوين المعلمات.</span><span class="sxs-lookup"><span data-stu-id="91e0c-121">Follow these steps to configure the parameters.</span></span>

1. <span data-ttu-id="91e0c-122">انتقل إلى **الحسابات المدينة \> إعداد \> معلمات الحسابات المدينة**.</span><span class="sxs-lookup"><span data-stu-id="91e0c-122">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="91e0c-123">اختياري: في علامة التبويب **دفتر الأستاذ وضريبة المبيعات**، على علامة التبويب السريعة **الدفع**، قم بتعيين الخيار **ضريبة المبيعات على إيصال يومية دفعات مقدمة** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="91e0c-123">Optional: On the **Ledger and sales tax** tab, on the **Payment** FastTab, set the **Sales tax on prepayment journal voucher** option to **Yes**.</span></span>
3. <span data-ttu-id="91e0c-124">في الحق **ملف تعريف الترحيل مع إيصال يومية دفعات مقدمة**، حدد ملف تعريف ترحيل العميل المراد استخدامه عند ترحيل الدفعات المقدمة للعميل.</span><span class="sxs-lookup"><span data-stu-id="91e0c-124">In the **Posting profile with prepayment journal voucher** field, select the customer posting profile to use when customer prepayments are posted.</span></span>
4. <span data-ttu-id="91e0c-125">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="91e0c-125">Close the page.</span></span>

## <a name="create-customer-prepayment-vouchers"></a><span data-ttu-id="91e0c-126">إنشاء إيصالات الدفعات المقدمة للعميل</span><span class="sxs-lookup"><span data-stu-id="91e0c-126">Create customer prepayment vouchers</span></span>

<span data-ttu-id="91e0c-127">عندما تقوم بإنشاء دفتر يومية المدفوعات للعميل، لكل دفعة، فإنه يجب عليك تعيين الخيار **إيصال يومية دفعات مقدم** إلى **نعم** في الصفحة **دفتر يومية المدفوعات للعميل**.</span><span class="sxs-lookup"><span data-stu-id="91e0c-127">When you create the customer payment journal, for every prepayment, you must set the **Prepayment journal voucher** option to **Yes** on the **Customer payment journal** page.</span></span> <span data-ttu-id="91e0c-128">لإنشاء دفع مقدم للعميل، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="91e0c-128">Follow these steps to create a customer prepayment.</span></span>

1. <span data-ttu-id="91e0c-129">انتقل إلى **الحسابات المدينة \> المدفوعات \> دفتر يومية المدفوعات للعميل**.</span><span class="sxs-lookup"><span data-stu-id="91e0c-129">Go to **Accounts receivable \> Payments \> Customer payment journal**.</span></span>
2. <span data-ttu-id="91e0c-130">حدد **جديد** لإنشاء دفتر يومية.</span><span class="sxs-lookup"><span data-stu-id="91e0c-130">Select **New** to create a journal.</span></span>
3. <span data-ttu-id="91e0c-131">حدد اسم دفتر اليومية في الحقل **الاسم** ليتم استخدامه.</span><span class="sxs-lookup"><span data-stu-id="91e0c-131">In the **Name** field, select the journal name to use.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="91e0c-132">إذا قمت بتعيين الخيار **ضريبة المبيعات على إيصال يومية دفعات مقدمة** إلى **نعم** في الإجراء السابق، فإنه يجب تحديد اسم دفتر اليومية حيث يتم تحديد المعلمة **المبلغ يتضمن ضريبة المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="91e0c-132">If you set the **Sales tax on prepayment journal voucher** option to **Yes** in the previous procedure, you must select a journal name where the **Amount includes sales tax** parameter is selected.</span></span> 

4. <span data-ttu-id="91e0c-133">اختياري: في الحقل **الوصف**، أدخل وصفًا مفصلاً.</span><span class="sxs-lookup"><span data-stu-id="91e0c-133">Optional: In the **Description** field, enter a detailed description.</span></span>
5. <span data-ttu-id="91e0c-134">حدد **البنود**.</span><span class="sxs-lookup"><span data-stu-id="91e0c-134">Select **Lines**.</span></span>
6. <span data-ttu-id="91e0c-135">في حالة عدم وجود بند فارغ، حدد **جديد** لإنشاء بند.</span><span class="sxs-lookup"><span data-stu-id="91e0c-135">If a blank line doesn't exist, select **New** to create a line.</span></span>
7. <span data-ttu-id="91e0c-136">في الحقل **التاريخ**، أدخل التاريخ الذي ينبغي فيه ترحيل الدفعة المقدمة.</span><span class="sxs-lookup"><span data-stu-id="91e0c-136">In the **Date** field, enter the date when the prepayment should be posted.</span></span>
8. <span data-ttu-id="91e0c-137">في الحقل **الحساب**، حدد العميل للدفعة المقدمة.</span><span class="sxs-lookup"><span data-stu-id="91e0c-137">In the **Account** field, select the customer for the prepayment.</span></span>
9. <span data-ttu-id="91e0c-138">اختياري: في الحقل **الوصف**، أدخل وصفًا مفصلاً للحركة.</span><span class="sxs-lookup"><span data-stu-id="91e0c-138">Optional: In the **Description** field, enter a detailed description of the transaction.</span></span>
10. <span data-ttu-id="91e0c-139">في الحقل **الائتمان**، أدخل مبلغ الدفعة المقدمة.</span><span class="sxs-lookup"><span data-stu-id="91e0c-139">In the **Credit** field, enter the amount of the prepayment.</span></span>
11. <span data-ttu-id="91e0c-140">في الحقل **الحساب المقابل**، حدد الحساب الذي سيتم دفع الحساب المقابل له.</span><span class="sxs-lookup"><span data-stu-id="91e0c-140">In the **Offset account** field, select the account to offset the payment to.</span></span> <span data-ttu-id="91e0c-141">على سبيل المثال، حدد البنك أو الحساب الرئيسي لترحيل الدفع إليه.</span><span class="sxs-lookup"><span data-stu-id="91e0c-141">For example, select the bank or main account to post the payment to.</span></span>
12. <span data-ttu-id="91e0c-142">في الحقل **طريقة الدفع**، حدد طريقة الدفع الخاصة بالعميل.</span><span class="sxs-lookup"><span data-stu-id="91e0c-142">In the **Method of payment** field, select the customer's method of payment.</span></span>
13. <span data-ttu-id="91e0c-143">من علامات التبويب **المدفوعات**، قم بتعيين الخيار **إيصال يومية الدفعات المقدمة**  إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="91e0c-143">On the **Payment** tab, set the **Prepayment journal voucher** option to **Yes**.</span></span>
14. <span data-ttu-id="91e0c-144">كرر الخطوات من 7 إلى 13 لكل دفعة مقدمة إضافية يجب ترحيلها.</span><span class="sxs-lookup"><span data-stu-id="91e0c-144">Repeat steps 7 through 13 for each additional prepayment that must be posted.</span></span>
15. <span data-ttu-id="91e0c-145">حدد **ترحيل** لترحيل دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="91e0c-145">Select **Post** to finalize the journal.</span></span>

## <a name="settle-prepayments-with-invoices"></a><span data-ttu-id="91e0c-146">تسوية الدفعات المقدمة بالفواتير</span><span class="sxs-lookup"><span data-stu-id="91e0c-146">Settle prepayments with invoices</span></span>

<span data-ttu-id="91e0c-147">يمكنك استخدام مساحة عمل **مدفوعات العميل** للعثور على المدفوعات التي لم تتم تسويتها بالكامل وتسويتها.</span><span class="sxs-lookup"><span data-stu-id="91e0c-147">You can use the **Customer payments** workspace to easily find and settle payments that haven't been fully settled.</span></span>

1. <span data-ttu-id="91e0c-148">في لوحة معلومات **الصفحة الرئيسية**، حدد لوحة **مدفوعات العميل**.</span><span class="sxs-lookup"><span data-stu-id="91e0c-148">On the **Home** dashboard, select the **Customer payments** tile.</span></span>
2. <span data-ttu-id="91e0c-149">في القسم **حركات العميل**، في علامة التبويب **لم تتم تسوية المدفوعات** ، ابحث عن الدفعة وحددها لتسويتها.</span><span class="sxs-lookup"><span data-stu-id="91e0c-149">In the **Customer transactions** section, on the **Payments not settled** tab, search for and select the payment to settle.</span></span>
3. <span data-ttu-id="91e0c-150">حدد **حركات التسوية**.</span><span class="sxs-lookup"><span data-stu-id="91e0c-150">Select **Settle transactions**.</span></span>
4. <span data-ttu-id="91e0c-151">حدد خانة الاختيار **وضع علامة** للفاتورة والدفع الذي ستتم تسويته.</span><span class="sxs-lookup"><span data-stu-id="91e0c-151">Select the **Mark** check box for the invoice and the payment that will be settled.</span></span>
5. <span data-ttu-id="91e0c-152">حدد **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="91e0c-152">Select **Post**.</span></span>

<span data-ttu-id="91e0c-153">لمزيد من المعلومات حول كيفية تسوية الحركات المفتوحة، راجع [نظرة عامة حول التسوية](/cash-bank-management/settlement-overview.md).</span><span class="sxs-lookup"><span data-stu-id="91e0c-153">For more information about how to settle open transactions, see [Settlement overview](/cash-bank-management/settlement-overview.md).</span></span>
