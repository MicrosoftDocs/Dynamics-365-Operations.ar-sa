---
title: وظيفة LEN ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني LEN (ER).
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
ms.openlocfilehash: fce4b5311d84364310b76545a775f1cc8db2fd70
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569958"
---
# <a name="len-er-function"></a><span data-ttu-id="b3e48-103">وظيفة LEN ER</span><span class="sxs-lookup"><span data-stu-id="b3e48-103">LEN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b3e48-104">تُرجع وظيفة `LEN` عدد الأحرف في السلسلة المحددة كقيمة *‏‫عدد صحيح* .</span><span class="sxs-lookup"><span data-stu-id="b3e48-104">The `LEN` function returns the number of characters in the specified string as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3e48-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="b3e48-105">Syntax</span></span>

```vb
LEN (text)
```

## <a name="arguments"></a><span data-ttu-id="b3e48-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="b3e48-106">Arguments</span></span>

<span data-ttu-id="b3e48-107">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="b3e48-107">`text`: *String*</span></span>

<span data-ttu-id="b3e48-108">قيمة *سلسلة* التي تُحدد النص.</span><span class="sxs-lookup"><span data-stu-id="b3e48-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="b3e48-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="b3e48-109">Return values</span></span>

<span data-ttu-id="b3e48-110">*عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="b3e48-110">*Integer*</span></span>

<span data-ttu-id="b3e48-111">القيمة العددية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="b3e48-111">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="b3e48-112">مثال</span><span class="sxs-lookup"><span data-stu-id="b3e48-112">Example</span></span>

<span data-ttu-id="b3e48-113">يُرجع التعبير `LEN ("Sample")` **6**.</span><span class="sxs-lookup"><span data-stu-id="b3e48-113">`LEN ("Sample")` returns **6**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b3e48-114">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="b3e48-114">Additional resources</span></span>

[<span data-ttu-id="b3e48-115">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="b3e48-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]