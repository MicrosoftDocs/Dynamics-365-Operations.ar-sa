---
title: لا تعمل إيصالات استلام المنتجات الملغية على تحديث حالة الحركة إلى مسجل
description: بعد إلغاء إيصالات استلام المنتجات في حمل العمل الوارد، يقوم النظام تلقائيًا بتحديث حالة حركة المخزون من تم الاستلام إلى مطلوب.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c86457d50a7a9ac2a699a0e0a9c7bdf4cd7c67b
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294000"
---
# <a name="canceled-product-receipts-dont-update-transaction-status-to-registered"></a>لا تعمل إيصالات استلام المنتجات الملغية على تحديث حالة الحركة إلى مسجل

## <a name="symptoms"></a>العلامات

بعد أن تقوم بتشغيل إجراء **إلغاء إيصالات استلام المنتجات** في حمل العمل الوارد، يقوم النظام تلقائيًا بتحديث حالة حركة المخزون من *تم الاستلام* إلى *مطلوب*.

## <a name="resolution"></a>الحل

عند إلغاء إيصالات التعبئة لأحمال العمل الواردة، تظل حالة حركات المخزون *منتقى*. ومع ذلك، عندما يتم إلغاء إيصالات استلام المنتجات من حمل العمل الوراد، لا يتم استعادة حالة حركات المخزون إلى *مسجل*. لذلك، بعد إلغاء إيصال استلام المنتجات من حمل العمل الوارد، يجب أن يقوم عامل المستودع بإعادة تسجيل كميات الأصناف لأحمال العمل.

لمزيد من المعلومات، راجع [تسجيل كميات الأصناف التي تصل إلى حمل العمل الوارد](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).
