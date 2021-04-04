---
title: وظيفة TRANSLATE ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني TRANSLATE (ER).
author: NickSelin
manager: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: f17d3439870710766906013e74452c2e76fec4ce
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560003"
---
# <a name="translate-er-function"></a><span data-ttu-id="899a1-103">وظيفة TRANSLATE ER</span><span class="sxs-lookup"><span data-stu-id="899a1-103">TRANSLATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="899a1-104">تقوم الدالة `TRANSLATE` بإرجاع قيمة *سلسلة* تحتوي على نتيجة استبدال النص المحدد بأحرف بمجموعة أحرف أخرى متوفرة.</span><span class="sxs-lookup"><span data-stu-id="899a1-104">The `TRANSLATE` function returns a *String* value that contains the result of the character replacement of specified text in characters of another provided set.</span></span>

## <a name="syntax"></a><span data-ttu-id="899a1-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="899a1-105">Syntax</span></span>

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="899a1-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="899a1-106">Arguments</span></span>

<span data-ttu-id="899a1-107">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="899a1-107">`text`: *String*</span></span>

<span data-ttu-id="899a1-108">المسار الصالح لمصدر البيانات من نوع *السلسلة*.</span><span class="sxs-lookup"><span data-stu-id="899a1-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="899a1-109">`pattern`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="899a1-109">`pattern`: *String*</span></span>

<span data-ttu-id="899a1-110">النص الذي يجب استبداله.</span><span class="sxs-lookup"><span data-stu-id="899a1-110">The text that must be replaced.</span></span>

<span data-ttu-id="899a1-111">`replacement`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="899a1-111">`replacement`: *String*</span></span>

<span data-ttu-id="899a1-112">النص الذي سيتم استخدامه كبديل.</span><span class="sxs-lookup"><span data-stu-id="899a1-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="899a1-113">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="899a1-113">Return values</span></span>

<span data-ttu-id="899a1-114">*سلسلة*</span><span class="sxs-lookup"><span data-stu-id="899a1-114">*String*</span></span>

<span data-ttu-id="899a1-115">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="899a1-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="899a1-116">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="899a1-116">Usage notes</span></span>

<span data-ttu-id="899a1-117">تقوم الدالة `TRANSLATE` باستبدال كل حرف على حدة.</span><span class="sxs-lookup"><span data-stu-id="899a1-117">The `TRANSLATE` function replaces one character at a time.</span></span> <span data-ttu-id="899a1-118">تقوم الدالة باستبدال الحرف الأول للوسيطة `text` بالحرف الأول من الوسيطة `pattern` ثم الحرف الثاني وتتبع سير العمل نفسه حتى الانتهاء.</span><span class="sxs-lookup"><span data-stu-id="899a1-118">The function replaces the first character of the `text` argument with the first character of the `pattern` argument and then the second character and follows the same flow until finished.</span></span> <span data-ttu-id="899a1-119">عندما يتطابق حرف من الوسيطتين `text` و`pattern`، يتم استبداله بحرف من الوسيطة `replacement` الموجودة في الموضع نفسه للحرف من الوسيطة `pattern`.</span><span class="sxs-lookup"><span data-stu-id="899a1-119">When a character from the `text` and `pattern` arguments match, it is replaced by a character from the `replacement` argument that is located in the same position as the character from the `pattern` argument.</span></span> <span data-ttu-id="899a1-120">إذا ظهر أحد الأحرف عدة مرات في الوسيطة `pattern`، فسيتم استخدام تعيين الوسيطة `replacement` الذي يتطابق مع الحدوث الأول لهذا الحرف.</span><span class="sxs-lookup"><span data-stu-id="899a1-120">If a character appears multiple times in the `pattern` argument, the `replacement` argument mapping that corresponds to the first occurrence of this character is used.</span></span>

## <a name="example-1"></a><span data-ttu-id="899a1-121">مثال1</span><span class="sxs-lookup"><span data-stu-id="899a1-121">Example 1</span></span>

<span data-ttu-id="899a1-122">تقوم الدالة `TRANSLATE ("abcdef", "cd", "GH")` باستبدال الحرف **"c"** للنص **“abcdef”** المحدد بالحرف **"G"** للنص `replacement` للأسباب التالية:</span><span class="sxs-lookup"><span data-stu-id="899a1-122">`TRANSLATE ("abcdef", "cd", "GH")` replaces the **"c"** character of the specified  **“abcdef”** text with the **"G"** character of the `replacement` text due to the following:</span></span>
-   <span data-ttu-id="899a1-123">تم تقديم الحرف **"c"** في النص `pattern` في الموضع الأول.</span><span class="sxs-lookup"><span data-stu-id="899a1-123">The **"c"** character is presented in the `pattern` text in the first position.</span></span>
-   <span data-ttu-id="899a1-124">يحتوي الموضع الأول للنص `replacement` على الحرف **"G"**.</span><span class="sxs-lookup"><span data-stu-id="899a1-124">The first position of the `replacement` text contains the **"G"** character.</span></span>

## <a name="example-2"></a><span data-ttu-id="899a1-125">مثال2</span><span class="sxs-lookup"><span data-stu-id="899a1-125">Example 2</span></span>

<span data-ttu-id="899a1-126">تقوم الدالة `TRANSLATE ("abcdef", "ccd", "GH")` بإرجاع **"abGdef"**.</span><span class="sxs-lookup"><span data-stu-id="899a1-126">`TRANSLATE ("abcdef", "ccd", "GH")` returns **"abGdef"**.</span></span>

## <a name="example-3"></a><span data-ttu-id="899a1-127">المثال الثالث</span><span class="sxs-lookup"><span data-stu-id="899a1-127">Example 3</span></span>

<span data-ttu-id="899a1-128">يُرجع التعبير `TRANSLATE ("abccba", "abc", "123")` **"123321"**.</span><span class="sxs-lookup"><span data-stu-id="899a1-128">`TRANSLATE ("abccba", "abc", "123")` returns **"123321"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="899a1-129">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="899a1-129">Additional resources</span></span>

[<span data-ttu-id="899a1-130">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="899a1-130">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]