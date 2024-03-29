---
title: وحدة دوارة
description: يتناول هذا المقال الوحدات الدوارة ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
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
ms.openlocfilehash: 8bf9f7294dfbb4e16814dbdfb27bf646fcb5f4b1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275817"
---
# <a name="carousel-module"></a>وحدة دوارة

[!include [banner](includes/banner.md)]

يتناول هذا المقال الوحدات الدوارة ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.

تُستخدم الوحدة النمطية الدوارة لوضع أصناف ترويجية متعددة (بما في ذلك الصور المنسقة) في شعار دوار يُمكن للعملاء استعراضه. على سبيل المثال، يُمكن لبائع التجزئة استخدام الوحدة النمطية الدوارة في الصفحة الرئيسية لإظهار منتجات جديدة متعددة أو عروض.

يُمكنك إضافة وحدات كتلة المحتوى داخل الوحدة النمطية الدوارة. ثم تُحدد خصائص الوحدة النمطية الدوارة كيفية عرض هذه الوحدات النمطية.

## <a name="examples-of-carousel-modules-in-e-commerce"></a>أمثلة على الوحدات النمطية الدوارة في التجارة الإلكترونية

- يُمكن استخدام الوحدة النمطية الدوارة تحتوي على وحدات نمطية ترويجية متعددة داخلها على الصفحة الرئيسية.
- يُمكن استخدام الوحدة النمطية الدوارة تحتوي على وحدات نمطية ترويجية متعددة داخلها على صفحة تفاصيل المنتج.
- ويُمكن استخدام الوحدة الدوارة على أي صفحة تسويق لترقية العروض أو المنتجات المُتعدة.

تعرض الصورة التالية مثالاً عن وحدة نمطية دوارة‬ مستخدمة في الصفحة الرئيسية. تحتوي الوحدة النمطية الدوارة‬ على عناصر كتل محتويات متعددة.

![مثال عن وحدة نمطية دوارة.](./media/Hero.PNG)

## <a name="carousel-module-properties"></a>خصائص الوحدة النمطية الدوارة

| اسم الخاصية             | قيمة                 | الوصف |
|---------------------------|-----------------------|-------------|
| تشغيل تلقائي                  | **صحيح** أم **خطأ** | إذا تم تعيين القيمة إلى **صحيح**، يُحدث انتقال بين العناصر داخل الوحدة النمطية الدوارة تلقائيًا. إذا تم تعيين القيمة إلى **خطأ**، فلن يُحدث أي انتقال ما لم يستخدم العميل لوحة المفاتيح أو الماوس للانتقال من عنصر إلى العنصر التالي. |
| فاصل المراحل الانتقالية للشرائح | القيمة بالثواني    | الفاصل الزمني للانتقال بين العناصر. |
| نوع الحركة           | **شريحة** أو **Fade** | تأثير المرحلة الانتقالية بين العناصر. |
| إخفاء الذراع الدوّار     | **صحيح** أم **خطأ** | إذا تم تعيين القيمة إلى **صواب**، فسيتم إخفاء الذراع الدوّار ومؤشر التسلسل. |
| السماح باستبعاد الوحدة الدوّارة    | **صحيح** أم **خطأ** | إذا تم تعيين القيمة إلى **صحيح**، فبإمكان العملاء استبعاد الوحدة الدوّارة. |

## <a name="add-a-carousel-module-to-a-page"></a>إضافة الوحدة النمطية الدوارة إلى صفحة

لإضافة الوحدة النمطية الدوارة إلى صفحة جديدة وتعيين الخصائص المطلوبة، اتبع الخطوات التالية.

1. انتقل إلى **القوالب**، ثم حدد **جديد** لإنشاء قالب جديد.
1. في مربع الحوار **قالب جديد**، تحت **اسم القالب**، أدخل **قالب دوار**، ثم حدد **موافق**.
1. في فتحة **النص الأساسي**، أضف الوحدة النمطية **الصفحة الافتراضية** .
1. حدد **إنهاء التحرير** لإيداع القالب، ثم حدد **نشر** لنشره.  
1. استخدم القالب الدوار الذي أنشأته للتو لإنشاء صفحة تسمى **صفحة دواره**.
1. في الفتحة **الرئيسية** للصفحة الجديدة، قم بإضافة وحدة الحاوية. 
1. في الجزء إلى اليسار، قم بتعيين قيمة **العرض** إلى **ملء الشاشة‬‏‫**.
1. ضمن **المخطط التفصيلي للصفحة**، أضف وحدة دوّارة إلى وحدة الحاوية.
1. أضف الوحدة النمطية لكتلة المحتوى إلى الوحدة النمطية الدوارة. قم بتعيين خصائص الوحدة النمطية لكتله المحتوى عن طريق توفير **عنوان** و **ارتباط** و **تخطيط** وخصائص أخرى.
1. أضف وحدة نمطية أخرى لكتلة المحتوى وتكوينها.
1. قم بتعيين خصائص إضافية للوحدة النمطية الدوّارة كما هو مطلوب.
1. حدد **حفظ**، ثم حدد **معاينة** لمعاينة الصفحة. يجب أن تُظهر الصفحة الوحدة النمطية الدوارة تحتوي على وحدتين نمطيتين بداخلها (الوحدة النمطية لجزء رئيسي والوحدة النمطية لميزة). يُمكنك تغيير الخصائص الإضافية للوحدات النمطية الدوارة والجزء الرئيسي والميزة لتحقيق التأثير المطلوب.
1. حدد **إنهاء التحرير** لإيداع الصفحة، ثم حدد **نشر** لنشرها.

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة حول مكتبة الوحدات النمطية](starter-kit-overview.md)

[وحدة الشعار الترويجي](add-alert.md)

[وحدة كتلة النص](add-content-rich-block.md)

[وحدة كتلة المحتوى](add-hero-module.md)

[وحدة نمطية لمشغل الفيديو](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
