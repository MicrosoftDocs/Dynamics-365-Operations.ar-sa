---
title: قائمة وظائف التقارير الإلكترونية في فئة جمع البيانات
description: يوفر هذا الموضوع معلومات حول وظائف جمع البيانات المعتمدة في التقارير الإلكترونية (ER).
author: NickSelin
manager: kfend
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b318945c9cd10b237843d26cfdc46fc08e84e268
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917800"
---
# <a name="list-of-er-functions-in-the-data-collection-category"></a><span data-ttu-id="83cd7-103">قائمة وظائف التقارير الإلكترونية في فئة جمع البيانات</span><span class="sxs-lookup"><span data-stu-id="83cd7-103">List of ER functions in the data collection category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="83cd7-104">يتم استخدام وظائف جمع بيانات التقارير الإلكترونية (ER) لإجراء العد والجمع بتنسيق التقارير الإلكترونية التي يتم تشغيلها، استنادًا إلى بيانات المخرجات التي تم إنشاؤها بالفعل بتنسيق **نص** أو **Xml** .</span><span class="sxs-lookup"><span data-stu-id="83cd7-104">Electronic reporting (ER) data collection functions are used to do counting and summing in an ER format that is being run, based on data of the output that has already been generated in **Text** or **Xml** format.</span></span> <span data-ttu-id="83cd7-105">يستخدم هذا الأسلوب للمساعدة في تحسين أداء تنسيق التقارير الإلكترونية التي يتم تشغيلها، وإدخال قيم تشغيل الإجماليات في المستندات التي تم إنشاؤها، ولأغراض أخرى.</span><span class="sxs-lookup"><span data-stu-id="83cd7-105">This approach is used to help improve performance of an ER format that is run, to enter values of running totals in generated documents, and for other purposes.</span></span> <span data-ttu-id="83cd7-106">يعرض هذا الموضوع ملخصًا لهذه الوظائف.</span><span class="sxs-lookup"><span data-stu-id="83cd7-106">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="83cd7-107">قائمة الوظائف المدعومة</span><span class="sxs-lookup"><span data-stu-id="83cd7-107">List of supported functions</span></span>

| <span data-ttu-id="83cd7-108">الوظيفة</span><span class="sxs-lookup"><span data-stu-id="83cd7-108">Function</span></span> | <span data-ttu-id="83cd7-109">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="83cd7-109">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="83cd7-110">CollectedList</span><span class="sxs-lookup"><span data-stu-id="83cd7-110">CollectedList</span></span>](er-functions-datacollection-collectedlist.md) | <span data-ttu-id="83cd7-111">تُرجع هذه الوظيفة قيمة *قائمة السجل* التي تحتوي على قائمة القيم التي تم ارجاعها بواسطة خاصية **قيمة مفتاح البيانات التي تم جمعها** من عناصر التنسيق والتي تم جمعها عند استخدام عناصر التنسيق لتكوين تشغيل مستند صادر أثناء التنسيق، والذي يفي بالشروط المحددة.</span><span class="sxs-lookup"><span data-stu-id="83cd7-111">This function returns a *Record list* value that contains the list of values that were returned by the **Collected data key value** property of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="83cd7-112">يتكون كل شرط من نطاق المفتاح وقيمة المفتاح.</span><span class="sxs-lookup"><span data-stu-id="83cd7-112">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="83cd7-113">CountIF</span><span class="sxs-lookup"><span data-stu-id="83cd7-113">CountIF</span></span>](er-functions-datacollection-countif.md) | <span data-ttu-id="83cd7-114">تقوم هذه الوظيفة بإرجاع قيمه *عدد صحيح* الذي يمثل رقم عناصر التنسيق التي تم تجميعها عند استخدام عناصر التنسيق لإنشاء مستند صادر أثناء تشغيل التنسيق، والذي يفي بالشرط المحدد.</span><span class="sxs-lookup"><span data-stu-id="83cd7-114">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="83cd7-115">يتكون الشرط من نطاق المفتاح وقيمة المفتاح.</span><span class="sxs-lookup"><span data-stu-id="83cd7-115">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="83cd7-116">CountIFs</span><span class="sxs-lookup"><span data-stu-id="83cd7-116">CountIFs</span></span>](er-functions-datacollection-countifs.md) | <span data-ttu-id="83cd7-117">تقوم هذه الوظيفة بإرجاع قيمه *عدد صحيح* الذي يمثل رقم عناصر التنسيق التي تم تجميعها عند استخدام عناصر التنسيق لإنشاء مستند صادر أثناء تشغيل التنسيق، والذي يفي بالشروط المحددة.</span><span class="sxs-lookup"><span data-stu-id="83cd7-117">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="83cd7-118">يتكون كل شرط من نطاق المفتاح وقيمة المفتاح.</span><span class="sxs-lookup"><span data-stu-id="83cd7-118">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="83cd7-119">FormatElementName</span><span class="sxs-lookup"><span data-stu-id="83cd7-119">FormatElementName</span></span>](er-functions-datacollection-formatelementname.md) | <span data-ttu-id="83cd7-120">تقوم هذه الوظيفة بإرجاع قيمة *سلسلة* التي تمثل اسم عنصر تنسيق التقارير الإلكترونية الحالية.</span><span class="sxs-lookup"><span data-stu-id="83cd7-120">This function returns a *String* value that represents the name of the current ER format's element.</span></span> |
| [<span data-ttu-id="83cd7-121">SumIF</span><span class="sxs-lookup"><span data-stu-id="83cd7-121">SumIF</span></span>](er-functions-datacollection-sumif.md) | <span data-ttu-id="83cd7-122">تقوم هذه الوظيفة بإرجاع قيمة *حقيقي* الذي يمثل مجموع القيم التي تم إرجاعها بواسطة روابط عناصر التنسيق والتي تم جمعها عند استخدام عناصر التنسيق لإنشاء مستند صادر أثناء تشغيل التنسيق، والتي تفي بالشرط المحدد .</span><span class="sxs-lookup"><span data-stu-id="83cd7-122">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="83cd7-123">يتكون الشرط من نطاق المفتاح وقيمة المفتاح.</span><span class="sxs-lookup"><span data-stu-id="83cd7-123">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="83cd7-124">SumIFs</span><span class="sxs-lookup"><span data-stu-id="83cd7-124">SumIFs</span></span>](er-functions-datacollection-sumifs.md) | <span data-ttu-id="83cd7-125">تقوم هذه الوظيفة بإرجاع قيمة *حقيقي* الذي يمثل مجموع القيم التي تم إرجاعها بواسطة روابط عناصر التنسيق والتي تم جمعها عند استخدام عناصر التنسيق لإنشاء مستند صادر أثناء تشغيل التنسيق، والتي تفي بالشروط المحددة.</span><span class="sxs-lookup"><span data-stu-id="83cd7-125">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="83cd7-126">يتكون كل شرط من نطاق المفتاح وقيمة المفتاح.</span><span class="sxs-lookup"><span data-stu-id="83cd7-126">Each condition consists of a key range and a key value.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="83cd7-127">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="83cd7-127">Additional resources</span></span>

[<span data-ttu-id="83cd7-128">نظرة عامة حول التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="83cd7-128">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="83cd7-129">مصمم المعادلات في التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="83cd7-129">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="83cd7-130">لغة تركيبة التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="83cd7-130">Electronic reporting formula language</span></span>](er-formula-language.md)
