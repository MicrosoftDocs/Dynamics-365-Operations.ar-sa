---
title: تكوين معلمات البيع بالتجزئة التي تؤثر على كشوف حساب البيع بالتجزئة
description: يوضح هذا الموضوع تكوينات معلمات البيع بالتجزئة التي تؤثر على كيفية إنشاء كشوفات حساب البيع بالتجزئة وترحيلها.
author: josaw1
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b9a0386a4d61395903e82d988244dd131c1febaf
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867261"
---
# <a name="configure-retail-parameters-that-affect-retail-statements"></a>تكوين معلمات البيع بالتجزئة التي تؤثر على كشوف حساب البيع بالتجزئة

[!include[task guide banner](../includes/task-guide-banner.md)]

يوضح هذا الموضوع تكوينات معلمات البيع بالتجزئة التي تؤثر على كيفية إنشاء كشوفات حساب البيع بالتجزئة وترحيلها. يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USRT.

1. في جزء التنقل، انتقل إلى **الوحدات النمطية > البيع بالتجزئة والتجارة > إعداد المراكز الرئيسية ‬ > المعلمات > معلمات البيع بالتجزئة‬**.
2. حدد علامة تبويب **الترحيل**.
    - حدد **نعم** إذا أردت تريد ترحيل مبالغ الخصم الدوري على وجه التحديد.  
    - حدد **قياسي** لاستخدام الحسابات الافتراضية، أو حدد **دوري** إذا كنت تريد تحديد الحساب المراد استخدامه لكل خصم دوري.  
      - حدد **الملخص** إذا كان ينبغي تجميع بنود المخزون كلما كان ذلك ممكنًا.  
      - حدد **نعم** إذا كان ينبغي تسوية الفواتير والمدفوعات تلقائيًا كجزء من عملية ترحيل كشف الحساب.  
      - حدد **نعم** إذا كان ينبغي تجميع حركات الإيداع بالخزينة.  
      - حدد **نعم** إذا كان ينبغي تجميع حركات الإيداع البنكي.  
      - حدد **نعم** لتشغيل التجميع لترحيل كشف الحساب.  
      - حدد **نعم** لإنشاء الأوامر ومعالجتها بالتوازي عند ترحيل كشوفات الحساب.  
      - أدخل الحد الأقصى للأوامر التي سيتم معالجتها في كل مهمة وظيفة دفعية.  
3. حدد **حفظ**.

