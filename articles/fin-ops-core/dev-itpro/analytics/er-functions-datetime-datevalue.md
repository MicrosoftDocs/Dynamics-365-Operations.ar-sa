---
title: 'وظيفة DATEVALUE ER '
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية DATEVALUE (ER).
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 43e65055b0803ed330a19568f9565c3fae488ab2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682403"
---
# <a name="datevalue-er-function"></a><span data-ttu-id="92675-103">وظيفة DATEVALUE ER</span><span class="sxs-lookup"><span data-stu-id="92675-103">DATEVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="92675-104">تُرجع الوظيفة `DATEVALUE` قيمة *التاريخ* التي تم تحويلها من قيمة نصية معينة في التنسيق المُحدد وفي [الثقافة](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) المُحددة بشكل اختياري إلى قيمة التاريخ.</span><span class="sxs-lookup"><span data-stu-id="92675-104">The `DATEVALUE` function returns a *Date* value that is converted from a given text value in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) to a date value.</span></span> <span data-ttu-id="92675-105">لمزيد من المعلومات حول التنسيقات المعتمدة، راجع [قياسي](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) و [مخصص](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="92675-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="92675-106">بناء الجملة 1</span><span class="sxs-lookup"><span data-stu-id="92675-106">Syntax 1</span></span>

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a><span data-ttu-id="92675-107">بناء الجملة 2</span><span class="sxs-lookup"><span data-stu-id="92675-107">Syntax 2</span></span>

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="92675-108">الوسائط</span><span class="sxs-lookup"><span data-stu-id="92675-108">Arguments</span></span>

<span data-ttu-id="92675-109">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="92675-109">`text`: *String*</span></span>

<span data-ttu-id="92675-110">النص الذي يمثل القيمة المراد تنسيقها.</span><span class="sxs-lookup"><span data-stu-id="92675-110">Text that represents the value to format.</span></span>

<span data-ttu-id="92675-111">`format`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="92675-111">`format`: *String*</span></span>

<span data-ttu-id="92675-112">تنسيق النص المُعين.</span><span class="sxs-lookup"><span data-stu-id="92675-112">The format of the given text.</span></span>

<span data-ttu-id="92675-113">`culture`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="92675-113">`culture`: *String*</span></span>

<span data-ttu-id="92675-114">الثقافة المستخدمة لتنسيق النص المُحدد.</span><span class="sxs-lookup"><span data-stu-id="92675-114">The culture that is used for formatting of the given text.</span></span>

## <a name="return-values"></a><span data-ttu-id="92675-115">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="92675-115">Return values</span></span>

<span data-ttu-id="92675-116">*التاريخ*</span><span class="sxs-lookup"><span data-stu-id="92675-116">*Date*</span></span>

<span data-ttu-id="92675-117">قيمة التاريخ الناتجة.</span><span class="sxs-lookup"><span data-stu-id="92675-117">The resulting date value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="92675-118">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="92675-118">Usage notes</span></span>

<span data-ttu-id="92675-119">عندما لا يتم تعريف الثقافة كوسيطة للوظيفة التي تم استدعائها، يتم تعريف قيمة `culture` عن طريق سياق الاستدعاء.</span><span class="sxs-lookup"><span data-stu-id="92675-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="92675-120">على سبيل المثال، إذا تم استدعاء الوظيفة `DATEVALUE` باستخدام بناء الجملة 1 في تنسيق التقارير الإلكترونية (ER) لعنصر **FILE** تم تكوينه لاستخدام الثقافة الألمانية، فسوف يتم التحويل باستخدام الثقافة الألمانية.</span><span class="sxs-lookup"><span data-stu-id="92675-120">For example, if the `DATEVALUE` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="92675-121">قيمة `culture` الافتراضية هي **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="92675-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="92675-122">مثال1</span><span class="sxs-lookup"><span data-stu-id="92675-122">Example 1</span></span>

<span data-ttu-id="92675-123">يُرجع التعبير `DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` قيمة التاريخ **21 ديسمبر 2016**، استنادًا إلى التنسيق المخصص وثقافة **EN-US** للتطبيق الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="92675-123">`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` returns the date value **December 21, 2016**, based on the specified custom format and the default application's **EN-US** culture.</span></span>

## <a name="example-2"></a><span data-ttu-id="92675-124">مثال2</span><span class="sxs-lookup"><span data-stu-id="92675-124">Example 2</span></span>

<span data-ttu-id="92675-125">يُرجع التعبير `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` قيمة التاريخ **21 يناير 2016** ، استنادًا إلى التنسيق المخصص المُحدد والثقافة.</span><span class="sxs-lookup"><span data-stu-id="92675-125">`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` returns the date value **January 21, 2016**, based on the specified custom format and culture.</span></span>

<span data-ttu-id="92675-126">ولكن، سوف يطرح `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` استثناءً لإبلاغ المستخدم أنه لم يتم التعرف على السلسلة المُحددة كقيمة صالحة للثقافة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="92675-126">However, `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` throws an exception to inform the user that the specified string isn't recognized as a valid date for the specified culture.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="92675-127">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="92675-127">Additional resources</span></span>

[<span data-ttu-id="92675-128">دلات التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="92675-128">Date and time functions</span></span>](er-functions-category-datetime.md)
