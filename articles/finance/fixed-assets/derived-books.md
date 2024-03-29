---
title: الدفاتر المشتقة
description: توفر هذه المقالة نظرة عامة على وظيفة الدفاتر المشتقة.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable
audience: Application User
ms.reviewer: kfend
ms.custom: 3401
ms.assetid: 862d6450-187b-497f-9822-cce45f2c65a9
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 81abb1b16069adb3cdcc73bdf6b963463cc88938
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/05/2022
ms.locfileid: "8714078"
---
# <a name="derived-books"></a>الدفاتر المشتقة

[!include [banner](../includes/banner.md)]

توفر هذه المقالة نظرة عامة على وظيفة الدفاتر المشتقة.

‏‫الغرض من الدفاتر المشتقة هو تبسيط ترحيل حركات دفتر الأصول الثابتة التي تم تخطيطها للفواصل الزمنية العادية.  يمكنك اختيار دفتر واحد كدفتر أساسي.‬ يكون هذا عادةً الكتاب المستخدم للإهلاك المحاسبي. وتقوم فيما بعد بإرفاقه بدفاتر أخرى التي تم إعدادها لترحيل الحركات في الفواصل الزمنية نفسها كالدفتر الأساسي. يتم غالبًا إعداد دفاتر إهلاك كدفاتر مشتقة. 

وتعتبر الحركات الأكثر شيوعًا التي يجب إعدادها لترحيل الدفاتر المشتقة عمليات الاستحواذ وتسويات الاستحواذ وعمليات التخلص. 

## <a name="example"></a>مثال

تم إعداد الدفتر "ب" والدفتر "ج" كدفاتر مشتقة للدفتر "أ" لنوع حركة الاستحواذ. في الدفتر "أ"، أدخل حركة الاستحواذ للأصل 123 بقيمة 1.500.00. 

عندما يتم ترحيل الحركة، يتم إنشاء حركة استحواذ ويتم ترحيلها في الأصل 123 للدفتر "ب" وفي الأصل 123 لنموذج للدفتر "ج" بقيمة 1.500.00. عندما تقوم بإعداد حركات الدفتر الأساسي لترحيلها في دفتر يومية الأصل الثابت، يمكنك أيضًا عرض حركات دفاتر الإهلاك المشتقة وتعديلها. وإذا قمت بإعداد حركات الدفتر الأساسي في دفتر يومية آخر، فلن تظهر حركات القيمة المشتقة. ومع ذلك، يتم ترحيلها إلى الحسابات المناسبة وطبقات الترحيل عند ترحيل حركات الدفتر الأساسي.

> [!NOTE]                                                                                                                               
> فيما يتعلق بالدفاتر التي يتم إعدادها لترحيل الحركات عند فواصل زمنية غير الفواصل الزمنية للدفتر الأساسي، يجب إرفاقها بالأصل الثابت كدفاتر منفصلة وليس كدفاتر مشتقة.  

لمزيد من المعلومات، راجع [‏‫الترحيل باستخدام الدفاتر المشتقة](post-derived-value-models.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
