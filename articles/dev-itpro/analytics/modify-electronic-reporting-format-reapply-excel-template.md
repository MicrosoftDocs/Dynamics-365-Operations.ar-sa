---
title: "تعديل تنسيق إعداد التقارير الإلكتروني من خلال إعادة تطبيق قالب Microsoft Excel"
description: "يوفر هذا الموضوع معلومات حول كيفية تعديل تنسيق التقارير الإلكترونية (ER) الذي يستخدم لإنشاء مستندات الأعمال عن طريق إعادة تطبيق قالب Excel معدل."
author: NickSelin
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: af7f9a373496eee4df354d5dd9e5a25c51317c43
ms.openlocfilehash: fca7fb75b965886c2ebc06b12940434f2ffc2543
ms.contentlocale: ar-sa
ms.lasthandoff: 02/27/2018

---
# <a name="modify-an-electronic-reporting-format-by-reapplying-a-microsoft-excel-template"></a><span data-ttu-id="51538-103">تعديل تنسيق إعداد التقارير الإلكتروني من خلال إعادة تطبيق قالب Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="51538-103">Modify an Electronic reporting format by reapplying a Microsoft Excel template</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="51538-104">يتم استخدام أداة إعداد التقارير الإلكترونية (ER) لإنشاء مستندات الأعمال بتنسيق إلكتروني.</span><span class="sxs-lookup"><span data-stu-id="51538-104">The Electronic reporting (ER) tool is used to generate business documents in an electronic format.</span></span> <span data-ttu-id="51538-105">لإنشاء مستند عمل، يجب إنشاء تنسيق ER، وبعد ذلك استخدم مصمم ER لتحديد تخطيط مستند الأعمال وتحديد البيانات التي يجب تضمينها به.</span><span class="sxs-lookup"><span data-stu-id="51538-105">To generate a business document, you must create an ER format, and then use the ER designer to define the layout of the business document and specify the data that should be included in it.</span></span> <span data-ttu-id="51538-106">يمكنك بعد ذلك تشغيل تنسيق ER لإنشاء مستند الأعمال.</span><span class="sxs-lookup"><span data-stu-id="51538-106">You can then run the ER format to generate the business document.</span></span>

<span data-ttu-id="51538-107">يمكن استخدام أداة ER لإنشاء مستندات الأعمال كملفات Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="51538-107">The ER tool can be used to generate business documents as Microsoft Excel files.</span></span> <span data-ttu-id="51538-108">ويمكنك استخدام مستند Excel كقالب لهذه المستندات.</span><span class="sxs-lookup"><span data-stu-id="51538-108">You can use an Excel document as a template for these documents.</span></span> <span data-ttu-id="51538-109">لتحديد تخطيط المستند في مصمم ER، يمكنك استيراد محتويات مستند Excel الذي تريد استخدامه كقالب في تنسيق ER المحدد.</span><span class="sxs-lookup"><span data-stu-id="51538-109">To define the document layout in the ER designer, you can import the contents of the Excel document that you want to use as a template into the defined ER format.</span></span> <span data-ttu-id="51538-110">لمزيد من التفاصيل، وممارسة هذا السيناريو، يمكنك تشغيل دليل المهمة **‬‏‫تصميم تكوين لإنشاء التقارير بتنسيق OPENXML في ER‬‏‫** (جزء من العملية التجارية ‬‏‫‬‏‫7.5.4.3 اكتساب/تطوير مكونات الخدمات/الحلول الخاصة بتقنية المعلومات (10677)).</span><span class="sxs-lookup"><span data-stu-id="51538-110">For more details, and to practice this scenario, play the task guide **ER Design a configuration for generating reports in OPENXML format** (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span>

<span data-ttu-id="51538-111">إذا قمت بتحرير المستند Excel الذي يتم استخدامه كقالب لمستند أعمال، تسمح لك وظيفة ER الجديدة بإعادة تطبيق القالب المحدث على تنسيق ER.</span><span class="sxs-lookup"><span data-stu-id="51538-111">If you edit the Excel document that is used as a template for a business document, new ER functionality lets you reapply the updated template to the ER format.</span></span> <span data-ttu-id="51538-112">يتم بعد ذلك تحديث تنسيق ER بحيث يلتزم بالقالب المحدث.</span><span class="sxs-lookup"><span data-stu-id="51538-112">The ER format is then updated so that it adheres to the updated template.</span></span> <span data-ttu-id="51538-113">للحصول على مزيد من التفاصيل حول هذه الوظيفة، قم بتشغيل دليل المهمة **‬‏‫تعديل تنسيق إعداد التقارير الإلكتروني من خلال إعادة تطبيق قالب Microsoft Excel** (جزء من عملية الأعمال 7.5.5.3 الحصول على/تطوير مكونات خدمة/حل تكنولوجيا المعلومات (10683)).</span><span class="sxs-lookup"><span data-stu-id="51538-113">For more details about this functionality, play the task guide **ER Modify a format by reapplying an Excel template** (part of the 7.5.5.3 Acquire/Develop IT service/solution components (10683) business process).</span></span> <span data-ttu-id="51538-114">في خطوة دليل المهمة حيث تقوم باستيراد قالب تم تحديثه، استخدم القالب المعدل لملف Excel تقرير الدفع، SampleVendPaymWsReport2، كقالب.</span><span class="sxs-lookup"><span data-stu-id="51538-114">In the task guide step where you import an updated template, use the modified template of the Payment Report Excel file, SampleVendPaymWsReport2, as a template.</span></span>

