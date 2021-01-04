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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d42767b814f36eb75b4a43d07c663b2dd1b2c879
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684931"
---
# <a name="datetimeformat-er-function"></a><span data-ttu-id="81cb0-103">وظيفة DATETIMEFORMAT ER</span><span class="sxs-lookup"><span data-stu-id="81cb0-103">DATETIMEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="81cb0-104">تُرجع الوظيفة `DATETIMEFORMAT` قيمة *السلسلة* التي تمثل قيمة تاريخ مُعيّن كنص في التنسيق المُحدد وفي [الثقافة](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) المُحددة بشكل اختياري.</span><span class="sxs-lookup"><span data-stu-id="81cb0-104">The `DATETIMEFORMAT` function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="81cb0-105">لمزيد من المعلومات حول التنسيقات المعتمدة، راجع [قياسي](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) و [مخصص](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="81cb0-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="81cb0-106">بناء الجملة 1</span><span class="sxs-lookup"><span data-stu-id="81cb0-106">Syntax 1</span></span>

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a><span data-ttu-id="81cb0-107">بناء الجملة 2</span><span class="sxs-lookup"><span data-stu-id="81cb0-107">Syntax 2</span></span>

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="81cb0-108">الوسائط</span><span class="sxs-lookup"><span data-stu-id="81cb0-108">Arguments</span></span>

<span data-ttu-id="81cb0-109">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="81cb0-109">`datetime`: *DateTime*</span></span>

<span data-ttu-id="81cb0-110">قيمة التاريخ/الوقت التي تمثل التاريخ والوقت المراد تنسيقه.</span><span class="sxs-lookup"><span data-stu-id="81cb0-110">A date/time value that represents the date and time to format.</span></span>

<span data-ttu-id="81cb0-111">`format`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="81cb0-111">`format`: *String*</span></span>

<span data-ttu-id="81cb0-112">تنسيق سلسلة الإخراج.</span><span class="sxs-lookup"><span data-stu-id="81cb0-112">The format of the output string.</span></span>

<span data-ttu-id="81cb0-113">`culture`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="81cb0-113">`culture`: *String*</span></span>

<span data-ttu-id="81cb0-114">الثقافة التي سيتم استخدامها للتنسيق.</span><span class="sxs-lookup"><span data-stu-id="81cb0-114">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="81cb0-115">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="81cb0-115">Return values</span></span>

<span data-ttu-id="81cb0-116">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="81cb0-116">*String*</span></span>

<span data-ttu-id="81cb0-117">قيمة السلسلة الناتجة.</span><span class="sxs-lookup"><span data-stu-id="81cb0-117">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="81cb0-118">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="81cb0-118">Usage notes</span></span>

<span data-ttu-id="81cb0-119">عندما لا يتم تعريف الثقافة كوسيطة للوظيفة التي تم استدعائها، يتم تعريف قيمة `culture` عن طريق سياق الاستدعاء.</span><span class="sxs-lookup"><span data-stu-id="81cb0-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="81cb0-120">على سبيل المثال، إذا تم استدعاء الوظيفة `DATETIMEFORMAT` باستخدام بناء الجملة 1 في تنسيق التقارير الإلكترونية (ER) لعنصر **FILE** تم تكوينه لاستخدام الثقافة الألمانية، فسوف يتم التحويل باستخدام الثقافة الألمانية.</span><span class="sxs-lookup"><span data-stu-id="81cb0-120">For example, if the `DATETIMEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="81cb0-121">قيمة `culture` الافتراضية هي **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="81cb0-121">The default `culture` value is **EN-US**.</span></span>

<span data-ttu-id="81cb0-122">عندما تقوم الوظيفة `DATETIMEFORMAT` بتحويل قيمة تاريخ/وقت مُحدد، فإنها تعتبر إعداد المنطقة الزمنية لمستخدم التطبيق الذي يقوم بتشغيل تنسيق ER الذي تمت استدعاء الوظيفة في سياقه.</span><span class="sxs-lookup"><span data-stu-id="81cb0-122">When the `DATETIMEFORMAT` function converts a given date/time value, it considers the time zone setting of the application user who is running the ER format that the function is called in the context of.</span></span>

## <a name="example-1"></a><span data-ttu-id="81cb0-123">مثال1</span><span class="sxs-lookup"><span data-stu-id="81cb0-123">Example 1</span></span>

<span data-ttu-id="81cb0-124">يُرجع التعبير `DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` قيمة تاريخ/وقت خادم التطبيق الحالي، 24 ديسمبر 2015، كـ **"24-12-2015"**، بناءً على التنسيق المخصص المُحدد.</span><span class="sxs-lookup"><span data-stu-id="81cb0-124">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="81cb0-125">مثال2</span><span class="sxs-lookup"><span data-stu-id="81cb0-125">Example 2</span></span>

<span data-ttu-id="81cb0-126">تُرجع وظيفة `DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` قيمة تاريخ/وقت جلسة التطبيق الحالية، 24 ديسمبر 2015، كـ **"24.12.2015"**، بناءً على الثقافة الألمانية المُحددة والتنسيق المُحدد. </span><span class="sxs-lookup"><span data-stu-id="81cb0-126">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="example-3"></a><span data-ttu-id="81cb0-127">المثال الثالث</span><span class="sxs-lookup"><span data-stu-id="81cb0-127">Example 3</span></span>

<span data-ttu-id="81cb0-128">تُرجع  `DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` قيمة السلسلة **2019-11-12T08:00:00.0000000-08:00** عندما يتم استدعاءها أثناء عملية تم البدء فيها بواسطة مستخدم تطبيق لديه قيمة منطقة زمنية **‏‏‫(GMT-08:00) توقيت الباسيفيكي (الولايات المتحدة وكند)‬‬** في قسم **تفضيلات البلد/المنطقة واللغة‬**.</span><span class="sxs-lookup"><span data-stu-id="81cb0-128">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returns the string value **2019-11-12T08:00:00.0000000-08:00** when it's called during a process that was initiated by an application user who has the time zone value **(GMT-08:00) Pacific Time (US & Canada)** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="81cb0-129">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="81cb0-129">Additional resources</span></span>

[<span data-ttu-id="81cb0-130">دلات التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="81cb0-130">Date and time functions</span></span>](er-functions-category-datetime.md)
