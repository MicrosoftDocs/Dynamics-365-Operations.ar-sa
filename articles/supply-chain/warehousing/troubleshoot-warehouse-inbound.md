---
title: استكشاف أخطاء ‏‫عمليات المستودعات الواردة‬ وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء العمل مع عمليات تشغيل المستودعات الواردة في Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 71f590ec01b757de298bd2692fdbdb0324843376
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970226"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a>استكشاف أخطاء ‏‫عمليات المستودعات الواردة‬ وإصلاحها

[!include [banner](../includes/banner.md)]

يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء العمل مع عمليات تشغيل المستودعات الواردة في Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a>أتلقى رسالة الخطا التالية: "تم إنشاء أمر الجودة %1. تعذر العثور على ملف تعريف نظام المجموعة، فيُرجى التحقق من التكوين."

### <a name="issue-description"></a>وصف المشكلة

ترتبط رسالة الخطا هذه بعمليه استلام يتم فيها تشغيل أداره الجودة (QMS). استنادا إلى التكوينات الموجودة في البيئة الخاصة بك ، قد تساعدك التفاصيل الاضافيه حول العملية التي تقوم بإنشاء رسالة الخطا علي إصلاح المشكلة.

### <a name="issue-resolution"></a>حل المشكلة

أولا ، قم بمراجعه [اعداد انتقاء الكتلة](set-up-cluster-picking.md)، وتاكد من اعداد ملفات تعريف المجموعة بشكل صحيح. لا يمكنك استخدام عنصر قائمه جهاز المحمول لانتقاء نظام المجموعة ما لم يتم اعداد ملفات تعريف نظام المجموعة. اعتمادا علي البيئة الخاصة بك ، قد يتوجب عليك أيضا مراجعه التكوينات الأخرى ذات الصلة.

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a>لا يعمل استلام لوحه الترخيص المختلط لأي كود ترتيب باستثناء الاعتماد.

### <a name="issue-description"></a>وصف المشكلة

عند تعيين حقل **الاجراء** الخاص بكود الترتيب إلى *دائن* أو *خردة*، يمكنك استخدام العنصر الموجود في قائمه [استلام لوح الترخيص المختلط ](mixed-license-plate-receiving.md) لمعالجه الأصناف المرتجعة فقط.

### <a name="issue-resolution"></a>حل المشكلة

قامت Microsoft بتقييم هذه المشكلة وقامت بتحديد انها قيد ميزه. حاليا، [يتم دعم أكواد الترتيب](../service-management/set-up-disposition-codes.md) فقط حيث تم تعيين حقل **الاجراء** إلى *دائن* أو *الخردة* لاستلام لوحه الترخيص المختلط.

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a>عند تشغيل المهمة الدورية لتحديث إيصالات استلام المنتجات ، يتم تاكيد أوامر الشراء غير المؤكدة.

### <a name="issue-description"></a>وصف المشكلة

بعد تشغيل المهمة الدورية *تحديث إيصالات استلام المنتجات*، يقوم النظام تلقائيا بتاكيد أوامر الشراء غير المؤكدة التي لها حاله حركه المخزون *المسجلة*.

### <a name="issue-resolution"></a>حل المشكلة

تعمل ميزه معالجه التحميل الواردة الجديدة، *عبر استلام كميات التحميل*، علي إصلاح هذه المشكلة. لتشغيل هذه الميزة، انتقل إلى [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) لتشغيل الميزات التالية (بهذا الترتيب):

1. إقران حركات مخزون أمر الشراء بحمل العمل
1. استلام زائد لكميات حمل العمل

لمزيد من المعلومات ، راجع [ترحيل كميات المنتج المسجلة مقابل أوامر الشراء](inbound-load-handling.md#post-registered-quantities).
