---
title: التعليم في طلب التعيين
description: يصف هذا الموضوع كيان التعليم في طلب التعيين لـ Dynamics 365 Human Resources.
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
ms.openlocfilehash: 9fe1a99debac3dc784ba82b711143337d4077be0
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067116"
---
# <a name="recruiting-request-education"></a>التعليم في طلب التعيين


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا الموضوع كيان التعليم في طلب التعيين لـ Dynamics 365 Human Resources.

الاسم الفعلي: mshr_hcmrecruitingrequesteducationentity

### <a name="description"></a>الوصف

وصف المتطلبات التعليمية لـ RecruitingRequest.

### <a name="json-representation"></a>تمثيل JSON

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_educationdisciplineid": "String",
    "mshr_educationdisciplinedescription": "String",
    "mshr_educationlevelid": "String",
    "mshr_educationleveldescription": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_educationdiscipline_id_value": "Guid",
    "_mshr_fk_educationlevel_id_value": "Guid",
    "mshr_hcmrecruitingrequesteducationentityid": "Guid"
}
```

### <a name="properties"></a>الخصائص

| الخاصية<br>**الاسم الفعلي**<br>**_النوع_** | استخدام | الوصف |
| --- | --- | --- |
| **معرف كيان التعليم في طلب التعيين**<br>mshr_hcmrecruitingrequesteducationentityid<br>*GUID* | للقراءة فقط<br>مطلوب | معرف فريد منشأ بواسطة النظام لسجل التعليم في طلب التعيين. |
| **معرف طلب التعيين**<br>mshr_recruitingrequestid<br>*سلسلة* | الكتابة مرة واحدة<br>مطلوب | المعرف الفريد القابل للقراءة من قبل المستخدم لطلب التعيين ذي الصلة. |
| **قيمة معرف طلب التعيين**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | للقراءة فقط<br>مطلوب<br>المفتاح الخارجي: mshr_hcmrecruitingrequestentityid لـ mshr_hcmrecruitingrequestentity | المعرف الفريد المنشأ بواسطة النظام لطلب التعيين ذي الصلة. |
| **معرف مستوى التعليم**<br>mshr_educationlevelid<br>*سلسلة* | الكتابة مرة واحدة<br>مطلوب | مستوى التعليم المطلوب. |
| **قيمة معرف المستوى التعليمي**<br>_mshr_fk_educationlevel_id_value<br>*GUID* | للقراءة فقط<br>مطلوب<br>المفتاح الخارجي: mshr_hcmeducationlevelentityid لـ mshr_hcmeducationlevelentity | معرف فريد منشأ بواسطة النظام لمستوى التعليم المطلوب. |
| **وصف مستوى التعليم**<br>mshr_educationleveldescription<br>*سلسلة* | للقراءة فقط<br>مطلوب | وصف المستوى المطلوب للمهارة. |
| **معرف النظام التعليمي**<br>mshr_educationdisciplinedescription<br>*سلسلة* | الكتابة مرة واحدة<br>مطلوب | منطقة النظام التعليمي. |
| **قيمة معرف النظام التعليمي**<br>_mshr_fk_educationdiscipline_id_value<br>*GUID* | للقراءة فقط<br>مطلوب<br>المفتاح الخارجي: mshr_hcmeducationdisciplineentityid of mshr_hcmeducationdisciplineentity | معرف فريد منشأ بواسطة النظام لمنطقة النظام التعليمي. |
| **وصف النظام التعليمي**<br>mshr_educationdisciplinedescription<br>سلسلة | للقراءة فقط<br>مطلوب | وصف المنطقة الخاصة بالنظام التعليمي. |
| **معرف منطقة البيانات**<br>mshr_dataareaid<br>*سلسلة* | قراءة/كتابة<br>اختياري | يحدد الكيان القانوني (الشركة).|
| **قيمة معرف منطقة البيانات**<br>_mshr_dataareaid_id_value<br>*GUID* | للقراءة فقط<br>اختياري<br>المفتاح الخارجي: cdm_companyid للكيان cdm_company | قيمة GUID تم إنشاؤها بواسطة النظام لتعرف الكيان القانوني (الشركة). |
| **الحقل الأساسي**<br>mshr_primaryfield<br>*سلسلة* | للقراءة فقط<br>مطلوب | سلسلة متصلة من قيمة طلب التعيين ومعرف مستوى التعليم ومعرف النظام التعليمي كأسلوب آخر لتعريف السجل بشكل فريد. |

## <a name="see-also"></a>راجع أيضًا

[مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب](hr-admin-integration-ats-api-introduction.md)<br>
[مثال لاستعلام عن طلب تعيين](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
