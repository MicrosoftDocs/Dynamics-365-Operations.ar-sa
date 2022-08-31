---
title: تصميم تكوينات ER لمنع أحرف قائمة مكونات الصنف في الملفات التي تم إنشاؤها
description: توضح هذه المقالة كيفية تكوين تنسيق إعداد التقارير الإلكترونية (ER) لإنشاء التقارير التي تقوم بمنع أحرف علامة ترتيب وحدات البايت (BOM).
author: kfend
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: EROperationDesigner
ms.openlocfilehash: a2ea132b51f2f451fbe81a9c7869bea84bf4017a
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/23/2022
ms.locfileid: "9324008"
---
# <a name="design-er-configurations-to-suppress-bom-characters-in-generated-files"></a>تصميم تكوينات ER لمنع أحرف قائمة مكونات الصنف في الملفات التي تم إنشاؤها

[!include [banner](../includes/banner.md)]

يمكنك تصميم تنسيقات [حل](er-quick-start1-new-solution.md) [إعداد التقارير الإلكترونية (ER)](general-electronic-reporting.md) لإنشاء مستندات صادرة بتنسيق XML. لإنشاء المستندات كنص أو كملفات XML، يجب ان يتضمن الحل [تكوين](general-electronic-reporting.md#Configuration) إعداد التقارير الإلكترونية (ER) الذي يحتوي علي مكون تنسيق ER. لتحديد [ترميز الأحرف](/windows/win32/intl/character-sets) الذي يمثل مجموعه الأحرف في الملفات التي تم إنشاؤها، يجب ان يحتوي التنسيق ER علي عنصر تنسيق **الملف\\عام**. لتكوين مكون تنسيق التقارير الإلكترونية ، افتح الإصدار التمهيدي لتكوين التقارير الإلكترونية في مصمم تنسيق التقارير الإلكترونية ، وأضف **عناصر\\الملف** الشائعة. في حقل **الترميز**، حدد ترميز الملفات الصادرة التي يتم إنشاؤها في وقت التشغيل باستخدام هذا المكون.

> [!NOTE]
> إذا كان التنسيق يحتوي علي اسم ترميز غير صحيح، يتم طرح خطا عند حفظ التغييرات إلى إعدادات التنسيق.

![إضافة عنصر جذر في صفحة مصمم التنسيق.](./media/er-suppress-bom-characters-image1.gif)

إذا قمت بتحديد **UTF-8** أو **UTF-16** أو **UTF-32** كترميز، سيتوفر الخيار إيقاف **أحرف قائمة مكونات الصنف**. يتم تعيين هذا الخيار على **نعم** لمنع [أحرف علامة ترتيب البايت (BOM)](/globalization/encoding/byte-order-mark) في الملفات الصادرة التي يتم إنشاؤها في وقت التشغيل عند تشغيل التنسيق ER القابل للتحرير.

> [!NOTE]
> وفي حالة ترك حقل **ترميز** فارغًا، فإنه يتم استخدام القيمة الافتراضية **UTF-8**.

![تعيين خيار إيقاف أحرف قائمة مكونات الصنف في الصفحة مصمم التنسيق.](./media/er-suppress-bom-characters-image2.gif)

لمراجعه الوظيفة في وقت التشغيل، أكمل الاجراء المناسب. علي سبيل المثال، أكمل الخطوات الموجودة في مقالة [تأجيل تنفيذ عناصر XML في تنسيق ER](er-defer-xml-element.md) . بعد إكمال الخطوات الموجودة في قسم [تعديل التنسيق بحيث يستند الحساب إلى الإخراج الذي تم إنشاؤه](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) بهذه المقالة، اتبع الخطوات الإضافية التالية.

1. حدد ترميز UTF:

    1. تحديد عنصر **تقرير** لنوع **عام\\ملف**.
    2. في حقل **الترميز**، حدد التشفير **UTF-8**.

2. إنشاء ملف XML يتضمن حرف قائمة مكونات الصنف:

    1. قم بتعيين خيار **إيقاف تحديد أحرف BOM** إلى **لا** لتضمين أحرف BOM في ملفات XML التي تم إنشاؤها.
    2. أكمل الخطوات الموجودة في قسم [تأجيل تنفيذ عنصر XML الملخص بحيث يتم استخدام المجموع المحسوب](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) من مقالة [تأجيل تنفيذ عناصر XML في](er-defer-xml-element.md) موضوع تنسيقات التقارير الإلكترونية وحفظ الملف الذي تم إنشاؤه باسم **SampleXmlReport.xml**.

3. إنشاء ملف XML لا تتضمن حرف قائمة مكونات الصنف:

    1. قم بتعيين خيار **إيقاف تحديد أحرف BOM** إلى **نعم** لتضمين أحرف BOM في ملفات XML التي تم إنشاؤها.
    2. أكمل الخطوات الموجودة في قسم [تأجيل تنفيذ عنصر XML الملخص بحيث يتم استخدام المجموع المحسوب](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) من مقالة [تأجيل تنفيذ عناصر XML في](er-defer-xml-element.md) موضوع تنسيقات التقارير الإلكترونية وحفظ الملف الذي تم إنشاؤه باسم **SampleXmlReport.xml**.

4. في الاداه المساعدة لمقارنه الملفات، قارن الملفات التي تم إنشاؤها.

    الفرق الأول الذي ستلاحظه هو الموجود في راس الملف. يحتوي الملف SampleXmlReport.xml علي حرف قائمة مكونات الصنف، حيث لا يكون ملف SampleXmlReport (1).xml.

    ![مقارنة الملفات التي تم إنشاؤها باستخدام الاداه المساعدة لمقارنه الملفات.](./media/er-suppress-bom-characters-image3.png)

## <a name="see-also"></a>راجع أيضًا

- [تأجيل تنفيذ عناصر XML في تنسيقات إعداد التقارير الإلكترونية](er-defer-xml-element.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
