--- 
title: "إنشاء فاتورة نص حر"
description: "توضح هذه المقالة كيفية إنشاء فاتورة نص حر."
author: mikefalkner
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f69505f0c6137121cae92d42d052b244326c8436
ms.openlocfilehash: 2a611bdd4dd97109709ed355eb80471e27413744
ms.contentlocale: ar-sa
ms.lasthandoff: 06/28/2018

---

# <a name="create-a-free-text-invoice"></a><span data-ttu-id="96e12-103">إنشاء فاتورة نص حر</span><span class="sxs-lookup"><span data-stu-id="96e12-103">Create a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="96e12-104">توضح هذه المقالة كيفية إنشاء فاتورة نص حر.</span><span class="sxs-lookup"><span data-stu-id="96e12-104">This article demonstrates how to create a free text invoice.</span></span> <span data-ttu-id="96e12-105">بالنسبة لهذا الإجراء، استخدم شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="96e12-105">For this procedure, use the USMF demo company.</span></span>

## <a name="create-a-free-text-invoice"></a><span data-ttu-id="96e12-106">إنشاء فاتورة نص حر</span><span class="sxs-lookup"><span data-stu-id="96e12-106">Create a free text invoice</span></span>

1. <span data-ttu-id="96e12-107">انتقل إلى الحسابات المدينة > الفواتير > جميع الفواتير بنص حر‬.</span><span class="sxs-lookup"><span data-stu-id="96e12-107">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="96e12-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="96e12-108">Click New.</span></span>
3. <span data-ttu-id="96e12-109">في الحقل "حساب العميل"، حدد قيمة.</span><span class="sxs-lookup"><span data-stu-id="96e12-109">In the Customer account field, select a value.</span></span>
    * <span data-ttu-id="96e12-110">وسوف يتم تعيين حساب الفاتورة افتراضيًا لنفس الحساب المستخدم لحساب العميل.</span><span class="sxs-lookup"><span data-stu-id="96e12-110">The invoice account will default to the same account used for the customer account.</span></span>   
    * <span data-ttu-id="96e12-111">تبدأ حالة المحاسبة بـ "قيد التنفيذ" إذا لم يتم ترحيل الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="96e12-111">The accounting status starts with In process if the invoice is not posted.</span></span>   
    * <span data-ttu-id="96e12-112">سوف يتم تعيين رقم الفاتورة عند ترحيل الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="96e12-112">The invoice number will be assigned when the invoice is posted.</span></span>  
    * <span data-ttu-id="96e12-113">إذا كنت تستخدم تفويضات SEPA‏‫، فسوف يتم ملء تفويض الخصم المباشر‬ تلقائيًا بتفويض عند تحديد حساب العميل.</span><span class="sxs-lookup"><span data-stu-id="96e12-113">If you are using SEPA mandates, the direct debit mandate will be automatically populated with a mandate when you select the customer account.</span></span>  
4. <span data-ttu-id="96e12-114">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="96e12-114">In the Description field, type a value.</span></span>
5. <span data-ttu-id="96e12-115">في الحقل "الحساب الرئيسي، حدد رقم حساب دون أبعاد.</span><span class="sxs-lookup"><span data-stu-id="96e12-115">In the Main account field, specify an account number without dimensions.</span></span>
    * <span data-ttu-id="96e12-116">يمكنك أيضًا إدخال حرف واحد أو أكثر للحساب الرئيسي، واستخدام خاصية البحث للعثور على حسابك.</span><span class="sxs-lookup"><span data-stu-id="96e12-116">You can also enter one or more characters for the main account and use the lookup to find your account.</span></span> <span data-ttu-id="96e12-117">ستقوم بإدخال الأبعاد فيما بعد في هذا الدليل.</span><span class="sxs-lookup"><span data-stu-id="96e12-117">You will enter dimensions later on in this guide.</span></span>  
6. <span data-ttu-id="96e12-118">قم بتوسيع علامة التبويب السريعة "تفاصيل البند" لكي تتمكن من إضافة أبعاد إلى حسابك الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="96e12-118">Expand the Line details fasttab so you can add dimensions to your main account.</span></span>
7. <span data-ttu-id="96e12-119">انقر فوق علامة تبويب بند "الأبعاد المالية".</span><span class="sxs-lookup"><span data-stu-id="96e12-119">Click the Financial dimensions line tab.</span></span>
    * <span data-ttu-id="96e12-120">تتعلق الأبعاد بالبند المحدد فقط.</span><span class="sxs-lookup"><span data-stu-id="96e12-120">The dimensions are for the selected line only.</span></span>    
    * <span data-ttu-id="96e12-121">يتم ملء مجموعة ضريبة المبيعات من العميل.</span><span class="sxs-lookup"><span data-stu-id="96e12-121">The sales tax group is populated from the customer.</span></span> <span data-ttu-id="96e12-122">إذا لم تتوفر لدى العميل مجموعة ضريبة مبيعات، فيتم استخدام مجموعة ضريبة المبيعات من الحساب الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="96e12-122">If the customer does not have a sales tax group, the sales tax group from the main account is used.</span></span>  
    * <span data-ttu-id="96e12-123">إذا تم ملء مجموعة ضريبة مبيعات الأصناف من الحساب الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="96e12-123">The items sales tax group is populated from the main account.</span></span> <span data-ttu-id="96e12-124">إذا لم يتوافر للحساب الرئيسي مجموعة ضريبة مبيعات أصناف، فمن ثم يتم استخدام مجموعة ضريبة مبيعات الأصناف في معلمات ضريبة المبيعات في دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="96e12-124">If the main account does not have an item sales tax group, then the item sales tax group in the General ledger sales tax parameters is used.</span></span>    
8. <span data-ttu-id="96e12-125">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="96e12-125">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="96e12-126">الكمية اختيارية.</span><span class="sxs-lookup"><span data-stu-id="96e12-126">The quantity is optional.</span></span>  
9. <span data-ttu-id="96e12-127">في حقل "سعر الوحدة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="96e12-127">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="96e12-128">سعر الوحدة اختياري.</span><span class="sxs-lookup"><span data-stu-id="96e12-128">The unit price is optional.</span></span>  
    * <span data-ttu-id="96e12-129">يتم حساب المبلغ بضرب الكميات في سعر الوحدة.</span><span class="sxs-lookup"><span data-stu-id="96e12-129">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="96e12-130">ومع ذلك، يمكنك تجاوز هذا الحساب وإدخال مبلغ.</span><span class="sxs-lookup"><span data-stu-id="96e12-130">However, you can override that calculation and enter an amount.</span></span>  
10. <span data-ttu-id="96e12-131">انقر فوق ضريبة المبيعات لعرض ضريبة المبيعات التي تم حسابها لفاتورتك.</span><span class="sxs-lookup"><span data-stu-id="96e12-131">Click on Sales tax to view the sales tax calculated for your invoice.</span></span>
    * <span data-ttu-id="96e12-132">استعرض مبالغ ضريبة المبيعات في هذه الصفحة، أو يمكنك تجاوز المبالغ في علامة تبويب "التسوية".</span><span class="sxs-lookup"><span data-stu-id="96e12-132">View the sales tax amounts in this page or you can override the amounts on the Adjustment tab.</span></span>  
11. <span data-ttu-id="96e12-133">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="96e12-133">Click OK.</span></span>
12. <span data-ttu-id="96e12-134">انقر فوق "التكاليف" لإضافة التكلفة إلى فاتورتك.</span><span class="sxs-lookup"><span data-stu-id="96e12-134">Click Charges to add a charge to your invoice.</span></span> 
13. <span data-ttu-id="96e12-135">في الحقل "كود التكاليف‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="96e12-135">In the Charges code field, type a value.</span></span>
14. <span data-ttu-id="96e12-136">في الحقل "قيمة التكاليف‬، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="96e12-136">In the Charges value field, enter a number.</span></span>
15. <span data-ttu-id="96e12-137">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="96e12-137">Close the page.</span></span>
16. <span data-ttu-id="96e12-138">انقر فوق "الإجماليات" لعرض ملخص تفاصيل الفاتورة والإجماليات.</span><span class="sxs-lookup"><span data-stu-id="96e12-138">Click Totals to view the summary invoice details and totals.</span></span>
17. <span data-ttu-id="96e12-139">انقر فوق "إغلاق".</span><span class="sxs-lookup"><span data-stu-id="96e12-139">Click Close.</span></span>
18. <span data-ttu-id="96e12-140">انقر فوق "ترحيل" لترحيل الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="96e12-140">Click Post to post the invoice.</span></span> <span data-ttu-id="96e12-141">سوف تتمكن من الإلغاء قبل الترحيل.</span><span class="sxs-lookup"><span data-stu-id="96e12-141">You will be able to cancel before you post.</span></span>
    * <span data-ttu-id="96e12-142">لتغيير توقيت طباعة الفواتير:  حدد "الحالي" لطباعة كل فاتورة عند تحديثها أو حدد "بعد" للطباعة بعد تحديث كافة الفواتير.</span><span class="sxs-lookup"><span data-stu-id="96e12-142">To change the timing of your invoice printing:  Select Current to print each invoice as it is updated   or  Select After to print after all invoices have been updated.</span></span>  
    * <span data-ttu-id="96e12-143">إذا أردت تغيير كيف يتم فحص حد الائتمان الخاص بالعميل قبل الترحيل، يمكنك تغيير نوع حد الائتمان.</span><span class="sxs-lookup"><span data-stu-id="96e12-143">If you want to change how the customer's credit limit is checked before posting, change the Credit limit type.</span></span>  
    * <span data-ttu-id="96e12-144">إذا أردت طباعة الفاتورة، فحدد "نعم".</span><span class="sxs-lookup"><span data-stu-id="96e12-144">If you want to print the invoice, select Yes.</span></span>  
    * <span data-ttu-id="96e12-145">إذا أردت ترحيل الفاتورة، فحدد "نعم".</span><span class="sxs-lookup"><span data-stu-id="96e12-145">If you want to post the invoice, select Yes.</span></span> <span data-ttu-id="96e12-146">يمكنك طباعة الفاتورة دون ترحيلها.</span><span class="sxs-lookup"><span data-stu-id="96e12-146">You can print the invoice without posting.</span></span>  
19. <span data-ttu-id="96e12-147">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="96e12-147">Click OK.</span></span>

## <a name="copy-lines"></a><span data-ttu-id="96e12-148">نسخ السطور</span><span class="sxs-lookup"><span data-stu-id="96e12-148">Copy lines</span></span>
<span data-ttu-id="96e12-149">لنسخ السطور في فاتورة نص حر، حدد سطر واحد أو أكثر ثم انقر فوق نسخ السطور المحددة.</span><span class="sxs-lookup"><span data-stu-id="96e12-149">To copy lines on the free text invoice, select one or more lines and then click Copy selected lines.</span></span> <span data-ttu-id="96e12-150">يمكنك تحديد عدد النسخ التي ترغب في إنشائها، ويمكنك أيضًا نسخ الملاحظات والمرفقات.</span><span class="sxs-lookup"><span data-stu-id="96e12-150">You can specify the number of copies that you want to make, and you can also copy notes and attachments.</span></span> <span data-ttu-id="96e12-151">يمكنك نسخ التوزيعات أو السماح بإعادة إنشائهم عندما تقوم بالترحيل.</span><span class="sxs-lookup"><span data-stu-id="96e12-151">You can copy the distributions or allow them to be recreated when you post.</span></span> <span data-ttu-id="96e12-152">بمجرد أن تقوم بنسخ السطور، يمكنك تحرير المعلومات حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="96e12-152">Once you copy the lines, you can edit the information as needed.</span></span> 

## <a name="create-a-free-text-invoice-from-a-template"></a><span data-ttu-id="96e12-153">إنشاء فاتورة نص حر من قالب</span><span class="sxs-lookup"><span data-stu-id="96e12-153">Create a free text invoice from a template</span></span>
<span data-ttu-id="96e12-154">يمكنك إنشاء فاتورة نص حر من قالب.</span><span class="sxs-lookup"><span data-stu-id="96e12-154">You can create a free text invoice from a template.</span></span> <span data-ttu-id="96e12-155">عندما تقوم بتحديد "جديد" من "قالب" من علامة تبويب الفاتورة، يمكنك تحديد اسم قالب وحساب العميل لفاتورة النص الحر الجديدة.</span><span class="sxs-lookup"><span data-stu-id="96e12-155">When you select New from template from the Invoice tab, you can select a template name and the customer account for the new free text invoice.</span></span> <span data-ttu-id="96e12-156">يمكنك أيضًا اختيار قيم افتراضية مثل شروط الدفع وطريقة الدفع من العميل أو استخدام القيم التي تم حفظها مع القالب.</span><span class="sxs-lookup"><span data-stu-id="96e12-156">You can also choose to default values such as the terms of payment and method of payment from the customer or use the values that were saved with the template.</span></span> <span data-ttu-id="96e12-157">سوف يتم إنشاء فاتورة نص حر جديدة ويمكنك تحرير القيم الموجودة في هذه الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="96e12-157">A new free text invoice will be created and you can edit the values in that invoice.</span></span> 


