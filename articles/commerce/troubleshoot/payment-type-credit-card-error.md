---
title: خطأ نوع الدفع يجب أن يكون بطاقة ائتمان في صفحة أمر المبيعات
description: يوفر هذا المقال إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة ظهور رسالة خطأ في صفحة أمر المبيعات بعد مزامنة أحد الأوامر.
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
ms.openlocfilehash: 71c5cbaf574866c74e222f4d67132004327db8fe
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285622"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a>خطأ "نوع الدفع يجب أن يكون بطاقة ائتمان" في صفحة أمر المبيعات

[!include [banner](../../includes/banner.md)]

يوفر هذا المقال إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة ظهور رسالة خطأ في صفحة أمر المبيعات بعد مزامنة أحد الأوامر.

## <a name="description"></a>الوصف

عند فتح صفحة أمر المبيعات بعد مزامنة أحد الأوامر، تتلقي رسالة الخطا التالية: "يجب أن يكون نوع الدفع بطاقة ائتمان، نظرًا لأنه تم تحديد رقم بطاقة الائتمان."

![خطأ نوع الدفع يجب أن يكون بطاقة ائتمان.](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a>الحل

### <a name="set-the-payment-type-in-commerce-headquarters"></a>تعيين نوع الدفع في المركز الرئيسي لـ Commerce

1. انتقل إلى **الحسابات المدينة \> إعداد المدفوعات‬ \> شروط الدفع**.
1. فى جزء التنقل الأيمن، حدد شروط الدفع.
1. في حقل **نوع الدفع**، تأكد من تحديد **بطاقة ائتمان**.

## <a name="additional-resources"></a>الموارد الإضافية

[ترحيل الدفعات والمبيعات على الإنترنت](../tasks/posting-online-sales-payments.md)
