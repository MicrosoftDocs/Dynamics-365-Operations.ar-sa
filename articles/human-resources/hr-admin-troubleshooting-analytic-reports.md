---
title: استكشاف أخطاء التقارير التحليلية وإصلاحها
description: يشرح هذا الموضوع كيفية استكشاف المشكلات وإصلاحها وتشخيصها إذا لم تظهر تغييرات بيانات العميل في أي من مساحات عمل العميل.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7e81bae4d9cb0bb0b77bb57bac16cc67bbbcf9ea
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/04/2022
ms.locfileid: "8694049"
---
# <a name="troubleshoot-analytic-reports"></a>استكشاف أخطاء التقارير التحليلية وإصلاحها


[!INCLUDE [PEAP](../includes/peap-2.md)]

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
