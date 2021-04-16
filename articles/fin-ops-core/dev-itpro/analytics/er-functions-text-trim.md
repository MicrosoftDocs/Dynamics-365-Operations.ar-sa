---
title: TRIM ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني TRIM (ER).
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 93b08792a7aab7245d0443da05e0330bf8b2d56e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746039"
---
# <a name="trim-er-function"></a><span data-ttu-id="43900-103">TRIM ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="43900-103">TRIM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43900-104">تقوم وظيفة `TRIM` بإرجاع سلسلة النص المُحددة كقيمة *سلسلة* بعد اقتطاع المسافات البادئة والزائدة، وبعد أن تمت إزالة المسافات المتعددة بين الكلمات.</span><span class="sxs-lookup"><span data-stu-id="43900-104">The `TRIM` function returns the specified text string as a *String* value after leading and trailing spaces have been truncated, and after multiple spaces between words have been removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="43900-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="43900-105">Syntax</span></span>

```vb
TRIM (text )
```

## <a name="arguments"></a><span data-ttu-id="43900-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="43900-106">Arguments</span></span>

<span data-ttu-id="43900-107">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="43900-107">`text`: *String*</span></span>

<span data-ttu-id="43900-108">المسار الصالح لمصدر البيانات من نوع *السلسلة*.</span><span class="sxs-lookup"><span data-stu-id="43900-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="43900-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="43900-109">Return values</span></span>

<span data-ttu-id="43900-110">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="43900-110">*String*</span></span>

<span data-ttu-id="43900-111">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="43900-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="43900-112">مثال</span><span class="sxs-lookup"><span data-stu-id="43900-112">Example</span></span>

<span data-ttu-id="43900-113">تُرجع `TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` **"نصًا نموذجيًا"**.</span><span class="sxs-lookup"><span data-stu-id="43900-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` returns **"Sample text"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="43900-114">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="43900-114">Additional resources</span></span>

[<span data-ttu-id="43900-115">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="43900-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]