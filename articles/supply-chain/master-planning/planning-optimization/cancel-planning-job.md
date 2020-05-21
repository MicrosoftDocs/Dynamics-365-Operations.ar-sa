---
title: إلغاء وظيفة تخطيط
description: يوضح هذا الموضوع كيفية إلغاء وظيفة تخطيط نشطة تستخدم وظيفة تحسين التخطيط.
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 4b65d344cd764740cc1485969c2fc4c2052e55e2
ms.sourcegitcommit: 68092ed283bfbb7b6f611cce1b62c791f9b6a208
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/30/2020
ms.locfileid: "3323452"
---
# <a name="cancel-a-planning-job"></a>إلغاء وظيفة تخطيط

[!include [banner](../../includes/banner.md)]

في Microsoft Dynamics 365 Supply Chain Management، يمكنك إلغاء وظيفة تخطيط نشطة تستخدم وظيفة تحسين التخطيط. عندما تقوم بتحديد **إلغاء** في مربع الحوار عند تشغيل مهمة تحسين التخطيط مباشرة من واجهة المستخدم (غير موجودة في الخلفية)، فلن يؤدي ذلك إلى إلغاء مهمة تحسين التخطيط. حتى إذا تلقيت تحذيرًا مثل "تم إلغاء العملية"، فإنك ستظل بحاجة إلى استخدام الخطوات التالية لإلغاء مهمة تخطيط بتحسين التخطيط.


لإلغاء وظيفة تخطيط نشطة، اتبع الخطوات التالية. 

> [!NOTE]
> يمكن إلغاء الوظائف النشطة فقط.

1. انتقل إلى **التخطيط الرئيسي \> الإعداد \> الخطط**.
2. حدد خطة مناسبة لتشغيل التخطيط.
3. حدد **المحفوظات**.
4. حدد وظيفة التخطيط المراد إلغاؤها.
5. حدد **إلغاء الأمر**.

ستكون حالة الوظيفة **قيد الإلغاء** حتى تؤكد خدمة تحسين التخطيط أنه تم إلغاء الوظيفة. سيتم تغيير الحالة بعد ذلك إلى **تم الإلغاء**.

> [!NOTE]
> لرؤية تغييرات الحالة، يجب تحديث الصفحة بتحديد الزر **تحديث**.

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على تحسين التخطيط‬](planning-optimization-overview.md)

[بدء تحسين التخطيط](get-started.md)

[تحليل ملاءمة تحسين التخطيط](planning-optimization-fit-analysis.md)

[عرض سجل محفوظات الخطط والتخطيط](plan-history-logs.md)

[تطبيق عوامل تصفية على خطة](plan-filters.md)
