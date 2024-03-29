---
title: إدارة سياسات شراء الإجازات وبيعها
description: يمكنك تمكين الموظفين من شراء الإجازات وبيعها في Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9db86f2a482e7a1c1eee854958cb3f097d6baf61
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888806"
---
# <a name="manage-buy-and-sell-leave-policies"></a>إدارة سياسات شراء الإجازة وبيعها

>[!Important]
>تتوفر الوظيفة المذكورة في هذة المقالة حاليًا للعملاء في Dynamics 365 Human Resources المستقل. ستتوفر بعض الوظائف أو كلها كجزء من الإصدار المستقبلي على بنية Finance الأساسية بعد إصدار 10.0.26 من Finance.


[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يمكنك تمكين الموظفين من شراء إجازة وبيعها عن طريق إنشاء سياسة شراء وبيع الإجازات. يُمكنك تكوين هذه السياسات لاستخدام سير العمل في عمليات الاعتماد وتعيين الحد الأقصى للمبالغ والنسب المئوية وتعيين النسب المئوية للشراء والبيع. 

## <a name="enable-employees-to-buy-and-sell-leave"></a>تمكين الموظفين من شراء الإجازات وبيعها

1. في صفحة **مُعلمات الإجازة والغياب**، حدد **نعم** لـ **السماح للموظفين بشراء الإجازة** و **السماح للموظفين ببيع الإجازة**.

## <a name="create-a-buy-and-sell-leave-policy"></a>إنشاء سياسة شراء وبيع الإجازات

1. في صفحة **‏‫الإجازة والغياب‬** حدد علامة التبويب **الارتباطات**. 

2. حدد **سياسة شراء الإجازات وبيعها‬**.

3. حدد **جديد**.

4. أدخل **اسم** و **وصف** السياسة تحت **سياسة شراء الإجازة وبيعها‬**. 

5. حدد **نوع السياسة**. 

   أنواع السياسات المتاحة هي **المبلغ** و **عدد الساعات في الأسبوع**. حدد **المبلغ** لإدخال **مبلغ ثابت** للمبالغ القصوى التي يمكن للموظفين شراؤها وبيعها. إذا حددت **عدد الساعات في الأسبوع**‬، يتم استخدام وقت العمل المحدد في تقويم وقت العمل المعيّن للموظف لتحديد الحد الأقصى لمبلغ السياسة. 

6. حدد **تاريخ بدء** و **تاريخ انتهاء** للسياسة. ستتوفر الطلبات الخاصة بشراء الإجازة أو بيعها بحيث يمكن تقديمها خلال هذه الفترة الزمنية فقط. 

7. حدد **معرف سير العمل** للسياسة. سوف تستخدم أي طلبات شراء وبيع سير العمل هذا للمراجعة والاعتماد. 

8. ضمن **سياسة الشراء**، حدد **معادلة الوقت الكامل‬** (FTE) لتقسيم الحد الأقصى للمبلغ استنادًا إلى FTE المحدد في منصب الموظف. إذا كان نوع السياسة **مبلغ**، فأدخل **الحد الأقصى للمبلغ الثابت**. 

9. حدد **إضافة** لإضافة أنواع الإجازات لشرائها من قبل الموظفين. يمكنك إضافة أنواع إجازات متعددة إلى السياسة. 

10. أدخل **أشهر الخدمة** لنوع الإجازة لتمكين أشهر خدمة مختلفة من تحديد الحد الأقصى الذي يسمح للموظف بشرائه. 

11. أدخل **الحد الأقصى للمبلغ** لنوع الإجازة. 

12. أدخل **السعر** الذي سيشتري به الموظف الإجازة. 

13. بشكل اختياري، أدخل **كود الأرباح‬** الذي‬ سيتم استخدامه لشراء الإجازة. 

14. بشكل اختياري، عيّن ما إذا كان سيتم استخدام FTE لتحديد الحد الأقصى للمبلغ الخاص بنوع الإجازة. 

15. لإنشاء سياسة بيع، اتبع الخطوات من 8 إلى 14 ضمن **سياسة البيع**. 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a>إضافة سياسة شراء الإجازات وبيعها لخطة الإجازة والغياب

1. في الصفحة **الإجازة والغياب**، حدد خطة الإجازة والغياب.

2. ضمن **القواعد**، حدد **سياسة شراء الإجازات وبيعها**.

## <a name="see-also"></a>راجع أيضًا

[نظرة عامة على الإجازة والغياب](hr-leave-and-absence-overview.md)</br>
[تكوين أنواع الإجازة والغياب](hr-leave-and-absence-types.md)</br>
[استحقاق خطط الإجازة والغياب](hr-leave-and-absence-accrue.md)</br>
[شراء الإجازة وبيعها](hr-employee-self-service-buy-sell-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
