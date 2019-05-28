---
title: إنشاء قاعدة كانبان لأنشطة متعددة
description: يوضح هذا الإجراء كيفية إنشاء قاعدة كانبان تتضمن أنشطة متعددة من تدفق إنتاج.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, KanbanFlowSelection, InventItemIdLookupSimple, KanbanCreateScheduled, Kanban
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3fe7e1c67161bd77e6ddc5d7c9f1607fe895ce21
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558447"
---
# <a name="create-a-kanban-rule-for-multiple-activities"></a>إنشاء قاعدة كانبان لأنشطة متعددة

[!include [task guide banner](../../includes/task-guide-banner.md)]

يوضح هذا الإجراء كيفية إنشاء قاعدة كانبان تتضمن أنشطة متعددة من تدفق إنتاج. شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USMF.‬ هذه المهمة مخصصة لمهندس العمليات أو مدير تدفق القيم عند قيامه بتحضير عملية إنتاج منتج جديد أو معدل في بيئة محدودة.


## <a name="create-a-new-kanban-rule"></a>إنشاء قاعدة كانبان جديدة
1. انتقل إلى إدارة معلومات المنتج‬ > خلية عمل Lean manufacturing > قواعد كنبان.
2. انقر فوق "جديد".
3. في حقل "استراتيجية التزويد"، حدد "مجدول".
4. في الحقل "نشاط الخطة الأول"، أدخل قيمة أو حددها.
    * حدد SpeakerAssemblyAndPolish.  
5. حدد خانة الاختيار "أنشطة متعددة".
    * الغرض هو تضمين أكثر من نشاط واحد في قاعدة كانبان. ستختار مسارًا في تدفق الإنتاج عند تحديد نشاط الخطة الأخير.  
6. في الحقل "نشاط الخطة الأخير‬"، أدخل قيمة أو حددها.
    * حدد SpeakerTestAndPackaging. بعد تحديد القيمة، تفتح صفحة تلقائيًا. حدد تدفق كانبان SpeakerAssemblyAndPolish > SpeakerTestAndPackaging. انقر فوق "موافق".  
7. قم بتوسيع القسم "التفاصيل".
8. في الحقل "المنتج"، أدخل قيمة أو حددها.
    * حدد الصنف L0006.  

## <a name="create-kanban-and-view-jobs"></a>إنشاء كانبان وعرض الوظائف
1. قم بتوسيع القسم "كانبان".
2. وانقر فوق إضافة.
3. في الحقل "عدد بطاقات كانبان الجديدة‬"، أدخل "1".
    * سيؤدي هذا إلى إنشاء كانبان.  
4. عيّن كمية المنتجات إلى "3".
    * سيعالج كانبان 3 منتجات.  
5. في الحقل "‏‫تاريخ/وقت الاستحقاق‬"، أدخل تاريخًا ووقتًا.
    * يمكنك إدخال "اليوم".  
6. انقر فوق "إنشاء".
7. انقر فوق "تفاصيل".
    * لاحظ وجود وظيفتي معالجة لكانبان من تدفق الإنتاج. الوظيفة الأولى هي SpeakerAssemblyAndPolish، والثانية هي SpeakerTestAndPackaging.  
    * هذه هي الخطوة الأخيرة!  

