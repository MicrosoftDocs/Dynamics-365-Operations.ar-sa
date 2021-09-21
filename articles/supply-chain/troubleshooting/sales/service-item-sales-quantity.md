---
title: لا يمكن تعيين كمية صنف خدمة في بند عرض أسعار المبيعات
description: عند العمل مع عروض أسعار المبيعات، لا يمكنك تعيين كمية مبيعات للمنتجات التي تكون أصناف خدمة، نظراً لعدم وجود أصناف فعلية لجردها.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea0f8f246e95f90b6ac5e78ee63950c9ca836a0e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475513"
---
# <a name="cant-change-the-sales-quantity-of-a-service-item-on-a-sales-quotation-line"></a>لا يمكن تغيير كمية المبيعات لصنف خدمة في بند عرض أسعار المبيعات

## <a name="symptoms"></a>العلامات

إذا حاولت تعيين كمية مبيعات (الحقل **SalesQty**) لصنف من النوع *خدمة* على بند عرض أسعار مبيعات، ستتلقى الرسالة التالية:

> التحديث غير مسموح لحقل الكمية.

## <a name="cause"></a>السبب

يتم هذا بسبب التصميم. لا يمكنك تعيين كمية مبيعات للمنتجات التي تعد أصناف خدمة. على سبيل المثال، إذا قمت بتقديم خدمة لتثبيت صنف، فلا يكون هذا الأمر منطقيًا لتسجيل كمية، بسبب عدم وجود صنف فعلي ليتم جرده. توجد خدمة فقط.
