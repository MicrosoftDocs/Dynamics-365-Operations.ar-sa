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
ms.openlocfilehash: 128caead04cf467c65a50bc6cd2f9e76e318f536b7eafa7972ffc1b5da5bceba
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738833"
---
# <a name="missing-field-settings-when-item-model-groups-are-copied-to-another-legal-entity"></a>إعدادات الحقل المفقودة عند نسخ مجموعات نماذج الأصناف إلى كيان قانوني آخر

رقم KB: 4612800

## <a name="symptoms"></a>العلامات

عند نسخ مجموعات نماذج الأصناف إلى كيان قانوني آخر (الشركة) باستخدام الكيان *سياسات مخزون مجموعة طراز الصنف*، فإن بعض إعدادات الحقول (على سبيل المثال، نموذج المخزون والوصف) تكون مفقودة في مجموعة النماذج الجديدة في الكيان القانوني للوجهة.

## <a name="resolution"></a>الدقة

لإنشاء نسخة كاملة من مجموعة نماذج صنف لكيان قانوني آخر، يجب أيضًا تحديد كل من سياسات مخزون مجموعة نموذج الصنف (`InventInventoryPolicyEntity`) وسياسات افتراضات تدفق التكلفة (`InventCostFlowAssumptionPolicyEntity`) المرتبطة بمجموعة نماذج الأصناف.
