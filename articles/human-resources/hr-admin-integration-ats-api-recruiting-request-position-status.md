---
title: حالة منصب طلب التعيين
description: توضح هذه المقالة مجموعة خيارات حالة المنصب لطلب التوظيف في Dynamics 365 Human Resources.
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
ms.openlocfilehash: 736bdbfb8759ab61202d1f17e3cdc8294be0ba84
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846388"
---
# <a name="recruiting-request-position-status"></a>حالة منصب طلب التعيين


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

توضح هذه المقالة مجموعة خيارات حالة المنصب لطلب التوظيف في Dynamics 365 Human Resources.

الاسم الفعلي: mshr_hcmrecruitingrequestpositionstatus

توفر قائمة التعداد هذه مجموعة الخيارات لقيم الحالة لكل منصب خاص بطلب تعيين في الكيان RecruitingRequestPosition.

| قيمة | تسمية | الوصف |
| --- | --- | --- |
| 200000000 | مفتوحة | المنصب في طلب التعيين مفتوح للتعيين. هذا لا يشير إلى أنه لا يوجد تعيين لمنصب نشط حاليًا للمنصب. قد يكون هناك موظف في المنصب وقت التوظيف. يشير فقط إلى أن المنصب متوفر للتعيين في سياق طلب التعيين. |
| 200000001 | مشغول‬ | تم تحديد عامل للتعيين في المنصب. |
| 200000002 | مُلغاة | تم إلغاء الطلب الخاص بالتعيين لهذا المنصب. |

## <a name="see-also"></a>راجع أيضًا

[مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب](hr-admin-integration-ats-api-introduction.md)<br>
[مثال لاستعلام عن طلب تعيين](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
