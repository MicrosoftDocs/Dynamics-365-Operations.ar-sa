---
title: المناصب‬
description: توضح هذه المقالة العناصر التصورية التي يمكن أن يتضمنها منصب ما. كما يوفر أمثلة تظهر كيفية استخدام هذه العناصر في المؤسسة الخاصة بك.
author: twheeloc
ms.date: 06/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPosition, HcmPersonnelManagementWorkspace
audience: Application User
ms.author: twheeloc
ms.reviewer: twheeloc
ms.custom: 269054
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 9c97a96e27188d12b9c5e626613e18d54d6632c0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888719"
---
# <a name="positions"></a>المناصب‬


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

توضح هذه المقالة العناصر التصورية التي يمكن أن يتضمنها منصب ما. كما يوفر أمثلة تظهر كيفية استخدام هذه العناصر في المؤسسة الخاصة بك.

قبل أن تتمكن من إنشاء منصب، يجب إعداد وظيفة. تكون بعض تفاصيل المنصب، مثل منطقة التعويض، وتعيين العامل، ومدة المنصب، وعلاقة التقارير سارية المفعول.

## <a name="general-information"></a>معلومات عامة

عند إنشاء منصب، يجب تحديد وظيفة. سيتم تلقائيًا ملء المعلومات التالية من الوظيفة التي قمت بتحديدها:

- الوصف
- المسمى الوظيفي
- مكافئ الوقت الكامل
- مجموعة الوظائف

يتم استخدام عنوان المنصب للإشارة إلى المسمي الوظيفي للموظف. (لا يتم استخدام المسمى الوظيفي المدرج للموظف.) لذلك، يجب أن تكون عناوين المناصب قياسية بقدر الإمكان.

> [!NOTE]
> لا يمكن تعيين عامل لأحد المناصب في التاريخ الذي يسبق تاريخ التعيين المتاح للتعيين.
>
> تتحكم معلمة في علامة تبويب **المنصب** بصفحة **المعلمات المشتركة للموارد البشرية** في سلوك التعيين الخاص بالعامل. حدد إحدى القيم التالية:
>
> - **دائمًا**– يمكنك تعيين عمال لمناصب جديدة عند إنشاء مناصب.‬ وعند إنشاء المناصب، يتم تعيين التاريخ والوقت **المتوفر للتعيين** في علامة التبويب **عام** من صفحة **المنصب** إلى تاريخ ووقت الإنشاء تلقائيًا.‬
> - **أبدًا**– لا يمكنك تعيين عمال لمناصب جديدة عند إنشاء مناصب. إذا قمت بتحديد هذا الخيار، فيجب فتح صفحة **المنصب** لكل منصب جديد حينما يصبح متوفراً. ثم في علامة التبويب **عام**، أدخل **المتاح للتعين** لتمكين تعيين العامل. إذا قمت بتحديد هذا الخيار، سيتم تعيين تاريخ تعيين العامل علة **أبدا** بشكل افتراضي عند محاولة تعيين العامل.

## <a name="position-duration"></a>مدة المنصب

ويكون كل منصب ساريًا لفترة محددة من الوقت يُشار إليها بالمدة. على سبيل المثال، قد تُتاح المناصب الصيفية للمدة من 1 مايو 2021، حتى 31 أغسطس 2021. تاريخ التنشيط هو التاريخ الذي يكون فيه المنصب نشطًا في النظام. تاريخ التقاعد هو التاريخ الذي يصبح فيه المنصب غير نشط في النظام.

لاحظ أنه لا يمكن أن يكون تاريخ المتاح للتعيين أو تاريخ تعيين العامل قبل تاريخ التنشيط. لا يعتبر المنصب نشطًا حتى يتم الوصول إلى تاريخ التنشيط. بالإضافة إلى ذلك، لا يمكن توسيع أحد تعيينات العامل بعد تاريخ التقاعد للمنصب.

## <a name="reports-to-position"></a>مرؤوس من منصب

المناصب هي عناصر مهمة في المستوى الأدنى للتدرج الهرمي للمؤسسات. وفي صفحة **المنصب**، يمكنك تحديد المنصب الذي يكون المنصب مرؤوسًا منه. وعندما تقوم بتعيين عامل إلى منصب مرؤوس من منصب آخر، يمكنك إنشاء علاقات تقرير بين العمال الذين يتم تعيينهم للمنصبين. على سبيل المثال ، المنصب 000220 مرؤوس من المنصب 000300. تم تعيين نجيب عطية للمنصب "000220"،يتم تعيين سانجاي باتيل للمنصب "000220". بالتالي، يكون نجيب عطية مرؤوسًا لسانجاي باتيل.

> [!TIP]
> يتم استخدام إعداد مرؤوس من منصب في أنحاء النظام لتحديد الشخص الذي سيكون مدير الموظف. في المثال السابق، إذا تم تعيين دور المدير إلى سانجاي باتيل في النظام، سيشاهد نجيب عطية كمرؤوس مباشر في الخدمة الذاتية للمدير. يمكن استخدام علاقة التقارير أيضًا عند إنشاء قواعد توجيه سير العمل ومهام قائمة الاختيار.

## <a name="relationships"></a>العلاقات

إذا كانت مؤسستك تستخدم تدرج هرمي لمصفوفة أو تدرج هرمي مخصص آخر، فيمكنك إعداد أنواع التدرجات الهرمية للمناصب. يمكنك بعد ذلك إضافة علاقات التقرير إلى المناصب لكل نوع من أنواع التدرج الهرمي الذي تقوم بإعداده. على سبيل المثال، لوري بينور هي مدير عام في "شركة المنتجات التجارية" وتم تعيينها إلى منصب **المدير العام**. تُدير لوري تطوير المنتج المستخدم لتنظيف الأدوات. وهي تتطلب محاسبًا يساعدها في في الشؤون المالية. ولذلك، قامت بتعيين نجيب عطية ليكون المحاسب الخاص بها. ويتبع نجيب مباشرة سانجاي باتيل، ولكنه يعمل أيضًا مع وري بينور في الأعمال المتعلقة بالشؤون المالية لتطوير منظف الأدوات.

وبالنسبة للمثال التالي، يجب عليك إكمال المهام التالية لإعداد علاقة العمل بين نجيب عطية ولوري بينور:

1. إنشاء نوع التدرج الهرمي للمناصب المخصص المسمى **الأداة** لإنشاء تدرج هرمي يتضمن المناصب المسؤولة عن العمل في منتج منظف الأدوات.
2. تحديد منصب **المدير العام** ليكون المنصب الذي يكون منصب نجيب مرؤوسًا له في في التدرج الهرمي **الأدوات**.
3. استخدام التدرج الهرمي للمناصب لعرض بنية الإبلاغ للمناصب. إذا كانت لديك تدرجات هرمية للمناصب متعددة، فإنه يمكنك عرض التدرج الهرمي لكل نوع تدرج هرمي في التدرج الهرمي للمناصب. يمكنك أيضًا البحث عن منصب باستخدام معرف المنصب أو اسم العامل الذي تم تعيينه إلى المنصب. التدرج الهرمي للمناصب هو التدرج الهرمي للمؤسسات.

## <a name="labor-union"></a>اتحاد العمال

يمكنك تسجيل ما إذا كانت أي اتفاقية اتحادية مطلوبة للمنصب، وأي اتحاد عمال يتم استخدامه. يمكنك أيضا إقران الاتفاقية بكيان قانوني.

## <a name="financial-dimensions"></a>الأبعاد المالية

عند إنشاء البعد المالي لأحد المناصب، يجب تحديد كيان قانوني. يمكنك تحديد الأبعاد الافتراضية لكل بُعد على حده. وبدلا من ذلك، يمكنك تحديد قالب توزيع لملء الأبعاد الافتراضية تلقائيًا. يوفر قالب التوزيع أيضًا خيارًا لتوزيع المبالغ عبر قيم أبعاد متعددة.
