---
title: إزالة وظيفة كانبان من الجدول
description: يركز هذا الإجراء على إزالة وظيفة كانبان للمعالجة مخططة من الجدول من خلال عكس حالة الوظيفة إلى "غير مخطط".
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, SysLookupMultiSelectGrid, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 838270189e08065f791c9e58888351025e0a6df8
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573623"
---
# <a name="remove-a-kanban-job-from-the-schedule"></a>إزالة وظيفة كانبان من الجدول

[!include [banner](../../includes/banner.md)]

يركز هذا الإجراء على إزالة وظيفة كانبان للمعالجة مخططة من الجدول من خلال عكس حالة الوظيفة إلى "غير مخطط". شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF. هذا الإجراء مخصص للمشرف على صالة الإنتاج‬ أو مخطط الإنتاج‬.


## <a name="find-a-planned-kanban-job"></a>البحث عن وظيفة كانبان مخططة
1. انتقل إلى التحكم بالإنتاج‬ > كانبان > جدولة وظيفة كانبان‬.
2. في الحقل "خلية العمل"، انقر فوق زر القائمة المنسدلة لفتح البحث.
3. في القائمة، انقر فوق الارتباط في الصف المحدد.
    * حدد خلية العمل 1250.  
4. انقر فوق تحديد.
5. في الحقل "عرض حالة الوظيفة‬"، حدد "'مجدول".

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a>إزالة وظيفة كانبان المخططة من الجدول
1. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
    * حدد وظيفة حالتها "مخطط"، على سبيل المثال، وظيفة من 19 كانون الأول/ديسمبر 2012.  
2. في جزء "الإجراءات"، انقر فوق "خطة".
3. انقر فوق "عكس حالة الوظيفة"
4. انقر فوق "موافق".
    * سيؤدي ذلك إلى عكس حالة الوظيفة الحالية من 'مخطط' 'غير مخطط' وإزالتها من لوحة المعالجة.   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]