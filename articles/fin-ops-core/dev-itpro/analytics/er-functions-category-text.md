---
title: قائمة وظائف التقارير الإلكترونية من فئة النص
description: يوفر هذا الموضوع معلومات حول وظائف النص المعتمدة في التقارير الإلكترونية (ER).
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
ms.openlocfilehash: f519d242fe74196b0d12bdc9df4f1b4b0e585752
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916604"
---
# <a name="list-of-er-functions-of-the-text-category"></a><span data-ttu-id="918a2-103">قائمة وظائف التقارير الإلكترونية من فئة النص</span><span class="sxs-lookup"><span data-stu-id="918a2-103">List of ER functions of the text category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="918a2-104">يُمكن استخدام وظائف النص في التقارير الإلكترونية (ER) لاستخراج المعلومات من وتنفيذ العمليات علي مصادر البيانات من نوع البيانات *السلسلة*.</span><span class="sxs-lookup"><span data-stu-id="918a2-104">Electronic reporting (ER) text functions can be used to perform operations on data sources of the *String* data type.</span></span> <span data-ttu-id="918a2-105">يعرض هذا الموضوع ملخصًا لهذه الوظائف.</span><span class="sxs-lookup"><span data-stu-id="918a2-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="918a2-106">قائمة الوظائف المدعومة</span><span class="sxs-lookup"><span data-stu-id="918a2-106">List of supported functions</span></span>

| <span data-ttu-id="918a2-107">الوظيفة</span><span class="sxs-lookup"><span data-stu-id="918a2-107">Function</span></span> | <span data-ttu-id="918a2-108">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="918a2-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="918a2-109">Char</span><span class="sxs-lookup"><span data-stu-id="918a2-109">Char</span></span>](er-functions-text-char.md) | <span data-ttu-id="918a2-110">تُرجع هذه الوظيفة قيمة *السلسلة* التي توضح حرف واحد مُشار إليه بواسطة رقم Unicode الموحد.</span><span class="sxs-lookup"><span data-stu-id="918a2-110">This function returns a *String* value that presents a single character that is referenced by the specified Unicode number.</span></span> |
| [<span data-ttu-id="918a2-111">تسلسل</span><span class="sxs-lookup"><span data-stu-id="918a2-111">Concatenate</span></span>](er-functions-text-concatenate.md) | <span data-ttu-id="918a2-112">تُرجع هذه الوظيفة جميع السلاسل النصية المُحددة كقيمة *السلسلة* بعد ضمها في سلسلة واحدة.</span><span class="sxs-lookup"><span data-stu-id="918a2-112">This function returns  all the specified text strings as a *String* value after they have been joined into one string.</span></span> |
| [<span data-ttu-id="918a2-113">تنسيق</span><span class="sxs-lookup"><span data-stu-id="918a2-113">Format</span></span>](er-functions-text-format.md) | <span data-ttu-id="918a2-114">تُرجع هذه الوظيفة السلسلة المُحددة كقيمة *السلسلة* بعد أن تم تنسيقها باستبدال أي تواجد من **%N** بالوسيطة *N*.</span><span class="sxs-lookup"><span data-stu-id="918a2-114">This function returns the specified string a *String* value after it has been formatted by substituting any occurrences of **%N** with the *N*th argument.</span></span> |
| [<span data-ttu-id="918a2-115">GetEnumValueByName</span><span class="sxs-lookup"><span data-stu-id="918a2-115">GetEnumValueByName</span></span>](er-functions-text-getenumvaluebyname.md) | <span data-ttu-id="918a2-116">تبحث هذه الوظيفة عن قيمة *تعداد* مُحددة في مصدر بيانات التعداد المُحدد باستخدام اسم التعداد المُحدد كقيمة *السلسلة*.</span><span class="sxs-lookup"><span data-stu-id="918a2-116">This function searches for a specific *Enum* value in the specified enumeration data source by using the enumeration name that is specified as a *String* value.</span></span> <span data-ttu-id="918a2-117">إذا تم العثور على قيمة *تعداد* ، تقوم الوظيفة بإرجاعها.</span><span class="sxs-lookup"><span data-stu-id="918a2-117">If the *Enum* value is found, the function returns it.</span></span> |
| [<span data-ttu-id="918a2-118">GUIDVALUE</span><span class="sxs-lookup"><span data-stu-id="918a2-118">GuidValue</span></span>](er-functions-text-guidvalue.md) | <span data-ttu-id="918a2-119">تقوم هذه الوظيفة بتحويل الإدخال المُحدد لنوع *السلسلة* إلى عنصر بيانات من النوع *GUID*.</span><span class="sxs-lookup"><span data-stu-id="918a2-119">This function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span> |
| [<span data-ttu-id="918a2-120">JsonValue</span><span class="sxs-lookup"><span data-stu-id="918a2-120">JsonValue</span></span>](er-functions-text-jsonvalue.md) | <span data-ttu-id="918a2-121">تُحلل هذه الوظيفة البيانات في تنسيق JavaScript Object Notation (JSON) الذي يتم الوصول إليه في المسار المُحدد، ويستخرج قيمة عددية تعتمد على المعرف المحدد.‬  </span><span class="sxs-lookup"><span data-stu-id="918a2-121">This function parses data in JavaScript Object Notation (JSON) format that is accessed at the specified path, and it extracts a scalar value that is based on the specified ID.</span></span> <span data-ttu-id="918a2-122">ثم يقوم بإرجاع القيمة العددية المستخرجة كقيمة *سلسلة* .</span><span class="sxs-lookup"><span data-stu-id="918a2-122">It then returns the extracted scalar value as a *String* value.</span></span> |
| [<span data-ttu-id="918a2-123">إلى اليسار</span><span class="sxs-lookup"><span data-stu-id="918a2-123">Left</span></span>](er-functions-text-left.md) | <span data-ttu-id="918a2-124">تُرجع هذه الوظيفة قيمة *السلسلة* التي توضح العدد المُحدد من الأحرف من بداية السلسلة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="918a2-124">This function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span> |
| [<span data-ttu-id="918a2-125">Len</span><span class="sxs-lookup"><span data-stu-id="918a2-125">Len</span></span>](er-functions-text-len.md) | <span data-ttu-id="918a2-126">تُرجع هذه الوظيفة قيمة *عدد صحيح* توضح عدد الأحرف في السلسلة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="918a2-126">This function returns an *Integer* value that presents the number of characters in the specified string.</span></span> |
| [<span data-ttu-id="918a2-127">Lower</span><span class="sxs-lookup"><span data-stu-id="918a2-127">Lower</span></span>](er-functions-text-lower.md) | <span data-ttu-id="918a2-128">تُرجع هذه الوظيفة سلسلة النص المُحددة كقيمة *السلسلة* بعد أن تم تحويلها إلى أحرف صغيرة.</span><span class="sxs-lookup"><span data-stu-id="918a2-128">This function returns the specified text string as a *String* value after it has been converted to lowercase letters.</span></span> |
| [<span data-ttu-id="918a2-129">Mid</span><span class="sxs-lookup"><span data-stu-id="918a2-129">Mid</span></span>](er-functions-text-mid.md) | <span data-ttu-id="918a2-130">تُرجع هذه الوظيفة قيمة *السلسلة* التي توضح العدد المُحدد من الأحرف من السلسلة المُحددة، بداية من المنصب المُحدد.</span><span class="sxs-lookup"><span data-stu-id="918a2-130">This function returns a *String* value that presents the specified number of characters from the specified string, starting at the specified position.</span></span> |
| [<span data-ttu-id="918a2-131">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="918a2-131">NumberFormat</span></span>](er-functions-text-numberformat.md) | <span data-ttu-id="918a2-132">تُرجع هذه الوظيفة قيمة *السلسلة* التي توضح الرقم المُحدد بالتنسيق المُحدد وفي الثقافة المُحددة بشكل اختياري.</span><span class="sxs-lookup"><span data-stu-id="918a2-132">This function returns a *String* value that presents the specified number in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="918a2-133">NumeralsToText</span><span class="sxs-lookup"><span data-stu-id="918a2-133">NumeralsToText</span></span>](er-functions-text-numeralstotext.md) | <span data-ttu-id="918a2-134">تُرجع هذه الوظيفة الرقم المُحدد كقيمة *السلسلة* بعد كتابته (أي تحويله إلى سلاسل نصية) باللغة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="918a2-134">This function returns the specified number as a *String* value after it has been spelled out (that is, converted to text strings) in the specified language.</span></span> |
| [<span data-ttu-id="918a2-135">PadLeft</span><span class="sxs-lookup"><span data-stu-id="918a2-135">PadLeft</span></span>](er-functions-text-padleft.md) | <span data-ttu-id="918a2-136">تُرجع هذه الوظيفة قيمة *السلسلة* بطول مُحدد، تمت فيه تعبئة بداية السلسلة المُحددة بمثيل واحد أو أكثر من الأحرف المُحددة.</span><span class="sxs-lookup"><span data-stu-id="918a2-136">This function returns a *String* value of the specified length, where the start of the specified string is padded with one or more instances of the specified characters.</span></span> |
| [<span data-ttu-id="918a2-137">QrCode</span><span class="sxs-lookup"><span data-stu-id="918a2-137">QrCode</span></span>](er-functions-text-qrcode.md) | <span data-ttu-id="918a2-138">تُرجع هذه الوظيفة قيمة *حاوية* تمثل صورة كود استجابة سريع (كود QR) للسلسلة المُحددة بالتنسيق الثنائي. </span><span class="sxs-lookup"><span data-stu-id="918a2-138">This function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span> |
| [<span data-ttu-id="918a2-139">استبدال</span><span class="sxs-lookup"><span data-stu-id="918a2-139">Replace</span></span>](er-functions-text-replace.md) | <span data-ttu-id="918a2-140">تُرجع هذه الوظيفة السلسلة النصية المُحددة كقيمة *السلسلة* بعد استبدالها كليًا أو جزئيًا بسلسلة أخرى.</span><span class="sxs-lookup"><span data-stu-id="918a2-140">This function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span> |
| [<span data-ttu-id="918a2-141">إلى اليمين</span><span class="sxs-lookup"><span data-stu-id="918a2-141">Right</span></span>](er-functions-text-right.md) | <span data-ttu-id="918a2-142">تُرجع هذه الوظيفة قيمة *السلسلة* التي توضح العدد المُحدد من الأحرف من نهاية السلسلة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="918a2-142">This function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span> |
| [<span data-ttu-id="918a2-143">النص</span><span class="sxs-lookup"><span data-stu-id="918a2-143">Text</span></span>](er-functions-text-text.md) | <span data-ttu-id="918a2-144">تُرجع هذه الوظيفة الرقم المُحدد كقيمة *سلسلة* بعد أن يتم تحويله إلى سلسلة نصية يتم تنسيقها وفقًا لإعدادات الخادم المحلية لمثيل التطبيق الحالي.</span><span class="sxs-lookup"><span data-stu-id="918a2-144">This function returns the specified number as a *String* value after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span> |
| [<span data-ttu-id="918a2-145">ترجمة</span><span class="sxs-lookup"><span data-stu-id="918a2-145">Translate</span></span>](er-functions-text-translate.md) | <span data-ttu-id="918a2-146">تُرجع هذه الوظيفة السلسلة النصية المُحددة كقيمة *السلسلة* بعد استبدالها كليًا أو جزئيًا بسلسلة أخرى.</span><span class="sxs-lookup"><span data-stu-id="918a2-146">This function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span> |
| [<span data-ttu-id="918a2-147">Trim</span><span class="sxs-lookup"><span data-stu-id="918a2-147">Trim</span></span>](er-functions-text-trim.md) | <span data-ttu-id="918a2-148">تُرجع هذه الوظيفة سلسلة النص المُحددة كقيمة *سلسلة* بعد اقتطاع المسافات البادئة والزائدة، وبعد أن تمت إزالة المسافات المتعددة بين الكلمات.</span><span class="sxs-lookup"><span data-stu-id="918a2-148">This function returns the specified text string as a *String* value after leading and trailing spaces have been truncated, and after multiple spaces between words have been removed.</span></span> |
| [<span data-ttu-id="918a2-149">Upper</span><span class="sxs-lookup"><span data-stu-id="918a2-149">Upper</span></span>](er-functions-text-upper.md) | <span data-ttu-id="918a2-150">تُرجع هذه الوظيفة سلسلة النص المُحددة كقيمة *السلسلة* بعد أن تم تحويلها إلى أحرف كبيرة.</span><span class="sxs-lookup"><span data-stu-id="918a2-150">This function returns the specified text string as a *String* value after it has been converted to uppercase letters.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="918a2-151">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="918a2-151">Additional resources</span></span>

[<span data-ttu-id="918a2-152">نظرة عامة حول التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="918a2-152">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="918a2-153">مصمم المعادلات في التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="918a2-153">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="918a2-154">لغة تركيبة التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="918a2-154">Electronic reporting formula language</span></span>](er-formula-language.md)