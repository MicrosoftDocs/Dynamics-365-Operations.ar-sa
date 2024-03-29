---
title: مصطلحات نموذج الصفحة
description: يصف هذا المقال العناصر المتعددة التي يتم استخدامها في موقع Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: intro-internal
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: a4c2a29e8c2112622b5e30064e26523b4f9e2d5a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281417"
---
# <a name="page-model-glossary"></a>مصطلحات نموذج الصفحة


[!include [banner](includes/banner.md)]

يصف هذا المقال العناصر المتعددة التي يتم استخدامها في موقع Microsoft Dynamics 365 Commerce.

## <a name="page-element-definitions"></a>تعريفات عناصر الصفحة

يسرد الجدول التالي ملخصًا للمصطلحات التي ينبغي أن تكون على دراية بها عندما تقوم بتغيير شكل وأسلوب ومحتوى موقعك. للحصول علي توضيحات وإجراءات أكثر شمولاً ، اتبع الارتباطات.

| الفصل الدراسي | الوصف والملاحظات |
|------|-----------------------|
| [الوحدة](work-with-modules.md) | <p>**التعريف:** الوحدات النمطية هي كتلة الإنشاء التي يمكن كتابتها وتشكل هيكل صفحة الويب. تشمل الأمثلة الوحدات النمطية للعناوين والوحدات النمطية للأجزاء الرئيسية والوحدات النمطية الدوارة.</p><p>**مكان تحدديها:** يمكن تحديد الوحدات النمطية المنشورة وتكوينها في مراحل مختلفة من سير عمل تأليف الموقع، مثل القالب والتخطيط والصفحة ومراحل تأليف الأجزاء.</p><p>**مكان تحريرها:** يتم إنشاء الوحدات النمطية المخصصة في التعليمات البرمجية باستخدام مجموعة تطوير البرامج (SDK). ويتم بعد ذلك تحميلها إلى الموقع الخاص بك، حيث تصبح متوفرة للتحديد.</p> |
| خاصية الوحدة النمطية | <p>**التعريف** : خصائص الوحدات النمطية هي إعدادات محددة يتم تعريفها بواسطة الوحدة النمطية. ويمكن تحريرها في أدوات تأليف التجارة الإلكترونية. على سبيل المثال، يتم استخدام خصائص الوحدات النمطية لتعيين صورة العنوان والخلفية لوحدة نمطية للشعار.</p><p>**مكان تكوينها:** يتم تحديد خصائص الوحدات النمطية وتكوينها في جزء الخاصية الذي يظهر في بيئات التأليف (المحررين) للقوالب والتخطيطات والصفحات والأجزاء وإعدادات التطبيق.</p> |
| [القالب](templates-layouts-overview.md) | <p>**التعريف:** تعرف القوالب مجموعات الوحدات النمطية والخيارات التي يجب استخدامها لفئة من الصفحات (على سبيل المثال، صفحات التسويق وصفحات الفئات وصفحات المنتجات).</p><p>**مكان تحديدها:** يمكن تحديد القوالب أثناء عمليات سير عمل إنشاء الصفحة أو التخطيط.</p><p>**مكان تحريرها:** تتم كتابة القوالب في محرر القالب. ليس ثمة حاجة لتعليمة برمجية لإنشاء القوالب أو تعديلها.</p> |
| [تخطيط](templates-layouts-overview.md) | <p>**التعريف:** تحدد التخطيطات الاختيار النهائي وترتيب الوحدات النمطية من مجموعة الخيارات الخاصة بالقالب الأصل. يمكن تكوين تخطيط لصفحة مفردة (*تخطيط مخصص*) ، أو يمكن مشاركته بين العديد من الصفحات (*التخطيط المعين مسبقا*).</p><p>**مكان تحديدها:** يمكن تحديد التخطيطات أثناء إنشاء الصفحة الجديدة أو عند الحاجة إلى تخطيط مختلف لصفحة موجودة.</p><p>**مكان تحريرها:** تتم كتابة التخطيطات في محرر التخطيط. ليس ثمة حاجة لتعليمة برمجية لإنشاء القوالب أو تعديلها.</p> |
| [مثيل الصفحة](modify-existing-page.md) | <p>**التعريف:** تحدد مثيلات الصفحة المحتوي المترجم النهائي الخاص بالصفحة لصفحة واحدة. يتم اشتقاق هذا المحتوى من قيم خصائص الوحدة النمطية.</p><p>**مكان تحديدها:** يتم تحديد الصفحات عند تعيين عناوين URL.</p><p>**مكان تحريرها:** يتم تحرير الصفحات في محرر الصفحة. ليس ثمة حاجة لتعليمة برمجية لإنشاء القوالب أو تعديلها.</p> |
| [سمة](select-site-theme.md) | <p>**التعريف:** تحدد السمات ورقه الأنماط المتتالية (CSS)، وتحدد شكل وأسلوب الوحدات النمطية التي يتم تقديمها في الصفحة.</p><p>**مكان تحديدها:** بعد تحميل سمة إلى موقعك باستخدام Microsoft Dynamics Lifecycle Services (LCS)، يمكن تحديدها كخاصية للوحدة النمطية لحاوية الصفحة.</p><p>**مكان تحريرها:** يتم إنشاء السمات وتحريرها حاليًا باستخدام SDK. ثم يتم تحميلها إلى موقعك باستخدام LCS.</p> |
| [جزء](work-with-fragments.md) | <p>**التعريف:** الأجزاء هي وحدات نمطية تم تكوينها بالكامل وتحتوي على محتوى مترجم يمكن إعادة استخدامه وتحديثه مركزيًا عبر عدة صفحات. على سبيل المثال، يمكن استخدام جزء تم إنشاؤه من الوحدة النمطية للعنوان في كافة القوالب وعلى كافة الصفحات عبر الموقع الخاص بك، ويتم تحديثه مركزيًا في مكان واحد.</p><p>**مكان تحديدها** يمكن تحديد الأجزاء أينما يمكن تحديد الوحدات النمطية. ويمكن استبدالها بوحدة نمطية للمساعدة على زيادة الكفاءة من خلال التأليف المركزي القابل لإعادة الاستخدام.</p><p>**مكان تحريرها:** يتم تحرير الأجزاء في محرر الجزء. ليس ثمة حاجة لتعليمة برمجية لإنشاء القوالب أو تعديلها.</p> |
| [عنوان URL](create-page-URL.md) | <p>**التعريف:** محددات مواقع الويب (URLs) هي عناوين تشير إلى صفحات الويب أو عناوين URL أخرى.</p><p>**مكان تحديدها:** يتم تحديد عناوين URL أينما كان مطلوبًا توفير ارتباطات بين الصفحات.</p><p>**مكان تحريرها:** يتم تحرير عناوين URL في محرر URL. ليس ثمة حاجة لتعليمة برمجية لإنشاء القوالب أو تعديلها.</p> |
| الأصل | <p>**التعريف** : الأصول هي ثنائيات الملف التي لها ملحق مثل jpg. أو docx. أو pdf. أو mpg..</p><p>**مكان تحديدها:** يتم تحديد الأصول كخصائص للوحدات النمطية للوحدات النمطية التي تتطلبها.</p><p>**مكان تحريرها** يتم تحميل الأصول، ويتم تحرير بيانات التعريف المقترنة في مدير الأصول.</p> |

## <a name="additional-resources"></a>الموارد الإضافية

[طرق إضافة المحتوى](add-manage-content.md)

[حالات المستند ودورة الحياة](document-states-overview.md)

[العمل مع مجموعات النشر](publish-groups.md)

[تمكين المشاركة عبر القنوات واستخدامها](cross-channel-sharing.md)

[العمل باستخدام الوحدات النمطية](work-with-modules.md)

[العمل باستخدام الأجزاء](work-with-fragments.md)

[نظرة عامة على القوالب والتخطيطات](templates-layouts-overview.md)

[تخصيص التنقل في الموقع](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
