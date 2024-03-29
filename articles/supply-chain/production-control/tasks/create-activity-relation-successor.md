---
title: إنشاء علاقة نشاط - عنصر لاحق
description: يتم توثيق تدفق الأنشطة في تدفق إنتاج محدود الفاقد من خلال علاقات النشاط.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup, DefaultDashboard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8cee0c75de1fee24cfb6df018de62ece102c96cc
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579198"
---
# <a name="create-activity-relation---successor"></a>إنشاء علاقة نشاط - عنصر لاحق

[!include [banner](../../includes/banner.md)]

يتم توثيق تدفق الأنشطة في تدفق إنتاج محدود الفاقد من خلال علاقات النشاط. يوضح هذا التسجيل كيفية إنشاء علاقة نشاط.

المتطلبات الأساسية:

- تدفق إنتاج وإصدار في وضع المسودة. 

- يتم إنشاء نشاطين يتبعان بعضهما البعض في تدفق الإنتاج لكن لا يتم ربطهما.


## <a name="find-the-production-flow-version"></a>البحث عن إصدار تدفق الإنتاج 
1. انتقل إلى عنصر التحكم بالإنتاج > الإعداد > تدفق الإنتاج محدود الفاقد > تدفقات الإنتاج.
2. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
3. في القائمة، انقر فوق الارتباط في الصف المحدد.
4. في القائمة، قم بوضع علامة للصف المحدد.
5. في القائمة، حدد إصدارًا مسودة.
    * يمكن إضافة علاقات للإصدارات المسودة أو الإصدارات النشطة لتدفق إنتاج.  

## <a name="open-the-activity-overview"></a>فتح نظرة عامة عن النشاط
1. انقر فوق "الأنشطة".
    * لاحظ أن النموذج يُظهر جميع أنشطة تدفق الإنتاج التي تم تخصيصها لإصدار تدفقات الإنتاج التي تعمل فيه.  

## <a name="add-a-successor"></a>إضافة عنصر لاحق
1. انقر فوق "إضافة عنصر لاحق".
2. في الحقل "النشاط"، انقر فوق زر القائمة المنسدلة لفتح البحث.
3. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
4. في القائمة، انقر فوق الارتباط في الصف المحدد.
5. حدد خانة اختيار "التقييد".
6. في الحقل "قيمة التقييد"، أدخل رقمًا.
    * وقت التقييد هو الوقت المطلوب جدولته بين النهاية المجدولة للنشاط السابق (تاريخ الاستحقاق ووقته) والبداية المجدولة للنشاط التالي.  
7. في الحقل "الوحدات"، اكتب قيمة.
8. في الحقل "نسبة زمن الدورة"، أدخل رقمًا.
    * في حالة تشغيل النشاطين في المنتج نفسه، يجب أن تكون نسبة زمن الدورة 1. في حالة تشغيل المهمة السابقة بسرعة مضاعفة مقارنة بالمهمة اللاحقة، يجب أن تكون النسبة 2.   تُستخدم نسب زمن الدورة لحساب أزمان الدورة الفردية لأنشطة تدفق الإنتاج.  
9. انقر فوق "موافق".
10. قم بإغلاق الصفحة.
11. انقر فوق علامة التبويب "GridPanel".
12. قم بإغلاق الصفحة.
13. قم بتحديث الصفحة.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]