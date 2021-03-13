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
ms.openlocfilehash: 3f7bae64f58f0bdc1603b3c1b5493f1ebcfa8de9
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126040"
---
# <a name="recruiting-request-position-status"></a>حالة منصب طلب التعيين

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
