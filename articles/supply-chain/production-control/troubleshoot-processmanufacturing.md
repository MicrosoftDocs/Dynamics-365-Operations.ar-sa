---
title: استكشاف أخطاء التصنيع التحويلي‬ وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع التصنيع التحويلي.
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 13eb50ef634de211a864a3f27defe2276cb66f411480e2074693c8b8972a284b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726695"
---
# <a name="troubleshoot-process-manufacturing"></a>استكشاف أخطاء التصنيع التحويلي‬ وإصلاحها

يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع التصنيع التحويلي.

## <a name="when-i-use-the-job-card-device-to-report-a-partial-quantity-on-the-last-job-in-a-production-order-all-the-previous-jobs-on-that-order-that-have-a-status-of-in-progress-are-automatically-ended"></a>عند استخدام جهاز بطاقة الوظيفة للإبلاغ عن الكمية الجزئية في الوظيفة الاخيره في أمر إنتاج ، يتم تلقائيا إنهاء كافة الوظائف السابقة في ذلك الأمر بالحالة قيد التقدم.

يتم هذا السلوك بسبب التصميم. في الصفحة **الإعدادات الافتراضية لأوامر الإنتاج**، في علامة التبويب **الإبلاغ كمنته**، يوجد خيار يسمي **المسار بعلامة النهاية**. في حاله تعيين هذا الموضوع علي *نعم*، يتم ترحيل دفتر يوميه بطاقة المسار عند استخدام العامل لجهاز بطاقة الوظيفة أو الوحدة الطرفية لبطاقة الوظيفة للإبلاغ عن العملية الاخيره. يقوم دفتر اليومية هذا بتمييز كافة العمليات كمكتملة وإنهاء كافة وظائف الإنتاج. عند تعيين خيار **وضع علامة نهاية علي المسار** إلى القيمة *نعم*، لا يقوم النظام بمراعاه حاله المهمة التي قام العامل بتحديدها عند الإبلاغ عن آخر عمليه. لا يقوم النظام أيضا بمراعاه ما إذا كان العامل يقوم بالإبلاغ عن الكمية الكاملة أو الجزئية.

## <a name="when-i-attempt-a-stock-closing-i-receive-the-following-warning-message-no-execution-of-backflush-costing-calculation-with-a-date-1-matching-period-end-has-been-registered"></a>عند محاولة اجراء إغلاق سهم ، أتلقى رسالة التحذير التالية: "عدم تنفيذ حساب تحديد تكاليف التنفيذ الحديث بالتاريخ %1 الذي تم فيه تسجيل نهاية الفترة."

في الإصدارات قبل إصدار 10.0.13 ، إذا كنت لا تستخدم تدفق تكلفه الإنتاج lean ، ستتلقى رسالة التحذير التالية اثناء اقفال المخزون:

> أنت علي وشك تنفيذ إغلاق المخزون بتاريخ %1. لا يوجد تنفيذ لحساب تكاليف الإصدار التلقائي %1 الذي تم تسجيل نهاية الفترة المطابقة. لا تنس تنفيذ حساب تكاليف الإصدار التلقائي بتاريخ %1 التي تطابق نهاية الفترة. قد لا تكون تقييم المخزونات وتكلفه البضائع المبيعة والنسب التي تم بيعها بالأستاذ الفرعي أو دفتر الأستاذ العام حتى يتم تنفيذ ذلك.

تم إصلاح هذه المشكلة في 10.0.13 الطرح والإصدارات الأحدث. للحصول على مزيد من المعلومات، راجع [قاعدة المعارف 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]