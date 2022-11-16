---
title: قابلية توسعة التعداد الأساسي للجنس
description: يقدم هذا المقال نظرة عامة على قابلية توسعة التعداد الأساسي للجنس (enum).
author: twheeloc
ms.date: 05/23/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, EssWorkspace
audience: Application User
ms.custom:
- "51941"
- intro-internal
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 61a80c16d24d8fda264340d79ed393db3f635908
ms.sourcegitcommit: 1717ff6af1879c6f3a8360936c42ecf55f86acd0
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/07/2022
ms.locfileid: "9749306"
---
# <a name="gender-base-enum-extensibility"></a>قابلية توسعة التعداد الأساسي للجنس

إن تعداد **الجنس** (enum) قابل للتوسعة الآن. يوضح هذا المقال التغييرات التي يجب إجراؤها في أساس الكود إذا كنت تخطط لتوسيع تعداد **الجنس**.

## <a name="gender-vs-hcmpersongender"></a>الجنس مقابل HcmPersonGender

هناك تعدادان لقيم الجنس:

- **الجنس** (النظام الأساسي للتطبيق)
- **HcmPersonGender** (PersonnelManagement)

يتم استخدام تعداد **الجنس** عبر Microsoft Dynamics 365 Finance، بينما يكون **HcmPersonGender** خاص بوظيفة إدارة رؤوس الأموال البشرية (HCM). إذا كنت تستخدم وظيفة HCM، وقامت بإجراء أية تغييرات على تعداد **الجنس**، فإنه يجب الأخذ في الاعتبار إجراء نفس التغييرات على **HcmPersonGender**. على سبيل المثال، إذا قمت بإضافة **مغاير الهوية الجنسانية** إلى تعداد **الجنس**، أضف **مغاير الهوية الجنسانية** إلى تعداد **HcmPersonGender** أيضًا.

## <a name="hcmpersongendertranformutil-class"></a>HcmPersonGenderTranformUtil (الفئة)

تم إنشاء فئة **HcmPersonGenderTranformUtil** جديدة للسماح بالترجمة بين التعدادين الأساسيين. في هذه الفئة، هناك طريقتان: **convertGenderToHcmPersonGender** و **convertHcmPersonGenderToGender**. يجب عليك إنشاء ملحق باستخدام الفئة **سلسلة الأمر** أو **معالجات الأحداث**، وتوسيع كلا الطريقتين لتعيين القيم الجديدة التي تتم إضافتها إلى أي من التعدادين الأساسيين.

## <a name="payrollstatewagetaxprepdp-class"></a>PayrollStateWageTaxPrepDP (الفئة)

إن **PayrollStateWageTaxPrepDP** عبارة عن فئة موفر البيانات الخاصة بتقرير SQL Server Reporting Services لـ **إعداد الضرائب وأجور الولاية والرواتب**. بالنسبة للولايات المتحدة، تتوفر ثلاثة قيم: **ذكر** و **أنثى** و **غير محدد**. في الأسلوب **populatePayrollStateWageTaxPrepTmp**، هناك عبارة switch يتم استخدامها لتعيين قيمة تعداد **HcmPersonGender** إلى أحد الحقول الثلاثة التالية: **IsMale** أو **IsFemale** أو **IsUnspecifiedGender**. القيمة الافتراضية لعبارة switch هي **IsUnspecifiedGender**. إذا قمت بإضافة أية قيم إلى التعداد **HcmPersonGender** للتعيين بشكل مختلف، فإنه يجب عليك إنشاء ملحق باستخدام الفئة **سلسة الأمر** عبر الأسلوب **populatePayrollStateWageTaxPrepTmp** لتغيير القيمة حسب الحاجة.

## <a name="smmoutlooksync_contact-class"></a>smmOutlookSync_Contact (الفئة)

ترتبط فئة تكامل **smmOutlookSync_Contact** بالقيم من وإلى **Outlook** و **جهات الاتصال**. يدعم **Outlook** ثلاث قيم: **ذكر** و **أنثى** و **غير محدد**. تتمتع الفئة بأسلوبين لمساعدتك في تعيين **الأجناس** إلى **OutlookGenders**. الأسلوب الافتراضي هو **NonSpecific/UnSpecified**. إذا قمت بإنشاء قيم إضافية لتعداد **الجنس**، فإنه يجب عليك إنشاء ملحق باستخدام الفئة **سلسلة الأمر** في كلا الأسلوبين والتعيين حسب الحاجة.
