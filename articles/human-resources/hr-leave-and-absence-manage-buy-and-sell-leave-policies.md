---
title: إدارة سياسات شراء الإجازات وبيعها
description: يمكنك تمكين الموظفين من شراء الإجازات وبيعها في Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 859445f2b6e980b5960e512e69129f6a8fc6df2b
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429003"
---
# <a name="manage-buy-and-sell-leave-policies"></a>إدارة سياسات شراء الإجازات وبيعها

[!include [banner](includes/preview-feature.md)]

يمكنك تمكين الموظفين من شراء إجازة عن طريق إنشاء سياسة شراء الإجازات.  

## <a name="enable-employees-to-buy-and-sell-leave"></a>تمكين الموظفين من شراء الإجازات وبيعها

1. في صفحة **معلمات الإجازة والغياب‬**، حدد **نعم** للخيار **السماح للموظفين بشراء الإجازات**. 

## <a name="create-a-buy-leave-policy"></a>إنشاء سياسة شراء الإجازات

1. في صفحة **‏‫الإجازة والغياب‬** حدد علامة التبويب **الارتباطات**. 

2. حدد **سياسة شراء الإجازات وبيعها‬**.

3. حدد **جديد**.

4. أدخل **اسم** و**وصف** السياسة تحت **سياسة شراء الإجازة وبيعها‬**. 

5. حدد **نوع السياسة**. 

   أنواع السياسات المتاحة هي **المبلغ** و**عدد الساعات في الأسبوع**. حدد **المبلغ** لإدخال **مبلغ ثابت** للمبالغ القصوى التي يمكن للموظفين شراؤها وبيعها. إذا حددت **عدد الساعات في الأسبوع**‬، يتم استخدام وقت العمل المحدد في تقويم وقت العمل المعيّن للموظف لتحديد الحد الأقصى لمبلغ السياسة. 

6. حدد **تاريخ بدء** و**تاريخ انتهاء** للسياسة. ستتوفر الطلبات الخاصة بشراء الإجازة أو بيعها بحيث يمكن تقديمها خلال هذه الفترة الزمنية فقط. 

7. ضمن **سياسة الشراء**، حدد **معادلة الوقت الكامل‬** (FTE) لتقسيم الحد الأقصى للمبلغ استنادًا إلى FTE المحدد في منصب الموظف. إذا كان نوع السياسة **مبلغ**، فأدخل **الحد الأقصى للمبلغ الثابت**. 

8. حدد **إضافة** لإضافة أنواع الإجازات لشرائها من قبل الموظفين. يمكنك إضافة أنواع إجازات متعددة إلى السياسة. 

9. أدخل **أشهر الخدمة** لنوع الإجازة لتمكين أشهر خدمة مختلفة من تحديد الحد الأقصى الذي يسمح للموظف بشرائه. 

10. أدخل **الحد الأقصى للمبلغ** لنوع الإجازة. 

11. أدخل **السعر** الذي سيشتري به الموظف الإجازة. 

12. بشكل اختياري، أدخل **كود الأرباح‬** الذي‬ سيتم استخدامه لشراء الإجازة. 

13. بشكل اختياري، عيّن ما إذا كان سيتم استخدام FTE لتحديد الحد الأقصى للمبلغ الخاص بنوع الإجازة. 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a>إضافة سياسة شراء الإجازات وبيعها لخطة الإجازة والغياب

1. في الصفحة **الإجازة والغياب**، حدد خطة الإجازة والغياب.

2. ضمن **القواعد**، حدد **سياسة شراء الإجازات وبيعها**.

## <a name="see-also"></a>راجع أيضًا

[نظرة عامة على الإجازة والغياب](hr-leave-and-absence-overview.md)</br>
[تكوين أنواع الإجازة والغياب](hr-leave-and-absence-types.md)</br>
[استحقاق خطط الإجازة والغياب](hr-leave-and-absence-accrue.md)</br>
[شراء الإجازة وبيعها](hr-employee-self-service-buy-sell-leave.md)
