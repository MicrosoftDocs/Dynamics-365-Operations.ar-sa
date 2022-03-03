---
title: وحدة منتقي الموقع
description: يتناول هذا الموضوع وحدة منتقي الموقع ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 02/11/2022
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 381163fdd6180a76def2e1bfb733f597b611c517
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109696"
---
# <a name="site-picker-module"></a>وحدة منتقي الموقع

[!include [banner](includes/banner.md)]

يتناول هذا الموضوع وحدة منتقي الموقع ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.

عندما يكون للشركة مواقع مختلفه عبر الأسواق والمناطق والإعدادات المحلية، فان مستخدمي الموقع يحتاجون إلى طريقة سهلة للتبديل بين المواقع وتحديد موقع التسوق المفضل لديهم. لاحتواء هذا السيناريو ، تسمح وحدة منتقي الموقع للمستخدمين بالاستعراض عبر مواقع متعددة.

يجب تكوين وحدة منتقي الموقع بقائمة المواقع (الأسواق أو المناطق أو الإعدادات المحلية) التي يمكن لمستخدمي الموقع استعراضها.

> [!NOTE]
> تتوفر وحدة منتقي الموقع في Dynamics 365 Commerce الإصدار 10.0.14.

يبين الرسم التوضيحي التالي مثالاً عن وحدة منتقي الموقع المضمنة في رأس صفحة الموقع.

![مثال عن وحدة منتقي الموقع في رأس صفحة موقع.](./media/ecommerce-sitepicker.PNG)

## <a name="site-picker-module-properties"></a>خصائص وحدة منتقي الموقع

| اسم الخاصية | قيمة                 | ‏‏الوصف‬ |
|---------------|-----------------------|-------------|
| العنوان‬       | النص                  | عنوان الوحدة النمطية. |
| خيارات المواقع  | الاسم، الصورة ، عنوان URL      | تحدد هذه الخاصية اسمًا وارتباطا بالصفحة الرئيسية للموقع وصورة اختياريه لعرضها لكل موقع يتم تضمينه في الوحدة النمطية. ويمكن أن تكون الصورة علامة أو تمثيلا لأحد الأسواق أو المنطقة أو الإعدادات المحلية. |

## <a name="add-a-site-picker-module-to-a-page"></a>إضافة وحدة منتقي الموقع إلى صفحة

يمكن إضافة وحدة منتقي الموقع إلى فتحة **منتقي الموقع** في وحدة [الرأس](author-header-module.md). بعد إضافة وحدة منتقي الموقع، يمكنك تحديد عنوان الوحدة وخيارات الموقع. بشكل عام، يتم تضمين وحدة الرأس في جزء رأس يمكن مشاركته عبر صفحات التجارة الإلكترونية لأحد المواقع. في المثال التالي ، تمت إضافة وحدة منتقي المواقع إلى فتحة **منتقي الموقع** في وحدة الرأس الموجودة في جزء الرأس الذي يسمى **HeaderContainer**.

![مثال عن وحدة منتقي الموقع في جزء الرأس.](./media/ecommerce-sitepicker-2.png)

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على مكتبة الوحدات](starter-kit-overview.md)

[الوحدة النمطية للرؤوس](author-header-module.md)

[الوحدة النمطية لمسار التنقل](add-breadcrumb.md)

[الوحدة النمطية لقائمة التنقل](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
