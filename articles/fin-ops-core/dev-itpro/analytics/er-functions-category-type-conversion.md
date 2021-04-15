---
title: قائمة وظائف التقارير الإلكترونية في فئة تحويل النوع
description: يوفر هذا الموضوع معلومات حول وظائف التحويل المعتمدة في التقارير الإلكترونية (ER).
author: NickSelin
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 199d51ae8a4dbdd7d2f3bd290a2b487ceb1174dc
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752594"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a><span data-ttu-id="2e659-103">قائمة وظائف التقارير الإلكترونية في فئة تحويل النوع</span><span class="sxs-lookup"><span data-stu-id="2e659-103">List of ER functions in the type conversion category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2e659-104">يُمكن استخدام وظائف تحويل نوع التقارير الإلكترونية (ER) لتحويل القيم بين الأنواع.</span><span class="sxs-lookup"><span data-stu-id="2e659-104">Electronic reporting (ER) type conversion functions can be used to convert values between types.</span></span> <span data-ttu-id="2e659-105">يعرض هذا الموضوع ملخصًا لهذه الوظائف.</span><span class="sxs-lookup"><span data-stu-id="2e659-105">This topic provides a summary of these functions.</span></span>

## <a name="type-conversion-functions"></a><span data-ttu-id="2e659-106">وظائف تحويل النوع</span><span class="sxs-lookup"><span data-stu-id="2e659-106">Type conversion functions</span></span>

| <span data-ttu-id="2e659-107">الوظيفة</span><span class="sxs-lookup"><span data-stu-id="2e659-107">Function</span></span> | <span data-ttu-id="2e659-108">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="2e659-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="2e659-109">Int64Value</span><span class="sxs-lookup"><span data-stu-id="2e659-109">Int64Value</span></span>](er-functions-conversion-int64value.md)   | <span data-ttu-id="2e659-110">تُرجع هذه الوظيفة قيمة *Int64* التي تمثل السلسلة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="2e659-110">This function returns an *Int64* value that represents the specified string.</span></span> |
| [<span data-ttu-id="2e659-111">IntValue</span><span class="sxs-lookup"><span data-stu-id="2e659-111">IntValue</span></span>](er-functions-conversion-intvalue.md)       | <span data-ttu-id="2e659-112">تُرجع هذه الوظيفة قيمة *Int* التي تمثل السلسلة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="2e659-112">This function returns an *Int* value that represents the specified string.</span></span> |
| [<span data-ttu-id="2e659-113">NumberValue</span><span class="sxs-lookup"><span data-stu-id="2e659-113">NumberValue</span></span>](er-functions-conversion-numbervalue.md) | <span data-ttu-id="2e659-114">تُرجع هذه الوظيفة قيمة *حقيقة* يتم تحويلها من قيمة *السلسلة* المُحددة.</span><span class="sxs-lookup"><span data-stu-id="2e659-114">This function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="2e659-115">في أثناء التحويل، يوضع في الاعتبار فواصل التجميع العشرية والرقمية المُحددة.</span><span class="sxs-lookup"><span data-stu-id="2e659-115">During the conversion, the specified decimal and digit grouping separators are considered.</span></span> |
| [<span data-ttu-id="2e659-116">القيمة</span><span class="sxs-lookup"><span data-stu-id="2e659-116">Value</span></span>](er-functions-conversion-value.md)             | <span data-ttu-id="2e659-117">تُرجع هذه الوظيفة قيمة *حقيقة* يتم تحويلها من قيمة *السلسلة* المُحددة.</span><span class="sxs-lookup"><span data-stu-id="2e659-117">This function returns a *Real* value that is converted from the specified *String* value.</span></span> |

## <a name="type-conversion-functions-in-the-container-category"></a><span data-ttu-id="2e659-118">وظائف تحويل النوع في فئة الحاوية</span><span class="sxs-lookup"><span data-stu-id="2e659-118">Type conversion functions in the container category</span></span>

<span data-ttu-id="2e659-119">يوضح الجدول التالي وظائف تحويل النوع في فئة [الحاوية](er-functions-category-container.md).</span><span class="sxs-lookup"><span data-stu-id="2e659-119">The following table describes the type conversion functions in the [container](er-functions-category-container.md) category.</span></span>

| <span data-ttu-id="2e659-120">الوظيفة</span><span class="sxs-lookup"><span data-stu-id="2e659-120">Function</span></span> | <span data-ttu-id="2e659-121">الوصف</span><span class="sxs-lookup"><span data-stu-id="2e659-121">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="2e659-122">Base64StringToContainer</span><span class="sxs-lookup"><span data-stu-id="2e659-122">Base64StringToContainer</span></span>](er-functions-container-base64stringtocontainer.md) | <span data-ttu-id="2e659-123">تقوم دالة بتحويل الإدخال المُحدد لنوع *السلسلة* إلى عنصر بيانات من النوع *الحاوية*.</span><span class="sxs-lookup"><span data-stu-id="2e659-123">This function converts the specified input of the *String* type to a data item of the *Container* type.</span></span> |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a><span data-ttu-id="2e659-124">وظائف تحويل النوع في فئة التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="2e659-124">Type conversion functions in the date and time category</span></span>

<span data-ttu-id="2e659-125">يوضح الجدول التالي وظائف تحويل النوع في [فئة التاريخ والوقت](er-functions-category-datetime.md).</span><span class="sxs-lookup"><span data-stu-id="2e659-125">The following table describes the type conversion functions in the [date and time category](er-functions-category-datetime.md).</span></span>

| <span data-ttu-id="2e659-126">الوظيفة</span><span class="sxs-lookup"><span data-stu-id="2e659-126">Function</span></span> | <span data-ttu-id="2e659-127">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="2e659-127">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="2e659-128">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="2e659-128">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md)   | <span data-ttu-id="2e659-129">تُرجع هذه الوظيفة قيمة *DateTime* التي تم تحويلها من قيمة *سلسلة* معينة في التنسيق المُحدد وفي الثقافة المُحددة بشكل اختياري إلى قيمة التاريخ/الوقت.</span><span class="sxs-lookup"><span data-stu-id="2e659-129">This function returns a *DateTime* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="2e659-130">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="2e659-130">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="2e659-131">تُرجع هذه الوظيفة قيمة *DateTime* التي تم تحويلها من قيمة *تاريخ* معين إلى قيمة التاريخ/الوقت بالتوقيت العالمي المنسق (توقيت جرينتش المتوسط \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="2e659-131">This function returns a *DateTime* value that is converted from a given *Date* value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="2e659-132">DateValue</span><span class="sxs-lookup"><span data-stu-id="2e659-132">DateValue</span></span>](er-functions-datetime-datevalue.md)           | <span data-ttu-id="2e659-133">تُرجع هذه الوظيفة قيمة *التاريخ* التي تم تحويلها من قيمة *سلسلة* معينة في التنسيق المُحدد وفي الثقافة المُحددة بشكل اختياري إلى قيمة التاريخ/الوقت.</span><span class="sxs-lookup"><span data-stu-id="2e659-133">This function returns a *Date* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date value.</span></span> |

## <a name="type-conversion-functions-in-the-list-category"></a><span data-ttu-id="2e659-134">وظائف تحويل النوع في فئة القائمة</span><span class="sxs-lookup"><span data-stu-id="2e659-134">Type conversion functions in the list category</span></span>

<span data-ttu-id="2e659-135">يوضح الجدول التالي وظائف تحويل النوع في [فئة القائمة](er-functions-category-list.md).</span><span class="sxs-lookup"><span data-stu-id="2e659-135">The following table describes the type conversion functions in the [list category](er-functions-category-list.md).</span></span>

| <span data-ttu-id="2e659-136">الوظيفة</span><span class="sxs-lookup"><span data-stu-id="2e659-136">Function</span></span> | <span data-ttu-id="2e659-137">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="2e659-137">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="2e659-138">قائمة</span><span class="sxs-lookup"><span data-stu-id="2e659-138">List</span></span>](er-functions-list-list.md)                 | <span data-ttu-id="2e659-139">تُرجع هذه الوظيفة قيمة *قائمة السجلات* كقائمة جديدة تم إنشاءها من الوسيطات المُحددة من النوع *الحاوية (سجل)*.</span><span class="sxs-lookup"><span data-stu-id="2e659-139">This function returns a *Record list* value as a new list that is created from specified arguments of the *Container (record)* type.</span></span> |
| [<span data-ttu-id="2e659-140">ListOfFields</span><span class="sxs-lookup"><span data-stu-id="2e659-140">ListOfFields</span></span>](er-functions-list-listoffields.md) | <span data-ttu-id="2e659-141">تُرجع هذه الوظيفة قيمة *قائمة السجل* التي تم إنشاؤها بناءً على بنية الوسيطة المُحددة للنوع *التعداد* أو *الحاوية (السجل)*.</span><span class="sxs-lookup"><span data-stu-id="2e659-141">This function returns a *Record list* value that is created based on the structure of a given argument of the *Enumeration* or *Container (record)* type.</span></span> |
| [<span data-ttu-id="2e659-142">تقسيم</span><span class="sxs-lookup"><span data-stu-id="2e659-142">Split</span></span>](er-functions-list-split.md)               | <span data-ttu-id="2e659-143">تقسم هذه الوظيفة قيمة *السلسلة* المُحددة إلى سلاسل فرعية وتُرجع النتيجة كقيمة *قائمة سجلات* جديدة.</span><span class="sxs-lookup"><span data-stu-id="2e659-143">This function splits the specified *String* value into substrings and returns the result as a new *Record list* value.</span></span> |
| [<span data-ttu-id="2e659-144">StringJoin</span><span class="sxs-lookup"><span data-stu-id="2e659-144">StringJoin</span></span>](er-functions-list-stringjoin.md)     | <span data-ttu-id="2e659-145">تُرجع هذه الوظيفة قيمة *السلسلة* التي تتكون من القيم المتصلة من الحقل المُحدد من قيمة *قائمة السجلات* المُحددة.</span><span class="sxs-lookup"><span data-stu-id="2e659-145">This function returns a *String* value that consists of concatenated values of the specified field from the specified *Record list* value.</span></span> <span data-ttu-id="2e659-146">يُمكن فصل القيم بالمحدد المعين.</span><span class="sxs-lookup"><span data-stu-id="2e659-146">The values can be separated by the specified delimiter.</span></span> |

## <a name="type-conversion-functions-in-the-text-category"></a><span data-ttu-id="2e659-147">وظائف تحويل النوع في فئة النص</span><span class="sxs-lookup"><span data-stu-id="2e659-147">Type conversion functions in the text category</span></span>

<span data-ttu-id="2e659-148">يوضح الجدول التالي وظائف تحويل النوع في [فئة النص](er-functions-category-text.md).</span><span class="sxs-lookup"><span data-stu-id="2e659-148">The following table describes the type conversion functions in the [text category](er-functions-category-text.md).</span></span>

| <span data-ttu-id="2e659-149">الوظيفة</span><span class="sxs-lookup"><span data-stu-id="2e659-149">Function</span></span> | <span data-ttu-id="2e659-150">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="2e659-150">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="2e659-151">Char</span><span class="sxs-lookup"><span data-stu-id="2e659-151">Char</span></span>](er-functions-text-char.md)                 | <span data-ttu-id="2e659-152">تُرجع هذه الوظيفة قيمة *السلسلة* التي تمثل حرف واحد مُشار إليه بواسطة رقم Unicode الموحد.</span><span class="sxs-lookup"><span data-stu-id="2e659-152">This function returns a *String* value that represents a single character that is referenced by the specified Unicode number.</span></span> |
| [<span data-ttu-id="2e659-153">GUIDVALUE</span><span class="sxs-lookup"><span data-stu-id="2e659-153">GuidValue</span></span>](er-functions-text-guidvalue.md)       | <span data-ttu-id="2e659-154">تقوم هذه الوظيفة بتحويل الإدخال المُحدد لنوع *السلسلة* إلى عنصر بيانات من النوع *GUID*.</span><span class="sxs-lookup"><span data-stu-id="2e659-154">This function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span> |
| [<span data-ttu-id="2e659-155">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="2e659-155">NumberFormat</span></span>](er-functions-text-numberformat.md) | <span data-ttu-id="2e659-156">تُرجع هذه الوظيفة قيمة *السلسلة* التي تمثل الرقم المُحدد بالتنسيق المُحدد وفي الثقافة المُحددة بشكل اختياري.</span><span class="sxs-lookup"><span data-stu-id="2e659-156">This function returns a *String* value that represents the specified number in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="2e659-157">QrCode</span><span class="sxs-lookup"><span data-stu-id="2e659-157">QrCode</span></span>](er-functions-text-qrcode.md)             | <span data-ttu-id="2e659-158">تُرجع هذه الوظيفة قيمة *حاوية* تمثل صورة كود استجابة سريع (كود QR) للسلسلة المُحددة بالتنسيق الثنائي. </span><span class="sxs-lookup"><span data-stu-id="2e659-158">This function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span> |
| [<span data-ttu-id="2e659-159">النص</span><span class="sxs-lookup"><span data-stu-id="2e659-159">Text</span></span>](er-functions-text-text.md)                 | <span data-ttu-id="2e659-160">تُرجع هذه الوظيفة قيمة *السلسلة* التي تمثل الرقم المُحدد بعد أن يتم تحويله إلى سلسلة نصية يتم تنسيقها وفقًا لإعدادات الخادم المحلية لمثيل التطبيق الحالي.</span><span class="sxs-lookup"><span data-stu-id="2e659-160">This function returns a *String* value that represents the specified number after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="2e659-161">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="2e659-161">Additional resources</span></span>

[<span data-ttu-id="2e659-162">نظرة عامة حول التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="2e659-162">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="2e659-163">مصمم المعادلات في التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="2e659-163">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="2e659-164">لغة تركيبة التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="2e659-164">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]