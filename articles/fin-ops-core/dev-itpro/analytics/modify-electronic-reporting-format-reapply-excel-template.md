---
title: تعديل تنسيقات التقارير الإلكترونية من خلال إعادة تطبيق قوالب Excel
description: يصف الموضوع كيفية تعديل تنسيق التقارير الإلكترونية (ER) الذي يستخدم لإنشاء مستندات الأعمال عن طريق إعادة تطبيق قالب Excel معدل.
author: NickSelin
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f28760f42d16b6ffcd301f121e583542bce0fac0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559280"
---
# <a name="modify-electronic-reporting-formats-by-reapplying-excel-templates"></a><span data-ttu-id="cd736-103">تعديل تنسيقات التقارير الإلكترونية من خلال إعادة تطبيق قوالب Excel</span><span class="sxs-lookup"><span data-stu-id="cd736-103">Modify Electronic reporting formats by reapplying Excel templates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd736-104">يتم استخدام أداة إعداد التقارير الإلكترونية (ER) لإنشاء مستندات الأعمال بتنسيق إلكتروني.</span><span class="sxs-lookup"><span data-stu-id="cd736-104">The Electronic reporting (ER) tool is used to generate business documents in an electronic format.</span></span> <span data-ttu-id="cd736-105">لإنشاء مستند عمل، يجب إنشاء تنسيق ER، وبعد ذلك استخدم مصمم ER لتحديد تخطيط مستند الأعمال وتحديد البيانات التي يجب تضمينها به.</span><span class="sxs-lookup"><span data-stu-id="cd736-105">To generate a business document, you must create an ER format, and then use the ER designer to define the layout of the business document and specify the data that should be included in it.</span></span> <span data-ttu-id="cd736-106">يمكنك بعد ذلك تشغيل تنسيق ER لإنشاء مستند الأعمال.</span><span class="sxs-lookup"><span data-stu-id="cd736-106">You can then run the ER format to generate the business document.</span></span>

<span data-ttu-id="cd736-107">يمكن استخدام أداة إعداد التقارير الإلكترونية لإنشاء مستندات أعمال كملفات Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="cd736-107">The ER tool can be used to generate business documents as Microsoft Excel files.</span></span> <span data-ttu-id="cd736-108">ويمكنك استخدام مستند Excel كقالب لهذه المستندات.</span><span class="sxs-lookup"><span data-stu-id="cd736-108">You can use an Excel document as a template for these documents.</span></span> <span data-ttu-id="cd736-109">لتحديد تخطيط المستند في مصمم ER، يمكنك استيراد محتويات مستند Excel الذي تريد استخدامه كقالب في تنسيق ER المحدد.</span><span class="sxs-lookup"><span data-stu-id="cd736-109">To define the document layout in the ER designer, you can import the contents of the Excel document that you want to use as a template into the defined ER format.</span></span> <span data-ttu-id="cd736-110">لمزيد من التفاصيل، وممارسة هذا السيناريو، يمكنك تشغيل دليل المهمة **‬‏‫تصميم تكوين لإنشاء التقارير بتنسيق OPENXML في ER‬‏‫** (جزء من العملية التجارية ‬‏‫‬‏‫7.5.4.3 اكتساب/تطوير مكونات الخدمات/الحلول الخاصة بتقنية المعلومات (10677)).</span><span class="sxs-lookup"><span data-stu-id="cd736-110">For more details, and to practice this scenario, play the task guide **ER Design a configuration for generating reports in OPENXML format** (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span>

<span data-ttu-id="cd736-111">إذا قمت بتحرير المستند Excel الذي يتم استخدامه كقالب لمستند أعمال، تسمح لك وظيفة ER الجديدة بإعادة تطبيق القالب المحدث على تنسيق ER.</span><span class="sxs-lookup"><span data-stu-id="cd736-111">If you edit the Excel document that is used as a template for a business document, new ER functionality lets you reapply the updated template to the ER format.</span></span> <span data-ttu-id="cd736-112">يتم بعد ذلك تحديث تنسيق ER بحيث يلتزم بالقالب المحدث.</span><span class="sxs-lookup"><span data-stu-id="cd736-112">The ER format is then updated so that it adheres to the updated template.</span></span> <span data-ttu-id="cd736-113">للحصول على مزيد من التفاصيل حول هذه الوظيفة، قم بتشغيل دليل المهمة **تعديل تنسيق إعداد التقارير الإلكتروني من خلال إعادة تطبيق قالب Excel** (جزء من عملية الأعمال 7.5.5.3 اكتساب/تطوير مكونات خدمة تكنولوجيا المعلومات/الحلول(10683)).</span><span class="sxs-lookup"><span data-stu-id="cd736-113">For more details about this functionality, play the task guide **ER Modify a format by reapplying an Excel template** (part of the 7.5.5.3 Acquire/Develop IT service/solution components (10683) business process).</span></span> <span data-ttu-id="cd736-114">في خطوة دليل المهمة حيث تقوم باستيراد قالب تم تحديثه، استخدم القالب المعدل لملف Excel تقرير الدفع، SampleVendPaymWsReport2، كقالب.</span><span class="sxs-lookup"><span data-stu-id="cd736-114">In the task guide step where you import an updated template, use the modified template of the Payment Report Excel file, SampleVendPaymWsReport2, as a template.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]