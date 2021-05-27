---
title: لا تظهر أوامر الشراء التي تم استلامها فعليًا في تقرير إقفال المخزون
description: لا تظهر أوامر الشراء التي تم استلامها فعليًا في تقرير إقفال المخزون للكميات المفتوحة.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventOpenQtyCritical
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 9508d6d75d8ebee7ca10140ed4c4215d7ad1dda7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026235"
---
# <a name="physically-received-purchase-orders-dont-appear-on-the-inventory-closing-report"></a>لا تظهر أوامر الشراء التي تم استلامها فعليًا في تقرير إقفال المخزون

رقم KB: 4612595

## <a name="symptoms"></a>العلامات

لا تظهر أوامر الشراء التي تم استلامها فعليًا في تقرير إقفال المخزون **للكميات المفتوحة**.

## <a name="resolution"></a>الدقة

يعرض التقرير **كميات المفتوحة** حركات الإصدار التي لا يمكن تسويتها مقابل إيصالات المخزون المحدثة ماليًا اعتبارًا من تاريخ الإقفال المحدد. يمكنك اختيار تضمين إيصالات فعلية في التقرير. وفي هذه الحالة، سيتم عرض عمليات الاستلام الفعلية إذا كان بإمكانها تغطية حركات الإصدار التي لا يمكن تسويتها. لمزيد من المعلومات، راجع [‏‫الإعداد لتشغيل إغلاق المخزون](/dynamicsax-2012/appuser-itpro/preparing-to-run-inventory-close).
