---
title: طرح سؤال يعتمد على إجابة السؤال السابق
description: تسمح لك الأسئلة المشروطة بتحديد سؤال المتابعة الذي سيتم تقديمه للمستجيب، استنادًا إلى الإجابة على السؤال السابق.
author: twheeloc
ms.date: 10/28/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMCollection, KMCollectionQuestion, KMCollectionQuestionTree, HcmLearningWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b2f7d55b577478f3156a8299fc2f827ab3bb60f1
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686069"
---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a>طرح سؤال يعتمد على إجابة السؤال السابق


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



تسمح لك الأسئلة المشروطة بتحديد سؤال المتابعة الذي سيتم تقديمه للمستجيب، استنادًا إلى الإجابة على السؤال السابق. على سبيل المثال، إذا طرحت السؤال "هل تفضل الشاي أو القهوة"، فيمكن تحديد سؤال متابعة منطقي وفقًا لاختيار المستجيب الشاي أو القهوة كجواب على السؤال. شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.


## <a name="find-the-existing-questionnaire"></a>البحث عن الاستبيان الموجود
1. انتقل إلى **الاستبيان** > **التصميم** > **الاستبيانات**.
2. في القائمة، حدد الاستبيان WorkFH.

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a>إضافة كافة الأسئلة والأسئلة الفرعية إلى الاستبيان
1. انقر فوق **الأسئلة**.
2. انقر فوق **جديد**.
3. في حقل **السؤال**، حدد رقم السؤال 00016.
4. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
5. في القائمة، انقر فوق الارتباط في الصف المحدد.
6. انقر فوق **حفظ**.
7. قم بإغلاق الصفحة.

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a>تعيين "تسلسل الاستبيان" إلى "مشروط" وطرح سؤال يعتمد على السؤال المناسب
1. انقر فوق **تحرير**.
2. قم بتوسيع قسم **الإعداد**.
3. في حقل **أمر السؤال**، حدد "شرطي".
4. انقر فوق السؤال **الشرطي**.
5. في الشجرة، حدد "الأسئلة/اشرح سبب إجابتك على السؤال السابق كما فعلت؟".
6. في حقل **السؤال الأساسي**، حدد السؤال 00009.
7. في القائمة، انقر فوق الارتباط في الصف المحدد.
8. في حقل **الإجابة**، أدخل معرف تسلسل الإجابة لخيار الإجابة الذي تريد جعل السؤال يعتمد عليه. على سبيل المثال، أدخل 1 لخيار الإجابة الأولى.
9. انقر فوق **حفظ**.
10. في الشجرة، حدد "الأسئلة‬\أتلقى مبلغًا عادلاً نوعًا ما مقابل العمل الذي أقوم به".
    * لاحظ أنه تم تحديث شجرة الأسئلة لإظهار التبعية.  



[!INCLUDE[footer-include](../includes/footer-banner.md)]
