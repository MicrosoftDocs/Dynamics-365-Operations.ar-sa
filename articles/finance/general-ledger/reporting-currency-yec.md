---
title: عملة التقارير خارج الرصيد عند تشغيل إقفال نهاية السنة
description: يوضح هذا المقال كيف يمكن أن تكون عملة التقارير خارج الرصيد عند تشغيل إقفال نهاية السنة.
author: kweekley
ms.date: 12/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 31f79791330e076d4fbd7b604ba9f9c6cd9b9195
ms.sourcegitcommit: 44f0b4ef8d74c86b5c5040be37981e32eb43e1a8
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/14/2022
ms.locfileid: "9850252"
---
# <a name="reporting-currency-out-of-balance-when-the-year-end-close-is-run"></a>عملة التقارير خارج الرصيد عند تشغيل إقفال نهاية السنة

بعد تمكين ميزة **الوعي بين تسوية دفتر الأستاذ وإقفال نهاية السنة** (ميزة **الوعي**)، لن يتم تضمين حركات دفتر الأستاذ التي تمت تسويتها بعد ذلك في الرصيد الافتتاحي لل المالية التالية عند تشغيل إقفال نهاية السنة لدفتر الأستاذ العام. قد يؤدي استبعاد حركات دفتر الأستاذ التي تمت تسويتها إلى تحدي في العملاء الموجودين في إقفال نهاية السنة إذا تم تحديد عملة التقارير لدفتر الأستاذ.

تتم تسوية دفتر الأستاذ لعملة المحاسبة فقط. عند تسوية حركات دفتر الأستاذ، فإن التحقق من الصحة يؤكد فقط أن خصم عملة المحاسبة مساوي لائتمانات عملة المحاسبة. ولا يتم التحقق من صحة مبالغ عملة التقارير لحركات دفتر الأستاذ هذه، وقد لا تكون العمليات المدينة مساوية لائتمانها. بالإضافة إلى ذلك، لا تقوم بتسوية دفتر الأستاذ بحساب الأرباح/الخسائر وترحيلها بعملة التقارير تلقائيًا.

وبسبب هذه القيود، يجب أن تكون حركة الأرباح/الخسائر موجودة بعملة التقارير عند الانتهاء من تسوية دفتر الأستاذ. إذا لم يتم تضمين الأرباح/الخسائر في تسوية دفتر الأستاذ، فإنه سيتم عرض رسالة نفاد الرصيد عند تشغيل إقفال نهاية السنة.

وينتقل المثال التالي خلال خطوات معالجة هذه المشكلة قبل تشغيل إقفال نهاية السنة.

## <a name="example-setup"></a>مثال الإعداد

لإعداد هذا المثال، قم بتمكين ميزة **الوعي**، وقم بإعداد الحساب الرئيسي 110180 لتسوية دفتر الأستاذ. يوضح الرسم التوضيحي التالي حركات دفتر الأستاذ التي تم ترحيلها في الكيان القانوني DEMF. عملة المحاسبة لـ DEMF هي الدولار الأمريكي (USD) وعملة التقرير هي اليورو (EUR).

![حركات دفتر الأستاذ المُرحلة بعملة التقارير.](./media/reporting-currency-1.png)

تعرض الصفحة **عمليات تسوية دفتر الأستاذ** حركات دفتر الأستاذ للحساب الرئيسي 110180. حدد مع الاستمرار (أو انقر بزر الماوس الأيمن) في الشبكة ، ثم حدد **إدراج الأعمدة**. أضف العمود **المبلغ بعملة التقارير** بحيث يتم عرض جميع مبالغ بعملة الحركة وعملة المحاسبة وعملة التقارير.

![المبلغ الموجود في عمود عملة التقارير والذي تمت إضافته إلى صفحة تسويات دفتر الأستاذ.](./media/Ledger-settlement2.png)

تتم تسوية أول حركتين من حركات دفتر الأستاذ بمبلغ 100.00 يورو كمجموعة واحدة، وتتم تسوية حركتي دفتر الأستاذ التاليتين لمبلغ 200.00 يورو على إنها مجموعة أخرى. (سيكون للحركتين معرفين تسوية مختلفين.) يوضح هذا الإعداد أن المؤسسات سيكون لديها مجموعات متعددة من حركات دفتر الأستاذ التي تتم تسويتها في أوقات مختلفة ولها تواريخ تسوية مختلفة. بعد اكتمال التسوية، تقوم صفحة **تسويات دفتر الأستاذ** بعرض المعلومات التالية عند تصفيتها لإظهار الحركات التي تكون حالتها **تمت التسوية**.

![الحركات التي تمت تسويتها على صفحة تسويات دفتر الأستاذ.](./media/Settled-trans-filtered3.png)

في الصفحة **تسويات دفتر الأستاذ**، حدد ثم اضغط مع الاستمرار (أو انقر بزر الماوس الأيمن) في العمود **المبلغ**، ثم حدد **إجمالي هذا العمود**. كرر هذه الخطوة للأعمدة **المبلغ بعملة التقرير** . يجب أن يكون لعملة المحاسبة اختلاف قيمته 0 (صفر) لحدوث التسوية. ومع ذلك، لا يوجد تحقق من صحة مبلغ التسوية الخاص بعملة التقارير. يبين الرسم التوضيحي التالي فرق بمقدار -27.79 دولار أمريكي بعملة التقارير.

![الفروق بعملة التقارير.](./media/Difference4.png)

## <a name="year-end-close"></a>إقفال نهاية السنة

وفي حالة تشغيل إقفال نهاية السنة الآن لعام 2022، ستنتهي العملية في خطأ نفاد الرصيد. يحدث هذا الخطأ مباشرة بسبب حقيقة أن عملة التقارير لا تحتوي على مبلغ تسوية دفتر أستاذ يصل إلى 0 (صفر).

![رسالة الخطأ التي تشير إلى أن مبلغ تسوية دفتر الأستاذ ليس 0 (صفر).](./media/YEC5.png)

## <a name="posting-reporting-currency-gainloss"></a>ترحيل الأرباح/الخسائر بعملة التقارير

بالنسبة لتشغيل إقفال نهاية السنة بنجاح، يجب أن يتم حساب الفرق بمبلغ عملة التقارير، وذلك عادة كأرباح أو خسائر، ويتم تضمينه في تسوية دفتر الأستاذ. يمكن ترحيل الأرباح/الخسائر بعملة التقارير بطرق متعددة:

- إذا كان الحساب الرئيسي هو حسابات دائنة أو حسابات مدينة، فإن تسوية الحسابات الدائنة/المدينة لتلك المستندات ستقوم بإنشاء الأرباح/الخسائر المطلوبة. ويجب تضمين إدخال المحاسبة في تسوية دفتر الأستاذ عند تسوية حركات دفتر الأستاذ المقابلة من الفاتورة والمدفوعات والإشعارات الدائنة وما إلى ذلك.
- إذا كان الحساب الرئيسي هو أي حساب بالإضافة إلى حسابات دائنة أو حسابات مدينة، فيجب إدخال الأرباح/الخسائر يدويًا. عند ترحيل الأرباح/الخسائر، يتم تحديد مستوى التفاصيل للإدخال المحاسبي بواسطة مؤسستك.
- بالنسبة لكل حساب رئيسي، حدد مبلغ الأرباح/الخسائر بعملة التقارير الذي يجب ترحيله.

وكما هو موضح سابقًا، يمكن إجراء الترحيل في الصفحة **تسويات دفتر الأستاذ** .

1. قم بإجراء التصفية بنطاق التاريخ الذي ترغب في ترحيل الأرباح/الخسائر له. إذا كنت تخطط لترحيل الأرباح/الخسائر كل شهر، قم بالتصفية لكل شهر. إذا كنت تخطط لترحيل الأرباح/الخسائر لكل سنة مالية، قم بالتصفية للسنة بأكملها.
2. قم بالتصفية على الحساب الرئيسي.
3. قم بالتصفية بالحالة، بحيث يتم عرض الحركات **التي تمت تسويتها** فقط.
4. أضف إجمالي على العمود **المبلغ بعملة التقارير**.
5. إذا كنت ترغب في ترحيل الأرباح/الخسائر بمستوى أكثر تفصيلاً، فإنه يمكنك القيام بتصفية إضافية على معرف التسوية والأبعاد المالية وما إلى ذلك. يمثل المبلغ الإجمالي للعمود **المبلغ بعملة التقارير** المبلغ الذي يتم ترحيل الأرباح/الخسائر له.
6. انتقل إلى **دفتر الأستاذ العام \> إدخالات دفتر اليومية \> دفاتر يومية تسوية عملة التقارير‬**.
7. أدخل الحركة للأرباح/الخسائر. سيقوم دفتر اليومية هذا بترحيل تعديل بعملة التقارير فقط. تكون مبالغ بعملة الحركة وعملة المحاسبة التي يتم ترحيلها دائمًا 0 (صفر). في حالة عدم استخدام دفتر اليومية هذا من قبل، ربما تقوم بإنشاء اسم دفتر يوميه يحتوي على نوع دفتر يومية بـ **تسوية عملة التقارير** على **دفتر الأستاذ العام \> إعداد دفتر اليومية \> أسماء دفتر اليومية**.
8. إذا لم يتم السماح بالحساب الرئيسي للإدخال اليدوي، فإنه لن يتم ترحيل هذه التسوية. وبالتالي، قد يلزم الأمر إيقاف تشغيل المعلمة **عدم السماح بالإدخال اليدوي** على الصفحة **الحساب الرئيسي** بشكل مؤقت.

![الإدخال اليدوي في صفحة إيصال دفتر اليومية.](./media/Manual-entry6.png)

بعد ترحيل دفتر يومية التسوية، ارجع إلى الصفحة **تسويات دفتر الأستاذ**، وحدد الحساب الرئيسي الذي قمت بترحيل الأرباح/الخسائر له. يجب تضمين تسوية الأرباح/الخسائر في تسوية دفتر الأستاذ. ونظرًا لأن مبلغ عملة التقارير لا يصل إلى 0 (صفر)، فإنه يمكنك إلغاء تسوية أية حركات سابقة وتسويتها مرة أخرى، ولكن مع تضمين الأرباح/الخسائر في هذا الوقت. ما مدى الدقة التي تريدها لترحيل الأرباح/الخسائر وتسوية هذه الأرباح/الخسائر في تسويات دفتر الأستاذ حتى تصل إلى مؤسستك.

يبين الرسم التوضيحي التالي أنه تمت تسوية الحركات لمبلغ 200 يورو ثم يتم تمييزها للتسوية مرة أخرى. في هذه المرة، ستتضمن تسوية الأرباح/الخسائر.

![تسوية الأرباح/الخسائر في صفحة تسويات دفتر الأستاذ.](./media/gain-loss7.png)

بعد تسوية الحركات، قم بتغيير عامل التصفية **الحالة** بحيث تعرض الصفحة الحركات **التي تمت تسويتها**. الإجمالي للعمود **‏‫المبلغ بعملة التقارير‬** 0 (صفر) الآن. يمكن الآن تشغيل إقفال نهاية السنة بنجاح.

![إقفال نهاية سنة ناجح.](./media/Zero-settled8.png)