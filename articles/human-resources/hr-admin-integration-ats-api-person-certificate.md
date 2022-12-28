---
title: شهادة الشخص
description: توضح هذه المقالة كيان شهادة الشخص لـ Dynamics 365 Human Resources.
author: jaredha
ms.date: 12/15/2022
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
ms.openlocfilehash: 1f9d5a8c83d9714a4d10dec16e66ab87b794b074
ms.sourcegitcommit: 69d7dd6a2d0dc7f2661c7d1f61e8874c7bde1448
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/19/2022
ms.locfileid: "9887307"
---
# <a name="person-certificate"></a>شهادة الشخص


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

توضح هذه المقالة كيان شهادة الشخص لـ Dynamics 365 Human Resources.

الاسم الفعلي: mshr_hcmpersoncertificateentity

## <a name="description"></a>الوصف

يصف هذا الكيان الشهادات المهنية لأحد المرشحين.

## <a name="json-representation"></a>تمثيل JSON

```json
{
    "mshr_certificatetypeid": "String",
    "mshr_startdate": "Date",
    "mshr_enddate": "Date",
    "mshr_notes": "String",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_certificatetype_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersoncertificateentityid": "Guid"
}
```

## <a name="properties"></a>الخصائص

| الخاصية<br>**الاسم الفعلي**<br>**_النوع_** | استخدام | ‏‏الوصف‬ |
| --- | --- | --- |
| **معرف نوع الشهادة**<br>mshr_certificatetypeid<br>*سلسلة* | قراءة/كتابة<br>مطلوب |  معرف نوع الشهادة المحدد في الموارد البشرية. |
| **تاريخ البدء**<br>mshr_startdate<br>*Datetime* | قراءة/كتابة<br>مرجو | التاريخ الذي تم فيه إصدار الشهادة. |
| **تاريخ النهاية**<br>mshr_enddate<br>*Datetime* | قراءة/كتابة<br>اختياري | التاريخ الذي ستنتهي فيه الشهادة. |
| **الملاحظات**<br>mshr_notes<br>*سلسلة* | قراءة/كتابة<br>اختياري | ملاحظات للاستخدام من جانب مسؤولي التعيين ومدراء التوظيف. |
| **رقم الطرف**<br>mshr_partynumber<br>*سلسلة* | قراءة/كتابة<br>مرجو | معرف الطرف (الشخص) للمرشح. |
| **الحقل الأساسي**<br>mshr_primaryfield<br>*سلسلة* | للقراءة فقط<br>مرجو |  حقل المطلوب استخدامه كمعرف لسجل الكيان. مجموعة رقم الطرف ومعرف نوع الشهادة وتاريخ البدء. |
| **قيمة معرف نوع الشهادة**<br>_mshr_fk_certificatetype_id_value<br>*GUID* | للقراءة فقط<br>مطلوب<br>المفتاح الخارجي: mshr_hcmcertificatetypeentityid لـ mshr_hcmcertificatetypeentity | معرف فريد منشأ بواسطة النظام لنوع الشهادة في الكيان المقترن. |
| **قيمة معرف الشخص**<br>_mshr_fk_person_id_value<br>*GUID* | للقراءة فقط<br>مطلوب<br>المفتاح الخارجي: mshr_dirpersonentityid لـ mshr_dirpersonentity | المعرف الفريد المنشأ بواسطة النظام لسجل كيان الطرف (الشخص). |
| **معرف كيان شهادة الشخص**<br>mshr_hcmpersoncertificateentityid<br>*GUID* | للقراءة فقط<br>مطلوب | معرف فريد منشأ بواسطة النظام لسجل كيان شهادة الشخص. |




## <a name="see-also"></a>راجع أيضًا

[مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب](hr-admin-integration-ats-api-introduction.md)<br>
[مثال الاستعلام عن مرشح مراد توظيفه](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
