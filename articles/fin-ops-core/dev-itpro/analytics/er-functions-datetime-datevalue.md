---
title: 'وظيفة DATEVALUE ER '
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية DATEVALUE (ER).
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: cfaf183c61d3663442cbc244239b872b9e1957bb
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891223"
---
# <a name="datevalue-er-function"></a><span data-ttu-id="3fdc1-103">وظيفة DATEVALUE ER</span><span class="sxs-lookup"><span data-stu-id="3fdc1-103">DATEVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3fdc1-104">تُرجع الوظيفة `DATEVALUE` قيمة *التاريخ* التي تم تحويلها من قيمة نصية معينة في التنسيق المُحدد وفي [الثقافة](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) المُحددة بشكل اختياري إلى قيمة التاريخ.</span><span class="sxs-lookup"><span data-stu-id="3fdc1-104">The `DATEVALUE` function returns a *Date* value that is converted from a given text value in the specified format and in an optionally specified [culture](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) to a date value.</span></span> <span data-ttu-id="3fdc1-105">لمزيد من المعلومات حول التنسيقات المعتمدة، راجع [قياسي](/dotnet/standard/base-types/standard-date-and-time-format-strings) و [مخصص](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span><span class="sxs-lookup"><span data-stu-id="3fdc1-105">For information about the supported formats, see [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) and [custom](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="3fdc1-106">بناء الجملة 1</span><span class="sxs-lookup"><span data-stu-id="3fdc1-106">Syntax 1</span></span>

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a><span data-ttu-id="3fdc1-107">بناء الجملة 2</span><span class="sxs-lookup"><span data-stu-id="3fdc1-107">Syntax 2</span></span>

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="3fdc1-108">الوسائط</span><span class="sxs-lookup"><span data-stu-id="3fdc1-108">Arguments</span></span>

<span data-ttu-id="3fdc1-109">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="3fdc1-109">`text`: *String*</span></span>

<span data-ttu-id="3fdc1-110">النص الذي يمثل القيمة المراد تنسيقها.</span><span class="sxs-lookup"><span data-stu-id="3fdc1-110">Text that represents the value to format.</span></span>

<span data-ttu-id="3fdc1-111">`format`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="3fdc1-111">`format`: *String*</span></span>

<span data-ttu-id="3fdc1-112">تنسيق النص المُعين.</span><span class="sxs-lookup"><span data-stu-id="3fdc1-112">The format of the given text.</span></span>

<span data-ttu-id="3fdc1-113">`culture`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="3fdc1-113">`culture`: *String*</span></span>

<span data-ttu-id="3fdc1-114">الثقافة المستخدمة لتنسيق النص المُحدد.</span><span class="sxs-lookup"><span data-stu-id="3fdc1-114">The culture that is used for formatting of the given text.</span></span>

## <a name="return-values"></a><span data-ttu-id="3fdc1-115">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="3fdc1-115">Return values</span></span>

<span data-ttu-id="3fdc1-116">*التاريخ*</span><span class="sxs-lookup"><span data-stu-id="3fdc1-116">*Date*</span></span>

<span data-ttu-id="3fdc1-117">قيمة التاريخ الناتجة.</span><span class="sxs-lookup"><span data-stu-id="3fdc1-117">The resulting date value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="3fdc1-118">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="3fdc1-118">Usage notes</span></span>

<span data-ttu-id="3fdc1-119">عندما لا يتم تعريف الثقافة كوسيطة للوظيفة التي تم استدعائها، يتم تعريف قيمة `culture` عن طريق سياق الاستدعاء.</span><span class="sxs-lookup"><span data-stu-id="3fdc1-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="3fdc1-120">على سبيل المثال، إذا تم استدعاء الوظيفة `DATEVALUE` باستخدام بناء الجملة 1 في تنسيق التقارير الإلكترونية (ER) لعنصر **FILE** تم تكوينه لاستخدام الثقافة الألمانية، فسوف يتم التحويل باستخدام الثقافة الألمانية.</span><span class="sxs-lookup"><span data-stu-id="3fdc1-120">For example, if the `DATEVALUE` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="3fdc1-121">قيمة `culture` الافتراضية هي **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="3fdc1-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="3fdc1-122">مثال1</span><span class="sxs-lookup"><span data-stu-id="3fdc1-122">Example 1</span></span>

<span data-ttu-id="3fdc1-123">يُرجع التعبير `DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` قيمة التاريخ **21 ديسمبر 2016**، استنادًا إلى التنسيق المخصص وثقافة **EN-US** للتطبيق الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="3fdc1-123">`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` returns the date value **December 21, 2016**, based on the specified custom format and the default application's **EN-US** culture.</span></span>

## <a name="example-2"></a><span data-ttu-id="3fdc1-124">مثال2</span><span class="sxs-lookup"><span data-stu-id="3fdc1-124">Example 2</span></span>

<span data-ttu-id="3fdc1-125">يُرجع التعبير `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` قيمة التاريخ **21 يناير 2016** ، استنادًا إلى التنسيق المخصص المُحدد والثقافة.</span><span class="sxs-lookup"><span data-stu-id="3fdc1-125">`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` returns the date value **January 21, 2016**, based on the specified custom format and culture.</span></span>

<span data-ttu-id="3fdc1-126">ولكن، سوف يطرح `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` استثناءً لإبلاغ المستخدم أنه لم يتم التعرف على السلسلة المُحددة كقيمة صالحة للثقافة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="3fdc1-126">However, `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` throws an exception to inform the user that the specified string isn't recognized as a valid date for the specified culture.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3fdc1-127">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="3fdc1-127">Additional resources</span></span>

[<span data-ttu-id="3fdc1-128">دلات التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="3fdc1-128">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]