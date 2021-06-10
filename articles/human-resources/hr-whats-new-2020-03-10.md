---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources (10 مارس 2020)
description: يصف هذا المقال الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 10 مارس 2020.
author: andreabichsel
ms.date: 03/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-03-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 296e11befb0dc916faab2eb0388188852bc3ceb6
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051082"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-10-2020"></a><span data-ttu-id="7b187-103">ما الجديد أو المتغير في Dynamics 365 Human Resources (10 مارس 2020)</span><span class="sxs-lookup"><span data-stu-id="7b187-103">What's new or changed in Dynamics 365 Human Resources (March 10, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="7b187-104">تصف هذه المقالة الميزات الجديدة أو المتغيرة في Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7b187-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="7b187-105">يتم تطبيق التغييرات على رقم الإصدار 8.1.2985.</span><span class="sxs-lookup"><span data-stu-id="7b187-105">Changes apply to build number 8.1.2985.</span></span> <span data-ttu-id="7b187-106">تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام دعم LCS للحصول على مرجع.</span><span class="sxs-lookup"><span data-stu-id="7b187-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="cant-access-skill-gap-analysis-report-394460"></a><span data-ttu-id="7b187-107">يتعذر الوصول إلى تقرير تحليل فروق المهارات (394460)</span><span class="sxs-lookup"><span data-stu-id="7b187-107">Can't access skill gap analysis report (394460)</span></span>

<span data-ttu-id="7b187-108">هذا التقرير غير مدعوم في Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7b187-108">This report isn't supported in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="7b187-109">تمت إزالة عنصر القائمة المطلوب لطباعة لتقرير SSRS.</span><span class="sxs-lookup"><span data-stu-id="7b187-109">The menu item to print the SSRS report is removed.</span></span>

## <a name="incorrect-message-accessing-the-getting-started-page-417950"></a><span data-ttu-id="7b187-110">رسالة غير صحيحة للوصول إلى صفحة بدء الاستخدام (417950)</span><span class="sxs-lookup"><span data-stu-id="7b187-110">Incorrect message accessing the Getting Started page (417950)</span></span>

<span data-ttu-id="7b187-111">مع هذا التغيير ، يقوم الأمان بإخفاء عنصر القائمة هذا إذا لم يكن لديك حق الوصول إلى النموذج</span><span class="sxs-lookup"><span data-stu-id="7b187-111">With this change, security hides this menu item if you don't have access to the form.</span></span>

## <a name="streamlined-task-maintenance-for-employees-380538"></a><span data-ttu-id="7b187-112">صيانة المهام بطريقة منظمة للموظفين (380538)</span><span class="sxs-lookup"><span data-stu-id="7b187-112">Streamlined task maintenance for employees (380538)</span></span>

<span data-ttu-id="7b187-113">يسرد نموذج صيانة مهام العامل كافة المهام الخاصة بموظف عبر الإعداد وإلغاء الإعداد والانتقالات وعمليات الأعمال.</span><span class="sxs-lookup"><span data-stu-id="7b187-113">The worker task maintenance form lists all tasks for an employee across onboarding, offboarding, transitions, and business processes.</span></span> <span data-ttu-id="7b187-114">يمكنك حذف حالة المهام أو إعادة تعيينها أو تحديثها.</span><span class="sxs-lookup"><span data-stu-id="7b187-114">You can delete, reassign, or update the status of tasks.</span></span>

<span data-ttu-id="7b187-115">مثال: بينجامين مارتن هو مسؤول المزايا.</span><span class="sxs-lookup"><span data-stu-id="7b187-115">Example: Benjamin Martin is a benefits administrator.</span></span> <span data-ttu-id="7b187-116">أثناء عملية إعداد الموظف، يتم إنشاء المهام لبينجامين لمراجعة مجموعة المزايا للموظف الجديد.</span><span class="sxs-lookup"><span data-stu-id="7b187-116">During employee onboarding, tasks are created for Benjamin to review the new employee’s benefit selection.</span></span> <span data-ttu-id="7b187-117">لدى بينجامين مهام سابقة أكلمها ومهام مستقبلية يحتاج إلى إكمالها.</span><span class="sxs-lookup"><span data-stu-id="7b187-117">Benjamin has past tasks that he's completed, and future tasks that he needs to complete.</span></span> <span data-ttu-id="7b187-118">قرر بينجامين مغادرة الشركة، لذا يجب إعادة تعيين مهامه أو ازالتها.</span><span class="sxs-lookup"><span data-stu-id="7b187-118">Benjamin decides to leave the company, so his tasks need to be either re-assigned or removed.</span></span> <span data-ttu-id="7b187-119">يسمح نموذج صيانة المهام (في جزء الإجراءات في نموذج **العامل**) بإعادة تعيين كافة مهام بينجامين إلى عامل آخر أو إزالتها.</span><span class="sxs-lookup"><span data-stu-id="7b187-119">The task maintenance form (in the action pane of the **Worker** form) allows all of Benjamin’s tasks to be re-assigned to another worker or removed.</span></span>  

## <a name="dataverse-solution-is-now-available-with-the-following-changes"></a><span data-ttu-id="7b187-120">يتوفر حل Dataverse الآن مع التغييرات التالية:</span><span class="sxs-lookup"><span data-stu-id="7b187-120">Dataverse solution is now available with the following changes:</span></span>

| <span data-ttu-id="7b187-121">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="7b187-121">Description</span></span> | <span data-ttu-id="7b187-122">تغيير</span><span class="sxs-lookup"><span data-stu-id="7b187-122">Change</span></span> |
| --- | --- |
| <span data-ttu-id="7b187-123">تغييرات كيان **الوظيفة/المنصب**</span><span class="sxs-lookup"><span data-stu-id="7b187-123">**Job/Position** entity changes</span></span> | <ul><li><span data-ttu-id="7b187-124">تم إضافة **منطقة التعويض**</span><span class="sxs-lookup"><span data-stu-id="7b187-124">**Compensation region** added</span></span></li>|
| <span data-ttu-id="7b187-125">تمت إضافة كيان **بُعد منصب الوظيفة**</span><span class="sxs-lookup"><span data-stu-id="7b187-125">**Job position dimension** entity added</span></span> | <ul><li><span data-ttu-id="7b187-126">تمت إضافة **الأبعاد المالية**</span><span class="sxs-lookup"><span data-stu-id="7b187-126">**Financial dimensions** added</span></span></li>
| <span data-ttu-id="7b187-127">تغييرات كيان **العامل**</span><span class="sxs-lookup"><span data-stu-id="7b187-127">**Worker** entity changes</span></span> | <ul><li><span data-ttu-id="7b187-128">تمت إضافة **تسلسل الاسم**</span><span class="sxs-lookup"><span data-stu-id="7b187-128">**Name sequence** added</span></span></li><li><span data-ttu-id="7b187-129">تم إضافة **الأعمال من الصفحة الرئيسية**</span><span class="sxs-lookup"><span data-stu-id="7b187-129">**Works from home** added</span></span></li><li><span data-ttu-id="7b187-130">تمت إضافة **اللغة**</span><span class="sxs-lookup"><span data-stu-id="7b187-130">**Language** added</span></span></li><li><span data-ttu-id="7b187-131">تمت إضافة **تاريخ الأقدمية**</span><span class="sxs-lookup"><span data-stu-id="7b187-131">**Seniority date** added</span></span></li><li><span data-ttu-id="7b187-132">تمت إضاف **تاريخ التفعيل السنوي**</span><span class="sxs-lookup"><span data-stu-id="7b187-132">**Anniversary date** added</span></span></li><li><span data-ttu-id="7b187-133">تمت إضافة **تاريخ التوظيف الأصلي**</span><span class="sxs-lookup"><span data-stu-id="7b187-133">**Original hire date** added</span></span></li></ul> |
| <span data-ttu-id="7b187-134">تغييرات كيان **التوظيف**</span><span class="sxs-lookup"><span data-stu-id="7b187-134">**Employment** entity changes</span></span> | <ul><li><span data-ttu-id="7b187-135">تمت إضافة **الأبعاد المالية**</span><span class="sxs-lookup"><span data-stu-id="7b187-135">**Financial dimensions** added</span></span></li><li><span data-ttu-id="7b187-136">تمت إضافة **سبب الإنهاء**</span><span class="sxs-lookup"><span data-stu-id="7b187-136">**Termination reason** added</span></span></li><li><span data-ttu-id="7b187-137">تمت إعادة تسمية **تاريخ الإنهاء** من **تاريخ الانتقال**</span><span class="sxs-lookup"><span data-stu-id="7b187-137">**Termination date** renamed from **Transition date**</span></span></li><li><span data-ttu-id="7b187-138">تمت إضافة **تاريخ فترة الاختبار**</span><span class="sxs-lookup"><span data-stu-id="7b187-138">**Probation date** added</span></span></li></ul> |
| <span data-ttu-id="7b187-139">تغييرات كيان **عنوان العامل**</span><span class="sxs-lookup"><span data-stu-id="7b187-139">**Worker address** entity changes</span></span> | <ul><li><span data-ttu-id="7b187-140">تمت إضافة **عنوان الشارع**</span><span class="sxs-lookup"><span data-stu-id="7b187-140">**Street address** added</span></span></li><li><span data-ttu-id="7b187-141">**سطر العنوان 1**، و **سطر العنوان 2**، و **سطر العنوان 3** المميز للإهلاك</span><span class="sxs-lookup"><span data-stu-id="7b187-141">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span></li></ul> |
| <span data-ttu-id="7b187-142">كيانات إعداد التعويض المتغيرة الجديدة</span><span class="sxs-lookup"><span data-stu-id="7b187-142">New variable compensation setup entities</span></span> | <ul><li><span data-ttu-id="7b187-143">**نوع خطة التعويض المتغير**</span><span class="sxs-lookup"><span data-stu-id="7b187-143">**Compensation variable plan type**</span></span></li><li><span data-ttu-id="7b187-144">**خطة التعويض المتغيرة**</span><span class="sxs-lookup"><span data-stu-id="7b187-144">**Compensation variable plan**</span></span></li><li><span data-ttu-id="7b187-145">**قواعد الاستحقاق**</span><span class="sxs-lookup"><span data-stu-id="7b187-145">**Vesting rules**</span></span></li><li><span data-ttu-id="7b187-146">**مستوى خطة التعويض المتغير**</span><span class="sxs-lookup"><span data-stu-id="7b187-146">**Compensation variable plan level**</span></span></li></ul> |
| <span data-ttu-id="7b187-147">كيان **توظيف تقويم العامل** الجديد</span><span class="sxs-lookup"><span data-stu-id="7b187-147">New **Worker calendar employment** entity</span></span> | <ul><li><span data-ttu-id="7b187-148">تمت إضافة **كيان تقويم العمل**</span><span class="sxs-lookup"><span data-stu-id="7b187-148">**Work calendar entity** added</span></span></li></ul> |
| <span data-ttu-id="7b187-149">كيان **تفاصيل المنصب في كشف الرواتب** الجديد</span><span class="sxs-lookup"><span data-stu-id="7b187-149">New **Payroll position detail** entity</span></span> | <ul><li><span data-ttu-id="7b187-150">تمت إضافة **تفاصيل المنصب في كشف الرواتب**</span><span class="sxs-lookup"><span data-stu-id="7b187-150">**Payroll position detail** added</span></span></li></ul> |
| <span data-ttu-id="7b187-151">كيان **العنوان** الجديد</span><span class="sxs-lookup"><span data-stu-id="7b187-151">New **Title** entity</span></span> | <ul><li><span data-ttu-id="7b187-152">تمت إضافة **العنوان**</span><span class="sxs-lookup"><span data-stu-id="7b187-152">**Title** added</span></span></li></ul> <span data-ttu-id="7b187-153">تم تضمين كيان **العنوان** الجديد في Dataverse ولكن لا تتم الإشارة إليها من الكيانين **منصب الوظيفة‬** أو **الوظيفة‬‏‎** في هذا الوقت.</span><span class="sxs-lookup"><span data-stu-id="7b187-153">The new **Title** entity is included in Dataverse but isn't referenced from the **Job Position** or **Job** entities at this time.</span></span> |

> [!NOTE]
> <span data-ttu-id="7b187-154">توفر الأبعاد المالية لكل من المنصب والتوظيف تكاملاً أحادي الاتجاه للتحديثات من Human Resources إلى Dataverse.</span><span class="sxs-lookup"><span data-stu-id="7b187-154">Financial dimensions for both positions and employment provide one-direction integration for updates from Human Resources to Dataverse.</span></span> <span data-ttu-id="7b187-155">في الوقت الحالي، لا تتم مزامنة تحديثات الأبعاد المالية من Dataverse إلى Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7b187-155">Financial dimensions updates don't currently synchronize from Dataverse to Human Resources.</span></span>

<span data-ttu-id="7b187-156">خلال الأسابيع القليلة التالية، ستتوفر هذه التغييرات الخاصة بالكيانات في كافة البيئات.</span><span class="sxs-lookup"><span data-stu-id="7b187-156">Over the next few weeks, these entity changes will be available in all environments.</span></span> <span data-ttu-id="7b187-157">لتثبيت حل Dataverse الأحدث لـ Human Resources:</span><span class="sxs-lookup"><span data-stu-id="7b187-157">To manually install the latest Dataverse solution for Human Resources:</span></span>

1.  <span data-ttu-id="7b187-158">انتقل إلى [مركز إدارة Power Platform](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="7b187-158">Go to the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).</span></span>

2.  <span data-ttu-id="7b187-159">حدد **بيئات**.</span><span class="sxs-lookup"><span data-stu-id="7b187-159">Select **Environments**.</span></span>

3.  <span data-ttu-id="7b187-160">ابحث عن البيئة التي تريد ترقيتها.</span><span class="sxs-lookup"><span data-stu-id="7b187-160">Find the environment you want to upgrade.</span></span> <span data-ttu-id="7b187-161">يجب أن تتطابق البيئة مع **اسم البيئة** في قسم **Dataverse المعلومات** في النموذج **حول** في Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7b187-161">The environment should correspond to **Environment name** in the **Dataverse information** section in the **About** form in Human Resources.</span></span>

4.  <span data-ttu-id="7b187-162">حدد البيئة لعرض تفاصيل البيئة.</span><span class="sxs-lookup"><span data-stu-id="7b187-162">Select the environment to view the environment details.</span></span>

5.  <span data-ttu-id="7b187-163">حدد **إدارة الحلول** في شريط الإجراءات في الجزء العلوي.</span><span class="sxs-lookup"><span data-stu-id="7b187-163">In the action bar at the top, select **Manage Solutions**.</span></span> <span data-ttu-id="7b187-164">ستفتح نافذة مستعرض جديدة وتنتقل إلى **مركز إدارة Dynamics 365** في سياق بيئتك.</span><span class="sxs-lookup"><span data-stu-id="7b187-164">A new browser window will open and navigate to **Dynamics 365 Administration Center** in the context of your environment.</span></span>

6.  <span data-ttu-id="7b187-165">في قائمة **الحل**، حدد **ارتساء Dynamics 365 Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="7b187-165">In the **Solution** list, select **Dynamics 365 Human Resources Anchor**.</span></span>

7.  <span data-ttu-id="7b187-166">حدد **ترقية** لتطبيق الحل الأخير.</span><span class="sxs-lookup"><span data-stu-id="7b187-166">Select **Upgrade** to apply the latest solution.</span></span>

## <a name="in-preview"></a><span data-ttu-id="7b187-167">قيد المعاينة</span><span class="sxs-lookup"><span data-stu-id="7b187-167">In preview</span></span>

<span data-ttu-id="7b187-168">تتوفر ميزات المعاينة التالية في 3 فبراير، 2020:</span><span class="sxs-lookup"><span data-stu-id="7b187-168">The following preview features are available on February 3, 2020:</span></span>

- <span data-ttu-id="7b187-169">**ميزات معاينة الغياب والإجازات** - لمزيد من المعلومات، راجع [ميزات معاينة الإجازات والغياب](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span><span class="sxs-lookup"><span data-stu-id="7b187-169">**Leave and absence preview features** - For more information, see [Leave and absence preview features](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span></span>

- <span data-ttu-id="7b187-170">**ميزة معاينة إدارة الميزات** - لمزيد من المعلومات، بما في ذلك المشكلات المعروفة، راجع [نظرة عامة على إدارة الميزات](hr-benefits-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7b187-170">**Benefits management preview feature** - For more information, including known issues, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>

## <a name="coming-soon"></a><span data-ttu-id="7b187-171">قريبًا</span><span class="sxs-lookup"><span data-stu-id="7b187-171">Coming Soon</span></span>

### <a name="platform-update-33"></a><span data-ttu-id="7b187-172">update 33 للنظام الأساسي</span><span class="sxs-lookup"><span data-stu-id="7b187-172">Platform update 33</span></span>

- <span data-ttu-id="7b187-173">تطبيقات الصفحة الكاملة (معاينة) - تسمح ميزة المعاينة هذه، التي تتطلب منك تمكين ميزة طرق العرض المحفوظة، بإضافة تطبيقات Power Apps وتطبيقات من جهة خارجية كتجارب صفحة كاملة عبر لوحة المعلومات.</span><span class="sxs-lookup"><span data-stu-id="7b187-173">Full page apps (Preview) - This preview feature, which requires you to enable the Saved views feature, allows Power Apps and third-party apps to be added as full-page experiences via the dashboard.</span></span>

- <span data-ttu-id="7b187-174">طرق العرض المحفوظة (معاينة) - تمكّن ميزة المعاينة طرق العرض المحفوظة، وهذا عبارة عن تحسين ملحوظ للنظام الفرعي للتخصيص.</span><span class="sxs-lookup"><span data-stu-id="7b187-174">Saved views (Preview) - This preview feature enables saved views, which is a significant enhancement to the personalization subsystem.</span></span> <span data-ttu-id="7b187-175">تسمح هذه الميزة للمستخدمين بالحصول على عدة مجموعات مسماة من التخصيصات لكل صفحة.</span><span class="sxs-lookup"><span data-stu-id="7b187-175">This feature allows users to have multiple named sets of personalizations per page.</span></span> <span data-ttu-id="7b187-176">يمكنك أيضًا نشر طرق العرض لأدوار الأمان.</span><span class="sxs-lookup"><span data-stu-id="7b187-176">You can also publish views to security roles.</span></span>

- <span data-ttu-id="7b187-177">تحسين تجربة التصفية "أحد مما يلي" - تمكن هذه الميزة ‏‫تحسين تجربة التصفية "أحد ما يلي"‬ التي تسهل إدخال قيم عوامل تصفية متعددة، وتشتمل على آلية أبسط لإزالة القيم الفردية أو جميع قيم عامل التصفية، كما تشتمل على مؤثرات عرض لقيم عامل التصفية أكثر بساطة وأصغر حجمًا.</span><span class="sxs-lookup"><span data-stu-id="7b187-177">Optimized "is one of" filtering experience - This feature enables an optimized "is one of" filtering experience that makes it easier to enter multiple filter values, has a simpler mechanism to remove individual or all filter values, and has a more compact and intuitive visualization of filter values.</span></span>

- <span data-ttu-id="7b187-178">الحقول المخصصة - يحتاج المستخدمون في أغلب الأحيان إلى إضافة حقول إلى شبكة أو صفحة.</span><span class="sxs-lookup"><span data-stu-id="7b187-178">Recommended fields - Users often need to add fields to a grid or page.</span></span> <span data-ttu-id="7b187-179">قد يكون هذا الأمر صعبًا مع وجود عدد كبير من الحقول المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="7b187-179">This can be difficult with so many available fields.</span></span> <span data-ttu-id="7b187-180">بدلاً من البحث عبر قائمة كبيرة، تسمح هذه الميزة للنظام بإظهار مجموعة من الحقول الموصى بها استنادًا إلى ما يضيفه المستخدمون الآخرون في أغلب الأحيان في سيناريوهات مماثلة.‬</span><span class="sxs-lookup"><span data-stu-id="7b187-180">Instead of having to search through a large list, this feature enables the system to surface a set of recommended fields based on what other users most often add in similar scenarios.</span></span>

- <span data-ttu-id="7b187-181">الإجراءات الافتراضية الثابتة في الشبكات‬ - تضمن هذه الميزة أن الإجراء الافتراضي في إحدى الشبكات مرتبط بعمود معين في شبكة، بغض النظر عما إذا كان قد تم نقل هذا العمود أو إخفاؤه.</span><span class="sxs-lookup"><span data-stu-id="7b187-181">Sticky default actions in grids - This feature ensures that the default action in a grid is linked to a specific column in a grid, regardless of whether that column is moved or hidden.</span></span>

## <a name="see-also"></a><span data-ttu-id="7b187-182">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="7b187-182">See also</span></span>

[<span data-ttu-id="7b187-183">المزايا الجديدة أو المتغيرة في Human Resources</span><span class="sxs-lookup"><span data-stu-id="7b187-183">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="7b187-184">نظره عامة حول الموجة 2 من إصدار Dynamics 365 Human Resources  2019</span><span class="sxs-lookup"><span data-stu-id="7b187-184">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="7b187-185">تحديث العملية</span><span class="sxs-lookup"><span data-stu-id="7b187-185">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="7b187-186">إدارة الميزات</span><span class="sxs-lookup"><span data-stu-id="7b187-186">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]