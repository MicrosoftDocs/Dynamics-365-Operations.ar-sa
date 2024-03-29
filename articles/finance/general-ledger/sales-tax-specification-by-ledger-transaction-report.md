---
title: تقرير مواصفات ضريبة المبيعات حسب حركة دفتر الأستاذ
description: توضح هذه المقالة كيفية استخدام ‏‫تقرير مواصفات ضريبة المبيعات حسب معاملة دفتر الأستاذ‬ لعرض وطباعة المعلومات عن معاملات دفتر الأستاذ التي يتم حساب ضريبة المبيعات لها.
author: EricWang
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2019-08-19
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: c96f457a0ea24aef1769f370c3c0657ada31eebf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898080"
---
# <a name="sales-tax-specification-by-ledger-transaction-report"></a>تقرير مواصفات ضريبة المبيعات حسب حركة دفتر الأستاذ
[!include [banner](../includes/banner.md)]

توضح هذه المقالة كيفية استخدام ‏‫تقرير **مواصفات ضريبة المبيعات حسب معاملة دفتر الأستاذ** ‬لعرض وطباعة المعلومات عن معاملات دفتر الأستاذ التي يتم حساب ضريبة المبيعات لها.

## <a name="tax-accounts-vs-non-tax-accounts"></a>الحسابات الضريبية مقابل الحسابات غير الضريبية

يعرض تقرير **‏‫مواصفات ضريبة المبيعات حسب حركة دفتر الأستاذ‬** حركات الضريبة لكل من الحسابات الضريبة والحسابات غير الضريبية. يتم تصنيف هذه الحسابات بالطريقة التالية:

- **حساب ضريبي** – يعتبر الحساب حسابًا ضريبيًا عند ترحيل حركة ضريبية، وعندما يكون الحساب الرئيسي في بند دفتر اليومية **ضريبة المبيعات** حساب ضريبة، مثل حساب ضريبة مبيعات مستحقة الدفع أو حساب ضريبة مبيعات مستحقه القبض.
- **حساب غير ضريبي** – يعتبر الحساب حسابًا غير ضريبي عند ترحيل حركة ضريبية، وعندما يكون الحساب الرئيسي في الحركة الأساسية هو حساب غير ضريبي، مثل حساب إيرادات أو حساب مصروفات.

بالنسبة للحسابات الضريبية تعرض الأعمدة **الأصل** و **‏‫ضريبة المبيعات مستحقة القبض‬** و **‏‫ضريبة المبيعات مستحقة الدفع** في التقرير **0** (صفر). بالنسبة للحسابات غير الضريبية، تعرض هذه الأعمدة المبالغ.

## <a name="filtering-the-data-on-the-report"></a>تصفية البيانات المعروضة في التقرير

عند إنشاء التقرير، تظهر الحقول الافتراضية التالية. يمكنك استخدام هذه الحقول لتصفية البيانات التي ستظهر في التقرير.

| الحقل                      | ‏‏الوصف |
|----------------------------|-------------|
| التاريخ                       | استخدم الحقول الموجودة في القسمين **من** و **إلى** لتحديد نطاق تاريخ لحركات الضرائب. |
| الحساب الرئيسي               | استخدم الحقول الموجودة في القسمين **من** و **إلى** لتحديد نطاق الحساب الرئيسية. |
| كود ضريبة المبيعات             | استخدم الحقول الموجودة في القسمين **من** و **إلى** لتحديد نطاق أكواد ضرائب المبيعات. |
| التجميع                   | حدد ما إذا كان يجب تجميع التقرير حسب حساب دفتر الأستاذ أو كود ضريبة المبيعات. |
| الإجمالي الفرعي حسب كود ضريبة المبيعات | قم بتعيين هذا الخيار إلى **نعم** لإظهار الإجماليات الفرعية بواسطة كود ضريبة المبيعات. |
| الإجماليات فقط                | قم بتعيين هذا الخيار إلى **نعم** لإظهار الإجماليات فقط. |
| الحسابات الرئيسية فقط         | قم بتعيين هذا الخيار إلى **نعم** لتضمين الحسابات الرئيسية فقط في التقرير. |

## <a name="showing-only-non-tax-accounts-on-the-report"></a>إظهار الحسابات غير الضريبية فقط في التقرير

لإظهار الحسابات غير الضريبية فقط في التقرير، قم باعداد شرط عامل تصفية، مثل العلامة النجمية (\*)، كما هو مبين في الشكل التوضيحي التالي.

![تقرير يوضح الحسابات غير الضريبية.](media/taxspecperledgertrans.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
