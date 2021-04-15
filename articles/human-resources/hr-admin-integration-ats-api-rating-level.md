---
title: مستوى التقييم
description: يصف هذا الموضوع كيان مستوى التقييم لـ Dynamics 365 Human Resources.
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
ms.openlocfilehash: eac80599de07a045aa233f1cdfd16fe0db8733a2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800323"
---
# <a name="rating-level"></a>مستوى التقييم

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا الموضوع كيان مستوى التقييم لـ Dynamics 365 Human Resources.

الاسم الفعلي: mshr_hcmratinglevelentity

## <a name="description"></a>الوصف

يوفر هذا الكيان مستويات التقييم المتاحة للمهارات. تنطبق مستويات التصنيف عبر كافة الكيانات القانونية.

## <a name="json-representation"></a>تمثيل JSON

```json
{
    "mshr_description": "String",
    "mshr_factor": Int,
    "mshr_note": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_ratingmodelentity_id_value": "Guid",
    "mshr_hcmratinglevelentityid": "Guid"
}
```

## <a name="properties"></a>الخصائص

| الخاصية<br>**الاسم الفعلي**<br>**_النوع_** | استخدام | الوصف |
| --- | --- | --- |
| **معرف كيان مستوى التقييم**<br>mshr_hcmratinglevelentityid<br>*GUID* | للقراءة فقط<br>مطلوب<br>منشأ بواسطة النظام | معرف فريد منشأ بواسطة النظام للمستوى. |
| **معرف مستوى التقييم**<br>mshr_ratinglevelid<br>*سلسلة* | قراءة/كتابة<br>مطلوب | معرف فريد قابل للقراءة بواسطة المستخدم للمستوى. |
| **معرف نموذج التقييم**<br>mshr_ratingmodelid<br>*سلسلة* | قراءة/كتابة<br>مطلوب | نموذج التقييم الذي ينتمي إليه مستوى التقييم. |
| **معرف كيان نموذج التقييم**<br>_mshr_fk_ratingmodelentity_id_value<br>*GUID* | للقراءة فقط<br>مطلوب<br>المفتاح الخارجي: mshr_hcmratingmodelentityid لـ mshr_hcmratingmodelentity | المعرف المنشأ بواسطة النظام لنموذج التقييم الذي ينتمي إليه مستوى التقييم. |
| **‏‏الوصف**<br>mshr_description<br>*سلسلة* | قراءة/كتابة<br>مطلوب | الوصف الخاص بمستوى التقييم. |
| **العامل‬**<br>mshr_factor<br>*عدد صحيح* | قراءة/كتابة<br>مطلوب | العامل لمستوى التقييم. وعندما تقوم بمقارنة الأصناف برقم مختلف لمستويات التقييم، يتم استخدام العامل لتسوية النتائج. يجب أن تكون القيمة عددًا صحيحًا بين 0 و9. |
| **ملاحظة**<br>mshr_note<br>*سلسلة* | قراءة/كتابة<br>اختياري | أية ملاحظات مرتبطة بمستوى التقييم. |
| **الحقل الأساسي**<br>mshr_primaryfield<br>*سلسلة* | للقراءة فقط<br>مطلوب | حقل المطلوب استخدامه كمعرف لسجل الكيان. مجموعة معرف مستوى التقييم ومعرف نموذج التقييم. |

## <a name="see-also"></a>راجع أيضًا

[مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب](hr-admin-integration-ats-api-introduction.md)<br>
[مثال الاستعلام عن مرشح مراد توظيفه](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]