---
title: القيام بتسويات يدوية في التنبؤ الأساسي
description: يشرح هذا الموضوع كيف يمكن إجراء التسويات اليدوية على تنبؤ خط أساسي وعرض تفاصيل التنبؤ.
author: roxanadiaconu
manager: tfehr
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72704
ms.assetid: e7c5d44e-07bc-40b1-a4b3-8ba46483ef9e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: afdcbb98c96b2a685f64a16886b9a064ed13c2c0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967020"
---
# <a name="make-manual-adjustments-to-the-baseline-forecast"></a>القيام بتسويات يدوية في التنبؤ الأساسي

[!include [banner](../includes/banner.md)]

يشرح هذا الموضوع كيف يمكن إجراء التسويات اليدوية على تنبؤ خط أساسي وعرض تفاصيل التنبؤ. 

قبل القيام بتسويات يدوية، من المهم أن تفهم بعض المفاهيم على صفحات مختلفة.

## <a name="grid-on-the-adjusted-demand-forecast-page"></a>الشبكة على صفحة التنبؤ بالطلب
تتضمن صفحة **‏‫‏‫التنبؤ بالطلب‬ الذي تمت تسويته‬** الشبكة التي تحتوي على الهيكل التالي:

-   يعرض العمود الأول الأصناف ومفاتيح توزيع الأصناف والشركات وهكذا، بحيث تم إنشاء التنبؤ. يوفر العنوان الفرعي للصفحة وصفًا لأبعاد التنبؤ الحالي التي تظهر في الشبكة. على سبيل المثال، إذا كان العنوان الفرعي للصفحة **الشركة/الموقع/مفتاح توزيع الصنف**، وأحد رؤوس الصفوف في الشبكة **USMF / 1 / D\_Alloc**، يظهر هذا الصف التنبؤ لشركة USMF، والموقع 1، ومفتاح توزيع الصنف **D\_Alloc**.
-   تمثل الأعمدة اللاحقة الفترات الزمنية للتنبؤ الذي تم إنشاؤه. يُعد رأس صفحة كل عمود هو أول تاريخ للفترة الزمنية للتنبؤ الذي يوضح العمود.
-   تمثل القيم الموجودة في الخلايا التنبؤ لصنف واحد ومفتاح توزيع الصنف وهكذا، للفترة الزمنية للتنبؤ المحدد.

## <a name="forecast-aggregation-and-de-aggregation"></a>تجميع التنبؤ وإزالة تجميعه
يظهر العنوان الفرعي للصفحة مستوى تجميع التنبؤ. 

على سبيل المثال، إذا كان العنوان الفرعي للصفحة هو **الشركة / الموقع / مفتاح التوزيع / رقم الصنف / اللون / الحجم / التكوين / نمط**، لا يوجد تجميع تنبؤ ويظهر التنبؤ على مستوى العنصر وأبعاده. لتغيير التجميع، استخدم صفحة **تغيير أبعاد التنبؤ**، التي يمكنك فتحها من قائمة التطبيق. 

لتعديل التنبؤ، انقر فوق أي من الخلايا المتوفرة، واكتب قيمة التنبؤ المعدل. تصبح الخلية المحررة غامقة مباشرة للإشارة إلى أن التنبؤ الذي يظهر ليس التنبؤ الذي أنشأته خدمة التنبؤ بالطلب، ولكن تم تعديلها يدويًا. 

إذا قمت بتغيير التجميع لجعل الصفحة تظهر بيانات مجمعة بشكل أكبر، فإنه يمكنك استخدام الصفحة **بنود التنبؤ بالطلب** لعرض بنود التنبؤ الفردية التي تشكل التنبؤ المجمع. 

على سبيل المثال، لقد قمت بإنشاء التنبؤ على مستوى الصنف، ولكنك تعلم أن الطلب على هذا الصنف سيزيد عبر كافة المواقع بسبب عرض ترويجي أو حدث مماثل آخر. في هذه الحالة، يمكنك تعيين التجميع إلى **الشركة / مفتاح توزيع الصنف / الصنف** على الصفحة **تغيير أبعاد التنبؤ**. يمكنك ضبط التنبؤ العمومي للصنف عبر كافة المواقع في الشبكة **توقعات الطلب المعدلة**. لرؤية تأثير التغييرات عبر كافة المواقع، افتح الصفحة **بنود التنبؤ بالطلب**. في هذه الصفحة، سترى سطر واحد للصنف لكل موقع وكمية التنبؤ المعدل وكمية التنبؤ الأصلي. 

عندما يتم القيام بتسوية الكمية المتوقعة على مستوى مجمع، يستخدم النظام التوزيع المرجح لتوزيع التغيير بين البنود التي تُنشئ التجميع. 

يمكنك أيضًا جعل التعديلات اليدوية على صفحة **بنود التنبؤ بالطلب**، عن طريق تعديل إما قيمة **الكمية الإجمالية** أو خلايا **الكمية** في شبكة إلغاء التجميع.

## <a name="viewing-details-of-the-forecast"></a>عرض تفاصيل التنبؤ
يمكنك فتح صفحة **تفاصيل التنبؤ بالطلب** لعرض مزيد من المعلومات حول التنبؤ. 

تظهر صفحة **تفاصيل التنبؤ بالطلب** المعلومات التالية في تنسيقات رسومية وجدولية:

-   الطلب التاريخية الذي يستند إليه توقعات التنبؤ.
-   التنبؤ الحالي الذي يستخدمه التخطيط الرئيسي.
-   قيم التنبؤ بالطلب والمبالغ التي تم تعديلها يدويًا.
-   فاصل الثقة للقيم المتوقعة.
-   نموذج التنبؤ الذي تم استخدامه لإنشاء التنبؤ. إذا كنت تقوم بعرض البيانات المجمعة، سترى قائمة بكافة الأساليب التي تم استخدامها لكافة السلاسل الزمنية المجمعة.
-   دقة نموذج داخلي (‏‫متوسط الأخطاء النسبية المطلقة‬). لمزيد من المعلومات حول دقة التنبؤ، راجع [مراقبة دقة التنبؤ](monitor-forecast-accuracy.md).

**ملاحظات:**

-   إذا قمت بتمكين **تحديد نموذج التنبؤ على تفاصيل التنبؤ بالطلب** من إدارة الميزات، فإنك ستتمكن من تحديد نماذج التنبؤ التي سيتم تضمينها، للتنبؤ التاريخي، في صفحة **تفاصيل التنبؤ بالطلب**.
-   فاصل الثقة الذي يظهر في قسم **التنبؤ** من الصفحة يمثل الفرق بين الحد الأعلى لفاصل الثقة والحد الأدنى لفاصل الثقة. لعرض القيم للحدود العليا والسفلية، قم بالمرور فوق التخطيط في القسم **‏‫التنبؤ والطلب التاريخي بشكل رسومي‬**.
-   إذا كنت تستخدم خدمة Machine Learning من Microsoft Azure للتنبؤ بالطلب، فإنه يمكنك تحديد النسبة المئوية لمستوى الثقة الذي ينبغي أن يتمتع به التنبؤ الذي تم إنشاؤه. فاصل الثقة يتكون من مجموعة من القيم التي تعمل كتقديرات جيدة للتنبؤ بالطلب. تشير النسبة المئوية لمستوى الثقة بنسبة 95% إلى وجود فرصة مخاطرة بنسبة 5% بخروج التنبؤ بالطلب من نطاق فاصل الثقة.

يمكن أيضًا إجراء التسويات اليدوية للتنبؤ على الصفحة **تفاصيل التنبؤ بالطلب** عن طريق تعديل القيم في الصف **التنبؤ** في القسم **التنبؤ**.

<a name="additional-resources"></a>الموارد الإضافية
--------

[رصد دقة التنبؤ​](monitor-forecast-accuracy.md)

[إنشاء تنبؤ أساسي إحصائي](generate-statistical-baseline-forecast.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]