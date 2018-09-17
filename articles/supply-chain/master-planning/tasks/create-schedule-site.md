--- 
title: "إنشاء جدول ما لموقع"
description: "يوضح هذا الإجراء كيفية جدولة أوامر الإنتاج التي لم تبدأ بعد لموقع ما."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 775428bf84a752c03c492e764fa9ed576ab64fb8
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-schedule-for-a-site"></a>إنشاء جدول ما لموقع

[!include [task guide banner](../../includes/task-guide-banner.md)]

يوضح هذا الإجراء كيفية جدولة أوامر الإنتاج التي لم تبدأ بعد لموقع ما.  يتم استخدام شركة بيانات العرض التوضيحي USMF لإكمال هذا الإجراء.


## <a name="identify-production-orders-that-are-not-started"></a>تحديد أوامر الإنتاج غير المبدوءة
1. انتقل إلى التحكم بالإنتاج‬ > أوامر الإنتاج > كافة أوامر الإنتاج.
2. استخدم عامل التصفية السريع للبحث عن السجلات. على سبيل المثال، قم بإجراء التصفية على حقل الموقع بقيمة "1".
    * 1 يمثل موقعًا في USMF. إذا كنت لا تستخدم USMF، حدد موقعًا من الشركة الخاصة بك.  
3. افتح عامل تصفية عمود الحالة.
4. استخدم عامل تصفية على حقل "الحالة" بقيمة "مجدول"، باستخدام مشغل عامل تصفية "تمامًا مثل".

## <a name="create-a-schedule"></a>إنشاء جدول
1. في القائمة، قم بوضع علامة أو إلغاء علامة كل الصفوف.
2. في جزء الإجراءات، انقر فوق "جدول".
3. انقر فوق "جدولة الوظائف".
4. في الحقل "اتجاه الجدولة"، حدد "العودة للخلف اعتبارًا من تاريخ التسليم".
5. حدد "لا" في حقل "القدرة المحدودة‬".
6. حدد "لا" في حقل "المواد المحدودة‬".
7. انقر فوق "موافق".
    * قد يستغرق هذا الأمر بعض الوقت.  

## <a name="view-the-result-of-scheduled-production-orders"></a>عرض نتائج أوامر الإنتاج المجدولة
1. في القائمة، قم بوضع علامة للصف المحدد.
    * يمكنك وضع علامة على أي صف.  
2. في جزء "الإجراءات"، انقر فوق "أمر إنتاج".
3. انقر فوق كافة الوظائف.
    * في هذه الصفحة، يمكنك رؤية قائمة المهام. من علامة التبويب "جدولة"، يمكنك رؤية تاريخ البدء وتاريخ الانتهاء لمهمة ما.  
4. انقر فوق المواد.
    * في هذه الصفحة، يمكنك رؤية استهلاك المواد المقدر للعمليات على أمر الإنتاج والمخزون المتاح الحالي.  


