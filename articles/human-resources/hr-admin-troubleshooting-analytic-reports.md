---
title: استكشاف أخطاء التقارير التحليلية وإصلاحها
description: يوضح هذا المقال ما يجب عليك القيام به إذا لم تظهر التغييرات في بيانات العميل في أيًا من مساحات العمل الخاصة بالعميل.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d4e76f3b6231b6f307173fa176360daf775c8a7950bc4ab2f2162c768102c369
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6717404"
---
# <a name="troubleshoot-analytic-reports"></a>استكشاف أخطاء التقارير التحليلية وإصلاحها

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**إصدار**

لا تظهر التغييرات في بيانات العميل على علامات تبويب **التحليلات** الخاصة بأيًا من مساحات عمل العميل.

**السبب**

بشكل افتراضي، يتم تحديث تقارير Microsoft Power BI كل أربع ساعات، وفقًا لجدول الوظيفة الدفعية لقياس النشر.

**‏‏الدقة**

وقد تكون هذه المشكلة مُجرد مسألة توقيت فقط. اتبع هذه الخطوات لبدء الوظيفة الدفعية وتحديث مساحات عمل التحليلات.

1. افتح صفحة **الوظائف الدفعية** في **إدارة النظام \>الارتباطات \>الوظائف الدفعية \>الوظائف الدفعية**. بدلاً من ذلك، استخدم بحث، ثم أدخل **الوظائف الدفعية**.
1. ابحث عن وظيفة **توزيع القياس** في القائمة.
1. حدد **تحرير** في أعلى الصفحة، ثم قم بتعيين وقت/تاريخ البدء المجدول للقيمة التي سوف تقوم بتحديث التحليلات لوقت أقرب إلى الوقت الحالي.

![الوظائف الدفعية.](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]