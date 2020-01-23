---
title: قائمة وظائف التقارير الإلكترونية في فئة التاريخ والوقت
description: يوفر هذا الموضوع معلومات حول وظائف التاريخ والوقت المعتمدة في التقارير الإلكترونية (ER).
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: fa8e725ac6bd7d280dc0269a70e3f7abf1ad4d43
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916558"
---
# <a name="list-of-er-functions-in-the-date-and-time-category"></a><span data-ttu-id="ead10-103">قائمة وظائف التقارير الإلكترونية في فئة التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="ead10-103">List of ER functions in the Date and time category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ead10-104">يمكن استخدام وظائف التاريخ والوقت في التقارير الإلكترونية (ER) لاستخراج المعلومات من قيم التاريخ والوقت، ولتنفيذ العمليات عليها.</span><span class="sxs-lookup"><span data-stu-id="ead10-104">Electronic reporting (ER) date and time functions can be used to extract information from date and time values, and to perform operations on them.</span></span> <span data-ttu-id="ead10-105">يعرض هذا الموضوع ملخصًا لهذه الوظائف.</span><span class="sxs-lookup"><span data-stu-id="ead10-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="ead10-106">قائمة الوظائف المدعومة</span><span class="sxs-lookup"><span data-stu-id="ead10-106">List of supported functions</span></span>

| <span data-ttu-id="ead10-107">الوظيفة</span><span class="sxs-lookup"><span data-stu-id="ead10-107">Function</span></span> | <span data-ttu-id="ead10-108">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="ead10-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="ead10-109">AddDays</span><span class="sxs-lookup"><span data-stu-id="ead10-109">AddDays</span></span>](er-functions-datetime-adddays.md) | <span data-ttu-id="ead10-110">تُرجع هذه الوظيفة قيمة *DateTime* والتي هي عدد الأيام المُحددة قبل أو بعد تاريخ البدء المُحدد.</span><span class="sxs-lookup"><span data-stu-id="ead10-110">This function returns a *DateTime* value that is the specified number of days before or after a specified start date.</span></span> |
| [<span data-ttu-id="ead10-111">DateFormat</span><span class="sxs-lookup"><span data-stu-id="ead10-111">DateFormat</span></span>](er-functions-datetime-dateformat.md) | <span data-ttu-id="ead10-112">تقوم هذه الوظيفة بإرجاع قيمة *السلسلة* التي تمثل قيمة تاريخ مُعين كنص في التنسيق المُحدد وفي الثقافة المُحددة بشكل اختياري.</span><span class="sxs-lookup"><span data-stu-id="ead10-112">This function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="ead10-113">DateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="ead10-113">DateTimeFormat</span></span>](er-functions-datetime-datetimeformat.md) | <span data-ttu-id="ead10-114">تقوم هذه الوظيفة بإرجاع قيمة *السلسلة* التي تمثل قيمة تاريخ/وقت مُعين كنص في التنسيق المُحدد وفي الثقافة المُحددة بشكل اختياري.</span><span class="sxs-lookup"><span data-stu-id="ead10-114">This function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="ead10-115">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="ead10-115">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md) | <span data-ttu-id="ead10-116">تقوم هذه الوظيفة بإرجاع قيمة *DateTime* التي تم تحويلها من قيمة نصية معينة في التنسيق المُحدد وفي الثقافة المُحددة بشكل اختياري إلى قيمة التاريخ/الوقت.</span><span class="sxs-lookup"><span data-stu-id="ead10-116">This function returns a *DateTime* value that is converted from a given text value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="ead10-117">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="ead10-117">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="ead10-118">تُرجع هذه الوظيفة قيمة *DateTime* التي تم تحويلها من قيمة تاريخ معين إلى قيمةالتاريخ/الوقت بالتوقيت  العالمي المنسق (توقيت جرينتش المتوسط \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="ead10-118">This function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="ead10-119">DateValue</span><span class="sxs-lookup"><span data-stu-id="ead10-119">DateValue</span></span>](er-functions-datetime-datevalue.md) | <span data-ttu-id="ead10-120">تقوم هذه الوظيفة بإرجاع قيمة *التاريخ* التي تم تحويلها من قيمة نصية معينة في التنسيق المُحدد وفي الثقافة المُحددة بشكل اختياري إلى قيمة التاريخ/الوقت.</span><span class="sxs-lookup"><span data-stu-id="ead10-120">This function returns a *Date* value that is converted from a given text value in the specified format and in an optionally specified culture to a date value.</span></span> |
| [<span data-ttu-id="ead10-121">DayOfYear</span><span class="sxs-lookup"><span data-stu-id="ead10-121">DayOfYear</span></span>](er-functions-datetime-dayofyear.md) | <span data-ttu-id="ead10-122">تُرجع هذه الوظيفة قيمة *عدد صحيح* تمثل عدد الأيام من 1 يناير إلى التاريخ المُحدد.</span><span class="sxs-lookup"><span data-stu-id="ead10-122">This function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span> |
| [<span data-ttu-id="ead10-123">الأيام</span><span class="sxs-lookup"><span data-stu-id="ead10-123">Days</span></span>](er-functions-datetime-days.md) | <span data-ttu-id="ead10-124">تُرجع هذه الوظيفة قيمة *عدد صحيح* تمثل عدد الأيام بين التاريخ المُحدد الأول والتاريخ المُحدد الثاني.</span><span class="sxs-lookup"><span data-stu-id="ead10-124">This function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span> |
| [<span data-ttu-id="ead10-125">Now</span><span class="sxs-lookup"><span data-stu-id="ead10-125">Now</span></span>](er-functions-datetime-now.md) | <span data-ttu-id="ead10-126">تُرجع هذه الوظيفة قيمة *DateTime* التي تمثل تاريخ خادم التطبيق الحالي والتوقيت.</span><span class="sxs-lookup"><span data-stu-id="ead10-126">This function returns a *DateTime* value that represents the current application server date and time.</span></span> |
| [<span data-ttu-id="ead10-127">NullDate</span><span class="sxs-lookup"><span data-stu-id="ead10-127">NullDate</span></span>](er-functions-datetime-nulldate.md) | <span data-ttu-id="ead10-128">تُرجع هذه الوظيفة قيمة *تاريخ* والتي تمثل التاريخ **الفارغ** (1 يناير 1900).</span><span class="sxs-lookup"><span data-stu-id="ead10-128">This function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span> |
| [<span data-ttu-id="ead10-129">NullDateTime</span><span class="sxs-lookup"><span data-stu-id="ead10-129">NullDateTime</span></span>](er-functions-datetime-nulldatetime.md) | <span data-ttu-id="ead10-130">تُرجع هذه الوظيفة قيمة *DateTime* التي تمثل قيمة التاريخ/الوقت **الفارغة** (1 يناير 1900) بالتوقيت العالمي المتفق عليه.</span><span class="sxs-lookup"><span data-stu-id="ead10-130">This function returns a *DateTime* value that represents the **null** date/time value (January 1, 1900) in Coordinated Universal Time.</span></span> |
| [<span data-ttu-id="ead10-131">SessionNow</span><span class="sxs-lookup"><span data-stu-id="ead10-131">SessionNow</span></span>](er-functions-datetime-sessionnow.md) | <span data-ttu-id="ead10-132">تُرجع هذه الوظيفة قيمة *DateTime* التي تمثل تاريخ جلسة التطبيق الحالية والتوقيت.</span><span class="sxs-lookup"><span data-stu-id="ead10-132">This function returns a *DateTime* value that represents the current application session date and time.</span></span> |
| [<span data-ttu-id="ead10-133">SessionToday</span><span class="sxs-lookup"><span data-stu-id="ead10-133">SessionToday</span></span>](er-functions-datetime-sessiontoday.md) | <span data-ttu-id="ead10-134">تُرجع هذه الوظيفة قيمة *التاريخ* التي تمثل تاريخ جلسة التطبيق الحالية.</span><span class="sxs-lookup"><span data-stu-id="ead10-134">This function returns a *Date* value that represents the current application session date.</span></span> |
| [<span data-ttu-id="ead10-135">اليوم</span><span class="sxs-lookup"><span data-stu-id="ead10-135">Today</span></span>](er-functions-datetime-today.md) | <span data-ttu-id="ead10-136">تُرجع هذه الوظيفة قيمة *التاريخ* التي تمثل تاريخ خادم التطبيق الحالي.</span><span class="sxs-lookup"><span data-stu-id="ead10-136">This function returns a *Date* value that represents the current application server date.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="ead10-137">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="ead10-137">Additional resources</span></span>

[<span data-ttu-id="ead10-138">نظرة عامة حول التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="ead10-138">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="ead10-139">مصمم المعادلات في التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="ead10-139">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="ead10-140">لغة تركيبة التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="ead10-140">Electronic reporting formula language</span></span>](er-formula-language.md)
