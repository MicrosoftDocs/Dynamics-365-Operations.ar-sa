---
title: لا يمكنك إعادة إصدار حمل عمل تم شحنه جزئيا للمستودع
description: في الإصدارات السابقة، تعذر عليك إعادة إصدار حمل عمل تم شحنه جزئياً عند استخدام وظائف معينة بعمليات حجز غير مكتملة. تم إصلاح هذا الأمر.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0380e1963a38f2be55b31e06b3845f935661eed2
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475489"
---
# <a name="cant-re-release-a-partially-shipped-load-to-the-warehouse"></a>لا يمكنك إصدار تحميل تم شحنه جزئيا للمستودع

## <a name="symptoms"></a>العلامات

لا يمكنك إصدار تحميل تم شحنه جزئيا للمستودع. عند القيام بالإصدار على المستودع ، تظهر رسالة "اكتملت العملية"، ولكن لا يحدث شيء ، ولا يتم إنشاء أي عمل للكمية المتبقية. تحدث هذه المشكلة عند استخدام وظيفة تحميل النقل ووجود حجز غير مكتمل.

## <a name="resolution"></a>الحل

[مشكلة قاعدة المعارف 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("يمكن أعاده إنشاء موجات لعمليات التحميل التي تم شحنها جزئيا وأعاده معالجتها") تم إصلاحها في [الإصدار 10.0.15](/dynamics365/supply-chain/get-started/whats-new-scm-10-0-15).
