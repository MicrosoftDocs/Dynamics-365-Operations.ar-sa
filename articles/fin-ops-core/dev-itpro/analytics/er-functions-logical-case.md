---
title: CASE ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية CASE (ER).
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 3bba9cd190db61fda3636cc3c8093030f886b9bd
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041758"
---
# <span data-ttu-id="ebfc5-103"><a name="CASE">CASE ER وظيفة</a></span><span class="sxs-lookup"><span data-stu-id="ebfc5-103"><a name="CASE">CASE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ebfc5-104">تٌقيّم الوظيفة `CASE` قيمة التعبير المُحدد في مقابل الخيارات البديلة المُحددة، وترجع نتيجة الخيار الأول الذي يساوي قيمة التعبير المُحدد.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-104">The `CASE` function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="ebfc5-105">وإلا، فإنه يقوم بإرجاع النتيجة الافتراضية الاختيارية، إذا كانت النتيجة الافتراضية مُحدد كآخر وسيطة للوظيفة التي تم استدعائها والتي لم يسبقها خيار.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-105">Otherwise, it returns the optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="ebfc5-106">يُمكن أن تكون القيمة التي يتم إرجاعها قيمة من أي أنواع بيانات مدعومة.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebfc5-107">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="ebfc5-107">Syntax</span></span>

```vb
CASE (expression, option 1, result 1[, option 2, result 2, …, option N, result N, default result])
```

## <a name="arguments"></a><span data-ttu-id="ebfc5-108">الوسائط</span><span class="sxs-lookup"><span data-stu-id="ebfc5-108">Arguments</span></span>

<span data-ttu-id="ebfc5-109">`expression`: *نوع البيانات الأساسية* (منطقية أو رقمية أو نصية)</span><span class="sxs-lookup"><span data-stu-id="ebfc5-109">`expression`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="ebfc5-110">تعبير صالح يقوم بإرجاع قيمة نوع البيانات الأساسية.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-110">A valid expression that returns a value of the primitive data type.</span></span>

<span data-ttu-id="ebfc5-111">`option 1`: *نوع البيانات الأساسية* (منطقية أو رقمية أو نصية)</span><span class="sxs-lookup"><span data-stu-id="ebfc5-111">`option 1`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="ebfc5-112">تعبير صالح يقوم بإرجاع قيمة نفس أنواع البيانات الأساسية مثل وسيطة `expression` للوظيفة التي تم استدعاؤها.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-112">A valid expression that returns a value of the same primitive data type as the `expression` argument of the called function.</span></span> <span data-ttu-id="ebfc5-113">هذه الوسيطة مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-113">This argument is required.</span></span>

<span data-ttu-id="ebfc5-114">`result 1`: *أي من أنواع البيانات المعتمدة*</span><span class="sxs-lookup"><span data-stu-id="ebfc5-114">`result 1`: *Any of the supported data types*</span></span>

<span data-ttu-id="ebfc5-115">النتيجة التي تم إرجاعها التي تتوافق مع الخيار السابق.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-115">The returned result that corresponds to the preceding option.</span></span> <span data-ttu-id="ebfc5-116">هذه الوسيطة مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-116">This argument is required.</span></span>

<span data-ttu-id="ebfc5-117">`option N`: *نوع البيانات الأساسية* (منطقية أو رقمية أو نصية)</span><span class="sxs-lookup"><span data-stu-id="ebfc5-117">`option N`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="ebfc5-118">تعبير صالح يقوم بإرجاع قيمة نفس أنواع البيانات الأساسية مثل وسيطة `expression` للوظيفة التي تم استدعاؤها.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-118">A valid expression that returns a value of the same primitive data type as the `expression` argument of the called function.</span></span> <span data-ttu-id="ebfc5-119">هذه الوسيطة اختيارية.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-119">This argument is optional.</span></span>

<span data-ttu-id="ebfc5-120">`result N`: *أي من أنواع البيانات المعتمدة*</span><span class="sxs-lookup"><span data-stu-id="ebfc5-120">`result N`: *Any of the supported data types*</span></span>

<span data-ttu-id="ebfc5-121">النتيجة التي تم إرجاعها التي تتوافق مع الخيار السابق.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-121">The returned result that corresponds to the preceding option.</span></span> <span data-ttu-id="ebfc5-122">هذه الوسيطة اختيارية.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-122">This argument is optional.</span></span>

<span data-ttu-id="ebfc5-123">`default result`: *أي من أنواع البيانات المعتمدة*</span><span class="sxs-lookup"><span data-stu-id="ebfc5-123">`default result`: *Any of the supported data types*</span></span>

<span data-ttu-id="ebfc5-124">النتيجة التي يجب إرجاعها في حالة عدم وجود تطابق.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-124">The result that should be returned if there is no match.</span></span> <span data-ttu-id="ebfc5-125">هذه الوسيطة اختيارية.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-125">This argument is optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="ebfc5-126">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="ebfc5-126">Return values</span></span>

<span data-ttu-id="ebfc5-127">*أي من أنواع البيانات المدعومة*</span><span class="sxs-lookup"><span data-stu-id="ebfc5-127">*Any of the supported data types*</span></span>

<span data-ttu-id="ebfc5-128">القيمة الناتجة لأي من أنواع البيانات المدعومة.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-128">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ebfc5-129">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="ebfc5-129">Usage notes</span></span>

<span data-ttu-id="ebfc5-130">يتم طرح استثناء في وقت التشغيل إذا لم يكن هناك تطابق ولم يتم تعريف نتيجة افتراضية اختيارية.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-130">An exception is thrown at runtime if there is no match and an optional default result isn't defined.</span></span>

<span data-ttu-id="ebfc5-131">يجب تحديد كافة النتائج باستخدام نفس نوع البيانات.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-131">All results must be specified by using the same data type.</span></span> <span data-ttu-id="ebfc5-132">يتم طرح استثناء في وقت التصميم إذا لم تتطابق أنواع بيانات النتائج المكونة.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-132">An exception is thrown at design time if the data types of the configured results don't match.</span></span>

<span data-ttu-id="ebfc5-133">إذا كانت قيمة النتيجة الأولى وقيمة النتيجة *N* هي قيم أنواع البيانات *الحاوية (السجل)* أو *قوائم السجلات* ، فإن النتيجة تحتوي فقط على الحقول الموجودة في كلا القيمتين.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-133">If the first result value and the *N*th result value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="ebfc5-134">مثال</span><span class="sxs-lookup"><span data-stu-id="ebfc5-134">Example</span></span>

<span data-ttu-id="ebfc5-135">يُرجع التعبير `CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` السلسلة **"WINTER"** إذا كان تاريخ جلسة عمل التطبيق الحالية بين أكتوبر وديسمبر.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-135">`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` returns the string **"WINTER"** if the current application session date is between October and December.</span></span> <span data-ttu-id="ebfc5-136">وإلا، تقوم بإرجاع سلسلة فارغة.</span><span class="sxs-lookup"><span data-stu-id="ebfc5-136">Otherwise, it returns a blank string.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ebfc5-137">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="ebfc5-137">Additional resources</span></span>

[<span data-ttu-id="ebfc5-138">الوظائف المنطقية</span><span class="sxs-lookup"><span data-stu-id="ebfc5-138">Logical functions</span></span>](er-functions-category-logical.md)
