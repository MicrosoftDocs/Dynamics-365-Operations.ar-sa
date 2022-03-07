---
title: إعدادات الحقل المفقودة عند نسخ مجموعات نماذج الأصناف إلى كيان قانوني آخر
description: إعدادات الحقل مفقودة عند نسخ مجموعات نموذج الأصناف إلى كيان قانوني آخر.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f6fdfef0bc377418ed8a9c8830e74526a0b95eb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026230"
---
# <a name="missing-field-settings-when-item-model-groups-are-copied-to-another-legal-entity"></a>إعدادات الحقل المفقودة عند نسخ مجموعات نماذج الأصناف إلى كيان قانوني آخر

رقم KB: 4612800

## <a name="symptoms"></a>العلامات

عند نسخ مجموعات نماذج الأصناف إلى كيان قانوني آخر (الشركة) باستخدام الكيان *سياسات مخزون مجموعة طراز الصنف*، فإن بعض إعدادات الحقول (على سبيل المثال، نموذج المخزون والوصف) تكون مفقودة في مجموعة النماذج الجديدة في الكيان القانوني للوجهة.

## <a name="resolution"></a>الدقة

لإنشاء نسخة كاملة من مجموعة نماذج صنف لكيان قانوني آخر، يجب أيضًا تحديد كل من سياسات مخزون مجموعة نموذج الصنف (`InventInventoryPolicyEntity`) وسياسات افتراضات تدفق التكلفة (`InventCostFlowAssumptionPolicyEntity`) المرتبطة بمجموعة نماذج الأصناف.
