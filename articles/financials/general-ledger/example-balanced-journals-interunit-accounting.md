---
title: "دفاتر اليومية التي تمت موازنتها للمحاسبة بين الوحدات"
description: "توضح هذه المقالة كيفية موازنة دفتر اليومية بشكل تلقائي عند تحديد بعد مالي للموازنة في صفحة دفتر الأستاذ."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f45d180dc8dcafb0579e76b890dd5d516df5b8c0
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="balanced-journals-for-interunit-accounting"></a>دفاتر اليومية التي تمت موازنتها للمحاسبة بين الوحدات

[!include[banner](../includes/banner.md)]


توضح هذه المقالة كيفية موازنة دفتر اليومية بشكل تلقائي عند تحديد بعد مالي للموازنة في صفحة دفتر الأستاذ. 

وإذا لم تتم موازنة الإدخالات المحاسبية على مستوى قيم البُعد المالي، يتم إنشاء إدخالات محاسبية إضافية تلقائيًا لموازنة دفتر اليومية. وتستخدم إدخالات الحساب هذه نوعي الترحيل **بين الوحدات - المدين** و**بين الوحدات - الدائن** في صفحة **حسابات للحركات التلقائية** لتحديد الحساب الرئيسي. على سبيل المثال، تم تحديد الفرع، الذي هو الجزء الثاني من حساب دفتر الأستاذ، بوصفه البعد المالي للموازنة، والقيود المحاسبية التالية على وشك أن يتم إنشاؤها.

|                      |           |
|----------------------|-----------|
| 6100 – MSP – OU\_256 | 100.00 DR |
| 6100 – NY – OU\_249  | 100.00 DR |
| 2100 – MSP – OU\_256 | 200.00 CR |

وفي هذه الحالة، تم تحديد الأرصدة التالية:

-   بالنسبة لفرع الرياض = 100.00 ريال سعودي
-   بالنسبة لفرع نيويورك = 100.00 دولار

ولذلك، يتم إنشاء الإدخالات المحاسبية التالية تلقائيًا لموازنة هذا الإدخال على مستوى قيم البُعد المالي.

|                                   |           |
|-----------------------------------|-----------|
| (المدين بين الوحدات) – MSP – OU\_256 | 100.00 DR |
| (الدائن بين الوحدات) – NY – OU\_249 | 100.00 CR |






