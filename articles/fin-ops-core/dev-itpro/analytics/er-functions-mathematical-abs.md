---
title: ABS ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية ABS (ER).
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 12165174806395b3c36a1dbb227ed7a86def77b1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565774"
---
# <a name="abs-er-function"></a><span data-ttu-id="7ad76-103">ABS ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="7ad76-103">ABS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7ad76-104">تُرجع الوظيفة `ABS` القيمة المُطلقة (للمعاملات) للرقم المُحدد كقيمة *حقيقة*.</span><span class="sxs-lookup"><span data-stu-id="7ad76-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="7ad76-105">وبمعني آخر، يقوم بإرجاع الرقم دون إشارته.</span><span class="sxs-lookup"><span data-stu-id="7ad76-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ad76-106">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="7ad76-106">Syntax</span></span>

```vb
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="7ad76-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="7ad76-107">Arguments</span></span>

<span data-ttu-id="7ad76-108">`number`: *حقيقي*</span><span class="sxs-lookup"><span data-stu-id="7ad76-108">`number`: *Real*</span></span>

<span data-ttu-id="7ad76-109">القيمة الرقمية التي تُريدها من المعاملات.</span><span class="sxs-lookup"><span data-stu-id="7ad76-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="7ad76-110">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="7ad76-110">Return values</span></span>

<span data-ttu-id="7ad76-111">*حقيقي*</span><span class="sxs-lookup"><span data-stu-id="7ad76-111">*Real*</span></span>

<span data-ttu-id="7ad76-112">القيمة العددية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="7ad76-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="7ad76-113">مثال</span><span class="sxs-lookup"><span data-stu-id="7ad76-113">Example</span></span>

<span data-ttu-id="7ad76-114">يُرجع التعبير `ABS (-1)` **1**.</span><span class="sxs-lookup"><span data-stu-id="7ad76-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7ad76-115">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="7ad76-115">Additional resources</span></span>

[<span data-ttu-id="7ad76-116">الدالات الحسابية</span><span class="sxs-lookup"><span data-stu-id="7ad76-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]