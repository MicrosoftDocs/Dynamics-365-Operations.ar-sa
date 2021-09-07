---
title: تجنب اقتطاع نص في التدرج الهرمي للمناصب والتصدير إلى Visio
description: يشرح هذا الموضوع كيفية إصلاح مشكلة الأسماء المبتورة للأفراد والمناصب في التسلسل الهرمي للمناصب في Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8a9a8d22df0416ef417a6216c3131bfb6d40d200
ms.sourcegitcommit: 7e32e5e39e762a4b1606161cb603a450d13b5251
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/23/2021
ms.locfileid: "7413525"
---
# <a name="avoid-text-truncation-on-the-position-hierarchy-and-export-to-visio"></a>تجنب اقتطاع نص في التدرج الهرمي للمناصب والتصدير إلى Visio

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**إصدار**

عندما يستعرض العميل التدرج الهرمي للمنصب في Microsoft Dynamics 365 Human Resources، يتم اقتطاع أسماء الأفراد ومناصبهم. لذلك، فقد يكون من الصعب أخذ لقطة شاشة أو طباعة وتوزيع التدرج الهرمي.

![التدرج الهرمي للمناصب الوظيفية.](media/position-h.png)

**السبب**

يتم هذا السلوك بسبب التصميم.

**الحل**

لسوء الحظ، لا يمكن للمستخدمين تغيير حجم النص بسهولة. ومع ذلك، يمكنك تصدير التدرج الهرمي للمنصب خارج Human Resources ثم استيراده إلى Microsoft Visio. على الرغم من كتابة المقالة التالية لبرنامج Microsoft Dynamics AX 2012، فإن العملية تنطبق مع ذلك على Human Resources: [تصدير التدرج الهرمي للمنصب إلى Microsoft Visio](/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).

اتبع هذه الخطوات للتصدير إلى Visio.

1. في Human Resources، افتح صفحة قائمة **المناصب** .

    لتضمين المزيد من المعلومات في مخطط بنية المؤسسة، أضف الحقول إلى قائمة **المناصب**، بحيث تكون متاحة عند استخدام **معالج مخطط المؤسسة** لاحقًا في هذا الإجراء.

2. في جزء الإجراءات، حدد الزر **فتح في Microsoft Office**، ثم ضمن **تصدير إلى Excel**، حدد **المناصب‏‎**. بدلاً من ذلك، اضغط على Ctrl + T.

    ![تصدير صفحة قائمة المناصب إلى Excel.](media/org-admin.png)

3. حفظ ملف Excel الذي تم تصديره.

    ![تصدير إلى مربع حوار Excel.](media/export-excel.png)

4. في Visio، حدد **Visio-إنشاء جديد**، ثم حدد فئة قالب **العمل**.

    ![مخطط جديد.](media/new.png)

5. حدد **مُعالج مخطط مؤسسة**، ثم قم بتحديد **إنشاء**.

    ![مربع حوار مُعالج مخطط مؤسسة.](media/orgchart-wizard.png)

6. حدد **المعلومات التي تم تخزينها مسبقًا في ملف أو قاعدة بيانات**، ثم قم بتحديد **التالي**.

    ![معالج مخطط المؤسسة 1.](media/orgchart-wizard7.png)

7. اختر **نص، Org Plus (\*.txt) أو ملف Excel**، ثم حدد **التالي**.

    ![معالج مخطط المؤسسة 2.](media/orgchart-wizard3.png)

8. استعرض لتحديد ملف Excel الذي تم تصديره الذي يحتوي على التدرج الهرمي للمناصب ثم قم بتحديد **التالي**.

    ![معالج مخطط المؤسسة 3.](media/orgchart-wizard2.png)

9. حدد حقل **الاسم** إلى **المنصب**، ثم قم بتعيين حقل **تقارير إلى** إلى  **تقارير إلى المنصب**، ثم قم بتحديد **التالي**.

    ![معالج مخطط المؤسسة 4.](media/orgchart-wizard1.png)

10. حدد الحقول التي ينبغي إظهارها في كل عقدة، ثم قم بتحديد **التالي**.

    ![معالج مخطط المؤسسة 5.](media/orgchart-wizard5.png)

11. إضافة عمود **المنصب** إلى قائمة **حقول بيانات الشكل**، ثم قم بتحديد **التالي**.

    ![معالج مخطط المؤسسة 6.](media/orgchart-wizard6.png)

12. الصور غير متوفرة حاليًا. لذلك، في الصفحة التالية، حدد **التالي**.
13. حدد **أريد أن يقوم المعالج بتقسيم مخطط المؤسسة الخاص بي تلقائيًا عبر الصفحات**.

    ![معالج مخطط المؤسسة 7.](media/orgchart-wizard4.png)

14. حدد **إنهاء**.

    إذا كانت هناك أي مناصب غير موجودة في البنية، سوف يُطلب منك تضمينها في المخطط.

يُظهر المخطط الذي تم إنشاؤه في Visio كل مدير في ورقة عمل منفصلة.

استنادًا إلى الحقول التي حددتها لتضمينها في المخطط، تُظهر كل عقدة المعلومات المناسبة عندما يتم إنشاء ملف Visio.

![مخطط التدرج الهرمي.](media/hierarchy.png)

**خيار إضافي**

في Human Resources، قد تتمكن أيضا من استخدام مساحة عمل **الأشخاص** لعرض بعض المعلومات المتعلقة بالتدرج الهرمي.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
