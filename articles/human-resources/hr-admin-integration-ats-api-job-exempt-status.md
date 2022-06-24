---
title: حالة الإعفاء من الوظيفة
description: توضح هذه المقالة مجموعة خيارات حالة الإعفاء من الوظيفة لـ Dynamics 365 Human Resources.
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
ms.openlocfilehash: e59a71264d50cecce4d31dfa26ad7f05ef3f34e4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894661"
---
# <a name="job-exempt-status"></a>حالة الإعفاء من الوظيفة


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

توضح هذه المقالة مجموعة خيارات حالة الإعفاء من الوظيفة لـ Dynamics 365 Human Resources.

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
