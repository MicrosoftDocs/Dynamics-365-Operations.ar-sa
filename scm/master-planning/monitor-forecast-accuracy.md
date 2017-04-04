---
title: "التنبؤ بدقة جهاز العرض"
description: "توضح هذه المقالة أنواع التنبؤ دقة حساب Microsoft Dynamics 365 للعمليات وتوضح هذه المقالة كيفية عرض قيم الدقة."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d3f88a4fa54217cea909c54955de05e2175db0cd
ms.lasthandoff: 03/29/2017


---

# <a name="monitor-forecast-accuracy"></a>التنبؤ بدقة جهاز العرض

توضح هذه المقالة أنواع التنبؤ دقة حساب Microsoft Dynamics 365 للعمليات وتوضح هذه المقالة كيفية عرض قيم الدقة.

ديناميكيات 365 لعمليات حساب الأنواع التالية من دقة التنبؤ:

-   دقة التنبؤ التاريخي، عن طريق مقارنة التنبؤ التاريخي الذي يستخدمه "التخطيط الرئيسي" مع الطلب التاريخي. لعرض القيم (كل من القيم المطلقة والنسب المئوية) لدقة التنبؤ التاريخي، انقر فوق **إظهار الدقة** على الصفحة **تفاصيل التنبؤ بالطلب**.
-   الدقة المقدرة لنموذج التنبؤ الذي يتم استخدامه لإنشاء التنبؤات. يمكنك عرض النسبة المئوية للدقة ضمن **تفاصيل النموذج -متوسط النسبة المئوية المطلقة للخطأ ** على الصفحة **تفاصيل التنبؤ بالطلب**. 

**ملاحظة:** إذا استخدمت 365 ديناميات الطلب على عمليات تقدير خدمة Microsoft Azure آلة التعلم، يستند حساب دقة نموذج داخلي على مجموعة بيانات الاختبار. لتحديد حجم مجموعة بيانات الاختبار، قم **اختبار\_تعيين\_حجم\_نسبة** المعلمة في **تقدير معلمات الطلب** الصفحة. على سبيل المثال، إذا قمت بتعيين القيمة إلى **20**، فإنه سيتم استخدام نسبة 20% الأخيرة من البيانات المسجلة لحساب دقة النموذج الداخلي.


<a name="see-also"></a>راجع أيضًا
--------

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)

[Remove outliers from historical transaction data when calculating a demand forecast](remove-historical-outliers-calculating-demand-forecast.md)


