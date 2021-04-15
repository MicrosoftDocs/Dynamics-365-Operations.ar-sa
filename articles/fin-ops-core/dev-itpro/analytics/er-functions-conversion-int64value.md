---
title: INT64VALUE ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية INT64VALUE (ER).
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
ms.openlocfilehash: 89a26e867579bcb34a9bae33fa0b98e1ecfe9995
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755386"
---
# <a name="int64value-er-function"></a><span data-ttu-id="cb593-103">INT64VALUE ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="cb593-103">INT64VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb593-104">تُعيد وظيفة `INT64VALUE` قيمة *Int64* التي تمثل السلسلة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="cb593-104">The `INT64VALUE` function returns an *Int64* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="cb593-105">بناء الجملة 1</span><span class="sxs-lookup"><span data-stu-id="cb593-105">Syntax 1</span></span>

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="cb593-106">بناء الجملة 2</span><span class="sxs-lookup"><span data-stu-id="cb593-106">Syntax 2</span></span>

```vb
INT64VALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="cb593-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="cb593-107">Arguments</span></span>

<span data-ttu-id="cb593-108">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="cb593-108">`text`: *String*</span></span>

<span data-ttu-id="cb593-109">قيمة نصية يجب تحويلها إلى رقم *Int64*.</span><span class="sxs-lookup"><span data-stu-id="cb593-109">A text value that must be converted to an *Int64* number.</span></span>

<span data-ttu-id="cb593-110">`number`: *عدد حقيقي* أو *صحيح*</span><span class="sxs-lookup"><span data-stu-id="cb593-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="cb593-111">قيمة رقمية *حقيقية* أو *عدد صحيح* يجب تحويلها إلى رقم *Int64*.</span><span class="sxs-lookup"><span data-stu-id="cb593-111">A numeric *Real* or *Integer* value that must be converted to an *Int64* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="cb593-112">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="cb593-112">Return values</span></span>

<span data-ttu-id="cb593-113">*Int64*</span><span class="sxs-lookup"><span data-stu-id="cb593-113">*Int64*</span></span>

<span data-ttu-id="cb593-114">القيمة العددية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="cb593-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="cb593-115">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="cb593-115">Usage notes</span></span>

<span data-ttu-id="cb593-116">يتم اقتطاع أيٍّ من المنازل العشرية.</span><span class="sxs-lookup"><span data-stu-id="cb593-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="cb593-117">مثال1</span><span class="sxs-lookup"><span data-stu-id="cb593-117">Example 1</span></span>

<span data-ttu-id="cb593-118">يُرجع `INT64VALUE ("22565422744")` قيمة *Int64* **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="cb593-118">`INT64VALUE ("22565422744")` returns the *Int64* value **22565422744**.</span></span>

## <a name="example-2"></a><span data-ttu-id="cb593-119">مثال2</span><span class="sxs-lookup"><span data-stu-id="cb593-119">Example 2</span></span>

<span data-ttu-id="cb593-120">يُرجع `INT64VALUE ( VALUE("22565422744.77"))` قيمة *Int64* **‎22565422744**.</span><span class="sxs-lookup"><span data-stu-id="cb593-120">`INT64VALUE ( VALUE("22565422744.77"))` returns the *Int64* value **22565422744**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cb593-121">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="cb593-121">Additional resources</span></span>

[<span data-ttu-id="cb593-122">وظائف تحويل النوع</span><span class="sxs-lookup"><span data-stu-id="cb593-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]