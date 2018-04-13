--- 
title: "إنشاء مهمة مجموعة"
description: "إن الوظيفة الدفعية عبارة عن مجموعة من المهام التي يتم إرسالها إلى مثيل خادم كائنات التطبيق‬ (AOS) للمعالجة التلقائية."
author: maertenm
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 31c8e2ba87ef8c17a3147e1159104585258d4164
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-batch-job"></a>إنشاء مهمة مجموعة

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

إن الوظيفة الدفعية عبارة عن مجموعة من المهام التي يتم إرسالها إلى مثيل خادم كائنات التطبيق‬ (AOS) للمعالجة التلقائية. ويتم تشغيل الوظائف الدفعية باستخدام بيانات اعتماد الأمان للمستخدم الذي قام بإنشاء الوظيفة. استخدم الإجراء التالي لإنشاء وظيفة دفعية. شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.


## <a name="create-the-batch-job"></a>إنشاء الوظيفة الدفعية
1. انتقل إلى إدارة النظام > الاستعلامات > الوظائف الدفعية.
2. انقر فوق "جديد".
3. في حقل "وصف الوظيفة"، اكتب قيمة.
4. في الحقل "تاريخ/وقت البدء المجدول‬"، أدخل الوقت والتاريخ.
5. انقر فوق "حفظ".

## <a name="create-a-recurrence"></a>إنشاء تكرار
1. في جزء الإجراءات، انقر فوق "وظيفة دفعية".
2. انقر فوق "تكرار".
    * استخدم هذه الخيارات لإدخال نطاق ونمط للتكرار.  
3. انقر فوق "موافق".

## <a name="add-alerts"></a>إضافة تنبيهات
1. في جزء الإجراءات، انقر فوق "وظيفة دفعية".
2. انقر فوق "تنبيهات".
    * حدد إن كنت تريد إرسال رسائل تنبيه عند انتهاء الوظيفة الدفعية‬، أو إذا احتوت الوظيفة الدفعية على خطأ أو إذا تم إلغاؤها. ثم حدد إذا كنت تريد عرض التنبيهات كرسائل منبثقة.   
3. انقر فوق "موافق".


