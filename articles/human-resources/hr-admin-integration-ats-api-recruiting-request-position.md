---
title: منصب طلب التعيين
description: يصف هذا الموضوع كيان المنصب لطلب التعيين لـ Dynamics 365 Human Resources.
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
ms.openlocfilehash: a709b8fb2f22c0e7a81399349cacbcfbfc91c8b2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059246"
---
# <a name="recruiting-request-position"></a>منصب طلب التعيين

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا الموضوع كيان المنصب لطلب التعيين لـ Dynamics 365 Human Resources.

الاسم الفعلي: mshr_hcmrecruitingrequestpositionentity

### <a name="description"></a>الوصف

يصف المنصب أو المناصب المراد تعبئتها لطلب التعيين. تعد إضافة منصب إلى طلب التعيين أمرا اختياريا. وتكون خصائص المنصب للقراءة فقط، حيث لا يجب أن تختلف خصائص المنصب في طلب التعيين عن السجل الرئيسي للمنصب. وإذا كانت الخصائص تحتاج إلى التغيير، فيجب القيام بذلك في السجل الرئيسي للمنصب قبل إضافة المنصب إلى طلب التعيين.

### <a name="json-representation"></a>تمثيل JSON
```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_positionid": "String",
    "mshr_description": "String",
    "mshr_positiontypeid": "String",
    "mshr_status": Int,
    "mshr_departmentnumber": "String",
    "mshr_reportstopositionid": "String",
    "mshr_reportstopersonnelnumber": "String",
    "mshr_financialdimension": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_position_id_value": "Guid",
    "_mshr_fk_positiontype_id_value": "Guid",
    "_mshr_fk_department_id_value": "Guid",
    "_mshr_fk_reportstoposition_id_value": "Guid",
    "_mshr_fk_reportstoworker_id_value": "Guid",
    "mshr_hcmrecruitingrequestpositionentityid": "Guid"
}
```

### <a name="properties"></a>الخصائص

| الخاصية<br>**الاسم الفعلي**<br>**_النوع_** | استخدام | الوصف |
| --- | --- | --- |
| **معرف كيان المنصب لطلب التعيين**<br>mshr_hcmrecruitingrequestpositionentityid<br>*GUID* | للقراءة فقط<br>مطلوب |    المعرف الفريد المنشأ بواسطة النظام لسجل منصب طلب التعيين. |
| **معرف طلب التعيين**<br>mshr_recruitingrequestid<br>*سلسلة* | الكتابة مرة واحدة<br>مطلوب | المعرف الفريد القابل للقراءة من قبل المستخدم لطلب التعيين. |
| **قيمة معرف طلب التعيين**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | للقراءة فقط<br>مطلوب<br>المفتاح الخارجي: mshr_hcmrecruitingrequestentityid لكيان mshr_hcmrecruitingrequestentity | المعرف الفريد المنشأ بواسطة النظام لطلب التعيين الذي سيتم تعيين المنصب له. |
| **معرف المنصب**<br>mshr_positionid<br>*سلسلة* | الكتابة مرة واحدة<br>مطلوب | المعرف الفريد القابل للقراءة من قبل المستخدم للمنصب. |
| **قيمة معرف المنصب**<br>_mshr_fk_position_id_value<br>*GUID* | للقراءة فقط<br>مطلوب<br>المفتاح الخارجي: mshr_hcmpositionv2entityid لكيان mshr_hcmpositionv2entity | المعرف الذي تم إنشاؤه بواسطة النظام للمنصب. |
| **‏‏الوصف**<br>mshr_description<br>*سلسلة* | للقراءة فقط<br>مطلوب | وصف المنصب. |
| **معرف نوع المنصب**<br>mshr_positiontypeid<br>*سلسلة* | للقراءة فقط<br>اختياري | المعرف الفريد القابل للقراءة من قبل المستخدم لنوع هذا المنصب. |
| **قيمة معرف نوع المنصب**<br>_mshr_fk_positiontype_id_value<br>*GUID* | للقراءة فقط<br>اختياري<br>المفتاح الخارجي: mshr_hcmpositiontypeentityid لكيان mshr_hcmpositiontypeentity | المعرف الفريد المنشأ بواسطة النظام لنوع هذا المنصب. |
| **الحالة**<br>mshr_status<br>مجموعة خيارات *RecruitingRequestPositionStatus* | قراءة/كتابة<br>مطلوب | حاله المنصب لطلب التعيين. |
| **رقم القسم**<br>mshr_departmentnumber<br>*سلسلة* | للقراءة فقط<br>اختياري<br> | رقم القسم للمنصب. |
| **قيمة معرف القسم**<br>_mshr_fk_department_id_value<br>*GUID* | للقراءة فقط<br>اختياري<br>المفتاح الخارجي: mshr_omdepartmententityid لكيان mshr_omdepartmententity | المعرف الفريد المنشأ بواسطة النظام للقسم الخاص بالمنصب. |
| **معرف منصب المدير المباشر**<br>mshr_reportstopositionid<br>*سلسلة* | للقراءة فقط<br>مطلوب | معرف قابلة للقراءة بواسطة المستخدم للمنصب الذي يتبعه المنصب الجاري تعيينه في التدرج الهرمي للمؤسسة. |
| **قيمة معرف منصب المدير المباشر**<br>_mshr_fk_reportstoposition_id_value<br>*GUID* | للقراءة فقط<br>مطلوب<br>المفتاح الخارجي: mshr_hcmpositionv2entityid لكيان mshr_hcmpositionv2entity | المعرف المنشأ بواسطة النظام للمنصب الذي يتبعه المنصب الجاري تعيينه. |
| **رقم موظف المدير المباشر**<br>mshr_reportstopersonnelnumber<br>*سلسلة* | للقراءة فقط<br>مطلوب | معرف العامل للعامل الذي سيتبعه المرشح الذي تم تعيينه. |
| **قيمة معرف العامل للمدير المباشر**<br>_mshr_fk_reportstoworker_id_value<br>*GUID* | للقراءة فقط<br>مطلوب<br>المفتاح الخارجي mshr_hcmworkerbaseentityid للكيان mshr_hcmworkerbaseentity | معرف منشأ بواسطة النظام للعامل الذي سيتبعه المرشح الذي تم تعيينه. |
| **البعد المالي**<br>mshr_financialdimension<br>*سلسلة* | للقراءة فقط<br>اختياري | البعد المالي (على سبيل المثال، مركز التكلفة) المخصص للمنصب. يتم تعيين البعد المالي لكل منصب لكل كيان قانوني. يمكن الوصول إلى مراكز التكلفة المحددة في الأبعاد من خلال كيان mshr_dimattributeomcostcenterentity. |
| **معرف منطقة البيانات**<br>mshr_dataareaid<br>*سلسلة* | قراءة/كتابة<br>اختياري | يحدد الكيان القانوني (الشركة) الخاصة بمنصب طلب التعيين. |
| **قيمة معرف منطقة البيانات**<br>_mshr_dataareaid_id_value<br>*GUID* | للقراءة فقط<br>اختياري<br>المفتاح الخارجي: cdm_companyid للكيان cdm_company | قيمة GUID منشأة بواسطة النظام لتعرف الكيان القانوني (الشركة) لمنصب طلب التعيين. |
| **الحقل الأساسي**<br>mshr_primaryfield<br>*سلسلة* | للقراءة فقط<br>مطلوب | سلسلة متصلة من قيمة طلب التعيين ومعرف المنصب كأسلوب آخر لتعريف السجل بشكل فريد. |

## <a name="see-also"></a>راجع أيضًا

[مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب](hr-admin-integration-ats-api-introduction.md)<br>
[مثال لاستعلام عن طلب تعيين](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]