---
title: وظيفة DATEFORMAT ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية DATEFORMAT (ER).
author: NickSelin
manager: kfend
ms.date: 01/04/2021
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
ms.openlocfilehash: 0a9580b0ab9e472796375f498059ec0864a919ce
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563644"
---
# <a name="dateformat-er-function"></a><span data-ttu-id="ef70a-103">وظيفة DATEFORMAT ER</span><span class="sxs-lookup"><span data-stu-id="ef70a-103">DATEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ef70a-104">تُرجع الوظيفة `DATEFORMAT` قيمة *السلسلة* التي تمثل قيمة تاريخ مُعيّن كنص في التنسيق المُحدد وفي [الثقافة](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) المُحددة بشكل اختياري.</span><span class="sxs-lookup"><span data-stu-id="ef70a-104">The `DATEFORMAT` function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="ef70a-105">لمزيد من المعلومات حول التنسيقات المعتمدة، راجع [قياسي](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) و [مخصص](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="ef70a-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="ef70a-106">بناء الجملة 1</span><span class="sxs-lookup"><span data-stu-id="ef70a-106">Syntax 1</span></span>

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a><span data-ttu-id="ef70a-107">بناء الجملة 2</span><span class="sxs-lookup"><span data-stu-id="ef70a-107">Syntax 2</span></span>

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="ef70a-108">الوسائط</span><span class="sxs-lookup"><span data-stu-id="ef70a-108">Arguments</span></span>

<span data-ttu-id="ef70a-109">`date`: *التاريخ*</span><span class="sxs-lookup"><span data-stu-id="ef70a-109">`date`: *Date*</span></span>

<span data-ttu-id="ef70a-110">قيمة التاريخ التي تمثل تاريخ التنسيق.</span><span class="sxs-lookup"><span data-stu-id="ef70a-110">A date value that represents the date to format.</span></span>

<span data-ttu-id="ef70a-111">`format`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="ef70a-111">`format`: *String*</span></span>

<span data-ttu-id="ef70a-112">تنسيق سلسلة الإخراج.</span><span class="sxs-lookup"><span data-stu-id="ef70a-112">The format of the output string.</span></span>

> [!NOTE]
> <span data-ttu-id="ef70a-113">تكون سلسله التنسيق حساسة لحاله الأحرف عند استخدام اما تنسيق قياسي أو تنسيق مخصص.</span><span class="sxs-lookup"><span data-stu-id="ef70a-113">The format string is case-sensitive when you use either a standard format or a custom format.</span></span> <span data-ttu-id="ef70a-114">علي سبيل المثال، يقوم محدد التنسيق [القياسي](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) "d" بإرجاع التاريخ باستخدام نمط التاريخ القصير، بينما يقوم محدد التنسيق القياسي "d" بإرجاع التاريخ باستخدام نمط التاريخ الطويل.</span><span class="sxs-lookup"><span data-stu-id="ef70a-114">For example, the [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) "d" format specifier returns the date by using the short date pattern, whereas the standard "D" format specifier returns the date by using the long date pattern.</span></span> <span data-ttu-id="ef70a-115">بالاضافه إلى ذلك ، يقوم محدد التنسيق [المخصص](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) "m" بإرجاع الشهر من 1 إلى 12، بينما يقوم محدد التنسيق المخصص "m" بإرجاع الدقيقة من 0 إلى 59.</span><span class="sxs-lookup"><span data-stu-id="ef70a-115">Additionally, the [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) "M" format specifier returns the month from 1 through 12, whereas the custom "m" format specifier returns the minute from 0 through 59.</span></span>

<span data-ttu-id="ef70a-116">`culture`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="ef70a-116">`culture`: *String*</span></span>

<span data-ttu-id="ef70a-117">الثقافة التي سيتم استخدامها للتنسيق.</span><span class="sxs-lookup"><span data-stu-id="ef70a-117">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="ef70a-118">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="ef70a-118">Return values</span></span>

<span data-ttu-id="ef70a-119">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="ef70a-119">*String*</span></span>

<span data-ttu-id="ef70a-120">قيمة السلسلة الناتجة.</span><span class="sxs-lookup"><span data-stu-id="ef70a-120">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ef70a-121">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="ef70a-121">Usage notes</span></span>

<span data-ttu-id="ef70a-122">إذا لم يتم تعريف الثقافة كوسيطة للوظيفة التي تم استدعائها، يتم تعريف قيمة `culture` عن طريق سياق الاستدعاء.</span><span class="sxs-lookup"><span data-stu-id="ef70a-122">If the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="ef70a-123">على سبيل المثال، إذا تم استدعاء الوظيفة `DATEFORMAT` باستخدام بناء الجملة 1 في تنسيق التقارير الإلكترونية (ER) لعنصر **FILE** تم تكوينه لاستخدام الثقافة الألمانية، فسوف يتم التحويل باستخدام الثقافة الألمانية.</span><span class="sxs-lookup"><span data-stu-id="ef70a-123">For example, if the `DATEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="ef70a-124">قيمة `culture` الافتراضية هي **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="ef70a-124">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="ef70a-125">مثال1</span><span class="sxs-lookup"><span data-stu-id="ef70a-125">Example 1</span></span>

<span data-ttu-id="ef70a-126">تُرجع وظيفة `DATEFORMAT (TODAY (), "dd-MM-yyyy")` تاريخ خادم التطبيق الحالي، 24 ديسمبر 2015، كسلسلة **"24-12-2015"**، بناءً على التنسيق المخصص المُحدد. </span><span class="sxs-lookup"><span data-stu-id="ef70a-126">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="ef70a-127">مثال2</span><span class="sxs-lookup"><span data-stu-id="ef70a-127">Example 2</span></span>

<span data-ttu-id="ef70a-128">تُرجع وظيفة `DATEFORMAT (SESSIONTODAY (), "d", "DE")` قيمة تاريخ جلسة التطبيق الحالية، 24 ديسمبر 2015، كسلسلة **"24-12-2015"**، بناءً على الثقافة الألمانية المُحددة والتنسيق المُحدد. </span><span class="sxs-lookup"><span data-stu-id="ef70a-128">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ef70a-129">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="ef70a-129">Additional resources</span></span>

[<span data-ttu-id="ef70a-130">دلات التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="ef70a-130">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]