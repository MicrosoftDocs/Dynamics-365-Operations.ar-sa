---
title: المنتجات والفئات مفقودة بعد نسخ البيئة
description: يوفر هذا المقال إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة عدم العثور على المنتجات والفئات بعد نسخ الموقع بين البيئات أو داخل نفس البيئة.
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
ms.openlocfilehash: d8df3f4cca6a7aaad98ffb7f2d284211a4f9589b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277896"
---
# <a name="products-and-categories-missing-after-environment-copy"></a>المنتجات والفئات مفقودة بعد نسخ البيئة

[!include [banner](../../includes/banner.md)]

يوفر هذا المقال إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة عدم العثور على المنتجات والفئات بعد نسخ الموقع بين البيئات أو داخل نفس البيئة.

## <a name="description"></a>الوصف

بعد نسخ الموقع من بيئة إلى أخرى، أو في نفس البيئة، يتم فقدان المنتجات والفئات من الموقع. تكون المنتجات والفئات مفقودة من واجهة متجر التجارة الإلكترونية ومن علامة تبويب **المنتجات** في منشئ موقع Commerce.

## <a name="resolution"></a>الدقة

### <a name="map-the-channel-operating-unit-number-to-a-newly-copied-site-in-commerce-site-builder"></a>تعيين رقم وحدة تشغيل القناة إلى موقع تم نسخه حديثًا في منشئ موقع Commerce

لتعيين رقم وحدة التشغيل (OUN) للقناة إلى موقع تم نسخه حديثًا في منشئ موقع Commerce، اتبع الخطوات التالية.

1. حدد الموقع المنسوخ حديثًا.
1. ضمن **إعدادات الموقع**، حدد **القنوات**.
1. بجوار اسم القناة، حدد علامة القطع (**...**)، ثم حدد **تغيير قناة المتجر على الإنترنت**.
1. في مربع الحوار **تغيير قناة المتجر على الإنترنت**، حدد القناة التي تريد تعيينها للموقع المنسوخ حديثًا، ثم حدد **موافق**.
1. حدد **حفظ ونشر**.

## <a name="additional-resources"></a>الموارد الإضافية

[إقران موقع Dynamics 365 Commerce بقناة عبر الإنترنت](../associate-site-online-store.md)
