---
title: كشوف حساب البيع بالتجزئة
description: يصف هذا الموضوع كيفية إنشاء وترحيل كشوف الحسابات.
author: ashishmsft
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: df9c62a2-6f13-4a08-bdca-07d041172c1b
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: 63cad6b2f7240bb14fe7a9237498c0140df77774
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025019"
---
# <a name="retail-statements"></a><span data-ttu-id="7d839-103">كشوف البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="7d839-103">Retail statements</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7d839-104">في Dynamics 365 Retail، يتم استخدام عملية ترحيل كشف الحساب لحساب الحركات التي تحدث في Cloud point of sale (POS) أو Modern POS (MPOS)</span><span class="sxs-lookup"><span data-stu-id="7d839-104">In Dynamics 365 Retail, the statement posting process is used to account for the transactions that occur in Cloud point of sale (POS) or Modern POS (MPOS).</span></span> <span data-ttu-id="7d839-105">تستخدم عملية ترحيل كشف الحساب جدول توزيع لاستخراج مجموعة من حركات نقاط البيع إلى عميل المقر الرئيسي (HQ).</span><span class="sxs-lookup"><span data-stu-id="7d839-105">The statement posting process uses the distribution schedule to pull a set of POS transactions into the headquarters (HQ) client.</span></span> <span data-ttu-id="7d839-106">تُستخدم المعلمات التي تم تعريفها في الصفحتين **معلمات البيع بالتجزئة‬** و**المتاجر** لتحديد الحركات المستخرجة لكشوف حساب فردية.</span><span class="sxs-lookup"><span data-stu-id="7d839-106">The parameters that are defined on the **Retail parameters** and **Stores** pages are used to select the transactions that are pulled into individual statements.</span></span>

<span data-ttu-id="7d839-107">يوضح الرسم التوضيحي التالي عملية ترحيل كشف الحساب.</span><span class="sxs-lookup"><span data-stu-id="7d839-107">The following illustration shows the statement posting process.</span></span> <span data-ttu-id="7d839-108">في هذه العملية، ترسل الحركات التي يتم تسجيلها في نقطة البيع إلى العميل باستخدام مجدول البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="7d839-108">In this process, transactions that are recorded in the POS are transmitted to the client by using the Retail scheduler.</span></span> <span data-ttu-id="7d839-109">بعد تلقي العميل الحركات، يمكنك إنشاء وحساب وترحيل كشف الحركات للمتجر.</span><span class="sxs-lookup"><span data-stu-id="7d839-109">After the client receives the transactions, you can create, calculate, and post the transaction statement for the store.</span></span>

<span data-ttu-id="7d839-110">[![عملية ترحيل كشف حساب](./media/retail-statements.png)](./media/retail-statements.png)</span><span class="sxs-lookup"><span data-stu-id="7d839-110">[![Statement posting process](./media/retail-statements.png)](./media/retail-statements.png)</span></span>

## <a name="creating-and-posting-statements"></a><span data-ttu-id="7d839-111">إنشاء الكشوف وتحديثها</span><span class="sxs-lookup"><span data-stu-id="7d839-111">Creating and posting statements</span></span>

<span data-ttu-id="7d839-112">يمكنك إنشاء كشف حساب يدويًا أو باستخدام معالجات الدُفعة التي يتم إعدادها للتشغيل بشكل دوري طوال اليوم.</span><span class="sxs-lookup"><span data-stu-id="7d839-112">You can create a statement manually or by using batch processes that you set up to run periodically throughout the day.</span></span> <span data-ttu-id="7d839-113">في كلتا الحالتين، يتم استخدام الخطوات التالية لإنشاء وترحيل الكشوف.</span><span class="sxs-lookup"><span data-stu-id="7d839-113">In both cases, the following steps are used to create and post statements.</span></span>

### <a name="create-the-statement"></a><span data-ttu-id="7d839-114">‎إنشاء كشف حساب</span><span class="sxs-lookup"><span data-stu-id="7d839-114">Create the statement</span></span>

<span data-ttu-id="7d839-115">تحدد هذه الخطوة المتجر الذي يتم إنشاء كشف حساب فيه يدويًا.</span><span class="sxs-lookup"><span data-stu-id="7d839-115">This step identifies the store that the statement is manually created for.</span></span> <span data-ttu-id="7d839-116">إذا قمت بتكوين معالجة دُفعة، يمكنك تلقائيًا إنشاء البيانات لكافة المتاجر، استنادًا إلى الجدول الذي تقوم بتحديده.</span><span class="sxs-lookup"><span data-stu-id="7d839-116">If you configure a batch process, you can automatically create statements for all stores, based on a schedule that you define.</span></span>

### <a name="calculate-the-statement"></a><span data-ttu-id="7d839-117">حساب كشف الحساب</span><span class="sxs-lookup"><span data-stu-id="7d839-117">Calculate the statement</span></span>

<span data-ttu-id="7d839-118">في هذه الخطوة، يتم تحديد بنود الحركة استنادًا إلى المعايير المحددة لكل متجر في الصفحتين **معلمات البيع بالتجزئة‬** و**المتاجر‬**.</span><span class="sxs-lookup"><span data-stu-id="7d839-118">In this step, the transaction lines are selected based on criteria that are defined for each store on the **Retail parameters** and **Stores** pages.</span></span> <span data-ttu-id="7d839-119">على هاتين الصفحتين، يمكنك تحديد المعايير وكيفية حساب الحركات.</span><span class="sxs-lookup"><span data-stu-id="7d839-119">On these pages, you define the criteria and specify how the transactions are calculated.</span></span> <span data-ttu-id="7d839-120">لعرض قائمة بالحركات التي تم تضمينها في كشف الحساب قبل حساب كشف الحساب، استخدم صفحة **الحركات**.</span><span class="sxs-lookup"><span data-stu-id="7d839-120">To view a list of the transactions that are included in the statement before you calculate the statement, use the **Transactions** page.</span></span>

<span data-ttu-id="7d839-121">تستخدم عملية حساب كشف الحساب إقرارات الدفع من السجلات كمبلغ محتسب.</span><span class="sxs-lookup"><span data-stu-id="7d839-121">Statement calculation uses tender declarations from the registers as the counted amount.</span></span> <span data-ttu-id="7d839-122">بدلاً من ذلك، يمكن إدخال المبلغ المحسوب يدويًا.</span><span class="sxs-lookup"><span data-stu-id="7d839-122">Alternatively, you can enter the counted amount manually.</span></span> <span data-ttu-id="7d839-123">يعرض كشف الحساب الفرق بين مبلغ المبيعات للحركات والمبلغ الفعلي المحتسب في أساليب الدفع.</span><span class="sxs-lookup"><span data-stu-id="7d839-123">The statement shows the difference between the sales amount for the transactions and the actual counted amount in all payment methods.</span></span> <span data-ttu-id="7d839-124">يتم ترحيل كشف الحساب فقط إذا كان هذا الفرق أقل من الحد الأقصى لفرق الترحيل المحدد للمتجر.</span><span class="sxs-lookup"><span data-stu-id="7d839-124">The statement is posted only if this difference is less than the maximum posting difference that is defined for the store.</span></span>

> [!NOTE]
> <span data-ttu-id="7d839-125">تستخدم عملية كشف الحساب التسلسل الرقمي العالمي.</span><span class="sxs-lookup"><span data-stu-id="7d839-125">The statement calculation process uses the global number sequence.</span></span>

<span data-ttu-id="7d839-126">عند حساب كشف حساب عبارة، يتضمن الحساب المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="7d839-126">When you calculate a statement, the calculation includes the following tasks:</span></span>

- <span data-ttu-id="7d839-127">بالنسبة إل نطاق التاريخ المحدد، ضع علامة على الحركات التي لم يتم تضمينها في كشف حساب سابق.</span><span class="sxs-lookup"><span data-stu-id="7d839-127">For the selected date range, mark transactions that weren't included in a previous statement calculation.</span></span>
- <span data-ttu-id="7d839-128">حساب إجمالي المبالغ التي تم الدفع لها في الحركات المحددة.</span><span class="sxs-lookup"><span data-stu-id="7d839-128">Calculate the total amounts that were tendered in the selected transactions.</span></span> <span data-ttu-id="7d839-129">يتم عرض النتائج في بنود كشف الحساب، استنادًا إلى طريقة كشف الحساب:</span><span class="sxs-lookup"><span data-stu-id="7d839-129">The results are shown on the statement lines, depending on the statement method:</span></span>

    - <span data-ttu-id="7d839-130">إذا كانت طريقة كشف الحساب **إجمالي**، فسيتم إنشاء بند لكل طريقة دفع في الحركات المحددة.</span><span class="sxs-lookup"><span data-stu-id="7d839-130">If the statement method is **Total**, a line is created for each payment method in the selected transactions.</span></span>
    - <span data-ttu-id="7d839-131">إذا كانت طريقة كشف الحساب **فريق العمل‬**، فسيتم إنشاء بند لكل طريقة دفع في الحركات التي يتم تنفيذها من قِبل عضو الفريق المحدد.</span><span class="sxs-lookup"><span data-stu-id="7d839-131">If the statement method is **Staff**, a line is created for each payment method in transactions that were performed by the selected staff member.</span></span>
    - <span data-ttu-id="7d839-132">إذا كانت طريقة كشف الحساب **محطة POS الطرفية‬**، فسيتم إنشاء بند لكل طريقة دفع في الحركات التي يتم تنفيذها على السجل المحدد.</span><span class="sxs-lookup"><span data-stu-id="7d839-132">If the statement method is **POS terminal**, a line is created for each payment method in transactions that were performed on the selected register.</span></span>
    - <span data-ttu-id="7d839-133">إذا كانت طريقة كشف الحساب **الوردية‬**، فسيتم إنشاء بند لكل طريقة دفع في الحركات التي يتم تنفيذها خلال الوردية‬.</span><span class="sxs-lookup"><span data-stu-id="7d839-133">If the statement method is **Shift**, a line is created for each payment method in transactions that were performed during a shift.</span></span>

<span data-ttu-id="7d839-134">إذا كانت خانة الاختيار **التقسيم حسب طريقة كشف الحساب‬** محددة في صفحة **المتاجر**، فسيتم إنشاء كشف حساب منفصل استنادًا إلى القيمة المحددة في حقل **طريقة كشف الحساب**.</span><span class="sxs-lookup"><span data-stu-id="7d839-134">If the **Split by Statement method** check box is selected on the **Stores** page, a separate statement is created based on the value that is selected in the **Statement method** field.</span></span>

<span data-ttu-id="7d839-135">إذا تم تمديد ساعات العمل في المتجر بعد منتصف الليل، فيمكنك تكوين ترحيل كشف الحساب بحيث يستند إلى نهاية يوم العمل بدلاً من نهاية يوم التقويم.</span><span class="sxs-lookup"><span data-stu-id="7d839-135">If your store's operating hours extend past midnight, you can configure statement posting so that it's based on the end of the business day instead of the end of the calendar day.</span></span>

<span data-ttu-id="7d839-136">في صفحة **المتاجر**، على علامة التبويب السريعة **كشف الحساب/الإقفال‬**، في الحقل **نهاية يوم العمل‬** أدخل الوقت الذي يجب تسجيل آخر حركة فيه لتضمينها في كشف حساب يوم العمل.</span><span class="sxs-lookup"><span data-stu-id="7d839-136">On the **Stores** page, on the **Statement/closing** FastTab, in the **End of business day** field, enter the time that the last transaction must be recorded to be included in the business day's statement.</span></span> <span data-ttu-id="7d839-137">حدد خانة الاختيار **الترحيل كيوم عمل‬** لترحيل الحركات في نفس يوم العمل.</span><span class="sxs-lookup"><span data-stu-id="7d839-137">Select the **Post as business day** check box to post the transactions within the same business day.</span></span> <span data-ttu-id="7d839-138">عند ترحيل كشف الحساب، يمكن تضمين الحركات التي تم تسجيلها في نفس يوم العمل، في نفس أمر المبيعات، حتى في حال حدوث بعض الحركات قبل منتصف الليل وحركات أخرى بعد منتصف الليل.</span><span class="sxs-lookup"><span data-stu-id="7d839-138">When the statement is posted, transactions that are recorded within the same business day can be included on the same sales order, even if some transactions occur before midnight and other transactions occur after midnight.</span></span>

#### <a name="example-post-a-statement-for-a-business-day-that-extends-over-two-calendar-days"></a><span data-ttu-id="7d839-139">على سبيل المثال: ترحيل كشف حساب ليوم عمل يمتد على مدى يومين من أيام التقويم</span><span class="sxs-lookup"><span data-stu-id="7d839-139">Example: Post a statement for a business day that extends over two calendar days</span></span>

<span data-ttu-id="7d839-140">هناك متجر مفتوح بين الساعة 8:00 صباحًا و3:00 صباحًا، وتم تحديد خانة الاختيار **الترحيل كيوم عمل‬** في تكوين المتجر.</span><span class="sxs-lookup"><span data-stu-id="7d839-140">A store is open between 8:00 AM and 3:00 AM, and the **Post as business day** check box is selected in the store's configuration.</span></span> <span data-ttu-id="7d839-141">بتاريخ 31 مايو، يسجل المتجر حركات بين الساعة 8:00 صباحًا ومنتصف الليل.</span><span class="sxs-lookup"><span data-stu-id="7d839-141">On May 31, the store records transactions between 8:00 AM and midnight.</span></span> <span data-ttu-id="7d839-142">يسجل المتجر أيضًا حركات بين 12:01 صباحًا و3:00 صباحًا في 1 يونيو.</span><span class="sxs-lookup"><span data-stu-id="7d839-142">The store also records transactions between 12:01 AM and 3:00 AM on June 1.</span></span>

<span data-ttu-id="7d839-143">عند يقوم المتجر بترحيل كشف حسابه لإغلاق يوم العمل، يتضمن أمر المبيعات الذي يتم إنشاؤه كل الحركات التي تم تسجيلها أثناء ساعات العمل أي بين 8:00 صباحًا و3:00 صباحًا، حتى وإن وقعت هذه الحركات في يومي 31 مايو و1 يونيو.</span><span class="sxs-lookup"><span data-stu-id="7d839-143">When the store posts its statement for the close of the business day, the sales order that is generated includes all transactions that were recorded between the business hours of 8:00 AM and 3:00 AM, even though the transactions occurred on two days, May 31 and June 1.</span></span>

<span data-ttu-id="7d839-144">إذا تم إلغاء تحديد خانة الاختيار **الترحيل كيوم عمل** للمتجر نفسه، يتم إنشاء أوامر مبيعات منفصلة عندما يقوم المتجر بترحيل كشف الحساب الخاص به لإغلاق يوم العمل.</span><span class="sxs-lookup"><span data-stu-id="7d839-144">If the **Post as business day** check box is cleared for the same store, separate sales orders are generated when the store posts its statement for the close of the business day.</span></span> <span data-ttu-id="7d839-145">يتضمن أحد أوامر المبيعات الحركات التي تم تسجيلها أثناء ساعات العمل أي من 8:00 صباحًا إلى منتصف ليل يوم 31 مايو، ويتضمن أمر المبيعات الثاني الحركات التي تم تسجيلها بين ساعات العمل 12:01 صباحًا و3:00 صباحًا في 1 يونيو.</span><span class="sxs-lookup"><span data-stu-id="7d839-145">One sales order includes the transactions that were recorded between the business hours of 8:00 AM and midnight on May 31, and the second sales order includes the transactions that were recorded between the business hours of 12:01 AM and 3:00 AM on June 1.</span></span>

> [!NOTE]
> <span data-ttu-id="7d839-146">قبل إنشاء كشوف الحساب، يجب عليك إغلاق التحولات في فترة كشف الحساب.</span><span class="sxs-lookup"><span data-stu-id="7d839-146">Before you can create statements, you should close the shifts in the statement period.</span></span>

### <a name="post-the-statement"></a><span data-ttu-id="7d839-147">ترحيل كشف الحساب</span><span class="sxs-lookup"><span data-stu-id="7d839-147">Post the statement</span></span>

<span data-ttu-id="7d839-148">عند ترحيل كشف حساب، يتم إنشاء أوامر مبيعات وفواتير لمبيعات البيع بالتجزئة في كشف الحساب.</span><span class="sxs-lookup"><span data-stu-id="7d839-148">When you post a statement, sales orders and invoices are created for the retail sales in the statement.</span></span>

- <span data-ttu-id="7d839-149">يتم تجميع المبيعات النقدية والمبالغ في أمر مبيعات، وتتم فوترتها للعميل الافتراضي الذي تم تعيينه إلى المتجر.</span><span class="sxs-lookup"><span data-stu-id="7d839-149">Cash and carry sales are aggregated onto one sales order, and are invoiced for the default customer who is assigned to the store.</span></span>
- <span data-ttu-id="7d839-150">تقوم مبيعات التجزئة التي تم إضافة عميل إلى الحركة من أجلها في نقطة بيع Retail بإنشاء أوامر مبيعات وفواتير منفصلة، واحد لكل عميل فردي.</span><span class="sxs-lookup"><span data-stu-id="7d839-150">Retail sales for which a customer was added to the transaction in Retail POS generate separate sales orders and invoices, one for each unique customer.</span></span>

<span data-ttu-id="7d839-151">يتم تلقائيًا إنشاء دفاتر دفع يومية للمدفوعات في كشف الحساب، ويتم تحديث المخزون لمتجر نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="7d839-151">Payment journals are automatically created for the payments in the statement, and the inventory is updated for the POS store.</span></span>
