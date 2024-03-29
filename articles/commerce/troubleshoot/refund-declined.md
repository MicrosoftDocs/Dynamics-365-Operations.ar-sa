---
title: رفض المبلغ المسترد في أمر الإرجاع
description: يوفر هذا المقال إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة رفض المبلغ المسترد لأمر الإرجاع نظرا لأن بطاقة الائتمان المستخدمة للفوترة تختلف عن البطاقة التي تم استخدامها أثناء تفويض الدفع الأصلي.
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
ms.openlocfilehash: d8d1c40673d4b159a7b7bf00bf6011ba45f47edd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268222"
---
# <a name="refund-on-a-return-order-is-declined"></a>رفض المبلغ المسترد في أمر الإرجاع

[!include [banner](../../includes/banner.md)]

يوفر هذا المقال إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة رفض المبلغ المسترد لأمر الإرجاع نظرا لأن بطاقة الائتمان المستخدمة للفوترة تختلف عن البطاقة التي تم استخدامها أثناء تفويض الدفع الأصلي.

## <a name="description"></a>الوصف

يتم رفض المبلغ المسترد عندما تختلف بطاقة الائتمان المستخدمة لفوترة أمر الإرجاع عن البطاقة التي تم استخدامها أثناء تفويض الدفع الأصلي. تظهر رسالة الخطا التالية: بعض المدفوعات ليست بالحالة الصحيحة للترحيل. الرجاء إعادة التحقق من صحة حالة كافة المدفوعات السابقة للفوترة."

ستتضمن تفاصيل تخويل الدفع رسالة الخطا التالية: "فشل SendRequest() في بوابة Adyen بالحالة'InternalServerError'.22144; تم إرجاع استجابة فارغة من Adyen.(22001);"

![خطأ رفض المبلغ المسترد في أمر الإرجاع.](media/refund-order-decline.jpg)

## <a name="resolution"></a>الحل

### <a name="enable-blind-returns-in-adyen"></a>تمكين المرتجعات المخفيه في Adyen

لتمكين المرتجعات المخفية، اتبع الخطوات الموجودة في [استكشاف الأخطاء وإصلاح مشكلات موصل الدفع Dynamics 365 لـ Adyen](adyen-support.md) للاتصال بفريق دعم Adyen وطلب أن يتم تمكين المرتجعات المخفية في حساب تاجر Adyen الخاص بك.

## <a name="additional-resources"></a>الموارد الإضافية

[موصل دفع Dynamics 365 لـ Adyen](../dev-itpro/adyen-connector.md)

[إعداد موصل دفع Adyen لـ Dynamics 365](https://docs.adyen.com/plugins/microsoft-dynamics)
