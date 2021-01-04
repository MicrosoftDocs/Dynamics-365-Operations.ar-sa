---
title: تقسيم ملفات XML التي تم إنشاؤها استنادًا إلى حجم الملف وكمية المحتوى
description: يقدم هذا الموضوع معلومات عن كيفية تقسم الملفات المنشأة حسب حجم الملف وكمية عنصر المحتوى.
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: d60266aba42f502e7707bdace921cfee4526b6ae
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682861"
---
# <a name="split-generated-xml-files-based-on-file-size-and-content-quantity"></a><span data-ttu-id="5ab2e-103">تقسيم ملفات XML التي تم إنشاؤها استنادًا إلى حجم الملف وكمية المحتوى</span><span class="sxs-lookup"><span data-stu-id="5ab2e-103">Split generated XML files based on file size and content quantity</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5ab2e-104">يمكنك تصميم تنسيقات إعداد التقارير الإلكترونية (ER) لإنشاء مستندات صادرة بتنسيق XML.</span><span class="sxs-lookup"><span data-stu-id="5ab2e-104">You can design Electronic reporting (ER) formats to generate outgoing documents in XML format.</span></span> <span data-ttu-id="5ab2e-105">أحيانًا، يمكن قبول تلك المستندات فقط عندما تفي بمعايير معينة، مثل الحجم الأقصى للملف أو العدد الأقصى لبعض عقد XML.</span><span class="sxs-lookup"><span data-stu-id="5ab2e-105">Sometimes, those documents can be accepted only when they meet specific criteria, such a maximum file size or a maximum number of some XML nodes.</span></span> <span data-ttu-id="5ab2e-106">يمكنك تصميم تنسيقات التقارير الإلكترونية لإنشاء المستندات الإلكترونية التي تفي بالمتطلبات التي يحددها مستلمو تلك المستندات.</span><span class="sxs-lookup"><span data-stu-id="5ab2e-106">You can design ER formats to generate electronic documents that satisfy the requirements that the recipients of those documents specify.</span></span>

- <span data-ttu-id="5ab2e-107">بالنسبة لعنصر بتنسيق FILE، فإنه يمكنك تحديد حدًا لحجم الملف كتعبير التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="5ab2e-107">For the FILE format element, you can define a limit on the file size as an ER expression.</span></span> <span data-ttu-id="5ab2e-108">إذا تجاوز الحد المحدد عند إنشاء تقرير إعداد التقارير الإلكترونية، فسيقوم تقرير إعداد التقارير الإلكترونية بإنشاء الملف الحالي ثم ينتقل لإنشاء الملف التالي.</span><span class="sxs-lookup"><span data-stu-id="5ab2e-108">If the defined limit is exceeded when an ER report is generated, ER finishes creating the current file and then moves on to create the next file.</span></span>
- <span data-ttu-id="5ab2e-109">بالنسبة لأي تنسيق لعنصر XML، فإنه يمكنك تحديد حدًا لعدد العناصر كتعبير إعداد التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="5ab2e-109">For any XML ELEMENT format, you can define a limit on the number of elements as an ER expression.</span></span> <span data-ttu-id="5ab2e-110">إذا تجاوز عدد عُقد XML في الملف التي تم إنشاؤه الحد المحدد عند تشغيل تقرير إعداد التقارير الإلكترونية، فسيقوم تقرير إعداد التقارير الإلكترونية بإنهاء إنشاء الملف الحالي ثم ينتقل لإنشاء الملف التالي.</span><span class="sxs-lookup"><span data-stu-id="5ab2e-110">If the number of XML nodes in the file that is generated exceeds the defined limit when an ER report is run, ER finishes creating the current file and then moves on to create the next file.</span></span>
- <span data-ttu-id="5ab2e-111">بالنسبة لأي عنصر بتنسيق تسلسل XML، فإنه يمكنك تحديد حدًا لعدد العناصر التابعة كتعبير إعداد التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="5ab2e-111">For any XML SEQUENCE format element, you can define a limit on the number of child elements as an ER expression.</span></span> <span data-ttu-id="5ab2e-112">إذا تجاوز عدد عُقد XML المتداخلة لعنصر التنسيق في الملف التي تم إنشاؤه الحد المحدد عند تشغيل تقرير إعداد التقارير الإلكترونية، فسيقوم تقرير إعداد التقارير الإلكترونية بإنهاء إنشاء الملف الحالي ثم ينتقل لإنشاء الملف التالي.</span><span class="sxs-lookup"><span data-stu-id="5ab2e-112">If the number of nested XML nodes of the format element in the generated file exceeds the defined limit when an ER report is run, ER finishes creating the current file and then moves on to create the next file.</span></span>
- <span data-ttu-id="5ab2e-113">يمكنك وضع علامة على أي عنصر بتنسيق XML ELEMENT كعنصر غير قابل للتقطيع.</span><span class="sxs-lookup"><span data-stu-id="5ab2e-113">You can mark any XML ELEMENT format element as non-breakable.</span></span> <span data-ttu-id="5ab2e-114">بهذه الطريقة، يمكنك الاحتفاظ بالعناصر المتداخلة لعقد XML التي يتم إنشاؤها وفقًا لعنصر التنسيق في ملف واحد منشأ.</span><span class="sxs-lookup"><span data-stu-id="5ab2e-114">In this way, you can keep the nested items of XML nodes that are generated under the format element in a single generated file.</span></span>

<span data-ttu-id="5ab2e-115">بالإضافة إلى استخدام عنصر XML وعناصر بتنسيق تسلسل XML لإضافة عقد XML إلى الملف المنشأ، فإنه يمكنك استخدام عنصر تنسيق XML أولي.</span><span class="sxs-lookup"><span data-stu-id="5ab2e-115">In addition to using the XML ELEMENT and XML SEQUENCE format elements to add XML nodes to the generated file, you can use the RAW XML format element.</span></span> <span data-ttu-id="5ab2e-116">وعلى الرغم من ذلك، لا تُوضع العقد التي تضيفها باستخدام عنصر تنسيق XML أولي في الاعتبار عندما يتم حساب عدد العقد لتقييم الحدود الموجودة على عدد العناصر.</span><span class="sxs-lookup"><span data-stu-id="5ab2e-116">However, nodes that you add by using the RAW XML format element aren't considered when the number of nodes is calculated to evaluate the limits on the number of elements.</span></span>

<span data-ttu-id="5ab2e-117">إذا قمت بتكوين وجهات الملف لعنصر بتنسيق FILE تم تكوينه لتقسيم الإخراج المنشأ متى يتم تجاوز حدود معينة، يتم إرسال كل جزء من الإخراج المنشأ إلى وجهة الملف المكون كملف واحد.</span><span class="sxs-lookup"><span data-stu-id="5ab2e-117">If you configured file destinations for a FILE format element that has been configured to split the generated output whenever specific limits are exceeded, each piece of generated output is sent to the configured file destination as an individual file.</span></span> <span data-ttu-id="5ab2e-118">لتسمية الملفات التي يتم إنشاؤها عن طريق تقسيم الإخراج بشكل فريد ، فإنه يجب تكوين تعبير التقارير الإلكترونية لعنصر تنسيق FILE.</span><span class="sxs-lookup"><span data-stu-id="5ab2e-118">To uniquely name the files that are created by splitting the output, you must configure an ER expression for the FILE format element.</span></span> <span data-ttu-id="5ab2e-119">إذا قمت بتضمين مصدر بيانات التقارير الإلكترونية لنوع التسلسل الرقمي ، فإنه ستتم زيادة الرقم التسلسلي لكل قطعة من الإخراج المنقسم.</span><span class="sxs-lookup"><span data-stu-id="5ab2e-119">If you include an ER data source of the NUMBER SEQUENCE type, the number sequence will be incremented for each piece of the split output.</span></span>

<span data-ttu-id="5ab2e-120">لمعرفة المزيد عن هذه الميزة، قم بتشغيل دليل المهمة **تقسم التقارير الإلكترونية لملفات XML استنادًا إلى حجم الملف أو كمية عنصر المحتوى** والتي تمثل جزءًا من العملية التجارية **7.5.4.3اكتساب/تطوير خدمة تكنولوجيا المعلومات/مكونات الحلول (10677‬‏‫)** ويمكن تنزيلها من[Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="5ab2e-120">To learn more about this feature, play the **ER Split XML files based on the file size or content item quantity** task guide, which is part of the **7.5.4.3 Acquire/Develop IT service/solution components (10677)** business process and can be downloaded from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span> <span data-ttu-id="5ab2e-121">يأخذك دليل المهمة هذا خلال عملية تكوين تنسيق إعداد التقارير الإلكترونية لتقسيم الملفات المنشأة حسب حدود حجم الملف وكمية عنصر المحتوى.</span><span class="sxs-lookup"><span data-stu-id="5ab2e-121">This task guide walks you through the process of configuring an ER format to split generated files based on limits on the file size and content item quantity.</span></span> <span data-ttu-id="5ab2e-122">لإكمال دليل المهمة هذا، يجب عليك تنزيل الملفات التالية:</span><span class="sxs-lookup"><span data-stu-id="5ab2e-122">To complete the task guide, you must download the following files:</span></span>

- [<span data-ttu-id="5ab2e-123">‏‫تكوين نموذج تقارير إلكترونية‬ - XmlFilesSplittingModel.xml</span><span class="sxs-lookup"><span data-stu-id="5ab2e-123">ER model configuration - XmlFilesSplittingModel.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111)
- [<span data-ttu-id="5ab2e-124">تكوين تنسيق التقارير الإلكترونية - XmlFilesSplittingFormat.xml</span><span class="sxs-lookup"><span data-stu-id="5ab2e-124">ER format configuration - XmlFilesSplittingFormat.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111)

## <a name="additional-resources"></a><span data-ttu-id="5ab2e-125">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="5ab2e-125">Additional resources</span></span>
[<span data-ttu-id="5ab2e-126">وجهات التقارير الإلكترونية‬</span><span class="sxs-lookup"><span data-stu-id="5ab2e-126">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)

[<span data-ttu-id="5ab2e-127">مصمم المعادلات في التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="5ab2e-127">Formula designer in Electronic reporting (ER)</span></span>](general-electronic-reporting-formula-designer.md)
