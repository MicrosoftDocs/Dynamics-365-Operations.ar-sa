---
title: إنشاء إصدار تدفق إنتاج
description: يركز هذا الإجراء على إنشاء إصدار تدفق إنتاج جديد.
author: johanhoffmann
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b72d6162edd0ae6ccbfdcfe3e63ecff30528454
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569250"
---
# <a name="create-a-production-flow-version"></a>إنشاء إصدار تدفق إنتاج

[!include [banner](../../includes/banner.md)]

يركز هذا الإجراء على إنشاء إصدار تدفق إنتاج جديد. بالنسبة لهذا الإجراء، يجب تعريف معلمات lean manufacturing للإنتاج ووحدات القياس للوقت الخاص بالفئة. كما تحتاج أيضا إلى تعريف تدفق قيم ومجموعة إنتاج. لمعرفة المزيد حول تدفقات الإنتاج والأنشطة المضمنة في lean manufacturing، راجع المستندات التقنية حول lean manufacturing لتطبيق Microsoft Dynamics AX. شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.


## <a name="create-a-production-flow"></a>إنشاء تدفق إنتاج
1. انتقل إلى عنصر التحكم بالإنتاج > الإعداد > تدفق الإنتاج محدود الفاقد > تدفقات الإنتاج.
2. انقر فوق "جديد".
3. في حقل "الاسم"، اكتب قيمة.
4. في وصف الحقل، اكتب قيمة.
5. في الحقل "الاسم"، انقر فوق زر القائمة المنسدلة لفتح البحث.
6. في القائمة، انقر فوق الارتباط في الصف المحدد.
    * حدد وحدة تشغيل من نوع تدفق القيم. تدفق القيم هي وحدة تشغيل تشمل جميع الأنشطة والتدفقات الخاصة بتدفق القيم. في هذه المرحلة، تتقيد وحدات التشغيل بكيان قانوني ولا يكون لها أية وظيفة إضافية.  
7. في الحقل "مجموعة الإنتاج"، انقر فوق زر القائمة المنسدلة لفتح البحث.
8. في القائمة، انقر فوق الارتباط في الصف المحدد.
    * حدد مجموعة إنتاج لتدفق الإنتاج. تسمح مجموعات الإنتاج بتعريف المواد والعمالة وحسابات الأعمال تحت التنفيذ لعملية إنتاج. لربط سياق المحاسبة بتدفق إنتاج، يجب تحديد مجموعة إنتاج.  
9. انقر فوق "حفظ".

## <a name="create-a-production-flow-version"></a>إنشاء إصدار تدفق إنتاج
1. وانقر فوق إضافة.
2. في الحقل "تاريخ انتهاء الصلاحية"، أدخل تاريخاً ووقتًا.
    * إذا لزم الأمر، حدد تاريخ انتهاء صلاحية للإصدار. يمكنك تحديث التاريخ في أي وقت، حتى بالنسبة للإصدارات النشطة. ويمكنك استخدامه للتخطيط للتخلص التدريجي من إصدار ما.  
3. انقر فوق "موافق".
4. في القائمة، قم بوضع علامة للصف المحدد.
5. في الحقل "الوحدة"، اكتب قيمة.
6. عرّف وحدة المنتج.
7. في الحقل "متوسط الوقت اللازم لإنتاج وحدة من المنتج"، أدخل رقمًا.
    * حدد متوسط الوقت اللازم لإنتاج وحدة من المنتج فيما يخص الإصدار. بالنسبة للتحكم في كمية الإنتاج حسب الوقت لإصدار تدفق الإنتاج، حدد متوسطًا مستهدفًا للوقت اللازم لإنتاج وحدة من المنتج. تعرف كمية الإنتاج حسب الوقت بأنه كمية الإنتاج لكل فترة زمنية. في المثال، يساوي الوقت اللازم لإنتاج وحدة من المنتج 0.2 ساعة لكل 10 قطع. بالنسبة لفترة عمل قدرها 8 ساعات، يوافق هذا قدرة إنتاجية يومية قدرها 400 قطعة.  
8. في الحقل "الكمية لكل دورة"، أدخل رقمًا.
    * حدد الكمية لكل دورة المتعلقة بمتوسط الوقت اللازم لإنتاج وحدة من المنتج.  
9. قم بتبديل التوسيع للقسم "تفاصيل الإصدار".
10. في الحقل "الحد الأدنى للوقت اللازم لإنتاج وحدة من المنتج"، أدخل رقمًا.
    * حدد الحد الأدنى للوقت اللازم لإنتاج وحدة من المنتج. يجب أن يكون الحد الأدنى للوقت اللازم لإنتاج وحدة من المنتج أقل من متوسط الوقت اللازم لإنتاج وحدة من المنتج أو مساويًا له.  
11. في الحقل "الحد الأقصى للوقت اللازم لإنتاج وحدة من المنتج"، أدخل رقمًا
    * يجب أن يكون الحد الأقصى للوقت اللازم لإنتاج وحدة من المنتج أكبر من متوسط الوقت اللازم لإنتاج وحدة من المنتج أو مساويًا له.  
12. في الحقل "فترة زمن الدورة الفعلي (الأيام)"، أدخل رقمًا.
    * أدخل عدد الأيام المضمنة في فترة زمن الدورة الفعلي. تمثل فترة زمن الدورة الفعلي عدد الأيام التي يتم تجميع الوظائف بها منذ الدقيقة رجوعًا لحساب زمن الدورة الفعلي. يمكن تغيير القيمة في أي وقت وتُستخدم لحساب أزمنة الدورة الفعلية فقط.  
13. انقر فوق "حفظ".



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]