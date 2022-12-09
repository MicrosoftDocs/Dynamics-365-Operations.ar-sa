---
title: طلب التوظيف
description: توضح هذه المقالة كيان طلب التوظيف لـ Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d89d3e77d096f5908207ac53f4e9022f686ac5f3
ms.sourcegitcommit: 5f8f042f3f7c3aee1a7303652ea66e40d34216e3
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806365"
---
# <a name="recruiting-request"></a>طلب التوظيف


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

توضح هذه المقالة كيان طلب التوظيف لـ Dynamics 365 Human Resources.

الاسم الفعلي: mshr_hcmrecruitingrequestentity

### <a name="description"></a>الوصف

يصف طلبًا للتعيين لوظيفة.

### <a name="json-representation"></a>تمثيل JSON

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_hiringmanagerpersonnelnumber": "String",
    "mshr_recruiterpartynumber": "String",
    "mshr_status": Int,
    "mshr_description": "String",
    "mshr_recruitingrequestlocationid": "String",
    "mshr_comments": "String",
    "mshr_jobid": "String",
    "mshr_titleid": "String",
    "mshr_jobfunctionid": "String",
    "mshr_defaultfulltimeequivalency": Decimal,
    "mshr_regulatoryjobcategory": Int,
    "mshr_jobtypeid": "String",
    "mshr_exemptstatus": Int,
    "mshr_estimatedstartdate": "Date",
    "mshr_externaldescription": "String",
    "mshr_compensationlevelid": "String",
    "mshr_compensationlowthreshold": Decimal,
    "mshr_compensationcontrolpoint": Decimal,
    "mshr_compensationhighthreshold": Decimal,
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "_mshr_fk_hiringmanager_id_value": "Guid",
    "_mshr_fk_recruiter_id_value": "Guid",
    "_mshr_fk_job_id_value": "Guid",
    "_mshr_fk_title_id_value": "Guid",
    "_mshr_fk_jobtype_id_value": "Guid",
    "_mshr_fk_compensationlevel_id_value": "Guid",
    "mshr_hcmrecruitingrequestentityid": "Guid",
    "_mshr_fk_recruitingrequestlocation_id_value": "Guid"
}
```

### <a name="properties"></a>الخصائص

| الخاصية<br>**الاسم الفعلي**<br>**_النوع_** | استخدام | الوصف |
| --- | --- | --- |
| **معرف طلب التعيين**<br>mshr_recruitingrequestid<br>*سلسلة* | للقراءة فقط<br>مطلوب<br>منشأ بواسطة النظام | معرف فريد يمكن قراءته بواسطة المستخدم للطلب المعروض في تطبيق الموارد البشرية. التسلسل الرقمي. |
| **معرف كيان طلب التعيين**<br>mshr_hcmrecruitingrequestentityid<br>*GUID* | للقراءة فقط<br>مطلوب<br>منشأ بواسطة النظام | قيمة معرف GUID منشأ بواسطة النظام لتعريف طلب التعيين بشكل فريد. |
| **معرف منطقة البيانات**<br>mshr_dataareaid<br>*سلسلة* | قراءة/كتابة<br>اختياري<br> | يحدد الكيان القانوني (الشركة) الخاصة بطلب التعيين. |
| **قيمة معرف منطقة البيانات**<br>_mshr_dataareaid_id_value<br>*GUID*<br> | للقراءة فقط<br>اختياري<br>المفتاح الخارجي: cdm_companyid للكيان cdm_company | قيمة GUID منشأة بواسطة النظام لتعرف الكيان القانوني (الشركة) لطلب التعيين. |
| **رقم الموظف لمدير التوظيف**<br>mshr_hiringmanagerpersonnelnumber<br>*سلسلة* | قراءة/كتابة<br>اختياري | رقم الموظف الخاص بمدير التوظيف المقترن بطلب التعيين هذا. |
| **قيمة معرف مدير التوظيف**<br>_mshr_fk_hiringmanager_id_value<br>*GUID* | للقراءة فقط<br>اختياري<br>المفتاح الخارجي mshr_hcmworkerbaseentityid للكيان mshr_hcmworkerbaseentity | قيمة معرف GUID منشأة بواسطة النظام لتحديد المدير المقترن بطلب التعيين. |
| **رقم الطرف لمسؤول التعيين‬**<br>mshr_recruiterpartynumber<br>*سلسلة* | قراءة/كتابة<br>اختياري | رقم معرف الطرف (الشخص) لمسؤول التعيين المحدد للطلب. |
| **قيمة معرف مسؤول التعيين**<br>_mshr_fk_recruiter_id_value<br>*GUID* | للقراءة فقط<br>اختياري<br>المفتاح الخارجي: mshr_dirpersonentityid للكيان mshr_dirpersonentity | قيمة معرف GUID منشأة بواسطة النظام لتحديد مسؤول التعيين المقترن بطلب التعيين. |
| **الحالة**<br>mshr_status<br>مجموعة خيارات *RecruitingRequestStatus* | قراءة/كتابة<br>مطلوب<br> | يشير إلى حالة طلب التعيين. |
| **‏‏الوصف**<br>mshr_description<br>*سلسلة* | قراءة/كتابة<br>مطلوب | وصف الطلب. |
| **معرف موقع طلب التعيين**<br>mshr_recruitingrequestlocationid<br>*سلسلة* | قراءة/كتابة<br>اختياري | المعرف الفريد القابل للقراءة من قبل المستخدم لموقع الوظيفة المقترن بهذا الطلب. |
| **قيمة معرف موقع التعيين**<br>_mshr_fk_recruitingrequestlocation_id_value<br>*GUID* | للقراءة فقط<br>اختياري<br>المفتاح الخارجي: mshr_hcmrecruitingrequestlocationentityid للكيان mshr_hcmrecruitingrequestlocationentity | قيمة معرف GUID منشأة بواسطة النظام لتحديد موقع طلب التعيين المحدد للطلب. |
| **التعليقات**<br>mshr_comments<br>*سلسلة* | قراءة/كتابة<br>اختياري | تعليقات حول الطلب للاستخدام من قِبل مديري التوظيف ومسؤولي التوظيف. |
| **معرف الوظيفة**<br>mshr_jobid<br>*سلسلة* | الكتابة مرة واحدة<br>مطلوب |   المعرف الفريد القابل للقراءة من قبل المستخدم للوظيفة التي تشاركها جميع المناصب المقترنة بهذا الطلب. |
| **قيمة معرف الوظيفة**<br>_mshr_fk_job_id_value<br>*GUID* | للقراءة فقط<br>مطلوب<br>المفتاح الخارجي: mshr_hcmjobentityid للكيان mshr_hcmjobentity | المعرف الفريد المنشأة بواسطة النظام للوظيفة التي تشاركها جميع المناصب المقترنة بطلب التعيين. |
| **معرف العنوان**<br>mshr_titleid<br>*سلسلة* | للقراءة فقط<br>مطلوب | المعرف الفريد القابل للقراءة من قبل المستخدم لعنوان الوظيفة المقترن بهذا الطلب. |
| **قيمة معرف العنوان**<br>_mshr_fk_title_id_value<br>*GUID* | للقراءة فقط<br>مطلوب<br>المفتاح الخارجي: mshr_hcmtitleid للكيان mshr_hcmtitleentity | المعرف الفريد المنشأ بواسطة النظام لعنوان الوظيفة المحدد لطلب التوظيف. |
| **معرف مهمة الوظيفة**<br>mshr_jobfunctionid<br>*سلسلة* | للقراءة فقط<br>مطلوب<br>المفتاح الخارجي: mshr_jobfunctionid للكيان mshr_hcmjobfunctionentity | المعرف الفريد القابل للقراءة من قبل المستخدم لمهمة الوظيفة المقترنة بهذا الطلب. |
| **مكافئ الدوام الكامل الافتراضي**<br>mshr_defaultfulltimeequivalency<br>*مزدوج* | للقراءة فقط<br>مطلوب | قيمة مكافئ الدوام الكامل للوظيفة، حيث تمثل 1.0 عامل بدوام كامل. |
| **فئة الوظيفة التنظيمية**<br>mshr_regulatoryjobcategory<br>مجموعة خيارات *RegulatoryJobCategory* | للقراءة فقط<br>اختياري | فئة وظيفة EEO لمهمة الوظيفة المحددة للوظيفة. القيم الصالحة المضمنة في مجموعة خيارات HcmRegulatoryJobCatetory (mshr_hcmregulatoryjobcategory). |
| **معرف نوع الوظيفة**<br>mshr_jobtypeid<br>*سلسلة* | للقراءة فقط<br>اختياري | نوع الوظيفة المقترنة بالمنصب. أنواع الوظائف هي عبارة عن قيم معرفة بواسطة المستخدم، متوفرة في الكيان mshr_hcmjobtypeentity. |
| **قيمة معرف نوع الوظيفة**<br>_mshr_fk_jobtype_id_value<br>*GUID* | للقراءة فقط<br>اختياري<br>المفتاح الخارجي: mshr_hcmjobtypeentityid للكيان mshr_hcmjobtypenentity | المعرف الفريد المنشأة بواسطة النظام لنوع الوظيفة المقترن بالوظيفة لطلب التعيين. |
| **حالة الإعفاء**<br>mshr_exemptstatus<br>مجموعة خيارات *JobExemptStatus* | للقراءة فقط<br>اختياري | حالة إعفاء FLSA استنادًا إلى نوع الوظيفة. |
| **تاريخ البدء التقديري**<br>mshr_estimatedstartdate<br>*التاريخ* | قراءة/كتابة<br>مطلوب | التاريخ المقدر الذي يبدأ فيه المرشح في العمل. |
| **وصف خارجي**<br>mshr_externaldescription<br>*سلسلة* | قراءة/كتابة<br>اختياري | وصف موجه للمرشح للوظيفة/المنصب. | 
| **الحد الأدنى للتعويض**<br>mshr_compensationlowthreshold<br>*مزدوج* | قراءة/كتابة<br>اختياري | الحد الأدنى لمستوى التعويض. |
| **نقطة تحكم التعويض**<br>mshr_compensationcontrolpoint<br>*مزدوج* | قراءة/كتابة<br>اختياري | نقطة التحكم الخاصة بمستوى التعويض. |
| **الحد الأعلى للتعويض**<br>mshr_compensationhighthreshold<br>*مزدوج* | قراءة/كتابة<br>اختياري | الحد الأعلى لمستوى التعويض. |
| **مستوى التعويض**<br>mshr_compensationlevelid<br>*سلسلة* | قراءة/كتابة<br>اختياري | مستوى التعويض للوظيفة. يمكن إعداد وظيفة بمستويات تعويض متعددة. تشير هذه السمة إلى مستوى تعويض الوظيفة المحدد لهذا الطلب. |
| **معرف التعويض للوظيفة**<br>_mshr_fk_jobcompensation_id_value<br>*GUID* | للقراءة فقط<br>اختياري<br>المفتاح الخارجي: mshr_hcmjobcompensationentityid للكيان mshr_hcmjobcompensationentity | المعرف الفريد المنشأة بواسطة النظام لمستوى التعويض المقترن بالوظيفة لطلب التعيين. |

## <a name="see-also"></a>راجع أيضًا

[مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب](hr-admin-integration-ats-api-introduction.md)<br>
[مثال لاستعلام عن طلب تعيين](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
