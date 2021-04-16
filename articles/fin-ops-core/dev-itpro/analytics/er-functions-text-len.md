---
title: وظيفة LEN ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني LEN (ER).
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
ms.openlocfilehash: 394e07a7a573cc4462196b17440f8b0547d8dd48
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746305"
---
# <a name="len-er-function"></a><span data-ttu-id="d7d35-103">وظيفة LEN ER</span><span class="sxs-lookup"><span data-stu-id="d7d35-103">LEN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d7d35-104">تُرجع وظيفة `LEN` عدد الأحرف في السلسلة المحددة كقيمة *‏‫عدد صحيح* .</span><span class="sxs-lookup"><span data-stu-id="d7d35-104">The `LEN` function returns the number of characters in the specified string as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7d35-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="d7d35-105">Syntax</span></span>

```vb
LEN (text)
```

## <a name="arguments"></a><span data-ttu-id="d7d35-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="d7d35-106">Arguments</span></span>

<span data-ttu-id="d7d35-107">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="d7d35-107">`text`: *String*</span></span>

<span data-ttu-id="d7d35-108">قيمة *سلسلة* التي تُحدد النص.</span><span class="sxs-lookup"><span data-stu-id="d7d35-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="d7d35-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="d7d35-109">Return values</span></span>

<span data-ttu-id="d7d35-110">*عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="d7d35-110">*Integer*</span></span>

<span data-ttu-id="d7d35-111">القيمة العددية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="d7d35-111">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="d7d35-112">مثال</span><span class="sxs-lookup"><span data-stu-id="d7d35-112">Example</span></span>

<span data-ttu-id="d7d35-113">يُرجع التعبير `LEN ("Sample")` **6**.</span><span class="sxs-lookup"><span data-stu-id="d7d35-113">`LEN ("Sample")` returns **6**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d7d35-114">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="d7d35-114">Additional resources</span></span>

[<span data-ttu-id="d7d35-115">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="d7d35-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]