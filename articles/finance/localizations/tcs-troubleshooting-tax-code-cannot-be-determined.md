---
title: لا يمكن تحديد كود الضريبة
description: توضح هذه المقالة كيفية استكشاف خطأ "لا يمكن تحديد كود الضريبة" وإصلاحه في خدمة حساب الضرائب‬.
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
ms.openlocfilehash: 6a74724de38cf362900277ab9addc8e6894f7689
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877848"
---
# <a name="tax-code-cannot-be-determined"></a>لا يمكن تحديد كود الضريبة

[!include [banner](../includes/banner.md)]

توضح هذه المقالة خطوات استكشاف الأخطاء وإصلاحها إذا تلقيت رسالة الخطأ "لا يمكن تحديد كود الضريبة" في خدمة حساب الضرائب‬.

## <a name="symptom"></a>العَرَضْ

تتلقى رسالة الخطأ التالية: "الرأس/البنود - 1، لا يمكن تحديد كود الضريبة." أو، يمكنك العثور على الخطأ في ملف استكشاف الأخطاء وإصلاحها، كما هو موضح في المثال التالي. لمزيد من المعلومات، راجع [‏‫تمكين وضع التصحيح لاستكشاف الأخطاء وإصلاحها‬](tcs-troubleshooting-enable-debug-mode.md).

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
                                "Code": "TaxSetup20001",
                                "Message": "Header/Lines - 1, tax code cannot be determined."
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

قد تحدث هذه المشكلة بسبب عدم تقاطع مجموعة الضرائب ومجموعة ضرائب الأصناف.

## <a name="troubleshoot"></a>استكشاف الأخطاء وإصلاحها‬

اتبع هذه الخطوات لاستكشاف المشكلة وإصلاحها.

1. في ملف استكشاف الأخطاء وإصلاحها، تحقق من تحديد مجموعة الضرائب ومجموعة ضرائب الأصناف. إذا كانت القيم في **مجموعة الضرائب** و **مجموعة ضرائب الأصناف** فارغة، فهذا يعني عدم تحديد مجموعة الضرائب ومجموعة ضرائب الأصناف. إذا تم تحديدها، فقد تكون النتائج غير صحيحة.

    فيما يلي مثال عن ملف استكشاف الأخطاء وإصلاحها.

    ```json
    ======================Tax service calculation result JSON:===========================
    {
        "taxDocument": {
            "Header": [
                {
                    "Lines": [
                        {
                            "Tax Codes": {},
                            "Measures": {
                                "Tax Group": "Group A",
                                "Item Tax Group": "Group B"
                            },
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

2. تحقق من تمكين **تجاوز ضريبة المبيعات‬** على علامة تبويب **الإعداد** لتفاصيل بنود أمر المبيعات.

    - إذا تم تمكين هذا الخيار، فيتم تحديد أكواد الضريبة بواسطة قيم **مجموعة الضرائب** و **مجموعة ضرائب الأصناف** التي تقوم بإدخالها في بند الحركة. تحقق من إدخال هذه القيم بشكل صحيح.
    - إذا لم يتم تمكين هذا الخيار، فتحقق من تعيين القيم الصحيحة للحقلين **قابلية تطبيق المجموعة الضريبية** و **قابلية تطبيق مجموعة ضرائب الأصناف‬‏‫**. لمزيد من المعلومات، راجع [لم يتم العثور على نتيجة مطابقة‬](tcs-troubleshooting-no-matching-result.md).

3. إذا تم تحديد مجموعة الضرائب ومجموعة ضرائب الأصناف بشكل صحيح، حدد ما إذا كانت هناك أي تقاطع لها.

    1. في RCS، انتقل إلى **ميزات الضريبة‬** \> **أكواد الضرائب ومجموعات الضرائب‬** \> **مجموعة الضرائب‬**.

        | مجموعة Line.Tax | أكواد الضرائب |
        |----------------|-----------|
        | المجموعة A        | أ         |

    2. انتقل إلى **ميزات الضريبة‬** \> **أكواد الضرائب ومجموعات الضرائب‬** \> **مجموعة ضرائب الأصناف‬**.

        | مجموعة الضرائب Line.Item | أكواد الضرائب |
        |---------------------|-----------|
        | المجموعة ب             | B         |

    في حالة عدم وجود تقاطع لمجموعة الضرائب الضريبة ومجموعة ضرائب الأصناف، فلن يتم تحديد كود الضريبة.

## <a name="mitigation"></a>تخفيف المخاطر

1. تنقل عبر كل خطوة في قسم [استكشاف الأخطاء وإصلاحها](#troubleshoot) في هذه المقالة، واعمل على إعداد الإصلاح كما تقتضي الحاجة. إذا لم يتم تحديد مجموعة الضرائب ومجموعة ضرائب الأصناف بشكل صحيح، فراجع [لم يتم العثور على نتيجة مطابقه](tcs-troubleshooting-no-matching-result.md).
2. في حال عدم وجود تقاطع لمجموعة الضرائب ومجموعة ضرائب الأصناف، فأنشئ إصدارًا جديدًا للميزة في RCS، ثم اعمل على إصلاح الإعداد.

    - انتقل إلى **ميزات الضريبة** \> **أكواد الضرائب ومجموعات الضرائب** > **مجموعة ضرائب الأصناف**.

        | مجموعة الضرائب Line.Item | الأكواد الضريبية |
        |---------------------|-----------|
        | المجموعة ب             | A;B       |

    سيتحدد كود الضريبة باعتباره **A**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
