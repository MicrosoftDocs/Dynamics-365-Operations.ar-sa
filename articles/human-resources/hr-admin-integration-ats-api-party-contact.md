---
title: جهة اتصال الطرف
description: يصف هذا الموضوع كيان جهة اتصال الطرف لـ Dynamics 365 Human Resources.
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
ms.openlocfilehash: fe25e37025a9f7945121a2a999c164a273e803fed750cc258e1ad30e33fc709b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6727175"
---
# <a name="party-contact"></a>جهة اتصال الطرف

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا الموضوع كيان جهة اتصال الطرف لـ Dynamics 365 Human Resources.

الاسم الفعلي: mshr_dirpartycontactentities

## <a name="description"></a>الوصف

ويصف هذا الكيان معلومات جهة الاتصال الخاصة بالمرشح، بما في ذلك الهاتف والبريد الإلكتروني وحسابات التواصل الاجتماعي.

## <a name="json-representation"></a>تمثيل JSON

```json
{
    "mshr_partynumber": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_type": Int,
    "mshr_countryregioncode": "String",
    "mshr_locator": "String",
    "mshr_locatorextension": "String",
    "mshr_purpose": "String",
    "mshr_ismobilephone": Int,
    "mshr_isinstantmessage": Int,
    "mshr_isprimary": Int,
    "mshr_isprivate": Int,
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "String",
    "mshr_dirpartycontactentityid": "String"
}
```

## <a name="properties"></a>الخصائص

| الخاصية<br>**الاسم الفعلي**<br>**_النوع_** | استخدام | الوصف |
| --- | --- | --- |
| **معرف كيان وحدة الاتصال بالطرف**<br>mshr_dirpartycontactentityid<br>*سلسلة* | للقراءة فقط<br>مطلوب | معرف فريد منشأ بواسطة النظام لسجل الكيان. |
| **رقم الطرف**<br>mshr_partynumber<br>*سلسلة* | قراءة/كتابة<br>مطلوب | معرف سجل الطرف المرتبط (الشخص). |
| **قيمة معرف الشخص**<br>_mshr_fk_person_id_value<br>*GUID* | للقراءة فقط<br>مطلوب<br>المفتاح الخارجي: mshr_dirpersonentityid لـ mshr_dirpersonentity | المعرف الفريد المنشأ بواسطة النظام لسجل كيان الطرف (الشخص). |
| **معرف الموقع**<br>mshr_locationid<br>*سلسلة* | قراءة/كتابة<br>مطلوب | معرف الموقع الخاص بسجل العنوان. الإعداد في كيان mshr_logisticspostaladdresslocationcdsentity. |
| **‏‏الوصف**<br>mshr_description<br>*سلسلة* | قراءة/كتابة<br>مطلوب | الوصف الخاص بتفاصيل جهة الاتصال. |
| **النوع**<br>mshr_type<br>*مجموعة الخيارات mshr_logisticselectronicaddressmethodtype* | قراءة/كتابة<br>مطلوب | نوع تفاصيل جهة الاتصال. |
| **كود البلد المنطقة**<br>mshr_countryregioncode<br>*سلسلة* | قراءة/كتابة<br>اختياري | بلد أو منطقة العنوان. |
| **محدد المواقع**<br>mshr_locator<br>*سلسلة* | قراءة/كتابة<br>اختياري | تفاصيل جهة الاتصال. على سبيل المثال، إذا كان النوع **عنوان بريد إلكتروني**، فسيحتوي هذا الحقل على عنوان البريد الإلكتروني الخاص بالمرشح. |
| **ملحق محدد الموقع**<br>mshr_locatorextension<br>*سلسلة* | قراءة/كتابة<br>اختياري | ملحق محدد الموقع. على سبيل المثال، إذا كان النوع **الهاتف**، فإن هذه الخاصية ستحتوي على ملحق رقم الهاتف. |
| **محمول**<br>mshr_ismobile<br>*مجموعة خيارات mshr_noyes* | قراءة/كتابة<br>مطلوب | تحديد ما إذا كان الهاتف رقم جوال أم لا. |
| **رسالة فورية**<br>mshr_isinstantmessage<br>*مجموعة خيارات mshr_noyes* | قراءة/كتابة<br>مطلوب | تحديد ما إذا كان الهاتف ممكّنا للمراسلة الفورية أم لا. |
| **رئيسي**<br>mshr_isprimary<br>*مجموعة خيارات mshr_noyes* | قراءة/كتابة<br>مطلوب | يحدد جهة الاتصال الرئيسية لنوع جهة الاتصال. يجب أن يكون هناك سجل أساسي واحد فقط لكل نوع جهة اتصال. |
| **خاص**<br>mshr_isprivate<br>*مجموعة خيارات mshr_noyes* | قراءة/كتابة<br>مطلوب | يحدد ما إذا كان هذا العنوان عبارة عن عنوان خاص للشخص أم لا. |
| **الغرض**<br>mshr_purpose<br>*سلسلة* | قراءة/كتابة<br>اختياري | الغرض/الدور لتفاصيل جهة الاتصال. |
| **الحقل الأساسي**<br>mshr_primaryfield<br>*سلسلة* | للقراءة فقط<br>مطلوب | حقل يستخدم كمعرف أساسي لسجل الكيان. مجموعة رقم الطرف والنوع والوصف ومحدد الموقع. |

## <a name="see-also"></a>راجع أيضًا

[مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب](hr-admin-integration-ats-api-introduction.md)<br>
[مثال الاستعلام عن مرشح مراد توظيفه](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]