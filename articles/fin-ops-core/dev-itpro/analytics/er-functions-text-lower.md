---
title: وظيفة LOWER ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية LOWER (ER).
author: NickSelin
ms.date: 12/11/2019
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
ms.openlocfilehash: e684883d4262e4c3cd8a84d0a1c6f1d685bb650b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746281"
---
# <a name="lower-er-function"></a><span data-ttu-id="b41fa-103">وظيفة LOWER ER</span><span class="sxs-lookup"><span data-stu-id="b41fa-103">LOWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b41fa-104">تقوم وظيفة `LOWER` بإرجاع سلسلة النص المُحددة كقيمة *سلسلة* بعد أن تم تحويلها إلى أحرف صغيرة.</span><span class="sxs-lookup"><span data-stu-id="b41fa-104">The `LOWER` function returns the specified text string as a *String* value after it has been converted to lowercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="b41fa-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="b41fa-105">Syntax</span></span>

```vb
LOWER (text)
```

## <a name="arguments"></a><span data-ttu-id="b41fa-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="b41fa-106">Arguments</span></span>

<span data-ttu-id="b41fa-107">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="b41fa-107">`text`: *String*</span></span>

<span data-ttu-id="b41fa-108">قيمة *سلسلة* التي تُحدد النص.</span><span class="sxs-lookup"><span data-stu-id="b41fa-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="b41fa-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="b41fa-109">Return values</span></span>

<span data-ttu-id="b41fa-110">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="b41fa-110">*String*</span></span>

<span data-ttu-id="b41fa-111">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="b41fa-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="b41fa-112">مثال</span><span class="sxs-lookup"><span data-stu-id="b41fa-112">Example</span></span>

<span data-ttu-id="b41fa-113">تُرجع `LOWER ("Sample")` **"sample"**.</span><span class="sxs-lookup"><span data-stu-id="b41fa-113">`LOWER ("Sample")` returns **"sample"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b41fa-114">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="b41fa-114">Additional resources</span></span>

[<span data-ttu-id="b41fa-115">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="b41fa-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]