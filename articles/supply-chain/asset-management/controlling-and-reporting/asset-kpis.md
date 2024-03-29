---
title: ‏‫مؤشرات الأداء الرئيسية‬ الخاصة بالأصل
description: يشرح هذا المقال مؤشرات الأداء الأساسية للأصول في إدارة الأصول.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectKPI
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ef0df92edaa2ee33bd75e01a666086e32c8101af
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870860"
---
# <a name="asset-kpis"></a>‏‫مؤشرات الأداء الرئيسية‬ الخاصة بالأصل

[!include [banner](../../includes/banner.md)]

 

في إدارة الأصول، يمكنك حساب مؤشرات أداء أساسيه متعددة (KPI) للأصول وأنواع الأصول. استخدم مؤشرات الأداء الأساسية للحصول على نظرة عامة حول الأصول بالنسبة إلى وقت التشغيل ووقت التعطل ووقت الإصلاح ومتوسط الوقت بين مرات الفشل (MTBF).

1. انقر فوق **إدارة الأصول** > **استعلامات** > **الأصول‏‎** > **مؤشرات الأداء الأساسية للأصول**.

2. في مربع الحوار **حساب مؤشرات الأداء الأساسية للأصول**، حدد **مقياس الوقت** الذي يجب استخدامه في الحساب، وفترة في الحقلين **من تاريخ** و **إلى تاريخ**. 

3. على علامة التبويب السريعة **السجلات المطلوب تضمينها**، يمكنك تحديد أصول وأنواع أصول معينة لتضمينها في الحساب، إذا كان ذلك مطلوبًا.

4. انقر فوق **موافق** لبدء الحساب.

5. على علامة التبويب السريعة **نظرة عامة**، تظهر نتائج الحساب في طريقة عرض الشبكة. يظهر كل أصل على بند منفصل.

6. على علامة التبويب السريعة **مؤشرات الأداء الأساسية للبند المحدد**، يمكنك أن ترى العمليات الحسابية للأصل المحدد **نظرة عامة**. يتم تصنيف قيم مؤشرات الأداء الأساسية بالنسبة إلى **الوقت** و **التوافر** و **أوامر العمل** و **الصيانة** و **الأخطاء** و **وقت تعطل الصيانة** و **التكلفة**.

في الجدول أدناه، ستجد وصفًا للحقول الموجودة في صفحة **مؤشرات الأداء الأساسية للأصول**.

| الحقل                   | الوصف                                                                                                                                                                                                                                                                                           |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| الأصل                   | معرف الأصل.                                                                                                                                                                                                                                                                                             |
| إجمالي الوقت              | إجمالي الوقت الذي تم إعداده في التقويم المستخدم في الحساب. إذا كان الأصل مرتبطًا بمورد، يتم استخدام تقويم المورد المرتبط. إذا لم يكن الأصل مرتبطًا بمورد، يتم استخدام التقويم المحدد في حقل **التقويم القياسي** في **محددات إدارة الأصول**. |
| وقت التشغيل‬                  | إجمالي الوقت يُطرح منه وقت التعطل                                                                                                                                                                                                                                                                            |
| وقت التوقف                | تسجيلات وقت تعطل الصيانة التي تتم على الأصل في الفترة المحددة.                                                                                                                                                                                                                              |
| وقت الإصلاح             | إجمالي عدد ساعات العمل المستهلكة في أوامر عمل الإصلاح.                                                                                                                                                                                                                                            |
| التوفر %          | وقت التشغيل‬ المقسوم على إجمالي الوقت ومضروب في 100.                                                                                                                                                                                                                                                   |
| عدد الأخطاء        | عدد أسباب الأخطاء المسجلة على اعراض الأخطاء الموجودة على الأصل في الفترة المحددة.                                                                                                                                                                                                             |
| متوسط الوقت بين حالات الفشل MTBF                    | متوسط الوقت بين حالات الفشل، وهو إجمالي الوقت المقسوم على عدد الأخطاء المسجلة في الأصل في الفترة المحددة. إذا كان عدد الأخطاء يساوي صفر، فسيتم تعيين MTBF إلى الوقت الإجمالي.                                                                                                                   |
| معدل الفشل               | 1 مقسوم على MTBF.                                                                                                                                                                                                                                                                                    |
| أداة إزالة البرامج الضارة (MRT)                     | متوسط وقت الإصلاح، وهو وقت الإصلاح المقسوم على عدد الأخطاء المسجلة في الأصل في الفترة المحددة. إذا كان عدد الأخطاء يساوي صفر، فسيتم تعيين MRT إلى وقت الإصلاح.                                                                                                                           |
| عدد عمليات التوقف         | عدد تسجيلات وقت تعطل الصيانة المنشأة على الأصل.                                                                                                                                                                                                                                     |
| MTBS                    | متوسط الوقت بين حالات التوقف، وهو إجمالي الوقت المقسوم على عدد تسجيلات وقت تعطل الصيانة. إذا كان عدد تسجيلات وقت تعطل الصيانة يساوي صفر في الفترة المحددة، يتم تعيين قيمة MTBS إلى إجمالي الوقت.                                                                                      |
| التكلفة الوقائية         | التكاليف المرحلة على الأصل المرتبطة بنوع التكلفة "وقائية" في الفترة المحددة. يتم إعداد أنواع التكلفة على أنواع أوامر العمل.                                                                                                                                                                       |
| التكلفة التصحيحية         | التكاليف المرحلة على الأصل المرتبطة بنوع التكلفة "تصحيحية" في الفترة المحددة. يتم إعداد أنواع التكلفة على أنواع أوامر العمل.                                                                                                                                                                       |
| قيمة الاستبدال       | القيمة المحددة في الأصل كتكلفة الإحلال.                                                                                                                                                                                                                                                  |
| نوع الأصل             | تعريف نوع الأصل المحدد في الأصل.                                                                                                                                                                                                                                             |
| الشركة المصنعة           | تعريف الشركة المصنعة المحددة في الأصل.                                                                                                                                                                                                                                                 |
| الطراز                   | تعريف طراز الشركة المصنعة المحدد في الأصل.                                                                                                                                                                                                                                           |
| من تاريخ               | تاريخ بدء حساب مؤشرات الأداء الأساسية. إذا تم إنشاء الأصل بعد تاريخ البدء المحدد للحساب، يظهر تاريخ بدء الأصل في هذا الحقل.                                                                                                                                  |
| إلى تاريخ                 | تاريخ انتهاء حساب مؤشرات الأداء الأساسية. إذا تم تسجيل الأصل كغير نشط قبل تاريخ الانتهاء المحدد للحساب، يظهر التاريخ الذي لم يعد الأصل نشطًا اعتبارًا منه في هذا الحقل.                                                                                               |
| مقياس الوقت              | اثناء حساب مؤشرات الأداء الأساسية، يمكنك تحديد مقياس الوقت الذي يجب استخدامه: الساعات أو الأيام أو الأسابيع.                                                                                                                                                                                                            |
| التوفر            | وقت التشغيل مقسوم على إجمالي الوقت.                                                                                                                                                                                                                                                                         |
| أوامر العمل             | العدد الإجمالي لأوامر العمل المضمنة في حساب مؤشرات الأداء الأساسية.                                                                                                                                                                                                                                          |
| وقت أمر العمل         | إجمالي عدد ساعات العمل المستهلكة على أوامر العمل.                                                                                                                                                                                                                                               |
| أوامر العمل الأساسية     | عدد أوامر العمل الرئيسية المضمنة في حساب مؤشرات الأداء الأساسية.                                                                                                                                                                                                                                        |
| أوامر العمل الثانوية   | عدد أوامر العمل الثانوية المضمنة في حساب مؤشرات الأداء الأساسية.                                                                                                                                                                                                                                      |
| أوامر عمل الصيانة | عدد أوامر عملي الصيانة المضمنة في حساب مؤشرات الأداء الأساسية. أمر عمل الصيانة هو أمر عمل من دون أسباب أخطاء متعلقة به.                                                                                                                                                             |
| وقت الصيانة        | إجمالي عدد ساعات العمل المستهلكة في أوامر عمل الصيانة.                                                                                                                                                                                                                                       |
| إصلاح أوامر العمل      | عدد أوامر عمل الإصلاح المضمنة في حساب مؤشرات الأداء الأساسية. أمر عمل الإصلاح هو أمر عمل من دون سبب خطأ متعلق به.                                                                                                                                                                        |
| الموثوقية %           | حساب يستند إلى التطور الأسي المتوقع في تسجيلات الأخطاء على أصل ما، مما يعني أن الأصل يصبح أقل موثوقية مع مرور الوقت بسبب كثرة استهلاكه. يستند حساب مؤشر الأداء الأساسي هذا إلى MTBF وإجمالي الوقت.                                                            |
| متوسط الوقت لحالات توقف الإنتاج MTPS                    | متوسط الوقت لحالات توقف الإنتاج، وهو وقت تعطل الصيانة المقسوم على عدد تسجيلات وقت تعطل الصيانة. إذا كان عدد تسجيلات وقت تعطل الصيانة يساوي صفر في الفترة المحددة، يتم تعيين قيمة MTPS إلى صفر.                                                                               |
| إجمالي التكلفة              | إجمالي التكاليف المرحلة على الأصل في الفترة المحددة.                                                                                                                                                                                                                                              |
| تكلفة الاستثمار         | التكاليف المرحلة على الأصل المرتبطة بنوع التكلفة "استثمار" في الفترة المحددة. يتم إعداد أنواع التكلفة على أنواع أوامر العمل.                                                                                                                                                                       |

يعرض الشكل أدناه لقطة شاشة لحساب مؤشرات الأداء الأساسية لأربعة أصول.

![لقطة لحساب مؤشر الأداء الرئيسي KPI لأربعة أصول.](media/11-controlling-and-reporting.png)

- يمكنك إجراء تحديد متعدد لعدة أصول في **جميع الأصول** والنقر فوق الزر **مؤشرات الأداء الأساسية للأصول** على علامة التبويب **عام**. بعد ذلك، انقر فوق **موافق** في مربع الحوار **حساب مؤشرات الأداء الأساسية للأصل** لحساب مؤشرات الأداء الأساسية للأصول المحددة.  
- قد تتضمن النتائج من حساب مؤشرات الأداء الأساسية أو قد لا تتضمن [تسجيلات وقت تعطل الصيانة](../work-orders/maintenance-downtime.md)، وهذا يتوقف على إعداد واستخدام أكواد أسباب وقت تعطل الصيانة. 



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]