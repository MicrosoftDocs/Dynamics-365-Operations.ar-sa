---
title: نتيجة تكامل مقدم الطلب
description: يصف هذا الموضوع مجموعة خيارات نتيجة تكامل مقدم الطلب لـ Dynamics 365 Human Resources.
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
ms.openlocfilehash: 3f173e15d5524dfd4d63113760760b2534cc8769456df621415a11e4053cc6fb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6725904"
---
# <a name="applicant-integration-result"></a>نتيجة تكامل مقدم الطلب

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا الموضوع مجموعة خيارات نتيجة تكامل مقدم الطلب لـ Dynamics 365 Human Resources.

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