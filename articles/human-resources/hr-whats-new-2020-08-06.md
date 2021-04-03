---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources (06 أغسطس 2020)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 06 أغسطس 2020.
author: andreabichsel
manager: tfehr
ms.date: 08/06/2020
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
ms.search.validFrom: 2020-08-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 235af2d4d10687e9d7d7676c29c95428eab99b0a
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467713"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-06-2020"></a><span data-ttu-id="993c3-103">ما الجديد أو المتغير في Dynamics 365 Human Resources (06 أغسطس 2020)</span><span class="sxs-lookup"><span data-stu-id="993c3-103">What's new or changed in Dynamics 365 Human Resources (August 06, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="993c3-104">يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="993c3-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="993c3-105">يتم تطبيق التغييرات على رقم الإصدار 8.1.3444.</span><span class="sxs-lookup"><span data-stu-id="993c3-105">Changes apply to build number 8.1.3444.</span></span> <span data-ttu-id="993c3-106">تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام دعم LCS للحصول على مرجع.</span><span class="sxs-lookup"><span data-stu-id="993c3-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="platform-update-1001236-is-now-available"></a><span data-ttu-id="993c3-107">يتوفر الآن تحديث النظام الأساسي 10.0.12(36)</span><span class="sxs-lookup"><span data-stu-id="993c3-107">Platform update 10.0.12(36) is now available</span></span>

<span data-ttu-id="993c3-108">لمزيد من المعلومات، راجع [تحديثات النظام الأساسي للإصدار 10.0.12 من تطبيقات Finance and Operations (أغسطس 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-10-0-12).</span><span class="sxs-lookup"><span data-stu-id="993c3-108">For more information, see [Platform updates for version 10.0.12 of Finance and Operations apps (August 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-10-0-12).</span></span>

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="993c3-109">كيانات إطار عمل إدارة البيانات (DMF) لإدارة المزايا</span><span class="sxs-lookup"><span data-stu-id="993c3-109">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="993c3-110">يتم إصدار كيانات إدارة المزايا.</span><span class="sxs-lookup"><span data-stu-id="993c3-110">Benefits management entities are releasing.</span></span> <span data-ttu-id="993c3-111">تتيح كيانات DMF استيراد البيانات وتصديرها لتكوين إدارة المزايا بسهولة.</span><span class="sxs-lookup"><span data-stu-id="993c3-111">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="993c3-112">كما سيتوفر قالب إدارة المزايا لنقل البيانات.</span><span class="sxs-lookup"><span data-stu-id="993c3-112">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="993c3-113">يقوم هذا القالب بتصدير البيانات واستيرادها بطريقة تسلسلية لمراعاة تبعيات البيانات.</span><span class="sxs-lookup"><span data-stu-id="993c3-113">The template exports and imports the data sequentially to respect data dependencies.</span></span> <span data-ttu-id="993c3-114">لمزيد من المعلومات، راجع:</span><span class="sxs-lookup"><span data-stu-id="993c3-114">For more information, see:</span></span>

- <span data-ttu-id="993c3-115">[دعم كيان DMF](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/dmf-entity-support) في خطة الموجة 1 من إصدار 2020 لتطبيق Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="993c3-115">[DMF entity support](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/dmf-entity-support) in the Dynamics 365 2020 release wave 1 plan</span></span>
- [<span data-ttu-id="993c3-116">نظرة عامة حول إدارة البيانات</span><span class="sxs-lookup"><span data-stu-id="993c3-116">Data management overview</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages)


## <a name="claire-creates-a-workflow-for-buying-and-selling-leave-requests-446557"></a><span data-ttu-id="993c3-117">تقوم كلير بإنشاء سير عمل لطلبات شراء وبيع الإجازات (446557)</span><span class="sxs-lookup"><span data-stu-id="993c3-117">Claire creates a workflow for buying and selling leave requests (446557)</span></span>

<span data-ttu-id="993c3-118">لمزيد من المعلومات، راجع:</span><span class="sxs-lookup"><span data-stu-id="993c3-118">For more information, see:</span></span>

- <span data-ttu-id="993c3-119">[السماح للموظفين ببيع وشراء الإجازات](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/allow-employees-buy-sell-leave) في خطة الموجة 2 لإصدار 2020‬ لتطبيق Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="993c3-119">[Allow employees to buy and sell leave](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/allow-employees-buy-sell-leave) in the Dynamics 365 2020 release wave 2 plan</span></span>
- [<span data-ttu-id="993c3-120">إدارة سياسات شراء الإجازة وبيعها</span><span class="sxs-lookup"><span data-stu-id="993c3-120">Manage buy and sell leave policies</span></span>](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-manage-buy-and-sell-leave-policies)
- [<span data-ttu-id="993c3-121">شراء الإجازة وبيعها</span><span class="sxs-lookup"><span data-stu-id="993c3-121">Buy and sell leave</span></span>](https://docs.microsoft.com/dynamics365/human-resources/hr-employee-self-service-buy-sell-leave)


## <a name="worker-postal-addresses-v2-entity-has-access-across-legal-entities-with-restricted-access-459126"></a><span data-ttu-id="993c3-122">يتوفر للإصدار V2 من العناوين البريدية للعامل حق الوصول عبر الكيانات القانونية مع وصول مقيد (459126)</span><span class="sxs-lookup"><span data-stu-id="993c3-122">Worker postal addresses V2 entity has access across legal entities with restricted access (459126)</span></span>

<span data-ttu-id="993c3-123">ومع هذا التغيير، سيقوم كيان **الإصدار V2 من العنوان البريدي للعامل** بتقييد الوصول إلى الكيان القانوني الذي تم إعطاؤه للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="993c3-123">With this change, the **Worker postal address V2** entity will restrict based on the legal entity access given to the user.</span></span>

## <a name="workflow-email-hyperlink-fails-to-open-relevant-reviews-437398"></a><span data-ttu-id="993c3-124">فشل ارتباط البريد الإلكتروني لسير العمل بفتح مراجعات ذات صلة (437398)</span><span class="sxs-lookup"><span data-stu-id="993c3-124">Workflow email hyperlink fails to open relevant reviews (437398)</span></span>

<span data-ttu-id="993c3-125">عند استخدام العنصر النائب لفتح مراجعة أداء في سير عمل المراجعة، يقوم الآن الارتباط التشعبي الذي تم إنشاؤه في البريد الإلكتروني بفتح السجل المحدد.</span><span class="sxs-lookup"><span data-stu-id="993c3-125">When you use the placeholder to open a performance review in the review workflow, the hyperlink generated in the email now opens the selected record.</span></span>

## <a name="new-entities-for-buying-and-selling-leave-473180"></a><span data-ttu-id="993c3-126">كيانات جديدة لإجازات لبيع وشراء الإجازات (473180)</span><span class="sxs-lookup"><span data-stu-id="993c3-126">New entities for buying and selling leave (473180)</span></span>

<span data-ttu-id="993c3-127">تتوفر الآن كيانات إطار عمل إدارة البيانات لبيع وشراء الإجازات.</span><span class="sxs-lookup"><span data-stu-id="993c3-127">Data management framework entities are now available for buying and selling leave.</span></span> <span data-ttu-id="993c3-128">لمزيد من المعلومات، راجع [‏‫نظرة عامة على إدارة البيانات](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages).</span><span class="sxs-lookup"><span data-stu-id="993c3-128">For more information, see [Data management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages).</span></span>

## <a name="when-viewing-record-information-and-using-advanced-filters-a-user-could-gain-access-to-other-employees-records-472490"></a><span data-ttu-id="993c3-129">عند عرض معلومات السجل واستخدام عوامل التصفية المتقدمة، قد يصل المستخدم إلى سجلات الموظفين الآخرين (472490)</span><span class="sxs-lookup"><span data-stu-id="993c3-129">When viewing record information and using advanced filters, a user could gain access to other employees' records (472490)</span></span>

<span data-ttu-id="993c3-130">ومع هذا التغيير، يمكن لمستخدمي الخدمة الذاتية للموظفين الوصول إلى السجلات الخاصة بهم فقط أثناء استخدام الخدمة الذاتية للموظفين.</span><span class="sxs-lookup"><span data-stu-id="993c3-130">With this change, Employee self-service users can only access their own records while using employee self service.</span></span> <span data-ttu-id="993c3-131">لم يعد عرض معلومات السجل أثناء تغيير خيار التصفية لم يكشف عن بيانات إضافية.</span><span class="sxs-lookup"><span data-stu-id="993c3-131">Viewing record information while changing the filtering option no longer exposes additional data.</span></span>

## <a name="personnel-management-analytics-include-exited-worker-records-382893"></a><span data-ttu-id="993c3-132">تتضمن تحليلات إدارة العاملين سجلات العاملين المغادرين (382893)</span><span class="sxs-lookup"><span data-stu-id="993c3-132">Personnel management analytics include exited worker records (382893)</span></span>

<span data-ttu-id="993c3-133">مع هذا الإصدار، تتضمن تحليلات إدارة العاملين الآن العاملين النشطاء فقط.</span><span class="sxs-lookup"><span data-stu-id="993c3-133">With this release, personnel management analytics now only include active workers.</span></span> 
 
## <a name="unable-to-process-a-merit-increase-for-an-employee-473125"></a><span data-ttu-id="993c3-134">تعذّر معالجه زيادة الأهلية للموظف (473125)</span><span class="sxs-lookup"><span data-stu-id="993c3-134">Unable to process a merit increase for an employee (473125)</span></span>

<span data-ttu-id="993c3-135">يسمح لك هذا التغيير بإدخال زيادات الأهلية عند تغيير تاريخ السريان لزيادة الأهلية الجديدة.</span><span class="sxs-lookup"><span data-stu-id="993c3-135">This change allows you to enter merit increases when you change the effective date for the new merit increase.</span></span>

## <a name="review-workflow-can-be-started-more-than-once-467541"></a><span data-ttu-id="993c3-136">يمكن بدء سير عمل المراجعة أكثر من مرة (467541)</span><span class="sxs-lookup"><span data-stu-id="993c3-136">Review workflow can be started more than once (467541)</span></span>

<span data-ttu-id="993c3-137">مع هذا التغيير، يمكنك بدء سير عمل مراجعة الأداء مرة واحدة فقط.</span><span class="sxs-lookup"><span data-stu-id="993c3-137">With this change, you can only start the performance review workflow once.</span></span> <span data-ttu-id="993c3-138">لم تعد حالة المدير تعرض خيار بدء المراجعة.</span><span class="sxs-lookup"><span data-stu-id="993c3-138">The status for the manager no longer displays the option to begin the review.</span></span>

## <a name="leave-request-work-flow-ends-in-error-when-canceling-an-approved-leave-request-472063"></a><span data-ttu-id="993c3-139">ينتهي سير عمل طلب الإجازة عند إلغاء طلب إجازة موافق عليه (472063)</span><span class="sxs-lookup"><span data-stu-id="993c3-139">Leave request work flow ends in error when canceling an approved leave request (472063)</span></span>

<span data-ttu-id="993c3-140">في هذا الإصدار، عندما تلغي طلب إجازة موافق عليها، لن يعود الطلب بحالة موافق عليها، وسيستمر سير العمل.</span><span class="sxs-lookup"><span data-stu-id="993c3-140">In this release, when you cancel an approved leave request, the state of the request no longer remains approved, and the workflow will continue.</span></span>

## <a name="system-suggests-exited-workers-when-creating-a-new-review-form-the-template-460624"></a><span data-ttu-id="993c3-141">يقترح النظام عاملين مغادرين عند إنشاء مراجعة جديدة من القالب (460624)</span><span class="sxs-lookup"><span data-stu-id="993c3-141">System suggests exited workers when creating a new review form the template (460624)</span></span>

<span data-ttu-id="993c3-142">ومع هذا التغيير، لن يعود العاملون المغادرون متاحين عند إنشاء مراجعات جديدة من قالب.</span><span class="sxs-lookup"><span data-stu-id="993c3-142">With this change, exited workers are longer available when creating new reviews from a template.</span></span> <span data-ttu-id="993c3-143">لا يمكنك إنشاء مراجعات للموظفين الذين هم خارج تواريخ توظيفهم.</span><span class="sxs-lookup"><span data-stu-id="993c3-143">You can't create reviews for employees who are outside the dates of their employment.</span></span>

## <a name="position-hierarchy-circular-reference-detection-415879"></a><span data-ttu-id="993c3-144">الكشف عن المرجع الدائري للتدرج الهرمي للمناصب (415879)</span><span class="sxs-lookup"><span data-stu-id="993c3-144">Position hierarchy circular reference detection (415879)</span></span>

<span data-ttu-id="993c3-145">مع هذا التغيير، يقتصر الكشف عن المرجع الدائري للتدرج الهرمي للمناصب على وقت معين.</span><span class="sxs-lookup"><span data-stu-id="993c3-145">With this change, position hierarchy circular reference detection is limited to a single point in time.</span></span> <span data-ttu-id="993c3-146">يمكنك تشغيل الكشف عن المراجع الدائرية لتواريخ مختلفة للتحقق من عدم وجود أي مراجع دائرية في بنية التدرج الهرمي للمناصب.</span><span class="sxs-lookup"><span data-stu-id="993c3-146">You can run circular reference detection for different dates to verify the reporting structure doesn't have any circular references.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="993c3-147">شراء الإجازة وبيعها</span><span class="sxs-lookup"><span data-stu-id="993c3-147">Buy and sell leave</span></span> 

<span data-ttu-id="993c3-148">توفر بعض المؤسسات ميزة تتيح للموظفين شراء الإجازات أو بيعها.</span><span class="sxs-lookup"><span data-stu-id="993c3-148">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="993c3-149">غالبا ما تُدار هذه العملية يدويًا.</span><span class="sxs-lookup"><span data-stu-id="993c3-149">This process is often managed manually.</span></span> <span data-ttu-id="993c3-150">تقوم هذه الميزة بأتمتة سياسات وطلبات الإدارة الخاصة بقسم الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="993c3-150">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="993c3-151">إذا تُبسط عملية عملية إدارة الإجازات وتساعد علي تقليل الأخطاء.</span><span class="sxs-lookup"><span data-stu-id="993c3-151">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="993c3-152">لمزيد من المعلومات، راجع:</span><span class="sxs-lookup"><span data-stu-id="993c3-152">For more information, see:</span></span>

- <span data-ttu-id="993c3-153">[السماح للموظفين ببيع وشراء الإجازات](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/allow-employees-buy-sell-leave) في خطة الموجة 2 لإصدار 2020‬ لتطبيق Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="993c3-153">[Allow employees to buy and sell leave](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/allow-employees-buy-sell-leave) in the Dynamics 365 2020 release wave 2 plan</span></span>
- [<span data-ttu-id="993c3-154">إدارة سياسات شراء الإجازة وبيعها</span><span class="sxs-lookup"><span data-stu-id="993c3-154">Manage buy and sell leave policies</span></span>](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-manage-buy-and-sell-leave-policies)
- [<span data-ttu-id="993c3-155">شراء الإجازة وبيعها</span><span class="sxs-lookup"><span data-stu-id="993c3-155">Buy and sell leave</span></span>](https://docs.microsoft.com/dynamics365/human-resources/hr-employee-self-service-buy-sell-leave)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="993c3-156">استحقاق الإجازة‬‏‫ لشركة فردية أو خطة فردية</span><span class="sxs-lookup"><span data-stu-id="993c3-156">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="993c3-157">يمكن للعملاء معالجة الاستحقاقات لشركة فردية أو إجازة فردية وخطه غياب.</span><span class="sxs-lookup"><span data-stu-id="993c3-157">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="993c3-158">وبذلك تصبح عملية الاستحقاق واضحة للعملاء الذين لديهم سياسات مختلفة تتعلق بسنوات الإجازة أو استحقاقات الإجازات.</span><span class="sxs-lookup"><span data-stu-id="993c3-158">This ability provides clarity for the accrual process for customers with different leave years or leaves accrual policies.</span></span> <span data-ttu-id="993c3-159">لمزيد من المعلومات، راجع [‏‫استحقاق الإجازات لكل شركة أو خطة إجازة‬](hr-leave-and-absence-accrue.md).</span><span class="sxs-lookup"><span data-stu-id="993c3-159">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="993c3-160">إضافة مرفقات إلى طلبات الإجازة</span><span class="sxs-lookup"><span data-stu-id="993c3-160">Add attachments to time-off requests</span></span>

<span data-ttu-id="993c3-161">تعد القدرة على إضافه مرفقات إلى طلبات الإجازات المعتمدة عاملا مهما في بيئة مرض كوفيد-19 الحالي.</span><span class="sxs-lookup"><span data-stu-id="993c3-161">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="993c3-162">يمكن للموظفين الآن إضافه هذه المرفقات.</span><span class="sxs-lookup"><span data-stu-id="993c3-162">Employees can now add these attachments.</span></span> <span data-ttu-id="993c3-163">كما يتوفر لديهم المعرفة الكافية حول كيفية إجراء التحديثات على طلبات الإجازات.</span><span class="sxs-lookup"><span data-stu-id="993c3-163">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="993c3-164">لمزيد من المعلومات، راجع [‏‫إضافة مرفق إلى طلب موجود‬](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="993c3-164">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="993c3-165">إضافة كود السبب إلى تعليقات الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="993c3-165">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="993c3-166">تمت إضافه أكواد السبب إلى تعليق الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="993c3-166">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="993c3-167">قواعد نقل الإجازة</span><span class="sxs-lookup"><span data-stu-id="993c3-167">Carry forward rules</span></span> 

<span data-ttu-id="993c3-168">يمكنك تحديد نوع الإجازة المنقولة للأرصدة المنقولة حيث يتم تحويل تسويات النقل.</span><span class="sxs-lookup"><span data-stu-id="993c3-168">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="993c3-169">على سبيل المثال، إذا قام أحد الموظفين بنقل إجازة من 10 أيام، يمكنك انتقاء نوع إجازة آخر لمدة العشرة أيام هذه.</span><span class="sxs-lookup"><span data-stu-id="993c3-169">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="993c3-170">لمزيد من المعلومات، راجع [تكوين أنواع الإجازة والغياب](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="993c3-170">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="993c3-171">تعليق استحقاق الإجازه لأنواع الإجازات المحددة</span><span class="sxs-lookup"><span data-stu-id="993c3-171">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="993c3-172">يمكن للموارد البشرية إنشاء قاعده لكي يتم تعليق استحقاق الإجازات للموظفين الذين لديهم طلبات الاجازه التي تم إدخالها لإجازه غير مدفوعة.</span><span class="sxs-lookup"><span data-stu-id="993c3-172">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="993c3-173">يمكن أن تكون الإجازة غير المدفوع نوعا، ولكن ليس من الضروري أن تكون كذلك.</span><span class="sxs-lookup"><span data-stu-id="993c3-173">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="993c3-174">يمكنك تعليق أي إجازة استنادا إلى نوع إجازة آخر.</span><span class="sxs-lookup"><span data-stu-id="993c3-174">You can suspend any leave based on another leave type.</span></span>

## <a name="in-preview"></a><span data-ttu-id="993c3-175">قيد المعاينة</span><span class="sxs-lookup"><span data-stu-id="993c3-175">In preview</span></span>

### <a name="mandatory-fields"></a><span data-ttu-id="993c3-176">حقول إلزامية</span><span class="sxs-lookup"><span data-stu-id="993c3-176">Mandatory fields</span></span>

<span data-ttu-id="993c3-177">يمكنك جعل الحقول إلزامية باستخدام إمكانيات التخصيص في Human Resources.</span><span class="sxs-lookup"><span data-stu-id="993c3-177">You can make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="993c3-178">تتطلب هذه الميزة **طرق عرض محفوظة**.</span><span class="sxs-lookup"><span data-stu-id="993c3-178">This feature requires **Saved views**.</span></span> <span data-ttu-id="993c3-179">لمزيد من المعلومات حول طرق العرض المحفوظة، راجع:</span><span class="sxs-lookup"><span data-stu-id="993c3-179">For more information about saved views, see:</span></span>

- <span data-ttu-id="993c3-180">[طرق العرض المحفوظة - التوفر العام](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) في خطة الموجة 2 لإصدار 2020‬ لتطبيق Dynamics 365‬</span><span class="sxs-lookup"><span data-stu-id="993c3-180">[Saved views - general availability](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) in the Dynamics 365 2020 release wave 2 plan</span></span>
- [<span data-ttu-id="993c3-181">إنشاء نماذج تستخدم طرق العرض المحفوظة بشكل كامل</span><span class="sxs-lookup"><span data-stu-id="993c3-181">Build forms that fully utilize saved views</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/user-interface/understanding-saved-views)

### <a name="human-resources-application-in-teams"></a><span data-ttu-id="993c3-182">تطبيق Human Resources في Teams</span><span class="sxs-lookup"><span data-stu-id="993c3-182">Human Resources application in Teams</span></span>

<span data-ttu-id="993c3-183">بإمكان الموظفين عرض وطلب الوقت بعيدًا عن العمل ضمن Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="993c3-183">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="993c3-184">يمكنهم التفاعل مع روبوت لإنشاء طلبات الإجازات.</span><span class="sxs-lookup"><span data-stu-id="993c3-184">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="993c3-185">لمزيد من المعلومات، راجع:</span><span class="sxs-lookup"><span data-stu-id="993c3-185">For more information, see:</span></span>

- <span data-ttu-id="993c3-186">[تجربة إجازة وغياب الموظف في Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) في خطة الموجة 2 لإصدار 2020‬ لتطبيق Dynamics 365‬</span><span class="sxs-lookup"><span data-stu-id="993c3-186">[Employee leave and absence experience in Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 1 plan</span></span>
- [<span data-ttu-id="993c3-187">تطبيق Human Resources في Teams</span><span class="sxs-lookup"><span data-stu-id="993c3-187">Human Resources app in Teams</span></span>](https://go.microsoft.com/fwlink/?linkid=2127841)

### <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="993c3-188">يتوفر كيان DMF لتعليقات الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="993c3-188">DMF entity available for accrual suspensions</span></span>

<span data-ttu-id="993c3-189">يتوفر كيان DMF الآن لتعليقات الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="993c3-189">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="993c3-190">قريبًا</span><span class="sxs-lookup"><span data-stu-id="993c3-190">Coming soon</span></span>

## <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="993c3-191">تضمين كيانات قائمة الاختيار في Dataverse</span><span class="sxs-lookup"><span data-stu-id="993c3-191">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="993c3-192">ستتوفر كيانات قائمة الاختيار لعمليات الإلحاق وإلغاء الإلحاق والتحويلات وعمليات الأعمال قريبًا في Dataverse.</span><span class="sxs-lookup"><span data-stu-id="993c3-192">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

## <a name="known-issues"></a><span data-ttu-id="993c3-193">مشكلات معروفة</span><span class="sxs-lookup"><span data-stu-id="993c3-193">Known issues</span></span>

<span data-ttu-id="993c3-194">قد تعرض مساحة عمل **إدارة الميزات** ميزات معطلة كميزات معاينة عندما تكون متوفرة بشكل عام.</span><span class="sxs-lookup"><span data-stu-id="993c3-194">The **Feature management** workspace may be displaying features that are disabled as preview features when they are generally available.</span></span> <span data-ttu-id="993c3-195">فيما يلي قائمة بالميزات المتوفرة بشكل عام والتي تعرض حالة غير صحيحة.</span><span class="sxs-lookup"><span data-stu-id="993c3-195">Below is a list of generally available features that show an incorrect status.</span></span> 

1.  <span data-ttu-id="993c3-196">إدارة المزايا</span><span class="sxs-lookup"><span data-stu-id="993c3-196">Benefits management</span></span>
2.  <span data-ttu-id="993c3-197">إدارة الحالة</span><span class="sxs-lookup"><span data-stu-id="993c3-197">Case management</span></span>
3.  <span data-ttu-id="993c3-198">تسجيل قاعدة البيانات (تدقيق)</span><span class="sxs-lookup"><span data-stu-id="993c3-198">Database logging (Auditing)</span></span>
4.  <span data-ttu-id="993c3-199">استحقاق الإجازة لشركة واحدة أو خطة واحدة</span><span class="sxs-lookup"><span data-stu-id="993c3-199">Leave accrual for a single company or a single plan</span></span>
5.  <span data-ttu-id="993c3-200">تعليق استحقاق الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="993c3-200">Leave and absence accrual suspension</span></span>
6.  <span data-ttu-id="993c3-201">كود سبب تسوية الرصيد والتعليق</span><span class="sxs-lookup"><span data-stu-id="993c3-201">Balance adjustment reason code and comment</span></span>
7.  <span data-ttu-id="993c3-202">شراء الإجازة وبيعها</span><span class="sxs-lookup"><span data-stu-id="993c3-202">Buy and sell leave</span></span>
8.  <span data-ttu-id="993c3-203">تقويم الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="993c3-203">Leave and absence calendar</span></span>
9.  <span data-ttu-id="993c3-204">قواعد الرصيد المحول للإجازة</span><span class="sxs-lookup"><span data-stu-id="993c3-204">Leave carry-forward rules</span></span>
10. <span data-ttu-id="993c3-205">تدقيق استحقاق الإجازة</span><span class="sxs-lookup"><span data-stu-id="993c3-205">Leave accrual auditing</span></span>
11. <span data-ttu-id="993c3-206">حذف استحقاقات الإجازة</span><span class="sxs-lookup"><span data-stu-id="993c3-206">Leave accrual deletion</span></span>
12. <span data-ttu-id="993c3-207">تقريب استحقاق الإجازة‬</span><span class="sxs-lookup"><span data-stu-id="993c3-207">Leave accrual rounding</span></span>
13. <span data-ttu-id="993c3-208">تكوين أنواع إجازات متعددة في خطة إجازة واحدة</span><span class="sxs-lookup"><span data-stu-id="993c3-208">Configure multiple leave types on a single leave plan</span></span>
14. <span data-ttu-id="993c3-209">تحسينات تحديث تفاصيل الإجازات</span><span class="sxs-lookup"><span data-stu-id="993c3-209">Update time-off enhancements</span></span>
15. <span data-ttu-id="993c3-210">استخدام تكافؤ الدوام الكامل‬ للموظف للاستحقاقات‬</span><span class="sxs-lookup"><span data-stu-id="993c3-210">Use an employee's FTE for accruals</span></span>
16. <span data-ttu-id="993c3-211">طريقة عرض التعويض الثابت عبر الشركة</span><span class="sxs-lookup"><span data-stu-id="993c3-211">Cross company compensation view</span></span>
17. <span data-ttu-id="993c3-212">طباعة مراجعات الأداء</span><span class="sxs-lookup"><span data-stu-id="993c3-212">Print performance reviews</span></span>
18. <span data-ttu-id="993c3-213">تصحيحات العطلات في استحقاق الإجازة</span><span class="sxs-lookup"><span data-stu-id="993c3-213">Leave accrual holiday corrections</span></span>

## <a name="see-also"></a><span data-ttu-id="993c3-214">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="993c3-214">See also</span></span>

[<span data-ttu-id="993c3-215">الجديد أو المتغير في Human Resources</span><span class="sxs-lookup"><span data-stu-id="993c3-215">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="993c3-216">نظره عامة حول الموجة 2 من إصدار Dynamics 365 Human Resources  2019</span><span class="sxs-lookup"><span data-stu-id="993c3-216">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="993c3-217">تحديث العملية</span><span class="sxs-lookup"><span data-stu-id="993c3-217">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="993c3-218">إدارة الميزات</span><span class="sxs-lookup"><span data-stu-id="993c3-218">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]