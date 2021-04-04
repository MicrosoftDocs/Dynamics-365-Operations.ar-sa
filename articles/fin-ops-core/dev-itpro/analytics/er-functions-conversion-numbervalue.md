---
title: 'وظيفة NUMBERVALUE ER '
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية NUMBERVALUE (ER).
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: f542621c4bcc29e03d8c92b0c700e2c80c9846f6
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561412"
---
# <a name="numbervalue-er-function"></a><span data-ttu-id="c3c8a-103">وظيفة NUMBERVALUE ER</span><span class="sxs-lookup"><span data-stu-id="c3c8a-103">NUMBERVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c3c8a-104">تُرجع الوظيفة `NUMBERVALUE` قيمة *حقيقية* يتم تحويلها من قيمة *السلسلة* المُحددة.</span><span class="sxs-lookup"><span data-stu-id="c3c8a-104">The `NUMBERVALUE` function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="c3c8a-105">في أثناء التحويل، يوضع في الاعتبار فواصل التجميع العشرية والرقمية المُحددة.</span><span class="sxs-lookup"><span data-stu-id="c3c8a-105">During the conversion, the specified decimal and digit grouping separators are considered.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3c8a-106">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="c3c8a-106">Syntax</span></span>

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a><span data-ttu-id="c3c8a-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="c3c8a-107">Arguments</span></span>

<span data-ttu-id="c3c8a-108">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="c3c8a-108">`text`: *String*</span></span>

<span data-ttu-id="c3c8a-109">قيمة نصية يجب تحويلها إلى رقم *حقيقي*.</span><span class="sxs-lookup"><span data-stu-id="c3c8a-109">A text value that must be converted to a *Real* number.</span></span>

<span data-ttu-id="c3c8a-110">`decimal separator`: السلسلة</span><span class="sxs-lookup"><span data-stu-id="c3c8a-110">`decimal separator`: String</span></span>

<span data-ttu-id="c3c8a-111">فاصل عشري.</span><span class="sxs-lookup"><span data-stu-id="c3c8a-111">A decimal separator.</span></span> <span data-ttu-id="c3c8a-112">يُستخدم لفصل العدد الصحيح والأجزاء الكسرية لرقم عشري.</span><span class="sxs-lookup"><span data-stu-id="c3c8a-112">It's used to separate the integer and fractional parts of a decimal number.</span></span>

<span data-ttu-id="c3c8a-113">`digit grouping separator`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="c3c8a-113">`digit grouping separator`: *String*</span></span>

<span data-ttu-id="c3c8a-114">فاصل تجميع أرقام.</span><span class="sxs-lookup"><span data-stu-id="c3c8a-114">A digit grouping separator.</span></span> <span data-ttu-id="c3c8a-115">يُستخدم كفاصل آلاف.</span><span class="sxs-lookup"><span data-stu-id="c3c8a-115">It's used as the thousands separator.</span></span>

## <a name="return-values"></a><span data-ttu-id="c3c8a-116">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="c3c8a-116">Return values</span></span>

<span data-ttu-id="c3c8a-117">*حقيقي*</span><span class="sxs-lookup"><span data-stu-id="c3c8a-117">*Real*</span></span>

<span data-ttu-id="c3c8a-118">القيمة العددية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="c3c8a-118">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="c3c8a-119">مثال</span><span class="sxs-lookup"><span data-stu-id="c3c8a-119">Example</span></span>

<span data-ttu-id="c3c8a-120">يُرجع التعبير `NUMBERVALUE( "1 234,56", ",", " ")` **1234.56**.</span><span class="sxs-lookup"><span data-stu-id="c3c8a-120">`NUMBERVALUE( "1 234,56", ",", " ")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c3c8a-121">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="c3c8a-121">Additional resources</span></span>

[<span data-ttu-id="c3c8a-122">وظائف تحويل النوع</span><span class="sxs-lookup"><span data-stu-id="c3c8a-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]