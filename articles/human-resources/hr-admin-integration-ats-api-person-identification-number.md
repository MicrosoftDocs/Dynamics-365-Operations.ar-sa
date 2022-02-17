---
title: رقم الهوية للشخص
description: يصف هذا الموضوع كيان رقم الهوية للشخص في Dynamics 365 Human Resources.
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
ms.openlocfilehash: 0991f5b2e17e64e23f78b346c451f7c43bc20378
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067141"
---
# <a name="person-identification-number"></a>رقم الهوية للشخص


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا الموضوع كيان رقم الهوية للشخص في Dynamics 365 Human Resources.

الاسم الفعلي: mshr_hcmpersonidentificationnumberentity

## <a name="description"></a>الوصف

يصف هذا الكيان أرقام الهوية للمرشحين. وهي تتيح لمستخدم واجهة API كتابة أرقام الهوية، مثل أرقام التأمين الاجتماعي وأرقام جوازات السفر في سجل المرشح. تظهر أرقام الهوية في سجل العامل، ولكن ليس على سجل المرشح. يمكن للتطبيق المتكامل كتابه القيم إلى قاعدة بيانات الموارد البشرية، لكن لن تكون الأرقام مرئية في الموارد البشرية حتى يتم إنشاء سجل العامل الخاص بالمرشح.

## <a name="json-representation"></a>تمثيل JSON

```json
{
    "mshr_entrytype": "String",
    "mshr_description": "String",
    "mshr_expirationdate": "Datetime",
    "mshr_isprimary": Int,
    "mshr_identificationnumber": "String",
    "mshr_partynumber": "String",
    "mshr_identificationtypeid": "String",
    "mshr_issuingagencyid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_issuingagency_id_value": "Guid",
    "_mshr_fk_identificationtype_id_value": "Guid",
    "mshr_hcmpersonidentificationnumberentityid": "Guid",
    "mshr_issueddate": "Datetime"
}
```

## <a name="properties"></a>الخصائص

| الخاصية<br>**الاسم الفعلي**<br>**_النوع_** | استخدام | الوصف |
| --- | --- | --- |
| **معرف كيان رقم هوية الشخص**<br>mshr_hcmpersonidentificationnumberentityid<br>*GUID* | للقراءة فقط<br>مطلوب<br>منشأ بواسطة النظام | المعرف الأساسي الفريد لسجل رقم هوية الشخص. |
| **نوع الإدخال**<br>mshr_entrytype<br>*سلسلة* | قراءة-كتابة<br>اختياري | قيمة حرة للإشارة إلى نوع الإدخال الخاص برقم الهوية. |
| **‏‏الوصف**<br>mshr_description<br>*سلسلة* | قراءة-كتابة<br>اختياري | وصف رقم الهوية. |
| **تاريخ انتهاء الصلاحية**<br>mshr_expirationdate<br>*Datetime* | قراءة-كتابة<br>اختياري | التاريخ الذي تنتهي فيه صلاحية رقم الهوية أو المستند المقترن. |
| **رئيسي**<br>mshr_isprimary<br>*مجموعة خيارات mshr_noyes* | قراءة-كتابة<br>اختياري | يتيح تحديد ما إذا كان رقم الهوية هو السجل الرئيسي للشخص لنوع الهوية هذا. |
| **رقم الهوية**<br>mshr_identificationnumber<br>*سلسلة* | قراءة-كتابة<br>مطلوب | رقم الهوية. |
| **رقم الطرف**<br>mshr_partynumber<br>*سلسلة* | قراءة-كتابة<br>مطلوب | معرف الطرف (الشخص) الذي يمتلك رقم الهوية. |
| **قيمة معرف الشخص**<br>_mshr_fk_person_id_value<br>*GUID* | للقراءة فقط<br>مطلوب<br>المفتاح الخارجي: mshr_dirpersonentityid للكيان mshr_dirpersonentity | المعرف الفريد للطرف (الشخص). |
| **معرف نوع الهوية**<br>mshr_identificationtypeid<br>*سلسلة* | قراءة-كتابة<br>مطلوب | نوع رقم الهوية. |
| **قيمة معرف نوع الهوية**<br>_mshr_fk_identificationtype_id_value<br>*GUID* | للقراءة فقط<br>مطلوب<br>المفتاح الخارجي: mshr_hcmidentificationtypeentityid لكيان mshr_hcmidentificationtypeentity | المعرف الفريد المنشأ بواسطة النظام لنوع الهوية. |
| **معرف جهة الإصدار**<br>mshr_issuingagencyid<br>*سلسلة* | قراءة-كتابة<br>اختياري | الوكالة أو المؤسسة التي تصدر رقم الهوية. |
| **قيمة معرف جهة الإصدار**<br>_mshr_fk_issuingagency_id_value<br>*GUID* | للقراءة فقط<br>اختياري<br>المفتاح الخارجي: mshr_hcmissuingagencyentityid لكيان mshr_hcmissuingagencyentity | المعرف الفريد المنشأ بواسطة النظام لجهة إصدار رقم الهوية. |
| **الحقل الأساسي**<br>mshr_primaryfield<br>*سلسلة* | للقراءة فقط<br>مطلوب | حقل المطلوب استخدامه كمعرف لسجل الكيان. مجموعة رقم الطرف ومعرف نوع الهوية ونوع الهوية. |
| **تاريخ الإصدار**<br>mshr_issuedate<br>*التاريخ* | قراءة-كتابة<br>اختياري | التاريخ الذي تم فيه إصدار رقم الهوية. |

## <a name="see-also"></a>راجع أيضًا

[مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب](hr-admin-integration-ats-api-introduction.md)<br>
[مثال الاستعلام عن مرشح مراد توظيفه](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
