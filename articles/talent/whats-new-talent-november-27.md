---
title: ما الجديد أو المتغير في Dynamics 365 Talent - Core HR (27نوفمبر 2018)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1d6b5f5f7b62c400679df5eb014dee05f02e11d0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460189"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-november-27-2018"></a>ما الجديد أو المتغير في Dynamics 365 Talent - Core HR (27نوفمبر 2018)

**الإصدار 8.1.2064**

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Core HR.


## <a name="changes"></a>التغييرات

### <a name="unable-to-create-a-note-in-case-management"></a>تعذر إنشاء ملاحظة في إدارة الحالة

تم إجراء تغيير لمشكلة تحدث عند محاولة تحرير أو إنشاء ملاحظة في سجل الحالة الخاص بإدارة الحالة.

### <a name="misspelled-word-on-the-analytics-tab-in-the-compensation-workspace"></a>الكلمات التي بها أخطاء إملائية في علامة تبويب التحليلات في مساحة عمل التعويض. 

تم إجراء تغيير لتصحيح الأخطاء الإملائية لـ "الأصل العرقي" في مخطط تحليلات التعويض في مساحة عمل التعويض.

### <a name="employee-self-service-workspace-not-displaying-when-a-user-isnt-assigned-to-a-worker"></a>لا يتم عرض مساحة عمل خدمة الموظف الذاتية عندما لا يتم تعيين مستخدم إلى عامل. 

تم إجراء تغيير عندما تم تحديد مساحة عمل **خدمة الموظف الذاتية** كصفحة أولية عند بدء التشغيل لمستخدم لم يتم تعيينه لعامل. في هذه الحالة، سوف يتم عرض لوحة معلومات الافتراضية.

### <a name="leave-and-absence-error-object-reference-not-set-to-an-instance-of-an-object"></a>خطأ في الإجازة أو الغياب: لم يتم تعيين مرجع الكائن إلى مثيل كائن.

تم إجراء تغييرات في الإجازة والغياب لتصحيح الخطأ بعد الموافقة على سجلات الإجازة والغياب في قائمة  **عناصر عمل تم تعيينها إليّ**.

### <a name="unable-to-recall-an-image-workflow"></a>تعذر استدعاء سير عمل صورة

بعد استدعاء سير عمل صورة، سوف يتم تعيين سير العمل إلى "ملغي" ويمكن حذف الطلب الموجود في مساحة عمل الخدمة الذاتية للموظف.

### <a name="rehired-employees-or-contractors-show-up-multiple-times-after-termination"></a>يظهر الموظفون أو المقاولون المعاد توظيفهم عدة مرات بعد الإنهاء 

باستخدام هذا التحديث، سوف يظهر الموظفون المنهي خدمتهم والذين أُعيد توظيفهم مرة واحدة فقط في قائمة الإنهاء. 

## <a name="known-issue"></a>مشكلات معروفة​

- **المشكلة**: عند إضافة مرفق جديد إلى عامل، يظهر الزران **جديد** و **تحرير** بلون رمادي. 
- **الحل البديل:** قبل فتح صفحة المرفق، تأكد من أن مربعات الحقائق في صفحة **العامل** مغلقة. إذا كانت مربعات الحقائق مغلقة عند تحميل صفحة **العامل**، سيتم تمكين زر المرفقات (سوف يتم إصلاح هذه المشكلة في التحديث التالي للنظام الأساسي.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]