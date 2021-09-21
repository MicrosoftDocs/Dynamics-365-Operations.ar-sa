---
title: غير مسموح بمالك المخزون عند معالجة الحركات
description: قد تتلقي الخطأ، "مالك المخزون غير %1 مسموح به". تدعم عمليات إدارة المستودع المخزون الذي يملكه الكيان القانوني فقط.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4ee29cfc7bad990cd1ee5deaa98fca217af772ed
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475448"
---
# <a name="inventory-owner-not-allowed-when-processing-movements-in-the-warehouse-app"></a>غير مسموح بمالك المخزون عند معالجة الحركات في تطبيق المستودع

## <a name="symptoms"></a>العلامات

عند معالجة الحركات في تطبيق Warehouse Management للأجهزة المحمولة، قد تستلم رسالة الخطأ التالية:

> غير مسموح بمالك المخزون %1 في هذه العملية.

## <a name="cause"></a>السبب

وهذا يحدث لأن بعد تتبع **المالك** يكون مفقودًا عند استخدام تطبيق Warehouse Management للأجهزة المحمولة لعمل الحركات. يظهر دفتر يوميه تحويل المخزون العادي من عميل Supply Chain Management للعمل كما يجب ولا يمكن ترحيله الا إذا تم ملء بعد **المالك**.

## <a name="resolution"></a>الحل

قامت Microsoft بتقييم هذه المشكلة وقامت بتحديد انها قيد ميزه. تدعم عمليات أداره المستودع حاليا المخزون الذي يملكه الكيان القانوني فقط.
