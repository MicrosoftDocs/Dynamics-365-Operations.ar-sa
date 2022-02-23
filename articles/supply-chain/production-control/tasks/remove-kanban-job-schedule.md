---
title: إزالة وظيفة كانبان من الجدول
description: يركز هذا الإجراء على إزالة وظيفة كانبان للمعالجة مخططة من الجدول من خلال عكس حالة الوظيفة إلى "غير مخطط".
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, SysLookupMultiSelectGrid, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fcd9247e24323ba606377d7e51bd4447ab51c905
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4961605"
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

