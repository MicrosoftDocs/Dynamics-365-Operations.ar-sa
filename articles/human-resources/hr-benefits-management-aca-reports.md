---
title: إنشاء تقارير قانون الرعاية ميسورة التكلفة في إدارة الميزات
description: توضح هذه الموضوعات كيفية قيام إدارة الميزات بمساعدك في تعقب المعلومات التي يتم رفع تقرير بها في النموذج 1095-B والنموذج 1095-C بشأن تكليف صاحب العمل وفق قانون الرعاية ميسورة التكلفة (ACA).
author: andreabichsel
ms.date: 12/28/2020
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
ms.search.validFrom: 2020-12-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: a41195ea3b52a707ce9deae38f12eb90de2ff5aa
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805792"
---
# <a name="generate-aca-reports-in-benefits-management"></a><span data-ttu-id="f258a-103">إنشاء تقارير قانون الرعاية ميسورة التكلفة في إدارة الميزات</span><span class="sxs-lookup"><span data-stu-id="f258a-103">Generate ACA reports in Benefits management</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f258a-104">تساعدك إدارة الميزات في تعقب المعلومات التي يتم رفع تقرير بها في النموذج 1095-B والنموذج 1095-C بشأن تكليف صاحب العمل وفق قانون الرعاية ميسورة التكلفة (ACA).</span><span class="sxs-lookup"><span data-stu-id="f258a-104">Benefits management helps you track information that is reported on Form 1095-B and Form 1095-C for the Affordable Care Act (ACA) employer mandate.</span></span> <span data-ttu-id="f258a-105">كمثل إمكانية إعداد تقارير قانون الرعاية ميسورة التكلفة في مساحة عمل **المزايا** القديمة، يتم تطبيق هذه الوظيفة فقط على الكيانات القانونية في الولايات المتحدة.</span><span class="sxs-lookup"><span data-stu-id="f258a-105">Like the ACA reporting capability in the old **Benefits** workspace, this functionality applies only to legal entities in the United States.</span></span>

<span data-ttu-id="f258a-106">لاستخدام هذه الوظيفة، يجب أولا تشغيل **إدارة الميزات المتقدمة**.</span><span class="sxs-lookup"><span data-stu-id="f258a-106">To use this functionality, you must first turn on **Advanced Benefits Management**.</span></span> <span data-ttu-id="f258a-107">لمزيد من المعلومات، بما في ذلك التنبيهات الهامة حول إدارة الميزات، راجع [تمكين إدارة الميزات أو تعطيلها](hr-admin-manage-features.md#enable-or-disable-benefits-management).</span><span class="sxs-lookup"><span data-stu-id="f258a-107">For more information, including important caveats about Benefits management, see [Enable or disable Benefits management](hr-admin-manage-features.md#enable-or-disable-benefits-management).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f258a-108">يمكنك استخدام تقارير قانون الرعاية ميسورة التكلفة فقط من مساحة عمل **إدارة الميزات** أو مساحة عمل **الميزات** القديمة، وليس من كليهما.</span><span class="sxs-lookup"><span data-stu-id="f258a-108">You can use ACA reporting only from either the **Benefits management** workspace or the old **Benefits** workspace, not from both.</span></span> <span data-ttu-id="f258a-109">على سبيل المثال، إذا قمت بالتبديل إلى إدارة الميزات، ستكون تقارير قانون الرعاية ميسورة التكلفة متوفرة فقط من مساحة عمل **إدارة الميزات**، وليس من مساحة عمل **الميزات** القديمة.</span><span class="sxs-lookup"><span data-stu-id="f258a-109">For example, if you switched to Benefits management, ACA reporting is available only from the **Benefits management** workspace, not from the old **Benefits** workspace.</span></span>
>
> <span data-ttu-id="f258a-110">إذا قمت بالتبديل إلى إدارة الميزات في منتصف سنة التسجيل، فيجب تكوين بيانات الموظف بشكل صحيح للسنة بأكملها في إدارة الميزات.</span><span class="sxs-lookup"><span data-stu-id="f258a-110">If you switch to Benefits management in the middle of an enrollment year, you must correctly configure employee data for the whole year in Benefits management.</span></span> <span data-ttu-id="f258a-111">وبهذه الطريقة، تتأكد من أنك ستتلقى معلومات التقرير الدقيقة للسنة بأكملها.</span><span class="sxs-lookup"><span data-stu-id="f258a-111">In this way, you ensure that you will receive accurate reporting information for the whole year.</span></span>

## <a name="getting-started"></a><span data-ttu-id="f258a-112">بدء الاستخدام</span><span class="sxs-lookup"><span data-stu-id="f258a-112">Getting started</span></span>

<span data-ttu-id="f258a-113">لتتبع المعلومات للإعلام لنماذج 1095-B، قم أولاً بإنشاء مجموعة واحدة أو أكثر من مجموعات التغطية التي يشملها قانون الرعاية ميسورة التكلفة.</span><span class="sxs-lookup"><span data-stu-id="f258a-113">To track information for 1095 forms, first create one or more Affordable Care coverage groups.</span></span> <span data-ttu-id="f258a-114">وتشير هذه المجموعات إلى المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="f258a-114">These groups indicate the following information:</span></span>

- <span data-ttu-id="f258a-115">عرض التغطية الذي تم تقديمه لأحد الموظفين.</span><span class="sxs-lookup"><span data-stu-id="f258a-115">The offer of coverage that was provided to an employee</span></span>
- <span data-ttu-id="f258a-116">حصة الموظف بأقل قسط شهري للتكلفة، إذا كانت التكلفة أعلى من خط الفقر الفيدرالي</span><span class="sxs-lookup"><span data-stu-id="f258a-116">The employee's share of the lowest-cost monthly premium, if the cost is above the federal poverty line</span></span>
- <span data-ttu-id="f258a-117">الملاذ الآمن الذي يستخدمه صاحب العمل، إن وجد</span><span class="sxs-lookup"><span data-stu-id="f258a-117">The safe harbor that is used by the employer, if applicable</span></span>

<span data-ttu-id="f258a-118">تساعدك مجموعات التغطية للرعاية ميسورة التكلفة في إدارة هذه المعلومات لسجلات موظفين متعددة لها نفس الشروط.</span><span class="sxs-lookup"><span data-stu-id="f258a-118">Affordable Care coverage groups help you manage this information for multiple employee records that have the same conditions.</span></span> <span data-ttu-id="f258a-119">يمكنك تعيين مجموعات بسهولة لموظف واحد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="f258a-119">You can easily assign groups to one or more employees.</span></span>

### <a name="create-or-edit-an-affordable-care-coverage-group"></a><span data-ttu-id="f258a-120">إنشاء مجموعة تغطية الرعاية ميسورة التكلفة أو تحريرها</span><span class="sxs-lookup"><span data-stu-id="f258a-120">Create or edit an Affordable Care coverage group</span></span>

1. <span data-ttu-id="f258a-121">في مساحة عمل **إدارة الميزات**، حدد **مجموعة تغطية الرعاية ميسورة التكلفة**.</span><span class="sxs-lookup"><span data-stu-id="f258a-121">In the **Benefits management** workspace, select **Affordable Care coverage group**.</span></span>

    ![تحديد مجموعة تغطية الرعاية ميسورة التكلفة](./media/hr-benefits-management-aca-coverage-group.png)

2. <span data-ttu-id="f258a-123">حدد **جديد** لإنشاء مجموعة تغطية جديدة للرعاية ميسورة التكلفة أو **تحرير** لتغيير مجموعة موجودة.</span><span class="sxs-lookup"><span data-stu-id="f258a-123">Select **New** to create a new Affordable Care coverage group or **Edit** to change an existing group.</span></span>

    ![تحديد جديد أو تحرير](./media/hr-benefits-management-aca-new.png)

3. <span data-ttu-id="f258a-125">قم بتعيين الحقول التالية.</span><span class="sxs-lookup"><span data-stu-id="f258a-125">Set the following fields.</span></span>

    | <span data-ttu-id="f258a-126">الحقل</span><span class="sxs-lookup"><span data-stu-id="f258a-126">Field</span></span> | <span data-ttu-id="f258a-127">الوصف</span><span class="sxs-lookup"><span data-stu-id="f258a-127">Description</span></span> |
    |---|---|
    | <span data-ttu-id="f258a-128">الاسم</span><span class="sxs-lookup"><span data-stu-id="f258a-128">Name</span></span> | <span data-ttu-id="f258a-129">أدخل اسمًا للمجموعة.</span><span class="sxs-lookup"><span data-stu-id="f258a-129">Enter a name for the group.</span></span> |
    | <span data-ttu-id="f258a-130">الوصف</span><span class="sxs-lookup"><span data-stu-id="f258a-130">Description</span></span> | <span data-ttu-id="f258a-131">أدخل وصفًا للمجموعة.</span><span class="sxs-lookup"><span data-stu-id="f258a-131">Enter a description of the group.</span></span> |
    | <span data-ttu-id="f258a-132">عرض التغطية</span><span class="sxs-lookup"><span data-stu-id="f258a-132">Offer of coverage</span></span> | <span data-ttu-id="f258a-133">التغطية التي يتم توفيرها للموظفين أو الزوج أو الشريك الخاص بهم والمعالين.</span><span class="sxs-lookup"><span data-stu-id="f258a-133">The coverage that is offered to employees, their spouse or partner, and their dependents.</span></span> |
    | <span data-ttu-id="f258a-134">حصة الموظف في التكلفة</span><span class="sxs-lookup"><span data-stu-id="f258a-134">Employee share of cost</span></span> | <span data-ttu-id="f258a-135">المبلغ الذي يتحمل الموظف المسؤولية عن دفعه.</span><span class="sxs-lookup"><span data-stu-id="f258a-135">The amount that the employee is responsible for.</span></span> |
    | <span data-ttu-id="f258a-136">المرفأ الآمن (safe harbor) 4980H للقسم القابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="f258a-136">Applicable section 4980H safe harbor</span></span> | <span data-ttu-id="f258a-137">الملاز الآمن 4980H أو رمز الإعفاء الانتقالي.</span><span class="sxs-lookup"><span data-stu-id="f258a-137">The 4980H safe harbor or transition relief code.</span></span> |
    | <span data-ttu-id="f258a-138">شهر بدء الخطة</span><span class="sxs-lookup"><span data-stu-id="f258a-138">Plan start month</span></span> | <span data-ttu-id="f258a-139">حدد شهر التقويم الذي تبدأ في سنة خطة المزايا الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="f258a-139">Select the calendar month when your benefit plan year begins.</span></span> |
    | <span data-ttu-id="f258a-140">المجموعة صالحة من</span><span class="sxs-lookup"><span data-stu-id="f258a-140">Group valid from</span></span> | <span data-ttu-id="f258a-141">أول تاريخ يكون فيه هذا السجل صالحًا.</span><span class="sxs-lookup"><span data-stu-id="f258a-141">The first date when this record is valid.</span></span> |
    | <span data-ttu-id="f258a-142">المجموعة صالحة من خلال</span><span class="sxs-lookup"><span data-stu-id="f258a-142">Group valid through</span></span> | <span data-ttu-id="f258a-143">آخر تاريخ يكون فيه هذا السجل صالحًا.</span><span class="sxs-lookup"><span data-stu-id="f258a-143">The last date when this record is valid.</span></span> <span data-ttu-id="f258a-144">إذا لم يكن هناك تاريخ انتهاء صلاحية، فادخل **أبدا**.</span><span class="sxs-lookup"><span data-stu-id="f258a-144">If there is no expiration date, enter **Never**.</span></span> |

    ![إنشاء مجموعة تغطية](./media/hr-benefits-management-aca-new-group.png)

4. <span data-ttu-id="f258a-146">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="f258a-146">Select **Save**.</span></span>

### <a name="assign-multiple-employees-to-an-affordable-care-coverage-group"></a><span data-ttu-id="f258a-147">تعيين عدة موظفين إلى مجموعة تغطية الرعاية ميسورة التكلفة</span><span class="sxs-lookup"><span data-stu-id="f258a-147">Assign multiple employees to an Affordable Care coverage group</span></span>

1. <span data-ttu-id="f258a-148">في مساحة عمل **إدارة الميزات**، حدد **مجموعة تغطية الرعاية ميسورة التكلفة**.</span><span class="sxs-lookup"><span data-stu-id="f258a-148">In the **Benefits management** workspace, select **Affordable Care coverage group**.</span></span>
2. <span data-ttu-id="f258a-149">حدد المجموعة التي سيتم تعيين الموظفين إليها.</span><span class="sxs-lookup"><span data-stu-id="f258a-149">Select the group to assign employees to.</span></span>
3. <span data-ttu-id="f258a-150">حدد **التعيين الشامل**.</span><span class="sxs-lookup"><span data-stu-id="f258a-150">Select **Mass assignment**.</span></span>

    ![تحديد التعيين الشامل](./media/hr-benefits-management-aca-mass-assignment.png)

4. <span data-ttu-id="f258a-152">حدد الموظفين في القائمة، ثم حدد **تعيين**.</span><span class="sxs-lookup"><span data-stu-id="f258a-152">Select employees in the list, and then select **Assign**.</span></span>

    ![تعيين الموظفين المحددين إلى مجموعة](./media/hr-benefits-management-aca-assign-coverage-group.png)

## <a name="maintain-multiple-versions-of-coverage-options"></a><span data-ttu-id="f258a-154">الحفاظ على إصدارات متعددة لخيارات التغطية</span><span class="sxs-lookup"><span data-stu-id="f258a-154">Maintain multiple versions of coverage options</span></span>

<span data-ttu-id="f258a-155">يمكنك الحفاظ على إصدارات متعددة لأي مجموعة تغطية.</span><span class="sxs-lookup"><span data-stu-id="f258a-155">You can maintain multiple versions of any coverage group.</span></span> <span data-ttu-id="f258a-156">عند إجراء تغييرات في مؤسستك أو في الميزات المقدمة، يمكنك الحفاظ على معلومات المجموعة محدثة دون الحاجة إلى إنشاء مجموعة جديدة وإعادة تعيين الموظفين لها.</span><span class="sxs-lookup"><span data-stu-id="f258a-156">When something changes in your organization or the benefits that are offered, you can keep the group's information up to date without having to create a new group and reassign employees to it.</span></span>

<span data-ttu-id="f258a-157">بعد إنشاء مجموعات تغطية الرعاية ميسورة التكلفة، يمكنك تعيين الموظفين بشكل شامل.</span><span class="sxs-lookup"><span data-stu-id="f258a-157">After you've created Affordable Care coverage groups, you can mass-assign employees to them.</span></span> <span data-ttu-id="f258a-158">ويمكنك أيضا تعيين الموظفين بشكل فردي إلى مجموعات، والإشارة إلى ما إذا كانت معلومات قانون الرعاية ميسورة التكلفة متعقبة أم يتم رفع تقرير بها.</span><span class="sxs-lookup"><span data-stu-id="f258a-158">You can also individually assign employees to groups, and indicate whether ACA information is tracked and reported.</span></span>

<span data-ttu-id="f258a-159">إذا لم يكن من الضروري تعقب معلومات قانون الرعاية ميسورة التكلفة الخاصة بأحد الموظفين ورفع تقرير بها، فيمكنك تعيين خيار **رفع تقرير بالتغطية** إلى **لا**.</span><span class="sxs-lookup"><span data-stu-id="f258a-159">If you don't have to track and report ACA information for an employee, you can set the **Report coverage** option to **No**.</span></span> <span data-ttu-id="f258a-160">على سبيل المثال، قد يكون لديك موظفون بدوام جزئي لا يتطلبون رفع تقارير قانون الرعاية ميسورة التكلفة.</span><span class="sxs-lookup"><span data-stu-id="f258a-160">For example, you might have part-time employees who don't require ACA reporting.</span></span>

### <a name="override-default-values-for-an-employee"></a><span data-ttu-id="f258a-161">تجاوز القيم الافتراضية للموظف</span><span class="sxs-lookup"><span data-stu-id="f258a-161">Override default values for an employee</span></span>

<span data-ttu-id="f258a-162">بالنسبة للموظفين الذين تم تعيينهم لإحدى مجموعات تغطية الرعاية ميسورة التكلفة، يمكنك تغيير الخيارات التالية لأي شهور تتطلب قيما مختلفة:</span><span class="sxs-lookup"><span data-stu-id="f258a-162">For employees who are assigned to an Affordable Care coverage group, you can change the following options for any months that require different values:</span></span>

- <span data-ttu-id="f258a-163">عرض التغطية</span><span class="sxs-lookup"><span data-stu-id="f258a-163">Offer of coverage</span></span>
- <span data-ttu-id="f258a-164">حصة الموظف في التكلفة</span><span class="sxs-lookup"><span data-stu-id="f258a-164">Employee share of cost</span></span>
- <span data-ttu-id="f258a-165">المرفأ الآمن (safe harbor) 4980H للقسم القابل للتطبيق</span><span class="sxs-lookup"><span data-stu-id="f258a-165">Applicable section 4980H safe harbor</span></span>

> [!NOTE]
> <span data-ttu-id="f258a-166">بالنسبة لتقارير 2020 ACA، يجب رفع تقارير بكل من الرموز البريدية للعمل والمنزل في النموذج 1095-C.</span><span class="sxs-lookup"><span data-stu-id="f258a-166">For 2020 ACA reports, you must report both work and home ZIP Codes on Form 1095-C.</span></span> <span data-ttu-id="f258a-167">يتم ملء القيم تلقائيًا، استنادا إلى المواقع النشطة الحالية.</span><span class="sxs-lookup"><span data-stu-id="f258a-167">Values are automatically filled in, based on current active locations.</span></span> <span data-ttu-id="f258a-168">إذا كان أحد المواقع مختلفًا أثناء أي جزء من السنm، فيجب تجاوز القيمة.</span><span class="sxs-lookup"><span data-stu-id="f258a-168">If either location was different during any part of the year, you must override the value.</span></span> <span data-ttu-id="f258a-169">يتم ملء حقل **الرمز البريدي** (السطر 17) في تقرير 1095-C فقط إذا كان رمز **عرض التغطية** يحتوي على **1L** عن طريق **1Q**، كما يلي:</span><span class="sxs-lookup"><span data-stu-id="f258a-169">The **ZIP Code** field (line 17) of the 1095-C report is filled in only if the **Offer of coverage** code contains **1L** through **1Q**, as follows:</span></span>
>
> - <span data-ttu-id="f258a-170">**1L أو 1M أو 1N:** الرمز البريدي الأساسي للإقامة</span><span class="sxs-lookup"><span data-stu-id="f258a-170">**1L, 1M, or 1N:** The primary residence ZIP Code</span></span>
> - <span data-ttu-id="f258a-171">**1O أو 1P أو 1Q:**  الرمز البريدي الأساسي للعمل</span><span class="sxs-lookup"><span data-stu-id="f258a-171">**1O, 1P, 1Q:** The primary work ZIP Code</span></span>

<span data-ttu-id="f258a-172">لإدخال استثناءات لأي قيم من مجموعة تغطية الرعاية ميسورة التكلفة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="f258a-172">To enter exceptions for any values of an Affordable Care coverage group, follow these steps.</span></span>

1. <span data-ttu-id="f258a-173">في مساحة عمل **إدارة العاملين**، حدد **ارتباطات**، ثم حدد **العاملون**.</span><span class="sxs-lookup"><span data-stu-id="f258a-173">In the **Personnel management** workspace, select **Links**, and then select **Workers**.</span></span>
2. <span data-ttu-id="f258a-174">حدد الموظف في القائمة.</span><span class="sxs-lookup"><span data-stu-id="f258a-174">Select the employee in the list.</span></span>
3. <span data-ttu-id="f258a-175">من علامة التبويب **التوظيف**، في قسم **معلومات إضافية**، حدد **تغطية الرعاية ميسورة التكلفة**.</span><span class="sxs-lookup"><span data-stu-id="f258a-175">On the **Employment** tab, in the **More information** section, select **Affordable Care coverage**.</span></span>

    ![تغيير الخيارات لموظف واحد](./media/hr-benefits-management-aca-change-single-employee.png)

4. <span data-ttu-id="f258a-177">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="f258a-177">Select **Edit**.</span></span>
5. <span data-ttu-id="f258a-178">بالنسبة لكل شهر يتطلب تغييرات، حدد خانة الاختيار **تجاوز الافتراضي**، ثم قم بتغيير القيم الأخرى كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="f258a-178">For each month that requires changes, select the **Override default** check box, and then change the other values as required.</span></span>

    ![تجاوز القيم الافتراضية](./media/hr-benefits-management-aca-override-default.png)

6. <span data-ttu-id="f258a-180">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="f258a-180">Select **Save**.</span></span>

## <a name="report-health-care-coverage"></a><span data-ttu-id="f258a-181">إعداد تقرير تغطية الرعاية الصحية</span><span class="sxs-lookup"><span data-stu-id="f258a-181">Report health care coverage</span></span>

<span data-ttu-id="f258a-182">يجب أن تتعقب أي تغطية صحية بنظام التأمين الذاتي تحت رعاية صاحب العمل للموظفين بدوام كامل دوام جزئي.</span><span class="sxs-lookup"><span data-stu-id="f258a-182">You must track any employer-sponsored, self-insured health care coverage for full-time and part-time employees.</span></span> <span data-ttu-id="f258a-183">قم بتضمين كل موظف، مع المعالين له، في التقرير 1095-C للأشهر التي يتم تغطيتهم فيها.</span><span class="sxs-lookup"><span data-stu-id="f258a-183">Include each employee, together with their dependents, on the 1095-C report for the months when they were covered.</span></span>

<span data-ttu-id="f258a-184">للإشارة إلى ما إذا كان يجب رفع تقرير عن خطة المزايا أم لا، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="f258a-184">To indicate whether a benefit plan must be reported, follow these steps.</span></span>

1. <span data-ttu-id="f258a-185">في مساحة العمل **إدارة المزايا**، حدد **خطط المزايا**.</span><span class="sxs-lookup"><span data-stu-id="f258a-185">In the **Benefits management** workspace, select **Benefit plans**.</span></span>
2. <span data-ttu-id="f258a-186">حدد خطة المزايا المراد رفع تقرير بها.</span><span class="sxs-lookup"><span data-stu-id="f258a-186">Select the benefit plan to report.</span></span>
3. <span data-ttu-id="f258a-187">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="f258a-187">Select **Edit**.</span></span>
4. <span data-ttu-id="f258a-188">قم بتعيين خيار **رفع تقرير بموجب قانون الرعاية ميسورة التكلفة** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="f258a-188">Set the **Reported under the Affordable Care Act** option to **Yes**.</span></span>

    ![إعداد تقرير تغطية الرعاية الصحية](./media/hr-benefits-management-aca-report-coverage.png)

5. <span data-ttu-id="f258a-190">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="f258a-190">Select **Save**.</span></span>

<span data-ttu-id="f258a-191">إذا اختار أحد الموظفين تغطية الرعاية الصحية لأحد المعالين، يتم تحديد فترة تغطية المعال حسب تاريخ تسجيل المعال أو إزالته.</span><span class="sxs-lookup"><span data-stu-id="f258a-191">If an employee chooses health care coverage for a dependent, the dependent's coverage period is determined by the date when the dependent was enrolled or removed.</span></span> <span data-ttu-id="f258a-192">يتم حساب تواريخ التغطية الخاصة بالمعالين تلقائيًا استنادا إلى الفترة التي كان فيها المعال مؤهلا ونشطًا في الخطة أثناء سنة التسجيل.</span><span class="sxs-lookup"><span data-stu-id="f258a-192">Coverage dates for dependents are automatically calculated based on the period when the dependent was eligible and active in a plan during the enrollment year.</span></span>

## <a name="generate-1095-b-and-1095-c-forms"></a><span data-ttu-id="f258a-193">إنشاء نماذج 1095-B و1095-C</span><span class="sxs-lookup"><span data-stu-id="f258a-193">Generate 1095-B and 1095-C forms</span></span>

<span data-ttu-id="f258a-194">يمكنك أيضًا إنشاء النموذجين 1095-B و1095-C وفق قانون الرعاية ميسورة التكلفة، ثم توزيعها على كل الموظفين لديك.</span><span class="sxs-lookup"><span data-stu-id="f258a-194">You can generate ACA 1095-B and 1095-C forms, and then distribute them to each of your employees.</span></span> <span data-ttu-id="f258a-195">كما يمكن إنشاء النموذج 1095-C وملفات 1094-C الانتقالية المقابلة تلقائيًا لإرسالها إلى خدمه الإيرادات الداخلية (IRS).</span><span class="sxs-lookup"><span data-stu-id="f258a-195">You can also electronically generate Form 1095-C and the corresponding 1094-C transmittal files to send to the Internal Revenue Service (IRS).</span></span>

1. <span data-ttu-id="f258a-196">في مساحة عمل **إدارة الميزات**، حدد **نموذج ACA 1095-B** أو **نموذج ACA 1095-C**.</span><span class="sxs-lookup"><span data-stu-id="f258a-196">In the **Benefits management** workspace, select **ACA 1095-B form** or **ACA 1095-C form**.</span></span>
2. <span data-ttu-id="f258a-197">قم بتغيير المعلمات كما هو مطلوب، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f258a-197">Change the parameters as required, and then select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f258a-198">إذا كنت تقوم بطباعة نماذج 1095-C لأكثر من 500 موظف، فستتلقى ملف PDF واحدًا أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="f258a-198">If you're printing 1095-C forms for more than 500 employees, you will receive more than one PDF file.</span></span> <span data-ttu-id="f258a-199">ونوصي بزيادة قيمة حقل **الحد الأقصى لحجم الملف بالميغا بايت** في صفحة **معلمات إدارة المستندات** إلى **150**.</span><span class="sxs-lookup"><span data-stu-id="f258a-199">We recommend that you increase the value of the **Maximum file size in megabytes** field on the **Document management parameters** page to **150**.</span></span> <span data-ttu-id="f258a-200">(لفتح هذه الصفحة بسرعة، يمكنك استخدام حقل البحث في شريط التنقل.)</span><span class="sxs-lookup"><span data-stu-id="f258a-200">(To quickly open that page, you can use the search field on the navigation bar.)</span></span>
    >
    > ![تغيير الحد الأقصى لحجم الملف](./media/hr-benefits-management-aca-maximum-file-size.png)

3. <span data-ttu-id="f258a-202">لفحص حاله التقارير وعرضها، استخدم حقل البحث في شريط التنقل لفتح صفحة **وظائف التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="f258a-202">To check the status of your reports and view them, use the search field on the navigation bar to open the **Electronic reporting jobs** page.</span></span>

    ![البحث عن الصفحة مهام التقارير الإلكترونية](./media/hr-benefits-management-aca-search-electronic-reporting-jobs.png)

4. <span data-ttu-id="f258a-204">حدد التقرير المراد عرضه، ثم حدد **إظهار الملفات**.</span><span class="sxs-lookup"><span data-stu-id="f258a-204">Select the report to view, and then select **Show files**.</span></span>

    ![إظهار الملفات](./media/hr-benefits-management-aca-show-files.png)

5. <span data-ttu-id="f258a-206">حدد **فتح**.</span><span class="sxs-lookup"><span data-stu-id="f258a-206">Select **Open**.</span></span>

    ![فتح ملف](./media/hr-benefits-management-aca-open-file.png)

6. <span data-ttu-id="f258a-208">من شريط الإخطارات الذي يظهر أسفل اطار المستعرض، افتح ملف zip، ثم حدد التقرير.</span><span class="sxs-lookup"><span data-stu-id="f258a-208">From the Notification bar that appears at the bottom of the browser window, open the zip file, and then select the report.</span></span> <span data-ttu-id="f258a-209">يمكنك عرض أو طباعة ملف PDF.</span><span class="sxs-lookup"><span data-stu-id="f258a-209">You can view or print the PDF file.</span></span>

    ![مثال نموذج 1095-C](./media/hr-benefits-management-aca-1095-c-form.png)

## <a name="view-aca-coverage-information"></a><span data-ttu-id="f258a-211">عرض معلومات تغطية الرعاية ميسورة التكلفة</span><span class="sxs-lookup"><span data-stu-id="f258a-211">View ACA coverage information</span></span>

<span data-ttu-id="f258a-212">تعرض صفحة **تغطية الرعاية ميسورة التكلفة** المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="f258a-212">The **Worker Affordable Care coverage** page shows the following information:</span></span>

- <span data-ttu-id="f258a-213">الموظفون الذين تم تعيينهم لكل مجموعة تغطية</span><span class="sxs-lookup"><span data-stu-id="f258a-213">Employees who are assigned to each coverage group</span></span>
- <span data-ttu-id="f258a-214">الموظفون الذين لم يتم تضمينهم في تقرير</span><span class="sxs-lookup"><span data-stu-id="f258a-214">Employees who don't have to be included on a report</span></span>
- <span data-ttu-id="f258a-215">الموظفون غير المعينون</span><span class="sxs-lookup"><span data-stu-id="f258a-215">Unassigned employees</span></span>

<span data-ttu-id="f258a-216">لعرض هذه المعلومات، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="f258a-216">To view this information, follow these steps.</span></span>

1. <span data-ttu-id="f258a-217">في مساحة عمل **إدارة الميزات**، حدد **تغطية الرعاية ميسورة التكلفة للعامل**.</span><span class="sxs-lookup"><span data-stu-id="f258a-217">In the **Benefits management** workspace, select **Worker Affordable Care coverage**.</span></span>
2. <span data-ttu-id="f258a-218">في الحقل **اسم المجموعة**، حدد مجموعة.</span><span class="sxs-lookup"><span data-stu-id="f258a-218">In the **Group name** field, select a group.</span></span>

    ![عرض تغطية الرعاية ميسورة التكلفة](./media/hr-benefits-management-aca-view-coverage.png)

<span data-ttu-id="f258a-220">إذا تم تجاوز أي من القيم الافتراضية من مجموعة التغطية التي يشملها قانون الرعاية ميسورة التكلفة‬، فستظهر علامة نجمية بجوار القيمة التي تم تغييرها.</span><span class="sxs-lookup"><span data-stu-id="f258a-220">If any default values from the Affordable Care coverage group have been overridden, an asterisk appears next to the value that was changed.</span></span> <span data-ttu-id="f258a-221">إذا كانت القيم هي نفسها لفترة 12 شهرًا ولم يتم تجاوزها، فستظهر القيمة في عمود **جميع الاثنى عشر شهرًا‬**.</span><span class="sxs-lookup"><span data-stu-id="f258a-221">If the values for all 12 months are the same and haven't been overridden, the value appears in the **All 12 months** column.</span></span>

<span data-ttu-id="f258a-222">يمكنك عرض الموظفين الذين تم وضع علامة عليهم باعتبارهم غير خاضعين لتقرير ACA، والذين لا يتطلبون نموذج 1095-C.</span><span class="sxs-lookup"><span data-stu-id="f258a-222">You can view employees who are marked as not ACA-reportable, and who won't require a Form 1095-C.</span></span> <span data-ttu-id="f258a-223">في حقل **تصفية حسب**، حدد **غير خاضع لتقرير ACA**.</span><span class="sxs-lookup"><span data-stu-id="f258a-223">In the **Filter by** field, select **Not ACA reportable**.</span></span>

<span data-ttu-id="f258a-224">يمكنك عرض الموظفين الذين لم يتم تعيينهم إلى مجموعة أو الذين تم تعيينهم لمجموعة منتهية الصلاحية.</span><span class="sxs-lookup"><span data-stu-id="f258a-224">You can view employees who aren't assigned to a group, or who are assigned to an expired group.</span></span> <span data-ttu-id="f258a-225">في حقل **تصفية حسب**، حدد **مجموعة غير معينه أو منتهية الصلاحية**.</span><span class="sxs-lookup"><span data-stu-id="f258a-225">In the **Filter by** field, select **Unassigned or expired group**.</span></span>

### <a name="export-to-excel"></a><span data-ttu-id="f258a-226">تصدير إلى Excel</span><span class="sxs-lookup"><span data-stu-id="f258a-226">Export to Excel</span></span>

<span data-ttu-id="f258a-227">لتصدير أي من القوائم إلى Microsoft Excel، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="f258a-227">To export any of the lists to Microsoft Excel, follow these steps.</span></span>

1. <span data-ttu-id="f258a-228">حدد الزر **فتح في Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="f258a-228">Select the **Open in Microsoft Office** button.</span></span>
2. <span data-ttu-id="f258a-229">حدد **جدول HCM مؤقت للموارد البشرية للاستخدام الداخلي**.</span><span class="sxs-lookup"><span data-stu-id="f258a-229">Select **HCM Human Resources temporary table for internal use**.</span></span>
3. <span data-ttu-id="f258a-230">حدد **تنزيل**.</span><span class="sxs-lookup"><span data-stu-id="f258a-230">Select **Download**.</span></span>

### <a name="view-aca-reportable-dependents"></a><span data-ttu-id="f258a-231">عرض المعالين الخاضعين لتقرير ACA</span><span class="sxs-lookup"><span data-stu-id="f258a-231">View ACA-reportable dependents</span></span>

<span data-ttu-id="f258a-232">إذا كان يجب عليك رفع تقرير بالأشخاص الذين تمت تغطيتهم نظرًا لأنك توفر تغطية ذاتية التأمين، فيمكنك عرض أي معالين تجري تغطيتهم تحت خطط الفوائد المعلمة على أنها **‬‏‫خاضعة لتقرير ACA**.</span><span class="sxs-lookup"><span data-stu-id="f258a-232">If you must report covered individuals because you provide self-insured coverage, you can view dependents who are covered under benefit plans that are marked as **ACA reportable**.</span></span> <span data-ttu-id="f258a-233">في جزء الإجراءات، حدد **عرض تغطية المعالين**.</span><span class="sxs-lookup"><span data-stu-id="f258a-233">On the Action Pane, select **View Dependent coverage**.</span></span>

![عرض تغطية المعالين](./media/hr-benefits-management-aca-view-dependent-coverage.png)

<span data-ttu-id="f258a-235">يتم عرض معلومات التغطية الخاصة بالمعالين للموظف.</span><span class="sxs-lookup"><span data-stu-id="f258a-235">Coverage information for the employee's dependents is shown.</span></span>

![تغطية المعال](./media/hr-benefits-management-aca-dependents.png)

> [!NOTE]
> <span data-ttu-id="f258a-237">تعرض الصفحة فقط خطط الميزات التي تم تمييزها على أنها **خاضع لتقرير ACA**.</span><span class="sxs-lookup"><span data-stu-id="f258a-237">The page shows only benefits plans that are marked as **ACA reportable**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]