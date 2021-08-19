---
title: خطا مزامنة الأمر المرتبط بخدمة الدفع الافتراضية
description: يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في إصلاح خطأ قد يحدث عند مزامنة أمر عبر الإنترنت.
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
ms.openlocfilehash: 6f8e0ea7675ffc5cbada36207422b410234e33afcaec90636e90e573a90ac484
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6715226"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a>خطا مزامنة الأمر المرتبط بخدمة الدفع الافتراضية

[!include [banner](../../includes/banner.md)]

يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في إصلاح خطأ قد يحدث عند مزامنة أمر عبر الإنترنت.

## <a name="description"></a>الوصف

عند مزامنة أحد الأوامر عبر الإنترنت، تتلقي رسالة الخطأ التالية: "يجب أن يكون هناك خدمة دفع افتراضية لمعالجة حركات بطاقات الائتمان."

![خطأ خدمة الدفع الافتراضية مفقودة.](media/default-payment-method-error.jpg)

## <a name="resolution"></a>الحل

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a>تأكيد خدمة الدفع الافتراضية في المركز الرئيسي لـ Commerce أو تعيينها

لتأكيد خدمة الدفع الافتراضية في المركز الرئيسي لـ Commerce أو تعيينها، اتبع الخطوات التالية.

1. انتقل إلى **الحسابات المدينة \> إعداد المدفوعات‬ \> ‏‫خدمات الدفع‬**.
1. تأكد من تعيين خيار **المعالج الافتراضي لبطاقات الائتمان الجديدة** على **نعم** لخدمة دفع واحدة.

## <a name="additional-resources"></a>الموارد الإضافية

[إعداد بطاقة الائتمان وتفويضها والتقاطها](../../finance/accounts-receivable/credit-card-authorizations.md)