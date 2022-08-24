---
title: عدم ظهور خيار الحفظ للدفع التالي
description: يوفر هذا المقال إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة عدم ظهور خانة الاختيار الحفظ للدفع التالي تحت طريقه الدفع في صفحة السداد مع الخروج الخاصة بموقع التجارة الإلكترونية.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: d0b398a4ffc5fb698ea04ba8642d05ccd4caf04c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287474"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a>عدم ظهور خيار "الحفظ للدفع التالي"

[!include [banner](../../includes/banner.md)]

يوفر هذا المقال إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة عدم ظهور خانة الاختيار **الحفظ للدفع التالي** تحت **طريقه الدفع** في صفحة السداد مع الخروج الخاصة بموقع التجارة الإلكترونية.

## <a name="description"></a>الوصف

لا تظهر خانة الاختيار **الحفظ للدفع التالي** في قسم **طريقة الدفع** في صفحة السداد مع الخروج لموقع التجارة الإلكترونية.

يبين الرسم التوضيحي التالي مثالا لصفحة السداد مع الخروج التي تتضمن خانة الاختيار **الحفظ للدفع التالي**.

![خانة الاختيار الحفظ للدفع التالي في وحدة الدفع النمطية.](media/payment-module-save-payment.jpg)

## <a name="resolution"></a>الحل

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a>التحقق من تكوين موصل الدفع Dynamics 365 لـ Adyen بشكل صحيح في المركز الرئيسي لـ Commerce

للتحقق من تكوين موصل الدفع Dynamics 365 لـ Adyen بشكل صحيح في المركز الرئيسي لـ Commerce، اتبع الخطوات التالية.

1. انتقل إلى **Retail وCommerce \> القنوات \> المتاجر على الإنترنت**.
1. حدد متجر على الإنترنت.
1. في علامة التبويب السريعة **حسابات الدفع**، تأكد من تعيين حقل **السماح بحفظ معلومات الدفع في التجارة الإلكترونية** على القيمة **True**.

![السماح بحفظ معلومات الدفع في حقل التجارة الإلكترونية في المركز الرئيسي لـ Commerce.](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a>الموارد الإضافية

[وحدة للدفع](../payment-module.md)

[حفظ وسائل الدفع عبر الإنترنت باستخدام موصل Adyen](../dev-itpro/adyen-connector-listPI.md)
