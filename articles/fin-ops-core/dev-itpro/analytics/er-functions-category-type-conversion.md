---
title: قائمة وظائف التقارير الإلكترونية في فئة تحويل النوع
description: يوفر هذا الموضوع معلومات حول وظائف التحويل المعتمدة في التقارير الإلكترونية (ER).
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 5613496d3131ccd39b198cac214eb791a6d07355
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561508"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a><span data-ttu-id="fdb92-103">قائمة وظائف التقارير الإلكترونية في فئة تحويل النوع</span><span class="sxs-lookup"><span data-stu-id="fdb92-103">List of ER functions in the type conversion category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fdb92-104">يُمكن استخدام وظائف تحويل نوع التقارير الإلكترونية (ER) لتحويل القيم بين الأنواع.</span><span class="sxs-lookup"><span data-stu-id="fdb92-104">Electronic reporting (ER) type conversion functions can be used to convert values between types.</span></span> <span data-ttu-id="fdb92-105">يعرض هذا الموضوع ملخصًا لهذه الوظائف.</span><span class="sxs-lookup"><span data-stu-id="fdb92-105">This topic provides a summary of these functions.</span></span>

## <a name="type-conversion-functions"></a><span data-ttu-id="fdb92-106">وظائف تحويل النوع</span><span class="sxs-lookup"><span data-stu-id="fdb92-106">Type conversion functions</span></span>

| <span data-ttu-id="fdb92-107">الوظيفة</span><span class="sxs-lookup"><span data-stu-id="fdb92-107">Function</span></span> | <span data-ttu-id="fdb92-108">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="fdb92-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="fdb92-109">Int64Value</span><span class="sxs-lookup"><span data-stu-id="fdb92-109">Int64Value</span></span>](er-functions-conversion-int64value.md)   | <span data-ttu-id="fdb92-110">تُرجع هذه الوظيفة قيمة *Int64* التي تمثل السلسلة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="fdb92-110">This function returns an *Int64* value that represents the specified string.</span></span> |
| [<span data-ttu-id="fdb92-111">IntValue</span><span class="sxs-lookup"><span data-stu-id="fdb92-111">IntValue</span></span>](er-functions-conversion-intvalue.md)       | <span data-ttu-id="fdb92-112">تُرجع هذه الوظيفة قيمة *Int* التي تمثل السلسلة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="fdb92-112">This function returns an *Int* value that represents the specified string.</span></span> |
| [<span data-ttu-id="fdb92-113">NumberValue</span><span class="sxs-lookup"><span data-stu-id="fdb92-113">NumberValue</span></span>](er-functions-conversion-numbervalue.md) | <span data-ttu-id="fdb92-114">تُرجع هذه الوظيفة قيمة *حقيقة* يتم تحويلها من قيمة *السلسلة* المُحددة.</span><span class="sxs-lookup"><span data-stu-id="fdb92-114">This function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="fdb92-115">في أثناء التحويل، يوضع في الاعتبار فواصل التجميع العشرية والرقمية المُحددة.</span><span class="sxs-lookup"><span data-stu-id="fdb92-115">During the conversion, the specified decimal and digit grouping separators are considered.</span></span> |
| [<span data-ttu-id="fdb92-116">القيمة</span><span class="sxs-lookup"><span data-stu-id="fdb92-116">Value</span></span>](er-functions-conversion-value.md)             | <span data-ttu-id="fdb92-117">تُرجع هذه الوظيفة قيمة *حقيقة* يتم تحويلها من قيمة *السلسلة* المُحددة.</span><span class="sxs-lookup"><span data-stu-id="fdb92-117">This function returns a *Real* value that is converted from the specified *String* value.</span></span> |

## <a name="type-conversion-functions-in-the-container-category"></a><span data-ttu-id="fdb92-118">وظائف تحويل النوع في فئة الحاوية</span><span class="sxs-lookup"><span data-stu-id="fdb92-118">Type conversion functions in the container category</span></span>

<span data-ttu-id="fdb92-119">يوضح الجدول التالي وظائف تحويل النوع في فئة [الحاوية](er-functions-category-container.md).</span><span class="sxs-lookup"><span data-stu-id="fdb92-119">The following table describes the type conversion functions in the [container](er-functions-category-container.md) category.</span></span>

| <span data-ttu-id="fdb92-120">الوظيفة</span><span class="sxs-lookup"><span data-stu-id="fdb92-120">Function</span></span> | <span data-ttu-id="fdb92-121">الوصف</span><span class="sxs-lookup"><span data-stu-id="fdb92-121">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="fdb92-122">Base64StringToContainer</span><span class="sxs-lookup"><span data-stu-id="fdb92-122">Base64StringToContainer</span></span>](er-functions-container-base64stringtocontainer.md) | <span data-ttu-id="fdb92-123">تقوم دالة بتحويل الإدخال المُحدد لنوع *السلسلة* إلى عنصر بيانات من النوع *الحاوية*.</span><span class="sxs-lookup"><span data-stu-id="fdb92-123">This function converts the specified input of the *String* type to a data item of the *Container* type.</span></span> |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a><span data-ttu-id="fdb92-124">وظائف تحويل النوع في فئة التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="fdb92-124">Type conversion functions in the date and time category</span></span>

<span data-ttu-id="fdb92-125">يوضح الجدول التالي وظائف تحويل النوع في [فئة التاريخ والوقت](er-functions-category-datetime.md).</span><span class="sxs-lookup"><span data-stu-id="fdb92-125">The following table describes the type conversion functions in the [date and time category](er-functions-category-datetime.md).</span></span>

| <span data-ttu-id="fdb92-126">الوظيفة</span><span class="sxs-lookup"><span data-stu-id="fdb92-126">Function</span></span> | <span data-ttu-id="fdb92-127">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="fdb92-127">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="fdb92-128">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="fdb92-128">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md)   | <span data-ttu-id="fdb92-129">تُرجع هذه الوظيفة قيمة *DateTime* التي تم تحويلها من قيمة *سلسلة* معينة في التنسيق المُحدد وفي الثقافة المُحددة بشكل اختياري إلى قيمة التاريخ/الوقت.</span><span class="sxs-lookup"><span data-stu-id="fdb92-129">This function returns a *DateTime* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="fdb92-130">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="fdb92-130">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="fdb92-131">تُرجع هذه الوظيفة قيمة *DateTime* التي تم تحويلها من قيمة *تاريخ* معين إلى قيمة التاريخ/الوقت بالتوقيت العالمي المنسق (توقيت جرينتش المتوسط \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="fdb92-131">This function returns a *DateTime* value that is converted from a given *Date* value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="fdb92-132">DateValue</span><span class="sxs-lookup"><span data-stu-id="fdb92-132">DateValue</span></span>](er-functions-datetime-datevalue.md)           | <span data-ttu-id="fdb92-133">تُرجع هذه الوظيفة قيمة *التاريخ* التي تم تحويلها من قيمة *سلسلة* معينة في التنسيق المُحدد وفي الثقافة المُحددة بشكل اختياري إلى قيمة التاريخ/الوقت.</span><span class="sxs-lookup"><span data-stu-id="fdb92-133">This function returns a *Date* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date value.</span></span> |

## <a name="type-conversion-functions-in-the-list-category"></a><span data-ttu-id="fdb92-134">وظائف تحويل النوع في فئة القائمة</span><span class="sxs-lookup"><span data-stu-id="fdb92-134">Type conversion functions in the list category</span></span>

<span data-ttu-id="fdb92-135">يوضح الجدول التالي وظائف تحويل النوع في [فئة القائمة](er-functions-category-list.md).</span><span class="sxs-lookup"><span data-stu-id="fdb92-135">The following table describes the type conversion functions in the [list category](er-functions-category-list.md).</span></span>

| <span data-ttu-id="fdb92-136">الوظيفة</span><span class="sxs-lookup"><span data-stu-id="fdb92-136">Function</span></span> | <span data-ttu-id="fdb92-137">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="fdb92-137">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="fdb92-138">قائمة</span><span class="sxs-lookup"><span data-stu-id="fdb92-138">List</span></span>](er-functions-list-list.md)                 | <span data-ttu-id="fdb92-139">تُرجع هذه الوظيفة قيمة *قائمة السجلات* كقائمة جديدة تم إنشاءها من الوسيطات المُحددة من النوع *الحاوية (سجل)*.</span><span class="sxs-lookup"><span data-stu-id="fdb92-139">This function returns a *Record list* value as a new list that is created from specified arguments of the *Container (record)* type.</span></span> |
| [<span data-ttu-id="fdb92-140">ListOfFields</span><span class="sxs-lookup"><span data-stu-id="fdb92-140">ListOfFields</span></span>](er-functions-list-listoffields.md) | <span data-ttu-id="fdb92-141">تُرجع هذه الوظيفة قيمة *قائمة السجل* التي تم إنشاؤها بناءً على بنية الوسيطة المُحددة للنوع *التعداد* أو *الحاوية (السجل)*.</span><span class="sxs-lookup"><span data-stu-id="fdb92-141">This function returns a *Record list* value that is created based on the structure of a given argument of the *Enumeration* or *Container (record)* type.</span></span> |
| [<span data-ttu-id="fdb92-142">تقسيم</span><span class="sxs-lookup"><span data-stu-id="fdb92-142">Split</span></span>](er-functions-list-split.md)               | <span data-ttu-id="fdb92-143">تقسم هذه الوظيفة قيمة *السلسلة* المُحددة إلى سلاسل فرعية وتُرجع النتيجة كقيمة *قائمة سجلات* جديدة.</span><span class="sxs-lookup"><span data-stu-id="fdb92-143">This function splits the specified *String* value into substrings and returns the result as a new *Record list* value.</span></span> |
| [<span data-ttu-id="fdb92-144">StringJoin</span><span class="sxs-lookup"><span data-stu-id="fdb92-144">StringJoin</span></span>](er-functions-list-stringjoin.md)     | <span data-ttu-id="fdb92-145">تُرجع هذه الوظيفة قيمة *السلسلة* التي تتكون من القيم المتصلة من الحقل المُحدد من قيمة *قائمة السجلات* المُحددة.</span><span class="sxs-lookup"><span data-stu-id="fdb92-145">This function returns a *String* value that consists of concatenated values of the specified field from the specified *Record list* value.</span></span> <span data-ttu-id="fdb92-146">يُمكن فصل القيم بالمحدد المعين.</span><span class="sxs-lookup"><span data-stu-id="fdb92-146">The values can be separated by the specified delimiter.</span></span> |

## <a name="type-conversion-functions-in-the-text-category"></a><span data-ttu-id="fdb92-147">وظائف تحويل النوع في فئة النص</span><span class="sxs-lookup"><span data-stu-id="fdb92-147">Type conversion functions in the text category</span></span>

<span data-ttu-id="fdb92-148">يوضح الجدول التالي وظائف تحويل النوع في [فئة النص](er-functions-category-text.md).</span><span class="sxs-lookup"><span data-stu-id="fdb92-148">The following table describes the type conversion functions in the [text category](er-functions-category-text.md).</span></span>

| <span data-ttu-id="fdb92-149">الوظيفة</span><span class="sxs-lookup"><span data-stu-id="fdb92-149">Function</span></span> | <span data-ttu-id="fdb92-150">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="fdb92-150">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="fdb92-151">Char</span><span class="sxs-lookup"><span data-stu-id="fdb92-151">Char</span></span>](er-functions-text-char.md)                 | <span data-ttu-id="fdb92-152">تُرجع هذه الوظيفة قيمة *السلسلة* التي تمثل حرف واحد مُشار إليه بواسطة رقم Unicode الموحد.</span><span class="sxs-lookup"><span data-stu-id="fdb92-152">This function returns a *String* value that represents a single character that is referenced by the specified Unicode number.</span></span> |
| [<span data-ttu-id="fdb92-153">GUIDVALUE</span><span class="sxs-lookup"><span data-stu-id="fdb92-153">GuidValue</span></span>](er-functions-text-guidvalue.md)       | <span data-ttu-id="fdb92-154">تقوم هذه الوظيفة بتحويل الإدخال المُحدد لنوع *السلسلة* إلى عنصر بيانات من النوع *GUID*.</span><span class="sxs-lookup"><span data-stu-id="fdb92-154">This function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span> |
| [<span data-ttu-id="fdb92-155">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="fdb92-155">NumberFormat</span></span>](er-functions-text-numberformat.md) | <span data-ttu-id="fdb92-156">تُرجع هذه الوظيفة قيمة *السلسلة* التي تمثل الرقم المُحدد بالتنسيق المُحدد وفي الثقافة المُحددة بشكل اختياري.</span><span class="sxs-lookup"><span data-stu-id="fdb92-156">This function returns a *String* value that represents the specified number in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="fdb92-157">QrCode</span><span class="sxs-lookup"><span data-stu-id="fdb92-157">QrCode</span></span>](er-functions-text-qrcode.md)             | <span data-ttu-id="fdb92-158">تُرجع هذه الوظيفة قيمة *حاوية* تمثل صورة كود استجابة سريع (كود QR) للسلسلة المُحددة بالتنسيق الثنائي. </span><span class="sxs-lookup"><span data-stu-id="fdb92-158">This function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span> |
| [<span data-ttu-id="fdb92-159">النص</span><span class="sxs-lookup"><span data-stu-id="fdb92-159">Text</span></span>](er-functions-text-text.md)                 | <span data-ttu-id="fdb92-160">تُرجع هذه الوظيفة قيمة *السلسلة* التي تمثل الرقم المُحدد بعد أن يتم تحويله إلى سلسلة نصية يتم تنسيقها وفقًا لإعدادات الخادم المحلية لمثيل التطبيق الحالي.</span><span class="sxs-lookup"><span data-stu-id="fdb92-160">This function returns a *String* value that represents the specified number after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="fdb92-161">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="fdb92-161">Additional resources</span></span>

[<span data-ttu-id="fdb92-162">نظرة عامة حول التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="fdb92-162">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="fdb92-163">مصمم المعادلات في التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="fdb92-163">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="fdb92-164">لغة تركيبة التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="fdb92-164">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]