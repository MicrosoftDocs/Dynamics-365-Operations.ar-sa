---
title: وحدة مشغل الفيديو
description: يتناول هذا المقال الوحدات النمطية لمشغل الفيديو ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 919446981f7439d61b01deb57b206cd457eed919
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269284"
---
# <a name="video-player-module"></a>وحدة مشغل الفيديو

[!include [banner](includes/banner.md)]

يتناول هذا المقال الوحدات النمطية لمشغل الفيديو ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.

تُستخدم الوحدة النمطية لمشغل الفيديو لدعم تشغيل الفيديو. ويمكن اضافتها إلى أي صفحة، شريطة أن يتم تحميل محتوى الفيديو وأن يكون متوفرًا في نظام إدارة المحتوى (CMS). تدعم الوحدة النمطية لمشغل الفيديو نوع الوسائط mp4.

## <a name="video-player-module"></a>وحدة نمطية لمشغل الفيديو

يمكن استخدام الوحدة النمطية لمشغل الفيديو لإظهار مقاطع الفيديو على موقع التجارة الإلكترونية. وهي تدعم كافة إمكانيات التشغيل، مثل وضع التشغيل، والإيقاف المؤقت، ووضع الحجم الكامل، وأوصاف الصوت والتسميات التوضيحية المغلقة. كما تدعم الوحدة النمطية لمشغل الفيديو تخصيص التسميات التوضيحية المغلقة لتلبية معايير إمكانية الوصول الخاصة بـ Microsoft. على سبيل المثال، يمكنك تخصيص حجم الخط ولون الخلفية.

تدعم وحدة مشغل الفيديو المسارات الصوتية الثانوية أيضًا. عند تحميل مقطع فيديو إلى CMS، يمكن أيضًا تحميل مقطع صوتي ثانوي. يمكن للوحدة النمطية لمشغل الفيديو تشغيل مسار الصوت الثانوي إذا قام المستخدم بتحديده.

### <a name="examples-of-video-player-modules-in-e-commerce"></a>أمثله للوحدات النمطية لمشغل الفيديو في التجارة الإلكترونية

- مقاطع فيديو إرشادية على صفحات تفاصيل المنتج أو صفحات التسويق
- مقاطع الفيديو الترويجية أو مقاطع الفيديو الخاصة بالسياسات في أي صفحة تسويق
- تسويق مقاطع الفيديو التي تبرز ميزات المنتج في صفحات تفاصيل المنتج أو صفحات التسويق

تعرض الصورة التالية مثالاُ عن وحدة مشغل الفيديو في صفحة رئيسية.

![مثال عن وحدة مشغل الفيديو.](./media/ecommerce-videoplayer.PNG)

### <a name="video-player-module-properties"></a>خصائص الوحدة النمطية لمشغل الفيديو

| اسم الخاصية         | قيمة                               | الوصف |
|-----------------------|-------------------------------------|-------------|
| العنوان‬               | نص العنوان وعلامة العنوان (**H1**, **H2**, **H3**, **H4**, **H5**, أو **H6**) | وبشكل افتراضي، يتم استخدام علامة العنوان **H2** مع العنوان، ولكن يُمكن تغيير العلامة لتتوافق مع متطلبات الوصول. |
| نص منسق             | نص الفقرة | تدعم الوحدة نص الفقرة في تنسيق نصي منسق. يتم دعم بعض إمكانيات النص المنسق الأساسية، مثل الارتباطات التشعبية والنص الغامق المُسطر والمائل. يمكن تجاوز بعض هذه القدرات بواسطة سمة الصفحة التي يتم تطبيقها على الوحدة النمطية. |
| الارتباط                  | ارتباط النص وعنوان URL للارتباط والتسمية الخاصة بتطبيقات الإنترنت الغنية القابلة للوصول (ARIA) ومحدد **فتح الارتباط في علامة تبويب جديدة** | تدعم الوحدة النمطية واحد أو أكثر من ارتباطات "استدعاء إجراء". إذا تمت إضافة ارتباط، فمن ثم يلزم وجود نص الارتباط وعنوان URL وتسمية ARIA. يجب أن تكون تسميات ARIA وصفية، لتلبية متطلبات إمكانية الوصول. يمكن تكوين الارتباطات بحيث يتم فتحها في علامة تبويب جديدة. |
| نص فرعي              | العنوان أو النص أو الارتباطات | يمكن إضافة سياق إضافي لوحدة مشغل الفيديو، مثل اسم الكاتب أو المصمم، أو الارتباطات بالمدونات الشخصية. |
| تشغيل تلقائي             | **صحيح** أم **خطأ**               | عند تعيين القيمة على **صحيح**، يتم تشغيل الفيديو تلقائيًا. |
| كتم الصوت                  | **صحيح** أم **خطأ**               | عند تعيين القيمة إلى **صحيح**، يتم كتم الصوت. بالنسبة لهذا المشغل، تكون القيمة الافتراضية هي **خطأ**. في المستعرض Chrome، يتم كتم صوت مقاطع الفيديو تلقائيًا، ويتم تشغيل الصوت فقط إذا قام المستخدم بتشغيل الفيديو يدويًا. |
| حلقة                  | **صحيح** أم **خطأ**               | عند تعيين القيمة إلى **صحيح**، يتكرر الفيديو في حلقة. |
| الوسائط                 | مسار ملف الفيديو واسمه. | ملف الفيديو الذي يتم تشغيله في مشغل الفيديو. |
| تشغيل وضع ‏‫ملء الشاشة‬       | **صحيح** أم **خطأ**               | عند تعيين القيمة إلى **صحيح**، يتم تشغيل الفيديو في وضع ‏‫ملء الشاشة‬. |
| ‏‫تشغيل/إيقاف مؤقت‬ المشغل    | **صحيح** أم **خطأ**               | عند تعيين القيمة إلى **صحيح**، يظهر الزر "تشغيل/إيقاف مؤقت" في الفيديو. |
| عناصر تحكم مشغل الفيديو | **صحيح** أم **خطأ**               | عند تعيين القيمة إلى **صحيح**، تظهر كافة عناصر تحكم مشغل الفيديو. تتضمن عناصر التحكم هذه أزرار التشغيل والإيقاف المؤقت ومؤشر التقدم وخيارات التسميات التوضيحية المغلقة. |
| إخفاء صورة الملصق     | **صحيح** أم **خطأ**               | يمكن أن يكون للفيديو صورة أولية. عند تعيين قيمه هذه الخاصية إلى **صحيح**، يتم إخفاء الصورة الأولية. |
| مستوى القناع            | الرقم من **0** إلى **100** | القناع المطبق على الفيديو للتنميط. |

> [!IMPORTANT]
> تتوفر خواص **العنوان**، و **نص منسق** و **ارتباط** و **نص فرعي** اعتبارًا من الإصدار 10.0.20 من Dynamics 365 Commerce.

## <a name="add-a-video-player-module-to-a-page"></a>إضافة الوحدة النمطية لمشغل الفيديو إلى صفحة

> [!NOTE] 
> قبل إنشاء الوحدة النمطية لمشغل الفيديو، يجب أولاً تحميل فيديو إلى مكتبة الوسائط.

لإضافة الوحدة النمطية لمشغل الفيديو إلى صفحة جديدة وتعيين الخصائص المطلوبة، اتبع الخطوات التالية.

1. انتقل إلى **القوالب**، ثم حدد **جديد** لإنشاء قالب جديد.
1. في مربع الحوار **قالب جديد**، تحت **اسم القالب**، أدخل **قالب مشغل الفيديو**، ثم حدد **موافق**.
1. في فتحة **النص الأساسي‬‬‏‫**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.
1. في مربع الحوار **تحديد وحدات**، حدد وحدة **الصفحة الافتراضية**، ثم حدد **موافق**.
1. في الفتحة **الرئيسية‏‎** في وحدة **الصفحة الافتراضية**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.
1. في مربع الحوار **تحديد وحدات**، حدد وحدة **الحاوية‬‏‎**، ثم حدد **موافق**.
1. في فتحة **الحاوية‬‬‏‫**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.
1. في مربع الحوار **تحديد وحدات**، حدد وحدة **مشغل الفيديو‬**، ثم حدد **موافق**.
1. حدد **حفظ**، وحدد **إنهاء التحرير** لإيداع القالب، ثم حدد **نشر** لنشره. 
1. انتقل إلى **الصفحات**، ثم حدد **جديد** لإنشاء صفحة جديدة.
1. في مربع الحوار **إنشاء صفحة جديدة**، تحت **اسم الصفحة**، أدخل **صفحة مشغل الفيديو**، ثم حدد **التالي**.
1. ضمن **اختيار قالب**، حدد **قالب مشغل الفيديو** الذي أنشأته، ثم حدد **التالي**.
1. ضمن **اختيار تخطيط**، حدد تخطيط صفحة (على سبيل المثال، **تخطيط مرن**)، ثم حدد **التالي**.
1. ضمن **مراجعة وإنهاء**، راجع تكوين الصفحة. إذا احتجت إلى تحرير معلومات الصفحة، فحدد **السابق**. إذا كانت معلومات الصفحة صحيحة، فحدد **إنشاء صفحة**.
1. في الفتحة **الرئيسية** للصفحة الجديدة، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة‬‏‫**.
1. في مربع الحوار **تحديد وحدات**، حدد وحدة **الحاوية‬‏‎**، ثم حدد **موافق**.
1. في فتحة **الحاوية‬‬‏‫**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.
1. في مربع الحوار **تحديد وحدات**، حدد وحدة **مشغل الفيديو‬**، ثم حدد **موافق**.
1. في جزء الخصائص لوحدة مشغل الفيديو، حدد **إضافة فيديو**.
1. في مربع حوار **منتقي‏‎ الوسائط**، حدد مقطع فيديو، ثم حدد **تحميل عنصر وسائط جديد**.
1. في "مستكشف الملفات"، حدد ملف فيديو، ثم حدد **فتح**.
1. في مربع الحوار **تحميل عنصر الوسائط**، أدخل عنوانًا ومعلومات أخرى كما تقتضي الحاجة، ثم حدد **موافق**.
1. في مربع حوار **منتقي الوسائط**، حدد **إغلاق**.
1. حدد **حفظ**، ثم حدد **معاينة** لمعاينة الصفحة. من المفترض أن ترى وحدة الفيديو في الصفحة. يمكنك تغيير الإعدادات الإضافية لتخصيص سلوك الوحدة النمطية.
1. حدد **إنهاء التحرير** لإيداع الصفحة، ثم حدد **نشر** لنشرها. 

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة حول مكتبة الوحدات النمطية](starter-kit-overview.md)

[وحدة الشعار الترويجي](add-alert.md)

[وحدة دوارة](add-carousel.md)

[وحدة كتلة النص](add-content-rich-block.md)

[وحدة كتلة المحتوى](add-hero-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
