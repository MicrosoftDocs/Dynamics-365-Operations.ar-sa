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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad971bd78fa1da17be916efcc6857aa32575f7ac
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680304"
---
# <a name="lower-er-function"></a><span data-ttu-id="48265-103">وظيفة LOWER ER</span><span class="sxs-lookup"><span data-stu-id="48265-103">LOWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="48265-104">تقوم وظيفة `LOWER` بإرجاع سلسلة النص المُحددة كقيمة *سلسلة* بعد أن تم تحويلها إلى أحرف صغيرة.</span><span class="sxs-lookup"><span data-stu-id="48265-104">The `LOWER` function returns the specified text string as a *String* value after it has been converted to lowercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="48265-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="48265-105">Syntax</span></span>

```vb
LOWER (text)
```

## <a name="arguments"></a><span data-ttu-id="48265-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="48265-106">Arguments</span></span>

<span data-ttu-id="48265-107">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="48265-107">`text`: *String*</span></span>

<span data-ttu-id="48265-108">قيمة *سلسلة* التي تُحدد النص.</span><span class="sxs-lookup"><span data-stu-id="48265-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="48265-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="48265-109">Return values</span></span>

<span data-ttu-id="48265-110">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="48265-110">*String*</span></span>

<span data-ttu-id="48265-111">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="48265-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="48265-112">مثال</span><span class="sxs-lookup"><span data-stu-id="48265-112">Example</span></span>

<span data-ttu-id="48265-113">تُرجع `LOWER ("Sample")` **"sample"**.</span><span class="sxs-lookup"><span data-stu-id="48265-113">`LOWER ("Sample")` returns **"sample"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="48265-114">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="48265-114">Additional resources</span></span>

[<span data-ttu-id="48265-115">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="48265-115">Text functions</span></span>](er-functions-category-text.md)
