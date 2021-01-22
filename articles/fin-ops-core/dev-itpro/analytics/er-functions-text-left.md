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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 112852ab955fdf8de9f78cc93486cc1d5f048517
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743773"
---
# <a name="left-er-function"></a><span data-ttu-id="391d5-103">وظيفة LEFT ER</span><span class="sxs-lookup"><span data-stu-id="391d5-103">LEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="391d5-104">تُرجع وظيفة `LEFT` قيمة *السلسلة* التي توضح العدد المُحدد من الأحرف من بداية السلسلة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="391d5-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="391d5-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="391d5-105">Syntax</span></span>

```vb
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="391d5-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="391d5-106">Arguments</span></span>

<span data-ttu-id="391d5-107">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="391d5-107">`text`: *String*</span></span>

<span data-ttu-id="391d5-108">قيمة *سلسلة* التي تمثل النص الأصلي.</span><span class="sxs-lookup"><span data-stu-id="391d5-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="391d5-109">`number`: *عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="391d5-109">`number`: *Integer*</span></span>

<span data-ttu-id="391d5-110">عدد الأحرف التي يجب إرجاعها من بداية النص الأصلي.</span><span class="sxs-lookup"><span data-stu-id="391d5-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="391d5-111">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="391d5-111">Return values</span></span>

<span data-ttu-id="391d5-112">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="391d5-112">*String*</span></span>

<span data-ttu-id="391d5-113">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="391d5-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="391d5-114">مثال</span><span class="sxs-lookup"><span data-stu-id="391d5-114">Example</span></span>

<span data-ttu-id="391d5-115">تُرجع `LEFT ("Sample", 3)` **"Sam"**.</span><span class="sxs-lookup"><span data-stu-id="391d5-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="391d5-116">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="391d5-116">Additional resources</span></span>

[<span data-ttu-id="391d5-117">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="391d5-117">Text functions</span></span>](er-functions-category-text.md)