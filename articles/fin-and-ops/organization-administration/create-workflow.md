---
title: "إنشاء سير عمل"
description: "يوضح هذا الموضوع كيفية إنشاء سير عمل."
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowSelectTemplateRnr, WorkflowTableListPageRnr
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195583
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ee3f60575d0eaaf56ce08adb1936728a76488dac
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="create-a-workflow"></a>إنشاء سير عمل

[!INCLUDE [banner](../includes/banner.md)]

يوضح هذا الموضوع كيفية إنشاء سير عمل.

<a name="open-the-workflow-editor"></a>فتح محرر سير العمل
------------------------

تحدد وحدة Microsoft Dynamics 365 for Finance and Operations النمطية التي تعمل فيها أنواع سير العمل التي يمكنك إنشاؤها. اتبع الخطوات التالية لتحديد نوع سير العمل لإنشاء محرر سير العمل وفتحه.

1.  افتح الوحدة النمطية التي تريد إنشاء سير عمل جديد لها. على سبيل المثال، لإنشاء سير عمل لطلبات الشراء، انقر فوق **التدبير وتحديد الموارد**.
2.  انقر فوق **الإعداد** &gt; **\[اسم الوحدة النمطية\] مهام سير عمل**.
3.  في صفحة القائمة التي تظهر، في جزء الإجراءات، انقر فوق **جديد**.
4.  في صفحة **إنشاء سير عمل**، حدد نوع سير العمل الذي ترغب في إنشائه، ثم انقر فوق **إنشاء سير عمل**. يظهر محرر سير العمل. يمكنك الآن استخدام الإجراءات التالية لتصميم سير العمل.

## <a name="drag-workflow-elements-onto-the-canvas"></a>سحب عناصر سير العمل فوق اللوحة القماشية
تتضمن منطقة **عناصر سير العمل** في محرر سير العمل العناصر التي يمكنك إضافتها إلى سير العمل. لإضافة عناصر إلى سير العمل، اسحبها إلى لوحة الرسم.

## <a name="connect-the-elements"></a>ربط العناصر
لربط بين عنصر واحد من عناصر سير العمل وبين عنصر آخر، اضغط باستمرار على المؤشر فوق العنصر إلى أن تظهر نقاط الربط. انقر فوق نقطة اتصال، واسحبها إلى عنصر آخر. وتأكد من ربط جميع العناصر.

## <a name="configure-the-properties-of-the-workflow"></a>تكوين خصائص سير العمل
اتبع الخطوات التالية لتكوين خصائص سير العمل.

1.  انقر فوق اللوحة القماشية للتأكد من عدم تحديد أي عنصر سير عمل.
2.  انقر فوق **خصائص** لفتح الصفحة **خصائص** لسير العمل.
3.  اتبع الإجراءات المذكورة في الموضوع [تكوين خصائص سير العمل](configure-workflow-properties.md).

## <a name="configure-the-elements-of-the-workflow"></a>تكوين عناصر سير العمل
قم بتكوين كل عنصر قمت بسحبه إلى اللوحة القماشية. لمزيد من المعلومات حول كيفية تكوين كل عنصر سير عمل، راجع المواضيع التالية:

-   [تكوين مهمة يدوية](configure-manual-task-workflow.md)
-   [تكوين مهمة تلقائية](configure-automated-task-workflow.md)
-   [تكوين عملية اعتماد](configure-approval-process-workflow.md)
-   [تكوين خطوة اعتماد](configure-approval-step-workflow.md)
-   [تكوين قرار يدوي](configure-manual-decision-workflow.md)
-   [تكوين قرار شرطي](configure-conditional-decision-workflow.md)
-   [تكوين نشاط موازٍ](configure-parallel-activity-workflow.md)
-   [تكوين فرع موازٍ](configure-parallel-branch-workflow.md)
-   [تكوين سير عمل لعنصر بند](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a>حل أية أخطاء أو تحذيرات
يعرض جزء **الأخطاء والتحذيرات** في الجزء السفلي من محرر سير العمل الرسائل التي تم إنشاؤها لسير العمل. لتحديد العنصر حيث حدث خطأ أو تحذير ما، انقر نقرا مزدوجًا فوق رسالة الخطأ أو التحذير. يجب حل كل الأخطاء والتحذيرات قبل جعل سير العمل نشطًا.

## <a name="save-and-activate-the-workflow"></a>حفظ سير العمل وتنشيطه
عندما تصبح جاهزًا لحفظ سير العمل وتنشيطه، اتبع الخطوات التالية.

1.  انقر فوق **حفظ وإغلاق** لإغلاق محرر سير العمل وفتح الصفحة **حفظ سير العمل**.
2.  أدخل تعليقات على التغييرات التي أدخلتها على سير العمل، ثم انقر فوق **موافق**.
3.  إذا تم حل جميع الأخطاء والتحذيرات، فستظهر صفحة **تنشيط سير العمل**. وحدد أحد الخيارات التالية:
    -   لتنشيط هذا الإصدار من سير العمل، انقر فوق **تنشيط الإصدار الجديد**. عندما يكون سير عمل ما نشطًا، يمكن للمستخدمين إرسال المستندات إليه للمعالجة.
    -   إذا لم ترغب في تنشيط هذا الإصدار، فانقر فوق **عدم تنشيط الإصدار الجديد‬**. يمكنك تنشيط سير العمل في وقت لاحق.






