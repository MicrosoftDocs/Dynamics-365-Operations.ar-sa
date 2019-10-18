---
title: إعداد الفصل بين المهام
description: يمكنك إعداد قواعد لفصل المهام التي يجب تنفيذها بواسطة مستخدمين مختلفين.
author: maertenm
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 40b40b77877680e28671b7a15ea8c8b58ce94417
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180865"
---
# <a name="set-up-segregation-of-duties"></a>إعداد الفصل بين المهام

[!include [task guide banner](../../includes/task-guide-banner.md)]

يمكنك إعداد قواعد لفصل المهام التي يجب تنفيذها بواسطة مستخدمين مختلفين. يسمى هذا المفهوم الفصل بين المهام. على سبيل المثال، قد لا تريد أن يقر نفس الشخص بكل من استلام البضائع ومعالجة الدفع للمورد. يساعدك الفصل بين المهام في الحد من مخاطر الغش كما يساعدك أيضًا على اكتشاف الأخطاء أو المخالفات. يمكنك أيضا استخدام الفصل بين المهام لفرض سياسات الرقابة الداخلية. أكمل الإجراء التالي لإنشاء قاعدة. يجب أن تكون مسؤول نظام لإكمال الإجراء. شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي DAT. 

1. انتقل إلى **جزء التنقل > الوحدات النمطية > إدارة النظام > الأمان > الفصل بين المهام > قواعد الفصل بين المهام‬**.
2. انقر فوق **جديد**.
3. في الحقل **الاسم**، اكتب قيمة للقاعدة.
4. في الحقل **المهمة الأولى**، انقر فوق زر القائمة المنسدلة لفتح البحث.
5. في القائمة، قم بالبحث عن السجل المطلوب وحدده. حدد المهمة الأولى التي تحكمها القاعدة.
6. في الحقل **المهمة الثانية**، انقر فوق زر القائمة المنسدلة لفتح البحث. 
7. في القائمة، قم بالبحث عن السجل المطلوب وحدده. حدد المهمة الثانية التي تحكمها القاعدة.
10. في الحقل **مستوى الشدة**، حدد خيارًا. حدد شدة المخاطر التي تحدث عندما ينفذ نفس المستخدم أو الدور كلتا المهمتين.  
11. في الحقل **مخاطر الأمان**، اكتب قيمة. أدخل وصفًا لمخاطر الأمان.  
12. في الحقل **تقليل المخاطر**، اكتب قيمة. أدخل وصفاً للإجراءات التي تتخذها لتقليل مخاطر الأمان. على سبيل المثال، يمكنك تقليل المخاطر بإجراء عمليات مراجعة أدق للعملية أو بإجراء مراجعة إدارية شهرية أو مشاركة الموارد مع الأقسام الأخرى.     
13. انقر فوق **حفظ**.
