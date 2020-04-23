---
title: REPLACE ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني REPLACE (ER).
author: NickSelin
manager: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: 83d5095620a938f1ac4b8428fff9209fda7a7831
ms.sourcegitcommit: fb8ad8e2b142441a6530b364f3258bbcc0c724d2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201056"
---
# <a name=""></a><span data-ttu-id="69b53-103"><a name="REPLACE">REPLACE ER وظيفة</a></span><span class="sxs-lookup"><span data-stu-id="69b53-103"><a name="REPLACE">REPLACE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="69b53-104">تقوم وظيفة `REPLACE` بإرجاع السلسلة النصية المُحددة كقيمة *سلسلة* بعد استبدالها كليًا أو جزئيًا بسلسلة أخرى.</span><span class="sxs-lookup"><span data-stu-id="69b53-104">The `REPLACE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="69b53-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="69b53-105">Syntax</span></span>

```vb
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a><span data-ttu-id="69b53-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="69b53-106">Arguments</span></span>

<span data-ttu-id="69b53-107">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="69b53-107">`text`: *String*</span></span>

<span data-ttu-id="69b53-108">المسار الصالح لمصدر البيانات من نوع *السلسلة*.</span><span class="sxs-lookup"><span data-stu-id="69b53-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="69b53-109">`pattern`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="69b53-109">`pattern`: *String*</span></span>

<span data-ttu-id="69b53-110">إذا كانت الوسيطة `regular expression flag` **FALSE**، تحتوي هذه الوسيطة على النص الذي يجب استبداله.</span><span class="sxs-lookup"><span data-stu-id="69b53-110">If the `regular expression flag` argument is **FALSE**, this argument contains the text that must be replaced.</span></span>

<span data-ttu-id="69b53-111">إذا كانت الوسيطة `regular expression flag` **TRUE**، تحتوي هذه الوسيطة على تعبير عادي يُعرف كل من نمط البحث ونص الاستبدال.</span><span class="sxs-lookup"><span data-stu-id="69b53-111">If the `regular expression flag` argument is **TRUE**, this argument contains a regular expression that defines both a search pattern and the replacement text.</span></span>

<span data-ttu-id="69b53-112">`replacement`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="69b53-112">`replacement`: *String*</span></span>

<span data-ttu-id="69b53-113">إذا كانت الوسيطة `regular expression flag` **FALSE**، تحتوي هذه الوسيطة على النص لاستخدامه كبديل.</span><span class="sxs-lookup"><span data-stu-id="69b53-113">If the `regular expression flag` argument is **FALSE**, this argument contains the text to use as a replacement.</span></span>

<span data-ttu-id="69b53-114">إذا كانت الوسيطة `regular expression flag` **TRUE**، لا يتم استخدام هذه الوسيطة.</span><span class="sxs-lookup"><span data-stu-id="69b53-114">If the `regular expression flag` argument is **TRUE**, this argument isn't used.</span></span>

<span data-ttu-id="69b53-115">`regular expression flag`: *منطقي*</span><span class="sxs-lookup"><span data-stu-id="69b53-115">`regular expression flag`: *Boolean*</span></span>

<span data-ttu-id="69b53-116">قيمة *منطقية* تشير إلى إذا ما كان يتم استخدام تعبير عادي للقيام بالاستبدال.</span><span class="sxs-lookup"><span data-stu-id="69b53-116">A *Boolean* value that indicates whether a regular expression is used to do the replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="69b53-117">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="69b53-117">Return values</span></span>

<span data-ttu-id="69b53-118">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="69b53-118">*String*</span></span>

<span data-ttu-id="69b53-119">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="69b53-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="69b53-120">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="69b53-120">Usage notes</span></span>

<span data-ttu-id="69b53-121">إذا كانت الوسيطة `regular expression flag` **TRUE**، تقوم هذه الوظيفة بإرجاع السلسلة المُحددة بعد أن تم تغييرها عن طريق تطبيق التعبير العادي المُحدد بواسطة الوسيطة `pattern`.</span><span class="sxs-lookup"><span data-stu-id="69b53-121">If the `regular expression flag` argument is **TRUE**, this function returns the specified string after it has been changed by applying the regular expression that is specified by the `pattern` argument.</span></span> <span data-ttu-id="69b53-122">يتم استخدام التعبير العادي للبحث عن الأحرف التي يجب استبدالها.</span><span class="sxs-lookup"><span data-stu-id="69b53-122">The regular expression is used to find the characters that must be replaced.</span></span>

<span data-ttu-id="69b53-123">إذا كانت الوسيطة `regular expression flag` بقيمة **FALSE**، ترجع هذه الدالة السلسلة المحددة بعد أن يتم استبدال مجموعة الأحرف التي تم تعريفها في الوسيطة `pattern` بأحرف من الوسيطة `replacement`.</span><span class="sxs-lookup"><span data-stu-id="69b53-123">If the `regular expression flag` argument is **FALSE**, this function returns the specified string after the set of characters that are defined in the `pattern` argument have been replaced by characters of the `replacement` argument.</span></span> 

## <a name="example-1"></a><span data-ttu-id="69b53-124">مثال1</span><span class="sxs-lookup"><span data-stu-id="69b53-124">Example 1</span></span>

<span data-ttu-id="69b53-125">تُطبق `REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` تعبيرًا عاديًا يقوم بإزالة كافة الرموز غير الرقيمة، ويُرجع **"19234564971"**. </span><span class="sxs-lookup"><span data-stu-id="69b53-125">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` applies a regular expression that removes all non-numeric symbols, and it returns **"19234564971"**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="69b53-126">مثال2</span><span class="sxs-lookup"><span data-stu-id="69b53-126">Example 2</span></span>

<span data-ttu-id="69b53-127">يستبدل `REPLACE ("abcdef", "cd", "GH", false)` النمط **"cd"** بالسلسلة **"GH"** وترجع **"abGHef"**.</span><span class="sxs-lookup"><span data-stu-id="69b53-127">`REPLACE ("abcdef", "cd", "GH", false)` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="69b53-128">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="69b53-128">Additional resources</span></span>

[<span data-ttu-id="69b53-129">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="69b53-129">Text functions</span></span>](er-functions-category-text.md)
