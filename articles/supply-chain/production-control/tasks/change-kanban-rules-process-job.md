--- 
title: "تغيير قواعد كانبان لوظيفة عملية"
description: "يركز هذا الإجراء على تغيير قاعدة كانبان المستخدمة لكانبان معينة."
author: ChristianRytt
manager: AnnBe
ms.date: 03/02/2016
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
ms.openlocfilehash: 7f8b2a67e03a64deae9d4bc9c7e3e714d134443c
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="change-kanban-rules-for-a-process-job"></a>تغيير قواعد كانبان لوظيفة عملية

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

يركز هذا الإجراء على تغيير قاعدة كانبان المستخدمة لكانبان معينة. وهذا مفيد لقياس مستوى حمل الموارد أو في حالة التصنيف. شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF. هذا الإجراء مخصص للمخطط، الذي يعمل في شركة lean manufacturing، والمسؤول عن تدفق القيم.


## <a name="copy-kanban-rule"></a>نسخ قاعدة كانبان
1. انتقل إلى قواعد كانبان.
2. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
    * حدد الحدث "قاعدة كانبان" 000022 لـ L0001.  
3. انقر فوق "تكرار قاعدة كانبان".
4. انقر فوق "موافق".

## <a name="change-kanban-rule"></a>تغيير قاعدة كانبان
1. قم بإغلاق الصفحة.
2. انتقل إلى جدولة وظيفة كانبان.
3. في القائمة، قم بوضع علامة للصف المحدد.
    * حدد بند مع كانبان 000177.  
4. انقر فوق استخدام قاعدة كانبان البديلة.
5. انقر فوق التالي.
6. في حقل "قاعدة كانبان"، أدخل قيمة أو حددها.
    * حدد قاعدة كانبان التي تم إنشاؤها مسبقًا. هذه هي قاعدة كانبان مع الرقم الأعلى.  
7. انقر فوق إنهاء.
    * تستخدم وظيفة كانبان الآن قاعدة كانبان أخرى. يمكن أن يكون ذلك مفيدًا لقياس مستوى حمل خلايا العمل.  


