---
title: مستندات تبرير تخطيط الموازنة
description: توفر مستندات التبرير سردًا لأولئك الذي يطلبون موازنة لتوضيح ضرورة وجود موازنة محددة.
author: panolte
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetPlanJustificationTemplate
audience: Application User
ms.reviewer: kfend
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 03780b36cb3a6a609350c61792f0c98f2c08244d
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711760"
---
# <a name="budget-planning-justification-documents"></a>مستندات تبرير تخطيط الموازنة

[!include [banner](../includes/banner.md)]

توفر مستندات التبرير سردًا لأولئك الذي يطلبون موازنة لتوضيح ضرورة وجود موازنة محددة. 

يتم إنشاء قالب خطة الموازنة بواسطة مدير الموازنة في Microsoft Word، ويتم تعيينه إلى عملية تخطيط الموازنة الحالية. بعد ذلك، يمكن لملاك الموازنة فتح القالب، وملء البيانات تلقائيًا في Word بناءً على طلبهم للموازنة. ثم يمكنهم بعد ذلك إضافة نص إضافي أو البيانات قبل حفظ وإرفاق مستندات مبرراتهم الشخصية لخطة الموازنة الخاصة بهم.

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a>إعداد الوظيفة الإضافية Microsoft Dynamics Office لـ Microsoft Word

1.  افتح مستند Microsoft Word جديدًا.
2.  انقر فوق **إدراج** على الشريط، ثم انقر فوق **متجر**.
3.  ابحث عن الوظيفة الإضافية Microsoft Dynamics Office وانقر فوق **إضافة**.
4.  في Word، في الجزء الأيمن، انقر فوق **إضافة معلومات الخادم**.
5.  اكتب أو الصق عنوان URL للخادم، ثم انقر فوق **موافق**.

##### <a name="define-the-justification-template-in-microsoft-word"></a>حدد قالب التبرير في Microsoft Word

1.  انقر فوق **تصميم** في الوظيفة الإضافية Microsoft Dynamics Office بعد تسجيل الدخول.
2.  بالنسبة لمعلومات العنوان، استخدم زر **إضافة حقول**.
3.  قم بتحديد مصدر بيانات الكيان لـ BudgetPlanJustification، ثم انقر فوق **التالي**. **ملاحظة:** هذا الكيان مطلوب لأي مستند تبرير. يمكن استخدام كيانات أخرى، ولكن سوف تفشل إعادة التحميل إلى Microsoft Dynamics 365 Finance إذا لم يتم تضمين هذا الكيان.
4.  إضافة تسميات وقيم BudgetPlanName وBudgetPlanPreparer وResponsibilityCenter وDocumentNumber في مستند Word. **ملاحظة:** يمكنك استخدام التسميات المخصصة لك بدلاً من التسميات القياسية، إذا لزم الأمر.
5.  انقر فوق **تم** لإكمال قسم العنوان.
6.  بالنسبة لتفاصيل مستوى بنود مبالغ خطة الموازنة، انقر فوق **إضافة جدول**.
7.  مرة أخرى، قم بتحديد مصدر بيانات الكيان لـ BudgetPlanJustification، ثم انقر فوق **التالي**.
8.  قم بإضافة حقول إلى EffectiveDate وScenarioName وAccountDisplayValue و AccountingCurrencyExpenseAmount. **ملاحظة:** إذا توفرت إضافة تعليقات ضمن بنود خطة الموازنة الفردية، فمن ثم يمكن إضافة هذه التعليمات إلى الجدول هنا.
9.  قم بإضافة أي تعليمات إضافية لتقديمها للمستخدم النهائي، وإجراء أي تنسيق ضروري أو أنماط إلى المستند.
10. قم بحفظ المستند إلى الكمبيوتر المحلي الخاص بك، وأغلق الملف قبل المتابعة.

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a>قم بإعداد عملية التخطيط للموازنة لاستخدام قالب التبرير.

1.  انتقل إلى **إعداد الموازنة** &gt; **إعداد** &gt; **تخطيط الموازنة** &gt; **‎قوالب مستندات التبرير**.
2.  انقر فوق **جديد‏‎** واستعرض وصولاً إلى مستند Microsoft Word الذي تم إنشاؤه حديثًا.
3.  أدخل اسم عرض قالب ووصفًا. انقر فوق **موافق**.
4.  انتقل إلى **إعداد الموازنة** &gt; **إعداد** &gt; **الموازنة** **تخطيط** &gt; **عملية تخطيط الموازنة**.
5.  حدد العملية التي يجب فيها استخدام قالب التبرير، وانقر فوق **تحرير**.
6.  في حقل **قالب مستند تبرير**، حدد القالب المناسب ثم انقر حفظ.

##### <a name="edit-and-save-personalized-justification-documents"></a>تحرير وحفظ مستندات التبرير المخصصة

1.  قم بإنشاء خطة موازنة جديدة أو افتح خطة موازنة حالية.
2.  في قائمة **تبرير** المنسدلة، حدد **إنشاء مبررات جديدة**.
3.  بعد ملء التفاصيل، حدد تحميل المستند المخصص من قائمة **تبرير** المنسدلة.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
