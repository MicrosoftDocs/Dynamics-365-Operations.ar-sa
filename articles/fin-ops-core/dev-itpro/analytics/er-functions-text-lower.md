---
title: وظيفة LOWER ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية LOWER (ER).
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
ms.openlocfilehash: 12577e571c8e87db79395895e2a22e66ee7df32c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745671"
---
# <a name="lower-er-function"></a><span data-ttu-id="8e648-103">وظيفة LOWER ER</span><span class="sxs-lookup"><span data-stu-id="8e648-103">LOWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8e648-104">تقوم وظيفة `LOWER` بإرجاع سلسلة النص المُحددة كقيمة *سلسلة* بعد أن تم تحويلها إلى أحرف صغيرة.</span><span class="sxs-lookup"><span data-stu-id="8e648-104">The `LOWER` function returns the specified text string as a *String* value after it has been converted to lowercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e648-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="8e648-105">Syntax</span></span>

```vb
LOWER (text)
```

## <a name="arguments"></a><span data-ttu-id="8e648-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="8e648-106">Arguments</span></span>

<span data-ttu-id="8e648-107">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="8e648-107">`text`: *String*</span></span>

<span data-ttu-id="8e648-108">قيمة *سلسلة* التي تُحدد النص.</span><span class="sxs-lookup"><span data-stu-id="8e648-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="8e648-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="8e648-109">Return values</span></span>

<span data-ttu-id="8e648-110">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="8e648-110">*String*</span></span>

<span data-ttu-id="8e648-111">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="8e648-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="8e648-112">مثال</span><span class="sxs-lookup"><span data-stu-id="8e648-112">Example</span></span>

<span data-ttu-id="8e648-113">تُرجع `LOWER ("Sample")` **"sample"**.</span><span class="sxs-lookup"><span data-stu-id="8e648-113">`LOWER ("Sample")` returns **"sample"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8e648-114">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="8e648-114">Additional resources</span></span>

[<span data-ttu-id="8e648-115">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="8e648-115">Text functions</span></span>](er-functions-category-text.md)
