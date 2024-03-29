---
title: تحميل صور
description: يصف هذا المقال كيفية تحميل الصور في منشئ موقع Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: d937e8c0e00ce28b0e4a4c2feab3ac1c8f075916
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283369"
---
# <a name="upload-images"></a>تحميل صور

[!include [banner](includes/banner.md)]

يصف هذا المقال كيفية تحميل الصور في منشئ موقع Microsoft Dynamics 365 Commerce.

تسمح لك مكتبة وسائط منشئ موقع Commerce بتحميل الصور، أو بشكل فردي أو بشكل مجمع باستخدام المجلدات. يجب أن تقوم دائمًا بتحميل إصدار الصورة الأعلى دقة وجودة، لأن مكون تغيير حجم الصورة سيقوم تلقائيًا بتحسين الصورة لمنافذ عرض مختلفة ونقاط التوقف الخاصة بها.

### <a name="image-information-specified-during-upload"></a>معلومات الصورة التي يتم تحديدها أثناء التحميل

عند تحميل صورة، يمكن تحديد المعلومات التالية.

- **العنوان والنص البديل والوصف والكلمات الأساسية**: بيانات تعريف الصورة أو الصور. العنوان والنص البديل هما قيم مطلوبة.
- **تحديد فئة**:
    - **بلا**: يُستخدم هذا الخيار لصورة أو صور تتعلق برواية قصة تجارة إلكترونية.
    - **المنتج، الفئة، العميل، الموظف، الكتالوج**: تُستخدم لصورة أو صور في القناة متعددة الاتجاهات في Dynamics 365 Commerce.
- **نشر الأصول بعد التحميل**: عند تحديد خانة الاختيار هذه، يتم نشر الصورة أو الصور مباشرةً بعد التحميل.

> [!NOTE]
> - يتم أيضًا تمييز صور الأصول ذات فئة معينة لها بشكل تلقائي بواسطة الفئة ككلمة أساسية للمساعدة في البحث عن أصول خاصة بفئة معينة.
> - تقوم صفحات تفاصيل المنتج بإنشاء **النص البديل** باستخدام اسم المنتج بشكل ديناميكي، لذلك لن يكون لتغيير **النص البديل** لصورة منتج أي تاثير على الصورة المعروضة.

### <a name="naming-conventions-for-omni-channel-images"></a>اصطلاحات التسمية لصور القناة متعددة الاتجاهات 

إذا قمت بتكوين مكتبة الوسائط كخلفية صورة قناة متعددة الاتجاهات، يمكنك استخدام فئات الصور للإشارة إلى الفئة التي تنتمي اليها الصورة التي تم تحميلها. هناك أيضًا اصطلاح تسمية يجب اتباعه للتأكد من استرداد الصور بشكل صحيح بواسطة القنوات الأخرى، مثل نقطة البيع (POS).

يختلف اصطلاح التسمية الافتراضي بالاستناد إلى الفئة:
- يجب تسمية صور الكتالوجات "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"
- يجب تسمية صور الفئات "**/Categories/\{CategoryName\}.png**"
- يجب تسمية صور العملاء "**/Customers/\{CustomerNumber\}.jpg**"
- يجب تسمية صور الموظفين "**/Workers/\{WorkerNumber\}.jpg**"
- يجب تسمية صور المنتجات باسم "**/Products/\{ProductNumber\}\_000_001.png**"
    - يمثل 001 تسلسل الصورة ويمكنها أن يكون 001 أو 002 أو 003 أو 004 أو 005
- يجب تسمية صور متغيرات المنتجات "**/Products/\{ProductNumber\} \^ \{Style\} \^ \{Size\} \^ \{Color\} \^\_000_001.png**"
    - على سبيل المثال: 93039 \^ &nbsp;\^ 2 \^ Black \^\_000_001.png
- يجب تسمية صور متغيرات المنتجات مع بُعد التكوين باسم "**/Products/\{ProductNumber\} \^ \{Configuration\}\_000_001.png**"
    - على سبيل المثال: 93039 \^ LB8017_000_001.png

> [!NOTE]
> بالنسبة لصور متغيرات المنتج، إذا كانت قيمة البعد فارغة، يجب أن يكون هناك مسافتان بين علامات الإقحام في اسم الملف.

تستخدم الأمثلة أعلاه التكوين الافتراضي. يمكن تكوين حرف الفاصل والأبعاد وقد تختلف التسمية الدقيقة المطلوبة بين عمليات النشر. تتمثل إحدى طرق تحديد اصطلاح التسمية الدقيق المطلوب في استخدام وحدة تحكم مطور المستعرض لفحص طلبات صور متغير المنتج أثناء تغيير أبعاد المنتج في صفحة تفاصيل المنتج لواجهة المتجر (PDP).

## <a name="upload-an-image"></a>تحميل صورة

لتحميل صورة في منشئ الموقع، اتبع الخطوات التالية.

1. في جزء التنقل الأيسر، حدد **مكتبة الوسائط**.
1. في شريط الأوامر، حدد **تحميل \> تحميل عناصر الوسائط**.
1. في نافذة مستكشف الملفات، انتقل إلى صورة أو أكثر لتحميلها، ثم حدد **فتح**.
1. في مربع الحوار **تحميل عنصر الوسائط**، أدخل العنوان والنص البديل المطلوبين.
1. أدخل وصفًا اختياريًا وكلمات أساسية اختيارية، وحدد فئة إذا أردت ذلك. 
1. إذا أردت نشر الصورة (الصور) مباشرةً بعد التحميل، فحدد خانه الاختيار **نشر عناصر الوسائط بعد التحميل**.
1. حدد **موافق**.

## <a name="upload-a-folder-of-images"></a>تحميل مجلد صور

لإجراء تحميل مجمع لمجلد صور في منشئ الموقع، اتبع الخطوات التالية.

1. في جزء التنقل الأيسر، حدد **مكتبة الوسائط**.
1. في شريط الأوامر، حدد **تحميل \> تحميل مجلد**.
1. في نافذة مستكشف الملفات، انتقل إلى مجلد لتحميله، ثم حدد **فتح**.
1. في مربع الحوار **تحميل عناصر الوسائط**، أدخل كلمات أساسية اختيارية وحدد فئة إذا أردت ذلك. 
1. إذا أردت نشر الصور مباشرةً بعد التحميل، فحدد خانه الاختيار **نشر عناصر الوسائط بعد التحميل**.
1. حدد **موافق**.

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على إدارة الأصول الرقمية](dam-overview.md)

[تحميل فيديو](dam-upload-video.md)

[تحميل الملفات](dam-upload-files.md)

[اقتصاص الصور](dam-crop-images.md)

[تخصيص نقاط تركيز الصورة](dam-custom-focal-point.md)

[تحميل الملفات الثابتة وخدمتها](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
