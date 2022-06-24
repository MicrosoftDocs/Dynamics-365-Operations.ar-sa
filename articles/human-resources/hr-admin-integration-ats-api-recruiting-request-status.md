---
title: حالة طلب التعيين
description: توضح هذه المقالة مجموعة خيارات حالة التوظيف في Dynamics 365 Human Resources.
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
ms.openlocfilehash: 6a8cb8bc61786425c996b976a2914e7b650e3941
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859593"
---
# <a name="recruiting-request-status"></a>حالة طلب التعيين


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

توضح هذه المقالة مجموعة خيارات حالة التوظيف في Dynamics 365 Human Resources.

الاسم الفعلي: mshr_hcmrecruitingrequeststatus

توفر قائمة التعداد هذه مجموعة الخيارات الخاصة بقيم الحالة لـ RecruitingRequest.

| قيمة | تسمية | الوصف |
| --- | --- | --- |
| 200000000 | مبدئي‬ | الطلب موجود في مسودة وهو غير جاهز للتوظيف النشط. |
| 200000001 | قيد المراجعة | تم إرسال الطلب ويجري توجيهه للموافقة بواسطة سير العمل. متوفر فقط عند تمكين سير العمل. |
| 200000002 | معلّق | الطلب معلق لانتظار إجراء سير العمل. متوفر فقط عند تمكين سير العمل. |
| 200000003 | مُلغاة | تم إلغاء الطلب. متوفر فقط عند تمكين سير العمل. |
| 200000004 | مرفوض | تم رفض الطلب. متوفر فقط عند تمكين سير العمل. |
| 200000005 | نشط | تم إكمال أي سير عمل والموافقة عليه، والطلب جاهز لعملية التوظيف النشطة. |
| 200000006 | مكتمل | تم إقفال طلب التعيين. |

## <a name="see-also"></a>راجع أيضًا

[مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب](hr-admin-integration-ats-api-introduction.md)<br>
[مثال لاستعلام عن طلب تعيين](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
