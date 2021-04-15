---
title: CASE ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية CASE (ER).
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 44815160957922f508fccd72174be2c4145a8d89
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745439"
---
# <a name="case-er-function"></a><span data-ttu-id="19558-103">CASE ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="19558-103">CASE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="19558-104">تٌقيّم الوظيفة `CASE` قيمة التعبير المُحدد في مقابل الخيارات البديلة المُحددة، وترجع نتيجة الخيار الأول الذي يساوي قيمة التعبير المُحدد.</span><span class="sxs-lookup"><span data-stu-id="19558-104">The `CASE` function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="19558-105">وإلا، فإنه يقوم بإرجاع النتيجة الافتراضية الاختيارية، إذا كانت النتيجة الافتراضية مُحدد كآخر وسيطة للوظيفة التي تم استدعائها والتي لم يسبقها خيار.</span><span class="sxs-lookup"><span data-stu-id="19558-105">Otherwise, it returns the optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="19558-106">يُمكن أن تكون القيمة التي يتم إرجاعها قيمة من أي أنواع بيانات مدعومة.</span><span class="sxs-lookup"><span data-stu-id="19558-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="19558-107">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="19558-107">Syntax</span></span>

```vb
CASE (expression, option 1, result 1[, option 2, result 2, …, option N, result N, default result])
```

## <a name="arguments"></a><span data-ttu-id="19558-108">الوسائط</span><span class="sxs-lookup"><span data-stu-id="19558-108">Arguments</span></span>

<span data-ttu-id="19558-109">`expression`: *نوع البيانات الأساسية* (منطقية أو رقمية أو نصية)</span><span class="sxs-lookup"><span data-stu-id="19558-109">`expression`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="19558-110">تعبير صالح يقوم بإرجاع قيمة نوع البيانات الأساسية.</span><span class="sxs-lookup"><span data-stu-id="19558-110">A valid expression that returns a value of the primitive data type.</span></span>

<span data-ttu-id="19558-111">`option 1`: *نوع البيانات الأساسية* (منطقية أو رقمية أو نصية)</span><span class="sxs-lookup"><span data-stu-id="19558-111">`option 1`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="19558-112">تعبير صالح يقوم بإرجاع قيمة نفس أنواع البيانات الأساسية مثل وسيطة `expression` للوظيفة التي تم استدعاؤها.</span><span class="sxs-lookup"><span data-stu-id="19558-112">A valid expression that returns a value of the same primitive data type as the `expression` argument of the called function.</span></span> <span data-ttu-id="19558-113">هذه الوسيطة مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="19558-113">This argument is required.</span></span>

<span data-ttu-id="19558-114">`result 1`: *أي من أنواع البيانات المعتمدة*</span><span class="sxs-lookup"><span data-stu-id="19558-114">`result 1`: *Any of the supported data types*</span></span>

<span data-ttu-id="19558-115">النتيجة التي تم إرجاعها التي تتوافق مع الخيار السابق.</span><span class="sxs-lookup"><span data-stu-id="19558-115">The returned result that corresponds to the preceding option.</span></span> <span data-ttu-id="19558-116">هذه الوسيطة مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="19558-116">This argument is required.</span></span>

<span data-ttu-id="19558-117">`option N`: *نوع البيانات الأساسية* (منطقية أو رقمية أو نصية)</span><span class="sxs-lookup"><span data-stu-id="19558-117">`option N`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="19558-118">تعبير صالح يقوم بإرجاع قيمة نفس أنواع البيانات الأساسية مثل وسيطة `expression` للوظيفة التي تم استدعاؤها.</span><span class="sxs-lookup"><span data-stu-id="19558-118">A valid expression that returns a value of the same primitive data type as the `expression` argument of the called function.</span></span> <span data-ttu-id="19558-119">هذه الوسيطة اختيارية.</span><span class="sxs-lookup"><span data-stu-id="19558-119">This argument is optional.</span></span>

<span data-ttu-id="19558-120">`result N`: *أي من أنواع البيانات المعتمدة*</span><span class="sxs-lookup"><span data-stu-id="19558-120">`result N`: *Any of the supported data types*</span></span>

<span data-ttu-id="19558-121">النتيجة التي تم إرجاعها التي تتوافق مع الخيار السابق.</span><span class="sxs-lookup"><span data-stu-id="19558-121">The returned result that corresponds to the preceding option.</span></span> <span data-ttu-id="19558-122">هذه الوسيطة اختيارية.</span><span class="sxs-lookup"><span data-stu-id="19558-122">This argument is optional.</span></span>

<span data-ttu-id="19558-123">`default result`: *أي من أنواع البيانات المعتمدة*</span><span class="sxs-lookup"><span data-stu-id="19558-123">`default result`: *Any of the supported data types*</span></span>

<span data-ttu-id="19558-124">النتيجة التي يجب إرجاعها في حالة عدم وجود تطابق.</span><span class="sxs-lookup"><span data-stu-id="19558-124">The result that should be returned if there is no match.</span></span> <span data-ttu-id="19558-125">هذه الوسيطة اختيارية.</span><span class="sxs-lookup"><span data-stu-id="19558-125">This argument is optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="19558-126">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="19558-126">Return values</span></span>

<span data-ttu-id="19558-127">*أي من أنواع البيانات المدعومة*</span><span class="sxs-lookup"><span data-stu-id="19558-127">*Any of the supported data types*</span></span>

<span data-ttu-id="19558-128">القيمة الناتجة لأي من أنواع البيانات المدعومة.</span><span class="sxs-lookup"><span data-stu-id="19558-128">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="19558-129">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="19558-129">Usage notes</span></span>

<span data-ttu-id="19558-130">يتم طرح استثناء في وقت التشغيل إذا لم يكن هناك تطابق ولم يتم تعريف نتيجة افتراضية اختيارية.</span><span class="sxs-lookup"><span data-stu-id="19558-130">An exception is thrown at runtime if there is no match and an optional default result isn't defined.</span></span>

<span data-ttu-id="19558-131">يجب تحديد كافة النتائج باستخدام نفس نوع البيانات.</span><span class="sxs-lookup"><span data-stu-id="19558-131">All results must be specified by using the same data type.</span></span> <span data-ttu-id="19558-132">يتم طرح استثناء في وقت التصميم إذا لم تتطابق أنواع بيانات النتائج المكونة.</span><span class="sxs-lookup"><span data-stu-id="19558-132">An exception is thrown at design time if the data types of the configured results don't match.</span></span>

<span data-ttu-id="19558-133">إذا كانت قيمة النتيجة الأولى وقيمة النتيجة *N* هي قيم أنواع البيانات *الحاوية (السجل)* أو *قوائم السجلات* ، فإن النتيجة تحتوي فقط على الحقول الموجودة في كلا القيمتين.</span><span class="sxs-lookup"><span data-stu-id="19558-133">If the first result value and the *N* th result value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="19558-134">مثال</span><span class="sxs-lookup"><span data-stu-id="19558-134">Example</span></span>

<span data-ttu-id="19558-135">يُرجع التعبير `CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` السلسلة **"WINTER"** إذا كان تاريخ جلسة عمل التطبيق الحالية بين أكتوبر وديسمبر.</span><span class="sxs-lookup"><span data-stu-id="19558-135">`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` returns the string **"WINTER"** if the current application session date is between October and December.</span></span> <span data-ttu-id="19558-136">وإلا، تقوم بإرجاع سلسلة فارغة.</span><span class="sxs-lookup"><span data-stu-id="19558-136">Otherwise, it returns a blank string.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="19558-137">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="19558-137">Additional resources</span></span>

[<span data-ttu-id="19558-138">الوظائف المنطقية</span><span class="sxs-lookup"><span data-stu-id="19558-138">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]