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
ms.openlocfilehash: eae703ce0b2c981518b18c4badd4f90031b902ece62f3ca0837427b306d618b1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731093"
---
# <a name="canceled-product-receipts-dont-update-transaction-status-to-registered"></a>لا تعمل إيصالات استلام المنتجات الملغية على تحديث حالة الحركة إلى مسجل

## <a name="symptoms"></a>العلامات

بعد أن تقوم بتشغيل إجراء **إلغاء إيصالات استلام المنتجات** في حمل العمل الوارد، يقوم النظام تلقائيًا بتحديث حالة حركة المخزون من *تم الاستلام* إلى *مطلوب*.

## <a name="resolution"></a>الحل

عند إلغاء إيصالات التعبئة لأحمال العمل الواردة، تظل حالة حركات المخزون *منتقى*. ومع ذلك، عندما يتم إلغاء إيصالات استلام المنتجات من حمل العمل الوراد، لا يتم استعادة حالة حركات المخزون إلى *مسجل*. لذلك، بعد إلغاء إيصال استلام المنتجات من حمل العمل الوارد، يجب أن يقوم عامل المستودع بإعادة تسجيل كميات الأصناف لأحمال العمل.

لمزيد من المعلومات، راجع [تسجيل كميات الأصناف التي تصل إلى حمل العمل الوارد](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).
