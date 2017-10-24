--- 
title: "طرح سؤال يعتمد على إجابة السؤال السابق"
description: "تسمح لك الأسئلة المشروطة بتحديد سؤال المتابعة الذي سيتم تقديمه للمستجيب، استنادًا إلى الإجابة على السؤال السابق."
author: twheeloc
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 05f7af94813934c1d77d6a509587280395f0e8bd
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a>طرح سؤال يعتمد على إجابة السؤال السابق

[!include[task guide banner](../../includes/task-guide-banner.md)]

تسمح لك الأسئلة المشروطة بتحديد سؤال المتابعة الذي سيتم تقديمه للمستجيب، استنادًا إلى الإجابة على السؤال السابق. على سبيل المثال، إذا طرحت السؤال "هل تفضل الشاي أو القهوة"، فيمكن تحديد سؤال متابعة منطقي وفقًا لاختيار المستجيب الشاي أو القهوة كجواب على السؤال. شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.


## <a name="find-the-existing-questionnaire"></a>البحث عن الاستبيان الموجود
1. انتقل إلى الاستبيان > تصميم > استبيانات‬.
2. في القائمة، حدد الاستبيان WorkFH.

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a>إضافة كافة الأسئلة والأسئلة الفرعية إلى الاستبيان
1. انقر فوق "الأسئلة".
2. انقر فوق "جديد".
3. في الحقل "السؤال‬"، حدد رقم السؤال 00016.
4. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
5. في القائمة، انقر فوق الارتباط في الصف المحدد.
6. انقر فوق "حفظ".
7. قم بإغلاق الصفحة.

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a>تعيين "تسلسل الاستبيان" إلى "مشروط" وطرح سؤال يعتمد على السؤال المناسب
1. انقر فوق "تحرير".
2. قم بتوسيع قسم "الإعداد".
3. في الحقل "ترتيب الأسئلة‬"، حدد "مشروط‬".
4. انقر فوق "سؤال مشروط".
5. في الشجرة، حدد "الأسئلة/اشرح سبب إجابتك على السؤال السابق كما فعلت؟".
6. في الحقل "سؤال أساسي‬"، حدد السؤال 00009.
7. في القائمة، انقر فوق الارتباط في الصف المحدد.
8. في حقل "الإجابة"، أدخل معرف تسلسل الإجابات لخيار الإجابة الذي تريد جعل السؤال يعتمد عليه. على سبيل المثال، أدخل 1 لخيار الإجابة الأولى.
9. انقر فوق حفظ.
10. في الشجرة، حدد "الأسئلة‬\أتلقى مبلغًا عادلاً نوعًا ما مقابل العمل الذي أقوم به".
    * لاحظ أنه تم تحديث شجرة الأسئلة لإظهار التبعية.  


