---
title: يعمل إلغاء التقارير كمنته على إنشاء حركة مفتوحة غير متوقعة
description: يؤدي إلغاء الإبلاغ كمنته الذي يحتوي على علامة إلى إنشاء حركة مفتوحة حيث تكون الكمية المعكوسة هي نفس أبعاد المخزون الخاصة بالحركة المعكوسة.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 73ebc45ee83516f573c3f73ef8106da9ae44c590c05d8dbd08520bc5ef19e49a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714200"
---
# <a name="reversal-of-reporting-as-finished-creates-an-unexpected-open-transaction"></a>يعمل إلغاء التقارير كمنته على إنشاء حركة مفتوحة غير متوقعة

رقم KB: 4612469

## <a name="symptoms"></a>العلامات

إذا قمت بعكس الإبلاغ كمنته الذي يحتوي على علامة، فإن النظام يعمل على إنشاء حركة مفتوحة حيث تكون الكمية المعكوسة هي نفس أبعاد المخزون الخاصة بالحركة المعكوسة.

## <a name="resolution"></a>الدقة

عند عكس عملية تقرير كمنته، تتم تهيئة بُعد المخزون من دفتر يومية الإنتاج. ولذلك، يحصل على رقم الدفعة. وبسبب التمييز، سترث حركات أمر المبيعات رقم الدفعة.

يمكن إعادة تعيين البُعد عند ترحيل الإبلاغ كمنته.
