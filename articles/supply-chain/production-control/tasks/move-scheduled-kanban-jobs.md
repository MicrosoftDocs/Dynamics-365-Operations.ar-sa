--- 
title: "نقل وظائف كانبان المجدولة"
description: "يركز هذا الإجراء على نقل وظائف كانبان للمعالجة مخططة لفترة أخرى."
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
ms.openlocfilehash: 2a12a6859a3a436706822873bc6fdd781e0ef032
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="move-scheduled-kanban-jobs"></a>نقل وظائف كانبان المجدولة

[!include [task guide banner](../../includes/task-guide-banner.md)]

يركز هذا الإجراء على نقل وظائف كانبان للمعالجة مخططة لفترة أخرى. شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF. هذا الإجراء مخصص للمشرف على صالة الإنتاج‬ أو مخطط الإنتاج‬ الذي يعمل مع كانبان.


## <a name="select-scheduled-kanban-jobs"></a>حدد "وظائف كانبان المجدولة".
1. Gå til Produktionsstyring > Kanban > Tidsplanlægning af kanban-job.
2. !MtCMR!في الحقل "خلية العمل"، انقر فوق زر القائمة المنسدلة لفتح البحث. áçêìõý !
3. Markér den valgte række på listen.
    * حدد خلية العمل 1250.  
4. Klik på Select.
5. Vælg 'Planlagt' i feltet عرض حالة الوظيفة.
    * يؤدي ذلك إلى تصفية قائمة الوظائف‬ لعرض وظائف كانبان المجدولة فقط.  

## <a name="move-kanban-jobs-to-a-different-period"></a>نقل وظائف كانبان إلى فترة أخرى
1. Find og vælg den ønskede post på listen.
    * حدد وظيفة حالتها "مخطط‬"، على سبيل المثال، وظيفة مجدولة في 20 كانون الأول/ديسمبر 2012 في الحقل "الفترة المخططة". ثم انقل الوظيفة إلى الفترة السابقة.  
2. Klik på الفترة السابقة.
3. Klik på End.
    * سيؤدي ذلك إلى نقل الوظيفة إلى نهاية قائمة الوظائف كالوظيفة الأخيرة في الفترة السابقة.  
4. Find og vælg den ønskede post på listen.
    * حدد وظيفة حالتها "مخطط‬"، على سبيل المثال، وظيفة مجدولة في 18 كانون الأول/ديسمبر 2012 في الحقل "الفترة المخططة". ثم انقل الوظيفة إلى الفترة التالية.  
5. Klik på الفترة التالية.
6. Klik på Start.
    * سيؤدي ذلك إلى نقل الوظيفة إلى بداية قائمة الوظائف كالوظيفة الأولى في الفترة السابقة.  

## <a name="task-move-a-job-within-a-period"></a>المهمة: نقل وظيفة ضمن فترة
1. Find og vælg den ønskede post på listen.
    * حدد وظيفة حالتها "مخطط‬"، على سبيل المثال، الوظيفة الثانية المجدولة في 19 كانون الأول/ديسمبر 2012 في الحقل "الفترة المخططة". ثم انقل الوظيفة ضمن الفترة المخططة.  
2. Klik på Forward.
    * لاحظ أنه قد تم نقل الوظيفة بمقدار سطر واحد إلى الأسفل في القائمة.  
3. Klik på Backward.
    * لاحظ أنه قد تم نقل الوظيفة بمقدار سطر واحد إلى الأعلى في القائمة.  


