---
title: SPLIT ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية SPLIT (ER).
author: NickSelin
ms.date: 04/01/2021
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
ms.openlocfilehash: 26b6ddeb2880fc220283b6389327a497549a4511
ms.sourcegitcommit: 74f5b04b482b2ae023c728e0df0eb78305493c6a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2021
ms.locfileid: "5853433"
---
# <a name="split-er-function"></a><span data-ttu-id="67988-103">SPLIT ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="67988-103">SPLIT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="67988-104">تقسم الوظيفة `SPLIT` سلسلة الإدخال المُحددة إلى سلاسل فرعية وتُرجع النتيجة كقيمة *قائمة سجلات* جديدة.</span><span class="sxs-lookup"><span data-stu-id="67988-104">The `SPLIT` function splits the specified input string into substrings and returns the result as a new *Record list* value.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="67988-105">بناء الجملة 1</span><span class="sxs-lookup"><span data-stu-id="67988-105">Syntax 1</span></span>

```vb
SPLIT (input, length)
```

<span data-ttu-id="67988-106">يستخدم بناء الجملة هذا لتقسيم سلسلة الإدخال المحددة إلى سلاسل فرعية، لكل منها الطول المحدد.</span><span class="sxs-lookup"><span data-stu-id="67988-106">This syntax is used to split the specified input string into substrings, each of which has the specified length.</span></span>

## <a name="syntax-2"></a><span data-ttu-id="67988-107">بناء الجملة 2</span><span class="sxs-lookup"><span data-stu-id="67988-107">Syntax 2</span></span>

```vb
SPLIT (input, delimiter)
```

<span data-ttu-id="67988-108">يستخدم بناء الجملة هذا لتقسيم سلسلة الإدخال المحددة إلى سلاسل فرعية، استنادًا إلى المحدد المعين.</span><span class="sxs-lookup"><span data-stu-id="67988-108">This syntax is used to split the specified input string into substrings, based on the specified delimiter.</span></span>

## <a name="arguments"></a><span data-ttu-id="67988-109">الوسائط</span><span class="sxs-lookup"><span data-stu-id="67988-109">Arguments</span></span>

<span data-ttu-id="67988-110">`input`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="67988-110">`input`: *String*</span></span>

<span data-ttu-id="67988-111">النص المراد تقسيمه.</span><span class="sxs-lookup"><span data-stu-id="67988-111">The text to split.</span></span>

<span data-ttu-id="67988-112">`length`: *عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="67988-112">`length`: *Integer*</span></span>

<span data-ttu-id="67988-113">الحد الأقصى لطول سلسلة فرعية واحدة.</span><span class="sxs-lookup"><span data-stu-id="67988-113">The maximum length of a single substring.</span></span>

<span data-ttu-id="67988-114">`delimiter`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="67988-114">`delimiter`: *String*</span></span>

<span data-ttu-id="67988-115">مُحدد يستخدم لفصل السلاسل الفرعية.</span><span class="sxs-lookup"><span data-stu-id="67988-115">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="67988-116">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="67988-116">Return values</span></span>

<span data-ttu-id="67988-117">*قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="67988-117">*Record list*</span></span>

<span data-ttu-id="67988-118">قائمة السجلات الناتجة.</span><span class="sxs-lookup"><span data-stu-id="67988-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="67988-119">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="67988-119">Usage notes</span></span>

<span data-ttu-id="67988-120">تتكون بنية سجل القائمة التي تم إرجاعها من حقل **القيمة** من نوع *السلسلة*.</span><span class="sxs-lookup"><span data-stu-id="67988-120">The record structure of the list that is returned consists of the **Value** field of the *String* type.</span></span> <span data-ttu-id="67988-121">يحتوي كل سجل من القائمة التي تم إرجاعها على سلاسل فرعية تم إنشاؤها في هذا الحقل.</span><span class="sxs-lookup"><span data-stu-id="67988-121">Every record of the list that is returned contains generated substrings in this field.</span></span>

<span data-ttu-id="67988-122">إذا كانت وسيطة `delimiter` فارغة، تتكون القائمة الجديدة التي تم إرجاعها من سجل واحد يحتوي على الحقل **القيمة** من نوع *السلسلة*.</span><span class="sxs-lookup"><span data-stu-id="67988-122">If the `delimiter` argument is empty, the new list that is returned consists of one record that has the **Value** field of the *String* type.</span></span> <span data-ttu-id="67988-123">يحتوي هذا الحقل علي نص الإدخال.</span><span class="sxs-lookup"><span data-stu-id="67988-123">This field contains the input text.</span></span>

<span data-ttu-id="67988-124">إذا كانت الوسيطة `input` فارغة، يتم إرجاع قائمة فارغة جديدة.</span><span class="sxs-lookup"><span data-stu-id="67988-124">If the `input` argument is empty, a new empty list is returned.</span></span> <span data-ttu-id="67988-125">إذا لم يتم تعيين الوسيطة `input` أو `delimiter` (null)، يتم طرح استثناء تطبيق.</span><span class="sxs-lookup"><span data-stu-id="67988-125">If either the `input` or `delimiter` argument is unspecified (null), an application exception is thrown.</span></span>

## <a name="example-1"></a><span data-ttu-id="67988-126">مثال1</span><span class="sxs-lookup"><span data-stu-id="67988-126">Example 1</span></span>

<span data-ttu-id="67988-127">يُرجع التعبير `SPLIT ("abcd", 3)` قائمة جديدة تتكون من سجلين لديهما حقل **القيمة** من نوع *السلسلة*.</span><span class="sxs-lookup"><span data-stu-id="67988-127">`SPLIT ("abcd", 3)` returns a new list that consists of two records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="67988-128">يحتوي حقل **القيمة** في السجل الأول على النص **"abc"** ، ويحتوي حقل **القيمة** في السجل الثاني على النص **"d"**.</span><span class="sxs-lookup"><span data-stu-id="67988-128">The **Value** field in the first record contains the text **"abc"**, and the **Value** field in the second record contains the text **"d"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="67988-129">مثال2</span><span class="sxs-lookup"><span data-stu-id="67988-129">Example 2</span></span>

<span data-ttu-id="67988-130">يُرجع التعبير `SPLIT ("XAb aBy", "aB")` قائمة جديدة تتكون من ثلاث سجلات لديهم حقل **القيمة** من نوع *السلسلة*.</span><span class="sxs-lookup"><span data-stu-id="67988-130">`SPLIT ("XAb aBy", "aB")` returns a new list that consists of three records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="67988-131">يحتوي حقل **القيمة** في السجل الأول على النص **"X"** ، ويحتوي حقل **القيمة** في السجل الثاني على النص **&nbsp;** ، ويحتوي حقل **القيمة** في السجل الثالث على النص **"y"**.</span><span class="sxs-lookup"><span data-stu-id="67988-131">The **Value** field in the first record contains the text **"X"**, the **Value** field in the second record contains the text **"&nbsp;"**, and the **Value** field in the third record contains the text **"y"**.</span></span> 

## <a name="example-3"></a><span data-ttu-id="67988-132">المثال الثالث</span><span class="sxs-lookup"><span data-stu-id="67988-132">Example 3</span></span>

<span data-ttu-id="67988-133">يمكنك استخدام الدالة [INDEX](er-functions-list-index.md) للوصول إلى العناصر الفردية لإعداد الإدخال المحدد.</span><span class="sxs-lookup"><span data-stu-id="67988-133">Yo can use the [INDEX](er-functions-list-index.md) function to access individual elements of the specified input string.</span></span> <span data-ttu-id="67988-134">إذا قمت بإدخال مصدر البيانات **MyList** من النوع **الحقل المحسوب** وقمت بتكوينه للتعبير `SPLIT("abc", 1)`، يرجع التعبير `INDEX(MyList,2).Value` النص **"b"**.</span><span class="sxs-lookup"><span data-stu-id="67988-134">If you enter the **MyList** data source of the **Calculated field** type and configure for it the `SPLIT("abc", 1)` expression, the expression `INDEX(MyList,2).Value` returns the text **"b"**.</span></span>

## <a name="example-4"></a><span data-ttu-id="67988-135">المثال الرابع</span><span class="sxs-lookup"><span data-stu-id="67988-135">Example 4</span></span>

<span data-ttu-id="67988-136">يمكنك استخدام الدالة [ENUMERATE](er-functions-list-enumerate.md) لمساعدتك في الوصول إلى العناصر الفردية لإعداد الإدخال المحدد.</span><span class="sxs-lookup"><span data-stu-id="67988-136">The [ENUMERATE](er-functions-list-enumerate.md) function can also help you access individual elements of the specified input string.</span></span> <span data-ttu-id="67988-137">إذا قمت أولاً بإدخال مصدر البيانات **MyList** للنوع **الحقل المحسوب** وقمت بتكوينه للتعبير `SPLIT("abc", 1)`، ثم أدخلت مصدر البيانات **EnumeratedList** للنوع **الحقل المحسوب** وقمت بتكوينه للتعبير `ENUMERATE(MyList)`، يرجع التعبير `FIRSTORNULL(WHERE(EnumeratedList, EnumeratedList.Number=2)).Value` النص **"b"**.</span><span class="sxs-lookup"><span data-stu-id="67988-137">If you first enter the **MyList** data source of the **Calculated field** type and configure for it the `SPLIT("abc", 1)` expression, and then enter the **EnumeratedList** data source of the **Calculated field** type and configure for it the `ENUMERATE(MyList)` expression, the expression `FIRSTORNULL(WHERE(EnumeratedList, EnumeratedList.Number=2)).Value` returns the text **"b"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="67988-138">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="67988-138">Additional resources</span></span>

[<span data-ttu-id="67988-139">دالات القائمة</span><span class="sxs-lookup"><span data-stu-id="67988-139">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
