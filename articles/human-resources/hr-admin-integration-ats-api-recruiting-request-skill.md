---
title: المهارة في طلب التعيين
description: يصف هذا الموضوع كيان المهارة لطلب التعيين لـ Dynamics 365 Human Resources.
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
ms.openlocfilehash: 52dc7a839249ad8d55bb1f52cc5efe15cdf18e13
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059198"
---
# <a name="recruiting-request-skill"></a>المهارة في طلب التعيين

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا الموضوع كيان المهارة لطلب التعيين لـ Dynamics 365 Human Resources.

الاسم الفعلي: mshr_hcmrecruitingrequestskillentity

### <a name="description"></a>الوصف

وصف متطلبات المهارة لـ RecruitingRequest.

### <a name="json-representation"></a>تمثيل JSON

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_skillid": "String",
    "mshr_skilldescription": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_ratingleveldescription": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_skill_id_value": "Guid",
    "_mshr_fk_ratinglevel_id_value": "Guid",
    "_mshr_fk_ratingmodel_id_value": "Guid",
    "mshr_hcmrecruitingrequestskillentityid": "Guid"
}
```

### <a name="properties"></a>الخصائص

| الخاصية<br>**الاسم الفعلي**<br>**_النوع_** | استخدام | الوصف |
| --- | --- | --- |
| **معرف كيان المهارة في طلب التعيين**<br>mshr_hcmrecruitingrequestskillentityid<br>*GUID* | للقراءة فقط<br>مطلوب | معرف فريد منشأ بواسطة النظام لسجل **المهارة في طلب التعيين**. |
| **معرف طلب التعيين**<br>mshr_recruitingrequestid<br>*سلسلة* | الكتابة مرة واحدة<br>مطلوب | المعرف الفريد القابل للقراءة من قبل المستخدم لطلب التعيين المقترن. |
| **قيمة معرف طلب التعيين**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | للقراءة فقط<br>مطلوب<br> المفتاح الخارجي: mshr_hcmrecruitingrequestentityid لكيان mshr_hcmrecruitingrequestentity | المعرف الفريد المنشأ بواسطة النظام لطلب التعيين المقترن. |
| **معرف المهارة**<br>mshr_skillid<br>*سلسلة*<br> | الكتابة مرة واحدة<br>مطلوب | المعرف الفريد القابل للقراءة من قبل المستخدم للمهارة المطلوبة. |
| **قيمة معرف المهارة**<br>_mshr_fk_skill_id_value<br>*GUID* | للقراءة فقط<br>مطلوب<br>المفتاح الخارجي: mshr_hcmskillentityid للكيان mshr_hcmskillentity | معرف فريد منشأ بواسطة النظام للمهارة المطلوبة. |
| **معرف مستوى التقييم**<br>mshr_ratinglevelid<br>*سلسلة* | الكتابة مرة واحدة<br>اختياري | قيمة مستوى المهارة المطلوبة المحددة للوظيفة، استنادا إلى نموذج التقييم المعين للمهارة. |
| **قيم معرف مستوى التقييم**<br>_mshr_fk_ratinglevel_id_value<br>*GUID* | للقراءة فقط<br>اختياري<br>المفتاح الخارجي: mshr_hcmratinglevelentityid للكيان mshr_hcmratinglevelentity | معرف فريد منشأ بواسطة النظام للمستوى. |
| **وصف المهارة**<br>mshr_skilldescription<br>*سلسلة* | للقراءة فقط<br>مطلوب | وصف المهارة. |
| **وصف مستوى التقييم**<br>mshr_ratingleveldescription<br>*سلسلة* | للقراءة فقط<br>اختياري | صف مستوى المهارة المحدد. |
| **معرف منطقة البيانات**<br>mshr_dataareaid<br>*سلسلة* | قراءة/كتابة<br>اختياري | يحدد الكيان القانوني (الشركة). |
| **قيمة معرف منطقة البيانات**<br>_mshr_dataareaid_id_value<br>*GUID* | للقراءة فقط<br>اختياري<br>المفتاح الخارجي: cdm_companyid للكيان cdm_company | قيمة GUID تم إنشاؤها بواسطة النظام لتعرف الكيان القانوني (الشركة). |
| **الحقل الأساسي**<br>mshr_primaryfield<br>*سلسلة* | للقراءة فقط<br>مطلوب | سلسلة متصلة من قيمة طلب التعيين ومعرف المهارة كأسلوب آخر لتعريف السجل بشكل فريد. |
| **معرف نموذج التقييم**<br>mshr_ratingmodelid<br>*سلسلة* | قراءة-كتابة<br>مطلوب | نموذج التقييم المستخدم لتقييم المهارة. |
| **قيمة معرف نموذج التقييم**<br>_mshr_fk_hcmratingmodel_id_value<br>*GUID* | للقراءة فقط<br>مطلوب<br>المفتاح الخارجي: mshr_hcmratingmodelentityid للكيان mshr_hcmratingmodelentity | المعرف الفريد الذي تم إنشاؤه بواسطة النظام لنموذج التقييم المستخدم لتقييم المهارة. |

## <a name="see-also"></a>راجع أيضًا

[مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب](hr-admin-integration-ats-api-introduction.md)<br>
[مثال لاستعلام عن طلب تعيين](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]