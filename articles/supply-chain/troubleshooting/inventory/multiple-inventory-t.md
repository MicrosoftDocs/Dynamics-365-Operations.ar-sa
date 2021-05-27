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
# <a name="multiple-inventory-transactions-for-batch-numbers-when-on-physical-update-is-disabled"></a><span data-ttu-id="04d1b-103">الحركات المخزنية المتعددة لأرقام الدفعات عند تعطيل التحديث الفعلي</span><span class="sxs-lookup"><span data-stu-id="04d1b-103">Multiple inventory transactions for batch numbers when On physical update is disabled</span></span>

<span data-ttu-id="04d1b-104">رقم KB: 4613390</span><span class="sxs-lookup"><span data-stu-id="04d1b-104">KB number: 4613390</span></span>

## <a name="symptoms"></a><span data-ttu-id="04d1b-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="04d1b-105">Symptoms</span></span>

<span data-ttu-id="04d1b-106">يتم إنشاء العديد من حركات المخزون بعد تسوية سطر أمر الشراء للأصناف التي يتم فيها تعيين خيار **عند التحديث الفعلي** مجموعة رقم الدفعة على *لا*.</span><span class="sxs-lookup"><span data-stu-id="04d1b-106">Multiple inventory transactions are created after you adjust a purchase order line for items where the **On physical update** option of the batch number group is set to *No*.</span></span>

<span data-ttu-id="04d1b-107">عند إنشاء صنف حيث يتم تعيين الخيار **عند التحديث الفعلي** لمجموعة رقم الدفعة على *لا*، يقوم النظام تلقائيًا بإنشاء رقم دفعة جديد إذا قمت بتعديل كمية بند الشراء وحفظ صفحة أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="04d1b-107">When you create an item where the **On physical update** option of the batch number group is set to *No*, the system automatically creates a new batch number if you modify a purchase line quantity and save the purchase order page.</span></span>

## <a name="resolution"></a><span data-ttu-id="04d1b-108">الدقة</span><span class="sxs-lookup"><span data-stu-id="04d1b-108">Resolution</span></span>

<span data-ttu-id="04d1b-109">يعمل الإعداد **عند التحديث الفعلي** لمجموعات رقم الدفعة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="04d1b-109">The **On physical update** setting for batch number groups works in the following way:</span></span>

- <span data-ttu-id="04d1b-110">عند تعيين الخيار إلى *نعم*، يتم إنشاء أرقام الدفعات الجديدة فقط بعد تحديث فعلي (على سبيل المثال، عند شحن الأصناف أو استلامها).</span><span class="sxs-lookup"><span data-stu-id="04d1b-110">When the option is set to *Yes*, new batch numbers are created only after a physical update (for example, when items are shipped or received).</span></span>
- <span data-ttu-id="04d1b-111">عند تعيين الخيار على *لا*، يتم إنشاء رقم دفعة جديد في كل مرة يتم فيها إجراء تحديث قابل للتطبيق (على سبيل المثال، عند إضافة كمية جديدة إلى أمر شراء).</span><span class="sxs-lookup"><span data-stu-id="04d1b-111">When the option is set to *No*, a new batch number is created every time that an applicable update occurs (for example, when a new quantity is added to a purchase order).</span></span>
