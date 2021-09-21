---
title: لا يتم تحديث معلومات الضريبة إذا تم تغيير موقع أمر المبيعات
description: إذا تم تغيير عنوان الموقع أو المستودع أو عنوان التسليم على رأس أمر المبيعات، فلن يتم تحديث معلومات ضريبة الحالة للبنود. يجب القيام بذلك يدوياً.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 77a73a787ff8a174c575f3b4f75694ded45d5712
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475476"
---
# <a name="tax-information-isnt-updated-if-location-on-a-sales-order-header-is-changed"></a>لا يتم تحديث معلومات الضريبة إذا تم تغيير الموقع في رأس أمر التوريد

## <a name="symptoms"></a>العلامات

إذا تم تغيير عنوان الموقع أو المستودع أو عنوان التسليم على رأس أمر المبيعات، فلن يتم تحديث معلومات ضريبة الحالة للبنود.

## <a name="resolution"></a>الحل

يتم هذا السلوك بسبب التصميم. تحدث المشكلة بسبب عدم تغيير عنوان التسليم والموقع والمستودع بشكل تلقائي على مستوى البنود. يجب تحديثها يدويًا.
