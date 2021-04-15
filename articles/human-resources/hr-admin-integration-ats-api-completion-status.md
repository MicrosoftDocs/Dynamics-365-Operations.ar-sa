---
title: حالة الإكمال
description: يصف هذا الموضوع مجموعة خيارات حالة الإكمال لـ Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f1b0c61ac9d9dc611d2a4700a1a004e3d15b4445
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798359"
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