--- 
title: "إنشاء وتعيين سياسة سلوك التكلفة إلى وحدة التحكم في التكلفة"
description: "يُعتبر سلوك التكلفة بمثابة تصنيف للتكاليف كثابتة أو متغيرة."
author: YuyuScheller
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 4190fde8c587475f34e5e3fdf6e2d32d59a26022
ms.contentlocale: ar-sa
ms.lasthandoff: 07/27/2017

---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a>إنشاء وتعيين سياسة سلوك التكلفة إلى وحدة التحكم في التكلفة

[!include[task guide banner](../../includes/task-guide-banner.md)]

يُعتبر سلوك التكلفة بمثابة تصنيف للتكاليف كثابتة أو متغيرة. يجب أن يتم تعيين سياسة وقواعد مناظرة إلى وحدة التحكم بالتكاليف لكي تصبح السياسة سارية. استخدم هذا الإجراء لإنشاء سياسة ثم تعيين السياسة إلى وحدة التحكم بالتكاليف.


## <a name="create-a-cost-behavior-hierarchy"></a>إنشاء تدرج هرمي لسلوك التكلفة
1. انتقل إلى محاسبة التكاليف > الأبعاد > التدرجات الهرمية للأبعاد‬.
2. انقر فوق "جديد".
3. انقر فوق "إنشاء".
4. في الحقل "اسم التدرج الهرمي للبعد"، اكتب '"التدرج الهرمي لسلوك التكلفة".
5. في حقل "البعد"، أدخل أو حدد قيمة.
    * حدد "عناصر التكلفة".  
6. انقر فوق "حفظ".
7. انقر فوق "عرض التدرج الهرمي".
8. انقر فوق "جديد".
9. في الحقل "اسم العقدة"، اكتب قيمة.
    * أدخل "تكلفة ثابتة".  
10. في الشجرة، حدد "التدرج الهرمي لسلوك التكلفة".
11. انقر فوق "جديد".
12. في الحقل "اسم العقدة"، اكتب قيمة.
    * أدخل "تكلفة متغيرة".  
13. انقر فوق "حفظ".
14. في الشجرة، حدد "التدرج الهرمي لسلوك التكلفة\تكلفة ثابتة".
15. انقر فوق "جديد".
16. في القائمة، قم بوضع علامة للصف المحدد.
17. في الحقل "من عضو البُعد‬"، أدخل قيمة أو حددها.
    * باستطاعة مجموعة أعضاء البعد أن تحتوي على ثغرات، ولكن يتعذر على الأعضاء التداخل.  
18. في الحقل "إلى عضو البُعد‬"، أدخل قيمة أو حددها.
    * باستطاعة مجموعة أعضاء البعد أن تحتوي على ثغرات، ولكن يتعذر على الأعضاء التداخل.  
19. في الشجرة، حدد "التدرج الهرمي لسلوك التكلفة\تكلفة متغيرة".
20. انقر فوق "جديد".
21. في القائمة، قم بوضع علامة للصف المحدد.
22. في الحقل "من عضو البُعد‬"، أدخل قيمة أو حددها.
    * باستطاعة مجموعة أعضاء البعد أن تحتوي على ثغرات، ولكن يتعذر على الأعضاء التداخل.  
23. في الحقل "إلى عضو البُعد‬"، أدخل قيمة أو حددها.
    * باستطاعة مجموعة أعضاء البعد أن تحتوي على ثغرات، ولكن يتعذر على الأعضاء التداخل.  
24. انقر فوق "حفظ".

## <a name="create-the-policy-and-rules"></a>إنشاء السياسة والقواعد
1. انتقل إلى محاسبة التكاليف > السياسات > سياسات سلوك التكلفة‬.
2. انقر فوق "جديد".
3. في الحقل "اسم السياسة"، اكتب قيمة.
4. في الحقل "تدرج بُعد عنصر التكلفة‬‬"، أدخل قيمة أو حددها.
    * حدد التدرج الهرمي للسياسة الذي أنشأته للتوّ.  
5. في الحقل "تدرج بُعد كائن التكلفة‬‬"، أدخل قيمة أو حددها.
    * حدد "المؤسسة".  
6. انقر فوق "حفظ".
7. انقر فوق "جديد".
8. في القائمة، قم بوضع علامة للصف المحدد.
9. في الحقل "عقدة التدرج الهرمي لبُعد عنصر التكلفة‬‬‬"، أدخل قيمة أو حددها.
    * قم بتوسيع التدرج الهرمي لتحديد تكلفة متغيرة.  
10. في العقدة "تدرج بُعد كائن التكلفة‬‬"، أدخل قيمة أو حددها.
    * بشكل افتراضي، النسبة المئوية المتغيرة هي 100 بالمائة.  
11. انقر فوق "تعيينات السياسة" لوحدة التحكم بالتكاليف.
12. انقر فوق "جديد".
13. في القائمة، قم بوضع علامة للصف المحدد.
14. أدخل تاريخًا في الحقل "صالح بدءًا من تاريخ المحاسبة‬‬".
    * للقواعد تاريخ سريان وباستطاعة المستخدم أو النظام إنهاء تاريخ صلاحية قاعدة إذا تم إنشاء إصدار أحدث.  
15. في الحقل "وحدة التحكم بالتكاليف‬"، أدخل قيمة أو حددها.
16. انقر فوق "حفظ".

