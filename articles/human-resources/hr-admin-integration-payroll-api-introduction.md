---
title: ‏‫مقدمة إلى واجهة API لتكامل كشف الرواتب
description: يصف هذا الموضوع واجهة API لتكامل كشف الرواتب في  Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 61b90c566325bb8d83b09fceebc721cfb14d3fc8
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891116"
---
# <a name="payroll-integration-api-introduction"></a><span data-ttu-id="22b1c-103">‏‫مقدمة إلى واجهة API لتكامل كشف الرواتب</span><span class="sxs-lookup"><span data-stu-id="22b1c-103">Payroll integration API introduction</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="22b1c-104">يصف هذا المستند واجهة API لتكامل كشف الرواتب في  Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="22b1c-104">This document describes the Dynamics 365 Human Resources Payroll integration API.</span></span> <span data-ttu-id="22b1c-105">تمكّن واجهة API عمليات التكامل الشاملة الانسيابية بين Human Resources وأنظمة كشف الرواتب الشريكة.</span><span class="sxs-lookup"><span data-stu-id="22b1c-105">The API enables streamlined end-to-end integrations between Human Resources and partnering payroll systems.</span></span> <span data-ttu-id="22b1c-106">تبدأ التجربة المتكاملة في Human Resources مع معلومات عن ملف تعريف الموظف والراتب والخصم ومعلومات المساهمة.</span><span class="sxs-lookup"><span data-stu-id="22b1c-106">The integrated experience begins in Human Resources with the employee profile, salary and deduction, and contribution information.</span></span> <span data-ttu-id="22b1c-107">عند توظيف أحد الموظفين وإدخال معلومات الدفع وملف التعريف المطلوبة في Human Resources، يسحب نظام كشف الرواتب هذه المعلومات لاستخدامها عند معالجة كشف الرواتب.</span><span class="sxs-lookup"><span data-stu-id="22b1c-107">When you hire an employee and enter the required profile and pay information into Human Resources, the payroll system pulls this information to use when processing payroll.</span></span> <span data-ttu-id="22b1c-108">ويتم أيضًا سحب التحديثات التي تتم على معلومات الموظف أو الدفع لاستخداما في عمليات تشغيل الدفع اللاحقة.</span><span class="sxs-lookup"><span data-stu-id="22b1c-108">Any updates made to the employee or pay information are also pulled for use in later pay runs.</span></span>

![‏‫سير مهام تكامل كشف الرواتب](media/hr-admin-integration-payroll-api-introduction-flow.png)

<span data-ttu-id="22b1c-110">لتمكين التكامل، تتضمن Human Resources المكونات التالية:</span><span class="sxs-lookup"><span data-stu-id="22b1c-110">To enable the integration, Human Resources includes the following components:</span></span>

- <span data-ttu-id="22b1c-111">وظيفة لوضع علامة على الموظف كجاهز للدفع</span><span class="sxs-lookup"><span data-stu-id="22b1c-111">Functionality to mark an employee as ready to pay</span></span>
- <span data-ttu-id="22b1c-112">واجهة API للتكامل تفتتح الوظائف الجديدة لتكامل التطبيقات.</span><span class="sxs-lookup"><span data-stu-id="22b1c-112">An integration API opening up the new functionality to integrating applications</span></span>

## <a name="microsoft-dataverse"></a><span data-ttu-id="22b1c-113">Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="22b1c-113">Microsoft Dataverse</span></span>

<span data-ttu-id="22b1c-114">تأتي واجهة API مدمجة في Microsoft Dataverse (المعروف سابقًا بـ Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="22b1c-114">This API is built on Microsoft Dataverse (formerly Common Data Service).</span></span> <span data-ttu-id="22b1c-115">وتجري كافة أشكال تفاعل RESTful مع واجهة API هذه عن طريق واجهة ويب Microsoft Dataverse، التي تستخدم OData.</span><span class="sxs-lookup"><span data-stu-id="22b1c-115">All RESTful interaction with this API is done via the Microsoft Dataverse Web API, which uses OData.</span></span> <span data-ttu-id="22b1c-116">تعد واجهة API هذه مجموعة فرعية من واجهة ويب Dataverse.</span><span class="sxs-lookup"><span data-stu-id="22b1c-116">This API is a subset of the Dataverse Web API.</span></span> <span data-ttu-id="22b1c-117">تحدد واجهة ويب Dataverse خصائص مثل المصادقة واتفاقيات SLA و, الدفعة والتحكم في التزامن ومعالجة الأخطاء.</span><span class="sxs-lookup"><span data-stu-id="22b1c-117">The Dataverse Web API defines characteristics such as authentication, SLAs, batch, concurrency control, and error handling.</span></span>

<span data-ttu-id="22b1c-118">لمزيد من المعلومات عن واجهة ويب Microsoft Dataverse، راجع:</span><span class="sxs-lookup"><span data-stu-id="22b1c-118">For more general information about the Microsoft Dataverse Web API, see:</span></span>

- [<span data-ttu-id="22b1c-119">ما هو Microsoft Dataverse؟</span><span class="sxs-lookup"><span data-stu-id="22b1c-119">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)
- [<span data-ttu-id="22b1c-120">استخدام  واجهة ويب Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="22b1c-120">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)
- [<span data-ttu-id="22b1c-121">دليل مطور Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="22b1c-121">Microsoft Dataverse developer guide</span></span>](/powerapps/developer/data-platform)

<span data-ttu-id="22b1c-122">تتضمن هذه الوثائق تفاصيل وإرشادات للمطور تتعلق باستخدام واجهة API الويب في Dataverse، بما في ذلك الموضوعات التالية:</span><span class="sxs-lookup"><span data-stu-id="22b1c-122">This documentation includes details and developer guidance for using the Dataverse Web API, including the following topics:</span></span>

- [<span data-ttu-id="22b1c-123">المصادقة مع Microsoft Dataverse باستخدام واجهة API‎ الويب</span><span class="sxs-lookup"><span data-stu-id="22b1c-123">Authenticate to Microsoft Dataverse with the Web API</span></span>](/powerapps/developer/data-platform/webapi/authenticate-web-api)
- [<span data-ttu-id="22b1c-124">تنفيذ عمليات باستخدام واجهة API‎ الويب</span><span class="sxs-lookup"><span data-stu-id="22b1c-124">Perform operations using the Web API</span></span>](/powerapps/developer/data-platform/webapi/perform-operations-web-api)
- [<span data-ttu-id="22b1c-125">استخدام Postman مع واجهة API‎ الويب</span><span class="sxs-lookup"><span data-stu-id="22b1c-125">Use Postman with the Web API</span></span>](/powerapps/developer/data-platform/webapi/use-postman-web-api)
- [<span data-ttu-id="22b1c-126">استخدام تعقب التغييرات لمزامنة البيانات مع الأنظمة الخارجية</span><span class="sxs-lookup"><span data-stu-id="22b1c-126">Use change tracking to synchronize data with external systems</span></span>](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)

### <a name="virtual-tables-for-human-resources-in-dataverse"></a><span data-ttu-id="22b1c-127">الجداول الظاهرية للموارد البشرية في Dataverse</span><span class="sxs-lookup"><span data-stu-id="22b1c-127">Virtual tables for Human Resources in Dataverse</span></span>

<span data-ttu-id="22b1c-128">تستخدم نقاط النهاية لواجهة API لتكامل كشف الرواتب قدرات النظام الأساسي للجداول الظاهرية فيـ Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="22b1c-128">The endpoints for the Payroll integration API use the virtual table platform capabilities of Microsoft Dataverse.</span></span> <span data-ttu-id="22b1c-129">بشكل افتراضي، لا يتم نشر الجداول الظاهرية ونقاط نهاية واجهات API المقترنة بها لبيئات Human Resources، مما يتيح للمؤسسات تحديد نقاط نهاية OData التي سيتم عرضها للبيئة.</span><span class="sxs-lookup"><span data-stu-id="22b1c-129">By default, the virtual tables and their associated API endpoints aren't deployed for Human Resources environments, enabling organizations to determine which OData endpoints will be exposed for the environment.</span></span> <span data-ttu-id="22b1c-130">لاستخدام واجهة API، يجب إنشاء الجداول الظاهرية لكيانات الموارد البشرية للبيئة.</span><span class="sxs-lookup"><span data-stu-id="22b1c-130">To use the API, the virtual tables for the Human Resources entities must be generated for the environment.</span></span>

<span data-ttu-id="22b1c-131">للحصول على معلومات حول إنشاء الجداول الظاهرية لواجهة API، راجع [تكوين الجداول الظاهرية في Dataverse](./hr-admin-integration-common-data-service-virtual-entities.md).</span><span class="sxs-lookup"><span data-stu-id="22b1c-131">For information on generating the virtual tables for the API, see [Configure Dataverse virtual tables](./hr-admin-integration-common-data-service-virtual-entities.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="22b1c-132">نموذج البيانات</span><span class="sxs-lookup"><span data-stu-id="22b1c-132">Data model</span></span>

<span data-ttu-id="22b1c-133">يوضح المخطط التالي العلاقات داخل API.</span><span class="sxs-lookup"><span data-stu-id="22b1c-133">The following diagram illustrates relationships within the API.</span></span> <span data-ttu-id="22b1c-134">تحتوي العديد من الأنواع على مفاتيح خارجية لكيانات أخرى موجودة مسبقا في الموارد البشرية لم يتم توضيحها هنا.</span><span class="sxs-lookup"><span data-stu-id="22b1c-134">Several types have foreign keys to other, pre-existing entities in Human Resources that aren't illustrated here.</span></span> <span data-ttu-id="22b1c-135">يوفر هذا المستند معلومات حول الكيانات الخاصة بسيناريوهات تكامل كشف الرواتب.</span><span class="sxs-lookup"><span data-stu-id="22b1c-135">This document provides information on entities that are specific to payroll integration scenarios.</span></span> <span data-ttu-id="22b1c-136">ومع ذلك، هناك العديد من الكيانات الأخرى في واجهة API الويب في Dataverse لـ Human Resources التي قد تكون أيضًا ذات صلة بعملية التكامل.</span><span class="sxs-lookup"><span data-stu-id="22b1c-136">However, there are many other entities in the Dataverse Web API for Human Resources that may also be relevant to your integration.</span></span> <span data-ttu-id="22b1c-137">يُشار إلى بعض هذه الكيانات في علاقات المفاتيح الخارجية أو خصائص التنقل.</span><span class="sxs-lookup"><span data-stu-id="22b1c-137">Some of these entities are referenced in foreign key relationships or navigation properties.</span></span>

![نموذج بيانات واجهة API لتكامل كشف الرواتب](media/hr-admin-payroll-api-data-model.png)

## <a name="payroll-employee-and-related-entities"></a><span data-ttu-id="22b1c-139">موظف كشف الرواتب والكيانات ذات الصلة</span><span class="sxs-lookup"><span data-stu-id="22b1c-139">Payroll employee and related entities</span></span>

<span data-ttu-id="22b1c-140">الكيانات:</span><span class="sxs-lookup"><span data-stu-id="22b1c-140">Entities:</span></span>

- [<span data-ttu-id="22b1c-141">الموظف حسب كشف الرواتب</span><span class="sxs-lookup"><span data-stu-id="22b1c-141">Payroll employee</span></span>](hr-admin-integration-payroll-api-payroll-employee.md)
- [<span data-ttu-id="22b1c-142">عنوان عامل كشف الرواتب</span><span class="sxs-lookup"><span data-stu-id="22b1c-142">Payroll worker address</span></span>](hr-admin-integration-payroll-api-payroll-worker-address.md)
- [<span data-ttu-id="22b1c-143">خطة التعويض الثابتة لكشف الرواتب</span><span class="sxs-lookup"><span data-stu-id="22b1c-143">Payroll fixed compensation plan</span></span>](hr-admin-integration-ats-api-recruiting-request-education.md)
- [<span data-ttu-id="22b1c-144">وظيفة منصب كشف الرواتب</span><span class="sxs-lookup"><span data-stu-id="22b1c-144">Payroll position job</span></span>](hr-admin-integration-payroll-api-payroll-position-job.md)
- [<span data-ttu-id="22b1c-145">منصب كشف الرواتب</span><span class="sxs-lookup"><span data-stu-id="22b1c-145">Payroll position</span></span>](hr-admin-integration-payroll-api-payroll-position.md)

## <a name="see-also"></a><span data-ttu-id="22b1c-146">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="22b1c-146">See also</span></span>

[<span data-ttu-id="22b1c-147">إنشاء كيانات كشف الرواتب ومراجعتها</span><span class="sxs-lookup"><span data-stu-id="22b1c-147">Generate and review payroll entities</span></span>](hr-admin-integration-payroll-api-generate-review-entities.md)<br>
[<span data-ttu-id="22b1c-148">تكوين معلمات Human Resources</span><span class="sxs-lookup"><span data-stu-id="22b1c-148">Configure Human Resources parameters</span></span>](hr-setup-parameters.md)<br>
[<span data-ttu-id="22b1c-149">تكوين المعلمات المشتركة لـ Human Resources</span><span class="sxs-lookup"><span data-stu-id="22b1c-149">Configure Human Resources shared parameters</span></span>](hr-setup-shared-parameters.md)<br>
[<span data-ttu-id="22b1c-150">ما هو Microsoft Dataverse؟</span><span class="sxs-lookup"><span data-stu-id="22b1c-150">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="22b1c-151">استخدام  واجهة ويب Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="22b1c-151">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]