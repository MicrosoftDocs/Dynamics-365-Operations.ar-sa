---
title: UPPER ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية Upper (ER).
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
ms.openlocfilehash: 672abf4938df7d96c0190bfd5325689b381e2764
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744325"
---
# <a name="upper-er-function"></a><span data-ttu-id="334ee-103">UPPER ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="334ee-103">UPPER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="334ee-104">تقوم وظيفة `UPPER` بإرجاع سلسلة النص المُحددة كقيمة *سلسلة* بعد أن تم تحويلها إلى أحرف كبيرة.</span><span class="sxs-lookup"><span data-stu-id="334ee-104">The `UPPER` function returns the specified text string as a *String* value after it has been converted to uppercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="334ee-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="334ee-105">Syntax</span></span>

```vb
UPPER (text )
```

## <a name="arguments"></a><span data-ttu-id="334ee-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="334ee-106">Arguments</span></span>

<span data-ttu-id="334ee-107">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="334ee-107">`text`: *String*</span></span>

<span data-ttu-id="334ee-108">المسار الصالح لمصدر البيانات من نوع *السلسلة*.</span><span class="sxs-lookup"><span data-stu-id="334ee-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="334ee-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="334ee-109">Return values</span></span>

<span data-ttu-id="334ee-110">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="334ee-110">*String*</span></span>

<span data-ttu-id="334ee-111">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="334ee-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="334ee-112">مثال</span><span class="sxs-lookup"><span data-stu-id="334ee-112">Example</span></span>

<span data-ttu-id="334ee-113">تُرجع `UPPER ("Sample")` **"SAMPLE"**.</span><span class="sxs-lookup"><span data-stu-id="334ee-113">`UPPER ("Sample")` returns **"SAMPLE"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="334ee-114">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="334ee-114">Additional resources</span></span>

[<span data-ttu-id="334ee-115">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="334ee-115">Text functions</span></span>](er-functions-category-text.md)
