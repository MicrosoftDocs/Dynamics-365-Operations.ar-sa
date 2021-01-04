---
title: وظيفة LEFT ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة LEFT ER.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 9e9cdff9bb5c22c74803cf17c056c0ff1af5ef43
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685873"
---
# <a name="left-er-function"></a><span data-ttu-id="fbd70-103">وظيفة LEFT ER</span><span class="sxs-lookup"><span data-stu-id="fbd70-103">LEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fbd70-104">تُرجع وظيفة `LEFT` قيمة *السلسلة* التي توضح العدد المُحدد من الأحرف من بداية السلسلة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="fbd70-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbd70-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="fbd70-105">Syntax</span></span>

```vb
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="fbd70-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="fbd70-106">Arguments</span></span>

<span data-ttu-id="fbd70-107">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="fbd70-107">`text`: *String*</span></span>

<span data-ttu-id="fbd70-108">قيمة *سلسلة* التي تمثل النص الأصلي.</span><span class="sxs-lookup"><span data-stu-id="fbd70-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="fbd70-109">`number`: *عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="fbd70-109">`number`: *Integer*</span></span>

<span data-ttu-id="fbd70-110">عدد الأحرف التي يجب إرجاعها من بداية النص الأصلي.</span><span class="sxs-lookup"><span data-stu-id="fbd70-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="fbd70-111">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="fbd70-111">Return values</span></span>

<span data-ttu-id="fbd70-112">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="fbd70-112">*String*</span></span>

<span data-ttu-id="fbd70-113">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="fbd70-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="fbd70-114">مثال</span><span class="sxs-lookup"><span data-stu-id="fbd70-114">Example</span></span>

<span data-ttu-id="fbd70-115">تُرجع `LEFT ("Sample", 3)` **"Sam"**.</span><span class="sxs-lookup"><span data-stu-id="fbd70-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fbd70-116">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="fbd70-116">Additional resources</span></span>

[<span data-ttu-id="fbd70-117">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="fbd70-117">Text functions</span></span>](er-functions-category-text.md)
