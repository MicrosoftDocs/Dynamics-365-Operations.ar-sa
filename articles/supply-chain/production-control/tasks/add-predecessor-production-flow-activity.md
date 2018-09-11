--- 
title: "إضافة مهمة سابقة إلى نشاط تدفق الإنتاج"
description: "في إصدار تدفق الإنتاج، يجب أن تكون كافة الأنشطة متسلسلة."
author: cvocph
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: d19fb20e8cc941daeaa506e4bf1cb0c7031cf2ee
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a>إضافة مهمة سابقة إلى نشاط تدفق الإنتاج

[!include [task guide banner](../../includes/task-guide-banner.md)]

في إصدار تدفق الإنتاج، يجب أن تكون كافة الأنشطة متسلسلة. بإمكان نشاط واحد أن يتضمن عدة مهام سابقة أو لاحقة. 

يوضح هذا الإجراء كيفية إقران مهمة سابقة بنشاط. 

لتنفيذ هذه المهمة، إنك تحتاج إلى تدفق إنتاج لديه إصدار "مسودة" مع نشاطين على الأقل يمكن توصيلهما. 

لمعرفة المزيد، اقرأ المستند التقنين "تدفقات الإنتاج والأنشطة في lean manufacturing".


## <a name="find-the-production-flow-and-version"></a>البحث عن تدفق الإنتاج والإصدار
1. انتقل إلى عنصر التحكم بالإنتاج > الإعداد > تدفق الإنتاج محدود الفاقد > تدفقات الإنتاج.
2. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
3. في القائمة، انقر فوق الارتباط في الصف المحدد.
4. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
5. انقر فوق "الأنشطة".

## <a name="select-an-activity-and-add-a-predecessor"></a>تحديد نشاط وإضافة عنصر سابق
1. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
2. انقر فوق "إضافة عنصر سابق".
3. في حقل "النشاط"، أدخل قيمة أو حددها.
4. في الحقل "نسبة زمن الدورة"، أدخل رقمًا.
    * نسبة زمن الدورة الافتراضية لعلاقة نشاط هي 1. هذا يفترض أن تشغيل النشاطين يتم بنفس الوتيرة أو الوقت اللازم لإنتاج وحدة من المنتج. إذا تم تنفيذ المهمة السابقة بوتيرة أسرع (مستوى أدنى للوقت اللازم لإنتاج وحدة من المنتج)، فيجب أن تكون النسبة أقل من 1، وإذا تم تنفيذ المهمة السابقة بوتيرة أبطأ (مستوى أعلى للوقت اللازم لإنتاج وحدة من المنتج)، فإن نسبة زمن الدورة ستكون أكبر من 1.  
5. انقر فوق "موافق".


