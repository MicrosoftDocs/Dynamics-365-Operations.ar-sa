---
title: استكشاف الأخطاء في عمليات الحجز بإدارة المستودعات وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء العمل مع عمليات حجز المستودعات في Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 5f3a9ab907c3cb0e6b99c414a78b6878bd5353274472c54e1f5eaf1d167f046a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6773095"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a>استكشاف الأخطاء في عمليات الحجز بإدارة المستودعات وإصلاحها

[!include [banner](../includes/banner.md)]

يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء العمل مع عمليات حجز المستودعات في Microsoft Dynamics 365 Supply Chain Management.

بالنسبة إلى الموضوعات المتعلقة بتسجيلات الدُفعات والرقم التسلسلي، راجع [استكشاف أخطاء دفعة المستودع والتسلسل الهرمي للحجز التسلسلي وإصلاحها](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md).

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a>أتلقى رسالة الخطأ " لا يمكن إزالة الحجوزات نظرًا لوجود عمل مُنشأ يعتمد على الحجوزات".‬

### <a name="issue-description"></a>وصف المشكلة

لا يمكنك إلغاء حجز المخزون في بند مبيعات ، نظرا لوجود عمل مفتوح للبند.

### <a name="issue-resolution"></a>حل المشكلة

التحقق من وجود عمل مجموعه التعبئة المفتوحة لإحضار الصنف من محطه تعبئة إلى موقع آخر (مثل *باب الخليج*). قم بمراجعه السجلات الموجودة في الصفحتين **سجل محفوظات إنشاء العمل** و **وتفاصيل العمل** لتحديد ما يقوم بحجز المخزون فعليا ، ثم قم بإكمال العمل أو حذفه لتحرير الحجز.

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a>أتلقى رسالة الخطا التالية: "تعذر تحديث كميه المخزون- %1 بسبب عدم كفاية حركات المخزون للصنف %2 ...."

### <a name="issue-description"></a>وصف المشكلة

قد تحدث هذه المشكلة في حاله عدم تمكن النظام من تحديث كميه مخزون نظرا لعدم وجود حركات مخزون كافيه بالابعاد المحددة. فيما يلي نص رسالة الخطأ الكاملة.

> تعذر تحديثكميه المخزون - %1 بسبب عدم كفاية حركات المخزون الخاصة بالصنف %2 ذي حجم الابعاد = %3، اللون = %4، الإضافات = %5، الموقع = %6، المستودع = %7، الموقع = %8، حاله المخزون = متاح، لوح الترخيص = %9، رقم المجموعة = %10 لمعرف المرجع %11 في معرف الشحنة %12.

### <a name="issue-resolution"></a>حل المشكلة

تاكد من عدم قيام إيه حركات مخزون بالفعل بحجز الكمية. علي سبيل المثال ، قد تقوم هذه الحركات بفتح أوامر الجودة أو سجلات حظر المخزون أو أوامر المخرجات.

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a>أتلقى رسالة الخطا التالية: "الفعلي... لا يمكن حجزه لان 0.00 فقط متاح في المخزون. "

### <a name="issue-description"></a>وصف المشكلة

قد تحدث هذه المشكلة في حاله عدم تمكن النظام من تحديث كميه مخزون نظرا لعدم وجود حركات مخزون كافيه بالابعاد المحددة. فيما يلي نص رسالة الخطأ الكاملة.

> موقع الفعلي = %1، المستودع = %2، حاله المخزون = متاح، رقم المجموعة = %3، المالك = %4 : لا يمكن حجز %5 نظرا لتوفر 0.00 فقط في المخزون.

### <a name="issue-resolution"></a>حل المشكلة

قد يكون سبب هذه المشكلة هو فتح العمل. قم اما بإكمال العمل أو الاستلام دون إنشاء العمل. تاكد من عدم قيام إيه حركات مخزون بالفعل بحجز الكمية. علي سبيل المثال ، قد تكون هذه الحركات أوامر جودة مفتوحة أو سجلات حظر المخزون أو أوامر المخرجات.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
