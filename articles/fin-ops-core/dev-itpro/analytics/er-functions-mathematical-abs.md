---
title: ABS ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية ABS (ER).
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3c7156b9990397822a6bea9ed8b3df8f65490572
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683271"
---
# <a name="abs-er-function"></a><span data-ttu-id="2ddc2-103">ABS ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="2ddc2-103">ABS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ddc2-104">تُرجع الوظيفة `ABS` القيمة المُطلقة (للمعاملات) للرقم المُحدد كقيمة *حقيقة*.</span><span class="sxs-lookup"><span data-stu-id="2ddc2-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="2ddc2-105">وبمعني آخر، يقوم بإرجاع الرقم دون إشارته.</span><span class="sxs-lookup"><span data-stu-id="2ddc2-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ddc2-106">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="2ddc2-106">Syntax</span></span>

```vb
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="2ddc2-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="2ddc2-107">Arguments</span></span>

<span data-ttu-id="2ddc2-108">`number`: *حقيقي*</span><span class="sxs-lookup"><span data-stu-id="2ddc2-108">`number`: *Real*</span></span>

<span data-ttu-id="2ddc2-109">القيمة الرقمية التي تُريدها من المعاملات.</span><span class="sxs-lookup"><span data-stu-id="2ddc2-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="2ddc2-110">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="2ddc2-110">Return values</span></span>

<span data-ttu-id="2ddc2-111">*حقيقي*</span><span class="sxs-lookup"><span data-stu-id="2ddc2-111">*Real*</span></span>

<span data-ttu-id="2ddc2-112">القيمة العددية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="2ddc2-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="2ddc2-113">مثال</span><span class="sxs-lookup"><span data-stu-id="2ddc2-113">Example</span></span>

<span data-ttu-id="2ddc2-114">يُرجع التعبير `ABS (-1)` **1**.</span><span class="sxs-lookup"><span data-stu-id="2ddc2-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2ddc2-115">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="2ddc2-115">Additional resources</span></span>

[<span data-ttu-id="2ddc2-116">الدالات الحسابية</span><span class="sxs-lookup"><span data-stu-id="2ddc2-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)
