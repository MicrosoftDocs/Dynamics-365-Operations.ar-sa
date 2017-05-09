---
title: "‏‫تخويل ‏‫التنبؤ الذي تمت تسويته"
description: "يجب عدم تخويل كافة بيانات التنبؤ على الفور. يشرح هذا المقال كيف يمكنك تحديد الفترة التي يتم فيها التخويل لتنبؤ. وهو يوضح أيضًا كيفية تخويل التنبؤ لشركات بعينها ونماذج التنبؤ."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f151f4b4290df0b2bf1b5d1159654bd248a439b1
ms.lasthandoff: 03/31/2017


---

# <a name="authorize-an-adjusted-forecast"></a>‏‫تخويل ‏‫التنبؤ الذي تمت تسويته

[!include[banner](../includes/banner.md)]


يجب عدم تخويل كافة بيانات التنبؤ على الفور. يشرح هذا المقال كيف يمكنك تحديد الفترة التي يتم فيها التخويل لتنبؤ. وهو يوضح أيضًا كيفية تخويل التنبؤ لشركات بعينها ونماذج التنبؤ.

يجب عدم تخويل كافة بيانات التنبؤ على الفور. يمكنك تحديد تواريخ البدء والانتهاء للفترة التي يتم تخويل التنبؤ لها. تتيح لك هذه الوظيفة تجميد مستودعات معينة. 

‏‫يجب أن تتوافق تواريخ البدء والانتهاء التي قمت بتحديدها مع تواريخ البدء والانتهاء من المستودع الذي تم إنشاء التنبؤ به. يفرض النظام هذا التقييد ويعدل التواريخ تلقائيًا، في حالة طلب التعديل.‬ 

في علامة التبويب **تفاصيل** في الصفحة **التخويل**، يمكنك عرض تفاصيل حول التنبؤ الذي تم إنشاؤه مؤخرًا. 

يمكنك تحديد الشركات ونماذج التنبؤ لتخويل التنبؤ للاستخدام. بشكل افتراضي، تتضمن الشبكة كافة الشركات التي تم إنشاء طلب للتنبؤ لها. لكل شركة، تتم تعبئة نموذج التنبؤ الذي يتوافق مع خطة التنبؤ الحالية التي يتم إعدادها في معلمات التخطيط الرئيسي. ومع ذلك، يمكنك تغيير نموذج التنبؤ هذا إلى أي نموذج تنبؤ ينتمي إلى هذه الشركة. إذا لم يتم إنشاء أي بيانات طلب للتنبؤ لشركة محددة، فإنك ستستلم رسالة تحذير في وقت الاستيراد. 

من المهم جدًا أن تفهم كيف تعمل خانة اختيار **‏‫حفظ التسويات اليدوية التي تم إدخالها على التنبؤ بالطلب الأساسي ‬**. إذا قمت بإجراء التسويات اليدوية للتنبؤ الأساسي الإحصائي، فإنه يتم تخويل القيم المعدلة للاستخدام، حتى إذا تم مسح خانة الاختيار هذه. ومع ذلك، يتم تجاهل التغييرات بعد التخويل. وبالتالي، في المرة التالية التي يتم فيها إنشاء تنبؤ، يكون هذا التنبؤ إحصائيًا فقط ولا يحتوي على أي تجاوزات يدوية، حتى إذا تم تحديد **‏‫نقل التسويات اليدوية إلى التنبؤ بالطلب‬**. وبالتالي، يمكنك اعتبار خانة الاختيار **‏‫حفظ التسويات اليدوية التي تم إدخالها على التنبؤ بالطلب الأساسي ‬** آلية تسمح لك الاحتفاظ كافة التغييرات اليدوية أو تجاهلها.

<a name="see-also"></a>راجع أيضًا
--------

[القيام بتسويات يدوية في تنبؤ الخط الأساسي](manual-adjustments-baseline-forecast.md)

[مراقبة دقة التنبؤ](monitor-forecast-accuracy.md)



