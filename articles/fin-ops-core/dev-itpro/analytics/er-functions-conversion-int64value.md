---
title: INT64VALUE ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية INT64VALUE (ER).
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
ms.openlocfilehash: 78b69b5280fb8c7ed99d73568097cd0c080a807a
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744829"
---
# <a name="int64value-er-function"></a><span data-ttu-id="0168a-103">INT64VALUE ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="0168a-103">INT64VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0168a-104">تُعيد وظيفة `INT64VALUE` قيمة *Int64* التي تمثل السلسلة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="0168a-104">The `INT64VALUE` function returns an *Int64* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="0168a-105">بناء الجملة 1</span><span class="sxs-lookup"><span data-stu-id="0168a-105">Syntax 1</span></span>

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="0168a-106">بناء الجملة 2</span><span class="sxs-lookup"><span data-stu-id="0168a-106">Syntax 2</span></span>

```vb
INT64VALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="0168a-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="0168a-107">Arguments</span></span>

<span data-ttu-id="0168a-108">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="0168a-108">`text`: *String*</span></span>

<span data-ttu-id="0168a-109">قيمة نصية يجب تحويلها إلى رقم *Int64*.</span><span class="sxs-lookup"><span data-stu-id="0168a-109">A text value that must be converted to an *Int64* number.</span></span>

<span data-ttu-id="0168a-110">`number`: *عدد حقيقي* أو *صحيح*</span><span class="sxs-lookup"><span data-stu-id="0168a-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="0168a-111">قيمة رقمية *حقيقية* أو *عدد صحيح* يجب تحويلها إلى رقم *Int64*.</span><span class="sxs-lookup"><span data-stu-id="0168a-111">A numeric *Real* or *Integer* value that must be converted to an *Int64* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="0168a-112">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="0168a-112">Return values</span></span>

<span data-ttu-id="0168a-113">*Int64*</span><span class="sxs-lookup"><span data-stu-id="0168a-113">*Int64*</span></span>

<span data-ttu-id="0168a-114">القيمة العددية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="0168a-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0168a-115">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="0168a-115">Usage notes</span></span>

<span data-ttu-id="0168a-116">يتم اقتطاع أيٍّ من المنازل العشرية.</span><span class="sxs-lookup"><span data-stu-id="0168a-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="0168a-117">مثال1</span><span class="sxs-lookup"><span data-stu-id="0168a-117">Example 1</span></span>

<span data-ttu-id="0168a-118">يُرجع `INT64VALUE ("22565422744")` قيمة *Int64* **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="0168a-118">`INT64VALUE ("22565422744")` returns the *Int64* value **22565422744**.</span></span>

## <a name="example-2"></a><span data-ttu-id="0168a-119">مثال2</span><span class="sxs-lookup"><span data-stu-id="0168a-119">Example 2</span></span>

<span data-ttu-id="0168a-120">يُرجع `INT64VALUE ( VALUE("22565422744.77"))` قيمة *Int64* **‎22565422744**.</span><span class="sxs-lookup"><span data-stu-id="0168a-120">`INT64VALUE ( VALUE("22565422744.77"))` returns the *Int64* value **22565422744**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0168a-121">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="0168a-121">Additional resources</span></span>

[<span data-ttu-id="0168a-122">وظائف تحويل النوع</span><span class="sxs-lookup"><span data-stu-id="0168a-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
