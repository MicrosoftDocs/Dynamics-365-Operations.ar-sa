---
title: خطا مزامنة الأمر المرتبط بخدمة الدفع الافتراضية
description: يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في إصلاح خطأ قد يحدث عند مزامنة أمر عبر الإنترنت.
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
ms.openlocfilehash: 45eeae751051b58e1c9e725eb4ed4b5240026e7f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801425"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a>خطا مزامنة الأمر المرتبط بخدمة الدفع الافتراضية

[!include [banner](../../includes/banner.md)]

يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في إصلاح خطأ قد يحدث عند مزامنة أمر عبر الإنترنت.

## <a name="description"></a>الوصف

عند مزامنة أحد الأوامر عبر الإنترنت، تتلقي رسالة الخطأ التالية: "يجب أن يكون هناك خدمة دفع افتراضية لمعالجة حركات بطاقات الائتمان."

![خطأ خدمة الدفع الافتراضية مفقودة](media/default-payment-method-error.jpg)

## <a name="resolution"></a>الدقة

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a>تأكيد خدمة الدفع الافتراضية في المركز الرئيسي لـ Commerce أو تعيينها

لتأكيد خدمة الدفع الافتراضية في المركز الرئيسي لـ Commerce أو تعيينها، اتبع الخطوات التالية.

1. انتقل إلى **الحسابات المدينة \> إعداد المدفوعات‬ \> ‏‫خدمات الدفع‬**.
1. تأكد من تعيين خيار **المعالج الافتراضي لبطاقات الائتمان الجديدة** على **نعم** لخدمة دفع واحدة.

## <a name="additional-resources"></a>الموارد الإضافية

[إعداد بطاقة الائتمان وتفويضها والتقاطها](https://docs.microsoft.com/dynamics365/finance/accounts-receivable/credit-card-authorizations)
