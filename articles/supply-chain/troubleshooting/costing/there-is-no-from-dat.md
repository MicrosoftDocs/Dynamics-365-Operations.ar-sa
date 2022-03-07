---
title: لا توجد قيمة "من تاريخ" في علامة التبويب "الأسعار النشطة" لصفحة أسعار الأصناف
description: لا توجد قيمة "من تاريخ" في علامة التبويب "الأسعار النشطة" لصفحة أسعار الأصناف.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dd13f6a3e5ce3c894e96f420358d337f2e43dba
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026250"
---
# <a name="there-is-no-from-date-value-on-the-active-prices-tab-of-the-item-price-page"></a>لا توجد قيمة "من تاريخ" في علامة التبويب "الأسعار النشطة" لصفحة أسعار الأصناف

رقم KB: 4613548

## <a name="symptoms"></a>العلامات

لا توجد قيمة **من تاريخ** في علامة التبويب **الأسعار النشطة** للصفحة **سعر الصنف**.

## <a name="resolution"></a>الدقة

لا يتم تحويل القيمة **من تاريخ** (تاريخ السريان) التي تم تعيينها في السعر المعلق إلى السعر النشط.

وعندما يتم إدخال سجل تكلفة الصنف أولاً، يكون بحالة *معلق* وتاريخ سريان محدد. وعندما تقوم بتنشيط سجل تكاليف الصنف، يتم تحديث الحالة إلى *نشطة*، وتاريخ السريان إلى تاريخ التنشيط. وبالتالي، يكون تاريخ تنشيط السعر النشط دائمًا هو التاريخ الفعلي للتنشيط.

لمزيد من المعلومات، راجع [نظرة عامة حول إصدارات التكلفة](../../cost-management/costing-versions.md).
