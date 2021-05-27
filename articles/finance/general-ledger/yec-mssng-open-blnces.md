---
title: إقفال نهاية السنة يفتقد إلى الأرصدة الافتتاحية
description: يشرح هذا الموضوع سبب فقد الأرصدة الافتتاحية عند إقفال سنة، وكيفية إعادة تكوين هذه الأرصدة إذا كانت مفقودة.
author: kweekley
ms.date: 05/12/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 045d0bf11b11c9a353858ce3ca82c698dbceea7c
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028547"
---
# <a name="year-end-close-missing-opening-balances"></a><span data-ttu-id="d94f4-103">إقفال نهاية السنة يفتقد إلى الأرصدة الافتتاحية</span><span class="sxs-lookup"><span data-stu-id="d94f4-103">Year-end close missing opening balances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d94f4-104">يشرح هذا الموضوع سبب فقد الأرصدة الافتتاحية عند إقفال سنة، وكيفية إعادة تكوين هذه الأرصدة إذا كانت مفقودة.</span><span class="sxs-lookup"><span data-stu-id="d94f4-104">This topic explains why opening balances might be missing when you close a year, and how to rebuild those balances if they are missing.</span></span>

### <a name="symptom"></a><span data-ttu-id="d94f4-105">العَرَضْ</span><span class="sxs-lookup"><span data-stu-id="d94f4-105">Symptom</span></span>

<span data-ttu-id="d94f4-106">لماذا لا توجد أي أرصدة افتتاحية بعد تشغيل إقفال نهاية السنة لدفتر الأستاذ العام؟</span><span class="sxs-lookup"><span data-stu-id="d94f4-106">Why are there no beginning balances after running the General ledger year-end close?</span></span> 

### <a name="resolution"></a><span data-ttu-id="d94f4-107">الحل</span><span class="sxs-lookup"><span data-stu-id="d94f4-107">Resolution</span></span>

<span data-ttu-id="d94f4-108">فيما يلي بعض الأشياء التي يجب التحقق منها إذا كنت قد أقفلت سنة في دفتر الأستاذ العام، ثم قمت بإنشاء ميزان مراجعة لا يعرض الأرصدة الافتتاحية للسنة المالية التالية.</span><span class="sxs-lookup"><span data-stu-id="d94f4-108">Here are things to check if you've closed a year in General ledger, and then generated a trial balance that doesn't display opening balances for the next fiscal year.</span></span>

<span data-ttu-id="d94f4-109">في حالة تعيين حقل **تراجع عن الإقفال السابق‬‏‫** إلى **نعم**، يتم إلغاء إقفال نهاية السنة السابقة لنفس السنة المالية.</span><span class="sxs-lookup"><span data-stu-id="d94f4-109">If the **Undo previous close** field is set to **Yes**, the previous year-end close for the same fiscal year is being reversed.</span></span> <span data-ttu-id="d94f4-110">عند تشغيل عملية لإلغاء إقفال نهاية السنة، سيتم حذف جميع إدخالات كل من الأرصدة الختامية والأرصدة الافتتاحية، كما لو لم يتم إقفال السنة مطلقًا.</span><span class="sxs-lookup"><span data-stu-id="d94f4-110">When running a process to reverse the year-end close, all entries for both closing and opening balances will be deleted, as if the year had never been closed.</span></span> <span data-ttu-id="d94f4-111">يتم حذف الإيصالات أيضًا.</span><span class="sxs-lookup"><span data-stu-id="d94f4-111">The vouchers are also deleted.</span></span> <span data-ttu-id="d94f4-112">لن يتم تشغيل عملية إقفال نهاية السنة تلقائيًا مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="d94f4-112">The year-end close process will not run again automatically.</span></span> <span data-ttu-id="d94f4-113">يجب عليك بدء العملية مرة أخرى، ولكن هذه المرة بتحديث **تراجع عن الإقفال السابق‬‏‫** إلى **لا**.</span><span class="sxs-lookup"><span data-stu-id="d94f4-113">You must start the process again, this time updating the **Undo previous close** option to **No**.</span></span>

<span data-ttu-id="d94f4-114">تمت تغطية هذا السيناريو في موضوع الأسئلة الشائعة حول إقفال نهاية السنة.</span><span class="sxs-lookup"><span data-stu-id="d94f4-114">This scenario is covered in the year-end close FAQ topic.</span></span> <span data-ttu-id="d94f4-115">لمزيد من المعلومات، راجع [الأسئلة الشائعة حول أنشطة نهاية السنة](faq-year-end-activities.md).</span><span class="sxs-lookup"><span data-stu-id="d94f4-115">For more information, see [Year-end activities FAQ](faq-year-end-activities.md).</span></span>

### <a name="symptom"></a><span data-ttu-id="d94f4-116">العَرَضْ</span><span class="sxs-lookup"><span data-stu-id="d94f4-116">Symptom</span></span>

<span data-ttu-id="d94f4-117">قمتُ بتشغيل إقفال نهاية السنة عن طريق تعيين خيار **تراجع عن الإقفال السابق** إلى **لا**، ومازلت لا أمتلك أرصدة افتتاحية للسنة المالية.</span><span class="sxs-lookup"><span data-stu-id="d94f4-117">I ran year-end close with the **Undo previous close** option set to **No**, and I still do not have opening balances for my fiscal year.</span></span>

### <a name="resolution"></a><span data-ttu-id="d94f4-118">الحل</span><span class="sxs-lookup"><span data-stu-id="d94f4-118">Resolution</span></span>

<span data-ttu-id="d94f4-119">تحقق أولاً من حالة وظيفة الدُفعة.</span><span class="sxs-lookup"><span data-stu-id="d94f4-119">First check the status of the batch job.</span></span> <span data-ttu-id="d94f4-120">يتضمن إقفال السنة عددًا من المهام المنفصلة، ولكن الخطوة الأكثر أهميةً هي مهمة الدُفعة مع وصف المهمة **الخطوة 5.0.0**.</span><span class="sxs-lookup"><span data-stu-id="d94f4-120">Closing a year includes a number of separate tasks, but the most critical step is the batch task with the task description **Step 5.0.0**.</span></span> <span data-ttu-id="d94f4-121">يتم ترحيل الحركات الافتتاحية، واختياريًا الحركات الختامية، إلى دفتر الأستاذ العام أثناء هذه الخطوة.</span><span class="sxs-lookup"><span data-stu-id="d94f4-121">Posting the opening transactions, and optionally the closing transactions, to General ledger takes place during this step.</span></span> 

<span data-ttu-id="d94f4-122">[![قائمة سجلات الدُفعات](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)</span><span class="sxs-lookup"><span data-stu-id="d94f4-122">[![Batch history list](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)</span></span>

<span data-ttu-id="d94f4-123">إذا انتهت هذه الخطوة بنجاح ولكنك لا ترى الأرصدة الافتتاحية في صفحة **الاستعلام عن ميزان المراجعة** (**دفتر الأستاذ العام > الاستعلامات والتقارير > ميزات المراجعة**)، فراجع نتائج وظيفة دُفعة إقفال نهاية السنة لمعرفة ما إذا كانت خطوة إعادة إنشاء الأرصدة قد اكتملت بنجاح.</span><span class="sxs-lookup"><span data-stu-id="d94f4-123">If this step ended successfully but you don’t see opening balances on the **Trial balance inquiry** page (**General ledger > Inquires and reports > Trial balance**), review the results of the year-end close batch job to see if the Rebuild balances step completed successfully.</span></span>

<span data-ttu-id="d94f4-124">[![نتائج وظيفة دُفعة إقفال نهاية السنة](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)</span><span class="sxs-lookup"><span data-stu-id="d94f4-124">[![Results of year-end close batch job](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)</span></span>

<span data-ttu-id="d94f4-125">إذا فشلت هذه الخطوة لأي سبب من الأسباب، فمن المحتمل أن يكون قد تم ترحيل الحركات الافتتاحية (والختامية اختياريًا) بنجاح.</span><span class="sxs-lookup"><span data-stu-id="d94f4-125">If this step has failed for any reason, the opening (and optionally closing) transactions were likely posted successfully.</span></span> <span data-ttu-id="d94f4-126">يمكنك التحقق من ترحيل حركات دفتر الأستاذ العام بنجاح باستخدام صفحة **الاستعلام عن حركات الإيصالات** عن طريق تحديد رقم الإيصال والتاريخ الموفرين في مربع حوار إقفال نهاية السنة للسنة التي أقفلتها، (**دفتر الأستاذ العام > الاستعلامات والتقارير > حركات الإيصالات**).</span><span class="sxs-lookup"><span data-stu-id="d94f4-126">You can verify that the General ledger transactions were posted successfully using the **Voucher transactions inquiry** page by specifying the voucher number and date provided on the year-end close dialog for the year that you closed, (**General Ledger > Inquiries and reports > Voucher transactions**).</span></span>

<span data-ttu-id="d94f4-127">[![الاستعلام عن حركات الإيصالات](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)</span><span class="sxs-lookup"><span data-stu-id="d94f4-127">[![Voucher transactions inquiry](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)</span></span>

<span data-ttu-id="d94f4-128">إذا كانت الإيصالات الافتتاحية (والختامية اختياريًا) موجودة، فلن تحتاج إلى إجراء إقفال نهاية السنة مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="d94f4-128">If the opening (and optionally closing) vouchers are present, you don’t need to run the year-end close again.</span></span> <span data-ttu-id="d94f4-129">بدلاً من ذلك، راجع القسم التالي للحصول على معلومات حول كيفية المُضي قدمًا.</span><span class="sxs-lookup"><span data-stu-id="d94f4-129">Instead refer to the next section for information about how to move forward.</span></span>

### <a name="symptom"></a><span data-ttu-id="d94f4-130">العَرَضْ</span><span class="sxs-lookup"><span data-stu-id="d94f4-130">Symptom</span></span>

<span data-ttu-id="d94f4-131">فشلت خطوة "إعادة إنشاء الأرصدة" في إقفال نهاية السنة، هل أحتاج إلى إعادة إجراء عملية إقفال نهاية السنة بالكامل؟</span><span class="sxs-lookup"><span data-stu-id="d94f4-131">The “Rebuild balances” step in the year-end close failed, do I need to re-run the entire year-end close process?</span></span>

### <a name="resolution"></a><span data-ttu-id="d94f4-132">الحل</span><span class="sxs-lookup"><span data-stu-id="d94f4-132">Resolution</span></span>

<span data-ttu-id="d94f4-133">تعمل خطوة إعادة إنشاء الأرصدة على تحديث أرصدة دفتر الأستاذ العام التي يتم استخدامها عند إنشاء استعلام عن ميزان المراجعة.</span><span class="sxs-lookup"><span data-stu-id="d94f4-133">The Rebuild balances step updates the General ledger balances that are used when the Trial balance inquiry is generated.</span></span>  <span data-ttu-id="d94f4-134">إنها الخطوة الأخيرة في عملية إقفال نهاية السنة.</span><span class="sxs-lookup"><span data-stu-id="d94f4-134">It is the final step in the year-end close process.</span></span>  <span data-ttu-id="d94f4-135">إذا كانت هذه الخطوة هي الخطوة الوحيدة التي فشلت، فقد تم ترحيل حركات دفتر الأستاذ العام بنجاح.</span><span class="sxs-lookup"><span data-stu-id="d94f4-135">If this step is the only step that failed, the General ledger transactions have posted successfully.</span></span>  <span data-ttu-id="d94f4-136">لا تحتاج إلى إجراء إقفال نهاية السنة مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="d94f4-136">You do not need to run the year-end close again.</span></span> <span data-ttu-id="d94f4-137">يمكنك إجراء العملية لإعادة تكوين الأرصدة يدويًا باستخدام صفحة **مجموعات الأبعاد المالية** (**دفتر الأستاذ العام > مخطط الحسابات > الأبعاد > مجموعات الأبعاد المالية**).</span><span class="sxs-lookup"><span data-stu-id="d94f4-137">You can run the process to rebuild the balances manually using the **Financial dimension sets** page (**General ledger > Chart of accounts > Dimensions > Financial dimension sets**).</span></span>

<span data-ttu-id="d94f4-138">[![زر إعادة إنشاء الأرصدة في صفحة مجموعات الأبعاد المالية](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)</span><span class="sxs-lookup"><span data-stu-id="d94f4-138">[![Rebuild balances button on Financial dimension sets page](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)</span></span>

<span data-ttu-id="d94f4-139">إذا كانت هذه الخطوة تستغرق وقتًا طويلاً للمعالجة، فإننا نوصي بمراجعة أفضل الممارسات لمجموعات الأبعاد المالية كما هو موضح في [أفضل الممارسات لتحديث مجموعات الأبعاد المالية](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets).</span><span class="sxs-lookup"><span data-stu-id="d94f4-139">If this step takes a long time to process, we recommend reviewing the best practices for financial dimension sets as described in [Best practices for updating Financial dimension sets](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets).</span></span> 

