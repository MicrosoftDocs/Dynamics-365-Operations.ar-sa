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
ms.openlocfilehash: a8af535257ce217629d5ba92e624623c3ea39345
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026248"
---
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a>لا يتم تحديث الكمية في أمر إدخال مخزن الفحص الذي تم بدؤه عند تقسيم الأمر

رقم KB: 4613113

## <a name="symptoms"></a>العلامات

عند إنشاء أمر الفحص ومحاولة تقسيمه، لا يتم تحديث كمية الأمر إلى الكمية المتبقية بعد التقسيم.

## <a name="resolution"></a>الدقة

لا يقوم النظام بتغيير الكمية الأصلية من أمر فحص لضمان أنه يمكنك تعقب الكمية الأصلية التي تم إنشاؤها لأمر الفحص هذا. ومع ذلك، يقوم النظام بتعقب الكمية التي تم تقسيمها من أحد أوامر الفحص. لتنفيذ عملية التعقب هذه، يتم استخدام حقل قاعدة البيانات يسمي `QuantityThatHasSplitIntoOtherQuarantineOrders` ومع ذلك، هذا الحقل غير مرئي في واجهة المستخدم (UI).
