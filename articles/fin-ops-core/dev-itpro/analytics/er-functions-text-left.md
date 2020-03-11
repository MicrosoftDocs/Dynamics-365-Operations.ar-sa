---
title: وظيفة LEFT ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة LEFT ER.
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
ms.openlocfilehash: 4293db244d04debf3679cf2bde0b892bd74e8ead
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041114"
---
# <span data-ttu-id="1c2ce-103"><a name="LEFT">وظيفة LEFT ER</a></span><span class="sxs-lookup"><span data-stu-id="1c2ce-103"><a name="LEFT">LEFT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1c2ce-104">تُرجع وظيفة `LEFT` قيمة *السلسلة* التي توضح العدد المُحدد من الأحرف من بداية السلسلة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="1c2ce-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c2ce-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="1c2ce-105">Syntax</span></span>

```vb
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="1c2ce-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="1c2ce-106">Arguments</span></span>

<span data-ttu-id="1c2ce-107">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="1c2ce-107">`text`: *String*</span></span>

<span data-ttu-id="1c2ce-108">قيمة *سلسلة* التي تمثل النص الأصلي.</span><span class="sxs-lookup"><span data-stu-id="1c2ce-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="1c2ce-109">`number`: *عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="1c2ce-109">`number`: *Integer*</span></span>

<span data-ttu-id="1c2ce-110">عدد الأحرف التي يجب إرجاعها من بداية النص الأصلي.</span><span class="sxs-lookup"><span data-stu-id="1c2ce-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="1c2ce-111">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="1c2ce-111">Return values</span></span>

<span data-ttu-id="1c2ce-112">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="1c2ce-112">*String*</span></span>

<span data-ttu-id="1c2ce-113">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="1c2ce-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="1c2ce-114">مثال</span><span class="sxs-lookup"><span data-stu-id="1c2ce-114">Example</span></span>

<span data-ttu-id="1c2ce-115">تُرجع `LEFT ("Sample", 3)` **"Sam"**.</span><span class="sxs-lookup"><span data-stu-id="1c2ce-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1c2ce-116">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="1c2ce-116">Additional resources</span></span>

[<span data-ttu-id="1c2ce-117">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="1c2ce-117">Text functions</span></span>](er-functions-category-text.md)
