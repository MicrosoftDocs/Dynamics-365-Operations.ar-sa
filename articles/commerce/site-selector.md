---
title: الوحدة النمطية لمحدد الموقع
description: يتناول هذا الموضوع وحدة محدّد الموقع ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.openlocfilehash: e24590d4a8f172809704aab0d761f6db0fb0e11b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234331"
---
# <a name="site-selector-module"></a>الوحدة النمطية لمحدد الموقع

[!include [banner](includes/banner.md)]

يتناول هذا الموضوع وحدة محدّد الموقع ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.

عندما يكون للشركة مواقع مختلفه عبر الأسواق والمناطق والإعدادات المحلية، فان مستخدمي الموقع يحتاجون إلى طريقة سهلة للتبديل بين المواقع وتحديد موقع التسوق المفضل لديهم. لاحتواء هذا السيناريو ، تسمح الوحدة النمطية لمحدد الموقع للمستخدمين بالاستعراض عبر مواقع متعددة.

يجب تكوين الوحدة النمطية لمحدد الموقع بقائمة المواقع (الأسواق أو المناطق أو الإعدادات المحلية) التي يمكن لمستخدمي الموقع استعراضها.

> [!NOTE]
> تتوفر الوحدة النمطية لمحدد الموقع في Dynamics 365 Commerce الإصدار 10.0.14.

يبين الرسم التوضيحي التالي مثالاً للوحدة النمطية لمحدد الموقع والتي تكون مميزه في رأس صفحة الموقع.

![مثال لوحدة نمطية لمحدد موقع في رأس صفحة موقع](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a>خصائص وحدة محدِّد الموقع

| اسم الخاصية | قيمة                 | الوصف |
|---------------|-----------------------|-------------|
| العنوان       | النص                  | عنوان الوحدة النمطية. |
| خيارات المواقع  | الاسم، الصورة ، عنوان URL      | تحدد هذه الخاصية اسمًا وارتباطا بالصفحة الرئيسية للموقع وصورة اختياريه لعرضها لكل موقع يتم تضمينه في الوحدة النمطية. ويمكن أن تكون الصورة علامة أو تمثيلا لأحد الأسواق أو المنطقة أو الإعدادات المحلية. |

## <a name="add-a-site-selector-module-to-a-page"></a>إضافة وحدة محدِّد موقع إلى صفحة

يمكن إضافة الوحدة النمطية لمحدد الموقع إلى [الوحدة النمطية للرؤوس](author-header-module.md) ضمن فتحة "محدد الموقع". بعد إضافتها، يمكنك تحديد عنوان الوحدة النمطية وخيارات الموقع.

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على مكتبة الوحدات](starter-kit-overview.md)

[الوحدة النمطية للرؤوس](author-header-module.md)

[الوحدة النمطية لمسار التنقل](add-breadcrumb.md)

[الوحدة النمطية لقائمة التنقل](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]