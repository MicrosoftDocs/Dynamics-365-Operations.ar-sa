---
title: خطة التعويض الثابتة لكشف الرواتب
description: يوفر هذا الموضوع تفاصيل ومثال استعلام لكيان خطة التعويض الثابت في كشف الرواتب في Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 85cfce6f626090adab422ea6c60fc0778fd1ac67
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021286"
---
# <a name="payroll-fixed-compensation-plan"></a>خطة التعويض الثابتة لكشف الرواتب

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يوفر هذا الموضوع تفاصيل ومثال استعلام لكيان خطة التعويض الثابت في كشف الرواتب في Dynamics 365 Human Resources.

## <a name="properties"></a>الخصائص

| الخاصية<br>**الاسم الفعلي**<br>**_النوع_** | استخدام | الوصف |
| --- | --- | --- |
| **معرف الموظف**<br>mshr_fk_employee_id_value<br>*GUID* | للقراءة فقط<br>مطلوب<br>مفتاح خارجي:mshr_Employee_id لـ mshr_payrollemployeeentity entity  | معرف الموظف |
| **معدل الدفع**<br>mshr_payrate<br>*عشري* | للقراءة فقط<br>مطلوب | معدل الدفع المحدد في خطة التعويض الثابت. |
| **معرف الخطة**<br>mshr_planid<br>*سلسلة* | للقراءة فقط<br>مطلوب |تحدد خطة التعويض.  |
| **صالح من**<br>mshr_validfrom<br>*الفرق بالتاريخ والوقت* |  للقراءة فقط<br>مطلوب |تاريخ بدء صلاحية التعويض الثابت للموظف.  |
| **كيان خطة التعويض الثابتة لكشف الرواتب**<br>mshr_payrollfixedcompensationplanentityid<br>*GUID* | مطلوب<br>منشأ بواسطة النظام | قيمة معرف GUID منشأ بواسطة النظام لتعريف خطة التعويض بشكل فريد. |
| **تكرار الدفع**<br>mshr_payfrequency<br>*سلسلة* | للقراءة فقط<br>مطلوب |تكرار تنفيذ عملية الدفع للموظف.  |
| **صالح حتى**<br>mshr_validto<br>*الفرق بالتاريخ والوقت* | للقراءة فقط <br>مطلوب | تاريخ انتهاء صلاحية التعويض الثابت للموظف. |
| **معرف المنصب**<br>mshr_positionid<br>*سلسلة* | للقراءة فقط <br>مطلوب | معرف المنصب المرتبط بالموظف وتسجيل خطة التعويض الثابت. |
| **عملة**<br>mshr_currency<br>*سلسلة* | للقراءة فقط <br>مطلوب |العملة المحددة لخطة التعويض الثابت   |
| **رقم الموظف**<br>mshr_personnelnumber<br>*سلسلة* | للقراءة فقط<br>مطلوب |رقم الموظف الفريد الخاص بالموظف.  |

**استعلام**

**الطلب**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

**استجابة**

```json
{
            "mshr_planid": "GradeC",
            "mshr_personnelnumber": "000041",
            "mshr_payrate": 75200,
            "mshr_positionid": "000276",
            "mshr_validfrom": "2011-04-05T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_payfrequency": "Annual",
            "mshr_currency": "USD",
            "_mshr_fk_employee_id_value": "00000d3c-0000-0000-d5ff-004105000000",
            "_mshr_fk_plan_id_value": "0000070c-0000-0000-b328-fef003000000",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "mshr_payrollfixedcompensationplanentityid": "0000029f-0000-0000-d5ff-004105000000",
            "_mshr_fk_payroll_id_value": null
}
```
