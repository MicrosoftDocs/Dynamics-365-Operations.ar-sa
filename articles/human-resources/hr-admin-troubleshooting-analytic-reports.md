---
title: استكشاف أخطاء التقارير التحليلية وإصلاحها
description: يوضح هذا المقال ما يجب عليك القيام به إذا لم تظهر التغييرات في بيانات العميل في أيًا من مساحات العمل الخاصة بالعميل.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 99d9eb3a16e6470820a2eb0a19c1d50e89bd3d36
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2020
ms.locfileid: "3007907"
---
# <a name="troubleshoot-analytic-reports"></a>استكشاف أخطاء التقارير التحليلية وإصلاحها

**إصدار**

لا تظهر التغييرات في بيانات العميل على علامات تبويب **التحليلات** الخاصة بأيًا من مساحات عمل العميل.

**السبب**

بشكل افتراضي، يتم تحديث تقارير Microsoft Power BI كل أربع ساعات، وفقًا لجدول الوظيفة الدفعية لقياس النشر.

**‏‏الدقة**

وقد تكون هذه المشكلة مُجرد مسألة توقيت فقط. اتبع هذه الخطوات لبدء الوظيفة الدفعية وتحديث مساحات عمل التحليلات.

1. افتح صفحة **الوظائف الدفعية** في **إدارة النظام \>الارتباطات \>الوظائف الدفعية \>الوظائف الدفعية**. بدلاً من ذلك، استخدم بحث، ثم أدخل **الوظائف الدفعية**.
1. ابحث عن وظيفة**توزيع القياس** في القائمة.
1. حدد **تحرير** في أعلى الصفحة، ثم قم بتعيين وقت/تاريخ البدء المجدول للقيمة التي سوف تقوم بتحديث التحليلات لوقت أقرب إلى الوقت الحالي.

![الوظائف الدفعية](media/batch-jobs.png)
