---
title: الموظف حسب كشف الرواتب
description: يوفر هذا الموضوع تفاصيل ومثال استعلام لكيان موظف كشف الرواتب في Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 57501d07f6b9cffdff9f37737df8c278c574cf30
ms.sourcegitcommit: 89bb2a7f402deed32998eddc1e56e75250e3d15e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314275"
---
# <a name="payroll-employee"></a>الموظف حسب كشف الرواتب

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا الموضوع كيان الموظف في الرواتب لـ Dynamics 365 Human Resources.

الاسم الفعلي: mshr_payrollemployeeentity.

### <a name="description"></a>الوصف

يوفر هذا الكيان معلومات حول الموظف. يجب تعيين [معلمات تكامل الرواتب](hr-admin-integration-payroll-api-parameters.md) قبل استخدام هذا الكيان.

## <a name="properties"></a>الخصائص

| الخاصية<br>**الاسم الفعلي**<br>**_النوع_** | استخدام | الوصف |
| --- | --- | --- |
| **رقم الموظف**<br>mshr_personnelnumber<br>*سلسلة* | للقراءة فقط<br>مطلوب | رقم الموظف الفريد الخاص بالموظف. |
| **الحقل الأساسي**<br>mshr_primaryfield<br>*سلسلة* | مطلوب<br>النظام منشأ |  |
| **اسم العائلة**<br>mshr_lastname<br>*سلسلة* | للقراءة فقط<br>مطلوب | اسم العائلة للموظف. |
| **معرف الكيان القانوني**<br>mshr_legalentityID<br>*سلسلة* | للقراءة فقط<br>مطلوب | يحدد الكيان القانوني (الشركة). |
| **صالح من**<br>mshr_namevalidfrom<br>*الفرق بالتاريخ والوقت* | للقراءة فقط <br>مطلوب | تاريخ بدء صلاحية معلومات الموظف.  |
| **الجنس**<br>mshr_gender<br>[مجموعة خيارات mshr_hcmpersongender](hr-admin-integration-payroll-api-gender.md) | للقراءة فقط<br>مطلوب | جنس الموظف. |
| **معرف كيان موظف كشف الرواتب**<br>mshr_payrollemployeeentityid<br>*GUID* | مطلوب<br>النظام منشأ | قيمة معرف GUID منشأ بواسطة النظام لتعريف الموظف بشكل فريد. |
| **تاريخ بداية التوظيف**<br>mshr_employmentstartdate<br>*الفرق بالتاريخ والوقت* | للقراءة فقط<br>مطلوب | تاريخ بدء توظيف الموظف. |
| **معرف نوع التعريف**<br>mshr_identificationtypeid<br>*سلسلة* |للقراءة فقط<br>مطلوب | نوع التعريف المحدد للموظف. |
| **تاريخ انتهاء التوظيف**<br>mshr_employmentenddate<br>*الفرق بالتاريخ والوقت* | للقراءة فقط<br>مطلوب |تاريخ انتهاء توظيف الموظف.  |
| **معرف منطقة البيانات**<br>mshr_dataareaid_id<br>*GUID* | مطلوب <br>النظام منشأ | قيمة GUID تم إنشاؤها بواسطة النظام لتعرف الكيان القانوني (الشركة). |
| **صالح حتى**<br>mshr_namevalidto<br>*الفرق بالتاريخ والوقت* |  للقراءة فقط<br>مطلوب | تاريخ انتهاء صلاحية معلومات الموظف. |
| **تاريخ الميلاد**<br>mshr_birthdate<br>*الفرق بالتاريخ والوقت* | للقراءة فقط <br>مطلوب | تاريخ ميلاد الموظف. |
| **رقم التعريف**<br>mshr_identificationnumber<br>*سلسلة* | للقراءة فقط <br>مطلوب |رقم التعريف المحدد للموظف.  |
| **الاسم الأول**<br>mshr_firstname<br>*سلسلة* | للقراءة فقط<br>مطلوب | الاسم الأول للموظف. |
| **الاسم الأوسط**<br>mshr_middlename<br>*سلسلة* | للقراءة فقط<br>مطلوب |الاسم الأوسط للموظف.  |

## <a name="example-query-for-payroll-employee"></a>نموذج الاستعلام لموظف كشل الرواتب

**الطلب**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollemployeeentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_identificationtypeid eq @idtype and mshr_namevalidfrom le @asofdate and mshr_namevalidto ge @asofdate&@personnelnumber='000041'&@idtype='SSN'&@asofdate=2021-04-01
```

**استجابة**

```json
{
    "mshr_legalentityid": "USMF",
    "mshr_personnelnumber": "000041",
    "mshr_employmentstartdate": "2011-04-05T07:00:00Z",
    "mshr_employmentenddate": "2154-12-31T23:59:59Z",
    "mshr_firstname": "Cassie",
    "mshr_middlename": "Lassie",
    "mshr_lastname": "Hicks",
    "mshr_namevalidfrom": "2021-03-12T20:34:25Z",
    "mshr_namevalidto": "2154-12-31T23:59:59Z",
    "mshr_birthdate": "1987-09-12T00:00:00Z",
    "mshr_gender": 200000002,
    "mshr_identificationtypeid": "SSN",
    "mshr_identificationnumber": "888-99-9342",
    "mshr_dataareaid": "USMF",
    "mshr_primaryfield": "000041 | USMF | 4/5/2011 07:00:00 am",
    "_mshr_fk_worker_id_value": "000000ad-0000-0000-d5ff-004105000000",
    "_mshr_fk_employment_id_value": "00000d0d-0000-0000-0600-014105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
    "mshr_payrollemployeeentityid": "00000d3c-0000-0000-d5ff-004105000000",
    "_mshr_dataareaid_id_value": null
}
```
## <a name="see-also"></a>راجع أيضًا

[‏‫مقدمة إلى واجهة API لتكامل كشف الرواتب](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]