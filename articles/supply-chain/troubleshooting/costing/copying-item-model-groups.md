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
# <a name="missing-field-settings-when-item-model-groups-are-copied-to-another-legal-entity"></a><span data-ttu-id="f010d-103">إعدادات الحقل المفقودة عند نسخ مجموعات نماذج الأصناف إلى كيان قانوني آخر</span><span class="sxs-lookup"><span data-stu-id="f010d-103">Missing field settings when item model groups are copied to another legal entity</span></span>

<span data-ttu-id="f010d-104">رقم KB: 4612800</span><span class="sxs-lookup"><span data-stu-id="f010d-104">KB number: 4612800</span></span>

## <a name="symptoms"></a><span data-ttu-id="f010d-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="f010d-105">Symptoms</span></span>

<span data-ttu-id="f010d-106">عند نسخ مجموعات نماذج الأصناف إلى كيان قانوني آخر (الشركة) باستخدام الكيان *سياسات مخزون مجموعة طراز الصنف*، فإن بعض إعدادات الحقول (على سبيل المثال، نموذج المخزون والوصف) تكون مفقودة في مجموعة النماذج الجديدة في الكيان القانوني للوجهة.</span><span class="sxs-lookup"><span data-stu-id="f010d-106">When you copy item model groups to another legal entity (company) by using the *Item model group inventory policies* entity, some field settings (for example, the inventory model and description) are missing in the new model group in the destination legal entity.</span></span>

## <a name="resolution"></a><span data-ttu-id="f010d-107">الدقة</span><span class="sxs-lookup"><span data-stu-id="f010d-107">Resolution</span></span>

<span data-ttu-id="f010d-108">لإنشاء نسخة كاملة من مجموعة نماذج صنف لكيان قانوني آخر، يجب أيضًا تحديد كل من سياسات مخزون مجموعة نموذج الصنف (`InventInventoryPolicyEntity`) وسياسات افتراضات تدفق التكلفة (`InventCostFlowAssumptionPolicyEntity`) المرتبطة بمجموعة نماذج الأصناف.</span><span class="sxs-lookup"><span data-stu-id="f010d-108">To create a complete copy of an item model group to another legal entity, you must also select both the item model group inventory policies (`InventInventoryPolicyEntity`) and the cost flow assumption policies (`InventCostFlowAssumptionPolicyEntity`) that are associated with the item model group.</span></span>
