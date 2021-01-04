---
title: توزيع المستندات الواردة بتنسيق JSON
description: يوضح هذا الموضوع كيفية إعداد تنسيقات التقارير الإلكترونية (ER) لتحليل المستندات الواردة بتنسيق JavaScript Object Notation (JSON).
author: kfend
manager: AnnBe
ms.date: 05/20/2019
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
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: b4ed81bb5527ea8e02caaa1262a57960dd7cdf29
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685753"
---
# <a name="parse-incoming-documents-in-json-format"></a><span data-ttu-id="b92e4-103">توزيع المستندات الواردة بتنسيق JSON</span><span class="sxs-lookup"><span data-stu-id="b92e4-103">Parse incoming documents in JSON format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b92e4-104">يمكنك تصميم تنسيقات التقارير الإلكترونية (ER) لتحليل المستندات الإلكترونية الواردة التي تمثل البيانات في تنسيق نص والتي تستند إلى JavaScript( بمعنى آخر، ملفات بتنسيق JavaScript Object Notation \[JSON\]).</span><span class="sxs-lookup"><span data-stu-id="b92e4-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents that represent data in a text format that is based on JavaScript (in other words, files in JavaScript Object Notation \[JSON\] format).</span></span>

<span data-ttu-id="b92e4-105">لمعرفة المزيد حول هذه الميزة، نزِّل الملفات الموجودة في الجدول التالي، ثم شغل "‏‫التقارير الإلكترونية - إنشاء تكوين تنسيق" لإنشاء تكوين لاستيراد البيانات من دليل مهام ملف JSON خارجي.</span><span class="sxs-lookup"><span data-stu-id="b92e4-105">To learn more about this feature, download the files in the following table, and then play the ER Create a format configuration to import data from an external JSON file task guide.</span></span> <span data-ttu-id="b92e4-106">يوضح دليل المهام هذا كيف يمكن استخدام تنسيق ER لتحليل ملف JSON وارد لتحديث بيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="b92e4-106">This task guide shows how an ER format can be used to parse an incoming JSON file to update application data.</span></span>

| <span data-ttu-id="b92e4-107">المسمى الوظيفي</span><span class="sxs-lookup"><span data-stu-id="b92e4-107">Title</span></span>                                  | <span data-ttu-id="b92e4-108">اسم الملف</span><span class="sxs-lookup"><span data-stu-id="b92e4-108">File name</span></span> |
|----------------------------------------|-----------|
| <span data-ttu-id="b92e4-109">تنسيق تكوين ER</span><span class="sxs-lookup"><span data-stu-id="b92e4-109">ER format configuration</span></span>                | [<span data-ttu-id="b92e4-110">تنسيق لاستيراد trans_JSON.xml للموردين</span><span class="sxs-lookup"><span data-stu-id="b92e4-110">Format for importing vendors' trans_JSON.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |
| <span data-ttu-id="b92e4-111">نموذج ملف وارد بتنسيق .csv</span><span class="sxs-lookup"><span data-stu-id="b92e4-111">Sample of incoming file in .csv format</span></span> | [<span data-ttu-id="b92e4-112">1099entries_JSON.txt</span><span class="sxs-lookup"><span data-stu-id="b92e4-112">1099entries_JSON.txt</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |

## <a name="requirements"></a><span data-ttu-id="b92e4-113">متطلبات</span><span class="sxs-lookup"><span data-stu-id="b92e4-113">Requirements</span></span>

<span data-ttu-id="b92e4-114">قبل إكمال "التقارير الإلكترونية - إنشاء تكوين تنسيق" لاستيراد بيانات من دليل مهام ملف JSON خارجي، يجب استيفاء المتطلب التالي:</span><span class="sxs-lookup"><span data-stu-id="b92e4-114">Before you complete the ER Create a format configuration to import data from an external JSON file task guide, the following requirement must be met:</span></span>

- <span data-ttu-id="b92e4-115">يمكن أن تكون عناصر الأصل في ملف JSON عناصر الكائن فقط.</span><span class="sxs-lookup"><span data-stu-id="b92e4-115">Parent elements in the JSON file can be only object elements.</span></span>
- <span data-ttu-id="b92e4-116">يجب أن تكون العناصر المتداخلة لأحد الكائنات عناصر خصائص، بحيث يتم إنشاء بنية JSON صالحة.</span><span class="sxs-lookup"><span data-stu-id="b92e4-116">Nested elements for an object should be property elements, so that a valid JSON structure is created.</span></span>
- <span data-ttu-id="b92e4-117">يمكن أن تكون صفائف JSON عناصر متداخلة فقط من عناصر خصائص لأحد الكائنات.</span><span class="sxs-lookup"><span data-stu-id="b92e4-117">JSON arrays can be only nested elements of the property elements of an object.</span></span>
- <span data-ttu-id="b92e4-118">يمكن أن تحتوي صفائف JSON علي كائنات JSON فقط.</span><span class="sxs-lookup"><span data-stu-id="b92e4-118">JSON arrays can contain only JSON objects.</span></span> <span data-ttu-id="b92e4-119">لا يمكن أن تحتوي علي صفائف متداخلة وقيم سلسلة/رقمية مباشرة.</span><span class="sxs-lookup"><span data-stu-id="b92e4-119">They can't contain direct string/numeric values and nested arrays.</span></span> <span data-ttu-id="b92e4-120">سيتم تحليل العناصر في هذه الصفائف بالترتيب، كما تم تحديدها في التنسيق.</span><span class="sxs-lookup"><span data-stu-id="b92e4-120">Elements in these arrays will be parsed in order, as they are specified in the format.</span></span> <span data-ttu-id="b92e4-121">سيتم التعامل مع إعدادات التعدد في كل كائن JSON.</span><span class="sxs-lookup"><span data-stu-id="b92e4-121">Multiplicity settings on each JSON object will be considered.</span></span>

<span data-ttu-id="b92e4-122">وبالإضافة إلى ذلك، يجب إكمال مهمة [التقارير الإلكترونية - إنشاء التكوينات المطلوبة لاستيراد بيانات من ملف خارجي](tasks/er-required-configurations-import-data.md) إذا لم تكن قد قمت بإكماله بالفعل.</span><span class="sxs-lookup"><span data-stu-id="b92e4-122">Additionally, you must complete the [ER Create required configurations to import data from an external file](tasks/er-required-configurations-import-data.md) task guide if you haven't already completed it.</span></span> <span data-ttu-id="b92e4-123">نزِّل الملف التالي لإكمال دليل المهام.</span><span class="sxs-lookup"><span data-stu-id="b92e4-123">Download the following file to complete the task guide.</span></span>

| <span data-ttu-id="b92e4-124">المسمى الوظيفي</span><span class="sxs-lookup"><span data-stu-id="b92e4-124">Title</span></span>                  | <span data-ttu-id="b92e4-125">اسم الملف</span><span class="sxs-lookup"><span data-stu-id="b92e4-125">File name</span></span> |
|------------------------|-----------|
| <span data-ttu-id="b92e4-126">تكوين نموذج تقارير إلكترونية</span><span class="sxs-lookup"><span data-stu-id="b92e4-126">ER model configuration</span></span> | [<span data-ttu-id="b92e4-127">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="b92e4-127">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |
