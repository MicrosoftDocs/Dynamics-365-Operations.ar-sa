---
title: حالة منصب طلب التعيين
description: يصف هذا الموضوع مجموعة خيارات حالة المنصب لطلب التعيين في Dynamics 365 Human Resources.
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
ms.openlocfilehash: 01e8aa5157d0ad1c01f996886e7845e49ab97603
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464708"
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