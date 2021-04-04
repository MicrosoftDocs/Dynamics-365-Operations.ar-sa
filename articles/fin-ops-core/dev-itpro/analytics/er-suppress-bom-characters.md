---
title: تصميم تكوينات ER لمنع أحرف قائمة مكونات الصنف في الملفات التي تم إنشاؤها
description: يوضح هذا الموضوع كيفيه تكوين تنسيق اعداد التقارير الكترونيه (ER) لإنشاء التقارير التي تقوم بمنع أحرف علامة ترتيب البايت (BOM).
author: NickSelin
manager: AnnBe
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9260db2edab75c9876ddf5af99bee4ff174c64e1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568963"
---
# <a name="design-er-configurations-to-suppress-bom-characters-in-generated-files"></a>تصميم تكوينات ER لمنع أحرف قائمة مكونات الصنف في الملفات التي تم إنشاؤها

[!include [banner](../includes/banner.md)]

يمكنك تصميم تنسيقات [حل](er-quick-start1-new-solution.md) [إعداد التقارير الإلكترونية (ER)](general-electronic-reporting.md) لإنشاء مستندات صادرة بتنسيق XML. لإنشاء المستندات كنص أو كملفات XML، يجب ان يتضمن الحل [تكوين ER](general-electronic-reporting.md#Configuration) الذي يحتوي علي [مكون التنسيق الخاص بـ ER](general-electronic-reporting.md#FormatComponentOutbound). لتحديد [ترميز الأحرف](https://docs.microsoft.com/windows/win32/intl/character-sets) الذي يمثل مجموعه الأحرف في الملفات التي تم إنشاؤها، يجب ان يحتوي التنسيق ER علي عنصر تنسيق **الملف\\عام**. لتكوين مكون التنسيق الخاص بـ ER، يجب فتح [الإصدار التمهيدي](general-electronic-reporting.md#component-versioning) لتكوين ER في مصمم التنسيق الخاص بـ ER، وإضافة العنصر **عام\\ملف**. في حقل **الترميز**، حدد ترميز الملفات الصادرة التي يتم إنشاؤها في وقت التشغيل باستخدام هذا المكون.

> [!NOTE]
> إذا كان التنسيق يحتوي علي اسم ترميز غير صحيح، يتم طرح خطا عند حفظ التغييرات إلى إعدادات التنسيق.

![إضافة عنصر جذر في صفحة مصمم التنسيق](./media/er-suppress-bom-characters-image1.gif)

إذا قمت بتحديد **UTF-8** أو **UTF-16** أو **UTF-32** كترميز، سيتوفر الخيار إيقاف **أحرف قائمة مكونات الصنف**. يتم تعيين هذا الخيار على **نعم** لمنع [أحرف علامة ترتيب البايت (BOM)](https://docs.microsoft.com/globalization/encoding/byte-order-mark) في الملفات الصادرة التي يتم إنشاؤها في وقت التشغيل عند تشغيل التنسيق ER القابل للتحرير.

> [!NOTE]
> وفي حالة ترك حقل **ترميز** فارغًا، فإنه يتم استخدام القيمة الافتراضية **UTF-8**.

![تعيين خيار إيقاف أحرف قائمه مكونات الصنف في الصفحة مصمم التنسيق](./media/er-suppress-bom-characters-image2.gif)

لمراجعه الوظيفة في وقت التشغيل، أكمل الاجراء المناسب. علي سبيل المثال، أكمل الخطوات الموجودة في الموضوع [تاجيل تنفيذ عناصر XML في التنسيق ER](er-defer-xml-element.md). بعد إكمال الخطوات الموجودة في [تعديل التنسيق بحيث يستند الحساب إلى قسم الإخراج الذي تم إنشاؤه ](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) لهذا الموضوع، اتبع الخطوات الاضافيه التالية.

1. حدد ترميز UTF:

    1. تحديد عنصر **تقرير** لنوع **عام\\ملف**.
    2. في حقل **الترميز**، حدد التشفير **UTF-8**.

2. إنشاء ملف XML يتضمن حرف قائمة مكونات الصنف:

    1. قم بتعيين خيار **إيقاف تحديد أحرف BOM** إلى **لا** لتضمين أحرف BOM في ملفات XML التي تم إنشاؤها.
    2. أكمل الخطوات الموجودة في [تاجيل تنفيذ عنصر XML الملخص بحيث يتم استخدام المجموع المحسوب](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used)لقسم [تاجيل تنفيذ عناصر XML في](er-defer-xml-element.md)موضوع تنسيقات ER، وحفظ الملف الذي تم إنشاؤه باسم **SampleXmlReport.xml**.

3. إنشاء ملف XML لا تتضمن حرف قائمة مكونات الصنف:

    1. قم بتعيين خيار **إيقاف تحديد أحرف BOM** إلى **نعم** لتضمين أحرف BOM في ملفات XML التي تم إنشاؤها.
    2. أكمل الخطوات الموجودة في [تاجيل تنفيذ عنصر XML الملخص بحيث يتم استخدام المجموع المحسوب](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used)لقسم [تاجيل تنفيذ عناصر XML في](er-defer-xml-element.md)موضوع تنسيقات ER، وحفظ الملف الذي تم إنشاؤه باسم **SampleXmlReport.xml**.

4. في الاداه المساعدة لمقارنه الملفات، قارن الملفات التي تم إنشاؤها.

    الفرق الأول الذي ستلاحظه هو الموجود في راس الملف. يحتوي الملف SampleXmlReport.xml علي حرف قائمة مكونات الصنف، حيث لا يكون ملف SampleXmlReport (1).xml.

    ![مقارنة الملفات التي تم إنشاؤها باستخدام الاداه المساعدة لمقارنه الملفات](./media/er-suppress-bom-characters-image3.png)

## <a name="see-also"></a>راجع أيضًا

- [تأجيل تنفيذ عناصر XML في تنسيقات إعداد التقارير الإلكترونية](er-defer-xml-element.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]