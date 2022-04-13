---
title: ‏‫مقدمة إلى واجهة API لتكامل كشف الرواتب
description: يصف هذا الموضوع واجهة API لتكامل كشف الرواتب في  Dynamics 365 Human Resources.
author: twheeloc
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3743561e3ea3c798c37d71d851eb6b197c8d1c41
ms.sourcegitcommit: d67f7edaf1a50077c2a7dd105e774f86fc586495
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2022
ms.locfileid: "8533815"
---
# <a name="payroll-integration-api-introduction"></a>‏‫مقدمة إلى واجهة API لتكامل كشف الرواتب


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا المستند واجهة API لتكامل كشف الرواتب في  Dynamics 365 Human Resources. تمكّن واجهة API عمليات التكامل الشاملة الانسيابية بين Human Resources وأنظمة كشف الرواتب الشريكة. تبدأ التجربة المتكاملة في Human Resources مع معلومات عن ملف تعريف الموظف والراتب والخصم ومعلومات المساهمة. عند توظيف أحد الموظفين وإدخال معلومات الدفع وملف التعريف المطلوبة في Human Resources، يسحب نظام كشف الرواتب هذه المعلومات لاستخدامها عند معالجة كشف الرواتب. ويتم أيضًا سحب التحديثات التي تتم على معلومات الموظف أو الدفع لاستخداما في عمليات تشغيل الدفع اللاحقة.

[![‏‫سير مهام تكامل كشف الرواتب.](media/hr-admin-integration-payroll-api-introduction-flow.png)](media/hr-admin-integration-payroll-api-introduction-flow-2.png#lightbox)

لتمكين التكامل، تتضمن Human Resources المكونات التالية:

- [وظيفة لوضع علامة على الموظف كجاهز للدفع.](hr-compensation-payroll.md)
- تفتح واجهة API للتكامل الوظائف الجديدة لتكامل الطلبات.

## <a name="microsoft-dataverse"></a>Microsoft Dataverse

تأتي واجهة API مدمجة في Microsoft Dataverse (المعروف سابقًا بـ Common Data Service). وتجري كافة أشكال تفاعل RESTful مع واجهة API هذه عن طريق واجهة ويب Microsoft Dataverse، التي تستخدم OData. تعد واجهة API هذه مجموعة فرعية من واجهة ويب Dataverse. تحدد واجهة ويب Dataverse خصائص مثل المصادقة واتفاقيات SLA و, الدفعة والتحكم في التزامن ومعالجة الأخطاء.

لمزيد من المعلومات عن واجهة ويب Microsoft Dataverse، راجع:

- [ما هو Microsoft Dataverse؟](/powerapps/maker/data-platform/data-platform-intro)
- [استخدام واجهة ويب Microsoft Dataverse](/powerapps/developer/data-platform/webapi/overview)
- [دليل مطور Microsoft Dataverse](/powerapps/developer/data-platform)

تتضمن هذه الوثائق تفاصيل وإرشادات للمطور تتعلق باستخدام واجهة API الويب في Dataverse، بما في ذلك الموضوعات التالية:

- [المصادقة مع Microsoft Dataverse باستخدام واجهة API‎ الويب](/powerapps/developer/data-platform/webapi/authenticate-web-api)
- [تنفيذ عمليات باستخدام واجهة API‎ الويب](/powerapps/developer/data-platform/webapi/perform-operations-web-api)
- [استخدام Postman مع واجهة API‎ الويب](/powerapps/developer/data-platform/webapi/use-postman-web-api)
- [استخدام تعقب التغييرات لمزامنة البيانات مع الأنظمة الخارجية](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)

### <a name="virtual-tables-for-human-resources-in-dataverse"></a>الجداول الظاهرية للموارد البشرية في Dataverse

تستخدم نقاط النهاية لواجهة API لتكامل كشف الرواتب قدرات النظام الأساسي للجداول الظاهرية فيـ Microsoft Dataverse. بشكل افتراضي، لا يتم نشر الجداول الظاهرية ونقاط نهاية واجهات API المقترنة بها لبيئات Human Resources، مما يتيح للمؤسسات تحديد نقاط نهاية OData التي سيتم عرضها للبيئة. لاستخدام واجهة API، يجب إنشاء الجداول الظاهرية لكيانات الموارد البشرية للبيئة.

للحصول على معلومات حول إنشاء الجداول الظاهرية لواجهة API، راجع [تكوين الجداول الظاهرية في Dataverse](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="data-model"></a>نموذج البيانات

يوضح المخطط التالي العلاقات داخل API. تحتوي العديد من الأنواع على مفاتيح خارجية لكيانات أخرى موجودة مسبقا في الموارد البشرية لم يتم توضيحها هنا. يوفر هذا المستند معلومات حول الكيانات الخاصة بسيناريوهات تكامل كشف الرواتب. ومع ذلك، هناك العديد من الكيانات الأخرى في واجهة API الويب في Dataverse لـ Human Resources التي قد تكون أيضًا ذات صلة بعملية التكامل. يُشار إلى بعض هذه الكيانات في علاقات المفاتيح الخارجية أو خصائص التنقل.

[![نموذج بيانات واجهة API لتكامل كشف الرواتب.](media/hr-admin-payroll-api-data-model.png)](media/hr-admin-payroll-api-data-model.png#lightbox)

## <a name="payroll-employee-and-related-entities"></a>موظف كشف الرواتب والكيانات ذات الصلة

الكيانات:

- [الموظف حسب كشف الرواتب](hr-admin-integration-payroll-api-payroll-employee.md)
- [عنوان عامل كشف الرواتب](hr-admin-integration-payroll-api-payroll-worker-address.md)
- [خطة التعويض الثابتة لكشف الرواتب](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md)
- [خطة التعويض المتغير لكشف الرواتب](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md)
- [وظيفة منصب كشف الرواتب](hr-admin-integration-payroll-api-payroll-position-job.md)
- [منصب كشف الرواتب](hr-admin-integration-payroll-api-payroll-position.md)

## <a name="see-also"></a>راجع أيضًا

[إنشاء كيانات كشف الرواتب ومراجعتها](hr-admin-integration-payroll-api-generate-review-entities.md)<br>
[تكوين معلمات Human Resources](hr-setup-parameters.md)<br>
[تكوين المعلمات المشتركة لـ Human Resources](hr-setup-shared-parameters.md)<br>
[ما هو Microsoft Dataverse؟](/powerapps/maker/data-platform/data-platform-intro)<br>
[استخدام واجهة ويب Microsoft Dataverse](/powerapps/developer/data-platform/webapi/overview)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
