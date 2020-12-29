---
title: إنشاء الأبعاد واستيراد أعضاء الأبعاد
description: تعتبر محاسبة التكاليف وحدة نمطية مستقلة تحتاج إلى بيانات رئيسية من الوحدات النمطية الأخرى.
author: ShylaThompson
manager: AnnBe
ms.date: 09/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 256254
ms.assetid: e1b0a6e3-0c72-4a7d-90e1-20f870c6dbad
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d61358be79adc943572bb4a5d624cb7c80b52e6e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439975"
---
# <a name="create-dimensions-and-import-dimension-members"></a>إنشاء الأبعاد واستيراد أعضاء الأبعاد

[!include [banner](../includes/banner.md)]

تعتبر محاسبة التكاليف وحدة نمطية مستقلة تحتاج إلى بيانات من الوحدات النمطية الأخرى. تم تصنيف هذه البيانات على الشكل التالي:

-  عناصر التكلفة
-  كائنات التكلفة
-  الأبعاد الإحصائية

يتطابق **عنصر التكلفة** مع عنصر ذي صلة بالتكلفة في دليل الحسابات. يتطابق **كائن التكلفة** مع أي نوع من أنواع الأبعاد المالية، مثل المنتجات ومراكز التكلفة والمشاريع التي تريدها لتقدير التكاليف أو توزيها أو قياسها مباشرة. يتم استخدام **البُعد الإحصائي** وأعضاء هذا البُعد لتسجيل الإدخالات غير النقدية. يمكن استخدام أعضاء الأبعاد الإحصائية كأساس تخصيص في توزيع التكلفة وتخصيصها. 

يوضح المخطط التالي الأبعاد المستخدمة في محاسبة التكاليف.

[![أبعاد محاسبة التكاليف](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)

بعد استيراد البيانات إلى محاسبة التكاليف، يمكنك استخدامها لإنشاء منظورات مختلفة توفر معلومات دقيقة إلى المدراء على جميع مستويات المؤسسة. توفر الموضوعات التالية معلومات حول إنشاء الأبعاد واستيراد أعضاء الأبعاد. 

-  [أبعاد عنصر التكلفة](cost-elements.md)
-  [إنشاء عناصر تكلفة](./tasks/create-cost-elements.md)
-  [أبعاد كائن التكلفة](cost-objects.md)
-  [تعيين أعضاء أبعاد عنصر التكلفة لمجموعة شائعة من أعضاء الأبعاد](map-cost-elements-dimension-members.md)
-  [تعيين بُعد عنصر التكلفة](./tasks/map-cost-element-dimension.md)
-  [أعضاء الأبعاد الإحصائية وقوالب موفري القياسات الإحصائية​](statistical-measure-provider-template.md)






