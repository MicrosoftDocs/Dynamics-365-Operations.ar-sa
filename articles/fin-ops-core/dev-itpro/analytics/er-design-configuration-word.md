---
title: تصميم تكوين ER جديد لإنشاء تقارير بتنسيق Word
description: يشرح هذا الموضوع كيفية قيام المستخدمين بتكوين تنسيق التقارير الإلكترونيه الجديد (ER) لإنشاء تقارير بتنسيق مستندات Microsoft Word.
author: NickSelin
manager: AnnBe
ms.date: 12/17/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: 535e46eb033bf2796ab8e4b0d2e29767ad0a8cdf
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/30/2021
ms.locfileid: "5094144"
---
# <a name="design-a-new-er-configuration-to-generate-reports-in-word-format"></a>تصميم تكوين ER جديد لإنشاء تقارير بتنسيق Word

[!include [banner](../includes/banner.md)]

لإنشاء تقارير كمستندات Microsoft Word، يجب تصميم قالب للتقارير باستخدام، علي سبيل المثال، تطبيق سطح المكتب الخاص ب Word. يوضح الرسم التوضيحي التالي نموذج القالب الخاص بتقرير التحكم الذي يمكن إنشاؤه لإظهار تفاصيل مدفوعات المورد التي تمت معالجتها.

![نموذج القالب الخاص بتقرير التحكم في تطبيق Word لسطح المكتب](./media/er-design-configuration-word-image1.png)

لاستخدام مستند Word كقالب للتقارير الموجودة في تنسيق Word، يمكنك تكوين حل [تقارير إلكترونيه (ER) ](general-electronic-reporting.md)[جديد](er-quick-start1-new-solution.md). يجب ان يتضمن هذا الحل [تكوين ER](general-electronic-reporting.md#Configuration)الذي يحتوي علي [مكون التنسيق الخاص بـ ER](general-electronic-reporting.md#FormatComponentOutbound).

> [!NOTE]
> عند إنشاء تكوين جديد ل "تنسيق ER" لإنشاء التقارير بتنسيق Word، يجب اما تحديد **Word** كتنسيق لمربع الحوار **إنشاء تكوين**، أو ترك حقل **نوع التنسيق** فارغا.

![إنشاء تكوين تنسيق مخصص في الصفحة تكوينات](./media/er-design-configuration-word-image2.gif)

يجب ان يحتوي مكون التنسيق الخاص بالحل علي عنصر تنسيق **ملف\\Excel**، ويجب ان يكون عنصر التنسيق هذا مرتبطا بمستند Word الذي سيتم استخدامه كقالب للتقارير التي تم إنشاؤها في وقت التشغيل. لتكوين مكون التنسيق الخاص بـ ER، يجب [فتح ](general-electronic-reporting.md#component-versioning)الإصدار التمهيدي لتكوين ER الذي تم إنشاؤه في مصمم التنسيق الخاص بـ ER. ثم قم باضافه عنصر **ملف\\Excel**، وقم بإرفاق قالب Word الخاص بك بتنسيق ER القابل للتحرير، ثم قم بربط هذا القالب بعنصر **ملف\\Excel** الذي قمت بإضافته.

> [!NOTE]
> عندما تقوم بإرفاق قالب يدويًا، يجب عليك استخدام [نوع مستند](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) تم [تكوينه](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) لهذا الغرض في معلمات ER.

![إرفاق قالب في الصفحة مصمم التنسيق](./media/er-design-configuration-word-image3.gif)

يمكنك أضافه **نطاق \\excel** والعناصر المتداخلة **بخليه\\excel** لعنصر  **ملف\\Excel** لتحديد بنيه البيانات التي سيتم إدخالها في التقارير التي تم إنشاؤها في وقت التشغيل. ثم يجب ربط هذه العناصر بمصادر البيانات الخاصة بتنسيق ER القابل للتحرير لتحديد البيانات الفعلية التي سيتم إدخالها في التقارير التي تم إنشاؤها في وقت التشغيل.

![إضافة العناصر المتداخلة في صفحة مصمم التنسيق](./media/er-design-configuration-word-image4.gif)

عند حفظ التغييرات التي أجريتها علي التنسيق الخاص ب ER في وقت التصميم، يتم تخزين بنيه التنسيق الهرمي في قالب Word المرفق [كجزء XML مخصص](https://docs.microsoft.com/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019)يتم تسميته باسم **التقرير**. يجب الوصول إلى القالب المعدل وتنزيله من المالية وتخزينها محليا وفتحها في تطبيق Word لسطح المكتب. يبين الرسم التوضيحي التالي قالب نموذج تم تخزينه محليا لتقرير التحكم الذي يحتوي علي جزء XML المخصص **للتقرير**.

![مراجعة القالب الخاص بتقرير القالب في تطبيق Word لسطح المكتب](./media/er-design-configuration-word-image5.gif)

عند تشغيل روابط **نطاق\\excel** وعناصر تنسيق **خليه\\excel** في وقت التشغيل، فان البيانات التي يتم تسليمها في كل ارتباط ستاتي في مستند Word الذي تم إنشاؤه كحقل فردي في جزء XML المخصص **للتقرير**. لإدخال القيم من حقول جزء XML المخصص في مستند تم إنشاؤه، يجب أضافه [عناصر تحكم محتوي word المناسبة](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word) إلى قالب word ليعمل كعناصر نائبه للبيانات التي سيتم تعبئتها في وقت التشغيل. لتحديد كيفيه ملء عناصر تحكم المحتوي، قم بتعيين كل عنصر تحكم محتوي إلى الحقل المناسب لجزء XML المخصص **للتقرير**.

![أضافه عناصر تحكم المحتوي وتعيينها في تطبيق سطح المكتب في Word](./media/er-design-configuration-word-image6.gif)

يجب عليك بعد ذلك استبدال قالب Word الأصلي لتنسيق ER القابل للتحرير بالقالب المعدل الذي يحتوي الآن علي عناصر تحكم المحتوي الخاصة ب Word والتي تم تعيينها إلى حقول جزء XML المخصص **للتقرير**.

![استبدال قالب في الصفحة مصمم التنسيق](./media/er-design-configuration-word-image7.gif)

عند تشغيل تنسيق ER الذي تم تكوينه، يتم استخدام قالب Word المرفق في إنشاء تقرير جديد. يتم تخزين البيانات الفعلية في تقرير Word كجزء XML مخصص يتم تسميته باسم **التقرير**. عند فتح التقرير الذي تم إنشاؤه، يتم ملء عناصر تحكم محتوي Word بالبيانات من جزء XML المخصص **للتقرير**.

## <a name="frequently-asked-questions"></a>الأسئلة المتداولة

**السؤال:** تم تكوين تنسيق ER لطباعه مستند Word يحتوي علي عنوان شركه. في قالب Word لتنسيق ER هذا، قمت بادراج عنصر تحكم لمحتوي نص منسق لتقديم عنوان الشركة. في Finance، قمت بإدخال عنوان الشركة كنص متعدد الأسطر و **الإدخال** المحدد لأضافه حرف إرجاع لكل سطر قمت بإدخاله. التالي، أتوقع ان يظهر عنوان الشركة كنص متعدد الأسطر في المستندات التي تم إنشاؤها. ومع ذلك، يظهر العنوان كسطر مفرد من النص يحتوي علي رموز خاصه بدلا من أحرف الرجوع. ما المقصود بالإعدادات الخاصة بي؟

**الاجابه:** بدلا من استخدام عنصر تحكم محتوي نص منسق ، يجب استخدام عنصر تحكم محتوي نص عادي وتحديد خانه الاختيار **السماح بادراج أسطر جديده (فقرات متعددة)** في خصائص عنصر التحكم.

## <a name="additional-resources"></a>الموارد الإضافية

- [إعادة استخدام التكوينات باستخدام قوالب Excel لإنشاء تقارير بتنسيقات Word](./tasks/er-design-configuration-word-2016-11.md)
- [تضمين الصور والأشكال في المستندات التي تقوم بإنشائها باستخدام التقارير الإلكترونية](electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]