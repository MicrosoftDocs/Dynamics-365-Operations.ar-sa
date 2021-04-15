---
title: وظيفة DATETIMEFORMAT ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية DATETIMEFORMAT (ER).
author: NickSelin
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
ms.openlocfilehash: 859753c04e3b3d3b61d9a61edaf396637ed5a003
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746977"
---
# <a name="datetimeformat-er-function"></a><span data-ttu-id="4b725-103">وظيفة DATETIMEFORMAT ER</span><span class="sxs-lookup"><span data-stu-id="4b725-103">DATETIMEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4b725-104">تُرجع الوظيفة `DATETIMEFORMAT` قيمة *السلسلة* التي تمثل قيمة تاريخ مُعيّن كنص في التنسيق المُحدد وفي [الثقافة](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) المُحددة بشكل اختياري.</span><span class="sxs-lookup"><span data-stu-id="4b725-104">The `DATETIMEFORMAT` function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="4b725-105">لمزيد من المعلومات حول التنسيقات المعتمدة، راجع [قياسي](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) و [مخصص](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="4b725-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="4b725-106">بناء الجملة 1</span><span class="sxs-lookup"><span data-stu-id="4b725-106">Syntax 1</span></span>

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a><span data-ttu-id="4b725-107">بناء الجملة 2</span><span class="sxs-lookup"><span data-stu-id="4b725-107">Syntax 2</span></span>

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="4b725-108">الوسائط</span><span class="sxs-lookup"><span data-stu-id="4b725-108">Arguments</span></span>

<span data-ttu-id="4b725-109">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="4b725-109">`datetime`: *DateTime*</span></span>

<span data-ttu-id="4b725-110">قيمة التاريخ/الوقت التي تمثل التاريخ والوقت المراد تنسيقه.</span><span class="sxs-lookup"><span data-stu-id="4b725-110">A date/time value that represents the date and time to format.</span></span>

<span data-ttu-id="4b725-111">`format`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="4b725-111">`format`: *String*</span></span>

<span data-ttu-id="4b725-112">تنسيق سلسلة الإخراج.</span><span class="sxs-lookup"><span data-stu-id="4b725-112">The format of the output string.</span></span>

> [!NOTE]
> <span data-ttu-id="4b725-113">تكون سلسله التنسيق حساسة لحاله الأحرف عند استخدام اما تنسيق قياسي أو تنسيق مخصص.</span><span class="sxs-lookup"><span data-stu-id="4b725-113">The format string is case-sensitive when you use either a standard format or a custom format.</span></span> <span data-ttu-id="4b725-114">علي سبيل المثال، يقوم محدد التنسيق [القياسي](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) "d" بإرجاع التاريخ باستخدام نمط التاريخ القصير، بينما يقوم محدد التنسيق القياسي "d" بإرجاع التاريخ باستخدام نمط التاريخ الطويل.</span><span class="sxs-lookup"><span data-stu-id="4b725-114">For example, the [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) "d" format specifier returns the date by using the short date pattern, whereas the standard "D" format specifier returns the date by using the long date pattern.</span></span> <span data-ttu-id="4b725-115">بالاضافه إلى ذلك ، يقوم محدد التنسيق [المخصص](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) "m" بإرجاع الشهر من 1 إلى 12، بينما يقوم محدد التنسيق المخصص "m" بإرجاع الدقيقة من 0 إلى 59.</span><span class="sxs-lookup"><span data-stu-id="4b725-115">Additionally, the [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) "M" format specifier returns the month from 1 through 12, whereas the custom "m" format specifier returns the minute from 0 through 59.</span></span>

<span data-ttu-id="4b725-116">`culture`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="4b725-116">`culture`: *String*</span></span>

<span data-ttu-id="4b725-117">الثقافة التي سيتم استخدامها للتنسيق.</span><span class="sxs-lookup"><span data-stu-id="4b725-117">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="4b725-118">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="4b725-118">Return values</span></span>

<span data-ttu-id="4b725-119">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="4b725-119">*String*</span></span>

<span data-ttu-id="4b725-120">قيمة السلسلة الناتجة.</span><span class="sxs-lookup"><span data-stu-id="4b725-120">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="4b725-121">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="4b725-121">Usage notes</span></span>

<span data-ttu-id="4b725-122">إذا لم يتم تعريف الثقافة كوسيطة للوظيفة التي تم استدعائها، يتم تعريف قيمة `culture` عن طريق سياق الاستدعاء.</span><span class="sxs-lookup"><span data-stu-id="4b725-122">If the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="4b725-123">على سبيل المثال، إذا تم استدعاء الوظيفة `DATETIMEFORMAT` باستخدام بناء الجملة 1 في تنسيق التقارير الإلكترونية (ER) لعنصر **FILE** تم تكوينه لاستخدام الثقافة الألمانية، فسوف يتم التحويل باستخدام الثقافة الألمانية.</span><span class="sxs-lookup"><span data-stu-id="4b725-123">For example, if the `DATETIMEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="4b725-124">قيمة `culture` الافتراضية هي **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="4b725-124">The default `culture` value is **EN-US**.</span></span>

<span data-ttu-id="4b725-125">عندما تقوم الوظيفة `DATETIMEFORMAT` بتحويل قيمة تاريخ/وقت مُحدد، فإنها تعتبر إعداد المنطقة الزمنية لمستخدم التطبيق الذي يقوم بتشغيل تنسيق ER الذي تمت استدعاء الوظيفة في سياقه.</span><span class="sxs-lookup"><span data-stu-id="4b725-125">When the `DATETIMEFORMAT` function converts a given date/time value, it considers the time zone setting of the application user who is running the ER format that the function is called in the context of.</span></span>

## <a name="example-1"></a><span data-ttu-id="4b725-126">مثال1</span><span class="sxs-lookup"><span data-stu-id="4b725-126">Example 1</span></span>

<span data-ttu-id="4b725-127">يُرجع التعبير `DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` قيمة تاريخ/وقت خادم التطبيق الحالي، 24 ديسمبر 2015، كـ **"24-12-2015"**، بناءً على التنسيق المخصص المُحدد.</span><span class="sxs-lookup"><span data-stu-id="4b725-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="4b725-128">مثال2</span><span class="sxs-lookup"><span data-stu-id="4b725-128">Example 2</span></span>

<span data-ttu-id="4b725-129">تُرجع وظيفة `DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` قيمة تاريخ/وقت جلسة التطبيق الحالية، 24 ديسمبر 2015، كـ **"24.12.2015"**، بناءً على الثقافة الألمانية المُحددة والتنسيق المُحدد. </span><span class="sxs-lookup"><span data-stu-id="4b725-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="example-3"></a><span data-ttu-id="4b725-130">المثال الثالث</span><span class="sxs-lookup"><span data-stu-id="4b725-130">Example 3</span></span>

<span data-ttu-id="4b725-131">تُرجع  `DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` قيمة السلسلة **2019-11-12T08:00:00.0000000-08:00** عندما يتم استدعاء الدالة أثناء عملية تم البدء فيها بواسطة مستخدم تطبيق لديه قيمة منطقة زمنية **‏‏‫(GMT-08:00) توقيت الباسيفيكي (الولايات المتحدة وكند)‬‬** في قسم **تفضيلات البلد/المنطقة واللغة‬**.</span><span class="sxs-lookup"><span data-stu-id="4b725-131">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returns the string value **2019-11-12T08:00:00.0000000-08:00** when the function is called during a process that was initiated by an application user who has the time zone value **(GMT-08:00) Pacific Time (US & Canada)** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4b725-132">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="4b725-132">Additional resources</span></span>

[<span data-ttu-id="4b725-133">دلات التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="4b725-133">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]