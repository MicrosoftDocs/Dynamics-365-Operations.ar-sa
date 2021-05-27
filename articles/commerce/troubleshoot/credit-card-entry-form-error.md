---
title: تعرض صفحة إدخال بطاقة الائتمان خطأ عند السحب
description: يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة عدم تحميل قسم طريقة الدفع وظهور رسالة خطأ.
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
ms.openlocfilehash: ea9105481e6c5812565f0d3604906c905bcb5443
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018496"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a>تعرض صفحة إدخال بطاقة الائتمان خطأ عند السحب

[!include [banner](../../includes/banner.md)]

يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة عدم تحميل قسم **طريقة الدفع** وظهور رسالة خطأ.

## <a name="description"></a>الوصف

عند فتح صفحة السداد مع الخروج من متجر على الإنترنت، لا يتم تحميل قسم **طريقة الدفع**، وتظهر رسالة الخطأ التالية: "حدث خطأ ما. الرجاء المحاولة مره أخرى لاحقا."

![خطأ الوحدة النمطية للدفع](media/payment-module-error.jpg)

## <a name="resolution"></a>الدقة

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a>انتظار انتهاء صلاحية ذاكره التخزين المؤقت لوحدة Commerce Scale Unit

يتم تخزين إعدادات خدمة الدفع في صفحة السداد مع الخروج لمتجر الإنترنت بشكل مؤقت في وحدة Commerce Scale Unit وقد تستغرق 15 دقيقه لتظهر في موقع التجارة الإلكترونية. تتضمن إعدادات خدمة الدفع هذه تغييرات في معرف حساب التاجر ومفتاح واجهة برمجة تطبيقات السحابة وإعدادات التكوين المتنوعة المرتبطة بطريقه الدفع.

## <a name="additional-resources"></a>الموارد الإضافية

[إعداد قناة على الإنترنت](../channel-setup-online.md)
