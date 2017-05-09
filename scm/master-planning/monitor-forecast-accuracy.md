---
title: "مراقبة دقة التنبؤ"
description: "توضح هذه المقالة أنواع دقة التنبؤ الذي يقوم Microsoft Dynamics 365 for Operations بحسابه وتشرح كيف يمكنك عرض قيم الدقة."
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

# <a name="monitor-forecast-accuracy"></a>مراقبة دقة التنبؤ

[!include[banner](../includes/banner.md)]


توضح هذه المقالة أنواع دقة التنبؤ الذي يقوم Microsoft Dynamics 365 for Operations بحسابه وتشرح كيف يمكنك عرض قيم الدقة.

يحسب Dynamics 365 for Operations الأنواع التالية من دقة التنبؤ:

-   دقة التنبؤ التاريخي، عن طريق مقارنة التنبؤ التاريخي الذي يستخدمه "التخطيط الرئيسي" مع الطلب التاريخي. لعرض القيم (كل من القيم المطلقة والنسب المئوية) لدقة التنبؤ التاريخي، انقر فوق **إظهار الدقة** على الصفحة **تفاصيل التنبؤ بالطلب**.
-   الدقة المقدرة لنموذج التنبؤ الذي يتم استخدامه لإنشاء التنبؤات. يمكنك عرض النسبة المئوية للدقة ضمن **تفاصيل النموذج -متوسط النسبة المئوية المطلقة للخطأ ** على الصفحة **تفاصيل التنبؤ بالطلب**. 

**ملاحظة:** إذا كنت تستخدم التنبؤ بطلب Dynamics 365 for Operations لخدمة Microsoft Azure Machine Learning، فإن حساب دقة نموذج داخلي يستند إلى مجموعة بيانات الاختبار. لتحديد حجم مجموعة بيانات الاختبار، قم بضبط المعلمة **TEST\_SET\_SIZE\_PERCENT** في الصفحة **معلمات التنبؤ بالطلب**. على سبيل المثال، إذا قمت بتعيين القيمة إلى **20**، فإنه سيتم استخدام نسبة 20% الأخيرة من البيانات المسجلة لحساب دقة النموذج الداخلي.


<a name="see-also"></a>راجع أيضًا
--------

[تخويل ‏‫التنبؤ الذي تمت تسويته](authorize-adjusted-forecast.md)

[إزالة القيم المتطرفة من بيانات الحركة القديمة عند حساب التنبؤ بالطلب](remove-historical-outliers-calculating-demand-forecast.md)




