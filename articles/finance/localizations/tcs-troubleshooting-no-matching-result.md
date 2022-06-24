---
title: تعذر العثور على نتيجة مطابقة
description: توضح هذه المقالة كيفية استكشاف خطأ "لم يتم العثور على نتيجة مطابقة" وإصلاحه في خدمة حساب الضرائب‬.
author: hangwan
ms.date: 03/25/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 03/23/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: d3bbc76741fdd018d1b2987538b8de7f6d92ee53
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845133"
---
# <a name="no-matching-result-could-be-found"></a>تعذر العثور على نتيجة مطابقة

[!include [banner](../includes/banner.md)]

توضح هذه المقالة خطوات استكشاف الأخطاء وإصلاحها إذا تلقيت رسالة خطأ "لم يتم العثور على نتيجة مطابقة" في خدمة حساب الضرائب‬.

## <a name="symptom"></a>العَرَضْ

تلقيت رسالة الخطأ التالية: "الرأس/البنود - 1، مجموعة الضرائب، لم يتم العثور على نتيجة مطابقة."

```json
======================Tax service calculation result JSON:===========================
{
    "taxDocument": {
        "Header": [
            {
                "Lines": [
                    {
                        ...
                        "Errors": [
                            {
                                "Code": "TaxSetup20000",
                                "Message": "Header/Lines - 1, Tax group applicability, no matching result could be found."
                            }
                        ],
                        "Adjustment": null
                    }
                ],
                "Measures": {
                    ...
                },
                ...
            }
        ]
    },
    ...
}
```

## <a name="cause"></a>السبب

تحدث هذه المشكلة عندما لا يكون إعداد الميزة في Regulatory Configuration Service (RCS) صحيحًا.

## <a name="troubleshoot"></a>استكشاف الأخطاء وإصلاحها‬

1. قم بتنزيل ملف استكشاف الأخطاء وإصلاحها. لمزيد من المعلومات، راجع [‏‫تمكين وضع التصحيح لاستكشاف الأخطاء وإصلاحها‬](tcs-troubleshooting-enable-debug-mode.md).
2. قارن بين إدخال حساب خدمة الضرائب وإعداد الميزة لحل مشكلة الإعداد.

    يوضح المثال التالي إدخال حساب خدمة الضرائب.

    ```json
    ===============================Tax service calculation input JSON:=====================================
    {
        "TaxableDocument": {
            "Header": [
                {
                    "Lines": [
                        {
                            ...
                        }
                    ],
                    "Business Process": "Sales",
                    "Ship From Zip Code": "30159",
                }
            ]
        },
        "Parameter": {
            ...
        },
        "Adjustment": {
            "Lines": {}
        }
    }
    ```

    يسرد الجدول التالي قابلية تطبيق مجموعة الضرائب في RCS.

    | عملية Header.Business | وحدة Lines.Business | Header.Ship من Zip Code | مجموعة الضريبة |
    |-------------------------|---------------------|---------------------------|-----------|
    | دفتر اليومية                 |                     |                           | المجموعة A   |
    | المبيعات                   |                     | 30160                     | المجموعة ب   |

    وفقًا لإدخال حساب الضرائب، فإن قيمة **دورة العمل** على الرأس هي **المبيعات**، وقيمة **الشحن من الرمز البريدي** على الرأس هي **30159**. يستند هذا الإدخال إلى إعداد قواعد قابلية التطبيق في RCS. وبسبب عدم وجود بند مطابق، يحدث هذا الخطأ.

    > [!NOTE]
    > إذا كانت القيمة الموجودة في قاعدة قابلية التطبيق فارغة، فإن القاعدة تنطبق على أي قيمة.

## <a name="mitigation"></a>تخفيف المخاطر

اتبع الخطوات التالية لتخفيف مخاطر الخطأ.

1. في RCS، انتقل إلى **ميزات العولمة** \> **حساب الضريبة**.
2. أنشئ إصدارًا جديدًا من الميزة.
3. أضف بندًا للمعلومات المناظرة.

    | عملية Header.Business | وحدة Lines.Business | Header.Ship من Zip Code| مجموعة الضريبة |
    |-------------------------|---------------------|--------------------------|-----------|
    | دفتر اليومية                 |                     |                          | المجموعة A   |
    | المبيعات                   |                     | 30160                    | المجموعة ب   |
    | المبيعات                   |                     | 30159                    | المجموعة ب   |

4. انشر إصدار إعداد الميزة.
5. في Microsoft Dynamics 365 Finance، انتقل إلى **الضريبة** \> **الإعداد‏‎** \> **تكوين الضريبة** \> **معلمات حساب الضرائب**، وحدد الإصدار الجديد.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
