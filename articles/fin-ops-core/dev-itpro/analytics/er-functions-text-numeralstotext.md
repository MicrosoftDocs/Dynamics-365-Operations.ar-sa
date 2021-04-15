---
title: NUMERALSTOTEXT ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية NUMERALSTOTEXT (ER).
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: e26890a0d99e0df631a3b3350d284e63aaed8e09
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746137"
---
# <a name="numeralstotext-er-function"></a><span data-ttu-id="96f0f-103">NUMERALSTOTEXT ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="96f0f-103">NUMERALSTOTEXT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="96f0f-104">تقوم وظيفة `NUMERALSTOTEXT` بإرجاع الرقم المحدد كقيمة *سلسلة* بعد كتابته (أي، تحويله إلى سلاسل نصية) باللغة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="96f0f-104">The `NUMERALSTOTEXT` function returns the specified number as a *String* value after it has been spelled out (that is, converted to text strings) in the specified language.</span></span>

## <a name="syntax"></a><span data-ttu-id="96f0f-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="96f0f-105">Syntax</span></span>

```vb
NUMERALSTOTEXT (number, language, currency, print currency name flag, decimal points)
```

## <a name="arguments"></a><span data-ttu-id="96f0f-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="96f0f-106">Arguments</span></span>

<span data-ttu-id="96f0f-107">`number`: *عدد صحيح* أو *حقيقي*</span><span class="sxs-lookup"><span data-stu-id="96f0f-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="96f0f-108">قيمة رقمية تُحدد الرقم الذي يجب كتابته.</span><span class="sxs-lookup"><span data-stu-id="96f0f-108">A numeric value that specifies the number that must be spelled out.</span></span>

<span data-ttu-id="96f0f-109">`language`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="96f0f-109">`language`: *String*</span></span>

<span data-ttu-id="96f0f-110">قيمة *سلسلة* تمثل كود اللغة.</span><span class="sxs-lookup"><span data-stu-id="96f0f-110">A *String* value that represents the language code.</span></span>

<span data-ttu-id="96f0f-111">`currency`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="96f0f-111">`currency`: *String*</span></span>

<span data-ttu-id="96f0f-112">قيمة *سلسلة* تمثل كود العملة.</span><span class="sxs-lookup"><span data-stu-id="96f0f-112">A *String* value that represents the currency code.</span></span>

<span data-ttu-id="96f0f-113">`print currency name flag`: *منطقي*</span><span class="sxs-lookup"><span data-stu-id="96f0f-113">`print currency name flag`: *Boolean*</span></span>

<span data-ttu-id="96f0f-114">قيمة *منطقية* تُشير إلى ما إذا كان يجب إضافة اسم عملة إلى النص المكتوب.</span><span class="sxs-lookup"><span data-stu-id="96f0f-114">A *Boolean* value that indicates whether a currency name must be added to the spelled-out text.</span></span>

<span data-ttu-id="96f0f-115">`decimal points`: *عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="96f0f-115">`decimal points`: *Integer*</span></span>

<span data-ttu-id="96f0f-116">قيمة *عدد صحيح* تُشير إلى عدد المنازل العشرية التي يجب أن تكون موجود في النص المكتوب.</span><span class="sxs-lookup"><span data-stu-id="96f0f-116">An *Integer* value that indicates the number of decimal places that the spelled-out text should have.</span></span>

## <a name="return-values"></a><span data-ttu-id="96f0f-117">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="96f0f-117">Return values</span></span>

<span data-ttu-id="96f0f-118">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="96f0f-118">*String*</span></span>

<span data-ttu-id="96f0f-119">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="96f0f-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="96f0f-120">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="96f0f-120">Usage notes</span></span>

<span data-ttu-id="96f0f-121">كود اللغة اختياري.</span><span class="sxs-lookup"><span data-stu-id="96f0f-121">The language code is optional.</span></span> <span data-ttu-id="96f0f-122">إذا حُدد كسلسلة فارغة، يتم استخدام كود اللغة الخاص بسياق التشغيل بدلاً من ذلك.</span><span class="sxs-lookup"><span data-stu-id="96f0f-122">If it's defined as an empty string, the language code for the running context is used.</span></span> <span data-ttu-id="96f0f-123">كود اللغة الافتراضية هو **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="96f0f-123">The default language code is **EN-US**.</span></span> <span data-ttu-id="96f0f-124">يتم تعريف كود اللغة الخاص بسياق التشغيل في عنصر **مجلد** أو **ملف** من تنسيق إعداد التقارير الإلكترونية (ER) قيد التشغيل.</span><span class="sxs-lookup"><span data-stu-id="96f0f-124">The language code for the running context is defined in a **Folder** or **File** element of the Electronic reporting (ER) format that is running.</span></span>

<span data-ttu-id="96f0f-125">كود العملة اختياري.</span><span class="sxs-lookup"><span data-stu-id="96f0f-125">The currency code is optional.</span></span> <span data-ttu-id="96f0f-126">إذا حُدد كسلسلة فارغة، يتم استخدام عملة الشركة الخاصة للسياق قيد التشغيل.</span><span class="sxs-lookup"><span data-stu-id="96f0f-126">If it's defined as an empty string, the company currency for the running context is used.</span></span>

> [!NOTE] 
> <span data-ttu-id="96f0f-127">يتم تحليل الوسيطات `print currency name flag` و `decimal points` فقط لأكواد اللغات التالية: **CS** و **ET** و **HU** و **LT** و **LV** و **PL** و **RU**.</span><span class="sxs-lookup"><span data-stu-id="96f0f-127">The `print currency name flag` and `decimal points` arguments are analyzed only for the following language codes: **CS**, **ET**, **HU**, **LT**, **LV**, **PL**, and **RU**.</span></span> <span data-ttu-id="96f0f-128">بالإضافة إلى ذلك، يتم تحليل وسيطة `print currency name flag` فقط للشركات التي يدعم فيها سياق البلد أو المنطقة صرف أسماء العملات.</span><span class="sxs-lookup"><span data-stu-id="96f0f-128">Additionally, the `print currency name flag` argument is analyzed only for companies where the country's or region's context supports declension of currency names.</span></span>

## <a name="example-1"></a><span data-ttu-id="96f0f-129">مثال1</span><span class="sxs-lookup"><span data-stu-id="96f0f-129">Example 1</span></span>

<span data-ttu-id="96f0f-130">تُرجع `NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` **"‬‏‫ألف ومئتين وأربعة وثلاثون و 56"**. </span><span class="sxs-lookup"><span data-stu-id="96f0f-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` returns **"One Thousand Two Hundred Thirty Four and 56"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="96f0f-131">مثال2</span><span class="sxs-lookup"><span data-stu-id="96f0f-131">Example 2</span></span>

<span data-ttu-id="96f0f-132">تُرجع `NUMERALSTOTEXT (120, "PL", "", false, 0)` **"Sto dwadzieścia"**. </span><span class="sxs-lookup"><span data-stu-id="96f0f-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)` returns **"Sto dwadzieścia"**.</span></span> 

## <a name="example-3"></a><span data-ttu-id="96f0f-133">المثال الثالث</span><span class="sxs-lookup"><span data-stu-id="96f0f-133">Example 3</span></span>

<span data-ttu-id="96f0f-134">تُرجع وظيفة `NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` **"Сто двадцать евро 21 евроцент"**. </span><span class="sxs-lookup"><span data-stu-id="96f0f-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` returns **"Сто двадцать евро 21 евроцент"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="96f0f-135">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="96f0f-135">Additional resources</span></span>

[<span data-ttu-id="96f0f-136">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="96f0f-136">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]