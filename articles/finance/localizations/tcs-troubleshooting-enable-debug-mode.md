---
title: تمكين وضع التصحيح في خدمة حساب الضرائب
description: توضح هذه المقالة كيفية تمكين وضع التصحيح في خدمة حساب الضرائب لفحص المشكلات.
author: hangwan
ms.date: 03/25/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: ''
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 03/23/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 2bb381939ebe32cb51caf730cdd441557d83a4c0
ms.sourcegitcommit: 088a7b5eb9a3b68710dfe012abf4c24776978750
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/01/2022
ms.locfileid: "9620888"
---
# <a name="enable-debug-mode-in-the-tax-calculation-service"></a>تمكين وضع التصحيح في خدمة حساب الضرائب

[!include [banner](../includes/banner.md)]

توضح هذه المقالة كيفية تمكين وضع التصحيح في خدمة حساب الضرائب لفحص المشكلات.

1. أضف **&debug=vs%2CconfirmExit&** إلى عنوان URL لخادم كائن التطبيق، ثم قم بتحديث الصفحة.
2. عندما تحدد **ضريبة المبيعات** لحساب ضريبة المبيعات، يفتح ملف يسمى **TaxServiceTroubleshootingLog.txt**. يحتوي الملف **TaxServiceTroubleshootingLog.txt** على **TaxableDocument** ومعلمة الحساب. يتم إرجاع هذه النتائج من خدمة الضرائب ومعلومات الاستثناء لاستكشاف الأخطاء وإصلاحها.

## <a name="sample"></a>عينة

```json
===============================Tax service calculation input JSON:=====================================
{
    "TaxableDocument": {
    "Header": [
        {
        "Lines": [
            {
            "Transaction Line ID": "5816,68719677391",
            ...
            }
        ],
        "Transaction Header ID": "2022,68719506302",
        ...
        }
    ]
    },
    "Parameter": {
    "ContinueOnErrors": true,
    ...
    },
    "Adjustment": {
    "Lines": {}
    }
}
===========================Tax service calculation result JSON:=================================
{
    "taxDocument": {
    "Header": [
        {
        "Lines": [
            {
            "Tax Codes": {
                ...
            }
        ],
        "Measures": {
            "List Code": "EUTrade"
        },
        "Tax Registration ID": null,
        "Transaction Header ID": "2022,68719506302",
        "Errors": null
        }
    ]
    },
    "solutionId": "b51e0025-cbbe-4d37-bf0b-90d7be4f214d|1",
    "isPartialSuccess": false
}
=============================CorrelationId:==============================
"21f3a8a1-ee9a-477b-b44e-b8ec79e74d16"
```

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
