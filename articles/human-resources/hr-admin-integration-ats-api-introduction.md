---
title: مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب
description: يصف هذا الموضوع واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب (ATS) في Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c043ac9c19a810d1718f0d4907cd5e9d651d778f
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055282"
---
# <a name="applicant-tracking-system-integration-api-introduction"></a>مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا الموضوع واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب (ATS) في Dynamics 365 Human Resources. وهدف واجهة API هو تمكين عمليات التكامل الانسيابية بين أنظمة ATS في Dynamics 365 Human Resources وأنظمة الشركاء.

![سير عمل تكامل نظام ATS](media/hr-admin-integration-ats-api-introduction-flow.png)

تبدأ التجربة المتكاملة في الموارد البشرية عندما يقوم مدير التوظيف بإنشاء طلب توظيف. عند تنشيط الطلب، يقوم نظام ATS بسحب تفاصيل الطلب لإنشاء مشروع تعيين. وبعد ذلك يتبع مسار التوظيف لتحديد مرشح للمنصب (المناصب) وتوظيفه. وأخيرا، يكمل نظام ATS رحلة التكامل الكاملة عن طريق إرسال سجل المرشح المحدد إلى الموارد البشرية. يمكن أن يمر سجل الترشيح بعد ذلك بمزيد من عمليات التحقق من الصحة ومهام سير العمل لإنشاء سجل الموظف.

لتمكين التكامل، أضافت الموارد البشرية المكونات التالية:

1.  وظيفة لإنشاء طلب التوظيف.
2.  ملف تعريف مرشح والسير العمل المرتبط.
3.  تفتح واجهة API للتكامل الوظائف الجديدة لتكامل الطلبات.

لمزيد من المعلومات حول إعداد طلب التعيين ووظيفة المرشح واستخدامها، راجع [توظيف المرشحين لوظيفة](hr-personnel-recruit.md).

## <a name="microsoft-dataverse"></a>Microsoft Dataverse

تأتي واجهة API مدمجة في Microsoft Dataverse (المعروف سابقًا بـ Common Data Service). وتجري كافة أشكال تفاعل RESTful مع واجهة API هذه عن طريق واجهة ويب Microsoft Dataverse، التي تستخدم OData. تعد واجهة API هذه مجموعة فرعية من واجهة ويب Dataverse. تحدد واجهة ويب Dataverse خصائص مثل المصادقة واتفاقيات SLA و, الدفعة والتحكم في التزامن ومعالجة الأخطاء.

لمزيد من المعلومات عن واجهة ويب Microsoft Dataverse، راجع:

- [ما هو Microsoft Dataverse؟](/powerapps/maker/data-platform/data-platform-intro)
- [استخدام  واجهة ويب Microsoft Dataverse](/powerapps/developer/data-platform/webapi/overview)
- [دليل مطور Microsoft Dataverse](/powerapps/developer/data-platform)

تتضمن الوثائق الواردة أعلاه تفاصيل وإرشادات للمطور حول استخدام واجهة ويب Dataverse، مثل [إدارة المصادقة](/powerapps/developer/data-platform/webapi/authenticate-web-api)، و[تنفيذ العمليات](/powerapps/developer/data-platform/webapi/perform-operations-web-api)، و[استخدام Postman مع واجهة API](/powerapps/developer/data-platform/webapi/use-postman-web-api)، و[استخدام تعقب التغييرات أو رموز دلتا](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) مع واجهة API.

### <a name="option-sets"></a>مجموعات الخيارات

يتضمن نموذج البيانات لواجهة API لتكامل نظام ATS الموضح في هذا المستند مجموعات الخيارات التي توفر قيمًا عددية مقترنة بخصائص الوحدة. للحصول على تفاصيل حول العمل مع مجموعات الخيارات في واجهة ويب Dataverse، راجع [إنشاء وتحديث مجموعات الخيارات باستخدام واجهة الويب](/powerapps/developer/data-platform/webapi/create-update-optionsets). يتم تحديد مجموعات الخيارات لكل بيئة من بيئات Dataverse.

### <a name="virtual-tables-for-human-resources-in-dataverse"></a>الجداول الظاهرية للموارد البشرية في Dataverse

تستخدم نقاط النهاية لواجهات API لتكامل نظام ATS قدرات النظام الأساسي في الجدول الظاهري لـ Microsoft Dataverse. بشكل افتراضي، لا يتم نشر الجداول الظاهرية ونقاط نهاية واجهات API المقترنة بها لبيئات الموارد البشرية، مما يتيح للمؤسسات تحديد نقاط نهاية OData التي سيتم عرضها للبيئة. لاستخدام واجهة API، يجب إنشاء الجداول الظاهرية لكيانات الموارد البشرية للبيئة. 

للحصول على معلومات حول إنشاء الجداول الظاهرية لواجهة API، راجع [تكوين الجداول الظاهرية في Dataverse](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="data-model"></a>نموذج البيانات

يتم توسيط نموذج البيانات حول وحدتين رئيسيتين:

- يمثل **RecruitingRequest** طلبًا إلى ATS لتوظيف شخص لأحد المناصب المفتوحة أو أكثر. لمطالعة مثال استعلام، راجع [مثال استعلام طلب توظيف](hr-admin-integration-ats-api-recruiting-request-example-query.md).
- يمثل **CandidateToHire** تفاصيل المرشح الذي قبل العرض الخاص بالمنصب. يمثل **الشخص** الفرد الذي سيكو المرشح. يمكن أن يكون لأحد الأشخاص أدوار متعددة في الشركة، مثل المرشح أو العامل أو الموظف أو المقاول. للاطلاع على مثال للاستعلام ، راجع [مثال الاستعلام عن المرشح المراد توظيفه](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).

يوضح المخطط التالي العلاقات داخل API. تحتوي العديد من الأنواع على مفاتيح خارجية لكيانات أخرى موجودة مسبقا في الموارد البشرية لم يتم توضيحها هنا. يوفر هذا المستند معلومات حول الكيانات الخاصة بسيناريوهات تكامل التعيين. ومع ذلك، هناك العديد من الكيانات الأخرى في واجهة ويب Dataverse لـ Dynamics 365 Human Resources يمكن أن تكون مرتبطة أيضًا بالتكامل الخاص بك. على سبيل المثال، قد تحتاج أيضا إلى تفصيل العاملين أو الوظائف أو المناصب أو الكيانات الأخرى غير المحددة. تجري الاشارة إلى العديد من هذه الكيانات في علاقات المفاتيح الخارجية أو خصائص التنقل.

![نموذج بيانات واجهة API لتكامل ATS](media/hr-admin-integration-ats-api-data-model.png)

## <a name="recruiting-request-and-related-entities-and-option-sets"></a>طلب التعيين والكيانات ذات الصلة ومجموعات الخيارات

مثال الاستعلام: 

- [مثال لاستعلام عن طلب تعيين](hr-admin-integration-ats-api-recruiting-request-example-query.md)

الكيانات:

- [طلب التعيين](hr-admin-integration-ats-api-recruiting-request.md)
- [منصب طلب التعيين](hr-admin-integration-ats-api-recruiting-request-position.md)
- [المهارة في طلب التعيين](hr-admin-integration-ats-api-recruiting-request-skill.md)
- [التعليم في طلب التعيين](hr-admin-integration-ats-api-recruiting-request-education.md)
- [موقع طلب التعيين](hr-admin-integration-ats-api-recruiting-request-location.md)

مجموعات الخيارات:

- [حالة الإعفاء من الوظيفة](hr-admin-integration-ats-api-job-exempt-status.md)
- [حالة منصب طلب التعيين](hr-admin-integration-ats-api-recruiting-request-position-status.md)
- [حالة طلب التعيين](hr-admin-integration-ats-api-recruiting-request-status.md)
- [فئة الوظيفة التنظيمية](hr-admin-integration-ats-api-regulatory-job-category.md)

## <a name="candidate-to-hire-and-related-entities-and-option-sets"></a>المرشح المراد توظيفه والكيانات ذات الصلة ومجموعات الخيارات

مثال الاستعلام:

- [مثال الاستعلام عن مرشح مراد توظيفه](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

الكيانات:

- [المرشح المُراد توظيفه](hr-admin-integration-ats-api-candidate-to-hire.md)
- [الشخص](hr-admin-integration-ats-api-person.md)
- [تعليم الشخص](hr-admin-integration-ats-api-person-education.md)
- [الخبرة المهنية للشخص](hr-admin-integration-ats-api-person-professional-experience.md)
- [عنوان الشخص](hr-admin-integration-ats-api-person-address.md)
- [جهة اتصال الطرف](hr-admin-integration-ats-api-party-contact.md)
- [مهارة الشخص](hr-admin-integration-ats-api-person-skill.md)
- [مستوى التقييم](hr-admin-integration-ats-api-rating-level.md)
- [شهادة الشخص](hr-admin-integration-ats-api-person-certificate.md)
- [نوع الشهادة](hr-admin-integration-ats-api-certificate-type.md)
- [مراقبة الأشخاص](hr-admin-integration-ats-api-person-screening.md)
- [أنواع المراقبة](hr-admin-integration-ats-api-screening-types.md)
- [رقم الهوية للشخص](hr-admin-integration-ats-api-person-identification-number.md)

مجموعات الخيارات:

- [نتيجة تكامل مقدم الطلب](hr-admin-integration-ats-api-applicant-integration-result.md)
- [فارغ نعم لا](hr-admin-integration-ats-api-blank-yes-no.md)
- [حالة الإكمال](hr-admin-integration-ats-api-completion-status.md)
- [نوع جهة الاتصال](hr-admin-integration-ats-api-contact-type.md)
- [أساس الائتمان التعليمي](hr-admin-integration-ats-api-education-credit-basis.md)
- [الجنس](hr-admin-integration-ats-api-gender.md)
- [الحالة الاجتماعية](hr-admin-integration-ats-api-marital-status.md)
- [شهور السنة](hr-admin-integration-ats-api-months-of-year.md)
- [لا     نعم](hr-admin-integration-ats-api-no-yes.md)
- [وحدة الفترة](hr-admin-integration-ats-api-period-unit.md)
- [تكرار المراقبة](hr-admin-integration-ats-api-screening-frequency.md)
- [إنشاء تكرار المراقبة من](hr-admin-integration-ats-api-screening-frequency-generate-from.md)
- [نوع مستوى المهارة](hr-admin-integration-ats-api-skill-level-type.md)

## <a name="see-also"></a>راجع أيضًا

[تعيين المرشحين للوظائف](hr-personnel-recruit.md)<br>
[ما هو Microsoft Dataverse؟](/powerapps/maker/data-platform/data-platform-intro)<br>
[استخدام  واجهة ويب Microsoft Dataverse](/powerapps/developer/data-platform/webapi/overview)<br>
[إنشاء مجموعات الخيارات وتحديثها باستخدام واجهة الويب](/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]