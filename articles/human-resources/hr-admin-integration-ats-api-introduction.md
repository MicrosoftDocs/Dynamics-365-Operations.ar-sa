---
title: مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب
description: يصف هذا الموضوع واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب (ATS) في Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 48e368fe69443a5105ddba78a887bf9159bfe52a
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125583"
---
# <a name="applicant-tracking-system-integration-api-introduction"></a><span data-ttu-id="d6758-103">مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب</span><span class="sxs-lookup"><span data-stu-id="d6758-103">Applicant Tracking System integration API introduction</span></span>

<span data-ttu-id="d6758-104">يصف هذا الموضوع واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب (ATS) في Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d6758-104">This topic describes the Dynamics 365 Human Resources Applicant Tracking System (ATS) integration API.</span></span> <span data-ttu-id="d6758-105">وهدف واجهة API هو تمكين عمليات التكامل الانسيابية بين أنظمة ATS في Dynamics 365 Human Resources وأنظمة الشركاء.</span><span class="sxs-lookup"><span data-stu-id="d6758-105">The intent of the API is to enable streamlined integrations between Dynamics 365 Human Resources and partnering ATSs.</span></span>

![سير عمل تكامل نظام ATS](media/hr-admin-integration-ats-api-introduction-flow.png)

<span data-ttu-id="d6758-107">تبدأ التجربة المتكاملة في الموارد البشرية عندما يقوم مدير التوظيف بإنشاء طلب توظيف.</span><span class="sxs-lookup"><span data-stu-id="d6758-107">The integrated experience begins in Human Resources when a hiring manager creates a recruiting request.</span></span> <span data-ttu-id="d6758-108">عند تنشيط الطلب، يقوم نظام ATS بسحب تفاصيل الطلب لإنشاء مشروع تعيين.</span><span class="sxs-lookup"><span data-stu-id="d6758-108">When the request is activated, the ATS pulls the detail for the request to create a recruiting project.</span></span> <span data-ttu-id="d6758-109">وبعد ذلك يتبع مسار التوظيف لتحديد مرشح للمنصب (المناصب) وتوظيفه.</span><span class="sxs-lookup"><span data-stu-id="d6758-109">Then it follows the recruiting pipeline to select and hire a candidate for the position(s).</span></span> <span data-ttu-id="d6758-110">وأخيرا، يكمل نظام ATS رحلة التكامل الكاملة عن طريق إرسال سجل المرشح المحدد إلى الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="d6758-110">Finally, the ATS completes the round-trip integration by sending the selected candidate’s record into Human Resources.</span></span> <span data-ttu-id="d6758-111">يمكن أن يمر سجل الترشيح بعد ذلك بمزيد من عمليات التحقق من الصحة ومهام سير العمل لإنشاء سجل الموظف.</span><span class="sxs-lookup"><span data-stu-id="d6758-111">The candidate record can then go through more onboarding validations and workflows to create the employee record.</span></span>

<span data-ttu-id="d6758-112">لتمكين التكامل، أضافت الموارد البشرية المكونات التالية:</span><span class="sxs-lookup"><span data-stu-id="d6758-112">To enable the integration, Human Resources has added the following components:</span></span>

1.  <span data-ttu-id="d6758-113">وظيفة لإنشاء طلب التوظيف.</span><span class="sxs-lookup"><span data-stu-id="d6758-113">Functionality to create a recruiting request.</span></span>
2.  <span data-ttu-id="d6758-114">ملف تعريف مرشح والسير العمل المرتبط.</span><span class="sxs-lookup"><span data-stu-id="d6758-114">An expanded candidate profile and related workflows.</span></span>
3.  <span data-ttu-id="d6758-115">تفتح واجهة API للتكامل الوظائف الجديدة لتكامل الطلبات.</span><span class="sxs-lookup"><span data-stu-id="d6758-115">An integration API opening up the new functionality to integrating applications.</span></span>

<span data-ttu-id="d6758-116">لمزيد من المعلومات حول إعداد طلب التعيين ووظيفة المرشح واستخدامها، راجع [توظيف المرشحين لوظيفة](hr-personnel-recruit.md).</span><span class="sxs-lookup"><span data-stu-id="d6758-116">For more information about setting up and using the recruiting request and candidate functionality, see [Recruit job candidates](hr-personnel-recruit.md).</span></span>

## <a name="microsoft-dataverse"></a><span data-ttu-id="d6758-117">Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="d6758-117">Microsoft Dataverse</span></span>

<span data-ttu-id="d6758-118">تأتي واجهة API مدمجة في Microsoft Dataverse (المعروف سابقًا بـ Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="d6758-118">This API is built on Microsoft Dataverse (formerly Common Data Service).</span></span> <span data-ttu-id="d6758-119">وتجري كافة أشكال تفاعل RESTful مع واجهة API هذه عن طريق واجهة ويب Microsoft Dataverse، التي تستخدم OData.</span><span class="sxs-lookup"><span data-stu-id="d6758-119">All RESTful interaction with this API is done via the Microsoft Dataverse Web API, which uses OData.</span></span> <span data-ttu-id="d6758-120">تعد واجهة API هذه مجموعة فرعية من واجهة ويب Dataverse.</span><span class="sxs-lookup"><span data-stu-id="d6758-120">This API is a subset of the Dataverse Web API.</span></span> <span data-ttu-id="d6758-121">تحدد واجهة ويب Dataverse خصائص مثل المصادقة واتفاقيات SLA و, الدفعة والتحكم في التزامن ومعالجة الأخطاء.</span><span class="sxs-lookup"><span data-stu-id="d6758-121">The Dataverse Web API defines characteristics such as authentication, SLAs, batch, concurrency control, and error handling.</span></span>

<span data-ttu-id="d6758-122">لمزيد من المعلومات عن واجهة ويب Microsoft Dataverse، راجع:</span><span class="sxs-lookup"><span data-stu-id="d6758-122">For more general information about the Microsoft Dataverse Web API, see:</span></span>

- [<span data-ttu-id="d6758-123">ما هو Microsoft Dataverse؟</span><span class="sxs-lookup"><span data-stu-id="d6758-123">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)
- [<span data-ttu-id="d6758-124">استخدام  واجهة ويب Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="d6758-124">Use the Microsoft Dataverse Web API</span></span>](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/overview)
- [<span data-ttu-id="d6758-125">دليل مطور Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="d6758-125">Microsoft Dataverse developer guide</span></span>](https://docs.microsoft.com/powerapps/developer/data-platform)

<span data-ttu-id="d6758-126">تتضمن الوثائق الواردة أعلاه تفاصيل وإرشادات للمطور حول استخدام واجهة ويب Dataverse، مثل [إدارة المصادقة](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/authenticate-web-api)، و[تنفيذ العمليات](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/perform-operations-web-api)، و[استخدام Postman مع واجهة API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/use-postman-web-api)، و[استخدام تعقب التغييرات أو رموز دلتا](https://docs.microsoft.com/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) مع واجهة API.</span><span class="sxs-lookup"><span data-stu-id="d6758-126">The above documentation includes detail and developer guidance on using the Dataverse Web API, such as [managing authentication](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/authenticate-web-api), [performing operations](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/perform-operations-web-api), [using Postman with the API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/use-postman-web-api), and [using change tracking or delta tokens](https://docs.microsoft.com/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) with the API.</span></span>

### <a name="option-sets"></a><span data-ttu-id="d6758-127">مجموعات الخيارات</span><span class="sxs-lookup"><span data-stu-id="d6758-127">Option sets</span></span>

<span data-ttu-id="d6758-128">يتضمن نموذج البيانات لواجهة API لتكامل نظام ATS الموضح في هذا المستند مجموعات الخيارات التي توفر قيمًا عددية مقترنة بخصائص الوحدة.</span><span class="sxs-lookup"><span data-stu-id="d6758-128">The data model for the ATS integration API described in this document includes option sets that provide enumerated values associated with entity properties.</span></span> <span data-ttu-id="d6758-129">للحصول على تفاصيل حول العمل مع مجموعات الخيارات في واجهة ويب Dataverse، راجع [إنشاء وتحديث مجموعات الخيارات باستخدام واجهة الويب](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets).</span><span class="sxs-lookup"><span data-stu-id="d6758-129">For detail on working with option sets in the Dataverse Web API, see [Create and update option sets using the Web API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets).</span></span> <span data-ttu-id="d6758-130">يتم تحديد مجموعات الخيارات لكل بيئة من بيئات Dataverse.</span><span class="sxs-lookup"><span data-stu-id="d6758-130">Option sets are defined for each Dataverse environment.</span></span>

### <a name="virtual-tables-for-human-resources-in-dataverse"></a><span data-ttu-id="d6758-131">الجداول الظاهرية للموارد البشرية في Dataverse</span><span class="sxs-lookup"><span data-stu-id="d6758-131">Virtual tables for Human Resources in Dataverse</span></span>

<span data-ttu-id="d6758-132">تستخدم نقاط النهاية لواجهات API لتكامل نظام ATS قدرات النظام الأساسي في الجدول الظاهري لـ Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="d6758-132">The endpoints for the ATS integration API use the virtual table platform capabilities of Microsoft Dataverse.</span></span> <span data-ttu-id="d6758-133">بشكل افتراضي، لا يتم نشر الجداول الظاهرية ونقاط نهاية واجهات API المقترنة بها لبيئات الموارد البشرية، مما يتيح للمؤسسات تحديد نقاط نهاية OData التي سيتم عرضها للبيئة.</span><span class="sxs-lookup"><span data-stu-id="d6758-133">By default, the virtual tables and their associated API endpoints are not deployed for Human Resources environments, enabling organizations to determine which OData endpoints will be exposed for the environment.</span></span> <span data-ttu-id="d6758-134">لاستخدام واجهة API، يجب إنشاء الجداول الظاهرية لكيانات الموارد البشرية للبيئة.</span><span class="sxs-lookup"><span data-stu-id="d6758-134">To use the API, the virtual tables for the Human Resources entities must be generated for the environment.</span></span> 

<span data-ttu-id="d6758-135">للحصول على معلومات حول إنشاء الجداول الظاهرية لواجهة API، راجع [تكوين الجداول الظاهرية في Dataverse](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span><span class="sxs-lookup"><span data-stu-id="d6758-135">For information on generating the virtual tables for the API, see [Configure Dataverse virtual tables](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span></span>

## <a name="data-model"></a><span data-ttu-id="d6758-136">نموذج البيانات</span><span class="sxs-lookup"><span data-stu-id="d6758-136">Data model</span></span>

<span data-ttu-id="d6758-137">يتم توسيط نموذج البيانات حول وحدتين رئيسيتين:</span><span class="sxs-lookup"><span data-stu-id="d6758-137">The data model is centered around two main entities:</span></span>

- <span data-ttu-id="d6758-138">يمثل **RecruitingRequest** طلبًا إلى ATS لتوظيف شخص لأحد المناصب المفتوحة أو أكثر. لمطالعة مثال استعلام، راجع [مثال استعلام طلب توظيف](hr-admin-integration-ats-api-recruiting-request-example-query.md).</span><span class="sxs-lookup"><span data-stu-id="d6758-138">**RecruitingRequest** represents a request to an ATS to recruit for one or more open positions.For an example query, see [Example query for Recruiting request](hr-admin-integration-ats-api-recruiting-request-example-query.md).</span></span>
- <span data-ttu-id="d6758-139">يمثل **CandidateToHire** تفاصيل المرشح الذي قبل العرض الخاص بالمنصب.</span><span class="sxs-lookup"><span data-stu-id="d6758-139">**CandidateToHire** represents details of a candidate who has accepted an offer for a position.</span></span> <span data-ttu-id="d6758-140">يمثل **الشخص** الفرد الذي سيكو المرشح.</span><span class="sxs-lookup"><span data-stu-id="d6758-140">**Person** represents the individual who is the candidate.</span></span> <span data-ttu-id="d6758-141">يمكن أن يكون لأحد الأشخاص أدوار متعددة في الشركة، مثل المرشح أو العامل أو الموظف أو المقاول.</span><span class="sxs-lookup"><span data-stu-id="d6758-141">A person can have multiple roles in the company, such as candidate, worker, employee, or contractor.</span></span> <span data-ttu-id="d6758-142">للاطلاع على مثال للاستعلام ، راجع [مثال الاستعلام عن المرشح المراد توظيفه](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).</span><span class="sxs-lookup"><span data-stu-id="d6758-142">For an example query, see [Example query for Candidate to hire](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).</span></span>

<span data-ttu-id="d6758-143">يوضح المخطط التالي العلاقات داخل API.</span><span class="sxs-lookup"><span data-stu-id="d6758-143">The following diagram illustrates relationships within the API.</span></span> <span data-ttu-id="d6758-144">تحتوي العديد من الأنواع على مفاتيح خارجية لكيانات أخرى موجودة مسبقا في الموارد البشرية لم يتم توضيحها هنا.</span><span class="sxs-lookup"><span data-stu-id="d6758-144">Several types have foreign keys to other, pre-existing entities in Human Resources that aren't illustrated here.</span></span> <span data-ttu-id="d6758-145">يوفر هذا المستند معلومات حول الكيانات الخاصة بسيناريوهات تكامل التعيين.</span><span class="sxs-lookup"><span data-stu-id="d6758-145">This document provides information on entities that are specific to recruiting integration scenarios.</span></span> <span data-ttu-id="d6758-146">ومع ذلك، هناك العديد من الكيانات الأخرى في واجهة ويب Dataverse لـ Dynamics 365 Human Resources يمكن أن تكون مرتبطة أيضًا بالتكامل الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="d6758-146">However, there are many other entities in the Dataverse Web API for Dynamics 365 Human Resources that may also be relevant to your integration.</span></span> <span data-ttu-id="d6758-147">على سبيل المثال، قد تحتاج أيضا إلى تفصيل العاملين أو الوظائف أو المناصب أو الكيانات الأخرى غير المحددة.</span><span class="sxs-lookup"><span data-stu-id="d6758-147">For example, you may also need detail for workers, jobs, positions, or other entities not defined here.</span></span> <span data-ttu-id="d6758-148">تجري الاشارة إلى العديد من هذه الكيانات في علاقات المفاتيح الخارجية أو خصائص التنقل.</span><span class="sxs-lookup"><span data-stu-id="d6758-148">Many of these entities are referenced in foreign key relationships or navigation properties.</span></span>

![نموذج بيانات واجهة API لتكامل ATS](media/hr-admin-integration-ats-api-data-model.png)

## <a name="recruiting-request-and-related-entities-and-option-sets"></a><span data-ttu-id="d6758-150">طلب التعيين والكيانات ذات الصلة ومجموعات الخيارات</span><span class="sxs-lookup"><span data-stu-id="d6758-150">Recruiting request and related entities and option sets</span></span>

<span data-ttu-id="d6758-151">مثال الاستعلام:</span><span class="sxs-lookup"><span data-stu-id="d6758-151">Example query:</span></span> 

- [<span data-ttu-id="d6758-152">مثال لاستعلام عن طلب تعيين</span><span class="sxs-lookup"><span data-stu-id="d6758-152">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)

<span data-ttu-id="d6758-153">الكيانات:</span><span class="sxs-lookup"><span data-stu-id="d6758-153">Entities:</span></span>

- [<span data-ttu-id="d6758-154">طلب التعيين</span><span class="sxs-lookup"><span data-stu-id="d6758-154">Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request.md)
- [<span data-ttu-id="d6758-155">منصب طلب التعيين</span><span class="sxs-lookup"><span data-stu-id="d6758-155">Recruiting request position</span></span>](hr-admin-integration-ats-api-recruiting-request-position.md)
- [<span data-ttu-id="d6758-156">المهارة في طلب التعيين</span><span class="sxs-lookup"><span data-stu-id="d6758-156">Recruiting request skill</span></span>](hr-admin-integration-ats-api-recruiting-request-skill.md)
- [<span data-ttu-id="d6758-157">التعليم في طلب التعيين</span><span class="sxs-lookup"><span data-stu-id="d6758-157">Recruiting request education</span></span>](hr-admin-integration-ats-api-recruiting-request-education.md)
- [<span data-ttu-id="d6758-158">موقع طلب التعيين</span><span class="sxs-lookup"><span data-stu-id="d6758-158">Recruiting request location</span></span>](hr-admin-integration-ats-api-recruiting-request-location.md)

<span data-ttu-id="d6758-159">مجموعات الخيارات:</span><span class="sxs-lookup"><span data-stu-id="d6758-159">Option sets:</span></span>

- [<span data-ttu-id="d6758-160">حالة الإعفاء من الوظيفة</span><span class="sxs-lookup"><span data-stu-id="d6758-160">Job exempt status</span></span>](hr-admin-integration-ats-api-job-exempt-status.md)
- [<span data-ttu-id="d6758-161">حالة منصب طلب التعيين</span><span class="sxs-lookup"><span data-stu-id="d6758-161">Recruiting request position status</span></span>](hr-admin-integration-ats-api-recruiting-request-position-status.md)
- [<span data-ttu-id="d6758-162">حالة طلب التعيين</span><span class="sxs-lookup"><span data-stu-id="d6758-162">Recruiting request status</span></span>](hr-admin-integration-ats-api-recruiting-request-status.md)
- [<span data-ttu-id="d6758-163">فئة الوظيفة التنظيمية</span><span class="sxs-lookup"><span data-stu-id="d6758-163">Regulatory job category</span></span>](hr-admin-integration-ats-api-regulatory-job-category.md)

## <a name="candidate-to-hire-and-related-entities-and-option-sets"></a><span data-ttu-id="d6758-164">المرشح المراد توظيفه والكيانات ذات الصلة ومجموعات الخيارات</span><span class="sxs-lookup"><span data-stu-id="d6758-164">Candidate to hire and related entities and option sets</span></span>

<span data-ttu-id="d6758-165">مثال الاستعلام:</span><span class="sxs-lookup"><span data-stu-id="d6758-165">Example query:</span></span>

- [<span data-ttu-id="d6758-166">مثال الاستعلام عن مرشح مراد توظيفه</span><span class="sxs-lookup"><span data-stu-id="d6758-166">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

<span data-ttu-id="d6758-167">الكيانات:</span><span class="sxs-lookup"><span data-stu-id="d6758-167">Entities:</span></span>

- [<span data-ttu-id="d6758-168">المرشح المُراد توظيفه</span><span class="sxs-lookup"><span data-stu-id="d6758-168">Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire.md)
- [<span data-ttu-id="d6758-169">الشخص</span><span class="sxs-lookup"><span data-stu-id="d6758-169">Person</span></span>](hr-admin-integration-ats-api-person.md)
- [<span data-ttu-id="d6758-170">تعليم الشخص</span><span class="sxs-lookup"><span data-stu-id="d6758-170">Person education</span></span>](hr-admin-integration-ats-api-person-education.md)
- [<span data-ttu-id="d6758-171">الخبرة المهنية للشخص</span><span class="sxs-lookup"><span data-stu-id="d6758-171">Person professional experience</span></span>](hr-admin-integration-ats-api-person-professional-experience.md)
- [<span data-ttu-id="d6758-172">عنوان الشخص</span><span class="sxs-lookup"><span data-stu-id="d6758-172">Person address</span></span>](hr-admin-integration-ats-api-person-address.md)
- [<span data-ttu-id="d6758-173">جهة اتصال الطرف</span><span class="sxs-lookup"><span data-stu-id="d6758-173">Party contact</span></span>](hr-admin-integration-ats-api-party-contact.md)
- [<span data-ttu-id="d6758-174">مهارة الشخص</span><span class="sxs-lookup"><span data-stu-id="d6758-174">Person skill</span></span>](hr-admin-integration-ats-api-person-skill.md)
- [<span data-ttu-id="d6758-175">مستوى التقييم</span><span class="sxs-lookup"><span data-stu-id="d6758-175">Rating level</span></span>](hr-admin-integration-ats-api-rating-level.md)
- [<span data-ttu-id="d6758-176">شهادة الشخص</span><span class="sxs-lookup"><span data-stu-id="d6758-176">Person certificate</span></span>](hr-admin-integration-ats-api-person-certificate.md)
- [<span data-ttu-id="d6758-177">نوع الشهادة</span><span class="sxs-lookup"><span data-stu-id="d6758-177">Certificate type</span></span>](hr-admin-integration-ats-api-certificate-type.md)
- [<span data-ttu-id="d6758-178">مراقبة الأشخاص</span><span class="sxs-lookup"><span data-stu-id="d6758-178">Person screening</span></span>](hr-admin-integration-ats-api-person-screening.md)
- [<span data-ttu-id="d6758-179">أنواع المراقبة</span><span class="sxs-lookup"><span data-stu-id="d6758-179">Screening types</span></span>](hr-admin-integration-ats-api-screening-types.md)
- [<span data-ttu-id="d6758-180">رقم الهوية للشخص</span><span class="sxs-lookup"><span data-stu-id="d6758-180">Person identification number</span></span>](hr-admin-integration-ats-api-person-identification-number.md)

<span data-ttu-id="d6758-181">مجموعات الخيارات:</span><span class="sxs-lookup"><span data-stu-id="d6758-181">Option sets:</span></span>

- [<span data-ttu-id="d6758-182">نتيجة تكامل مقدم الطلب</span><span class="sxs-lookup"><span data-stu-id="d6758-182">Applicant integration result</span></span>](hr-admin-integration-ats-api-applicant-integration-result.md)
- [<span data-ttu-id="d6758-183">فارغ نعم لا</span><span class="sxs-lookup"><span data-stu-id="d6758-183">Blank Yes No</span></span>](hr-admin-integration-ats-api-blank-yes-no.md)
- [<span data-ttu-id="d6758-184">حالة الإكمال</span><span class="sxs-lookup"><span data-stu-id="d6758-184">Completion status</span></span>](hr-admin-integration-ats-api-completion-status.md)
- [<span data-ttu-id="d6758-185">نوع جهة الاتصال</span><span class="sxs-lookup"><span data-stu-id="d6758-185">Contact type</span></span>](hr-admin-integration-ats-api-contact-type.md)
- [<span data-ttu-id="d6758-186">أساس رصيد التعليم</span><span class="sxs-lookup"><span data-stu-id="d6758-186">Education credit basis</span></span>](hr-admin-integration-ats-api-education-credit-basis.md)
- [<span data-ttu-id="d6758-187">الجنس</span><span class="sxs-lookup"><span data-stu-id="d6758-187">Gender</span></span>](hr-admin-integration-ats-api-gender.md)
- [<span data-ttu-id="d6758-188">الحالة الاجتماعية</span><span class="sxs-lookup"><span data-stu-id="d6758-188">Marital status</span></span>](hr-admin-integration-ats-api-marital-status.md)
- [<span data-ttu-id="d6758-189">شهور السنة</span><span class="sxs-lookup"><span data-stu-id="d6758-189">Months of year</span></span>](hr-admin-integration-ats-api-months-of-year.md)
- [<span data-ttu-id="d6758-190">لا نعم</span><span class="sxs-lookup"><span data-stu-id="d6758-190">No Yes</span></span>](hr-admin-integration-ats-api-no-yes.md)
- [<span data-ttu-id="d6758-191">وحدة الفترة</span><span class="sxs-lookup"><span data-stu-id="d6758-191">Period unit</span></span>](hr-admin-integration-ats-api-period-unit.md)
- [<span data-ttu-id="d6758-192">تكرار المراقبة</span><span class="sxs-lookup"><span data-stu-id="d6758-192">Screening frequency</span></span>](hr-admin-integration-ats-api-screening-frequency.md)
- [<span data-ttu-id="d6758-193">إنشاء تكرار المراقبة من</span><span class="sxs-lookup"><span data-stu-id="d6758-193">Screening frequency generate from</span></span>](hr-admin-integration-ats-api-screening-frequency-generate-from.md)
- [<span data-ttu-id="d6758-194">نوع مستوى المهارة</span><span class="sxs-lookup"><span data-stu-id="d6758-194">Skill level type</span></span>](hr-admin-integration-ats-api-skill-level-type.md)

## <a name="see-also"></a><span data-ttu-id="d6758-195">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="d6758-195">See also</span></span>

[<span data-ttu-id="d6758-196">تعيين المرشحين للوظائف</span><span class="sxs-lookup"><span data-stu-id="d6758-196">Recruit job candidates</span></span>](hr-personnel-recruit.md)<br>
[<span data-ttu-id="d6758-197">ما هو Microsoft Dataverse؟</span><span class="sxs-lookup"><span data-stu-id="d6758-197">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="d6758-198">استخدام  واجهة ويب Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="d6758-198">Use the Microsoft Dataverse Web API</span></span>](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/overview)<br>
[<span data-ttu-id="d6758-199">إنشاء مجموعات الخيارات وتحديثها باستخدام واجهة الويب</span><span class="sxs-lookup"><span data-stu-id="d6758-199">Create and update option sets using the Web API</span></span>](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>