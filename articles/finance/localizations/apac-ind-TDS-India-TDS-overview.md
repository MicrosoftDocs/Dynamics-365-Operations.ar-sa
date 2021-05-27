---
title: نظرة عامة على الضريبة الهندية المخصومة في المصدر (TDS)
description: يوفر هذا الموضوع معلومات تفصيلية حول الضريبة الهندية المخصومة في المصدر (TDS). وتغطي وثائق TDS وظيفة هذه الإمكانية.
author: kailiang
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 28ee843036e11bd37b97a065ce53d2eb860c79d9
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023011"
---
# <a name="indian-tax-deducted-at-source-tds-overview"></a><span data-ttu-id="cb343-104">نظرة عامة على الضريبة الهندية المخصومة في المصدر (TDS)</span><span class="sxs-lookup"><span data-stu-id="cb343-104">Indian Tax Deducted at Source (TDS) overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb343-105">يوفر هذا الموضوع معلومات تفصيلية حول الضريبة الهندية المخصومة في المصدر (TDS).</span><span class="sxs-lookup"><span data-stu-id="cb343-105">This topic provides detailed information about Indian Tax Deducted at Source (TDS).</span></span>

<span data-ttu-id="cb343-106">وتغطي وثائق TDS وظيفة هذه الإمكانية.</span><span class="sxs-lookup"><span data-stu-id="cb343-106">The TDS documentation covers the functionality of this capability.</span></span> <span data-ttu-id="cb343-107">كما يوضح كيفية القيام بالإعداد الأساسي لـ TDS، وحساب TDS في الحركات، وإكمال عملية تسوية TDS، وتسجيل أرقام الشهادات TDS، وإنشاء استعلامات TDS وعبارات TDS وشهادات TDS.</span><span class="sxs-lookup"><span data-stu-id="cb343-107">It also explains how to do the basic setup for TDS, calculate TDS on transactions, complete the TDS settlement process, record TDS certificate numbers, and generate TDS inquiries, TDS statements, and TDS certificates.</span></span> <span data-ttu-id="cb343-108">تتضمن الوثائق الموضوعين التاليين:</span><span class="sxs-lookup"><span data-stu-id="cb343-108">The documentation includes the following topics:</span></span>

- [<span data-ttu-id="cb343-109">إعداد TDS الأساسي</span><span class="sxs-lookup"><span data-stu-id="cb343-109">Basic setup for TDS</span></span>](apac-ind-TDS-TDS-ledger-accounts-setup.md)
- [<span data-ttu-id="cb343-110">مصمم المعادلة ووظيفة الحد المستخدمة في حساب TDS</span><span class="sxs-lookup"><span data-stu-id="cb343-110">Formula designer and threshold limit functionality used for TDS calculation</span></span>](apac-ind-TDS-Formula-designer.md)
- [<span data-ttu-id="cb343-111">حساب TDS في الفواتير والمدفوعات والسندات إذنية وحركات بين شركات شقيقة</span><span class="sxs-lookup"><span data-stu-id="cb343-111">Calculation of TDS on invoices, payments, promissory notes, and intercompany transactions</span></span>](apac-ind-TDS-Calculate-TDS-on-invoices-using-journals.md)
- [<span data-ttu-id="cb343-112">عملية تسوية TDS دوريه وتسوية مبالغ TDS لموردي الهيئة الخاصة بـ TDS</span><span class="sxs-lookup"><span data-stu-id="cb343-112">Periodic TDS settlement process and settlement of TDS amounts to TDS authority vendors</span></span>](apac-ind-TDS-Run-the-periodic-TDS-settlement-process.md)
- [<span data-ttu-id="cb343-113">تسجيل وتحديث أرقام وتواريخ شهادات TDS</span><span class="sxs-lookup"><span data-stu-id="cb343-113">Recording and updating TDS certificate numbers and dates</span></span>](apac-ind-TDS-Record-TDS-concession-certificate-numbers.md)

## <a name="introduction-to-tds"></a><span data-ttu-id="cb343-114">مقدمة إلى TDS</span><span class="sxs-lookup"><span data-stu-id="cb343-114">Introduction to TDS</span></span>

<span data-ttu-id="cb343-115">بالنسبة لكل دور من ضرائب الدخل، 1961، يتم خصم ضريبة الدخل في المصدر من قبل مستلم الخدمة في وقت الدفع المقدم أو حساب الاعتماد، أيهما يحدث أولاً.</span><span class="sxs-lookup"><span data-stu-id="cb343-115">Per the Income tax Act, 1961, income tax is deducted at the source by the receiver of the service at the time of advance payment or accounting of credit, whichever occurs first.</span></span> <span data-ttu-id="cb343-116">يجب أن يقوم الشخص الذي يقوم بإجراء الدفع بخصم مبلغ الضريبة ودفع الرصيد الصافي فقط إلى موفر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="cb343-116">The person who makes the payment must deduct the tax amount and pay only the net balance to the provider of the service.</span></span> <span data-ttu-id="cb343-117">يتم تطبيق TDS على الخدمات التي تحددها الحكومة، ويتم خصم الضريبة باستخدام الأسعار التي تحددها الحكومة لفترة.</span><span class="sxs-lookup"><span data-stu-id="cb343-117">TDS is applied on services that the government specifies, and the tax is deducted by using the rates that the government specifies for a period.</span></span> <span data-ttu-id="cb343-118">وتعتمد نسبة الخصم على حالة الكيان الذي يتلقى الدفع أو يوفر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="cb343-118">The rate of deduction is based on the status of the entity that receives the payment or provides the service.</span></span> <span data-ttu-id="cb343-119">تتضمن الحالات **فردي** و **عائلة هندوسية غير مقسمة** (**HUF**) و **شركة** و **مؤسسة** و **رابطة الأشخاص** (**AOP**) و **هيئة الأفراد** (**BOI**) و **السلطة المحلية**.</span><span class="sxs-lookup"><span data-stu-id="cb343-119">Statuses include **Individual**, **Hindu Undivided Family** (**HUF**), **Company**, **Firm**, **Association of Persons** (**AOP**), **Body of Individuals** (**BOI**), and **Local authority**.</span></span>

<span data-ttu-id="cb343-120">تسرد الأقسام التالية الخدمات التي يتم تطبيق TDS عليها، كما هو محدد بواسطة حكومة الهند.</span><span class="sxs-lookup"><span data-stu-id="cb343-120">The following sections list the services that TDS is applied on, as specified by the Government of India.</span></span>

<span data-ttu-id="cb343-121">**المقيمون**</span><span class="sxs-lookup"><span data-stu-id="cb343-121">**Residents**</span></span>

- <span data-ttu-id="cb343-122">الدخل من الرواتب (ضمن القسم 192)</span><span class="sxs-lookup"><span data-stu-id="cb343-122">Income from salaries (Under section 192)</span></span>
- <span data-ttu-id="cb343-123">الدخل من الفائدة على الأمان (ضمن القسم 193)</span><span class="sxs-lookup"><span data-stu-id="cb343-123">Income from interest on securities (Under section 193)</span></span>
- <span data-ttu-id="cb343-124">الدخل من المقسوم (ضمن القسم 194)</span><span class="sxs-lookup"><span data-stu-id="cb343-124">Income from dividend (Under section 194)</span></span>
- <span data-ttu-id="cb343-125">الدخل من الفائدة (ضمن القسم 194A)</span><span class="sxs-lookup"><span data-stu-id="cb343-125">Income from interest (Under section 194A)</span></span>
- <span data-ttu-id="cb343-126">الدخل من اليانصيب أو الألغاز (ضمن القسم 194B)</span><span class="sxs-lookup"><span data-stu-id="cb343-126">Income from lotteries or puzzles (Under section 194B)</span></span>
- <span data-ttu-id="cb343-127">الفوز من سباقات الخيول (ضمن القسم 194BB)</span><span class="sxs-lookup"><span data-stu-id="cb343-127">Winning from horse races etc. (Under section 194BB)</span></span>
- <span data-ttu-id="cb343-128">المقاولون والمقاولون الفرعيون (ضمن القسم 194C)</span><span class="sxs-lookup"><span data-stu-id="cb343-128">Contractors and sub-contractors (Under section 194C)</span></span>
- <span data-ttu-id="cb343-129">عمولة التأمين (ضمن القسم 194D)</span><span class="sxs-lookup"><span data-stu-id="cb343-129">Insurance commission (Under section 194D)</span></span>
- <span data-ttu-id="cb343-130">الدخل من الإيداع ضمن نظام الحفظ القومي (ضمن القسم 194EE)</span><span class="sxs-lookup"><span data-stu-id="cb343-130">Income from deposit under national saving scheme (Under section 194EE)</span></span>
- <span data-ttu-id="cb343-131">الدخل من الأموال المتبادلة أو UTI (ضمن القسم 194F)</span><span class="sxs-lookup"><span data-stu-id="cb343-131">Income from mutual fund or UTI (Under section 194F)</span></span>
- <span data-ttu-id="cb343-132">العمولة أو المكافأة أو الجائزة وما إلى ذلك، عند البيع أو اليانصيب (ضمن القسم 194G)</span><span class="sxs-lookup"><span data-stu-id="cb343-132">Commission, Remuneration, Prize etc., on sale or lottery (Under section 194G)</span></span>
- <span data-ttu-id="cb343-133">دفع العمولة أو السمسرة (ضمن القسم 194H)</span><span class="sxs-lookup"><span data-stu-id="cb343-133">Payment of Commission or brokerage (Under section 194H)</span></span>
- <span data-ttu-id="cb343-134">الإيجار (ضمن القسم 194I)</span><span class="sxs-lookup"><span data-stu-id="cb343-134">Rent (Under section 194I)</span></span>
- <span data-ttu-id="cb343-135">خدمة مهنية (ضمن القسم 194J)</span><span class="sxs-lookup"><span data-stu-id="cb343-135">Professional service (Under section 194J)</span></span>
- <span data-ttu-id="cb343-136">الدخل من الوحدات (ضمن القسم 194K)</span><span class="sxs-lookup"><span data-stu-id="cb343-136">Income from Units (Under section 194K)</span></span>
- <span data-ttu-id="cb343-137">دفع التعويض عند امتلاك خاصية الاستحواذ المحددة (ضمن القسم 194LA)</span><span class="sxs-lookup"><span data-stu-id="cb343-137">Payment of compensation on acquisition of certain immovable property (Under section 194LA)</span></span>

<span data-ttu-id="cb343-138">**غير المقيمين**</span><span class="sxs-lookup"><span data-stu-id="cb343-138">**Non-residents**</span></span>

- <span data-ttu-id="cb343-139">دفعات إلى الرياضيين غير المقيميين أو اتحاد رياضي (ضمن القسم 194E)</span><span class="sxs-lookup"><span data-stu-id="cb343-139">Payments to Non-resident sportsmen or sports association (Under section 194E)</span></span>
- <span data-ttu-id="cb343-140">مبالغ أخرى (ضمن القسم 195)</span><span class="sxs-lookup"><span data-stu-id="cb343-140">Other sums (Under section 195)</span></span>
- <span data-ttu-id="cb343-141">الدخل بالنسبة لوحدات غير المقيمين (ضمن القسم 196A)</span><span class="sxs-lookup"><span data-stu-id="cb343-141">Income in respect of units of non-residents (Under section 196A)</span></span>

    - <span data-ttu-id="cb343-142">الدخل من سندات أو أسهم العملة الأجنبية بالشركة الهندية (ضمن القسم 196C)</span><span class="sxs-lookup"><span data-stu-id="cb343-142">Income from foreign currency bonds or shares of Indian Company (Under section 196C)</span></span>
    - <span data-ttu-id="cb343-143">دخول المستثمرين المؤسسيين الخارجيين من الأمان (ضمن القسم 196D)</span><span class="sxs-lookup"><span data-stu-id="cb343-143">Incomes of foreign institutional investors from securities (Under section 196D)</span></span>
    - <span data-ttu-id="cb343-144">الراتب وكافة الدخول الموجبة الأخرى تحت أي رأس في الدخل (القسم 192)</span><span class="sxs-lookup"><span data-stu-id="cb343-144">Salary and all other positive incomes under any head on income (Section 192)</span></span>
    - <span data-ttu-id="cb343-145">الفائدة على الأمان (القسم 193)</span><span class="sxs-lookup"><span data-stu-id="cb343-145">Interest on securities (Section 193)</span></span>
    - <span data-ttu-id="cb343-146">الفائدة غير المهتمة على الأمان (القسم 194A)</span><span class="sxs-lookup"><span data-stu-id="cb343-146">Interest other than interest on securities (Section 194A)</span></span>
    - <span data-ttu-id="cb343-147">عمليات الدفع للمقاولين والمقاولين الفرعيين (القسم 194C)</span><span class="sxs-lookup"><span data-stu-id="cb343-147">Payments to contractors and sub-contractors (Section 194C)</span></span>
    - <span data-ttu-id="cb343-148">الفوز من اليانصيب أو الكلمات المتقاطعة (القسم 194B)</span><span class="sxs-lookup"><span data-stu-id="cb343-148">Winnings from Lottery or crossword puzzles (Section 194B)</span></span>
    - <span data-ttu-id="cb343-149">الفوز من سباقات الخيول (القسم 194BB)</span><span class="sxs-lookup"><span data-stu-id="cb343-149">Winnings from horse races (Section 194BB)</span></span>
    - <span data-ttu-id="cb343-150">عمولة التأمين تغطي كافة المدفوعات لشركة التأمين الشراء (القسم 194D)</span><span class="sxs-lookup"><span data-stu-id="cb343-150">Insurance Commission covering all payments for procuring Insurance business (Section 194D)</span></span>
    - <span data-ttu-id="cb343-151">أي فائدة غير الفائدة على الأمان في الشركات الدائنة لغير المقيمين لم تكن شركة أو إلى شركة أجنبية (المقطع 195)</span><span class="sxs-lookup"><span data-stu-id="cb343-151">Any interest other than interest on securities payable to non-residents not being a company or to a foreign company (Section 195)</span></span>
    - <span data-ttu-id="cb343-152">الدفع إلى رجل رياضي غير مقيم بما في ذلك لاعب رياضي أو اتحاد أو مؤسسة رياضية.</span><span class="sxs-lookup"><span data-stu-id="cb343-152">Payment to non-resident sportsman including athlete or sports association or institution.</span></span> <span data-ttu-id="cb343-153">في حالة وجود جل رباضي غير مقيم، المدفوعات الخاصة بالإعلانات بالإضافة إلى المقالات الموجودة على أي لعبة/ رياضة بالهند في الجرائد والمجلات وهكذا.</span><span class="sxs-lookup"><span data-stu-id="cb343-153">In case of non-resident sportsman, payments in respect of advertisements as well as articles on any game/sports in India in newspapers, magazines, and so.</span></span> <span data-ttu-id="cb343-154">مضمن (القسم 194E)</span><span class="sxs-lookup"><span data-stu-id="cb343-154">is included (Section 194E)</span></span>
    - <span data-ttu-id="cb343-155">الدفع بالنسبة لعمليات الإيداع في NSS \[نظام التوفير القومي \] (القسم 194EE)</span><span class="sxs-lookup"><span data-stu-id="cb343-155">Payment in respect of deposits under NSS \[National Savings Scheme\] (Section 194EE)</span></span>
    - <span data-ttu-id="cb343-156">دفع على حساب الاسترجاع الخاص بالوحدات من خلال التبرعات المتبادلة أو UTI (القسم ال194f)</span><span class="sxs-lookup"><span data-stu-id="cb343-156">Payment on account of repurchase of Units by Mutual Fund or UTI (Section 194F)</span></span>
    - <span data-ttu-id="cb343-157">دفع العمولة أو السمسرة (القسم 194H)</span><span class="sxs-lookup"><span data-stu-id="cb343-157">Payment for Commission or brokerage (Section 194H)</span></span>
    - <span data-ttu-id="cb343-158">دفع الإيجار (القسم 194I)</span><span class="sxs-lookup"><span data-stu-id="cb343-158">Payment of rent (Section 194I)</span></span>
    - <span data-ttu-id="cb343-159">دفع رسوم للمحترفين أو الخدمات الفنية (القسم 194J)</span><span class="sxs-lookup"><span data-stu-id="cb343-159">Payment of fees for professional or technical services (Section 194J)</span></span>
    - <span data-ttu-id="cb343-160">عمولة للمخزنين والموزعين والمشتريات والبائعين لتذاكر اليانصيب بما في ذلك المكافأة أو الجائزة في مثل هذه التذاكر (القسم 194G)</span><span class="sxs-lookup"><span data-stu-id="cb343-160">Commission to Stockiest, distributors, buyers and sellers of Lottery tickets including remuneration or prize on such tickets (Section 194G)</span></span>
    - <span data-ttu-id="cb343-161">الدخل من الوحدات التي تم شرائها بعملة أجنبية أو مكسب رأس المال على المدى الطويل من نقل مثل تلك الوحدات التي تم شراؤها بالعملة الأجنبية (القسم 196B)</span><span class="sxs-lookup"><span data-stu-id="cb343-161">Income from Units purchased in foreign currency or long-term capital gain arising from the transfer of such Units purchased in foreign currency (Section 196B)</span></span>
    - <span data-ttu-id="cb343-162">الدفع بأي دخل لغير المقيمين للاهتمام أو المقسوم على السندات والأسهم (القسم 196C)</span><span class="sxs-lookup"><span data-stu-id="cb343-162">Payment of any income to non-residents in respect of interest or dividend on bonds and shares (Section 196C)</span></span>

<span data-ttu-id="cb343-163">يتم حساب TDS في المشتريات والمبيعات ومرتجعات المبيعات والإشعارات الدائنة وعمليات امتلاك الأصول الثابتة والدفعات المسبقة والمدفوعات المقدمة والسندات الإذنية وضريبة العمل والحركات بين شركات شقيقة.</span><span class="sxs-lookup"><span data-stu-id="cb343-163">TDS is calculated on purchases, sales, sales returns, credit notes, fixed asset acquisitions, prepayments, advance payments, promissory notes, works tax, and intercompany transactions.</span></span>

> [!NOTE]
> <span data-ttu-id="cb343-164">في سيناريو الضريبة الهندية الحالي، لا يتم حساب TDS في حركات المبيعات.</span><span class="sxs-lookup"><span data-stu-id="cb343-164">In the current Indian tax scenario, TDS isn't calculated on sales transactions.</span></span> <span data-ttu-id="cb343-165">ومع ذلك، يتضمن النظام مخصصًا لحساب TDS القابلة للاسترداد في حركات المبيعات، خاصة للحركات بين الشركات الشقيقة.</span><span class="sxs-lookup"><span data-stu-id="cb343-165">However, the system includes a provision to calculate TDS recoverable on sales transactions, especially for intercompany transactions.</span></span>

<span data-ttu-id="cb343-166">يعتبر حساب TDS دائمًا الحد والحد الاستثنائي الذي يتم تحديده لمكون TDS.</span><span class="sxs-lookup"><span data-stu-id="cb343-166">The calculation of TDS always considers the threshold and the exception threshold that are defined for the TDS component.</span></span>

<span data-ttu-id="cb343-167">يجب تشغيل عملية تسوية TDS الدورية، ويجب تسوية المدفوعات الخاصة بـ TDS على موردي الهيئة الخاصة بـ TDS.</span><span class="sxs-lookup"><span data-stu-id="cb343-167">The periodic TDS settlement process must be run, and the TDS payments must be settled to TDS authority vendors.</span></span>

<span data-ttu-id="cb343-168">يمكن تسجيل أرقام الشهادات وتواريخها لشهادات TDS التي يتم استلامها من الموردين أو العملاء وتحديثها.</span><span class="sxs-lookup"><span data-stu-id="cb343-168">The certificate numbers and dates for TDS certificates that are received from vendors or customers can be recorded and updated.</span></span> <span data-ttu-id="cb343-169">بالإضافة إلى ذلك، يمكن إنشاء نموذج 26Q وكشوفات نموذج 27Q الربع سنوي، وشهادة نموذج 16A لـ TDS، في التمويل.</span><span class="sxs-lookup"><span data-stu-id="cb343-169">Additionally, Form 26Q and Form 27Q quarterly statements, and the Form 16A certificate for TDS, can be generated in Finance.</span></span>

## <a name="setting-up-and-working-with-tds"></a><span data-ttu-id="cb343-170">الإعداد والعمل باستخدام TDS</span><span class="sxs-lookup"><span data-stu-id="cb343-170">Setting up and working with TDS</span></span>

<span data-ttu-id="cb343-171">وفيما يلي نظرة عامة على العملية الخاصة بإعداد TDS والعمل باستخدامه:</span><span class="sxs-lookup"><span data-stu-id="cb343-171">Here is an overview of the process for setting up and working with TDS:</span></span>

1. <span data-ttu-id="cb343-172">**إعداد TDS:**</span><span class="sxs-lookup"><span data-stu-id="cb343-172">**TDS setup:**</span></span>

    - <span data-ttu-id="cb343-173">إعداد المعلمة:</span><span class="sxs-lookup"><span data-stu-id="cb343-173">Parameter setup:</span></span>

        - <span data-ttu-id="cb343-174">في معلمات دفتر الأستاذ العام، قم بتنشيط المعلمات المرتبطة بـ TDS.</span><span class="sxs-lookup"><span data-stu-id="cb343-174">In General ledger parameters, activate parameters that are related to TDS.</span></span>
        - <span data-ttu-id="cb343-175">في معلمات دفتر الأستاذ العام، قم بإعداد التسلسل الرقمي لمدفوعات ضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="cb343-175">In General ledger parameters, set up the number sequence for withholding tax payments.</span></span>
        - <span data-ttu-id="cb343-176">إعداد المعلمات في الحسابات الدائنة والحسابات المدينة.</span><span class="sxs-lookup"><span data-stu-id="cb343-176">Set up parameters in Accounts payable and Accounts receivable.</span></span>

    - <span data-ttu-id="cb343-177">الإعداد الأساسي:</span><span class="sxs-lookup"><span data-stu-id="cb343-177">Basic setup:</span></span>

        - <span data-ttu-id="cb343-178">قم بإعداد أرقام تسجيل TDS لشركة وعملاء وموردين.</span><span class="sxs-lookup"><span data-stu-id="cb343-178">Set up TDS registration numbers for a company, customers, and vendors.</span></span>
        - <span data-ttu-id="cb343-179">إعداد مجموعات مكون TDS.</span><span class="sxs-lookup"><span data-stu-id="cb343-179">Set up TDS component groups.</span></span>
        - <span data-ttu-id="cb343-180">قم بإعداد مكونات TDS، وأرفق مجموعات المكون TDS بها، وتحديد الحد والحد الاستثنائي الخاصين بهما.</span><span class="sxs-lookup"><span data-stu-id="cb343-180">Set up TDS components, attach TDS component groups to them, and define the threshold and exception threshold for them.</span></span>
        - <span data-ttu-id="cb343-181">إعداد هيئات TDS.</span><span class="sxs-lookup"><span data-stu-id="cb343-181">Set up TDS authorities.</span></span>
        - <span data-ttu-id="cb343-182">قم بإعداد فترات تسوية TDS.</span><span class="sxs-lookup"><span data-stu-id="cb343-182">Set up TDS settlement periods.</span></span>
        - <span data-ttu-id="cb343-183">قم بإعداد أكواد ضريبة TDS، وقم بإرفاق مكونات TDS بها.</span><span class="sxs-lookup"><span data-stu-id="cb343-183">Set up TDS tax codes, and attach TDS components to them.</span></span>
        - <span data-ttu-id="cb343-184">قم بإعداد مجموعات ضريبة TDS، وقم بإرفاق أكواد ضريبة TDS بها.</span><span class="sxs-lookup"><span data-stu-id="cb343-184">Set up TDS tax groups, and attach TDS tax codes to them.</span></span>
        - <span data-ttu-id="cb343-185">في "مصمم المعادلة"، قم بتحديد معادلة لحساب TDS لمجموعة TDS.</span><span class="sxs-lookup"><span data-stu-id="cb343-185">In the formula designer, define a formula to calculate TDS for a TDS group.</span></span>
        - <span data-ttu-id="cb343-186">قم بتسجيل أرقام شهادات تخويل TDS.</span><span class="sxs-lookup"><span data-stu-id="cb343-186">Record TDS concession certificate numbers.</span></span>

    - <span data-ttu-id="cb343-187">حسابات دفتر الأستاذ وإعداد الشركة:</span><span class="sxs-lookup"><span data-stu-id="cb343-187">Ledger accounts and company setup:</span></span>

        - <span data-ttu-id="cb343-188">قم بإعداد حسابات دفتر الأستاذ الدائنة والمدينة.</span><span class="sxs-lookup"><span data-stu-id="cb343-188">Set up TDS payable and receivable ledger accounts.</span></span>
        - <span data-ttu-id="cb343-189">قم بإعداد خصم ضريبي ورقم حساب المجموعة (TAN) وفئة نوع خاصم للشركة.</span><span class="sxs-lookup"><span data-stu-id="cb343-189">Set up a Tax Deduction and Collection Account Number (TAN) and a deductor type category for the company.</span></span>

    - <span data-ttu-id="cb343-190">إعداد آخر:</span><span class="sxs-lookup"><span data-stu-id="cb343-190">Other setup:</span></span>

        - <span data-ttu-id="cb343-191">قم بإعداد جدول دفع يتضمن توزيع TDS.</span><span class="sxs-lookup"><span data-stu-id="cb343-191">Set up a payment schedule that includes TDS allocation.</span></span>
        - <span data-ttu-id="cb343-192">قم بإعداد نوع رسوم الدفع للمدفوعات إلى هيئة TDS.</span><span class="sxs-lookup"><span data-stu-id="cb343-192">Set up a payment fee type for payments to the TDS authority.</span></span>
        - <span data-ttu-id="cb343-193">قم بإعداد معلومات حول مجموعات TDS وأرقام الحساب الدائمة (PAN) وأرقام TAN للموردين والعملاء.</span><span class="sxs-lookup"><span data-stu-id="cb343-193">Set up information about TDS groups, permanent account numbers (PANs), and TANs for vendors and customers.</span></span>

2. <span data-ttu-id="cb343-194">**حساب TDS في الحركات.**</span><span class="sxs-lookup"><span data-stu-id="cb343-194">**Calculation of TDS in transactions:**</span></span>

    - <span data-ttu-id="cb343-195">الفواتير والمدفوعات</span><span class="sxs-lookup"><span data-stu-id="cb343-195">Invoices and payments</span></span>
    - <span data-ttu-id="cb343-196">السندات الإذنية</span><span class="sxs-lookup"><span data-stu-id="cb343-196">Promissory notes</span></span>
    - <span data-ttu-id="cb343-197">دفعات مقدم</span><span class="sxs-lookup"><span data-stu-id="cb343-197">Advance payments</span></span>
    - <span data-ttu-id="cb343-198">دفعات مسبقة</span><span class="sxs-lookup"><span data-stu-id="cb343-198">Prepayments</span></span>

3. <span data-ttu-id="cb343-199">**تسوية TDS:**</span><span class="sxs-lookup"><span data-stu-id="cb343-199">**TDS settlement:**</span></span>

    - <span data-ttu-id="cb343-200">عملية تسوية TDS الدورية</span><span class="sxs-lookup"><span data-stu-id="cb343-200">Periodic TDS settlement process</span></span>
    - <span data-ttu-id="cb343-201">تسوية مدفوعات TDS لموردي هيئة TDS وإنشاء TDS في تشالان</span><span class="sxs-lookup"><span data-stu-id="cb343-201">Settlement of TDS payments to TDS authority vendors and generation of TDS challan</span></span>

4. <span data-ttu-id="cb343-202">**استعلامات TDS وكشوف الحسابات والشهادات:**</span><span class="sxs-lookup"><span data-stu-id="cb343-202">**TDS inquiries, statements, and certificate:**</span></span>

    - <span data-ttu-id="cb343-203">تسجيل وتحديث أرقام وتواريخ شهادات TDS.</span><span class="sxs-lookup"><span data-stu-id="cb343-203">Record and update TDS certificate numbers and dates.</span></span>
    - <span data-ttu-id="cb343-204">إنشاء استعلام TDS واستعلام TDS الذي تم ترحيله.</span><span class="sxs-lookup"><span data-stu-id="cb343-204">Generate a TDS inquiry and a posted TDS inquiry.</span></span>
    - <span data-ttu-id="cb343-205">قم بإنشاء نموذج 27A والنموذج 26Q، والنموذج 27Q TDS والكشوفات الربع سنوية لـ TDS.</span><span class="sxs-lookup"><span data-stu-id="cb343-205">Generate Form 27A, Form 26Q, and Form 27Q TDS and e-TDS quarterly statements.</span></span>
    - <span data-ttu-id="cb343-206">قم بإنشاء شهادة نموذج 16A TDS.</span><span class="sxs-lookup"><span data-stu-id="cb343-206">Generate a Form 16A TDS certificate.</span></span>
