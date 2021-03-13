---
title: ‏‫الأسئلة المتداولة حول التكامل مع Finance
description: يوضح هذا المقال البيانات التي تتم مزامنتها في تكامل Human Resources وFinance.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0a6432fb5b04097d81680aed4e940e47f5ff2902
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111338"
---
# <a name="integration-with-finance-faq"></a><span data-ttu-id="e38ae-103">‏‫الأسئلة المتداولة حول التكامل مع Finance</span><span class="sxs-lookup"><span data-stu-id="e38ae-103">Integration with Finance FAQ</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="e38ae-104">يجيب هذا الموضوع عن الأسئلة الشائعة حول البيانات التي تتم مزامنتها عندما يتكامل Dynamics 365 Human Resources مع Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="e38ae-104">This topic answers common questions associated about what data is synchronized when Dynamics 365 Human Resources is integrated with Dynamics 365 Finance.</span></span>

## <a name="can-i-edit-the-dynamics-365-talent-application-user-in-power-apps"></a><span data-ttu-id="e38ae-105">هل يمكنني تحرير مستخدم تطبيق Dynamics 365 Talent في Power Apps؟</span><span class="sxs-lookup"><span data-stu-id="e38ae-105">Can I edit the Dynamics 365 Talent application user in Power Apps?</span></span>

<span data-ttu-id="e38ae-106">الرقم</span><span class="sxs-lookup"><span data-stu-id="e38ae-106">No.</span></span> <span data-ttu-id="e38ae-107">إذا قمت بتحرير مستخدم تطبيق Human Resources، فقد يفشل التكامل بين Human Resources وDataverse.</span><span class="sxs-lookup"><span data-stu-id="e38ae-107">If you edit the Human Resources application user, the integration between Human Resources and Dataverse might fail.</span></span> <span data-ttu-id="e38ae-108">يوضح الجدول التالي الإعدادات الافتراضية لمستخدم تطبيق Talent.</span><span class="sxs-lookup"><span data-stu-id="e38ae-108">The following table shows the default settings for the Talent application user.</span></span>

| <span data-ttu-id="e38ae-109">الاسم الكامل</span><span class="sxs-lookup"><span data-stu-id="e38ae-109">Full Name</span></span> | <span data-ttu-id="e38ae-110">مُعرِّف التطبيق</span><span class="sxs-lookup"><span data-stu-id="e38ae-110">Application ID</span></span> | <span data-ttu-id="e38ae-111">معرف كائن Azure AD</span><span class="sxs-lookup"><span data-stu-id="e38ae-111">Azure AD Object ID</span></span> | <span data-ttu-id="e38ae-112">عنوان URI لمُعرِّف التطبيق</span><span class="sxs-lookup"><span data-stu-id="e38ae-112">Application ID URI</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="e38ae-113">Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="e38ae-113">Dynamics365 for Talent</span></span> | <span data-ttu-id="e38ae-114">f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="e38ae-114">f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span> | <span data-ttu-id="e38ae-115">27fd8129-4b3c-43f7-b1bf-47495d3a049b</span><span class="sxs-lookup"><span data-stu-id="e38ae-115">27fd8129-4b3c-43f7-b1bf-47495d3a049b</span></span> | <span data-ttu-id="e38ae-116">f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="e38ae-116">f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span> |

![الإعدادات الافتراضية لمستخدم تطبيق Talent](media/DynamicsApplicationUser.png)

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a><span data-ttu-id="e38ae-118">هل تتم مزامنة جميع البيانات أو بعض كيانات البيانات فقط؟</span><span class="sxs-lookup"><span data-stu-id="e38ae-118">Is all data synchronized or just some data entities?</span></span>

<span data-ttu-id="e38ae-119">تتم مزامنة مجموعة فرعية من البيانات.</span><span class="sxs-lookup"><span data-stu-id="e38ae-119">A subset of the data is synchronized.</span></span> <span data-ttu-id="e38ae-120">للحصول على قائمة بجميع الكيانات، راجع [التكامل مع Dynamics 365 Finance](hr-admin-integration-finance.md).</span><span class="sxs-lookup"><span data-stu-id="e38ae-120">For a list of all the entities, see [Integration with Dynamics 365 Finance](hr-admin-integration-finance.md).</span></span>

## <a name="why-dont-i-see-any-data-synced-to-dataverse"></a><span data-ttu-id="e38ae-121">لماذا لا أرى أية بيانات متزامنة مع Dataverse؟</span><span class="sxs-lookup"><span data-stu-id="e38ae-121">Why don't I see any data synced to Dataverse?</span></span>

<span data-ttu-id="e38ae-122">افتراضيًا، يكون تكامل خدمة Dataverse متوقف في البيئات الجديدة التي لا تتضمن بيانات العرض التوضيحي المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="e38ae-122">By default, the Dataverse integration is turned off in new environments that don't include the provided demo data.</span></span> <span data-ttu-id="e38ae-123">بشكل افتراضي، يتم تشغيله في بيئات جديده تتضمن البيانات التجريبية، وتبدأ مزامنة البيانات عند توفير البيئة.</span><span class="sxs-lookup"><span data-stu-id="e38ae-123">By default, it's turned on in new environments that include demo data, and data synchronization begins when the environment is provisioned.</span></span> <span data-ttu-id="e38ae-124">بعد تجهيز البيئة الخاصة بك لمزامنة البيانات، يمكنك تشغيل التكامل.</span><span class="sxs-lookup"><span data-stu-id="e38ae-124">After your environment is ready to sync data, you can turn on the integration.</span></span> <span data-ttu-id="e38ae-125">وللحصول على المزيد من المعلومات، راجع قسم [تكوين تكامل Dataverse](hr-admin-integration-common-data-service.md)</span><span class="sxs-lookup"><span data-stu-id="e38ae-125">For more information, see [Configure Dataverse integration](hr-admin-integration-common-data-service.md).</span></span>

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a><span data-ttu-id="e38ae-126">هل يمكنني إنشاء تعيين جديد من دون استخدام القوالب؟</span><span class="sxs-lookup"><span data-stu-id="e38ae-126">Can I create a new mapping without using the templates?</span></span>

<span data-ttu-id="e38ae-127">تعتبر القوالب نقطة بداية.</span><span class="sxs-lookup"><span data-stu-id="e38ae-127">Templates are the starting point.</span></span> <span data-ttu-id="e38ae-128">يمكنك إنشاء قالبك الخاص، ولكنك تحتاج دائمًا إلى قالب عند إنشاء مشروع تكامل.</span><span class="sxs-lookup"><span data-stu-id="e38ae-128">You can create your own template, but a template is always needed when creating an integration project.</span></span> <span data-ttu-id="e38ae-129">للحصول على مزيد من المعلومات حول موحد البيانات (DI) والقوالب والمشاريع، راجع [دمج البيانات في Microsoft Dataverse](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="e38ae-129">For more information about data integrator (DI), templates, and projects, see [Integrate data into Microsoft Dataverse](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

## <a name="can-i-map-financial-dimensions-to-transfer-between-human-resources-and-finance"></a><span data-ttu-id="e38ae-130">هل يمكنني تعيين الأبعاد المالية للتحويل بين Human Resources وFinance؟</span><span class="sxs-lookup"><span data-stu-id="e38ae-130">Can I map financial dimensions to transfer between Human Resources and Finance?</span></span>

<span data-ttu-id="e38ae-131">الأبعاد المالية غير موجودة حاليًا في Dataverse ونتيجة لذلك لا تشكل جزءًا من القالب الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="e38ae-131">Financial dimensions aren’t currently in Dataverse and as a result aren’t part of the default template.</span></span> <span data-ttu-id="e38ae-132">تم التخطيط لهذا الكيان، ولكن لا يتوفر حاليًا أي مخطط زمني للإصدار.</span><span class="sxs-lookup"><span data-stu-id="e38ae-132">This entity is planned, but currently no release timeline is available.</span></span>

<span data-ttu-id="e38ae-133">بالنسبة إلى البيانات الموجودة في Finance and Operations ولكن غير الموجودة في Human Resources، يمكن ربط النظامين معًا باستخدام **تكوين الارتباطات** في Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e38ae-133">For data that resides in Finance but does not exist in Human Resources, link the two systems together by using **Configure Links** in Human Resources.</span></span>

![تعيين الأبعاد المالية](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-why"></a><span data-ttu-id="e38ae-135">عندما أستورد موظفين، ينتقل هؤلاء في بعض الأحيان إلى عاملين غير نشطين في Finance.</span><span class="sxs-lookup"><span data-stu-id="e38ae-135">Sometimes when I import employees, they go into inactive workers in Finance.</span></span> <span data-ttu-id="e38ae-136">ما السبب؟</span><span class="sxs-lookup"><span data-stu-id="e38ae-136">Why?</span></span>

<span data-ttu-id="e38ae-137">قد تتلقى رسالة الخطأ هذه إذا لم يكن لدى الموظفين سجل تفاصيل التوظيف نشط في Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e38ae-137">You may get this error if employees don’t have an active employment detail record in Human Resources.</span></span> <span data-ttu-id="e38ae-138">لحل هذه المشكلة، انتقل إلى **إدارة الموظفين \> الموظفون \> سجل التوظيف‬ \> مدير التاريخ**، وتأكد من وجود سجل يتضمن تفاصيل التوظيف النشط.</span><span class="sxs-lookup"><span data-stu-id="e38ae-138">To resolve this, go to **Personnel Management \> Employees \> Employment History \> Date Manager**, and verify that there is an active employment detail record.</span></span>

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a><span data-ttu-id="e38ae-139">إذا اخترت تعيين مجموعة فرعية فقط من الحقول، فهل ستؤدي التغييرات التي تم إدخالها على حقول غير معينة إلى تشغيل عملية مزامنة؟</span><span class="sxs-lookup"><span data-stu-id="e38ae-139">If I select to map only a subset of fields, will changes made to non-mapped fields trigger a sync?</span></span>

<span data-ttu-id="e38ae-140">تتبع مزامنة البيانات جدول التنفيذ.</span><span class="sxs-lookup"><span data-stu-id="e38ae-140">Data sync follows the execution schedule.</span></span> <span data-ttu-id="e38ae-141">ستختار عملية التكامل سجلاً إذا تم تغيير أي حقل في السجل بصرف النظر عما إذا كان الحقل جزءًا من تعيين التكامل.</span><span class="sxs-lookup"><span data-stu-id="e38ae-141">The integration will pick up a record if any field in the record changes regardless if the field is part of integration mapping.</span></span>

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a><span data-ttu-id="e38ae-142">كيف يمكنني إرسال تغييرات العاملين النشطاء فقط وليس سجلات العاملين المنتهية خدماتهم؟</span><span class="sxs-lookup"><span data-stu-id="e38ae-142">How can I send only active worker changes and not the terminated records?</span></span>

<span data-ttu-id="e38ae-143">باستخدام "الاستعلام المتقدم"، يمكنك تصفية البيانات المصدر وإعادة تشكيلها قبل تمريرها إلى الوجهة.</span><span class="sxs-lookup"><span data-stu-id="e38ae-143">With the use of "Advanced query", you can filter and reshape source data before passing it into the destination.</span></span>

![الاستعلام المتقدم للعاملين النشطين](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-for-a-specific-entity"></a><span data-ttu-id="e38ae-145">هل يمكنني تحديد الحقول التي سيتم إرسالها إلى Finance لكيان معين؟</span><span class="sxs-lookup"><span data-stu-id="e38ae-145">Can I specify which fields to send to Finance for a specific entity?</span></span>

<span data-ttu-id="e38ae-146">يمكنك إضافة حقول أو إزالتها من مهمة التكامل.</span><span class="sxs-lookup"><span data-stu-id="e38ae-146">Fields can be added or removed from the integration task.</span></span> <span data-ttu-id="e38ae-147">لن يتم ملء كافة حقول البيانات الموجودة على جدول Dataverse من Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e38ae-147">Not all data fields that exist on the Dataverse table will be populated from Human Resources.</span></span>
<span data-ttu-id="e38ae-148">يمكنك ملء بيانات إضافية عبر Power Apps.</span><span class="sxs-lookup"><span data-stu-id="e38ae-148">Additional data can be populated via Power Apps.</span></span>

![إضافة حقول إلى أو إزالتها من مهمة تكامل](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-human-resources-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a><span data-ttu-id="e38ae-150">بعد إعداد التكامل كوظيفة دفعية، ولكن فقد Human Resources الاتصال بالنظام الوجهة.</span><span class="sxs-lookup"><span data-stu-id="e38ae-150">I set up integration as a batch job, but Human Resources lost connection to the destination system.</span></span> <span data-ttu-id="e38ae-151">كيف يمكنني إرسال مجموعة التغييرات نفسها إلى النظام الوجهة؟</span><span class="sxs-lookup"><span data-stu-id="e38ae-151">How can I send the same set of changes to the destination system?</span></span>

<span data-ttu-id="e38ae-152">لا حاجة إلى أي إعداد خاص لمعالجة الاستثناء.</span><span class="sxs-lookup"><span data-stu-id="e38ae-152">No special setup is required for exception handling.</span></span> <span data-ttu-id="e38ae-153">سيقوم موحد البيانات بشكل تلقائي بالتقاط الأخطاء التي تحدث في المصدر والوجهة وسيبلغ عنها وسيسمح بإعادة المحاولة يدويًا.</span><span class="sxs-lookup"><span data-stu-id="e38ae-153">The Data Integrator will automatically catch and report errors which occur at the source and destination and will allow manual retries.</span></span> <span data-ttu-id="e38ae-154">ومع ذلك، فهو لا يسمح بتصحيح البيانات يدويًا.</span><span class="sxs-lookup"><span data-stu-id="e38ae-154">However, it doesn’t allow manual data correction.</span></span> <span data-ttu-id="e38ae-155">إن كان هناك حاجة إلى إجراء عمليات تحديث للبيانات، فيجب أن تحدث في المصدر أو الوجهة.</span><span class="sxs-lookup"><span data-stu-id="e38ae-155">If data updates are needed, that should happen either at the source or the destination.</span></span>

## <a name="can-i-set-up-bi-directional-integration"></a><span data-ttu-id="e38ae-156">هل يمكنني إعداد تكامل ثنائي الاتجاه؟</span><span class="sxs-lookup"><span data-stu-id="e38ae-156">Can I set up bi-directional integration?</span></span>

<span data-ttu-id="e38ae-157">لا، يكون التكامل حاليًا ذو اتجاه واحد (من Human Resources إلى Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="e38ae-157">No, integration is currently one-way (Human Resources to Finance and Operations).</span></span> <span data-ttu-id="e38ae-158">ومع ذلك، يوجد قالب افتراضي لإرسال البيانات من Human Resources إلى Finance.</span><span class="sxs-lookup"><span data-stu-id="e38ae-158">However, there is a default template available to send data from Human Resources to Finance.</span></span>

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a><span data-ttu-id="e38ae-159">هل يمكنني السماح بحذف السجلات كجزء من عملية التكامل؟</span><span class="sxs-lookup"><span data-stu-id="e38ae-159">Can I allow record deletion as part of my integration?</span></span>

<span data-ttu-id="e38ae-160">لا، لن يلتقط موحد البيانات السجلات المحذوفة لنقل البيانات.</span><span class="sxs-lookup"><span data-stu-id="e38ae-160">No, Data Integrator will not capture deleted records for data transfer.</span></span> <span data-ttu-id="e38ae-161">في الوقت الحالي، لم يتم تضمين سواء عمليات إنشاء وتحديث البيانات (UPSERT).</span><span class="sxs-lookup"><span data-stu-id="e38ae-161">Only data creation and updates (UPSERT) are currently included.</span></span>

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a><span data-ttu-id="e38ae-162">هل يمكن إعادة تشغيل التنفيذ الذي يتضمن أخطاء؟</span><span class="sxs-lookup"><span data-stu-id="e38ae-162">Can I rerun the errored execution?</span></span> <span data-ttu-id="e38ae-163">إذا كان الأمر كذلك، فهل سيرسل ملفًا كاملاً أو التغييرات فقط؟</span><span class="sxs-lookup"><span data-stu-id="e38ae-163">If so, will it send a full file or only the changes?</span></span>

<span data-ttu-id="e38ae-164">عملية التشغيل الأولى لموحد البيانات هي دائمًا عملية تشغيل كاملة.</span><span class="sxs-lookup"><span data-stu-id="e38ae-164">The first run of Data Integrator is always a full run.</span></span> <span data-ttu-id="e38ae-165">وتستند عمليات التشغيل التالية إلى تعقب التغييرات.</span><span class="sxs-lookup"><span data-stu-id="e38ae-165">Subsequent runs are based on change tracking.</span></span> <span data-ttu-id="e38ae-166">يستخرج تشغيل الخطأ، عند تنفيذه، السجلات الموجودة في نطاق التشغيل ويرسل أحدث التغييرات من Dataverse.</span><span class="sxs-lookup"><span data-stu-id="e38ae-166">When an error run is executed, it extracts the records in scope of the run and sends out the most recent changes from Dataverse.</span></span>

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a><span data-ttu-id="e38ae-167">عند حفظ المشروع، أتلقى رسالة الخطأ: "يتضمن المشروع أخطاء تعيين".</span><span class="sxs-lookup"><span data-stu-id="e38ae-167">When I save the project, I get the error: “Project has mapping errors."</span></span> <span data-ttu-id="e38ae-168">ماذا أفعل؟</span><span class="sxs-lookup"><span data-stu-id="e38ae-168">What do I do?</span></span>

<span data-ttu-id="e38ae-169">تحقق من إعداد مفاتيح التكامل، وأدخل أية تغييرات مطلوبة على الإعداد، ثم قم بتحديث الكيانات في المشروع.</span><span class="sxs-lookup"><span data-stu-id="e38ae-169">Check the setup of your integration keys, make any required changes to the setup, then refresh the entities in the project.</span></span>

<span data-ttu-id="e38ae-170">عند استخدام القالب الافتراضي، سيتم استيراد مفاتيح التكامل بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="e38ae-170">When the default template is used, the integration keys will be automatically imported.</span></span> <span data-ttu-id="e38ae-171">قد تحدث هذه المشكلة عند إضافة مهام جديدة إلى القالب الموجود.</span><span class="sxs-lookup"><span data-stu-id="e38ae-171">This issue may occur when new tasks are added to the existing template.</span></span>

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a><span data-ttu-id="e38ae-172">إذا كان لديّ العدد N من الكيانات القانونية حتى توجد توظيفات للعاملين، هل أحتاج إلى إنشاء تعيين لكل واحد منهم؟</span><span class="sxs-lookup"><span data-stu-id="e38ae-172">If I have N number of legal entities where workers have employments, do I need to create a mapping for each of them?</span></span>

<span data-ttu-id="e38ae-173">نعم، لكل كيان قانوني في Finance، ستحتاج إلى مشروع تكامل منفصل في تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="e38ae-173">Yes, for each legal entity in Finance, you'll need a separate integration project in the data integration.</span></span>

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a><span data-ttu-id="e38ae-174">أحتاج إلى نقل البيانات التي لا تشكل جزءًا من القالب الافتراضي التي وفرته Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e38ae-174">I need to transfer data that is not part of the default template provided by Microsoft.</span></span> <span data-ttu-id="e38ae-175">هل يمكنني القيام بذلك؟</span><span class="sxs-lookup"><span data-stu-id="e38ae-175">Can I do this?</span></span>

<span data-ttu-id="e38ae-176">نعم، يمكن إضافة حقول أو إزالتها من القالب الموجود.</span><span class="sxs-lookup"><span data-stu-id="e38ae-176">Yes, fields can be added to or removed from the existing template.</span></span> <span data-ttu-id="e38ae-177">ويمكن تعديل القالب لتضمين بيانات إضافية من جداول أخرى في Dataverse.</span><span class="sxs-lookup"><span data-stu-id="e38ae-177">The template can be modified to include additional data from other Dataverse tables.</span></span> <span data-ttu-id="e38ae-178">يجب أن يكون الكيان في Dataverse لكي يتم تضمينه في القالب.</span><span class="sxs-lookup"><span data-stu-id="e38ae-178">The entity must be in Dataverse for it to be included in the template.</span></span> 

## <a name="i-just-created-new-finance-and-human-resources-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a><span data-ttu-id="e38ae-179">لقد انتهيت الآن من إنشاء بيئات Finance وHuman Resources الجديدة، وتلقيت رسالة الخطأ "‏‫انتهكت قيمة البيانات قيود التكامل."</span><span class="sxs-lookup"><span data-stu-id="e38ae-179">I just created new Finance and Human Resources environments, and I'm getting the error "The data value violates integrity constraints."</span></span> <span data-ttu-id="e38ae-180">ما السبب؟</span><span class="sxs-lookup"><span data-stu-id="e38ae-180">Why?</span></span>

<span data-ttu-id="e38ae-181">بإمكان أسباب هذا الخطأ أن تشتمل على:</span><span class="sxs-lookup"><span data-stu-id="e38ae-181">Reasons for this error can include:</span></span>

- <span data-ttu-id="e38ae-182">أدى نقل البيانات إلى استخراج سجلات مكررة في المصدر (Dataverse).</span><span class="sxs-lookup"><span data-stu-id="e38ae-182">The data transfer resulted in duplicate records extraction at the source (Dataverse).</span></span>

- <span data-ttu-id="e38ae-183">تتضمن عملية نقل البيانات قيمًا فارغة للحقول المطلوبة في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e38ae-183">The data transfer has null values for fields that are required in Finance and Operations.</span></span> <span data-ttu-id="e38ae-184">تأكد من أن البيانات موجودة في Dataverse وتستوفي شروط Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e38ae-184">Verify the data that is in Dataverse and meets the requirements of Finance and Operations.</span></span>

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a><span data-ttu-id="e38ae-185">إذا ظهرت أخطاء تتعلق بالتنفيذ ولم تتم مزامنة معرّف الموظف، كيف يمكنني العثور على محفوظات الوظيفة التي تتضمن سجل الموظف الفاشل؟</span><span class="sxs-lookup"><span data-stu-id="e38ae-185">If there are execution errors and the Employee ID didn't sync, how do I find the history job which has the failed employee record?</span></span>

<span data-ttu-id="e38ae-186">سينشئ موحد البيانات عدة مشاريع في Finance.</span><span class="sxs-lookup"><span data-stu-id="e38ae-186">Data Integrator will create multiple projects in Finance.</span></span> <span data-ttu-id="e38ae-187">وتكون العلاقة بين مهمة موحد البيانات ومشروع Finance علاقة واحد بواحد.</span><span class="sxs-lookup"><span data-stu-id="e38ae-187">The relationship between the Data Integrator task and the Finance project is one to one.</span></span>

<span data-ttu-id="e38ae-188">تتبع الوقت اعتبارًا من سجل تنفيذ موحد البيانات وابحث عن مشروع الفهرس-1 في Finance.</span><span class="sxs-lookup"><span data-stu-id="e38ae-188">Trace the time from the Data Integrator execution history and look for the index -1 project in Finance.</span></span> <span data-ttu-id="e38ae-189">إذا كان رقم مهمة 9 في موحد البيانات"، فسيكون الفهرس 8 في Finance.</span><span class="sxs-lookup"><span data-stu-id="e38ae-189">If the task number is 9 in Data Integrator, the index in Finance is 8.</span></span>

1. <span data-ttu-id="e38ae-190">التقط فهرس المهمة من موحد البيانات (إنه "9" في هذا المثال).</span><span class="sxs-lookup"><span data-stu-id="e38ae-190">Capture the task index from Data Integrator (in this example it is "9").</span></span>

    ![التقاط فهرس المهمة من موحد البيانات](media/CaptureTaskIndex.png)

2. <span data-ttu-id="e38ae-192">تعقب وقت تنفيذ المشروع.</span><span class="sxs-lookup"><span data-stu-id="e38ae-192">Track the execution time of the project.</span></span>

    ![تعقب وقت تنفيذ المشروع](media/CaptureTimeOfExecution.png)

3. <span data-ttu-id="e38ae-194">في Finance، قم بتعريف الفهرس-1.</span><span class="sxs-lookup"><span data-stu-id="e38ae-194">In Finance, identify index - 1.</span></span> <span data-ttu-id="e38ae-195">في هذا المثال، يتوافق المشروع مع اللاحقة "8" ووقت تنفيذ مشروع الفهرس "0" مع وقت التنفيذ في الخطوة 2.</span><span class="sxs-lookup"><span data-stu-id="e38ae-195">In this example, the project with suffix "8" and execution time of index "0" project matches with the execution time in Step 2.</span></span>

    ![تعريف الفهرس](media/IdentifyIndex.png)

## <a name="after-integrating-human-resources-and-finance-i-dont-see-my-human-resources-data-in-finance-what-do-i-do"></a><span data-ttu-id="e38ae-197">بعد تكامل Human Resources وFinance، لا يمكنني رؤية بيانات Human Resources الخاصة بي في Finance.</span><span class="sxs-lookup"><span data-stu-id="e38ae-197">After integrating Human Resources and Finance, I don’t see my Human Resources data in Finance.</span></span> <span data-ttu-id="e38ae-198">ماذا أفعل؟</span><span class="sxs-lookup"><span data-stu-id="e38ae-198">What do I do?</span></span>

<span data-ttu-id="e38ae-199">التكامل مع Finance عبارة عن عملية تتكون من خطوتين.</span><span class="sxs-lookup"><span data-stu-id="e38ae-199">The integration to Finance is a two-step process.</span></span> <span data-ttu-id="e38ae-200">أولاً، تحقق من تحديث بيانات Human Resources ومن توفرها في Dataverse.</span><span class="sxs-lookup"><span data-stu-id="e38ae-200">First, verify that the Human Resources data is updated and available in Dataverse.</span></span> <span data-ttu-id="e38ae-201">هذا الأمر عبارة عن مزامنة قريبة من الوقت الحقيقي ويمكن التحقق منها في Power Apps عن طريق مراجعة البيانات في جداول البيانات.</span><span class="sxs-lookup"><span data-stu-id="e38ae-201">This is a near real-time sync and can be verified in Power Apps by looking at the data within the data tables.</span></span>

![البيانات الموجودة في Dataverse](media/DataInCDS.png)

<span data-ttu-id="e38ae-203">إذا لم تظهر البيانات كما هو متوقع في Dataverse، فتأكد من دعم الكيان في التكامل.</span><span class="sxs-lookup"><span data-stu-id="e38ae-203">If the data is not appearing as expected in Dataverse, verify that the entity is supported in the integration.</span></span> <span data-ttu-id="e38ae-204">لتضمين بيانات إضافية في Dataverse، ستتم مطالبة بإجراء تغيير من جانب Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e38ae-204">To include additional data in Dataverse, a change will be required on the Microsoft side.</span></span>

<span data-ttu-id="e38ae-205">إذا كان الكيان مدعومًا والبيانات متوفرة في Dataverse، فتأكد من صحة التعيين في موحد البيانات.</span><span class="sxs-lookup"><span data-stu-id="e38ae-205">If the entity is supported and the data is available in Dataverse, verify the mapping is correct in Data Integrator.</span></span> <span data-ttu-id="e38ae-206">إذا كان تعيين موحد البيانات مقبولاً، فتحقق عندئذِ من نجاح تشغيل مهام إدارة البيانات.</span><span class="sxs-lookup"><span data-stu-id="e38ae-206">If the integrator mapping looks okay, then verify the data management jobs have successfully run.</span></span> <span data-ttu-id="e38ae-207">قد تحدث بعض الأخطاء أثناء تنفيذ الوظائف الدفعية.</span><span class="sxs-lookup"><span data-stu-id="e38ae-207">Errors may occur during the execution of the batch jobs.</span></span> <span data-ttu-id="e38ae-208">لمزيد من المعلومات حول إدارة البيانات، راجع [إدارة البيانات](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).</span><span class="sxs-lookup"><span data-stu-id="e38ae-208">For more information about Data Management, see [Data management](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).</span></span>

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-what-should-i-do"></a><span data-ttu-id="e38ae-209">عناوين الموظفين غير صحيحة بعد استيرادها إلى Finance.</span><span class="sxs-lookup"><span data-stu-id="e38ae-209">The addresses for my employees are incorrect after I import them into Finance.</span></span> <span data-ttu-id="e38ae-210">ماذا أفعل؟</span><span class="sxs-lookup"><span data-stu-id="e38ae-210">What should I do?</span></span>

<span data-ttu-id="e38ae-211">يستخدم التسلسل الرقمي في **معرّف الموقع** النمط نفسه في كل من Human Resources وFinance.</span><span class="sxs-lookup"><span data-stu-id="e38ae-211">The number sequence for **Location ID** uses the same pattern in both Human Resources and Finance.</span></span> <span data-ttu-id="e38ae-212">يجب أن يكون التسلسل الرقمي فريدًا على الجانبين لتفادي حدوث تضارب في العناوين عند تنفيذ تكامل البيانات من Dataverse إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e38ae-212">The number sequence needs to be unique on both sides so there are no address collisions when integrating data from Dataverse to Finance and Operations.</span></span>

<span data-ttu-id="e38ae-213">أثناء تنفيذ Human Resources، تأكد من أن التسلسلات الرقمية ليست هي نفسها في Human Resources وFinance.</span><span class="sxs-lookup"><span data-stu-id="e38ae-213">During implementation of Human Resources, verify that the number sequences are not the same in Human Resources and Finance.</span></span> <span data-ttu-id="e38ae-214">تأكد من أن كافة التسلسلات الرقمية ليست مماثلة حيث قد يتم الاحتفاظ بالبيانات في كلا النظامين.</span><span class="sxs-lookup"><span data-stu-id="e38ae-214">Validate that all number sequences are not identical where data may be maintained in both systems.</span></span>

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a><span data-ttu-id="e38ae-215">عند إنشاء مجموعة الاتصالات، لا يمكنني رؤية الاتصال في القائمة المنسدلة "اتصال".</span><span class="sxs-lookup"><span data-stu-id="e38ae-215">When creating my connection set, I am unable to see the connection in the Connection drop-down list.</span></span> <span data-ttu-id="e38ae-216">ماذا أفعل؟</span><span class="sxs-lookup"><span data-stu-id="e38ae-216">What do I do?</span></span>

<span data-ttu-id="e38ae-217">عند إنشاء اتصالاتك، تأكد من اختيار Dynamics 365 Finance و Dataverse.</span><span class="sxs-lookup"><span data-stu-id="e38ae-217">Make sure when creating your connections, you choose Dynamics 365 Finance and Dataverse.</span></span>

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a><span data-ttu-id="e38ae-218">عند مزامنة عمليات التوظيف، أتلقى رسائل الخطأ "CompanyInfo_FK غير موجود" أو "القيمة '12/31/2154 11:59:59 ص" في الحقل "تاريخ انتهاء التوظيف" غير موجودة في الجدول ذي الصلة "التوظيف"." ماذا أفعل؟‬</span><span class="sxs-lookup"><span data-stu-id="e38ae-218">When syncing employments, I get the errors “CompanyInfo_FK doesn’t exist" or “The value '12/31/2154 11:59:59 pm' in field 'Employment end date' is not found in the related table 'Employment'.” What should I do?</span></span>

<span data-ttu-id="e38ae-219">تأكد من أنك تقوم بالتعيين إلى الكيانات القانونية الصحيحة.</span><span class="sxs-lookup"><span data-stu-id="e38ae-219">Ensure that you are mapping to the correct legal entities.</span></span> <span data-ttu-id="e38ae-220">لا تمثل مزامنة الكيان القانوني جزءًا من القالب الافتراضي، وبالتالي من المتوقع أن يكون كل كيان قانوني موجود في Human Resources و Dataverse موجود أيضًا في Finance.</span><span class="sxs-lookup"><span data-stu-id="e38ae-220">Legal entity syncing is not part of the default template, so it is expected that each legal entity that is present in Human Resources and Dataverse is also present in Finance.</span></span>
<span data-ttu-id="e38ae-221">تأكد أيضًا من أنك تحدد الكيانات القانونية الصحيحة لمجموعة الاتصالات المرتبطة.</span><span class="sxs-lookup"><span data-stu-id="e38ae-221">Also, make sure that you are selecting the correct legal entities for the associated Connection Set.</span></span>

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-appears-to-be-empty-what-should-i-do"></a><span data-ttu-id="e38ae-222">بعد إعداد مشروعي، يبدو تعيين الحقول في Finance فارغًا.</span><span class="sxs-lookup"><span data-stu-id="e38ae-222">After setting up my project, the field mapping for Finance appears to be empty.</span></span> <span data-ttu-id="e38ae-223">ماذا أفعل؟</span><span class="sxs-lookup"><span data-stu-id="e38ae-223">What should I do?</span></span>

<span data-ttu-id="e38ae-224">يمكنك تحديث كيانات البيانات في Finance بالانتقال إلى **إدارة البيانات \> محددات إطار العمل‬ \> إعدادات الكيان‬ \> تحديث قائمة الكيانات.**</span><span class="sxs-lookup"><span data-stu-id="e38ae-224">Refresh the data entities in Finance by going to **Data management \> Framework Parameters \> Entity settings \> Refresh entity list.**</span></span> <span data-ttu-id="e38ae-225">قد يستغرق استكمال هذا الإجراء دقائق قليلة تتمكن بعدها من رؤية هذه التعيينات.</span><span class="sxs-lookup"><span data-stu-id="e38ae-225">This should take a couple of minutes to complete, then you should see those mappings.</span></span> <span data-ttu-id="e38ae-226">تحدث هذه المشكلة عند إنشاء مشاريع جديدة.</span><span class="sxs-lookup"><span data-stu-id="e38ae-226">This issue occurs when new projects are created.</span></span>

![تعيين حقول مفقود](media/MissingFieldMapping.png)

## <a name="additional-resources"></a><span data-ttu-id="e38ae-228">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="e38ae-228">Additional resources</span></span>

- <span data-ttu-id="e38ae-229">موحد البيانات (DI):</span><span class="sxs-lookup"><span data-stu-id="e38ae-229">Data Integrator (DI):</span></span> 

  - [<span data-ttu-id="e38ae-230">دمج البيانات في Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="e38ae-230">Integrate data into Microsoft Dataverse</span></span>](https://docs.microsoft.com/powerapps/administrator/data-integrator)

  - [<span data-ttu-id="e38ae-231">إدارة أخطاء موحد البيانات واستكشاف الأخطاء وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="e38ae-231">Data Integrator error management and troubleshooting</span></span>](https://docs.microsoft.com/powerapps/administrator/data-integrator-error-management)

  - [<span data-ttu-id="e38ae-232">الاستجابة لطلبات DSR للسجلات التي أنشأها النظام في Power Apps، وMicrosoft Power Automate، وDataverse</span><span class="sxs-lookup"><span data-stu-id="e38ae-232">Responding to DSR requests for system-generated logs in Power Apps, Microsoft Power Automate, and Dataverse</span></span>](https://docs.microsoft.com/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- <span data-ttu-id="e38ae-233">إدارة البيانات:</span><span class="sxs-lookup"><span data-stu-id="e38ae-233">Data Management:</span></span>

  - [<span data-ttu-id="e38ae-234">إدارة البيانات</span><span class="sxs-lookup"><span data-stu-id="e38ae-234">Data management</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)
