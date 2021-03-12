---
title: تمكين عملية المرتبات للوقت والحضور
description: يوضح هذا الإجراء كيفية تمكين عملية مرتبات الوقت والحضور‬.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgPayTable, JmgPayRate, JmgPayAgreementTable, JmgPayAgreementLine, HcmWorker
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c855f388e8afbd12559cd633cfcdebc7740bce6a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977778"
---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a>تمكين عملية المرتبات للوقت والحضور

[!include [banner](../../includes/banner.md)]

يوضح هذا الإجراء كيفية تمكين عملية مرتبات الوقت والحضور‬. شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.


## <a name="create-a-pay-type-with-a-related-pay-rate"></a>إنشاء نوع دفع مع معدل دفع ذي صلة
1. التوقيت والحضور > إعداد > كشف الرواتب‬ > أنواع الدفع
2. انقر فوق "جديد".
3. في حقل "نوع الدفع"، اكتب قيمة.
4. في وصف الحقل، اكتب قيمة.
5. انقر فوق "حفظ".
6. انقر فوق "المعدلات‬".
    * يتم إعداد معدلات لأنواع الدفع لفترات زمنية محددة، ويمكن إنشاء معدلات فردية للموظفين. ليس من الضروري دائمًا إنشاء معدلات لأنواع الدفع في التوقيت والحضور. ربما توجد هذه المعلومات مسبقًا في نظام الرواتب المستخدم لإنشاء أجور الموظفين.  
7. انقر فوق "جديد".
8. في القائمة، قم بوضع علامة للصف المحدد.
9. أدخل رقمًا في الحقل "المعدل‬".
10. انقر فوق "حفظ".

## <a name="create-a-pay-agreement"></a>إنشاء اتفاقية دفع
1. قم بإغلاق الصفحة.
2. قم بإغلاق الصفحة.
3. انتقل إلى "اتفاقيات الدفع".
    * التوقيت والحضور > إعداد > اتفاقيات الدفع  
4. انقر فوق "جديد".
5. في حقل "اتفاقية الدفع"، اكتب قيمة.
6. في وصف الحقل، اكتب قيمة.
7. انقر فوق "حفظ".
8. انقر فوق "بنود الاتفاقية".
9. انقر فوق "جديد".
10. في القائمة، قم بوضع علامة للصف المحدد.
11. في الحقل "نوع ملف التعريف‬"، أدخل قيمة أو حددها.
12. في الحقل "نوع الدفع"، أدخل قيمة أو حددها.

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a>إعداد اتفاقية دفع لعامل التوقيت والتسجيل
1. قم بإغلاق الصفحة.
2. قم بإغلاق الصفحة.
3. انتقل إلى "عاملو التسجيل الزمني".
    * التوقيت والحضور > إعداد > عاملو التسجيل الزمني‬  
4. في القائمة، انقر فوق الارتباط في الصف المحدد.
5. انقر فوق علامة التبويب "التوظيف‬‬".
6. وسّع مقطع "التسجيل الزمني‬".
7. انقر فوق "تحرير".
8. في الحقل "اتفاقية الدفع"، أدخل قيمة أو حددها.

