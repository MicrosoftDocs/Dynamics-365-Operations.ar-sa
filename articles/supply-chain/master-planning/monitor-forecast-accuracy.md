---
title: "مراقبة دقة التنبؤ"
description: "توضح هذه المقالة أنواع دقة التنبؤ الذي يقوم Microsoft Dynamics 365 for Finance and Operations بحسابه وتشرح كيف يمكنك عرض قيم الدقة."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1f54251b6f6937c59293bd44a0fc27272ffd3d55
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---

# <a name="monitor-forecast-accuracy"></a>مراقبة دقة التنبؤ

[!include [banner](../includes/banner.md)]

توضح هذه المقالة أنواع دقة التنبؤ الذي يقوم Microsoft Dynamics 365 for Finance and Operations بحسابه وتشرح كيف يمكنك عرض قيم الدقة.

يحسب Finance and Operations الأنواع التالية من دقة التنبؤ:

-   دقة التنبؤ التاريخي، عن طريق مقارنة التنبؤ التاريخي الذي يستخدمه "التخطيط الرئيسي" مع الطلب التاريخي. لعرض القيم (كل من القيم المطلقة والنسب المئوية) لدقة التنبؤ التاريخي، انقر فوق **إظهار الدقة** على الصفحة **تفاصيل التنبؤ بالطلب**.
-   الدقة المقدرة لنموذج التنبؤ الذي يتم استخدامه لإنشاء التنبؤات. يمكنك عرض النسبة المئوية للدقة ضمن **تفاصيل النموذج -متوسط النسبة المئوية المطلقة للخطأ** على الصفحة **تفاصيل التنبؤ بالطلب**. 

**ملاحظة:** إذا كنت تستخدم التنبؤ بالطلب Finance and Operations لخدمة التعلم الآلي من Microsoft Azure، فإن حساب دقة النموذج الداخلي يستند إلى مجموعة بيانات الاختبار. لتحديد حجم مجموعة بيانات الاختبار، قم بضبط المعلمة **TEST\_SET\_SIZE\_PERCENT** في الصفحة **معلمات التنبؤ بالطلب**. على سبيل المثال، إذا قمت بتعيين القيمة إلى **20**، فإنه سيتم استخدام نسبة 20% الأخيرة من البيانات المسجلة لحساب دقة النموذج الداخلي.


<a name="additional-resources"></a>الموارد الإضافية
--------

[تخويل ‏‫التنبؤ الذي تمت تسويته](authorize-adjusted-forecast.md)

[إزالة القيم المتطرفة من بيانات الحركة التاريخية عند حساب التنبؤ بالطلب](remove-historical-outliers-calculating-demand-forecast.md)




