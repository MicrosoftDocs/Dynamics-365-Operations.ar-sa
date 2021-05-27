---
title: وظيفة منصب كشف الرواتب
description: يوفر هذا الموضوع تفاصيل ومثال استعلام لكيان وظيفة منصب كشف الرواتب في Dynamics 365 Human Resources.
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
ms.openlocfilehash: 9444a36f5ddf92bd41008c83ec77ab7ff5191fa3
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019336"
---
# <a name="payroll-position-job"></a>وظيفة منصب كشف الرواتب

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يوفر هذا الموضوع تفاصيل ومثال استعلام لكيان علاقة منصب كشف الرواتب في Dynamics 365 Human Resources.

## <a name="properties"></a>الخصائص

| الخاصية<br>**الاسم الفعلي**<br>**_النوع_** | استخدام | الوصف |
| --- | --- | --- |
| **معرف الوظيفة**<br>mshr_jobid<br>*سلسلة* | للقراءة فقط<br>مطلوب |معرف الوظيفة. |
| **صالح من**<br>mshr_validto<br>*الفرق بالتاريخ والوقت* | للقراءة فقط <br>مطلوب | تاريخ بدء صلاحية علاقة المنصب والوظيفة. |
| **صالح حتى**<br>mshr_validto<br>*الفرق بالتاريخ والوقت* | للقراءة فقط <br>مطلوب | تاريخ انتهاء صلاحية علاقة المنصب والوظيفة.  |
| **معرف المنصب**<br>mshr_positionid<br>*سلسلة* | للقراءة فقط<br>مطلوب | معرف المنصب. |
| **الحقل الأساسي**<br>mshr_primaryfield<br>*سلسلة* | مطلوب<br>النظام منشأ |  |
| **قيمة معرف وظيفة المنصب**<br>_mshr_fk_positionjob_id_value<br>*GUID* | للقراءة فقط<br>مطلوب<br>مفتاح خارجي:mshr_PayrollPositionJobEntity لـ mshr_payrollpositionjobentity |معرف الوظيفة المقترنة بالمنصب.|
| **قيمة معرف خطة التعويض الثابت**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | للقراءة فقط<br>مطلوب<br>مفتاح خارجي: mshr_FixedCompPlan_id لـ mshr_payrollfixedcompensationplanentity  | معرف خطة التعويض الثابت المقترنة بالمنصب. |
| **معرف كيان وظيفة المنصب في كشف الرواتب**<br>mshr_payrollpositionjobentityid<br>*Guid* | مطلوب<br>منشأ بواسطة النظام. | قيمة معرف GUID منشأ بواسطة النظام لتعريف الوظيفة بشكل فريد.  |

