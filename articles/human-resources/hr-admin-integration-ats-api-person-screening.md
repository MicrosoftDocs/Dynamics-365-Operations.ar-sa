---
title: مراقبة الأشخاص
description: يصف هذا الموضوع كيان مراقبة الشخص لـ Dynamics 365 Human Resources.
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
ms.openlocfilehash: c6287f30aaa008ea77b91fd46a8dfb2b7c905036
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467231"
---
# <a name="person-screening"></a>مراقبة الأشخاص

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا الموضوع كيان مراقبة الشخص لـ Dynamics 365 Human Resources.

الاسم الفعلي: mshr_hcmpersonscreeningentity

## <a name="description"></a>الوصف

يصف هذا الكيان عمليات المراقبة لمرشح الذي نجح أو يجب أن ينجح في التوظيف.

## <a name="json-representation"></a>تمثيل JSON

```json
{
    "mshr_note": "String",
    "mshr_requiredby": "Date",
    "mshr_status": Int,
    "mshr_partynumber": "String",
    "mshr_screeningtypeid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a>الخصائص

| الخاصية<br>**الاسم الفعلي**<br>**_النوع_** | استخدام | الوصف |
| --- | --- | --- |
| **معرف كيان مراقبة الشخص**<br>mshr_hcmpersonscreeningentityid<br>*GUID* | للقراءة فقط<br>مطلوب<br>منشأ بواسطة النظام | المعرف الأساسي الفريد لسجل مراقبة الشخص. |
| **رقم الطرف**<br>mshr_partynumber<br>*سلسلة* | قراءة/كتابة<br>مطلوب | رقم الطرف (الشخص) المقترن بالمرشح. |
| **قيمة معرف الشخص**<br>_mshr_fk_person_id_value<br>*GUID* | للقراءة فقط<br>مطلوب<br>المفتاح الخارجي: mshr_dirpersonentityid لـ mshr_dirpersonentity | المعرف الفريد المنشأ بواسطة النظام لسجل كيان الطرف (الشخص). |
| **معرف نوع المراقبة**<br>mshr_screeningtypeid<br>*سلسلة* | قراءة/كتابة<br>مطلوب<br>المفتاح الخارجي: ScreeningType | معرف نوع المراقبة المحدد في الموارد البشرية. |
| **قيمة معرف نوع المراقبة**<br>_mshr_fk_screeningtype_id_value<br>*GUID* | للقراءة فقط<br>مطلوب<br>المفتاح الخارجي: mshr_hcmscreeningtypeentityid لـ mshr_hcmscreeningtypeentity | معرف فريد منشأ بواسطة النظام لسجل نوع المراقبة في الكيان المقترن. |
| **مطلوب من**<br>mshr_requiredby<br>*Datetime* | قراءة/كتابة<br>اختياري | التاريخ المطلوب فيه إكمال عملية المراقبة. |
| **الحالة**<br>mshr_status<br>*مجموعة خيارات mshr_hcmcompletionstatus*<br>قراءة/كتابة<br>مطلوب | يوفر حالة المرشح لعملية المراقبة. |
| **تاريخ الإكمال**<br>mshr_completeddate<br>*Datetime* | قراءة/كتابة<br>اختياري | تاريخ اكتمال عملية المراقبة. |
| **الملاحظات**<br>mshr_note<br>*سلسلة* | قراءة/كتابة<br>اختياري | ملاحظات للاستخدام من جانب مسؤولي التعيين ومدراء التوظيف. |

## <a name="see-also"></a>راجع أيضًا

[مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب](hr-admin-integration-ats-api-introduction.md)<br>
[مثال الاستعلام عن مرشح مراد توظيفه](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]