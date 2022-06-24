---
title: مراقبة الأشخاص
description: توضح هذه المقالة كيان مراقبة الشخص لـ Dynamics 365 Human Resources.
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
ms.openlocfilehash: e9b2bbda8f8191f592462f4fbd1902e7274cf7f8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907629"
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
