---
title: إلغاء وظيفة التخطيط الرئيسي
description: يشرح هذا الموضوع كيفية إلغاء وظيفة تخطيط نشطة تستخدم وظيفة التخطيط المُضمن.
author: ChristianRytt
manager: AnnBe
ms.date: 01/10/2020
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
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 66d5b10e1471b98274d4049df18a2e53873f789a
ms.sourcegitcommit: 92cd55028be556a0bd41b6972c9c6d14b695dfa0
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/10/2020
ms.locfileid: "2947470"
---
# <a name="cancel-a-master-planning-job"></a>إلغاء وظيفة التخطيط الرئيسي

في Microsoft Dynamics 365 Supply Chain Management، هناك اختيارات متعددة لإلغاء وظيفة التخطيط الرئيسي. علي سبيل المثال، قد ترغب في إلغاء وظيفة تخطيط رئيسيه إذا تم تشغيلها عن طريق الخطأ أو انها تعمل لفتره أطول من المتوقع وتريد إنهائها. أفضل طريقة لإلغاء وظيفة التخطيط هي من صفحة **عمليات التخطيط غير المكتملة** . تُستخدم اختيارات بديلة من صفحات **الوظائف الدفعية‬** و **الوظائف الدفعية‬ المحسّنة** فقط في حالة عدم اكتمال إلغاء وظيفة التخطيط الرئيسية من صفحة **عمليات التخطيط غير المكتملة** في غضون بضع دقائق.

## <a name="preferred-cancel-option"></a>خيار الإلغاء المفضل
### <a name="cancel-master-planning-job-from-unfinished-planning-processes-page"></a>إلغاء وظيفة التخطيط الرئيسية من صفحة **عمليات التخطيط غير المكتملة** .
1. انتقل إلى **التخطيط الرئيسي‬ > الاستعلامات والتقارير‬ > التخطيط الرئيسي‬ > عمليات التخطيط غير المكتملة**.
2. حدد سطر عملية التخطيط التي تريد إلغاؤها.
3. وانقر فوق **إلغاء الأمر**.

## <a name="additional-cancel-options"></a>خيارات إلغاء إضافية
تُستخدم هذه فقط إذا لم يكتمل إلغاء وظيفة التخطيط الرئيسية من صفحة **عمليات التخطيط غير المكتملة** في غضون بضع دقائق.

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a>حذف وظيفة التخطيط الرئيسي من صفحة **الوظائف الدفعية** .
1. انتقل إلى **إدارة النظام > الاستعلامات > الوظائف الدفعية**.
2. حدد سطر وظيفة التخطيط التي تريد إلغاؤها.
3. انقر فوق **حذف**.

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a>حذف وظيفة التخطيط الرئيسية من صفحة **الوظائف الدفعية المُحسنة** .
1. انتقل إلى **إدارة النظام > الاستعلامات > الوظائف الدفعية**.
2. إذا لم يتم عرض معرف الوظيفة في القائمة، فانقر فوق **التبديل إلى النموذج المحسّن**، وإلا فتابع الخطوة التالية.
3. فتح الوظيفة الدفعية انقر فوق **معرف الوظيفة** للوظيفة الدفعية مع المهام التي تريد إنهائها.
4. في **الوظائف الدفعية**، حدد المهام المطلوب إنهاؤها.
5. في علامة التبويب السريعة **مهام الدُفعة** ، انقر فوق **إيقاف**.
