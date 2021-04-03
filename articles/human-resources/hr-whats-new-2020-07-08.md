---
title: ما الجديد والمتغير في Dynamics 365 Human Resources (08 يوليو 2020)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 8 يوليو 2020.
author: andreabichsel
manager: tfehr
ms.date: 07/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9715f332088b7b5340f4252af5f789d226d90ff2
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463588"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-8-2020"></a><span data-ttu-id="ef4b5-103">ما الجديد والمتغير في Dynamics 365 Human Resources (8 يوليو 2020)</span><span class="sxs-lookup"><span data-stu-id="ef4b5-103">What's new or changed in Dynamics 365 Human Resources (July 8, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="ef4b5-104">يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="ef4b5-105">يتم تطبيق التغييرات على رقم الإصدار 8.1.3382.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-105">Changes apply to build number 8.1.3382.</span></span> <span data-ttu-id="ef4b5-106">تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام دعم LCS للحصول على مرجع.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="database-logging"></a><span data-ttu-id="ef4b5-107">تسجيل قاعدة البيانات</span><span class="sxs-lookup"><span data-stu-id="ef4b5-107">Database logging</span></span>

<span data-ttu-id="ef4b5-108">يسمح تسجيل قاعدة البيانات بتحديد الجدول والحقول التي يجب مراقبتها.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-108">Database logging allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="ef4b5-109">كما تسمح لك بتحديد الأحداث التي يجب أن تشغّل تعقب التغييرات.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-109">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="ef4b5-110">يمكنك استخدام إمكانيات تسجيل قاعده البيانات لرؤية هذه التغييرات بمرور الوقت.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-110">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="ef4b5-111">لمزيد من المعلومات، راجع [‏‫تكوين وإدارة تسجيل قاعده البيانات‬](hr-admin-database-logging.md).</span><span class="sxs-lookup"><span data-stu-id="ef4b5-111">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="ef4b5-112">تكوين اسم الخدمة الذاتية للموظف</span><span class="sxs-lookup"><span data-stu-id="ef4b5-112">Configure the name of Employee self service</span></span>

<span data-ttu-id="ef4b5-113">في **معلمات الموارد البشرية**، يمكنك الآن تغيير اسم مساحة عمل **الخدمة الذاتية للموظف** ليصبح **الخدمة الذاتية**.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-113">In **Human Resources parameters**, you can now change the name of the **Employee self service** workspace to **Self service**.</span></span> <span data-ttu-id="ef4b5-114">لمزيد من المعلومات، راجع [تغيير اسم مساحة عمل الخدمة الذاتية للموظف](hr-employee-self-service-workspace-name.md)</span><span class="sxs-lookup"><span data-stu-id="ef4b5-114">For more information, see [Change Employee self service workspace name](hr-employee-self-service-workspace-name.md)</span></span>

## <a name="benefits-management-open-enrollment-access-outside-of-period"></a><span data-ttu-id="ef4b5-115">الوصول إلى التسجيل المفتوح لإدارة الميزات خارج الفترة</span><span class="sxs-lookup"><span data-stu-id="ef4b5-115">Benefits management open enrollment access outside of period</span></span>

<span data-ttu-id="ef4b5-116">يعمل هذا الإصدار على إصلاح خطأ حيث يمكن للموظفين الوصول إلى التسجيل المفتوح للميزات خارج فترة التسجيل أو من دون حدث حياة.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-116">This release fixes a bug where employees could access benefits open enrollment outside of the enrollment period or without a life event.</span></span> <span data-ttu-id="ef4b5-117">ونتيجة لذلك، إذا كنت بحاجة إلى عرض التسجيل المفتوح في الخدمة الذاتية للموظف، يجب تعديل تواريخ التسجيل المفتوح إلى اليوم (أو قبل ذلك) لتمكين الوصول إليه.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-117">As a result, if you need to demo open enrollment in Employee self service, you must adjust the open enrollment dates to today (or earlier) to make it accessible.</span></span> <span data-ttu-id="ef4b5-118">يمكنك تغيير هذا الإعداد ضمن **إدارة الميزات > فترات القواعد والخيارات**.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-118">You can change this setting under **Benefits management > Rules and options periods**.</span></span>

## <a name="email-employee-enrollment-confirmation"></a><span data-ttu-id="ef4b5-119">إرسال بريد إلكتروني لتأكيد تسجيل الموظف</span><span class="sxs-lookup"><span data-stu-id="ef4b5-119">Email employee enrollment confirmation</span></span>

<span data-ttu-id="ef4b5-120">يمكنك الآن إرسال رسائل بريد إلكتروني إلى الموظفين بعد إكمال تحديد ميزاتهم.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-120">You can now send emails to employees after they complete their benefits selection.</span></span> <span data-ttu-id="ef4b5-121">يمكنك إرسال رسالة افتراضية أو استخدام قالب بريد إلكتروني للمؤسسة.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-121">You can either send a default message or use an organization email template.</span></span> <span data-ttu-id="ef4b5-122">توجد هذه الإعدادات ضمن **معلمات الموارد البشرية > إدارة الميزات**.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-122">These settings are under **Human resource parameters > Benefits management**.</span></span>

## <a name="canceled-leave-still-appears-in-upcoming-time-off-on-people-workspace-441358"></a><span data-ttu-id="ef4b5-123">لا تزال الإجازة الملغية تظهر في الإجازة القادمة في مساحة عمل الأشخاص (441358)</span><span class="sxs-lookup"><span data-stu-id="ef4b5-123">Canceled leave still appears in upcoming time off on People workspace (441358)</span></span>

<span data-ttu-id="ef4b5-124">لم تعد الإجازات الملغية تظهر كإجازات قادمة في بطاقات الإجازات في مساحة عمل **الأشخاص**.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-124">Canceled leave no longer displays as upcoming time off on the leave cards in the **People** workspace.</span></span>

## <a name="unable-to-use-the-department-entity-property-in-the-positionv2-entity-456486"></a><span data-ttu-id="ef4b5-125">غير قادر على استخدام خاصية كيان القسم في الكيان PositionV2 (456486)</span><span class="sxs-lookup"><span data-stu-id="ef4b5-125">Unable to use the department entity property in the PositionV2 entity (456486)</span></span>

<span data-ttu-id="ef4b5-126">يمكنك الآن إضافة قسم دون إنشاء علاقة مكررة.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-126">You can now add a department without creating a duplicate relation.</span></span>

## <a name="payrollworkerenrolledbenefitdetailentity-should-only-use-calculated-field-for-retirement-plans-459779"></a><span data-ttu-id="ef4b5-127">لا ينبغي لـ PayrollWorkerEnrolledBenefitDetailEntity إلا استخدام الحقل المحسوب لخطط التقاعد (459779)</span><span class="sxs-lookup"><span data-stu-id="ef4b5-127">PayrollWorkerEnrolledBenefitDetailEntity should only use calculated field for retirement plans (459779)</span></span>

<span data-ttu-id="ef4b5-128">عند تصدير الكيان **PayrollWorkerEnrolledBenefitDetailEntity**، يحدد التصدير ما إذا كان ينبغي استخدام حقل محسوب يستند إلى جدول أسعار أم استخدام الحقل **ContributionAmountCur** في الجدول المساعد.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-128">When exporting the **PayrollWorkerEnrolledBenefitDetailEntity** entity, the export determines whether it should use a calculated field based on a rate table or use the **ContributionAmountCur** field on the backing table.</span></span> <span data-ttu-id="ef4b5-129">يستخدم المنطق الذي يستخدمه كيان البيانات جدول الأسعار في المواقف التي لا يتم فيها التطبيق بصورة طبيعية.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-129">The logic used by the data entity uses the rate table in situations where the application normally doesn't.</span></span> <span data-ttu-id="ef4b5-130">يؤدي هذا المنطق إلى إرجاع صادرات الكيان إلى القيمة صفر لهذا العمود، وذلك نظرًا لعدم وجود جدول أسعار حساب وعدم إتاحة المنتج للعميل بتحديد واحد.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-130">This logic causes the entity exports to return a zero value for this column, because there's no calculation rate table and the product doesn't allow the customer to specify one.</span></span>
 
## <a name="confusing-translations-in-czech-language-in-personnel-management-and-employee-self-service-400276"></a><span data-ttu-id="ef4b5-131">الترجمات المحيرة في اللغة التشيكية لإدارة العاملين والخدمة الذاتية للموظف (400276)</span><span class="sxs-lookup"><span data-stu-id="ef4b5-131">Confusing translations in Czech language in Personnel management and Employee self service (400276)</span></span>

<span data-ttu-id="ef4b5-132">يصحح هذا الإصدار الترجمات **لدليل الشركة** و **الدورة التدريبية المسجلة التالية** و **الوظيفة** و **المنصب**.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-132">This release corrects the translations for **Company directory**, **Next registered course**, **Job**, and **Position**.</span></span>
 
## <a name="the-workcalendaremployment-table-doesnt-have-the-created-and-modified-system-fields-enabled-460171"></a><span data-ttu-id="ef4b5-133">لا يحتوي الجدول WorkCalendarEmployment على حقول النظام المُمكَّنة التي تم إنشاؤها وتعديلها (460171)</span><span class="sxs-lookup"><span data-stu-id="ef4b5-133">The WorkCalendarEmployment table doesn't have the created and modified system fields enabled (460171)</span></span>

<span data-ttu-id="ef4b5-134">حقول النظام التي تم إنشاؤها وتعديلها في الجدول **WorkCalendarEmployment** في الموارد البشرية قيد التمكين الآن.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-134">Created and modified system fields are now enabled on the **WorkCalendarEmployment** table in Human Resources.</span></span>
 
## <a name="null-reference-exception-for-hire-and-add-details-for-future-employee-455475"></a><span data-ttu-id="ef4b5-135">استثناء مرجع فارغ للتعيين وإضافة تفاصيل للموظف المستقبلي (455475)</span><span class="sxs-lookup"><span data-stu-id="ef4b5-135">Null reference exception for Hire and add details for future employee (455475)</span></span>

<span data-ttu-id="ef4b5-136">يعمل هذا الإصدار على تصحيح خطأ (مرجع فارغ) في إدخال الموظف بشكل مبسط عند تعيين موظف باستخدام الخيار **للتعيين وإضافة تفاصيل**.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-136">This release corrects an error (null reference) in streamlined employee entry when you hire an employee using the option to **Hire and add details**.</span></span>

## <a name="changes-made-in-the-dataverse-worker-entity-dont-reflect-in-human-resources-455652"></a><span data-ttu-id="ef4b5-137">لا يتم عرض التغييرات التي يتم إجراؤها على كيان عامل Dataverse في الموارد البشرية (455652)</span><span class="sxs-lookup"><span data-stu-id="ef4b5-137">Changes made in the Dataverse Worker entity don't reflect in Human Resources (455652)</span></span>

<span data-ttu-id="ef4b5-138">ستظهر الآن التغييرات التي تم إجراؤها على الحقول التالية في كيان **العامل** في Dataverse في الموارد البشرية:</span><span class="sxs-lookup"><span data-stu-id="ef4b5-138">Changes made to the following fields in the **Worker** entity in Dataverse will now show up in Human Resources:</span></span>

- <span data-ttu-id="ef4b5-139">**العمل من المنزل**</span><span class="sxs-lookup"><span data-stu-id="ef4b5-139">**Works from home**</span></span>
- <span data-ttu-id="ef4b5-140">**تاريخ الأقدمية**</span><span class="sxs-lookup"><span data-stu-id="ef4b5-140">**Seniority date**</span></span>
- <span data-ttu-id="ef4b5-141">**تاريخ الذكرى السنوية**</span><span class="sxs-lookup"><span data-stu-id="ef4b5-141">**Anniversary date**</span></span>
- <span data-ttu-id="ef4b5-142">**تاريخ التوظيف الأصلي**</span><span class="sxs-lookup"><span data-stu-id="ef4b5-142">**Original hire date**</span></span>

## <a name="correct-compensation-level-doesnt-default-based-on-the-job-assigned-to-the-position-394136"></a><span data-ttu-id="ef4b5-143">لا يعتمد مستوى التعويض الصحيح افتراضيًا على الوظيفة المعينة للمنصب (394136)</span><span class="sxs-lookup"><span data-stu-id="ef4b5-143">Correct compensation level doesn't default based on the job assigned to the position (394136)</span></span>

<span data-ttu-id="ef4b5-144">وبهذا التغيير، تعتمد القيم الافتراضية لمستويات التعويضات الصحيحة على سجلات **تاريخ السريان** **لتفاصيل المنصب** و **تاريخ بدء** **تعيين خطة التعويض**.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-144">With this change, the correct compensation level defaults based on the **Date effective** records for the **Position details** and the **Start date** of the **Compensation plan assignment**.</span></span>

## <a name="in-preview"></a><span data-ttu-id="ef4b5-145">قيد المعاينة</span><span class="sxs-lookup"><span data-stu-id="ef4b5-145">In preview</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="ef4b5-146">حقول إلزامية</span><span class="sxs-lookup"><span data-stu-id="ef4b5-146">Mandatory fields</span></span> 

<span data-ttu-id="ef4b5-147">يمكنك الآن جعل الحقول إلزامية باستخدام إمكانيات إضفاء طابع شخصي للموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-147">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="ef4b5-148">تتطلب هذه الميزة **طرق عرض محفوظة**.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-148">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="ef4b5-149">تطبيق Human Resources في Teams</span><span class="sxs-lookup"><span data-stu-id="ef4b5-149">Human Resources application in Teams</span></span>

<span data-ttu-id="ef4b5-150">بإمكان الموظفين عرض وطلب الوقت بعيدًا عن العمل ضمن Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="ef4b5-150">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="ef4b5-151">يمكنهم التفاعل مع روبوت لإنشاء طلبات الإجازات.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-151">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="ef4b5-152">لمزيد من المعلومات، راجع [تطبيق Human Resources في Teams‎](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="ef4b5-152">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="ef4b5-153">كيانات إطار عمل إدارة البيانات (DMF) لإدارة المزايا</span><span class="sxs-lookup"><span data-stu-id="ef4b5-153">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="ef4b5-154">يتم إصدار كيانات إدارة المزايا.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-154">Benefits management entities are releasing.</span></span> <span data-ttu-id="ef4b5-155">تتيح كيانات DMF استيراد البيانات وتصديرها لتكوين إدارة المزايا بسهولة.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-155">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="ef4b5-156">كما سيتوفر قالب إدارة المزايا لنقل البيانات.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-156">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="ef4b5-157">يقوم هذا القالب بتصدير البيانات واستيرادها بطريقة تسلسلية لمراعاة تبعيات البيانات.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-157">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="ef4b5-158">شراء الإجازة وبيعها</span><span class="sxs-lookup"><span data-stu-id="ef4b5-158">Buy and sell leave</span></span> 

<span data-ttu-id="ef4b5-159">توفر بعض المؤسسات ميزة تتيح للموظفين شراء الإجازات أو بيعها.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-159">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="ef4b5-160">غالبا ما تُدار هذه العملية يدويًا.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-160">This process is often managed manually.</span></span> <span data-ttu-id="ef4b5-161">تقوم هذه الميزة بأتمتة سياسات وطلبات الإدارة الخاصة بقسم الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-161">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="ef4b5-162">إذا تُبسط عملية عملية إدارة الإجازات وتساعد علي تقليل الأخطاء.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-162">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="ef4b5-163">لمزيد من المعلومات، راجع:</span><span class="sxs-lookup"><span data-stu-id="ef4b5-163">For more information, see:</span></span>

- [<span data-ttu-id="ef4b5-164">إدارة سياسات شراء الإجازة وبيعها</span><span class="sxs-lookup"><span data-stu-id="ef4b5-164">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="ef4b5-165">شراء الإجازة وبيعها</span><span class="sxs-lookup"><span data-stu-id="ef4b5-165">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="ef4b5-166">استحقاق الإجازة‬‏‫ لشركة فردية أو خطة فردية</span><span class="sxs-lookup"><span data-stu-id="ef4b5-166">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="ef4b5-167">يمكن للعملاء معالجة الاستحقاقات لشركة فردية أو إجازة فردية وخطه غياب.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-167">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="ef4b5-168">وبذلك تصبح عملية الاستحقاق واضحة للعملاء الذين لديهم سياسات مختلفة تتعلق بسنوات الإجازة أو استحقاقات الإجازات.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-168">This ability provides clarity for the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="ef4b5-169">لمزيد من المعلومات، راجع [‏‫استحقاق الإجازات لكل شركة أو خطة إجازة‬](hr-leave-and-absence-accrue.md).</span><span class="sxs-lookup"><span data-stu-id="ef4b5-169">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="ef4b5-170">إضافة مرفقات إلى طلبات الإجازة</span><span class="sxs-lookup"><span data-stu-id="ef4b5-170">Add attachments to time-off requests</span></span>

<span data-ttu-id="ef4b5-171">تعد القدرة على إضافه مرفقات إلى طلبات الإجازات المعتمدة عاملا مهما في بيئة مرض كوفيد-19 الحالي.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-171">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="ef4b5-172">يمكن للموظفين الآن إضافه هذه المرفقات.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-172">Employees can now add these attachments.</span></span> <span data-ttu-id="ef4b5-173">كما يتوفر لديهم المعرفة الكافية حول كيفية إجراء التحديثات على طلبات الإجازات.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-173">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="ef4b5-174">لمزيد من المعلومات، راجع [‏‫إضافة مرفق إلى طلب موجود‬](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="ef4b5-174">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="ef4b5-175">إضافة كود السبب إلى تعليقات الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="ef4b5-175">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="ef4b5-176">تمت إضافه أكواد السبب إلى تعليق الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-176">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="ef4b5-177">قواعد نقل الإجازة</span><span class="sxs-lookup"><span data-stu-id="ef4b5-177">Carry forward rules</span></span> 

<span data-ttu-id="ef4b5-178">يمكنك تحديد نوع الإجازة المنقولة للأرصدة المنقولة حيث يتم تحويل تسويات النقل.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-178">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="ef4b5-179">على سبيل المثال، إذا قام أحد الموظفين بنقل إجازة من 10 أيام، يمكنك انتقاء نوع إجازة آخر لمدة العشرة أيام هذه.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-179">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="ef4b5-180">لمزيد من المعلومات، راجع [تكوين أنواع الإجازة والغياب](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="ef4b5-180">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="ef4b5-181">تعليق استحقاق الإجازه لأنواع الإجازات المحددة</span><span class="sxs-lookup"><span data-stu-id="ef4b5-181">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="ef4b5-182">يمكن للموارد البشرية إنشاء قاعده لكي يتم تعليق استحقاق الإجازات للموظفين الذين لديهم طلبات الاجازه التي تم إدخالها لإجازه غير مدفوعة.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-182">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="ef4b5-183">يمكن أن تكون الإجازة غير المدفوع نوعا، ولكن ليس من الضروري أن تكون كذلك.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-183">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="ef4b5-184">يمكنك تعليق أي إجازة استنادا إلى نوع إجازة آخر.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-184">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="ef4b5-185">يتوفر كيان DMF لتعليقات الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="ef4b5-185">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="ef4b5-186">يتوفر كيان DMF الآن لتعليقات الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-186">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="ef4b5-187">قريبًا</span><span class="sxs-lookup"><span data-stu-id="ef4b5-187">Coming soon</span></span>

## <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="ef4b5-188">تضمين كيانات قائمة الاختيار في Dataverse</span><span class="sxs-lookup"><span data-stu-id="ef4b5-188">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="ef4b5-189">ستتوفر كيانات قائمة الاختيار لعمليات الإلحاق وإلغاء الإلحاق والتحويلات وعمليات الأعمال قريبًا في Dataverse.</span><span class="sxs-lookup"><span data-stu-id="ef4b5-189">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

## <a name="see-also"></a><span data-ttu-id="ef4b5-190">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="ef4b5-190">See also</span></span>

[<span data-ttu-id="ef4b5-191">المزايا الجديدة أو المتغيرة في Human Resources</span><span class="sxs-lookup"><span data-stu-id="ef4b5-191">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="ef4b5-192">نظره عامة حول الموجة 2 من إصدار Dynamics 365 Human Resources  2019</span><span class="sxs-lookup"><span data-stu-id="ef4b5-192">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="ef4b5-193">تحديث العملية</span><span class="sxs-lookup"><span data-stu-id="ef4b5-193">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="ef4b5-194">إدارة الميزات</span><span class="sxs-lookup"><span data-stu-id="ef4b5-194">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]