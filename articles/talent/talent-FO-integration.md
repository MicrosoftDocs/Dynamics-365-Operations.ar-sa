---
title: الأسئلة المتداول حول تكامل Dynamics 365 Talent إلى Dynamics 365 Finance
description: يوضح هذا الموضوع البيانات التي تتم مزامنتها في تكامل Talent وFinance.
author: andreabichsel
manager: AnnBe
ms.date: 10/14/2019
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
ms.openlocfilehash: 8b9fa6b8d5109f873c784d384d49f685f94da228
ms.sourcegitcommit: dd991154231280aff9c9c5799e42799e2bfc02fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/15/2019
ms.locfileid: "2622758"
---
# <a name="dynamics-365-talent-to-dynamics-365-finance-integration-faq"></a><span data-ttu-id="12263-103">الأسئلة المتداول حول تكامل Dynamics 365 Talent إلى Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="12263-103">Dynamics 365 Talent to Dynamics 365 Finance integration FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="12263-104">يجيب هذا الموضوع عن الأسئلة الشائعة حول البيانات التي تتم مزامنتها عندما يتكامل Dynamics 365 Talent مع Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="12263-104">This topic answers common questions associated about what data is synchronized when Dynamics 365 Talent is integrated with Dynamics 365 Finance.</span></span>

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a><span data-ttu-id="12263-105">هل تتم مزامنة جميع البيانات أو بعض كيانات البيانات فقط؟</span><span class="sxs-lookup"><span data-stu-id="12263-105">Is all data synchronized or just some data entities?</span></span>

<span data-ttu-id="12263-106">بالنسبة لـ Core HR، تتم مزامنة مجموعة فرعية من البيانات.</span><span class="sxs-lookup"><span data-stu-id="12263-106">For Core HR, a subset of the data is synchronized.</span></span> <span data-ttu-id="12263-107">للحصول على قائمة بجميع الكيانات، راجع [التكامل من Dynamics 365 Talent إلى Dynamics 365 Finance](talent-financeandoperations-integration.md).</span><span class="sxs-lookup"><span data-stu-id="12263-107">For a list of all the entities, see [Integration from Dynamics 365 Talent to Dynamics 365 Finance](talent-financeandoperations-integration.md).</span></span>

<span data-ttu-id="12263-108">بالنسبة إلى Attract وOnboard، تعتبر كافة البيانات أصلية في Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="12263-108">For Attract and Onboard, all data is native to Common Data Service.</span></span>

## <a name="why-dont-i-see-any-data-synced-to-common-data-service"></a><span data-ttu-id="12263-109">لماذا لا أرى أية بيانات متزامنة مع Common Data Service؟</span><span class="sxs-lookup"><span data-stu-id="12263-109">Why don't I see any data synced to Common Data Service?</span></span>

<span data-ttu-id="12263-110">افتراضيًا، يكون تكامل خدمة Common Data Service متوقف في البيئات الجديدة التي لا تتضمن بيانات العرض التوضيحي المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="12263-110">By default, the Common Data Service integration is turned off in new environments that don't include the provided demo data.</span></span> <span data-ttu-id="12263-111">بشكل افتراضي، يتم تشغيله في بيئات جديده تتضمن البيانات التجريبية، وتبدأ مزامنة البيانات عند توفير البيئة.</span><span class="sxs-lookup"><span data-stu-id="12263-111">By default, it's turned on in new environments that include demo data, and data synchronization begins when the environment is provisioned.</span></span> <span data-ttu-id="12263-112">بعد تجهيز البيئة الخاصة بك لمزامنة البيانات، يمكنك تشغيل التكامل.</span><span class="sxs-lookup"><span data-stu-id="12263-112">After your environment is ready to sync data, you can turn on the integration.</span></span> <span data-ttu-id="12263-113">وللحصول على المزيد من المعلومات، راجع قسم [تكوين تكامل Common Data Service](hr-common-data-service-integration.md)</span><span class="sxs-lookup"><span data-stu-id="12263-113">For more information, see [Configure Common Data Service integration](hr-common-data-service-integration.md).</span></span>

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a><span data-ttu-id="12263-114">هل يمكنني إنشاء تعيين جديد من دون استخدام القوالب؟</span><span class="sxs-lookup"><span data-stu-id="12263-114">Can I create a new mapping without using the templates?</span></span>

<span data-ttu-id="12263-115">تعتبر القوالب نقطة بداية.</span><span class="sxs-lookup"><span data-stu-id="12263-115">Templates are the starting point.</span></span> <span data-ttu-id="12263-116">يمكنك إنشاء قالبك الخاص، ولكنك تحتاج دائمًا إلى قالب عند إنشاء مشروع تكامل.</span><span class="sxs-lookup"><span data-stu-id="12263-116">You can create your own template, but a template is always needed when creating an integration project.</span></span> <span data-ttu-id="12263-117">للحصول على مزيد من المعلومات حول موحد البيانات (DI) والقوالب والمشاريع، راجع [دمج البيانات في Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="12263-117">For more information about data integrator (DI), templates, and projects, see [Integrate data into Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

## <a name="can-i-map-financial-dimensions-to-transfer-between-talent-and-finance"></a><span data-ttu-id="12263-118">هل يمكنني تعيين الأبعاد المالية للتحويل بين Talent وFinance؟</span><span class="sxs-lookup"><span data-stu-id="12263-118">Can I map financial dimensions to transfer between Talent and Finance?</span></span>

<span data-ttu-id="12263-119">الأبعاد المالية غير موجودة حاليًا في Common Data Service ونتيجة لذلك لا تشكل جزءًا من القالب الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="12263-119">Financial dimensions aren’t currently in Common Data Service and as a result aren’t part of the default template.</span></span> <span data-ttu-id="12263-120">تم التخطيط لهذا الكيان، ولكن لا يتوفر حاليًا أي مخطط زمني للإصدار.</span><span class="sxs-lookup"><span data-stu-id="12263-120">This entity is planned, but currently no release timeline is available.</span></span>

<span data-ttu-id="12263-121">بالنسبة إلى البيانات الموجودة في Finance ولكن غير الموجودة في Talent، يمكن ربط النظامين معًا باستخدام **تكوين الارتباطات** في Talent.</span><span class="sxs-lookup"><span data-stu-id="12263-121">For data that resides in Finance but does not exist in Talent, link the two systems together by using **Configure Links** in Talent.</span></span> <span data-ttu-id="12263-122">للحصول على مزيد من المعلومات حول كيفية تكوين الارتباطات بين Talent وFinance، راجع [ما الجديد أو المتغير في Dynamics 365 Talent: Core HR (31 أكتوبر 2018)](whats-new-talent-october-31.md).</span><span class="sxs-lookup"><span data-stu-id="12263-122">For more information about how to configure links between Talent and Finance, see [What's new or changed in Dynamics 365 Talent: Core HR (October 31, 2018)](whats-new-talent-october-31.md).</span></span>

![تعيين الأبعاد المالية](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-why"></a><span data-ttu-id="12263-124">عندما أستورد موظفين، ينتقل هؤلاء في بعض الأحيان إلى عاملين غير نشطين في Finance.</span><span class="sxs-lookup"><span data-stu-id="12263-124">Sometimes when I import employees, they go into inactive workers in Finance.</span></span> <span data-ttu-id="12263-125">ما السبب؟</span><span class="sxs-lookup"><span data-stu-id="12263-125">Why?</span></span>

<span data-ttu-id="12263-126">قد تتلقى رسالة الخطأ هذه إذا لم يكن لدى الموظفين أي سجل يتضمن تفاصيل التوظيف النشط في Talent.</span><span class="sxs-lookup"><span data-stu-id="12263-126">You may get this error if employees don’t have an active employment detail record in Talent.</span></span> <span data-ttu-id="12263-127">لحل هذه المشكلة، انتقل إلى **إدارة الموظفين \> الموظفون \> سجل التوظيف‬ \> مدير التاريخ**، وتأكد من وجود سجل يتضمن تفاصيل التوظيف النشط.</span><span class="sxs-lookup"><span data-stu-id="12263-127">To resolve this, go to **Personnel Management \> Employees \> Employment History \> Date Manager**, and verify that there is an active employment detail record.</span></span>

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a><span data-ttu-id="12263-128">إذا اخترت تعيين مجموعة فرعية فقط من الحقول، فهل ستؤدي التغييرات التي تم إدخالها على حقول غير معينة إلى تشغيل عملية مزامنة؟</span><span class="sxs-lookup"><span data-stu-id="12263-128">If I select to map only a subset of fields, will changes made to non-mapped fields trigger a sync?</span></span>

<span data-ttu-id="12263-129">تتبع مزامنة البيانات جدول التنفيذ.</span><span class="sxs-lookup"><span data-stu-id="12263-129">Data sync follows the execution schedule.</span></span> <span data-ttu-id="12263-130">ستختار عملية التكامل سجلاً إذا تم تغيير أي حقل في السجل بصرف النظر عما إذا كان الحقل جزءًا من تعيين التكامل.</span><span class="sxs-lookup"><span data-stu-id="12263-130">The integration will pick up a record if any field in the record changes regardless if the field is part of integration mapping.</span></span>

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a><span data-ttu-id="12263-131">كيف يمكنني إرسال تغييرات العاملين النشطاء فقط وليس سجلات العاملين المنتهية خدماتهم؟</span><span class="sxs-lookup"><span data-stu-id="12263-131">How can I send only active worker changes and not the terminated records?</span></span>

<span data-ttu-id="12263-132">باستخدام "الاستعلام المتقدم"، يمكنك تصفية البيانات المصدر وإعادة تشكيلها قبل تمريرها إلى الوجهة.</span><span class="sxs-lookup"><span data-stu-id="12263-132">With the use of "Advanced query", you can filter and reshape source data before passing it into the destination.</span></span>

![الاستعلام المتقدم للعاملين النشطين](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-for-a-specific-entity"></a><span data-ttu-id="12263-134">هل يمكنني تحديد الحقول التي سيتم إرسالها إلى Finance لكيان معين؟</span><span class="sxs-lookup"><span data-stu-id="12263-134">Can I specify which fields to send to Finance for a specific entity?</span></span>

<span data-ttu-id="12263-135">يمكنك إضافة حقول أو إزالتها من مهمة التكامل.</span><span class="sxs-lookup"><span data-stu-id="12263-135">Fields can be added or removed from the integration task.</span></span> <span data-ttu-id="12263-136">لن يتم ملء كافة حقول البيانات الموجودة على كيان Common Data Service من Core HR.</span><span class="sxs-lookup"><span data-stu-id="12263-136">Not all data fields that exist on the Common Data Service entity will be populated from Core HR.</span></span>
<span data-ttu-id="12263-137">يمكنك ملء بيانات إضافية عبر PowerApps.</span><span class="sxs-lookup"><span data-stu-id="12263-137">Additional data can be populated via PowerApps.</span></span>

![إضافة حقول إلى أو إزالتها من مهمة تكامل](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-talent-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a><span data-ttu-id="12263-139">بعد إعداد التكامل كوظيفة دفعية، فقد Talent الاتصال بالنظام الوجهة.</span><span class="sxs-lookup"><span data-stu-id="12263-139">I set up integration as a batch job, but Talent lost connection to the destination system.</span></span> <span data-ttu-id="12263-140">كيف يمكنني إرسال مجموعة التغييرات نفسها إلى النظام الوجهة؟</span><span class="sxs-lookup"><span data-stu-id="12263-140">How can I send the same set of changes to the destination system?</span></span>

<span data-ttu-id="12263-141">لا حاجة إلى أي إعداد خاص لمعالجة الاستثناء.</span><span class="sxs-lookup"><span data-stu-id="12263-141">No special setup is required for exception handling.</span></span> <span data-ttu-id="12263-142">سيقوم موحد البيانات بشكل تلقائي بالتقاط الأخطاء التي تحدث في المصدر والوجهة وسيبلغ عنها وسيسمح بإعادة المحاولة يدويًا.</span><span class="sxs-lookup"><span data-stu-id="12263-142">The Data Integrator will automatically catch and report errors which occur at the source and destination and will allow manual retries.</span></span> <span data-ttu-id="12263-143">ومع ذلك، فهو لا يسمح بتصحيح البيانات يدويًا.</span><span class="sxs-lookup"><span data-stu-id="12263-143">However, it doesn’t allow manual data correction.</span></span> <span data-ttu-id="12263-144">إن كان هناك حاجة إلى إجراء عمليات تحديث للبيانات، فيجب أن تحدث في المصدر أو الوجهة.</span><span class="sxs-lookup"><span data-stu-id="12263-144">If data updates are needed, that should happen either at the source or the destination.</span></span>

## <a name="can-i-set-up-bi-directional-integration"></a><span data-ttu-id="12263-145">هل يمكنني إعداد تكامل ثنائي الاتجاه؟</span><span class="sxs-lookup"><span data-stu-id="12263-145">Can I set up bi-directional integration?</span></span>

<span data-ttu-id="12263-146">لا، التكامل أحادي الاتجاه في الوقت الحالي (Talent إلى Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="12263-146">No, integration is currently one-way (Talent to Finance and Operations).</span></span> <span data-ttu-id="12263-147">ومع ذلك، يوجد قالب افتراضي لإرسال البيانات من Talent إلى Finance.</span><span class="sxs-lookup"><span data-stu-id="12263-147">However, there is a default template available to send data from Talent to Finance.</span></span>

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a><span data-ttu-id="12263-148">هل يمكنني السماح بحذف السجلات كجزء من عملية التكامل؟</span><span class="sxs-lookup"><span data-stu-id="12263-148">Can I allow record deletion as part of my integration?</span></span>

<span data-ttu-id="12263-149">لا، لن يلتقط موحد البيانات السجلات المحذوفة لنقل البيانات.</span><span class="sxs-lookup"><span data-stu-id="12263-149">No, Data Integrator will not capture deleted records for data transfer.</span></span> <span data-ttu-id="12263-150">في الوقت الحالي، لم يتم تضمين سواء عمليات إنشاء وتحديث البيانات (UPSERT).</span><span class="sxs-lookup"><span data-stu-id="12263-150">Only data creation and updates (UPSERT) are currently included.</span></span>

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a><span data-ttu-id="12263-151">هل يمكن إعادة تشغيل التنفيذ الذي يتضمن أخطاء؟</span><span class="sxs-lookup"><span data-stu-id="12263-151">Can I rerun the errored execution?</span></span> <span data-ttu-id="12263-152">إذا كان الأمر كذلك، فهل سيرسل ملفًا كاملاً أو التغييرات فقط؟</span><span class="sxs-lookup"><span data-stu-id="12263-152">If so, will it send a full file or only the changes?</span></span>

<span data-ttu-id="12263-153">عملية التشغيل الأولى لموحد البيانات هي دائمًا عملية تشغيل كاملة.</span><span class="sxs-lookup"><span data-stu-id="12263-153">The first run of Data Integrator is always a full run.</span></span> <span data-ttu-id="12263-154">وتستند عمليات التشغيل التالية إلى تعقب التغييرات.</span><span class="sxs-lookup"><span data-stu-id="12263-154">Subsequent runs are based on change tracking.</span></span> <span data-ttu-id="12263-155">يستخرج تشغيل الخطأ، عند تنفيذه، السجلات الموجودة في نطاق التشغيل ويرسل أحدث التغييرات من Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="12263-155">When an error run is executed, it extracts the records in scope of the run and sends out the most recent changes from Common Data Service.</span></span>

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a><span data-ttu-id="12263-156">عند حفظ المشروع، أتلقى رسالة الخطأ: "يتضمن المشروع أخطاء تعيين".</span><span class="sxs-lookup"><span data-stu-id="12263-156">When I save the project, I get the error: “Project has mapping errors."</span></span> <span data-ttu-id="12263-157">ماذا أفعل؟</span><span class="sxs-lookup"><span data-stu-id="12263-157">What do I do?</span></span>

<span data-ttu-id="12263-158">تحقق من إعداد مفاتيح التكامل، وأدخل أية تغييرات مطلوبة على الإعداد، ثم قم بتحديث الكيانات في المشروع.</span><span class="sxs-lookup"><span data-stu-id="12263-158">Check the setup of your integration keys, make any required changes to the setup, then refresh the entities in the project.</span></span>

<span data-ttu-id="12263-159">عند استخدام القالب الافتراضي، سيتم استيراد مفاتيح التكامل بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="12263-159">When the default template is used, the integration keys will be automatically imported.</span></span> <span data-ttu-id="12263-160">قد تحدث هذه المشكلة عند إضافة مهام جديدة إلى القالب الموجود.</span><span class="sxs-lookup"><span data-stu-id="12263-160">This issue may occur when new tasks are added to the existing template.</span></span>

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a><span data-ttu-id="12263-161">إذا كان لديّ العدد N من الكيانات القانونية حتى توجد توظيفات للعاملين، هل أحتاج إلى إنشاء تعيين لكل واحد منهم؟</span><span class="sxs-lookup"><span data-stu-id="12263-161">If I have N number of legal entities where workers have employments, do I need to create a mapping for each of them?</span></span>

<span data-ttu-id="12263-162">نعم، لكل كيان قانوني في Finance، ستحتاج إلى مشروع تكامل منفصل في تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="12263-162">Yes, for each legal entity in Finance, you'll need a separate integration project in the data integration.</span></span>

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a><span data-ttu-id="12263-163">أحتاج إلى نقل البيانات التي لا تشكل جزءًا من القالب الافتراضي التي وفرته Microsoft.</span><span class="sxs-lookup"><span data-stu-id="12263-163">I need to transfer data that is not part of the default template provided by Microsoft.</span></span> <span data-ttu-id="12263-164">هل يمكنني القيام بذلك؟</span><span class="sxs-lookup"><span data-stu-id="12263-164">Can I do this?</span></span>

<span data-ttu-id="12263-165">نعم، يمكن إضافة حقول أو إزالتها من القالب الموجود.</span><span class="sxs-lookup"><span data-stu-id="12263-165">Yes, fields can be added to or removed from the existing template.</span></span> <span data-ttu-id="12263-166">ويمكن تعديل القالب لتضمين بيانات إضافية من كيانات أخرى في Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="12263-166">The template can be modified to include additional data from other Common Data Service entities.</span></span> <span data-ttu-id="12263-167">يجب أن يكون الكيان في Common Data Service لكي يتم تضمينه في القالب.</span><span class="sxs-lookup"><span data-stu-id="12263-167">The entity must be in Common Data Service for it to be included in the template.</span></span> 

## <a name="i-just-created-new-finance-and-talent-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a><span data-ttu-id="12263-168">لقد انتهيت الآن من إنشاء بيئات Finance وTalent، وتلقيت رسالة الخطأ "قيمة البيانات انتهاك قيود التكامل."</span><span class="sxs-lookup"><span data-stu-id="12263-168">I just created new Finance and Talent environments, and I'm getting the error "The data value violates integrity constraints."</span></span> <span data-ttu-id="12263-169">ما السبب؟</span><span class="sxs-lookup"><span data-stu-id="12263-169">Why?</span></span>

<span data-ttu-id="12263-170">بإمكان أسباب هذا الخطأ أن تشتمل على:</span><span class="sxs-lookup"><span data-stu-id="12263-170">Reasons for this error can include:</span></span>

- <span data-ttu-id="12263-171">أدى نقل البيانات إلى استخراج سجلات مكررة في المصدر (Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="12263-171">The data transfer resulted in duplicate records extraction at the source (Common Data Service).</span></span>

- <span data-ttu-id="12263-172">تتضمن عملية نقل البيانات قيمًا فارغة للحقول المطلوبة في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="12263-172">The data transfer has null values for fields that are required in Finance and Operations.</span></span> <span data-ttu-id="12263-173">تأكد من أن البيانات موجودة في Common Data Service وتستوفي شروط Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="12263-173">Verify the data that is in Common Data Service and meets the requirements of Finance and Operations.</span></span>

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a><span data-ttu-id="12263-174">إذا ظهرت أخطاء تتعلق بالتنفيذ ولم تتم مزامنة معرّف الموظف، كيف يمكنني العثور على محفوظات الوظيفة التي تتضمن سجل الموظف الفاشل؟</span><span class="sxs-lookup"><span data-stu-id="12263-174">If there are execution errors and the Employee ID didn't sync, how do I find the history job which has the failed employee record?</span></span>

<span data-ttu-id="12263-175">سينشئ موحد البيانات عدة مشاريع في Finance.</span><span class="sxs-lookup"><span data-stu-id="12263-175">Data Integrator will create multiple projects in Finance.</span></span> <span data-ttu-id="12263-176">وتكون العلاقة بين مهمة موحد البيانات ومشروع Finance علاقة واحد بواحد.</span><span class="sxs-lookup"><span data-stu-id="12263-176">The relationship between the Data Integrator task and the Finance project is one to one.</span></span>

<span data-ttu-id="12263-177">تتبع الوقت اعتبارًا من سجل تنفيذ موحد البيانات وابحث عن مشروع الفهرس-1 في Finance.</span><span class="sxs-lookup"><span data-stu-id="12263-177">Trace the time from the Data Integrator execution history and look for the index -1 project in Finance.</span></span> <span data-ttu-id="12263-178">إذا كان رقم مهمة 9 في موحد البيانات"، فسيكون الفهرس 8 في Finance.</span><span class="sxs-lookup"><span data-stu-id="12263-178">If the task number is 9 in Data Integrator, the index in Finance is 8.</span></span>

1. <span data-ttu-id="12263-179">التقط فهرس المهمة من موحد البيانات (إنه "9" في هذا المثال).</span><span class="sxs-lookup"><span data-stu-id="12263-179">Capture the task index from Data Integrator (in this example it is "9").</span></span>

![التقاط فهرس المهمة من موحد البيانات](media/CaptureTaskIndex.png)

2. <span data-ttu-id="12263-181">تعقب وقت تنفيذ المشروع.</span><span class="sxs-lookup"><span data-stu-id="12263-181">Track the execution time of the project.</span></span>

![تعقب وقت تنفيذ المشروع](media/CaptureTimeOfExecution.png)

3. <span data-ttu-id="12263-183">في Finance، قم بتعريف الفهرس-1.</span><span class="sxs-lookup"><span data-stu-id="12263-183">In Finance, identify index - 1.</span></span> <span data-ttu-id="12263-184">في هذا المثال، يتوافق المشروع مع اللاحقة "8" ووقت تنفيذ مشروع الفهرس "0" مع وقت التنفيذ في الخطوة 2.</span><span class="sxs-lookup"><span data-stu-id="12263-184">In this example, the project with suffix "8" and execution time of index "0" project matches with the execution time in Step 2.</span></span>

![تعريف الفهرس](media/IdentifyIndex.png)

## <a name="after-integrating-talent-and-finance-i-dont-see-my-talent-data-in-finance-what-do-i-do"></a><span data-ttu-id="12263-186">بعد تمكين التكامل بين Talent وFinance، لا يمكنني رؤية بيانات Talent في Finance.</span><span class="sxs-lookup"><span data-stu-id="12263-186">After integrating Talent and Finance, I don’t see my Talent data in Finance.</span></span> <span data-ttu-id="12263-187">ماذا أفعل؟</span><span class="sxs-lookup"><span data-stu-id="12263-187">What do I do?</span></span>

<span data-ttu-id="12263-188">التكامل مع Finance عبارة عن عملية تتكون من خطوتين.</span><span class="sxs-lookup"><span data-stu-id="12263-188">The integration to Finance is a two-step process.</span></span> <span data-ttu-id="12263-189">أولاً، تحقق من تحديث بيانات Talent ومن توفرها في Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="12263-189">First, verify that the Talent data is updated and available in Common Data Service.</span></span> <span data-ttu-id="12263-190">هذا الأمر عبارة عن مزامنة قريبة من الوقت الحقيقي ويمكن التحقق منها في PowerApps عن طريق مراجعة البيانات في كيانات البيانات.</span><span class="sxs-lookup"><span data-stu-id="12263-190">This is a near real-time sync and can be verified in PowerApps by looking at the data within the data entities.</span></span>

![البيانات الموجودة في Common Data Service](media/DataInCDS.png)

<span data-ttu-id="12263-192">إذا لم تظهر البيانات كما هو متوقع في Common Data Service، فتأكد من دعم الكيان في التكامل.</span><span class="sxs-lookup"><span data-stu-id="12263-192">If the data is not appearing as expected in Common Data Service, verify that the entity is supported in the integration.</span></span> <span data-ttu-id="12263-193">لتضمين بيانات إضافية في Common Data Service، ستتم مطالبة بإجراء تغيير من جانب Microsoft.</span><span class="sxs-lookup"><span data-stu-id="12263-193">To include additional data in Common Data Service, a change will be required on the Microsoft side.</span></span>

<span data-ttu-id="12263-194">إذا كان الكيان مدعومًا والبيانات متوفرة في Common Data Service، فتأكد من صحة التعيين في موحد البيانات.</span><span class="sxs-lookup"><span data-stu-id="12263-194">If the entity is supported and the data is available in Common Data Service, verify the mapping is correct in Data Integrator.</span></span> <span data-ttu-id="12263-195">إذا كان تعيين موحد البيانات مقبولاً، فتحقق عندئذِ من نجاح تشغيل مهام إدارة البيانات.</span><span class="sxs-lookup"><span data-stu-id="12263-195">If the integrator mapping looks okay, then verify the data management jobs have successfully run.</span></span> <span data-ttu-id="12263-196">قد تحدث بعض الأخطاء أثناء تنفيذ الوظائف الدفعية.</span><span class="sxs-lookup"><span data-stu-id="12263-196">Errors may occur during the execution of the batch jobs.</span></span> <span data-ttu-id="12263-197">لمزيد من المعلومات حول إدارة البيانات، راجع [إدارة البيانات](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).</span><span class="sxs-lookup"><span data-stu-id="12263-197">For more information about Data Management, see [Data management](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).</span></span>

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-what-should-i-do"></a><span data-ttu-id="12263-198">عناوين الموظفين غير صحيحة بعد استيرادها إلى Finance.</span><span class="sxs-lookup"><span data-stu-id="12263-198">The addresses for my employees are incorrect after I import them into Finance.</span></span> <span data-ttu-id="12263-199">ماذا أفعل؟</span><span class="sxs-lookup"><span data-stu-id="12263-199">What should I do?</span></span>

<span data-ttu-id="12263-200">يستخدم التسلسل الرقمي في **معرّف الموقع** النمط نفسه في كل من Talent وFinance.</span><span class="sxs-lookup"><span data-stu-id="12263-200">The number sequence for **Location ID** uses the same pattern in both Talent and Finance.</span></span> <span data-ttu-id="12263-201">يجب أن يكون التسلسل الرقمي فريدًا على الجانبين لتفادي حدوث تضارب في العناوين عند تنفيذ تكامل البيانات من Common Data Service إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="12263-201">The number sequence needs to be unique on both sides so there are no address collisions when integrating data from Common Data Service to Finance and Operations.</span></span>

<span data-ttu-id="12263-202">أثناء تنفيذ Talent، تأكد من أن التسلسلات الرقمية ليست نفسها في Talent قدرات وFinance.</span><span class="sxs-lookup"><span data-stu-id="12263-202">During implementation of Talent, verify that the number sequences are not the same in Talent and Finance.</span></span> <span data-ttu-id="12263-203">تأكد من أن كافة التسلسلات الرقمية ليست مماثلة حيث قد يتم الاحتفاظ بالبيانات في كلا النظامين.</span><span class="sxs-lookup"><span data-stu-id="12263-203">Validate that all number sequences are not identical where data may be maintained in both systems.</span></span>

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a><span data-ttu-id="12263-204">عند إنشاء مجموعة الاتصالات، لا يمكنني رؤية الاتصال في القائمة المنسدلة "اتصال".</span><span class="sxs-lookup"><span data-stu-id="12263-204">When creating my connection set, I am unable to see the connection in the Connection drop-down list.</span></span> <span data-ttu-id="12263-205">ماذا أفعل؟</span><span class="sxs-lookup"><span data-stu-id="12263-205">What do I do?</span></span>

<span data-ttu-id="12263-206">عند إنشاء اتصالاتك، تأكد من اختيار Dynamics 365 Finance و Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="12263-206">Make sure when creating your connections, you choose Dynamics 365 Finance and Common Data Service.</span></span>

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a><span data-ttu-id="12263-207">عند مزامنة عمليات التوظيف، أتلقى رسائل الخطأ "CompanyInfo_FK غير موجود" أو "القيمة '12/31/2154 11:59:59 ص" في الحقل "تاريخ انتهاء التوظيف" غير موجودة في الجدول ذي الصلة "التوظيف"." ماذا أفعل؟‬</span><span class="sxs-lookup"><span data-stu-id="12263-207">When syncing employments, I get the errors “CompanyInfo_FK doesn’t exist" or “The value '12/31/2154 11:59:59 pm' in field 'Employment end date' is not found in the related table 'Employment'.” What should I do?</span></span>

<span data-ttu-id="12263-208">تأكد من أنك تقوم بالتعيين إلى الكيانات القانونية الصحيحة.</span><span class="sxs-lookup"><span data-stu-id="12263-208">Ensure that you are mapping to the correct legal entities.</span></span> <span data-ttu-id="12263-209">مزامنة الكيان القانوني ليست جزءًا من القالب الافتراضي، وبالتالي من المتوقع أن يكون كل كيان قانوني موجود في Talent وCommon Data Service موجود أيضًا في Finance.</span><span class="sxs-lookup"><span data-stu-id="12263-209">Legal entity syncing is not part of the default template, so it is expected that each legal entity that is present in Talent and Common Data Service is also present in Finance.</span></span>
<span data-ttu-id="12263-210">تأكد أيضًا من أنك تحدد الكيانات القانونية الصحيحة لمجموعة الاتصالات المرتبطة.</span><span class="sxs-lookup"><span data-stu-id="12263-210">Also, make sure that you are selecting the correct legal entities for the associated Connection Set.</span></span>

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-appears-to-be-empty-what-should-i-do"></a><span data-ttu-id="12263-211">بعد إعداد مشروعي، يبدو تعيين الحقول في Finance فارغًا.</span><span class="sxs-lookup"><span data-stu-id="12263-211">After setting up my project, the field mapping for Finance appears to be empty.</span></span> <span data-ttu-id="12263-212">ماذا أفعل؟</span><span class="sxs-lookup"><span data-stu-id="12263-212">What should I do?</span></span>

<span data-ttu-id="12263-213">يمكنك تحديث كيانات البيانات في Finance بالانتقال إلى **إدارة البيانات \> محددات إطار العمل‬ \> إعدادات الكيان‬ \> تحديث قائمة الكيانات.**</span><span class="sxs-lookup"><span data-stu-id="12263-213">Refresh the data entities in Finance by going to **Data management \> Framework Parameters \> Entity settings \> Refresh entity list.**</span></span> <span data-ttu-id="12263-214">قد يستغرق استكمال هذا الإجراء دقائق قليلة تتمكن بعدها من رؤية هذه التعيينات.</span><span class="sxs-lookup"><span data-stu-id="12263-214">This should take a couple of minutes to complete, then you should see those mappings.</span></span> <span data-ttu-id="12263-215">تحدث هذه المشكلة عند إنشاء مشاريع جديدة.</span><span class="sxs-lookup"><span data-stu-id="12263-215">This issue occurs when new projects are created.</span></span>

![تعيين حقول مفقود](media/MissingFieldMapping.png)

## <a name="additional-resources"></a><span data-ttu-id="12263-217">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="12263-217">Additional resources</span></span>

- <span data-ttu-id="12263-218">موحد البيانات (DI):</span><span class="sxs-lookup"><span data-stu-id="12263-218">Data Integrator (DI):</span></span> 

  - [<span data-ttu-id="12263-219">دمج البيانات في Common Data Service</span><span class="sxs-lookup"><span data-stu-id="12263-219">Integrate data into Common Data Service</span></span>](https://docs.microsoft.com/powerapps/administrator/data-integrator)

  - [<span data-ttu-id="12263-220">إدارة أخطاء موحد البيانات واستكشاف الأخطاء وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="12263-220">Data Integrator error management and troubleshooting</span></span>](https://docs.microsoft.com/powerapps/administrator/data-integrator-error-management)

  - [<span data-ttu-id="12263-221">الاستجابة لطلبات DSR للسجلات التي أنشأها النظام في PowerApps و Microsoft FlowوCommon Data Service</span><span class="sxs-lookup"><span data-stu-id="12263-221">Responding to DSR requests for system-generated logs in PowerApps, Microsoft Flow, and Common Data Service</span></span>](https://docs.microsoft.com/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- <span data-ttu-id="12263-222">إدارة البيانات:</span><span class="sxs-lookup"><span data-stu-id="12263-222">Data Management:</span></span>

  - [<span data-ttu-id="12263-223">إدارة البيانات</span><span class="sxs-lookup"><span data-stu-id="12263-223">Data management</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)
