---
title: التحقق من صحة تدفق الإنتاج وإصداره
description: يوضح هذا الإجراء كيفية إنشاء تدفق إنتاج جديد وإصدار أول لـlean manufacturing.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6d87aa427c2bc3868e255c97ea11fd4e79456eef
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573575"
---
# <a name="validate-a-production-flow-and-version"></a>التحقق من صحة تدفق الإنتاج وإصداره

[!include [banner](../../includes/banner.md)]

يوضح هذا الإجراء كيفية إنشاء تدفق إنتاج جديد وإصدار أول لـlean manufacturing. المتطلبات الأساسية: يجب تحديد معلمات lean manufacturing ووحدات القياس للوقت الخاص بالفئة. وتحتاج إلى تحديد تدفق قيم ومجموعة إنتاج. ارجع إلى المستندات التقنية حول lean manufacturing للتعرف على مفاهيم تدفقات الإنتاج والأنشطة. يشير هذا الإجراء إلى الكيان القانوني USMF في بيانات العرض التوضيحي. ومع ذلك، مع افتراض أنه يتم تكوين الكيان القانوني لـlean manufacturing، يمكن استخدام كيانات قانونية أخرى.


## <a name="create-a-production-flow"></a>إنشاء تدفق إنتاج
1. انتقل إلى عنصر التحكم بالإنتاج > الإعداد > تدفق الإنتاج محدود الفاقد > تدفقات الإنتاج.
2. انقر فوق "جديد".
3. في حقل "الاسم"، اكتب قيمة.
4. في وصف الحقل، اكتب قيمة.
5. في الحقل "الاسم"، انقر فوق زر القائمة المنسدلة لفتح البحث.
6. في القائمة، انقر فوق الارتباط في الصف المحدد.
    * تدفق القيم هو وحدة تشغيل تشمل جميع الأنشطة والتدفقات الخاصة بتدفق القيم.   في هذه المرحلة، تتقيد وحدات التشغيل بكيان قانوني ولا يكون لها أية وظيفة إضافية.  
7. في الحقل "مجموعة الإنتاج"، انقر فوق زر القائمة المنسدلة لفتح البحث.
8. في القائمة، انقر فوق الارتباط في الصف المحدد.
    * تسمح مجموعات الإنتاج بتعريف المواد والعمالة وحسابات الأعمال تحت التنفيذ لعملية إنتاج. لربط سياق المحاسبة بتدفق إنتاج، يجب تحديد مجموعة إنتاج.  
9. انقر فوق "حفظ".

## <a name="create-a-production-flow-version"></a>إنشاء إصدار تدفق إنتاج
1. وانقر فوق إضافة.
2. في الحقل "تاريخ انتهاء الصلاحية"، أدخل تاريخاً ووقتًا.
    * يمكنك تحديث تاريخ انتهاء الصلاحية للإصدار في أي وقت، حتى بالنسبة للإصدارات النشطة. استخدم انتهاء صلاحية الإصدار للتخطيط للتخلص التدريجي من إصدار.  
3. انقر فوق "موافق".
4. في القائمة، قم بوضع علامة للصف المحدد.
5. في الحقل "الوحدة"، اكتب قيمة.
6. حدد وحدة المنتج.
7. في الحقل "متوسط الوقت اللازم لإنتاج وحدة من المنتج"، أدخل رقمًا.
    * بالنسبة للتحكم في كمية الإنتاج حسب الوقت لإصدار تدفق الإنتاج، حدد متوسطًا مستهدفًا للوقت اللازم لإنتاج وحدة من المنتج.   تعرف كمية الإنتاج حسب الوقت بأنه كمية الإنتاج لكل فترة زمنية.  في المثال الموضح، يساوي الوقت اللازم لإنتاج وحدة من المنتج 0.2 ساعة لكل 10 قطع. بالنسبة لفترة عمل قدرها 8 ساعات، يوافق هذا قدرة إنتاجية يومية قدرها 400 قطعة.  
8. في الحقل "الكمية لكل دورة"، أدخل رقمًا.
9. قم بتوسيع القسم "تفاصيل الإصدار" أو طيّه.
10. في الحقل "الحد الأدنى للوقت اللازم لإنتاج وحدة من المنتج"، أدخل رقمًا.
    * يجب أن يكون الحد الأدنى للوقت اللازم لإنتاج وحدة من المنتج أقل من متوسط الوقت اللازم لإنتاج وحدة من المنتج أو مساويًا له.  
11. في الحقل "الحد الأقصى للوقت اللازم لإنتاج وحدة من المنتج"، أدخل رقمًا
    * يجب أن يكون الحد الأقصى للوقت اللازم لإنتاج وحدة من المنتج أكبر من متوسط الوقت اللازم لإنتاج وحدة من المنتج أو مساويًا له.  
12. أدخل عددًا للأيام المضمنة في فترة زمن الدورة الفعلي.
    * تمثل فترة زمن الدورة الفعلي عدد الأيام التي يتم تجميع الوظائف بها منذ الدقيقة رجوعًا لحساب زمن الدورة الفعلي. يمكن تغيير القيمة في أي وقت وتُستخدم لحساب أزمنة الدورة الفعلية فقط.  
13. انقر فوق "حفظ".



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]