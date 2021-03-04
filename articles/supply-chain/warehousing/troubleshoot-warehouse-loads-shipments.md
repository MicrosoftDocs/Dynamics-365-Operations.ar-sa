---
title: استكشاف أخطاء تحميل الإنشاء والشحنات وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء العمل مع إنشاء حمل العمل والشحنات في Microsoft Dynamics 365 Supply Chain Management.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2933bcfd2cc526e39a4e1343cd472334a5b95607
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645322"
---
# <a name="troubleshoot-load-building-and-shipments"></a>استكشاف أخطاء تحميل الإنشاء والشحنات وإصلاحها

[!include [banner](../includes/banner.md)]

يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء العمل مع إنشاء حمل العمل والشحنات في Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-you-cant-create-a-load-line-for-this-order-line-because-it-contains-inventory-dimensions-that-are-invalid"></a>أتلقى رسالة الخطا التالية: "لا يمكنك إنشاء بند تحميل لسطر الأمر هذا لأنه يحتوي علي ابعاد مخزون غير صالحه..."

### <a name="issue-description"></a>وصف المشكلة

وتظهر رسالة الخطا التالية عند محاولة إصدار أمر توريد الإرجاع إلى المستودع:

> لا يمكنك إنشاء بند تحميل لسطر الأمر هذا لأنه يحتوي علي ابعاد مخزون غير صالحه. لا يمكنك الاشاره إلى ابعاد المخزون الموجودة أسفل بعد الموقع في التدرج الهرمي للحجز. تتيح أزاله الابعاد غير الصالحة من سطر الأمر.

### <a name="issue-resolution"></a>حل المشكلة

لسوء الأسف ، لا يدعم المنتج معالجه التحميل لعمليه إرجاع المبيعات. التالي ، لا يمكن تحرير أمر الشراء المرتجع إلى المستودع.

في حركات أمر المبيعات، يمكنك الاشاره إلى ابعاد المخزون الموجودة أسفل بعد **الموقع** في التدرج الهرمي للحجز. الحل هو أزاله الابعاد غير الصالحة من سطر الأمر.

## <a name="i-receive-the-following-error-message-one-of-the-lines-is-already-on-a-load-unable-to-release-to-warehouse"></a>أتلقى رسالة الخطا التالية: "أحد البنود قيد التحميل بالفعل. تعذر الإصدار إلى المستودع."

### <a name="issue-description"></a>وصف المشكلة

إذا قمت بإنشاء التحميل يدويا ، أو إذا قمت باعداد العملية بحيث يتم إنشاء التحميلات بالفعل قبل حدوث إدخال سطر أمر المبيعات ، فان الافتراض هو ان يتم اجراء الإصدار اللاحق يدويا ، سيتم استخدام المسار والتقدير من الحمل.

في السيناريو المحتمل الآخر ، تحاول القيام بإصدار تلقائي للمستودع ، ولكن فشل عمليه الموجه في إنشاء العمل. لذلك ، لا يزال يتم إنشاء شحنه مفتوحة أو عمليه تحميل. يقوم الشحن أو التحميل المفتوح بعد ذلك بحظر المحاولات اللاحقة لإصدار الأمر تلقائيا حتى تقوم بحذف الشحنة أو التحميل المفتوح ، أو إعادة معالجة الموجه يدويا.

### <a name="issue-resolution"></a>حل المشكلة

يمكنك الإصدار من الصفحة أمر المبيعات ، أو يمكن اجراء الإصدار التلقائي من الصفحة أمر المبيعات الخاص بالإصدار ، وذلك فقط في حاله عدم وجود تحميل قبل الإصدار الخاص بالمستودع. سيتم تلقائيا إنشاء التحميل بعد معالجه الموجه.

## <a name="i-receive-the-following-error-message-the-delivery-note-correction-cant-be-processed-the-delivery-note-only-contains-items-that-are-subject-to-warehouse-management-processes-as-these-are-not-supported-by-delivery-note-correction"></a>أتلقى رسالة الخطا التالية: "لا يمكن معالجه تصحيح مذكره التسليم. لا تحتوي اشعار التسليم الا علي الأصناف التي تخضع لعمليات أداره المستودع ، لان هذه الأصناف غير معتمده من قبل تصحيح مذكره التسليم."

### <a name="issue-description"></a>وصف المشكلة

بعد ترحيل مذكره تسليم ، لا يمكنك إلغاؤها ، لأنه لم يتم توفير الزر **إلغاء**. لا يمكنك أيضا تصحيح مذكرة التسليم. في حاله المحاولة ، تظهر رسالة الخطا هذه.

### <a name="issue-resolution"></a>حل المشكلة

لتصحيح إيصالات التعبئة التي تم ترحيلها للأصناف التي تم تمكينها لأداره المستودعات المتقدمة (WMS) ، يجب القيام بالترحيل من التحميل ، وليس من الأمر مباشره.

## <a name="how-can-i-create-work-from-outbound-loads-instead-of-waves"></a>كيف يمكنني إنشاء عمل من التحميلات الصادرة بدلا من الموجات؟

### <a name="issue-description"></a>وصف المشكلة

وفيما يلي أحدي الطرق لأعاده إنتاج هذه المشكلة.

1. قم بإنشاء حمل عمل خارجي باستخدام أمر مبيعات أو أمر نقل.
2. قم بإصدار حمل العمل للمستودع.
3. لاحظ انه لم يتم إنشاء عمل انتقاء بعد.

### <a name="issue-resolution"></a>حل المشكلة

إذا كان يجب إنشاء العمل فورا عند إصدار الحمل ، يجب ان تقوم بتكوين قالب الموجه وفقا لذلك. في قالب الموجه ، قم بتعيين الخيارات التالية إلى *نعم*:

- جعل إنشاء الموجة تلقائيًا
- معالجة الموجة عند الإصدار إلى المستودع
- جعل تحرير الموجة تلقائيًا

## <a name="i-cant-re-release-a-partially-shipped-load"></a>لا يمكنني أعاده إصدار تحميل تم شحنه جزئيا.

### <a name="issue-description"></a>وصف المشكلة

لا يمكنك إصدار تحميل تم شحنه جزئيا للمستودع. عند القيام بالإصدار علي المستودع ، تظهر رسالة "اكتملت العملية" ولكن لا يحدث شيء ، ولا يتم إنشاء اي عمل للكمية المتبقية. تحدث هذه المشكلة عند استخدام وظيفة تحميل النقل ووجود حجز غير مكتمل.

### <a name="issue-resolution"></a>حل المشكلة

[مشكلة قاعدة المعارف 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("يمكن أعاده إنشاء موجات لعمليات التحميل التي تم شحنها جزئيا وأعاده معالجتها") تم إصلاحها في [الإصدار 10.0.15](../get-started/whats-new-scm-10-0-15.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]