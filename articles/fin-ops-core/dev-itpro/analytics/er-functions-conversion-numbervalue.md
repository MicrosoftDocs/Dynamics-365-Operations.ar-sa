---
title: 'وظيفة NUMBERVALUE ER '
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية NUMBERVALUE (ER).
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 13346c4810d6c93d4ef47ce525831332562c7f51
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743389"
---
# <a name="numbervalue-er-function"></a><span data-ttu-id="d068a-103">وظيفة NUMBERVALUE ER</span><span class="sxs-lookup"><span data-stu-id="d068a-103">NUMBERVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d068a-104">تُرجع الوظيفة `NUMBERVALUE` قيمة *حقيقية* يتم تحويلها من قيمة *السلسلة* المُحددة.</span><span class="sxs-lookup"><span data-stu-id="d068a-104">The `NUMBERVALUE` function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="d068a-105">في أثناء التحويل، يوضع في الاعتبار فواصل التجميع العشرية والرقمية المُحددة.</span><span class="sxs-lookup"><span data-stu-id="d068a-105">During the conversion, the specified decimal and digit grouping separators are considered.</span></span>

## <a name="syntax"></a><span data-ttu-id="d068a-106">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="d068a-106">Syntax</span></span>

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a><span data-ttu-id="d068a-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="d068a-107">Arguments</span></span>

<span data-ttu-id="d068a-108">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="d068a-108">`text`: *String*</span></span>

<span data-ttu-id="d068a-109">قيمة نصية يجب تحويلها إلى رقم *حقيقي*.</span><span class="sxs-lookup"><span data-stu-id="d068a-109">A text value that must be converted to a *Real* number.</span></span>

<span data-ttu-id="d068a-110">`decimal separator`: السلسلة</span><span class="sxs-lookup"><span data-stu-id="d068a-110">`decimal separator`: String</span></span>

<span data-ttu-id="d068a-111">فاصل عشري.</span><span class="sxs-lookup"><span data-stu-id="d068a-111">A decimal separator.</span></span> <span data-ttu-id="d068a-112">يُستخدم لفصل العدد الصحيح والأجزاء الكسرية لرقم عشري.</span><span class="sxs-lookup"><span data-stu-id="d068a-112">It's used to separate the integer and fractional parts of a decimal number.</span></span>

<span data-ttu-id="d068a-113">`digit grouping separator`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="d068a-113">`digit grouping separator`: *String*</span></span>

<span data-ttu-id="d068a-114">فاصل تجميع أرقام.</span><span class="sxs-lookup"><span data-stu-id="d068a-114">A digit grouping separator.</span></span> <span data-ttu-id="d068a-115">يُستخدم كفاصل آلاف.</span><span class="sxs-lookup"><span data-stu-id="d068a-115">It's used as the thousands separator.</span></span>

## <a name="return-values"></a><span data-ttu-id="d068a-116">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="d068a-116">Return values</span></span>

<span data-ttu-id="d068a-117">*حقيقي*</span><span class="sxs-lookup"><span data-stu-id="d068a-117">*Real*</span></span>

<span data-ttu-id="d068a-118">القيمة العددية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="d068a-118">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="d068a-119">مثال</span><span class="sxs-lookup"><span data-stu-id="d068a-119">Example</span></span>

<span data-ttu-id="d068a-120">يُرجع التعبير `NUMBERVALUE( "1 234,56", ",", " ")` **1234.56**.</span><span class="sxs-lookup"><span data-stu-id="d068a-120">`NUMBERVALUE( "1 234,56", ",", " ")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d068a-121">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="d068a-121">Additional resources</span></span>

[<span data-ttu-id="d068a-122">وظائف تحويل النوع</span><span class="sxs-lookup"><span data-stu-id="d068a-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
