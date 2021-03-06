---
title: دمج الشحنات عند تجاوز سياسة دمج الشحنات من صفحة الإصدار إلى المستودع
description: يقدم هذا الموضوع سيناريو يجب أن يتم فيه إصدار بند مبيعات واحد أو أكثر يدويا إلى المستودع من صفحة الإصدار إلى المستودع، ويجب تجاوز نهج دمج الشحنات المحدد بواسطة النظام قبل الإصدار.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipConsolidationSetShipment, WHSShipmentConsolidation, WHSFilterGenerallyAvail, WHSReleaseToWarehouse
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 4aaaa7949d988607b38dd6e38a3c3497f227b8af
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963325"
---
# <a name="consolidate-shipments-when-the-shipment-consolidation-policy-is-overridden-from-the-release-to-warehouse-page"></a>دمج الشحنات عند تجاوز سياسة دمج الشحنات من صفحة الإصدار إلى المستودع

[!include [banner](../includes/banner.md)]

يقدم هذا الموضوع سيناريو يجب أن يتم فيه إصدار بند مبيعات واحد أو أكثر يدويا إلى المستودع من صفحة **الإصدار إلى المستودع**، ويجب تجاوز نهج دمج الشحنات المحدد بواسطة النظام قبل الإصدار. قد يكون تجاوز نهج دمج الشحنات مطلوبًا، إذا كان الأمر، على سبيل المثال، الذي لم يتم دمجه عادة مع الشحنات المفتوحة يلزم دمجه مع شحنات مفتوحة.

أثناء السيناريو، ستقوم بإنشاء مجموعة من أوامر المبيعات ثم تجاوز نهج دمج الشحنات الافتراضية قبل إصدار الأوامر إلى المستودع.

## <a name="make-demo-data-available"></a>جعل بيانات العرض التوضيحي متاحة

يشير السيناريو في هذا الموضوع إلى قيم وسجلات مضمنة في بيانات العرض التوضيحي القياسية المتوفرة لـ Microsoft Dynamics 365 Supply Chain Management. إذا كنت ترغب في استخدام القيم الواردة هنا أثناء تنفيذ التمرينات، فتأكد من العمل في بيئة تم فيها تثبيت بيانات العرض التوضيحي، وقم بتعيين الكيان القانوني إلى **USMF** قبل أن تبدأ.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>إعداد نُهج دمج الشحنات وعوامل تصفيه المنتجات

يفترض السيناريو الموضح هنا أنك قمت بالفعل بتشغيل الميزة، ونفذت التمرينات في [تكوين نهج دمج الشحنات](configure-shipment-consolidation-policies.md)، وإنشاء النهج والسجلات الأخرى التي تم وصفها هناك. تأكد من تنفيذ تلك التمرينات قبل المتابعة في هذا السيناريو.

## <a name="create-the-sales-orders-for-this-scenario"></a>إنشاء أوامر مبيعات لهذا السيناريو

1. انتقل إلى **الحسابات المدينة \> أوامر المبيعات \> جميع أوامر المبيعات** وقم بإنشاء ثلاثة أوامر مبيعات متماثلة تتضمن الإعدادات التالية:

    - **حساب العميل:** *US-002*

1. أضف بند أمر يتضمن الإعدادات التالية:

    - **رقم الصنف:** *A0001* (صنف لم يتم تعيين عامل تصفية **الرمز 4** له)
    - **الكمية:** *1.00*

1. حدد **المخزون \> حجز**، ثم في جزء الإجراءات، حدد **حجز الدفعة** لحجز بند الأمر.

## <a name="release-the-sales-orders-from-the-release-to-warehouse-page"></a>إصدار أوامر المبيعات من صفحة الإصدار إلى المستودع

اتبع الخطوات التالية لتجاوز نهج دمج الشحنات أثناء الإصدار إلى المستودع.

1. انتقل إلى **إدارة المستودعات \> الإصدار إلى المستودع \> الإصدار إلى المستودع**.
1. في الجزء العلوي، حدد أمر المبيعات الأول الذي قمت بإنشائه لهذا السيناريو.
1. حدد **إضافة** لإضافة البند إلى الإصدار إلى المستودع. لاحظ أنه تم تطبيق نهج دمج الشحنات *الافتراضي* في الجزء السفلي.
1. في الجزء السفلي، حدد **تحديد نهج دمج شحنات جديد**.
1. حدد نهجًا يسمح بالدمج مع الشحنات المفتوحة الأخرى لنفس النهج. على سبيل المثال، حدد نهج *CustomerOrderNo*.
1. حدد **الإصدار إلى المستودع**.
1. حدد أمر المبيعات الثاني والثالث الذي قمت بإنشائه لهذا السيناريو.
1. حدد **إضافة** لإضافة البنود إلى الإصدار إلى المستودع. لاحظ أنه تم تطبيق النهج *الافتراضي* في الجزء السفلي.
1. حدد البند الثاني، ثم في حقل **تحديد نهج دمج الشحنات الجديد**، حدد نهج *CustomerOrderNo*.
1. حدد **الإصدار إلى المستودع** لكل من البندين.

## <a name="verify-the-shipments"></a>التحقق من الشحنات

ينبغي أن يتم إنشاء شحنتين:

- تحتوي الشحنة الأولى على بندين وتم إنشاؤها باستخدام نهج دمج الشحنات *CustomerOrderNo*.
- تحتوي الشحنة الثاني على بند واحد وتم إنشاؤها باستخدام نهج دمج الشحنات *الافتراضي*.

اتبع هذه الخطوات لمراجعة الشحنات التي تم إنشاؤها.

1. انتقل إلى **إدارة المستودعات \> الشحنات \> جميع الشحنات**.
1. ابحث عن الشحنة المطلوبة وحددها.
1. في حقل **نهج دمج الشحنات**، رجع نهج الدمج الذي تم استخدامه عند إنشاء الشحنة.

## <a name="additional-resources"></a>الموارد الإضافية

- [سياسات دمج الشحنات](about-shipment-consolidation-policies.md)
- [تكوين نُهج دمج الشحنات](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]