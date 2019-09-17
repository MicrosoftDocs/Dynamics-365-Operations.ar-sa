---
title: الأسئلة المتداول حول تكامل Dynamics 365 for Talent إلى Dynamics 365 for Finance and Operations
description: يوضح هذا الموضوع البيانات التي تتم مزامنتها في تكامل Talent وFinance and Operations.
author: andreabichsel
manager: AnnBe
ms.date: 01/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: cb9e01316f4b154a3e9a73042eaf0492f016c46c
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742685"
---
# <a name="dynamics-365-for-talent-to-dynamics-365-for-finance-and-operations-integration-faq"></a><span data-ttu-id="6a533-103">الأسئلة المتداول حول تكامل Dynamics 365 for Talent إلى Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6a533-103">Dynamics 365 for Talent to Dynamics 365 for Finance and Operations integration FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6a533-104">يجيب هذا الموضوع عن الأسئلة الشائعة حول البيانات التي تتم مزامنتها عندما يتكامل Dynamics 365 for Talent مع Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6a533-104">This topic answers common questions associated about what data is synchronized when Dynamics 365 for Talent is integrated with Dynamics 365 for Finance and Operations.</span></span>

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a><span data-ttu-id="6a533-105">هل تتم مزامنة جميع البيانات أو بعض كيانات البيانات فقط؟</span><span class="sxs-lookup"><span data-stu-id="6a533-105">Is all data synchronized or just some data entities?</span></span>

<span data-ttu-id="6a533-106">مع Core Human Resources (HR)، تتم مزامنة مجموعة فرعية من البيانات.</span><span class="sxs-lookup"><span data-stu-id="6a533-106">With Core Human Resources (HR), a subset of the data is synchronized.</span></span> <span data-ttu-id="6a533-107">للحصول على قائمة بجميع الكيانات، راجع [التكامل من Dynamics 365 for Talent إلى Dynamics 365 for Finance and Operations](talent-financeandoperations-integration.md).</span><span class="sxs-lookup"><span data-stu-id="6a533-107">For a list of all the entities, see [Integration from Dynamics 365 for Talent to Dynamics 365 for Finance and Operations](talent-financeandoperations-integration.md).</span></span>

<span data-ttu-id="6a533-108">بالنسبة إلى Attract وOnboard، تعتبر كافة البيانات أصلية في Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="6a533-108">For Attract and Onboard, all data is native to Common Data Service.</span></span>

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a><span data-ttu-id="6a533-109">هل يمكنني إنشاء تعيين جديد من دون استخدام القوالب؟</span><span class="sxs-lookup"><span data-stu-id="6a533-109">Can I create a new mapping without using the templates?</span></span>

<span data-ttu-id="6a533-110">تعتبر القوالب نقطة بداية.</span><span class="sxs-lookup"><span data-stu-id="6a533-110">Templates are the starting point.</span></span> <span data-ttu-id="6a533-111">يمكنك إنشاء قالبك الخاص، ولكنك تحتاج دائمًا إلى قالب عند إنشاء مشروع تكامل.</span><span class="sxs-lookup"><span data-stu-id="6a533-111">You can create your own template, but a template is always needed when creating an integration project.</span></span> <span data-ttu-id="6a533-112">للحصول على مزيد من المعلومات حول موحد البيانات (DI) والقوالب والمشاريع، راجع [دمج البيانات في Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="6a533-112">For more information about data integrator (DI), templates, and projects, see [Integrate data into Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

## <a name="can-i-map-financial-dimensions-to-transfer-between-talent-and-finance-and-operations"></a><span data-ttu-id="6a533-113">هل يمكنني تعيين الأبعاد المالية للتحويل بين Talent وFinance and Operations؟</span><span class="sxs-lookup"><span data-stu-id="6a533-113">Can I map financial dimensions to transfer between Talent and Finance and Operations?</span></span>

<span data-ttu-id="6a533-114">الأبعاد المالية غير موجودة حاليًا في Common Data Service ونتيجة لذلك لا تشكل جزءًا من القالب الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="6a533-114">Financial dimensions aren’t currently in Common Data Service and as a result aren’t part of the default template.</span></span> <span data-ttu-id="6a533-115">تم التخطيط لهذا الكيان، ولكن لا يتوفر حاليًا أي مخطط زمني للإصدار.</span><span class="sxs-lookup"><span data-stu-id="6a533-115">This entity is planned, but currently no release timeline is available.</span></span>

<span data-ttu-id="6a533-116">بالنسبة إلى البيانات الموجودة في Finance and Operations ولكن غير الموجودة في Talent، يمكن ربط النظامين معًا باستخدام **تكوين الارتباطات** في Talent.</span><span class="sxs-lookup"><span data-stu-id="6a533-116">For data that resides in Finance and Operations but does not exist in Talent, link the two systems together by using **Configure Links** in Talent.</span></span> <span data-ttu-id="6a533-117">للحصول على مزيد من المعلومات حول كيفية تكوين الارتباطات بين Talent وFinance and Operations، راجع [ما الجديد أو المتغير في Dynamics 365 for Talent Core HR (31 أكتوبر 2018)](whats-new-talent-october-31.md).</span><span class="sxs-lookup"><span data-stu-id="6a533-117">For more information about how to configure links between Talent and Finance and Operations, see [What's new or changed in Dynamics 365 for Talent Core HR (October 31, 2018)](whats-new-talent-october-31.md).</span></span>

![تعيين الأبعاد المالية](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-and-operations-why"></a><span data-ttu-id="6a533-119">عندما أستورد موظفين، ينتقل هؤلاء في بعض الأحيان إلى عاملين غير نشطين في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6a533-119">Sometimes when I import employees, they go into inactive workers in Finance and Operations.</span></span> <span data-ttu-id="6a533-120">ما السبب؟</span><span class="sxs-lookup"><span data-stu-id="6a533-120">Why?</span></span>

<span data-ttu-id="6a533-121">قد تتلقى رسالة الخطأ هذه إذا لم يكن لدى الموظفين أي سجل يتضمن تفاصيل التوظيف النشط في Talent.</span><span class="sxs-lookup"><span data-stu-id="6a533-121">You may get this error if employees don’t have an active employment detail record in Talent.</span></span> <span data-ttu-id="6a533-122">لحل هذه المشكلة، انتقل إلى **إدارة الموظفين \> الموظفون \> سجل التوظيف‬ \> مدير التاريخ**، وتأكد من وجود سجل يتضمن تفاصيل التوظيف النشط.</span><span class="sxs-lookup"><span data-stu-id="6a533-122">To resolve this, go to **Personnel Management \> Employees \> Employment History \> Date Manager**, and verify that there is an active employment detail record.</span></span>

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a><span data-ttu-id="6a533-123">إذا اخترت تعيين مجموعة فرعية فقط من الحقول، فهل ستؤدي التغييرات التي تم إدخالها على حقول غير معينة إلى تشغيل عملية مزامنة؟</span><span class="sxs-lookup"><span data-stu-id="6a533-123">If I select to map only a subset of fields, will changes made to non-mapped fields trigger a sync?</span></span>

<span data-ttu-id="6a533-124">تتبع مزامنة البيانات جدول التنفيذ.</span><span class="sxs-lookup"><span data-stu-id="6a533-124">Data sync follows the execution schedule.</span></span> <span data-ttu-id="6a533-125">ستختار عملية التكامل سجلاً إذا تم تغيير أي حقل في السجل بصرف النظر عما إذا كان الحقل جزءًا من تعيين التكامل.</span><span class="sxs-lookup"><span data-stu-id="6a533-125">The integration will pick up a record if any field in the record changes regardless if the field is part of integration mapping.</span></span>

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a><span data-ttu-id="6a533-126">كيف يمكنني إرسال تغييرات العاملين النشطاء فقط وليس سجلات العاملين المنتهية خدماتهم؟</span><span class="sxs-lookup"><span data-stu-id="6a533-126">How can I send only active worker changes and not the terminated records?</span></span>

<span data-ttu-id="6a533-127">باستخدام "الاستعلام المتقدم"، يمكنك تصفية البيانات المصدر وإعادة تشكيلها قبل تمريرها إلى الوجهة.</span><span class="sxs-lookup"><span data-stu-id="6a533-127">With the use of "Advanced query", you can filter and reshape source data before passing it into the destination.</span></span>

![الاستعلام المتقدم للعاملين النشطين](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-and-operations-for-a-specific-entity"></a><span data-ttu-id="6a533-129">هل يمكنني تحديد الحقول التي سيتم إرسالها إلى Finance and Operations لكيان معين؟</span><span class="sxs-lookup"><span data-stu-id="6a533-129">Can I specify which fields to send to Finance and Operations for a specific entity?</span></span>

<span data-ttu-id="6a533-130">يمكنك إضافة حقول أو إزالتها من مهمة التكامل.</span><span class="sxs-lookup"><span data-stu-id="6a533-130">Fields can be added or removed from the integration task.</span></span> <span data-ttu-id="6a533-131">لن يتم ملء كافة حقول البيانات الموجودة على كيان Common Data Service من Core HR.</span><span class="sxs-lookup"><span data-stu-id="6a533-131">Not all data fields that exist on the Common Data Service entity will be populated from Core HR.</span></span>
<span data-ttu-id="6a533-132">يمكنك ملء بيانات إضافية عبر PowerApps.</span><span class="sxs-lookup"><span data-stu-id="6a533-132">Additional data can be populated via PowerApps.</span></span>

![إضافة حقول إلى أو إزالتها من مهمة تكامل](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-talent-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a><span data-ttu-id="6a533-134">بعد إعداد التكامل كوظيفة دفعية، فقد Talent الاتصال بالنظام الوجهة.</span><span class="sxs-lookup"><span data-stu-id="6a533-134">I set up integration as a batch job, but Talent lost connection to the destination system.</span></span> <span data-ttu-id="6a533-135">كيف يمكنني إرسال مجموعة التغييرات نفسها إلى النظام الوجهة؟</span><span class="sxs-lookup"><span data-stu-id="6a533-135">How can I send the same set of changes to the destination system?</span></span>

<span data-ttu-id="6a533-136">لا حاجة إلى أي إعداد خاص لمعالجة الاستثناء.</span><span class="sxs-lookup"><span data-stu-id="6a533-136">No special setup is required for exception handling.</span></span> <span data-ttu-id="6a533-137">سيقوم موحد البيانات بشكل تلقائي بالتقاط الأخطاء التي تحدث في المصدر والوجهة وسيبلغ عنها وسيسمح بإعادة المحاولة يدويًا.</span><span class="sxs-lookup"><span data-stu-id="6a533-137">The Data Integrator will automatically catch and report errors which occur at the source and destination and will allow manual retries.</span></span> <span data-ttu-id="6a533-138">ومع ذلك، فهو لا يسمح بتصحيح البيانات يدويًا.</span><span class="sxs-lookup"><span data-stu-id="6a533-138">However, it doesn’t allow manual data correction.</span></span> <span data-ttu-id="6a533-139">إن كان هناك حاجة إلى إجراء عمليات تحديث للبيانات، فيجب أن تحدث في المصدر أو الوجهة.</span><span class="sxs-lookup"><span data-stu-id="6a533-139">If data updates are needed, that should happen either at the source or the destination.</span></span>

## <a name="can-i-set-up-bi-directional-integration"></a><span data-ttu-id="6a533-140">هل يمكنني إعداد تكامل ثنائي الاتجاه؟</span><span class="sxs-lookup"><span data-stu-id="6a533-140">Can I set up bi-directional integration?</span></span>

<span data-ttu-id="6a533-141">لا، التكامل أحادي الاتجاه في الوقت الحالي (Talent إلى Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="6a533-141">No, integration is currently one-way (Talent to Finance and Operations).</span></span> <span data-ttu-id="6a533-142">ومع ذلك، يوجد قالب افتراضي لإرسال البيانات من Talent إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6a533-142">However, there is a default template available to send data from Talent to Finance and Operations.</span></span>

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a><span data-ttu-id="6a533-143">هل يمكنني السماح بحذف السجلات كجزء من عملية التكامل؟</span><span class="sxs-lookup"><span data-stu-id="6a533-143">Can I allow record deletion as part of my integration?</span></span>

<span data-ttu-id="6a533-144">لا، لن يلتقط موحد البيانات السجلات المحذوفة لنقل البيانات.</span><span class="sxs-lookup"><span data-stu-id="6a533-144">No, Data Integrator will not capture deleted records for data transfer.</span></span> <span data-ttu-id="6a533-145">في الوقت الحالي، لم يتم تضمين سواء عمليات إنشاء وتحديث البيانات (UPSERT).</span><span class="sxs-lookup"><span data-stu-id="6a533-145">Only data creation and updates (UPSERT) are currently included.</span></span>

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a><span data-ttu-id="6a533-146">هل يمكن إعادة تشغيل التنفيذ الذي يتضمن أخطاء؟</span><span class="sxs-lookup"><span data-stu-id="6a533-146">Can I rerun the errored execution?</span></span> <span data-ttu-id="6a533-147">إذا كان الأمر كذلك، فهل سيرسل ملفًا كاملاً أو التغييرات فقط؟</span><span class="sxs-lookup"><span data-stu-id="6a533-147">If so, will it send a full file or only the changes?</span></span>

<span data-ttu-id="6a533-148">عملية التشغيل الأولى لموحد البيانات هي دائمًا عملية تشغيل كاملة.</span><span class="sxs-lookup"><span data-stu-id="6a533-148">The first run of Data Integrator is always a full run.</span></span> <span data-ttu-id="6a533-149">وتستند عمليات التشغيل التالية إلى تعقب التغييرات.</span><span class="sxs-lookup"><span data-stu-id="6a533-149">Subsequent runs are based on change tracking.</span></span> <span data-ttu-id="6a533-150">يستخرج تشغيل الخطأ، عند تنفيذه، السجلات الموجودة في نطاق التشغيل ويرسل أحدث التغييرات من Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="6a533-150">When an error run is executed, it extracts the records in scope of the run and sends out the most recent changes from Common Data Service.</span></span>

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a><span data-ttu-id="6a533-151">عند حفظ المشروع، أتلقى رسالة الخطأ: "يتضمن المشروع أخطاء تعيين".</span><span class="sxs-lookup"><span data-stu-id="6a533-151">When I save the project, I get the error: “Project has mapping errors."</span></span> <span data-ttu-id="6a533-152">ماذا أفعل؟</span><span class="sxs-lookup"><span data-stu-id="6a533-152">What do I do?</span></span>

<span data-ttu-id="6a533-153">تحقق من إعداد مفاتيح التكامل، وأدخل أية تغييرات مطلوبة على الإعداد، ثم قم بتحديث الكيانات في المشروع.</span><span class="sxs-lookup"><span data-stu-id="6a533-153">Check the setup of your integration keys, make any required changes to the setup, then refresh the entities in the project.</span></span>

<span data-ttu-id="6a533-154">عند استخدام القالب الافتراضي، سيتم استيراد مفاتيح التكامل بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="6a533-154">When the default template is used, the integration keys will be automatically imported.</span></span> <span data-ttu-id="6a533-155">قد تحدث هذه المشكلة عند إضافة مهام جديدة إلى القالب الموجود.</span><span class="sxs-lookup"><span data-stu-id="6a533-155">This issue may occur when new tasks are added to the existing template.</span></span>

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a><span data-ttu-id="6a533-156">إذا كان لديّ العدد N من الكيانات القانونية حتى توجد توظيفات للعاملين، هل أحتاج إلى إنشاء تعيين لكل واحد منهم؟</span><span class="sxs-lookup"><span data-stu-id="6a533-156">If I have N number of legal entities where workers have employments, do I need to create a mapping for each of them?</span></span>

<span data-ttu-id="6a533-157">نعم، لكل كيان قانوني في Finance and Operations، ستحتاج إلى مشروع تكامل منفصل في تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="6a533-157">Yes, for each legal entity in Finance and Operations, you'll need a separate integration project in the data integration.</span></span>

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a><span data-ttu-id="6a533-158">أحتاج إلى نقل البيانات التي لا تشكل جزءًا من القالب الافتراضي التي وفرته Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6a533-158">I need to transfer data that is not part of the default template provided by Microsoft.</span></span> <span data-ttu-id="6a533-159">هل يمكنني القيام بذلك؟</span><span class="sxs-lookup"><span data-stu-id="6a533-159">Can I do this?</span></span>

<span data-ttu-id="6a533-160">نعم، يمكن إضافة حقول أو إزالتها من القالب الموجود.</span><span class="sxs-lookup"><span data-stu-id="6a533-160">Yes, fields can be added to or removed from the existing template.</span></span> <span data-ttu-id="6a533-161">ويمكن تعديل القالب لتضمين بيانات إضافية من كيانات أخرى في Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="6a533-161">The template can be modified to include additional data from other Common Data Service entities.</span></span> <span data-ttu-id="6a533-162">يجب أن يكون الكيان في Common Data Service لكي يتم تضمينه في القالب.</span><span class="sxs-lookup"><span data-stu-id="6a533-162">The entity must be in Common Data Service for it to be included in the template.</span></span> 

## <a name="i-just-created-new-finance-and-operations-and-talent-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a><span data-ttu-id="6a533-163">لقد انتهيت الآن من إنشاء بيئات Finance and Operations وTalent، وتلقيت رسالة الخطأ "قيمة البيانات انتهاك قيود التكامل."</span><span class="sxs-lookup"><span data-stu-id="6a533-163">I just created new Finance and Operations and Talent environments, and I'm getting the error "The data value violates integrity constraints."</span></span> <span data-ttu-id="6a533-164">ما السبب؟</span><span class="sxs-lookup"><span data-stu-id="6a533-164">Why?</span></span>

<span data-ttu-id="6a533-165">بإمكان أسباب هذا الخطأ أن تشتمل على:</span><span class="sxs-lookup"><span data-stu-id="6a533-165">Reasons for this error can include:</span></span>

- <span data-ttu-id="6a533-166">أدى نقل البيانات إلى استخراج سجلات مكررة في المصدر (Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="6a533-166">The data transfer resulted in duplicate records extraction at the source (Common Data Service).</span></span>

- <span data-ttu-id="6a533-167">تتضمن عملية نقل البيانات قيمًا فارغة للحقول المطلوبة في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6a533-167">The data transfer has null values for fields that are required in Finance and Operations.</span></span> <span data-ttu-id="6a533-168">تأكد من أن البيانات موجودة في Common Data Service وتستوفي شروط Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6a533-168">Verify the data that is in Common Data Service and meets the requirements of Finance and Operations.</span></span>

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a><span data-ttu-id="6a533-169">إذا ظهرت أخطاء تتعلق بالتنفيذ ولم تتم مزامنة معرّف الموظف، كيف يمكنني العثور على محفوظات الوظيفة التي تتضمن سجل الموظف الفاشل؟</span><span class="sxs-lookup"><span data-stu-id="6a533-169">If there are execution errors and the Employee ID didn't sync, how do I find the history job which has the failed employee record?</span></span>

<span data-ttu-id="6a533-170">سينشئ موحد البيانات عدة مشاريع في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6a533-170">Data Integrator will create multiple projects in Finance and Operations.</span></span> <span data-ttu-id="6a533-171">وتكون العلاقة بين مهمة موحد البيانات ومشروع Finance and Operations علاقة واحد بواحد.</span><span class="sxs-lookup"><span data-stu-id="6a533-171">The relationship between the Data Integrator task and the Finance and Operations project is one to one.</span></span>

<span data-ttu-id="6a533-172">تتبع الوقت اعتبارًا من سجل تنفيذ موحد البيانات وابحث عن مشروع الفهرس-1 في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6a533-172">Trace the time from the Data Integrator execution history and look for the index -1 project in Finance and Operations.</span></span> <span data-ttu-id="6a533-173">إذا كان رقم مهمة 9 في موحد البيانات"، فسيكون الفهرس 8 في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6a533-173">If the task number is 9 in Data Integrator, the index in Finance and Operations is 8.</span></span>

1. <span data-ttu-id="6a533-174">التقط فهرس المهمة من موحد البيانات (إنه "9" في هذا المثال).</span><span class="sxs-lookup"><span data-stu-id="6a533-174">Capture the task index from Data Integrator (in this example it is "9").</span></span>

![التقاط فهرس المهمة من موحد البيانات](media/CaptureTaskIndex.png)

2. <span data-ttu-id="6a533-176">تعقب وقت تنفيذ المشروع.</span><span class="sxs-lookup"><span data-stu-id="6a533-176">Track the execution time of the project.</span></span>

![تعقب وقت تنفيذ المشروع](media/CaptureTimeOfExecution.png)

3. <span data-ttu-id="6a533-178">في Finance and Operations، حدد الفهرس - 1.</span><span class="sxs-lookup"><span data-stu-id="6a533-178">In Finance and Operations, identify index - 1.</span></span> <span data-ttu-id="6a533-179">في هذا المثال، يتوافق المشروع مع اللاحقة "8" ووقت تنفيذ مشروع الفهرس "0" مع وقت التنفيذ في الخطوة 2.</span><span class="sxs-lookup"><span data-stu-id="6a533-179">In this example, the project with suffix "8" and execution time of index "0" project matches with the execution time in Step 2.</span></span>

![تعريف الفهرس](media/IdentifyIndex.png)

## <a name="after-integrating-talent-and-finance-and-operations-i-dont-see-my-talent-data-in-finance-and-operations-what-do-i-do"></a><span data-ttu-id="6a533-181">بعد تمكين التكامل بين Talent وFinance and Operations، لا يمكنني رؤية بيانات Talent في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6a533-181">After integrating Talent and Finance and Operations, I don’t see my Talent data in Finance and Operations.</span></span> <span data-ttu-id="6a533-182">ماذا أفعل؟</span><span class="sxs-lookup"><span data-stu-id="6a533-182">What do I do?</span></span>

<span data-ttu-id="6a533-183">التكامل مع Finance and Operations عبارة عن عملية تتكون من خطوتين.</span><span class="sxs-lookup"><span data-stu-id="6a533-183">The integration to Finance and Operations is a two-step process.</span></span> <span data-ttu-id="6a533-184">أولاً، تحقق من تحديث بيانات Talent ومن توفرها في Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="6a533-184">First, verify that the Talent data is updated and available in Common Data Service.</span></span> <span data-ttu-id="6a533-185">هذا الأمر عبارة عن مزامنة قريبة من الوقت الحقيقي ويمكن التحقق منها في PowerApps عن طريق مراجعة البيانات في كيانات البيانات.</span><span class="sxs-lookup"><span data-stu-id="6a533-185">This is a near real-time sync and can be verified in PowerApps by looking at the data within the data entities.</span></span>

![البيانات الموجودة في Common Data Service](media/DataInCDS.png)

<span data-ttu-id="6a533-187">إذا لم تظهر البيانات كما هو متوقع في Common Data Service، فتأكد من دعم الكيان في التكامل.</span><span class="sxs-lookup"><span data-stu-id="6a533-187">If the data is not appearing as expected in Common Data Service, verify that the entity is supported in the integration.</span></span> <span data-ttu-id="6a533-188">لتضمين بيانات إضافية في Common Data Service، ستتم مطالبة بإجراء تغيير من جانب Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6a533-188">To include additional data in Common Data Service, a change will be required on the Microsoft side.</span></span>

<span data-ttu-id="6a533-189">إذا كان الكيان مدعومًا والبيانات متوفرة في Common Data Service، فتأكد من صحة التعيين في موحد البيانات.</span><span class="sxs-lookup"><span data-stu-id="6a533-189">If the entity is supported and the data is available in Common Data Service, verify the mapping is correct in Data Integrator.</span></span> <span data-ttu-id="6a533-190">إذا كان تعيين موحد البيانات مقبولاً، فتحقق عندئذِ من نجاح تشغيل مهام إدارة البيانات.</span><span class="sxs-lookup"><span data-stu-id="6a533-190">If the integrator mapping looks okay, then verify the data management jobs have successfully run.</span></span> <span data-ttu-id="6a533-191">قد تحدث بعض الأخطاء أثناء تنفيذ الوظائف الدفعية.</span><span class="sxs-lookup"><span data-stu-id="6a533-191">Errors may occur during the execution of the batch jobs.</span></span> <span data-ttu-id="6a533-192">لمزيد من المعلومات حول إدارة البيانات، راجع [إدارة البيانات](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).</span><span class="sxs-lookup"><span data-stu-id="6a533-192">For more information about Data Management, see [Data management](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).</span></span>

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-and-operations-what-should-i-do"></a><span data-ttu-id="6a533-193">عناوين الموظفين غير صحيحة بعد استيرادها إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6a533-193">The addresses for my employees are incorrect after I import them into Finance and Operations.</span></span> <span data-ttu-id="6a533-194">ماذا أفعل؟</span><span class="sxs-lookup"><span data-stu-id="6a533-194">What should I do?</span></span>

<span data-ttu-id="6a533-195">يستخدم التسلسل الرقمي في **معرّف الموقع** النمط نفسه في كل من Talent وFinance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6a533-195">The number sequence for **Location ID** uses the same pattern in both Talent and Finance and Operations.</span></span> <span data-ttu-id="6a533-196">يجب أن يكون التسلسل الرقمي فريدًا على الجانبين لتفادي حدوث تضارب في العناوين عند تنفيذ تكامل البيانات من Common Data Service إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6a533-196">The number sequence needs to be unique on both sides so there are no address collisions when integrating data from Common Data Service to Finance and Operations.</span></span>

<span data-ttu-id="6a533-197">أثناء تنفيذ Talent، تأكد من أن التسلسلات الرقمية ليست نفسها في Talent قدرات وFinance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6a533-197">During implementation of Talent, verify that the number sequences are not the same in Talent and Finance and Operations.</span></span> <span data-ttu-id="6a533-198">تأكد من أن كافة التسلسلات الرقمية ليست مماثلة حيث قد يتم الاحتفاظ بالبيانات في كلا النظامين.</span><span class="sxs-lookup"><span data-stu-id="6a533-198">Validate that all number sequences are not identical where data may be maintained in both systems.</span></span>

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a><span data-ttu-id="6a533-199">عند إنشاء مجموعة الاتصالات، لا يمكنني رؤية الاتصال في القائمة المنسدلة "اتصال".</span><span class="sxs-lookup"><span data-stu-id="6a533-199">When creating my connection set, I am unable to see the connection in the Connection drop-down list.</span></span> <span data-ttu-id="6a533-200">ماذا أفعل؟</span><span class="sxs-lookup"><span data-stu-id="6a533-200">What do I do?</span></span>

<span data-ttu-id="6a533-201">عند إنشاء اتصالاتك، تأكد من اختيار Dynamics 365 for Finance and Operations (حاليًا في المعاينة) وCommon Data Service.</span><span class="sxs-lookup"><span data-stu-id="6a533-201">Make sure when creating your connections, you choose Dynamics 365 for Finance and Operations (currently in preview) and Common Data Service.</span></span>

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a><span data-ttu-id="6a533-202">عند مزامنة عمليات التوظيف، أتلقى رسائل الخطأ "CompanyInfo_FK غير موجود" أو "القيمة '12/31/2154 11:59:59 ص" في الحقل "تاريخ انتهاء التوظيف" غير موجودة في الجدول ذي الصلة "التوظيف"." ماذا أفعل؟‬</span><span class="sxs-lookup"><span data-stu-id="6a533-202">When syncing employments, I get the errors “CompanyInfo_FK doesn’t exist" or “The value '12/31/2154 11:59:59 pm' in field 'Employment end date' is not found in the related table 'Employment'.” What should I do?</span></span>

<span data-ttu-id="6a533-203">تأكد من أنك تقوم بالتعيين إلى الكيانات القانونية الصحيحة.</span><span class="sxs-lookup"><span data-stu-id="6a533-203">Ensure that you are mapping to the correct legal entities.</span></span> <span data-ttu-id="6a533-204">مزامنة الكيان القانوني ليست جزءًا من القالب الافتراضي، وبالتالي من المتوقع أن يكون كل كيان قانوني موجود في Talent وCommon Data Service موجود أيضًا في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6a533-204">Legal entity syncing is not part of the default template, so it is expected that each legal entity that is present in Talent and Common Data Service is also present in Finance and Operations.</span></span>
<span data-ttu-id="6a533-205">تأكد أيضًا من أنك تحدد الكيانات القانونية الصحيحة لمجموعة الاتصالات المرتبطة.</span><span class="sxs-lookup"><span data-stu-id="6a533-205">Also, make sure that you are selecting the correct legal entities for the associated Connection Set.</span></span>

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-and-operations-appears-to-be-empty-what-should-i-do"></a><span data-ttu-id="6a533-206">بعد إعداد مشروعي، يبدو تعيين الحقول في Finance and Operations فارغًا.</span><span class="sxs-lookup"><span data-stu-id="6a533-206">After setting up my project, the field mapping for Finance and Operations appears to be empty.</span></span> <span data-ttu-id="6a533-207">ماذا أفعل؟</span><span class="sxs-lookup"><span data-stu-id="6a533-207">What should I do?</span></span>

<span data-ttu-id="6a533-208">يمكنك تحديث كيانات البيانات في Finance and Operations بالانتقال إلى **إدارة البيانات \> محددات إطار العمل‬ \> إعدادات الكيان‬ \> تحديث قائمة الكيانات.**</span><span class="sxs-lookup"><span data-stu-id="6a533-208">Refresh the data entities in Finance and Operations by going to **Data management \> Framework Parameters \> Entity settings \> Refresh entity list.**</span></span> <span data-ttu-id="6a533-209">قد يستغرق استكمال هذا الإجراء دقائق قليلة تتمكن بعدها من رؤية هذه التعيينات.</span><span class="sxs-lookup"><span data-stu-id="6a533-209">This should take a couple of minutes to complete, then you should see those mappings.</span></span> <span data-ttu-id="6a533-210">تحدث هذه المشكلة عند إنشاء مشاريع جديدة.</span><span class="sxs-lookup"><span data-stu-id="6a533-210">This issue occurs when new projects are created.</span></span>

![تعيين حقول مفقود](media/MissingFieldMapping.png)

## <a name="additional-resources"></a><span data-ttu-id="6a533-212">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="6a533-212">Additional resources</span></span>

- <span data-ttu-id="6a533-213">موحد البيانات (DI):</span><span class="sxs-lookup"><span data-stu-id="6a533-213">Data Integrator (DI):</span></span> 

  - [<span data-ttu-id="6a533-214">دمج البيانات في Common Data Service</span><span class="sxs-lookup"><span data-stu-id="6a533-214">Integrate data into Common Data Service</span></span>](https://docs.microsoft.com/powerapps/administrator/data-integrator)

  - [<span data-ttu-id="6a533-215">إدارة أخطاء موحد البيانات واستكشاف الأخطاء وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="6a533-215">Data Integrator error management and troubleshooting</span></span>](https://docs.microsoft.com/powerapps/administrator/data-integrator-error-management)

  - [<span data-ttu-id="6a533-216">الاستجابة لطلبات DSR للسجلات التي أنشأها النظام في PowerApps وMicrosoft Flow وCommon Data Service</span><span class="sxs-lookup"><span data-stu-id="6a533-216">Responding to DSR requests for system-generated logs in PowerApps, Microsoft Flow, and Common Data Service</span></span>](https://docs.microsoft.com/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- <span data-ttu-id="6a533-217">إدارة البيانات:</span><span class="sxs-lookup"><span data-stu-id="6a533-217">Data Management:</span></span>

  - [<span data-ttu-id="6a533-218">إدارة البيانات</span><span class="sxs-lookup"><span data-stu-id="6a533-218">Data management</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)
