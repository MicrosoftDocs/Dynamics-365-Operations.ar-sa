--- 
title: "إنشاء فاتورة نص حر"
description: "يوضح دليل المهمة هذا كيفية إنشاء فاتورة نص حر."
author: mikefalkner
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 33324a9b95026600bcc6facb9c22a04fd2e323c8
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-free-text-invoice"></a><span data-ttu-id="da077-103">إنشاء فاتورة نص حر</span><span class="sxs-lookup"><span data-stu-id="da077-103">Create a free text invoice</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="da077-104">يوضح دليل المهمة هذا كيفية إنشاء فاتورة نص حر.</span><span class="sxs-lookup"><span data-stu-id="da077-104">This task guide demonstrates creating a free text invoice.</span></span> <span data-ttu-id="da077-105">تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="da077-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="da077-106">انتقل إلى الحسابات المدينة > الفواتير > جميع الفواتير بنص حر‬.</span><span class="sxs-lookup"><span data-stu-id="da077-106">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="da077-107">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="da077-107">Click New.</span></span>
3. <span data-ttu-id="da077-108">في الحقل "حساب العميل"، حدد قيمة.</span><span class="sxs-lookup"><span data-stu-id="da077-108">In the Customer account field, select a value.</span></span>
    * <span data-ttu-id="da077-109">وسوف يتم تعيين حساب الفاتورة افتراضيًا لنفس الحساب المستخدم لحساب العميل.</span><span class="sxs-lookup"><span data-stu-id="da077-109">The invoice account will default to the same account used for the customer account.</span></span>   
    * <span data-ttu-id="da077-110">تبدأ حالة المحاسبة بـ "قيد التنفيذ" إذا لم يتم ترحيل الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="da077-110">The accounting status starts with In process if the invoice is not posted.</span></span>   
    * <span data-ttu-id="da077-111">سوف يتم تعيين رقم الفاتورة عند ترحيل الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="da077-111">The invoice number will be assigned when the invoice is posted.</span></span>  
    * <span data-ttu-id="da077-112">إذا كنت تستخدم تفويضات SEPA‏‫، فسوف يتم ملء تفويض الخصم المباشر‬ تلقائيًا بتفويض عند تحديد حساب العميل.</span><span class="sxs-lookup"><span data-stu-id="da077-112">If you are using SEPA mandates, the direct debit mandate will be automatically populated with a mandate when you select the customer account.</span></span>  
4. <span data-ttu-id="da077-113">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="da077-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="da077-114">في الحقل "الحساب الرئيسي، حدد رقم حساب دون أبعاد.</span><span class="sxs-lookup"><span data-stu-id="da077-114">In the Main account field, specify an account number without dimensions.</span></span>
    * <span data-ttu-id="da077-115">يمكنك أيضًا إدخال حرف واحد أو أكثر للحساب الرئيسي، واستخدام خاصية البحث للعثور على حسابك.</span><span class="sxs-lookup"><span data-stu-id="da077-115">You can also enter one or more characters for the main account and use the lookup to find your account.</span></span> <span data-ttu-id="da077-116">ستقوم بإدخال الأبعاد فيما بعد في هذا الدليل.</span><span class="sxs-lookup"><span data-stu-id="da077-116">You will enter dimensions later on in this guide.</span></span>  
6. <span data-ttu-id="da077-117">قم بتوسيع علامة التبويب السريعة "تفاصيل البند" لكي تتمكن من إضافة أبعاد إلى حسابك الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="da077-117">Expand the Line details fasttab so you can add dimensions to your main account.</span></span>
7. <span data-ttu-id="da077-118">انقر فوق علامة تبويب بند "الأبعاد المالية".</span><span class="sxs-lookup"><span data-stu-id="da077-118">Click the Financial dimensions line tab.</span></span>
    * <span data-ttu-id="da077-119">تتعلق الأبعاد بالبند المحدد فقط.</span><span class="sxs-lookup"><span data-stu-id="da077-119">The dimensions are for the selected line only.</span></span>    
    * <span data-ttu-id="da077-120">يتم ملء مجموعة ضريبة المبيعات من العميل.</span><span class="sxs-lookup"><span data-stu-id="da077-120">The sales tax group is populated from the customer.</span></span> <span data-ttu-id="da077-121">إذا لم تتوفر لدى العميل مجموعة ضريبة مبيعات، فيتم استخدام مجموعة ضريبة المبيعات من الحساب الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="da077-121">If the customer does not have a sales tax group, the sales tax group from the main account is used.</span></span>  
    * <span data-ttu-id="da077-122">إذا تم ملء مجموعة ضريبة مبيعات الأصناف من الحساب الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="da077-122">The items sales tax group is populated from the main account.</span></span> <span data-ttu-id="da077-123">إذا لم يتوافر للحساب الرئيسي مجموعة ضريبة مبيعات أصناف، فمن ثم يتم استخدام مجموعة ضريبة مبيعات الأصناف في محددات ضريبة المبيعات في دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="da077-123">If the main account does not have a item sales tax group, then the item sales tax group in the General ledger sales tax parameters is used.</span></span>    
8. <span data-ttu-id="da077-124">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="da077-124">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="da077-125">الكمية اختيارية.</span><span class="sxs-lookup"><span data-stu-id="da077-125">The quantity is optional.</span></span>  
9. <span data-ttu-id="da077-126">في حقل "سعر الوحدة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="da077-126">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="da077-127">سعر الوحدة اختياري.</span><span class="sxs-lookup"><span data-stu-id="da077-127">The unit price is optional.</span></span>  
    * <span data-ttu-id="da077-128">يتم حساب المبلغ بضرب الكميات في سعر الوحدة.</span><span class="sxs-lookup"><span data-stu-id="da077-128">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="da077-129">ومع ذلك، يمكنك تجاوز هذا الحساب وإدخال مبلغ.</span><span class="sxs-lookup"><span data-stu-id="da077-129">However, you can override that calculation and enter an amount.</span></span>  
10. <span data-ttu-id="da077-130">انقر فوق ضريبة المبيعات لعرض ضريبة المبيعات التي تم حسابها لفاتورتك.</span><span class="sxs-lookup"><span data-stu-id="da077-130">Click on Sales tax to view the sales tax calculated for your invoice.</span></span>
    * <span data-ttu-id="da077-131">استعرض مبالغ ضريبة المبيعات في هذه الصفحة، أو يمكنك تجاوز المبالغ في علامة تبويب "التسوية".</span><span class="sxs-lookup"><span data-stu-id="da077-131">View the sales tax amounts in this page or you can override the amounts on the Adjustment tab.</span></span>  
11. <span data-ttu-id="da077-132">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="da077-132">Click OK.</span></span>
12. <span data-ttu-id="da077-133">انقر فوق "التكاليف" لإضافة التكلفة إلى فاتورتك.</span><span class="sxs-lookup"><span data-stu-id="da077-133">Click Charges to add a charge to your invoice.</span></span> 
13. <span data-ttu-id="da077-134">في الحقل "كود التكاليف‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="da077-134">In the Charges code field, type a value.</span></span>
14. <span data-ttu-id="da077-135">في الحقل "قيمة التكاليف‬، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="da077-135">In the Charges value field, enter a number.</span></span>
15. <span data-ttu-id="da077-136">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="da077-136">Close the page.</span></span>
16. <span data-ttu-id="da077-137">انقر فوق "الإجماليات" لعرض ملخص تفاصيل الفاتورة والإجماليات.</span><span class="sxs-lookup"><span data-stu-id="da077-137">Click Totals to view the summary invoice details and totals.</span></span>
17. <span data-ttu-id="da077-138">انقر فوق "إغلاق".</span><span class="sxs-lookup"><span data-stu-id="da077-138">Click Close.</span></span>
18. <span data-ttu-id="da077-139">انقر فوق "ترحيل" لترحيل الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="da077-139">Click Post to post the invoice.</span></span> <span data-ttu-id="da077-140">سوف تتمكن من الإلغاء قبل الترحيل.</span><span class="sxs-lookup"><span data-stu-id="da077-140">You will be able to cancel before you post.</span></span>
    * <span data-ttu-id="da077-141">لتغيير توقيت طباعة الفواتير:  حدد "الحالي" لطباعة كل فاتورة عند تحديثها أو حدد "بعد" للطباعة بعد تحديث كافة الفواتير.</span><span class="sxs-lookup"><span data-stu-id="da077-141">To change the timing of your invoice printing:  Select Current to print each invoice as it is updated   or  Select After to print after all invoices have been updated.</span></span>  
    * <span data-ttu-id="da077-142">إذا أردت تغيير كيف يتم فحص حد الائتمان الخاص بالعميل قبل الترحيل، يمكنك تغيير نوع حد الائتمان.</span><span class="sxs-lookup"><span data-stu-id="da077-142">If you want to change how the customer's credit limit is checked before posting, change the Credit limit type.</span></span>  
    * <span data-ttu-id="da077-143">إذا أردت طباعة الفاتورة، فحدد "نعم".</span><span class="sxs-lookup"><span data-stu-id="da077-143">If you want to print the invoice, select Yes.</span></span>  
    * <span data-ttu-id="da077-144">إذا أردت ترحيل الفاتورة، فحدد "نعم".</span><span class="sxs-lookup"><span data-stu-id="da077-144">If you want to post the invoice, select Yes.</span></span> <span data-ttu-id="da077-145">يمكنك طباعة الفاتورة دون ترحيلها.</span><span class="sxs-lookup"><span data-stu-id="da077-145">You can print the invoice without posting.</span></span>  
19. <span data-ttu-id="da077-146">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="da077-146">Click OK.</span></span>


