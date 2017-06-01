---
title: "مراقبة دقة التنبؤ"
description: "توضح هذه المقالة أنواع دقة التنبؤ الذي يقوم Microsoft Dynamics 365 for Operations بحسابه وتشرح كيف يمكنك عرض قيم الدقة."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 580b45263b45e6ef730b0fac32575fcdd9c358b6
ms.contentlocale: ar-sa
ms.lasthandoff: 05/25/2017


---

# <a name="monitor-forecast-accuracy"></a>مراقبة دقة التنبؤ

[!include[banner](../includes/banner.md)]


توضح هذه المقالة أنواع دقة التنبؤ الذي يقوم Microsoft Dynamics 365 for Operations بحسابه وتشرح كيف يمكنك عرض قيم الدقة.

يحسب Dynamics 365 for Operations الأنواع التالية من دقة التنبؤ:

-   دقة التنبؤ التاريخي، عن طريق مقارنة التنبؤ التاريخي الذي يستخدمه "التخطيط الرئيسي" مع الطلب التاريخي. لعرض القيم (كل من القيم المطلقة والنسب المئوية) لدقة التنبؤ التاريخي، انقر فوق **إظهار الدقة** على الصفحة **تفاصيل التنبؤ بالطلب**.
-   الدقة المقدرة لنموذج التنبؤ الذي يتم استخدامه لإنشاء التنبؤات. يمكنك عرض النسبة المئوية للدقة ضمن **تفاصيل النموذج -متوسط النسبة المئوية المطلقة للخطأ** على الصفحة **تفاصيل التنبؤ بالطلب**. 

**ملاحظة:** إذا كنت تستخدم التنبؤ بطلب Dynamics 365 for Operations لخدمة Microsoft Azure Machine Learning، فإن حساب دقة نموذج داخلي يستند إلى مجموعة بيانات الاختبار. لتحديد حجم مجموعة بيانات الاختبار، قم بضبط المعلمة **TEST\_SET\_SIZE\_PERCENT** في الصفحة **معلمات التنبؤ بالطلب**. على سبيل المثال، إذا قمت بتعيين القيمة إلى **20**، فإنه سيتم استخدام نسبة 20% الأخيرة من البيانات المسجلة لحساب دقة النموذج الداخلي.


<a name="see-also"></a>راجع أيضًا
--------

[تخويل ‏‫التنبؤ الذي تمت تسويته](authorize-adjusted-forecast.md)

[إزالة القيم المتطرفة من بيانات الحركة القديمة عند حساب التنبؤ بالطلب](remove-historical-outliers-calculating-demand-forecast.md)




