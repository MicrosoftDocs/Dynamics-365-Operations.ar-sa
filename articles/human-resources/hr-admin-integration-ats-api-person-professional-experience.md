---
title: الخبرة المهنية للشخص
description: يصف هذا الموضوع كيان الخبرة المهوية للشخص في Dynamics 365 Human Resources.
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
ms.openlocfilehash: cc26e0ae1428811161b3573edec4aa47b46ae16dd8a69d44d2cdd77d49e68193
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763024"
---
# <a name="person-professional-experience"></a>الخبرة المهنية للشخص

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا الموضوع كيان الخبرة المهوية للشخص في Dynamics 365 Human Resources.

الاسم الفعلي: mshr_hcmpersonprofessionalexperienceentity

## <a name="description"></a>الوصف

يصف هذا الكيان الخبرة المهنية أو محفوظات العمل الخاصة بأحد الترشيحات.

## <a name="json-representation"></a>تمثيل JSON

```json
{
    "mshr_partynumber": "String",
    "mshr_employerposition": "String",
    "mshr_startdate": "Date",
    "mshr_allowcontactemployer": Int,
    "mshr_employerlocation": "String",
    "mshr_employername": "String",
    "mshr_enddate": "Date",
    "mshr_note": "String",
    "mshr_phone": "String",
    "mshr_url": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonprofessionalexperienceentityid": "Guid"
}
```

## <a name="properties"></a>الخصائص

| الخاصية<br>**الاسم الفعلي**<br>**_النوع_** | استخدام | الوصف |
| --- | --- | --- |
| **معرف كيان الخبرة المهنية للشخص**<br>mshr_hcmpersonprofessionalexperienceentityid<br>*GUID* | للقراءة فقط<br>مطلوب | معرف فريد منشأ بواسطة النظام لسجل الكيان. |
| **رقم الطرف**<br>mshr_partynumber<br>*سلسلة* | قراءة/كتابة<br>مطلوب | المعرف الفريد لسجل الشخص الخاص بالمرشح. |
| **قيمة معرف الشخص**<br>_mshr_fk_person_id_value<br>*GUID* | للقراءة فقط<br>مطلوب<br>المفتاح الخارجي: mshr_dirpersonentityid لـ mshr_dirpersonentity | معرف فريد منشأ بواسطة النظام لسجل كيان الشخص. |
| **منصب صاحب العمل**<br>mshr_employerposition<br>*سلسلة* | قراءة/كتابة<br>مطلوب | لقب المنصب الذي كان المرشح يشغله أثناء التوظيف. |
| **اسم صاحب العمل**<br>mshr_employername<br>*سلسلة* | قراءة/كتابة<br>مطلوب | اسم صاحب العمل. |
| **موقع صاحب العمل**<br>mshr_employerlocation<br>*سلسلة* | قراءة/كتابة<br>اختياري | موقع صاحب العمل. الحد الأقصى للطول: 60. لا يوجد تنسيق خاص مطلوب أو محدد. |
| **الهاتف**<br>mshr_phone<br>*سلسلة* | قراءة/كتابة<br>اختياري | رقم هاتف صاحب العمل. |
| **عنوان URL**<br>mshr_url<br>*سلسلة* | قراءة/كتابة<br>اختياري | عنوان URL لموقع ويب صاحب العمل. |
| **تاريخ البدء**<br>mshr_startdate<br>*Datetime* | قراءة/كتابة<br>مطلوب | تاريخ بدء توظيف المرشح. |
| **تاريخ النهاية**<br>mshr_enddate<br>*Datetime* | قراءة/كتابة<br>اختياري | تاريخ الانتهاء الخاص بتوظيف المرشح أو قيمة خالية في حالة ما إذا كانت المرشح ما يزال موظفًا هنا. |
| **السماح بالاتصال بصاحب العمل**<br>mshr_allowcontactemployer<br>*مجموعة خيارات mshr_hrmblankyesno* | قراءة/كتابة<br>اختياري | يشير ما إذا كان المرشح يسمح بالاتصال بصاحب العمل السابق أم لا. |
| **الملاحظات**<br>mshr_note<br>*سلسلة* | قراءة/كتابة<br>اختياري | ملاحظات للاستخدام من جانب مسؤولي التعيين أو مدراء التوظيف. |
| **الحقل الأساسي**<br>mshr_primaryfield<br>*سلسلة* | للقراءة فقط<br>مطلوب | حقل يستخدم كمعرف أساسي لسجل الكيان. مجموعة رقم الطرف وتاريخ البدء ومنصب صاحب العمل واسم صاحب العمل. |

## <a name="see-also"></a>راجع أيضًا

[مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب](hr-admin-integration-ats-api-introduction.md)<br>
[مثال الاستعلام عن مرشح مراد توظيفه](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]