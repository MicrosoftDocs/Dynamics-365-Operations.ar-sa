---
title: تكرار دفع التعويض
description: يوفر هذا الموضوع تفاصيل ومثال استعلام لكيان تكرار دفع التعويض‬‏‫ في Dynamics 365 Human Resources.
author: marcelbf
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 171b7fb7b361bd1fe2e7e637cd555c88a81a8bcf
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066133"
---
# <a name="compensation-pay-frequency"></a>تكرار دفع التعويض


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا الموضوع كيان تكرار دفع التعويض‬‏‫ في Dynamics 365 Human Resources.

الاسم الفعلي: mshr_hcmpayrateconversionentity.

### <a name="description"></a>‏‏الوصف

يوفر هذا الكيان معلومات حول تحويل معدل الدفع لتكرار دفع تعويضات معين.

## <a name="properties"></a>الخصائص

| الخاصية</br>**الاسم الفعلي**</br>**_النوع_** | استخدام | ‏‏الوصف |
| --- | --- | --- |
| **تحويل معدل الدفع السنوي**</br>mshr_annualconversionfactor</br>*عشري* | للقراءة فقط | عامل التحويل السنوي لتكرار الدفع. |
| **‏‏الوصف**</br>mshr_description</br>*سلسلة* | للقراءة فقط | وصف معدل التحويل. |
| **تحويل معدل الدفع بالساعة**</br>mshr_hourlyconversionfactor</br>*عشري* | للقراءة فقط | عامل التحويل بالساعة لتكرار الدفع. |
| **تحويل معدل الدفع الشهري**</br>mshr_monthlyconversionfactor</br>*عشري* | للقراءة فقط | عامل التحويل الشهري لتكرار الدفع. |
| **تحويل ‏‫معدل الدفع**</br>mshr_payrateconversion</br>*سلسلة* | للقراءة فقط | سلسله فريدة لتعريف معدل التحويل. |
| **الفترة**</br>mshr_period</br>*مجموعة خيارات الفترة* | للقراءة فقط | الفترة الرئيسية لتحويل معدل الدفع المحدد. |
| **تحويل معدل الدفع الأسبوعي**</br>mshr_weeklyconversionfactor</br>*عشري* | للقراءة فقط | عامل التحويل الأسبوعي لتكرار الدفع. |
| **معرف منطقة البيانات**</br>mshr_dataareaid</br>*سلسلة* | للقراءة فقط | الكيان القانوني (الشركة). |
| **معرف كيان تكرار دفع التعويض**</br>mshr_dirpersonnamehistoricalentityid</br>*GUID* | النظام منشأ | قيمة معرف فريد عمومي (GUID) يقوم النظام بإنشائه لتعريف السجل بشكل فريد. |

## <a name="example-query-for-payroll-employee"></a>نموذج الاستعلام لموظف كشل الرواتب

**الطلب**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_hcmpayrateconversionentities?$filter=mshr_payrateconversion eq 'Annual' and mshr_dataareaid eq 'usmf'
```

**استجابة**

```json
{
    "mshr_annualconversionfactor": 1,
    "mshr_description": "Annual",
    "mshr_hourlyconversionfactor": 0.0004807692,
    "mshr_monthlyconversionfactor": 0.0833333333,
    "mshr_payrateconversion": "Annual",
    "mshr_period": 200000000,
    "mshr_weeklyconversionfactor": 0.0192307692,
    "mshr_dataareaid": "usmf",
    "mshr_hcmpayrateconversionentityid": "0000056e-0000-0000-b027-fef003000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>راجع أيضًا

[‏‫مقدمة إلى واجهة API لتكامل كشف الرواتب](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
