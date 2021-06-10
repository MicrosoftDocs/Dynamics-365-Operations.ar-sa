---
title: تفاصيل كشف الرواتب للمناصب
description: يوفر هذا الموضوع تفاصيل ومثال استعلام لتفاصيل كشف الرواتب لكيان المناصب في Dynamics 365 Human Resources.
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
ms.openlocfilehash: 8918044dbf84e79015dc3bca904f204123a37db8
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056770"
---
# <a name="payroll-position"></a>منصب كشف الرواتب

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يوفر هذا الموضوع تفاصيل ومثال استعلام لتفاصيل كشف الرواتب لكيان المناصب في Dynamics 365 Human Resources.

## <a name="properties"></a>الخصائص

| الخاصية<br>**الاسم الفعلي**<br>**_النوع_** | استخدام | الوصف |
| --- | --- | --- |
| **الساعات العادية السنوية**<br>annualregularhours<br>*عشري* | للقراءة فقط<br>مطلوب | ساعات العمل الدورية السنوية المحددة في المنصب.  |
| **معرف كيان تفاصيل المنصب في كشف الرواتب**<br>payrollpositiondetailsentityid<br>*Guid* | مطلوب<br>منشأ بواسطة النظام. | قيمة معرف GUID منشأ بواسطة النظام لتعريف المنصب بشكل فريد.  |
| **الحقل الأساسي**<br>mshr_primaryfield<br>*سلسلة* | مطلوب<br>النظام منشأ |  |
| **قيمة معرف وظيفة المنصب**<br>_mshr_fk_positionjob_id_value<br>*GUID* | للقراءة فقط<br>مطلوب<br>مفتاح خارجي:mshr_PayrollPositionJobEntity لـ mshr_payrollpositionjobentity |معرف الوظيفة المقترنة بالمنصب.|
| **قيمة معرف خطة التعويض الثابت**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | للقراءة فقط<br>مطلوب<br>مفتاح خارجي: mshr_FixedCompPlan_id لـ mshr_payrollfixedcompensationplanentity  | معرف خطة التعويض الثابت المقترنة بالمنصب. |
| **معرف دورة الدفع**<br>mshr_primaryfield<br>*سلسلة* | للقراءة فقط<br>مطلوب | دورة الدفع المحددة في المنصب. |
| **الدفع بواسطة الكيان القانوني**<br>paidbylegalentity<br>*سلسلة* | للقراءة فقط<br>مطلوب | الكيان القانوني المحدد في المنصب المسؤول عن إصدار الدفع. |
| **معرف المنصب**<br>mshr_positionid<br>*سلسلة* | للقراءة فقط<br>مطلوب | معرف المنصب. |
| **صالح حتى**<br>validto<br>*الفرق بالتاريخ والوقت* | للقراءة فقط<br>مطلوب |تاريخ بدء صلاحيه تفاصيل المنصب.  |
| **صالح من**<br>validfrom<br>*الفرق بالتاريخ والوقت* | للقراءة فقط<br>مطلوب |تاريخ انتهاء صلاحيه تفاصيل المنصب.  |

**استعلام**

**الطلب**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

**استجابة**

```json
{
            "mshr_positionid": "000276",
            "mshr_paycycleid": "w",
            "mshr_annualregularhours": 3000,
            "mshr_paidbylegalentity": "USMF",
            "mshr_validfrom": "2021-03-14T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_primaryfield": "000276 | 3/14/2021",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
            "mshr_payrollpositionentityid": "00010097-0000-0000-df00-014105000000"
}
```
