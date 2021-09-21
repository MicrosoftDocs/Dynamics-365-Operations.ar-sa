---
title: المزامنة عند الطلب باستخدام محرك تسعير Supply Chain Management
description: يصف هذا الموضوع كيفية استخدام محرك التسعير في  Microsoft Dynamics 365 Supply Chain Management من Dynamics 365 Sales.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: f84a81444e6d5ce9a0d2da4c9a60b1ae3478ee2f
ms.sourcegitcommit: 2d8035f8bb75957c793c0d293c079a792595eeaf
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/08/2021
ms.locfileid: "7481305"
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
    
5. لضمان أن النظام يضع في الاعتبار اتفاقيات التجارة لحساب السعر:
    1. انتقل إلى بيئة Supply Chain Management.
    2. انتقل إلى **الحسابات المدينة \> إعداد \> معلمات الحسابات المدينة**.
    3. حدد علامة تبويب **الأسعار** في شريط التنقل الجانبي.
    4. تحت علامة التبويب السريعة **تقييم اتفاقية التجارة** قم بإلغاء تحديد خيار **الإدخال اليدوي**.

## <a name="how-it-works"></a>كيف يعمل

عند تحديد **أمر السعر** في Sales، يتم استدعاء وظيفة **الإجماليات** في علامة التبويب **أمر المبيعات\> عرض** في Supply Chain Management لأمر المبيعات المقترن. يتم استخدام القيم في إجمالي الأمر في Sales لملء الأعمدة المقابلة في Supply Chain Management.

عند حساب إجمالي أمر المبيعات في Supply Chain Management، يقيّم الحساب اتفاقيات التجارة واتفاقيات الحالية للعميل والمنتجات المدرجة في أمر المبيعات. يتم استخدام هذه المعلومات لحساب الإجماليات. عند تحديد **أمر السعر**، يعكس Sales تلقائيًا كل الإعداد الذي تم إجراؤه في Supply Chain Management.

## <a name="limitations"></a>قيود

عند ملء الأعمدة في Sales، يتم تطبيق القيود التالية:

+ لا يتم تكرار إعداد الرسوم ومخصصات الرسوم في Supply Chain Management في Sales.
+ لا يأخذ التشعير بعين الاعتبار تسعير البيع بالتجزئة الخاص المحدد في عمود **قناة البيع بالتجزئة** في صفحة بند أمر المبيعات في Supply Chain Management.
+ لا يتم الأخذ بعين الاعتبار الخصومات المحددة في قسم **إدارة البدل التجاري‬** في Supply Chain Management.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
