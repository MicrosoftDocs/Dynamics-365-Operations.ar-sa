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
ms.openlocfilehash: b016feb0c907ef384eae91840791c357d61cf634
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916811"
---
# <span data-ttu-id="4b0a4-103"><a name="LOWER">وظيفة LOWER ER</a></span><span class="sxs-lookup"><span data-stu-id="4b0a4-103"><a name="LOWER">LOWER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4b0a4-104">تقوم وظيفة `LOWER` بإرجاع سلسلة النص المُحددة كقيمة *سلسلة* بعد أن تم تحويلها إلى أحرف صغيرة.</span><span class="sxs-lookup"><span data-stu-id="4b0a4-104">The `LOWER` function returns the specified text string as a *String* value after it has been converted to lowercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b0a4-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="4b0a4-105">Syntax</span></span>

```
LOWER (text)
```

## <a name="arguments"></a><span data-ttu-id="4b0a4-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="4b0a4-106">Arguments</span></span>

<span data-ttu-id="4b0a4-107">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="4b0a4-107">`text`: *String*</span></span>

<span data-ttu-id="4b0a4-108">قيمة *سلسلة* التي تُحدد النص.</span><span class="sxs-lookup"><span data-stu-id="4b0a4-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="4b0a4-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="4b0a4-109">Return values</span></span>

<span data-ttu-id="4b0a4-110">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="4b0a4-110">*String*</span></span>

<span data-ttu-id="4b0a4-111">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="4b0a4-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="4b0a4-112">مثال</span><span class="sxs-lookup"><span data-stu-id="4b0a4-112">Example</span></span>

<span data-ttu-id="4b0a4-113">تُرجع `LOWER ("Sample")` **"sample"**.</span><span class="sxs-lookup"><span data-stu-id="4b0a4-113">`LOWER ("Sample")` returns **"sample"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4b0a4-114">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="4b0a4-114">Additional resources</span></span>

[<span data-ttu-id="4b0a4-115">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="4b0a4-115">Text functions</span></span>](er-functions-category-text.md)
