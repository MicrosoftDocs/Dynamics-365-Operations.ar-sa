---
title: استخدام مصادر بيانات الأكواد الشريطية لإنشاء صور للكود الشريطي
description: يشرح هذا الموضوع كيفية استخدام مصادر بيانات الأكواد الشريطية لإنشاء صور الأكواد الشريطية.
author: NickSelin
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Version 10.0.13
ms.openlocfilehash: 08b9d03517a600cf46b1093cfa3bc454621eabd0
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748355"
---
# <a name="use-barcode-data-sources-to-generate-bar-code-images"></a><span data-ttu-id="574a0-103">استخدام مصادر بيانات الأكواد الشريطية لإنشاء صور للكود الشريطي</span><span class="sxs-lookup"><span data-stu-id="574a0-103">Use Barcode data sources to generate bar code images</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="574a0-104">يمكنك استخدام إطار عمل [التقارير الإكترونية (ER)](general-electronic-reporting.md) لتصميم [مكونات تنسيق ER](general-electronic-reporting.md#FormatComponentOutbound) التي يمكنك تشغيلها لإنشاء مستندات صادرة إلكترونية وقابلة للطباعة تتطلب الحصول عليها.</span><span class="sxs-lookup"><span data-stu-id="574a0-104">You can use the [Electronic reporting (ER)](general-electronic-reporting.md) framework to design [ER format components](general-electronic-reporting.md#FormatComponentOutbound) that you can run to generate electronic and printable outbound documents that you require.</span></span> <span data-ttu-id="574a0-105">لإنشاء مستند صادر في تنسيق Microsoft Office، فإنه يجب تحديد التقرير باستخدام إما مستند Microsoft Excel أو مستند Microsoft Word كقالب تقرير.</span><span class="sxs-lookup"><span data-stu-id="574a0-105">To generate an outbound document in Microsoft Office format, you must specify the layout of the report by using either a Microsoft Excel document or a Microsoft Word document as a report template.</span></span> <span data-ttu-id="574a0-106">يسمح لك [مصمم عمليات ER](general-electronic-reporting.md#building-a-format-that-uses-a-data-model-as-a-base) بإرفاق مستند Excel أو Word كقالب لتنسيق ER.</span><span class="sxs-lookup"><span data-stu-id="574a0-106">The [ER Operations designer](general-electronic-reporting.md#building-a-format-that-uses-a-data-model-as-a-base) lets you attach an Excel or Word document as a template for an ER format.</span></span> <span data-ttu-id="574a0-107">يتم إقتران العناصر التالية التي تمت تسميتها في القالب المرفق بعناصر مكون التنسيق الذي تم تكوينه:</span><span class="sxs-lookup"><span data-stu-id="574a0-107">The following named elements in the attached template are associated with the elements of the configured format component:</span></span>

- <span data-ttu-id="574a0-108">عناصر تحكم المحتوى في Word</span><span class="sxs-lookup"><span data-stu-id="574a0-108">Content controls in Word</span></span>
- <span data-ttu-id="574a0-109">كشوف والنطاقات والخلايا والأشكال والصور التي تمت تسميتها في Excel</span><span class="sxs-lookup"><span data-stu-id="574a0-109">Named sheets, ranges, cells, shapes, and images in Excel</span></span>

<span data-ttu-id="574a0-110">يتم استخدام هذه العناصر التي تمت تسميتها كعناصر نائبة للبيانات التي يتم إدخالها في المستند الذي تم إنشاؤه عند تشغيل تنسيق ER.</span><span class="sxs-lookup"><span data-stu-id="574a0-110">These named elements are used as placeholders for data that is entered in a generated document when an ER format is run.</span></span> <span data-ttu-id="574a0-111">يتم ربط عناصر التنسيق ER إلى مصادر البيانات.</span><span class="sxs-lookup"><span data-stu-id="574a0-111">ER format elements are bound to data sources.</span></span> <span data-ttu-id="574a0-112">وتحدد مصادر البيانات هذه البيانات التي سيتم إدخالها في المستندات التي تم إنشاؤها في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="574a0-112">These data sources specify the data that will be entered in the generated documents at runtime.</span></span> <span data-ttu-id="574a0-113">للمزيد من المعلومات، راجع [تضمين الصور والأشكال في المستندات التي تقوم بإنشائها باستخدام التقارير الإلكترونية](electronic-reporting-embed-images-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="574a0-113">For more information, see [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md).</span></span>

<span data-ttu-id="574a0-114">يدعم ER الآن نوع مصدر البيانات **الكود الشريطي**.</span><span class="sxs-lookup"><span data-stu-id="574a0-114">ER now supports the **Barcode** data source type.</span></span> <span data-ttu-id="574a0-115">وبالتالي، يمكنك الآن إنشاء صورة تمثل الكود الشريطي للنص المعين.</span><span class="sxs-lookup"><span data-stu-id="574a0-115">Therefore, you can now generate an image that represents the bar code for specified text.</span></span> <span data-ttu-id="574a0-116">عندما تقوم بتكوين تنسيق ER، فإنه يمكنك تحديد مصادر البيانات لنوع **الكود الشريطي** لإنشاء صور الكود الشريطي.</span><span class="sxs-lookup"><span data-stu-id="574a0-116">When you configure an ER format, you can specify data sources of the **Barcode** type to generate bar code images.</span></span> <span data-ttu-id="574a0-117">ثم يمكنك بعد ذلك إضافة تلك الصور إلى مستندات العمل التي تم إنشاؤها، مثل الأوامر والفواتير وإيصال التعبئة والإيصالات.</span><span class="sxs-lookup"><span data-stu-id="574a0-117">You can then add those images to generated business documents, such as orders, invoices, packing slips, and receipts.</span></span> <span data-ttu-id="574a0-118">يمكنك أيضًا إضافتها إلى أنواع مختلفة من التسميات، مثل تسميات المنتج والرف وتسميات التعبئة والشحن.</span><span class="sxs-lookup"><span data-stu-id="574a0-118">You can also add them to various kind of labels, such as product and shelf labels, and packaging and shipping labels.</span></span>

<span data-ttu-id="574a0-119">يمكن استخدام العناصر النائبة التالية في قوالب التقارير لإدخال صور الأكواد الشريطية:</span><span class="sxs-lookup"><span data-stu-id="574a0-119">The following placeholders can be used in report templates to enter bar code images:</span></span>

- <span data-ttu-id="574a0-120">[صورة](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word) التحكم بمحتوى Word</span><span class="sxs-lookup"><span data-stu-id="574a0-120">[Picture](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word) content control for Word</span></span>
- <span data-ttu-id="574a0-121">[صورة](https://support.office.com/article/insert-pictures-3c51edf4-22e1-460a-b372-9329a8724344) كائن في Excel</span><span class="sxs-lookup"><span data-stu-id="574a0-121">[Picture](https://support.office.com/article/insert-pictures-3c51edf4-22e1-460a-b372-9329a8724344) object in Excel</span></span>

<span data-ttu-id="574a0-122">باستخدام مصدر بيانات من نوع **الكود الشريطي**، يمكنك إنشاء الأكواد الشريطية بالتنسيقات التالية:</span><span class="sxs-lookup"><span data-stu-id="574a0-122">By using a data source of the **Barcode** type, you can generate bar codes in the following formats:</span></span>

- <span data-ttu-id="574a0-123">الأكواد الشريطية أحادية الأبعاد:</span><span class="sxs-lookup"><span data-stu-id="574a0-123">One-dimensional bar codes:</span></span>

    - <span data-ttu-id="574a0-124">Codabar</span><span class="sxs-lookup"><span data-stu-id="574a0-124">Codabar</span></span>
    - <span data-ttu-id="574a0-125">Code 39</span><span class="sxs-lookup"><span data-stu-id="574a0-125">Code 39</span></span>
    - <span data-ttu-id="574a0-126">Code 93</span><span class="sxs-lookup"><span data-stu-id="574a0-126">Code 93</span></span>
    - <span data-ttu-id="574a0-127">Code 128</span><span class="sxs-lookup"><span data-stu-id="574a0-127">Code 128</span></span>
    - <span data-ttu-id="574a0-128">EAN-8</span><span class="sxs-lookup"><span data-stu-id="574a0-128">EAN-8</span></span>
    - <span data-ttu-id="574a0-129">EAN-13</span><span class="sxs-lookup"><span data-stu-id="574a0-129">EAN-13</span></span>
    - <span data-ttu-id="574a0-130">ITF-14</span><span class="sxs-lookup"><span data-stu-id="574a0-130">ITF-14</span></span>
    - <span data-ttu-id="574a0-131">البريد الذكي</span><span class="sxs-lookup"><span data-stu-id="574a0-131">Intelligent Mail</span></span>
    - <span data-ttu-id="574a0-132">MSI</span><span class="sxs-lookup"><span data-stu-id="574a0-132">MSI</span></span>
    - <span data-ttu-id="574a0-133">Plessey</span><span class="sxs-lookup"><span data-stu-id="574a0-133">Plessey</span></span>
    - <span data-ttu-id="574a0-134">PDF417</span><span class="sxs-lookup"><span data-stu-id="574a0-134">PDF417</span></span>
    - <span data-ttu-id="574a0-135">UPC-A</span><span class="sxs-lookup"><span data-stu-id="574a0-135">UPC-A</span></span>
    - <span data-ttu-id="574a0-136">UPC-E</span><span class="sxs-lookup"><span data-stu-id="574a0-136">UPC-E</span></span>

- <span data-ttu-id="574a0-137">الأكواد الشريطية ثنائية الأبعاد:</span><span class="sxs-lookup"><span data-stu-id="574a0-137">Two-dimensional bar codes:</span></span>

    - <span data-ttu-id="574a0-138">Aztec</span><span class="sxs-lookup"><span data-stu-id="574a0-138">Aztec</span></span>
    - <span data-ttu-id="574a0-139">مصفوفة البيانات</span><span class="sxs-lookup"><span data-stu-id="574a0-139">Data Matrix</span></span>
    - <span data-ttu-id="574a0-140">شفرة استجابة سريعة (QR)</span><span class="sxs-lookup"><span data-stu-id="574a0-140">QR Code</span></span>

<span data-ttu-id="574a0-141">عندما تقوم بتكوين مصدر بيانات **كود شريطي**، فإنه يمكنك تعريف معلمات عرض معينة يتم استخدامها لإنشاء صورة:</span><span class="sxs-lookup"><span data-stu-id="574a0-141">When you configure a **Barcode** data source, you can define specific rendering parameters that are used to generate an image:</span></span>

- <span data-ttu-id="574a0-142">**العرض** – تحديد عرض الكود الشريطي بالبكسل.</span><span class="sxs-lookup"><span data-stu-id="574a0-142">**Width** – Specify the bar code's width in pixels.</span></span> <span data-ttu-id="574a0-143">وتشير القيمة **0** (صفر) إلى أنه يتم استخدام العرض الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="574a0-143">A value of **0** (zero) indicates that the default width is used.</span></span> <span data-ttu-id="574a0-144">يمكن أن يختلف المعنى بالنسبة للتنسيقات المختلفة.</span><span class="sxs-lookup"><span data-stu-id="574a0-144">The meaning can vary for different formats.</span></span>
- <span data-ttu-id="574a0-145">**الارتفاع** – تحديد ارتفاع الكود الشريطي بالبكسل.</span><span class="sxs-lookup"><span data-stu-id="574a0-145">**Height** – Specify the bar code's height in pixels.</span></span> <span data-ttu-id="574a0-146">وتشير القيمة **0** (صفر) إلى أنه يتم استخدام الارتفاع الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="574a0-146">A value of **0** (zero) indicates that the default height is used.</span></span> <span data-ttu-id="574a0-147">يمكن أن يختلف المعنى بالنسبة للتنسيقات المختلفة.</span><span class="sxs-lookup"><span data-stu-id="574a0-147">The meaning can vary for different formats.</span></span>
- <span data-ttu-id="574a0-148">**الهامش** – حدد حجم هامش الكود الشريطي بالبكسل.</span><span class="sxs-lookup"><span data-stu-id="574a0-148">**Margin** – Specify the size of the bar code's margin in pixels.</span></span> <span data-ttu-id="574a0-149">الهامش هو المنطقة الموجودة على كل جانب من جوانب الكود الشريطي والتي يجب الاحتفاظ بمسحها (المنطقة الهادئة).</span><span class="sxs-lookup"><span data-stu-id="574a0-149">The margin is the area on each side of a bar code that must be kept clear (quiet zone).</span></span> <span data-ttu-id="574a0-150">وتشير القيمة **0** (صفر) إلى أنه يتم استخدام الهامش الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="574a0-150">A value of **0** (zero) indicates that the default margin is used.</span></span> <span data-ttu-id="574a0-151">يمكن أن يختلف المعنى بالنسبة للتنسيقات المختلفة.</span><span class="sxs-lookup"><span data-stu-id="574a0-151">The meaning can vary for different formats.</span></span>
- <span data-ttu-id="574a0-152">**محتوى الإخراج** – قم بتعيين القيمة إلى **نعم** لإنشاء صورة كود شريطي تحتوي على المعلومات المرمزة كنص.</span><span class="sxs-lookup"><span data-stu-id="574a0-152">**Output content** – Set the value to **Yes** to generate a bar code image that contains the encoded information as text.</span></span> <span data-ttu-id="574a0-153">القيمة الافتراضية هي **لا**.</span><span class="sxs-lookup"><span data-stu-id="574a0-153">The default value is **No**.</span></span>
- <span data-ttu-id="574a0-154">**الترميز** – يحدد نوع الحروف التي يتم ترميزها في صورة الكود الشريطي الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="574a0-154">**Encoding** – Specify the type of characters that are encoded in the generated bar code image.</span></span> <span data-ttu-id="574a0-155">افتراضيًا، يتم استخدام الترميز **UTF-8**.</span><span class="sxs-lookup"><span data-stu-id="574a0-155">By default, the **UTF-8** encoding is used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="574a0-156">عندما تقوم بإضافة مصدر بيانات **الكود الشريطي**، فإنه يجب عليك وضعه ضمن عنصر آخر (الحاوية) كعنصر متداخل.</span><span class="sxs-lookup"><span data-stu-id="574a0-156">When you add a new **Barcode** data source, you must place it under another item (container) as a nested element.</span></span>
>
> <span data-ttu-id="574a0-157">عند ربط مصدر بيانات **كود شريطي** بعنصر خلية في تنسيق، ويمثل عنصر الخلية إما عنصر تحكم محتوى Word أو صورة Excel، فإنه يتم تقديم مصدر البيانات في ذلك الربط كوظيفة تحتوي على معلمة واحدة من نوع **السلسلة**.</span><span class="sxs-lookup"><span data-stu-id="574a0-157">When you bind a **Barcode** data source to a cell element in a format, and the cell element represents either a Word content control or an Excel picture, the data source is presented in that binding as a function that has a single parameter of the **String** type.</span></span> <span data-ttu-id="574a0-158">يجب عليك استخدام هذه المعلمة لتحديد النص الذي يجب تحويله إلى صورة كود شريطي والقراءة عند فحص الكود الشريطي الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="574a0-158">You must use this parameter to specify the text that should be transformed into a bar code image and read when a generated bar code is scanned.</span></span>

<span data-ttu-id="574a0-159">لمعرفة المزيد من المعلومات حول هذه الميزة، أكمل الامثلة في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="574a0-159">For more information about this feature, complete the examples in this topic.</span></span>

## <a name="example-generate-a-payment-check-that-contains-a-bar-code-that-encodes-the-payable-amount"></a><span data-ttu-id="574a0-160">مثال: إنشاء شيك دفع يحتوي على كود شريطي يقوم بترميز المبلغ المستحق الدفع</span><span class="sxs-lookup"><span data-stu-id="574a0-160">Example: Generate a payment check that contains a bar code that encodes the payable amount</span></span>

<span data-ttu-id="574a0-161">يوضح هذا المثال كيف يمكن لمستخدم في دور **مسؤول النظام** أو **مستشار وظائف التقارير الإلكترونية** تكوين تنسيق ER يحتوي على قالب يتم استخدامه لإنشاء مستند صادر بتنسيق Excel يحتوي على كود شريطي.</span><span class="sxs-lookup"><span data-stu-id="574a0-161">This example shows how a user in the **System administrator** or **Electronic reporting functional consultant** role can configure an ER format that contains a template that is used to generate an outbound document in Excel format that contains a bar code.</span></span> <span data-ttu-id="574a0-162">وفيما يلي نظرة عامة على الخطوات المضمنة.</span><span class="sxs-lookup"><span data-stu-id="574a0-162">Here is an overview of the steps that are involved.</span></span>

1. <span data-ttu-id="574a0-163">[أكمل المتطلبات الأساسية](#ExamplePrerequisites).</span><span class="sxs-lookup"><span data-stu-id="574a0-163">[Complete the prerequisites](#ExamplePrerequisites).</span></span>
2. <span data-ttu-id="574a0-164">[تنشيط موفر تكوين](#ExampleProvider).</span><span class="sxs-lookup"><span data-stu-id="574a0-164">[Activate a configuration provider](#ExampleProvider).</span></span>
3. <span data-ttu-id="574a0-165">[استيراد حل التقاير الإلكترونية المتوفرة](#ExampleImportSolution).</span><span class="sxs-lookup"><span data-stu-id="574a0-165">[Import the provided ER solution](#ExampleImportSolution).</span></span>
4. <span data-ttu-id="574a0-166">[إنشاء شيك دفع](#ExampleGenerateCheque).</span><span class="sxs-lookup"><span data-stu-id="574a0-166">[Generate a payment check](#ExampleGenerateCheque).</span></span>
5. <span data-ttu-id="574a0-167">[مراجعة شيك دفع تم إنشاؤه](#ExampleReviewGeneratedCheque).</span><span class="sxs-lookup"><span data-stu-id="574a0-167">[Review the generated payment check](#ExampleReviewGeneratedCheque).</span></span>
6. <span data-ttu-id="574a0-168">[تعديل تنسيق حل ER المتوفر](#ExampleModifyFormat).</span><span class="sxs-lookup"><span data-stu-id="574a0-168">[Modify the format of the provided ER solution](#ExampleModifyFormat).</span></span>

    1. <span data-ttu-id="574a0-169">[تطبيق قالب شيك جديد](#ExampleModifyFormatApplyTemplate).</span><span class="sxs-lookup"><span data-stu-id="574a0-169">[Apply a new check template](#ExampleModifyFormatApplyTemplate).</span></span>
    2. <span data-ttu-id="574a0-170">[إضافة مصدر بيانات كود شريطي](#ExampleModifyFormatAddDataSource).</span><span class="sxs-lookup"><span data-stu-id="574a0-170">[Add a new Barcode data source](#ExampleModifyFormatAddDataSource).</span></span>
    3. <span data-ttu-id="574a0-171">[ربط عنصر تنسيق جديد](#ExampleModifyFormatBindFormatElement).</span><span class="sxs-lookup"><span data-stu-id="574a0-171">[Bind a new format element](#ExampleModifyFormatBindFormatElement).</span></span>
    4. <span data-ttu-id="574a0-172">[قم بإتاحة الإصدار الذي تم تعديله لتشغيل الاختبار](#ExampleModifyFormatMakeVersionAvailable).</span><span class="sxs-lookup"><span data-stu-id="574a0-172">[Make the modified version available for test runs](#ExampleModifyFormatMakeVersionAvailable).</span></span>

        1. <span data-ttu-id="574a0-173">[أكمل إصدار التنسيق المعدل](#CompleteToRun).</span><span class="sxs-lookup"><span data-stu-id="574a0-173">[Complete the modified format version](#CompleteToRun).</span></span>
        2. <span data-ttu-id="574a0-174">[اجعل إصدار المسودة متاحًا للاستخدام](#MarkToRun).</span><span class="sxs-lookup"><span data-stu-id="574a0-174">[Make the draft version available for use](#MarkToRun).</span></span>

7. <span data-ttu-id="574a0-175">[إنشاء شيك دفع](#ExampleGenerateCheque2).</span><span class="sxs-lookup"><span data-stu-id="574a0-175">[Generate a payment check](#ExampleGenerateCheque2).</span></span>
8. <span data-ttu-id="574a0-176">[قم بتحويل الشيك الذي تم إنشاؤه إلى PDF](#ExampleConvertToPDF).</span><span class="sxs-lookup"><span data-stu-id="574a0-176">[Convert the generated check to a PDF](#ExampleConvertToPDF).</span></span>

<span data-ttu-id="574a0-177">في هذا المثال، ستستخدم الحل ER المتوفر الذي تم تكوينه لإنشاء شيكات دفع.</span><span class="sxs-lookup"><span data-stu-id="574a0-177">In this example, you will use the provided ER solution that has been configured to generate payment checks.</span></span> <span data-ttu-id="574a0-178">يقوم هذا الحل بإنشاء شيكات الدفع حيث تتم كتابة المبلغ الدائن كرقم وكنص.</span><span class="sxs-lookup"><span data-stu-id="574a0-178">This solution generates payment checks where the payable amount is written both as a number and as text.</span></span> <span data-ttu-id="574a0-179">ستقوم بتعديل حل ER هذا بحيث يتضمن الفحص أيضًا الكود الشريطي الذي تم إنشاؤه حيث يتم ترميز المبلغ الدائن ويمكن قراءته باستخدام الماسح الضوئي للكود الشريطي.</span><span class="sxs-lookup"><span data-stu-id="574a0-179">You will modify this ER solution so that the check also includes a generated bar code where the payable amount is encoded and can be read by using a bar code scanner.</span></span>

<span data-ttu-id="574a0-180">يمكن إكمال الخطوات في شركة **USMF** في Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="574a0-180">The steps can be completed in the **USMF** company in Microsoft Dynamics 365 Finance.</span></span>

### <a name="complete-the-prerequisites"></a><a name="ExamplePrerequisites"></a><span data-ttu-id="574a0-181">إكمال المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="574a0-181">Complete the prerequisites</span></span>

<span data-ttu-id="574a0-182">لإكمال هذا المثال، يجب أن يكون لديك حق الوصول إلى شركة USMF في Finance لأحد الأدوار التالية:</span><span class="sxs-lookup"><span data-stu-id="574a0-182">To complete this example, you must have access to the USMF company in Finance for one of the following roles:</span></span>

- <span data-ttu-id="574a0-183">مستشار وظيفي لإعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="574a0-183">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="574a0-184">مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="574a0-184">System administrator</span></span>

<span data-ttu-id="574a0-185">إذا لم تكن قد أكملت بعد المثال الموجود في [تضمين الصور والأشكال في المستندات التي تقوم بإنشائها باستخدام موضوع ER](electronic-reporting-embed-images-shapes.md)، قم بتنزيل التكوينات التالية لنموذج حل ER.</span><span class="sxs-lookup"><span data-stu-id="574a0-185">If you haven't yet completed the example in the [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md) topic, download the following configurations of the sample ER solution.</span></span>

| <span data-ttu-id="574a0-186">وصف المحتوى</span><span class="sxs-lookup"><span data-stu-id="574a0-186">Content description</span></span>         | <span data-ttu-id="574a0-187">اسم الملف</span><span class="sxs-lookup"><span data-stu-id="574a0-187">File name</span></span>                   |
|-----------------------------|-----------------------------|
| <span data-ttu-id="574a0-188">تكوين نموذج بيانات التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="574a0-188">ER data model configuration</span></span> | <span data-ttu-id="574a0-189">Model for cheques.xml</span><span class="sxs-lookup"><span data-stu-id="574a0-189">Model for cheques.xml</span></span>       |
| <span data-ttu-id="574a0-190">تنسيق تكوين ER</span><span class="sxs-lookup"><span data-stu-id="574a0-190">ER format configuration</span></span>     | <span data-ttu-id="574a0-191">Cheques printing format.xml</span><span class="sxs-lookup"><span data-stu-id="574a0-191">Cheques printing format.xml</span></span> |

<span data-ttu-id="574a0-192">بالإضافة إلى ذلك، قم بتنزيل ملف Excel التالي الذي يحتوي على القالب المعدل الخاص بحل ER المتوفر.</span><span class="sxs-lookup"><span data-stu-id="574a0-192">Additionally, download the following Excel file that contains the modified template for the provided ER solution.</span></span>

| <span data-ttu-id="574a0-193">وصف المحتوى</span><span class="sxs-lookup"><span data-stu-id="574a0-193">Content description</span></span> | <span data-ttu-id="574a0-194">اسم الملف</span><span class="sxs-lookup"><span data-stu-id="574a0-194">File name</span></span>                 |
|---------------------|---------------------------|
| <span data-ttu-id="574a0-195">قالب التقرير</span><span class="sxs-lookup"><span data-stu-id="574a0-195">Report template</span></span>     | <span data-ttu-id="574a0-196">Check template Excel.xlsx</span><span class="sxs-lookup"><span data-stu-id="574a0-196">Check template Excel.xlsx</span></span> |

### <a name="activate-a-configuration-provider"></a><a name="ExampleProvider"></a><span data-ttu-id="574a0-197">تنشيط موفر تكوين</span><span class="sxs-lookup"><span data-stu-id="574a0-197">Activate a configuration provider</span></span>

1. <span data-ttu-id="574a0-198">انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="574a0-198">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="574a0-199">في صفحة **تكوينات الترجمة**، في القسم **موفري التكوين**، تحقق من أنه يتم إدراج [موفر التكوين](general-electronic-reporting.md#Provider) لنموذج الشركة **Litware, Inc.**، وأنه يتم وضع علامة عليه كنشط.</span><span class="sxs-lookup"><span data-stu-id="574a0-199">On the **Localization configurations** page, in the **Configuration providers** section, make sure that the [configuration provider](general-electronic-reporting.md#Provider) for the **Litware, Inc.** sample company is listed, and that it's marked as active.</span></span> <span data-ttu-id="574a0-200">في حالة عدم الإدراج، أو عدم وضع علامة عليه كنشط، اتبع الخطوات الموجودة في الموضوع [إنشاء موفر تكوين ووضع علامة عليه على أنه نشط.](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="574a0-200">If it isn't listed, or if it isn't marked as active, follow the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) topic.</span></span>

![تعيين نموذج الشركة إلى نشط في صفحة تكوينات الترجمة](./media/er-barcode-data-source-active-provider.png)

### <a name="import-the-provided-er-solution"></a><a name="ExampleImportSolution"></a><span data-ttu-id="574a0-202">استيراد حل التقاير الإلكترونية المتوفرة</span><span class="sxs-lookup"><span data-stu-id="574a0-202">Import the provided ER solution</span></span>

1. <span data-ttu-id="574a0-203">انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="574a0-203">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="574a0-204">في الصفحة **تكوينات الترجمة**، في قسم **التكوينات**، حدد تجانب **تكوينات إعداد التقارير** .</span><span class="sxs-lookup"><span data-stu-id="574a0-204">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="574a0-205">في صفحة **التكوينات**، في حالة عدم توفر تكوين **نموذج للشيكات** في شجرة التكوين، ابتع هذه الخطوات لاستيراد تكوين نموذج بيانات التقارير الإلكترونية:</span><span class="sxs-lookup"><span data-stu-id="574a0-205">On the **Configurations** page, if the **Model for cheques** configuration isn't available in the configuration tree, follow these steps to import the ER data model configuration:</span></span>

    1. <span data-ttu-id="574a0-206">في جزء الإجراءات، حدد **التبادل** \> **تحميل من ملف XML**.</span><span class="sxs-lookup"><span data-stu-id="574a0-206">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
    2. <span data-ttu-id="574a0-207">في مربع الحوار، حدد **استعراض**، وابحث عن ملف **Model for cheques.xml**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="574a0-207">In the dialog box, select **Browse**, find and select the **Model for cheques.xml** file, and then select **OK**.</span></span>

4. <span data-ttu-id="574a0-208">في حالة عدم توفر التكوين **تنسيق طباعة الشيكات** في شجرة التكوين، اتبع هذه الخطوات لاستيراد تكوين تنسيق التقارير الإلكترونية:</span><span class="sxs-lookup"><span data-stu-id="574a0-208">If the **Cheques printing format** configuration isn't available in the configuration tree, follow these steps to import the ER format configuration:</span></span>

    1. <span data-ttu-id="574a0-209">في جزء الإجراءات، حدد **التبادل** \> **تحميل من ملف XML**.</span><span class="sxs-lookup"><span data-stu-id="574a0-209">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
    2. <span data-ttu-id="574a0-210">في مربع الحوار، حدد **استعراض**، ابحث وحدد عن ملف **Cheques printing format.xml**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="574a0-210">In the dialog box, select **Browse**, find and select the **Cheques printing format.xml** file, and then select **OK**.</span></span>

5. <span data-ttu-id="574a0-211">في شجرة التكوين، قم بتوسيع **نموذج للشيكات**.</span><span class="sxs-lookup"><span data-stu-id="574a0-211">In the configuration tree, expand **Model for cheques**.</span></span>
6. <span data-ttu-id="574a0-212">راجع قائمة تكوينات إعداد التقارير الإلكترونية المستوردة في شجرة التكوين.</span><span class="sxs-lookup"><span data-stu-id="574a0-212">Review the list of imported ER configurations in the configuration tree.</span></span>

### <a name="generate-a-payment-check"></a><a name="ExampleGenerateCheque"></a><span data-ttu-id="574a0-213">إنشاء شيك دفع</span><span class="sxs-lookup"><span data-stu-id="574a0-213">Generate a payment check</span></span>

1. <span data-ttu-id="574a0-214">انتقل إلى **إدارة النقد والبنوك** \> **الحسابات البنكية** \> **الحسابات البنكية**.</span><span class="sxs-lookup"><span data-stu-id="574a0-214">Go to **Cash and bank management** \> **Bank accounts** \> **Bank accounts**.</span></span>
2. <span data-ttu-id="574a0-215">في الصفحة **الحسابات البنكية**، حدد الحساب **USMF OPER**.</span><span class="sxs-lookup"><span data-stu-id="574a0-215">On the **Bank accounts** page, select the **USMF OPER** account.</span></span>
3. <span data-ttu-id="574a0-216">في صفحة تفاصيل الحساب البنكي، في جزء الإجراء، في علامة التبويب **إعداد**، في المجموعة **تخطيط**، حدد **شيك**.</span><span class="sxs-lookup"><span data-stu-id="574a0-216">On the bank account details page, on the Action Pane, on the **Set up** tab, in the **Layout** group, select **Check**.</span></span>
4. <span data-ttu-id="574a0-217">في الصفحة **مخطط الشيكات**، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="574a0-217">On the **Check layout** page, select **Edit**.</span></span>
5. <span data-ttu-id="574a0-218">في علامة التبويب السريعة **عام**، قم بتعيين خيار **تنسيق التصدير الإلكتروني العام‬** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="574a0-218">On the **General** FastTab, set the **Generic electronic Export format** option to **Yes**.</span></span>
6. <span data-ttu-id="574a0-219">في الحقل **تكوين التنسيق التصدير**، حدد تنسيق التقرير الإلكتروني **تنسيق طباعة الشيكات** الذي الذي قمت باستيراده سابقًا.</span><span class="sxs-lookup"><span data-stu-id="574a0-219">In the **Export format configuration** field, select the **Cheques printing format** ER format that you imported earlier.</span></span>
7. <span data-ttu-id="574a0-220">في جزء الإجراءات، حدد **اختبار طباعة**.</span><span class="sxs-lookup"><span data-stu-id="574a0-220">On the Action Pane, select **Print test**.</span></span>
8. <span data-ttu-id="574a0-221">في مربع الحوار، قم بتعيين خيار **تنسيق الشيك القابل للتداول** إلى **نعم**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="574a0-221">In the dialog box, set the **Negotiable check format** option to **Yes**, and then select **OK**.</span></span>

    ![مخطط الشيكات - مربع حوار اختبار الطباعة](./media/er-barcode-data-source-check-layout.png)

### <a name="review-the-generated-payment-check"></a><a name="ExampleReviewGeneratedCheque"></a><span data-ttu-id="574a0-223">مراجعة شيك دفع تم إنشاؤه</span><span class="sxs-lookup"><span data-stu-id="574a0-223">Review the generated payment check</span></span>

- <span data-ttu-id="574a0-224">افتح الشيك الذي تم إنشاؤه في Excel.</span><span class="sxs-lookup"><span data-stu-id="574a0-224">Open the generated check in Excel.</span></span>
2. <span data-ttu-id="574a0-225">راجع الشيك الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="574a0-225">Review the generated check.</span></span>

    ![شيك الدفع الذي تم إنشاؤه في Excel](./media/er-barcode-data-source-cheque1.png)

### <a name="modify-the-format-of-the-provided-er-solution"></a><a name="ExampleModifyFormat"></a><span data-ttu-id="574a0-227">تعديل تنسيق حل التقرير الإلكتروني المتوفر</span><span class="sxs-lookup"><span data-stu-id="574a0-227">Modify the format of the provided ER solution</span></span>

#### <a name="apply-a-new-check-template"></a><a name="ExampleModifyFormatApplyTemplate"></a><span data-ttu-id="574a0-228">تطبيق قالب شيك جديد</span><span class="sxs-lookup"><span data-stu-id="574a0-228">Apply a new check template</span></span>

<span data-ttu-id="574a0-229">يمكنك استخدام تطبيق سطح مكتب Excel لفتح الملف **Cheque template Excel.xlsx** الذي قمت باستيراده سابقًا.</span><span class="sxs-lookup"><span data-stu-id="574a0-229">You can use the Excel desktop application to open the **Cheque template Excel.xlsx** file that you imported earlier.</span></span> <span data-ttu-id="574a0-230">لاحظ أن هذا القالب يختلف عن القالب الذي استخدمته لإنشاء شيك دفع في حل التقرير الإلكتروني المتوفر.</span><span class="sxs-lookup"><span data-stu-id="574a0-230">Notice that this template differs from the template that you used to generate a payment check in the provided ER solution.</span></span> <span data-ttu-id="574a0-231">بالإضاف إلى ذلك، يتضمن العنصر **AmountBarcode** لصورة الكود الشريطي.</span><span class="sxs-lookup"><span data-stu-id="574a0-231">In addition, it includes an **AmountBarcode** element for the bar code image.</span></span>

![عنصر AmountBarcode في قالب Excel](./media/er-barcode-data-source-cheque2.png)

<span data-ttu-id="574a0-233">يجب الآن تعديل حل التقرير الإلكتروني ، ثم [إعادة تطبيق](modify-electronic-reporting-format-reapply-excel-template.md) القالب المعدل.</span><span class="sxs-lookup"><span data-stu-id="574a0-233">You must now modify the ER solution and then [reapply](modify-electronic-reporting-format-reapply-excel-template.md) the modified template.</span></span>

1. <span data-ttu-id="574a0-234">انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="574a0-234">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="574a0-235">في الصفحة **تكوينات الترجمة**، في قسم **التكوينات**، حدد **تكوينات إعداد التقارير** .</span><span class="sxs-lookup"><span data-stu-id="574a0-235">On the **Localization configurations** page, in the **Configurations** section, select **Reporting configurations**.</span></span>
3. <span data-ttu-id="574a0-236">في الصفحة **تكوينات**، في شجرة التكوين، قم بتوسيع **نموذج للشيكات**، وحدد **تنسيق طباعة الشيكات**.</span><span class="sxs-lookup"><span data-stu-id="574a0-236">On the **Configurations** page, in the configuration tree, expand **Model for cheques**, and select **Cheques printing format**.</span></span>
4. <span data-ttu-id="574a0-237">في جزء الإجراءات، حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="574a0-237">On the Action Pane, select **Designer**.</span></span>
5. <span data-ttu-id="574a0-238">في مصمم عمليات التقرير الإلكتروني، حدد علامة التبويب **تعيين** على الجانب الأيمن للصفحة، ثم، في جزء شجرة التنسيق على الجانب الأيسر، ثم حدد **توسيع/طي**.</span><span class="sxs-lookup"><span data-stu-id="574a0-238">In the ER Operations designer, select the **Mapping** tab on the right side of the page, and then, in the format tree pane on the left, select **Expand/collapse**.</span></span>
6. <span data-ttu-id="574a0-239">لاحظ أنه يتم ربط كافة عناصر تنسيق الخلايا بمصادر البيانات المناسبة.</span><span class="sxs-lookup"><span data-stu-id="574a0-239">Notice that all cell format elements are bound to the appropriate data sources.</span></span>

    ![ربط عناصر تنسيق الخلية بمصادر البيانات في مصمم عمليات التقارير الإلكترونية](./media/er-barcode-data-source-cells-bound.png)

7. <span data-ttu-id="574a0-241">حدد علامة التبويب **تنسيق** على الجانب الأيمن من الصفحة.</span><span class="sxs-lookup"><span data-stu-id="574a0-241">Select the **Format** tab on the right side of the page.</span></span>
8. <span data-ttu-id="574a0-242">في جزء الإجراء، حدد علامة الحذف (**...**)، ثم حدد **استيراد**.</span><span class="sxs-lookup"><span data-stu-id="574a0-242">On the Action Pane, select the ellipsis (**...**), and then select **Import**.</span></span>
9. <span data-ttu-id="574a0-243">في المجموعة **استيراد**، حدد **تحديث من Excel**، ثم حدد **تحديث القالب**.</span><span class="sxs-lookup"><span data-stu-id="574a0-243">In the **Import** group, select **Update from Excel**, and then select **Update template**.</span></span>
10. <span data-ttu-id="574a0-244">في مربع الحوار، استعرض الملف **Cheque template Excel.xlsx** الذي يتم حفظه على جهاز الكمبيوتر الخاص بك، وحدده، ثم حدد **موافق** للتأكد من أنه يجب تطبيق القالب المحدد.</span><span class="sxs-lookup"><span data-stu-id="574a0-244">In the dialog box, browse to the **Cheque template Excel.xlsx** file that is saved on your computer, select it, and then select **OK** to confirm that the selected template should be applied.</span></span>
11. <span data-ttu-id="574a0-245">حدد علامة التبويب **تعيين** على الجانب الأيمن للصفحة، ثم، في جزء شجرة التنسيق على الجانب الأيسر، ثم حدد **توسيع/طي**.</span><span class="sxs-lookup"><span data-stu-id="574a0-245">Select the **Mapping** tab on the right side of the page, and then, in the format tree pane on the left, select **Expand/collapse**.</span></span>
12. <span data-ttu-id="574a0-246">لاحظ أنه تتم إضافة عنصر الخلية **AmountBarcode** إلى التنسيق.</span><span class="sxs-lookup"><span data-stu-id="574a0-246">Notice that the **AmountBarcode** cell element has been added to the format.</span></span> <span data-ttu-id="574a0-247">يتم ربط هذا العنصر بالعنصر **AmountBarcode** الذي تمت إضافته إلى قالب Excel المعدل كعنصر نائب لصورة الكود الشريطي.</span><span class="sxs-lookup"><span data-stu-id="574a0-247">This element is associated with the **AmountBarcode** element that has been added to the modified Excel template as a placeholder for a bar code image.</span></span>

    ![عنصر AmountBarcode المُضاف إلى التنسيق في مصمم عمليات التقارير الإلكترونية](./media/er-barcode-data-source-cell-added.png)

#### <a name="add-a-new-barcode-data-source"></a><a name="ExampleModifyFormatAddDataSource"></a><span data-ttu-id="574a0-249">إضافة مصدر بيانات كود شريطي جديد</span><span class="sxs-lookup"><span data-stu-id="574a0-249">Add a new Barcode data source</span></span>

<span data-ttu-id="574a0-250">بعد ذلك، يجب إضافة مصدر بيانات جديد لنوع **الكود الشريطي**.</span><span class="sxs-lookup"><span data-stu-id="574a0-250">Next, you must add a new data source of the **Barcode** type.</span></span>

1. <span data-ttu-id="574a0-251">في مصمم عمليات التقارير الإلكترونية، ضمن علامة التبويب **تعيين** على الجانب الأيمن من الصفحة، حدد مصدر بيانات **طباعة**.</span><span class="sxs-lookup"><span data-stu-id="574a0-251">In the ER Operations designer, on the **Mapping** tab on the right side of the page, select the **print** data source.</span></span>
2. <span data-ttu-id="574a0-252">حدد **إضافة**، ثم، في المجموعة  **الوظائف**، حدد نوع مصدر البيانات **الكود الشريطي**.</span><span class="sxs-lookup"><span data-stu-id="574a0-252">Select **Add**, and then, in the **Functions** group, select the **Barcode** data source type.</span></span>

    ![تحديد نوع مصدر بيانات الكود الشريطي](./media/er-barcode-data-source-add.png)

3. <span data-ttu-id="574a0-254">في مربع الحوار، في الحقل **الاسم**، أدخل **الكود الشريطي**.</span><span class="sxs-lookup"><span data-stu-id="574a0-254">In the dialog box, in the **Name** field, enter **barcode**.</span></span>
4. <span data-ttu-id="574a0-255">في **تنسيق الكود الشريطي**، حدد **الكود 128**.</span><span class="sxs-lookup"><span data-stu-id="574a0-255">In the **Barcode format**, select **Code 128**.</span></span>
5. <span data-ttu-id="574a0-256">في الحقل **العرض**، أدخل **500**.</span><span class="sxs-lookup"><span data-stu-id="574a0-256">In the **Width** field, enter **500**.</span></span>
6. <span data-ttu-id="574a0-257">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="574a0-257">Select **OK**.</span></span>

    ![مربع حوار خصائص مصدر البيانات](./media/er-barcode-data-source-add2.png)

#### <a name="bind-a-new-format-element"></a><a name="ExampleModifyFormatBindFormatElement"></a><span data-ttu-id="574a0-259">ربط عنصر تنسيق جديد</span><span class="sxs-lookup"><span data-stu-id="574a0-259">Bind a new format element</span></span>

<span data-ttu-id="574a0-260">بعد ذلك، يجب ربط عنصر التنسيق الجديد بمصدر البيانات الذي قمت بإضافته.</span><span class="sxs-lookup"><span data-stu-id="574a0-260">Next, you must bind the new format element to the data source that you just added.</span></span>

1. <span data-ttu-id="574a0-261">في مصمم عمليات التقارير الإلكترونية، ضمن علامة التبويب **تعيين** على الجانب الأيمن من الصفحة، حدد مصدر البيانات **طباعة\\الكود الشريطي**.</span><span class="sxs-lookup"><span data-stu-id="574a0-261">In the ER Operations designer, on the **Mapping** tab on the right side of the page, select the **print\\barcode** data source.</span></span>
2. <span data-ttu-id="574a0-262">في جزء شجرة التنسيق على اليسار، حدد عنصر الخلية **AmountBarcode**، ثم حدد **ربط**.</span><span class="sxs-lookup"><span data-stu-id="574a0-262">In the format tree pane on the left, select the **AmountBarcode** cell element, and then select **Bind**.</span></span>
3. <span data-ttu-id="574a0-263">في جزء الإجراءات، حدد **عرض التفاصيل**.</span><span class="sxs-lookup"><span data-stu-id="574a0-263">On the Action Pane, select **Show details**.</span></span>
4. <span data-ttu-id="574a0-264">لاحظ أنه نظرًا لأنه يتم تمثيل مصدر بيانات **الكود الشريطي** في الربط كوظيفة تحتوي على معلمة واحدة، فإنه تم أخذ اسم عنصر التنسيق المنضم تلقائيًا كوسيطة لتلك المعلمة.</span><span class="sxs-lookup"><span data-stu-id="574a0-264">Notice that, because the **Barcode** data source is represented in the binding as a function that contains a single parameter, the name of the bound format element has been automatically taken as the argument of that parameter.</span></span>

    ![تفاصيل مصدر بيانات الكود الشريطي في مصمم عمليات التقارير الإلكترونية](./media/er-barcode-data-source-bind1.png)

5. <span data-ttu-id="574a0-266&quot;>حدد **تحرير المعادلة** لضبط الربط.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;574a0-266&quot;>Select **Edit formula** to adjust the binding.</span></span>

    <span data-ttu-id=&quot;574a0-267&quot;>إنك لا تريد أن يتم إرجاع اسم عنصر الخلية.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;574a0-267&quot;>You don't want the name of the cell element to be returned.</span></span> <span data-ttu-id=&quot;574a0-268&quot;>وبالتالي، يجب عليك تكوين تعبير يرجع النص الذي يحتوي على المبلغ الدائن للشيك الحالي.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;574a0-268&quot;>Therefore, you must configure an expression that returns text that contains the payable amount of the current check.</span></span> <span data-ttu-id=&quot;574a0-269&quot;>نظرًا لأن نطاق **ChequeLines** مرتبط بـ **model.cheques**، يتوفر المبلغ الدائن للشيك الحالي في الحقل **model.cheques.attributes.amount** لنوع البيانات **فعلي**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;574a0-269&quot;>Because the parent **ChequeLines** range is bound to the **model.cheques** data source, the payable amount of the current check is available in the **model.cheques.attributes.amount** field of the **Real** data type.</span></span>

6. <span data-ttu-id=&quot;574a0-270&quot;>في الحقل **معادلة**، أدخل **print.barcode(NUMBERFORMAT(@.attributes.amount, &quot;F2"))**.</span><span class="sxs-lookup"><span data-stu-id="574a0-270">In the **Formula** field, enter **print.barcode(NUMBERFORMAT(@.attributes.amount, "F2"))**.</span></span>
7. <span data-ttu-id="574a0-271">حدد **حفظ**، ثم أغلق [مصمم معادلة التقارير الإلكترونية](general-electronic-reporting-formula-designer.md).</span><span class="sxs-lookup"><span data-stu-id="574a0-271">Select **Save**, and then close the [ER Formula designer](general-electronic-reporting-formula-designer.md).</span></span>
8. <span data-ttu-id="574a0-272">لاحظ أنه تم تعديل الربط.</span><span class="sxs-lookup"><span data-stu-id="574a0-272">Notice that the binding has been adjusted.</span></span>

    ![الربط المعدل في مصمم العمليات التقارير الإلكترونية](./media/er-barcode-data-source-bind2.png)

9. <span data-ttu-id="574a0-274">حدد **حفظ**، ثم أغلق مصمم عمليات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="574a0-274">Select **Save**, and then close the ER Operations designer.</span></span>

#### <a name="make-the-modified-version-available-for-test-runs"></a><a name="ExampleModifyFormatMakeVersionAvailable"></a><span data-ttu-id="574a0-275">القيام بالإصدار المعدل المتاحة لتشغيل الاختبار</span><span class="sxs-lookup"><span data-stu-id="574a0-275">Make the modified version available for test runs</span></span>

<span data-ttu-id="574a0-276">افتراضيًا، يتم استخدام الإصدارات التي تكون حالتها **مكتمل** و **مشترك** فقط عند تشغيل تنسيق التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="574a0-276">By default, the only versions that have a status of **Completed** and **Shared** are used when you run an ER format.</span></span>

<span data-ttu-id="574a0-277">إذا قمت بإنهاء التغييرات الخاصة بك، فإنه يمكنك إكمال عملك مع إصدار المسودة الحالي وتوفير التغييرات الخاصة بك للاستخدام.</span><span class="sxs-lookup"><span data-stu-id="574a0-277">If you've finalized your changes, you can complete your work with the current draft version and make your changes available for use.</span></span> <span data-ttu-id="574a0-278">للحصول على التعليمات، راجع القسم [إكمال إصدار التنسيق المعدل](#CompleteToRun) الذي يليه.</span><span class="sxs-lookup"><span data-stu-id="574a0-278">For instructions, see the [Complete the modified format version](#CompleteToRun) section that follows.</span></span>

<span data-ttu-id="574a0-279">إذا كنت ترغب في متابعة العمل مع إصدار المسودة الحالي، ولكن يجب عليك استخدامه لإصدار الشيكات، يجب عليك تحديد ما إذا كنت ترغب في استخدام إصدار المسودة من التنسيق لتنفيذه بشكل صريح.</span><span class="sxs-lookup"><span data-stu-id="574a0-279">If you want to continue to work with the current draft version, but you have to use it to generate checks, you must explicitly specify that you want to use the draft version of the format for execution.</span></span> <span data-ttu-id="574a0-280">للحصول على الإرشادات، راجع القسم [جعل إصدار المسودة متاحًا للاستخدام](#MarkToRun).</span><span class="sxs-lookup"><span data-stu-id="574a0-280">For instructions, see the [Make the draft version available for use](#MarkToRun) section.</span></span>

##### <a name="complete-the-modified-format-version"></a><a name="CompleteToRun"></a><span data-ttu-id="574a0-281">إكمال إصدار التنسيق المعدل</span><span class="sxs-lookup"><span data-stu-id="574a0-281">Complete the modified format version</span></span>

1. <span data-ttu-id="574a0-282">انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="574a0-282">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="574a0-283">في الصفحة **تكوينات الترجمة**، في قسم **التكوينات**، حدد **تكوينات إعداد التقارير** .</span><span class="sxs-lookup"><span data-stu-id="574a0-283">On the **Localization configurations** page, in the **Configurations** section, select **Reporting configurations**.</span></span>
3. <span data-ttu-id="574a0-284">في الصفحة **تكوينات**، في شجرة التكوين، قم بتوسيع **نموذج للشيكات**، وحدد **تنسيق طباعة الشيكات**.</span><span class="sxs-lookup"><span data-stu-id="574a0-284">On the **Configurations** page, in the configuration tree, expand **Model for cheques**, and select **Cheques printing format**.</span></span>
4. <span data-ttu-id="574a0-285">في علامة التبويب السريعة **الإصدارات**، حدد السجل الذي بحالة **مسودة**.</span><span class="sxs-lookup"><span data-stu-id="574a0-285">On the **Versions** FastTab, select the record that has a status of **Draft**.</span></span>
5. <span data-ttu-id="574a0-286">حدد **حالة التغيير**، ثم حدد **إكمال**.</span><span class="sxs-lookup"><span data-stu-id="574a0-286">Select **Change status**, and then select **Complete**.</span></span>
6. <span data-ttu-id="574a0-287">في مربع الحوار، حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="574a0-287">In the dialog box, select **OK**.</span></span>

<span data-ttu-id="574a0-288">يتم تغيير حالة الإصدار الحالي من **المسودة** إلى **مكتمل**، يتم إنشاء إصدار جديد به حالة **مسودة**.</span><span class="sxs-lookup"><span data-stu-id="574a0-288">The status of the current version is changed from **Draft** to **Completed**, and a new version that has a status of **Draft** is created.</span></span> <span data-ttu-id="574a0-289">يمكنك استخدام إصدار المسودة الجديد هذا لتطبيق تغييرات إضافية.</span><span class="sxs-lookup"><span data-stu-id="574a0-289">You can use this new draft version to apply additional changes.</span></span>

##### <a name="make-the-draft-version-available-for-use"></a><a name="MarkToRun"></a><span data-ttu-id="574a0-290">إتاحة إصدار المسودة للاستخدام</span><span class="sxs-lookup"><span data-stu-id="574a0-290">Make the draft version available for use</span></span>

1. <span data-ttu-id="574a0-291">انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="574a0-291">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="574a0-292">في الصفحة **تكوينات الترجمة**، في قسم **التكوينات**، حدد **تكوينات إعداد التقارير** .</span><span class="sxs-lookup"><span data-stu-id="574a0-292">On the **Localization configurations** page, in the **Configurations** section, select **Reporting configurations**.</span></span>
3. <span data-ttu-id="574a0-293">في صفحة **التكوينات**، في جزء الإجراءات، في علامة التبويب **التكوينات**، في مجموعة **الإعدادات المتقدمة**، حدد **معلمات المستخدمين**.</span><span class="sxs-lookup"><span data-stu-id="574a0-293">On the **Configurations** page, on the Action Pane, in the **Configurations** tab, in the **Advance settings** group, select **User parameters**.</span></span>
4. <span data-ttu-id="574a0-294">في مربع الحوار، قم بتعيين الخيارات **تشغيل الإعداد** إلى **نعم**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="574a0-294">In the dialog box, set the **Run setting** options to **Yes**, and then select **OK**.</span></span>
5. <span data-ttu-id="574a0-295">في شجرة التكوين، قم بتوسيع **نموذج للشيكات**، حدد **تنسيق طباعة الشيكات**.</span><span class="sxs-lookup"><span data-stu-id="574a0-295">In the configuration tree, expand **Model for cheques**, and select **Cheques printing format**.</span></span>
6. <span data-ttu-id="574a0-296">عيّن الخيار **تشغيل المسودة** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="574a0-296">Set the **Run draft** option to **Yes**.</span></span>
7. <span data-ttu-id="574a0-297">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="574a0-297">Select **Save**.</span></span>

<span data-ttu-id="574a0-298">يتم وضع علامة على إصدار المسودة للتنسيق المحدد على أنه متوفر للاستخدام عند تشغيل التنسيق المحدد.</span><span class="sxs-lookup"><span data-stu-id="574a0-298">The draft version of the selected format is marked as available for use when the selected format is run.</span></span>

### <a name="generate-a-payment-check"></a><a name="ExampleGenerateCheque2"></a><span data-ttu-id="574a0-299">إنشاء شيك دفع</span><span class="sxs-lookup"><span data-stu-id="574a0-299">Generate a payment check</span></span>

1. <span data-ttu-id="574a0-300">انتقل إلى **إدارة النقد والبنوك** \> **الحسابات البنكية** \> **الحسابات البنكية**.</span><span class="sxs-lookup"><span data-stu-id="574a0-300">Go to **Cash and bank management** \> **Bank accounts** \> **Bank accounts**.</span></span>
2. <span data-ttu-id="574a0-301">في الصفحة **الحسابات البنكية**، حدد الحساب **USMF OPER**.</span><span class="sxs-lookup"><span data-stu-id="574a0-301">On the **Bank accounts** page, select the **USMF OPER** account.</span></span>
3. <span data-ttu-id="574a0-302">في صفحة تفاصيل الحساب البنكي، في جزء الإجراء، في علامة التبويب **إعداد**، في المجموعة **تخطيط**، حدد **شيك**.</span><span class="sxs-lookup"><span data-stu-id="574a0-302">On the bank account details page, on the Action Pane, on the **Set up** tab, in the **Layout** group, select **Check**.</span></span>
4. <span data-ttu-id="574a0-303">في الصفحة **مخطط الشيكات**، في جزء الإجراء، حدد **طباعة الاختبار**.</span><span class="sxs-lookup"><span data-stu-id="574a0-303">On the **Check layout** page, on the Action Pane, select **Print test**.</span></span>
5. <span data-ttu-id="574a0-304">في مربع الحوار، قم بتعيين الخيار **تنسيق الشيك القابل للتداول** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="574a0-304">In the dialog box, set the **Negotiable check format** option to **Yes**.</span></span>
6. <span data-ttu-id="574a0-305">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="574a0-305">Select **OK**.</span></span>
7. <span data-ttu-id="574a0-306">راجع الشيك الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="574a0-306">Review the generated check.</span></span> <span data-ttu-id="574a0-307">لاحظ أنه قد تم إنشاء كود شريطي لترميز المبلغ الدائن الخاص بالشيك.</span><span class="sxs-lookup"><span data-stu-id="574a0-307">Notice that a bar code has been generated to encode the payable amount of the check.</span></span>

    ![شيك الدفع الذي تم إنشاؤه باستخدام الكود الشريطي في Excel](./media/er-barcode-data-source-cheque3.png)

> [!IMPORTANT]
> <span data-ttu-id="574a0-309">يتم طرح استثناء إذا كانت وسيطة مصدر بيانات **الكود الشريطي** لا تتوافق مع المتطلبات المناسبة المحددة لتنسيق الكود الشريطي.</span><span class="sxs-lookup"><span data-stu-id="574a0-309">An exception is thrown if the argument of a **Barcode** data source doesn't comply with the appropriate requirements that are specific to the bar code format.</span></span> <span data-ttu-id="574a0-310">على سبيل المثال، عندما يتم استدعاء مصدر بيانات **الكود الشريطي** لإنشاء كود شريطي [EAN-8](https://wikipedia.org/wiki/EAN-8) للنص المقدم، يتم عرض استثناء إذا كان طول النص يتجاوز سبعة أحرف.</span><span class="sxs-lookup"><span data-stu-id="574a0-310">For example, when the **Barcode** data source is called to generate an [EAN-8](https://wikipedia.org/wiki/EAN-8) bar code for the provided text, an exception is thrown if the length of the text exceeds seven characters.</span></span>

### <a name="convert-the-generated-check-to-a-pdf"></a><a name="ExampleConvertToPDF"></a><span data-ttu-id="574a0-311">تحويل الشيك الذي تم إنشاؤه إلى PDF</span><span class="sxs-lookup"><span data-stu-id="574a0-311">Convert the generated check to a PDF</span></span>

<span data-ttu-id="574a0-312">كما هو موضح في الموضوع [إنشاء نماذج فاتورة ذات نص حر](er-generate-printable-fti-forms.md#finland)، يمكنك استخدام خط خاص لإنتاج الأكواد الشريطية في المستند الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="574a0-312">As described in the [Generate printable FTI forms](er-generate-printable-fti-forms.md#finland) topic, you can use a special font to produce bar codes in a generated document.</span></span> <span data-ttu-id="574a0-313">في هذه الحالة، قد تعتمد التحويلات الإضافية للمستند الذي تم إنشاؤه على توفر ذلك الخط في بيئة التحويل.</span><span class="sxs-lookup"><span data-stu-id="574a0-313">In this case, additional transformations of the generated document might depend on the availability of that font in the transformation environment.</span></span> <span data-ttu-id="574a0-314">على سبيل المثال، إذا حاولت تحويل وثيقة إلى تنسيق PDF أو معاينتها في بيئة لا يكون الخط فيها مفقودًا، فإن الأكواد الشريطية لن يتم عرضها بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="574a0-314">For example, if you try to convert a document to PDF format or preview it in an environment where the font is missing, bar codes won't be rendered correctly.</span></span>

<span data-ttu-id="574a0-315">ومع ذلك، عندما تقوم باستخدام مصدر بيانات **الكود الشريطي** لإنتاج الأكواد الشريطية، لا يعتمد عرض تلك الرموز الشريطية على أي خط.</span><span class="sxs-lookup"><span data-stu-id="574a0-315">However, when you use the **Barcode** data source to produce bar codes, the rendering of those bar codes doesn't depend on any font.</span></span> <span data-ttu-id="574a0-316">لذلك، يمكنك بسهولة تحويل المستندات التي تحتوي على أكواد شريطية إلى تنسيق PDF.</span><span class="sxs-lookup"><span data-stu-id="574a0-316">Therefore, you can easily convert documents that contain the bar codes to PDF format.</span></span> <span data-ttu-id="574a0-317">تبين الرسوم التوضيحية التالية معاينة شيك الدفع الذي تم إنشاؤه أنه تم [تحويل](electronic-reporting-destinations.md#OutputConversionToPDF) إلى ملف PDF، استنادًا إلى إعداد وجهة التقارير الإلكترونية [المكونة](electronic-reporting-destinations.md).</span><span class="sxs-lookup"><span data-stu-id="574a0-317">The following illustration shows the preview of a generated payment check that has been [converted](electronic-reporting-destinations.md#OutputConversionToPDF) to a PDF, based on the setting of the configured ER [destination](electronic-reporting-destinations.md).</span></span>

![معاينة ملف PDF الخاص بشيك الدفع](./media/er-barcode-data-source-cheque4.png)

## <a name="limitations"></a><span data-ttu-id="574a0-319">قيود</span><span class="sxs-lookup"><span data-stu-id="574a0-319">Limitations</span></span>

> [!NOTE]
> <span data-ttu-id="574a0-320">تحتوي بعض أنواع الأكواد الشريطية التي يتم إنشاؤها على نسبة أبعاد ثابتة.</span><span class="sxs-lookup"><span data-stu-id="574a0-320">Some types of bar codes that are generated have a fixed aspect ratio.</span></span> <span data-ttu-id="574a0-321">يكون هذا السلوك مفيدًا إذا قمت بتشغيل الميزة **تمكين استخدام مكتبة EPPlus في إطار عمل التقارير الإلكترونية** للعمل باستخدام مستندات Excel في التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="574a0-321">This behavior makes sense if you've turned on the **Enable usage of EPPlus library in Electronic reporting framework** feature to work with Excel documents in ER.</span></span> <span data-ttu-id="574a0-322">في تلك الحالة، يتم إدخال صورة في عنصر نائب بنسبة العرض إلى الارتفاع المؤمنة.</span><span class="sxs-lookup"><span data-stu-id="574a0-322">In that case, an image is entered into a placeholder that has a locked aspect ratio.</span></span> <span data-ttu-id="574a0-323">وبالتالي، عندما تتوافق أبعاد العنصر النائب في أحد القوالب مع نسبة العرض إلى الارتفاع لصورة تم إدخالها، قد يتم تغيير حجم صورة حقيقية في مستند تم إنشائها للحفاظ على نسبة العرض إلى الارتفاع المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="574a0-323">Therefore, when the dimensions of a placeholder in a template correspond to the ratio of an image that is entered, a real picture in a generated document might be resized to maintain the required aspect ratio.</span></span> <span data-ttu-id="574a0-324">لمنع تغيير حجم الصورة، استخدم عنصرًا نائبًا له نسبة العرض إلى الارتفاع المتوقعة.</span><span class="sxs-lookup"><span data-stu-id="574a0-324">To prevent picture resizing, use a placeholder that has an expected aspect ratio.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="574a0-325">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="574a0-325">Additional resources</span></span>

- [<span data-ttu-id="574a0-326">نظرة عامة حول التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="574a0-326">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="574a0-327">وجهات إعداد التقارير الإلكترونية‬</span><span class="sxs-lookup"><span data-stu-id="574a0-327">Electronic Reporting destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="574a0-328">لغة تركيبة التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="574a0-328">Electronic reporting formula language</span></span>](er-formula-language.md)
- [<span data-ttu-id="574a0-329">وظيفة NUMBERFORMAT</span><span class="sxs-lookup"><span data-stu-id="574a0-329">NUMBERFORMAT function</span></span>](er-functions-text-numberformat.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]