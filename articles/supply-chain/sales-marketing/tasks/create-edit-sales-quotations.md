---
title: إنشاء عروض أسعار المبيعات وتحريرها
description: يوضح هذا الإجراء كيفية إنشاء عرض أسعار مبيعات وتحديثه.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SalesQuotationTotals, SalesQuotationPriceSimulation, SalesQuotationEditLines, SrsReportViewerForm, smmSetNumSeqIfManual, CustTable, SalesTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5b5618a815aaff12dd366523920ed275801b3b16
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "343617"
---
# <a name="create-and-edit-sales-quotations"></a><span data-ttu-id="da92b-103">إنشاء عروض أسعار المبيعات وتحريرها</span><span class="sxs-lookup"><span data-stu-id="da92b-103">Create and edit sales quotations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="da92b-104">يوضح هذا الإجراء كيفية إنشاء عرض أسعار مبيعات وتحديثه.</span><span class="sxs-lookup"><span data-stu-id="da92b-104">This procedure demonstrates how to create and update a sales quotation.</span></span> <span data-ttu-id="da92b-105">يمكنك تنفيذ هذا الإجراء في البيانات الخاصة بك أو في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="da92b-105">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-sales-quotation"></a><span data-ttu-id="da92b-106">إنشاء عرض أسعار مبيعات</span><span class="sxs-lookup"><span data-stu-id="da92b-106">Create a sales quotation</span></span>
1. <span data-ttu-id="da92b-107">انتقل إلى المبيعات والتسويق > عروض أسعار المبيعات > جميع عروض الأسعار.</span><span class="sxs-lookup"><span data-stu-id="da92b-107">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
2. <span data-ttu-id="da92b-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="da92b-108">Click New.</span></span>
3. <span data-ttu-id="da92b-109">في الحقل "نوع الحساب"، اكتب "عميل متوقع".</span><span class="sxs-lookup"><span data-stu-id="da92b-109">In the Account type field, select 'Prospect'.</span></span>
4. <span data-ttu-id="da92b-110">في الحقل "عميل متوقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="da92b-110">In the Prospect field, enter or select a value.</span></span>
5. <span data-ttu-id="da92b-111">قم بتوسيع القسم "عام".</span><span class="sxs-lookup"><span data-stu-id="da92b-111">Expand the General section.</span></span>
    * <span data-ttu-id="da92b-112">وحيث أنك اخترت إنشاء عرض أسعار من منطقة المبيعات والتسويق، سيتم تعيين النوع تلقائياً إلى عرض أسعار المبيعات.</span><span class="sxs-lookup"><span data-stu-id="da92b-112">Because you chose to create a quotation from the Sales and Marketing area, the type is automatically set to Sales quotation.</span></span> <span data-ttu-id="da92b-113">لإنشاء عرض أسعار لمشروع، عليك الوصول إليه من الوحدة النمطية لإدارة المشاريع والمحاسبة.</span><span class="sxs-lookup"><span data-stu-id="da92b-113">To create a quotation for a project you must access it from the Project management and accounting module.</span></span>   
6. <span data-ttu-id="da92b-114">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="da92b-114">Click OK.</span></span>
    * <span data-ttu-id="da92b-115">تتشابه الحقول والإجراءات ببنود عرض الأسعار جداً مع تلك الموجودة في بنود أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="da92b-115">The fields and actions on the quotation lines are very similar to the ones on the sales order lines.</span></span>   <span data-ttu-id="da92b-116">وعلى غرار أوامر المبيعات، يمكنك إنشاء عروض أسعار لصنف معين، أو عندما يكون رقم الصنف مجهولًا أو غير موجود في وقت إنشاء عرض الأسعار، يمكنك إنشاء عروض أسعار لفئة مبيعات.</span><span class="sxs-lookup"><span data-stu-id="da92b-116">Like sales orders, quotations can be created for a specific item or, when item number is not known or does not exist at the time of quotation creation, quotations can be created for a sales category.</span></span>  
7. <span data-ttu-id="da92b-117">في الحقل "الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="da92b-117">In the Item field, enter or select a value.</span></span>
8. <span data-ttu-id="da92b-118">في الحقل "الصنف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="da92b-118">In the Item field, type a value.</span></span>
9. <span data-ttu-id="da92b-119">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="da92b-119">Close the page.</span></span>
10. <span data-ttu-id="da92b-120">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="da92b-120">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="da92b-121">إذا كان هناك اتفاقيات تجارية صالحة للصنف المحدد في البند، سيتم نسخ السعر والخصومات القابلة للتطبيق تلقائياً لبند عرض الأسعار.</span><span class="sxs-lookup"><span data-stu-id="da92b-121">If there are valid trade agreements for the item selected on the line, the applicable price and discounts will be automatically copied to the quotation line.</span></span> <span data-ttu-id="da92b-122">تأكد أن الحقل "سعر الوحدة" يحتوي على قيمة ويمكنك أيضًا إدخال قيم الخصم إذا أردت.</span><span class="sxs-lookup"><span data-stu-id="da92b-122">Make sure that the Unit price field contains a value and you can also enter discount values if you want to.</span></span>  
11. <span data-ttu-id="da92b-123">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="da92b-123">Click Save.</span></span>
12. <span data-ttu-id="da92b-124">في جزء "الإجراءات"، انقر فوق "عرض أسعار المبيعات".</span><span class="sxs-lookup"><span data-stu-id="da92b-124">On the Action Pane, click Sales quotation.</span></span>
13. <span data-ttu-id="da92b-125">انقر فوق "الإجماليات".</span><span class="sxs-lookup"><span data-stu-id="da92b-125">Click Totals.</span></span>
14. <span data-ttu-id="da92b-126">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="da92b-126">Click OK.</span></span>
15. <span data-ttu-id="da92b-127">انقر فوق بند عرض أسعار المبيعات.</span><span class="sxs-lookup"><span data-stu-id="da92b-127">Click Sales quotation line.</span></span>
16. <span data-ttu-id="da92b-128">انقر فوق "الأسعار".</span><span class="sxs-lookup"><span data-stu-id="da92b-128">Click Prices.</span></span>
    * <span data-ttu-id="da92b-129">في الصفحة "تشغيل محاكاة السعر"، يمكنك إجراء تجربة ضبط الإيراد أو الربحية المتوقعة لعرض الأسعار الخاص بك على أساس سعر الوحدة أو مبلغ الخص أو النسبة المئوية للخصم أو المبلغ الإجمالي أو الهامش أو هامش المساهمة المطلوب.</span><span class="sxs-lookup"><span data-stu-id="da92b-129">In the Run price simulation page you can experiment with adjusting the expected revenue or profitability of your quotation based on the desired unit price, discount amount, discount percentage, total amount, margin, or contribution ratio.</span></span>   <span data-ttu-id="da92b-130">عندما تكون راضيًا عن الأرقام المستهدفة، ستطبق الاقتراح على بند عرض الأسعار، وسيتم تحديث الحقول المتعلقة بسعره وفقا لذلك.</span><span class="sxs-lookup"><span data-stu-id="da92b-130">When you are satisfied with the target figures, you apply the suggestion to the quotation line, and its price-related fields will be updated accordingly.</span></span>  
    * <span data-ttu-id="da92b-131">يمكنك إنشاء العديد من عمليات محاكاة السعر بالطريقة التي تريدها.</span><span class="sxs-lookup"><span data-stu-id="da92b-131">Y ou can create as many price simulations as you wish.</span></span> <span data-ttu-id="da92b-132">عند النقر فوق "جديد"، يتم نسخ شروط السعر من بند عرض الأسعار الحالي للصفحة.</span><span class="sxs-lookup"><span data-stu-id="da92b-132">When you click New, the price conditions from the current quotation line are copied to the page.</span></span> <span data-ttu-id="da92b-133">يمكنك بعد ذلك تعديل القيم في أي من المجالات المتعلقة بالأسعار إلى القيم المستهدفة.</span><span class="sxs-lookup"><span data-stu-id="da92b-133">You can then modify values in any of the price-related fields to the target ones.</span></span> <span data-ttu-id="da92b-134">سوف يؤدي تغيير أحد الحقول إلى تشغيل إعادة الحساب في جميع الحقول الأخرى.</span><span class="sxs-lookup"><span data-stu-id="da92b-134">A change in one of the fields will trigger recalculation in all the other fields.</span></span> <span data-ttu-id="da92b-135">لكي يحسب النظام هامش المبيعات ونسبة المساهمة، يجب أن تكون تكلفة وحدة المنتج معلومة.</span><span class="sxs-lookup"><span data-stu-id="da92b-135">In order for the system to calculate the sales margin and contribution ratio, the product's unit cost has to be known.</span></span> <span data-ttu-id="da92b-136">استخدم علامة التبويب "الأسعار التي تمت محاكاتها" للحصول على عرض مفصل للأسعار الأصلية والتغييرات المقترحة وأثرها على إجماليات عرض الأسعار.</span><span class="sxs-lookup"><span data-stu-id="da92b-136">Use the Simulated prices tab for a detailed view of the original prices, proposed changes and their effect on the quotation totals.</span></span>   <span data-ttu-id="da92b-137">كقاعدة عامة، عندما يتم تطبيق محاكاة تحدد مبلغًا جديدًا لبند عرض الأسعار، سيعيد النظام الحساب ويدخل قيمة جديدة في الحقل "سعر الوحدة".</span><span class="sxs-lookup"><span data-stu-id="da92b-137">As a general rule, when a simulation that sets a new amount is applied to the quotation line, the system recalculates and enters a new value in the Unit price field.</span></span> <span data-ttu-id="da92b-138">إذا كانت المحاكاة مستندة إلى هامش جديد أو نسبة هامش مساهمة جديدة، سيتم تحديث الحقل "المبلغ الصافي" فقط، وستكون الحقل "سعر الوحدة" فارغاً.</span><span class="sxs-lookup"><span data-stu-id="da92b-138">If the simulation is based on a new margin or a new contribution ratio, only the Net amount field is updated, and the Unit price is blank.</span></span> <span data-ttu-id="da92b-139">وفي كلتا الحالتين، سيتم حذف أية خصومات كانت في بند عرض الأسعار قبل إجراء المحاكاة.</span><span class="sxs-lookup"><span data-stu-id="da92b-139">In both cases, any discounts that were on the quotation line before simulation will be deleted.</span></span>  
17. <span data-ttu-id="da92b-140">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="da92b-140">Close the page.</span></span>
18. <span data-ttu-id="da92b-141">في جزء "الإجراءات"، انقر فوق "عرض أسعار".</span><span class="sxs-lookup"><span data-stu-id="da92b-141">On the Action Pane, click Quotation.</span></span>
19. <span data-ttu-id="da92b-142">انقر فوق "إرسال عرض أسعار".</span><span class="sxs-lookup"><span data-stu-id="da92b-142">Click Send quotation.</span></span>
20. <span data-ttu-id="da92b-143">حدد "نعم" في الحقل "طباعة عرض الأسعار".</span><span class="sxs-lookup"><span data-stu-id="da92b-143">Select Yes in the Print quotation field.</span></span>
21. <span data-ttu-id="da92b-144">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="da92b-144">Click OK.</span></span>
    * <span data-ttu-id="da92b-145">قد يستغرق التقرير دقيقة لإنشائه.</span><span class="sxs-lookup"><span data-stu-id="da92b-145">The report may take a minute to generate.</span></span> <span data-ttu-id="da92b-146">لا تغلق الصفحة حتى تنشئَ التقرير.</span><span class="sxs-lookup"><span data-stu-id="da92b-146">Don’t close the page until it does so.</span></span>  
22. <span data-ttu-id="da92b-147">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="da92b-147">Close the page.</span></span>

## <a name="update-a-sales-quotation"></a><span data-ttu-id="da92b-148">تحديث عرض أسعار مبيعات</span><span class="sxs-lookup"><span data-stu-id="da92b-148">Update a sales quotation</span></span>
1. <span data-ttu-id="da92b-149">في جزء "الإجراءات"، انقر فوق "متابعة".</span><span class="sxs-lookup"><span data-stu-id="da92b-149">On the Action Pane, click Follow up.</span></span>
2. <span data-ttu-id="da92b-150">انقر فوق "تحويل إلى عميل".</span><span class="sxs-lookup"><span data-stu-id="da92b-150">Click Convert to customer.</span></span>
3. <span data-ttu-id="da92b-151">في الحقل "حساب العميل"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="da92b-151">In the Customer account field, type a value.</span></span>
4. <span data-ttu-id="da92b-152">انقر فوق "تحقق".</span><span class="sxs-lookup"><span data-stu-id="da92b-152">Click Check.</span></span>
    * <span data-ttu-id="da92b-153">تأكد من رؤية رسالة تفيد بأن رقم الحساب الذي قمت بكتابته مُتاح للاستخدام.</span><span class="sxs-lookup"><span data-stu-id="da92b-153">Make sure you see a message that the account number you typed in is free to use.</span></span>  
5. <span data-ttu-id="da92b-154">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="da92b-154">Click OK.</span></span>
    * <span data-ttu-id="da92b-155">أنشأ النظام الآن حساب عميل جديد للعميل المتوقع في عرض الأسعار.</span><span class="sxs-lookup"><span data-stu-id="da92b-155">The system has now created a new customer account for the prospect on the quotation.</span></span>  
6. <span data-ttu-id="da92b-156">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="da92b-156">Close the page.</span></span>
7. <span data-ttu-id="da92b-157">في جزء "الإجراءات"، انقر فوق "متابعة".</span><span class="sxs-lookup"><span data-stu-id="da92b-157">On the Action Pane, click Follow up.</span></span>
8. <span data-ttu-id="da92b-158">انقر فوق "تأكيد".</span><span class="sxs-lookup"><span data-stu-id="da92b-158">Click Confirm.</span></span>
9. <span data-ttu-id="da92b-159">في الحقل "السبب"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="da92b-159">In the Reason field, enter or select a value.</span></span>
10. <span data-ttu-id="da92b-160">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="da92b-160">Click OK.</span></span>
11. <span data-ttu-id="da92b-161">في جزء "الإجراءات"، انقر فوق "عام".</span><span class="sxs-lookup"><span data-stu-id="da92b-161">On the Action Pane, click General.</span></span>
12. <span data-ttu-id="da92b-162">انقر فوق "أوامر المبيعات".</span><span class="sxs-lookup"><span data-stu-id="da92b-162">Click Sales orders.</span></span>
13. <span data-ttu-id="da92b-163">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="da92b-163">Close the page.</span></span>

