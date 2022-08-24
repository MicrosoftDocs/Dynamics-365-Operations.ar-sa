---
title: لا تظهر سجلات العملاء في Commerce Headquarters
description: يوفر هذا المقال إرشادات استكشاف الأخطاء وإصلاحها التي يمكن أن تساعد في حالة عدم ظهور سجلات العملاء على الفور في Commerce headquarters.
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
ms.openlocfilehash: f1ad1f45abbc95cbf6d41b3c8681db781c6c9d23
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268828"
---
# <a name="customer-records-dont-appear-in-commerce-headquarters"></a>لا تظهر سجلات العملاء في Commerce Headquarters

[!include [banner](../../includes/banner.md)]

يوفر هذا المقال إرشادات استكشاف الأخطاء وإصلاحها التي يمكن أن تساعد في حالة عدم ظهور سجلات العملاء على الفور في Commerce headquarters.

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
