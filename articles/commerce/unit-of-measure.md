---
title: تطبيق إعدادات وحدة القياس
description: يغطي هذا المقال إعدادات وحدة القياس ويصف كيفية تطبيقها في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 7a7be6395a8bfce38e84f850bd792f358941c18a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275531"
---
# <a name="apply-unit-of-measure-settings"></a>تطبيق إعدادات وحدة القياس

[!include [banner](includes/banner.md)]

يغطي هذا المقال إعدادات وحدة القياس ويصف كيفية تطبيقها في Microsoft Dynamics 365 Commerce.

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
