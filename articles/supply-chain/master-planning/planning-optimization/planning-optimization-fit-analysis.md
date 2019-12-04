---
title: تحليل ملاءمة تحسين التخطيط
description: يشرح هذا الموضوع كيفيه التحقق من صحة الاعداد والبيانات الحالية في مقابل قدرات وظيفة تحسين التخطيط.
author: ChristianRytt
manager: AnnBe
ms.date: 1030/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 26b067f8526df16474c0ab52d0abf816170ff5cb
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773894"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="planning-optimization-fit-analysis"></a>تحليل ملاءمة تحسين التخطيط

لمعرفه مدى توافق الاعداد والبيانات الحالية مع وظيفة تحسين التخطيط، انتقل إلى **التخطيط الرئيسي**\> **الإعداد** \>**تحليل ملائمة تحسين التخطيط**، ثم حدد **تشغيل التحليل**. إذا عثر التحليل علي إيه حالات عدم اتساق ، سيتم ادراجها في نفس الصفحة. (قد تستغرق عمليه التحليل بضع دقائق ليتم تشغيلها.)

> [!NOTE]
> إذا تم العثور علي حالات عدم تناسق ، فلا يزال بإمكانك استخدام تحسين التخطيط. تعرض نتائج تحليل الملائمة فقط الأماكن التي لا تقوم فيها خدمه التخطيط بالسماح بعمليه الاعداد الحالية. بمعني آخر ، تعرض الأماكن التي قد يتم فيها تجاهل بعض العمليات أو عدم اعتمادها.

## <a name="analysis-results-example-1"></a>نتائج التحليل: مثال 1

- **الميزة:** الإنتاج
- **المشكلة:** الأصناف التي بها مستوى قائمة مكونات أصناف أكبر من الصفر: 56
- **التوضيح:** عثر التحليل الملائم على 56 عنصرًا يحتوي على إعداد قائمة مكونات الصنف (BOM) للإنتاج. ونظرا لان الإصدار الحالي من تحسين التخطيط لا يدعم الإنتاج ، سيقوم تحسين التخطيط بإنشاء أوامر شراء مخططه بدلا من أوامر الإنتاج المخططة. سيعرض أيضًا تحذيرًا يسرد العناصر المتأثره.

### <a name="analysis-results-example-2"></a>نتائج التحليل: مثال 2

- **الميزة:** الإجراءات
- **المشكلة:** مجموعات التغطية مع تمكين حساب الإجراءات: 6
- **التوضيح:** عثر تحليل الملائمة على ست مجموعات تغطيه حيث يتم تشغيل حساب الإجراء. ونظرا لان الإصدار الحالي من تحسين التخطيط لا يدعم الإجراءات ، فلن يتم إنشاء إيه إجراءات اثناء التخطيط الرئيسي.

## <a name="related-resources"></a>الموارد ذات الصلة

[نظرة عامة على تحسين التخطيط‬](planning-optimization-overview.md)

[بدء تحسين التخطيط](get-started.md)

[عرض سجل محفوظات الخطط والتخطيط](plan-history-logs.md)

[تطبيق عوامل تصفية على خطة](plan-filters.md)

[إلغاء وظيفة تخطيط](cancel-planning-job.md)
