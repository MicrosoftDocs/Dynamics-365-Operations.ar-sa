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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3e594138ef8e28f1b3aaf333026fa8f9e55cca0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688331"
---
# <a name="upper-er-function"></a><span data-ttu-id="5d98a-103">UPPER ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="5d98a-103">UPPER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5d98a-104">تقوم وظيفة `UPPER` بإرجاع سلسلة النص المُحددة كقيمة *سلسلة* بعد أن تم تحويلها إلى أحرف كبيرة.</span><span class="sxs-lookup"><span data-stu-id="5d98a-104">The `UPPER` function returns the specified text string as a *String* value after it has been converted to uppercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d98a-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="5d98a-105">Syntax</span></span>

```vb
UPPER (text )
```

## <a name="arguments"></a><span data-ttu-id="5d98a-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="5d98a-106">Arguments</span></span>

<span data-ttu-id="5d98a-107">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="5d98a-107">`text`: *String*</span></span>

<span data-ttu-id="5d98a-108">المسار الصالح لمصدر البيانات من نوع *السلسلة*.</span><span class="sxs-lookup"><span data-stu-id="5d98a-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="5d98a-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="5d98a-109">Return values</span></span>

<span data-ttu-id="5d98a-110">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="5d98a-110">*String*</span></span>

<span data-ttu-id="5d98a-111">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="5d98a-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="5d98a-112">مثال</span><span class="sxs-lookup"><span data-stu-id="5d98a-112">Example</span></span>

<span data-ttu-id="5d98a-113">تُرجع `UPPER ("Sample")` **"SAMPLE"**.</span><span class="sxs-lookup"><span data-stu-id="5d98a-113">`UPPER ("Sample")` returns **"SAMPLE"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5d98a-114">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="5d98a-114">Additional resources</span></span>

[<span data-ttu-id="5d98a-115">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="5d98a-115">Text functions</span></span>](er-functions-category-text.md)
