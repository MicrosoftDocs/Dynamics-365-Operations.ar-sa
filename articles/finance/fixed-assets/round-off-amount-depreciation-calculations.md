---
title: المبلغ التقريبي لعمليات حساب الإهلاك
description: تتناول هذه المقالة حقل "تقريب الإهلاك" الموجود في صفحات إعداد الدفتر.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0bf7cf68c98b14fb6c206c99673168153b32a449
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830413"
---
# <a name="round-off-amount-for-depreciation-calculations"></a>المبلغ التقريبي لعمليات حساب الإهلاك

[!include [banner](../includes/banner.md)]

تتناول هذه المقالة حقل "تقريب الإهلاك" الموجود في صفحات إعداد الدفتر.

‏‫يتم تعيين مبالغ تقريب الإهلاك لكل دفتر. وتُستخدم مبالغ الإهلاك التقريبية في ملف تعريف إهلاك الأصول الثابتة، الذي يوضح الإهلاك المستقبلي وقيمة الأصل الثابت، وكذلك في مقترحات الإهلاك.‬ أدخل الحد الأدنى لمبلغ إهلاك المسموح به للدفتر. 

وبغض النظر عن التقريب الذي تم إعداده، يتم تقريب مبلغ الإهلاك في فترة الإهلاك الأخيرة. وفي نهاية فترة الإهلاك الأخيرة، يجب أن تكون قيمة الأصل الثابت 0 (صفر) أو قيمة الخردة، إذا تم استخدام قيمة الخردة.

### <a name="example"></a>مثال

يتم حساب الإهلاك بدون أي تقريب على شكل 2,444.44. وكما يُظهر الجدول التالي، تختلف المبالغ المقترحة، استنادًا إلى كيفية إعداد التقريب.

| أسلوب التقريب | مبلغ الإهلاك |
|-----------------|---------------------|
| التقريب 0.1    | 2,444.40            |
| التقريب 1.00   | 2,444.00            |
| التقريب 10.00  | 2,440.00            |
| التقريب 100.00 | 2,400.00            |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]