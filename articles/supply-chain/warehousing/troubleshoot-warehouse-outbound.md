---
title: استكشاف أخطاء ‏‫عمليات المستودعات الصادرة‬‬ وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء العمل مع عمليات تشغيل المستودعات الصادرة في Microsoft Dynamics 365 Supply Chain Management.
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
ms.openlocfilehash: 165ac8145ad75c2c6619764b9abe855b9d32eb46
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993968"
---
# <a name="troubleshoot-outbound-warehouse-operations"></a>استكشاف أخطاء ‏‫عمليات المستودعات الصادرة‬‬ وإصلاحها

[!include [banner](../includes/banner.md)]

يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء العمل مع عمليات تشغيل المستودعات الصادرة في Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-sales-order-could-not-be-released"></a>أتلقى رسالة الخطا التالية: "تعذر إصدار أمر المبيعات".

### <a name="issue-description"></a>وصف المشكلة

قد تحدث هذه المشكلة لأسباب عديده. علي سبيل المثال ، يكون الأمر في انتظار أداره الائتمان ، ولا يمكن إنشاء إيه شحنات حتى يتم إدخال عنوان بريدي صالح لكافة بنود المبيعات المرتبطة بامر المبيعات. وبدلا من ذلك ، هناك قائمه احتجاز يجب معالجتها قبل التمكن من إصدار الأمر إلى المستودع. وقد تكون قائمه الاحتجاز هذه خاصه بالطلب ، أو قد تكون موجودة في حساب العميل.

### <a name="issue-resolution"></a>حل المشكلة

قم باضافه العنوان أو تحديثه علي بنود أمر المبيعات والأمر ، ثم قم بتحرير الأمر إلى المستودع. يمكن إصدار الأوامر إلى المستودع فقط إذا كان لديها عنوان تسليم صالح (لكل اعداد تنسيق العنوان في الوحدة النمطية **أداره المؤسسة**).

التحقق من احتجاز الأمر ومعالجه المشكلات. ثم قم بازاله التعليق من الأمر أو العميل ، ثم قم بإصدار الأمر إلى المستودع.

## <a name="i-receive-the-following-message-the-shipment-for-load-1-has-been-confirmed-however-no-lines-are-posted"></a>أتلقى الرسالة التالية: "تم تاكيد الشحنة الخاصة بالتحميل 1%." ومع ذلك ، لا يتم ترحيل إيه بنود.

### <a name="issue-description"></a>وصف المشكلة

تم تاكيد الشحن علي الحمل ، لكن لم يتم اجراء ترحيل آخر.

### <a name="issue-resolution"></a>حل المشكلة

لا يؤثر تاكيد الشحن علي الترحيل. وهي تقوم فقط بتحديث الشحنة وحاله التحميل. يجب ان تحدث عمليه الترحيل في عمليه منفصلة.

## <a name="i-receive-the-following-error-message-direct-delivery-is-not-able-to-process-for-warehouse-1-as-it-has-warehouse-management-enabled-please-specify-another-warehouse-that-is-not-enabled-for-warehouse-management"></a>أتلقى رسالة الخطا التالية: "التسليم المباشر غير قادر علي معالجه المستودع 1% نظرا لأنه يحتوي علي أداره مستودع ممكنة. الرجاء تحديد مستودع آخر غير ممكن لأداره المستودعات. "

### <a name="issue-description"></a>وصف المشكلة

تتم أضافه صنف إلى بند مبيعات للتسليم المباشر من مستودع يتم تمكينه لأداره المستودعات (WMS). تظهر رسالة الخطا هذه عند تحديث بند المبيعات. 

### <a name="issue-resolution"></a>حل المشكلة

قامت Microsoft بتقييم هذه المشكلة وقامت بتحديد انها قيد ميزه. حاليا ، لا يدعم WMS التسليم المباشر. التالي ، لاستخدام التسليم المباشر ، يجب تحديد صنف ومستودع غير WMS.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]