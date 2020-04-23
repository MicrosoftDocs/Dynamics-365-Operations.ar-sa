---
title: رصد دقة التنبؤ​
description: يوضح هذا الموضوع  أنواع دقة التنبؤ التي يحسبها Dynamics 365 Supply Chain Management، وتشرح لك كيف يمكنك عرض قيم الدقة.
author: roxanadiaconu
manager: tfehr
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ab74ba88ba9eb683107ef82bc105f5a3ed8fac08
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209802"
---
# <a name="monitor-forecast-accuracy"></a>رصد دقة التنبؤ​

[!include [banner](../includes/banner.md)]

يوضح هذا الموضوع  أنواع دقة التنبؤ التي يحسبها Dynamics 365 Supply Chain Management الخاص بشركة Microsoft، وتشرح لك كيف يمكنك عرض قيم الدقة.

يحسب Supply Chain Management الأنواع التالية من دقة التنبؤ:

-   دقة التنبؤ التاريخي، عن طريق مقارنة التنبؤ التاريخي الذي يستخدمه "التخطيط الرئيسي" مع الطلب التاريخي. لعرض القيم (كل من القيم المطلقة والنسب المئوية) لدقة التنبؤ التاريخي، انقر فوق **إظهار الدقة** على الصفحة **تفاصيل التنبؤ بالطلب**.
-   الدقة المقدرة لنموذج التنبؤ الذي يتم استخدامه لإنشاء التنبؤات. يمكنك عرض النسبة المئوية للدقة ضمن **تفاصيل النموذج -متوسط النسبة المئوية المطلقة للخطأ** على الصفحة **تفاصيل التنبؤ بالطلب**. 

> [!NOTE]
> إذا كنت تستخدم Machine Learning من Microsoft Azure للتنبؤ بالطلب، يستند حساب دقة النموذج الداخلي إلى مجموعة بيانات الاختبار. لتحديد حجم مجموعة بيانات الاختبار، قم بضبط المعلمة **TEST\_SET\_SIZE\_PERCENT** في الصفحة **معلمات التنبؤ بالطلب**. على سبيل المثال، إذا قمت بتعيين القيمة إلى **20**، فإنه سيتم استخدام نسبة 20% الأخيرة من البيانات المسجلة لحساب دقة النموذج الداخلي.


<a name="additional-resources"></a>الموارد الإضافية
--------

[تخويل ‏‫التنبؤ الذي تمت تسويته](authorize-adjusted-forecast.md)

[إزالة القيم المتطرفة من بيانات الحركة التاريخية عند حساب التنبؤ بالطلب](remove-historical-outliers-calculating-demand-forecast.md)



