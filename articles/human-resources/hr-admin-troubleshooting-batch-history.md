---
title: تحسين الأداء باستخدام مهام التنظيف التلقائية
description: توضح هذه المقالة كيفية تحسين الأداء في Microsoft Dynamics 365 Human Resources عن طريق تنظيف محفوظات الوظائف الدفعية.
author: twheeloc
ms.date: 08/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 10d535e54f71e7bb90c7385e09926270a446df7d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902187"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a>تحسين الأداء باستخدام مهام التنظيف التلقائية


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**إصدار**

يمكن أن يواجه Microsoft Dynamics 365 Human Resources مشكلات في الأداء إذا زاد حجم سجل الوظائف الدفعية بدرجة كبيرة.

**السبب**

قد تؤدي المهام الدفعية التي تعمل بشكل متكرر إلى زيادة مستدامة في سجل الوظائف الدفعية. يمكن أن يسبب هذا مشاكل في الأداء. 

**الدقة**

قم بجدولة مهمة تلقائية لتنظيف سجل الوظائف الدفعيه الخاصة بك. نوصي بإعداد المهمة لتعمل أسبوعيًا، ولكن قد تحتاج إلى تشغيل التنظيف على نحو أكثر تكرارًا أو أقل تكرارًا، وفقًا للبيئة الخاصة بك. يحتوي الإجراء التالي على الإعدادات المستحسنة الخاصة بنا، ولكن يمكنك تغيير هذه الإعدادات وفقًا لاحتياجاتك.

1. في Human Resources، حدد **إدارة النظام**.

2. في شريط **البحث**، أدخل **‏‫تنظيف محفوظات الوظيفة الدُفعية**.

   ![بحث عن تنظيف سجل الوظائف الدفعية.](media/talent-batch-history-cleanup-search-bar.png)

3. في **حد السجل (أيام)**، أدخل **30**.

   ![قم بتعيين حد السجل إلى 30.](media/talent-batch-history-cleanup-history-limit.png)

4. حدد **تشغيل في الخلفية** ثم حدد **التكرار**.

   ![تعيين التكرار.](media/talent-batch-history-cleanup-recurrence.png)

5. ضمن **تعريف التكرار**، قم بتعيين **تاريخ البدء** و **وقت البدء** بحيث يقعان خلال ساعات التوقف عن العمل أو عطلة نهاية الأسبوع، ثم حدد **بلا تاريخ انتهاء**. 

   ![تعيين تاريخ بدء التكرار ووقته.](media/talent-batch-history-cleanup-define-recurrence.png)

6. ضمن **نمط التكرار**، حدد **أيام** وقم بتعيين **‏‫تكرار بعد الفترة المحددة** إلى **7**.

   ![تعيين التنظيف ليتكرر أسبوعيًا.](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. حدد **موافق**.

8. قم بتغيير إية معلمات أخرى ضمن **تشغيل في الخلفية** عند الضرورة، ثم حدد **موافق**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
