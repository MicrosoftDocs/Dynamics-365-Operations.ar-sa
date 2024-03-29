---
title: إنشاء متغيرات للمنتجات الهندسية
description: يصف هذا المقال كيفية إنشاء متغيرات للمنتجات الهندسية
author: t-benebo
ms.date: 06/08/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 08feb66dedfa79f5a21a7723a22f3bef883431e6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870742"
---
# <a name="generate-variants-for-engineering-products"></a>إنشاء متغيرات للمنتجات الهندسية

[!include [banner](../includes/banner.md)]

يصف هذا المقال كيفية إنشاء متغيرات للمنتجات الهندسية.

## <a name="turn-variant-generation-for-engineering-products-on-or-off"></a>تشغيل ميزة إنشاء متغيرات للمنتجات الهندسية‬ أو إيقاف تشغيلها

تتطلب الوظيفة الموضحة في هذا المقال تشغيل الميزتين *إدارة التغييرات الهندسية* و *إنشاء متغيرات للمنتجات الهندسية‬‬* في النظام. للحصول علي تفاصيل حول كيفية تشغيل هذه الميزات أو إيقاف تشغيلها، راجع [نظرة عامة حول إدارة التغييرات الهندسية](product-engineering-overview.md).

## <a name="generate-one-or-more-new-variants-of-an-engineering-product"></a>إنشاء متغير جديد أو أكثر لمنتج هندسي

يمكنك إنشاء متغير جديد أو أكثر من منتج دون نسخ معلومات من منتج موجود. وهذا مفيد عندما تحتاج إلى إنشاء عدة متغيرات للمنتج في نفس الوقت.

يوفر الإجراء التالي مثالا عن كيفية إنشاء العديد من المتغيرات التي تتضمن بعد اللون.

1. افتح صفحة **المنتجات التي تم إصدارها** (على سبيل المثال، انتقل إلى **إدارة التغيير الهندسي\> عام \> المنتجات الصادرة**).
1. في جزء الإجراءات، افتح علامة تبويب **المنتج**، ومن مجموعة **جديد‬**، حدد **منتج هندسي**.
1. يفتح مربع الحوار **منتج جديد**. حدد **الفئة الهندسية** المناسبة.
1. إذا كانت الفئة الهندسية المحددة تتضمن أبعاد متغيرة، فيمكنك تعيين قيم لها الآن. على سبيل المثال، إذا كانت الفئة ذات بعد **لون**، فيمكنك تعيينها إلى *الأزرق*.
1. قم بإعدادات أخرى حسب الحاجة. حدد **موافق** لإنشاء المنتج.
1. يتم إنشاء المنتج ومتغير V-1 الأزرق، ويتم الآن فتح المنتج الجديد.
1. أضف قائمة مكونات الصنف (BOM) والمسار إلى المتغير حسب الحاجة.
1. في جزء الإجراءات، افتح علامة تبويب **المنتج**، ومن مجموعة **أصل المنتج‬**، حدد **أبعاد المنتج**.
1. يتم فتح صفحة **أبعاد المنتج**. تتضمن هذه الصفحة علامة تبويب لكل بعد متوفر. في كل علامة تبويب، أضف صفا لكل قيمة ستدعمها لكل بعد ذي صلة. (لهذا المثال، يمكنك إضافة صفوف على علامة تبويب **اللون** لـ *الأبيض* و *الأصفر* و *الأخضر*).
1. أغلق الصفحة، ثم حدد **متغيرات المنتجات التي تم إصدارها**. لاحظ ظهور المتغير الأول الذي قمت بإنشائه (الأزرق V-1).
1. في جزء "الإجراءات"، على علامة تبويب **متغير المنتج**، حدد **اقتراحات المتغيرات**.
1. في مربع الحوار **اقتراحات المتغيرات**، اتبع إحدى هذه الخطوات:

    - في أعلى مربع الحوار، يوجد قسم لكل بعد متاح. بالنسبة لكل بعد، حدد خانة الاختيار لكل قيمة تريد إنشاء اقتراح متغير لها، ثم حدد **اقتراح** في شريط الأدوات. تتم إضافة الاقتراحات ذات الصلة إلى قسم **المتغيرات المقترحة**.
    - حدد **اقتراح الكل** في شريط الأدوات لإنشاء اقتراحات متغيرات لكافة مجموعات قيم الأبعاد المتوفرة. تتم إضافة الاقتراحات إلى قسم **المتغيرات المقترحة**.

1. في قسم **المتغيرات المقترحة**، حدد خانة الاختيار لكل متغير تريد إنشاؤه. ثم حدد **إنشاء** لإنشاء وإصدار المتغيرات المحددة للشركة الهندسية. تنطبق الشروط التالية:

    - لن يكون لأي من المتغيرات التي تم إنشاؤها قائمة مكونات صنف أو مسار.
    - سيتم الافتراضي سمات هذه المتغيرات من الفئة الهندسية ولن يتم نسخ من البديل السابق.

## <a name="generate-a-variant-as-a-copy-of-another-product-variant"></a>إنشاء متغير ك نسخة من متغير منتج آخر

يمكنك إنشاء متغير لمنتج استنادا إلى متغير منتج آخر. يتم نسخ شجرة المواد (BOM) والمسار من متغير المنتج المصدر إلى المتغير الجديد. قد يكون هذا مفيدا لمنتجات التصنيع المنفصلة حيث يمكن أن يكون من المفيد إنشاء شجرة المواد استنادا إلى شجرة مواد بداية وتتبع التغييرات من المتغير السابق. للحفاظ على إمكانية التتبع، يسجل النظام الذي تم نسخ المتغير لإنشاء نسخة جديدة.

يوفر الإجراء التالي مثالا عن كيفية إنشاء متغير جديد يتضمن بعد اللون عن طريق إنشاء نسخة من متغير موجود

1. افتح صفحة **المنتجات التي تم إصدارها** (على سبيل المثال، انتقل إلى **إدارة التغيير الهندسي\> عام \> المنتجات الصادرة**).
1. في جزء الإجراءات، افتح علامة تبويب **المنتج**، ومن مجموعة **جديد‬**، حدد **منتج هندسي**.
1. يفتح مربع الحوار **منتج جديد**. حدد **الفئة الهندسية** المناسبة.
1. إذا كانت الفئة الهندسية المحددة تتضمن أبعاد متغيرة، فيمكنك تعيين قيم لها الآن. على سبيل المثال، إذا كانت الفئة ذات بعد **لون**، فيمكنك تعيينها إلى *الأزرق*.)
1. قم بإعدادات أخرى حسب الحاجة. حدد **موافق** لإنشاء المنتج.
1. يتم إنشاء المنتج ومتغير V-1 الأزرق، ويتم الآن فتح المنتج الجديد.
1. أضف قائمة مكونات الصنف (BOM) والمسار إلى المتغير حسب الحاجة.
1. أضف سمات إلى متغير المنتج حسب الحاجة.
1. أضف متغير المنتج الأزرق V-1 إلى أمر تغيير هندسي.
1. قم بتعيين **التأثير** إلى *متغير جديد*.
1. حدد قيمة اللون الجديد (على سبيل المثال، *الأبيض*). لاحظ أنه سيتم تطبيق الشروط التالية: 
    - يحتوي المتغير الجديد على قائمة مكونات صنف ومسار تم نسخها من المتغير السابق.
    - يحتوي المتغير الجديد على السمات المنسوخة من المتغير السابق.
1. الموافقة على أمر التغيير.
1. معالجة أمر التغيير. بعد معالجة الأمر، سيتم إنشاء متغير V-1 الجديد وإصداره للشركة الهندسية.
