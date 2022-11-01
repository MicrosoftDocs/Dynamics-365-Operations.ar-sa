---
title: نتيجة تكامل مقدم الطلب
description: توضح هذه المقالة مجموعة خيارات نتيجة تكامل مقدم الطلب لـ Dynamics 365 Human Resources.
author: jaredha
ms.date: 09/12/2022
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
ms.openlocfilehash: 86f3f75e538268644cea4f927f04c07aae115f00
ms.sourcegitcommit: 27ce4fc706100b626b81c3a1023238acd872e76c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/20/2022
ms.locfileid: "9702218"
---
# <a name="applicant-integration-result"></a>نتيجة تكامل مقدم الطلب


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

توضح هذه المقالة مجموعة خيارات نتيجة تكامل مقدم الطلب لـ Dynamics 365 Human Resources.

الاسم الفعلي: mshr_hcmapplicantintegrationresult

يوفر هذا التعداد الحالة لسجل مرشح.

| قيمة | تسمية | الوصف |
| --- | --- | --- |
| 200000000 | لم تتم المعالجة | لا يزال المرشح تحت الاعتبار. |
| 200000001 | تم التوظيف | تم توظيف المرشح. |
| 200000002 | لم يتم توظيفه | تم اتخاذ قرار بعدم توظيف المرشح. |
| 200000003 | مستبعد | تم استبعاد المرشح من الاعتبار. |

## <a name="see-also"></a>راجع أيضًا

[مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب](hr-admin-integration-ats-api-introduction.md)<br>
[مثال الاستعلام عن مرشح مراد توظيفه](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
