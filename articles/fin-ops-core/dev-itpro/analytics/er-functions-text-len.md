---
title: وظيفة LEN ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني LEN (ER).
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
ms.openlocfilehash: e51e181de53cd185679110e99b9f89695bacdf92
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744253"
---
# <a name="len-er-function"></a><span data-ttu-id="e0cf1-103">وظيفة LEN ER</span><span class="sxs-lookup"><span data-stu-id="e0cf1-103">LEN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e0cf1-104">تُرجع وظيفة `LEN` عدد الأحرف في السلسلة المحددة كقيمة *‏‫عدد صحيح* .</span><span class="sxs-lookup"><span data-stu-id="e0cf1-104">The `LEN` function returns the number of characters in the specified string as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0cf1-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="e0cf1-105">Syntax</span></span>

```vb
LEN (text)
```

## <a name="arguments"></a><span data-ttu-id="e0cf1-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="e0cf1-106">Arguments</span></span>

<span data-ttu-id="e0cf1-107">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-107">`text`: *String*</span></span>

<span data-ttu-id="e0cf1-108">قيمة *سلسلة* التي تُحدد النص.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="e0cf1-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="e0cf1-109">Return values</span></span>

<span data-ttu-id="e0cf1-110">*عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="e0cf1-110">*Integer*</span></span>

<span data-ttu-id="e0cf1-111">القيمة العددية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-111">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="e0cf1-112">مثال</span><span class="sxs-lookup"><span data-stu-id="e0cf1-112">Example</span></span>

<span data-ttu-id="e0cf1-113">يُرجع التعبير `LEN ("Sample")` **6**.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-113">`LEN ("Sample")` returns **6**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e0cf1-114">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="e0cf1-114">Additional resources</span></span>

[<span data-ttu-id="e0cf1-115">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="e0cf1-115">Text functions</span></span>](er-functions-category-text.md)
