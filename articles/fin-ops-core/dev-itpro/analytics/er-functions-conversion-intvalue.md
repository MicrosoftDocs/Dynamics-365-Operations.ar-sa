---
title: 'وظيفة INTVALUE ER  '
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية INTVALUE (ER).
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
ms.openlocfilehash: 2b279de39cf91c3919145735518034fc60cd3341
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917708"
---
# <span data-ttu-id="71756-103"><a name="INTVALUE">وظيفة INTVALUE ER  </a></span><span class="sxs-lookup"><span data-stu-id="71756-103"><a name="INTVALUE">INTVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="71756-104">تُعيد وظيفة `INTVALUE` قيمة *Int* التي تمثل السلسلة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="71756-104">The `INTVALUE` function returns an *Int* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="71756-105">بناء الجملة 1</span><span class="sxs-lookup"><span data-stu-id="71756-105">Syntax 1</span></span>

```
INTVALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="71756-106">بناء الجملة 2</span><span class="sxs-lookup"><span data-stu-id="71756-106">Syntax 2</span></span>

```
INTVALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="71756-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="71756-107">Arguments</span></span>

<span data-ttu-id="71756-108">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="71756-108">`text`: *String*</span></span>

<span data-ttu-id="71756-109">قيمة نصية يجب تحويلها إلى رقم *Int*.</span><span class="sxs-lookup"><span data-stu-id="71756-109">A text value that must be converted to an *Int* number.</span></span>

<span data-ttu-id="71756-110">`number`: *عدد حقيقي* أو *صحيح*</span><span class="sxs-lookup"><span data-stu-id="71756-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="71756-111">قيمة رقمية *حقيقية* أو *عدد صحيح* يجب تحويلها إلى رقم *Int*.</span><span class="sxs-lookup"><span data-stu-id="71756-111">A numeric *Real* or *Integer* value that must be converted to an *Int* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="71756-112">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="71756-112">Return values</span></span>

<span data-ttu-id="71756-113">*Int*</span><span class="sxs-lookup"><span data-stu-id="71756-113">*Int*</span></span>

<span data-ttu-id="71756-114">القيمة العددية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="71756-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="71756-115">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="71756-115">Usage notes</span></span>

<span data-ttu-id="71756-116">يتم اقتطاع أيٍّ من المنازل العشرية.</span><span class="sxs-lookup"><span data-stu-id="71756-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="71756-117">مثال1</span><span class="sxs-lookup"><span data-stu-id="71756-117">Example 1</span></span>

<span data-ttu-id="71756-118">يُرجع `INTVALUE ("100.77")` قيمة *Int* **100**.</span><span class="sxs-lookup"><span data-stu-id="71756-118">`INTVALUE ("100.77")` returns the *Int* value **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="71756-119">مثال2</span><span class="sxs-lookup"><span data-stu-id="71756-119">Example 2</span></span>

<span data-ttu-id="71756-120">يُرجع `INTVALUE (-100.77)` قيمة *Int* **100**.</span><span class="sxs-lookup"><span data-stu-id="71756-120">`INTVALUE (-100.77)` returns the *Int* value **-100**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="71756-121">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="71756-121">Additional resources</span></span>

[<span data-ttu-id="71756-122">وظائف تحويل النوع</span><span class="sxs-lookup"><span data-stu-id="71756-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
