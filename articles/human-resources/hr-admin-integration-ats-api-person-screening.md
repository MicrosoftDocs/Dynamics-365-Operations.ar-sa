---
title: مراقبة الأشخاص
description: توضح هذه المقالة كيان مراقبة الشخص لـ Dynamics 365 Human Resources.
author: jaredha
ms.date: 12/05/2022
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
ms.openlocfilehash: 3c316e0381f4d407ed7c4c39b5949717b71477bd
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831880"
---
# <a name="person-screening"></a>مراقبة الأشخاص


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

توضح هذه المقالة كيان مراقبة الشخص لـ Dynamics 365 Human Resources.

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
    "_mshr_fk_screeningtype_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a>الخصائص

| الخاصية<br>**الاسم الفعلي**<br>**_النوع_** | استخدام | ‏‏الوصف‬ |
| --- | --- | --- |
| **الملاحظات**<br>mshr_note<br>*سلسلة* | قراءة/كتابة<br>اختياري | ملاحظات للاستخدام من جانب مسؤولي التعيين ومدراء التوظيف. |
| **مطلوب من**<br>mshr_requiredby<br>*Datetime* | قراءة/كتابة<br>اختياري | التاريخ المطلوب فيه إكمال عملية المراقبة. |
| **الحالة**<br>mshr_status<br>*مجموعة خيارات mshr_hcmcompletionstatus*|قراءة/كتابة<br>مرجو | يوفر حالة المرشح لعملية المراقبة. |
| **رقم الطرف**<br>mshr_partynumber<br>*سلسلة* | قراءة/كتابة<br>مرجو | رقم الطرف (الشخص) المقترن بالمرشح. |
| **معرف نوع المراقبة**<br>mshr_screeningtypeid<br>*سلسلة* | قراءة/كتابة<br>مطلوب<br>المفتاح الخارجي: ScreeningType | معرف نوع المراقبة المحدد في الموارد البشرية. |
| **قيمة معرف نوع المراقبة**<br>_mshr_fk_screeningtype_id_value<br>*GUID* | للقراءة فقط<br>مطلوب<br>المفتاح الخارجي: mshr_hcmscreeningtypeentityid لـ mshr_hcmscreeningtypeentity | معرف فريد منشأ بواسطة النظام لسجل نوع المراقبة في الكيان المقترن. |
| **الحقل الأساسي**<br>mshr_primaryfield<br>*سلسلة* |  للقراءة فقط<br>مرجو | حقل المطلوب استخدامه كمعرف لسجل الكيان. |
| **قيمة معرف الشخص**<br>_mshr_fk_person_id_value<br>*GUID* | للقراءة فقط<br>مطلوب<br>المفتاح الخارجي: mshr_dirpersonentityid لـ mshr_dirpersonentity | المعرف الفريد المنشأ بواسطة النظام لسجل كيان الطرف (الشخص). |
| **معرف كيان مراقبة الشخص**<br>mshr_hcmpersonscreeningentityid<br>*GUID* | للقراءة فقط<br>مطلوب<br>منشأ بواسطة النظام| المعرف الأساسي الفريد لسجل مراقبة الشخص. |
| **تاريخ الإكمال**<br>mshr_completeddate<br>*Datetime* | قراءة/كتابة<br>اختياري | تاريخ اكتمال عملية المراقبة. |


## <a name="see-also"></a>راجع أيضًا

[مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب](hr-admin-integration-ats-api-introduction.md)<br>
[مثال الاستعلام عن مرشح مراد توظيفه](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
