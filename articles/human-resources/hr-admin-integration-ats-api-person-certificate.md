---
title: شهادة الشخص
description: يصف هذا الموضوع كيان شهادة الشخص لـ Dynamics 365 Human Resources.
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
ms.openlocfilehash: fa4582dc00341a647f1ea43ed16d9dce8bfcf688
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125343"
---
# <a name="person-certificate"></a>شهادة الشخص

يصف هذا الموضوع كيان شهادة الشخص لـ Dynamics 365 Human Resources.

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

| الخاصية<br>**الاسم الفعلي**<br>**_النوع_** | استخدام | الوصف |
| --- | --- | --- |
| **معرف كيان شهادة الشخص**<br>mshr_hcmpersoncertificateentityid<br>*GUID* | للقراءة فقط<br>مطلوب | معرف فريد منشأ بواسطة النظام لسجل كيان شهادة الشخص. |
| **رقم الطرف**<br>mshr_partynumber<br>*سلسلة* | قراءة/كتابة<br>مطلوب | معرف الطرف (الشخص) للمرشح. |
| **قيمة معرف الشخص**<br>_mshr_fk_person_id_value<br>*GUID* | للقراءة فقط<br>مطلوب<br>المفتاح الخارجي: mshr_dirpersonentityid لـ mshr_dirpersonentity | المعرف الفريد المنشأ بواسطة النظام لسجل كيان الطرف (الشخص). |
| **معرف نوع الشهادة**<br>mshr_certificatetypeid<br>*سلسلة* | قراءة/كتابة<br>مطلوب |  معرف نوع الشهادة المحدد في الموارد البشرية. |
| **قيمة معرف نوع الشهادة**<br>_mshr_fk_certificatetype_id_value<br>*GUID* | للقراءة فقط<br>مطلوب<br>المفتاح الخارجي: mshr_hcmcertificatetypeentityid لـ mshr_hcmcertificatetypeentity | معرف فريد منشأ بواسطة النظام لنوع الشهادة في الكيان المقترن. |
| **تاريخ البدء**<br>mshr_startdate<br>*Datetime* | قراءة/كتابة<br>مطلوب | التاريخ الذي تم فيه إصدار الشهادة. |
| **تاريخ النهاية**<br>mshr_enddate<br>*Datetime* | قراءة/كتابة<br>اختياري | التاريخ الذي ستنتهي فيه الشهادة. |
| **الملاحظات**<br>mshr_notes<br>*سلسلة* | قراءة/كتابة<br>اختياري | ملاحظات للاستخدام من جانب مسؤولي التعيين ومدراء التوظيف. |
| **الحقل الأساسي**<br>mshr_primaryfield<br>*سلسلة* | للقراءة فقط<br>مطلوب |  حقل المطلوب استخدامه كمعرف لسجل الكيان. مجموعة رقم الطرف ومعرف نوع الشهادة وتاريخ البدء. |

## <a name="see-also"></a>راجع أيضًا

[مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب](hr-admin-integration-ats-api-introduction.md)<br>
[مثال الاستعلام عن مرشح مراد توظيفه](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]