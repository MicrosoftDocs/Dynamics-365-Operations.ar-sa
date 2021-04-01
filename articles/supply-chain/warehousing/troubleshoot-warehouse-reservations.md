---
title: استكشاف الأخطاء في عمليات الحجز بإدارة المستودعات وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء العمل مع عمليات حجز المستودعات في Microsoft Dynamics 365 Supply Chain Management.
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
ms.openlocfilehash: a9a5d20732a802fc58c392853af8334bbc07de73
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248705"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a>استكشاف الأخطاء في عمليات الحجز بإدارة المستودعات وإصلاحها

[!include [banner](../includes/banner.md)]

يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء العمل مع عمليات حجز المستودعات في Microsoft Dynamics 365 Supply Chain Management.

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

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a>أتلقى رسالة الخطا التالية: "لتعيينها إلى موجه ، يجب ان تحدد سطور التحميل الابعاد فوق الموقع. لتعيين هذه الابعاد ، قم بحجز بند التحميل وأعاده إنشائه. "

### <a name="issue-description"></a>وصف المشكلة

عند استخدام صنف يحتوي علي "مجموعه أعلى" تدرج هرمي للحجز (مع وضع البعد **رقم المجموعة** *فوق* بعد **الموقع**)، لا يعمل الأمر **إصدار إلى مستودع** في الصفحة **منضدة تخطيط التحميل** الخاصة بالكمية الجزئية. تظهر رسالة الخطا هذه ، ولا يتم إنشاء اي عمل للكمية الجزئية.

عند استخدام صنف يحتوي علي "مجموعه أعلى" تدرج هرمي للحجز (مع وضع البعد **رقم المجموعة** *أسفل* بعد **الموقع**)، لا يعمل الأمر إصدار إلى مستودع في الصفحة **منضدة تخطيط التحميل** الخاصة بالكمية الجزئية.

### <a name="issue-resolution"></a>حل المشكلة

يتم هذا السلوك بسبب التصميم. إذا قمت بوضع بعد فوق بعد **الموقع** في التدرج الهرمي للحجز ، فيجب تحديده قبل إصدار المستودع. قامت Microsoft بتقييم هذه المشكلة وقامت بتحديد انها قيد ميزه اثناء الإصدارات إلى المستودع من منضدة تخطيط التحميل. لا يمكن إصدار الكميات الجزئية في حاله عدم تحديد واحده أو أكثر من الابعاد الموجودة اعلي **الموقع**.

لمزيد من المعلومات، راجع [سياسة مرنة لحجز البعد على مستوى المستودع](flexible-warehouse-level-dimension-reservation.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]