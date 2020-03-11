---
title: وظيفة DATEFORMAT ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية DATEFORMAT (ER).
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 759ccd3cf16c6c109faf44cea350745e3b2bff0b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042425"
---
# <span data-ttu-id="97749-103"><a name="DATEFORMAT">وظيفة DATEFORMAT ER</a></span><span class="sxs-lookup"><span data-stu-id="97749-103"><a name="DATEFORMAT">DATEFORMAT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="97749-104">تُرجع الوظيفة `DATEFORMAT` قيمة *السلسلة* التي تمثل قيمة تاريخ مُعيّن كنص في التنسيق المُحدد وفي [الثقافة](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) المُحددة بشكل اختياري.</span><span class="sxs-lookup"><span data-stu-id="97749-104">The `DATEFORMAT` function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="97749-105">(لمزيد من المعلومات حول التنسيقات المعتمدة، راجع [قياسي](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) و [مخصص](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="97749-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="97749-106">بناء الجملة 1</span><span class="sxs-lookup"><span data-stu-id="97749-106">Syntax 1</span></span>

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a><span data-ttu-id="97749-107">بناء الجملة 2</span><span class="sxs-lookup"><span data-stu-id="97749-107">Syntax 2</span></span>

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="97749-108">الوسائط</span><span class="sxs-lookup"><span data-stu-id="97749-108">Arguments</span></span>

<span data-ttu-id="97749-109">`date`: *التاريخ*</span><span class="sxs-lookup"><span data-stu-id="97749-109">`date`: *Date*</span></span>

<span data-ttu-id="97749-110">قيمة التاريخ التي تمثل تاريخ التنسيق.</span><span class="sxs-lookup"><span data-stu-id="97749-110">A date value that represents the date to format.</span></span>

<span data-ttu-id="97749-111">`format`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="97749-111">`format`: *String*</span></span>

<span data-ttu-id="97749-112">تنسيق سلسلة الإخراج.</span><span class="sxs-lookup"><span data-stu-id="97749-112">The format of the output string.</span></span>

<span data-ttu-id="97749-113">`culture`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="97749-113">`culture`: *String*</span></span>

<span data-ttu-id="97749-114">الثقافة التي سيتم استخدامها للتنسيق.</span><span class="sxs-lookup"><span data-stu-id="97749-114">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="97749-115">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="97749-115">Return values</span></span>

<span data-ttu-id="97749-116">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="97749-116">*String*</span></span>

<span data-ttu-id="97749-117">قيمة السلسلة الناتجة.</span><span class="sxs-lookup"><span data-stu-id="97749-117">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="97749-118">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="97749-118">Usage notes</span></span>

<span data-ttu-id="97749-119">عندما لا يتم تعريف الثقافة كوسيطة للوظيفة التي تم استدعائها، يتم تعريف قيمة `culture` عن طريق سياق الاستدعاء.</span><span class="sxs-lookup"><span data-stu-id="97749-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="97749-120">على سبيل المثال، إذا تم استدعاء الوظيفة `DATEFORMAT` باستخدام بناء الجملة 1 في تنسيق التقارير الإلكترونية (ER) لعنصر **FILE** تم تكوينه لاستخدام الثقافة الألمانية، فسوف يتم التحويل باستخدام الثقافة الألمانية.</span><span class="sxs-lookup"><span data-stu-id="97749-120">For example, if the `DATEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="97749-121">قيمة `culture` الافتراضية هي **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="97749-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="97749-122">مثال1</span><span class="sxs-lookup"><span data-stu-id="97749-122">Example 1</span></span>

<span data-ttu-id="97749-123">تُرجع وظيفة `DATEFORMAT (TODAY (), "dd-MM-yyyy")` تاريخ خادم التطبيق الحالي، 24 ديسمبر 2015، كسلسلة **"24-12-2015"**، بناءً على التنسيق المخصص المُحدد. </span><span class="sxs-lookup"><span data-stu-id="97749-123">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="97749-124">مثال2</span><span class="sxs-lookup"><span data-stu-id="97749-124">Example 2</span></span>

<span data-ttu-id="97749-125">تُرجع الوظيفة `DATEFORMAT (SESSIONTODAY (), "d", "DE")` تاريخ جلسة التطبيق الحالية، 24 ديسمبر 2015، كسلسلة **"24-12-2015"**، بناءً على الثقافة الألمانية المُحددة والتنسيق المُحدد.</span><span class="sxs-lookup"><span data-stu-id="97749-125">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string  **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="97749-126">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="97749-126">Additional resources</span></span>

[<span data-ttu-id="97749-127">دلات التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="97749-127">Date and time functions</span></span>](er-functions-category-datetime.md)
