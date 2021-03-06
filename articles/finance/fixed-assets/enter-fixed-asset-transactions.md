---
title: خيارات حركات الأصول الثابتة
description: يصف هذا الموضوع الطرق المختلفة لإنشاء حركات الأصول الثابتة.
author: ShylaThompson
manager: AnnBe
ms.date: 02/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: roschlom
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 494087bc7a1247999d3f63dcdc0a0f403dcfdb2d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978679"
---
# <a name="fixed-asset-transaction-options"></a>خيارات حركات الأصول الثابتة

[!include [banner](../includes/banner.md)]

يصف هذا الموضوع الطرق المختلفة لإنشاء حركات الأصول الثابتة.

يمكن إعداد الأصول الثابتة لتتكامل مع الحسابات الدائنة والحسابات المدينة والتدبير والمصادر ودفتر الأستاذ العام. يمكنك أيضًا تحويل الأصناف من إدارة المخزون إلى الأصول الثابتة إذا أردت استخدامها داخليًا.

## <a name="accounts-payable"></a>حسابات دائنة
يمكنك إدخال حركات الأصول الثابتة في صفحة إيصال دفتر اليومية. ويمكن فتح هذه الصفحة من صفحة دفتر يومية الفاتورة. كما يمكنك فتح صفحة إيصال دفتر اليومية من صفحة دفتر يومية اعتماد الفواتير. وفي حقل نوع الحساب المقابل، حدد الأصول الثابتة. وبعد ذلك، في حقل الحساب المقابل، حدد رقم أصل ثابت. في علامة التبويب "الأصول الثابتة"، أدخل القيم في حقلي "نوع الحركة" و"الدفاتر".

## <a name="accounts-receivable"></a>الحسابات المدينة
يمكنك إدخال حركات الأصول الثابتة في صفحة فاتورة النص الحر.  وفي صفحة فاتورة النص الحر في شبكة بنود الفاتورة، حدد صنف بند.‬ انقر فوق علامة التبويب السريعة تفاصيل البند. أدخل رقم الأصل الثابت والدفتر لحركة التخلص. في فاتورة النص الحر، تكون حركة الأصل الثابت دائمًا من نوع ‏‫التخلص - البيع‬.

## <a name="procurement-and-sourcing"></a>التدبير وتحديد الموارد
يمكنك إدخال حركات الأصول الثابتة في صفحة أمر الشراء. وأدخل المعلومات المطلوبة لإنشاء أمر شراء، ثم انقر فوق موافق. وفي صفحة "أمر الشراء"، انقر فوق علامة التبويب السريعة تفاصيل بند. وبعد ذلك، في علامة التبويب الأصول الثابتة، أدخل معلومات حول الأصل الثابت. 

لترحيل حركة استحواذ لأصل ثابت موجود، حدد رقم الأصل الثابت والدفتر ونوع الحركة. لا يمكن ترحيل الأصل الثابت في حالة فقدان أي من هذه المعلومات. لترحيل حركة امتلاك لأصل ثابت جديد، حدد خيار أصل ثابت جديد؟، ثم قم بتحديد مجموعة الأصل الثابت لتعيين الأصل الثابت الجديد لها. برغم هذا لا تتوفر حقول أصول ثابتة لسطر، إذا كان الصنف في مجموعة نموذج مخزون تستخدم نموذج مخزون تكلفة قياسي. بالإضافة إلى ذلك، تحدد الخيارات التي تم تحديدها في صفحة معلمات الأصول الثابتة ما إذا كان يمكنك ترحيل حركات الامتلاك من وحدات الشراء. 

عند استخدام أمر شراء أو مخزون دفتر يومية الأصول الثابتة لامتلاك الأصول الثابتة، تتأثر قيمة المخزون.

## <a name="general-ledger"></a>دفتر الأستاذ العام
يمكن ترحيل أي نوع حركة أصل ثابت في صفحة دفتر اليومية العام. يمكنك أيضا استخدام دفاتر يومية الأصول الثابتة لترحيل حركات الأصول الثابتة.

## <a name="options-for-entering-fixed-asset-transaction-types"></a>خيارات إدخال أنواع حركات الأصول الثابتة


| نوع الحركة                    | الوحدة النمطية                   | الخيارات                                   |
|-------------------------------------|--------------------------|-------------------------------------------|
| الاستحواذ، تسوية الاستحواذ‬ | الأصول الثابتة             | الأصول الثابتة، مخزون الأصول الثابتة   |
|                                     | دفتر الأستاذ العام           | دفتر اليومية العام                           |
|                                     | حسابات دائنة         | دفتر يومية الفواتير، دفتر يومية اعتماد الفواتير |
|                                     | التدبير وتحديد الموارد | أمر شراء                            |
| الإهلاك                        | الأصول الثابتة             | الأصول الثابتة                              |
|                                     | دفتر الأستاذ العام           | دفتر اليومية العام                           |
| التخلص                            | الأصول الثابتة             | الأصول الثابتة                              |
| ** **                               | دفتر الأستاذ العام           | دفتر اليومية العام                           |
| ** **                               | الحسابات المدينة      | فاتورة ذات نص حر                         |


لا يتم تحديث القيمة المتبقية للأصل الثابت خلال فترات الإهلاك عند إنشاء أو استيراد بند دفتر يومية من نوع حركة إهلاك عبر كيان بيانات بطريقة يدوية. يتم تحديث هذه القيمة عند استخدام عملية مقترح الإهلاك لإنشاء بند دفتر اليومية.

لمزيد من المعلومات، راجع [تكامل الأصول الثابتة](fixed-asset-integration.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]