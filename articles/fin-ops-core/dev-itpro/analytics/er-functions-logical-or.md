---
title: OR ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية OR (ER).
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
ms.openlocfilehash: 2a850b1cbe7224ab1a7b2bd39ac4667304781cbb
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041666"
---
# <span data-ttu-id="ec5a5-103"><a name="OR">OR ER وظيفة</a></span><span class="sxs-lookup"><span data-stu-id="ec5a5-103"><a name="OR">OR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec5a5-104">تُرجع الوظيفة `OR` قيمة *منطقية* **FALSE** إذا كانت جميع الشروط المُحددة خطأ.</span><span class="sxs-lookup"><span data-stu-id="ec5a5-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="ec5a5-105">إذا كانت أي من الشروط المُحددة صحيحة، تُرجع هذه الوظيفة قيمة *منطقية* **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="ec5a5-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec5a5-106">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="ec5a5-106">Syntax</span></span>

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="ec5a5-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="ec5a5-107">Arguments</span></span>

<span data-ttu-id="ec5a5-108">`condition 1`: *منطقي*</span><span class="sxs-lookup"><span data-stu-id="ec5a5-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="ec5a5-109">تعبير شرطي صالح يجب اختباره.</span><span class="sxs-lookup"><span data-stu-id="ec5a5-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="ec5a5-110">هذه الوسيطة مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="ec5a5-110">This argument is required.</span></span>

<span data-ttu-id="ec5a5-111">`condition N`: *منطقي*</span><span class="sxs-lookup"><span data-stu-id="ec5a5-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="ec5a5-112">تعبير شرطي صالح يجب اختباره.</span><span class="sxs-lookup"><span data-stu-id="ec5a5-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="ec5a5-113">هذه الوسائط الإضافية اختيارية.</span><span class="sxs-lookup"><span data-stu-id="ec5a5-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="ec5a5-114">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="ec5a5-114">Return values</span></span>

<span data-ttu-id="ec5a5-115">*منطقي*</span><span class="sxs-lookup"><span data-stu-id="ec5a5-115">*Boolean*</span></span>

<span data-ttu-id="ec5a5-116">القيمة *المنطقية* الناتجة.</span><span class="sxs-lookup"><span data-stu-id="ec5a5-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="ec5a5-117">مثال</span><span class="sxs-lookup"><span data-stu-id="ec5a5-117">Example</span></span>

<span data-ttu-id="ec5a5-118">يُرجع التعبير `OR (1=2, "a"="a")` **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="ec5a5-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ec5a5-119">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="ec5a5-119">Additional resources</span></span>

[<span data-ttu-id="ec5a5-120">الوظائف المنطقية</span><span class="sxs-lookup"><span data-stu-id="ec5a5-120">Logical functions</span></span>](er-functions-category-logical.md)
