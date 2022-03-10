---
title: لا يتم تحديث الكمية في أمر إدخال مخزن الفحص الذي تم بدؤه عند تقسيم الأمر
description: عند إنشاء أمر الفحص ومحاولة تقسيمه، لا يتم تحديث كمية الأمر إلى الكمية المتبقية التي يتم تقسيمها.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 4625570cb706199dca78f23b1864ca1d81cc66e896cf10d6d5f16cf1a9d1dc16
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713484"
---
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a>لا يتم تحديث الكمية في أمر إدخال مخزن الفحص الذي تم بدؤه عند تقسيم الأمر

رقم KB: 4613113

## <a name="symptoms"></a>العلامات

عند إنشاء أمر الفحص ومحاولة تقسيمه، لا يتم تحديث كمية الأمر إلى الكمية المتبقية بعد التقسيم.

## <a name="resolution"></a>الدقة

لا يقوم النظام بتغيير الكمية الأصلية من أمر فحص لضمان أنه يمكنك تعقب الكمية الأصلية التي تم إنشاؤها لأمر الفحص هذا. ومع ذلك، يقوم النظام بتعقب الكمية التي تم تقسيمها من أحد أوامر الفحص. لتنفيذ عملية التعقب هذه، يتم استخدام حقل قاعدة البيانات يسمي `QuantityThatHasSplitIntoOtherQuarantineOrders` ومع ذلك، هذا الحقل غير مرئي في واجهة المستخدم (UI).
