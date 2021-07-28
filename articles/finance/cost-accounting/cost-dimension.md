---
title: إنشاء الأبعاد واستيراد أعضاء الأبعاد
description: تعتبر محاسبة التكاليف وحدة نمطية مستقلة تحتاج إلى بيانات رئيسية من الوحدات النمطية الأخرى.
author: ShylaThompson
ms.date: 09/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: roschlom
ms.custom: 256254
ms.assetid: e1b0a6e3-0c72-4a7d-90e1-20f870c6dbad
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 09dd9e2d648bec32d1504175dbb1470751e5c915
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/06/2021
ms.locfileid: "6355169"
---
# <a name="create-dimensions-and-import-dimension-members"></a>إنشاء الأبعاد واستيراد أعضاء الأبعاد

[!include [banner](../includes/banner.md)]

تعتبر محاسبة التكاليف وحدة نمطية مستقلة تحتاج إلى بيانات من الوحدات النمطية الأخرى. تم تصنيف هذه البيانات على الشكل التالي:

-  عناصر التكلفة
-  كائنات التكلفة
-  الأبعاد الإحصائية

يتطابق **عنصر التكلفة** مع عنصر ذي صلة بالتكلفة في دليل الحسابات. يتطابق **كائن التكلفة** مع أي نوع من أنواع الأبعاد المالية، مثل المنتجات ومراكز التكلفة والمشاريع التي تريدها لتقدير التكاليف أو توزيها أو قياسها مباشرة. يتم استخدام **البُعد الإحصائي** وأعضاء هذا البُعد لتسجيل الإدخالات غير النقدية. يمكن استخدام أعضاء الأبعاد الإحصائية كأساس تخصيص في توزيع التكلفة وتخصيصها. 

يوضح المخطط التالي الأبعاد المستخدمة في محاسبة التكاليف.

[![أبعاد محاسبة التكاليف.](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)

بعد استيراد البيانات إلى محاسبة التكاليف، يمكنك استخدامها لإنشاء منظورات مختلفة توفر معلومات دقيقة إلى المدراء على جميع مستويات المؤسسة. توفر الموضوعات التالية معلومات حول إنشاء الأبعاد واستيراد أعضاء الأبعاد. 

-  [أبعاد عنصر التكلفة](cost-elements.md)
-  [إنشاء عناصر تكلفة](./tasks/create-cost-elements.md)
-  [أبعاد كائن التكلفة](cost-objects.md)
-  [تعيين أعضاء أبعاد عنصر التكلفة لمجموعة شائعة من أعضاء الأبعاد](map-cost-elements-dimension-members.md)
-  [تعيين بُعد عنصر التكلفة](./tasks/map-cost-element-dimension.md)
-  [أعضاء الأبعاد الإحصائية وقوالب موفري القياسات الإحصائية​](statistical-measure-provider-template.md)








[!INCLUDE[footer-include](../../includes/footer-banner.md)]