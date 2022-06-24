---
title: مهارة الشخص
description: توضح هذه المقالة كيان مهارة الشخص لـ Dynamics 365 Human Resources.
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
ms.openlocfilehash: 713fde6d05904f96f7b17721e15805e07159cf78
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891310"
---
# <a name="person-skill"></a>مهارة الشخص


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

توضح هذه المقالة كيان مهارة الشخص لـ Dynamics 365 Human Resources.

الاسم الفعلي: mshr_hcmpersonskillentity

## <a name="description"></a>الوصف

يصف هذا الكيان المهارات الخاصة بالمرشح.

## <a name="json-representation"></a>تمثيل JSON

```json
{
    "mshr_certifier": "String",
    "mshr_partynumber": "String",
    "mshr_levelid": "String",
    "mshr_ratinglevelexaminer": "String",
    "mshr_skillid": "String",
    "mshr_ratingid": "String",
    "mshr_leveltype": Int,
    "mshr_yearsofexperience": Decimal,
    "mshr_verified": Int,
    "mshr_leveldate": "Date",
    "mshr_primaryfield": "String",
    "_mshr_fk_certifier_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_ratinglevel_id_value": "Guid",
    "_mshr_fk_ratinglevelexaminer_id_value": "Guid",
    "_mshr_fk_skill_id_value": "Guid",
    "mshr_hcmpersonskillentityid": "Guid"
}
```

## <a name="properties"></a>الخصائص

| الخاصية<br>**الاسم الفعلي**<br>**_النوع_** | استخدام | الوصف |
| --- | --- | --- |
| **معرف كيان مهارة الشخص**<br>mshr_hcmpersonskillentityid<br>*GUID* | للقراءة فقط<br>مطلوب | معرف فريد منشأ بواسطة النظام لسجل الكيان. |
| **رقم الطرف**<br>mshr_partynumber<br>*سلسلة* | قراءة/كتابة<br>مطلوب |   معرف سجل الطرف المرتبط (الشخص). |
| **قيمة معرف الشخص**<br>_mshr_fk_person_id_value<br>*GUID* | للقراءة فقط<br>مطلوب<br>المفتاح الخارجي: mshr_dirpersonentityid لـ mshr_dirpersonentity | المعرف الفريد المنشأ بواسطة النظام لسجل كيان الطرف (الشخص). |
| **مصدر الشهادة**<br>mshr_certifier<br>*سلسلة* | قراءة/كتابة<br>اختياري | رقم الموظف للعامل الذي قام باعتماد هذه المهارة. |
| **قيمة معرف مصدر الشهادة**<br>_mshr_fk_certifier_id_value<br>*GUID* | للقراءة فقط<br>اختياري<br>المفتاح الخارجي mshr_hcmworkerentityid لـ mshr_hcmworkerentity | المعرف الفريد الذي تم إنشاؤه بواسطة النظام لسجل العامل للعامل الذي قام باعتماد المهارة. |
| **معرف المهارة**<br>mshr_skillid<br>*سلسلة* | قراءة/كتابة<br>مطلوب | معرف المهارة المحددة في الموارد البشرية. |
| **قيمة معرف المهارة**<br>_mshr_fk_skill_id_value<br>*GUID* | للقراءة فقط<br>مطلوب<br>المفتاح الخارجي: mshr_hcmskillentityid of mshr_hcmskillentity | المعرف الذي تم إنشاؤه بواسطة النظام للمهارة المحددة. |
| **سنوات الخبرة**<br>mshr_yearsofexperience<br>*عشري* | قراءة/كتابة<br>اختياري | سنوات الخبرة التي يتمتع بها المرشح في هذه المهارة. |
| **معرف التقييم**<br>mshr_ratingid<br>*سلسلة* | قراءة/كتابة<br>مطلوب | نوع مقياس التقييم. بالنسبة لهذا الكيان، تكون القيمة **مهارات**. |
| **نوع المستوى**<br>mshr_leveltype<br>*مجموعة خيارات mshr_hrmskillleveltype* | قراءة/كتابة<br>مطلوب | تصنيف نوع للمستوى المعين للمهارة. |
| **معرف المستوى**<br>mshr_levelid<br>*سلسلة* | قراءة/كتابة<br>مطلوب | معرف مستوى التقييم الخاص بالمرشح لهذه المهارة. |
| **قيم معرف مستوى التقييم**<br>_mshr_fk_ratinglevel_id_value<br>*GUID* | للقراءة فقط<br>مطلوب<br>المفتاح الخارجي: mshr_hcmratinglevelentityid لـ mshr_hcmratinglevelentity | المعرف الذي تم إنشاؤه بواسطة النظام لمستوى التقييم. |
| **تاريخ المستوى**<br>mshr_leveldate<br>*Datetime* | قراءة/كتابة<br>مطلوب | التاريخ الذي تم فيه تصنيف المرشح في المهارة. |
| **مسؤول اختبار مستوى التقييم**<br>mshr_ratinglevelexaminer<br>*سلسلة* | قراءة/كتابة<br>اختياري | رقم الموظف للعامل الذي قام بتقييم المرشح. |
| **قيم معرف مسؤول اختبار مستوى التقييم**<br>_mshr_fk_ratinglevelexaminer_id_value<br>*GUID* | للقراءة فقط<br>اختياري<br>المفتاح الخارجي mshr_hcmworkerentityid لـ mshr_hcmworkerentity | المعرف المنشأ بواسطة النظام للعامل الذي قام باختبار مستوى مهارة المرشح. |
| **تم التحقق من الصحة**<br>mshr_verified<br>*مجموعة خيارات mshr_noyes* | قراءة/كتابة<br>مطلوب | يشير إلى إذا تم التحقق من مستوى المهارة الذي تم تقييمه أم لا. |
| **الحقل الأساسي**<br>mshr_primaryfield<br>*سلسلة* | للقراءة فقط<br>مطلوب | حقل المطلوب استخدامه كمعرف لسجل الكيان. مجموعة رقم الطرف ونوع المستوى ومعرف المهارة وتاريخ المستوى. |

## <a name="see-also"></a>راجع أيضًا

[مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب](hr-admin-integration-ats-api-introduction.md)<br>
[مثال الاستعلام عن مرشح مراد توظيفه](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
