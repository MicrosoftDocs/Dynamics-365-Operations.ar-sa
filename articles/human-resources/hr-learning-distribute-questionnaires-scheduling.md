---
title: توزيع الاستبيانات باستخدام الجدولة
description: تتيح لك جدولة الاستبيان إمكانية تخطيط وتوزيع استبيانات على عدة مستجيبين.
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMKnowledgeCollectorPlanningTable, KMKnowledgeCollectorPlanningMulti, SysQueryForm, HcmPersonLookup, KMKnowledgeCollectorPlanning, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0cd101bfe88ae1acb051ba11a676da66ef6a3db6
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115452"
---
# <a name="distribute-questionnaires-using-scheduling"></a>توزيع الاستبيانات باستخدام الجدولة

تتيح لك جدولة الاستبيان إمكانية تخطيط وتوزيع استبيانات على عدة مستجيبين. شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.

## <a name="create-a-questionnaire-schedule"></a>إنشاء جدول استبيان

1. انتقل إلى الاستبيان > توزيع > جداول الاستبيانات.

2. انقر فوق "جديد".

3. في حقل الجدولة، أدخل قيمة.

4. في وصف الحقل، اكتب قيمة.
    * قم بتعيين الجدولة إلى مجهول إذا كان يجب تسجيل الاستجابات دون أسماء مقترنة بالاستجابة.  
    * يجب إعداد السماح بالنتائج المجهولة‬ في محددات الموارد البشرية أولاً.  

5. في حقل النوع، حدد نوع التخطيط.  في هذا المثال سوف نستخدم النوع "رضا".

6. في القائمة، قم بالبحث عن السجل المطلوب وحدده.

7. في القائمة، انقر فوق الارتباط في الصف المحدد.

8. في حقل "التاريخ"، أدخل تاريخًا.

9. قم بتوسيع المقطع "بريد إلكتروني لخدمة الموظف الذاتية‬".

10. في الحقل "الموضوع"، اكتب قيمة.

    * على سبيل المثال: الاستبيان المتوفر  

11. في حقل "النص"، اكتب النص الأساسي لرسالة البريد الإلكتروني. تجدر الإشارة إلى أنه يمكن استخدام المتغير لكي يحل محل القيم في النظام.

    * على سبيل المثال: عزيزي % P %، الرجاء تسجيل الدخول إلى ‏‫خدمة الموظف الذاتية‬ لإكمال الاستبيان "صحة القوى العاملة".  شركة الرشيدي  

12. انقر فوق "حفظ".

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a>استخدم تفاصيل الإعداد لتحديد الاستبيان (الاستبيانات) الذي تتعين الإجابة عليه بالإضافة إلى أية استعلامات لاستخدامها في تحديد المستجيبين.

1. انقر فوق تفاصيل الإعداد.

2. في القائمة، حدد استعلامًا لاستخدامه للبحث في النظام عن المستجيبين للاستبيان.

    * مثال: العاملون‬  

3. انقر فوق عرض أو تعديل الاستعلام لتحديد أشخاص معينين أو تعديل الاستعلام للبحث عن الأشخاص الذين يتطابقون مع معايير معينة.

    * لاحظ أن جميع المستجيبين يجب أن يكونوا مستخدمين في النظام.  

4. في القائمة، ضع علامة على صف "الشخص".

5. في الحقل "المعايير‬"، أدخل قيمة أو حددها.

    * حدد جوليا فونديربورك  

6. في القائمة، حدد جوليا فونديربورك‬

7. انقر فوق "موافق".

8. انقر فوق علامة التبويب الاستبيانات.

9. في الشجرة، قم بتوسيع "عقدة نوع الاستبيان استقصاء‬ الرضا".

10. في الشجرة، حدد "تقييم صحة العاملين".

11. انقر فوق "موافق".

12. انقر فوق جلسة إجابة مخططة.

    * لاحظ أنه تم إنشاء جلسات الإجابة المخططة لكل مستخدم تم تحديده/الاستعلام عنه.  

13. قم بإغلاق الصفحة.

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a>ابدأ جدولة الاستبيان لتوفير الاستبيان للمستجيبين لإكماله.

1. انقر فوق "الوظائف".

2. انقر فوق "بدء".

3. انقر فوق "موافق".

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a>أرسل رسالة بريد إلكتروني لإعلام المستجيبين بالاستبيان المتوفر.

1. انقر فوق "الوظائف".

2. انقر فوق "إرسال بريد الإلكتروني".

3. انقر فوق "إلغاء".

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a>استخدم جلسات الإجابة المخططة لمراقبة من يحتاج إلى إكمال الاستبيان.

1. انقر فوق جلسة إجابة مخططة.

    * احذف أي جلسة إجابة مخططة متبقية عندما تصبح جاهزاً لإنهاء الجلسة المجدولة.  

2. انقر فوق حذف.

3. انقر فوق نعم.

4. قم بإغلاق الصفحة.

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a>قم بإنهاء الجدول عند قيام جميع المستجيبين بإكمال الاستبيان و/أو عند حذف كل جلسات الإجابات المخططة.

1. انقر فوق "الوظائف".
2. انقر فوق "إنهاء".
3. انقر فوق "موافق".



[!INCLUDE[footer-include](../includes/footer-banner.md)]