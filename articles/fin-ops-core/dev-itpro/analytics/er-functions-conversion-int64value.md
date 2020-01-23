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
ms.openlocfilehash: 75df802b75454baeea75a8ceb32d5d045a77a3a0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916535"
---
# <span data-ttu-id="d0380-103"><a name="INT64VALUE">INT64VALUE ER وظيفة</a></span><span class="sxs-lookup"><span data-stu-id="d0380-103"><a name="INT64VALUE">INT64VALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d0380-104">تُعيد وظيفة `INT64VALUE` قيمة *Int64* التي تمثل السلسلة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="d0380-104">The `INT64VALUE` function returns an *Int64* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="d0380-105">بناء الجملة 1</span><span class="sxs-lookup"><span data-stu-id="d0380-105">Syntax 1</span></span>

```
INT64VALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="d0380-106">بناء الجملة 2</span><span class="sxs-lookup"><span data-stu-id="d0380-106">Syntax 2</span></span>

```
INT64VALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="d0380-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="d0380-107">Arguments</span></span>

<span data-ttu-id="d0380-108">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="d0380-108">`text`: *String*</span></span>

<span data-ttu-id="d0380-109">قيمة نصية يجب تحويلها إلى رقم *Int64*.</span><span class="sxs-lookup"><span data-stu-id="d0380-109">A text value that must be converted to an *Int64* number.</span></span>

<span data-ttu-id="d0380-110">`number`: *عدد حقيقي* أو *صحيح*</span><span class="sxs-lookup"><span data-stu-id="d0380-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="d0380-111">قيمة رقمية *حقيقية* أو *عدد صحيح* يجب تحويلها إلى رقم *Int64*.</span><span class="sxs-lookup"><span data-stu-id="d0380-111">A numeric *Real* or *Integer* value that must be converted to an *Int64* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="d0380-112">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="d0380-112">Return values</span></span>

<span data-ttu-id="d0380-113">*Int64*</span><span class="sxs-lookup"><span data-stu-id="d0380-113">*Int64*</span></span>

<span data-ttu-id="d0380-114">القيمة العددية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="d0380-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d0380-115">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="d0380-115">Usage notes</span></span>

<span data-ttu-id="d0380-116">يتم اقتطاع أيٍّ من المنازل العشرية.</span><span class="sxs-lookup"><span data-stu-id="d0380-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="d0380-117">مثال1</span><span class="sxs-lookup"><span data-stu-id="d0380-117">Example 1</span></span>

<span data-ttu-id="d0380-118">يُرجع `INT64VALUE ("22565422744")` قيمة *Int64* **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="d0380-118">`INT64VALUE ("22565422744")` returns the *Int64* value **22565422744**.</span></span>

## <a name="example-2"></a><span data-ttu-id="d0380-119">مثال2</span><span class="sxs-lookup"><span data-stu-id="d0380-119">Example 2</span></span>

<span data-ttu-id="d0380-120">يُرجع `INT64VALUE ( VALUE("22565422744.77"))` قيمة *Int64* **‎22565422744**.</span><span class="sxs-lookup"><span data-stu-id="d0380-120">`INT64VALUE ( VALUE("22565422744.77"))` returns the *Int64* value **22565422744**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d0380-121">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="d0380-121">Additional resources</span></span>

[<span data-ttu-id="d0380-122">وظائف تحويل النوع</span><span class="sxs-lookup"><span data-stu-id="d0380-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
