---
title: عدم ظهور خيار الحفظ للدفع التالي
description: يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة عدم ظهور خانة الاختيار الحفظ للدفع التالي تحت طريقه الدفع في صفحة السداد مع الخروج الخاصة بموقع التجارة الإلكترونية.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 7e3156d1aa9a05dc5d159b6f9b33ae341de640bf
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801689"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a>عدم ظهور خيار "الحفظ للدفع التالي"

[!include [banner](../../includes/banner.md)]

يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة عدم ظهور خانة الاختيار **الحفظ للدفع التالي** تحت **طريقه الدفع** في صفحة السداد مع الخروج الخاصة بموقع التجارة الإلكترونية.

## <a name="description"></a>الوصف

لا تظهر خانة الاختيار **الحفظ للدفع التالي** في قسم **طريقة الدفع** في صفحة السداد مع الخروج لموقع التجارة الإلكترونية.

يبين الرسم التوضيحي التالي مثالا لصفحة السداد مع الخروج التي تتضمن خانة الاختيار **الحفظ للدفع التالي**.

![خانة الاختيار الحفظ للدفع التالي في وحدة الدفع النمطية](media/payment-module-save-payment.jpg)

## <a name="resolution"></a>الدقة

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a>التحقق من تكوين موصل الدفع Dynamics 365 لـ Adyen بشكل صحيح في المركز الرئيسي لـ Commerce

للتحقق من تكوين موصل الدفع Dynamics 365 لـ Adyen بشكل صحيح في المركز الرئيسي لـ Commerce، اتبع الخطوات التالية.

1. انتقل إلى **Retail وCommerce \> القنوات \> المتاجر على الإنترنت**.
1. حدد متجر على الإنترنت.
1. في علامة التبويب السريعة **حسابات الدفع**، تأكد من تعيين حقل **السماح بحفظ معلومات الدفع في التجارة الإلكترونية** على القيمة **True**.

![السماح بحفظ معلومات الدفع في حقل التجارة الإلكترونية في المركز الرئيسي لـ Commerce](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a>الموارد الإضافية

[الوحدة النمطية للدفع](../payment-module.md)

[حفظ وسائل الدفع عبر الإنترنت باستخدام موصل Adyen](../dev-itpro/adyen-connector-listPI.md)
