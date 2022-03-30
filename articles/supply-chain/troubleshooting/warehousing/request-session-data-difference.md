---
title: فرق غير متوقع بين بيانات الطلب وبيانات جلسة العمل أثناء الاختبار
description: حدث فرق غير متوقع بين بيانات الطلب وبيانات جلسة العمل في نتائج التحقق من صحة مهمة تطبيق المستودع.
author: mamuszal
ms.date: 03/11/2022
ms.topic: troubleshooting
ms.search.form: WHSValidatorRunInstance_executeRun
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mamuszal
ms.search.validFrom: 2022-03-11
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: da8f0506a76b0d0cc02bfc2e1bff01b4ddccb578
ms.sourcegitcommit: 941119133be1765f653d5d5270dfdf58466e1d07
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/17/2022
ms.locfileid: "8456929"
---
# <a name="unexpected-difference-between-request-and-session-data-during-testing"></a>فرق غير متوقع بين بيانات الطلب وبيانات جلسة العمل أثناء الاختبار

رمز الخطأ: WarehouseMobileDeviceRequestInputValidationError

## <a name="symptoms"></a>العلامات

عند استخدام [اطار عمل التحقق من صحة مهمة تطبيق المستودع](/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/warehouse-app-task-validation-rsat)، تقوم أداه التحقق من الصحة بإرجاع رسالة الخطأ التالية:

> فرق غير متوقع بين بيانات الطلب وبيانات جلسة العمل. تم انتهاك بروتوكول XML للأجهزة المحمولة في المستودع. REQUEST_XML_TAMPERING

## <a name="cause"></a>السبب

يحدث الخطأ عندما لا يتطابق إخراج الخطوة الأخيرة التي تم تشغيلها بنجاح في التشغيل التجريبي مع الإدخال المسجل للخطوة التالية. قد تنشأ هذه الحالة لأن أداة التحقق من صحة المهمة لا تستخدم إخراج خطوة سابقة كمدخل لخطوة متتالية. وهي تستخدم، بدلاً من ذلك، XML المسجل كإدخال لكل خطوة.

في معظم الحالات، يحدث الخطأ عند إعادة تشغيل مهمة، ولكن الاختبار يتطلب بعض السجلات التي تم تعديلها أو إزالتها بواسطة تشغيل سابق لنفس المهمة.

## <a name="resolution"></a>القرار

لا يعد تشغيل اختبار التحقق من صحة مهمة تطبيق المستودع عملية جارية ولكنه يعدل البيانات الأساسية. وبالتالي، قبل إعادة تشغيل مهمة قد يلزم إعادة تعيين البيانات ذات الصلة.

1. راجع إخراج XML الخاص بخطوة الاختبار الناجحة الأخيرة لتحديد مكان توقف تشغيل الاختبار.
1. افحص اختبارك وتأكد من أن جميع أوامر المبيعات وأوامر التحويل ورؤوس العمل والسجلات الأخرى المطلوبة لا تزال موجودة وفي الحالة المتوقعة.
1. أعد إنشاء السجلات المفقودة أو المعدّلة أو قم بتحريرها. بدلاً من ذلك، قم بإنشاء إعداد اختبار جديد، وصمم الاختبار لاستخدام سجلات موجودة صالحة.
