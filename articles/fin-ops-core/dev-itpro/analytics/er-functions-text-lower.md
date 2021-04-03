---
title: وظيفة LOWER ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية LOWER (ER).
author: NickSelin
manager: kfend
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
ms.openlocfilehash: e507a17f5125a3cba0d2434a1aaec0f04f0cd388
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562773"
---
# <a name="lower-er-function"></a><span data-ttu-id="891b1-103">وظيفة LOWER ER</span><span class="sxs-lookup"><span data-stu-id="891b1-103">LOWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="891b1-104">تقوم وظيفة `LOWER` بإرجاع سلسلة النص المُحددة كقيمة *سلسلة* بعد أن تم تحويلها إلى أحرف صغيرة.</span><span class="sxs-lookup"><span data-stu-id="891b1-104">The `LOWER` function returns the specified text string as a *String* value after it has been converted to lowercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="891b1-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="891b1-105">Syntax</span></span>

```vb
LOWER (text)
```

## <a name="arguments"></a><span data-ttu-id="891b1-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="891b1-106">Arguments</span></span>

<span data-ttu-id="891b1-107">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="891b1-107">`text`: *String*</span></span>

<span data-ttu-id="891b1-108">قيمة *سلسلة* التي تُحدد النص.</span><span class="sxs-lookup"><span data-stu-id="891b1-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="891b1-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="891b1-109">Return values</span></span>

<span data-ttu-id="891b1-110">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="891b1-110">*String*</span></span>

<span data-ttu-id="891b1-111">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="891b1-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="891b1-112">مثال</span><span class="sxs-lookup"><span data-stu-id="891b1-112">Example</span></span>

<span data-ttu-id="891b1-113">تُرجع `LOWER ("Sample")` **"sample"**.</span><span class="sxs-lookup"><span data-stu-id="891b1-113">`LOWER ("Sample")` returns **"sample"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="891b1-114">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="891b1-114">Additional resources</span></span>

[<span data-ttu-id="891b1-115">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="891b1-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]