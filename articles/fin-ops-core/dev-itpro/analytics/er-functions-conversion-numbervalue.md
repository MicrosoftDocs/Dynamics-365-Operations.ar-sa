---
title: 'وظيفة NUMBERVALUE ER '
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية NUMBERVALUE (ER).
author: NickSelin
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
ms.openlocfilehash: 84d7f17f37a83547522cf09047b72100f6f5b859
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755338"
---
# <a name="numbervalue-er-function"></a><span data-ttu-id="0f890-103">وظيفة NUMBERVALUE ER</span><span class="sxs-lookup"><span data-stu-id="0f890-103">NUMBERVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f890-104">تُرجع الوظيفة `NUMBERVALUE` قيمة *حقيقية* يتم تحويلها من قيمة *السلسلة* المُحددة.</span><span class="sxs-lookup"><span data-stu-id="0f890-104">The `NUMBERVALUE` function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="0f890-105">في أثناء التحويل، يوضع في الاعتبار فواصل التجميع العشرية والرقمية المُحددة.</span><span class="sxs-lookup"><span data-stu-id="0f890-105">During the conversion, the specified decimal and digit grouping separators are considered.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f890-106">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="0f890-106">Syntax</span></span>

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a><span data-ttu-id="0f890-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="0f890-107">Arguments</span></span>

<span data-ttu-id="0f890-108">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="0f890-108">`text`: *String*</span></span>

<span data-ttu-id="0f890-109">قيمة نصية يجب تحويلها إلى رقم *حقيقي*.</span><span class="sxs-lookup"><span data-stu-id="0f890-109">A text value that must be converted to a *Real* number.</span></span>

<span data-ttu-id="0f890-110">`decimal separator`: السلسلة</span><span class="sxs-lookup"><span data-stu-id="0f890-110">`decimal separator`: String</span></span>

<span data-ttu-id="0f890-111">فاصل عشري.</span><span class="sxs-lookup"><span data-stu-id="0f890-111">A decimal separator.</span></span> <span data-ttu-id="0f890-112">يُستخدم لفصل العدد الصحيح والأجزاء الكسرية لرقم عشري.</span><span class="sxs-lookup"><span data-stu-id="0f890-112">It's used to separate the integer and fractional parts of a decimal number.</span></span>

<span data-ttu-id="0f890-113">`digit grouping separator`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="0f890-113">`digit grouping separator`: *String*</span></span>

<span data-ttu-id="0f890-114">فاصل تجميع أرقام.</span><span class="sxs-lookup"><span data-stu-id="0f890-114">A digit grouping separator.</span></span> <span data-ttu-id="0f890-115">يُستخدم كفاصل آلاف.</span><span class="sxs-lookup"><span data-stu-id="0f890-115">It's used as the thousands separator.</span></span>

## <a name="return-values"></a><span data-ttu-id="0f890-116">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="0f890-116">Return values</span></span>

<span data-ttu-id="0f890-117">*حقيقي*</span><span class="sxs-lookup"><span data-stu-id="0f890-117">*Real*</span></span>

<span data-ttu-id="0f890-118">القيمة العددية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="0f890-118">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="0f890-119">مثال</span><span class="sxs-lookup"><span data-stu-id="0f890-119">Example</span></span>

<span data-ttu-id="0f890-120">يُرجع التعبير `NUMBERVALUE( "1 234,56", ",", " ")` **1234.56**.</span><span class="sxs-lookup"><span data-stu-id="0f890-120">`NUMBERVALUE( "1 234,56", ",", " ")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0f890-121">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="0f890-121">Additional resources</span></span>

[<span data-ttu-id="0f890-122">وظائف تحويل النوع</span><span class="sxs-lookup"><span data-stu-id="0f890-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]