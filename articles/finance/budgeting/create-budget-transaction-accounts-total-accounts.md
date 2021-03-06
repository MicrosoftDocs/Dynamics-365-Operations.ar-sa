---
title: إنشاء موازنة من حسابات الحركات والحسابات الإجمالية
description: توفر هذه المقالة نظرة عامة على عملية إنشاء موازنات بالاستناد إلى الحسابات الإجمالية. وهي تشرح أيضًا كيفية تشغيل رقابة الموازنة للحسابات الإجمالية، إذا كانت رقابة الموازنة مطلوبة.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetControlConfiguration, BudgetPlanGenerate
audience: Application User
ms.reviewer: roschlom
ms.custom: 13051
ms.assetid: fb1bb2d3-445c-402f-a9a3-aa6503eed78e
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2c2298a774e35bc92fafb8bc24871b288fb198d7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003071"
---
# <a name="create-a-budget-from-transaction-accounts-and-total-accounts"></a>إنشاء موازنة من حسابات الحركات والحسابات الإجمالية

[!include [banner](../includes/banner.md)]

توفر هذه المقالة نظرة عامة على عملية إنشاء موازنات بالاستناد إلى الحسابات الإجمالية. وهي تشرح أيضًا كيفية تشغيل رقابة الموازنة للحسابات الإجمالية، إذا كانت رقابة الموازنة مطلوبة.

تسمح كلُّ من خطة الموازنة ووثائق إدخال سجل الموازنة بإعداد الموازنة في الحسابات التي لها نوع حساب الرئيسي **إجمالي**. ويمكن ترحيل القيم الفعلية إلى حركات الحسابات الرئيسية فقط. 

وبالنسبة للعملية الدورية **إنشاء خطة الموازنة من دفتر الأستاذ العام**، في علامة التبويب **مصدر**، يمكنك تحديد نوع الحساب الرئيسي **إجمالي** كمعيار. وفي هذه الحالة، سيتم تضمين كل حساب رئيسي إجمالي في خطة الموازنة الهدف، وسيساوي المبلغ المبلغ الإجمالي لمجموعة الحسابات الرئيسية المحددة. 

ويمكنك تنشيط رقابة الموازنة للحسابات الرئيسية من النوع **إجمالي**. ويتم اعتماد هذه الوظيفة من خلال استخدام مجموعات الموازنة. بالنسبة لكل حساب رئيسي إجمالي، يجب إنشاء الموازنة التي ينبغي مراقبتها لمجموعة موازنة في صفحة **تكوين رقابة الموازنة**. ويجب أن تتضمن المعايير التي تحددها الحساب الرئيسي الإجمالي ونطاق الحسابات‬.‬ ولتسريع عملية إنشاء مجموعات الموازنة، يمكنك الاستفادة من وحدة بيانات مجموعات رقابة الموازنة. 

عند استخدام موازنة في عمليات الإبلاغ، على سبيل المثال، في قائمة مالية، فإن مجموع الموازنة للحساب الإجمالي يتكون من المبالغ التالية:

-   الموازنات التي تم إنشاؤها من كل حساب لدفتر أستاذ الحركات خلال فترة الحساب الإجمالي.
-   مبلغ الموازنة الذي تم إدخاله مباشرة على الحساب الإجمالي.

وبالتالي، يمكنك إنشاء موازنات منفصلة لمعظم حسابات الحركات المهمة في فترة الحساب الإجمالي، ثم إضافة مبلغ الموازنة المتوفر إلى الحساب الإجمالي.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]