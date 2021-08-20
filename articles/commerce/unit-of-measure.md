---
title: تطبيق إعدادات وحدة القياس
description: يغطي هذا الموضوع إعدادات وحدة القياس ويصف كيفية تطبيقها في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7fe5cf6b57a8897a0bd541146cb1ad17b496d5633c0a1df9d58b2a4fbc868139
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6761504"
---
# <a name="apply-unit-of-measure-settings"></a>تطبيق إعدادات وحدة القياس

[!include [banner](includes/banner.md)]

يغطي هذا الموضوع إعدادات وحدة القياس ويصف كيفية تطبيقها في Microsoft Dynamics 365 Commerce.

يمكن بيع المنتج في وحدات مختلفة، مثل "كل" و"زوج" و"دستة". في مقر Commerce، يمكن تعريف وحدة قياس البيع حسب المنتج وعرضها على موقع التجارة الإلكترونية. على سبيل المثال، إذا قام بائع تجزئة ببيع منتج ما بشكل فردي أو بالعشرات، فيمكن عرض وحدات القياس المتاحة مع معلومات المنتج الأخرى.

في المثال الموضح في الرسم التوضيحي التالي، يتم بيع وحدة قياس مقدارها **ea** تم تكوين (كل) لمنتج في Commerce headquarters.

![مثال على منتج تم تكوينه باستخدام وحدة قياس في المقر الرئيسي لـ Commerce.](./media/Productunit-headquarters.PNG)

> [!NOTE]
> يتوفر دعم لتطبيق وإظهار وحدة القياس اعتبارًا من إصدار Commerce رقم 10.0.19.

## <a name="unit-of-measure-settings"></a>إعدادات وحدة القياس

يتم تحديد إعدادات عرض وحدة القياس في منشئ موقع Commerce، في **إعدادات الموقع \> الأبعاد \> عرض وحدة القياس للمنتجات**. هناك ثلاثة إعدادات مدعومة:

- **عدم العرض** – عند تحديد هذا الإعداد، لن يعرض موقع التجارة الإلكترونية وحدة قياس المنتج. هذا السلوك هو السلوك الافتراضي.
- **عرض في تجربة شراء المنتج** – عند تحديد هذا الإعداد، يتم عرض وحدة القياس في صفحات تفاصيل المنتج، وعربة التسوق، والسداد، وسجل الطلبات، وصفحات تفاصيل الأمر.
- **عرض في تصفح المنتج وتجربة الشراء** – عند تحديد هذا الإعداد، يتم عرض وحدة القياس على صفحات تجربة شراء المنتج وأيضًا أثناء تجربة تصفح المنتج. كجزء من هذا السلوك، يتم عرض وحدات القياس في نتائج البحث ووحدات تجميع المنتجات.

> [!IMPORTANT]
> تتوفر إعدادات عرض وحدة القياس اعتبارًا من إصدار Commerce رقم 10.0.19. إذا كنت تقوم بالتحديث من إصدار قديم من Commerce، فيجب عليك تحديث ملف appsettings.json يدويًا. للاطلاع على التعليمات، راجع [تحديثات مكتبة الوحدات وSDK](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="modules-that-use-unit-of-measure-settings"></a>الوحدات التي تستخدم إعدادات وحدة القياس

تشمل الوحدات التي تستخدم إعدادات وحدة القياس صندوق الشراء، وقائمة الرغبات، والعربة، وأيقونة عربة التسوق، وحاوية نتائج البحث، ومجموعة المنتجات، والسداد، ووحدات تفاصيل الطلب.

في المثال الموضح في الرسم التوضيحي التالي، تعرض صفحة تفاصيل المنتج (PDP) وحدة القياس (**ea**) لمنتج.

![مثال على PDP يعرض وحدة القياس.](./media/Productunit-PDP.png)

في المثال الموضح في الرسم التوضيحي التالي، تعرض وحدة تجميع المنتج وحدة القياس (**ea**) للمنتج.

![مثال على وحدة تجميع المنتج التي تعرض وحدة القياس.](./media/Productunit-productcollection.png)

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على مكتبة الوحدات](starter-kit-overview.md)

[وحدة عربة التسوق](add-cart-module.md)

[الوحدة النمطية لصندوق الشراء](add-buy-box.md)

[الصفحات والوحدات النمطية لإدارة الحسابات](account-management.md)

[تحديثات SDK ومكتبة الوحدات](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
