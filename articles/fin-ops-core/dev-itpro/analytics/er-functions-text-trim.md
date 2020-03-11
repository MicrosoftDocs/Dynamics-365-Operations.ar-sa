---
title: TRIM ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني TRIM (ER).
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
ms.openlocfilehash: c95663f1aacaf93c1c4bfc8d36d9515f495bf61e
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040815"
---
# <span data-ttu-id="30617-103"><a name="TRIM">TRIM ER وظيفة</a></span><span class="sxs-lookup"><span data-stu-id="30617-103"><a name="TRIM">TRIM ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="30617-104">تقوم وظيفة `TRIM` بإرجاع سلسلة النص المُحددة كقيمة *سلسلة* بعد اقتطاع المسافات البادئة والزائدة، وبعد أن تمت إزالة المسافات المتعددة بين الكلمات.</span><span class="sxs-lookup"><span data-stu-id="30617-104">The `TRIM` function returns the specified text string as a *String* value after leading and trailing spaces have been truncated, and after multiple spaces between words have been removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="30617-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="30617-105">Syntax</span></span>

```vb
TRIM (text )
```

## <a name="arguments"></a><span data-ttu-id="30617-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="30617-106">Arguments</span></span>

<span data-ttu-id="30617-107">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="30617-107">`text`: *String*</span></span>

<span data-ttu-id="30617-108">المسار الصالح لمصدر البيانات من نوع *السلسلة*.</span><span class="sxs-lookup"><span data-stu-id="30617-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="30617-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="30617-109">Return values</span></span>

<span data-ttu-id="30617-110">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="30617-110">*String*</span></span>

<span data-ttu-id="30617-111">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="30617-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="30617-112">مثال</span><span class="sxs-lookup"><span data-stu-id="30617-112">Example</span></span>

<span data-ttu-id="30617-113">تُرجع `TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` **"نصًا نموذجيًا"**.</span><span class="sxs-lookup"><span data-stu-id="30617-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` returns **"Sample text"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="30617-114">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="30617-114">Additional resources</span></span>

[<span data-ttu-id="30617-115">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="30617-115">Text functions</span></span>](er-functions-category-text.md)
