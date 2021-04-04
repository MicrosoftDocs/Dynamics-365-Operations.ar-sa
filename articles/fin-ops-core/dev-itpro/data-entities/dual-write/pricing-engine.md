---
title: المزامنة عند الطلب باستخدام محرك تسعير Supply Chain Management
description: يصف هذا الموضوع كيفية استخدام محرك التسعير في  Microsoft Dynamics 365 Supply Chain Management من Dynamics 365 Sales.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: e2067e83d3f0c98e986873b8eaf1b817de912c0f
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570130"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a>المزامنة عند الطلب باستخدام محرك تسعير Supply Chain Management

[!include [banner](../../includes/banner.md)]



يتضمن Microsoft Dynamics 365 Supply Chain Management محرك تسعير يتعامل مع اتفاقيات التجارة وقوائم الأسعار وبرامج ولاء العملاء والعروض الترويجية والخصومات. يستخدم محرك التسعير قواعد معقدة لتحديد أفضل سعر لعرض أسعار أو أمر معين. عند استخدام الكتابة الثنائية، فإنك تستخدم إما محرك التسعير من Dynamics 365 Supply Chain Managementمن صفحات عرض الأسعار والنظام في Dynamics 365 Sales.

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a>استخدام محرك التسعير من Supply Chain Management في Sales

1. في Sales، انتقل إلى **Sales \> الأوامر**.
2. حدد **جديد** لإنشاء أمر جديد أو حدد أمرًا موجودًا في قائمة **الأوامر الخاصة بي**.
3. أضف بند أمر جديدًا.
4. إذا كنت تقوم بإنشاء أمر جديد، فحدد **أمر سعر** في جزء الإجراء. إذا كنت تقوم بتحديث أمر موجود، فحدد **إعادة حساب** في جزء الإجراء.

    يتم ملء الأعمدة التالية تلقائيًا:

    + تفاصيل المبلغ
    + النسبة المئوية للخصم
    + الخصم
    + مبلغ ما قبل الشحن
    + مبلغ الشحن
    + إجمالي الضريبة
    + المبلغ الإجمالي
    
5. لضمان أن النظام يضع في الاعتبار اتفاقيات التجارة والبيع لحساب السعر:
    1. انتقل إلى بيئة Supply Chain Management.
    2. انتقل إلى **الحسابات المدينة \> إعداد \> معلمات الحسابات المدينة**.
    3. حدد علامة تبويب **الأسعار** في شريط التنقل الجانبي.
    4. تحت علامة التبويب السريعة **تقييم اتفاقية التجارة** قم بإلغاء تحديد خيار **الإدخال اليدوي**.

## <a name="how-it-works"></a>كيف يعمل

عند تحديد **أمر السعر** في Sales، يتم استدعاء وظيفة **الإجماليات** في علامة التبويب **أمر المبيعات\> عرض** في Supply Chain Management لأمر المبيعات المقترن. يتم استخدام القيم في إجمالي الأمر في Sales لملء الأعمدة المقابلة في Supply Chain Management.

عند حساب إجمالي أمر المبيعات في Supply Chain Management، يقيّم الحساب اتفاقيات التجارة واتفاقيات المبيعات الحالية للعميل والمنتجات المدرجة في أمر المبيعات. يتم استخدام هذه المعلومات لحساب الإجماليات. عند تحديد **أمر السعر**، يعكس Sales تلقائيًا كل الإعداد الذي تم إجراؤه في Supply Chain Management.

## <a name="limitations"></a>قيود

عند ملء الأعمدة في Sales، يتم تطبيق القيود التالية:

+ لا يتم تكرار إعداد الرسوم ومخصصات الرسوم في Supply Chain Management في Sales.
+ لا يأخذ التشعير بعين الاعتبار تسعير البيع بالتجزئة الخاص المحدد في عمود **قناة البيع بالتجزئة** في صفحة بند أمر المبيعات في Supply Chain Management.
+ لا يتم الأخذ بعين الاعتبار الخصومات المحددة في قسم **إدارة البدل التجاري‬** في Supply Chain Management.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]