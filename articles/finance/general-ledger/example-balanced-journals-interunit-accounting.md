---
title: دفاتر اليومية التي تمت موازنتها للمحاسبة بين الوحدات
description: توضح هذه المقالة كيفية موازنة دفتر اليومية بشكل تلقائي عند تحديد بعد مالي للموازنة في صفحة دفتر الأستاذ.
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f189d1ed5b0917c9975587accc2275556ceb8143
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968744"
---
# <a name="balanced-journals-for-interunit-accounting"></a>دفاتر اليومية التي تمت موازنتها للمحاسبة بين الوحدات

[!include [banner](../includes/banner.md)]

توضح هذه المقالة كيفية موازنة دفتر اليومية بشكل تلقائي عند تحديد بعد مالي للموازنة في صفحة دفتر الأستاذ. 

وإذا لم تتم موازنة الإدخالات المحاسبية على مستوى قيم البُعد المالي، يتم إنشاء إدخالات محاسبية إضافية تلقائيًا لموازنة دفتر اليومية. وتستخدم إدخالات الحساب هذه نوعي الترحيل **بين الوحدات - المدين** و **بين الوحدات - الدائن** في صفحة **حسابات للحركات التلقائية** لتحديد الحساب الرئيسي. على سبيل المثال، تم تحديد وحدة الأعمال، التي هي الجزء الثاني من حساب دفتر الأستاذ، بوصفها البعد المالي للموازنة، والقيود المحاسبية التالية على وشك أن يتم إنشاؤها.

|                      |           |
|----------------------|-----------|
| 6100 – MSP – OU\_256 | 100.00 DR |
| 6100 – NY – OU\_249  | 100.00 DR |
| 2100 – MSP – OU\_256 | 200.00 CR |

وفي هذه الحالة، تم تحديد الأرصدة التالية:

-   لوحدة الأعمال MSP‏ = 100.00 CR
-   لوحدة الأعمال NY‏ = 100.00 DR

ولذلك، يتم إنشاء الإدخالات المحاسبية التالية تلقائيًا لموازنة هذا الإدخال على مستوى قيم البُعد المالي.

|                                   |           |
|-----------------------------------|-----------|
| (المدين بين الوحدات) – MSP‏ – OU\_256 | 100.00 DR |
| (الدائن بين الوحدات) – NY‏ – OU\_249 | 100.00 CR |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]