---
title: معالجة دفتر اليومية العام
description: يُوضح هذا الموضوع القدرات المتوفرة في Microsoft Dynamics 365 Finance التي يمكنها المساعدة في تسهيل معالجة دفتر اليومية العام، والتي يمكنها أيضًا المساعدة في ضمان التقاط البيانات الصحيحة وعدم اختراق التحكم الداخلي.
author: ShylaThompson
manager: AnnBe
ms.date: 08/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c067b7b6cbbcad4456df6037da8ab124776261e9
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771812"
---
# <a name="general-journal-processing"></a><span data-ttu-id="8ec6d-103">معالجة دفتر اليومية العام</span><span class="sxs-lookup"><span data-stu-id="8ec6d-103">General journal processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ec6d-104">يُوضح هذا الموضوع القدرات التي يمكنها المساعدة في تسهيل معالجة دفتر اليومية العام، والتي يمكنها أيضًا المساعدة في ضمان التقاط البيانات الصحيحة وعدم اختراق التحكم الداخلي.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-104">This topic describes capabilities that can help make general journal processing easier, and that can also help ensure that correct data is captured and internal control isn't compromised.</span></span>  

## <a name="journal-names"></a><span data-ttu-id="8ec6d-105">أسماء دفاتر اليومية</span><span class="sxs-lookup"><span data-stu-id="8ec6d-105">Journal names</span></span>

<span data-ttu-id="8ec6d-106">إحدى المناطق الأهم التي يتعين إعدادها هي أسماء دفاتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-106">One of the most important areas to set up is journal names.</span></span> <span data-ttu-id="8ec6d-107">وإنها لفكرة جيدة أن يتم تحديد أسماء دفاتر يومية محددة لكل غرض، مثل الشركات الشقيقة، وتسوية الاستحقاق، وتصحيح الخطأ.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-107">It's a good idea to define specific journal names for each purpose, such as intercompany, accrual adjustment, and error correction.</span></span> <span data-ttu-id="8ec6d-108">ويمكنك تعديل كل اسم دفتر يومية للمساعدة في جعل إدخال البيانات لكل غرض سهلاً وآمنًا.‬</span><span class="sxs-lookup"><span data-stu-id="8ec6d-108">You can tailor each journal name to help make data entry for each purpose easy and secure.</span></span> 

<span data-ttu-id="8ec6d-109">وفي صفحة **أسماء دفاتر اليومية**، يمكنك إعداد العناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="8ec6d-109">On the **Journal names** page, you can set up the following elements:</span></span>

-   <span data-ttu-id="8ec6d-110">**اعتماد سير العمل** – لزيادة المراقبة الداخلية، حدد مهام سير عمل دفتر اليومية التي تضع حدود الأهمية النسبية لخطوات المراجعة والاعتماد، استناداً إلى معايير مثل إجمالي المبلغ المدين.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-110">**Workflow approval** – To increase internal control, define journal workflows that establish materiality limits for review and approval steps, based on criteria such as total debit amount.</span></span> <span data-ttu-id="8ec6d-111">وتقوم بإعداد مهام سير العمل لدفاتر اليومية العامة في صفحة **مهام سير العمل في دفتر الأستاذ العام**.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-111">You set up workflows for the general journals on the **General ledger workflows** page.</span></span>
-   <span data-ttu-id="8ec6d-112">**القيم الافتراضية** – تحديد القيم الافتراضية للحسابات المقابلة والعملة والأبعاد المالية.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-112">**Default values** – Select default values for offset accounts, currency, and financial dimensions.</span></span>
-   <span data-ttu-id="8ec6d-113">**التحكم في دفتر اليومية** – يمكنك إعداد قيود على الشركة ونوع الحساب وأيضًا قيم الشرائح.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-113">**Journal control** – You can set up restrictions on the company and account type, and also the segment values.</span></span> 

<span data-ttu-id="8ec6d-114">**أمثلة**</span><span class="sxs-lookup"><span data-stu-id="8ec6d-114">**Examples**</span></span>

<span data-ttu-id="8ec6d-115">ويمكن استخدام اسم دفتر يومية للتسويات فقط.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-115">A journal name can be used only for adjustments.</span></span> <span data-ttu-id="8ec6d-116">وفي هذه الحالة، يمكنك تحديد أن نوع حساب **دفتر الأستاذ** فقط صالح في كافة الشركات.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-116">In this case, you can specify that only the **Ledger** account type is valid across all companies.</span></span> 

<span data-ttu-id="8ec6d-117">[![أنواع حساب التحكم في دفتر اليومية](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span><span class="sxs-lookup"><span data-stu-id="8ec6d-117">[![Journal control account types](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span></span>

<span data-ttu-id="8ec6d-118">يمكن استخدام اسم دفتر اليومية فقط لمقطع محدد أو لمجموعة حسابات رئيسية.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-118">A journal name can be used only for a specific segment or for a range for main accounts.</span></span> 

<span data-ttu-id="8ec6d-119">[![مقطع التحكم في دفتر اليومية](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span><span class="sxs-lookup"><span data-stu-id="8ec6d-119">[![Journal control segment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span></span>

<span data-ttu-id="8ec6d-120">يتوفر خيار **الإلغاء التلقائي** في دفاتر اليومية العامة.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-120">The **Automatic reversal** option is available in general journals.</span></span> <span data-ttu-id="8ec6d-121">على سبيل المثال، لديك تسوية استحقاق لم تتم فيها معالجة المستند الفعلي، كما هو مبين في التوضيح التالي.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-121">For example, you have an accrual adjustment where the actual document hasn't yet been processed, as shown in the following illustration.</span></span>
<span data-ttu-id="8ec6d-122">[![عكس دفتر اليومية العام](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span><span class="sxs-lookup"><span data-stu-id="8ec6d-122">[![General journal reversing](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span></span> 

<span data-ttu-id="8ec6d-123">يوفر مكون Microsoft Excel الإضافي لإدخال دفتر اليومية مستوى إضافيًا من التشغيل الآلي ويجعل إدخال البيانات أسهل.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-123">The Microsoft Excel add-in for journal entry provides an additional level of automation and makes data entry easier.</span></span> <span data-ttu-id="8ec6d-124">ويتوفر إجراء **فتح البنود في Excel** في صفحتي **دفتر اليومية العام** و**إيصال دفتر اليومية**.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-124">The **Open lines in Excel** action is available on the **General journal** and **Journal voucher** pages.</span></span> 

<span data-ttu-id="8ec6d-125">وفي صفحة **دفاتر اليومية الدورية**، يمكنك إعداد دفاتر اليومية المتكررة لإجراء معالجة دفتر اليومية تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-125">On the **Periodic journals** page, you can set up recurring journals to automate journal processing.</span></span> 

<span data-ttu-id="8ec6d-126">يمكنك استخدام قوالب الإيصال في أي وقت.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-126">You can use voucher templates at any time.</span></span> <span data-ttu-id="8ec6d-127">وفي صفحة **دفاتر اليومية العامة**، يتم العثور على إجراءات **الحفظ** و**تحديد قالب الإيصال** في صفحة **إيصال دفتر اليومية**، ضمن **الوظائف** لبنود الإيصال.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-127">On the **General journals** page, the **Save** and **Select voucher template** actions are found on the **Journal voucher** page, under **Functions** for the voucher lines.</span></span>

## <a name="related-setup"></a><span data-ttu-id="8ec6d-128">الإعداد ذو الصلة</span><span class="sxs-lookup"><span data-stu-id="8ec6d-128">Related setup</span></span>
<span data-ttu-id="8ec6d-129">الإعداد التالي ليس خاصًا بدفاتر اليومية العامة، ولكنه سيساعد على ضمان أن يكون إدخال البيانات صحيحًا وسهلاً.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-129">The following setup isn't specific to general journals, but will help ensure that data entry is correct data and easy.</span></span>

### <a name="main-account"></a><span data-ttu-id="8ec6d-130">الحساب الرئيسي</span><span class="sxs-lookup"><span data-stu-id="8ec6d-130">Main account</span></span>

<span data-ttu-id="8ec6d-131">ويوفر إعداد الحساب الرئيسي يوفر العديد من الخيارات لمعالجة دفتر اليومية العام:</span><span class="sxs-lookup"><span data-stu-id="8ec6d-131">The main account setup provides many options for general journal processing:</span></span>

-   <span data-ttu-id="8ec6d-132">**متطلبات DC/CR** – استخدم هذا الخيار إذا كان حساب رئيسي يقتصر على الحركات المدينة أو الدائنة.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-132">**DC/CR requirement** – Use this option if a main account is limited to debit or credit transactions.</span></span> <span data-ttu-id="8ec6d-133">ويتم التحقق من الإعداد عندما يتم التحقق من صحة دفتر يومية أو ترحيله.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-133">The setup is verified when a journal is validated or posted.</span></span>

-   <span data-ttu-id="8ec6d-134">**الحساب المقابل الافتراضي**</span><span class="sxs-lookup"><span data-stu-id="8ec6d-134">**Default offset account**</span></span>
-   <span data-ttu-id="8ec6d-135">**معلق** - تعليق حساب رئيسي لإدخال البيانات عبر كافة الشركات أو لكيان قانوني/شركة محددة.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-135">**Suspended** – Suspend a main account for data entry across all companies or for a specific company/legal entity.</span></span>
-   <span data-ttu-id="8ec6d-136">**عدم السماح بالإدخال اليدوي** – منع المستخدمين من إدخال قيمة يدوياً للحساب في دفاتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-136">**Do not allow manual entry** – Prevent users from manually entering a value for the account in journals.</span></span>
-   <span data-ttu-id="8ec6d-137">**العملة الافتراضية/التحقق من العملة**</span><span class="sxs-lookup"><span data-stu-id="8ec6d-137">**Default/Validate currency**</span></span>
-   <span data-ttu-id="8ec6d-138">**تجاوز الكيان القانوني** -هذا الإعداد خاص بالكيان القانوني/الشركة المحددة.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-138">**Legal entity override** – This setup is specific to the defined company/legal entity:</span></span>
    -   <span data-ttu-id="8ec6d-139">**ضريبة المبيعات الافتراضية/التحقق منها**</span><span class="sxs-lookup"><span data-stu-id="8ec6d-139">**Default/Validate sales tax**</span></span>
    -   <span data-ttu-id="8ec6d-140">**البعد الافتراضي** - **قيمة غير ثابتة** أو **قيمة ثابتة**.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-140">**Default dimension** – **Not fixed** or **Fixed value**.</span></span> <span data-ttu-id="8ec6d-141">ستساعد **القيمة الثابتة** على ضمان أن جميع عمليات الترحيل لهذا الحساب الرئيسي تستخدم دائماً أي قيمة بعد يتم إعدادها كـ **ثابتة**.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-141">**Fixed value** will help ensure that all postings for this main account always use any dimension value that is set up as **Fixed**.</span></span>
-   <span data-ttu-id="8ec6d-142">**التحقق من صحة الترحيل**</span><span class="sxs-lookup"><span data-stu-id="8ec6d-142">**Posting validation**</span></span>
    -   <span data-ttu-id="8ec6d-143">**التحقق من صحة المستخدم** – يتحكم هذا الخيار في المستخدمين المسموح لهم بالترحيل إلى حساب رئيسي.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-143">**User validation** – This option controls which users are allowed to post to a main account.</span></span>
    -   <span data-ttu-id="8ec6d-144">**التحقق من صحة نوع الترحيل** – يتحكم هذا الخيار في أنواع الترحيل المسموح بها لحساب رئيسي.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-144">**Posting type validation** – This option controls which posting types are allowed for a main account.</span></span>

### <a name="accounting-structures-and-advanced-rules-structures"></a><span data-ttu-id="8ec6d-145">هياكل المحاسبة وهياكل القواعد المتقدمة</span><span class="sxs-lookup"><span data-stu-id="8ec6d-145">Accounting structures and advanced rules structures</span></span>

<span data-ttu-id="8ec6d-146">هياكل المحاسبة وهياكل القواعد المتقدمة تعتبر بالغة الأهمية لضمان أن يتم التقاط البيانات اللازمة للتقارير المالية وتتبع الأداء أثناء معالجة دفتر اليومية العام وأية وثائق.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-146">Accounting structures and advanced rules structures are extremely important for ensuring that the data that is required for financial reporting and performance tracking is captured during general journal processing and any documentation.</span></span> <span data-ttu-id="8ec6d-147">وتسمح لك هياكل المحاسبة وهياكل القواعد المتقدمة بتفصيل تجربة إدخال البيانات.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-147">Accounting structures and advanced rules structures let you tailor the data entry experience.</span></span> <span data-ttu-id="8ec6d-148">ويمكنك السماح بإدخال البيانات فقط للأبعاد المالية ذات الصلة في كل حالة، ويمكن أيضًا فرض متطلب الحصول على البيانات المطلوبة والدقيقة دائماً.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-148">You can allow data entry only for financial dimensions that are relevant in each situation, and can also enforce the requirement that required and accurate data always be captured.</span></span>

<span data-ttu-id="8ec6d-149">لمزيد من المعلومات، راجع الموضوعات التالية:</span><span class="sxs-lookup"><span data-stu-id="8ec6d-149">For more information, see the following topics:</span></span>
- [<span data-ttu-id="8ec6d-150">تخطيط دليل الحسابات</span><span class="sxs-lookup"><span data-stu-id="8ec6d-150">Plan your chart of accounts</span></span>](plan-chart-of-accounts.md) 
- [<span data-ttu-id="8ec6d-151">إنشاء قواعد متقدمة لدفاتر اليومية</span><span class="sxs-lookup"><span data-stu-id="8ec6d-151">Create advanced rules for journals</span></span>](tasks/create-advanced-rules-journals.md)
- [<span data-ttu-id="8ec6d-152">إنشاء إدخال دفتر يومية باستخدام قالب</span><span class="sxs-lookup"><span data-stu-id="8ec6d-152">Create a journal entry using template</span></span>](tasks/create-journal-entry-template.md)
- [<span data-ttu-id="8ec6d-153">إنشاء دفاتر اليومية والتحقق من صحتها</span><span class="sxs-lookup"><span data-stu-id="8ec6d-153">Create and validate journals</span></span>](tasks/create-validate-journals.md)
- [<span data-ttu-id="8ec6d-154">ترحيل دفاتر اليومية الدورية</span><span class="sxs-lookup"><span data-stu-id="8ec6d-154">Post periodic journals</span></span>](tasks/post-periodic-journals.md)
- [<span data-ttu-id="8ec6d-155">‏‫معالجة دفتر يومية توزيع دفتر الأستاذ‬</span><span class="sxs-lookup"><span data-stu-id="8ec6d-155">Process ledger allocation journal</span></span>](tasks/process-ledger-allocation-journal.md)

## <a name="simulate-posting"></a><span data-ttu-id="8ec6d-156">محاكاة الترحيل</span><span class="sxs-lookup"><span data-stu-id="8ec6d-156">Simulate posting</span></span>
<span data-ttu-id="8ec6d-157">يمكنك العثور على **محاكاة الترحيل** في قائمة **التحقق من الصحة** لمعظم دفاتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-157">You can find **Simulate posting** on the **Validate** menu for most journals.</span></span> <span data-ttu-id="8ec6d-158">عند التحقق من صحة دفتر يومية باستخدام وظيفة **التحقق من الصحة**، يقوم النظام باختبار دفتر اليومية لحالات أخطاء معينة.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-158">When you validate a journal using the **Validate** function, the system tests the journal for specific error conditions.</span></span> <span data-ttu-id="8ec6d-159">إذا قمت باستخدام وظيفة **محاكاة الترحيل**، سوف يقوم النظام بتشغيل كافة العمليات المماثلة التي يتم تشغيلها أثناء عملية الترحيل دون ترحيل دفتر اليومية فعليًا.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-159">If you use the **Simulate posting** function, the system runs all of the same processes that are run during posting without actually posting the journal.</span></span> <span data-ttu-id="8ec6d-160">عندئذٍ، يمكنك مراجعة رسائل الترحيل التي يتم عرضها، وإصلاح أي أخطاء يتم العثور عليها، ثم فتح قائمة **الترحيل** لترحيل دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-160">You can then review the posting messages that are displayed, fix any errors that you find, and then open the **Post** menu to post the journal.</span></span> 

<span data-ttu-id="8ec6d-161">**محاكاة الترحيل** غير متوفرة لمعالجة الدفعة.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-161">**Simulate posting** is not available for batch processing.</span></span> <span data-ttu-id="8ec6d-162">ومع ذلك، يوجد كود متوفر لمحاكاة الترحيل في الدفعة، ويمكن للمطورين توسيع الكود لإضافة هذه الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-162">However, there is code available to simulate posting in batch and developers can extend the code to add that functionality.</span></span>  

## <a name="journal-unlock"></a><span data-ttu-id="8ec6d-163">إلغاء تأمين دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="8ec6d-163">Journal unlock</span></span>
<span data-ttu-id="8ec6d-164">يتوفر زر في صفحة دفتر اليومية لإلغاء تأمين دفتر يومية بالحالة "تم تأمينه بواسطة النظام" يتم تعيينه إلى "نعم".</span><span class="sxs-lookup"><span data-stu-id="8ec6d-164">A button is available on the journal page to unlock a journal that has a status of "locked by system" set to Yes.</span></span> <span data-ttu-id="8ec6d-165">يمكن إجراء إلغاء التأمين من قِبل مسؤول النظام الذي قام بتحليل أي وظائف دفعية قيد التنفيذ وقام بتأكيد بأن دفتر اليومية هذا لم يعد قيد المعالجة النشطة بواسطة وظيفة دفعية.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-165">This unlock can be performed by an administrator of the system who has analyzed any executing batch jobs and confirmed this journal is no longer actively being processed by a batch job.</span></span> <span data-ttu-id="8ec6d-166">يتم تمكين هذا الزر بواسطة الميزة المسماة **زر إلغاء تأمين دفتر اليومية** على صفحة **إدارة الميزات**.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-166">This button is enabled by the feature named **Journal Unlock button** on the **Feature management** page.</span></span> 

## <a name="workflow-recall"></a><span data-ttu-id="8ec6d-167">إعادة استدعاء سير العمل</span><span class="sxs-lookup"><span data-stu-id="8ec6d-167">Workflow recall</span></span> 
<span data-ttu-id="8ec6d-168">يتم تمكين القدرة على إعادة استدعاء دفتر اليومية في سير عمل بالحالة "غير قابل للاسترداد" باستخدام زر **سير العمل** الموجود في صفحة **محفوظات سير العمل**.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-168">The ability to recall a journal in a workflow that has a status of "unrecoverable" is enabled by using the **Workflow** button on a journal, and on the **Workflow history** page.</span></span> <span data-ttu-id="8ec6d-169">يتم تمكين ذلك بواسطة الميزة المسماة **إعادة تعيين حالة سير العمل لدفاتر اليومية** في صفحة **إدارة الميزات**.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-169">This is enabled by the feature named **Resetting the workflow status for journals** on the **Feature management** page.</span></span>

## <a name="delete-journal-lines"></a><span data-ttu-id="8ec6d-170">حذف بنود دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="8ec6d-170">Delete Journal Lines</span></span>
<span data-ttu-id="8ec6d-171">يتم تمكين القدرة على حذف كافة بنود دفتر اليومية بسرعة في دفتر يومية تحت **الوظائف** > **حذف بنود دفتر اليومية**.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-171">The ability to delete all journal lines quickly is enabled in a journal under **Functions** > **Delete Journal Lines**.</span></span> <span data-ttu-id="8ec6d-172">لتمكين هذه الميزة، في **إدارة الميزات**، حدد **حذف تحسينات أداء دفتر اليومية**.</span><span class="sxs-lookup"><span data-stu-id="8ec6d-172">To enable this feature, on the **Feature management**, select **Delete journal performance optimizations**.</span></span>