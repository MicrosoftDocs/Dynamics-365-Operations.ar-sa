---
title: الحركات المخزنية المتعددة لأرقام الدفعات عند تعطيل التحديث الفعلي
description: يتم إنشاء العديد من حركات المخزون بعد تسوية سطر أمر الشراء للأصناف التي يتم فيها تعيين خيار عند التحديث الفعلي لمجموعة رقم الدفعة على لا.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventNumGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1fa54cdfdbc5608fb6c7114dced0f96bab47253e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026249"
---
# <a name="multiple-inventory-transactions-for-batch-numbers-when-on-physical-update-is-disabled"></a>الحركات المخزنية المتعددة لأرقام الدفعات عند تعطيل التحديث الفعلي

رقم KB: 4613390

## <a name="symptoms"></a>العلامات

يتم إنشاء العديد من حركات المخزون بعد تسوية سطر أمر الشراء للأصناف التي يتم فيها تعيين خيار **عند التحديث الفعلي** مجموعة رقم الدفعة على *لا*.

عند إنشاء صنف حيث يتم تعيين الخيار **عند التحديث الفعلي** لمجموعة رقم الدفعة على *لا*، يقوم النظام تلقائيًا بإنشاء رقم دفعة جديد إذا قمت بتعديل كمية بند الشراء وحفظ صفحة أمر الشراء.

## <a name="resolution"></a>الدقة

يعمل الإعداد **عند التحديث الفعلي** لمجموعات رقم الدفعة بالطريقة التالية:

- عند تعيين الخيار إلى *نعم*، يتم إنشاء أرقام الدفعات الجديدة فقط بعد تحديث فعلي (على سبيل المثال، عند شحن الأصناف أو استلامها).
- عند تعيين الخيار على *لا*، يتم إنشاء رقم دفعة جديد في كل مرة يتم فيها إجراء تحديث قابل للتطبيق (على سبيل المثال، عند إضافة كمية جديدة إلى أمر شراء).
