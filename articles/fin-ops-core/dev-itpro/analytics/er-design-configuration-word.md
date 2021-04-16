---
title: تصميم تكوين ER جديد لإنشاء تقارير بتنسيق Word
description: يشرح هذا الموضوع كيفية قيام المستخدمين بتكوين تنسيق التقارير الإلكترونيه الجديد (ER) لإنشاء تقارير بتنسيق مستندات Microsoft Word.
author: NickSelin
ms.date: 12/17/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: 4885caf017fa0f9d36d293fa32aad53c21d3f162
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753566"
---
# <a name="design-a-new-er-configuration-to-generate-reports-in-word-format"></a><span data-ttu-id="21e4b-103">تصميم تكوين ER جديد لإنشاء تقارير بتنسيق Word</span><span class="sxs-lookup"><span data-stu-id="21e4b-103">Design a new ER configuration to generate reports in Word format</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="21e4b-104">لإنشاء تقارير كمستندات Microsoft Word، يجب تصميم قالب للتقارير باستخدام، علي سبيل المثال، تطبيق سطح المكتب الخاص ب Word.</span><span class="sxs-lookup"><span data-stu-id="21e4b-104">To generate reports as Microsoft Word documents, you must design a template for the reports by using, for example, the Word desktop application.</span></span> <span data-ttu-id="21e4b-105">يوضح الرسم التوضيحي التالي نموذج القالب الخاص بتقرير التحكم الذي يمكن إنشاؤه لإظهار تفاصيل مدفوعات المورد التي تمت معالجتها.</span><span class="sxs-lookup"><span data-stu-id="21e4b-105">The following illustration shows the sample template for the control report that can be generated to show details of processed vendor payments.</span></span>

![نموذج القالب الخاص بتقرير التحكم في تطبيق Word لسطح المكتب](./media/er-design-configuration-word-image1.png)

<span data-ttu-id="21e4b-107">لاستخدام مستند Word كقالب للتقارير الموجودة في تنسيق Word، يمكنك تكوين حل [تقارير إلكترونيه (ER) ](general-electronic-reporting.md)[جديد](er-quick-start1-new-solution.md).</span><span class="sxs-lookup"><span data-stu-id="21e4b-107">To use a Word document as a template for reports in Word format, you can configure a new [Electronic reporting (ER)](general-electronic-reporting.md) [solution](er-quick-start1-new-solution.md).</span></span> <span data-ttu-id="21e4b-108">يجب ان يتضمن هذا الحل [تكوين ER](general-electronic-reporting.md#Configuration)الذي يحتوي علي [مكون التنسيق الخاص بـ ER](general-electronic-reporting.md#FormatComponentOutbound).</span><span class="sxs-lookup"><span data-stu-id="21e4b-108">This solution must include an ER [configuration](general-electronic-reporting.md#Configuration) that contains an ER [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span>

> [!NOTE]
> <span data-ttu-id="21e4b-109">عند إنشاء تكوين جديد ل "تنسيق ER" لإنشاء التقارير بتنسيق Word، يجب اما تحديد **Word** كتنسيق لمربع الحوار **إنشاء تكوين**، أو ترك حقل **نوع التنسيق** فارغا.</span><span class="sxs-lookup"><span data-stu-id="21e4b-109">When you create a new ER format configuration to generate reports in Word format, you must either select **Word** as the format type in the **Create configuration** drop-down dialog box or leave the **Format type** field blank.</span></span>

![إنشاء تكوين تنسيق مخصص في الصفحة تكوينات](./media/er-design-configuration-word-image2.gif)

<span data-ttu-id="21e4b-111">يجب ان يحتوي مكون التنسيق الخاص بالحل علي عنصر تنسيق **ملف\\Excel**، ويجب ان يكون عنصر التنسيق هذا مرتبطا بمستند Word الذي سيتم استخدامه كقالب للتقارير التي تم إنشاؤها في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="21e4b-111">The ER format component of the solution must contain the **Excel\\File** format element, and that format element must be linked to the Word document that will be used as the template for generated reports at runtime.</span></span> <span data-ttu-id="21e4b-112">لتكوين مكون التنسيق الخاص بـ ER، يجب [فتح ](general-electronic-reporting.md#component-versioning)الإصدار التمهيدي لتكوين ER الذي تم إنشاؤه في مصمم التنسيق الخاص بـ ER.</span><span class="sxs-lookup"><span data-stu-id="21e4b-112">To configure the ER format component, you must open the [draft](general-electronic-reporting.md#component-versioning) version of the created ER configuration in the ER format designer.</span></span> <span data-ttu-id="21e4b-113">ثم قم باضافه عنصر **ملف\\Excel**، وقم بإرفاق قالب Word الخاص بك بتنسيق ER القابل للتحرير، ثم قم بربط هذا القالب بعنصر **ملف\\Excel** الذي قمت بإضافته.</span><span class="sxs-lookup"><span data-stu-id="21e4b-113">Then add the **Excel\\File** element, attach your Word template to the editable ER format, and link that template to the **Excel\\File** element that you added.</span></span>

> [!NOTE]
> <span data-ttu-id="21e4b-114">عندما تقوم بإرفاق قالب يدويًا، يجب عليك استخدام [نوع مستند](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) تم [تكوينه](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) لهذا الغرض في معلمات ER.</span><span class="sxs-lookup"><span data-stu-id="21e4b-114">When you attach a template, you must use a [document type](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) that has previously been [configured](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in the ER parameters to store templates of ER formats.</span></span>

![إرفاق قالب في الصفحة مصمم التنسيق](./media/er-design-configuration-word-image3.gif)

<span data-ttu-id="21e4b-116">يمكنك أضافه **نطاق \\excel** والعناصر المتداخلة **بخليه\\excel** لعنصر  **ملف\\Excel** لتحديد بنيه البيانات التي سيتم إدخالها في التقارير التي تم إنشاؤها في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="21e4b-116">You can add **Excel\\Range** and **Excel\\Cell** nested elements for the **Excel\\File** element to specify the structure of data that will be entered in generated reports at runtime.</span></span> <span data-ttu-id="21e4b-117">ثم يجب ربط هذه العناصر بمصادر البيانات الخاصة بتنسيق ER القابل للتحرير لتحديد البيانات الفعلية التي سيتم إدخالها في التقارير التي تم إنشاؤها في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="21e4b-117">You must then bind those elements to data sources of the editable ER format to specify the actual data that will be entered in generated reports at runtime.</span></span>

![إضافة العناصر المتداخلة في صفحة مصمم التنسيق](./media/er-design-configuration-word-image4.gif)

<span data-ttu-id="21e4b-119">عند حفظ التغييرات التي أجريتها علي التنسيق الخاص ب ER في وقت التصميم، يتم تخزين بنيه التنسيق الهرمي في قالب Word المرفق [كجزء XML مخصص](https://docs.microsoft.com/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019)يتم تسميته باسم **التقرير**.</span><span class="sxs-lookup"><span data-stu-id="21e4b-119">When you save your changes to the ER format at design time, the hierarchical format structure is stored in the attached Word template as a [custom XML part](https://docs.microsoft.com/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019) that is named **Report**.</span></span> <span data-ttu-id="21e4b-120">يجب الوصول إلى القالب المعدل وتنزيله من المالية وتخزينها محليا وفتحها في تطبيق Word لسطح المكتب.</span><span class="sxs-lookup"><span data-stu-id="21e4b-120">You must access the modified template, download it from Finance, store it locally, and open it in the Word desktop application.</span></span> <span data-ttu-id="21e4b-121">يبين الرسم التوضيحي التالي قالب نموذج تم تخزينه محليا لتقرير التحكم الذي يحتوي علي جزء XML المخصص **للتقرير**.</span><span class="sxs-lookup"><span data-stu-id="21e4b-121">The following illustration shows the locally stored sample template for the control report that contains the **Report** custom XML part.</span></span>

![مراجعة القالب الخاص بتقرير القالب في تطبيق Word لسطح المكتب](./media/er-design-configuration-word-image5.gif)

<span data-ttu-id="21e4b-123">عند تشغيل روابط **نطاق\\excel** وعناصر تنسيق **خليه\\excel** في وقت التشغيل، فان البيانات التي يتم تسليمها في كل ارتباط ستاتي في مستند Word الذي تم إنشاؤه كحقل فردي في جزء XML المخصص **للتقرير**.</span><span class="sxs-lookup"><span data-stu-id="21e4b-123">When bindings of **Excel\\Range** and **Excel\\Cell** format elements are run at runtime, the data that every binding delivers comes into the generated Word document as an individual field of the **Report** custom XML part.</span></span> <span data-ttu-id="21e4b-124">لإدخال القيم من حقول جزء XML المخصص في مستند تم إنشاؤه، يجب أضافه [عناصر تحكم محتوي word المناسبة](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word) إلى قالب word ليعمل كعناصر نائبه للبيانات التي سيتم تعبئتها في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="21e4b-124">To enter the values from the fields of the custom XML part in a generated document, you must add the appropriate Word [content controls](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word) to your Word template to serve as placeholders for data that will be filled in at runtime.</span></span> <span data-ttu-id="21e4b-125">لتحديد كيفيه ملء عناصر تحكم المحتوي، قم بتعيين كل عنصر تحكم محتوي إلى الحقل المناسب لجزء XML المخصص **للتقرير**.</span><span class="sxs-lookup"><span data-stu-id="21e4b-125">To specify how content controls are filled in, map every content control to the appropriate field of the **Report** custom XML part.</span></span>

![أضافه عناصر تحكم المحتوي وتعيينها في تطبيق سطح المكتب في Word](./media/er-design-configuration-word-image6.gif)

<span data-ttu-id="21e4b-127">يجب عليك بعد ذلك استبدال قالب Word الأصلي لتنسيق ER القابل للتحرير بالقالب المعدل الذي يحتوي الآن علي عناصر تحكم المحتوي الخاصة ب Word والتي تم تعيينها إلى حقول جزء XML المخصص **للتقرير**.</span><span class="sxs-lookup"><span data-stu-id="21e4b-127">You must then replace the original Word template of the editable ER format with the modified template that now contains Word content controls that were mapped to the fields of the **Report** custom XML part.</span></span>

![استبدال قالب في الصفحة مصمم التنسيق](./media/er-design-configuration-word-image7.gif)

<span data-ttu-id="21e4b-129">عند تشغيل تنسيق ER الذي تم تكوينه، يتم استخدام قالب Word المرفق في إنشاء تقرير جديد.</span><span class="sxs-lookup"><span data-stu-id="21e4b-129">When you run the configured ER format, the attached Word template is used to generate a new report.</span></span> <span data-ttu-id="21e4b-130">يتم تخزين البيانات الفعلية في تقرير Word كجزء XML مخصص يتم تسميته باسم **التقرير**.</span><span class="sxs-lookup"><span data-stu-id="21e4b-130">The actual data is stored in the Word report as a custom XML part that is named **Report**.</span></span> <span data-ttu-id="21e4b-131">عند فتح التقرير الذي تم إنشاؤه، يتم ملء عناصر تحكم محتوي Word بالبيانات من جزء XML المخصص **للتقرير**.</span><span class="sxs-lookup"><span data-stu-id="21e4b-131">When the generated report is opened, the Word content controls are filled in with data from the **Report** custom XML part.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="21e4b-132">الأسئلة المتداولة</span><span class="sxs-lookup"><span data-stu-id="21e4b-132">Frequently asked questions</span></span>

<span data-ttu-id="21e4b-133">**السؤال:** تم تكوين تنسيق ER لطباعه مستند Word يحتوي علي عنوان شركه.</span><span class="sxs-lookup"><span data-stu-id="21e4b-133">**Question:** I configured an ER format to print a Word document that contains a company address.</span></span> <span data-ttu-id="21e4b-134">في قالب Word لتنسيق ER هذا، قمت بادراج عنصر تحكم لمحتوي نص منسق لتقديم عنوان الشركة.</span><span class="sxs-lookup"><span data-stu-id="21e4b-134">In the Word template for this ER format, I inserted a rich text content control to present a company address.</span></span> <span data-ttu-id="21e4b-135">في Finance، قمت بإدخال عنوان الشركة كنص متعدد الأسطر و **الإدخال** المحدد لأضافه حرف إرجاع لكل سطر قمت بإدخاله.</span><span class="sxs-lookup"><span data-stu-id="21e4b-135">In Finance, I entered the company address as multiline text and selected **Enter** to add a carriage return for every line that I entered.</span></span> <span data-ttu-id="21e4b-136">التالي، أتوقع ان يظهر عنوان الشركة كنص متعدد الأسطر في المستندات التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="21e4b-136">Therefore, I expect the company address to appear as multiline text in generated documents.</span></span> <span data-ttu-id="21e4b-137">ومع ذلك، يظهر العنوان كسطر مفرد من النص يحتوي علي رموز خاصه بدلا من أحرف الرجوع.</span><span class="sxs-lookup"><span data-stu-id="21e4b-137">However, the address appears as a single line of text that contains special symbols instead of carriage returns.</span></span> <span data-ttu-id="21e4b-138">ما المقصود بالإعدادات الخاصة بي؟</span><span class="sxs-lookup"><span data-stu-id="21e4b-138">What is wrong with my settings?</span></span>

<span data-ttu-id="21e4b-139">**الاجابه:** بدلا من استخدام عنصر تحكم محتوي نص منسق ، يجب استخدام عنصر تحكم محتوي نص عادي وتحديد خانه الاختيار **السماح بادراج أسطر جديده (فقرات متعددة)** في خصائص عنصر التحكم.</span><span class="sxs-lookup"><span data-stu-id="21e4b-139">**Answer:** Instead of using a rich text content control, you must use a plain text content control and select the **Allow carriage returns (multiple paragraphs)** check box in the control's properties.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="21e4b-140">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="21e4b-140">Additional resources</span></span>

- [<span data-ttu-id="21e4b-141">إعادة استخدام التكوينات باستخدام قوالب Excel لإنشاء تقارير بتنسيقات Word</span><span class="sxs-lookup"><span data-stu-id="21e4b-141">Reuse ER configurations with Excel templates to generate reports in Word format</span></span>](./tasks/er-design-configuration-word-2016-11.md)
- [<span data-ttu-id="21e4b-142">تضمين الصور والأشكال في المستندات التي تقوم بإنشائها باستخدام التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="21e4b-142">Embed images and shapes in documents that you generate by using ER</span></span>](electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]