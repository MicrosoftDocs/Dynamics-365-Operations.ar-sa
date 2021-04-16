---
title: خطأ نوع الدفع يجب أن يكون بطاقة ائتمان في صفحة أمر المبيعات
description: يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة ظهور رسالة خطأ في صفحة أمر المبيعات بعد مزامنة أحد الأوامر.
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
ms.openlocfilehash: eabc64acc74645c7e6c7c4ab5794ed9fdb9dc997
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801665"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a>خطأ "نوع الدفع يجب أن يكون بطاقة ائتمان" في صفحة أمر المبيعات

[!include [banner](../../includes/banner.md)]

يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة ظهور رسالة خطأ في صفحة أمر المبيعات بعد مزامنة أحد الأوامر.

## <a name="description"></a>الوصف

عند فتح صفحة أمر المبيعات بعد مزامنة أحد الأوامر، تتلقي رسالة الخطا التالية: "يجب أن يكون نوع الدفع بطاقة ائتمان، نظرًا لأنه تم تحديد رقم بطاقة الائتمان."

![خطأ نوع الدفع يجب أن يكون بطاقة ائتمان](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a>الدقة

### <a name="set-the-payment-type-in-commerce-headquarters"></a>تعيين نوع الدفع في المركز الرئيسي لـ Commerce

1. انتقل إلى **الحسابات المدينة \> إعداد المدفوعات‬ \> شروط الدفع**.
1. فى جزء التنقل الأيمن، حدد شروط الدفع.
1. في حقل **نوع الدفع**، تأكد من تحديد **بطاقة ائتمان**.

## <a name="additional-resources"></a>الموارد الإضافية

[ترحيل الدفعات والمبيعات على الإنترنت](../tasks/posting-online-sales-payments.md)
