---
title: نوع الشهادة
description: يصف هذا الموضوع كيان نوع المرشح لـ Dynamics 365 Human Resources.
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
ms.openlocfilehash: cc8f49be9af3f95ba182e1e0f1b288334a959ec40315b319a73feff3dbb3fdc6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771553"
---
# <a name="certificate-type"></a>نوع الشهادة

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا الموضوع كيان نوع المرشح لـ Dynamics 365 Human Resources.

الاسم الفعلي: mshr_hcmcertificatetypeentity

## <a name="description"></a>الوصف

يحدد هذا الكيان قائمة أنواع الشهادات المهنية التي تم إعدادها في الموارد البشرية. الكيان غير خاص بأحد الكيانات القانونية (الشركة).

## <a name="json-representation"></a>تمثيل JSON

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a>الخصائص

| الخاصية<br>**الاسم الفعلي**<br>**_النوع_** | استخدام | الوصف |
| --- | --- | --- |
| **معرف كيان نوع الشهادة**<br>mshr_hcmcertificatetypeentityid<br>*GUID* | للقراءة فقط<br>مطلوب 
منشأ بواسطة النظام | المعرف الرئيسي الفريد لنوع الشهادة. |
| **نوع الشهادة**<br>mshr_certificatetype<br>*سلسلة* | قراءة/كتابة<br>مطلوب | معرف فريد قابل للقراءة بواسطة المستخدم لنوع الشهادة. |
| **‏‏الوصف**<br>mshr_description<br>*سلسلة* | قراءة/كتابة<br>مطلوب | وصف نوع الشهادة. |
| **يتطلب التجديد**<br>mshr_requirerenewal<br>*مجموعة خيارات mshr_noyes* | قراءة/كتابة<br>اختياري | يشير إلى ما إذا كان التجديد مطلوبًا للشهادة أم لا. |

## <a name="see-also"></a>راجع أيضًا

[مقدمة واجهة برمجة التطبيقات لتكامل نظام تعقب مقدم الطلب](hr-admin-integration-ats-api-introduction.md)<br>
[مثال الاستعلام عن مرشح مراد توظيفه](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]