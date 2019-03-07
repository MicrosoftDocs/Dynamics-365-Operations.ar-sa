---
title: تكوين إدارة المصروفات
description: توضح هذه المقالة الاعتبارات والقرارات التي يجب أن تتخذها خلال عملية التخطيط قبل تكوين إدارة المصروفات في Microsoft Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ac9959a4ee66e52ead5050897403602e407ca10
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "322020"
---
# <a name="configure-expense-management"></a><span data-ttu-id="c75f4-103">تكوين إدارة المصروفات</span><span class="sxs-lookup"><span data-stu-id="c75f4-103">Configure expense management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c75f4-104">يصف هذا الموضوع الاعتبارات والقرارات التي يجب أن تتخذها خلال عملية التخطيط قبل تكوين إدارة المصروفات في Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c75f4-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="c75f4-105">في إدارة المصروفات، يمكنك تخزين معلومات حول طرق الدفع وطلبات السفر وتقارير المصروفات والسياسات، وغير ذلك.</span><span class="sxs-lookup"><span data-stu-id="c75f4-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="c75f4-106">لأن العديد من القرارات التي تتخذها عندما تخطط للتكوين الخاص بك لإدارة المصروفات مبنية على الهيكل المالي والتدرج الهرمي للمؤسسة الخاصة بك، فإنه يجب عليك الرجوع إلى وثائق التخطيط لتلك المناطق.</span><span class="sxs-lookup"><span data-stu-id="c75f4-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="c75f4-107">المصروفات المشتركة بين الشركات الشقيقة</span><span class="sxs-lookup"><span data-stu-id="c75f4-107">Intercompany expenses</span></span>

<span data-ttu-id="c75f4-108">وعندما تقوم بتمكين المصروفات بين الشركات الشقيقة، فأنت تسمح للكيانات القانونية والموظفين بتحمل المصروفات نيابةً عن كيان قانوني آخر، وتحصيل المدفوعات من الكيان القانوني للتوظيف ضمن مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="c75f4-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="c75f4-109">على سبيل المثال، يكمل أحد الموظفين في الكيان القانوني أ مشروعًا للكيان القانوني ب، ويتكبد المشروع مصروفات تتعلق بالسفر.</span><span class="sxs-lookup"><span data-stu-id="c75f4-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="c75f4-110">وإذا تم تمكين المصروفات بين الشركات الشقيقة، فباستطاعة الموظف عندئذٍ تقديم تقرير مصروفات يقوم بترحيل المصروفات إلى الكيان القانوني ب، ويجب عندئذٍ دفع المصروفات بواسطة الكيان القانوني أ. وإذا لم يكن لدى مؤسستك كيانات قانونية متعددة، فلن تحتاج إلى تمكين المصروفات بين الشركات الشقيقة.</span><span class="sxs-lookup"><span data-stu-id="c75f4-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="c75f4-111">**القرار:** هل تريد تمكين المصروفات بين الشركات الشقيقة؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="c75f4-112">الإدارة المالية</span><span class="sxs-lookup"><span data-stu-id="c75f4-112">Financial management</span></span>

<span data-ttu-id="c75f4-113">تتكامل إدارة المصروفات مع الإدارة المالية للمؤسسة الخاصة بك بشدة.</span><span class="sxs-lookup"><span data-stu-id="c75f4-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="c75f4-114">سوف تستند الكثير من تكوينات دارة المصروفات إلى القرارات التي اتخذتها حول الموارد المالية للمؤسسة.</span><span class="sxs-lookup"><span data-stu-id="c75f4-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="c75f4-115">تصف الأقسام التالية مختلف المجالات التي تتطلب التخطيط واتخاذ القرارات استنادًا إلى القرارات المالية لمؤسستك والتوجيه المقدم من فريق القيادة.</span><span class="sxs-lookup"><span data-stu-id="c75f4-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="c75f4-116">المصروفات اليومية</span><span class="sxs-lookup"><span data-stu-id="c75f4-116">Per diems</span></span>

<span data-ttu-id="c75f4-117">يجب عليك تحديد الموظف في اليومية الذي توفره المؤسسة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="c75f4-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="c75f4-118">ولأنه يتم عادةً استخدام اليومية لتغطية المصاريف، مثل الوجبات والإقامة والمصروفات العرضية الأخرى، فإنه يمكنك إنشاء قواعد لبدلات المصروفات اليومية التي تقدمها مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="c75f4-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="c75f4-119">يمكن تعيين معدلات المصروفات اليومية استنادًا إلى الفترات الزمنية من العام وموقع السفر أو كليهما.</span><span class="sxs-lookup"><span data-stu-id="c75f4-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="c75f4-120">وعند إنشاء قاعدة اليومية، يمكنك تحديد أن النسبة المئوية لمعدل المصروف اليومي سيتم اقتطاعها إذا ما تلقى العامل وجبات أو خدمات مجانية.</span><span class="sxs-lookup"><span data-stu-id="c75f4-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="c75f4-121">ويمكنك أيضًا تحديد مستويات المعدل اليومي لتعيين الحد الأدنى والحد الأقصى لعدد الساعات التي يمكن خلالها تطبيق معدل المصروف اليومي على سفر العامل.</span><span class="sxs-lookup"><span data-stu-id="c75f4-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="c75f4-122">**القرارات:**</span><span class="sxs-lookup"><span data-stu-id="c75f4-122">**Decisions:**</span></span>

- <span data-ttu-id="c75f4-123">قواعد المصروف اليومي الافتراضية للأيام الأولى والأخيرة:</span><span class="sxs-lookup"><span data-stu-id="c75f4-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="c75f4-124">ما هو الحد الأدنى لعدد الساعات الذي يمكن لموظف المطالبة به ليوم ولا يزال يتلقى المصروف اليومي؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="c75f4-125">هل هناك تخفيض في المبلغ المقدم لوجبات الطعام لليوم الأول والأخير؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="c75f4-126">في حال وجود تخفيض، ما هي النسبة المئوية للتخفيض؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="c75f4-127">هل هناك تخفيض في المبلغ المقدم للفندق لليوم الأول والأخير؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="c75f4-128">في حال وجود تخفيض، ما هي النسبة المئوية للتخفيض؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="c75f4-129">هل هناك تخفيض في المبلغ المقدم للمصروفات الأخرى التي يتم تكبدها في اليومين الأول والأخير؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="c75f4-130">في حال وجود تخفيض، ما هي النسبة المئوية للتخفيض؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="c75f4-131">قواعد المصروف اليومي الافتراضية:</span><span class="sxs-lookup"><span data-stu-id="c75f4-131">Default per diem rules:</span></span>

    - <span data-ttu-id="c75f4-132">هل هناك انخفاض في النسبة المئوية لبدل المصروف اليومي لكل وجبة، على سبيل المثال، الوجبة مجانية؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="c75f4-133">في حال وجود تخفيض، ما هي النسبة المئوية للتخفيض لكل وجبة؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="c75f4-134">هل يتم حساب تخفيض الوجبة كل يوم، ام للرحلة الواحدة، أم بعدد الوجبات يوميًا؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="c75f4-135">هل يجب تقريب مبالغ المصروفات اليومية بالطريقة العادية أو تقريبها لأعلى؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="c75f4-136">هل يتم حساب المصاريف اليومية على أساس فترة الـ 24 ساعة أم يوم التقويم؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="c75f4-137">قواعد المصروف اليومي التي تستند إلى الموقع:</span><span class="sxs-lookup"><span data-stu-id="c75f4-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="c75f4-138">هل تختلف معدلات المصروف اليومي وفقًا للموقع؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="c75f4-139">ما هي المواقع المضمنة؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-139">What locations are included?</span></span>
    - <span data-ttu-id="c75f4-140">في حالة اختلاف معدلات المصروف اليومي وفقًا للموقع، لكل موقع، ما مبلغ النسبة المئوية المتوفر لأنواع المصروفات التالية:</span><span class="sxs-lookup"><span data-stu-id="c75f4-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="c75f4-141">الوجبات</span><span class="sxs-lookup"><span data-stu-id="c75f4-141">Meals</span></span>
        - <span data-ttu-id="c75f4-142">فندق</span><span class="sxs-lookup"><span data-stu-id="c75f4-142">Hotel</span></span>
        - <span data-ttu-id="c75f4-143">مصروفات أخرى</span><span class="sxs-lookup"><span data-stu-id="c75f4-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="c75f4-144">حسابات ودفاتر يومية إدارة المصروفات</span><span class="sxs-lookup"><span data-stu-id="c75f4-144">Expense management journals and accounts</span></span>

<span data-ttu-id="c75f4-145">تتطلب إدارة المصروفات استخدام حسابات ودفاتر يومية متعددة.</span><span class="sxs-lookup"><span data-stu-id="c75f4-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="c75f4-146">ويجب أن تقرر، على سبيل المثال، استخدام نفس الحساب للسلف النقدية ومنازعات بطاقة الائتمان أو لا.</span><span class="sxs-lookup"><span data-stu-id="c75f4-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="c75f4-147">**القرارات:**</span><span class="sxs-lookup"><span data-stu-id="c75f4-147">**Decisions:**</span></span>

- <span data-ttu-id="c75f4-148">ما دفتر يومية الأستاذ الذي يتم ترحيل تقارير المصروفات المعتمدة إليه؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="c75f4-149">ما الحساب الذي يتم استخدامه للسلف النقدية؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="c75f4-150">هل يجب ترحيل السلف النقدية مباشرةً؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="c75f4-151">طرق الدفع</span><span class="sxs-lookup"><span data-stu-id="c75f4-151">Payment methods</span></span>

<span data-ttu-id="c75f4-152">عند السماح للموظفين بتحمل المصروفات باسم شركتك، يجب عليك تحديد طرق الدفع التي يُسمح للموظفين باستخدامها.</span><span class="sxs-lookup"><span data-stu-id="c75f4-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="c75f4-153">على سبيل المثال، قد تسمح للموظفين باستخدام النقدية أو بطاقة ائتمان شركة.</span><span class="sxs-lookup"><span data-stu-id="c75f4-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="c75f4-154">كما قد تسمح للموظفين باستخدام بطاقات الائتمان الشخصية، ومن ثم تعويض الموظفين.</span><span class="sxs-lookup"><span data-stu-id="c75f4-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="c75f4-155">يجب اتخاذ القرارات التالية لكل طريقة دفع تسمح بها.</span><span class="sxs-lookup"><span data-stu-id="c75f4-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="c75f4-156">**القرارات:**</span><span class="sxs-lookup"><span data-stu-id="c75f4-156">**Decisions:**</span></span>

- <span data-ttu-id="c75f4-157">ما طرق الدفع المسموح بها؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="c75f4-158">مَن الذي يملك مصروفات طريقة الدفع؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="c75f4-159">هل هناك نوع حساب مقابل؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-159">Is there an offset account type?</span></span> <span data-ttu-id="c75f4-160">إذا كان هناك نوع حساب مقابل، فما هو؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="c75f4-161">إذا كان هناك حساب مقابل، فما الحساب؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="c75f4-162">إذا كانت طريقة الدفع بطاقة ائتمان، فهل يجب استخدام طريقة الدفع فقط في الحركات المستوردة؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="c75f4-163">الفئات المشتركة وفئات المصروفات</span><span class="sxs-lookup"><span data-stu-id="c75f4-163">Expense categories and shared categories</span></span>

<span data-ttu-id="c75f4-164">عند قيام الموظفين بإنشاء تقرير مصروفات، يجب أن يكون كل مصروف يقومون بتسجيله مقترنًا بفئة مصروفات.</span><span class="sxs-lookup"><span data-stu-id="c75f4-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="c75f4-165">ويتم اشتقاق فئات المصروفات من الفئات المشتركة التي يمكن مشاركتها عبر الكيانات القانونية في مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="c75f4-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="c75f4-166">ويمكن أيضًا مشاركة هذه الفئات في محاسبة وإدارة المشاريع، استنادًا إلى الطريقة التي تم بها تعريف مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="c75f4-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="c75f4-167">استنادًا إلى تعريف مؤسستك والتوجيه من فريق التنفيذ، حدد ما إذا كان سيتم استخدام الفئات المستخدمة في إدارة المصروفات في إدارة المصروفات فقط أو ما إذا كان يجب مشاركتها بين إدارة ومحاسبة المشروع وإدارة المصروفات.</span><span class="sxs-lookup"><span data-stu-id="c75f4-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="c75f4-168">ولاحظ أنه يمكن مشاركة هذه الفئات بين المشروع والمصروفات أو المشروع والإنتاج، ولكن ليس بين المصروفات والإنتاج.</span><span class="sxs-lookup"><span data-stu-id="c75f4-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="c75f4-169">يجب اتخاذ القرارات التالية لكل فئة مصروفات.</span><span class="sxs-lookup"><span data-stu-id="c75f4-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="c75f4-170">**القرارات:**</span><span class="sxs-lookup"><span data-stu-id="c75f4-170">**Decisions:**</span></span>

- <span data-ttu-id="c75f4-171">ما المقصود بفئة المصروفات؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-171">What is the expense category?</span></span> <span data-ttu-id="c75f4-172">تتضمن الأمثلة فئات الرحلات أو الفنادق أو المسافة المقطوعة بالميل.</span><span class="sxs-lookup"><span data-stu-id="c75f4-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="c75f4-173">هل يمكن أيضًا استخدام فئات المصروفات في محاسبة وإدارة المشروع؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="c75f4-174">ما نوع المصروفات؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-174">What is the expense type?</span></span>
- <span data-ttu-id="c75f4-175">ما طريقة الدفع الافتراضية لفئة المصروفات؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="c75f4-176">هل يجب تفصيل المصروفات في فئة المصروفات إلى بنود؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="c75f4-177">ما الحساب الافتراضي الرئيسي لفئة المصروفات؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="c75f4-178">ما مجموعة ضريبة مبيعات الصنف الافتراضية لفئة المصروفات؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="c75f4-179">هل يُسمح بطرق الدفع الإضافية لفئة المصروفات؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="c75f4-180">في حال تم السماح بطرق دفع إضافية، فما هي؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="c75f4-181">هل توجد فئات فرعية في فئة المصروفات هذه؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="c75f4-182">إذا كان هناك فئات فرعية، فيجب أيضًا اتخاذ القرارات التالية:</span><span class="sxs-lookup"><span data-stu-id="c75f4-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="c75f4-183">هل يتم استبعاد الفئات الفرعية من استرداد الضريبة؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="c75f4-184">ما مجموعة ضريبة مبيعات الصنف في الفئات الفرعية؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="c75f4-185">إذا تم أيضًا استخدام فئة المصروفات في محاسبة وإدارة المشروع، فأجب على الأسئلة المتبقية.</span><span class="sxs-lookup"><span data-stu-id="c75f4-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="c75f4-186">وإلا، فانتقل إلى القسم التالي.</span><span class="sxs-lookup"><span data-stu-id="c75f4-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="c75f4-187">ما حسابات التكاليف التي سيتم استخدامها للمصروفات التالية؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="c75f4-188">التكلفة</span><span class="sxs-lookup"><span data-stu-id="c75f4-188">Cost</span></span>
    - <span data-ttu-id="c75f4-189">توزيع الرواتب</span><span class="sxs-lookup"><span data-stu-id="c75f4-189">Payroll allocation</span></span>
    - <span data-ttu-id="c75f4-190">الأعمال تحت التنفيذ – قيمة التكلفة</span><span class="sxs-lookup"><span data-stu-id="c75f4-190">WIP-cost value</span></span>
    - <span data-ttu-id="c75f4-191">التكلفة - الصنف</span><span class="sxs-lookup"><span data-stu-id="c75f4-191">Cost-item</span></span>
    - <span data-ttu-id="c75f4-192">الأعمال تحت التنفيذ - قيمة التكلفة - الصنف</span><span class="sxs-lookup"><span data-stu-id="c75f4-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="c75f4-193">الخسارة المستحقة</span><span class="sxs-lookup"><span data-stu-id="c75f4-193">Accrued loss</span></span>
    - <span data-ttu-id="c75f4-194">الأعمال تحت التنفيذ - الخسارة المستحقة</span><span class="sxs-lookup"><span data-stu-id="c75f4-194">WIP-accrued loss</span></span>

- <span data-ttu-id="c75f4-195">ما حسابات الإيرادات التي سيتم استخدامها لما يلي؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="c75f4-196">إيراد تمت فوترته</span><span class="sxs-lookup"><span data-stu-id="c75f4-196">Invoiced revenue</span></span>
    - <span data-ttu-id="c75f4-197">الإيراد المستحق – قيمة المبيعات</span><span class="sxs-lookup"><span data-stu-id="c75f4-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="c75f4-198">الأعمال تحت التنفيذ – قيمة المبيعات</span><span class="sxs-lookup"><span data-stu-id="c75f4-198">WIP-sales value</span></span>
    - <span data-ttu-id="c75f4-199">الإيراد المستحق - الإنتاج</span><span class="sxs-lookup"><span data-stu-id="c75f4-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="c75f4-200">الأعمال تحت التنفيذ - الإنتاج</span><span class="sxs-lookup"><span data-stu-id="c75f4-200">WIP-production</span></span>
    - <span data-ttu-id="c75f4-201">الإيراد المستحق - الأرباح</span><span class="sxs-lookup"><span data-stu-id="c75f4-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="c75f4-202">الأعمال تحت التنفيذ - الأرباح</span><span class="sxs-lookup"><span data-stu-id="c75f4-202">WIP-profit</span></span>
    - <span data-ttu-id="c75f4-203">الإيراد المستحق - الاشتراك</span><span class="sxs-lookup"><span data-stu-id="c75f4-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="c75f4-204">الأعمال تحت التنفيذ - الاشتراكات</span><span class="sxs-lookup"><span data-stu-id="c75f4-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="c75f4-205">الضرائب</span><span class="sxs-lookup"><span data-stu-id="c75f4-205">Taxes</span></span>

<span data-ttu-id="c75f4-206">بالنسبة للضرائب المتعلقة بالمصروفات، يجب عليك تحديد ما يتم تضمينه أو تمكينه في تقارير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="c75f4-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="c75f4-207">**القرارات:**</span><span class="sxs-lookup"><span data-stu-id="c75f4-207">**Decisions:**</span></span>

- <span data-ttu-id="c75f4-208">هل يتم تضمين ضريبة المبيعات في مبالغ المصروفات؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="c75f4-209">هل يجب تمكين استرداد الضريبة في المصروفات؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="c75f4-210">عندما تم التخطيط دفتر الأستاذ العام، أو إذا قررت تطبيق ضريبة المبيعات في الولايات المتحدة واستخدام القواعد الضريبية، فلا يمكنك تمكين استرداد الضريبة على المصروفات.‬</span><span class="sxs-lookup"><span data-stu-id="c75f4-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="c75f4-211">(تطبيق ضريبة المبيعات في الولايات المتحدة واستخدام القواعد الضريبية، عيّن الخيار **تطبيق قواعد الضرائب لضريبة المبيعات** إلى **نعم**.)</span><span class="sxs-lookup"><span data-stu-id="c75f4-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="c75f4-212">السياسات</span><span class="sxs-lookup"><span data-stu-id="c75f4-212">Policies</span></span>

<span data-ttu-id="c75f4-213">من خلال إنشاء سياسات تقارير المصروفات، يمكنك مساعدة مؤسستك على توفير الوقت والمال عندما يتحمل الموظفون المصروفات بالنيابة عنها.</span><span class="sxs-lookup"><span data-stu-id="c75f4-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="c75f4-214">تساعد السياسات على ضمان بقاء الموظفين في حدود الميزانية وتوفير كافة المعلومات المطلوبة وإنفاق الأموال عند الحاجة إليها.</span><span class="sxs-lookup"><span data-stu-id="c75f4-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="c75f4-215">ويجب عليك اتخاذ القرارات التالية لكل سياسة تقرير مصروفات وكل سياسة موافقة على تقرير مصروفات تقوم بإنشائها.</span><span class="sxs-lookup"><span data-stu-id="c75f4-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="c75f4-216">**القرارات:**</span><span class="sxs-lookup"><span data-stu-id="c75f4-216">**Decisions:**</span></span>

- <span data-ttu-id="c75f4-217">ما اسم السياسة؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-217">What is the name of the policy?</span></span>
- <span data-ttu-id="c75f4-218">ما الذي يتم وضع سياسة المصروفات له؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-218">What is the expense policy for?</span></span>
- <span data-ttu-id="c75f4-219">إذا كنت قررت سابقًا تمكين المصروفات بين الشركات الشقيقة، على أي شركات في مؤسستك سيتم تطبيق هذه السياسة؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="c75f4-220">متى تصبح السياسة فعالة؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-220">When does the policy become effective?</span></span>
- <span data-ttu-id="c75f4-221">متى ينتهي تاريخ صلاحية السياسة؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-221">When does the policy expire?</span></span>
- <span data-ttu-id="c75f4-222">ما المقصود بقاعدة السياسة؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-222">What is the policy rule?</span></span>
- <span data-ttu-id="c75f4-223">ما نتيجة قاعدة السياسة؟</span><span class="sxs-lookup"><span data-stu-id="c75f4-223">What is the outcome of the policy rule?</span></span>
