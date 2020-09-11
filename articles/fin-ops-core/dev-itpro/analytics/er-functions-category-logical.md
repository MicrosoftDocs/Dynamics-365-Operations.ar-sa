---
title: قائمة وظائف التقارير الإلكترونية في الفئة المنطقية
description: يوفر هذا الموضوع معلومات حول الوظائف المنطقية المعتمدة في التقارير الإلكترونية (ER).
author: NickSelin
manager: kfend
ms.date: 08/19/2020
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
ms.openlocfilehash: e622778c60646e5cc84cd6e23a5d4954a0fe0bb3
ms.sourcegitcommit: 38ad6f791c3d5688a5dc201a234ba89f155f7f03
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/19/2020
ms.locfileid: "3705085"
---
# <a name="list-of-er-functions-in-the-logical-category"></a><span data-ttu-id="fe70e-103">قائمة وظائف التقارير الإلكترونية في الفئة المنطقية</span><span class="sxs-lookup"><span data-stu-id="fe70e-103">List of ER functions in the logical category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fe70e-104">يُمكن استخدام الوظائف المنطقية للتقارير الإلكترونية (ER) للعمل باستخدام القيم المنطقية لإجراء أكثر من مقارنة واحدة في تعبير واحد أو اختبار شروط متعددة.</span><span class="sxs-lookup"><span data-stu-id="fe70e-104">Electronic reporting (ER) logical functions can be used to work with logical values to perform more than one comparison in a single expression or test multiple conditions.</span></span> <span data-ttu-id="fe70e-105">يعرض هذا الموضوع ملخصًا لهذه الوظائف.</span><span class="sxs-lookup"><span data-stu-id="fe70e-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="fe70e-106">قائمة الوظائف المدعومة</span><span class="sxs-lookup"><span data-stu-id="fe70e-106">List of supported functions</span></span>

| <span data-ttu-id="fe70e-107">الوظيفة</span><span class="sxs-lookup"><span data-stu-id="fe70e-107">Function</span></span> | <span data-ttu-id="fe70e-108">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="fe70e-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="fe70e-109">و</span><span class="sxs-lookup"><span data-stu-id="fe70e-109">And</span></span>](er-functions-logical-and.md)                       | <span data-ttu-id="fe70e-110">تُرجع هذه الوظيفة قيمة *منطقية* **TRUE** إذا كانت جميع الشروط المُحددة صحيحة.</span><span class="sxs-lookup"><span data-stu-id="fe70e-110">This function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="fe70e-111">وبخلاف ذلك، تُرجع قيمة *منطقية* لـ **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="fe70e-111">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="fe70e-112">الحالة</span><span class="sxs-lookup"><span data-stu-id="fe70e-112">Case</span></span>](er-functions-logical-case.md)                     | <span data-ttu-id="fe70e-113">تٌقيّم هذه الوظيفة قيمة التعبير المُحدد في مقابل الخيارات البديلة المُحددة، وترجع نتيجة الخيار الأول الذي يساوي قيمة التعبير المُحدد.</span><span class="sxs-lookup"><span data-stu-id="fe70e-113">This function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="fe70e-114">وإلا، فإنه يقوم بإرجاع النتيجة الافتراضية الاختيارية، إذا كانت النتيجة الافتراضية مُحدد كآخر وسيطة للوظيفة التي تم استدعائها والتي لم يسبقها خيار.</span><span class="sxs-lookup"><span data-stu-id="fe70e-114">Otherwise, it returns an optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="fe70e-115">يُمكن أن تكون القيمة التي يتم إرجاعها قيمة من أي أنواع بيانات مدعومة.</span><span class="sxs-lookup"><span data-stu-id="fe70e-115">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="fe70e-116">إذا</span><span class="sxs-lookup"><span data-stu-id="fe70e-116">If</span></span>](er-functions-logical-if.md)                         | <span data-ttu-id="fe70e-117">تُرجع هذه الوظيفة القيمة المُحددة الأولى عند تحقق الشرط المُحدد.</span><span class="sxs-lookup"><span data-stu-id="fe70e-117">This function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="fe70e-118">وإلا، تُرجع القيمة المحددة الثانية.</span><span class="sxs-lookup"><span data-stu-id="fe70e-118">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="fe70e-119">يُمكن أن تكون القيمة التي يتم إرجاعها قيمة من أي أنواع بيانات مدعومة.</span><span class="sxs-lookup"><span data-stu-id="fe70e-119">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="fe70e-120">ليس</span><span class="sxs-lookup"><span data-stu-id="fe70e-120">Not</span></span>](er-functions-logical-not.md)                       | <span data-ttu-id="fe70e-121">ترجع هذه الوظيفة القيمة المنطقية المعكوسة للشرط المُحدد كقيمة *منطقية*.</span><span class="sxs-lookup"><span data-stu-id="fe70e-121">This function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span> |
| [<span data-ttu-id="fe70e-122">Or</span><span class="sxs-lookup"><span data-stu-id="fe70e-122">Or</span></span>](er-functions-logical-or.md)                         | <span data-ttu-id="fe70e-123">تُرجع هذه الوظيفة قيمة *منطقية* **FALSE** إذا كانت جميع الشروط المُحددة خطأ.</span><span class="sxs-lookup"><span data-stu-id="fe70e-123">This function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="fe70e-124">إذا كانت أي من الشروط المُحددة صحيحة، تُرجع هذه الوظيفة قيمة *منطقية* **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="fe70e-124">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span> |
| [<span data-ttu-id="fe70e-125">ValueIn</span><span class="sxs-lookup"><span data-stu-id="fe70e-125">ValueIn</span></span>](er-functions-logical-valuein.md)               | <span data-ttu-id="fe70e-126">تُحدد هذه الوظيفة ما إذا كان الإدخال المُحدد يطابق أي قيمة عنصر مُحدد في القائمة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="fe70e-126">This function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="fe70e-127">يقوم بإرجاع قيمة *منطقية* **TRUE** إذا كان الإدخال المُحدد يُطابق نتيجة تشغيل التعبير المُحدد لسجل واحد على الأقل من القائمة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="fe70e-127">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="fe70e-128">وبخلاف ذلك، تُرجع قيمة *منطقية* لـ **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="fe70e-128">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="fe70e-129">ValueInLarge</span><span class="sxs-lookup"><span data-stu-id="fe70e-129">ValueInLarge</span></span>](er-functions-logical-valueinlarge.md)     | <span data-ttu-id="fe70e-130">تُحدد هذه الوظيفة ما إذا كان الإدخال المُحدد من النوع *Int64* أو *عدد صحيح* يطابق أي قيمة عنصر مُحدد في القائمة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="fe70e-130">This function determines whether the specified input of the *Int64* or *Integer* type matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="fe70e-131">يقوم بإرجاع قيمة *منطقية* **TRUE** إذا كان الإدخال المُحدد يُطابق نتيجة تشغيل التعبير المُحدد لسجل واحد على الأقل من القائمة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="fe70e-131">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="fe70e-132">وبخلاف ذلك، تُرجع قيمة *منطقية* لـ **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="fe70e-132">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |


## <a name="additional-resources"></a><span data-ttu-id="fe70e-133">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="fe70e-133">Additional resources</span></span>

[<span data-ttu-id="fe70e-134">نظرة عامة حول التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="fe70e-134">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="fe70e-135">مصمم المعادلات في التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="fe70e-135">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="fe70e-136">لغة تركيبة التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="fe70e-136">Electronic reporting formula language</span></span>](er-formula-language.md)
