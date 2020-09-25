---
title: وظيفة DATETIMEFORMAT ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية DATETIMEFORMAT (ER).
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
ms.openlocfilehash: 65b988e6c58aed35577288e01157b8c1f76e6efd
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744853"
---
# <a name="datetimeformat-er-function"></a><span data-ttu-id="ffb0f-103">وظيفة DATETIMEFORMAT ER</span><span class="sxs-lookup"><span data-stu-id="ffb0f-103">DATETIMEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ffb0f-104">تُرجع الوظيفة `DATETIMEFORMAT` قيمة *السلسلة* التي تمثل قيمة تاريخ مُعيّن كنص في التنسيق المُحدد وفي [الثقافة](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) المُحددة بشكل اختياري.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-104">The `DATETIMEFORMAT` function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="ffb0f-105">لمزيد من المعلومات حول التنسيقات المعتمدة، راجع [قياسي](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) و [مخصص](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="ffb0f-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="ffb0f-106">بناء الجملة 1</span><span class="sxs-lookup"><span data-stu-id="ffb0f-106">Syntax 1</span></span>

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a><span data-ttu-id="ffb0f-107">بناء الجملة 2</span><span class="sxs-lookup"><span data-stu-id="ffb0f-107">Syntax 2</span></span>

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="ffb0f-108">الوسائط</span><span class="sxs-lookup"><span data-stu-id="ffb0f-108">Arguments</span></span>

<span data-ttu-id="ffb0f-109">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="ffb0f-109">`datetime`: *DateTime*</span></span>

<span data-ttu-id="ffb0f-110">قيمة التاريخ/الوقت التي تمثل التاريخ والوقت المراد تنسيقه.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-110">A date/time value that represents the date and time to format.</span></span>

<span data-ttu-id="ffb0f-111">`format`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="ffb0f-111">`format`: *String*</span></span>

<span data-ttu-id="ffb0f-112">تنسيق سلسلة الإخراج.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-112">The format of the output string.</span></span>

<span data-ttu-id="ffb0f-113">`culture`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="ffb0f-113">`culture`: *String*</span></span>

<span data-ttu-id="ffb0f-114">الثقافة التي سيتم استخدامها للتنسيق.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-114">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="ffb0f-115">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="ffb0f-115">Return values</span></span>

<span data-ttu-id="ffb0f-116">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="ffb0f-116">*String*</span></span>

<span data-ttu-id="ffb0f-117">قيمة السلسلة الناتجة.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-117">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ffb0f-118">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="ffb0f-118">Usage notes</span></span>

<span data-ttu-id="ffb0f-119">عندما لا يتم تعريف الثقافة كوسيطة للوظيفة التي تم استدعائها، يتم تعريف قيمة `culture` عن طريق سياق الاستدعاء.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="ffb0f-120">على سبيل المثال، إذا تم استدعاء الوظيفة `DATETIMEFORMAT` باستخدام بناء الجملة 1 في تنسيق التقارير الإلكترونية (ER) لعنصر **FILE** تم تكوينه لاستخدام الثقافة الألمانية، فسوف يتم التحويل باستخدام الثقافة الألمانية.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-120">For example, if the `DATETIMEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="ffb0f-121">قيمة `culture` الافتراضية هي **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-121">The default `culture` value is **EN-US**.</span></span>

<span data-ttu-id="ffb0f-122">عندما تقوم الوظيفة `DATETIMEFORMAT` بتحويل قيمة تاريخ/وقت مُحدد، فإنها تعتبر إعداد المنطقة الزمنية لمستخدم التطبيق الذي يقوم بتشغيل تنسيق ER الذي تمت استدعاء الوظيفة في سياقه.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-122">When the `DATETIMEFORMAT` function converts a given date/time value, it considers the time zone setting of the application user who is running the ER format that the function is called in the context of.</span></span>

## <a name="example-1"></a><span data-ttu-id="ffb0f-123">مثال1</span><span class="sxs-lookup"><span data-stu-id="ffb0f-123">Example 1</span></span>

<span data-ttu-id="ffb0f-124">يُرجع التعبير `DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` قيمة تاريخ/وقت خادم التطبيق الحالي، 24 ديسمبر 2015، كـ **"24-12-2015"**، بناءً على التنسيق المخصص المُحدد.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-124">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="ffb0f-125">مثال2</span><span class="sxs-lookup"><span data-stu-id="ffb0f-125">Example 2</span></span>

<span data-ttu-id="ffb0f-126">تُرجع وظيفة `DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` قيمة تاريخ/وقت جلسة التطبيق الحالية، 24 ديسمبر 2015، كـ **"24.12.2015"**، بناءً على الثقافة الألمانية المُحددة والتنسيق المُحدد. </span><span class="sxs-lookup"><span data-stu-id="ffb0f-126">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="example-3"></a><span data-ttu-id="ffb0f-127">المثال الثالث</span><span class="sxs-lookup"><span data-stu-id="ffb0f-127">Example 3</span></span>

<span data-ttu-id="ffb0f-128">تُرجع  `DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` قيمة السلسلة **2019-11-12T08:00:00.0000000-08:00** عندما يتم استدعاءها أثناء عملية تم البدء فيها بواسطة مستخدم تطبيق لديه قيمة منطقة زمنية **‏‏‫(GMT-08:00) توقيت الباسيفيكي (الولايات المتحدة وكند)‬‬** في قسم **تفضيلات البلد/المنطقة واللغة‬**.</span><span class="sxs-lookup"><span data-stu-id="ffb0f-128">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returns the string value **2019-11-12T08:00:00.0000000-08:00** when it's called during a process that was initiated by an application user who has the time zone value **(GMT-08:00) Pacific Time (US & Canada)** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ffb0f-129">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="ffb0f-129">Additional resources</span></span>

[<span data-ttu-id="ffb0f-130">دلات التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="ffb0f-130">Date and time functions</span></span>](er-functions-category-datetime.md)
