---
title: لم تتم مزامنة اسم التسليم بعد تغيير عنوان تسليم أمر الشراء
description: بعد قيامك بتغيير عنوان التسليم على رأس أمر الشراء، لا تتم مزامنة اسم التسليم
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 588d1ef6250d249aa4fc9da4f5125e9a34c0255f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475440"
---
# <a name="the-delivery-name-isnt-synced-after-changing-a-purchase-order-delivery-address"></a>لم تتم مزامنة اسم التسليم بعد تغيير عنوان تسليم أمر الشراء

## <a name="symptoms"></a>العلامات

يتم تحديث العنوان الموجود على رأس أمر الشراء إلى عنوان ليس عنوان تسليم. علي الرغم من تحديث العنوان على أمر الشراء، لا يتم تحديث اسم التسليم استنادًا إلى العنوان المحدّث.

## <a name="resolution"></a>الحل

يتم هذا السلوك بسبب التصميم. يجب تصنيف العنوان المحدد كعنوان تسليم. وبخلاف ذلك، لا يتم تحديث اسم التسليم استنادًا إلى العنوان المحدد.
