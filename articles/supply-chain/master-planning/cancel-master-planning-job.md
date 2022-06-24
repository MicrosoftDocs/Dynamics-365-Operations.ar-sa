---
title: إلغاء وظيفة التخطيط الرئيسي
description: يشرح هذا المقال كيفية إلغاء وظيفة تخطيط نشطة تستخدم وظيفة التخطيط المُضمن.
author: t-benebo
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace, ReqProcessList
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6a9667be9921fdde7e1ca5de68c7f51d48905ac8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860772"
---
# <a name="cancel-a-master-planning-job"></a>إلغاء وظيفة التخطيط الرئيسي

[!include [banner](../includes/banner.md)]

في Microsoft Dynamics 365 Supply Chain Management، هناك اختيارات متعددة لإلغاء وظيفة التخطيط الرئيسي. على سبيل المثال، قد ترغب في إلغاء وظيفة تخطيط رئيسيه إذا تم تشغيلها عن طريق الخطأ أو انها تعمل لفتره أطول من المتوقع وتريد إنهائها. أفضل طريقة لإلغاء وظيفة التخطيط هي من صفحة **عمليات التخطيط غير المكتملة** . تُستخدم اختيارات بديلة من صفحات **الوظائف الدفعية‬** و **الوظائف الدفعية‬ المحسّنة** فقط في حالة عدم اكتمال إلغاء وظيفة التخطيط الرئيسية من صفحة **عمليات التخطيط غير المكتملة** في غضون بضع دقائق.

## <a name="preferred-cancel-option"></a>خيار الإلغاء المفضل
### <a name="cancel-master-planning-job-from-unfinished-planning-processes-page"></a>إلغاء وظيفة التخطيط الرئيسية من صفحة **عمليات التخطيط غير المكتملة** .
1. انتقل إلى **التخطيط الرئيسي‬ > الاستعلامات والتقارير‬ > التخطيط الرئيسي‬ > عمليات التخطيط غير المكتملة**.
2. حدد سطر عملية التخطيط التي تريد إلغاؤها.
3. وانقر فوق **إلغاء الأمر**.

## <a name="additional-cancel-options"></a>خيارات إلغاء إضافية
تُستخدم هذه فقط إذا لم يكتمل إلغاء وظيفة التخطيط الرئيسي من صفحة **عمليات التخطيط غير المكتملة** في غضون بضع دقائق.

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a>حذف وظيفة التخطيط الرئيسي من صفحة **الوظائف الدفعية** .
1. انتقل إلى **إدارة النظام > الاستعلامات > الوظائف الدفعية**.
2. حدد سطر وظيفة التخطيط التي تريد إلغاؤها.
3. انقر فوق **حذف**.

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a>حذف وظيفة التخطيط الرئيسية من صفحة **الوظائف الدفعية المُحسنة** .
1. انتقل إلى **إدارة النظام > الاستعلامات > الوظائف الدفعية**.
2. إذا لم يتم عرض معرف الوظيفة في القائمة، فانقر فوق **التبديل إلى النموذج المحسّن**، وإلا فتابع الخطوة التالية.
3. فتح الوظيفة الدفعية انقر فوق **معرف الوظيفة** للوظيفة الدفعية مع المهام التي تريد إنهائها.
4. في **الوظائف الدفعية**، حدد المهام المطلوب إنهاؤها.
5. انقر فوق **تغيير الحالة**، واختر **إلغاء التحديد** ثم انقر فوق **موافق**.
6. في علامة التبويب السريعة **مهام الدُفعة** ، انقر فوق **إيقاف**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]