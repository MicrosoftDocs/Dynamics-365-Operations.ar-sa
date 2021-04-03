---
title: نتيجة تكامل مقدم الطلب
description: يصف هذا الموضوع مجموعة خيارات نتيجة تكامل مقدم الطلب لـ Dynamics 365 Human Resources.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dd25eca9cccf46ec4e4bb2a1d948ca98985e73e4
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467543"
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