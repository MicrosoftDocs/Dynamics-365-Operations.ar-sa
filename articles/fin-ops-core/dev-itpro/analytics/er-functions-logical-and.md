---
title: AND ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية AND (ER).
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: dd9c0ed0238009f70ad7a9bf5a5e19ebfb95cccc
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917156"
---
# <span data-ttu-id="2235a-103"><a name="AND">AND ER وظيفة</a></span><span class="sxs-lookup"><span data-stu-id="2235a-103"><a name="AND">AND ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2235a-104">تُرجع الوظيفة `AND` قيمة *منطقية* لـ **TRUE** إذا كانت جميع الشروط المُحددة صحيحة.</span><span class="sxs-lookup"><span data-stu-id="2235a-104">The `AND` function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="2235a-105">وبخلاف ذلك، تُرجع قيمة *منطقية* لـ **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="2235a-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2235a-106">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="2235a-106">Syntax</span></span>

```
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="2235a-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="2235a-107">Arguments</span></span>

<span data-ttu-id="2235a-108">`condition 1`: *منطقي*</span><span class="sxs-lookup"><span data-stu-id="2235a-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="2235a-109">تعبير شرطي صالح يجب اختباره.</span><span class="sxs-lookup"><span data-stu-id="2235a-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="2235a-110">هذه الوسيطة مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="2235a-110">This argument is required.</span></span>

<span data-ttu-id="2235a-111">`condition N`: *منطقي*</span><span class="sxs-lookup"><span data-stu-id="2235a-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="2235a-112">تعبير شرطي صالح يجب اختباره.</span><span class="sxs-lookup"><span data-stu-id="2235a-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="2235a-113">هذه الوسائط الإضافية اختيارية.</span><span class="sxs-lookup"><span data-stu-id="2235a-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="2235a-114">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="2235a-114">Return values</span></span>

<span data-ttu-id="2235a-115">*منطقي*</span><span class="sxs-lookup"><span data-stu-id="2235a-115">*Boolean*</span></span>

<span data-ttu-id="2235a-116">القيمة *المنطقية* الناتجة.</span><span class="sxs-lookup"><span data-stu-id="2235a-116">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2235a-117">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="2235a-117">Usage notes</span></span>

<span data-ttu-id="2235a-118">في وسيطات الوظائف المنطقية، يُمكنك استخدام مراجع مصادر البيانات والقيم الرقمية والنصية والقيم المنطقية وعوامل تشغيل المقارنة ووظائف التقارير الإلكترونية (ER) الأخرى.</span><span class="sxs-lookup"><span data-stu-id="2235a-118">In the arguments of logical functions, you can use data source references, numeric and text values, Boolean values, comparison operators, and other Electronic reporting (ER) functions.</span></span> <span data-ttu-id="2235a-119">ولكن، يجب تقييم كافة الوسيطات إلى قيمة *منطقية* **TRUE** أو **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="2235a-119">However, all the arguments must be evaluated to a *Boolean* value of **TRUE** or **FALSE**.</span></span>

## <a name="example"></a><span data-ttu-id="2235a-120">مثال</span><span class="sxs-lookup"><span data-stu-id="2235a-120">Example</span></span>

<span data-ttu-id="2235a-121">يُرجع التعبير `AND (1=1, "a"="a")` **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="2235a-121">`AND (1=1, "a"="a")` returns **TRUE**.</span></span>

<span data-ttu-id="2235a-122">يُرجع التعبير `AND (1=2, "a"="a")` **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="2235a-122">`AND (1=2, "a"="a")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2235a-123">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="2235a-123">Additional resources</span></span>

[<span data-ttu-id="2235a-124">الوظائف المنطقية</span><span class="sxs-lookup"><span data-stu-id="2235a-124">Logical functions</span></span>](er-functions-category-logical.md)
