---
title: حالة الإعفاء من الوظيفة
description: يصف هذا الموضوع مجموعة خيارات حالة الإعفاء من الوظيفة لـ Dynamics 365 Human Resources.
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
ms.openlocfilehash: 0cd6ffc01793c8ff12e36175c7c9feaf8a4b3cdf
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125559"
---
# <a name="job-exempt-status"></a>حالة الإعفاء من الوظيفة

يصف هذا الموضوع مجموعة خيارات حالة الإعفاء من الوظيفة لـ Dynamics 365 Human Resources.

الاسم الفعلي: cdm_jobexemptstatus

تحدد قائمة التعداد هذه مجموعة خيارات لقيم حالة حالة الإعفاء من الوظيفة لـ FLSA. يتم توفير ذلك في مجموعة خيارات cdm_jobexemptstatus الموجودة.

| قيمة | تسمية | الوصف |
| --- | --- | --- |
| 200000000 | إعفاء | تحتوي الوظيفة على حالة إعفاء استنادا إلى إرشادات FLSA. |
| 200000001 | NonExempt | تحتوي الوظيفة على حالة عدم إعفاء استنادا إلى إرشادات FLSA. |
| 200000002 | لا ينطبق | لا تنطبق إرشادات حالة FLSA على الوظيفة. |

## <a name="see-also"></a>راجع أيضًا

[مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب](hr-admin-integration-ats-api-introduction.md)<br>
[مثال لاستعلام عن طلب تعيين](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]