---
title: ما الجديد أو المتغير في Dynamics 365 Talent - Core HR‏ (11 يناير 2019)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 01/11/2019
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
ms.search.validFrom: 2019-01-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d49a4aca368e3de10ae37b56c6d286d78f7f369a
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/06/2019
ms.locfileid: "2899164"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-january-11-2019"></a>ما الجديد أو المتغير في Dynamics 365 Talent - Core HR‏ (11 يناير 2019)

**الإصدار 8.1.2100**

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Core HR.

## <a name="changes"></a>التغييرات

### <a name="validate-leave-requests-by-forecasting-available-balance"></a>التحقق من صحة طلبات الإجازة عن طريق التنبؤ بالرصيد المتوفر
تسمح التغييرات التي تم إدخالها في هذا الإصدار للموظفين بالمطالبة بوقت إجازة مستقبلي من دون طرحه من رصيدهم الحالي. سيتم استخدام مهام سير العمل القياسية لأي طلبات مستقبلية يتم تقديمها. للحصول على مزيد من المعلومات، اقرأ [الإجازة المستحقة بناءً على ساعات العمل](leave-accrue-hours-worked.md).

### <a name="view-forecasted-leave-balance-in-ess-and-people"></a>عرض رصيد الإجازات المتوقع في خدمة الموظف الذاتية والأشخاص
تسمح هذه الميزة بعرض أرصدة فترات الإجازات المستقبلية من قِبل قسم الموارد البشرية والمدراء والموظفين. بإمكان الموظفين عرض الأرصدة المستقبلية في مساحة عمل **خدمة الموظف الذاتية‬**، ويستطيع قسم الموارد البشرية الوصول إلى نفس المعلومات باستخدام مساحة عمل **الأشخاص**.

### <a name="notifications-for-changing-leave-balances"></a>الإخطارات المتعلقة بأرصدة الإجازات المتغيرة
سوف تعرض أرصدة الإجازات الرصيد الحالي للموظفين. وتتوفر الأرصدة المستقبلية على مساحتي العمل **خدمة الموظف الذاتية‬** و**الأشخاص** عن طريق إدخال "اعتبارًا من تاريخ" لحساب الرصيد المتوقع.

تمت إضافة التنقل لعرض الأرصدة المتوقعة في النواحي التالية:
  - بطاقة **زمن التوقف** على مساحة عمل **خدمة الموظف الذاتية‬**.
  - بطاقة عمل **الإجازة والغياب** على مساحة عمل **الخدمة الذاتية للمدير‬**.
  - صفحة **الإجازة والغياب** على مساحة عمل **الأشخاص**.

### <a name="allow-decimals-for-variable-compensation-plans-cash-plans"></a>السماح بالأرقام العشرية لخطط التعويض المتغير (خطط نقدية)
تتميز الآن المكافآت والخطط النقدية المتغيرة بمرونة إضافية للمبالغ وتجاوزات للقيم ذات المبالغ العشرية.

### <a name="unable-to-change-the-dates-on-variable-comp-enrollments-after-the-plan-is-saved"></a>يتعذر تغيير التواريخ في عمليات التسجيل في التعويض المتغير بعد حفظ الخطة
يسمح هذا التغيير بتحديث تاريخ انتهاء الخطة (ممددة أو منتهية صلاحيته) بعد حفظ الخطة. لا يزال باستطاعتك تنشيط الخطط أو إلغاء تنشيطها بشكل مستقل عن تاريخي البدء والانتهاء.

### <a name="payroll-information-available-when-assigned-the-payroll-admin-security-role"></a>تتوفر معلومات المرتبات عند تعيين دور أمان مسؤول المرتبات
تم تحديث دور مسؤول المرتبات بحيث يتمكن من الوصول إلى معلومات المرتبات أثناء عملية الطلب.

### <a name="employee-self-service--position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a>فشل خدمة الموظف الذاتية | التدرج الهرمي للمناصب في التنقل وصولاً إلى العقدة الأصلية
تم إدخال تغييرات للتخلص من خطأ كان يحدث عند إضافة التدرج الهرمي للمناصب إلى مساحات عمل جديدة والتنقل في البنية التنظيمية.

### <a name="new-validation-message-when-personnel-number-sequence-is-in-use"></a>رسالة تحقق من الصحة جديدة عند استخدام التسلسل الرقمي للموظفين
تم إجراء تغيير لتوضيح المشكلة التي تظهر عند تعيين موظف ويكون رقم الموظف التالي قيد الاستخدام.

### <a name="employee-self-service-workspace-selected-as-the-initial-startup-page"></a>تحديد مساحة عمل خدمة الموظف الذاتية‬ المحددة كصفحة بدء تشغيل أولي
عند تحديد مساحة عمل **خدمة الموظف الذاتية‬** كصفحة بدء تشغيل أولي لأحد المستخدمين، ولم يتم تعيين دور الموظف لهذا المستخدم، سيعيد النظام توجيه المستخدم إلى لوحة المعلومات افتراضية.

### <a name="termination-reason-code-updates-position-assignment-record"></a>كود سبب الإنهاء‬ يحدّث سجل تعيين المنصب‬
سيحدّث كود سبب الإنهاء‬ الآن سجل تعيين المنصب‬ عند إنهاء عمل أحد الموظفين وإنهاء المنصب. 
