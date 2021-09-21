---
title: الموظف حسب كشف الرواتب
description: يوفر هذا الموضوع تفاصيل ومثال استعلام لكيان موظف كشف الرواتب في Dynamics 365 Human Resources.
author: jcart
ms.date: 08/25/2021
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
ms.openlocfilehash: 450872a38c833de9d37e2c6224839f2bca7cb4c6
ms.sourcegitcommit: 4d11061f5de0ddba1f968bd5c3fd694a8b104ccc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/26/2021
ms.locfileid: "7429214"
---
# <a name="payroll-employee"></a>الموظف حسب كشف الرواتب

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا الموضوع كيان الموظف في الرواتب لـ Dynamics 365 Human Resources.

الاسم الفعلي: mshr_payrollemployeeentity.

### <a name="description"></a>الوصف

يوفر هذا الكيان معلومات حول الموظف. يجب تعيين [معلمات تكامل الرواتب](hr-admin-integration-payroll-api-parameters.md) قبل استخدام هذا الكيان.

>[!IMPORTANT] 
>حقول **FirstName**، و **MiddleName**، و **LastName**، و **NameValidFrom**، و **NameValidTo** لن تكون متوفرة على هذا الكيان. وهذا يضمن وجود مصدر بيانات تاريخ فعال واحد فقط يدعم هذا الكيان.
>ستكون هذه الحقول متوفرة على **DirPersonNameHistoricalEntity**، الذي تم إصداره في تحديث النظام الأساسي 43. هناك علاقة OData من **PayrollEmployeeEntity** إلى **DirPersonNameHistoricalEntity**. 

## <a name="properties"></a>الخصائص

| الخاصية</br>**الاسم الفعلي**</br>**_النوع_** | استخدام | الوصف |
| --- | --- | --- |
| **معرف الكيان القانوني**</br>mshr_legalentityid</br>*سلسلة* | للقراءة فقط | يحدد الكيان القانوني (الشركة). |
| **رقم الموظف**</br>mshr_personnelnumber</br>*سلسلة* | للقراءة فقط | رقم الموظف الفريد الخاص بالموظف. |
| **تاريخ بداية التوظيف**</br>mshr_employmentstartdate</br>*الفرق بالتاريخ والوقت* | للقراءة فقط | تاريخ بدء توظيف الموظف. |
| **تاريخ انتهاء التوظيف**</br>mshr_employmentenddate</br>*الفرق بالتاريخ والوقت* | للقراءة فقط |تاريخ انتهاء توظيف الموظف.  |
| **تاريخ الميلاد**</br>mshr_birthdate</br>*الفرق بالتاريخ والوقت* | للقراءة فقط | تاريخ ميلاد الموظف. |
| **الجنس**</br>mshr_gender</br>[مجموعة خيارات mshr_hcmpersongender](hr-admin-integration-payroll-api-gender.md) | للقراءة فقط | جنس الموظف. |
| **نوع التوظيف**</br>mshr_employmenttype</br>[مجموعة خيارات mshr_hcmemploymenttype](hr-admin-integration-payroll-api-hcmemploymenttype.md) | للقراءة فقط | نوع التوظيف. |
| **معرف نوع التعريف**</br>mshr_identificationtypeid</br>*سلسلة* |للقراءة فقط | نوع التعريف المحدد للموظف. |
| **رقم التعريف**</br>mshr_identificationnumber</br>*سلسلة* | للقراءة فقط |رقم التعريف المحدد للموظف. |
| **جاهز للدفع**</br>mshr_readytopay</br>[مجموعة خيارات mshr_noyes](hr-admin-integration-payroll-api-no-yes.md) | للقراءة فقط | يشير إلى ما إذا كان الموظف قد تم وضع علامة عليه كجاهز للدفع أم لا. |
| **معرف كيان موظف كشف الرواتب**</br>mshr_payrollemployeeentityid</br>*GUID* | مطلوب</br>النظام منشأ | قيمة معرف GUID منشأ بواسطة النظام لتعريف الموظف بشكل فريد. |

## <a name="relations"></a>العلاقات

|قيمة الخاصية | الكيان المرتبط | خاصيه التنقل | نوع التجميع |
| --- | --- | --- | --- |
| _mshr_fk_employment_id_value | mshr_hcmemploymentdetailentity | mshr_FK_Employment_id | - |
| _mshr_fk_fixedcompplan_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_Employee |
| _mshr_fk_name_id_value | mshr_dirpersonnamehistoricalentity | mshr_FK_Name_id | - |
| _mshr_fk_worker_id_value | mshr_hcmworkerbaseentity | mshr_FK_Worker_id | - |
| _mshr_fk_workerbankaccount_id_value | mshr_hcmworkerbankaccountentity | mshr_FK_WorkerBankAccount_id | - |
| _mshr_fk_variablecompaward_id_value | [mshr_payrollvariablecompensationawardentity](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md) | mshr_FK_VariableCompAward_id | mshr_FK_PayrollVariableCompensationAwardEntity_Employee |
| _mshr_fk_address_id_value | [mshr_payrollworkeraddressentity](hr-admin-integration-payroll-api-payroll-worker-address.md) | mshr_FK_Address_id | mshr_FK_PayrollWorkerAddressEntity_Worker |

## <a name="example-query-for-payroll-employee"></a>نموذج الاستعلام لموظف كشل الرواتب

**الطلب**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollemployeeentities?$filter=mshr_personnelnumber eq '000041'
```

**استجابة**

```json
{
    "mshr_legalentityid": "USMF",
    "mshr_personnelnumber": "000041",
    "mshr_employmentstartdate": "2011-04-05T07:00:00Z",
    "mshr_employmentenddate": "2154-12-31T23:59:59Z",
    "mshr_birthdate": "1987-09-12T00:00:00Z",
    "mshr_gender": 200000002,
    "mshr_employmenttype": 200000000,
    "mshr_identificationtypeid": "SSN",
    "mshr_identificationnumber": "888-99-9342",
    "mshr_readytopay": 200000000,
    "mshr_dataareaid": "USMF",
    "mshr_primaryfield": "000041 | USMF | 4/5/2011 07:00:00 am",
    "_mshr_fk_employment_id_value": "00000d4e-0000-0000-0600-014105000000",
    "_mshr_fk_fixedcompplan_id_value": "00000598-0000-0000-4cd0-fda002000000",
    "_mshr_fk_name_id_value": "00000832-0000-0000-d700-014105000000",
    "_mshr_fk_worker_id_value": "000000af-0000-0000-d5ff-004105000000",
    "_mshr_fk_workerbankaccount_id_value": "000006f2-0000-0000-b7ff-004105000000",
    "mshr_payrollemployeeentityid": "00000666-0000-0000-d5ff-004105000000",
    "_mshr_fk_address_id_value": null,
    "_mshr_fk_variablecompaward_id_value": null,
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>راجع أيضًا

[‏‫مقدمة إلى واجهة API لتكامل كشف الرواتب](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
