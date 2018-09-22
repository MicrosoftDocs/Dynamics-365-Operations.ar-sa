--- 
title: "إنشاء الفواتير ذات النص الحر‬"
description: "يشرح هذا الموضوع كيفية إنشاء الفواتير ذات النص الحر‬."
author: mikefalkner
manager: AnnBe
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: f64292a1b3726ea9b43f959a44c4ed2a1f392484
ms.openlocfilehash: f6ee6fda0b52b8af7c253b7d22e470345a8a421f
ms.contentlocale: ar-sa
ms.lasthandoff: 09/05/2018

---

# <a name="create-free-text-invoices"></a><span data-ttu-id="8a4fd-103">إنشاء الفواتير ذات النص الحر‬</span><span class="sxs-lookup"><span data-stu-id="8a4fd-103">Create free text invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8a4fd-104">يشرح هذا الموضوع كيفية إنشاء الفواتير ذات النص الحر‬.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-104">This topic explains how to create free text invoices.</span></span> <span data-ttu-id="8a4fd-105">بالنسبة إلى هذا الإجراء، استخدم شركة بيانات العرض التوضيحي **USMF**.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-105">For the procedure, use the **USMF** demo company.</span></span>

## <a name="create-a-free-text-invoice"></a><span data-ttu-id="8a4fd-106">إنشاء فاتورة نص حر</span><span class="sxs-lookup"><span data-stu-id="8a4fd-106">Create a free text invoice</span></span>

1. <span data-ttu-id="8a4fd-107">انتقل إلى **الحسابات المدينة \> الفواتير \> جميع الفواتير ذات نص حر‬**.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-107">Go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>
2. <span data-ttu-id="8a4fd-108">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-108">Select **New**.</span></span>
3. <span data-ttu-id="8a4fd-109">في الحقل **حساب العميل**، حدد قيمة.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-109">In the **Customer account** field, select a value.</span></span>

    * <span data-ttu-id="8a4fd-110">بشكل افتراضي، يُستخدم الحساب المحدد على أنه حساب العميل كحساب فاتورة.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-110">By default, the account that is selected as the customer account is used as the invoice account.</span></span>
    * <span data-ttu-id="8a4fd-111">إذا لم يتم ترحيل الفاتورة، فستبدأ حالة المحاسبة مع **قيد التنفيذ‬**.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-111">If the invoice isn't posted, the accounting status starts with **In process**.</span></span>
    * <span data-ttu-id="8a4fd-112">سوف يتم تعيين رقم الفاتورة عند ترحيل الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-112">The invoice number will be assigned when the invoice is posted.</span></span>
    * <span data-ttu-id="8a4fd-113">إذا كنت تستخدم تفويضات منطقة التداول باليورو (SEPA) فسيتم إدخال تفويض الخصم المباشر‬ تلقائيًا عند تحديد حساب العميل.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-113">If you're using Single Euro Payments Area (SEPA) mandates, the direct debit mandate is automatically entered when you select the customer account.</span></span>

4. <span data-ttu-id="8a4fd-114">في حقل **الوصف**، أدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-114">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="8a4fd-115">في الحقل **الحساب الرئيسي**، حدد رقم حساب من دون أبعاد.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-115">In the **Main account** field, specify an account number that doesn't have dimensions.</span></span> <span data-ttu-id="8a4fd-116">سوف تقوم بإدخال الأبعاد لاحقًا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-116">You will enter dimensions later in this topic.</span></span>

    <span data-ttu-id="8a4fd-117">يمكنك أيضًا إدخال حرف واحد أو أكثر للحساب الرئيسي، واستخدام خاصية البحث للعثور على الحساب.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-117">You can also enter one or more characters for the main account, and use the lookup to find the account.</span></span>

6. <span data-ttu-id="8a4fd-118">حدد علامة التبويب السريعة **تفاصيل البند** لإضافة الأبعاد إلى الحساب الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-118">Select the **Line details** FastTab to add dimensions to the main account.</span></span>
7. <span data-ttu-id="8a4fd-119">حدد علامة تبويب **بند الأبعاد المالية**.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-119">Select the **Financial dimensions line** tab.</span></span>

    * <span data-ttu-id="8a4fd-120">تتعلق الأبعاد بالبند المحدد فقط.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-120">The dimensions are for the selected line only.</span></span>
    * <span data-ttu-id="8a4fd-121">يتم ملء مجموعة ضريبة المبيعات من العميل.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-121">The sales tax group is filled in from the customer.</span></span> <span data-ttu-id="8a4fd-122">إذا لم يكن لدى العميل مجموعة ضريبة مبيعات، فسوف تستخدم مجموعة ضريبة المبيعات من الحساب الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-122">If the customer doesn't have a sales tax group, the sales tax group from the main account is used.</span></span>
    * <span data-ttu-id="8a4fd-123">يتم ملء مجموعة ضريبة مبيعات الأصناف من الحساب الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-123">The items sales tax group is filled in from the main account.</span></span> <span data-ttu-id="8a4fd-124">إذا لم يتوافر للحساب الرئيسي مجموعة ضريبة مبيعات أصناف، فسيتم استخدام مجموعة ضريبة مبيعات الأصناف المحددة في معلمات ضريبة المبيعات في دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-124">If the main account doesn't have an item sales tax group, the item sales tax group that is specified in the sales tax parameters in General ledger is used.</span></span>

8. <span data-ttu-id="8a4fd-125">اختياري: في حقل **الكمية**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-125">Optional: In the **Quantity** field, enter a number.</span></span>
9. <span data-ttu-id="8a4fd-126">اختياري: في حقل **سعر الوحدة**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-126">Optional: In the **Unit price** field, enter a number.</span></span>

    <span data-ttu-id="8a4fd-127">يتم حساب المبلغ بضرب الكميات في سعر الوحدة.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-127">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="8a4fd-128">ومع ذلك، يمكنك تجاوز هذا الحساب من خلال إدخال مبلغ.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-128">However, you can override that calculation by entering an amount.</span></span>

10. <span data-ttu-id="8a4fd-129">حدد **ضريبة المبيعات** لعرض ضريبة المبيعات التي تم حسابها لفاتورتك.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-129">Select **Sales tax** to view the sales tax that is calculated for the invoice.</span></span>

    <span data-ttu-id="8a4fd-130">يمكنك عرض مبالغ ضريبة المبيعات في هذه الصفحة، أو يمكنك تجاوز المبالغ في علامة تبويب **التسوية**.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-130">You can view the sales tax amounts on this page, or you can override the amounts on the **Adjustment** tab.</span></span>

11. <span data-ttu-id="8a4fd-131">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-131">Select **OK**.</span></span>
12. <span data-ttu-id="8a4fd-132">حدد **التكاليف** لإضافة تكلفة إلى فاتورتك.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-132">Select **Charges** to add a charge to the invoice.</span></span>
13. <span data-ttu-id="8a4fd-133">في حقل **كود التكاليف‬**، أدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-133">In the **Charges code** field, enter a value.</span></span>
14. <span data-ttu-id="8a4fd-134">في حقل **قيمة التكاليف**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-134">In the **Charges value** field, enter a number.</span></span>
15. <span data-ttu-id="8a4fd-135">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-135">Close the page.</span></span>
16. <span data-ttu-id="8a4fd-136">حدد **الإجماليات** لعرض ملخص تفاصيل الفاتورة والإجماليات.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-136">Select **Totals** to view a summary of the invoice details and totals.</span></span>
17. <span data-ttu-id="8a4fd-137">حدد **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-137">Select **Close**.</span></span>
18. <span data-ttu-id="8a4fd-138">حدد **ترحيل** لترحيل الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-138">Select **Post** to post the invoice.</span></span> <span data-ttu-id="8a4fd-139">تبقى لديك فرصة لإلغاء قبل ترحيل الفاتورة فعليًا.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-139">You will still have an opportunity to cancel before you actually post.</span></span>

    * <span data-ttu-id="8a4fd-140">يمكنك تغيير توقيت طباعة الفواتير.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-140">You can change the timing of invoice printing.</span></span> <span data-ttu-id="8a4fd-141">حدد **الحالية** لطباعة كل فاتورة عند تحديثها.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-141">Select **Current** to print each invoice as it's updated.</span></span> <span data-ttu-id="8a4fd-142">حدد **بعد** لطباعة جميع الفواتير بعد تحديثها.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-142">Select **After** to print after all invoices have been updated.</span></span>
    * <span data-ttu-id="8a4fd-143">لتغيير كيفية التحقق من حد الائتمان الخاص بالعميل قبل أن يتم ترحيل الفاتورة، قم بتغيير القيمة في الحقل **نوع حد الائتمان**.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-143">To change how the customer's credit limit is verified before the invoice is posted, change the value in the **Credit limit type** field.</span></span>
    * <span data-ttu-id="8a4fd-144">لطباعة الفاتورة، عيّن الخيار إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-144">To print the invoice, set the option to **Yes**.</span></span>
    * <span data-ttu-id="8a4fd-145">لترحيل الفاتورة، عيّن الخيار إلى **لا**.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-145">To post the invoice, set the option to **Yes**.</span></span> <span data-ttu-id="8a4fd-146">يمكنك طباعة الفاتورة من دون ترحيلها.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-146">You can print the invoice without posting it.</span></span>

19. <span data-ttu-id="8a4fd-147">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-147">Select **OK**.</span></span>

## <a name="copy-lines"></a><span data-ttu-id="8a4fd-148">نسخ السطور</span><span class="sxs-lookup"><span data-stu-id="8a4fd-148">Copy lines</span></span>
<span data-ttu-id="8a4fd-149">لنسخ البنود في فاتورة نص حر، حدد بندًا واحدًا أو أكثر، ثم حدد **نسخ البنود المحددة**.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-149">To copy lines on a free text invoice, select one or more lines, and then select **Copy selected lines**.</span></span> <span data-ttu-id="8a4fd-150">يمكنك تحديد عدد النسخ التي ترغب في إنشائها، ويمكنك أيضًا نسخ الملاحظات والمرفقات.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-150">You can specify the number of copies to make, and you can also copy notes and attachments.</span></span> <span data-ttu-id="8a4fd-151">يمكنك إما نسخ التوزيعات أو السماح بإعادة إنشائها عند إجراء الترحيل.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-151">You can either copy the distributions or let them be re-created when you post.</span></span>

<span data-ttu-id="8a4fd-152">بعد نسخ البنود، يمكنك تحرير المعلومات حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-152">After you copy lines, you can edit the information as you require.</span></span>

## <a name="create-a-free-text-invoice-from-a-template"></a><span data-ttu-id="8a4fd-153">إنشاء فاتورة نص حر من قالب</span><span class="sxs-lookup"><span data-stu-id="8a4fd-153">Create a free text invoice from a template</span></span>
<span data-ttu-id="8a4fd-154">يمكنك إنشاء فاتورة نص حر من قالب.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-154">You can create a free text invoice from a template.</span></span> <span data-ttu-id="8a4fd-155">عندما تحدد **جديد من قالب** من علامة تبويب **الفاتورة**، يمكنك تحديد اسم قالب وحساب العميل لفاتورة النص الحر الجديدة.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-155">When you select **New from template** on the **Invoice** tab, you can select a template name and the customer account for the new free text invoice.</span></span> <span data-ttu-id="8a4fd-156">يمكن ملء القيم الافتراضية، مثل شروط الدفع وطريقة الدفع، من العميل بشكل تلقائي، أو يمكنك استخدام القيم التي تم حفظها مع القالب.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-156">Default values, such as the terms of payment and method of payment, can be automatically filled in from the customer, or you can use the values that were saved in the template.</span></span>

<span data-ttu-id="8a4fd-157">يتم إنشاء فاتورة نص حر جديدة ويمكنك تحرير القيم حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="8a4fd-157">A new free text invoice is created, and you can edit the values as you require.</span></span>

