---
title: وظيفة LEFT ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة LEFT ER.
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
ms.openlocfilehash: 69b1d95ea0e82b1947b665b0724cff6c5b319633
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746329"
---
# <a name="left-er-function"></a><span data-ttu-id="7e051-103">وظيفة LEFT ER</span><span class="sxs-lookup"><span data-stu-id="7e051-103">LEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7e051-104">تُرجع وظيفة `LEFT` قيمة *السلسلة* التي توضح العدد المُحدد من الأحرف من بداية السلسلة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="7e051-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e051-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="7e051-105">Syntax</span></span>

```vb
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="7e051-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="7e051-106">Arguments</span></span>

<span data-ttu-id="7e051-107">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="7e051-107">`text`: *String*</span></span>

<span data-ttu-id="7e051-108">قيمة *سلسلة* التي تمثل النص الأصلي.</span><span class="sxs-lookup"><span data-stu-id="7e051-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="7e051-109">`number`: *عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="7e051-109">`number`: *Integer*</span></span>

<span data-ttu-id="7e051-110">عدد الأحرف التي يجب إرجاعها من بداية النص الأصلي.</span><span class="sxs-lookup"><span data-stu-id="7e051-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="7e051-111">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="7e051-111">Return values</span></span>

<span data-ttu-id="7e051-112">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="7e051-112">*String*</span></span>

<span data-ttu-id="7e051-113">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="7e051-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="7e051-114">مثال</span><span class="sxs-lookup"><span data-stu-id="7e051-114">Example</span></span>

<span data-ttu-id="7e051-115">تُرجع `LEFT ("Sample", 3)` **"Sam"**.</span><span class="sxs-lookup"><span data-stu-id="7e051-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7e051-116">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="7e051-116">Additional resources</span></span>

[<span data-ttu-id="7e051-117">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="7e051-117">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]