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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3c9d3b6748ecb1680586a2d47a425b5ef98551f1
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682905"
---
# <a name="replace-er-function"></a><span data-ttu-id="96326-103">REPLACE ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="96326-103">REPLACE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="96326-104">تقوم وظيفة `REPLACE` بإرجاع السلسلة النصية المُحددة كقيمة *سلسلة* بعد استبدالها كليًا أو جزئيًا بسلسلة أخرى.</span><span class="sxs-lookup"><span data-stu-id="96326-104">The `REPLACE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="96326-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="96326-105">Syntax</span></span>

```vb
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a><span data-ttu-id="96326-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="96326-106">Arguments</span></span>

<span data-ttu-id="96326-107">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="96326-107">`text`: *String*</span></span>

<span data-ttu-id="96326-108">المسار الصالح لمصدر البيانات من نوع *السلسلة*.</span><span class="sxs-lookup"><span data-stu-id="96326-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="96326-109">`pattern`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="96326-109">`pattern`: *String*</span></span>

<span data-ttu-id="96326-110">إذا كانت الوسيطة `regular expression flag` **FALSE**، تحتوي هذه الوسيطة على النص الذي يجب استبداله.</span><span class="sxs-lookup"><span data-stu-id="96326-110">If the `regular expression flag` argument is **FALSE**, this argument contains the text that must be replaced.</span></span>

<span data-ttu-id="96326-111">إذا كانت الوسيطة `regular expression flag` **TRUE**، تحتوي هذه الوسيطة على تعبير عادي يُعرف كل من نمط البحث ونص الاستبدال.</span><span class="sxs-lookup"><span data-stu-id="96326-111">If the `regular expression flag` argument is **TRUE**, this argument contains a regular expression that defines both a search pattern and the replacement text.</span></span>

<span data-ttu-id="96326-112">`replacement`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="96326-112">`replacement`: *String*</span></span>

<span data-ttu-id="96326-113">إذا كانت الوسيطة `regular expression flag` **FALSE**، تحتوي هذه الوسيطة على النص لاستخدامه كبديل.</span><span class="sxs-lookup"><span data-stu-id="96326-113">If the `regular expression flag` argument is **FALSE**, this argument contains the text to use as a replacement.</span></span>

<span data-ttu-id="96326-114">إذا كانت الوسيطة `regular expression flag` **TRUE**، لا يتم استخدام هذه الوسيطة.</span><span class="sxs-lookup"><span data-stu-id="96326-114">If the `regular expression flag` argument is **TRUE**, this argument isn't used.</span></span>

<span data-ttu-id="96326-115">`regular expression flag`: *منطقي*</span><span class="sxs-lookup"><span data-stu-id="96326-115">`regular expression flag`: *Boolean*</span></span>

<span data-ttu-id="96326-116">قيمة *منطقية* تشير إلى إذا ما كان يتم استخدام تعبير عادي للقيام بالاستبدال.</span><span class="sxs-lookup"><span data-stu-id="96326-116">A *Boolean* value that indicates whether a regular expression is used to do the replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="96326-117">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="96326-117">Return values</span></span>

<span data-ttu-id="96326-118">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="96326-118">*String*</span></span>

<span data-ttu-id="96326-119">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="96326-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="96326-120">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="96326-120">Usage notes</span></span>

<span data-ttu-id="96326-121">إذا كانت الوسيطة `regular expression flag` **TRUE**، تقوم هذه الوظيفة بإرجاع السلسلة المُحددة بعد أن تم تغييرها عن طريق تطبيق التعبير العادي المُحدد بواسطة الوسيطة `pattern`.</span><span class="sxs-lookup"><span data-stu-id="96326-121">If the `regular expression flag` argument is **TRUE**, this function returns the specified string after it has been changed by applying the regular expression that is specified by the `pattern` argument.</span></span> <span data-ttu-id="96326-122">يتم استخدام التعبير العادي للبحث عن الأحرف التي يجب استبدالها.</span><span class="sxs-lookup"><span data-stu-id="96326-122">The regular expression is used to find the characters that must be replaced.</span></span>

<span data-ttu-id="96326-123">إذا كانت الوسيطة `regular expression flag` بقيمة **FALSE**، ترجع هذه الدالة السلسلة المحددة بعد أن يتم استبدال مجموعة الأحرف التي تم تعريفها في الوسيطة `pattern` بأحرف من الوسيطة `replacement`.</span><span class="sxs-lookup"><span data-stu-id="96326-123">If the `regular expression flag` argument is **FALSE**, this function returns the specified string after the set of characters that are defined in the `pattern` argument have been replaced by characters of the `replacement` argument.</span></span> 

## <a name="example-1"></a><span data-ttu-id="96326-124">مثال1</span><span class="sxs-lookup"><span data-stu-id="96326-124">Example 1</span></span>

<span data-ttu-id="96326-125">تُطبق `REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` تعبيرًا عاديًا يقوم بإزالة كافة الرموز غير الرقيمة، ويُرجع **"19234564971"**. </span><span class="sxs-lookup"><span data-stu-id="96326-125">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` applies a regular expression that removes all non-numeric symbols, and it returns **"19234564971"**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="96326-126">مثال2</span><span class="sxs-lookup"><span data-stu-id="96326-126">Example 2</span></span>

<span data-ttu-id="96326-127">يستبدل `REPLACE ("abcdef", "cd", "GH", false)` النمط **"cd"** بالسلسلة **"GH"** وترجع **"abGHef"**.</span><span class="sxs-lookup"><span data-stu-id="96326-127">`REPLACE ("abcdef", "cd", "GH", false)` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="96326-128">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="96326-128">Additional resources</span></span>

[<span data-ttu-id="96326-129">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="96326-129">Text functions</span></span>](er-functions-category-text.md)
