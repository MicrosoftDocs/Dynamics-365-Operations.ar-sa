---
title: "إزالة القيم المتطرفة من بيانات الحركة التاريخية عند حساب التنبؤ بالطلب"
description: "يصف هذا المقال كيفية استبعاد القيم المتطرفة من البيانات التاريخية التي يتم استخدامها لحساب التنبؤ بطلب. وباستبعاد الأخطاء، يمكنك تحسين دقة التنبؤ."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 72735c9e3fb4291076f0b577f45384dec319b2a7
ms.contentlocale: ar-sa
ms.lasthandoff: 05/25/2017

---

# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a>إزالة القيم المتطرفة من بيانات الحركة التاريخية عند حساب التنبؤ بالطلب

[!include[banner](../includes/banner.md)]


يصف هذا المقال كيفية استبعاد القيم المتطرفة من البيانات التاريخية التي يتم استخدامها لحساب التنبؤ بطلب. وباستبعاد الأخطاء، يمكنك تحسين دقة التنبؤ.

يمكنك استبعاد القيم المتطرفة لتحسين دقة التنبؤ. هذه المهمة اختيارية. وفيما يلي نظرة عامة على العملية:

1.  انقر فوق **التخطيط الرئيسي** &gt; **إعداد‏‎** &gt; **التنبؤ بالطلب** &gt; **‎إزالة الأخطاء** لفتح صفحة **إزالة الأخطاء**، حيث يمكنك استخدام استعلام لتحديد الحركات لاستبعادها.
2.  حدد الشركة التي ينطبق عليها الاستعلام، ثم أدخل اسمًا ووصفًا. ويتم تعيين حقل **تاريخ الاستعلام** تلقائياً تعيين إلى التاريخ الحالي.
3.  حدد خانة الاختيار **نشطة** لاستبعاد الحركات التي تم العثور عليها من قِبل الاستعلام من البيانات التاريخية. سيتم تطبيق هذا الإعداد عند إنشاء تنبؤ أساسي.
4.  في صفحة **استعلام إزالة الأخطاء‬**، يمكنك إضافة وإزالة وتحديد المعايير التي تحدد الحركات التي سيتم استبعادها عندما يتم حساب التنبؤ الأساسي. على سبيل المثال، حدد صنف أو حركة أمر معين تريد استبعادها.
5.  انقر فوق **عرض الحركات**. تسرد صفحة **حركات الأخطاء** الحركات التي تفي بالمعيار المحدد في الاستعلام والتي سيتم استبعاده من البيانات التاريخية عند حساب التنبؤ بالطلب.

**ملاحظة:** يمكنك أيضًا إنشاء استعلام يستند إلى استعلام موجود. حدد الاستعلام المراد نسخه، ثم انقر فوق **نسخ**. يحدد حقل **تاريخ الاستعلام** الإصدار. يمكنك استخدام الاستعلام كما هو، أو يمكنك النقر فوق **تحرير استعلام** لتعديل المعايير. ويمكنك بشكل اختياري تعديل اسم ووصف الاستعلام الجديد.

<a name="see-also"></a>راجع أيضًا
--------

[مقدمة إلى التنبؤ بالطلب](introduction-demand-forecasting.md)

[مراقبة دقة التنبؤ](monitor-forecast-accuracy.md)



