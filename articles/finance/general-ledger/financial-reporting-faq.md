---
title: الأسئلة الشائعة حول إعداد التقارير المالية
description: يسرد هذا الموضوع الأسئلة المتعلقة بالتقارير المالية التي قام بها مستخدمون آخرون.
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a0718db77399901acc8c88278c5b373b77b3cb16
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811288"
---
# <a name="financial-reporting-faq"></a>الأسئلة الشائعة حول إعداد التقارير المالية 

يسرد هذا الموضوع الأسئلة المتعلقة بالتقارير المالية التي قام بها مستخدمون آخرون. 


## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a>كيف يمكن تقييد الوصول إلى تقرير باستخدام "أمان الشجرة"؟

السيناريو: تحتوي الشركة التجريبية USMF على تقرير الميزانية العمومية التي لا ترغب في أن يتمكن كافة مستخدمي التقارير المالية من عرضها في D365. الحل: يمكنك استخدام أمان الشجرة لتقييد الوصول إلى تقرير واحد بحيث يتمكن بعض المستخدمين فقط من الوصول إلى التقرير. 

1.  التسجيل في مصمم تقرير التقارير المالية

2.  إنشاء تعريف شجرة جديد (الملف | جديد | تعريف الشجرة) ا.    انقر نقرًا مزدوجًا فوق بند **الملخص** في العمود **أمان الوحدة**.
  i    انقر فوق "المستخدمون والمجموعات".  
          1. حدد المستخدمين أو المجموعة التي ترغب في الوصول إلى هذا التقرير. 
          
[![شاشة المستخدم](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)

[![شاشة الأمان](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)

  b.    انقر فوق **حفظ**.
  
[![الزر حفظ](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)

3.  في تعريف التقرير قم بإضافة تعريف الشجرة الجديد

[![نموذج تعريف الشجرة](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)

A.  في "تعريف الشجرة" انقر فوق "الإعداد" وضمن "تحديد وحدة التقرير" حدد "تضمين كل الوحدات"

[![نموذج تحديد وحدة التقارير](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)

**قبل:** [![قبل لقطة الشاشة](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)

**بعد:** [![بعد لقطة الشاشة](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)

ملاحظة: سبب الرسالة أعلاه ليس لدى المستخدم حق الوصول إلى هذا التقرير بعد تطبيق أمان الوحدة



## <a name="how-do-i-determine-which-accounts-do-not-matching-my-balances-in-d365"></a>كيف يمكنني تحديد الحسابات التي لا تطابق الأرصدة الخاصة بي في الـ D365؟

عندما يكون لديك تقرير لا يطابق ما تتوقعه في D365، ففيما يلي بعض الخطوات التي يمكنك اتخاذها لتحديد هذه الحسابات والتباينات. 

### <a name="in-financial-reporter-report-designer"></a>في مصمم تقرير التقارير المالية

1.  إنشاء تعريف صف جديد a.    انقر فوق "تحرير" | ، ‬‏‫إدراج الصفوف من الأبعاد i.  حدد الحساب الرئيسي [![تحديد الشاشة الرئيسية_](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)
    
    ii. انقر فوق "موافق" b.    احفظ "تعريف الصف".

2.  إنشاء تعريف عمود جديد     [![إنشاء تعريف عمود جديد](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)

3.  إنشاء تعريف تقرير جديد a.    انقر فوق "الإعدادات" وقم بإلغاء تحديد [![نموذج الإعدادات](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)
   
4.  قم بإنشاء التقرير. 

5.  قم بتصدير التقرير إلى Excel.

### <a name="in-d365"></a>في D365: 
1.  انقر فوق دفتر الأستاذ العام | الاستعلامات والتقارير | ميزان المراجعة a.    محددات i.  من "التاريخ": بدء السنة المالية ii. إلى تاريخ: التاريخ الذي أنشأت فيه التقرير لـ iii.    مجموعة الأبعاد المالية "مجموعة الحساب الرئيسي"، [![نموذج الحساب الرئيسي](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)
      
  b.    انقر فوق "حساب".

2.  تصدير التقرير إلى Excel

الآن يمكنك نسخ البيانات من تقرير FR Excel والي تقرير ميزان مراجعة D365 ومقارنة الأعمدة "رصيد الاقفال".


[!INCLUDE[footer-include](../../includes/footer-banner.md)]