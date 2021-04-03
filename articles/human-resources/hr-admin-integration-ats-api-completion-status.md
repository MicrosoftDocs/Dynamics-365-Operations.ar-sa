---
title: حالة الإكمال
description: يصف هذا الموضوع مجموعة خيارات حالة الإكمال لـ Dynamics 365 Human Resources.
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
ms.openlocfilehash: d8ea90785f303301a21a4ac799578b08cabd0e3d
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468193"
---
# <a name="completion-status"></a>حالة الإكمال

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا الموضوع مجموعة خيارات حالة الإكمال لـ Dynamics 365 Human Resources.

الاسم الفعلي: mshr_hcmcompletionstatus

توفر قائمة التعداد هذه مجموعة الخيارات الخاصة بقيم الحالة لعمليات مراقبة المرشحين. 

| قيمة | تسمية | الوصف |
| --- | --- | --- |
| 200000000 | غير كامل | لم يقم المرشح بإكمال عملية المراقبة بعد. |
| 200000001 | نجاح | اجتاز المرشح عملية المراقبة. |
| 200000002 | فشل | فشل المرشح في اجتياز عملية المراقبة. |

## <a name="see-also"></a>راجع أيضًا

[مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب](hr-admin-integration-ats-api-introduction.md)<br>
[مثال الاستعلام عن مرشح مراد توظيفه](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]