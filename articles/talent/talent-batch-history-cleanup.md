---
title: تحسين الأداء باستخدام تنظيف المهام تلقائيًا
description: يوضح هذا الموضوع كيفية حل بعض مشكلات الأداء باستخدام Dynamics 365 Talent عن طريق تنظيف سجل الوظائف الدفعية.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: fe536ace5c25765bd9c573f9303bd92f834765f7
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897962"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a>تحسين الأداء باستخدام تنظيف المهام تلقائيًا

**إصدار**

يمكن أن يواجه Microsoft Dynamics 365 Talent مشكلات في الأداء إذا زاد حجم سجل الوظائف الدفعية بدرجة كبيرة.

**السبب**

قد تؤدي المهام الدفعية التي تعمل بشكل متكرر إلى زيادة مستدامة في سجل الوظائف الدفعية. يمكن أن يسبب هذا مشاكل في الأداء. 

**الدقة**

قم بجدولة مهمة تلقائية لتنظيف سجل الوظائف الدفعيه الخاصة بك. نوصي بإعداد المهمة لتعمل أسبوعيًا، ولكن قد تحتاج إلى تشغيل التنظيف على نحو أكثر تكرارًا أو أقل تكرارًا، وفقًا للبيئة الخاصة بك. يحتوي الإجراء التالي على الإعدادات المستحسنة الخاصة بنا، ولكن يمكنك تغيير هذه الإعدادات وفقًا لاحتياجاتك.

1. في Talent، حدد **إدارة النظام**.

2. في شريط **البحث**، أدخل **‏‫تنظيف محفوظات الوظيفة الدُفعية**.

   ![بحث عن تنظيف سجل الوظائف الدفعية](media/talent-batch-history-cleanup-search-bar.png)

3. في **حد السجل (أيام)**، أدخل **30**.

   ![قم بتعيين حد السجل إلى 30](media/talent-batch-history-cleanup-history-limit.png)

4. حدد **تشغيل في الخلفية** ثم حدد **التكرار**.

   ![تعيين التكرار](media/talent-batch-history-cleanup-recurrence.png)

5. ضمن **تعريف التكرار**، قم بتعيين **تاريخ البدء** و**وقت البدء** بحيث يقعان خلال ساعات التوقف عن العمل أو عطلة نهاية الأسبوع، ثم حدد **بلا تاريخ انتهاء**. 

   ![تعيين تاريخ بدء التكرار ووقته](media/talent-batch-history-cleanup-define-recurrence.png)

6. ضمن **نمط التكرار**، حدد **أيام** وقم بتعيين **‏‫تكرار بعد الفترة المحددة** إلى **7**.

   ![تعيين التنظيف ليتكرر أسبوعيًا](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. حدد **موافق**.

8. قم بتغيير إية معلمات أخرى ضمن **تشغيل في الخلفية** عند الضرورة، ثم حدد **موافق**.

