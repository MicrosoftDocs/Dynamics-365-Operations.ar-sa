---
title: تغيير قواعد كانبان لوظيفة عملية
description: يركز هذا الإجراء على تغيير قاعدة كانبان المستخدمة لكانبان معينة.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 13798e3521efacda896ca88a39faf36ac979d42c
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574487"
---
# <a name="change-kanban-rules-for-a-process-job"></a>تغيير قواعد كانبان لوظيفة عملية

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]