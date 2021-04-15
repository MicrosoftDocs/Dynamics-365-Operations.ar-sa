---
title: إنشاء تقارير قانون الرعاية ميسورة التكلفة (Affordable Care Act)
description: تقوم تقارير الرعاية ميسورة التكلفة (ACA) بإنشاء النماذج 1095-B و 1095-C لدعم جزء **تكليف صاحب العمل (Employer Mandate)** في قانون الرعاية ميسورة التكلفة.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 055de1f0ff3f8fd4fadba0a685fd703b9d19d918
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805984"
---
# <a name="generate-aca-reports"></a><span data-ttu-id="7c9f2-103">إنشاء تقارير ACA</span><span class="sxs-lookup"><span data-stu-id="7c9f2-103">Generate ACA reports</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="7c9f2-104">تقوم تقارير الرعاية ميسورة التكلفة (ACA) بإنشاء النماذج 1095-B و 1095-C لدعم جزء **تكليف صاحب العمل (Employer Mandate)** في قانون الرعاية ميسورة التكلفة.</span><span class="sxs-lookup"><span data-stu-id="7c9f2-104">Affordable Care Act (ACA) reporting generates forms 1095-B and 1095-C in support of the **Employer Mandate** portion of the Affordable Care Act.</span></span>

> [!NOTE]
> <span data-ttu-id="7c9f2-105">يتم تمكين تقارير الرعاية ميسورة التكلفة (ACA) فقط للكيانات القانونية في الولايات المتحدة.</span><span class="sxs-lookup"><span data-stu-id="7c9f2-105">ACA reporting is only enabled for legal entities in the United States.</span></span>

## <a name="getting-started"></a><span data-ttu-id="7c9f2-106">بدء الاستخدام</span><span class="sxs-lookup"><span data-stu-id="7c9f2-106">Getting started</span></span>

<span data-ttu-id="7c9f2-107">لتتبع المعلومات للإعلام للنموذجين 1095-B و1095-C، يجب أولاً إنشاء مجموعة واحدة أو أكثر من مجموعات التغطية التي يشملها قانون الرعاية ميسورة التكلفة.</span><span class="sxs-lookup"><span data-stu-id="7c9f2-107">To track information for forms 1095-B and 1095-C, you must first create one or more Affordable care coverage groups.</span></span> <span data-ttu-id="7c9f2-108">تشير مجموعات تغطية الرعاية ميسورة التكلفة إلى:</span><span class="sxs-lookup"><span data-stu-id="7c9f2-108">Affordable Care coverage groups indicate:</span></span>

- <span data-ttu-id="7c9f2-109">عرض التغطية لموظف</span><span class="sxs-lookup"><span data-stu-id="7c9f2-109">The offer of coverage for an employee</span></span>
- <span data-ttu-id="7c9f2-110">حصة الموظف بأقل قسط شهري للتكلفة، إذا كانت التكلفة أعلى من خط الفقر الفيدرالي</span><span class="sxs-lookup"><span data-stu-id="7c9f2-110">The employee’s share of the lowest cost monthly premium, if the cost is above the federal poverty line</span></span>
- <span data-ttu-id="7c9f2-111">الملاذ الآمن الذي يستخدمه صاحب العمل، إن وجد</span><span class="sxs-lookup"><span data-stu-id="7c9f2-111">Safe Harbor used by the employer, if applicable</span></span>

<span data-ttu-id="7c9f2-112">يسمح لك استخدام مجموعات تغطية الرعاية ميسورة التكلفة بإدارة المعلومات المتعلقة بهذه المجالات من دون تغيير كل سجل موظف حين تكون الظروف نفسها.</span><span class="sxs-lookup"><span data-stu-id="7c9f2-112">Affordable Care coverage groups allow you to manage the information for these fields without changing every employee record where the conditions are the same.</span></span> <span data-ttu-id="7c9f2-113">يمكنك بسهولة تعيين مجموعات تغطية الرعاية ميسورة التكلفة‬ إلى موظف أو أكثر باستخدام خيار **التعيين الجماعي‬** على الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7c9f2-113">You can easily assign Affordable Care coverage groups to one or more employees by using the **Mass assign** option on the page.</span></span>

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a><span data-ttu-id="7c9f2-114">الحفاظ على إصدارات متعددة من مجموعة تغطية</span><span class="sxs-lookup"><span data-stu-id="7c9f2-114">Maintaining multiple versions of a coverage group</span></span>

<span data-ttu-id="7c9f2-115">يمكنك الحفاظ على إصدارات متعددة لأي مجموعة تغطية.</span><span class="sxs-lookup"><span data-stu-id="7c9f2-115">You can maintain multiple versions of any coverage group.</span></span> <span data-ttu-id="7c9f2-116">تسمح لك هذه الوظيفة بإجراء تغييرات دون الحاجة إلى إنشاء مجموعة جديدة وإعادة تعيين الموظفين إليها.</span><span class="sxs-lookup"><span data-stu-id="7c9f2-116">This functionality allows you to make changes without having to create a new group and reassign employees to it.</span></span> 

<span data-ttu-id="7c9f2-117">بعد إنشاء مجموعات تغطية ACA، يمكنك تعيين المجموعات بشكل شامل للموظفين باستخدام خيار **التعيين الشامل**.</span><span class="sxs-lookup"><span data-stu-id="7c9f2-117">After you’ve created ACA coverage groups, you can mass assign the groups to employees with the **Mass assignment** option.</span></span> <span data-ttu-id="7c9f2-118">كما يمكنك أيضًا الاشارة فرديًا إلى ما إذا كانت تتبّع معلومات ACA ورفع تقرير بها وتعيين موظف إلى مجموعة تغطية الرعاية ميسورة التكلفة.</span><span class="sxs-lookup"><span data-stu-id="7c9f2-118">You can also individually indicate whether to track and report ACA information, and assign an employee to an Affordable Care coverage group.</span></span>

<span data-ttu-id="7c9f2-119">لست بحاجه لتعقب بعض معلومات التغطية لـ ACA، مثل موظفي الدوام الجزئي.</span><span class="sxs-lookup"><span data-stu-id="7c9f2-119">You don't need to track some ACA coverage information, such as for part-time employees.</span></span> <span data-ttu-id="7c9f2-120">في هذه الحالة، قم بتعيين حقل **رفع تقرير بالتغطية** على **لا**.</span><span class="sxs-lookup"><span data-stu-id="7c9f2-120">In this case, set the **Report coverage** field to **No**.</span></span> <span data-ttu-id="7c9f2-121">على الرغم من أنه يجب عليك تعيين كل موظف بمعلومات ACA قابلة للتعقب إلى مجموعة تغطية الرعاية ميسورة التكلفة، إلا أنه ما يزال بإمكانك تغيير الخيارات التالية للأشهر بقيم مختلفه:</span><span class="sxs-lookup"><span data-stu-id="7c9f2-121">Although you must assign each employee with trackable ACA information to an Affordable Care coverage group, you can still change the following options for months with different values:</span></span>

- <span data-ttu-id="7c9f2-122">**عرض التغطية**</span><span class="sxs-lookup"><span data-stu-id="7c9f2-122">**Offer of coverage**</span></span>
- <span data-ttu-id="7c9f2-123">**حصة الموظف في التكلفة**</span><span class="sxs-lookup"><span data-stu-id="7c9f2-123">**Employee share of cost**</span></span>
- <span data-ttu-id="7c9f2-124">**الملاذ الآمن**</span><span class="sxs-lookup"><span data-stu-id="7c9f2-124">**Safe Harbor**</span></span>

<span data-ttu-id="7c9f2-125">لإدخال استثناءات لقيم مجموعة التغطية التي يشملها قانون الرعاية ميسورة التكلفة‬، حدد ارتباط **تغطية الرعاية ميسورة التكلفة** الموجود على صفحة **تفاصيل العامل**، تحت القسم **معلومات إضافية** في **علامة التبويب التوظيف**.</span><span class="sxs-lookup"><span data-stu-id="7c9f2-125">To enter exceptions for Affordable Care coverage group values, select the **Affordable Care Coverage** link on the **Worker detail** page under the **Additional information** section on the **Employment tab**.</span></span>

## <a name="reporting-health-care-coverage"></a><span data-ttu-id="7c9f2-126">إعداد تقرير تغطية الرعاية الصحية</span><span class="sxs-lookup"><span data-stu-id="7c9f2-126">Reporting health care coverage</span></span>

<span data-ttu-id="7c9f2-127">بالإضافة إلى تعقب ما إذا كان قد تم تقديم تغطية الرعاية الصحية للموظفين بدوام كامل، إذا قدم صاحب العمل تغطية صحية ذات تأمين ذاتي مشمولة بالرعاية والتي سجل الموظف نفسه للحصول عليها (بغض النظر عما إذا كانت حالة التوظيف بدوام كامل أو دوام جزئي)، فيجب رفع تقرير بالمعلومات الإضافية على 1095-C.</span><span class="sxs-lookup"><span data-stu-id="7c9f2-127">In addition to tracking health insurance coverage offered to full-time employees, if the employer offers employer-sponsored self-insured health coverage for which the employee is enrolled (regardless of whether their employment status is full-time or part-time), additional information needs to be reported on the 1095-C.</span></span> <span data-ttu-id="7c9f2-128">بالنسبة إلى كل موظف (بما في ذلك الأشخاص المعالين) مغطى بواسطة خطط الميزات المشمولة بالرعاية التي يقدمها صاحب العمل، يجب تضمينه في التقرير الخاص بالأشهر التي تمت تغطيتها.</span><span class="sxs-lookup"><span data-stu-id="7c9f2-128">Each employee (including dependents) covered by the employer-sponsored benefit plans needs to be included on the report for the months they were covered.</span></span> 

<span data-ttu-id="7c9f2-129">يمكنك الإشارة إلى ما إذا كان يجب الإبلاغ عن كل خطة ميزات عن طريق تحديد خانة الاختيار **يمكن إرسال تقرير به إلى ACA‬**.</span><span class="sxs-lookup"><span data-stu-id="7c9f2-129">You can indicate whether or not each benefit plan must be reported by selecting the **ACA reportable** check box.</span></span>

<span data-ttu-id="7c9f2-130">بالإضافة إلى ذلك، إذا اختار أحد الموظفين تغطية أي واحد من المعالين التابعين له ضمن ميزة معينة، فيمكنك الإشارة إلى التواريخ التي تمت فيها تغطية الشخص المعال لكل موظف على صفحة **الاحتفاظ بالميزات‬**.</span><span class="sxs-lookup"><span data-stu-id="7c9f2-130">In addition, if employees have chosen to have any of their dependents covered under a benefit, you can indicate the dates the dependent was covered for each employee on the **Maintain benefits** page.</span></span> <span data-ttu-id="7c9f2-131">للإشارة إلى أن الشخص المعال مغطى بالميزة، حدد زر **تحرير** في جزء الإجراءات من علامة التبويب السريعة **المعالون**.</span><span class="sxs-lookup"><span data-stu-id="7c9f2-131">To indicate that the dependent is covered under the benefit, select the **Edit** button in the action pane of the **Dependents** fast tab.</span></span>

<span data-ttu-id="7c9f2-132">في صفحة **إدارة تاريخ تغطية المعال‬**، يمكنك الإشارة إلى التواريخ التي تم فيها تغطية المعال بواسطة الميزة.</span><span class="sxs-lookup"><span data-stu-id="7c9f2-132">On the **Dependent coverage date manager** page, you can indicate the dates the dependent was covered by the benefit.</span></span> <span data-ttu-id="7c9f2-133">سيؤدي إدخال التواريخ في هذه الصفحة إلى تحديد خانة الاختيار **‏‫تمت تغطيته‬** في صفحة **الاحتفاظ بالميزات** بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="7c9f2-133">Entering dates on this page will automatically select the **Covered** checkbox on the **Maintain benefits** page.</span></span>

## <a name="generate-1095-b-and-1095-c-forms"></a><span data-ttu-id="7c9f2-134">إنشاء نماذج 1095-B و1095-C</span><span class="sxs-lookup"><span data-stu-id="7c9f2-134">Generate 1095-B and 1095-C forms</span></span>

<span data-ttu-id="7c9f2-135">يمكنك أيضًا إنشاء النموذجين 1095-B و1095-C من ضمن المنتج، وتوزيعها على كل الموظفين.</span><span class="sxs-lookup"><span data-stu-id="7c9f2-135">You can also generate 1095-B and 1095-C forms from within the product, and distribute them to each of your employees.</span></span> <span data-ttu-id="7c9f2-136">يمكن للنظام أيضا إنشاء نماذج 1095-C بشكل إلكتروني وملفات إرسال IRS 1094-C.</span><span class="sxs-lookup"><span data-stu-id="7c9f2-136">The system can also electronically generate 1095-C forms and the 1094-C IRS transmittal files.</span></span>  

<span data-ttu-id="7c9f2-137">عند إنشاء نموذج 1095-C، أدخل السنة الضريبية‬ المناسبة مع الإشارة إلى ما إذا كان يجب إخفاء أرقام الضمان الاجتماعي.</span><span class="sxs-lookup"><span data-stu-id="7c9f2-137">When generating the 1095-C form, enter the appropriate tax year and indicate if social security numbers should be masked.</span></span> <span data-ttu-id="7c9f2-138">إذا كنت تقوم بطباعة نماذج 1095-C لأكثر من 500 موظف، فستتلقى ملف PDF واحدًا أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="7c9f2-138">If you're printing 1095-C forms for more than 500 employees, you'll receive more than one PDF file.</span></span> <span data-ttu-id="7c9f2-139">من المستحسن أن تقوم بزيادة **الحد الأقصى لحجم الملف** في نافذة **معلمات إدارة المستندات** إلى 150 ميغابايت.</span><span class="sxs-lookup"><span data-stu-id="7c9f2-139">It’s recommended that you increase the **Maximum file size** in the **Document management parameters** window to 150 MB.</span></span>

## <a name="viewing-information"></a><span data-ttu-id="7c9f2-140">عرض المعلومات</span><span class="sxs-lookup"><span data-stu-id="7c9f2-140">Viewing information</span></span>

<span data-ttu-id="7c9f2-141">يمكنك استخدام الصفحة **التغطية التي يشملها قانون الرعاية ميسورة التكلفة للعامل‬** لمعرفة من هم الموظفون الذين تم تعيينهم إلى كل مجموعة تغطية، والموظفون الذين لا يجب تضمينهم على تقرير والموظفون غير المعينين.</span><span class="sxs-lookup"><span data-stu-id="7c9f2-141">You can use the **Worker Affordable Care coverage** page to see which employees have been assigned to each coverage group, which employees don’t need to be included on a report, and which employees are unassigned.</span></span>

<span data-ttu-id="7c9f2-142">إذا تم تجاوز أي من القيم الافتراضية من مجموعة التغطية التي يشملها قانون الرعاية ميسورة التكلفة‬، فسوف تظهر على علامة نجمية بجوار القيمة التي تم تغييرها.</span><span class="sxs-lookup"><span data-stu-id="7c9f2-142">If any of the default values from the Affordable Care coverage group have been overridden, an asterisk will appear next to the value that was changed.</span></span> <span data-ttu-id="7c9f2-143">إذا كانت القيم هي نفسها لفترة 12 شهرًا ولم يتم تجاوزها، فستتم طباعة القيمة في عمود **جميع الاثنى عشر شهرًا‬**.</span><span class="sxs-lookup"><span data-stu-id="7c9f2-143">If the values for all 12 months are the same and haven’t been overridden, the value will print in the **All 12 months** column.</span></span>

<span data-ttu-id="7c9f2-144">يمكنك أيضا استخدام اطار الاستعلام لمعرفة الموظفين الذين تم وضع علامة عليهم باعتبارهم غير قابلين للتقرير وفق قانون الرعاية ميسورة التكلفة.</span><span class="sxs-lookup"><span data-stu-id="7c9f2-144">You can also use the inquiry window to understand which employees have been flagged as not ACA reportable.</span></span> <span data-ttu-id="7c9f2-145">لست بحاجة لتعقب ما إذا كان قد تم تقديم التغطية لهم أم لا ولا يلزم إصدار 1095 إليهم في نهاية السنة.</span><span class="sxs-lookup"><span data-stu-id="7c9f2-145">You don’t need to track whether coverage was offered to them and won't need to issue a 1095-C to them at the end of the year.</span></span> <span data-ttu-id="7c9f2-146">حدد **لا يمكن إرسال تقرير به إلى ACA** في حقل **تصفيه حسب** لإنشاء قائمة بكافة الموظفين الذين لن يتلقوا نموذج 1095-C.</span><span class="sxs-lookup"><span data-stu-id="7c9f2-146">Select **Not ACA reportable** in the **Filter by** field to generate a list of all employees who won't receive a 1095-C.</span></span>

<span data-ttu-id="7c9f2-147">بالإضافة إلى ذلك، يمكنك أيضًا عرض أي موظفين لم يتم تعيينهم (الحقل **تغطية تقرير ACA** فارغ) أو تم تعيينهم إلى مجموعة تغطية يشملها قانون الرعاية ميسورة التكلفة‬ انتهت مدة صلاحيتها للسنة المحددة في حقل **السنة**.</span><span class="sxs-lookup"><span data-stu-id="7c9f2-147">In addition, you can view any employees who are unassigned (the **ACA Report coverage** field is empty) or who have been assigned to an Affordable Care coverage group that is expired for the year selected in the **Year** field.</span></span>

<span data-ttu-id="7c9f2-148">يمكنك تصدير قوائم الموظفين التي تم إنشاؤها باستخدام أي من خيارات التصفية في Excel.</span><span class="sxs-lookup"><span data-stu-id="7c9f2-148">You can export lists of employees that were generated using any of the filtering options to Excel.</span></span>

<span data-ttu-id="7c9f2-149">إذا كنت بحاجة إلى رفع تقرير بالأشخاص الذين تمت تغطيتهم نظرًا لأنك توفر تغطية ذاتية التأمين، فيمكنك عرض أي معالين تمت تغطيتهم تحت خطط الفوائد المعلمة على أنها **‬‏‫يمكن إرسال تقرير بها إلى ACA**.</span><span class="sxs-lookup"><span data-stu-id="7c9f2-149">If you need to report covered individuals because you provide self-insured coverage, you can view any dependents covered under benefit plans marked as **ACA reportable**.</span></span> <span data-ttu-id="7c9f2-150">حدد **عرض تغطية المعالين** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="7c9f2-150">Select **View Dependent coverage** on the action pane.</span></span>

> [!NOTE]
> <span data-ttu-id="7c9f2-151">يتم عرض خطط المزايا المعلمة على أنها **‬‏‫يمكن إرسال تقرير بها إلى ACA** في اطار الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="7c9f2-151">Only benefit plans marked as **ACA reportable** display in the inquiry window.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]