---
title: سجل اسم الشخص
description: يوفر هذا الموضوع تفاصيل ومثال استعلام لكيان محفوظات أسماء الأشخاص في Dynamics 365 Human Resources.
author: marcelbf
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d87803b6ae0ada3ed2de6e4e7da5ffa57bf22eec
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/31/2022
ms.locfileid: "8064831"
---
# <a name="person-name-history"></a>سجل اسم الشخص


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا الموضوع كيان محفوظات أسماء الأشخاص في Dynamics 365 Human Resources.

الاسم الفعلي: mshr_dirpersonnamehistoricalentity.

### <a name="description"></a>‏‏الوصف

يوفر هذا الكيان معلومات حول محفوظات الأسماء لشخص معين.

> [!IMPORTANT] 
> لم تعد الحقول **FirstName**، و **MiddleName**، و **LastName**، و **NameValidFrom**، و **NameValidTo** متوفرة على كيان موظف كشف الرواتب‬‏‫. وقد تمت إزالتها للتأكد من وجود مصدر بيانات واحد فقط لتاريخ السريان يدعم هذا الكيان.

## <a name="properties"></a>الخصائص

| الخاصية</br>**الاسم الفعلي**</br>**_النوع_** | استخدام | ‏‏الوصف |
| --- | --- | --- |
| **الاسم الأول**</br>mshr_firstname</br>*سلسلة* | للقراءة فقط | الاسم الأول. |
| **بادئة اسم العائلة**</br>mshr_lastnameprefix</br>*سلسلة*) | للقراءة فقط | بادئة اسم العائلة. |
| **اسم العائلة**</br>mshr_lastname</br>*سلسلة*) | للقراءة فقط | اسم العائلة. |
| **الاسم الأوسط**</br>mshr_middlename</br>*سلسلة*) | للقراءة فقط | الاسم الأوسط. |
| **صالح حتى**</br>mshr_validto</br>*سلسلة*) | للقراءة فقط | تاريخ انتهاء صلاحية الاسم. |
| **رقم الطرف**</br>mshr_partynumber</br>*سلسلة* | للقراءة فقط | معرف فريد منشأ بواسطة النظام للشخص. |
| **الحقل الأساسي**</br>mshr_primaryfield</br>*سلسلة* | للقراءة فقط | المعرف الفريد للسجل. |
| **معرف كيان محفوظات أسماء الأشخاص**</br>mshr_dirpersonnamehistoricalentityid</br>*GUID* | النظام منشأ | قيمة معرف فريد عمومي (GUID) يقوم النظام بإنشائه لتعريف السجل بشكل فريد. |

## <a name="relations"></a>العلاقات

| قيمة الخاصية | الكيان المرتبط | خاصيه التنقل | نوع التجميع |
| --- | --- | --- | --- |
| غير قابل للتطبيق | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | غير قابل للتطبيق | mshr_FK_PayrollEmployeeEntity_Name |

## <a name="example-query-for-payroll-employee"></a>نموذج الاستعلام لموظف كشل الرواتب

**الطلب**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_dirpersonnamehistoricalentities?$filter=mshr_partynumber eq 'HR000001606'
```

**استجابة**

```json
{
    "mshr_firstname": "Agustina",
    "mshr_lastnameprefix": "",
    "mshr_lastname": "Fierro",
    "mshr_middlename": "middle",
    "mshr_validto": "2021-09-10T21:23:53Z",
    "mshr_partynumber": "HR000001606",
    "mshr_primaryfield": "HR000001606 | ",
    "mshr_dirpersonnamehistoricalentityid": "00000832-0000-0000-c12b-014105000000",
    "mshr_validfrom": null
},
{
    "mshr_firstname": "Agustina",
    "mshr_lastnameprefix": "",
    "mshr_lastname": "Fierro",
    "mshr_middlename": "",
    "mshr_validto": "2154-12-31T23:59:59Z",
    "mshr_partynumber": "HR000001606",
    "mshr_primaryfield": "HR000001606 | 9/10/2021 09:23:54 pm",
    "mshr_dirpersonnamehistoricalentityid": "00000832-0000-0000-d20b-000010000000",
    "mshr_validfrom": "2021-09-10T21:23:54Z"
}
```

## <a name="see-also"></a>راجع أيضًا

[‏‫مقدمة إلى واجهة API لتكامل كشف الرواتب](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
