--- 
title: "تسجيل عمولات المبيعات"
description: "يوضح هذا الإجراء كيفية حساب عمولات المبيعات وتسجيلها."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f195f9e466eab3cf87afea2b5d430d0ea25c5a83
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="register-sales-commissions"></a><span data-ttu-id="709c0-103">تسجيل عمولات المبيعات</span><span class="sxs-lookup"><span data-stu-id="709c0-103">Register sales commissions</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="709c0-104">يوضح هذا الإجراء كيفية حساب عمولات المبيعات وتسجيلها.</span><span class="sxs-lookup"><span data-stu-id="709c0-104">This procedure shows you how sales commissions are calculated and registered.</span></span> <span data-ttu-id="709c0-105">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF أو باستخدام بياناتك الخاصة.</span><span class="sxs-lookup"><span data-stu-id="709c0-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="709c0-106">قبل تشغيل هذا الدليل، قم بتشغيل الدليل المُسمى "إعداد قواعد عمولات المبيعات" للتأكد من وجود توفر إعداد حساب العمولات الضروري بالكامل.</span><span class="sxs-lookup"><span data-stu-id="709c0-106">Before starting this guide, run the guide called "Set up sales commission rules" to make sure that you have all the necessary commission calculation setup.</span></span>

<span data-ttu-id="709c0-107">قم بتدوين ملاحظة بالعميل وأرقام الأصناف التي قمت باختيارها لعملية العمولات واستخدمها عندما يُطلبك منك إنشاء أمر مبيعات في هذا الدليل.</span><span class="sxs-lookup"><span data-stu-id="709c0-107">Take note of the customer and item numbers that you have chosen for the commission process and use them when asked to create a sales order in this guide.</span></span>


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a><span data-ttu-id="709c0-108">فوترة أمر مبيعات يؤهل مندوب مبيعات لعمولة</span><span class="sxs-lookup"><span data-stu-id="709c0-108">Invoice a sales order that qualifies a salesperson for a commission</span></span>
1. <span data-ttu-id="709c0-109">انتقل إلى المبيعات والتسويق > أوامر المبيعات > كافة أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="709c0-109">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="709c0-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="709c0-110">Click New.</span></span>
3. <span data-ttu-id="709c0-111">في الحقل "حساب العميل"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="709c0-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="709c0-112">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="709c0-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="709c0-113">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="709c0-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="709c0-114">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="709c0-114">Click OK.</span></span>
7. <span data-ttu-id="709c0-115">في جزء الإجراءات، انقر فوق "خيارات".</span><span class="sxs-lookup"><span data-stu-id="709c0-115">On the Action Pane, click Options.</span></span>
8. <span data-ttu-id="709c0-116">انقر فوق "تغيير طريقة العرض‬".</span><span class="sxs-lookup"><span data-stu-id="709c0-116">Click Change view.</span></span>
9. <span data-ttu-id="709c0-117">انقر فوق "عرض الرأس".</span><span class="sxs-lookup"><span data-stu-id="709c0-117">Click Header view.</span></span>
10. <span data-ttu-id="709c0-118">قم بتوسيع قسم "الإعداد".</span><span class="sxs-lookup"><span data-stu-id="709c0-118">Expand the Setup section.</span></span>
    * <span data-ttu-id="709c0-119">تمثل القيمة الموجودة في الحقل "مجموعة المبيعات" مجموعة معين لها مندوب مبيعات واحد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="709c0-119">The value in the Sales group field represents a group with one or more sales representatives assigned to it.</span></span> <span data-ttu-id="709c0-120">ويمثل الأشخاص الذين تحتوي عليهم المجموعة من سيحصل على العمولات عند فوترة الأمر، وفقًا للنسب والتوزيع المحدد مسبقاً.</span><span class="sxs-lookup"><span data-stu-id="709c0-120">The people in the group are the ones who will receive commissions when the order is invoiced, as per predefined rates and distribution.</span></span>   <span data-ttu-id="709c0-121">يتم نسخ القيمة من بطاقة العميل، ولكن يمكنك تغييرها إذا أردت.</span><span class="sxs-lookup"><span data-stu-id="709c0-121">The value is copied from the Customer card, but you can change it if you wish.</span></span>  <span data-ttu-id="709c0-122">ويتم أيضا نسخ مجموعة المبيعات لبند أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="709c0-122">The Sales group is also copied to the sales order line.</span></span> <span data-ttu-id="709c0-123">ويمكنك تغيير القيمة بحيث قد تختلف عن القيمة المضمنة في الرأس و/أو بين السطور.</span><span class="sxs-lookup"><span data-stu-id="709c0-123">You can change it so that it can differ from the one in the header and/or between lines.</span></span>  
    * <span data-ttu-id="709c0-124">تمثل القيمة الموجودة في الحقل "مجموعة العمولات" مجموعة قمت بإنشائها لعميل واحد أو أكثر لتتبع العمولات.</span><span class="sxs-lookup"><span data-stu-id="709c0-124">The value in the Commission group field represents a group that you have created for one or more customers with the purpose of tracking commissions.</span></span>   <span data-ttu-id="709c0-125">يتم نسخ القيمة من بطاقة العميل، ولكن يمكنك تغييرها إذا أردت.</span><span class="sxs-lookup"><span data-stu-id="709c0-125">The value is copied from the Customer card, but you can change it if you wish.</span></span>   
11. <span data-ttu-id="709c0-126">في جزء الإجراءات، انقر فوق "خيارات".</span><span class="sxs-lookup"><span data-stu-id="709c0-126">On the Action Pane, click Options.</span></span>
12. <span data-ttu-id="709c0-127">انقر فوق "تغيير طريقة العرض‬".</span><span class="sxs-lookup"><span data-stu-id="709c0-127">Click Change view.</span></span>
13. <span data-ttu-id="709c0-128">انقر فوق "عرض البند".</span><span class="sxs-lookup"><span data-stu-id="709c0-128">Click Line view.</span></span>
14. <span data-ttu-id="709c0-129">في الحقل "رقم الصنف"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="709c0-129">In the Item number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="709c0-130">في القائمة، حدد العنصر الذي قمت بإعداده للعمولات.</span><span class="sxs-lookup"><span data-stu-id="709c0-130">In the list, select the item you have set up for commissions.</span></span> 
16. <span data-ttu-id="709c0-131">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="709c0-131">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="709c0-132">قم بتدوين ملاحظة بالمبلغ الصافي للبند.</span><span class="sxs-lookup"><span data-stu-id="709c0-132">Take note of the line's Net amount.</span></span> <span data-ttu-id="709c0-133">فهو يمثل إيراد المبيعات، والذي يُعد أساس حساب العمولة في هذا المثال.</span><span class="sxs-lookup"><span data-stu-id="709c0-133">It represents the sales revenue, which in this example is the basis for commission calculation.</span></span>  
17. <span data-ttu-id="709c0-134">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="709c0-134">Click Save.</span></span>
18. <span data-ttu-id="709c0-135">في جزء "الإجراءات"، انقر فوق "فاتورة".</span><span class="sxs-lookup"><span data-stu-id="709c0-135">On the Action Pane, click Invoice.</span></span>
19. <span data-ttu-id="709c0-136">انقر فوق "فاتورة".</span><span class="sxs-lookup"><span data-stu-id="709c0-136">Click Invoice.</span></span>
20. <span data-ttu-id="709c0-137">وسّع مقطع "المحددات".</span><span class="sxs-lookup"><span data-stu-id="709c0-137">Expand the Parameters section.</span></span>
21. <span data-ttu-id="709c0-138">في الحقل "الكمية"، حدد "الكل".</span><span class="sxs-lookup"><span data-stu-id="709c0-138">In the Quantity field, select 'All'.</span></span>
22. <span data-ttu-id="709c0-139">حدد "نعم" في الحقل "الترحيل".</span><span class="sxs-lookup"><span data-stu-id="709c0-139">Select Yes in the Posting field.</span></span>
23. <span data-ttu-id="709c0-140">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="709c0-140">Click OK.</span></span>
24. <span data-ttu-id="709c0-141">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="709c0-141">Click OK.</span></span>
    * <span data-ttu-id="709c0-142">قد يستغرق الأمر دقيقة أو نحو ذلك لترحيل الحركة.</span><span class="sxs-lookup"><span data-stu-id="709c0-142">It may take a minute or so to post the transaction.</span></span> <span data-ttu-id="709c0-143">اترك المعالجة تكتمل ولا تغلق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="709c0-143">Allow the processing to complete and don’t close the page.</span></span>  

## <a name="review-the-registered-sales-commissions"></a><span data-ttu-id="709c0-144">مراجعة عمولات المبيعات المسجلة</span><span class="sxs-lookup"><span data-stu-id="709c0-144">Review the registered sales commissions</span></span>
1. <span data-ttu-id="709c0-145">في جزء "الإجراءات"، انقر فوق "فاتورة".</span><span class="sxs-lookup"><span data-stu-id="709c0-145">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="709c0-146">انقر فوق "فاتورة".</span><span class="sxs-lookup"><span data-stu-id="709c0-146">Click Invoice.</span></span>
3. <span data-ttu-id="709c0-147">في جزء "الإجراءات"، انقر فوق "فاتورة".</span><span class="sxs-lookup"><span data-stu-id="709c0-147">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="709c0-148">انقر فوق "حركات العمولات".</span><span class="sxs-lookup"><span data-stu-id="709c0-148">Click Commission transactions.</span></span>
    * <span data-ttu-id="709c0-149">تعرض علامة التبويب "نظرة عامة" البنود التي تمثل مبالغ العمولات التي تُدفع لمندوبي المبيعات المرتبطين بأمر المبيعات المفوتر.</span><span class="sxs-lookup"><span data-stu-id="709c0-149">The Overview tab displays lines representing the commission amounts payable to sales representatives who are associated with the invoiced sales order.</span></span> <span data-ttu-id="709c0-150">فلنراجع التفاصيل.</span><span class="sxs-lookup"><span data-stu-id="709c0-150">Let's review the details.</span></span>     
    * <span data-ttu-id="709c0-151">إذا استخدمتَ الدليل "إعداد قواعد عمولات المبيعات" لإعداد مجموعة مبيعات العمولة، هناك مندوبا مبيعات سيحصلان على عمولة مبيعات وسيتم تقسيم العمولة بينهما بالتساوي.</span><span class="sxs-lookup"><span data-stu-id="709c0-151">If you used the "Set up sales commission rules" guide to set up the Commission sales group, there are two sales people to receive a sales commissions, and the commission is split equally between them.</span></span>  
    * <span data-ttu-id="709c0-152">في هذا المثال، يُحسب إجمالي مبلغ العمولة كنسبة مئوية لإيراد المبيعات (المبلغ الصافي لبند الأمر).</span><span class="sxs-lookup"><span data-stu-id="709c0-152">In this example, the total amount of the commission is calculated as a percentage of the sales revenue (the net amount of order line).</span></span>   
5. <span data-ttu-id="709c0-153">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="709c0-153">Close the page.</span></span>
6. <span data-ttu-id="709c0-154">انقر فوق "الإيصال".</span><span class="sxs-lookup"><span data-stu-id="709c0-154">Click Voucher.</span></span>
    * <span data-ttu-id="709c0-155">يمكنك مراجعة حركات الإيصال لمبالغ العمولات التي تم ترحيلها إلى حسابات مصروفات العمولة والحسابات الدائنة للعمولة المعرفة مسبقاً.</span><span class="sxs-lookup"><span data-stu-id="709c0-155">You can review the voucher transactions for the commission amounts that have been posted to the predefined commission expense and commission payable accounts.</span></span>  


