---
title: 'وظيفة ROUNDAMOUNT ER '
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية ROUNDAMOUNT (ER).
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
ms.openlocfilehash: c68933352da1f9c7dc5dad76e8635981f8a89fce
ms.sourcegitcommit: 9291e6dc0de076a16684980e528c5aa98845bb34
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2918969"
---
# <span data-ttu-id="5d0ee-103"><a name="ROUNDAMOUNT">وظيفة ROUNDAMOUNT ER </a></span><span class="sxs-lookup"><span data-stu-id="5d0ee-103"><a name="ROUNDAMOUNT">ROUNDAMOUNT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5d0ee-104">تُرجع الوظيفة `ROUNDAMOUNT` قيمة *حقيقية* كنتيجة لتقريب الرقم المُحدد إلى أقرب مضاعف لرقم آخر وفقًا لقاعدة التقريب المُحددة.</span><span class="sxs-lookup"><span data-stu-id="5d0ee-104">The `ROUNDAMOUNT` function returns a *Real* value as the result of the rounding of the specified number to the nearest multiple of another number according to the specified rounding rule.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d0ee-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="5d0ee-105">Syntax</span></span>

```
ROUNDAMOUNT (number, decimals, round rule)
```

## <a name="arguments"></a><span data-ttu-id="5d0ee-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="5d0ee-106">Arguments</span></span>

<span data-ttu-id="5d0ee-107">`number`: *عدد صحيح* أو *حقيقي*</span><span class="sxs-lookup"><span data-stu-id="5d0ee-107">`number`: *Int* or *Real*</span></span>

<span data-ttu-id="5d0ee-108">قيمة رقمية يجب تقريبها.</span><span class="sxs-lookup"><span data-stu-id="5d0ee-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="5d0ee-109">`decimals`: *عدد صحيح* أو *حقيقي*</span><span class="sxs-lookup"><span data-stu-id="5d0ee-109">`decimals`: *Int* or *Real*</span></span>

<span data-ttu-id="5d0ee-110">الرقم الذي يجب تقريب قيمة مُعلمة `number` إلى مضاعفه.</span><span class="sxs-lookup"><span data-stu-id="5d0ee-110">The number that the value of the `number` parameter must be rounded to a multiple of.</span></span>

<span data-ttu-id="5d0ee-111">`round rule`: *قيمة التعداد*</span><span class="sxs-lookup"><span data-stu-id="5d0ee-111">`round rule`: *Enum value*</span></span>

<span data-ttu-id="5d0ee-112">قيمة التعداد لتعداد **RoundOffType** التي تُعرف قاعدة التقريب.</span><span class="sxs-lookup"><span data-stu-id="5d0ee-112">An enumeration value of the **RoundOffType** enumeration that defines the rounding rule.</span></span> <span data-ttu-id="5d0ee-113">يعرض هذا التعداد القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="5d0ee-113">This enumeration offers the following values:</span></span>

- <span data-ttu-id="5d0ee-114">عادي (عادي)</span><span class="sxs-lookup"><span data-stu-id="5d0ee-114">Normal (Ordinary)</span></span>
- <span data-ttu-id="5d0ee-115">انحداري (انحداري)</span><span class="sxs-lookup"><span data-stu-id="5d0ee-115">Downward (RoundDown)</span></span>
- <span data-ttu-id="5d0ee-116">التقريب (التقريب)</span><span class="sxs-lookup"><span data-stu-id="5d0ee-116">Rounding-up (RoundUp)</span></span>

## <a name="return-values"></a><span data-ttu-id="5d0ee-117">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="5d0ee-117">Return values</span></span>

<span data-ttu-id="5d0ee-118">*حقيقي*</span><span class="sxs-lookup"><span data-stu-id="5d0ee-118">*Real*</span></span>

<span data-ttu-id="5d0ee-119">القيمة الرقمية الناتجة هي مضاعف للقيمة المُحدد بواسطة المُعلمة `decimals` وهي الأقرب إلى القيمة المُحددة بواسطة المُعلمة `number`.</span><span class="sxs-lookup"><span data-stu-id="5d0ee-119">The resulting numeric value is a multiple of the value specified by the `decimals` parameter and is closest to the value specified by the `number` parameter.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="5d0ee-120">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="5d0ee-120">Usage notes</span></span>

<span data-ttu-id="5d0ee-121">عندما تكون المُعلمة `number` صفر، تُرجع هذه الوظيفة دومًا صفر.</span><span class="sxs-lookup"><span data-stu-id="5d0ee-121">When the `number` parameter is zero, this function always returns zero.</span></span>

<span data-ttu-id="5d0ee-122">عندما تكون المُعلمة `decimals` صفر، تُقرب هذه الوظيفة إلى قيمة التقريب الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="5d0ee-122">When the `decimals` parameter is zero, this function rounds to the default round-off value.</span></span> <span data-ttu-id="5d0ee-123">عندما يتم تعيين مُعلمة `round rule` إلى **RoundOffType.Ordinary** ، تكون قيمة التقريب الافتراضية هي **0.01**. </span><span class="sxs-lookup"><span data-stu-id="5d0ee-123">When the `round rule` parameter is set to **RoundOffType.Ordinary**, the default round-off value is **0.01**.</span></span> <span data-ttu-id="5d0ee-124">وبخلاف ذلك، تكون قيمة التقريب الافتراضية هي **1.0**.</span><span class="sxs-lookup"><span data-stu-id="5d0ee-124">Otherwise, the default round-off value is **1.0**.</span></span>

<span data-ttu-id="5d0ee-125">عند تعيين المُعلمة `round rule` إلى **RoundOffType.Ordinary** ، تُقرب هذه الوظيفة إلى أقرب مبلغ تقريب. </span><span class="sxs-lookup"><span data-stu-id="5d0ee-125">When the `round rule` parameter is set to **RoundOffType.Ordinary**, this function rounds to the nearest round-off amount.</span></span>

<span data-ttu-id="5d0ee-126">عند تعيين المُعلمة `round rule` إلى **RoundOffType.RoundDown** ، تُقرب هذه الوظيفة في اتجاه الصفر إلى أقرب مبلغ تقريب.</span><span class="sxs-lookup"><span data-stu-id="5d0ee-126">When the `round rule` parameter is set to **RoundOffType.RoundDown**, this function rounds towards zero to the nearest round-off amount.</span></span>

<span data-ttu-id="5d0ee-127">عند تعيين المُعلمة `round rule` إلى **RoundOffType.RoundUp** ، تُقرب هذه الوظيفة بعيدًا عن اتجاه الصفر إلى أقرب مبلغ تقريب.</span><span class="sxs-lookup"><span data-stu-id="5d0ee-127">When the `round rule` parameter is set to **RoundOffType.RoundUp**, this function rounds away from zero to the nearest round-off amount.</span></span>

<span data-ttu-id="5d0ee-128">عند تعيين المُعلمة `round rule` إلى **RoundOffType.Ordinary** ، تتصرف هذه الوظيفة مثل وظيفة Excel [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) ووظيفة X++ [ROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round).</span><span class="sxs-lookup"><span data-stu-id="5d0ee-128">When the `round rule` parameter is set to **RoundOffType.Ordinary**, this function behaves like the [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel function and the [ROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round) X++ function.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d0ee-129">ملاحظات</span><span class="sxs-lookup"><span data-stu-id="5d0ee-129">Remarks</span></span>

<span data-ttu-id="5d0ee-130">لتقريب قيمة رقمية إلى رقم محدد من المنازل العشرية، استخدم وظيفة [ROUND](er-functions-mathematical-round.md).</span><span class="sxs-lookup"><span data-stu-id="5d0ee-130">To round a numeric value to a specified number of decimal places, use the [ROUND](er-functions-mathematical-round.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="5d0ee-131">مثال</span><span class="sxs-lookup"><span data-stu-id="5d0ee-131">Example</span></span>

<span data-ttu-id="5d0ee-132">إذا تم تعيين المعلمة **model.RoundOff** إلى **RoundOffType.Ordinary** ، تٌرجع `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 7.35. </span><span class="sxs-lookup"><span data-stu-id="5d0ee-132">If the **model.RoundOff** parameter is set to **RoundOffType.Ordinary**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 7.35.</span></span> 

<span data-ttu-id="5d0ee-133">إذا تم تعيين المعلمة **model.RoundOff** إلى **RoundOffType.RoundDown** ، تٌرجع `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 7.35. </span><span class="sxs-lookup"><span data-stu-id="5d0ee-133">If the **model.RoundOff** parameter is set to **RoundOffType.RoundDown**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 7.35.</span></span> 

<span data-ttu-id="5d0ee-134">إذا تم تعيين المعلمة **model.RoundOff** إلى **RoundOffType.RoundUp** ، تٌرجع `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 8.4. </span><span class="sxs-lookup"><span data-stu-id="5d0ee-134">If the **model.RoundOff** parameter is set to **RoundOffType.RoundUp**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 8.4.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5d0ee-135">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="5d0ee-135">Additional resources</span></span>

[<span data-ttu-id="5d0ee-136">دالات أخرى (خاصة بمجال الأعمال)</span><span class="sxs-lookup"><span data-stu-id="5d0ee-136">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)

[<span data-ttu-id="5d0ee-137">الدالات الحسابية</span><span class="sxs-lookup"><span data-stu-id="5d0ee-137">Mathematical functions</span></span>](er-functions-category-mathematical.md)