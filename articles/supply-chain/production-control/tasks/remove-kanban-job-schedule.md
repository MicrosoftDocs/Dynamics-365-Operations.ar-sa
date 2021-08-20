---
title: إزالة وظيفة كانبان من الجدول
description: يركز هذا الإجراء على إزالة وظيفة كانبان للمعالجة مخططة من الجدول من خلال عكس حالة الوظيفة إلى "غير مخطط".
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, SysLookupMultiSelectGrid, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eeedfad5f294f73097fc1b6a973d63125df72209227fc06470663665961af2d4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756909"
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