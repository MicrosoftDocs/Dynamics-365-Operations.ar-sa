---
title: إزالة القيم المتطرفة من بيانات الحركة التاريخية عند حساب التنبؤ بالطلب
description: يصف هذا المقال كيفية استبعاد القيم المتطرفة من البيانات التاريخية التي يتم استخدامها لحساب التنبؤ بطلب. وباستبعاد الأخطاء، يمكنك تحسين دقة التنبؤ.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup, ReqDemPlanOutlierQueryPreview
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9dec963ed5abd6f77e82029a3ea5ba1a69d44e36
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421239"
---
# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a>إزالة القيم المتطرفة من بيانات الحركة التاريخية عند حساب التنبؤ بالطلب

[!include [banner](../includes/banner.md)]

يصف هذا المقال كيفية استبعاد القيم المتطرفة من البيانات التاريخية التي يتم استخدامها لحساب التنبؤ بطلب. وباستبعاد الأخطاء، يمكنك تحسين دقة التنبؤ.

يمكنك استبعاد القيم المتطرفة لتحسين دقة التنبؤ. هذه المهمة اختيارية. وفيما يلي نظرة عامة على العملية:

1.  انقر فوق **التخطيط الرئيسي** &gt; **إعداد‏‎** &gt; **التنبؤ بالطلب** &gt; **‎إزالة الأخطاء** لفتح صفحة **إزالة الأخطاء**، حيث يمكنك استخدام استعلام لتحديد الحركات لاستبعادها.
2.  حدد الشركة التي ينطبق عليها الاستعلام، ثم أدخل اسمًا ووصفًا. ويتم تعيين حقل **تاريخ الاستعلام** تلقائياً تعيين إلى التاريخ الحالي.
3.  حدد خانة الاختيار **نشطة** لاستبعاد الحركات التي تم العثور عليها من قِبل الاستعلام من البيانات التاريخية. سيتم تطبيق هذا الإعداد عند إنشاء تنبؤ أساسي.
4.  في صفحة **استعلام إزالة الأخطاء‬**، يمكنك إضافة وإزالة وتحديد المعايير التي تحدد الحركات التي سيتم استبعادها عندما يتم حساب التنبؤ الأساسي. على سبيل المثال، حدد صنف أو حركة أمر معين تريد استبعادها.
5.  انقر فوق **عرض الحركات**. تسرد صفحة **حركات الأخطاء** الحركات التي تفي بالمعيار المحدد في الاستعلام والتي سيتم استبعاده من البيانات التاريخية عند حساب التنبؤ بالطلب.

**ملاحظة:** يمكنك أيضًا إنشاء استعلام يستند إلى استعلام موجود. حدد الاستعلام المراد نسخه، ثم انقر فوق **نسخ**. يحدد حقل **تاريخ الاستعلام** الإصدار. يمكنك استخدام الاستعلام كما هو، أو يمكنك النقر فوق **تحرير استعلام** لتعديل المعايير. ويمكنك بشكل اختياري تعديل اسم ووصف الاستعلام الجديد.

<a name="additional-resources"></a>الموارد الإضافية
--------

[نظرة عامة على التنبؤ بالطلب‬](introduction-demand-forecasting.md)

[رصد دقة التنبؤ​](monitor-forecast-accuracy.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]