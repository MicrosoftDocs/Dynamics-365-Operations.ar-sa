---
title: حالة منصب طلب التعيين
description: يصف هذا الموضوع مجموعة خيارات حالة المنصب لطلب التعيين في Dynamics 365 Human Resources.
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
ms.openlocfilehash: dee34366289f2e7ade1a1ae24bea15c0d19683d79720a44a6327879e8060a810
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6725880"
---
# <a name="recruiting-request-position-status"></a>حالة منصب طلب التعيين

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا الموضوع مجموعة خيارات حالة المنصب لطلب التعيين في Dynamics 365 Human Resources.

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