---
title: تكوين معلمات Human resources
description: يوضح هذا الموضوع كيفية إعداد المحددات الخاصة بالشركة في Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 10f3c62925f6b951f88b990cb8b103dde54c27d1
ms.sourcegitcommit: 45d10d0c25b3ec585323709bb97ba1895b500429
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/05/2021
ms.locfileid: "5502930"
---
# <a name="configure-human-resources-parameters"></a><span data-ttu-id="14e11-103">تكوين معلمات Human resources</span><span class="sxs-lookup"><span data-stu-id="14e11-103">Configure Human resources parameters</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="14e11-104">تتم مشاركة إعدادات بعض معلمات الموارد البشرية بين الشركات، بينما تكون إعدادات المعلمات الأخرى خاصة بكل شركة.</span><span class="sxs-lookup"><span data-stu-id="14e11-104">The settings of some Human resources parameters are shared across companies, while the settings of other parameters are company-specific.</span></span> <span data-ttu-id="14e11-105">يوضح هذا الموضوع كيفية إعداد معلمات الموار البشرية الخاصة بالشركة.</span><span class="sxs-lookup"><span data-stu-id="14e11-105">This topic explains how to set up company-specific Human resources parameters.</span></span>

<span data-ttu-id="14e11-106">يتم استخدام صفحتين لتعيين معلمات الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="14e11-106">Two pages are used to set Human resources parameters.</span></span> <span data-ttu-id="14e11-107">وبالنسبة للمعلمات التي تتم مشاركتها بين الشركات، تستخدم صفحة **المعلمات المشتركة للموارد البشرية**.</span><span class="sxs-lookup"><span data-stu-id="14e11-107">For parameters that are shared across companies, you use the **Human resources shared parameters** page.</span></span> <span data-ttu-id="14e11-108">وبالنسبة للمعلمات الخاصة بالشركة (أي الإعدادات التي يتم تطبيقها على شركة واحدة)، تستخدم **معلمات الموارد البشرية**.</span><span class="sxs-lookup"><span data-stu-id="14e11-108">For parameters that are company-specific (in other words, the settings apply to a single company), you use the **Human resource parameters** page.</span></span>

![انتقل إلى معلمات الموارد البشرية](./media/hr-employee-self-service-human-resources-parameters.png)

<span data-ttu-id="14e11-110">في صفحة **معلمات الموارد البشرية**، يتم تقسيم الإعدادات بين ست علامات تبويب:</span><span class="sxs-lookup"><span data-stu-id="14e11-110">On the **Human resources parameters** page, the settings are divided among six tabs:</span></span>

- <span data-ttu-id="14e11-111">**عام**</span><span class="sxs-lookup"><span data-stu-id="14e11-111">**General**</span></span>
- <span data-ttu-id="14e11-112">**التوظيف** (علامة التبويب هذه غير متضمنة في Dynamics 365 Human Resources)</span><span class="sxs-lookup"><span data-stu-id="14e11-112">**Recruitment** (this tab isn't included in Dynamics 365 Human Resources)</span></span>
- <span data-ttu-id="14e11-113">**التعويض**</span><span class="sxs-lookup"><span data-stu-id="14e11-113">**Compensation**</span></span>
- <span data-ttu-id="14e11-114">**التسلسلات الرقمية**</span><span class="sxs-lookup"><span data-stu-id="14e11-114">**Number sequences**</span></span>
- <span data-ttu-id="14e11-115">**FMLA**</span><span class="sxs-lookup"><span data-stu-id="14e11-115">**FMLA**</span></span>
- <span data-ttu-id="14e11-116">**خدمة الموظف الذاتية**</span><span class="sxs-lookup"><span data-stu-id="14e11-116">**Employee self service**</span></span>
- <span data-ttu-id="14e11-117">**الخدمة الذاتية للمدير**</span><span class="sxs-lookup"><span data-stu-id="14e11-117">**Manager self service**</span></span>
- <span data-ttu-id="14e11-118">**إدارة المزايا**</span><span class="sxs-lookup"><span data-stu-id="14e11-118">**Benefits management**</span></span>
- <span data-ttu-id="14e11-119">**الإجازة والغياب**</span><span class="sxs-lookup"><span data-stu-id="14e11-119">**Leave and absence**</span></span>
- <span data-ttu-id="14e11-120">**طرق الدفع**</span><span class="sxs-lookup"><span data-stu-id="14e11-120">**Payment methods**</span></span>

<span data-ttu-id="14e11-121">تحتوي كل علامة تبويب على المعلومات المتعلقة بشركة واحدة.</span><span class="sxs-lookup"><span data-stu-id="14e11-121">Each tab contains information that pertains to a single company.</span></span>

## <a name="general"></a><span data-ttu-id="14e11-122">عام</span><span class="sxs-lookup"><span data-stu-id="14e11-122">General</span></span>

<span data-ttu-id="14e11-123">وتحدد الإعدادات الموجودة في علامة التبويب **عام** مظهر المعلومات المتعلقة بالغياب، والإصابة والمرض، والتعيينات الجديدة.</span><span class="sxs-lookup"><span data-stu-id="14e11-123">The settings on the **General** tab define the appearance of information about absence, injury and illness, and new hires.</span></span> <span data-ttu-id="14e11-124">كما تحدد الإعدادات الموجودة في علامة التبويب هذه بعض الإدخالات الافتراضية التي تظهر أثناء العمل.</span><span class="sxs-lookup"><span data-stu-id="14e11-124">The settings on this tab also define some default entries that appear as you work.</span></span> <span data-ttu-id="14e11-125">وبشكل خاص، تتيح لك علامة التبويب هذه:</span><span class="sxs-lookup"><span data-stu-id="14e11-125">Specifically, this tab lets you:</span></span>

- <span data-ttu-id="14e11-126">تحديد لون لتطبيقه على فتح معاملات الغياب</span><span class="sxs-lookup"><span data-stu-id="14e11-126">Select a color to apply to open absence transactions</span></span>
- <span data-ttu-id="14e11-127">تحديد ورقه الأنماط المراد استخدامها للتقارير</span><span class="sxs-lookup"><span data-stu-id="14e11-127">Specify the style sheet to use for reports</span></span>
- <span data-ttu-id="14e11-128">تمكين التكامل بين الدورات التدريبية وتسجيل الغياب</span><span class="sxs-lookup"><span data-stu-id="14e11-128">Enable the integration between training courses and absence registration</span></span>
- <span data-ttu-id="14e11-129">حدد كود الغياب المستخدم للتحكم في هذا التكامل.</span><span class="sxs-lookup"><span data-stu-id="14e11-129">Select the absence code that is used to control this integration.</span></span>
- <span data-ttu-id="14e11-130">قم بالإشارة إلى المدة المطلوبة للاحتفاظ بالحوادث الخاصة بالإصابة والمرض.</span><span class="sxs-lookup"><span data-stu-id="14e11-130">Indicate how long to keep injury and illness case incidents.</span></span>
- <span data-ttu-id="14e11-131">حدد رقم التعريف الافتراضي الذي يظهر عند توظيف عامل جديد.</span><span class="sxs-lookup"><span data-stu-id="14e11-131">Specify the default identification number shown when a new worker is hired.</span></span>

![علامة التبويب عام](./media/hr-setup-parameters-general.png)

## <a name="recruitment"></a><span data-ttu-id="14e11-133">التوظيف</span><span class="sxs-lookup"><span data-stu-id="14e11-133">Recruitment</span></span>

<span data-ttu-id="14e11-134">تحدد الإعدادات الموجودة ضمن علامة التبويب **التوظيف** أنواع المستندات المستخدمة في المراسلات المرسلة تلقائيًا إلى مقدمي الطلبات.</span><span class="sxs-lookup"><span data-stu-id="14e11-134">The settings on the **Recruitment** tab define the document types used for correspondence automatically sent to applicants.</span></span> <span data-ttu-id="14e11-135">يمكنك أيضًا الإشارة إلى مشروع التعيين المستخدم للتطبيقات غير المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="14e11-135">You can also indicate the recruitment project used for unsolicited applications.</span></span>

<span data-ttu-id="14e11-136">تعمل الفترة التي يتم تحديدها لتقادم مشروع التعيين على تحديد مشاريع التعيين التي تم تضمينها في اللوحة **مشاريع التقادم** في مساحة عمل **إدارة التعيين**.</span><span class="sxs-lookup"><span data-stu-id="14e11-136">The period defined for recruitment project aging determines the recruitment projects included on the **Aging projects** tile in the **Recruitment management** workspace.</span></span> <span data-ttu-id="14e11-137">ويتم استخدام الفترة لتحذير الموعد النهائي لتقديم الطلب لعرض مشاريع التوظيف التي تقترب من الموعد النهائي لتقديم الطلبات في تجانب **اقترب الموعد النهائي لاستمارة التقديم‬** في مساحة عمل **التوظيف**.</span><span class="sxs-lookup"><span data-stu-id="14e11-137">The period defined for the application deadline warning is used to display recruitment projects that are approaching their application deadline on the **Application deadline approaching** tile in the **Recruitment** workspace.</span></span>

<span data-ttu-id="14e11-138">لمزيد من المعلومات حول التعيين، راجع [تعيين المرشحين للوظائف](hr-personnel-recruit.md).</span><span class="sxs-lookup"><span data-stu-id="14e11-138">For more information about recruiting, see [Recruit job candidates](hr-personnel-recruit.md).</span></span>

## <a name="compensation"></a><span data-ttu-id="14e11-139">التعويض</span><span class="sxs-lookup"><span data-stu-id="14e11-139">Compensation</span></span>

<span data-ttu-id="14e11-140">في Dynamics 365 Finance، تحدد الإعدادات الموجودة في علامة التبويب **التعويض** ما إذا كان يجب على المستخدمين التأكد من أنهم يريدون حفظ المعلومات لخطة تعويض ثابتة أو متغيرة.</span><span class="sxs-lookup"><span data-stu-id="14e11-140">In Dynamics 365 Finance, the settings on the **Compensation** tab define whether users must confirm that they want to save information for a fixed or variable compensation plan.</span></span> <span data-ttu-id="14e11-141">وإذا قمت بتحديد **تمكين التحقق من صحة الحفظ**، عندما يقوم خلاله المستخدمون بإغلاق الصفحة المتعلقة بالتعويض، يتلقون رسالة تسأل عما إذا كانوا يرغبون في حفظ السجل.</span><span class="sxs-lookup"><span data-stu-id="14e11-141">If you select **Enable save validation**, when users close a compensation-related page, they receive a message that asks whether they want to save the record.</span></span> <span data-ttu-id="14e11-142">ولا تسمح بعض الصفحات في إدارة التعويض للمستخدمين بحذف المعلومات.‬</span><span class="sxs-lookup"><span data-stu-id="14e11-142">Some pages in Compensation management don't let users delete information.</span></span> <span data-ttu-id="14e11-143">من خلال مطالبة المستخدمين بالتحقق من أنهم يريدون حفظ المعلومات، فقد تكون قادرًا على تحديد مقدار المعلومات الذي يتم حفظه ولكن لا يمكن حذف لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="14e11-143">By prompting users to verify that they want to save information, you might be able to limit the amount of information that is saved but can't be deleted later.</span></span> <span data-ttu-id="14e11-144">وإذا قمت بإلغاء تحديد **تمكين التحقق من صحة الحفظ**، يتم حفظ السجلات مباشرةً، ربما قبل أن يصبح المستخدم جاهزًا.</span><span class="sxs-lookup"><span data-stu-id="14e11-144">If you clear **Enable save validation**, records save immediately, possibly before the user is ready.</span></span> <span data-ttu-id="14e11-145">وإذا كنت تستخدم إدارة الأداء، تتيح لك علامة التبويب **التعويض** إمكانية تحديد نموذج تقدير لاستخدامه بدلاً من النموذج الذي تم تعيينه لخطط التعويض عندما يتم تقدير الأداء.</span><span class="sxs-lookup"><span data-stu-id="14e11-145">If you're using Performance management, the **Compensation** tab also lets you select a rating model to use instead of the model assigned to compensation plans when rating performance.</span></span>

<span data-ttu-id="14e11-146">في Human Resources، يمكنك استخدام علامة التبويب **التعويض** لاختيار تقييد الوصول إلى خطط التعويض وتعيين العملة الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="14e11-146">In Human Resources, you can use the **Compensation** tab to choose to restrict access to compensation plans and to set a default currency.</span></span>

<span data-ttu-id="14e11-147">لمزيد من المعلومات حول التعويض، راجع [نظرة عامة حول خطط التعويض](hr-compensation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="14e11-147">For more information about compensation, see [Compensation plans overview](hr-compensation-overview.md).</span></span>

![علامة التبويب التعويض](./media/hr-setup-parameters-compensation.png)

## <a name="number-sequences"></a><span data-ttu-id="14e11-149">التسلسلات الرقمية</span><span class="sxs-lookup"><span data-stu-id="14e11-149">Number sequences</span></span>

<span data-ttu-id="14e11-150">تحدد الإعدادات الموجودة ضمن علامة التبويب **التسلسل الرقمي** التسلسلات المستخدمة لتعيين المعرفات تلقائيًا للأصناف في Human Resources، مثل:</span><span class="sxs-lookup"><span data-stu-id="14e11-150">The settings on the **Number sequence** tab determine the sequences used to automatically assign IDs to items in Human Resources, such as:</span></span>

- <span data-ttu-id="14e11-151">التطبيقات</span><span class="sxs-lookup"><span data-stu-id="14e11-151">Applications</span></span>
- <span data-ttu-id="14e11-152">تسجيلات الغياب</span><span class="sxs-lookup"><span data-stu-id="14e11-152">Absence registrations</span></span>
- <span data-ttu-id="14e11-153">نتائج عملية التعويض</span><span class="sxs-lookup"><span data-stu-id="14e11-153">Compensation process results</span></span>
- <span data-ttu-id="14e11-154">أرقام الحالات</span><span class="sxs-lookup"><span data-stu-id="14e11-154">Case numbers</span></span>
- <span data-ttu-id="14e11-155">الدورات التدريبية</span><span class="sxs-lookup"><span data-stu-id="14e11-155">Courses</span></span>
- <span data-ttu-id="14e11-156">جداول أعمال الدورة التدريبية</span><span class="sxs-lookup"><span data-stu-id="14e11-156">Course agendas</span></span>

<span data-ttu-id="14e11-157">للاحتفاظ بمراجع التسلسلات الرقمية والرموز، استخدم صفحة قائمة **التسلسلات الرقمية** (حدد **إدارة المؤسسة > التسلسلات الرقمية > التسلسلات الرقمية**).</span><span class="sxs-lookup"><span data-stu-id="14e11-157">To maintain number sequence references and codes, use the **Number sequences** list page (select **Organization administration > Number sequences > Number sequences**).</span></span>

<span data-ttu-id="14e11-158">لمزيد من المعلومات، راجع [مراجعة عامة حول التسلسلات الرقمية](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview?toc=/dynamics365/human-resources/toc.json).</span><span class="sxs-lookup"><span data-stu-id="14e11-158">For more information, see [Number sequences overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview?toc=/dynamics365/human-resources/toc.json).</span></span>

> [!NOTE]
> <span data-ttu-id="14e11-159">لا يمكن أن يتجاوز عدد الساعات التي يتم العمل خلالها 1,250، ولا يمكن أن تتجاوز مدة العمل 12 شهرًا.</span><span class="sxs-lookup"><span data-stu-id="14e11-159">The number of hours that are worked can't exceed 1,250, and the length of employment can't exceed 12 months.</span></span> <span data-ttu-id="14e11-160">وتكون هذه القيم القصوى وفقًا للقانون الفيدرالي في الولايات المتحدة.</span><span class="sxs-lookup"><span data-stu-id="14e11-160">These maximum values are in accordance with federal law in the United States.</span></span>

![علامة التبويب التسلسلات الرقمية](./media/hr-setup-parameters-number-sequences.png)

## <a name="fmla"></a><span data-ttu-id="14e11-162">FMLA</span><span class="sxs-lookup"><span data-stu-id="14e11-162">FMLA</span></span>

<span data-ttu-id="14e11-163">من علامة التبويب FMLA، يمكنك تعيين متطلبات أهلية FMLA وساعات استحقاق FMLA.</span><span class="sxs-lookup"><span data-stu-id="14e11-163">On the FMLA tab, you set FMLA eligibility requirements and FMLA entitlement hours.</span></span> <span data-ttu-id="14e11-164">لمزيد من المعلومات، راجع [تكوين معلمات الإجازة والغياب](hr-leave-and-absence-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="14e11-164">For more information, see [Configure leave and absence parameters](hr-leave-and-absence-parameters.md).</span></span>

![علامة تبويب FMLA](./media/hr-setup-parameters-fmla.png)

## <a name="employee-self-service"></a><span data-ttu-id="14e11-166">خدمة الموظف الذاتية</span><span class="sxs-lookup"><span data-stu-id="14e11-166">Employee self service</span></span>

<span data-ttu-id="14e11-167">وتؤثر الإعدادات الموجودة في علامة التبويب **الخدمة الذاتية للموظف** على كيفية ظهور خدمة الموظف الذاتية للموظفين.</span><span class="sxs-lookup"><span data-stu-id="14e11-167">The settings on the **Employee self service** tab affect how Employee self service appears to employees.</span></span> <span data-ttu-id="14e11-168">في علامة التبويب هذه، يمكنك:</span><span class="sxs-lookup"><span data-stu-id="14e11-168">On this tab, you can:</span></span>

- <span data-ttu-id="14e11-169">أدخل اسمًا لمساحة عمل الخدمة الذاتية للموظف</span><span class="sxs-lookup"><span data-stu-id="14e11-169">Enter a name for the Employee self service workspace</span></span>
- <span data-ttu-id="14e11-170">تحديد المعلومات التي يمكن للمدير إدخالها للموظفين</span><span class="sxs-lookup"><span data-stu-id="14e11-170">Select which information a manager can enter for employees</span></span>
- <span data-ttu-id="14e11-171">إضافة ارتباطات مفيدة للموظفين</span><span class="sxs-lookup"><span data-stu-id="14e11-171">Add useful links for employees</span></span>
- <span data-ttu-id="14e11-172">قم بتقييد الموظفين من إضافة أو تحرير تفاصيل جهة اتصال العمل.</span><span class="sxs-lookup"><span data-stu-id="14e11-172">Restrict employees from adding or editing business contact details.</span></span> <span data-ttu-id="14e11-173">لمزيد من المعلومات، راجع [تقييد تحرير المعلومات الشخصية](hr-employee-self-service-restrict-editing.md).</span><span class="sxs-lookup"><span data-stu-id="14e11-173">For more information, see [Restrict editing of personal information](hr-employee-self-service-restrict-editing.md).</span></span>

<span data-ttu-id="14e11-174">لمزيد من المعلومات حول إعداد الخدمة الذاتية للموظف، راجع [نظرة عامة حول الخدمة الذاتية للموظف والمدير](hr-employee-manager-self-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="14e11-174">For more information about setting up Employee self service, see [Employee and Manager self service overview](hr-employee-manager-self-service-overview.md).</span></span>

![علامة التبويب خدمة الموظف الذاتية](./media/hr-setup-parameters-employee-self-service.png)

## <a name="manager-self-service"></a><span data-ttu-id="14e11-176">الخدمة الذاتية للمدير</span><span class="sxs-lookup"><span data-stu-id="14e11-176">Manager self service</span></span>

<span data-ttu-id="14e11-177">إن الإعدادات الموجودة في علامة التبويب **الخدمة الذاتية للمدير** تؤثر على ما يراه المديرين في خدمة الإدارة الذاتية.</span><span class="sxs-lookup"><span data-stu-id="14e11-177">The settings on the **Manager self service** tab affect what managers see in Manager self service.</span></span> <span data-ttu-id="14e11-178">في علامة التبويب هذه، يمكنك تكوين الخيارات التالية:</span><span class="sxs-lookup"><span data-stu-id="14e11-178">On this tab, you can configure the following options:</span></span>

- <span data-ttu-id="14e11-179">نطاق السجلات منتهية الصلاحية</span><span class="sxs-lookup"><span data-stu-id="14e11-179">The range for expiring records</span></span>
- <span data-ttu-id="14e11-180">يمكن لمديري المعلومات عرض السجلات التي انتهت صلاحيتها</span><span class="sxs-lookup"><span data-stu-id="14e11-180">Information managers can view in expiring records</span></span>
- <span data-ttu-id="14e11-181">ما إذا كان بإمكان المديرين عرض المواضع المفتوحة للتقارير الموسعة</span><span class="sxs-lookup"><span data-stu-id="14e11-181">Whether managers can view open positions for extended reports</span></span>
- <span data-ttu-id="14e11-182">طرق عرض العمال المغادرون</span><span class="sxs-lookup"><span data-stu-id="14e11-182">Views of exiting workers</span></span>
- <span data-ttu-id="14e11-183">ارتباطات مفيدة للمديرين</span><span class="sxs-lookup"><span data-stu-id="14e11-183">Useful links for managers</span></span>

<span data-ttu-id="14e11-184">لمزيد من المعلومات حول إعداد الخدمة الذاتية للمدير، راجع [نظرة عامة حول الخدمة الذاتية للموظف والمدير](hr-employee-manager-self-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="14e11-184">For more information about setting up Manager self service, see [Employee and Manager self service overview](hr-employee-manager-self-service-overview.md).</span></span>

![علامة التبويب الخدمة الذاتية للمدير](./media/hr-setup-parameters-manager-self-service.png)

## <a name="benefits-management"></a><span data-ttu-id="14e11-186">إدارة المزايا</span><span class="sxs-lookup"><span data-stu-id="14e11-186">Benefits management</span></span>

<span data-ttu-id="14e11-187">في علامة التبويب إدارة المزايا، يمكنك تكوين خيارات البريد الإلكتروني لإدارة المزايا.</span><span class="sxs-lookup"><span data-stu-id="14e11-187">On the Benefits management tab, you can configure email options for Benefits management.</span></span> <span data-ttu-id="14e11-188">لمزيد من المعلومات حول إعداد إدارة المزايا واستخدامها، راجع [نظرة عامة حول إدارة المزايا](hr-benefits-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="14e11-188">For information about setting up and using Benefits management, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>

![علامة التبويب إدارة المزايا](./media/hr-setup-parameters-benefits-management.png)

## <a name="leave-and-absence"></a><span data-ttu-id="14e11-190">الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="14e11-190">Leave and absence</span></span>

<span data-ttu-id="14e11-191">للحصول على معلومات حول إعداد واستخدام الغياب والإجازات، راجع [نظرة عامة حول الغياب والإجازات](hr-leave-and-absence-overview.md).</span><span class="sxs-lookup"><span data-stu-id="14e11-191">For information about setting up and using Leave and absence, see [Leave and absence overview](hr-leave-and-absence-overview.md).</span></span>

## <a name="payment-methods"></a><span data-ttu-id="14e11-192">طرق الدفع</span><span class="sxs-lookup"><span data-stu-id="14e11-192">Payment methods</span></span>

<span data-ttu-id="14e11-193">في علامة التبويب **طرق الدفع**، يمكنك تحديد طرق الدفع التي تدعمها مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="14e11-193">On the **Payment methods** tab, you can select the payment methods supported by your organization.</span></span> <span data-ttu-id="14e11-194">لمزيد من المعلومات حول تكوين التعويض، راجع [نظرة عامة حول خطط التعويض](hr-compensation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="14e11-194">For more information about configuring compensation, see [Compensation plans overview](hr-compensation-overview.md).</span></span>

![علامة التبويب طرق الدفع](./media/hr-setup-parameters-payment-methods.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]