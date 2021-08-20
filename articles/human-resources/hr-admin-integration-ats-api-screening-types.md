---
title: أنواع المراقبة
description: يصف هذا الموضوع كيان أنواع المراقبة لـ Dynamics 365 Human Resources.
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
ms.openlocfilehash: a7e726f88eb5c00fef98256de7a8f924156ba8f52392bc4dc6ae6e7914227152
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782158"
---
# <a name="screening-types"></a>أنواع المراقبة

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا الموضوع كيان أنواع المراقبة لـ Dynamics 365 Human Resources.

الاسم الفعلي: mshr_hcmscreeningtypeentity

## <a name="description"></a>الوصف

يصف هذا الكيان أنواع عمليات المراقبة التي قامت الشركة بإعدادها لعمليات مراقبة التوظيف المسبق والمستمر.

## <a name="json-representation"></a>تمثيل JSON

```json
{
    "mshr_description": "String",
    "mshr_frequencyunit": Int,
    "mshr_generatefrom": Int,
    "mshr_frequencyinterval": Int,
    "mshr_screeningtypeid": "String",
    "mshr_hcmscreeningtypeentityid": "Guid"
}
```

## <a name="properties"></a>الخصائص

| الخاصية<br>**الاسم الفعلي**<br>**_النوع_** | استخدام | الوصف |
| --- | --- | --- |
| **معرف كيان نوع المراقبة**<br>mshr_hcmscreeningtypeentityid<br>*GUID* | للقراءة فقط<br>مطلوب<br>منشأ بواسطة النظام | المعرف الأساسي الفريد لسجل نوع المراقبة. |
| **معرف نوع المراقبة**<br>mshr_screeningtypeid<br>*سلسلة* | قراءة/كتابة<br>مطلوب | المعرف الفريد المحدد بواسطة المستخدم لنوع المراقبة. |
| **‏‏الوصف**<br>mshr_description<br>*سلسلة* | قراءة/كتابة<br>مطلوب | وصف نوع المراقبة. |
| **وحدة التكرار**<br>mshr_frequencyunit<br>*مجموعة خيارات mshr_hcmfrequencyunit* | قراءة/كتابة<br>مطلوب | يصف التكرار الذي يجب أن تكتمل معه المراقبة للشخص المعين. |
| **إنشاء من**<br>mshr_generatefrom<br>*مجموعة خيارات mshr_hcmfrequencygeneratefrom* | قراءة-كتابة<br>مطلوب | إذا كانت قيمة التكرار هي أي قيمة بخلاف "مرة واحدة فقط" ، تحدد القيمة GenerateFrom التاريخ الذي يتم منه حساب حدث المراقبة التالي. |
| **فاصل التكرار**<br>mshr_frequencyinterval<br>*عدد صحيح* | قراءة-كتابة<br>مطلوب | إذا كانت قيمة التكرار هي أي قيمة خلاف "مرة واحدة فقط" ، فيجب عليك تحديد فاصل زمني لوحدات الوقت بين كل حدث من أحداث المراقبة. |

## <a name="see-also"></a>راجع أيضًا

[مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب](hr-admin-integration-ats-api-introduction.md)<br>
[مثال الاستعلام عن مرشح مراد توظيفه](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]