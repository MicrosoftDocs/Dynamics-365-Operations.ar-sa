--- 
title: "إزالة وظيفة كانبان من الجدول"
description: "يركز هذا الإجراء على إزالة وظيفة كانبان للمعالجة مخططة من الجدول من خلال عكس حالة الوظيفة إلى \"غير مخطط\"."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9a0f246bfe42dde0befdf5c4f01d2ad1e1200b12
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="remove-a-kanban-job-from-the-schedule"></a>إزالة وظيفة كانبان من الجدول

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


