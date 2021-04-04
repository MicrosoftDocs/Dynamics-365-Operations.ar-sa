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
# <a name="design-er-configurations-to-suppress-bom-characters-in-generated-files"></a><span data-ttu-id="c8ce3-103">تصميم تكوينات ER لمنع أحرف قائمة مكونات الصنف في الملفات التي تم إنشاؤها</span><span class="sxs-lookup"><span data-stu-id="c8ce3-103">Design ER configurations to suppress BOM characters in generated files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c8ce3-104">يمكنك تصميم تنسيقات [حل](er-quick-start1-new-solution.md) [إعداد التقارير الإلكترونية (ER)](general-electronic-reporting.md) لإنشاء مستندات صادرة بتنسيق XML.</span><span class="sxs-lookup"><span data-stu-id="c8ce3-104">You can design an [Electronic reporting (ER)](general-electronic-reporting.md) [solution](er-quick-start1-new-solution.md) to generate outgoing documents.</span></span> <span data-ttu-id="c8ce3-105">لإنشاء المستندات كنص أو كملفات XML، يجب ان يتضمن الحل [تكوين ER](general-electronic-reporting.md#Configuration) الذي يحتوي علي [مكون التنسيق الخاص بـ ER](general-electronic-reporting.md#FormatComponentOutbound).</span><span class="sxs-lookup"><span data-stu-id="c8ce3-105">To generate the documents as text or XML files, the solution must include an ER [configuration](general-electronic-reporting.md#Configuration) that contains an ER [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="c8ce3-106">لتحديد [ترميز الأحرف](https://docs.microsoft.com/windows/win32/intl/character-sets) الذي يمثل مجموعه الأحرف في الملفات التي تم إنشاؤها، يجب ان يحتوي التنسيق ER علي عنصر تنسيق **الملف\\عام**.</span><span class="sxs-lookup"><span data-stu-id="c8ce3-106">To specify the [character encoding](https://docs.microsoft.com/windows/win32/intl/character-sets) that represents the set of characters in generated files, the ER format must contain the **Common\\File** format element.</span></span> <span data-ttu-id="c8ce3-107">لتكوين مكون التنسيق الخاص بـ ER، يجب فتح [الإصدار التمهيدي](general-electronic-reporting.md#component-versioning) لتكوين ER في مصمم التنسيق الخاص بـ ER، وإضافة العنصر **عام\\ملف**.</span><span class="sxs-lookup"><span data-stu-id="c8ce3-107">To configure the ER format component, open the [draft](general-electronic-reporting.md#component-versioning) version of the ER configuration in the ER format designer, and add the **Common\\File** element.</span></span> <span data-ttu-id="c8ce3-108">في حقل **الترميز**، حدد ترميز الملفات الصادرة التي يتم إنشاؤها في وقت التشغيل باستخدام هذا المكون.</span><span class="sxs-lookup"><span data-stu-id="c8ce3-108">In the **Encoding** field, specify the encoding of outbound files that are generated at runtime by using this component.</span></span>

> [!NOTE]
> <span data-ttu-id="c8ce3-109">إذا كان التنسيق يحتوي علي اسم ترميز غير صحيح، يتم طرح خطا عند حفظ التغييرات إلى إعدادات التنسيق.</span><span class="sxs-lookup"><span data-stu-id="c8ce3-109">If the format contains an incorrect encoding name, an error is thrown when you save your changes to the format's settings.</span></span>

![إضافة عنصر جذر في صفحة مصمم التنسيق](./media/er-suppress-bom-characters-image1.gif)

<span data-ttu-id="c8ce3-111">إذا قمت بتحديد **UTF-8** أو **UTF-16** أو **UTF-32** كترميز، سيتوفر الخيار إيقاف **أحرف قائمة مكونات الصنف**.</span><span class="sxs-lookup"><span data-stu-id="c8ce3-111">If you specify **UTF-8**, **UTF-16**, or **UTF-32** as the encoding, the **Suppress BOM characters** option becomes available.</span></span> <span data-ttu-id="c8ce3-112">يتم تعيين هذا الخيار على **نعم** لمنع [أحرف علامة ترتيب البايت (BOM)](https://docs.microsoft.com/globalization/encoding/byte-order-mark) في الملفات الصادرة التي يتم إنشاؤها في وقت التشغيل عند تشغيل التنسيق ER القابل للتحرير.</span><span class="sxs-lookup"><span data-stu-id="c8ce3-112">Set this option to **Yes** to suppress [byte order mark (BOM) characters](https://docs.microsoft.com/globalization/encoding/byte-order-mark) in outbound files that are generated at runtime when the editable ER format is run.</span></span>

> [!NOTE]
> <span data-ttu-id="c8ce3-113">وفي حالة ترك حقل **ترميز** فارغًا، فإنه يتم استخدام القيمة الافتراضية **UTF-8**.</span><span class="sxs-lookup"><span data-stu-id="c8ce3-113">If you leave the **Encoding** field blank, the default **UTF-8** encoding is used.</span></span>

![تعيين خيار إيقاف أحرف قائمه مكونات الصنف في الصفحة مصمم التنسيق](./media/er-suppress-bom-characters-image2.gif)

<span data-ttu-id="c8ce3-115">لمراجعه الوظيفة في وقت التشغيل، أكمل الاجراء المناسب.</span><span class="sxs-lookup"><span data-stu-id="c8ce3-115">To review the functionality at runtime, complete the appropriate procedure.</span></span> <span data-ttu-id="c8ce3-116">علي سبيل المثال، أكمل الخطوات الموجودة في الموضوع [تاجيل تنفيذ عناصر XML في التنسيق ER](er-defer-xml-element.md).</span><span class="sxs-lookup"><span data-stu-id="c8ce3-116">For example, complete the steps in the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic.</span></span> <span data-ttu-id="c8ce3-117">بعد إكمال الخطوات الموجودة في [تعديل التنسيق بحيث يستند الحساب إلى قسم الإخراج الذي تم إنشاؤه ](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) لهذا الموضوع، اتبع الخطوات الاضافيه التالية.</span><span class="sxs-lookup"><span data-stu-id="c8ce3-117">After you've completed the steps in the [Modify the format so that the calculation is based on generated output](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) section of that topic, follow these additional steps.</span></span>

1. <span data-ttu-id="c8ce3-118">حدد ترميز UTF:</span><span class="sxs-lookup"><span data-stu-id="c8ce3-118">Specify the UTF encoding:</span></span>

    1. <span data-ttu-id="c8ce3-119">تحديد عنصر **تقرير** لنوع **عام\\ملف**.</span><span class="sxs-lookup"><span data-stu-id="c8ce3-119">Select the **Report** element of the **Common\\File** type.</span></span>
    2. <span data-ttu-id="c8ce3-120">في حقل **الترميز**، حدد التشفير **UTF-8**.</span><span class="sxs-lookup"><span data-stu-id="c8ce3-120">In the **Encoding** field, specify the **UTF-8** encoding.</span></span>

2. <span data-ttu-id="c8ce3-121">إنشاء ملف XML يتضمن حرف قائمة مكونات الصنف:</span><span class="sxs-lookup"><span data-stu-id="c8ce3-121">Generate an XML file that includes a BOM character:</span></span>

    1. <span data-ttu-id="c8ce3-122">قم بتعيين خيار **إيقاف تحديد أحرف BOM** إلى **لا** لتضمين أحرف BOM في ملفات XML التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="c8ce3-122">Set the **Suppress BOM characters** option to **No** to include BOM characters in generated XML files.</span></span>
    2. <span data-ttu-id="c8ce3-123">أكمل الخطوات الموجودة في [تاجيل تنفيذ عنصر XML الملخص بحيث يتم استخدام المجموع المحسوب](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used)لقسم [تاجيل تنفيذ عناصر XML في](er-defer-xml-element.md)موضوع تنسيقات ER، وحفظ الملف الذي تم إنشاؤه باسم **SampleXmlReport.xml**.</span><span class="sxs-lookup"><span data-stu-id="c8ce3-123">Complete the steps in the [Defer the execution of the summary XML element so that the calculated total is used](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) section of the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic, and save the generated file as **SampleXmlReport.xml**.</span></span>

3. <span data-ttu-id="c8ce3-124">إنشاء ملف XML لا تتضمن حرف قائمة مكونات الصنف:</span><span class="sxs-lookup"><span data-stu-id="c8ce3-124">Generate an XML file that doesn't include a BOM character:</span></span>

    1. <span data-ttu-id="c8ce3-125">قم بتعيين خيار **إيقاف تحديد أحرف BOM** إلى **نعم** لتضمين أحرف BOM في ملفات XML التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="c8ce3-125">Set the **Suppress BOM characters** option to **Yes** to suppress BOM characters in generated XML files.</span></span>
    2. <span data-ttu-id="c8ce3-126">أكمل الخطوات الموجودة في [تاجيل تنفيذ عنصر XML الملخص بحيث يتم استخدام المجموع المحسوب](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used)لقسم [تاجيل تنفيذ عناصر XML في](er-defer-xml-element.md)موضوع تنسيقات ER، وحفظ الملف الذي تم إنشاؤه باسم **SampleXmlReport.xml**.</span><span class="sxs-lookup"><span data-stu-id="c8ce3-126">Complete the steps in the [Defer the execution of the summary XML element so that the calculated total is used](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) section of the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic, and save the generated file as **SampleXmlReport (1).xml**.</span></span>

4. <span data-ttu-id="c8ce3-127">في الاداه المساعدة لمقارنه الملفات، قارن الملفات التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="c8ce3-127">In a file comparison utility, compare the generated files.</span></span>

    <span data-ttu-id="c8ce3-128">الفرق الأول الذي ستلاحظه هو الموجود في راس الملف.</span><span class="sxs-lookup"><span data-stu-id="c8ce3-128">The first difference that you will notice is in the file header.</span></span> <span data-ttu-id="c8ce3-129">يحتوي الملف SampleXmlReport.xml علي حرف قائمة مكونات الصنف، حيث لا يكون ملف SampleXmlReport (1).xml.</span><span class="sxs-lookup"><span data-stu-id="c8ce3-129">The SampleXmlReport.xml file contains a BOM character, where the SampleXmlReport (1).xml file doesn't.</span></span>

    ![مقارنة الملفات التي تم إنشاؤها باستخدام الاداه المساعدة لمقارنه الملفات](./media/er-suppress-bom-characters-image3.png)

## <a name="see-also"></a><span data-ttu-id="c8ce3-131">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="c8ce3-131">See also</span></span>

- [<span data-ttu-id="c8ce3-132">تأجيل تنفيذ عناصر XML في تنسيقات إعداد التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="c8ce3-132">Defer the execution of XML elements in ER formats</span></span>](er-defer-xml-element.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]