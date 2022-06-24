---
title: تحديد سمة الموقع
description: يصف هذا المقال كيفية تعيين أو تغيير سمة خاصة بموقعك في Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b038dc996c571d54dce3f2aec679f7af8af85074
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900376"
---
# <a name="select-a-site-theme"></a>تحديد سمة الموقع

[!include [banner](includes/banner.md)]

يصف هذا المقال كيفية تعيين أو تغيير سمة خاصة بموقعك في Microsoft Dynamics 365 Commerce.

يتم تحديد تخطيط الموقع ونمطه (على سبيل المثال، الخطوط والأحجام والألوان) بواسطة السمة التي تحددها ويتم تطبيقها على الموقع. يتم إنشاء السمة ونشرها من قبل مطور يعمل في شركتك. للحصول على نظرة عامة حول السمات، راجع [نظرة عامة حول السمات](e-commerce-extensibility/theming.md). لمزيد من المعلومات حول كيفية إنشاء السمات ونشرها، راجع [إنشاء سمة جديدة](e-commerce-extensibility/create-theme.md).

بشكل افتراضي، عندما تقوم بإنشاء موقع للمرة الأولى، فإنه يستخدم سمة تُسمى **Fabrikam**. يتم توفير هذا النسق الافتراضي كجزء من مكتبة الوحدات النمطية في Commerce. بعد قيامك بتوزيع سمات إضافية للموقع الخاص بك، فإنه يمكنك تكوين الموقع بحيث يستخدم إحدى السمتين بدلاً من ذلك.

## <a name="select-the-site-theme"></a>تحديد سمة الموقع

لتحديد السمة المطبقة على موقعك، اتبع هذه الخطوات.

1. في بيئة التأليف الخاصة بالموقع، انتقل إلى الموقع الخاص بك.
1. انتقل إلى **إدارة الموقع** \> **قابلية التوسعة**.
1. ضمن **السمة**، حدد سمة من القائمة المنسدلة.
1. لتطبيق السمة المحددة على الموقع الخاص بك، حدد **حفظ ونشر**.

> [!NOTE]
> يتم نشر السمة التي تحددها على موقعك بمجرد تحديد **حفظ ونشر** في الصفحة **قابلية التوسعة**. لمعاينة سمة على موقعك قبل تطبيقها، يمكنك استخدام بيئة التطوير أو وضع الحماية.

## <a name="additional-resources"></a>الموارد الإضافية

[إضافة شعار](add-logo.md)

[العمل CSS مع ملفات التجاوز](css-override-files.md)

[إضافة أيقونة المفضلة](add-favicon.md)

[إضافة إشعار لحقوق النشر](add-copyright-notice.md)

[إضافة لغات إلى الموقع الخاص بك](add-languages-to-site.md)

[إضافة تعليمات برمجية لبرنامج نصي إلى صفحات الموقع لدعم تتبع الاستخدام](add-telemetry.md)

[نظرة عامة على النُسق](e-commerce-extensibility/theming.md)

[إنشاء سمة جديدة](e-commerce-extensibility/create-theme.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
