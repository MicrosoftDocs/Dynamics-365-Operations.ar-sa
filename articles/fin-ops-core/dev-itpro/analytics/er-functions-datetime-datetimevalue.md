---
title: وظيفة DATETIMEVALUE ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية DATETIMEVALUE (ER).
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
ms.openlocfilehash: de601ad08b85797a4241ef74ecb3eba37eda37ca
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917524"
---
# <span data-ttu-id="ad741-103"><a name="DATETIMEVALUE">وظيفة DATETIMEVALUE ER</a></span><span class="sxs-lookup"><span data-stu-id="ad741-103"><a name="DATETIMEVALUE">DATETIMEVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ad741-104">تُرجع الوظيفة `DATETIMEVALUE` قيمة *DateTime* التي تم تحويلها من قيمة نصية مُعينة في التنسيق المُحدد وفي [الثقافة](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) المُحددة بشكل اختياري إلى قيمة التاريخ/الوقت.</span><span class="sxs-lookup"><span data-stu-id="ad741-104">The `DATETIMEVALUE` function returns a *DateTime* value that is converted from a given text value in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) to a date/time value.</span></span> <span data-ttu-id="ad741-105">(لمزيد من المعلومات حول التنسيقات المعتمدة، راجع [قياسي](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) و [مخصص](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="ad741-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="ad741-106">بناء الجملة 1</span><span class="sxs-lookup"><span data-stu-id="ad741-106">Syntax 1</span></span>

```
DATETIMEVALUE (text, format)
```

## <a name="syntax-2"></a><span data-ttu-id="ad741-107">بناء الجملة 2</span><span class="sxs-lookup"><span data-stu-id="ad741-107">Syntax 2</span></span>

```
DATETIMEVALUE (text, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="ad741-108">الوسائط</span><span class="sxs-lookup"><span data-stu-id="ad741-108">Arguments</span></span>

<span data-ttu-id="ad741-109">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="ad741-109">`text`: *String*</span></span>

<span data-ttu-id="ad741-110">النص الذي يمثل القيمة المراد تنسيقها.</span><span class="sxs-lookup"><span data-stu-id="ad741-110">Text that represents the value to format.</span></span>

<span data-ttu-id="ad741-111">`format`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="ad741-111">`format`: *String*</span></span>

<span data-ttu-id="ad741-112">تنسيق النص المُعين.</span><span class="sxs-lookup"><span data-stu-id="ad741-112">The format of the given text.</span></span>

<span data-ttu-id="ad741-113">`culture`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="ad741-113">`culture`: *String*</span></span>

<span data-ttu-id="ad741-114">الثقافة المستخدمة لتنسيق النص المُحدد.</span><span class="sxs-lookup"><span data-stu-id="ad741-114">The culture that is used for formatting of the given text.</span></span>

## <a name="return-values"></a><span data-ttu-id="ad741-115">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="ad741-115">Return values</span></span>

<span data-ttu-id="ad741-116">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="ad741-116">*DateTime*</span></span>

<span data-ttu-id="ad741-117">قيمة التاريخ/الوقت الناتجة.</span><span class="sxs-lookup"><span data-stu-id="ad741-117">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ad741-118">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="ad741-118">Usage notes</span></span>

<span data-ttu-id="ad741-119">عندما لا يتم تعريف الثقافة كوسيطة للوظيفة التي تم استدعائها، يتم تعريف قيمة `culture` عن طريق سياق الاستدعاء.</span><span class="sxs-lookup"><span data-stu-id="ad741-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="ad741-120">على سبيل المثال، إذا تم استدعاء الوظيفة `DATETIMEVALUE` باستخدام بناء الجملة 1 في تنسيق التقارير الإلكترونية (ER) لعنصر **FILE** تم تكوينه لاستخدام الثقافة الألمانية، فسوف يتم التحويل باستخدام الثقافة الألمانية.</span><span class="sxs-lookup"><span data-stu-id="ad741-120">For example, if the `DATETIMEVALUE` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="ad741-121">قيمة `culture` الافتراضية هي **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="ad741-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="ad741-122">مثال1</span><span class="sxs-lookup"><span data-stu-id="ad741-122">Example 1</span></span>

<span data-ttu-id="ad741-123">يُرجع التعبير `DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` **2:55:00 ص في 21 ديسمبر 2016** ، استنادًا إلى التنسيق المخصص وثقافة **EN-US** للتطبيق الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="ad741-123">`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` returns **2:55:00 AM on December 21, 2016**, based on the specified custom format and the default application's **EN-US** culture.</span></span>

## <a name="example-2"></a><span data-ttu-id="ad741-124">مثال2</span><span class="sxs-lookup"><span data-stu-id="ad741-124">Example 2</span></span>

<span data-ttu-id="ad741-125">يُرجع التعبير `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` **‬‏‫2:55:00 ص في 21 ديسمبر 2016** ، استنادًا إلى التنسيق المخصص والثقافة.</span><span class="sxs-lookup"><span data-stu-id="ad741-125">`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` returns **2:55:00 AM on December 21, 2016**, based on the specified custom format and culture.</span></span>

<span data-ttu-id="ad741-126">ومع ذلك، ستطرح `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` استثناءً لإعلام المستخدم بأنه لم يتم التعرف على السلسلة المحددة كقيمة تاريخ/وقت صالحة للثقافة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="ad741-126">However, `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` throws an exception to inform the user that the specified string isn't recognized as a valid date/time value for the specified culture.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ad741-127">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="ad741-127">Additional resources</span></span>

[<span data-ttu-id="ad741-128">دلات التاريخ والوقت</span><span class="sxs-lookup"><span data-stu-id="ad741-128">Date and time functions</span></span>](er-functions-category-datetime.md)