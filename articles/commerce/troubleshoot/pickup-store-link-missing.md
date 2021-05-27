---
title: لا يظهر خيار الانتقاء في صفحات سلة التسوق أو تفاصيل المنتج
description: يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة عدم ظهور خيار التقاط في المتجر على صفحة سلة التسوق أو تفاصيل المنتج.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f692d73bf1755422e9bfc8314c1156e043ccf761
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020794"
---
# <a name="pick-this-up-option-doesnt-appear-on-cart-or-product-details-pages"></a>لا يظهر خيار "انتقاء هذا" في صفحات سلة التسوق أو تفاصيل المنتج

[!include [banner](../../includes/banner.md)]

يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة عدم ظهور خيار التقاط في المتجر على صفحة سلة التسوق أو تفاصيل المنتج.

## <a name="description"></a>الوصف

لا يظهر زر **انتقاء هذا** في صفحة سلة التسوق أو صفحات تفاصيل المنتج.

يبين الرسم التوضيحي التالي مثالا للصفحة التي تتضمن زر **انتقاء هذا**.

![زر انتهاء هذا](media/pickup-button-missing.jpg)

## <a name="resolution"></a>الدقة

### <a name="enable-the-bopis-extension-in-commerce-site-builder"></a>تمكين ملحق BOPIS في منشئ مواقع Commerce

لتمكين ملحق "الشراء عبر الإنترنت، الانتقاء في المتجر" (BOPIS) في منشئ موقع Commerce، اتبع الخطوات التالية.

1. حدد موقعك.
1. حدد **إعدادات الموقع**، ثم حدد **الملحقات**.
1. تاكد من أنه تم مسح خيار **تعطيل BOPIS**.

### <a name="configure-modes-of-delivery-in-commerce-headquarters"></a>تكوين أوضاع التسليم في المركز الرئيسي لـ Commerce

لتكوين أوضاع التسليم في المركز الرئيسي لـ Commerce، اتبع الخطوات التالية.

1. انتقل إلى **‏‫التدبير والتوريد‬ \> الإعداد \> أوضاع التسليم**.
1. تأكد من أنه تم إنشاء وضع **الالتقاط للعميل**، وأنه تعيين المنتجات والعناوين إليه.
1. انتقل إلى **Retail وCommerce \> إعداد المركز الرئيسي \> المعلمات**.
1. في جزء التنقل الأيسر، حدد **أوامر العملاء**.
1. تأكد من تكوين **وضع انتقاء التسليم** بشكل صحيح.

### <a name="configure-customer-orders-payments"></a>تكوين مدفوعات أوامر العميل

لتكوين مدفوعات أوامر العميل في المركز الرئيسي لـ Commerce، اتبع الخطوات التالية.

1. انتقل إلى **Retail وCommerce \> إعداد المركز الرئيسي \> المعلمات**.
1. في جزء التنقل الأيسر، حدد **أوامر العملاء**.
1. في علامة التبويب السريعة **المدفوعات**، تأكد من تعيين حقول **شروط الدفع** و **طريقة الدفع** بشكل صحيح.

## <a name="additional-resources"></a>الموارد الإضافية

[تكوين BOPIS](../cpe-bopis.md)

[تمكين أوضاع تسليم الانتقاء المتعددة لأوامر العملاء](../multiple-pickup-modes.md)

[مدفوعات أمر Commerce بالقناة متعددة الاتجاهات](../dev-itpro/commerce-payments.md)

[الوحدة النمطية لمحدد المتجر](../store-selector.md)
