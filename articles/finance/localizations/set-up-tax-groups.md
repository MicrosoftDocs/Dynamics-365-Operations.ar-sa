---
title: إعداد مجموعات الضرائب
description: توضح هذه المقالة كيفية إعداد مجموعات الضرائب في خدمة حساب الضرائب.
author: wangchen
ms.date: 11/30/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 89c5670ee7e78f2dc51f128c3ae8d284bb6b925b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862888"
---
# <a name="set-up-tax-groups"></a>إعداد مجموعات الضرائب

[!include [banner](../includes/banner.md)]

توضح هذه المقالة كيفية إعداد مجموعات الضرائب في خدمة حساب الضرائب. كما يوضح كيفية إعداد مصفوفة قاعدة لإمكانية تطبيق مجموعة الضريبة وتكوين البنود في المصفوفة.

يمثل مفهوم مجموعات الضرائب في خدمة حساب الضرائب مفهوم مجموعات ضرائب المبيعات في ‎365 Finance Microsoft Dynamics. وهي عبارة عن مجموعات من أكواد الضريبة. تستخدم خدمة حساب الضريبة تقاطع مجموعة ضريبة ومجموعة ضريبة الصنف لتحديد أكواد الضريبة.

ومع ذلك، تختلف مجموعات الضرائب في خدمة حساب الضريبة عن مجموعات ضريبة المبيعات في Finance في حالة عدم وجود أية معلمات إضافية عليها، مثل **ضريبة الانتفاع** و **ضريبة الإعفاء**. وبدلاً من ذلك، تتوفر هذه المعلمات على مستوى كود الضريبة.

> [!IMPORTANT]
> يُعد إعداد مجموعات الضرائب في خدمة حساب الضرائب هو الكيان القانوني – غير المحدد. يمكنك إكمال هذا الإعداد في Regulatory Configuration Service (RCS) مرة واحدة فقط. عندما تقوم بتمكين خدمة حساب الضرائب في Finance، فإنه تتم مزامنة مجموعات الضرائب تلقائيًا للكيان القانوني المحدد.

## <a name="set-up-a-tax-group"></a>إعداد مجموعة الضريبة

اتبع هذه الخطوات لإعداد مجموعة الضريبة.

1. سجل الدخول إلى [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).
2. انتقل إلى **مساحات عمل** \> **ميزات العولمة** \> **حساب الضريبة**.
3. حدد الميزة والإصدار الذي ترغب في إعداده، ثم حدد **تحرير**.
4. في علامة التبويب **عام**، حدد **إصدار التكوين**.
5. من علامة التبويب **مجموعة الضريبة**، حدد **إدارة الأعمدة**. إذا كنت تقوم بإعداد مجموعة ضريبة للمرة الأولى، فإنه يتم تعيين الحقول في مربع الحوار **إدارة الأعمدة** تلقائيًا.
6. في القائمة الموجودة على اليسار، قم بتوسيع العقدة **البنود**، ثم حدد خانة الاختيار **مجموعة الضريبة**.

    ![مجموعه الضريبة المحددة ضمن عقدة البنود في مربع الحوار "إدارة الأعمدة".](media/select-tax-group.png)

7. حدد زر السهم الأيمن لإضافة **مجموعة الضريبة** إلى قائمة **الأعمدة المحددة** على اليمين.

    ![مجموعة الضريبة المضافة إلى القائمة "الأعمدة المحددة".](media/add-tax-group.png)

8. حدد **موافق**.

## <a name="configure-a-tax-group"></a>تكوين مجموعة الضريبة

بعد إعداد مجموعة ضريبة، يتم إنشاء مصفوفة قاعدة لإمكانية تطبيق مجموعة الضريبة. يمكنك إضافة بنود إلى المصفوفة لتكوين مجموعة الضريبة.

1. على علامة التبويب **مجموعة الضريبة**، حدد **إضافة**.
2. في الحقل **مجموعة الضريبة**، أدخل اسم مجموعة الضريبة.

    > [!IMPORTANT]
    > نُوصي باقتصار اسم مجموعة الضريبة على 10 أحرف. تتم مزامنة هذا الاسم مع Finance، وبه حد أدنى 10 أحرف لأسماء مجموعات ضريبة المبيعات.

3. في الحقل **أكواد الضريبة**، حدد خانة الاختيار لكل كود ضريبة ترغب في تضمينه في مجموعة الضريبة. يمكنك تضمين أكواد ضريبة متعددة في مجموعة ضريبة واحدة.

    ![تم تحديد أكواد ضريبة متعددة في حقل أكواد الضريبة.](media/multiple-tax-codes-selection.png)

4. كرر الخطوات من 1 إلى 3 لإضافة مزيد من مجموعات الضرائب.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
