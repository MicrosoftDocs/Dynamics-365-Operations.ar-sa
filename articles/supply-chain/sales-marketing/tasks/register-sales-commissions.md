---
title: تسجيل عمولات المبيعات
description: يشرح هذا الموضوع كيفية حساب عمولة المبيعات وتسجيلها.
author: omulvad
manager: tfehr
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher, CustClassificationGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 57e3b95cb1f4a13b49ddcd336efaeabb12e5defc
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421195"
---
# <a name="register-sales-commissions"></a><span data-ttu-id="b7f25-103">تسجيل عمولات المبيعات</span><span class="sxs-lookup"><span data-stu-id="b7f25-103">Register sales commissions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b7f25-104">يشرح هذا الموضوع كيفية حساب عمولة المبيعات وتسجيلها.</span><span class="sxs-lookup"><span data-stu-id="b7f25-104">This topic explains how sales commissions are calculated and registered.</span></span> <span data-ttu-id="b7f25-105">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF أو باستخدام بياناتك الخاصة.</span><span class="sxs-lookup"><span data-stu-id="b7f25-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="b7f25-106">قبل تشغيل هذا الدليل، قم بتشغيل الدليل المُسمى "إعداد قواعد عمولات المبيعات" للتأكد من وجود توفر إعداد حساب العمولات الضروري بالكامل.</span><span class="sxs-lookup"><span data-stu-id="b7f25-106">Before starting this guide, run the guide called "Set up sales commission rules" to make sure that you have all the necessary commission calculation setup.</span></span>

<span data-ttu-id="b7f25-107">قم بتدوين ملاحظة بالعميل وأرقام الأصناف التي قمت باختيارها لعملية العمولات واستخدمها عندما يُطلبك منك إنشاء أمر مبيعات في هذا الدليل.</span><span class="sxs-lookup"><span data-stu-id="b7f25-107">Take note of the customer and item numbers that you have chosen for the commission process and use them when asked to create a sales order in this guide.</span></span>


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a><span data-ttu-id="b7f25-108">فوترة أمر مبيعات يؤهل مندوب مبيعات لعمولة</span><span class="sxs-lookup"><span data-stu-id="b7f25-108">Invoice a sales order that qualifies a salesperson for a commission</span></span>
1. <span data-ttu-id="b7f25-109">في جزء التنقل، انتقل إلى **الوحدات النمطية > المبيعات والتسويق > أوامر المبيعات > كافة أوامر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="b7f25-109">In the navigation pane, go to **Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="b7f25-110">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="b7f25-110">Select **New**.</span></span>
3. <span data-ttu-id="b7f25-111">في حقل **حساب العميل**، حدد السجل المطلوب من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="b7f25-111">In the **Customer account** field, select the desired record from the drop-down menu.</span></span>
4. <span data-ttu-id="b7f25-112">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b7f25-112">Select **OK**.</span></span>
5. <span data-ttu-id="b7f25-113">في جزء الإجراءات، حدد **خيارات**.</span><span class="sxs-lookup"><span data-stu-id="b7f25-113">On the Action Pane, select **Options**.</span></span>
6. <span data-ttu-id="b7f25-114">حدد **تغيير طريقة العرض**.</span><span class="sxs-lookup"><span data-stu-id="b7f25-114">Select **Change view**.</span></span>
7. <span data-ttu-id="b7f25-115">حدد **طريقة عرض الرأس**.</span><span class="sxs-lookup"><span data-stu-id="b7f25-115">Select **Header view**.</span></span>
8. <span data-ttu-id="b7f25-116">قم بتوسيع قسم **الإعداد**.</span><span class="sxs-lookup"><span data-stu-id="b7f25-116">Expand the **Setup** section.</span></span>

    - <span data-ttu-id="b7f25-117">تمثل القيمة الموجودة في حقل **مجموعة المبيعات** مجموعة معين لها مندوب مبيعات واحد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="b7f25-117">The value in the **Sales group** field represents a group with one or more sales representatives assigned to it.</span></span> <span data-ttu-id="b7f25-118">ويمثل الأشخاص الذين تحتوي عليهم المجموعة من سيحصل على العمولات عند فوترة الأمر، وفقًا للنسب والتوزيع المحدد مسبقاً.</span><span class="sxs-lookup"><span data-stu-id="b7f25-118">The people in the group are the ones who will receive commissions when the order is invoiced, as per predefined rates and distribution.</span></span>   
    - <span data-ttu-id="b7f25-119">يتم نسخ القيمة من بطاقة العميل، ولكن يمكنك تغييرها إذا أردت.</span><span class="sxs-lookup"><span data-stu-id="b7f25-119">The value is copied from the Customer card, but you can change it if you wish.</span></span>  
    - <span data-ttu-id="b7f25-120">ويتم أيضا نسخ مجموعة المبيعات لبند أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="b7f25-120">The Sales group is also copied to the sales order line.</span></span> <span data-ttu-id="b7f25-121">ويمكنك تغيير القيمة بحيث قد تختلف عن القيمة المضمنة في الرأس و/أو بين السطور.</span><span class="sxs-lookup"><span data-stu-id="b7f25-121">You can change it so that it can differ from the one in the header and/or between lines.</span></span>  
    - <span data-ttu-id="b7f25-122">تمثل القيمة الموجودة في حقل **مجموعة العمولات** مجموعة قمت بإنشائها لعميل واحد أو أكثر لتتبع العمولات.</span><span class="sxs-lookup"><span data-stu-id="b7f25-122">The value in the **Commission group** field represents a group that you have created for one or more customers with the purpose of tracking commissions.</span></span>   
    - <span data-ttu-id="b7f25-123">يتم نسخ القيمة من بطاقة العميل، ولكن يمكنك تغييرها إذا أردت.</span><span class="sxs-lookup"><span data-stu-id="b7f25-123">The value is copied from the Customer card, but you can change it if you wish.</span></span>   

9. <span data-ttu-id="b7f25-124">في جزء الإجراءات، حدد **خيارات**.</span><span class="sxs-lookup"><span data-stu-id="b7f25-124">On the Action Pane, select **Options**.</span></span>
10. <span data-ttu-id="b7f25-125">حدد **تغيير طريقة العرض**.</span><span class="sxs-lookup"><span data-stu-id="b7f25-125">Select **Change view**.</span></span>
11. <span data-ttu-id="b7f25-126">حدد **عرض البند**.</span><span class="sxs-lookup"><span data-stu-id="b7f25-126">Select **Line view**.</span></span>
12. <span data-ttu-id="b7f25-127">في القائمة المنسدلة لحقل **رقم الصنف**، حدد الصنف الذي قمت بإعداده للعمولات.</span><span class="sxs-lookup"><span data-stu-id="b7f25-127">In the drop down menu of the **Item number** field, select the item you have set up for commissions.</span></span> 
13. <span data-ttu-id="b7f25-128">في الحقل **الكمية**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="b7f25-128">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="b7f25-129">قم بتدوين ملاحظة بالمبلغ الصافي للبند.</span><span class="sxs-lookup"><span data-stu-id="b7f25-129">Take note of the line's Net amount.</span></span> <span data-ttu-id="b7f25-130">فهو يمثل إيراد المبيعات، والذي يُعد أساس حساب العمولة في هذا المثال.</span><span class="sxs-lookup"><span data-stu-id="b7f25-130">It represents the sales revenue, which in this example is the basis for commission calculation.</span></span>  
14. <span data-ttu-id="b7f25-131">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="b7f25-131">Select **Save**.</span></span>
15. <span data-ttu-id="b7f25-132">في جزء الإجراءات، حدد **فاتورة**.</span><span class="sxs-lookup"><span data-stu-id="b7f25-132">On the Action Pane, select **Invoice**.</span></span>
16. <span data-ttu-id="b7f25-133">حدد **فاتورة**.</span><span class="sxs-lookup"><span data-stu-id="b7f25-133">Select **Invoice**.</span></span>
17. <span data-ttu-id="b7f25-134">قم بتوسيع قسم **المحددات**.</span><span class="sxs-lookup"><span data-stu-id="b7f25-134">Expand the **Parameters** section.</span></span>
18. <span data-ttu-id="b7f25-135">في حقل **الكمية**، حدد **الكل**.</span><span class="sxs-lookup"><span data-stu-id="b7f25-135">In the **Quantity** field, select **All**.</span></span>
19. <span data-ttu-id="b7f25-136">حدد **نعم** في حقل **الترحيل**.</span><span class="sxs-lookup"><span data-stu-id="b7f25-136">Select **Yes** in the **Posting** field.</span></span>
20. <span data-ttu-id="b7f25-137">حدد **موافق**، ثم حدد **موافق** في الجزء التالي.</span><span class="sxs-lookup"><span data-stu-id="b7f25-137">Select **OK**, then select **OK** in the next pane.</span></span> <span data-ttu-id="b7f25-138">قد يستغرق الأمر دقيقة أو نحو ذلك لترحيل الحركة.</span><span class="sxs-lookup"><span data-stu-id="b7f25-138">It may take a minute or so to post the transaction.</span></span> <span data-ttu-id="b7f25-139">اترك المعالجة تكتمل ولا تغلق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b7f25-139">Allow the processing to complete and don't close the page.</span></span>  

## <a name="review-the-registered-sales-commissions"></a><span data-ttu-id="b7f25-140">مراجعة عمولات المبيعات المسجلة</span><span class="sxs-lookup"><span data-stu-id="b7f25-140">Review the registered sales commissions</span></span>
1. <span data-ttu-id="b7f25-141">في جزء الإجراءات، حدد **الفاتورة‬**، ثم حدد **الفاتورة** مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="b7f25-141">On the Action Pane, select **Invoice**, then select **Invoice** again.</span></span>
2. <span data-ttu-id="b7f25-142">في جزء الإجراءات، حدد **الفاتورة‬**، ثم حدد **حركات العمولة‬**.</span><span class="sxs-lookup"><span data-stu-id="b7f25-142">On the Action Pane, select **Invoice**, then select **Commission transactions**.</span></span>

    - <span data-ttu-id="b7f25-143">تعرض علامة التبويب **نظرة عامة** البنود التي تمثل مبالغ العمولات التي تُدفع لمندوبي المبيعات المرتبطين بأمر المبيعات المفوتر.</span><span class="sxs-lookup"><span data-stu-id="b7f25-143">The **Overview** tab displays lines representing the commission amounts payable to sales representatives who are associated with the invoiced sales order.</span></span> <span data-ttu-id="b7f25-144">فلنراجع التفاصيل.</span><span class="sxs-lookup"><span data-stu-id="b7f25-144">Let's review the details.</span></span>  
    - <span data-ttu-id="b7f25-145">إذا استخدمت دليل "إعداد قواعد عمولات المبيعات" لإعداد مجموعة **مبيعات العمولة**، هناك مندوبا مبيعات سيحصلان على عمولة مبيعات وسيتم تقسيم العمولة بينهما بالتساوي.</span><span class="sxs-lookup"><span data-stu-id="b7f25-145">If you used the "Set up sales commission rules" guide to set up the **Commission sales** group, there are two sales people to receive a sales commissions, and the commission is split equally between them.</span></span>  
    - <span data-ttu-id="b7f25-146">في هذا المثال، يُحسب إجمالي مبلغ العمولة كنسبة مئوية لإيراد المبيعات (المبلغ الصافي لبند الأمر).</span><span class="sxs-lookup"><span data-stu-id="b7f25-146">In this example, the total amount of the commission is calculated as a percentage of the sales revenue (the net amount of order line).</span></span>  
3. <span data-ttu-id="b7f25-147">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b7f25-147">Close the page.</span></span>
4. <span data-ttu-id="b7f25-148">حدد **الإيصال**.</span><span class="sxs-lookup"><span data-stu-id="b7f25-148">Select **Voucher**.</span></span> <span data-ttu-id="b7f25-149">يمكنك مراجعة حركات الإيصال لمبالغ العمولات التي تم ترحيلها إلى حسابات مصروفات العمولة والحسابات الدائنة للعمولة المعرفة مسبقاً.</span><span class="sxs-lookup"><span data-stu-id="b7f25-149">You can review the voucher transactions for the commission amounts that have been posted to the predefined commission expense and commission payable accounts.</span></span>  

