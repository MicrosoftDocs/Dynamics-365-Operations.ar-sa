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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: e8355a94322e6489fe64f22a049a34b7ecfe65b9
ms.contentlocale: ar-sa
ms.lasthandoff: 07/27/2017

---
# <a name="change-kanban-rules-for-a-process-job"></a>تغيير قواعد كانبان لوظيفة عملية

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


