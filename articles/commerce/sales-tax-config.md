---
title: تكوين ضريبة المبيعات للأوامر عبر الإنترنت
description: يوفر هذا الموضوع نظرة عامة على تحديد مجموعة ضريبة المبيعات لأنواع مختلفة من الأوامر عبر الإنترنت في Dynamics 365 Commerce.
author: gvrmohanreddy
manager: AnnBe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: gmohanv
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 40c20bf13779f73289e43df21b763e1b864686a7
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/17/2020
ms.locfileid: "4530187"
---
# <a name="configure-sales-tax-for-online-orders"></a>تكوين ضريبة المبيعات للأوامر عبر الإنترنت

[!include [banner](../includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

يقدم هذا الموضوع نظرة عامة حول تحديد مجموعة ضريبة المبيعات لأنواع مختلفة من الأوامر عبر الإنترنت. 

قد ترغب قناة التجارة الإلكترونية الخاصة بك في دعم خيارات مثل التسليم أو الالتقاط للأوامر عبر الإنترنت. يعتمد تطبيق ضريبة المبيعات على الخيار الذي حدده المستخدمون عبر الإنترنت. عندما يختار عميل الموقع شراء عنصر عبر الإنترنت وشحنه إلى عنوان، يتم تحديد ضريبة المبيعات بناءً على إعداد مجموعة ضريبة عنوان الشحن الخاص بالعميل. عندما يختار العميل استلام عنصر تم شراؤه من متجر، يتم تحديد ضريبة المبيعات بناءً على إعداد مجموعة ضرائب متجر الالتقاط. 

## <a name="orders-shipped-to-a-customer-address"></a>الأوامر التي يتم شحنها إلى عنوان العميل 

بشكل عام ، يتم تحديد ضرائب الأوامر عبر الإنترنت التي يتم شحنها إلى عناوين العملاء حسب الوجهة. تحتوي كل مجموعة ضرائب مبيعات على تكوين ضريبي قائم على وجهة البيع بالتجزئة حيث يمكن لنشاطك التجاري تحديد تفاصيل الوجهة مثل المقاطعة / المنطقة والولاية والمقاطعة والمدينة في شكل هرمي. عند إنشاء أمر عبر الإنترنت، يستخدم مُشغل الضرائب التجارية عنوان التسليم لكل صنف في الأمر، ويبحث عن مجموعات ضريبة المبيعات بمعايير ضريبية مطابقة للوجهة. على سبيل المثال، بالنسبة للأمر عبر الإنترنت وعنوان تسليم صنف إلى سان فرانسيسكو، كاليفورنيا، سوف يبحث محرك الضرائب عن مجموعة ضريبة المبيعات ورمز ضريبة المبيعات لولاية كاليفورنيا، ثم يحسب الضريبة لكل صنف وفقًا لذلك.  

## <a name="customer-based-tax-groups"></a>مجموعات الضرائب المستندة إلى العميل

في المراكز الرئيسية لـ Commerce، يوجد مكانان يتم فيهما تكوين مجموعات ضرائب العملاء:

- **ملف تعريف العميل**
- **عنوان الشحن الخاص بالعميل**

### <a name="if-a-customers-profile-has-a-tax-group-configured"></a>إذا كان ملف تعريف العميل يحتوي على مجموعة ضريبية مُكونة

قد يكون لسجل ملف تعريف العميل في المراكز الرئيسية مجموعة ضريبة مبيعات مُكونة، ولكن بالنسبة للأوامر عبر الإنترنت، لن يتم استخدام مجموعة ضريبة المبيعات المُكونة في ملف تعريف العميل بواسطة محرك الضرائب. 

### <a name="if-a-customers-shipping-address-has-a-tax-group-configured"></a>إذا كان عنوان الشحن الخاص بالعميل به مجموعة ضريبية مُكونة

إذا كان سجل عنوان الشحن الخاص بالعميل يحتوي على مجموعة ضريبية مُكونة وتم شحن الأمر عبر الإنترنت (أو صنف) إلى عنوان الشحن الخاص بالعميل، فسيتم استخدام المجموعة الضريبية المُكونة في سجل عنوان العميل بواسطة محرك الضرائب لحسابات الضرائب.

#### <a name="configure-a-tax-group-for-a-customers-shipping-address-record"></a>تكوين مجموعة ضريبية لسجل عنوان الشحن الخاص بالعميل

لتكوين مجموعة ضريبية لسجل عنوان الشحن الخاص بالعميل في المراكز الرئيسية لـ Commerce، اتبع هذه الخطوات.

1. انتقل إلى **كافة العملاء**، ثم حدد العميل المطلوب. 
1. في علامة التبويب السريعة **العناوين** ، حدد العنوان المطلوب، ثم حدد **المزيد من الخيارات \> خيارات متقدمة**. 
1. ضمن علامة التبويب **عام** في صفحة **إدارة العناوين** ، قم بتعيين قيمة ضريبة المبيعات حسب الحاجة.

> [!NOTE]
> يتم تحديد مجموعة الضرائب باستخدام عنوان التسليم لصنف الأمر ويتم تكوين الضرائب المستندة إلى الوجهة في مجموعة الضرائب نفسها. لمزيد من المعلومات، راجع [‏‫إعداد الضرائب للمتاجر على الإنترنت مستندة إلى الوجهة‬](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).

## <a name="order-pickup-in-store"></a>التقاط الأمر في المتجر

بالنسبة لأصناف الأمر ذات الوضع التقاط في المتجر أو التقاط على الطريق المُحدد، سيتم تطبيق المجموعة الضريبية من متجر الالتقاط المحدد. للحصول على تفاصيل حول كيفية تكوين مجموعة الضرائب لمتجر معين، راجع [تعيين خيارات الضرائب الأخرى للمتاجر](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).

> [!NOTE]
> عندما يتم استلام بند أمر في أحد المتاجر، سيتم تجاهل إعدادات ضريبة عنوان العميل (في حالة الإعداد) بواسطة محرك الضرائب وسيتم تطبيق تكوين ضريبة متجر الالتقاط. 

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على ضريبة المبيعات](https://docs.microsoft.com/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json) 

[طرق حساب ضريبة المبيعات في حقل الأصل](https://docs.microsoft.com/dynamics365/finance/general-ledger/sales-tax-calculation-methods-origin-field?toc=/dynamics365/commerce/toc.json) 

[ تعيين ضريبة المبيعات والتجاوزات](https://docs.microsoft.com/dynamics365/supply-chain/procurement/tasks/sales-tax-assignment-overrides?toc=/dynamics365/commerce/toc.json) 

[خيارات حساب المبلغ بالكامل والفاصل الزمني لأكواد ضريبة المبيعات](https://docs.microsoft.com/dynamics365/finance/general-ledger/whole-amount-interval-options-sales-tax-codes?toc=/dynamics365/commerce/toc.json) 

[حساب الإعفاء الضريبي](tax-exempt-price-inclusive.md) 

