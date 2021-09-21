---
title: لا يتم ملء مجموعة الضريبة الافتراضية والخصم النقدي من حساب الفاتورة
description: لا يتم ملء مجموعة الضرائب الافتراضية والخصم النقدي الافتراضي من حساب الفاتورة
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: bb984eb17209dc92e336df5ad475bb0f70c6e35c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475465"
---
# <a name="default-tax-group-and-cash-discount-arent-filled-in-from-the-invoice-account"></a>لا يتم ملء مجموعة الضريبة الافتراضية والخصم النقدي من حساب الفاتورة

## <a name="symptoms"></a>العلامات

إذا كنت تستخدم حساب فاتورة يختلف عن حساب العميل، فلن يتم ملء مجموعة الضرائب الافتراضية والخصم النقدي الافتراضي من حساب الفاتورة عند إنشاء أمر شراء.

## <a name="resolution"></a>الحل

يتم هذا السلوك بسبب التصميم. تعتمد القيم الافتراضية لمجموعة الضرائب والخصومات النقدية ومعلومات السعر الأخرى إلى حساب العميل، وليس حساب الفاتورة.
