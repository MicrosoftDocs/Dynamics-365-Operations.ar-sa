---
title: لا تظهر سجلات العملاء في المركز الرئيسية لـ Commerce
description: يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها التي يمكن أن تساعد في حالة عدم ظهور سجلات العملاء على الفور في المركز الرئيسي لـ Commerce.
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
ms.openlocfilehash: 5499e3c059c9e735df87ef8b462d446e0710d90c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801785"
---
# <a name="customer-records-dont-appear-in-commerce-headquarters"></a>لا تظهر سجلات العملاء في المركز الرئيسية لـ Commerce

[!include [banner](../../includes/banner.md)]

يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها التي يمكن أن تساعد في حالة عدم ظهور سجلات العملاء على الفور في المركز الرئيسي لـ Commerce.

## <a name="description"></a>الوصف

عند إنشاء سجل عميل جديد باستخدام تدفق التسجيل في واجهة متجر التجارة الإلكترونية، لا يظهر سجل العميل المقابل على الفور في المركز الرئيسي لـ Commerce.

## <a name="resolution"></a>الدقة

### <a name="disable-customer-creation-in-async-mode"></a>تعطيل إنشاء العملاء في الوضع غير المتزامن

> [!IMPORTANT]
> إذا قمت بتعطيل إنشاء عميل غير متزامن، فقد يتأثر أداء النظام، لأن إنشاء كل سجل سينتج طلبًا في الوقت الحقيقي إلى المركز الرئيسي لـ Commerce. بالإضافة إلى ذلك، إذا كان المركز الرئيسي لـ Commerce معطلًا (على سبيل المثال، أثناء تدفقات الصيانة)، فإن أي تدفقات إنشاء عميل جديد سوف تنتج أخطاء.

لتعطيل إنشاء العملاء في الوضع غير المتزامن في المركز الرئيسي لـ Commerce، اتبع الخطوات التالية.

1. انتقل إلى **Retail وCommerce \> إعداد القناة \> إعداد متجر على الإنترنت \> ملفات تعريف الوظائف**.
1. إذا لم تكن تستخدم بالفعل ملف تعريف وظائف للقناة على الإنترنت، فقم بإنشاء واحد.
1. تأكد من تعيين الخيار **إنشاء عميل في الوضع غير متزامن** إلى **لا**.
1. انتقل إلى **Retail وCommerce \> القنوات \> المتاجر على الإنترنت**.
1. حدد المتجر على الإنترنت لتعطيل إنشاء العميل غير المتزامن له.
1. في علامة التبويب **عام**، تأكد من تعيين حقل **ملف تعريف الوظائف** على ملف تعريف الوظائف الذي تستخدمه في القناة على الإنترنت.

## <a name="additional-resources"></a>الموارد الإضافية

[إعداد مستأجر متاجرة عمل-مستهلك في Commerce](../set-up-b2c-tenant.md)
