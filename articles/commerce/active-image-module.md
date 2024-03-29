---
title: وحدة الصور النشطة
description: يتناول هذا المقال الوحدات النمطية للصورة النشطة ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: fdcd54adc98c7bc52ab6ff1ef7d5d03616aadfc3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267607"
---
# <a name="active-image-module"></a>وحدة الصور النشطة

[!include [banner](includes/banner.md)]

يتناول هذا المقال الوحدات النمطية للصورة النشطة ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.

يمكن استخدام الوحدة النمطية للصورة النشطة لتضمين علامات المنتج في صورة ما. يمكن لمستخدمي موقع التجارة الإلكترونية التحليق بالماوس فوق العلامات لمعاينة المنتجات التي تظهر في الصورة. تظهر المعاينات في الإطارات المنبثقة. بتحديد أحد الإطارات المنبثقة للمعاينة، يمكن للمستخدمين الانتقال مباشرة إلى صفحة تفاصيل المنتج (PDP) للمنتج المقابل.

يتم تعريف العلامات باستخدام إحداثيات س و ص في الصورة. يجب أن يتم تكوين كل نقطة مميزة بمعرف المنتج للمنتج المعروض في الصورة.

يبين الرسم التوضيحي التالي مثالاً للنافذة المنبثقة للمعاينة على صورة رئيسية في الصفحة الرئيسية لـ Adventure Works.

![مثال لمعاينة الإطار المنبثق في الوحدة النمطية للصورة النشطة](./media/Active_image.PNG)

> [!IMPORTANT]
> - تتوفر الوحدة النمطية للصورة النشطة اعتبارا من إصدار 10.0.20 من Dynamics 365 Commerce.
> - يتم عرض وحدة الصورة النشطة بنسق Adventure Works.

## <a name="active-image-module-properties"></a>خصائص وحدة الصور النشطة

| اسم الخاصية      | القيم | الوصف |
|--------------------|--------|-------------|
| صورة              | ملف الصورة | يمكن استخدام صورة لعرض أحد المنتجات أو أكثر. يمكن تحميل الصورة إلى مكتبة الوسائط في منشئ موقع Commerce، أو يمكن استخدام صورة موجودة. |
| العرض              | عدد البكسلات | تحدد هذه الخاصية عرض الصورة. يتم حساب الإحداثيات النشطة استناداً إلى عرض الصورة.|
| الإحداثيات النشطة | إحداثيات س و ص، ورقم معرف المنتج | يتالف كل صفيف صورة نشطة من إحداثيات س وص، ورقم معرف المنتج.|
| العنوان‬            | نص العنوان وعلامة العنوان (**H1**, **H2**, **H3**, **H4**, **H5**, أو **H6**) | وبشكل افتراضي، يتم استخدام علامة العنوان **H2** مع العنوان، ولكن يُمكن تغيير العلامة لتتوافق مع متطلبات الوصول. |
| فقرة          | نص الفقرة | تدعم الوحدة نص الفقرة في تنسيق نصي منسق. يتم دعم بعض إمكانيات النص المنسق الأساسية، مثل الارتباطات التشعبية والنص الغامق المُسطر والمائل. يمكن تجاوز بعض هذه القدرات بواسطة سمة الصفحة التي يتم تطبيقها على الوحدة النمطية. |
| الارتباط               | ارتباط النص وعنوان URL للارتباط والتسمية الخاصة بتطبيقات الإنترنت الغنية القابلة للوصول (ARIA) ومحدد **فتح الارتباط في علامة تبويب جديدة** | تدعم الوحدة النمطية واحد أو أكثر من ارتباطات "استدعاء إجراء". إذا تمت إضافة ارتباط، فمن ثم يلزم وجود نص الارتباط وعنوان URL وتسمية ARIA. يجب أن تكون تسميات ARIA وصفية، لتلبية متطلبات إمكانية الوصول. يمكن تكوين الارتباطات بحيث يتم فتحها في علامة تبويب جديدة. |
| نص فرعي           | العنوان والنص والارتباطات | يمكن إضافة سياق إضافي للصورة، مثل اسم الكاتب أو المصمم، أو الارتباطات بالمدونات الشخصية.|
| نسق النص         | **فاتح** أو **داكن** | تتيح هذه الخاصية للمستخدم تعيين النص إلى فاتح أو داكن، استنادا إلى صورة الخلفية. وهي متوفرة كملحق للنسق في نسق Adventure Works. |

## <a name="add-an-active-image-module-to-a-new-page"></a>إضافة الوحدة النمطية لصورة نشطة إلى صفحة جديدة

لإضافة الوحدة النمطية لصورة نشطة إلى صفحة جديدة وتعيين الخصائص المطلوبة، اتبع الخطوات التالية.

1. انتقل إلى **القوالب**، وافتح قالب التسويق للصفحة الرئيسية للموقع الخاص بك (أو قم بإنشاء قالب تسويق جديد).
1. في الفتحة **الرئيسية‏‎** للصفحة الافتراضية، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.
1. في مربع الحوار **تحديد وحدات**، حدد وحدة **الصورة النشطة**، ثم حدد **موافق**.
1. حدد **حفظ**، وحدد **إنهاء التحرير** لإيداع القالب، ثم حدد **نشر** لنشره.
1. انتقل إلى **الصفحات**، وافتح الصفحة الرئيسية للموقع (أو قم بإنشاء صفحة رئيسية جديدة باستخدام قالب التسويق).
1. في الفتحة **الرئيسية** في الصفحة الافتراضية، حدد زر علامة الحذف (**...**) ، ثم حدد **إضافة وحدة نمطية**.
1. في مربع الحوار **تحديد وحدات**، حدد وحدة **الصورة النشطة**، ثم حدد **موافق**.
1. في جزء الخصائص الخاص بالوحدة النمطية للصورة النشطة، قم بإضافة صورة، وقم بتعيين عرض اللوحة القماشية إلى حجم الصورة.
1. قم بتعيين الإحداثيات س وص، وأضف رقم معرف المنتج المناسب.
1. قم بإضافة وتكوين وحدات الصورة النشطة حسب الحاجة.
1. حدد **حفظ**، ثم حدد **معاينة** لمعاينة الصفحة.
1. حدد **إنهاء التحرير** لإيداع القالب، ثم حدد **نشر** لنشره.

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على مكتبة الوحدات](starter-kit-overview.md)

[نسق Adventure Works](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
