---
title: إنشاء تسلسل خطاب تحصيل
description: استخدم هذا الإجراء لإنشاء تسلسل خطاب تحصيل.
author: JodiChristiansen
ms.date: 12/07/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CollectionLetterCourse
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af5d0a001fbe705834e116516933be67f2de8826
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734147"
---
# <a name="create-a-collection-letter-sequence"></a>إنشاء تسلسل خطاب تحصيل

[!include [banner](../../includes/banner.md)]

استخدم هذا الإجراء لإنشاء تسلسل خطاب تحصيل. تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.

1. انتقل إلى **التحصيلات والائتمان‬ > إعداد > إعداد تسلسل خطاب التحصيل**.
2. انقر فوق **جديد**.
3. في الحقل **تسلسل خطاب التحصيل‬**، أدخل معرف تسلسل سيمثل التسلسل. سيتم استخدامه عند إعداد ملف تعريف ترحيل.
4. في حقل **الوصف**، اكتب قيمة. شروط الدفع اختيارية. إذا قمت بإدخال قيمة هنا، فستستخدم فاتورة رسوم خطاب التحصيل شروط الدفع هذه بدلاً من شروط الدفع التي يتم تخزينها مع العميل.  
5. في الحقل **كود خطاب التحصيل‬**، حدد كود خطاب التحصيل الأول الذي تريد إرساله. يتم إنشاء خطاب التحصيل الأول وفقًا لتاريخ الاستحقاق على الفاتورة، والقيمة التي تقوم بإدخالها لفترة السماح في الحقل "الأيام" على هذا البند، ومعلومات أخرى تقوم بإدخالها على هذا البند.  
6. في حقل **الوصف**، اكتب قيمة. 
7. العملة الافتراضية للرسم هي عملة الكيان القانوني. بإمكان كود العملة هذا أن يكون مختلفًا عن عملة الفاتورة.   
8. انقر فوق **إضافة** لإضافة خطاب التحصيل التالي الذي سيتم إرساله في التسلسل. في الكثير من الحالات، يُعد خطاب التحصيل الأول مجرد تحذير. يمكنك إضافة رسوم، إذا لزم الأمر.  
9. في الحقل **كود خطاب التحصيل**، حدد كود خطاب التحصيل التالي الذي سيتم إرساله في التسلسل.
10. في الحقل **الحساب الرئيسي**، حدد حساب الإيرادات الذي سيتم استخدامه للرسوم.
11. أدخل الرسوم التي سيتم فرضها عند ترحيل خطاب التحصيل هذا.
12. في الحقل **مجموعة ضرائب مبيعات الأصناف**، انقر فوق زر القائمة المنسدلة لفتح البحث. حدد مجموعة ضريبة مبيعات الصنف‬ إذا كان يجب حساب ضريبة المبيعات على الرسوم.  
13. في القائمة، انقر فوق الارتباط في الصف المحدد.
14. في الحقل **الحد الأدنى للرصيد المتأخر‬** أدخل الحد الأدنى للرصيد المتأخر المطلوب قبل إرسال خطاب التحصيل.
15. في حقل **الأيام**، أدخل عدد أيام السماح التي ستسمح بها. هذا هو عدد الأيام بعد تاريخ الاستحقاق حيث يمكن إنشاء خطاب تحصيل. يتوقف تاريخ الاستحقاق المستخدم لعملية الحساب على موضع خطاب التحصيل في تسلسل خطاب التحصيل:
    - ترتبط فترة السماح لخطاب التحصيل 1 بتاريخ الاستحقاق في الفاتورة.
    - ترتبط فترة السماح لخطابات التحصيل 2 وما فوقها بتاريخ ترحيل خطاب التحصيل السابق أو طباعته، وهذا يتوقف على التحديد في الحقل "تحديث كود خطاب التحصيل‬" في الصفحة "محددات الحسابات المدينة‬".  
16. انقر فوق **إضافة** لإضافة خطاب التحصيل الأخير في التسلسل. يمكنك إضافة ما يصل لغاية خمسة أكواد خطاب تحصيل لتسلسل خطاب التحصيل.  
17. في الحقل **كود خطاب التحصيل**، حدد كود خطاب التحصيل التالي الذي سيتم إرساله في التسلسل.
18. في حقل **الوصف**، اكتب قيمة.
19. في حقل **الحساب الرئيسي**، حدد القيم المطلوبة.
20. في الحقل **الرسوم بالعملة‬**، أدخل رقمًا.
21. في الحقل **مجموعة ضرائب مبيعات الأصناف**، انقر فوق زر القائمة المنسدلة لفتح البحث.
22. في القائمة، انقر فوق الارتباط في الصف المحدد.
23. في الحقل **الحد الأدنى للرصيد المتأخر‬**، أدخل رقمًا.
24. في الحقل **الأيام**، أدخل رقمًا.
25. حدد خانة الاختيار **حظر** لمنع العميل من إجراء عمليات تسليم وفوترة إضافية. لإلغاء حظر الحساب، حدد **لا** في حقل **الفوترة والتسليم قيد الانتظار** في صفحة **العملاء**.  
26. وسّع علامة التبويب السريعة **ملاحظة**.
27. أدخل النص الذي سيظهر على خطاب التحصيل لكود خطاب التحصيل المحدد. يمكن ترجمة هذا النص إلى لغات متعددة باستخدام القائمة **ترجمات** في أعلى مربع الملاحظة.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
